---
title: NUMBERFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMBERFORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 8de57d8b0a45b8b58849a24f2d8f0cde41e0ea3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746222"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="c1a90-103">NUMBERFORMAT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="c1a90-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1a90-104">`NUMBERFORMAT` funkcija atgriež *Virknes* vērtību, kas norādīto skaitu uzrāda norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="c1a90-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="c1a90-105">Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="c1a90-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="c1a90-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="c1a90-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="c1a90-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="c1a90-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="c1a90-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="c1a90-108">Arguments</span></span>

<span data-ttu-id="c1a90-109">`number`: *Vesels skaitlis* vai *Reāls*</span><span class="sxs-lookup"><span data-stu-id="c1a90-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="c1a90-110">Skaitliska vērtība, kas norāda skaitli, kas ir jāformatē.</span><span class="sxs-lookup"><span data-stu-id="c1a90-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="c1a90-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="c1a90-111">`format` : *String*</span></span>

<span data-ttu-id="c1a90-112">*Virknes* vērtība, kas apzīmē formātu.</span><span class="sxs-lookup"><span data-stu-id="c1a90-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="c1a90-113">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="c1a90-113">`culture`: *String*</span></span>

<span data-ttu-id="c1a90-114">*Virknes* vērtība, kas apzīmē kultūru, kuru izmantot formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="c1a90-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="c1a90-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="c1a90-115">Return values</span></span>

<span data-ttu-id="c1a90-116">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="c1a90-116">*String*</span></span>

<span data-ttu-id="c1a90-117">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="c1a90-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c1a90-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="c1a90-118">Usage notes</span></span>

<span data-ttu-id="c1a90-119">Ja kultūra nav definēta kā izsauktās funkcijas arguments, šī funkcija tiek palaista kontekstā, kas nosaka, kāda kultūra tiek izmantota skaitļu formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="c1a90-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="c1a90-120">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="c1a90-120">Example 1</span></span>

<span data-ttu-id="c1a90-121">Kultūrai **EN-US** izteiksme `NUMBERFORMAT (0.45, "p")` atgriež **"45.00 %"** un `NUMBERFORMAT (10.45, "#")` atgriež **"10"**.</span><span class="sxs-lookup"><span data-stu-id="c1a90-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c1a90-122">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="c1a90-122">Example 2</span></span>

<span data-ttu-id="c1a90-123">`NUMBERFORMAT (10/3, "F2", "de")` atgriež **3,33**, bet `NUMBERFORMAT (10/3, "F2", "en-us")` atgriež **3,33**.</span><span class="sxs-lookup"><span data-stu-id="c1a90-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1a90-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c1a90-124">Additional resources</span></span>

[<span data-ttu-id="c1a90-125">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="c1a90-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]