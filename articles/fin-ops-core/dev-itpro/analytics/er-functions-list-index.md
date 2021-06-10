---
title: INDEX ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INDEX elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087755"
---
# <a name="index-er-function"></a><span data-ttu-id="a64a8-103">INDEX ER funkcija</span><span class="sxs-lookup"><span data-stu-id="a64a8-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a64a8-104">`INDEX` funkcija atgriež *Konteinera (ieraksta)* vērtību, kas ir atlasīta, izmantojot norādītajā sarakstā norādīto skaitlisko indeksu.</span><span class="sxs-lookup"><span data-stu-id="a64a8-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="a64a8-105">Tiek parādīts izņēmums, ja indekss neietilpst sarakstā esošo ierakstu diapazonā.</span><span class="sxs-lookup"><span data-stu-id="a64a8-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64a8-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="a64a8-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="a64a8-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="a64a8-107">Arguments</span></span>

<span data-ttu-id="a64a8-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="a64a8-108">`list`: *Record list*</span></span>

<span data-ttu-id="a64a8-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="a64a8-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a64a8-110">`index`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="a64a8-110">`index`: *Integer*</span></span>

<span data-ttu-id="a64a8-111">Skaitlisks indekss, kas norāda vajadzīgā ieraksta novietojumu norādītajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="a64a8-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="a64a8-112">Tā kā šai funkcijai tiek izmantota vienreizējā numerācija, norādiet vērtību **1**, lai atgrieztu pirmo norādītā saraksta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a64a8-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="a64a8-113">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="a64a8-113">Return values</span></span>

<span data-ttu-id="a64a8-114">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="a64a8-114">*Container (record)*</span></span>

<span data-ttu-id="a64a8-115">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="a64a8-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a64a8-116">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="a64a8-116">Example 1</span></span>

<span data-ttu-id="a64a8-117">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`,izteiksme `DS.Value` atgriež teksta vērtību **"B"** otrajam ierakstam šajā ierakstu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="a64a8-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="a64a8-118">Izteiksme `INDEX (SPLIT ("A|B|C", "|"), 2).Value` arī atgriež teksta vērtību **"B"**.</span><span class="sxs-lookup"><span data-stu-id="a64a8-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a64a8-119">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="a64a8-119">Example 2</span></span>

<span data-ttu-id="a64a8-120">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `INDEX (SPLIT ("A|B|C", "|"), 4).Value` izpildlaikā rāda izņēmumu.</span><span class="sxs-lookup"><span data-stu-id="a64a8-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a64a8-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a64a8-121">Additional resources</span></span>

[<span data-ttu-id="a64a8-122">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="a64a8-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
