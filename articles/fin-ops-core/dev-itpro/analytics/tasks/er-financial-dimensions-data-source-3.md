---
title: ER finanšu dimensijas, ko izmanto kā datu avotu (3. daļa. Pārskata izkārtošana)
description: Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684791"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="6f508-103">ER finanšu dimensijas, ko izmanto kā datu avotu (3. daļa. Pārskata izkārtošana)</span><span class="sxs-lookup"><span data-stu-id="6f508-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f508-104">Tālāk ir paskaidrots kā lietotājs, kam piešķirta loma sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="6f508-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="6f508-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="6f508-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6f508-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Finanšu dimensijas, ko izmanto kā datu avotu" (2. daļa: Modeļa kartēšana).</span><span class="sxs-lookup"><span data-stu-id="6f508-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="6f508-107">Izveidojiet pārskatu, lai parādītu finanšu dimensijas</span><span class="sxs-lookup"><span data-stu-id="6f508-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="6f508-108">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="6f508-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6f508-109">Koka struktūrā atlasiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="6f508-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6f508-110">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f508-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="6f508-111">Laukā Jauns ievadiet "Formāts pamatojoties uz datu modeli 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="6f508-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="6f508-112">Izmantojiet iepriekš izveidoto modeli kā jaunā pārskata datu avotu.</span><span class="sxs-lookup"><span data-stu-id="6f508-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="6f508-113">Laukā Nosaukums ierakstiet 'Virsgrāmatas žurnāla pārskats'.</span><span class="sxs-lookup"><span data-stu-id="6f508-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="6f508-114">Laukā Datu modeļa definīcija atlasiet Ieraksts.</span><span class="sxs-lookup"><span data-stu-id="6f508-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="6f508-115">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="6f508-115">Click Create configuration.</span></span>
8. <span data-ttu-id="6f508-116">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="6f508-116">Click Designer.</span></span>
9. <span data-ttu-id="6f508-117">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="6f508-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="6f508-118">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="6f508-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="6f508-119">Laukā Nosaukums ierakstiet 'Sakne'.</span><span class="sxs-lookup"><span data-stu-id="6f508-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="6f508-120">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="6f508-120">Click OK.</span></span>
13. <span data-ttu-id="6f508-121">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f508-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="6f508-122">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="6f508-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="6f508-123">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="6f508-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="6f508-124">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="6f508-124">Click OK.</span></span>
17. <span data-ttu-id="6f508-125">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f508-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="6f508-126">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="6f508-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="6f508-127">Laukā Nosaukums ierakstiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="6f508-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="6f508-128">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="6f508-128">Click OK.</span></span>
21. <span data-ttu-id="6f508-129">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="6f508-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="6f508-130">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f508-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="6f508-131">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="6f508-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="6f508-132">Laukā Nosaukums ierakstiet 'Partija'.</span><span class="sxs-lookup"><span data-stu-id="6f508-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="6f508-133">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="6f508-133">Click OK.</span></span>
26. <span data-ttu-id="6f508-134">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f508-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="6f508-135">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="6f508-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="6f508-136">Laukā Nosaukums ierakstiet 'Darbība'.</span><span class="sxs-lookup"><span data-stu-id="6f508-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="6f508-137">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="6f508-137">Click OK.</span></span>
30. <span data-ttu-id="6f508-138">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="6f508-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="6f508-139">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f508-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="6f508-140">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="6f508-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="6f508-141">Laukā Nosaukums ierakstiet 'Dokuments'.</span><span class="sxs-lookup"><span data-stu-id="6f508-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="6f508-142">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f508-142">Click OK.</span></span>
35. <span data-ttu-id="6f508-143">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="6f508-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="6f508-144">Laukā Nosaukums ierakstiet 'Datums'.</span><span class="sxs-lookup"><span data-stu-id="6f508-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="6f508-145">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f508-145">Click OK.</span></span>
38. <span data-ttu-id="6f508-146">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="6f508-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="6f508-147">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="6f508-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="6f508-148">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f508-148">Click OK.</span></span>
41. <span data-ttu-id="6f508-149">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="6f508-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="6f508-150">Laukā Nosaukums ierakstiet 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="6f508-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="6f508-151">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f508-151">Click OK.</span></span>
44. <span data-ttu-id="6f508-152">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="6f508-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="6f508-153">Laukā Nosaukums ierakstiet 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="6f508-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="6f508-154">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f508-154">Click OK.</span></span>
47. <span data-ttu-id="6f508-155">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f508-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="6f508-156">Kokā atlasiet "XML\Elements".</span><span class="sxs-lookup"><span data-stu-id="6f508-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="6f508-157">Laukā Nosaukums ierakstiet 'Dimensijas'.</span><span class="sxs-lookup"><span data-stu-id="6f508-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="6f508-158">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="6f508-158">Click OK.</span></span>
51. <span data-ttu-id="6f508-159">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensija: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="6f508-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="6f508-160">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f508-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="6f508-161">Kokā atlasiet "XML\Atribūts".</span><span class="sxs-lookup"><span data-stu-id="6f508-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="6f508-162">Laukā Nosaukums ierakstiet 'Kods'.</span><span class="sxs-lookup"><span data-stu-id="6f508-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="6f508-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f508-163">Click OK.</span></span>
56. <span data-ttu-id="6f508-164">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="6f508-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="6f508-165">Laukā Nosaukums ierakstiet 'Vērtība'.</span><span class="sxs-lookup"><span data-stu-id="6f508-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="6f508-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f508-166">Click OK.</span></span>
59. <span data-ttu-id="6f508-167">Noklikšķiniet uz Pievienot atribūtu.</span><span class="sxs-lookup"><span data-stu-id="6f508-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="6f508-168">Laukā Nosaukums ierakstiet 'Desc'.</span><span class="sxs-lookup"><span data-stu-id="6f508-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="6f508-169">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="6f508-169">Click OK.</span></span>
<span data-ttu-id="6f508-170">![ER operāciju veidotāja lapa](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="6f508-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="6f508-171">Kartējiet pārskata elementus datu avotiem</span><span class="sxs-lookup"><span data-stu-id="6f508-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="6f508-172">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="6f508-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="6f508-173">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="6f508-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6f508-174">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="6f508-175">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="6f508-176">Kokā izvērsiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="6f508-177">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Desc: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="6f508-178">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Apraksts: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="6f508-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="6f508-179">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-179">Click Bind.</span></span>
9. <span data-ttu-id="6f508-180">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Vērtība: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="6f508-181">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Kods: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="6f508-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="6f508-182">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-182">Click Bind.</span></span>
12. <span data-ttu-id="6f508-183">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensijas: XML elements\Kods: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="6f508-184">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts\Nosaukums: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="6f508-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="6f508-185">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-185">Click Bind.</span></span>
15. <span data-ttu-id="6f508-186">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Darbība: Ierakstu saraksts\Dimensiju dati: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="6f508-187">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dimensija: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="6f508-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="6f508-188">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-188">Click Bind.</span></span>
18. <span data-ttu-id="6f508-189">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Ct: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="6f508-190">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Kredīts: Reāls'.</span><span class="sxs-lookup"><span data-stu-id="6f508-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="6f508-191">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-191">Click Bind.</span></span>
21. <span data-ttu-id="6f508-192">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dt: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="6f508-193">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Debets: Reāls'.</span><span class="sxs-lookup"><span data-stu-id="6f508-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="6f508-194">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-194">Click Bind.</span></span>
24. <span data-ttu-id="6f508-195">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Valūta: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="6f508-196">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Valūta: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="6f508-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="6f508-197">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-197">Click Bind.</span></span>
27. <span data-ttu-id="6f508-198">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Datums: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="6f508-199">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Datums: Datums'.</span><span class="sxs-lookup"><span data-stu-id="6f508-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="6f508-200">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-200">Click Bind.</span></span>
30. <span data-ttu-id="6f508-201">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements\Dokuments: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="6f508-202">Koka atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Dokuments: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="6f508-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="6f508-203">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-203">Click Bind.</span></span>
33. <span data-ttu-id="6f508-204">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Darbība: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="6f508-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="6f508-205">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Dimensiju iestatīšana: Ierakstu saraksts\Darbība: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="6f508-206">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-206">Click Bind.</span></span>
36. <span data-ttu-id="6f508-207">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements\Partija: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="6f508-208">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts\Partija: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="6f508-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="6f508-209">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-209">Click Bind.</span></span>
39. <span data-ttu-id="6f508-210">Kokā atlasiet 'Sakne: XML elements\Žurnāls: XML elements'.</span><span class="sxs-lookup"><span data-stu-id="6f508-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="6f508-211">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Žurnāls: Ierakstu saraksts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="6f508-212">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-212">Click Bind.</span></span>
42. <span data-ttu-id="6f508-213">Kokā atlasiet 'Sakne: XML elements\Uzņēmums: XML atribūts'.</span><span class="sxs-lookup"><span data-stu-id="6f508-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="6f508-214">Kokā atlasiet 'modelis: datu modelis Finanšu dimensiju parauga modelis\Uzņēmums: Virkne'.</span><span class="sxs-lookup"><span data-stu-id="6f508-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="6f508-215">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f508-215">Click Bind.</span></span>
45. <span data-ttu-id="6f508-216">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6f508-216">Click Save.</span></span>
46. <span data-ttu-id="6f508-217">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6f508-217">Close the page.</span></span>
<span data-ttu-id="6f508-218">![ER operāciju veidotāja lapa](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="6f508-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

