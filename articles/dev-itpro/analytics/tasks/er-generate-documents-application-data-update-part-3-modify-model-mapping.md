---
title: Modeļu un kartējumu modificēšana, lai ģenerētu dokumentus ar programmas datiem
description: 'Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (2. daļa — ģenerēt dokumentus)".'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 580f00faf6694dc2da476ffa75f995d9a24e0f8b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "361939"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="69145-103">Modeļu un kartējumu modificēšana, lai ģenerētu dokumentus ar programmas datiem</span><span class="sxs-lookup"><span data-stu-id="69145-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="69145-104">Lai pabeigtu šīs procedūras darbības, vispirms jāpabeidz procedūra "ER: ģenerēt dokumentus ar pieteikumu datu atjaunināšanu (2. daļa — ģenerēt dokumentus)".</span><span class="sxs-lookup"><span data-stu-id="69145-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="69145-105">Šajā procedūrā skaidrots, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, lai ģenerētu elektronisku dokumentu un atjauninātu pieteikuma datus.</span><span class="sxs-lookup"><span data-stu-id="69145-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="69145-106">Šajā procedūrā jūs modificēsit ER konfigurācijas, lai sāktu tās lietot elektronisku dokumentu ģenerēšanai un pieteikumu datu atjaunināšanai.</span><span class="sxs-lookup"><span data-stu-id="69145-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="69145-107">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="69145-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="69145-108">Šīs darbības var veikt, izmantojot DEMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="69145-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="69145-109">Datu modeļa modificēšana</span><span class="sxs-lookup"><span data-stu-id="69145-109">Modify data model</span></span>
1. <span data-ttu-id="69145-110">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="69145-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="69145-111">Kokā atlasiet "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="69145-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="69145-112">Jums būs jāpaplašina, kā izmantosiet datu modeli.</span><span class="sxs-lookup"><span data-stu-id="69145-112">You will extend how you use the data model.</span></span> <span data-ttu-id="69145-113">Papildus tā izmantošanai kā datu avotu, lai ģenerētu Intrastat pārskatu, datu modelis tiks izmantots, lai apkopotu informāciju par Intrastat pārskatu veidošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="69145-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="69145-114">Pēc tam detalizēta informācija tiks izmantota, lai atjauninātu pieteikumu datus.</span><span class="sxs-lookup"><span data-stu-id="69145-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="69145-115">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="69145-115">Click Designer.</span></span>
4. <span data-ttu-id="69145-116">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="69145-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="69145-117">Laukā Jauns zars ievadiet “Modeļa sakne”.</span><span class="sxs-lookup"><span data-stu-id="69145-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="69145-118">Laukā Nosaukums ierakstiet "For application data update".</span><span class="sxs-lookup"><span data-stu-id="69145-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="69145-119">Pieteikumu datu atjaunināšanai</span><span class="sxs-lookup"><span data-stu-id="69145-119">For application data update</span></span>  
7. <span data-ttu-id="69145-120">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="69145-120">Click Add.</span></span>
8. <span data-ttu-id="69145-121">Kokā atlasiet "For application data update".</span><span class="sxs-lookup"><span data-stu-id="69145-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="69145-122">Šis jaunais saknes vienums tika pievienots, lai norādītu datu plūsmu datu pārvietošanai no Intrastat pārskata (izmantots kā datu avots) uz pieteikuma tabulām (atjaunināšanas galamērķis).</span><span class="sxs-lookup"><span data-stu-id="69145-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="69145-123">Ņemiet vērā, ka datu iegūšanai, kas grāmatoti izejošā dokumentā, un datu iegūšanai no dokumenta, kas tiek izmantots pieteikumu datu atjaunināšanai, ir jāizmanto dažādi saknes vienumi.</span><span class="sxs-lookup"><span data-stu-id="69145-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="69145-124">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="69145-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="69145-125">Laukā Nosaukums ierakstiet "Archive header".</span><span class="sxs-lookup"><span data-stu-id="69145-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="69145-126">Arhīva galvene</span><span class="sxs-lookup"><span data-stu-id="69145-126">Archive header</span></span>  
11. <span data-ttu-id="69145-127">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="69145-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="69145-128">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="69145-128">Click Add.</span></span>
    * <span data-ttu-id="69145-129">Tā kā izveidosit ierakstu katram ģenerētajam Intrastat pārskatam, jums tam ir jāizveido jauns vienums.</span><span class="sxs-lookup"><span data-stu-id="69145-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="69145-130">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="69145-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="69145-131">Laukā Nosaukums ierakstiet 'File name'.</span><span class="sxs-lookup"><span data-stu-id="69145-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="69145-132">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="69145-132">File name</span></span>  
