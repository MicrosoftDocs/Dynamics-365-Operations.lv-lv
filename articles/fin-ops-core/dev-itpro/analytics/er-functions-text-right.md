---
title: RIGHT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota RIGHT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 75255eccf4da468b0946253f7570b1621f905cd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570244"
---
# <a name="right-er-function"></a><span data-ttu-id="e52af-103">RIGHT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e52af-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e52af-104">`RIGHT` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes beigām.</span><span class="sxs-lookup"><span data-stu-id="e52af-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e52af-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="e52af-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="e52af-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="e52af-106">Arguments</span></span>

<span data-ttu-id="e52af-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="e52af-107">`text`: *String*</span></span>

<span data-ttu-id="e52af-108">*Virknes* vērtība, kas apzīmē oriģinālo tekstu.</span><span class="sxs-lookup"><span data-stu-id="e52af-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="e52af-109">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="e52af-109">`number`: *Integer*</span></span>

<span data-ttu-id="e52af-110">Rakstzīmju skaits, kas ir jāatgriež no sākotnējā teksta beigām.</span><span class="sxs-lookup"><span data-stu-id="e52af-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="e52af-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="e52af-111">Return values</span></span>

<span data-ttu-id="e52af-112">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e52af-112">*String*</span></span>

<span data-ttu-id="e52af-113">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="e52af-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e52af-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="e52af-114">Example</span></span>

<span data-ttu-id="e52af-115">`RIGHT ("Sample", 3)` atgriež **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="e52af-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e52af-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e52af-116">Additional resources</span></span>

[<span data-ttu-id="e52af-117">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="e52af-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]