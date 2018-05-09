--- 
title: "Formāta darbināšana, lai veiktu inventarizāciju un summēšanu"
description: "Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 689514f0614aeb4a8bfad39459267005d0aaf6ef
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="run-the-format-to-do-counting-and-summing"></a><span data-ttu-id="57d48-103">Formāta darbināšana, lai veiktu inventarizāciju un summēšanu</span><span class="sxs-lookup"><span data-stu-id="57d48-103">Run the format to do counting and summing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57d48-104">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="57d48-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="57d48-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="57d48-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="57d48-106">Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras “ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (3. daļa: Izmantot aprēķinus izvades sagatavošanai)” darbības.</span><span class="sxs-lookup"><span data-stu-id="57d48-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="57d48-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="57d48-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="57d48-108">Pārbaudīt šo konfigurāciju attiecībā uz Intrastat pārskatu izveidošanu</span><span class="sxs-lookup"><span data-stu-id="57d48-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="57d48-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="57d48-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="57d48-110">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="57d48-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="57d48-111">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="57d48-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="57d48-112">Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="57d48-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="57d48-113">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="57d48-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="57d48-114">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="57d48-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="57d48-115">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="57d48-115">Click User parameters.</span></span>
8. <span data-ttu-id="57d48-116">Laukā Palaist iestatījumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="57d48-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="57d48-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="57d48-117">Click OK.</span></span>
10. <span data-ttu-id="57d48-118">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="57d48-118">Click Edit.</span></span>
11. <span data-ttu-id="57d48-119">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="57d48-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="57d48-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="57d48-120">Click Save.</span></span>
13. <span data-ttu-id="57d48-121">Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="57d48-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="57d48-122">Izvērsiet sadaļu Elektroniskie pārskati.</span><span class="sxs-lookup"><span data-stu-id="57d48-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="57d48-123">Atlasiet konfigurāciju “Intrastat (DE) with counting & summing”.</span><span class="sxs-lookup"><span data-stu-id="57d48-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="57d48-124">Atlasiet konfigurāciju “Intrastat (DE) with counting & summing”.</span><span class="sxs-lookup"><span data-stu-id="57d48-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="57d48-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="57d48-125">Click Save.</span></span>
18. <span data-ttu-id="57d48-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="57d48-126">Close the page.</span></span>
19. <span data-ttu-id="57d48-127">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="57d48-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="57d48-128">Noklikšķiniet uz Izvade.</span><span class="sxs-lookup"><span data-stu-id="57d48-128">Click Output.</span></span>
21. <span data-ttu-id="57d48-129">Noklikšķiniet uz Atskaite.</span><span class="sxs-lookup"><span data-stu-id="57d48-129">Click Report.</span></span>
    * <span data-ttu-id="57d48-130">Izpildiet Intrastat pārskata ģenerēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="57d48-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="57d48-131">Laukā No datuma iestatiet datumu 2000-01-01.</span><span class="sxs-lookup"><span data-stu-id="57d48-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="57d48-132">Definējiet tāda pārskata perioda sākuma un beigu datumus, kas ietver esošos datumus transakciju veidlapā.</span><span class="sxs-lookup"><span data-stu-id="57d48-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="57d48-133">Laukā Līdz datumam iestatiet datumu uz 2022-12-31.</span><span class="sxs-lookup"><span data-stu-id="57d48-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="57d48-134">Definējiet tāda pārskata perioda sākuma un beigu datumus, kas ietver esošos datumus transakciju veidlapā.</span><span class="sxs-lookup"><span data-stu-id="57d48-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="57d48-135">Laukā Virziens atlasiet opciju 'Arrivals'.</span><span class="sxs-lookup"><span data-stu-id="57d48-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="57d48-136">Laukā Ģenerēt failu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="57d48-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="57d48-137">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="57d48-137">Click OK.</span></span>
    * <span data-ttu-id="57d48-138">Pārskatiet izveidoto izvades dokumentu ar kopsavilkuma rindām beigās.</span><span class="sxs-lookup"><span data-stu-id="57d48-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="57d48-139">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="57d48-139">Click New.</span></span>
