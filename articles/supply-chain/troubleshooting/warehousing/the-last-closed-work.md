---
title: Pēdējās slēgtās darba rindas statusam ir jābūt izvietotam
description: Pēdējās slēgtās darba rindas statusam ir jābūt izvietotam
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 221c64c89d0e8addbf44acab8e7561e5f3a27239
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474752"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a>Pēdējās slēgtās darba rindas statusam ir jābūt izvietotam

Kļūdas kods: WAX1285

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Pēdējās slēgtās darba rindas statusam ir jābūt izvietotam.

## <a name="cause"></a>Iemesls

Darbu nevar atcelt tā pašreizējā stāvoklī.

Pēdējā darba rindā lauks **darba statuss** ir iestatīts uz *Slēgts*, bet lauks **Darba veids** nav iestatīts kā *Ievietot*.

## <a name="resolution"></a>Novēršana

Lai atceltu darbu, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.
1. Laukā **Darba ID** norādiet darba ID, ko vēlaties atcelt.
1. Atlasiet **Labi**.
1. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.

Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).
