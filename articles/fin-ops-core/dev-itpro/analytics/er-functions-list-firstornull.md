---
title: FIRSTORNULL ER funkcija
description: Šajā tēmā ir paskaidrots, kā tiek lietota FIRSTORNULL elektronisko atskaišu veidošanas (ER) funkcija
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 075b2e064641061adf5404591a784311b6d28697
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917331"
---
# <span data-ttu-id="46031-103"><a name="FIRSTORNULL">FIRSTORNULL ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="46031-103"><a name="FIRSTORNULL">FIRSTORNULL ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46031-104">`FIRSTORNULL`funkcija atgriež norādītā saraksta pirmo ierakstu kā vērtību *Konteiners (ieraksts)*, ja šis ieraksts nav tukšs.</span><span class="sxs-lookup"><span data-stu-id="46031-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="46031-105">Ja ieraksts ir tukšs, šī funkcija atgriež tukšu *Konteinera (ieraksta)* vērtību.</span><span class="sxs-lookup"><span data-stu-id="46031-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="46031-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="46031-106">Syntax</span></span>

```
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="46031-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="46031-107">Arguments</span></span>

<span data-ttu-id="46031-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="46031-108">`list`: *Record list*</span></span>

<span data-ttu-id="46031-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="46031-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="46031-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="46031-110">Return values</span></span>

<span data-ttu-id="46031-111">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="46031-111">*Container (record)*</span></span>

<span data-ttu-id="46031-112">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="46031-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="46031-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="46031-113">Example</span></span>

<span data-ttu-id="46031-114">Izteiksme `FIRSTORNULL(SPLIT("",1)).Value` atgriež tukšu virkni (**""**).</span><span class="sxs-lookup"><span data-stu-id="46031-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46031-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="46031-115">Additional resources</span></span>

[<span data-ttu-id="46031-116">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="46031-116">List functions</span></span>](er-functions-category-list.md)
