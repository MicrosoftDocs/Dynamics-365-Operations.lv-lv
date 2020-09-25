---
title: DAYOFYEAR ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DAYOFYEAR elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 755f5f1de28f95ed682648caf47155ad71c8f4b0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745493"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="9c4b1-103">DAYOFYEAR ER funkcija</span><span class="sxs-lookup"><span data-stu-id="9c4b1-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c4b1-104">`DAYOFYEAR` funkcija atgriež *Vesela* skaitļa vērtību, kas reprezentē dienu skaitu no 1. janvāra līdz norādītajam datumam.</span><span class="sxs-lookup"><span data-stu-id="9c4b1-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c4b1-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="9c4b1-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="9c4b1-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="9c4b1-106">Arguments</span></span>

<span data-ttu-id="9c4b1-107">`date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="9c4b1-107">`date`: *Date*</span></span>

<span data-ttu-id="9c4b1-108">Datuma vērtība, kas apzīmē datumu, kas jāizmanto, aprēķinot dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="9c4b1-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c4b1-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="9c4b1-109">Return values</span></span>

<span data-ttu-id="9c4b1-110">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="9c4b1-110">*Integer*</span></span>

<span data-ttu-id="9c4b1-111">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="9c4b1-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="9c4b1-112">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="9c4b1-112">Example 1</span></span>

<span data-ttu-id="9c4b1-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` atgriež **61**.</span><span class="sxs-lookup"><span data-stu-id="9c4b1-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9c4b1-114">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="9c4b1-114">Example 2</span></span>

<span data-ttu-id="9c4b1-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` atgriež **1**.</span><span class="sxs-lookup"><span data-stu-id="9c4b1-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c4b1-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9c4b1-116">Additional resources</span></span>

[<span data-ttu-id="9c4b1-117">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="9c4b1-117">Date and time functions</span></span>](er-functions-category-datetime.md)
