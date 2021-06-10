---
title: Dataverse virtuālo tabulu konfigurēšana
description: Šajā tēmā parādīts, kā konfigurēt virtuālās tabulas Dynamics 365 Human Resources. Ģenerējiet un atjauniniet esošās virtuālās tabulas un analizējiet ģenerētās un pieejamās tabulas.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8c2e207efe0eeec6fc7e679a6ae12edcb21b291f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058588"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="b36be-104">Dataverse virtuālo tabulu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b36be-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b36be-105">Dynamics 365 Human Resources ir virtuālais datu avots platformā Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b36be-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="b36be-106">Tas nodrošina pilnīgas izveides, lasīšanas, atjaunināšanas un dzēšanas (CRUD) operācijas no Dataverse un Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="b36be-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="b36be-107">Dati virtuālajām tabulām netiek saglabāti Dataverse, bet gan programmas datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="b36be-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="b36be-108">Lai iespējotu CRUD operācijas personāla vadības elementos no Dataverse, jums jāpadara šos elementus pieejamus kā virtuālas tabulas Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b36be-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="b36be-109">Tas ļauj veikt CRUD operācijas no Dataverse un Microsoft Power Platform personāla vadības datos.</span><span class="sxs-lookup"><span data-stu-id="b36be-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="b36be-110">Operācijas atbalsta arī pilnas biznesa loģikas personāla vadības pārbaudes, lai nodrošinātu datu integritāti, rakstot datus elementos.</span><span class="sxs-lookup"><span data-stu-id="b36be-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="b36be-111">Human Resources elementi atbilst Dataverse tabulām.</span><span class="sxs-lookup"><span data-stu-id="b36be-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="b36be-112">Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="b36be-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="b36be-113">Pieejamās virtuālās tabulas Human Resources</span><span class="sxs-lookup"><span data-stu-id="b36be-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="b36be-114">Visi atvērtie datu protokola (OData) elementi Human Resources ir pieejamas kā virtuālās tabulas Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b36be-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="b36be-115">Tie ir pieejami arī Power Platform.</span><span class="sxs-lookup"><span data-stu-id="b36be-115">They're also available in Power Platform.</span></span> <span data-ttu-id="b36be-116">Tagad varat veidot lietojumprogrammas un pieredzi ar datiem tieši no personāla vadības ar pilnām CRUD iespējām, nekopējot vai nesinhronizējot datus ar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b36be-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="b36be-117">Varat izmantot Power Apps portālus, lai veidotu tīmekļa vietnes ar ārējo piekļuvi, kas iespējo sadarbības scenārijus biznesa procesiem personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="b36be-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="b36be-118">Varat apskatīt vidē iespējoto virtuālo tabulu sarakstu un sākt darbu ar tabulām pakalpojumā [Power Apps](https://make.powerapps.com), **Dynamics 365 HR Virtual Tables** risinājumā.</span><span class="sxs-lookup"><span data-stu-id="b36be-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Dynamics 365 HR Virtual Tables pakalpojumā Power Apps](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="b36be-120">Virtuālās tabulas pret vietējām tabulām</span><span class="sxs-lookup"><span data-stu-id="b36be-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="b36be-121">Virtuālās Human Resources tabulas atšķiras no vietējām Dataverse tabulām, kas veidotas Human Resources vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="b36be-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="b36be-122">Vietējās tabulas Human Resources vajadzībām tiek veidotas atsevišķi un uzturētas kopējā HCM risinājumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b36be-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="b36be-123">Vietējo tabulu gadījumā dati tiek saglabāti Dataverse un tiem nepieciešama sinhronizācija ar Human Resources programmas datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="b36be-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="b36be-124">Vietējo Dataverse tabulu Human Resources vajadzībām sarakstu skatiet [Dataverse tabulas](./hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="b36be-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="b36be-125">Iestatīt</span><span class="sxs-lookup"><span data-stu-id="b36be-125">Setup</span></span>

<span data-ttu-id="b36be-126">Sekojiet šīm iestatīšanas darbībām, lai iespējotu virtuālās tabulas jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="b36be-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="b36be-127">Iespējot virtuālās tabulas Human Resources</span><span class="sxs-lookup"><span data-stu-id="b36be-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="b36be-128">Vispirms **Funkciju pārvaldības** darbvietā ir jāiespējo virtuālas tabulas.</span><span class="sxs-lookup"><span data-stu-id="b36be-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="b36be-129">Human Resources atlasiet **Sistēmas administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="b36be-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="b36be-130">Atlasiet elementu **Funkciju pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="b36be-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="b36be-131">Atlasiet **Virtuālās tabulas atbalsts HR programmā Dataverse** un pēc tam atlasiet **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="b36be-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="b36be-132">Lai iegūtu papildinformāciju par priekšskatījuma līdzekļu iespējošanu un atspējošanu, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="b36be-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="b36be-133">Lietojumprogrammas reģistrēšana Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="b36be-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="b36be-134">Vispirms jūsu Personāla vadības instance ir jāreģistrē Azure portālā, lai Microsoft Identity platforma var nodrošināt autentifikāciju un autorizācijas pakalpojumus lietojumprogrammai un lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="b36be-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="b36be-135">Lai iegūtu vairāk informācijas par lietojumprogrammu reģistrāciju Azure, skatiet [Īsa pamācība: lietojumprogrammas reģistrēšana platformā Microsoft Identity](/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="b36be-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="b36be-136">Atveriet [Microsoft Azure portālu](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="b36be-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="b36be-137">Azure pakalpojumu sarakstā atlasiet **Lietojumprogrammu reģistrācijas**.</span><span class="sxs-lookup"><span data-stu-id="b36be-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="b36be-138">Atlasiet **Jauna reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="b36be-138">Select **New registration**.</span></span>

4. <span data-ttu-id="b36be-139">Laukā **Nosaukums** ievadiet aprakstošu lietojumprogrammas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b36be-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="b36be-140">Piemēram, **Dynamics 365 Human Resources virtuālās tabulas**.</span><span class="sxs-lookup"><span data-stu-id="b36be-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="b36be-141">**Novirzīšanas URI** laukā ievadiet savas personāla vadības instances nosaukumvietas URL.</span><span class="sxs-lookup"><span data-stu-id="b36be-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="b36be-142">Atlasiet **Reģistrēt**.</span><span class="sxs-lookup"><span data-stu-id="b36be-142">Select **Register**.</span></span>

7. <span data-ttu-id="b36be-143">Kad reģistrācija pabeigta, Azure portālā tiek parādīta lietojumprogrammas reģistrācijas **pārskata** rūts, kurā ir ietverts tās **lietojumprogrammas (klienta) ID**.</span><span class="sxs-lookup"><span data-stu-id="b36be-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="b36be-144">Pašlaik ņemiet vērā **lietojumprogrammas (klienta) ID**.</span><span class="sxs-lookup"><span data-stu-id="b36be-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="b36be-145">Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālās tabulas datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="b36be-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="b36be-146">Kreisajā navigācijas rūtī atlasiet **sertifikāti un noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="b36be-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="b36be-147">Lapas sadaļā **Klienta noslēpumi** atlasiet **Jauns klienta noslēpums**.</span><span class="sxs-lookup"><span data-stu-id="b36be-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="b36be-148">Ievadiet aprakstu, atlasiet ilgumu un atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b36be-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="b36be-149">Ierakstiet neslēpuma vērtību no tabulas rekvizīta **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="b36be-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="b36be-150">Jūs ievadīsiet šo informāciju, kad [konfigurēsiet virtuālās tabulas datu avotu](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span><span class="sxs-lookup"><span data-stu-id="b36be-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="b36be-151">Pārliecinieties, ka ņemat vērā pašreizējo noslēpuma vērtību.</span><span class="sxs-lookup"><span data-stu-id="b36be-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="b36be-152">Pēc iziešanas no šīs lapas noslēpums nekad vairs netiek parādīts.</span><span class="sxs-lookup"><span data-stu-id="b36be-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="b36be-153">Dynamics 365 HR Virtual Tables programmas instalēšana</span><span class="sxs-lookup"><span data-stu-id="b36be-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="b36be-154">Instalējiet Dynamics 365 HR Virtual Tables programmu jūsu Power Apps vidē, lai izvietotu virtuālās tabulas risinājuma pakotni Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b36be-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="b36be-155">Human Resources atveriet lapu **Microsoft Dataverse integrācija**.</span><span class="sxs-lookup"><span data-stu-id="b36be-155">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="b36be-156">Atlasiet cilni **Virtuālās tabulas**.</span><span class="sxs-lookup"><span data-stu-id="b36be-156">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="b36be-157">Atlasiet **Instalēt virtuālās tabulas programmu**.</span><span class="sxs-lookup"><span data-stu-id="b36be-157">Select **Install virtual table app**.</span></span>

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="b36be-158">Virtuālās tabulas datu avota konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b36be-158">Configure the virtual table data source</span></span>

<span data-ttu-id="b36be-159">Nākamais solis ir konfigurēt virtuālās tabulas datu avotu Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="b36be-159">The next step is to configure the virtual table data source in the Power Apps environment.</span></span>

1. <span data-ttu-id="b36be-160">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b36be-160">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="b36be-161">Sarakstā **Vides** atlasiet ar jūsu personāla vadības instanci saistīto Power Apps vidi.</span><span class="sxs-lookup"><span data-stu-id="b36be-161">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="b36be-162">Atlasiet **Vides URL** lapas sadaļā **Detalizēti**.</span><span class="sxs-lookup"><span data-stu-id="b36be-162">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="b36be-163">**Risinājumu darbspējas centrmezglā** atlasiet ikonu **Detalizētā atrašana** lietojumprogrammas lapas augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="b36be-163">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="b36be-164">Lapā **Detalizētā atrašana**, nolaižamajā sarakstā **Meklēt** atlasiet **Finance and Operations virtuālo datu avotu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="b36be-164">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="b36be-165">Virtuālās tabulas programmas instalēšana no iepriekšējās iestatīšanas darbības var ilgt dažas minūtes.</span><span class="sxs-lookup"><span data-stu-id="b36be-165">The installation of the virtual table app from the previous setup step can take a few minutes.</span></span> <span data-ttu-id="b36be-166">Ja **Finance and Operations virtuālās datu avota konfigurācijas** nav pieejamas sarakstā, uzgaidiet kādu minūti un atsvaidziniet sarakstu.</span><span class="sxs-lookup"><span data-stu-id="b36be-166">If **Finance and Operations Virtual Data Source Configurations** isn't available in the list, wait for a minute and refresh the list.</span></span>

6. <span data-ttu-id="b36be-167">Atlasiet **Rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="b36be-167">Select **Results**.</span></span>

7. <span data-ttu-id="b36be-168">Atlasiet ierakstu **Microsoft HR datu avots**.</span><span class="sxs-lookup"><span data-stu-id="b36be-168">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="b36be-169">Ievadiet nepieciešamo informāciju par datu avota konfigurāciju:</span><span class="sxs-lookup"><span data-stu-id="b36be-169">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="b36be-170">**Mērķa URL**: jūsu personāla vadības nosaukumvietas URL.</span><span class="sxs-lookup"><span data-stu-id="b36be-170">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="b36be-171">Mērķa URL formāts ir:</span><span class="sxs-lookup"><span data-stu-id="b36be-171">The format of the target URL is:</span></span>
     
     <span data-ttu-id="b36be-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="b36be-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="b36be-173">Piemēram:</span><span class="sxs-lookup"><span data-stu-id="b36be-173">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="b36be-174">Noteikti iekļaujiet rakstzīmi "**/**" vietrāža URL beigās, lai izvairītos no kļūdas saņemšanas.</span><span class="sxs-lookup"><span data-stu-id="b36be-174">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="b36be-175">**Nomnieka ID**: Azure Active Directory (Azure AD) nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="b36be-175">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="b36be-176">**AAD lietojumprogrammas ID**: lietojumprogrammas (klienta) ID, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="b36be-176">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="b36be-177">Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="b36be-177">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="b36be-178">**AAD lietojumprogrammas noslēpums**: klienta noslēpums, kas izveidots Microsoft Azure portālā reģistrētai lietojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="b36be-178">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="b36be-179">Jūs saņēmāt šo informāciju iepriekš, veicot darbību [Lietojumprogrammas reģistrēšana Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span><span class="sxs-lookup"><span data-stu-id="b36be-179">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR datu avots](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="b36be-181">Atlasiet **Saglabāt un aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="b36be-181">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="b36be-182">Piešķiriet lietojumprogrammas atļaujas personāla vadībā</span><span class="sxs-lookup"><span data-stu-id="b36be-182">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="b36be-183">Piešķiriet atļaujas abām Azure AD lietojumprogrammām personāla vadībā:</span><span class="sxs-lookup"><span data-stu-id="b36be-183">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="b36be-184">Lietojumprogramma, kas izveidota jūsu nomniekam Microsoft Azure portālā</span><span class="sxs-lookup"><span data-stu-id="b36be-184">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="b36be-185">Dynamics 365 HR Virtual Table programma, kas instalēta Power Apps vidē</span><span class="sxs-lookup"><span data-stu-id="b36be-185">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="b36be-186">Personāla vadībā atveriet **Azure Active Directory lietojumprogrammu** lapu.</span><span class="sxs-lookup"><span data-stu-id="b36be-186">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="b36be-187">Atlasiet **Jauns**, lai izveidotu jaunu lietojumprogrammas ierakstu:</span><span class="sxs-lookup"><span data-stu-id="b36be-187">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="b36be-188">Laukā **Klienta ID**, ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas klienta ID.</span><span class="sxs-lookup"><span data-stu-id="b36be-188">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="b36be-189">Laukā **Nosaukums** ievadiet Microsoft Azure portālā reģistrētās lietojumprogrammas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b36be-189">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="b36be-190">Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="b36be-190">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="b36be-191">Atlasiet **Jauns**, lai izveidotu otru lietojumprogrammas ierakstu:</span><span class="sxs-lookup"><span data-stu-id="b36be-191">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="b36be-192">**Klienta Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="b36be-192">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="b36be-193">**Nosaukums**: Dynamics 365 HR Virtual Table</span><span class="sxs-lookup"><span data-stu-id="b36be-193">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="b36be-194">Laukā **Lietotāja ID** atlasiet tā lietotāja ID, kam ir administratora atļaujas personāla vadībā un Power Apps vidē.</span><span class="sxs-lookup"><span data-stu-id="b36be-194">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="b36be-195">Virtuālo tabulu ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="b36be-195">Generate virtual tables</span></span>

<span data-ttu-id="b36be-196">Kad iestatīšana ir pabeigta, varat atlasīt virtuālās tabulas, kuras vēlaties ģenerēt un iespējot savā Dataverse instancē.</span><span class="sxs-lookup"><span data-stu-id="b36be-196">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="b36be-197">Human Resources atveriet lapu **Microsoft Dataverse integrācija**.</span><span class="sxs-lookup"><span data-stu-id="b36be-197">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="b36be-198">Atlasiet cilni **Virtuālās tabulas**.</span><span class="sxs-lookup"><span data-stu-id="b36be-198">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="b36be-199">Kad visa nepieciešamā uzstādīšana būs pabeigta, slēdzis **Iespējot virtuālo tabulu** automātiski tiks iestatīts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b36be-199">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="b36be-200">Ja slēdzis tiek iestatīts uz **Nē**, pārskatiet šā dokumenta iepriekšējās sadaļās norādītās darbības, lai nodrošinātu, ka visi priekšnosacījumu iestatīšana ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="b36be-200">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="b36be-201">Atlasiet tabulu vai tabulas, kuras vēlaties ģenerēt pakalpojumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b36be-201">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="b36be-202">Atlasiet **Ģenerēt/atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="b36be-202">Select **Generate/refresh**.</span></span>

![Dataverse integrācija](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a><span data-ttu-id="b36be-204">Tabulas ģenerēšanas statusa pārbaude</span><span class="sxs-lookup"><span data-stu-id="b36be-204">Check table generation status</span></span>

<span data-ttu-id="b36be-205">Virtuālās tabulas pakalpojumā Dataverse tiek ģenerētas, izmantojot asinhronu fona procesu.</span><span class="sxs-lookup"><span data-stu-id="b36be-205">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="b36be-206">Procesa atjauninājumi tiek parādīti darbību centrā.</span><span class="sxs-lookup"><span data-stu-id="b36be-206">Updates on the process display in the action center.</span></span> <span data-ttu-id="b36be-207">Detalizēta informācija par procesu, ieskaitot kļūdu žurnālus, tiek parādīta lapā **Procesa automatizācija**.</span><span class="sxs-lookup"><span data-stu-id="b36be-207">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="b36be-208">Programmā Human Resources atveriet lapu **Procesa automatizācija**.</span><span class="sxs-lookup"><span data-stu-id="b36be-208">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="b36be-209">Atlasiet cilni **Fona procesi**.</span><span class="sxs-lookup"><span data-stu-id="b36be-209">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="b36be-210">Atlasiet **Virtuālo tabulu kopuma asinhronās darbības fona process**.</span><span class="sxs-lookup"><span data-stu-id="b36be-210">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="b36be-211">Atlasiet **Skatīt pēdējos rezultātus**.</span><span class="sxs-lookup"><span data-stu-id="b36be-211">Select **View most recent results**.</span></span>

<span data-ttu-id="b36be-212">Nolaižamā saraksta rūtī tiek rādīti pēdējie procesa izpildes rezultāti.</span><span class="sxs-lookup"><span data-stu-id="b36be-212">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="b36be-213">Varat skatīt procesa žurnālu, tostarp visas kļūdas, kas atgrieztas no pakalpojuma Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b36be-213">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="b36be-214">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="b36be-214">See also</span></span>

[<span data-ttu-id="b36be-215">Kas ir Dataverse?</span><span class="sxs-lookup"><span data-stu-id="b36be-215">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="b36be-216">Tabulas Dataverse</span><span class="sxs-lookup"><span data-stu-id="b36be-216">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="b36be-217">Tabulas attiecību pārskats</span><span class="sxs-lookup"><span data-stu-id="b36be-217">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="b36be-218">Izveidot un rediģēt virtuālās tabulas, kas satur datus no ārējo datu avota</span><span class="sxs-lookup"><span data-stu-id="b36be-218">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="b36be-219">Kas ir Power Apps portāli?</span><span class="sxs-lookup"><span data-stu-id="b36be-219">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="b36be-220">Lietojumprogrammu izveides pārskats Power Apps</span><span class="sxs-lookup"><span data-stu-id="b36be-220">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
