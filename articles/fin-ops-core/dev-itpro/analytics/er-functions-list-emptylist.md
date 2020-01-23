---
title: EMPTYLIST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota EMPTYLIST elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: a60bc948ff6223b6e3acccd0ba40bf64f238aac2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917400"
---
# <span data-ttu-id="65b3c-103"><a name="EMPTYLIST">EMPTYLIST ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="65b3c-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65b3c-104">`EMPTYLIST` funkcija atgriež tukšu *Ierakstu saraksta* vērtību, šī saraksta struktūrai kā avotu izmantojot norādīto sarakstu.</span><span class="sxs-lookup"><span data-stu-id="65b3c-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b3c-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="65b3c-105">Syntax</span></span>

```
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="65b3c-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="65b3c-106">Arguments</span></span>

<span data-ttu-id="65b3c-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="65b3c-107">`list`: *Record list*</span></span>

<span data-ttu-id="65b3c-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="65b3c-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="65b3c-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="65b3c-109">Return values</span></span>

<span data-ttu-id="65b3c-110">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="65b3c-110">*Record list*</span></span>

<span data-ttu-id="65b3c-111">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="65b3c-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="65b3c-112">Paraugs</span><span class="sxs-lookup"><span data-stu-id="65b3c-112">Example</span></span>

<span data-ttu-id="65b3c-113">`EMPTYLIST (SPLIT ("abc", 1))` atgriež jaunu tukšu sarakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež izmantotā funkcija `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="65b3c-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65b3c-114">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="65b3c-114">Additional resources</span></span>

[<span data-ttu-id="65b3c-115">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="65b3c-115">List functions</span></span>](er-functions-category-list.md)
