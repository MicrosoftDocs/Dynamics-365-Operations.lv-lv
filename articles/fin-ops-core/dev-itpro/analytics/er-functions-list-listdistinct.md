---
title: LISTDISTINCT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LISTDISTINCT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: f20565d73cea8d0cc1361bd03cda86a79a97955e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563828"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="f7e35-103">LISTDISTINCT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="f7e35-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f7e35-104">`LISTDISTINCT` funkcija aprēķina norādīto izteiksmi kā atlasītāju katram norādītā saraksta ierakstam.</span><span class="sxs-lookup"><span data-stu-id="f7e35-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="f7e35-105">Tiek atgriezta jauna *Ierakstu saraksta* vērtība, kurā ir viens ieraksts katrai unikālajai atlasītāja vērtībai.</span><span class="sxs-lookup"><span data-stu-id="f7e35-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e35-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="f7e35-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="f7e35-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="f7e35-107">Arguments</span></span>

<span data-ttu-id="f7e35-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="f7e35-108">`list`: *Record list*</span></span>

<span data-ttu-id="f7e35-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="f7e35-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f7e35-110">`selector`: *Primitīvu datu tips*</span><span class="sxs-lookup"><span data-stu-id="f7e35-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="f7e35-111">Derīga izteiksme, ko izmanto, lai aprēķinātu atlasītāja vērtību katram ierakstam norādītajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f7e35-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="f7e35-112">Šim parametram tiek atbalstīti šādi datu tipi:</span><span class="sxs-lookup"><span data-stu-id="f7e35-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="f7e35-113">Būla</span><span class="sxs-lookup"><span data-stu-id="f7e35-113">Boolean</span></span>
- <span data-ttu-id="f7e35-114">Datums</span><span class="sxs-lookup"><span data-stu-id="f7e35-114">Date</span></span>
- <span data-ttu-id="f7e35-115">Datums un laiks</span><span class="sxs-lookup"><span data-stu-id="f7e35-115">DateTime</span></span>
- <span data-ttu-id="f7e35-116">GUID</span><span class="sxs-lookup"><span data-stu-id="f7e35-116">GUID</span></span>
- <span data-ttu-id="f7e35-117">Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="f7e35-117">Integer</span></span>
- <span data-ttu-id="f7e35-118">Int64</span><span class="sxs-lookup"><span data-stu-id="f7e35-118">Int64</span></span>
- <span data-ttu-id="f7e35-119">Reāls</span><span class="sxs-lookup"><span data-stu-id="f7e35-119">Real</span></span>
- <span data-ttu-id="f7e35-120">Virkne</span><span class="sxs-lookup"><span data-stu-id="f7e35-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="f7e35-121">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="f7e35-121">Return values</span></span>

<span data-ttu-id="f7e35-122">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="f7e35-122">*Record list*</span></span>

<span data-ttu-id="f7e35-123">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="f7e35-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f7e35-124">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="f7e35-124">Usage notes</span></span>

<span data-ttu-id="f7e35-125">Izveidotā saraksta struktūra atbilst norādītā saraksta struktūrai.</span><span class="sxs-lookup"><span data-stu-id="f7e35-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="f7e35-126">Norādītajam sarakstam var tikt aprēķināta vienāda atlasītāja vērtība vairākiem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="f7e35-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="f7e35-127">Šajā gadījumā atbilstošā ieraksta lauka vērtības izveidotajā sarakstā ir vienādas ar vērtību pirmajam ierakstam no norādītā saraksta, kam tiek aprēķināta atlasītāja vērtība.</span><span class="sxs-lookup"><span data-stu-id="f7e35-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="f7e35-128">Šīs funkcijas izpilde tiek veikta jebkurā atmiņā esošā *Ierakstu saraksta* tipa [Elektroniskā pārskata (ER)](general-electronic-reporting.md) datu avota.</span><span class="sxs-lookup"><span data-stu-id="f7e35-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="f7e35-129">**GROUPBY** datu avotu var arī izmantot, lai ģenerētu to ierakstu sarakstu, kuriem tiek aprēķināts atlasītājs, kuram ir noteiktas vērtības.</span><span class="sxs-lookup"><span data-stu-id="f7e35-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="f7e35-130">Tomēr no veiktspējas un atmiņas patēriņa perspektīvas ir labāk izmantot `LISTDISTINCT` funkciju nekā **GROUPBY** datu avotu, jo funkcijas izpilde tiek veikta atmiņā.</span><span class="sxs-lookup"><span data-stu-id="f7e35-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="f7e35-131">Paraugs</span><span class="sxs-lookup"><span data-stu-id="f7e35-131">Example</span></span>

<span data-ttu-id="f7e35-132">Sekojošais piemērs parāda, kā var iegūt unikālo debitoru kontu numuru sarakstu, kas ir izsniegts vismaz vienam pārdošanas vai projekta rēķinam noteiktā periodā.</span><span class="sxs-lookup"><span data-stu-id="f7e35-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="f7e35-133">Ievadiet **SalesInvoice** datu avotu `Record list` tipam, kas attiecas uz **CustInvoiceJour** pieteikumu tabulu un filtrē rēķinus par noteiktiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="f7e35-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="f7e35-134">Šī datu avota `InvoiceAccount` lauks atgriež rēķinā iekļauta debitora konta numuru.</span><span class="sxs-lookup"><span data-stu-id="f7e35-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="f7e35-135">Ievadiet **ProjectInvoice** datu avotu `Record list` tipam, kas attiecas uz **ProjInvoiceJour** pieteikumu tabulu un filtrē projektu rēķinus par noteiktiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="f7e35-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="f7e35-136">Šī datu avota `InvoiceAccount` lauks atgriež rēķinā iekļauta debitora konta numuru.</span><span class="sxs-lookup"><span data-stu-id="f7e35-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="f7e35-137">Konfigurējiet `Calculated field` tipa **AllInvoices** datu avotu, kas satur izteiksmi `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="f7e35-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="f7e35-138">Šajā datu avotā tiek atgriezts pārdošanas rēķinu un projekta rēķinu apvienotais saraksts.</span><span class="sxs-lookup"><span data-stu-id="f7e35-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="f7e35-139">Konfigurējiet `Record list` tipa **InvoicedCustomer** datu avotu, kas satur izteiksmi `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="f7e35-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="f7e35-140">Šis datu avots atgriež jaunu sarakstu, kurā ir viens ieraksts katram unikālam debitoram, kuram noteiktajā periodā ir izrakstīts rēķins.</span><span class="sxs-lookup"><span data-stu-id="f7e35-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="f7e35-141">Šī saraksta `InvoiceAccount` lauks satur debitora konta numuru.</span><span class="sxs-lookup"><span data-stu-id="f7e35-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7e35-142">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f7e35-142">Additional resources</span></span>

[<span data-ttu-id="f7e35-143">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="f7e35-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]