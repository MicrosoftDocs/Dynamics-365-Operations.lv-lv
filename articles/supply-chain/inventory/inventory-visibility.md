---
title: Krājumu uztveramības pievienojumprogramma
description: Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt krājumu uztveramības pievienojumprogrammu sistēmai Dynamics 365 Supply Chain Management.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625069"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="4391b-103">Krājumu uztveramības pievienojumprogramma</span><span class="sxs-lookup"><span data-stu-id="4391b-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4391b-104">Krājumu uztveramības pievienojumprogramma ir neatkarīgs un ļoti mērogojams pakalpojums, kas nodrošina reāllaika rīcībā esošo krājumu izsekošanu, tādējādi sniedzot globālu skatījumu uz krājumu uztveramību.</span><span class="sxs-lookup"><span data-stu-id="4391b-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="4391b-105">Visa informācija, kas saistīta ar rīcībā esošajiem krājumiem, tiek eksportēta uz pakalpojumu gandrīz reāllaikā, izmantojot zema līmeņa SQL integrāciju.</span><span class="sxs-lookup"><span data-stu-id="4391b-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="4391b-106">Ārējās sistēmas piekļūst pakalpojumam, izmantojot RESTful API, lai vaicātu rīcībā esošo informāciju par noteiktajām dimensiju kopām, tādējādi izgūstot pieejamo rīcībā esošo pozīciju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="4391b-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="4391b-107">Krājumu uztveramība ir Common Data Service iebūvēts pakalpojums, kas nozīmē, ka varat to pagarināt, izveidojot Power Apps un pielietojot Power BI, lai nodrošinātu pielāgotu funkcionalitāti, kas atbilst jūsu biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="4391b-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="4391b-108">Var arī jaunināt indeksu, lai veiktu krājumu vaicājumus.</span><span class="sxs-lookup"><span data-stu-id="4391b-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="4391b-109">Krājumu uztveramība nodrošina konfigurācijas opcijas, kas ļauj to integrēt ar vairākām trešās puses sistēmām.</span><span class="sxs-lookup"><span data-stu-id="4391b-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="4391b-110">Tā atbalsta standartizētu krājumu dimensiju, pielāgoto paplašināšanos un standartizētu, konfigurējamu aprēķināto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="4391b-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="4391b-111">Šajā tēmā ir aprakstīts, kā instalēt un konfigurēt Krājumu uztveramības pievienojumprogrammu Dynamics 365 Supply Chain Management un kā izmantot tās programmas programmēšanas interfeisu (API).</span><span class="sxs-lookup"><span data-stu-id="4391b-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="4391b-112">Instalēt krājumu uztveramības pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="4391b-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="4391b-113">Jums ir jāinstalē Krājumu uztveramības pievienojumprogramma, izmantojot Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4391b-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4391b-114">LCS ir sadarbības portāls, kas nodrošina vides un regulāri atjauninātu pakalpojumu kopu, kas palīdz pārvaldīt jūsu lietojumprogrammu dzīves ciklu Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4391b-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="4391b-115">Papildinformāciju skatiet šeit: [Lifecycle Services resursi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="4391b-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4391b-116">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="4391b-116">Prerequisites</span></span>

<span data-ttu-id="4391b-117">Pirms instalējat Krājumu uztveramības pievienojumprogrammu, jums ir jādara sekojošais:</span><span class="sxs-lookup"><span data-stu-id="4391b-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="4391b-118">Iegūt LCS ieviešanas projektu, kurā ir vismaz viens izvietošanas vides objekts.</span><span class="sxs-lookup"><span data-stu-id="4391b-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="4391b-119">Ģenerējiet sava piedāvājuma beta atslēgas LCS.</span><span class="sxs-lookup"><span data-stu-id="4391b-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="4391b-120">Iespējojiet beta atslēgas savam piedāvājumam savam lietotājam LCS.</span><span class="sxs-lookup"><span data-stu-id="4391b-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="4391b-121">Sazinieties ar Microsoft krājumu redzamības preču darba grupu un norādiet vides ID, kur vēlaties izvietot krājumu uztveramības pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="4391b-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="4391b-122">Ja jums ir kādi jautājumi par šiem priekšnosacījumiem, lūdzu, sazinieties ar krājumu redzamības preču darba grupu.</span><span class="sxs-lookup"><span data-stu-id="4391b-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="4391b-123">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="4391b-123">Install the add-in</span></span>

