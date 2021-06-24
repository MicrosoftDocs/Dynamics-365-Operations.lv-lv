---
title: Konfigurācija Finance Insights – versijām līdz 10.0.19
description: Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finance Insights versijām līdz 10.0.19.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186424"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="c8d74-103">Konfigurācijas Finance Insights (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="c8d74-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="c8d74-104">Tālāk norādītās procedūras Finance Insights iestatīšanai ir derīgas Microsoft Dynamics 365 Finance versijām līdz 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="c8d74-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="c8d74-105">Lai iestatītu Finance Insights versijā 10.0.20 vai jaunākā, skatiet [Finance Insights (priekšskatījuma) konfigurāciju – versijai 10.0.20 un jaunākām](configure-for-fin-insites-PubPrvw.md).</span><span class="sxs-lookup"><span data-stu-id="c8d74-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="c8d74-106">Finance Insights apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Microsoft Dataverse, Azure un AI Builder, lai nodrošinātu jaudīgus prognozēšanas rīkus jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="c8d74-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="c8d74-107">Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="c8d74-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="c8d74-108">Dynamics 365 Finance izvietošana</span><span class="sxs-lookup"><span data-stu-id="c8d74-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="c8d74-109">Izvietojiet vides, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c8d74-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="c8d74-110">Microsoft Dynamics Lifecycle Services (LCS) izveidojiet vai atjauniniet Dynamics 365 Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="c8d74-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="c8d74-111">Videi nepieciešama programmas versija 10.0.11/ platformas atjauninājums 35 vai jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="c8d74-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="c8d74-112">Videi ir jābūt augstas pieejamības (AP) videi smilškastē.</span><span class="sxs-lookup"><span data-stu-id="c8d74-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="c8d74-113">(Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="c8d74-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="c8d74-114">Konfigurējot Finance Insights, izmantojot smilškastes vidi, jums vajadzēs kopēt ražošanas datus uz šo vidi, lai varētu prognozēt darbu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="c8d74-115">Prognozēšanas modelī tiek izmantoti vairāki datu gadi, lai izveidotu prognozes.</span><span class="sxs-lookup"><span data-stu-id="c8d74-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="c8d74-116">Contoso demonstrācijas dati neietver pietiekami daudz vēsturiskos datu, lai apmācītu prognozēšanas modeli.</span><span class="sxs-lookup"><span data-stu-id="c8d74-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="c8d74-117">Dataverse konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c8d74-117">Configure Dataverse</span></span>

<span data-ttu-id="c8d74-118">Izmantojiet tālāk norādītās darbības, lai konfigurētu Dataverse programmai Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="c8d74-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="c8d74-119">Atvērt vides lapu LCS un pārbaudīt, vai sadaļa **Power Platform integrācija** jau ir instalēta.</span><span class="sxs-lookup"><span data-stu-id="c8d74-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="c8d74-120">Ja tā jau ir iestatīta, Dataverse ir jāuzskaita vides nosaukums, kas saistīts ar Dynamics 365 Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="c8d74-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="c8d74-121">Kopējiet Dataverse vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="c8d74-122">Ja tā nav iestatīta, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="c8d74-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="c8d74-123">Sadaļā Power Platform integrācija atlasiet pogu **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="c8d74-124">Vides iestatīšana var aizņemt aptuveni stundu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="c8d74-125">Ja Dataverse vide ir veiksmīgi iestatīta, ir jāuzskaita Dataverse vides nosaukums, kas saistīts ar Dynamics 365 Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="c8d74-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="c8d74-126">Kopējiet Dataverse vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="c8d74-127">Pēc vides iestatīšanas pabeigšanas **NAV** jāatlasa poga **Saite uz CDS programmām**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="c8d74-128">Tas nav nepieciešams programmai Finance Insights un deaktivizēs iespēju izpildīt nepieciešamās vides pievienojumprogrammas LCS.</span><span class="sxs-lookup"><span data-stu-id="c8d74-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="c8d74-129">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/) un veiciet tālāk norādītās darbības, lai izveidotu jaunu Dataverse vidi tajā pašā Active Directory nomniekā.</span><span class="sxs-lookup"><span data-stu-id="c8d74-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="c8d74-130">Atveriet lapu **Vides**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="c8d74-131">[![Lapa Vides](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="c8d74-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="c8d74-132">Atlasiet Dataverse vidi, kas izveidota iepriekš, un pēc atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="c8d74-133">Atlasiet **Resursi \> Visi mantotie iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="c8d74-134">Augšējā navigācijas joslā atlasiet **Iestatījumi** un pēc tam atlasiet **Pielāgojumi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="c8d74-135">Atlasiet **Izstrādātāja resursi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="c8d74-136">Kopējiet **Dataverse organizācijas ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="c8d74-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="c8d74-137">Pierakstiet pārlūkprogrammas adreses joslā esošo Dataverse organizācijas URL.</span><span class="sxs-lookup"><span data-stu-id="c8d74-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="c8d74-138">Piemēram, URL varētu būt `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="c8d74-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="c8d74-139">Ja plānojat izmantot Skaidras naudas plūsmas prognožu vai Budžeta prognožu līdzekli, veiciet tālāk norādītās darbības, lai atjauninātu jūsu organizācijas anotāciju ierobežojumu līdz vismaz 50 megabaitiem (MB).</span><span class="sxs-lookup"><span data-stu-id="c8d74-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="c8d74-140">Atveriet [Power Apps portālu](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="c8d74-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="c8d74-141">Atlasiet tikko izveidoto vidi un pēc tam atlasiet **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="c8d74-142">Atlasiet **Iestatījumi \> E-pasta konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="c8d74-143">Mainiet lauka **Maksimālais faila izmērs** vērtību uz **51 200**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="c8d74-144">(Šī vērtība ir izteikta kilobaitos \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="c8d74-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="c8d74-145">Atlasiet **Labi**, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="c8d74-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="c8d74-146">Azure iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c8d74-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="c8d74-147">Ievadiet Dataverse direktorijas ID un lietotāja Azure AD objekta ID</span><span class="sxs-lookup"><span data-stu-id="c8d74-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="c8d74-148">Ievadiet Dataverse direktorijas ID.</span><span class="sxs-lookup"><span data-stu-id="c8d74-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="c8d74-149">Atveriet [Azure portālu](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="c8d74-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="c8d74-150">Pierakstieties, izmantojot lietotāja ID, kas tika izmantots Dataverse vides izveidei.</span><span class="sxs-lookup"><span data-stu-id="c8d74-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="c8d74-151">Dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="c8d74-152">Kopējiet **Nomnieka ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="c8d74-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="c8d74-153">Ievadiet lietotāja Azure Active Directory (Azure AD) objekta ID.</span><span class="sxs-lookup"><span data-stu-id="c8d74-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="c8d74-154">[Azure portālā](https://portal.azure.com) dodieties uz **Lietotāji** un uzmeklējiet lietotāju, izmantojot e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="c8d74-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="c8d74-155">Atlasiet lietotāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-155">Select the user's name.</span></span>
    3. <span data-ttu-id="c8d74-156">Kopējiet **Objekta ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="c8d74-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="c8d74-157">Izmantojiet Azure Cloud Shell, lai iestatītu Data Lake resursus programmā Finance Insights</span><span class="sxs-lookup"><span data-stu-id="c8d74-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="c8d74-158">Windows PowerShell skripta izmantošana</span><span class="sxs-lookup"><span data-stu-id="c8d74-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="c8d74-159">Windows PowerShell skripts tiek nodrošināts, lai varētu viegli iestatīt Azure resursus, kas aprakstīti sadaļā [Eksporta konfigurēšana uz Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="c8d74-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="c8d74-160">Ja vēlaties veikt manuālu iestatīšanu, izlaidiet šo procedūru un turpiniet ar procedūru sadaļā [Manuālā iestatīšana](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="c8d74-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="c8d74-161">Izpildiet tālāk norādītās darbības, lai palaistu PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="c8d74-162">Azure CLI opcija "Izmēģiniet to" vai skripta palaišana datorā, iespējams, nedarbosies.</span><span class="sxs-lookup"><span data-stu-id="c8d74-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="c8d74-163">Izpildiet tālāk norādītās darbības, lai konfigurētu Azure, izmantojot Windows PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="c8d74-164">Jums ir jābūt tiesībām izveidot Azure resursu grupu, Azure resursus un Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="c8d74-165">Lai iegūtu informāciju par nepieciešamajām atļaujām, skatiet [Pakalpojuma Azure AD atļauju pārbaude](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="c8d74-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="c8d74-166">[Azure portālā](https://portal.azure.com) dodieties uz savu mērķa Azure abonementu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="c8d74-167">Atlasiet pogu **Mākoņa čaula**, kas atrodas pa labi no lauka **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="c8d74-168">Atlasiet **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="c8d74-169">Izveidojiet krātuvi, ja saņemat aicinājumu to darīt.</span><span class="sxs-lookup"><span data-stu-id="c8d74-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="c8d74-170">Dodieties uz cilni **Azure CLI** un atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="c8d74-171">Atveriet Notepad un ielīmējiet PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="c8d74-172">Saglabājiet failu kā ConfigureDataEzer.ps1.</span><span class="sxs-lookup"><span data-stu-id="c8d74-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="c8d74-173">Augšupielādējiet Windows PowerShell skriptu sesijā, izmantojot izvēlnes opciju augšupielādei Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="c8d74-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="c8d74-174">Palaidiet skriptu .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="c8d74-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="c8d74-175">Sekojiet uzvednēm, lai palaistu skriptu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="c8d74-176">Izmantojiet skripta izvades informāciju, lai LCS instalētu pievienojumprogrammu **Eksportēt uz Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="c8d74-177">Izmantojiet skripta izvades informāciju, lai iespējotu elementa krātuvi Finance lapā **Datu savienojumi** (**Sistēmas administrēšana \> Sistēmas parametri \> Datu savienojumi**).</span><span class="sxs-lookup"><span data-stu-id="c8d74-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="c8d74-178">Manuāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c8d74-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="c8d74-179">Pieteikumu pievienošana Azure AD nomniekam</span><span class="sxs-lookup"><span data-stu-id="c8d74-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="c8d74-180">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="c8d74-181">Atlasiet **Pārvaldīt \> Uzņēmuma pieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="c8d74-182">Uzmeklējiet tālāk norādītos pieteikumus, izmantojot pieteikuma ID.</span><span class="sxs-lookup"><span data-stu-id="c8d74-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="c8d74-183">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="c8d74-183">Application</span></span>                              | <span data-ttu-id="c8d74-184">Programmas ID</span><span class="sxs-lookup"><span data-stu-id="c8d74-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="c8d74-185">Microsoft Dynamics ERP apakšpakalpojumi</span><span class="sxs-lookup"><span data-stu-id="c8d74-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="c8d74-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="c8d74-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="c8d74-187">Microsoft Dynamics ERP apakšpakalpojumi CDS</span><span class="sxs-lookup"><span data-stu-id="c8d74-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="c8d74-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="c8d74-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="c8d74-189">AI Builder autorizācijas pakalpojums</span><span class="sxs-lookup"><span data-stu-id="c8d74-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="c8d74-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="c8d74-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="c8d74-191">Ja nevarat atrast nevienu no iepriekšējiem pieteikumiem, izmēģiniet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c8d74-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="c8d74-192">Savā lokālajā datorā atlasiet izvēlni **Sākt** un uzmeklējiet **powershell**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="c8d74-193">Atlasiet un turiet nospiestu (vai noklikšķiniet ar peles labo pogu) **Windows PowerShell** un pēc tam atlasiet **Palaist kā administratoram**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="c8d74-194">Palaidiet tālāk norādīto komandu, lai instalētu **AzureAD** moduli.</span><span class="sxs-lookup"><span data-stu-id="c8d74-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="c8d74-195">Ja ir nepieciešams NuGet nodrošinātājs, lai turpinātu, atlasiet **Y**, lai to instalētu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="c8d74-196">Ja parādās ziņojums "Neuzticams repozitorijs", atlasiet **Y**, lai turpinātu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="c8d74-197">Katram pieteikumam, kas jāpievieno, palaidiet tālāk norādītās komandas, lai pievienotu pieteikumu Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c8d74-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="c8d74-198">Kad saņemat aicinājumu, pierakstieties kā Azure AD administrators.</span><span class="sxs-lookup"><span data-stu-id="c8d74-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="c8d74-199">Azure resursu izveidošana</span><span class="sxs-lookup"><span data-stu-id="c8d74-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="c8d74-200">Pārliecinieties, ka izveidojat tālāk norādītos resursus tajā pašā Azure AD instancē kā Dataverse vide.</span><span class="sxs-lookup"><span data-stu-id="c8d74-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="c8d74-201">Nav iespējams izmantot resursus no citas Azure AD instances.</span><span class="sxs-lookup"><span data-stu-id="c8d74-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="c8d74-202">Izveidojiet jaunu krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="c8d74-203">[Azure portālā](https://portal.azure.com) izveidojiet krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="c8d74-204">Dialoglodziņā **Izveidot krātuves kontu** iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="c8d74-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="c8d74-205">**Atrašanās vieta** — atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="c8d74-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="c8d74-206">**Veiktspēja** — ieteicams atlasīt **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="c8d74-207">**Konta veids** — jāatlasa **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="c8d74-208">Dialoglodziņā **Papildu opcijas** opcijā **Data Lake Storage Gen2** atlasiet **Iespējot** līdzeklī **Hierarhiskās nosaukumvietas**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="c8d74-209">Deaktivizējot šo līdzekli, nevarat patērēt datus, ko Finance and Operations programmas raksta, izmantojot tādus pakalpojumus kā Power BI datu plūsmas.</span><span class="sxs-lookup"><span data-stu-id="c8d74-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="c8d74-210">Atlasiet **Pārskatīt un izveidot**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-210">Select **Review and create**.</span></span> <span data-ttu-id="c8d74-211">Kad izvietošana ir pabeigta, jaunais resurss tiks parādīts Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="c8d74-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="c8d74-212">Dodieties uz izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="c8d74-213">Kreisās puses izvēlnē atlasiet **Piekļuves galvenie akreditācijas dati**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="c8d74-214">Kopējiet un saglabājiet savienojuma virkni vai nu **Key1**, vai **Key2**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="c8d74-215">Kopējiet un saglabājiet krātuves konta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="c8d74-216">Izveidojiet jaunu galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="c8d74-217">[Azure portālā](https://portal.azure.com) izveidojiet galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="c8d74-218">Dialoglodziņā **Izveidot galveno akreditācijas datu glabātavu** laukā **Novietojums** atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="c8d74-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="c8d74-219">Pēc galvenās akreditācijas datu glabātavas izveides atlasiet to sarakstā un pēc tam atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="c8d74-220">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="c8d74-221">Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="c8d74-222">Ievadiet noslēpuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-222">Enter a name for the secret.</span></span> <span data-ttu-id="c8d74-223">Pierakstiet nosaukumu, jo jums tas būs jānorāda vēlāk.</span><span class="sxs-lookup"><span data-stu-id="c8d74-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="c8d74-224">Laukā **Vērtība** ievadiet savienojuma virkni, ko ieguvāt no krātuves konta iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="c8d74-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="c8d74-225">Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="c8d74-226">Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.</span><span class="sxs-lookup"><span data-stu-id="c8d74-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="c8d74-227">Dodieties uz **Galvenās akreditācijas datu glabātavas pārskatu** un pierakstiet DNS nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="c8d74-228">Izveidojiet un reģistrējiet Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="c8d74-229">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory** un atlasiet **Pieteikumu reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="c8d74-230">Atlasiet **Jauna pieteikuma reģistrācija** un iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="c8d74-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="c8d74-231">**Nosaukums** — ievadiet pieteikuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="c8d74-232">**Pieteikuma veids** — atlasiet **Web API**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="c8d74-233">**Novirzīt URI iestatīšanu** — ievadiet savas Dynamics 365 instances URL, piemēram, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="c8d74-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="c8d74-234">Dodieties uz tikko izveidoto pieteikumu, kopējiet un saglabājiet tās **Pieteikuma (klienta) ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="c8d74-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="c8d74-235">Šī vērtība būs jānorāda vēlāk, kad iestatīsiet galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="c8d74-236">Dodieties uz **API atļaujas** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c8d74-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="c8d74-237">Atlasiet **Pievienot atļauju**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="c8d74-238">Atlasiet **Azure Galvenā akreditācijas datu glabātava**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="c8d74-239">Pēc deleģēto atļauju atlases atlasiet **lietotājs\_personifikācija**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="c8d74-240">Atlasiet **Pievienot atļaujas**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="c8d74-241">Pieteikuma izvēlnē atlasiet **Sertifikāti \& noslēpumi** un pēc tam izpildiet tālāk norādītās darbības, lai izveidotu galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="c8d74-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="c8d74-242">Atlasiet **Jauns klienta noslēpums**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="c8d74-243">Ievadiet nosaukumu laukā **Akreditācijas datu glabātavas apraksts**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="c8d74-244">Atlasiet ilgumu un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="c8d74-245">Noslēpums tiek ģenerēts laukā **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="c8d74-246">Kopējiet un saglabājiet slepeno vērtību.</span><span class="sxs-lookup"><span data-stu-id="c8d74-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="c8d74-247">Izveidojiet Galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="c8d74-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="c8d74-248">Dodieties uz galveno akreditācijas datu glabātavu, ko izveidojāt iepriekš, un atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="c8d74-249">Katram noslēpuma nosaukumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c8d74-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="c8d74-250">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="c8d74-251">Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="c8d74-252">Izveidojiet noslēpuma nosaukumu un vērtību no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="c8d74-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="c8d74-253">Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="c8d74-254">Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.</span><span class="sxs-lookup"><span data-stu-id="c8d74-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="c8d74-255">Slepenais nosaukums</span><span class="sxs-lookup"><span data-stu-id="c8d74-255">Secret name</span></span>                       | <span data-ttu-id="c8d74-256">Noslēpuma vērtība</span><span class="sxs-lookup"><span data-stu-id="c8d74-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="c8d74-257">app-id</span><span class="sxs-lookup"><span data-stu-id="c8d74-257">app-id</span></span>                            | <span data-ttu-id="c8d74-258">Iepriekš izveidotā pieteikuma ID</span><span class="sxs-lookup"><span data-stu-id="c8d74-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="c8d74-259">app-secret</span><span class="sxs-lookup"><span data-stu-id="c8d74-259">app-secret</span></span>                        | <span data-ttu-id="c8d74-260">Iepriekš saglabātais klienta noslēpums</span><span class="sxs-lookup"><span data-stu-id="c8d74-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="c8d74-261">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="c8d74-261">storage-account-name</span></span>              | <span data-ttu-id="c8d74-262">Iepriekš izveidotā krātuves konta nosaukums, piemēram, **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="c8d74-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="c8d74-263">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="c8d74-263">storage-account-connection-string</span></span> | <span data-ttu-id="c8d74-264">Savienojuma virkne, ko krātuves kontam kopējāt no lapas **Piekļuves galvenie akreditācijas dati**</span><span class="sxs-lookup"><span data-stu-id="c8d74-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="c8d74-265">Autorizējiet pieteikumu, lai piekļūtu galveno akreditācijas datu glabātavai.</span><span class="sxs-lookup"><span data-stu-id="c8d74-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="c8d74-266">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="c8d74-267">Atlasiet piekļuves politikas.</span><span class="sxs-lookup"><span data-stu-id="c8d74-267">Select the access policies.</span></span>
    3. <span data-ttu-id="c8d74-268">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c8d74-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="c8d74-269">Atlasiet **Pievienot piekļuves politiku**, lai izveidotu piekļuves politiku.</span><span class="sxs-lookup"><span data-stu-id="c8d74-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="c8d74-270">Laukā **Noslēpuma atļaujas** atlasiet atļaujas no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="c8d74-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="c8d74-271">Laukā **Noslēpuma vadītājs** uzmeklējiet pieteikuma parādāmo nosaukumu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="c8d74-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="c8d74-272">Atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-272">Select **Select**.</span></span>
        5. <span data-ttu-id="c8d74-273">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-273">Select **Add**.</span></span>
        6. <span data-ttu-id="c8d74-274">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-274">Select **Save**.</span></span>

        | <span data-ttu-id="c8d74-275">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="c8d74-275">Application</span></span>                                              | <span data-ttu-id="c8d74-276">Tiesības</span><span class="sxs-lookup"><span data-stu-id="c8d74-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="c8d74-277">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="c8d74-277">The display name of the new application that you created</span></span> | <span data-ttu-id="c8d74-278">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="c8d74-278">Get, List</span></span>   |
        | <span data-ttu-id="c8d74-279">**Microsoft Dynamics ERP apakšpakalpojumi**</span><span class="sxs-lookup"><span data-stu-id="c8d74-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="c8d74-280">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="c8d74-280">Get, List</span></span>   |

6. <span data-ttu-id="c8d74-281">Piešķiriet lomas, lai piekļūtu krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="c8d74-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="c8d74-282">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="c8d74-283">Atlasiet **Piekļuves kontrole (IAM)** un pēc tam atlasiet **Lomu piešķires**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="c8d74-284">Atlasiet **Pievienot, pievienot lomas piešķiri**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="c8d74-285">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c8d74-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="c8d74-286">Atlasiet lomu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="c8d74-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="c8d74-287">Atstājiet lauku **Piešķirt piekļuvi** iestatītu uz **Azure AD lietotājs, grupa vai pakalpojuma vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="c8d74-288">Laukā **Atlasīt** ievadiet pieteikumu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="c8d74-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="c8d74-289">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-289">Select **Save**.</span></span>

        | <span data-ttu-id="c8d74-290">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="c8d74-290">Application</span></span>                                              | <span data-ttu-id="c8d74-291">Loma</span><span class="sxs-lookup"><span data-stu-id="c8d74-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="c8d74-292">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="c8d74-292">The display name of the new application that you created</span></span> | <span data-ttu-id="c8d74-293">Īpašnieks</span><span class="sxs-lookup"><span data-stu-id="c8d74-293">Owner</span></span>                       |
        | <span data-ttu-id="c8d74-294">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="c8d74-294">The display name of the new application that you created</span></span> | <span data-ttu-id="c8d74-295">Līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="c8d74-295">Contributor</span></span>                 |
        | <span data-ttu-id="c8d74-296">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="c8d74-296">The display name of the new application that you created</span></span> | <span data-ttu-id="c8d74-297">Krātuves konta līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="c8d74-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="c8d74-298">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="c8d74-298">The display name of the new application that you created</span></span> | <span data-ttu-id="c8d74-299">Krātuves BLOB datu īpašnieks</span><span class="sxs-lookup"><span data-stu-id="c8d74-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="c8d74-300">**AI Builder autorizācijas pakalpojums**</span><span class="sxs-lookup"><span data-stu-id="c8d74-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="c8d74-301">Krātuves BLOB datu lasītājs</span><span class="sxs-lookup"><span data-stu-id="c8d74-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="c8d74-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="c8d74-302">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="c8d74-303">Data Lake konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c8d74-303">Configure the data lake</span></span>

<span data-ttu-id="c8d74-304">Veiciet tālāk norādītās darbības, lai izmantotu LCS, lai pievienotu videi Azure Data Lake pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="c8d74-305">Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="c8d74-306">Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="c8d74-307">Atlasiet pievienojumprogrammu **Eksportēt uz Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="c8d74-308">Ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="c8d74-308">Enter the following values.</span></span>

    | <span data-ttu-id="c8d74-309">Vērtība</span><span class="sxs-lookup"><span data-stu-id="c8d74-309">Value</span></span>                                                              | <span data-ttu-id="c8d74-310">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c8d74-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="c8d74-311">Nomnieka ID Azure abonementam, kur atrodas Galvenās akreditācijas datu glabātava</span><span class="sxs-lookup"><span data-stu-id="c8d74-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="c8d74-312">Nomnieka ID, kur atrodas krātuves konts, pieteikumi un galvenās akreditācijas datu glabātavas.</span><span class="sxs-lookup"><span data-stu-id="c8d74-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="c8d74-313">Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="c8d74-314">Norādiet sava Key Vault DNS nosaukumu</span><span class="sxs-lookup"><span data-stu-id="c8d74-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="c8d74-315">Galvenās akreditācijas datu glabātavas DNS nosaukums, piemēram, `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="c8d74-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="c8d74-316">(Šī vērtība atbilst DNS nosaukumam, kas tiek izmantots elementa krātuvē.)</span><span class="sxs-lookup"><span data-stu-id="c8d74-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="c8d74-317">Norādiet noslēpumu, kas satur krātuves konta nosaukumu</span><span class="sxs-lookup"><span data-stu-id="c8d74-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="c8d74-318">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="c8d74-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="c8d74-319">Pieteikuma ID noslēpuma nosaukums, kas jāizmanto, lai piekļūtu Data Lake</span><span class="sxs-lookup"><span data-stu-id="c8d74-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="c8d74-320">**app-id**</span><span class="sxs-lookup"><span data-stu-id="c8d74-320">**app-id**</span></span> |
    | <span data-ttu-id="c8d74-321">Noslēpuma nosaukums, kas jāizmanto ar pieteikuma ID</span><span class="sxs-lookup"><span data-stu-id="c8d74-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="c8d74-322">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="c8d74-322">**app-secret**</span></span> |

