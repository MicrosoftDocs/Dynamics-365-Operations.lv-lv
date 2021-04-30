---
title: ROuNDAMOUNT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ROUNDAMOUNT elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: 7dfc7817eab68e9dd70ce84e68f26d14fd8cf1df
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891213"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="adb4c-103">ROuNDAMOUNT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="adb4c-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adb4c-104">`ROUNDAMOUNT` funkcija atgriež *Reālu* vērtību, kas apzīmē rezultātu norādītās summas noapaļošanai uz tuvāko cita skaitļa reizinātāju saskaņā ar norādīto noapaļošanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="adb4c-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb4c-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="adb4c-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="adb4c-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="adb4c-106">Arguments</span></span>

<span data-ttu-id="adb4c-107">`number`: *Int* vai *Real*</span><span class="sxs-lookup"><span data-stu-id="adb4c-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="adb4c-108">Skaitliska vērtība, kas ir jānoapaļo.</span><span class="sxs-lookup"><span data-stu-id="adb4c-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="adb4c-109">`decimals`: *Int* vai *Real*</span><span class="sxs-lookup"><span data-stu-id="adb4c-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="adb4c-110">Skaitlis, līdz kura daudzkārtnim ir jānoapaļo `number` parametra vērtība.</span><span class="sxs-lookup"><span data-stu-id="adb4c-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="adb4c-111">`round rule`: *Uzskaitījuma vērtība*</span><span class="sxs-lookup"><span data-stu-id="adb4c-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="adb4c-112">Uzskaitījuma vērtība **RoundOffType** uzskaitījumam, kas definē noapaļošanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="adb4c-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="adb4c-113">Šis uzskaitījums piedāvā šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adb4c-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="adb4c-114">Parasts (parastais)</span><span class="sxs-lookup"><span data-stu-id="adb4c-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="adb4c-115">Uz leju (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="adb4c-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="adb4c-116">Noapaļot uz augšu (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="adb4c-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="adb4c-117">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="adb4c-117">Return values</span></span>

<span data-ttu-id="adb4c-118">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="adb4c-118">*Real*</span></span>

<span data-ttu-id="adb4c-119">Iegūtā skaitliskā vērtība ir reizinātājs vērtībai, ko norāda parametrs `decimals` un kas ir vistuvāk `number` parametra norādītajai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="adb4c-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="adb4c-120">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="adb4c-120">Usage notes</span></span>

<span data-ttu-id="adb4c-121">Ja `number` parametrs ir nulle, šī funkcija vienmēr atgriež nulli.</span><span class="sxs-lookup"><span data-stu-id="adb4c-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="adb4c-122">Ja `decimals` parametrs ir nulle, šī funkcija noapaļo uz noklusējuma noapaļoto vērtību.</span><span class="sxs-lookup"><span data-stu-id="adb4c-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="adb4c-123">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, noklusējuma noapaļotā vērtība ir **0,01.**</span><span class="sxs-lookup"><span data-stu-id="adb4c-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="adb4c-124">Pretējā gadījumā noklusējuma noapaļotā vērtība ir **1,0.**</span><span class="sxs-lookup"><span data-stu-id="adb4c-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="adb4c-125">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, šī funkcija noapaļo līdz tuvākajai noapaļošanās summai.</span><span class="sxs-lookup"><span data-stu-id="adb4c-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="adb4c-126">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.RoundDown**, šī funkcija noapaļo nulles virzienā līdz tuvākajai noapaļošanās summai.</span><span class="sxs-lookup"><span data-stu-id="adb4c-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="adb4c-127">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.RoundUp**, šī funkcija noapaļo prom no nulles līdz tuvākajai noapaļošanās summai.</span><span class="sxs-lookup"><span data-stu-id="adb4c-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="adb4c-128">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, šī funkcija darbojas līdzīgi kā [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel funkcija un [ROUND](../dev-ref/xpp-math-run-time-functions.md#round) X++ funkcija.</span><span class="sxs-lookup"><span data-stu-id="adb4c-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](../dev-ref/xpp-math-run-time-functions.md#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="adb4c-129">Piezīmes</span><span class="sxs-lookup"><span data-stu-id="adb4c-129">Remarks</span></span>

<span data-ttu-id="adb4c-130">Lai skaitlisko vērtību noapaļotu līdz noteiktam decimāldaļu skaitam, izmantojiet funkciju [ROUND](er-functions-mathematical-round.md)</span><span class="sxs-lookup"><span data-stu-id="adb4c-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="adb4c-131">Paraugs</span><span class="sxs-lookup"><span data-stu-id="adb4c-131">Example</span></span>

<span data-ttu-id="adb4c-132">Ja **model.RoundOff** parametrs ir iestatīts uz **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` atgriež 7,35.</span><span class="sxs-lookup"><span data-stu-id="adb4c-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="adb4c-133">Ja **model.RoundOff** parametrs ir iestatīts uz **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` atgriež 7,35.</span><span class="sxs-lookup"><span data-stu-id="adb4c-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="adb4c-134">Ja **model.RoundOff** parametrs ir iestatīts uz **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` atgriež 8,4.</span><span class="sxs-lookup"><span data-stu-id="adb4c-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adb4c-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="adb4c-135">Additional resources</span></span>

[<span data-ttu-id="adb4c-136">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="adb4c-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="adb4c-137">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="adb4c-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]