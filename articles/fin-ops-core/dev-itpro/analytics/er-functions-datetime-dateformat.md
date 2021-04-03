---
title: DATEFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATEFORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0a9580b0ab9e472796375f498059ec0864a919ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563658"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="5bcd1-103">DATEFORMAT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="5bcd1-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5bcd1-104">`DATEFORMAT` funkcija atgriež *Virknes* vērtību, kas norādīto datuma vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="5bcd1-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="5bcd1-105">Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="5bcd1-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="5bcd1-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="5bcd1-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="5bcd1-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="5bcd1-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="5bcd1-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="5bcd1-108">Arguments</span></span>

<span data-ttu-id="5bcd1-109">`date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="5bcd1-109">`date`: *Date*</span></span>

<span data-ttu-id="5bcd1-110">Datuma/laika vērtība, kas apzīmē formatējamo datumu.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="5bcd1-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="5bcd1-111">`format`: *String*</span></span>

<span data-ttu-id="5bcd1-112">Izvades virknes formāts.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="5bcd1-113">Ja izmantojat standarta formātu vai pielāgotu formātu, formāta virkne ir reģistrjutīga.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="5bcd1-114">Piemēram, [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" formāta apzīmētājs atgriež datumu, izmantojot īsa datuma modeli, turpretī standarta "D" formāta apzīmētājs atgriež datumu, izmantojot garo datuma modeli.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="5bcd1-115">Turklāt [pielāgotais](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) formāta apzīmētājs atgriež mēnesi no 1 līdz 12, bet pielāgotais "m" formāta apzīmētājs atgriež minūti no 0 līdz 59.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="5bcd1-116">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="5bcd1-116">`culture`: *String*</span></span>

<span data-ttu-id="5bcd1-117">Kultūra, ko izmantot formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="5bcd1-118">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="5bcd1-118">Return values</span></span>

<span data-ttu-id="5bcd1-119">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="5bcd1-119">*String*</span></span>

<span data-ttu-id="5bcd1-120">Iegūtā virknes vērtībā.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5bcd1-121">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="5bcd1-121">Usage notes</span></span>

<span data-ttu-id="5bcd1-122">Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="5bcd1-123">Piemēram, ja `DATEFORMAT` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="5bcd1-124">Noklusējuma `culture` vērtība ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="5bcd1-125">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="5bcd1-125">Example 1</span></span>

<span data-ttu-id="5bcd1-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā virkni **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="5bcd1-127">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="5bcd1-127">Example 2</span></span>

<span data-ttu-id="5bcd1-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datumu, 2015. gada 24. decembri, kā virkni **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.</span><span class="sxs-lookup"><span data-stu-id="5bcd1-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bcd1-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5bcd1-129">Additional resources</span></span>

[<span data-ttu-id="5bcd1-130">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="5bcd1-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]