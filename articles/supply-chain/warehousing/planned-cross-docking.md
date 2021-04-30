---
title: Plānotā pārkraušana sadales centrā
description: Šajā tēmā ir aprakstīta uzlabota plānotā pārkraušana sadales centrā, kur pasūtījumam nepieciešamais krājumu daudzums ir novirzīts tieši no saņemšanas vai izveides uz pareizo nosūtīšanas doku vai sagatavošanas apgabalu. Visi atlikušie krājumi no saņemšanas avota tiek novirzīti uz pareizo glabāšanas vietu, izmantojot regulāro izvietošanas procesu.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911252"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="3d8b0-104">Plānotā pārkraušana sadales centrā</span><span class="sxs-lookup"><span data-stu-id="3d8b0-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d8b0-105">Šī tēma apraksta detalizētu plānoto pārkraušanu sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="3d8b0-106">Šajā tēmā ir aprakstīta uzlabota plānotā pārkraušana sadales centrā, kur pasūtījumam nepieciešamais krājumu daudzums ir novirzīts tieši no saņemšanas vai izveides uz pareizo nosūtīšanas doku vai sagatavošanas apgabalu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="3d8b0-107">Visi atlikušie krājumi no saņemšanas avota tiek novirzīti uz pareizo glabāšanas vietu, izmantojot regulāro izvietošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="3d8b0-108">Pārkraušana sadales centrā ļauj darbiniekiem izlaist ienākošo krājumu izvietošanu un izejošo krājumu izsniegšanu, kas jau ir atzīmēta izejošam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="3d8b0-109">Tāpēc, krājuma saskares reižu skaits tiek minimizēts iespēju robežās.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="3d8b0-110">Turklāt, ņemot vērā, ka ir mazāka mijiedarbība ar sistēmu, laika un vietas ietaupījums noliktavas ražotnē ir palielināts.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="3d8b0-111">Pirms var veikt pārkraušanu sadales centrā, ir jākonfigurē jauna nosūtīšanas nosūtīšanai paredzētā veidne, kurā ir norādīts piegādes avots un citas prasību kopas pārkraušanai sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="3d8b0-112">Kad izejošais pasūtījums ir izveidots, rinda ir jāatzīmē ar ienākošo pasūtījumu, kas ietver to pašu elementu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="3d8b0-113">Varat izvēlēties direktīvas koda lauku veidnē Pārkraušana sadales centrā, kas ir līdzīgs tam, kā iestatījāt papildināšanas un pirkšanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="3d8b0-114">Saņemšanas pasūtījuma saņemšanas laikā pārkraušanas sadales centrā iestatījums automātiski nosaka nepieciešamību veikt pārkraušanu sadales centrā un izveido vajadzīgā daudzuma kustības darbu, pamatojoties uz novietojuma direktīvas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="3d8b0-115">Krājumu darbības *tiek* reģistrētas, atceļot pārkraušanas sadales centrā darbu, pat ja iestatījumi šai iespējai ir ieslēgti Noliktavas pārvaldības parametros.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="3d8b0-116">Iespējot plānotās pārkraušanas opcijas</span><span class="sxs-lookup"><span data-stu-id="3d8b0-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="3d8b0-117">Ja sistēmā vēl nav ietverti šajā tēmā aprakstītie līdzekļi, pārejiet uz sadaļu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet tālāk norādītās funkcijas šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="3d8b0-118">*Plānotā pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="3d8b0-119">*Pārkraušana sadales centrā — veidnes ar atrašanās vietas norādēm*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="3d8b0-120">Šis līdzeklis ļauj lauku **Direktīvas kods** norādīt veidnē Pārkraušana sadales centrā līdzīgi tam, kā iestatījāt papildināšanas veidnes.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="3d8b0-121">Šī līdzekļa iespējošana neļauj galarezultātā pievienot direktīvas kodu darba veidnes Pārkraušana sadales centrā rindām pēdējai *Izvietojuma* rindai.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="3d8b0-122">Tas nodrošina, ka darba izveides laikā var noteikt pēdējo izvietošanas novietojumu, pirms tiek apsvērtas darba veidnes.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="3d8b0-123">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="3d8b0-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="3d8b0-124">Atkārtoti ģenerēt noslodzes grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="3d8b0-124">Regenerate load posting methods</span></span>

