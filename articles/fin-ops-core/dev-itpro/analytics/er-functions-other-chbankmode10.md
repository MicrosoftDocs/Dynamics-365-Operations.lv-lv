---
title: CH_BANK_MOD_10 funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CH_BANK_MOD_10 elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: bca82cd596ba1e3ec42b3dba91ee6c4871ff8601
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686862"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="7b0da-103">CH_BANK_MOD_10 funkcija</span><span class="sxs-lookup"><span data-stu-id="7b0da-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b0da-104">`CH_BANK_MOD_10` funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci kā MOD10 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem.</span><span class="sxs-lookup"><span data-stu-id="7b0da-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0da-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="7b0da-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="7b0da-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="7b0da-106">Arguments</span></span>

<span data-ttu-id="7b0da-107">`invoice number digits`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="7b0da-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="7b0da-108">Teksta vērtība, kas attēlo rēķina numura ciparus.</span><span class="sxs-lookup"><span data-stu-id="7b0da-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="7b0da-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="7b0da-109">Return values</span></span>

<span data-ttu-id="7b0da-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="7b0da-110">*String*</span></span>

<span data-ttu-id="7b0da-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="7b0da-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="7b0da-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="7b0da-112">Example</span></span>

<span data-ttu-id="7b0da-113">`CH_BANK_MOD_10 ("VEND-200002")` atgriež **3**.</span><span class="sxs-lookup"><span data-stu-id="7b0da-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b0da-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7b0da-114">Additional resources</span></span>

[<span data-ttu-id="7b0da-115">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="7b0da-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
