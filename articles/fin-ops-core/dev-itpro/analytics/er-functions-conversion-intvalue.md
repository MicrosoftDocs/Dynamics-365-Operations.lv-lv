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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98b91a983c60bb99280763f7f7a944d08f535e60
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686007"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="a7aa6-103">INTVALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="a7aa6-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7aa6-104">`INTVALUE` funkcija atgriež *Int* vērtību, kas apzīmē norādīto virkni.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="a7aa6-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="a7aa6-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="a7aa6-106">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="a7aa6-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="a7aa6-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="a7aa6-107">Arguments</span></span>

<span data-ttu-id="a7aa6-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="a7aa6-108">`text`: *String*</span></span>

<span data-ttu-id="a7aa6-109">Teksta vērtība, kas ir jāpārvērš par *Int* skaitli.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="a7aa6-110">`number`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="a7aa6-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="a7aa6-111">Skaitliska *Reālā* vai *Veselā skaitļa* vērtība , kas ir jāpārvērš par *Int* skaitli.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="a7aa6-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="a7aa6-112">Return values</span></span>

<span data-ttu-id="a7aa6-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="a7aa6-113">*Int*</span></span>

<span data-ttu-id="a7aa6-114">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a7aa6-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="a7aa6-115">Usage notes</span></span>

<span data-ttu-id="a7aa6-116">Tiek aprautas visas decimāldaļas.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="a7aa6-117">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="a7aa6-117">Example 1</span></span>

<span data-ttu-id="a7aa6-118">`INTVALUE ("100.77")` atgriež *Int* vērtību **100**.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a7aa6-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="a7aa6-119">Example 2</span></span>

<span data-ttu-id="a7aa6-120">`INTVALUE (-100.77)` atgriež *Int* vērtību **-100**.</span><span class="sxs-lookup"><span data-stu-id="a7aa6-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7aa6-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a7aa6-121">Additional resources</span></span>

[<span data-ttu-id="a7aa6-122">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="a7aa6-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
