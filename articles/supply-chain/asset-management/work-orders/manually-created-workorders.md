---
title: Manuāli izveidoti darba pasūtījumi
description: Šajā tēmā ir paskaidrots, kā manuāli izveidot darba pasūtījumus programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a4b148d9ac5d032d2caa5fcea0398a5a3726f0e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432595"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="c9319-103">Manuāli izveidotie darba pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="c9319-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="c9319-104">Ir divi veidi, kādos var manuāli izveidot darba pasūtījumus:</span><span class="sxs-lookup"><span data-stu-id="c9319-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="c9319-105">Lapā **Visi darba pasūtījumi** vai **Aktīvi darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="c9319-106">Lapā **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi** vai **Mani funkcionālā novietojuma uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="c9319-107">Izveidot darba pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="c9319-107">Create work order</span></span>

1. <span data-ttu-id="c9319-108">Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**</span><span class="sxs-lookup"><span data-stu-id="c9319-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c9319-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c9319-109">Select **New**.</span></span>

3. <span data-ttu-id="c9319-110">Dialogā **Izveidot darba pasūtījumu** atlasiet darba pasūtījuma veidu laukā **Darba pasūtījuma veids**.</span><span class="sxs-lookup"><span data-stu-id="c9319-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="c9319-111">Ja nepieciešams, atlasiet **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="c9319-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="c9319-112">Atlasiet līdzekli laukā **Līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="c9319-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="c9319-113">Atlasot līdzekli, **Līdzeklis** nolaižamajā sarakstā var būt pieejamas trīs cilnes:</span><span class="sxs-lookup"><span data-stu-id="c9319-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="c9319-114">**Aktīvie līdzekļi** - Šajā cilnē ir iekļauts visu līdzekļu saraksts ar līdzekļa dzīves cikla statusu "Aktīvs".</span><span class="sxs-lookup"><span data-stu-id="c9319-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="c9319-115">**Līdzekļu skats** - Šī cilne parāda funkcionālo novietojumu koku un tajos uzstādītos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="c9319-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="c9319-116">**Mani līdzekļi** - Šajā cilnē ir ietverti līdzekļi, kas ir saistīti ar funkcionālajiem novietojumiem, ko jums (darbiniekam, kurš ir pieteicies sistēmā) var tikt piešķirts.</span><span class="sxs-lookup"><span data-stu-id="c9319-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="c9319-117">(Informāciju par iestatīšanu skatiet [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md).) Ja speciālistam nav iestatīti funkcionālie novietojumi [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md), tad cilne **Mani līdzekļi** nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="c9319-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="c9319-118">Laukā **Uzturēšanas darba tips** atlasiet darba pasūtījuma uzturēšanas darba veidu.</span><span class="sxs-lookup"><span data-stu-id="c9319-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="c9319-119">Ja nepieciešams, atlasiet opcijas **Uzturēšanas darba tipa variants** un **Amats**.</span><span class="sxs-lookup"><span data-stu-id="c9319-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="c9319-120">Ja nepieciešams, jūs varat mainīt darba pasūtījuma servisa līmeni laukā **Servisa līmenis**.</span><span class="sxs-lookup"><span data-stu-id="c9319-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="c9319-121">Attiecīgajos laukos atlasiet datumus **Paredzamais sākums** un **Paredzamās beigas**.</span><span class="sxs-lookup"><span data-stu-id="c9319-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="c9319-122">Noklikšķiniet uz **Labi**, lai izveidotu darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c9319-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="c9319-123">Sarakstu lapā **Visi darba pasūtījumi** jūs varat labot darba pasūtījumu, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="c9319-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="c9319-124">Ņemiet vērā šādus punktus:</span><span class="sxs-lookup"><span data-stu-id="c9319-124">Note the following points:</span></span>

