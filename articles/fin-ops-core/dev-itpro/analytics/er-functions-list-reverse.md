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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 895d5f13f065b2188f245d081fa69e7e63555dde
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686444"
---
# <a name="reverse-er-function"></a><span data-ttu-id="82a8d-103">REVERSE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="82a8d-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82a8d-104">`REVERSE` funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību apgrieztā kārtošanas secībā.</span><span class="sxs-lookup"><span data-stu-id="82a8d-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a8d-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="82a8d-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="82a8d-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="82a8d-106">Arguments</span></span>

<span data-ttu-id="82a8d-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="82a8d-107">`list`: *Record list*</span></span>

<span data-ttu-id="82a8d-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="82a8d-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="82a8d-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="82a8d-109">Return values</span></span>

<span data-ttu-id="82a8d-110">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="82a8d-110">*Record list*</span></span>

<span data-ttu-id="82a8d-111">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="82a8d-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="82a8d-112">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="82a8d-112">Example 1</span></span>

<span data-ttu-id="82a8d-113">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("C|B|A", "|")`, izteiksme `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` atgriež teksta vērtību **C**.</span><span class="sxs-lookup"><span data-stu-id="82a8d-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="82a8d-114">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="82a8d-114">Example 2</span></span>

<span data-ttu-id="82a8d-115">Ja parametrs **Kreditors** ir konfigurēts kā elektronisko pārskatu (ER) datu avots, kurš atsaucas uz tabulu VendTable, tad izteiksme `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` atgriež sarakstu ar kreditoriem, kuri ir sakārtoti dilstošā secībā pēc nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="82a8d-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82a8d-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="82a8d-116">Additional resources</span></span>

[<span data-ttu-id="82a8d-117">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="82a8d-117">List functions</span></span>](er-functions-category-list.md)
