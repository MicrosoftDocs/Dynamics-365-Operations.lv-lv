---
title: "Kandidātu piesaiste, izmantojot LinkedIn Recruiter"
description: "Šajā tēmā ir sniegta informācija par algoritmiskās mācīšanās izmantošanu, lai iegūtu darba un amata kandidātu ieteikumus."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: lv-lv
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="3a640-103">Kandidātu piesaiste, izmantojot LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="3a640-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="3a640-104">LinkedIn ir pasaulē lielākā potenciālo kandidātu datu bāze un bieži vien galvenā sistēma, ko izmanto personāla atlases darbinieki, lai atrastu kandidātus aktuālajām vakancēm, sazinātos ar šiem kandidātiem un piesaistītu viņus.</span><span class="sxs-lookup"><span data-stu-id="3a640-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="3a640-105">LinkedIn Recruiter integrācija ar programmu Dynamics 365 for Talent: Attract atvieglo pieņemšanu darbā un datu sinhronizāciju abās sistēmās.</span><span class="sxs-lookup"><span data-stu-id="3a640-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="3a640-106">Lai varētu izmantot LinkedIn Recruiter integrāciju ar Attract, ir nepieciešams visaptverošais darbā pieņemšanas papildinājums un LinkedIn Recruiter licences.</span><span class="sxs-lookup"><span data-stu-id="3a640-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="3a640-107">LinkedIn Recruiter iestatīšana programmā Attract</span><span class="sxs-lookup"><span data-stu-id="3a640-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="3a640-108">Lai varētu izmantot LinkedIn Recruiter iespējas, vispirms Attract instancē ir jākonfigurē līguma līmeņa vai uzņēmuma līmeņa piekļuve.</span><span class="sxs-lookup"><span data-stu-id="3a640-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="3a640-109">Lai pabeigtu konfigurēšanas procesu, ir jāizmanto lietotāja konts, kas LinkedIn Recruiter līgumā ir norādīts kā administrators.</span><span class="sxs-lookup"><span data-stu-id="3a640-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="3a640-110">Veiciet tālāk norādītās darbības, lai konfigurētu LinkedIn Recruiter programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="3a640-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="3a640-111">Pierakstieties programmā Attract, izmantojot administratora kontu, un pārejiet uz sadaļu **Administratora iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="3a640-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="3a640-112">Kreisajā rūtī noklikšķiniet uz cilnes **LinkedIn integrācija**.</span><span class="sxs-lookup"><span data-stu-id="3a640-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="3a640-113">[![Attract administratora skats, kurā var sākt LinkedIn Recruiter integrāciju](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="3a640-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="3a640-114">Noklikšķiniet uz **Izveidot savienojumu**, lai sāktu iestatīšanu un izpildītu sniegtos LinkedIn pierakstīšanās procesa norādījumus.</span><span class="sxs-lookup"><span data-stu-id="3a640-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="3a640-115">Ja jums ir vairāku LinkedIn līgumu licences, atlasiet to līgumu, kam vēlaties izveidot savienojumu ar sistēmu Attract.</span><span class="sxs-lookup"><span data-stu-id="3a640-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="3a640-116">Ja jums ir tikai viena LinkedIn līguma licence, šī darbība nav jāveic.</span><span class="sxs-lookup"><span data-stu-id="3a640-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="3a640-117">Tagad sadaļā Administratora iestatījumi tiek ielādēts LinkedIn logrīks, kurā tiek rādīts integrācijas gadījumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="3a640-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="3a640-118">Sadaļā **Recruiter System Connect** noklikšķiniet uz **Pieprasīt**.</span><span class="sxs-lookup"><span data-stu-id="3a640-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="3a640-119">[![Attract administratora skats, kurā var pieprasīt LinkedIn Recruiter integrāciju](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="3a640-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="3a640-120">Pēc integrācijas pieprasījuma iesniegšanas no programmas Attract, tiek parādīts statuss **Partneris gatavs** un šo līdzekli var ieslēgt sadaļā **Recruiter administratora iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="3a640-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="3a640-121">Ja šajā lapā tiek rādīts statuss **Paziņot partnerim**, uzgaidiet pāris sekundes, noklikšķiniet uz **Paziņot partnerim** un pēc tam atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="3a640-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="3a640-122">Tagad statusam ir jābūt **Partneris gatavs**.</span><span class="sxs-lookup"><span data-stu-id="3a640-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="3a640-123">[![Attract administratora skats, kurā var norādīt Attract, ka programmā Attract ir pabeigtas pieprasījumu iesniegšanas darbības](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="3a640-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="3a640-124">Lai pabeigtu nākamo darbību, ir vajadzīga administratora atļauja, kad ir piešķirta LinkedIn Recruiter līgumā.</span><span class="sxs-lookup"><span data-stu-id="3a640-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="3a640-125">Pierakstieties pakalpojumā LinkedIn, izmantojot administratora kontu, un pārejiet uz sadaļu LinkedIn Recruiter lapas augšējā labajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="3a640-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="3a640-126">Ekrāna augšdaļā esošajā izvēlnē **Vairāk** noklikšķiniet uz **Administratora iestatījumi** un pēc tam noklikšķiniet uz cilnes **ATS**.</span><span class="sxs-lookup"><span data-stu-id="3a640-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="3a640-127">Tiek parādīta sistēma Attract un dažas opcijas, ko var ieslēgt.</span><span class="sxs-lookup"><span data-stu-id="3a640-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="3a640-128">Ja vēlaties iespējot tikai **ATS pieejamo datu indikatora** un **ATS pieejamo datu profila logrīka** viena klikšķa eksportēšanu, atlasiet **Uzņēmuma līmeņa piekļuve**.</span><span class="sxs-lookup"><span data-stu-id="3a640-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="3a640-129">Ja vēlaties iespējot visus uzņēmuma līmeņa piekļuves līmeņus, kā arī InMail vēsturi, piezīmju vēsturi un InMail pasakņa profilu, atlasiet **Līguma līmeņa piekļuve**.</span><span class="sxs-lookup"><span data-stu-id="3a640-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="3a640-130">Ieslēdziet vēlamo piekļuves līmeni LinkedIn Recruiter iestatījumu sadaļā **ATS administrēšana**.</span><span class="sxs-lookup"><span data-stu-id="3a640-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="3a640-131">[![Attract integrācijas ieslēgšana LinkedIn Recruiter administratora skatā](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="3a640-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="3a640-132">Pierakstieties kā Attract administrators, pārejiet uz Attract sadaļu Admin Settings (Administratora iestatījumi) un atlasiet cilni **LinkedIn integrācija**. Tagad tiek ielādēts LinkedIn logrīks, kurā tiek rādīts statuss **Iespējots** un ir ieslēgts atlasītais piekļuves līmenis.</span><span class="sxs-lookup"><span data-stu-id="3a640-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="3a640-133">[![LinkedIn Recruiter integrācija ir pabeigta](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="3a640-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="3a640-134">LinkedIn Recruiter iespēju lietošana</span><span class="sxs-lookup"><span data-stu-id="3a640-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="3a640-135">Kad Attract administrators ir iespējojis LinkedIn Recruiter iespējas, tām var piekļūt par pieņemšanu darbā atbildīgie vadītāji un personāla atlases darbinieki.</span><span class="sxs-lookup"><span data-stu-id="3a640-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="3a640-136">Lai izmantotu šīs iespējas, sadaļā **Lietotāja iestatījumi** izveidojiet savienojumu ar savu LinkedIn kontu.</span><span class="sxs-lookup"><span data-stu-id="3a640-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="3a640-137">Dažas iespējas kļūst pieejamas pēc tam, kad ir izveidots savienojums gan administratora, gan lietotāja iestatījumu sadaļā.</span><span class="sxs-lookup"><span data-stu-id="3a640-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="3a640-138">ATS pieejamo datu profila logrīks</span><span class="sxs-lookup"><span data-stu-id="3a640-138">In-ATS profile widget</span></span>

<span data-ttu-id="3a640-139">Varat skatīt kandidāta LinkedIn profilu programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="3a640-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="3a640-140">Ja lietotāju ATS informācija atbilst LinkedIn informācijai, LinkedIn logrīkā tiek rādīts kandidāta profils.</span><span class="sxs-lookup"><span data-stu-id="3a640-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="3a640-141">Lai skatītu profilu, pārejiet uz kandidāta profilu vakances vai potenciālo kandidātu kopas sadaļā.</span><span class="sxs-lookup"><span data-stu-id="3a640-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="3a640-142">Kandidāta profilā atlasiet cilni **LinkedIn**, lai ielādētu profila logrīku.</span><span class="sxs-lookup"><span data-stu-id="3a640-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="3a640-143">Izmantojot profila logrīku, norādiet, vai atbilstība ir noteikta pareizi.</span><span class="sxs-lookup"><span data-stu-id="3a640-143">Using the profile widget, indicate if this is the correct match.</span></span> <span data-ttu-id="3a640-144">Ja tā nav, atrodiet pareizo personu.</span><span class="sxs-lookup"><span data-stu-id="3a640-144">If it is not, find the correct person.</span></span> <span data-ttu-id="3a640-145">Šajā lapā varat arī saglabāt kandidātu savos LinkedIn Recruiter projektos.</span><span class="sxs-lookup"><span data-stu-id="3a640-145">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="3a640-146">Viena klikšķa eksportēšana</span><span class="sxs-lookup"><span data-stu-id="3a640-146">1-click export</span></span> 

<span data-ttu-id="3a640-147">Kamēr piesaistāt kandidātus pakalpojumā LinkedIn, varat ar vienu klikšķi eksportēt kandidātu uz pašlaik brīvajām vakancēm.</span><span class="sxs-lookup"><span data-stu-id="3a640-147">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="3a640-148">Lai veiktu viena klikšķa eksportēšanu, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="3a640-148">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="3a640-149">Pirms šo darbību veikšanas pārbaudiet, vai jums ir piešķirta loma Par pieņemšanu darbā atbildīgais vadītājs vai Personāla atlases darbinieks attiecīgajai vakancei un vai vakancei ir posms **Potenciālais kandidāts**.</span><span class="sxs-lookup"><span data-stu-id="3a640-149">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="3a640-150">Izveidojiet vakanci, piešķiriet atbilstošās lomas un aktivizējiet šo vakanci.</span><span class="sxs-lookup"><span data-stu-id="3a640-150">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="3a640-151">Kad vakance ir aktivizēta, pārejiet uz LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="3a640-151">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="3a640-152">Atrodiet meklēto kandidātu un pārejiet uz viņa profilu.</span><span class="sxs-lookup"><span data-stu-id="3a640-152">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="3a640-153">Izmantojot kontaktinformācijas kartiņā pieejamo vakanču meklēšanas lodziņu, atrodiet programmā Attract aktivizēto vakanci pēc nosaukuma vai vakances ID.</span><span class="sxs-lookup"><span data-stu-id="3a640-153">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="3a640-154">Ja neatrodat vakanci, noklikšķiniet uz **Mainīt ATS**, lai atrastu pareizo Attract instanci.</span><span class="sxs-lookup"><span data-stu-id="3a640-154">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="3a640-155">Kad vakance ir atlasīta, noklikšķiniet uz **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="3a640-155">After the job is selected, click **Export**.</span></span> <span data-ttu-id="3a640-156">Tagad kandidāts tiek izgūts programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="3a640-156">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="3a640-157">Pārejiet uz programmu Attract un atveriet atbilstošo vakanci.</span><span class="sxs-lookup"><span data-stu-id="3a640-157">Go to Attract and open the respective job.</span></span> <span data-ttu-id="3a640-158">Tikko eksportētais kandidāts ir pievienots vakances posmam **Potenciālais kandidāts**.</span><span class="sxs-lookup"><span data-stu-id="3a640-158">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="3a640-159">ATS pieejamo datu indikators</span><span class="sxs-lookup"><span data-stu-id="3a640-159">In-ATS indicator</span></span> 

<span data-ttu-id="3a640-160">Izmantojot LinkedIn Recruiter, varat izsekot tam, vai kandidāts ir pietiecies citām vakancēm jūsu organizācijā, uzzināt, vai viņam ir iestatīti dažādi darba pieteikumu posmi, un skatīt programmā Attract pievienotās atsauksmes un komentārus pakalpojumā LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="3a640-160">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="3a640-161">Atveriet LinkedIn Recruiter un atrodiet meklēto kandidāta profilu.</span><span class="sxs-lookup"><span data-stu-id="3a640-161">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="3a640-162">Ritiniet uz leju, lai skatītu kandidāta profila sadaļu **ATS pieejamie dati**.</span><span class="sxs-lookup"><span data-stu-id="3a640-162">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="3a640-163">Varat izmantot šo logrīku, lai LinkedIn Recruiter skatā piekļūtu visai informācijai par kandidātu, kas ir pieejama programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="3a640-163">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="3a640-164">Atlasiet cilni **Vakances un statusi**, lai skatītu ar kandidātu saistītās vakances, viņa jaunāko statusu un progresu katras vakances darbā pieņemšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="3a640-164">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="3a640-165">Atlasiet cilni **Atsauksmes par interviju**, lai skatītu atsauksmes, ko intervētāji ir iesnieguši programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="3a640-165">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="3a640-166">Atlasiet cilni **Piezīmes**, lai skatītu programmā Attract saglabātās piezīmes par šo kandidātu.</span><span class="sxs-lookup"><span data-stu-id="3a640-166">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="3a640-167">InMail vēsture</span><span class="sxs-lookup"><span data-stu-id="3a640-167">InMail history</span></span>

<span data-ttu-id="3a640-168">LinkedIn InMail vēsture ir pieejama tad, ja ir pieejama līguma līmeņa piekļuve pakalpojumam LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="3a640-168">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="3a640-169">Ja ir iespējots šis līdzeklis, varat skatīt visu saziņas ar kandidātu InMail vēsturi.</span><span class="sxs-lookup"><span data-stu-id="3a640-169">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="3a640-170">Varat arī uzzināt, kas vēl jūsu organizācijā ir sazinājies ar kandidātu, izmantojot InMail, taču nevarat skatīt šīs saziņas ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="3a640-170">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="3a640-171">Lai skatītu InMail vēsturi, pārejiet uz kandidāta profilu, atveriet cilni **LinkedIn** un ritiniet līdz lapas apakšdaļai, kur ir pieejama vēsture.</span><span class="sxs-lookup"><span data-stu-id="3a640-171">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="3a640-172">InMail vēsturi varat skatīt tikai tad, ja kandidāts ir atbildējis uz jūsu pieprasījumu un izvēlējies ar jums kopīgot savu profilu pakalpojumā LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="3a640-172">You can view the InMail history only if the candidate has responded to your request and chosen to share their profile with you in LinkedIn.</span></span> <span data-ttu-id="3a640-173">InMail ziņojumi tiek sinhronizēti ar programmu Attract ik pēc dažām stundām.</span><span class="sxs-lookup"><span data-stu-id="3a640-173">The messages from InMail sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="3a640-174">Piezīmju vēsture</span><span class="sxs-lookup"><span data-stu-id="3a640-174">Notes history</span></span> 

<span data-ttu-id="3a640-175">LinkedIn piezīmju vēsture ir pieejama tad, ja ir pieejama līguma līmeņa piekļuve pakalpojumam LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="3a640-175">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="3a640-176">Ja ir iespējots šis līdzeklis, varat skatīt piezīmes par kandidātu, kuras ir saglabājuši dažādi jūsu organizācijas personāla atlases darbinieki.</span><span class="sxs-lookup"><span data-stu-id="3a640-176">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="3a640-177">Lai skatītu piezīmju vēsturi, pārejiet uz kandidāta profilu, atveriet cilni **LinkedIn** un ritiniet līdz lapas apakšdaļai, kur ir pieejama vēsture.</span><span class="sxs-lookup"><span data-stu-id="3a640-177">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="3a640-178">Varat skatīt visas piezīmes par kandidātu pakalpojumā LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="3a640-178">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="3a640-179">InMail pasakņa profils</span><span class="sxs-lookup"><span data-stu-id="3a640-179">InMail stub profile</span></span>

<span data-ttu-id="3a640-180">InMail pasakņa profils ir pieejams tad, ja ir pieejama līguma līmeņa piekļuve pakalpojumam LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="3a640-180">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="3a640-181">Ja kandidāti piekrīt kopīgot savu LinkedIn profilu ar jebkuru jūsu organizācijas lietotāju, jūs varat izsekot kandidātus programmā Attract un katram kandidātam tiek izveidots jauns kandidāta ieraksts.</span><span class="sxs-lookup"><span data-stu-id="3a640-181">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span>

<span data-ttu-id="3a640-182">Lai skatītu kandidātu sarakstu, pārejiet uz sadaļu **Potenciālo kandidātu kopas**, kurā ir redzama sistēmas izveidota LinkedIn potenciālo kandidātu kopa.</span><span class="sxs-lookup"><span data-stu-id="3a640-182">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="3a640-183">Šajā potenciālo kandidātu kopā ir ietverts no LinkedIn saņemtais kandidātu un to pasakņa profilu saraksts, kurā ir redzams kandidāta vārds un uzvārds.</span><span class="sxs-lookup"><span data-stu-id="3a640-183">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="3a640-184">Ja kandidāts ir izvēlējies kopīgot savu e-pasta adresi, tiek rādīts kandidāta e-pasta adreses ID.</span><span class="sxs-lookup"><span data-stu-id="3a640-184">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>

