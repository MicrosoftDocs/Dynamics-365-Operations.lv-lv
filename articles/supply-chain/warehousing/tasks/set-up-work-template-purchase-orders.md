---
title: Pirkšanas pasūtījumu darba veidnes iestatīšana
description: Šajā tēmā aprakstīta vienkāršas darba veidnes izveide, kuru paredzēts izmantot saņemto krājumu izvietošanai.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe0b6f9b966a5ce31af9da74a2038877debd2e7c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215749"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="0afa4-103">Pirkšanas pasūtījumu darba veidnes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0afa4-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0afa4-104">Šajā tēmā aprakstīta vienkāršas darba veidnes izveide, kuru paredzēts izmantot saņemto krājumu izvietošanai.</span><span class="sxs-lookup"><span data-stu-id="0afa4-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="0afa4-105">Darba veidnes nosaka norādījumu kopu, kas noliktavas darbiniekam tiek sniegti mobilajā ierīcē, pārvietojot krājumus no saņemšanas zonas.</span><span class="sxs-lookup"><span data-stu-id="0afa4-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="0afa4-106">Šo procedūru varat lietot, izmantojot datus, kas minēti demonstrācijas datu uzņēmumam USMF.</span><span class="sxs-lookup"><span data-stu-id="0afa4-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="0afa4-107">Pirms sākat darbu ar šo ceļvedi, izveidojiet darbu kopas ID.</span><span class="sxs-lookup"><span data-stu-id="0afa4-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="0afa4-108">Šajā piemērā tiek izmantots darbu kopas ID ar nosaukumu Ienākošs.</span><span class="sxs-lookup"><span data-stu-id="0afa4-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="0afa4-109">Šī procedūra ir paredzēta noliktavas pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="0afa4-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="0afa4-110">Navigācijas rūtī dodieties uz **Moduļi > Noliktavas pārvaldība > Iestatīšana > Darba > Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="0afa4-111">Laukā **Darba pasūtījuma veids** atlasiet **Pirkuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="0afa4-112">Izveidojiet darba veidnes virsrakstu</span><span class="sxs-lookup"><span data-stu-id="0afa4-112">Create a work template header</span></span>
1. <span data-ttu-id="0afa4-113">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-113">Select **New**.</span></span>
2. <span data-ttu-id="0afa4-114">Ievadiet skaitli laukā **Secības numurs**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="0afa4-115">Šī ir darba veidņu novērtēšanas secība.</span><span class="sxs-lookup"><span data-stu-id="0afa4-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="0afa4-116">Ja nepieciešams, šo secību varat mainīt.</span><span class="sxs-lookup"><span data-stu-id="0afa4-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="0afa4-117">Laukā **Darba veidne** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0afa4-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="0afa4-118">Tas ir šīs veidnes veidnes unikālais identifikators.</span><span class="sxs-lookup"><span data-stu-id="0afa4-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="0afa4-119">Laukā **Darba veidnes apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0afa4-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="0afa4-120">Opcija **Derīgs** nebūs atzīmēta, kamēr nebūsiet aizpildījis visu veidnei nepieciešamo informāciju un atlasījis **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="0afa4-121">Darba pasūtījumu, kura tips ir **Pirkšanas pasūtījums**, nevar apstrādāt automātiski, tāpēc opcijai **Automātiski apstrādāt** atstājiet iestatījumu **Nē**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="0afa4-122">Laukā **Darba kopas ID** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0afa4-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="0afa4-123">Darbu kopu ID ļauj organizēt darbu grupās.</span><span class="sxs-lookup"><span data-stu-id="0afa4-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="0afa4-124">Šeit iestatītā vērtība būs noklusējuma vērtība visiem darbiem, kas izveidoti, lietojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="0afa4-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="0afa4-125">Laukā **Darba prioritāte** ievadiet skaitli `1`.</span><span class="sxs-lookup"><span data-stu-id="0afa4-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="0afa4-126">Tas norāda darba svarīgumu, un šeit iestatītā vērtība būs noklusējuma vērtība visiem darbiem, kas izveidoti, lietojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="0afa4-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="0afa4-127">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-127">Select **Save**.</span></span> <span data-ttu-id="0afa4-128">Pirms kļūst pieejama poga **Rediģēt vaicājumu**, vispirms jāsaglabā darba veidnes virsraksts.</span><span class="sxs-lookup"><span data-stu-id="0afa4-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="0afa4-129">Darba veidnes vaicājuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0afa4-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="0afa4-130">Atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-130">Select **Edit query**.</span></span> <span data-ttu-id="0afa4-131">Mēs noteiksim ierobežojumu, ka veidni var izmantot tikai noteiktā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="0afa4-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="0afa4-132">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-132">Select **Add**.</span></span>
3. <span data-ttu-id="0afa4-133">Jaunās rindas laukā **Lauks** ierakstiet vērtību `warehouse`.</span><span class="sxs-lookup"><span data-stu-id="0afa4-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="0afa4-134">Laukā **Kritēriji** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0afa4-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="0afa4-135">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-135">Select **OK**.</span></span>
6. <span data-ttu-id="0afa4-136">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="0afa4-137">Detalizētas informācijas par darba veidni iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0afa4-137">Set work template details</span></span>
1. <span data-ttu-id="0afa4-138">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-138">Select **New**.</span></span>
2. <span data-ttu-id="0afa4-139">Laukā **Darba tips atlasiet** vienumu **Izdošana**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="0afa4-140">Laukā **Darba klases ID** ierakstiet vērtību `purchase`.</span><span class="sxs-lookup"><span data-stu-id="0afa4-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="0afa4-141">Šeit iestatītā darba klase būs noklusējuma klase visās darba rindās, kuru veids ir Izdošana un kuras izveidotas, lietojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="0afa4-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="0afa4-142">Šo darba klasi nevar pārrakstīt no darba pasūtījuma rindām.</span><span class="sxs-lookup"><span data-stu-id="0afa4-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="0afa4-143">Darba klases tiek izmantotas, lai virzītu un/vai ierobežotu darba pasūtījuma rindu veidu, ko noliktavas darbinieks var apstrādāt mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="0afa4-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="0afa4-144">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-144">Select **New**.</span></span>
5. <span data-ttu-id="0afa4-145">Laukā **Darba veids** atlasiet **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="0afa4-146">Laukā **Darba klases ID** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="0afa4-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="0afa4-147">Izdošanas un izvietošanas instrukcijas ir kopa.</span><span class="sxs-lookup"><span data-stu-id="0afa4-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="0afa4-148">Katrai izdošanas/izvietošanas kopai ir jābūt vienai un tai pašai darba klasei.</span><span class="sxs-lookup"><span data-stu-id="0afa4-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="0afa4-149">Izmantojiet to pašu darba klasi, kuru norādījāt izdošanas instrukcijai.</span><span class="sxs-lookup"><span data-stu-id="0afa4-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="0afa4-150">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-150">Select **Save**.</span></span> <span data-ttu-id="0afa4-151">Pievērsiet uzmanību, ka tagad ir atzīmēta izvēles rūtiņa **Derīgs**.</span><span class="sxs-lookup"><span data-stu-id="0afa4-151">Note that the **Valid** checkbox is now checked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]