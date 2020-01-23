---
title: NOT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NOT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916043"
---
# <span data-ttu-id="adf17-103"><a name="NOT">NOT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="adf17-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adf17-104">`NOT` funkcija atgriež norādītā nosacījuma apgriezto loģisko vērtību kā *Būla* vērtību.</span><span class="sxs-lookup"><span data-stu-id="adf17-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf17-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="adf17-105">Syntax</span></span>

```
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="adf17-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="adf17-106">Arguments</span></span>

<span data-ttu-id="adf17-107">`condition`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="adf17-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="adf17-108">Derīga nosacījuma izteiksme, kas ir jāatsauc.</span><span class="sxs-lookup"><span data-stu-id="adf17-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="adf17-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="adf17-109">Return values</span></span>

<span data-ttu-id="adf17-110">*Būla*</span><span class="sxs-lookup"><span data-stu-id="adf17-110">*Boolean*</span></span>

<span data-ttu-id="adf17-111">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="adf17-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="adf17-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="adf17-112">Example</span></span>

<span data-ttu-id="adf17-113">`NOT (TRUE)` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="adf17-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adf17-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="adf17-114">Additional resources</span></span>

[<span data-ttu-id="adf17-115">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="adf17-115">Logical functions</span></span>](er-functions-category-logical.md)
