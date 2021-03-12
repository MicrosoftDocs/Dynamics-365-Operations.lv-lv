---
title: Fiksēta daudzuma Kanban kārtulu izveide ražošanai
description: Šī procedūra fokusējas iestatījumiem, kas nepieciešami, lai izveidotu fiksētus ražošanas Kanban nosacījumus transformēšanas aktivitāšu palaišanai darba šūnā racionālā vidē.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af912ecfb07a7af2f299e354243ba0d80c063a9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981310"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="7d129-103">Fiksēta daudzuma Kanban kārtulu izveide ražošanai</span><span class="sxs-lookup"><span data-stu-id="7d129-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d129-104">Šī procedūra fokusējas iestatījumiem, kas nepieciešami, lai izveidotu fiksētus ražošanas Kanban nosacījumus transformēšanas aktivitāšu palaišanai darba šūnā racionālā vidē.</span><span class="sxs-lookup"><span data-stu-id="7d129-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="7d129-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="7d129-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7d129-106">Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jaunas vai modificētas preces ražošanai.</span><span class="sxs-lookup"><span data-stu-id="7d129-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="7d129-107">Jaunu Kanban nosacījumu izveide</span><span class="sxs-lookup"><span data-stu-id="7d129-107">Create new kanban rule</span></span>
1. <span data-ttu-id="7d129-108">Dodieties uz Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="7d129-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="7d129-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="7d129-109">Click New.</span></span>
    * <span data-ttu-id="7d129-110">Ievērojiet, ka noklusējuma Tips ir Ražošana un Papildināšanas stratēģija ir Fiksēts.</span><span class="sxs-lookup"><span data-stu-id="7d129-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="7d129-111">Šie parametri nav jāmaina.</span><span class="sxs-lookup"><span data-stu-id="7d129-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="7d129-112">Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d129-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="7d129-113">Tā ir aktivitāte, kas tiks veikta Kanban, kas izveidoti, pamatojoties uz šiem Kanban nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="7d129-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="7d129-114">Atlasiet "SpeakerTestAndPackaging".</span><span class="sxs-lookup"><span data-stu-id="7d129-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="7d129-115">Izvērsiet sadaļu Detalizēti.</span><span class="sxs-lookup"><span data-stu-id="7d129-115">Expand the Details section.</span></span>
