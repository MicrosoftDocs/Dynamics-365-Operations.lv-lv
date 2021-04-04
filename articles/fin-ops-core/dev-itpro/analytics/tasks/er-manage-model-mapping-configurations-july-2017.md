---
title: Elektronisko pārskatu modeļa kartēšanas pārvaldība atsevišķās elektronisko pārskatu konfigurācijās
description: Šajā tēmā ir aprakstīts, kā pārvaldīt elektronisko pārskatu (Electronic reporting — ER) modeļu kartējumus atsevišķas ER konfigurācijās.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdd6804c33cc153974229c60b64c3bd76426241a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569417"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="ce264-103">ER modeļa kartēšanas pārvaldība atsevišķās ER konfigurācijās</span><span class="sxs-lookup"><span data-stu-id="ce264-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce264-104">Turpmāk uzskaitītajos posmos paskaidrots, kā lietotājs, kurš piešķirts sistēmas administratoram vai elektronisko ziņojumu izstrādātāja lomai, var pārvaldīt elektronisko ziņojumu (ER) modeļu veidošanu atsevišķās ER konfigurācijās.</span><span class="sxs-lookup"><span data-stu-id="ce264-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="ce264-105">Šajā uzdevumu ceļvedis jūs izveidosiet nepieciešamās ER konfigurācijas parauga uzņēmumam Litware, Inc. Lai izpildītu šīs uzskaitītajos posmos darbības, vispirms izpildiet uzskaitītajos posmos "ER: Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".</span><span class="sxs-lookup"><span data-stu-id="ce264-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="ce264-106">Jo ER konfigurācijas ir kopīgotas starp uzņēmumiem, var aizpildīt rokasgrāmatas uzdevumu, izmantojot uzņēmuma datu kopas pēc savas izvēles.</span><span class="sxs-lookup"><span data-stu-id="ce264-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="ce264-107">Šī uzdevuma ceļveža funkcionalitāte ir pieejama tad, ja esat instalējis kādu no šiem labojumfailiem: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 versijai Dynamics AX 7.0 vai https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 versijai Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="ce264-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="ce264-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="ce264-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="ce264-109">Pārbaudiet, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="ce264-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="ce264-110">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas uzdevuma ceļvedī “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.</span><span class="sxs-lookup"><span data-stu-id="ce264-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="ce264-111">Pievienot jaunu ER modeļa konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="ce264-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="ce264-112">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="ce264-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="ce264-113">Pievienojiet jaunu modeļa konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="ce264-113">Add a new model configuration.</span></span> <span data-ttu-id="ce264-114">Nosaukumam jābūt unikālam konfigurāciju kokā.</span><span class="sxs-lookup"><span data-stu-id="ce264-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="ce264-115">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ce264-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="ce264-116">Laukā Nosaukums ierakstiet “Parauga datu modelis”.</span><span class="sxs-lookup"><span data-stu-id="ce264-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="ce264-117">Parauga datu modelis</span><span class="sxs-lookup"><span data-stu-id="ce264-117">Sample data model</span></span>  
4. <span data-ttu-id="ce264-118">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="ce264-118">Click Create configuration.</span></span>
5. <span data-ttu-id="ce264-119">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="ce264-119">Click Designer.</span></span>
6. <span data-ttu-id="ce264-120">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ce264-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="ce264-121">Laukā Nosaukums ierakstiet 'Sakne'.</span><span class="sxs-lookup"><span data-stu-id="ce264-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="ce264-122">Sakne</span><span class="sxs-lookup"><span data-stu-id="ce264-122">Root</span></span>  
8. <span data-ttu-id="ce264-123">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ce264-123">Click Add.</span></span>
9. <span data-ttu-id="ce264-124">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ce264-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="ce264-125">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="ce264-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="ce264-126">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="ce264-126">Company</span></span>  
11. <span data-ttu-id="ce264-127">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ce264-127">Click Add.</span></span>
12. <span data-ttu-id="ce264-128">Ievadiet tekstu, juridiska persona vai uzņēmums, kurā lietotājs reģistrējies izpildes laikā aprakstu laukā Apraksts.</span><span class="sxs-lookup"><span data-stu-id="ce264-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="ce264-129">Tās juridiskās persona vai uzņēmuma apraksts, kurā lietotājs ir pieteicies izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="ce264-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="ce264-130">Noklikšķiniet uz Saknes atsauce.</span><span class="sxs-lookup"><span data-stu-id="ce264-130">Click Root reference.</span></span>
14. <span data-ttu-id="ce264-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ce264-131">Click OK.</span></span>
15. <span data-ttu-id="ce264-132">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ce264-132">Click Save.</span></span>
16. <span data-ttu-id="ce264-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ce264-133">Close the page.</span></span>
17. <span data-ttu-id="ce264-134">Noklikšķiniet uz Mainīt statusu.</span><span class="sxs-lookup"><span data-stu-id="ce264-134">Click Change status.</span></span>
18. <span data-ttu-id="ce264-135">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="ce264-135">Click Complete.</span></span>
19. <span data-ttu-id="ce264-136">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="ce264-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="ce264-137">Pievienot jaunu ER datu modeļa kartējuma konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="ce264-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="ce264-138">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ce264-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="ce264-139">Laukā Jauns ievadiet "Model Mapping based on data model Sample data model".</span><span class="sxs-lookup"><span data-stu-id="ce264-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="ce264-140">Laukā Nosaukums ierakstiet "Sample mapping".</span><span class="sxs-lookup"><span data-stu-id="ce264-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="ce264-141">Kartējuma paraugs</span><span class="sxs-lookup"><span data-stu-id="ce264-141">Sample mapping</span></span>  
4. <span data-ttu-id="ce264-142">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="ce264-142">Click Create configuration.</span></span>
5. <span data-ttu-id="ce264-143">Izvērsiet priekšnoteikumu sadaļu.</span><span class="sxs-lookup"><span data-stu-id="ce264-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="ce264-144">Ir automātiski pievienota grupa “Ieviešanas priekšnoteikumi”.</span><span class="sxs-lookup"><span data-stu-id="ce264-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="ce264-145">Grupa satur priekšnoteikumu komponentu, kas attiecas uz pamata datu modeļa konfigurāciju un ir atzīmēts kā Ieviešana.</span><span class="sxs-lookup"><span data-stu-id="ce264-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="ce264-146">Tas nozīmē, ka šī parauga kartējuma modeļa kartēšanas konfigurācija tiek uzskatīta par datu modeļa Parauga datu modelis ieviešanu.</span><span class="sxs-lookup"><span data-stu-id="ce264-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="ce264-147">Tāpēc šis komponents liks ER lejupielādēt modeļa kartējuma konfigurāciju Kartējuma paraugs no ER repozitorija, kad tiks lejupielādēta modeļa konfigurācija Parauga datu modelis.</span><span class="sxs-lookup"><span data-stu-id="ce264-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="ce264-148">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="ce264-148">Click Designer.</span></span>
    * <span data-ttu-id="ce264-149">Izveidotā modeļa kartējuma konfigurācija satur jaunu tukšu kartējumu ar tādu pašu nosaukumu kā izveidotajai konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="ce264-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="ce264-150">Gadījumā, kad atlasītā pamata modeļa konfigurācija ietver modeļa kartējumus, tie tiks kopēti uz jaunu modeļa kartēšanas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="ce264-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="ce264-151">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="ce264-151">Click Designer.</span></span>
