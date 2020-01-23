---
title: OR ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota OR elektroniskā pārskata (ER) funkcija.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917124"
---
# <span data-ttu-id="16fca-103"><a name="OR">OR ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="16fca-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16fca-104">`OR` funkcija atgriež *Būla* vērtību **FALSE**, ja visi norādītie nosacījumi ir nepatiesi.</span><span class="sxs-lookup"><span data-stu-id="16fca-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="16fca-105">Šī funkcija atgriež *Būla* vērtību **TRUE**, ja jebkurš norādītais nosacījums ir patiess.</span><span class="sxs-lookup"><span data-stu-id="16fca-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="16fca-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="16fca-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="16fca-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="16fca-107">Arguments</span></span>

<span data-ttu-id="16fca-108">`condition 1`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="16fca-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="16fca-109">Derīga nosacījuma izteiksme, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="16fca-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="16fca-110">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="16fca-110">This argument is required.</span></span>

<span data-ttu-id="16fca-111">`condition N`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="16fca-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="16fca-112">Derīga nosacījuma izteiksme, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="16fca-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="16fca-113">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="16fca-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="16fca-114">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="16fca-114">Return values</span></span>

<span data-ttu-id="16fca-115">*Būla*</span><span class="sxs-lookup"><span data-stu-id="16fca-115">*Boolean*</span></span>

<span data-ttu-id="16fca-116">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="16fca-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="16fca-117">Paraugs</span><span class="sxs-lookup"><span data-stu-id="16fca-117">Example</span></span>

<span data-ttu-id="16fca-118">`OR (1=2, "a"="a")` atgriež **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="16fca-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16fca-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="16fca-119">Additional resources</span></span>

[<span data-ttu-id="16fca-120">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="16fca-120">Logical functions</span></span>](er-functions-category-logical.md)
