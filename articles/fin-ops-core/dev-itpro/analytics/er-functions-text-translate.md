---
title: TRANSLATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TRANSLATE elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 7e4d6417757e27190ab7cabf2bf01243bb87b55c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746077"
---
# <a name="translate-er-function"></a><span data-ttu-id="2a1b5-103">TRANSLATE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="2a1b5-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a1b5-104">`TRANSLATE` funkcija atgriež *Virknes* vērtību, kas satur noteiktā teksta rakstzīmju aizstāšanas rezultātu citas nodrošinātās kopas rakstzīmēs.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a1b5-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="2a1b5-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="2a1b5-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="2a1b5-106">Arguments</span></span>

<span data-ttu-id="2a1b5-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="2a1b5-107">`text`: *String*</span></span>

<span data-ttu-id="2a1b5-108">*Virknes* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="2a1b5-109">`pattern`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="2a1b5-109">`pattern`: *String*</span></span>

<span data-ttu-id="2a1b5-110">Teksts, kas ir jāaizstāj.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-110">The text that must be replaced.</span></span>

<span data-ttu-id="2a1b5-111">`replacement`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="2a1b5-111">`replacement`: *String*</span></span>

<span data-ttu-id="2a1b5-112">Teksts, ko izmantot kā aizvietotāju.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="2a1b5-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="2a1b5-113">Return values</span></span>

<span data-ttu-id="2a1b5-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="2a1b5-114">*String*</span></span>

<span data-ttu-id="2a1b5-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2a1b5-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="2a1b5-116">Usage notes</span></span>

<span data-ttu-id="2a1b5-117">`TRANSLATE` funkcija aizstāj pa vienai rakstzīmei reizē.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="2a1b5-118">Funkcija aizvieto pirmo `text` argumenta rakstzīmi ar `pattern` argumenta pirmo rakstzīmi un pēc tam otro rakstzīmi un seko tai pašai plūsmai līdz beigām.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="2a1b5-119">Kad rakstzīme no `text` un `pattern` argumentiem atbilst, tā tiek aizstāta ar rakstzīmi no `replacement` argumenta, kas atrodas tādā pašā pozīcijā kā rakstzīme no `pattern` argumenta.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="2a1b5-120">Ja rakstzīme tiek parādīta vairākas reizes `pattern` argumentā, tiek izmantota `replacement` argumenta kartēšana, kas atbilst šīs rakstzīmes pirmajam parādīšanās gadījumam.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="2a1b5-121">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="2a1b5-121">Example 1</span></span>

<span data-ttu-id="2a1b5-122">`TRANSLATE ("abcdef", "cd", "GH")` aizvieto norādītā  **"abcdef"** teksta **"c"** rakstzīmi ar `replacement` teksta **"G"** rakstzīmi sakarā ar:</span><span class="sxs-lookup"><span data-stu-id="2a1b5-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="2a1b5-123">Rakstzīme **"c"** tiek parādīta `pattern` teksta pirmajā pozīcijā.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="2a1b5-124">`replacement` teksta pirmajā pozīcijā ir ietverta rakstzīme **"G"**.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="2a1b5-125">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="2a1b5-125">Example 2</span></span>

<span data-ttu-id="2a1b5-126">`TRANSLATE ("abcdef", "ccd", "GH")` atgriež **"abGdef"**.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="2a1b5-127">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="2a1b5-127">Example 3</span></span>

<span data-ttu-id="2a1b5-128">`TRANSLATE ("abccba", "abc", "123")` atgriež **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="2a1b5-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a1b5-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2a1b5-129">Additional resources</span></span>

[<span data-ttu-id="2a1b5-130">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="2a1b5-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]