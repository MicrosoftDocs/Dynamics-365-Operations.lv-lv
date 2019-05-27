---
title: Aizstāšanas Kanban kārtulas izveide
description: Šī procedūra aizstāj esošo kanban nosacījumu ar jaunu kanban nosacījumu noteiktā datumā.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8a9367d4796999857e473bcbe36a709d534f3b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564067"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="20fda-103">Aizstāšanas Kanban kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="20fda-103">Create a replacement kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20fda-104">Šī procedūra aizstāj esošo kanban nosacījumu ar jaunu kanban nosacījumu noteiktā datumā.</span><span class="sxs-lookup"><span data-stu-id="20fda-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="20fda-105">Tas ir noderīgi, kad ir nepieciešams saskaņot un plānot izmaiņas ražošanas plūsmā vai papildināšanas kārtulās.</span><span class="sxs-lookup"><span data-stu-id="20fda-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="20fda-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="20fda-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="20fda-107">Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie sagatavo ražošanas procesu izmanītai ražošanas plūsmai vai jauniem papildināšanas noteikumiem.</span><span class="sxs-lookup"><span data-stu-id="20fda-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="20fda-108">Šis uzdevums aizstāj kanban nosacījumu 000022 ar jaunu nosacījumu, un palielina maksimālo daudzumu jaunajam nosacījumam no 48 līdz 100.</span><span class="sxs-lookup"><span data-stu-id="20fda-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="20fda-109">Atlasiet aizstājamo kanban nosacījumu</span><span class="sxs-lookup"><span data-stu-id="20fda-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="20fda-110">Dodieties uz Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="20fda-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="20fda-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="20fda-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="20fda-112">Atlasiet kanban nosacījumu 000022.</span><span class="sxs-lookup"><span data-stu-id="20fda-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="20fda-113">Aizstāšanas Kanban kārtulas izveide</span><span class="sxs-lookup"><span data-stu-id="20fda-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="20fda-114">Noklikšķiniet uz Aizstāt kanban nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="20fda-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="20fda-115">Laukā Spēkā stāšanās datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="20fda-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="20fda-116">Izvēlieties datumu nākotnē, piemēram, vienu nedēļu uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="20fda-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="20fda-117">Šis ir datums un laiks, kad jaunais kanban nosacījums kļūst aktīvs un aizstāj veco kanban nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="20fda-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="20fda-118">Ja kanban nosacījums maina ražošanas plūsmas ceļu, var atlasīt citu darbību.</span><span class="sxs-lookup"><span data-stu-id="20fda-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="20fda-119">Šajā procedūrā mēs atstāsim aktivitāti neskartu.</span><span class="sxs-lookup"><span data-stu-id="20fda-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="20fda-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="20fda-120">Click OK.</span></span>
    * <span data-ttu-id="20fda-121">Ņemiet vērā, ka tiek izveidots jauns kanban nosacījums, lai aizstātu kanban nosacījumu 000022.</span><span class="sxs-lookup"><span data-stu-id="20fda-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="20fda-122">Spēkā stāšanās datums tiek iestatīts saskaņā ar izvēlēto datumu, aizstājot kanban nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="20fda-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="20fda-123">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="20fda-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="20fda-124">Atlasiet aizstāto kanban nosacījumu 000022.</span><span class="sxs-lookup"><span data-stu-id="20fda-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="20fda-125">Ņemiet vērā, ka aizstājamajam kanban nosacījumam ir tāds pats datums kā beigu datums, jo tas ir nosacījuma derīguma termiņš.</span><span class="sxs-lookup"><span data-stu-id="20fda-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="20fda-126">Sarakstā atlasiet 1. rindu.</span><span class="sxs-lookup"><span data-stu-id="20fda-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="20fda-127">Atlasiet jaunu kanban nosacījumu saraksta augšgalā.</span><span class="sxs-lookup"><span data-stu-id="20fda-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="20fda-128">Šis ir kanban nosacījums ar lielāko kanban nosacījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="20fda-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="20fda-129">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="20fda-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="20fda-130">Noklikšķiniet uz kanban nosacījuma numura, lai atvērtu kanban nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="20fda-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="20fda-131">Modificējiet maksimālo daudzumu kanban nosacījuma nomaiņai</span><span class="sxs-lookup"><span data-stu-id="20fda-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="20fda-132">Iestatiet maksimālo daudzumu uz "100".</span><span class="sxs-lookup"><span data-stu-id="20fda-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="20fda-133">Izvērsiet daudzumu kopsavilkuma cilni, lai redzētu lauku Maksimālais daudzums.</span><span class="sxs-lookup"><span data-stu-id="20fda-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="20fda-134">Nomainot maksimālo daudzumu uz 100, ļaus apstrādāt līdz pat 100 kanban.</span><span class="sxs-lookup"><span data-stu-id="20fda-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="20fda-135">Šā ir pēdējā darbība šajā uzdevumā.</span><span class="sxs-lookup"><span data-stu-id="20fda-135">This is the last step in this task.</span></span>  

