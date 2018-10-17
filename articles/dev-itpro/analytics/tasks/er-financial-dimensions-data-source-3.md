--- 
title: "ER finanšu dimensijas, ko izmanto kā datu avotu (3. daļa. Pārskata izkārtošana)"
description: "Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 45096a728ad6f9e331b53b4e12ca0ff9317a3939
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a><span data-ttu-id="dbf40-103">ER Finanšu dimensijas, ko izmanto kā datu avotu (3. daļa: Pārskata izkārtošana)</span><span class="sxs-lookup"><span data-stu-id="dbf40-103">ER Use financial dimensions as a data source (Part 3: Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dbf40-104">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="dbf40-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="dbf40-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="dbf40-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="dbf40-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (2. daļa: Modeļa kartēšana).</span><span class="sxs-lookup"><span data-stu-id="dbf40-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="dbf40-107">Izveidojiet pārskatu, lai parādītu finanšu dimensijas</span><span class="sxs-lookup"><span data-stu-id="dbf40-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="dbf40-108">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="dbf40-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="dbf40-109">Koka struktūrā atlasiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="dbf40-110">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="dbf40-111">Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="dbf40-112">Izmantojiet iepriekš izveidoto modeli kā jaunā pārskata datu avotu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="dbf40-113">Laukā Nosaukums ierakstiet 'Virsgrāmatas žurnāla pārskats'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="dbf40-114">Laukā Datu modeļa definīcija atlasiet Ieraksts.</span><span class="sxs-lookup"><span data-stu-id="dbf40-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="dbf40-115">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="dbf40-115">Click Create configuration.</span></span>
8. <span data-ttu-id="dbf40-116">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="dbf40-116">Click Designer.</span></span>
9. <span data-ttu-id="dbf40-117">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="dbf40-118">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="dbf40-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="dbf40-119">Laukā Nosaukums ierakstiet 'Sakne'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="dbf40-120">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="dbf40-120">Click OK.</span></span>
13. <span data-ttu-id="dbf40-121">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="dbf40-122">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="dbf40-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="dbf40-123">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="dbf40-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="dbf40-124">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="dbf40-124">Click OK.</span></span>
17. <span data-ttu-id="dbf40-125">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="dbf40-126">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="dbf40-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="dbf40-127">Laukā Nosaukums ierakstiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="dbf40-128">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="dbf40-128">Click OK.</span></span>
21. <span data-ttu-id="dbf40-129">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="dbf40-130">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="dbf40-131">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="dbf40-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="dbf40-132">Laukā Nosaukums ierakstiet 'Partija'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="dbf40-133">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="dbf40-133">Click OK.</span></span>
26. <span data-ttu-id="dbf40-134">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="dbf40-135">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="dbf40-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="dbf40-136">Laukā Nosaukums ierakstiet 'Darbība'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="dbf40-137">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="dbf40-137">Click OK.</span></span>
30. <span data-ttu-id="dbf40-138">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="dbf40-139">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="dbf40-140">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="dbf40-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="dbf40-141">Laukā Nosaukums ierakstiet 'Dokuments'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="dbf40-142">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbf40-142">Click OK.</span></span>
35. <span data-ttu-id="dbf40-143">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="dbf40-144">Laukā Nosaukums ierakstiet 'Datums'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="dbf40-145">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbf40-145">Click OK.</span></span>
38. <span data-ttu-id="dbf40-146">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="dbf40-147">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="dbf40-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="dbf40-148">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbf40-148">Click OK.</span></span>
41. <span data-ttu-id="dbf40-149">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="dbf40-150">Laukā Nosaukums ierakstiet 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="dbf40-151">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbf40-151">Click OK.</span></span>
44. <span data-ttu-id="dbf40-152">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="dbf40-153">Laukā Nosaukums ierakstiet 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="dbf40-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbf40-154">Click OK.</span></span>
47. <span data-ttu-id="dbf40-155">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="dbf40-156">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="dbf40-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="dbf40-157">Laukā Nosaukums ierakstiet 'Dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="dbf40-158">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="dbf40-158">Click OK.</span></span>
51. <span data-ttu-id="dbf40-159">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensija: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="dbf40-160">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="dbf40-161">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="dbf40-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="dbf40-162">Laukā Nosaukums ierakstiet 'Kods'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="dbf40-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbf40-163">Click OK.</span></span>
56. <span data-ttu-id="dbf40-164">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="dbf40-165">Laukā Nosaukums ierakstiet 'Vērtība'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="dbf40-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbf40-166">Click OK.</span></span>
59. <span data-ttu-id="dbf40-167">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="dbf40-168">Laukā Nosaukums ierakstiet 'Desc'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="dbf40-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="dbf40-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="dbf40-170">Kartējiet pārskata elementus datu avotiem</span><span class="sxs-lookup"><span data-stu-id="dbf40-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="dbf40-171">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="dbf40-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="dbf40-172">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="dbf40-173">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="dbf40-174">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="dbf40-175">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="dbf40-176">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Desc: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="dbf40-177">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Apraksts: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="dbf40-178">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-178">Click Bind.</span></span>
9. <span data-ttu-id="dbf40-179">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Vērtība: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="dbf40-180">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Kods: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="dbf40-181">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-181">Click Bind.</span></span>
12. <span data-ttu-id="dbf40-182">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Kods: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="dbf40-183">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Nosaukums: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="dbf40-184">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-184">Click Bind.</span></span>
15. <span data-ttu-id="dbf40-185">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="dbf40-186">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensija: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="dbf40-187">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-187">Click Bind.</span></span>
18. <span data-ttu-id="dbf40-188">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Ct: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="dbf40-189">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Kredīts: Reāls'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="dbf40-190">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-190">Click Bind.</span></span>
21. <span data-ttu-id="dbf40-191">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dt: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="dbf40-192">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Debets: Reāls'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="dbf40-193">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-193">Click Bind.</span></span>
24. <span data-ttu-id="dbf40-194">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Valūta: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="dbf40-195">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Valūta: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="dbf40-196">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-196">Click Bind.</span></span>
27. <span data-ttu-id="dbf40-197">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Datums: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="dbf40-198">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Datums: Datums'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="dbf40-199">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-199">Click Bind.</span></span>
30. <span data-ttu-id="dbf40-200">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dokuments: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="dbf40-201">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Dokuments: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="dbf40-202">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-202">Click Bind.</span></span>
33. <span data-ttu-id="dbf40-203">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="dbf40-204">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="dbf40-205">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-205">Click Bind.</span></span>
36. <span data-ttu-id="dbf40-206">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Partija: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="dbf40-207">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Partija: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="dbf40-208">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-208">Click Bind.</span></span>
39. <span data-ttu-id="dbf40-209">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="dbf40-210">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="dbf40-211">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-211">Click Bind.</span></span>
42. <span data-ttu-id="dbf40-212">Kokā atlasiet 'Sakne: XML elements\Uzņēmums: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="dbf40-213">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Uzņēmums: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="dbf40-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="dbf40-214">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-214">Click Bind.</span></span>
45. <span data-ttu-id="dbf40-215">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dbf40-215">Click Save.</span></span>
46. <span data-ttu-id="dbf40-216">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="dbf40-216">Close the page.</span></span>


