---
title: "Resursu iespējas"
description: "Šajā rakstā ir sniegta informācija par resursu iespējām. Iespēja ir operācijas resursa pieejamība konkrētas aktivitātes izpildīšanai. Rakstā ir izskaidrots, kā iespējas un saistītās koncepcijas, piemēram, prasmes līmenis un prioritāte, tiek izmantotas, lai atlasītu attiecīgos darbības resursus."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f6b4ccf4d7f9727819831b07221d859e3c5cdd39
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="resource-capabilities"></a>Resursu iespējas

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par resursu iespējām. Iespēja ir operācijas resursa pieejamība konkrētas aktivitātes izpildīšanai. Rakstā ir izskaidrots, kā iespējas un saistītās koncepcijas, piemēram, prasmes līmenis un prioritāte, tiek izmantotas, lai atlasītu attiecīgos darbības resursus.

Iespēja ir operācijas resursu pieejamība konkrētas aktivitātes izpildīšanai. Operācijas resursiem var būt piešķirta vairāk nekā viena iespēja un iespēju var piešķirt vairāk nekā vienam resursam. Varat uz laiku piešķirt iespējas resursiem, definējot iespējas piešķiršanas sākuma un beigu datumu. Beidzoties resursu iespējas darbības termiņam, resursu nevar ieplānot projektam vai ražošanai, kas prasa šo iespēju. Iespēju, kuras termiņš ir beidzies, var atjaunināt. Iespējas var dzēst, ja tās neatrodas aktīva ražošanas pasūtījuma maršruta atsaucē vai ražošanas maršruta daļā. Kopumā, esiet uzmanīgi, dzēšot iespējas. Tā vietā apsveriet iespēju pielāgot resursu, kuriem ir šī iespēja, termiņa beigu datumu. Iespējas var piešķirt visu veidu resursiem: rīkam, kreditoram, iekārtai, novietojumam, iestādei vai cilvēkresursiem.

## <a name="level"></a>Līmenis
Vairākiem resursiem bieži vien ir viena un tā pati funkcionālā iespēja, bet dažādos prasmes līmeņos (piemēram, izturība, apstrādes ātrums vai precizitāte). Tādēļ, piešķirot iespēju resursam, varat norādīt vērtību **Līmenis**. Līmenis ir vienkārša skaitliska vērtība. Ja norādāt, ka iespēja ir resursu prasība ražošanas maršrutam, šai iespējai var arī norādīt vērtību **Minimālais nepieciešamais līmenis**. Pēc tam plānošanas programma atlasa tikai resursus, kuriem ir nepieciešama iespēja līmenī, kas ir vienāds ar vai pārsniedz minimālo līmeni, kas norādīts resursu prasībā.

## <a name="priority"></a>Prioritāte
Operācijas resursiem, kuriem ir vienādas iespējas, var piešķirt prioritāti. Šādā gadījumā, ja vairākiem resursiem ir iespējas, kas atbilst plānošanas prasībām pieprasījuma līmenī, un ir brīva noslodze, plānošanas programma var atlasīt kādu no šiem resursiem. Ja lapā **Parametru plānošana** ir atlasīta lauka **Primāro resursu atlase** vērtība **Prioritāte**, plānošanas laikā vispirms tiek atlasīts resurss ar augtāko prioritāti (mazāko skaitlisko lauka **Prioritāte** vērtību).

## <a name="resource-requirements"></a>Resursu vajadzības
Definējot resursu prasības ražošanas maršrutam, kā prasības var norādīt vienu vai vairākas iespējas. Ražošanas plānošanas laikā iespējas, kas ir definētas resursu prasībās maršruta operācijā, tiek saskaņotas ar iespējām, kas ir definētas resursiem. Tiek atlasīti resursi, kuriem ir iespējas, kas atbilst prasībām. Ja vairākiem resursiem ir vienādas funkcionālas iespējas, bet dažādas prasmes (piemēram, izturība, apstrādes ātrums vai precizitāte), var definēt vairākas iespējas vai izmantot iespēju līmeni, lai kvalificētu resursu iespēju. Tālāk minēts piemērs:

-   Maršrutā urbšanas procesa laiks tiek iestatīts uz 10 vienībām stundā, bet pati prasība ir definēta kā Urbšana.
-   Jums ir divas urbšanas iekārtas — M1 un M2.
-   Urbšanas iespēja ir piešķirta abiem resursiem — iekārtai M1 un iekārtai M2.
-   Iekārta M1 var urbt divas vienības stundā un iekārta M2 var urbt 11 vienības stundā.

Šajā piemērā, plānošanas programma var atlasīt abas iekārtas, jo abas apmierina pamatiespējas prasību (urbšanu). Tomēr iekārta M1 var urbt tikai divas vienības stundā. Tā kā šis ātrums ir daudz mazāks nekā 10 vienības stundā, kas norādītas maršrutā, iekārta M1 radīs ražošanas problēmas, ja tā tiks atlasīta. Šo problēmu var atrisināt un nodrošināt, lai tiktu atlasīta iekārta M2, divējādi:

-   Izveidojiet divas atsevišķas iespējas: urbšanu zemā ātrumā un urbšanu lielā ātrumā. Definējiet zema ātruma urbšanu kā urbšanu, kurai ir procesa laiks no vienas līdz deviņām vienībām stundā. Definējiet lielātruma urbšanu kā urbšanu, kurai urbšanas procesa laiks ir no 10 līdz 19 vienībām stundā. Pēc tam piešķiriet iekārtai M1 zema ātruma urbšanas iespēju un piešķiriet iekārtai M2 liela ātruma urbšanas iespēju. Visbeidzot mainiet maršruta resursa iespējas prasību uz liela ātruma urbšanu. Pēc tam plānošanas programma atlasīs pareizo iekārtu (M2).
-   Izmantojiet iespējas līmeni, lai kvalificētu urbšanas iespēju, kura ir piešķirta urbšanas iekārtām. Norādiet, ka iekārtas M1 urbšanas iespējas līmenis ir 2,0, bet iekārtas M2 urbšanas iespējas līmenis ir 11,0. Pēc tam norādiet, ka maršruta urbšanas iespējas prasības minimālais līmenis ir 10,0. Pēc tam plānošanas programma noteiks, ka tikai iekārta M2 atbilst resursu prasībām.

## <a name="competencies-for-human-resources"></a>Cilvēkresursu zināšanas
Ja jums ir operācijas resursi ar tipu **Cilvēkresursi**, kas ir saistīti ar darbiniekiem Cilvēkresursos, jūs varat arī izmantot darbinieku zināšanas, definējot resursu prasības ražošanas maršrutam. Citiem vārdiem sakot, varat arī norādīt prasības specifiskām prasmēm, kursiem, sertifikātiem vai amatiem. Pēc tam plānošanas programma var atlasīt resursus, kas ir saistīti ar darbiniekiem, un atlases pamatā būs šo darbinieku zināšanas. Zināšanas ir iestatītas Cilvēkresursos, nevis lapā **Resursu iespējas** lapu. Definējot prasmes, kursus, sertifikātus vai amatus kā resursu prasības, ir jāizmanto moduļa Personāla vadība funkcionalitāte un katrs resurss, kura veids ir **Cilvēkresursi**, ir jāsaista ar atbilstošu nodarbinātā veidu. Ja nelietojat moduļa Personāla vadība funkcionalitāti, varat lapā **Resursu iespējas** definēt iespējas, kas līdzinās kompetencēm modelī Personāla vadība vai ir to dublikāti. Tomēr, lapā **Resursu iespējas** nav funkcionalitātes, kas ir nepieciešama, lai saglabātu prasmes, kursus, sertifikācijas vai amatus.




