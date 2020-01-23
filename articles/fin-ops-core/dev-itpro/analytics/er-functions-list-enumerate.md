---
title: ENUMERATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ENUMERATE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: f0a1c83ee869810e816b6d32ea890d172d2910e5
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916227"
---
# <span data-ttu-id="9affc-103"><a name="ENUMERATE">ENUMERATE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="9affc-103"><a name="ENUMERATE">ENUMERATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9affc-104">`ENUMERATE` funkcija atgriež jaunu *Ierakstu saraksta* vērtību, kas sastāv no uzskaitījumā norādītājiem saraksta ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="9affc-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9affc-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="9affc-105">Syntax</span></span>

```
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="9affc-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="9affc-106">Arguments</span></span>

<span data-ttu-id="9affc-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="9affc-107">`list`: *Record list*</span></span>

<span data-ttu-id="9affc-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="9affc-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9affc-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="9affc-109">Return values</span></span>

<span data-ttu-id="9affc-110">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="9affc-110">*Record list*</span></span>

<span data-ttu-id="9affc-111">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="9affc-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9affc-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="9affc-112">Usage notes</span></span>

<span data-ttu-id="9affc-113">Saraksts ar uzskaitītajiem atgrieztajiem ierakstiem parāda šādus papildu elementus:</span><span class="sxs-lookup"><span data-stu-id="9affc-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="9affc-114">Lauku ieraksts (komponents **Vērtība**)</span><span class="sxs-lookup"><span data-stu-id="9affc-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="9affc-115">Pašreizējā ieraksta indekss (komponents **Number**)</span><span class="sxs-lookup"><span data-stu-id="9affc-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="9affc-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="9affc-116">Example</span></span>

<span data-ttu-id="9affc-117">Tālāk esošajā attēlā datu avots **Enumerated** tiek izveidots kā uzskaitījuma kreditoru ierakstu saraksts no datu avota **Vendors**, kas atsaucas uz tabulu VendTable.</span><span class="sxs-lookup"><span data-stu-id="9affc-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="9affc-118">Šajā attēlā ir parādīta elektronisko pārskatu (ER) formāts.</span><span class="sxs-lookup"><span data-stu-id="9affc-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="9affc-119">Šajā formātā tiek izveidoti saistījumi, lai ģenerētu izvadi XML formātā</span><span class="sxs-lookup"><span data-stu-id="9affc-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="9affc-120">Šajā izvadē atsevišķi kreditori attēloti kā uzskaitījuma mezgli.</span><span class="sxs-lookup"><span data-stu-id="9affc-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="9affc-121">Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</span><span class="sxs-lookup"><span data-stu-id="9affc-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="9affc-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9affc-122">Additional resources</span></span>

[<span data-ttu-id="9affc-123">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="9affc-123">List functions</span></span>](er-functions-category-list.md)