15. <span data-ttu-id="69145-133">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="69145-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="69145-134">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="69145-134">Click Add.</span></span>
17. <span data-ttu-id="69145-135">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="69145-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="69145-136">Laukā Nosaukums ierakstiet "Number of lines".</span><span class="sxs-lookup"><span data-stu-id="69145-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="69145-137">Rindu skaits</span><span class="sxs-lookup"><span data-stu-id="69145-137">Number of lines</span></span>  
19. <span data-ttu-id="69145-138">Laukā Vienuma tips atlasiet "Integer".</span><span class="sxs-lookup"><span data-stu-id="69145-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="69145-139">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="69145-139">Click Add.</span></span>
    * <span data-ttu-id="69145-140">Pievienojiet šo vienumu, lai norādītu Intrastat darbību skaitu, kas tiek reģistrētas pašreizējā pārskata veidošanas procesā.</span><span class="sxs-lookup"><span data-stu-id="69145-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="69145-141">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="69145-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="69145-142">Laukā Nosaukums ierakstiet "Archive lines".</span><span class="sxs-lookup"><span data-stu-id="69145-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="69145-143">Arhīva rindas</span><span class="sxs-lookup"><span data-stu-id="69145-143">Archive lines</span></span>  
23. <span data-ttu-id="69145-144">Laukā Vienuma tips atlasiet "Record list".</span><span class="sxs-lookup"><span data-stu-id="69145-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="69145-145">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="69145-145">Click Add.</span></span>
    * <span data-ttu-id="69145-146">Pievienojiet šo vienumu, lai norādītu sarakstu ar Intrastat darbībām, kas tiek reģistrētas pašreizējā pārskata veidošanas procesā.</span><span class="sxs-lookup"><span data-stu-id="69145-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="69145-147">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="69145-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="69145-148">Laukā Nosaukums ierakstiet "Summa".</span><span class="sxs-lookup"><span data-stu-id="69145-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="69145-149">Summa</span><span class="sxs-lookup"><span data-stu-id="69145-149">Amount</span></span>  
