--- 
title: "Formāta modificēšana un darbināšana, lai dokumentu pārvaldības failus lietotu formāta izvades datos"
description: "Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1c8a71c76b81991e88097c6d043e6ac50b5a3ad9
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs"></a><span data-ttu-id="6f769-103">Formāta modificēšana un darbināšana, lai dokumentu pārvaldības failus lietotu formāta izvades datos</span><span class="sxs-lookup"><span data-stu-id="6f769-103">Modify and run format to use Document Management files in format outputs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f769-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="6f769-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="6f769-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="6f769-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="6f769-106">Lai veiktu šīs darbības, vispirms pabeidziet darbības procedūrā "ER izmantot dokumentu pārvaldības failus formāta izvadēs (4. daļa): Formatēšanas izpilde".</span><span class="sxs-lookup"><span data-stu-id="6f769-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="6f769-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="6f769-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="6f769-108">Modificējiet formātu, lai aizpildītu pielikumus, ģenerējot ziņojumus binārā formātā</span><span class="sxs-lookup"><span data-stu-id="6f769-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="6f769-109">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="6f769-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6f769-110">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="6f769-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="6f769-111">Kokā izvērsiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)".</span><span class="sxs-lookup"><span data-stu-id="6f769-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="6f769-112">Kokā atlasiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)\Elektronisks rēķina parauga ziņojums".</span><span class="sxs-lookup"><span data-stu-id="6f769-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="6f769-113">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="6f769-113">Click Designer.</span></span>
    * <span data-ttu-id="6f769-114">Jūs aizpildīsiet rēķina ziņojumu, veidojot ražojumu kā XML failu, izmantojot unikoda kodējumu.</span><span class="sxs-lookup"><span data-stu-id="6f769-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="6f769-115">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="6f769-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="6f769-116">Kokā atlasiet "Vispārīgi\Fails".</span><span class="sxs-lookup"><span data-stu-id="6f769-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="6f769-117">Laukā Nosaukums ierakstiet 'Xml ziņojums'.</span><span class="sxs-lookup"><span data-stu-id="6f769-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="6f769-118">Xml ziņojums</span><span class="sxs-lookup"><span data-stu-id="6f769-118">Xml message</span></span>  
9. <span data-ttu-id="6f769-119">Laukā Kodēšana ierakstiet "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="6f769-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="6f769-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="6f769-120">UTF-8</span></span>  
10. <span data-ttu-id="6f769-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f769-121">Click OK.</span></span>
    * <span data-ttu-id="6f769-122">Konfigurējiet ražojuma veidošanu kā arhivēto failu.</span><span class="sxs-lookup"><span data-stu-id="6f769-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="6f769-123">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="6f769-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="6f769-124">Kokā atlasiet "Vispārīgi\Mape".</span><span class="sxs-lookup"><span data-stu-id="6f769-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="6f769-125">Laukā Nosaukums ierakstiet 'Arhivēta izvade.</span><span class="sxs-lookup"><span data-stu-id="6f769-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="6f769-126">Zip izvade</span><span class="sxs-lookup"><span data-stu-id="6f769-126">Zip output</span></span>  
