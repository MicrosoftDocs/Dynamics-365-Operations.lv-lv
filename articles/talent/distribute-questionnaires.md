---
title: Anketu izplatīšana un plānošana
description: Šajā tēmā ir skaidrots, kā jūsu izveidotās anketas izplatīt tā, lai tās būtu pieejamas tai personai vai personu grupai, kas anketas aizpildīs.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc392c965a0d3bc308e0396263e84ecf1e713491
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898367"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="ba0ac-103">Anketu izplatīšana un plānošana</span><span class="sxs-lookup"><span data-stu-id="ba0ac-103">Distribute and schedule questionnaires</span></span>

<span data-ttu-id="ba0ac-104">Šajā tēmā ir skaidrots, kā jūsu izveidotās anketas izplatīt tā, lai tās būtu pieejamas tai personai vai personu grupai, kas anketas aizpildīs.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="ba0ac-105">Anketu var izplatīt vairākos veidos:</span><span class="sxs-lookup"><span data-stu-id="ba0ac-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="ba0ac-106">Atzīmējiet anketu kā aktīvu.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="ba0ac-107">Pēc tam anketa ir pieejama visiem darbiniekiem, ja vien nav iestatīta anketu grupa, kas tai ierobežotu piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="ba0ac-108">Piešķiriet tiesības anketu grupai.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="ba0ac-109">Pēc tam anketa ir pieejama visiem atlasītās grupas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="ba0ac-110">Izveidojiet plānotas atbilžu sesijas.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-110">Create planned answer sessions.</span></span> <span data-ttu-id="ba0ac-111">Pēc tam anketa ir pieejama tikai noteiktai personai.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="ba0ac-112">Izveidojiet grafiku.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-112">Create a schedule.</span></span> <span data-ttu-id="ba0ac-113">Pēc tam anketa var būt pieejama vairākām personām.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="ba0ac-114">Anketu kā aktīvas atzīmēšana</span><span class="sxs-lookup"><span data-stu-id="ba0ac-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="ba0ac-115">Lapā **Anketas** lauku **Aktīvs** iestatot uz **Jā**, šo anketu varat padarīt pieejamu aizpildīšanai visiem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="ba0ac-116">Respondenti anketu var aizpildīt vairākas reizes.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="ba0ac-117">Šī funkcionalitāte noder, ja vēlaties iegūt pastāvīgas atsauksmes visa gada laikā.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="ba0ac-118">Piemēram, varat izveidot anketu, ko darbinieki izmanto, lai sniegtu atsauksmes par pusdienu pakalpojumu kafejnīcā.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="ba0ac-119">Aptauju grupas</span><span class="sxs-lookup"><span data-stu-id="ba0ac-119">Questionnaire groups</span></span>
<span data-ttu-id="ba0ac-120">Varat iestatīt anketu grupas un pēc tam iekļaut respondentus, kuriem šī anketa ir jāizplata.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="ba0ac-121">Anketu grupas varat izveidot no šādām lapām:</span><span class="sxs-lookup"><span data-stu-id="ba0ac-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="ba0ac-122">**Anketu grupas** — atlasīto anketu var aizpildīt tikai anketu grupā iekļautās personas.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="ba0ac-123">Piemēram, jūsu mērķauditorija ir darbuzņēmēji, tāpēc jūs izveidojat anketu grupu, kas ir raksturīga šiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="ba0ac-124">**Aptauju grupu dalībnieki** — anketu grupām varat pievienot personas.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="ba0ac-125">Lai anketai piešķirtu anketu grupu, lapā **Anketas** noklikšķiniet uz **Lietotāja tiesības**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="ba0ac-126">Kad anketa ir saglabāta kā aktīva, anketu grupas dalībnieki var aizpildīt šo anketu.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="ba0ac-127">Šī funkcionalitāte noder, ja anketu vēlaties testēt ar atlasītu personu grupu, pirms to izplatāt lielākai grupai, vai ja anketu vēlaties izmantot ļoti specifiskai mērķauditorijai.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="ba0ac-128">Plānotās atbilžu sesijas anketā</span><span class="sxs-lookup"><span data-stu-id="ba0ac-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="ba0ac-129">Plānotās atbilžu sesijas ir anketas, ko esat izstrādājis un kam esat atlasījis respondentus.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> [!NOTE]
>   <span data-ttu-id="ba0ac-130">Pirms iestatāt plānotās atbilžu sesijas, ir jāizveido anketa.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-130">Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="ba0ac-131">Lapā **Plānotā atbilžu sesija** varat izveidot plānoto atbilžu sesiju atsevišķam darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="ba0ac-132">Lapas sarakstā tiek rādītas visas plānotās anketas.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="ba0ac-133">Plānotās atbilžu sesijas tiek lietotas arī lapā **Anketu grafiki**, kur varat plānot anketas vairākām personām:</span><span class="sxs-lookup"><span data-stu-id="ba0ac-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="ba0ac-134">Darbinieki</span><span class="sxs-lookup"><span data-stu-id="ba0ac-134">Employees</span></span>
-   <span data-ttu-id="ba0ac-135">Kursu dalībnieki</span><span class="sxs-lookup"><span data-stu-id="ba0ac-135">Course participants</span></span>
-   <span data-ttu-id="ba0ac-136">Organizācijas vienības</span><span class="sxs-lookup"><span data-stu-id="ba0ac-136">Organizational units</span></span>

