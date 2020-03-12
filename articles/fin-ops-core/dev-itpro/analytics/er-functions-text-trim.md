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
ms.openlocfilehash: c95663f1aacaf93c1c4bfc8d36d9515f495bf61e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040829"
---
# <span data-ttu-id="58d83-103"><a name="TRIM">TRIM ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="58d83-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58d83-104">`TRIM` funkcija atgriež norādīto teksta virkni kā *Virknes* vērtību, kam ir aprautas sākuma un beigu atstarpes un noņemtas vairākas atstarpes starp vārdiem.</span><span class="sxs-lookup"><span data-stu-id="58d83-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d83-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="58d83-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="58d83-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="58d83-106">Arguments</span></span>

<span data-ttu-id="58d83-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="58d83-107">`text`: *String*</span></span>

<span data-ttu-id="58d83-108">*Virknes* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="58d83-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="58d83-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="58d83-109">Return values</span></span>

<span data-ttu-id="58d83-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="58d83-110">*String*</span></span>

<span data-ttu-id="58d83-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="58d83-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="58d83-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="58d83-112">Example</span></span>

<span data-ttu-id="58d83-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` atgriež **"Sample text"**.</span><span class="sxs-lookup"><span data-stu-id="58d83-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58d83-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="58d83-114">Additional resources</span></span>

[<span data-ttu-id="58d83-115">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="58d83-115">Text functions</span></span>](er-functions-category-text.md)
