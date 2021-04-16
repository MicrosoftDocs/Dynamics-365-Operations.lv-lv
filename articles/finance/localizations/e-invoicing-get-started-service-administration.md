---
title: Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu
description: Šajā tēmā ir paskaidrots, kā sākt darbu ar Elektronisko rēķinu izrakstīšanu.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840152"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="2398f-103">Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu</span><span class="sxs-lookup"><span data-stu-id="2398f-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="2398f-104">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="2398f-104">Prerequisites</span></span>

<span data-ttu-id="2398f-105">Pirms pabeidzat šajā tēmā norādītās procedūras, ir jāievieš šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="2398f-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="2398f-106">Jums ir jābūt piekļuvei jūsu Microsoft Dynamics Lifecycle Services (LCS) kontam.</span><span class="sxs-lookup"><span data-stu-id="2398f-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="2398f-107">Jums jābūt LCS projektam, kas ietver Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management programmu versiju 10.0.17 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="2398f-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2398f-108">Turklāt šīs programmas ir jāizvieto vienā no tālāk minētajām Azure ģeogrāfiskām vietām:</span><span class="sxs-lookup"><span data-stu-id="2398f-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="2398f-109">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="2398f-109">East US</span></span>
    - <span data-ttu-id="2398f-110">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="2398f-110">West US</span></span>
    - <span data-ttu-id="2398f-111">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="2398f-111">North EU</span></span>
    - <span data-ttu-id="2398f-112">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="2398f-112">West EU</span></span>

- <span data-ttu-id="2398f-113">Jums ir jābūt piekļuvei jūsu Dynamics 365 Regulatory Configuration Services (RCS) kontam.</span><span class="sxs-lookup"><span data-stu-id="2398f-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="2398f-114">Jums jāaktivizē Globalizācijas līdzeklis jūsu RCS kontā Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="2398f-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="2398f-115">Papildinformāciju skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="2398f-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="2398f-116">Jums jāizveido galvenā glabātuve un krātuves kontu risinājumā Azure.</span><span class="sxs-lookup"><span data-stu-id="2398f-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="2398f-117">Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="2398f-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="2398f-118">Instalējiet programmu Microservices pievienojumprogrammu pakalpojumam Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="2398f-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="2398f-119">Piesakieties savā LCS kontā.</span><span class="sxs-lookup"><span data-stu-id="2398f-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="2398f-120">Atlasiet **Priekšskatījuma līdzekļu pārvaldības** elementu.</span><span class="sxs-lookup"><span data-stu-id="2398f-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="2398f-121">Sadaļā **Publiskā priekšskatījuma līdzekļi** atlasiet **e-rēķinu izrakstīšanas pakalpojumu**.</span><span class="sxs-lookup"><span data-stu-id="2398f-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="2398f-122">Pārliecinieties, vai opcija **Priekšskatījuma līdzeklis iespējots** ir iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="2398f-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="2398f-123">LCS informācijas panelī atlasiet savu LCS izvietošanas projektu.</span><span class="sxs-lookup"><span data-stu-id="2398f-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="2398f-124">LCS projektam jādarbojas.</span><span class="sxs-lookup"><span data-stu-id="2398f-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="2398f-125">Cilnē **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="2398f-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="2398f-126">Izvēlieties **e-rēķinu pakalpojumus**.</span><span class="sxs-lookup"><span data-stu-id="2398f-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="2398f-127">Laukā **AAD pieteikuma ID** ievadiet **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="2398f-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="2398f-128">Šī ir fiksēta vērtība.</span><span class="sxs-lookup"><span data-stu-id="2398f-128">This is a fixed value.</span></span>
10. <span data-ttu-id="2398f-129">Laukā **AAD nomnieka ID** ievadiet jūsu Azure abonementa konta nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="2398f-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="2398f-130">Pārskatiet noteikumus un nosacījumus un atzīmējiet izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="2398f-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="2398f-131">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="2398f-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="2398f-132">Iestatiet RCS integrācijas parametrus ar elektronisko rēķinu izrakstīšanu</span><span class="sxs-lookup"><span data-stu-id="2398f-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="2398f-133">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="2398f-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="2398f-134">Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="2398f-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="2398f-135">Cilnē **e-rēķinu pakalpojums** laukā **Pakalpojuma galapunkta URI** ievadiet atbilstoši azure ģeogrāfijas pakalpojuma galapunktu, kā norādīts tālāk sniegtajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="2398f-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="2398f-136">Datacenter Azure ģeogrāfija</span><span class="sxs-lookup"><span data-stu-id="2398f-136">Datacenter Azure geography</span></span> | <span data-ttu-id="2398f-137">Pakalpojuma galapunkta URI</span><span class="sxs-lookup"><span data-stu-id="2398f-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="2398f-138">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="2398f-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="2398f-139">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="2398f-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="2398f-140">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="2398f-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="2398f-141">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="2398f-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="2398f-142">Pārbaudiet, vai **Lietojumprogrammas Id** lauks ir iestatīts uz **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="2398f-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="2398f-143">Šī vērtība ir fiksēta vērtība.</span><span class="sxs-lookup"><span data-stu-id="2398f-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="2398f-144">Laukā **LCS vides Id** ievadiet jūsu LCS vides ID.</span><span class="sxs-lookup"><span data-stu-id="2398f-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="2398f-145">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="2398f-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="2398f-146">Atslēgas akreditācijas datu komplekta atsauksmju veidošana</span><span class="sxs-lookup"><span data-stu-id="2398f-146">Create Key Vault references</span></span>

