---
title: Konfigurācija Finanšu ieskatiem (priekšskatījums)
description: Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 60e4d69157d7b73bd9e47310adae320687230080
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941230"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="e6705-103">Konfigurācija Finanšu ieskatiem (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="e6705-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e6705-104">Finanšu ieskati apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Microsoft Dataverse, Azure un AI Builder, lai nodrošinātu jaudīgus prognozēšanas rīkus jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="e6705-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="e6705-105">Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finanšu ieskatos.</span><span class="sxs-lookup"><span data-stu-id="e6705-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="e6705-106">Dynamics 365 Finance izvietošana</span><span class="sxs-lookup"><span data-stu-id="e6705-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="e6705-107">Izvietojiet vides, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e6705-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="e6705-108">Microsoft Dynamics Lifecycle Services (LCS) izveidojiet vai atjauniniet Dynamics 365 Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="e6705-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="e6705-109">Videi nepieciešama programmas versija 10.0.11/ platformas atjauninājums 35 vai jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="e6705-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="e6705-110">Videi ir jābūt augstas pieejamības (AP) videi smilškastē.</span><span class="sxs-lookup"><span data-stu-id="e6705-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="e6705-111">(Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="e6705-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="e6705-112">Ja izmantojat Contoso demonstrācijas datus, būs nepieciešami papildu parauga dati, lai izmantotu Debitora maksājumu prognozes, Skaidras naudas plūsmas prognozes un Budžeta prognožu līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="e6705-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="e6705-113">Dataverse konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e6705-113">Configure Dataverse</span></span>

