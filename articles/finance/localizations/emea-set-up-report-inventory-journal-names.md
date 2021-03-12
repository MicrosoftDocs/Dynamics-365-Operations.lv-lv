---
title: Krājumu žurnāla pārskati
description: Kad lietojat konfigurējamus krājumu pārskatus, kuru pamatā ir elektronisko pārskatu veidošana, ir nepieciešams iestatīt attiecības starp konkrētu pārskatu un žurnāla tipu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalName
audience: Application User
ms.reviewer: kfend
ms.custom: 265144
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4345ec1388a369e9ffc8d01b4f5153e5478fd723
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002846"
---
# <a name="inventory-journal-reports"></a><span data-ttu-id="f6297-103">Krājumu žurnāla pārskati</span><span class="sxs-lookup"><span data-stu-id="f6297-103">Inventory journal reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6297-104">Kad lietojat konfigurējamus krājumu pārskatus, kuru pamatā ir elektronisko pārskatu veidošana, ir nepieciešams iestatīt attiecības starp konkrētu pārskatu un žurnāla tipu.</span><span class="sxs-lookup"><span data-stu-id="f6297-104">When you use configurable inventory reports based on electronic reporting, you need to set up a relationship between a specific report and a journal type.</span></span>

<span data-ttu-id="f6297-105">Lai iestatītu attiecības starp konkrētu pārskatu un kādu žurnāla tipu, lapā **Krājumu žurnālu nosaukumi** (**Krājumu vadība** &gt; **Iestatīšana** &gt; **Žurnālu nosaukumi** &gt; **Krājumi**) ievadiet šī pārskata nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f6297-105">To set up a relationship between a specific report and a journal type, on the **Inventory journal names** page (**Inventory management** &gt; **Setup** &gt; **Journal names** &gt; **Inventory**), enter a name for the report.</span></span> <span data-ttu-id="f6297-106">**Piezīme.** Lai iestatītu atbalstītās konfigurācijas, lejupielādējiet nepieciešamās elektronisko pārskatu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="f6297-106">**Note:** To set up supported configurations, download the required electronic reporting configurations.</span></span> <span data-ttu-id="f6297-107">Papildinformāciju skatiet rakstā [Lejupielādēt elektronisko pārskatu konfigurācijas no Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="f6297-107">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span> <span data-ttu-id="f6297-108">Nākamajā tabulā ir uzskaitīti krājumu pārskatu piemēri ar Eiropā atbalstītām konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="f6297-108">Examples of inventory reports with supported configurations in Europe are listed in the following table.</span></span>

