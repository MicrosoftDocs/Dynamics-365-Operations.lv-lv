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
ms.openlocfilehash: cce35a33ca179ad85bbde879122d3afbeefe5ee7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745667"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="ffcf2-103">ROuNDAMOUNT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="ffcf2-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffcf2-104">`ROUNDAMOUNT` funkcija atgriež *Reālu* vērtību, kas apzīmē rezultātu norādītās summas noapaļošanai uz tuvāko cita skaitļa reizinātāju saskaņā ar norādīto noapaļošanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffcf2-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="ffcf2-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="ffcf2-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="ffcf2-106">Arguments</span></span>

<span data-ttu-id="ffcf2-107">`number`: *Int* vai *Real*</span><span class="sxs-lookup"><span data-stu-id="ffcf2-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="ffcf2-108">Skaitliska vērtība, kas ir jānoapaļo.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="ffcf2-109">`decimals`: *Int* vai *Real*</span><span class="sxs-lookup"><span data-stu-id="ffcf2-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="ffcf2-110">Skaitlis, līdz kura daudzkārtnim ir jānoapaļo `number` parametra vērtība.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="ffcf2-111">`round rule`: *Uzskaitījuma vērtība*</span><span class="sxs-lookup"><span data-stu-id="ffcf2-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="ffcf2-112">Uzskaitījuma vērtība **RoundOffType** uzskaitījumam, kas definē noapaļošanas kārtulu.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="ffcf2-113">Šis uzskaitījums piedāvā šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="ffcf2-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="ffcf2-114">Parasts (parastais)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="ffcf2-115">Uz leju (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="ffcf2-116">Noapaļot uz augšu (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="ffcf2-117">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="ffcf2-117">Return values</span></span>

<span data-ttu-id="ffcf2-118">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="ffcf2-118">*Real*</span></span>

<span data-ttu-id="ffcf2-119">Iegūtā skaitliskā vērtība ir reizinātājs vērtībai, ko norāda parametrs `decimals` un kas ir vistuvāk `number` parametra norādītajai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ffcf2-120">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="ffcf2-120">Usage notes</span></span>

<span data-ttu-id="ffcf2-121">Ja `number` parametrs ir nulle, šī funkcija vienmēr atgriež nulli.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="ffcf2-122">Ja `decimals` parametrs ir nulle, šī funkcija noapaļo uz noklusējuma noapaļoto vērtību.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="ffcf2-123">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, noklusējuma noapaļotā vērtība ir **0,01.**</span><span class="sxs-lookup"><span data-stu-id="ffcf2-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="ffcf2-124">Pretējā gadījumā noklusējuma noapaļotā vērtība ir **1,0.**</span><span class="sxs-lookup"><span data-stu-id="ffcf2-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="ffcf2-125">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, šī funkcija noapaļo līdz tuvākajai noapaļošanās summai.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="ffcf2-126">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.RoundDown**, šī funkcija noapaļo nulles virzienā līdz tuvākajai noapaļošanās summai.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="ffcf2-127">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.RoundUp**, šī funkcija noapaļo prom no nulles līdz tuvākajai noapaļošanās summai.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="ffcf2-128">Ja `round rule` parametrs ir iestatīts uz **RoundOffType.Ordinary**, šī funkcija darbojas līdzīgi kā [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel funkcija un [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ funkcija.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffcf2-129">Piezīmes</span><span class="sxs-lookup"><span data-stu-id="ffcf2-129">Remarks</span></span>

<span data-ttu-id="ffcf2-130">Lai skaitlisko vērtību noapaļotu līdz noteiktam decimāldaļu skaitam, izmantojiet funkciju [ROUND](er-functions-mathematical-round.md)</span><span class="sxs-lookup"><span data-stu-id="ffcf2-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="ffcf2-131">Paraugs</span><span class="sxs-lookup"><span data-stu-id="ffcf2-131">Example</span></span>

<span data-ttu-id="ffcf2-132">Ja **model.RoundOff** parametrs ir iestatīts uz **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` atgriež 7,35.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="ffcf2-133">Ja **model.RoundOff** parametrs ir iestatīts uz **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` atgriež 7,35.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="ffcf2-134">Ja **model.RoundOff** parametrs ir iestatīts uz **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` atgriež 8,4.</span><span class="sxs-lookup"><span data-stu-id="ffcf2-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffcf2-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ffcf2-135">Additional resources</span></span>

[<span data-ttu-id="ffcf2-136">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="ffcf2-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="ffcf2-137">Matemātiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="ffcf2-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]