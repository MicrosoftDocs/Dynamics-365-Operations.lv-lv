---
title: Dataverse virtuālo tabulu konfigurēšana
description: Šajā tēmā parādīts, kā konfigurēt virtuālās tabulas Dynamics 365 Human Resources. Ģenerējiet un atjauniniet esošās virtuālās tabulas un analizējiet ģenerētās un pieejamās tabulas.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: d8780be777c9a204fcb95950f5679a5711aee298
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465826"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="67cc0-104">Dataverse virtuālo tabulu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="67cc0-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="67cc0-105">Dynamics 365 Human Resources ir virtuālais datu avots platformā Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67cc0-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="67cc0-106">Tas nodrošina pilnīgas izveides, lasīšanas, atjaunināšanas un dzēšanas (CRUD) operācijas no Dataverse un Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="67cc0-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="67cc0-107">Dati virtuālajām tabulām netiek saglabāti Dataverse, bet gan programmas datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="67cc0-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="67cc0-108">Lai iespējotu CRUD operācijas personāla vadības elementos no Dataverse, jums jāpadara šos elementus pieejamus kā virtuālas tabulas Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67cc0-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="67cc0-109">Tas ļauj veikt CRUD operācijas no Dataverse un Microsoft Power Platform personāla vadības datos.</span><span class="sxs-lookup"><span data-stu-id="67cc0-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="67cc0-110">Operācijas atbalsta arī pilnas biznesa loģikas personāla vadības pārbaudes, lai nodrošinātu datu integritāti, rakstot datus elementos.</span><span class="sxs-lookup"><span data-stu-id="67cc0-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="67cc0-111">Human Resources elementi atbilst Dataverse tabulām.</span><span class="sxs-lookup"><span data-stu-id="67cc0-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="67cc0-112">Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="67cc0-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="67cc0-113">Pieejamās virtuālās tabulas Human Resources</span><span class="sxs-lookup"><span data-stu-id="67cc0-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="67cc0-114">Visi atvērtie datu protokola (OData) elementi Human Resources ir pieejamas kā virtuālās tabulas Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67cc0-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="67cc0-115">Tie ir pieejami arī Power Platform.</span><span class="sxs-lookup"><span data-stu-id="67cc0-115">They're also available in Power Platform.</span></span> <span data-ttu-id="67cc0-116">Tagad varat veidot lietojumprogrammas un pieredzi ar datiem tieši no personāla vadības ar pilnām CRUD iespējām, nekopējot vai nesinhronizējot datus ar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67cc0-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="67cc0-117">Varat izmantot Power Apps portālus, lai veidotu tīmekļa vietnes ar ārējo piekļuvi, kas iespējo sadarbības scenārijus biznesa procesiem personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="67cc0-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="67cc0-118">Varat apskatīt vidē iespējoto virtuālo tabulu sarakstu un sākt darbu ar tabulām pakalpojumā [Power Apps](https://make.powerapps.com), **Dynamics 365 HR Virtual Tables** risinājumā.</span><span class="sxs-lookup"><span data-stu-id="67cc0-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Dynamics 365 HR Virtual Tables pakalpojumā Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="67cc0-120">Virtuālās tabulas pret vietējām tabulām</span><span class="sxs-lookup"><span data-stu-id="67cc0-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="67cc0-121">Virtuālās Human Resources tabulas atšķiras no vietējām Dataverse tabulām, kas veidotas Human Resources vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="67cc0-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="67cc0-122">Vietējās tabulas Human Resources vajadzībām tiek veidotas atsevišķi un uzturētas kopējā HCM risinājumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67cc0-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="67cc0-123">Vietējo tabulu gadījumā dati tiek saglabāti Dataverse un tiem nepieciešama sinhronizācija ar Human Resources programmas datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="67cc0-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="67cc0-124">Vietējo Dataverse tabulu Human Resources vajadzībām sarakstu skatiet [Dataverse tabulas](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="67cc0-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="67cc0-125">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="67cc0-125">Setup</span></span>

<span data-ttu-id="67cc0-126">Sekojiet šīm iestatīšanas darbībām, lai iespējotu virtuālās tabulas jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="67cc0-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="67cc0-127">Iespējot virtuālās tabulas Human Resources</span><span class="sxs-lookup"><span data-stu-id="67cc0-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="67cc0-128">Vispirms **Funkciju pārvaldības** darbvietā ir jāiespējo virtuālas tabulas.</span><span class="sxs-lookup"><span data-stu-id="67cc0-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="67cc0-129">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="67cc0-130">Atlasiet elementu **Funkciju pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="67cc0-131">Atlasiet **Virtuālās tabulas atbalsts HR programmā Dataverse** un pēc tam atlasiet **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="67cc0-132">Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu un atspējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="67cc0-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="67cc0-133">Lietojumprogrammas reģistrēšana Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="67cc0-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="67cc0-134">Vispirms jūsu Personāla vadības instance ir jāreģistrē Azure portālā, lai Microsoft Identity platforma var nodrošināt autentifikāciju un autorizācijas pakalpojumus lietojumprogrammai un lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="67cc0-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="67cc0-135">Lai iegūtu vairāk informācijas par lietojumprogrammu reģistrāciju Azure, skatiet [Īsa pamācība: lietojumprogrammas reģistrēšana platformā Microsoft Identity](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="67cc0-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="67cc0-136">Atveriet [Microsoft Azure portālu](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="67cc0-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="67cc0-137">Azure pakalpojumu sarakstā atlasiet **Lietojumprogrammu reģistrācijas**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="67cc0-138">Atlasiet **Jauna reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-138">Select **New registration**.</span></span>

4. <span data-ttu-id="67cc0-139">Laukā **Nosaukums** ievadiet aprakstošu lietojumprogrammas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="67cc0-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="67cc0-140">Piemēram, **Dynamics 365 Human Resources virtuālās tabulas**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="67cc0-141">**Novirzīšanas URI** laukā ievadiet savas personāla vadības instances nosaukumvietas URL.</span><span class="sxs-lookup"><span data-stu-id="67cc0-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="67cc0-142">Atlasiet **Reģistrēt**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-142">Select **Register**.</span></span>

7. <span data-ttu-id="67cc0-143">Kad reģistrācija pabeigta, Azure portālā tiek parādīta lietojumprogrammas reģistrācijas **pārskata** rūts, kurā ir ietverts tās **lietojumprogrammas (klienta) ID**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="67cc0-144">Pašlaik ņemiet vērā **lietojumprogrammas (klienta) ID**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="67cc0-145">Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālās tabulas datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="67cc0-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="67cc0-146">Kreisajā navigācijas rūtī atlasiet **sertifikāti un noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="67cc0-147">Lapas sadaļā **Klienta noslēpumi** atlasiet **Jauns klienta noslēpums**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="67cc0-148">Ievadiet aprakstu, atlasiet ilgumu un atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="67cc0-149">Reģistrējiet noslēpuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="67cc0-149">Record the secret's value.</span></span> <span data-ttu-id="67cc0-150">Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālās tabulas datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="67cc0-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="67cc0-151">Pārliecinieties, ka ņemat vērā pašreizējo noslēpuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="67cc0-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="67cc0-152">Pēc iziešanas no šīs lapas noslēpums nekad vairs netiek parādīts.</span><span class="sxs-lookup"><span data-stu-id="67cc0-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="67cc0-153">Dynamics 365 HR Virtual Tables programmas instalēšana</span><span class="sxs-lookup"><span data-stu-id="67cc0-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="67cc0-154">Instalējiet Dynamics 365 HR Virtual Tables programmu jūsu Power Apps vidē, lai izvietotu virtuālās tabulas risinājuma pakotni Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67cc0-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="67cc0-155">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="67cc0-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="67cc0-156">Sarakstā **Vides** atlasiet ar jūsu personāla vadības instanci saistīto Power Apps vidi.</span><span class="sxs-lookup"><span data-stu-id="67cc0-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="67cc0-157">Lapas sadaļā **Resursi** atlasiet **Dynamics 365 lietojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="67cc0-158">Atlasiet darbību **Lietojumprogrammas instalēšana**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="67cc0-159">Atlasiet **Dynamics 365 HR Virtual Table** un atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="67cc0-160">Pārskatiet un atzīmējiet, ka piekrītat pakalpojuma nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="67cc0-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="67cc0-161">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-161">Select **Install**.</span></span>

<span data-ttu-id="67cc0-162">Instalācija aizņem dažas minūtes.</span><span class="sxs-lookup"><span data-stu-id="67cc0-162">The install takes a few minutes.</span></span> <span data-ttu-id="67cc0-163">Kad tā ir pabeigta, pārejiet pie nākamajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="67cc0-163">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Virtual Table programmas instalēšana no Power Platform administrēšanas centra](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="67cc0-165">Virtuālās tabulas datu avota konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="67cc0-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="67cc0-166">Nākamais solis ir konfigurēt virtuālās tabulas datu avotu Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="67cc0-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="67cc0-167">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="67cc0-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="67cc0-168">Sarakstā **Vides** atlasiet ar jūsu personāla vadības instanci saistīto Power Apps vidi.</span><span class="sxs-lookup"><span data-stu-id="67cc0-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="67cc0-169">Atlasiet **Vides URL** lapas sadaļā **Detalizēti**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="67cc0-170">**Risinājumu darbspējas centrmezglā** atlasiet ikonu **Detalizētā atrašana** lietojumprogrammas lapas augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="67cc0-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="67cc0-171">Lapā **Detalizētā atrašana**, nolaižamajā sarakstā **Meklēt** atlasiet **Finance and Operations virtuālo datu avotu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="67cc0-172">Atlasiet **Rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-172">Select **Results**.</span></span>

7. <span data-ttu-id="67cc0-173">Atlasiet ierakstu **Microsoft HR datu avots**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="67cc0-174">Ievadiet nepieciešamo informāciju par datu avota konfigurāciju:</span><span class="sxs-lookup"><span data-stu-id="67cc0-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="67cc0-175">**Mērķa URL**: jūsu personāla vadības nosaukumvietas URL.</span><span class="sxs-lookup"><span data-stu-id="67cc0-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="67cc0-176">Mērķa URL formāts ir:</span><span class="sxs-lookup"><span data-stu-id="67cc0-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="67cc0-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="67cc0-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="67cc0-178">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="67cc0-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="67cc0-179">Noteikti iekļaujiet rakstzīmi "**/**" vietrāža URL beigās, lai izvairītos no kļūdas saņemšanas.</span><span class="sxs-lookup"><span data-stu-id="67cc0-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="67cc0-180">**Nomnieka ID**: Azure Active Directory (Azure AD) nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="67cc0-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="67cc0-181">**AAD lietojumprogrammas ID**: lietojumprogrammas (klienta) ID, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="67cc0-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="67cc0-182">Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="67cc0-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="67cc0-183">**AAD lietojumprogrammas noslēpums**: klienta noslēpums, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="67cc0-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="67cc0-184">Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="67cc0-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR datu avots](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="67cc0-186">Atlasiet **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="67cc0-187">Piešķiriet lietojumprogrammas atļaujas personāla vadībā</span><span class="sxs-lookup"><span data-stu-id="67cc0-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="67cc0-188">Piešķiriet atļaujas abām Azure AD lietojumprogrammām personāla vadībā:</span><span class="sxs-lookup"><span data-stu-id="67cc0-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="67cc0-189">Lietojumprogramma, kas izveidota jūsu nomniekam Microsoft Azure portālā</span><span class="sxs-lookup"><span data-stu-id="67cc0-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="67cc0-190">Dynamics 365 HR Virtual Table programma, kas instalēta Power Apps vidē</span><span class="sxs-lookup"><span data-stu-id="67cc0-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="67cc0-191">Personāla vadībā atveriet **Azure Active Directory lietojumprogrammu** lapu.</span><span class="sxs-lookup"><span data-stu-id="67cc0-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="67cc0-192">Atlasiet **Jauns**, lai izveidotu jaunu lietojumprogrammas ierakstu:</span><span class="sxs-lookup"><span data-stu-id="67cc0-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="67cc0-193">Laukā **Klienta ID**, ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas klienta ID.</span><span class="sxs-lookup"><span data-stu-id="67cc0-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="67cc0-194">Laukā **Nosaukums** ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="67cc0-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="67cc0-195">Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="67cc0-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="67cc0-196">Atlasiet **Jauns**, lai izveidotu otru lietojumprogrammas ierakstu:</span><span class="sxs-lookup"><span data-stu-id="67cc0-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="67cc0-197">**Klienta Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="67cc0-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="67cc0-198">**Nosaukums**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="67cc0-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="67cc0-199">Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="67cc0-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="67cc0-200">Virtuālo tabulu ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="67cc0-200">Generate virtual tables</span></span>

<span data-ttu-id="67cc0-201">Kad iestatīšana ir pabeigta, varat atlasīt virtuālās tabulas, kuras vēlaties ģenerēt un iespējot savā Dataverse instancē.</span><span class="sxs-lookup"><span data-stu-id="67cc0-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="67cc0-202">Human Resources atveriet lapu **Dataverse integrācija**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="67cc0-203">Atlasiet cilni **Virtuālās tabulas**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="67cc0-204">Kad visa nepieciešamā uzstādīšana būs pabeigta, slēdzis **Iespējot virtuālo tabulu** automātiski tiks iestatīts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="67cc0-205">Ja slēdzis tiek iestatīts uz **Nē**, pārskatiet šā dokumenta iepriekšējās sadaļās norādītās darbības, lai nodrošinātu, ka visi priekšnosacījumu iestatīšana ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="67cc0-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="67cc0-206">Atlasiet tabulu vai tabulas, kuras vēlaties ģenerēt pakalpojumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67cc0-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="67cc0-207">Atlasiet **Ģenerēt/atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-207">Select **Generate/refresh**.</span></span>

![Dataverse integrācija](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="67cc0-209">Tabulas ģenerēšanas statusa pārbaude</span><span class="sxs-lookup"><span data-stu-id="67cc0-209">Check table generation status</span></span>

<span data-ttu-id="67cc0-210">Virtuālās tabulas pakalpojumā Dataverse tiek ģenerētas, izmantojot asinhronu fona procesu.</span><span class="sxs-lookup"><span data-stu-id="67cc0-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="67cc0-211">Procesa atjauninājumi tiek parādīti darbību centrā.</span><span class="sxs-lookup"><span data-stu-id="67cc0-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="67cc0-212">Detalizēta informācija par procesu, ieskaitot kļūdu žurnālus, tiek parādīta lapā **Procesa automatizācija**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="67cc0-213">Programmā Human Resources atveriet lapu **Procesa automatizācija**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="67cc0-214">Atlasiet cilni **Fona procesi**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="67cc0-215">Atlasiet **Virtuālo tabulu kopuma asinhronās darbības fona process**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="67cc0-216">Atlasiet **Skatīt pēdējos rezultātus**.</span><span class="sxs-lookup"><span data-stu-id="67cc0-216">Select **View most recent results**.</span></span>

<span data-ttu-id="67cc0-217">Nolaižamā saraksta rūtī tiek rādīti pēdējie procesa izpildes rezultāti.</span><span class="sxs-lookup"><span data-stu-id="67cc0-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="67cc0-218">Varat skatīt procesa žurnālu, tostarp visas kļūdas, kas atgrieztas no pakalpojuma Dataverse.</span><span class="sxs-lookup"><span data-stu-id="67cc0-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="67cc0-219">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="67cc0-219">See also</span></span>

[<span data-ttu-id="67cc0-220">Kas ir Dataverse?</span><span class="sxs-lookup"><span data-stu-id="67cc0-220">What is Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="67cc0-221">Tabulas Dataverse</span><span class="sxs-lookup"><span data-stu-id="67cc0-221">Tables in Dataverse</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="67cc0-222">Tabulas attiecību pārskats</span><span class="sxs-lookup"><span data-stu-id="67cc0-222">Table relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="67cc0-223">Izveidot un rediģēt virtuālās tabulas, kas satur datus no ārējo datu avota</span><span class="sxs-lookup"><span data-stu-id="67cc0-223">Create and edit virtual tables that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="67cc0-224">Kas ir Power Apps portāli?</span><span class="sxs-lookup"><span data-stu-id="67cc0-224">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="67cc0-225">Lietojumprogrammu izveides pārskats Power Apps</span><span class="sxs-lookup"><span data-stu-id="67cc0-225">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]