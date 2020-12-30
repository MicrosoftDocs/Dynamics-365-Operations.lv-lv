---
title: COUNTIF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota COUNTIF elektroniskā pārskata (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1429ad98f9d4fdab992c2011c6518734484a84
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681188"
---
# <a name="countif-er-function"></a><span data-ttu-id="51e68-103">COUNTIF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="51e68-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51e68-104">`COUNTIF` funkcija atgriež *Vesela skaitļa* vērtību, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="51e68-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="51e68-105">Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="51e68-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e68-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="51e68-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="51e68-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="51e68-107">Arguments</span></span>

<span data-ttu-id="51e68-108">`condition range`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="51e68-108">`condition range`: *String*</span></span>

<span data-ttu-id="51e68-109">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta elektronisko pārskatu (ER) formāta komponenta rekvizītā **Ievāktais datu atslēgas nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="51e68-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="51e68-110">`condition value`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="51e68-110">`condition value`: *String*</span></span>

<span data-ttu-id="51e68-111">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktā datu atslēgas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="51e68-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="51e68-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="51e68-112">Return values</span></span>

<span data-ttu-id="51e68-113">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="51e68-113">*Integer*</span></span>

<span data-ttu-id="51e68-114">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="51e68-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="51e68-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="51e68-115">Usage notes</span></span>

<span data-ttu-id="51e68-116">Rekvizītus **Ievāktās datu atslēgas nosaukums** un **Ievāktā datu atslēgas vērtība** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="51e68-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="51e68-117">Šī funkcija atgriež **0** (nulles) vērtību, ja pašreizējā komponenta **Vispārīgi\\Fails** opcija **Apkopot izvades informāciju** ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="51e68-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="51e68-118">`condition range` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="51e68-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="51e68-119">`condition value` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="51e68-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="51e68-120">Paraugs</span><span class="sxs-lookup"><span data-stu-id="51e68-120">Example</span></span>

<span data-ttu-id="51e68-121">Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.</span><span class="sxs-lookup"><span data-stu-id="51e68-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51e68-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="51e68-122">Additional resources</span></span>

[<span data-ttu-id="51e68-123">Datu apkopošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="51e68-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
