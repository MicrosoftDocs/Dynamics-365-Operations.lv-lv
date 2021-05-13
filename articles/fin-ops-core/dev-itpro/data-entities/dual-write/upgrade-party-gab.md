---
title: Jaunināšana uz pušu un globālās adrešu grāmatas modeli
description: Šajā tēmā ir aprakstīts, kā jaunināt dubultās rakstīšanas datus puses un globālās adrešu grāmatas modelī.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 32128d48bfac195530d70b60e67cfd4921fc001e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941087"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="61e06-103">Jaunināšana uz pušu un globālās adrešu grāmatas modeli</span><span class="sxs-lookup"><span data-stu-id="61e06-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="61e06-104">Šī [Azure datu fabrikas veidne](https://aka.ms/dual-write-gab-adf) palīdz jaunināt esošo **Konta**, **Kontaktpersonas** un **Kreditora** tabulas datus dubultās rakstīšanas puses un globālās adrešu grāmatas modelī.</span><span class="sxs-lookup"><span data-stu-id="61e06-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="61e06-105">Veidne saskaņo datus no Finance and Operations programmām un Customer Engagement programmām.</span><span class="sxs-lookup"><span data-stu-id="61e06-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="61e06-106">Procesa beigās **Puses** ierakstu **Puses** un **Kontaktpersonas** lauki tiks izveidoti un saistīti ar **Konta**, **Kontaktpersonas** un **Kreditora** ierakstiem Customer Engagement programmās.</span><span class="sxs-lookup"><span data-stu-id="61e06-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="61e06-107">Tiek ģenerēts .csv fails (`FONewParty.csv`), lai izveidotu jaunus **Puses** ierakstus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61e06-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="61e06-108">Šajā tēmā ir sniegtas norādes par datu fabrikas veidnes lietošanu un datu jaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="61e06-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="61e06-109">Ja jums nav nekādu pielāgojumu, varat izmantot veidni, kāda tā ir.</span><span class="sxs-lookup"><span data-stu-id="61e06-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="61e06-110">Ja ir pielāgojumi **Kontam**, **Kontaktpersonai** un **Kreditoram** veidne jāmodificē, izmantojot tālāk norādītās instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="61e06-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="61e06-111">Veidne palīdz jaunināt tikai **Puses** datus.</span><span class="sxs-lookup"><span data-stu-id="61e06-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="61e06-112">Nākamajā laidienā tiks iekļautas pasta un elektroniskās adreses.</span><span class="sxs-lookup"><span data-stu-id="61e06-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="61e06-113">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="61e06-113">Prerequisites</span></span>

<span data-ttu-id="61e06-114">Ir nepieciešami šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="61e06-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="61e06-115">Azure abonements</span><span class="sxs-lookup"><span data-stu-id="61e06-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="61e06-116">Piekļuve veidnei</span><span class="sxs-lookup"><span data-stu-id="61e06-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="61e06-117">Jūs esat jau esošs duālās rakstīšanas debitors.</span><span class="sxs-lookup"><span data-stu-id="61e06-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="61e06-118">Sagatavoties jaunināšanai</span><span class="sxs-lookup"><span data-stu-id="61e06-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="61e06-119">**Pilnībā sinhronizēts**: abas vides ir pilnībā sinhronizētas **Kontam (Debitoram)**, **Kontaktpersonai** un **Kreditoram**.</span><span class="sxs-lookup"><span data-stu-id="61e06-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="61e06-120">**Integrācijas atslēgas**: tabulas **Konts (Debitors)**, **Kontaktpersona** un **Kreditors** Customer Engagement programmās izmanto integrācijas atslēgas, kas nosūtītas nestandarti.</span><span class="sxs-lookup"><span data-stu-id="61e06-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="61e06-121">Pielāgojot integrācijas atslēgas, veidne ir jāpielāgo.</span><span class="sxs-lookup"><span data-stu-id="61e06-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="61e06-122">**Puses numurs**: visiem **Konta (Debitora)**, **Kontaktpersonas** un **Kreditora** ierakstiem, kas tiks jaunināti, ir **Puses** numurs.</span><span class="sxs-lookup"><span data-stu-id="61e06-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="61e06-123">Ieraksti bez **Puses** numura tiks ignorēti.</span><span class="sxs-lookup"><span data-stu-id="61e06-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="61e06-124">Ja vēlaties jaunināt šos ierakstus, pirms jaunināšanas procesa sākšanas pievienojiet tiem **Puses** numuru.</span><span class="sxs-lookup"><span data-stu-id="61e06-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="61e06-125">**Sistēmas noplūde**: jaunināšanas laikā jums būs jāizmanto gan Finance and Operations, gan Customer Engagement vides bezsaistē.</span><span class="sxs-lookup"><span data-stu-id="61e06-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="61e06-126">**Momentuzņēmums**: izveidot momentuzņēmumus gan no Finance and Operations, gan no Customer Engagement programmām.</span><span class="sxs-lookup"><span data-stu-id="61e06-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="61e06-127">Izmantojiet momentuzņēmumus, lai atjaunotu iepriekšējo stāvokli, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="61e06-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="61e06-128">Izvietojums</span><span class="sxs-lookup"><span data-stu-id="61e06-128">Deployment</span></span>

1. <span data-ttu-id="61e06-129">Lejupielādējiet veidni no [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="61e06-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="61e06-130">Pierakstīšanās programmā [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="61e06-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="61e06-131">Izveidojiet [resursu grupu](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="61e06-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="61e06-132">Izveidojiet [glabāšanas kontu](/azure/storage/common/storage-account-create?tabs=azure-portal) izveidoto resursu grupā.</span><span class="sxs-lookup"><span data-stu-id="61e06-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="61e06-133">Izveidojiet [datu fabriku](/azure/data-factory/quickstart-create-data-factory-portal) virs izveidotās resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="61e06-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="61e06-134">Atveriet datu fabriku un atlasiet elementu **Autors & Pārraudzīt**.</span><span class="sxs-lookup"><span data-stu-id="61e06-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="61e06-135">Cilnē **Pārvaldīt** atlasiet **ARM veidne**.</span><span class="sxs-lookup"><span data-stu-id="61e06-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="61e06-136">Izvēlieties **Importēt ARM veidni**, lai importētu **Puses** veidni.</span><span class="sxs-lookup"><span data-stu-id="61e06-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="61e06-137">Importējiet veidni datu fabrikā.</span><span class="sxs-lookup"><span data-stu-id="61e06-137">Import the template into the data factory.</span></span> <span data-ttu-id="61e06-138">Ievadiet tālāk norādītās vērtības **Projekta detalizēta informācija** un **Instances detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="61e06-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="61e06-139">Lauks</span><span class="sxs-lookup"><span data-stu-id="61e06-139">Field</span></span> | <span data-ttu-id="61e06-140">Vērtība</span><span class="sxs-lookup"><span data-stu-id="61e06-140">Value</span></span>
    ---|---
    <span data-ttu-id="61e06-141">Abonements</span><span class="sxs-lookup"><span data-stu-id="61e06-141">Subscription</span></span> | <span data-ttu-id="61e06-142">Azure abonements</span><span class="sxs-lookup"><span data-stu-id="61e06-142">Azure subscription</span></span>
    <span data-ttu-id="61e06-143">Resursa grupa</span><span class="sxs-lookup"><span data-stu-id="61e06-143">Resource group</span></span> | <span data-ttu-id="61e06-144">Nodrošiniet to pašu resursu, kurā ir izveidots glabāšanas konts.</span><span class="sxs-lookup"><span data-stu-id="61e06-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="61e06-145">Reģions</span><span class="sxs-lookup"><span data-stu-id="61e06-145">Region</span></span> | <span data-ttu-id="61e06-146">Norādīt reģionu.</span><span class="sxs-lookup"><span data-stu-id="61e06-146">Specify region.</span></span>
    <span data-ttu-id="61e06-147">Fabrikas nosaukums</span><span class="sxs-lookup"><span data-stu-id="61e06-147">Factory Name</span></span> | <span data-ttu-id="61e06-148">Norādiet fabrikas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="61e06-148">Specify factory name.</span></span>
    <span data-ttu-id="61e06-149">FO saistīta Pakalpojums_pakalpojums galvenā atslēga</span><span class="sxs-lookup"><span data-stu-id="61e06-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="61e06-150">Norādiet pieteikuma atslēgu.</span><span class="sxs-lookup"><span data-stu-id="61e06-150">Specify the application's key.</span></span>
    <span data-ttu-id="61e06-151">Azure Blob krātuves_savienojuma virknes</span><span class="sxs-lookup"><span data-stu-id="61e06-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="61e06-152">Azure Blob krātuves savienojuma virkne.</span><span class="sxs-lookup"><span data-stu-id="61e06-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="61e06-153">Dynamics CRM saistīta Pakalpojuma_parole</span><span class="sxs-lookup"><span data-stu-id="61e06-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="61e06-154">Parole lietotāja kontam, kuru norādījāt kā lietotājvārdu.</span><span class="sxs-lookup"><span data-stu-id="61e06-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="61e06-155">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_url</span><span class="sxs-lookup"><span data-stu-id="61e06-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="61e06-156">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_nomnieks</span><span class="sxs-lookup"><span data-stu-id="61e06-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="61e06-157">Norādiet informāciju par nomnieku (domēna vārdu vai nomnieka ID), kurā atrodas jūsu pieteikums.</span><span class="sxs-lookup"><span data-stu-id="61e06-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="61e06-158">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_aad Resursa ID</span><span class="sxs-lookup"><span data-stu-id="61e06-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="61e06-159">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_pakalpojums Galvenā ID</span><span class="sxs-lookup"><span data-stu-id="61e06-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="61e06-160">Norādiet pieteikuma debitora ID.</span><span class="sxs-lookup"><span data-stu-id="61e06-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="61e06-161">Dynamics CRM saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_lietotājvārds</span><span class="sxs-lookup"><span data-stu-id="61e06-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="61e06-162">Lietotājvārds, ar kuru jāizveido savienojums ar Dynamics.</span><span class="sxs-lookup"><span data-stu-id="61e06-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="61e06-163">Papildinformāciju skatiet šeit: [Manuāli veicināt Resource Manager veidni katrai videi](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Saistīto pakalpojumu rekvizīti](/azure/data-factory/connector-dynamics-ax#linked-service-properties) un [Kopēt datus, izmantojot Azure datu fabriku](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="61e06-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="61e06-164">Pēc izvietošanas validējiet datu fabrikas datu kopas, datu plūsmu un saistīto pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="61e06-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datu kopas, datu plūsma un saistītais pakalpojums](media/data-factory-validate.png)

11. <span data-ttu-id="61e06-166">Dodieties uz **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="61e06-166">Navigate to **Manage**.</span></span> <span data-ttu-id="61e06-167">Sadaļā **Savienojumi** atlasiet **Saistītais pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="61e06-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="61e06-168">Atlasiet **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="61e06-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="61e06-169">Formā **Rediģēt saistīto pakalpojumu (Dynamics CRM)** ievadiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="61e06-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="61e06-170">Lauks</span><span class="sxs-lookup"><span data-stu-id="61e06-170">Field</span></span> | <span data-ttu-id="61e06-171">Vērtība</span><span class="sxs-lookup"><span data-stu-id="61e06-171">Value</span></span>
    ---|---
    <span data-ttu-id="61e06-172">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="61e06-172">Name</span></span> | <span data-ttu-id="61e06-173">Atlasiet DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="61e06-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="61e06-174">Apraksts</span><span class="sxs-lookup"><span data-stu-id="61e06-174">Description</span></span> | <span data-ttu-id="61e06-175">Saistītie pakalpojumi, kas ir jāsavieno ar CRM instanci, lai ienestu elementu datus</span><span class="sxs-lookup"><span data-stu-id="61e06-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="61e06-176">Izveidot savienojumu, izmantojot integrācijas izpildlaiku</span><span class="sxs-lookup"><span data-stu-id="61e06-176">Connect via integration runtime</span></span> | <span data-ttu-id="61e06-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="61e06-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="61e06-178">Izvietošanas veids</span><span class="sxs-lookup"><span data-stu-id="61e06-178">Deployment type</span></span> | <span data-ttu-id="61e06-179">Tiešsaiste</span><span class="sxs-lookup"><span data-stu-id="61e06-179">Online</span></span>
    <span data-ttu-id="61e06-180">Pakalpojuma Uri</span><span class="sxs-lookup"><span data-stu-id="61e06-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="61e06-181">Autentifikācijas veids</span><span class="sxs-lookup"><span data-stu-id="61e06-181">Authentication type</span></span> | <span data-ttu-id="61e06-182">Office365</span><span class="sxs-lookup"><span data-stu-id="61e06-182">Office365</span></span>
    <span data-ttu-id="61e06-183">Lietotājvārds</span><span class="sxs-lookup"><span data-stu-id="61e06-183">User name</span></span> |
    <span data-ttu-id="61e06-184">Parole vai Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="61e06-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="61e06-185">Parole</span><span class="sxs-lookup"><span data-stu-id="61e06-185">Password</span></span>
    <span data-ttu-id="61e06-186">Parole</span><span class="sxs-lookup"><span data-stu-id="61e06-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="61e06-187">Palaist veidni</span><span class="sxs-lookup"><span data-stu-id="61e06-187">Run the template</span></span>

1. <span data-ttu-id="61e06-188">Apturiet šo **Konta**, **Kontaktpersonas** un **Kreditora** dubultās rakstīšanas darbību, izmantojot programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61e06-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="61e06-189">Debitori V3 (konti)</span><span class="sxs-lookup"><span data-stu-id="61e06-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="61e06-190">Debitori V3 (kontaktpersonas)</span><span class="sxs-lookup"><span data-stu-id="61e06-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="61e06-191">CDS kontaktpersonas V2 (kontaktpersonas)</span><span class="sxs-lookup"><span data-stu-id="61e06-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="61e06-192">CDS kontaktpersonas V2 (kontaktpersonas)</span><span class="sxs-lookup"><span data-stu-id="61e06-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="61e06-193">Kreditors V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="61e06-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="61e06-194">Pārliecinieties, ka kartes no tabulas ir noņemtas no tabulas `msdy_dualwriteruntimeconfig` pakalpojumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="61e06-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="61e06-195">Instalējiet [Dubultās rakstīšanas puses un globālās adrešu grāmatas risinājumus](https://aka.ms/dual-write-gab) no AppSource.</span><span class="sxs-lookup"><span data-stu-id="61e06-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="61e06-196">Ja šajās tabulās ir dati, tad programmā Finance and Operations palaidiet tām **Sākuma sinhronizāciju**.</span><span class="sxs-lookup"><span data-stu-id="61e06-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="61e06-197">Uzrunas</span><span class="sxs-lookup"><span data-stu-id="61e06-197">Salutations</span></span>
    + <span data-ttu-id="61e06-198">Personas rakstura veidi</span><span class="sxs-lookup"><span data-stu-id="61e06-198">Personal character types</span></span>
    + <span data-ttu-id="61e06-199">Komplimentāra slēgšana</span><span class="sxs-lookup"><span data-stu-id="61e06-199">Complimentary closing</span></span>
    + <span data-ttu-id="61e06-200">Kontaktpersonu amati</span><span class="sxs-lookup"><span data-stu-id="61e06-200">Contact person titles</span></span>
    + <span data-ttu-id="61e06-201">Lēmumu pieņemšanas lomas</span><span class="sxs-lookup"><span data-stu-id="61e06-201">Decision making roles</span></span>
    + <span data-ttu-id="61e06-202">Lojalitātes programmu līmeņi</span><span class="sxs-lookup"><span data-stu-id="61e06-202">Loyalty levels</span></span>

5. <span data-ttu-id="61e06-203">Customer Engagement programmā deaktivizējiet tālāk norādītas darbības.</span><span class="sxs-lookup"><span data-stu-id="61e06-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="61e06-204">Konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-204">Account Update</span></span>
         + <span data-ttu-id="61e06-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="61e06-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="61e06-207">Kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-207">Contact Update</span></span>
         + <span data-ttu-id="61e06-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="61e06-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="61e06-210">msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-210">msdyn_party Update</span></span>
         + <span data-ttu-id="61e06-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="61e06-212">msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="61e06-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="61e06-214">Customer Engagement programmā deaktivizējiet tālāk norādītas darba plūsmas.</span><span class="sxs-lookup"><span data-stu-id="61e06-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="61e06-215">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="61e06-216">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="61e06-217">Izveidot kreditorus ar veidu persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="61e06-218">Izveidot kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="61e06-219">Kreditoru atjaunināšana kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="61e06-220">Kreditoru atjaunināšana kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="61e06-221">Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="61e06-222">Atjaunināt kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="61e06-223">Datu fabrikā palaidiet veidni, atlasot **Aktivizēt tūlīt**, kā parādīts šajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="61e06-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="61e06-224">Šis process var ilgt dažas stundas, balstoties uz datu apjomu.</span><span class="sxs-lookup"><span data-stu-id="61e06-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Trigera palaišana](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="61e06-226">Ja ir pielāgojumi **Kontam**, **Kontaktpersonai** un **Kreditoram** veidne jāmodificē.</span><span class="sxs-lookup"><span data-stu-id="61e06-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="61e06-227">Importēt jaunos **Puses** ierakstus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61e06-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="61e06-228">Lejupielādējiet `FONewParty.csv` failu no Azure BLOB krātuves.</span><span class="sxs-lookup"><span data-stu-id="61e06-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="61e06-229">Ceļš ir `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="61e06-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="61e06-230">Konvertējiet `FONewParty.csv` failu par Excel failu un importējiet Excel failu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61e06-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="61e06-231">Ja jums darbojas csv importēšana, varat tieši importēt csv failu.</span><span class="sxs-lookup"><span data-stu-id="61e06-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="61e06-232">Atkarībā no datu apjoma, importēšanas laiks var ilgt dažas stundas.</span><span class="sxs-lookup"><span data-stu-id="61e06-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="61e06-233">Papildinformāciju skatiet [Datu importēšanas un eksportēšanas darbu apskats](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="61e06-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Importēt Datavers puses ierakstus](media/data-factory-import-party.png)

9. <span data-ttu-id="61e06-235">Customer Engagement programmās aktivizējiet tālāk norādītas darbības:</span><span class="sxs-lookup"><span data-stu-id="61e06-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="61e06-236">Konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-236">Account Update</span></span>
         + <span data-ttu-id="61e06-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="61e06-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="61e06-239">Kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-239">Contact Update</span></span>
         + <span data-ttu-id="61e06-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="61e06-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="61e06-242">msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-242">msdyn_party Update</span></span>
         + <span data-ttu-id="61e06-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="61e06-244">msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="61e06-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="61e06-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="61e06-246">Customer Engagement programmās aktivizējiet šādas darbplūsmas, ja tās ir deaktivizētas iepriekšējās darbībās:</span><span class="sxs-lookup"><span data-stu-id="61e06-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="61e06-247">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="61e06-248">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="61e06-249">Izveidot kreditorus ar veidu persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="61e06-250">Izveidot kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="61e06-251">Kreditoru atjaunināšana kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="61e06-252">Kreditoru atjaunināšana kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="61e06-253">Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="61e06-254">Atjaunināt kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="61e06-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="61e06-255">Palaidiet ar **Pusi** saistītās kartes, kā norādīts sadaļā [Puse un globālā adrešu grāmata](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="61e06-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="61e06-256">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="61e06-256">Troubleshooting</span></span>

1. <span data-ttu-id="61e06-257">Procesā neizdodas vēlreiz palaist datu fabriku, sākot no neveiksmīgās darbības.</span><span class="sxs-lookup"><span data-stu-id="61e06-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="61e06-258">Dažus failus ģenerē datu fabrika, ko varat izmantot datu apstiprināšanas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="61e06-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="61e06-259">Datu fabrika darbojas, pamatojoties uz csv failiem, kas tiek atdalīti ar komatu.</span><span class="sxs-lookup"><span data-stu-id="61e06-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="61e06-260">Ja lauka vērtībai ir komats, tas var traucēt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="61e06-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="61e06-261">Ir jānoņem komati.</span><span class="sxs-lookup"><span data-stu-id="61e06-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="61e06-262">Cilne **Pārraudzība** sniedz informāciju par visam darbībam un apstrādātajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="61e06-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="61e06-263">Atlasiet noteiktu darbību, lai to atkļūdotu.</span><span class="sxs-lookup"><span data-stu-id="61e06-263">Select a specific step to debug it.</span></span>

    ![Cilne Pārraudzība](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="61e06-265">Uzziniet vairāk par veidni</span><span class="sxs-lookup"><span data-stu-id="61e06-265">Learn more about the template</span></span>

<span data-ttu-id="61e06-266">Komentārus veidnei varat atrast [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) failā.</span><span class="sxs-lookup"><span data-stu-id="61e06-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>