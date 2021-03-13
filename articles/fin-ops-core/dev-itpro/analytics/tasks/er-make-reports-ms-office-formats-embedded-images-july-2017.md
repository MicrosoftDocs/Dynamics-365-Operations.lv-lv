---
title: Konfigurāciju noformēšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli
description: Šajā tēmā paskaidrots, kā izstrādāt konfigurācijas, kas ģenerē elektronisko pārskatu dokumentus Excel un Word formātos, kas satur ģenerētu iegultus attēlus.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b60ed6b07851c44ceb4b8f313bc65f04b802e646
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093674"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="f3c14-103">Konfigurāciju noformēšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli</span><span class="sxs-lookup"><span data-stu-id="f3c14-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3c14-104">Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūru "ER konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu."</span><span class="sxs-lookup"><span data-stu-id="f3c14-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="f3c14-105">Šīs procedūrās aprakstā ir paskaidrots, kā izstrādāt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurācijas, lai ģenerētu iegultus attēlus saturošus Microsoft Excel vai Word dokumentus.</span><span class="sxs-lookup"><span data-stu-id="f3c14-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="f3c14-106">Šajā procedūrā izveidosit nepieciešamās ER konfigurācijas parauga uzņēmumam Litware, Inc. Šīs darbības var izpildīt, izmantojot USMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="f3c14-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="f3c14-107">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="f3c14-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="f3c14-108">Pirms sākat, lejupielādējiet un saglabājiet failus, kas uzskaitīti palīdzības tēmā [Attēlu un formu iegulšana dokumentos, kuri tiek ģenerēti, izmantojot EP](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="f3c14-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="f3c14-109">Šie faili ir: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png un Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="f3c14-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="f3c14-110">pārbaudiet priekšnoteikumus;</span><span class="sxs-lookup"><span data-stu-id="f3c14-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="f3c14-111">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="f3c14-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="f3c14-112">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="f3c14-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="f3c14-113">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".</span><span class="sxs-lookup"><span data-stu-id="f3c14-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="f3c14-114">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="f3c14-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="f3c14-115">Pievienot jaunu ER modeļa konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="f3c14-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="f3c14-116">Tā vietā, lai izveidotu jaunu modeli, varat ielādēt ER modeļa konfigurācijas failu (Model for cheques.xml), kuru saglabājāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="f3c14-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="f3c14-117">Šis fails satur parauga datu modeli maksājumu čekiem un datu modeļa kartējumu uz programmas Dynamics 365 for Operations datu komponentiem.</span><span class="sxs-lookup"><span data-stu-id="f3c14-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="f3c14-118">Kopsavilkuma cilnē Versijas noklikšķiniet uz Mainīt.</span><span class="sxs-lookup"><span data-stu-id="f3c14-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="f3c14-119">Noklikšķiniet uz Ielādēt no XML faila.</span><span class="sxs-lookup"><span data-stu-id="f3c14-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="f3c14-120">Noklikšķiniet uz Pārlūkot un pēc tam atlasiet Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="f3c14-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="f3c14-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f3c14-121">Click OK.</span></span>  
 6. <span data-ttu-id="f3c14-122">Ielādētais modelis tiks izmantots kā datu avots informācijai, lai ģenerētu dokumentus, kuros ir attēli, programmā Excel un Word.</span><span class="sxs-lookup"><span data-stu-id="f3c14-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="f3c14-123">Jaunas ER formāta konfigurācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="f3c14-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="f3c14-124">Tā vietā, lai izveidotu jaunu formātu, varat ielādēt ER formāta konfigurācijas failu (Cheques printing format.xml), kuru saglabājāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="f3c14-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="f3c14-125">Šis fails satur formāta parauga izkārtojumu, lai izdrukātu čekus, izmantojot iepriekš izdrukātu formu un šī formāta kartējumu uz datu modeli 'Čeku modelis'.</span><span class="sxs-lookup"><span data-stu-id="f3c14-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="f3c14-126">Noklikšķiniet uz Mainīt.</span><span class="sxs-lookup"><span data-stu-id="f3c14-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="f3c14-127">Noklikšķiniet uz Ielādēt no XML faila.</span><span class="sxs-lookup"><span data-stu-id="f3c14-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="f3c14-128">Noklikšķiniet uz Pārlūkot un atlasiet failu Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="f3c14-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="f3c14-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f3c14-129">Click OK.</span></span>  
 6. <span data-ttu-id="f3c14-130">Koka struktūrā izvērsiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="f3c14-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="f3c14-131">Kokā atlasiet 'Model for cheques\Cheques printing format'.</span><span class="sxs-lookup"><span data-stu-id="f3c14-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="f3c14-132">Ielādētais formāts tiks izmantots, lai ģenerētu dokumentus, kuros ir attēli, programmā Excel un Word.</span><span class="sxs-lookup"><span data-stu-id="f3c14-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="f3c14-133">ER lietotāju parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="f3c14-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="f3c14-134">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="f3c14-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="f3c14-135">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="f3c14-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="f3c14-136">Laukā Palaist iestatījumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="f3c14-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="f3c14-137">Ieslēdziet karodziņu 'Palaist melnrakstu', lai startētu atlasītā formāta melnraksta versiju, nevis pabeigto.</span><span class="sxs-lookup"><span data-stu-id="f3c14-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="f3c14-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f3c14-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="f3c14-139">Kases un bankas vadības parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="f3c14-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="f3c14-140">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="f3c14-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="f3c14-141">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="f3c14-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="f3c14-142">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="f3c14-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="f3c14-143">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="f3c14-143">Click Check.</span></span>  
 5. <span data-ttu-id="f3c14-144">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="f3c14-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="f3c14-145">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="f3c14-145">Click Edit.</span></span>  
 7. <span data-ttu-id="f3c14-146">Laukā Uzņēmuma logotips atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="f3c14-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="f3c14-147">Noklikšķiniet uz Uzņēmuma logotips.</span><span class="sxs-lookup"><span data-stu-id="f3c14-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="f3c14-148">Noklikšķiniet uz Mainīt.</span><span class="sxs-lookup"><span data-stu-id="f3c14-148">Click Change.</span></span>  
 10. <span data-ttu-id="f3c14-149">Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="f3c14-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="f3c14-150">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f3c14-150">Click Save.</span></span>  
 12. <span data-ttu-id="f3c14-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f3c14-151">Close the page.</span></span>  
 13. <span data-ttu-id="f3c14-152">Izvērsiet sadaļu Paraksts.</span><span class="sxs-lookup"><span data-stu-id="f3c14-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="f3c14-153">Laukā Drukāt pirmo parakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="f3c14-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="f3c14-154">Noklikšķiniet uz Mainīt.</span><span class="sxs-lookup"><span data-stu-id="f3c14-154">Click Change.</span></span>  
 16. <span data-ttu-id="f3c14-155">Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="f3c14-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="f3c14-156">Izvērsiet sadaļu Kopijas.</span><span class="sxs-lookup"><span data-stu-id="f3c14-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="f3c14-157">Laukā Ūdenszīme atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="f3c14-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="f3c14-158">Laukā Vispārīgs elektroniskās eksportēšanas formāts atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="f3c14-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="f3c14-159">Atlasiet konfigurāciju “Čeku drukāšanas forma”.</span><span class="sxs-lookup"><span data-stu-id="f3c14-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="f3c14-160">Tagad atlasītais ER formāts tiks izmantots čeku drukāšanai.</span><span class="sxs-lookup"><span data-stu-id="f3c14-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="f3c14-161">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="f3c14-161">Click Attach.</span></span>  
 23. <span data-ttu-id="f3c14-162">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f3c14-162">Click New.</span></span>  
 24. <span data-ttu-id="f3c14-163">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="f3c14-163">Click File.</span></span>  
 25. <span data-ttu-id="f3c14-164">Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="f3c14-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="f3c14-165">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f3c14-165">Close the page.</span></span>  
 27. <span data-ttu-id="f3c14-166">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f3c14-166">Close the page.</span></span>  
 28. <span data-ttu-id="f3c14-167">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f3c14-167">Close the page.</span></span>  
 29. <span data-ttu-id="f3c14-168">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="f3c14-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="f3c14-169">Laukā Atļaut darījuma pārbaudes izveidi neaktīviem bankas kontiem atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="f3c14-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="f3c14-170">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f3c14-170">Click Save.</span></span>  
 32. <span data-ttu-id="f3c14-171">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f3c14-171">Close the page.</span></span>  
