--- 
title: "Iestatīt priekšnosacījumus neatbilstības pārvaldībai"
description: "Izmantojiet šo procedūru, lai iespējotu neatbilstības pārvaldības procesus."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 0a4062acc91e024e3a0a41c0b3cb35ff5ffe2a4a
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="1cc4b-103">Iestatīt priekšnosacījumus neatbilstības pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="1cc4b-103">Set up prerequisites for nonconformance management</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1cc4b-104">Izmantojiet šo procedūru, lai iespējotu neatbilstības pārvaldības procesus.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="1cc4b-105">Neatbilstība apraksta procedūru vai vienību, kam ir problēmas ar kvalitāti, kur aprakstošajā informācijā ietverts problēmas cēlonis un tips.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="1cc4b-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="1cc4b-107">Parasti šo procedūru veic kvalitātes pārvaldītājs.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="1cc4b-108">Iespējojiet uzņēmuma kvalitātes pārvaldības procesus</span><span class="sxs-lookup"><span data-stu-id="1cc4b-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="1cc4b-109">Pārejiet uz sadaļu Krājumu pārvaldība > Iestatījumi > Krājumu un noliktavas pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="1cc4b-110">Noklikšķiniet uz cilnes Kvalitātes pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="1cc4b-111">Laukā Izmantot kvalitātes pārvaldību atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="1cc4b-112">Atlasiet šo parametru, lai uzņēmumam iespējotu kvalitātes pārvaldības procesus.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="1cc4b-113">Ievadiet vērtību laukā Stundas likme.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="1cc4b-114">Laukā Stundas likme ievadiet darbaspēka stundas likmi vietējā valūtā.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="1cc4b-115">Stundas likme tiek lietota, lai aprēķinātu izmaksas par operācijām, kas saistītas ar neatbilstību.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="1cc4b-116">Stundas nomināls un aprēķinātās izmaksas sniedz atsauces informāciju par neatbilstību un tās nemijiedarbojas ar citām funkcijām.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="1cc4b-117">Noklikšķiniet uz Pārskatu iestatījums.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-117">Click Report setup.</span></span>
    * <span data-ttu-id="1cc4b-118">Šajā lapā iespējams definēt kvalitātes pārskata piezīmju tipus, kas tiks izmantoti dažāda veida kvalitātes pārvaldības pārskatos.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="1cc4b-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-119">Close the page.</span></span>
