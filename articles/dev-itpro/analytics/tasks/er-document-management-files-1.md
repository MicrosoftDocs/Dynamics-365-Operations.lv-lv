--- 
title: "Datu modeļa sagatavošana, lai dokumentu pārvaldības failus lietotu formāta izvades datos"
description: "Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9f99259056fab2d56d1ccf7487681c183551c64f
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs"></a><span data-ttu-id="6ac14-103">Datu modeļa sagatavošana, lai dokumentu pārvaldības failus lietotu formāta izvades datos</span><span class="sxs-lookup"><span data-stu-id="6ac14-103">Prepare data model to use Document Management files in format outputs</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ac14-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="6ac14-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="6ac14-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="6ac14-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6ac14-106">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="6ac14-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="6ac14-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="6ac14-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="6ac14-108">Iegūt piekļuvi korporācijas Microsoft nodrošināto konfigurāciju sarakstam</span><span class="sxs-lookup"><span data-stu-id="6ac14-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6ac14-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="6ac14-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6ac14-110">Pārliecinieties, vai "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="6ac14-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="6ac14-111">ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="6ac14-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="6ac14-112">Atlasiet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="6ac14-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="6ac14-113">nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="6ac14-113">provider.</span></span>
3. <span data-ttu-id="6ac14-114">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="6ac14-114">Click Repositories.</span></span>
    * <span data-ttu-id="6ac14-115">Ja tipa Operācijas resursi repozitorijs jau pastāv, izlaidiet pašreizējā apakšuzdevuma pārējos soļus.</span><span class="sxs-lookup"><span data-stu-id="6ac14-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="6ac14-116">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6ac14-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="6ac14-117">Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.</span><span class="sxs-lookup"><span data-stu-id="6ac14-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="6ac14-118">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="6ac14-118">Click Create repository.</span></span>
7. <span data-ttu-id="6ac14-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6ac14-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="6ac14-120">Saņemiet debitoru rēķinu modeļa konfigurācijas, ko nodrošina korporācija Microsoft</span><span class="sxs-lookup"><span data-stu-id="6ac14-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="6ac14-121">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="6ac14-121">Click Show filters.</span></span>
2. <span data-ttu-id="6ac14-122">Aktivizējiet šādus filtrus: Ievadīt vienuma “Operāciju resursi” filtrēšanas vērtību laukā “Nosaukums”, izmantojot filtra operatoru “sākas ar”; Ievadīt "" filtra vērtību laukā “Apraksts”, izmantojot filtra operatoru “sākas ar”</span><span class="sxs-lookup"><span data-stu-id="6ac14-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="6ac14-123">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="6ac14-123">Click Show filters.</span></span>
4. <span data-ttu-id="6ac14-124">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="6ac14-124">Click Open.</span></span>
5. <span data-ttu-id="6ac14-125">Koka struktūrā atlasiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="6ac14-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="6ac14-126">Atlasiet modeļa konfigurāciju 'Customer invoice model', lai to importētu.</span><span class="sxs-lookup"><span data-stu-id="6ac14-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="6ac14-127">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="6ac14-127">Click Import.</span></span>
    * <span data-ttu-id="6ac14-128">Noklikšķiniet uz Atlasītās konfigurācijas versijas 1 importēšana.</span><span class="sxs-lookup"><span data-stu-id="6ac14-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="6ac14-129">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="6ac14-129">Click Yes.</span></span>
8. <span data-ttu-id="6ac14-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6ac14-130">Close the page.</span></span>
9. <span data-ttu-id="6ac14-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6ac14-131">Close the page.</span></span>
10. <span data-ttu-id="6ac14-132">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="6ac14-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="6ac14-133">Koka struktūrā atlasiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="6ac14-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="6ac14-134">Izveidot atvasināto modeli, lai atbalstītu piekļuvi dokumentu pārvaldības failiem.</span><span class="sxs-lookup"><span data-stu-id="6ac14-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="6ac14-135">Tiks izveidota sava debitoru rēķina modeļa konfigurācija, iegūstot to no korporācijas Microsoft nodrošinātas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="6ac14-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="6ac14-136">Šī konfigurācija tiks izmantota, lai izveidotu piekļuvi dokumentu pārvaldības failiem un nodrošinātu to pieejamību elektroniskajiem dokumentiem, kas tiks izveidoti, izmantojot šo modeli.</span><span class="sxs-lookup"><span data-stu-id="6ac14-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="6ac14-137">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="6ac14-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="6ac14-138">Laukā Jauns ievadiet 'Derive from Name: Customer invoice model, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6ac14-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="6ac14-139">Laukā Nosaukums ierakstiet 'Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="6ac14-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="6ac14-140">Debitora rēķina modelis (pielāgots)</span><span class="sxs-lookup"><span data-stu-id="6ac14-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="6ac14-141">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="6ac14-141">Click Create configuration.</span></span>


