---
title: "Saskaņoti starpvienību uzskaites žurnāli"
description: "Šajā rakstā ir izskaidrots, kā automātiski tiek noteikts žurnāla atlikums, ja lapā Virsgrāmata ir atlasīta finanšu dimensijas atlikuma noteikšana."
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5b1d788ebd5617a1d3f1c8ca36f5ae3c29b534c5
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a>Saskaņoti starpvienību uzskaites žurnāli

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā automātiski tiek noteikts žurnāla atlikums, ja lapā Virsgrāmata ir atlasīta finanšu dimensijas atlikuma noteikšana. 

Ja konta ieraksti nav saskaņoti finanšu dimensijas vērtību līmenī, tiek automātiski izveidoti papildu kona ieraksti, lai saskaņotu žurnālu. Šie konta ieraksti izmanto grāmatošanas tipus **Starpvienību uzskaite — debets** un **Starpvienību uzskaite — kredīts** lapā **Automātisko darījumu konti**, lai noteiktu galveno kontu. Piemēram, kā saskaņošanas finanšu dimensija tiek atlasīta dimensija Struktūrvienība, kas ir otrais virsgrāmatas konta segments, un tiks izveidoti tālāk norādītie uzskaites ieraksti.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

Šādā gadījumā tiek noteiktas tālāk norādītās bilances.

-   Struktūrvienībai MSP = 100,00 CR
-   Struktūrvienībai NY = 100,00 DR

Tāpēc tiek automātiski izveidoti tālāk norādītie uzskaites ieraksti, lai saskaņotu žurnālu finanšu dimensijas vērtību līmenī.

|                                   |           |
|-----------------------------------|-----------|
| (Starpvienību debets) – MSP – OU\_256 | 100.00 DR |
| (Starpvienību kredīts) – NY – OU\_249 | 100.00 CR |