<span data-ttu-id="4391b-124">Lai instalētu Krājumu uztveramības pievienojumprogrammu, jums jārīkojas šādi:</span><span class="sxs-lookup"><span data-stu-id="4391b-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="4391b-125">Pierakstieties portālā [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="4391b-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="4391b-126">Sākumlapā atlasiet projektu, kurā tiek izvietota jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="4391b-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="4391b-127">Projekta lapā atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="4391b-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="4391b-128">Vides lapā ritiniet uz leju, līdz redzat sadaļu **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="4391b-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="4391b-129">Ja sadaļa nav redzama, pārliecinieties, vai ir pilnībā apstrādātas priekšnosacījumu beta atslēgas.</span><span class="sxs-lookup"><span data-stu-id="4391b-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="4391b-130">Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="4391b-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="4391b-131">![Vides lapa portālā LCS](media/inventory-visibility-environment.png "Vides lapa portālā LCS")</span><span class="sxs-lookup"><span data-stu-id="4391b-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="4391b-132">Atlasiet saiti **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="4391b-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="4391b-133">Tiek atvērts pieejamo pievienojumprogrammu saraksts.</span><span class="sxs-lookup"><span data-stu-id="4391b-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="4391b-134">Sarakstā atlasiet **Krājumu pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="4391b-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="4391b-135">(Ņemiet vērā, ka tagad to var uzskaitīt kā **Krājumu uztveramības pievienojumprogramma sistēmai Dynamics 365 Supply Chain Management**.)</span><span class="sxs-lookup"><span data-stu-id="4391b-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="4391b-136">Ievadiet vērtības savai video šādiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="4391b-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="4391b-137">**AAD lietojumprogrammas ID**</span><span class="sxs-lookup"><span data-stu-id="4391b-137">**AAD application ID**</span></span>
    - <span data-ttu-id="4391b-138">**AAD nomnieka ID**</span><span class="sxs-lookup"><span data-stu-id="4391b-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="4391b-139">![Pievienot iestatīšanas lapā](media/inventory-visibility-setup.png "Pievienojumprogrammas iestatīšanas lapa")</span><span class="sxs-lookup"><span data-stu-id="4391b-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="4391b-140">Piekrist noteikumiem un nosacījumam, atlasot izvēles rūtiņu **Noteikumi un nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="4391b-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="4391b-141">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="4391b-141">Select **Install**.</span></span> <span data-ttu-id="4391b-142">Pievienojumprogrammu statuss tiks rādīts kā **Instalē**.</span><span class="sxs-lookup"><span data-stu-id="4391b-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="4391b-143">Kad tas ir izdarīts, atsvaidziniet lapu, lai redzētu statusa maiņu uz **Instalēts**.</span><span class="sxs-lookup"><span data-stu-id="4391b-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="4391b-144">Iegūt drošības pakalpojuma marķieri</span><span class="sxs-lookup"><span data-stu-id="4391b-144">Get a security service token</span></span>

