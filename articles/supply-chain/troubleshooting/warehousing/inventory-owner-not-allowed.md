---
title: Krājuma īpašnieks nav atļauts, apstrādājot kustību
description: Iespējams, saņemsit kļūdu "Krājuma īpašnieks %1 nav atļauts." Noliktavas pārvaldības procesi atbalsta tikai krājumu, kas pieder juridiskai personai.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4ee29cfc7bad990cd1ee5deaa98fca217af772ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476960"
---
# <a name="inventory-owner-not-allowed-when-processing-movements-in-the-warehouse-app"></a>Krājuma īpašnieks nav atļauts, apstrādājot kustību noliktavas lietojumprogrammā

## <a name="symptoms"></a>Simptomi

Apstrādājot kustību Warehouse Management mobilajā programmā, iespējams, saņemsit šādu kļūdas ziņojumu:

> Krājuma īpašnieks %1 nav atļauts Šajā procesā.

## <a name="cause"></a>Iemesls

Tā notiek jo trūkst **Īpašnieka** izsekošanas dimensijas, kad Warehouse Management mobilā programma tiek izmantota kustību veikšanai. Regulārs krājumu pārsūtīšanas žurnāls no Supply Chain Management klienta tiek rādīts, lai darbotos, kā paredzēts, un to var grāmatot tikai tad, ja ir ievadīta **Īpašnieka** dimensija.

## <a name="resolution"></a>Novēršana

Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums. Pašlaik noliktavas pārvaldības procesi atbalsta tikai tos krājumus, kas pieder juridiskai personai.
