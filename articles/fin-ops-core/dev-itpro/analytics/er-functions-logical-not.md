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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041726"
---
# <span data-ttu-id="cb69c-103"><a name="NOT">NOT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="cb69c-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb69c-104">`NOT` funkcija atgriež norādītā nosacījuma apgriezto loģisko vērtību kā *Būla* vērtību.</span><span class="sxs-lookup"><span data-stu-id="cb69c-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb69c-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="cb69c-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="cb69c-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="cb69c-106">Arguments</span></span>

<span data-ttu-id="cb69c-107">`condition`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="cb69c-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="cb69c-108">Derīga nosacījuma izteiksme, kas ir jāatsauc.</span><span class="sxs-lookup"><span data-stu-id="cb69c-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb69c-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="cb69c-109">Return values</span></span>

<span data-ttu-id="cb69c-110">*Būla*</span><span class="sxs-lookup"><span data-stu-id="cb69c-110">*Boolean*</span></span>

<span data-ttu-id="cb69c-111">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="cb69c-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="cb69c-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="cb69c-112">Example</span></span>

<span data-ttu-id="cb69c-113">`NOT (TRUE)` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="cb69c-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb69c-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cb69c-114">Additional resources</span></span>

[<span data-ttu-id="cb69c-115">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="cb69c-115">Logical functions</span></span>](er-functions-category-logical.md)
