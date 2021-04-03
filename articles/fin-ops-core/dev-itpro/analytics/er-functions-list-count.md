---
title: COUNT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota COUNT elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: e36347d928148e85bc9295d529cbf2801946433a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567896"
---
# <a name="count-er-function"></a><span data-ttu-id="8a818-103">COUNT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="8a818-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a818-104">`COUNT` funkcija atgriež *Vesela skaitļa* vērtību, kas apzīmē ierakstu skaitu norādītajā sarakstā, ja saraksts nav tukšs.</span><span class="sxs-lookup"><span data-stu-id="8a818-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="8a818-105">Ja saraksts ir tukšs, šī funkcija atgriež **0** (nulli).</span><span class="sxs-lookup"><span data-stu-id="8a818-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a818-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="8a818-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="8a818-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="8a818-107">Arguments</span></span>

<span data-ttu-id="8a818-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="8a818-108">`list`: *Record list*</span></span>

<span data-ttu-id="8a818-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="8a818-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8a818-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="8a818-110">Return values</span></span>

<span data-ttu-id="8a818-111">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="8a818-111">*Integer*</span></span>

<span data-ttu-id="8a818-112">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="8a818-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="8a818-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="8a818-113">Example</span></span>

<span data-ttu-id="8a818-114">`COUNT (SPLIT("abcd" , 3))` atgriež **2**, jo `SPLIT` funkcija, kas tiek izmantota šajā piemērā, izveido sarakstu, kas sastāv no diviem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="8a818-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a818-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8a818-115">Additional resources</span></span>

[<span data-ttu-id="8a818-116">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="8a818-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]