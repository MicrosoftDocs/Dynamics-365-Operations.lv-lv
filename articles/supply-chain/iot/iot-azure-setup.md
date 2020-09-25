---
title: Azure resursu iestatīšana IoT informācijai
description: Šajā tēmā ir paskaidrots, kā izveidot un konfigurēt Microsoft Azure resursus, kas nepieciešami IoT informācijai.
author: ''
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ea1083a65efb25699b9237c72c081f50e1fb476c
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802777"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="bccf0-103">Azure resursu iestatīšana IoT informācijai</span><span class="sxs-lookup"><span data-stu-id="bccf0-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bccf0-104">Šajā tēmā ir paskaidrots, kā izveidot un konfigurēt Microsoft Azure resursus, kas nepieciešami IoT informācijai.</span><span class="sxs-lookup"><span data-stu-id="bccf0-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="bccf0-105">Azure resursu izveidošana</span><span class="sxs-lookup"><span data-stu-id="bccf0-105">Create Azure resources</span></span>

<span data-ttu-id="bccf0-106">Veiciet šīs darbības, lai izveidotu IoT centrmezglu, Redis kešatmiņu un atslēgu akreditācijas datu komplektu, kam var piekļūt korporācija Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bccf0-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="bccf0-107">Pārbaudīt, vai Microsoft Dynamics ERP apakšpakalpojumu pirmās puses programmas ID ir jūsu nomniekā</span><span class="sxs-lookup"><span data-stu-id="bccf0-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="bccf0-108">Lai pārbaudītu, vai programmas ID Microsoft Dynamics ERP apakšpakalpojuma pirmās puses programmai ir jūsu nomniekā, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="bccf0-109">Pierakstieties Azure portālā vietnē <https://portal.azure.com>.</span><span class="sxs-lookup"><span data-stu-id="bccf0-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="bccf0-110">Dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="bccf0-111">Dodieties uz **Uzņēmuma lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="bccf0-112">Laukā **Lietojumprogrammas veids** atlasiet **Microsoft lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="bccf0-113">Meklēšanas laukā ievadiet **Microsoft Dynamics ERP apakšpakalpojumi**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="bccf0-114">Pārbaudiet, vai **Microsoft Dynamics ERP apakšpakalpojumi** ir sarakstā.</span><span class="sxs-lookup"><span data-stu-id="bccf0-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="bccf0-115">Citām lietojumprogrammām ir līdzīgi nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-115">Other applications have similar names.</span></span> <span data-ttu-id="bccf0-116">Tāpēc pārliecinieties, vai tiek atrastas pareizās lietojumprogrammas.</span><span class="sxs-lookup"><span data-stu-id="bccf0-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="bccf0-117">Programmas ID ir **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="bccf0-118">Ja lietojumprogramma nav sarakstā, tā ir jāpievieno nomniekam:</span><span class="sxs-lookup"><span data-stu-id="bccf0-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="bccf0-119">Azure portāla rīkjoslā atlasiet pogu, lai atvērtu Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="bccf0-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="bccf0-120">Izpildiet komandu **Install-Module AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="bccf0-121">Ievadiet **Y**, lai instalētu moduli.</span><span class="sxs-lookup"><span data-stu-id="bccf0-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="bccf0-122">Izpildiet komandu **Get-InstalledModule -Name "AzureAD"**, lai pārbaudītu, vai modulis ir instalēts.</span><span class="sxs-lookup"><span data-stu-id="bccf0-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="bccf0-123">Izpildiet komandu **Connect-AzureAD -Confirm**, lai palaistu autentifikāciju.</span><span class="sxs-lookup"><span data-stu-id="bccf0-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="bccf0-124">Izpildiet komandu **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="bccf0-125">Tagad varat atkārtot 1. līdz 6. darbību, lai pārbaudītu, vai programmas ID ir jūsu nomniekā.</span><span class="sxs-lookup"><span data-stu-id="bccf0-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="bccf0-126">Atslēgas akreditācijas datu komplekta resursa veidošana</span><span class="sxs-lookup"><span data-stu-id="bccf0-126">Create a key vault resource</span></span>

