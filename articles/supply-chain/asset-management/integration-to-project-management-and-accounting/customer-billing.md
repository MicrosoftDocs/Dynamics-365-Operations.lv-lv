---
title: Rēķins par uzturēšanu debitora īpašumā aktīviem
description: Šajā tēmā skaidrots, kā izveidot, apstrādāt un izrakstīt rēķinu uzturēšanas darbu, kas tiek veikts jūsu debitoriem piederošām pamatlīdzekļiem.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a93436d101e6201c9d86279ea5b1a37fcc644fd1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500458"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="9b966-103">Rēķins par uzturēšanu debitora īpašumā aktīviem</span><span class="sxs-lookup"><span data-stu-id="9b966-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

<span data-ttu-id="9b966-104">*Darba pasūtījuma rēķinu izrakstīšanas* funkcija ļauj izveidot, apstrādāt un izrakstīt rēķinu uzturēšanas darbu, kas tiek veikts jūsu debitoriem piederošām pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="9b966-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="9b966-105">Šī funkcija ļauj veikt šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="9b966-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="9b966-106">Saistiet debitorus ar tiem piederošajiem pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="9b966-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="9b966-107">Atlasiet debitoru un skatiet līdzekļus, kas debitoram pieder, veidojot darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="9b966-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="9b966-108">Iestatiet pamatprojektu katram debitoram.</span><span class="sxs-lookup"><span data-stu-id="9b966-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="9b966-109">Reģistrējiet darba pasūtījumam stundas, krājumus, izdevumus un komisijas maksas un pēc tam vēlāk izveidojiet debitoram rēķina priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="9b966-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="9b966-110">Turklāt šī funkcija nodrošina sekojošo funkcionalitāti:</span><span class="sxs-lookup"><span data-stu-id="9b966-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="9b966-111">Projekta līgums no debitora pamatprojekta tiek automātiski kopēts uz atbilstošo darba pasūtījuma projektu.</span><span class="sxs-lookup"><span data-stu-id="9b966-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="9b966-112">Tagad līdzekļu vadība var izmantot *maksas* projekta darbības tipu gan darba pasūtījumu prognozēs, gan darba pasūtījumu žurnālos.</span><span class="sxs-lookup"><span data-stu-id="9b966-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="9b966-113">Ieslēdziet debitora maksājumu ieskatu līdzekli</span><span class="sxs-lookup"><span data-stu-id="9b966-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="9b966-114">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="9b966-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="9b966-115">Administratori var izmantot [funkciju pārvaldības](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="9b966-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="9b966-116">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="9b966-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9b966-117">**Modulis:** *Projektu pārvaldība un uzskaite*</span><span class="sxs-lookup"><span data-stu-id="9b966-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="9b966-118">**Funkcionalitātes nosaukums:** *Darba pasūtījuma norēķini*</span><span class="sxs-lookup"><span data-stu-id="9b966-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="9b966-119">Piemērs</span><span class="sxs-lookup"><span data-stu-id="9b966-119">Example scenario</span></span>

