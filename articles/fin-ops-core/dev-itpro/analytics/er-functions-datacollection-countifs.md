---
title: COUNTIFS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota COUNTIFS elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: a28e2dd263c3f2cabd1c07c4aba8dfb22db01cc4
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745661"
---
# <a name="countifs-er-function"></a><span data-ttu-id="65d0b-103">COUNTIFS ER funkcija</span><span class="sxs-lookup"><span data-stu-id="65d0b-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65d0b-104">`COUNTIFS` funkcija atgriež *Vesela skaitļa* vērtību, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="65d0b-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="65d0b-105">Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="65d0b-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d0b-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="65d0b-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="65d0b-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="65d0b-107">Arguments</span></span>

<span data-ttu-id="65d0b-108">`condition 1 range`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="65d0b-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="65d0b-109">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta elektronisko pārskatu (ER) formāta komponenta rekvizītā **Ievāktais datu atslēgas nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="65d0b-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="65d0b-110">Šis ir obligāts arguments.</span><span class="sxs-lookup"><span data-stu-id="65d0b-110">This argument is mandatory.</span></span>

<span data-ttu-id="65d0b-111">`condition 1 value`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="65d0b-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="65d0b-112">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktā datu atslēgas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="65d0b-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="65d0b-113">Šis ir obligāts arguments.</span><span class="sxs-lookup"><span data-stu-id="65d0b-113">This argument is mandatory.</span></span>

<span data-ttu-id="65d0b-114">`condition N range`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="65d0b-114">`condition N range`: *String*</span></span>

<span data-ttu-id="65d0b-115">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktās datu atslēgas nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="65d0b-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="65d0b-116">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="65d0b-116">These additional arguments are optional.</span></span>

<span data-ttu-id="65d0b-117">`condition N value`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="65d0b-117">`condition N value`: *String*</span></span>

<span data-ttu-id="65d0b-118">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktā datu atslēgas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="65d0b-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="65d0b-119">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="65d0b-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="65d0b-120">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="65d0b-120">Return values</span></span>

<span data-ttu-id="65d0b-121">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="65d0b-121">*Integer*</span></span>

<span data-ttu-id="65d0b-122">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="65d0b-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="65d0b-123">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="65d0b-123">Usage notes</span></span>

<span data-ttu-id="65d0b-124">Rekvizītus **Ievāktās datu atslēgas nosaukums** un **Ievāktā datu atslēgas vērtība** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="65d0b-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="65d0b-125">Šī funkcija atgriež **0** (nulles) vērtību, ja pašreizējā komponenta **Vispārīgi\\Fails** opcija **Apkopot izvades informāciju** ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="65d0b-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="65d0b-126">`condition range` argumentos aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="65d0b-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="65d0b-127">`condition value` argumentos aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="65d0b-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="65d0b-128">Paraugs</span><span class="sxs-lookup"><span data-stu-id="65d0b-128">Example</span></span>

<span data-ttu-id="65d0b-129">Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.</span><span class="sxs-lookup"><span data-stu-id="65d0b-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65d0b-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="65d0b-130">Additional resources</span></span>

[<span data-ttu-id="65d0b-131">Datu apkopošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="65d0b-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
