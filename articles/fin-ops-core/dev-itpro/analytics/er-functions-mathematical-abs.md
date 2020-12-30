---
title: ABS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ABS elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3c7156b9990397822a6bea9ed8b3df8f65490572
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683285"
---
# <a name="abs-er-function"></a><span data-ttu-id="bb99f-103">ABS ER funkcija</span><span class="sxs-lookup"><span data-stu-id="bb99f-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb99f-104">`ABS` funkcija atgriež norādītā numura absolūto vērtību (moduli) kā *Reālu* vērtību.</span><span class="sxs-lookup"><span data-stu-id="bb99f-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="bb99f-105">Tas ir, tā atgriež skaitli bez tā zīmes.</span><span class="sxs-lookup"><span data-stu-id="bb99f-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb99f-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="bb99f-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="bb99f-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="bb99f-107">Arguments</span></span>

<span data-ttu-id="bb99f-108">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="bb99f-108">`number`: *Real*</span></span>

<span data-ttu-id="bb99f-109">Skaitliska vērtība, kurai vēlaties izveidot moduli.</span><span class="sxs-lookup"><span data-stu-id="bb99f-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="bb99f-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="bb99f-110">Return values</span></span>

<span data-ttu-id="bb99f-111">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="bb99f-111">*Real*</span></span>

<span data-ttu-id="bb99f-112">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="bb99f-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="bb99f-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="bb99f-113">Example</span></span>

<span data-ttu-id="bb99f-114">`ABS (-1)` atgriež **1**.</span><span class="sxs-lookup"><span data-stu-id="bb99f-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb99f-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bb99f-115">Additional resources</span></span>

[<span data-ttu-id="bb99f-116">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="bb99f-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
