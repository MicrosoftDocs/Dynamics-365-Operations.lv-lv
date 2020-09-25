---
title: CURCREDREF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CURCREDREF elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 95e90289f43896b83ba98a6edefe0cd6028f4043
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744195"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="c8dc7-103">CURCREDREF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="c8dc7-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8dc7-104">`CURCREDREF` funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci, pamatojoties uz norādītā rēķina numura cipariem.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8dc7-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="c8dc7-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="c8dc7-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="c8dc7-106">Arguments</span></span>

<span data-ttu-id="c8dc7-107">`invoice number digits`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="c8dc7-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="c8dc7-108">Teksta vērtība, kas attēlo rēķina numura ciparus.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="c8dc7-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="c8dc7-109">Return values</span></span>

<span data-ttu-id="c8dc7-110">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="c8dc7-110">*String*</span></span>

<span data-ttu-id="c8dc7-111">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c8dc7-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="c8dc7-112">Example</span></span>

<span data-ttu-id="c8dc7-113">`CURCredRef ("VEND-200002")` atgriež **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="c8dc7-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8dc7-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c8dc7-114">Additional resources</span></span>

[<span data-ttu-id="c8dc7-115">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="c8dc7-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
