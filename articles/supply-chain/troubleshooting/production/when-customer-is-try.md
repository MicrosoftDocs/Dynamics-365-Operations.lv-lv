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
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="a4177-103">Partijas numurs tiek notīrīts, kad ir atlasīts jauns laidiena ID</span><span class="sxs-lookup"><span data-stu-id="a4177-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="a4177-104">KB numurs: 4613107</span><span class="sxs-lookup"><span data-stu-id="a4177-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="a4177-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="a4177-105">Symptoms</span></span>

<span data-ttu-id="a4177-106">Kad pārskatāt izdošanas saraksta žurnāla rindu, vērtība laukā **Partijas numurs** tiek notīrīta, ja laukā **Laidiena ID** atlasāt jaunu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a4177-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="a4177-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="a4177-107">Resolution</span></span>

<span data-ttu-id="a4177-108">Sistēma darbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="a4177-108">The system is behaving as designed.</span></span> <span data-ttu-id="a4177-109">Mainot laidiena ID, tiek mainīts krājuma konteksts.</span><span class="sxs-lookup"><span data-stu-id="a4177-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="a4177-110">Tāpēc partijas numurs tiek atiestatīts.</span><span class="sxs-lookup"><span data-stu-id="a4177-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="a4177-111">Lai partijas numuru saistītu ar laidiena ID, vispirms iestatiet laidiena ID.</span><span class="sxs-lookup"><span data-stu-id="a4177-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