7. <span data-ttu-id="1cc4b-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="1cc4b-121">Iespējojiet lietotājam neatbilstību apstrādi.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="1cc4b-122">Pārejiet uz sadaļu Sistēmas administrēšana > Lietotāji > Lietotāji.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="1cc4b-123">Lai apstrādātu neatbilstības apstiprinājumu, lietotājam, kurš apstiprina vai noraida neatbilstību, lapā Lietotāji jābūt piešķirtai vērtībai "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="1cc4b-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="1cc4b-124">Lai lietotu dokumentu piezīmes, lietotājam jābūt aktivizētai Dokumentu apstrāde lietotāja opcijās.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="1cc4b-125">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1cc4b-126">Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "Ricardo".</span><span class="sxs-lookup"><span data-stu-id="1cc4b-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="1cc4b-127">Izmantojiet filtru, lai atrastu lietotāju, kurš apstiprinās vai noraidīs neatbilstības ierakstus.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="1cc4b-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1cc4b-129">Lai apstrādātu neatbilstības apstiprinājumu, lietotājam, kurš apstiprina vai noraida neatbilstību, lapā Lietotāji jābūt piešķirtai vērtībai "Nosaukums".</span><span class="sxs-lookup"><span data-stu-id="1cc4b-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="1cc4b-130">Noklikšķiniet uz Lietotāja opcijas.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-130">Click User options.</span></span>
5. <span data-ttu-id="1cc4b-131">Noklikšķiniet uz cilnes Preferences.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="1cc4b-132">Laukā Iespējot dokumenta apstrādi atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="1cc4b-133">Lai lietotu dokumentu piezīmes, lietotājam jābūt aktivizētai Dokumentu apstrāde lietotāja opcijās.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="1cc4b-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-134">Close the page.</span></span>
8. <span data-ttu-id="1cc4b-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-135">Close the page.</span></span>
9. <span data-ttu-id="1cc4b-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="1cc4b-137">Definējiet diagnostikas tipus neatbilstības apstrādei</span><span class="sxs-lookup"><span data-stu-id="1cc4b-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="1cc4b-138">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Diagnostikas tipi.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="1cc4b-139">Izmantojiet lapu Diagnostikas tipi, lai definētu diagnostikas darbību klasifikāciju.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="1cc4b-140">Izlabošana identificē, kāda tipa diagnostikas darbības jāizdara apstiprinātajā neatbilstībā, kuram tas jāizpilda un pieprasītās un plānotās izpildes datumu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="1cc4b-141">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-141">Click New.</span></span>
3. <span data-ttu-id="1cc4b-142">Ierakstiet vērtību Diagnostikas laukā.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="1cc4b-143">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1cc4b-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="1cc4b-145">Definējiet kvalitātes maksas neatbilstības apstrādei</span><span class="sxs-lookup"><span data-stu-id="1cc4b-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="1cc4b-146">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Kvalitātes maksas.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="1cc4b-147">Izmantojiet kvalitātes maksas lapu, lai definētu maksu klasifikāciju, kas tiks izmantota darbībām, kas saistītas ar neatbilstībām.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="1cc4b-148">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-148">Click New.</span></span>
3. <span data-ttu-id="1cc4b-149">Laukā Maksu kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="1cc4b-150">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1cc4b-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="1cc4b-152">Definējiet operācijas neatbilstības apstrādei</span><span class="sxs-lookup"><span data-stu-id="1cc4b-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="1cc4b-153">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Operācijas.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="1cc4b-154">Izmantojiet lapu Operācijas, lai definētu klasifikāciju darbam, ko var veikt apstiprinātajai neatbilstībai.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="1cc4b-155">Ja piešķirat saistīto darbību neatbilstībai, varat definēt detalizētu informāciju par saistīto materiālu, darba stundām, un dažādām papildmaksām, kas nepieciešami operācijas izpildei.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="1cc4b-156">Šī informācija sniedz pamatu izvērtēto izmaksu aprēķināšanas operāciju veikšanai.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="1cc4b-157">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-157">Click New.</span></span>
3. <span data-ttu-id="1cc4b-158">Ierakstiet vērtību laukā Operācijas.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="1cc4b-159">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1cc4b-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="1cc4b-161">Definējiet problēmu tipus neatbilstības apstrādei</span><span class="sxs-lookup"><span data-stu-id="1cc4b-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="1cc4b-162">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Problēmu tipi.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="1cc4b-163">Izmantojiet lapu Problēmtipi, lai definētu to kvalitātes problēmu klasifikāciju, kas rodas dažādiem neatbilstības veidiem.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="1cc4b-164">Neatbilstības veidi: Iekšējais, Debitora, Kreditora, Pakalpojuma pieprasījuma, Ražošanas un Līdzprodukta ražošanas.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="1cc4b-165">Viens problēmas veids var būt saistīts ar vairākiem neatbilstības veidiem.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="1cc4b-166">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-166">Click New.</span></span>
3. <span data-ttu-id="1cc4b-167">Ierakstiet vērtību laukā Problēmas tips.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="1cc4b-168">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1cc4b-169">Noklikšķiniet uz Neatbilstības tipi.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="1cc4b-170">Izmantojiet lapu Neatbilstības tipi, lai autorizētu problēmas veida, kas jāizmanto vienam vai vairākiem neatbilstības veidiem.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="1cc4b-171">Piemēram, problēmas veids, kas attiecas uz defekta kodu, var attiekties uz visiem neatbilstības veidiem, turpretī problēmas veids saistībā ar debitora sūdzībām var attiekties tikai uz debitora un pakalpojuma pieprasījuma neatbilstības veidiem.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="1cc4b-172">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-172">Click New.</span></span>
7. <span data-ttu-id="1cc4b-173">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1cc4b-174">Atlasiet opciju laukā Neatbilstības tips.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="1cc4b-175">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-175">Close the page.</span></span>
10. <span data-ttu-id="1cc4b-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="1cc4b-177">Definējiet karantīnas zonas neatbilstības apstrādei</span><span class="sxs-lookup"><span data-stu-id="1cc4b-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="1cc4b-178">Dodieties uz Krājumu vadība > Iestatīšana > Kvalitātes pārvaldība > Karantīnas zonas.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="1cc4b-179">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-179">Click New.</span></span>
3. <span data-ttu-id="1cc4b-180">Ierakstiet vērtību laukā Karantīnas zona.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="1cc4b-181">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1cc4b-182">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1cc4b-182">Close the page.</span></span>


