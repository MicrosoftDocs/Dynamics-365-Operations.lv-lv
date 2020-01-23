---
title: ROUNDDOWN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUNDDOWN elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: ef7d81852a0bbb84fd8f37cd89555766cc47f5f8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915859"
---
# <span data-ttu-id="96a67-103"><a name="ROUNDDOWN">ROUNDDOWN ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="96a67-103"><a name="ROUNDDOWN">ROUNDDOWN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96a67-104">`ROUNDDOWN` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots uz leju līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="96a67-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a67-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="96a67-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="96a67-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="96a67-106">Arguments</span></span>

<span data-ttu-id="96a67-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="96a67-107">`number`: *Real*</span></span>

<span data-ttu-id="96a67-108">Skaitliska vērtība, kas ir jānoapaļo uz leju.</span><span class="sxs-lookup"><span data-stu-id="96a67-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="96a67-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="96a67-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="96a67-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="96a67-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="96a67-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="96a67-111">Return values</span></span>

<span data-ttu-id="96a67-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="96a67-112">*Real*</span></span>

<span data-ttu-id="96a67-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="96a67-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="96a67-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="96a67-114">Usage notes</span></span>

<span data-ttu-id="96a67-115">Šī funkcija darbojas līdzīgi funkcijai [ROUND](er-functions-mathematical-round.md), bet norādīto skaitli tā vienmēr noapaļo uz leju (nulles virzienā).</span><span class="sxs-lookup"><span data-stu-id="96a67-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="96a67-116">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="96a67-116">Example 1</span></span>

<span data-ttu-id="96a67-117">`ROUNDDOWN (1200.767, 2)` noapaļo uz leju līdz diviem cipariem aiz komata un atgriež **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="96a67-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="96a67-118">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="96a67-118">Example 2</span></span>

<span data-ttu-id="96a67-119">`ROUNDDOWN (1700.767, -3)` noapaļo uz leju līdz tuvākajam 1 000 reizinājumam un atgriež **1000**.</span><span class="sxs-lookup"><span data-stu-id="96a67-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96a67-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="96a67-120">Additional resources</span></span>

[<span data-ttu-id="96a67-121">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="96a67-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
