---
title: Common Data Service virtuālo elementu konfigurēšana
description: Šajā tēmā parādīts, kā konfigurēt virtuālos elementus Dynamics 365 Human Resources. Ģenerējiet un atjauniniet esošos virtuālos elementus un analizējiet ģenerētos un pieejamos elementus.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959579"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="525b7-104">Common Data Service virtuālo elementu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="525b7-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="525b7-105">Dynamics 365 Human Resources ir virtuālais datu avots platformā Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="525b7-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="525b7-106">Tas nodrošina pilnīgas izveides, lasīšanas, atjaunināšanas un dzēšanas (CRUD) operācijas no Common Data Service un Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="525b7-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="525b7-107">Dati virtuālajiem elementiem netiek saglabāti Common Data Service, bet gan lietojumprogrammas datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="525b7-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="525b7-108">Lai iespējotu CRUD operācijas personāla vadības elementos no Common Data Service, jums jāpadara šos elementus pieejamus kā virtuālus elementus Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="525b7-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="525b7-109">Tas ļauj veikt CRUD operācijas no Common Data Service un Microsoft Power Platform personāla vadības datos.</span><span class="sxs-lookup"><span data-stu-id="525b7-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="525b7-110">Operācijas atbalsta arī pilnas biznesa loģikas personāla vadības pārbaudes, lai nodrošinātu datu integritāti, rakstot datus elementos.</span><span class="sxs-lookup"><span data-stu-id="525b7-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="525b7-111">Pieejamie virtuālie elementi personāla vadībai</span><span class="sxs-lookup"><span data-stu-id="525b7-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="525b7-112">Visi atvērtie datu protokola (OData) elementi personāla vadībā ir pieejami kā virtuālie elementi Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="525b7-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="525b7-113">Tie ir pieejami arī Power Platform.</span><span class="sxs-lookup"><span data-stu-id="525b7-113">They're also available in Power Platform.</span></span> <span data-ttu-id="525b7-114">Tagad varat veidot lietojumprogrammas un pieredzi ar datiem tieši no personāla vadības ar pilnām CRUD iespējām, nekopējot vai nesinhronizējot datus ar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="525b7-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="525b7-115">Varat izmantot Power Apps portālus, lai veidotu tīmekļa vietnes ar ārējo piekļuvi, kas iespējo sadarbības scenārijus biznesa procesiem personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="525b7-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="525b7-116">Varat apskatīt vidē iespējoto virtuālo elementu sarakstu un sākt darbu ar elementiem pakalpojumā [Power Apps](https://make.powerapps.com), **Dynamics 365 HR Virtual Entity** risinājumā.</span><span class="sxs-lookup"><span data-stu-id="525b7-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Dynamics 365 HR Virtual Entity pakalpojumā Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="525b7-118">Virtuālie elementi salīdzinājumā ar fiziskām personām</span><span class="sxs-lookup"><span data-stu-id="525b7-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="525b7-119">Virtuālie personāla vadības elementi atšķiras no fiziskajām personām Common Data Service, kas veidotas personāla vadības vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="525b7-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="525b7-120">Fiziskās personas personāla vadības vajadzībām tiek veidotas atsevišķi un uzturētas kopējā HCM risinājumā Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="525b7-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="525b7-121">Fizisku personu gadījumā dati tiek saglabāti Common Data Service un tiem nepieciešama sinhronizācija ar personāla vadības lietojumprogrammas datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="525b7-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="525b7-122">Fizisko personu sarakstu Common Data Service personāla vadības vajadzībām skatiet [Common Data Service elementi](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="525b7-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="525b7-123">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="525b7-123">Setup</span></span>