<span data-ttu-id="3d8b0-125">Plānotā pārkraušana sadales centrā tiek ieviesta kā noslodzes grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="3d8b0-126">Pēc opcijas iespējošanas ir atkārtoti jāģenerē metodes.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="3d8b0-127">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noslodzes grāmatošanas metodes**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="3d8b0-128">Darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="3d8b0-129">Kad reģenerācija ir pabeigta, ir jābūt redzamai metodei ar **Metodes nosaukuma** vērtību *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="3d8b0-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="3d8b0-131">Izveidojiet pārkraušanas sadales centra veidni</span><span class="sxs-lookup"><span data-stu-id="3d8b0-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="3d8b0-132">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Darbs \> Pārkraušanas sadales centrā veidnes**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="3d8b0-133">Lai izveidotu veidni, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="3d8b0-134">Galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-135">**Secība:** *1*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="3d8b0-136">Šis lauks nosaka secību, kādā tiek novērtētas veidnes.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="3d8b0-137">**Pārkraušanas sadales centra veidnes ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="3d8b0-138">**Apraksts:** *Noliktava 51*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="3d8b0-139">**Pieprasījuma izlaides politika:** *Kvīts pirms piegādes*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="3d8b0-140">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="3d8b0-141">Kopsavilkuma cilnes **Plānošana** iestatījums kontrolē veidnes darbību.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="3d8b0-142">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-142">Set the following values:</span></span>

    - <span data-ttu-id="3d8b0-143">**Pieprasījuma prasības:** *Nav*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="3d8b0-144">Šis lauks nosaka pieprasījuma krājumu vajadzības.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="3d8b0-145">Ja pieprasījumam ir jābūt saistītam ar piegādi pirms nodošanas, atlasiet *Iezīmēšana*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="3d8b0-146">Ja pieprasījumam ir jābūt rezervētam pasūtījumam pirms nodošanas, atlasiet *Pasūtījuma rezervācija*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="3d8b0-147">**Atrašanas tips:** *Piegādes vietas*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="3d8b0-148">Šis lauks nosaka, vai pārkraušanai sadales centrā ir jāizmanto nosūtījuma sagatavošanas/noslodzes vietas, vai arī ir jāizmanto novietojuma direktīvas, lai atrastu savas sagatavošanas/noslodzes vietas.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="3d8b0-149">**Darba veidne:** Atstājiet šo lauku tukšu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="3d8b0-150">Šis lauks definē darba veidni, kas jāizmanto, izveidojot pārkraušanas sadales centrā darbu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="3d8b0-151">**Atkārtoti apliecināt piegādes kvīti:** *Nē*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="3d8b0-152">Šī opcija nosaka, vai, saņemot kvīti, ir atkārtoti jāapliecina piegāde.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="3d8b0-153">Ja šī opcija ir iestatīta uz *Jā*, ir jāpārbauda gan maksimālais laika logs, gan beigu dienu diapazons.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="3d8b0-154">**Direktīvas kods:** atstājiet šo lauku tukšu</span><span class="sxs-lookup"><span data-stu-id="3d8b0-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="3d8b0-155">Šo opciju aktivizē līdzeklis *Veidnes Pārkraušana sadales centrā ar novietojuma direktīvam*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="3d8b0-156">Sistēma izmanto novietojuma direktīvas, lai palīdzētu noteikt labāko novietojumu, uz kuru pārvietot krājumus pārkraušanai sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="3d8b0-157">To var iestatīt, katrai atbilstošai veidnei pārkraušanai sadales centrā piešķirot direktīvas kodu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="3d8b0-158">Ja direktīvas kods ir iestatīts, sistēma meklē vietas direktīvas pēc direktīvas koda, ģenerējot darbu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="3d8b0-159">Šādā veidā var ierobežot novietojuma direktīvas, kas tiek izmantotas noteiktai veidnei Pārkraušana sadales centrā.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="3d8b0-160">**Validēt maksimālo laika logu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="3d8b0-161">Šī opcija nosaka, vai maksimālais laika logs ir jānovērtē, kad ir atlasīts piegādes avots.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="3d8b0-162">Ja šī opcija ir iestatīta uz *Jā*, ir pieejami lauki, kas saistīti ar maksimālo un minimālo laiku logiem.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="3d8b0-163">**Maksimālā laika logs:** *5*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="3d8b0-164">Šis lauks nosaka maksimālo atļauto laika periodu starp piegādes saņemšanu un pieprasījuma izsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="3d8b0-165">**Maksimālais laika loga bloks:** *Dienas*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="3d8b0-166">**Minimālais laika logs:** *0*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="3d8b0-167">Šis lauks nosaka minimālo atļauto laika periodu starp piegādes saņemšanu un pieprasījuma izsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="3d8b0-168">**Minimālā laika loga vienība:** *Dienas*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="3d8b0-169">**Termiņa beigu dienu diapazons:** *0*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="3d8b0-170">*Pirmā beigu datuma (FEFO) kritēriji:* Šis lauks nosaka maksimālo dienu skaitu starp pirmās beigu partijas, kas pašlaik atrodas noliktavā, beigu datumu un saņemto partiju.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="3d8b0-171">Kopsavilkuma cilnē **Piegādes avoti** norādiet šai veidnei derīgus piegādes tipus.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="3d8b0-172">Atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="3d8b0-173">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="3d8b0-174">**Piegādes avots:** *Pirkuma pasūtījums*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="3d8b0-175">Darba klases izveide</span><span class="sxs-lookup"><span data-stu-id="3d8b0-175">Create a work class</span></span>

