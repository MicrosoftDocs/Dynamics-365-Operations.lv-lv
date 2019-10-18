---
title: Seguma iestatījumi
description: Šajā tēmā ir sniegta informācija par vajadzību iestatījumiem, kurus vispārējā plānošana izmanto, lai aprēķinātu krājumu vajadzības.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a63184852751bb65fb7e80d721f8c48fd847609
ms.sourcegitcommit: edfd805356894710488ce07cb1c89313f448b222
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2019
ms.locfileid: "1998975"
---
# <a name="coverage-settings"></a><span data-ttu-id="a12e2-103">Seguma iestatījumi</span><span class="sxs-lookup"><span data-stu-id="a12e2-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a12e2-104">Vispārējā plānošana izmanto vajadzības iestatījumus, lai aprēķinātu krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="a12e2-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="a12e2-105">Jūs varat norādīt vajadzības iestatījumus vairākos veidos:</span><span class="sxs-lookup"><span data-stu-id="a12e2-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="a12e2-106">Norādiet vajadzību grupas vajadzības iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="a12e2-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="a12e2-107">Varat izveidot vajadzību grupu, kas satur iestatījumus visām precēm, kuras ir saistītas ar šo vajadzību grupu.</span><span class="sxs-lookup"><span data-stu-id="a12e2-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="a12e2-108">Lai izveidotu seguma grupu, noklikšķiniet uz **Vispārējā plānošana &gt; Iestatīšana &gt; Vajadzība &gt; Vajadzības grupas**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="a12e2-109">Vajadzību grupu varat saistīt ar preci.</span><span class="sxs-lookup"><span data-stu-id="a12e2-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="a12e2-110">Ja saite attiecas uz noteiktu vietu, noliktavu vai preces dimensiju, izmantojiet lauku **Vajadzības grupa** lapā **Krājumu vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="a12e2-111">Ja saite ir vispārīga un nav atkarīga no preču dimensijām, izmantojiet lauku **Vajadzības grupa** lapas **Detalizēta informācija par preci** FastTab cilnē **Plāns**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="a12e2-112">Ja vajadzību grupa netiek saistīta ar preci, vispārējai plānošanai pēc noklusējuma tiek izmantota vispārējā vajadzību grupa, kas ir norādīta lapā **Vispārējās plānošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="a12e2-113">Norādiet preces vajadzības iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="a12e2-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="a12e2-114">Varat izveidot vajadzību iestatījumus noteiktai precei.</span><span class="sxs-lookup"><span data-stu-id="a12e2-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="a12e2-115">Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="a12e2-116">Atlasiet preci un pēc tam lapas sadaļā Darbību rūts, cilnē **Plāns**, grupā **Vajadzība** noklikšķiniet uz **Krājumu vajadzība** , lai atvērtu lapu **Krājumu vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="a12e2-117">Ja prece jau ir saistīta ar vajadzību grupu, varat ignorēt vajadzību grupas iestatījumus, izmantojot lauku **Ignorēt**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="a12e2-118">Vajadzības iestatījumiem lapā **Krājumu vajadzība** ir augstāka prioritāte nekā iestatījumiem lapā **Vajadzības grupa**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="a12e2-119">Norādiet preces vajadzības iestatījumus, izmantojot vedni.</span><span class="sxs-lookup"><span data-stu-id="a12e2-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="a12e2-120">Vednī soli pa solim ir izskaidrots primāro krājumu vajadzību parametru iestatīšanas process.</span><span class="sxs-lookup"><span data-stu-id="a12e2-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="a12e2-121">Lapas **Krājumu vajadzība** darbību rūtī noklikšķiniet uz **Vednis**, lai atvērtu sadaļu **Krājumu vajadzību vednis**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="a12e2-122">Norādiet dimensiju grupas vajadzības iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="a12e2-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="a12e2-123">Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="a12e2-124">Lapas **Detalizēta informācija par izlaistajām precēm** FasTab cilnes **Vispārīgi** sadaļā **Administrēšana** atlasiet saiti laukā **Noliktavas izmēru grupa**.</span><span class="sxs-lookup"><span data-stu-id="a12e2-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="a12e2-125">Lapā **Noliktavas dimensiju grupas** atlasiet izvēles rūtiņu **Vajadzības plāns pa dimensijām**, lai izveidotu vajadzības iestatījumus dimensijai noliktavas dimensiju grupā.</span><span class="sxs-lookup"><span data-stu-id="a12e2-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="a12e2-126">Lauks **Vajadzības plāns pa dimensijām** ir jāatlasa visām preces dimensijām, piemēram, konfigurācijai, krāsai, izmēram un stilam.</span><span class="sxs-lookup"><span data-stu-id="a12e2-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="a12e2-127">Vajadzības kodi</span><span class="sxs-lookup"><span data-stu-id="a12e2-127">Coverage codes</span></span>

