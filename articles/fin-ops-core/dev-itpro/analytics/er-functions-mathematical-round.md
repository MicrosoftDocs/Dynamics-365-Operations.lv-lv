---
title: ROUND ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUND elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 716ac0bbc9fec992ec1bbfc99bfc86434bf97984
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570402"
---
# <a name="round-er-function"></a><span data-ttu-id="595a3-103">ROUND ER funkcija</span><span class="sxs-lookup"><span data-stu-id="595a3-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="595a3-104">`ROUND` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="595a3-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="595a3-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="595a3-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="595a3-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="595a3-106">Arguments</span></span>

<span data-ttu-id="595a3-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="595a3-107">`number`: *Real*</span></span>

<span data-ttu-id="595a3-108">Skaitliska vērtība, kas ir jānoapaļo.</span><span class="sxs-lookup"><span data-stu-id="595a3-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="595a3-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="595a3-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="595a3-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="595a3-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="595a3-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="595a3-111">Return values</span></span>

<span data-ttu-id="595a3-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="595a3-112">*Real*</span></span>

<span data-ttu-id="595a3-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="595a3-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="595a3-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="595a3-114">Usage notes</span></span>

<span data-ttu-id="595a3-115">Ja argumenta `decimals` vērtība ir lielāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz attiecīgajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="595a3-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="595a3-116">Ja argumenta `decimals` vērtība ir **0** (nulle), norādītais skaitlis tiek noapaļots līdz tuvākajam veselajam pāra skaitlim.</span><span class="sxs-lookup"><span data-stu-id="595a3-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="595a3-117">Ja argumenta `decimals` vērtība ir mazāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz skaitlim, kas atrodas pa kreisi no komata.</span><span class="sxs-lookup"><span data-stu-id="595a3-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="595a3-118">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="595a3-118">Example 1</span></span>

<span data-ttu-id="595a3-119">`ROUND (1200.767, 2)` noapaļo līdz diviem cipariem aiz komata un atgriež **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="595a3-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="595a3-120">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="595a3-120">Example 2</span></span>

<span data-ttu-id="595a3-121">`ROUND (1200.767, -3)` noapaļo līdz tuvākajam 1 000 reizinājumam un atgriež **1000**.</span><span class="sxs-lookup"><span data-stu-id="595a3-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="595a3-122">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="595a3-122">Example 3</span></span>

<span data-ttu-id="595a3-123">`ROUND (1200.5, 0)` noapaļo līdz tuvākajam veselajam pāra skaitlim un atgriež **1200**, bet `ROUND (1201.5, 0)` dara to pašu un atgriež **1202**.</span><span class="sxs-lookup"><span data-stu-id="595a3-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="595a3-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="595a3-124">Additional resources</span></span>

[<span data-ttu-id="595a3-125">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="595a3-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]