---
title: Tiešsaistes sinhronizācijas problēmu novēršana
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar tiešsaistes sinhronizāciju.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d45b19c1e88e6a27bde4335d4a356f2173bdfcd3
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275421"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="91566-103">Tiešsaistes sinhronizācijas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="91566-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="91566-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="91566-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="91566-105">Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar tiešsaistes sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="91566-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91566-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="91566-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="91566-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="91566-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="91566-108">Tiešsaistes sinhronizācija rāda kļūdu 403 Aizliegts, kad veidojat ierakstu programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="91566-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="91566-109">Izveidojot ierakstu Finance and Operations programmā, iespējams, saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="91566-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="91566-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"ziņojums\\":\\"Lietotājs nav organizācijas dalībnieks.\\"}}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts."}}".*</span><span class="sxs-lookup"><span data-stu-id="91566-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="91566-111">Lai labotu problēmu, izpildiet darbības, kas norādītas rakstā [Sistēmas prasības un priekšnosacījumi](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="91566-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="91566-112">Lai izpildītu šīs darbības, duālā ieraksta programmas lietotājiem, kas izveidoti sistēmā Common Data Service, ir jābūt sistēmas administratora lomai.</span><span class="sxs-lookup"><span data-stu-id="91566-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="91566-113">Arī atbildīgajai noklusējuma komandai ir jābūt sistēmas administratora lomai.</span><span class="sxs-lookup"><span data-stu-id="91566-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="91566-114">Tiešsaistes sinhronizācija jebkuram elementam nepārtraukti rāda līdzīgu kļūdu, kad veidojat ierakstu programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="91566-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="91566-115">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="91566-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="91566-116">Varat saņemt kļūdas ziņojumu, piemēram, katru reizi, kad mēģināt saglabāt elementa datus Finance and Operations programmā:</span><span class="sxs-lookup"><span data-stu-id="91566-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="91566-117">*Nevar saglabāt izmaiņas datu bāzē. Darba vienība nevar izpildīt transakciju. Nevar rakstīt datus elementa mērvienībās. Ieraksti UnitOfMeasureEntity neizdevās ar kļūdas ziņojumu Nevar sinhronizēt ar elementa mērvienībām.*</span><span class="sxs-lookup"><span data-stu-id="91566-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="91566-118">Lai atrisinātu problēmu, jums jāpārliecinās, ka priekšnosacījumu atsauces dati ir gan Finance and Operations, gan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="91566-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="91566-119">Piemēram, ja klients, kura Finance and Operations programmā esat, pieder noteiktai klientu grupai, pārliecinieties, ka šī klientu grupa pastāv sistēmā Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="91566-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="91566-120">Ja dati ir abās pusēs un apstiprinājāt, ka problēma nav saistīta ar datiem, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="91566-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="91566-121">Apturiet saistīto elementu.</span><span class="sxs-lookup"><span data-stu-id="91566-121">Stop the related entity.</span></span>
2. <span data-ttu-id="91566-122">Piesakieties Finance and Operations programmā un pārliecinieties, ka tabulās DualWriteProjectConfiguration un DualWriteProjectFieldConfiguration ir kļūmīgā elementa ieraksti.</span><span class="sxs-lookup"><span data-stu-id="91566-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="91566-123">Šādi izskatās, piemēram, vaicājums, ja ir neveiksmīgs elements **Klienti**.</span><span class="sxs-lookup"><span data-stu-id="91566-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="91566-124">Ja neveiksmīgam elementam ir ieraksti pat pēc elementa kartēšanas apturēšanas, dzēsiet ierakstus, kas ir saistīti ar neveiksmīgo elementu.</span><span class="sxs-lookup"><span data-stu-id="91566-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="91566-125">Atzīmējiet kolonnu **projectname** tabulā DualWriteProjectConfiguration un ienesiet ierakstu DualWriteProjectFieldConfiguration tabulā, izmantojot projekta nosaukumu, lai dzēstu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="91566-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="91566-126">Sāciet elementa kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="91566-126">Start the entity mapping.</span></span> <span data-ttu-id="91566-127">Pārbaudiet, vai dati ir sinhronizēti bez jebkādām problēmām.</span><span class="sxs-lookup"><span data-stu-id="91566-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="91566-128">Apstrādāt lasīšanas vai rakstīšanas privilēģiju kļūdas, kad Finance and Operations programmā tiek veidoti dati</span><span class="sxs-lookup"><span data-stu-id="91566-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="91566-129">Iespējams, saņemsit kļūdas ziņojumu "Nederīgs pieprasījums", kas līdzīgs šim piemēram, kad Finance and Operations programmā veidojat datus.</span><span class="sxs-lookup"><span data-stu-id="91566-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Slikta pieprasījuma kļūmes ziņojuma piemērs](media/error_record_id_source.png)

<span data-ttu-id="91566-131">Lai labotu problēmu, ir jāpiešķir pareiza drošības loma kartētas Dynamics 365 Sales vai Dynamics 365 Customer Service biznesa struktūrvienības grupai, lai iespējotu trūkstošās privilēģijas.</span><span class="sxs-lookup"><span data-stu-id="91566-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="91566-132">Programmā Finance and Operations atrodiet biznesa struktūrvienību, kas ir kartēta datu integrācijas savienojuma kopā.</span><span class="sxs-lookup"><span data-stu-id="91566-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organizācijas kartēšana](media/mapped_business_unit.png)

