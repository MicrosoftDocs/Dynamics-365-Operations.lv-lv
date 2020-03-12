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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040875"
---
# <span data-ttu-id="3c9d7-103"><a name="RIGHT">RIGHT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="3c9d7-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c9d7-104">`RIGHT` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes beigām.</span><span class="sxs-lookup"><span data-stu-id="3c9d7-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c9d7-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="3c9d7-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="3c9d7-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="3c9d7-106">Arguments</span></span>

<span data-ttu-id="3c9d7-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="3c9d7-107">`text`: *String*</span></span>

<span data-ttu-id="3c9d7-108">*Virknes* vērtība, kas apzīmē oriģinālo tekstu.</span><span class="sxs-lookup"><span data-stu-id="3c9d7-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="3c9d7-109">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="3c9d7-109">`number`: *Integer*</span></span>

<span data-ttu-id="3c9d7-110">Rakstzīmju skaits, kas ir jāatgriež no sākotnējā teksta beigām.</span><span class="sxs-lookup"><span data-stu-id="3c9d7-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="3c9d7-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="3c9d7-111">Return values</span></span>

<span data-ttu-id="3c9d7-112">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="3c9d7-112">*String*</span></span>

<span data-ttu-id="3c9d7-113">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="3c9d7-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3c9d7-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="3c9d7-114">Example</span></span>

<span data-ttu-id="3c9d7-115">`RIGHT ("Sample", 3)`atgriež **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="3c9d7-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c9d7-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3c9d7-116">Additional resources</span></span>

[<span data-ttu-id="3c9d7-117">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="3c9d7-117">Text functions</span></span>](er-functions-category-text.md)
