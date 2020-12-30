---
title: CONCATENATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CONCATENATE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 903429994ae5618b597aa0ab0991e9f6783a96ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687942"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="7b765-103">CONCATENATE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="7b765-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b765-104">`CONCATENATE` funkcija atgriež visas norādītās teksta virknes kā *Virknes* vērtību pēc tam, kad tās ir apvienotas vienā virknē.</span><span class="sxs-lookup"><span data-stu-id="7b765-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b765-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="7b765-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="7b765-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="7b765-106">Arguments</span></span>

<span data-ttu-id="7b765-107">`text 1`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="7b765-107">`text 1`: *String*</span></span>

<span data-ttu-id="7b765-108">Atsauce uz datu avotu *Virknes* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="7b765-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="7b765-109">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="7b765-109">This argument is required.</span></span>

<span data-ttu-id="7b765-110">`text N`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="7b765-110">`text N`: *String*</span></span>

<span data-ttu-id="7b765-111">Atsauce uz datu avotu *Virknes* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="7b765-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="7b765-112">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="7b765-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="7b765-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="7b765-113">Return values</span></span>

<span data-ttu-id="7b765-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="7b765-114">*String*</span></span>

<span data-ttu-id="7b765-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="7b765-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7b765-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="7b765-116">Example</span></span>

<span data-ttu-id="7b765-117">`CONCATENATE ("abc", "def")` atgriež **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="7b765-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7b765-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="7b765-118">Usage notes</span></span>

<span data-ttu-id="7b765-119">Arī izteiksme `"abc" & "def"` atgriež **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="7b765-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b765-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7b765-120">Additional resources</span></span>

[<span data-ttu-id="7b765-121">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="7b765-121">Text functions</span></span>](er-functions-category-text.md)
