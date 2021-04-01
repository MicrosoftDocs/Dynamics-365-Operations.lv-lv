---
title: Uzturēšanas pieprasījumu dzīves cikla stāvokļi
description: Šajā tēmā ir aprakstīts, kā iestatīt uzturēšanas pieprasījuma dzīves cikla stāvokļus Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9022d866bf0da08a72ba9169587f87c1b77527a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217225"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="7f4b5-103">Uzturēšanas pieprasījumu dzīves cikla stāvokļi</span><span class="sxs-lookup"><span data-stu-id="7f4b5-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="7f4b5-104">Uzturēšanas pieprasījumadzīves cikla stāvokļi nosaka posmus, kuriem pieprasījums var iet cauri.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="7f4b5-105">Piemēri ietver **Izveidots**, **Aktīvs** un **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="7f4b5-106">Kad uzturēšanas pieprasījums tiek pārvērsts par darba pasūtījumu, uzturēšanas pieprasījuma dzīves cikla stāvoklis ir jāatjaunina uz **Pabeigts** vai **Aizvērts**, lai norādītu, ka uzturēšanas pieprasījums vairs nav aktīvs.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="7f4b5-107">Saraksta lapā **Visi uzturēšanas pieprasījumi** varat skatīt visus uzturēšanas pieprasījumus neatkarīgi no to dzīves cikla stāvokļa.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="7f4b5-108">Iestatīt uzturēšanas pieprasījuma dzīves cikla stāvokļus</span><span class="sxs-lookup"><span data-stu-id="7f4b5-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="7f4b5-109">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="7f4b5-110">Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="7f4b5-111">Laukā **Dzīves cikla stāvoklis** ievadiet dzīves cikla stāvokļa ID.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="7f4b5-112">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="7f4b5-113">Kopsavilkuma cilnes **Detalizēta informācija** laukā **Dzīves cikla modeļi** ir parādīts to uzturēšanas pieprasījumu dzīves cikla modeļu skaits, kuri izmanto dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="7f4b5-114">Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Aktīvs** uz **Jā**, ja uzturēšanas pieprasījumam ir jābūt aktīvam, kamēr tas atrodas šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="7f4b5-115">Iestatiet opciju **Iestatīt faktisko beigu datumu** uz **Jā**, ja faktiskais beigu datums un laiks ir automātiski jāievada uzturēšanas pieprasījumā, kas ir šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-115">Set the **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="7f4b5-116">Iestatiet opciju **Izveidot darba pasūtījumu** uz **Jā**, ja darba pasūtījumu var izveidot no uzturēšanas pieprasījuma, kas ir šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="7f4b5-117">Iestatiet opciju **Dzēst** uz **Jā**, ja uzturēšanas pieprasījumu var dzēst, kamēr tas atrodas šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="7f4b5-118">Kopsavilkuma cilnē **Atjaunināt** opcijas **Ienākošie** un **Izejošie** sadaļā **Līdzeklis** ir būtiskas, lietojot noliktavas labošanu.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.</span></span> <span data-ttu-id="7f4b5-119">Iestatiet atbilstošo opciju uz **Jā**, ja līdzekļu, kas atlasīti uzturēšanas pieprasījumā, līdzekļa dzīves cikla stāvoklis ir automātiski jāatjaunina uz **Ienākošie** vai **Izejošie**, kad šī uzturēšanas pieprasījuma dzīves cikla stāvoklis ir iestatīts uz **Ienākošie** vai **Izejošie**.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-119">Set the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="7f4b5-120">Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu dzīves cikla stāvokļi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-120">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Uzturēšanas pieprasījumu dzīves cikla stāvokļu lapa](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="7f4b5-122">Uzturēšanas pieprasījuma dzīves cikla stāvokļi, dzīves cikla stāvokļa grupas un veidi ir saistīti ar darba pasūtījuma dzīves cikla stāvokļiem, dzīves cikla stāvokļa grupām un veidiem, un tiek lietoti tādā pašā veidā.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-122">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="7f4b5-123">Uzturēšanas pieprasījuma dzīves cikla modeļu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7f4b5-123">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="7f4b5-124">Kad esat izveidojis dzīves cikla stāvokļus, kas nepieciešami uzturēšanas pieprasījumiem, tos var iedalīt cikla stāvokļa grupās vai dzīves cikla modeļos.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-124">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="7f4b5-125">Uzturēšanas pieprasījuma dzīves cikla modeļi tiek lietoti, lai izveidotu plūsmu, ko var izmantot dažādiem uzturēšanas pieprasījumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-125">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="7f4b5-126">Jāizveido vismaz viens standarta uzturēšanas pieprasījuma dzīves cikla modelis.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-126">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="7f4b5-127">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Dzīves cikla modeļi**.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-127">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="7f4b5-128">Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-128">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="7f4b5-129">Laukā **Dzīves cikla modelis** ievadiet dzīves cikla modeļa ID.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-129">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="7f4b5-130">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-130">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="7f4b5-131">Kopsavilkuma cilnē **Detalizēta informācija** laukā **Dzīves cikla stāvokļi** ir parādīts to līdzekļu dzīves cikla stāvokļu skaits, kuri ir atlasīti šajā līdzekļa dzīves cikla modelī.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-131">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="7f4b5-132">Laukā **Uzturēšanas pieprasījumu veidi** ir parādīts to uzturēšanas pieprasījumu veidu skaits, kuri izmanto šo dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-132">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="7f4b5-133">Kopsavilkuma cilnē **Dzīves cikla stāvokļi** atlasiet dzīves cikla stāvokļus, kuri būtu jāiekļauj dzīves cikla modelī:</span><span class="sxs-lookup"><span data-stu-id="7f4b5-133">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="7f4b5-134">Lai iekļautu dzīves cikla stāvokli dzīves cikla modelī, atlasiet to sadaļā **Atlikušie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa labi pogu ![Bultiņa pa labi](media/03-setup-for-requests.png), lai pārvietotu to uz sadaļu **Atlasītie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-134">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="7f4b5-135">Lai iekļautu visus pieejamos dzīves cikla stāvokļus dzīves cikla modelī, atlasiet pogu **Atlasīt visus pieejamos dzīves cikla stāvokļus** ![Atlasīt visus pieejamos dzīves cikla stāvokļus](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="7f4b5-135">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="7f4b5-136">Visi dzīves cikla stāvokļi tiek pārvietoti uz sadaļu **Atlasītie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-136">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="7f4b5-137">Lai dzīves cikla modelim noņemtu dzīves cikla stāvokli, atlasiet to sadaļā **Atlasītie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa kreisi pogui ![Bultiņa pa kreisi](media/05-setup-for-requests.png), lai pārvietotu to uz sadaļu **Atlikušie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-137">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="7f4b5-138">Kopsavilkuma cilnē **Vispārīgi** lauki sadaļā **Atjauninājumi** ir būtiski, ja izmantojat labošanu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-138">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="7f4b5-139">Lauka **Saņemtā līdzekļa dzīves cikla stāvoklis** atlasiet līdzekļa dzīves cikla stāvokli, uz kuru automātiski jāatjaunina līdzekļi, kas ir atlasīti uzturēšanas pieprasījumā, kad tie tiek saņemti labošanai noliktavā.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-139">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="7f4b5-140">Laukā **Piegādātā līdzekļa dzīves cikla stāvoklis** atlasiet līdzekļa dzīves cikla stāvokli, uz kuru automātiski jāatjaunina līdzekļi, kas ir atlasīti uzturēšanas pieprasījumā, kad tie tiek atgriezti pēc remonta.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-140">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="7f4b5-141">Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu dzīves cikla modeļi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="7f4b5-141">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Uzturēšanas dzīves cikla modeļu lapa](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]