---
title: Starpuzņēmumu plāna izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c368e461860a41d0110f5aed79c2aac49c437d68
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011416"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="5720c-103">Starpuzņēmumu plāna izveide</span><span class="sxs-lookup"><span data-stu-id="5720c-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5720c-104">Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.</span><span class="sxs-lookup"><span data-stu-id="5720c-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="5720c-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="5720c-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="5720c-106">Iestatīt starpuzņēmuma plānošanas grupu</span><span class="sxs-lookup"><span data-stu-id="5720c-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="5720c-107">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Šablona plānošana > Iestatīšana > Starpuzņēmumu plānošanas grupas**.</span><span class="sxs-lookup"><span data-stu-id="5720c-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="5720c-108">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="5720c-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5720c-109">Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "10".</span><span class="sxs-lookup"><span data-stu-id="5720c-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="5720c-110">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5720c-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5720c-111">Noklikšķiniet uz **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="5720c-111">Click **Delete**.</span></span> <span data-ttu-id="5720c-112">Šī darbība ir nepieciešama, lai saīsinātu starpuzņēmuma plānošanas izpildi.</span><span class="sxs-lookup"><span data-stu-id="5720c-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="5720c-113">Izmantojot starpuzņēmuma plānošanu, tiks izpildīta vispārējā plānošana plānošanas grupas visos uzņēmumos, sākot no zemākās plānošanas secības.</span><span class="sxs-lookup"><span data-stu-id="5720c-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="5720c-114">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="5720c-114">Click **Yes**.</span></span>
6. <span data-ttu-id="5720c-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5720c-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="5720c-116">Starpuzņēmumu plāna izveide</span><span class="sxs-lookup"><span data-stu-id="5720c-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="5720c-117">**Navigācijas rūtī** ejiet uz **Moduļi > Vispārējā plānošana > Darbvietas > Vispārējā plānošana**.</span><span class="sxs-lookup"><span data-stu-id="5720c-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="5720c-118">Klikšķiniet uz **Starpuzņēmumu vispārējā plānošana**.</span><span class="sxs-lookup"><span data-stu-id="5720c-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="5720c-119">Laukā **Starpuzņēmumu plānošanas grupa** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="5720c-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5720c-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="5720c-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="5720c-121">Atlasiet starpuzņēmuma plānošanas 10. grupu.</span><span class="sxs-lookup"><span data-stu-id="5720c-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="5720c-122">Laukā **Starpuzņēmumu plānošanas atkārtojumi** ievadiet „2”.</span><span class="sxs-lookup"><span data-stu-id="5720c-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="5720c-123">Starpuzņēmuma plānošanas 10. grupā ir divi dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="5720c-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="5720c-124">Lai ieviestu aizkaves, kas radušās no avota uzņēmuma (USMF) līdz klienta uzņēmumam (DEMF), ir jāizpilda starpuzņēmuma forma abos uzņēmumos divas reizes.</span><span class="sxs-lookup"><span data-stu-id="5720c-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="5720c-125">Pirmās iterācijas ieviesīs pieprasījumu un identificēs aizkaves avota uzņēmumā (USMF).</span><span class="sxs-lookup"><span data-stu-id="5720c-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="5720c-126">Otrā iterācija ieviesīs aizkaves no USMF līdz DEMF.</span><span class="sxs-lookup"><span data-stu-id="5720c-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="5720c-127">Laukā **Pirmais atkārtojums** atlasiet „Reģenerācija”.</span><span class="sxs-lookup"><span data-stu-id="5720c-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="5720c-128">Laukā **Turpmākie atkārtojumi** atlasiet „Reģenerācija”.</span><span class="sxs-lookup"><span data-stu-id="5720c-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="5720c-129">Laukā **Pavedienu skaits** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="5720c-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="5720c-130">Tas norāda, cik paralēli pavedieni ir izmantoti plānošanā.</span><span class="sxs-lookup"><span data-stu-id="5720c-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="5720c-131">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5720c-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="5720c-132">Skatīt plānošanas rezultātu</span><span class="sxs-lookup"><span data-stu-id="5720c-132">View the result of the plan</span></span>
1. <span data-ttu-id="5720c-133">Laukā **Plāns** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="5720c-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="5720c-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="5720c-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="5720c-135">Noklikšķiniet uz StaticPlan saites.</span><span class="sxs-lookup"><span data-stu-id="5720c-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="5720c-136">Jums jābūt uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="5720c-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="5720c-137">Klikšķiniet uz **Plānotie pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="5720c-137">Click **Planned orders**.</span></span>

