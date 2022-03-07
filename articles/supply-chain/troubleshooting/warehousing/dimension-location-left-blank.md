---
title: Dimensijas atrašanās vieta nevar būt tukša, ja ir iestatīts sērijas numurs
description: Ja pēc sērijas vienuma pārsūtīšanas pasūtījuma izveidnes sūtījuma apstiprināšanas saņemat šo kļūdas ziņojumu, noklusējuma saņemšanas vietas lauks ir tukšs.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477020"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Kļūda, apstiprinot sūtījumu pēc sērijas vienuma pārsūtīšanas pasūtīšanas izveidnes

## <a name="symptoms"></a>Simptomi

Ja izveidojat sērijas vienuma pārsūtīšanas pasūtījumu, izmantojot noliktavu, kurai ir iespējota papildu noliktavas pārvaldība (WMS), un pēc tam mēģināt apstiprināt sūtīšanu pēc darba beigām, jūs saņemsit šādu kļūdas ziņojumu:

> Dimensijas atrašanās vieta nevar būt tukša, ja ir iestatīts dimensijas sērijas numurs

## <a name="cause"></a>Iemesls

Tā notiek, jo lauks **Noklusējuma saņemšanas vieta** ir tukšs pārsūtīšanas noliktavai no nosūtīšanas noliktavas.

## <a name="resolution"></a>Novēršana

Lai labotu šo problēmu, norādiet noklusēto ieejas plūsmas vietu tranzīta noliktavā. Pārliecinieties, ka šī vieta tiek pārvaldīta ar numura zīmi.
