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
ms.openlocfilehash: 035bf720a892e987ff9fc073ab8ed6f6cc6ea18e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745109"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="82dc2-103">LISTJOIN ER funkcija</span><span class="sxs-lookup"><span data-stu-id="82dc2-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82dc2-104">`LISTJOIN` funkcija atgriež *Ierakstu saraksta* vērtību, kas pārstāv jaunu savienotu ierakstu sarakstu, kas ir izveidots no norādītiem argumentiem.</span><span class="sxs-lookup"><span data-stu-id="82dc2-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="82dc2-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="82dc2-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="82dc2-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="82dc2-106">Arguments</span></span>

<span data-ttu-id="82dc2-107">`list 1`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="82dc2-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="82dc2-108">Atsauce uz datu avotu *Ieraksta saraksta* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="82dc2-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="82dc2-109">Šis ir obligāts arguments.</span><span class="sxs-lookup"><span data-stu-id="82dc2-109">This argument is mandatory.</span></span>

<span data-ttu-id="82dc2-110">`list N`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="82dc2-110">`list N`: *Record list*</span></span>

<span data-ttu-id="82dc2-111">Atsauce uz datu avotu *Ieraksta saraksta* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="82dc2-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="82dc2-112">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="82dc2-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="82dc2-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="82dc2-113">Return values</span></span>

<span data-ttu-id="82dc2-114">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="82dc2-114">*Record list*</span></span>

<span data-ttu-id="82dc2-115">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="82dc2-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="82dc2-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="82dc2-116">Usage notes</span></span>

<span data-ttu-id="82dc2-117">Izveidotā saraksta struktūrā ir tikai tie lauki, kas ir parādīti visu ierakstu saraksta struktūrā, kas ir minēti argumentos.</span><span class="sxs-lookup"><span data-stu-id="82dc2-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="82dc2-118">Paraugs</span><span class="sxs-lookup"><span data-stu-id="82dc2-118">Example</span></span>

<span data-ttu-id="82dc2-119">Ievadiet datu avotu **Ieraksts 1** veidam `Container`.</span><span class="sxs-lookup"><span data-stu-id="82dc2-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="82dc2-120">Šis datu avots satur šādus ligzdotus `Calculated field` tipa laukus:</span><span class="sxs-lookup"><span data-stu-id="82dc2-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="82dc2-121">**Kods**: šis lauks satur izteiksmi, kas atgriež `String` tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="82dc2-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="82dc2-122">**Daudzums**: šis lauks satur izteiksmi, kas atgriež `Real` tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="82dc2-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="82dc2-123">Tad ievadiet datu avotu **Ieraksts 2** veidam `Container`.</span><span class="sxs-lookup"><span data-stu-id="82dc2-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="82dc2-124">Šis datu avots satur šādus ligzdotus `Calculated field` tipa laukus:</span><span class="sxs-lookup"><span data-stu-id="82dc2-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="82dc2-125">**Daudzums**: šis lauks satur izteiksmi, kas atgriež `Real` tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="82dc2-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="82dc2-126">**IsValid**: šis lauks satur izteiksmi, kas atgriež `Boolean` tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="82dc2-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER modeļa kartēšanas noformētāja lapa](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="82dc2-128">Šajā gadījumā izteiksme `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` atgriež jaunu sarakstu, kurā ir divi ieraksti.</span><span class="sxs-lookup"><span data-stu-id="82dc2-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![ER modeļa kartēšanas veidotāja lapa ar diviem ierakstiem](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="82dc2-130">Šī saraksta struktūra sastāv no viena **Daudzuma** lauka tipā `Real`, jo šis lauks ir vienīgais lauks, kas tiek parādīts katrā izsauktās funkcijas argumentā.</span><span class="sxs-lookup"><span data-stu-id="82dc2-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![ER modeļa kartēšanas veidotāja lapas summas lauks](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="82dc2-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="82dc2-132">Additional resources</span></span>

[<span data-ttu-id="82dc2-133">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="82dc2-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="82dc2-134">Atkļūdot izpildītā ER formāta datu avotus, lai analizētu datu plūsmu un transformāciju</span><span class="sxs-lookup"><span data-stu-id="82dc2-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
