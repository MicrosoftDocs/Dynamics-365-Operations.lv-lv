---
title: CN_GBT_ADDITIONALDIMENSIONID ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CN_GBT_ADDITIONALDIMENSIONID elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ac0b54476265171b3826e43600f99097701231e1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744395"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="f942c-103">CN_GBT_ADDITIONALDIMENSIONID ER funkcija</span><span class="sxs-lookup"><span data-stu-id="f942c-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f942c-104">`CN_GBT_ADDITIONALDIMENSIONID` funkcija atgriež *Virknes* vērtību, kas apzīmē vienu finanšu dimensijas ID, kas tiek ņemts no norādītās virknes.</span><span class="sxs-lookup"><span data-stu-id="f942c-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="f942c-105">Norādītā virkne parāda visas dimensijas kā komatatdalītu ID sarakstu.</span><span class="sxs-lookup"><span data-stu-id="f942c-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f942c-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="f942c-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="f942c-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="f942c-107">Arguments</span></span>

<span data-ttu-id="f942c-108">`text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="f942c-108">`text`: *String*</span></span>

<span data-ttu-id="f942c-109">*Virknes* vērtība, kas parāda visas dimensijas kā komatatdalītu ID sarakstu.</span><span class="sxs-lookup"><span data-stu-id="f942c-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="f942c-110">`number`: Vesels skaitlis</span><span class="sxs-lookup"><span data-stu-id="f942c-110">`number`: Integer</span></span>

<span data-ttu-id="f942c-111">*Vesela skaitļa* vērtība, kas definē pieprasītās dimensijas sērijas kodu norādītajā virknē.</span><span class="sxs-lookup"><span data-stu-id="f942c-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="f942c-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="f942c-112">Return values</span></span>

<span data-ttu-id="f942c-113">*Virkne*</span><span class="sxs-lookup"><span data-stu-id="f942c-113">*String*</span></span>

<span data-ttu-id="f942c-114">Iegūtā teksta vērtība.</span><span class="sxs-lookup"><span data-stu-id="f942c-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f942c-115">Paraugs</span><span class="sxs-lookup"><span data-stu-id="f942c-115">Example</span></span>

<span data-ttu-id="f942c-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` atgriež **"CC"**.</span><span class="sxs-lookup"><span data-stu-id="f942c-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f942c-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f942c-117">Additional resources</span></span>

[<span data-ttu-id="f942c-118">Citas (biznesa jomai specifiskas) funkcijas</span><span class="sxs-lookup"><span data-stu-id="f942c-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]