27. <span data-ttu-id="69145-150">Laukā Vienuma tips atlasiet "Real".</span><span class="sxs-lookup"><span data-stu-id="69145-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="69145-151">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="69145-151">Click Add.</span></span>
29. <span data-ttu-id="69145-152">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="69145-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="69145-153">Laukā Nosaukums ierakstiet "Commodity rec id".</span><span class="sxs-lookup"><span data-stu-id="69145-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="69145-154">Preces ieraksta ID</span><span class="sxs-lookup"><span data-stu-id="69145-154">Commodity rec id</span></span>  
31. <span data-ttu-id="69145-155">Laukā Krājuma veids atlasiet "Int64".</span><span class="sxs-lookup"><span data-stu-id="69145-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="69145-156">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="69145-156">Click Add.</span></span>
33. <span data-ttu-id="69145-157">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="69145-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="69145-158">Laukā Nosaukums ierakstiet "Item number".</span><span class="sxs-lookup"><span data-stu-id="69145-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="69145-159">Krājums</span><span class="sxs-lookup"><span data-stu-id="69145-159">Item number</span></span>  
35. <span data-ttu-id="69145-160">Laukā Vienuma tips atlasiet "String".</span><span class="sxs-lookup"><span data-stu-id="69145-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="69145-161">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="69145-161">Click Add.</span></span>
37. <span data-ttu-id="69145-162">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="69145-162">Click Save.</span></span>
38. <span data-ttu-id="69145-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="69145-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="69145-164">Modeļa kartējuma modificēšana</span><span class="sxs-lookup"><span data-stu-id="69145-164">Modify model mapping</span></span>
1. <span data-ttu-id="69145-165">Kokā izvērsiet "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="69145-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="69145-166">Kokā atlasiet "Intrastat (model)\Intrastat (mapping)".</span><span class="sxs-lookup"><span data-stu-id="69145-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="69145-167">Modificējiet esošu modeļa kartējumu, lai sāktu to izmantot pieteikumu datu atjaunināšanai un arhivētu Intrastat pārskata datus.</span><span class="sxs-lookup"><span data-stu-id="69145-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="69145-168">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="69145-168">Click Designer.</span></span>
4. <span data-ttu-id="69145-169">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="69145-169">Click New.</span></span>
5. <span data-ttu-id="69145-170">Laukā Nosaukums ierakstiet "Update archive".</span><span class="sxs-lookup"><span data-stu-id="69145-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="69145-171">Atjaunināt arhīvu</span><span class="sxs-lookup"><span data-stu-id="69145-171">Update archive</span></span>  
6. <span data-ttu-id="69145-172">Laukā Virziens atlasiet "To destination".</span><span class="sxs-lookup"><span data-stu-id="69145-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="69145-173">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="69145-173">Click Save.</span></span>
    * <span data-ttu-id="69145-174">Šis jaunais kartējums norāda datu plūsmu datu (Intrastat pārskata dati) pārvietošanai no datu modeļa uz pieteikuma tabulām (atjaunināšanas galamērķis).</span><span class="sxs-lookup"><span data-stu-id="69145-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="69145-175">Ņemiet vērā, ka, lai iegūtu datus no pieteikuma pārskatu veidošanas procesam un pēc tam izmantotu datus no datu modeļa pieteikumu datu atjaunināšanai, ir jāizmanto dažādi modeļa saknes vienumi.</span><span class="sxs-lookup"><span data-stu-id="69145-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="69145-176">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="69145-176">Click Designer.</span></span>
9. <span data-ttu-id="69145-177">Kokā atlasiet "Data model\Data model".</span><span class="sxs-lookup"><span data-stu-id="69145-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="69145-178">Pievienojiet nepieciešamo datu avotu.</span><span class="sxs-lookup"><span data-stu-id="69145-178">Add the required data source.</span></span> <span data-ttu-id="69145-179">Šis ir datu modelis, kas ietver detalizētu informāciju par pārskatā iekļautajām Intrastat darbībām, kuras nepieciešams arhivēt.</span><span class="sxs-lookup"><span data-stu-id="69145-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="69145-180">Noklikšķiniet uz Pievienot sakni.</span><span class="sxs-lookup"><span data-stu-id="69145-180">Click Add root.</span></span>
11. <span data-ttu-id="69145-181">Laukā Nosaukums ierakstiet "model".</span><span class="sxs-lookup"><span data-stu-id="69145-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="69145-182">modelis</span><span class="sxs-lookup"><span data-stu-id="69145-182">model</span></span>  
12. <span data-ttu-id="69145-183">Laukā Definīcija ievadiet vai atlasiet vērtību "For application data update".</span><span class="sxs-lookup"><span data-stu-id="69145-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="69145-184">Pieteikumu datu atjaunināšanai</span><span class="sxs-lookup"><span data-stu-id="69145-184">For application data update</span></span>  
13. <span data-ttu-id="69145-185">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="69145-185">Click OK.</span></span>
14. <span data-ttu-id="69145-186">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="69145-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="69145-187">Kokā atlasiet Funkcijas\Aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="69145-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="69145-188">Kokā atlasiet "model\Archive header".</span><span class="sxs-lookup"><span data-stu-id="69145-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="69145-189">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="69145-189">Click Add.</span></span>
    * <span data-ttu-id="69145-190">Tā kā vēlaties arhivēšanas nolūkā uzskaitīt pārskatā iekļautās Intrastat darbības, jāpievieno atbilstošs datu avots.</span><span class="sxs-lookup"><span data-stu-id="69145-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="69145-191">Laukā Nosaukums ierakstiet "Enumerated lines".</span><span class="sxs-lookup"><span data-stu-id="69145-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="69145-192">Uzskaitījuma rindas</span><span class="sxs-lookup"><span data-stu-id="69145-192">Enumerated lines</span></span>  
