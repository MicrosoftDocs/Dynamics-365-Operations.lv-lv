---
title: ABS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ABS elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a3613483d53fb265741b5d6a34a91da443dcef7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753148"
---
# <a name="abs-er-function"></a><span data-ttu-id="69e7a-103">ABS ER funkcija</span><span class="sxs-lookup"><span data-stu-id="69e7a-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69e7a-104">`ABS` funkcija atgriež norādītā numura absolūto vērtību (moduli) kā *Reālu* vērtību.</span><span class="sxs-lookup"><span data-stu-id="69e7a-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="69e7a-105">Tas ir, tā atgriež skaitli bez tā zīmes.</span><span class="sxs-lookup"><span data-stu-id="69e7a-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e7a-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="69e7a-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="69e7a-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="69e7a-107">Arguments</span></span>

<span data-ttu-id="69e7a-108">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="69e7a-108">`number`: *Real*</span></span>

<span data-ttu-id="69e7a-109">Skaitliska vērtība, kurai vēlaties izveidot moduli.</span><span class="sxs-lookup"><span data-stu-id="69e7a-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="69e7a-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="69e7a-110">Return values</span></span>

<span data-ttu-id="69e7a-111">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="69e7a-111">*Real*</span></span>

<span data-ttu-id="69e7a-112">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="69e7a-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="69e7a-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="69e7a-113">Example</span></span>

<span data-ttu-id="69e7a-114">`ABS (-1)` atgriež **1**.</span><span class="sxs-lookup"><span data-stu-id="69e7a-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69e7a-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="69e7a-115">Additional resources</span></span>

[<span data-ttu-id="69e7a-116">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="69e7a-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]