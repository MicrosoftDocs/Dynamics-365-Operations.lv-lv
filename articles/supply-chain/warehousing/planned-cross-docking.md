---
title: Plānotā pārkraušana sadales centrā
description: Šajā tēmā ir aprakstīta uzlabota plānotā pārkraušana sadales centrā, kur pasūtījumam nepieciešamais krājumu daudzums ir novirzīts tieši no saņemšanas vai izveides uz pareizo nosūtīšanas doku vai sagatavošanas apgabalu. Visi atlikušie krājumi no saņemšanas avota tiek novirzīti uz pareizo glabāšanas vietu, izmantojot regulāro izvietošanas procesu.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017763"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="77243-104">Plānotā pārkraušana sadales centrā</span><span class="sxs-lookup"><span data-stu-id="77243-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77243-105">Šī tēma apraksta detalizētu plānoto pārkraušanu sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="77243-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="77243-106">Šajā tēmā ir aprakstīta uzlabota plānotā pārkraušana sadales centrā, kur pasūtījumam nepieciešamais krājumu daudzums ir novirzīts tieši no saņemšanas vai izveides uz pareizo nosūtīšanas doku vai sagatavošanas apgabalu.</span><span class="sxs-lookup"><span data-stu-id="77243-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="77243-107">Visi atlikušie krājumi no saņemšanas avota tiek novirzīti uz pareizo glabāšanas vietu, izmantojot regulāro izvietošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="77243-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="77243-108">Pārkraušana sadales centrā ļauj darbiniekiem izlaist ienākošo krājumu izvietošanu un izejošo krājumu izsniegšanu, kas jau ir atzīmēta izejošam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="77243-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="77243-109">Tāpēc, krājuma saskares reižu skaits tiek minimizēts iespēju robežās.</span><span class="sxs-lookup"><span data-stu-id="77243-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="77243-110">Turklāt, ņemot vērā, ka ir mazāka mijiedarbība ar sistēmu, laika un vietas ietaupījums noliktavas ražotnē ir palielināts.</span><span class="sxs-lookup"><span data-stu-id="77243-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="77243-111">Pirms var veikt pārkraušanu sadales centrā, lietotājam ir jākonfigurē jauna nosūtīšanas nosūtīšanai paredzētā veidne, kurā ir norādīts piegādes avots un citas prasību kopas pārkraušanai sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="77243-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="77243-112">Kad izejošais pasūtījums ir izveidots, rinda ir jāatzīmē ar ienākošo pasūtījumu, kas ietver to pašu elementu.</span><span class="sxs-lookup"><span data-stu-id="77243-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="77243-113">Saņemšanas pasūtījuma saņemšanas laikā pārkraušanas sadales centrā iestatījums automātiski nosaka nepieciešamību veikt pārkraušanu sadales centrā un izveido vajadzīgā daudzuma kustības darbu, pamatojoties uz novietojuma direktīvas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="77243-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="77243-114">Krājumu darbības **tiek** reģistrētas, atceļot pārkraušanas sadales centrā darbu, pat ja iestatījumi šai iespējai ir ieslēgti Noliktavas pārvaldības parametros.</span><span class="sxs-lookup"><span data-stu-id="77243-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="77243-115">Iespējot plānoto pārkraušanas opciju</span><span class="sxs-lookup"><span data-stu-id="77243-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="77243-116">Pirms izmantot uzlabotu plānoto pārkraušanu sadales centrā, funkcijai ir jābūt iespējotai sistēmā.</span><span class="sxs-lookup"><span data-stu-id="77243-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="77243-117">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="77243-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="77243-118">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="77243-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="77243-119">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="77243-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="77243-120">**Opcijas nosaukums:** *Plānotā pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="77243-121">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="77243-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="77243-122">Atkārtoti ģenerēt noslodzes grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="77243-122">Regenerate load posting methods</span></span>

