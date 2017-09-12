---
title: "Aptaujas izplatīšana un aizpildīšana"
description: "Šajā tēmā ir skaidrots, kā jūsu izveidotās anketas izplatīt tā, lai tās būtu pieejamas tai personai vai personu grupai, kas anketas aizpildīs."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b2b1b99fd4c7c439ad89440827ad78173d371855
ms.openlocfilehash: c3afd12ed82935cd3d4b1c4ebeab62892cfe7178
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="84016-103">Aptaujas izplatīšana un aizpildīšana</span><span class="sxs-lookup"><span data-stu-id="84016-103">Distribute and complete a questionnaire</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="84016-104">Šajā tēmā ir skaidrots, kā jūsu izveidotās anketas izplatīt tā, lai tās būtu pieejamas tai personai vai personu grupai, kas anketas aizpildīs.</span><span class="sxs-lookup"><span data-stu-id="84016-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="84016-105">Anketu var izplatīt vairākos veidos:</span><span class="sxs-lookup"><span data-stu-id="84016-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="84016-106">Atzīmējiet anketu kā aktīvu.</span><span class="sxs-lookup"><span data-stu-id="84016-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="84016-107">Pēc tam anketa ir pieejama visiem darbiniekiem, ja vien nav iestatīta anketu grupa, kas tai ierobežotu piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="84016-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="84016-108">Piešķiriet tiesības anketu grupai.</span><span class="sxs-lookup"><span data-stu-id="84016-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="84016-109">Pēc tam anketa ir pieejama visiem atlasītās grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="84016-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="84016-110">Izveidojiet plānotas atbilžu sesijas.</span><span class="sxs-lookup"><span data-stu-id="84016-110">Create planned answer sessions.</span></span> <span data-ttu-id="84016-111">Pēc tam anketa ir pieejama tikai noteiktai personai.</span><span class="sxs-lookup"><span data-stu-id="84016-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="84016-112">Izveidojiet grafiku.</span><span class="sxs-lookup"><span data-stu-id="84016-112">Create a schedule.</span></span> <span data-ttu-id="84016-113">Pēc tam anketa var būt pieejama vairākām personām.</span><span class="sxs-lookup"><span data-stu-id="84016-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="84016-114">Anketu kā aktīvas atzīmēšana</span><span class="sxs-lookup"><span data-stu-id="84016-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="84016-115">Lapā **Anketas** lauku **Aktīvs** iestatot uz **Jā**, šo anketu varat padarīt pieejamu aizpildīšanai visiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="84016-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="84016-116">Respondenti anketu var aizpildīt vairākas reizes.</span><span class="sxs-lookup"><span data-stu-id="84016-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="84016-117">Šī funkcionalitāte noder, ja vēlaties iegūt pastāvīgas atsauksmes visa gada laikā.</span><span class="sxs-lookup"><span data-stu-id="84016-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="84016-118">Piemēram, varat izveidot anketu, ko darbinieki izmanto, lai sniegtu atsauksmes par pusdienu pakalpojumu kafejnīcā.</span><span class="sxs-lookup"><span data-stu-id="84016-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="84016-119">Aptauju grupas</span><span class="sxs-lookup"><span data-stu-id="84016-119">Questionnaire groups</span></span>
<span data-ttu-id="84016-120">Varat iestatīt anketu grupas un pēc tam iekļaut respondentus, kuriem šī anketa ir jāizplata.</span><span class="sxs-lookup"><span data-stu-id="84016-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="84016-121">Anketu grupas varat izveidot no šādām lapām:</span><span class="sxs-lookup"><span data-stu-id="84016-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="84016-122">**Anketu grupas** — atlasīto anketu var aizpildīt tikai anketu grupā iekļautās personas.</span><span class="sxs-lookup"><span data-stu-id="84016-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="84016-123">Piemēram, jūsu mērķauditorija ir darbuzņēmēji, tāpēc jūs izveidojat anketu grupu, kas ir raksturīga šiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="84016-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="84016-124">**Aptauju grupu dalībnieki** — anketu grupām varat pievienot personas.</span><span class="sxs-lookup"><span data-stu-id="84016-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="84016-125">Lai anketai piešķirtu anketu grupu, lapā **Anketas** noklikšķiniet uz **Lietotāja tiesības**.</span><span class="sxs-lookup"><span data-stu-id="84016-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="84016-126">Kad anketa ir saglabāta kā aktīva, anketu grupas dalībnieki var aizpildīt šo anketu.</span><span class="sxs-lookup"><span data-stu-id="84016-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="84016-127">Šī funkcionalitāte noder, ja anketu vēlaties testēt ar atlasītu personu grupu, pirms to izplatāt lielākai grupai, vai ja anketu vēlaties izmantot ļoti specifiskai mērķauditorijai.</span><span class="sxs-lookup"><span data-stu-id="84016-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="84016-128">Plānotās atbilžu sesijas anketā</span><span class="sxs-lookup"><span data-stu-id="84016-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="84016-129">Plānotās atbilžu sesijas ir anketas, ko esat izstrādājis un kam esat atlasījis respondentus.</span><span class="sxs-lookup"><span data-stu-id="84016-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="84016-130">**Piezīme.** Pirms iestatāt plānotās atbilžu sesijas, ir jāizveido anketa.</span><span class="sxs-lookup"><span data-stu-id="84016-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="84016-131">Lapā **Plānotā atbilžu sesija** varat izveidot plānoto atbilžu sesiju atsevišķam darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="84016-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="84016-132">Lapas sarakstā tiek rādītas visas plānotās anketas.</span><span class="sxs-lookup"><span data-stu-id="84016-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="84016-133">Plānotās atbilžu sesijas tiek lietotas arī lapā **Anketu grafiki**, kur varat plānot anketas vairākām personām:</span><span class="sxs-lookup"><span data-stu-id="84016-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="84016-134">Darbinieki</span><span class="sxs-lookup"><span data-stu-id="84016-134">Employees</span></span>
-   <span data-ttu-id="84016-135">Kursu dalībnieki</span><span class="sxs-lookup"><span data-stu-id="84016-135">Course participants</span></span>
-   <span data-ttu-id="84016-136">Organizācijas vienības</span><span class="sxs-lookup"><span data-stu-id="84016-136">Organizational units</span></span>

