---
title: Jaunināšana uz pušu un globālās adrešu grāmatas modeli
description: Šajā tēmā ir aprakstīts, kā jaunināt dubultās rakstīšanas datus puses un globālās adrešu grāmatas modelī.
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 90ddbe704ab21d62752b581a813601e8986c2103
ms.sourcegitcommit: 180548e3c10459776cf199989d3753e0c1555912
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2021
ms.locfileid: "6112677"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="20c4d-103">Jaunināšana uz pušu un globālās adrešu grāmatas modeli</span><span class="sxs-lookup"><span data-stu-id="20c4d-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="20c4d-104">Šī [Microsoft Azure datu fabrikas veidne](https://aka.ms/dual-write-gab-adf) palīdz jaunināt esošo **Konta**, **Kontaktpersonas** un **Kreditora** tabulas datus dubultās rakstīšanas puses un globālās adrešu grāmatas modelī.</span><span class="sxs-lookup"><span data-stu-id="20c4d-104">The [Microsoft Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="20c4d-105">Veidne saskaņo datus no Finance and Operations programmām un Customer Engagement programmām.</span><span class="sxs-lookup"><span data-stu-id="20c4d-105">The template reconciles the data from both finance and operations apps and customer engagement applications.</span></span> <span data-ttu-id="20c4d-106">Procesa beigās **Puses** ierakstu **Puses** un **Kontaktpersonas** lauki tiks izveidoti un saistīti ar **Konta**, **Kontaktpersonas** un **Kreditora** ierakstiem Customer Engagement programmās.</span><span class="sxs-lookup"><span data-stu-id="20c4d-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="20c4d-107">Tiek ģenerēts .csv fails (`FONewParty.csv`), lai izveidotu jaunus **Puses** ierakstus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="20c4d-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the finance and operations app.</span></span> <span data-ttu-id="20c4d-108">Šajā tēmā ir sniegtas norādes par to kā lietot datu fabrikas veidnes un jaunināt datus.</span><span class="sxs-lookup"><span data-stu-id="20c4d-108">This topic provides instructions about how to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="20c4d-109">Ja jums nav nekādu pielāgojumu, varat izmantot veidni, kāda tā ir.</span><span class="sxs-lookup"><span data-stu-id="20c4d-109">If you don’t have any customizations, you can use the template as is.</span></span> <span data-ttu-id="20c4d-110">Ja ir pielāgojumi **Kontam**, **Kontaktpersonai** un **Kreditoram** veidne jāmodificē, izmantojot tālāk norādītās instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="20c4d-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!NOTE]
> <span data-ttu-id="20c4d-111">Veidne jaunina tikai **Puses** datus.</span><span class="sxs-lookup"><span data-stu-id="20c4d-111">The template only upgrades the **Party** data.</span></span> <span data-ttu-id="20c4d-112">Nākamajā laidienā tiks iekļautas pasta un elektroniskās adreses.</span><span class="sxs-lookup"><span data-stu-id="20c4d-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="20c4d-113">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="20c4d-113">Prerequisites</span></span>

<span data-ttu-id="20c4d-114">Ir nepieciešami šādi priekšnosacījumi, lai jauninātu uz pusi un globālās adrešu grāmatas modeli:</span><span class="sxs-lookup"><span data-stu-id="20c4d-114">The following prerequisites are required to upgrade to the party and global address book model:</span></span>

