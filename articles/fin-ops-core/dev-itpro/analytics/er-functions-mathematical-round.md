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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041611"
---
# <span data-ttu-id="48f04-103"><a name="ROUND">ROUND ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="48f04-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48f04-104">`ROUND` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="48f04-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f04-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="48f04-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="48f04-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="48f04-106">Arguments</span></span>

<span data-ttu-id="48f04-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="48f04-107">`number`: *Real*</span></span>

<span data-ttu-id="48f04-108">Skaitliska vērtība, kas ir jānoapaļo.</span><span class="sxs-lookup"><span data-stu-id="48f04-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="48f04-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="48f04-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="48f04-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="48f04-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="48f04-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="48f04-111">Return values</span></span>

<span data-ttu-id="48f04-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="48f04-112">*Real*</span></span>

<span data-ttu-id="48f04-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="48f04-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="48f04-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="48f04-114">Usage notes</span></span>

<span data-ttu-id="48f04-115">Ja argumenta `decimals` vērtība ir lielāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz attiecīgajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="48f04-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="48f04-116">Ja argumenta `decimals` vērtība ir **0** (nulle), norādītais skaitlis tiek noapaļots līdz tuvākajam veselajam skaitlim.</span><span class="sxs-lookup"><span data-stu-id="48f04-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="48f04-117">Ja argumenta  `decimals` vērtība ir mazāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz skaitlim, kas atrodas pa kreisi no komata.</span><span class="sxs-lookup"><span data-stu-id="48f04-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="48f04-118">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="48f04-118">Example 1</span></span>

<span data-ttu-id="48f04-119">`ROUND (1200.767, 2)` noapaļo līdz diviem cipariem aiz komata un atgriež **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="48f04-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="48f04-120">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="48f04-120">Example 2</span></span>

<span data-ttu-id="48f04-121">`ROUND (1200.767, -3)` noapaļo līdz tuvākajam 1 000 reizinājumam un atgriež **1000**.</span><span class="sxs-lookup"><span data-stu-id="48f04-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48f04-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="48f04-122">Additional resources</span></span>

[<span data-ttu-id="48f04-123">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="48f04-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