<span data-ttu-id="84016-137">Katra persona uz anketu var atbildēt tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="84016-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="84016-138">Anketas plānošana</span><span class="sxs-lookup"><span data-stu-id="84016-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="84016-139">Pēc izvēles anketu varat plānot vairākiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="84016-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="84016-140">Plānošanas tipi</span><span class="sxs-lookup"><span data-stu-id="84016-140">Planning types</span></span>

<span data-ttu-id="84016-141">Ja plānotās atbilžu sesijas vēlaties plānot vairākiem respondentiem, plānošanas tipi ir obligāti.</span><span class="sxs-lookup"><span data-stu-id="84016-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="84016-142">Plānošanas tipi tiek izmantoti, lai klasificētu anketu grafikus.</span><span class="sxs-lookup"><span data-stu-id="84016-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="84016-143">Piemēram, anketas varat plānot tālāk norādītajiem mērķiem.</span><span class="sxs-lookup"><span data-stu-id="84016-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="84016-144">Novērtējums</span><span class="sxs-lookup"><span data-stu-id="84016-144">Evaluation</span></span>
-   <span data-ttu-id="84016-145">Aptauja</span><span class="sxs-lookup"><span data-stu-id="84016-145">Survey</span></span>
-   <span data-ttu-id="84016-146">Testēšana</span><span class="sxs-lookup"><span data-stu-id="84016-146">Testing</span></span>

<span data-ttu-id="84016-147">Anketas grafikam plānošanas tipu varat norādīt lapā **Anketu grafiki**.</span><span class="sxs-lookup"><span data-stu-id="84016-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="84016-148">Anketas atsauču tipi</span><span class="sxs-lookup"><span data-stu-id="84016-148">Reference types for questionnaire</span></span>

<span data-ttu-id="84016-149">Atsauču tipus var izmantot, lai ievadītu kritērijus respondentiem, kurus varat atlasīt, kad plānojat anketu.</span><span class="sxs-lookup"><span data-stu-id="84016-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="84016-150">Izmantojiet lapu **Atsauču tipi**, lai anketai iestatītu atsauču tipus.</span><span class="sxs-lookup"><span data-stu-id="84016-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="84016-151">Katrs atsauču tips atbilst tabulai programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="84016-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="84016-152">Kad veidojat anketu grafikus, tabulā varat norādīt atsevišķus ierakstus vai ierakstu diapazonu, ar kuriem anketa būs saistīta.</span><span class="sxs-lookup"><span data-stu-id="84016-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="84016-153">Piemēram, ja atlasāt tabulu Kursi, varat izlemt, kuram konkrētajam kursam šī anketa būs paredzēta.</span><span class="sxs-lookup"><span data-stu-id="84016-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="84016-154">Kad iestatāt atsauci tabulai Kursi, lapā **Kursi** kļūst pieejami daži lauki un pogas.</span><span class="sxs-lookup"><span data-stu-id="84016-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="84016-155">Anketu grafiki</span><span class="sxs-lookup"><span data-stu-id="84016-155">Questionnaire schedules</span></span>

