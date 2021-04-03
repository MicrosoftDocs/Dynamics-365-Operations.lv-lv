---
title: ER finanšu dimensijas, kuras izmanto kā datu avotu (1. daļa. Datu modeļa noformēšana)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) modeli, lai finanšu dimensijas izmantotu kā datu avotu ER pārskatiem. (1. daļa)
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570196"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="386c0-104">ER finanšu dimensijas, kuras izmanto kā datu avotu (1. daļa. Datu modeļa noformēšana)</span><span class="sxs-lookup"><span data-stu-id="386c0-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="386c0-105">Tālāk ir paskaidrots kā sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="386c0-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="386c0-106">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="386c0-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="386c0-107">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet procedūras darbības "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".</span><span class="sxs-lookup"><span data-stu-id="386c0-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="386c0-108">Izveidot jaunu datu modeli</span><span class="sxs-lookup"><span data-stu-id="386c0-108">Create a new data model</span></span>
1. <span data-ttu-id="386c0-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="386c0-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="386c0-110">Pārliecinieties, vai "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="386c0-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="386c0-111">ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="386c0-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="386c0-112">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="386c0-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="386c0-113">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="386c0-114">Laukā Nosaukums ierakstiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="386c0-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="386c0-115">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="386c0-115">Click Create configuration.</span></span>
6. <span data-ttu-id="386c0-116">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="386c0-116">Click Designer.</span></span>
7. <span data-ttu-id="386c0-117">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="386c0-118">Laukā Nosaukums ierakstiet 'Ieraksts'.</span><span class="sxs-lookup"><span data-stu-id="386c0-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="386c0-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-119">Click Add.</span></span>
10. <span data-ttu-id="386c0-120">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="386c0-121">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="386c0-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="386c0-122">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-122">Click Add.</span></span>
    * <span data-ttu-id="386c0-123">Pievienosim mūsu modelim jaunu ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="386c0-123">We will add to our model a new record list.</span></span> <span data-ttu-id="386c0-124">Šajā sarakstā tiks atklāti (visiem ER pārskatiem, kas izmanto šo modeli kā datu avotu) atlasīto finanšu dimensiju iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="386c0-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="386c0-125">Katra finanšu dimensija tiks parādīta šajā sarakstā kā ieraksts ar atbilstošiem laukiem, kas norāda dimensijas iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="386c0-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="386c0-126">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="386c0-127">Laukā Nosaukums ierakstiet 'Dimensiju iestatīšana'.</span><span class="sxs-lookup"><span data-stu-id="386c0-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="386c0-128">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="386c0-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="386c0-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-129">Click Add.</span></span>
17. <span data-ttu-id="386c0-130">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="386c0-131">Laukā Nosaukums ierakstiet 'Kods'.</span><span class="sxs-lookup"><span data-stu-id="386c0-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="386c0-132">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="386c0-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="386c0-133">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-133">Click Add.</span></span>
21. <span data-ttu-id="386c0-134">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="386c0-135">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="386c0-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="386c0-136">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-136">Click Add.</span></span>
24. <span data-ttu-id="386c0-137">Kokā atlasiet 'Ieraksts'.</span><span class="sxs-lookup"><span data-stu-id="386c0-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="386c0-138">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="386c0-139">Laukā Nosaukums ierakstiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="386c0-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="386c0-140">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="386c0-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="386c0-141">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-141">Click Add.</span></span>
29. <span data-ttu-id="386c0-142">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="386c0-143">Laukā Nosaukums ierakstiet 'Partija'.</span><span class="sxs-lookup"><span data-stu-id="386c0-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="386c0-144">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="386c0-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="386c0-145">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-145">Click Add.</span></span>
33. <span data-ttu-id="386c0-146">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="386c0-147">Laukā Nosaukums ierakstiet 'Darbība'.</span><span class="sxs-lookup"><span data-stu-id="386c0-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="386c0-148">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="386c0-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="386c0-149">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-149">Click Add.</span></span>
37. <span data-ttu-id="386c0-150">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="386c0-151">Laukā Nosaukums ierakstiet 'Datums'.</span><span class="sxs-lookup"><span data-stu-id="386c0-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="386c0-152">Laukā Vienuma tips atlasiet "Date".</span><span class="sxs-lookup"><span data-stu-id="386c0-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="386c0-153">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-153">Click Add.</span></span>
41. <span data-ttu-id="386c0-154">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="386c0-155">Laukā Nosaukums ierakstiet 'Debets'.</span><span class="sxs-lookup"><span data-stu-id="386c0-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="386c0-156">Laukā Vienuma tips atlasiet "Real".</span><span class="sxs-lookup"><span data-stu-id="386c0-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="386c0-157">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-157">Click Add.</span></span>
45. <span data-ttu-id="386c0-158">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="386c0-159">Laukā Nosaukums ierakstiet 'Kredīts'.</span><span class="sxs-lookup"><span data-stu-id="386c0-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="386c0-160">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-160">Click Add.</span></span>
48. <span data-ttu-id="386c0-161">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="386c0-162">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="386c0-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="386c0-163">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="386c0-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="386c0-164">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-164">Click Add.</span></span>
52. <span data-ttu-id="386c0-165">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="386c0-166">Laukā Nosaukums ierakstiet 'Dokuments'.</span><span class="sxs-lookup"><span data-stu-id="386c0-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="386c0-167">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-167">Click Add.</span></span>
55. <span data-ttu-id="386c0-168">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="386c0-169">Laukā Nosaukums ierakstiet 'Dimensiju dati.</span><span class="sxs-lookup"><span data-stu-id="386c0-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="386c0-170">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="386c0-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="386c0-171">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-171">Click Add.</span></span>
    * <span data-ttu-id="386c0-172">Pievienojām mūsu modelim jaunu ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="386c0-172">We added to our model a new record list.</span></span> <span data-ttu-id="386c0-173">Šajā sarakstā tiks atklāti (visiem ER pārskatiem, kas izmanto šo modeli kā datu avotu) atlasīto finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="386c0-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="386c0-174">Katra finanšu dimensija tiks parādīta šajā sarakstā kā ieraksts ar atbilstošiem laukiem, kas norāda dimensijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="386c0-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="386c0-175">Dimensijas nosaukums arī tiks iesniegts šajā ierakstā kā lauks, kas jāizmanto atlases nolūkiem, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="386c0-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="386c0-176">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="386c0-177">Laukā Nosaukums ierakstiet 'Kods'.</span><span class="sxs-lookup"><span data-stu-id="386c0-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="386c0-178">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="386c0-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="386c0-179">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-179">Click Add.</span></span>
63. <span data-ttu-id="386c0-180">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="386c0-181">Laukā Nosaukums ierakstiet "Apraksts".</span><span class="sxs-lookup"><span data-stu-id="386c0-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="386c0-182">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-182">Click Add.</span></span>
66. <span data-ttu-id="386c0-183">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="386c0-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="386c0-184">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="386c0-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="386c0-185">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="386c0-185">Click Add.</span></span>
69. <span data-ttu-id="386c0-186">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="386c0-186">Click Save.</span></span>
70. <span data-ttu-id="386c0-187">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="386c0-187">Close the page.</span></span>

![EP datu modeļa veidotāja lapa](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]