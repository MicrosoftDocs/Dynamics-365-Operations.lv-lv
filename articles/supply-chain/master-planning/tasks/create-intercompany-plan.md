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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 194bb78eed5a673030f7cead031cf286cddbe77c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845213"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="1714e-103">Starpuzņēmumu plāna izveide</span><span class="sxs-lookup"><span data-stu-id="1714e-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1714e-104">Šajā procedūrā ir aprakstīts, kā izveidot starpuzņēmuma plānu.</span><span class="sxs-lookup"><span data-stu-id="1714e-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="1714e-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="1714e-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="1714e-106">Iestatīt starpuzņēmuma plānošanas grupu</span><span class="sxs-lookup"><span data-stu-id="1714e-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="1714e-107">Dodieties uz sadaļu Starpuzņēmuma plānošanas grupas.</span><span class="sxs-lookup"><span data-stu-id="1714e-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="1714e-108">Vispārējā plānošana > Iestatīšana > Starpuzņēmumu plānošanas grupas</span><span class="sxs-lookup"><span data-stu-id="1714e-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="1714e-109">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="1714e-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1714e-110">Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "10".</span><span class="sxs-lookup"><span data-stu-id="1714e-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="1714e-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1714e-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1714e-112">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="1714e-112">Click Delete.</span></span>
    * <span data-ttu-id="1714e-113">Šī darbība ir nepieciešama, lai saīsinātu starpuzņēmuma plānošanas izpildi.</span><span class="sxs-lookup"><span data-stu-id="1714e-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="1714e-114">Izmantojot starpuzņēmuma plānošanu, tiks izpildīta vispārējā plānošana plānošanas grupas visos uzņēmumos, sākot no zemākās plānošanas secības.</span><span class="sxs-lookup"><span data-stu-id="1714e-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="1714e-115">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="1714e-115">Click Yes.</span></span>
6. <span data-ttu-id="1714e-116">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1714e-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="1714e-117">Starpuzņēmumu plāna izveide</span><span class="sxs-lookup"><span data-stu-id="1714e-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="1714e-118">Noklikšķiniet uz Starpuzņēmuma vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="1714e-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="1714e-119">Tas attiecas uz vispārējās plānošanas darbvietu.</span><span class="sxs-lookup"><span data-stu-id="1714e-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="1714e-120">Laukā Starpuzņēmuma plānošanas grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas tabulu.</span><span class="sxs-lookup"><span data-stu-id="1714e-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="1714e-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1714e-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1714e-122">Atlasiet starpuzņēmuma plānošanas 10. grupu.</span><span class="sxs-lookup"><span data-stu-id="1714e-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="1714e-123">Laukā Starpuzņēmuma plānoto iterāciju skaits ievadiet skaitli 2.</span><span class="sxs-lookup"><span data-stu-id="1714e-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="1714e-124">Starpuzņēmuma plānošanas 10. grupā ir divi dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="1714e-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="1714e-125">Lai ieviestu aizkaves, kas radušās no avota uzņēmuma (USMF) līdz klienta uzņēmumam DEMF), ir jāizpilda starpuzņēmuma forma abos uzņēmumos divas reizes.</span><span class="sxs-lookup"><span data-stu-id="1714e-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="1714e-126">Pirmās iterācijas ieviesīs pieprasījumu un identificēs aizkaves avota uzņēmumā (USMF).</span><span class="sxs-lookup"><span data-stu-id="1714e-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="1714e-127">Otrā iterācija ieviesīs aizkaves no USMF līdz DEMF.</span><span class="sxs-lookup"><span data-stu-id="1714e-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="1714e-128">Atlasiet opciju laukā Pirmā iterācija.</span><span class="sxs-lookup"><span data-stu-id="1714e-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="1714e-129">Laukā Pirmā iterācija atlasiet opciju Reģenerācija.</span><span class="sxs-lookup"><span data-stu-id="1714e-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="1714e-130">Laukā Turpmākās iterācijas atlasiet opciju Reģenerācija.</span><span class="sxs-lookup"><span data-stu-id="1714e-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="1714e-131">Laukā Pavedienu skaits ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="1714e-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="1714e-132">Tas norāda, cik paralēli pavedieni ir izmantoti plānošanā.</span><span class="sxs-lookup"><span data-stu-id="1714e-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="1714e-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1714e-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="1714e-134">Skatīt plānošanas rezultātu</span><span class="sxs-lookup"><span data-stu-id="1714e-134">View the result of the plan</span></span>
1. <span data-ttu-id="1714e-135">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1714e-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="1714e-136">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1714e-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1714e-137">Noklikšķiniet uz StaticPlan saites.</span><span class="sxs-lookup"><span data-stu-id="1714e-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="1714e-138">Jums jābūt uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="1714e-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="1714e-139">Noklikšķiniet uz Plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="1714e-139">Click Planned orders.</span></span>

