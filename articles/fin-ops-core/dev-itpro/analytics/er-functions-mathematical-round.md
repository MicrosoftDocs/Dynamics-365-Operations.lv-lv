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
ms.openlocfilehash: 12af71a024a76fca98fc2e876da9b59e5762cf07
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744555"
---
# <a name="round-er-function"></a><span data-ttu-id="7a0e8-103">ROUND ER funkcija</span><span class="sxs-lookup"><span data-stu-id="7a0e8-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a0e8-104">`ROUND` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a0e8-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="7a0e8-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="7a0e8-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="7a0e8-106">Arguments</span></span>

<span data-ttu-id="7a0e8-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="7a0e8-107">`number`: *Real*</span></span>

<span data-ttu-id="7a0e8-108">Skaitliska vērtība, kas ir jānoapaļo.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="7a0e8-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="7a0e8-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="7a0e8-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="7a0e8-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="7a0e8-111">Return values</span></span>

<span data-ttu-id="7a0e8-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="7a0e8-112">*Real*</span></span>

<span data-ttu-id="7a0e8-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7a0e8-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="7a0e8-114">Usage notes</span></span>

<span data-ttu-id="7a0e8-115">Ja argumenta `decimals` vērtība ir lielāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz attiecīgajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="7a0e8-116">Ja argumenta `decimals` vērtība ir **0** (nulle), norādītais skaitlis tiek noapaļots līdz tuvākajam veselajam skaitlim.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="7a0e8-117">Ja argumenta `decimals` vērtība ir mazāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz skaitlim, kas atrodas pa kreisi no komata.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="7a0e8-118">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="7a0e8-118">Example 1</span></span>

<span data-ttu-id="7a0e8-119">`ROUND (1200.767, 2)` noapaļo līdz diviem cipariem aiz komata un atgriež **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7a0e8-120">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="7a0e8-120">Example 2</span></span>

<span data-ttu-id="7a0e8-121">`ROUND (1200.767, -3)` noapaļo līdz tuvākajam 1 000 reizinājumam un atgriež **1000**.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a0e8-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7a0e8-122">Additional resources</span></span>

[<span data-ttu-id="7a0e8-123">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="7a0e8-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
