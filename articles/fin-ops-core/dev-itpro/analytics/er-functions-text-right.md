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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682946"
---
# <a name="right-er-function"></a><span data-ttu-id="0925b-103">RIGHT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="0925b-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0925b-104">`RIGHT` funkcija atgriež *Virknes* vērtību, kas norāda norādītu zīmju skaitu no norādītās virknes beigām.</span><span class="sxs-lookup"><span data-stu-id="0925b-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0925b-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="0925b-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="0925b-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="0925b-106">Arguments</span></span>

<span data-ttu-id="0925b-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="0925b-107">`text`: *String*</span></span>

<span data-ttu-id="0925b-108">*Virknes* vērtība, kas apzīmē oriģinālo tekstu.</span><span class="sxs-lookup"><span data-stu-id="0925b-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="0925b-109">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="0925b-109">`number`: *Integer*</span></span>

<span data-ttu-id="0925b-110">Rakstzīmju skaits, kas ir jāatgriež no sākotnējā teksta beigām.</span><span class="sxs-lookup"><span data-stu-id="0925b-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="0925b-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="0925b-111">Return values</span></span>

<span data-ttu-id="0925b-112">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="0925b-112">*String*</span></span>

<span data-ttu-id="0925b-113">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0925b-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0925b-114">Paraugs</span><span class="sxs-lookup"><span data-stu-id="0925b-114">Example</span></span>

<span data-ttu-id="0925b-115">`RIGHT ("Sample", 3)` atgriež **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="0925b-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0925b-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0925b-116">Additional resources</span></span>

[<span data-ttu-id="0925b-117">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="0925b-117">Text functions</span></span>](er-functions-category-text.md)
