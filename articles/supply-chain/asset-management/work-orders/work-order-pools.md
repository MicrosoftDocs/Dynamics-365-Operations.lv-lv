---
title: Darba pasūtījumu kopas
description: Šajā tēmā ir aprakstīts, kā strādāt ar darba pasūtījuma kopām līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875778"
---
# <a name="work-order-pools"></a><span data-ttu-id="64860-103">Darba pasūtījumu kopas</span><span class="sxs-lookup"><span data-stu-id="64860-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="64860-104">Darba pasūtījumu kopas var izmantot, lai grupētu darba pasūtījumus, kuriem ir kaut kas kopīgs.</span><span class="sxs-lookup"><span data-stu-id="64860-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="64860-105">Piemēram, varat izveidot darba pasūtījumu kopas</span><span class="sxs-lookup"><span data-stu-id="64860-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="64860-106">darba komandām, piemēram, uzturēšanas komanda A, uzturēšanas komanda B</span><span class="sxs-lookup"><span data-stu-id="64860-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="64860-107">profesionālajām prasmēm, piemēram, elektriķi vai santehniķi</span><span class="sxs-lookup"><span data-stu-id="64860-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="64860-108">fiziskām atrašanās vietām</span><span class="sxs-lookup"><span data-stu-id="64860-108">physical locations</span></span>  

- <span data-ttu-id="64860-109">laika grafikiem, piemēram, nedēļas vai citi periodi</span><span class="sxs-lookup"><span data-stu-id="64860-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="64860-110">Ja nepieciešams, vienu darba pasūtījumu var ievietot daudzās darba pasūtījuma kopās.</span><span class="sxs-lookup"><span data-stu-id="64860-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="64860-111">Darba pasūtījumu kopas izveide</span><span class="sxs-lookup"><span data-stu-id="64860-111">Create work order pool</span></span>

<span data-ttu-id="64860-112">Sadaļās **Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījumu kopas** varat iegūt pārskatu par darba pasūtījuma kopām un izveidot jaunas kopas.</span><span class="sxs-lookup"><span data-stu-id="64860-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="64860-113">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumu kopas** > **Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījuma kopas**.</span><span class="sxs-lookup"><span data-stu-id="64860-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="64860-114">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="64860-114">Click **New**.</span></span>

