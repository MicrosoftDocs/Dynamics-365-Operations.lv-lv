---
title: LEN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LEN elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: fce4b5311d84364310b76545a775f1cc8db2fd70
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569972"
---
# <a name="len-er-function"></a><span data-ttu-id="fb346-103">LEN ER funkcija</span><span class="sxs-lookup"><span data-stu-id="fb346-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb346-104">`LEN` funkcija atgriež *Vesela skaitļa* vērtību, kas norāda norādītu zīmju skaitu norādītajā virknē.</span><span class="sxs-lookup"><span data-stu-id="fb346-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb346-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="fb346-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="fb346-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="fb346-106">Arguments</span></span>

<span data-ttu-id="fb346-107">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="fb346-107">`text`: *String*</span></span>

<span data-ttu-id="fb346-108">*Virknes* vērtība, kas konkretizē tekstu.</span><span class="sxs-lookup"><span data-stu-id="fb346-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="fb346-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="fb346-109">Return values</span></span>

<span data-ttu-id="fb346-110">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="fb346-110">*Integer*</span></span>

<span data-ttu-id="fb346-111">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="fb346-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="fb346-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="fb346-112">Example</span></span>

<span data-ttu-id="fb346-113">`LEN ("Sample")` atgriež **6**.</span><span class="sxs-lookup"><span data-stu-id="fb346-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb346-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fb346-114">Additional resources</span></span>

[<span data-ttu-id="fb346-115">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="fb346-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]