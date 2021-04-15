---
title: CURCREDREF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CURCREDREF elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 65f04e23000e4d2429574db71b18b6907403855e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744347"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="0b300-103">CURCREDREF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="0b300-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b300-104">`CURCREDREF` funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci, pamatojoties uz norādītā rēķina numura cipariem.</span><span class="sxs-lookup"><span data-stu-id="0b300-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b300-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="0b300-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="0b300-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="0b300-106">Arguments</span></span>

<span data-ttu-id="0b300-107">`invoice number digits`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="0b300-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="0b300-108">Teksta vērtība, kas attēlo rēķina numura ciparus.</span><span class="sxs-lookup"><span data-stu-id="0b300-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="0b300-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="0b300-109">Return values</span></span>

<span data-ttu-id="0b300-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="0b300-110">*String*</span></span>

<span data-ttu-id="0b300-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0b300-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0b300-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="0b300-112">Example</span></span>

<span data-ttu-id="0b300-113">`CURCredRef ("VEND-200002")` atgriež **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="0b300-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b300-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0b300-114">Additional resources</span></span>

[<span data-ttu-id="0b300-115">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="0b300-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]