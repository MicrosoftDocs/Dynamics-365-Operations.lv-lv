---
title: Aptauju sadalīšana, izmantojot plānošanu
description: Izmantojot anketēšanas plānošanu, var plānot un sadalīt anketas vairākiem respondentiem.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0448a7ebe802a961c8c1296ef57d12ea22e4ec27
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009831"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="1ec75-103">Aptauju sadalīšana, izmantojot plānošanu</span><span class="sxs-lookup"><span data-stu-id="1ec75-103">Distribute questionnaires using scheduling</span></span>

<span data-ttu-id="1ec75-104">Izmantojot anketēšanas plānošanu, var plānot un sadalīt anketas vairākiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="1ec75-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="1ec75-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="1ec75-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="1ec75-106">Izveidot anketas grafiku</span><span class="sxs-lookup"><span data-stu-id="1ec75-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="1ec75-107">Pārejiet uz sadaļu Anketa > Sadale > Anketēšanas grafiki.</span><span class="sxs-lookup"><span data-stu-id="1ec75-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="1ec75-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1ec75-108">Click New.</span></span>

3. <span data-ttu-id="1ec75-109">Ierakstiet vērtību laukā Plānošana.</span><span class="sxs-lookup"><span data-stu-id="1ec75-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="1ec75-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ec75-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1ec75-111">Iestatiet grafika statusu Anonīms, ja atbildes ir jāreģistrē bez vārda un uzvārda saistīšanas ar atbildi.</span><span class="sxs-lookup"><span data-stu-id="1ec75-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="1ec75-112">Lai iespējotu anonīmus rezultātus, vispirms ir jāiestata personāla vadības parametrus.</span><span class="sxs-lookup"><span data-stu-id="1ec75-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="1ec75-113">Laukā Veids atlasiet plānošanas veidu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="1ec75-114">Šajā piemērā tiks izmantots Apmierinātības tips.</span><span class="sxs-lookup"><span data-stu-id="1ec75-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="1ec75-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="1ec75-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1ec75-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="1ec75-117">Laukā Datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="1ec75-118">Izvērsiet sadaļu E-pasta ziņojums darbinieku patstāvīgai izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="1ec75-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="1ec75-119">Ierakstiet vērtību laukā Tēma.</span><span class="sxs-lookup"><span data-stu-id="1ec75-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="1ec75-120">Piemērs: Anketa pieejama</span><span class="sxs-lookup"><span data-stu-id="1ec75-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="1ec75-121">Teksta laukā ierakstiet e-pasta ziņojuma pamattekstu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="1ec75-122">Ņemiet vērā, ka mainīgais var tikt izmantots, lai aizstātu vērtības sistēmā.</span><span class="sxs-lookup"><span data-stu-id="1ec75-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="1ec75-123">Piemērs: Cien. %P%! Lūdzu, piesakieties darbinieku pašapkalpes pakalpojumā, lai aizpildītu darbaspēka veselības novērtējuma anketu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="1ec75-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="1ec75-124">Contoso</span></span>  

12. <span data-ttu-id="1ec75-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1ec75-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="1ec75-126">Izmantojiet detalizētu informācija par Iestatīšanu, lai atlasītu anketu(as), kura(s) jāatbild, kā arī vaicājumus, kas ir jāizmanto respondentu atlasei.</span><span class="sxs-lookup"><span data-stu-id="1ec75-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="1ec75-127">Noklikšķināt uz Detalizēta informācija par iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-127">Click Setup details.</span></span>

2. <span data-ttu-id="1ec75-128">Sarakstā atlasiet vaicājumu, ko izmantot, lai veiktu anketas respondentu meklēšanu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="1ec75-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="1ec75-129">Piemērs: Darbinieki</span><span class="sxs-lookup"><span data-stu-id="1ec75-129">Example: Workers</span></span>  

