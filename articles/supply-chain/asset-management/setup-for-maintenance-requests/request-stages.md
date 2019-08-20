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
ms.openlocfilehash: f68e11a1cd14bc35282b957a4262cbecdd627b3b
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790518"
---
# <a name="maintenance-request-states"></a><span data-ttu-id="0e001-103">Uzturēšanas pieprasījumu stāvokļi</span><span class="sxs-lookup"><span data-stu-id="0e001-103">Maintenance request states</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="0e001-104">Uzturēšanas pieprasījumadzīves cikla stāvokļi nosaka posmus, kuriem pieprasījums var iet cauri.</span><span class="sxs-lookup"><span data-stu-id="0e001-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="0e001-105">Piemēri ietver **Izveidots**, **Aktīvs** un **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="0e001-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="0e001-106">Kad uzturēšanas pieprasījums tiek pārvērsts par darba pasūtījumu, uzturēšanas pieprasījuma dzīves cikla stāvoklis ir jāatjaunina uz **Pabeigts** vai **Aizvērts**, lai norādītu, ka uzturēšanas pieprasījums vairs nav aktīvs.</span><span class="sxs-lookup"><span data-stu-id="0e001-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="0e001-107">Saraksta lapā **Visi uzturēšanas pieprasījumi** varat skatīt visus uzturēšanas pieprasījumus neatkarīgi no to dzīves cikla stāvokļa.</span><span class="sxs-lookup"><span data-stu-id="0e001-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="0e001-108">Iestatīt uzturēšanas pieprasījuma dzīves cikla stāvokļus</span><span class="sxs-lookup"><span data-stu-id="0e001-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="0e001-109">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="0e001-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="0e001-110">Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="0e001-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="0e001-111">Laukā **Dzīves cikla stāvoklis** ievadiet dzīves cikla stāvokļa ID.</span><span class="sxs-lookup"><span data-stu-id="0e001-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="0e001-112">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0e001-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="0e001-113">Kopsavilkuma cilnes **Detalizēta informācija** laukā **Dzīves cikla modeļi** ir parādīts to uzturēšanas pieprasījumu dzīves cikla modeļu skaits, kuri izmanto dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="0e001-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="0e001-114">Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Aktīvs** uz **Jā**, ja uzturēšanas pieprasījumam ir jābūt aktīvam, kamēr tas atrodas šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="0e001-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="0e001-115">Iestatiet opciju **Iestatīt faktisko beigu datumu** uz **Jā**, ja faktiskais beigu datums un laiks ir automātiski jāievada uzturēšanas pieprasījumā, kas ir šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="0e001-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="0e001-116">Iestatiet opciju **Izveidot darba pasūtījumu** uz **Jā**, ja darba pasūtījumu var izveidot no uzturēšanas pieprasījuma, kas ir šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="0e001-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="0e001-117">Iestatiet opciju **Dzēst** uz **Jā**, ja uzturēšanas pieprasījumu var dzēst, kamēr tas atrodas šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="0e001-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="0e001-118">Kopsavilkuma cilnē **Atjaunināšana** opcijas **Ienākošie** un **Izejošie** sadaļā **Llīdzekļi** ir būtiskas, ja izmantojat labošanu noliktavā. Iestatiet atbilstošo opciju uz **Jā**, ja līdzekļu, kas atlasīti uzturēšanas pieprasījumā, līdzekļa dzīves cikla stāvoklis ir automātiski jāatjaunina uz **Ienākošie** vai **Izejošie**, kad šī uzturēšanas pieprasījuma dzīves cikla stāvoklis ir iestatīts uz **Ienākošie** vai **Izejošie**.</span><span class="sxs-lookup"><span data-stu-id="0e001-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="0e001-119">Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu dzīves cikla stāvokļi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="0e001-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![1. attēls](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="0e001-121">Uzturēšanas pieprasījuma dzīves cikla stāvokļi, dzīves cikla stāvokļa grupas un veidi ir saistīti ar darba pasūtījuma dzīves cikla stāvokļiem, dzīves cikla stāvokļa grupām un veidiem, un tiek lietoti tādā pašā veidā.</span><span class="sxs-lookup"><span data-stu-id="0e001-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="0e001-122">Uzturēšanas pieprasījuma dzīves cikla modeļu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0e001-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="0e001-123">Kad esat izveidojis dzīves cikla stāvokļus, kas nepieciešami uzturēšanas pieprasījumiem, tos var iedalīt cikla stāvokļa grupās vai dzīves cikla modeļos.</span><span class="sxs-lookup"><span data-stu-id="0e001-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="0e001-124">Uzturēšanas pieprasījuma dzīves cikla modeļi tiek lietoti, lai izveidotu plūsmu, ko var izmantot dažādiem uzturēšanas pieprasījumu veidiem.</span><span class="sxs-lookup"><span data-stu-id="0e001-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="0e001-125">Jāizveido vismaz viens standarta uzturēšanas pieprasījuma dzīves cikla modelis.</span><span class="sxs-lookup"><span data-stu-id="0e001-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="0e001-126">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Uzturēšanas pieprasījumi** \> **Dzīves cikla modeļi**.</span><span class="sxs-lookup"><span data-stu-id="0e001-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="0e001-127">Atlasiet **Jauns**, lai izveidotu uzturēšanas pieprasījuma dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="0e001-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="0e001-128">Laukā **Dzīves cikla modelis** ievadiet dzīves cikla modeļa ID.</span><span class="sxs-lookup"><span data-stu-id="0e001-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="0e001-129">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0e001-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="0e001-130">Kopsavilkuma cilnē **Detalizēta informācija** laukā **Dzīves cikla stāvokļi** ir parādīts to līdzekļu dzīves cikla stāvokļu skaits, kuri ir atlasīti šajā līdzekļa dzīves cikla modelī.</span><span class="sxs-lookup"><span data-stu-id="0e001-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="0e001-131">Laukā **Uzturēšanas pieprasījumu veidi** ir parādīts to uzturēšanas pieprasījumu veidu skaits, kuri izmanto šo dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="0e001-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="0e001-132">Kopsavilkuma cilnē **Dzīves cikla stāvokļi** atlasiet dzīves cikla stāvokļus, kuri būtu jāiekļauj dzīves cikla modelī:</span><span class="sxs-lookup"><span data-stu-id="0e001-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="0e001-133">Lai iekļautu dzīves cikla stāvokli dzīves cikla modelī, atlasiet to sadaļā **Atlikušie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa labi pogu ![Bultiņa pa labi](media/03-setup-for-requests.png), lai pārvietotu to uz sadaļu **Atlasītie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="0e001-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="0e001-134">Lai iekļautu visus pieejamos dzīves cikla stāvokļus dzīves cikla modelī, atlasiet pogu **Atlasīt visus pieejamos dzīves cikla stāvokļus** ![Atlasīt visus pieejamos dzīves cikla stāvokļus](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="0e001-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="0e001-135">Visi dzīves cikla stāvokļi tiek pārvietoti uz sadaļu **Atlasītie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="0e001-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="0e001-136">Lai dzīves cikla modelim noņemtu dzīves cikla stāvokli, atlasiet to sadaļā **Atlasītie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa kreisi pogui ![Bultiņa pa kreisi](media/05-setup-for-requests.png), lai pārvietotu to uz sadaļu **Atlikušie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="0e001-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="0e001-137">Kopsavilkuma cilnē **Vispārīgi** lauki sadaļā **Atjauninājumi** ir būtiski, ja izmantojat labošanu noliktavā.</span><span class="sxs-lookup"><span data-stu-id="0e001-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="0e001-138">Lauka **Saņemtā līdzekļa dzīves cikla stāvoklis** atlasiet līdzekļa dzīves cikla stāvokli, uz kuru automātiski jāatjaunina līdzekļi, kas ir atlasīti uzturēšanas pieprasījumā, kad tie tiek saņemti labošanai noliktavā.</span><span class="sxs-lookup"><span data-stu-id="0e001-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="0e001-139">Laukā **Piegādātā līdzekļa dzīves cikla stāvoklis** atlasiet līdzekļa dzīves cikla stāvokli, uz kuru automātiski jāatjaunina līdzekļi, kas ir atlasīti uzturēšanas pieprasījumā, kad tie tiek atgriezti pēc remonta.</span><span class="sxs-lookup"><span data-stu-id="0e001-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="0e001-140">Nākamajā attēlā ir parādīts lapas **Uzturēšanas pieprasījumu dzīves cikla modeļi** piemērs.</span><span class="sxs-lookup"><span data-stu-id="0e001-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![2. attēls](media/06-setup-for-requests.png)