<span data-ttu-id="77243-123">Plānotā pārkraušana sadales centrā tiek ieviesta kā noslodzes grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="77243-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="77243-124">Pēc opcijas iespējošanas ir atkārtoti jāģenerē metodes.</span><span class="sxs-lookup"><span data-stu-id="77243-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="77243-125">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noslodzes grāmatošanas metodes**.</span><span class="sxs-lookup"><span data-stu-id="77243-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="77243-126">Darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**.</span><span class="sxs-lookup"><span data-stu-id="77243-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="77243-127">Kad reģenerācija ir pabeigta, ir jābūt redzamai metodei ar **Metodes nosaukuma** vērtību *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="77243-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="77243-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="77243-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="77243-129">Izveidojiet pārkraušanas sadales centra veidni</span><span class="sxs-lookup"><span data-stu-id="77243-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="77243-130">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Darbs \> Pārkraušanas sadales centrā veidnes**.</span><span class="sxs-lookup"><span data-stu-id="77243-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="77243-131">Lai izveidotu veidni, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="77243-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="77243-132">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="77243-133">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="77243-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="77243-134">Šis lauks nosaka secību, kādā tiek novērtētas veidnes.</span><span class="sxs-lookup"><span data-stu-id="77243-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="77243-135">**Pārkraušanas sadales centra veidnes ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="77243-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="77243-136">**Apraksts:** *Noliktava 51*</span><span class="sxs-lookup"><span data-stu-id="77243-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="77243-137">**Pieprasījuma izlaides politika:** *Kvīts pirms piegādes*</span><span class="sxs-lookup"><span data-stu-id="77243-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="77243-138">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="77243-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="77243-139">Kopsavilkuma cilnes **Plānošana** iestatījums kontrolē veidnes darbību.</span><span class="sxs-lookup"><span data-stu-id="77243-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="77243-140">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-140">Set the following values:</span></span>

    - <span data-ttu-id="77243-141">**Pieprasījuma prasības:** *Nav*</span><span class="sxs-lookup"><span data-stu-id="77243-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="77243-142">Šis lauks nosaka pieprasījuma krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="77243-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="77243-143">Ja pieprasījumam ir jābūt saistītam ar piegādi pirms nodošanas, atlasiet *Iezīmēšana*.</span><span class="sxs-lookup"><span data-stu-id="77243-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="77243-144">Ja pieprasījumam ir jābūt rezervētam pasūtījumam pirms nodošanas, atlasiet *Pasūtījuma rezervācija*.</span><span class="sxs-lookup"><span data-stu-id="77243-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="77243-145">**Atrašanas tips:** *Piegādes vietas*</span><span class="sxs-lookup"><span data-stu-id="77243-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="77243-146">Šis lauks nosaka, vai pārkraušanai sadales centrā ir jāizmanto nosūtījuma sagatavošanas/noslodzes vietas, vai arī ir jāizmanto novietojuma direktīvas, lai atrastu savas sagatavošanas/noslodzes vietas.</span><span class="sxs-lookup"><span data-stu-id="77243-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="77243-147">**Darba veidne:** Atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="77243-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="77243-148">Šis lauks definē darba veidni, kas jāizmanto, izveidojot pārkraušanas sadales centrā darbu.</span><span class="sxs-lookup"><span data-stu-id="77243-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="77243-149">**Atkārtoti apliecināt piegādes kvīti:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="77243-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="77243-150">Šī opcija nosaka, vai, saņemot kvīti, ir atkārtoti jāapliecina piegāde.</span><span class="sxs-lookup"><span data-stu-id="77243-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="77243-151">Ja šī opcija ir iestatīta uz *Jā* , ir jāpārbauda gan maksimālais laika logs, gan beigu dienu diapazons.</span><span class="sxs-lookup"><span data-stu-id="77243-151">If this option is set to *Yes* , both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="77243-152">**Validēt maksimālo laika logu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="77243-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="77243-153">Šī opcija nosaka, vai maksimālais laika logs ir jānovērtē, kad ir atlasīts piegādes avots.</span><span class="sxs-lookup"><span data-stu-id="77243-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="77243-154">Ja šī opcija ir iestatīta uz *Jā* , ir pieejami lauki, kas saistīti ar maksimālo un minimālo laiku logiem.</span><span class="sxs-lookup"><span data-stu-id="77243-154">If this option is set to *Yes* , the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="77243-155">**Maksimālā laika logs:** *5*</span><span class="sxs-lookup"><span data-stu-id="77243-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="77243-156">Šis lauks nosaka maksimālo atļauto laika periodu starp piegādes saņemšanu un pieprasījuma izsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="77243-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="77243-157">**Maksimālais laika loga bloks:** *Dienas*</span><span class="sxs-lookup"><span data-stu-id="77243-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="77243-158">**Minimālais laika logs:** *0*</span><span class="sxs-lookup"><span data-stu-id="77243-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="77243-159">Šis lauks nosaka minimālo atļauto laika periodu starp piegādes saņemšanu un pieprasījuma izsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="77243-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="77243-160">**Minimālā laika loga vienība:** *Dienas*</span><span class="sxs-lookup"><span data-stu-id="77243-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="77243-161">**Termiņa beigu dienu diapazons:** *0*</span><span class="sxs-lookup"><span data-stu-id="77243-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="77243-162">*Pirmā beigu datuma (FEFO) kritēriji:* Šis lauks nosaka maksimālo dienu skaitu starp pirmās beigu partijas, kas pašlaik atrodas noliktavā, beigu datumu un saņemto partiju.</span><span class="sxs-lookup"><span data-stu-id="77243-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="77243-163">Kopsavilkuma cilnē **Piegādes avoti** norādiet šai veidnei derīgus piegādes tipus.</span><span class="sxs-lookup"><span data-stu-id="77243-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="77243-164">Atlasiet **Jauns** , un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-164">Select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="77243-165">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="77243-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="77243-166">**Piegādes avots:** *Pirkuma pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="77243-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="77243-167">Darba klases izveide</span><span class="sxs-lookup"><span data-stu-id="77243-167">Create a work class</span></span>

