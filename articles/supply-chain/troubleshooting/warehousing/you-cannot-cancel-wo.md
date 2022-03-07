---
title: Nevar atcelt lietotājam izveidotu darbu
description: Nevar atcelt lietotājam izveidotu darbu
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
ms.openlocfilehash: 1d7b0140d0c2724234a549ca4dfb23109012654abe0e60fcea1f98e8f17c153a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748695"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>Nevar atcelt lietotājam izveidotu darbu

Kļūdas kods: WAX708

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Nevar atcelt lietotājam piešķirtu darbu.

## <a name="cause"></a>Iemesls

Darbu ir bloķējis lietotājs, un to nevar atcelt. Lai to apstiprinātu, atveriet darba ID un pēc tam atveriet cilni **Vispārīgi**. Ja darbs ir bloķēts, lauks **Darba statuss** tiks iestatīts uz *Notiek* un lauks **Bloķēts** tiks iestatīts uz lietotāja ID.

## <a name="resolution"></a>Novēršana

Lai atceltu darbu, veiciet tālāk norādītās darbības.

1. Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.
1. Laukā **Darba ID** norādiet darba ID, ko vēlaties atcelt.
1. Atlasiet **Labi**.
1. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.

Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).
