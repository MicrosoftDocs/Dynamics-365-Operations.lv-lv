---
title: NOT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NOT elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751722"
---
# <a name="not-er-function"></a><span data-ttu-id="96092-103">NOT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="96092-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96092-104">`NOT` funkcija atgriež norādītā nosacījuma apgriezto loģisko vērtību kā *Būla* vērtību.</span><span class="sxs-lookup"><span data-stu-id="96092-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="96092-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="96092-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="96092-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="96092-106">Arguments</span></span>

<span data-ttu-id="96092-107">`condition`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="96092-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="96092-108">Derīga nosacījuma izteiksme, kas ir jāatsauc.</span><span class="sxs-lookup"><span data-stu-id="96092-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="96092-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="96092-109">Return values</span></span>

<span data-ttu-id="96092-110">*Būla*</span><span class="sxs-lookup"><span data-stu-id="96092-110">*Boolean*</span></span>

<span data-ttu-id="96092-111">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="96092-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="96092-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="96092-112">Example</span></span>

<span data-ttu-id="96092-113">`NOT (TRUE)` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="96092-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96092-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="96092-114">Additional resources</span></span>

[<span data-ttu-id="96092-115">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="96092-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]