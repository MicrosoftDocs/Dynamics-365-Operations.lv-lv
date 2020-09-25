---
title: NUMBERFORMAT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMBERFORMAT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 8a431414044846bf4e79e6b9f0e5b27281ea8f46
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744411"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="6ee37-103">NUMBERFORMAT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="6ee37-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ee37-104">`NUMBERFORMAT` funkcija atgriež *Virknes* vērtību, kas norādīto skaitu uzrāda norādītajā formātā un pēc izvēles norādītajā [kultūrā](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="6ee37-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="6ee37-105">Papildinformāciju par atbalstītajiem formātiem skatiet sadaļās [standarta](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) un [pielāgots](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="6ee37-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="6ee37-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="6ee37-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="6ee37-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="6ee37-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="6ee37-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="6ee37-108">Arguments</span></span>

<span data-ttu-id="6ee37-109">`number`: *Vesels skaitlis* vai *Reāls*</span><span class="sxs-lookup"><span data-stu-id="6ee37-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="6ee37-110">Skaitliska vērtība, kas norāda skaitli, kas ir jāformatē.</span><span class="sxs-lookup"><span data-stu-id="6ee37-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="6ee37-111">`format`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="6ee37-111">`format` : *String*</span></span>

<span data-ttu-id="6ee37-112">*Virknes* vērtība, kas apzīmē formātu.</span><span class="sxs-lookup"><span data-stu-id="6ee37-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="6ee37-113">`culture`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="6ee37-113">`culture`: *String*</span></span>

<span data-ttu-id="6ee37-114">*Virknes* vērtība, kas apzīmē kultūru, kuru izmantot formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="6ee37-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ee37-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="6ee37-115">Return values</span></span>

<span data-ttu-id="6ee37-116">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="6ee37-116">*String*</span></span>

<span data-ttu-id="6ee37-117">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="6ee37-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6ee37-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="6ee37-118">Usage notes</span></span>

<span data-ttu-id="6ee37-119">Ja kultūra nav definēta kā izsauktās funkcijas arguments, šī funkcija tiek palaista kontekstā, kas nosaka, kāda kultūra tiek izmantota skaitļu formatēšanai.</span><span class="sxs-lookup"><span data-stu-id="6ee37-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="6ee37-120">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="6ee37-120">Example 1</span></span>

<span data-ttu-id="6ee37-121">Kultūrai **EN-US** izteiksme `NUMBERFORMAT (0.45, "p")` atgriež **"45.00 %"** un `NUMBERFORMAT (10.45, "#")` atgriež **"10"**.</span><span class="sxs-lookup"><span data-stu-id="6ee37-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6ee37-122">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="6ee37-122">Example 2</span></span>

<span data-ttu-id="6ee37-123">`NUMBERFORMAT (10/3, "F2", "de")` atgriež **3,33**, bet `NUMBERFORMAT (10/3, "F2", "en-us")` atgriež **3,33**.</span><span class="sxs-lookup"><span data-stu-id="6ee37-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ee37-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6ee37-124">Additional resources</span></span>

[<span data-ttu-id="6ee37-125">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="6ee37-125">Text functions</span></span>](er-functions-category-text.md)
