---
title: Starpuzņēmumu plāna izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8cf4ed879b6b2202d0b0f1f45052f5e21452967
ms.sourcegitcommit: 9b07d536b4bd8addfbdba42d2429c9fedb664635
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867354"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="f1a9c-103">Starpuzņēmumu plāna izveide</span><span class="sxs-lookup"><span data-stu-id="f1a9c-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1a9c-104">Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="f1a9c-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="f1a9c-106">Iestatīt starpuzņēmuma plānošanas grupu</span><span class="sxs-lookup"><span data-stu-id="f1a9c-106">Set up an intercompany planning group</span></span>

1. <span data-ttu-id="f1a9c-107">**Navigācijas rūtī** pārejiet uz sadaļu **Moduļi > Šablona plānošana > Iestatīšana > Starpuzņēmumu plānošanas grupas**.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="f1a9c-108">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f1a9c-109">Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "10".</span><span class="sxs-lookup"><span data-stu-id="f1a9c-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="f1a9c-110">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f1a9c-111">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-111">Select **Delete**.</span></span> <span data-ttu-id="f1a9c-112">Šī darbība ir nepieciešama, lai saīsinātu starpuzņēmuma plānošanas izpildi.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="f1a9c-113">Izmantojot starpuzņēmuma plānošanu, tiks izpildīta vispārējā plānošana plānošanas grupas visos uzņēmumos, sākot no zemākās plānošanas secības.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="f1a9c-114">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-114">Select **Yes**.</span></span>
6. <span data-ttu-id="f1a9c-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-115">Close the page.</span></span>

## <a name="create-an-intercompany-master-plan"></a><span data-ttu-id="f1a9c-116">Starpuzņēmumu vispārējā plāna izveide</span><span class="sxs-lookup"><span data-stu-id="f1a9c-116">Create an intercompany master plan</span></span>

1. <span data-ttu-id="f1a9c-117">**Navigācijas rūtī** ejiet uz **Moduļi > Vispārējā plānošana > Darbvietas > Vispārējā plānošana**.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="f1a9c-118">Atlasiet **Starpuzņēmumu vispārējā plānošana**.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-118">Select **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="f1a9c-119">Laukā **Starpuzņēmumu plānošanas grupa** atlasiet nolaižamo pogu uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-119">In the **Intercompany planning group** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f1a9c-120">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-120">In the list, select the link in the selected row.</span></span> <span data-ttu-id="f1a9c-121">Atlasiet starpuzņēmuma plānošanas 10. grupu.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="f1a9c-122">Laukā **Starpuzņēmumu plānošanas atkārtojumi** ievadiet „2”.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="f1a9c-123">Starpuzņēmuma plānošanas 10. grupā ir divi dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="f1a9c-124">Lai ieviestu aizkaves, kas radušās no avota uzņēmuma (USMF) līdz klienta uzņēmumam (DEMF), ir jāizpilda starpuzņēmuma forma abos uzņēmumos divas reizes.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="f1a9c-125">Pirmās iterācijas ieviesīs pieprasījumu un identificēs aizkaves avota uzņēmumā (USMF).</span><span class="sxs-lookup"><span data-stu-id="f1a9c-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="f1a9c-126">Otrā iterācija ieviesīs aizkaves no USMF līdz DEMF.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="f1a9c-127">Laukā **Pirmais atkārtojums** atlasiet „Reģenerācija”.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="f1a9c-128">Laukā **Turpmākie atkārtojumi** atlasiet „Reģenerācija”.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="f1a9c-129">Laukā **Pavedienu skaits** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="f1a9c-130">Tas norāda, cik paralēli pavedieni ir izmantoti plānošanā.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="f1a9c-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-131">Select **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="f1a9c-132">Skatīt plānošanas rezultātu</span><span class="sxs-lookup"><span data-stu-id="f1a9c-132">View the result of the plan</span></span>

1. <span data-ttu-id="f1a9c-133">Laukā **Plāns** atlasiet nolaižamo pogu uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-133">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="f1a9c-134">Sarakstā atlasiet saiti atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-134">In the list, select the link in the selected row.</span></span> <span data-ttu-id="f1a9c-135">Atlasiet StaticPlan saiti.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-135">Select the link for StaticPlan.</span></span> <span data-ttu-id="f1a9c-136">Jums jābūt uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="f1a9c-137">Atlasiet **Plānotie pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="f1a9c-137">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]