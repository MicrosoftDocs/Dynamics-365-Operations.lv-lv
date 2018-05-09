--- 
title: "Atvilkuma Kanban kārtulas izveide"
description: "Šī procedūra parāda iestatījumu, kas ir nepieciešams, lai izveidotu atvilkuma kanban nosacījumu, materiāla pārvietošanai racionālās vidē."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b533d1b7b0c92fd6072500f2856036f0dffb7809
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="ca2b5-103">Atvilkuma Kanban kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="ca2b5-103">Create a withdrawal kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca2b5-104">Šī procedūra parāda iestatījumu, kas ir nepieciešams, lai izveidotu atvilkuma kanban nosacījumu, materiāla pārvietošanai racionālās vidē.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="ca2b5-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ca2b5-106">Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jauna vai modificēta materiāla papildināšanai.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="ca2b5-107">Jaunu Kanban nosacījumu izveide</span><span class="sxs-lookup"><span data-stu-id="ca2b5-107">Create new kanban rule</span></span>
1. <span data-ttu-id="ca2b5-108">Dodieties uz Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ca2b5-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-109">Click New.</span></span>
3. <span data-ttu-id="ca2b5-110">Laukā Veids, atlasiet 'Atvilkums'.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="ca2b5-111">Atvilkuma veids tiek izmantots kanban nosacījumiem, lai pārsūtītu materiālus vai preces.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="ca2b5-112">Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ca2b5-113">Atlasiet ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="ca2b5-114">Šī aktivitātei ir iestatīta, lai pārvietotu komponentus no noliktavas 11, atrašanās vietas 11 uz noliktavu 12 un atrašanās vietu 12.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="ca2b5-115">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="ca2b5-116">Atlasiet M0007.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-116">Select M0007.</span></span>  
6. <span data-ttu-id="ca2b5-117">Laukā Izpildes laiks ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="ca2b5-118">Piemēram, 60.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-118">For example, 60.</span></span>  
7. <span data-ttu-id="ca2b5-119">Laukā Mērvienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="ca2b5-120">Piemēram, Minūtes.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="ca2b5-121">Iestatiet Kanban daudzumus</span><span class="sxs-lookup"><span data-stu-id="ca2b5-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="ca2b5-122">Vienumam Noklusējuma daudzums iestatiet vērtību "5".</span><span class="sxs-lookup"><span data-stu-id="ca2b5-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="ca2b5-123">Tas ir daudzums, kas tiks pārsūtīts katram Kanban.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="ca2b5-124">Laukā Fiksētais Kanban daudzums ievadiet "2".</span><span class="sxs-lookup"><span data-stu-id="ca2b5-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="ca2b5-125">Tas ir Kanban daudzums, kuram jābūt aktīvam.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="ca2b5-126">Šajā gadījumā, katrs no 2 Kanban pārsūta 5.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="ca2b5-127">Laukā Minimālā brīdinājuma robeža ievadiet "1".</span><span class="sxs-lookup"><span data-stu-id="ca2b5-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="ca2b5-128">Izmantojiet, lai sekotu līdzi pilnu Kanban minimālajam skaitam, kuram jābūt galamērķī.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="ca2b5-129">Piemēram, tas tiek izmantots Kanban daudzuma pārskatā.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="ca2b5-130">Laukā Maksimālā brīdinājuma robeža ievadiet "2".</span><span class="sxs-lookup"><span data-stu-id="ca2b5-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="ca2b5-131">Izmantojiet, lai sekotu līdzi pilnu Kanban maksimālajam skaitam, kuram jābūt galamērķī.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="ca2b5-132">Piemēram, tas tiek izmantots Kanban daudzuma pārskatā.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="ca2b5-133">Izveidot Kanban darbus</span><span class="sxs-lookup"><span data-stu-id="ca2b5-133">Create kanbans</span></span>
1. <span data-ttu-id="ca2b5-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-134">Click Save.</span></span>
    * <span data-ttu-id="ca2b5-135">Lai Kanban varētu izveidot, Kanban nosacījumi ir jāsaglabā.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="ca2b5-136">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-136">Click Add.</span></span>
    * <span data-ttu-id="ca2b5-137">Ņemiet vērā, ka nav neviena aktīva Kanban, tāpēc ieteicamais "Jauno Kanban skaits" ir 2. Tas ir vienāds ar "Fiksēto Kanban daudzumu".</span><span class="sxs-lookup"><span data-stu-id="ca2b5-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="ca2b5-138">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-138">Click Create.</span></span>
    * <span data-ttu-id="ca2b5-139">Šādi tiks izveidoti divi Kanban.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="ca2b5-140">Ņemiet vērā, ka šim atvilkuma Kanban nosacījumam tika izveidoti 2 Kanban pa 5 katrs.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="ca2b5-141">Šā ir pēdējā darbība šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="ca2b5-141">This is the last step in this procedure.</span></span>  