1. <span data-ttu-id="2398f-147">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="2398f-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="2398f-148">Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="2398f-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="2398f-149">Lapā **Vides iestatījumi** darbības rūtī atlasiet **Pakalpojuma vide** un atlasiet **Atslēgas glabātuves parametri**.</span><span class="sxs-lookup"><span data-stu-id="2398f-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="2398f-150">Atlasiet **Jauns**, lai izveidotu atslēgas glabātuves atsauci.</span><span class="sxs-lookup"><span data-stu-id="2398f-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="2398f-151">Laukā **Nosaukums** ievadiet atslēgas glabātuves atsauces nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2398f-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="2398f-152">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="2398f-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="2398f-153">Laukā **Atslēgas glabātuves URI** ielīmējiet atslēgas glabātuves noslēpumu no Azure atslēgas glabātuves.</span><span class="sxs-lookup"><span data-stu-id="2398f-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="2398f-154">Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="2398f-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="2398f-155">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2398f-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="2398f-156">Izveidojiet krātuves noslēpumu</span><span class="sxs-lookup"><span data-stu-id="2398f-156">Create Storage account secret</span></span>

1. <span data-ttu-id="2398f-157">Lapā **Vides iestatījumi** darbības rūtī atlasiet **Pakalpojuma vide** > **Atslēgas glabātuves parametri**.</span><span class="sxs-lookup"><span data-stu-id="2398f-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="2398f-158">Atlasiet **Atslēgas glabātuves atsauce** un sadaļā **Sertifikāti** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="2398f-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="2398f-159">Laukā **Nosaukums** ievadiet glabātuves konta noslēpuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2398f-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="2398f-160">Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="2398f-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="2398f-161">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="2398f-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="2398f-162">Laukā **Tips** atlasiet **Noslēpums**.</span><span class="sxs-lookup"><span data-stu-id="2398f-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="2398f-163">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="2398f-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="2398f-164">Ciparsertifikātu noslēpuma izveide</span><span class="sxs-lookup"><span data-stu-id="2398f-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="2398f-165">Lapā **Vides iestatījumi** darbības rūtī atlasiet **Pakalpojuma vide** un atlasiet **Atslēgas glabātuves parametri**.</span><span class="sxs-lookup"><span data-stu-id="2398f-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="2398f-166">Atlasiet **Atslēgas glabātuves atsauce** un tad sadaļā **Sertifikāti** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="2398f-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="2398f-167">Laukā **Nosaukums** ievadiet ciparsertifikāta noslēpuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2398f-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="2398f-168">Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="2398f-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="2398f-169">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="2398f-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="2398f-170">Laukā **Tips** atlasiet **Sertifikāts**.</span><span class="sxs-lookup"><span data-stu-id="2398f-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="2398f-171">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="2398f-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="2398f-172">Pakalpojumu vides izveide</span><span class="sxs-lookup"><span data-stu-id="2398f-172">Create a service environment</span></span>

