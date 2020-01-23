---
title: ROUND ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUND elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917078"
---
# <span data-ttu-id="118b4-103"><a name="ROUND">ROUND ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="118b4-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="118b4-104">`ROUND` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="118b4-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="118b4-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="118b4-105">Syntax</span></span>

```
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="118b4-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="118b4-106">Arguments</span></span>

<span data-ttu-id="118b4-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="118b4-107">`number`: *Real*</span></span>

<span data-ttu-id="118b4-108">Skaitliska vērtība, kas ir jānoapaļo.</span><span class="sxs-lookup"><span data-stu-id="118b4-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="118b4-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="118b4-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="118b4-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="118b4-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="118b4-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="118b4-111">Return values</span></span>

<span data-ttu-id="118b4-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="118b4-112">*Real*</span></span>

<span data-ttu-id="118b4-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="118b4-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="118b4-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="118b4-114">Usage notes</span></span>

<span data-ttu-id="118b4-115">Ja argumenta `decimals` vērtība ir lielāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz attiecīgajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="118b4-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="118b4-116">Ja argumenta `decimals` vērtība ir **0** (nulle), norādītais skaitlis tiek noapaļots līdz tuvākajam veselajam skaitlim.</span><span class="sxs-lookup"><span data-stu-id="118b4-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="118b4-117">Ja argumenta  `decimals` vērtība ir mazāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz skaitlim, kas atrodas pa kreisi no komata.</span><span class="sxs-lookup"><span data-stu-id="118b4-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="118b4-118">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="118b4-118">Example 1</span></span>

<span data-ttu-id="118b4-119">`ROUND (1200.767, 2)` noapaļo līdz diviem cipariem aiz komata un atgriež **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="118b4-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="118b4-120">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="118b4-120">Example 2</span></span>

<span data-ttu-id="118b4-121">`ROUND (1200.767, -3)` noapaļo līdz tuvākajam 1 000 reizinājumam un atgriež **1000**.</span><span class="sxs-lookup"><span data-stu-id="118b4-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="118b4-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="118b4-122">Additional resources</span></span>

[<span data-ttu-id="118b4-123">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="118b4-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
