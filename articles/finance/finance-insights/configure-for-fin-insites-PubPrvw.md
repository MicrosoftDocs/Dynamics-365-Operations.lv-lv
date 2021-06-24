---
title: Finance Insights konfigurācija publiskam priekšskatījumam (priekšskatījums) – versija 10.0.20 un jaunākas
description: Šajā tēmā ir izskaidrots, kā konfigurēt sistēmu, lai izmantotu iespējas, kas pieejamas Finance Insights publiskam priekšskatījumam versijā 10.0.20 un jaunākās.
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
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222616"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="9f922-103">Finance Insights konfigurācija publiskam priekšskatījumam (priekšskatījums) – versija 10.0.20 un jaunākas</span><span class="sxs-lookup"><span data-stu-id="9f922-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9f922-104">Finance Insights apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Dataverse, Azure un AI Builder, lai nodrošinātu jaudīgus prognozēšanas rīkus jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="9f922-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="9f922-105">Šajā tēmā ir izskaidrots, kā konfigurēt Dynamics 365 Finance versiju 10.0.20, lai sistēma varētu izmantotu iespējas, kas ir pieejamas Finance Insights publiskam priekšskatījumam.</span><span class="sxs-lookup"><span data-stu-id="9f922-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="9f922-106">Šajā tēmā aprakstītās konfigurācijas darbības attiecas tikai uz Finance versiju 10.0.20 un jaunāku.</span><span class="sxs-lookup"><span data-stu-id="9f922-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="9f922-107">'Lai iestatītu Finance Insights versijai 10.0.19 vai jaunākai, skatiet [Finance Insights konfigurācija – versijām līdz 10.0.18](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="9f922-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="9f922-108">Finance izvietošana</span><span class="sxs-lookup"><span data-stu-id="9f922-108">Deploy Finance</span></span>

<span data-ttu-id="9f922-109">Lai izvietotu vides, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9f922-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="9f922-110">Programmā Microsoft Dynamics Lifecycle Services (LCS) izveidojiet vai atjauniniet Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="9f922-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="9f922-111">Videi nepieciešama Finance and Operations programmas versija 10.0.20 vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="9f922-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="9f922-112">Videi ir jābūt augstas pieejamības (AP) videi smilškastē.</span><span class="sxs-lookup"><span data-stu-id="9f922-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="9f922-113">(Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="9f922-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="9f922-114">Konfigurējot Finance Insights, izmantojot smilškastes vidi, jums vajadzēs kopēt ražošanas datus uz šo vidi, lai varētu prognozēt darbu.</span><span class="sxs-lookup"><span data-stu-id="9f922-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="9f922-115">Prognozēšanas modelī tiek izmantoti vairāki datu gadi, lai izveidotu prognozes.</span><span class="sxs-lookup"><span data-stu-id="9f922-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="9f922-116">Contoso demonstrācijas dati neietver pietiekami daudz vēsturiskos datu, lai apmācītu prognozēšanas modeli.</span><span class="sxs-lookup"><span data-stu-id="9f922-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="9f922-117">Dataverse konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9f922-117">Configure Dataverse</span></span>

