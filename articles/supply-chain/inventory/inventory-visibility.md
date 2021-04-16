---
title: Krājumu uztveramības pievienojumprogramma
description: Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt krājumu uztveramības pievienojumprogrammu sistēmai Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e294ada8dd3e764987aa363adb2614416986575b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821133"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="a137f-103">Krājumu uztveramības pievienojumprogramma</span><span class="sxs-lookup"><span data-stu-id="a137f-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="a137f-104">Krājumu uztveramības pievienojumprogramma ir neatkarīgs un ļoti mērogojams pakalpojums, kas nodrošina reāllaika rīcībā esošo krājumu izsekošanu, tādējādi sniedzot globālu skatījumu uz krājumu uztveramību.</span><span class="sxs-lookup"><span data-stu-id="a137f-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="a137f-105">Visa informācija, kas saistīta ar rīcībā esošajiem krājumiem, tiek eksportēta uz pakalpojumu gandrīz reāllaikā, izmantojot zema līmeņa SQL integrāciju.</span><span class="sxs-lookup"><span data-stu-id="a137f-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="a137f-106">Ārējās sistēmas piekļūst pakalpojumam, izmantojot RESTful API, lai vaicātu rīcībā esošo informāciju par noteiktajām dimensiju kopām, tādējādi izgūstot pieejamo rīcībā esošo pozīciju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a137f-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="a137f-107">Krājumu uztveramība ir Microsoft Dataverse iebūvēts pakalpojums, kas nozīmē, ka varat to pagarināt, izveidojot Power Apps un pielietojot Power BI, lai nodrošinātu pielāgotu funkcionalitāti, kas atbilst jūsu biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="a137f-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="a137f-108">Var arī jaunināt indeksu, lai veiktu krājumu vaicājumus.</span><span class="sxs-lookup"><span data-stu-id="a137f-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="a137f-109">Krājumu uztveramība nodrošina konfigurācijas opcijas, kas ļauj to integrēt ar vairākām trešās puses sistēmām.</span><span class="sxs-lookup"><span data-stu-id="a137f-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="a137f-110">Tā atbalsta standartizētu krājumu dimensiju, pielāgoto paplašināšanos un standartizētu, konfigurējamu aprēķināto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="a137f-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="a137f-111">Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt Krājumu uztveramības pievienojumprogrammu Dynamics 365 Supply Chain Management un kā izmantot tās programmas programmēšanas interfeisu (API).</span><span class="sxs-lookup"><span data-stu-id="a137f-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="a137f-112">Instalēt krājumu uztveramības pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="a137f-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="a137f-113">Jums ir jāinstalē Krājumu uztveramības pievienojumprogramma, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a137f-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a137f-114">LCS ir sadarbības portāls, kas nodrošina vides un regulāri atjauninātu pakalpojumu kopu, kas palīdz pārvaldīt jūsu lietojumprogrammu dzīves ciklu Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a137f-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="a137f-115">Papildinformāciju skatiet šeit: [Lifecycle Services resursi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="a137f-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a137f-116">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="a137f-116">Prerequisites</span></span>

<span data-ttu-id="a137f-117">Pirms instalējat Krājumu uztveramības pievienojumprogrammu, jums ir jādara sekojošais:</span><span class="sxs-lookup"><span data-stu-id="a137f-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="a137f-118">Iegūt LCS ieviešanas projektu, kurā ir vismaz viens izvietošanas vides objekts.</span><span class="sxs-lookup"><span data-stu-id="a137f-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="a137f-119">Pārliecinieties, ka pievienojumprogrammu pārskata iestatīšanas priekšnoteikumi, kas sniegti [Pievienojumprogrammu pārskatā](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) ir pabeigti.</span><span class="sxs-lookup"><span data-stu-id="a137f-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="a137f-120">Krājumu redzamībai nav nepieciešama dubultās rakstīšanas saistīšana.</span><span class="sxs-lookup"><span data-stu-id="a137f-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="a137f-121">Sazinieties ar krājumu redzamības grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu šādus trīs nepieciešamos failus:</span><span class="sxs-lookup"><span data-stu-id="a137f-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="a137f-122">`Inventory Visibility Integration.zip` (Ja jūsu darbinātā Supply Chain Management versija ir agrāka nekā versija 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="a137f-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="a137f-123">Pašlaik atbalstītās valstis un reģioni ietver Kanādu, Amerikas Savienotās Valstis un Eiropas Savienību (ES).</span><span class="sxs-lookup"><span data-stu-id="a137f-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="a137f-124">Ja jums ir kādi jautājumi par šiem priekšnosacījumiem, lūdzu, sazinieties ar krājumu redzamības preču darba grupu.</span><span class="sxs-lookup"><span data-stu-id="a137f-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="a137f-125">Dataverse iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a137f-125">Set up Dataverse</span></span>

