---
title: Vispārējās plānošanas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar vispārējo plānošanu.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1492854b7d2da480942800e378be9d2bb60bb1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645069"
---
# <a name="troubleshoot-master-planning"></a>Vispārējās plānošanas problēmu novēršana

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar vispārējo plānošanu.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Materiālu komplekta izvēršana darbojas atšķirīgi apstiprinātajiem ražošanas pasūtījumiem un prognozētajiem ražošanas pasūtījumiem manuāli izveidotajam darbam.

### <a name="issue-description"></a>Problēmas apraksts

Kad ražošanas pasūtījums ir apstiprināts, krājumi netiek izvērsti, kad tiek izvērsti materiālu komplekti (MK). Tomēr, kad manuāli veidojat darba pasūtījumu un pēc tam novērtējat ražošanas pasūtījumu, krājumi tiek izvērsti.

### <a name="issue-resolution"></a>Problēmas risinājums

Sistēma darbojas, kā paredzēts. Izvērsums, kas rodas, kad ražošanas pasūtījums ir apstiprināts, norādīs uz plānoto pasūtījumu, bet neparādās, ka šajā gadījumā plānotais pasūtījums pašlaik ir apstiprināts. Tomēr, ja ražošanas pasūtījums ir novērtēts, izvērsums tiek izraisīts no nodotā ražošanas pasūtījuma, kur nepastāv plānotais pasūtījums.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Kavējuma vērtība netiek atjaunināta, pārplānojot plānoto pasūtījumu.

Lai atjauninātu plānoto pasūtījumu kavēšanos, atveriet plānotā pasūtījuma dialoglodziņu **Pārplānošana**. Kopsavilkuma cilnē **Izvēršana** pārliecinieties, ka opcija **Veikt izvēršanu pēc pārplānošanas** ir iestatīts uz *Jā*.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Ražošanas plānošanā netiek ņemtas vērā drošības rezerves, kas iestatītas krājuma segumam piesaistītajai piegādei.

### <a name="issue-description"></a>Problēmas apraksts

Vispārējā plānošanā tiek aplūkotas drošības rezerves. Tomēr drošības rezerves tiek ignorētas, kad ir paredzēti plānoti ražošanas pasūtījumi.

### <a name="issue-resolution"></a>Problēmas risinājums

Rezerves tiek apsvērtas tikai vispārējās plānošanas laikā, nevis manuālajā plānošanā. Rezerves ir paredzētas, lai tā darbotos kā buferis plānošanas fāzes laikā, lai piešķirtu kādam "rezervi" faktiskajam procesam.

Lai iegūtu vēlamo rezultātu, varat noņemt rezervi. Pēc tam maršruts ir jāatjaunina, lai tas ietvertu vēlamo laiku (piemēram, kā gaidīšanas laiku). Tad gan vispārējā plānošana, gan manuālā plānošana uzrāda tādu pašu rezultātu.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Plānotie pasūtījumi tiek ģenerēti, pat ja tiem ir preces krājumos un ražošanas pasūtījumi jau pastāv.

Šo problēmu var novērst, palielinot **Pozitīvo dienu** vērtību attiecīgajām grupām lapā **Pārklājumu grupa**. Šī izmaiņa liks sistēmai noteikt, vai rīcībā esošie krājumi var tikt izmantoti pieprasījumam. Pēc tam krājumos esošām precēm netiks ģenerēts jauns plānotais pasūtījums.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Vispārējai plānošanai nav jāievēro noslodzes ierobežojumi, un tā plānošana ir lielāka par pieejamo noslodzi.

### <a name="issue-description"></a>Problēmas apraksts

Kad izmantojat operāciju plānošanu, kur ir ierobežota noslodze un kur maršruts norāda vajadzību kopumu gan resursu grupai, gan atsevišķiem resursiem, ir neliela iespēja rezervēt vairāk, jo algoritms apstiprina noslodzes konfliktus. Šī rezervēšana var notikt, kad izmantojat palīgus, lai veiktu vispārējo plānošanu. Tas visdrīzāk var notikt, ja ir daudz darbu ar relatīvi īsu izpildlaiku.

### <a name="issue-resolution"></a>Problēmas risinājums

Ja ir svarīgi, lai operāciju plānošana netiktu pārgrāmatota, ieslēdzot opciju **Precīza ierobežota noslodzes operāciju plānošanai** opciju lapā **Vispārējās plānošanas plānošana**. Šī opcija nav pieejama pēc noklusējuma. Tas ir manuāli jāpievieno lapai, izmantojot personalizēšanas līdzekļus. Kad izmantojat šo opciju, plānošana darbosies lēnāk, jo nav paralēlās apstrādes.

## <a name="planned-orders-take-a-long-time-to-update"></a>Plānotajiem pasūtījumiem nepieciešams ilgs laiks, lai atjauninātu.

### <a name="issue-description"></a>Problēmas apraksts

Atjauninot vajadzības daudzumu un/vai piedāvājuma datumu plānotajā pasūtījumā, parasti katrā pasūtījumā ir nepieciešamas vismaz 30 sekundes, lai saglabātu atjauninājumu.

### <a name="issue-resolution"></a>Problēmas risinājums

Šī ir zināma problēma iebūvētajā vispārējās plānošanas programmā. Tas ir saistīts ar pamata automātisko izvēršanu rediģēšanas laikā, izmantojot MK struktūru. Šī problēma ir adresēta Plānošanas optimizācijā, kur plānotājs var atjaunināt un apstiprināt atbilstošos pasūtījumus un, ja nepieciešams, aktivizēt plānošanas izpildi, lai atjauninātu plānotos pasūtījumus pamata MK struktūrai.

Viens no veidiem, kā uzlabot veiktspēju ar iebūvēto vispārējās plānošanas programmu, ir veikt šādas darbības:

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Atlasiet plānu.
1. Izvērsiet kopsavilkuma cilni **Laika robeža dienās**.
1. Iestatiet **Izvēršana** uz *Jā* un iestatiet lauku zem šī iestatījuma uz 0 (nulle).

> [!NOTE]
> Tas ierobežos šim vispārējam plānam veikto sprādzienu periodu uz vienu dienu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]