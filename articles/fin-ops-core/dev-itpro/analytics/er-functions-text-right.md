---
title: RIGHT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota RIGHT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916733"
---
# <span data-ttu-id="9b5a5-103"><a name="RIGHT">RIGHT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="9b5a5-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b5a5-104">`RIGHT` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes beigām.</span><span class="sxs-lookup"><span data-stu-id="9b5a5-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b5a5-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="9b5a5-105">Syntax</span></span>

```
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="9b5a5-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="9b5a5-106">Arguments</span></span>

<span data-ttu-id="9b5a5-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="9b5a5-107">`text`: *String*</span></span>

<span data-ttu-id="9b5a5-108">*Virknes* vērtība, kas apzīmē oriģinālo tekstu.</span><span class="sxs-lookup"><span data-stu-id="9b5a5-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="9b5a5-109">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="9b5a5-109">`number`: *Integer*</span></span>

<span data-ttu-id="9b5a5-110">Rakstzīmju skaits, kas ir jāatgriež no sākotnējā teksta beigām.</span><span class="sxs-lookup"><span data-stu-id="9b5a5-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="9b5a5-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="9b5a5-111">Return values</span></span>

<span data-ttu-id="9b5a5-112">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="9b5a5-112">*String*</span></span>

<span data-ttu-id="9b5a5-113">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="9b5a5-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9b5a5-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="9b5a5-114">Example</span></span>

<span data-ttu-id="9b5a5-115">`RIGHT ("Sample", 3)`atgriež **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="9b5a5-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b5a5-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9b5a5-116">Additional resources</span></span>

[<span data-ttu-id="9b5a5-117">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="9b5a5-117">Text functions</span></span>](er-functions-category-text.md)
