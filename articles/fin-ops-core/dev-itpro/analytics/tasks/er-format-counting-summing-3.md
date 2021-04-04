---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (3. daļa. Aprēķinu izmantošana izvades datu izveidei)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu formātu, lai to skaitītu un summētu, pamatojoties uz jau ģenerētā teksta izvades datiem. (3. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af95399118b9059b9bead3a1b84203cf3b6e74c2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567120"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="38512-104">ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (3. daļa. Aprēķinu izmantošana izvades datu izveidei)</span><span class="sxs-lookup"><span data-stu-id="38512-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38512-105">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="38512-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="38512-106">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="38512-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="38512-107">Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras "ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (2. daļa: Konfigurēt aprēķinus)" darbības.</span><span class="sxs-lookup"><span data-stu-id="38512-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="38512-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="38512-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="38512-109">Konfigurēt šo pārskatu, lai varētu izmantot uzskaites un summēšanas datus</span><span class="sxs-lookup"><span data-stu-id="38512-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="38512-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="38512-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="38512-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="38512-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="38512-112">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="38512-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="38512-113">Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="38512-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="38512-114">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="38512-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="38512-115">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="38512-115">Click Designer.</span></span>
7. <span data-ttu-id="38512-116">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="38512-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="38512-117">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="38512-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="38512-118">Pievienojiet jaunu datu avotu, lai iegūtu atmiņā saglabāto bloku sarakstu.</span><span class="sxs-lookup"><span data-stu-id="38512-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="38512-119">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="38512-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="38512-120">Laukā Nosaukums ierakstiet '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="38512-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="38512-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="38512-121">$BlocksList</span></span>  
11. <span data-ttu-id="38512-122">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="38512-122">Click Edit formula.</span></span>
12. <span data-ttu-id="38512-123">Koka struktūrā atlasiet 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="38512-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="38512-124">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="38512-124">Click Add function.</span></span>
14. <span data-ttu-id="38512-125">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="38512-125">Click Add data source.</span></span>
15. <span data-ttu-id="38512-126">Laukā Formula ievadiet 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="38512-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="38512-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="38512-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="38512-128">Laukā Formula ievadiet 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="38512-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="38512-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="38512-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="38512-130">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="38512-130">Click Save.</span></span>
    * <span data-ttu-id="38512-131">Simbols "\*" norāda, ka visi bloki tiks iekļauti šī ieraksta sarakstā.</span><span class="sxs-lookup"><span data-stu-id="38512-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="38512-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="38512-132">Close the page.</span></span>
19. <span data-ttu-id="38512-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="38512-133">Click OK.</span></span>
20. <span data-ttu-id="38512-134">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="38512-134">Click the Format tab.</span></span>
21. <span data-ttu-id="38512-135">Koka struktūrā atlasiet 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="38512-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="38512-136">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="38512-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="38512-137">Koka struktūrā atlasiet 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="38512-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="38512-138">Laukā Nosaukums ierakstiet 'Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="38512-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="38512-139">Kopsummas pēc blokiem</span><span class="sxs-lookup"><span data-stu-id="38512-139">Totals by blocks</span></span>  
25. <span data-ttu-id="38512-140">Laukā Īpašas rakstzīmes atlasiet 'New line - Windows (CR LF)'.</span><span class="sxs-lookup"><span data-stu-id="38512-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="38512-141">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="38512-141">Click OK.</span></span>
27. <span data-ttu-id="38512-142">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="38512-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="38512-143">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="38512-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="38512-144">Kokā atlasiet elementu “Teksts\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="38512-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="38512-145">Laukā Nosaukums ierakstiet 'Block code'.</span><span class="sxs-lookup"><span data-stu-id="38512-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="38512-146">Bloka kods</span><span class="sxs-lookup"><span data-stu-id="38512-146">Block code</span></span>  
31. <span data-ttu-id="38512-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="38512-147">Click OK.</span></span>
32. <span data-ttu-id="38512-148">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="38512-148">Click Add String.</span></span>
33. <span data-ttu-id="38512-149">Laukā Nosaukums ierakstiet 'Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="38512-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="38512-150">Uzskaites rindas</span><span class="sxs-lookup"><span data-stu-id="38512-150">Lines counting</span></span>  
34. <span data-ttu-id="38512-151">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="38512-151">Click OK.</span></span>
35. <span data-ttu-id="38512-152">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="38512-152">Click Add String.</span></span>
36. <span data-ttu-id="38512-153">Laukā Nosaukums ierakstiet 'Total amount'.</span><span class="sxs-lookup"><span data-stu-id="38512-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="38512-154">Kopējā summa</span><span class="sxs-lookup"><span data-stu-id="38512-154">Total amount</span></span>  
37. <span data-ttu-id="38512-155">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="38512-155">Click OK.</span></span>
38. <span data-ttu-id="38512-156">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="38512-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="38512-157">Koka struktūrā atlasiet '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="38512-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="38512-158">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="38512-158">Click Bind.</span></span>
    * <span data-ttu-id="38512-159">Izveidojiet kopsavilkuma rindu katram atmiņā saglabātajam blokam.</span><span class="sxs-lookup"><span data-stu-id="38512-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="38512-160">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="38512-160">Click the Format tab.</span></span>
42. <span data-ttu-id="38512-161">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="38512-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="38512-162">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="38512-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="38512-163">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="38512-163">Click Edit formula.</span></span>
45. <span data-ttu-id="38512-164">Laukā Formula ievadiet '"Block id: " & '.</span><span class="sxs-lookup"><span data-stu-id="38512-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="38512-165">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="38512-165">"Block id: " &</span></span>  
46. <span data-ttu-id="38512-166">Koka struktūrā izvērsiet sadaļu '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="38512-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="38512-167">Koka struktūrā atlasiet '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="38512-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="38512-168">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="38512-168">Click Add data source.</span></span>
49. <span data-ttu-id="38512-169">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="38512-169">Click Save.</span></span>
50. <span data-ttu-id="38512-170">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="38512-170">Close the page.</span></span>
51. <span data-ttu-id="38512-171">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="38512-171">Click the Format tab.</span></span>
52. <span data-ttu-id="38512-172">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="38512-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="38512-173">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="38512-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="38512-174">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="38512-174">Click Edit formula.</span></span>
    * <span data-ttu-id="38512-175">Izveidojiet rindu skaita izvadi katram pārskatā esošajam blokam.</span><span class="sxs-lookup"><span data-stu-id="38512-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="38512-176">Laukā Formula ievadiet '"Number of lines in this block: " & '.</span><span class="sxs-lookup"><span data-stu-id="38512-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="38512-177">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="38512-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="38512-178">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="38512-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="38512-179">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="38512-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="38512-180">Koka struktūrā atlasiet 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="38512-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="38512-181">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="38512-181">Click Add function.</span></span>
59. <span data-ttu-id="38512-182">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="38512-182">Click Add data source.</span></span>
60. <span data-ttu-id="38512-183">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="38512-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="38512-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="38512-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="38512-185">Koka struktūrā izvērsiet sadaļu '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="38512-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="38512-186">Koka struktūrā atlasiet '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="38512-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="38512-187">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="38512-187">Click Add data source.</span></span>
64. <span data-ttu-id="38512-188">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="38512-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="38512-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="38512-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="38512-190">Koka struktūrā atlasiet '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="38512-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="38512-191">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="38512-191">Click Add data source.</span></span>
67. <span data-ttu-id="38512-192">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="38512-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="38512-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="38512-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="38512-194">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="38512-194">Click Save.</span></span>
69. <span data-ttu-id="38512-195">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="38512-195">Close the page.</span></span>
70. <span data-ttu-id="38512-196">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="38512-196">Click the Format tab.</span></span>
71. <span data-ttu-id="38512-197">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="38512-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="38512-198">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="38512-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="38512-199">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="38512-199">Click Edit formula.</span></span>
    * <span data-ttu-id="38512-200">Izveidojiet izvadi, kas būs visu šajā pārskatā esošo bloku rēķinā iekļauto summu kopsumma.</span><span class="sxs-lookup"><span data-stu-id="38512-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="38512-201">Laukā Formula ievadiet '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="38512-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="38512-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="38512-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="38512-203">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="38512-203">Click Save.</span></span>
76. <span data-ttu-id="38512-204">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="38512-204">Close the page.</span></span>
77. <span data-ttu-id="38512-205">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="38512-205">Click Save.</span></span>
78. <span data-ttu-id="38512-206">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="38512-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]