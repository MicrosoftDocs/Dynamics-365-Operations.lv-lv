---
title: ISEMPTY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ISEMPTY elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 5dbba375104b57f9fb09ed4e330d85181ec0dff8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684887"
---
# <a name="isempty-er-function"></a><span data-ttu-id="bbdee-103">ISEMPTY ER funkcija</span><span class="sxs-lookup"><span data-stu-id="bbdee-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbdee-104">`ISEMPTY` funkcija atgriež *Būla* vērtību **TRUE**, ja norādītajā sarakstā nav ierakstu.</span><span class="sxs-lookup"><span data-stu-id="bbdee-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="bbdee-105">Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bbdee-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbdee-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="bbdee-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="bbdee-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="bbdee-107">Arguments</span></span>

<span data-ttu-id="bbdee-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="bbdee-108">`list`: *Record list*</span></span>

<span data-ttu-id="bbdee-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="bbdee-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="bbdee-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="bbdee-110">Return values</span></span>

<span data-ttu-id="bbdee-111">*Būla*</span><span class="sxs-lookup"><span data-stu-id="bbdee-111">*Boolean*</span></span>

<span data-ttu-id="bbdee-112">Iegūtā *Būla* vērtība.</span><span class="sxs-lookup"><span data-stu-id="bbdee-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="bbdee-113">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="bbdee-113">Example 1</span></span>

<span data-ttu-id="bbdee-114">Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `ISEMPTY(DS)` atgriež **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bbdee-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="bbdee-115">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="bbdee-115">Example 2</span></span>

<span data-ttu-id="bbdee-116">Izteiksme `ISEMPTY (SPLIT ("",1))` atgriež **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="bbdee-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbdee-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bbdee-117">Additional resources</span></span>

[<span data-ttu-id="bbdee-118">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="bbdee-118">List functions</span></span>](er-functions-category-list.md)
