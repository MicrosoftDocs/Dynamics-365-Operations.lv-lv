---
title: SPLITLISTBYLIMIT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SPLITLISTBYLIMIT elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 54c78f36c93e1bdb472b84fc7ca6428d20088bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041864"
---
# <span data-ttu-id="f1cae-103"><a name="SPLITLISTBYLIMIT">SPLITLISTBYLIMIT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="f1cae-103"><a name="SPLITLISTBYLIMIT">SPLITLISTBYLIMIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1cae-104">`SPLITLISTBYLIMIT` funkcija sadala norādīto sarakstu jaunā apakšsaraksta (partiju) sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f1cae-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="f1cae-105">Katras partijas ierakstu skaits tiek aprēķināts dinamiski.</span><span class="sxs-lookup"><span data-stu-id="f1cae-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="f1cae-106">Pēc tam funkcija atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību, kas sastāv no partijām.</span><span class="sxs-lookup"><span data-stu-id="f1cae-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1cae-107">Sintakse</span><span class="sxs-lookup"><span data-stu-id="f1cae-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="f1cae-108">Argumenti</span><span class="sxs-lookup"><span data-stu-id="f1cae-108">Arguments</span></span>

<span data-ttu-id="f1cae-109">`list`: *Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="f1cae-109">`list`: *Record list*</span></span>

<span data-ttu-id="f1cae-110">*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.</span><span class="sxs-lookup"><span data-stu-id="f1cae-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f1cae-111">`limit value`: *Vesels skaitlis* vai *Reāls*</span><span class="sxs-lookup"><span data-stu-id="f1cae-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="f1cae-112">Maksimālā robežvērtība, kas tiek izmantota, lai sadalītu sākotnējo sarakstu partijās.</span><span class="sxs-lookup"><span data-stu-id="f1cae-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="f1cae-113">`limit source`: *Lauks*</span><span class="sxs-lookup"><span data-stu-id="f1cae-113">`limit source`: *Field*</span></span>

<span data-ttu-id="f1cae-114">Derīgs ceļš laukam no veida *Vesels skaitlis* vai *Reāls* norādītajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f1cae-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="f1cae-115">Šī lauka vērtība nosaka darbību, kurā tiek palielināta kopējā summa.</span><span class="sxs-lookup"><span data-stu-id="f1cae-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="f1cae-116">Atgrieztās vērtības</span><span class="sxs-lookup"><span data-stu-id="f1cae-116">Return values</span></span>

<span data-ttu-id="f1cae-117">*Ierakstu saraksts*</span><span class="sxs-lookup"><span data-stu-id="f1cae-117">*Record list*</span></span>

<span data-ttu-id="f1cae-118">Iegūtais ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="f1cae-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f1cae-119">Lietošanas piezīmes</span><span class="sxs-lookup"><span data-stu-id="f1cae-119">Usage notes</span></span>

<span data-ttu-id="f1cae-120">Atgriezts partiju saraksts satur šādus elementus:</span><span class="sxs-lookup"><span data-stu-id="f1cae-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="f1cae-121">**Vērtība:**: *Saraksts*</span><span class="sxs-lookup"><span data-stu-id="f1cae-121">**Value**: *List*</span></span>

    <span data-ttu-id="f1cae-122">To ierakstu saraksts, kas pieder pašreizējai partijai.</span><span class="sxs-lookup"><span data-stu-id="f1cae-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="f1cae-123">**BatchNumber**: *Vesels skaitlis*</span><span class="sxs-lookup"><span data-stu-id="f1cae-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="f1cae-124">Pašreizējās partijas numurs atgrieztajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f1cae-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="f1cae-125">Ierobežojums netiek lietots atsevišķam vienumam attiecīgajā sarakstā, ja ierobežojuma avots pārsniedz definēto ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="f1cae-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="f1cae-126">Paraugs</span><span class="sxs-lookup"><span data-stu-id="f1cae-126">Example</span></span>

<span data-ttu-id="f1cae-127">Šajā attēlā ir parādīts elektronisko pārskatu (ER) formāts.</span><span class="sxs-lookup"><span data-stu-id="f1cae-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="f1cae-128">Nākamajā attēlā ir parādīti datu avoti, kas tiek izmantoti šim formātam.</span><span class="sxs-lookup"><span data-stu-id="f1cae-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="f1cae-129">Tālāk esošajā attēlā parādīts rezultāts pēc formāta palaišanas.</span><span class="sxs-lookup"><span data-stu-id="f1cae-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="f1cae-130">Šajā gadījumā izvade ir nekārtots preču saraksts.</span><span class="sxs-lookup"><span data-stu-id="f1cae-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="f1cae-131">Nākamajos attēlos tas pats formāts ir pielāgots tā, lai preču sarakstu rādītu pa partijām, ja vienā partijā jāietver preces un nevar pārsniegt kopējā svara ierobežojumu 9.</span><span class="sxs-lookup"><span data-stu-id="f1cae-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="f1cae-132">Tālāk esošajā attēlā parādīts rezultāts pēc pielāgotā formāta palaišanas.</span><span class="sxs-lookup"><span data-stu-id="f1cae-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="f1cae-133">Ierobežojums netiek lietots pēdējam sākotnējā saraksta vienumam, jo ierobežojuma avota (**svara**) vērtība (**11**) pārsniedz noteikto ierobežojumu (**9**).</span><span class="sxs-lookup"><span data-stu-id="f1cae-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="f1cae-134">Lai pārskata ģenerēšanas laikā ignorētu apakšsarakstus, izmantojiet vai nu funkciju `WHERE`, vai izteiksmi **Iespējots** no atbildstošā formāta elementa pēc jūsu nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="f1cae-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1cae-135">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f1cae-135">Additional resources</span></span>

[<span data-ttu-id="f1cae-136">Saraksta funkcijas</span><span class="sxs-lookup"><span data-stu-id="f1cae-136">List functions</span></span>](er-functions-category-list.md)
