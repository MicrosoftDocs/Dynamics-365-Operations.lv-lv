---
title: INDEX ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INDEX elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745182"
---
# <a name="index-er-function"></a><span data-ttu-id="775a7-103">INDEX ER funkcija</span><span class="sxs-lookup"><span data-stu-id="775a7-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="775a7-104">`INDEX` funkcija atgriež *Konteinera (ieraksta)* vērtību, kas ir atlasīta, izmantojot norādītajā sarakstā norādīto skaitlisko indeksu.</span><span class="sxs-lookup"><span data-stu-id="775a7-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="775a7-105">Tiek parādīts izņēmums, ja indekss neietilpst sarakstā esošo ierakstu diapazonā.</span><span class="sxs-lookup"><span data-stu-id="775a7-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="775a7-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="775a7-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="775a7-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="775a7-107">Arguments</span></span>

<span data-ttu-id="775a7-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="775a7-108">`list`: *Record list*</span></span>

<span data-ttu-id="775a7-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="775a7-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="775a7-110">`index`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="775a7-110">`index`: *Integer*</span></span>

<span data-ttu-id="775a7-111">Skaitlisks indekss, kas norāda vajadzīgā ieraksta novietojumu norādītajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="775a7-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="775a7-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="775a7-112">Return values</span></span>

<span data-ttu-id="775a7-113">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="775a7-113">*Container (record)*</span></span>

<span data-ttu-id="775a7-114">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="775a7-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="775a7-115">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="775a7-115">Example 1</span></span>

<span data-ttu-id="775a7-116">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`,izteiksme `DS.Value` atgriež teksta vērtību **"B"** otrajam ierakstam šajā ierakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="775a7-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="775a7-117">Izteiksme `INDEX (SPLIT ("A|B|C", "|"), 2).Value` arī atgriež teksta vērtību **"B"**.</span><span class="sxs-lookup"><span data-stu-id="775a7-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="775a7-118">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="775a7-118">Example 2</span></span>

<span data-ttu-id="775a7-119">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `INDEX (SPLIT ("A|B|C", "|"), 4).Value` izpildlaikā rāda izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="775a7-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="775a7-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="775a7-120">Additional resources</span></span>

[<span data-ttu-id="775a7-121">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="775a7-121">List functions</span></span>](er-functions-category-list.md)
