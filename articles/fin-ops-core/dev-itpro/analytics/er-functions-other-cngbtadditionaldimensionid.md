---
title: CN_GBT_ADDITIONALDIMENSIONID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CN_GBT_ADDITIONALDIMENSIONID elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: df693d745d1fe74b4500dd3fda0cc0c4be21142d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917032"
---
# <span data-ttu-id="3d327-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="3d327-103"><a name="CN_GBT_ADDITIONALDIMENSIONID">CN_GBT_ADDITIONALDIMENSIONID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d327-104">`CN_GBT_ADDITIONALDIMENSIONID` funkcija atgriež *Virknes* vērtību, kas apzīmē vienu finanšu dimensijas ID, kas tiek ņemts no norādītās virknes.</span><span class="sxs-lookup"><span data-stu-id="3d327-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="3d327-105">Norādītā virkne parāda visas dimensijas kā komatatdalītu ID sarakstu.</span><span class="sxs-lookup"><span data-stu-id="3d327-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d327-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="3d327-106">Syntax</span></span>

```
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="3d327-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="3d327-107">Arguments</span></span>

<span data-ttu-id="3d327-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="3d327-108">`text`: *String*</span></span>

<span data-ttu-id="3d327-109">*Virknes* vērtība, kas parāda visas dimensijas kā komatatdalītu ID sarakstu.</span><span class="sxs-lookup"><span data-stu-id="3d327-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="3d327-110">`number`: Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="3d327-110">`number`: Integer</span></span>

<span data-ttu-id="3d327-111">*Vesela skaitļa* vērtība, kas definē pieprasītās dimensijas sērijas kodu norādītajā virknē.</span><span class="sxs-lookup"><span data-stu-id="3d327-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="3d327-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="3d327-112">Return values</span></span>

<span data-ttu-id="3d327-113">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="3d327-113">*String*</span></span>

<span data-ttu-id="3d327-114">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="3d327-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3d327-115">Paraugs</span><span class="sxs-lookup"><span data-stu-id="3d327-115">Example</span></span>

<span data-ttu-id="3d327-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` atgriež **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="3d327-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d327-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3d327-117">Additional resources</span></span>

[<span data-ttu-id="3d327-118">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="3d327-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
