---
title: Darba pasūtījumu kopas
description: Šajā tēmā ir aprakstīts, kā strādāt ar darba pasūtījuma kopām līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 161244cb4451ddc7b13b579fd02e828a61adeea4
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626366"
---
# <a name="work-order-pools"></a><span data-ttu-id="bd799-103">Darba pasūtījumu kopas</span><span class="sxs-lookup"><span data-stu-id="bd799-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="bd799-104">Darba pasūtījumu kopas var izmantot, lai grupētu darba pasūtījumus, kuriem ir kaut kas kopīgs.</span><span class="sxs-lookup"><span data-stu-id="bd799-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="bd799-105">Šeit ir daži piemēri lietām, kurām varat izveidot darba pasūtījumu kopas:</span><span class="sxs-lookup"><span data-stu-id="bd799-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="bd799-106">Darba komandām, piemēram, Uzturēšanas komanda A vai Uzturēšanas komanda B</span><span class="sxs-lookup"><span data-stu-id="bd799-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="bd799-107">Profesionālajām prasmēm, piemēram, elektriķi vai santehniķi</span><span class="sxs-lookup"><span data-stu-id="bd799-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="bd799-108">Fiziskām atrašanās vietām</span><span class="sxs-lookup"><span data-stu-id="bd799-108">Physical locations</span></span>  

- <span data-ttu-id="bd799-109">Laika grafikiem, piemēram, nedēļas vai citi periodi</span><span class="sxs-lookup"><span data-stu-id="bd799-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="bd799-110">Pēc nepieciešamības, varat iekļaut vienu darba pasūtījumu vairākās darbu pasūtījumu kopās.</span><span class="sxs-lookup"><span data-stu-id="bd799-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="bd799-111">Darba pasūtījumu kopas izveide</span><span class="sxs-lookup"><span data-stu-id="bd799-111">Create a work order pool</span></span>

<span data-ttu-id="bd799-112">Sarakstu lapās **Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījumu kopas** varat iegūt pārskatu par darba pasūtījuma kopām un izveidot jaunas kopas.</span><span class="sxs-lookup"><span data-stu-id="bd799-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="bd799-113">Atlasiet **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumu kopas** > **Visas darba pasūtījumu kopas** vai **Aktīvās darba pasūtījuma kopas**.</span><span class="sxs-lookup"><span data-stu-id="bd799-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="bd799-114">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="bd799-114">Select **New**.</span></span>

