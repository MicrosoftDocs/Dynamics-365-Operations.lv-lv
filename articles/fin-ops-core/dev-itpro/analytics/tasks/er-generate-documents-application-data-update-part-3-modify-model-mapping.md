---
title: Modeļu un kartējumu modificēšana, lai ģenerētu dokumentus ar programmas datiem
description: Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu. (2. daļa – dokumentu ģenerēšana).
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
ms.openlocfilehash: 64bcf885fe2f5fca6b91589171b5e539eff2c3e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567096"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="50fb0-104">Modeļu un kartējumu modificēšana, lai ģenerētu dokumentus ar programmas datiem</span><span class="sxs-lookup"><span data-stu-id="50fb0-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50fb0-105">Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (2. daļa: Ģenerēt dokumentus)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="50fb0-106">Šajā procedūrā skaidrots, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu un atjauninātu pieteikuma datus.</span><span class="sxs-lookup"><span data-stu-id="50fb0-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="50fb0-107">Šajā procedūrā jūs modificēsit ER konfigurācijas, lai sāktu tās lietot elektronisku dokumentu ģenerēšanai un pieteikumu datu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="50fb0-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="50fb0-108">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="50fb0-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="50fb0-109">Šīs darbības var veikt, izmantojot DEMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="50fb0-110">Datu modeļa modificēšana</span><span class="sxs-lookup"><span data-stu-id="50fb0-110">Modify data model</span></span>
1. <span data-ttu-id="50fb0-111">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="50fb0-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="50fb0-112">Kokā atlasiet "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="50fb0-113">Jums būs jāpaplašina, kā izmantosiet datu modeli.</span><span class="sxs-lookup"><span data-stu-id="50fb0-113">You will extend how you use the data model.</span></span> <span data-ttu-id="50fb0-114">Papildus tā izmantošanai kā datu avotu, lai ģenerētu Intrastat pārskatu, datu modelis tiks izmantots, lai apkopotu informāciju par Intrastat pārskatu veidošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="50fb0-115">Pēc tam detalizēta informācija tiks izmantota, lai atjauninātu pieteikumu datus.</span><span class="sxs-lookup"><span data-stu-id="50fb0-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="50fb0-116">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="50fb0-116">Click Designer.</span></span>
4. <span data-ttu-id="50fb0-117">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="50fb0-118">Laukā Jauns zars ievadiet “Modeļa sakne”.</span><span class="sxs-lookup"><span data-stu-id="50fb0-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="50fb0-119">Laukā Nosaukums ierakstiet "For application data update".</span><span class="sxs-lookup"><span data-stu-id="50fb0-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="50fb0-120">Pieteikumu datu atjaunināšanai</span><span class="sxs-lookup"><span data-stu-id="50fb0-120">For application data update</span></span>  
7. <span data-ttu-id="50fb0-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="50fb0-121">Click Add.</span></span>
8. <span data-ttu-id="50fb0-122">Kokā atlasiet "For application data update".</span><span class="sxs-lookup"><span data-stu-id="50fb0-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="50fb0-123">Šis jaunais saknes vienums tika pievienots, lai norādītu datu plūsmu datu pārvietošanai no Intrastat pārskata (izmantots kā datu avots) uz pieteikuma tabulām (atjaunināšanas galamērķis).</span><span class="sxs-lookup"><span data-stu-id="50fb0-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="50fb0-124">Ņemiet vērā, ka datu iegūšanai, kas grāmatoti izejošā dokumentā, un datu iegūšanai no dokumenta, kas tiek izmantots pieteikumu datu atjaunināšanai, ir jāizmanto dažādi saknes vienumi.</span><span class="sxs-lookup"><span data-stu-id="50fb0-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="50fb0-125">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="50fb0-126">Laukā Nosaukums ierakstiet "Archive header".</span><span class="sxs-lookup"><span data-stu-id="50fb0-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="50fb0-127">Arhīva galvene</span><span class="sxs-lookup"><span data-stu-id="50fb0-127">Archive header</span></span>  
11. <span data-ttu-id="50fb0-128">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="50fb0-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="50fb0-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="50fb0-129">Click Add.</span></span>
    * <span data-ttu-id="50fb0-130">Tā kā izveidosit ierakstu katram ģenerētajam Intrastat pārskatam, jums tam ir jāizveido jauns vienums.</span><span class="sxs-lookup"><span data-stu-id="50fb0-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="50fb0-131">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="50fb0-132">Laukā Nosaukums ierakstiet 'File name'.</span><span class="sxs-lookup"><span data-stu-id="50fb0-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="50fb0-133">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="50fb0-133">File name</span></span>  
