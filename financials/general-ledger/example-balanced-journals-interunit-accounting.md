---
title: "Saskaņoti starpvienību uzskaites žurnāli"
description: "Šajā rakstā ir izskaidrots, kā automātiski tiek noteikts žurnāla atlikums, ja lapā Virsgrāmata ir atlasīta finanšu dimensijas atlikuma noteikšana."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 8b6fda79222905b0df211a0b944aca9e4dc76850
ms.lasthandoff: 03/31/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>Saskaņoti starpvienību uzskaites žurnāli

[!include[banner](../includes/banner.md)]


Šajā rakstā ir izskaidrots, kā automātiski tiek noteikts žurnāla atlikums, ja lapā Virsgrāmata ir atlasīta finanšu dimensijas atlikuma noteikšana. 

Ja konta ieraksti nav saskaņoti finanšu dimensijas vērtību līmenī, tiek automātiski izveidoti papildu kona ieraksti, lai saskaņotu žurnālu. Šie konta ieraksti izmanto grāmatošanas tipus **Starpvienību uzskaite — debets** un **Starpvienību uzskaite — kredīts** lapā **Automātisko darījumu konti**, lai noteiktu galveno kontu. Piemēram, kā saskaņošanas finanšu dimensija tiek atlasīta dimensija Filiāle, kas ir otrais virsgrāmatas konta segments, un tiks izveidoti tālāk norādītie uzskaites ieraksti.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

Šādā gadījumā tiek noteiktas tālāk norādītās bilances.

-   Filiālei MSP = 100,00 CR
-   Filiālei NY = 100,00 DR

Tāpēc tiek automātiski izveidoti tālāk norādītie uzskaites ieraksti, lai saskaņotu žurnālu finanšu dimensijas vērtību līmenī.

|                                   |           |
|-----------------------------------|-----------|
| (Starpvienību debets) – MSP – OU\_256 | 100.00 DR |
| (Starpvienību kredīts) – NY – OU\_249 | 100.00 CR |