1. <span data-ttu-id="2398f-173">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="2398f-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="2398f-174">Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="2398f-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="2398f-175">Lapā **Vides iestatījumi** darbību rūtī atlasiet **Pakalpojuma vide**.</span><span class="sxs-lookup"><span data-stu-id="2398f-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="2398f-176">Atlasiet **Jauns**, lai izveidotu jaunu pakalpojuma vidi.</span><span class="sxs-lookup"><span data-stu-id="2398f-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="2398f-177">Laukā **Nosaukums** ievadiet e-rēķinu izrakstīšanas vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2398f-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="2398f-178">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="2398f-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="2398f-179">Laukā **Krātuves SAS marķiera noslēpums** atlasiet tā krātuves konta noslēpuma nosaukumu, kas jāizmanto, lai autentificētu piekļuvi krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="2398f-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="2398f-180">Sadaļā **Lietotāji** atlasiet **Pievienot**, lai pievienotu lietotāju, kuram ir atļauts iesniegt elektroniskos rēķinus, izmantojot vidi, un arī pievienojieties krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="2398f-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="2398f-181">Laukā **Lietotāja ID** ievadiet lietotāja aizstājvārdu.</span><span class="sxs-lookup"><span data-stu-id="2398f-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="2398f-182">Laukā **E-pasta adrese** ievadiet lietotāja e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="2398f-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="2398f-183">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2398f-183">Select **Save**.</span></span>
10. <span data-ttu-id="2398f-184">Ja jūsu valstij/reģionam raksturīgiem rēķiniem ir nepieciešama sertifikātu ķēde, lai pielietotu elektroniskos parakstus, Darbības rūtī atlasiet **Atslēgas glabātuves parametrus** pēc tam atlasiet **Sertifikātu ķēde** un sekojiet šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="2398f-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="2398f-185">Atlasiet **Jauns**, lai izveidotu sertifikātu ķēdi.</span><span class="sxs-lookup"><span data-stu-id="2398f-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="2398f-186">Laukā **Nosaukums** ievadiet sertifikātu ķēdes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2398f-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="2398f-187">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="2398f-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="2398f-188">Sadaļā **Sertifikāti** atlasiet **Pievienot**, lai pievienotu ķēdei sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="2398f-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="2398f-189">Izmantojiet pogu **Augšā** vai **Lejā**, lai mainītu sertifikāta pozīciju ķēdē.</span><span class="sxs-lookup"><span data-stu-id="2398f-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="2398f-190">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="2398f-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="2398f-191">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2398f-191">Close the page.</span></span>
11. <span data-ttu-id="2398f-192">Darbības rūtī lapā **Pakalpojuma vide** atlasiet **Publicēt**, lai publicētu vidi mākonī.</span><span class="sxs-lookup"><span data-stu-id="2398f-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="2398f-193">Lauka **Statuss** vērtība mainīta uz **Publicēts**.</span><span class="sxs-lookup"><span data-stu-id="2398f-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="2398f-194">Izveidojiet pievienotu pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="2398f-194">Create a connected application</span></span>

