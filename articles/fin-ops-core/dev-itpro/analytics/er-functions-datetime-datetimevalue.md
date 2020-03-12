---
title: DATETIMEVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATETIMEVALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 29d81599563dec2827fa8a82c86b74cb9e34eea2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070694"
---
# <span data-ttu-id="d27a2-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="d27a2-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d27a2-104">`DATETIMEVALUE` funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) datuma/laika vērtībai.</span><span class="sxs-lookup"><span data-stu-id="d27a2-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="d27a2-105">(Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="d27a2-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d27a2-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="d27a2-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d27a2-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="d27a2-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d27a2-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d27a2-108">Arguments</span></span>

<span data-ttu-id="d27a2-109">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d27a2-109">`text`: *String*</span></span>

<span data-ttu-id="d27a2-110">Teksts, kas apzīmē formatējamo vērtību.</span><span class="sxs-lookup"><span data-stu-id="d27a2-110">Text that represents the value to format.</span></span>

<span data-ttu-id="d27a2-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d27a2-111">`format`: *String*</span></span>

<span data-ttu-id="d27a2-112">Norādītā teksta formāts.</span><span class="sxs-lookup"><span data-stu-id="d27a2-112">The format of the given text.</span></span>

<span data-ttu-id="d27a2-113">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d27a2-113">`culture`: *String*</span></span>

<span data-ttu-id="d27a2-114">Kultūra, kas tiek izmantota dotā teksta formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="d27a2-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="d27a2-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d27a2-115">Return values</span></span>

<span data-ttu-id="d27a2-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="d27a2-116">*DateTime*</span></span>

<span data-ttu-id="d27a2-117">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="d27a2-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d27a2-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="d27a2-118">Usage notes</span></span>

<span data-ttu-id="d27a2-119">Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts.</span><span class="sxs-lookup"><span data-stu-id="d27a2-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="d27a2-120">Piemēram, ja `DATETIMEVALUE` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru.</span><span class="sxs-lookup"><span data-stu-id="d27a2-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="d27a2-121">Noklusējuma `culture` vērtība ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="d27a2-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="d27a2-122">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="d27a2-122">Example 1</span></span>

<span data-ttu-id="d27a2-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` atgriež **2:55:00 AM 2016. gada 21. decembrī**, pamatojoties uz norādīto pielāgoto formātu un noklusējuma lietojumprogrammas **EN-US** kultūru.</span><span class="sxs-lookup"><span data-stu-id="d27a2-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="d27a2-124">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="d27a2-124">Example 2</span></span>

<span data-ttu-id="d27a2-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` atgriež **2:55:00 AM 2016. gada 21. decembrī**, pamatojoties uz norādīto pielāgoto formātu un kultūru.</span><span class="sxs-lookup"><span data-stu-id="d27a2-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="d27a2-126">Taču `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` parāda izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīga datuma/laika vērtība norādītajai kultūrai.</span><span class="sxs-lookup"><span data-stu-id="d27a2-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d27a2-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d27a2-127">Additional resources</span></span>

[<span data-ttu-id="d27a2-128">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="d27a2-128">Date and time functions</span></span>](er-functions-category-datetime.md)
