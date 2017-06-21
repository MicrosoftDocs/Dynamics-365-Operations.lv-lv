---
title: "Saskaņoti starpvienību uzskaites žurnāli"
description: "Šajā rakstā ir izskaidrots, kā automātiski tiek noteikts žurnāla atlikums, ja lapā Virsgrāmata ir atlasīta finanšu dimensijas atlikuma noteikšana."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0909b64a77024d551af0dad2de985887cf6ff06d
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


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






