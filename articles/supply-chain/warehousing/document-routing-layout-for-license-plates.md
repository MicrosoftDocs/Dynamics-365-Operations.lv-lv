---
title: Dokumenta maršrutēšanas izkārtojums numura zīmes etiķetēm
description: Šajā tēmā ir aprakstīts, kā lietot formatēšanas metodes etiķešu vērtību drukāšanai.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 8c96aef5d66ed8f8c44d74eee9b60f0a7d38a46d
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017717"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="9fee1-103">Dokumenta maršrutēšanas izkārtojums numura zīmes etiķetēm</span><span class="sxs-lookup"><span data-stu-id="9fee1-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fee1-104">Dokumenta maršrutēšanas izkārtojums nosaka numura zīmes etiķešu izskatu un uz tām izdrukātos datus.</span><span class="sxs-lookup"><span data-stu-id="9fee1-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="9fee1-105">Konfigurējiet drukāšanas trigera punktus, iestatot mobilās ierīces izvēlnes elementus un darba veidnes.</span><span class="sxs-lookup"><span data-stu-id="9fee1-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="9fee1-106">Tipiskā scenārijā noliktavas saņemšanas darbinieki drukā numura zīmju etiķetes uzreiz pēc tam, kad tie reģistrē paletes saturu, kas tiek saņemti saņemšanas zonā.</span><span class="sxs-lookup"><span data-stu-id="9fee1-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="9fee1-107">Fiziskās etiķetes tiek lietotas paletēm.</span><span class="sxs-lookup"><span data-stu-id="9fee1-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="9fee1-108">Tos var izmantot validācijai kā daļu no izvietošanas procesa, kas seko turpmākajām nosūtīšanas izdošanas operācijām.</span><span class="sxs-lookup"><span data-stu-id="9fee1-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="9fee1-109">Jūs varat drukāt augstas sarežģītības etiķetes, ar nosacījumu, ka drukas ierīce spēj interpretēt tai sūtīto tekstu.</span><span class="sxs-lookup"><span data-stu-id="9fee1-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="9fee1-110">Piemēram, Zebra programmēšanas valodas (ZPL) izkārtojums, kas ietver svītrkodu, var izskatīties līdzīgi šim piemēram.</span><span class="sxs-lookup"><span data-stu-id="9fee1-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="9fee1-111">Kā daļa no etiķešu drukāšanas procesa teksts `$LicensePlateId$` šajā piemērā tiks aizstāts ar datu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9fee1-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="9fee1-112">Lai apskatītu vērtības, kas tiks drukātas, dodieties uz **Noliktavas pārvaldība \> Vaicājumi un pārskati \> Numura zīmes etiķetes**.</span><span class="sxs-lookup"><span data-stu-id="9fee1-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="9fee1-113">Vairāki plaši pieejami etiķešu ģenerēšanas rīki var jums palīdzēt formatēt etiķetes izkārtojuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="9fee1-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="9fee1-114">Daudzi no šiem rīkiem atbalsta `$FieldName$` formātu.</span><span class="sxs-lookup"><span data-stu-id="9fee1-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="9fee1-115">Turklāt Microsoft Dynamics 365 Supply Chain Management izmanto īpašu formatēšanas loģiku kā daļu no lauka kartējuma dokumenta maršrutēšanas izkārtojumam.</span><span class="sxs-lookup"><span data-stu-id="9fee1-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="9fee1-116">Pielāgoti skaitļu formāti</span><span class="sxs-lookup"><span data-stu-id="9fee1-116">Custom number formats</span></span>

<span data-ttu-id="9fee1-117">Jūs varat pielāgot formatējumu skaitliskām lauka vērtībām, kas tiek drukātas, izmantojot kodus, kuriem ir šāds formāts.</span><span class="sxs-lookup"><span data-stu-id="9fee1-117">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="9fee1-118">Tālāk minēts šī formāta paskaidrojums:</span><span class="sxs-lookup"><span data-stu-id="9fee1-118">Here is an explanation of this format:</span></span>

- <span data-ttu-id="9fee1-119">`FieldName` ir datu lauka nosaukums (piemēram, **Daudzums** ).</span><span class="sxs-lookup"><span data-stu-id="9fee1-119">`FieldName` is the name of the data field (such as **Qty** ).</span></span>
- <span data-ttu-id="9fee1-120">`FormatString` nosaka, kā jādrukā dati.</span><span class="sxs-lookup"><span data-stu-id="9fee1-120">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="9fee1-121">Sekojošie piemēri parāda, kā varat pielāgot darba daudzuma ( **Daudzums** ) lauku:</span><span class="sxs-lookup"><span data-stu-id="9fee1-121">The following examples show how you can customize the work quantity ( **Qty** ) field:</span></span>

