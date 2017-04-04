---
title: "Sadalīt periodu periodiskajos žurnālos"
description: "Periodiskos žurnālus dažreiz sauc par cikliskiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtota katru reizi, kad tiek grāmatots šis žurnāls. Veidojot žurnālu, norādiet atkārtošanās perioda intervālu, piemēram, dienas vai mēnešus. Norādiet arī to periodu skaitu, kuros jāgrāmato žurnāls."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261354
ms.assetid: 76c0d7bf-f795-4d42-9a86-a9f36989962c
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 58ab77aea9e66834c516806e5f0cfe3069c94ff3
ms.lasthandoff: 03/31/2017


---

# <a name="split-periods-in-periodic-journals"></a>Sadalīt periodu periodiskajos žurnālos

Periodiskos žurnālus dažreiz sauc par cikliskiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtota katru reizi, kad tiek grāmatots šis žurnāls. Veidojot žurnālu, norādiet atkārtošanās perioda intervālu, piemēram, dienas vai mēnešus. Norādiet arī to periodu skaitu, kuros jāgrāmato žurnāls.

Lai atkārtoti izgūt un grāmatot darbības rindas, varat izmantot **periodiskajos žurnālos** lapā. Juridiskām personām ar Čehijas, Igaunijas, Ungārijas, Latvija, Lietuva, Polija un Krievija, **periodiskajos žurnālos** lapu pagarināja sadalīt periodu funkcionalitātei. <!---For more information, see [Create and process a periodic journal](http://ax.help.dynamics.com/en/wiki/create-and-process-a-periodic-journal/).-->

### <a name="example-split-for-periods-in-periodic-journals"></a>Piemērs: Sadalīt periodu periodiskajos žurnālos

Apdrošināšanas sabiedrība piedāvā uzņēmuma atlaidi par apdrošināšanas polisi prepaying visu gadu. Maksājums tiek grāmatots aktīvu kontā, piemēram, kā priekšapmaksas apdrošināšana. Pēc tam jūs dzēšat ikmēneša apdrošināšanas izdevumus visa gada garumā, izveidojot periodisku žurnālu, kas ietver priekšapmaksas apdrošināšanas konta kredītu un apdrošināšanas izdevumu konta debetu. Šajā gadījumā var izmantot sadalījumu periodos funkcionalitāti. Noklikšķiniet uz **sadalīt periodu** pogu darbību rūtī **periodiskā žurnāla****līnijas** lapa, un pēc tam norādiet šādus laukus.

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**             | **Description**                                                                                                                                                                                             |
| **Start date**        | Atlasiet pirmo periodiskā žurnāla rindas datums.                                                                                                                                                        |
| **Number of periods** | Ievadiet periodu, pār kuru sadalīt žurnāla rindu skaits. Šī vērtība nosaka, cik daudz jaunu darījumu tiek ģenerēts. Darījuma summa ir vienmērīgi sadalīta pa jaunajiem darījumiem. |
| **Unit**              | Periodam atlasiet mērvienību.                                                                                                                                                                  |
| **Perioda intervāla**   | Nosaka intervālu starp grāmatošanas periodus.                                                                                                                                                              |

Piemēram, lai ģenerētu ceturkšņa grāmatojumus, ievadiet **4**, **periodu skaits** lauku, atlasiet **mēneši**, **vienību** laukam un ievadiet **3**, **perioda intervāla** lauku. Sistēma ģenerē četri žurnāla rindas, katra par vienu ceturto daļu no žurnāla rindas summa, kuru ievadījāt, 3 mēnešu starplaikiem. Līdzīga funkcionalitāte pieejama arī v/g žurnālā. Apskatot Virsgrāmatas žurnāla rindas, atlasiet **periodisko darbību žurnālā**&gt;**saglabāt žurnālu**.


