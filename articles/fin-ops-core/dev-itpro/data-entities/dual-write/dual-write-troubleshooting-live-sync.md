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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59c8bd80b167cdfaa7a65e469f4dc7ebf8f50844
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744617"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="22a50-103">Tiešsaistes sinhronizācijas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="22a50-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="22a50-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="22a50-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="22a50-105">Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar tiešsaistes sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="22a50-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22a50-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="22a50-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="22a50-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="22a50-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="22a50-108">Tiešsaistes sinhronizācija rāda kļūdu 403 Aizliegts, kad veidojat rindu programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="22a50-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="22a50-109">Izveidojot rindu Finance and Operations programmā, iespējams, saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="22a50-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="22a50-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"ziņojums\\":\\"Lietotājs nav organizācijas dalībnieks.\\"}}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts."}}".*</span><span class="sxs-lookup"><span data-stu-id="22a50-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="22a50-111">Lai labotu problēmu, izpildiet darbības, kas norādītas rakstā [Sistēmas prasības un priekšnosacījumi](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="22a50-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="22a50-112">Lai izpildītu šīs darbības, duālā ieraksta programmas lietotājiem, kas izveidoti sistēmā Dataverse, ir jābūt sistēmas administratora lomai.</span><span class="sxs-lookup"><span data-stu-id="22a50-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="22a50-113">Arī atbildīgajai noklusējuma komandai ir jābūt sistēmas administratora lomai.</span><span class="sxs-lookup"><span data-stu-id="22a50-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="22a50-114">Tiešsaistes sinhronizācija jebkurai tabulai nepārtraukti rāda līdzīgu kļūdu, veidojot rindu programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="22a50-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="22a50-115">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="22a50-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="22a50-116">Varat saņemt kļūdas ziņojumu, piemēram, katru reizi, kad mēģināt saglabāt tabulas datus programmā Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="22a50-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="22a50-117">*Nevar saglabāt izmaiņas datu bāzē. Darba vienība nevar izpildīt transakciju. Nevar rakstīt datus elementa mērvienībās. Ieraksti UnitOfMeasureEntity neizdevās ar kļūdas ziņojumu Nevar sinhronizēt ar elementa mērvienībām.*</span><span class="sxs-lookup"><span data-stu-id="22a50-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="22a50-118">Lai atrisinātu problēmu, jums jāpārliecinās, ka priekšnosacījumu atsauces dati ir gan Finance and Operations, gan Dataverse.</span><span class="sxs-lookup"><span data-stu-id="22a50-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="22a50-119">Piemēram, ja klients, kura Finance and Operations programmā esat, pieder noteiktai klientu grupai, pārliecinieties, ka šī klientu grupa pastāv sistēmā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="22a50-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="22a50-120">Ja dati ir abās pusēs un apstiprinājāt, ka problēma nav saistīta ar datiem, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="22a50-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="22a50-121">Apturiet saistīto tabulu.</span><span class="sxs-lookup"><span data-stu-id="22a50-121">Stop the related table.</span></span>
2. <span data-ttu-id="22a50-122">Piesakieties Finance and Operations programmā un pārliecinieties, ka tabulās DualWriteProjectConfiguration un DualWriteProjectFieldConfiguration ir kļūmīgās rindas ieraksti.</span><span class="sxs-lookup"><span data-stu-id="22a50-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="22a50-123">Šādi izskatās, piemēram, vaicājums, ja ir kļūdaina tabula **Klienti**.</span><span class="sxs-lookup"><span data-stu-id="22a50-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="22a50-124">Ja neveiksmīgajai rindai ir ieraksti pat pēc tabulas kartēšanas apturēšanas, dzēsiet rindas, kas ir saistītas ar neveiksmīgo tabulu.</span><span class="sxs-lookup"><span data-stu-id="22a50-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="22a50-125">Atzīmējiet kolonnu **projectname** tabulā DualWriteProjectConfiguration un ienesiet ierakstu DualWriteProjectFieldConfiguration tabulā, izmantojot projekta nosaukumu, lai dzēstu rindu.</span><span class="sxs-lookup"><span data-stu-id="22a50-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="22a50-126">Sāciet tabulas kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="22a50-126">Start the table mapping.</span></span> <span data-ttu-id="22a50-127">Pārbaudiet, vai dati ir sinhronizēti bez jebkādām problēmām.</span><span class="sxs-lookup"><span data-stu-id="22a50-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="22a50-128">Apstrādāt lasīšanas vai rakstīšanas privilēģiju kļūdas, kad Finance and Operations programmā tiek veidoti dati</span><span class="sxs-lookup"><span data-stu-id="22a50-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="22a50-129">Iespējams, saņemsit kļūdas ziņojumu "Nederīgs pieprasījums", kas līdzīgs šim piemēram, kad Finance and Operations programmā veidojat datus.</span><span class="sxs-lookup"><span data-stu-id="22a50-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Slikta pieprasījuma kļūmes ziņojuma piemērs](media/error_record_id_source.png)

<span data-ttu-id="22a50-131">Lai labotu problēmu, ir jāpiešķir pareiza drošības loma kartētas Dynamics 365 Sales vai Dynamics 365 Customer Service biznesa struktūrvienības grupai, lai iespējotu trūkstošās privilēģijas.</span><span class="sxs-lookup"><span data-stu-id="22a50-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="22a50-132">Programmā Finance and Operations atrodiet biznesa struktūrvienību, kas ir kartēta datu integrācijas savienojuma kopā.</span><span class="sxs-lookup"><span data-stu-id="22a50-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organizācijas kartēšana](media/mapped_business_unit.png)

