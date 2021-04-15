---
title: ER finanšu dimensijas, kuras izmanto kā datu avotu (1. daļa. Datu modeļa noformēšana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) modeli, lai finanšu dimensijas izmantotu kā datu avotu ER pārskatiem. (1. daļa)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92b44532dfae70f03d6686ca1d2f8b6f74345ee6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752464"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="72cb2-104">ER finanšu dimensijas, kuras izmanto kā datu avotu (1. daļa. Datu modeļa noformēšana)</span><span class="sxs-lookup"><span data-stu-id="72cb2-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72cb2-105">Tālāk ir paskaidrots kā sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="72cb2-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="72cb2-106">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="72cb2-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="72cb2-107">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet procedūras darbības "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".</span><span class="sxs-lookup"><span data-stu-id="72cb2-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="72cb2-108">Izveidot jaunu datu modeli</span><span class="sxs-lookup"><span data-stu-id="72cb2-108">Create a new data model</span></span>
1. <span data-ttu-id="72cb2-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="72cb2-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="72cb2-110">Pārliecinieties, vai "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="72cb2-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="72cb2-111">ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="72cb2-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="72cb2-112">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="72cb2-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="72cb2-113">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="72cb2-114">Laukā Nosaukums ierakstiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="72cb2-115">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="72cb2-115">Click Create configuration.</span></span>
6. <span data-ttu-id="72cb2-116">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="72cb2-116">Click Designer.</span></span>
7. <span data-ttu-id="72cb2-117">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="72cb2-118">Laukā Nosaukums ierakstiet 'Ieraksts'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="72cb2-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-119">Click Add.</span></span>
10. <span data-ttu-id="72cb2-120">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="72cb2-121">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="72cb2-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="72cb2-122">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-122">Click Add.</span></span>
    * <span data-ttu-id="72cb2-123">Pievienosim mūsu modelim jaunu ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-123">We will add to our model a new record list.</span></span> <span data-ttu-id="72cb2-124">Šajā sarakstā tiks atklāti (visiem ER pārskatiem, kas izmanto šo modeli kā datu avotu) atlasīto finanšu dimensiju iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="72cb2-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="72cb2-125">Katra finanšu dimensija tiks parādīta šajā sarakstā kā ieraksts ar atbilstošiem laukiem, kas norāda dimensijas iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="72cb2-126">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="72cb2-127">Laukā Nosaukums ierakstiet 'Dimensiju iestatīšana'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="72cb2-128">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="72cb2-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="72cb2-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-129">Click Add.</span></span>
17. <span data-ttu-id="72cb2-130">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="72cb2-131">Laukā Nosaukums ierakstiet 'Kods'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="72cb2-132">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="72cb2-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="72cb2-133">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-133">Click Add.</span></span>
21. <span data-ttu-id="72cb2-134">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="72cb2-135">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="72cb2-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="72cb2-136">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-136">Click Add.</span></span>
24. <span data-ttu-id="72cb2-137">Kokā atlasiet 'Ieraksts'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="72cb2-138">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="72cb2-139">Laukā Nosaukums ierakstiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="72cb2-140">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="72cb2-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="72cb2-141">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-141">Click Add.</span></span>
29. <span data-ttu-id="72cb2-142">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="72cb2-143">Laukā Nosaukums ierakstiet 'Partija'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="72cb2-144">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="72cb2-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="72cb2-145">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-145">Click Add.</span></span>
33. <span data-ttu-id="72cb2-146">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="72cb2-147">Laukā Nosaukums ierakstiet 'Darbība'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="72cb2-148">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="72cb2-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="72cb2-149">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-149">Click Add.</span></span>
37. <span data-ttu-id="72cb2-150">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="72cb2-151">Laukā Nosaukums ierakstiet 'Datums'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="72cb2-152">Laukā Vienuma tips atlasiet "Date".</span><span class="sxs-lookup"><span data-stu-id="72cb2-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="72cb2-153">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-153">Click Add.</span></span>
41. <span data-ttu-id="72cb2-154">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="72cb2-155">Laukā Nosaukums ierakstiet 'Debets'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="72cb2-156">Laukā Vienuma tips atlasiet "Real".</span><span class="sxs-lookup"><span data-stu-id="72cb2-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="72cb2-157">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-157">Click Add.</span></span>
45. <span data-ttu-id="72cb2-158">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="72cb2-159">Laukā Nosaukums ierakstiet 'Kredīts'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="72cb2-160">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-160">Click Add.</span></span>
48. <span data-ttu-id="72cb2-161">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="72cb2-162">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="72cb2-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="72cb2-163">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="72cb2-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="72cb2-164">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-164">Click Add.</span></span>
52. <span data-ttu-id="72cb2-165">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="72cb2-166">Laukā Nosaukums ierakstiet 'Dokuments'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="72cb2-167">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-167">Click Add.</span></span>
55. <span data-ttu-id="72cb2-168">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="72cb2-169">Laukā Nosaukums ierakstiet 'Dimensiju dati.</span><span class="sxs-lookup"><span data-stu-id="72cb2-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="72cb2-170">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="72cb2-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="72cb2-171">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-171">Click Add.</span></span>
    * <span data-ttu-id="72cb2-172">Pievienojām mūsu modelim jaunu ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-172">We added to our model a new record list.</span></span> <span data-ttu-id="72cb2-173">Šajā sarakstā tiks atklāti (visiem ER pārskatiem, kas izmanto šo modeli kā datu avotu) atlasīto finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="72cb2-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="72cb2-174">Katra finanšu dimensija tiks parādīta šajā sarakstā kā ieraksts ar atbilstošiem laukiem, kas norāda dimensijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="72cb2-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="72cb2-175">Dimensijas nosaukums arī tiks iesniegts šajā ierakstā kā lauks, kas jāizmanto atlases nolūkiem, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="72cb2-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="72cb2-176">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="72cb2-177">Laukā Nosaukums ierakstiet 'Kods'.</span><span class="sxs-lookup"><span data-stu-id="72cb2-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="72cb2-178">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="72cb2-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="72cb2-179">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-179">Click Add.</span></span>
63. <span data-ttu-id="72cb2-180">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="72cb2-181">Laukā Nosaukums ierakstiet "Apraksts".</span><span class="sxs-lookup"><span data-stu-id="72cb2-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="72cb2-182">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-182">Click Add.</span></span>
66. <span data-ttu-id="72cb2-183">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="72cb2-184">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="72cb2-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="72cb2-185">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cb2-185">Click Add.</span></span>
69. <span data-ttu-id="72cb2-186">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="72cb2-186">Click Save.</span></span>
70. <span data-ttu-id="72cb2-187">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="72cb2-187">Close the page.</span></span>

![EP datu modeļa veidotāja lapa](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]