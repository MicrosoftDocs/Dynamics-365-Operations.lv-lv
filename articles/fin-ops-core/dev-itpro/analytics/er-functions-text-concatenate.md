---
title: CONCATENATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CONCATENATE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569609"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="69bb8-103">CONCATENATE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="69bb8-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69bb8-104">`CONCATENATE` funkcija atgriež visas norādītās teksta virknes kā *Virknes* vērtību pēc tam, kad tās ir apvienotas vienā virknē.</span><span class="sxs-lookup"><span data-stu-id="69bb8-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="69bb8-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="69bb8-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="69bb8-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="69bb8-106">Arguments</span></span>

<span data-ttu-id="69bb8-107">`text 1`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="69bb8-107">`text 1`: *String*</span></span>

<span data-ttu-id="69bb8-108">Atsauce uz datu avotu *Virknes* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="69bb8-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="69bb8-109">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="69bb8-109">This argument is required.</span></span>

<span data-ttu-id="69bb8-110">`text N`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="69bb8-110">`text N`: *String*</span></span>

<span data-ttu-id="69bb8-111">Atsauce uz datu avotu *Virknes* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="69bb8-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="69bb8-112">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="69bb8-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="69bb8-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="69bb8-113">Return values</span></span>

<span data-ttu-id="69bb8-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="69bb8-114">*String*</span></span>

<span data-ttu-id="69bb8-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="69bb8-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="69bb8-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="69bb8-116">Example</span></span>

<span data-ttu-id="69bb8-117">`CONCATENATE ("abc", "def")` atgriež **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="69bb8-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="69bb8-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="69bb8-118">Usage notes</span></span>

<span data-ttu-id="69bb8-119">Arī izteiksme `"abc" & "def"` atgriež **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="69bb8-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69bb8-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="69bb8-120">Additional resources</span></span>

[<span data-ttu-id="69bb8-121">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="69bb8-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]