---
title: CONCATENATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CONCATENATE elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: f1a47a05127412588f4628cb425eab0379493c3c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746486"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="bc455-103">CONCATENATE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="bc455-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc455-104">`CONCATENATE` funkcija atgriež visas norādītās teksta virknes kā *Virknes* vērtību pēc tam, kad tās ir apvienotas vienā virknē.</span><span class="sxs-lookup"><span data-stu-id="bc455-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc455-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="bc455-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="bc455-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="bc455-106">Arguments</span></span>

<span data-ttu-id="bc455-107">`text 1`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="bc455-107">`text 1`: *String*</span></span>

<span data-ttu-id="bc455-108">Atsauce uz datu avotu *Virknes* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="bc455-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="bc455-109">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="bc455-109">This argument is required.</span></span>

<span data-ttu-id="bc455-110">`text N`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="bc455-110">`text N`: *String*</span></span>

<span data-ttu-id="bc455-111">Atsauce uz datu avotu *Virknes* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="bc455-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="bc455-112">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="bc455-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="bc455-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="bc455-113">Return values</span></span>

<span data-ttu-id="bc455-114">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="bc455-114">*String*</span></span>

<span data-ttu-id="bc455-115">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="bc455-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="bc455-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="bc455-116">Example</span></span>

<span data-ttu-id="bc455-117">`CONCATENATE ("abc", "def")` atgriež **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="bc455-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bc455-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="bc455-118">Usage notes</span></span>

<span data-ttu-id="bc455-119">Arī izteiksme `"abc" & "def"` atgriež **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="bc455-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc455-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bc455-120">Additional resources</span></span>

[<span data-ttu-id="bc455-121">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="bc455-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]