<span data-ttu-id="84016-156">Anketu grafikus varat izmantot, lai ģenerētu vairākas plānotās atbilžu sesijas lietotāju grupai, pamatojoties uz atsauču tipu.</span><span class="sxs-lookup"><span data-stu-id="84016-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="84016-157">Izveidojiet grafiku lapā **Anketu grafiki**.</span><span class="sxs-lookup"><span data-stu-id="84016-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="84016-158">Atlasiet plānošanas tipu, lai kategorizētu šo grafiku, kā arī atlasiet atsauču tipu, kas ir jālieto, lai sistēmai veidotu vaicājumus par konkrētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="84016-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="84016-159">Piemēram, ja atsauču tipu iestatāt uz tabulu Kursi, laukā **Atsauce** varat atlasīt konkrētu kursu.</span><span class="sxs-lookup"><span data-stu-id="84016-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="84016-160">Noklikšķiniet uz **Detalizēta informācija par iestatījumu**, lai atlasītu anketu un citus kritērijus.</span><span class="sxs-lookup"><span data-stu-id="84016-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="84016-161">Piemēram, ja anketa ir instruktora novērtējums, kā kritēriju norādiet instruktora vārdu.</span><span class="sxs-lookup"><span data-stu-id="84016-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="84016-162">Kad esat beidzis ievadīt informāciju par iestatījumiem, sistēma ģenerē plānotās atbilžu sesijas vaicājumā iekļautajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="84016-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="84016-163">Noklikšķiniet uz **Plānotās atbilžu sesijas**, lai skatītu atbilžu sesijas šim grafikam.</span><span class="sxs-lookup"><span data-stu-id="84016-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="84016-164">Pēc tam varat manuāli izveidot papildu plānotās atbilžu sesijas vai dzēst plānotās atbilžu sesijas, kuras nav atbildētas.</span><span class="sxs-lookup"><span data-stu-id="84016-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="84016-165">Lai anketu paradītu pieejamu lietotājiem saistītajās plānotajās atbilžu sesijās, noklikšķiniet uz **Funkcijas** &gt; **Sākums**.</span><span class="sxs-lookup"><span data-stu-id="84016-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="84016-166">Noklikšķiniet uz **Atbildes**, lai skatītu aizpildītās atbildes uz anketas jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="84016-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="84016-167">Anketas grafika iestatījumus, plānotās atbilžu sesijas un atbildes pēc izvēles varat kopēt uz jaunu anketas grafiku.</span><span class="sxs-lookup"><span data-stu-id="84016-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="84016-168">Ziņošana respondentiem par viņiem pieejamām anketām</span><span class="sxs-lookup"><span data-stu-id="84016-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="84016-169">Kad izplatāt kādu anketu, jums ir jāpaziņo respondentiem, ka viņiem ir pieejamas anketas.</span><span class="sxs-lookup"><span data-stu-id="84016-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="84016-170">Ziņošana respondentiem par plānoto atbilžu sesiju</span><span class="sxs-lookup"><span data-stu-id="84016-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="84016-171">Ja izmantojat plānoto atbilžu sesiju, jums persona ir jāinformē tieši, piemēram, pa tālruni vai e-pastu.</span><span class="sxs-lookup"><span data-stu-id="84016-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="84016-172">Respondentu informēšana par plānošanu</span><span class="sxs-lookup"><span data-stu-id="84016-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="84016-173">Izmantojiet lapu **Anketu grafiki**, lai sagatavotu un nosūtītu e-pasta ziņojumus visiem anketai piešķirtajiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="84016-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="84016-174">Ievadiet e-pasta ziņojuma tekstu cilnē **E-pasta ziņojums, ko sūtīt uz darbinieku pašapkalpošanos**.</span><span class="sxs-lookup"><span data-stu-id="84016-174">Enter the email text on the **E-mail for employee self service** tab.</span></span> <span data-ttu-id="84016-175">Kad grafiks ir sācies, noklikšķiniet uz **Funkcijas** &gt; **Nosūtīt e-pastu**, lai ģenerētu un respondentiem nosūtītu e-pasta ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="84016-175">After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="84016-176">Pēc tam respondenti var pierakstīties vietnē un aizpildīt anketu.</span><span class="sxs-lookup"><span data-stu-id="84016-176">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="84016-177">**Piezīme.** Lai varētu izmantot e-pasta funkcionalitāti, IT administratoram ir jāievada e-pasta iestatījumi lapā **E-pasta parametri**.</span><span class="sxs-lookup"><span data-stu-id="84016-177">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="84016-178">Plānotas anketas beigšana</span><span class="sxs-lookup"><span data-stu-id="84016-178">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="84016-179">Ieplānoto anketu var pabeigt pēc tam, kad visi respondenti ir aizpildījuši piešķirtās atbilžu sesijas.</span><span class="sxs-lookup"><span data-stu-id="84016-179">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="84016-180">Kad plānota anketa ir beigusies, tās iestatījumus vairs nevarat kopēt uz jaunu grafiku.</span><span class="sxs-lookup"><span data-stu-id="84016-180">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="84016-181">**Piezīme.** Ja viens vai vairāki respondenti nav aizpildījuši anketu, bet jūs joprojām vēlaties beigt plānošanu, vispirms šie respondenti ir jāizdzēš no saraksta lapā **Plānotā atbilžu sesija**.</span><span class="sxs-lookup"><span data-stu-id="84016-181">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="84016-182">Pēc tam grafiku varat beigt.</span><span class="sxs-lookup"><span data-stu-id="84016-182">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="84016-183">Anketu aizpildīšana</span><span class="sxs-lookup"><span data-stu-id="84016-183">Completing questionnaires</span></span>
<span data-ttu-id="84016-184">Kad esat izstrādājis un izplatījis kādu anketu, šo anketu var aizpildīt atlasīti respondenti.</span><span class="sxs-lookup"><span data-stu-id="84016-184">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="84016-185">Jūs varat aizpildīt jums pieejamās aptaujas anketas no divām vietām:</span><span class="sxs-lookup"><span data-stu-id="84016-185">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="84016-186">Navigācijas rūtī noklikšķiniet uz **Anketas** &gt; **Izplatīt** &gt; **Aizpildīt anketu**.</span><span class="sxs-lookup"><span data-stu-id="84016-186">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="84016-187">Darbinieku pašapkalpošanās lapā noklikšķiniet uz **Aizpildāmās anketas**.</span><span class="sxs-lookup"><span data-stu-id="84016-187">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="84016-188">Anketas var tikt padarītas pieejamas noteiktiem lietotājiem vai lietotāju grupām, vai visiem lietotājiem tīklā.</span><span class="sxs-lookup"><span data-stu-id="84016-188">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="84016-189">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="84016-189">See also</span></span>
--------

