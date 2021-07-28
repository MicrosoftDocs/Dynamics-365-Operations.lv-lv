---
title: Plānošana ar neierobežotu noslodzi
description: Šajā tēmā ir sniegta informācija par neierobežotas noslodzes plānošanu Plānošanas optimizēšanai. Šeit aprakstīti arī pašreizējie funkcionalitātes ierobežojumi.
author: crytt
ms.date: 6/9/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c493522ea55dd7e69c0133aceef43a3e59021c3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361347"
---
# <a name="scheduling-with-infinite-capacity"></a>Plānošana ar neierobežotu noslodzi

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Līdzeklis *Neierobežotās noslodzes Plānošana optimizācija* ievieš plānošanu, kuras pamatā ir maršruta informācija. Tas ļauj plānot darbus, balstoties uz plašu maršruta iestatījumu diapazonu. Plānošana Plānošanas optimizācijai aptver bieži izmantotos maršruta iestatījumus, tostarp maršruta operāciju secību vai maršruta operāciju resursu prasības.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Ieslēgt neierobežotās noslodzes plānošanas līdzekli

Ja sistēmā vēl nav ietverts šajā tēmā aprakstītais līdzeklis, atveriet darbvietu [Līdzekļu pārvaldība](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet līdzekli *Bezgalīga jaudas plānošana Plānošanas optimizācijai*.

## <a name="added-functionality"></a>Pievienota funkcionalitāte

Līdzeklis *Neierobežotās noslodzes Plānošana optimizācija* ļauj plānot darbu, kura pamatā ir maršruta informācija. Tāpēc ražošanas procesu plānošanai var izmantot maršruta iestatījumus. Lai gan šim līdzeklim ir daži ierobežojumi, kuru iebūvētajam pamatplānojumam nav, tas atbalsta visbiežāk sastopamās funkcionalitātes, kas nepieciešamas ražošanas scenārijiem.

Šis līdzeklis apsver gan *vienkāršus maršrutus*, gan *maršruta tīklus*. Izmantojot lauku **Nākošais** maršruta operācijā, varat iestatīt kompleksus maršrutus, kuriem ir vairāki sākuma punkti un vairākas darbības, kas darbojas paralēli. Plānošanas laikā sistēma apsvērs šāda veida sarežģītas maršruta struktūras.

Turklāt līdzeklis atbalsta *paralēlās operācijas* maršrutos. Izmantojot opcijas *Primārais* un *Sekundārais* maršruta operāciju laukā **Prioritāte**, varat definēt maršruta struktūru, kur viena maršruta operācija ir primārā operācija un cita operācija ir sekundāra. Šajā gadījumā plānošanas laikā sistēma ņems vērā maršruta struktūru.

Plānošanas procesa laikā sistēma ņem vērā arī *resursu prasības*, kas noteiktas operācijai. Sistēma izmanto resursu prasības, lai noteiktu, kuri resursi ir nepieciešami darbības veikšanai. Pašlaik līdzeklis *Neierobežotās noslodzes Plānošanas optimizācija* atbalsta šādus resursu pieprasījumu tipus:

- Resursa tips
- Resurss
- Resursa grupa
- Iespēja

> [!NOTE]
> Prasības, kas saistītas ar personāla resursiem, piemēram, prasmju vai sertifikātu prasības, vēl nav atbalstītas.

Līdzeklis atbalsta arī operāciju rekvizītus **Iestatīšanas laiks** un **Izpildes laiks**. Iestatot šos rekvizītus maršruta operācijā, plānošanas process izveidos atbilstošus iestatījumus un apstrādās darbus.

Kopumā Plānošanas optimizācijas plānošana atbalsta visbiežāk izmantotos scenārijus. Varat izveidot maršrutu, pievienot primārās un sekundārās operācijas, definēt nākamās operācijas, pievienot resursu prasības un pievienot uzstādīšanas laiku un izpildes laiku. Tad sistēma šo informāciju ņems vērā plānošanas laikā.

## <a name="limitations"></a>Ierobežojumi

Uz Plānošanas optimizāciju attiecas šādi ierobežojumi:

- Šis lmīdzeklis atbalsta tikai darbu plānošanu. Iestatījumi, kas ir saistīti ar operāciju plānošanu, plānošanas laikā netiek izskatīti neatkarīgi no plānošanas metodes vispārējos plānos.
- Šis līdzeklis atbalsta tikai neierobežotu noslodzi.
- Šis līdzeklis neatbalsta resursu noslodzes funkcionalitāti.
- Šis līdzeklis neietver maršruta brāķi.
- Līdzeklis atbalsta *Ilgumu* tikai kā primāro resursu atlasi.

Ņemiet vērā, ka līdzeklis *Neierobežotās noslodzes Plānošanas optimizācija* ir uzlabots. Microsoft plāno ieviest atbalstu papildu plānošanas iestatījumiem turpmākajos laidienos.
