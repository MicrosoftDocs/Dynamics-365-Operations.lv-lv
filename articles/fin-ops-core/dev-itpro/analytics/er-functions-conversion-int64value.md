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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042692"
---
# <span data-ttu-id="dccaf-103"><a name="INT64VALUE">INT64VALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="dccaf-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dccaf-104">`INT64VALUE` funkcija atgriež *Int64* vērtību, kas apzīmē norādīto virkni.</span><span class="sxs-lookup"><span data-stu-id="dccaf-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="dccaf-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="dccaf-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="dccaf-106">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="dccaf-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="dccaf-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="dccaf-107">Arguments</span></span>

<span data-ttu-id="dccaf-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="dccaf-108">`text`: *String*</span></span>

<span data-ttu-id="dccaf-109">Teksta vērtība, kas ir jāpārvērš par *Int64* skaitli.</span><span class="sxs-lookup"><span data-stu-id="dccaf-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="dccaf-110">`number`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="dccaf-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="dccaf-111">Skaitliska *Reālā* vai *Veselā skaitļa* vērtība , kas ir jāpārvērš par *Int64* skaitli.</span><span class="sxs-lookup"><span data-stu-id="dccaf-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="dccaf-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="dccaf-112">Return values</span></span>

<span data-ttu-id="dccaf-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="dccaf-113">*Int64*</span></span>

<span data-ttu-id="dccaf-114">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="dccaf-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="dccaf-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="dccaf-115">Usage notes</span></span>

<span data-ttu-id="dccaf-116">Tiek aprautas visas decimāldaļas.</span><span class="sxs-lookup"><span data-stu-id="dccaf-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="dccaf-117">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="dccaf-117">Example 1</span></span>

<span data-ttu-id="dccaf-118">`INT64VALUE ("22565422744")`atgriež *Int64* vērtību **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="dccaf-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="dccaf-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="dccaf-119">Example 2</span></span>

<span data-ttu-id="dccaf-120">`INT64VALUE ( VALUE("22565422744.77"))`atgriež *Int64* vērtību **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="dccaf-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dccaf-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="dccaf-121">Additional resources</span></span>

[<span data-ttu-id="dccaf-122">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="dccaf-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
