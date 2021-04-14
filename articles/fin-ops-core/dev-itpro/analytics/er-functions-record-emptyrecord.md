---
title: EMPTYRECORD ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota EMPTYRECORD elektroniskā pārskata (ER) funkcija.
author: NickSelin
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
ms.openlocfilehash: e614c06b4cfad628bbd8a966719ed994ce05b792
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746535"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="031b1-103">EMPTYRECORD ER funkcija</span><span class="sxs-lookup"><span data-stu-id="031b1-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="031b1-104">Funkcija `EMPTYRECORD` atgriež norādītā saraksta pirmo ierakstu kā tukšu vērtību *Konteiners (ieraksts)*, kurai ir tāda pati struktūra kā ieraksta norādītajam ierakstu sarakstam.</span><span class="sxs-lookup"><span data-stu-id="031b1-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="031b1-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="031b1-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="031b1-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="031b1-106">Arguments</span></span>

<span data-ttu-id="031b1-107">`list`: *Ierakstu saraksts* vai *Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="031b1-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="031b1-108">*Ierakstu saraksta* vai *Konteinera (ieraksta)* tipa datu avota vienuma derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="031b1-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="031b1-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="031b1-109">Return values</span></span>

<span data-ttu-id="031b1-110">*Konteiners (ieraksts)*</span><span class="sxs-lookup"><span data-stu-id="031b1-110">*Container (record)*</span></span>

<span data-ttu-id="031b1-111">Iegūtā ieraksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="031b1-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="031b1-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="031b1-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="031b1-113">Ieraksts null ir ieraksts, kurā visos laukos ir tukšas vērtības.</span><span class="sxs-lookup"><span data-stu-id="031b1-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="031b1-114">Tukša vērtība skaitļiem ir **0** (nulle), virknēm tā ir tukša virkne utt.</span><span class="sxs-lookup"><span data-stu-id="031b1-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="031b1-115">Paraugs</span><span class="sxs-lookup"><span data-stu-id="031b1-115">Example</span></span>

<span data-ttu-id="031b1-116">`EMPTYRECORD (SPLIT ("abc", 1))` atgriež jaunu tukšu ierakstu, kura struktūra ir tāda pati kā sarakstam, ko atgriež izmantotā funkcija `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="031b1-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="031b1-117">Plašāku informāciju skatiet šeit: [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="031b1-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="031b1-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="031b1-118">Additional resources</span></span>

[<span data-ttu-id="031b1-119">Ieraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="031b1-119">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]