--- 
title: "Palaist formātu dokumentu pārvaldības failu lietošanai formāta izvades datos elektronisko pārskatu veidošanai (ER)"
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
ms.openlocfilehash: 09eaf28b0f4ed93d602f84688369614c17502d95
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="73e05-103">Palaist formātu dokumentu pārvaldības failu lietošanai formāta izvades datos elektronisko pārskatu veidošanai (ER)</span><span class="sxs-lookup"><span data-stu-id="73e05-103">Run format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73e05-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="73e05-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="73e05-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="73e05-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="73e05-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā “ER Izmantot dokumentu pārvaldības failus formāta izvadē (3. daļa: Izveidot formātu)”.</span><span class="sxs-lookup"><span data-stu-id="73e05-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="73e05-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="73e05-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="73e05-108">Pievienojiet viena rēķina nepieciešamos pielikumus pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="73e05-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="73e05-109">Pārejiet uz sadaļu Debitori > Rēķini > Atvērtie debitoru rēķini.</span><span class="sxs-lookup"><span data-stu-id="73e05-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="73e05-110">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="73e05-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="73e05-111">Piemēram, filtrējiet lauku Rēķins ar vērtību 'CIV-000148'.</span><span class="sxs-lookup"><span data-stu-id="73e05-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="73e05-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="73e05-112">CIV-000148</span></span>  
3. <span data-ttu-id="73e05-113">Noklikšķiniet, lai atvērtu atlasīto rēķina saiti.</span><span class="sxs-lookup"><span data-stu-id="73e05-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="73e05-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="73e05-114">CIV-000148</span></span>  
4. <span data-ttu-id="73e05-115">Noklikšķiniet, lai atvērtu saiti laukā Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="73e05-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="73e05-116">000148</span><span class="sxs-lookup"><span data-stu-id="73e05-116">000148</span></span>  
5. <span data-ttu-id="73e05-117">Laukā rindas vai virsrakstw, atlasiet Virsraksta opciju.</span><span class="sxs-lookup"><span data-stu-id="73e05-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="73e05-118">Atlasiet Virsraksts, lai norādītu, ka šis ir pielikumu pievienošanas mērķis.</span><span class="sxs-lookup"><span data-stu-id="73e05-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="73e05-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="73e05-119">Click Attach.</span></span>
    * <span data-ttu-id="73e05-120">Pievienojiet šim pārdošanas pasūtījumam dažus failus kā pielikumus.</span><span class="sxs-lookup"><span data-stu-id="73e05-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="73e05-121">Izmantojiet tādu dokumentu tipu failus, ko atbalsta dokumentu pārvaldība (ar faila paplašinājumu DOCX, DPF, XML, JPG u. c.).</span><span class="sxs-lookup"><span data-stu-id="73e05-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="73e05-122">Pārlūkojiet un atlasiet failus, kas jāpievieno un papildus jāapstrādā kopā ar attiecīgo rēķinu ER elektroniskajā ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="73e05-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="73e05-123">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="73e05-123">Click New.</span></span>
8. <span data-ttu-id="73e05-124">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="73e05-124">Click File.</span></span>
9. <span data-ttu-id="73e05-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="73e05-125">Click New.</span></span>
10. <span data-ttu-id="73e05-126">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="73e05-126">Click File.</span></span>
11. <span data-ttu-id="73e05-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="73e05-127">Close the page.</span></span>
12. <span data-ttu-id="73e05-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="73e05-128">Close the page.</span></span>
13. <span data-ttu-id="73e05-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="73e05-129">Close the page.</span></span>
14. <span data-ttu-id="73e05-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="73e05-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="73e05-131">Atlasītajam rēķinam noformētas atskaites palaišana</span><span class="sxs-lookup"><span data-stu-id="73e05-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="73e05-132">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="73e05-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="73e05-133">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="73e05-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="73e05-134">Kokā izvērsiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)".</span><span class="sxs-lookup"><span data-stu-id="73e05-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="73e05-135">Kokā atlasiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)\Elektronisks rēķina parauga ziņojums".</span><span class="sxs-lookup"><span data-stu-id="73e05-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="73e05-136">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="73e05-136">Click Run.</span></span>
6. <span data-ttu-id="73e05-137">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="73e05-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="73e05-138">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="73e05-138">Click Filter.</span></span>
8. <span data-ttu-id="73e05-139">Atlasiet rindu no debitora rēķinu žurnāla un pārdošanas pasūtījuma lauka.</span><span class="sxs-lookup"><span data-stu-id="73e05-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="73e05-140">Laukā Kritēriji ierakstiet '000148'.</span><span class="sxs-lookup"><span data-stu-id="73e05-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="73e05-141">Kritērija laukā “Pārdošanas pasūtījums” ierakstiet pasūtījuma numuru 000148.</span><span class="sxs-lookup"><span data-stu-id="73e05-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="73e05-142">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="73e05-142">Click OK.</span></span>
11. <span data-ttu-id="73e05-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="73e05-143">Click OK.</span></span>
    * <span data-ttu-id="73e05-144">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="73e05-144">Review the generated output.</span></span> <span data-ttu-id="73e05-145">Ņemiet vērā, ka katram pielikumam ir izveidots atsevišķs XML mezgls.</span><span class="sxs-lookup"><span data-stu-id="73e05-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="73e05-146">Pielikuma saturs tiek aizpildīts XML izvadē MIME (base64) teksta formātā.</span><span class="sxs-lookup"><span data-stu-id="73e05-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  