28. <span data-ttu-id="57d48-140">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="57d48-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="57d48-141">Laukā Virziens atlasiet opciju 'Dispatches'.</span><span class="sxs-lookup"><span data-stu-id="57d48-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="57d48-142">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="57d48-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="57d48-143">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="57d48-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="57d48-144">Iestatiet svara vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="57d48-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="57d48-145">Iestatiet vienuma Rēķina summa vērtību 10000.</span><span class="sxs-lookup"><span data-stu-id="57d48-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="57d48-146">Iestatiet vienuma Statistiskā summa vērtību 10000.</span><span class="sxs-lookup"><span data-stu-id="57d48-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="57d48-147">Noklikšķiniet uz Izvade.</span><span class="sxs-lookup"><span data-stu-id="57d48-147">Click Output.</span></span>
36. <span data-ttu-id="57d48-148">Noklikšķiniet uz Atskaite.</span><span class="sxs-lookup"><span data-stu-id="57d48-148">Click Report.</span></span>
37. <span data-ttu-id="57d48-149">Laukā Virziens atlasiet opciju 'Dispatches'.</span><span class="sxs-lookup"><span data-stu-id="57d48-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="57d48-150">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="57d48-150">Click OK.</span></span>
    * <span data-ttu-id="57d48-151">Pārskatiet izveidoto izvades dokumentu ar kopsavilkuma rindām beigās.</span><span class="sxs-lookup"><span data-stu-id="57d48-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="57d48-152">Ņemiet vērā, ka tas ir izmainīts, salīdzinot ar pirmo izpildi.</span><span class="sxs-lookup"><span data-stu-id="57d48-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="57d48-153">Palaist šo konfigurāciju atkļūdošanas režīmā, lai pārskatītu apkopotos uzskaites & summēšanas datus</span><span class="sxs-lookup"><span data-stu-id="57d48-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="57d48-154">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="57d48-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="57d48-155">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="57d48-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="57d48-156">Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="57d48-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="57d48-157">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="57d48-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="57d48-158">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="57d48-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="57d48-159">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="57d48-159">Click User parameters.</span></span>
7. <span data-ttu-id="57d48-160">Laukā Palaist atkļūdošanas režīmu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="57d48-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="57d48-161">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="57d48-161">Click OK.</span></span>
9. <span data-ttu-id="57d48-162">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="57d48-162">Close the page.</span></span>
10. <span data-ttu-id="57d48-163">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="57d48-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="57d48-164">Noklikšķiniet uz Izvade.</span><span class="sxs-lookup"><span data-stu-id="57d48-164">Click Output.</span></span>
12. <span data-ttu-id="57d48-165">Noklikšķiniet uz Atskaite.</span><span class="sxs-lookup"><span data-stu-id="57d48-165">Click Report.</span></span>
13. <span data-ttu-id="57d48-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="57d48-166">Click OK.</span></span>
14. <span data-ttu-id="57d48-167">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="57d48-167">Close the page.</span></span>
15. <span data-ttu-id="57d48-168">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="57d48-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="57d48-169">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="57d48-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="57d48-170">Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="57d48-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="57d48-171">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="57d48-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="57d48-172">Noklikšķiniet uz Atkļūdošanas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="57d48-172">Click Debug logs.</span></span>
    * <span data-ttu-id="57d48-173">Ņemiet vērā, ka atlasītās konfigurācijas izpildes procesam ir izveidots atkļūdošanas žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="57d48-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="57d48-174">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="57d48-174">Click Attach.</span></span>
21. <span data-ttu-id="57d48-175">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="57d48-175">Click Open.</span></span>
    * <span data-ttu-id="57d48-176">Pārskatiet izveidoto XML failu, kas ietver uzskaites un summēšanas datus, kas tika apkopoti atlasītās konfigurācijas izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="57d48-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


