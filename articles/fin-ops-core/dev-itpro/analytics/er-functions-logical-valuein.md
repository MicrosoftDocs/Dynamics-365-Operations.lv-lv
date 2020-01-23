---
title: VALUEIN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota VALUEIN elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915974"
---
# <span data-ttu-id="065d9-103"><a name="VALUEIN">VALUEIN ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="065d9-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="065d9-104">`VALUEIN` funkcija nosaka, vai norādītā ievade atbilst kāda norādītā saraksta norādītā elementa vērtībai.</span><span class="sxs-lookup"><span data-stu-id="065d9-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="065d9-105">Tas atgriež *Būla* vērtību **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes palaišanas rezultātam vismaz vienam norādītā saraksta ierakstam.</span><span class="sxs-lookup"><span data-stu-id="065d9-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="065d9-106">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="065d9-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="065d9-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="065d9-107">Syntax</span></span>

```
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="065d9-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="065d9-108">Arguments</span></span>

<span data-ttu-id="065d9-109">`input`: *Lauks*</span><span class="sxs-lookup"><span data-stu-id="065d9-109">`input`: *Field*</span></span>

<span data-ttu-id="065d9-110">*Ierakstu saraksta* tipa datu avota vienuma derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="065d9-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="065d9-111">Šī elementa vērtībai tiks noteikta atbilstība.</span><span class="sxs-lookup"><span data-stu-id="065d9-111">The value of this item will be matched.</span></span>

<span data-ttu-id="065d9-112">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="065d9-112">`list`: *Record list*</span></span>

<span data-ttu-id="065d9-113">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="065d9-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="065d9-114">`list item expression`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="065d9-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="065d9-115">Derīga nosacījuma izteiksme apzīmē izteiksmi, kas norāda uz vai satur vienu norādītā saraksta lauku, kurš ir jāizmanto atbilstības noteikšanai.</span><span class="sxs-lookup"><span data-stu-id="065d9-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="065d9-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="065d9-116">Return values</span></span>

<span data-ttu-id="065d9-117">*Būla*</span><span class="sxs-lookup"><span data-stu-id="065d9-117">*Boolean*</span></span>

<span data-ttu-id="065d9-118">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="065d9-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="065d9-119">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="065d9-119">Usage notes</span></span>

<span data-ttu-id="065d9-120">Parasti funkcija `VALUEIN` tiek tulkota uz **OR** nosacījumu kopu.</span><span class="sxs-lookup"><span data-stu-id="065d9-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="065d9-121">Dažos gadījumos to var pārtulkot uz datu bāzes SQL paziņojumu, izmantojot `EXISTS JOIN` operatoru.</span><span class="sxs-lookup"><span data-stu-id="065d9-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="065d9-122">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="065d9-122">Example 1</span></span>

<span data-ttu-id="065d9-123">Savā modeļa kartējumā jūs definējat  datu avotu: **Saraksts** ar tipu*Aprēķinātais lauks* .</span><span class="sxs-lookup"><span data-stu-id="065d9-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="065d9-124">Šajā datu avotā ir izteiksme `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="065d9-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="065d9-125">Ja tiek izsaukts datu avots, ja tas ir konfigurēts kā `VALUEIN ("B", List, List.Value)` izteiksme, tas atgriež **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="065d9-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="065d9-126">Šajā gadījumā `VALUEIN` funkcija tiek tulkota uz šādu nosacījumu kopu: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="065d9-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="065d9-127">Ja tiek izsaukts datu avots, ja tas ir konfigurēts kā `VALUEIN ("B", List, LEFT(List.Value, 0))` izteiksme, tas atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="065d9-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="065d9-128">Šajā gadījumā `VALUEIN` funkcija tiek tulkota uz šādu nosacījumu: `("B" = "")`, kas nav vienāds ar **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="065d9-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="065d9-129">Šāda nosacījuma tekstā rakstzīmju skaita augšējā robežvērtība ir 32 768 rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="065d9-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="065d9-130">Tādēļ nevajadzētu veidot datu avotus, kas izpildlaikā varētu pārsniegt šo ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="065d9-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="065d9-131">Ja ierobežojums tiek pārsniegts, programmas darbība tiek pārtraukta un tiek parādīts izņēmums.</span><span class="sxs-lookup"><span data-stu-id="065d9-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="065d9-132">Piemēram, šāda situācija var rasties, ja datu avots ir konfigurēts kā `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` un sarakstā **List1** un **List2** ir daudz ierakstu.</span><span class="sxs-lookup"><span data-stu-id="065d9-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="065d9-133">Noteiktos gadījumos funkcija `VALUEIN` tiek tulkota uz datu bāzes priekšrakstu, izmantojot operatoru `EXISTS JOIN`.</span><span class="sxs-lookup"><span data-stu-id="065d9-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="065d9-134">Šāda uzvedība it spēkā, kad tiek izmantota funkcija [FILTER](er-functions-list-filter.md) un tiek ievēroti šādi nosacījumi:</span><span class="sxs-lookup"><span data-stu-id="065d9-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="065d9-135">Opcija **ASK FOR QUERY** ir izslēgta funkcijas `VALUEIN` datu avotam tādai funkcijai, kas atsaucas uz ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="065d9-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="065d9-136">Šim datu avotam izpildlaikā netiks lietoti nekādi papildu nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="065d9-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="065d9-137">Funkcijas `VALUEIN` datu avotam tādai funkcijai, kas atsaucas uz ierakstu sarakstu, nav konfigurētas ligzdotās izteiksmes.</span><span class="sxs-lookup"><span data-stu-id="065d9-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="065d9-138">Funkcijas `VALUEIN` saraksta elements atsaucas uz kādu norādītā datu avota lauku, nevis izteiksmi vai metodi.</span><span class="sxs-lookup"><span data-stu-id="065d9-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="065d9-139">Apsveriet iespēju izmantot šo opciju, nevis funkciju [WHERE](er-functions-list-where.md), kā iepriekš aprakstīts šajā piemērā.</span><span class="sxs-lookup"><span data-stu-id="065d9-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="065d9-140">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="065d9-140">Example 2</span></span>

