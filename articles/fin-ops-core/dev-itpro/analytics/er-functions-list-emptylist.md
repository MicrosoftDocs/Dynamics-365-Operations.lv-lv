---
title: EMPTYLIST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota EMPTYLIST elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: f6c2777065656affc992a427194286008c1df42f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559204"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="0ddd7-103">EMPTYLIST ER funkcija</span><span class="sxs-lookup"><span data-stu-id="0ddd7-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ddd7-104">`EMPTYLIST` funkcija atgriež tukšu *Ierakstu saraksta* vērtību, šī saraksta struktūrai kā avotu izmantojot norādīto sarakstu.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ddd7-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="0ddd7-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="0ddd7-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="0ddd7-106">Arguments</span></span>

<span data-ttu-id="0ddd7-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="0ddd7-107">`list`: *Record list*</span></span>

<span data-ttu-id="0ddd7-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0ddd7-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="0ddd7-109">Return values</span></span>

<span data-ttu-id="0ddd7-110">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="0ddd7-110">*Record list*</span></span>

<span data-ttu-id="0ddd7-111">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="0ddd7-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="0ddd7-112">Example</span></span>

<span data-ttu-id="0ddd7-113">`EMPTYLIST (SPLIT ("abc", 1))` atgriež jaunu tukšu sarakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež izmantotā funkcija `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ddd7-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0ddd7-114">Additional resources</span></span>

[<span data-ttu-id="0ddd7-115">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="0ddd7-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]