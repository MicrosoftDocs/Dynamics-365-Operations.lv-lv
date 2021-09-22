---
title: Numura zīmei jābūt konkretizētai šai vietai
description: Ja pēc pārsūtīšanas pasūtījuma izveidnes WMS iespējotai noliktavai saņemat šo kļūdas ziņojumu, noklusējuma saņemšanas atrašanās vietas lauks pārsūtīšanas noliktavai ir tukšs.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476951"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Numura zīmes konkretizēšanas kļūda, apstiprinot pārsūtīšanas pasūtījuma sūtīšanu

## <a name="symptoms"></a>Simptomi

Ja izveidojat pārsūtīšanas pasūtījumu, izmantojot noliktavu, kurai ir iespējota papildu noliktavas pārvaldība (WMS), un pēc tam mēģināt apstiprināt sūtīšanu pēc darba beigām, iespējams, saņemsit šādu kļūdas ziņojumu:

> Šim novietojumam jābūt norādītai numura zīmei.

## <a name="cause"></a>Iemesls

Tā notiek, jo lauks **Noklusējuma saņemšanas vieta** ir tukšs pārsūtīšanas noliktavai no nosūtīšanas noliktavas.

## <a name="resolution"></a>Novēršana

Lai labotu šo problēmu, norādiet noklusēto ieejas plūsmas vietu tranzīta noliktavā. Pārliecinieties, ka šī vieta tiek pārvaldīta ar numura zīmi.
