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
ms.openlocfilehash: e1871ee41267c2c0e8b35007a47c9601079f05d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745253"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="1db62-103">ENUMERATE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="1db62-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1db62-104">`ENUMERATE` funkcija atgriež jaunu *Ierakstu saraksta* vērtību, kas sastāv no uzskaitījumā norādītājiem saraksta ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="1db62-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db62-105">Sintakse</span><span class="sxs-lookup"><span data-stu-id="1db62-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="1db62-106">Argumenti</span><span class="sxs-lookup"><span data-stu-id="1db62-106">Arguments</span></span>

<span data-ttu-id="1db62-107">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="1db62-107">`list`: *Record list*</span></span>

<span data-ttu-id="1db62-108">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="1db62-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1db62-109">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="1db62-109">Return values</span></span>

<span data-ttu-id="1db62-110">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="1db62-110">*Record list*</span></span>

<span data-ttu-id="1db62-111">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="1db62-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1db62-112">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="1db62-112">Usage notes</span></span>

<span data-ttu-id="1db62-113">Saraksts ar uzskaitītajiem atgrieztajiem ierakstiem parāda šādus papildu elementus:</span><span class="sxs-lookup"><span data-stu-id="1db62-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="1db62-114">Lauku ieraksts (**Vērtība** komponents)</span><span class="sxs-lookup"><span data-stu-id="1db62-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="1db62-115">Pašreizējā ieraksta indekss (**Number** komponents)</span><span class="sxs-lookup"><span data-stu-id="1db62-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="1db62-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="1db62-116">Example</span></span>

<span data-ttu-id="1db62-117">Tālāk esošajā attēlā datu avots **Enumerated** tiek izveidots kā uzskaitījuma kreditoru ierakstu saraksts no datu avota **Vendors**, kas atsaucas uz tabulu VendTable.</span><span class="sxs-lookup"><span data-stu-id="1db62-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="1db62-118">Šajā attēlā ir parādīta elektronisko pārskatu (ER) formāts.</span><span class="sxs-lookup"><span data-stu-id="1db62-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="1db62-119">Šajā formātā tiek izveidoti saistījumi, lai ģenerētu izvadi XML formātā</span><span class="sxs-lookup"><span data-stu-id="1db62-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="1db62-120">Šajā izvadē atsevišķi kreditori attēloti kā uzskaitījuma mezgli.</span><span class="sxs-lookup"><span data-stu-id="1db62-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="1db62-121">Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</span><span class="sxs-lookup"><span data-stu-id="1db62-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="1db62-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1db62-122">Additional resources</span></span>

[<span data-ttu-id="1db62-123">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="1db62-123">List functions</span></span>](er-functions-category-list.md)
