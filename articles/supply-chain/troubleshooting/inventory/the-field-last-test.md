---
title: Pēdējā pārbaudītā datuma lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi
description: Pēdējā pārbaudītā datuma lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026722"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="7f42f-103">Pēdējā pārbaudītā datuma lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="7f42f-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="7f42f-104">KB numurs: 4612803</span><span class="sxs-lookup"><span data-stu-id="7f42f-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="7f42f-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="7f42f-105">Symptoms</span></span>

<span data-ttu-id="7f42f-106">**Pēdējā pārbaudītā datuma** lauks netiek atjaunināts, ja tiek izveidoti vairāki kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="7f42f-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="7f42f-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="7f42f-107">Resolution</span></span>

<span data-ttu-id="7f42f-108">Sistēma darbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="7f42f-108">The system is behaving as designed.</span></span> <span data-ttu-id="7f42f-109">Pēdējais pārbaudītais datums nav saistīts ar kvalitātes pārbaudes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="7f42f-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="7f42f-110">Tajā tiek glabāts datums, kad pabeigtās preces tikušas pirmo reizi iegādātas vai saražotas.</span><span class="sxs-lookup"><span data-stu-id="7f42f-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="7f42f-111">Šis datums tiek izmantots, lai aprēķinātu glabāšanas laika izziņas datumu.</span><span class="sxs-lookup"><span data-stu-id="7f42f-111">This date is used to calculate the shelf life advice date.</span></span>
