---
title: NUMERALSTOTEXT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMERALSTOTEXT elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 459123a66dae7a3d87a22b042e1be6585959ac15
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915629"
---
# <span data-ttu-id="17eb1-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="17eb1-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17eb1-104">`NUMERALSTOTEXT` funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tas ir uzrakstīts (tas ir, konvertēts teksta virknēs) norādītajā valodā.</span><span class="sxs-lookup"><span data-stu-id="17eb1-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="17eb1-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="17eb1-105">Syntax</span></span>

```
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="17eb1-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="17eb1-106">Arguments</span></span>

<span data-ttu-id="17eb1-107">`number`: *Vesels skaitlis* vai *Reāls*</span><span class="sxs-lookup"><span data-stu-id="17eb1-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="17eb1-108">Skaitliska vērtība, kas norāda skaitli, kas ir jāizburto.</span><span class="sxs-lookup"><span data-stu-id="17eb1-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="17eb1-109">`language`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="17eb1-109">`language`: *String*</span></span>

<span data-ttu-id="17eb1-110">*Virknes* vērtība, kas apzīmē valodas kodu.</span><span class="sxs-lookup"><span data-stu-id="17eb1-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="17eb1-111">`currency`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="17eb1-111">`currency`: *String*</span></span>

<span data-ttu-id="17eb1-112">*Virknes* vērtība, kas apzīmē valūtas kodu.</span><span class="sxs-lookup"><span data-stu-id="17eb1-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="17eb1-113">`print currency name flag`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="17eb1-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="17eb1-114">*Būla* vērtība, kas norāda, vai uzrakstam ir jāpievieno valūtas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="17eb1-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="17eb1-115">`decimal points`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="17eb1-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="17eb1-116">*Vesela skaitļa* vērtība, kas norāda ciparu aiz komata skaitu, kuram vajadzētu būt uzrakstā.</span><span class="sxs-lookup"><span data-stu-id="17eb1-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="17eb1-117">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="17eb1-117">Return values</span></span>

<span data-ttu-id="17eb1-118">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="17eb1-118">*String*</span></span>

<span data-ttu-id="17eb1-119">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="17eb1-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17eb1-120">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="17eb1-120">Usage notes</span></span>

<span data-ttu-id="17eb1-121">Valodas kods nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="17eb1-121">The language code is optional.</span></span> <span data-ttu-id="17eb1-122">Ja tas ir definēts kā tukša virkne, tiek izmantots izpildes konteksta valodas kods.</span><span class="sxs-lookup"><span data-stu-id="17eb1-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="17eb1-123">Noklusējuma valodas kods ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="17eb1-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="17eb1-124">Valodas kods darbības kontekstam ir definēts tā elektroniskā pārskata (ER) vienumā  **Mape** vai **Fails**, formātā, kas tiek izpildīts.</span><span class="sxs-lookup"><span data-stu-id="17eb1-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="17eb1-125">Valūtas kods nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="17eb1-125">The currency code is optional.</span></span> <span data-ttu-id="17eb1-126">Ja tas ir definēts kā tukša virkne, tiek izmantota izpildes konteksta uzņēmuma valūta.</span><span class="sxs-lookup"><span data-stu-id="17eb1-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="17eb1-127">Argumenti `print currency name flag` un `decimal points` tiek analizēti tikai šādiem valodu kodiem:  **CS**, **ET**, **HU**, **LT**, **LV**, **PL** un **RU**.</span><span class="sxs-lookup"><span data-stu-id="17eb1-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="17eb1-128">Turklāt arguments `print currency name flag` tiek analizēts tikai tiem uzņēmumiem, kuru valsts vai reģiona konteksts atbalsta valūtu nosaukumu locījumus.</span><span class="sxs-lookup"><span data-stu-id="17eb1-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="17eb1-129">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="17eb1-129">Example 1</span></span>

<span data-ttu-id="17eb1-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)`atgriež **"One Thousand Two Hundred Thirty Four and 56"**.</span><span class="sxs-lookup"><span data-stu-id="17eb1-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="17eb1-131">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="17eb1-131">Example 2</span></span>

<span data-ttu-id="17eb1-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)`atgriež **"Sto dwadzieścia"**.</span><span class="sxs-lookup"><span data-stu-id="17eb1-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="17eb1-133">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="17eb1-133">Example 3</span></span>

<span data-ttu-id="17eb1-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)`atgriež **"Сто двадцать евро 21 евроцент"**.</span><span class="sxs-lookup"><span data-stu-id="17eb1-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17eb1-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="17eb1-135">Additional resources</span></span>

[<span data-ttu-id="17eb1-136">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="17eb1-136">Text functions</span></span>](er-functions-category-text.md)
