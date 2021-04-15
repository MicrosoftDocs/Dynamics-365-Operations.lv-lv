---
title: RIGHT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota RIGHT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746127"
---
# <a name="right-er-function"></a><span data-ttu-id="5e4f2-103">RIGHT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="5e4f2-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e4f2-104">`RIGHT` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes beigām.</span><span class="sxs-lookup"><span data-stu-id="5e4f2-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e4f2-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="5e4f2-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5e4f2-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="5e4f2-106">Arguments</span></span>

<span data-ttu-id="5e4f2-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="5e4f2-107">`text`: *String*</span></span>

<span data-ttu-id="5e4f2-108">*Virknes* vērtība, kas apzīmē oriģinālo tekstu.</span><span class="sxs-lookup"><span data-stu-id="5e4f2-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="5e4f2-109">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="5e4f2-109">`number`: *Integer*</span></span>

<span data-ttu-id="5e4f2-110">Rakstzīmju skaits, kas ir jāatgriež no sākotnējā teksta beigām.</span><span class="sxs-lookup"><span data-stu-id="5e4f2-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5e4f2-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="5e4f2-111">Return values</span></span>

<span data-ttu-id="5e4f2-112">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="5e4f2-112">*String*</span></span>

<span data-ttu-id="5e4f2-113">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="5e4f2-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5e4f2-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="5e4f2-114">Example</span></span>

<span data-ttu-id="5e4f2-115">`RIGHT ("Sample", 3)` atgriež **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="5e4f2-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e4f2-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5e4f2-116">Additional resources</span></span>

[<span data-ttu-id="5e4f2-117">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="5e4f2-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]