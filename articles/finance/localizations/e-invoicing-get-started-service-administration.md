---
title: Darba sākšana ar Elektroniskās rēķinu izrakstīšanas pievienojumprogrammas pakalpojuma administrēšanu
description: Šajā tēmā ir paskaidrots, kā sākt darbu ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104408"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="0c97d-103">Darba sākšana ar Elektroniskās rēķinu izrakstīšanas pievienojumprogrammas pakalpojuma administrēšanu</span><span class="sxs-lookup"><span data-stu-id="0c97d-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="0c97d-104">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="0c97d-104">Prerequisites</span></span>

<span data-ttu-id="0c97d-105">Pirms pabeidzat šajā tēmā norādītās procedūras, ir jāievieš šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="0c97d-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="0c97d-106">Jums ir jābūt piekļuvei jūsu Microsoft Dynamics Lifecycle Services (LCS) kontam.</span><span class="sxs-lookup"><span data-stu-id="0c97d-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="0c97d-107">Jums jābūt LCS projektam, kas ietver Microsoft Dynamics 365 Finance un Dynamics 365 Supply Chain Management programmu versiju 10.0.13 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="0c97d-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0c97d-108">Turklāt šīs programmas ir jāizvieto vienā no tālāk minētajām Azure ģeogrāfiskām vietām:</span><span class="sxs-lookup"><span data-stu-id="0c97d-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="0c97d-109">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="0c97d-109">East US</span></span>
    - <span data-ttu-id="0c97d-110">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="0c97d-110">West US</span></span>
    - <span data-ttu-id="0c97d-111">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="0c97d-111">North EU</span></span>
    - <span data-ttu-id="0c97d-112">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="0c97d-112">West EU</span></span>

- <span data-ttu-id="0c97d-113">Jums ir jābūt piekļuvei jūsu Dynamics 365 Regulatory Configuration Services (RCS) kontam.</span><span class="sxs-lookup"><span data-stu-id="0c97d-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="0c97d-114">Jums jāaktivizē Globalizācijas līdzeklis jūsu RCS kontā Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="0c97d-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="0c97d-115">Papildinformāciju skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="0c97d-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="0c97d-116">Jums jāizveido galvenā glabātuve un krātuves kontu risinājumā Azure.</span><span class="sxs-lookup"><span data-stu-id="0c97d-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="0c97d-117">Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="0c97d-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="0c97d-118">Instalējiet programmu Microservices pievienojumprogrammu pakalpojumam Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0c97d-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="0c97d-119">Piesakieties savā LCS kontā.</span><span class="sxs-lookup"><span data-stu-id="0c97d-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="0c97d-120">Atlasiet **Priekšskatījuma līdzekļu pārvaldības** elementu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="0c97d-121">Sadaļā **Publiskā priekšskatījuma līdzekļi** atlasiet **e-rēķinu izrakstīšanas pakalpojumu**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="0c97d-122">Pārliecinieties, vai opcija **Priekšskatījuma līdzeklis iespējots** ir iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="0c97d-123">Iestatiet RCS integrācijas parametrus ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="0c97d-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="0c97d-124">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="0c97d-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0c97d-125">Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="0c97d-126">Cilnē **e-rēķinu pakalpojums** laukā **Pakalpojuma galapunkta URI** ievadiet atbilstoši azure ģeogrāfijas pakalpojuma galapunktu, kā norādīts tālāk sniegtajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="0c97d-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="0c97d-127">Datacenter Azure ģeogrāfija</span><span class="sxs-lookup"><span data-stu-id="0c97d-127">Datacenter Azure geography</span></span> | <span data-ttu-id="0c97d-128">Pakalpojuma galapunkta URI</span><span class="sxs-lookup"><span data-stu-id="0c97d-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="0c97d-129">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="0c97d-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c97d-130">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="0c97d-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c97d-131">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="0c97d-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c97d-132">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="0c97d-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="0c97d-133">Pārbaudiet, vai **Lietojumprogrammas Id** lauks ir iestatīts uz **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="0c97d-134">Šī vērtība ir fiksēta vērtība.</span><span class="sxs-lookup"><span data-stu-id="0c97d-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="0c97d-135">Laukā **LCS vides Id** ievadiet jūsu LCS abonementa konta ID.</span><span class="sxs-lookup"><span data-stu-id="0c97d-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="0c97d-136">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="0c97d-137">Izveidojiet Galvenās glabātavas noslēpumu</span><span class="sxs-lookup"><span data-stu-id="0c97d-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="0c97d-138">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="0c97d-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0c97d-139">Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **e-rēķinu izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="0c97d-140">Lapā **Vides iestatījumi** darbības rūtī atlasiet **Pakalpojuma vide** un atlasiet **Atslēgas glabātuves parametri**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="0c97d-141">Atlasiet **Jauns**, lai izveidotu atslēgas glabātuves noslēpumu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="0c97d-142">Laukā **Nosaukums** ievadiet atslēgas glabātuves noslēpuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="0c97d-143">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="0c97d-144">Laukā **Atslēgas glabātuves URI** ielīmējiet noslēpumu no Azure atslēgas glabātuves.</span><span class="sxs-lookup"><span data-stu-id="0c97d-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="0c97d-145">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="0c97d-146">Izveidojiet krātuves noslēpumu</span><span class="sxs-lookup"><span data-stu-id="0c97d-146">Create Storage account secret</span></span>