<span data-ttu-id="4391b-145">Lai iegūtu drošības pakalpojuma pilnvaru, rīkojieties šādi:</span><span class="sxs-lookup"><span data-stu-id="4391b-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="4391b-146">Iegūt jūsu `aadToken` un izsaukt galapunktu: https://securityservice.operations365.dynamics.com/token.</span><span class="sxs-lookup"><span data-stu-id="4391b-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="4391b-147">Nomainiet to `client_assertion` pamattekstā ar savu `aadToken`.</span><span class="sxs-lookup"><span data-stu-id="4391b-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="4391b-148">Aizstājiet kontekstu pamattekstā ar vidi, kurā vēlaties izvietot pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="4391b-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="4391b-149">Nomainiet pamatteksta apjomu ar sekojošo:</span><span class="sxs-lookup"><span data-stu-id="4391b-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="4391b-150">MCK tvērums -"https://inventoryservice.operations365.dynamics.cn/.default"</span><span class="sxs-lookup"><span data-stu-id="4391b-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="4391b-151">(Jūs varat atrast Azure Active Directory programmas ID un nomnieka ID MCK `appsettings.mck.json`.)</span><span class="sxs-lookup"><span data-stu-id="4391b-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="4391b-152">PROD tvērums -"https://inventoryservice.operations365.dynamics.com/.default"</span><span class="sxs-lookup"><span data-stu-id="4391b-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="4391b-153">(Jūs varat atrast Azure Active Directory programmas ID un nomnieka ID PROD `appsettings.prod.json`.)</span><span class="sxs-lookup"><span data-stu-id="4391b-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="4391b-154">Rezultātiem vajadzētu izskatīties līdzīgi kā tālāk sniegtais piemērs.</span><span class="sxs-lookup"><span data-stu-id="4391b-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="4391b-155">`access_token` jūs saņemsiet atbildē.</span><span class="sxs-lookup"><span data-stu-id="4391b-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="4391b-156">Tas ir tas, kas jums nepieciešams kā nesēja marķieris, lai izsauktu krājumu redzamības API.</span><span class="sxs-lookup"><span data-stu-id="4391b-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="4391b-157">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="4391b-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="4391b-158">Pievienojumprogrammas atinstalēšana</span><span class="sxs-lookup"><span data-stu-id="4391b-158">Uninstall the add-in</span></span>

<span data-ttu-id="4391b-159">Lai atinstalētu pievienojumprogrammu, atlasiet **Atinstalēt**.</span><span class="sxs-lookup"><span data-stu-id="4391b-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="4391b-160">Atsvaidziniet LCS un Krājumu uztveramības pievienojumprogramma tiks noņemts.</span><span class="sxs-lookup"><span data-stu-id="4391b-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="4391b-161">Atinstalēšanas process noņems pievienojumprogrammu reģistrāciju un arī sāks darbu, lai notīrītu visus pakalpojumā saglabātos biznesa datus.</span><span class="sxs-lookup"><span data-stu-id="4391b-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="4391b-162">Krājumu uztveramības pievienojumprogrammas publiskais API</span><span class="sxs-lookup"><span data-stu-id="4391b-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="4391b-163">Krājumu uztveramības pievienojumprogrammas publiskais REST API piedāvā vairākus specifiskus integrācijas galapunktus.</span><span class="sxs-lookup"><span data-stu-id="4391b-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="4391b-164">Tas atbalsta trīs galvenos mijiedarbības tipus:</span><span class="sxs-lookup"><span data-stu-id="4391b-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="4391b-165">Iegrāmatojot pievienojumprogrammā rīcībā esošās izmaiņas no ārējās sistēmas.</span><span class="sxs-lookup"><span data-stu-id="4391b-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="4391b-166">Tiek vaicāti pašreizējie rīcībā esošie daudzumi no ārējās sistēmas.</span><span class="sxs-lookup"><span data-stu-id="4391b-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="4391b-167">Automātiska sinhronizācija ar Supply Chain Management rīcībā esošiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="4391b-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="4391b-168">Automātiskā sinhronizēšana nav daļa no publiskā API, bet tā vietā tiek apstrādāta fonā vidēm, kam ir iespējota Krājumu uztveramības pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="4391b-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="4391b-169">Autentifikācija</span><span class="sxs-lookup"><span data-stu-id="4391b-169">Authentication</span></span>

