--- 
title: "Tādu jautājumu izveide, kas ir atkarīgi no iepriekšējā jautājuma atbildes"
description: "Nosacījuma jautājumi ļauj norādīt, kurš turpinājuma jautājums tiks attēlots respondentam, pamatojoties uz iepriekšējā jautājuma atbildes."
author: ShylaThompson
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 3e0a6d63a266bf49764c8cdcfd407ff0733ea27c
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="make-questions-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="8fddd-103">Tādu jautājumu izveide, kas ir atkarīgi no iepriekšējā jautājuma atbildes</span><span class="sxs-lookup"><span data-stu-id="8fddd-103">Make questions dependent on the answer of the previous question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8fddd-104">Nosacījuma jautājumi ļauj norādīt, kurš turpinājuma jautājums tiks attēlots respondentam, pamatojoties uz iepriekšējā jautājuma atbildes.</span><span class="sxs-lookup"><span data-stu-id="8fddd-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="8fddd-105">Piemēram, ja jautājat "Jums labāk garšo kafija vai tēja?", loģisku turpinājuma jautājumu var noteikt atkarībā no tā, vai atbildētājs atbildē izvēlas kafiju vai tēju.</span><span class="sxs-lookup"><span data-stu-id="8fddd-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="8fddd-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="8fddd-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="8fddd-107">Atrodiet pastāvošu anketu</span><span class="sxs-lookup"><span data-stu-id="8fddd-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="8fddd-108">Pārejiet uz sadaļu Anketa > Dizains > Anketas.</span><span class="sxs-lookup"><span data-stu-id="8fddd-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="8fddd-109">Sarakstā atlasiet WorkFH anketa.</span><span class="sxs-lookup"><span data-stu-id="8fddd-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="8fddd-110">Pievienojiet anketai visus jautājumus un to pakārtotos jautājumus</span><span class="sxs-lookup"><span data-stu-id="8fddd-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="8fddd-111">Noklikšķiniet uz Jautājumi.</span><span class="sxs-lookup"><span data-stu-id="8fddd-111">Click Questions.</span></span>
2. <span data-ttu-id="8fddd-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8fddd-112">Click New.</span></span>
3. <span data-ttu-id="8fddd-113">Laukā Jautājums atlasiet jautājumu ar numuru 00016.</span><span class="sxs-lookup"><span data-stu-id="8fddd-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="8fddd-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8fddd-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8fddd-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8fddd-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8fddd-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8fddd-116">Click Save.</span></span>
7. <span data-ttu-id="8fddd-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8fddd-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="8fddd-118">Iestatiet anketas secību par nosacītu un norādiet, ka jautājums ir atkarīgs no atbilstoša jautājuma</span><span class="sxs-lookup"><span data-stu-id="8fddd-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="8fddd-119">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="8fddd-119">Click Edit.</span></span>
2. <span data-ttu-id="8fddd-120">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="8fddd-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="8fddd-121">Laukā Jautājumu secība atlasiet vērtību Nosacījuma.</span><span class="sxs-lookup"><span data-stu-id="8fddd-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="8fddd-122">Noklikšķiniet uz Nosacījuma jautājums.</span><span class="sxs-lookup"><span data-stu-id="8fddd-122">Click Conditional question.</span></span>
5. <span data-ttu-id="8fddd-123">Koka struktūrā atlasiet "Jautājumi\Paskaidrojiet, kāpēc sniedzāt šādu atbildi uz iepriekšējo jautājumu?".</span><span class="sxs-lookup"><span data-stu-id="8fddd-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="8fddd-124">Laukā Primārais jautājums atlasiet jautājumu ar numuru 00009</span><span class="sxs-lookup"><span data-stu-id="8fddd-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="8fddd-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8fddd-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8fddd-126">Laukā Atbilde ievadiet tās atbildes opcijas atbilžu sērijas ID, no kuras vēlaties padarīt atkarīgu šo jautājumu.</span><span class="sxs-lookup"><span data-stu-id="8fddd-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="8fddd-127">Piemēram, ievadiet 1, lai norādītu uz pirmo atbildes opciju.</span><span class="sxs-lookup"><span data-stu-id="8fddd-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="8fddd-128">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8fddd-128">Click Save.</span></span>
10. <span data-ttu-id="8fddd-129">Koka struktūrā atlasiet "Jautājumi\Par padarīto darbu saņemu pienācīgu atalgojumu."</span><span class="sxs-lookup"><span data-stu-id="8fddd-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="8fddd-130">Ievērojiet, ka jautājumu koks tika atjaunināts, lai attēlotu sakarību.</span><span class="sxs-lookup"><span data-stu-id="8fddd-130">Note that the question tree updated to show the dependency.</span></span>  


