---
title: Uzsāktā karantīnas pasūtījuma daudzums netiek atjaunināts, ja pasūtījums ir sadalīts
description: Veidojot karantīnas pasūtījumu un mēģinot to sadalīt, pasūtījuma daudzums netiek atjaunināts uz sadalīto atlikušo daudzumu.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026724"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="7a9d0-103">Uzsāktā karantīnas pasūtījuma daudzums netiek atjaunināts, ja pasūtījums ir sadalīts</span><span class="sxs-lookup"><span data-stu-id="7a9d0-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="7a9d0-104">KB numurs: 4613113</span><span class="sxs-lookup"><span data-stu-id="7a9d0-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="7a9d0-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="7a9d0-105">Symptoms</span></span>

<span data-ttu-id="7a9d0-106">Veidojot karantīnas pasūtījumu un mēģinot to sadalīt, pasūtījuma daudzums netiek atjaunināts uz atlikušo daudzumu pēc sadalīšanas.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="7a9d0-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="7a9d0-107">Resolution</span></span>

<span data-ttu-id="7a9d0-108">Sistēma nemaina sākotnējo daudzumu no karantīnas pasūtījuma, lai nodrošinātu, ka varat izsekot sākotnējam daudzumam, kas tika izveidots šim karantīnas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="7a9d0-109">Tomēr sistēma izseko daudzumu, kas ir sadalīts no karantīnas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="7a9d0-110">Lai to paveiktu, tā izmanto datu bāzes lauku ar nosaukumu `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="7a9d0-111">Tomēr šis lauks nav redzams lietotāja interfeisā (user interface — UI).</span><span class="sxs-lookup"><span data-stu-id="7a9d0-111">However, this field isn't visible in the user interface (UI).</span></span>
