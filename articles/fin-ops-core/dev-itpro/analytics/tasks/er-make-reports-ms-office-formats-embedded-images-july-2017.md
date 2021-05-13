---
title: Konfigurāciju noformēšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli
description: Šajā tēmā paskaidrots, kā izstrādāt konfigurācijas, kas ģenerē elektronisko pārskatu dokumentus Excel un Word formātos, kas satur ģenerētu iegultus attēlus.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944561"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="c0bf3-103">Konfigurāciju noformēšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli</span><span class="sxs-lookup"><span data-stu-id="c0bf3-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0bf3-104">Lai izpildītu šīs procedūras darbības, vispirms izpildiet procedūru "ER konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu."</span><span class="sxs-lookup"><span data-stu-id="c0bf3-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="c0bf3-105">Šīs procedūrās aprakstā ir paskaidrots, kā izstrādāt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurācijas, lai ģenerētu iegultus attēlus saturošus Microsoft Excel vai Word dokumentus.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="c0bf3-106">Šajā procedūrā izveidosit nepieciešamās ER konfigurācijas parauga uzņēmumam Litware, Inc. Šīs darbības var izpildīt, izmantojot USMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="c0bf3-107">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c0bf3-108">Pirms sākšanas, lejupielādējiet un saglabājiet tālāk norādītos failus:</span><span class="sxs-lookup"><span data-stu-id="c0bf3-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="c0bf3-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c0bf3-109">Description</span></span>                                          | <span data-ttu-id="c0bf3-110">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="c0bf3-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="c0bf3-111">ER datu modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="c0bf3-111">ER data model configuration</span></span>                          | [<span data-ttu-id="c0bf3-112">cheques.xml modelis</span><span class="sxs-lookup"><span data-stu-id="c0bf3-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="c0bf3-113">ER formāta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="c0bf3-113">ER format configuration</span></span>                              | [<span data-ttu-id="c0bf3-114">Čeku drukāšanas formāts.xml</span><span class="sxs-lookup"><span data-stu-id="c0bf3-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="c0bf3-115">Uzņēmuma logo attēls</span><span class="sxs-lookup"><span data-stu-id="c0bf3-115">Company logo image</span></span>                                   | [<span data-ttu-id="c0bf3-116">Uzņēmuma logo.png</span><span class="sxs-lookup"><span data-stu-id="c0bf3-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="c0bf3-117">Paraksta attēls</span><span class="sxs-lookup"><span data-stu-id="c0bf3-117">Signature image</span></span>                                      | [<span data-ttu-id="c0bf3-118">Paraksta attēls.png</span><span class="sxs-lookup"><span data-stu-id="c0bf3-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="c0bf3-119">Alternatīva paraksta attēls</span><span class="sxs-lookup"><span data-stu-id="c0bf3-119">Alternative signature image</span></span>                          | [<span data-ttu-id="c0bf3-120">Paraksta attēls 2.png</span><span class="sxs-lookup"><span data-stu-id="c0bf3-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="c0bf3-121">Microsoft Word veidne maksājumu čeku drukāšanai</span><span class="sxs-lookup"><span data-stu-id="c0bf3-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="c0bf3-122">Čeka veidne Word.docx</span><span class="sxs-lookup"><span data-stu-id="c0bf3-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="c0bf3-123">pārbaudiet priekšnoteikumus;</span><span class="sxs-lookup"><span data-stu-id="c0bf3-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="c0bf3-124">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="c0bf3-125">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="c0bf3-126">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā "Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu".</span><span class="sxs-lookup"><span data-stu-id="c0bf3-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="c0bf3-127">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="c0bf3-128">Pievienot jaunu ER modeļa konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="c0bf3-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="c0bf3-129">Tā vietā, lai izveidotu jaunu modeli, varat ielādēt ER modeļa konfigurācijas failu (Model for cheques.xml), kuru saglabājāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="c0bf3-130">Šis fails satur parauga datu modeli maksājumu čekiem un datu modeļa kartējumu uz programmas Dynamics 365 for Operations datu komponentiem.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="c0bf3-131">Kopsavilkuma cilnē Versijas noklikšķiniet uz Mainīt.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="c0bf3-132">Noklikšķiniet uz Ielādēt no XML faila.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c0bf3-133">Noklikšķiniet uz Pārlūkot un pēc tam atlasiet Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="c0bf3-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-134">Click OK.</span></span>  
 6. <span data-ttu-id="c0bf3-135">Ielādētais modelis tiks izmantots kā datu avots informācijai, lai ģenerētu dokumentus, kuros ir attēli, programmā Excel un Word.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="c0bf3-136">Jaunas ER formāta konfigurācijas pievienošana</span><span class="sxs-lookup"><span data-stu-id="c0bf3-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="c0bf3-137">Tā vietā, lai izveidotu jaunu formātu, varat ielādēt ER formāta konfigurācijas failu (Cheques printing format.xml), kuru saglabājāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="c0bf3-138">Šis fails satur formāta parauga izkārtojumu, lai izdrukātu čekus, izmantojot iepriekš izdrukātu formu un šī formāta kartējumu uz datu modeli 'Čeku modelis'.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="c0bf3-139">Noklikšķiniet uz Mainīt.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="c0bf3-140">Noklikšķiniet uz Ielādēt no XML faila.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="c0bf3-141">Noklikšķiniet uz Pārlūkot un atlasiet failu Cheques printing format.xml.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="c0bf3-142">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-142">Click OK.</span></span>  
 6. <span data-ttu-id="c0bf3-143">Koka struktūrā izvērsiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="c0bf3-144">Kokā atlasiet 'Model for cheques\Cheques printing format'.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="c0bf3-145">Ielādētais formāts tiks izmantots, lai ģenerētu dokumentus, kuros ir attēli, programmā Excel un Word.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="c0bf3-146">ER lietotāju parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c0bf3-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="c0bf3-147">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="c0bf3-148">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="c0bf3-149">Laukā Palaist iestatījumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="c0bf3-150">Ieslēdziet karodziņu 'Palaist melnrakstu', lai startētu atlasītā formāta melnraksta versiju, nevis pabeigto.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="c0bf3-151">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="c0bf3-152">Kases un bankas vadības parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c0bf3-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="c0bf3-153">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="c0bf3-154">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="c0bf3-155">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="c0bf3-156">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-156">Click Check.</span></span>  
 5. <span data-ttu-id="c0bf3-157">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="c0bf3-158">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-158">Click Edit.</span></span>  
 7. <span data-ttu-id="c0bf3-159">Laukā Uzņēmuma logotips atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="c0bf3-160">Noklikšķiniet uz Uzņēmuma logotips.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="c0bf3-161">Noklikšķiniet uz Mainīt.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-161">Click Change.</span></span>  
 10. <span data-ttu-id="c0bf3-162">Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="c0bf3-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-163">Click Save.</span></span>  
 12. <span data-ttu-id="c0bf3-164">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-164">Close the page.</span></span>  
 13. <span data-ttu-id="c0bf3-165">Izvērsiet sadaļu Paraksts.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="c0bf3-166">Laukā Drukāt pirmo parakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="c0bf3-167">Noklikšķiniet uz Mainīt.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-167">Click Change.</span></span>  
 16. <span data-ttu-id="c0bf3-168">Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="c0bf3-169">Izvērsiet sadaļu Kopijas.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="c0bf3-170">Laukā Ūdenszīme atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="c0bf3-171">Laukā Vispārīgs elektroniskās eksportēšanas formāts atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="c0bf3-172">Atlasiet konfigurāciju “Čeku drukāšanas forma”.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="c0bf3-173">Tagad atlasītais ER formāts tiks izmantots čeku drukāšanai.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="c0bf3-174">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-174">Click Attach.</span></span>  
 23. <span data-ttu-id="c0bf3-175">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-175">Click New.</span></span>  
 24. <span data-ttu-id="c0bf3-176">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-176">Click File.</span></span>  
 25. <span data-ttu-id="c0bf3-177">Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="c0bf3-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-178">Close the page.</span></span>  
 27. <span data-ttu-id="c0bf3-179">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-179">Close the page.</span></span>  
 28. <span data-ttu-id="c0bf3-180">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-180">Close the page.</span></span>  
 29. <span data-ttu-id="c0bf3-181">Pārejiet uz sadaļu Kases un bankas pārvaldība > Iestatījumi > Kases un bankas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="c0bf3-182">Laukā Atļaut darījuma pārbaudes izveidi neaktīviem bankas kontiem atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="c0bf3-183">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-183">Click Save.</span></span>  
 32. <span data-ttu-id="c0bf3-184">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="c0bf3-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
