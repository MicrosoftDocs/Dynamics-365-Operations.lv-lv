---
title: ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (2. daļa. Aprēķinu konfigurēšana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu formātu, lai to skaitītu un summētu, pamatojoties uz jau ģenerētā teksta izvades datiem. (2. daļa)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6215fe1f32bcb4833bd009b7c33e09edbba17817
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093001"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="33b0b-104">ER formāta konfigurēšana, lai veiktu uzskaiti un summēšanu (2. daļa. Aprēķinu konfigurēšana)</span><span class="sxs-lookup"><span data-stu-id="33b0b-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33b0b-105">Tālāk aprakstītajos soļos ir izskaidrots, kā sistēmas lietotājs, kam ir piešķirta administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektronisko pārskatu sagatavošanas (ER) formātu, lai veiktu uzskaiti un summēšanu, izmantojot jau izveidotās teksta izvades datus.</span><span class="sxs-lookup"><span data-stu-id="33b0b-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="33b0b-106">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="33b0b-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="33b0b-107">Lai veiktu šīs darbības, vispirms ir jāpabeidz procedūras "ER konfigurēt formātu, lai veiktu uzskaiti un summēšanu (1. daļa: Izveidot formātu)" darbības.</span><span class="sxs-lookup"><span data-stu-id="33b0b-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="33b0b-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="33b0b-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="33b0b-109">Izveidot formāta konfigurāciju, lai pievienotu uzskaites un summēšanas detalizētus datus</span><span class="sxs-lookup"><span data-stu-id="33b0b-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="33b0b-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="33b0b-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="33b0b-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="33b0b-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="33b0b-112">Kokā struktūrā izvērsiet 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="33b0b-113">Koka struktūrā atlasiet 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="33b0b-114">Pieņemsim, ka jums ir jāpielāgo korporācijas Microsoft nodrošinātais formāts, pievienojot rindas ar kopsavilkuma datiem Intrastat pārskata beigās.</span><span class="sxs-lookup"><span data-stu-id="33b0b-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="33b0b-115">Lai to izdarītu un varētu veikt izmaiņas, no Microsoft instances ir jāiegūst sava Intrastat konfigurācijas instance.</span><span class="sxs-lookup"><span data-stu-id="33b0b-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="33b0b-116">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="33b0b-117">Laukā Jauns ievadiet 'Derive from Name: Intrastat (DE), Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="33b0b-118">Laukā Nosaukums ierakstiet 'Intrastat (DE) with counting & summing'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="33b0b-119">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="33b0b-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="33b0b-120">Konfigurēt šo pārskatu, lai veiktu uzskaiti un summēšana, izmantojot izejas datus</span><span class="sxs-lookup"><span data-stu-id="33b0b-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="33b0b-121">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="33b0b-121">Click Designer.</span></span>
2. <span data-ttu-id="33b0b-122">Laukā Apkopot izvades datus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="33b0b-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="33b0b-123">Šis karodziņš aktivizē izpildes laikā izvades datu apkopošanas procesu, kas paredzēts Intrastat failu izveidei.</span><span class="sxs-lookup"><span data-stu-id="33b0b-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="33b0b-124">Tas ir jāatkārto dažādiem Intrastat virzieniem, tāpēc pievienojiet īpašo modeļa uzskaitījumu šīs formāta konfigurācijas datu avotu sarakstam.</span><span class="sxs-lookup"><span data-stu-id="33b0b-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="33b0b-125">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="33b0b-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="33b0b-126">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="33b0b-127">Koka struktūrā atlasiet 'Data model\Enumeration '.</span><span class="sxs-lookup"><span data-stu-id="33b0b-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="33b0b-128">Laukā Nosaukums ierakstiet 'Direction'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="33b0b-129">Ievadiet vai atlasiet vērtību laukā Modeļa uzskaitījums.</span><span class="sxs-lookup"><span data-stu-id="33b0b-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="33b0b-130">Atlasiet vērtību Virziens.</span><span class="sxs-lookup"><span data-stu-id="33b0b-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="33b0b-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="33b0b-131">Click OK.</span></span>
9. <span data-ttu-id="33b0b-132">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="33b0b-133">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="33b0b-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="33b0b-134">Laukā Nosaukums ierakstiet '$BlockName'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="33b0b-135">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-135">Click Edit formula.</span></span>
13. <span data-ttu-id="33b0b-136">Laukā Formula ievadiet '"block"'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="33b0b-137">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-137">Click Save.</span></span>
15. <span data-ttu-id="33b0b-138">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-138">Close the page.</span></span>
16. <span data-ttu-id="33b0b-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="33b0b-139">Click OK.</span></span>
17. <span data-ttu-id="33b0b-140">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="33b0b-141">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="33b0b-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="33b0b-142">Laukā Nosaukums ierakstiet '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="33b0b-143">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-143">Click Edit formula.</span></span>
21. <span data-ttu-id="33b0b-144">Laukā Formula ievadiet "record"'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="33b0b-145">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-145">Click Save.</span></span>
23. <span data-ttu-id="33b0b-146">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-146">Close the page.</span></span>
24. <span data-ttu-id="33b0b-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="33b0b-147">Click OK.</span></span>
25. <span data-ttu-id="33b0b-148">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="33b0b-149">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="33b0b-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="33b0b-150">Laukā Nosaukums ierakstiet '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="33b0b-151">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-151">Click Edit formula.</span></span>
29. <span data-ttu-id="33b0b-152">Laukā Formula ievadiet '"InvoicedAmountEUR"'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="33b0b-153">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-153">Click Save.</span></span>
31. <span data-ttu-id="33b0b-154">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-154">Close the page.</span></span>
32. <span data-ttu-id="33b0b-155">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="33b0b-155">Click OK.</span></span>
33. <span data-ttu-id="33b0b-156">Koka struktūrā atlasiet 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="33b0b-157">Noklikšķiniet uz lauka 'Apkopoto datu atslēgas nosaukums' pogas Rediģēt</span><span class="sxs-lookup"><span data-stu-id="33b0b-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="33b0b-158">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-158">Click Add data source.</span></span>
    * <span data-ttu-id="33b0b-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="33b0b-159">$BlockName</span></span>  
36. <span data-ttu-id="33b0b-160">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-160">Click Save.</span></span>
37. <span data-ttu-id="33b0b-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-161">Close the page.</span></span>
38. <span data-ttu-id="33b0b-162">Noklikšķiniet uz lauka Apkopoto datu atslēgas vērtība pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="33b0b-163">Laukā Formula ievadiet “IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")”.</span><span class="sxs-lookup"><span data-stu-id="33b0b-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="33b0b-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="33b0b-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="33b0b-165">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-165">Click Save.</span></span>
41. <span data-ttu-id="33b0b-166">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-166">Close the page.</span></span>
    * <span data-ttu-id="33b0b-167">Saskaitiet šīs secības līnijas.</span><span class="sxs-lookup"><span data-stu-id="33b0b-167">Count the lines of this sequence.</span></span> <span data-ttu-id="33b0b-168">Rezultāti tiks izmantoti ar nosaukumu "bloķēt" atsevišķi dažādiem virzieniem.</span><span class="sxs-lookup"><span data-stu-id="33b0b-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="33b0b-169">Vērtība "Importēt" tiks izmantota visām ienākošajām Intrastat transakcijām.</span><span class="sxs-lookup"><span data-stu-id="33b0b-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="33b0b-170">Vērtība "Eksportēt" tiks izmantota visām Intrastat nosūtītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="33b0b-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="33b0b-171">Uzskatiet to par virtuālu Excel izklājlapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="33b0b-172">Katra transakcijas rindas, kur pirmā kolonna ir "bloķēt", tiek aizpildīta ar attiecīgi ar vērtību "Importēt" un "Eksportēt".</span><span class="sxs-lookup"><span data-stu-id="33b0b-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="33b0b-173">Kokā struktūrā izvērsiet Intrastat\Data: Sequence'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="33b0b-174">Koka struktūrā atlasiet 'Intrastat\Data: Sequence\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="33b0b-175">Noklikšķiniet uz lauka 'Apkopoto datu atslēgas nosaukums' pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="33b0b-176">Saskaitiet šīs secības līnijas.</span><span class="sxs-lookup"><span data-stu-id="33b0b-176">Count the lines of this sequence.</span></span> <span data-ttu-id="33b0b-177">Rezultāti tiks saglabāti atmiņā ar vārdu "ierakstīt".</span><span class="sxs-lookup"><span data-stu-id="33b0b-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="33b0b-178">Koka struktūrā atlasiet '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="33b0b-179">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-179">Click Add data source.</span></span>
47. <span data-ttu-id="33b0b-180">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-180">Click Save.</span></span>
48. <span data-ttu-id="33b0b-181">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-181">Close the page.</span></span>
49. <span data-ttu-id="33b0b-182">Noklikšķiniet uz lauka 'Apkopoto datu atslēgas vērtība' pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="33b0b-183">Laukā Formula ievadiet “Intrastat.CommodityRecord.CommodityCode”.</span><span class="sxs-lookup"><span data-stu-id="33b0b-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="33b0b-184">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-184">Click Save.</span></span>
52. <span data-ttu-id="33b0b-185">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-185">Close the page.</span></span>
    * <span data-ttu-id="33b0b-186">Saskaitiet šīs secības līnijas.</span><span class="sxs-lookup"><span data-stu-id="33b0b-186">Count the lines of this sequence.</span></span> <span data-ttu-id="33b0b-187">Rezultāti tiks izmantoti ar nosaukumu "ierakstīt" atsevišķi dažādiem preces kodiem.</span><span class="sxs-lookup"><span data-stu-id="33b0b-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="33b0b-188">Uzskatiet to par virtuālu Excel izklājlapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="33b0b-189">Katra transakcijas rinda, kur pirmā kolonna ir "bloķēt", tiek aizpildīta ar attiecīgi ar vērtību "Importēt" un "Eksportēt" un otrais bloks "ierakstīt" tiek aizpildīts ar preces koda vērtību.</span><span class="sxs-lookup"><span data-stu-id="33b0b-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="33b0b-190">Koka struktūrā atlasiet 'Intrastat\Data: Sequence\Dispatches?'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="33b0b-191">Noklikšķiniet uz lauka 'Apkopoto datu atslēgas nosaukums' pogas Rediģēt</span><span class="sxs-lookup"><span data-stu-id="33b0b-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="33b0b-192">Koka struktūrā atlasiet '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="33b0b-193">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-193">Click Add data source.</span></span>
57. <span data-ttu-id="33b0b-194">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-194">Click Save.</span></span>
58. <span data-ttu-id="33b0b-195">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-195">Close the page.</span></span>
59. <span data-ttu-id="33b0b-196">Noklikšķiniet uz lauka 'Apkopoto datu atslēgas vērtība' pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="33b0b-197">Laukā Formula ievadiet “Intrastat.CommodityRecord.CommodityCode”.</span><span class="sxs-lookup"><span data-stu-id="33b0b-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="33b0b-198">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-198">Click Save.</span></span>
62. <span data-ttu-id="33b0b-199">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-199">Close the page.</span></span>
63. <span data-ttu-id="33b0b-200">Kokā struktūrā izvērsiet 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="33b0b-201">Kokā struktūrā izvērsiet 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="33b0b-202">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="33b0b-202">Click the Format tab.</span></span>
66. <span data-ttu-id="33b0b-203">Koka struktūrā atlasiet 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="33b0b-204">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="33b0b-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="33b0b-205">Noklikšķiniet uz lauka 'Apkopoto datu atslēgas nosaukums' pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="33b0b-206">Koka struktūrā atlasiet '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="33b0b-207">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-207">Click Add data source.</span></span>
71. <span data-ttu-id="33b0b-208">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-208">Click Save.</span></span>
72. <span data-ttu-id="33b0b-209">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-209">Close the page.</span></span>
    * <span data-ttu-id="33b0b-210">Aprēķiniet šīs secības rindas rēķinā iekļauto summu vērtību.</span><span class="sxs-lookup"><span data-stu-id="33b0b-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="33b0b-211">Rezultāti tiks izmantoti ar nosaukumu "InvoicedAmountEUR" atsevišķi dažādiem Intrastat virzieniem un preces kodiem.</span><span class="sxs-lookup"><span data-stu-id="33b0b-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="33b0b-212">Uzskatiet to par virtuālu Excel izklājlapas izveidi.</span><span class="sxs-lookup"><span data-stu-id="33b0b-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="33b0b-213">Katra transakcijas rindas, kur pirmā kolonna ir "bloķēt", tiek aizpildīta ar attiecīgi ar vērtību "Importēt" un "Eksportēt".</span><span class="sxs-lookup"><span data-stu-id="33b0b-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="33b0b-214">Otrs bloks "ierakstīt" tiek aizpildīts ar preces koda vērtību un trešā kolonna "InvoicedAmountEUR" tiek aizpildīta ar rēķina summas vērtību.</span><span class="sxs-lookup"><span data-stu-id="33b0b-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="33b0b-215">Kokā struktūrā izvērsiet 'Intrastat\Data\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="33b0b-216">Koka struktūrā izvērsiet 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="33b0b-217">Noklikšķiniet uz cilnes Formāts.</span><span class="sxs-lookup"><span data-stu-id="33b0b-217">Click the Format tab.</span></span>
76. <span data-ttu-id="33b0b-218">Koka struktūrā atlasiet 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="33b0b-219">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="33b0b-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="33b0b-220">Noklikšķiniet uz lauka 'Apkopoto datu atslēgas nosaukums' pogas Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="33b0b-221">Koka struktūrā atlasiet '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="33b0b-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="33b0b-222">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-222">Click Add data source.</span></span>
81. <span data-ttu-id="33b0b-223">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-223">Click Save.</span></span>
82. <span data-ttu-id="33b0b-224">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-224">Close the page.</span></span>
83. <span data-ttu-id="33b0b-225">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="33b0b-225">Click Save.</span></span>
84. <span data-ttu-id="33b0b-226">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="33b0b-226">Close the page.</span></span>