[<span data-ttu-id="84016-190">Anketu veidošana</span><span class="sxs-lookup"><span data-stu-id="84016-190">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="84016-191">Anketu lietošana</span><span class="sxs-lookup"><span data-stu-id="84016-191">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="84016-192">Anketu rezultātu skatīšana un novērtēšana</span><span class="sxs-lookup"><span data-stu-id="84016-192">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)



<a name=""></a>=======
---
# <a name="required-metadata"></a><span data-ttu-id="84016-193">Nepieciešamie metadati</span><span class="sxs-lookup"><span data-stu-id="84016-193">required metadata</span></span>

<span data-ttu-id="84016-194">Virsraksts: Anketas izplatīšanas un aizpildīšanas apraksts: Šajā tēmā ir paskaidrots, kā jūsu izveidotās anketas izplatīt tā, lai tās būtu pieejamas tai personai vai personu grupai, kas anketas aizpildīs.</span><span class="sxs-lookup"><span data-stu-id="84016-194">title: Distribute and complete a questionnaire description: This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> <span data-ttu-id="84016-195">Autors: twheeloc vadītājs: AnnBe ms.date: 06/20/2017 ms.topic: article ms.prod: ms.service: Dynamics365Operations ms.technology:</span><span class="sxs-lookup"><span data-stu-id="84016-195">author: twheeloc manager: AnnBe ms.date: 06/20/2017 ms.topic: article ms.prod: ms.service: Dynamics365Operations ms.technology:</span></span> 

# <a name="optional-metadata"></a><span data-ttu-id="84016-196">Papildu metadati</span><span class="sxs-lookup"><span data-stu-id="84016-196">optional metadata</span></span>

