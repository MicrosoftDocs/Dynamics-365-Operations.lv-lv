---
title: COUNTIF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota COUNTIF elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 19ceb8d3023aadeb6307ed5d930587a8f00f63b7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561378"
---
# <a name="countif-er-function"></a><span data-ttu-id="164f6-103">COUNTIF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="164f6-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="164f6-104">`COUNTIF` funkcija atgriež *Vesela skaitļa* vērtību, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="164f6-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="164f6-105">Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="164f6-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="164f6-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="164f6-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="164f6-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="164f6-107">Arguments</span></span>

<span data-ttu-id="164f6-108">`condition range`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="164f6-108">`condition range`: *String*</span></span>

<span data-ttu-id="164f6-109">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta elektronisko pārskatu (ER) formāta komponenta rekvizītā **Ievāktais datu atslēgas nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="164f6-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="164f6-110">`condition value`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="164f6-110">`condition value`: *String*</span></span>

<span data-ttu-id="164f6-111">Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktā datu atslēgas vērtība**.</span><span class="sxs-lookup"><span data-stu-id="164f6-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="164f6-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="164f6-112">Return values</span></span>

<span data-ttu-id="164f6-113">*Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="164f6-113">*Integer*</span></span>

<span data-ttu-id="164f6-114">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="164f6-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="164f6-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="164f6-115">Usage notes</span></span>

<span data-ttu-id="164f6-116">Rekvizītus **Ievāktās datu atslēgas nosaukums** un **Ievāktā datu atslēgas vērtība** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="164f6-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="164f6-117">Šī funkcija atgriež **0** (nulles) vērtību, ja pašreizējā komponenta **Vispārīgi\\Fails** opcija **Apkopot izvades informāciju** ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="164f6-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="164f6-118">`condition range` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="164f6-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="164f6-119">`condition value` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="164f6-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="164f6-120">Paraugs</span><span class="sxs-lookup"><span data-stu-id="164f6-120">Example</span></span>

<span data-ttu-id="164f6-121">Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.</span><span class="sxs-lookup"><span data-stu-id="164f6-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="164f6-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="164f6-122">Additional resources</span></span>

[<span data-ttu-id="164f6-123">Datu apkopošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="164f6-123">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]