<span data-ttu-id="bccf0-127">Lai izveidotu atslēgas akreditācijas datu komplekta resursu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="bccf0-128">Azure portālā izveidojiet vai dodieties uz resursu grupu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="bccf0-129">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-129">Select **Add**.</span></span>
3. <span data-ttu-id="bccf0-130">Lapā **Jauns** meklēšanas laukā ievadiet **Atslēgas akreditācijas datu komplekts**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="bccf0-131">Pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-131">Then select **Create**.</span></span>
4. <span data-ttu-id="bccf0-132">Lapas **Atslēgas akreditācijas datu komplekta izveide**, laukā **Atslēgas akreditācijas datu komplekta nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="bccf0-133">Pārskatiet noklusējuma vērtības un pēc tam atlasiet **Pārskatīt + izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="bccf0-134">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-134">Select **Create**.</span></span>

<span data-ttu-id="bccf0-135">Atslēgas akreditācijas datu komplekts tiek veidots fonā.</span><span class="sxs-lookup"><span data-stu-id="bccf0-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="bccf0-136">IoT centrmezgla resursa izveidošana</span><span class="sxs-lookup"><span data-stu-id="bccf0-136">Create an IoT hub resource</span></span>

<span data-ttu-id="bccf0-137">Lai izveidotu IoT centrmezgla resursu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="bccf0-138">Izveidojiet vai dodieties uz resursu grupu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="bccf0-139">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-139">Select **Add**.</span></span>
3. <span data-ttu-id="bccf0-140">Lapā **Jauns** meklēšanas laukā ievadiet **IoT centrmezgls**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="bccf0-141">Pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-141">Then select **Create**.</span></span>
4. <span data-ttu-id="bccf0-142">Laukā **IoT centrmezgla nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="bccf0-143">Pārskatiet noklusējuma vērtības un pēc tam atlasiet **Pārskatīt + izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="bccf0-144">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-144">Select **Create**.</span></span>

<span data-ttu-id="bccf0-145">IoT centrmezgls tiek veidots fonā.</span><span class="sxs-lookup"><span data-stu-id="bccf0-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="bccf0-146">Ieteicams izveidot tikai vienu IoT centrmezgla resursu katrai videi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="bccf0-147">Redis kešatmiņas resursa izveidošana</span><span class="sxs-lookup"><span data-stu-id="bccf0-147">Create a Redis cache resource</span></span>

<span data-ttu-id="bccf0-148">Lai izveidotu Redis kešatmiņas resursu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="bccf0-149">Izveidojiet vai dodieties uz resursu grupu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="bccf0-150">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-150">Select **Add**.</span></span>
3. <span data-ttu-id="bccf0-151">Lapā **Jauns** meklēšanas laukā ievadiet **Azure kešatmiņa Redis**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="bccf0-152">Pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-152">Then select **Create**.</span></span>
4. <span data-ttu-id="bccf0-153">Laukā **DNS nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="bccf0-154">Pārskatiet noklusējuma vērtības un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="bccf0-155">Redis kešatmiņa tiek veidota fonā.</span><span class="sxs-lookup"><span data-stu-id="bccf0-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="bccf0-156">Ieteicams izveidot tikai vienu Redis kešatmiņu katrai videi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="bccf0-157">Visi resursi tagad ir izveidoti.</span><span class="sxs-lookup"><span data-stu-id="bccf0-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="bccf0-158">Azure resursu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="bccf0-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="bccf0-159">IoT centrmezgla konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="bccf0-159">Configure the IoT hub</span></span>

<span data-ttu-id="bccf0-160">Lai konfigurētu IoT centrmezglu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="bccf0-161">Savos resursos atlasiet IoT centrmezgla resursu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="bccf0-162">Kreisās puses navigācijas rūtī atlasiet **Iebūvētie galapunkti**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="bccf0-163">Sadaļā **Patērētāju grupas** ielīmējiet šādas patērētāju grupas.</span><span class="sxs-lookup"><span data-stu-id="bccf0-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="bccf0-164">Šīs patērētāju grupas atbilst standarta komplektācijā iekļautajiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="bccf0-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="bccf0-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="bccf0-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="bccf0-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="bccf0-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="bccf0-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="bccf0-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="bccf0-168">Atslēgas akreditācijas datu komplekta konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="bccf0-168">Configure the key vault</span></span>

