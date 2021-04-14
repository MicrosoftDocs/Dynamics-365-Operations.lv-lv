---
title: ROUND ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUND elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: ce0f50cd5e544455626862e44b774dba39cf6e57
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744491"
---
# <a name="round-er-function"></a><span data-ttu-id="f2c18-103">ROUND ER funkcija</span><span class="sxs-lookup"><span data-stu-id="f2c18-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2c18-104">`ROUND` funkcija atgriež norādīto numuru kā *Reālu* vērtību pēc tam, kad tas ir noapaļots līdz norādītajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="f2c18-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c18-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="f2c18-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="f2c18-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="f2c18-106">Arguments</span></span>

<span data-ttu-id="f2c18-107">`number`: *Reāls*</span><span class="sxs-lookup"><span data-stu-id="f2c18-107">`number`: *Real*</span></span>

<span data-ttu-id="f2c18-108">Skaitliska vērtība, kas ir jānoapaļo.</span><span class="sxs-lookup"><span data-stu-id="f2c18-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="f2c18-109">`decimals`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="f2c18-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="f2c18-110">Skaitliska vērtība, kas apzīmē ciparu aiz komata skaitu.</span><span class="sxs-lookup"><span data-stu-id="f2c18-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="f2c18-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="f2c18-111">Return values</span></span>

<span data-ttu-id="f2c18-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="f2c18-112">*Real*</span></span>

<span data-ttu-id="f2c18-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="f2c18-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f2c18-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="f2c18-114">Usage notes</span></span>

<span data-ttu-id="f2c18-115">Ja argumenta `decimals` vērtība ir lielāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz attiecīgajam ciparu skaitam aiz komata.</span><span class="sxs-lookup"><span data-stu-id="f2c18-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="f2c18-116">Ja argumenta `decimals` vērtība ir **0** (nulle), norādītais skaitlis tiek noapaļots līdz tuvākajam veselajam pāra skaitlim.</span><span class="sxs-lookup"><span data-stu-id="f2c18-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="f2c18-117">Ja argumenta `decimals` vērtība ir mazāka par 0 (nulli), norādītais skaitlis tiek noapaļots līdz skaitlim, kas atrodas pa kreisi no komata.</span><span class="sxs-lookup"><span data-stu-id="f2c18-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="f2c18-118">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="f2c18-118">Example 1</span></span>

<span data-ttu-id="f2c18-119">`ROUND (1200.767, 2)` noapaļo līdz diviem cipariem aiz komata un atgriež **1200.77**.</span><span class="sxs-lookup"><span data-stu-id="f2c18-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f2c18-120">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="f2c18-120">Example 2</span></span>

<span data-ttu-id="f2c18-121">`ROUND (1200.767, -3)` noapaļo līdz tuvākajam 1 000 reizinājumam un atgriež **1000**.</span><span class="sxs-lookup"><span data-stu-id="f2c18-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="f2c18-122">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="f2c18-122">Example 3</span></span>

<span data-ttu-id="f2c18-123">`ROUND (1200.5, 0)` noapaļo līdz tuvākajam veselajam pāra skaitlim un atgriež **1200**, bet `ROUND (1201.5, 0)` dara to pašu un atgriež **1202**.</span><span class="sxs-lookup"><span data-stu-id="f2c18-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2c18-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f2c18-124">Additional resources</span></span>

[<span data-ttu-id="f2c18-125">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="f2c18-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]