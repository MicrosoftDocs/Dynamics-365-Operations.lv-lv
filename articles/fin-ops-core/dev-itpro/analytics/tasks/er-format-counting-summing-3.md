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
ms.openlocfilehash: e8a4965c07c5a084b21da40667747db36530284c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141957"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="850d6-103">ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (3. daļa. Aprēķinu izmantošana izvades datu izveidei)</span><span class="sxs-lookup"><span data-stu-id="850d6-103">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="850d6-104">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="850d6-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="850d6-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="850d6-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="850d6-106">Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras "ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (2. daļa: Konfigurēt aprēķinus)" darbības.</span><span class="sxs-lookup"><span data-stu-id="850d6-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="850d6-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="850d6-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="850d6-108">Konfigurēt šo pārskatu, lai varētu izmantot uzskaites un summēšanas datus</span><span class="sxs-lookup"><span data-stu-id="850d6-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="850d6-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="850d6-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="850d6-110">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="850d6-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="850d6-111">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="850d6-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="850d6-112">Koka struktūrā izvērsiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="850d6-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="850d6-113">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="850d6-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="850d6-114">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="850d6-114">Click Designer.</span></span>
7. <span data-ttu-id="850d6-115">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="850d6-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="850d6-116">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="850d6-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="850d6-117">Pievienojiet jaunu datu avotu, lai iegūtu atmiņā saglabāto bloku sarakstu.</span><span class="sxs-lookup"><span data-stu-id="850d6-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="850d6-118">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="850d6-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="850d6-119">Laukā Nosaukums ierakstiet '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="850d6-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="850d6-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="850d6-120">$BlocksList</span></span>  
11. <span data-ttu-id="850d6-121">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="850d6-121">Click Edit formula.</span></span>
12. <span data-ttu-id="850d6-122">Koka struktūrā atlasiet 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="850d6-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="850d6-123">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="850d6-123">Click Add function.</span></span>
14. <span data-ttu-id="850d6-124">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="850d6-124">Click Add data source.</span></span>
15. <span data-ttu-id="850d6-125">Laukā Formula ievadiet 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="850d6-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="850d6-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="850d6-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="850d6-127">Laukā Formula ievadiet 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="850d6-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="850d6-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="850d6-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="850d6-129">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="850d6-129">Click Save.</span></span>
    * <span data-ttu-id="850d6-130">Simbols "\*" norāda, ka visi bloki tiks iekļauti šī ieraksta sarakstā.</span><span class="sxs-lookup"><span data-stu-id="850d6-130">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="850d6-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="850d6-131">Close the page.</span></span>
19. <span data-ttu-id="850d6-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="850d6-132">Click OK.</span></span>
20. <span data-ttu-id="850d6-133">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="850d6-133">Click the Format tab.</span></span>
21. <span data-ttu-id="850d6-134">Koka struktūrā atlasiet 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="850d6-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="850d6-135">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="850d6-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="850d6-136">Koka struktūrā atlasiet 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="850d6-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="850d6-137">Laukā Nosaukums ierakstiet 'Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="850d6-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="850d6-138">Kopsummas pēc blokiem</span><span class="sxs-lookup"><span data-stu-id="850d6-138">Totals by blocks</span></span>  
25. <span data-ttu-id="850d6-139">Laukā Īpašas rakstzīmes atlasiet 'New line - Windows (CR LF)'.</span><span class="sxs-lookup"><span data-stu-id="850d6-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="850d6-140">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="850d6-140">Click OK.</span></span>
27. <span data-ttu-id="850d6-141">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="850d6-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="850d6-142">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="850d6-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="850d6-143">Kokā atlasiet elementu “Teksts\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="850d6-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="850d6-144">Laukā Nosaukums ierakstiet 'Block code'.</span><span class="sxs-lookup"><span data-stu-id="850d6-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="850d6-145">Bloka kods</span><span class="sxs-lookup"><span data-stu-id="850d6-145">Block code</span></span>  
31. <span data-ttu-id="850d6-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="850d6-146">Click OK.</span></span>
32. <span data-ttu-id="850d6-147">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="850d6-147">Click Add String.</span></span>
33. <span data-ttu-id="850d6-148">Laukā Nosaukums ierakstiet 'Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="850d6-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="850d6-149">Uzskaites rindas</span><span class="sxs-lookup"><span data-stu-id="850d6-149">Lines counting</span></span>  
34. <span data-ttu-id="850d6-150">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="850d6-150">Click OK.</span></span>
35. <span data-ttu-id="850d6-151">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="850d6-151">Click Add String.</span></span>
36. <span data-ttu-id="850d6-152">Laukā Nosaukums ierakstiet 'Total amount'.</span><span class="sxs-lookup"><span data-stu-id="850d6-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="850d6-153">Kopējā summa</span><span class="sxs-lookup"><span data-stu-id="850d6-153">Total amount</span></span>  
37. <span data-ttu-id="850d6-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="850d6-154">Click OK.</span></span>
38. <span data-ttu-id="850d6-155">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="850d6-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="850d6-156">Koka struktūrā atlasiet '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="850d6-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="850d6-157">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="850d6-157">Click Bind.</span></span>
    * <span data-ttu-id="850d6-158">Izveidojiet kopsavilkuma rindu katram atmiņā saglabātajam blokam.</span><span class="sxs-lookup"><span data-stu-id="850d6-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="850d6-159">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="850d6-159">Click the Format tab.</span></span>
