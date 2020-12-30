---
title: EMPTYRECORD ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota EMPTYRECORD elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: d50b31fcbbb99050fca46b0a5ce10cc3fd243691
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684815"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="2c5ba-103">EMPTYRECORD ER funkcija</span><span class="sxs-lookup"><span data-stu-id="2c5ba-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c5ba-104">Funkcija `EMPTYRECORD` atgriež norādītā saraksta pirmo ierakstu kā tukšu vērtību *Konteiners (ieraksts)*, kurai ir tāda pati struktūra kā ieraksta norādītajam ierakstu sarakstam.</span><span class="sxs-lookup"><span data-stu-id="2c5ba-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c5ba-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="2c5ba-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="2c5ba-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="2c5ba-106">Arguments</span></span>

<span data-ttu-id="2c5ba-107">`list`: *Ierakstu saraksts* vai *Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="2c5ba-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="2c5ba-108">*Ierakstu saraksta* vai *Konteinera (ieraksta)* tipa datu avota vienuma derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="2c5ba-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c5ba-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="2c5ba-109">Return values</span></span>

<span data-ttu-id="2c5ba-110">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="2c5ba-110">*Container (record)*</span></span>

<span data-ttu-id="2c5ba-111">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="2c5ba-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2c5ba-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="2c5ba-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="2c5ba-113">Ieraksts null ir ieraksts, kurā visos laukos ir tukšas vērtības.</span><span class="sxs-lookup"><span data-stu-id="2c5ba-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="2c5ba-114">Tukša vērtība skaitļiem ir **0** (nulle), virknēm tā ir tukša virkne utt.</span><span class="sxs-lookup"><span data-stu-id="2c5ba-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="2c5ba-115">Paraugs</span><span class="sxs-lookup"><span data-stu-id="2c5ba-115">Example</span></span>

<span data-ttu-id="2c5ba-116">`EMPTYRECORD (SPLIT ("abc", 1))` atgriež jaunu tukšu ierakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež izmantotā funkcija `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="2c5ba-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="2c5ba-117">Plašāku informāciju skatiet šeit: [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="2c5ba-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c5ba-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2c5ba-118">Additional resources</span></span>

[<span data-ttu-id="2c5ba-119">Ieraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="2c5ba-119">Record functions</span></span>](er-functions-category-record.md)
