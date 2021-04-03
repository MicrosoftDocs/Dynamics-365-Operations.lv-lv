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
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556270"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="adf06-104">Plānotā pārkraušana sadales centrā</span><span class="sxs-lookup"><span data-stu-id="adf06-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adf06-105">Šī tēma apraksta detalizētu plānoto pārkraušanu sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="adf06-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="adf06-106">Šajā tēmā ir aprakstīta uzlabota plānotā pārkraušana sadales centrā, kur pasūtījumam nepieciešamais krājumu daudzums ir novirzīts tieši no saņemšanas vai izveides uz pareizo nosūtīšanas doku vai sagatavošanas apgabalu.</span><span class="sxs-lookup"><span data-stu-id="adf06-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="adf06-107">Visi atlikušie krājumi no saņemšanas avota tiek novirzīti uz pareizo glabāšanas vietu, izmantojot regulāro izvietošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="adf06-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="adf06-108">Pārkraušana sadales centrā ļauj darbiniekiem izlaist ienākošo krājumu izvietošanu un izejošo krājumu izsniegšanu, kas jau ir atzīmēta izejošam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="adf06-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="adf06-109">Tāpēc, krājuma saskares reižu skaits tiek minimizēts iespēju robežās.</span><span class="sxs-lookup"><span data-stu-id="adf06-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="adf06-110">Turklāt, ņemot vērā, ka ir mazāka mijiedarbība ar sistēmu, laika un vietas ietaupījums noliktavas ražotnē ir palielināts.</span><span class="sxs-lookup"><span data-stu-id="adf06-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="adf06-111">Pirms var veikt pārkraušanu sadales centrā, lietotājam ir jākonfigurē jauna nosūtīšanas nosūtīšanai paredzētā veidne, kurā ir norādīts piegādes avots un citas prasību kopas pārkraušanai sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="adf06-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="adf06-112">Kad izejošais pasūtījums ir izveidots, rinda ir jāatzīmē ar ienākošo pasūtījumu, kas ietver to pašu elementu.</span><span class="sxs-lookup"><span data-stu-id="adf06-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="adf06-113">Saņemšanas pasūtījuma saņemšanas laikā pārkraušanas sadales centrā iestatījums automātiski nosaka nepieciešamību veikt pārkraušanu sadales centrā un izveido vajadzīgā daudzuma kustības darbu, pamatojoties uz novietojuma direktīvas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="adf06-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="adf06-114">Krājumu darbības **tiek** reģistrētas, atceļot pārkraušanas sadales centrā darbu, pat ja iestatījumi šai iespējai ir ieslēgti Noliktavas pārvaldības parametros.</span><span class="sxs-lookup"><span data-stu-id="adf06-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="adf06-115">Iespējot plānotās pārkraušanas opcijas</span><span class="sxs-lookup"><span data-stu-id="adf06-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="adf06-116">Ja sistēmā vēl nav ietverti šajā tēmā aprakstītie līdzekļi, pārejiet uz sadaļu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet tālāk norādītās funkcijas šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="adf06-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="adf06-117">*Plānotā pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="adf06-118">*Pārkraušana sadales centrā — veidnes ar atrašanās vietas norādēm*</span><span class="sxs-lookup"><span data-stu-id="adf06-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="adf06-119">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="adf06-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="adf06-120">Atkārtoti ģenerēt noslodzes grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="adf06-120">Regenerate load posting methods</span></span>

