---
title: NUMERALSTOTEXT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMERALSTOTEXT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: e26890a0d99e0df631a3b3350d284e63aaed8e09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746151"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="d8625-103">NUMERALSTOTEXT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="d8625-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8625-104">`NUMERALSTOTEXT` funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tas ir uzrakstīts (tas ir, konvertēts teksta virknēs) norādītajā valodā.</span><span class="sxs-lookup"><span data-stu-id="d8625-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8625-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="d8625-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="d8625-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d8625-106">Arguments</span></span>

<span data-ttu-id="d8625-107">`number`: *Vesels skaitlis* vai *Reāls*</span><span class="sxs-lookup"><span data-stu-id="d8625-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="d8625-108">Skaitliska vērtība, kas norāda skaitli, kas ir jāizburto.</span><span class="sxs-lookup"><span data-stu-id="d8625-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="d8625-109">`language`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d8625-109">`language`: *String*</span></span>

<span data-ttu-id="d8625-110">*Virknes* vērtība, kas apzīmē valodas kodu.</span><span class="sxs-lookup"><span data-stu-id="d8625-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="d8625-111">`currency`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d8625-111">`currency`: *String*</span></span>

<span data-ttu-id="d8625-112">*Virknes* vērtība, kas apzīmē valūtas kodu.</span><span class="sxs-lookup"><span data-stu-id="d8625-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="d8625-113">`print currency name flag`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="d8625-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="d8625-114">*Būla* vērtība, kas norāda, vai uzrakstam ir jāpievieno valūtas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="d8625-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="d8625-115">`decimal points`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="d8625-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="d8625-116">*Vesela skaitļa* vērtība, kas norāda ciparu aiz komata skaitu, kuram vajadzētu būt uzrakstā.</span><span class="sxs-lookup"><span data-stu-id="d8625-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="d8625-117">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d8625-117">Return values</span></span>

<span data-ttu-id="d8625-118">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="d8625-118">*String*</span></span>

<span data-ttu-id="d8625-119">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="d8625-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d8625-120">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="d8625-120">Usage notes</span></span>

<span data-ttu-id="d8625-121">Valodas kods nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="d8625-121">The language code is optional.</span></span> <span data-ttu-id="d8625-122">Ja tas ir definēts kā tukša virkne, tiek izmantots izpildes konteksta valodas kods.</span><span class="sxs-lookup"><span data-stu-id="d8625-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="d8625-123">Noklusējuma valodas kods ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="d8625-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="d8625-124">Valodas kods darbības kontekstam ir definēts tā elektroniskā pārskata (ER) vienumā **Mape** vai **Fails**, formātā, kas tiek izpildīts.</span><span class="sxs-lookup"><span data-stu-id="d8625-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="d8625-125">Valūtas kods nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="d8625-125">The currency code is optional.</span></span> <span data-ttu-id="d8625-126">Ja tas ir definēts kā tukša virkne, tiek izmantota izpildes konteksta uzņēmuma valūta.</span><span class="sxs-lookup"><span data-stu-id="d8625-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="d8625-127">Argumenti `print currency name flag` un `decimal points` tiek analizēti tikai šādiem valodu kodiem: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** un **RU**.</span><span class="sxs-lookup"><span data-stu-id="d8625-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="d8625-128">Turklāt arguments `print currency name flag` tiek analizēts tikai tiem uzņēmumiem, kuru valsts vai reģiona konteksts atbalsta valūtu nosaukumu locījumus.</span><span class="sxs-lookup"><span data-stu-id="d8625-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="d8625-129">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="d8625-129">Example 1</span></span>

<span data-ttu-id="d8625-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` atgriež **"One Thousand Two Hundred Thirty Four and 56"**.</span><span class="sxs-lookup"><span data-stu-id="d8625-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d8625-131">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="d8625-131">Example 2</span></span>

<span data-ttu-id="d8625-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` atgriež **"Sto dwadzieścia"**.</span><span class="sxs-lookup"><span data-stu-id="d8625-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="d8625-133">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="d8625-133">Example 3</span></span>

<span data-ttu-id="d8625-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` atgriež **"Сто двадцать евро 21 евроцент"**.</span><span class="sxs-lookup"><span data-stu-id="d8625-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8625-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d8625-135">Additional resources</span></span>

[<span data-ttu-id="d8625-136">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="d8625-136">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]