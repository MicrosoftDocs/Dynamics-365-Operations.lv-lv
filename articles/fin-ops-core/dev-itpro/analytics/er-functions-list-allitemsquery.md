---
title: ALLITEMSQUERY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ALLITEMSQUERY elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 647019a103006c8b74bc26885c51f5372dcf0c42
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917515"
---
# <span data-ttu-id="6ee87-103"><a name="ALLITEMSQUERY">ALLITEMSQUERY ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="6ee87-103"><a name="ALLITEMSQUERY">ALLITEMSQUERY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ee87-104">`ALLITEMSQUERY` funkcija darbojas kā apvienots SQL vaicājums.</span><span class="sxs-lookup"><span data-stu-id="6ee87-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="6ee87-105">Tā atgriež jaunu izplātu *Ierakstu saraksta* vērtību, kas sastāv no ierakstu saraksta, kas apzīmē visus vienumus, kuri atbilst norādītajam ceļam.</span><span class="sxs-lookup"><span data-stu-id="6ee87-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee87-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="6ee87-106">Syntax</span></span>

```
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="6ee87-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="6ee87-107">Arguments</span></span>

<span data-ttu-id="6ee87-108">`path`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="6ee87-108">`path`: *Record list*</span></span>

<span data-ttu-id="6ee87-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="6ee87-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="6ee87-110">Tam jāsatur vismaz viena relācija.</span><span class="sxs-lookup"><span data-stu-id="6ee87-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ee87-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="6ee87-111">Return values</span></span>

<span data-ttu-id="6ee87-112">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="6ee87-112">*Record list*</span></span>

<span data-ttu-id="6ee87-113">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="6ee87-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6ee87-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="6ee87-114">Usage notes</span></span>

<span data-ttu-id="6ee87-115">Norādītais ceļš ir jādefinē kā derīgs datu avota ceļš datu avota elementam ar *Ierakstu saraksta* datu tipu.</span><span class="sxs-lookup"><span data-stu-id="6ee87-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="6ee87-116">Tam arī jāsatur vismaz viena relācija.</span><span class="sxs-lookup"><span data-stu-id="6ee87-116">It must also contain at least one relation.</span></span> <span data-ttu-id="6ee87-117">Tādiem datu elementiem kā *Virkne* un *Datums* elektronisko pārskatu (ER) izteiksmju veidotājā veidošanas laikā ir jāizraisa kļūda.</span><span class="sxs-lookup"><span data-stu-id="6ee87-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="6ee87-118">Ja šī funkcija tiek lietota datu tipa *Ierakstu saraksta* datu avotiem, kas attiecas uz programmas objektu, kuru var tieši izsaukt, izmantojot SQL (piemēram, tabulu, entītiju vai vaicājumu), tā darbojas kā savienots SQL vaicājums.</span><span class="sxs-lookup"><span data-stu-id="6ee87-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="6ee87-119">Pretējā gadījumā tas darbojas atmiņā kā [ALLITEMS](er-functions-list-allitems.md) funkcija.</span><span class="sxs-lookup"><span data-stu-id="6ee87-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="6ee87-120">Paraugs</span><span class="sxs-lookup"><span data-stu-id="6ee87-120">Example</span></span>

<span data-ttu-id="6ee87-121">Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.</span><span class="sxs-lookup"><span data-stu-id="6ee87-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="6ee87-122">**CustInv** datu avots no veida *Tabulas ieraksti*, kas atsaucas uz tabulu CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="6ee87-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="6ee87-123">Datu avots **Filteredinv** no veida *Aprēķinātais lauks*, kas satur izteiksmi `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="6ee87-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="6ee87-124">Datu avots **JourLines** no veida *Aprēķinātais lauks*, kas satur izteiksmi `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="6ee87-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="6ee87-125">Kad palaižat modeļa kartēšanu, lai izsauktu datu avotu **JourLines**, tiek izpildīts tālāk norādītais SQL priekšraksts.</span><span class="sxs-lookup"><span data-stu-id="6ee87-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="6ee87-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6ee87-126">Additional resources</span></span>

[<span data-ttu-id="6ee87-127">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="6ee87-127">List functions</span></span>](er-functions-category-list.md)