<span data-ttu-id="84016-197">ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters</span><span class="sxs-lookup"><span data-stu-id="84016-197">ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters</span></span>
# <a name="robots"></a><span data-ttu-id="84016-198">ROBOTS:</span><span class="sxs-lookup"><span data-stu-id="84016-198">ROBOTS:</span></span> 
<span data-ttu-id="84016-199">Auditorija: programmas lietotājs</span><span class="sxs-lookup"><span data-stu-id="84016-199">audience: Application User</span></span>
# <a name="msdevlang"></a><span data-ttu-id="84016-200">ms.devlang:</span><span class="sxs-lookup"><span data-stu-id="84016-200">ms.devlang:</span></span> 
<span data-ttu-id="84016-201">ms.reviewer: twheeloc ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations</span><span class="sxs-lookup"><span data-stu-id="84016-201">ms.reviewer: twheeloc ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations</span></span>
# <a name="mstgtpltfrm"></a><span data-ttu-id="84016-202">ms.tgt_pltfrm:</span><span class="sxs-lookup"><span data-stu-id="84016-202">ms.tgt_pltfrm:</span></span> 
<span data-ttu-id="84016-203">ms.custom: 17424 ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470 ms.search.region: globāls</span><span class="sxs-lookup"><span data-stu-id="84016-203">ms.custom: 17424 ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470 ms.search.region: Global</span></span>
# <a name="mssearchindustry"></a><span data-ttu-id="84016-204">ms.search.industry:</span><span class="sxs-lookup"><span data-stu-id="84016-204">ms.search.industry:</span></span> 
<span data-ttu-id="84016-205">ms.author: twheeloc ms.search.validFrom: 2016-02-28 ms.dyn365.ops.version: AX 7.0.0, Talent 2017. gada jūlija atjauninājums</span><span class="sxs-lookup"><span data-stu-id="84016-205">ms.author: twheeloc ms.search.validFrom: 2016-02-28 ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update</span></span>

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="84016-206">Izplatīt un aizpildīt anketu</span><span class="sxs-lookup"><span data-stu-id="84016-206">Distribute and complete a questionnaire</span></span>

<span data-ttu-id="84016-207">Šajā tēmā ir skaidrots, kā jūsu izveidotās anketas izplatīt tā, lai tās būtu pieejamas tai personai vai personu grupai, kas anketas aizpildīs.</span><span class="sxs-lookup"><span data-stu-id="84016-207">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="84016-208">Anketu var izplatīt vairākos veidos:</span><span class="sxs-lookup"><span data-stu-id="84016-208">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="84016-209">Atzīmējiet anketu kā aktīvu.</span><span class="sxs-lookup"><span data-stu-id="84016-209">Mark the questionnaire as active.</span></span> <span data-ttu-id="84016-210">Pēc tam anketa ir pieejama visiem darbiniekiem, ja vien nav iestatīta anketu grupa, kas tai ierobežotu piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="84016-210">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="84016-211">Piešķiriet tiesības anketu grupai.</span><span class="sxs-lookup"><span data-stu-id="84016-211">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="84016-212">Pēc tam anketa ir pieejama visiem atlasītās grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="84016-212">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="84016-213">Izveidojiet plānotas atbilžu sesijas.</span><span class="sxs-lookup"><span data-stu-id="84016-213">Create planned answer sessions.</span></span> <span data-ttu-id="84016-214">Pēc tam anketa ir pieejama tikai noteiktai personai.</span><span class="sxs-lookup"><span data-stu-id="84016-214">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="84016-215">Izveidojiet grafiku.</span><span class="sxs-lookup"><span data-stu-id="84016-215">Create a schedule.</span></span> <span data-ttu-id="84016-216">Pēc tam anketa var būt pieejama vairākām personām.</span><span class="sxs-lookup"><span data-stu-id="84016-216">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="84016-217">Anketu kā aktīvas atzīmēšana</span><span class="sxs-lookup"><span data-stu-id="84016-217">Marking a questionnaire as active</span></span>
<span data-ttu-id="84016-218">Lapā **Anketas** lauku **Aktīvs** iestatot uz **Jā**, šo anketu varat padarīt pieejamu aizpildīšanai visiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="84016-218">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="84016-219">Respondenti anketu var aizpildīt vairākas reizes.</span><span class="sxs-lookup"><span data-stu-id="84016-219">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="84016-220">Šī funkcionalitāte noder, ja vēlaties iegūt pastāvīgas atsauksmes visa gada laikā.</span><span class="sxs-lookup"><span data-stu-id="84016-220">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="84016-221">Piemēram, varat izveidot anketu, ko darbinieki izmanto, lai sniegtu atsauksmes par pusdienu pakalpojumu kafejnīcā.</span><span class="sxs-lookup"><span data-stu-id="84016-221">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="84016-222">Aptauju grupas</span><span class="sxs-lookup"><span data-stu-id="84016-222">Questionnaire groups</span></span>
<span data-ttu-id="84016-223">Varat iestatīt anketu grupas un pēc tam iekļaut respondentus, kuriem šī anketa ir jāizplata.</span><span class="sxs-lookup"><span data-stu-id="84016-223">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="84016-224">Anketu grupas varat izveidot no šādām lapām:</span><span class="sxs-lookup"><span data-stu-id="84016-224">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="84016-225">**Anketu grupas** — atlasīto anketu var aizpildīt tikai anketu grupā iekļautās personas.</span><span class="sxs-lookup"><span data-stu-id="84016-225">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="84016-226">Piemēram, jūsu mērķauditorija ir darbuzņēmēji, tāpēc jūs izveidojat anketu grupu, kas ir raksturīga šiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="84016-226">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="84016-227">**Aptauju grupu dalībnieki** — anketu grupām varat pievienot personas.</span><span class="sxs-lookup"><span data-stu-id="84016-227">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="84016-228">Lai anketai piešķirtu anketu grupu, lapā **Anketas** noklikšķiniet uz **Lietotāja tiesības**.</span><span class="sxs-lookup"><span data-stu-id="84016-228">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="84016-229">Kad anketa ir saglabāta kā aktīva, anketu grupas dalībnieki var aizpildīt šo anketu.</span><span class="sxs-lookup"><span data-stu-id="84016-229">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="84016-230">Šī funkcionalitāte noder, ja anketu vēlaties testēt ar atlasītu personu grupu, pirms to izplatāt lielākai grupai, vai ja anketu vēlaties izmantot ļoti specifiskai mērķauditorijai.</span><span class="sxs-lookup"><span data-stu-id="84016-230">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="84016-231">Plānotās atbilžu sesijas anketā</span><span class="sxs-lookup"><span data-stu-id="84016-231">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="84016-232">Plānotās atbilžu sesijas ir anketas, ko esat izstrādājis un kam esat atlasījis respondentus.</span><span class="sxs-lookup"><span data-stu-id="84016-232">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