<span data-ttu-id="bccf0-169">Lai konfigurētu atslēgas akreditācijas datu komplektu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="bccf0-170">Savos resursos atlasiet atslēgas akreditācijas datu komplekta resursu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="bccf0-171">Kreisās puses navigācijas rūtī atlasiet **Piekļuves politikas**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="bccf0-172">Atlasiet **Pievienot piekļuves politiku**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="bccf0-173">Lapas **Pievienot piekļuves politiku** laukā **Slepenās atļaujas** atlasiet **Iegūt** un **Saraksts**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="bccf0-174">Noklikšķiniet uz **Atlasīt vadītāju**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="bccf0-175">Dialoglodziņā **Vadītājs** meklējiet un atlasiet **Microsoft Dynamics ERP apakšpakalpojumi**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="bccf0-176">Pēc tam atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-176">Then select **Select**.</span></span>
7. <span data-ttu-id="bccf0-177">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-177">Select **Add**.</span></span>
8. <span data-ttu-id="bccf0-178">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-178">Select **Save**.</span></span>

<span data-ttu-id="bccf0-179">Programmai tagad ir piekļuve atslēgas akreditācijas datu komplekta noslēpumiem.</span><span class="sxs-lookup"><span data-stu-id="bccf0-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="bccf0-180">Saglabāt IoT centrmezgla savienojuma virknes noslēpumu</span><span class="sxs-lookup"><span data-stu-id="bccf0-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="bccf0-181">Lai saglabātu IoT centrmezgla savienojuma virknes noslēpumu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="bccf0-182">Savos resursos atlasiet IoT centrmezgla resursu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="bccf0-183">Kreisās puses navigācijas rūtī atlasiet **Iebūvētie galapunkti**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="bccf0-184">Kopējiet lauka **Event Hub-saderīgs galapunkts** vērtību.</span><span class="sxs-lookup"><span data-stu-id="bccf0-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="bccf0-185">Dodieties uz atslēgas akreditācijas datu komplekta resursu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="bccf0-186">Kreisās puses navigācijas rūtī atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="bccf0-187">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="bccf0-188">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="bccf0-189">Laukā **Vērtība** ielīmējiet iepriekš nokopēto galapunkta vērtību.</span><span class="sxs-lookup"><span data-stu-id="bccf0-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="bccf0-190">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="bccf0-191">Saglabāt Redis kešatmiņas savienojuma virknes noslēpumu</span><span class="sxs-lookup"><span data-stu-id="bccf0-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="bccf0-192">Lai saglabātu Redis kešatmiņas savienojuma virknes noslēpumu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="bccf0-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="bccf0-193">Savos resursos atlasiet Redis kešatmiņas resursu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="bccf0-194">Atlasiet **Piekļuves atslēgas**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="bccf0-195">Kopējiet vērtību **Primārā savienojuma virkne** laukā.</span><span class="sxs-lookup"><span data-stu-id="bccf0-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="bccf0-196">Dodieties uz atslēgas akreditācijas datu komplekta resursu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="bccf0-197">Kreisās puses navigācijas rūtī atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="bccf0-198">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="bccf0-199">Laukā **Nosaukums** ievadiet nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="bccf0-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="bccf0-200">Laukā **Vērtība** ielīmējiet iepriekš nokopēto savienojuma virkni.</span><span class="sxs-lookup"><span data-stu-id="bccf0-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="bccf0-201">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="bccf0-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="bccf0-202">Atjauninot vienu no savienojuma virknēm, ir jāatjaunina arī slepenās vērtības.</span><span class="sxs-lookup"><span data-stu-id="bccf0-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="bccf0-203">Tagad ir pabeigta nepieciešamo Azure resursu nodrošināšana.</span><span class="sxs-lookup"><span data-stu-id="bccf0-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="bccf0-204">Nākamā darbība ir [instalēt IoT informācijas pievienojumprogrammu Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="bccf0-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>
