---
title: Anketas rezultātu analizēšana
description: Anketu statistiku var izmantot, lai aprēķinātu vidējās vērtības, kopsummas un procentus, balstoties uz demogrāfisko datu kopu.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d8f9c2fcf0be117f8fcde5113c0d42f11786679
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "858587"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="439b6-103">Anketas rezultātu analizēšana</span><span class="sxs-lookup"><span data-stu-id="439b6-103">Analyzing questionnaire results</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="439b6-104">Anketu statistiku var izmantot, lai aprēķinātu vidējās vērtības, kopsummas un procentus, balstoties uz demogrāfisko datu kopu.</span><span class="sxs-lookup"><span data-stu-id="439b6-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="439b6-105">Lai sāktu šo procedūru, pārejiet uz sadaļu Anketa > Skatīt un analizēt rezultātus > Anketas statistika.</span><span class="sxs-lookup"><span data-stu-id="439b6-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="439b6-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="439b6-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="439b6-107">Anketas statistikas ieraksta izveide</span><span class="sxs-lookup"><span data-stu-id="439b6-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="439b6-108">Dodieties uz sadaļu Anketas statistika.</span><span class="sxs-lookup"><span data-stu-id="439b6-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="439b6-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="439b6-109">Click New.</span></span>
3. <span data-ttu-id="439b6-110">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="439b6-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="439b6-111">Ierakstiet vērtību laukā Statistika.</span><span class="sxs-lookup"><span data-stu-id="439b6-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="439b6-112">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="439b6-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="439b6-113">Laukā Anketa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="439b6-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="439b6-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="439b6-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="439b6-115">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="439b6-115">Click the General tab.</span></span>
    * <span data-ttu-id="439b6-116">Atlasiet, vai vēlaties ietvert anonīmus rezultātus vai rezultātus no darbiniekiem, kontaktpersonām un kandidātiem.</span><span class="sxs-lookup"><span data-stu-id="439b6-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="439b6-117">Atzīmējiet izvēles rūtiņu Darbinieks vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="439b6-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="439b6-118">Ja skatīsit rezultātus pēc darba stāža vai vecuma, norādiet intervālus, kurus vēlaties izmantot rezultātu grupēšanai.</span><span class="sxs-lookup"><span data-stu-id="439b6-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="439b6-119">Ievadot vecuma intervālu 5, rezultāti tiks grupēti, ņemot vērā piecu gadu vecuma intervālus.</span><span class="sxs-lookup"><span data-stu-id="439b6-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="439b6-120">Ievadiet skaitli laukā Vecums.</span><span class="sxs-lookup"><span data-stu-id="439b6-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="439b6-121">Atlasiet, vai vēlaties veikt aprēķinu visai anketai, katrai rezultātu grupai, katram jautājumam vai katrai jautājuma rindai.</span><span class="sxs-lookup"><span data-stu-id="439b6-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="439b6-122">Atlasiet veidu, kādā vēlaties rezultātus grupēt.</span><span class="sxs-lookup"><span data-stu-id="439b6-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="439b6-123">Piemēram, ja aprēķināt vidējo punktu skaitu par katru jautājumu, varat apskatīt jautājumus, kas grupēti pēc rezultātu grupas.</span><span class="sxs-lookup"><span data-stu-id="439b6-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="439b6-124">Atlasiet datus, uz kuriem balstīt aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="439b6-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="439b6-125">Piemēram, ja vēlaties redzēt saņemto vidējo procentuālo daļu anketā starp jūsu darbiniekiem pret vidējo punktu skaitu starp jūsu darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="439b6-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="439b6-126">Noklikšķiniet uz cilnes Diapazons.</span><span class="sxs-lookup"><span data-stu-id="439b6-126">Click the Range tab.</span></span>
    * <span data-ttu-id="439b6-127">Izmantojiet diapazonus, lai ierobežotu rezultātu kopu, atstājot tikai tos, kas atbilst diapazona kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="439b6-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="439b6-128">Noklikšķiniet uz cilnes Grupēšana pēc.</span><span class="sxs-lookup"><span data-stu-id="439b6-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="439b6-129">Lai noteiktu, kā rezultāti ir jāattēlo, izmantojiet grupējumus.</span><span class="sxs-lookup"><span data-stu-id="439b6-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="439b6-130">Piemēram, grupējiet rezultātus pēc dzimuma un tad pēc vecuma.</span><span class="sxs-lookup"><span data-stu-id="439b6-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="439b6-131">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="439b6-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="439b6-132">Pārvietojiet grupējumus uz pusi Atlasīts un izvietojiet tos vēlamajā secībā.</span><span class="sxs-lookup"><span data-stu-id="439b6-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="439b6-133">Statistikas aprēķina izpilde</span><span class="sxs-lookup"><span data-stu-id="439b6-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="439b6-134">Noklikšķiniet uz Izpildīt.</span><span class="sxs-lookup"><span data-stu-id="439b6-134">Click Execute.</span></span>
    * <span data-ttu-id="439b6-135">Atlasiet aprēķina funkciju, kuru vēlaties pielietot rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="439b6-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="439b6-136">Piemēram, aprēķiniet vidējo procentuālo daļu anketā atlasītajiem grupējumiem vai kopējo punktu skaitu rezultātu grupām izvēlētajiem grupējumiem.</span><span class="sxs-lookup"><span data-stu-id="439b6-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="439b6-137">Atlasiet vai izņemiet atzīmi no izvēles rūtiņas Dzēst iepriekš meklēto.</span><span class="sxs-lookup"><span data-stu-id="439b6-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="439b6-138">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="439b6-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="439b6-139">Skatiet anketas statistikas laidiena rezultātus.</span><span class="sxs-lookup"><span data-stu-id="439b6-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="439b6-140">Klikšķiniet Rezultāts.</span><span class="sxs-lookup"><span data-stu-id="439b6-140">Click Result.</span></span>
2. <span data-ttu-id="439b6-141">Klikšķiniet Rezultāts.</span><span class="sxs-lookup"><span data-stu-id="439b6-141">Click Result.</span></span>
3. <span data-ttu-id="439b6-142">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="439b6-142">Close the page.</span></span>