1. <span data-ttu-id="77243-168">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.</span><span class="sxs-lookup"><span data-stu-id="77243-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="77243-169">Lai izveidotu darba klasi, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="77243-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="77243-170">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-170">Set the following values:</span></span>

    - <span data-ttu-id="77243-171">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="77243-172">**Apraksts:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="77243-173">**Darba pasūtījuma tips:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="77243-174">Izveidojiet darba veidni</span><span class="sxs-lookup"><span data-stu-id="77243-174">Create a work template</span></span>

1. <span data-ttu-id="77243-175">Doties uz **Noliktavas vadība \> Iestatīšana \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="77243-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="77243-176">Laukā **Darba pasūtījuma veids** atlasiet *Pārkraušana sadales centrā*.</span><span class="sxs-lookup"><span data-stu-id="77243-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="77243-177">Lai pievienotu rindu cilnē **Pārskats** , darbības rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="77243-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="77243-178">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77243-179">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="77243-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="77243-180">**Pārkraušanas veidne:** *51 Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="77243-181">**Pārkraušanas veidnes apraksts:** *51 Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="77243-182">Atlasiet **Saglabāt** , lai padarītu pieejamu kopsavilkuma cilni **Darba veidnes informācija**.</span><span class="sxs-lookup"><span data-stu-id="77243-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="77243-183">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns** , lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="77243-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="77243-184">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77243-185">**Darba veids:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="77243-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="77243-186">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="77243-187">Atlasiet **Jauns** , lai pievienotu citu rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="77243-188">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="77243-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="77243-189">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="77243-190">Atlasiet **Saglabāt** un apstipriniet, ka ir atlasīta rūtiņa **Derīgs** veidnei *51 Pārkraušana sadales centrā*.</span><span class="sxs-lookup"><span data-stu-id="77243-190">Select **Save** , and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="77243-191">Darba klases ID *Izdošanas* un *Izvietošanas* darbu tipiem jābūt vienādiem.</span><span class="sxs-lookup"><span data-stu-id="77243-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="77243-192">Novietojuma direktīvu izveide</span><span class="sxs-lookup"><span data-stu-id="77243-192">Create location directives</span></span>