8. <span data-ttu-id="ce264-152">Kokā atlasiet 'Dynamics 365 for Operations\Tabula'.</span><span class="sxs-lookup"><span data-stu-id="ce264-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="ce264-153">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="ce264-153">Click Add root.</span></span>
10. <span data-ttu-id="ce264-154">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="ce264-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="ce264-155">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="ce264-155">Company</span></span>  
11. <span data-ttu-id="ce264-156">Laukā Tabula ierakstiet "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="ce264-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="ce264-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="ce264-157">CompanyInfo</span></span>  
12. <span data-ttu-id="ce264-158">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ce264-158">Click OK.</span></span>
13. <span data-ttu-id="ce264-159">Kokā izvērsiet elementu “Uzņēmums”.</span><span class="sxs-lookup"><span data-stu-id="ce264-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="ce264-160">Kokā izvērsiet 'Company\find()'.</span><span class="sxs-lookup"><span data-stu-id="ce264-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="ce264-161">Kokā atlasiet 'Company\find()\Name'.</span><span class="sxs-lookup"><span data-stu-id="ce264-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="ce264-162">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="ce264-162">Click Bind.</span></span>
17. <span data-ttu-id="ce264-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ce264-163">Click Save.</span></span>
18. <span data-ttu-id="ce264-164">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ce264-164">Close the page.</span></span>
19. <span data-ttu-id="ce264-165">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ce264-165">Close the page.</span></span>
20. <span data-ttu-id="ce264-166">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="ce264-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="ce264-167">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="ce264-167">Click User parameters.</span></span>
22. <span data-ttu-id="ce264-168">Laukā Palaist iestatījumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ce264-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="ce264-169">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ce264-169">Click OK.</span></span>
24. <span data-ttu-id="ce264-170">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="ce264-170">Click Edit.</span></span>
25. <span data-ttu-id="ce264-171">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ce264-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="ce264-172">Jaunas ER formāta konfigurācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="ce264-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="ce264-173">Kokā atlasiet "Sample data model".</span><span class="sxs-lookup"><span data-stu-id="ce264-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="ce264-174">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ce264-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="ce264-175">Laukā Jauns ievadiet "Format based on data model Sample data model".</span><span class="sxs-lookup"><span data-stu-id="ce264-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="ce264-176">Laukā Nosaukums ierakstiet "Sample format".</span><span class="sxs-lookup"><span data-stu-id="ce264-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="ce264-177">Parauga formāts</span><span class="sxs-lookup"><span data-stu-id="ce264-177">Sample format</span></span>  
5. <span data-ttu-id="ce264-178">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="ce264-178">Click Create configuration.</span></span>
6. <span data-ttu-id="ce264-179">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="ce264-179">Click Designer.</span></span>
7. <span data-ttu-id="ce264-180">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="ce264-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="ce264-181">Kokā atlasiet elementu “Teksts\Virkne”.</span><span class="sxs-lookup"><span data-stu-id="ce264-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="ce264-182">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ce264-182">Click OK.</span></span>
10. <span data-ttu-id="ce264-183">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="ce264-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="ce264-184">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="ce264-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="ce264-185">Kokā atlasiet 'model\Company'.</span><span class="sxs-lookup"><span data-stu-id="ce264-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="ce264-186">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="ce264-186">Click Bind.</span></span>
14. <span data-ttu-id="ce264-187">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ce264-187">Click Save.</span></span>
15. <span data-ttu-id="ce264-188">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ce264-188">Close the page.</span></span>
    * <span data-ttu-id="ce264-189">Palaist melnraksta versiju izveides formāts testēšanas nolūkos.</span><span class="sxs-lookup"><span data-stu-id="ce264-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="ce264-190">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="ce264-190">Click Run.</span></span>
    * <span data-ttu-id="ce264-191">Kopsavilkuma cilnē Versijas noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="ce264-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="ce264-192">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ce264-192">Click OK.</span></span>
    * <span data-ttu-id="ce264-193">Pārskatiet izvadi, kas norādīts, kurā nav pieteicies lietotājs, kurš darbojas šī formāta konfigurāciju uzņēmuma nosaukums.</span><span class="sxs-lookup"><span data-stu-id="ce264-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="ce264-194">Izveidotā modeļa kartēšanas konfigurācijā tiek izmantota šī formāta konfigurācija, jo ir pieejama tikai vienu konfigurācija, kas satur nepieciešamā modeļa kartējumus.</span><span class="sxs-lookup"><span data-stu-id="ce264-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="ce264-195">Alternatīvas ER modeļa kartējuma konfigurācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="ce264-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="ce264-196">Kokā atlasiet "Sample data model".</span><span class="sxs-lookup"><span data-stu-id="ce264-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="ce264-197">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ce264-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="ce264-198">Laukā Jauns ievadiet "Model Mapping based on data model Sample data model".</span><span class="sxs-lookup"><span data-stu-id="ce264-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="ce264-199">Laukā Nosaukums ierakstiet "Sample mapping (alternative)".</span><span class="sxs-lookup"><span data-stu-id="ce264-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="ce264-200">Kartējuma paraugs (alternatīva)</span><span class="sxs-lookup"><span data-stu-id="ce264-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="ce264-201">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="ce264-201">Click Create configuration.</span></span>