<span data-ttu-id="9b966-120">Lai uzzinātu, kā šī funkcija darbojas, aplukojiet nākamo situācijas paraugu.</span><span class="sxs-lookup"><span data-stu-id="9b966-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="9b966-121">Lai, izmantojot šo scenāriju, strādātu ar norādītajiem parauga ierakstiem un vērtībām, jāizmanto sistēma, kurā ir instalēti standarta [demonstrācijas dati](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9b966-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="9b966-122">Pirms sākat, jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="9b966-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="9b966-123">Varat arī izmantot šo scenāriju kā norādījumus, lai līdzekli lietotu darbā ar ražošanas sistēmu.</span><span class="sxs-lookup"><span data-stu-id="9b966-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="9b966-124">Tomēr šādā gadījumā jums ir jāaizstāj savas vērtības, un, iespējams, trūks dažu nepieciešamo ierakstu tipu, ko sniedz standarta demonstrācijas dati.</span><span class="sxs-lookup"><span data-stu-id="9b966-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="9b966-125">1. darbība: jauna projekta līguma izveide debitoram</span><span class="sxs-lookup"><span data-stu-id="9b966-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="9b966-126">Dodieties uz **Projektu vadība un uzskaite \> Projekti \> Projekta līgumi**.</span><span class="sxs-lookup"><span data-stu-id="9b966-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="9b966-127">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="9b966-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9b966-128">Dialoglodziņā **Jauns projekta līgums** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="9b966-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9b966-129">**Nosaukums:** *Pelican vairumtirdzniecība*</span><span class="sxs-lookup"><span data-stu-id="9b966-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="9b966-130">**Finansējuma tips:** *Debitors*</span><span class="sxs-lookup"><span data-stu-id="9b966-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="9b966-131">**Finansējuma avots:** *US-013* (*Pelican vairumtirdzniecība*)</span><span class="sxs-lookup"><span data-stu-id="9b966-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="9b966-132">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9b966-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="9b966-133">2. darbība: jauna projekta līguma izveide debitoram</span><span class="sxs-lookup"><span data-stu-id="9b966-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="9b966-134">Šeit izveidotais pamatprojekts tiks izmantots, veidojot debitora darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="9b966-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="9b966-135">Dodieties uz **Projektu vadība un uzskaite \> Projekti \> Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="9b966-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="9b966-136">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="9b966-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9b966-137">Dialoglodziņā **Jauns produkts** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="9b966-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9b966-138">**Projekta veids:** *Laiks un materiāls*</span><span class="sxs-lookup"><span data-stu-id="9b966-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="9b966-139">**Projekta nosaukums:** *Pelican vairumtirdzniecības darba pasūtījumi*</span><span class="sxs-lookup"><span data-stu-id="9b966-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="9b966-140">**Projektu grupa:** *TM*</span><span class="sxs-lookup"><span data-stu-id="9b966-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="9b966-141">**Projekta līguma ID:** *Pelican vairumtirdzniecība* (iepriekš izveidotais līgums)</span><span class="sxs-lookup"><span data-stu-id="9b966-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="9b966-142">**Sākuma datums:** atlasiet šodienas datumu.</span><span class="sxs-lookup"><span data-stu-id="9b966-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="9b966-143">Atlasiet **Izveidot projektu**.</span><span class="sxs-lookup"><span data-stu-id="9b966-143">Select **Create project**.</span></span>
1. <span data-ttu-id="9b966-144">Jaunais projekts ir atvērts.</span><span class="sxs-lookup"><span data-stu-id="9b966-144">The new project is opened.</span></span> <span data-ttu-id="9b966-145">Pierakstiet **Projekta ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="9b966-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="9b966-146">Tā būs jāievada vēlāk.</span><span class="sxs-lookup"><span data-stu-id="9b966-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="9b966-147">3. darbība: jauna darba pasūtījuma tipa izveide Līdzekļu pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="9b966-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="9b966-148">Atlasiet **Līdzekļu pārvaldība \> Iestatīšana \> Darba pasūtījumi \> Darba pasūtījumu veidi**.</span><span class="sxs-lookup"><span data-stu-id="9b966-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="9b966-149">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="9b966-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9b966-150">Sarakstam tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="9b966-150">A new record is added to the list.</span></span> <span data-ttu-id="9b966-151">Iestatiet rindai šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="9b966-151">Set the following values for it:</span></span>

    - <span data-ttu-id="9b966-152">**Darba pasūtījuma veids:** *Pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="9b966-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="9b966-153">**Nosaukums:** *Pakalpojuma darba pasūtījumi*</span><span class="sxs-lookup"><span data-stu-id="9b966-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="9b966-154">**Darba pasūtījuma dzīves cikla statuss:** *Standarts*</span><span class="sxs-lookup"><span data-stu-id="9b966-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="9b966-155">4. darbība: debitora konta saistīšana ar pamatprojektu</span><span class="sxs-lookup"><span data-stu-id="9b966-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="9b966-156">Tagad debitora konts ir jāsaista ar pamatprojektu Līdzekļu pārvaldības projektu iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="9b966-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="9b966-157">Dodieties uz **Līdzekļu pārvaldība \> Iestatīšana \> Darba pasūtījumi \> Projekta iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="9b966-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="9b966-158">Cilnē **Pamatprojekts** atlasiet **Pievienot**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="9b966-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="9b966-159">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="9b966-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9b966-160">**Debitora konts:** *US-013* (*Pelican vairumtirdzniecība*)</span><span class="sxs-lookup"><span data-stu-id="9b966-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="9b966-161">**Projekta ID:** Ievadiet projekta ID, kuru iepriekš atzīmējāt.</span><span class="sxs-lookup"><span data-stu-id="9b966-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="9b966-162">5. solis: projektu grupas un tipa saistīšana ar darba pasūtījuma projektu</span><span class="sxs-lookup"><span data-stu-id="9b966-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="9b966-163">Jums joprojām jābūt lapā **Projekta iestatījumi** (**Līdzekļu pārvaldība \>Iestatījumi \> Darba pasūtījumi \> Projekta iestatījumi**).</span><span class="sxs-lookup"><span data-stu-id="9b966-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="9b966-164">Cilnē **Projekta grupa** atlasiet **Pievienot**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="9b966-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="9b966-165">Jaunajā rindā iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="9b966-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9b966-166">**Darba pasūtījuma tips:** *Pakalpojums* (iepriekš izveidotais darba pasūtījuma tips)</span><span class="sxs-lookup"><span data-stu-id="9b966-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="9b966-167">**Projektu grupa:** *TM*</span><span class="sxs-lookup"><span data-stu-id="9b966-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="9b966-168">Projekta līgums darba pasūtījuma projektā vienmēr ir pārmantots no pamatprojekta.</span><span class="sxs-lookup"><span data-stu-id="9b966-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="9b966-169">6. darbība: līdzekļa saistīšana ar debitora ID</span><span class="sxs-lookup"><span data-stu-id="9b966-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="9b966-170">Dodieties uz **Līdzekļu pārvaldība \> Līdzekļi \> Aktīvie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="9b966-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="9b966-171">Laukā **Filtrs** ievadiet *VE-102 un* atlasiet, lai filtrētu pēc **Līdzekļiem**.</span><span class="sxs-lookup"><span data-stu-id="9b966-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="9b966-172">Atlasiet līdzekli, lai atvērtu tā iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="9b966-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="9b966-173">Kopsavilkuma cilnē **Klients** iestatiet lauku **Klienta konts** uz *US-013* (*Pelican vairumtirdzniecība*).</span><span class="sxs-lookup"><span data-stu-id="9b966-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="9b966-174">Lauks **Nosaukums** tiek automātiski atjaunināts uz *Pelican vairumtirdzniecība*.</span><span class="sxs-lookup"><span data-stu-id="9b966-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="9b966-175">7. darbība: jauna darba pasūtījuma tipa izveide līdzeklim</span><span class="sxs-lookup"><span data-stu-id="9b966-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="9b966-176">Dodieties uz **Līdzekļu pārvaldība \> Darba pasūtījumi \> Aktīvie darba pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="9b966-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="9b966-177">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="9b966-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9b966-178">Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:</span><span class="sxs-lookup"><span data-stu-id="9b966-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9b966-179">**Darba pasūtījuma veids:** *Pakalpojums*</span><span class="sxs-lookup"><span data-stu-id="9b966-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="9b966-180">**Apraksts:** *Kravas automašīnas remonts*</span><span class="sxs-lookup"><span data-stu-id="9b966-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="9b966-181">**Debitora konts:** *US-013* (*Pelican vairumtirdzniecība*)</span><span class="sxs-lookup"><span data-stu-id="9b966-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="9b966-182">**Pamatlīdzeklis:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="9b966-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="9b966-183">Uzmeklēšana parāda tikai līdzekļus, kas ir saistīti ar atlasīto debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="9b966-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="9b966-184">**Uzturēšanas darba veids:** *Labošana*</span><span class="sxs-lookup"><span data-stu-id="9b966-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="9b966-185">**Tirdzniecība:** *Mehānika*</span><span class="sxs-lookup"><span data-stu-id="9b966-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="9b966-186">**Pakalpojumu līmenis:** *4*</span><span class="sxs-lookup"><span data-stu-id="9b966-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="9b966-187">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9b966-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="9b966-188">8. darbība: darba pasūtījuma pārskatīšana un darba sākšana ar to</span><span class="sxs-lookup"><span data-stu-id="9b966-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="9b966-189">Šajā sadaļā jūs strādāsiet pie darba pasūtījuma, ko izveidojāt iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="9b966-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="9b966-190">Izpildiet šīs darbības, lai pārbaudītu, vai pamatprojekts ir *Pelican vairumtirdzniecības darba pasūtījuma* projekts:</span><span class="sxs-lookup"><span data-stu-id="9b966-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="9b966-191">Sadaļā **Darba pasūtījuma uzturēšanas darbi** atlasiet rindu.</span><span class="sxs-lookup"><span data-stu-id="9b966-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="9b966-192">Pārbaudiet **Projekta ID** vērtību kopsavilkuma cilnē **Detalizēta informācija par rindu**.</span><span class="sxs-lookup"><span data-stu-id="9b966-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="9b966-193">Veidlapā jābūt numuram ar defisi *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="9b966-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="9b966-194">Šī vērtība ir saite.</span><span class="sxs-lookup"><span data-stu-id="9b966-194">This value is a link.</span></span>
    1. <span data-ttu-id="9b966-195">Izvēlieties projekta ID saiti, lai atvērtu lapu, kur jūs variet skatīt projektu pamatprojektu un projektu nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="9b966-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="9b966-196">Darbību rūts cilnē **Darba pasūtījums** grupā **Dzīves cikla statuss** atlasiet **Atjaunināt darba pasūtījuma statusu**.</span><span class="sxs-lookup"><span data-stu-id="9b966-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="9b966-197">Dialoglodziņa **Atjaunināt darba pasūtījuma stāvokli** kolonnā **Atlasīt** atzīmējiet izvēles rūtiņu rindai, kurā lauks **Dzīves cikla stāvoklis** ir iestatīts uz *Notiek*.</span><span class="sxs-lookup"><span data-stu-id="9b966-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="9b966-198">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9b966-198">Select **OK**.</span></span>
