---
title: REVERSE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota REVERSE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917239"
---
# <span data-ttu-id="4ddcb-103"><a name="REVERSE">REVERSE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="4ddcb-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ddcb-104">`REVERSE` funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību apgrieztā kārtošanas secībā.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ddcb-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="4ddcb-105">Syntax</span></span>

```
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="4ddcb-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="4ddcb-106">Arguments</span></span>

<span data-ttu-id="4ddcb-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="4ddcb-107">`list`: *Record list*</span></span>

<span data-ttu-id="4ddcb-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ddcb-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="4ddcb-109">Return values</span></span>

<span data-ttu-id="4ddcb-110">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="4ddcb-110">*Record list*</span></span>

<span data-ttu-id="4ddcb-111">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="4ddcb-112">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="4ddcb-112">Example 1</span></span>

<span data-ttu-id="4ddcb-113">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("C|B|A", "|")`, izteiksme `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` atgriež teksta vērtību **C**.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4ddcb-114">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="4ddcb-114">Example 2</span></span>

<span data-ttu-id="4ddcb-115">Ja parametrs **Kreditors** ir konfigurēts kā elektronisko pārskatu (ER) datu avots, kurš atsaucas uz tabulu VendTable, tad izteiksme `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` atgriež sarakstu ar kreditoriem, kuri ir sakārtoti dilstošā secībā pēc nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ddcb-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4ddcb-116">Additional resources</span></span>

[<span data-ttu-id="4ddcb-117">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="4ddcb-117">List functions</span></span>](er-functions-category-list.md)
