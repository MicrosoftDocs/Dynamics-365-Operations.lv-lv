---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (3. daļa. Aprēķinu izmantošana izvades datu izveidei)
description: Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544614"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="f8949-103">ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (3. daļa: Aprēķināšanu izmantošana, lai izveidotu izvades datus)</span><span class="sxs-lookup"><span data-stu-id="f8949-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8949-104">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="f8949-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="f8949-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="f8949-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f8949-106">Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras “ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (2. daļa: Konfigurēt aprēķinus)” darbības.</span><span class="sxs-lookup"><span data-stu-id="f8949-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="f8949-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="f8949-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="f8949-108">Konfigurēt šo pārskatu, lai varētu izmantot uzskaites un summēšanas datus</span><span class="sxs-lookup"><span data-stu-id="f8949-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="f8949-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="f8949-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f8949-110">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="f8949-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f8949-111">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="f8949-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="f8949-112">Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="f8949-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="f8949-113">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="f8949-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="f8949-114">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="f8949-114">Click Designer.</span></span>
7. <span data-ttu-id="f8949-115">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="f8949-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="f8949-116">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="f8949-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="f8949-117">Pievienojiet jaunu datu avotu, lai iegūtu atmiņā saglabāto bloku sarakstu.</span><span class="sxs-lookup"><span data-stu-id="f8949-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="f8949-118">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="f8949-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="f8949-119">Laukā Nosaukums ierakstiet '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="f8949-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="f8949-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="f8949-120">$BlocksList</span></span>  
11. <span data-ttu-id="f8949-121">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="f8949-121">Click Edit formula.</span></span>
12. <span data-ttu-id="f8949-122">Koka struktūrā atlasiet 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="f8949-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="f8949-123">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="f8949-123">Click Add function.</span></span>
14. <span data-ttu-id="f8949-124">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="f8949-124">Click Add data source.</span></span>
15. <span data-ttu-id="f8949-125">Laukā Formula ievadiet 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="f8949-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="f8949-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="f8949-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="f8949-127">Laukā Formula ievadiet 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="f8949-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="f8949-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="f8949-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="f8949-129">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f8949-129">Click Save.</span></span>
    * <span data-ttu-id="f8949-130">Simbols “\*” norāda, ka visi bloki tiks iekļauti šī ieraksta sarakstā.</span><span class="sxs-lookup"><span data-stu-id="f8949-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="f8949-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f8949-131">Close the page.</span></span>
19. <span data-ttu-id="f8949-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f8949-132">Click OK.</span></span>
20. <span data-ttu-id="f8949-133">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="f8949-133">Click the Format tab.</span></span>
21. <span data-ttu-id="f8949-134">Koka struktūrā atlasiet 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="f8949-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="f8949-135">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="f8949-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="f8949-136">Koka struktūrā atlasiet 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="f8949-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="f8949-137">Laukā Nosaukums ierakstiet 'Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="f8949-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="f8949-138">Kopsummas pēc blokiem</span><span class="sxs-lookup"><span data-stu-id="f8949-138">Totals by blocks</span></span>  
25. <span data-ttu-id="f8949-139">Laukā Īpašas rakstzīmes atlasiet 'New line - Windows (CR LF)'.</span><span class="sxs-lookup"><span data-stu-id="f8949-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="f8949-140">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="f8949-140">Click OK.</span></span>
27. <span data-ttu-id="f8949-141">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="f8949-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="f8949-142">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="f8949-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="f8949-143">Kokā atlasiet elementu “Teksts\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="f8949-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="f8949-144">Laukā Nosaukums ierakstiet 'Block code'.</span><span class="sxs-lookup"><span data-stu-id="f8949-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="f8949-145">Bloka kods</span><span class="sxs-lookup"><span data-stu-id="f8949-145">Block code</span></span>  
31. <span data-ttu-id="f8949-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f8949-146">Click OK.</span></span>
32. <span data-ttu-id="f8949-147">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="f8949-147">Click Add String.</span></span>
33. <span data-ttu-id="f8949-148">Laukā Nosaukums ierakstiet 'Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="f8949-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="f8949-149">Uzskaites rindas</span><span class="sxs-lookup"><span data-stu-id="f8949-149">Lines counting</span></span>  
34. <span data-ttu-id="f8949-150">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f8949-150">Click OK.</span></span>
35. <span data-ttu-id="f8949-151">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="f8949-151">Click Add String.</span></span>
36. <span data-ttu-id="f8949-152">Laukā Nosaukums ierakstiet 'Total amount'.</span><span class="sxs-lookup"><span data-stu-id="f8949-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="f8949-153">Kopējā summa</span><span class="sxs-lookup"><span data-stu-id="f8949-153">Total amount</span></span>  
37. <span data-ttu-id="f8949-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f8949-154">Click OK.</span></span>
38. <span data-ttu-id="f8949-155">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="f8949-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="f8949-156">Koka struktūrā atlasiet '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="f8949-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="f8949-157">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="f8949-157">Click Bind.</span></span>
    * <span data-ttu-id="f8949-158">Izveidojiet kopsavilkuma rindu katram atmiņā saglabātajam blokam.</span><span class="sxs-lookup"><span data-stu-id="f8949-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="f8949-159">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="f8949-159">Click the Format tab.</span></span>
