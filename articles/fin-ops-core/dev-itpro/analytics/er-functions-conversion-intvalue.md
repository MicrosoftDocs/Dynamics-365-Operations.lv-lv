---
title: INTVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INTVALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755376"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="a2af6-103">INTVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="a2af6-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2af6-104">`INTVALUE` funkcija atgriež *Int* vērtību, kas apzīmē norādīto virkni.</span><span class="sxs-lookup"><span data-stu-id="a2af6-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="a2af6-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="a2af6-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="a2af6-106">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="a2af6-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="a2af6-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="a2af6-107">Arguments</span></span>

<span data-ttu-id="a2af6-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="a2af6-108">`text`: *String*</span></span>

<span data-ttu-id="a2af6-109">Teksta vērtība, kas ir jāpārvērš par *Int* skaitli.</span><span class="sxs-lookup"><span data-stu-id="a2af6-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="a2af6-110">`number`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="a2af6-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="a2af6-111">Skaitliska *Reālā* vai *Veselā skaitļa* vērtība , kas ir jāpārvērš par *Int* skaitli.</span><span class="sxs-lookup"><span data-stu-id="a2af6-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="a2af6-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="a2af6-112">Return values</span></span>

<span data-ttu-id="a2af6-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="a2af6-113">*Int*</span></span>

<span data-ttu-id="a2af6-114">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="a2af6-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a2af6-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="a2af6-115">Usage notes</span></span>

<span data-ttu-id="a2af6-116">Tiek aprautas visas decimāldaļas.</span><span class="sxs-lookup"><span data-stu-id="a2af6-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="a2af6-117">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="a2af6-117">Example 1</span></span>

<span data-ttu-id="a2af6-118">`INTVALUE ("100.77")` atgriež *Int* vērtību **100**.</span><span class="sxs-lookup"><span data-stu-id="a2af6-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a2af6-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="a2af6-119">Example 2</span></span>

<span data-ttu-id="a2af6-120">`INTVALUE (-100.77)` atgriež *Int* vērtību **-100**.</span><span class="sxs-lookup"><span data-stu-id="a2af6-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2af6-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a2af6-121">Additional resources</span></span>

[<span data-ttu-id="a2af6-122">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="a2af6-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]