---
title: Plānošanas optimizācijas paplašināmība
description: Šajā rakstā ir aprakstīti paplašināmības scenāriji, kas tiek atbalstīti optimizācijas plānošanā.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d649110959e6bcfdaeb32dd53c55dbc446ed1be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857549"
---
# <a name="planning-optimization-extensibility"></a>Plānošanas optimizācijas paplašināmība

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīti paplašināmības scenāriji, kas ir saistīti ar vispārējo plānošanu un tiek atbalstīti optimizācijas plānošanā. Šīs iespējas ir pieejamas no Microsoft versijas Dynamics 365 Supply Chain Management 10.0.13.

## <a name="custom-processing-when-master-planning-is-completed"></a>Pielāgota apstrāde pēc vispārējās plānošanas pabeigšanas

Visbiežāk lietotajā paplašināmības scenārijā Plānošanas optimizācijā pielāgotā apstrāde tiek veikta pēc plāna atjaunināšanas. Piemēram, kolonnu var pievienot plānoto pasūtījumu tabulai (`ReqPO`) vai, iespējams, vēlēsieties iegūt statistikas informāciju no ģenerētā plāna. Galvenais paplašināmības punkts, kas iespējo šos scenārijus, ir `jobCompletedSuccessfully` metode `MpsMasterPlanningEvents` klasē.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Šeit parādīts paplašinājuma piemērs, kas iestata pielāgoto `CstmOrderPriority` lauku plānotajā pasūtījumā.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Kad pievienojat pielāgotu loģiku, apsveriet šādus ierobežojumus un labākās prakses:

- Metode `jobCompletedSuccessfully` tiek izsaukta ārpus darbību sfēras. Tāpēc plāns lietotājam jau ir redzams, kad sāk darboties pielāgotā loģika. Ja pielāgošana plānotajiem pasūtījumiem iestata papildu laukus, ir svarīgi ļaut lietotājiem zināt, ka šo lauku vērtības visbeidzot būs konsekventas (citiem vārdiem sakot, tie var būt novajā datumā uzreiz pēc plānošanas darba pabeigšanas).
- Cits vispārējās plānošanas darbs var sākties pēc `jobCompletedSuccessfully` metodes nosaukšanas. Jaunais darbs var ietekmēt visu plānu vai daļu no plāna. Jaunais darbs var atjaunināt vai dzēst tos pašus plānotos pasūtījumus vai pieprasījumu darbības, kas tika izveidotas vai atjauninātas kā daļa no apstrādātā plānošanas darba `jobCompletedSuccessfully`. Ja šis notikums ir paplašināts, jāapstrādā atjaunināšanas konfliktu izņēmumi.
- Paplašinot šo metodi, izvairieties lietot vienas darbības jomu. Vienas vispārējās plānošanas palaišanas laikā var tikt radītas miljonās vajadzības darbības un tūkstošiem tūkstošiem plānoto pasūtījumu. Ja visas šīs darbības un plānotie pasūtījumi tiek apstrādāti vienas darbības ietvaros, veidosies daudzi SQL slēgi un bloķēs citus plānošanas procesus. Turklāt, ja darbība tiek glabāta ilgstoši, SQL datu bāzē tiks izveidoti "pagātnes ieraksti". Pagātnes ieraksti negatīvi ietekmēs katru sistēmas procesu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]