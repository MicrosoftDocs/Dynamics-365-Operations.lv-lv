---
title: Darba sākšana ar Elektroniskās rēķinu izrakstīšanas pievienojumprogrammas pakalpojuma administrēšanu
description: Šajā tēmā ir paskaidrots, kā sākt darbu ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592530"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="7eee9-103">Darba sākšana ar Elektroniskās rēķinu izrakstīšanas pievienojumprogrammas pakalpojuma administrēšanu</span><span class="sxs-lookup"><span data-stu-id="7eee9-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="7eee9-104">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="7eee9-104">Prerequisites</span></span>

<span data-ttu-id="7eee9-105">Pirms pabeidzat šajā tēmā norādītās procedūras, ir jāievieš šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="7eee9-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="7eee9-106">Jums ir jābūt piekļuvei jūsu Microsoft Dynamics Lifecycle Services (LCS) kontam.</span><span class="sxs-lookup"><span data-stu-id="7eee9-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="7eee9-107">Jums jābūt LCS projektam, kas ietver Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management programmu versiju 10.0.17 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="7eee9-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="7eee9-108">Turklāt šīs programmas ir jāizvieto vienā no tālāk minētajām Azure ģeogrāfiskām vietām:</span><span class="sxs-lookup"><span data-stu-id="7eee9-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="7eee9-109">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="7eee9-109">East US</span></span>
    - <span data-ttu-id="7eee9-110">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="7eee9-110">West US</span></span>
    - <span data-ttu-id="7eee9-111">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="7eee9-111">North EU</span></span>
    - <span data-ttu-id="7eee9-112">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="7eee9-112">West EU</span></span>

- <span data-ttu-id="7eee9-113">Jums ir jābūt piekļuvei jūsu Dynamics 365 Regulatory Configuration Services (RCS) kontam.</span><span class="sxs-lookup"><span data-stu-id="7eee9-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="7eee9-114">Jums jāaktivizē Globalizācijas līdzeklis jūsu RCS kontā Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="7eee9-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="7eee9-115">Papildinformāciju skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="7eee9-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="7eee9-116">Jums jāizveido galvenā glabātuve un krātuves kontu risinājumā Azure.</span><span class="sxs-lookup"><span data-stu-id="7eee9-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="7eee9-117">Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="7eee9-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="7eee9-118">Instalējiet programmu Microservices pievienojumprogrammu pakalpojumam Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="7eee9-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="7eee9-119">Piesakieties savā LCS kontā.</span><span class="sxs-lookup"><span data-stu-id="7eee9-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="7eee9-120">Atlasiet **Priekšskatījuma līdzekļu pārvaldības** elementu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="7eee9-121">Sadaļā **Publiskā priekšskatījuma līdzekļi** atlasiet **e-rēķinu izrakstīšanas pakalpojumu**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="7eee9-122">Pārliecinieties, vai opcija **Priekšskatījuma līdzeklis iespējots** ir iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="7eee9-123">LCS informācijas panelī atlasiet savu LCS izvietošanas projektu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="7eee9-124">LCS projektam jādarbojas.</span><span class="sxs-lookup"><span data-stu-id="7eee9-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="7eee9-125">Cilnē **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="7eee9-126">Atlasiet **e-rēķinu izrakstīšanas pakalpojumi** un laikā **AAD programmas ID** ievadiet **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="7eee9-127">Šī ir fiksēta vērtība.</span><span class="sxs-lookup"><span data-stu-id="7eee9-127">This is a fixed value.</span></span>
10. <span data-ttu-id="7eee9-128">Laukā **AAD nomnieka ID** ievadiet jūsu Azure abonementa konta nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="7eee9-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="7eee9-129">Pārskatiet noteikumus un nosacījumus un atzīmējiet izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="7eee9-130">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="7eee9-131">Iestatiet RCS integrācijas parametrus ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="7eee9-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="7eee9-132">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="7eee9-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="7eee9-133">Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="7eee9-134">Cilnē **e-rēķinu pakalpojums** laukā **Pakalpojuma galapunkta URI** ievadiet atbilstoši azure ģeogrāfijas pakalpojuma galapunktu, kā norādīts tālāk sniegtajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="7eee9-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="7eee9-135">Datacenter Azure ģeogrāfija</span><span class="sxs-lookup"><span data-stu-id="7eee9-135">Datacenter Azure geography</span></span> | <span data-ttu-id="7eee9-136">Pakalpojuma galapunkta URI</span><span class="sxs-lookup"><span data-stu-id="7eee9-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="7eee9-137">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="7eee9-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7eee9-138">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="7eee9-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7eee9-139">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="7eee9-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7eee9-140">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="7eee9-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="7eee9-141">Pārbaudiet, vai **Lietojumprogrammas Id** lauks ir iestatīts uz **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="7eee9-142">Šī vērtība ir fiksēta vērtība.</span><span class="sxs-lookup"><span data-stu-id="7eee9-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="7eee9-143">Laukā **LCS vides Id** ievadiet jūsu LCS abonementa konta ID.</span><span class="sxs-lookup"><span data-stu-id="7eee9-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="7eee9-144">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="7eee9-145">Izveidojiet Galvenās glabātavas noslēpumu</span><span class="sxs-lookup"><span data-stu-id="7eee9-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="7eee9-146">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="7eee9-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="7eee9-147">Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="7eee9-148">Lapā **Vides iestatījumi** darbības rūtī atlasiet **Pakalpojuma vide** un atlasiet **Atslēgas glabātuves parametri**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="7eee9-149">Atlasiet **Jauns**, lai izveidotu atslēgas glabātuves noslēpumu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="7eee9-150">Laukā **Nosaukums** ievadiet atslēgas glabātuves noslēpuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="7eee9-151">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="7eee9-152">Laukā **Atslēgas glabātuves URI** ielīmējiet noslēpumu no Azure atslēgas glabātuves.</span><span class="sxs-lookup"><span data-stu-id="7eee9-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="7eee9-153">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="7eee9-154">Izveidojiet krātuves noslēpumu</span><span class="sxs-lookup"><span data-stu-id="7eee9-154">Create Storage account secret</span></span>

