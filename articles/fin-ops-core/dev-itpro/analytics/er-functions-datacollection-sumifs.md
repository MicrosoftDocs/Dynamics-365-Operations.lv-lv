---
title: SUMIFS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SUMIFS elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ccf8d373bb081270573f6f80711d8e31ff6c0dc3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042508"
---
# <span data-ttu-id="a6ed8-103"><a name="SUMIFS">SUMIFS ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="a6ed8-103"><a name="SUMIFS">SUMIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6ed8-104">`SUMIFS` funkcija atgriež vērtību *Reāls* skaitlis, kas apzīmē to vērtību summu, kuras atgrieza formāta elementu saistījumi un kuras tika savāktas, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="a6ed8-105">Katrs nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ed8-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="a6ed8-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="a6ed8-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="a6ed8-107">Arguments</span></span>

<span data-ttu-id="a6ed8-108">`key name for summing`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="a6ed8-109">Vērtība, kas tiek atgriezta, izmantojot izteiksmi, kas konfigurēta komponenta elektroniskā pārskata (ER) formāta rekvizītā **Ievāktās atslēgas nosaukums**, kurai summēšanas nolūkā ir jāizmanto saistījuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="a6ed8-110">Rekvizītu **Ievāktās datu atslēgas nosaukums** var konfigurēt vainu komponentā **Skaitlis** vai komponentā **Virkne** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="a6ed8-111">`condition 1 range`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="a6ed8-112">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktās datu atslēgas nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="a6ed8-113">Šis ir obligāts arguments.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-113">This argument is mandatory.</span></span>

<span data-ttu-id="a6ed8-114">Rekvizītu **Ievāktās datu atslēgas nosaukums** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="a6ed8-115">`condition 1 value`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="a6ed8-116">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktā datu atslēgas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="a6ed8-117">Šis ir obligāts arguments.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-117">This argument is mandatory.</span></span>

<span data-ttu-id="a6ed8-118">Rekvizītu **Ievāktās datu atslēgas vērtība** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="a6ed8-119">`condition N range`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-119">`condition N range`: *String*</span></span>

<span data-ttu-id="a6ed8-120">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktās datu atslēgas nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="a6ed8-121">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-121">These additional arguments are optional.</span></span>

<span data-ttu-id="a6ed8-122">Rekvizītu **Ievāktās datu atslēgas nosaukums** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="a6ed8-123">`condition N value`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-123">`condition N value`: *String*</span></span>

<span data-ttu-id="a6ed8-124">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktā datu atslēgas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="a6ed8-125">Šie papildu argumenti nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-125">These additional arguments are optional.</span></span>

<span data-ttu-id="a6ed8-126">Rekvizītu **Ievāktās datu atslēgas vērtība** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="a6ed8-127">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="a6ed8-127">Return values</span></span>

<span data-ttu-id="a6ed8-128">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="a6ed8-128">*Real*</span></span>

<span data-ttu-id="a6ed8-129">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a6ed8-130">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="a6ed8-130">Usage notes</span></span>

<span data-ttu-id="a6ed8-131">Šī funkcija atgriež **0** (nulles) vērtību, ja pašreizējā komponenta **Vispārīgi\\Fails** opcija **Apkopot izvades informāciju** ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="a6ed8-132">`condition range` argumentos aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="a6ed8-133">`condition value` argumentos aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="a6ed8-134">Paraugs</span><span class="sxs-lookup"><span data-stu-id="a6ed8-134">Example</span></span>

<span data-ttu-id="a6ed8-135">Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.</span><span class="sxs-lookup"><span data-stu-id="a6ed8-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6ed8-136">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a6ed8-136">Additional resources</span></span>

[<span data-ttu-id="a6ed8-137">Datu apkopošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="a6ed8-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
