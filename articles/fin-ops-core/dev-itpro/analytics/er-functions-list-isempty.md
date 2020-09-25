---
title: ISEMPTY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ISEMPTY elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5b6fde7cbadec7aae052742ef598e1af4dbae793
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745133"
---
# <a name="isempty-er-function"></a><span data-ttu-id="4ba43-103">ISEMPTY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="4ba43-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ba43-104">`ISEMPTY` funkcija atgriež *Būla* vērtību **TRUE**, ja norādītajā sarakstā nav ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4ba43-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="4ba43-105">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4ba43-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba43-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="4ba43-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="4ba43-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="4ba43-107">Arguments</span></span>

<span data-ttu-id="4ba43-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="4ba43-108">`list`: *Record list*</span></span>

<span data-ttu-id="4ba43-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="4ba43-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ba43-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="4ba43-110">Return values</span></span>

<span data-ttu-id="4ba43-111">*Būla*</span><span class="sxs-lookup"><span data-stu-id="4ba43-111">*Boolean*</span></span>

<span data-ttu-id="4ba43-112">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="4ba43-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="4ba43-113">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="4ba43-113">Example 1</span></span>

<span data-ttu-id="4ba43-114">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `ISEMPTY(DS)` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4ba43-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4ba43-115">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="4ba43-115">Example 2</span></span>

<span data-ttu-id="4ba43-116">Izteiksme `ISEMPTY (SPLIT ("",1))` atgriež **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="4ba43-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ba43-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4ba43-117">Additional resources</span></span>

[<span data-ttu-id="4ba43-118">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="4ba43-118">List functions</span></span>](er-functions-category-list.md)
