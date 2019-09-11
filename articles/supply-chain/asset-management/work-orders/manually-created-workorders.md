---
title: Manuāli izveidoti darba pasūtījumi
description: Šajā tēmā ir paskaidrots, kā manuāli izveidot darba pasūtījumus programmā Asset Management.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875776"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="5d14d-103">Manuāli izveidoti darba pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="5d14d-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="5d14d-104">Ir divi veidi, kādos var manuāli izveidot darba pasūtījumus:</span><span class="sxs-lookup"><span data-stu-id="5d14d-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="5d14d-105">sadaļā **Visi darba pasūtījumi** vai **Aktīvi darba pasūtījumi**</span><span class="sxs-lookup"><span data-stu-id="5d14d-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="5d14d-106">sadaļās **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi** vai **Mani funkcionālā novietojuma uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="5d14d-107">Izveidot darba pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="5d14d-107">Create work order</span></span>

1. <span data-ttu-id="5d14d-108">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="5d14d-109">Noklikšķiniet uz pogas **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-109">Click the **New** button.</span></span>

3. <span data-ttu-id="5d14d-110">nolaižamajā sarakstā **Izveidot darba pasūtījumu** atlasiet darba pasūtījuma tipu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="5d14d-111">Ja nepieciešams, atlasiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-111">If required, select a description.</span></span>