15. <span data-ttu-id="50fb0-134">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="50fb0-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="50fb0-135">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="50fb0-135">Click Add.</span></span>
17. <span data-ttu-id="50fb0-136">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="50fb0-137">Laukā Nosaukums ierakstiet "Number of lines".</span><span class="sxs-lookup"><span data-stu-id="50fb0-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="50fb0-138">Rindu skaits</span><span class="sxs-lookup"><span data-stu-id="50fb0-138">Number of lines</span></span>  
19. <span data-ttu-id="50fb0-139">Laukā Vienuma tips atlasiet "Integer".</span><span class="sxs-lookup"><span data-stu-id="50fb0-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="50fb0-140">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="50fb0-140">Click Add.</span></span>
    * <span data-ttu-id="50fb0-141">Pievienojiet šo vienumu, lai norādītu Intrastat darbību skaitu, kas tiek reģistrētas pašreizējā pārskata veidošanas procesā.</span><span class="sxs-lookup"><span data-stu-id="50fb0-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="50fb0-142">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="50fb0-143">Laukā Nosaukums ierakstiet "Archive lines".</span><span class="sxs-lookup"><span data-stu-id="50fb0-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="50fb0-144">Arhīva rindas</span><span class="sxs-lookup"><span data-stu-id="50fb0-144">Archive lines</span></span>  
23. <span data-ttu-id="50fb0-145">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="50fb0-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="50fb0-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="50fb0-146">Click Add.</span></span>
    * <span data-ttu-id="50fb0-147">Pievienojiet šo vienumu, lai norādītu sarakstu ar Intrastat darbībām, kas tiek reģistrētas pašreizējā pārskata veidošanas procesā.</span><span class="sxs-lookup"><span data-stu-id="50fb0-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="50fb0-148">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="50fb0-149">Laukā Nosaukums ierakstiet "Summa".</span><span class="sxs-lookup"><span data-stu-id="50fb0-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="50fb0-150">Summa</span><span class="sxs-lookup"><span data-stu-id="50fb0-150">Amount</span></span>  
