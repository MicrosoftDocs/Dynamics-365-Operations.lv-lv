---
title: Līdzekļu pārvaldības integrēšana ar pamatlīdzekļiem
description: Šajā tēmā skaidrots, kā integrēt Līdzekļu pārvaldības un Pamatlīdzekļu moduļus, lai varētu saistīt pamatlīdzekļus ar uzturēšanā esošiem līdzekļiem.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432669"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="c8b99-103">Līdzekļu pārvaldības integrēšana ar pamatlīdzekļiem</span><span class="sxs-lookup"><span data-stu-id="c8b99-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8b99-104">Integrējot **Līdzekļu pārvaldības** un **Pamatlīdzekļu** moduļus, jūs varat saistīt pamatlīdzekļus ar uzturēšanā esošiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="c8b99-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="c8b99-105">Pamatlīdzekļu lietotāji var izveidot uzturēšanā esošu līdzekli no jauna vai esoša pamatlīdzekļa, un Līdzekļu pārvaldības lietotāji var saistīt uzturēšanā esošu līdzekli ar esošu pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="c8b99-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="c8b99-106">Šis līdzeklis arī atvieglo Pamatlīdzekļu lietotājiem skatīt izmaksas, kas tika grāmatotas no darba pasūtījumiem, kas saistīti ar saistītajiem uzturēšanā esošiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="c8b99-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="c8b99-107">Šajā tēmā *Uzturēšanā esoši līdzekļi* attiecas uz līdzekļiem no **Līdzekļu pārvaldības** moduļa, un *Pamatlīdzekļi* attiecas uz līdzekļiem no **Pamatlīdzekļu** moduļa.</span><span class="sxs-lookup"><span data-stu-id="c8b99-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="c8b99-108">Iestatiet noklusējuma novietojumu jauniem uzturēšanā esošiem līdzekļiem, kas izveidoti no pamatlīdzekļiem (neobligāti)</span><span class="sxs-lookup"><span data-stu-id="c8b99-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="c8b99-109">Šī izvēles konfigurācija ļauj iestatīt funkcionālo novietojumu jauniem uzturēšanā esošiem līdzekļiem, kas izveidoti no pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="c8b99-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="c8b99-110">Parasti šī konfigurācija tiek pabeigta tikai vienu reizi, ja to vispār pabeidzat.</span><span class="sxs-lookup"><span data-stu-id="c8b99-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="c8b99-111">Lai pabeigtu konfigurāciju, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="c8b99-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="c8b99-112">Doties uz **Līdzekļu pārvaldība \> Iestatīšana \> Līdzekļu pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="c8b99-113">Cilnē **Pamatlīdzekļi** laukā **Funkcionālais novietojums** atlasiet noklusējuma novietojumu.</span><span class="sxs-lookup"><span data-stu-id="c8b99-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="c8b99-114">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="c8b99-115">Darbs ar integrētiem uzturēšanā esošiem līdzekļiem un pamatlīdzekļiem</span><span class="sxs-lookup"><span data-stu-id="c8b99-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="c8b99-116">Šajā sadaļā ir apkopotas procedūras, kas parāda dažādus veidus, kā var strādāt ar integrētās Līdzekļu pārvaldības un pamatlīdzekļu līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="c8b99-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="c8b99-117">Saistīt jau eksistējošu uzturēšanā esošu pamatlīdzekli ar pamatlīdzekļiem</span><span class="sxs-lookup"><span data-stu-id="c8b99-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="c8b99-118">Lai saistītu jau eksistējošu uzturēšanā esošu pamatlīdzekli ar pamatlīdzekļiem, sekojiet šīm darbībām.</span><span class="sxs-lookup"><span data-stu-id="c8b99-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="c8b99-119">Dodieties uz **Līdzekļu pārvaldība \> Līdzekļi  \> Visi līdzekļi** (vai **Aktīvie līdzekļi**).</span><span class="sxs-lookup"><span data-stu-id="c8b99-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="c8b99-120">Izvēlieties līdzekli.</span><span class="sxs-lookup"><span data-stu-id="c8b99-120">Select an asset.</span></span>
1. <span data-ttu-id="c8b99-121">**Pamatlīdzekļu** kopsavilkuma cilnē laukā **Pamatlīdzekļa numurs** atlasiet esošu pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="c8b99-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="c8b99-122">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="c8b99-123">Skatīt ar atlasīto uzturēšanā esošu līdzekli saistīto pamatlīdzekli</span><span class="sxs-lookup"><span data-stu-id="c8b99-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="c8b99-124">Lai skatītu ar atlasīto uzturēšanā esošu līdzekli saistīto pamatlīdzekli, sekojiet šīm darbībām.</span><span class="sxs-lookup"><span data-stu-id="c8b99-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="c8b99-125">Dodieties uz **Līdzekļu pārvaldība \> Līdzekļi  \> Visi līdzekļi** (vai **Aktīvie līdzekļi**).</span><span class="sxs-lookup"><span data-stu-id="c8b99-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="c8b99-126">Izvēlieties līdzekli.</span><span class="sxs-lookup"><span data-stu-id="c8b99-126">Select an asset.</span></span>
1. <span data-ttu-id="c8b99-127">**Pamatlīdzekļu** kopsavilkuma cilnē laukā **Pamatlīdzekļa numurs** atlasiet saiti.</span><span class="sxs-lookup"><span data-stu-id="c8b99-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="c8b99-128">Tiek atvērta atlasītā pamatlīdzekļa lapa **Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="c8b99-129">(Parasti šī lapa tiek atrasta **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.)</span><span class="sxs-lookup"><span data-stu-id="c8b99-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="c8b99-130">Skatīt ar atlasīto pamatlīdzekli saistīto uzturēšanā esošo līdzekli</span><span class="sxs-lookup"><span data-stu-id="c8b99-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="c8b99-131">Lai skatītu ar atlasīto pamatlīdzekli saistīto uzturēšanā esošo līdzekli, sekojiet šīm darbībām.</span><span class="sxs-lookup"><span data-stu-id="c8b99-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="c8b99-132">Dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="c8b99-133">Izvēlieties līdzekli.</span><span class="sxs-lookup"><span data-stu-id="c8b99-133">Select an asset.</span></span>
1. <span data-ttu-id="c8b99-134">Darbību rūtī cilnē **Līdzekļu pārvaldība** grupā **Skatīt** atlasiet **Uzturēšanā esošs līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="c8b99-135">Ar atlasīto pamatlīdzekli saistītā **Uzturēšanā esošā līdzekļa** lapa līdzeklim ir atvērta.</span><span class="sxs-lookup"><span data-stu-id="c8b99-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="c8b99-136">(Parasti šī lapa tiek atrasta **Līdzekļa pārvaldība \> Līdzekļi \> Visi līdzekļi**.)</span><span class="sxs-lookup"><span data-stu-id="c8b99-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="c8b99-137">Skatīt ar pamatlīdzekļiem saistītās uzturēšanas izmaksas</span><span class="sxs-lookup"><span data-stu-id="c8b99-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="c8b99-138">Līdzekļu pārvaldības darba pasūtījumus var grāmatot uzturēšanā esošiem līdzekļiem, un katram no šiem darba pasūtījumiem parasti ir izmaksas.</span><span class="sxs-lookup"><span data-stu-id="c8b99-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="c8b99-139">Kad pamatlīdzeklis ir saistīts ar uzturēšanā esošu līdzekli, varat pāriet tieši no pamatlīdzekļa, lai apskatītu saistītās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="c8b99-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="c8b99-140">Lai skatītu ar atlasīto pamatlīdzekli saistītās uzturēšanas izmaksas, sekojiet šīm darbībām.</span><span class="sxs-lookup"><span data-stu-id="c8b99-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="c8b99-141">Dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="c8b99-142">Izvēlieties līdzekli.</span><span class="sxs-lookup"><span data-stu-id="c8b99-142">Select an asset.</span></span>
1. <span data-ttu-id="c8b99-143">Darbību rūtī cilnē **Līdzekļu pārvaldība** grupā **Skatīt** atlasiet **Uzturēšanas izmaksas**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="c8b99-144">Tiek atvērta lapa **Uzturēšanas izmaksas** un parādītas saistītās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="c8b99-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="c8b99-145">Izveidot jaunu uzturēšanā esošu pamatlīdzekli jau esošam pamatlīdzekļiem</span><span class="sxs-lookup"><span data-stu-id="c8b99-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="c8b99-146">Lai izveidotu jaunu uzturēšanā esošu līdzekli ar jau esošam pamatlīdzeklim, sekojiet šīm darbībām.</span><span class="sxs-lookup"><span data-stu-id="c8b99-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="c8b99-147">Dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="c8b99-148">Izvēlieties līdzekli.</span><span class="sxs-lookup"><span data-stu-id="c8b99-148">Select an asset.</span></span>
1. <span data-ttu-id="c8b99-149">Darbību rūtī cilnē **Līdzekļu pārvaldība** grupā **Jauns** atlasiet **Izveidot uzturēšanā esošu līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="c8b99-150">(Ja šī opcija nav pieejama, iespējams, ka uzturēšanā esošs līdzeklis jau ir saistīts ar atlasīto pamatlīdzekli.)</span><span class="sxs-lookup"><span data-stu-id="c8b99-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="c8b99-151">Pabeidziet līdzekļa veidošanu, kā aprakstīts sadaļā [Izveidot līdzekli](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="c8b99-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="c8b99-152">Izveidot jaunu pamatlīdzekli un pievienot tam jaunu uzturēšanā esošu līdzekli</span><span class="sxs-lookup"><span data-stu-id="c8b99-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="c8b99-153">Lai izveidotu jaunu pamatlīdzekli un pievienotu tam jaunu uzturēšanā esošu līdzekli, sekojiet šīm darbībām.</span><span class="sxs-lookup"><span data-stu-id="c8b99-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="c8b99-154">Dodieties uz **Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="c8b99-155">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c8b99-156">Pabeidziet pamatlīdzekļa veidošanu, kā aprakstīts sadaļā [Izveidot pamatlīdzekli](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="c8b99-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="c8b99-157">Darbību rūtī cilnē **Līdzekļu pārvaldība** grupā **Jauns** atlasiet **Izveidot uzturēšanā esošu līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="c8b99-158">Pabeidziet līdzekļa veidošanu, kā aprakstīts sadaļā [Izveidot līdzekli](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="c8b99-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="c8b99-159">Noņemt saistību starp diviem līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="c8b99-159">Remove the association between two assets</span></span>

<span data-ttu-id="c8b99-160">Dažos gadījumos, iespējams, ir jāsaista uzturēšanā esošs līdzeklis no tā pamatlīdzekļa.</span><span class="sxs-lookup"><span data-stu-id="c8b99-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="c8b99-161">Piemēram, ja vēlaties [izveidot jaunu uzturēšanā esošu līdzekli](#new-maintenance-from-fixed) no pamatlīdzekļa, vispirms jānoņem kāda no esošajām saistībām.</span><span class="sxs-lookup"><span data-stu-id="c8b99-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="c8b99-162">Lai noņemtu jau eksistējošu saistību starp uzturēšanā esošu pamatlīdzekli un pamatlīdzekli, sekojiet šīm darbībām.</span><span class="sxs-lookup"><span data-stu-id="c8b99-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="c8b99-163">Dodieties uz **Līdzekļu pārvaldība \> Līdzekļi  \> Visi līdzekļi** (vai **Aktīvie līdzekļi**).</span><span class="sxs-lookup"><span data-stu-id="c8b99-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="c8b99-164">Atrast un atvērt pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="c8b99-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="c8b99-165">**Pamatlīdzekļu** kopsavilkuma cilnē nodzēsiet vērtību no **Funkcionālā novietojuma** lauka.</span><span class="sxs-lookup"><span data-stu-id="c8b99-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="c8b99-166">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c8b99-166">On the Action Pane, select **Save**.</span></span>
