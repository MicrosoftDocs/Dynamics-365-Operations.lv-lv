---
title: Vienuma RM nevar rezervēt, kad tiek izlaists ražošanas pasūtījums
description: 'Izlaizot ražošanas pasūtījumu, iespējams, saņemsit kļūdas ziņojumu: "Vienuma RM nav iespējams pilnībā rezervēt." Nodrošiniet, ka pilns daudzums ir pieejams, vai rezervējiet vienumus manuāli.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477011"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Vienuma RM nevar pilnībā rezervēt, kad tiek izlaists ražošanas pasūtījums

## <a name="symptoms"></a>Simptomi

Ja ne visi BOM rindas vienumi ir fiziski pieejami, kad uz noliktavu tiek izlaists ražošanas pasūtījums, un politika **Izlaist uz noliktavu** tiek iestatīta uz opciju *Vajadzīga pilna rezervācija*, tiks saņemts šāds kļūdas ziņojums:

> Krājumu RM nevarēja pilnībā rezervēt. Pārliecinieties, vai ir pieejams pilns daudzums vai rezervējiet krājumus manuāli, ja lauks Rezervācija MK rindā ir iestatīts uz Manuāli vai Sākts. Nevarēja izlaist pasūtījumu nosūtīšanai uz noliktavu, jo dažus materiālus nevarēja rezervēt.

## <a name="resolution"></a>Novēršana

Šī darbība ir pēc dizaina, un tā darbojas, kā paredzēts. Lai novērstu šo problēmu, izpildiet norādījumus, kas sniegti kļūdas ziņojumā: "Nodrošiniet, ka pilnais daudzums ir pieejams, vai rezervējiet vienumus manuāli, ja BOM rindas rezervācijas lauks ir iestatīts uz vērtību Manuāla vai Uzsākta."
