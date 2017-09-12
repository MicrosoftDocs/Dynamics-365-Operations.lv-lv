--- 
title: "Modificēt un palaist formātu dokumentu pārvaldības failu lietošanai formāta izvades datos elektronisko pārskatu veidošanai (ER)"
description: "Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 58e79f4d969e8bf0c7f150fd307f9f48334d6405
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="660c6-103">Modificēt un palaist formātu dokumentu pārvaldības failu lietošanai formāta izvades datos elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="660c6-103">Modify and run format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="660c6-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="660c6-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="660c6-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="660c6-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="660c6-106">Lai veiktu šīs darbības, vispirms pabeidziet darbības procedūrā "ER izmantot dokumentu pārvaldības failus formāta izvadēs (4. daļa): Formatēšanas izpilde".</span><span class="sxs-lookup"><span data-stu-id="660c6-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="660c6-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="660c6-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="660c6-108">Modificējiet formātu, lai aizpildītu pielikumus, ģenerējot ziņojumus binārā formātā</span><span class="sxs-lookup"><span data-stu-id="660c6-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="660c6-109">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="660c6-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="660c6-110">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="660c6-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="660c6-111">Kokā izvērsiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)".</span><span class="sxs-lookup"><span data-stu-id="660c6-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="660c6-112">Kokā atlasiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)\Elektronisks rēķina parauga ziņojums".</span><span class="sxs-lookup"><span data-stu-id="660c6-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="660c6-113">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="660c6-113">Click Designer.</span></span>
    * <span data-ttu-id="660c6-114">Jūs aizpildīsiet rēķina ziņojumu, veidojot ražojumu kā XML failu, izmantojot unikoda kodējumu.</span><span class="sxs-lookup"><span data-stu-id="660c6-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="660c6-115">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="660c6-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="660c6-116">Kokā atlasiet "Vispārīgi\Fails".</span><span class="sxs-lookup"><span data-stu-id="660c6-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="660c6-117">Laukā Nosaukums ierakstiet 'Xml ziņojums'.</span><span class="sxs-lookup"><span data-stu-id="660c6-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="660c6-118">Xml ziņojums</span><span class="sxs-lookup"><span data-stu-id="660c6-118">Xml message</span></span>  
9. <span data-ttu-id="660c6-119">Laukā Kodēšana ierakstiet "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="660c6-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="660c6-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="660c6-120">UTF-8</span></span>  
10. <span data-ttu-id="660c6-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="660c6-121">Click OK.</span></span>
    * <span data-ttu-id="660c6-122">Konfigurējiet ražojuma veidošanu kā arhivēto failu.</span><span class="sxs-lookup"><span data-stu-id="660c6-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="660c6-123">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="660c6-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="660c6-124">Kokā atlasiet "Vispārīgi\Mape".</span><span class="sxs-lookup"><span data-stu-id="660c6-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="660c6-125">Laukā Nosaukums ierakstiet 'Arhivēta izvade.</span><span class="sxs-lookup"><span data-stu-id="660c6-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="660c6-126">Zip izvade</span><span class="sxs-lookup"><span data-stu-id="660c6-126">Zip output</span></span>  