- <span data-ttu-id="c9319-125">Detalizētajā skatā **Visi darba pasūtījumi** sarakstu lapā jūs varat darba pasūtījumam pievienot vairākus līdzekļus, pievienojot rindas kopsavilkuma cilnē **Darba pasūtījuma uzturēšanas darbi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="c9319-126">Līdzeklī jūs varat atlasīt vienīgi tos uzturēšanas darbu tipus, kuri ir definēti līdzekļa veidā, kas ir atlasīts līdzeklī.</span><span class="sxs-lookup"><span data-stu-id="c9319-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="c9319-127">Ja maināt līdzekļa servisa līmeni vai līdzekļa kritiskumu pēc tam, kad esat to jau izmantojis līdzekli darba pasūtījumā, servisa līmenis vai kritiskums darba pasūtījumā netiek attiecīgi atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="c9319-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="c9319-128">Lai iegūtu papildinformāciju par servisa līmeņiem un kritiskumu, skatiet [Līdzekļu servisa līmeņi](../setup-for-objects/object-priorities.md) un [Līdzekļa kritiskuma veidi](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="c9319-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="c9319-129">Kritiskums darba pasūtījumā tiek pārrēķināts katru reizi, kad darba pasūtījuma darbs tiek pievienots vai dzēsts darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="c9319-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="c9319-130">Detalizētajā skatā **Visi darba pasūtījumi** > cilnē **Galvene** > ātrajā cilnē **Grafiks** laukos **Atbildīgā grupa** vai **Atbildīgais** jūs varat atlasīt atbildīgo uzturēšanas speciālistu grupu vai atbildīgo uzturēšanas speciālistu.</span><span class="sxs-lookup"><span data-stu-id="c9319-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="c9319-131">Šos iestatījumus var mainīt, kamēr darba pasūtījums ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="c9319-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="c9319-132">Piemēram, tos var mainīt, ja mainās darba pasūtījuma dzīves cikla stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="c9319-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="c9319-133">Automātiskā atlase, kas ir veikts darba pasūtījuma izveides laikā, tiek balstīta uzstādījumā lapā **Atbildīgie uzturēšanas speciālisti**.</span><span class="sxs-lookup"><span data-stu-id="c9319-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="c9319-134">Ja pievienojat vai dzēšat darba pasūtījuma darbus pēc tam, kad izveidojāt darba pasūtījumu, un ja lauki **Atbildīgo grupa** un **Atbildīgais** ir tukši, kad atjaunināt darba pasūtījumu, programma Līdzekļu pārvaldība mēģina atrast atbildīgo uzturēšanas speciālistu grupu vai atbildīgo uzturēšanas speciālistu iespējamai sakritībai uzstādīšanas veidlapā.</span><span class="sxs-lookup"><span data-stu-id="c9319-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="c9319-135">Ja lauki **Atbildīgo grupa** vai **Atbildīgais** jau ir iestatīti, kad atjaunināt darba pasūtījumu, netiek veiktas nekādas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="c9319-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="c9319-136">Papildinformāciju par atbildīgiem uzturēšanas speciālistiem un speciālistu grupām, skatiet nodaļā [Atbildīgie uzturēšanas speciālisti](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="c9319-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="c9319-137">Lapā [Uzturēšanas stāvoklis](../controlling-and-reporting/maintenance-status.md) jūs varat veikt aprēķinu par to, kā iegūt pārskatu par darba slodzi ienākošajiem un pabeigtajiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="c9319-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="c9319-138">Lapas **Visi darba pasūtījumi** detalizētajā skatā, kopsavilkuma cilnē **Detalizētā informācija par rindu** jūs var izmantot laukus **Platums** un **Garums**, lai pievienotu ģeogrāfiskās koordinātes līdzeklim, kas atlasīts darba pasūtījuma darbā.</span><span class="sxs-lookup"><span data-stu-id="c9319-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="c9319-139">Izveidot saistītu darba pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="c9319-139">Create related work order</span></span>

<span data-ttu-id="c9319-140">Jūs varat izveidot darba pasūtījumu, kas ir saistīts ar esošo darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c9319-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="c9319-141">Šī spēja ir noderīga, ja, piemēram, vēlaties strādāt ar primāriem un sekundāriem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="c9319-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="c9319-142">Jauns darba pasūtījums ir balstīts darba pasūtījuma darbā no esoša darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="c9319-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="c9319-143">Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**</span><span class="sxs-lookup"><span data-stu-id="c9319-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c9319-144">Atlasiet darba pasūtījumu, lai tam izveidotu saistīto darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c9319-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="c9319-145">Darbību rūtī cilnē **Darba pasūtījums** grupā **Jauns** atlasiet **Saistīts darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="c9319-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="c9319-146">Dialogā **Izveidot saistītu darba pasūtījumu** laukā **Darba pasūtījuma darbs** atlasiet darba pasūtījuma darbu, kuram vēlaties izveidot saistītu darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c9319-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="c9319-147">Atlasiet uzturēšanas darba veidu laukā **Uzturēšanas darba veids**.</span><span class="sxs-lookup"><span data-stu-id="c9319-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="c9319-148">Laukos **Uzturēšanas darba tipa variants** un **Amats** atlasiet saistīto uzturēšanas darba veida variantu un amatu, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="c9319-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="c9319-149">Ja šis darba pasūtījums ir pirmais saistītais darba pasūtījums, kas tika izveidots atlasītajam darba pasūtījumam, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="c9319-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="c9319-150">Atlasiet **Jauns darba pasūtījums** opciju.</span><span class="sxs-lookup"><span data-stu-id="c9319-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="c9319-151">Atlasiet darba pasūtījuma veidu laukā **Darba pasūtījuma veids**.</span><span class="sxs-lookup"><span data-stu-id="c9319-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="c9319-152">Laukā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="c9319-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="c9319-153">Ja nepieciešams, laukā **Servisa līmenis** mainiet darba pasūtījuma servisa līmeni.</span><span class="sxs-lookup"><span data-stu-id="c9319-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="c9319-154">Laukos **Paredzamais sākums** un **Paredzamas beigas** atlasiet paredzamos sākuma un beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="c9319-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="c9319-155">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-155">Select **OK**.</span></span> <span data-ttu-id="c9319-156">Jaunais saistītais darba pasūtījums tiek rādīts lapā **Visi darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="c9319-157">Ja darba pasūtījumam, kuram jūs veidojat šo saistīto darba pasūtījumu, jau ir saistīti darba pasūtījumi, veiciet tālāk norādītās darbības, lai pievienotu jaunu darba pasūtījuma darbu esošam saistītajam darba pasūtījumam:</span><span class="sxs-lookup"><span data-stu-id="c9319-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="c9319-158">Atlasiet opciju **Pievienot saistītam darba pasūtījumam**.</span><span class="sxs-lookup"><span data-stu-id="c9319-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="c9319-159">Laukā **Darba pasūtījums** atlasiet saistītu darba pasūtījumu, kuram vēlaties pievienot jaunu darba pasūtījuma darbu.</span><span class="sxs-lookup"><span data-stu-id="c9319-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="c9319-160">Ja nepieciešams, laukā **Servisa līmenis** mainiet darba pasūtījuma servisa līmeni.</span><span class="sxs-lookup"><span data-stu-id="c9319-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="c9319-161">Laukos **Paredzamais sākums** un **Paredzamas beigas** pēc nepieciešamības mainiet paredzamos sākuma un beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="c9319-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="c9319-162">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-162">Select **OK**.</span></span> <span data-ttu-id="c9319-163">Darba pasūtījuma darbs ir pievienots esošam saistītam darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="c9319-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="c9319-164">Attēlā tālāk ir parādīts sarakstu dialoga **Izveidot saistīto darba pasūtījumu** piemērs.</span><span class="sxs-lookup"><span data-stu-id="c9319-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![1. attēls](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="c9319-166">Ja iestatījāt saistītā darba pasūtījuma masku **Līdzekļa pārvaldības parametri** > **Darba pasūtījumi** cilne > **Saistīta darba pasūtījuma maska** lauks, darba pasūtījuma ID tiek izveidoti atbilstoši maskas uzstādījumam.</span><span class="sxs-lookup"><span data-stu-id="c9319-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="c9319-167">Ja nav uzstādīta neviena saistīta darba pasūtījuma maska, saistītiem darba pasūtījumiem tiks izmantots nākamais pieejamais darba pasūtījuma ID</span><span class="sxs-lookup"><span data-stu-id="c9319-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="c9319-168">Kopēt darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c9319-168">Copy a work order</span></span>

<span data-ttu-id="c9319-169">Jūs varat ātri izveidot jaunu darba pasūtījumu no esoša darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="c9319-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="c9319-170">Tādējādi darbs ar darba pasūtījumiem atšķiras no darba pasūtījumu izveides, kuri ir balstīti uz [uzturēšanas plāni](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="c9319-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="c9319-171">Tas ir noderīgi, ja, piemēram, darba pasūtījums satur daudzus darba pasūtījuma darbus un dažādiem darbiem jābūt pabeigtiem atšķirīgos līdzekļos regulāros intervālos.</span><span class="sxs-lookup"><span data-stu-id="c9319-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="c9319-172">Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**</span><span class="sxs-lookup"><span data-stu-id="c9319-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c9319-173">Atlasiet darba pasūtījumu, no kura kopēt saturu.</span><span class="sxs-lookup"><span data-stu-id="c9319-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="c9319-174">Darbību rūtī cilnē > **Darba pasūtījums** > grupā **Jauns** atlasiet **Kopēt darba pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="c9319-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="c9319-175">Tiek parādīts darba pasūtījuma uzstādījums no atlasītā darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="c9319-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="c9319-176">Ja nepieciešams, jūs varat rediģēt dažus laukus.</span><span class="sxs-lookup"><span data-stu-id="c9319-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="c9319-177">Atlasiet **Labi**, lai izveidotu jaunu darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c9319-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="c9319-178">Sarakstu lapā **Visi darba pasūtījumi** jūs varat labot darba pasūtījumu, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="c9319-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="c9319-179">Kad ir izveidots jauns darba pasūtījums, daļa informācijas tiek kopēta tieši no esošā darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="c9319-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="c9319-180">Informācija par prognozēm, rīkiem, uzturēšanas kontrolsarakstiem, funkcionālo novietojumu, adresēm un plānošanu netiek kopēta.</span><span class="sxs-lookup"><span data-stu-id="c9319-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="c9319-181">Tā vietā tas tiek inicializēts no pašreizējiem Līdzekļu pārvaldības iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="c9319-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="c9319-182">Tāpēc, ja šī informācija tika mainīta starp laiku, kad tika izveidots pirmais darba pasūtījums, un laiku, kad veicāt darba pasūtījuma kopiju, izmaiņas tiek iekļautas jaunajā darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="c9319-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="c9319-183">Piemēri iekļauj izmaiņas prognozēs un uzturēšanas kontrolsarakstu atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="c9319-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="c9319-184">Attēlā zemāk ir parādīts dialoglodziņš **Kopēt darba pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="c9319-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![2. attēls](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="c9319-186">Izveidojiet darba pasūtījumu balstītu uz uzturēšanas pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="c9319-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="c9319-187">Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas pieprasījumi** > **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="c9319-188">Atlasiet uzturēšanas pieprasījumu, kuram izveidot darba pasūtījumu, un noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="c9319-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="c9319-189">Darbību rūtī cilnē > **Uzturēšanas pieprasījums** > grupā **Jauns** atlasiet **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="c9319-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="c9319-190">Dialogā **Darba pasūtījums** iestatiet laukus.</span><span class="sxs-lookup"><span data-stu-id="c9319-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="c9319-191">Ja uzturēšanas darba veids ir atlasīts uzturēšanas pieprasījumā, jūs varat atlasīt citu uzturēšanas darba veidu, ja nepieciešams, kad izveidojat darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c9319-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="c9319-192">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-192">Select **OK**.</span></span> <span data-ttu-id="c9319-193">Ziņojums jūs informē, ka ir izveidots darba pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="c9319-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="c9319-194">Lai skatītu darba pasūtījumus, kas ir savienoti ar uzturēšanas pieprasījumu, atlasiet uzturēšanas pieprasījumu sarakstu lapā **Visi uzturēšanas pieprasījumi** vai **Aktīvi uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="c9319-195">Pēc tam darbību rūtī cilnē **Uzturēšanas pieprasījums** grupā **Skatīt** atlasiet **Darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="c9319-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="c9319-196">Attēlā zemāk ir parādīts dialoglodziņš **Izveidot darba pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="c9319-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![3. attēls](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="c9319-198">Ja jūs vēlāties, lai darba pasūtījumi izveidotos automātiski, jūs varat ieplānot uzturēšanas plāna darbus vai līdzeklī uzstādīt "Automātiskā izveide" [uzturēšanas plāni](../preventive-and-reactive-maintenance/maintenance-plans.md) vai [uzturēšanas cikli](../preventive-and-reactive-maintenance/maintenance-rounds.md).</span><span class="sxs-lookup"><span data-stu-id="c9319-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="c9319-199">Darba pasūtījumiem, kas ir izveidoti no uzturēšanas pieprasījumiem sarakstu lapā **Viss uzturēšanas grafiks**, ir uzturēšanas darba veidi, kas ir atlasīti uzturēšanas pieprasījumos.</span><span class="sxs-lookup"><span data-stu-id="c9319-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

