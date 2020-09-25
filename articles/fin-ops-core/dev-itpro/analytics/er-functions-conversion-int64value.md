---
title: INT64VALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INT64VALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 78b69b5280fb8c7ed99d73568097cd0c080a807a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744843"
---
# <a name="int64value-er-function"></a><span data-ttu-id="31867-103">INT64VALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="31867-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31867-104">`INT64VALUE` funkcija atgriež *Int64* vērtību, kas apzīmē norādīto virkni.</span><span class="sxs-lookup"><span data-stu-id="31867-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="31867-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="31867-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="31867-106">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="31867-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="31867-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="31867-107">Arguments</span></span>

<span data-ttu-id="31867-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="31867-108">`text`: *String*</span></span>

<span data-ttu-id="31867-109">Teksta vērtība, kas ir jāpārvērš par *Int64* skaitli.</span><span class="sxs-lookup"><span data-stu-id="31867-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="31867-110">`number`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="31867-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="31867-111">Skaitliska *Reālā* vai *Veselā skaitļa* vērtība , kas ir jāpārvērš par *Int64* skaitli.</span><span class="sxs-lookup"><span data-stu-id="31867-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="31867-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="31867-112">Return values</span></span>

<span data-ttu-id="31867-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="31867-113">*Int64*</span></span>

<span data-ttu-id="31867-114">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="31867-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="31867-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="31867-115">Usage notes</span></span>

<span data-ttu-id="31867-116">Tiek aprautas visas decimāldaļas.</span><span class="sxs-lookup"><span data-stu-id="31867-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="31867-117">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="31867-117">Example 1</span></span>

<span data-ttu-id="31867-118">`INT64VALUE ("22565422744")` atgriež *Int64* vērtību **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="31867-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="31867-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="31867-119">Example 2</span></span>

<span data-ttu-id="31867-120">`INT64VALUE ( VALUE("22565422744.77"))` atgriež *Int64* vērtību **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="31867-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31867-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="31867-121">Additional resources</span></span>

[<span data-ttu-id="31867-122">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="31867-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
