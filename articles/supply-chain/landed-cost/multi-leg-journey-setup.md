---
title: Vairākfāžu ceļojuma iestatījums
description: Šajā tēmā ir aprakstīts, kā iestatīt vairākfāžu ceļojumus Kopējo izmaksu modulim.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 045ded1fb881b0572f4490ab3a5d4ca1cb8c341a4d245e6d98991228a90aadb7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774082"
---
# <a name="multi-leg-journey-setup"></a>Vairākfāžu ceļojuma iestatījums

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt vairākfāžu ceļojumus **Kopējo izmaksu** modulim.

## <a name="legs"></a>Fāzes

Fāzes tiek izmantotas, lai identificētu atsevišķas ceļojuma daļas. Katra varētu būt veidota, atlasot nosūtīšanas ostas "uz" un "no" un šim sūtījumam izmantoto transportēšanas metodi. Izpildes laikus var saistīt ar katru fāzi. Izpildes laiki var palīdzēt atsekot kravu, un to var izmantot arī, lai aprēķinātu paredzamo preču piegādes datumu reisā. Turklāt, kad ceļojuma posms ir pabeigts, reisa, nosūtīšanas konteinera un saistīto pirkšanas pasūtījuma rindu statusu var atjaunināt, izmantojot izsekošanas kontroles iestatījumus. Ceļus var izmantot ar vienu ceļojuma veidni vai arī tos var atkārtoti izmantot vairākas ceļojuma veidnes. Konteinera iekraušana, muita un lokālais transports parasti tiek iestatīts kā fāzes, un tiem tiek izmantota neraksturīga nosūtīšanas osta.

Lai darbotos ar fāzēm, dodieties uz **Kopējās izmaksas \> Vairākfāžu ceļojuma izmaksas iestatījumi \> Fāzes**. Tur ir iespējams apskatīt, atvērt, izveidot un dzēst ierakstus par brīvdienām. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.

| Lauks | Apraksts |
|---|---|
| Fāze | Ievadiet nosūtīšanas ostai unikālu ID nosaukumu/numuru. |
| Apraksts | Ievadiet ceļojuma fāzes aprakstu. Parasti šis apraksts identificē ostas "uz" un "no" vai ceļojuma soli. |
| No ostas | Ievadiet preces izcelsmes punktu fāzei. |
| Uz ostu | Ievadiet preces galapunktu fāzei. |
| Piegādes metode | Ievadiet fāzes transportēšanas veidu. |

## <a name="journey-templates"></a>Maršruta veidnes

Ceļojuma veidne nosaka vairākfāžu ceļojumu starp divām ostām, no kurām preces tiek transportētas reisa laikā. Ceļojuma posms ir apvienots, lai noteiktu laika daudzumu, kas nepieciešams, lai preces varētu ceļot no kreditora izcelsmes punkta uz gala noliktavas galamērķi. Kad kravas kravas veidne tiek novietota ceļojuma veidnē, izpildes laiki identificēs katras reisa, konteinera un pirkuma rindu datumu un statusu. Lietojiet [Izsekošanas kontroles centru](delivery-information-setup.md), lai iestatītu izpildes laikus, kas ir saistīti ar katru kājai, kas veido ceļojuma veidni. Ceļojuma veidni izmanto arī, kad ir iestatītas reisa automātiskās izmaksas. Kad ir definēta transportēšana, ar preču transportēšanu saistītās izmaksas var definēt automātiskās izmaksu lapā.

Lai darbotos ar ceļojuma veidnēm, dodieties uz **Kopējās izmaksas \> Vairākfāžu ceļojuma izmaksas iestatījumi \> Ceļojuma veidnes**. Tur ir iespējams apskatīt, atvērt, izveidot un dzēst ceļojumu veidnes.

Katrai ceļojuma veidnei galvenē iestatiet šādus laukus.

| Lauks | Apraksts |
|---|---|
| Maršruta veidne | Ievadiet ceļojuma veidnei unikālu ID nosaukumu/numuru. Parasti ceļojuma veidne raksturo ceļojuma izcelsmes punktu un galamērķa punktu. |
| Apraksts | Ievadiet ceļojumu veidnes aprakstu. Apraksts parasti norāda ostas "uz" un "no" un ceļojuma tipu. |

Sadaļā **Rindas** pievienojiet rindu katrai ceļojuma kājai un novietojiet rindas secībā. Lai mainītu rindu secību, rīkjoslā izmantojiet bultiņas **Augšup** un **Lejup**. Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katrai rindai.

| Lauks | Apraksts |
|---|---|
| Fāze | Izvēlieties fāzi, ko pievienot ceļojumam. |
| Apraksts | Fāzes apraksts. |
| No ostas | Osta, kas ir preču izcelsmes vieta fāzē. Šī osta ir osta "uz", kas tiek izmantota, lai noteiktu automātiskās reisa izmaksas. |
| Uz ostu | Preču galamērķa osta fāzē. |
| Piegādes veids | Piegādes veids, ko izmanto fāzē. |
| Maršruts no ostas | Ja, lai noteiktu automātiskās izmaksas, tiek izmantota fāzei norādītā osta, atzīmējiet šo izvēles rūtiņu, lai identificētu to kā "ceļojuma no" ostu. Šī osta tiks parādīta reisa galvenē. |
| Maršruts uz ostu | Ja, lai noteiktu automātiskās izmaksas, tiek izmantota fāzei norādītā osta, atzīmējiet šo izvēles rūtiņu, lai identificētu to kā "ceļojuma uz" ostu. Šī osta tiks parādīta reisa galvenē. |
| Nosūtīšanas uzņēmums | Atlasiet sūtīšanas uzņēmumu, kuru izmanto fāzē. |

## <a name="activities"></a>Aktivitātes

Iestatījumi lapā **Darbības** izveido aktivitāšu tipus, kas var rasties kādā ostas fāzē. Lietotāji, kuri strādā lapā **Visi pārvadāšanas konteineri**, var izvēlēties starp šīm vērtībām, kad tie novērtē katras aktivitātes ilgumu un reģistrē faktisko ilgumu salīdzināšanas nolūkiem.

Lai iestatītu savas aktivitātes, dodieties uz **Kopējās izmaksas \> Vairākfāžu ceļojumu iestatīšana \> Darbības**. Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu darbības.

Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katrai darbībai režģī.

| Lauks | Apraksts |
|---|---|
| Aktivitāte | Darbības nosaukums. |
| Apraksts | Darbības apraksts. |
| Nosūtīšanas uzņēmums | Atlasiet nosūtīšanas uzņēmuma kreditora kontu, kas ir saistīts ar darbību. |
