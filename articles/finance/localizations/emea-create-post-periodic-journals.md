---
title: Sadalīt periodus periodiskajos žurnālos
description: Šajā rakstā ir sniegta informācija par periodisko žurnālu vai periodisku juridisku personu periodisko žurnālu dalījuma periodiskajiem žurnāliem Čehijai, Igaunijai, Ungārijai, Latvijai, Lietuvai, Polijai un Krievijai.
author: mrolecki
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 261354
ms.search.form: LedgerJournalTable
ms.openlocfilehash: 2446edd0f569efbe2f6304ecbb46d5a4265ff95e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287041"
---
# <a name="split-periods-in-periodic-journals"></a>Sadalīt periodus periodiskajos žurnālos

[!include [banner](../includes/banner.md)]

Periodiskos žurnālus dažreiz sauc par cikliskiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtota katru reizi, kad tiek grāmatots šis žurnāls. Veidojot žurnālu, norādiet atkārtošanās perioda intervālu, piemēram, dienas vai mēnešus. Norādiet arī to periodu skaitu, kuros jāgrāmato žurnāls.

Lai periodiski izgūtu un grāmatotu transakciju rindas, varat lietot lapu **Periodiskie žurnāli**. Juridiskajām personām Čehijā, Igaunijā, Ungārijā, Latvijā, Lietuvā, Polijā un Krievijā lapa **Periodiskie žurnāli** ir paplašināta ar funkcionalitāti sadalīšanai pa periodiem. Papildinformāciju skatiet rakstā [Periodisko žurnālu grāmatošana](../general-ledger/tasks/post-periodic-journals.md)

### <a name="example-split-for-periods-in-periodic-journals"></a>Piemērs: sadalīt pa periodiem periodiskajos žurnālos

Kāda apdrošināšanas sabiedrība jūsu uzņēmumam piedāvā atlaidi, veicot apdrošināšanas polises priekšapmaksu par visu gadu. Maksājums tiek grāmatots aktīvu kontā, piemēram, kā priekšapmaksas apdrošināšana. Pēc tam jūs dzēšat ikmēneša apdrošināšanas izdevumus visa gada garumā, izveidojot periodisku žurnālu, kas ietver priekšapmaksas apdrošināšanas konta kredītu un apdrošināšanas izdevumu konta debetu. Šajā gadījumā varat lietot funkcionalitāti sadalīšanai pa periodiem. Lapas **Periodisko žurnālu** **rindas** darbību rūtī noklikšķiniet uz pogas **Sadalīt pa periodiem**, un pēc tam norādiet tālāk uzskaitīto lauku vērtības.


| Lauks            | Apraksts                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------|
| **Sākuma datums**        | Atlasiet datumu pirmajai periodiskā žurnāla rindai.                                                                                                                                                        |
| **Periodu skaits** | Ievadiet skaitu, cik periodos sadalīt šo žurnāla rindu. Šī vērtība nosaka, cik daudz jaunu darījumu tiek ģenerēts. Darījuma summa ir vienmērīgi sadalīta pa jaunajiem darījumiem. |
| **Vienība**              | Atlasiet perioda mērvienību.                                                                                                                                                                  |
| **Perioda intervāls**   | Nosakiet intervālu starp grāmatošanas periodiem.                                                                                                                                                              |

Piemēram, lai ģenerētu ceturkšņa grāmatojumus, laukā **Periodu skaits** ievadiet **4**, laukā **Vienība** atlasiet vērtību **Mēneši** un laukā **Periodu intervāls** ievadiet **3**. Sistēma ģenerē četras žurnāla rindas ar 3 mēnešu intervāliem, un katra no tām ietver vienu ceturto daļu no jūsu ievadītās žurnāla rindas summas. Līdzīga funkcionalitāte ir pieejama arī virsgrāmatas žurnālam. Kad apskatāt virsgrāmatas žurnāla rindas, atlasiet **Periodiskais žurnāls** &gt; **Saglabāt žurnālu**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
