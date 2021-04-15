---
title: OR ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota OR elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 9763cdbabfbaba1af433c1fd753b03982ecb550d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751729"
---
# <a name="or-er-function"></a><span data-ttu-id="4703e-103">OR ER funkcija</span><span class="sxs-lookup"><span data-stu-id="4703e-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4703e-104">`OR` funkcija atgriež *Būla* vērtību **FALSE**, ja visi norādītie nosacījumi ir nepatiesi.</span><span class="sxs-lookup"><span data-stu-id="4703e-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="4703e-105">Šī funkcija atgriež *Būla* vērtību **TRUE**, ja jebkurš norādītais nosacījums ir patiess.</span><span class="sxs-lookup"><span data-stu-id="4703e-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4703e-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="4703e-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="4703e-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="4703e-107">Arguments</span></span>

<span data-ttu-id="4703e-108">`condition 1`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="4703e-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="4703e-109">Derīga nosacījuma izteiksme, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="4703e-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4703e-110">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="4703e-110">This argument is required.</span></span>

<span data-ttu-id="4703e-111">`condition N`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="4703e-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="4703e-112">Derīga nosacījuma izteiksme, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="4703e-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4703e-113">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="4703e-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4703e-114">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="4703e-114">Return values</span></span>

<span data-ttu-id="4703e-115">*Būla*</span><span class="sxs-lookup"><span data-stu-id="4703e-115">*Boolean*</span></span>

<span data-ttu-id="4703e-116">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="4703e-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="4703e-117">Paraugs</span><span class="sxs-lookup"><span data-stu-id="4703e-117">Example</span></span>

<span data-ttu-id="4703e-118">`OR (1=2, "a"="a")` atgriež **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="4703e-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4703e-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4703e-119">Additional resources</span></span>

[<span data-ttu-id="4703e-120">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="4703e-120">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]