1. <span data-ttu-id="0c97d-147">Lapā **Atslēgas glabātuves parametri** sadaļā **Sertifikāti** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="0c97d-148">Laukā **Nosaukums** ievadiet to pašu glabātuves konta noslēpumu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="0c97d-149">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="0c97d-150">Laukā **Tips** atlasiet **Sertifikāts**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="0c97d-151">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="0c97d-152">Izveidot elektronisko rēķinu izrakstīšanas pievienojumprogrammas vidi</span><span class="sxs-lookup"><span data-stu-id="0c97d-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="0c97d-153">Piesakieties savā RCS kontā.</span><span class="sxs-lookup"><span data-stu-id="0c97d-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="0c97d-154">Darbvietā **Globalizācijas līdzeklis** sadaļā **Vide** atlasiet elementu **e-rēķinu izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="0c97d-155">Pakalpojumu vides izveide</span><span class="sxs-lookup"><span data-stu-id="0c97d-155">Create a service environment</span></span>

1. <span data-ttu-id="0c97d-156">Lapā **Vides iestatījumi** darbību rūtī atlasiet **Pakalpojuma vide**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="0c97d-157">Atlasiet **Jauns**, lai izveidotu jaunu pakalpojuma vidi.</span><span class="sxs-lookup"><span data-stu-id="0c97d-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="0c97d-158">Laukā **Nosaukums** ievadiet e-rēķinu izrakstīšanas vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="0c97d-159">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="0c97d-160">Laukā **Krātuves SAS marķiera noslēpums** atlasiet tā sertifikāta nosaukumu, kas jāizmanto, lai autentificētu piekļuvi krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="0c97d-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="0c97d-161">Sadaļā **Lietotāji** atlasiet **Pievienot**, lai pievienotu lietotāju, kuram ir atļauts iesniegt elektroniskos rēķinus, izmantojot vidi, un arī pievienojieties krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="0c97d-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="0c97d-162">Laukā **Lietotāja ID** ievadiet lietotāja aizstājvārdu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="0c97d-163">Laukā **E-pasta adrese** ievadiet lietotāja e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="0c97d-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="0c97d-164">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-164">Select **Save**.</span></span>
8. <span data-ttu-id="0c97d-165">Ja jūsu valstij/reģionam raksturīgiem rēķiniem ir nepieciešama sertifikātu ķēde, lai pielietotu elektroniskos parakstus, Darbības rūtī atlasiet **Atslēgas glabātuves parametrus** pēc tam atlasiet **Sertifikātu ķēde** un sekojiet šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="0c97d-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="0c97d-166">Atlasiet **Jauns**, lai izveidotu sertifikātu ķēdi.</span><span class="sxs-lookup"><span data-stu-id="0c97d-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="0c97d-167">Laukā **Nosaukums** ievadiet sertifikātu ķēdes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="0c97d-168">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="0c97d-169">Sadaļā **Sertifikāti** atlasiet **Pievienot**, lai pievienotu ķēdei sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="0c97d-170">Izmantojiet pogu **Augšā** vai **Lejā**, lai mainītu sertifikāta pozīciju ķēdē.</span><span class="sxs-lookup"><span data-stu-id="0c97d-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="0c97d-171">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="0c97d-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-172">Close the page.</span></span>
9. <span data-ttu-id="0c97d-173">Darbības rūtī lapā **Pakalpojuma vide** atlasiet **Publicēt**, lai publicētu vidi mākonī.</span><span class="sxs-lookup"><span data-stu-id="0c97d-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="0c97d-174">Lauka **Statuss** vērtība mainīta uz **Publicēts**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="0c97d-175">Izveidojiet pievienotu pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="0c97d-175">Create a connected application</span></span>

