--- 
title: "Elektronisko pārskatu veidošanas (ER) formātu konfigurāciju izveide"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8c11f64fd899b8be4e6c3179913787eb2c32c6c6
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="create-electronic-reporting-er-format-configurations"></a><span data-ttu-id="28677-103">Elektronisko pārskatu veidošanas (ER) formātu konfigurāciju izveide</span><span class="sxs-lookup"><span data-stu-id="28677-103">Create Electronic reporting (ER) format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28677-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektroniskā pārskata izstrādātājs var izveidot formāta konfigurāciju Elektroniskajos pārskatos (ER).</span><span class="sxs-lookup"><span data-stu-id="28677-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="28677-105">Šī formāta konfigurāciju noteiks to elektronisko dokumentu formātu, kas tiek izmantoti maksājumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="28677-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="28677-106">Šajā piemērā jāuzveido parauga uzņēmuma Litware, Inc. formāta konfigurācija. Lai varētu veikt šīs darbības, vispirms jāizpilda procedūrā “Modeļa kartēšana izvēlētajos datu avotos” aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="28677-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="28677-107">Jaunas formāta konfigurācijas izveide</span><span class="sxs-lookup"><span data-stu-id="28677-107">Create a new format configuration</span></span>
1. <span data-ttu-id="28677-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="28677-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="28677-109">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="28677-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="28677-110">Kokā atlasiet “Maksājumi (vienkāršotais modelis)”.</span><span class="sxs-lookup"><span data-stu-id="28677-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="28677-111">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="28677-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="28677-112">Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="28677-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="28677-113">Laukā Nosaukums ierakstiet "BAKS (UK fiktīvs)".</span><span class="sxs-lookup"><span data-stu-id="28677-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="28677-114">BAKS (UK fiktīvs)</span><span class="sxs-lookup"><span data-stu-id="28677-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="28677-115">Laukā Apraksts ierakstiet "BAKS kreditora maksājuma formāts (UK fiktīvs)".</span><span class="sxs-lookup"><span data-stu-id="28677-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="28677-116">BAKS kreditora maksājuma formāts (UK fiktīvs)</span><span class="sxs-lookup"><span data-stu-id="28677-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="28677-117">Šeit tiek automātiski ievadīts aktīvais konfigurācijas nodrošinātājs.</span><span class="sxs-lookup"><span data-stu-id="28677-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="28677-118">Šis nodrošinātājs varēs uzturēt šo konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="28677-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="28677-119">Citi nodrošinātāji var izmantot šo konfigurāciju, bet nevar uzturēt to.</span><span class="sxs-lookup"><span data-stu-id="28677-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="28677-120">Var definēt noteiktu elektroniskā dokumenta formātu.</span><span class="sxs-lookup"><span data-stu-id="28677-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="28677-121">Atstājiet šo lauku tukšu, ja vēlaties atlasīt formātu izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="28677-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="28677-122">Ievadiet vai atlasiet kādu vērtību laukā Datu modelis.</span><span class="sxs-lookup"><span data-stu-id="28677-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="28677-123">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="28677-123">Click Create configuration.</span></span>
    * <span data-ttu-id="28677-124">Tika izveidota jauna konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="28677-124">A new configuration has been created.</span></span> <span data-ttu-id="28677-125">Melnraksta versiju var izmantot, lai saglabātu dizaina formātu elektronisko dokumentu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="28677-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="28677-126">Elektronisko dokumentu formāta noformēšana</span><span class="sxs-lookup"><span data-stu-id="28677-126">Design format of electronic document</span></span>