<span data-ttu-id="84016-233">**Piezīme.** Pirms iestatāt plānotās atbilžu sesijas, ir nepieciešams izveidot anketu.</span><span class="sxs-lookup"><span data-stu-id="84016-233">**Note:** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="84016-234">Lapā **Plānotā atbilžu sesija** varat izveidot plānoto atbilžu sesiju atsevišķam darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="84016-234">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="84016-235">Lapas sarakstā tiek rādītas visas plānotās anketas.</span><span class="sxs-lookup"><span data-stu-id="84016-235">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="84016-236">Plānotās atbilžu sesijas tiek lietotas arī lapā **Anketu grafiki**, kur varat plānot anketas vairākām personām:</span><span class="sxs-lookup"><span data-stu-id="84016-236">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="84016-237">Darbinieki</span><span class="sxs-lookup"><span data-stu-id="84016-237">Employees</span></span>
-   <span data-ttu-id="84016-238">Kursu dalībnieki</span><span class="sxs-lookup"><span data-stu-id="84016-238">Course participants</span></span>
-   <span data-ttu-id="84016-239">Organizācijas vienības</span><span class="sxs-lookup"><span data-stu-id="84016-239">Organizational units</span></span>

<span data-ttu-id="84016-240">Katra persona uz anketu var atbildēt tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="84016-240">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="84016-241">Anketas plānošana</span><span class="sxs-lookup"><span data-stu-id="84016-241">Scheduling a questionnaire</span></span>
<span data-ttu-id="84016-242">Pēc izvēles anketu varat plānot vairākiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="84016-242">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="84016-243">Plānošanas tipi</span><span class="sxs-lookup"><span data-stu-id="84016-243">Planning types</span></span>

<span data-ttu-id="84016-244">Ja plānotās atbilžu sesijas vēlaties plānot vairākiem respondentiem, plānošanas tipi ir obligāti.</span><span class="sxs-lookup"><span data-stu-id="84016-244">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="84016-245">Plānošanas tipi tiek izmantoti, lai klasificētu anketu grafikus.</span><span class="sxs-lookup"><span data-stu-id="84016-245">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="84016-246">Piemēram, anketas varat plānot tālāk norādītajiem mērķiem.</span><span class="sxs-lookup"><span data-stu-id="84016-246">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="84016-247">Novērtējums</span><span class="sxs-lookup"><span data-stu-id="84016-247">Evaluation</span></span>
-   <span data-ttu-id="84016-248">Aptauja</span><span class="sxs-lookup"><span data-stu-id="84016-248">Survey</span></span>
-   <span data-ttu-id="84016-249">Testēšana</span><span class="sxs-lookup"><span data-stu-id="84016-249">Testing</span></span>

<span data-ttu-id="84016-250">Anketas grafikam plānošanas tipu varat norādīt lapā **Anketu grafiki**.</span><span class="sxs-lookup"><span data-stu-id="84016-250">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="84016-251">Anketas atsauču tipi</span><span class="sxs-lookup"><span data-stu-id="84016-251">Reference types for questionnaire</span></span>

