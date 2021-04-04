---
title: FORMATELEMENTNAME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FORMATELEMENTNAME elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561306"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="3dcd7-103">FORMATELEMENTNAME ER funkcija</span><span class="sxs-lookup"><span data-stu-id="3dcd7-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3dcd7-104">`FORMATELEMENTNAME` funkcija atgriež vērtību *Virkne*, kas apzīmē pašreizējā elektroniskā pārskata (ER) formāta elementa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="3dcd7-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dcd7-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="3dcd7-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="3dcd7-106">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="3dcd7-106">Return values</span></span>

<span data-ttu-id="3dcd7-107">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="3dcd7-107">*String*</span></span>

<span data-ttu-id="3dcd7-108">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="3dcd7-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3dcd7-109">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="3dcd7-109">Usage notes</span></span>

<span data-ttu-id="3dcd7-110">Šo funkciju var izteikt ER izteiksmēs, kas bija konfigurētas rekvizītiem **Ievāktās datu atslēgas nosaukums** un **Ievāktās datu atslēgas vērtība** ER formāta komponentē no grupas **Teksts**, kas atrodas komponentē **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.</span><span class="sxs-lookup"><span data-stu-id="3dcd7-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="3dcd7-111">Paraugs</span><span class="sxs-lookup"><span data-stu-id="3dcd7-111">Example</span></span>

<span data-ttu-id="3dcd7-112">Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.</span><span class="sxs-lookup"><span data-stu-id="3dcd7-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3dcd7-113">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3dcd7-113">Additional resources</span></span>

[<span data-ttu-id="3dcd7-114">Datu apkopošanas funkcijas</span><span class="sxs-lookup"><span data-stu-id="3dcd7-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]