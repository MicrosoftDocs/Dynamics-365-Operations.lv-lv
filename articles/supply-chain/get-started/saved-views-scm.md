---
title: Standarta saglabātie skati Supply Chain Management
description: Šajā tēmā aprakstīti pieejamie standarta saglabātie skati un skaidrots, kā tos iespējot.
author: kamaybac
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0709574ea44fcf841321044da31781862fcf1420
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103692"
---
# <a name="standard-saved-views-for-supply-chain-management"></a>Standarta saglabātie skati Supply Chain Management

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management ietver vairākus saglabātus skatus, ko varat iespējot un lietot pēc nepieciešamības. Daži no šiem standarta saglabātajiem skatiem ir optimizēti un nosaukti noteiktai lomai vai uzdevumam (piemēram, "Kvalitātes kontrole" vai "Saņemšana"). Citi ir optimizēti, tādējādi tajos ir ietverti tikai lauki un iestatījumi, ko norāda Microsoft lietošanas statistika, visbiežāk tiek izmantoti debitori. Uz šiem saglabātajiem skatiem parasti tiek saukti kā uz *vienkāršotajiem* skatiem. Šajā tēmā aprakstīti pieejamie standarta saglabātie skati un skaidrots, kā tos iespējot un pielāgot.

Pilnīgu informāciju par to, kā strādāt ar saglabātajiem skatiem, ieskaitot standarta saglabātos skatus, pēc to iespējošanas, skatiet [Saglabātie skati](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="customizing-the-standard-saved-views"></a>Standarta saglabāto skatu pielāgošana

Varat pielāgot standarta saglabātos skatus tāpat, kā varat pielāgot savus saglabātos skatus. Tomēr, pielāgojot standarta saglabāto skatu, ļoti ieteicams saglabāt pielāgoto versiju ar jaunu nosaukumu. Pretējā gadījumā pielāgojumi var tikt pārrakstīti, atjauninot Supply Chain Management.

Papildinformāciju par to, kā pielāgot un pārdēvēt saglabātos skatus, skatiet [sadaļā Saglabātie skati](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="available-saved-views-and-how-to-enable-them"></a>Pieejamie saglabātie skati un to iespējošanas veids

Lai izmantotu jebkurus saglabātos skatus neatkarīgi no tā, vai izmantosit standarta saglabātos skatus, *·*[aktivizējot](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) līdzekli Saglabātie skati līdzekļu pārvaldībā (no versijas 10.0.21, šī funkcija ir iespējota pēc noklusējuma).

Šīs tēmas pārējās sadaļās ir sniegtas tabulas, kurās ir aprakstīti standarta saglabātie skati, kas pašlaik ir pieejami katram atbilstošajam modulim. Katrā tabulā ir parādīts katra saglabātā skata nosaukums, lapa, kurā to var atrast, un tā apraksts. Katrā tabulā ir parādīts arī tās funkcionalitātes nosaukums, kas ietver saglabāto skatu. Lai redzētu standarta saglabāto skatu jūsu sistēmā, ir jāieslēdz norādītā funkcija [Līdzekļu pārvaldībā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). No versijas 10.0.25 visi uzskaitītie skati ir ieslēgti pēc noklusējuma.

## <a name="saved-views-for-the-inventory-management-module"></a>Krājumu vadības moduļa saglabātie skati

Tabulā ir aprakstīti krājumu vadības modulim pieejamie saglabātie skati.

| Lapa | Skata nosaukums | Skatiet aprakstu | Līdzekļa nosaukums |
|---|---|---|---|
| Rīcībā esošā saraksts | Finanšu dati | Šis vienkāršotais skats ļauj fokusam uz finanšu informāciju, kamēr pārvaldāt rīcībā esošos krājumus. | Saglabātie krājumu pārvaldības skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Rīcībā esošā saraksts | Kvalitātes kontrole | Šis vienkāršotais skats ļauj koncentrēties uz kvalitātes kontroli, kamēr pārvaldāt rīcībā esošos krājumus. | Saglabātie krājumu pārvaldības skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Rīcībā esošā saraksts | saņemšanu, | Šis vienkāršotais skats ļauj koncentrēties uz saņemtajām darbībām, kamēr pārvaldāt rīcībā esošos krājumus. | Saglabātie krājumu pārvaldības skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Rīcībā esošā saraksts | Piegāde | Šis vienkāršotais skats ļauj koncentrēties uz nosūtīšanas darbībām, kamēr pārvaldāt rīcībā esošos krājumus. | Saglabātie krājumu pārvaldības skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Darījumi | Vienkāršots | Šis vienkāršotais skats ļauj pārskatīt krājumu statusu, netraucējot finanšu informāciju un citus laukus, kas tiek lietoti mazāk bieži. | Saglabātie krājumu pārvaldības skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Pārsūtīšanas pasūtījumi | Piegāde | Šis vienkāršotais skats ļauj koncentrēties uz nosūtīšanas darbībām, kamēr pārvaldāt pārsūtīšanas pasūtījumus. | Saglabātie krājumu pārvaldības skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Pārsūtīšanas pasūtījumi | saņemšanu, | Šis vienkāršotais skats ļauj koncentrēties uz saņemšanas darbībām, kamēr pārvaldāt pārsūtīšanas pasūtījumus. | Saglabātie krājumu pārvaldības skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Pārsūtīšanas pasūtījumi | Kvalitātes kontrole | Šis vienkāršotais skats ļauj koncentrēties uz kvalitāts kontroli, kamēr pārvaldāt pārsūtīšanas pasūtījumus. | Saglabātie krājumu pārvaldības skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Pārsūtīšanas pasūtījumi | Finanšu dati | Šis vienkāršotais skats ļauj koncentrēties uz finanšu informāciju, kamēr pārvaldāt pārsūtīšanas pasūtījumus. | Saglabātie krājumu pārvaldības skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |

## <a name="saved-views-for-the-master-planning-module"></a>Vispārējā plānošanas moduļa saglabātie skati

Tabulā ir aprakstīti vispārīgajam modulim pieejamie saglabātie skati.

| Lapa | Skata nosaukums | Skatiet aprakstu | Līdzekļa nosaukums |
|---|---|---|---|
| Plānotie pasūtījumi: lapa Detalizēta informācija par plānoto pasūtījumu | Vienkāršoti | Vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti darbam ar viena plānotā pasūtījuma detaļām. Šādā veidā tas nodrošina ātrāku pārskatu un racionalizētu darba procesu. | Saglabātie skati plānotajiem pasūtījumiem<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Plānotie pasūtījumi: lapa Detalizēta informācija par plānoto pasūtījumu | Vienkāršots | Vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti darbam ar viena plānotā pasūtījuma detaļām. Šādā veidā tas nodrošina ātrāku pārskatu un racionalizētu darba procesu. | Saglabātie skati plānotajiem pasūtījumiem<br><br>(Pēc noklusējuma no versijas 10.0.25) |

## <a name="saved-views-for-the-procurement-and-sourcing-module"></a>Sagādes un avotu moduļa saglabātie skati

Tabulā ir aprakstīti Sagādes un avotu modulim pieejamie saglabātie skati.

| Lapa | Skata nosaukums | Skatiet aprakstu | Līdzekļa nosaukums |
|---|---|---|---|
| Pirkšanas pasūtījuma dati | Pirkšanas pasūtījuma izveide | Šis vienkāršotais skats ir optimizēts jaunu pirkšanas pasūtījumu veidošanai. | Saglabātie pirkšanas pasūtījumu skati<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Pirkšanas pasūtījuma dati | Krājumu vadība | Šis vienkāršotais skats ir optimizēts ar krājumiem saistītu aktivitāšu veikšanai, piemēram, saņemtajiem krājumiem sekošanai, krājumu saņemšanai, neto prasību pārbaudei un pasūtījuma daudzumu pielāgošanai. | Saglabātie pirkšanas pasūtījumu skati<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Pirkšanas pasūtījuma dati | Finanšu pārvaldība | Šis vienkāršotais skats ir optimizēts ar finansēm saistītu aktivitāšu veikšanai, piemēram, cenu, kopsummu un maksu rēķinu izrakstīšanai un pārbaudei. | Saglabātie pirkšanas pasūtījumu skati<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Pirkšanas pasūtījuma dati | Pasūtījuma apstiprinājums | Šis vienkāršotais skats ir optimizēts jaunu pirkšanas pasūtījumu apstiprināšanai. | Saglabātie pirkšanas pasūtījumu skati<br><br>(Pēc noklusējuma no versijas 10.0.25) |

## <a name="saved-views-for-the-product-information-management-module"></a>Preces informācijas pārvaldības moduļa saglabātie skati

Tabulā ir aprakstīti Preces informācijas pārvaldības modulim pieejamie saglabātie skati.

| Lapa | Skata nosaukums | Skatiet aprakstu | Līdzekļa nosaukums |
|---|---|---|---|
| Izlaisto preču saraksts | Preces izveide | Vienkāršots lapas skats, kurā iekļauti tikai tie lauki, kurus visbiežāk izmanto, veidojot produktus. | Saglabātie izlaisto preču skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Nodoto preču papildinformācija | Preces izveide | Vienkāršots lapas skats, kurā iekļauti tikai tie lauki, kurus visbiežāk izmanto, veidojot produktus. | Saglabātie izlaisto preču skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Nodoto preču papildinformācija | Loģistikas informācijas pārvaldība | Vienkāršots lapas skats, kurā iekļauti tikai tie lauki, kurus visbiežāk izmanto, pārvaldot produktu loģistikas informāciju. | Saglabātie izlaisto preču skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Nodoto preču papildinformācija | Pirkumu informācijas pārvaldība | Vienkāršots lapas skats, kurā iekļauti tikai tie lauki, kurus visbiežāk izmanto, pārvaldot produktu pirkumu informāciju. | Saglabātie izlaisto preču skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Nodoto preču papildinformācija | Pārdošanas informācijas pārvaldība | Vienkāršots lapas skats, kurā iekļauti tikai tie lauki, kurus visbiežāk izmanto, pārvaldot produktu pārdošanas informāciju. | Saglabātie izlaisto preču skati<br><br>(Pēc noklusējuma no versijas 10.0.21) |

## <a name="saved-views-for-the-production-control-module"></a>Preču kontroles moduļa saglabātie skati

Tabulā ir aprakstīti Preču kontroles modulim pieejamie saglabātie skati.

| Lapa | Skata nosaukums | Skatiet aprakstu | Līdzekļa nosaukums |
|---|---|---|---|
| Ražošanas pasūtījuma MK lapa | Vienkāršoti | Vienkāršotais skats ietver tikai visbiežāk izmantotos laukus. Šādā veidā tas nodrošina ātrāku pārskatu un racionalizētu darba procesu. | Saglabātie skati ražošanas kontrolei<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Ražosanas pasūtījumu informācijas lapa | Vienkāršots | Vienkāršotais skats ietver tikai visbiežāk izmantotos laukus. Šādā veidā tas nodrošina ātrāku pārskatu un racionalizētu darba procesu. | Saglabātie skati ražošanas kontrolei<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Ražošanas pasūtījuma izdošanas saraksta žurnāls | Vienkāršots | Vienkāršotais skats ietver tikai visbiežāk izmantotos laukus. Šādā veidā tas nodrošina ātrāku pārskatu un racionalizētu darba procesu. | Saglabātie skati ražošanas kontrolei<br><br>(Pēc noklusējuma no versijas 10.0.21) |
| Ražošanas pasūtījuma izdošanas saraksta žurnāls | Vienkāršots | Vienkāršotais skats ietver tikai visbiežāk izmantotos laukus. Šādā veidā tas nodrošina ātrāku pārskatu un racionalizētu darba procesu. | Saglabātie skati ražošanas kontrolei<br><br>(Pēc noklusējuma no versijas 10.0.21) |

## <a name="saved-views-for-the-sales-and-marketing-module"></a>Pārdošanas un mārketinga moduļa saglabātie skati

Tabulā ir aprakstīti Pārdošanas un mārketinga modulim pieejamie saglabātie skati.

| Lapa | Skata nosaukums | Skatiet aprakstu | Līdzekļa nosaukums |
|---|---|---|---|
| Pavadzīmju žurnāls | Žurnāla pārskatīšana | Šis vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti pavadzīmju žurnālu pārskatīšanai. | Pārdošanas un mārketinga moduļa saglabātie skati<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Pārdošanas pasūtījums | Pasūtījuma izveide | Šis vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti pārdošanas pasūtījumu izveidei. | Pārdošanas un mārketinga moduļa saglabātie skati<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Pārdošanas pasūtījums | Pasūtījuma pārskats | Šis vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti pārdošanas pasūtījumu pārskatīšanai. | Pārdošanas un mārketinga moduļa saglabātie skati<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Pārdošanas piedāvājums | Piedāvājuma izveide | Šis vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti pārdošanas piedāvājumu izveidei. | Pārdošanas un mārketinga moduļa saglabātie skati<br><br>(Pēc noklusējuma no versijas 10.0.25) |

## <a name="saved-views-for-the-warehouse-management-module"></a>Noliktavas pārvaldības moduļa saglabātie skati

Tabulā ir aprakstīti Noliktavas pārvaldības modulim pieejamie saglabātie skati.

| Lapa | Skata nosaukums | Skatiet aprakstu | Līdzekļa nosaukums |
|---|---|---|---|
| Visas kravas | Ienākošās plūsmas apstrāde | Šis vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti ienākošās kravas plūsmas apstrādei. | Saglabātie skati noslodzes apstrādei<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Visas kravas | Izejošā apstrāde | Šis vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti izejošās kravas plūsmas apstrādei. | Saglabātie skati noslodzes apstrādei<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Visi sūtījumi | Ienākošā apstrāde | Šis vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti ienākošo kravu apstrādei. | Saglabātie skati sūtījuma apstrādei<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Visi sūtījumi | Izejošā apstrāde | Šis vienkāršotais skats ietver tikai tos laukus, kas visbiežāk tiek izmantoti ienākošo kravu apstrādei. | Saglabātie skati sūtījuma apstrādei<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Visi kopumi | Vienkāršots | Vienkāršotais skats ietver tikai visbiežāk izmantotos laukus. Šādā veidā tas nodrošina ātrāku pārskatu un racionalizētu darba procesu. | Saglabāts skats kopuma apstrādei<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Kravu plānošanas rīks | Vienkāršots | Vienkāršotais skats ietver tikai visbiežāk izmantotos laukus. Šādā veidā tas nodrošina ātrāku pārskatu un racionalizētu darba procesu. | Saglabāts skats kravu plānošanas rīkam<br><br>(Pēc noklusējuma no versijas 10.0.25) |
| Detalizēta informācija par darbu | Vienkāršots | Vienkāršotais skats ietver tikai visbiežāk izmantotos laukus. Šādā veidā tas nodrošina ātrāku pārskatu un racionalizētu darba procesu. | Saglabāts skats darba detalizētās informācijas lapai<br><br>(Pēc noklusējuma no versijas 10.0.25) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]