1. <span data-ttu-id="0c97d-176">Lapā **Vides iestatījumi** darbību rūtī atlasiet **Savienotās lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="0c97d-177">Atlasiet **Jauns**, lai izveidotu savienotu lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="0c97d-178">Laukā **Nosaukums** ievadiet savienotās lietojumprogrammas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="0c97d-179">Laukā **Lietojumprogramma** ievadiet Finance un Supply Chain Management vides URL, ar kuru veidot savienojumu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="0c97d-180">Laukā **Īrnieks** ievadiet Finance un Supply Chain Management vides īrnieku.</span><span class="sxs-lookup"><span data-stu-id="0c97d-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="0c97d-181">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-181">Select **Save**.</span></span>
6. <span data-ttu-id="0c97d-182">Darbību rūtī atlasiet **Pārbaudīt savienojumu**, lai pārbaudītu savienojumu ar vidi.</span><span class="sxs-lookup"><span data-stu-id="0c97d-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="0c97d-183">Tad aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="0c97d-184">Saistīt savienotās programmas ar vidēm</span><span class="sxs-lookup"><span data-stu-id="0c97d-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="0c97d-185">Lai videi piešķirtu pievienoto programmu **Vides iestatījumu** lapā atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="0c97d-186">Laukā **Savienotā programma** atlasiet savienoto lietojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="0c97d-187">Laukā **Pakalpojuma vide** atlasiet darba pasūtījuma pakalpojuma vidi.</span><span class="sxs-lookup"><span data-stu-id="0c97d-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="0c97d-188">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="0c97d-189">Iestatīt elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšanu Finance un Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0c97d-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="0c97d-190">Iesledziet elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrācijas līdzekli</span><span class="sxs-lookup"><span data-stu-id="0c97d-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="0c97d-191">Pierakstieties jūsu Finance vai Supply Chain Management instancē.</span><span class="sxs-lookup"><span data-stu-id="0c97d-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="0c97d-192">Darbvietā **Līdzekļu pārvaldība** meklējiet līdzekli **Konfigurējamā elektronisko rēķinu pievienošanas integrācija**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="0c97d-193">Ja šis līdzeklis lapā nav redzams, atlasiet **Pārbaudīt, vai nav atjauninājumu**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="0c97d-194">Atlasiet līdzekli un pēc tam atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="0c97d-195">Pakalpojuma galapunkta URL iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0c97d-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="0c97d-196">Dodieties uz **Organizācijas administrēšana \> Iestatījumi \> Elektronisko dokumentu parametri**.</span><span class="sxs-lookup"><span data-stu-id="0c97d-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="0c97d-197">Cilnē **Iesniegšanas pakalpojums** laukā **Pakalpojuma galapunkta URL** ievadiet atbilstoši azure ģeogrāfijas pakalpojuma galapunktu, kā norādīts tālāk sniegtajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="0c97d-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="0c97d-198">Datacenter Azure ģeogrāfija</span><span class="sxs-lookup"><span data-stu-id="0c97d-198">Datacenter Azure geography</span></span> | <span data-ttu-id="0c97d-199">Pakalpojuma galapunkta URL</span><span class="sxs-lookup"><span data-stu-id="0c97d-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="0c97d-200">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="0c97d-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c97d-201">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="0c97d-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c97d-202">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="0c97d-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="0c97d-203">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="0c97d-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="0c97d-204">Laukā **Vide** ievadiet elektronisko rēķinu izrakstīšanas pievienojuma vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="0c97d-205">Atlasiet **Saglabāt** un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="0c97d-205">Select **Save**, and then close the page.</span></span>
