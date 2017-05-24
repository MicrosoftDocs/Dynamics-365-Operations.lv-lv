---
title: "Sadalīt periodus periodiskajos žurnālos"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8a0c6ee25b7130dcee2cc8eada9e83823db21faf
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="split-periods-in-periodic-journals"></a>Sadalīt periodus periodiskajos žurnālos

[!include[banner](../includes/banner.md)]


Periodiskos žurnālus dažreiz sauc par cikliskiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtota katru reizi, kad tiek grāmatots šis žurnāls. Veidojot žurnālu, norādiet atkārtošanās perioda intervālu, piemēram, dienas vai mēnešus. Norādiet arī to periodu skaitu, kuros jāgrāmato žurnāls.

Lai periodiski izgūtu un grāmatotu transakciju rindas, varat lietot lapu **Periodiskie žurnāli**. Juridiskajām personām Čehijā, Igaunijā, Ungārijā, Latvijā, Lietuvā, Polijā un Krievijā lapa **Periodiskie žurnāli** ir paplašināta ar funkcionalitāti sadalīšanai pa periodiem. <!---For more information, see [Create and process a periodic journal](http://ax.help.dynamics.com/en/wiki/create-and-process-a-periodic-journal/).-->

### <a name="example-split-for-periods-in-periodic-journals"></a>Piemērs: sadalīt pa periodiem periodiskajos žurnālos

Kāda apdrošināšanas sabiedrība jūsu uzņēmumam piedāvā atlaidi, veicot apdrošināšanas polises priekšapmaksu par visu gadu. Maksājums tiek grāmatots aktīvu kontā, piemēram, kā priekšapmaksas apdrošināšana. Pēc tam jūs dzēšat ikmēneša apdrošināšanas izdevumus visa gada garumā, izveidojot periodisku žurnālu, kas ietver priekšapmaksas apdrošināšanas konta kredītu un apdrošināšanas izdevumu konta debetu. Šajā gadījumā varat lietot funkcionalitāti sadalīšanai pa periodiem. Lapas **Periodisko žurnālu** **rindas** darbību rūtī noklikšķiniet uz pogas **Sadalīt pa periodiem**, un pēc tam norādiet tālāk uzskaitīto lauku vērtības.

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lauks**             | **Apraksts**                                                                                                                                                                                             |
| **Sākuma datums**        | Atlasiet datumu pirmajai periodiskā žurnāla rindai.                                                                                                                                                        |
| **Periodu skaits** | Ievadiet skaitu, cik periodos sadalīt šo žurnāla rindu. Šī vērtība nosaka, cik daudz jaunu darījumu tiek ģenerēts. Darījuma summa ir vienmērīgi sadalīta pa jaunajiem darījumiem. |
| **Vienība**              | Atlasiet perioda mērvienību.                                                                                                                                                                  |
| **Perioda intervāls**   | Nosakiet intervālu starp grāmatošanas periodiem.                                                                                                                                                              |

Piemēram, lai ģenerētu ceturkšņa grāmatojumus, laukā **Periodu skaits** ievadiet **4**, laukā **Vienība** atlasiet vērtību **Mēneši** un laukā **Periodu intervāls** ievadiet **3**. Sistēma ģenerē četras žurnāla rindas ar 3 mēnešu intervāliem, un katra no tām ietver vienu ceturto daļu no jūsu ievadītās žurnāla rindas summas. Līdzīga funkcionalitāte ir pieejama arī virsgrāmatas žurnālam. Kad apskatāt virsgrāmatas žurnāla rindas, atlasiet **Periodiskais žurnāls** &gt; **Saglabāt žurnālu**.



