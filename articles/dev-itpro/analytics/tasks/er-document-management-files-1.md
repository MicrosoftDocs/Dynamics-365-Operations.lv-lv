--- 
title: "Datu modeļu sagatavošana, lai dokumentu pārvaldības failus lietotu ER izvadē"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fcafaf17315f54594116a143f36e924bc705d839
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="prepare-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="ce7ea-103">Datu modeļu sagatavošana, lai dokumentu pārvaldības failus lietotu ER izvadē</span><span class="sxs-lookup"><span data-stu-id="ce7ea-103">Prepare data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce7ea-104">Tālāk aprakstītie soļi izskaidro, kā lietotājs, kam piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma, var konfigurēt elektroniskā pārskata (ER) formātu, lai izmantotu dokumentu pārvaldības failus (pielikumi) ER izvadē.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ce7ea-105">Šīs darbības var veikt jebkurā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="ce7ea-106">Lai veiktu šīs darbības, vispirms veiciet "Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu" procedūras darbības.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="ce7ea-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="ce7ea-108">Iegūt piekļuvi korporācijas Microsoft nodrošināto konfigurāciju sarakstam</span><span class="sxs-lookup"><span data-stu-id="ce7ea-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="ce7ea-109">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="ce7ea-110">Pārliecinieties, vai "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="ce7ea-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="ce7ea-111">ir pieejams un atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="ce7ea-112">Atlasiet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="ce7ea-113">nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-113">provider.</span></span>
3. <span data-ttu-id="ce7ea-114">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-114">Click Repositories.</span></span>
    * <span data-ttu-id="ce7ea-115">Ja tipa Operācijas resursi repozitorijs jau pastāv, izlaidiet pašreizējā apakšuzdevuma pārējos soļus.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="ce7ea-116">Noklikšķiniet uz Pievienot, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="ce7ea-117">Laukā Konfigurācijas repozitorija tips ievadiet Operācijas resursi.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="ce7ea-118">Noklikšķiniet uz Izveidot repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-118">Click Create repository.</span></span>
7. <span data-ttu-id="ce7ea-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="ce7ea-120">Saņemiet debitoru rēķinu modeļa konfigurācijas, ko nodrošina korporācija Microsoft</span><span class="sxs-lookup"><span data-stu-id="ce7ea-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="ce7ea-121">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-121">Click Show filters.</span></span>
2. <span data-ttu-id="ce7ea-122">Aktivizējiet šādus filtrus: Ievadīt vienuma “Operāciju resursi” filtrēšanas vērtību laukā “Nosaukums”, izmantojot filtra operatoru “sākas ar”; Ievadīt "" filtra vērtību laukā “Apraksts”, izmantojot filtra operatoru “sākas ar”</span><span class="sxs-lookup"><span data-stu-id="ce7ea-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="ce7ea-123">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-123">Click Show filters.</span></span>
4. <span data-ttu-id="ce7ea-124">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-124">Click Open.</span></span>
5. <span data-ttu-id="ce7ea-125">Koka struktūrā atlasiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="ce7ea-126">Atlasiet modeļa konfigurāciju 'Customer invoice model', lai to importētu.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="ce7ea-127">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-127">Click Import.</span></span>
    * <span data-ttu-id="ce7ea-128">Noklikšķiniet uz Atlasītās konfigurācijas versijas 1 importēšana.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="ce7ea-129">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-129">Click Yes.</span></span>
8. <span data-ttu-id="ce7ea-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-130">Close the page.</span></span>
9. <span data-ttu-id="ce7ea-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-131">Close the page.</span></span>
10. <span data-ttu-id="ce7ea-132">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="ce7ea-133">Koka struktūrā atlasiet 'Customer invoice model'.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="ce7ea-134">Izveidot atvasināto modeli, lai atbalstītu piekļuvi dokumentu pārvaldības failiem.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="ce7ea-135">Tiks izveidota sava debitoru rēķina modeļa konfigurācija, iegūstot to no korporācijas Microsoft nodrošinātas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="ce7ea-136">Šī konfigurācija tiks izmantota, lai izveidotu piekļuvi dokumentu pārvaldības failiem un nodrošinātu to pieejamību elektroniskajiem dokumentiem, kas tiks izveidoti, izmantojot šo modeli.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="ce7ea-137">Noklikšķiniet uz Izveidot konfigurāciju, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="ce7ea-138">Laukā Jauns ievadiet 'Derive from Name: Customer invoice model, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="ce7ea-139">Laukā Nosaukums ierakstiet 'Customer invoice model (custom)'.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="ce7ea-140">Debitora rēķina modelis (pielāgots)</span><span class="sxs-lookup"><span data-stu-id="ce7ea-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="ce7ea-141">Klikšķiniet Izveidot konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="ce7ea-141">Click Create configuration.</span></span>


