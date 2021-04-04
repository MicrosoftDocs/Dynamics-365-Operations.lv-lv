---
title: ROUNDDOWN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUNDDOWN elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: f199d662eb31f184b6f978b3d251e64907254584
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567144"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="8ae34-103">ROUNDDOWN ER funkcija</span><span class="sxs-lookup"><span data-stu-id="8ae34-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ae34-104">`ROUNDDOWN` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots uz leju līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="8ae34-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae34-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="8ae34-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="8ae34-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="8ae34-106">Arguments</span></span>

<span data-ttu-id="8ae34-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="8ae34-107">`number`: *Real*</span></span>

<span data-ttu-id="8ae34-108">Skaitliska vērtība, kas ir jānoapaļo uz leju.</span><span class="sxs-lookup"><span data-stu-id="8ae34-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="8ae34-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="8ae34-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="8ae34-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="8ae34-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="8ae34-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="8ae34-111">Return values</span></span>

<span data-ttu-id="8ae34-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="8ae34-112">*Real*</span></span>

<span data-ttu-id="8ae34-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="8ae34-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8ae34-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="8ae34-114">Usage notes</span></span>

<span data-ttu-id="8ae34-115">Šī funkcija darbojas līdzīgi funkcijai [ROUND](er-functions-mathematical-round.md), bet norādīto skaitli tā vienmēr noapaļo uz leju (nulles virzienā).</span><span class="sxs-lookup"><span data-stu-id="8ae34-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="8ae34-116">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="8ae34-116">Example 1</span></span>

<span data-ttu-id="8ae34-117">`ROUNDDOWN (1200.767, 2)` noapaļo uz leju līdz diviem cipariem aiz komata un atgriež **1200.76**.</span><span class="sxs-lookup"><span data-stu-id="8ae34-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="8ae34-118">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="8ae34-118">Example 2</span></span>

<span data-ttu-id="8ae34-119">`ROUNDDOWN (1700.767, -3)` noapaļo uz leju līdz tuvākajam 1 000 reizinājumam un atgriež **1000**.</span><span class="sxs-lookup"><span data-stu-id="8ae34-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ae34-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8ae34-120">Additional resources</span></span>

[<span data-ttu-id="8ae34-121">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="8ae34-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]