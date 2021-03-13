---
title: Līdzekļu dzīves cikla stāvokļi
description: Šajā tēmā ir paskaidroti līdzekļu dzīves cikla stāvokļi un dzīves cikla modeļi Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dffedfafd9d75320accf0e27f072bab6fd51f135
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016556"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="f7fdf-103">Līdzekļu dzīves cikla stāvokļi</span><span class="sxs-lookup"><span data-stu-id="f7fdf-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f7fdf-104">Šajā tēmā ir paskaidroti līdzekļu dzīves cikla stāvokļi un dzīves cikla modeļi Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="f7fdf-105">Līdzekļa dzīves cikla stāvokļi tiek izmantoti, lai definētu, vai līdzeklis ir aktīvs vai neaktīvs.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="f7fdf-106">Piemēram, varat iestatīt tādus līdzekļa dzīves cikla stāvokļus kā **Izveidots**, **Aktīvs** un **Izbeigts**.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="f7fdf-107">Pieprasījuma dzīves cikla stāvokļi ir saistīti ar līdzekļu dzīves cikla stāvokļiem.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="f7fdf-108">Tādēļ, kad pieprasījums tiek mainīts uz jaunu pieprasījuma dzīves cikla stāvokli, pieprasījumam pievienotais līdzeklis tiek mainīts uz jaunu līdzekļa dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="f7fdf-109">Piemēram, ja pieprasījuma dzīves cikla stāvoklis tiek nomainīts uz **Ienākošais**, pievienotā līdzekļa dzīves cikla stāvoklis tiek mainīts uz to dzīves cikla stāvokli, kas atlasīts lapas **Līdzekļa dzīves cikla stāvokļa modeļi** kopsavilkuma cilnes **Līdzekļa dzīves cikla stāvoklis** laukā **Ienākošais dzīves cikla stāvoklis**.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="f7fdf-110">Līdzekļa dzīves cikla stāvokļus var iestatīt līdzekļa dzīves cikla modeļos, kur var definēt nepieciešamos dzīves cikla stāvokļus dažādiem līdzekļu veidiem.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="f7fdf-111">Vispirms iestatiet dzīves cikla stāvokļus.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-111">You first set up lifecycle states.</span></span> <span data-ttu-id="f7fdf-112">Pēc tam izveidojiet dzīves cikla modeli un atlasiet tam dzīves cikla stāvokļus.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="f7fdf-113">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="f7fdf-114">Atlasiet **Jauns**, lai izveidotu jaunu dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="f7fdf-115">Laukā **Dzīves cikla stāvoklis** ievadiet dzīves cikla stāvokļa ID.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="f7fdf-116">Laukā **Nosaukums** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="f7fdf-117">Laukā **Dzīves cikla modeļi** ir parādīts to līdzekļu dzīves cikla modeļu skaits, kuri izmanto līdzekļa dzīves cikla stāvokli.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="f7fdf-118">Iestatiet opciju **Aktīvs** uz **Jā**, ja šim dzīves cikla stāvoklim jābūt aktīvam dzīves cikla stāvoklim (citiem vārdiem, ja darba pasūtījumus var izveidot līdzekļiem, kas ir šajā dzīves cikla stāvoklī).</span><span class="sxs-lookup"><span data-stu-id="f7fdf-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="f7fdf-119">Iestatiet opciju **Dzēst atvērtās kalendāra rindas** uz **Jā**, ja atvērtās līdzekļu kalendāra rindas, kuru līdzekļa dzīves cikla stāvoklis ir **Izveidots**, ir jāizdzēš, kad tās ir šajā dzīves cikla stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="f7fdf-120">Šis iestatījums ir noderīgs, ja vēlaties notīrīt visus atvērtos uzturēšanas grafikus, kas vairs nav atbilstoši līdzeklim (piemēram, ja līdzeklis vairs nav aktīvs).</span><span class="sxs-lookup"><span data-stu-id="f7fdf-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="f7fdf-121">Līdzekļa dzīves cikla stāvokļi, līdzekļa dzīves cikla modeļi un līdzekļu veidi ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="f7fdf-122">Tos izmanto tādā pašā veidā kā darba pasūtījuma dzīves cikla stāvokļus, darba pasūtījuma dzīves cikla modeļus un darba pasūtījumu veidus.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="f7fdf-123">Kad esat izveidojis nepieciešamos līdzekļa dzīves cikla stāvokļus, varat iestatīt dzīves cikla stāvokļus līdzekļa dzīves cikla modeļos.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="f7fdf-124">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Dzīves cikla modeļi**.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="f7fdf-125">Atlasiet **Jauns**, lai izveidotu jaunu dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="f7fdf-126">Laukā **Dzīves cikla modelis** ievadiet dzīves cikla modeļa ID.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="f7fdf-127">Laukā **Nosaukums** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="f7fdf-128">Laukā **Dzīves cikla stāvokļi** ir parādīts to līdzekļu dzīves cikla stāvokļu skaits, kuri ir atlasīti līdzekļa dzīves cikla modelī.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="f7fdf-129">Laukā **Līdzekļu veidi** ir parādīts to līdzekļu veidu skaits, kuri izmanto līdzekļa dzīves cikla modeli.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="f7fdf-130">Kopsavilkuma cilnē **Dzīves cikla stāvokļi** atlasiet līdzekļa dzīves cikla stāvokļus, kuri būtu jāiekļauj līdzekļa dzīves cikla modelī:</span><span class="sxs-lookup"><span data-stu-id="f7fdf-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="f7fdf-131">Lai modelim izmantotu dzīves cikla stāvokli, atlasiet to sadaļā **Atlikušie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa labi pogu ![Bultiņa pa labi](media/15-setup-for-objects.png), lai pārvietotu to uz sadaļu **Atlasītie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="f7fdf-132">Lai modelim izmantotu visus pieejamos dzīves cikla stāvokļus, atlasiet pogu **Visi pieejamie dzīves cikla stāvokļi** ![Visi pieejamie dzīves cikla stāvokļi](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="f7fdf-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="f7fdf-133">Visi dzīves cikla stāvokļi tiek nosūtīti uz sadaļu **Atlasītie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="f7fdf-134">Lai modelim noņemtu dzīves cikla stāvokli, atlasiet to sadaļā **Atlasītie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa kreisi pogui ![Bultiņa pa kreisi](media/16-setup-for-objects.png), lai pārvietotu to uz sadaļu **Atlikušie dzīves cikla stāvokļi**.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="f7fdf-135">Atlasiet **Dzīves cikla stāvokļa atjauninājumi**, lai definētu, kuri līdzekļa dzīves cikla stāvokļi var sekot atlasītajam dzīves cikla stāvoklim.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="f7fdf-136">Izmantojiet kopsavilkuma cilni **Līdzekļa stāvoklis**, ja apstrādat līdzekļus, kurus saņemat remontam.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="f7fdf-137">Sadaļā **Ienākošais/Izejošais** varat atlasīt līdzekļa dzīves cikla stāvokļus, lai norādītu remontam saņemtā līdzekļa darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="f7fdf-138">Ja piedāvājat patapinājuma līdzekļus debitoriem vai nodaļām, sadaļā **Patapinājums** varat atlasīt dzīves cikla stāvokļus patapinājuma līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="f7fdf-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