1. <span data-ttu-id="3d8b0-176">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba klases**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="3d8b0-177">Lai izveidotu darba klasi, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="3d8b0-178">Iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-178">Set the following values:</span></span>

    - <span data-ttu-id="3d8b0-179">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="3d8b0-180">**Apraksts:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="3d8b0-181">**Darba pasūtījuma tips:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="3d8b0-182">Izveidojiet darba veidni</span><span class="sxs-lookup"><span data-stu-id="3d8b0-182">Create a work template</span></span>

1. <span data-ttu-id="3d8b0-183">Doties uz **Noliktavas vadība \> Iestatīšana \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="3d8b0-184">Laukā **Darba pasūtījuma veids** atlasiet *Pārkraušana sadales centrā*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="3d8b0-185">Lai pievienotu rindu cilnē **Pārskats**, darbības rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="3d8b0-186">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-187">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="3d8b0-188">**Pārkraušanas veidne:** *51 Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="3d8b0-189">**Pārkraušanas veidnes apraksts:** *51 Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="3d8b0-190">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Darba veidnes informācija**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="3d8b0-191">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="3d8b0-192">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-193">**Darba veids:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="3d8b0-194">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="3d8b0-195">Atlasiet **Jauns**, lai pievienotu citu rindu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="3d8b0-196">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="3d8b0-197">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="3d8b0-198">Atlasiet **Saglabāt** un apstipriniet, ka ir atlasīta rūtiņa **Derīgs** veidnei *51 Pārkraušana sadales centrā*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="3d8b0-199">Darba klases ID *Izdošanas* un *Izvietošanas* darbu tipiem jābūt vienādiem.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="3d8b0-200">Novietojuma direktīvu izveide</span><span class="sxs-lookup"><span data-stu-id="3d8b0-200">Create location directives</span></span>