<span data-ttu-id="4391b-170">Platformas drošības marķieris tiek izmantots, lai izsauktu Krājumu uztveramības pievienojumprogrammu, tāpēc jums ir jāizveido Azure Active Directory marķieris, izmantojot savu Azure Active Directory programmu.</span><span class="sxs-lookup"><span data-stu-id="4391b-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="4391b-171">Papildinformāciju par to, kā iegūt drošības marķieri, skatiet šeit: [Krājumu uztveramības pievienojumprogrammas instalēšana](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="4391b-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="4391b-172">Konfigurēt krājumu uztveramības API</span><span class="sxs-lookup"><span data-stu-id="4391b-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="4391b-173">Pirms pakalpojuma izmantošanas ir jāpabeidz konfigurācijas, kas aprakstītas sekojošās apakšsadaļās.</span><span class="sxs-lookup"><span data-stu-id="4391b-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="4391b-174">Konfigurācija var atšķirties atkarībā no jūsu vides datiem.</span><span class="sxs-lookup"><span data-stu-id="4391b-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="4391b-175">Tā galvenokārt ietver četras daļas:</span><span class="sxs-lookup"><span data-stu-id="4391b-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="4391b-176">Sadalīšana</span><span class="sxs-lookup"><span data-stu-id="4391b-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="4391b-177">Dimensiju konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="4391b-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="4391b-178">Indeksācija</span><span class="sxs-lookup"><span data-stu-id="4391b-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="4391b-179">Pielāgots mērījums</span><span class="sxs-lookup"><span data-stu-id="4391b-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="4391b-180">Sadalīšana</span><span class="sxs-lookup"><span data-stu-id="4391b-180">Partitioning</span></span>

<span data-ttu-id="4391b-181">Sadalīšana var būtiski ietekmēt Krājumu uztveramības API veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="4391b-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="4391b-182">Ir ieteicams definēt shēmu, kas ļauj izmantot mazus datu grupējumus, vienlaikus atļaujot jēgpilnus datu vaicājumus.</span><span class="sxs-lookup"><span data-stu-id="4391b-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="4391b-183">`organizationId` (`dataAreaId` Supply Chain Management) vienmēr būs daļa no sadalīšanas, un pēc noklusējuma Krājumu uztveramība ir iestatīta uz sadalījumu pēc dimensijām kā *Vietne + Atrašanās vieta*.</span><span class="sxs-lookup"><span data-stu-id="4391b-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="4391b-184">Tas nozīmē, ka pakalpojumi vienmēr ir jāvaicā ar šīm filtriem definētajām dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="4391b-185">*Vietne* un *Atrašanās vieta* ir divas galvenās noklusējuma dimensijas Krājumu uztveramībai.</span><span class="sxs-lookup"><span data-stu-id="4391b-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="4391b-186">Supply Chain Management šīs dimensijas tiek sauktas par *Vietni* (`InventSiteId`) un *Noliktavu* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="4391b-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="4391b-187">Dimensiju konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="4391b-187">Dimension configurations</span></span>

<span data-ttu-id="4391b-188">Krājumu uztveramība nodrošinās vispārēju noklusējuma dimensiju sarakstu, lai iespējotu vairāku avotu sistēmu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="4391b-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="4391b-189">Sekojošajā tabulā ir minētas krājumu dimensijas, kas būs noklusējuma dimensiju nosaukumi Krājumu uztveramībai.</span><span class="sxs-lookup"><span data-stu-id="4391b-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="4391b-190">Dimensiju veids</span><span class="sxs-lookup"><span data-stu-id="4391b-190">Dimension type</span></span> | <span data-ttu-id="4391b-191">Dimensijas nosaukums</span><span class="sxs-lookup"><span data-stu-id="4391b-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="4391b-192">Produkts</span><span class="sxs-lookup"><span data-stu-id="4391b-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="4391b-193">Produkts</span><span class="sxs-lookup"><span data-stu-id="4391b-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="4391b-194">Produkts</span><span class="sxs-lookup"><span data-stu-id="4391b-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="4391b-195">Produkts</span><span class="sxs-lookup"><span data-stu-id="4391b-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="4391b-196">Izsekošana</span><span class="sxs-lookup"><span data-stu-id="4391b-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="4391b-197">Izsekošana</span><span class="sxs-lookup"><span data-stu-id="4391b-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="4391b-198">Novietojums</span><span class="sxs-lookup"><span data-stu-id="4391b-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="4391b-199">Novietojums</span><span class="sxs-lookup"><span data-stu-id="4391b-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="4391b-200">Krājumu statuss</span><span class="sxs-lookup"><span data-stu-id="4391b-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="4391b-201">Specifiska noliktava</span><span class="sxs-lookup"><span data-stu-id="4391b-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="4391b-202">Specifiska noliktava</span><span class="sxs-lookup"><span data-stu-id="4391b-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="4391b-203">Specifiska noliktava</span><span class="sxs-lookup"><span data-stu-id="4391b-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="4391b-204">Dimensijas tips, kas norādīts iepriekšējā tabulā, ir tikai atsaucei.</span><span class="sxs-lookup"><span data-stu-id="4391b-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="4391b-205">Nav nepieciešams definēt dimensijas tipu Krājumu uztveramībai.</span><span class="sxs-lookup"><span data-stu-id="4391b-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="4391b-206">Ja pielāgota dimensija pastāv un tai ir jāplūst uz noklusēto vērtību, kad to patērē Krājuma uztveramība, varat konfigurēt **Pielāgoto dimensiju** nosaukumu Krājuma uztveramībā.</span><span class="sxs-lookup"><span data-stu-id="4391b-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="4391b-207">Ārējās sistēmas piekļūst Krājumu uztveramībai, izmantojot REST API, kas iespējo rīcībā esošo informāciju par norādītajām dimensiju kopām.</span><span class="sxs-lookup"><span data-stu-id="4391b-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="4391b-208">Lai to izdarītu, Krājumu uztveramība ļauj konfigurēt *ārējā kanāla datu avotu* un avota dimensiju uz *mērķa dimensijām* Krājumu uztveramībā.</span><span class="sxs-lookup"><span data-stu-id="4391b-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="4391b-209">Mērķa dimensijām jābūt vienai no sekojošajām:</span><span class="sxs-lookup"><span data-stu-id="4391b-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="4391b-210">Noklusētās dimensijas Krājumu pārredzamībai</span><span class="sxs-lookup"><span data-stu-id="4391b-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="4391b-211">Pielāgotas dimensijas</span><span class="sxs-lookup"><span data-stu-id="4391b-211">Custom dimensions</span></span>