<span data-ttu-id="ba0ac-137">Katra persona uz anketu var atbildēt tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="ba0ac-138">Anketas plānošana</span><span class="sxs-lookup"><span data-stu-id="ba0ac-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="ba0ac-139">Pēc izvēles anketu varat plānot vairākiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="ba0ac-140">Plānošanas tipi</span><span class="sxs-lookup"><span data-stu-id="ba0ac-140">Planning types</span></span>

<span data-ttu-id="ba0ac-141">Ja plānotās atbilžu sesijas vēlaties plānot vairākiem respondentiem, plānošanas tipi ir obligāti.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="ba0ac-142">Plānošanas tipi tiek izmantoti, lai klasificētu anketu grafikus.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="ba0ac-143">Piemēram, anketas varat plānot tālāk norādītajiem mērķiem.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="ba0ac-144">Novērtējums</span><span class="sxs-lookup"><span data-stu-id="ba0ac-144">Evaluation</span></span>
-   <span data-ttu-id="ba0ac-145">Aptauja</span><span class="sxs-lookup"><span data-stu-id="ba0ac-145">Survey</span></span>
-   <span data-ttu-id="ba0ac-146">Testēšana</span><span class="sxs-lookup"><span data-stu-id="ba0ac-146">Testing</span></span>

<span data-ttu-id="ba0ac-147">Anketas grafikam plānošanas tipu varat norādīt lapā **Anketu grafiki**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="ba0ac-148">Anketas atsauču tipi</span><span class="sxs-lookup"><span data-stu-id="ba0ac-148">Reference types for questionnaire</span></span>

<span data-ttu-id="ba0ac-149">Atsauču tipus var izmantot, lai ievadītu kritērijus respondentiem, kurus varat atlasīt, kad plānojat anketu.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="ba0ac-150">Izmantojiet lapu **Atsauču tipi**, lai anketai iestatītu atsauču tipus.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="ba0ac-151">Katrs atsauču tips atbilst tabulai programmā Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-151">Each reference type corresponds to a table in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="ba0ac-152">Kad veidojat anketu grafikus, tabulā varat norādīt atsevišķus ierakstus vai ierakstu diapazonu, ar kuriem anketa būs saistīta.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="ba0ac-153">Piemēram, ja atlasāt tabulu Kursi, varat izlemt, kuram konkrētajam kursam šī anketa būs paredzēta.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="ba0ac-154">Kad iestatāt atsauci tabulai Kursi, lapā **Kursi** kļūst pieejami daži lauki un pogas.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="ba0ac-155">Anketu grafiki</span><span class="sxs-lookup"><span data-stu-id="ba0ac-155">Questionnaire schedules</span></span>