1. <span data-ttu-id="3d8b0-201">Dodieties uz **Noliktavas vadība \> Iestatījumi \> Novietojuma direktīvas**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="3d8b0-202">Laukā **Darba pasūtījuma veids** atlasiet *Pārkraušana sadales centrā*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="3d8b0-203">Darbību rūtī atlasiet **Jauns**, un pēc tam iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="3d8b0-204">**Secības numurs:** *1*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="3d8b0-205">**Nosaukums:** *51 Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="3d8b0-206">**Darba veids:** *Izvietošana*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="3d8b0-207">**Vieta:** *5*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-207">**Site:** *5*</span></span>
    - <span data-ttu-id="3d8b0-208">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="3d8b0-209">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="3d8b0-210">Kopsavilkuma cilnē **Rindas** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="3d8b0-211">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-212">**No daudzuma:** *1*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="3d8b0-213">**Līdz daudzumam:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="3d8b0-214">Atlasiet **Saglabāt**, lai padarītu pieejamu kopsavilkuma cilni **Novietojuma direktīvu darbības**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="3d8b0-215">Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="3d8b0-216">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-217">**Nosaukums:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="3d8b0-218">**Fiksēta novietojuma lietojums:** *Fiksētas un nefiksētas vietas*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="3d8b0-219">Atlasiet **Saglabāt**, lai padarītu pogu **Rediģēt vaicājumu** rīkjoslā **Novietojuma direktīvu darbības** pieejamu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="3d8b0-220">Atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktoru.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="3d8b0-221">Cilnē **Diapazons** pārliecinieties, ka šīs divas rindas ir konfigurētas:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="3d8b0-222">1. rinda:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-222">Line 1:</span></span>

        - <span data-ttu-id="3d8b0-223">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="3d8b0-224">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="3d8b0-225">**Lauks:** *Noliktava*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="3d8b0-226">**Kritēriji:** *51*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="3d8b0-227">2. rinda:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-227">Line 2:</span></span>

        - <span data-ttu-id="3d8b0-228">**Tabula:** *Novietojumi*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="3d8b0-229">**Atvasinātā tabula:** *Vietas*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="3d8b0-230">**Lauks:** *Novietojums*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="3d8b0-231">**Kritēriji:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="3d8b0-232">Atlasiet **Labi**, lai aizvērtu vaicājuma lapu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="3d8b0-233">Mobilās ierīces izvēlnes elementa izveide</span><span class="sxs-lookup"><span data-stu-id="3d8b0-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="3d8b0-234">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="3d8b0-235">Kreisās rūts izvēlnes elementu sarakstā atlasiet **Pirkumu izvietošana**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="3d8b0-236">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-236">Select **Edit**.</span></span>
1. <span data-ttu-id="3d8b0-237">Kopsavilkuma cilnē **Darba klases** atlasiet **Jauns**, lai pievienotu režģim rindu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="3d8b0-238">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-239">**Darba klases ID:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="3d8b0-240">**Darba pasūtījuma tips:** *Pārkraušana sadales centrā*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="3d8b0-241">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="3d8b0-242">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="3d8b0-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="3d8b0-243">Pirkuma pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="3d8b0-243">Create a purchase order</span></span>

<span data-ttu-id="3d8b0-244">Sekojiet šiem soļiem, lai izveidotu pirkuma pasūtījumu kā piegādes avotu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="3d8b0-245">Dodieties uz **Sagāde un avoti \> Pirkuma pasūtījumi \> Visi pirkuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="3d8b0-246">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3d8b0-247">Dialoglodziņā **Izveidot pirkuma pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-248">**Tirgotāja konts:** *104*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="3d8b0-249">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="3d8b0-250">Atlasiet **Labi** un pierakstiet pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="3d8b0-251">Kopsavilkuma cilnei **Pirkuma pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="3d8b0-252">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-253">**Elementa numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3d8b0-254">**Daudzums:** *5*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="3d8b0-255">Izveidot pārdošanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="3d8b0-255">Create a sales order</span></span>

<span data-ttu-id="3d8b0-256">Sekojiet šiem soļiem, lai izveidotu pārdošanas pasūtījumu kā piegādes avotu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="3d8b0-257">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="3d8b0-258">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3d8b0-259">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-260">**Klienta konts:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="3d8b0-261">**Noliktava:** *51*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="3d8b0-262">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-262">Select **OK**.</span></span>
1. <span data-ttu-id="3d8b0-263">Kopsavilkuma cilnei **Pārdošanas pasūtījuma rindas** tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="3d8b0-264">Iestatiet šādas vērtības šai rindai:</span><span class="sxs-lookup"><span data-stu-id="3d8b0-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="3d8b0-265">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3d8b0-266">**Daudzums:** *3*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="3d8b0-267">Izveidot plānoto pārkraušanu sadales centrā</span><span class="sxs-lookup"><span data-stu-id="3d8b0-267">Create planned cross-docking</span></span>

