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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c18a7f96096fbc6bbc7b6d15135c11bd70960d26
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744474"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="d4390-103">CH_BANK_MOD_10 funkcija</span><span class="sxs-lookup"><span data-stu-id="d4390-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4390-104">`CH_BANK_MOD_10` funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci kā MOD10 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem.</span><span class="sxs-lookup"><span data-stu-id="d4390-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4390-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="d4390-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="d4390-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d4390-106">Arguments</span></span>

<span data-ttu-id="d4390-107">`invoice number digits`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d4390-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="d4390-108">Teksta vērtība, kas attēlo rēķina numura ciparus.</span><span class="sxs-lookup"><span data-stu-id="d4390-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="d4390-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d4390-109">Return values</span></span>

<span data-ttu-id="d4390-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="d4390-110">*String*</span></span>

<span data-ttu-id="d4390-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="d4390-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d4390-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="d4390-112">Example</span></span>

<span data-ttu-id="d4390-113">`CH_BANK_MOD_10 ("VEND-200002")` atgriež **3**.</span><span class="sxs-lookup"><span data-stu-id="d4390-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4390-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d4390-114">Additional resources</span></span>

[<span data-ttu-id="d4390-115">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="d4390-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