- <span data-ttu-id="9fee1-122">Lai vienmēr parādītu četrus ciparus (izmantojot nulles kā vietturus), lietojiet `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="9fee1-122">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="9fee1-123">Piemēram, ja daudzums ir 10, etiķetē tiks parādīts "0010".</span><span class="sxs-lookup"><span data-stu-id="9fee1-123">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="9fee1-124">Lai vienmēr parādītu divas decimāldaļas vietas, izmantojiet `$Qty:0.00$`.</span><span class="sxs-lookup"><span data-stu-id="9fee1-124">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="9fee1-125">Piemēram, ja daudzums ir 10, etiķetē tiks parādīts "10.00".</span><span class="sxs-lookup"><span data-stu-id="9fee1-125">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="9fee1-126">Pilnīgu pieejamo skaitļu formāta virkņu sarakstu skatiet [Pielāgotās skaitļu formāta virknes](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="9fee1-126">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="9fee1-127">Pielāgotu virkņu formāti</span><span class="sxs-lookup"><span data-stu-id="9fee1-127">Custom string formats</span></span>

<span data-ttu-id="9fee1-128">Jūs varat noņemt virknes pirmās rakstzīmes, izmantojot šādu lauku un formāta kodu.</span><span class="sxs-lookup"><span data-stu-id="9fee1-128">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="9fee1-129">Šeit `#` norāda izlaisto rakstzīmju skaitu.</span><span class="sxs-lookup"><span data-stu-id="9fee1-129">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="9fee1-130">Piemēram, lai drukātu Sērijas pārvadāšanas konteinera koda (SSCC) numura zīmes numuru, kurā nav iekļautas pirmās divas rakstzīmes, izmantojiet `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="9fee1-130">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="9fee1-131">Šādā gadījumā numura zīmes numurs 0011111111111222221 tiks drukāts kā "11111111111222221".</span><span class="sxs-lookup"><span data-stu-id="9fee1-131">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="9fee1-132">Pielāgotie datuma/laika formāti</span><span class="sxs-lookup"><span data-stu-id="9fee1-132">Custom date/time formats</span></span>

<span data-ttu-id="9fee1-133">Šajā piemērā ir parādīts, kā varat kontrolēt formātu, kas tiek izmantots, lai drukātu datumus.</span><span class="sxs-lookup"><span data-stu-id="9fee1-133">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="9fee1-134">Šajā piemērā datums 2020. gada 30. aprīlis tiks drukāts kā "30-04-2020".</span><span class="sxs-lookup"><span data-stu-id="9fee1-134">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="9fee1-135">Pilnīgu pieejamo datuma/laika formātu sarakstu skatiet [Pielāgotās datuma un laika formāta virknes](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="9fee1-135">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="9fee1-136">Drukāt atsevišķas rindas no vairākrindu datiem</span><span class="sxs-lookup"><span data-stu-id="9fee1-136">Print individual lines from multiline data</span></span>

<span data-ttu-id="9fee1-137">Ja datu lauks satur vairākas rindas (t.i., rindas, kas atdalītas ar rindu pārtraukumiem), varat izdrukāt atsevišķu rindu, lietojot šādu formātu.</span><span class="sxs-lookup"><span data-stu-id="9fee1-137">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="9fee1-138">Šeit `#` ir rindas numurs, ko vēlaties drukāt.</span><span class="sxs-lookup"><span data-stu-id="9fee1-138">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="9fee1-139">(Pirmajai rindai izmantojiet 1.)</span><span class="sxs-lookup"><span data-stu-id="9fee1-139">(Use 1 for the first line.)</span></span>

<span data-ttu-id="9fee1-140">Piemēram, sistēmai ir `AdditionalAddress` lauks, kurā tiek uzglabāta šāda daudzrindu adrese:</span><span class="sxs-lookup"><span data-stu-id="9fee1-140">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="9fee1-141">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="9fee1-141">Contoso Inc.</span></span>  
<span data-ttu-id="9fee1-142">Ielas nosaukums 123</span><span class="sxs-lookup"><span data-stu-id="9fee1-142">123 Street Name</span></span>  
<span data-ttu-id="9fee1-143">Kāda pilsēta, kāds štats</span><span class="sxs-lookup"><span data-stu-id="9fee1-143">Some City, Some State</span></span>

<span data-ttu-id="9fee1-144">Šo adresi var drukāt pa vienai rindai, izmantojot tālāk norādītos kodus.</span><span class="sxs-lookup"><span data-stu-id="9fee1-144">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="9fee1-145">Kods</span><span class="sxs-lookup"><span data-stu-id="9fee1-145">Code</span></span> | <span data-ttu-id="9fee1-146">Drukātais teksts</span><span class="sxs-lookup"><span data-stu-id="9fee1-146">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="9fee1-147">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="9fee1-147">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="9fee1-148">Ielas nosaukums 123</span><span class="sxs-lookup"><span data-stu-id="9fee1-148">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="9fee1-149">Kāda pilsēta, kāds štats</span><span class="sxs-lookup"><span data-stu-id="9fee1-149">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="9fee1-150">Drukāt un formatēt no ekrāna metodes</span><span class="sxs-lookup"><span data-stu-id="9fee1-150">Print and format from a display method</span></span>

<span data-ttu-id="9fee1-151">Jūs varat drukāt no ekrāna metodes, izmantojot sekojošo formātu.</span><span class="sxs-lookup"><span data-stu-id="9fee1-151">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="9fee1-152">Jūs varat kombinēt šo formātu ar citiem tipiem, kas tika aprakstīti iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="9fee1-152">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="9fee1-153">Piemēram, jums ir ekrāna metode, kas ir nosaukta `DisplayListOfItemsNumbers()`, un jūs vēlaties izdrukāt šīs metodes pirmo preces numuru.</span><span class="sxs-lookup"><span data-stu-id="9fee1-153">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="9fee1-154">Šajā gadījumā, var izmantot sekojošo kodu.</span><span class="sxs-lookup"><span data-stu-id="9fee1-154">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="9fee1-155">Papildinformācija par etiķešu drukāšanu</span><span class="sxs-lookup"><span data-stu-id="9fee1-155">More information about how to print labels</span></span>

<span data-ttu-id="9fee1-156">Papildinformāciju par to, kā iestatīt un drukāt etiķetes, skatiet [Iespējot numura zīmes etiķetes drukāšanu](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="9fee1-156">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>