<span data-ttu-id="3d8b0-268">Sekojiet šiem soļiem, lai izveidotu plānoto pārkraušanu sadales centrā no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="3d8b0-269">Lapā **Pārdošanas pasūtījuma detalizēta informācija** lapā tikko izveidotajam pārdošanas pasūtījumam atlasiet darbības rūtī cilnē **Noliktava** grupā **Darbības** atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="3d8b0-270">Darbība nodot noliktavā izveido sūtījumu un noslodzes rindu pārdošanas pasūtījuma rindai un mēģina piešķirt krājumus.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="3d8b0-271">Tiek parādīts informatīvs ziņojums.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-271">You receive an informational message.</span></span> <span data-ttu-id="3d8b0-272">Tiek parādīts arī šāds brīdinājuma ziņojums: "Ar kopumu XXXX netika izveidots neviens darbs.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="3d8b0-273">Detalizētu informāciju meklējiet darba izveides vēstures žurnālā. "</span><span class="sxs-lookup"><span data-stu-id="3d8b0-273">See the work creation history log for details."</span></span> <span data-ttu-id="3d8b0-274">Šī darbība ir paredzama, jo noliktavā nav krājumu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="3d8b0-275">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Noliktava** atlasiet **Detalizēta informācija par nosūtīšanu**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="3d8b0-276">Tiek parādīta lapa **Detalizēta informācija par nosūtīšanu**, un tā parāda sūtījumu, kas tika izveidots pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="3d8b0-277">Kopsavilkuma cilnē **Noslodzes rindas** ievērojiet, ka **Plānotais pārkraušanas sadales centrā daudzums** ir iestatīts uz *3*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="3d8b0-278">Tā kā noliktavā nav pieejami krājumi, bet derīgs piegādes avots ieradīsies laika loga ietvaros, kas ir definēts nosūtīšanas pārkraušanas veidnē, tika izveidots nosūtīšanas pārkraušanas daudzums.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="3d8b0-279">Kopsavilkuma cilnē **Noslodzes rindas** atlasiet **Plānotā nosūtīšana-pārkraušana**, lai skatītu detalizētu informāciju par izveidoto nosūtīšanu-pārkraušanu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="3d8b0-280">Apstrādāt pārkraušanu sadales centrā</span><span class="sxs-lookup"><span data-stu-id="3d8b0-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="3d8b0-281">Pirkuma pasūtījuma saņemšana, izmantojot noliktavas mobilo programmu</span><span class="sxs-lookup"><span data-stu-id="3d8b0-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="3d8b0-282">Sistēma saņems 5 elementu daudzumu no pirkuma pasūtījuma saņemšanas vietā un izveidos divus darba gabalus.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="3d8b0-283">Pirmajam izveidotajam darba ID ir **Darba pasūtījuma tipa** vērtība *Pārkraušana sadales centrā*, un tā ir saistīta ar pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="3d8b0-284">Tā daudzums ir 3, un tas ir novirzīts uz galīgo nosūtīšanas vietu, lai to varētu nosūtīt nekavējoties.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="3d8b0-285">Otrajam izveidotajam darba ID ir **Darba pasūtījuma tipa** vērtība *Pirkuma pasūtījumi*, un tā ir saistīta ar pirkuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="3d8b0-286">Tā atlikušais daudzums ir 2, kas netika nodots nosūtīšanai, un tas ir novirzīts izvietošanai noliktavā.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="3d8b0-287">Pierakstieties mobilajā ierīcē kā lietotājs noliktavā *51*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="3d8b0-288">Doties uz **Ienākošie \> Pirkumu saņemšana**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="3d8b0-289">Laukā **PONum** ievadiet savu pirkuma pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="3d8b0-290">Laukā **Daudzums** ievadiet *5*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="3d8b0-291">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-291">Select **OK**.</span></span>
1. <span data-ttu-id="3d8b0-292">Nākamajā lapā iestatiet lauku **Elements** uz *A0001*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="3d8b0-293">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-293">Select **OK**.</span></span>
1. <span data-ttu-id="3d8b0-294">Nākamajā lapā apstipriniet **PONum**, **Elements** un **Daudzums** vērtības, atlasot **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="3d8b0-295">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="3d8b0-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="3d8b0-296">Atlasiet **Atcelt**, lai izietu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="3d8b0-297">Nosūtīšanas-pārkraušanas un lielapjoma preču izvietošana</span><span class="sxs-lookup"><span data-stu-id="3d8b0-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="3d8b0-298">Patlaban abiem darba ID ir vienāda mērķa numura zīme.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="3d8b0-299">Lai veiktu nākamās darbības, ir jāiegūst darba ID un mērķa numura zīmes ID.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="3d8b0-300">Šo informāciju var iegūt no detalizētas informācijas par pirkuma pasūtījuma rindu un pārdošanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="3d8b0-301">Pārmaiņus varat doties uz **Noliktavas pārvaldība \> Darbs \> Darba detaļas** un filtrēt darbu, kur **Noliktavas** vērtība ir *51*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="3d8b0-302">Mobilajā ierīcē atveriet **Ienākošie \> Pirkumu izvietošana** un ievadiet mērķa numura zīmi no darba.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="3d8b0-303">Laukā **ID** ievadiet mērķa numura zīmes ID no darba informācijas.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="3d8b0-304">Nosūtīšanas-pārkraušanas lapa ataino izdošanas vietu (*RECV*), mērķa numura zīmi (*numura zīmi*), krājumu (*A0001*) un daudzumu (*3*).</span><span class="sxs-lookup"><span data-stu-id="3d8b0-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="3d8b0-305">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-305">Select **OK**.</span></span>
1. <span data-ttu-id="3d8b0-306">Laukā **Mērķa LP** ievadiet mērķa numura zīmi numura zīmes ID, kas ir jānovieto (bez uzglabāšanas nosūtāms) uz nosūtīšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="3d8b0-307">Varat atlasīt jebkuru numura zīmes ID pēc savas izvēles.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="3d8b0-308">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-308">Select **OK**.</span></span>
1. <span data-ttu-id="3d8b0-309">Laukā **ID** ievadiet mērķa numura zīmes ID.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="3d8b0-310">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-310">Select **OK**.</span></span>
1. <span data-ttu-id="3d8b0-311">Apstipriniet darbu, izdodot atlikušo daudzumu 2, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="3d8b0-312">Nākamajā lapā atlasiet **Gatavs**, lai beigtu izdošanas procesu un sāktu izvietošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="3d8b0-313">Mobilajā programmā ir ietverta vieta un noliktavas numura zīme krājuma novietošanai.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="3d8b0-314">Apstipriniet lielapjoma glabāšanas **Izvietošanu**, atlasot **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="3d8b0-315">Nākamajā lapā apstipriniet nosūtīšanai bez uzglabāšanas **Izvietošanu**, atlasot **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="3d8b0-316">Tiek saņemts ziņojums "Darbība pabeigta".</span><span class="sxs-lookup"><span data-stu-id="3d8b0-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="3d8b0-317">Atlasiet **Atcelt**, lai izietu.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="3d8b0-318">Sekojošajā attēlā ir parādīts, kā programmā Microsoft Dynamics 365 Supply Chain Management var tikt parādīts aizpildīts nosūtīšanas bez uzglabāšanas darbs.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="3d8b0-319">![Nosūtīšanas bez uzglabāšanas darbs ir pabeigts](media/PlannedCrossDockingWork.png "Nosūtīšanas bez uzglabāšanas darbs ir pabeigts")</span><span class="sxs-lookup"><span data-stu-id="3d8b0-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]