+ [<span data-ttu-id="20c4d-115">Azure abonements</span><span class="sxs-lookup"><span data-stu-id="20c4d-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="20c4d-116">Piekļuve veidnei</span><span class="sxs-lookup"><span data-stu-id="20c4d-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="20c4d-117">Jums jābūt jau esošam duālās rakstīšanas debitoram.</span><span class="sxs-lookup"><span data-stu-id="20c4d-117">You must be an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="20c4d-118">Sagatavoties jaunināšanai</span><span class="sxs-lookup"><span data-stu-id="20c4d-118">Prepare for the upgrade</span></span>
<span data-ttu-id="20c4d-119">Lai sagatavotos jaunināšanai, ir nepieciešamas šādas aktivitātes:</span><span class="sxs-lookup"><span data-stu-id="20c4d-119">The following activities are needed to prepare for the upgrade:</span></span>

+ <span data-ttu-id="20c4d-120">**Pilnībā sinhronizēts**: abas vides ir pilnībā sinhronizētas **Kontam (Debitoram)**, **Kontaktpersonai** un **Kreditoram**.</span><span class="sxs-lookup"><span data-stu-id="20c4d-120">**Fully synced**: Both environments are in a fully synced state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="20c4d-121">**Integrācijas atslēgas**: tabulas **Konts (Debitors)**, **Kontaktpersona** un **Kreditors** Customer Engagement programmās izmanto integrācijas atslēgas, kas nosūtītas nestandarti.</span><span class="sxs-lookup"><span data-stu-id="20c4d-121">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="20c4d-122">Pielāgojot integrācijas atslēgas, veidne ir jāpielāgo.</span><span class="sxs-lookup"><span data-stu-id="20c4d-122">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="20c4d-123">**Puses numurs**: visiem **Konta (Debitora)**, **Kontaktpersonas** un **Kreditora** ierakstiem, kas tiks jaunināti, ir **Puses** numurs.</span><span class="sxs-lookup"><span data-stu-id="20c4d-123">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="20c4d-124">Ieraksti bez **Puses** numura tiks ignorēti.</span><span class="sxs-lookup"><span data-stu-id="20c4d-124">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="20c4d-125">Ja vēlaties jaunināt šos ierakstus, pirms jaunināšanas procesa sākšanas pievienojiet tiem **Puses** numuru.</span><span class="sxs-lookup"><span data-stu-id="20c4d-125">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="20c4d-126">**Sistēmas noplūde**: jaunināšanas laikā jums būs jāizmanto gan Finance and Operations, gan Customer Engagement vides bezsaistē.</span><span class="sxs-lookup"><span data-stu-id="20c4d-126">**System outage**: During the upgrade process, you will have to take both the finance and operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="20c4d-127">**Momentuzņēmums**: izveidot momentuzņēmumus gan no Finance and Operations, gan no Customer Engagement programmām.</span><span class="sxs-lookup"><span data-stu-id="20c4d-127">**Snapshot**: Take snapshots of both the finance and operations apps and customer engagement apps.</span></span> <span data-ttu-id="20c4d-128">Izmantojiet momentuzņēmumus, lai atjaunotu iepriekšējo stāvokli, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="20c4d-128">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="20c4d-129">Izvietojums</span><span class="sxs-lookup"><span data-stu-id="20c4d-129">Deployment</span></span>

1. <span data-ttu-id="20c4d-130">Lejupielādējiet veidni no [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="20c4d-130">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="20c4d-131">Pierakstīšanās programmā [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="20c4d-131">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="20c4d-132">Izveidojiet [resursu grupu](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="20c4d-132">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="20c4d-133">Izveidojiet [glabāšanas kontu](/azure/storage/common/storage-account-create?tabs=azure-portal) izveidoto resursu grupā.</span><span class="sxs-lookup"><span data-stu-id="20c4d-133">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="20c4d-134">Izveidojiet [datu fabriku](/azure/data-factory/quickstart-create-data-factory-portal) virs izveidotās resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="20c4d-134">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="20c4d-135">Atveriet datu fabriku un atlasiet elementu **Autors & Pārraudzīt**.</span><span class="sxs-lookup"><span data-stu-id="20c4d-135">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="20c4d-136">Cilnē **Pārvaldīt** atlasiet **ARM veidne**.</span><span class="sxs-lookup"><span data-stu-id="20c4d-136">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="20c4d-137">Izvēlieties **Importēt ARM veidni**, lai importētu **Puses** veidni.</span><span class="sxs-lookup"><span data-stu-id="20c4d-137">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="20c4d-138">Importējiet veidni datu fabrikā.</span><span class="sxs-lookup"><span data-stu-id="20c4d-138">Import the template into the data factory.</span></span> <span data-ttu-id="20c4d-139">Ievadiet tālāk norādītās vērtības **Projekta detalizēta informācija** un **Instances detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="20c4d-139">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="20c4d-140">Lauks</span><span class="sxs-lookup"><span data-stu-id="20c4d-140">Field</span></span> | <span data-ttu-id="20c4d-141">Vērtība</span><span class="sxs-lookup"><span data-stu-id="20c4d-141">Value</span></span>
    ---|---
    <span data-ttu-id="20c4d-142">Abonements</span><span class="sxs-lookup"><span data-stu-id="20c4d-142">Subscription</span></span> | <span data-ttu-id="20c4d-143">Azure abonements</span><span class="sxs-lookup"><span data-stu-id="20c4d-143">Azure subscription</span></span>
    <span data-ttu-id="20c4d-144">Resursa grupa</span><span class="sxs-lookup"><span data-stu-id="20c4d-144">Resource group</span></span> | <span data-ttu-id="20c4d-145">Nodrošiniet to pašu resursu, kurā ir izveidots glabāšanas konts.</span><span class="sxs-lookup"><span data-stu-id="20c4d-145">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="20c4d-146">Reģions</span><span class="sxs-lookup"><span data-stu-id="20c4d-146">Region</span></span> | <span data-ttu-id="20c4d-147">Norādīt reģionu.</span><span class="sxs-lookup"><span data-stu-id="20c4d-147">Specify region.</span></span>
    <span data-ttu-id="20c4d-148">Fabrikas nosaukums</span><span class="sxs-lookup"><span data-stu-id="20c4d-148">Factory Name</span></span> | <span data-ttu-id="20c4d-149">Norādiet fabrikas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="20c4d-149">Specify factory name.</span></span>
    <span data-ttu-id="20c4d-150">FO saistīta Pakalpojums_pakalpojums galvenā atslēga</span><span class="sxs-lookup"><span data-stu-id="20c4d-150">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="20c4d-151">Norādiet pieteikuma atslēgu.</span><span class="sxs-lookup"><span data-stu-id="20c4d-151">Specify the application's key.</span></span>
    <span data-ttu-id="20c4d-152">Azure Blob krātuves_savienojuma virknes</span><span class="sxs-lookup"><span data-stu-id="20c4d-152">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="20c4d-153">Azure Blob krātuves savienojuma virkne.</span><span class="sxs-lookup"><span data-stu-id="20c4d-153">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="20c4d-154">Dynamics CRM saistīta Pakalpojuma_parole</span><span class="sxs-lookup"><span data-stu-id="20c4d-154">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="20c4d-155">Parole lietotāja kontam, kuru norādījāt kā lietotājvārdu.</span><span class="sxs-lookup"><span data-stu-id="20c4d-155">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="20c4d-156">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_url</span><span class="sxs-lookup"><span data-stu-id="20c4d-156">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="20c4d-157">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_nomnieks</span><span class="sxs-lookup"><span data-stu-id="20c4d-157">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="20c4d-158">Norādiet informāciju par nomnieku (domēna vārdu vai nomnieka ID), kurā atrodas jūsu pieteikums.</span><span class="sxs-lookup"><span data-stu-id="20c4d-158">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="20c4d-159">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_aad Resursa ID</span><span class="sxs-lookup"><span data-stu-id="20c4d-159">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="20c4d-160">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_pakalpojums Galvenā ID</span><span class="sxs-lookup"><span data-stu-id="20c4d-160">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="20c4d-161">Norādiet pieteikuma debitora ID.</span><span class="sxs-lookup"><span data-stu-id="20c4d-161">Specify the application's client ID.</span></span>
    <span data-ttu-id="20c4d-162">Dynamics CRM saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_lietotājvārds</span><span class="sxs-lookup"><span data-stu-id="20c4d-162">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="20c4d-163">Lietotājvārds, ar kuru jāizveido savienojums ar Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="20c4d-163">The username to connect to Dynamics 365.</span></span>

    <span data-ttu-id="20c4d-164">Papildinformāciju skatiet tālāk norādītās tēmas.</span><span class="sxs-lookup"><span data-stu-id="20c4d-164">For additional information, refer to the following topics:</span></span> 
    
    - [<span data-ttu-id="20c4d-165">Manuāli veicināt Resource Manager veidni katrai videi</span><span class="sxs-lookup"><span data-stu-id="20c4d-165">Manually promote a Resource Manager template for each environment</span></span>](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [<span data-ttu-id="20c4d-166">Saistītie pakalpojuma rekvizīti</span><span class="sxs-lookup"><span data-stu-id="20c4d-166">Linked service properties</span></span>](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [<span data-ttu-id="20c4d-167">Kopēt datus, izmantojot Azure datu ražotni</span><span class="sxs-lookup"><span data-stu-id="20c4d-167">Copy data using Azure Data Factory</span></span>](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. <span data-ttu-id="20c4d-168">Pēc izvietošanas validējiet datu fabrikas datu kopas, datu plūsmu un saistīto pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="20c4d-168">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datu kopas, datu plūsma un saistītais pakalpojums](media/data-factory-validate.png)

11. <span data-ttu-id="20c4d-170">Dodieties uz **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="20c4d-170">Navigate to **Manage**.</span></span> <span data-ttu-id="20c4d-171">Sadaļā **Savienojumi** atlasiet **Saistītais pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="20c4d-171">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="20c4d-172">Atlasiet **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="20c4d-172">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="20c4d-173">Formā **Rediģēt saistīto pakalpojumu (Dynamics CRM)** ievadiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="20c4d-173">In the **Edit linked service (Dynamics CRM)** form, enter the following values.</span></span>

    <span data-ttu-id="20c4d-174">Lauks</span><span class="sxs-lookup"><span data-stu-id="20c4d-174">Field</span></span> | <span data-ttu-id="20c4d-175">Vērtība</span><span class="sxs-lookup"><span data-stu-id="20c4d-175">Value</span></span>
    ---|---
    <span data-ttu-id="20c4d-176">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="20c4d-176">Name</span></span> | <span data-ttu-id="20c4d-177">Atlasiet DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="20c4d-177">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="20c4d-178">Apraksts</span><span class="sxs-lookup"><span data-stu-id="20c4d-178">Description</span></span> | <span data-ttu-id="20c4d-179">Saistītie pakalpojumi, kas ir jāsavieno ar CRM instanci, lai ienestu elementu datus</span><span class="sxs-lookup"><span data-stu-id="20c4d-179">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="20c4d-180">Izveidot savienojumu, izmantojot integrācijas izpildlaiku</span><span class="sxs-lookup"><span data-stu-id="20c4d-180">Connect via integration runtime</span></span> | <span data-ttu-id="20c4d-181">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="20c4d-181">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="20c4d-182">Izvietošanas veids</span><span class="sxs-lookup"><span data-stu-id="20c4d-182">Deployment type</span></span> | <span data-ttu-id="20c4d-183">Tiešsaiste</span><span class="sxs-lookup"><span data-stu-id="20c4d-183">Online</span></span>
    <span data-ttu-id="20c4d-184">Pakalpojuma Uri</span><span class="sxs-lookup"><span data-stu-id="20c4d-184">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="20c4d-185">Autentifikācijas veids</span><span class="sxs-lookup"><span data-stu-id="20c4d-185">Authentication type</span></span> | <span data-ttu-id="20c4d-186">Office365</span><span class="sxs-lookup"><span data-stu-id="20c4d-186">Office365</span></span>
    <span data-ttu-id="20c4d-187">Lietotājvārds</span><span class="sxs-lookup"><span data-stu-id="20c4d-187">User name</span></span> |
    <span data-ttu-id="20c4d-188">Parole vai Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="20c4d-188">Password or Azure Key Vault</span></span> | <span data-ttu-id="20c4d-189">Parole</span><span class="sxs-lookup"><span data-stu-id="20c4d-189">Password</span></span>
    <span data-ttu-id="20c4d-190">Parole</span><span class="sxs-lookup"><span data-stu-id="20c4d-190">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="20c4d-191">Palaist veidni</span><span class="sxs-lookup"><span data-stu-id="20c4d-191">Run the template</span></span>

1. <span data-ttu-id="20c4d-192">Apturiet šo **Konta**, **Kontaktpersonas** un **Kreditora** dubultās rakstīšanas kartes, izmantojot programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="20c4d-192">Stop the following **Account**, **Contact**, and **Vendor** dual-write maps using the Finance and Operations app.</span></span>

    + <span data-ttu-id="20c4d-193">Debitori V3 (konti)</span><span class="sxs-lookup"><span data-stu-id="20c4d-193">Customers V3(accounts)</span></span>
    + <span data-ttu-id="20c4d-194">Debitori V3 (kontaktpersonas)</span><span class="sxs-lookup"><span data-stu-id="20c4d-194">Customers V3(contacts)</span></span>
    + <span data-ttu-id="20c4d-195">CDS kontaktpersonas V2 (kontaktpersonas)</span><span class="sxs-lookup"><span data-stu-id="20c4d-195">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="20c4d-196">CDS kontaktpersonas V2 (kontaktpersonas)</span><span class="sxs-lookup"><span data-stu-id="20c4d-196">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="20c4d-197">Kreditors V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="20c4d-197">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="20c4d-198">Pārliecinieties, ka kartes no tabulas ir noņemtas no tabulas `msdy_dualwriteruntimeconfig` pakalpojumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="20c4d-198">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="20c4d-199">Instalējiet [Dubultās rakstīšanas puses un globālās adrešu grāmatas risinājumus](https://aka.ms/dual-write-gab) no AppSource.</span><span class="sxs-lookup"><span data-stu-id="20c4d-199">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="20c4d-200">Ja šajās tabulās ir dati, tad programmā Finance and Operations palaidiet tām **Sākuma sinhronizāciju**.</span><span class="sxs-lookup"><span data-stu-id="20c4d-200">In the finance and operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="20c4d-201">Uzrunas</span><span class="sxs-lookup"><span data-stu-id="20c4d-201">Salutations</span></span>
    + <span data-ttu-id="20c4d-202">Personas rakstura veidi</span><span class="sxs-lookup"><span data-stu-id="20c4d-202">Personal character types</span></span>
    + <span data-ttu-id="20c4d-203">Komplimentāra slēgšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-203">Complimentary closing</span></span>
    + <span data-ttu-id="20c4d-204">Kontaktpersonu amati</span><span class="sxs-lookup"><span data-stu-id="20c4d-204">Contact person titles</span></span>
    + <span data-ttu-id="20c4d-205">Lēmumu pieņemšanas lomas</span><span class="sxs-lookup"><span data-stu-id="20c4d-205">Decision making roles</span></span>
    + <span data-ttu-id="20c4d-206">Lojalitātes programmu līmeņi</span><span class="sxs-lookup"><span data-stu-id="20c4d-206">Loyalty levels</span></span>

5. <span data-ttu-id="20c4d-207">Customer Engagement programmā deaktivizējiet tālāk norādītas darbības.</span><span class="sxs-lookup"><span data-stu-id="20c4d-207">In the customer engagement app, disable the following plug-in steps.</span></span>

    + <span data-ttu-id="20c4d-208">Konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-208">Account Update</span></span>
         + <span data-ttu-id="20c4d-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-209">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="20c4d-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-210">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="20c4d-211">Kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-211">Contact Update</span></span>
         + <span data-ttu-id="20c4d-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-212">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="20c4d-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-213">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="20c4d-214">msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-214">msdyn_party Update</span></span>
         + <span data-ttu-id="20c4d-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-215">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="20c4d-216">msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-216">msdyn_vendor Update</span></span>
         + <span data-ttu-id="20c4d-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-217">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="20c4d-218">Customer Engagement programmā deaktivizējiet tālāk norādītas darba plūsmas.</span><span class="sxs-lookup"><span data-stu-id="20c4d-218">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="20c4d-219">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-219">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20c4d-220">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-220">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20c4d-221">Izveidot kreditorus ar veidu persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-221">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="20c4d-222">Izveidot kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-222">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="20c4d-223">Kreditoru atjaunināšana kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-223">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20c4d-224">Kreditoru atjaunināšana kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-224">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="20c4d-225">Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-225">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="20c4d-226">Atjaunināt kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-226">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="20c4d-227">Datu fabrikā palaidiet veidni, atlasot **Aktivizēt tūlīt**, kā parādīts šajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="20c4d-227">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="20c4d-228">Šis process var ilgt dažas stundas, balstoties uz datu apjomu.</span><span class="sxs-lookup"><span data-stu-id="20c4d-228">This process might take a few hours to complete based on the data volume.</span></span>

    ![Trigera palaišana](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="20c4d-230">Ja ir pielāgojumi **Kontam**, **Kontaktpersonai** un **Kreditoram**, veidne jāmodificē.</span><span class="sxs-lookup"><span data-stu-id="20c4d-230">If you have customizations for **Account**, **Contact**, and **Vendor**, then you need to modify the template.</span></span>

8. <span data-ttu-id="20c4d-231">Importēt jaunos **Puses** ierakstus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="20c4d-231">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="20c4d-232">Lejupielādējiet `FONewParty.csv` failu no Azure BLOB krātuves.</span><span class="sxs-lookup"><span data-stu-id="20c4d-232">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="20c4d-233">Ceļš ir `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="20c4d-233">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="20c4d-234">Konvertējiet `FONewParty.csv` failu par Excel failu un importējiet Excel failu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="20c4d-234">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the finance and operations app.</span></span> <span data-ttu-id="20c4d-235">Ja jums darbojas csv importēšana, varat tieši importēt csv failu.</span><span class="sxs-lookup"><span data-stu-id="20c4d-235">If the csv import works for you, you can import the csv file directly.</span></span> <span data-ttu-id="20c4d-236">Atkarībā no datu apjoma, importēšanas laiks var ilgt dažas stundas.</span><span class="sxs-lookup"><span data-stu-id="20c4d-236">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="20c4d-237">Papildinformāciju skatiet [Datu importēšanas un eksportēšanas darbu apskats](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="20c4d-237">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Importēt Datavers puses ierakstus](media/data-factory-import-party.png)

9. <span data-ttu-id="20c4d-239">Customer Engagement programmās aktivizējiet tālāk norādītas darbības:</span><span class="sxs-lookup"><span data-stu-id="20c4d-239">In the customer engagement apps, enable the following plug-in steps:</span></span>

    + <span data-ttu-id="20c4d-240">Konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-240">Account Update</span></span>
         + <span data-ttu-id="20c4d-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-241">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="20c4d-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-242">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="20c4d-243">Kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-243">Contact Update</span></span>
         + <span data-ttu-id="20c4d-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-244">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="20c4d-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-245">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="20c4d-246">msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-246">msdyn_party Update</span></span>
         + <span data-ttu-id="20c4d-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-247">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="20c4d-248">msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-248">msdyn_vendor Update</span></span>
         + <span data-ttu-id="20c4d-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="20c4d-249">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="20c4d-250">Customer Engagement programmās aktivizējiet šādas darbplūsmas, ja tās ir deaktivizētas iepriekšējās darbībās:</span><span class="sxs-lookup"><span data-stu-id="20c4d-250">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="20c4d-251">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-251">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20c4d-252">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-252">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20c4d-253">Izveidot kreditorus ar veidu persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-253">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="20c4d-254">Izveidot kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-254">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="20c4d-255">Kreditoru atjaunināšana kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-255">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="20c4d-256">Kreditoru atjaunināšana kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-256">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="20c4d-257">Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-257">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="20c4d-258">Atjaunināt kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="20c4d-258">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="20c4d-259">Palaidiet ar **Pusi** saistītās kartes, kā norādīts sadaļā [Puse un globālā adrešu grāmata](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="20c4d-259">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="20c4d-260">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="20c4d-260">Troubleshooting</span></span>

1. <span data-ttu-id="20c4d-261">Ja process neizdodas, vēlreiz palaidiet datu fabriku, sākot no neveiksmīgās darbības.</span><span class="sxs-lookup"><span data-stu-id="20c4d-261">If the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="20c4d-262">Dažus failus ģenerē datu fabrika, ko varat izmantot datu apstiprināšanas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="20c4d-262">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="20c4d-263">Datu fabrika darbojas, pamatojoties uz csv failiem, kas tiek atdalīti ar komatu.</span><span class="sxs-lookup"><span data-stu-id="20c4d-263">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="20c4d-264">Ja lauka vērtībai ir komats, tas var traucēt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="20c4d-264">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="20c4d-265">Ir jānoņem komati.</span><span class="sxs-lookup"><span data-stu-id="20c4d-265">You need to remove the commas.</span></span>
4. <span data-ttu-id="20c4d-266">Cilne **Pārraudzība** sniedz informāciju par visam darbībam un apstrādātajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="20c4d-266">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="20c4d-267">Atlasiet noteiktu darbību, lai to atkļūdotu.</span><span class="sxs-lookup"><span data-stu-id="20c4d-267">Select a specific step to debug it.</span></span>

    ![Cilne Pārraudzība](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="20c4d-269">Uzziniet vairāk par veidni</span><span class="sxs-lookup"><span data-stu-id="20c4d-269">Learn more about the template</span></span>

<span data-ttu-id="20c4d-270">Jūs varat atrast papildinformāciju par veidne sadaļā [Komentāri par Azure datu fabrikas veidnes lasīšanu](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span><span class="sxs-lookup"><span data-stu-id="20c4d-270">You can find additional information about the template in [Comments for Azure Data Factory template readme](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md).</span></span>