27. <span data-ttu-id="50fb0-151">Laukā Vienuma tips atlasiet "Real".</span><span class="sxs-lookup"><span data-stu-id="50fb0-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="50fb0-152">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="50fb0-152">Click Add.</span></span>
29. <span data-ttu-id="50fb0-153">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="50fb0-154">Laukā Nosaukums ierakstiet "Commodity rec id".</span><span class="sxs-lookup"><span data-stu-id="50fb0-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="50fb0-155">Preces ieraksta ID</span><span class="sxs-lookup"><span data-stu-id="50fb0-155">Commodity rec id</span></span>  
31. <span data-ttu-id="50fb0-156">Laukā Krājuma veids atlasiet "Int64".</span><span class="sxs-lookup"><span data-stu-id="50fb0-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="50fb0-157">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="50fb0-157">Click Add.</span></span>
33. <span data-ttu-id="50fb0-158">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="50fb0-159">Laukā Nosaukums ierakstiet "Item number".</span><span class="sxs-lookup"><span data-stu-id="50fb0-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="50fb0-160">Krājums</span><span class="sxs-lookup"><span data-stu-id="50fb0-160">Item number</span></span>  
35. <span data-ttu-id="50fb0-161">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="50fb0-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="50fb0-162">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="50fb0-162">Click Add.</span></span>
37. <span data-ttu-id="50fb0-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-163">Click Save.</span></span>
38. <span data-ttu-id="50fb0-164">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="50fb0-165">Modeļa kartējuma modificēšana</span><span class="sxs-lookup"><span data-stu-id="50fb0-165">Modify model mapping</span></span>
1. <span data-ttu-id="50fb0-166">Kokā izvērsiet "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="50fb0-167">Kokā atlasiet "Intrastat (model)\Intrastat (mapping)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="50fb0-168">Modificējiet esošu modeļa kartējumu, lai sāktu to izmantot pieteikumu datu atjaunināšanai un arhivētu Intrastat pārskata datus.</span><span class="sxs-lookup"><span data-stu-id="50fb0-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="50fb0-169">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="50fb0-169">Click Designer.</span></span>
4. <span data-ttu-id="50fb0-170">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="50fb0-170">Click New.</span></span>
5. <span data-ttu-id="50fb0-171">Laukā Nosaukums ierakstiet "Update archive".</span><span class="sxs-lookup"><span data-stu-id="50fb0-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="50fb0-172">Atjaunināt arhīvu</span><span class="sxs-lookup"><span data-stu-id="50fb0-172">Update archive</span></span>  
6. <span data-ttu-id="50fb0-173">Laukā Virziens atlasiet "To destination".</span><span class="sxs-lookup"><span data-stu-id="50fb0-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="50fb0-174">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-174">Click Save.</span></span>
    * <span data-ttu-id="50fb0-175">Šis jaunais kartējums norāda datu plūsmu datu (Intrastat pārskata dati) pārvietošanai no datu modeļa uz pieteikuma tabulām (atjaunināšanas galamērķis).</span><span class="sxs-lookup"><span data-stu-id="50fb0-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="50fb0-176">Ņemiet vērā, ka, lai iegūtu datus no pieteikuma pārskatu veidošanas procesam un pēc tam izmantotu datus no datu modeļa pieteikumu datu atjaunināšanai, ir jāizmanto dažādi modeļa saknes vienumi.</span><span class="sxs-lookup"><span data-stu-id="50fb0-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="50fb0-177">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="50fb0-177">Click Designer.</span></span>
9. <span data-ttu-id="50fb0-178">Kokā atlasiet "Data model\Data model".</span><span class="sxs-lookup"><span data-stu-id="50fb0-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="50fb0-179">Pievienojiet nepieciešamo datu avotu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-179">Add the required data source.</span></span> <span data-ttu-id="50fb0-180">Šis ir datu modelis, kas ietver detalizētu informāciju par pārskatā iekļautajām Intrastat darbībām, kuras nepieciešams arhivēt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="50fb0-181">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="50fb0-181">Click Add root.</span></span>
11. <span data-ttu-id="50fb0-182">Laukā Nosaukums ierakstiet "model".</span><span class="sxs-lookup"><span data-stu-id="50fb0-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="50fb0-183">modelis</span><span class="sxs-lookup"><span data-stu-id="50fb0-183">model</span></span>  
12. <span data-ttu-id="50fb0-184">Laukā Definīcija ievadiet vai atlasiet vērtību 'Programmas datu atjauninājumam'.</span><span class="sxs-lookup"><span data-stu-id="50fb0-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="50fb0-185">Pieteikumu datu atjaunināšanai</span><span class="sxs-lookup"><span data-stu-id="50fb0-185">For application data update</span></span>  
13. <span data-ttu-id="50fb0-186">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="50fb0-186">Click OK.</span></span>
14. <span data-ttu-id="50fb0-187">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="50fb0-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="50fb0-188">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="50fb0-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="50fb0-189">Kokā atlasiet "model\Archive header".</span><span class="sxs-lookup"><span data-stu-id="50fb0-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="50fb0-190">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="50fb0-190">Click Add.</span></span>
    * <span data-ttu-id="50fb0-191">Tā kā vēlaties arhivēšanas nolūkā uzskaitīt pārskatā iekļautās Intrastat darbības, jāpievieno atbilstošs datu avots.</span><span class="sxs-lookup"><span data-stu-id="50fb0-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="50fb0-192">Laukā Nosaukums ierakstiet "Enumerated lines".</span><span class="sxs-lookup"><span data-stu-id="50fb0-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="50fb0-193">Uzskaitījuma rindas</span><span class="sxs-lookup"><span data-stu-id="50fb0-193">Enumerated lines</span></span>  
