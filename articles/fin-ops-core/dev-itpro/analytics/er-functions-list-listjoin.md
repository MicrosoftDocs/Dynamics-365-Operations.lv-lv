---
title: LISTJOIN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LISTJOIN elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249039"
---
# <a name=""></a><span data-ttu-id="6bda0-103"><a name="LISTJOIN">LISTJOIN ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="6bda0-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bda0-104">`LISTJOIN` funkcija atgriež *Ierakstu saraksta* vērtību, kas pārstāv jaunu savienotu ierakstu sarakstu, kas ir izveidots no norādītiem argumentiem.</span><span class="sxs-lookup"><span data-stu-id="6bda0-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bda0-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="6bda0-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="6bda0-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="6bda0-106">Arguments</span></span>

<span data-ttu-id="6bda0-107">`list 1`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="6bda0-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="6bda0-108">Atsauce uz datu avotu *Ieraksta saraksta* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="6bda0-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="6bda0-109">Šis ir obligāts arguments.</span><span class="sxs-lookup"><span data-stu-id="6bda0-109">This argument is mandatory.</span></span>

<span data-ttu-id="6bda0-110">`list N`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="6bda0-110">`list N`: *Record list*</span></span>

<span data-ttu-id="6bda0-111">Atsauce uz datu avotu *Ieraksta saraksta* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="6bda0-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="6bda0-112">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="6bda0-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="6bda0-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="6bda0-113">Return values</span></span>

<span data-ttu-id="6bda0-114">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="6bda0-114">*Record list*</span></span>

<span data-ttu-id="6bda0-115">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="6bda0-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6bda0-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="6bda0-116">Usage notes</span></span>

<span data-ttu-id="6bda0-117">Izveidotā saraksta struktūrā ir tikai tie lauki, kas ir parādīti visu ierakstu saraksta struktūrā, kas ir minēti argumentos.</span><span class="sxs-lookup"><span data-stu-id="6bda0-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="6bda0-118">Paraugs</span><span class="sxs-lookup"><span data-stu-id="6bda0-118">Example</span></span>

<span data-ttu-id="6bda0-119">Ievadiet datu avotu **Ieraksts 1** veidam `Container`.</span><span class="sxs-lookup"><span data-stu-id="6bda0-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="6bda0-120">Šis datu avots satur šādus ligzdotus `Calculated field` tipa laukus:</span><span class="sxs-lookup"><span data-stu-id="6bda0-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="6bda0-121">**Kods**: šis lauks satur izteiksmi, kas atgriež `String` tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="6bda0-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="6bda0-122">**Daudzums**: šis lauks satur izteiksmi, kas atgriež `Real` tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="6bda0-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="6bda0-123">Tad ievadiet datu avotu **Ieraksts 2** veidam `Container`.</span><span class="sxs-lookup"><span data-stu-id="6bda0-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="6bda0-124">Šis datu avots satur šādus ligzdotus `Calculated field` tipa laukus:</span><span class="sxs-lookup"><span data-stu-id="6bda0-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="6bda0-125">**Daudzums**: šis lauks satur izteiksmi, kas atgriež `Real` tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="6bda0-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="6bda0-126">**IsValid**: šis lauks satur izteiksmi, kas atgriež `Boolean` tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="6bda0-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="6bda0-127">Šajā gadījumā izteiksme `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` atgriež jaunu sarakstu, kurā ir divi ieraksti.</span><span class="sxs-lookup"><span data-stu-id="6bda0-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="6bda0-128">Šī saraksta struktūra sastāv no viena **Daudzuma** lauka tipā `Real`, jo šis lauks ir vienīgais lauks, kas tiek parādīts katrā izsauktās funkcijas argumentā.</span><span class="sxs-lookup"><span data-stu-id="6bda0-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6bda0-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6bda0-129">Additional resources</span></span>

[<span data-ttu-id="6bda0-130">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="6bda0-130">List functions</span></span>](er-functions-category-list.md)