2. <span data-ttu-id="91566-134">Piesakieties vidē ar modeļa vadītu Dynamics 365 programmu, pārejiet uz **Iestatījumi \> Drošība** un sameklējiet kartētās biznesa vienības grupu.</span><span class="sxs-lookup"><span data-stu-id="91566-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Kartētās biznesa vienības grupa](media/setting_security_page.png)

3. <span data-ttu-id="91566-136">Atveriet komandas lapu rediģēšanai, pēc tam atlasiet **Pārvaldīt lomas**, lai atvērtu dialoglodziņu **Pārvaldīt grupu lomas**.</span><span class="sxs-lookup"><span data-stu-id="91566-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Lomu pārvaldības poga](media/manage_team_roles.png)

4. <span data-ttu-id="91566-138">Piešķiriet lomu ar lasīšanas/rakstīšanas privilēģiju attiecīgajiem elementiem un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="91566-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="91566-139">Labot sinhronizācijas problēmas vidē, kurai ir nesen mainījusies Common Data Service vide</span><span class="sxs-lookup"><span data-stu-id="91566-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="91566-140">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="91566-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="91566-141">Veidojot datus Finance and Operations programmā, iespējams, saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="91566-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="91566-142">*{"entityName": "CustCustomerV3Entity", "executionStatus": 2, "fieldResponses":\[\], "recordResponses":\[{"errorMessage": "**Nevar ģenerēt lietderīgās vērtības elementam CustCustomerV3Entity**", "logDateTime": "2019-08-27T 18:51:52.5843124Z", "verboseError": "Lietderīgas vērtības izveide neizdevās, kļūdas dēļ Nederīgs URI: URI ir tukšs." }\], "isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="91566-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="91566-143">Šādi izskatās kļūda modeļa vadītā Dynamics 365 lietojumprogrammā:</span><span class="sxs-lookup"><span data-stu-id="91566-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="91566-144">*No ISV koda radās neparedzēta kļūda. (ErrorType = ClientError) Negaidīts izņēmums no spraudņa (Izpildīt): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: neizdevās apstrādāt elementa kontu — (savienojuma izveides mēģinājums neizdevās, jo savienotā puse pēc noteikta laikposma nav atbilstoši atbildējusi vai izveidotais savienojums neizdevās, jo savienotais resursdators nav atbildējis*</span><span class="sxs-lookup"><span data-stu-id="91566-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="91566-145">Šī kļūda rodas, ja Common Data Service vide tiek nepareizi atiestatīta tajā pašā laikā, kad mēģināt izveidot datus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="91566-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="91566-146">Lai novērstu problēmu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="91566-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="91566-147">Piesakieties Finance and Operations virtuālajā mašīnā (VM), atveriet SQL Server Management Studio (SSMS) un meklējiet ierakstus DUALWRITEPROJECTCONFIGURATIONENTITY tabulā, kur **internalentityname** ir vienāds ar **Klienti V3** un **externalentityname** ir vienāds ar **konti**.</span><span class="sxs-lookup"><span data-stu-id="91566-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="91566-148">Šādi izskatās vaicājums.</span><span class="sxs-lookup"><span data-stu-id="91566-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="91566-149">Izmantojiet projekta nosaukumu no iepriekšējā vaicājuma rezultātus, lai palaistu šo vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="91566-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="91566-150">Pārliecinieties, vai **externalenvironmentURL** kolonnai ir pareizs Common Data Service vai programmas vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="91566-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="91566-151">Dzēsiet visus dublētos ierakstus, kas norāda nepareizu Common Data Service vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="91566-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="91566-152">Dzēsiet atbilstošos ierakstus DUALWRITEPROJECTFIELDCONFIGURATION un DUALWRITEPROJECTCONFIGURATION tabulās.</span><span class="sxs-lookup"><span data-stu-id="91566-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="91566-153">Apturēt elementa kartēšanu un pēc tam to atsākt</span><span class="sxs-lookup"><span data-stu-id="91566-153">Stop the entity mapping, and then restart it</span></span>
