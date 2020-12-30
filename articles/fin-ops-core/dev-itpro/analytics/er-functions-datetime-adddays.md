---
title: ADDDAYS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ADDAYS elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: e3d90c19ddc64286843347976c000267e416bf05
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688447"
---
# <a name="adddays-er-function"></a><span data-ttu-id="ee89e-103">ADDDAYS ER funkcija</span><span class="sxs-lookup"><span data-stu-id="ee89e-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee89e-104">`ADDDAYS` funkcija aprēķina *DateTime* vērtību, kas ir norādītais dienu skaits pirms vai pēc norādītā sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="ee89e-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee89e-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="ee89e-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="ee89e-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="ee89e-106">Arguments</span></span>

<span data-ttu-id="ee89e-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="ee89e-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="ee89e-108">Datuma/laika vērtība, kas apzīmē sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="ee89e-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="ee89e-109">`days`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="ee89e-109">`days`: *Integer*</span></span>

<span data-ttu-id="ee89e-110">Dienu skaits pirms vai pēc `datetime`.</span><span class="sxs-lookup"><span data-stu-id="ee89e-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="ee89e-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="ee89e-111">Return values</span></span>

<span data-ttu-id="ee89e-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="ee89e-112">*DateTime*</span></span>

<span data-ttu-id="ee89e-113">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="ee89e-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ee89e-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="ee89e-114">Usage notes</span></span>

<span data-ttu-id="ee89e-115">Pozitīva vērtība `days` norāda uz nākotnes datumu.</span><span class="sxs-lookup"><span data-stu-id="ee89e-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="ee89e-116">Negatīva vērtība norāda uz pagātnes datumu.</span><span class="sxs-lookup"><span data-stu-id="ee89e-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="ee89e-117">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="ee89e-117">Example 1</span></span>

<span data-ttu-id="ee89e-118">`ADDDAYS (NOW(), 7)` atgriež datumu un laiku septiņas dienas uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="ee89e-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="ee89e-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="ee89e-119">Example 2</span></span>

<span data-ttu-id="ee89e-120">`ADDDAYS (NOW(), -3)` atgriež datumu un laiku trīs dienas pagātnē.</span><span class="sxs-lookup"><span data-stu-id="ee89e-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee89e-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ee89e-121">Additional resources</span></span>

[<span data-ttu-id="ee89e-122">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="ee89e-122">Date and time functions</span></span>](er-functions-category-datetime.md)
