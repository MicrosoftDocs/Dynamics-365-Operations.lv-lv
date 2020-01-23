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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915767"
---
# <span data-ttu-id="bbe30-103"><a name="CONCATENATE">CONCATENATE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="bbe30-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbe30-104">`CONCATENATE` funkcija atgriež visas norādītās teksta virknes kā *Virknes* vērtību pēc tam, kad tās ir apvienotas vienā virknē.</span><span class="sxs-lookup"><span data-stu-id="bbe30-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe30-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="bbe30-105">Syntax</span></span>

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="bbe30-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="bbe30-106">Arguments</span></span>

<span data-ttu-id="bbe30-107">`text 1`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="bbe30-107">`text 1`: *String*</span></span>

<span data-ttu-id="bbe30-108">Atsauce uz datu avotu *Virknes* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="bbe30-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="bbe30-109">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="bbe30-109">This argument is required.</span></span>

<span data-ttu-id="bbe30-110">`text N`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="bbe30-110">`text N`: *String*</span></span>

<span data-ttu-id="bbe30-111">Atsauce uz datu avotu *Virknes* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="bbe30-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="bbe30-112">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="bbe30-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="bbe30-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="bbe30-113">Return values</span></span>

<span data-ttu-id="bbe30-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="bbe30-114">*String*</span></span>

<span data-ttu-id="bbe30-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="bbe30-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="bbe30-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="bbe30-116">Example</span></span>

<span data-ttu-id="bbe30-117">`CONCATENATE ("abc", "def")`atgriež **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="bbe30-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bbe30-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="bbe30-118">Usage notes</span></span>

<span data-ttu-id="bbe30-119">Arī izteiksme `"abc" & "def"` atgriež **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="bbe30-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbe30-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bbe30-120">Additional resources</span></span>

[<span data-ttu-id="bbe30-121">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="bbe30-121">Text functions</span></span>](er-functions-category-text.md)
