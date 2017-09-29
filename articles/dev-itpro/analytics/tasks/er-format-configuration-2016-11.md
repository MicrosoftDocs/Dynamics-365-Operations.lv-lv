--- 
title: "Izveidot formāta konfigurāciju elektronisko pārskatu veidošanai (ER)"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot formāta konfigurāciju Elektroniskajos pārskatos (ER)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="0e629-103">Izveidot formāta konfigurāciju elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="0e629-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e629-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot formāta konfigurāciju Elektroniskajos pārskatos (ER).</span><span class="sxs-lookup"><span data-stu-id="0e629-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="0e629-105">Šī formāta konfigurāciju noteiks to elektronisko dokumentu formātu, kas tiek izmantoti maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="0e629-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="0e629-106">Šajā piemērā jāuzveido parauga uzņēmuma Litware, Inc. formāta konfigurācija. Lai varētu veikt šīs darbības, vispirms jāizpilda procedūrā “Modeļa kartēšana izvēlētajos datu avotos” aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0e629-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="0e629-107">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="0e629-107">Create a new format configuration</span></span>
1. <span data-ttu-id="0e629-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="0e629-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0e629-109">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="0e629-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0e629-110">Kokā atlasiet “Maksājumi (vienkāršotais modelis)”.</span><span class="sxs-lookup"><span data-stu-id="0e629-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="0e629-111">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0e629-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="0e629-112">Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="0e629-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="0e629-113">Laukā Nosaukums ierakstiet "BAKS (UK fiktīvs)".</span><span class="sxs-lookup"><span data-stu-id="0e629-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="0e629-114">BAKS (UK fiktīvs)</span><span class="sxs-lookup"><span data-stu-id="0e629-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="0e629-115">Laukā Apraksts ierakstiet "BAKS kreditora maksājuma formāts (UK fiktīvs)".</span><span class="sxs-lookup"><span data-stu-id="0e629-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="0e629-116">BAKS kreditora maksājuma formāts (UK fiktīvs)</span><span class="sxs-lookup"><span data-stu-id="0e629-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="0e629-117">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="0e629-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="0e629-118">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0e629-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="0e629-119">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="0e629-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="0e629-120">Var definēt noteiktu elektroniskā dokumenta formātu.</span><span class="sxs-lookup"><span data-stu-id="0e629-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="0e629-121">Atstājiet šo lauku tukšu, ja vēlaties atlasīt formātu izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="0e629-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="0e629-122">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="0e629-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="0e629-123">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="0e629-123">Click Create configuration.</span></span>
    * <span data-ttu-id="0e629-124">Tika izveidota jauna konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="0e629-124">A new configuration has been created.</span></span> <span data-ttu-id="0e629-125">Melnraksta versiju var izmantot, lai saglabātu dizaina formātu elektronisko dokumentu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="0e629-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="0e629-126">Elektronisko dokumentu formāta noformēšana</span><span class="sxs-lookup"><span data-stu-id="0e629-126">Design format of electronic document</span></span>
