---
title: ORDERBY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ORDERBY elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a995713a795b3f24a4fcfadcc4be596e932a22c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564170"
---
# <a name="orderby-er-function"></a><span data-ttu-id="fdb37-103">ORDERBY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="fdb37-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdb37-104">Funkcija `ORDERBY` atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību pēc tam, kad tas ir sakārtots atbilstoši norādītajiem argumentiem.</span><span class="sxs-lookup"><span data-stu-id="fdb37-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="fdb37-105">Šos argumentus var definēt kā izteiksmes.</span><span class="sxs-lookup"><span data-stu-id="fdb37-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdb37-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="fdb37-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="fdb37-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="fdb37-107">Arguments</span></span>

<span data-ttu-id="fdb37-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="fdb37-108">`list`: *Record list*</span></span>

<span data-ttu-id="fdb37-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="fdb37-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="fdb37-110">`expression 1`: *Lauks*</span><span class="sxs-lookup"><span data-stu-id="fdb37-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="fdb37-111">Derīgs datu avota lauka ceļš, uz kuru ir atsauce izsauktās funkcijas `list` argumentā.</span><span class="sxs-lookup"><span data-stu-id="fdb37-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="fdb37-112">Laukam, uz kuru ir atsauce, jābūt primitīva datu tipa laukam.</span><span class="sxs-lookup"><span data-stu-id="fdb37-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="fdb37-113">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="fdb37-113">This argument is required.</span></span>

<span data-ttu-id="fdb37-114">`expression N`: *Lauks*</span><span class="sxs-lookup"><span data-stu-id="fdb37-114">`expression N`: *Field*</span></span>

<span data-ttu-id="fdb37-115">Derīgs datu avota lauka ceļš, uz kuru ir atsauce izsauktās funkcijas `list` argumentā.</span><span class="sxs-lookup"><span data-stu-id="fdb37-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="fdb37-116">Laukam, uz kuru ir atsauce, jābūt primitīva datu tipa laukam.</span><span class="sxs-lookup"><span data-stu-id="fdb37-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="fdb37-117">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="fdb37-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="fdb37-118">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="fdb37-118">Return values</span></span>

<span data-ttu-id="fdb37-119">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="fdb37-119">*Record list*</span></span>

<span data-ttu-id="fdb37-120">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="fdb37-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="fdb37-121">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="fdb37-121">Example 1</span></span>

<span data-ttu-id="fdb37-122">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("C|B|A", "|")`, izteiksme `FIRST( ORDERBY( DS, DS. Value)).Value` atgriež teksta vērtību **A**.</span><span class="sxs-lookup"><span data-stu-id="fdb37-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="fdb37-123">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="fdb37-123">Example 2</span></span>

<span data-ttu-id="fdb37-124">Ja parametrs **Kreditors** ir konfigurēts kā elektronisko pārskatu (ER) datu avots, kurš atsaucas uz tabulu VendTable, tad izteiksme `ORDERBY (Vendors, Vendors.'name()')` atgriež sarakstu ar kreditoriem, kuri ir sakārtoti augošā secībā pēc nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="fdb37-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdb37-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fdb37-125">Additional resources</span></span>

[<span data-ttu-id="fdb37-126">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="fdb37-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]