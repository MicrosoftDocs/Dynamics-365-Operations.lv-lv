---
title: IF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota IF elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687006"
---
# <a name="if-er-function"></a><span data-ttu-id="fe0d9-103">IF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="fe0d9-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe0d9-104">`IF` funkcija atgriež pirmo norādīto vērtību, ja tiek izpildīts norādītais nosacījums.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="fe0d9-105">Pretējā gadījumā tiek atgriezta otrā norādītā vērtība.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="fe0d9-106">Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0d9-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="fe0d9-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="fe0d9-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="fe0d9-108">Arguments</span></span>

<span data-ttu-id="fe0d9-109">`condition`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="fe0d9-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="fe0d9-110">Derīga nosacījuma izteiksme, kas ir jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="fe0d9-111">`first value`: *Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="fe0d9-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="fe0d9-112">Rezultāts, kas tiek atgriezts, ja nosacījums ir izpildīts.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="fe0d9-113">`second value`: *Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="fe0d9-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="fe0d9-114">Rezultāts, kas tiek atgriezts, ja nosacījums nav izpildīts.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="fe0d9-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="fe0d9-115">Return values</span></span>

<span data-ttu-id="fe0d9-116">*Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="fe0d9-116">*Any of the supported data types*</span></span>

<span data-ttu-id="fe0d9-117">Jebkura atbalstītā datu tipa iegūtā vērtība.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fe0d9-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="fe0d9-118">Usage notes</span></span>

<span data-ttu-id="fe0d9-119">Argumenti `first value` un `second value` ir jānorāda, izmantojot vienu datu tipu.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="fe0d9-120">Noformēšanas laikā tiek parādīts izņēmums, ja konfigurētās vērtības nesakrīt.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="fe0d9-121">Ja pirmā rezultāta vērtība un otrā rezultāta vērtība ir *Konteinera (ieraksta)* vai *Ierakstu saraksta* datu tipa vērtības, rezultātam ir tikai tie lauki, kas ir abās vērtībās.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="fe0d9-122">Paraugs</span><span class="sxs-lookup"><span data-stu-id="fe0d9-122">Example</span></span>

<span data-ttu-id="fe0d9-123">`IF (1=2, "condition is met", "condition is not met")` atgriež virkni **"nosacījums nav izpildīts"**.</span><span class="sxs-lookup"><span data-stu-id="fe0d9-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe0d9-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fe0d9-124">Additional resources</span></span>

[<span data-ttu-id="fe0d9-125">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="fe0d9-125">Logical functions</span></span>](er-functions-category-logical.md)