19. <span data-ttu-id="69145-193">Noklikšķiniet uz Rediģēt formulu.</span><span class="sxs-lookup"><span data-stu-id="69145-193">Click Edit formula.</span></span>
20. <span data-ttu-id="69145-194">Kokā atlasiet "List\ENUMERATE".</span><span class="sxs-lookup"><span data-stu-id="69145-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="69145-195">Noklikšķiniet uz Pievienot funkciju.</span><span class="sxs-lookup"><span data-stu-id="69145-195">Click Add function.</span></span>
22. <span data-ttu-id="69145-196">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="69145-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="69145-197">Kokā izvērsiet "model\Archive header".</span><span class="sxs-lookup"><span data-stu-id="69145-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="69145-198">Kokā atlasiet "model\Archive header\Archive lines".</span><span class="sxs-lookup"><span data-stu-id="69145-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="69145-199">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="69145-199">Click Add data source.</span></span>
26. <span data-ttu-id="69145-200">Laukā Formula ievadiet "ENUMERATE(model.'Archive header'.'Archive lines')".</span><span class="sxs-lookup"><span data-stu-id="69145-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="69145-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="69145-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="69145-202">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="69145-202">Click Save.</span></span>
28. <span data-ttu-id="69145-203">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="69145-203">Close the page.</span></span>
29. <span data-ttu-id="69145-204">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="69145-204">Click OK.</span></span>
30. <span data-ttu-id="69145-205">Noklikšķiniet uz Pievienot mērķi.</span><span class="sxs-lookup"><span data-stu-id="69145-205">Click Add destination.</span></span>
    * <span data-ttu-id="69145-206">Pievienojiet pieteikuma tabulas kā nepieciešamos mērķus, kuriem vajadzīga atjaunināšana, lai arhivētu detalizētu informāciju par pārskatā iekļautajām Intrastat darbībām.</span><span class="sxs-lookup"><span data-stu-id="69145-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="69145-207">Laukā Nosaukums ierakstiet "Archive".</span><span class="sxs-lookup"><span data-stu-id="69145-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="69145-208">Arhivēt</span><span class="sxs-lookup"><span data-stu-id="69145-208">Archive</span></span>  
32. <span data-ttu-id="69145-209">Laukā Tabulas nosaukums ierakstiet "IntrastatArchiveGeneral".</span><span class="sxs-lookup"><span data-stu-id="69145-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="69145-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="69145-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="69145-211">Saglabājiet ieraksta darbību 'Insert', lai varētu pievienot ierakstus katra Intrastat pārskatu veidošanas procesa detalizētas informācijas arhivēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="69145-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="69145-212">Laukā Reģistrēt informācijas žurnālu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="69145-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="69145-213">Atlasiet Jā, lai iegūtu informāciju par problēmām, kas saistītas ar pieteikumu datu atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="69145-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="69145-214">Laukā Izlaist ieraksta darbības validēšanu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="69145-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="69145-215">Atlasiet Jā, lai likvidētu pārbaudes kļūdas par tukšu lauku "Intrastat archive ID".</span><span class="sxs-lookup"><span data-stu-id="69145-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="69145-216">Tas tiks veikts pēc ierakstu pievienošanas, pamatojoties uz sērijas numuru iestatījumiem, kas konfigurēti šai tabulai formā Ārējās tirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="69145-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="69145-217">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="69145-217">Click OK.</span></span>
    * <span data-ttu-id="69145-218">Saistiet pievienoto datu avotu (filtrētais modelis, pamatojoties uz atlasīto saknes vienumu) elementus ar elementiem no pievienotā galamērķa.</span><span class="sxs-lookup"><span data-stu-id="69145-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="69145-219">Kokā izvērsiet "Archive".</span><span class="sxs-lookup"><span data-stu-id="69145-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="69145-220">Kokā izvērsiet "Archive\<Relations".</span><span class="sxs-lookup"><span data-stu-id="69145-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="69145-221">Kokā izvērsiet "Archive\<Relations\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="69145-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="69145-222">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)".</span><span class="sxs-lookup"><span data-stu-id="69145-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="69145-223">Kokā izvērsiet "model\Archive header\Enumerated lines".</span><span class="sxs-lookup"><span data-stu-id="69145-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="69145-224">Kokā izvērsiet "model\Archive header\Enumerated lines\Value".</span><span class="sxs-lookup"><span data-stu-id="69145-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="69145-225">Kokā atlasiet "model\Archive header\Enumerated lines\Value\Amount".</span><span class="sxs-lookup"><span data-stu-id="69145-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="69145-226">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="69145-226">Click Bind.</span></span>