3. <span data-ttu-id="64860-115">Ievadiet darba pasūtījumu kopas ID laukā **Kopa** un ievadiet tās nosaukumu laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="64860-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="64860-116">Atlasiet “Jā” pie pārslēgšanas pogas **Aktīva**, lai norādītu, ka darba pasūtījumu kopa ir aktīva.</span><span class="sxs-lookup"><span data-stu-id="64860-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="64860-117">Atlasiet “Jā” pie pārslēgšanas pogas **Dzēst visas darba pasūtījuma relācijas**, ja vēlaties, lai darba pasūtījumi tiktu automātiski noņemti no darba pasūtījumu kopas.</span><span class="sxs-lookup"><span data-stu-id="64860-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="64860-118">Laukā **Dzēst dzīves cikla stāvokli** atlasiet darba pasūtījuma dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="64860-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="64860-119">Piemēram, darba pasūtījuma dzīves cikla stāvoklis, lai pabeigtu darba pasūtījumu, var tikt iestatīts automātiski dzēst relācijas ar darba pasūtījuma kopām.</span><span class="sxs-lookup"><span data-stu-id="64860-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="64860-120">Varat uzreiz sākt pievienot darba pasūtījumus darba pasūtījumu kopai.</span><span class="sxs-lookup"><span data-stu-id="64860-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="64860-121">Kopsavilkuma cilnē **Darba pasūtījumi** noklikšķiniet uz **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="64860-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="64860-122">Atlasiet darba pasūtījumu laukā **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="64860-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="64860-123">Saistītie lauki tiek atjaunināti automātiski.</span><span class="sxs-lookup"><span data-stu-id="64860-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="64860-124">Atkārtojiet 7.–8. darbību, ja vēlaties pievienot papildu darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="64860-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="64860-125">Laukā **Kārtošanas secība** varat norādīt, vai darba pasūtījumi ir jāveic noteiktā secībā.</span><span class="sxs-lookup"><span data-stu-id="64860-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="64860-126">Ievietojiet skaitļus 1, 2, 3 un tā tālāk, lai norādītu noteiktu secību atlasītajiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="64860-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="64860-127">Noklikšķiniet uz pogas **Darba pasūtījumi**, lai skatītu sarakstu ar visiem darba pasūtījumiem, kas iekļauti darba pasūtījumu kopā.</span><span class="sxs-lookup"><span data-stu-id="64860-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="64860-128">Noklikšķiniet uz pogas **Noslodze**, lai atvērtu sadaļu **Noslodze**, lai aprēķinātu un skatītu noslodzi uzturēšanas grafikam, neplānotajiem darba pasūtījumiem un plānotajiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="64860-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="64860-129">Noklikšķiniet uz pogas **Krājumu prognoze**, lai atvērtu sadaļu **Krājumu prognoze**, lai aprēķinātu un skatītu krājumu (rezerves daļu un citu nepieciešamo krājumu) prognozes saistībā ar uzturēšanas grafiku, neplānotajiem darba pasūtījumiem un plānotajiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="64860-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="64860-130">Noklikšķiniet uz pogas **Darba pasūtījuma pirkšanas pieprasījums**, lai atvērtu sarakstu **Darba pasūtījuma pirkšanas pieprasījumi** un skatītu pirkšanas pieprasījumu sarakstu, kas saistīts ar darba pasūtījumiem darba pasūtījumu kopā.</span><span class="sxs-lookup"><span data-stu-id="64860-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="64860-131">Noklikšķiniet uz pogas **Darba pasūtījuma pirkšana**, lai atvērtu sarakstu **Darba pasūtījuma pirkšana** un skatītu pirkšanas pieprasījumus, kas saistīti ar darba pasūtījumiem darba pasūtījumu kopā.</span><span class="sxs-lookup"><span data-stu-id="64860-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="64860-132">Kad darba pasūtījumu kopa jūsu darba plānošanai vairs nav atbilstoša, iestatiet izvēles rūtiņu **Aktīva** uz “Nē” saraksta skatā **Darba pasūtījumu kopas**.</span><span class="sxs-lookup"><span data-stu-id="64860-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="64860-133">Ja vēlaties dzēst visas darba pasūtījumu rindas, atzīmējiet izvēles rūtiņu **Dzēst darba pasūtījumu relācijas**, piemēram, lai izveidotu tukšu kopu, ko vēlāk var izmantot citiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="64860-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="64860-134">Atcerieties noņemt izvēles rūtiņu **Dzēst darba pasūtījuma attiecības**, ja vēlaties izmantot darba pasūtījuma kopu, lai vēlāk izveidotu jaunas darba pasūtījuma attiecības.</span><span class="sxs-lookup"><span data-stu-id="64860-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![1. attēls](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="64860-136">Darba pasūtījuma pievienošana darba pasūtījumu kopai</span><span class="sxs-lookup"><span data-stu-id="64860-136">Add work order to a work order pool</span></span>

<span data-ttu-id="64860-137">Kā iepriekš aprakstīts šajā sadaļā, varat pievienot darba pasūtījumus darba pasūtījumu kopai, kad veidojat kopu.</span><span class="sxs-lookup"><span data-stu-id="64860-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="64860-138">Darba pasūtījumu varat pievienot darba pasūtījumu kopai arī no kāda saraksta **Visi darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="64860-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="64860-139">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="64860-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="64860-140">Sarakstā atlasiet darba pasūtījumu un noklikšķiniet uz **Darba pasūtījumu kopa**.</span><span class="sxs-lookup"><span data-stu-id="64860-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="64860-141">Laukā **Pievienot/noņemt** atlasiet “Pievienot”.</span><span class="sxs-lookup"><span data-stu-id="64860-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="64860-142">Atlasiet darba pasūtījumu kopu laukā **Kopa**.</span><span class="sxs-lookup"><span data-stu-id="64860-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="64860-143">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="64860-143">Click **OK**.</span></span>

6. <span data-ttu-id="64860-144">Pēc tam, kad darba pasūtījums ir pievienots darba pasūtījumu kopai, ja vēlaties ievietot darba pasūtījumu kopā noteiktā secībā, atveriet vienu no darba pasūtījumu kopu saraksta lapām, atlasiet kopu un noklikšķiniet uz **Rediģēt** un pielāgojiet darba pasūtījumu, kas ietverti kopā, kārtošanas secību, atverot veidlapu **Darba pasūtījumu kopas** > kopsavilkuma cilni **Darba pasūtījumi** > lauku **Kārtošanas secība**.</span><span class="sxs-lookup"><span data-stu-id="64860-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="64860-145">Ja vēlaties noņemt atlasīto darba pasūtījumu no darba pasūtījumu kopas, 3. darbībā atlasiet “Noņemt”.</span><span class="sxs-lookup"><span data-stu-id="64860-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

