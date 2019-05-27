---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (2. daļa. Aprēķinu konfigurēšana)
description: Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ef657b13bc1f7f4a84676821e4175ace32c069a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551303"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2-configure-computations"></a><span data-ttu-id="dbd96-103">ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (2. daļa: Konfigurēt aprēķināšanas)</span><span class="sxs-lookup"><span data-stu-id="dbd96-103">ER Configure format to do counting and summing (Part 2: Configure computations)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dbd96-104">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="dbd96-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="dbd96-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="dbd96-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="dbd96-106">Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras “ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (1. daļa: Izveidot formātu)” darbības.</span><span class="sxs-lookup"><span data-stu-id="dbd96-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="dbd96-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="dbd96-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="dbd96-108">Izveidot formāta konfigurāciju, lai pievienotu uzskaites un summēšanas detalizētus datus</span><span class="sxs-lookup"><span data-stu-id="dbd96-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="dbd96-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="dbd96-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="dbd96-110">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="dbd96-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="dbd96-111">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="dbd96-112">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="dbd96-113">Pieņemsim, ka jums ir jāpielāgo korporācijas Microsoft nodrošinātais formāts, pievienojot rindas ar kopsavilkuma datiem Intrastat pārskata beigās.</span><span class="sxs-lookup"><span data-stu-id="dbd96-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="dbd96-114">Lai to izdarītu un varētu veikt izmaiņas, no Microsoft instances ir jāiegūst sava Intrastat konfigurācijas instance.</span><span class="sxs-lookup"><span data-stu-id="dbd96-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="dbd96-115">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="dbd96-116">Laukā Jauns ievadiet 'Derive from Name: Intrastat (DE), Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="dbd96-117">Laukā Nosaukums ierakstiet 'Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="dbd96-118">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="dbd96-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="dbd96-119">Konfigurēt šo pārskatu, lai veiktu uzskaiti un summēšana, izmantojot izejas datus</span><span class="sxs-lookup"><span data-stu-id="dbd96-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="dbd96-120">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="dbd96-120">Click Designer.</span></span>
2. <span data-ttu-id="dbd96-121">Laukā Apkopot izvades datus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="dbd96-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="dbd96-122">Šis karodziņš aktivizē izpildes laikā izvades datu apkopošanas procesu, kas paredzēts Intrastat failu izveidei.</span><span class="sxs-lookup"><span data-stu-id="dbd96-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="dbd96-123">Tas ir jāatkārto dažādiem Intrastat virzieniem, tāpēc pievienojiet īpašo modeļa uzskaitījumu šīs formāta konfigurācijas datu avotu sarakstam.</span><span class="sxs-lookup"><span data-stu-id="dbd96-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="dbd96-124">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="dbd96-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="dbd96-125">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="dbd96-126">Koka struktūrā atlasiet 'Data model\Enumeration '.</span><span class="sxs-lookup"><span data-stu-id="dbd96-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="dbd96-127">Laukā Nosaukums ierakstiet 'Direction'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="dbd96-128">Ievadiet vai atlasiet vērtību laukā Modeļa uzskaitījums.</span><span class="sxs-lookup"><span data-stu-id="dbd96-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="dbd96-129">Atlasiet vērtību Virziens.</span><span class="sxs-lookup"><span data-stu-id="dbd96-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="dbd96-130">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbd96-130">Click OK.</span></span>
9. <span data-ttu-id="dbd96-131">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="dbd96-132">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="dbd96-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="dbd96-133">Laukā Nosaukums ierakstiet '$BlockName'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="dbd96-134">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-134">Click Edit formula.</span></span>
13. <span data-ttu-id="dbd96-135">Laukā Formula ievadiet '"block"'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="dbd96-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-136">Click Save.</span></span>
15. <span data-ttu-id="dbd96-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-137">Close the page.</span></span>
16. <span data-ttu-id="dbd96-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbd96-138">Click OK.</span></span>
17. <span data-ttu-id="dbd96-139">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="dbd96-140">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="dbd96-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="dbd96-141">Laukā Nosaukums ierakstiet '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="dbd96-142">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-142">Click Edit formula.</span></span>
21. <span data-ttu-id="dbd96-143">Laukā Formula ievadiet "record"'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="dbd96-144">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-144">Click Save.</span></span>
23. <span data-ttu-id="dbd96-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-145">Close the page.</span></span>
24. <span data-ttu-id="dbd96-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbd96-146">Click OK.</span></span>
25. <span data-ttu-id="dbd96-147">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="dbd96-148">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="dbd96-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="dbd96-149">Laukā Nosaukums ierakstiet '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="dbd96-150">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-150">Click Edit formula.</span></span>
29. <span data-ttu-id="dbd96-151">Laukā Formula ievadiet '"InvoicedAmountEUR"'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="dbd96-152">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-152">Click Save.</span></span>
31. <span data-ttu-id="dbd96-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-153">Close the page.</span></span>
32. <span data-ttu-id="dbd96-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbd96-154">Click OK.</span></span>
33. <span data-ttu-id="dbd96-155">Koka struktūrā atlasiet 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="dbd96-156">Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt</span><span class="sxs-lookup"><span data-stu-id="dbd96-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="dbd96-157">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-157">Click Add data source.</span></span>
    * <span data-ttu-id="dbd96-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="dbd96-158">$BlockName</span></span>  
