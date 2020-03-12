---
title: STRINGJOIN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota STRINGJOIN elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 10a98e98d913b0b4fe36690f7effd5d8d9a3faf4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041795"
---
# <span data-ttu-id="8bebc-103"><a name="STRINGJOIN">STRINGJOIN ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="8bebc-103"><a name="STRINGJOIN">STRINGJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bebc-104">`STRINGJOIN` funkcija atgriež *Virknes* vērtību, kas sastāv no norādītā saraksta norādītā lauka savirknētajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="8bebc-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="8bebc-105">Vērtības var atdalīt ar norādīto norobežotāju.</span><span class="sxs-lookup"><span data-stu-id="8bebc-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bebc-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="8bebc-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="8bebc-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="8bebc-107">Arguments</span></span>

<span data-ttu-id="8bebc-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="8bebc-108">`list`: *Record list*</span></span>

<span data-ttu-id="8bebc-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="8bebc-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="8bebc-110">`field`: *Lauks*</span><span class="sxs-lookup"><span data-stu-id="8bebc-110">`field`: *Field*</span></span>

<span data-ttu-id="8bebc-111">Derīgs ceļš laukam no veida *Virkne* norādītajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="8bebc-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="8bebc-112">`delimiter`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="8bebc-112">`delimiter`: *String*</span></span>

<span data-ttu-id="8bebc-113">Norobežotājs, ko izmanto, lai atdalītu apakšvirknes.</span><span class="sxs-lookup"><span data-stu-id="8bebc-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="8bebc-114">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="8bebc-114">Return values</span></span>

<span data-ttu-id="8bebc-115">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="8bebc-115">*String*</span></span>

<span data-ttu-id="8bebc-116">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="8bebc-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8bebc-117">Paraugs</span><span class="sxs-lookup"><span data-stu-id="8bebc-117">Example</span></span>

<span data-ttu-id="8bebc-118">Ja `SPLIT("abc" , 1)` ievadāt kā datu avotu **DS**, izteiksme `STRINGJOIN (DS, DS.Value, "-")` atgriež **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="8bebc-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8bebc-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8bebc-119">Additional resources</span></span>

[<span data-ttu-id="8bebc-120">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="8bebc-120">List functions</span></span>](er-functions-category-list.md)
