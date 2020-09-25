---
title: ROUNDUP ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUNDUP elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 83262a11f92a924e5e49461cf414fb07ab278541
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744507"
---
# <a name="roundup-er-function"></a><span data-ttu-id="7dc84-103">ROUNDUP ER funkcija</span><span class="sxs-lookup"><span data-stu-id="7dc84-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dc84-104">`ROUNDUP` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="7dc84-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc84-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="7dc84-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="7dc84-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="7dc84-106">Arguments</span></span>

<span data-ttu-id="7dc84-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="7dc84-107">`number`: *Real*</span></span>

<span data-ttu-id="7dc84-108">Skaitliska vērtība, kas ir jānoapaļo uz augšu.</span><span class="sxs-lookup"><span data-stu-id="7dc84-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="7dc84-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="7dc84-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="7dc84-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="7dc84-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="7dc84-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="7dc84-111">Return values</span></span>

<span data-ttu-id="7dc84-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="7dc84-112">*Real*</span></span>

<span data-ttu-id="7dc84-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="7dc84-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7dc84-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="7dc84-114">Usage notes</span></span>

<span data-ttu-id="7dc84-115">Šī funkcija darbojas līdzīgi funkcijai [ROUND](er-functions-mathematical-round.md), bet norādīto skaitli tā vienmēr noapaļo uz augšu (prom no nulles).</span><span class="sxs-lookup"><span data-stu-id="7dc84-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="7dc84-116">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="7dc84-116">Example 1</span></span>

<span data-ttu-id="7dc84-117">`ROUNDUP (1200.763, 2)` noapaļo uz augšu līdz diviem cipariem aiz komata un atgriež **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="7dc84-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7dc84-118">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="7dc84-118">Example 2</span></span>

<span data-ttu-id="7dc84-119">`ROUNDUP (1200.767, -3)` noapaļo uz augšu līdz tuvākajam 1 000 reizinājumam un atgriež **2000**.</span><span class="sxs-lookup"><span data-stu-id="7dc84-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7dc84-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7dc84-120">Additional resources</span></span>

[<span data-ttu-id="7dc84-121">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="7dc84-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
