---
title: NOT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NOT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b55b3d8930ece7e2f2925579821ca88749801f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565884"
---
# <a name="not-er-function"></a><span data-ttu-id="48c5c-103">NOT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="48c5c-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48c5c-104">`NOT` funkcija atgriež norādītā nosacījuma apgriezto loģisko vērtību kā *Būla* vērtību.</span><span class="sxs-lookup"><span data-stu-id="48c5c-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c5c-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="48c5c-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="48c5c-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="48c5c-106">Arguments</span></span>

<span data-ttu-id="48c5c-107">`condition`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="48c5c-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="48c5c-108">Derīga nosacījuma izteiksme, kas ir jāatsauc.</span><span class="sxs-lookup"><span data-stu-id="48c5c-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="48c5c-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="48c5c-109">Return values</span></span>

<span data-ttu-id="48c5c-110">*Būla*</span><span class="sxs-lookup"><span data-stu-id="48c5c-110">*Boolean*</span></span>

<span data-ttu-id="48c5c-111">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="48c5c-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="48c5c-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="48c5c-112">Example</span></span>

<span data-ttu-id="48c5c-113">`NOT (TRUE)` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="48c5c-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48c5c-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="48c5c-114">Additional resources</span></span>

[<span data-ttu-id="48c5c-115">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="48c5c-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]