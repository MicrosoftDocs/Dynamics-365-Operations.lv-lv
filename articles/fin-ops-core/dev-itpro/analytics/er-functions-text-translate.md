---
title: TRANSLATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TRANSLATE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916710"
---
# <span data-ttu-id="8d2eb-103"><a name="TRANSLATE">TRANSLATE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="8d2eb-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d2eb-104">`TRANSLATE` funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, ja visa vai daļa no tās ir aizstāta ar citu virkni.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d2eb-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="8d2eb-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="8d2eb-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="8d2eb-106">Arguments</span></span>

<span data-ttu-id="8d2eb-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="8d2eb-107">`text`: *String*</span></span>

<span data-ttu-id="8d2eb-108">*Virknes* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="8d2eb-109">`pattern`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="8d2eb-109">`pattern`: *String*</span></span>

<span data-ttu-id="8d2eb-110">Teksts, kas ir jāaizstāj.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-110">The text that must be replaced.</span></span>

<span data-ttu-id="8d2eb-111">`replacement`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="8d2eb-111">`replacement`: *String*</span></span>

<span data-ttu-id="8d2eb-112">Teksts, ko izmantot kā aizvietotāju.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d2eb-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="8d2eb-113">Return values</span></span>

<span data-ttu-id="8d2eb-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="8d2eb-114">*String*</span></span>

<span data-ttu-id="8d2eb-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8d2eb-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="8d2eb-116">Example</span></span>

<span data-ttu-id="8d2eb-117">`TRANSLATE ("abcdef", "cd", "GH")` aizstāj burtus **"cd"** ar virkni **"GH"**  un atgriež **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="8d2eb-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d2eb-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8d2eb-118">Additional resources</span></span>

[<span data-ttu-id="8d2eb-119">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="8d2eb-119">Text functions</span></span>](er-functions-category-text.md)
