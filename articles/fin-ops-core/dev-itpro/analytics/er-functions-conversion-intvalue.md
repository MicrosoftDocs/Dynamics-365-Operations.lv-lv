---
title: INTVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INTVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2b279de39cf91c3919145735518034fc60cd3341
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917722"
---
# <span data-ttu-id="04c4e-103"><a name="INTVALUE">INTVALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="04c4e-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04c4e-104">`INTVALUE` funkcija atgriež *Int* vērtību, kas apzīmē norādīto virkni.</span><span class="sxs-lookup"><span data-stu-id="04c4e-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="04c4e-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="04c4e-105">Syntax 1</span></span>

```
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="04c4e-106">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="04c4e-106">Syntax 2</span></span>

```
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="04c4e-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="04c4e-107">Arguments</span></span>

<span data-ttu-id="04c4e-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="04c4e-108">`text`: *String*</span></span>

<span data-ttu-id="04c4e-109">Teksta vērtība, kas ir jāpārvērš par *Int* skaitli.</span><span class="sxs-lookup"><span data-stu-id="04c4e-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="04c4e-110">`number`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="04c4e-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="04c4e-111">Skaitliska *Reālā* vai *Veselā skaitļa* vērtība , kas ir jāpārvērš par *Int* skaitli.</span><span class="sxs-lookup"><span data-stu-id="04c4e-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="04c4e-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="04c4e-112">Return values</span></span>

<span data-ttu-id="04c4e-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="04c4e-113">*Int*</span></span>

<span data-ttu-id="04c4e-114">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="04c4e-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="04c4e-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="04c4e-115">Usage notes</span></span>

<span data-ttu-id="04c4e-116">Tiek aprautas visas decimāldaļas.</span><span class="sxs-lookup"><span data-stu-id="04c4e-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="04c4e-117">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="04c4e-117">Example 1</span></span>

<span data-ttu-id="04c4e-118">`INTVALUE ("100.77")`atgriež *Int* vērtību **100**.</span><span class="sxs-lookup"><span data-stu-id="04c4e-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="04c4e-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="04c4e-119">Example 2</span></span>

<span data-ttu-id="04c4e-120">`INTVALUE (-100.77)`atgriež *Int* vērtību **-100**.</span><span class="sxs-lookup"><span data-stu-id="04c4e-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04c4e-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="04c4e-121">Additional resources</span></span>

[<span data-ttu-id="04c4e-122">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="04c4e-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
