---
title: DAYOFYEAR ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DAYOFYEAR elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 569e988db91ff992fb7db6e7fd6e8c6aa6a1a3e8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746919"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="ff40e-103">DAYOFYEAR ER funkcija</span><span class="sxs-lookup"><span data-stu-id="ff40e-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff40e-104">`DAYOFYEAR` funkcija atgriež *Vesela* skaitļa vērtību, kas reprezentē dienu skaitu no 1. janvāra līdz norādītajam datumam.</span><span class="sxs-lookup"><span data-stu-id="ff40e-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff40e-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="ff40e-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="ff40e-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="ff40e-106">Arguments</span></span>

<span data-ttu-id="ff40e-107">`date`: *Datums*</span><span class="sxs-lookup"><span data-stu-id="ff40e-107">`date`: *Date*</span></span>

<span data-ttu-id="ff40e-108">Datuma vērtība, kas apzīmē datumu, kas jāizmanto, aprēķinot dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="ff40e-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="ff40e-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="ff40e-109">Return values</span></span>

<span data-ttu-id="ff40e-110">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="ff40e-110">*Integer*</span></span>

<span data-ttu-id="ff40e-111">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="ff40e-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="ff40e-112">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="ff40e-112">Example 1</span></span>

<span data-ttu-id="ff40e-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` atgriež **61**.</span><span class="sxs-lookup"><span data-stu-id="ff40e-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ff40e-114">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="ff40e-114">Example 2</span></span>

<span data-ttu-id="ff40e-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` atgriež **1**.</span><span class="sxs-lookup"><span data-stu-id="ff40e-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff40e-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ff40e-116">Additional resources</span></span>

[<span data-ttu-id="ff40e-117">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="ff40e-117">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]