3. <span data-ttu-id="bd799-115">Laukā **Kopa** ievadiet ID darba pasūtījumu kopai.</span><span class="sxs-lookup"><span data-stu-id="bd799-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="bd799-116">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bd799-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="bd799-117">Uzstādiet opciju **Aktīvs** uz **Jā**, lai norādītu, ka darba pasūtījumu kopa ir aktīva.</span><span class="sxs-lookup"><span data-stu-id="bd799-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="bd799-118">Uzstādiet opciju **Dzēst darba pasūtījuma attiecības** uz **Jā**, ja vēlaties, lai darba pasūtījumi tiktu automātiski noņemti no darba pasūtījumu kopas.</span><span class="sxs-lookup"><span data-stu-id="bd799-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="bd799-119">Laukā **Dzēst dzīves cikla stāvokli** atlasiet darba pasūtījuma dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="bd799-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="bd799-120">Piemēram, darba pasūtījuma dzīves cikla stāvoklis, lai pabeigtu darba pasūtījumu, var tikt iestatīts automātiski dzēst relācijas ar darba pasūtījuma kopām.</span><span class="sxs-lookup"><span data-stu-id="bd799-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="bd799-121">Varat uzreiz sākt pievienot darba pasūtījumus darba pasūtījumu kopai.</span><span class="sxs-lookup"><span data-stu-id="bd799-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="bd799-122">Kopsavilkuma cilnē **Darba pasūtījumi** atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="bd799-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="bd799-123">Atlasiet darba pasūtījumu laukā **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="bd799-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="bd799-124">Saistītie lauki tiek atjaunināti automātiski.</span><span class="sxs-lookup"><span data-stu-id="bd799-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="bd799-125">Atkārtojiet 8. līdz 9. soli, lai pievienotu vairāk darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="bd799-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="bd799-126">Ja darba pasūtījumi, ko pievienojāt, ir jāveic noteiktā kārtībā, laukā **Kārtošanas secība** varat ievadīt ciparus **1**, **2**, **3** utt., lai precizētu šo pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="bd799-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="bd799-127">Lai skatītu sarakstu ar visiem darba pasūtījumiem, kas ir iekļauti darba pasūtījumu kopā, darbības rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Skatīt saistīto darba pasūtījumu kopu**, atlasiet **Darba pasūtījumus**, lai atvērtu **Visu darbu pasūtījumu** saraksta lapa.</span><span class="sxs-lookup"><span data-stu-id="bd799-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="bd799-128">Lai aprēķinātu un skatītu noslodzi uzturēšanas grafikam, neplānotiem darba pasūtījumiem un ieplānotajiem darba pasūtījumiem, darbību rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Skatīt saistīto darba pasūtījumu kopu**, atlasiet **Noslodze**, lai atvērtu dialogu **Aprēķināt noslodzi**.</span><span class="sxs-lookup"><span data-stu-id="bd799-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="bd799-129">Lai aprēķinātu un skatītu prognozes precēm (rezerves daļas un cita nepieciešamās preces), kas ir saistītas ar uzturēšanas grafiku, neplānotiem darba pasūtījumiem un ieplānotajiem darba pasūtījumiem, darbību rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Skatīt saistīto darba pasūtījumu kopu**, atlasiet **Preču prognoze**, lai atvērtu dialogu **Aprēķināt preču prognozi**.</span><span class="sxs-lookup"><span data-stu-id="bd799-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="bd799-130">Lai skatītu sarakstu ar visiem pirkšanas pieprasījumiem, kas ir saistīti ar darba pasūtījumiem to kopā, darbības rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Sagāde**, atlasiet **Darba pasūtījumu pirkšanas pieprasījumu**, lai atvērtu **Darba pasūtījumu pirkšanas pieprasījumu** saraksta lapa.</span><span class="sxs-lookup"><span data-stu-id="bd799-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="bd799-131">Lai skatītu sarakstu ar visiem pirkšanas pasūtījumiem, kas ir saistīti ar darba pasūtījumiem to kopā, darbības rūtī cilnē **Darba pasūtījumu kopa**, kas atrodas grupā **Sagāde**, atlasiet **Darba pasūtījumu pirkšana**, lai atvērtu **Darba pasūtījumu pirkšanas** saraksta lapu.</span><span class="sxs-lookup"><span data-stu-id="bd799-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="bd799-132">Kad darba pasūtījumu kopa jūsu darba plānošanai vairs nav atbilstoša, iestatiet opciju **Aktīvs** attiecīgajai kopai uz **Nē** saraksta skatā **Darba pasūtījumu kopas** lapā.</span><span class="sxs-lookup"><span data-stu-id="bd799-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="bd799-133">Lai dzēstu visas darbinieka pasūtījuma rindas, iestatiet opciju **Dzēst darba pasūtījumu attiecības** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="bd799-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="bd799-134">Šī opcija noder, piemēram, ja vēlaties izveidot tukšu kopu, ko vēlāk var izmantot citiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="bd799-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="bd799-135">Atcerieties iestatīt opciju **Dzēst darba pasūtījuma attiecības** uz **Nē**, kad esat gatavi izmantot darba pasūtījuma kopu, lai vēlāk izveidotu jaunas darba pasūtījuma attiecības.</span><span class="sxs-lookup"><span data-stu-id="bd799-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="bd799-136">Attēlā tālāk ir parādīts sarakstu lapas **Darba pasūtījumu kopa** piemērs.</span><span class="sxs-lookup"><span data-stu-id="bd799-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![1. attēls](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="bd799-138">Darba pasūtījuma pievienošana darba pasūtījumu kopai</span><span class="sxs-lookup"><span data-stu-id="bd799-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="bd799-139">Kā aprakstīts iepriekšējā sadaļā, varat pievienot darba pasūtījumus darba pasūtījumu kopai, kad veidojat kopu.</span><span class="sxs-lookup"><span data-stu-id="bd799-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="bd799-140">Darba pasūtījumus var pievienot arī darba pasūtījumu kopai **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi** saraksta lapā.</span><span class="sxs-lookup"><span data-stu-id="bd799-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="bd799-141">Atlasiet darba pasūtījumu un pēc tam darbības rūtī, cilnē **Darba pasūtījums** grupā **Uzturēt** atlasiet **Darba pasūtījumu kopa**.</span><span class="sxs-lookup"><span data-stu-id="bd799-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="bd799-142">Sarakstā atlasiet darba pasūtījumu un noklikšķiniet uz **Darba pasūtījumu kopa**.</span><span class="sxs-lookup"><span data-stu-id="bd799-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="bd799-143">Dialogā **Uzturēt darba uzdevumu kopu**, laukā **Pievienot/noņemt** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="bd799-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="bd799-144">Atlasiet darba pasūtījumu kopu laukā **Kopa**.</span><span class="sxs-lookup"><span data-stu-id="bd799-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="bd799-145">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="bd799-145">Select **OK**.</span></span>

6. <span data-ttu-id="bd799-146">Lai noliktu darba pasūtījumu, ko pievienojāt noteiktam pasūtījumam darba pasūtījumu kopā, **Visas darba pasūtījumu kopas** vai **Aktīvo darbu pasūtījumu kopas** saraksta lapā, atlasiet kopu un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="bd799-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="bd799-147">Pēc tam lapā **Darba pasūtījumu kopa** kopsavilkuma cilnē **Darba pasūtījumi** lietojiet lauku **Kārtot secību**, lai koriģētu kārtošanas secību darba pasūtījumiem, kas iekļauti kopā.</span><span class="sxs-lookup"><span data-stu-id="bd799-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="bd799-148">Lai noņemtu darba pasūtījumu no darba pasūtījumu kopas, atkārtojiet šīs darbības, bet atlasiet opciju **Noņemt** 3. solī.</span><span class="sxs-lookup"><span data-stu-id="bd799-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