<span data-ttu-id="4391b-212">Dimensijas konfigurācijas nolūks ir standartizēt vairāku sistēmu integrāciju vaicājumam dimensijās un grāmatošanas notikumā ar dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="4391b-213">Indeksācija</span><span class="sxs-lookup"><span data-stu-id="4391b-213">Indexing</span></span>

<span data-ttu-id="4391b-214">Vairākumā gadījumu rīcībā esošie krājumi būs ne tikai visaugstākajā "kopējā" līmenī, bet, iespējams, vēlēsities apskatīt apkopotos rezultātus, pamatojoties uz krājumu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="4391b-215">Krājumu pārredzamība nodrošina elastību, ļaujot iestatīt indeksus, kas ir balstīti uz dimensiju vai dimensiju kombināciju.</span><span class="sxs-lookup"><span data-stu-id="4391b-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="4391b-216">Pašlaik varat konfigurēt tikai līdz pieciem indeksiem.</span><span class="sxs-lookup"><span data-stu-id="4391b-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="4391b-217">Jums ir rūpīgi jāapsver, kuru dimensiju vai dimensiju kombināciju izmantosiet pirms ieviešanas, lai nodrošinātu, ka tā atbilst jūsu biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="4391b-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="4391b-218">Piemēram, ja vēlaties vaicāt preces šādi:</span><span class="sxs-lookup"><span data-stu-id="4391b-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="4391b-219">Vaicāt apkopotos rīcībā esošos produktus pēc *Krāsas* un *Izmēra* dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="4391b-220">Dažos gadījumos jūs vienkārši vēlaties veikt vaicājumu par preci kopumā.</span><span class="sxs-lookup"><span data-stu-id="4391b-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="4391b-221">Ir divi indeksi, kas definēti kā:</span><span class="sxs-lookup"><span data-stu-id="4391b-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="4391b-222">Tukšas iekavas tiks apkopotas, pamatojoties uz produkta ID nodalījumā.</span><span class="sxs-lookup"><span data-stu-id="4391b-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="4391b-223">Indeksēšana definē, kā varat grupēt rezultātus, pamatojoties uz `groupBy` vaicājuma iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="4391b-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="4391b-224">Šādā gadījumā, ja nedefinējat nevienu `groupBy` vērtību, kopsummas tiks iegūtas pēc `productid`.</span><span class="sxs-lookup"><span data-stu-id="4391b-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="4391b-225">Pretējā gadījumā, ja definējat `groupBy` kā `groupBy=ColorId&groupBy=SizeId`, jūs saņemsiet atpakaļ vairākas rindas, pamatojoties uz atšķirīgām krāsu un izmēru kombinācijām sistēmā.</span><span class="sxs-lookup"><span data-stu-id="4391b-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="4391b-226">Vaicājuma kritērijus var ievietot pieprasījuma pamattekstā.</span><span class="sxs-lookup"><span data-stu-id="4391b-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="4391b-227">Šeit ir parauga vaicājums produktam ar krāsu un izmēru kombināciju.</span><span class="sxs-lookup"><span data-stu-id="4391b-227">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="4391b-228">Pielāgots mērījums</span><span class="sxs-lookup"><span data-stu-id="4391b-228">Custom measurement</span></span>

