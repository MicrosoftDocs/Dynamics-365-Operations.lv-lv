---
title: Nodarbināto atvieglojumu plānu izveide
description: Varat izveidot nodarbināto atvieglojumu plānus Microsoft Dynamics 365 Human Resources, lai atlasītu atvieglojumu plānus darbiniekiem un apstiprinātu atvieglojumu plāna atlases.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5ac357bbef4bf84b9eaf153834bc7a609240c45e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464230"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="91344-103">Nodarbināto atvieglojumu plānu izveide</span><span class="sxs-lookup"><span data-stu-id="91344-103">Create worker benefit plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="91344-104">Varat izveidot nodarbināto atvieglojumu plānus Microsoft Dynamics 365 Human Resources, lai atlasītu atvieglojumu plānus darbiniekiem un apstiprinātu atvieglojumu plāna atlases.</span><span class="sxs-lookup"><span data-stu-id="91344-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="91344-105">Parasti darbinieki paši atlasa atvieglojumu plānus, izmantojot darbinieku patstāvīgi izmantojamo pakalpojumu, un pēc tam atvieglojumu administrators apstiprina atlases.</span><span class="sxs-lookup"><span data-stu-id="91344-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="91344-106">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Plāni** atlasiet **Nodarbināto atvieglojumu plāni**.</span><span class="sxs-lookup"><span data-stu-id="91344-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="91344-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="91344-107">Select **New**.</span></span>

3. <span data-ttu-id="91344-108">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="91344-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="91344-109">Lauks</span><span class="sxs-lookup"><span data-stu-id="91344-109">Field</span></span> | <span data-ttu-id="91344-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="91344-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="91344-111">Periods</span><span class="sxs-lookup"><span data-stu-id="91344-111">Period</span></span> | <span data-ttu-id="91344-112">Norāda atvieglojumu periodu, ko izmantot, lai filtrētu plānus kopsavilkuma cilnē Plāni. Filtrē plānus, lai palīdzētu veikt atlasi no visu plānu ierakstu apakškopas, lai varētu apstiprināt apakškopu.</span><span class="sxs-lookup"><span data-stu-id="91344-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="91344-113">Piemēram, atlasiet izveidoto periodu ar nosaukumu 2015, lai apstiprinātu visas atvieglojumu reģistrācijas atlases 2015. gadam.</span><span class="sxs-lookup"><span data-stu-id="91344-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="91344-114">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="91344-114">Worker</span></span> | <span data-ttu-id="91344-115">Norāda nodarbināto, kuru izmantot, lai filtrētu plānus kopsavilkuma cilnē Plāni. Filtrē plānus, lai palīdzētu veikt atlasi no visu plānu ierakstu apakškopas, lai varētu apstiprināt apakškopu.</span><span class="sxs-lookup"><span data-stu-id="91344-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="91344-116">Juridiska persona</span><span class="sxs-lookup"><span data-stu-id="91344-116">Legal entity</span></span> | <span data-ttu-id="91344-117">Norāda juridisko personu, ko izmantot, lai filtrētu plānus kopsavilkuma cilnē Plāni. Filtrē plānus, lai palīdzētu veikt atlasi no visu plānu ierakstu apakškopas, lai varētu apstiprināt apakškopu.</span><span class="sxs-lookup"><span data-stu-id="91344-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="91344-118">Vajadzības opcija</span><span class="sxs-lookup"><span data-stu-id="91344-118">Coverage option</span></span> | <span data-ttu-id="91344-119">Norāda seguma opciju, ko izmantot, lai filtrētu plānus kopsavilkuma cilnē Plāni. Filtrē plānus, lai palīdzētu veikt atlasi no visu plānu ierakstu apakškopas, lai varētu apstiprināt apakškopu.</span><span class="sxs-lookup"><span data-stu-id="91344-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="91344-120">Noklusējuma vērtība</span><span class="sxs-lookup"><span data-stu-id="91344-120">Default</span></span> | <span data-ttu-id="91344-121">Filtrē atvieglojumu plānus, pamatojoties uz to, vai tie ir noklusējuma plāni.</span><span class="sxs-lookup"><span data-stu-id="91344-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="91344-122">Filtrē plānus, lai palīdzētu veikt atlasi no visu plānu ierakstu apakškopas, lai varētu apstiprināt apakškopu.</span><span class="sxs-lookup"><span data-stu-id="91344-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="91344-123">Statuss</span><span class="sxs-lookup"><span data-stu-id="91344-123">Status</span></span> | <span data-ttu-id="91344-124">Filtrē atvieglojumu plānus, pamatojoties uz to statusu.</span><span class="sxs-lookup"><span data-stu-id="91344-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="91344-125">Filtrē plānus, lai palīdzētu veikt atlasi no visu plānu ierakstu apakškopas, lai varētu apstiprināt apakškopu.</span><span class="sxs-lookup"><span data-stu-id="91344-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="91344-126">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="91344-126">Confirmation</span></span> | <span data-ttu-id="91344-127">Norāda apstiprinājuma statusu, ko izmantot, lai filtrētu plānus kopsavilkuma cilnē Plāni. Filtrē plānus, lai palīdzētu veikt atlasi no visu plānu ierakstu apakškopas, lai varētu apstiprināt apakškopu.</span><span class="sxs-lookup"><span data-stu-id="91344-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="91344-128">Atcelšana</span><span class="sxs-lookup"><span data-stu-id="91344-128">Cancellation</span></span> | <span data-ttu-id="91344-129">Norāda atcelšanas statusu, ko izmantot, lai filtrētu plānus kopsavilkuma cilnē Plāni. Filtrē plānus, lai palīdzētu veikt atlasi no visu plānu ierakstu apakškopas, lai varētu apstiprināt apakškopu.</span><span class="sxs-lookup"><span data-stu-id="91344-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="91344-130">Efektīvs datuma filtrs</span><span class="sxs-lookup"><span data-stu-id="91344-130">Effective date filter</span></span> | <span data-ttu-id="91344-131">Filtrē plānus atkarībā no tā, vai tiem beidzies darbības termiņš, vai tie ir aktīvi vai būs aktīvi nākotnē.</span><span class="sxs-lookup"><span data-stu-id="91344-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="91344-132">Atlasiet izvēles rūtiņas, kas atbilst plāniem, ko vēlaties redzēt kopsavilkuma cilnē Plāni.</span><span class="sxs-lookup"><span data-stu-id="91344-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="91344-133">Plāni</span><span class="sxs-lookup"><span data-stu-id="91344-133">Plans</span></span> | <span data-ttu-id="91344-134">Kopsavilkuma cilne plāni satur plānus, kas atbilst norādītajiem filtrēšanas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="91344-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="91344-135">Atbilstošās konfigurācijas opcijas, ko iestatīja personāla vadības darbinieki, un darbinieku izvēlētās reģistrācijas atlases tiek iekļautas katrā rindā.</span><span class="sxs-lookup"><span data-stu-id="91344-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="91344-136">Lauks Kvalificējušies norāda, vai pastāv pārbaudes konflikts ar plāna atlasi.</span><span class="sxs-lookup"><span data-stu-id="91344-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="91344-137">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="91344-137">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]