<span data-ttu-id="ba0ac-156">Anketu grafikus varat izmantot, lai ģenerētu vairākas plānotās atbilžu sesijas lietotāju grupai, pamatojoties uz atsauču tipu.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="ba0ac-157">Izveidojiet grafiku lapā **Anketu grafiki**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="ba0ac-158">Atlasiet plānošanas tipu, lai kategorizētu šo grafiku, kā arī atlasiet atsauču tipu, kas ir jālieto, lai sistēmai veidotu vaicājumus par konkrētiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="ba0ac-159">Piemēram, ja atsauču tipu iestatāt uz tabulu Kursi, laukā **Atsauce** varat atlasīt konkrētu kursu.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="ba0ac-160">Noklikšķiniet uz **Detalizēta informācija par iestatījumu**, lai atlasītu anketu un citus kritērijus.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="ba0ac-161">Piemēram, ja anketa ir instruktora novērtējums, kā kritēriju norādiet instruktora vārdu.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="ba0ac-162">Kad esat beidzis ievadīt informāciju par iestatījumiem, sistēma ģenerē plānotās atbilžu sesijas vaicājumā iekļautajiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="ba0ac-163">Noklikšķiniet uz **Plānotās atbilžu sesijas**, lai skatītu atbilžu sesijas šim grafikam.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="ba0ac-164">Pēc tam varat manuāli izveidot papildu plānotās atbilžu sesijas vai dzēst plānotās atbilžu sesijas, kuras nav atbildētas.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="ba0ac-165">Lai anketu paradītu pieejamu lietotājiem saistītajās plānotajās atbilžu sesijās, noklikšķiniet uz **Funkcijas** &gt; **Sākums**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="ba0ac-166">Noklikšķiniet uz **Atbildes**, lai skatītu aizpildītās atbildes uz anketas jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="ba0ac-167">Anketas grafika iestatījumus, plānotās atbilžu sesijas un atbildes pēc izvēles varat kopēt uz jaunu anketas grafiku.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="ba0ac-168">Ziņošana respondentiem par viņiem pieejamām anketām</span><span class="sxs-lookup"><span data-stu-id="ba0ac-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="ba0ac-169">Kad izplatāt kādu anketu, jums ir jāpaziņo respondentiem, ka viņiem ir pieejamas anketas.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="ba0ac-170">Ziņošana respondentiem par plānoto atbilžu sesiju</span><span class="sxs-lookup"><span data-stu-id="ba0ac-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="ba0ac-171">Ja izmantojat plānoto atbilžu sesiju, jums persona ir jāinformē tieši, piemēram, pa tālruni vai e-pastu.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="ba0ac-172">Respondentu informēšana par plānošanu</span><span class="sxs-lookup"><span data-stu-id="ba0ac-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="ba0ac-173">Izmantojiet lapu **Anketu grafiki**, lai sagatavotu un nosūtītu e-pasta ziņojumus visiem anketai piešķirtajiem respondentiem.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="ba0ac-174">Ievadiet e-pasta ziņojuma tekstu cilnē **E-pasta ziņojums, ko sūtīt uz darbinieku pašapkalpošanos**. Kad grafiks ir sācies, noklikšķiniet uz **Funkcijas** &gt; **Nosūtīt e-pastu**, lai ģenerētu un respondentiem nosūtītu e-pasta ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="ba0ac-175">Pēc tam respondenti var pierakstīties vietnē un aizpildīt anketu.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> [!NOTE]
>   <span data-ttu-id="ba0ac-176">Lai varētu izmantot e-pasta funkcionalitāti, IT administratoram ir jāievada e-pasta iestatījumi lapā **E-pasta parametri**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-176">Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="ba0ac-177">Plānotas anketas beigšana</span><span class="sxs-lookup"><span data-stu-id="ba0ac-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="ba0ac-178">Ieplānoto anketu var pabeigt pēc tam, kad visi respondenti ir aizpildījuši piešķirtās atbilžu sesijas.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="ba0ac-179">Kad plānota anketa ir beigusies, tās iestatījumus vairs nevarat kopēt uz jaunu grafiku.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> [!NOTE]
>   <span data-ttu-id="ba0ac-180">Ja viens vai vairāki respondenti nav aizpildījuši anketu, bet jūs joprojām vēlaties beigt plānošanu, vispirms šie respondenti ir jāizdzēš no saraksta lapā **Plānotā atbilžu sesija**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-180">If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="ba0ac-181">Pēc tam grafiku varat beigt.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="ba0ac-182">Anketu aizpildīšana</span><span class="sxs-lookup"><span data-stu-id="ba0ac-182">Completing questionnaires</span></span>
<span data-ttu-id="ba0ac-183">Kad esat izstrādājis un izplatījis kādu anketu, šo anketu var aizpildīt atlasīti respondenti.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="ba0ac-184">Jūs varat aizpildīt jums pieejamās aptaujas anketas no divām vietām:</span><span class="sxs-lookup"><span data-stu-id="ba0ac-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="ba0ac-185">Navigācijas rūtī noklikšķiniet uz **Anketas** &gt; **Izplatīt** &gt; **Aizpildīt anketu**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="ba0ac-186">Darbinieku pašapkalpošanās lapā noklikšķiniet uz **Aizpildāmās anketas**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="ba0ac-187">Anketas var tikt padarītas pieejamas noteiktiem lietotājiem vai lietotāju grupām, vai visiem lietotājiem tīklā.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ba0ac-188">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ba0ac-188">Additional resources</span></span>
--------

[<span data-ttu-id="ba0ac-189">Anketu projektēšana</span><span class="sxs-lookup"><span data-stu-id="ba0ac-189">Design questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="ba0ac-190">Anketas</span><span class="sxs-lookup"><span data-stu-id="ba0ac-190">Questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="ba0ac-191">Anketu rezultātu skatīšana un novērtēšana</span><span class="sxs-lookup"><span data-stu-id="ba0ac-191">View and evaluate the results of questionnaires</span></span>](evaluate-questionnaire-results.md)