1. <span data-ttu-id="9b966-199">Dialoglodziņā **Dzīves cikla stāvoklis: Notiek** atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9b966-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="9b966-200">9. darbība: darba pasūtījumam veltīto stundu grāmatošana un jauna rēķina priekšlikuma izveide</span><span class="sxs-lookup"><span data-stu-id="9b966-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="9b966-201">Šajā sadaļā jūs strādāsiet pie darba pasūtījuma, ko izveidojāt iepriekšējā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="9b966-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="9b966-202">Darbību rūts cilnē **Darba pasūtījumi**, grupā **Projekti**, atlasiet **Žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="9b966-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="9b966-203">Tiek parādīta lapa **Darba pasūtījumu žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="9b966-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="9b966-204">Šeit var reģistrēt laiku, kas pavadīts darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="9b966-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="9b966-205">Kopsavilkuma cilnē **Stundas** atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="9b966-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="9b966-206">Jaunajā rindā iestatiet laukam **Stundas** vērtību *4*.</span><span class="sxs-lookup"><span data-stu-id="9b966-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="9b966-207">Darbību rūtī atlasiet **Publicēt žurnālus**.</span><span class="sxs-lookup"><span data-stu-id="9b966-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="9b966-208">Aizveriet lapu **Darba pasūtījumu žurnāli**, lai atgrieztos darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="9b966-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="9b966-209">Darbību rūts cilnē **Rēķini** atlasiet **Jauna rēķina piedāvājums**.</span><span class="sxs-lookup"><span data-stu-id="9b966-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="9b966-210">Dialoglodziņa **Izveidot rēķina priekšlikumu** sadaļā **Projekta darbības** atzīmējiet **Izvēles** rūtiņu katrai rindai, ko vēlaties iekļaut rēķinā.</span><span class="sxs-lookup"><span data-stu-id="9b966-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="9b966-211">Atlasiet **Labi**, lai aizvērtu dialoglodziņu un skatītu jaunu rēķina piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="9b966-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]