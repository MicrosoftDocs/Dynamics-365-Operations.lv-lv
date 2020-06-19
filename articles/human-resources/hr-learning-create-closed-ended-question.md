---
title: Slēgta jautājuma izveide
description: Slēgto jautājumu atbildēm varat norādīt opcijas, no kurām respondents var izvēlēties.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2eb53290d39fef0bf439a199dfd774138823ec2
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428620"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="1812a-103">Slēgta jautājuma izveide</span><span class="sxs-lookup"><span data-stu-id="1812a-103">Create a closed ended question</span></span>



<span data-ttu-id="1812a-104">Slēgto jautājumu atbildēm varat norādīt opcijas, no kurām respondents var izvēlēties.</span><span class="sxs-lookup"><span data-stu-id="1812a-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="1812a-105">Pirmkārt, nepieciešams izveidot atbilžu grupu ar atbildēm, tad jāizveido jautājums, kas izmantos šo atbilžu grupu.</span><span class="sxs-lookup"><span data-stu-id="1812a-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="1812a-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="1812a-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="1812a-107">Atbilžu grupas izveide</span><span class="sxs-lookup"><span data-stu-id="1812a-107">Create an answer group</span></span>
1. <span data-ttu-id="1812a-108">Dodieties uz Anketa > Dizains > Atbilžu grupas.</span><span class="sxs-lookup"><span data-stu-id="1812a-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="1812a-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1812a-109">Click New.</span></span>
3. <span data-ttu-id="1812a-110">Ierakstiet vērtību laukā Atbilžu grupa.</span><span class="sxs-lookup"><span data-stu-id="1812a-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="1812a-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1812a-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1812a-112">Izmantojiet funkcionalitāti Kārtot nejaušā secībā, lai nejauši izvietotu atbildes citā secībā katru reizi, kad atbilžu grupa tiek izmantota jautājumam.</span><span class="sxs-lookup"><span data-stu-id="1812a-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="1812a-113">Noklikšķiniet uz Atbilde.</span><span class="sxs-lookup"><span data-stu-id="1812a-113">Click Answer.</span></span>
6. <span data-ttu-id="1812a-114">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1812a-114">Click New.</span></span>
    * <span data-ttu-id="1812a-115">Sērijas numurs kontrolē secību, kādā tiek parādītas atbildes, ja vien atbilžu grupai nav atzīmēta funkcionalitāte Kārtot nejaušā secībā.</span><span class="sxs-lookup"><span data-stu-id="1812a-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="1812a-116">Atbildēm var piešķirt punktus, kuri tiek izmantoti anketas vērtēšanā.</span><span class="sxs-lookup"><span data-stu-id="1812a-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="1812a-117">Ievadiet skaitli laukā Punkti.</span><span class="sxs-lookup"><span data-stu-id="1812a-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="1812a-118">Pareizo atbildi var iezīmēt, lai norādītu, ka atlasītā atbilde ir pareiza.</span><span class="sxs-lookup"><span data-stu-id="1812a-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="1812a-119">To var izmantot anketas punktu skaitīšanai.</span><span class="sxs-lookup"><span data-stu-id="1812a-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="1812a-120">Ierakstiet vērtību laukā Atbilde.</span><span class="sxs-lookup"><span data-stu-id="1812a-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="1812a-121">Turpiniet veidot atbilžu grupas atbilžu atlases opcijas.</span><span class="sxs-lookup"><span data-stu-id="1812a-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="1812a-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1812a-122">Click New.</span></span>
10. <span data-ttu-id="1812a-123">Ievadiet skaitli laukā Punkti.</span><span class="sxs-lookup"><span data-stu-id="1812a-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="1812a-124">Ierakstiet vērtību laukā Atbilde.</span><span class="sxs-lookup"><span data-stu-id="1812a-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="1812a-125">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="1812a-125">Click New.</span></span>
13. <span data-ttu-id="1812a-126">Ievadiet skaitli laukā Punkti.</span><span class="sxs-lookup"><span data-stu-id="1812a-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="1812a-127">Ierakstiet vērtību laukā Atbilde.</span><span class="sxs-lookup"><span data-stu-id="1812a-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="1812a-128">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="1812a-128">Click New.</span></span>
16. <span data-ttu-id="1812a-129">Ievadiet skaitli laukā Punkti.</span><span class="sxs-lookup"><span data-stu-id="1812a-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="1812a-130">Ierakstiet vērtību laukā Atbilde.</span><span class="sxs-lookup"><span data-stu-id="1812a-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="1812a-131">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="1812a-131">Click New.</span></span>
19. <span data-ttu-id="1812a-132">Ievadiet skaitli laukā Punkti.</span><span class="sxs-lookup"><span data-stu-id="1812a-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="1812a-133">Ierakstiet vērtību laukā Atbilde.</span><span class="sxs-lookup"><span data-stu-id="1812a-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="1812a-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1812a-134">Close the page.</span></span>
22. <span data-ttu-id="1812a-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1812a-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="1812a-136">Jautājuma izveide</span><span class="sxs-lookup"><span data-stu-id="1812a-136">Create the question</span></span>
1. <span data-ttu-id="1812a-137">Pārejiet uz sadaļu Anketa> Dizains > Jautājumi.</span><span class="sxs-lookup"><span data-stu-id="1812a-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="1812a-138">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1812a-138">Click New.</span></span>
3. <span data-ttu-id="1812a-139">Izmantojiet lauku Tips, lai sagrupētu saistītus jautājumus.</span><span class="sxs-lookup"><span data-stu-id="1812a-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="1812a-140">Slēgtiem jautājumiem varat izmantot tādus ievades tipus kā izvēles rūtiņa, alternatīvā poga vai kombinētais lodziņš.</span><span class="sxs-lookup"><span data-stu-id="1812a-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="1812a-141">Atlasiet opciju laukā Ievades tips.</span><span class="sxs-lookup"><span data-stu-id="1812a-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="1812a-142">Laukā Atbilžu grupa ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1812a-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="1812a-143">Ierakstiet vērtību laukā Teksts.</span><span class="sxs-lookup"><span data-stu-id="1812a-143">In the Text field, type a value.</span></span>

