---
title: Bieži uzdotie jautājumi par Dynamics 365 Talent integrāciju ar Dynamics 365 Finance
description: Šajā tēmā ir paskaidrots, kādi dati tiek sinhronizēti risinājumu Talent un Finance integrācijas laikā.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5bb855e6dd7ff236b7bda9e59e12ed8cc8ab9bc9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251018"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="e279e-103">Bieži uzdotie jautājumi par Dynamics 365 Talent integrāciju ar Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="e279e-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e279e-104">Šajā tēmā ir sniegtas atbildes uz bieži uzdotiem jautājumiem par to, kādi dati tiek sinhronizēti, integrējot Dynamics 365 Talent ar Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="e279e-105">Vai tiek sinhronizēti visi dati vai tikai daži datu elementi?</span><span class="sxs-lookup"><span data-stu-id="e279e-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="e279e-106">Core HR gadījumā tiek sinhronizēta datu apakškopa.</span><span class="sxs-lookup"><span data-stu-id="e279e-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="e279e-107">Visu elementu sarakstu skatiet tēmā [Integrācija no Dynamics 365 Talent uz Dynamics 365 Finance](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="e279e-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="e279e-108">Attract un Onboard gadījumā visi dati tiek iegūti no Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e279e-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="e279e-109">Vai var izveidot jaunu kartējumu, neizmantojot veidnes?</span><span class="sxs-lookup"><span data-stu-id="e279e-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="e279e-110">Veidnes ir sākumpunkts.</span><span class="sxs-lookup"><span data-stu-id="e279e-110">Templates are the starting point.</span></span> <span data-ttu-id="e279e-111">Varat izveidot savu veidni, taču veidne vienmēr ir nepieciešama, veidojot integrācijas projektu.</span><span class="sxs-lookup"><span data-stu-id="e279e-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="e279e-112">Plašāku informāciju par datu integrētāju (DI), veidnēm un projektiem skatiet rakstā [Datu integrēšana pakalpojumā Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="e279e-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="e279e-113">Vai var kartēt finanšu dimensijas pārsūtīšanai starp Talent un Finance?</span><span class="sxs-lookup"><span data-stu-id="e279e-113">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="e279e-114">Finanšu dimensijas pašlaik nav pakalpojumā Common Data Service un līdz ar to nav noklusējuma veidnes sastāvdaļa.</span><span class="sxs-lookup"><span data-stu-id="e279e-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="e279e-115">Šis elements ir plānots, bet pašlaik nav zināms izlaišanas laiks.</span><span class="sxs-lookup"><span data-stu-id="e279e-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="e279e-116">Tādu datu gadījumā, kuri atrodas risinājumā Finance, bet kuru nav risinājumā Talent, saistiet abas sistēmas kopā, izmantojot vienumu **Konfigurēt saites** risinājumā Talent.</span><span class="sxs-lookup"><span data-stu-id="e279e-116">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="e279e-117">Plašāku informāciju par to, kā konfigurēt saites starp Talent un Finance, skatiet tēmā [Jaunumi un izmaiņas programmā Dynamics 365 Talent: Core HR (2018. gada 31. oktobris)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="e279e-117">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![Kartēt finanšu dimensijas](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="e279e-119">Dažreiz, importējot darbiniekus, tie tiek iekļauti neaktīvo darbinieku sarakstā risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-119">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="e279e-120">Kādēļ?</span><span class="sxs-lookup"><span data-stu-id="e279e-120">Why?</span></span>

<span data-ttu-id="e279e-121">Šī kļūda var rasties, ja darbiniekiem nav aktīva nodarbinātības detalizētas informācijas ieraksta risinājumā Talent.</span><span class="sxs-lookup"><span data-stu-id="e279e-121">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="e279e-122">Lai to atrisinātu, atveriet sadaļu **Personāla vadība \> Darbinieki \> Nodarbinātības vēsture \> Datumu pārvaldnieks** un pārbaudiet, vai ir aktīvs nodarbinātības detalizētas informācijas ieraksts.</span><span class="sxs-lookup"><span data-stu-id="e279e-122">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="e279e-123">Vai, izvēloties kartēt tikai lauku apakškopu, izmaiņas, kas veiktas nekartētiem laukiem, izraisīs sinhronizāciju?</span><span class="sxs-lookup"><span data-stu-id="e279e-123">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="e279e-124">Datu sinhronizācija tiek veikta saskaņā ar izpildes grafiku.</span><span class="sxs-lookup"><span data-stu-id="e279e-124">Data sync follows the execution schedule.</span></span> <span data-ttu-id="e279e-125">Integrācija ņems vērā ierakstu, ja ir mainīts kāds no ieraksta laukiem neatkarīgi no tā, vai lauks ietilpst integrācijas kartējumā.</span><span class="sxs-lookup"><span data-stu-id="e279e-125">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="e279e-126">Kā var nosūtīt tikai aktīvo nodarbināto izmaiņas, nevis pārtrauktu darba attiecību ierakstus?</span><span class="sxs-lookup"><span data-stu-id="e279e-126">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="e279e-127">Ar opciju “Papildu vaicājums” varat filtrēt un pārveidot avota datus pirms to nosūtīšanas uz galamērķi.</span><span class="sxs-lookup"><span data-stu-id="e279e-127">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Aktīvo darbinieku papildu vaicājums](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="e279e-129">Vai var norādīt, kurus laukus nosūtīt uz risinājumu Finance konkrētam elementam?</span><span class="sxs-lookup"><span data-stu-id="e279e-129">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="e279e-130">Laukus var pievienot vai noņemt no integrācijas uzdevuma.</span><span class="sxs-lookup"><span data-stu-id="e279e-130">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="e279e-131">Ne visi datu lauki, kas pastāv pakalpojuma Common Data Service elementā, tiks aizpildīti no Core HR.</span><span class="sxs-lookup"><span data-stu-id="e279e-131">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="e279e-132">Papildu datus var aizpildīt, izmantojot PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e279e-132">Additional data can be populated via PowerApps.</span></span>

![Pievienot vai noņemt laukus no integrācijas uzdevuma](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="e279e-134">Es iestatīju integrāciju kā pakešuzdevumu, bet tika zaudēts risinājuma Talent savienojums ar mērķa sistēmu.</span><span class="sxs-lookup"><span data-stu-id="e279e-134">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="e279e-135">Kā var nosūtīt to pašu izmaiņu kopumu uz mērķa sistēmu?</span><span class="sxs-lookup"><span data-stu-id="e279e-135">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="e279e-136">Izņēmumu apstrādei nav nepieciešama īpaša iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="e279e-136">No special setup is required for exception handling.</span></span> <span data-ttu-id="e279e-137">Datu integrētājs automātiski konstatēs un ziņos par kļūdām, kas notiek avota un mērķa sistēmā, un ļaus manuāli veikt atkārtotu mēģinājumu.</span><span class="sxs-lookup"><span data-stu-id="e279e-137">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="e279e-138">Tomēr tas neļauj manuāli veikt datu korekciju.</span><span class="sxs-lookup"><span data-stu-id="e279e-138">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="e279e-139">Ja ir nepieciešami datu atjauninājumi, tie jāveic avota vai mērķa sistēmā.</span><span class="sxs-lookup"><span data-stu-id="e279e-139">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="e279e-140">Vai var iestatīt divvirzienu integrāciju?</span><span class="sxs-lookup"><span data-stu-id="e279e-140">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="e279e-141">Nē, pašlaik tiek nodrošināta vienvirziena integrācija (no Talent uz Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="e279e-141">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="e279e-142">Tomēr ir pieejama noklusējuma veidne datu sūtīšanai no Talent uz Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-142">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="e279e-143">Vai var atļaut ieraksta dzēšanu integrācijas ietvaros?</span><span class="sxs-lookup"><span data-stu-id="e279e-143">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="e279e-144">Nē, datu integrētājs nevarēs iegūt dzēstos ierakstus datu pārsūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="e279e-144">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="e279e-145">Pašlaik ir iekļauta tikai datu izveide un atjauninājumi (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="e279e-145">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="e279e-146">Vai var atkārtoti palaist izpildi ar kļūdām?</span><span class="sxs-lookup"><span data-stu-id="e279e-146">Can I rerun the errored execution?</span></span> <span data-ttu-id="e279e-147">Ja tas tā ir, vai tiks nosūtīts fails pilnībā vai tikai izmaiņas?</span><span class="sxs-lookup"><span data-stu-id="e279e-147">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="e279e-148">Pirmoreiz palaižot datu integrētāju, vienmēr tiek veikta pilna izpilde.</span><span class="sxs-lookup"><span data-stu-id="e279e-148">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="e279e-149">Turpmāko palaišanas reižu pamatā ir izmaiņu izsekošana.</span><span class="sxs-lookup"><span data-stu-id="e279e-149">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="e279e-150">Izpildot kļūdainu palaišanu, tiek izgūti ieraksti palaišanas ietvaros un tiek nosūtītas jaunākās izmaiņas no Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e279e-150">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="e279e-151">Saglabājot projektu, tiek parādīts kļūdas ziņojums: “Projektam ir kartēšanas kļūdas.”</span><span class="sxs-lookup"><span data-stu-id="e279e-151">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="e279e-152">Ko darīt?</span><span class="sxs-lookup"><span data-stu-id="e279e-152">What do I do?</span></span>

<span data-ttu-id="e279e-153">Pārbaudiet integrācijas atslēgu iestatījumus, veiciet nepieciešamās izmaiņas iestatījumos un pēc tam atsvaidziniet projekta elementus.</span><span class="sxs-lookup"><span data-stu-id="e279e-153">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="e279e-154">Ja tiek izmantota noklusējuma veidne, integrācijas atslēgas tiks importētas automātiski.</span><span class="sxs-lookup"><span data-stu-id="e279e-154">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="e279e-155">Šī problēma var rasties, pievienojot jaunus uzdevumus esošai veidnei.</span><span class="sxs-lookup"><span data-stu-id="e279e-155">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="e279e-156">Ja ir noteikts skaits N juridisko personu, kurās nodarbinātajiem ir iestatītas nodarbinātības, vai ir jāveido kartējums katrai no tām?</span><span class="sxs-lookup"><span data-stu-id="e279e-156">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="e279e-157">Jā, katrai juridiskajai personai risinājumā Finance ir nepieciešams atsevišķs integrācijas projekts datu integrācijas ietvaros.</span><span class="sxs-lookup"><span data-stu-id="e279e-157">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="e279e-158">Ir nepieciešams pārsūtīt datus, kas nav daļa no Microsoft nodrošinātās noklusējuma veidnes.</span><span class="sxs-lookup"><span data-stu-id="e279e-158">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="e279e-159">Vai to var izdarīt?</span><span class="sxs-lookup"><span data-stu-id="e279e-159">Can I do this?</span></span>

<span data-ttu-id="e279e-160">Jā, esošajai veidnei var pievienot vai noņemt laukus.</span><span class="sxs-lookup"><span data-stu-id="e279e-160">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="e279e-161">Veidni var modificēt, lai iekļautu papildu datus no citiem Common Data Service elementiem.</span><span class="sxs-lookup"><span data-stu-id="e279e-161">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="e279e-162">Lai elements tiktu iekļauts veidnē, tam ir jāatrodas pakalpojumā Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e279e-162">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="e279e-163">Es tikko izveidoju jaunas Finance un Talent vides, un tiek rādīts kļūdas ziņojums “Datu vērtība ir ārpus integritātes ierobežojumiem”.</span><span class="sxs-lookup"><span data-stu-id="e279e-163">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="e279e-164">Kādēļ?</span><span class="sxs-lookup"><span data-stu-id="e279e-164">Why?</span></span>

<span data-ttu-id="e279e-165">Minētajai kļūdai var būt šādi iemesli:</span><span class="sxs-lookup"><span data-stu-id="e279e-165">Reasons for this error can include:</span></span>

- <span data-ttu-id="e279e-166">Datu pārsūtīšanas dēļ avotā (Common Data Service) tika izgūti dublēti ieraksti.</span><span class="sxs-lookup"><span data-stu-id="e279e-166">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="e279e-167">Datu pārsūtīšanai ir nulles vērtības laukiem, kas ir nepieciešami risinājumā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e279e-167">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="e279e-168">Pārbaudiet, vai dati, kas atrodas pakalpojumā Common Data Service, atbilst Finance and Operations prasībām.</span><span class="sxs-lookup"><span data-stu-id="e279e-168">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="e279e-169">Ja radušās izpildes kļūdas un darbinieka ID netika sinhronizēts, kā atrast vēsturē darbu, kurā ir nesekmīgi apstrādātais darbinieka ieraksts?</span><span class="sxs-lookup"><span data-stu-id="e279e-169">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="e279e-170">Datu integrētājs izveidos vairākus projektus risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-170">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="e279e-171">Relācija starp datu integrētāja uzdevumu un Finance projektu ir viens pret vienu.</span><span class="sxs-lookup"><span data-stu-id="e279e-171">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="e279e-172">Izsekojiet laiku datu integrētāja izpildes vēsturē un meklējiet projektu ar vērtību “indekss -1” risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-172">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="e279e-173">Ja datu integrētājā uzdevuma numurs ir 9, indekss risinājumā Finance ir 8.</span><span class="sxs-lookup"><span data-stu-id="e279e-173">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="e279e-174">Iegūstiet uzdevuma indeksu no datu integrētāja (šajā piemērā tas ir “9”).</span><span class="sxs-lookup"><span data-stu-id="e279e-174">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Uzdevuma indeksa iegūšana no datu integrētāja](media/CaptureTaskIndex.png)

2. <span data-ttu-id="e279e-176">Izsekojiet projekta izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="e279e-176">Track the execution time of the project.</span></span>

![Projekta izpildes laika izsekošana](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="e279e-178">Risinājumā Finance norādiet indeksu-1.</span><span class="sxs-lookup"><span data-stu-id="e279e-178">In Finance, identify index - 1.</span></span> <span data-ttu-id="e279e-179">Šajā piemērā projekts ar sufiksu “8” un projekta ar indeksu “0” izpildes laiks atbilst izpildes laikam 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="e279e-179">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Indeksa atrašana](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="e279e-181">Pēc Talent un Finance integrācijas Talent dati netiek rādīti risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-181">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="e279e-182">Ko darīt?</span><span class="sxs-lookup"><span data-stu-id="e279e-182">What do I do?</span></span>

<span data-ttu-id="e279e-183">Integrācija risinājumā Finance paredz divas darbības.</span><span class="sxs-lookup"><span data-stu-id="e279e-183">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="e279e-184">Vispirms pārliecinieties, vai Talent dati ir atjaunināti un ir pieejami pakalpojumā Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e279e-184">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="e279e-185">Šī sinhronizācija tiek veikta gandrīz reālā laikā, un to var pārbaudīt risinājumā PowerApps, skatot datus, kuri ir datu elementos.</span><span class="sxs-lookup"><span data-stu-id="e279e-185">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Dati pakalpojumā Common Data Service](media/DataInCDS.png)

<span data-ttu-id="e279e-187">Ja dati pakalpojumā Common Data Service netiek rādīti paredzētajā veidā, pārbaudiet, vai integrācijā šis elements tiek atbalstīts.</span><span class="sxs-lookup"><span data-stu-id="e279e-187">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="e279e-188">Lai iekļautu papildu datus pakalpojumā Common Data Service, būs nepieciešamas izmaiņas no Microsoft puses.</span><span class="sxs-lookup"><span data-stu-id="e279e-188">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="e279e-189">Ja elements tiek atbalstīts un šie dati ir pieejami pakalpojumā Common Data Service, pārbaudiet, vai datu integrētājā ir pareizs kartējums.</span><span class="sxs-lookup"><span data-stu-id="e279e-189">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="e279e-190">Ja integrētāja kartējums ir pareizs, pārbaudiet, vai ir veiksmīgi izpildīti datu pārvaldības darbi.</span><span class="sxs-lookup"><span data-stu-id="e279e-190">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="e279e-191">Pakešveida darbu izpildes laikā var rasties kļūdas.</span><span class="sxs-lookup"><span data-stu-id="e279e-191">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="e279e-192">Plašāku informāciju par to, kā izmantot rīku Datu pārvaldība, skatiet sadaļā [Datu pārvaldība](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e279e-192">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="e279e-193">Manu darbinieku adreses ir nepareizas pēc tam, kad tās ir importētas risinājumā Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-193">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="e279e-194">Ko darīt?</span><span class="sxs-lookup"><span data-stu-id="e279e-194">What should I do?</span></span>

<span data-ttu-id="e279e-195">Vienuma **Atrašanās vietas ID** numuru sērija izmanto vienu un to pašu modeli gan risinājumā Talent, gan Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-195">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="e279e-196">Numuru sērijai ir jābūt unikālai abās pusēs, lai nebūtu adrešu sadursmju, integrējot datus no Common Data Service uz Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e279e-196">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="e279e-197">Veicot Talent ieviešanu, pārbaudiet, vai numuru sērijas nav vienādas risinājumā Talent un Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-197">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="e279e-198">Pārbaudiet, vai visas numuru sērijas nav identiskas, ja dati tiek uzturēti abās sistēmās.</span><span class="sxs-lookup"><span data-stu-id="e279e-198">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="e279e-199">Izveidojot savienojumu kopu, savienojums netiek rādīts nolaižamajā sarakstā Savienojums.</span><span class="sxs-lookup"><span data-stu-id="e279e-199">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="e279e-200">Ko darīt?</span><span class="sxs-lookup"><span data-stu-id="e279e-200">What do I do?</span></span>

<span data-ttu-id="e279e-201">Pārliecinieties, ka, veidojot savienojumus, izvēlaties Dynamics 365 Finance un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e279e-201">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="e279e-202">Veicot nodarbinātību sinhronizāciju, tiek parādīti kļūdas ziņojumi “CompanyInfo_FK neeksistē” vai “Vērtība “31.12.2154. 23:59:59” laukā “Nodarbinātības beigu datums” nav atrasta saistītajā tabulā “Nodarbinātība”.” Ko darīt?</span><span class="sxs-lookup"><span data-stu-id="e279e-202">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="e279e-203">Pārliecinieties, ka veicat kartēšanu pareizajai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="e279e-203">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="e279e-204">Juridiskās personas sinhronizēšana neietilpst noklusējuma veidnē, tāpēc ir paredzēts, ka visas juridiskās personas, kas atrodas programmā Talent un Common Data Service, atrodas arī programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="e279e-204">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="e279e-205">Pārliecinieties, ka esat atlasījis pareizās juridiskās personas saistītajai savienojumu kopai.</span><span class="sxs-lookup"><span data-stu-id="e279e-205">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="e279e-206">Pēc mana projekta iestatīšanas lauku kartējums risinājumam Finance ir tukšs.</span><span class="sxs-lookup"><span data-stu-id="e279e-206">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="e279e-207">Ko darīt?</span><span class="sxs-lookup"><span data-stu-id="e279e-207">What should I do?</span></span>

<span data-ttu-id="e279e-208">Atsvaidziniet datu elementus risinājumā Finance, atverot sadaļu **Datu pārvaldība \> Struktūras parametri \> Elementu iestatījumi \> Atsvaidzināt elementu sarakstu.**</span><span class="sxs-lookup"><span data-stu-id="e279e-208">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="e279e-209">Šīs darbības pabeigšanai ir nepieciešamas dažas minūtes, un pēc tam būs redzami attiecīgie kartējumi.</span><span class="sxs-lookup"><span data-stu-id="e279e-209">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="e279e-210">Šī problēma rodas, veidojot jaunus projektus.</span><span class="sxs-lookup"><span data-stu-id="e279e-210">This issue occurs when new projects are created.</span></span>

![Trūkst lauku kartējuma](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="e279e-212">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e279e-212">Additional resources</span></span>

- <span data-ttu-id="e279e-213">Datu integrētājs (DI):</span><span class="sxs-lookup"><span data-stu-id="e279e-213">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="e279e-214">Datu integrēšana pakalpojumā Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e279e-214">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="e279e-215">Datu integrētāja kļūdu pārvaldība un problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="e279e-215">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="e279e-216">Atbildes sniegšana uz DSR pieprasījumiem sistēmas ģenerētiem žurnāliem platformā PowerApps, Microsoft Flow un Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e279e-216">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="e279e-217">Datu pārvaldība:</span><span class="sxs-lookup"><span data-stu-id="e279e-217">Data Management:</span></span>

  - [<span data-ttu-id="e279e-218">Datu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="e279e-218">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