1. <span data-ttu-id="77243-193">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="77243-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="77243-194">Laukā **Darba pasūtījuma veids** atlasiet *Pārkraušana sadales centrā*.</span><span class="sxs-lookup"><span data-stu-id="77243-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="77243-195">Darbību rūtī atlasiet **Jauns** , un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-195">On the Action Pane, select **New** , and set the following values:</span></span>

    - <span data-ttu-id="77243-196">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="77243-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="77243-197">**Nosaukums:** *51 Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="77243-198">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="77243-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="77243-199">**Vieta:** *5*</span><span class="sxs-lookup"><span data-stu-id="77243-199">**Site:** *5*</span></span>
    - <span data-ttu-id="77243-200">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="77243-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="77243-201">Atlasiet **Saglabāt** , lai padarītu pieejamu kopsavilkuma cilni **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="77243-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="77243-202">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns** , lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="77243-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="77243-203">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77243-204">**No daudzuma:** *1*</span><span class="sxs-lookup"><span data-stu-id="77243-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="77243-205">**Līdz daudzumam:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="77243-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="77243-206">Atlasiet **Saglabāt** , lai padarītu pieejamu kopsavilkuma cilni **Novietojuma direktīvu darbības**.</span><span class="sxs-lookup"><span data-stu-id="77243-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="77243-207">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns** , lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="77243-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="77243-208">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77243-209">**Nosaukums:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="77243-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="77243-210">**Fiksēta novietojuma lietojums:** *Fiksētas un nefiksētas vietas*</span><span class="sxs-lookup"><span data-stu-id="77243-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="77243-211">Atlasiet **Saglabāt** , lai padarītu pogu **Rediģēt vaicājumu** rīkjoslā **Novietojuma direktīvu darbības** pieejamu.</span><span class="sxs-lookup"><span data-stu-id="77243-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="77243-212">Atlasiet **Rediģēt vaicājumu** , lai atvērtu vaicājumu redaktoru.</span><span class="sxs-lookup"><span data-stu-id="77243-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="77243-213">Cilnē **Diapazons** pārliecinieties, ka šīs divas rindas ir konfigurētas:</span><span class="sxs-lookup"><span data-stu-id="77243-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="77243-214">1. rinda:</span><span class="sxs-lookup"><span data-stu-id="77243-214">Line 1:</span></span>

        - <span data-ttu-id="77243-215">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="77243-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="77243-216">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="77243-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="77243-217">**Lauks:** *Noliktava*</span><span class="sxs-lookup"><span data-stu-id="77243-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="77243-218">**Kritēriji:** *51*</span><span class="sxs-lookup"><span data-stu-id="77243-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="77243-219">2. rinda:</span><span class="sxs-lookup"><span data-stu-id="77243-219">Line 2:</span></span>

        - <span data-ttu-id="77243-220">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="77243-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="77243-221">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="77243-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="77243-222">**Lauks:** *Novietojums*</span><span class="sxs-lookup"><span data-stu-id="77243-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="77243-223">**Kritēriji:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="77243-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="77243-224">Atlasiet **Labi** , lai aizvērtu vaicājuma lapu.</span><span class="sxs-lookup"><span data-stu-id="77243-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="77243-225">Mobilās ierīces izvēlnes elementa izveide</span><span class="sxs-lookup"><span data-stu-id="77243-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="77243-226">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="77243-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="77243-227">Kreisās rūts izvēlnes elementu sarakstā atlasiet **Pirkumu izvietošana**.</span><span class="sxs-lookup"><span data-stu-id="77243-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="77243-228">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="77243-228">Select **Edit**.</span></span>
