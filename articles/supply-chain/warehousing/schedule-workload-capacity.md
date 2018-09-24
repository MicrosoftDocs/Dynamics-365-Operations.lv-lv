---
title: "Darba noslodzes ieplānošana"
description: "Šajā tēmā ir paskaidrots, kā iestatīt un plānot darba noslodzi darbiniekiem noliktavā vai visai noliktavai."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: 1b1334dcba7d12f2da301f70e21a08fceb88e2b4
ms.contentlocale: lv-lv
ms.lasthandoff: 09/22/2018

---

# <a name="schedule-workload-capacity"></a><span data-ttu-id="2d94b-103">Darba noslodzes plānošana</span><span class="sxs-lookup"><span data-stu-id="2d94b-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2d94b-104">Varat plānot darba noslodzi noliktavām, un varat arī projektēt pašreizējās un turpmākās darba slodzes darbiniekiem atsevišķās noliktavās.</span><span class="sxs-lookup"><span data-stu-id="2d94b-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="2d94b-105">Varat projektēt noslodzi visai noliktavai vai projektēt noslodzi atsevišķi ienākošajām un izejošajām slodzēm.</span><span class="sxs-lookup"><span data-stu-id="2d94b-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="2d94b-106">Lai projektētu darba slodzi atlasītajām noliktavām, šīm noliktavām ir jābūt pieejamiem vispārējās plānošanas datiem.</span><span class="sxs-lookup"><span data-stu-id="2d94b-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="2d94b-107">Papildinformāciju skatiet sadaļā [Vispārējie plāni](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="2d94b-107">For more information, see [Master plans](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="2d94b-108">Noliktavas darba slodžu plānošana un skatīšana</span><span class="sxs-lookup"><span data-stu-id="2d94b-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="2d94b-109">Lai plānotu darba slodzi noliktavai, izveidojiet darba slodzes iestatījumu vienai vai vairākām noliktavām un pēc tam saistiet šo slodzes iestatījumu ar vispārējo plānu.</span><span class="sxs-lookup"><span data-stu-id="2d94b-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="2d94b-110">Darba noslodzes iestatījumā varat definēt svara vai tilpuma ierobežojumus ienākošajām un izejošajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="2d94b-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="2d94b-111">Varat arī izveidot vairākus iestatījumus katrai noliktavai un pēc tam šo iestatījumu saistīt ar atsevišķiem vispārējiem plāniem.</span><span class="sxs-lookup"><span data-stu-id="2d94b-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="2d94b-112">Šo metodi varat izmantot, piemēram, lai pielāgotos darbaspēka sezonālajām izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="2d94b-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="2d94b-113">Ja noliktavas darbinieki strādā ar darījumiem gan ienākošajām, gan izejošajām darba slodzēm, varat konfigurēt noliktavas noslodzes iestatījumu tā, lai darba slodze būtu projektēta kombinētajā skatā.</span><span class="sxs-lookup"><span data-stu-id="2d94b-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="2d94b-114">Lai plānotu un skatītu darba slodzes noliktavām, ir jāizpilda tālāk uzskaitītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="2d94b-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="2d94b-115">Izveidojiet darba noslodzes iestatījumu un definējiet darba noslodzes ierobežojumus vienā vai vairākās noliktavās.</span><span class="sxs-lookup"><span data-stu-id="2d94b-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="2d94b-116">Saistiet darba noslodzes iestatījumu ar vispārējo plānu, lai izveidotu darba noslodzes projektēšanas, un norādiet, cik ilgi šīs projektēšanas ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="2d94b-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="2d94b-117">Darba noslodzes iestatījuma izveidošana noliktavai</span><span class="sxs-lookup"><span data-stu-id="2d94b-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="2d94b-118">Atlasiet **Krājumu pārvaldība** \> **Iestatīšana** \> **Noliktavas uzraudzība** \> **Darba noslodze**.</span><span class="sxs-lookup"><span data-stu-id="2d94b-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="2d94b-119">Darbību rūtī atlasiet **Jauns**, lai izveidotu darba noslodzes iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="2d94b-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="2d94b-120">Kopsavilkuma cilnē **Noliktavas** atlasiet **Jauns** un pēc tam rindai ierakstiet vērtības, lai kādu noliktavu saistītu ar darba noslodzes iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="2d94b-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="2d94b-121">Atzīmējiet izvēles rūtiņu **Ienākošās un izejošās darba noslodzes apvienojums**, ja pārskatā **Darba noslodze** kopējā darba noslodze ienākošajām un izejošajām transakcijām ir jārāda vienā skatā.</span><span class="sxs-lookup"><span data-stu-id="2d94b-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="2d94b-122">Kopsavilkuma cilnē **Transakciju veidi** atlasiet ienākošo un izejošo transakciju veidus, uz ko attiecas darba noslodzes ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="2d94b-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2d94b-123">Gan ienākošajai darba slodzei, gan izejošajai darba slodzei ir jāatlasa vismaz viens transakciju veids.</span><span class="sxs-lookup"><span data-stu-id="2d94b-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="2d94b-124">Tilpuma vai svara ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="2d94b-124">Define limits for volume or weight</span></span>

