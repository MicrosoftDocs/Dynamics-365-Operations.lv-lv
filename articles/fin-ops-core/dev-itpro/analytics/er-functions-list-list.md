---
title: LIST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LIST elektroniskā pārskata (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f8e701ec2836206d2299abba5e5b8542b4cf92
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683091"
---
# <a name="list-er-function"></a><span data-ttu-id="e8b48-103">LIST ER funkcija</span><span class="sxs-lookup"><span data-stu-id="e8b48-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8b48-104">`LIST` funkcija atgriež jaunu *Ierakstu saraksta* vērtību, kas sastāv no jauna ierakstu saraksta, kas ir izveidots no norādītiem argumentiem.</span><span class="sxs-lookup"><span data-stu-id="e8b48-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b48-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="e8b48-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="e8b48-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="e8b48-106">Arguments</span></span>

<span data-ttu-id="e8b48-107">`record 1`: *Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="e8b48-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="e8b48-108">Atsauce uz datu avotu *Ieraksta* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="e8b48-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="e8b48-109">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="e8b48-109">This argument is required.</span></span>

<span data-ttu-id="e8b48-110">`record N`: *Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="e8b48-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="e8b48-111">Atsauce uz datu avotu *Ieraksta* datu tipam.</span><span class="sxs-lookup"><span data-stu-id="e8b48-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="e8b48-112">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="e8b48-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="e8b48-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="e8b48-113">Return values</span></span>

<span data-ttu-id="e8b48-114">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="e8b48-114">*Record list*</span></span>

<span data-ttu-id="e8b48-115">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="e8b48-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e8b48-116">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="e8b48-116">Usage notes</span></span>

<span data-ttu-id="e8b48-117">Izveidotā saraksta struktūrā ir tikai tie lauki, kas ir parādīti visu ierakstu struktūrā, kas ir minēti argumentos.</span><span class="sxs-lookup"><span data-stu-id="e8b48-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="e8b48-118">Paraugs</span><span class="sxs-lookup"><span data-stu-id="e8b48-118">Example</span></span>

<span data-ttu-id="e8b48-119">Ievadiet datu avotu **Ieraksts 1** veidam *Konteiners*.</span><span class="sxs-lookup"><span data-stu-id="e8b48-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="e8b48-120">Šis datu avots satur šādus ligzdotus *Aprēķinātā lauka* tipa laukus:</span><span class="sxs-lookup"><span data-stu-id="e8b48-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="e8b48-121">**Kods:** šis lauks satur izteiksmi, kas atgriež *Virknes* tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="e8b48-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="e8b48-122">**Daudzums:** šis lauks satur izteiksmi, kas atgriež *Reālā skaitļa* tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="e8b48-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="e8b48-123">Tad ievadiet datu avotu **Ieraksts 2** veidam *Konteiners*.</span><span class="sxs-lookup"><span data-stu-id="e8b48-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="e8b48-124">Šis datu avots satur šādus ligzdotus *Aprēķinātā lauka* tipa laukus:</span><span class="sxs-lookup"><span data-stu-id="e8b48-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="e8b48-125">**Daudzums:** šis lauks satur izteiksmi, kas atgriež *Reālā skaitļa* tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="e8b48-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="e8b48-126">**IsValid:** šis lauks satur izteiksmi, kas atgriež *Būla* tipa vērtību.</span><span class="sxs-lookup"><span data-stu-id="e8b48-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="e8b48-127">Šajā gadījumā izteiksme `LIST('Record 1', 'Record 2')` atgriež jaunu sarakstu, kurā ir divi ieraksti.</span><span class="sxs-lookup"><span data-stu-id="e8b48-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="e8b48-128">Šī saraksta struktūra sastāv no viena **Daudzuma** lauka tipā *Reāls skaitlis*, jo šis lauks ir vienīgais lauks, kas tiek parādīts katrā izsauktās funkcijas argumentā.</span><span class="sxs-lookup"><span data-stu-id="e8b48-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8b48-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e8b48-129">Additional resources</span></span>

[<span data-ttu-id="e8b48-130">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="e8b48-130">List functions</span></span>](er-functions-category-list.md)
