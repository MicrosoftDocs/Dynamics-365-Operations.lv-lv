---
title: ROUND ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUND elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 83fb5c04938e0aba1277f2d6017d4b66208a8858
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683260"
---
# <a name="round-er-function"></a><span data-ttu-id="c825c-103">ROUND ER funkcija</span><span class="sxs-lookup"><span data-stu-id="c825c-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c825c-104">`ROUND` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="c825c-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="c825c-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="c825c-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="c825c-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="c825c-106">Arguments</span></span>

<span data-ttu-id="c825c-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="c825c-107">`number`: *Real*</span></span>

<span data-ttu-id="c825c-108">Skaitliska vērtība, kas ir jānoapaļo.</span><span class="sxs-lookup"><span data-stu-id="c825c-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="c825c-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="c825c-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="c825c-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="c825c-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="c825c-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="c825c-111">Return values</span></span>

<span data-ttu-id="c825c-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="c825c-112">*Real*</span></span>

<span data-ttu-id="c825c-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="c825c-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c825c-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="c825c-114">Usage notes</span></span>

<span data-ttu-id="c825c-115">Ja argumenta `decimals` vērtība ir lielāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz attiecīgajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="c825c-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="c825c-116">Ja argumenta `decimals` vērtība ir **0** (nulle), norādītais skaitlis tiek noapaļots līdz tuvākajam veselajam pāra skaitlim.</span><span class="sxs-lookup"><span data-stu-id="c825c-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="c825c-117">Ja argumenta `decimals` vērtība ir mazāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz skaitlim, kas atrodas pa kreisi no komata.</span><span class="sxs-lookup"><span data-stu-id="c825c-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="c825c-118">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="c825c-118">Example 1</span></span>

<span data-ttu-id="c825c-119">`ROUND (1200.767, 2)` noapaļo līdz diviem cipariem aiz komata un atgriež **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="c825c-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c825c-120">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="c825c-120">Example 2</span></span>

<span data-ttu-id="c825c-121">`ROUND (1200.767, -3)` noapaļo līdz tuvākajam 1 000 reizinājumam un atgriež **1000**.</span><span class="sxs-lookup"><span data-stu-id="c825c-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="c825c-122">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="c825c-122">Example 3</span></span>

<span data-ttu-id="c825c-123">`ROUND (1200.5, 0)` noapaļo līdz tuvākajam veselajam pāra skaitlim un atgriež **1200**, bet `ROUND (1201.5, 0)` dara to pašu un atgriež **1202**.</span><span class="sxs-lookup"><span data-stu-id="c825c-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c825c-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c825c-124">Additional resources</span></span>

[<span data-ttu-id="c825c-125">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="c825c-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)
