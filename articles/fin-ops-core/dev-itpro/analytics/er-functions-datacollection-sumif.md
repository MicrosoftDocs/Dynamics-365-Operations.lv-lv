---
title: SUMIF ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SUMIF elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 04/27/2020
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
ms.openlocfilehash: 6f5069d197abf2e38d09012defeb982a9e5e1234
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565968"
---
# <a name="sumif-er-function"></a><span data-ttu-id="f35fe-103">SUMIF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="f35fe-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f35fe-104">`SUMIF` funkcija atgriež vērtību *Reāls* skaitlis, kas apzīmē to vērtību summu, kuras atgrieza formāta elementu saistījumi un kuras tika savāktas, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="f35fe-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="f35fe-105">Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="f35fe-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f35fe-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="f35fe-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="f35fe-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="f35fe-107">Arguments</span></span>

<span data-ttu-id="f35fe-108">`key name for summing`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="f35fe-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="f35fe-109">Vērtība, kas tiek atgriezta, izmantojot izteiksmi, kas konfigurēta komponenta elektroniskā pārskata (ER) formāta rekvizītā **Ievāktās atslēgas nosaukums**, kurai summēšanas nolūkā ir jāizmanto saistījuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="f35fe-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="f35fe-110">Rekvizītu **Ievāktās datu atslēgas vērtība** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="f35fe-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="f35fe-111">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="f35fe-111">Return values</span></span>

<span data-ttu-id="f35fe-112">*Reāls*</span><span class="sxs-lookup"><span data-stu-id="f35fe-112">*Real*</span></span>

<span data-ttu-id="f35fe-113">Iegūtā skaitliskā vērtība.</span><span class="sxs-lookup"><span data-stu-id="f35fe-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f35fe-114">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="f35fe-114">Usage notes</span></span>

<span data-ttu-id="f35fe-115">Šī funkcija atgriež **0** (nulles) vērtību, ja pašreizējā komponenta **Vispārīgi\\Fails** opcija **Apkopot izvades informāciju** ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="f35fe-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="f35fe-116">`condition range` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="f35fe-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="f35fe-117">`condition value` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="f35fe-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="f35fe-118">Paraugs</span><span class="sxs-lookup"><span data-stu-id="f35fe-118">Example</span></span>

<span data-ttu-id="f35fe-119">Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.</span><span class="sxs-lookup"><span data-stu-id="f35fe-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="f35fe-120">Lai iegūtu papildu informāciju un piemērus par šīs funkcijas izmantošanu, skatiet [Secības elementu izpildes atlikšana ER formātos](er-defer-sequence-element.md#Example) un [XML elementu izpildes atlikšana ER formātos](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="f35fe-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f35fe-121">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f35fe-121">Additional resources</span></span>

[<span data-ttu-id="f35fe-122">Datu apkopošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="f35fe-122">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]