2. <span data-ttu-id="22a50-134">Piesakieties vidē ar modeļa vadītu Dynamics 365 programmu, pārejiet uz **Iestatījumi \> Drošība** un sameklējiet kartētās biznesa vienības grupu.</span><span class="sxs-lookup"><span data-stu-id="22a50-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Kartētās biznesa vienības grupa](media/setting_security_page.png)

3. <span data-ttu-id="22a50-136">Atveriet komandas lapu rediģēšanai, pēc tam atlasiet **Pārvaldīt lomas**, lai atvērtu dialoglodziņu **Pārvaldīt grupu lomas**.</span><span class="sxs-lookup"><span data-stu-id="22a50-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Lomu pārvaldības poga](media/manage_team_roles.png)

4. <span data-ttu-id="22a50-138">Piešķiriet lomu ar lasīšanas/rakstīšanas privilēģiju attiecīgajām tabulām un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="22a50-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="22a50-139">Labot sinhronizācijas problēmas vidē, kurai ir nesen mainījusies Dataverse vide</span><span class="sxs-lookup"><span data-stu-id="22a50-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="22a50-140">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="22a50-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="22a50-141">Veidojot datus Finance and Operations programmā, iespējams, saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="22a50-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="22a50-142">*{"entityName": "CustCustomerV3Entity", "executionStatus": 2, "fieldResponses":\[\], "recordResponses":\[{"errorMessage": "**Nevar ģenerēt lietderīgās vērtības elementam CustCustomerV3Entity**", "logDateTime": "2019-08-27T 18:51:52.5843124Z", "verboseError": "Lietderīgas vērtības izveide neizdevās, kļūdas dēļ Nederīgs URI: URI ir tukšs." }\], "isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="22a50-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="22a50-143">Šādi izskatās kļūda modeļa vadītā Dynamics 365 lietojumprogrammā:</span><span class="sxs-lookup"><span data-stu-id="22a50-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="22a50-144">*No ISV koda radās neparedzēta kļūda. (ErrorType = ClientError) Negaidīts izņēmums no spraudņa (Izpildīt): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: neizdevās apstrādāt elementa kontu — (savienojuma izveides mēģinājums neizdevās, jo savienotā puse pēc noteikta laikposma nav atbilstoši atbildējusi vai izveidotais savienojums neizdevās, jo savienotais resursdators nav atbildējis*</span><span class="sxs-lookup"><span data-stu-id="22a50-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="22a50-145">Šī kļūda rodas, ja Dataverse vide tiek nepareizi atiestatīta tajā pašā laikā, kad mēģināt izveidot datus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="22a50-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="22a50-146">Lai novērstu problēmu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="22a50-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="22a50-147">Piesakieties Finance and Operations virtuālajā mašīnā (VM), atveriet SQL Server Management Studio (SSMS) un meklējiet rindas DUALWRITEPROJECTCONFIGURATIONENTITY tabulā, kur **internalentityname** ir vienāds ar **Klienti V3** un **externalentityname** ir vienāds ar **konti**.</span><span class="sxs-lookup"><span data-stu-id="22a50-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="22a50-148">Šādi izskatās vaicājums.</span><span class="sxs-lookup"><span data-stu-id="22a50-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="22a50-149">Izmantojiet projekta nosaukumu no iepriekšējā vaicājuma rezultātus, lai palaistu šo vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="22a50-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="22a50-150">Pārliecinieties, vai **externalenvironmentURL** kolonnai ir pareizs Dataverse vai programmas vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="22a50-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="22a50-151">Dzēsiet visas dublētās rindas, kas norāda nepareizu Dataverse vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="22a50-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="22a50-152">Dzēsiet atbilstošās rindas DUALWRITEPROJECTFIELDCONFIGURATION un DUALWRITEPROJECTCONFIGURATION tabulās.</span><span class="sxs-lookup"><span data-stu-id="22a50-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="22a50-153">Tabulas kartēšanas apturēšana un pēc tam atsākšana</span><span class="sxs-lookup"><span data-stu-id="22a50-153">Stop the table mapping, and then restart it</span></span>