36. <span data-ttu-id="dbd96-159">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-159">Click Save.</span></span>
37. <span data-ttu-id="dbd96-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-160">Close the page.</span></span>
38. <span data-ttu-id="dbd96-161">Noklikšķiniet uz lauka Apkopoto datu atslēgas vērtība pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="dbd96-162">Laukā Formula ievadiet “IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")”.</span><span class="sxs-lookup"><span data-stu-id="dbd96-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="dbd96-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="dbd96-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="dbd96-164">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-164">Click Save.</span></span>
41. <span data-ttu-id="dbd96-165">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-165">Close the page.</span></span>
    * <span data-ttu-id="dbd96-166">Saskaitiet šīs secības līnijas.</span><span class="sxs-lookup"><span data-stu-id="dbd96-166">Count the lines of this sequence.</span></span> <span data-ttu-id="dbd96-167">Rezultāti tiks izmantoti ar nosaukumu “bloķēt” atsevišķi dažādiem virzieniem.</span><span class="sxs-lookup"><span data-stu-id="dbd96-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="dbd96-168">Vērtība “Importēt” tiks izmantota visām ienākošajām Intrastat transakcijām.</span><span class="sxs-lookup"><span data-stu-id="dbd96-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="dbd96-169">Vērtība “Eksportēt” tiks izmantota visām Intrastat nosūtītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="dbd96-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="dbd96-170">Uzskatiet to par virtuālu Excel izklājlapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="dbd96-171">Katra transakcijas rindas, kur pirmā kolonna ir “bloķēt”, tiek aizpildīta ar attiecīgi ar vērtību “Importēt” un “Eksportēt”.</span><span class="sxs-lookup"><span data-stu-id="dbd96-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="dbd96-172">Kokā struktūrā izvērsiet Intrastat\Data: Sequence'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="dbd96-173">Koka struktūrā atlasiet 'Intrastat\Data: Sequence\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="dbd96-174">Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="dbd96-175">Saskaitiet šīs secības līnijas.</span><span class="sxs-lookup"><span data-stu-id="dbd96-175">Count the lines of this sequence.</span></span> <span data-ttu-id="dbd96-176">Rezultāti tiks saglabāti atmiņā ar vārdu “ierakstīt”.</span><span class="sxs-lookup"><span data-stu-id="dbd96-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="dbd96-177">Koka struktūrā atlasiet '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="dbd96-178">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-178">Click Add data source.</span></span>
47. <span data-ttu-id="dbd96-179">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-179">Click Save.</span></span>
48. <span data-ttu-id="dbd96-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-180">Close the page.</span></span>
49. <span data-ttu-id="dbd96-181">Noklikšķiniet uz lauka Apkopoto datu atslēgas vērtība pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="dbd96-182">Laukā Formula ievadiet “Intrastat.CommodityRecord.CommodityCode”.</span><span class="sxs-lookup"><span data-stu-id="dbd96-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="dbd96-183">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-183">Click Save.</span></span>
52. <span data-ttu-id="dbd96-184">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-184">Close the page.</span></span>
    * <span data-ttu-id="dbd96-185">Saskaitiet šīs secības līnijas.</span><span class="sxs-lookup"><span data-stu-id="dbd96-185">Count the lines of this sequence.</span></span> <span data-ttu-id="dbd96-186">Rezultāti tiks izmantoti ar nosaukumu “ierakstīt” atsevišķi dažādiem preces kodiem.</span><span class="sxs-lookup"><span data-stu-id="dbd96-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="dbd96-187">Uzskatiet to par virtuālu Excel izklājlapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="dbd96-188">Katra transakcijas rinda, kur pirmā kolonna ir “bloķēt”, tiek aizpildīta ar attiecīgi ar vērtību “Importēt” un “Eksportēt” un otrais bloks “ierakstīt” tiek aizpildīts ar preces koda vērtību.</span><span class="sxs-lookup"><span data-stu-id="dbd96-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="dbd96-189">Koka struktūrā atlasiet 'Intrastat\Data: Sequence\Dispatches?'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="dbd96-190">Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt</span><span class="sxs-lookup"><span data-stu-id="dbd96-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="dbd96-191">Koka struktūrā atlasiet '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="dbd96-192">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-192">Click Add data source.</span></span>