44. <span data-ttu-id="69145-227">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)".</span><span class="sxs-lookup"><span data-stu-id="69145-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="69145-228">Kokā atlasiet "model\Archive header\Enumerated lines\Value\Commodity rec id".</span><span class="sxs-lookup"><span data-stu-id="69145-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="69145-229">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="69145-229">Click Bind.</span></span>
47. <span data-ttu-id="69145-230">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)".</span><span class="sxs-lookup"><span data-stu-id="69145-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="69145-231">Kokā atlasiet "model\Archive header\Enumerated lines\Value\Item number".</span><span class="sxs-lookup"><span data-stu-id="69145-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="69145-232">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="69145-232">Click Bind.</span></span>
50. <span data-ttu-id="69145-233">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)".</span><span class="sxs-lookup"><span data-stu-id="69145-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="69145-234">Kokā atlasiet "model\Archive header\Enumerated lines\Number".</span><span class="sxs-lookup"><span data-stu-id="69145-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="69145-235">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="69145-235">Click Bind.</span></span>
53. <span data-ttu-id="69145-236">Kokā atlasiet "Archive\<Relations\IntrastatArchiveDetail".</span><span class="sxs-lookup"><span data-stu-id="69145-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="69145-237">Kokā atlasiet "model\Archive header\Enumerated lines".</span><span class="sxs-lookup"><span data-stu-id="69145-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="69145-238">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="69145-238">Click Bind.</span></span>
56. <span data-ttu-id="69145-239">Kokā atlasiet "Archive\File name(FileName)".</span><span class="sxs-lookup"><span data-stu-id="69145-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="69145-240">Kokā atlasiet "model\Archive header\File name".</span><span class="sxs-lookup"><span data-stu-id="69145-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="69145-241">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="69145-241">Click Bind.</span></span>
59. <span data-ttu-id="69145-242">Kokā atlasiet "Archive\Number of lines(NumberOfLines)".</span><span class="sxs-lookup"><span data-stu-id="69145-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="69145-243">Kokā atlasiet "model\Archive header\Number of lines".</span><span class="sxs-lookup"><span data-stu-id="69145-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="69145-244">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="69145-244">Click Bind.</span></span>
62. <span data-ttu-id="69145-245">Kokā atlasiet "Archive".</span><span class="sxs-lookup"><span data-stu-id="69145-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="69145-246">Kokā atlasiet "model\Archive header".</span><span class="sxs-lookup"><span data-stu-id="69145-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="69145-247">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="69145-247">Click Bind.</span></span>
65. <span data-ttu-id="69145-248">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="69145-248">Click Save.</span></span>
66. <span data-ttu-id="69145-249">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="69145-249">Close the page.</span></span>
67. <span data-ttu-id="69145-250">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="69145-250">Close the page.</span></span>

