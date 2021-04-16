---
title: CH_BANK_MOD_10 funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CH_BANK_MOD_10 elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 92750ca7e7396077d8c56c3b336f495c228dddce
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744419"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="4be61-103">CH_BANK_MOD_10 funkcija</span><span class="sxs-lookup"><span data-stu-id="4be61-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4be61-104">`CH_BANK_MOD_10` funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci kā MOD10 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem.</span><span class="sxs-lookup"><span data-stu-id="4be61-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="4be61-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="4be61-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="4be61-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="4be61-106">Arguments</span></span>

<span data-ttu-id="4be61-107">`invoice number digits`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="4be61-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="4be61-108">Teksta vērtība, kas attēlo rēķina numura ciparus.</span><span class="sxs-lookup"><span data-stu-id="4be61-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="4be61-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="4be61-109">Return values</span></span>

<span data-ttu-id="4be61-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="4be61-110">*String*</span></span>

<span data-ttu-id="4be61-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="4be61-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4be61-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="4be61-112">Example</span></span>

<span data-ttu-id="4be61-113">`CH_BANK_MOD_10 ("VEND-200002")` atgriež **3**.</span><span class="sxs-lookup"><span data-stu-id="4be61-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4be61-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4be61-114">Additional resources</span></span>

[<span data-ttu-id="4be61-115">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="4be61-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]