<span data-ttu-id="e6705-114">Izmantojiet tālāk norādītās darbības, lai konfigurētu Dataverse programmai Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="e6705-114">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="e6705-115">Atvērt vides lapu LCS un pārbaudīt, vai sadaļa **Power Platform integrācija** jau ir instalēta.</span><span class="sxs-lookup"><span data-stu-id="e6705-115">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="e6705-116">Ja tā jau ir iestatīta, Dataverse ir jāuzskaita vides nosaukums, kas saistīts ar Dynamics 365 Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="e6705-116">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="e6705-117">Kopējiet Dataverse vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e6705-117">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="e6705-118">Ja tā nav iestatīta, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="e6705-118">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="e6705-119">Sadaļā Power Platform integrācija atlasiet pogu **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-119">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="e6705-120">Vides iestatīšana var aizņemt aptuveni stundu.</span><span class="sxs-lookup"><span data-stu-id="e6705-120">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="e6705-121">Ja Dataverse vide ir veiksmīgi iestatīta, ir jāuzskaita Dataverse vides nosaukums, kas saistīts ar Dynamics 365 Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="e6705-121">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="e6705-122">Kopējiet Dataverse vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e6705-122">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="e6705-123">Pēc vides iestatīšanas pabeigšanas **NAV** jāatlasa poga **Saite uz CDS programmām**.</span><span class="sxs-lookup"><span data-stu-id="e6705-123">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="e6705-124">Tas nav nepieciešams programmai Finance Insights un deaktivizēs iespēju izpildīt nepieciešamās vides pievienojumprogrammas LCS.</span><span class="sxs-lookup"><span data-stu-id="e6705-124">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="e6705-125">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/) un veiciet tālāk norādītās darbības, lai izveidotu jaunu Dataverse vidi tajā pašā Active Directory nomniekā.</span><span class="sxs-lookup"><span data-stu-id="e6705-125">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="e6705-126">Atveriet lapu **Vides**.</span><span class="sxs-lookup"><span data-stu-id="e6705-126">Open the **Environments** page.</span></span>

        <span data-ttu-id="e6705-127">[![Lapa Vides](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="e6705-127">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="e6705-128">Atlasiet Dataverse vidi, kas izveidota iepriekš, un pēc atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-128">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="e6705-129">Atlasiet **Resursi \> Visi mantotie iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-129">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="e6705-130">Augšējā navigācijas joslā atlasiet **Iestatījumi** un pēc tam atlasiet **Pielāgojumi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-130">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="e6705-131">Atlasiet **Izstrādātāja resursi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-131">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="e6705-132">Kopējiet **Dataverse organizācijas ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="e6705-132">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="e6705-133">Pierakstiet pārlūkprogrammas adreses joslā esošo Dataverse organizācijas URL.</span><span class="sxs-lookup"><span data-stu-id="e6705-133">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="e6705-134">Piemēram, URL varētu būt `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="e6705-134">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="e6705-135">Ja plānojat izmantot Skaidras naudas plūsmas prognožu vai Budžeta prognožu līdzekli, veiciet tālāk norādītās darbības, lai atjauninātu jūsu organizācijas anotāciju ierobežojumu līdz vismaz 50 megabaitiem (MB).</span><span class="sxs-lookup"><span data-stu-id="e6705-135">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="e6705-136">Atveriet [Power Apps portālu](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="e6705-136">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="e6705-137">Atlasiet tikko izveidoto vidi un pēc tam atlasiet **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-137">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="e6705-138">Atlasiet **Iestatījumi \> E-pasta konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="e6705-138">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="e6705-139">Mainiet lauka **Maksimālais faila izmērs** vērtību uz **51 200**.</span><span class="sxs-lookup"><span data-stu-id="e6705-139">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="e6705-140">(Šī vērtība ir izteikta kilobaitos \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="e6705-140">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="e6705-141">Atlasiet **Labi**, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="e6705-141">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="e6705-142">Azure iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e6705-142">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="e6705-143">Ievadiet Dataverse direktorijas ID un lietotāja Azure AD objekta ID</span><span class="sxs-lookup"><span data-stu-id="e6705-143">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="e6705-144">Ievadiet Dataverse direktorijas ID.</span><span class="sxs-lookup"><span data-stu-id="e6705-144">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="e6705-145">Atveriet [Azure portālu](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="e6705-145">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="e6705-146">Pierakstieties, izmantojot lietotāja ID, kas tika izmantots Dataverse vides izveidei.</span><span class="sxs-lookup"><span data-stu-id="e6705-146">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="e6705-147">Dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e6705-147">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="e6705-148">Kopējiet **Nomnieka ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="e6705-148">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="e6705-149">Ievadiet lietotāja Azure Active Directory (Azure AD) objekta ID.</span><span class="sxs-lookup"><span data-stu-id="e6705-149">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="e6705-150">[Azure portālā](https://portal.azure.com) dodieties uz **Lietotāji** un uzmeklējiet lietotāju, izmantojot e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="e6705-150">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="e6705-151">Atlasiet lietotāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="e6705-151">Select the user's name.</span></span>
    3. <span data-ttu-id="e6705-152">Kopējiet **Objekta ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="e6705-152">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="e6705-153">Izmantojiet Azure Cloud Shell, lai iestatītu Finanšu ieskatu Data Lake resursus</span><span class="sxs-lookup"><span data-stu-id="e6705-153">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="e6705-154">Windows PowerShell skripta izmantošana</span><span class="sxs-lookup"><span data-stu-id="e6705-154">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="e6705-155">Windows PowerShell skripts tiek nodrošināts, lai varētu viegli iestatīt Azure resursus, kas aprakstīti sadaļā [Eksporta konfigurēšana uz Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="e6705-155">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="e6705-156">Ja vēlaties veikt manuālu iestatīšanu, izlaidiet šo procedūru un turpiniet ar procedūru sadaļā [Manuālā iestatīšana](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="e6705-156">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="e6705-157">Izpildiet tālāk norādītās darbības, lai palaistu PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="e6705-157">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="e6705-158">Azure CLI opcija "Izmēģiniet to" vai skripta palaišana datorā, iespējams, nedarbosies.</span><span class="sxs-lookup"><span data-stu-id="e6705-158">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="e6705-159">Izpildiet tālāk norādītās darbības, lai konfigurētu Azure, izmantojot Windows PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="e6705-159">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="e6705-160">Jums ir jābūt tiesībām izveidot Azure resursu grupu, Azure resursus un Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="e6705-160">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="e6705-161">Lai iegūtu informāciju par nepieciešamajām atļaujām, skatiet [Pakalpojuma Azure AD atļauju pārbaude](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="e6705-161">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="e6705-162">[Azure portālā](https://portal.azure.com) dodieties uz savu mērķa Azure abonementu.</span><span class="sxs-lookup"><span data-stu-id="e6705-162">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="e6705-163">Atlasiet pogu **Mākoņa čaula**, kas atrodas pa labi no lauka **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="e6705-163">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="e6705-164">Atlasiet **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="e6705-164">Select **PowerShell**.</span></span>
3. <span data-ttu-id="e6705-165">Izveidojiet krātuvi, ja saņemat aicinājumu to darīt.</span><span class="sxs-lookup"><span data-stu-id="e6705-165">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="e6705-166">Dodieties uz cilni **Azure CLI** un atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="e6705-166">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="e6705-167">Atveriet Notepad un ielīmējiet PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="e6705-167">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="e6705-168">Saglabājiet failu kā ConfigureDataEzer.ps1.</span><span class="sxs-lookup"><span data-stu-id="e6705-168">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="e6705-169">Augšupielādējiet Windows PowerShell skriptu sesijā, izmantojot izvēlnes opciju augšupielādei Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="e6705-169">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="e6705-170">Palaidiet skriptu .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="e6705-170">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="e6705-171">Sekojiet uzvednēm, lai palaistu skriptu.</span><span class="sxs-lookup"><span data-stu-id="e6705-171">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="e6705-172">Izmantojiet skripta izvades informāciju, lai LCS instalētu pievienojumprogrammu **Eksportēt uz Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="e6705-172">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="e6705-173">Izmantojiet skripta izvades informāciju, lai iespējotu elementa krātuvi Finance lapā **Datu savienojumi** (**Sistēmas administrēšana \> Sistēmas parametri \> Datu savienojumi**).</span><span class="sxs-lookup"><span data-stu-id="e6705-173">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="e6705-174">Manuāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e6705-174">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="e6705-175">Pieteikumu pievienošana Azure AD nomniekam</span><span class="sxs-lookup"><span data-stu-id="e6705-175">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="e6705-176">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e6705-176">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="e6705-177">Atlasiet **Pārvaldīt \> Uzņēmuma pieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-177">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="e6705-178">Uzmeklējiet tālāk norādītos pieteikumus, izmantojot pieteikuma ID.</span><span class="sxs-lookup"><span data-stu-id="e6705-178">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="e6705-179">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="e6705-179">Application</span></span>                              | <span data-ttu-id="e6705-180">Programmas ID</span><span class="sxs-lookup"><span data-stu-id="e6705-180">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="e6705-181">Microsoft Dynamics ERP apakšpakalpojumi</span><span class="sxs-lookup"><span data-stu-id="e6705-181">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="e6705-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="e6705-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="e6705-183">Microsoft Dynamics ERP apakšpakalpojumi CDS</span><span class="sxs-lookup"><span data-stu-id="e6705-183">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="e6705-184">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="e6705-184">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="e6705-185">AI Builder autorizācijas pakalpojums</span><span class="sxs-lookup"><span data-stu-id="e6705-185">AI Builder Authorization Service</span></span>         | <span data-ttu-id="e6705-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="e6705-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="e6705-187">Ja nevarat atrast nevienu no iepriekšējiem pieteikumiem, izmēģiniet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e6705-187">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="e6705-188">Savā lokālajā datorā atlasiet izvēlni **Sākt** un uzmeklējiet **powershell**.</span><span class="sxs-lookup"><span data-stu-id="e6705-188">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="e6705-189">Atlasiet un turiet nospiestu (vai noklikšķiniet ar peles labo pogu) **Windows PowerShell** un pēc tam atlasiet **Palaist kā administratoram**.</span><span class="sxs-lookup"><span data-stu-id="e6705-189">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="e6705-190">Palaidiet tālāk norādīto komandu, lai instalētu **AzureAD** moduli.</span><span class="sxs-lookup"><span data-stu-id="e6705-190">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="e6705-191">Ja ir nepieciešams NuGet nodrošinātājs, lai turpinātu, atlasiet **Y**, lai to instalētu.</span><span class="sxs-lookup"><span data-stu-id="e6705-191">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="e6705-192">Ja parādās ziņojums "Neuzticams repozitorijs", atlasiet **Y**, lai turpinātu.</span><span class="sxs-lookup"><span data-stu-id="e6705-192">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="e6705-193">Katram pieteikumam, kas jāpievieno, palaidiet tālāk norādītās komandas, lai pievienotu pieteikumu Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e6705-193">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="e6705-194">Kad saņemat aicinājumu, pierakstieties kā Azure AD administrators.</span><span class="sxs-lookup"><span data-stu-id="e6705-194">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="e6705-195">Azure resursu izveidošana</span><span class="sxs-lookup"><span data-stu-id="e6705-195">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="e6705-196">Pārliecinieties, ka izveidojat tālāk norādītos resursus tajā pašā Azure AD instancē kā Dataverse vide.</span><span class="sxs-lookup"><span data-stu-id="e6705-196">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="e6705-197">Nav iespējams izmantot resursus no citas Azure AD instances.</span><span class="sxs-lookup"><span data-stu-id="e6705-197">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="e6705-198">Izveidojiet jaunu krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="e6705-198">Create a new storage account:</span></span>

    1. <span data-ttu-id="e6705-199">[Azure portālā](https://portal.azure.com) izveidojiet krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="e6705-199">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="e6705-200">Dialoglodziņā **Izveidot krātuves kontu** iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="e6705-200">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="e6705-201">**Atrašanās vieta** — atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="e6705-201">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="e6705-202">**Veiktspēja** — ieteicams atlasīt **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="e6705-202">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="e6705-203">**Konta veids** — jāatlasa **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="e6705-203">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="e6705-204">Dialoglodziņā **Papildu opcijas** opcijā **Data Lake Storage Gen2** atlasiet **Iespējot** līdzeklī **Hierarhiskās nosaukumvietas**.</span><span class="sxs-lookup"><span data-stu-id="e6705-204">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="e6705-205">Deaktivizējot šo līdzekli, nevarat patērēt datus, ko Finance and Operations programmas raksta, izmantojot tādus pakalpojumus kā Power BI datu plūsmas.</span><span class="sxs-lookup"><span data-stu-id="e6705-205">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="e6705-206">Atlasiet **Pārskatīt un izveidot**.</span><span class="sxs-lookup"><span data-stu-id="e6705-206">Select **Review and create**.</span></span> <span data-ttu-id="e6705-207">Kad izvietošana ir pabeigta, jaunais resurss tiks parādīts Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="e6705-207">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="e6705-208">Dodieties uz izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="e6705-208">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="e6705-209">Kreisās puses izvēlnē atlasiet **Piekļuves galvenie akreditācijas dati**.</span><span class="sxs-lookup"><span data-stu-id="e6705-209">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="e6705-210">Kopējiet un saglabājiet savienojuma virkni vai nu **Key1**, vai **Key2**.</span><span class="sxs-lookup"><span data-stu-id="e6705-210">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="e6705-211">Kopējiet un saglabājiet krātuves konta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e6705-211">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="e6705-212">Izveidojiet jaunu galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="e6705-212">Create a new key vault:</span></span>

    1. <span data-ttu-id="e6705-213">[Azure portālā](https://portal.azure.com) izveidojiet galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="e6705-213">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="e6705-214">Dialoglodziņā **Izveidot galveno akreditācijas datu glabātavu** laukā **Novietojums** atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="e6705-214">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="e6705-215">Pēc galvenās akreditācijas datu glabātavas izveides atlasiet to sarakstā un pēc tam atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-215">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="e6705-216">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="e6705-216">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="e6705-217">Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="e6705-217">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="e6705-218">Ievadiet noslēpuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e6705-218">Enter a name for the secret.</span></span> <span data-ttu-id="e6705-219">Pierakstiet nosaukumu, jo jums tas būs jānorāda vēlāk.</span><span class="sxs-lookup"><span data-stu-id="e6705-219">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="e6705-220">Laukā **Vērtība** ievadiet savienojuma virkni, ko ieguvāt no krātuves konta iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="e6705-220">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="e6705-221">Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="e6705-221">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="e6705-222">Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.</span><span class="sxs-lookup"><span data-stu-id="e6705-222">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="e6705-223">Dodieties uz **Galvenās akreditācijas datu glabātavas pārskatu** un pierakstiet DNS nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e6705-223">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="e6705-224">Izveidojiet un reģistrējiet Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="e6705-224">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="e6705-225">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory** un atlasiet **Pieteikumu reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="e6705-225">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="e6705-226">Atlasiet **Jauna pieteikuma reģistrācija** un iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="e6705-226">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="e6705-227">**Nosaukums** — ievadiet pieteikuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e6705-227">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="e6705-228">**Pieteikuma veids** — atlasiet **Web API**.</span><span class="sxs-lookup"><span data-stu-id="e6705-228">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="e6705-229">**Novirzīt URI iestatīšanu** — ievadiet savas Dynamics 365 instances URL, piemēram, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="e6705-229">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="e6705-230">Dodieties uz tikko izveidoto pieteikumu, kopējiet un saglabājiet tās **Pieteikuma (klienta) ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="e6705-230">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="e6705-231">Šī vērtība būs jānorāda vēlāk, kad iestatīsiet galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="e6705-231">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="e6705-232">Dodieties uz **API atļaujas** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e6705-232">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="e6705-233">Atlasiet **Pievienot atļauju**.</span><span class="sxs-lookup"><span data-stu-id="e6705-233">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="e6705-234">Atlasiet **Azure Galvenā akreditācijas datu glabātava**.</span><span class="sxs-lookup"><span data-stu-id="e6705-234">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="e6705-235">Pēc deleģēto atļauju atlases atlasiet **lietotājs\_personifikācija**.</span><span class="sxs-lookup"><span data-stu-id="e6705-235">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="e6705-236">Atlasiet **Pievienot atļaujas**.</span><span class="sxs-lookup"><span data-stu-id="e6705-236">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="e6705-237">Pieteikuma izvēlnē atlasiet **Sertifikāti \& noslēpumi** un pēc tam izpildiet tālāk norādītās darbības, lai izveidotu galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="e6705-237">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="e6705-238">Atlasiet **Jauns klienta noslēpums**.</span><span class="sxs-lookup"><span data-stu-id="e6705-238">Select **New client secret**.</span></span>
        2. <span data-ttu-id="e6705-239">Ievadiet nosaukumu laukā **Akreditācijas datu glabātavas apraksts**.</span><span class="sxs-lookup"><span data-stu-id="e6705-239">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="e6705-240">Atlasiet ilgumu un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e6705-240">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="e6705-241">Noslēpums tiek ģenerēts laukā **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="e6705-241">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="e6705-242">Kopējiet un saglabājiet slepeno vērtību.</span><span class="sxs-lookup"><span data-stu-id="e6705-242">Copy and save the secret value.</span></span>

4. <span data-ttu-id="e6705-243">Izveidojiet Galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="e6705-243">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="e6705-244">Dodieties uz galveno akreditācijas datu glabātavu, ko izveidojāt iepriekš, un atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-244">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="e6705-245">Katram noslēpuma nosaukumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e6705-245">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="e6705-246">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="e6705-246">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="e6705-247">Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="e6705-247">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="e6705-248">Izveidojiet noslēpuma nosaukumu un vērtību no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="e6705-248">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="e6705-249">Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="e6705-249">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="e6705-250">Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.</span><span class="sxs-lookup"><span data-stu-id="e6705-250">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="e6705-251">Slepenais nosaukums</span><span class="sxs-lookup"><span data-stu-id="e6705-251">Secret name</span></span>                       | <span data-ttu-id="e6705-252">Noslēpuma vērtība</span><span class="sxs-lookup"><span data-stu-id="e6705-252">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="e6705-253">app-id</span><span class="sxs-lookup"><span data-stu-id="e6705-253">app-id</span></span>                            | <span data-ttu-id="e6705-254">Iepriekš izveidotā pieteikuma ID</span><span class="sxs-lookup"><span data-stu-id="e6705-254">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="e6705-255">app-secret</span><span class="sxs-lookup"><span data-stu-id="e6705-255">app-secret</span></span>                        | <span data-ttu-id="e6705-256">Iepriekš saglabātais klienta noslēpums</span><span class="sxs-lookup"><span data-stu-id="e6705-256">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="e6705-257">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="e6705-257">storage-account-name</span></span>              | <span data-ttu-id="e6705-258">Iepriekš izveidotā krātuves konta nosaukums, piemēram, **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="e6705-258">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="e6705-259">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="e6705-259">storage-account-connection-string</span></span> | <span data-ttu-id="e6705-260">Savienojuma virkne, ko krātuves kontam kopējāt no lapas **Piekļuves galvenie akreditācijas dati**</span><span class="sxs-lookup"><span data-stu-id="e6705-260">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="e6705-261">Autorizējiet pieteikumu, lai piekļūtu galveno akreditācijas datu glabātavai.</span><span class="sxs-lookup"><span data-stu-id="e6705-261">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="e6705-262">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="e6705-262">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="e6705-263">Atlasiet piekļuves politikas.</span><span class="sxs-lookup"><span data-stu-id="e6705-263">Select the access policies.</span></span>
    3. <span data-ttu-id="e6705-264">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e6705-264">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="e6705-265">Atlasiet **Pievienot piekļuves politiku**, lai izveidotu piekļuves politiku.</span><span class="sxs-lookup"><span data-stu-id="e6705-265">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="e6705-266">Laukā **Noslēpuma atļaujas** atlasiet atļaujas no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="e6705-266">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="e6705-267">Laukā **Noslēpuma vadītājs** uzmeklējiet pieteikuma parādāmo nosaukumu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="e6705-267">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="e6705-268">Atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="e6705-268">Select **Select**.</span></span>
        5. <span data-ttu-id="e6705-269">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e6705-269">Select **Add**.</span></span>
        6. <span data-ttu-id="e6705-270">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e6705-270">Select **Save**.</span></span>

        | <span data-ttu-id="e6705-271">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="e6705-271">Application</span></span>                                              | <span data-ttu-id="e6705-272">Tiesības</span><span class="sxs-lookup"><span data-stu-id="e6705-272">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="e6705-273">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="e6705-273">The display name of the new application that you created</span></span> | <span data-ttu-id="e6705-274">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="e6705-274">Get, List</span></span>   |
        | <span data-ttu-id="e6705-275">**Microsoft Dynamics ERP apakšpakalpojumi**</span><span class="sxs-lookup"><span data-stu-id="e6705-275">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="e6705-276">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="e6705-276">Get, List</span></span>   |

6. <span data-ttu-id="e6705-277">Piešķiriet lomas, lai piekļūtu krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="e6705-277">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="e6705-278">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="e6705-278">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="e6705-279">Atlasiet **Piekļuves kontrole (IAM)** un pēc tam atlasiet **Lomu piešķires**.</span><span class="sxs-lookup"><span data-stu-id="e6705-279">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="e6705-280">Atlasiet **Pievienot, pievienot lomas piešķiri**.</span><span class="sxs-lookup"><span data-stu-id="e6705-280">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="e6705-281">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e6705-281">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="e6705-282">Atlasiet lomu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="e6705-282">Select the role from the following table.</span></span>
        2. <span data-ttu-id="e6705-283">Atstājiet lauku **Piešķirt piekļuvi** iestatītu uz **Azure AD lietotājs, grupa vai pakalpojuma vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="e6705-283">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="e6705-284">Laukā **Atlasīt** ievadiet pieteikumu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="e6705-284">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="e6705-285">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e6705-285">Select **Save**.</span></span>

        | <span data-ttu-id="e6705-286">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="e6705-286">Application</span></span>                                              | <span data-ttu-id="e6705-287">Loma</span><span class="sxs-lookup"><span data-stu-id="e6705-287">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="e6705-288">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="e6705-288">The display name of the new application that you created</span></span> | <span data-ttu-id="e6705-289">Īpašnieks</span><span class="sxs-lookup"><span data-stu-id="e6705-289">Owner</span></span>                       |
        | <span data-ttu-id="e6705-290">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="e6705-290">The display name of the new application that you created</span></span> | <span data-ttu-id="e6705-291">Līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="e6705-291">Contributor</span></span>                 |
        | <span data-ttu-id="e6705-292">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="e6705-292">The display name of the new application that you created</span></span> | <span data-ttu-id="e6705-293">Krātuves konta līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="e6705-293">Storage Account Contributor</span></span> |
        | <span data-ttu-id="e6705-294">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="e6705-294">The display name of the new application that you created</span></span> | <span data-ttu-id="e6705-295">Krātuves BLOB datu īpašnieks</span><span class="sxs-lookup"><span data-stu-id="e6705-295">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="e6705-296">**AI Builder autorizācijas pakalpojums**</span><span class="sxs-lookup"><span data-stu-id="e6705-296">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="e6705-297">Krātuves BLOB datu lasītājs</span><span class="sxs-lookup"><span data-stu-id="e6705-297">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="e6705-298">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="e6705-298">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="e6705-299">Data Lake konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e6705-299">Configure the data lake</span></span>

<span data-ttu-id="e6705-300">Veiciet tālāk norādītās darbības, lai izmantotu LCS, lai pievienotu videi Azure Data Lake pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="e6705-300">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="e6705-301">Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.</span><span class="sxs-lookup"><span data-stu-id="e6705-301">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="e6705-302">Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="e6705-302">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="e6705-303">Atlasiet pievienojumprogrammu **Eksportēt uz Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="e6705-303">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="e6705-304">Ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6705-304">Enter the following values.</span></span>

    | <span data-ttu-id="e6705-305">Vērtība</span><span class="sxs-lookup"><span data-stu-id="e6705-305">Value</span></span>                                                              | <span data-ttu-id="e6705-306">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e6705-306">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="e6705-307">Nomnieka ID Azure abonementam, kur atrodas Galvenās akreditācijas datu glabātava</span><span class="sxs-lookup"><span data-stu-id="e6705-307">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="e6705-308">Nomnieka ID, kur atrodas krātuves konts, pieteikumi un galvenās akreditācijas datu glabātavas.</span><span class="sxs-lookup"><span data-stu-id="e6705-308">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="e6705-309">Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**.</span><span class="sxs-lookup"><span data-stu-id="e6705-309">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="e6705-310">Norādiet sava Key Vault DNS nosaukumu</span><span class="sxs-lookup"><span data-stu-id="e6705-310">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="e6705-311">Galvenās akreditācijas datu glabātavas DNS nosaukums, piemēram, `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="e6705-311">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="e6705-312">(Šī vērtība atbilst DNS nosaukumam, kas tiek izmantots elementa krātuvē.)</span><span class="sxs-lookup"><span data-stu-id="e6705-312">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="e6705-313">Norādiet noslēpumu, kas satur krātuves konta nosaukumu</span><span class="sxs-lookup"><span data-stu-id="e6705-313">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="e6705-314">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="e6705-314">**storage-account-name**</span></span> |
    | <span data-ttu-id="e6705-315">Pieteikuma ID noslēpuma nosaukums, kas jāizmanto, lai piekļūtu Data Lake</span><span class="sxs-lookup"><span data-stu-id="e6705-315">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="e6705-316">**app-id**</span><span class="sxs-lookup"><span data-stu-id="e6705-316">**app-id**</span></span> |
    | <span data-ttu-id="e6705-317">Noslēpuma nosaukums, kas jāizmanto ar pieteikuma ID</span><span class="sxs-lookup"><span data-stu-id="e6705-317">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="e6705-318">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="e6705-318">**app-secret**</span></span> |

5. <span data-ttu-id="e6705-319">Piekrītiet nosacījumiem un atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="e6705-319">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="e6705-320">Pievienojumprogramma tiks instalēta dažu minūšu laikā.</span><span class="sxs-lookup"><span data-stu-id="e6705-320">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="e6705-321">AI Builder konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e6705-321">Configure AI Builder</span></span>

1. <span data-ttu-id="e6705-322">Pierakstieties LCS un atveriet lapu **Detalizēta informācija par vidi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-322">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="e6705-323">Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="e6705-323">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="e6705-324">Ir jābūt redzamām pievienojumprogrammām, kas jau ir instalētas šajā vidē.</span><span class="sxs-lookup"><span data-stu-id="e6705-324">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="e6705-325">Ja pievienojumprogramma **Eksportēt uz Data Lake** nav to vidū, konfigurējiet šo pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="e6705-325">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="e6705-326">Atlasiet pievienojumprogrammu **Iegūt ieskatus**.</span><span class="sxs-lookup"><span data-stu-id="e6705-326">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="e6705-327">Pievienojumprogrammas detalizētās informācijas lapā **Iegūt ieskatus** ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6705-327">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="e6705-328">Vērtība</span><span class="sxs-lookup"><span data-stu-id="e6705-328">Value</span></span>                                                    | <span data-ttu-id="e6705-329">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e6705-329">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="e6705-330">CDS organizācijas URL</span><span class="sxs-lookup"><span data-stu-id="e6705-330">CDS Organization URL</span></span>                                     | <span data-ttu-id="e6705-331">Iepriekš kopētais Dataverse organizācijas URL.</span><span class="sxs-lookup"><span data-stu-id="e6705-331">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="e6705-332">CDS org. ID</span><span class="sxs-lookup"><span data-stu-id="e6705-332">CDS Org ID</span></span>                                               | <span data-ttu-id="e6705-333">Iepriekš kopētais Dataverse organizācijas ID.</span><span class="sxs-lookup"><span data-stu-id="e6705-333">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="e6705-334">Iespējot **Vai šī ir nomnieka noklusējuma vide**.</span><span class="sxs-lookup"><span data-stu-id="e6705-334">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="e6705-335">Elementu krātuves konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e6705-335">Configure the entity store</span></span>

<span data-ttu-id="e6705-336">Izpildiet tālāk norādītās darbības, lai iestatītu Finanšu vides elementu krātuvi.</span><span class="sxs-lookup"><span data-stu-id="e6705-336">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="e6705-337">Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Sistēmas parametri \> Datu savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="e6705-337">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="e6705-338">Iestatiet tālāk norādītos galvenās akreditācijas datu glabātavas laukus.</span><span class="sxs-lookup"><span data-stu-id="e6705-338">Set the following key vault fields:</span></span>

    - <span data-ttu-id="e6705-339">**Pieteikuma (klienta) ID** — ievadiet iepriekš izveidoto pieteikuma klienta ID.</span><span class="sxs-lookup"><span data-stu-id="e6705-339">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="e6705-340">**Pieteikuma noslēpums** — ievadiet noslēpumu, ko saglabājāt iepriekš izveidotajam pieteikumam.</span><span class="sxs-lookup"><span data-stu-id="e6705-340">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="e6705-341">**DNS nosaukums** — varat atrast domēna nosaukuma sistēmas (DNS) nosaukumu iepriekš izveidotā pieteikuma detalizētas informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="e6705-341">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="e6705-342">**Noslēpuma nosaukums** — ievadiet **krātuve-konts-savienojums-virkne**.</span><span class="sxs-lookup"><span data-stu-id="e6705-342">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="e6705-343">Iespējot **Iespējot Data Lake integrāciju**.</span><span class="sxs-lookup"><span data-stu-id="e6705-343">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="e6705-344">Atlasiet **Testa Azure Key Vault** un pārbaudiet, vai nav kļūdu.</span><span class="sxs-lookup"><span data-stu-id="e6705-344">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="e6705-345">Atlasiet **Testa Azure krātuve** un pārbaudiet, vai nav kļūdu.</span><span class="sxs-lookup"><span data-stu-id="e6705-345">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="e6705-346">Atsauksmes un atbalsts</span><span class="sxs-lookup"><span data-stu-id="e6705-346">Feedback and support</span></span>

<span data-ttu-id="e6705-347">Lūdzu, sūtiet e-pastu [klientu maksājumu ieskatiem (priekšskatījums)](mailto:fiap@microsoft.com), ja vēlaties sniegt atsauksmes vai ir nepieciešams atbalsts.</span><span class="sxs-lookup"><span data-stu-id="e6705-347">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e6705-348">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="e6705-348">Privacy notice</span></span>

<span data-ttu-id="e6705-349">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="e6705-349">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
