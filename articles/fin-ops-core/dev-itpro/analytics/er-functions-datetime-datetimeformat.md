---
title: DATETIMEFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATETIMEFORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 90bd2900434b1be509f72ec82375e52ea32bc424
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/04/2021
ms.locfileid: "4825377"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="e0254-103">DATETIMEFORMAT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e0254-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0254-104">`DATETIMEFORMAT` funkcija atgriež *Virknes vērtību*, kas norādīto datuma/laika vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="e0254-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="e0254-105">Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="e0254-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="e0254-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="e0254-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="e0254-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="e0254-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="e0254-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="e0254-108">Arguments</span></span>

<span data-ttu-id="e0254-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="e0254-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="e0254-110">Datuma/laika vērtība, kas apzīmē formatējamo datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="e0254-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="e0254-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="e0254-111">`format`: *String*</span></span>

<span data-ttu-id="e0254-112">Izvades virknes formāts.</span><span class="sxs-lookup"><span data-stu-id="e0254-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="e0254-113">Ja izmantojat standarta formātu vai pielāgotu formātu, formāta virkne ir reģistrjutīga.</span><span class="sxs-lookup"><span data-stu-id="e0254-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="e0254-114">Piemēram, [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" formāta apzīmētājs atgriež datumu, izmantojot īsa datuma modeli, turpretī standarta "D" formāta apzīmētājs atgriež datumu, izmantojot garo datuma modeli.</span><span class="sxs-lookup"><span data-stu-id="e0254-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="e0254-115">Turklāt [pielāgotais](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) formāta apzīmētājs atgriež mēnesi no 1 līdz 12, bet pielāgotais "m" formāta apzīmētājs atgriež minūti no 0 līdz 59.</span><span class="sxs-lookup"><span data-stu-id="e0254-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="e0254-116">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="e0254-116">`culture`: *String*</span></span>

<span data-ttu-id="e0254-117">Kultūra, ko izmantot formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="e0254-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="e0254-118">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="e0254-118">Return values</span></span>

<span data-ttu-id="e0254-119">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e0254-119">*String*</span></span>

<span data-ttu-id="e0254-120">Iegūtā virknes vērtībā.</span><span class="sxs-lookup"><span data-stu-id="e0254-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e0254-121">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="e0254-121">Usage notes</span></span>

<span data-ttu-id="e0254-122">Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts.</span><span class="sxs-lookup"><span data-stu-id="e0254-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="e0254-123">Piemēram, ja `DATETIMEFORMAT` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru.</span><span class="sxs-lookup"><span data-stu-id="e0254-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="e0254-124">Noklusējuma `culture` vērtība ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="e0254-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="e0254-125">Kad `DATETIMEFORMAT` funkcija konvertē konkrētu datuma/laika vērtību, tā ņem vērā tā programmas lietotāja laika joslas iestatījumu lietotājs, kurš darbina ER formātu, kura kontekstā tikusi izsaukta funkcija.</span><span class="sxs-lookup"><span data-stu-id="e0254-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="e0254-126">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="e0254-126">Example 1</span></span>

<span data-ttu-id="e0254-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.</span><span class="sxs-lookup"><span data-stu-id="e0254-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="e0254-128">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="e0254-128">Example 2</span></span>

<span data-ttu-id="e0254-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` atgriež pašreizējās lietojumprogrammas sesijas datuma/laika vērtību, 2015. gada 24. decembri, kā **"24-12-2015"**, pamatojoties uz izvēlēto vācu kultūru un norādīto formātu.</span><span class="sxs-lookup"><span data-stu-id="e0254-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="e0254-130">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="e0254-130">Example 3</span></span>

<span data-ttu-id="e0254-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` atgriež virknes vērtību **2019-11-12T08:00:00.0000000-08:00**, kad tā tiek saukta procesa laikā, ko iniciēja lietojumprogrammas lietotājs, kuram ir laika joslas vērtība **(GMT-08:00) Klusā okeāna laiks (ASV & Kanāda)** sadaļā **Valodas un valsts/reģiona preferences**.</span><span class="sxs-lookup"><span data-stu-id="e0254-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0254-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e0254-132">Additional resources</span></span>

[<span data-ttu-id="e0254-133">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="e0254-133">Date and time functions</span></span>](er-functions-category-datetime.md)