<span data-ttu-id="adf06-121">Plānotā pārkraušana sadales centrā tiek ieviesta kā noslodzes grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="adf06-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="adf06-122">Pēc opcijas iespējošanas ir atkārtoti jāģenerē metodes.</span><span class="sxs-lookup"><span data-stu-id="adf06-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="adf06-123">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noslodzes grāmatošanas metodes**.</span><span class="sxs-lookup"><span data-stu-id="adf06-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="adf06-124">Darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**.</span><span class="sxs-lookup"><span data-stu-id="adf06-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="adf06-125">Kad reģenerācija ir pabeigta, ir jābūt redzamai metodei ar **Metodes nosaukuma** vērtību *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="adf06-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="adf06-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="adf06-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="adf06-127">Izveidojiet pārkraušanas sadales centra veidni</span><span class="sxs-lookup"><span data-stu-id="adf06-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="adf06-128">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Darbs \> Pārkraušanas sadales centrā veidnes**.</span><span class="sxs-lookup"><span data-stu-id="adf06-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="adf06-129">Lai izveidotu veidni, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="adf06-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="adf06-130">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="adf06-131">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="adf06-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="adf06-132">Šis lauks nosaka secību, kādā tiek novērtētas veidnes.</span><span class="sxs-lookup"><span data-stu-id="adf06-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="adf06-133">**Pārkraušanas sadales centra veidnes ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="adf06-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="adf06-134">**Apraksts:** *Noliktava 51*</span><span class="sxs-lookup"><span data-stu-id="adf06-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="adf06-135">**Pieprasījuma izlaides politika:** *Kvīts pirms piegādes*</span><span class="sxs-lookup"><span data-stu-id="adf06-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="adf06-136">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="adf06-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="adf06-137">Kopsavilkuma cilnes **Plānošana** iestatījums kontrolē veidnes darbību.</span><span class="sxs-lookup"><span data-stu-id="adf06-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="adf06-138">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-138">Set the following values:</span></span>

    - <span data-ttu-id="adf06-139">**Pieprasījuma prasības:** *Nav*</span><span class="sxs-lookup"><span data-stu-id="adf06-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="adf06-140">Šis lauks nosaka pieprasījuma krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="adf06-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="adf06-141">Ja pieprasījumam ir jābūt saistītam ar piegādi pirms nodošanas, atlasiet *Iezīmēšana*.</span><span class="sxs-lookup"><span data-stu-id="adf06-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="adf06-142">Ja pieprasījumam ir jābūt rezervētam pasūtījumam pirms nodošanas, atlasiet *Pasūtījuma rezervācija*.</span><span class="sxs-lookup"><span data-stu-id="adf06-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="adf06-143">**Atrašanas tips:** *Piegādes vietas*</span><span class="sxs-lookup"><span data-stu-id="adf06-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="adf06-144">Šis lauks nosaka, vai pārkraušanai sadales centrā ir jāizmanto nosūtījuma sagatavošanas/noslodzes vietas, vai arī ir jāizmanto novietojuma direktīvas, lai atrastu savas sagatavošanas/noslodzes vietas.</span><span class="sxs-lookup"><span data-stu-id="adf06-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="adf06-145">**Darba veidne:** Atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="adf06-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="adf06-146">Šis lauks definē darba veidni, kas jāizmanto, izveidojot pārkraušanas sadales centrā darbu.</span><span class="sxs-lookup"><span data-stu-id="adf06-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="adf06-147">**Atkārtoti apliecināt piegādes kvīti:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="adf06-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="adf06-148">Šī opcija nosaka, vai, saņemot kvīti, ir atkārtoti jāapliecina piegāde.</span><span class="sxs-lookup"><span data-stu-id="adf06-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="adf06-149">Ja šī opcija ir iestatīta uz *Jā*, ir jāpārbauda gan maksimālais laika logs, gan beigu dienu diapazons.</span><span class="sxs-lookup"><span data-stu-id="adf06-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="adf06-150">**Direktīvas kods:** atstājiet šo lauku tukšu</span><span class="sxs-lookup"><span data-stu-id="adf06-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="adf06-151">Šī opcija ļauj sistēmai izmantot novietojuma direktīvas, lai palīdzētu noteikt labāko novietojumu, uz kuru pārvietot krājumus pārkraušanai sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="adf06-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="adf06-152">To var iestatīt, katrai atbilstošai veidnei pārkraušanai sadales centrā piešķirot direktīvas kodu.</span><span class="sxs-lookup"><span data-stu-id="adf06-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="adf06-153">Katrs direktīvas kods identificē unikālu novietojuma direktīvu.</span><span class="sxs-lookup"><span data-stu-id="adf06-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="adf06-154">**Validēt maksimālo laika logu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="adf06-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="adf06-155">Šī opcija nosaka, vai maksimālais laika logs ir jānovērtē, kad ir atlasīts piegādes avots.</span><span class="sxs-lookup"><span data-stu-id="adf06-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="adf06-156">Ja šī opcija ir iestatīta uz *Jā*, ir pieejami lauki, kas saistīti ar maksimālo un minimālo laiku logiem.</span><span class="sxs-lookup"><span data-stu-id="adf06-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="adf06-157">**Maksimālā laika logs:** *5*</span><span class="sxs-lookup"><span data-stu-id="adf06-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="adf06-158">Šis lauks nosaka maksimālo atļauto laika periodu starp piegādes saņemšanu un pieprasījuma izsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="adf06-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="adf06-159">**Maksimālais laika loga bloks:** *Dienas*</span><span class="sxs-lookup"><span data-stu-id="adf06-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="adf06-160">**Minimālais laika logs:** *0*</span><span class="sxs-lookup"><span data-stu-id="adf06-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="adf06-161">Šis lauks nosaka minimālo atļauto laika periodu starp piegādes saņemšanu un pieprasījuma izsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="adf06-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="adf06-162">**Minimālā laika loga vienība:** *Dienas*</span><span class="sxs-lookup"><span data-stu-id="adf06-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="adf06-163">**Termiņa beigu dienu diapazons:** *0*</span><span class="sxs-lookup"><span data-stu-id="adf06-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="adf06-164">*Pirmā beigu datuma (FEFO) kritēriji:* Šis lauks nosaka maksimālo dienu skaitu starp pirmās beigu partijas, kas pašlaik atrodas noliktavā, beigu datumu un saņemto partiju.</span><span class="sxs-lookup"><span data-stu-id="adf06-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="adf06-165">Kopsavilkuma cilnē **Piegādes avoti** norādiet šai veidnei derīgus piegādes tipus.</span><span class="sxs-lookup"><span data-stu-id="adf06-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="adf06-166">Atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="adf06-167">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="adf06-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="adf06-168">**Piegādes avots:** *Pirkuma pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="adf06-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="adf06-169">Darba klases izveide</span><span class="sxs-lookup"><span data-stu-id="adf06-169">Create a work class</span></span>

