---
title: Darbu nevar atcelt, tā statusa dēļ
description: Darbu nevar atcelt, tā statusa dēļ
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
ms.openlocfilehash: f983501b490c5516525b4d5904603ed62e8799f9e6124e5672b36a12804ecb0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755982"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>Darbu nevar atcelt, tā statusa dēļ

Kļūdas kods: WAX2190

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Darbu %1 nevar atcelt, jo tā statuss ir %2.

## <a name="cause"></a>Iemesls

Darbu nevar atcelt tā pašreizējā stāvoklī.

Darba virsrakstam vai darba rindām nav paredzamā vērtība **Darba statuss**. Lauks **Darba statuss** darba virsrakstā nav iestatīts uz *Atvērts* vai *Notiek*.

## <a name="resolution"></a>Novēršana

Lai atceltu darbu, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.
1. Laukā **Darba ID** norādiet darba ID, ko vēlaties atcelt.
1. Atlasiet **Labi**.
1. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.

Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).
