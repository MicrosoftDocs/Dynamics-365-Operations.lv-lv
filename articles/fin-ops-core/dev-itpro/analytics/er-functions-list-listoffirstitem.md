---
title: LISTOFFIRSTITEM ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LISTOFFIRSTITEM elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 8ea81bce8cd6b922f3ef1d53ec0c4b2574780377
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686492"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="81b88-103">LISTOFFIRSTITEM ER funkcija</span><span class="sxs-lookup"><span data-stu-id="81b88-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81b88-104">`LISTOFFIRSTITEM` funkcija atgriež *Ierakstu saraksta* vērtību, kas sastāv vienīgi no norādītā saraksta pirmā ieraksta.</span><span class="sxs-lookup"><span data-stu-id="81b88-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b88-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="81b88-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="81b88-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="81b88-106">Arguments</span></span>

<span data-ttu-id="81b88-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="81b88-107">`list`: *Record list*</span></span>

<span data-ttu-id="81b88-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="81b88-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="81b88-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="81b88-109">Return values</span></span>

<span data-ttu-id="81b88-110">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="81b88-110">*Record list*</span></span>

<span data-ttu-id="81b88-111">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="81b88-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="81b88-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="81b88-112">Example</span></span>

<span data-ttu-id="81b88-113">Izteiksme `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` atgriež teksta vērtību **"A".**</span><span class="sxs-lookup"><span data-stu-id="81b88-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81b88-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="81b88-114">Additional resources</span></span>

[<span data-ttu-id="81b88-115">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="81b88-115">List functions</span></span>](er-functions-category-list.md)
