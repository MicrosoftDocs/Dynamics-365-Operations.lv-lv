---
title: Starpuzņēmumu plāna izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "333741"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="e2597-103">Starpuzņēmumu plāna izveide</span><span class="sxs-lookup"><span data-stu-id="e2597-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e2597-104">Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.</span><span class="sxs-lookup"><span data-stu-id="e2597-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="e2597-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="e2597-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="e2597-106">Iestatīt starpuzņēmuma plānošanas grupu</span><span class="sxs-lookup"><span data-stu-id="e2597-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="e2597-107">Dodieties uz sadaļu Starpuzņēmuma plānošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="e2597-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="e2597-108">Vispārējā plānošana > Iestatīšana > Starpuzņēmumu plānošanas grupas</span><span class="sxs-lookup"><span data-stu-id="e2597-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="e2597-109">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="e2597-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e2597-110">Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "10".</span><span class="sxs-lookup"><span data-stu-id="e2597-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="e2597-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e2597-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e2597-112">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="e2597-112">Click Delete.</span></span>
    * <span data-ttu-id="e2597-113">Šī darbība ir nepieciešama, lai saīsinātu starpuzņēmuma plānošanas izpildi.</span><span class="sxs-lookup"><span data-stu-id="e2597-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="e2597-114">Izmantojot starpuzņēmuma plānošanu, tiks izpildīta vispārējā plānošana plānošanas grupas visos uzņēmumos, sākot no zemākās plānošanas secības.</span><span class="sxs-lookup"><span data-stu-id="e2597-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="e2597-115">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="e2597-115">Click Yes.</span></span>
6. <span data-ttu-id="e2597-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2597-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="e2597-117">Starpuzņēmumu plāna izveide</span><span class="sxs-lookup"><span data-stu-id="e2597-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="e2597-118">Noklikšķiniet uz Starpuzņēmuma vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="e2597-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="e2597-119">Tas attiecas uz vispārējās plānošanas darbvietu.</span><span class="sxs-lookup"><span data-stu-id="e2597-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="e2597-120">Laukā Starpuzņēmuma plānošanas grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas tabulu.</span><span class="sxs-lookup"><span data-stu-id="e2597-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e2597-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e2597-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2597-122">Atlasiet starpuzņēmuma plānošanas 10. grupu.</span><span class="sxs-lookup"><span data-stu-id="e2597-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="e2597-123">Laukā Starpuzņēmuma plānoto iterāciju skaits ievadiet skaitli 2.</span><span class="sxs-lookup"><span data-stu-id="e2597-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="e2597-124">Starpuzņēmuma plānošanas 10. grupā ir divi dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="e2597-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="e2597-125">Lai ieviestu aizkaves, kas radušās no avota uzņēmuma (USMF) līdz klienta uzņēmumam DEMF), ir jāizpilda starpuzņēmuma forma abos uzņēmumos divas reizes.</span><span class="sxs-lookup"><span data-stu-id="e2597-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="e2597-126">Pirmās iterācijas ieviesīs pieprasījumu un identificēs aizkaves avota uzņēmumā (USMF).</span><span class="sxs-lookup"><span data-stu-id="e2597-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="e2597-127">Otrā iterācija ieviesīs aizkaves no USMF līdz DEMF.</span><span class="sxs-lookup"><span data-stu-id="e2597-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="e2597-128">Atlasiet opciju laukā Pirmā iterācija.</span><span class="sxs-lookup"><span data-stu-id="e2597-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="e2597-129">Laukā Pirmā iterācija atlasiet opciju Reģenerācija.</span><span class="sxs-lookup"><span data-stu-id="e2597-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="e2597-130">Laukā Turpmākās iterācijas atlasiet opciju Reģenerācija.</span><span class="sxs-lookup"><span data-stu-id="e2597-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="e2597-131">Laukā Pavedienu skaits ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="e2597-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="e2597-132">Tas norāda, cik paralēli pavedieni ir izmantoti plānošanā.</span><span class="sxs-lookup"><span data-stu-id="e2597-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="e2597-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e2597-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="e2597-134">Skatīt plānošanas rezultātu</span><span class="sxs-lookup"><span data-stu-id="e2597-134">View the result of the plan</span></span>
1. <span data-ttu-id="e2597-135">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="e2597-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="e2597-136">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e2597-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2597-137">Noklikšķiniet uz StaticPlan saites.</span><span class="sxs-lookup"><span data-stu-id="e2597-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="e2597-138">Jums jābūt uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="e2597-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="e2597-139">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e2597-139">Click Planned orders.</span></span>

