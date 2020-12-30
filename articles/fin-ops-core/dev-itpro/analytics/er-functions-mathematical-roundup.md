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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ed86e2a848248dd8f2fc99401d12e0a162bf20a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686838"
---
# <a name="roundup-er-function"></a><span data-ttu-id="7cc0d-103">ROUNDUP ER funkcija</span><span class="sxs-lookup"><span data-stu-id="7cc0d-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cc0d-104">`ROUNDUP` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="7cc0d-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cc0d-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="7cc0d-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="7cc0d-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="7cc0d-106">Arguments</span></span>

<span data-ttu-id="7cc0d-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="7cc0d-107">`number`: *Real*</span></span>

<span data-ttu-id="7cc0d-108">Skaitliska vērtība, kas ir jānoapaļo uz augšu.</span><span class="sxs-lookup"><span data-stu-id="7cc0d-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="7cc0d-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="7cc0d-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="7cc0d-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="7cc0d-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="7cc0d-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="7cc0d-111">Return values</span></span>

<span data-ttu-id="7cc0d-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="7cc0d-112">*Real*</span></span>

<span data-ttu-id="7cc0d-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="7cc0d-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7cc0d-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="7cc0d-114">Usage notes</span></span>

<span data-ttu-id="7cc0d-115">Šī funkcija darbojas līdzīgi funkcijai [ROUND](er-functions-mathematical-round.md), bet norādīto skaitli tā vienmēr noapaļo uz augšu (prom no nulles).</span><span class="sxs-lookup"><span data-stu-id="7cc0d-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="7cc0d-116">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="7cc0d-116">Example 1</span></span>

<span data-ttu-id="7cc0d-117">`ROUNDUP (1200.763, 2)` noapaļo uz augšu līdz diviem cipariem aiz komata un atgriež **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="7cc0d-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="7cc0d-118">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="7cc0d-118">Example 2</span></span>

<span data-ttu-id="7cc0d-119">`ROUNDUP (1200.767, -3)` noapaļo uz augšu līdz tuvākajam 1 000 reizinājumam un atgriež **2000**.</span><span class="sxs-lookup"><span data-stu-id="7cc0d-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7cc0d-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7cc0d-120">Additional resources</span></span>

[<span data-ttu-id="7cc0d-121">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="7cc0d-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