1. <span data-ttu-id="adf06-170">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.</span><span class="sxs-lookup"><span data-stu-id="adf06-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="adf06-171">Lai izveidotu darba klasi, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="adf06-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="adf06-172">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-172">Set the following values:</span></span>

    - <span data-ttu-id="adf06-173">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="adf06-174">**Apraksts:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="adf06-175">**Darba pasūtījuma tips:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="adf06-176">Izveidojiet darba veidni</span><span class="sxs-lookup"><span data-stu-id="adf06-176">Create a work template</span></span>

1. <span data-ttu-id="adf06-177">Doties uz **Noliktavas vadība \> Iestatīšana \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="adf06-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="adf06-178">Laukā **Darba pasūtījuma veids** atlasiet *Pārkraušana sadales centrā*.</span><span class="sxs-lookup"><span data-stu-id="adf06-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="adf06-179">Lai pievienotu rindu cilnē **Pārskats**, darbības rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="adf06-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="adf06-180">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="adf06-181">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="adf06-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="adf06-182">**Pārkraušanas veidne:** *51 Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="adf06-183">**Pārkraušanas veidnes apraksts:** *51 Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="adf06-184">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Darba veidnes informācija**.</span><span class="sxs-lookup"><span data-stu-id="adf06-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="adf06-185">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="adf06-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="adf06-186">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="adf06-187">**Darba veids:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="adf06-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="adf06-188">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="adf06-189">Atlasiet **Jauns**, lai pievienotu citu rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="adf06-190">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="adf06-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="adf06-191">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="adf06-192">Atlasiet **Saglabāt** un apstipriniet, ka ir atlasīta rūtiņa **Derīgs** veidnei *51 Pārkraušana sadales centrā*.</span><span class="sxs-lookup"><span data-stu-id="adf06-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="adf06-193">Darba klases ID *Izdošanas* un *Izvietošanas* darbu tipiem jābūt vienādiem.</span><span class="sxs-lookup"><span data-stu-id="adf06-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="adf06-194">Novietojuma direktīvu izveide</span><span class="sxs-lookup"><span data-stu-id="adf06-194">Create location directives</span></span>

