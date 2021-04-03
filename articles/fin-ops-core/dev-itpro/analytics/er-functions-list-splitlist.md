---
title: SPLITLIST ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SPLITLIST elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559142"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="484a5-103">SPLITLIST ER funkcija</span><span class="sxs-lookup"><span data-stu-id="484a5-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="484a5-104">`SPLITLIST` funkcija sadala norādīto sarakstu apakšsarakstos (jeb partijās), kuri katrs satur norādītu ierakstu skaitu.</span><span class="sxs-lookup"><span data-stu-id="484a5-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="484a5-105">Pēc tam tā atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību, kas sastāv no partijām.</span><span class="sxs-lookup"><span data-stu-id="484a5-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="484a5-106">Sintakse</span><span class="sxs-lookup"><span data-stu-id="484a5-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="484a5-107">Argumenti</span><span class="sxs-lookup"><span data-stu-id="484a5-107">Arguments</span></span>

<span data-ttu-id="484a5-108">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="484a5-108">`list`: *Record list*</span></span>

<span data-ttu-id="484a5-109">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="484a5-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="484a5-110">`number`: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="484a5-110">`number`: *Integer*</span></span>

<span data-ttu-id="484a5-111">Maksimālais ierakstu skaits partijā.</span><span class="sxs-lookup"><span data-stu-id="484a5-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="484a5-112">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="484a5-112">Return values</span></span>

<span data-ttu-id="484a5-113">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="484a5-113">*Record list*</span></span>

<span data-ttu-id="484a5-114">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="484a5-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="484a5-115">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="484a5-115">Usage notes</span></span>

<span data-ttu-id="484a5-116">Atgriezts partiju saraksts satur šādus elementus:</span><span class="sxs-lookup"><span data-stu-id="484a5-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="484a5-117">**Vērtība:** *Saraksts*</span><span class="sxs-lookup"><span data-stu-id="484a5-117">**Value:** *List*</span></span>

    <span data-ttu-id="484a5-118">To ierakstu saraksts, kas pieder pašreizējai partijai.</span><span class="sxs-lookup"><span data-stu-id="484a5-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="484a5-119">**BatchNumber:** *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="484a5-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="484a5-120">Pašreizējās partijas numurs atgrieztajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="484a5-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="484a5-121">Paraugs</span><span class="sxs-lookup"><span data-stu-id="484a5-121">Example</span></span>

<span data-ttu-id="484a5-122">Tālāk esošajā attēlā redzamais datu avots **Rindas** tiek izveidots kā ierakstu saraksts, kuram ir trīs ieraksti.</span><span class="sxs-lookup"><span data-stu-id="484a5-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="484a5-123">Šis saraksts tiek sadalīts divās partijās — katrā no partijām ir līdz diviem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="484a5-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="484a5-124">Tālāk esošajā attēlā parādīts izveidotā formāta izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="484a5-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="484a5-125">Šajā formāta izkārtojumā saistījumi ar datu avotu **Lines** tiek izveidoti, lai ģenerētu izvadi XML formātā</span><span class="sxs-lookup"><span data-stu-id="484a5-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="484a5-126">Šajā izvadē ietverti atsevišķi mezgli katrai partijai un tajā esošajiem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="484a5-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="484a5-127">Tālāk esošajā attēlā parādīts rezultāts pēc izveidotā formāta palaišanas.</span><span class="sxs-lookup"><span data-stu-id="484a5-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="484a5-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="484a5-128">Additional resources</span></span>

[<span data-ttu-id="484a5-129">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="484a5-129">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]