--- 
title: "Lean manufacturing apakšuzņēmēja darba šūnas izveide"
description: "Lai modelētu lean manufacturing apakšlīguma darbu, jāizveido darba šūna, kas saistīta ar kreditoru, kurš nodrošina darbu."
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fc8dc0bc29c6bdb662c46808491abf5395f0be5d
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="72cf6-103">Lean manufacturing apakšuzņēmēja darba šūnas izveide</span><span class="sxs-lookup"><span data-stu-id="72cf6-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72cf6-104">Lai modelētu lean manufacturing apakšlīguma darbu, jāizveido darba šūna, kas saistīta ar kreditoru, kurš nodrošina darbu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="72cf6-105">Apakšuzņēmēja darba šūna ir saistīta ar kreditoru, izmantojot kreditora veida resursa saistību.</span><span class="sxs-lookup"><span data-stu-id="72cf6-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="72cf6-106">Atskaņojot šo ierakstu USMF demonstrācijas uzņēmumā, varat atlasīt kreditora konta ID 1002 un vietu 1.</span><span class="sxs-lookup"><span data-stu-id="72cf6-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="72cf6-107">Kreditora resursa izveide</span><span class="sxs-lookup"><span data-stu-id="72cf6-107">Create a vendor resource</span></span>
1. <span data-ttu-id="72cf6-108">Dodieties uz Resursi.</span><span class="sxs-lookup"><span data-stu-id="72cf6-108">Go to Resources.</span></span>
2. <span data-ttu-id="72cf6-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="72cf6-109">Click New.</span></span>
3. <span data-ttu-id="72cf6-110">Laukā Resursi ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="72cf6-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="72cf6-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="72cf6-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="72cf6-112">Laukā veids atlasiet "Vendor".</span><span class="sxs-lookup"><span data-stu-id="72cf6-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="72cf6-113">Laukā Kreditors noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="72cf6-114">Resursu grupas izveide</span><span class="sxs-lookup"><span data-stu-id="72cf6-114">Create the resource group</span></span>
1. <span data-ttu-id="72cf6-115">Dodieties uz Resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="72cf6-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="72cf6-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="72cf6-116">Click New.</span></span>
3. <span data-ttu-id="72cf6-117">Laukā Resursu grupa ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="72cf6-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="72cf6-118">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="72cf6-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="72cf6-119">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="72cf6-120">Atlasiet vietu, kurai ir jāpiešķir darba šūna.</span><span class="sxs-lookup"><span data-stu-id="72cf6-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="72cf6-121">Teorētiski vieta var apzīmēt atsevišķu vietu, ko vada kreditors.</span><span class="sxs-lookup"><span data-stu-id="72cf6-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="72cf6-122">Tomēr vairumā gadījumu apakšuzņēmēja resursi ir tikai piešķirti vietai, kas pasūta apakšuzņēmēja darbu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="72cf6-123">Ņemiet vērā, ka apakšuzņēmēja darba šūnu ievades un izvades noliktavām jābūt tajā pašā vietā.</span><span class="sxs-lookup"><span data-stu-id="72cf6-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="72cf6-124">Laukā Vieta ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="72cf6-124">In the Site field, type a value.</span></span>
7. @SysTaskRecorder:_RequestClose
8. <span data-ttu-id="72cf6-125">Atzīmējiet izvēles rūtiņu Darba šūna vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="72cf6-125">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="72cf6-126">Laukā Ievades noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-126">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="72cf6-127">Atlasiet noliktavu un vietu, kas tiek izmantota, lai novietotu materiālu kreditora pārvaldītai darba šūnai.</span><span class="sxs-lookup"><span data-stu-id="72cf6-127">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="72cf6-128">Daudzos gadījumos noliktava un vieta tiek modelēta, izmantojot atsevišķu noliktavu katram kreditoram un vienu vietu darba šūnai.</span><span class="sxs-lookup"><span data-stu-id="72cf6-128">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="72cf6-129">Laukā Ievades vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="72cf6-130">Laukā Izvades noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-130">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="72cf6-131">Definējiet noliktavu un vietu, kur tiek grāmatots materiāls, grāmatojot darba šūnas apakšuzņēmēju aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="72cf6-131">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="72cf6-132">Ja kreditora pārskati ir Kanban darbi, noliktava un vieta var būt kreditora vietnē.</span><span class="sxs-lookup"><span data-stu-id="72cf6-132">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="72cf6-133">Vai arī noliktava un vieta var būt saņemšanas vieta, kas saistīta ar ražošanas plūsmas nākamo soli.</span><span class="sxs-lookup"><span data-stu-id="72cf6-133">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="72cf6-134">Laukā Izvades vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-134">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="72cf6-135">Izvērsiet vai sakļaujiet sadaļu Kalendāri.</span><span class="sxs-lookup"><span data-stu-id="72cf6-135">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="72cf6-136">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cf6-136">Click Add.</span></span>
15. <span data-ttu-id="72cf6-137">Laukā Kalendārs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-137">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="72cf6-138">Saistiet darba šūnas darba laika kalendāru ar resursu grupu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-138">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="72cf6-139">Kritiskiem resursiem iesakām definēt noteiktus kalendārus, kas attēlo precīzus darba laikus un darba šūnas vai kreditora vietnes saistītās iespējas.</span><span class="sxs-lookup"><span data-stu-id="72cf6-139">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="72cf6-140">Izvērsiet vai sakļaujiet sadaļu Resursi.</span><span class="sxs-lookup"><span data-stu-id="72cf6-140">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="72cf6-141">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cf6-141">Click Add.</span></span>
    * <span data-ttu-id="72cf6-142">Apakšuzņēmēja resursu grupai ir nepieciešams kreditora veida saistītais resurss, kas saista resursu grupu ar kreditora kontu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-142">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="72cf6-143">Laukā Resursi noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-143">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="72cf6-144">Atlasiet vai ievadiet kreditora resursu, ko izveidojāt iepriekšējā apakšuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="72cf6-144">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="72cf6-145">Izvērsiet vai sakļaujiet sadaļu Darba šūnas noslodze.</span><span class="sxs-lookup"><span data-stu-id="72cf6-145">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="72cf6-146">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="72cf6-146">Click Add.</span></span>
    * <span data-ttu-id="72cf6-147">Darba šūnai ir jādefinē noslodze.</span><span class="sxs-lookup"><span data-stu-id="72cf6-147">A work cell must have a defined capacity.</span></span> <span data-ttu-id="72cf6-148">Šajā piemērā izveidojām 100 vienību caurlaides noslodzi uz standarta darbdienu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-148">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="72cf6-149">Laukā Ražošanas plūsmas modelis noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-149">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="72cf6-150">Laukā Noslodzes periods atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="72cf6-150">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="72cf6-151">Laukā Vidējais caurlaides daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="72cf6-151">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="72cf6-152">Laukā Vienība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="72cf6-152">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="72cf6-153">ResolveChanges vienumam Vienība.</span><span class="sxs-lookup"><span data-stu-id="72cf6-153">ResolveChanges the Unit.</span></span>


