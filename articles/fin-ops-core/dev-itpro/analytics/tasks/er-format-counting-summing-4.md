---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (4. daļa. Formāta palaišana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu formātu, lai to skaitītu un summētu, pamatojoties uz jau ģenerētā teksta izvades datiem. (4. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5576229e8b81824dff6d0b38b8ab5483e04ade8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092951"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="c4493-104">ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (4. daļa. Formāta palaišana)</span><span class="sxs-lookup"><span data-stu-id="c4493-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4493-105">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="c4493-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="c4493-106">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="c4493-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="c4493-107">Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras “ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (3. daļa: Izmantot aprēķinus izvades sagatavošanai)” darbības.</span><span class="sxs-lookup"><span data-stu-id="c4493-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="c4493-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="c4493-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="c4493-109">Pārbaudīt šo konfigurāciju attiecībā uz Intrastat pārskatu izveidošanu</span><span class="sxs-lookup"><span data-stu-id="c4493-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="c4493-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="c4493-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c4493-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c4493-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c4493-112">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="c4493-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="c4493-113">Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="c4493-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="c4493-114">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="c4493-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="c4493-115">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c4493-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="c4493-116">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="c4493-116">Click User parameters.</span></span>
8. <span data-ttu-id="c4493-117">Laukā Palaist iestatījumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c4493-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="c4493-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c4493-118">Click OK.</span></span>
10. <span data-ttu-id="c4493-119">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="c4493-119">Click Edit.</span></span>
11. <span data-ttu-id="c4493-120">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c4493-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="c4493-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c4493-121">Click Save.</span></span>
13. <span data-ttu-id="c4493-122">Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="c4493-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="c4493-123">Izvērsiet sadaļu Elektroniskie pārskati.</span><span class="sxs-lookup"><span data-stu-id="c4493-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="c4493-124">Atlasiet konfigurāciju “Intrastat (DE) with counting & summing”.</span><span class="sxs-lookup"><span data-stu-id="c4493-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="c4493-125">Atlasiet konfigurāciju “Intrastat (DE) with counting & summing”.</span><span class="sxs-lookup"><span data-stu-id="c4493-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="c4493-126">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c4493-126">Click Save.</span></span>
18. <span data-ttu-id="c4493-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c4493-127">Close the page.</span></span>
19. <span data-ttu-id="c4493-128">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="c4493-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="c4493-129">Noklikšķiniet uz Izvade.</span><span class="sxs-lookup"><span data-stu-id="c4493-129">Click Output.</span></span>
21. <span data-ttu-id="c4493-130">Noklikšķiniet uz Atskaite.</span><span class="sxs-lookup"><span data-stu-id="c4493-130">Click Report.</span></span>
    * <span data-ttu-id="c4493-131">Izpildiet Intrastat pārskata ģenerēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="c4493-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="c4493-132">Laukā No datuma iestatiet datumu 2000-01-01.</span><span class="sxs-lookup"><span data-stu-id="c4493-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="c4493-133">Definējiet tāda pārskata perioda sākuma un beigu datumus, kas ietver esošos datumus transakciju veidlapā.</span><span class="sxs-lookup"><span data-stu-id="c4493-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="c4493-134">Laukā Līdz datumam iestatiet datumu uz 2022-12-31.</span><span class="sxs-lookup"><span data-stu-id="c4493-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="c4493-135">Definējiet tāda pārskata perioda sākuma un beigu datumus, kas ietver esošos datumus transakciju veidlapā.</span><span class="sxs-lookup"><span data-stu-id="c4493-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="c4493-136">Laukā Virziens atlasiet opciju 'Arrivals'.</span><span class="sxs-lookup"><span data-stu-id="c4493-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="c4493-137">Laukā Ģenerēt failu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c4493-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="c4493-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c4493-138">Click OK.</span></span>
    * <span data-ttu-id="c4493-139">Pārskatiet izveidoto izvades dokumentu ar kopsavilkuma rindām beigās.</span><span class="sxs-lookup"><span data-stu-id="c4493-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="c4493-140">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c4493-140">Click New.</span></span>
28. <span data-ttu-id="c4493-141">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="c4493-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="c4493-142">Laukā Virziens atlasiet opciju 'Dispatches'.</span><span class="sxs-lookup"><span data-stu-id="c4493-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="c4493-143">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4493-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="c4493-144">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c4493-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="c4493-145">Iestatiet svara vērtību 10.</span><span class="sxs-lookup"><span data-stu-id="c4493-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="c4493-146">Iestatiet vienuma Rēķina summa vērtību 10000.</span><span class="sxs-lookup"><span data-stu-id="c4493-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="c4493-147">Iestatiet vienuma Statistiskā summa vērtību 10000.</span><span class="sxs-lookup"><span data-stu-id="c4493-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="c4493-148">Noklikšķiniet uz Izvade.</span><span class="sxs-lookup"><span data-stu-id="c4493-148">Click Output.</span></span>
36. <span data-ttu-id="c4493-149">Noklikšķiniet uz Atskaite.</span><span class="sxs-lookup"><span data-stu-id="c4493-149">Click Report.</span></span>
37. <span data-ttu-id="c4493-150">Laukā Virziens atlasiet opciju 'Dispatches'.</span><span class="sxs-lookup"><span data-stu-id="c4493-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="c4493-151">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c4493-151">Click OK.</span></span>
    * <span data-ttu-id="c4493-152">Pārskatiet izveidoto izvades dokumentu ar kopsavilkuma rindām beigās.</span><span class="sxs-lookup"><span data-stu-id="c4493-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="c4493-153">Ņemiet vērā, ka tas ir izmainīts, salīdzinot ar pirmo izpildi.</span><span class="sxs-lookup"><span data-stu-id="c4493-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="c4493-154">Palaist šo konfigurāciju atkļūdošanas režīmā, lai pārskatītu apkopotos uzskaites & summēšanas datus</span><span class="sxs-lookup"><span data-stu-id="c4493-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="c4493-155">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c4493-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c4493-156">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="c4493-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="c4493-157">Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="c4493-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="c4493-158">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="c4493-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="c4493-159">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c4493-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="c4493-160">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="c4493-160">Click User parameters.</span></span>
7. <span data-ttu-id="c4493-161">Laukā Palaist atkļūdošanas režīmu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c4493-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="c4493-162">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c4493-162">Click OK.</span></span>
9. <span data-ttu-id="c4493-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c4493-163">Close the page.</span></span>
10. <span data-ttu-id="c4493-164">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="c4493-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="c4493-165">Noklikšķiniet uz Izvade.</span><span class="sxs-lookup"><span data-stu-id="c4493-165">Click Output.</span></span>
12. <span data-ttu-id="c4493-166">Noklikšķiniet uz Atskaite.</span><span class="sxs-lookup"><span data-stu-id="c4493-166">Click Report.</span></span>
13. <span data-ttu-id="c4493-167">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c4493-167">Click OK.</span></span>
14. <span data-ttu-id="c4493-168">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c4493-168">Close the page.</span></span>
15. <span data-ttu-id="c4493-169">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c4493-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="c4493-170">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="c4493-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="c4493-171">Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="c4493-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="c4493-172">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="c4493-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="c4493-173">Noklikšķiniet uz Atkļūdošanas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="c4493-173">Click Debug logs.</span></span>
    * <span data-ttu-id="c4493-174">Ņemiet vērā, ka atlasītās konfigurācijas izpildes procesam ir izveidots atkļūdošanas žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="c4493-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="c4493-175">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c4493-175">Click Attach.</span></span>
21. <span data-ttu-id="c4493-176">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="c4493-176">Click Open.</span></span>
    * <span data-ttu-id="c4493-177">Pārskatiet izveidoto XML failu, kas ietver uzskaites un summēšanas datus, kas tika apkopoti atlasītās konfigurācijas izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="c4493-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