3. <span data-ttu-id="1ec75-130">Noklikšķiniet uz Skatīt vai mainīt vaicājumu, lai atlasītu konkrētas personas vai pielāgotu vaicājumu un atrastu personas, kas atbilst noteiktiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="1ec75-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="1ec75-131">Ņemiet vērā, ka visiem respondentiem ir jābūt arī sistēmas lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="1ec75-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="1ec75-132">Sarakstā atzīmējiet rindu Personai</span><span class="sxs-lookup"><span data-stu-id="1ec75-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="1ec75-133">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1ec75-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="1ec75-134">Atlasiet Jūlija Funderburka</span><span class="sxs-lookup"><span data-stu-id="1ec75-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="1ec75-135">Sarakstā atlasiet Jūlija Funderburka</span><span class="sxs-lookup"><span data-stu-id="1ec75-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="1ec75-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ec75-136">Click OK.</span></span>

8. <span data-ttu-id="1ec75-137">Noklikšķiniet uz cilnes Anketas.</span><span class="sxs-lookup"><span data-stu-id="1ec75-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="1ec75-138">Kokā izvērsiet 'mezglu anketas tipam Apmierinātības aptauja'.</span><span class="sxs-lookup"><span data-stu-id="1ec75-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="1ec75-139">Kokā pārbaudiet 'Darbaspēka veselības novērtējums'.</span><span class="sxs-lookup"><span data-stu-id="1ec75-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="1ec75-140">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ec75-140">Click OK.</span></span>

12. <span data-ttu-id="1ec75-141">Noklikšķiniet uz Plānotā atbilžu sesija.</span><span class="sxs-lookup"><span data-stu-id="1ec75-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="1ec75-142">Ņemiet vērā, ka plānotās atbilžu sesijas ir izveidotas katram atlasītajam vai anketētajam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="1ec75-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="1ec75-143">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="1ec75-144">Sāciet anketēšanas grafiku, lai respondents var piekļūt anketai un to aizpildīt.</span><span class="sxs-lookup"><span data-stu-id="1ec75-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="1ec75-145">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="1ec75-145">Click Functions.</span></span>

2. <span data-ttu-id="1ec75-146">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="1ec75-146">Click Start.</span></span>

3. <span data-ttu-id="1ec75-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ec75-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="1ec75-148">Nosūtiet e-pasta ziņojumu, lai informētu respondentus par pieejamo anketu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="1ec75-149">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="1ec75-149">Click Functions.</span></span>

2. <span data-ttu-id="1ec75-150">Noklikšķiniet uz Sūtīt e-pasta ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-150">Click Send email.</span></span>

3. <span data-ttu-id="1ec75-151">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="1ec75-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="1ec75-152">Izmantojiet plānotās atbilžu sesijas, lai pārraudzītu, kam ir jāaizpilda anketa.</span><span class="sxs-lookup"><span data-stu-id="1ec75-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="1ec75-153">Noklikšķiniet uz Plānotā atbilžu sesija.</span><span class="sxs-lookup"><span data-stu-id="1ec75-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="1ec75-154">Dzēsiet visas atlikušās plānotās atbilžu sesijas, kad viss ir sagatavots plānotās sesijas pabeigšanai.</span><span class="sxs-lookup"><span data-stu-id="1ec75-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="1ec75-155">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="1ec75-155">Click Delete.</span></span>

3. <span data-ttu-id="1ec75-156">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="1ec75-156">Click Yes.</span></span>

4. <span data-ttu-id="1ec75-157">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1ec75-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="1ec75-158">Kad visi respondenti ir aizpildījuši anketu, varat plānošanu beigt, un/vai visas atlikušās plānotās atbilžu sesijas ir dzēstas.</span><span class="sxs-lookup"><span data-stu-id="1ec75-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="1ec75-159">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="1ec75-159">Click Functions.</span></span>
2. <span data-ttu-id="1ec75-160">Noklikšķiniet uz Beigt.</span><span class="sxs-lookup"><span data-stu-id="1ec75-160">Click End.</span></span>
3. <span data-ttu-id="1ec75-161">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1ec75-161">Click OK.</span></span>
