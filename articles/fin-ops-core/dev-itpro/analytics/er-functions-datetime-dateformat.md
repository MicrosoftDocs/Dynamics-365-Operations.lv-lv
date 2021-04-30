---
title: DATEFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATEFORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 1b3a0a2608328b233004034f7ab2ccfa833c17e3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890914"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="839da-103">DATEFORMAT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="839da-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="839da-104">`DATEFORMAT` funkcija atgriež *Virknes* vērtību, kas norādīto datuma vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā [kultūrā](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="839da-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="839da-105">Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](/dotnet/standard/base-types/standard-date-and-time-format-strings) un [pielāgots](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="839da-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="839da-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="839da-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="839da-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="839da-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="839da-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="839da-108">Arguments</span></span>

<span data-ttu-id="839da-109">`date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="839da-109">`date`: *Date*</span></span>

<span data-ttu-id="839da-110">Datuma/laika vērtība, kas apzīmē formatējamo datumu.</span><span class="sxs-lookup"><span data-stu-id="839da-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="839da-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="839da-111">`format`: *String*</span></span>

<span data-ttu-id="839da-112">Izvades virknes formāts.</span><span class="sxs-lookup"><span data-stu-id="839da-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="839da-113">Ja izmantojat standarta formātu vai pielāgotu formātu, formāta virkne ir reģistrjutīga.</span><span class="sxs-lookup"><span data-stu-id="839da-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="839da-114">Piemēram, [standarta](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" formāta apzīmētājs atgriež datumu, izmantojot īsa datuma modeli, turpretī standarta "D" formāta apzīmētājs atgriež datumu, izmantojot garo datuma modeli.</span><span class="sxs-lookup"><span data-stu-id="839da-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="839da-115">Turklāt [pielāgotais](/dotnet/standard/base-types/custom-date-and-time-format-strings) formāta apzīmētājs atgriež mēnesi no 1 līdz 12, bet pielāgotais "m" formāta apzīmētājs atgriež minūti no 0 līdz 59.</span><span class="sxs-lookup"><span data-stu-id="839da-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="839da-116">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="839da-116">`culture`: *String*</span></span>

<span data-ttu-id="839da-117">Kultūra, ko izmantot formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="839da-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="839da-118">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="839da-118">Return values</span></span>

<span data-ttu-id="839da-119">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="839da-119">*String*</span></span>

<span data-ttu-id="839da-120">Iegūtā virknes vērtībā.</span><span class="sxs-lookup"><span data-stu-id="839da-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="839da-121">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="839da-121">Usage notes</span></span>

<span data-ttu-id="839da-122">Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts.</span><span class="sxs-lookup"><span data-stu-id="839da-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="839da-123">Piemēram, ja `DATEFORMAT` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru.</span><span class="sxs-lookup"><span data-stu-id="839da-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="839da-124">Noklusējuma `culture` vērtība ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="839da-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="839da-125">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="839da-125">Example 1</span></span>

<span data-ttu-id="839da-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā virkni **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.</span><span class="sxs-lookup"><span data-stu-id="839da-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="839da-127">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="839da-127">Example 2</span></span>

<span data-ttu-id="839da-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datumu, 2015. gada 24. decembri, kā virkni **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.</span><span class="sxs-lookup"><span data-stu-id="839da-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="839da-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="839da-129">Additional resources</span></span>

[<span data-ttu-id="839da-130">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="839da-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]