14. <span data-ttu-id="6f769-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f769-127">Click OK.</span></span>
15. <span data-ttu-id="6f769-128">Kokā atlasiet 'Arhivēta izvade'.</span><span class="sxs-lookup"><span data-stu-id="6f769-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="6f769-129">Pievienojiet pielikumus veidošanas arhivētajam failam kā failus ar sākotnējiem nosaukumiem un paplašinājumiem.</span><span class="sxs-lookup"><span data-stu-id="6f769-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="6f769-130">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f769-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="6f769-131">Kokā atlasiet "Vispārīgi\Fails".</span><span class="sxs-lookup"><span data-stu-id="6f769-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="6f769-132">Laukā Nosaukums, ierakstiet 'Pievienotais fails'.</span><span class="sxs-lookup"><span data-stu-id="6f769-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="6f769-133">Pievienotais fails</span><span class="sxs-lookup"><span data-stu-id="6f769-133">Attached file</span></span>  
19. <span data-ttu-id="6f769-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f769-134">Click OK.</span></span>
20. <span data-ttu-id="6f769-135">Kokā atlasiet 'Arhivēta izvade\Pievienotais fails'.</span><span class="sxs-lookup"><span data-stu-id="6f769-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="6f769-136">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6f769-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="6f769-137">Koka struktūrā atlasiet 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="6f769-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="6f769-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f769-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="6f769-139">Kartējiet jaunus formatēšanas elementus datu modelī</span><span class="sxs-lookup"><span data-stu-id="6f769-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="6f769-140">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="6f769-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="6f769-141">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="6f769-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="6f769-142">Koka struktūrā izvērsiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="6f769-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="6f769-143">Kokā atlasiet 'Arhivēta izvade\Pievienotais fails\Base64'.</span><span class="sxs-lookup"><span data-stu-id="6f769-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="6f769-144">Koka struktūrā atlasiet 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="6f769-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="6f769-145">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f769-145">Click Bind.</span></span>
7. <span data-ttu-id="6f769-146">Kokā atlasiet 'Arhivēta izvade\Pievienotais fails'.</span><span class="sxs-lookup"><span data-stu-id="6f769-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="6f769-147">Noklikšķiniet uz rediģēt faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6f769-147">Click Edit filename.</span></span>
9. <span data-ttu-id="6f769-148">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="6f769-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="6f769-149">Koka struktūrā izvērsiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="6f769-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="6f769-150">Koka struktūrā atlasiet 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="6f769-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="6f769-151">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="6f769-151">Click Add data source.</span></span>
13. <span data-ttu-id="6f769-152">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6f769-152">Click Save.</span></span>
14. <span data-ttu-id="6f769-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6f769-153">Close the page.</span></span>
15. <span data-ttu-id="6f769-154">Koka struktūrā atlasiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="6f769-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="6f769-155">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="6f769-155">Click Bind.</span></span>
17. <span data-ttu-id="6f769-156">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6f769-156">Click Save.</span></span>
18. <span data-ttu-id="6f769-157">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6f769-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="6f769-158">Atlasītajam rēķinam noformētas atskaites palaišana</span><span class="sxs-lookup"><span data-stu-id="6f769-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="6f769-159">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="6f769-159">Click Run.</span></span>
2. <span data-ttu-id="6f769-160">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="6f769-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="6f769-161">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="6f769-161">Click Filter.</span></span>
4. <span data-ttu-id="6f769-162">Atlasiet rindu no debitora rēķinu žurnāla un pārdošanas pasūtījuma lauka.</span><span class="sxs-lookup"><span data-stu-id="6f769-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="6f769-163">Laukā Kritēriji, kritērija “pārdošanas pasūtījums' laukā ierakstiet pasūtījuma numuru 000148.</span><span class="sxs-lookup"><span data-stu-id="6f769-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="6f769-164">000148</span><span class="sxs-lookup"><span data-stu-id="6f769-164">000148</span></span>  
6. <span data-ttu-id="6f769-165">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f769-165">Click OK.</span></span>
7. <span data-ttu-id="6f769-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6f769-166">Click OK.</span></span>
    * <span data-ttu-id="6f769-167">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="6f769-167">Review the generated output.</span></span> <span data-ttu-id="6f769-168">Ņemiet vērā, ka papildus rēķina ziņojumam XML formātā katram pielikumam ir izveidots atsevišķs fails.</span><span class="sxs-lookup"><span data-stu-id="6f769-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="6f769-169">Pielikumu faili tiek aizpildīti ar arhivētu izvadi binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="6f769-169">The attachment files are populated with the zipped output in binary format.</span></span>  


