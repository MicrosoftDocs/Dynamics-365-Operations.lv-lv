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
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026696"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Partijas numurs tiek notīrīts, kad ir atlasīts jauns laidiena ID

KB numurs: 4613107

## <a name="symptoms"></a>Simptomi

Kad pārskatāt izdošanas saraksta žurnāla rindu, vērtība laukā **Partijas numurs** tiek notīrīta, ja laukā **Laidiena ID** atlasāt jaunu vērtību.

## <a name="resolution"></a>Novēršana

Sistēma darbojas kā paredzēts. Mainot laidiena ID, tiek mainīts krājuma konteksts. Tāpēc partijas numurs tiek atiestatīts.

Lai partijas numuru saistītu ar laidiena ID, vispirms iestatiet laidiena ID.