19. <span data-ttu-id="50fb0-194">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-194">Click Edit formula.</span></span>
20. <span data-ttu-id="50fb0-195">Kokā atlasiet "List\ENUMERATE".</span><span class="sxs-lookup"><span data-stu-id="50fb0-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="50fb0-196">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="50fb0-196">Click Add function.</span></span>
22. <span data-ttu-id="50fb0-197">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="50fb0-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="50fb0-198">Kokā izvērsiet "model\Archive header".</span><span class="sxs-lookup"><span data-stu-id="50fb0-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="50fb0-199">Kokā atlasiet "model\Archive header\Archive lines".</span><span class="sxs-lookup"><span data-stu-id="50fb0-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="50fb0-200">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-200">Click Add data source.</span></span>
26. <span data-ttu-id="50fb0-201">Laukā Formula ievadiet "ENUMERATE(model.'Archive header'.'Archive lines')".</span><span class="sxs-lookup"><span data-stu-id="50fb0-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="50fb0-202">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="50fb0-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="50fb0-203">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-203">Click Save.</span></span>
28. <span data-ttu-id="50fb0-204">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-204">Close the page.</span></span>
29. <span data-ttu-id="50fb0-205">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="50fb0-205">Click OK.</span></span>
30. <span data-ttu-id="50fb0-206">Noklikšķiniet uz Pievienot mērķi.</span><span class="sxs-lookup"><span data-stu-id="50fb0-206">Click Add destination.</span></span>
    * <span data-ttu-id="50fb0-207">Pievienojiet pieteikuma tabulas kā nepieciešamos mērķus, kuriem vajadzīga atjaunināšana, lai arhivētu detalizētu informāciju par pārskatā iekļautajām Intrastat darbībām.</span><span class="sxs-lookup"><span data-stu-id="50fb0-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="50fb0-208">Laukā Nosaukums ierakstiet "Archive".</span><span class="sxs-lookup"><span data-stu-id="50fb0-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="50fb0-209">Arhivēt</span><span class="sxs-lookup"><span data-stu-id="50fb0-209">Archive</span></span>  
