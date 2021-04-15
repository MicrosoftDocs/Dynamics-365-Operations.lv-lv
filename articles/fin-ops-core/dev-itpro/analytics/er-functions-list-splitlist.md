---
title: SPLITLIST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SPLITLIST elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745573"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="1e783-103">SPLITLIST ER funkcija</span><span class="sxs-lookup"><span data-stu-id="1e783-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e783-104">`SPLITLIST` funkcija sadala norādīto sarakstu apakšsarakstos (jeb partijās), kuri katrs satur norādītu ierakstu skaitu.</span><span class="sxs-lookup"><span data-stu-id="1e783-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="1e783-105">Pēc tam tā atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību, kas sastāv no partijām.</span><span class="sxs-lookup"><span data-stu-id="1e783-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1e783-106">Sintakse 1</span><span class="sxs-lookup"><span data-stu-id="1e783-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="1e783-107">Sintakse 2</span><span class="sxs-lookup"><span data-stu-id="1e783-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="1e783-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="1e783-108">Arguments</span></span>

<span data-ttu-id="1e783-109">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="1e783-109">`list`: *Record list*</span></span>

<span data-ttu-id="1e783-110">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="1e783-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="1e783-111">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="1e783-111">`number`: *Integer*</span></span>

<span data-ttu-id="1e783-112">Maksimālais ierakstu skaits partijā.</span><span class="sxs-lookup"><span data-stu-id="1e783-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="1e783-113">`on-demand reading flag`: *Būla*</span><span class="sxs-lookup"><span data-stu-id="1e783-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="1e783-114">Vērtība *Būla*, kas norāda, vai pēc pieprasījuma jāģenerē apakšsarakstu elementi.</span><span class="sxs-lookup"><span data-stu-id="1e783-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e783-115">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="1e783-115">Return values</span></span>

<span data-ttu-id="1e783-116">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="1e783-116">*Record list*</span></span>

<span data-ttu-id="1e783-117">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="1e783-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1e783-118">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="1e783-118">Usage notes</span></span>

<span data-ttu-id="1e783-119">Atgriezts partiju saraksts satur šādus elementus:</span><span class="sxs-lookup"><span data-stu-id="1e783-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="1e783-120">**Vērtība:** *Saraksts*</span><span class="sxs-lookup"><span data-stu-id="1e783-120">**Value:** *List*</span></span>

    <span data-ttu-id="1e783-121">To ierakstu saraksts, kas pieder pašreizējai partijai.</span><span class="sxs-lookup"><span data-stu-id="1e783-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="1e783-122">**BatchNumber:** *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="1e783-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="1e783-123">Pašreizējās partijas numurs atgrieztajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="1e783-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="1e783-124">Ja lasīšanas karodziņš pēc pieprasījuma ir iestatīts uz **Patiess**, pēc pieprasījuma tiek ģenerēti apakšsaraksti, kas ļauj samazināt atmiņas patēriņu, bet var izraisīt veiktspējas samazināšanos, ja elementi netiek izmantoti secīgi.</span><span class="sxs-lookup"><span data-stu-id="1e783-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="1e783-125">Paraugs</span><span class="sxs-lookup"><span data-stu-id="1e783-125">Example</span></span>

<span data-ttu-id="1e783-126">Tālāk esošajā attēlā redzamais datu avots **Rindas** tiek izveidots kā ierakstu saraksts, kuram ir trīs ieraksti.</span><span class="sxs-lookup"><span data-stu-id="1e783-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="1e783-127">Šis saraksts tiek sadalīts divās partijās — katrā no partijām ir līdz diviem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="1e783-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="1e783-128">Tālāk esošajā attēlā parādīts izveidotā formāta izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="1e783-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="1e783-129">Šajā formāta izkārtojumā saistījumi ar datu avotu **Lines** tiek izveidoti, lai ģenerētu izvadi XML formātā</span><span class="sxs-lookup"><span data-stu-id="1e783-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="1e783-130">Šajā izvadē ietverti atsevišķi mezgli katrai partijai un tajā esošajiem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="1e783-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="1e783-131">Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</span><span class="sxs-lookup"><span data-stu-id="1e783-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="1e783-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1e783-132">Additional resources</span></span>

[<span data-ttu-id="1e783-133">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="1e783-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
