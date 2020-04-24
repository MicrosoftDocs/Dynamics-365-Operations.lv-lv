---
title: REPLACE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota REPLACE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 83d5095620a938f1ac4b8428fff9209fda7a7831
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201070"
---
# <a name=""></a><span data-ttu-id="31307-103"><a name="REPLACE">REPLACE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="31307-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31307-104">`REPLACE` funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, ja visa vai daļa no tās ir aizstāta ar citu virkni.</span><span class="sxs-lookup"><span data-stu-id="31307-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="31307-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="31307-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="31307-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="31307-106">Arguments</span></span>

<span data-ttu-id="31307-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="31307-107">`text`: *String*</span></span>

<span data-ttu-id="31307-108">*Virknes* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="31307-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="31307-109">`pattern`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="31307-109">`pattern`: *String*</span></span>

<span data-ttu-id="31307-110">Ja `regular expression flag` arguments ir **FALSE**, šis arguments satur tekstu, kas ir jāaizstāj.</span><span class="sxs-lookup"><span data-stu-id="31307-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="31307-111">Ja `regular expression flag` arguments ir **TRUE**, šis arguments ietver parastu izteiksmi, kas definē gan meklēšanas rakstu, gan aizstājējtekstu.</span><span class="sxs-lookup"><span data-stu-id="31307-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="31307-112">`replacement`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="31307-112">`replacement`: *String*</span></span>

<span data-ttu-id="31307-113">Ja `regular expression flag` arguments ir **FALSE**, šis arguments satur tekstu, kas ir jāizmanto kā aizstājējs.</span><span class="sxs-lookup"><span data-stu-id="31307-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="31307-114">Ja `regular expression flag` arguments ir **TRUE**, šis arguments netiek izmantots.</span><span class="sxs-lookup"><span data-stu-id="31307-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="31307-115">`regular expression flag`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="31307-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="31307-116">*Būla* vērtība, kas norāda, vai aizstāšanas laikā tiek izmantota parasta izteiksme.</span><span class="sxs-lookup"><span data-stu-id="31307-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="31307-117">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="31307-117">Return values</span></span>

<span data-ttu-id="31307-118">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="31307-118">*String*</span></span>

<span data-ttu-id="31307-119">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="31307-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="31307-120">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="31307-120">Usage notes</span></span>

<span data-ttu-id="31307-121">Ja `regular expression flag`arguments ir **patiess**, šī funkcija atgriež norādīto virkni pēc tam, kad tā ir mainīta, lietojot `pattern` argumenta norādīto regulāro izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="31307-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="31307-122">Regulārā izteiksme tiek izmantota, lai atrastu rakstzīmes, kas ir jāaizstāj.</span><span class="sxs-lookup"><span data-stu-id="31307-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="31307-123">Ja `regular expression flag` arguments ir **APLAMS**, šī funkcija atgriež norādīto virkni pēc tam, kad rakstzīmju kopa, kas definēta `pattern` argumentā, ir aizstāta ar `replacement` argumenta rakstzīmēm.</span><span class="sxs-lookup"><span data-stu-id="31307-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="31307-124">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="31307-124">Example 1</span></span>

<span data-ttu-id="31307-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` lieto parastu izteiksmi, kas noņem visus simbolus, kuri nav skaitļi, un atgriež **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="31307-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="31307-126">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="31307-126">Example 2</span></span>

<span data-ttu-id="31307-127">`REPLACE ("abcdef", "cd", "GH", false)` aizstāj burtus **"cd"** ar virkni **"GH"**  un atgriež **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="31307-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31307-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="31307-128">Additional resources</span></span>

[<span data-ttu-id="31307-129">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="31307-129">Text functions</span></span>](er-functions-category-text.md)
