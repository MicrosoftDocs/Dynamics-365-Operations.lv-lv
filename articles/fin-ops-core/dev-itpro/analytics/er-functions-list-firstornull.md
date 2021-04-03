---
title: FIRSTORNULL ER funkcija
description: Šajā tēmā ir paskaidrots, kā tiek lietota FIRSTORNULL elektronisko atskaišu veidošanas (ER) funkcija
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 53284333507ef1264d3eb66b0c7141eb69f32392
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564629"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="4d6a7-103">FIRSTORNULL ER funkcija</span><span class="sxs-lookup"><span data-stu-id="4d6a7-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d6a7-104">`FIRSTORNULL` funkcija atgriež norādītā saraksta pirmo ierakstu kā vērtību *Konteiners (ieraksts)*, ja šis ieraksts nav tukšs.</span><span class="sxs-lookup"><span data-stu-id="4d6a7-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="4d6a7-105">Ja ieraksts ir tukšs, šī funkcija atgriež tukšu *Konteinera (ieraksta)* vērtību.</span><span class="sxs-lookup"><span data-stu-id="4d6a7-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d6a7-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="4d6a7-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="4d6a7-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="4d6a7-107">Arguments</span></span>

<span data-ttu-id="4d6a7-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="4d6a7-108">`list`: *Record list*</span></span>

<span data-ttu-id="4d6a7-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="4d6a7-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4d6a7-110">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="4d6a7-110">Return values</span></span>

<span data-ttu-id="4d6a7-111">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="4d6a7-111">*Container (record)*</span></span>

<span data-ttu-id="4d6a7-112">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="4d6a7-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="4d6a7-113">Paraugs</span><span class="sxs-lookup"><span data-stu-id="4d6a7-113">Example</span></span>

<span data-ttu-id="4d6a7-114">Izteiksme `FIRSTORNULL(SPLIT("",1)).Value` atgriež tukšu virkni (**""**).</span><span class="sxs-lookup"><span data-stu-id="4d6a7-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d6a7-115">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4d6a7-115">Additional resources</span></span>

[<span data-ttu-id="4d6a7-116">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="4d6a7-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]