<span data-ttu-id="065d9-141">Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.</span><span class="sxs-lookup"><span data-stu-id="065d9-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="065d9-142">**Tabulas ierakstu** veida datu avots *In*.</span><span class="sxs-lookup"><span data-stu-id="065d9-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="065d9-143">Šis datu avots attiecas uz Intrastat tabulu.</span><span class="sxs-lookup"><span data-stu-id="065d9-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="065d9-144">**Tabulas ierakstu** veida datu avots *Port*.</span><span class="sxs-lookup"><span data-stu-id="065d9-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="065d9-145">Šis datu avots attiecas uz IntrastatPort tabulu.</span><span class="sxs-lookup"><span data-stu-id="065d9-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="065d9-146">Kad tiek izsaukts datu avots, kas ir konfigurēts kā izteiksme `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, tiek ģenerēts šāds SQL priekšraksts, lai atgrieztu filtrētos ierakstus Intrastat tabulā.</span><span class="sxs-lookup"><span data-stu-id="065d9-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="065d9-147">Laukiem **dataAreaId** gala SQL priekšraksts tiek ģenerēts, izmantojot operatoru `IN`.</span><span class="sxs-lookup"><span data-stu-id="065d9-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="065d9-148">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="065d9-148">Example 3</span></span>

<span data-ttu-id="065d9-149">Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.</span><span class="sxs-lookup"><span data-stu-id="065d9-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="065d9-150">**Aprēķinātā lauka** veida datu avots *Le*.</span><span class="sxs-lookup"><span data-stu-id="065d9-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="065d9-151">Šajā datu avotā ir izteiksme `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="065d9-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="065d9-152">**Tabulas ierakstu** veida datu avots *In*.</span><span class="sxs-lookup"><span data-stu-id="065d9-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="065d9-153">Šis datu avots attiecas uz Intrastat tabulu, un tam ir ieslēgta opcija **Starpuzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="065d9-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="065d9-154">Kad tiek izsaukts datu avots, kas ir konfigurēts kā izteiksme `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, gala SQL priekšrakstā ir šāds nosacījums:</span><span class="sxs-lookup"><span data-stu-id="065d9-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="065d9-155">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="065d9-155">Additional resources</span></span>

[<span data-ttu-id="065d9-156">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="065d9-156">Logical functions</span></span>](er-functions-category-logical.md)