57. <span data-ttu-id="dbd96-193">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-193">Click Save.</span></span>
58. <span data-ttu-id="dbd96-194">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-194">Close the page.</span></span>
59. <span data-ttu-id="dbd96-195">Noklikšķiniet uz lauka Apkopoto datu atslēgas vērtība pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="dbd96-196">Laukā Formula ievadiet “Intrastat.CommodityRecord.CommodityCode”.</span><span class="sxs-lookup"><span data-stu-id="dbd96-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="dbd96-197">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-197">Click Save.</span></span>
62. <span data-ttu-id="dbd96-198">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-198">Close the page.</span></span>
63. <span data-ttu-id="dbd96-199">Kokā struktūrā izvērsiet 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="dbd96-200">Kokā struktūrā izvērsiet 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="dbd96-201">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="dbd96-201">Click the Format tab.</span></span>
66. <span data-ttu-id="dbd96-202">Koka struktūrā atlasiet 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="dbd96-203">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="dbd96-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="dbd96-204">Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="dbd96-205">Koka struktūrā atlasiet '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="dbd96-206">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-206">Click Add data source.</span></span>
71. <span data-ttu-id="dbd96-207">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-207">Click Save.</span></span>
72. <span data-ttu-id="dbd96-208">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-208">Close the page.</span></span>
    * <span data-ttu-id="dbd96-209">Aprēķiniet šīs secības rindas rēķinā iekļauto summu vērtību.</span><span class="sxs-lookup"><span data-stu-id="dbd96-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="dbd96-210">Rezultāti tiks izmantoti ar nosaukumu “InvoicedAmountEUR” atsevišķi dažādiem Intrastat virzieniem un preces kodiem.</span><span class="sxs-lookup"><span data-stu-id="dbd96-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="dbd96-211">Uzskatiet to par virtuālu Excel izklājlapas izveidi.</span><span class="sxs-lookup"><span data-stu-id="dbd96-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="dbd96-212">Katra transakcijas rindas, kur pirmā kolonna ir “bloķēt”, tiek aizpildīta ar attiecīgi ar vērtību “Importēt” un “Eksportēt”.</span><span class="sxs-lookup"><span data-stu-id="dbd96-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="dbd96-213">Otrs bloks “ierakstīt” tiek aizpildīts ar preces koda vērtību un trešā kolonna “InvoicedAmountEUR” tiek aizpildīta ar rēķina summas vērtību.</span><span class="sxs-lookup"><span data-stu-id="dbd96-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="dbd96-214">Kokā struktūrā izvērsiet 'Intrastat\Data\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="dbd96-215">Koka struktūrā izvērsiet 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="dbd96-216">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="dbd96-216">Click the Format tab.</span></span>
76. <span data-ttu-id="dbd96-217">Koka struktūrā atlasiet 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="dbd96-218">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="dbd96-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="dbd96-219">Noklikšķiniet uz lauka Apkopoto datu atslēgas nosaukums pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="dbd96-220">Koka struktūrā atlasiet '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="dbd96-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="dbd96-221">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-221">Click Add data source.</span></span>
81. <span data-ttu-id="dbd96-222">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-222">Click Save.</span></span>
82. <span data-ttu-id="dbd96-223">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-223">Close the page.</span></span>
83. <span data-ttu-id="dbd96-224">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbd96-224">Click Save.</span></span>
84. <span data-ttu-id="dbd96-225">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbd96-225">Close the page.</span></span>