5. <span data-ttu-id="5d14d-112">Atlasiet darba pasūtījumam līdzekli, kā arī uzturēšanas darba tipu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="5d14d-113">Atlasot līdzekli, var būt pieejamas trīs cilnes: Cilne **Mani līdzekļi** satur līdzekļus, kas ir saistīti ar funkcionālo novietojumu, kurš jums (speciālistam, kurš ir pieteicies sistēmā) var būt piešķirts (uzstādīts [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="5d14d-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="5d14d-114">Ja speciālistam sadaļā [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md) nav uzstādīts funkcionālais novietojums, cilne **Mani līdzekļi** nebūs redzama.</span><span class="sxs-lookup"><span data-stu-id="5d14d-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="5d14d-115">Cilnē **Aktīvie līdzekļī** ir iekļauts visu līdzekļu saraksts ar līdzekļa dzīves cikla statusu "Aktīvs".</span><span class="sxs-lookup"><span data-stu-id="5d14d-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="5d14d-116">Cilne **Līdzekļu skats** parāda funkcionālo novietojumu koku un šajos novietojumos uzstādītos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="5d14d-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="5d14d-117">Ja nepieciešams, atlasiet opcijas **Uzturēšanas darba tipa variants** un **Amats**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="5d14d-118">Ja nepieciešams, jūs varat mainīt darba pasūtījuma servisa līmeni laukā **Servisa līmenis**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="5d14d-119">Attiecīgajos laukos atlasiet paredzamo sākumu un beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="5d14d-120">Noklikšķiniet uz **Labi**, lai izveidotu jaunu darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="5d14d-121">Ja nepieciešams, rediģējiet darba pasūtījumu laukā **Visi darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="5d14d-122">Laukā **Visi darba pasūtījumi** jūs varat darba pasūtījumam pievienot vairākus līdzekļus Detalizētajā skatā, pievienojot rindas kopsavilkuma cilnē **Darba pasūtījuma uzturēšanas darbi**. </span><span class="sxs-lookup"><span data-stu-id="5d14d-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="5d14d-123">Līdzeklī jūs varat atlasīt vienīgi tos uzturēšanas darbu tipus, kuri ir definēti līdzeklim atlasītajā līdzekļa tipā.</span><span class="sxs-lookup"><span data-stu-id="5d14d-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="5d14d-124">Ja esat mainījis līdzekļa servisa līmeni vai līdzekļa kritiskos faktorus pēc tam, kad tie izmantoti darba pasūtījumā (skatīt [Līdzekļa servisa līmeņi](../setup-for-objects/object-priorities.md) un [Līdzekļu kritiskie faktori](../setup-for-objects/object-criticalities.md)), servisa līmenis vai kritiskie faktori darba pasūtījumā netiek atjaunināti.</span><span class="sxs-lookup"><span data-stu-id="5d14d-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="5d14d-125">Darba pasūtījuma kritiskie faktori tiek atkārtoti aprēķināti katru reizi, kad darba pasūtījuma rinda tiek pievienota darba pasūtījumam vai dzēsta no tā.</span><span class="sxs-lookup"><span data-stu-id="5d14d-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="5d14d-126">Detalizētajā skatā **Visi darba pasūtījumi** > skatā **Galvene** > ātrajā cilnē grafiks **Schedule** jūs varat atlasīt atbildīgo uzturēšanas speciālistu grupu vai atbildīgo uzturēšanas speciālistu laukos **Atbildīgā grupa** vai **Atbildīgais**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="5d14d-127">Šos uzstādījumus var mainīt, kamēr vien darba pasūtījums ir aktīvs, piemēram, ja mainās darba pasūtījuma dzīves cikla stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="5d14d-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="5d14d-128">Automātiskā atlase, kas veikts darba pasūtījuma izveides laikā, tiek balstīta uzstādījumā sadaļā **Atbildīgie uzturēšanas speciālisti**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="5d14d-129">Ja pievienojat vai dzēšat darba pasūtījuma darbus pēc tam, kad izveidojāt darba pasūtījumu, un lauki **Atbildīgo grupa** un **Atbildīgais** ir tukši, kad atjaunināt darba pasūtījumu, programma Asset Management meklē iespējamo atbildīgu uzstādīšanas veidlapā atbildīgajai uzturēšanas speciālistu grupai vai atbildīgajam uzturēšanas speciālistam.</span><span class="sxs-lookup"><span data-stu-id="5d14d-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="5d14d-130">Ja lauki **Atbildīgo grupa** vai **Atbildīgais** jau ir aizpildīti, kad atjaunināt darba pasūtījumu, netiek veiktas nekādas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="5d14d-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="5d14d-131">Sadaļā **Uzturēšanas stāvoklis** jūs varat veikt aprēķinu par to, kā iegūt pārskatu par darba slodzi attiecībā uz ienākošajiem un pabeigtajiem darba pasūtījumiem. </span><span class="sxs-lookup"><span data-stu-id="5d14d-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="5d14d-132">Ātrajā cilnē **Rindas detalizēta informācija**, izmantojiet laukus **Platums** un **Garums**, lai pievienotu ģeogrāfiskās koordinātas līdzeklim, kas atlasīts darba pasūtījuma darbā.</span><span class="sxs-lookup"><span data-stu-id="5d14d-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="5d14d-133">Izveidot saistītu darba pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="5d14d-133">Create related work order</span></span>

<span data-ttu-id="5d14d-134">Jūs varat izveidot saistītu darba pasūtījumu esošam darba pasūtījumam, ja, piemēram, vēlaties strādāt ar primāriem un sekundāriem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="5d14d-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="5d14d-135">Jauns darba pasūtījums ir balstīts darba pasūtījuma darbā no esoša darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="5d14d-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="5d14d-136">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="5d14d-137">Atlasiet darba pasūtījumu, kuram vēlaties izveidot saistītu darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="5d14d-138">Noklikšķiniet uz **Saistīts darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="5d14d-139">Nolaižamajā dialogā **Izveidot saistītu darba pasūtījumu** atlasiet darba pasūtījuma darbu, kuram vēlaties izveidot saistītu darba pasūtījumu laukā **Darba pasūtījuma darbs**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="5d14d-140">Laukā **Uzturēšanas darba tips** atlasiet uzturēšanas darba tipu un, ja nepieciešams, saistītā uzturēšanas darba tipa variantu un amatu laukos **Uzturēšanas darba tipa variants** un **Amats**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="5d14d-141">Ja šis ir pirmais saistītais darba pasūtījums, ko veicat, noklikšķiniet uz radiopogas **Jauns darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="5d14d-142">Atbilstošajos laukos atlasiet opcijas **Darba pasūtījuma tips** un **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="5d14d-143">Ja nepieciešams, mainiet darba pasūtījuma servisa līmeni laukā **Servisa līmenis**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="5d14d-144">Atbilstošajos laukos ievadiet paredzamos sākuma un beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="5d14d-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="5d14d-145">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-145">Click **OK**.</span></span> <span data-ttu-id="5d14d-146">Jaunais saistītais darba pasūtījums tiek rādīts sarakstā **Visi darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="5d14d-147">Ja jūs izveidojat saistītu darba pasūtījumu darba pasūtījumam, kuram jau ir saistīti darba pasūtījumi, jūs varat pievienot darba pasūtījumu jau saistītam darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="5d14d-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="5d14d-148">Tas tiek izdarīts, 6. darbībā noklikšķinot radiopogu **Pievienot saistītam darba pasūtījumam**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="5d14d-149">Pēc tam jūs atlasāt saistītu darba pasūtījumu, kuram vēlaties pievienot jaunu darba pasūtījuma darbu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="5d14d-150">Pēc nepieciešamības rediģējiet laukus **Servisa līmenis**, **Paredzamais sākums** un **Paredzamās beigas** un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="5d14d-151">Darba pasūtījuma darbs ir pievienots esošam saistītam darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="5d14d-151">The work order job is added to the existing related work order.</span></span>


![1. attēls](media/03-work-orders.png)

<span data-ttu-id="5d14d-153">**Piezīme:** Ja iestatījāt saistītā darba pasūtījuma masku, dodoties uz **Līdzekļa pārvaldības parametri** > **Darba pasūtījumi** saite > lauks **Saistīta darba pasūtījuma maska**, darba pasūtījuma ID tiks izveidoti atbilstoši maskas uzstādījumam.</span><span class="sxs-lookup"><span data-stu-id="5d14d-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="5d14d-154">Ja nav uzstādīta neviena saistīta darba pasūtījuma maska, saistītiem darba pasūtījumiem tiks izmantots nākamais pieejamais darba pasūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="5d14d-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="5d14d-155">Kopēt darba pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="5d14d-155">Copy work order</span></span>

<span data-ttu-id="5d14d-156">Ir iespējams ātri izveidot jaunu darba pasūtījumu no esoša darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="5d14d-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="5d14d-157">Tādējādi darbs ar darba pasūtījumiem atšķiras no darba pasūtījumu izveides, kuri ir balstīti uzturēšanas plānos.</span><span class="sxs-lookup"><span data-stu-id="5d14d-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="5d14d-158">Tas ir noderīgi, ja jums ir, piemēram, darba pasūtījums, kas satur daudzus darba pasūtījuma darbus ar dažādiem darbiem atšķirīgiem līdzekļiem, kurus vajadzētu pabeigt regulāros intervālos.</span><span class="sxs-lookup"><span data-stu-id="5d14d-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="5d14d-159">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopējs** > **Darba pasūtījumi** > **Visi darba pasūtījumi** vai **Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="5d14d-160">Atlasiet darba pasūtījumu, no kura vēlaties kopēt saturu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="5d14d-161">Noklikšķiniet uz **Kopēt darba pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-161">Click **Copy work order**.</span></span> <span data-ttu-id="5d14d-162">Tiek parādīts darba pasūtījuma uzstādījums no atlasītā darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="5d14d-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="5d14d-163">Ja nepieciešams, jūs varat dažus laukus rediģēt.</span><span class="sxs-lookup"><span data-stu-id="5d14d-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="5d14d-164">Noklikšķiniet uz **Labi**, lai izveidotu jaunu darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="5d14d-165">Ja nepieciešams, rediģējiet darba pasūtījumu laukā **Visi darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="5d14d-166">Kad ir izveidots jauns darba pasūtījums, daļa informācijas tiek kopēta tieši no esošā darba pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="5d14d-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="5d14d-167">Informācija, kas attiecas uz prognozēm, rīkiem, uzturēšanas kontrolsarakstiem, funkcionālo novietojumu, adresēm un plānošanu, netiek kopēta, bet tiek inicializēta no pašreizējā uzstādījuma programmā Asset Management.</span><span class="sxs-lookup"><span data-stu-id="5d14d-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="5d14d-168">Tādējādi, ja šajos datos tika veiktas izmaiņas laikā no pirmā darba pasūtījuma izveides datuma līdz darba pasūtījuma kopēšanas laikam, šīs izmaiņas tiek iekļautas jaunajā darba pasūtījumā, kuru izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="5d14d-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="5d14d-169">Piemēri ir izmaiņas prognozēs vai atjauninātos uzturēšanas kontrolsarakstos.</span><span class="sxs-lookup"><span data-stu-id="5d14d-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![2. attēls](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="5d14d-171">Izveidojiet uzturēšanas pieprasījumā balstītu darba pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="5d14d-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="5d14d-172">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas pieprasījumi** > **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="5d14d-173">Atlasiet uzturēšanas pieprasījumu, kuram vēlaties izveidot darba pasūtījumu, un noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="5d14d-174">Laukā **Visi pieprasījumi** noklikšķiniet uz **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="5d14d-175">Aizpildiet nolaižamo lauku **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="5d14d-176">Ja uzturēšanas darba tips ir atlasīts uzturēšanas pieprasījumā, jūs varat atlasīt citu uzturēšanas darba tipu, ja nepieciešams, kad izveidojat darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5d14d-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="5d14d-177">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-177">Click **OK**.</span></span> <span data-ttu-id="5d14d-178">Tiks parādīts ziņojums, ka darba pasūtījums ir izveidots.</span><span class="sxs-lookup"><span data-stu-id="5d14d-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="5d14d-179">Ja vēlaties redzēt, kuri darba pasūtījumi ir savienoti ar uzturēšanas pieprasījumu, atlasiet uzturēšanas pieprasījumu sarakstos **Visi uzturēšanas pieprasījumi** vai **Aktīvi uzturēšanas pieprasījumi** un noklikšķiniet uz pogas **Darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5d14d-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![3. attēls](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="5d14d-181">Darba pasūtījumus var arī izveidot automātiski, ieplānojot uzturēšanas plāna darbus vai līdzeklī uzstādot "Automātiskās izveides" uzturēšanas plānus vai uzturēšanas ciklus.</span><span class="sxs-lookup"><span data-stu-id="5d14d-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="5d14d-182">Darba pasūtījumi, kas izveidoti no uzturēšanas pieprasījumiem opcijā **Uzturēšanas grafiks**, tiek izveidoti ar uzturēšanas darba tipiem, kas atlasīti uzturēšanas pieprasījumos. </span><span class="sxs-lookup"><span data-stu-id="5d14d-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