1. <span data-ttu-id="28677-127">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="28677-127">Click Designer.</span></span>
2. <span data-ttu-id="28677-128">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="28677-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="28677-129">Kokā atlasiet "Vispārīgi\Fails".</span><span class="sxs-lookup"><span data-stu-id="28677-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="28677-130">Laukā Nosaukums ierakstiet "Xml".</span><span class="sxs-lookup"><span data-stu-id="28677-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="28677-131">Xml</span><span class="sxs-lookup"><span data-stu-id="28677-131">Xml</span></span>  
5. <span data-ttu-id="28677-132">Laukā Kodēšana ierakstiet "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="28677-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="28677-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="28677-133">UTF-8</span></span>  
6. <span data-ttu-id="28677-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-134">Click OK.</span></span>
7. <span data-ttu-id="28677-135">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="28677-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="28677-136">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="28677-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="28677-137">Laukā Nosaukums ierakstiet "Ziņojums".</span><span class="sxs-lookup"><span data-stu-id="28677-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="28677-138">Paziņojums</span><span class="sxs-lookup"><span data-stu-id="28677-138">Message</span></span>  
10. <span data-ttu-id="28677-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-139">Click OK.</span></span>
11. <span data-ttu-id="28677-140">Koka struktūrā atlasiet zaru “Xml\Ziņojums”.</span><span class="sxs-lookup"><span data-stu-id="28677-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="28677-141">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-141">Click Add Element.</span></span>
13. <span data-ttu-id="28677-142">Laukā Nosaukums ievadiet "ProcessingDate".</span><span class="sxs-lookup"><span data-stu-id="28677-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="28677-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="28677-143">ProcessingDate</span></span>  
14. <span data-ttu-id="28677-144">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-144">Click OK.</span></span>
15. <span data-ttu-id="28677-145">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-145">Click Add Element.</span></span>
16. <span data-ttu-id="28677-146">Laukā Nosaukums ierakstiet "MessageId".</span><span class="sxs-lookup"><span data-stu-id="28677-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="28677-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="28677-147">MessageId</span></span>  
17. <span data-ttu-id="28677-148">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-148">Click OK.</span></span>
18. <span data-ttu-id="28677-149">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-149">Click Add Element.</span></span>
19. <span data-ttu-id="28677-150">Laukā Nosaukums ierakstiet "Maksājumi".</span><span class="sxs-lookup"><span data-stu-id="28677-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="28677-151">Maksājumi</span><span class="sxs-lookup"><span data-stu-id="28677-151">Payments</span></span>  
20. <span data-ttu-id="28677-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-152">Click OK.</span></span>
21. <span data-ttu-id="28677-153">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="28677-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="28677-154">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-154">Click Add Element.</span></span>
23. <span data-ttu-id="28677-155">Laukā Nosaukums ierakstiet "Krājums".</span><span class="sxs-lookup"><span data-stu-id="28677-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="28677-156">Objekts</span><span class="sxs-lookup"><span data-stu-id="28677-156">Item</span></span>  
24. <span data-ttu-id="28677-157">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-157">Click OK.</span></span>
25. <span data-ttu-id="28677-158">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.</span><span class="sxs-lookup"><span data-stu-id="28677-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="28677-159">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="28677-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="28677-160">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="28677-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="28677-161">Laukā Nosaukums ierakstiet "Id".</span><span class="sxs-lookup"><span data-stu-id="28677-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="28677-162">ID</span><span class="sxs-lookup"><span data-stu-id="28677-162">Id</span></span>  
29. <span data-ttu-id="28677-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-163">Click OK.</span></span>
30. <span data-ttu-id="28677-164">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="28677-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="28677-165">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="28677-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="28677-166">Laukā Nosaukums ierakstiet "Kreditors".</span><span class="sxs-lookup"><span data-stu-id="28677-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="28677-167">Kreditors</span><span class="sxs-lookup"><span data-stu-id="28677-167">Vendor</span></span>  
33. <span data-ttu-id="28677-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-168">Click OK.</span></span>
34. <span data-ttu-id="28677-169">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="28677-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="28677-170">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-170">Click Add Element.</span></span>
36. <span data-ttu-id="28677-171">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="28677-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="28677-172">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="28677-172">Name</span></span>  
37. <span data-ttu-id="28677-173">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-173">Click OK.</span></span>
38. <span data-ttu-id="28677-174">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-174">Click Add Element.</span></span>
39. <span data-ttu-id="28677-175">Laukā Nosaukums ierakstiet "Banka".</span><span class="sxs-lookup"><span data-stu-id="28677-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="28677-176">Banka</span><span class="sxs-lookup"><span data-stu-id="28677-176">Bank</span></span>  
40. <span data-ttu-id="28677-177">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-177">Click OK.</span></span>
41. <span data-ttu-id="28677-178">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka”.</span><span class="sxs-lookup"><span data-stu-id="28677-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="28677-179">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-179">Click Add Element.</span></span>
43. <span data-ttu-id="28677-180">Laukā Nosaukums ierakstiet "RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="28677-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="28677-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="28677-181">RoutingNumber</span></span>  
44. <span data-ttu-id="28677-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-182">Click OK.</span></span>
45. <span data-ttu-id="28677-183">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-183">Click Add Element.</span></span>
46. <span data-ttu-id="28677-184">Laukā Nosaukums ierakstiet "AccountNumber".</span><span class="sxs-lookup"><span data-stu-id="28677-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="28677-185">Konta numurs</span><span class="sxs-lookup"><span data-stu-id="28677-185">AccountNumber</span></span>  
47. <span data-ttu-id="28677-186">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-186">Click OK.</span></span>
48. <span data-ttu-id="28677-187">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors”.</span><span class="sxs-lookup"><span data-stu-id="28677-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="28677-188">Noklikšķiniet uz Kopēt.</span><span class="sxs-lookup"><span data-stu-id="28677-188">Click Copy.</span></span>
50. <span data-ttu-id="28677-189">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.</span><span class="sxs-lookup"><span data-stu-id="28677-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="28677-190">Noklikšķiniet uz Ielīmēt.</span><span class="sxs-lookup"><span data-stu-id="28677-190">Click Paste.</span></span>
52. <span data-ttu-id="28677-191">Laukā Nosaukums ierakstiet "Maksātājs".</span><span class="sxs-lookup"><span data-stu-id="28677-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="28677-192">Maksātājs</span><span class="sxs-lookup"><span data-stu-id="28677-192">Payer</span></span>  
53. <span data-ttu-id="28677-193">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums”.</span><span class="sxs-lookup"><span data-stu-id="28677-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="28677-194">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-194">Click Add Element.</span></span>
55. <span data-ttu-id="28677-195">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="28677-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="28677-196">Valūta</span><span class="sxs-lookup"><span data-stu-id="28677-196">Currency</span></span>  
56. <span data-ttu-id="28677-197">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-197">Click OK.</span></span>
57. <span data-ttu-id="28677-198">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-198">Click Add Element.</span></span>
58. <span data-ttu-id="28677-199">Laukā Nosaukums ierakstiet "Apraksts".</span><span class="sxs-lookup"><span data-stu-id="28677-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="28677-200">Apraksts</span><span class="sxs-lookup"><span data-stu-id="28677-200">Description</span></span>  
59. <span data-ttu-id="28677-201">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-201">Click OK.</span></span>
60. <span data-ttu-id="28677-202">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-202">Click Add Element.</span></span>
61. <span data-ttu-id="28677-203">Laukā Nosaukums ierakstiet "TransDate".</span><span class="sxs-lookup"><span data-stu-id="28677-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="28677-204">Darbības datums</span><span class="sxs-lookup"><span data-stu-id="28677-204">TransDate</span></span>  
62. <span data-ttu-id="28677-205">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-205">Click OK.</span></span>
63. <span data-ttu-id="28677-206">Noklikšķiniet uz Pievienot elementu.</span><span class="sxs-lookup"><span data-stu-id="28677-206">Click Add Element.</span></span>
64. <span data-ttu-id="28677-207">Laukā Nosaukums ierakstiet "Summa".</span><span class="sxs-lookup"><span data-stu-id="28677-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="28677-208">Summa</span><span class="sxs-lookup"><span data-stu-id="28677-208">Amount</span></span>  
65. <span data-ttu-id="28677-209">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="28677-210">Formātā komponentu sagatavošana kartēšanai datu modeļa elementos</span><span class="sxs-lookup"><span data-stu-id="28677-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="28677-211">Koka struktūrā atlasiet zaru “Xml\Ziņojums\ProcessingDate”.</span><span class="sxs-lookup"><span data-stu-id="28677-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="28677-212">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="28677-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="28677-213">Koka struktūrā atlasiet zaru “Teksts\DateTime”.</span><span class="sxs-lookup"><span data-stu-id="28677-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="28677-214">Laukā Formāts ierakstiet "gggg-MM-dd".</span><span class="sxs-lookup"><span data-stu-id="28677-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="28677-215">gggg-MM-dd</span><span class="sxs-lookup"><span data-stu-id="28677-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="28677-216">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-216">Click OK.</span></span>
6. <span data-ttu-id="28677-217">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\TransDate”.</span><span class="sxs-lookup"><span data-stu-id="28677-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="28677-218">Noklikšķiniet uz Pievienot DateTime.</span><span class="sxs-lookup"><span data-stu-id="28677-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="28677-219">Laukā Formāts ierakstiet "gggg-MM-dd".</span><span class="sxs-lookup"><span data-stu-id="28677-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="28677-220">gggg-MM-dd</span><span class="sxs-lookup"><span data-stu-id="28677-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="28677-221">Laukā DateTime tips atlasiet “Datums”.</span><span class="sxs-lookup"><span data-stu-id="28677-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="28677-222">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28677-222">Click OK.</span></span>
11. <span data-ttu-id="28677-223">Koka struktūrā atlasiet zaru “Xml\Ziņojums\MessageId”.</span><span class="sxs-lookup"><span data-stu-id="28677-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="28677-224">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="28677-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="28677-225">Kokā atlasiet elementu “Teksts\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="28677-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="28677-226">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-226">Click OK.</span></span>
15. <span data-ttu-id="28677-227">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="28677-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="28677-228">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="28677-228">Click Add String.</span></span>
17. <span data-ttu-id="28677-229">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-229">Click OK.</span></span>
18. <span data-ttu-id="28677-230">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="28677-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="28677-231">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="28677-231">Click Add String.</span></span>
20. <span data-ttu-id="28677-232">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-232">Click OK.</span></span>
21. <span data-ttu-id="28677-233">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Kreditors\Banka\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="28677-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="28677-234">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="28677-234">Click Add String.</span></span>
23. <span data-ttu-id="28677-235">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-235">Click OK.</span></span>
24. <span data-ttu-id="28677-236">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Nosaukums”.</span><span class="sxs-lookup"><span data-stu-id="28677-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="28677-237">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="28677-237">Click Add String.</span></span>
26. <span data-ttu-id="28677-238">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-238">Click OK.</span></span>
27. <span data-ttu-id="28677-239">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="28677-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="28677-240">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="28677-240">Click Add String.</span></span>
29. <span data-ttu-id="28677-241">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-241">Click OK.</span></span>
30. <span data-ttu-id="28677-242">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Maksātājs\Banka\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="28677-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="28677-243">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="28677-243">Click Add String.</span></span>
32. <span data-ttu-id="28677-244">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-244">Click OK.</span></span>
33. <span data-ttu-id="28677-245">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Valūta”.</span><span class="sxs-lookup"><span data-stu-id="28677-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="28677-246">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="28677-246">Click Add String.</span></span>
35. <span data-ttu-id="28677-247">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-247">Click OK.</span></span>
36. <span data-ttu-id="28677-248">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Apraksts”.</span><span class="sxs-lookup"><span data-stu-id="28677-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="28677-249">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="28677-249">Click Add String.</span></span>
38. <span data-ttu-id="28677-250">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-250">Click OK.</span></span>
39. <span data-ttu-id="28677-251">Koka struktūrā atlasiet zaru “Xml\Ziņojums\Maksājumi\Krājums\Summa”.</span><span class="sxs-lookup"><span data-stu-id="28677-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="28677-252">Noklikšķiniet uz Pievienot virkni.</span><span class="sxs-lookup"><span data-stu-id="28677-252">Click Add String.</span></span>
41. <span data-ttu-id="28677-253">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="28677-253">Click OK.</span></span>
42. <span data-ttu-id="28677-254">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="28677-254">Click Save.</span></span>
43. <span data-ttu-id="28677-255">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="28677-255">Close the page.</span></span>


