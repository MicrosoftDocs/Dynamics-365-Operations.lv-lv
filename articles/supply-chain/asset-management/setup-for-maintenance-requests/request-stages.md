---
title: Uzturēšanas pieprasījumu dzīves cikla stāvokļi
description: Šajā tēmā ir aprakstīts, kā iestatīt uzturēšanas pieprasījuma dzīves cikla stāvokļus Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 151db9ca8a121759e39b690ec296b36a18dc1729
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571166"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="50846-103">Uzturēšanas pieprasījumu dzīves cikla stāvokļi</span><span class="sxs-lookup"><span data-stu-id="50846-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="50846-104">Uzturēšanas pieprasījumadzīves cikla stāvokļi nosaka posmus, kuriem pieprasījums var iet cauri.</span><span class="sxs-lookup"><span data-stu-id="50846-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="50846-105">Piemēri ietver **Izveidots**, **Aktīvs** un **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="50846-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="50846-106">Kad uzturēšanas pieprasījums tiek pārvērsts par darba pasūtījumu, uzturēšanas pieprasījuma dzīves cikla stāvoklis ir jāatjaunina uz **Pabeigts** vai **Aizvērts**, lai norādītu, ka uzturēšanas pieprasījums vairs nav aktīvs.</span><span class="sxs-lookup"><span data-stu-id="50846-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="50846-107">Saraksta lapā **Visi uzturēšanas pieprasījumi** varat skatīt visus uzturēšanas pieprasījumus neatkarīgi no to dzīves cikla stāvokļa.</span><span class="sxs-lookup"><span data-stu-id="50846-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="50846-108">Iestatīt uzturēšanas pieprasījuma dzīves cikla stāvokļus</span><span class="sxs-lookup"><span data-stu-id="50846-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="50846-109">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="50846-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="50846-110">Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="50846-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="50846-111">Laukā **Dzīves cikla stāvoklis** ievadiet dzīves cikla stāvokļa ID.</span><span class="sxs-lookup"><span data-stu-id="50846-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="50846-112">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="50846-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="50846-113">Kopsavilkuma cilnes **Detalizēta informācija** laukā **Dzīves cikla modeļi** ir parādīts to uzturēšanas pieprasījumu dzīves cikla modeļu skaits, kuri izmanto dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="50846-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="50846-114">Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Aktīvs** uz **Jā**, ja uzturēšanas pieprasījumam ir jābūt aktīvam, kamēr tas atrodas šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="50846-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="50846-115">Iestatiet opciju **Iestatīt faktisko beigu datumu** uz **Jā**, ja faktiskais beigu datums un laiks ir automātiski jāievada uzturēšanas pieprasījumā, kas ir šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="50846-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="50846-116">Iestatiet opciju **Izveidot darba pasūtījumu** uz **Jā**, ja darba pasūtījumu var izveidot no uzturēšanas pieprasījuma, kas ir šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="50846-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="50846-117">Iestatiet opciju **Dzēst** uz **Jā**, ja uzturēšanas pieprasījumu var dzēst, kamēr tas atrodas šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="50846-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="50846-118">Kopsavilkuma cilnē **Atjaunināšana** opcijas **Ienākošie** un **Izejošie** sadaļā **Llīdzekļi** ir būtiskas, ja izmantojat labošanu noliktavā. Iestatiet atbilstošo opciju uz **Jā**, ja līdzekļu, kas atlasīti uzturēšanas pieprasījumā, līdzekļa dzīves cikla stāvoklis ir automātiski jāatjaunina uz **Ienākošie** vai **Izejošie**, kad šī uzturēšanas pieprasījuma dzīves cikla stāvoklis ir iestatīts uz **Ienākošie** vai **Izejošie**.</span><span class="sxs-lookup"><span data-stu-id="50846-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="50846-119">Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu dzīves cikla stāvokļi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="50846-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Uzturēšanas pieprasījumu dzīves cikla stāvokļu lapa](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="50846-121">Uzturēšanas pieprasījuma dzīves cikla stāvokļi, dzīves cikla stāvokļa grupas un veidi ir saistīti ar darba pasūtījuma dzīves cikla stāvokļiem, dzīves cikla stāvokļa grupām un veidiem, un tiek lietoti tādā pašā veidā.</span><span class="sxs-lookup"><span data-stu-id="50846-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="50846-122">Uzturēšanas pieprasījuma dzīves cikla modeļu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="50846-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="50846-123">Kad esat izveidojis dzīves cikla stāvokļus, kas nepieciešami uzturēšanas pieprasījumiem, tos var iedalīt cikla stāvokļa grupās vai dzīves cikla modeļos.</span><span class="sxs-lookup"><span data-stu-id="50846-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="50846-124">Uzturēšanas pieprasījuma dzīves cikla modeļi tiek lietoti, lai izveidotu plūsmu, ko var izmantot dažādiem uzturēšanas pieprasījumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="50846-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="50846-125">Jāizveido vismaz viens standarta uzturēšanas pieprasījuma dzīves cikla modelis.</span><span class="sxs-lookup"><span data-stu-id="50846-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="50846-126">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Dzīves cikla modeļi**.</span><span class="sxs-lookup"><span data-stu-id="50846-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="50846-127">Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="50846-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="50846-128">Laukā **Dzīves cikla modelis** ievadiet dzīves cikla modeļa ID.</span><span class="sxs-lookup"><span data-stu-id="50846-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="50846-129">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="50846-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="50846-130">Kopsavilkuma cilnē **Detalizēta informācija** laukā **Dzīves cikla stāvokļi** ir parādīts to līdzekļu dzīves cikla stāvokļu skaits, kuri ir atlasīti šajā līdzekļa dzīves cikla modelī.</span><span class="sxs-lookup"><span data-stu-id="50846-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="50846-131">Laukā **Uzturēšanas pieprasījumu veidi** ir parādīts to uzturēšanas pieprasījumu veidu skaits, kuri izmanto šo dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="50846-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="50846-132">Kopsavilkuma cilnē **Dzīves cikla stāvokļi** atlasiet dzīves cikla stāvokļus, kuri būtu jāiekļauj dzīves cikla modelī:</span><span class="sxs-lookup"><span data-stu-id="50846-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="50846-133">Lai iekļautu dzīves cikla stāvokli dzīves cikla modelī, atlasiet to sadaļā **Atlikušie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa labi pogu ![Bultiņa pa labi](media/03-setup-for-requests.png), lai pārvietotu to uz sadaļu **Atlasītie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="50846-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="50846-134">Lai iekļautu visus pieejamos dzīves cikla stāvokļus dzīves cikla modelī, atlasiet pogu **Atlasīt visus pieejamos dzīves cikla stāvokļus** ![Atlasīt visus pieejamos dzīves cikla stāvokļus](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="50846-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="50846-135">Visi dzīves cikla stāvokļi tiek pārvietoti uz sadaļu **Atlasītie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="50846-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="50846-136">Lai dzīves cikla modelim noņemtu dzīves cikla stāvokli, atlasiet to sadaļā **Atlasītie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa kreisi pogui ![Bultiņa pa kreisi](media/05-setup-for-requests.png), lai pārvietotu to uz sadaļu **Atlikušie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="50846-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="50846-137">Kopsavilkuma cilnē **Vispārīgi** lauki sadaļā **Atjauninājumi** ir būtiski, ja izmantojat labošanu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="50846-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="50846-138">Lauka **Saņemtā līdzekļa dzīves cikla stāvoklis** atlasiet līdzekļa dzīves cikla stāvokli, uz kuru automātiski jāatjaunina līdzekļi, kas ir atlasīti uzturēšanas pieprasījumā, kad tie tiek saņemti labošanai noliktavā.</span><span class="sxs-lookup"><span data-stu-id="50846-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="50846-139">Laukā **Piegādātā līdzekļa dzīves cikla stāvoklis** atlasiet līdzekļa dzīves cikla stāvokli, uz kuru automātiski jāatjaunina līdzekļi, kas ir atlasīti uzturēšanas pieprasījumā, kad tie tiek atgriezti pēc remonta.</span><span class="sxs-lookup"><span data-stu-id="50846-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="50846-140">Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu dzīves cikla modeļi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="50846-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Uzturēšanas dzīves cikla modeļu lapa](media/06-setup-for-requests.png)
