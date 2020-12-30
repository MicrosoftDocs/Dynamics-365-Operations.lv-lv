---
title: COUNT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota COUNT elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: b3a5bb33964c70c85c7d8571057060c1c2b9d433
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687724"
---
# <a name="count-er-function"></a><span data-ttu-id="feb1b-103">COUNT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="feb1b-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="feb1b-104">`COUNT` funkcija atgriež *Vesela skaitļa* vērtību, kas apzīmē ierakstu skaitu norādītajā sarakstā, ja saraksts nav tukšs.</span><span class="sxs-lookup"><span data-stu-id="feb1b-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="feb1b-105">Ja saraksts ir tukšs, šī funkcija atgriež **0** (nulli).</span><span class="sxs-lookup"><span data-stu-id="feb1b-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="feb1b-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="feb1b-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="feb1b-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="feb1b-107">Arguments</span></span>

<span data-ttu-id="feb1b-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="feb1b-108">`list`: *Record list*</span></span>

<span data-ttu-id="feb1b-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="feb1b-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="feb1b-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="feb1b-110">Return values</span></span>

<span data-ttu-id="feb1b-111">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="feb1b-111">*Integer*</span></span>

<span data-ttu-id="feb1b-112">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="feb1b-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="feb1b-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="feb1b-113">Example</span></span>

<span data-ttu-id="feb1b-114">`COUNT (SPLIT("abcd" , 3))` atgriež **2**, jo `SPLIT` funkcija, kas tiek izmantota šajā piemērā, izveido sarakstu, kas sastāv no diviem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="feb1b-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="feb1b-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="feb1b-115">Additional resources</span></span>

[<span data-ttu-id="feb1b-116">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="feb1b-116">List functions</span></span>](er-functions-category-list.md)