| <span data-ttu-id="f6297-109">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="f6297-109">Country</span></span>            |    <span data-ttu-id="f6297-110">Pārskata apraksts</span><span class="sxs-lookup"><span data-stu-id="f6297-110">Report description</span></span>               | <span data-ttu-id="f6297-111">Žurnāla tips</span><span class="sxs-lookup"><span data-stu-id="f6297-111">Journal type</span></span>     |    <span data-ttu-id="f6297-112">Formāta kartēšanas nosaukums</span><span class="sxs-lookup"><span data-stu-id="f6297-112">Format mapping name</span></span>                  |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| <span data-ttu-id="f6297-113">Lietuva, Ungārija</span><span class="sxs-lookup"><span data-stu-id="f6297-113">Lithuania, Hungary</span></span> | <span data-ttu-id="f6297-114">Inventarizācijas akta pārskats</span><span class="sxs-lookup"><span data-stu-id="f6297-114">Inventory statement report</span></span>          | <span data-ttu-id="f6297-115">Inventarizācija</span><span class="sxs-lookup"><span data-stu-id="f6297-115">Counting</span></span>         | <span data-ttu-id="f6297-116">Inventarizācijas akts (HU, LT)</span><span class="sxs-lookup"><span data-stu-id="f6297-116">Inventory statement (HU, LT)</span></span>            |
| <span data-ttu-id="f6297-117">Latvija, Polija</span><span class="sxs-lookup"><span data-stu-id="f6297-117">Latvia, Poland</span></span>     | <span data-ttu-id="f6297-118">Krājumu pārklasificēšanas dokuments</span><span class="sxs-lookup"><span data-stu-id="f6297-118">Inventory reclassification document</span></span> | <span data-ttu-id="f6297-119">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="f6297-119">Transfer</span></span>         | <span data-ttu-id="f6297-120">InventoryReclassificationDocument\_PLLV</span><span class="sxs-lookup"><span data-stu-id="f6297-120">InventoryReclassificationDocument\_PLLV</span></span> |
| <span data-ttu-id="f6297-121">Igaunija</span><span class="sxs-lookup"><span data-stu-id="f6297-121">Estonia</span></span>            | <span data-ttu-id="f6297-122">Krājumu pārklasificēšanas dokuments</span><span class="sxs-lookup"><span data-stu-id="f6297-122">Inventory reclassification document</span></span> | <span data-ttu-id="f6297-123">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="f6297-123">Transfer</span></span>         | <span data-ttu-id="f6297-124">InventoryReclassificationDocument\_EE</span><span class="sxs-lookup"><span data-stu-id="f6297-124">InventoryReclassificationDocument\_EE</span></span>   |
| <span data-ttu-id="f6297-125">Polija</span><span class="sxs-lookup"><span data-stu-id="f6297-125">Poland</span></span>             | <span data-ttu-id="f6297-126">Iekšējais PW/RW</span><span class="sxs-lookup"><span data-stu-id="f6297-126">Internal PW/RW</span></span>                      | <span data-ttu-id="f6297-127">Kustība</span><span class="sxs-lookup"><span data-stu-id="f6297-127">Movement</span></span>         | <span data-ttu-id="f6297-128">InventJournalLinesDocPL</span><span class="sxs-lookup"><span data-stu-id="f6297-128">InventJournalLinesDocPL</span></span>                 |
| <span data-ttu-id="f6297-129">Latvija</span><span class="sxs-lookup"><span data-stu-id="f6297-129">Latvia</span></span>             | <span data-ttu-id="f6297-130">Krājumu kustības dokuments</span><span class="sxs-lookup"><span data-stu-id="f6297-130">Inventory movement document</span></span>         | <span data-ttu-id="f6297-131">Kustība</span><span class="sxs-lookup"><span data-stu-id="f6297-131">Movement</span></span>         | <span data-ttu-id="f6297-132">Kustība\_LV</span><span class="sxs-lookup"><span data-stu-id="f6297-132">Movement\_LV</span></span>                            |
| <span data-ttu-id="f6297-133">Latvija</span><span class="sxs-lookup"><span data-stu-id="f6297-133">Latvia</span></span>             | <span data-ttu-id="f6297-134">Krājumu norakstīšanas dokuments</span><span class="sxs-lookup"><span data-stu-id="f6297-134">Inventory write-down document</span></span>       | <span data-ttu-id="f6297-135">Pielāgojums</span><span class="sxs-lookup"><span data-stu-id="f6297-135">Adjustment</span></span>       | <span data-ttu-id="f6297-136">InventJournalLines\_LV</span><span class="sxs-lookup"><span data-stu-id="f6297-136">InventJournalLines\_LV</span></span>                  |
| <span data-ttu-id="f6297-137">Latvija</span><span class="sxs-lookup"><span data-stu-id="f6297-137">Latvia</span></span>             | <span data-ttu-id="f6297-138">Pārvietojuma pavadzīme</span><span class="sxs-lookup"><span data-stu-id="f6297-138">Transfer delivery note</span></span>              | <span data-ttu-id="f6297-139">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="f6297-139">Transfer</span></span>         | <span data-ttu-id="f6297-140">InternalTransferDeliveryNote\_LV</span><span class="sxs-lookup"><span data-stu-id="f6297-140">InternalTransferDeliveryNote\_LV</span></span>        |
| <span data-ttu-id="f6297-141">Latvija</span><span class="sxs-lookup"><span data-stu-id="f6297-141">Latvia</span></span>             | <span data-ttu-id="f6297-142">Uzskaitīšanas dokumenta pārskats</span><span class="sxs-lookup"><span data-stu-id="f6297-142">Counting document report</span></span>            | <span data-ttu-id="f6297-143">Inventarizācija</span><span class="sxs-lookup"><span data-stu-id="f6297-143">Counting</span></span>         | <span data-ttu-id="f6297-144">CountedDocument\_LV</span><span class="sxs-lookup"><span data-stu-id="f6297-144">CountedDocument\_LV</span></span>                     |
| <span data-ttu-id="f6297-145">Latvija</span><span class="sxs-lookup"><span data-stu-id="f6297-145">Latvia</span></span>             | <span data-ttu-id="f6297-146">Inventarizācijas saraksta pārskats</span><span class="sxs-lookup"><span data-stu-id="f6297-146">Counting list report</span></span>                | <span data-ttu-id="f6297-147">Inventarizācija</span><span class="sxs-lookup"><span data-stu-id="f6297-147">Counting</span></span>         | <span data-ttu-id="f6297-148">Inventarizācijas saraksts</span><span class="sxs-lookup"><span data-stu-id="f6297-148">Counting list</span></span>                           |





