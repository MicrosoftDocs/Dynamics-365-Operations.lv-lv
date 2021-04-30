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
ms.openlocfilehash: d09c7be5de75511b10d7a69d4b8ac12917b0dbe8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910429"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="0561b-103">Krājumu uztveramības pievienojumprogramma</span><span class="sxs-lookup"><span data-stu-id="0561b-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="0561b-104">Krājumu uztveramības pievienojumprogramma ir neatkarīgs un ļoti mērogojams pakalpojums, kas nodrošina reāllaika rīcībā esošo krājumu izsekošanu, tādējādi sniedzot globālu skatījumu uz krājumu uztveramību.</span><span class="sxs-lookup"><span data-stu-id="0561b-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="0561b-105">Visa informācija, kas saistīta ar rīcībā esošajiem krājumiem, tiek eksportēta uz pakalpojumu gandrīz reāllaikā, izmantojot zema līmeņa SQL integrāciju.</span><span class="sxs-lookup"><span data-stu-id="0561b-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="0561b-106">Ārējās sistēmas piekļūst pakalpojumam, izmantojot RESTful API, lai vaicātu rīcībā esošo informāciju par noteiktajām dimensiju kopām, tādējādi izgūstot pieejamo rīcībā esošo pozīciju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="0561b-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="0561b-107">Krājumu uztveramība ir Microsoft Dataverse iebūvēts pakalpojums, kas nozīmē, ka varat to pagarināt, izveidojot Power Apps un pielietojot Power BI, lai nodrošinātu pielāgotu funkcionalitāti, kas atbilst jūsu biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="0561b-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="0561b-108">Var arī jaunināt indeksu, lai veiktu krājumu vaicājumus.</span><span class="sxs-lookup"><span data-stu-id="0561b-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="0561b-109">Krājumu uztveramība nodrošina konfigurācijas opcijas, kas ļauj to integrēt ar vairākām trešās puses sistēmām.</span><span class="sxs-lookup"><span data-stu-id="0561b-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="0561b-110">Tā atbalsta standartizētu krājumu dimensiju, pielāgoto paplašināšanos un standartizētu, konfigurējamu aprēķināto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="0561b-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="0561b-111">Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt Krājumu uztveramības pievienojumprogrammu Dynamics 365 Supply Chain Management un kā izmantot tās programmas programmēšanas interfeisu (API).</span><span class="sxs-lookup"><span data-stu-id="0561b-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="0561b-112">Instalēt krājumu uztveramības pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="0561b-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="0561b-113">Jums ir jāinstalē Krājumu uztveramības pievienojumprogramma, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0561b-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0561b-114">LCS ir sadarbības portāls, kas nodrošina vides un regulāri atjauninātu pakalpojumu kopu, kas palīdz pārvaldīt jūsu lietojumprogrammu dzīves ciklu Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0561b-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="0561b-115">Papildinformāciju skatiet šeit: [Lifecycle Services resursi](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="0561b-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0561b-116">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="0561b-116">Prerequisites</span></span>

<span data-ttu-id="0561b-117">Pirms instalējat Krājumu uztveramības pievienojumprogrammu, jums ir jādara sekojošais:</span><span class="sxs-lookup"><span data-stu-id="0561b-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="0561b-118">Iegūt LCS ieviešanas projektu, kurā ir vismaz viens izvietošanas vides objekts.</span><span class="sxs-lookup"><span data-stu-id="0561b-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="0561b-119">Pārliecinieties, ka pievienojumprogrammu pārskata iestatīšanas priekšnoteikumi, kas sniegti [Pievienojumprogrammu pārskatā](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) ir pabeigti.</span><span class="sxs-lookup"><span data-stu-id="0561b-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="0561b-120">Krājumu redzamībai nav nepieciešama dubultās rakstīšanas saistīšana.</span><span class="sxs-lookup"><span data-stu-id="0561b-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="0561b-121">Sazinieties ar krājumu redzamības grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu šādus trīs nepieciešamos failus:</span><span class="sxs-lookup"><span data-stu-id="0561b-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="0561b-122">`Inventory Visibility Integration.zip` (Ja jūsu darbinātā Supply Chain Management versija ir agrāka nekā versija 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="0561b-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="0561b-123">Izpildiet sadaļā [Ātrā sākšana: reģistrējiet programmu ar Microsoft identitātes platformu](/azure/active-directory/develop/quickstart-register-app) sniegtās instrukcijas, lai reģistrētu programmu un pievienotu AAD klienta noslēpumu atbilstoši Azure abonementam.</span><span class="sxs-lookup"><span data-stu-id="0561b-123">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
    - [<span data-ttu-id="0561b-124">Lietojumprogrammas reģistrācija</span><span class="sxs-lookup"><span data-stu-id="0561b-124">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
    - [<span data-ttu-id="0561b-125">Pievienot klienta noslēpumu</span><span class="sxs-lookup"><span data-stu-id="0561b-125">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
    - <span data-ttu-id="0561b-126">Opcijas **Programmas (klienta) ID**, **Klienta noslēpums** un **Nomnieka ID** tiks izmantots sekojošās darbībās.</span><span class="sxs-lookup"><span data-stu-id="0561b-126">The **Application(Client) Id**, **Client Secret** and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="0561b-127">Pašlaik atbalstītās valstis un reģioni ietver Kanādu, Amerikas Savienotās Valstis un Eiropas Savienību (ES).</span><span class="sxs-lookup"><span data-stu-id="0561b-127">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="0561b-128">Ja jums ir kādi jautājumi par šiem priekšnosacījumiem, lūdzu, sazinieties ar krājumu redzamības preču darba grupu.</span><span class="sxs-lookup"><span data-stu-id="0561b-128">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="0561b-129">Iestātīt Dataverse</span><span class="sxs-lookup"><span data-stu-id="0561b-129">Set up Dataverse</span></span>

<span data-ttu-id="0561b-130">Lai iestatītu Dataverse, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="0561b-130">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="0561b-131">Pievienojiet pakalpojumu principu savam nomniekam:</span><span class="sxs-lookup"><span data-stu-id="0561b-131">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="0561b-132">Instalējiet Azure AD PowerShell moduli v2, kā aprakstīts [Pakalpojuma Azure Active Directory instalēšana PowerShell grafikam](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="0561b-132">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="0561b-133">Izpildiet šādu PowerShell komandu.</span><span class="sxs-lookup"><span data-stu-id="0561b-133">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="0561b-134">Izveidot programmas lietotāju, lai noteiktu krājumu redzamību Dataverse šeit:</span><span class="sxs-lookup"><span data-stu-id="0561b-134">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="0561b-135">Atveriet Dataverse vides URL.</span><span class="sxs-lookup"><span data-stu-id="0561b-135">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="0561b-136">Dodieties uz **Papildu iestatījumi \> Sistēma \> Drošība \> Lietotāji** un izveidojiet programmas lietotāju.</span><span class="sxs-lookup"><span data-stu-id="0561b-136">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="0561b-137">Izmantojiet skata izvēlni, lai mainītu lapas skatu uz **Programmas lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="0561b-137">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="0561b-138">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0561b-138">Select **New**.</span></span> <span data-ttu-id="0561b-139">Iestatiet Programmas ID uz *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span><span class="sxs-lookup"><span data-stu-id="0561b-139">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="0561b-140">(Saglabājot izmaiņas, objekta ID tiks ielādēts automātiski.) Šo nosaukumu var pielāgot.</span><span class="sxs-lookup"><span data-stu-id="0561b-140">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="0561b-141">Piemēram, to var mainīt uz *Krājumu redzamība*.</span><span class="sxs-lookup"><span data-stu-id="0561b-141">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="0561b-142">Pēc pabeigšanas atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0561b-142">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="0561b-143">Atlasiet **Piešķirt lomu** un pēc tam atlasiet **Sistēmas administrators**.</span><span class="sxs-lookup"><span data-stu-id="0561b-143">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="0561b-144">Ja ir loma ar nosaukumu **Common Data Service Lietotājs**, atlasiet to arī.</span><span class="sxs-lookup"><span data-stu-id="0561b-144">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="0561b-145">Papildinformāciju skatiet nodaļā [Programmas lietotāja izveide](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="0561b-145">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="0561b-146">Ja jūsu noklusētā valoda Dataverse nav **Angļu**:</span><span class="sxs-lookup"><span data-stu-id="0561b-146">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="0561b-147">Pārejiet uz **Papildu iestatījums \> Administrēšana \> Valodas**,</span><span class="sxs-lookup"><span data-stu-id="0561b-147">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="0561b-148">Atlasiet **Angļu (ValodasKods=1033)** un atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="0561b-148">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="0561b-149">Importēt `Inventory Visibility Dataverse Solution.zip` failu, kas ietver Dataverse ar konfigurāciju saistītos elementus un Power Apps:</span><span class="sxs-lookup"><span data-stu-id="0561b-149">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="0561b-150">Doties uz lapu **Risinājumi**.</span><span class="sxs-lookup"><span data-stu-id="0561b-150">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="0561b-151">Atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="0561b-151">Select **Import**.</span></span>

1. <span data-ttu-id="0561b-152">Importēt konfigurācijas jaunināšanas trigera plūsmu:</span><span class="sxs-lookup"><span data-stu-id="0561b-152">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="0561b-153">Doties uz lapu Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="0561b-153">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="0561b-154">Pārliecinieties, vai pastāv savienojums ar nosaukumu *Dataverse (mantojums)*.</span><span class="sxs-lookup"><span data-stu-id="0561b-154">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="0561b-155">(Ja tāda nav, izveidojiet to.)</span><span class="sxs-lookup"><span data-stu-id="0561b-155">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="0561b-156">Importēt `Inventory Visibility Configuration Trigger.zip` failu.</span><span class="sxs-lookup"><span data-stu-id="0561b-156">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="0561b-157">Pēc tā importēšanas trigeris parādīsies zem **Manas plūsmas**.</span><span class="sxs-lookup"><span data-stu-id="0561b-157">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="0561b-158">Inicializējiet tālāk norādītos četrus mainīgos, pamatojoties uz vides informāciju:</span><span class="sxs-lookup"><span data-stu-id="0561b-158">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="0561b-159">Azure nomnieka ID</span><span class="sxs-lookup"><span data-stu-id="0561b-159">Azure Tenant ID</span></span>
        - <span data-ttu-id="0561b-160">Azure Lietojumprogrammas klienta ID</span><span class="sxs-lookup"><span data-stu-id="0561b-160">Azure Application Client ID</span></span>
        - <span data-ttu-id="0561b-161">Azure Lietojumprogrammas klienta noslēpums</span><span class="sxs-lookup"><span data-stu-id="0561b-161">Azure Application Client Secret</span></span>
        - <span data-ttu-id="0561b-162">Krājumu redzamības galapunkts</span><span class="sxs-lookup"><span data-stu-id="0561b-162">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="0561b-163">Papildinformāciju par šo mainīgo skatiet tālāk šīs tēmas sadaļā [Krājumu redzamības integrācijas iestatīšana](#setup-inventory-visibility-integration).</span><span class="sxs-lookup"><span data-stu-id="0561b-163">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="0561b-164">![Konfigurācijas trigeris](media/configuration-trigger.png "Konfigurācijas trigeris")</span><span class="sxs-lookup"><span data-stu-id="0561b-164">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="0561b-165">Atlasiet **Ieslēgt**.</span><span class="sxs-lookup"><span data-stu-id="0561b-165">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="0561b-166">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="0561b-166">Install the add-in</span></span>

<span data-ttu-id="0561b-167">Lai instalētu Krājumu uztveramības pievienojumprogrammu, jums jārīkojas šādi:</span><span class="sxs-lookup"><span data-stu-id="0561b-167">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="0561b-168">Pierakstieties portālā [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="0561b-168">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="0561b-169">Sākumlapā atlasiet projektu, kurā tiek izvietota jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="0561b-169">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="0561b-170">Projekta lapā atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="0561b-170">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="0561b-171">Vides lapā ritiniet uz leju, līdz redzat sadaļu **Vides pievienojumprogrammas** sadaļā **Power Platform integrācija**, kur varat atrast Dataverse vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0561b-171">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="0561b-172">Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="0561b-172">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="0561b-173">![Vides lapa portālā LCS](media/inventory-visibility-environment.png "Vides lapa portālā LCS")</span><span class="sxs-lookup"><span data-stu-id="0561b-173">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="0561b-174">Atlasiet saiti **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="0561b-174">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="0561b-175">Tiek atvērts pieejamo pievienojumprogrammu saraksts.</span><span class="sxs-lookup"><span data-stu-id="0561b-175">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="0561b-176">Atlasiet no saraksta **Krājumu redzamība**.</span><span class="sxs-lookup"><span data-stu-id="0561b-176">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="0561b-177">Ievadiet vērtības savai video šādiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="0561b-177">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="0561b-178">**AAD Lietojumprogrammas (klienta) ID**</span><span class="sxs-lookup"><span data-stu-id="0561b-178">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="0561b-179">**AAD nomnieka ID**</span><span class="sxs-lookup"><span data-stu-id="0561b-179">**AAD tenant ID**</span></span>

    <span data-ttu-id="0561b-180">![Pievienot iestatīšanas lapā](media/inventory-visibility-setup.png "Pievienojumprogrammas iestatīšanas lapa")</span><span class="sxs-lookup"><span data-stu-id="0561b-180">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="0561b-181">Piekrist noteikumiem un nosacījumam, atlasot izvēles rūtiņu **Noteikumi un nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="0561b-181">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="0561b-182">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="0561b-182">Select **Install**.</span></span> <span data-ttu-id="0561b-183">Pievienojumprogrammu statuss tiks rādīts kā **Instalē**.</span><span class="sxs-lookup"><span data-stu-id="0561b-183">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="0561b-184">Kad tas ir izdarīts, atsvaidziniet lapu, lai redzētu statusa maiņu uz **Instalēts**.</span><span class="sxs-lookup"><span data-stu-id="0561b-184">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="0561b-185">Pievienojumprogrammas atinstalēšana</span><span class="sxs-lookup"><span data-stu-id="0561b-185">Uninstall the add-in</span></span>

<span data-ttu-id="0561b-186">Lai atinstalētu pievienojumprogrammu, atlasiet **Atinstalēt**.</span><span class="sxs-lookup"><span data-stu-id="0561b-186">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="0561b-187">Kad atsvaidzināsiet LCS, Krājumu uztveramības pievienojumprogramma tiks noņemta.</span><span class="sxs-lookup"><span data-stu-id="0561b-187">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="0561b-188">Atinstalēšanas process noņems pievienojumprogrammu reģistrāciju un arī sāks darbu, lai notīrītu visus pakalpojumā saglabātos biznesa datus.</span><span class="sxs-lookup"><span data-stu-id="0561b-188">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="0561b-189">Patērēt rīcībā esošos krājumu datus no Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0561b-189">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="0561b-190">Izvietot Krājumu redzamības integrācijas pakotni</span><span class="sxs-lookup"><span data-stu-id="0561b-190">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="0561b-191">Ja jūs palaidāt Supply Chain Management versiju 10.0.17 vai agrāk, sazinieties ar Krājumu redzamības standarta atbalsta komandu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu iepakojuma failu.</span><span class="sxs-lookup"><span data-stu-id="0561b-191">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="0561b-192">Pēc tam izvietojiet pakotni LCS.</span><span class="sxs-lookup"><span data-stu-id="0561b-192">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="0561b-193">Ja izvietošanas laikā rodas versiju neatbilstības kļūda, X++ projekts ir jāimportē manuāli izstrādes vidē.</span><span class="sxs-lookup"><span data-stu-id="0561b-193">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="0561b-194">Pēc tam izveidojiet izvietojamu pakotni savā izstrādes vidē un izvietojiet to ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="0561b-194">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="0561b-195">Kods ir iekļauts Supply Chain Management versijā 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="0561b-195">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="0561b-196">Ja izmantojat šo versiju vai jaunāku, izvietošana nav nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="0561b-196">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="0561b-197">Pārliecinieties, ka jūsu Supply Chain Management vidē ir ieslēgtas šādas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="0561b-197">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="0561b-198">(Pēc noklusējuma tās ir iespējotas.)</span><span class="sxs-lookup"><span data-stu-id="0561b-198">(By default, they are turned on.)</span></span>

| <span data-ttu-id="0561b-199">Līdzekļa apraksts</span><span class="sxs-lookup"><span data-stu-id="0561b-199">Feature description</span></span> | <span data-ttu-id="0561b-200">Koda versija</span><span class="sxs-lookup"><span data-stu-id="0561b-200">Code version</span></span> | <span data-ttu-id="0561b-201">Pārslēgt klasi</span><span class="sxs-lookup"><span data-stu-id="0561b-201">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="0561b-202">Iespējot vai atspējot krājumu dimensiju izmantošana InventSum tabulā</span><span class="sxs-lookup"><span data-stu-id="0561b-202">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="0561b-203">10.0.11</span><span class="sxs-lookup"><span data-stu-id="0561b-203">10.0.11</span></span> | <span data-ttu-id="0561b-204">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="0561b-204">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="0561b-205">Iespējot vai atspējot krājumu dimensiju izmantošana InventSumDelta tabulā</span><span class="sxs-lookup"><span data-stu-id="0561b-205">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="0561b-206">10.0.12</span><span class="sxs-lookup"><span data-stu-id="0561b-206">10.0.12</span></span> | <span data-ttu-id="0561b-207">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="0561b-207">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="0561b-208">Pievienojumprogrammas Krājumu redzamība integrācijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0561b-208">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="0561b-209">Programmā Supply Chain Management atveriet **[Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbvietu un iespējojiet **Krājumu redzamības integrācijas** līdzekli.</span><span class="sxs-lookup"><span data-stu-id="0561b-209">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="0561b-210">Pārejiet uz sadaļu **Krājumu pārvaldība \> Iestatījumi \> Krājumu redzamības integrēšanas parametri** un ievadiet URL, kurā palaižat Krājumu redzamību.</span><span class="sxs-lookup"><span data-stu-id="0561b-210">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="0561b-211">Atrodiet LCS vides Azure reģionu un pēc tam ievadiet vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="0561b-211">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="0561b-212">URL ir šāda veidlapa:</span><span class="sxs-lookup"><span data-stu-id="0561b-212">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="0561b-213">Piemēram, ja esat Eiropā, jūsu videi būs viens no šiem vietrāžiem URL:</span><span class="sxs-lookup"><span data-stu-id="0561b-213">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="0561b-214">Pieejami šādi reģioni.</span><span class="sxs-lookup"><span data-stu-id="0561b-214">The following regions are currently available.</span></span>

    | <span data-ttu-id="0561b-215">Azure reģions</span><span class="sxs-lookup"><span data-stu-id="0561b-215">Azure region</span></span> | <span data-ttu-id="0561b-216">Reģiona īsais nosaukums</span><span class="sxs-lookup"><span data-stu-id="0561b-216">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="0561b-217">Austrālijas austrumi</span><span class="sxs-lookup"><span data-stu-id="0561b-217">Australia east</span></span> | <span data-ttu-id="0561b-218">eau</span><span class="sxs-lookup"><span data-stu-id="0561b-218">eau</span></span> |
    | <span data-ttu-id="0561b-219">Austrālijas dienvidaustrumi</span><span class="sxs-lookup"><span data-stu-id="0561b-219">Australia southeast</span></span> | <span data-ttu-id="0561b-220">seau</span><span class="sxs-lookup"><span data-stu-id="0561b-220">seau</span></span> |
    | <span data-ttu-id="0561b-221">Kanādas centrālā daļā</span><span class="sxs-lookup"><span data-stu-id="0561b-221">Canada central</span></span> | <span data-ttu-id="0561b-222">cca</span><span class="sxs-lookup"><span data-stu-id="0561b-222">cca</span></span> |
    | <span data-ttu-id="0561b-223">Kanādas austrumi</span><span class="sxs-lookup"><span data-stu-id="0561b-223">Canada east</span></span> | <span data-ttu-id="0561b-224">eca</span><span class="sxs-lookup"><span data-stu-id="0561b-224">eca</span></span> |
    | <span data-ttu-id="0561b-225">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="0561b-225">North Europe</span></span> | <span data-ttu-id="0561b-226">neu</span><span class="sxs-lookup"><span data-stu-id="0561b-226">neu</span></span> |
    | <span data-ttu-id="0561b-227">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="0561b-227">West Europe</span></span> | <span data-ttu-id="0561b-228">weu</span><span class="sxs-lookup"><span data-stu-id="0561b-228">weu</span></span> |
    | <span data-ttu-id="0561b-229">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="0561b-229">East US</span></span> | <span data-ttu-id="0561b-230">eus</span><span class="sxs-lookup"><span data-stu-id="0561b-230">eus</span></span> |
    | <span data-ttu-id="0561b-231">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="0561b-231">West US</span></span> | <span data-ttu-id="0561b-232">wus</span><span class="sxs-lookup"><span data-stu-id="0561b-232">wus</span></span> |

1. <span data-ttu-id="0561b-233">Dodieties uz **Krājumu pārvaldība \> Periodiskie \> Krājumu redzamības integrāciju** un iespējojiet darbu.</span><span class="sxs-lookup"><span data-stu-id="0561b-233">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="0561b-234">Visi krājumu izmaiņu notikumi no Supply Chain Management tagad tiks grāmatoti Krājumu redzamībai.</span><span class="sxs-lookup"><span data-stu-id="0561b-234">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="0561b-235">Krājumu redzamības pievienojumprogrammas publiskais API</span><span class="sxs-lookup"><span data-stu-id="0561b-235">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="0561b-236">Krājumu redzamības pievienojumprogrammas publiskais REST API piedāvā vairākus specifiskus integrācijas galapunktus.</span><span class="sxs-lookup"><span data-stu-id="0561b-236">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="0561b-237">Tas atbalsta trīs galvenos mijiedarbības tipus:</span><span class="sxs-lookup"><span data-stu-id="0561b-237">It supports three main interaction types:</span></span>

- <span data-ttu-id="0561b-238">Iegrāmatojot pievienojumprogrammas rīcībā esošās izmaiņas no ārējās sistēmas</span><span class="sxs-lookup"><span data-stu-id="0561b-238">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="0561b-239">Tiek vaicāti pašreizējie rīcībā esošie daudzumi no ārējās sistēmas</span><span class="sxs-lookup"><span data-stu-id="0561b-239">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="0561b-240">Automātiska sinhronizācija ar Supply Chain Management rīcībā esošiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="0561b-240">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="0561b-241">Automātiskā sinhronizācija nav daļa no publiskā API.</span><span class="sxs-lookup"><span data-stu-id="0561b-241">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="0561b-242">Tā vietā tā tiek apstrādāta fonā vidēm, kurās ir iespējota krājumu redzamības pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="0561b-242">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="0561b-243">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="0561b-243">Authentication</span></span>

<span data-ttu-id="0561b-244">Platformas drošības marķieris tiek izmantots, lai izsauktu Krājumu redzamības pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="0561b-244">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="0561b-245">Tāpēc, izmantojot programmu, ir jāizveido *Azure Active Directory (Azure AD) marķieris* ar Azure AD lietotni.</span><span class="sxs-lookup"><span data-stu-id="0561b-245">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="0561b-246">Pēc tam ir jāizmanto Azure AD marķieris, lai iegūtu *piekļuves pilnvaras* no drošības pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="0561b-246">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="0561b-247">Lai iegūtu drošības pakalpojuma pilnvaru, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="0561b-247">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="0561b-248">Pieteikties Azure portālā un izmantot to, lai atrastu `clientId` un `clientSecret` savai Supply Chain Management programmai.</span><span class="sxs-lookup"><span data-stu-id="0561b-248">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="0561b-249">Panest marķieri Azure Active Directory (`aadToken`), iesniedzot HTTP pieprasījumu ar šādiem rekvizītiem:</span><span class="sxs-lookup"><span data-stu-id="0561b-249">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="0561b-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="0561b-250">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="0561b-251">**Metode** - `GET`</span><span class="sxs-lookup"><span data-stu-id="0561b-251">**Method** - `GET`</span></span>
    - <span data-ttu-id="0561b-252">**Pamatteksta saturs (formas dati)**:</span><span class="sxs-lookup"><span data-stu-id="0561b-252">**Body content (form data)**:</span></span>

        | <span data-ttu-id="0561b-253">key</span><span class="sxs-lookup"><span data-stu-id="0561b-253">key</span></span> | <span data-ttu-id="0561b-254">vērtība</span><span class="sxs-lookup"><span data-stu-id="0561b-254">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="0561b-255">client_id</span><span class="sxs-lookup"><span data-stu-id="0561b-255">client_id</span></span> | <span data-ttu-id="0561b-256">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="0561b-256">${aadAppId}</span></span> |
        | <span data-ttu-id="0561b-257">client_secret</span><span class="sxs-lookup"><span data-stu-id="0561b-257">client_secret</span></span> | <span data-ttu-id="0561b-258">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="0561b-258">${aadAppSecret}</span></span> |
        | <span data-ttu-id="0561b-259">grant_type</span><span class="sxs-lookup"><span data-stu-id="0561b-259">grant_type</span></span> | <span data-ttu-id="0561b-260">client_credentials</span><span class="sxs-lookup"><span data-stu-id="0561b-260">client_credentials</span></span> |
        | <span data-ttu-id="0561b-261">resource</span><span class="sxs-lookup"><span data-stu-id="0561b-261">resource</span></span> | <span data-ttu-id="0561b-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="0561b-262">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="0561b-263">Jums jāsaņem `aadToken` atbilde, kas ir līdzīga šim piemēram.</span><span class="sxs-lookup"><span data-stu-id="0561b-263">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="0561b-264">Formulējiet JSON pieprasījumu, kas ir līdzīgs šim:</span><span class="sxs-lookup"><span data-stu-id="0561b-264">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="0561b-265">Kur:</span><span class="sxs-lookup"><span data-stu-id="0561b-265">Where:</span></span>
    - <span data-ttu-id="0561b-266">Vērtībai `client_assertion` jābūt `aadToken` tai, kas saņemta iepriekšējā solī.</span><span class="sxs-lookup"><span data-stu-id="0561b-266">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="0561b-267">Vērtībai `context` ir jābūt vides ID, kur vēlaties izvietot pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="0561b-267">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="0561b-268">Iestatiet visas citas vērtības, kā parādītas piemērā.</span><span class="sxs-lookup"><span data-stu-id="0561b-268">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="0561b-269">Iesniedziet HTTP pieprasījumu ar šādiem rekvizītiem:</span><span class="sxs-lookup"><span data-stu-id="0561b-269">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="0561b-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="0561b-270">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="0561b-271">**Metode** - `POST`</span><span class="sxs-lookup"><span data-stu-id="0561b-271">**Method** - `POST`</span></span>
    - <span data-ttu-id="0561b-272">**HTTP virsraksts** - iekļaut API versiju (atslēga ir `Api-Version` un vērtība ir `1.0`)</span><span class="sxs-lookup"><span data-stu-id="0561b-272">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="0561b-273">**Pamatteksts** - iekļaut JSON pieprasījumu, ko izveidojāt iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="0561b-273">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="0561b-274">`access_token` jūs saņemsiet atbildē.</span><span class="sxs-lookup"><span data-stu-id="0561b-274">You will get an `access_token` in response.</span></span> <span data-ttu-id="0561b-275">Tas ir tas, kas jums nepieciešams kā nesēja marķieris, lai izsauktu krājumu redzamības API.</span><span class="sxs-lookup"><span data-stu-id="0561b-275">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="0561b-276">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="0561b-276">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="0561b-277">Pieprasījuma paraugs</span><span class="sxs-lookup"><span data-stu-id="0561b-277">Sample Request</span></span>

<span data-ttu-id="0561b-278">Jūsu atsaucei šeit ir http pieprasījuma paraugs, jūs varat izmantot jebkuru rīku vai kodēšanas valodu, lai nosūtītu šo pieprasījumu, piemēram,  ``Postman``.</span><span class="sxs-lookup"><span data-stu-id="0561b-278">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="0561b-279">Konfigurēt krājumu uztveramības API</span><span class="sxs-lookup"><span data-stu-id="0561b-279">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="0561b-280">Pirms pakalpojuma izmantošanas ir jāpabeidz konfigurācijas, kas aprakstītas sekojošās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="0561b-280">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="0561b-281">Konfigurācija var atšķirties atkarībā no jūsu vides datiem.</span><span class="sxs-lookup"><span data-stu-id="0561b-281">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="0561b-282">Tā galvenokārt ietver četras daļas:</span><span class="sxs-lookup"><span data-stu-id="0561b-282">It primarily includes four parts:</span></span>

- [<span data-ttu-id="0561b-283">Sadalīšana</span><span class="sxs-lookup"><span data-stu-id="0561b-283">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="0561b-284">Dimensiju konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="0561b-284">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="0561b-285">Indeksācija</span><span class="sxs-lookup"><span data-stu-id="0561b-285">Indexing</span></span>](#indexing)
- [<span data-ttu-id="0561b-286">Pielāgots mērījums</span><span class="sxs-lookup"><span data-stu-id="0561b-286">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="0561b-287">Sadalīšana</span><span class="sxs-lookup"><span data-stu-id="0561b-287">Partitioning</span></span>

<span data-ttu-id="0561b-288">Sadalīšana var būtiski ietekmēt Krājumu uztveramības API veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="0561b-288">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="0561b-289">Ir ieteicams definēt shēmu, kas ļauj izmantot mazus datu grupējumus, vienlaikus atļaujot jēgpilnus datu vaicājumus.</span><span class="sxs-lookup"><span data-stu-id="0561b-289">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="0561b-290">`organizationId` (`dataAreaId` Supply Chain Management) vienmēr būs daļa no sadalīšanas, un pēc noklusējuma Krājumu uztveramība ir iestatīta uz sadalījumu pēc dimensijām kā *Vietne + Atrašanās vieta*.</span><span class="sxs-lookup"><span data-stu-id="0561b-290">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="0561b-291">Tas nozīmē, ka pakalpojumi vienmēr ir jāvaicā ar šīm filtriem definētajām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-291">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="0561b-292">*Vietne* un *Atrašanās vieta* ir divas galvenās noklusējuma dimensijas Krājumu uztveramībai.</span><span class="sxs-lookup"><span data-stu-id="0561b-292">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="0561b-293">Supply Chain Management šīs dimensijas tiek sauktas par *Vietni* (`InventSiteId`) un *Noliktavu* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="0561b-293">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="0561b-294">Dimensiju konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="0561b-294">Dimension configurations</span></span>

<span data-ttu-id="0561b-295">Krājumu uztveramība nodrošinās vispārēju noklusējuma dimensiju sarakstu, lai iespējotu vairāku avotu sistēmu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="0561b-295">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="0561b-296">Sekojošajā tabulā ir minētas krājumu dimensijas, kas būs noklusējuma dimensiju nosaukumi Krājumu uztveramībai.</span><span class="sxs-lookup"><span data-stu-id="0561b-296">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="0561b-297">Dimensiju veids</span><span class="sxs-lookup"><span data-stu-id="0561b-297">Dimension type</span></span> | <span data-ttu-id="0561b-298">Dimensijas nosaukums</span><span class="sxs-lookup"><span data-stu-id="0561b-298">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="0561b-299">Produkts</span><span class="sxs-lookup"><span data-stu-id="0561b-299">Product</span></span> | `ColorId` |
| <span data-ttu-id="0561b-300">Produkts</span><span class="sxs-lookup"><span data-stu-id="0561b-300">Product</span></span> | `SizeId` |
| <span data-ttu-id="0561b-301">Produkts</span><span class="sxs-lookup"><span data-stu-id="0561b-301">Product</span></span> | `StyleId` |
| <span data-ttu-id="0561b-302">Produkts</span><span class="sxs-lookup"><span data-stu-id="0561b-302">Product</span></span> | `ConfigId` |
| <span data-ttu-id="0561b-303">Izsekošana</span><span class="sxs-lookup"><span data-stu-id="0561b-303">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="0561b-304">Izsekošana</span><span class="sxs-lookup"><span data-stu-id="0561b-304">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="0561b-305">Novietojums</span><span class="sxs-lookup"><span data-stu-id="0561b-305">Location</span></span> | `LocationId` |
| <span data-ttu-id="0561b-306">Novietojums</span><span class="sxs-lookup"><span data-stu-id="0561b-306">Location</span></span> | `SiteId` |
| <span data-ttu-id="0561b-307">Krājumu statuss</span><span class="sxs-lookup"><span data-stu-id="0561b-307">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="0561b-308">Specifiska noliktava</span><span class="sxs-lookup"><span data-stu-id="0561b-308">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="0561b-309">Specifiska noliktava</span><span class="sxs-lookup"><span data-stu-id="0561b-309">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="0561b-310">Specifiska noliktava</span><span class="sxs-lookup"><span data-stu-id="0561b-310">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="0561b-311">Dimensijas tips, kas norādīts iepriekšējā tabulā, ir tikai atsaucei.</span><span class="sxs-lookup"><span data-stu-id="0561b-311">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="0561b-312">Nav nepieciešams definēt dimensijas tipu Krājumu uztveramībai.</span><span class="sxs-lookup"><span data-stu-id="0561b-312">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="0561b-313">Ja pielāgota dimensija pastāv un tai ir jāplūst uz noklusēto vērtību, kad to patērē Krājuma uztveramība, varat konfigurēt **Pielāgoto dimensiju** nosaukumu Krājuma uztveramībā.</span><span class="sxs-lookup"><span data-stu-id="0561b-313">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="0561b-314">Ārējās sistēmas piekļūst Krājumu uztveramībai, izmantojot REST API, kas iespējo rīcībā esošo informāciju par norādītajām dimensiju kopām.</span><span class="sxs-lookup"><span data-stu-id="0561b-314">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="0561b-315">Lai to izdarītu, Krājumu uztveramība ļauj konfigurēt *ārējā kanāla datu avotu* un avota dimensiju uz *mērķa dimensijām* Krājumu uztveramībā.</span><span class="sxs-lookup"><span data-stu-id="0561b-315">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="0561b-316">Mērķa dimensijām jābūt vienai no sekojošajām:</span><span class="sxs-lookup"><span data-stu-id="0561b-316">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="0561b-317">Noklusētās dimensijas Krājumu pārredzamībai</span><span class="sxs-lookup"><span data-stu-id="0561b-317">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="0561b-318">Pielāgotas dimensijas</span><span class="sxs-lookup"><span data-stu-id="0561b-318">Custom dimensions</span></span>

<span data-ttu-id="0561b-319">Dimensijas konfigurācijas nolūks ir standartizēt vairāku sistēmu integrāciju vaicājumam dimensijās un grāmatošanas notikumā ar dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-319">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="0561b-320">Indeksācija</span><span class="sxs-lookup"><span data-stu-id="0561b-320">Indexing</span></span>

<span data-ttu-id="0561b-321">Vairākumā gadījumu rīcībā esošie krājumi būs ne tikai visaugstākajā "kopējā" līmenī, bet, iespējams, vēlēsities apskatīt apkopotos rezultātus, pamatojoties uz krājumu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-321">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="0561b-322">Krājumu pārredzamība nodrošina elastību, ļaujot iestatīt indeksus, kas ir balstīti uz dimensiju vai dimensiju kombināciju.</span><span class="sxs-lookup"><span data-stu-id="0561b-322">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="0561b-323">Pašlaik varat konfigurēt tikai līdz pieciem indeksiem.</span><span class="sxs-lookup"><span data-stu-id="0561b-323">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="0561b-324">Jums ir rūpīgi jāapsver, kuru dimensiju vai dimensiju kombināciju izmantosiet pirms ieviešanas, lai nodrošinātu, ka tā atbilst jūsu biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="0561b-324">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="0561b-325">Piemēram, ja vēlaties vaicāt preces šādi:</span><span class="sxs-lookup"><span data-stu-id="0561b-325">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="0561b-326">Vaicāt apkopotos rīcībā esošos produktus pēc *Krāsas* un *Izmēra* dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-326">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="0561b-327">Dažos gadījumos jūs vienkārši vēlaties veikt vaicājumu par preci kopumā.</span><span class="sxs-lookup"><span data-stu-id="0561b-327">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="0561b-328">Ir divi indeksi, kas definēti kā:</span><span class="sxs-lookup"><span data-stu-id="0561b-328">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="0561b-329">Tukšas iekavas tiks apkopotas, pamatojoties uz produkta ID nodalījumā.</span><span class="sxs-lookup"><span data-stu-id="0561b-329">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="0561b-330">Indeksēšana definē, kā varat grupēt rezultātus, pamatojoties uz `groupBy` vaicājuma iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="0561b-330">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="0561b-331">Šādā gadījumā, ja nedefinējat nevienu `groupBy` vērtību, kopsummas tiks iegūtas pēc `productid`.</span><span class="sxs-lookup"><span data-stu-id="0561b-331">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="0561b-332">Pretējā gadījumā, ja definējat `groupBy` kā `groupBy=ColorId&groupBy=SizeId`, jūs saņemsiet atpakaļ vairākas rindas, pamatojoties uz atšķirīgām krāsu un izmēru kombinācijām sistēmā.</span><span class="sxs-lookup"><span data-stu-id="0561b-332">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="0561b-333">Vaicājuma kritērijus var ievietot pieprasījuma pamattekstā.</span><span class="sxs-lookup"><span data-stu-id="0561b-333">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="0561b-334">Šeit ir parauga vaicājums produktam ar krāsu un izmēru kombināciju.</span><span class="sxs-lookup"><span data-stu-id="0561b-334">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="0561b-335">Laukam `filters` pašreiz tikai `ProductId` atbalsta vairākas vērtības.</span><span class="sxs-lookup"><span data-stu-id="0561b-335">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="0561b-336">Ja `ProductId` masīvs ir tukšs, tiks pieprasīti visi produkti.</span><span class="sxs-lookup"><span data-stu-id="0561b-336">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="0561b-337">Pielāgots mērījums</span><span class="sxs-lookup"><span data-stu-id="0561b-337">Custom measurement</span></span>

<span data-ttu-id="0561b-338">Noklusējuma mērījumu daudzumi ir saistīti ar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0561b-338">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="0561b-339">Tomēr, iespējams, vēlēsieties daudzumu, kas veidots no noklusēto mērījumu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="0561b-339">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="0561b-340">Lai to paveiktu, var izveidot pielāgoto daudzumu konfigurāciju, kas tiks pievienota rīcībā esošo vaicājumu izvadei.</span><span class="sxs-lookup"><span data-stu-id="0561b-340">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="0561b-341">Funkcionalitāte vienkārši ļauj definēt mērvienību kopu, kas tiks pievienota, un/vai mēru kopa, kas tiks atņemta, lai izveidotu pielāgotu mērījumu.</span><span class="sxs-lookup"><span data-stu-id="0561b-341">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="0561b-342">Piemēram, ar šādu vaicājuma nosacījumu, jūs konfigurēsit pielāgoto mērījumu daudzumu kā `MyCustomAvailableforReservation`, kas tiks patērēts patēriņa sistēmai.</span><span class="sxs-lookup"><span data-stu-id="0561b-342">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="0561b-343">Patēriņa sistēma</span><span class="sxs-lookup"><span data-stu-id="0561b-343">Consumption system</span></span> | <span data-ttu-id="0561b-344">Aprēķinātie līdzekļi</span><span class="sxs-lookup"><span data-stu-id="0561b-344">Calculated measurers</span></span> | <span data-ttu-id="0561b-345">Datu avots</span><span class="sxs-lookup"><span data-stu-id="0561b-345">Data source</span></span> | <span data-ttu-id="0561b-346">Modifikators</span><span class="sxs-lookup"><span data-stu-id="0561b-346">Modifier</span></span> | <span data-ttu-id="0561b-347">Modifikatora aprēķina tips</span><span class="sxs-lookup"><span data-stu-id="0561b-347">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="0561b-348">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="0561b-348">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="0561b-349">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="0561b-349">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="0561b-350">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="0561b-350">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="0561b-351">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="0561b-351">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="0561b-352">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="0561b-352">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="0561b-353">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="0561b-353">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="0561b-354">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="0561b-354">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="0561b-355">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="0561b-355">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="0561b-356">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="0561b-356">Subtraction</span></span> |

<span data-ttu-id="0561b-357">Ar to vaicājums uz pielāgoto mērījumu daudzumu atgriezīs tālāk norādīto izvadi.</span><span class="sxs-lookup"><span data-stu-id="0561b-357">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="0561b-358">`MyCustomAvailableforReservation` izvade tiek balstīta uz aprēķina iestatījumu pielāgotos mērījumos kā:</span><span class="sxs-lookup"><span data-stu-id="0561b-358">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="0561b-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="0561b-359">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="0561b-360">Rīcībā esošo izmaiņu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="0561b-360">Posting on-hand changes</span></span>

<span data-ttu-id="0561b-361">Precīzais vietrādis URL, uz kuru tiks izlikts pasākums, būs atkarīgs no jūsu ģeogrāfiskā reģiona.</span><span class="sxs-lookup"><span data-stu-id="0561b-361">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="0561b-362">Tam būs šāds formāts:</span><span class="sxs-lookup"><span data-stu-id="0561b-362">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="0561b-363">Kad šis vietrādis URL ir autentificēts, to var izmantot kopā ar HTTP `POST` metodi, lai nosūtītu rīcībā esošo izmaiņu notikumus pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="0561b-363">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="0561b-364">Īpašu galveni izmanto, lai sazinātos ar Dynamics 365 pakalpojumiem, izmantojot HTTP pieprasījumus, kas norāda Supply Chain Management instances vides ID, ar kuru ir saistīti dati.</span><span class="sxs-lookup"><span data-stu-id="0561b-364">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="0561b-365">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="0561b-365">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="0561b-366">Iegrāmatošanas rīcībā esošo izmaiņu vaicājums 1. piemērs</span><span class="sxs-lookup"><span data-stu-id="0561b-366">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="0561b-367">Šajā piemērā ir parādīts scenārijs, kur tiks iestatīta dimensiju konfigurācija risinājumā Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0561b-367">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0561b-368">Izmantojiet šo vaicājumu, lai konfigurētu dimensiju kartēšanu risinājumā Power Apps:</span><span class="sxs-lookup"><span data-stu-id="0561b-368">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0561b-369">Tagad varat norādīt `dimensionDataSource` un izmantot pielāgotās dimensijas savos vaicājumos.</span><span class="sxs-lookup"><span data-stu-id="0561b-369">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0561b-370">Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-370">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="0561b-371">Iegrāmatošanas rīcībā esošo izmaiņu vaicājums 2. piemērs</span><span class="sxs-lookup"><span data-stu-id="0561b-371">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="0561b-372">Šis piemērs rāda scenāriju, kad dimensiju konfigurācijai nav iestatīti kartējumi risinājumā Power Apps, tāpēc grāmatošanai jāizmanto arī pamata dimensijas.</span><span class="sxs-lookup"><span data-stu-id="0561b-372">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0561b-373">Ja `dimensionDataSource` lauks ir nulle, tukša vai baltstarpa, visām dimensijām ir jābūt pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-373">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="0561b-374">JSON dokumenta lauku rekvizīti</span><span class="sxs-lookup"><span data-stu-id="0561b-374">JSON document field properties</span></span>

<span data-ttu-id="0561b-375">Iepriekš sniegtajos JSON vaicājuma piemēru laukos ir rekvizīti, kas norādīti šajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="0561b-375">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="0561b-376">Lauka kods</span><span class="sxs-lookup"><span data-stu-id="0561b-376">Field ID</span></span> | <span data-ttu-id="0561b-377">Apraksts</span><span class="sxs-lookup"><span data-stu-id="0561b-377">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="0561b-378">Unikāls ID noteiktam izmaiņu notikumam.</span><span class="sxs-lookup"><span data-stu-id="0561b-378">A unique ID for the specific change event.</span></span> <span data-ttu-id="0561b-379">Šis ID tiek izmantots, lai nodrošinātu, ka, ja grāmatošanas laikā sakari ar pakalpojumu neizdodas, notikuma atkārtota iesniegšana nenozīmē, ka viens un tas pats notikums sistēmā tiek skaitīts divas reizes.</span><span class="sxs-lookup"><span data-stu-id="0561b-379">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="0561b-380">Ar notikumu saistītās organizācijas identifikators.</span><span class="sxs-lookup"><span data-stu-id="0561b-380">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="0561b-381">Tas attiecas uz Supply Chain Management organizācijām vai datu apgabala ID.</span><span class="sxs-lookup"><span data-stu-id="0561b-381">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="0561b-382">Attiecīgā produkta identifikators.</span><span class="sxs-lookup"><span data-stu-id="0561b-382">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="0561b-383">Daudzums, par kādu ir jāmaina rīcībā esošais krājums.</span><span class="sxs-lookup"><span data-stu-id="0561b-383">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="0561b-384">Piemēram, ja plauktam pievienoti 10 jauni beigeļi, šī vērtība ir 10.</span><span class="sxs-lookup"><span data-stu-id="0561b-384">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="0561b-385">Ja 3 beigeļi tiks noņemti no plaukta vai pārdoti, šī vērtība būs -3.</span><span class="sxs-lookup"><span data-stu-id="0561b-385">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="0561b-386">Grāmatošanas izmaiņu notikumā un vaicājumā izmantoto dimensiju datu avots.</span><span class="sxs-lookup"><span data-stu-id="0561b-386">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="0561b-387">Ja norādāt datu avotu, varat izmantot pielāgotās dimensijas no norādītā datu avota.</span><span class="sxs-lookup"><span data-stu-id="0561b-387">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="0561b-388">Ar dimensiju konfigurāciju Krājumu pārredzamība var kartēt pielāgotās dimensijas uz vispārīgajām noklusējuma dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-388">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="0561b-389">Ja `dimensionDataSource` nav norādīts, jūsu vaicājumos var izmantot tikai vispārīgās noklusējuma dimensijas.</span><span class="sxs-lookup"><span data-stu-id="0561b-389">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="0561b-390">Dinamisks atslēgu/vērtību pāru kopums.</span><span class="sxs-lookup"><span data-stu-id="0561b-390">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="0561b-391">Tās tiks kartētas uz dažām Supply Chain Management dimensijām, bet varat pievienot arī pielāgotas dimensijas (piemēram *Avotu)*, kas var norādīt, ka notikums tika saņemts no Supply Chain Management vai ārējas sistēmas.</span><span class="sxs-lookup"><span data-stu-id="0561b-391">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="0561b-392">Pašreizējo rīcībā esošo krājumu vaicājums</span><span class="sxs-lookup"><span data-stu-id="0561b-392">Querying current on-hand</span></span>

<span data-ttu-id="0561b-393">Pašreizējo rīcībā esošo krājumu vaicājuma galapunkts būs līdzīgs vietrādis URL:</span><span class="sxs-lookup"><span data-stu-id="0561b-393">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="0561b-394">Ar HTTP `POST` metodi tiks veikts vaicājums.</span><span class="sxs-lookup"><span data-stu-id="0561b-394">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="0561b-395">Pašreizējais rīcībā esošais vaicājums 1. piemērs</span><span class="sxs-lookup"><span data-stu-id="0561b-395">Current on-hand query example 1</span></span>

<span data-ttu-id="0561b-396">Šajā piemērā ir parādīts scenārijs, kurā jau ir iestatīta dimensiju konfigurācija risinājumā Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0561b-396">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="0561b-397">Izmantojiet šo vaicājumu, lai konfigurētu dimensiju kartēšanu risinājumā Power Apps:</span><span class="sxs-lookup"><span data-stu-id="0561b-397">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="0561b-398">Tagad varat norādīt `dimensionDataSource` un izmantot pielāgotās dimensijas savos vaicājumos.</span><span class="sxs-lookup"><span data-stu-id="0561b-398">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="0561b-399">Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-399">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="0561b-400">Varat norādīt `DimensionDataSource` `filters` un norādīt pielāgotās dimensijas gan `filters`, gan `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="0561b-400">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="0561b-401">Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-401">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="0561b-402">Pašreizējais rīcībā esošais vaicājums 2. piemērs</span><span class="sxs-lookup"><span data-stu-id="0561b-402">Current on-hand query example 2</span></span>

<span data-ttu-id="0561b-403">Šis piemērs rāda scenāriju, kad dimensiju konfigurācijai nav iestatīti kartējumi risinājumā Power Apps, tāpēc grāmatošanai jāizmanto arī pamata dimensijas.</span><span class="sxs-lookup"><span data-stu-id="0561b-403">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="0561b-404">Ja `dimensionDataSource` lauks sadaļā `filters` ir nulle, tukšs vai kā atstarpe, visām dimensijām ir jābūt pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="0561b-404">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="0561b-405">Piemēra atgriešanas rezultāts</span><span class="sxs-lookup"><span data-stu-id="0561b-405">Example return result</span></span>

<span data-ttu-id="0561b-406">Iepriekšējos piemēros parādītie vaicājumi var atgriezt, piemēram, šādu rezultātu.</span><span class="sxs-lookup"><span data-stu-id="0561b-406">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="0561b-407">Ievērojiet, ka daudzuma lauki ir strukturēti kā mērvienību vārdnīca un to saistītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="0561b-407">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]