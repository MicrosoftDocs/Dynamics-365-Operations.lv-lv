---
title: ER funkciju saraksts veida konvertēšanas kategorijā
description: Šajā tēmā ir sniegta informācija par konvertēšanas funkcijām, kas tiek atbalstītas elektronisko atskaišu veidošanā (ER).
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 5613496d3131ccd39b198cac214eb791a6d07355
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561522"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="4815b-103">ER funkciju saraksts veida konvertēšanas kategorijā</span><span class="sxs-lookup"><span data-stu-id="4815b-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4815b-104">Elektronisko atskaišu veidošanas (ER) veida konvertēšanas funkcijas var izmantot, lai konvertētu vērtības starp veidiem.</span><span class="sxs-lookup"><span data-stu-id="4815b-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="4815b-105">Šajā tēmā ir sniegts šo funkciju kopsavilkums.</span><span class="sxs-lookup"><span data-stu-id="4815b-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="4815b-106">Veida pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="4815b-106">Type conversion functions</span></span>

| <span data-ttu-id="4815b-107">Funkcija</span><span class="sxs-lookup"><span data-stu-id="4815b-107">Function</span></span> | <span data-ttu-id="4815b-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4815b-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4815b-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="4815b-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="4815b-110">Šī funkcija atgriež *Int64* vērtību, kas apzīmē norādīto virkni.</span><span class="sxs-lookup"><span data-stu-id="4815b-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="4815b-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="4815b-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="4815b-112">Šī funkcija atgriež *Int* vērtību, kas apzīmē norādīto virkni.</span><span class="sxs-lookup"><span data-stu-id="4815b-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="4815b-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="4815b-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="4815b-114">Šī funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās *Virknes* vērtības.</span><span class="sxs-lookup"><span data-stu-id="4815b-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="4815b-115">Konvertēšanas laikā tiek uzskatīti norādītie decimālo un ciparu grupēšanas atdalītāji.</span><span class="sxs-lookup"><span data-stu-id="4815b-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="4815b-116">Vērtība</span><span class="sxs-lookup"><span data-stu-id="4815b-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="4815b-117">Šī funkcija atgriež *Reālu* vērtību, kas tiek konvertēta no norādītās *Virknes* vērtības.</span><span class="sxs-lookup"><span data-stu-id="4815b-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="4815b-118">Veida konvertēšanas funkcijas konteinera kategorijā</span><span class="sxs-lookup"><span data-stu-id="4815b-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="4815b-119">Šajā tabulā aprakstītas veida konvertēšanas funkcijas [konteinera](er-functions-category-container.md) kategorijā.</span><span class="sxs-lookup"><span data-stu-id="4815b-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="4815b-120">Funkcija</span><span class="sxs-lookup"><span data-stu-id="4815b-120">Function</span></span> | <span data-ttu-id="4815b-121">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4815b-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4815b-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="4815b-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="4815b-123">Šī funkcija konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *Konteiners*.</span><span class="sxs-lookup"><span data-stu-id="4815b-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="4815b-124">Veida konvertēšanas funkcijas datuma un laika kategorijā</span><span class="sxs-lookup"><span data-stu-id="4815b-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="4815b-125">Šajā tabulā aprakstītas veida konvertēšanas funkcijas [datuma un laika kategorijā](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="4815b-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="4815b-126">Funkcija</span><span class="sxs-lookup"><span data-stu-id="4815b-126">Function</span></span> | <span data-ttu-id="4815b-127">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4815b-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4815b-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="4815b-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="4815b-129">Šī funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no dotās *Virknes* vērtības norādītajā formātā un pēc izvēles norādītajā kultūrā datuma/laika vērtībai.</span><span class="sxs-lookup"><span data-stu-id="4815b-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="4815b-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="4815b-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="4815b-131">Šī funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no konkrētā *Datuma* vērtības uz datuma/laika vērtību pēc universālā koordinētā laika (Griničas laika \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="4815b-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="4815b-132">DateValue:</span><span class="sxs-lookup"><span data-stu-id="4815b-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="4815b-133">Šī funkcija atgriež *Datuma* vērtību, kas tiek konvertēta no dotās *Virknes* vērtības norādītajā formātā un pēc izvēles norādītajā kultūrā datuma vērtībai.</span><span class="sxs-lookup"><span data-stu-id="4815b-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="4815b-134">Veida konvertēšanas funkcijas saraksta kategorijā</span><span class="sxs-lookup"><span data-stu-id="4815b-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="4815b-135">Šajā tabulā aprakstītas veida konvertēšanas funkcijas [saraksta kategorijā](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="4815b-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="4815b-136">Funkcija</span><span class="sxs-lookup"><span data-stu-id="4815b-136">Function</span></span> | <span data-ttu-id="4815b-137">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4815b-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4815b-138">Saraksts</span><span class="sxs-lookup"><span data-stu-id="4815b-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="4815b-139">Šī funkcija atgriež jaunu *Ierakstu saraksta* vērtību kā jaunu sarakstu, kas ir izveidots no norādītiem *Konteinera (ieraksta)* veida argumentiem.</span><span class="sxs-lookup"><span data-stu-id="4815b-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="4815b-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="4815b-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="4815b-141">Šī funkcija atgriež *Ierakstu saraksta* vērtību, kas tiek izveidota, pamatojoties uz norādītā *Uzskaitījuma* vai *Konteinera (ieraksta)* veida argumenta struktūru.</span><span class="sxs-lookup"><span data-stu-id="4815b-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="4815b-142">Sadalīt</span><span class="sxs-lookup"><span data-stu-id="4815b-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="4815b-143">Šī funkcija sadala norādīto ievades *Virknes* vērtību apakšvirknēs un atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību.</span><span class="sxs-lookup"><span data-stu-id="4815b-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="4815b-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="4815b-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="4815b-145">Šī funkcija atgriež *Virknes* vērtību, kas sastāv no norādītā *Ierakstu saraksta* vērtībā norādītā lauka savirknētajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="4815b-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="4815b-146">Vērtības var atdalīt ar norādīto norobežotāju.</span><span class="sxs-lookup"><span data-stu-id="4815b-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="4815b-147">Veida konvertēšanas funkcijas teksta kategorijā</span><span class="sxs-lookup"><span data-stu-id="4815b-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="4815b-148">Šajā tabulā aprakstītas veida konvertēšanas funkcijas [teksta kategorijā](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="4815b-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="4815b-149">Funkcija</span><span class="sxs-lookup"><span data-stu-id="4815b-149">Function</span></span> | <span data-ttu-id="4815b-150">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4815b-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4815b-151">Char</span><span class="sxs-lookup"><span data-stu-id="4815b-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="4815b-152">Šī funkcija atgriež *Virknes* vērtību, kas apzīmē vienu rakstzīmi, uz kuru atsaucas norādītais unikoda numurs.</span><span class="sxs-lookup"><span data-stu-id="4815b-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="4815b-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="4815b-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="4815b-154">Šī funkcija konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *GUID*.</span><span class="sxs-lookup"><span data-stu-id="4815b-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="4815b-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="4815b-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="4815b-156">Šī funkcija atgriež *Virknes* vērtību, kas apzīmē skaitu uzrāda norādītajā formātā un pēc izvēles norādītajā kultūrā.</span><span class="sxs-lookup"><span data-stu-id="4815b-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="4815b-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="4815b-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="4815b-158">Šī funkcija atgriež *Konteinera* vērtību, kas parāda ātrās atbildes kodu (QR koda) attēlu norādītajai virknei binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="4815b-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="4815b-159">Teksts</span><span class="sxs-lookup"><span data-stu-id="4815b-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="4815b-160">Šī funkcija atgriež *Virknes* vērtību, kas apzīmē norādīto skaitli pēc tam, kad tā ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās programmas instances servera lokalizācijas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="4815b-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="4815b-161">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4815b-161">Additional resources</span></span>

[<span data-ttu-id="4815b-162">Elektronisko pārskatu veidošanas apskats</span><span class="sxs-lookup"><span data-stu-id="4815b-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="4815b-163">Formulu veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="4815b-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4815b-164">Elektronisko atskaišu veidošanas formulas valoda</span><span class="sxs-lookup"><span data-stu-id="4815b-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]