1. <span data-ttu-id="adf06-195">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="adf06-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="adf06-196">Laukā **Darba pasūtījuma veids** atlasiet *Pārkraušana sadales centrā*.</span><span class="sxs-lookup"><span data-stu-id="adf06-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="adf06-197">Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="adf06-198">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="adf06-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="adf06-199">**Nosaukums:** *51 Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="adf06-200">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="adf06-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="adf06-201">**Vieta:** *5*</span><span class="sxs-lookup"><span data-stu-id="adf06-201">**Site:** *5*</span></span>
    - <span data-ttu-id="adf06-202">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="adf06-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="adf06-203">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="adf06-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="adf06-204">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="adf06-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="adf06-205">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="adf06-206">**No daudzuma:** *1*</span><span class="sxs-lookup"><span data-stu-id="adf06-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="adf06-207">**Līdz daudzumam:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="adf06-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="adf06-208">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Novietojuma direktīvu darbības**.</span><span class="sxs-lookup"><span data-stu-id="adf06-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="adf06-209">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="adf06-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="adf06-210">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="adf06-211">**Nosaukums:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="adf06-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="adf06-212">**Fiksēta novietojuma lietojums:** *Fiksētas un nefiksētas vietas*</span><span class="sxs-lookup"><span data-stu-id="adf06-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="adf06-213">Atlasiet **Saglabāt**, lai padarītu pogu **Rediģēt vaicājumu** rīkjoslā **Novietojuma direktīvu darbības** pieejamu.</span><span class="sxs-lookup"><span data-stu-id="adf06-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="adf06-214">Atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktoru.</span><span class="sxs-lookup"><span data-stu-id="adf06-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="adf06-215">Cilnē **Diapazons** pārliecinieties, ka šīs divas rindas ir konfigurētas:</span><span class="sxs-lookup"><span data-stu-id="adf06-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="adf06-216">1. rinda:</span><span class="sxs-lookup"><span data-stu-id="adf06-216">Line 1:</span></span>

        - <span data-ttu-id="adf06-217">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="adf06-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="adf06-218">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="adf06-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="adf06-219">**Lauks:** *Noliktava*</span><span class="sxs-lookup"><span data-stu-id="adf06-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="adf06-220">**Kritēriji:** *51*</span><span class="sxs-lookup"><span data-stu-id="adf06-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="adf06-221">2. rinda:</span><span class="sxs-lookup"><span data-stu-id="adf06-221">Line 2:</span></span>

        - <span data-ttu-id="adf06-222">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="adf06-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="adf06-223">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="adf06-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="adf06-224">**Lauks:** *Novietojums*</span><span class="sxs-lookup"><span data-stu-id="adf06-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="adf06-225">**Kritēriji:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="adf06-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="adf06-226">Atlasiet **Labi**, lai aizvērtu vaicājuma lapu.</span><span class="sxs-lookup"><span data-stu-id="adf06-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="adf06-227">Mobilās ierīces izvēlnes elementa izveide</span><span class="sxs-lookup"><span data-stu-id="adf06-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="adf06-228">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="adf06-229">Kreisās rūts izvēlnes elementu sarakstā atlasiet **Pirkumu izvietošana**.</span><span class="sxs-lookup"><span data-stu-id="adf06-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="adf06-230">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="adf06-230">Select **Edit**.</span></span>