1. <span data-ttu-id="77243-229">Kopsavilkuma cilnē **Darba klases** atlasiet **Jauns** , lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="77243-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="77243-230">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="77243-231">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="77243-232">**Darba pasūtījuma tips:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="77243-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="77243-233">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="77243-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="77243-234">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="77243-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="77243-235">Pirkuma pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="77243-235">Create a purchase order</span></span>

<span data-ttu-id="77243-236">Sekojiet šiem soļiem, lai izveidotu pirkuma pasūtījumu kā piegādes avotu.</span><span class="sxs-lookup"><span data-stu-id="77243-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="77243-237">Dodieties uz **Sagāde un avoti \> Pirkuma pasūtījumi \> Visi pirkuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="77243-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="77243-238">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="77243-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="77243-239">Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="77243-240">**Tirgotāja konts:** *104*</span><span class="sxs-lookup"><span data-stu-id="77243-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="77243-241">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="77243-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="77243-242">Atlasiet **Labi** un pierakstiet pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="77243-242">Select **OK** , and make a note of the order number.</span></span>
1. <span data-ttu-id="77243-243">Kopsavilkuma cilnei **Pirkuma pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="77243-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="77243-244">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="77243-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="77243-245">**Elementa numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="77243-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="77243-246">**Daudzums:** *5*</span><span class="sxs-lookup"><span data-stu-id="77243-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="77243-247">Izveidot pārdošanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="77243-247">Create a sales order</span></span>

<span data-ttu-id="77243-248">Sekojiet šiem soļiem, lai izveidotu pārdošanas pasūtījumu kā piegādes avotu.</span><span class="sxs-lookup"><span data-stu-id="77243-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="77243-249">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="77243-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="77243-250">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="77243-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="77243-251">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="77243-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="77243-252">**Klienta konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="77243-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="77243-253">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="77243-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="77243-254">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-254">Select **OK**.</span></span>
1. <span data-ttu-id="77243-255">Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="77243-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="77243-256">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="77243-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="77243-257">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="77243-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="77243-258">**Daudzums:** *3*</span><span class="sxs-lookup"><span data-stu-id="77243-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="77243-259">Izveidot plānoto pārkraušanu sadales centrā</span><span class="sxs-lookup"><span data-stu-id="77243-259">Create planned cross-docking</span></span>

