---
title: Patēriņa cenu indeksa grafiks
description: Šajā rakstā skaidrots, kā izveidot plaša patēriņa cenu indeksa (CPI) grafiku sarakstu, ko iegūstat no interneta, lai palīdzētu noteikt eskalācijas maksu abonementa rēķinos.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f08b79ee00baab3713d9ccc24a7595b1de7a7768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904878"
---
# <a name="consumer-price-index-schedule"></a>Patēriņa cenu indeksa grafiks

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā izveidot, dzēst, pārskatīt un apstrādāt plaša patēriņa cenu indeksa (CPI) grafikus. CPI grafiku var izmantot, lai noteiktu plaša patēriņa preču un pakalpojumu cenas, ko pievienojat kā rēķinu grafika rindas. Pēc tam CPI grafiku var izmantot ar eskalāciju un atlaides cenu norēķinu grafikā, vai arī to var manuāli apstrādāt, lai atjauninātu rēķinu summu norēķinu grafikās. Jūs varat manuāli ievadīt CPI grafikus, vai arī jūs variet importēt tos, izmantojot CPI grafika salikto elementu.

Lai pievienotu CPI grafiku, sekojiet šiem soļiem.

1. Lapā Patērētāja **cenu indeksa grafiks** atlasiet **Jauns**.
2. Laukā **Patērētāja cenu indeksa** grafiks ievadiet unikālu nosaukumu.
3. Ievadiet aprakstu laukā **Apraksts**.
4. Cilnē Patērētāja **cenu indeksa grafiks** atlasiet **Pievienot**.
5. Laukā **Patērētāja cenu indeksa datums** norādiet datumu, kad jaunais CPI grafiks kļūst aktīvs.
6. Laukā **Patērētāja cenu indeksa** grafiks ievadiet nosaukumu, kuru ievadījāt 2. solī.
7. Atlasiet **Saglabāt**.

Lai dzēstu CPI grafika datumu, sekojiet šiem soļiem.

1. Lapā Patērētāja **cenu indeksa grafiks** atlasiet vienu vai vairākas rindas, ko vēlaties dzēst, un pēc tam atlasiet **Noņemt**.
2. Lai dzēstu visu CPI grafiku, darbību rūtī atlasiet **Dzēst**. Atlasīto CPI grafiku nevar dzēst, ja tas ir saistīts ar norēķinu grafiku.
3. Darbību rūtī atlasiet Apstrādāt, lai **atjauninātu** norēķinu grafikus, kas izmanto atlasīto CPI grafiku. Visjaunākos CPI datumus un grafiku summas tiks izmantotas, lai atjauninātu norēķinu grafika cenas.
4. Kopsavilkuma cilnē **Patērētāja cenu indekss** pārskatiet **atjaunināto** norēķinu grafika numuru, krājuma numuru, **·** **norēķinu** sākuma datumu, norēķinu beigu datumu, **·** **eskalācijas** **datumu un eskalācijas biežuma** laukus.

Pēc CPI grafiku iestatīšanas tos var izmantot eskalācijai un atlaižu cenu izmaiņām norēķinu plānos.

## <a name="cpi-calculation"></a>CPI aprēķins

Šiem piemēriem periods ir no 2020. gada 1. janvāra līdz 2022. gada 31. decembrim. Pamata CPI likme (CPI vērtība, kad līgums sākas) ir 105,65. 2021. gada 1. janvārī pašreizējais CPI ir 110,5. 2022. gada 1. janvārī pašreizējais CPI ir 114,25. Sākotnējā summa ir $1,000.

**1. piemērs**

Lapā Periodiskie **līguma norēķinu parametri iestatiet** patēriņa cenu indeksa **aprēķina** lauku uz bāzes patērētāja **cenu indeksu**.

2021. gada 1. janvārī pirmā eskalācijas summa tiek aprēķināta šādi, pamatojoties uz sākotnējo summu:

1000 + (110,5 – 105,65) &divide; 105,65 &times; 1000 = 1,045,91

2022. gada 1. janvārī eskalācijas summa tiek aprēķināta šādi:

1000 + (114,25 – 105,65) &divide; 105,65 &times; 1000 = 1,081,40

**2. piemērs**

Lapā Periodiskie **līguma norēķinu parametri iestatiet** patēriņa cenu indeksa **aprēķina** lauku uz iepriekšējo patērētāja **cenu indeksu**.

2021. gada 1. janvārī pirmā eskalācijas summa tiek aprēķināta šādi, pamatojoties uz sākotnējo summu:

1000 + (110,5 – 105,65) &divide; 105,65 &times; 1000 = 1,045,91

2022. gada 1. janvārī eskalācijas summa tiek aprēķināta šādi, pamatojoties uz pirmo eskalācijas summu:

1 045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1,045,91 = 1,081,40

> [!NOTE]
> Eskalācijas process vienmēr izmanto pēdējo CPI vērtību neatkarīgi no indeksa datuma. Piemēram, ja eskalācija ir septembrī, bet pēdējā CPI vērtība ir jūlijam, tiek lietots jūlija indekss. Pēc septembrī indeksa ievadīšanas netiek veikti nekādi pielāgojumi.

## <a name="prorated-escalation"></a>Prorated eskalācija

Ja eskalācija ir rēķina perioda vidū, summa tiek prorated. Piemēram, norēķinu periods ir no 2020. gada 1. augusta līdz 2021. gada 31. jūlijam. CPI datumā 2019. gada 1. septembrī CPI vērtība ir 244. CPI datumā 2020. gada 1. septembrī šī CPI vērtība ir 250. Ja iepriekšējā likme ir 1000, rēķina summas aprēķināšanai par periodu tiek izmantotas šādas formulas:

* *CPI izmaiņas* = (250 – 244) &divide; 244 = 2,459%
* *Pašreizējā likme* = 1000 &times; 2,459% = 1,024,59
* *Dienu skaits ar pašreizējo likmi* = 2021. gada 31. jūlijs – 2020. gada 1. septembris = 334
* *Iepriekšējā likme* = 1000
* *Dienu skaits ar iepriekšējo* likmi = 2020. gada 31. augusts – 2020. gada 1. augusts = 31
* *Kopējais norēķinu perioda dienu skaits* = 2021. gada 31. jūlijs – 2020. gada 1. augusts + 1 = 365.
* *Rēķina summa šim* periodam = (1000 &times; 31 &divide; 365) + (1,024,59 &times; 334 &divide; 365) = 1,022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Eskalācija, kas izmanto CPI un procentus

Eskalācijas var veikt, izmantojot CPI. CPI plus 3 procentu eskalācija sākas 2020. gada 1. janvārī, un tai ir gada biežums.

- Summa, par kuru tiek izrakstīts rēķins par 2019. gada 1. janvāri līdz 2020. gada 31. decembrim ir 4000.
- Rēķina periods, kas tiks eskalēts, ir 2020. gada 1. janvāris līdz 2020. gada 31. decembrim.
- CPI datumā 2018. gada 1. decembrī CPI vērtība ir 205,3. CPI datumā 2019. gada 1. decembrī CPI vērtība ir 219,6.

Ja iepriekšējā likme ir 4000, rēķina summa šim periodam tiek aprēķināta šādā veidā:

- *CPI izmaiņas* = (219,6 – 205,3) &divide; 205,3 = 6,965%
- *Pašreizējā likme* = (4000 &times; 6,965%) – 4000 = 278,60
- *Procentu izmaiņas* = (4000 &times; 1,03) – 4000 = 120
- *Rēķina summa* = 4000 + 278,6 + 120 = 4 398,6