1. <span data-ttu-id="0e629-127">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="0e629-127">Click Designer.</span></span>
2. <span data-ttu-id="0e629-128">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="0e629-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="0e629-129">Kokā atlasiet "Vispārīgi\Fails".</span><span class="sxs-lookup"><span data-stu-id="0e629-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="0e629-130">Laukā Nosaukums ierakstiet "Xml".</span><span class="sxs-lookup"><span data-stu-id="0e629-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="0e629-131">Xml</span><span class="sxs-lookup"><span data-stu-id="0e629-131">Xml</span></span>  
5. <span data-ttu-id="0e629-132">Laukā Kodēšana ierakstiet "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="0e629-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="0e629-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="0e629-133">UTF-8</span></span>  
6. <span data-ttu-id="0e629-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-134">Click OK.</span></span>
7. <span data-ttu-id="0e629-135">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0e629-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="0e629-136">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="0e629-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="0e629-137">Laukā Nosaukums ierakstiet "Ziņojums".</span><span class="sxs-lookup"><span data-stu-id="0e629-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="0e629-138">Paziņojums</span><span class="sxs-lookup"><span data-stu-id="0e629-138">Message</span></span>  
10. <span data-ttu-id="0e629-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-139">Click OK.</span></span>
11. <span data-ttu-id="0e629-140">Koka struktūrā atlasiet zaru “Xml\Ziņojums”.</span><span class="sxs-lookup"><span data-stu-id="0e629-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="0e629-141">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-141">Click Add Element.</span></span>
13. <span data-ttu-id="0e629-142">Laukā Nosaukums ievadiet "ProcessingDate".</span><span class="sxs-lookup"><span data-stu-id="0e629-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="0e629-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="0e629-143">ProcessingDate</span></span>  
14. <span data-ttu-id="0e629-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-144">Click OK.</span></span>
15. <span data-ttu-id="0e629-145">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-145">Click Add Element.</span></span>
16. <span data-ttu-id="0e629-146">Laukā Nosaukums ierakstiet "MessageId".</span><span class="sxs-lookup"><span data-stu-id="0e629-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="0e629-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="0e629-147">MessageId</span></span>  
17. <span data-ttu-id="0e629-148">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-148">Click OK.</span></span>
18. <span data-ttu-id="0e629-149">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-149">Click Add Element.</span></span>
19. <span data-ttu-id="0e629-150">Laukā Nosaukums ierakstiet "Maksājumi".</span><span class="sxs-lookup"><span data-stu-id="0e629-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="0e629-151">Maksājumi</span><span class="sxs-lookup"><span data-stu-id="0e629-151">Payments</span></span>  
20. <span data-ttu-id="0e629-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-152">Click OK.</span></span>
21. <span data-ttu-id="0e629-153">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="0e629-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="0e629-154">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-154">Click Add Element.</span></span>
23. <span data-ttu-id="0e629-155">Laukā Nosaukums ierakstiet "Krājums".</span><span class="sxs-lookup"><span data-stu-id="0e629-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="0e629-156">Objekts</span><span class="sxs-lookup"><span data-stu-id="0e629-156">Item</span></span>  
24. <span data-ttu-id="0e629-157">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-157">Click OK.</span></span>
25. <span data-ttu-id="0e629-158">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.</span><span class="sxs-lookup"><span data-stu-id="0e629-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="0e629-159">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0e629-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="0e629-160">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="0e629-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="0e629-161">Laukā Nosaukums ierakstiet "Id".</span><span class="sxs-lookup"><span data-stu-id="0e629-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="0e629-162">ID</span><span class="sxs-lookup"><span data-stu-id="0e629-162">Id</span></span>  
29. <span data-ttu-id="0e629-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-163">Click OK.</span></span>
30. <span data-ttu-id="0e629-164">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0e629-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="0e629-165">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="0e629-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="0e629-166">Laukā Nosaukums ierakstiet "Kreditors".</span><span class="sxs-lookup"><span data-stu-id="0e629-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="0e629-167">Kreditors</span><span class="sxs-lookup"><span data-stu-id="0e629-167">Vendor</span></span>  
33. <span data-ttu-id="0e629-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-168">Click OK.</span></span>
34. <span data-ttu-id="0e629-169">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="0e629-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="0e629-170">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-170">Click Add Element.</span></span>
36. <span data-ttu-id="0e629-171">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="0e629-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="0e629-172">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="0e629-172">Name</span></span>  
37. <span data-ttu-id="0e629-173">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-173">Click OK.</span></span>
38. <span data-ttu-id="0e629-174">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-174">Click Add Element.</span></span>
39. <span data-ttu-id="0e629-175">Laukā Nosaukums ierakstiet "Banka".</span><span class="sxs-lookup"><span data-stu-id="0e629-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="0e629-176">Banka</span><span class="sxs-lookup"><span data-stu-id="0e629-176">Bank</span></span>  
40. <span data-ttu-id="0e629-177">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-177">Click OK.</span></span>
41. <span data-ttu-id="0e629-178">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka”.</span><span class="sxs-lookup"><span data-stu-id="0e629-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="0e629-179">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-179">Click Add Element.</span></span>
43. <span data-ttu-id="0e629-180">Laukā Nosaukums ierakstiet "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="0e629-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="0e629-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="0e629-181">RoutingNumber</span></span>  
44. <span data-ttu-id="0e629-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-182">Click OK.</span></span>
45. <span data-ttu-id="0e629-183">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-183">Click Add Element.</span></span>
46. <span data-ttu-id="0e629-184">Laukā Nosaukums ierakstiet "AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="0e629-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="0e629-185">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="0e629-185">AccountNumber</span></span>  
47. <span data-ttu-id="0e629-186">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-186">Click OK.</span></span>
48. <span data-ttu-id="0e629-187">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="0e629-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="0e629-188">Noklikšķiniet uz Kopēt.</span><span class="sxs-lookup"><span data-stu-id="0e629-188">Click Copy.</span></span>
50. <span data-ttu-id="0e629-189">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.</span><span class="sxs-lookup"><span data-stu-id="0e629-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="0e629-190">Noklikšķiniet uz Ielīmēt.</span><span class="sxs-lookup"><span data-stu-id="0e629-190">Click Paste.</span></span>
52. <span data-ttu-id="0e629-191">Laukā Nosaukums ierakstiet "Maksātājs".</span><span class="sxs-lookup"><span data-stu-id="0e629-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="0e629-192">Maksātājs</span><span class="sxs-lookup"><span data-stu-id="0e629-192">Payer</span></span>  
53. <span data-ttu-id="0e629-193">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.</span><span class="sxs-lookup"><span data-stu-id="0e629-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="0e629-194">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-194">Click Add Element.</span></span>
55. <span data-ttu-id="0e629-195">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="0e629-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="0e629-196">Valūta</span><span class="sxs-lookup"><span data-stu-id="0e629-196">Currency</span></span>  
56. <span data-ttu-id="0e629-197">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-197">Click OK.</span></span>
57. <span data-ttu-id="0e629-198">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-198">Click Add Element.</span></span>
58. <span data-ttu-id="0e629-199">Laukā Nosaukums ierakstiet "Apraksts".</span><span class="sxs-lookup"><span data-stu-id="0e629-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="0e629-200">apraksts</span><span class="sxs-lookup"><span data-stu-id="0e629-200">Description</span></span>  
59. <span data-ttu-id="0e629-201">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-201">Click OK.</span></span>
60. <span data-ttu-id="0e629-202">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-202">Click Add Element.</span></span>
61. <span data-ttu-id="0e629-203">Laukā Nosaukums ierakstiet "TransDate".</span><span class="sxs-lookup"><span data-stu-id="0e629-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="0e629-204">Darbības datums</span><span class="sxs-lookup"><span data-stu-id="0e629-204">TransDate</span></span>  
62. <span data-ttu-id="0e629-205">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-205">Click OK.</span></span>
63. <span data-ttu-id="0e629-206">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="0e629-206">Click Add Element.</span></span>
64. <span data-ttu-id="0e629-207">Laukā Nosaukums ierakstiet "Summa".</span><span class="sxs-lookup"><span data-stu-id="0e629-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="0e629-208">Summa</span><span class="sxs-lookup"><span data-stu-id="0e629-208">Amount</span></span>  
65. <span data-ttu-id="0e629-209">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="0e629-210">Formātā komponentu sagatavošana kartēšanai datu modeļa elementos</span><span class="sxs-lookup"><span data-stu-id="0e629-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="0e629-211">Koka struktūrā atlasiet zaru “Xml\Ziņojums\ProcessingDate”.</span><span class="sxs-lookup"><span data-stu-id="0e629-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="0e629-212">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0e629-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="0e629-213">Koka struktūrā atlasiet zaru “Teksts\DateTime”.</span><span class="sxs-lookup"><span data-stu-id="0e629-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="0e629-214">Laukā Formāts ierakstiet "gggg-MM-dd".</span><span class="sxs-lookup"><span data-stu-id="0e629-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="0e629-215">gggg-MM-dd</span><span class="sxs-lookup"><span data-stu-id="0e629-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="0e629-216">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-216">Click OK.</span></span>
6. <span data-ttu-id="0e629-217">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\TransDate”.</span><span class="sxs-lookup"><span data-stu-id="0e629-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="0e629-218">Noklikšķiniet uz Pievienot DateTime.</span><span class="sxs-lookup"><span data-stu-id="0e629-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="0e629-219">Laukā Formāts ierakstiet "gggg-MM-dd".</span><span class="sxs-lookup"><span data-stu-id="0e629-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="0e629-220">gggg-MM-dd</span><span class="sxs-lookup"><span data-stu-id="0e629-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="0e629-221">Laukā DateTime tips atlasiet “Datums”.</span><span class="sxs-lookup"><span data-stu-id="0e629-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="0e629-222">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e629-222">Click OK.</span></span>
11. <span data-ttu-id="0e629-223">Koka struktūrā atlasiet zaru “Xml\Ziņojums\MessageId”.</span><span class="sxs-lookup"><span data-stu-id="0e629-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="0e629-224">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="0e629-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="0e629-225">Kokā atlasiet elementu “Teksts\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="0e629-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="0e629-226">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-226">Click OK.</span></span>
15. <span data-ttu-id="0e629-227">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="0e629-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="0e629-228">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="0e629-228">Click Add String.</span></span>
17. <span data-ttu-id="0e629-229">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-229">Click OK.</span></span>
18. <span data-ttu-id="0e629-230">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="0e629-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="0e629-231">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="0e629-231">Click Add String.</span></span>
20. <span data-ttu-id="0e629-232">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-232">Click OK.</span></span>
21. <span data-ttu-id="0e629-233">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="0e629-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="0e629-234">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="0e629-234">Click Add String.</span></span>
23. <span data-ttu-id="0e629-235">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-235">Click OK.</span></span>
24. <span data-ttu-id="0e629-236">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="0e629-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="0e629-237">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="0e629-237">Click Add String.</span></span>
26. <span data-ttu-id="0e629-238">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-238">Click OK.</span></span>
27. <span data-ttu-id="0e629-239">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="0e629-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="0e629-240">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="0e629-240">Click Add String.</span></span>
29. <span data-ttu-id="0e629-241">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-241">Click OK.</span></span>
30. <span data-ttu-id="0e629-242">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="0e629-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="0e629-243">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="0e629-243">Click Add String.</span></span>
32. <span data-ttu-id="0e629-244">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-244">Click OK.</span></span>
33. <span data-ttu-id="0e629-245">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="0e629-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="0e629-246">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="0e629-246">Click Add String.</span></span>
35. <span data-ttu-id="0e629-247">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-247">Click OK.</span></span>
36. <span data-ttu-id="0e629-248">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Apraksts”.</span><span class="sxs-lookup"><span data-stu-id="0e629-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="0e629-249">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="0e629-249">Click Add String.</span></span>
38. <span data-ttu-id="0e629-250">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-250">Click OK.</span></span>
39. <span data-ttu-id="0e629-251">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Summa”.</span><span class="sxs-lookup"><span data-stu-id="0e629-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="0e629-252">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="0e629-252">Click Add String.</span></span>
41. <span data-ttu-id="0e629-253">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="0e629-253">Click OK.</span></span>
42. <span data-ttu-id="0e629-254">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0e629-254">Click Save.</span></span>
43. <span data-ttu-id="0e629-255">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e629-255">Close the page.</span></span>


