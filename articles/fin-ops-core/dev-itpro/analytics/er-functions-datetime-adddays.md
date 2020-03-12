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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08b9727fb34210fecff31826cc1f2b8da022156b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042462"
---
# <span data-ttu-id="f4c6f-103"><a name="ADDDAYS">ADDDAYS ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="f4c6f-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4c6f-104">`ADDDAYS` funkcija aprēķina *DateTime* vērtību, kas ir norādītais dienu skaits pirms vai pēc norādītā sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="f4c6f-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c6f-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="f4c6f-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="f4c6f-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="f4c6f-106">Arguments</span></span>

<span data-ttu-id="f4c6f-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="f4c6f-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="f4c6f-108">Datuma/laika vērtība, kas apzīmē sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="f4c6f-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="f4c6f-109">`days`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="f4c6f-109">`days`: *Integer*</span></span>

<span data-ttu-id="f4c6f-110">Dienu skaits pirms vai pēc `datetime`.</span><span class="sxs-lookup"><span data-stu-id="f4c6f-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="f4c6f-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="f4c6f-111">Return values</span></span>

<span data-ttu-id="f4c6f-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="f4c6f-112">*DateTime*</span></span>

<span data-ttu-id="f4c6f-113">Iegūtā datuma/laika vērtība.</span><span class="sxs-lookup"><span data-stu-id="f4c6f-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f4c6f-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="f4c6f-114">Usage notes</span></span>

<span data-ttu-id="f4c6f-115">Pozitīva vērtība `days` norāda uz nākotnes datumu.</span><span class="sxs-lookup"><span data-stu-id="f4c6f-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="f4c6f-116">Negatīva vērtība norāda uz pagātnes datumu.</span><span class="sxs-lookup"><span data-stu-id="f4c6f-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="f4c6f-117">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="f4c6f-117">Example 1</span></span>

<span data-ttu-id="f4c6f-118">`ADDDAYS (NOW(), 7)` atgriež datumu un laiku septiņas dienas uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="f4c6f-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="f4c6f-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="f4c6f-119">Example 2</span></span>

<span data-ttu-id="f4c6f-120">`ADDDAYS (NOW(), -3)` atgriež datumu un laiku trīs dienas pagātnē.</span><span class="sxs-lookup"><span data-stu-id="f4c6f-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4c6f-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f4c6f-121">Additional resources</span></span>

[<span data-ttu-id="f4c6f-122">Datuma un laika funkcijas</span><span class="sxs-lookup"><span data-stu-id="f4c6f-122">Date and time functions</span></span>](er-functions-category-datetime.md)
