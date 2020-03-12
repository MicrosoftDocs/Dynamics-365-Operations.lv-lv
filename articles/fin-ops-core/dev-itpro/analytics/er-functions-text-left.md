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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4293db244d04debf3679cf2bde0b892bd74e8ead
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041128"
---
# <span data-ttu-id="13ba3-103"><a name="LEFT">LEFT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="13ba3-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13ba3-104">`LEFT` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes sākuma.</span><span class="sxs-lookup"><span data-stu-id="13ba3-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ba3-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="13ba3-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="13ba3-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="13ba3-106">Arguments</span></span>

<span data-ttu-id="13ba3-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="13ba3-107">`text`: *String*</span></span>

<span data-ttu-id="13ba3-108">*Virknes* vērtība, kas apzīmē oriģinālo tekstu.</span><span class="sxs-lookup"><span data-stu-id="13ba3-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="13ba3-109">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="13ba3-109">`number`: *Integer*</span></span>

<span data-ttu-id="13ba3-110">Rakstzīmju skaits, kas ir jāatgriež no sākotnējā teksta sākuma.</span><span class="sxs-lookup"><span data-stu-id="13ba3-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="13ba3-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="13ba3-111">Return values</span></span>

<span data-ttu-id="13ba3-112">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="13ba3-112">*String*</span></span>

<span data-ttu-id="13ba3-113">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="13ba3-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="13ba3-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="13ba3-114">Example</span></span>

<span data-ttu-id="13ba3-115">`LEFT ("Sample", 3)`atgriež **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="13ba3-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13ba3-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="13ba3-116">Additional resources</span></span>

[<span data-ttu-id="13ba3-117">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="13ba3-117">Text functions</span></span>](er-functions-category-text.md)