<span data-ttu-id="84016-252">Atsauču tipus var izmantot, lai ievadītu kritērijus respondentiem, kurus varat atlasīt, kad plānojat anketu.</span><span class="sxs-lookup"><span data-stu-id="84016-252">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="84016-253">Izmantojiet lapu **Atsauču tipi**, lai anketai iestatītu atsauču tipus.</span><span class="sxs-lookup"><span data-stu-id="84016-253">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="84016-254">Katrs atsauču tips atbilst tabulai programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise.</span><span class="sxs-lookup"><span data-stu-id="84016-254">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span></span> <span data-ttu-id="84016-255">Kad veidojat anketu grafikus, tabulā varat norādīt atsevišķus ierakstus vai ierakstu diapazonu, ar kuriem anketa būs saistīta.</span><span class="sxs-lookup"><span data-stu-id="84016-255">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="84016-256">Piemēram, ja atlasāt tabulu Kursi, varat izlemt, kuram konkrētajam kursam šī anketa būs paredzēta.</span><span class="sxs-lookup"><span data-stu-id="84016-256">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="84016-257">Kad iestatāt atsauci tabulai Kursi, lapā **Kursi** kļūst pieejami daži lauki un pogas.</span><span class="sxs-lookup"><span data-stu-id="84016-257">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="84016-258">Anketu grafiki</span><span class="sxs-lookup"><span data-stu-id="84016-258">Questionnaire schedules</span></span>

<span data-ttu-id="84016-259">Anketu grafikus varat izmantot, lai ģenerētu vairākas plānotās atbilžu sesijas lietotāju grupai, pamatojoties uz atsauču tipu.</span><span class="sxs-lookup"><span data-stu-id="84016-259">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="84016-260">Izveidojiet grafiku lapā **Anketu grafiki**.</span><span class="sxs-lookup"><span data-stu-id="84016-260">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="84016-261">Atlasiet plānošanas tipu, lai kategorizētu šo grafiku, kā arī atlasiet atsauču tipu, kas ir jālieto, lai sistēmai veidotu vaicājumus par konkrētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="84016-261">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="84016-262">Piemēram, ja atsauču tipu iestatāt uz tabulu Kursi, laukā **Atsauce** varat atlasīt konkrētu kursu.</span><span class="sxs-lookup"><span data-stu-id="84016-262">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="84016-263">Noklikšķiniet uz **Detalizēta informācija par iestatījumu**, lai atlasītu anketu un citus kritērijus.</span><span class="sxs-lookup"><span data-stu-id="84016-263">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="84016-264">Piemēram, ja anketa ir instruktora novērtējums, kā kritēriju norādiet instruktora vārdu.</span><span class="sxs-lookup"><span data-stu-id="84016-264">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="84016-265">Kad esat beidzis ievadīt informāciju par iestatījumiem, sistēma ģenerē plānotās atbilžu sesijas vaicājumā iekļautajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="84016-265">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="84016-266">Noklikšķiniet uz **Plānotās atbilžu sesijas**, lai skatītu atbilžu sesijas šim grafikam.</span><span class="sxs-lookup"><span data-stu-id="84016-266">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="84016-267">Pēc tam varat manuāli izveidot papildu plānotās atbilžu sesijas vai dzēst plānotās atbilžu sesijas, kuras nav atbildētas.</span><span class="sxs-lookup"><span data-stu-id="84016-267">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="84016-268">Lai anketu paradītu pieejamu lietotājiem saistītajās plānotajās atbilžu sesijās, noklikšķiniet uz **Funkcijas** &gt; **Sākums**.</span><span class="sxs-lookup"><span data-stu-id="84016-268">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="84016-269">Noklikšķiniet uz **Atbildes**, lai skatītu aizpildītās atbildes uz anketas jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="84016-269">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="84016-270">Anketas grafika iestatījumus, plānotās atbilžu sesijas un atbildes pēc izvēles varat kopēt uz jaunu anketas grafiku.</span><span class="sxs-lookup"><span data-stu-id="84016-270">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="84016-271">Ziņošana respondentiem par viņiem pieejamām anketām</span><span class="sxs-lookup"><span data-stu-id="84016-271">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="84016-272">Kad izplatāt kādu anketu, jums ir jāpaziņo respondentiem, ka viņiem ir pieejamas anketas.</span><span class="sxs-lookup"><span data-stu-id="84016-272">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

