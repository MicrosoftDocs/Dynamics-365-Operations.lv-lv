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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680666"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="63e39-103">ISVALIDCHARACTERISO7064 ER funkcija</span><span class="sxs-lookup"><span data-stu-id="63e39-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63e39-104">`ISVALIDCHARACTERISO7064` funkcija atgriež *Būla* vērtību **TRUE**, ja norādītā virkne attēlo derīgu starptautisko bankas konta numuru (IBAN).</span><span class="sxs-lookup"><span data-stu-id="63e39-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="63e39-105">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="63e39-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e39-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="63e39-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="63e39-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="63e39-107">Arguments</span></span>

<span data-ttu-id="63e39-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="63e39-108">`text`: *String*</span></span>

<span data-ttu-id="63e39-109">Teksta vērtība, kas apzīmē IBAN.</span><span class="sxs-lookup"><span data-stu-id="63e39-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="63e39-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="63e39-110">Return values</span></span>

<span data-ttu-id="63e39-111">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="63e39-111">*String*</span></span>

<span data-ttu-id="63e39-112">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="63e39-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="63e39-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="63e39-113">Example</span></span>

<span data-ttu-id="63e39-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` atgriež **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="63e39-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="63e39-115">`ISVALIDCHARACTERISO7064 ("AT61")` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="63e39-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63e39-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="63e39-116">Additional resources</span></span>

[<span data-ttu-id="63e39-117">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="63e39-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