14. <span data-ttu-id="660c6-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="660c6-127">Click OK.</span></span>
15. <span data-ttu-id="660c6-128">Kokā atlasiet 'Arhivēta izvade'.</span><span class="sxs-lookup"><span data-stu-id="660c6-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="660c6-129">Pievienojiet pielikumus veidošanas arhivētajam failam kā failus ar sākotnējiem nosaukumiem un paplašinājumiem.</span><span class="sxs-lookup"><span data-stu-id="660c6-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="660c6-130">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="660c6-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="660c6-131">Kokā atlasiet "Vispārīgi\Fails".</span><span class="sxs-lookup"><span data-stu-id="660c6-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="660c6-132">Laukā Nosaukums, ierakstiet 'Pievienotais fails'.</span><span class="sxs-lookup"><span data-stu-id="660c6-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="660c6-133">Pievienotais fails</span><span class="sxs-lookup"><span data-stu-id="660c6-133">Attached file</span></span>  
19. <span data-ttu-id="660c6-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="660c6-134">Click OK.</span></span>
20. <span data-ttu-id="660c6-135">Kokā atlasiet 'Arhivēta izvade\Pievienotais fails'.</span><span class="sxs-lookup"><span data-stu-id="660c6-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="660c6-136">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="660c6-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="660c6-137">Koka struktūrā atlasiet 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="660c6-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="660c6-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="660c6-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="660c6-139">Kartējiet jaunus formatēšanas elementus datu modelī</span><span class="sxs-lookup"><span data-stu-id="660c6-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="660c6-140">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="660c6-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="660c6-141">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="660c6-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="660c6-142">Koka struktūrā izvērsiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="660c6-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="660c6-143">Kokā atlasiet 'Arhivēta izvade\Pievienotais fails\Base64'.</span><span class="sxs-lookup"><span data-stu-id="660c6-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="660c6-144">Koka struktūrā atlasiet 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="660c6-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="660c6-145">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="660c6-145">Click Bind.</span></span>
7. <span data-ttu-id="660c6-146">Kokā atlasiet 'Arhivēta izvade\Pievienotais fails'.</span><span class="sxs-lookup"><span data-stu-id="660c6-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="660c6-147">Noklikšķiniet uz rediģēt faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="660c6-147">Click Edit filename.</span></span>
9. <span data-ttu-id="660c6-148">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="660c6-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="660c6-149">Koka struktūrā izvērsiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="660c6-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="660c6-150">Koka struktūrā atlasiet 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="660c6-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="660c6-151">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="660c6-151">Click Add data source.</span></span>
13. <span data-ttu-id="660c6-152">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="660c6-152">Click Save.</span></span>
14. <span data-ttu-id="660c6-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="660c6-153">Close the page.</span></span>
15. <span data-ttu-id="660c6-154">Koka struktūrā atlasiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="660c6-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="660c6-155">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="660c6-155">Click Bind.</span></span>
17. <span data-ttu-id="660c6-156">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="660c6-156">Click Save.</span></span>
18. <span data-ttu-id="660c6-157">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="660c6-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="660c6-158">Atlasītajam rēķinam noformētas atskaites palaišana</span><span class="sxs-lookup"><span data-stu-id="660c6-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="660c6-159">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="660c6-159">Click Run.</span></span>
2. <span data-ttu-id="660c6-160">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="660c6-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="660c6-161">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="660c6-161">Click Filter.</span></span>
4. <span data-ttu-id="660c6-162">Atlasiet rindu no debitora rēķinu žurnāla un pārdošanas pasūtījuma lauka.</span><span class="sxs-lookup"><span data-stu-id="660c6-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="660c6-163">Laukā Kritēriji, kritērija “pārdošanas pasūtījums' laukā ierakstiet pasūtījuma numuru 000148.</span><span class="sxs-lookup"><span data-stu-id="660c6-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="660c6-164">000148</span><span class="sxs-lookup"><span data-stu-id="660c6-164">000148</span></span>  
6. <span data-ttu-id="660c6-165">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="660c6-165">Click OK.</span></span>
7. <span data-ttu-id="660c6-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="660c6-166">Click OK.</span></span>
    * <span data-ttu-id="660c6-167">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="660c6-167">Review the generated output.</span></span> <span data-ttu-id="660c6-168">Ņemiet vērā, ka papildus rēķina ziņojumam XML formātā, viens fails tika izveidots katram pielikumam.</span><span class="sxs-lookup"><span data-stu-id="660c6-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="660c6-169">Pielikumu faili tiek aizpildīti ar arhivētu izvadi binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="660c6-169">The attachment files are populated with the zipped output in binary format.</span></span>  