<span data-ttu-id="4391b-229">Noklusējuma mērījumu daudzumi ir saistīti ar Supply Chain Management, tomēr, iespējams, vēlēsities izveidot daudzumu, kas sastāv no noklusējuma mērījumu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="4391b-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="4391b-230">Lai to paveiktu, var izveidot pielāgoto daudzumu konfigurāciju, kas tiks pievienota rīcībā esošo vaicājumu izvadei.</span><span class="sxs-lookup"><span data-stu-id="4391b-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="4391b-231">Funkcionalitāte vienkārši ļauj definēt mērvienību kopu, kas tiks pievienota, un/vai mēru kopa, kas tiks atņemta, lai izveidotu pielāgotu mērījumu.</span><span class="sxs-lookup"><span data-stu-id="4391b-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="4391b-232">Piemēram, ar šādu vaicājuma nosacījumu, jūs konfigurēsit pielāgoto mērījumu daudzumu kā `MyCustomAvailableforReservation`, kas tiks patērēts patēriņa sistēmai.</span><span class="sxs-lookup"><span data-stu-id="4391b-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="4391b-233">Patēriņa sistēma</span><span class="sxs-lookup"><span data-stu-id="4391b-233">Consumption system</span></span> | <span data-ttu-id="4391b-234">Aprēķinātie līdzekļi</span><span class="sxs-lookup"><span data-stu-id="4391b-234">Calculated measurers</span></span> | <span data-ttu-id="4391b-235">Datu avots</span><span class="sxs-lookup"><span data-stu-id="4391b-235">Data source</span></span> | <span data-ttu-id="4391b-236">Modifikators</span><span class="sxs-lookup"><span data-stu-id="4391b-236">Modifier</span></span> | <span data-ttu-id="4391b-237">Modifikatora aprēķina tips</span><span class="sxs-lookup"><span data-stu-id="4391b-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="4391b-238">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="4391b-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="4391b-239">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="4391b-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="4391b-240">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="4391b-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="4391b-241">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="4391b-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="4391b-242">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="4391b-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="4391b-243">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="4391b-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="4391b-244">Papildinājums</span><span class="sxs-lookup"><span data-stu-id="4391b-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="4391b-245">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="4391b-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="4391b-246">Atņemšana</span><span class="sxs-lookup"><span data-stu-id="4391b-246">Subtraction</span></span> |

<span data-ttu-id="4391b-247">Ar to vaicājums uz pielāgoto mērījumu daudzumu atgriezīs tālāk norādīto izvadi.</span><span class="sxs-lookup"><span data-stu-id="4391b-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="4391b-248">`MyCustomAvailableforReservation` izvade tiek balstīta uz aprēķina iestatījumu pielāgotos mērījumos kā:</span><span class="sxs-lookup"><span data-stu-id="4391b-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="4391b-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="4391b-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="4391b-250">Rīcībā esošo izmaiņu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="4391b-250">Posting on-hand changes</span></span>

