---
title: ER finanšu dimensijas, kuras izmanto kā datu avotu (1. daļa. Datu modeļa noformēšana)
description: Tālāk ir paskaidrots kā sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b951c9074c68a9f7592c17e0688498880397b223
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406547"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="8d11a-103">ER finanšu dimensijas, kuras izmanto kā datu avotu (1. daļa. Datu modeļa noformēšana)</span><span class="sxs-lookup"><span data-stu-id="8d11a-103">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d11a-104">Tālāk ir paskaidrots kā sistēmas administrators vai elektroniskā pārskata izstrādātājs var konfigurēt datu modeli Elektroniskie pārskati (ER) izmantošanai finanšu dimensijās, kā datu avotu ER pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="8d11a-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="8d11a-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="8d11a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="8d11a-106">Lai izpildītu tālāk norādītās darbības, vispirms izpildiet procedūras darbības "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu".</span><span class="sxs-lookup"><span data-stu-id="8d11a-106">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="8d11a-107">Izveidot jaunu datu modeli</span><span class="sxs-lookup"><span data-stu-id="8d11a-107">Create a new data model</span></span>
1. <span data-ttu-id="8d11a-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="8d11a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="8d11a-109">Pārliecinieties, vai "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="8d11a-109">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="8d11a-110">ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="8d11a-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="8d11a-111">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="8d11a-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="8d11a-112">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="8d11a-113">Laukā Nosaukums ierakstiet 'Finanšu dimensiju parauga modelis'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="8d11a-114">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="8d11a-114">Click Create configuration.</span></span>
6. <span data-ttu-id="8d11a-115">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="8d11a-115">Click Designer.</span></span>
7. <span data-ttu-id="8d11a-116">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="8d11a-117">Laukā Nosaukums ierakstiet 'Ieraksts'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="8d11a-118">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-118">Click Add.</span></span>
10. <span data-ttu-id="8d11a-119">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="8d11a-120">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="8d11a-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="8d11a-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-121">Click Add.</span></span>
    * <span data-ttu-id="8d11a-122">Pievienosim mūsu modelim jaunu ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-122">We will add to our model a new record list.</span></span> <span data-ttu-id="8d11a-123">Šajā sarakstā tiks atklāti (visiem ER pārskatiem, kas izmanto šo modeli kā datu avotu) atlasīto finanšu dimensiju iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="8d11a-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="8d11a-124">Katra finanšu dimensija tiks parādīta šajā sarakstā kā ieraksts ar atbilstošiem laukiem, kas norāda dimensijas iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="8d11a-125">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="8d11a-126">Laukā Nosaukums ierakstiet 'Dimensiju iestatīšana'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="8d11a-127">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="8d11a-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="8d11a-128">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-128">Click Add.</span></span>
17. <span data-ttu-id="8d11a-129">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="8d11a-130">Laukā Nosaukums ierakstiet 'Kods'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="8d11a-131">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="8d11a-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="8d11a-132">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-132">Click Add.</span></span>
21. <span data-ttu-id="8d11a-133">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="8d11a-134">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="8d11a-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="8d11a-135">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-135">Click Add.</span></span>
24. <span data-ttu-id="8d11a-136">Kokā atlasiet 'Ieraksts'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="8d11a-137">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="8d11a-138">Laukā Nosaukums ierakstiet 'Žurnāls'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="8d11a-139">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="8d11a-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="8d11a-140">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-140">Click Add.</span></span>
29. <span data-ttu-id="8d11a-141">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="8d11a-142">Laukā Nosaukums ierakstiet 'Partija'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="8d11a-143">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="8d11a-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="8d11a-144">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-144">Click Add.</span></span>
33. <span data-ttu-id="8d11a-145">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="8d11a-146">Laukā Nosaukums ierakstiet 'Darbība'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="8d11a-147">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="8d11a-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="8d11a-148">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-148">Click Add.</span></span>
37. <span data-ttu-id="8d11a-149">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="8d11a-150">Laukā Nosaukums ierakstiet 'Datums'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="8d11a-151">Laukā Vienuma tips atlasiet "Date".</span><span class="sxs-lookup"><span data-stu-id="8d11a-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="8d11a-152">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-152">Click Add.</span></span>
41. <span data-ttu-id="8d11a-153">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="8d11a-154">Laukā Nosaukums ierakstiet 'Debets'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="8d11a-155">Laukā Vienuma tips atlasiet "Real".</span><span class="sxs-lookup"><span data-stu-id="8d11a-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="8d11a-156">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-156">Click Add.</span></span>
45. <span data-ttu-id="8d11a-157">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="8d11a-158">Laukā Nosaukums ierakstiet 'Kredīts'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="8d11a-159">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-159">Click Add.</span></span>
48. <span data-ttu-id="8d11a-160">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="8d11a-161">Laukā Nosaukums ierakstiet "Valūta".</span><span class="sxs-lookup"><span data-stu-id="8d11a-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="8d11a-162">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="8d11a-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="8d11a-163">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-163">Click Add.</span></span>
52. <span data-ttu-id="8d11a-164">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="8d11a-165">Laukā Nosaukums ierakstiet 'Dokuments'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="8d11a-166">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-166">Click Add.</span></span>
55. <span data-ttu-id="8d11a-167">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="8d11a-168">Laukā Nosaukums ierakstiet 'Dimensiju dati.</span><span class="sxs-lookup"><span data-stu-id="8d11a-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="8d11a-169">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="8d11a-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="8d11a-170">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-170">Click Add.</span></span>
    * <span data-ttu-id="8d11a-171">Pievienojām mūsu modelim jaunu ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-171">We added to our model a new record list.</span></span> <span data-ttu-id="8d11a-172">Šajā sarakstā tiks atklāti (visiem ER pārskatiem, kas izmanto šo modeli kā datu avotu) atlasīto finanšu dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="8d11a-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="8d11a-173">Katra finanšu dimensija tiks parādīta šajā sarakstā kā ieraksts ar atbilstošiem laukiem, kas norāda dimensijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="8d11a-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="8d11a-174">Dimensijas nosaukums arī tiks iesniegts šajā ierakstā kā lauks, kas jāizmanto atlases nolūkiem, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="8d11a-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="8d11a-175">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="8d11a-176">Laukā Nosaukums ierakstiet 'Kods'.</span><span class="sxs-lookup"><span data-stu-id="8d11a-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="8d11a-177">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="8d11a-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="8d11a-178">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-178">Click Add.</span></span>
63. <span data-ttu-id="8d11a-179">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="8d11a-180">Laukā Nosaukums ierakstiet "Apraksts".</span><span class="sxs-lookup"><span data-stu-id="8d11a-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="8d11a-181">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-181">Click Add.</span></span>
66. <span data-ttu-id="8d11a-182">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="8d11a-183">Laukā Nosaukums ierakstiet "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="8d11a-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="8d11a-184">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8d11a-184">Click Add.</span></span>
69. <span data-ttu-id="8d11a-185">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8d11a-185">Click Save.</span></span>
70. <span data-ttu-id="8d11a-186">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8d11a-186">Close the page.</span></span>

![EP datu modeļa veidotāja lapa](../media/er-financial-dimensions-guides-data-model.png)

