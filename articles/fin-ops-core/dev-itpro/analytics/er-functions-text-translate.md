---
title: TRANSLATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TRANSLATE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 415444bda097c00522155d1b37988a79da836902
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201116"
---
# <a name=""></a><span data-ttu-id="7575b-103"><a name="TRANSLATE">TRANSLATE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="7575b-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7575b-104">`TRANSLATE` funkcija atgriež *Virknes* vērtību, kas satur noteiktā teksta rakstzīmju aizstāšanas rezultātu citas nodrošinātās kopas rakstzīmēs.</span><span class="sxs-lookup"><span data-stu-id="7575b-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="7575b-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="7575b-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="7575b-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="7575b-106">Arguments</span></span>

<span data-ttu-id="7575b-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="7575b-107">`text`: *String*</span></span>

<span data-ttu-id="7575b-108">*Virknes* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="7575b-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="7575b-109">`pattern`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="7575b-109">`pattern`: *String*</span></span>

<span data-ttu-id="7575b-110">Teksts, kas ir jāaizstāj.</span><span class="sxs-lookup"><span data-stu-id="7575b-110">The text that must be replaced.</span></span>

<span data-ttu-id="7575b-111">`replacement`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="7575b-111">`replacement`: *String*</span></span>

<span data-ttu-id="7575b-112">Teksts, ko izmantot kā aizvietotāju.</span><span class="sxs-lookup"><span data-stu-id="7575b-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="7575b-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="7575b-113">Return values</span></span>

<span data-ttu-id="7575b-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="7575b-114">*String*</span></span>

<span data-ttu-id="7575b-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="7575b-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7575b-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="7575b-116">Usage notes</span></span>

<span data-ttu-id="7575b-117">`TRANSLATE` funkcija aizstāj pa vienai rakstzīmei reizē.</span><span class="sxs-lookup"><span data-stu-id="7575b-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="7575b-118">Funkcija aizvieto pirmo `text` argumenta rakstzīmi ar `pattern` argumenta pirmo rakstzīmi un pēc tam otro rakstzīmi un seko tai pašai plūsmai līdz beigām.</span><span class="sxs-lookup"><span data-stu-id="7575b-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="7575b-119">Kad rakstzīme no `text` un `pattern` argumentiem atbilst, tā tiek aizstāta ar rakstzīmi no `replacement` argumenta, kas atrodas tādā pašā pozīcijā kā rakstzīme no `pattern` argumenta.</span><span class="sxs-lookup"><span data-stu-id="7575b-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="7575b-120">Ja rakstzīme tiek parādīta vairākas reizes `pattern` argumentā, tiek izmantota `replacement` argumenta kartēšana, kas atbilst šīs rakstzīmes pirmajam parādīšanās gadījumam.</span><span class="sxs-lookup"><span data-stu-id="7575b-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="7575b-121">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="7575b-121">Example 1</span></span>

<span data-ttu-id="7575b-122">`TRANSLATE ("abcdef", "cd", "GH")` aizvieto norādītā **"abcdef"** teksta **"c"** rakstzīmi ar  `replacement` teksta **"G"** rakstzīmi sakarā ar:</span><span class="sxs-lookup"><span data-stu-id="7575b-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="7575b-123">Rakstzīme **"c"** tiek parādīta `pattern` teksta pirmajā pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="7575b-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="7575b-124">`replacement` teksta pirmajā pozīcijā ir ietverta rakstzīme **"G"**.</span><span class="sxs-lookup"><span data-stu-id="7575b-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="7575b-125">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="7575b-125">Example 2</span></span>

<span data-ttu-id="7575b-126">`TRANSLATE ("abcdef", "ccd", "GH")` atgriež **"abGdef"**.</span><span class="sxs-lookup"><span data-stu-id="7575b-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="7575b-127">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="7575b-127">Example 3</span></span>

<span data-ttu-id="7575b-128">`TRANSLATE ("abccba", "abc", "123")` atgriež **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="7575b-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7575b-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7575b-129">Additional resources</span></span>

[<span data-ttu-id="7575b-130">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="7575b-130">Text functions</span></span>](er-functions-category-text.md)
