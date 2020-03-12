---
title: NULLCONTAINER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NULLCONTAINER elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: ea71bfc4b30164fd32e804bf83a46c49cd18d155
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041473"
---
# <span data-ttu-id="91a79-103"><a name="NULLCONTAINER">NULLCONTAINER ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="91a79-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91a79-104"> `NULLCONTAINER` funkcija atgriež norādītā saraksta pirmo ierakstu kā tukšu vērtību *Konteiners (ieraksts)*, kurai ir tāda pati struktūra kā ieraksta norādītajam ierakstu sarakstam.</span><span class="sxs-lookup"><span data-stu-id="91a79-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a79-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="91a79-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="91a79-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="91a79-106">Arguments</span></span>

<span data-ttu-id="91a79-107">`list`: *Ierakstu saraksts* vai *Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="91a79-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="91a79-108">*Ierakstu saraksta* vai *Konteinera (ieraksta)* tipa datu avota vienuma derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="91a79-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="91a79-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="91a79-109">Return values</span></span>

<span data-ttu-id="91a79-110">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="91a79-110">*Container (record)*</span></span>

<span data-ttu-id="91a79-111">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="91a79-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="91a79-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="91a79-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="91a79-113">Šī funkcija ir novecojusi.</span><span class="sxs-lookup"><span data-stu-id="91a79-113">This function is obsolete.</span></span> <span data-ttu-id="91a79-114">Tā vietā izmantojiet `EMPTYRECORD`funkciju.</span><span class="sxs-lookup"><span data-stu-id="91a79-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="91a79-115">Plašāku informāciju skatiet šeit: [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="91a79-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="91a79-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="91a79-116">Example</span></span>

<span data-ttu-id="91a79-117">`NULLCONTAINER (SPLIT ("abc", 1))` atgriež jaunu tukšu ierakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež izmantotā funkcija `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="91a79-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="91a79-118">Plašāku informāciju skatiet šeit: [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="91a79-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91a79-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="91a79-119">Additional resources</span></span>

[<span data-ttu-id="91a79-120">Ieraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="91a79-120">Record functions</span></span>](er-functions-category-record.md)