<span data-ttu-id="a12e2-128">Vispārējo plānošanu var konfigurēt tā, lai izmantotu dažādas papildināšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="a12e2-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="a12e2-129">Papildināšanas metodes vai laidiena lieluma metodes ir metodes, ko sistēma izmanto, lai noteiktu partijas lielumu nopirktajiem vai saražotajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="a12e2-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="a12e2-130">Katrai papildināšanas metodei ir piešķirts viens no šiem vajadzības kodiem:</span><span class="sxs-lookup"><span data-stu-id="a12e2-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="a12e2-131">**Manuāla** – laidiena lieluma metode, kad sistēma neiesaka krājumam Pirkšanas, pārsūtīšanas vai ražošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="a12e2-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="a12e2-132">Krājuma plānotājs būs atbildīgs par krājuma papildināšanai nepieciešamo pasūtījumu izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="a12e2-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="a12e2-133">**Pēc vajadzības** – laidiena lieluma metode, saskaņā ar kuru sistēma izveido plānoto pirkšanas, pārsūtīšanas vai ražošanas pasūtījumu krājuma vajadzībai.</span><span class="sxs-lookup"><span data-stu-id="a12e2-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="a12e2-134">Parasti tas tiek izmantots dārgiem krājumiem ar neregulāro pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="a12e2-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="a12e2-135">**Pa periodiem** – laidiena lieluma metode, kas apvieno visu perioda pieprasījumu vienā pasūtījumā šim krājumam.</span><span class="sxs-lookup"><span data-stu-id="a12e2-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="a12e2-136">Pasūtījums tiks plānots pirmajai perioda dienai, un tā daudzums atbilstīs neto prasībām noteiktajā periodā.</span><span class="sxs-lookup"><span data-stu-id="a12e2-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="a12e2-137">Periods sākas ar krājuma pirmo pieprasījumu un sedz noteikto laika periodu.</span><span class="sxs-lookup"><span data-stu-id="a12e2-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="a12e2-138">Nākamais periods sāksies ar nākamā krājuma prasībām.</span><span class="sxs-lookup"><span data-stu-id="a12e2-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="a12e2-139">**Min/max** — laidiena lieluma metode, kas ietver krājumu papildināšanu līdz noteiktam līmenim, ja paredzētais rīcībā esošais daudzums ir mazāks par noteikto slieksni.</span><span class="sxs-lookup"><span data-stu-id="a12e2-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="a12e2-140">Papildināšanas daudzums būs vienāds ar starpību starp maksimālo līmeni un prognozēto rīcībā esošo līmeni.</span><span class="sxs-lookup"><span data-stu-id="a12e2-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a12e2-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a12e2-141">Additional resources</span></span>

[<span data-ttu-id="a12e2-142">Vispārējie plāni</span><span class="sxs-lookup"><span data-stu-id="a12e2-142">Master plans</span></span>](master-plans.md)
