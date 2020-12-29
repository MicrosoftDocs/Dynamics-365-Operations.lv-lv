---
title: Kandidātu piesaistīšana ar LinkedIn Recruiter sistēmā Attract
description: Izmantojiet programmas Microsoft Dynamics 365 Talent - Attract nodrošināto LinkedIn integrāciju, lai piesaistītu darba kandidātus ar LinkedIn Recruiter.
author: andreabichsel
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 96e4660c4958bf5f2a0910bfad770e1e713f800f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528273"
---
# <a name="source-candidates-with-linkedin-recruiter-in-attract"></a><span data-ttu-id="ed1df-103">Kandidātu piesaistīšana ar LinkedIn Recruiter sistēmā Attract</span><span class="sxs-lookup"><span data-stu-id="ed1df-103">Source candidates with LinkedIn Recruiter in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed1df-104">LinkedIn ir pasaulē lielākais tiešsaistes profesionāļu tīkls, kas sniedz jums pieeju pasaules augstākā līmeņa talantiem.</span><span class="sxs-lookup"><span data-stu-id="ed1df-104">LinkedIn is the world's largest online professional network, giving you access to the world's top talent.</span></span> <span data-ttu-id="ed1df-105">Microsoft Dynamics 365 Talent: Attract ļauj piesaistīt kandidātus tieši no LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="ed1df-105">Microsoft Dynamics 365 Talent: Attract lets you source candidates directly from LinkedIn.</span></span> <span data-ttu-id="ed1df-106">Tāpēc ir vieglāk nekā jebkad atrast talantu, kas nepieciešams, lai aizpildītu vakances.</span><span class="sxs-lookup"><span data-stu-id="ed1df-106">Therefore, it's easier than ever to find the talent that you need to fill your open positions.</span></span> <span data-ttu-id="ed1df-107">Kad esat iestatījis savienojumu ar LinkedIn, izmantojot Attract, varat skatīt potenciālos LinkedIn kandidātus savām vakancēm un eksportēt tos sistēmā Attract ar tikai vienu klikšķi.</span><span class="sxs-lookup"><span data-stu-id="ed1df-107">After you set up your connection with LinkedIn through Attract, you can view potential LinkedIn candidates for your positions and export them into Attract with just one click.</span></span>

