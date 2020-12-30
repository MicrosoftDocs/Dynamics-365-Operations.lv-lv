---
title: LEFT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LEFT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685887"
---
# <a name="left-er-function"></a><span data-ttu-id="9687e-103">LEFT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="9687e-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9687e-104">`LEFT` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes sākuma.</span><span class="sxs-lookup"><span data-stu-id="9687e-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9687e-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="9687e-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="9687e-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="9687e-106">Arguments</span></span>

<span data-ttu-id="9687e-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="9687e-107">`text`: *String*</span></span>

<span data-ttu-id="9687e-108">*Virknes* vērtība, kas apzīmē oriģinālo tekstu.</span><span class="sxs-lookup"><span data-stu-id="9687e-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="9687e-109">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="9687e-109">`number`: *Integer*</span></span>

<span data-ttu-id="9687e-110">Rakstzīmju skaits, kas ir jāatgriež no sākotnējā teksta sākuma.</span><span class="sxs-lookup"><span data-stu-id="9687e-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="9687e-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="9687e-111">Return values</span></span>

<span data-ttu-id="9687e-112">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="9687e-112">*String*</span></span>

<span data-ttu-id="9687e-113">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="9687e-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9687e-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="9687e-114">Example</span></span>

<span data-ttu-id="9687e-115">`LEFT ("Sample", 3)` atgriež **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="9687e-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9687e-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9687e-116">Additional resources</span></span>

[<span data-ttu-id="9687e-117">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="9687e-117">Text functions</span></span>](er-functions-category-text.md)
