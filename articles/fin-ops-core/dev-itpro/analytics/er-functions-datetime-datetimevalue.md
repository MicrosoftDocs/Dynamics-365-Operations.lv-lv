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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30879796b483752a578e516d8afd75f5a690cabc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684911"
---
# <a name="datetimevalue-er-function"></a><span data-ttu-id="2a84a-103">DATETIMEVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="2a84a-103">DATETIMEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a84a-104">`DATETIMEVALUE` funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) datuma/laika vērtībai.</span><span class="sxs-lookup"><span data-stu-id="2a84a-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="2a84a-105">Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="2a84a-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="2a84a-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="2a84a-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="2a84a-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="2a84a-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="2a84a-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="2a84a-108">Arguments</span></span>

<span data-ttu-id="2a84a-109">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="2a84a-109">`text`: *String*</span></span>

<span data-ttu-id="2a84a-110">Teksts, kas apzīmē formatējamo vērtību.</span><span class="sxs-lookup"><span data-stu-id="2a84a-110">Text that represents the value to format.</span></span>

<span data-ttu-id="2a84a-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="2a84a-111">`format`: *String*</span></span>

<span data-ttu-id="2a84a-112">Norādītā teksta formāts.</span><span class="sxs-lookup"><span data-stu-id="2a84a-112">The format of the given text.</span></span>

<span data-ttu-id="2a84a-113">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="2a84a-113">`culture`: *String*</span></span>

<span data-ttu-id="2a84a-114">Kultūra, kas tiek izmantota dotā teksta formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="2a84a-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="2a84a-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="2a84a-115">Return values</span></span>

<span data-ttu-id="2a84a-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="2a84a-116">*DateTime*</span></span>

<span data-ttu-id="2a84a-117">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="2a84a-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2a84a-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="2a84a-118">Usage notes</span></span>

<span data-ttu-id="2a84a-119">Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts.</span><span class="sxs-lookup"><span data-stu-id="2a84a-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="2a84a-120">Piemēram, ja `DATETIMEVALUE` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru.</span><span class="sxs-lookup"><span data-stu-id="2a84a-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="2a84a-121">Noklusējuma `culture` vērtība ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="2a84a-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="2a84a-122">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="2a84a-122">Example 1</span></span>

<span data-ttu-id="2a84a-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` atgriež **2:55:00 AM 2016. gada 21. decembrī**, pamatojoties uz norādīto pielāgoto formātu un noklusējuma lietojumprogrammas **EN-US** kultūru.</span><span class="sxs-lookup"><span data-stu-id="2a84a-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="2a84a-124">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="2a84a-124">Example 2</span></span>

<span data-ttu-id="2a84a-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` atgriež **2:55:00 AM 2016. gada 21. decembrī**, pamatojoties uz norādīto pielāgoto formātu un kultūru.</span><span class="sxs-lookup"><span data-stu-id="2a84a-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="2a84a-126">Taču `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` parāda izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīga datuma/laika vērtība norādītajai kultūrai.</span><span class="sxs-lookup"><span data-stu-id="2a84a-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a84a-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2a84a-127">Additional resources</span></span>

[<span data-ttu-id="2a84a-128">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="2a84a-128">Date and time functions</span></span>](er-functions-category-datetime.md)
