---
title: DATEVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATEVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: d760c3f874bfebad11b9497b136cb67df4e9ea61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746943"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="287ac-103">DATEVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="287ac-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="287ac-104">`DATEVALUE` funkcija atgriež *Datuma* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) datuma/laika vērtībai.</span><span class="sxs-lookup"><span data-stu-id="287ac-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="287ac-105">Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="287ac-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="287ac-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="287ac-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="287ac-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="287ac-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="287ac-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="287ac-108">Arguments</span></span>

<span data-ttu-id="287ac-109">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="287ac-109">`text`: *String*</span></span>

<span data-ttu-id="287ac-110">Teksts, kas apzīmē formatējamo vērtību.</span><span class="sxs-lookup"><span data-stu-id="287ac-110">Text that represents the value to format.</span></span>

<span data-ttu-id="287ac-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="287ac-111">`format`: *String*</span></span>

<span data-ttu-id="287ac-112">Norādītā teksta formāts.</span><span class="sxs-lookup"><span data-stu-id="287ac-112">The format of the given text.</span></span>

<span data-ttu-id="287ac-113">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="287ac-113">`culture`: *String*</span></span>

<span data-ttu-id="287ac-114">Kultūra, kas tiek izmantota dotā teksta formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="287ac-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="287ac-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="287ac-115">Return values</span></span>

<span data-ttu-id="287ac-116">*Datums*</span><span class="sxs-lookup"><span data-stu-id="287ac-116">*Date*</span></span>

<span data-ttu-id="287ac-117">Iegūtā datuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="287ac-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="287ac-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="287ac-118">Usage notes</span></span>

<span data-ttu-id="287ac-119">Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts.</span><span class="sxs-lookup"><span data-stu-id="287ac-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="287ac-120">Piemēram, ja `DATEVALUE` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru.</span><span class="sxs-lookup"><span data-stu-id="287ac-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="287ac-121">Noklusējuma `culture` vērtība ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="287ac-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="287ac-122">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="287ac-122">Example 1</span></span>

<span data-ttu-id="287ac-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` atgriež datuma vērtību **2016. gada 21. decembris**, pamatojoties uz norādīto pielāgoto formātu un noklusējuma lietojumprogrammas **EN-US** kultūru.</span><span class="sxs-lookup"><span data-stu-id="287ac-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="287ac-124">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="287ac-124">Example 2</span></span>

<span data-ttu-id="287ac-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` atgriež datuma vērtību **2016. gada 21. janvāri**, pamatojoties uz norādīto pielāgoto formātu un kultūru.</span><span class="sxs-lookup"><span data-stu-id="287ac-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="287ac-126">Taču `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` parāda izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīga datuma vērtība norādītajai kultūrai.</span><span class="sxs-lookup"><span data-stu-id="287ac-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="287ac-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="287ac-127">Additional resources</span></span>

[<span data-ttu-id="287ac-128">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="287ac-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]