6. <span data-ttu-id="ce264-202">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="ce264-202">Click Designer.</span></span>
7. <span data-ttu-id="ce264-203">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="ce264-203">Click Designer.</span></span>
8. <span data-ttu-id="ce264-204">Kokā atlasiet 'Dynamics 365 for Operations\Tabula'.</span><span class="sxs-lookup"><span data-stu-id="ce264-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="ce264-205">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="ce264-205">Click Add root.</span></span>
10. <span data-ttu-id="ce264-206">Laukā Nosaukums ierakstiet "Uzņēmums".</span><span class="sxs-lookup"><span data-stu-id="ce264-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="ce264-207">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="ce264-207">Company</span></span>  
11. <span data-ttu-id="ce264-208">Laukā Tabula ierakstiet "CompanyInfo".</span><span class="sxs-lookup"><span data-stu-id="ce264-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="ce264-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="ce264-209">CompanyInfo</span></span>  
12. <span data-ttu-id="ce264-210">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ce264-210">Click OK.</span></span>
13. <span data-ttu-id="ce264-211">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="ce264-211">Click Edit.</span></span>
14. <span data-ttu-id="ce264-212">Kokā atlasiet “Virkne\CONCATENATE”.</span><span class="sxs-lookup"><span data-stu-id="ce264-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="ce264-213">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="ce264-213">Click Add function.</span></span>
16. <span data-ttu-id="ce264-214">Kokā izvērsiet elementu “Uzņēmums”.</span><span class="sxs-lookup"><span data-stu-id="ce264-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="ce264-215">Kokā izvērsiet 'Company\find()'.</span><span class="sxs-lookup"><span data-stu-id="ce264-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="ce264-216">Kokā atlasiet 'Company\find()\Name'.</span><span class="sxs-lookup"><span data-stu-id="ce264-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="ce264-217">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ce264-217">Click Add data source.</span></span>
20. <span data-ttu-id="ce264-218">Laukā Formula ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ce264-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="ce264-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="ce264-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="ce264-220">Kokā atlasiet 'Company\find()\Company(DataArea)'.</span><span class="sxs-lookup"><span data-stu-id="ce264-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="ce264-221">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="ce264-221">Click Add data source.</span></span>
23. <span data-ttu-id="ce264-222">Laukā Formula ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="ce264-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="ce264-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="ce264-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="ce264-224">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ce264-224">Click Save.</span></span>
25. <span data-ttu-id="ce264-225">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ce264-225">Close the page.</span></span>
26. <span data-ttu-id="ce264-226">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ce264-226">Click Save.</span></span>
27. <span data-ttu-id="ce264-227">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ce264-227">Close the page.</span></span>
28. <span data-ttu-id="ce264-228">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ce264-228">Close the page.</span></span>
29. <span data-ttu-id="ce264-229">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="ce264-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="ce264-230">Esošas ER modeļa kartēšanas konfigurācijas izmantošana</span><span class="sxs-lookup"><span data-stu-id="ce264-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="ce264-231">Kokā atlasiet "Sample data model\Sample format".</span><span class="sxs-lookup"><span data-stu-id="ce264-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="ce264-232">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="ce264-232">Click Run.</span></span>
    * <span data-ttu-id="ce264-233">Atlasīto ER formāta konfigurācijas melnraksta versiju nevar izpildīt, jo ir vairāk nekā viena modeļu kartēšanas konfigurācija, kas pieejama nedefinētam datu modelim, kurš ir izvēlēts kā aktīva ER formāta datu avots.</span><span class="sxs-lookup"><span data-stu-id="ce264-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="ce264-234">Pēc tam jūs definēsiet alternatīvu modeļu kartēšanas konfigurāciju kā vienu no tiem modeļu kartējumiem, kas tiks izmantoti kā datu avoti ER formāta izpildei.</span><span class="sxs-lookup"><span data-stu-id="ce264-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="ce264-235">Kokā atlasiet "Sample data model\Sample mapping (alternative)".</span><span class="sxs-lookup"><span data-stu-id="ce264-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="ce264-236">Modeļu kartējuma laukā Noklusējums atlasiet vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="ce264-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="ce264-237">Kokā atlasiet "Sample data model\Sample format".</span><span class="sxs-lookup"><span data-stu-id="ce264-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="ce264-238">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="ce264-238">Click Run.</span></span>
7. <span data-ttu-id="ce264-239">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="ce264-239">Click OK.</span></span>
    * <span data-ttu-id="ce264-240">Noklusējuma modeļu kartēšanas konfigurācija tiek izmantota šai formāta konfigurācijai, lai ģenerētu elektronisko dokumentu (izveidotā izvade ietver uzņēmuma kodu).</span><span class="sxs-lookup"><span data-stu-id="ce264-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]