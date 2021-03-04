---
title: Krājumu bloķēšana
description: Šajā tēmā ir sniegts pārskats par krājuma bloķēšanu, kas ir kvalitātes pārbaudes procesa elements Supply Chain Management. Krājuma bloķēšanu var izmantot, lai nepieļautu krājumu apstrādi vai patēriņu.
author: perlynne
manager: tfehr
ms.date: 01/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8807756f16a08f9818f998ce19a8088c7dd37405
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432848"
---
# <a name="inventory-blocking"></a>Krājumu bloķēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par krājuma bloķēšanu, kas ir kvalitātes pārbaudes procesa elements Supply Chain Management. Krājuma bloķēšanu var izmantot, lai nepieļautu krājumu apstrādi vai patēriņu.

Varat bloķēt krājumu vienības tālāk norādītajos veidos.
-   Manuāli
-   Izveidojot kvalitātes pārbaudes pasūtījumu
-   Izmantojot procesu, kas ģenerē kvalitātes pasūtījumu
-   Izmantojot krājuma statusa aizturēšanu

## <a name="blocking-items-manually"></a>Manuāla krājumu aizturēšana
Varat aizturēt noteiktu krājuma daudzumu, izveidojot transakciju lapā **Krājumu aizturēšana**. Manuāli var aizturēt tikai rīcībā esošos krājumus. Attiecībā uz manuāli aizturētajiem daudzumiem jums ir jāizlemj, vai plānošanas aktivitātes ietver paredzētās ieejas plūsmas kā paredzētos rīcībā esošo daudzumu. Paredzētās ieejas plūsmas ir aizturētie krājumi, kas būs pieejami kā rīcībā esošie krājumi pēc pārbaudes pabeigšanas. Varat uzturēt paredzēto datumu. Pēc noklusējuma krājumiem, kas ir aizturēti, izmantojot kvalitātes pārbaudes pasūtījumu, ir atlasīta opcija **Plānotie ieņēmumi**. Varat atcelt manuālu aizturēšanu pēc daudzuma, dzēšot transakciju lapā **Krājumu aizturēšana**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Krājumu aizturēšana, izveidojot kvalitātes pārbaudes pasūtījumu
Var norādīt krājumus, kas ir jāpārbauda, izveidojot kvalitātes pārbaudes pasūtījumu lapā **Kvalitātes pasūtījumi**. Izveidojot kvalitātes pārbaudes pasūtījumu, tiek aizturēts norādītais krājuma daudzums. Ar kvalitātes pārbaudes pasūtījumu saistītais paraugu ņemšanas plāns nosaka tikai pārbaudāmo krājumu daudzumu, nevis aizturēto daudzumu. Kvalitātes pārbaudes pasūtījumā ievadītais daudzums ir aizturētais daudzums neatkarīgi no daudzuma, kas saskaņā ar paraugu ņemšanas plānu ir jānosūta pārbaudei.

> [!NOTE]
> Vispārējā plānošanā netiek atbalstīta gan partijas beigu datuma, gan bloķēšanas krājumu statusa funkciju izmantošana. Tas var novest pie rīcībā esošo krājumu dubultas izslēgšanas, kas var notikt vispārējās plānošanas laikā. Ieteicams paļauties uz partijas atgriešanas kodiem, nevis krājumu statusu, lai bloķētu partijas ar beigušos derīgumu.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Krājumu aizturēšana, izmantojot procesu, kas ģenerē kvalitātes pārbaudes pasūtījumu
Ja kvalitātes pārbaudes procesā ir norādīts, ka krājums ir jāpārbauda, tiek automātiski aizturēts attiecīgs krājuma daudzums. Tāpēc, kad tiek automātiski ģenerēts kvalitātes pārbaudes pasūtījums, ar kvalitātes pārbaudes pasūtījumu saistītais krājuma paraugu ņemšanas plāns nosaka gan aizturēto krājumu daudzumu, gan pārbaudāmo daudzumu. Ja lapā **Krājumu iztveršana** ir atlasīta opcija **Pilna aizturēšana**, pārbaudes laikā tiek aizturēts viss, piemēram, pirkšanas pasūtījuma daudzums neatkarīgi no krājuma paraugu ņemšanas daudzuma.
### <a name="example"></a>Piemērs

Šajā piemērā kvalitātes pārbaudes pasūtījums tiek ģenerēts, kad pirkšanas pasūtījuma pavadzīme ir iegrāmatota. Lapā **Kvalitātes piesaistes** jūs norādījāt, ka kvalitātes pārbaudes pasūtījumu aktivizē pirkšanas pasūtījuma pavadzīmes grāmatošana.

|Iestatīšana                                                                     |Lietotāja darbība                 |Rezultāts             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Kvalitātes saistība nosaka, ka, grāmatojot pirkšanas pasūtījuma pavadzīmi, ir jāģenerē kvalitātes pārbaudes pasūtījums. Kvalitātes pārbaudes pasūtījuma krājuma paraugu ņemšanas iestatījumi nosaka, ka ir jāpārbauda 10% no pirkšanas pasūtījuma rindā norādīta daudzuma. Turklāt, tā kā krājuma paraugu ņemšanas iestatījumos ir atlasīta opcija **Pilna aizturēšana**, pārbaudes laikā ir jāaiztur viss pirkšanas pasūtījuma rindā norādītais daudzums neatkarīgi no pārbaudei nosūtītā daudzuma. | Pavadzīme ir iegrāmatota | Kvalitātes pārbaudes pasūtījums ir izveidots. Pārbaudei tiek nosūtīti desmit procenti no krājuma pirkšanas pasūtījuma daudzuma. Viss pirkšanas pasūtījuma rindu daudzums ir bloķēts. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Krājumu aizturēšana, izmantojot krājuma statusa aizturēšanu
Varat norādīt, kuri krājumu statusi ir aizturēšanas statusi, izmantojot parametru **Krājuma bloķēšana** lapā **Krājumu statusi**. Krājumu statusus nevar izmantot kā ražošanas pasūtījumu, pārdošanas pasūtījumu, pārsūtīšanas pasūtījumu, izejošo transakciju vai projekta integrācijas aizturēšanas statusus. Izejošam darbam izmantojiet vienības, kam krājuma statuss ir Pieejams. Ja krājumu statuss ir **Bojāts** un šiem krājumiem tiek veikta vispārējā plānošana, šie krājumi tiek uzskatīti par trūkstošiem un krājumi tiek automātiski papildināti.



<a name="additional-resources"></a>Papildu resursi
--------

[Izveidot un uzturēt krājuma bloķēšanu](tasks/create-maintain-inventory-blocking.md)

[Kvalitātes pārvaldības procesi](quality-management-processes.md)

[Preču kvalitātes pārbaude](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]