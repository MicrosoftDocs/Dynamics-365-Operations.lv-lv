---
title: STRINGJOIN ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota STRINGJOIN elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: ac21651e0f5b5a1579b9335bb7f3217370c4d5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745525"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="d366e-103">STRINGJOIN ER funkcija</span><span class="sxs-lookup"><span data-stu-id="d366e-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d366e-104">`STRINGJOIN` funkcija atgriež *Virknes* vērtību, kas sastāv no norādītā saraksta norādītā lauka savirknētajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d366e-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="d366e-105">Vērtības var atdalīt ar norādīto norobežotāju.</span><span class="sxs-lookup"><span data-stu-id="d366e-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d366e-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="d366e-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="d366e-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="d366e-107">Arguments</span></span>

<span data-ttu-id="d366e-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="d366e-108">`list`: *Record list*</span></span>

<span data-ttu-id="d366e-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="d366e-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d366e-110">`field`: *Lauks*</span><span class="sxs-lookup"><span data-stu-id="d366e-110">`field`: *Field*</span></span>

<span data-ttu-id="d366e-111">Derīgs ceļš laukam no veida *Virkne* norādītajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="d366e-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="d366e-112">`delimiter`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="d366e-112">`delimiter`: *String*</span></span>

<span data-ttu-id="d366e-113">Norobežotājs, ko izmanto, lai atdalītu apakšvirknes.</span><span class="sxs-lookup"><span data-stu-id="d366e-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="d366e-114">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="d366e-114">Return values</span></span>

<span data-ttu-id="d366e-115">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="d366e-115">*String*</span></span>

<span data-ttu-id="d366e-116">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="d366e-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d366e-117">Paraugs</span><span class="sxs-lookup"><span data-stu-id="d366e-117">Example</span></span>

<span data-ttu-id="d366e-118">Ja `SPLIT("abc" , 1)` ievadāt kā datu avotu **DS**, izteiksme `STRINGJOIN (DS, DS.Value, "-")` atgriež **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="d366e-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d366e-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d366e-119">Additional resources</span></span>

[<span data-ttu-id="d366e-120">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="d366e-120">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]