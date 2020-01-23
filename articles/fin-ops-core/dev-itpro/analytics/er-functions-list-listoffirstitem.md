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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d985ef5015bc104a83260b64418821cc715e8cb
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917262"
---
# <span data-ttu-id="af065-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="af065-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af065-104">`LISTOFFIRSTITEM` funkcija atgriež *Ierakstu saraksta* vērtību, kas sastāv vienīgi no norādītā saraksta pirmā ieraksta.</span><span class="sxs-lookup"><span data-stu-id="af065-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="af065-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="af065-105">Syntax</span></span>

```
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="af065-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="af065-106">Arguments</span></span>

<span data-ttu-id="af065-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="af065-107">`list`: *Record list*</span></span>

<span data-ttu-id="af065-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="af065-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="af065-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="af065-109">Return values</span></span>

<span data-ttu-id="af065-110">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="af065-110">*Record list*</span></span>

<span data-ttu-id="af065-111">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="af065-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="af065-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="af065-112">Example</span></span>

<span data-ttu-id="af065-113">Izteiksme `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` atgriež teksta vērtību **"A".**</span><span class="sxs-lookup"><span data-stu-id="af065-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af065-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="af065-114">Additional resources</span></span>

[<span data-ttu-id="af065-115">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="af065-115">List functions</span></span>](er-functions-category-list.md)
