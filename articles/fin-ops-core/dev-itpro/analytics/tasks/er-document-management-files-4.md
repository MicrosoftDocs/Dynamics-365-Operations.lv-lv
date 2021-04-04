---
title: ER izmantot dokumentu pārvaldības failus formātu izvades datos (4. daļa - Palaist formātu)
description: Šajā tēmā ir aprakstīts, kā konfigurēt elektronisko pārskatu (ER) formātu dokumentu pārvaldības failu (pielikumu) izmantošanai ER izvadē. (4. daļa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ede71118f64eec27b150a4c575aead97d3174509
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559729"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="df4bc-104">ER izmantot dokumentu pārvaldības failus formātu izvades datos (4. daļa - Palaist formātu)</span><span class="sxs-lookup"><span data-stu-id="df4bc-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df4bc-105">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="df4bc-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="df4bc-106">Šīs darbības var veikt uzņēmumā DEMF.</span><span class="sxs-lookup"><span data-stu-id="df4bc-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="df4bc-107">Lai izpildītu šos soļus, vispirms ir jāpabeidz soļi, kas aprakstīti procedūrā "ER Izmantot dokumentu pārvaldības failus formāta izvadē (3. daļa: Izveidot formātu)".</span><span class="sxs-lookup"><span data-stu-id="df4bc-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="df4bc-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="df4bc-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="df4bc-109">Pievienojiet viena rēķina nepieciešamos pielikumus pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="df4bc-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="df4bc-110">Pārejiet uz sadaļu Debitori > Rēķini > Atvērtie debitoru rēķini.</span><span class="sxs-lookup"><span data-stu-id="df4bc-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="df4bc-111">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="df4bc-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="df4bc-112">Piemēram, filtrējiet lauku Rēķins ar vērtību 'CIV-000148'.</span><span class="sxs-lookup"><span data-stu-id="df4bc-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="df4bc-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="df4bc-113">CIV-000148</span></span>  
3. <span data-ttu-id="df4bc-114">Noklikšķiniet, lai atvērtu atlasīto rēķina saiti.</span><span class="sxs-lookup"><span data-stu-id="df4bc-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="df4bc-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="df4bc-115">CIV-000148</span></span>  
4. <span data-ttu-id="df4bc-116">Noklikšķiniet, lai atvērtu saiti laukā Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="df4bc-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="df4bc-117">000148</span><span class="sxs-lookup"><span data-stu-id="df4bc-117">000148</span></span>  
5. <span data-ttu-id="df4bc-118">Laukā rindas vai virsrakstw, atlasiet Virsraksta opciju.</span><span class="sxs-lookup"><span data-stu-id="df4bc-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="df4bc-119">Atlasiet Virsraksts, lai norādītu, ka šis ir pielikumu pievienošanas mērķis.</span><span class="sxs-lookup"><span data-stu-id="df4bc-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="df4bc-120">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="df4bc-120">Click Attach.</span></span>
    * <span data-ttu-id="df4bc-121">Pievienojiet šim pārdošanas pasūtījumam dažus failus kā pielikumus.</span><span class="sxs-lookup"><span data-stu-id="df4bc-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="df4bc-122">Izmantojiet tādu dokumentu tipu failus, ko atbalsta dokumentu pārvaldība (ar faila paplašinājumu DOCX, DPF, XML, JPG u. c.).</span><span class="sxs-lookup"><span data-stu-id="df4bc-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="df4bc-123">Pārlūkojiet un atlasiet failus, kas jāpievieno un papildus jāapstrādā kopā ar attiecīgo rēķinu ER elektroniskajā ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="df4bc-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="df4bc-124">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="df4bc-124">Click New.</span></span>
8. <span data-ttu-id="df4bc-125">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="df4bc-125">Click File.</span></span>
9. <span data-ttu-id="df4bc-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="df4bc-126">Click New.</span></span>
10. <span data-ttu-id="df4bc-127">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="df4bc-127">Click File.</span></span>
11. <span data-ttu-id="df4bc-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="df4bc-128">Close the page.</span></span>
12. <span data-ttu-id="df4bc-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="df4bc-129">Close the page.</span></span>
13. <span data-ttu-id="df4bc-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="df4bc-130">Close the page.</span></span>
14. <span data-ttu-id="df4bc-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="df4bc-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="df4bc-132">Atlasītajam rēķinam noformētas atskaites palaišana</span><span class="sxs-lookup"><span data-stu-id="df4bc-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="df4bc-133">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="df4bc-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="df4bc-134">Koka struktūrā izvērsiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="df4bc-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="df4bc-135">Kokā izvērsiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)".</span><span class="sxs-lookup"><span data-stu-id="df4bc-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="df4bc-136">Kokā atlasiet "Debitora rēķina modelis\Debitora rēķina modelis (pielāgots)\Elektronisks rēķina parauga ziņojums".</span><span class="sxs-lookup"><span data-stu-id="df4bc-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="df4bc-137">Noklikšķiniet uz Palaist.</span><span class="sxs-lookup"><span data-stu-id="df4bc-137">Click Run.</span></span>
6. <span data-ttu-id="df4bc-138">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="df4bc-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="df4bc-139">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="df4bc-139">Click Filter.</span></span>
8. <span data-ttu-id="df4bc-140">Atlasiet rindu no debitora rēķinu žurnāla un pārdošanas pasūtījuma lauka.</span><span class="sxs-lookup"><span data-stu-id="df4bc-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="df4bc-141">Laukā Kritēriji ierakstiet '000148'.</span><span class="sxs-lookup"><span data-stu-id="df4bc-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="df4bc-142">Kritērija laukā "Pārdošanas pasūtījums" ierakstiet pasūtījuma numuru 000148.</span><span class="sxs-lookup"><span data-stu-id="df4bc-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="df4bc-143">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="df4bc-143">Click OK.</span></span>
11. <span data-ttu-id="df4bc-144">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="df4bc-144">Click OK.</span></span>
    * <span data-ttu-id="df4bc-145">Pārskatiet ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="df4bc-145">Review the generated output.</span></span> <span data-ttu-id="df4bc-146">Ņemiet vērā, ka katram pielikumam ir izveidots atsevišķs XML mezgls.</span><span class="sxs-lookup"><span data-stu-id="df4bc-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="df4bc-147">Pielikuma saturs tiek aizpildīts XML izvadē MIME (base64) teksta formātā.</span><span class="sxs-lookup"><span data-stu-id="df4bc-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]