1. <span data-ttu-id="2398f-195">Lapā **Vides iestatījumi** darbību rūtī atlasiet **Savienotās lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="2398f-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="2398f-196">Atlasiet **Jauns**, lai izveidotu savienotu lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="2398f-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="2398f-197">Laukā **Nosaukums** ievadiet savienotās lietojumprogrammas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2398f-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="2398f-198">Laukā **Lietojumprogramma** ievadiet Finance un Supply Chain Management vides URL, ar kuru veidot savienojumu.</span><span class="sxs-lookup"><span data-stu-id="2398f-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="2398f-199">Laukā **Īrnieks** ievadiet Finance un Supply Chain Management vides īrnieku.</span><span class="sxs-lookup"><span data-stu-id="2398f-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="2398f-200">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="2398f-200">Select **Save**.</span></span>
6. <span data-ttu-id="2398f-201">Darbību rūtī atlasiet **Pārbaudīt savienojumu**, lai pārbaudītu savienojumu ar vidi.</span><span class="sxs-lookup"><span data-stu-id="2398f-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="2398f-202">Tad aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="2398f-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="2398f-203">Saistīt savienotās programmas ar vidēm</span><span class="sxs-lookup"><span data-stu-id="2398f-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="2398f-204">Lai videi piešķirtu pievienoto programmu **Vides iestatījumu** lapā atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="2398f-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="2398f-205">Laukā **Savienotā programma** atlasiet savienoto lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="2398f-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="2398f-206">Laukā **Pakalpojuma vide** atlasiet darba pasūtījuma pakalpojuma vidi.</span><span class="sxs-lookup"><span data-stu-id="2398f-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="2398f-207">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="2398f-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="2398f-208">Iestatīt elektronisko rēķinu izrakstīšanas integrēšanu Finance un Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2398f-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="2398f-209">Iesledziet elektronisko rēķinu izrakstīšanas integrācijas līdzekli</span><span class="sxs-lookup"><span data-stu-id="2398f-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="2398f-210">Pierakstieties jūsu Finance vai Supply Chain Management instancē.</span><span class="sxs-lookup"><span data-stu-id="2398f-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="2398f-211">Darbvietā **Līdzekļu pārvaldība** meklējiet līdzekli **Konfigurējamā elektronisko rēķinu izrakstīšanas integrācija**.</span><span class="sxs-lookup"><span data-stu-id="2398f-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="2398f-212">Ja šis līdzeklis lapā nav redzams, atlasiet **Pārbaudīt, vai nav atjauninājumu**.</span><span class="sxs-lookup"><span data-stu-id="2398f-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="2398f-213">Atlasiet līdzekli un pēc tam atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="2398f-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="2398f-214">Pakalpojuma galapunkta URL iestatīšana</span><span class="sxs-lookup"><span data-stu-id="2398f-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="2398f-215">Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.</span><span class="sxs-lookup"><span data-stu-id="2398f-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="2398f-216">Cilnē **Iesniegšanas pakalpojums** laukā **Pakalpojuma galapunkta URL** ievadiet atbilstoši azure ģeogrāfijas pakalpojuma galapunktu, kā norādīts tālāk sniegtajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="2398f-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="2398f-217">Datacenter Azure ģeogrāfija</span><span class="sxs-lookup"><span data-stu-id="2398f-217">Datacenter Azure geography</span></span> | <span data-ttu-id="2398f-218">Pakalpojuma galapunkta URL</span><span class="sxs-lookup"><span data-stu-id="2398f-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="2398f-219">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="2398f-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="2398f-220">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="2398f-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="2398f-221">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="2398f-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="2398f-222">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="2398f-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="2398f-223">Laukā **Vide** ievadiet pakalpojumu vides nosaukumu, kas publicēts elektronisko rēķinu izrakstīšanā.</span><span class="sxs-lookup"><span data-stu-id="2398f-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="2398f-224">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="2398f-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="2398f-225">Iespējot testējamās atslēgas</span><span class="sxs-lookup"><span data-stu-id="2398f-225">Enable Flighting keys</span></span>

<span data-ttu-id="2398f-226">Iespējojiet testējamās atslēgas Microsoft Dynamics 365 Finance vai Microsoft Dynamics 365 Supply Chain Management versijām 10.0.17 vai vecākām versijām.</span><span class="sxs-lookup"><span data-stu-id="2398f-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="2398f-227">Izpildiet šādu SQL komandu:</span><span class="sxs-lookup"><span data-stu-id="2398f-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="2398f-228">IEVIETOT SYSFLIGHTING (FLIGHTNAME, IESPĒJOTS) VĒRTĪBAS ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="2398f-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="2398f-229">IEVIETOT SYSFLIGHTING (FLIGHTNAME, IESPĒJOTS) VĒRTĪBAS ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="2398f-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="2398f-230">Izpildiet IISreset komandu visām AOS.</span><span class="sxs-lookup"><span data-stu-id="2398f-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
