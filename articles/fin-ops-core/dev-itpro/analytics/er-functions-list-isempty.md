---
title: ISEMPTY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ISEMPTY elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750440"
---
# <a name="isempty-er-function"></a><span data-ttu-id="8d75b-103">ISEMPTY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="8d75b-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d75b-104">`ISEMPTY` funkcija atgriež *Būla* vērtību **TRUE**, ja norādītajā sarakstā nav ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8d75b-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="8d75b-105">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8d75b-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d75b-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="8d75b-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="8d75b-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="8d75b-107">Arguments</span></span>

<span data-ttu-id="8d75b-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="8d75b-108">`list`: *Record list*</span></span>

<span data-ttu-id="8d75b-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="8d75b-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d75b-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="8d75b-110">Return values</span></span>

<span data-ttu-id="8d75b-111">*Būla*</span><span class="sxs-lookup"><span data-stu-id="8d75b-111">*Boolean*</span></span>

<span data-ttu-id="8d75b-112">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="8d75b-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="8d75b-113">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="8d75b-113">Example 1</span></span>

<span data-ttu-id="8d75b-114">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `ISEMPTY(DS)` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8d75b-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="8d75b-115">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="8d75b-115">Example 2</span></span>

<span data-ttu-id="8d75b-116">Izteiksme `ISEMPTY (SPLIT ("",1))` atgriež **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="8d75b-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d75b-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8d75b-117">Additional resources</span></span>

[<span data-ttu-id="8d75b-118">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="8d75b-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]