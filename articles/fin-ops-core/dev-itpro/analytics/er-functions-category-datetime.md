---
title: ER funkciju saraksts datuma un laika kategorijā
description: Šajā tēmā ir sniegta informācija par datuma un laika funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 2dd8524c9cd368f0fe64347e3212b419bb0902b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744565"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="f509a-103">ER funkciju saraksts datuma un laika kategorijā</span><span class="sxs-lookup"><span data-stu-id="f509a-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f509a-104">Elektroniskā pārskata (ER) datuma un laika funkcijas var izmantot, lai iegūtu informāciju no datuma un laika vērtībām un veiktu operācijas ar tām.</span><span class="sxs-lookup"><span data-stu-id="f509a-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="f509a-105">Šajā tēmā ir sniegts šo funkciju kopsavilkums.</span><span class="sxs-lookup"><span data-stu-id="f509a-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="f509a-106">Atbalstīto funkciju saraksts</span><span class="sxs-lookup"><span data-stu-id="f509a-106">List of supported functions</span></span>

| <span data-ttu-id="f509a-107">Funkcija</span><span class="sxs-lookup"><span data-stu-id="f509a-107">Function</span></span> | <span data-ttu-id="f509a-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="f509a-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="f509a-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="f509a-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="f509a-110">Šī funkcija atgriež *DateTime* vērtību, kas ir norādītais dienu skaits pirms vai pēc norādītā sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="f509a-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="f509a-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="f509a-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="f509a-112">Šī funkcija atgriež *Virknes* vērtību, kas norādīto datuma vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā kultūrā.</span><span class="sxs-lookup"><span data-stu-id="f509a-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="f509a-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f509a-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="f509a-114">Šī funkcija atgriež *Virknes* vērtību, kas norādīto datuma/laika vērtību uzrāda kā tekstu norādītajā formātā un pēc izvēles norādītajā kultūrā.</span><span class="sxs-lookup"><span data-stu-id="f509a-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="f509a-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="f509a-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="f509a-116">Šī funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā kultūrā datuma/laika vērtībai.</span><span class="sxs-lookup"><span data-stu-id="f509a-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="f509a-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="f509a-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="f509a-118">Šī funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no konkrētā datuma vērtības uz datuma/laika vērtību pēc universālā koordinētā laika (Griničas laika \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="f509a-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="f509a-119">DateValue:</span><span class="sxs-lookup"><span data-stu-id="f509a-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="f509a-120">Šī funkcija atgriež *Datuma* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā kultūrā datuma/laika vērtībai.</span><span class="sxs-lookup"><span data-stu-id="f509a-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="f509a-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="f509a-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="f509a-122">Šī funkcija atgriež *Vesela skaitļa* vērtību, kas reprezentē dienu skaitu no 1. janvāra līdz norādītajam datumam.</span><span class="sxs-lookup"><span data-stu-id="f509a-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="f509a-123">Dienas</span><span class="sxs-lookup"><span data-stu-id="f509a-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="f509a-124">Šī funkcija atgriež *Vesela skaitļa* vērtību, kas reprezentē dienu skaitu no viena norādītā datuma līdz otram norādītajam datumam.</span><span class="sxs-lookup"><span data-stu-id="f509a-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="f509a-125">Now</span><span class="sxs-lookup"><span data-stu-id="f509a-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="f509a-126">Šī funkcija atgriež *DateTime* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="f509a-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="f509a-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="f509a-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="f509a-128">Šī funkcija atgriež *Datuma* vērtību, kas apzīmē **nulles** datumu (1900. gada 1. janvāris).</span><span class="sxs-lookup"><span data-stu-id="f509a-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="f509a-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="f509a-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="f509a-130">Šī funkcija atgriež *DateTime* vērtību, kas apzīmē **nulles** datuma/laika vērtību (1900. gada 1. janvāris) universālajā koordinētajā laikā.</span><span class="sxs-lookup"><span data-stu-id="f509a-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="f509a-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="f509a-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="f509a-132">Šī funkcija atgriež *DateTime* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="f509a-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="f509a-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="f509a-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="f509a-134">Šī funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu sesijas datumu.</span><span class="sxs-lookup"><span data-stu-id="f509a-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="f509a-135">Šodien</span><span class="sxs-lookup"><span data-stu-id="f509a-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="f509a-136">Šī funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu.</span><span class="sxs-lookup"><span data-stu-id="f509a-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="f509a-137">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f509a-137">Additional resources</span></span>

[<span data-ttu-id="f509a-138">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="f509a-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="f509a-139">Formulu veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="f509a-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="f509a-140">Elektronisko atskaišu veidošanas formulas valoda</span><span class="sxs-lookup"><span data-stu-id="f509a-140">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]