<span data-ttu-id="525b7-124">Sekojiet šīm iestatīšanas darbībām, lai iespējotu virtuālos elementus jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="525b7-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="525b7-125">Lietojumprogrammas reģistrēšana Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="525b7-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="525b7-126">Vispirms lietojumprogramma ir jāreģistrē Azure portālā, lai Microsoft Identity platforma var nodrošināt autentifikāciju un autorizācijas pakalpojumus lietojumprogrammai un lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="525b7-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="525b7-127">Lai iegūtu vairāk informācijas par lietojumprogrammu reģistrāciju Azure, skatiet [Īsa pamācība: lietojumprogrammas reģistrēšana platformā Microsoft Identity](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="525b7-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="525b7-128">Atveriet [Microsoft Azure portālu](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="525b7-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="525b7-129">Azure pakalpojumu sarakstā atlasiet **Lietojumprogrammu reģistrācijas**.</span><span class="sxs-lookup"><span data-stu-id="525b7-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="525b7-130">Atlasiet **Jauna reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="525b7-130">Select **New registration**.</span></span>

4. <span data-ttu-id="525b7-131">Laukā **Nosaukums** ievadiet aprakstošu lietojumprogrammas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="525b7-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="525b7-132">Piemēram, **Dynamics 365 Human Resources virtuālie elementi**.</span><span class="sxs-lookup"><span data-stu-id="525b7-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="525b7-133">**Novirzīšanas URI** laukā ievadiet savas personāla vadības instances nosaukumvietas URL.</span><span class="sxs-lookup"><span data-stu-id="525b7-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="525b7-134">Atlasiet **Reģistrēt**.</span><span class="sxs-lookup"><span data-stu-id="525b7-134">Select **Register**.</span></span>

7. <span data-ttu-id="525b7-135">Kad reģistrācija pabeigta, Azure portālā tiek parādīta lietojumprogrammas reģistrācijas **pārskata** rūts, kurā ir ietverts tās **lietojumprogrammas (klienta) ID**.</span><span class="sxs-lookup"><span data-stu-id="525b7-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="525b7-136">Pašlaik ņemiet vērā **lietojumprogrammas (klienta) ID**.</span><span class="sxs-lookup"><span data-stu-id="525b7-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="525b7-137">Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālā elementa datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="525b7-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="525b7-138">Kreisajā navigācijas rūtī atlasiet **sertifikāti un noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="525b7-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="525b7-139">Lapas sadaļā **Klienta noslēpumi** atlasiet **Jauns klienta noslēpums**.</span><span class="sxs-lookup"><span data-stu-id="525b7-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="525b7-140">Ievadiet aprakstu, atlasiet ilgumu un atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="525b7-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="525b7-141">Reģistrējiet noslēpuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="525b7-141">Record the secret's value.</span></span> <span data-ttu-id="525b7-142">Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālā elementa datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span><span class="sxs-lookup"><span data-stu-id="525b7-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="525b7-143">Pārliecinieties, ka ņemat vērā pašreizējo noslēpuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="525b7-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="525b7-144">Pēc iziešanas no šīs lapas noslēpums nekad vairs netiek parādīts.</span><span class="sxs-lookup"><span data-stu-id="525b7-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="525b7-145">Dynamics 365 HR Virtual Entity lietojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="525b7-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="525b7-146">Instalējiet Dynamics 365 HR Virtual Entity lietojumprogrammu jūsu Power Apps vidē, lai izvietotu virtuālos elementu risinājuma pakotni Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="525b7-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="525b7-147">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="525b7-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="525b7-148">Sarakstā **Vides** atlasiet ar jūsu personāla vadības instanci saistīto Power Apps vidi.</span><span class="sxs-lookup"><span data-stu-id="525b7-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="525b7-149">Lapas sadaļā **Resursi** atlasiet **Dynamics 365 lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="525b7-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="525b7-150">Atlasiet darbību **Lietojumprogrammas instalēšana**.</span><span class="sxs-lookup"><span data-stu-id="525b7-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="525b7-151">Atlasiet **Dynamics 365 HR Virtual Entity** un atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="525b7-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="525b7-152">Pārskatiet un atzīmējiet, ka piekrītat pakalpojuma nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="525b7-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="525b7-153">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="525b7-153">Select **Install**.</span></span>

<span data-ttu-id="525b7-154">Instalācija aizņem dažas minūtes.</span><span class="sxs-lookup"><span data-stu-id="525b7-154">The install takes a few minutes.</span></span> <span data-ttu-id="525b7-155">Kad tā ir pabeigta, pārejiet pie nākamajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="525b7-155">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtual Entity lietojumprogrammas instalēšana no Power Platform administrēšanas centra](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="525b7-157">Virtuālo elementu datu avota konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="525b7-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="525b7-158">Nākamais solis ir konfigurēt virtuālā elementa datu avotu Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="525b7-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="525b7-159">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="525b7-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="525b7-160">Sarakstā **Vides** atlasiet ar jūsu personāla vadības instanci saistīto Power Apps vidi.</span><span class="sxs-lookup"><span data-stu-id="525b7-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="525b7-161">Atlasiet **Vides URL** lapas sadaļā **Detalizēti**.</span><span class="sxs-lookup"><span data-stu-id="525b7-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="525b7-162">**Risinājumu darbspējas centrmezglā** atlasiet ikonu **Detalizētā atrašana** lietojumprogrammas lapas augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="525b7-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="525b7-163">Lapā **Detalizētā atrašana**, nolaižamajā sarakstā **Meklēt** atlasiet **Finance and Operations virtuālo datu avotu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="525b7-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="525b7-164">Atlasiet **Rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="525b7-164">Select **Results**.</span></span>

7. <span data-ttu-id="525b7-165">Atlasiet ierakstu **Microsoft HR datu avots**.</span><span class="sxs-lookup"><span data-stu-id="525b7-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="525b7-166">Ievadiet nepieciešamo informāciju par datu avota konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="525b7-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="525b7-167">**Mērķa URL**: jūsu personāla vadības nosaukumvietas URL.</span><span class="sxs-lookup"><span data-stu-id="525b7-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="525b7-168">**Nomnieka ID**: Azure Active Directory (Azure AD) nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="525b7-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="525b7-169">**AAD lietojumprogrammas ID**: lietojumprogrammas (klienta) ID, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="525b7-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="525b7-170">Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="525b7-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="525b7-171">**AAD lietojumprogrammas noslēpums**: klienta noslēpums, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="525b7-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="525b7-172">Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="525b7-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="525b7-173">Atlasiet **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="525b7-173">Select **Save & Close**.</span></span>

   ![Microsoft HR datu avots](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="525b7-175">Piešķiriet lietojumprogrammas atļaujas personāla vadībā</span><span class="sxs-lookup"><span data-stu-id="525b7-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="525b7-176">Piešķiriet atļaujas abām Azure AD lietojumprogrammām personāla vadībā:</span><span class="sxs-lookup"><span data-stu-id="525b7-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="525b7-177">Lietojumprogramma, kas izveidota jūsu nomniekam Microsoft Azure portālā</span><span class="sxs-lookup"><span data-stu-id="525b7-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="525b7-178">Dynamics 365 HR Virtual Entity lietojumprogramma, kas instalēta Power Apps vidē</span><span class="sxs-lookup"><span data-stu-id="525b7-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="525b7-179">Personāla vadībā atveriet **Azure Active Directory lietojumprogrammu** lapu.</span><span class="sxs-lookup"><span data-stu-id="525b7-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="525b7-180">Atlasiet **Jauns**, lai izveidotu jaunu lietojumprogrammas ierakstu:</span><span class="sxs-lookup"><span data-stu-id="525b7-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="525b7-181">Laukā **Klienta ID**, ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas klienta ID.</span><span class="sxs-lookup"><span data-stu-id="525b7-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="525b7-182">Laukā **Nosaukums** ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="525b7-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="525b7-183">Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="525b7-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="525b7-184">Atlasiet **Jauns**, lai izveidotu otru lietojumprogrammas ierakstu:</span><span class="sxs-lookup"><span data-stu-id="525b7-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="525b7-185">**Klienta Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="525b7-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="525b7-186">**Nosaukums**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="525b7-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="525b7-187">Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="525b7-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="525b7-188">Virtuālo elementu ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="525b7-188">Generate virtual entities</span></span>

<span data-ttu-id="525b7-189">Kad iestatīšana ir pabeigta, varat atlasīt virtuālos elementus, kurus vēlaties ģenerēt un iespējot savā Common Data Service instancē.</span><span class="sxs-lookup"><span data-stu-id="525b7-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="525b7-190">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="525b7-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="525b7-191">Sarakstā **Vides** atlasiet ar jūsu personāla vadības instanci saistīto Power Apps vidi.</span><span class="sxs-lookup"><span data-stu-id="525b7-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="525b7-192">Atlasiet **Vides URL** lapas sadaļā **Detalizēti**.</span><span class="sxs-lookup"><span data-stu-id="525b7-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="525b7-193">**Risinājumu darbspējas centrmezglā** atlasiet ikonu **Detalizētā atrašana** lapas augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="525b7-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="525b7-194">Lapas **Detalizētā atrašana** nolaižamajā sarakstā **Meklēt** atlasiet **Pieejamie HR elementi**.</span><span class="sxs-lookup"><span data-stu-id="525b7-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="525b7-195">Izmantojiet filtra opcijas, lai atrastu elementu vai elementus, kurus vēlaties iespējot.</span><span class="sxs-lookup"><span data-stu-id="525b7-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="525b7-196">Sarakstā atlasiet elementu.</span><span class="sxs-lookup"><span data-stu-id="525b7-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="525b7-197">Elementu lapā attiecīgajam elementam nomainiet rekvizītu **Ir ģenerēts** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="525b7-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="525b7-198">Saglabājiet un aizveriet elementu lapu.</span><span class="sxs-lookup"><span data-stu-id="525b7-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="525b7-199">Varat vienlaicīgi ģenerēt vairākus virtuālos elementus, izmantojot lapu **Mainīt vairākus ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="525b7-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="525b7-200">Lapā atlasiet vairākus ierakstus un lentē atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="525b7-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="525b7-201">Pēc tam varat mainīt rekvizītu **Ir ģenerēts** visiem atlasītajiem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="525b7-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![Pieejamie HR elementi](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="525b7-203">Lai racionalizētu virtuālo elementu ģenerēšanas procesu nākamajos izlaidumos, process notiks personāla vadības lapā.</span><span class="sxs-lookup"><span data-stu-id="525b7-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="525b7-204">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="525b7-204">See also</span></span>

[<span data-ttu-id="525b7-205">Kas ir Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="525b7-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="525b7-206">Elementu pārskats</span><span class="sxs-lookup"><span data-stu-id="525b7-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="525b7-207">Elementu attiecību pārskats</span><span class="sxs-lookup"><span data-stu-id="525b7-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="525b7-208">Izveidot un rediģēt virtuālos elementus, kas satur datus no ārējo datu avota</span><span class="sxs-lookup"><span data-stu-id="525b7-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="525b7-209">Kas ir Power Apps portāli?</span><span class="sxs-lookup"><span data-stu-id="525b7-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="525b7-210">Lietojumprogrammu izveides pārskats Power Apps</span><span class="sxs-lookup"><span data-stu-id="525b7-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