1. <span data-ttu-id="adf06-231">Kopsavilkuma cilnē **Darba klases** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="adf06-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="adf06-232">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="adf06-233">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="adf06-234">**Darba pasūtījuma tips:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="adf06-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="adf06-235">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="adf06-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="adf06-236">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="adf06-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="adf06-237">Pirkuma pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="adf06-237">Create a purchase order</span></span>

<span data-ttu-id="adf06-238">Sekojiet šiem soļiem, lai izveidotu pirkuma pasūtījumu kā piegādes avotu.</span><span class="sxs-lookup"><span data-stu-id="adf06-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="adf06-239">Dodieties uz **Sagāde un avoti \> Pirkuma pasūtījumi \> Visi pirkuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="adf06-240">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="adf06-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="adf06-241">Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="adf06-242">**Tirgotāja konts:** *104*</span><span class="sxs-lookup"><span data-stu-id="adf06-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="adf06-243">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="adf06-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="adf06-244">Atlasiet **Labi** un pierakstiet pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="adf06-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="adf06-245">Kopsavilkuma cilnei **Pirkuma pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="adf06-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="adf06-246">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="adf06-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="adf06-247">**Elementa numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="adf06-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="adf06-248">**Daudzums:** *5*</span><span class="sxs-lookup"><span data-stu-id="adf06-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="adf06-249">Izveidot pārdošanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="adf06-249">Create a sales order</span></span>

<span data-ttu-id="adf06-250">Sekojiet šiem soļiem, lai izveidotu pārdošanas pasūtījumu kā piegādes avotu.</span><span class="sxs-lookup"><span data-stu-id="adf06-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="adf06-251">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="adf06-252">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="adf06-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="adf06-253">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="adf06-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="adf06-254">**Klienta konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="adf06-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="adf06-255">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="adf06-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="adf06-256">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-256">Select **OK**.</span></span>
1. <span data-ttu-id="adf06-257">Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="adf06-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="adf06-258">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="adf06-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="adf06-259">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="adf06-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="adf06-260">**Daudzums:** *3*</span><span class="sxs-lookup"><span data-stu-id="adf06-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="adf06-261">Izveidot plānoto pārkraušanu sadales centrā</span><span class="sxs-lookup"><span data-stu-id="adf06-261">Create planned cross-docking</span></span>

