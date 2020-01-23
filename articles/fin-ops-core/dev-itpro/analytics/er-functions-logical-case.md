---
title: CASE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CASE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 38b51a4d8bf8dc997bae2ae9206d8e71ca48dec6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916066"
---
# <span data-ttu-id="23a50-103"><a name="CASE">CASE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="23a50-103"><a name="CASE">CASE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23a50-104">`CASE` funkcija novērtē norādītās izteiksmes vērtību pret norādītajām alternatīvajām opcijām un atgriež pirmās opcijas, kas ir vienāda ar norādītās izteiksmes vērtību, rezultātu.</span><span class="sxs-lookup"><span data-stu-id="23a50-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="23a50-105">Pretējā gadījumā tas atgriež neobligātu noklusējuma rezultātu, ja noklusējuma rezultāts ir norādīts kā pēdējās funkcijas izsauktais arguments, pirms kura neatrodas opcija.</span><span class="sxs-lookup"><span data-stu-id="23a50-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="23a50-106">Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība.</span><span class="sxs-lookup"><span data-stu-id="23a50-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a50-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="23a50-107">Syntax</span></span>

```
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="23a50-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="23a50-108">Arguments</span></span>

<span data-ttu-id="23a50-109">`expression`: *Primitīvs datu tips* (Būla, skaitlisks vai teksta)</span><span class="sxs-lookup"><span data-stu-id="23a50-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="23a50-110">Derīga izteiksme, kas atgriež vērtību no primitīva datu tipa.</span><span class="sxs-lookup"><span data-stu-id="23a50-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="23a50-111">`option 1`: *Primitīvs datu tips* (Būla, skaitlisks vai teksta)</span><span class="sxs-lookup"><span data-stu-id="23a50-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="23a50-112">Derīga izteiksme, kas atgriež vērtību no tā paša primitīva datu tipa kā izsauktās `expression` funkcijas argumentu.</span><span class="sxs-lookup"><span data-stu-id="23a50-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="23a50-113">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="23a50-113">This argument is required.</span></span>

<span data-ttu-id="23a50-114">`result 1`: *Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="23a50-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="23a50-115">Atgrieztais rezultāts, kas atbilst iepriekšējai opcijai.</span><span class="sxs-lookup"><span data-stu-id="23a50-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="23a50-116">Šis arguments ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="23a50-116">This argument is required.</span></span>

<span data-ttu-id="23a50-117">`option N`: *Primitīvs datu tips* (Būla, skaitlisks vai teksta)</span><span class="sxs-lookup"><span data-stu-id="23a50-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="23a50-118">Derīga izteiksme, kas atgriež vērtību no tā paša primitīva datu tipa kā izsauktās `expression` funkcijas argumentu.</span><span class="sxs-lookup"><span data-stu-id="23a50-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="23a50-119">ŠIs arguments nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="23a50-119">This argument is optional.</span></span>

<span data-ttu-id="23a50-120">`result N`: *Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="23a50-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="23a50-121">Atgrieztais rezultāts, kas atbilst iepriekšējai opcijai.</span><span class="sxs-lookup"><span data-stu-id="23a50-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="23a50-122">ŠIs arguments nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="23a50-122">This argument is optional.</span></span>

<span data-ttu-id="23a50-123">`default result`: *Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="23a50-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="23a50-124">Rezultāts, kas ir jāatgriež, ja nav atbilstības.</span><span class="sxs-lookup"><span data-stu-id="23a50-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="23a50-125">ŠIs arguments nav obligāts.</span><span class="sxs-lookup"><span data-stu-id="23a50-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="23a50-126">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="23a50-126">Return values</span></span>

<span data-ttu-id="23a50-127">*Jebkurš no atbalstītajiem datu tipiem*</span><span class="sxs-lookup"><span data-stu-id="23a50-127">*Any of the supported data types*</span></span>

<span data-ttu-id="23a50-128">Jebkura atbalstītā datu tipa iegūtā vērtība.</span><span class="sxs-lookup"><span data-stu-id="23a50-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="23a50-129">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="23a50-129">Usage notes</span></span>

<span data-ttu-id="23a50-130">Izņēmums tiek rādīts izpildlaikā, ja nav atbilstības un nav definēts izvēles noklusējuma rezultāts.</span><span class="sxs-lookup"><span data-stu-id="23a50-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="23a50-131">Visi rezultāti ir jānorāda, izmantojot vienu datu tipu.</span><span class="sxs-lookup"><span data-stu-id="23a50-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="23a50-132">Noformēšanas laikā tiek parādīts izņēmums, ja konfigurēto rezultātu datu tipi nesakrīt.</span><span class="sxs-lookup"><span data-stu-id="23a50-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="23a50-133">Ja pirmā rezultāta vērtība un *N*-tā rezultāta vērtība ir *Konteinera (ieraksta)* vai *Ierakstu saraksta* datu tipa vērtības, rezultātam ir tikai tie lauki, kas ir abās vērtībās.</span><span class="sxs-lookup"><span data-stu-id="23a50-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="23a50-134">Paraugs</span><span class="sxs-lookup"><span data-stu-id="23a50-134">Example</span></span>

<span data-ttu-id="23a50-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")`atgriež virkni **"WINTER"**, ja pašreizējās lietojumprogrammas sesijas datums ir no oktobra līdz decembrim.</span><span class="sxs-lookup"><span data-stu-id="23a50-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="23a50-136">Pretējā gadījumā šī izteiksme atgriež tukšu virkni.</span><span class="sxs-lookup"><span data-stu-id="23a50-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23a50-137">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="23a50-137">Additional resources</span></span>

[<span data-ttu-id="23a50-138">Loģiskas funkcijas</span><span class="sxs-lookup"><span data-stu-id="23a50-138">Logical functions</span></span>](er-functions-category-logical.md)