32. <span data-ttu-id="50fb0-210">Laukā Tabulas nosaukums ierakstiet "IntrastatArchiveGeneral".</span><span class="sxs-lookup"><span data-stu-id="50fb0-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="50fb0-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="50fb0-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="50fb0-212">Saglabājiet ieraksta darbību 'Ievietot', lai varētu pievienot ierakstus katra Intrastat pārskatu veidošanas procesa detalizētas informācijas arhivēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="50fb0-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="50fb0-213">Laukā Reģistrēt informācijas žurnālu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="50fb0-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="50fb0-214">Atlasiet Jā, lai iegūtu informāciju par problēmām, kas saistītas ar pieteikumu datu atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="50fb0-215">Laukā Izlaist ieraksta darbības validēšanu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="50fb0-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="50fb0-216">Atlasiet Jā, lai likvidētu pārbaudes kļūdas par tukšu lauku 'Intrastat arhīva ID'.</span><span class="sxs-lookup"><span data-stu-id="50fb0-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="50fb0-217">Tas tiks veikts pēc ierakstu pievienošanas, pamatojoties uz sērijas numuru iestatījumiem, kas konfigurēti šai tabulai formā Ārējās tirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="50fb0-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="50fb0-218">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="50fb0-218">Click OK.</span></span>
    * <span data-ttu-id="50fb0-219">Saistiet pievienoto datu avotu (filtrētais modelis, pamatojoties uz atlasīto saknes vienumu) elementus ar elementiem no pievienotā galamērķa.</span><span class="sxs-lookup"><span data-stu-id="50fb0-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="50fb0-220">Kokā izvērsiet "Archive".</span><span class="sxs-lookup"><span data-stu-id="50fb0-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="50fb0-221">Kokā izvērsiet "Archive\<Relations".</span><span class="sxs-lookup"><span data-stu-id="50fb0-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="50fb0-222">Kokā izvērsiet "Archive\<Relations\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="50fb0-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="50fb0-223">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="50fb0-224">Kokā izvērsiet "model\Archive header\Enumerated lines".</span><span class="sxs-lookup"><span data-stu-id="50fb0-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="50fb0-225">Kokā izvērsiet "model\Archive header\Enumerated lines\Value".</span><span class="sxs-lookup"><span data-stu-id="50fb0-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="50fb0-226">Kokā atlasiet "model\Archive header\Enumerated lines\Value\Amount".</span><span class="sxs-lookup"><span data-stu-id="50fb0-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="50fb0-227">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-227">Click Bind.</span></span>
44. <span data-ttu-id="50fb0-228">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="50fb0-229">Kokā atlasiet "model\Archive header\Enumerated lines\Value\Commodity rec id".</span><span class="sxs-lookup"><span data-stu-id="50fb0-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="50fb0-230">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-230">Click Bind.</span></span>
47. <span data-ttu-id="50fb0-231">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="50fb0-232">Kokā atlasiet "model\Archive header\Enumerated lines\Value\Item number".</span><span class="sxs-lookup"><span data-stu-id="50fb0-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="50fb0-233">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-233">Click Bind.</span></span>
50. <span data-ttu-id="50fb0-234">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="50fb0-235">Kokā atlasiet "model\Archive header\Enumerated lines\Number".</span><span class="sxs-lookup"><span data-stu-id="50fb0-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="50fb0-236">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-236">Click Bind.</span></span>
53. <span data-ttu-id="50fb0-237">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="50fb0-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="50fb0-238">Kokā atlasiet "model\Archive header\Enumerated lines".</span><span class="sxs-lookup"><span data-stu-id="50fb0-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="50fb0-239">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-239">Click Bind.</span></span>
56. <span data-ttu-id="50fb0-240">Kokā atlasiet "Archive\File name(FileName)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="50fb0-241">Kokā atlasiet "model\Archive header\File name".</span><span class="sxs-lookup"><span data-stu-id="50fb0-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="50fb0-242">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-242">Click Bind.</span></span>
59. <span data-ttu-id="50fb0-243">Kokā atlasiet "Archive\Number of lines(NumberOfLines)".</span><span class="sxs-lookup"><span data-stu-id="50fb0-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="50fb0-244">Kokā atlasiet "model\Archive header\Number of lines".</span><span class="sxs-lookup"><span data-stu-id="50fb0-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="50fb0-245">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-245">Click Bind.</span></span>
62. <span data-ttu-id="50fb0-246">Kokā atlasiet "Archive".</span><span class="sxs-lookup"><span data-stu-id="50fb0-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="50fb0-247">Kokā atlasiet "model\Archive header".</span><span class="sxs-lookup"><span data-stu-id="50fb0-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="50fb0-248">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-248">Click Bind.</span></span>
65. <span data-ttu-id="50fb0-249">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="50fb0-249">Click Save.</span></span>
66. <span data-ttu-id="50fb0-250">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-250">Close the page.</span></span>
67. <span data-ttu-id="50fb0-251">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="50fb0-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]