<span data-ttu-id="adf06-262">Sekojiet šiem soļiem, lai izveidotu plānoto pārkraušanu sadales centrā no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="adf06-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="adf06-263">Lapā **Pārdošanas pasūtījuma detalizēta informācija** lapā tikko izveidotajam pārdošanas pasūtījumam atlasiet darbības rūtī cilnē **Noliktava** grupā **Darbības** atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="adf06-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="adf06-264">Darbība nodot noliktavā izveido sūtījumu un noslodzes rindu pārdošanas pasūtījuma rindai un mēģina piešķirt krājumus.</span><span class="sxs-lookup"><span data-stu-id="adf06-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="adf06-265">Tiek parādīts informatīvs ziņojums.</span><span class="sxs-lookup"><span data-stu-id="adf06-265">You receive an informational message.</span></span> <span data-ttu-id="adf06-266">Tiek parādīts arī šāds brīdinājuma ziņojums: "Ar kopumu XXXX netika izveidots neviens darbs.</span><span class="sxs-lookup"><span data-stu-id="adf06-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="adf06-267">Detalizētu informāciju meklējiet darba izveides vēstures žurnālā. "</span><span class="sxs-lookup"><span data-stu-id="adf06-267">See the work creation history log for details."</span></span> <span data-ttu-id="adf06-268">Šī darbība ir paredzama, jo noliktavā nav krājumu.</span><span class="sxs-lookup"><span data-stu-id="adf06-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="adf06-269">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Noliktava** atlasiet **Detalizēta informācija par nosūtīšanu**.</span><span class="sxs-lookup"><span data-stu-id="adf06-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="adf06-270">Tiek parādīta lapa **Detalizēta informācija par nosūtīšanu**, un tā parāda sūtījumu, kas tika izveidots pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="adf06-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="adf06-271">Kopsavilkuma cilnē **Noslodzes rindas** ievērojiet, ka **Plānotais pārkraušanas sadales centrā daudzums** ir iestatīts uz *3*.</span><span class="sxs-lookup"><span data-stu-id="adf06-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="adf06-272">Tā kā noliktavā nav pieejami krājumi, bet derīgs piegādes avots ieradīsies laika loga ietvaros, kas ir definēts nosūtīšanas pārkraušanas veidnē, tika izveidots nosūtīšanas pārkraušanas daudzums.</span><span class="sxs-lookup"><span data-stu-id="adf06-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="adf06-273">Kopsavilkuma cilnē **Noslodzes rindas** atlasiet **Plānotā nosūtīšana-pārkraušana**, lai skatītu detalizētu informāciju par izveidoto nosūtīšanu-pārkraušanu.</span><span class="sxs-lookup"><span data-stu-id="adf06-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="adf06-274">Apstrādāt pārkraušanu sadales centrā</span><span class="sxs-lookup"><span data-stu-id="adf06-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="adf06-275">Pirkuma pasūtījuma saņemšana, izmantojot noliktavas mobilo programmu</span><span class="sxs-lookup"><span data-stu-id="adf06-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="adf06-276">Sistēma saņems 5 elementu daudzumu no pirkuma pasūtījuma saņemšanas vietā un izveidos divus darba gabalus.</span><span class="sxs-lookup"><span data-stu-id="adf06-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="adf06-277">Pirmajam izveidotajam darba ID ir **Darba pasūtījuma tipa** vērtība *Pārkraušana sadales centrā*, un tā ir saistīta ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="adf06-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="adf06-278">Tā daudzums ir 3, un tas ir novirzīts uz galīgo nosūtīšanas vietu, lai to varētu nosūtīt nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="adf06-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="adf06-279">Otrajam izveidotajam darba ID ir **Darba pasūtījuma tipa** vērtība *Pirkuma pasūtījumi*, un tā ir saistīta ar pirkuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="adf06-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="adf06-280">Tā atlikušais daudzums ir 2, kas netika nodots nosūtīšanai, un tas ir novirzīts izvietošanai noliktavā.</span><span class="sxs-lookup"><span data-stu-id="adf06-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="adf06-281">Pierakstieties mobilajā ierīcē kā lietotājs noliktavā *51*.</span><span class="sxs-lookup"><span data-stu-id="adf06-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="adf06-282">Doties uz **Ienākošie \> Pirkumu saņemšana**.</span><span class="sxs-lookup"><span data-stu-id="adf06-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="adf06-283">Laukā **PONum** ievadiet savu pirkuma pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="adf06-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="adf06-284">Laukā **Daudzums** ievadiet *5*.</span><span class="sxs-lookup"><span data-stu-id="adf06-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="adf06-285">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-285">Select **OK**.</span></span>
1. <span data-ttu-id="adf06-286">Nākamajā lapā iestatiet lauku **Elements** uz *A0001*.</span><span class="sxs-lookup"><span data-stu-id="adf06-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="adf06-287">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-287">Select **OK**.</span></span>
1. <span data-ttu-id="adf06-288">Nākamajā lapā apstipriniet **PONum**, **Elements** un **Daudzums** vērtības, atlasot **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="adf06-289">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="adf06-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="adf06-290">Atlasiet **Atcelt**, lai izietu.</span><span class="sxs-lookup"><span data-stu-id="adf06-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="adf06-291">Nosūtīšanas-pārkraušanas un lielapjoma preču izvietošana</span><span class="sxs-lookup"><span data-stu-id="adf06-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="adf06-292">Patlaban abiem darba ID ir vienāda mērķa numura zīme.</span><span class="sxs-lookup"><span data-stu-id="adf06-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="adf06-293">Lai veiktu nākamās darbības, ir jāiegūst darba ID un mērķa numura zīmes ID.</span><span class="sxs-lookup"><span data-stu-id="adf06-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="adf06-294">Šo informāciju var iegūt no detalizētas informācijas par pirkuma pasūtījuma rindu un pārdošanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="adf06-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="adf06-295">Pārmaiņus varat doties uz **Noliktavas pārvaldība \> Darbs \> Darba detaļas** un filtrēt darbu, kur **Noliktavas** vērtība ir *51*.</span><span class="sxs-lookup"><span data-stu-id="adf06-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="adf06-296">Mobilajā ierīcē atveriet **Ienākošie \> Pirkumu izvietošana** un ievadiet mērķa numura zīmi no darba.</span><span class="sxs-lookup"><span data-stu-id="adf06-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="adf06-297">Laukā **ID** ievadiet mērķa numura zīmes ID no darba informācijas.</span><span class="sxs-lookup"><span data-stu-id="adf06-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="adf06-298">Nosūtīšanas-pārkraušanas lapa ataino izdošanas vietu (*RECV*), mērķa numura zīmi (*numura zīmi*), krājumu (*A0001*) un daudzumu (*3*).</span><span class="sxs-lookup"><span data-stu-id="adf06-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="adf06-299">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-299">Select **OK**.</span></span>
1. <span data-ttu-id="adf06-300">Laukā **Mērķa LP** ievadiet mērķa numura zīmi numura zīmes ID, kas ir jānovieto (bez uzglabāšanas nosūtāms) uz nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="adf06-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="adf06-301">Varat atlasīt jebkuru numura zīmes ID pēc savas izvēles.</span><span class="sxs-lookup"><span data-stu-id="adf06-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="adf06-302">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-302">Select **OK**.</span></span>
1. <span data-ttu-id="adf06-303">Laukā **ID** ievadiet mērķa numura zīmes ID.</span><span class="sxs-lookup"><span data-stu-id="adf06-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="adf06-304">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-304">Select **OK**.</span></span>
1. <span data-ttu-id="adf06-305">Apstipriniet darbu, izdodot atlikušo daudzumu 2, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="adf06-306">Nākamajā lapā atlasiet **Gatavs**, lai beigtu izdošanas procesu un sāktu izvietošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="adf06-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="adf06-307">Mobilajā programmā ir ietverta vieta un noliktavas numura zīme krājuma novietošanai.</span><span class="sxs-lookup"><span data-stu-id="adf06-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="adf06-308">Apstipriniet lielapjoma glabāšanas **Izvietošanu**, atlasot **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="adf06-309">Nākamajā lapā apstipriniet nosūtīšanai bez uzglabāšanas **Izvietošanu**, atlasot **Labi**.</span><span class="sxs-lookup"><span data-stu-id="adf06-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="adf06-310">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="adf06-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="adf06-311">Atlasiet **Atcelt**, lai izietu.</span><span class="sxs-lookup"><span data-stu-id="adf06-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="adf06-312">Sekojošajā attēlā ir parādīts, kā programmā Microsoft Dynamics 365 Supply Chain Management var tikt parādīts aizpildīts nosūtīšanas bez uzglabāšanas darbs.</span><span class="sxs-lookup"><span data-stu-id="adf06-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="adf06-313">![Nosūtīšanas bez uzglabāšanas darbs ir pabeigts](media/PlannedCrossDockingWork.png "Nosūtīšanas bez uzglabāšanas darbs ir pabeigts")</span><span class="sxs-lookup"><span data-stu-id="adf06-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]