<span data-ttu-id="ed1df-108">Ja šķiet, ka jums nav šīs iespējas, sazinieties ar savu administratoru. Lai varētu izmantot LinkedIn Recruiter priekšrocības no sistēmas Attract, administratoram ir [jāiestata integrācija ar LinkedIn](./attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="ed1df-108">If you don't seem to have this capability, contact your admin. Before you can take advantage of LinkedIn Recruiter from Attract, your admin must [set up integration with LinkedIn](./attract-admin-linkedin.md).</span></span> <span data-ttu-id="ed1df-109">Pēc tam varat iestatīt savienojumu ar LinkedIn Recruiter un sākt meklēt kandidātus.</span><span class="sxs-lookup"><span data-stu-id="ed1df-109">You can then set up your connection with LinkedIn Recruiter and start finding candidates.</span></span>

>[!IMPORTANT]
><span data-ttu-id="ed1df-110">No 2020. gada 1. jūlija LinkedIn vairs neatbalsta Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="ed1df-110">As of July 1, 2020, LinkedIn no longer supports Internet Explorer 11.</span></span> <span data-ttu-id="ed1df-111">Lietotāji joprojām var piekļūt LinkedIn ar Internet Explorer 11, bet tiem tiks piedāvāts jaunināt vai izmantot citu pārlūkprogrammu.</span><span class="sxs-lookup"><span data-stu-id="ed1df-111">Users can still access LinkedIn with Internet Explorer 11, but will be prompted to upgrade or use a different browser.</span></span> <span data-ttu-id="ed1df-112">Plašāku informāciju skatiet [Atbalstītie Interneta pārlūki pakalpojumam LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).</span><span class="sxs-lookup"><span data-stu-id="ed1df-112">For more information, see [Supported Internet Browsers for LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).</span></span>

## <a name="set-up-your-connection-with-linkedin-recruiter"></a><span data-ttu-id="ed1df-113">Savienojuma ar LinkedIn Recruiter iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ed1df-113">Set up your connection with LinkedIn Recruiter</span></span>

<span data-ttu-id="ed1df-114">Lai varētu sākt darbu ar LinkedIn Recruiter, izmantojot sistēmu Attract, ir jāiestata savienojums ar LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="ed1df-114">Before you can start working with LinkedIn Recruiter through Attract, you must set up your connection with LinkedIn Recruiter.</span></span> <span data-ttu-id="ed1df-115">Šai darbībai ir nepieciešami jūsu LinkedIn Recruiter akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="ed1df-115">For this step, you need your LinkedIn Recruiter credentials.</span></span>

1. <span data-ttu-id="ed1df-116">Lapas augšējā labajā stūrī atlasiet pogu **Iestatījumi** (zobrata ikona).</span><span class="sxs-lookup"><span data-stu-id="ed1df-116">Select the **Settings** button (gear icon) in the upper-right corner of the page.</span></span>
2. <span data-ttu-id="ed1df-117">Atlasiet **Lietotāja iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="ed1df-117">Select **User settings**.</span></span>
3. <span data-ttu-id="ed1df-118">Cilnē **Savienojumi** atlasiet **Izveidot savienojumu** blakus **LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="ed1df-118">On the **Connections** tab, select **Connect** next to **LinkedIn**.</span></span> <span data-ttu-id="ed1df-119">Izpildiet LinkedIn sniegtos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="ed1df-119">Follow the instructions that are provided by LinkedIn.</span></span>

    ![[<span data-ttu-id="ed1df-120">Iestatīt savienojumu ar LinkedIn Recruiter no Attract</span><span class="sxs-lookup"><span data-stu-id="ed1df-120">Set up connection to LinkedIn Recruiter from Attract</span></span>](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a><span data-ttu-id="ed1df-121">LinkedIn kandidātu skatīšana sistēmā Attract</span><span class="sxs-lookup"><span data-stu-id="ed1df-121">View LinkedIn candidates in Attract</span></span>

<span data-ttu-id="ed1df-122">Kad esat izveidojis savienojumu ar LinkedIn Recruiter, varat skatīt kandidātu LinkedIn profilus sistēmā Attract.</span><span class="sxs-lookup"><span data-stu-id="ed1df-122">After you're connected to LinkedIn Recruiter, you can view candidates' LinkedIn profiles in Attract.</span></span>

>[!NOTE]
><span data-ttu-id="ed1df-123">Ja jums ir piešķirta Personāla atlases speciālista licence, varat apskatīt visu kandidātu informāciju.</span><span class="sxs-lookup"><span data-stu-id="ed1df-123">If you have a Recruiter seat assigned to you, you can see the candidates' full information.</span></span><br><br>
><span data-ttu-id="ed1df-124">Ja jums ir Nolīgšanas pārvaldnieka licence vai nav piešķirta licence, noteikti izrakstieties no LinkedIn vai LinkedIn Recruiter pirms naviģēšanas uz cilni LinkedIn kandidātam programmā Attrakt.</span><span class="sxs-lookup"><span data-stu-id="ed1df-124">If you have a Hiring Manager seat or no seat assigned to you, be sure to sign out of LinkedIn or LinkedIn Recruiter before navigating to the LinkedIn tab for a candidate in Attract.</span></span> <span data-ttu-id="ed1df-125">Jūs varēsiet redzēt kandidāta publiskā profila pamatdatus, piemēram, vārdu un uzvārdu.</span><span class="sxs-lookup"><span data-stu-id="ed1df-125">You'll be able to see the candidate's basic public profile data, such as their first and last name.</span></span>

1. <span data-ttu-id="ed1df-126">Sistēmā Attract kreisajā pusē atlasiet vienumu **Darbi** vai **Talantu kopas** un pēc tam atlasiet kandidātu.</span><span class="sxs-lookup"><span data-stu-id="ed1df-126">In Attract, select **Jobs** or **Talent pools** on the left, and then select an applicant.</span></span>

    ![[<span data-ttu-id="ed1df-127">LinkedIn kandidātu skatīšana sistēmā Attract</span><span class="sxs-lookup"><span data-stu-id="ed1df-127">View LinkedIn candidates in Attract</span></span>](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. <span data-ttu-id="ed1df-128">Kandidāta profilā atlasiet cilni **LinkedIn** Varat skatīt kandidāta profilu un InMail vēsturi.</span><span class="sxs-lookup"><span data-stu-id="ed1df-128">In the candidate's profile, select the **LinkedIn** tab. You can view the candidate's profile and InMail history.</span></span>

   ![Skatīt kandidāta LinkedIn informāciju](./media/attract-candidate-linkedin-tab.png)

<span data-ttu-id="ed1df-130">Šeit varat veikt tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ed1df-130">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="ed1df-131">Atlasiet cilni **Personāla atlases aktivitātes**, lai apskatītu:</span><span class="sxs-lookup"><span data-stu-id="ed1df-131">Select the **Recruiting activities** tab to view:</span></span>
   
   - <span data-ttu-id="ed1df-132">Personāla atlases speciālista piezīmes (gan publiskas, gan privātas).</span><span class="sxs-lookup"><span data-stu-id="ed1df-132">Recruiter notes (both public and private).</span></span> <span data-ttu-id="ed1df-133">Pēc noklusējuma piezīmes ir privātas un redzamas tikai piezīmju īpašniekam.</span><span class="sxs-lookup"><span data-stu-id="ed1df-133">By default, notes are private and only visible to the owner of the notes.</span></span>
   - <span data-ttu-id="ed1df-134">InMail aktivitāte (bet ne InMail saturs).</span><span class="sxs-lookup"><span data-stu-id="ed1df-134">InMail activity (but not the InMail content).</span></span> <span data-ttu-id="ed1df-135">Ritiniet līdz lapas apakšai, lai apskatītu InMail apmaiņu ar savu potenciālo klientu un skatītu citus lietotājus jūsu organizācijā, kuri mijiedarbojas ar jūsu potenciālo klientu.</span><span class="sxs-lookup"><span data-stu-id="ed1df-135">Scroll to the bottom of the page to view the InMail exchange with your prospect and view other users in your organization who are interacting with your prospect.</span></span>
   - <span data-ttu-id="ed1df-136">Kandidātu noraidīšanas aktivitāte</span><span class="sxs-lookup"><span data-stu-id="ed1df-136">Candidate rejection activity</span></span>

- <span data-ttu-id="ed1df-137">Atlasiet **Sūtīt InMail**, lai nosūtītu InMail, bez nepieciešamības atstāt Attract.</span><span class="sxs-lookup"><span data-stu-id="ed1df-137">Select **Send InMail** to send InMail without having to leave Attract.</span></span>

- <span data-ttu-id="ed1df-138">Atlasiet **Saglabāt darbu**, lai saglabātu darbu, neatstājot Attract.</span><span class="sxs-lookup"><span data-stu-id="ed1df-138">Select **Save to a job** to save the job without leaving Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="ed1df-139">Kandidāta LinkedIn profils tiks parādīts sistēmā Attract, kad kandidāta Attract informācija atbildīs LinkedIn informācijai.</span><span class="sxs-lookup"><span data-stu-id="ed1df-139">A candidate's LinkedIn profile will display in Attract when the candidate's Attract information matches the LinkedIn information.</span></span> <span data-ttu-id="ed1df-140">Tālāk ir norādītas izmantotās atbilstības kārtulas.</span><span class="sxs-lookup"><span data-stu-id="ed1df-140">Here are the matching rules that are used:</span></span>
> 
> 1. <span data-ttu-id="ed1df-141">Ja e-pasta adrese un LinkedIn dalībnieka ID atbilst sistēmā Attract un LinkedIn, tiek parādīts kandidāta profils.</span><span class="sxs-lookup"><span data-stu-id="ed1df-141">If the email address and LinkedIn member ID match in Attract and LinkedIn, the candidate's profile is shown.</span></span> <span data-ttu-id="ed1df-142">Kandidātiem joprojām ir iespēja saistīt vai atsaistīt savu LinkedIn profilu no sistēmas Attract.</span><span class="sxs-lookup"><span data-stu-id="ed1df-142">Candidates still have the option to link or unlink their LinkedIn profile from Attract.</span></span>
> 2. <span data-ttu-id="ed1df-143">Ja e-pasta adrese vai LinkedIn dalībnieka ID nesakrīt, tiek parādīts iespējamo kandidātu saraksts.</span><span class="sxs-lookup"><span data-stu-id="ed1df-143">If the email address or LinkedIn member ID doesn't match, you see a list of possible candidates.</span></span> <span data-ttu-id="ed1df-144">Pēc tam varat sarakstā atlasīt kandidātu un saistīt profilu.</span><span class="sxs-lookup"><span data-stu-id="ed1df-144">You can then select a candidate in the list and link the profile.</span></span>
> 3. <span data-ttu-id="ed1df-145">Ja nav pienācīgu atbilstību, saņemsit paziņojumu, ka atbilstība netika atrasta.</span><span class="sxs-lookup"><span data-stu-id="ed1df-145">If there are no good matches, you're notified that no match was found.</span></span>

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a><span data-ttu-id="ed1df-146">LinkedIn kandidātu eksportēšana uz Attract ar vienu klikšķi</span><span class="sxs-lookup"><span data-stu-id="ed1df-146">Export LinkedIn candidates to Attract with one click</span></span>

<span data-ttu-id="ed1df-147">Kamēr pārskatāt kandidātus LinkedIn Recruiter, varat tos eksportēt uz darbiem, kas pašlaik ir atvērti sistēmā Attract.</span><span class="sxs-lookup"><span data-stu-id="ed1df-147">While you're reviewing candidates in LinkedIn Recruiter, you can export them to jobs that you currently have open in Attract.</span></span> <span data-ttu-id="ed1df-148">Šai darbībai ir nepieciešamas personāla atlases darbinieka vai par pieņemšanu darbā atbildīgā vadītāja atļaujas sistēmā Attract.</span><span class="sxs-lookup"><span data-stu-id="ed1df-148">For this step, you need Recruiter or Hiring Manager permissions in Attract.</span></span> <span data-ttu-id="ed1df-149">Papildinformāciju par lomām sistēmā Attract skatiet rakstā [Drošība un lomu pārvaldība sistēmā Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).</span><span class="sxs-lookup"><span data-stu-id="ed1df-149">For more information about roles in Attract, see [Security and role management in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).</span></span>

<span data-ttu-id="ed1df-150">Jums ir arī jāpārliecinās, ka darbs ir stadijā Potenciālais kandidāts.</span><span class="sxs-lookup"><span data-stu-id="ed1df-150">You must also make sure that the job has a Prospect stage.</span></span> <span data-ttu-id="ed1df-151">Plašāku informāciju skatiet tēmā [Potenciālā kandidāta darbība](./activities-attract.md#prospect-activity).</span><span class="sxs-lookup"><span data-stu-id="ed1df-151">For more information, see [Prospect activity](./activities-attract.md#prospect-activity).</span></span>

1. <span data-ttu-id="ed1df-152">Sistēmā Attract izveidojiet vakanci, piešķiriet atbilstošās lomas un aktivizējiet šo vakanci.</span><span class="sxs-lookup"><span data-stu-id="ed1df-152">In Attract, create a job, assign the appropriate roles, and activate the job.</span></span>
2. <span data-ttu-id="ed1df-153">In LinkedIn Recruiter atrodiet labu kandidātu vakancei un dodieties uz kandidāta profilu.</span><span class="sxs-lookup"><span data-stu-id="ed1df-153">In LinkedIn Recruiter, find a good candidate for the job, and go to the candidate's profile.</span></span>
3. <span data-ttu-id="ed1df-154">Kontaktinformācijas kartiņā pieejamo vakanču meklēšanas lodziņā atrodiet vakanci, izmantojot sistēmā Attract aktivizēto nosaukumu vai vakances ID.</span><span class="sxs-lookup"><span data-stu-id="ed1df-154">In the job search box in the contact card, find the job by using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="ed1df-155">Ja nevarat atrast vakanci, atlasiet **Mainīt ATS**, lai atrastu pareizo Attract instanci.</span><span class="sxs-lookup"><span data-stu-id="ed1df-155">If you can't find the job, select **Change ATS** to find the correct Attract instance.</span></span>
4. <span data-ttu-id="ed1df-156">Atlasiet vakanci un pēc tam atlasiet **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="ed1df-156">Select the job, and then select **Export**.</span></span>
5. <span data-ttu-id="ed1df-157">Sistēmā Attract atveriet darbu.</span><span class="sxs-lookup"><span data-stu-id="ed1df-157">In Attract, open the job.</span></span> <span data-ttu-id="ed1df-158">Eksportētais kandidāts tiks parādīts darba cilnē **Potenciālais kandidāts**.</span><span class="sxs-lookup"><span data-stu-id="ed1df-158">The exported candidate will appear on the **Prospect** tab of the job.</span></span>

## <a name="view-attract-information-in-linkedin-recruiter"></a><span data-ttu-id="ed1df-159">Attract informācijas skatīšana LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="ed1df-159">View Attract information in LinkedIn Recruiter</span></span>

<span data-ttu-id="ed1df-160">LinkedIn Recruiter varat izsekot tam, vai kandidāts ir pietiecies citām vakancēm jūsu organizācijā, skatīt, vai kandidāts ir dažādos darba pieteikumu posmos, un skatīt programmā Attract pievienotās atsauksmes un komentārus.</span><span class="sxs-lookup"><span data-stu-id="ed1df-160">In LinkedIn Recruiter, you can track whether a candidate applied to other jobs in your organization, see where the candidate is in the various stages for job applications, and view feedback and comments from Attract.</span></span>

1. <span data-ttu-id="ed1df-161">Atveriet LinkedIn Recruiter un atlasiet kandidāta profilu.</span><span class="sxs-lookup"><span data-stu-id="ed1df-161">Open LinkedIn Recruiter, and select a candidate profile.</span></span>
2. <span data-ttu-id="ed1df-162">Virziet kursoru uz **ATS**.</span><span class="sxs-lookup"><span data-stu-id="ed1df-162">Hover over **In ATS**.</span></span>
3. <span data-ttu-id="ed1df-163">Atlasiet kādu no tālāk minētajām opcijām, lai skatītu informāciju par kandidātu, kas glabājas sistēmā Attract.</span><span class="sxs-lookup"><span data-stu-id="ed1df-163">Select any of the following options to view the candidate information that is stored in Attract:</span></span>

    - <span data-ttu-id="ed1df-164">**Darbi un statusi** — skatiet darbus, kuru daļa ir kandidāts, jaunāko statusu un kandidāta virzību katram darbam.</span><span class="sxs-lookup"><span data-stu-id="ed1df-164">**Jobs & Statuses** – See jobs that the candidate is part of, the latest status, and how the candidate is progressing for each job.</span></span>
    - <span data-ttu-id="ed1df-165">**Atsauksmes par interviju** — skatiet atsauksmes, ko intervētāji ir iesnieguši sistēmā Attract.</span><span class="sxs-lookup"><span data-stu-id="ed1df-165">**Interview Feedback** – See feedback that interviewers have submitted in Attract.</span></span>
    - <span data-ttu-id="ed1df-166">**Piezīmes** — skatiet piezīmes, kas ievadītas par šo kandidātu sistēmā Attract.</span><span class="sxs-lookup"><span data-stu-id="ed1df-166">**Notes** – See any notes that have been entered for this candidate in Attract.</span></span>

    ![[<span data-ttu-id="ed1df-167">Attract informācijas skatīšana no LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="ed1df-167">View Attract information from LinkedIn Recruiter</span></span>](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> <span data-ttu-id="ed1df-168">Ja kandidāts nav ticis tālāk par potenciālā kandidāta posmu, kandidāta un pieteikuma dati netiks sinhronizēti ar LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="ed1df-168">Candidate and application data won't be synced with LinkedIn Recruiter if the candidate hasn't moved past the Prospect stage.</span></span>

## <a name="view-linkedin-talent-pools"></a><span data-ttu-id="ed1df-169">LinkedIn talantu kopu skatīšana</span><span class="sxs-lookup"><span data-stu-id="ed1df-169">View LinkedIn talent pools</span></span>

<span data-ttu-id="ed1df-170">Ja kandidāti piekrīt kopīgot savus LinkedIn profilus ar jebkuru lietotāju jūsu organizācijā, sistēmā Attract tiek izveidots jauns kandidāta ieraksts.</span><span class="sxs-lookup"><span data-stu-id="ed1df-170">If candidates agree to share their LinkedIn profiles with any user in your organization, a new candidate record is created in Attract.</span></span> <span data-ttu-id="ed1df-171">Pēc tam šie kandidāti tiek rādīti sistēmas izveidotajā LinkedIn talantu kopā.</span><span class="sxs-lookup"><span data-stu-id="ed1df-171">These candidates then appear in a system-created LinkedIn talent pool.</span></span>

1. <span data-ttu-id="ed1df-172">Sistēmā Attract kreisajā pusē atlasiet **Talantu kopas**.</span><span class="sxs-lookup"><span data-stu-id="ed1df-172">In Attract, select **Talent pools** on the left.</span></span>
2. <span data-ttu-id="ed1df-173">Atlasiet LinkedIn talantu kopu.</span><span class="sxs-lookup"><span data-stu-id="ed1df-173">Select the LinkedIn talent pool.</span></span> <span data-ttu-id="ed1df-174">Redzēsit kandidātu sarakstu un to pasakņa profilus no LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="ed1df-174">You will see a list of candidates and their stub profiles from LinkedIn.</span></span> <span data-ttu-id="ed1df-175">Pasakņa profili ietver kandidāta vārdu, uzvārdu un e-pasta adresi, ja kandidāts izvēlējies to kopīgot.</span><span class="sxs-lookup"><span data-stu-id="ed1df-175">Stub profiles contain the candidate's first and last names and email address, if the candidate chose to share it.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed1df-176">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="ed1df-176">See also</span></span>

[<span data-ttu-id="ed1df-177">Attract integrācija ar LinkedIn — bieži uzdotie jautājumi</span><span class="sxs-lookup"><span data-stu-id="ed1df-177">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="ed1df-178">Integrācijas ar LinkedIn iestatīšana programmai Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="ed1df-178">Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-admin-linkedin.md)

[<span data-ttu-id="ed1df-179">Darbu izveide, apstiprināšana un grāmatošana programmā Attract</span><span class="sxs-lookup"><span data-stu-id="ed1df-179">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="ed1df-180">Vakanču publicēšana LinkedIn no pakalpojuma Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="ed1df-180">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="ed1df-181">Integrācijas problēmu novēršana ar LinkedIn un Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="ed1df-181">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
