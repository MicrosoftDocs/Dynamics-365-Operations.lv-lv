--- 
title: "Jautājuma izveide, kas atkarīgs no iepriekšējā jautājuma atbildes"
description: "Nosacījuma jautājumi ļauj norādīt, kurš turpinājuma jautājums tiks attēlots respondentam, pamatojoties uz iepriekšējā jautājuma atbildes."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: deb79398f5a0ebdbdb774c106c90ca50a69c275e
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="4c44a-103">Jautājuma izveide, kas atkarīgs no iepriekšējā jautājuma atbildes</span><span class="sxs-lookup"><span data-stu-id="4c44a-103">Make a question dependent on the answer of the previous question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c44a-104">Nosacījuma jautājumi ļauj norādīt, kurš turpinājuma jautājums tiks attēlots respondentam, pamatojoties uz iepriekšējā jautājuma atbildes.</span><span class="sxs-lookup"><span data-stu-id="4c44a-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="4c44a-105">Piemēram, ja jautājat "Jums labāk garšo kafija vai tēja?", loģisku turpinājuma jautājumu var noteikt atkarībā no tā, vai atbildētājs atbildē izvēlas kafiju vai tēju.</span><span class="sxs-lookup"><span data-stu-id="4c44a-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="4c44a-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="4c44a-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="4c44a-107">Atrodiet pastāvošu anketu</span><span class="sxs-lookup"><span data-stu-id="4c44a-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="4c44a-108">Pārejiet uz sadaļu Anketa > Dizains > Anketas.</span><span class="sxs-lookup"><span data-stu-id="4c44a-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="4c44a-109">Sarakstā atlasiet WorkFH anketa.</span><span class="sxs-lookup"><span data-stu-id="4c44a-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="4c44a-110">Pievienojiet anketai visus jautājumus un to pakārtotos jautājumus</span><span class="sxs-lookup"><span data-stu-id="4c44a-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="4c44a-111">Noklikšķiniet uz Jautājumi.</span><span class="sxs-lookup"><span data-stu-id="4c44a-111">Click Questions.</span></span>
2. <span data-ttu-id="4c44a-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4c44a-112">Click New.</span></span>
3. <span data-ttu-id="4c44a-113">Laukā Jautājums atlasiet jautājumu ar numuru 00016.</span><span class="sxs-lookup"><span data-stu-id="4c44a-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="4c44a-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4c44a-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4c44a-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4c44a-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4c44a-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4c44a-116">Click Save.</span></span>
7. <span data-ttu-id="4c44a-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="4c44a-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="4c44a-118">Iestatiet anketas secību par nosacītu un norādiet, ka jautājums ir atkarīgs no atbilstoša jautājuma</span><span class="sxs-lookup"><span data-stu-id="4c44a-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="4c44a-119">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="4c44a-119">Click Edit.</span></span>
2. <span data-ttu-id="4c44a-120">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="4c44a-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="4c44a-121">Laukā Jautājumu secība atlasiet vērtību Nosacījuma.</span><span class="sxs-lookup"><span data-stu-id="4c44a-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="4c44a-122">Noklikšķiniet uz Nosacījuma jautājums.</span><span class="sxs-lookup"><span data-stu-id="4c44a-122">Click Conditional question.</span></span>
5. <span data-ttu-id="4c44a-123">Koka struktūrā atlasiet "Jautājumi\Paskaidrojiet, kāpēc sniedzāt šādu atbildi uz iepriekšējo jautājumu?".</span><span class="sxs-lookup"><span data-stu-id="4c44a-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="4c44a-124">Laukā Primārais jautājums atlasiet jautājumu ar numuru 00009</span><span class="sxs-lookup"><span data-stu-id="4c44a-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="4c44a-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4c44a-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4c44a-126">Laukā Atbilde ievadiet tās atbildes opcijas atbilžu sērijas ID, no kuras vēlaties padarīt atkarīgu šo jautājumu.</span><span class="sxs-lookup"><span data-stu-id="4c44a-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="4c44a-127">Piemēram, ievadiet 1, lai norādītu uz pirmo atbildes opciju.</span><span class="sxs-lookup"><span data-stu-id="4c44a-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="4c44a-128">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4c44a-128">Click Save.</span></span>
10. <span data-ttu-id="4c44a-129">Koka struktūrā atlasiet "Jautājumi\Par padarīto darbu saņemu pienācīgu atalgojumu."</span><span class="sxs-lookup"><span data-stu-id="4c44a-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="4c44a-130">Ievērojiet, ka jautājumu koks tika atjaunināts, lai attēlotu sakarību.</span><span class="sxs-lookup"><span data-stu-id="4c44a-130">Note that the question tree updated to show the dependency.</span></span>  


