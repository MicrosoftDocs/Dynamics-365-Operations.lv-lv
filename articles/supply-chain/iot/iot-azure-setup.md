---
title: Azure resursu iestatīšana IoT informācijai
description: Šajā tēmā ir paskaidrots, kā izveidot un konfigurēt Microsoft Azure resursus, kas nepieciešami IoT informācijai.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 33c28f8e7982c6ec9b892e975525de69fc637892
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881376"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="a8b9a-103">Azure resursu iestatīšana IoT informācijai</span><span class="sxs-lookup"><span data-stu-id="a8b9a-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8b9a-104">Šajā tēmā ir paskaidrots, kā izveidot un konfigurēt Microsoft Azure resursus, kas nepieciešami IoT informācijai.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="a8b9a-105">Azure resursu izveidošana</span><span class="sxs-lookup"><span data-stu-id="a8b9a-105">Create Azure resources</span></span>

<span data-ttu-id="a8b9a-106">Veiciet šīs darbības, lai izveidotu IoT centrmezglu, Redis kešatmiņu un atslēgu akreditācijas datu komplektu, kam var piekļūt korporācija Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="a8b9a-107">Pārbaudīt, vai Microsoft Dynamics ERP apakšpakalpojumu pirmās puses programmas ID ir jūsu nomniekā</span><span class="sxs-lookup"><span data-stu-id="a8b9a-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="a8b9a-108">Lai pārbaudītu, vai programmas ID Microsoft Dynamics ERP apakšpakalpojuma pirmās puses programmai ir jūsu nomniekā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="a8b9a-109">Pierakstieties Azure portālā vietnē <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="a8b9a-110">Dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="a8b9a-111">Dodieties uz **Uzņēmuma lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="a8b9a-112">Laukā **Lietojumprogrammas veids** atlasiet **Microsoft lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="a8b9a-113">Meklēšanas laukā ievadiet **Microsoft Dynamics ERP apakšpakalpojumi**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="a8b9a-114">Pārbaudiet, vai **Microsoft Dynamics ERP apakšpakalpojumi** ir sarakstā.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="a8b9a-115">Citām lietojumprogrammām ir līdzīgi nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-115">Other applications have similar names.</span></span> <span data-ttu-id="a8b9a-116">Tāpēc pārliecinieties, vai tiek atrastas pareizās lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="a8b9a-117">Programmas ID ir **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="a8b9a-118">Ja lietojumprogramma nav sarakstā, tā ir jāpievieno nomniekam:</span><span class="sxs-lookup"><span data-stu-id="a8b9a-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="a8b9a-119">Azure portāla rīkjoslā atlasiet pogu, lai atvērtu Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="a8b9a-120">Izpildiet komandu **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="a8b9a-121">Ievadiet **Y**, lai instalētu moduli.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="a8b9a-122">Izpildiet komandu **Get-InstalledModule -Name "AzureAD"**, lai pārbaudītu, vai modulis ir instalēts.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="a8b9a-123">Izpildiet komandu **Connect-AzureAD -Confirm**, lai palaistu autentifikāciju.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="a8b9a-124">Izpildiet komandu **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="a8b9a-125">Tagad varat atkārtot 1. līdz 6. darbību, lai pārbaudītu, vai programmas ID ir jūsu nomniekā.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="a8b9a-126">Atslēgas akreditācijas datu komplekta resursa veidošana</span><span class="sxs-lookup"><span data-stu-id="a8b9a-126">Create a key vault resource</span></span>

<span data-ttu-id="a8b9a-127">Lai izveidotu atslēgas akreditācijas datu komplekta resursu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="a8b9a-128">Azure portālā izveidojiet vai dodieties uz resursu grupu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="a8b9a-129">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-129">Select **Add**.</span></span>
3. <span data-ttu-id="a8b9a-130">Lapā **Jauns** meklēšanas laukā ievadiet **Atslēgas akreditācijas datu komplekts**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="a8b9a-131">Pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-131">Then select **Create**.</span></span>
4. <span data-ttu-id="a8b9a-132">Lapas **Atslēgas akreditācijas datu komplekta izveide**, laukā **Atslēgas akreditācijas datu komplekta nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="a8b9a-133">Pārskatiet noklusējuma vērtības un pēc tam atlasiet **Pārskatīt + izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="a8b9a-134">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-134">Select **Create**.</span></span>

<span data-ttu-id="a8b9a-135">Atslēgas akreditācijas datu komplekts tiek veidots fonā.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="a8b9a-136">IoT centrmezgla resursa izveidošana</span><span class="sxs-lookup"><span data-stu-id="a8b9a-136">Create an IoT hub resource</span></span>

<span data-ttu-id="a8b9a-137">Lai izveidotu IoT centrmezgla resursu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="a8b9a-138">Izveidojiet vai dodieties uz resursu grupu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="a8b9a-139">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-139">Select **Add**.</span></span>
3. <span data-ttu-id="a8b9a-140">Lapā **Jauns** meklēšanas laukā ievadiet **IoT centrmezgls**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="a8b9a-141">Pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-141">Then select **Create**.</span></span>
4. <span data-ttu-id="a8b9a-142">Laukā **IoT centrmezgla nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="a8b9a-143">Pārskatiet noklusējuma vērtības un pēc tam atlasiet **Pārskatīt + izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="a8b9a-144">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-144">Select **Create**.</span></span>

