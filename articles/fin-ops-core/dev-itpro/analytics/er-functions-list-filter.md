---
title: FILTER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FILTER elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: d281fe710381b0ecb075a0d9281d46bd6edf987d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745301"
---
# <a name="filter-er-function"></a><span data-ttu-id="d91a3-103">FILTER ER funkcija</span><span class="sxs-lookup"><span data-stu-id="d91a3-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d91a3-104">`FILTER` funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību, kad vaicājums ir mainīts tā, ka tas filtrē norādīto nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="d91a3-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="d91a3-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="d91a3-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="d91a3-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d91a3-106">Arguments</span></span>

<span data-ttu-id="d91a3-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="d91a3-107">`list`: *Record list*</span></span>

<span data-ttu-id="d91a3-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="d91a3-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d91a3-109">`condition`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="d91a3-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="d91a3-110">Derīga nosacījuma izteiksme, ko izmanto, lai filtrētu norādītā saraksta ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d91a3-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="d91a3-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d91a3-111">Return values</span></span>

<span data-ttu-id="d91a3-112">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="d91a3-112">*Record list*</span></span>

<span data-ttu-id="d91a3-113">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="d91a3-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d91a3-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="d91a3-114">Usage notes</span></span>

<span data-ttu-id="d91a3-115">Šī funkcija atšķiras no funkcijas [WHERE](er-functions-list-where.md), jo norādītais nosacījums tiek lietots datu bāzes līmenī visiem elektronisko pārskatu (ER) datu avotiem ar tipu *Tabulas ieraksti*.</span><span class="sxs-lookup"><span data-stu-id="d91a3-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="d91a3-116">Sarakstu un nosacījumu var definēt, izmantojot tabulas un relācijas.</span><span class="sxs-lookup"><span data-stu-id="d91a3-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="d91a3-117">Ja viens vai abi argumenti, kas ir konfigurēts šai funkcijai (`list` un `condition`) neļauj šo pieprasījumu tulkot uz tiešo SQL zvanu, noformēšanas laikā tiek rādīts izņēmums.</span><span class="sxs-lookup"><span data-stu-id="d91a3-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="d91a3-118">Šis izņēmums informē lietotāju, ka `list` vai `condition` nevar izmantot vaicājuma veikšanai datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="d91a3-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="d91a3-119">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="d91a3-119">Example 1</span></span>

<span data-ttu-id="d91a3-120">Ja parametrs **Kreditors** ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, izteiksme `FILTER (Vendors, Vendors.VendGroup = "40")` atgriež tikai kreditoru grupā 40 ietverto kreditoru sarakstu.</span><span class="sxs-lookup"><span data-stu-id="d91a3-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="d91a3-121">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="d91a3-121">Example 2</span></span>

<span data-ttu-id="d91a3-122">Ja parametrs **Kreditors** ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, un ja parametrs **parmVendorBankGroup** ir konfigurēts kā ER datu avots, kurš atgriež vērtību ar datu tipu *Virkne*, izteiksme `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` atgriež sarakstu, kurā ir tikai to kreditoru konti, kas pieder noteiktai banku grupai.</span><span class="sxs-lookup"><span data-stu-id="d91a3-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="d91a3-123">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="d91a3-123">Example 3</span></span>

<span data-ttu-id="d91a3-124">Ievadāt datu avotu **DS** no veida *Aprēķinātais lauks*, un tas satur izteiksmi `SPLIT ("A,B,C", ",")`</span><span class="sxs-lookup"><span data-stu-id="d91a3-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="d91a3-125">Pēc tam ievadāt citu izteiksmi, `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="d91a3-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="d91a3-126">Mēģinot saglabāt šo izteiksmi ER formulas noformētājā, tiek rādīts šāds izņēmums: "Validācijas kļūda: FILTER funkcijas izteiksmju sarakstam nevar veikt vaicājumus."</span><span class="sxs-lookup"><span data-stu-id="d91a3-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d91a3-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d91a3-127">Additional resources</span></span>

[<span data-ttu-id="d91a3-128">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="d91a3-128">List functions</span></span>](er-functions-category-list.md)
