---
title: AND ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota AND elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 8ccb7feb1d0f6836e7e8001870034900f6a1f598
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687078"
---
# <a name="and-er-function"></a><span data-ttu-id="07751-103">AND ER funkcija</span><span class="sxs-lookup"><span data-stu-id="07751-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07751-104">`AND` funkcija atgriež *Būla* vērtību **TRUE**, ja visi norādītie nosacījumi ir patiesi.</span><span class="sxs-lookup"><span data-stu-id="07751-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="07751-105">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="07751-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="07751-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="07751-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="07751-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="07751-107">Arguments</span></span>

<span data-ttu-id="07751-108">`condition 1`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="07751-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="07751-109">Derīga nosacījuma izteiksme, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="07751-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="07751-110">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="07751-110">This argument is required.</span></span>

<span data-ttu-id="07751-111">`condition N`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="07751-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="07751-112">Derīga nosacījuma izteiksme, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="07751-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="07751-113">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="07751-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="07751-114">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="07751-114">Return values</span></span>

<span data-ttu-id="07751-115">*Būla*</span><span class="sxs-lookup"><span data-stu-id="07751-115">*Boolean*</span></span>

<span data-ttu-id="07751-116">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="07751-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="07751-117">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="07751-117">Usage notes</span></span>

<span data-ttu-id="07751-118">Loģisko funkciju argumentos var izmantot datu avota atsauces, skaitliskās un teksta vērtības, Būla vērtības, salīdzināšanas operatorus un citas elektronisko pārskatu (ER) funkcijas.</span><span class="sxs-lookup"><span data-stu-id="07751-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="07751-119">Tomēr visi argumenti ir jānovērtē ar *Būla* vērtību **TRUE** vai **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="07751-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="07751-120">Paraugs</span><span class="sxs-lookup"><span data-stu-id="07751-120">Example</span></span>

<span data-ttu-id="07751-121">`AND (1=1, "a"="a")` atgriež **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="07751-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="07751-122">`AND (1=2, "a"="a")` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="07751-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07751-123">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="07751-123">Additional resources</span></span>

[<span data-ttu-id="07751-124">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="07751-124">Logical functions</span></span>](er-functions-category-logical.md)