<span data-ttu-id="84016-273">**Piezīme.** Lai aizpildītu anketu, respondentiem ir jābūt programmatūras Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="84016-273">**Note:** Respondents must be users in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition to complete a questionnaire.</span></span>

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="84016-274">Ziņošana respondentiem par plānoto atbilžu sesiju</span><span class="sxs-lookup"><span data-stu-id="84016-274">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="84016-275">Ja izmantojat plānoto atbilžu sesiju, jums persona ir jāinformē tieši, piemēram, pa tālruni vai e-pastu.</span><span class="sxs-lookup"><span data-stu-id="84016-275">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="84016-276">Respondentu informēšana par plānošanu</span><span class="sxs-lookup"><span data-stu-id="84016-276">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="84016-277">Izmantojiet lapu **Anketu grafiki**, lai sagatavotu un nosūtītu e-pasta ziņojumus visiem anketai piešķirtajiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="84016-277">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="84016-278">Ievadiet e-pasta ziņojuma tekstu cilnē **E-pasta ziņojums, ko sūtīt uz darbinieku pašapkalpošanos**.</span><span class="sxs-lookup"><span data-stu-id="84016-278">Enter the email text on the **E-mail for employee self service** tab.</span></span> <span data-ttu-id="84016-279">Kad grafiks ir sācies, noklikšķiniet uz **Funkcijas** &gt; **Nosūtīt e-pastu**, lai ģenerētu un respondentiem nosūtītu e-pasta ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="84016-279">After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="84016-280">Pēc tam respondenti var pierakstīties vietnē un aizpildīt anketu.</span><span class="sxs-lookup"><span data-stu-id="84016-280">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

<span data-ttu-id="84016-281">**Piezīme.** Lai varētu izmantot e-pasta funkcionalitāti, IT administratoram ir jāievada e-pasta iestatījumi lapā **E-pasta parametri**.</span><span class="sxs-lookup"><span data-stu-id="84016-281">**Note:** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="84016-282">Plānotas anketas beigšana</span><span class="sxs-lookup"><span data-stu-id="84016-282">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="84016-283">Ieplānoto anketu var pabeigt pēc tam, kad visi respondenti ir aizpildījuši piešķirtās atbilžu sesijas.</span><span class="sxs-lookup"><span data-stu-id="84016-283">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="84016-284">Kad plānota anketa ir beigusies, tās iestatījumus vairs nevarat kopēt uz jaunu grafiku.</span><span class="sxs-lookup"><span data-stu-id="84016-284">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

<span data-ttu-id="84016-285">**Piezīme.** Ja viens vai vairāki respondenti nav aizpildījusi anketu, bet jūs joprojām vēlaties beigt plānošanu, jums vispirms šie respondenti ir jāizdzēš no saraksta lapā **Plānotā atbilžu sesija**.</span><span class="sxs-lookup"><span data-stu-id="84016-285">**Note:** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="84016-286">Pēc tam grafiku varat beigt.</span><span class="sxs-lookup"><span data-stu-id="84016-286">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="84016-287">Anketu aizpildīšana</span><span class="sxs-lookup"><span data-stu-id="84016-287">Completing questionnaires</span></span>
<span data-ttu-id="84016-288">Kad esat izstrādājis un izplatījis kādu anketu, šo anketu var aizpildīt atlasīti respondenti.</span><span class="sxs-lookup"><span data-stu-id="84016-288">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="84016-289">Jūs varat aizpildīt jums pieejamās aptaujas anketas no divām vietām:</span><span class="sxs-lookup"><span data-stu-id="84016-289">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="84016-290">Navigācijas rūtī noklikšķiniet uz **Anketas** &gt; **Izplatīt** &gt; **Aizpildīt anketu**.</span><span class="sxs-lookup"><span data-stu-id="84016-290">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="84016-291">Darbinieku pašapkalpošanās lapā noklikšķiniet uz **Aizpildāmās anketas**.</span><span class="sxs-lookup"><span data-stu-id="84016-291">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="84016-292">Anketas var tikt padarītas pieejamas noteiktiem lietotājiem vai lietotāju grupām, vai visiem lietotājiem tīklā.</span><span class="sxs-lookup"><span data-stu-id="84016-292">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="84016-293">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="84016-293">See also</span></span>
--------

[<span data-ttu-id="84016-294">Anketu veidošana</span><span class="sxs-lookup"><span data-stu-id="84016-294">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="84016-295">Anketu lietošana</span><span class="sxs-lookup"><span data-stu-id="84016-295">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="84016-296">Anketu rezultātu skatīšana un novērtēšana</span><span class="sxs-lookup"><span data-stu-id="84016-296">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)

<span data-ttu-id="84016-297">Šablons</span><span class="sxs-lookup"><span data-stu-id="84016-297">master</span></span>