1. <span data-ttu-id="7eee9-155">Dodieties uz **Sistēmas administrēšana** > **Iestatījumi** > **Atslēgas glabātavas parametri** un atlasiet Atslēgas glabātavas noslēpumu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="7eee9-156">Sadaļā **Sertifikāti** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="7eee9-157">Laukā **Nosaukums** ievadiet glabāšanas konta noslēpuma nosaukumu un laukā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="7eee9-158">Laukā **Tips** atlasiet **Sertifikāts**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="7eee9-159">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="7eee9-160">Ciparsertifikātu noslēpuma izveide</span><span class="sxs-lookup"><span data-stu-id="7eee9-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="7eee9-161">Dodieties uz **Sistēmas administrēšana** > **Iestatījumi** > **Atslēgas glabātavas parametri** un atlasiet Atslēgas glabātavas noslēpumu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="7eee9-162">Sadaļā **Sertifikāti** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="7eee9-163">Laukā **Nosaukums** ievadiet ciparsertifikāta noslēpuma nosaukumu un laukā **Apraksts** ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="7eee9-164">Laukā **Tips** atlasiet **Sertifikāts**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="7eee9-165">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="7eee9-166">Izveidot elektronisko rēķinu izrakstīšanas pievienojumprogrammas vidi</span><span class="sxs-lookup"><span data-stu-id="7eee9-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="7eee9-167">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="7eee9-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="7eee9-168">Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="7eee9-169">Pakalpojumu vides izveide</span><span class="sxs-lookup"><span data-stu-id="7eee9-169">Create a service environment</span></span>

1. <span data-ttu-id="7eee9-170">Lapā **Vides iestatījumi** darbību rūtī atlasiet **Pakalpojuma vide**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="7eee9-171">Atlasiet **Jauns**, lai izveidotu jaunu pakalpojuma vidi.</span><span class="sxs-lookup"><span data-stu-id="7eee9-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="7eee9-172">Laukā **Nosaukums** ievadiet e-rēķinu izrakstīšanas vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="7eee9-173">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="7eee9-174">Laukā **Krātuves SAS marķiera noslēpums** atlasiet tā krātuves konta noslēpuma nosaukumu, kas jāizmanto, lai autentificētu piekļuvi krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="7eee9-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="7eee9-175">Sadaļā **Lietotāji** atlasiet **Pievienot**, lai pievienotu lietotāju, kuram ir atļauts iesniegt elektroniskos rēķinus, izmantojot vidi, un arī pievienojieties krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="7eee9-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="7eee9-176">Laukā **Lietotāja ID** ievadiet lietotāja aizstājvārdu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="7eee9-177">Laukā **E-pasta adrese** ievadiet lietotāja e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="7eee9-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="7eee9-178">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-178">Select **Save**.</span></span>
8. <span data-ttu-id="7eee9-179">Ja jūsu valstij/reģionam raksturīgiem rēķiniem ir nepieciešama sertifikātu ķēde, lai pielietotu elektroniskos parakstus, Darbības rūtī atlasiet **Atslēgas glabātuves parametrus** pēc tam atlasiet **Sertifikātu ķēde** un sekojiet šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="7eee9-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="7eee9-180">Atlasiet **Jauns**, lai izveidotu sertifikātu ķēdi.</span><span class="sxs-lookup"><span data-stu-id="7eee9-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="7eee9-181">Laukā **Nosaukums** ievadiet sertifikātu ķēdes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="7eee9-182">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="7eee9-183">Sadaļā **Sertifikāti** atlasiet **Pievienot**, lai pievienotu ķēdei sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="7eee9-184">Izmantojiet pogu **Augšā** vai **Lejā**, lai mainītu sertifikāta pozīciju ķēdē.</span><span class="sxs-lookup"><span data-stu-id="7eee9-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="7eee9-185">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="7eee9-186">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-186">Close the page.</span></span>
9. <span data-ttu-id="7eee9-187">Darbības rūtī lapā **Pakalpojuma vide** atlasiet **Publicēt**, lai publicētu vidi mākonī.</span><span class="sxs-lookup"><span data-stu-id="7eee9-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="7eee9-188">Lauka **Statuss** vērtība mainīta uz **Publicēts**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="7eee9-189">Izveidojiet pievienotu pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="7eee9-189">Create a connected application</span></span>

