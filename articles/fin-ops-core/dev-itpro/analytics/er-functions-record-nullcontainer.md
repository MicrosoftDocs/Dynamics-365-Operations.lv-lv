---
title: NULLCONTAINER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NULLCONTAINER elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: d08a4a12d2b142744d3f35c6f1088ec25158c97c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563226"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="ee1ed-103">NULLCONTAINER ER funkcija</span><span class="sxs-lookup"><span data-stu-id="ee1ed-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee1ed-104">Funkcija `NULLCONTAINER` atgriež norādītā saraksta pirmo ierakstu kā tukšu vērtību *Konteiners (ieraksts)*, kurai ir tāda pati struktūra kā ieraksta norādītajam ierakstu sarakstam.</span><span class="sxs-lookup"><span data-stu-id="ee1ed-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee1ed-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="ee1ed-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="ee1ed-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="ee1ed-106">Arguments</span></span>

<span data-ttu-id="ee1ed-107">`list`: *Ierakstu saraksts* vai *Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="ee1ed-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="ee1ed-108">*Ierakstu saraksta* vai *Konteinera (ieraksta)* tipa datu avota vienuma derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="ee1ed-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ee1ed-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="ee1ed-109">Return values</span></span>

<span data-ttu-id="ee1ed-110">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="ee1ed-110">*Container (record)*</span></span>

<span data-ttu-id="ee1ed-111">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="ee1ed-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ee1ed-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="ee1ed-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="ee1ed-113">Šī funkcija ir novecojusi.</span><span class="sxs-lookup"><span data-stu-id="ee1ed-113">This function is obsolete.</span></span> <span data-ttu-id="ee1ed-114">Tā vietā izmantojiet `EMPTYRECORD` funkciju.</span><span class="sxs-lookup"><span data-stu-id="ee1ed-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="ee1ed-115">Plašāku informāciju skatiet šeit: [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="ee1ed-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="ee1ed-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="ee1ed-116">Example</span></span>

<span data-ttu-id="ee1ed-117">`NULLCONTAINER (SPLIT ("abc", 1))` atgriež jaunu tukšu ierakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež izmantotā funkcija `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="ee1ed-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="ee1ed-118">Plašāku informāciju skatiet šeit: [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="ee1ed-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee1ed-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ee1ed-119">Additional resources</span></span>

[<span data-ttu-id="ee1ed-120">Ieraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="ee1ed-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]