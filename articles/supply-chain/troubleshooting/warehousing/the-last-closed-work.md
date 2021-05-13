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
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924379"
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
