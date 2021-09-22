---
title: Rīcībā esošie krājumi, kas nav ņemti vērā attiecībā uz vienībām virs partijas
description: Dažas slotu veidnes apsver pašreizējos rīcībā esošos krājumus vienībām virs partijas. Partijas vai sērijas numurs ir jānorāda pieprasījuma pasūtījumā.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476984"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Slotu veidnes apsver rīcībā esošos krājumus vienībām virs partijas

## <a name="symptoms"></a>Simptomi

Nišu veidnes, kurām ir *Rīcībā esošais nišas kritērijs*, neuztver pašreizējos rīcībā esošos krājumus *virs partijas* iespējotiem krājumiem. Viņi to apsver, ja partijas numurs ir norādīts pārdošanas pasūtījuma rindā.

Tomēr, ja izmantojat partijas krājumus, kas ir *zemāki par krājumiem*, pašreizējie rīcībā esošie krājumi tiek uzskatīti par paredzamiem.

Plašāku informāciju skatiet [Noliktavas niša](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Novēršana

Slotēšanas veidnes virsrakstu var definēt stratēģijai *Pasūtīts*, *Rezervēts* vai *Nodots izpildei*. *Pasūtītā* pieprasījuma stratēģijai tiek lietotas tās pašas rezervāciju hierarhijas prasības, kas attiecas uz rezervācijas vai izlaišanas noliktavas procesiem. Tāpēc krājumiem, kuru pakešuzdevums atrodas *virs* un sērijas atrodas *zem* rezervāciju hierarhijām, pieprasījuma pasūtījumā (pārdošana vai pārsūtīšana) ir jānorāda paketes vai sērijas numurs.

Alternatīvi *Rezervētā* pieprasījuma stratēģiju var izmantot, lai atlasītu partiju vai sērijas numuru pirms noliktavas pieprasījuma ģenerēšanas noliktavas slotā.