<span data-ttu-id="4391b-251">Precīzais vietrādis URL, uz kuru tiks izlikts pasākums, būs atkarīgs no jūsu ģeogrāfiskā reģiona.</span><span class="sxs-lookup"><span data-stu-id="4391b-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="4391b-252">Tam būs šāds formāts:</span><span class="sxs-lookup"><span data-stu-id="4391b-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="4391b-253">Kad šis vietrādis URL ir autentificēts, to var izmantot kopā ar HTTP `POST` metodi, lai nosūtītu rīcībā esošo izmaiņu notikumus pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="4391b-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="4391b-254">Īpašu galveni izmanto, lai sazinātos ar Dynamics 365 pakalpojumiem, izmantojot HTTP pieprasījumus, kas norāda Supply Chain Management instances vides ID, ar kuru ir saistīti dati.</span><span class="sxs-lookup"><span data-stu-id="4391b-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="4391b-255">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="4391b-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="4391b-256">Iegrāmatošanas rīcībā esošo izmaiņu vaicājums 1. piemērs</span><span class="sxs-lookup"><span data-stu-id="4391b-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="4391b-257">Šajā piemērā ir parādīts scenārijs, kur tiks iestatīta dimensiju konfigurācija risinājumā Power Apps.</span><span class="sxs-lookup"><span data-stu-id="4391b-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="4391b-258">Izmantojiet šo vaicājumu, lai konfigurētu dimensiju kartēšanu risinājumā Power Apps:</span><span class="sxs-lookup"><span data-stu-id="4391b-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="4391b-259">Tagad varat norādīt `dimensionDataSource` un izmantot pielāgotās dimensijas savos vaicājumos.</span><span class="sxs-lookup"><span data-stu-id="4391b-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="4391b-260">Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="4391b-261">Iegrāmatošanas rīcībā esošo izmaiņu vaicājums 2. piemērs</span><span class="sxs-lookup"><span data-stu-id="4391b-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="4391b-262">Šis piemērs rāda scenāriju, kad dimensiju konfigurācijai nav iestatīti kartējumi risinājumā Power Apps, tāpēc grāmatošanai jāizmanto arī pamata dimensijas.</span><span class="sxs-lookup"><span data-stu-id="4391b-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="4391b-263">Ja `dimensionDataSource` lauks ir nulle, tukša vai baltstarpa, visām dimensijām ir jābūt pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="4391b-264">JSON dokumenta lauku rekvizīti</span><span class="sxs-lookup"><span data-stu-id="4391b-264">JSON document field properties</span></span>

<span data-ttu-id="4391b-265">Iepriekš sniegtajos JSON vaicājuma piemēru laukos ir rekvizīti, kas norādīti šajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="4391b-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="4391b-266">Lauka kods</span><span class="sxs-lookup"><span data-stu-id="4391b-266">Field ID</span></span> | <span data-ttu-id="4391b-267">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4391b-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="4391b-268">Unikāls ID noteiktam izmaiņu notikumam.</span><span class="sxs-lookup"><span data-stu-id="4391b-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="4391b-269">Šis ID tiek izmantots, lai nodrošinātu, ka, ja grāmatošanas laikā sakari ar pakalpojumu neizdodas, notikuma atkārtota iesniegšana nenozīmē, ka viens un tas pats notikums sistēmā tiek skaitīts divas reizes.</span><span class="sxs-lookup"><span data-stu-id="4391b-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="4391b-270">Ar notikumu saistītās organizācijas identifikators.</span><span class="sxs-lookup"><span data-stu-id="4391b-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="4391b-271">Tas attiecas uz Supply Chain Management organizācijām vai datu apgabala ID.</span><span class="sxs-lookup"><span data-stu-id="4391b-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="4391b-272">Attiecīgā produkta identifikators.</span><span class="sxs-lookup"><span data-stu-id="4391b-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="4391b-273">Daudzums, par kādu ir jāmaina rīcībā esošais krājums.</span><span class="sxs-lookup"><span data-stu-id="4391b-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="4391b-274">Piemēram, ja plauktam pievienoti 10 jauni beigeļi, šī vērtība ir 10.</span><span class="sxs-lookup"><span data-stu-id="4391b-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="4391b-275">Ja 3 beigeļi tiks noņemti no plaukta vai pārdoti, šī vērtība būs -3.</span><span class="sxs-lookup"><span data-stu-id="4391b-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="4391b-276">Grāmatošanas izmaiņu notikumā un vaicājumā izmantoto dimensiju datu avots.</span><span class="sxs-lookup"><span data-stu-id="4391b-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="4391b-277">Ja norādāt datu avotu, varat izmantot pielāgotās dimensijas no norādītā datu avota.</span><span class="sxs-lookup"><span data-stu-id="4391b-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="4391b-278">Ar dimensiju konfigurāciju Krājumu pārredzamība var kartēt pielāgotās dimensijas uz vispārīgajām noklusējuma dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="4391b-279">Ja `dimensionDataSource` nav norādīts, jūsu vaicājumos var izmantot tikai vispārīgās noklusējuma dimensijas.</span><span class="sxs-lookup"><span data-stu-id="4391b-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="4391b-280">Dinamisks atslēgu/vērtību pāru kopums.</span><span class="sxs-lookup"><span data-stu-id="4391b-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="4391b-281">Tās tiks kartētas uz dažām Supply Chain Management dimensijām, bet varat pievienot arī pielāgotas dimensijas (piemēram *Avotu)*, kas var norādīt, ka notikums tika saņemts no Supply Chain Management vai ārējas sistēmas.</span><span class="sxs-lookup"><span data-stu-id="4391b-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="4391b-282">Pašreizējo rīcībā esošo krājumu vaicājums</span><span class="sxs-lookup"><span data-stu-id="4391b-282">Querying current on-hand</span></span>