5. <span data-ttu-id="c8d74-323">Piekrītiet nosacījumiem un atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="c8d74-324">Pievienojumprogramma tiks instalēta dažu minūšu laikā.</span><span class="sxs-lookup"><span data-stu-id="c8d74-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="c8d74-325">AI Builder konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c8d74-325">Configure AI Builder</span></span>

1. <span data-ttu-id="c8d74-326">Pierakstieties LCS un atveriet lapu **Detalizēta informācija par vidi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="c8d74-327">Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="c8d74-328">Ir jābūt redzamām pievienojumprogrammām, kas jau ir instalētas šajā vidē.</span><span class="sxs-lookup"><span data-stu-id="c8d74-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="c8d74-329">Ja pievienojumprogramma **Eksportēt uz Data Lake** nav to vidū, konfigurējiet šo pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="c8d74-330">Atlasiet pievienojumprogrammu **Iegūt ieskatus**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="c8d74-331">Pievienojumprogrammas detalizētās informācijas lapā **Iegūt ieskatus** ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="c8d74-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="c8d74-332">Vērtība</span><span class="sxs-lookup"><span data-stu-id="c8d74-332">Value</span></span>                                                    | <span data-ttu-id="c8d74-333">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c8d74-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="c8d74-334">CDS organizācijas URL</span><span class="sxs-lookup"><span data-stu-id="c8d74-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="c8d74-335">Iepriekš kopētais Dataverse organizācijas URL.</span><span class="sxs-lookup"><span data-stu-id="c8d74-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="c8d74-336">CDS org. ID</span><span class="sxs-lookup"><span data-stu-id="c8d74-336">CDS Org ID</span></span>                                               | <span data-ttu-id="c8d74-337">Iepriekš kopētais Dataverse organizācijas ID.</span><span class="sxs-lookup"><span data-stu-id="c8d74-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="c8d74-338">Iespējot **Vai šī ir nomnieka noklusējuma vide**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="c8d74-339">Elementu krātuves konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c8d74-339">Configure the entity store</span></span>

