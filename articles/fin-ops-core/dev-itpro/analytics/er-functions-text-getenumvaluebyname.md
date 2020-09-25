---
title: GETENUMVALUEBYNAME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota GETENUMVALUEBYNAME elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743859"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="96ca1-103">GETENUMVALUEBYNAME ER funkcija</span><span class="sxs-lookup"><span data-stu-id="96ca1-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96ca1-104">`GETENUMVALUEBYNAME` funkcija meklē konkrētu *Enum* vērtību norādītajā uzskaitījuma datu avotā, izmantojot uzskaitījuma nosaukumu, kas ir norādīts kā *Virknes* vērtība.</span><span class="sxs-lookup"><span data-stu-id="96ca1-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="96ca1-105">Ja tiek tiek atrasta *Enum* vērtība, funkcija to atgriež.</span><span class="sxs-lookup"><span data-stu-id="96ca1-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="96ca1-106">Pretējā gadījumā funkcija atgriež uzskaitījuma vērtību **null**.</span><span class="sxs-lookup"><span data-stu-id="96ca1-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="96ca1-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="96ca1-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="96ca1-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="96ca1-108">Arguments</span></span>

<span data-ttu-id="96ca1-109">`enumeration data source path`: *Uzskaitījums*</span><span class="sxs-lookup"><span data-stu-id="96ca1-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="96ca1-110">Derīgs datu avota atsauces ceļš vienam no šādiem uzskaitījumu tipiem:</span><span class="sxs-lookup"><span data-stu-id="96ca1-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="96ca1-111">Elektronisko pārskatu (ER) modeļu uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="96ca1-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="96ca1-112">ER formāta uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="96ca1-112">ER format enumeration</span></span>
- <span data-ttu-id="96ca1-113">Microsoft Dynamics 365 Finance uzskaitījums</span><span class="sxs-lookup"><span data-stu-id="96ca1-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="96ca1-114">`enumeration value text`: *Virkne*</span><span class="sxs-lookup"><span data-stu-id="96ca1-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="96ca1-115">Virknes vērtība, kas apzīmē vienas uzskaitījuma vērtības nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="96ca1-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="96ca1-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="96ca1-116">Return values</span></span>

<span data-ttu-id="96ca1-117">Nullējama *Enum*</span><span class="sxs-lookup"><span data-stu-id="96ca1-117">Nullable *Enum*</span></span>

<span data-ttu-id="96ca1-118">Iegūtā uzskaitījuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="96ca1-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="96ca1-119">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="96ca1-119">Usage notes</span></span>

<span data-ttu-id="96ca1-120">Netiek rādīts izņēmums, ja *Enum* vērtība nav atrasta, izmantojot uzskaitījuma vērtības nosaukumu, kas ir norādīts kā *Virknes* vērtība.</span><span class="sxs-lookup"><span data-stu-id="96ca1-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="96ca1-121">Paraugs</span><span class="sxs-lookup"><span data-stu-id="96ca1-121">Example</span></span>

<span data-ttu-id="96ca1-122">Tālāk esošajā attēlā ir parādīts datu modelī ieviests uzskaitījums **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="96ca1-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="96ca1-123">Ņemiet vērā, ka etiķetes ir definētas uzskaitījumu vērtībām.</span><span class="sxs-lookup"><span data-stu-id="96ca1-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="96ca1-124">Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.</span><span class="sxs-lookup"><span data-stu-id="96ca1-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="96ca1-125">**$Direction** datu avots ir konfigurēts ER pārskatā.</span><span class="sxs-lookup"><span data-stu-id="96ca1-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="96ca1-126">Šis datu avots ir konfigurēts, pamatojoties uz modeļa uzskaitījumu **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="96ca1-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="96ca1-127">Izteiksme `$IsArrivals` ir izveidota ar mērķi lietot modeļa uzskaitījumā bāzētu datu avotu **$Direction** kā šīs funkcijas parametru.</span><span class="sxs-lookup"><span data-stu-id="96ca1-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="96ca1-128">Šīs salīdzinājuma izteiksmes vērtība ir **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="96ca1-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="96ca1-129">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="96ca1-129">Additional resources</span></span>

[<span data-ttu-id="96ca1-130">Teksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="96ca1-130">Text functions</span></span>](er-functions-category-text.md)
