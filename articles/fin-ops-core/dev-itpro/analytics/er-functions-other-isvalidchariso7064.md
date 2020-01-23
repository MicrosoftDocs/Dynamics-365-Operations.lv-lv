---
title: ISVALIDCHARACTERISO7064 ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ISVALIDCHARACTERISO7064 elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 6f6f3326c9ca5cdcb3cef52f243d6d3da34251ce
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915928"
---
# <span data-ttu-id="7d7ec-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="7d7ec-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d7ec-104">`ISVALIDCHARACTERISO7064` funkcija atgriež *Būla* vērtību **TRUE**, ja norādītā virkne attēlo derīgu starptautisko bankas konta numuru (IBAN).</span><span class="sxs-lookup"><span data-stu-id="7d7ec-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="7d7ec-105">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7d7ec-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d7ec-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="7d7ec-106">Syntax</span></span>

```
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="7d7ec-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="7d7ec-107">Arguments</span></span>

<span data-ttu-id="7d7ec-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="7d7ec-108">`text`: *String*</span></span>

<span data-ttu-id="7d7ec-109">Teksta vērtība, kas apzīmē IBAN.</span><span class="sxs-lookup"><span data-stu-id="7d7ec-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="7d7ec-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="7d7ec-110">Return values</span></span>

<span data-ttu-id="7d7ec-111">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="7d7ec-111">*String*</span></span>

<span data-ttu-id="7d7ec-112">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="7d7ec-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7d7ec-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="7d7ec-113">Example</span></span>

<span data-ttu-id="7d7ec-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` atgriež **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="7d7ec-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="7d7ec-115">`ISVALIDCHARACTERISO7064 ("AT61")` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="7d7ec-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d7ec-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7d7ec-116">Additional resources</span></span>

[<span data-ttu-id="7d7ec-117">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="7d7ec-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
