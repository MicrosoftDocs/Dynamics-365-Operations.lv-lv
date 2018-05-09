---
title: "Atbilstības izveide un apstrāde"
description: "Izmantojiet šo procedūru, lai veiktu neatbilstības pārvaldību, pamatojoties uz esošo kvalitātes pārbaudes pasūtījumu."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e73295698a17b7500db40820dd9603855810ca3a
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="54107-103">Atbilstības izveide un apstrāde</span><span class="sxs-lookup"><span data-stu-id="54107-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54107-104">Izmantojiet šo procedūru, lai veiktu neatbilstības pārvaldību, pamatojoties uz esošo kvalitātes pārbaudes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="54107-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="54107-105">Šo ierakstu var palaist USMF demonstrācijas uzņēmumā un var izmantot ieteiktās vērtības.</span><span class="sxs-lookup"><span data-stu-id="54107-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="54107-106">Parasti šo procedūru veic kvalitātes darbinieks.</span><span class="sxs-lookup"><span data-stu-id="54107-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="54107-107">Kā priekšnosacījumu, palaidiet uzdevuma ierakstu "Pārbaudīt preču kvalitāti".</span><span class="sxs-lookup"><span data-stu-id="54107-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="54107-108">Lai apstrādātu neatbilstības apstiprinājumu, lietotājam, kurš palaiž uzdevumu ierakstu, lapā Lietotāji jābūt piešķirtai vērtībai "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="54107-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="54107-109">Lai lietotu dokumentu piezīmes, lietotājam jābūt aktivizētai Dokumentu apstrāde lietotāja opcijās.</span><span class="sxs-lookup"><span data-stu-id="54107-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="54107-110">Atlasiet kvalitātes pārbaudes pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="54107-110">Select a quality order</span></span>
1. <span data-ttu-id="54107-111">Dodieties uz Kvalitātes pārbaudes pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="54107-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="54107-112">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="54107-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="54107-113">Atlasiet kvalitātes pārbaudes pasūtījumu, kas tika izveidots no uzdevuma ieraksta "Preču kvalitātes pārbaude".</span><span class="sxs-lookup"><span data-stu-id="54107-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="54107-114">Neatbilstības izveide</span><span class="sxs-lookup"><span data-stu-id="54107-114">Create a nonconformance</span></span>
1. <span data-ttu-id="54107-115">Noklikšķiniet uz Uzziņas.</span><span class="sxs-lookup"><span data-stu-id="54107-115">Click Inquiries.</span></span>
2. <span data-ttu-id="54107-116">Noklikšķiniet uz Neatbilstības.</span><span class="sxs-lookup"><span data-stu-id="54107-116">Click Non conformances.</span></span>
3. <span data-ttu-id="54107-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="54107-117">Click New.</span></span>
4. <span data-ttu-id="54107-118">Laukā Problēmtips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="54107-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="54107-119">Atlasiet problēmu, kas tika konstatēta pārbaudes procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="54107-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="54107-120">Laukā Problēmtips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="54107-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="54107-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="54107-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="54107-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="54107-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="54107-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="54107-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="54107-124">Neatbilstības apstiprināšana/noraidīšana</span><span class="sxs-lookup"><span data-stu-id="54107-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="54107-125">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="54107-125">Click Functions.</span></span>
2. <span data-ttu-id="54107-126">Noklikšķiniet uz Apstiprināt neatbilstību.</span><span class="sxs-lookup"><span data-stu-id="54107-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="54107-127">Šim piemēram apstipriniet neatbilstību.</span><span class="sxs-lookup"><span data-stu-id="54107-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="54107-128">Apstiprinātas neatbilstības var saistīt ar saistītām operācijām, lai ierakstītu darbu, kas tiek veikts kā daļa no neatbilstības apstrādes, un, kā šajā uzdevuma ierakstā, korekcijas apstrādes apstrādes.</span><span class="sxs-lookup"><span data-stu-id="54107-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="54107-129">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="54107-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="54107-130">Labojuma darbības izveide</span><span class="sxs-lookup"><span data-stu-id="54107-130">Create a correction action</span></span>
1. <span data-ttu-id="54107-131">Skatīt Labojumi.</span><span class="sxs-lookup"><span data-stu-id="54107-131">Click Corrections.</span></span>
2. <span data-ttu-id="54107-132">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="54107-132">Click New.</span></span>
3. <span data-ttu-id="54107-133">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="54107-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="54107-134">Laukā Personāla numurs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="54107-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="54107-135">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="54107-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="54107-136">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="54107-136">Click Select.</span></span>
7. <span data-ttu-id="54107-137">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="54107-137">Click Attach.</span></span>
    * <span data-ttu-id="54107-138">Izveidojiet piezīmi par šo labojumu.</span><span class="sxs-lookup"><span data-stu-id="54107-138">Create a note about the correction.</span></span> <span data-ttu-id="54107-139">Šajā piemērā darbība ir sazināties ar kreditoru, lai apspriestu neatbilstības gadījumu.</span><span class="sxs-lookup"><span data-stu-id="54107-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="54107-140">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="54107-140">Click New.</span></span>
9. <span data-ttu-id="54107-141">Noklikšķiniet uz Piezīme.</span><span class="sxs-lookup"><span data-stu-id="54107-141">Click Note.</span></span>
    * <span data-ttu-id="54107-142">Ievērojiet, ka, atkarībā no pārskata iestatījumiem, dažādus dokumentu tipus var drukāt pārskatos, kas saistīti ar neatbilstību pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="54107-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="54107-143">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="54107-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="54107-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54107-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="54107-145">Labojuma uzturēšana</span><span class="sxs-lookup"><span data-stu-id="54107-145">Maintain a correction</span></span>
1. <span data-ttu-id="54107-146">Noklikšķiniet uz Atzīmēt kā pabeigtu.</span><span class="sxs-lookup"><span data-stu-id="54107-146">Click Mark complete.</span></span>
2. <span data-ttu-id="54107-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="54107-147">Click OK.</span></span>
3. <span data-ttu-id="54107-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54107-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="54107-149">Neatbilstības aizvēršana</span><span class="sxs-lookup"><span data-stu-id="54107-149">Close a nonconformance</span></span>
1. <span data-ttu-id="54107-150">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="54107-150">Click Functions.</span></span>
2. <span data-ttu-id="54107-151">Noklikšķiniet uz Aizvērt neatbilstību.</span><span class="sxs-lookup"><span data-stu-id="54107-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="54107-152">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="54107-152">Click Yes.</span></span>
4. <span data-ttu-id="54107-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54107-153">Close the page.</span></span>
5. <span data-ttu-id="54107-154">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54107-154">Close the page.</span></span>

