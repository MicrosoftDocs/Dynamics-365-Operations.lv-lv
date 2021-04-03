---
title: ISVALIDCHARACTERISO7064 ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ISVALIDCHARACTERISO7064 elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 26300adce5f9a8a567510885577c6cfb9b1c859a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563370"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="e5cda-103">ISVALIDCHARACTERISO7064 ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e5cda-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5cda-104">`ISVALIDCHARACTERISO7064` funkcija atgriež *Būla* vērtību **TRUE**, ja norādītā virkne attēlo derīgu starptautisko bankas konta numuru (IBAN).</span><span class="sxs-lookup"><span data-stu-id="e5cda-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="e5cda-105">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e5cda-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5cda-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="e5cda-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="e5cda-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="e5cda-107">Arguments</span></span>

<span data-ttu-id="e5cda-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5cda-108">`text`: *String*</span></span>

<span data-ttu-id="e5cda-109">Teksta vērtība, kas apzīmē IBAN.</span><span class="sxs-lookup"><span data-stu-id="e5cda-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="e5cda-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="e5cda-110">Return values</span></span>

<span data-ttu-id="e5cda-111">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="e5cda-111">*String*</span></span>

<span data-ttu-id="e5cda-112">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="e5cda-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e5cda-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="e5cda-113">Example</span></span>

<span data-ttu-id="e5cda-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` atgriež **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="e5cda-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="e5cda-115">`ISVALIDCHARACTERISO7064 ("AT61")` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e5cda-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5cda-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e5cda-116">Additional resources</span></span>

[<span data-ttu-id="e5cda-117">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="e5cda-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]