42. <span data-ttu-id="850d6-160">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="850d6-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="850d6-161">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="850d6-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="850d6-162">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="850d6-162">Click Edit formula.</span></span>
45. <span data-ttu-id="850d6-163">Laukā Formula ievadiet '"Block id: " & '.</span><span class="sxs-lookup"><span data-stu-id="850d6-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="850d6-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="850d6-164">"Block id: " &</span></span>  
46. <span data-ttu-id="850d6-165">Koka struktūrā izvērsiet sadaļu '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="850d6-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="850d6-166">Koka struktūrā atlasiet '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="850d6-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="850d6-167">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="850d6-167">Click Add data source.</span></span>
49. <span data-ttu-id="850d6-168">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="850d6-168">Click Save.</span></span>
50. <span data-ttu-id="850d6-169">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="850d6-169">Close the page.</span></span>
51. <span data-ttu-id="850d6-170">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="850d6-170">Click the Format tab.</span></span>
52. <span data-ttu-id="850d6-171">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="850d6-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="850d6-172">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="850d6-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="850d6-173">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="850d6-173">Click Edit formula.</span></span>
    * <span data-ttu-id="850d6-174">Izveidojiet rindu skaita izvadi katram pārskatā esošajam blokam.</span><span class="sxs-lookup"><span data-stu-id="850d6-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="850d6-175">Laukā Formula ievadiet '"Number of lines in this block: " & '.</span><span class="sxs-lookup"><span data-stu-id="850d6-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="850d6-176">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="850d6-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="850d6-177">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="850d6-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="850d6-178">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="850d6-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="850d6-179">Koka struktūrā atlasiet 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="850d6-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="850d6-180">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="850d6-180">Click Add function.</span></span>
59. <span data-ttu-id="850d6-181">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="850d6-181">Click Add data source.</span></span>
60. <span data-ttu-id="850d6-182">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="850d6-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="850d6-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="850d6-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="850d6-184">Koka struktūrā izvērsiet sadaļu '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="850d6-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="850d6-185">Koka struktūrā atlasiet '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="850d6-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="850d6-186">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="850d6-186">Click Add data source.</span></span>
64. <span data-ttu-id="850d6-187">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="850d6-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="850d6-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="850d6-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="850d6-189">Koka struktūrā atlasiet '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="850d6-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="850d6-190">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="850d6-190">Click Add data source.</span></span>
67. <span data-ttu-id="850d6-191">Laukā Formula ievadiet '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="850d6-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="850d6-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="850d6-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="850d6-193">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="850d6-193">Click Save.</span></span>
69. <span data-ttu-id="850d6-194">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="850d6-194">Close the page.</span></span>
70. <span data-ttu-id="850d6-195">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="850d6-195">Click the Format tab.</span></span>
71. <span data-ttu-id="850d6-196">Koka struktūrā atlasiet 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="850d6-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="850d6-197">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="850d6-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="850d6-198">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="850d6-198">Click Edit formula.</span></span>
    * <span data-ttu-id="850d6-199">Izveidojiet izvadi, kas būs visu šajā pārskatā esošo bloku rēķinā iekļauto summu kopsumma.</span><span class="sxs-lookup"><span data-stu-id="850d6-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="850d6-200">Laukā Formula ievadiet '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="850d6-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="850d6-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="850d6-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="850d6-202">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="850d6-202">Click Save.</span></span>
76. <span data-ttu-id="850d6-203">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="850d6-203">Close the page.</span></span>
77. <span data-ttu-id="850d6-204">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="850d6-204">Click Save.</span></span>
78. <span data-ttu-id="850d6-205">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="850d6-205">Close the page.</span></span>