<span data-ttu-id="4391b-283">Pašreizējo rīcībā esošo krājumu vaicājuma galapunkts būs līdzīgs vietrādis URL:</span><span class="sxs-lookup"><span data-stu-id="4391b-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="4391b-284">Ar HTTP `POST` metodi tiks veikts vaicājums.</span><span class="sxs-lookup"><span data-stu-id="4391b-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="4391b-285">Pašreizējais rīcībā esošais vaicājums 1. piemērs</span><span class="sxs-lookup"><span data-stu-id="4391b-285">Current on-hand query example 1</span></span>

<span data-ttu-id="4391b-286">Šajā piemērā ir parādīts scenārijs, kurā jau ir iestatīta dimensiju konfigurācija risinājumā Power Apps.</span><span class="sxs-lookup"><span data-stu-id="4391b-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="4391b-287">Izmantojiet šo vaicājumu, lai konfigurētu dimensiju kartēšanu risinājumā Power Apps:</span><span class="sxs-lookup"><span data-stu-id="4391b-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="4391b-288">Tagad varat norādīt `dimensionDataSource` un izmantot pielāgotās dimensijas savos vaicājumos.</span><span class="sxs-lookup"><span data-stu-id="4391b-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="4391b-289">Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="4391b-290">Varat norādīt `DimensionDataSource` `filters` un norādīt pielāgotās dimensijas gan `filters`, gan `groupByValues`.</span><span class="sxs-lookup"><span data-stu-id="4391b-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="4391b-291">Sistēma automātiski konvertēs pielāgotās dimensijas uz pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="4391b-292">Pašreizējais rīcībā esošais vaicājums 2. piemērs</span><span class="sxs-lookup"><span data-stu-id="4391b-292">Current on-hand query example 2</span></span>

<span data-ttu-id="4391b-293">Šis piemērs rāda scenāriju, kad dimensiju konfigurācijai nav iestatīti kartējumi risinājumā Power Apps, tāpēc grāmatošanai jāizmanto arī pamata dimensijas.</span><span class="sxs-lookup"><span data-stu-id="4391b-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="4391b-294">Ja `dimensionDataSource` lauks sadaļā `filters` ir nulle, tukšs vai kā atstarpe, visām dimensijām ir jābūt pamata dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4391b-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="4391b-295">Piemēra atgriešanas rezultāts</span><span class="sxs-lookup"><span data-stu-id="4391b-295">Example return result</span></span>

<span data-ttu-id="4391b-296">Iepriekšējos piemēros parādītie vaicājumi var atgriezt, piemēram, šādu rezultātu.</span><span class="sxs-lookup"><span data-stu-id="4391b-296">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="4391b-297">Ievērojiet, ka daudzuma lauki ir strukturēti kā mērvienību vārdnīca un to saistītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="4391b-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