1. <span data-ttu-id="7eee9-190">Lapā **Vides iestatījumi** darbību rūtī atlasiet **Savienotās lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="7eee9-191">Atlasiet **Jauns**, lai izveidotu savienotu lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="7eee9-192">Laukā **Nosaukums** ievadiet savienotās lietojumprogrammas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="7eee9-193">Laukā **Lietojumprogramma** ievadiet Finance un Supply Chain Management vides URL, ar kuru veidot savienojumu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="7eee9-194">Laukā **Īrnieks** ievadiet Finance un Supply Chain Management vides īrnieku.</span><span class="sxs-lookup"><span data-stu-id="7eee9-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="7eee9-195">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-195">Select **Save**.</span></span>
6. <span data-ttu-id="7eee9-196">Darbību rūtī atlasiet **Pārbaudīt savienojumu**, lai pārbaudītu savienojumu ar vidi.</span><span class="sxs-lookup"><span data-stu-id="7eee9-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="7eee9-197">Tad aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="7eee9-198">Saistīt savienotās programmas ar vidēm</span><span class="sxs-lookup"><span data-stu-id="7eee9-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="7eee9-199">Lai videi piešķirtu pievienoto programmu **Vides iestatījumu** lapā atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="7eee9-200">Laukā **Savienotā programma** atlasiet savienoto lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="7eee9-201">Laukā **Pakalpojuma vide** atlasiet darba pasūtījuma pakalpojuma vidi.</span><span class="sxs-lookup"><span data-stu-id="7eee9-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="7eee9-202">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="7eee9-203">Iestatīt elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšanu Finance un Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7eee9-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="7eee9-204">Iesledziet elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrācijas līdzekli</span><span class="sxs-lookup"><span data-stu-id="7eee9-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="7eee9-205">Pierakstieties jūsu Finance vai Supply Chain Management instancē.</span><span class="sxs-lookup"><span data-stu-id="7eee9-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="7eee9-206">Darbvietā **Līdzekļu pārvaldība** meklējiet līdzekli **Konfigurējamā elektronisko rēķinu pievienošanas integrācija**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="7eee9-207">Ja šis līdzeklis lapā nav redzams, atlasiet **Pārbaudīt, vai nav atjauninājumu**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="7eee9-208">Atlasiet līdzekli un pēc tam atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="7eee9-209">Pakalpojuma galapunkta URL iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7eee9-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="7eee9-210">Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.</span><span class="sxs-lookup"><span data-stu-id="7eee9-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="7eee9-211">Cilnē **Iesniegšanas pakalpojums** laukā **Pakalpojuma galapunkta URL** ievadiet atbilstoši azure ģeogrāfijas pakalpojuma galapunktu, kā norādīts tālāk sniegtajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="7eee9-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="7eee9-212">Datacenter Azure ģeogrāfija</span><span class="sxs-lookup"><span data-stu-id="7eee9-212">Datacenter Azure geography</span></span> | <span data-ttu-id="7eee9-213">Pakalpojuma galapunkta URL</span><span class="sxs-lookup"><span data-stu-id="7eee9-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="7eee9-214">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="7eee9-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7eee9-215">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="7eee9-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7eee9-216">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="7eee9-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="7eee9-217">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="7eee9-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="7eee9-218">Laukā **Vide** ievadiet elektronisko rēķinu izrakstīšanas pievienojuma vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="7eee9-219">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="7eee9-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
