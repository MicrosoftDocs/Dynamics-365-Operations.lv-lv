---
title: ER finanšu dimensijas, ko izmanto kā datu avotu (3. daļa. Pārskata izkārtošana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) modeli, lai finanšu dimensijas izmantotu kā datu avotu ER pārskatiem. (3. daļa)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a3b9a8b5775d2001f3384480e2f9593f2dfa8b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752416"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="50bb2-104">ER finanšu dimensijas, ko izmanto kā datu avotu (3. daļa. Pārskata izkārtošana)</span><span class="sxs-lookup"><span data-stu-id="50bb2-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50bb2-105">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="50bb2-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="50bb2-106">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="50bb2-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="50bb2-107">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (2. daļa: Modeļa kartēšana).</span><span class="sxs-lookup"><span data-stu-id="50bb2-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="50bb2-108">Izveidojiet pārskatu, lai parādītu finanšu dimensijas</span><span class="sxs-lookup"><span data-stu-id="50bb2-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="50bb2-109">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="50bb2-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="50bb2-110">Koka struktūrā atlasiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="50bb2-111">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="50bb2-112">Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="50bb2-113">Izmantojiet iepriekš izveidoto modeli kā jaunā pārskata datu avotu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="50bb2-114">Laukā Nosaukums ierakstiet 'Virsgrāmatas žurnāla pārskats'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="50bb2-115">Laukā Datu modeļa definīcija atlasiet Ieraksts.</span><span class="sxs-lookup"><span data-stu-id="50bb2-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="50bb2-116">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="50bb2-116">Click Create configuration.</span></span>
8. <span data-ttu-id="50bb2-117">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="50bb2-117">Click Designer.</span></span>
9. <span data-ttu-id="50bb2-118">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="50bb2-119">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="50bb2-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="50bb2-120">Laukā Nosaukums ierakstiet 'Sakne'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="50bb2-121">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50bb2-121">Click OK.</span></span>
13. <span data-ttu-id="50bb2-122">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="50bb2-123">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="50bb2-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="50bb2-124">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="50bb2-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="50bb2-125">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50bb2-125">Click OK.</span></span>
17. <span data-ttu-id="50bb2-126">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="50bb2-127">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="50bb2-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="50bb2-128">Laukā Nosaukums ierakstiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="50bb2-129">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50bb2-129">Click OK.</span></span>
21. <span data-ttu-id="50bb2-130">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="50bb2-131">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="50bb2-132">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="50bb2-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="50bb2-133">Laukā Nosaukums ierakstiet 'Partija'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="50bb2-134">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50bb2-134">Click OK.</span></span>
26. <span data-ttu-id="50bb2-135">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="50bb2-136">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="50bb2-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="50bb2-137">Laukā Nosaukums ierakstiet 'Darbība'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="50bb2-138">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50bb2-138">Click OK.</span></span>
30. <span data-ttu-id="50bb2-139">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="50bb2-140">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="50bb2-141">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="50bb2-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="50bb2-142">Laukā Nosaukums ierakstiet 'Dokuments'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="50bb2-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="50bb2-143">Click OK.</span></span>
35. <span data-ttu-id="50bb2-144">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="50bb2-145">Laukā Nosaukums ierakstiet 'Datums'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="50bb2-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="50bb2-146">Click OK.</span></span>
38. <span data-ttu-id="50bb2-147">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="50bb2-148">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="50bb2-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="50bb2-149">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="50bb2-149">Click OK.</span></span>
41. <span data-ttu-id="50bb2-150">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="50bb2-151">Laukā Nosaukums ierakstiet 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="50bb2-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="50bb2-152">Click OK.</span></span>
44. <span data-ttu-id="50bb2-153">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="50bb2-154">Laukā Nosaukums ierakstiet 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="50bb2-155">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="50bb2-155">Click OK.</span></span>
47. <span data-ttu-id="50bb2-156">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="50bb2-157">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="50bb2-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="50bb2-158">Laukā Nosaukums ierakstiet 'Dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="50bb2-159">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50bb2-159">Click OK.</span></span>
51. <span data-ttu-id="50bb2-160">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensija: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="50bb2-161">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="50bb2-162">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="50bb2-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="50bb2-163">Laukā Nosaukums ierakstiet 'Kods'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="50bb2-164">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="50bb2-164">Click OK.</span></span>
56. <span data-ttu-id="50bb2-165">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="50bb2-166">Laukā Nosaukums ierakstiet 'Vērtība'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="50bb2-167">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="50bb2-167">Click OK.</span></span>
59. <span data-ttu-id="50bb2-168">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="50bb2-169">Laukā Nosaukums ierakstiet 'Desc'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="50bb2-170">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50bb2-170">Click OK.</span></span>
<span data-ttu-id="50bb2-171">![ER operāciju veidotāja lapa](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="50bb2-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="50bb2-172">Kartējiet pārskata elementus datu avotiem</span><span class="sxs-lookup"><span data-stu-id="50bb2-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="50bb2-173">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="50bb2-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="50bb2-174">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="50bb2-175">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="50bb2-176">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="50bb2-177">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="50bb2-178">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Desc: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="50bb2-179">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Apraksts: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="50bb2-180">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-180">Click Bind.</span></span>
9. <span data-ttu-id="50bb2-181">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Vērtība: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="50bb2-182">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Kods: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="50bb2-183">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-183">Click Bind.</span></span>
12. <span data-ttu-id="50bb2-184">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Kods: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="50bb2-185">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Nosaukums: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="50bb2-186">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-186">Click Bind.</span></span>
15. <span data-ttu-id="50bb2-187">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="50bb2-188">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensija: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="50bb2-189">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-189">Click Bind.</span></span>
18. <span data-ttu-id="50bb2-190">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Ct: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="50bb2-191">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Kredīts: Reāls'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="50bb2-192">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-192">Click Bind.</span></span>
21. <span data-ttu-id="50bb2-193">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dt: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="50bb2-194">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Debets: Reāls'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="50bb2-195">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-195">Click Bind.</span></span>
24. <span data-ttu-id="50bb2-196">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Valūta: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="50bb2-197">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Valūta: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="50bb2-198">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-198">Click Bind.</span></span>
27. <span data-ttu-id="50bb2-199">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Datums: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="50bb2-200">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Datums: Datums'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="50bb2-201">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-201">Click Bind.</span></span>
30. <span data-ttu-id="50bb2-202">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dokuments: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="50bb2-203">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Dokuments: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="50bb2-204">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-204">Click Bind.</span></span>
33. <span data-ttu-id="50bb2-205">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="50bb2-206">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="50bb2-207">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-207">Click Bind.</span></span>
36. <span data-ttu-id="50bb2-208">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Partija: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="50bb2-209">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Partija: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="50bb2-210">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-210">Click Bind.</span></span>
39. <span data-ttu-id="50bb2-211">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="50bb2-212">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="50bb2-213">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-213">Click Bind.</span></span>
42. <span data-ttu-id="50bb2-214">Kokā atlasiet 'Sakne: XML elements\Uzņēmums: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="50bb2-215">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Uzņēmums: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="50bb2-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="50bb2-216">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-216">Click Bind.</span></span>
45. <span data-ttu-id="50bb2-217">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="50bb2-217">Click Save.</span></span>
46. <span data-ttu-id="50bb2-218">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="50bb2-218">Close the page.</span></span>
<span data-ttu-id="50bb2-219">![ER operāciju veidotāja lapa](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="50bb2-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]