---
title: Noliktava izdošanas saraksta žurnālā nav atjaunināta MK rindā.
description: Noliktava izdošanas saraksta žurnālā nav atjaunināta materiālu komplekta (MK) rindā.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026702"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a><span data-ttu-id="36862-103">Noliktava izdošanas saraksta žurnālā nav atjaunināta MK rindā</span><span class="sxs-lookup"><span data-stu-id="36862-103">The warehouse in the picking list journal isn't updated on a BOM line</span></span>

<span data-ttu-id="36862-104">KB numurs: 4614848</span><span class="sxs-lookup"><span data-stu-id="36862-104">KB number: 4614848</span></span>

## <a name="symptoms"></a><span data-ttu-id="36862-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="36862-105">Symptoms</span></span>

<span data-ttu-id="36862-106">Noliktava izdošanas saraksta žurnālā nav atjaunināta materiālu komplekta (MK) rindā.</span><span class="sxs-lookup"><span data-stu-id="36862-106">The warehouse in the picking list journal isn't updated on a bill of materials (BOM) line.</span></span>

## <a name="resolution"></a><span data-ttu-id="36862-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="36862-107">Resolution</span></span>

<span data-ttu-id="36862-108">Sistēma darbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="36862-108">The system is behaving as designed.</span></span> <span data-ttu-id="36862-109">Ja izdošanas saraksta žurnāla rinda ir izveidota, kam ir atsauce (izmantojot laidiena ID) uz ražošanas MK rindu, noliktava ražošanas MK rindā netiks atjaunināta, ja noliktavas dimensija ražošanas izdošanas saraksta žurnāla rindā tiks mainīta vēlāk.</span><span class="sxs-lookup"><span data-stu-id="36862-109">If a picking list journal line is created that has a reference (via the lot ID) to a production BOM line, the warehouse on the production BOM line won't be updated if the warehouse dimension on the production picking list journal line is changed later.</span></span>
