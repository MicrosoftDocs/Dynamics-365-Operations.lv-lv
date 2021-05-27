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
ms.openlocfilehash: 95472a00d34ba939ac89b4e2484f34d50bee3088
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018316"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a><span data-ttu-id="5008e-103">Jaunināšana uz pušu un globālās adrešu grāmatas modeli</span><span class="sxs-lookup"><span data-stu-id="5008e-103">Upgrade to the party and global address book model</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5008e-104">Šī [Azure datu fabrikas veidne](https://aka.ms/dual-write-gab-adf) palīdz jaunināt esošo **Konta**, **Kontaktpersonas** un **Kreditora** tabulas datus dubultās rakstīšanas puses un globālās adrešu grāmatas modelī.</span><span class="sxs-lookup"><span data-stu-id="5008e-104">The [Azure Data Factory template](https://aka.ms/dual-write-gab-adf) helps you upgrade existing **Account**, **Contact**, and **Vendor** table data in dual-write to the party and global address book model.</span></span> <span data-ttu-id="5008e-105">Veidne saskaņo datus no Finance and Operations programmām un Customer Engagement programmām.</span><span class="sxs-lookup"><span data-stu-id="5008e-105">The template reconciles the data from both Finance and Operations apps and customer engagement applications.</span></span> <span data-ttu-id="5008e-106">Procesa beigās **Puses** ierakstu **Puses** un **Kontaktpersonas** lauki tiks izveidoti un saistīti ar **Konta**, **Kontaktpersonas** un **Kreditora** ierakstiem Customer Engagement programmās.</span><span class="sxs-lookup"><span data-stu-id="5008e-106">At the end of the process, **Party** and **Contact** fields for **Party** records will be created and associated with **Account**, **Contact**, and **Vendor** records in customer engagement applications.</span></span> <span data-ttu-id="5008e-107">Tiek ģenerēts .csv fails (`FONewParty.csv`), lai izveidotu jaunus **Puses** ierakstus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5008e-107">A .csv file (`FONewParty.csv`) is generated to create new **Party** records inside the Finance and Operations app.</span></span> <span data-ttu-id="5008e-108">Šajā tēmā ir sniegtas norādes par datu fabrikas veidnes lietošanu un datu jaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="5008e-108">This topic provides the instructions to use the Data Factory template and upgrade your data.</span></span>

<span data-ttu-id="5008e-109">Ja jums nav nekādu pielāgojumu, varat izmantot veidni, kāda tā ir.</span><span class="sxs-lookup"><span data-stu-id="5008e-109">If you don’t have any customizations, you can use the template as-is.</span></span> <span data-ttu-id="5008e-110">Ja ir pielāgojumi **Kontam**, **Kontaktpersonai** un **Kreditoram** veidne jāmodificē, izmantojot tālāk norādītās instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="5008e-110">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template using the following instructions.</span></span>

> [!Note]
> <span data-ttu-id="5008e-111">Veidne palīdz jaunināt tikai **Puses** datus.</span><span class="sxs-lookup"><span data-stu-id="5008e-111">The template helps to upgrade only the **Party** data.</span></span> <span data-ttu-id="5008e-112">Nākamajā laidienā tiks iekļautas pasta un elektroniskās adreses.</span><span class="sxs-lookup"><span data-stu-id="5008e-112">In a future release, postal and electronic addresses will be included.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5008e-113">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="5008e-113">Prerequisites</span></span>

<span data-ttu-id="5008e-114">Ir nepieciešami šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="5008e-114">These prerequisites are required:</span></span>

+ [<span data-ttu-id="5008e-115">Azure abonements</span><span class="sxs-lookup"><span data-stu-id="5008e-115">Azure subscription</span></span>](https://portal.azure.com/)
+ [<span data-ttu-id="5008e-116">Piekļuve veidnei</span><span class="sxs-lookup"><span data-stu-id="5008e-116">Access to the template</span></span>](https://aka.ms/dual-write-gab-adf)
+ <span data-ttu-id="5008e-117">Jūs esat jau esošs duālās rakstīšanas debitors.</span><span class="sxs-lookup"><span data-stu-id="5008e-117">You are an existing dual-write customer.</span></span>

## <a name="prepare-for-the-upgrade"></a><span data-ttu-id="5008e-118">Sagatavoties jaunināšanai</span><span class="sxs-lookup"><span data-stu-id="5008e-118">Prepare for the upgrade</span></span>

+ <span data-ttu-id="5008e-119">**Pilnībā sinhronizēts**: abas vides ir pilnībā sinhronizētas **Kontam (Debitoram)**, **Kontaktpersonai** un **Kreditoram**.</span><span class="sxs-lookup"><span data-stu-id="5008e-119">**Fully synched**: Both environments are fully synched state for **Account (Customer)**, **Contact**, and **Vendor**.</span></span>
+ <span data-ttu-id="5008e-120">**Integrācijas atslēgas**: tabulas **Konts (Debitors)**, **Kontaktpersona** un **Kreditors** Customer Engagement programmās izmanto integrācijas atslēgas, kas nosūtītas nestandarti.</span><span class="sxs-lookup"><span data-stu-id="5008e-120">**Integration keys**: **Account (Customer)**, **Contact**, and **Vendor** tables in customer engagement apps are using the integration keys that shipped out-of-the-box.</span></span> <span data-ttu-id="5008e-121">Pielāgojot integrācijas atslēgas, veidne ir jāpielāgo.</span><span class="sxs-lookup"><span data-stu-id="5008e-121">If you customized the integration keys, you must customize the template.</span></span>
+ <span data-ttu-id="5008e-122">**Puses numurs**: visiem **Konta (Debitora)**, **Kontaktpersonas** un **Kreditora** ierakstiem, kas tiks jaunināti, ir **Puses** numurs.</span><span class="sxs-lookup"><span data-stu-id="5008e-122">**Party number**: All **Account (Customer)**, **Contact**, and **Vendor** records that will be upgraded have a **Party** number.</span></span> <span data-ttu-id="5008e-123">Ieraksti bez **Puses** numura tiks ignorēti.</span><span class="sxs-lookup"><span data-stu-id="5008e-123">Records without a **Party** number will be ignored.</span></span> <span data-ttu-id="5008e-124">Ja vēlaties jaunināt šos ierakstus, pirms jaunināšanas procesa sākšanas pievienojiet tiem **Puses** numuru.</span><span class="sxs-lookup"><span data-stu-id="5008e-124">If you want to upgrade those records, add a **Party** number to them before you start the upgrade process.</span></span>
+ <span data-ttu-id="5008e-125">**Sistēmas noplūde**: jaunināšanas laikā jums būs jāizmanto gan Finance and Operations, gan Customer Engagement vides bezsaistē.</span><span class="sxs-lookup"><span data-stu-id="5008e-125">**System outage**: During the upgrade process, you will have to take both the Finance and Operations and customer engagement environments offline.</span></span>
+ <span data-ttu-id="5008e-126">**Momentuzņēmums**: izveidot momentuzņēmumus gan no Finance and Operations, gan no Customer Engagement programmām.</span><span class="sxs-lookup"><span data-stu-id="5008e-126">**Snapshot**: Take snapshots of both the Finance and Operations and customer engagement apps.</span></span> <span data-ttu-id="5008e-127">Izmantojiet momentuzņēmumus, lai atjaunotu iepriekšējo stāvokli, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="5008e-127">Use the snapshots to restore the previous state if you need to.</span></span>

## <a name="deployment"></a><span data-ttu-id="5008e-128">Izvietojums</span><span class="sxs-lookup"><span data-stu-id="5008e-128">Deployment</span></span>

1. <span data-ttu-id="5008e-129">Lejupielādējiet veidni no [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span><span class="sxs-lookup"><span data-stu-id="5008e-129">Download the template from [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf).</span></span>

2. <span data-ttu-id="5008e-130">Pierakstīšanās programmā [Microsoft Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="5008e-130">Sign in to [Microsoft Azure](https://portal.azure.com/).</span></span>

3. <span data-ttu-id="5008e-131">Izveidojiet [resursu grupu](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span><span class="sxs-lookup"><span data-stu-id="5008e-131">Create a [resource group](/azure/azure-resource-manager/management/manage-resource-groups-portal).</span></span>

4. <span data-ttu-id="5008e-132">Izveidojiet [glabāšanas kontu](/azure/storage/common/storage-account-create?tabs=azure-portal) izveidoto resursu grupā.</span><span class="sxs-lookup"><span data-stu-id="5008e-132">Create a [storage account](/azure/storage/common/storage-account-create?tabs=azure-portal) in the resource group that you created.</span></span>

5. <span data-ttu-id="5008e-133">Izveidojiet [datu fabriku](/azure/data-factory/quickstart-create-data-factory-portal) virs izveidotās resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="5008e-133">Create a [data factory](/azure/data-factory/quickstart-create-data-factory-portal) in above resource group that you created.</span></span>

6. <span data-ttu-id="5008e-134">Atveriet datu fabriku un atlasiet elementu **Autors & Pārraudzīt**.</span><span class="sxs-lookup"><span data-stu-id="5008e-134">Open the data factory and select the **Author & Monitor** tile.</span></span>

7. <span data-ttu-id="5008e-135">Cilnē **Pārvaldīt** atlasiet **ARM veidne**.</span><span class="sxs-lookup"><span data-stu-id="5008e-135">On the **Manage** tab, select **ARM template**.</span></span>

8. <span data-ttu-id="5008e-136">Izvēlieties **Importēt ARM veidni**, lai importētu **Puses** veidni.</span><span class="sxs-lookup"><span data-stu-id="5008e-136">Select the **Import ARM template** to import the **Party** template.</span></span>

9. <span data-ttu-id="5008e-137">Importējiet veidni datu fabrikā.</span><span class="sxs-lookup"><span data-stu-id="5008e-137">Import the template into the data factory.</span></span> <span data-ttu-id="5008e-138">Ievadiet tālāk norādītās vērtības **Projekta detalizēta informācija** un **Instances detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="5008e-138">Enter the following values for **Project details** and **Instance details**.</span></span>

    <span data-ttu-id="5008e-139">Lauks</span><span class="sxs-lookup"><span data-stu-id="5008e-139">Field</span></span> | <span data-ttu-id="5008e-140">Vērtība</span><span class="sxs-lookup"><span data-stu-id="5008e-140">Value</span></span>
    ---|---
    <span data-ttu-id="5008e-141">Abonements</span><span class="sxs-lookup"><span data-stu-id="5008e-141">Subscription</span></span> | <span data-ttu-id="5008e-142">Azure abonements</span><span class="sxs-lookup"><span data-stu-id="5008e-142">Azure subscription</span></span>
    <span data-ttu-id="5008e-143">Resursa grupa</span><span class="sxs-lookup"><span data-stu-id="5008e-143">Resource group</span></span> | <span data-ttu-id="5008e-144">Nodrošiniet to pašu resursu, kurā ir izveidots glabāšanas konts.</span><span class="sxs-lookup"><span data-stu-id="5008e-144">Provide same resource under which storage account is created.</span></span>
    <span data-ttu-id="5008e-145">Reģions</span><span class="sxs-lookup"><span data-stu-id="5008e-145">Region</span></span> | <span data-ttu-id="5008e-146">Norādīt reģionu.</span><span class="sxs-lookup"><span data-stu-id="5008e-146">Specify region.</span></span>
    <span data-ttu-id="5008e-147">Fabrikas nosaukums</span><span class="sxs-lookup"><span data-stu-id="5008e-147">Factory Name</span></span> | <span data-ttu-id="5008e-148">Norādiet fabrikas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="5008e-148">Specify factory name.</span></span>
    <span data-ttu-id="5008e-149">FO saistīta Pakalpojums_pakalpojums galvenā atslēga</span><span class="sxs-lookup"><span data-stu-id="5008e-149">FO Linked Service_service Principal Key</span></span> | <span data-ttu-id="5008e-150">Norādiet pieteikuma atslēgu.</span><span class="sxs-lookup"><span data-stu-id="5008e-150">Specify the application's key.</span></span>
    <span data-ttu-id="5008e-151">Azure Blob krātuves_savienojuma virknes</span><span class="sxs-lookup"><span data-stu-id="5008e-151">Azure Blob Storage_connection String</span></span> | <span data-ttu-id="5008e-152">Azure Blob krātuves savienojuma virkne.</span><span class="sxs-lookup"><span data-stu-id="5008e-152">Azure Blob storage connection string.</span></span>
    <span data-ttu-id="5008e-153">Dynamics CRM saistīta Pakalpojuma_parole</span><span class="sxs-lookup"><span data-stu-id="5008e-153">Dynamics Crm Linked Service_password</span></span> | <span data-ttu-id="5008e-154">Parole lietotāja kontam, kuru norādījāt kā lietotājvārdu.</span><span class="sxs-lookup"><span data-stu-id="5008e-154">The password for the user account you specified as the username.</span></span>
    <span data-ttu-id="5008e-155">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_url</span><span class="sxs-lookup"><span data-stu-id="5008e-155">FO Linked Service_properties_type Properties_url</span></span>  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    <span data-ttu-id="5008e-156">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_nomnieks</span><span class="sxs-lookup"><span data-stu-id="5008e-156">FO Linked Service_properties_type Properties_tenant</span></span> | <span data-ttu-id="5008e-157">Norādiet informāciju par nomnieku (domēna vārdu vai nomnieka ID), kurā atrodas jūsu pieteikums.</span><span class="sxs-lookup"><span data-stu-id="5008e-157">Specify the tenant information (domain name or tenant ID) under which your application resides.</span></span>
    <span data-ttu-id="5008e-158">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_aad Resursa ID</span><span class="sxs-lookup"><span data-stu-id="5008e-158">FO Linked Service_properties_type Properties_aad Resource Id</span></span> | `https://sampledynamics.sandboxoperationsdynamics.com`
    <span data-ttu-id="5008e-159">FO saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_pakalpojums Galvenā ID</span><span class="sxs-lookup"><span data-stu-id="5008e-159">FO Linked Service_properties_type Properties_service Principal Id</span></span> | <span data-ttu-id="5008e-160">Norādiet pieteikuma debitora ID.</span><span class="sxs-lookup"><span data-stu-id="5008e-160">Specify the application's client ID.</span></span>
    <span data-ttu-id="5008e-161">Dynamics CRM saistīts Pakalpojuma_rekvizītu_veids Rekvizītu_lietotājvārds</span><span class="sxs-lookup"><span data-stu-id="5008e-161">Dynamics Crm Linked Service_properties_type Properties_username</span></span> | <span data-ttu-id="5008e-162">Lietotājvārds, ar kuru jāizveido savienojums ar Dynamics.</span><span class="sxs-lookup"><span data-stu-id="5008e-162">The username to connect to Dynamics.</span></span>

    <span data-ttu-id="5008e-163">Papildinformāciju skatiet šeit: [Manuāli veicināt Resource Manager veidni katrai videi](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Saistīto pakalpojumu rekvizīti](/azure/data-factory/connector-dynamics-ax#linked-service-properties) un [Kopēt datus, izmantojot Azure datu fabriku](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span><span class="sxs-lookup"><span data-stu-id="5008e-163">For more information, see [Manually promote a Resource Manager template for each environment](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment), [Linked service properties](/azure/data-factory/connector-dynamics-ax#linked-service-properties), and [Copy data using Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)</span></span>

10. <span data-ttu-id="5008e-164">Pēc izvietošanas validējiet datu fabrikas datu kopas, datu plūsmu un saistīto pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="5008e-164">After deployment, validate the datasets, data flow, and linked service of the data factory.</span></span>

   ![Datu kopas, datu plūsma un saistītais pakalpojums](media/data-factory-validate.png)

11. <span data-ttu-id="5008e-166">Dodieties uz **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="5008e-166">Navigate to **Manage**.</span></span> <span data-ttu-id="5008e-167">Sadaļā **Savienojumi** atlasiet **Saistītais pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="5008e-167">Under **Connections**, select **Linked Service**.</span></span> <span data-ttu-id="5008e-168">Atlasiet **DynamicsCrmLinkedService**.</span><span class="sxs-lookup"><span data-stu-id="5008e-168">Select **DynamicsCrmLinkedService**.</span></span> <span data-ttu-id="5008e-169">Formā **Rediģēt saistīto pakalpojumu (Dynamics CRM)** ievadiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="5008e-169">In the **Edit linked service (Dynamics CRM)** form, enter the following values:</span></span>

    <span data-ttu-id="5008e-170">Lauks</span><span class="sxs-lookup"><span data-stu-id="5008e-170">Field</span></span> | <span data-ttu-id="5008e-171">Vērtība</span><span class="sxs-lookup"><span data-stu-id="5008e-171">Value</span></span>
    ---|---
    <span data-ttu-id="5008e-172">Nosaukums/vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="5008e-172">Name</span></span> | <span data-ttu-id="5008e-173">Atlasiet DynamicsCrmLinkedService</span><span class="sxs-lookup"><span data-stu-id="5008e-173">DynamicsCrmLinkedService</span></span>
    <span data-ttu-id="5008e-174">Apraksts</span><span class="sxs-lookup"><span data-stu-id="5008e-174">Description</span></span> | <span data-ttu-id="5008e-175">Saistītie pakalpojumi, kas ir jāsavieno ar CRM instanci, lai ienestu elementu datus</span><span class="sxs-lookup"><span data-stu-id="5008e-175">Linked services to connect with CRM instance to fetch entities data</span></span>
    <span data-ttu-id="5008e-176">Izveidot savienojumu, izmantojot integrācijas izpildlaiku</span><span class="sxs-lookup"><span data-stu-id="5008e-176">Connect via integration runtime</span></span> | <span data-ttu-id="5008e-177">AutoResolvelntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5008e-177">AutoResolvelntegrationRuntime</span></span>
    <span data-ttu-id="5008e-178">Izvietošanas veids</span><span class="sxs-lookup"><span data-stu-id="5008e-178">Deployment type</span></span> | <span data-ttu-id="5008e-179">Tiešsaiste</span><span class="sxs-lookup"><span data-stu-id="5008e-179">Online</span></span>
    <span data-ttu-id="5008e-180">Pakalpojuma Uri</span><span class="sxs-lookup"><span data-stu-id="5008e-180">Service Uri</span></span> | `https://<organization-name>.crm[x].dynamics.com`
    <span data-ttu-id="5008e-181">Autentifikācijas veids</span><span class="sxs-lookup"><span data-stu-id="5008e-181">Authentication type</span></span> | <span data-ttu-id="5008e-182">Office365</span><span class="sxs-lookup"><span data-stu-id="5008e-182">Office365</span></span>
    <span data-ttu-id="5008e-183">Lietotājvārds</span><span class="sxs-lookup"><span data-stu-id="5008e-183">User name</span></span> |
    <span data-ttu-id="5008e-184">Parole vai Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="5008e-184">Password or Azure Key Vault</span></span> | <span data-ttu-id="5008e-185">Parole</span><span class="sxs-lookup"><span data-stu-id="5008e-185">Password</span></span>
    <span data-ttu-id="5008e-186">Parole</span><span class="sxs-lookup"><span data-stu-id="5008e-186">Password</span></span> |

## <a name="run-the-template"></a><span data-ttu-id="5008e-187">Palaist veidni</span><span class="sxs-lookup"><span data-stu-id="5008e-187">Run the template</span></span>

1. <span data-ttu-id="5008e-188">Apturiet šo **Konta**, **Kontaktpersonas** un **Kreditora** dubultās rakstīšanas darbību, izmantojot programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5008e-188">Stop the following **Account**, **Contact**, and **Vendor** dual-write using the Finance and Operations app.</span></span>

    + <span data-ttu-id="5008e-189">Debitori V3 (konti)</span><span class="sxs-lookup"><span data-stu-id="5008e-189">Customers V3(accounts)</span></span>
    + <span data-ttu-id="5008e-190">Debitori V3 (kontaktpersonas)</span><span class="sxs-lookup"><span data-stu-id="5008e-190">Customers V3(contacts)</span></span>
    + <span data-ttu-id="5008e-191">CDS kontaktpersonas V2 (kontaktpersonas)</span><span class="sxs-lookup"><span data-stu-id="5008e-191">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="5008e-192">CDS kontaktpersonas V2 (kontaktpersonas)</span><span class="sxs-lookup"><span data-stu-id="5008e-192">CDS Contacts V2(contacts)</span></span>
    + <span data-ttu-id="5008e-193">Kreditors V2 (msdyn_vendor)</span><span class="sxs-lookup"><span data-stu-id="5008e-193">Vendor V2 (msdyn_vendor)</span></span>

2. <span data-ttu-id="5008e-194">Pārliecinieties, ka kartes no tabulas ir noņemtas no tabulas `msdy_dualwriteruntimeconfig` pakalpojumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5008e-194">Make sure the maps are removed from the `msdy_dualwriteruntimeconfig` table in Dataverse.</span></span>

3. <span data-ttu-id="5008e-195">Instalējiet [Dubultās rakstīšanas puses un globālās adrešu grāmatas risinājumus](https://aka.ms/dual-write-gab) no AppSource.</span><span class="sxs-lookup"><span data-stu-id="5008e-195">Install [Dual-write Party and Global Address Book Solutions](https://aka.ms/dual-write-gab) from AppSource.</span></span>

4. <span data-ttu-id="5008e-196">Ja šajās tabulās ir dati, tad programmā Finance and Operations palaidiet tām **Sākuma sinhronizāciju**.</span><span class="sxs-lookup"><span data-stu-id="5008e-196">In the Finance and Operations app, if the following tables contain data, then run **Initial Sync** for them.</span></span>

    + <span data-ttu-id="5008e-197">Uzrunas</span><span class="sxs-lookup"><span data-stu-id="5008e-197">Salutations</span></span>
    + <span data-ttu-id="5008e-198">Personas rakstura veidi</span><span class="sxs-lookup"><span data-stu-id="5008e-198">Personal character types</span></span>
    + <span data-ttu-id="5008e-199">Komplimentāra slēgšana</span><span class="sxs-lookup"><span data-stu-id="5008e-199">Complimentary closing</span></span>
    + <span data-ttu-id="5008e-200">Kontaktpersonu amati</span><span class="sxs-lookup"><span data-stu-id="5008e-200">Contact person titles</span></span>
    + <span data-ttu-id="5008e-201">Lēmumu pieņemšanas lomas</span><span class="sxs-lookup"><span data-stu-id="5008e-201">Decision making roles</span></span>
    + <span data-ttu-id="5008e-202">Lojalitātes programmu līmeņi</span><span class="sxs-lookup"><span data-stu-id="5008e-202">Loyalty levels</span></span>

5. <span data-ttu-id="5008e-203">Customer Engagement programmā deaktivizējiet tālāk norādītas darbības.</span><span class="sxs-lookup"><span data-stu-id="5008e-203">In the customer engagement app, disable the following plugin steps.</span></span>

    + <span data-ttu-id="5008e-204">Konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-204">Account Update</span></span>
         + <span data-ttu-id="5008e-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-205">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="5008e-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-206">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="5008e-207">Kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-207">Contact Update</span></span>
         + <span data-ttu-id="5008e-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-208">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="5008e-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-209">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="5008e-210">msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-210">msdyn_party Update</span></span>
         + <span data-ttu-id="5008e-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-211">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="5008e-212">msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-212">msdyn_vendor Update</span></span>
         + <span data-ttu-id="5008e-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-213">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

6. <span data-ttu-id="5008e-214">Customer Engagement programmā deaktivizējiet tālāk norādītas darba plūsmas.</span><span class="sxs-lookup"><span data-stu-id="5008e-214">In the customer engagement app, disable the following workflows:</span></span>

    + <span data-ttu-id="5008e-215">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-215">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="5008e-216">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-216">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="5008e-217">Izveidot kreditorus ar veidu persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-217">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="5008e-218">Izveidot kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-218">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="5008e-219">Kreditoru atjaunināšana kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-219">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="5008e-220">Kreditoru atjaunināšana kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-220">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="5008e-221">Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-221">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="5008e-222">Atjaunināt kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-222">Update Vendors of type Person in Vendors Table</span></span>

7. <span data-ttu-id="5008e-223">Datu fabrikā palaidiet veidni, atlasot **Aktivizēt tūlīt**, kā parādīts šajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="5008e-223">In the data factory, run the template by selecting **Trigger now** as shown in the following image.</span></span> <span data-ttu-id="5008e-224">Šis process var ilgt dažas stundas, balstoties uz datu apjomu.</span><span class="sxs-lookup"><span data-stu-id="5008e-224">This process might take a few hours to complete based on the data volume.</span></span>

    ![Trigera palaišana](media/data-factory-trigger.png)

    > [!NOTE]
    > <span data-ttu-id="5008e-226">Ja ir pielāgojumi **Kontam**, **Kontaktpersonai** un **Kreditoram** veidne jāmodificē.</span><span class="sxs-lookup"><span data-stu-id="5008e-226">If you have customizations for **Account**, **Contact**, and **Vendor** then you must modify the template.</span></span>

8. <span data-ttu-id="5008e-227">Importēt jaunos **Puses** ierakstus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5008e-227">Import the new **Party** records in the Finance and Operations app.</span></span>

    + <span data-ttu-id="5008e-228">Lejupielādējiet `FONewParty.csv` failu no Azure BLOB krātuves.</span><span class="sxs-lookup"><span data-stu-id="5008e-228">Download the `FONewParty.csv` file from Azure blob storage.</span></span> <span data-ttu-id="5008e-229">Ceļš ir `partybootstrapping/output/FONewParty.csv`.</span><span class="sxs-lookup"><span data-stu-id="5008e-229">The path is `partybootstrapping/output/FONewParty.csv`.</span></span>
    + <span data-ttu-id="5008e-230">Konvertējiet `FONewParty.csv` failu par Excel failu un importējiet Excel failu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5008e-230">Convert the `FONewParty.csv` file into an Excel file and import the Excel file into the Finance and Operations app.</span></span>  <span data-ttu-id="5008e-231">Ja jums darbojas csv importēšana, varat tieši importēt csv failu.</span><span class="sxs-lookup"><span data-stu-id="5008e-231">If the csv import works for you, you can import csv file directly.</span></span> <span data-ttu-id="5008e-232">Atkarībā no datu apjoma, importēšanas laiks var ilgt dažas stundas.</span><span class="sxs-lookup"><span data-stu-id="5008e-232">The import could take a few hours to run, depending on the data volume.</span></span> <span data-ttu-id="5008e-233">Papildinformāciju skatiet [Datu importēšanas un eksportēšanas darbu apskats](../data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="5008e-233">For more information, see [Data import and export jobs overview](../data-import-export-job.md).</span></span>

    ![Importēt Datavers puses ierakstus](media/data-factory-import-party.png)

9. <span data-ttu-id="5008e-235">Customer Engagement programmās aktivizējiet tālāk norādītas darbības:</span><span class="sxs-lookup"><span data-stu-id="5008e-235">In the customer engagement apps, enable the following plugin steps:</span></span>

    + <span data-ttu-id="5008e-236">Konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-236">Account Update</span></span>
         + <span data-ttu-id="5008e-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-237">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromAccountEntity: Update of account</span></span>
         + <span data-ttu-id="5008e-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: konta atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-238">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: Update of account</span></span>
    + <span data-ttu-id="5008e-239">Kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-239">Contact Update</span></span>
         + <span data-ttu-id="5008e-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-240">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromContactEntity: Update of contact</span></span>
         + <span data-ttu-id="5008e-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: kontaktpersonas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-241">Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: Update of contact</span></span>
    + <span data-ttu-id="5008e-242">msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-242">msdyn_party Update</span></span>
         + <span data-ttu-id="5008e-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: msdyn_party atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-243">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromPartyEntity: Update of msdyn_party</span></span>
    + <span data-ttu-id="5008e-244">msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-244">msdyn_vendor Update</span></span>
         + <span data-ttu-id="5008e-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: msdyn_vendor atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5008e-245">Microsoft.Dynamics.GABExtended.Plugins.UpdatePartyAttributesFromVendorEntity: Update of msdyn_vendor</span></span>

10. <span data-ttu-id="5008e-246">Customer Engagement programmās aktivizējiet šādas darbplūsmas, ja tās ir deaktivizētas iepriekšējās darbībās:</span><span class="sxs-lookup"><span data-stu-id="5008e-246">In the customer engagement apps, activate the following workflows if you deactivated them in previous steps:</span></span>

    + <span data-ttu-id="5008e-247">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-247">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="5008e-248">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-248">Create Vendors in Accounts Table</span></span>
    + <span data-ttu-id="5008e-249">Izveidot kreditorus ar veidu persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-249">Create Vendors of type person in Contacts Table</span></span>
    + <span data-ttu-id="5008e-250">Izveidot kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-250">Create Vendors of type Person in Vendors Table</span></span>
    + <span data-ttu-id="5008e-251">Kreditoru atjaunināšana kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-251">Update Vendors in Accounts Table</span></span>
    + <span data-ttu-id="5008e-252">Kreditoru atjaunināšana kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-252">Update Vendors in Vendors Table</span></span>
    + <span data-ttu-id="5008e-253">Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-253">Update Vendors of type Person in Contacts Table</span></span>
    + <span data-ttu-id="5008e-254">Atjaunināt kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="5008e-254">Update Vendors of type Person in Vendors Table</span></span>

11. <span data-ttu-id="5008e-255">Palaidiet ar **Pusi** saistītās kartes, kā norādīts sadaļā [Puse un globālā adrešu grāmata](party-gab.md).</span><span class="sxs-lookup"><span data-stu-id="5008e-255">Run the **Party**-related maps as instructed in [Party and global address book](party-gab.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="5008e-256">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="5008e-256">Troubleshooting</span></span>

1. <span data-ttu-id="5008e-257">Procesā neizdodas vēlreiz palaist datu fabriku, sākot no neveiksmīgās darbības.</span><span class="sxs-lookup"><span data-stu-id="5008e-257">In the process fails, rerun the data factory starting from the failed activity.</span></span>
2. <span data-ttu-id="5008e-258">Dažus failus ģenerē datu fabrika, ko varat izmantot datu apstiprināšanas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="5008e-258">Some files are generated by the data factory that you can use for data validation purpose.</span></span>
3. <span data-ttu-id="5008e-259">Datu fabrika darbojas, pamatojoties uz csv failiem, kas tiek atdalīti ar komatu.</span><span class="sxs-lookup"><span data-stu-id="5008e-259">The data factory runs based on csv files that are comma-delimited.</span></span> <span data-ttu-id="5008e-260">Ja lauka vērtībai ir komats, tas var traucēt rezultātus.</span><span class="sxs-lookup"><span data-stu-id="5008e-260">If there is a field value that has a comma, it may interfere with the results.</span></span> <span data-ttu-id="5008e-261">Ir jānoņem komati.</span><span class="sxs-lookup"><span data-stu-id="5008e-261">You need to remove the commas.</span></span>
4. <span data-ttu-id="5008e-262">Cilne **Pārraudzība** sniedz informāciju par visam darbībam un apstrādātajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="5008e-262">The **Monitoring** tab provides information about all steps and data processed.</span></span> <span data-ttu-id="5008e-263">Atlasiet noteiktu darbību, lai to atkļūdotu.</span><span class="sxs-lookup"><span data-stu-id="5008e-263">Select a specific step to debug it.</span></span>

    ![Cilne Pārraudzība](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a><span data-ttu-id="5008e-265">Uzziniet vairāk par veidni</span><span class="sxs-lookup"><span data-stu-id="5008e-265">Learn more about the template</span></span>

<span data-ttu-id="5008e-266">Komentārus veidnei varat atrast [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) failā.</span><span class="sxs-lookup"><span data-stu-id="5008e-266">You can find comments for the template the [readme.md](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md) file.</span></span>