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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca7c0f449aff75527e5052ba01e6fc0e29bb0fd7
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917699"
---
# <span data-ttu-id="ec554-103"><a name="COUNTIF">COUNTIF ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="ec554-103"><a name="COUNTIF">COUNTIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec554-104">`COUNTIF` funkcija atgriež *Vesela skaitļa* vērtību, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="ec554-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="ec554-105">Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="ec554-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec554-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="ec554-106">Syntax</span></span>

```
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="ec554-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="ec554-107">Arguments</span></span>

<span data-ttu-id="ec554-108">`condition range`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="ec554-108">`condition range`: *String*</span></span>

<span data-ttu-id="ec554-109">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta elektronisko pārskatu (ER) formāta komponenta rekvizītā **Ievāktais datu atslēgas nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="ec554-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="ec554-110">`condition value`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="ec554-110">`condition value`: *String*</span></span>

<span data-ttu-id="ec554-111">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktā datu atslēgas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="ec554-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="ec554-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="ec554-112">Return values</span></span>

<span data-ttu-id="ec554-113">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="ec554-113">*Integer*</span></span>

<span data-ttu-id="ec554-114">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="ec554-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ec554-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="ec554-115">Usage notes</span></span>

<span data-ttu-id="ec554-116">Rekvizītus **Ievāktās datu atslēgas nosaukums** un **Ievāktā datu atslēgas vērtība** var konfigurēt vainu komponentā  **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="ec554-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="ec554-117">Šī funkcija atgriež **0** (nulles) vērtību, ja pašreizējā komponenta **Vispārīgi\\Fails** opcija **Apkopot izvades informāciju** ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="ec554-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="ec554-118">`condition range` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="ec554-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="ec554-119">`condition value` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="ec554-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="ec554-120">Paraugs</span><span class="sxs-lookup"><span data-stu-id="ec554-120">Example</span></span>

<span data-ttu-id="ec554-121">Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.</span><span class="sxs-lookup"><span data-stu-id="ec554-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec554-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ec554-122">Additional resources</span></span>

[<span data-ttu-id="ec554-123">Datu apkopošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="ec554-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
