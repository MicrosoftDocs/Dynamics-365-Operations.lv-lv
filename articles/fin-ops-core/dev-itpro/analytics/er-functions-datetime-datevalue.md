---
title: DATEVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATEVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 82feb8284f4b6116a53d174dcdd9b8c09c4fa63a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563562"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="8da2f-103">DATEVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="8da2f-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8da2f-104">`DATEVALUE` funkcija atgriež *Datuma* vērtību, kas tiek konvertēta no dotās teksta vērtības norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) datuma/laika vērtībai.</span><span class="sxs-lookup"><span data-stu-id="8da2f-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="8da2f-105">Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="8da2f-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="8da2f-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="8da2f-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="8da2f-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="8da2f-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="8da2f-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="8da2f-108">Arguments</span></span>

<span data-ttu-id="8da2f-109">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="8da2f-109">`text`: *String*</span></span>

<span data-ttu-id="8da2f-110">Teksts, kas apzīmē formatējamo vērtību.</span><span class="sxs-lookup"><span data-stu-id="8da2f-110">Text that represents the value to format.</span></span>

<span data-ttu-id="8da2f-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="8da2f-111">`format`: *String*</span></span>

<span data-ttu-id="8da2f-112">Norādītā teksta formāts.</span><span class="sxs-lookup"><span data-stu-id="8da2f-112">The format of the given text.</span></span>

<span data-ttu-id="8da2f-113">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="8da2f-113">`culture`: *String*</span></span>

<span data-ttu-id="8da2f-114">Kultūra, kas tiek izmantota dotā teksta formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="8da2f-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="8da2f-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="8da2f-115">Return values</span></span>

<span data-ttu-id="8da2f-116">*Datums*</span><span class="sxs-lookup"><span data-stu-id="8da2f-116">*Date*</span></span>

<span data-ttu-id="8da2f-117">Iegūtā datuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="8da2f-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8da2f-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="8da2f-118">Usage notes</span></span>

<span data-ttu-id="8da2f-119">Ja kultūra nav definēta kā izsauktās funkcijas arguments, vērtību `culture` nosaka izsaukuma konteksts.</span><span class="sxs-lookup"><span data-stu-id="8da2f-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="8da2f-120">Piemēram, ja `DATEVALUE` funkcija tiek izsaukta, izmantojot 1. sintaksi elektroniskā pārskata (ER) formātā **FAILA** elementam, kas ir konfigurēts, lai izmantotu vācu kultūru, konvertēšana tiks veikta, izmantojot vācu kultūru.</span><span class="sxs-lookup"><span data-stu-id="8da2f-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="8da2f-121">Noklusējuma `culture` vērtība ir **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="8da2f-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="8da2f-122">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="8da2f-122">Example 1</span></span>

<span data-ttu-id="8da2f-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` atgriež datuma vērtību **2016. gada 21. decembris**, pamatojoties uz norādīto pielāgoto formātu un noklusējuma lietojumprogrammas **EN-US** kultūru.</span><span class="sxs-lookup"><span data-stu-id="8da2f-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="8da2f-124">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="8da2f-124">Example 2</span></span>

<span data-ttu-id="8da2f-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` atgriež datuma vērtību **2016. gada 21. janvāri**, pamatojoties uz norādīto pielāgoto formātu un kultūru.</span><span class="sxs-lookup"><span data-stu-id="8da2f-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="8da2f-126">Taču `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` parāda izņēmumu, lai informētu lietotāju par to, ka norādītā virkne nav atpazīta kā derīga datuma vērtība norādītajai kultūrai.</span><span class="sxs-lookup"><span data-stu-id="8da2f-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8da2f-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8da2f-127">Additional resources</span></span>

[<span data-ttu-id="8da2f-128">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="8da2f-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]