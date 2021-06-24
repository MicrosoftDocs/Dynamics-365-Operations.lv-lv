---
title: Daudzumu nevar samazināt, ja pārdošanas pasūtījums ir atcelts
description: Daudzumu nevar samazināt, ja pārdošanas pasūtījums ir atcelts.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230840"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="64912-103">Daudzumu nevar samazināt, ja pārdošanas pasūtījums ir atcelts</span><span class="sxs-lookup"><span data-stu-id="64912-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="64912-104">Kļūdas kods: SYS138831</span><span class="sxs-lookup"><span data-stu-id="64912-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="64912-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="64912-105">Symptoms</span></span>

<span data-ttu-id="64912-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="64912-106">The system shows the following error message:</span></span>

> <span data-ttu-id="64912-107">Daudzumu nevar samazināt.</span><span class="sxs-lookup"><span data-stu-id="64912-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="64912-108">Krājumu darbību skaits pasūtījumā ir pārāk mazs, jo uz tā daudzumu vai daļu ir atsauce izdošanas pasūtījumā vai ražošanas pasūtījumā vai arī tā daudzums vai daļa ir atzīmēta citās darbībās.</span><span class="sxs-lookup"><span data-stu-id="64912-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="64912-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="64912-109">Cause</span></span>

<span data-ttu-id="64912-110">Ja darbs ir saistīts ar pārdošanas pasūtījumu, jūs nevarat atcelt pārdošanas pasūtījumu, kamēr nav atcelts un atsaukts darbs.</span><span class="sxs-lookup"><span data-stu-id="64912-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="64912-111">Šī prasība ir spēkā pat tad, ja ar pārdošanas pasūtījumu saistītais darbs ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="64912-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="64912-112">Novēršana</span><span class="sxs-lookup"><span data-stu-id="64912-112">Resolution</span></span>

<span data-ttu-id="64912-113">Lai atrisinātu šo problēmu, izpildiet tālāk norādītos uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="64912-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="64912-114">Atceliet atvērto darbu.</span><span class="sxs-lookup"><span data-stu-id="64912-114">Cancel open work.</span></span>
1. <span data-ttu-id="64912-115">Dzēsiet noslodzi.</span><span class="sxs-lookup"><span data-stu-id="64912-115">Delete the load.</span></span>
1. <span data-ttu-id="64912-116">Samaziniet izdoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="64912-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="64912-117">Atvērtā darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="64912-117">Cancel open work</span></span>

<span data-ttu-id="64912-118">Lai atceltu atvērto darbu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="64912-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="64912-119">Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.</span><span class="sxs-lookup"><span data-stu-id="64912-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="64912-120">Laukā **Darba ID** norādiet darba ID, kuru vēlaties atcelt un kura vērtība **Darba statuss** pašlaik ir *Atvērts*, *Notiek*, *Atcelts*, *Apvienots* vai *Slēgts*.</span><span class="sxs-lookup"><span data-stu-id="64912-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="64912-121">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="64912-121">Select **OK**.</span></span>
1. <span data-ttu-id="64912-122">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.</span><span class="sxs-lookup"><span data-stu-id="64912-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="64912-123">Noslodzes dzēšana</span><span class="sxs-lookup"><span data-stu-id="64912-123">Delete the load</span></span>

<span data-ttu-id="64912-124">Lai dzēstu noslodzi, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="64912-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="64912-125">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="64912-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="64912-126">Atveriet attiecīgo pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="64912-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="64912-127">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Noliktava \> Detalizēta informācija par darbu**.</span><span class="sxs-lookup"><span data-stu-id="64912-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="64912-128">Lapas **Darbs** darbību rūts cilnē **Darbs** grupā **Darbs** atlasiet **Atcelt darbu**.</span><span class="sxs-lookup"><span data-stu-id="64912-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="64912-129">Apstipriniet, vai lauks **Darba statuss** ir iestatīts uz *Atcelts*.</span><span class="sxs-lookup"><span data-stu-id="64912-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="64912-130">Aizveriet lapu **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="64912-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="64912-131">Pārdošanas pasūtījuma informācijas lapas kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Noliktava \> Noslodzes informācija**.</span><span class="sxs-lookup"><span data-stu-id="64912-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="64912-132">Darbību rūtī atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="64912-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="64912-133">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties dzēst noslodzi.</span><span class="sxs-lookup"><span data-stu-id="64912-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="64912-134">Aizveriet lapu **Noslodze**.</span><span class="sxs-lookup"><span data-stu-id="64912-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="64912-135">Izdotā daudzuma samazināšana</span><span class="sxs-lookup"><span data-stu-id="64912-135">Reduce the picked quantity</span></span>

<span data-ttu-id="64912-136">Kad viss darbs ir atcelts, sekojiet šīm darbībām, lai samazinātu izdoto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="64912-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="64912-137">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="64912-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="64912-138">Atveriet attiecīgo pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="64912-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="64912-139">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Atjaunināt rindu \> Izdot** no rīkjoslas.</span><span class="sxs-lookup"><span data-stu-id="64912-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="64912-140">Lapas **Izdošana** sadaļā **Darbības** atlasiet rindu, kur lauks **Izejas plūsmas statuss** ir iestatīts uz *Izdots*.</span><span class="sxs-lookup"><span data-stu-id="64912-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="64912-141">Sadaļā **Darbības** no rīkjoslas atlasiet **Pievienot izdošanas rindu**.</span><span class="sxs-lookup"><span data-stu-id="64912-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="64912-142">Sadaļā **Izdošanas rindas** no rīkjoslas atlasiet **Apstiprināt visu izdošanu**.</span><span class="sxs-lookup"><span data-stu-id="64912-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="64912-143">Aizveriet lapu **Izdošana**.</span><span class="sxs-lookup"><span data-stu-id="64912-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="64912-144">Pārdošanas pasūtījumu informācijas lapas darbību rūts cilnē **Pārdošanas pasūtījums** grupā **Uzturēt** atlasiet **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="64912-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="64912-145">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt pārdošanas pasūtījuma darbu.</span><span class="sxs-lookup"><span data-stu-id="64912-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