42. <span data-ttu-id="f8949-160">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="f8949-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="f8949-161">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="f8949-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="f8949-162">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="f8949-162">Click Edit formula.</span></span>
45. <span data-ttu-id="f8949-163">Laukā Formula ievadiet '"Block id: " & '.</span><span class="sxs-lookup"><span data-stu-id="f8949-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="f8949-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="f8949-164">"Block id: " &</span></span>  
46. <span data-ttu-id="f8949-165">Koka struktūrā izvērsiet sadaļu '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="f8949-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="f8949-166">Koka struktūrā atlasiet '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="f8949-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="f8949-167">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="f8949-167">Click Add data source.</span></span>
49. <span data-ttu-id="f8949-168">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f8949-168">Click Save.</span></span>
50. <span data-ttu-id="f8949-169">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f8949-169">Close the page.</span></span>
51. <span data-ttu-id="f8949-170">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="f8949-170">Click the Format tab.</span></span>
52. <span data-ttu-id="f8949-171">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="f8949-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="f8949-172">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="f8949-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="f8949-173">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="f8949-173">Click Edit formula.</span></span>
    * <span data-ttu-id="f8949-174">Izveidojiet rindu skaita izvadi katram pārskatā esošajam blokam.</span><span class="sxs-lookup"><span data-stu-id="f8949-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="f8949-175">Laukā Formula ievadiet '"Number of lines in this block: " & '.</span><span class="sxs-lookup"><span data-stu-id="f8949-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="f8949-176">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="f8949-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="f8949-177">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="f8949-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="f8949-178">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="f8949-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="f8949-179">Koka struktūrā atlasiet 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="f8949-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="f8949-180">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="f8949-180">Click Add function.</span></span>
59. <span data-ttu-id="f8949-181">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="f8949-181">Click Add data source.</span></span>
60. <span data-ttu-id="f8949-182">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="f8949-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="f8949-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="f8949-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="f8949-184">Koka struktūrā izvērsiet sadaļu '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="f8949-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="f8949-185">Koka struktūrā atlasiet '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="f8949-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="f8949-186">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="f8949-186">Click Add data source.</span></span>
64. <span data-ttu-id="f8949-187">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="f8949-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="f8949-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="f8949-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="f8949-189">Koka struktūrā atlasiet '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="f8949-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="f8949-190">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="f8949-190">Click Add data source.</span></span>
67. <span data-ttu-id="f8949-191">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="f8949-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="f8949-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="f8949-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="f8949-193">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f8949-193">Click Save.</span></span>
69. <span data-ttu-id="f8949-194">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f8949-194">Close the page.</span></span>
70. <span data-ttu-id="f8949-195">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="f8949-195">Click the Format tab.</span></span>
71. <span data-ttu-id="f8949-196">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="f8949-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="f8949-197">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="f8949-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="f8949-198">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="f8949-198">Click Edit formula.</span></span>
    * <span data-ttu-id="f8949-199">Izveidojiet izvadi, kas būs visu šajā pārskatā esošo bloku rēķinā iekļauto summu kopsumma.</span><span class="sxs-lookup"><span data-stu-id="f8949-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="f8949-200">Laukā Formula ievadiet '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="f8949-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="f8949-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="f8949-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="f8949-202">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f8949-202">Click Save.</span></span>
76. <span data-ttu-id="f8949-203">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f8949-203">Close the page.</span></span>
77. <span data-ttu-id="f8949-204">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f8949-204">Click Save.</span></span>
78. <span data-ttu-id="f8949-205">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f8949-205">Close the page.</span></span>