<span data-ttu-id="2d94b-125">Tilpuma vai svara ierobežojumus varat iestatīt atkarībā ierobežojuma, kas attiecas uz noliktavas darbaspēku.</span><span class="sxs-lookup"><span data-stu-id="2d94b-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="2d94b-126">Jūsu norādītie ierobežojumi tiek ietverti darba noslodzes projektēšanā, ko varat skatīt pārskatā **Darba noslodze**.</span><span class="sxs-lookup"><span data-stu-id="2d94b-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="2d94b-127">Lai projektētu informāciju par krājumu tilpumu un svaru, visām precēm ir jānorāda vienas krājuma vienības standarta tilpums un vienas krājuma vienības svars.</span><span class="sxs-lookup"><span data-stu-id="2d94b-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="2d94b-128">Obligāti aizpildāmie lauki ir pieejami tālāk norādītajās lauku grupās kopsavilkuma cilnē **Pārvaldīt krājumus**, lapā **Nodoto preču papildinformācija**.</span><span class="sxs-lookup"><span data-stu-id="2d94b-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="2d94b-129">Apstrāde</span><span class="sxs-lookup"><span data-stu-id="2d94b-129">Handling</span></span>
- <span data-ttu-id="2d94b-130">Fiziskās dimensijas</span><span class="sxs-lookup"><span data-stu-id="2d94b-130">Physical dimensions</span></span>
- <span data-ttu-id="2d94b-131">Svara mērījumi</span><span class="sxs-lookup"><span data-stu-id="2d94b-131">Weight measurements</span></span>

<span data-ttu-id="2d94b-132">Ja šī informācija nav norādīta pareizi, jūs saņemat ziņojumu, kad ģenerējat pārskatu **Darba noslodze**.</span><span class="sxs-lookup"><span data-stu-id="2d94b-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="2d94b-133">Pēc tam no pārskata informāciju varat detalizēt, lai identificētu trūkstošo informāciju, kas ir nepieciešama turpmākās darba noslodzes projektēšanai.</span><span class="sxs-lookup"><span data-stu-id="2d94b-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="2d94b-134">Darba noslodzes iestatījuma saistīšana ar vispārējo plānu</span><span class="sxs-lookup"><span data-stu-id="2d94b-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="2d94b-135">Atlasiet **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Ieplānot darba slodzi**.</span><span class="sxs-lookup"><span data-stu-id="2d94b-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="2d94b-136">Laukā **Vispārējais plāns** atlasiet vispārējo plānu, ko izmantot darba slodzes projektēšanai.</span><span class="sxs-lookup"><span data-stu-id="2d94b-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="2d94b-137">Laukā **Dienu skaits** norādiet dienu skaitu, uz kādu attiecas šī darba slodzes projektēšana.</span><span class="sxs-lookup"><span data-stu-id="2d94b-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="2d94b-138">Laukā **Darba slodze** atlasiet darba slodzes iestatījumu, ko saistīt ar vispārējo plānu.</span><span class="sxs-lookup"><span data-stu-id="2d94b-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="2d94b-139">Darba slodzes skatīšana</span><span class="sxs-lookup"><span data-stu-id="2d94b-139">View workload capacity</span></span>

1. <span data-ttu-id="2d94b-140">Atlasiet **Krājumu pārvaldība** \> **Pieprasījumi un pārskati** \> **Fizisko krājumu pārskati** \> **Darba noslodze**.</span><span class="sxs-lookup"><span data-stu-id="2d94b-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="2d94b-141">Laukā **Kolonnu skaits** norādiet kolonnu skaitu, ko rādīt pārskatā.</span><span class="sxs-lookup"><span data-stu-id="2d94b-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="2d94b-142">Laukā **Pasūtījuma veids** atlasiet **Plānots un apstiprināts**, **Plānots** vai **Apstiprināts**, lai norādītu pasūtījumu veidu, kurus projektēt pārskatā.</span><span class="sxs-lookup"><span data-stu-id="2d94b-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="2d94b-143">Laukā **Noslodzes veids** atlasiet noslodzes veidu, lai norādītu, vai darba noslodzi ir nepieciešams projektēt tilpumam vai svaram.</span><span class="sxs-lookup"><span data-stu-id="2d94b-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="2d94b-144">Laukā **Darba noslodze** atlasiet darba noslodzes iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="2d94b-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>

