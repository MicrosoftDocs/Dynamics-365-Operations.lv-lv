--- 
title: "Pirkšanas pasūtījumu darba veidnes iestatīšana"
description: "Šajā procedūrā aprakstīta vienkāršas darba veidnes izveide, kuru paredzēts izmantot saņemto krājumu izvietošanai."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d737f9dfd1888602266a87853e54407618ae2781
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="59610-103">Pirkšanas pasūtījumu darba veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="59610-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59610-104">Šajā procedūrā aprakstīta vienkāršas darba veidnes izveide, kuru paredzēts izmantot saņemto krājumu izvietošanai.</span><span class="sxs-lookup"><span data-stu-id="59610-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="59610-105">Darba veidnes nosaka norādījumu kopu, kas noliktavas darbiniekam tiek sniegti mobilajā ierīcē, pārvietojot krājumus no saņemšanas zonas.</span><span class="sxs-lookup"><span data-stu-id="59610-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="59610-106">Šo procedūru varat lietot, izmantojot datus, kas minēti demonstrācijas datu uzņēmumam USMF.</span><span class="sxs-lookup"><span data-stu-id="59610-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="59610-107">Pirms sākat darbu ar šo ceļvedi, izveidojiet darbu kopas ID.</span><span class="sxs-lookup"><span data-stu-id="59610-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="59610-108">Šajā piemērā tiek izmantots darbu kopas ID ar nosaukumu Ienākošs.</span><span class="sxs-lookup"><span data-stu-id="59610-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="59610-109">Šī procedūra ir paredzēta noliktavas pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="59610-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="59610-110">Doties uz Noliktavas vadība > Iestatīšana > Darbs > Darbu veidnes.</span><span class="sxs-lookup"><span data-stu-id="59610-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="59610-111">Laukā Darba pasūtījuma tips atlasiet “Pirkšanas pasūtījumi”.</span><span class="sxs-lookup"><span data-stu-id="59610-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="59610-112">Izveidojiet darba veidnes virsrakstu</span><span class="sxs-lookup"><span data-stu-id="59610-112">Create a work template header</span></span>
1. <span data-ttu-id="59610-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="59610-113">Click New.</span></span>
2. <span data-ttu-id="59610-114">Ievadiet skaitli laukā Secības numurs.</span><span class="sxs-lookup"><span data-stu-id="59610-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="59610-115">Šī ir darba veidņu novērtēšanas secība.</span><span class="sxs-lookup"><span data-stu-id="59610-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="59610-116">Ja nepieciešams, šo secību varat mainīt.</span><span class="sxs-lookup"><span data-stu-id="59610-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="59610-117">Laukā Darba veidne ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="59610-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="59610-118">Tas ir šīs veidnes veidnes unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="59610-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="59610-119">Laukā Darba veidnes apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="59610-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="59610-120">Opcija Derīgs nebūs atzīmēta, kamēr nebūsiet aizpildījis visu veidnei nepieciešamo informāciju un noklikšķinājis uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="59610-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="59610-121">Darba pasūtījumu, kura veids ir Pirkšanas pasūtījums, nevar apstrādāt automātiski, tāpēc atstājiet opcijai Automātiski apstrādāt iestatījumu Nē.</span><span class="sxs-lookup"><span data-stu-id="59610-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="59610-122">Laukā Darba kopas ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="59610-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="59610-123">Darbu kopu ID ļauj organizēt darbu grupās.</span><span class="sxs-lookup"><span data-stu-id="59610-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="59610-124">Šeit iestatītā vērtība būs noklusējuma vērtība visiem darbiem, kas izveidoti, lietojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="59610-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="59610-125">Laukā Darba prioritāte ievadiet skaitli "1".</span><span class="sxs-lookup"><span data-stu-id="59610-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="59610-126">Tas norāda darba svarīgumu, un šeit iestatītā vērtība būs noklusējuma vērtība visiem darbiem, kas izveidoti, lietojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="59610-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="59610-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="59610-127">Click Save.</span></span>
    * <span data-ttu-id="59610-128">Pirms kļūst pieejama poga Rediģēt vaicājumu, vispirms jāsaglabā darba veidnes virsraksts.</span><span class="sxs-lookup"><span data-stu-id="59610-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="59610-129">Darba veidnes vaicājuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="59610-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="59610-130">Noklikšķiniet uz Rediģēt vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="59610-130">Click Edit query.</span></span>
    * <span data-ttu-id="59610-131">Mēs noteiksim ierobežojumu, ka veidni var izmantot tikai noteiktā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="59610-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="59610-132">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="59610-132">Click Add.</span></span>
3. <span data-ttu-id="59610-133">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="59610-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="59610-134">Laukā Lauks ierakstiet "noliktava".</span><span class="sxs-lookup"><span data-stu-id="59610-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="59610-135">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="59610-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="59610-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="59610-136">Click OK.</span></span>
7. <span data-ttu-id="59610-137">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="59610-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="59610-138">Detalizētas informācijas par darba veidni iestatīšana</span><span class="sxs-lookup"><span data-stu-id="59610-138">Set work template details</span></span>
1. <span data-ttu-id="59610-139">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="59610-139">Click New.</span></span>
2. <span data-ttu-id="59610-140">Laukā Darba tips atlasiet vienumu “Izdošana”.</span><span class="sxs-lookup"><span data-stu-id="59610-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="59610-141">Laukā Darba klases ID ierakstiet "pirkšana".</span><span class="sxs-lookup"><span data-stu-id="59610-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="59610-142">Šeit iestatītā darba klase būs noklusējuma klase visās darba rindās, kuru veids ir Izdošana un kuras izveidotas, lietojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="59610-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="59610-143">Šo darba klasi nevar pārrakstīt no darba pasūtījuma rindām.</span><span class="sxs-lookup"><span data-stu-id="59610-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="59610-144">Darba klases tiek izmantotas, lai virzītu un/vai ierobežotu darba pasūtījuma rindu veidu, ko noliktavas darbinieks var apstrādāt mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="59610-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="59610-145">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="59610-145">Click New.</span></span>
5. <span data-ttu-id="59610-146">Laukā Darba tips atlasiet vienumu “Izvietošana”.</span><span class="sxs-lookup"><span data-stu-id="59610-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="59610-147">Laukā Darba klases ID ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="59610-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="59610-148">Izdošanas un izvietošanas instrukcijas ir kopa.</span><span class="sxs-lookup"><span data-stu-id="59610-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="59610-149">Katrai izdošanas/izvietošanas kopai ir jābūt vienai un tai pašai darba klasei.</span><span class="sxs-lookup"><span data-stu-id="59610-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="59610-150">Izmantojiet to pašu darba klasi, kuru norādījāt izdošanas instrukcijai.</span><span class="sxs-lookup"><span data-stu-id="59610-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="59610-151">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="59610-151">Click Save.</span></span>
    * <span data-ttu-id="59610-152">Pievērsiet uzmanību, ka tagad ir atzīmēta izvēles rūtiņa Derīgs.</span><span class="sxs-lookup"><span data-stu-id="59610-152">Note that the Valid checkbox is now checked.</span></span>  


