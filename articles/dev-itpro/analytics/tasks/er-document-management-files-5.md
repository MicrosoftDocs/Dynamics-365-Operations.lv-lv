---
title: ER dokumentu pārvaldības faili, ko izmanto formāta izvades datos (5. daļa. Formāta modificēšana un darbināšana)
description: Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23e91b6aee62157da9141cc7b6c4fae39c19ce32
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544683"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5-modify-and-run-format"></a><span data-ttu-id="d88b1-103">ER izmantot dokumentu pārvaldības failus formātu izvades datos (5. daļa: Modificēt un palaist formātu)</span><span class="sxs-lookup"><span data-stu-id="d88b1-103">ER Use Document Management files in format outputs (Part 5: Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d88b1-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="d88b1-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="d88b1-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="d88b1-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="d88b1-106">Lai veiktu šīs darbības, vispirms pabeidziet darbības procedūrā "ER izmantot dokumentu pārvaldības failus formāta izvadēs (4. daļa): Formatēšanas izpilde".</span><span class="sxs-lookup"><span data-stu-id="d88b1-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="d88b1-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="d88b1-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="d88b1-108">Modificējiet formātu, lai aizpildītu pielikumus, ģenerējot ziņojumus binārā formātā</span><span class="sxs-lookup"><span data-stu-id="d88b1-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="d88b1-109">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="d88b1-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d88b1-110">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="d88b1-111">Kokā izvērsiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)".</span><span class="sxs-lookup"><span data-stu-id="d88b1-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="d88b1-112">Kokā atlasiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)\Elektronisks rēķina parauga ziņojums".</span><span class="sxs-lookup"><span data-stu-id="d88b1-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="d88b1-113">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="d88b1-113">Click Designer.</span></span>
    * <span data-ttu-id="d88b1-114">Jūs aizpildīsiet rēķina ziņojumu, veidojot ražojumu kā XML failu, izmantojot unikoda kodējumu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="d88b1-115">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="d88b1-116">Kokā atlasiet "Vispārīgi\Fails".</span><span class="sxs-lookup"><span data-stu-id="d88b1-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="d88b1-117">Laukā Nosaukums ierakstiet 'Xml ziņojums'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="d88b1-118">Xml ziņojums</span><span class="sxs-lookup"><span data-stu-id="d88b1-118">Xml message</span></span>  
9. <span data-ttu-id="d88b1-119">Laukā Kodēšana ierakstiet "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="d88b1-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="d88b1-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="d88b1-120">UTF-8</span></span>  
10. <span data-ttu-id="d88b1-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d88b1-121">Click OK.</span></span>
    * <span data-ttu-id="d88b1-122">Konfigurējiet ražojuma veidošanu kā arhivēto failu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="d88b1-123">Noklikšķiniet uz Pievienot sakni, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="d88b1-124">Kokā atlasiet "Vispārīgi\Mape".</span><span class="sxs-lookup"><span data-stu-id="d88b1-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="d88b1-125">Laukā Nosaukums ierakstiet 'Arhivēta izvade.</span><span class="sxs-lookup"><span data-stu-id="d88b1-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="d88b1-126">Zip izvade</span><span class="sxs-lookup"><span data-stu-id="d88b1-126">Zip output</span></span>  
14. <span data-ttu-id="d88b1-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d88b1-127">Click OK.</span></span>
15. <span data-ttu-id="d88b1-128">Kokā atlasiet 'Arhivēta izvade'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="d88b1-129">Pievienojiet pielikumus veidošanas arhivētajam failam kā failus ar sākotnējiem nosaukumiem un paplašinājumiem.</span><span class="sxs-lookup"><span data-stu-id="d88b1-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="d88b1-130">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="d88b1-131">Kokā atlasiet "Vispārīgi\Fails".</span><span class="sxs-lookup"><span data-stu-id="d88b1-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="d88b1-132">Laukā Nosaukums, ierakstiet 'Pievienotais fails'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="d88b1-133">Pievienotais fails</span><span class="sxs-lookup"><span data-stu-id="d88b1-133">Attached file</span></span>  
19. <span data-ttu-id="d88b1-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d88b1-134">Click OK.</span></span>
20. <span data-ttu-id="d88b1-135">Kokā atlasiet 'Arhivēta izvade\Pievienotais fails'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="d88b1-136">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="d88b1-137">Koka struktūrā atlasiet 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="d88b1-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d88b1-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="d88b1-139">Kartējiet jaunus formatēšanas elementus datu modelī</span><span class="sxs-lookup"><span data-stu-id="d88b1-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="d88b1-140">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="d88b1-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="d88b1-141">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="d88b1-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="d88b1-142">Koka struktūrā izvērsiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="d88b1-143">Kokā atlasiet 'Arhivēta izvade\Pievienotais fails\Base64'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="d88b1-144">Koka struktūrā atlasiet 'model\Invoice attachments\File content'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="d88b1-145">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="d88b1-145">Click Bind.</span></span>
7. <span data-ttu-id="d88b1-146">Kokā atlasiet 'Arhivēta izvade\Pievienotais fails'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="d88b1-147">Noklikšķiniet uz rediģēt faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-147">Click Edit filename.</span></span>
9. <span data-ttu-id="d88b1-148">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="d88b1-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="d88b1-149">Koka struktūrā izvērsiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="d88b1-150">Koka struktūrā atlasiet 'model\Invoice attachments\File name'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="d88b1-151">Noklikšķiniet uz Pievienot datu avotu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-151">Click Add data source.</span></span>
13. <span data-ttu-id="d88b1-152">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d88b1-152">Click Save.</span></span>
14. <span data-ttu-id="d88b1-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-153">Close the page.</span></span>
15. <span data-ttu-id="d88b1-154">Koka struktūrā atlasiet 'model\Invoice attachments'.</span><span class="sxs-lookup"><span data-stu-id="d88b1-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="d88b1-155">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="d88b1-155">Click Bind.</span></span>
17. <span data-ttu-id="d88b1-156">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d88b1-156">Click Save.</span></span>
18. <span data-ttu-id="d88b1-157">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d88b1-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="d88b1-158">Atlasītajam rēķinam noformētas atskaites palaišana</span><span class="sxs-lookup"><span data-stu-id="d88b1-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="d88b1-159">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="d88b1-159">Click Run.</span></span>
2. <span data-ttu-id="d88b1-160">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="d88b1-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="d88b1-161">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="d88b1-161">Click Filter.</span></span>
4. <span data-ttu-id="d88b1-162">Atlasiet rindu no debitora rēķinu žurnāla un pārdošanas pasūtījuma lauka.</span><span class="sxs-lookup"><span data-stu-id="d88b1-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="d88b1-163">Laukā Kritēriji, kritērija “pārdošanas pasūtījums' laukā ierakstiet pasūtījuma numuru 000148.</span><span class="sxs-lookup"><span data-stu-id="d88b1-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="d88b1-164">000148</span><span class="sxs-lookup"><span data-stu-id="d88b1-164">000148</span></span>  
6. <span data-ttu-id="d88b1-165">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d88b1-165">Click OK.</span></span>
7. <span data-ttu-id="d88b1-166">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d88b1-166">Click OK.</span></span>
    * <span data-ttu-id="d88b1-167">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d88b1-167">Review the generated output.</span></span> <span data-ttu-id="d88b1-168">Ņemiet vērā, ka papildus rēķina ziņojumam XML formātā, viens fails tika izveidots katram pielikumam.</span><span class="sxs-lookup"><span data-stu-id="d88b1-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="d88b1-169">Pielikumu faili tiek aizpildīti ar arhivētu izvadi binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="d88b1-169">The attachment files are populated with the zipped output in binary format.</span></span>  

