---
title: ORDERBY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ORDERBY elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: a6aed53dcad6d402fc2ca61ae0687016cdb3af5b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916204"
---
# <span data-ttu-id="13753-103"><a name="ORDERBY">ORDERBY ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="13753-103"><a name="ORDERBY">ORDERBY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13753-104"> `ORDERBY` funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību pēc tam, kad tas ir sakārtots atbilstoši norādītajiem argumentiem.</span><span class="sxs-lookup"><span data-stu-id="13753-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="13753-105">Šos argumentus var definēt kā izteiksmes.</span><span class="sxs-lookup"><span data-stu-id="13753-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="13753-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="13753-106">Syntax</span></span>

```
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="13753-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="13753-107">Arguments</span></span>

<span data-ttu-id="13753-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="13753-108">`list`: *Record list*</span></span>

<span data-ttu-id="13753-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="13753-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="13753-110">`expression 1`: *Lauks*</span><span class="sxs-lookup"><span data-stu-id="13753-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="13753-111">Derīgs datu avota lauka ceļš, uz kuru ir atsauce izsauktās funkcijas `list` argumentā.</span><span class="sxs-lookup"><span data-stu-id="13753-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="13753-112">Laukam, uz kuru ir atsauce, jābūt primitīva datu tipa laukam.</span><span class="sxs-lookup"><span data-stu-id="13753-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="13753-113">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="13753-113">This argument is required.</span></span>

<span data-ttu-id="13753-114">`expression N`: *Lauks*</span><span class="sxs-lookup"><span data-stu-id="13753-114">`expression N`: *Field*</span></span>

<span data-ttu-id="13753-115">Derīgs datu avota lauka ceļš, uz kuru ir atsauce izsauktās funkcijas `list` argumentā.</span><span class="sxs-lookup"><span data-stu-id="13753-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="13753-116">Laukam, uz kuru ir atsauce, jābūt primitīva datu tipa laukam.</span><span class="sxs-lookup"><span data-stu-id="13753-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="13753-117">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="13753-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="13753-118">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="13753-118">Return values</span></span>

<span data-ttu-id="13753-119">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="13753-119">*Record list*</span></span>

<span data-ttu-id="13753-120">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="13753-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="13753-121">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="13753-121">Example 1</span></span>

<span data-ttu-id="13753-122">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("C|B|A", "|")`, izteiksme `FIRST( ORDERBY( DS, DS. Value)).Value` atgriež teksta vērtību **A**.</span><span class="sxs-lookup"><span data-stu-id="13753-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="13753-123">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="13753-123">Example 2</span></span>

<span data-ttu-id="13753-124">Ja parametrs **Kreditors** ir konfigurēts kā elektronisko pārskatu (ER) datu avots, kurš atsaucas uz tabulu VendTable, tad izteiksme `ORDERBY (Vendors, Vendors.'name()')` atgriež sarakstu ar kreditoriem, kuri ir sakārtoti augošā secībā pēc nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="13753-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13753-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="13753-125">Additional resources</span></span>

[<span data-ttu-id="13753-126">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="13753-126">List functions</span></span>](er-functions-category-list.md)
