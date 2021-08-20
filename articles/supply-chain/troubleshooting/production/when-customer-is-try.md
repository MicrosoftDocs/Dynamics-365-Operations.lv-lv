---
title: Partijas numurs tiek notīrīts, kad ir atlasīts jauns laidiena ID
description: Kad pārskatāt izdošanas saraksta žurnāla rindu, vērtība laukā Partijas numurs tiek notīrīta, ja laukā Laidiena ID atlasāt jaunu vērtību.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d71720b1d3a34a31639db0f829dee300d6f96d53fd61c0a8740be9f2306d6dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738823"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Partijas numurs tiek notīrīts, kad ir atlasīts jauns laidiena ID

KB numurs: 4613107

## <a name="symptoms"></a>Simptomi

Kad pārskatāt izdošanas saraksta žurnāla rindu, vērtība laukā **Partijas numurs** tiek notīrīta, ja laukā **Laidiena ID** atlasāt jaunu vērtību.

## <a name="resolution"></a>Novēršana

Sistēma darbojas kā paredzēts. Mainot laidiena ID, tiek mainīts krājuma konteksts. Tāpēc partijas numurs tiek atiestatīts.

Lai partijas numuru saistītu ar laidiena ID, vispirms iestatiet laidiena ID.
