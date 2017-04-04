---
title: "Krājumu žurnālu pārskatiem"
description: "Lietojot konfigurējamu krājumu atskaitēm, kas balstītas uz elektronisko atskaišu, jums iestatīt relāciju starp konkrēto atskaiti un žurnāla tips."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalName
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265144
ms.assetid: 0f07f62f-1053-46e9-b235-a7b38cbda409
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: eed3398651612743958722814ec5594ec34e4e5e
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-journal-reports"></a>Krājumu žurnālu pārskatiem

Lietojot konfigurējamu krājumu atskaitēm, kas balstītas uz elektronisko atskaišu, jums iestatīt relāciju starp konkrēto atskaiti un žurnāla tips.

Izveidot attiecības starp konkrēto atskaiti un žurnāla tipā, uz **krājumu žurnālu nosaukumus** lapas (**krājumu vadība**&gt;**Setup**&gt;**žurnālu nosaukumus**&gt;**krājumu**), ievadīt atskaites nosaukumu. **Piezīme:** iestatīt atbalstīto sastāvi, lejupielādēt nepieciešamo elektronisko atskaišu konfigurācijas. Lai iegūtu papildinformāciju, skatiet [Download elektroniskās ziņošanas no Lifecycle Services konfigurācijas](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Ar atbalstīto konfigurācijas Eiropā noliktavas atskaišu piemēri ir uzskaitīti tabulā turpmāk.
|                    |                                     |                  |                                         |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| **Country**        | **Atskaites apraksts**              | **Journal type** | **Kartējuma nosaukumu formātu**                 |
| Lietuva, Ungārija | Krājumu pārskatu          | Inventarizācija         | Inventarizācijas akts (HU, LT)            |
| Latvija, Polija     | Krājumu pārklasificēšanas dokuments | Pārsūtījums         | InventoryReclassificationDocument\_PLLV |
| Igaunija            | Krājumu pārklasificēšanas dokuments | Pārsūtījums         | InventoryReclassificationDocument\_EE   |
| Polija             | Iekšējā PW/RW                      | Kustība         | InventJournalLinesDocPL                 |
| Latvija             |  Krājumu kustības dokuments         | Kustība         | Kustības\_LV                            |
| Latvija             | Dokumentu krājumu vērtības norakstīšana       | Pielāgojums       | InventJournalLines\_LV                  |
| Latvija             | Pārvietojuma pavadzīme              | Pārsūtījums         | InternalTransferDeliveryNote\_LV        |
| Latvija             | Inventarizācijas dokumentu pārskats            | Inventarizācija         | CountedDocument\_LV                     |
| Latvija             | Inventarizācijas saraksta pārskats                | Inventarizācija         | Inventarizācijas saraksts                           |