<span data-ttu-id="a8b9a-145">IoT centrmezgls tiek veidots fonā.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="a8b9a-146">Ieteicams izveidot tikai vienu IoT centrmezgla resursu katrai videi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="a8b9a-147">Redis kešatmiņas resursa izveidošana</span><span class="sxs-lookup"><span data-stu-id="a8b9a-147">Create a Redis cache resource</span></span>

<span data-ttu-id="a8b9a-148">Lai izveidotu Redis kešatmiņas resursu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="a8b9a-149">Izveidojiet vai dodieties uz resursu grupu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="a8b9a-150">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-150">Select **Add**.</span></span>
3. <span data-ttu-id="a8b9a-151">Lapā **Jauns** meklēšanas laukā ievadiet **Azure kešatmiņa Redis**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="a8b9a-152">Pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-152">Then select **Create**.</span></span>
4. <span data-ttu-id="a8b9a-153">Laukā **DNS nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="a8b9a-154">Pārskatiet noklusējuma vērtības un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="a8b9a-155">Redis kešatmiņa tiek veidota fonā.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="a8b9a-156">Ieteicams izveidot tikai vienu Redis kešatmiņu katrai videi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="a8b9a-157">Visi resursi tagad ir izveidoti.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="a8b9a-158">Azure resursu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a8b9a-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="a8b9a-159">IoT centrmezgla konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a8b9a-159">Configure the IoT hub</span></span>

<span data-ttu-id="a8b9a-160">Lai konfigurētu IoT centrmezglu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="a8b9a-161">Savos resursos atlasiet IoT centrmezgla resursu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="a8b9a-162">Kreisās puses navigācijas rūtī atlasiet **Iebūvētie galapunkti**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="a8b9a-163">Sadaļā **Patērētāju grupas** ielīmējiet šādas patērētāju grupas.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="a8b9a-164">Šīs patērētāju grupas atbilst standarta komplektācijā iekļautajiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="a8b9a-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="a8b9a-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="a8b9a-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="a8b9a-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="a8b9a-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="a8b9a-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="a8b9a-168">Atslēgas akreditācijas datu komplekta konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a8b9a-168">Configure the key vault</span></span>

<span data-ttu-id="a8b9a-169">Lai konfigurētu atslēgas akreditācijas datu komplektu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="a8b9a-170">Savos resursos atlasiet atslēgas akreditācijas datu komplekta resursu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="a8b9a-171">Kreisās puses navigācijas rūtī atlasiet **Piekļuves politikas**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="a8b9a-172">Atlasiet **Pievienot piekļuves politiku**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="a8b9a-173">Lapas **Pievienot piekļuves politiku** laukā **Slepenās atļaujas** atlasiet **Iegūt** un **Saraksts**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="a8b9a-174">Noklikšķiniet uz **Atlasīt vadītāju**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="a8b9a-175">Dialoglodziņā **Vadītājs** meklējiet un atlasiet **Microsoft Dynamics ERP apakšpakalpojumi**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="a8b9a-176">Pēc tam atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-176">Then select **Select**.</span></span>
7. <span data-ttu-id="a8b9a-177">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-177">Select **Add**.</span></span>
8. <span data-ttu-id="a8b9a-178">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-178">Select **Save**.</span></span>

<span data-ttu-id="a8b9a-179">Programmai tagad ir piekļuve atslēgas akreditācijas datu komplekta noslēpumiem.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="a8b9a-180">Saglabāt IoT centrmezgla savienojuma virknes noslēpumu</span><span class="sxs-lookup"><span data-stu-id="a8b9a-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="a8b9a-181">Lai saglabātu IoT centrmezgla savienojuma virknes noslēpumu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="a8b9a-182">Savos resursos atlasiet IoT centrmezgla resursu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="a8b9a-183">Kreisās puses navigācijas rūtī atlasiet **Iebūvētie galapunkti**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="a8b9a-184">Kopējiet lauka **Event Hub-saderīgs galapunkts** vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="a8b9a-185">Dodieties uz atslēgas akreditācijas datu komplekta resursu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="a8b9a-186">Kreisās puses navigācijas rūtī atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="a8b9a-187">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="a8b9a-188">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="a8b9a-189">Laukā **Vērtība** ielīmējiet iepriekš nokopēto galapunkta vērtību.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="a8b9a-190">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="a8b9a-191">Saglabāt Redis kešatmiņas savienojuma virknes noslēpumu</span><span class="sxs-lookup"><span data-stu-id="a8b9a-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="a8b9a-192">Lai saglabātu Redis kešatmiņas savienojuma virknes noslēpumu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="a8b9a-193">Savos resursos atlasiet Redis kešatmiņas resursu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="a8b9a-194">Atlasiet **Piekļuves atslēgas**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="a8b9a-195">Kopējiet vērtību **Primārā savienojuma virkne** laukā.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="a8b9a-196">Dodieties uz atslēgas akreditācijas datu komplekta resursu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="a8b9a-197">Kreisās puses navigācijas rūtī atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="a8b9a-198">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="a8b9a-199">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="a8b9a-200">Laukā **Vērtība** ielīmējiet iepriekš nokopēto savienojuma virkni.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="a8b9a-201">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="a8b9a-202">Atjauninot vienu no savienojuma virknēm, ir jāatjaunina arī slepenās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="a8b9a-203">Tagad ir pabeigta nepieciešamo Azure resursu nodrošināšana.</span><span class="sxs-lookup"><span data-stu-id="a8b9a-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="a8b9a-204">Nākamā darbība ir [instalēt IoT informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a8b9a-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
