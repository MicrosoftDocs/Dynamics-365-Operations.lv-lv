---
title: Formātu izpilde, lai dokumentu pārvaldības failus lietotu ER izvadē
description: Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus ER izvadē.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8dc541af4d26b61ff9b90e08a8ca2c6a6bb8e70
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850259"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4-run-format"></a><span data-ttu-id="a6fcb-103">ER izmantot dokumentu pārvaldības failus formātu izvades datos (4. daļa: Palaist formātu)</span><span class="sxs-lookup"><span data-stu-id="a6fcb-103">ER Use Document Management files in format outputs (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a6fcb-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="a6fcb-105">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a6fcb-106">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā “ER Izmantot dokumentu pārvaldības failus formāta izvadē (3. daļa: Izveidot formātu)”.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="a6fcb-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="a6fcb-108">Pievienojiet viena rēķina nepieciešamos pielikumus pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="a6fcb-109">Pārejiet uz sadaļu Debitori > Rēķini > Atvērtie debitoru rēķini.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="a6fcb-110">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a6fcb-111">Piemēram, filtrējiet lauku Rēķins ar vērtību 'CIV-000148'.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="a6fcb-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="a6fcb-112">CIV-000148</span></span>  
3. <span data-ttu-id="a6fcb-113">Noklikšķiniet, lai atvērtu atlasīto rēķina saiti.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="a6fcb-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="a6fcb-114">CIV-000148</span></span>  
4. <span data-ttu-id="a6fcb-115">Noklikšķiniet, lai atvērtu saiti laukā Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="a6fcb-116">000148</span><span class="sxs-lookup"><span data-stu-id="a6fcb-116">000148</span></span>  
5. <span data-ttu-id="a6fcb-117">Laukā rindas vai virsrakstw, atlasiet Virsraksta opciju.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="a6fcb-118">Atlasiet Virsraksts, lai norādītu, ka šis ir pielikumu pievienošanas mērķis.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="a6fcb-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-119">Click Attach.</span></span>
    * <span data-ttu-id="a6fcb-120">Pievienojiet šim pārdošanas pasūtījumam dažus failus kā pielikumus.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="a6fcb-121">Izmantojiet tādu dokumentu tipu failus, ko atbalsta dokumentu pārvaldība (ar faila paplašinājumu DOCX, DPF, XML, JPG u. c.).</span><span class="sxs-lookup"><span data-stu-id="a6fcb-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="a6fcb-122">Pārlūkojiet un atlasiet failus, kas jāpievieno un papildus jāapstrādā kopā ar attiecīgo rēķinu ER elektroniskajā ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="a6fcb-123">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-123">Click New.</span></span>
8. <span data-ttu-id="a6fcb-124">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-124">Click File.</span></span>
9. <span data-ttu-id="a6fcb-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-125">Click New.</span></span>
10. <span data-ttu-id="a6fcb-126">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-126">Click File.</span></span>
11. <span data-ttu-id="a6fcb-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-127">Close the page.</span></span>
12. <span data-ttu-id="a6fcb-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-128">Close the page.</span></span>
13. <span data-ttu-id="a6fcb-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-129">Close the page.</span></span>
14. <span data-ttu-id="a6fcb-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="a6fcb-131">Atlasītajam rēķinam noformētas atskaites palaišana</span><span class="sxs-lookup"><span data-stu-id="a6fcb-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="a6fcb-132">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a6fcb-133">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="a6fcb-134">Kokā izvērsiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)".</span><span class="sxs-lookup"><span data-stu-id="a6fcb-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="a6fcb-135">Kokā atlasiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)\Elektronisks rēķina parauga ziņojums".</span><span class="sxs-lookup"><span data-stu-id="a6fcb-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="a6fcb-136">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-136">Click Run.</span></span>
6. <span data-ttu-id="a6fcb-137">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="a6fcb-138">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-138">Click Filter.</span></span>
8. <span data-ttu-id="a6fcb-139">Atlasiet rindu no debitora rēķinu žurnāla un pārdošanas pasūtījuma lauka.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="a6fcb-140">Laukā Kritēriji ierakstiet '000148'.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="a6fcb-141">Kritērija laukā “Pārdošanas pasūtījums” ierakstiet pasūtījuma numuru 000148.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="a6fcb-142">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-142">Click OK.</span></span>
11. <span data-ttu-id="a6fcb-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-143">Click OK.</span></span>
    * <span data-ttu-id="a6fcb-144">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-144">Review the generated output.</span></span> <span data-ttu-id="a6fcb-145">Ņemiet vērā, ka katram pielikumam ir izveidots atsevišķs XML mezgls.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="a6fcb-146">Pielikuma saturs tiek aizpildīts XML izvadē MIME (base64) teksta formātā.</span><span class="sxs-lookup"><span data-stu-id="a6fcb-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  

