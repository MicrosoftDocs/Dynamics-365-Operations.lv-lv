---
title: DATEFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATEFORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 4e9347937d088f15b4f489f0b85704a8688f8131
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743307"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="088b4-103">DATEFORMAT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="088b4-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="088b4-104">`DATEFORMAT` funkcija atgriež *Virknes* vērtību, kas norādīto datuma vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="088b4-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="088b4-105">Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="088b4-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="088b4-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="088b4-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="088b4-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="088b4-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="088b4-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="088b4-108">Arguments</span></span>

<span data-ttu-id="088b4-109">`date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="088b4-109">`date`: *Date*</span></span>

<span data-ttu-id="088b4-110">Datuma/laika vērtība, kas apzīmē formatējamo datumu.</span><span class="sxs-lookup"><span data-stu-id="088b4-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="088b4-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="088b4-111">`format`: *String*</span></span>

<span data-ttu-id="088b4-112">Izvades virknes formāts.</span><span class="sxs-lookup"><span data-stu-id="088b4-112">The format of the output string.</span></span>

<span data-ttu-id="088b4-113">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="088b4-113">`culture`: *String*</span></span>

<span data-ttu-id="088b4-114">Kultūra, ko izmantot formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="088b4-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="088b4-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="088b4-115">Return values</span></span>

<span data-ttu-id="088b4-116">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="088b4-116">*String*</span></span>

<span data-ttu-id="088b4-117">Iegūtā virknes vērtībā.</span><span class="sxs-lookup"><span data-stu-id="088b4-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="088b4-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="088b4-118">Usage notes</span></span>

<span data-ttu-id="088b4-119">Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts.</span><span class="sxs-lookup"><span data-stu-id="088b4-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="088b4-120">Piemēram, ja `DATEFORMAT` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru.</span><span class="sxs-lookup"><span data-stu-id="088b4-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="088b4-121">Noklusējuma `culture` vērtība ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="088b4-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="088b4-122">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="088b4-122">Example 1</span></span>

<span data-ttu-id="088b4-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā virkni **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.</span><span class="sxs-lookup"><span data-stu-id="088b4-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="088b4-124">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="088b4-124">Example 2</span></span>

<span data-ttu-id="088b4-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datumu, 2015. gada 24. decembri, kā virkni  **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.</span><span class="sxs-lookup"><span data-stu-id="088b4-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="088b4-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="088b4-126">Additional resources</span></span>

[<span data-ttu-id="088b4-127">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="088b4-127">Date and time functions</span></span>](er-functions-category-datetime.md)