<span data-ttu-id="9f922-118">Sekojiet tālāk norādītajām darbībām, lai konfigurētu Dataverse programmai Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="9f922-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="9f922-119">Atveriet vides lapu LCS un pārbaudīt, vai sadaļa **Power Platform integrācija** jau ir instalēta.</span><span class="sxs-lookup"><span data-stu-id="9f922-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="9f922-120">Ja tā jau ir iestatīta, jāuzskaita ar Finance vidi saistītais Dataverse vides nosaukums.</span><span class="sxs-lookup"><span data-stu-id="9f922-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="9f922-121">Ja tā nav iestatīta, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="9f922-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="9f922-122">Sadaļā **Power Platform integrācija** atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="9f922-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="9f922-123">Vides iestatīšana var ilgt vienu stundu.</span><span class="sxs-lookup"><span data-stu-id="9f922-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="9f922-124">Ja Dataverse vide ir veiksmīgi iestatīta, ir jāuzskaita Dataverse vides nosaukums, kas ir saistīts ar Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="9f922-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="9f922-125">Pēc vides iestatīšanas **neatlasiet** pogu **Saite uz CDS programmām**.</span><span class="sxs-lookup"><span data-stu-id="9f922-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="9f922-126">Šī poga nav paredzēta Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="9f922-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="9f922-127">Ja to atlasīsit, nevarēsit konfigurēt nepieciešamās vides pievienojumprogrammas LCS.</span><span class="sxs-lookup"><span data-stu-id="9f922-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="9f922-128">Azure konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9f922-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="9f922-129">Izmantojiet Azure Cloud Shell, lai iestatītu Data Lake resursus programmā Finance Insights</span><span class="sxs-lookup"><span data-stu-id="9f922-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="9f922-130">Windows PowerShell skripta izmantošana</span><span class="sxs-lookup"><span data-stu-id="9f922-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="9f922-131">Windows PowerShell skripts tiek nodrošināts, lai varētu viegli iestatīt Azure resursus, kas aprakstīti sadaļā [Eksporta konfigurēšana uz Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="9f922-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="9f922-132">Ja vēlaties iestatīšanu veikt manuāli, izlaidiet šo procedūru un pabeidziet procedūru sadaļā [Manuālā iestatīšana](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="9f922-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="9f922-133">Izmantojiet šo procedūru, lai palaistu Windows PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="9f922-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="9f922-134">Iespējams, iestatījums nedarbosies, ja izmantojat opciju **Izmēģināt** to Azure CLI vai palaižat skriptu datorā.</span><span class="sxs-lookup"><span data-stu-id="9f922-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="9f922-135">Izpildiet tālāk norādītās darbības, lai konfigurējot Azure tiktu izmantots Windows PowerShell skripts.</span><span class="sxs-lookup"><span data-stu-id="9f922-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="9f922-136">Jums ir jābūt tiesībām izveidot Azure resursu grupu, Azure resursus un Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="9f922-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="9f922-137">Lai iegūtu informāciju par nepieciešamajām atļaujām, skatiet [Pakalpojuma Azure AD atļauju pārbaude](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="9f922-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="9f922-138">[Azure portālā](https://portal.azure.com) dodieties uz savu mērķa Azure abonementu.</span><span class="sxs-lookup"><span data-stu-id="9f922-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="9f922-139">Atlasiet **Cloud Shell**, kas atrodas pa labi no lauka **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="9f922-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="9f922-140">Atlasiet **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="9f922-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="9f922-141">Izveidojiet krātuvi, ja saņemat aicinājumu to darīt.</span><span class="sxs-lookup"><span data-stu-id="9f922-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="9f922-142">Cilnē **Azure CLI** atlasiet **Kopēt**.</span><span class="sxs-lookup"><span data-stu-id="9f922-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="9f922-143">Programmā Notepad atveriet jaunu failu un ielīmējiet Windows PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="9f922-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="9f922-144">Saglabājiet failu kā **ConfigureDataEzer.ps1**.</span><span class="sxs-lookup"><span data-stu-id="9f922-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="9f922-145">Augšupielādējiet Windows PowerShell skriptu sesijā, izmantojot izvēlnes opciju augšupielādei Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="9f922-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="9f922-146">Palaidiet **.\ConfigureDataLake.ps1** skriptu.</span><span class="sxs-lookup"><span data-stu-id="9f922-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="9f922-147">Sekojiet uzvednēm, lai palaistu skriptu.</span><span class="sxs-lookup"><span data-stu-id="9f922-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="9f922-148">Izmantojiet skripta izvades informāciju, lai LCS instalētu pievienojumprogrammu Eksportēt uz Data Lake.</span><span class="sxs-lookup"><span data-stu-id="9f922-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="9f922-149">Manuāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9f922-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="9f922-150">Pieteikumu pievienošana Azure AD nomniekam</span><span class="sxs-lookup"><span data-stu-id="9f922-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="9f922-151">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9f922-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="9f922-152">Atlasiet **Pārvaldīt \> Uzņēmuma pieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="9f922-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="9f922-153">Uzmeklējiet tālāk norādītos pieteikumus, izmantojot pieteikuma ID.</span><span class="sxs-lookup"><span data-stu-id="9f922-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="9f922-154">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="9f922-154">Application</span></span>                              | <span data-ttu-id="9f922-155">Programmas ID</span><span class="sxs-lookup"><span data-stu-id="9f922-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="9f922-156">Microsoft Dynamics ERP apakšpakalpojumi</span><span class="sxs-lookup"><span data-stu-id="9f922-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="9f922-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="9f922-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="9f922-158">Microsoft Dynamics ERP apakšpakalpojumi CDS</span><span class="sxs-lookup"><span data-stu-id="9f922-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="9f922-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="9f922-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="9f922-160">AI Builder autorizācijas pakalpojums</span><span class="sxs-lookup"><span data-stu-id="9f922-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="9f922-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="9f922-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="9f922-162">Ja nevarat atrast nevienu no iepriekšējiem pieteikumiem, izmēģiniet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9f922-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="9f922-163">Sava lokālā datora izvēlnē **Sākt** uzmeklējiet **powershell**.</span><span class="sxs-lookup"><span data-stu-id="9f922-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="9f922-164">Atlasiet un turiet nospiestu (vai noklikšķiniet ar peles labo pogu) **Windows PowerShell** un pēc tam atlasiet **Palaist kā administratoram**.</span><span class="sxs-lookup"><span data-stu-id="9f922-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="9f922-165">Palaidiet tālāk norādīto komandu, lai instalētu **AzureAD** moduli.</span><span class="sxs-lookup"><span data-stu-id="9f922-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="9f922-166">Ja ir nepieciešams NuGet nodrošinātājs, lai turpinātu, atlasiet **Y**, lai to instalētu.</span><span class="sxs-lookup"><span data-stu-id="9f922-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="9f922-167">Ja tiek parādīts ziņojums “Neuzticams repozitorijs”, atlasiet **Y**, lai turpinātu.</span><span class="sxs-lookup"><span data-stu-id="9f922-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="9f922-168">Katram pieteikumam, kas jāpievieno, palaidiet tālāk norādītās komandas, lai pievienotu pieteikumu Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9f922-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="9f922-169">Kad saņemat aicinājumu, pierakstieties kā Azure AD administrators.</span><span class="sxs-lookup"><span data-stu-id="9f922-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="9f922-170">Azure resursu izveidošana</span><span class="sxs-lookup"><span data-stu-id="9f922-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="9f922-171">Pārliecinieties, ka izveidojat tālāk norādītos resursus tajā pašā Azure AD instancē, kurā ir Dataverse vide.</span><span class="sxs-lookup"><span data-stu-id="9f922-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="9f922-172">Nav iespējams izmantot resursus no citas Azure AD instances.</span><span class="sxs-lookup"><span data-stu-id="9f922-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="9f922-173">Izveidojiet krātuves kontu:</span><span class="sxs-lookup"><span data-stu-id="9f922-173">Create a storage account:</span></span>

    1. <span data-ttu-id="9f922-174">[Azure portālā](https://portal.azure.com) izveidojiet krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="9f922-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="9f922-175">Dialoglodziņā **Izveidot krātuves kontu** iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="9f922-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="9f922-176">**Atrašanās vieta** — atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="9f922-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="9f922-177">**Veiktspēja** — ieteicams atlasīt **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="9f922-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="9f922-178">**Konta veids** — jāatlasa **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="9f922-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="9f922-179">Dialoglodziņā **Papildu opcijas** opcijā **Data Lake Storage Gen2** atlasiet **Iespējot** līdzeklī **Hierarhiskās nosaukumvietas**.</span><span class="sxs-lookup"><span data-stu-id="9f922-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="9f922-180">Ja šis līdzeklis netiks iespējots, nevarēsit patērēt datus, ko Finance and Operations programmas raksta, izmantojot tādus pakalpojumus kā Power BI datu plūsmas.</span><span class="sxs-lookup"><span data-stu-id="9f922-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="9f922-181">Atlasiet **Pārskatīt un izveidot**.</span><span class="sxs-lookup"><span data-stu-id="9f922-181">Select **Review and create**.</span></span> <span data-ttu-id="9f922-182">Kad izvietošana ir pabeigta, jaunais resurss tiks parādīts Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="9f922-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="9f922-183">Dodieties uz izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="9f922-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="9f922-184">Kreisās puses izvēlnē atlasiet **Piekļuves galvenie akreditācijas dati**.</span><span class="sxs-lookup"><span data-stu-id="9f922-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="9f922-185">Kopējiet un saglabājiet krātuves konta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9f922-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="9f922-186">Šī vērtība būs jānorāda vēlāk, kad iestatīsit galvenos akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="9f922-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="9f922-187">Izveidojiet galveno akreditācijas datu glabātavu:</span><span class="sxs-lookup"><span data-stu-id="9f922-187">Create a key vault:</span></span>

    1. <span data-ttu-id="9f922-188">[Azure portālā](https://portal.azure.com) izveidojiet galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="9f922-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="9f922-189">Dialoglodziņā **Izveidot galveno akreditācijas datu glabātavu** laukā **Novietojums** atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="9f922-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="9f922-190">Pēc galvenās akreditācijas datu glabātavas izveidess dodieties uz **Galvenās akreditācijas datu glabātavas pārskatu** un kopējiet un saglabājiet DNS nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9f922-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="9f922-191">Šī vērtība būs jānorāda vēlāk, kad iestatīsit Data Lake pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="9f922-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="9f922-192">Izveidojiet un reģistrējiet Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="9f922-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="9f922-193">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory** un atlasiet **Pieteikumu reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="9f922-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="9f922-194">Atlasiet **Jauna pieteikuma reģistrācija** un iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="9f922-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="9f922-195">**Nosaukums** — ievadiet pieteikuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9f922-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="9f922-196">**Pieteikuma veids** — atlasiet **Web API**.</span><span class="sxs-lookup"><span data-stu-id="9f922-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="9f922-197">**Novirzīt URI iestatīšanu** — ievadiet savas Dynamics 365 instances URL, piemēram, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="9f922-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="9f922-198">Dodieties uz tikko izveidoto pieteikumu, kopējiet un saglabājiet tās **Pieteikuma (klienta) ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f922-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="9f922-199">Šī vērtība būs jānorāda vēlāk, kad iestatīsit galvenos akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="9f922-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="9f922-200">Dodieties uz **API atļaujas** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9f922-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="9f922-201">Atlasiet **Pievienot atļauju**.</span><span class="sxs-lookup"><span data-stu-id="9f922-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="9f922-202">Atlasiet **Azure Galvenā akreditācijas datu glabātava**.</span><span class="sxs-lookup"><span data-stu-id="9f922-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="9f922-203">Pēc deleģēto atļauju atlases atlasiet **lietotājs\_personifikācija**.</span><span class="sxs-lookup"><span data-stu-id="9f922-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="9f922-204">Atlasiet **Pievienot atļaujas**.</span><span class="sxs-lookup"><span data-stu-id="9f922-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="9f922-205">Pieteikuma izvēlnē atlasiet **Sertifikāti \& noslēpumi** un pēc tam izpildiet tālāk norādītās darbības, lai izveidotu galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="9f922-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="9f922-206">Atlasiet **Jauns klienta noslēpums**.</span><span class="sxs-lookup"><span data-stu-id="9f922-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="9f922-207">Ievadiet nosaukumu laukā **Akreditācijas datu glabātavas apraksts**.</span><span class="sxs-lookup"><span data-stu-id="9f922-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="9f922-208">Atlasiet ilgumu un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9f922-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="9f922-209">Noslēpums tiek ģenerēts laukā **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="9f922-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="9f922-210">Kopējiet un saglabājiet klienta slepeno vērtību.</span><span class="sxs-lookup"><span data-stu-id="9f922-210">Copy and save the client secret value.</span></span> <span data-ttu-id="9f922-211">Šī vērtība būs jānorāda vēlāk, kad iestatīsit galvenos akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="9f922-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="9f922-212">Izveidojiet Galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="9f922-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="9f922-213">Dodieties uz galveno akreditācijas datu glabātavu, ko izveidojāt iepriekš, un atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="9f922-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="9f922-214">Katram noslēpuma nosaukumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9f922-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="9f922-215">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="9f922-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="9f922-216">Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="9f922-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="9f922-217">Izveidojiet noslēpuma nosaukumu un vērtību no tabulas.</span><span class="sxs-lookup"><span data-stu-id="9f922-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="9f922-218">Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="9f922-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="9f922-219">Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.</span><span class="sxs-lookup"><span data-stu-id="9f922-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="9f922-220">Slepenais nosaukums</span><span class="sxs-lookup"><span data-stu-id="9f922-220">Secret name</span></span>                       | <span data-ttu-id="9f922-221">Noslēpuma vērtība</span><span class="sxs-lookup"><span data-stu-id="9f922-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="9f922-222">app-id</span><span class="sxs-lookup"><span data-stu-id="9f922-222">app-id</span></span>                            | <span data-ttu-id="9f922-223">Iepriekš izveidotā pieteikuma ID.</span><span class="sxs-lookup"><span data-stu-id="9f922-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="9f922-224">app-secret</span><span class="sxs-lookup"><span data-stu-id="9f922-224">app-secret</span></span>                        | <span data-ttu-id="9f922-225">Iepriekš saglabātais klienta noslēpums.</span><span class="sxs-lookup"><span data-stu-id="9f922-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="9f922-226">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="9f922-226">storage-account-name</span></span>              | <span data-ttu-id="9f922-227">Iepriekš izveidotā krātuves konta nosaukums, piemēram, **storageaccount1**.</span><span class="sxs-lookup"><span data-stu-id="9f922-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="9f922-228">Autorizējiet pieteikumu, lai piekļūtu galveno akreditācijas datu glabātavai.</span><span class="sxs-lookup"><span data-stu-id="9f922-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="9f922-229">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="9f922-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="9f922-230">Atlasiet piekļuves politikas.</span><span class="sxs-lookup"><span data-stu-id="9f922-230">Select the access policies.</span></span>
    3. <span data-ttu-id="9f922-231">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9f922-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="9f922-232">Atlasiet **Pievienot piekļuves politiku**, lai izveidotu piekļuves politiku.</span><span class="sxs-lookup"><span data-stu-id="9f922-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="9f922-233">Laukā **Noslēpuma atļaujas** atlasiet atļaujas no tabulas.</span><span class="sxs-lookup"><span data-stu-id="9f922-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="9f922-234">Laukā **Noslēpuma vadītājs** uzmeklējiet pieteikuma parādāmo nosaukumu no tabulas.</span><span class="sxs-lookup"><span data-stu-id="9f922-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="9f922-235">Atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="9f922-235">Select **Select**.</span></span>
        5. <span data-ttu-id="9f922-236">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="9f922-236">Select **Add**.</span></span>
        6. <span data-ttu-id="9f922-237">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="9f922-237">Select **Save**.</span></span>

        | <span data-ttu-id="9f922-238">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="9f922-238">Application</span></span>                                              | <span data-ttu-id="9f922-239">Tiesības</span><span class="sxs-lookup"><span data-stu-id="9f922-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="9f922-240">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="9f922-240">The display name of the new application that you created</span></span> | <span data-ttu-id="9f922-241">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="9f922-241">Get, List</span></span>   |
        | <span data-ttu-id="9f922-242">**Microsoft Dynamics ERP apakšpakalpojumi**</span><span class="sxs-lookup"><span data-stu-id="9f922-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="9f922-243">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="9f922-243">Get, List</span></span>   |

6. <span data-ttu-id="9f922-244">Piešķiriet lomas, lai piekļūtu krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="9f922-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="9f922-245">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="9f922-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="9f922-246">Atlasiet **Piekļuves kontrole (IAM)** un pēc tam atlasiet **Lomu piešķires**.</span><span class="sxs-lookup"><span data-stu-id="9f922-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="9f922-247">Atlasiet **Pievienot, pievienot lomas piešķiri**.</span><span class="sxs-lookup"><span data-stu-id="9f922-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="9f922-248">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9f922-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="9f922-249">Atlasiet lomu no tabulas.</span><span class="sxs-lookup"><span data-stu-id="9f922-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="9f922-250">Atstājiet lauku **Piešķirt piekļuvi** iestatītu uz **Azure AD lietotājs, grupa vai pakalpojuma vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="9f922-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="9f922-251">Laukā **Atlasīt** ievadiet pieteikumu no tabulas.</span><span class="sxs-lookup"><span data-stu-id="9f922-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="9f922-252">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="9f922-252">Select **Save**.</span></span>

        | <span data-ttu-id="9f922-253">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="9f922-253">Application</span></span>                                              | <span data-ttu-id="9f922-254">Loma</span><span class="sxs-lookup"><span data-stu-id="9f922-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="9f922-255">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="9f922-255">The display name of the new application that you created</span></span> | <span data-ttu-id="9f922-256">Īpašnieks</span><span class="sxs-lookup"><span data-stu-id="9f922-256">Owner</span></span>                       |
        | <span data-ttu-id="9f922-257">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="9f922-257">The display name of the new application that you created</span></span> | <span data-ttu-id="9f922-258">Līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="9f922-258">Contributor</span></span>                 |
        | <span data-ttu-id="9f922-259">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="9f922-259">The display name of the new application that you created</span></span> | <span data-ttu-id="9f922-260">Krātuves konta līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="9f922-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="9f922-261">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="9f922-261">The display name of the new application that you created</span></span> | <span data-ttu-id="9f922-262">Krātuves BLOB datu īpašnieks</span><span class="sxs-lookup"><span data-stu-id="9f922-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="9f922-263">**AI Builder autorizācijas pakalpojums**</span><span class="sxs-lookup"><span data-stu-id="9f922-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="9f922-264">Krātuves BLOB datu lasītājs</span><span class="sxs-lookup"><span data-stu-id="9f922-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="9f922-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="9f922-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="9f922-266">Konfigurēt eksportēšanu uz Data Lake pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="9f922-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="9f922-267">Veiciet tālāk norādītās darbības, lai izmantotu LCS, pievienojot videi eksportēšanu uz Data Lake pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="9f922-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="9f922-268">Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.</span><span class="sxs-lookup"><span data-stu-id="9f922-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="9f922-269">Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="9f922-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="9f922-270">Atlasiet pievienojumprogrammu **Eksportēt uz Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="9f922-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="9f922-271">Ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="9f922-271">Enter the following values.</span></span>

    | <span data-ttu-id="9f922-272">Vērtība</span><span class="sxs-lookup"><span data-stu-id="9f922-272">Value</span></span>                                                              | <span data-ttu-id="9f922-273">Apraksts</span><span class="sxs-lookup"><span data-stu-id="9f922-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="9f922-274">Nomnieka ID Azure abonementam, kur atrodas Galvenās akreditācijas datu glabātava</span><span class="sxs-lookup"><span data-stu-id="9f922-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="9f922-275">Nomnieka ID, kur atrodas krātuves konts, pieteikumi un galvenās akreditācijas datu glabātavas.</span><span class="sxs-lookup"><span data-stu-id="9f922-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="9f922-276">Lai iegūtu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**.</span><span class="sxs-lookup"><span data-stu-id="9f922-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="9f922-277">Norādiet sava Key Vault DNS nosaukumu</span><span class="sxs-lookup"><span data-stu-id="9f922-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="9f922-278">Galvenās akreditācijas datu glabātavas DNS nosaukums, piemēram, `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="9f922-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="9f922-279">Norādiet noslēpumu, kas satur krātuves konta nosaukumu</span><span class="sxs-lookup"><span data-stu-id="9f922-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="9f922-280">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="9f922-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="9f922-281">Pieteikuma ID noslēpuma nosaukums, kas jāizmanto, lai piekļūtu Data Lake</span><span class="sxs-lookup"><span data-stu-id="9f922-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="9f922-282">**app-id**</span><span class="sxs-lookup"><span data-stu-id="9f922-282">**app-id**</span></span> |
    | <span data-ttu-id="9f922-283">Programmas klienta noslēpuma nosaukums</span><span class="sxs-lookup"><span data-stu-id="9f922-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="9f922-284">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="9f922-284">**app-secret**</span></span> |

5. <span data-ttu-id="9f922-285">Piekrītiet nosacījumiem un pēc tam atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="9f922-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="9f922-286">Pievienojumprogramma tiks instalēta dažu minūšu laikā.</span><span class="sxs-lookup"><span data-stu-id="9f922-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="9f922-287">Finance Insights pievienojumprogrammas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9f922-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="9f922-288">Ja iepriekš instalējāt pievienojumprogrammu Iegūt ieskatus, atinstalējiet to, pirms tālāk norādītās procedūras izpildes.</span><span class="sxs-lookup"><span data-stu-id="9f922-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="9f922-289">Izpildiet šīs darbības, lai instalētu Finance Insights pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="9f922-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="9f922-290">Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.</span><span class="sxs-lookup"><span data-stu-id="9f922-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="9f922-291">Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="9f922-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="9f922-292">Atlasiet pievienojumprogrammu **Finance Insights**.</span><span class="sxs-lookup"><span data-stu-id="9f922-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="9f922-293">Piekrītiet nosacījumiem un pēc tam atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="9f922-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="9f922-294">Atsauksmes un atbalsts</span><span class="sxs-lookup"><span data-stu-id="9f922-294">Feedback and support</span></span>

<span data-ttu-id="9f922-295">Ja vēlaties sniegt atsauksmes vai jums nepieciešams atbalsts, sūtiet e-pastu uz [Finance Insights (priekšskatījums)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="9f922-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