5. <span data-ttu-id="7d129-116">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d129-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="7d129-117">Atlasiet L0050.</span><span class="sxs-lookup"><span data-stu-id="7d129-117">Select L0050.</span></span>  
6. <span data-ttu-id="7d129-118">Laukā Mērvienība ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7d129-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="7d129-119">Atlasiet minūtes.</span><span class="sxs-lookup"><span data-stu-id="7d129-119">Select minutes.</span></span>  
7. <span data-ttu-id="7d129-120">Laukā Izpildes laiks ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="7d129-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="7d129-121">Ievadiet 5.</span><span class="sxs-lookup"><span data-stu-id="7d129-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="7d129-122">Daudzumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7d129-122">Set quantities</span></span>
1. <span data-ttu-id="7d129-123">Izvērsiet sadaļu Daudzumi.</span><span class="sxs-lookup"><span data-stu-id="7d129-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="7d129-124">Vienumam Noklusējuma daudzums iestatiet vērtību "10".</span><span class="sxs-lookup"><span data-stu-id="7d129-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="7d129-125">Tas ir daudzums, kas tiks pārsūtīts katram Kanban.</span><span class="sxs-lookup"><span data-stu-id="7d129-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="7d129-126">Atzīmējiet izvēles rūtiņu Preču daudzuma novirze.</span><span class="sxs-lookup"><span data-stu-id="7d129-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="7d129-127">Ar šo, atlasītos Kanban var papildināt ar novirzi no noklusējuma daudzuma.</span><span class="sxs-lookup"><span data-stu-id="7d129-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="7d129-128">Lai atļautu papildināt Kanban ar daudzumu no 8 līdz 12, iestatiet abas novirzes uz 2.</span><span class="sxs-lookup"><span data-stu-id="7d129-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="7d129-129">Iestatiet Novirze zem uz "2".</span><span class="sxs-lookup"><span data-stu-id="7d129-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="7d129-130">Tas ļaus papildināt līdz pat 10 - 2 = 8</span><span class="sxs-lookup"><span data-stu-id="7d129-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="7d129-131">Iestatiet Novirze virs uz "2".</span><span class="sxs-lookup"><span data-stu-id="7d129-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="7d129-132">Tas ļaus papildināt līdz pat 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="7d129-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="7d129-133">Laukā Fiksēts Kanban daudzums ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="7d129-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="7d129-134">Tas ir Kanban daudzums, kuram jābūt aktīvam.</span><span class="sxs-lookup"><span data-stu-id="7d129-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="7d129-135">Šajā gadījumā, katrs no 5 Kanban apstrādā 10.</span><span class="sxs-lookup"><span data-stu-id="7d129-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="7d129-136">Laukā Minimālā brīdinājuma robeža ievadiet "2".</span><span class="sxs-lookup"><span data-stu-id="7d129-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="7d129-137">Izmantojiet, lai sekotu līdzi pilnu Kanban minimālajam skaitam, kuram jābūt galamērķī.</span><span class="sxs-lookup"><span data-stu-id="7d129-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="7d129-138">Piemēram, tas tiek izmantots Kanban daudzuma pārskatā.</span><span class="sxs-lookup"><span data-stu-id="7d129-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="7d129-139">Laukā Maksimālā brīdinājuma robeža ievadiet "4".</span><span class="sxs-lookup"><span data-stu-id="7d129-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="7d129-140">Izmantojiet, lai sekotu līdzi pilnu Kanban maksimālajam skaitam, kuram jābūt galamērķī.</span><span class="sxs-lookup"><span data-stu-id="7d129-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="7d129-141">Piemēram, tas tiek izmantots Kanban daudzuma pārskatā.</span><span class="sxs-lookup"><span data-stu-id="7d129-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="7d129-142">Laukā Automātiskais plānošanas daudzums ievadiet "1".</span><span class="sxs-lookup"><span data-stu-id="7d129-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="7d129-143">Iestatot šo uz 1 nozīmē, ka katrs Kanban tiks automātiski plānots.</span><span class="sxs-lookup"><span data-stu-id="7d129-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="7d129-144">Ievadot 3, Kanban netiks plānoti, kamēr plānošanai nebūs gatavi 3 tukši Kanban.</span><span class="sxs-lookup"><span data-stu-id="7d129-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="7d129-145">Tas ir noderīgi darbu grupēšanai, izvairoties no pārāk daudziem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="7d129-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="7d129-146">Vairāku Kanban izveide</span><span class="sxs-lookup"><span data-stu-id="7d129-146">Create Kanbans</span></span>
1. <span data-ttu-id="7d129-147">Izvērsiet sadaļu Vairāki Kanban.</span><span class="sxs-lookup"><span data-stu-id="7d129-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="7d129-148">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="7d129-148">Click Save.</span></span>
    * <span data-ttu-id="7d129-149">Lai Kanban varētu izveidot, Kanban nosacījumi ir jāsaglabā.</span><span class="sxs-lookup"><span data-stu-id="7d129-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="7d129-150">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="7d129-150">Click Add.</span></span>
    * <span data-ttu-id="7d129-151">Ņemiet vērā: tā kā nav neviena aktīva Kanban, ieteiktā opcijas "Jaunu Kanban skaits" vērtība ir 5.</span><span class="sxs-lookup"><span data-stu-id="7d129-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="7d129-152">Tas ir vienāds ar vērtību "Fiksēts Kanban daudzums".</span><span class="sxs-lookup"><span data-stu-id="7d129-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="7d129-153">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="7d129-153">Click Create.</span></span>
    * <span data-ttu-id="7d129-154">Šādi tiks izveidoti 5 Kanban.</span><span class="sxs-lookup"><span data-stu-id="7d129-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="7d129-155">Ņemiet vērā, ka šim ražošanas Kanban nosacījumam tika izveidoti 5 Kanban pa 10 katrs.</span><span class="sxs-lookup"><span data-stu-id="7d129-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="7d129-156">Šā ir pēdējā darbība šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="7d129-156">This is the last step in this procedure.</span></span>  