<span data-ttu-id="77243-260">Sekojiet šiem soļiem, lai izveidotu plānoto pārkraušanu sadales centrā no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="77243-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="77243-261">Lapā **Pārdošanas pasūtījuma detalizēta informācija** lapā tikko izveidotajam pārdošanas pasūtījumam atlasiet darbības rūtī cilnē **Noliktava** grupā **Darbības** atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="77243-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="77243-262">Darbība nodot noliktavā izveido sūtījumu un noslodzes rindu pārdošanas pasūtījuma rindai un mēģina piešķirt krājumus.</span><span class="sxs-lookup"><span data-stu-id="77243-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="77243-263">Tiek parādīts informatīvs ziņojums.</span><span class="sxs-lookup"><span data-stu-id="77243-263">You receive an informational message.</span></span> <span data-ttu-id="77243-264">Tiek parādīts arī šāds brīdinājuma ziņojums: "Ar kopumu XXXX netika izveidots neviens darbs.</span><span class="sxs-lookup"><span data-stu-id="77243-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="77243-265">Detalizētu informāciju meklējiet darba izveides vēstures žurnālā. "</span><span class="sxs-lookup"><span data-stu-id="77243-265">See the work creation history log for details."</span></span> <span data-ttu-id="77243-266">Šī darbība ir paredzama, jo noliktavā nav krājumu.</span><span class="sxs-lookup"><span data-stu-id="77243-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="77243-267">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Noliktava** atlasiet **Detalizēta informācija par nosūtīšanu**.</span><span class="sxs-lookup"><span data-stu-id="77243-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="77243-268">Tiek parādīta lapa **Detalizēta informācija par nosūtīšanu** , un tā parāda sūtījumu, kas tika izveidots pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="77243-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="77243-269">Kopsavilkuma cilnē **Noslodzes rindas** ievērojiet, ka **Plānotais pārkraušanas sadales centrā daudzums** ir iestatīts uz *3*.</span><span class="sxs-lookup"><span data-stu-id="77243-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="77243-270">Tā kā noliktavā nav pieejami krājumi, bet derīgs piegādes avots ieradīsies laika loga ietvaros, kas ir definēts nosūtīšanas pārkraušanas veidnē, tika izveidots nosūtīšanas pārkraušanas daudzums.</span><span class="sxs-lookup"><span data-stu-id="77243-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="77243-271">Kopsavilkuma cilnē **Noslodzes rindas** atlasiet **Plānotā nosūtīšana-pārkraušana** , lai skatītu detalizētu informāciju par izveidoto nosūtīšanu-pārkraušanu.</span><span class="sxs-lookup"><span data-stu-id="77243-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="77243-272">Apstrādāt pārkraušanu sadales centrā</span><span class="sxs-lookup"><span data-stu-id="77243-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="77243-273">Pirkuma pasūtījuma saņemšana, izmantojot noliktavas mobilo programmu</span><span class="sxs-lookup"><span data-stu-id="77243-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="77243-274">Sistēma saņems 5 elementu daudzumu no pirkuma pasūtījuma saņemšanas vietā un izveidos divus darba gabalus.</span><span class="sxs-lookup"><span data-stu-id="77243-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="77243-275">Pirmajam izveidotajam darba ID ir **Darba pasūtījuma tipa** vērtība *Pārkraušana sadales centrā* , un tā ir saistīta ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="77243-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="77243-276">Tā daudzums ir 3, un tas ir novirzīts uz galīgo nosūtīšanas vietu, lai to varētu nosūtīt nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="77243-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="77243-277">Otrajam izveidotajam darba ID ir **Darba pasūtījuma tipa** vērtība *Pirkuma pasūtījumi* , un tā ir saistīta ar pirkuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="77243-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="77243-278">Tā atlikušais daudzums ir 2, kas netika nodots nosūtīšanai, un tas ir novirzīts izvietošanai noliktavā.</span><span class="sxs-lookup"><span data-stu-id="77243-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="77243-279">Pierakstieties mobilajā ierīcē kā lietotājs noliktavā *51*.</span><span class="sxs-lookup"><span data-stu-id="77243-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="77243-280">Doties uz **Ienākošie \> Pirkumu saņemšana**.</span><span class="sxs-lookup"><span data-stu-id="77243-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="77243-281">Laukā **PONum** ievadiet savu pirkuma pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="77243-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="77243-282">Laukā **Daudzums** ievadiet *5*.</span><span class="sxs-lookup"><span data-stu-id="77243-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="77243-283">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-283">Select **OK**.</span></span>
1. <span data-ttu-id="77243-284">Nākamajā lapā iestatiet lauku **Elements** uz *A0001*.</span><span class="sxs-lookup"><span data-stu-id="77243-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="77243-285">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-285">Select **OK**.</span></span>
1. <span data-ttu-id="77243-286">Nākamajā lapā apstipriniet **PONum** , **Elements** un **Daudzums** vērtības, atlasot **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-286">On the next page, confirm the **PONum** , **Item** , and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="77243-287">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="77243-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="77243-288">Atlasiet **Atcelt** , lai izietu.</span><span class="sxs-lookup"><span data-stu-id="77243-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="77243-289">Nosūtīšanas-pārkraušanas un lielapjoma preču izvietošana</span><span class="sxs-lookup"><span data-stu-id="77243-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="77243-290">Patlaban abiem darba ID ir vienāda mērķa numura zīme.</span><span class="sxs-lookup"><span data-stu-id="77243-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="77243-291">Lai veiktu nākamās darbības, ir jāiegūst darba ID un mērķa numura zīmes ID.</span><span class="sxs-lookup"><span data-stu-id="77243-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="77243-292">Šo informāciju var iegūt no detalizētas informācijas par pirkuma pasūtījuma rindu un pārdošanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="77243-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="77243-293">Pārmaiņus varat doties uz **Noliktavas pārvaldība \> Darbs \> Darba detaļas** un filtrēt darbu, kur **Noliktavas** vērtība ir *51*.</span><span class="sxs-lookup"><span data-stu-id="77243-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="77243-294">Mobilajā ierīcē atveriet **Ienākošie \> Pirkumu izvietošana** un ievadiet mērķa numura zīmi no darba.</span><span class="sxs-lookup"><span data-stu-id="77243-294">On the mobile device, go to **Inbound \> Purchase put-away** , and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="77243-295">Laukā **ID** ievadiet mērķa numura zīmes ID no darba informācijas.</span><span class="sxs-lookup"><span data-stu-id="77243-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="77243-296">Nosūtīšanas-pārkraušanas lapa ataino izdošanas vietu ( *RECV* ), mērķa numura zīmi ( *numura zīmi* ), krājumu ( *A0001* ) un daudzumu ( *3* ).</span><span class="sxs-lookup"><span data-stu-id="77243-296">The cross-docking pick page shows the picking location ( *RECV* ), target license plate ( *license plate* ), item ( *A0001* ), and quantity ( *3* ).</span></span>

