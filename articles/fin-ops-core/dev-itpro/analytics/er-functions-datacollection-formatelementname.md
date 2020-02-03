---
title: FORMATELEMENTNAME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FORMATELEMENTNAME elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: d66fed3815188fa7e31735e3523376ae4ea1cf46
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917676"
---
# <span data-ttu-id="71db9-103"><a name="FORMATELEMENTNAME">FORMATELEMENTNAME ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="71db9-103"><a name="FORMATELEMENTNAME">FORMATELEMENTNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71db9-104">`FORMATELEMENTNAME` funkcija atgriež vērtību *Virkne*, kas apzīmē pašreizējā elektroniskā pārskata (ER) formāta elementa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="71db9-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="71db9-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="71db9-105">Syntax</span></span>

```
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="71db9-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="71db9-106">Return values</span></span>

<span data-ttu-id="71db9-107">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="71db9-107">*String*</span></span>

<span data-ttu-id="71db9-108">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="71db9-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="71db9-109">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="71db9-109">Usage notes</span></span>

<span data-ttu-id="71db9-110">Šo funkciju var izteikt ER izteiksmēs, kas bija konfigurētas rekvizītiem **Ievāktās datu atslēgas nosaukums** un **Ievāktās datu atslēgas vērtība** ER formāta komponentē no grupas **Teksts**, kas atrodas komponentē **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="71db9-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="71db9-111">Paraugs</span><span class="sxs-lookup"><span data-stu-id="71db9-111">Example</span></span>

<span data-ttu-id="71db9-112">Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.</span><span class="sxs-lookup"><span data-stu-id="71db9-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71db9-113">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="71db9-113">Additional resources</span></span>

[<span data-ttu-id="71db9-114">Datu apkopošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="71db9-114">Data collection functions</span></span>](er-functions-category-data-collection.md)