<span data-ttu-id="c8d74-340">Izpildiet tālāk norādītās darbības, lai iestatītu Finanšu vides elementu krātuvi.</span><span class="sxs-lookup"><span data-stu-id="c8d74-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="c8d74-341">Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Sistēmas parametri \> Datu savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="c8d74-342">Iestatiet tālāk norādītos galvenās akreditācijas datu glabātavas laukus.</span><span class="sxs-lookup"><span data-stu-id="c8d74-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="c8d74-343">**Pieteikuma (klienta) ID** — ievadiet iepriekš izveidoto pieteikuma klienta ID.</span><span class="sxs-lookup"><span data-stu-id="c8d74-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="c8d74-344">**Pieteikuma noslēpums** — ievadiet noslēpumu, ko saglabājāt iepriekš izveidotajam pieteikumam.</span><span class="sxs-lookup"><span data-stu-id="c8d74-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="c8d74-345">**DNS nosaukums** — varat atrast domēna nosaukuma sistēmas (DNS) nosaukumu iepriekš izveidotā pieteikuma detalizētas informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="c8d74-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="c8d74-346">**Noslēpuma nosaukums** — ievadiet **krātuve-konts-savienojums-virkne**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="c8d74-347">Iespējot **Iespējot Data Lake integrāciju**.</span><span class="sxs-lookup"><span data-stu-id="c8d74-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="c8d74-348">Atlasiet **Testa Azure Key Vault** un pārbaudiet, vai nav kļūdu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="c8d74-349">Atlasiet **Testa Azure krātuve** un pārbaudiet, vai nav kļūdu.</span><span class="sxs-lookup"><span data-stu-id="c8d74-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="c8d74-350">Atsauksmes un atbalsts</span><span class="sxs-lookup"><span data-stu-id="c8d74-350">Feedback and support</span></span>

<span data-ttu-id="c8d74-351">Lūdzu, sūtiet e-pastu [klientu maksājumu ieskatiem (priekšskatījums)](mailto:fiap@microsoft.com), ja vēlaties sniegt atsauksmes vai ir nepieciešams atbalsts.</span><span class="sxs-lookup"><span data-stu-id="c8d74-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="c8d74-352">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="c8d74-352">Privacy notice</span></span>

<span data-ttu-id="c8d74-353">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="c8d74-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