1. <span data-ttu-id="77243-297">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-297">Select **OK**.</span></span>
1. <span data-ttu-id="77243-298">Laukā **Mērķa LP** ievadiet mērķa numura zīmi numura zīmes ID, kas ir jānovieto (bez uzglabāšanas nosūtāms) uz nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="77243-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="77243-299">Varat atlasīt jebkuru numura zīmes ID pēc savas izvēles.</span><span class="sxs-lookup"><span data-stu-id="77243-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="77243-300">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-300">Select **OK**.</span></span>
1. <span data-ttu-id="77243-301">Laukā **ID** ievadiet mērķa numura zīmes ID.</span><span class="sxs-lookup"><span data-stu-id="77243-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="77243-302">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-302">Select **OK**.</span></span>
1. <span data-ttu-id="77243-303">Apstipriniet darbu, izdodot atlikušo daudzumu 2, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="77243-304">Nākamajā lapā atlasiet **Gatavs** , lai beigtu izdošanas procesu un sāktu izvietošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="77243-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="77243-305">Mobilajā programmā ir ietverta vieta un noliktavas numura zīme krājuma novietošanai.</span><span class="sxs-lookup"><span data-stu-id="77243-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="77243-306">Apstipriniet lielapjoma glabāšanas **Izvietošanu** , atlasot **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="77243-307">Nākamajā lapā apstipriniet nosūtīšanai bez uzglabāšanas **Izvietošanu** , atlasot **Labi**.</span><span class="sxs-lookup"><span data-stu-id="77243-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="77243-308">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="77243-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="77243-309">Atlasiet **Atcelt** , lai izietu.</span><span class="sxs-lookup"><span data-stu-id="77243-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="77243-310">Sekojošajā attēlā ir parādīts, kā programmā Microsoft Dynamics 365 Supply Chain Management var tikt parādīts aizpildīts nosūtīšanas bez uzglabāšanas darbs.</span><span class="sxs-lookup"><span data-stu-id="77243-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="77243-311">![Nosūtīšanas bez uzglabāšanas darbs ir pabeigts](media/PlannedCrossDockingWork.png "Nosūtīšanas bez uzglabāšanas darbs ir pabeigts")</span><span class="sxs-lookup"><span data-stu-id="77243-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
