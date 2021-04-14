---
title: INT64VALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INT64VALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 89a26e867579bcb34a9bae33fa0b98e1ecfe9995
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755400"
---
# <a name="int64value-er-function"></a><span data-ttu-id="c7991-103">INT64VALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="c7991-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7991-104">`INT64VALUE` funkcija atgriež *Int64* vērtību, kas apzīmē norādīto virkni.</span><span class="sxs-lookup"><span data-stu-id="c7991-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="c7991-105">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="c7991-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="c7991-106">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="c7991-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="c7991-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="c7991-107">Arguments</span></span>

<span data-ttu-id="c7991-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="c7991-108">`text`: *String*</span></span>

<span data-ttu-id="c7991-109">Teksta vērtība, kas ir jāpārvērš par *Int64* skaitli.</span><span class="sxs-lookup"><span data-stu-id="c7991-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="c7991-110">`number`: *Reāls* vai *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="c7991-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="c7991-111">Skaitliska *Reālā* vai *Veselā skaitļa* vērtība , kas ir jāpārvērš par *Int64* skaitli.</span><span class="sxs-lookup"><span data-stu-id="c7991-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="c7991-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="c7991-112">Return values</span></span>

<span data-ttu-id="c7991-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="c7991-113">*Int64*</span></span>

<span data-ttu-id="c7991-114">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="c7991-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c7991-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="c7991-115">Usage notes</span></span>

<span data-ttu-id="c7991-116">Tiek aprautas visas decimāldaļas.</span><span class="sxs-lookup"><span data-stu-id="c7991-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="c7991-117">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="c7991-117">Example 1</span></span>

<span data-ttu-id="c7991-118">`INT64VALUE ("22565422744")` atgriež *Int64* vērtību **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="c7991-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c7991-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="c7991-119">Example 2</span></span>

<span data-ttu-id="c7991-120">`INT64VALUE ( VALUE("22565422744.77"))` atgriež *Int64* vērtību **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="c7991-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7991-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c7991-121">Additional resources</span></span>

[<span data-ttu-id="c7991-122">Tipa pārveidošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="c7991-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]