<span data-ttu-id="a137f-126">Lai iestatītu Dataverse, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="a137f-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="a137f-127">Pievienojiet pakalpojumu principu savam nomniekam:</span><span class="sxs-lookup"><span data-stu-id="a137f-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="a137f-128">Instalējiet Azure AD PowerShell moduli v2, kā aprakstīts [Azure Active Directory instalēšana PowerShell grafikam](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="a137f-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="a137f-129">Izpildiet šādu PowerShell komandu.</span><span class="sxs-lookup"><span data-stu-id="a137f-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="a137f-130">Izveidot programmas lietotāju, lai noteiktu krājumu redzamību Dataverse šeit:</span><span class="sxs-lookup"><span data-stu-id="a137f-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="a137f-131">Atveriet Dataverse vides URL.</span><span class="sxs-lookup"><span data-stu-id="a137f-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="a137f-132">Dodieties uz **Papildu iestatījumi \> Sistēma \> Drošība \> Lietotāji** un izveidojiet programmas lietotāju.</span><span class="sxs-lookup"><span data-stu-id="a137f-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="a137f-133">Izmantojiet skata izvēlni, lai mainītu lapas skatu uz **Programmas lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="a137f-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="a137f-134">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="a137f-134">Select **New**.</span></span> <span data-ttu-id="a137f-135">Iestatiet Programmas ID uz *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="a137f-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="a137f-136">(Saglabājot izmaiņas, objekta ID tiks ielādēts automātiski.) Šo nosaukumu var pielāgot.</span><span class="sxs-lookup"><span data-stu-id="a137f-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="a137f-137">Piemēram, to var mainīt uz *Krājumu redzamība*.</span><span class="sxs-lookup"><span data-stu-id="a137f-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="a137f-138">Pēc pabeigšanas atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a137f-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="a137f-139">Atlasiet **Piešķirt lomu** un pēc tam atlasiet **Sistēmas administrators**.</span><span class="sxs-lookup"><span data-stu-id="a137f-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="a137f-140">Ja ir loma ar nosaukumu **Common Data Service Lietotājs**, atlasiet to arī.</span><span class="sxs-lookup"><span data-stu-id="a137f-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="a137f-141">Papildinformāciju skatiet nodaļā [Programmas lietotāja izveide](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="a137f-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="a137f-142">Importēt `Inventory Visibility Dataverse Solution.zip` failu, kas ietver Dataverse ar konfigurāciju saistītos elementus un Power Apps:</span><span class="sxs-lookup"><span data-stu-id="a137f-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="a137f-143">Doties uz lapu **Risinājumi**.</span><span class="sxs-lookup"><span data-stu-id="a137f-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="a137f-144">Atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="a137f-144">Select **Import**.</span></span>

1. <span data-ttu-id="a137f-145">Importēt konfigurācijas jaunināšanas trigera plūsmu:</span><span class="sxs-lookup"><span data-stu-id="a137f-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="a137f-146">Doties uz lapu Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="a137f-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="a137f-147">Pārliecinieties, vai pastāv savienojums ar nosaukumu *Dataverse (mantojums)*.</span><span class="sxs-lookup"><span data-stu-id="a137f-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="a137f-148">(Ja tāda nav, izveidojiet to.)</span><span class="sxs-lookup"><span data-stu-id="a137f-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="a137f-149">Importēt `Inventory Visibility Configuration Trigger.zip` failu.</span><span class="sxs-lookup"><span data-stu-id="a137f-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="a137f-150">Pēc tā importēšanas trigeris parādīsies zem **Manas plūsmas**.</span><span class="sxs-lookup"><span data-stu-id="a137f-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="a137f-151">Inicializējiet tālāk norādītos četrus mainīgos, pamatojoties uz vides informāciju:</span><span class="sxs-lookup"><span data-stu-id="a137f-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="a137f-152">Azure nomnieka ID</span><span class="sxs-lookup"><span data-stu-id="a137f-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="a137f-153">Azure Lietojumprogrammas klienta ID</span><span class="sxs-lookup"><span data-stu-id="a137f-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="a137f-154">Azure Lietojumprogrammas klienta noslēpums</span><span class="sxs-lookup"><span data-stu-id="a137f-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="a137f-155">Krājumu redzamības galapunkts</span><span class="sxs-lookup"><span data-stu-id="a137f-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="a137f-156">Papildinformāciju par šo mainīgo skatiet tālāk šīs tēmas sadaļā [Krājumu redzamības integrācijas iestatīšana](#setup-inventory-visibility-integration).</span><span class="sxs-lookup"><span data-stu-id="a137f-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="a137f-157">![Konfigurācijas trigeris](media/configuration-trigger.png "Konfigurācijas trigeris")</span><span class="sxs-lookup"><span data-stu-id="a137f-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="a137f-158">Atlasiet **Ieslēgt**.</span><span class="sxs-lookup"><span data-stu-id="a137f-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="a137f-159">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="a137f-159">Install the add-in</span></span>

<span data-ttu-id="a137f-160">Lai instalētu Krājumu uztveramības pievienojumprogrammu, jums jārīkojas šādi:</span><span class="sxs-lookup"><span data-stu-id="a137f-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="a137f-161">Pierakstieties portālā [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="a137f-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="a137f-162">Sākumlapā atlasiet projektu, kurā tiek izvietota jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="a137f-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="a137f-163">Projekta lapā atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="a137f-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="a137f-164">Vides lapā ritiniet uz leju, līdz redzat sadaļu **Vides pievienojumprogrammas** sadaļā **Power Platform integrācija**, kur varat atrast Dataverse vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a137f-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="a137f-165">Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="a137f-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="a137f-166">![Vides lapa portālā LCS](media/inventory-visibility-environment.png "Vides lapa portālā LCS")</span><span class="sxs-lookup"><span data-stu-id="a137f-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="a137f-167">Atlasiet saiti **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="a137f-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="a137f-168">Tiek atvērts pieejamo pievienojumprogrammu saraksts.</span><span class="sxs-lookup"><span data-stu-id="a137f-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="a137f-169">Atlasiet no saraksta **Krājumu redzamība**.</span><span class="sxs-lookup"><span data-stu-id="a137f-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="a137f-170">Ievadiet vērtības savai video šādiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="a137f-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="a137f-171">**AAD Lietojumprogrammas (klienta) ID**</span><span class="sxs-lookup"><span data-stu-id="a137f-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="a137f-172">**AAD nomnieka ID**</span><span class="sxs-lookup"><span data-stu-id="a137f-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="a137f-173">![Pievienot iestatīšanas lapā](media/inventory-visibility-setup.png "Pievienojumprogrammas iestatīšanas lapa")</span><span class="sxs-lookup"><span data-stu-id="a137f-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="a137f-174">Piekrist noteikumiem un nosacījumam, atlasot izvēles rūtiņu **Noteikumi un nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="a137f-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="a137f-175">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="a137f-175">Select **Install**.</span></span> <span data-ttu-id="a137f-176">Pievienojumprogrammu statuss tiks rādīts kā **Instalē**.</span><span class="sxs-lookup"><span data-stu-id="a137f-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="a137f-177">Kad tas ir izdarīts, atsvaidziniet lapu, lai redzētu statusa maiņu uz **Instalēts**.</span><span class="sxs-lookup"><span data-stu-id="a137f-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="a137f-178">Pievienojumprogrammas atinstalēšana</span><span class="sxs-lookup"><span data-stu-id="a137f-178">Uninstall the add-in</span></span>

<span data-ttu-id="a137f-179">Lai atinstalētu pievienojumprogrammu, atlasiet **Atinstalēt**.</span><span class="sxs-lookup"><span data-stu-id="a137f-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="a137f-180">Kad atsvaidzināsiet LCS, Krājumu uztveramības pievienojumprogramma tiks noņemta.</span><span class="sxs-lookup"><span data-stu-id="a137f-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="a137f-181">Atinstalēšanas process noņems pievienojumprogrammu reģistrāciju un arī sāks darbu, lai notīrītu visus pakalpojumā saglabātos biznesa datus.</span><span class="sxs-lookup"><span data-stu-id="a137f-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="a137f-182">Patērēt rīcībā esošos krājumu datus no Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="a137f-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="a137f-183">Izvietot Krājumu redzamības integrācijas pakotni</span><span class="sxs-lookup"><span data-stu-id="a137f-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="a137f-184">Ja jūs palaidāt Supply Chain Management versiju 10.0.17 vai agrāk, sazinieties ar Krājumu redzamības standarta atbalsta komandu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu iepakojuma failu.</span><span class="sxs-lookup"><span data-stu-id="a137f-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="a137f-185">Pēc tam izvietojiet pakotni LCS.</span><span class="sxs-lookup"><span data-stu-id="a137f-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="a137f-186">Ja izvietošanas laikā rodas versiju neatbilstības kļūda, X++ projekts ir jāimportē manuāli izstrādes vidē.</span><span class="sxs-lookup"><span data-stu-id="a137f-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="a137f-187">Pēc tam izveidojiet izvietojamu pakotni savā izstrādes vidē un izvietojiet to ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="a137f-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="a137f-188">Kods ir iekļauts Supply Chain Management versijā 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="a137f-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="a137f-189">Ja izmantojat šo versiju vai jaunāku, izvietošana nav nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="a137f-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="a137f-190">Pārliecinieties, ka jūsu Supply Chain Management vidē ir ieslēgtas šādas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="a137f-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="a137f-191">(Pēc noklusējuma tās ir iespējotas.)</span><span class="sxs-lookup"><span data-stu-id="a137f-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="a137f-192">Līdzekļa apraksts</span><span class="sxs-lookup"><span data-stu-id="a137f-192">Feature description</span></span> | <span data-ttu-id="a137f-193">Koda versija</span><span class="sxs-lookup"><span data-stu-id="a137f-193">Code version</span></span> | <span data-ttu-id="a137f-194">Pārslēgt klasi</span><span class="sxs-lookup"><span data-stu-id="a137f-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="a137f-195">Iespējot vai atspējot krājumu dimensiju izmantošana InventSum tabulā</span><span class="sxs-lookup"><span data-stu-id="a137f-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="a137f-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="a137f-196">10.0.11</span></span> | <span data-ttu-id="a137f-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="a137f-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="a137f-198">Iespējot vai atspējot krājumu dimensiju izmantošana InventSumDelta tabulā</span><span class="sxs-lookup"><span data-stu-id="a137f-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="a137f-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="a137f-199">10.0.12</span></span> | <span data-ttu-id="a137f-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="a137f-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="a137f-201">Pievienojumprogrammas Krājumu redzamība integrācijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a137f-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="a137f-202">Programmā Supply Chain Management atveriet **[Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbvietu un iespējojiet **Krājumu redzamības integrācijas** līdzekli.</span><span class="sxs-lookup"><span data-stu-id="a137f-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="a137f-203">Pārejiet uz sadaļu **Krājumu pārvaldība \> Iestatījumi \> Krājumu redzamības integrēšanas parametri** un ievadiet URL, kurā palaižat Krājumu redzamību.</span><span class="sxs-lookup"><span data-stu-id="a137f-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="a137f-204">Atrodiet LCS vides Azure reģionu un pēc tam ievadiet vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="a137f-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="a137f-205">URL ir šāda veidlapa:</span><span class="sxs-lookup"><span data-stu-id="a137f-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="a137f-206">Piemēram, ja esat Eiropā, jūsu videi būs viens no šiem vietrāžiem URL:</span><span class="sxs-lookup"><span data-stu-id="a137f-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="a137f-207">Pieejami šādi reģioni.</span><span class="sxs-lookup"><span data-stu-id="a137f-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="a137f-208">Azure reģions</span><span class="sxs-lookup"><span data-stu-id="a137f-208">Azure region</span></span> | <span data-ttu-id="a137f-209">Reģiona īsais nosaukums</span><span class="sxs-lookup"><span data-stu-id="a137f-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="a137f-210">Austrālijas austrumi</span><span class="sxs-lookup"><span data-stu-id="a137f-210">Australia east</span></span> | <span data-ttu-id="a137f-211">eau</span><span class="sxs-lookup"><span data-stu-id="a137f-211">eau</span></span> |
    | <span data-ttu-id="a137f-212">Austrālijas dienvidaustrumi</span><span class="sxs-lookup"><span data-stu-id="a137f-212">Australia southeast</span></span> | <span data-ttu-id="a137f-213">seau</span><span class="sxs-lookup"><span data-stu-id="a137f-213">seau</span></span> |
    | <span data-ttu-id="a137f-214">Kanādas centrālā daļā</span><span class="sxs-lookup"><span data-stu-id="a137f-214">Canada central</span></span> | <span data-ttu-id="a137f-215">cca</span><span class="sxs-lookup"><span data-stu-id="a137f-215">cca</span></span> |
    | <span data-ttu-id="a137f-216">Kanādas austrumi</span><span class="sxs-lookup"><span data-stu-id="a137f-216">Canada east</span></span> | <span data-ttu-id="a137f-217">eca</span><span class="sxs-lookup"><span data-stu-id="a137f-217">eca</span></span> |
    | <span data-ttu-id="a137f-218">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="a137f-218">North Europe</span></span> | <span data-ttu-id="a137f-219">neu</span><span class="sxs-lookup"><span data-stu-id="a137f-219">neu</span></span> |
    | <span data-ttu-id="a137f-220">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="a137f-220">West Europe</span></span> | <span data-ttu-id="a137f-221">weu</span><span class="sxs-lookup"><span data-stu-id="a137f-221">weu</span></span> |
    | <span data-ttu-id="a137f-222">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="a137f-222">East US</span></span> | <span data-ttu-id="a137f-223">eus</span><span class="sxs-lookup"><span data-stu-id="a137f-223">eus</span></span> |
    | <span data-ttu-id="a137f-224">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="a137f-224">West US</span></span> | <span data-ttu-id="a137f-225">wus</span><span class="sxs-lookup"><span data-stu-id="a137f-225">wus</span></span> |

1. <span data-ttu-id="a137f-226">Dodieties uz **Krājumu pārvaldība \> Periodiskie \> Krājumu redzamības integrāciju** un iespējojiet darbu.</span><span class="sxs-lookup"><span data-stu-id="a137f-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="a137f-227">Visi krājumu izmaiņu notikumi no Supply Chain Management tagad tiks grāmatoti Krājumu redzamībai.</span><span class="sxs-lookup"><span data-stu-id="a137f-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="a137f-228">Krājumu redzamības pievienojumprogrammas publiskais API</span><span class="sxs-lookup"><span data-stu-id="a137f-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="a137f-229">Krājumu redzamības pievienojumprogrammas publiskais REST API piedāvā vairākus specifiskus integrācijas galapunktus.</span><span class="sxs-lookup"><span data-stu-id="a137f-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="a137f-230">Tas atbalsta trīs galvenos mijiedarbības tipus:</span><span class="sxs-lookup"><span data-stu-id="a137f-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="a137f-231">Iegrāmatojot pievienojumprogrammas rīcībā esošās izmaiņas no ārējās sistēmas</span><span class="sxs-lookup"><span data-stu-id="a137f-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="a137f-232">Tiek vaicāti pašreizējie rīcībā esošie daudzumi no ārējās sistēmas</span><span class="sxs-lookup"><span data-stu-id="a137f-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="a137f-233">Automātiska sinhronizācija ar Supply Chain Management rīcībā esošiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="a137f-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="a137f-234">Automātiskā sinhronizācija nav daļa no publiskā API.</span><span class="sxs-lookup"><span data-stu-id="a137f-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="a137f-235">Tā vietā tā tiek apstrādāta fonā vidēm, kurās ir iespējota krājumu redzamības pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="a137f-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="a137f-236">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="a137f-236">Authentication</span></span>

<span data-ttu-id="a137f-237">Platformas drošības marķieris tiek izmantots, lai izsauktu Krājumu redzamības pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="a137f-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="a137f-238">Tāpēc, izmantojot programmu, ir jāizveido *Azure Active Directory (Azure AD) marķieris* ar Azure AD lietotni.</span><span class="sxs-lookup"><span data-stu-id="a137f-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="a137f-239">Pēc tam ir jāizmanto Azure AD marķieris, lai iegūtu *piekļuves pilnvaras* no drošības pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="a137f-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="a137f-240">Lai iegūtu drošības pakalpojuma pilnvaru, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="a137f-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="a137f-241">Pieteikties Azure portālā un izmantot to, lai atrastu `clientId` un `clientSecret` savai Supply Chain Management programmai.</span><span class="sxs-lookup"><span data-stu-id="a137f-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="a137f-242">Panest marķieri Azure Active Directory (`aadToken`), iesniedzot HTTP pieprasījumu ar šādiem rekvizītiem:</span><span class="sxs-lookup"><span data-stu-id="a137f-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="a137f-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="a137f-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="a137f-244">**Metode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="a137f-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="a137f-245">**Pamatteksta saturs (formas dati)**:</span><span class="sxs-lookup"><span data-stu-id="a137f-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="a137f-246">key</span><span class="sxs-lookup"><span data-stu-id="a137f-246">key</span></span> | <span data-ttu-id="a137f-247">vērtība</span><span class="sxs-lookup"><span data-stu-id="a137f-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="a137f-248">client_id</span><span class="sxs-lookup"><span data-stu-id="a137f-248">client_id</span></span> | <span data-ttu-id="a137f-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="a137f-249">${aadAppId}</span></span> |
        | <span data-ttu-id="a137f-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="a137f-250">client_secret</span></span> | <span data-ttu-id="a137f-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="a137f-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="a137f-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="a137f-252">grant_type</span></span> | <span data-ttu-id="a137f-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="a137f-253">client_credentials</span></span> |
        | <span data-ttu-id="a137f-254">resource</span><span class="sxs-lookup"><span data-stu-id="a137f-254">resource</span></span> | <span data-ttu-id="a137f-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="a137f-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="a137f-256">Jums jāsaņem `aadToken` atbilde, kas ir līdzīga šim piemēram.</span><span class="sxs-lookup"><span data-stu-id="a137f-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="a137f-257">Formulējiet JSON pieprasījumu, kas ir līdzīgs šim:</span><span class="sxs-lookup"><span data-stu-id="a137f-257">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="a137f-258">Kur:</span><span class="sxs-lookup"><span data-stu-id="a137f-258">Where:</span></span>
    - <span data-ttu-id="a137f-259">Vērtībai `client_assertion` jābūt `aadToken` tai, kas saņemta iepriekšējā solī.</span><span class="sxs-lookup"><span data-stu-id="a137f-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="a137f-260">Vērtībai `context` ir jābūt vides ID, kur vēlaties izvietot pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="a137f-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="a137f-261">Iestatiet visas citas vērtības, kā parādītas piemērā.</span><span class="sxs-lookup"><span data-stu-id="a137f-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="a137f-262">Iesniedziet HTTP pieprasījumu ar šādiem rekvizītiem:</span><span class="sxs-lookup"><span data-stu-id="a137f-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="a137f-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="a137f-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="a137f-264">**Metode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="a137f-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="a137f-265">**HTTP virsraksts** - iekļaut API versiju (atslēga ir `Api-Version`un vērtība ir `1.0`)</span><span class="sxs-lookup"><span data-stu-id="a137f-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="a137f-266">**Pamatteksts** - iekļaut JSON pieprasījumu, ko izveidojāt iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="a137f-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="a137f-267">`access_token` jūs saņemsiet atbildē.</span><span class="sxs-lookup"><span data-stu-id="a137f-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="a137f-268">Tas ir tas, kas jums nepieciešams kā nesēja marķieris, lai izsauktu krājumu redzamības API.</span><span class="sxs-lookup"><span data-stu-id="a137f-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="a137f-269">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="a137f-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="a137f-270">Konfigurēt krājumu uztveramības API</span><span class="sxs-lookup"><span data-stu-id="a137f-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="a137f-271">Pirms pakalpojuma izmantošanas ir jāpabeidz konfigurācijas, kas aprakstītas sekojošās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="a137f-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="a137f-272">Konfigurācija var atšķirties atkarībā no jūsu vides datiem.</span><span class="sxs-lookup"><span data-stu-id="a137f-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="a137f-273">Tā galvenokārt ietver četras daļas:</span><span class="sxs-lookup"><span data-stu-id="a137f-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="a137f-274">Sadalīšana</span><span class="sxs-lookup"><span data-stu-id="a137f-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="a137f-275">Dimensiju konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="a137f-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="a137f-276">Indeksācija</span><span class="sxs-lookup"><span data-stu-id="a137f-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="a137f-277">Pielāgots mērījums</span><span class="sxs-lookup"><span data-stu-id="a137f-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="a137f-278">Sadalīšana</span><span class="sxs-lookup"><span data-stu-id="a137f-278">Partitioning</span></span>

<span data-ttu-id="a137f-279">Sadalīšana var būtiski ietekmēt Krājumu uztveramības API veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="a137f-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="a137f-280">Ir ieteicams definēt shēmu, kas ļauj izmantot mazus datu grupējumus, vienlaikus atļaujot jēgpilnus datu vaicājumus.</span><span class="sxs-lookup"><span data-stu-id="a137f-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="a137f-281">`organizationId` (`dataAreaId` Supply Chain Management) vienmēr būs daļa no sadalīšanas, un pēc noklusējuma Krājumu uztveramība ir iestatīta uz sadalījumu pēc dimensijām kā *Vietne + Atrašanās vieta*.</span><span class="sxs-lookup"><span data-stu-id="a137f-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="a137f-282">Tas nozīmē, ka pakalpojumi vienmēr ir jāvaicā ar šīm filtriem definētajām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="a137f-283">*Vietne* un *Atrašanās vieta* ir divas galvenās noklusējuma dimensijas Krājumu uztveramībai.</span><span class="sxs-lookup"><span data-stu-id="a137f-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="a137f-284">Supply Chain Management šīs dimensijas tiek sauktas par *Vietni* (`InventSiteId`) un *Noliktavu* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="a137f-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="a137f-285">Dimensiju konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="a137f-285">Dimension configurations</span></span>

<span data-ttu-id="a137f-286">Krājumu uztveramība nodrošinās vispārēju noklusējuma dimensiju sarakstu, lai iespējotu vairāku avotu sistēmu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="a137f-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="a137f-287">Sekojošajā tabulā ir minētas krājumu dimensijas, kas būs noklusējuma dimensiju nosaukumi Krājumu uztveramībai.</span><span class="sxs-lookup"><span data-stu-id="a137f-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="a137f-288">Dimensiju veids</span><span class="sxs-lookup"><span data-stu-id="a137f-288">Dimension type</span></span> | <span data-ttu-id="a137f-289">Dimensijas nosaukums</span><span class="sxs-lookup"><span data-stu-id="a137f-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="a137f-290">Produkts</span><span class="sxs-lookup"><span data-stu-id="a137f-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="a137f-291">Produkts</span><span class="sxs-lookup"><span data-stu-id="a137f-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="a137f-292">Produkts</span><span class="sxs-lookup"><span data-stu-id="a137f-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="a137f-293">Produkts</span><span class="sxs-lookup"><span data-stu-id="a137f-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="a137f-294">Izsekošana</span><span class="sxs-lookup"><span data-stu-id="a137f-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="a137f-295">Izsekošana</span><span class="sxs-lookup"><span data-stu-id="a137f-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="a137f-296">Novietojums</span><span class="sxs-lookup"><span data-stu-id="a137f-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="a137f-297">Novietojums</span><span class="sxs-lookup"><span data-stu-id="a137f-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="a137f-298">Krājumu statuss</span><span class="sxs-lookup"><span data-stu-id="a137f-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="a137f-299">Specifiska noliktava</span><span class="sxs-lookup"><span data-stu-id="a137f-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="a137f-300">Specifiska noliktava</span><span class="sxs-lookup"><span data-stu-id="a137f-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="a137f-301">Specifiska noliktava</span><span class="sxs-lookup"><span data-stu-id="a137f-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="a137f-302">Dimensijas tips, kas norādīts iepriekšējā tabulā, ir tikai atsaucei.</span><span class="sxs-lookup"><span data-stu-id="a137f-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="a137f-303">Nav nepieciešams definēt dimensijas tipu Krājumu uztveramībai.</span><span class="sxs-lookup"><span data-stu-id="a137f-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="a137f-304">Ja pielāgota dimensija pastāv un tai ir jāplūst uz noklusēto vērtību, kad to patērē Krājuma uztveramība, varat konfigurēt **Pielāgoto dimensiju** nosaukumu Krājuma uztveramībā.</span><span class="sxs-lookup"><span data-stu-id="a137f-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="a137f-305">Ārējās sistēmas piekļūst Krājumu uztveramībai, izmantojot REST API, kas iespējo rīcībā esošo informāciju par norādītajām dimensiju kopām.</span><span class="sxs-lookup"><span data-stu-id="a137f-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="a137f-306">Lai to izdarītu, Krājumu uztveramība ļauj konfigurēt *ārējā kanāla datu avotu* un avota dimensiju uz *mērķa dimensijām* Krājumu uztveramībā.</span><span class="sxs-lookup"><span data-stu-id="a137f-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="a137f-307">Mērķa dimensijām jābūt vienai no sekojošajām:</span><span class="sxs-lookup"><span data-stu-id="a137f-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="a137f-308">Noklusētās dimensijas Krājumu pārredzamībai</span><span class="sxs-lookup"><span data-stu-id="a137f-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="a137f-309">Pielāgotas dimensijas</span><span class="sxs-lookup"><span data-stu-id="a137f-309">Custom dimensions</span></span>

<span data-ttu-id="a137f-310">Dimensijas konfigurācijas nolūks ir standartizēt vairāku sistēmu integrāciju vaicājumam dimensijās un grāmatošanas notikumā ar dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="a137f-311">Indeksācija</span><span class="sxs-lookup"><span data-stu-id="a137f-311">Indexing</span></span>

<span data-ttu-id="a137f-312">Vairākumā gadījumu rīcībā esošie krājumi būs ne tikai visaugstākajā "kopējā" līmenī, bet, iespējams, vēlēsities apskatīt apkopotos rezultātus, pamatojoties uz krājumu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="a137f-313">Krājumu pārredzamība nodrošina elastību, ļaujot iestatīt indeksus, kas ir balstīti uz dimensiju vai dimensiju kombināciju.</span><span class="sxs-lookup"><span data-stu-id="a137f-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="a137f-314">Pašlaik varat konfigurēt tikai līdz pieciem indeksiem.</span><span class="sxs-lookup"><span data-stu-id="a137f-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="a137f-315">Jums ir rūpīgi jāapsver, kuru dimensiju vai dimensiju kombināciju izmantosiet pirms ieviešanas, lai nodrošinātu, ka tā atbilst jūsu biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="a137f-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="a137f-316">Piemēram, ja vēlaties vaicāt preces šādi:</span><span class="sxs-lookup"><span data-stu-id="a137f-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="a137f-317">Vaicāt apkopotos rīcībā esošos produktus pēc *Krāsas* un *Izmēra* dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="a137f-318">Dažos gadījumos jūs vienkārši vēlaties veikt vaicājumu par preci kopumā.</span><span class="sxs-lookup"><span data-stu-id="a137f-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="a137f-319">Ir divi indeksi, kas definēti kā:</span><span class="sxs-lookup"><span data-stu-id="a137f-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="a137f-320">Tukšas iekavas tiks apkopotas, pamatojoties uz produkta ID nodalījumā.</span><span class="sxs-lookup"><span data-stu-id="a137f-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="a137f-321">Indeksēšana definē, kā varat grupēt rezultātus, pamatojoties uz `groupBy` vaicājuma iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="a137f-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="a137f-322">Šādā gadījumā, ja nedefinējat nevienu `groupBy` vērtību, kopsummas tiks iegūtas pēc `productid`.</span><span class="sxs-lookup"><span data-stu-id="a137f-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="a137f-323">Pretējā gadījumā, ja definējat `groupBy` kā `groupBy=ColorId&groupBy=SizeId`, jūs saņemsiet atpakaļ vairākas rindas, pamatojoties uz atšķirīgām krāsu un izmēru kombinācijām sistēmā.</span><span class="sxs-lookup"><span data-stu-id="a137f-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="a137f-324">Vaicājuma kritērijus var ievietot pieprasījuma pamattekstā.</span><span class="sxs-lookup"><span data-stu-id="a137f-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="a137f-325">Šeit ir parauga vaicājums produktam ar krāsu un izmēru kombināciju.</span><span class="sxs-lookup"><span data-stu-id="a137f-325">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a><span data-ttu-id="a137f-326">Pielāgots mērījums</span><span class="sxs-lookup"><span data-stu-id="a137f-326">Custom measurement</span></span>

<span data-ttu-id="a137f-327">Noklusējuma mērījumu daudzumi ir saistīti ar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a137f-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="a137f-328">Tomēr, iespējams, vēlēsieties daudzumu, kas veidots no noklusēto mērījumu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="a137f-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="a137f-329">Lai to paveiktu, var izveidot pielāgoto daudzumu konfigurāciju, kas tiks pievienota rīcībā esošo vaicājumu izvadei.</span><span class="sxs-lookup"><span data-stu-id="a137f-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="a137f-330">Funkcionalitāte vienkārši ļauj definēt mērvienību kopu, kas tiks pievienota, un/vai mēru kopa, kas tiks atņemta, lai izveidotu pielāgotu mērījumu.</span><span class="sxs-lookup"><span data-stu-id="a137f-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="a137f-331">Piemēram, ar šādu vaicājuma nosacījumu, jūs konfigurēsit pielāgoto mērījumu daudzumu kā `MyCustomAvailableforReservation`, kas tiks patērēts patēriņa sistēmai.</span><span class="sxs-lookup"><span data-stu-id="a137f-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="a137f-332">Patēriņa sistēma</span><span class="sxs-lookup"><span data-stu-id="a137f-332">Consumption system</span></span> | <span data-ttu-id="a137f-333">Aprēķinātie līdzekļi</span><span class="sxs-lookup"><span data-stu-id="a137f-333">Calculated measurers</span></span> | <span data-ttu-id="a137f-334">Datu avots</span><span class="sxs-lookup"><span data-stu-id="a137f-334">Data source</span></span> | <span data-ttu-id="a137f-335">Modifikators</span><span class="sxs-lookup"><span data-stu-id="a137f-335">Modifier</span></span> | <span data-ttu-id="a137f-336">Modifikatora aprēķina tips</span><span class="sxs-lookup"><span data-stu-id="a137f-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="a137f-337">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="a137f-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="a137f-338">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="a137f-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="a137f-339">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="a137f-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="a137f-340">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="a137f-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="a137f-341">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="a137f-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="a137f-342">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="a137f-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="a137f-343">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="a137f-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="a137f-344">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="a137f-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="a137f-345">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="a137f-345">Subtraction</span></span> |

<span data-ttu-id="a137f-346">Ar to vaicājums uz pielāgoto mērījumu daudzumu atgriezīs tālāk norādīto izvadi.</span><span class="sxs-lookup"><span data-stu-id="a137f-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="a137f-347">`MyCustomAvailableforReservation` izvade tiek balstīta uz aprēķina iestatījumu pielāgotos mērījumos kā:</span><span class="sxs-lookup"><span data-stu-id="a137f-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="a137f-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="a137f-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="a137f-349">Rīcībā esošo izmaiņu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="a137f-349">Posting on-hand changes</span></span>

<span data-ttu-id="a137f-350">Precīzais vietrādis URL, uz kuru tiks izlikts pasākums, būs atkarīgs no jūsu ģeogrāfiskā reģiona.</span><span class="sxs-lookup"><span data-stu-id="a137f-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="a137f-351">Tam būs šāds formāts:</span><span class="sxs-lookup"><span data-stu-id="a137f-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="a137f-352">Kad šis vietrādis URL ir autentificēts, to var izmantot kopā ar HTTP `POST` metodi, lai nosūtītu rīcībā esošo izmaiņu notikumus pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="a137f-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="a137f-353">Īpašu galveni izmanto, lai sazinātos ar Dynamics 365 pakalpojumiem, izmantojot HTTP pieprasījumus, kas norāda Supply Chain Management instances vides ID, ar kuru ir saistīti dati.</span><span class="sxs-lookup"><span data-stu-id="a137f-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="a137f-354">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="a137f-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="a137f-355">Iegrāmatošanas rīcībā esošo izmaiņu vaicājums 1. piemērs</span><span class="sxs-lookup"><span data-stu-id="a137f-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="a137f-356">Šajā piemērā ir parādīts scenārijs, kur tiks iestatīta dimensiju konfigurācija risinājumā Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a137f-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="a137f-357">Izmantojiet šo vaicājumu, lai konfigurētu dimensiju kartēšanu risinājumā Power Apps:</span><span class="sxs-lookup"><span data-stu-id="a137f-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="a137f-358">Tagad varat norādīt `dimensionDataSource` un izmantot pielāgotās dimensijas savos vaicājumos.</span><span class="sxs-lookup"><span data-stu-id="a137f-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="a137f-359">Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="a137f-360">Iegrāmatošanas rīcībā esošo izmaiņu vaicājums 2. piemērs</span><span class="sxs-lookup"><span data-stu-id="a137f-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="a137f-361">Šis piemērs rāda scenāriju, kad dimensiju konfigurācijai nav iestatīti kartējumi risinājumā Power Apps, tāpēc grāmatošanai jāizmanto arī pamata dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a137f-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="a137f-362">Ja `dimensionDataSource` lauks ir nulle, tukša vai baltstarpa, visām dimensijām ir jābūt pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="a137f-363">JSON dokumenta lauku rekvizīti</span><span class="sxs-lookup"><span data-stu-id="a137f-363">JSON document field properties</span></span>

<span data-ttu-id="a137f-364">Iepriekš sniegtajos JSON vaicājuma piemēru laukos ir rekvizīti, kas norādīti šajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="a137f-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="a137f-365">Lauka kods</span><span class="sxs-lookup"><span data-stu-id="a137f-365">Field ID</span></span> | <span data-ttu-id="a137f-366">Apraksts</span><span class="sxs-lookup"><span data-stu-id="a137f-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="a137f-367">Unikāls ID noteiktam izmaiņu notikumam.</span><span class="sxs-lookup"><span data-stu-id="a137f-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="a137f-368">Šis ID tiek izmantots, lai nodrošinātu, ka, ja grāmatošanas laikā sakari ar pakalpojumu neizdodas, notikuma atkārtota iesniegšana nenozīmē, ka viens un tas pats notikums sistēmā tiek skaitīts divas reizes.</span><span class="sxs-lookup"><span data-stu-id="a137f-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="a137f-369">Ar notikumu saistītās organizācijas identifikators.</span><span class="sxs-lookup"><span data-stu-id="a137f-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="a137f-370">Tas attiecas uz Supply Chain Management organizācijām vai datu apgabala ID.</span><span class="sxs-lookup"><span data-stu-id="a137f-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="a137f-371">Attiecīgā produkta identifikators.</span><span class="sxs-lookup"><span data-stu-id="a137f-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="a137f-372">Daudzums, par kādu ir jāmaina rīcībā esošais krājums.</span><span class="sxs-lookup"><span data-stu-id="a137f-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="a137f-373">Piemēram, ja plauktam pievienoti 10 jauni beigeļi, šī vērtība ir 10.</span><span class="sxs-lookup"><span data-stu-id="a137f-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="a137f-374">Ja 3 beigeļi tiks noņemti no plaukta vai pārdoti, šī vērtība būs -3.</span><span class="sxs-lookup"><span data-stu-id="a137f-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="a137f-375">Grāmatošanas izmaiņu notikumā un vaicājumā izmantoto dimensiju datu avots.</span><span class="sxs-lookup"><span data-stu-id="a137f-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="a137f-376">Ja norādāt datu avotu, varat izmantot pielāgotās dimensijas no norādītā datu avota.</span><span class="sxs-lookup"><span data-stu-id="a137f-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="a137f-377">Ar dimensiju konfigurāciju Krājumu pārredzamība var kartēt pielāgotās dimensijas uz vispārīgajām noklusējuma dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="a137f-378">Ja `dimensionDataSource` nav norādīts, jūsu vaicājumos var izmantot tikai vispārīgās noklusējuma dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a137f-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="a137f-379">Dinamisks atslēgu/vērtību pāru kopums.</span><span class="sxs-lookup"><span data-stu-id="a137f-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="a137f-380">Tās tiks kartētas uz dažām Supply Chain Management dimensijām, bet varat pievienot arī pielāgotas dimensijas (piemēram *Avotu)*, kas var norādīt, ka notikums tika saņemts no Supply Chain Management vai ārējas sistēmas.</span><span class="sxs-lookup"><span data-stu-id="a137f-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="a137f-381">Pašreizējo rīcībā esošo krājumu vaicājums</span><span class="sxs-lookup"><span data-stu-id="a137f-381">Querying current on-hand</span></span>

<span data-ttu-id="a137f-382">Pašreizējo rīcībā esošo krājumu vaicājuma galapunkts būs līdzīgs vietrādis URL:</span><span class="sxs-lookup"><span data-stu-id="a137f-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="a137f-383">Ar HTTP `POST` metodi tiks veikts vaicājums.</span><span class="sxs-lookup"><span data-stu-id="a137f-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="a137f-384">Pašreizējais rīcībā esošais vaicājums 1. piemērs</span><span class="sxs-lookup"><span data-stu-id="a137f-384">Current on-hand query example 1</span></span>

<span data-ttu-id="a137f-385">Šajā piemērā ir parādīts scenārijs, kurā jau ir iestatīta dimensiju konfigurācija risinājumā Power Apps.</span><span class="sxs-lookup"><span data-stu-id="a137f-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="a137f-386">Izmantojiet šo vaicājumu, lai konfigurētu dimensiju kartēšanu risinājumā Power Apps:</span><span class="sxs-lookup"><span data-stu-id="a137f-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="a137f-387">Tagad varat norādīt `dimensionDataSource` un izmantot pielāgotās dimensijas savos vaicājumos.</span><span class="sxs-lookup"><span data-stu-id="a137f-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="a137f-388">Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="a137f-389">Varat norādīt `DimensionDataSource` `filters` un norādīt pielāgotās dimensijas gan `filters`, gan `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="a137f-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="a137f-390">Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="a137f-391">Pašreizējais rīcībā esošais vaicājums 2. piemērs</span><span class="sxs-lookup"><span data-stu-id="a137f-391">Current on-hand query example 2</span></span>

<span data-ttu-id="a137f-392">Šis piemērs rāda scenāriju, kad dimensiju konfigurācijai nav iestatīti kartējumi risinājumā Power Apps, tāpēc grāmatošanai jāizmanto arī pamata dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a137f-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="a137f-393">Ja `dimensionDataSource` lauks sadaļā `filters` ir nulle, tukšs vai kā atstarpe, visām dimensijām ir jābūt pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="a137f-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="a137f-394">Piemēra atgriešanas rezultāts</span><span class="sxs-lookup"><span data-stu-id="a137f-394">Example return result</span></span>

<span data-ttu-id="a137f-395">Iepriekšējos piemēros parādītie vaicājumi var atgriezt, piemēram, šādu rezultātu.</span><span class="sxs-lookup"><span data-stu-id="a137f-395">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="a137f-396">Ievērojiet, ka daudzuma lauki ir strukturēti kā mērvienību vārdnīca un to saistītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a137f-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
