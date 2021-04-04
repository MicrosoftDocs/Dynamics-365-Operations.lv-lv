---
title: INDEX ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INDEX elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 88be8f8bdc82bf3eab5c99e72046c794d8fac361
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566929"
---
# <a name="index-er-function"></a><span data-ttu-id="451d0-103">INDEX ER funkcija</span><span class="sxs-lookup"><span data-stu-id="451d0-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="451d0-104">`INDEX` funkcija atgriež *Konteinera (ieraksta)* vērtību, kas ir atlasīta, izmantojot norādītajā sarakstā norādīto skaitlisko indeksu.</span><span class="sxs-lookup"><span data-stu-id="451d0-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="451d0-105">Tiek parādīts izņēmums, ja indekss neietilpst sarakstā esošo ierakstu diapazonā.</span><span class="sxs-lookup"><span data-stu-id="451d0-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="451d0-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="451d0-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="451d0-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="451d0-107">Arguments</span></span>

<span data-ttu-id="451d0-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="451d0-108">`list`: *Record list*</span></span>

<span data-ttu-id="451d0-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="451d0-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="451d0-110">`index`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="451d0-110">`index`: *Integer*</span></span>

<span data-ttu-id="451d0-111">Skaitlisks indekss, kas norāda vajadzīgā ieraksta novietojumu norādītajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="451d0-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="451d0-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="451d0-112">Return values</span></span>

<span data-ttu-id="451d0-113">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="451d0-113">*Container (record)*</span></span>

<span data-ttu-id="451d0-114">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="451d0-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="451d0-115">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="451d0-115">Example 1</span></span>

<span data-ttu-id="451d0-116">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`,izteiksme `DS.Value` atgriež teksta vērtību **"B"** otrajam ierakstam šajā ierakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="451d0-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="451d0-117">Izteiksme `INDEX (SPLIT ("A|B|C", "|"), 2).Value` arī atgriež teksta vērtību **"B"**.</span><span class="sxs-lookup"><span data-stu-id="451d0-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="451d0-118">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="451d0-118">Example 2</span></span>

<span data-ttu-id="451d0-119">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `INDEX (SPLIT ("A|B|C", "|"), 4).Value` izpildlaikā rāda izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="451d0-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="451d0-120">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="451d0-120">Additional resources</span></span>

[<span data-ttu-id="451d0-121">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="451d0-121">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]