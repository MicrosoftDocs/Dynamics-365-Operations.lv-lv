---
title: VALUEINLARGE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota VALUEINLARGE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705147"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="f9623-103">VALUEINLARGE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="f9623-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9623-104">`VALUEINLARGE` funkcija nosaka, vai norādītā *Int64* vai *Integer* tipa ievade atbilst kāda norādītā saraksta norādītā elementa vērtībai.</span><span class="sxs-lookup"><span data-stu-id="f9623-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="f9623-105">Šī funkcija atgriež *Būla* vērtību **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes palaišanas rezultātam vismaz vienam norādītā saraksta ierakstam.</span><span class="sxs-lookup"><span data-stu-id="f9623-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="f9623-106">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f9623-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="f9623-107">Lai saprastu atšķirību ar `VALUEIN` funkciju, skatiet šīs tēmas [Lietojuma piezīme](#usage_note) sadaļu.</span><span class="sxs-lookup"><span data-stu-id="f9623-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9623-108">Sintakse</span><span class="sxs-lookup"><span data-stu-id="f9623-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="f9623-109">Argumenti</span><span class="sxs-lookup"><span data-stu-id="f9623-109">Arguments</span></span>

<span data-ttu-id="f9623-110">`input`: *Lauks*</span><span class="sxs-lookup"><span data-stu-id="f9623-110">`input`: *Field*</span></span>

<span data-ttu-id="f9623-111">*Ierakstu saraksta* tipa datu avota vienības tipa derīgais ceļš.</span><span class="sxs-lookup"><span data-stu-id="f9623-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="f9623-112">Šī elementa vērtībai tiks noteikta atbilstība.</span><span class="sxs-lookup"><span data-stu-id="f9623-112">The value of this item will be matched.</span></span>

<span data-ttu-id="f9623-113">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="f9623-113">`list`: *Record list*</span></span>

<span data-ttu-id="f9623-114">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="f9623-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f9623-115">`list item expression`: *Izteiksme*</span><span class="sxs-lookup"><span data-stu-id="f9623-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="f9623-116">Derīga nosacījuma izteiksme apzīmē izteiksmi, kas norāda uz vai satur vienu norādītā saraksta lauku, kurš ir jāizmanto atbilstības noteikšanai.</span><span class="sxs-lookup"><span data-stu-id="f9623-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9623-117">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="f9623-117">Return values</span></span>

<span data-ttu-id="f9623-118">*Būla*</span><span class="sxs-lookup"><span data-stu-id="f9623-118">*Boolean*</span></span>

<span data-ttu-id="f9623-119">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="f9623-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="f9623-120"><a name="usage_note">Lietošanas piezīmes</a></span><span class="sxs-lookup"><span data-stu-id="f9623-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="f9623-121">Kad norādītā ievade attēlo *Int64* vai *Integer* datu avota krājuma tipu, izsaukums, kas ir iztulkojams tiešam SQL pārskatam, norādītais saraksts tiek pārveidots uz pagaidu SQL tabulu un salīdzināšana tiek veikta datu bāzē, izpildot vienu `EXISTS JOIN` vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="f9623-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="f9623-122">Pretējā gadījumā šī funkcija darbojas kā [`VALUEIN`](er-functions-logical-valuein.md) funkcija.</span><span class="sxs-lookup"><span data-stu-id="f9623-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="f9623-123">Kad norādītā ievade attēlo datu avota vienumu, kas ir izveidots kā krājums, kas nav *Int64* un *Integer*, kļūda rodas noformēšanas laikā, informējot, ka `VALUEINLARGE` funkcija nav piemērojama konfigurētai ER izteiksmei.</span><span class="sxs-lookup"><span data-stu-id="f9623-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="f9623-124">Kad `VALUEINLARGE` funkcijas izteiksme tiek izpildīta un tiek izmantota vairāk nekā viena pagaidu tabula šīs izpildes jomā, rodas izpildlaika kļūda.</span><span class="sxs-lookup"><span data-stu-id="f9623-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="f9623-125">Paraugs</span><span class="sxs-lookup"><span data-stu-id="f9623-125">Example</span></span>

<span data-ttu-id="f9623-126">Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.</span><span class="sxs-lookup"><span data-stu-id="f9623-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="f9623-127">**Tabulas ierakstu** veida datu avots *In*.</span><span class="sxs-lookup"><span data-stu-id="f9623-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="f9623-128">Šis datu avots attiecas uz **Intrastat** tabulu.</span><span class="sxs-lookup"><span data-stu-id="f9623-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="f9623-129">**Starpuzņēmumu** opcija ir iestatīta uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="f9623-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="f9623-130">**Aprēķinātā lauka** veida datu avots *InMemory*.</span><span class="sxs-lookup"><span data-stu-id="f9623-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="f9623-131">Šajā datu avotā ir izteiksme `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="f9623-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="f9623-132">**Aprēķinātā lauka** veida datu avots *InFiltered*.</span><span class="sxs-lookup"><span data-stu-id="f9623-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="f9623-133">Šajā datu avotā ir izteiksme `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="f9623-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="f9623-134">Ja datu avots **InFiltered** tiek izsaukts uzņēmuma **DEMF** kontekstā, programmas datu bāzē tiek izveidota jauna pagaidu tabula, šajā tabulā tiek ievietoti uzkrātie atmiņas ierakstu identifikācijas kodi, un tiek ģenerēts šāds SQL izraksts, lai atgrieztu filtrētus ierakstus **Intrastat** tabulā.</span><span class="sxs-lookup"><span data-stu-id="f9623-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="f9623-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f9623-135">Additional resources</span></span>

[<span data-ttu-id="f9623-136">Loģiskās funkcijas</span><span class="sxs-lookup"><span data-stu-id="f9623-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="f9623-137">VALUEIN funkcijas</span><span class="sxs-lookup"><span data-stu-id="f9623-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)
