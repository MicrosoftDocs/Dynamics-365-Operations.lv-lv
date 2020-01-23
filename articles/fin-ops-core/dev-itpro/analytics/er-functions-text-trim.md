---
title: TRIM ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TRIM elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2673b0167f7602a6d6eaa79be639905028e99822
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915537"
---
# <span data-ttu-id="d94cd-103"><a name="TRIM">TRIM ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="d94cd-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d94cd-104">`TRIM` funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, kam ir aprautas sākuma un beigu atstarpes un noņemtas vairākas atstarpes starp vārdiem.</span><span class="sxs-lookup"><span data-stu-id="d94cd-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d94cd-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="d94cd-105">Syntax</span></span>

```
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="d94cd-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d94cd-106">Arguments</span></span>

<span data-ttu-id="d94cd-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d94cd-107">`text`: *String*</span></span>

<span data-ttu-id="d94cd-108">*Virknes* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="d94cd-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d94cd-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d94cd-109">Return values</span></span>

<span data-ttu-id="d94cd-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="d94cd-110">*String*</span></span>

<span data-ttu-id="d94cd-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="d94cd-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d94cd-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="d94cd-112">Example</span></span>

<span data-ttu-id="d94cd-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` atgriež **"Sample text"**.</span><span class="sxs-lookup"><span data-stu-id="d94cd-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d94cd-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d94cd-114">Additional resources</span></span>

[<span data-ttu-id="d94cd-115">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="d94cd-115">Text functions</span></span>](er-functions-category-text.md)
