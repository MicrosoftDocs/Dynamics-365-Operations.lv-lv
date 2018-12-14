---
title: "Aktivitātes procesa ietvaros"
description: "Šajā tēma ir sniegta informācija par dažādajiem aktivitāšu veidiem, ko var izmantot darbā pieņemšanas procesa ietvaros."
author: 
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
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: ccd9e2d0ff1f7fb6825c6823936b4013b3054f5d
ms.contentlocale: lv-lv
ms.lasthandoff: 10/22/2018

---

# <a name="activities-in-the-hiring-processes"></a><span data-ttu-id="d0959-103">Aktivitātes darbā pieņemšanas procesa ietvaros</span><span class="sxs-lookup"><span data-stu-id="d0959-103">Activities in the hiring processes</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d0959-104">Darbā pieņemšanas procesam programmā Microsoft Dynamics 365 for Talent: Attract var pievienot aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="d0959-104">Activities can be added as a part of the hiring process in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="d0959-105">Aktivitātes var pievienot procesa veidnei vai tiešā veidā pievienot vakances darbā pieņemšanas procesam.</span><span class="sxs-lookup"><span data-stu-id="d0959-105">Activities can be added to a process template, or they can be added directly to the hiring process in the job.</span></span> <span data-ttu-id="d0959-106">Definējot vakanci, tiek atlasīta procesa veidne un šai vakancei tiek lietotas veidnē ietvertās aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="d0959-106">When a job is defined, a process template is selected, and the activities that are included in the template are applied to the job.</span></span> <span data-ttu-id="d0959-107">Ja netiek atlasīta veidne, tiek izmantota noklusējuma veidne.</span><span class="sxs-lookup"><span data-stu-id="d0959-107">If a template isn't selected, the default template is used.</span></span> <span data-ttu-id="d0959-108">Vakances darbā pieņemšanas procesu var modificēt arī pēc veidnes lietošanas.</span><span class="sxs-lookup"><span data-stu-id="d0959-108">The hiring process can also be modified on the job after the template is applied.</span></span>

> [!NOTE] 
> <span data-ttu-id="d0959-109">Procesa veidnes ir pieejamas tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.</span><span class="sxs-lookup"><span data-stu-id="d0959-109">Process templates are available with the Comprehensive hiring add-on.</span></span>

## <a name="prospect-activity"></a><span data-ttu-id="d0959-110">Aktivitāte Potenciālais kandidāts</span><span class="sxs-lookup"><span data-stu-id="d0959-110">Prospect activity</span></span>

<span data-ttu-id="d0959-111">Aktivitāte Potenciālais kandidāts sniedz iespēju kontrolēt to, vai potenciālos kandidātus var pievienot vakancei.</span><span class="sxs-lookup"><span data-stu-id="d0959-111">The Prospect activity controls whether prospects can be added to a job.</span></span> <span data-ttu-id="d0959-112">Pēc noklusējuma vakancei var pievienot potenciālos kandidātus.</span><span class="sxs-lookup"><span data-stu-id="d0959-112">By default, prospects can be added to a job.</span></span> <span data-ttu-id="d0959-113">Lai izslēgtu aktivitāti Potenciālais kandidāts, iestatiet opcijas **Iespējot potenciālos kandidātus** vērtību **Izslēgts**.</span><span class="sxs-lookup"><span data-stu-id="d0959-113">To turn off the Prospect activity, set the **Enable prospects** option to **Off**.</span></span> <span data-ttu-id="d0959-114">Kad ir ieslēgta aktivitāte Potenciālais kandidāts, par pieņemšanu darbā atbildīgie vadītāji var pievienot un skatīt potenciālos kandidātus un vakances sadaļā tiek rādīta cilne **Potenciālais kandidāts**.</span><span class="sxs-lookup"><span data-stu-id="d0959-114">When the Prospect activity is turned on, hiring managers can add and view prospects, and the **Prospect** tab is shown on the job.</span></span>

## <a name="application-activity"></a><span data-ttu-id="d0959-115">Aktivitāte Pieteikums</span><span class="sxs-lookup"><span data-stu-id="d0959-115">Application activity</span></span>

<span data-ttu-id="d0959-116">Aktivitāte Pieteikums ir obligāta darbā pieņemšanas procesa veidnes aktivitāte.</span><span class="sxs-lookup"><span data-stu-id="d0959-116">The Application activity is required in the hiring process template.</span></span> <span data-ttu-id="d0959-117">Lai kandidātiem nosūtītu e-pasta ziņojumu, kad viņi iesniedz savu pieteikumu vai tiek pievienoti posmam Pieteikums, iestatiet opcijas **Sūtīt vēstuli kandidātam** vērtību **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="d0959-117">To send email to candidates when they submit their application or are added to the Application stage, set the **Send mail to candidate** option to **On**.</span></span>

## <a name="scheduler-activity"></a><span data-ttu-id="d0959-118">Aktivitāte Plānotājs</span><span class="sxs-lookup"><span data-stu-id="d0959-118">Scheduler activity</span></span>

<span data-ttu-id="d0959-119">Aktivitāte Plānotājs ir izvēles aktivitāte.</span><span class="sxs-lookup"><span data-stu-id="d0959-119">The Scheduler activity is optional.</span></span> <span data-ttu-id="d0959-120">Šī aktivitāte sastāv no diviem komponentiem: Kandidāta pieejamība un Grafiks.</span><span class="sxs-lookup"><span data-stu-id="d0959-120">This activity has two components: Candidate availability and Schedule.</span></span> <span data-ttu-id="d0959-121">Komponents Kandidāta pieejamība sniedz jums iespēju izmantot e-pastu, lai pieprasītu kandidāta pieejamību.</span><span class="sxs-lookup"><span data-stu-id="d0959-121">The Candidate availability component lets you use email to request a candidate's availability.</span></span> <span data-ttu-id="d0959-122">Komponents Grafiks sniedz iespēju ieplānot intervijas, saskaņojot grafiku ar kandidātu un darbā pieņemšanas grupu.</span><span class="sxs-lookup"><span data-stu-id="d0959-122">The Schedule component provides the ability to schedule interviews with the candidate and the hiring team.</span></span> <span data-ttu-id="d0959-123">Aktivitātes Plānotājs ietvaros var konfigurēt šādas opcijas: **Pieprasīt kandidāta pieejamību**, **Tiešsaistes sapulce** un **Sūtīt vēstuli kandidātam**.</span><span class="sxs-lookup"><span data-stu-id="d0959-123">In the Scheduler activity, the following options can be configured: **Request candidate availability**, **Online meeting**, and **Send mail to candidate**.</span></span>

- <span data-ttu-id="d0959-124">Lai sūtītu kandidātiem e-pasta ziņojumus un pieprasītu viņu pieejamību, iestatiet opcijas **Pieprasīt kandidāta pieejamību** vērtību **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="d0959-124">To send email to candidates to request their availability, set the **Request candidate availability** option to **On**.</span></span> <span data-ttu-id="d0959-125">Ja iestatāt šīs opcijas vērtību **Izslēgts**, šī darbība netiek rādīta vakances darbā pieņemšanas procesa ietvaros.</span><span class="sxs-lookup"><span data-stu-id="d0959-125">If you set the option to **Off**, this step won't be shown in the hiring process on the job.</span></span>
- <span data-ttu-id="d0959-126">Lai veiktu tiešsaistes straumēšanu vai konferences zvanu, izmantojot Skype darbam, iestatiet lauka **Tiešsaistes sapulce** vērtību **Skype darbam**.</span><span class="sxs-lookup"><span data-stu-id="d0959-126">To live-stream or have a conference call by using Skype for Business, set the **Online meeting** field to **Skype for Business**.</span></span> <span data-ttu-id="d0959-127">Pēc tam intervētājiem nosūtītajā intervijas sapulces pieprasījumā tiek ietverta pareizā saite **Pievienoties Skype sapulcei**.</span><span class="sxs-lookup"><span data-stu-id="d0959-127">The correct **Join Skype Meeting** link will then be added in the interview meeting request that is sent to interviewers.</span></span>
- <span data-ttu-id="d0959-128">Lai sūtītu kandidātiem e-pasta ziņojumus un precizētu grafiku, iestatiet opcijas **Sūtīt vēstuli kandidātam** vērtību **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="d0959-128">To send email to candidates to finalize the schedule, set the **Send mail to candidate** option to **On**.</span></span> <span data-ttu-id="d0959-129">Ja iestatāt šīs opcijas vērtību **Izslēgts**, kandidāti saņem intervijas grafiku tikai pēc pierakstīšanās kandidātu portālā.</span><span class="sxs-lookup"><span data-stu-id="d0959-129">If you set the option to **Off**, candidates will receive the interview schedule only when they sign in to the Candidate portal.</span></span>

## <a name="feedback-activity"></a><span data-ttu-id="d0959-130">Aktivitāte Atsauksmes</span><span class="sxs-lookup"><span data-stu-id="d0959-130">Feedback activity</span></span>

<span data-ttu-id="d0959-131">Aktivitāte Atsauksmes ir izvēles aktivitāte.</span><span class="sxs-lookup"><span data-stu-id="d0959-131">The Feedback activity is optional.</span></span> <span data-ttu-id="d0959-132">Šī aktivitāte sniedz intervijas dalībniekiem iespēju ievadīt ieteikumus kandidātam.</span><span class="sxs-lookup"><span data-stu-id="d0959-132">This activity lets interview participants enter recommendations for an applicant.</span></span> <span data-ttu-id="d0959-133">Viņi var arī ievadīt jebkādus komentārus ar atsauksmēm.</span><span class="sxs-lookup"><span data-stu-id="d0959-133">They can also enter any feedback comments that they have.</span></span> <span data-ttu-id="d0959-134">Ja ieslēdzat opciju **Pārmantot atsauksmju dalībniekus no darbā pieņemšanas grupas**, personāla atlases darbinieks, par pieņemšanu darbā atbildīgais vadītājs un intervētāji tiek automātiski pievienoti aktivitātei Atsauksmes.</span><span class="sxs-lookup"><span data-stu-id="d0959-134">If you turn on the **Inherit feedback participants from Hiring Team** option, the recruiter, hiring manager, and interviewers are automatically entered in the Feedback activity.</span></span> <span data-ttu-id="d0959-135">Organizācijas var atļaut intervētajiem skatīt citu personu atsauksmes pirms savu atsauksmju iesniegšanas.</span><span class="sxs-lookup"><span data-stu-id="d0959-135">Organizations can allow interviewers to view the feedback of other people before they submit their own feedback.</span></span> <span data-ttu-id="d0959-136">Organizācijas var atļaut intervētājiem arī rediģēt savas atsauksmes pēc to iesniegšanas.</span><span class="sxs-lookup"><span data-stu-id="d0959-136">Organizations can also allow interviewers to edit their feedback after they submit it.</span></span>

## <a name="interview-activity"></a><span data-ttu-id="d0959-137">Aktivitāte Intervija</span><span class="sxs-lookup"><span data-stu-id="d0959-137">Interview activity</span></span>

<span data-ttu-id="d0959-138">Aktivitāte Intervija ir izvēles aktivitāte.</span><span class="sxs-lookup"><span data-stu-id="d0959-138">The Interview activity is optional.</span></span> <span data-ttu-id="d0959-139">Šī aktivitāte sastāv no trim komponentiem: Kandidāta pieejamība, Grafiks un Atsauksmes.</span><span class="sxs-lookup"><span data-stu-id="d0959-139">This activity has three components: Candidate availability, Schedule, and Feedback.</span></span> <span data-ttu-id="d0959-140">Komponents Kandidāta pieejamība sniedz jums iespēju izmantot e-pastu, lai pieprasītu kandidāta pieejamību.</span><span class="sxs-lookup"><span data-stu-id="d0959-140">The Candidate availability component lets you use email to request a candidate's availability.</span></span> <span data-ttu-id="d0959-141">Komponents Grafiks sniedz iespēju ieplānot intervijas, saskaņojot grafiku ar kandidātu un darbā pieņemšanas grupu.</span><span class="sxs-lookup"><span data-stu-id="d0959-141">The Schedule component provides the ability to schedule interviews with the candidate and the hiring team.</span></span> <span data-ttu-id="d0959-142">Aktivitātes Plānotājs ietvaros var konfigurēt šādas opcijas: **Pieprasīt kandidāta pieejamību**, **Tiešsaistes sapulce** un **Sūtīt vēstuli kandidātam**.</span><span class="sxs-lookup"><span data-stu-id="d0959-142">In the Scheduler activity, the following options can be configured: **Request candidate availability**, **Online meeting**, and **Send mail to candidate**.</span></span>

- <span data-ttu-id="d0959-143">Lai sūtītu kandidātiem e-pasta ziņojumus un pieprasītu viņu pieejamību, iestatiet opcijas **Pieprasīt kandidāta pieejamību** vērtību **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="d0959-143">To send email to candidates to request their availability, set the **Request candidate availability** option to **On**.</span></span> <span data-ttu-id="d0959-144">Ja iestatāt šīs opcijas vērtību **Izslēgts**, šī darbība netiek rādīta vakances darbā pieņemšanas procesa ietvaros.</span><span class="sxs-lookup"><span data-stu-id="d0959-144">If you set the option to **Off**, this step won't be shown in the hiring process on the job.</span></span>
- <span data-ttu-id="d0959-145">Lai veiktu tiešsaistes straumēšanu vai konferences zvanu, izmantojot Skype darbam, iestatiet lauka **Tiešsaistes sapulce** vērtību **Skype darbam**.</span><span class="sxs-lookup"><span data-stu-id="d0959-145">To live-stream or have a conference call by using Skype for Business, set the **Online meeting** field to **Skype for Business**.</span></span> <span data-ttu-id="d0959-146">Pēc tam intervijas sapulces pieprasījumā tiek ietverta pareizā saite **Pievienoties Skype sapulcei**.</span><span class="sxs-lookup"><span data-stu-id="d0959-146">The correct **Join Skype Meeting** link will then be added in the interview meeting request.</span></span>
- <span data-ttu-id="d0959-147">Lai sūtītu kandidātiem e-pasta ziņojumus un precizētu grafiku, iestatiet opcijas **Sūtīt vēstuli kandidātam** vērtību **Ieslēgts**.</span><span class="sxs-lookup"><span data-stu-id="d0959-147">To send email to candidates to finalize the schedule, set the **Send mail to candidate** option to **On**.</span></span> <span data-ttu-id="d0959-148">Ja iestatāt šīs opcijas vērtību **Izslēgts**, kandidāti saņem intervijas grafiku tikai pēc pierakstīšanās kandidātu portālā.</span><span class="sxs-lookup"><span data-stu-id="d0959-148">If you set the option to **Off**, candidates will receive the interview schedule only when they sign in to the Candidate portal.</span></span>

<span data-ttu-id="d0959-149">Komponents Atsauksmes sniedz personām iespēju ievadīt ieteikumus kandidātam.</span><span class="sxs-lookup"><span data-stu-id="d0959-149">The Feedback component lets people enter recommendations for an applicant.</span></span> <span data-ttu-id="d0959-150">Viņi var arī ievadīt jebkādus komentārus ar atsauksmēm.</span><span class="sxs-lookup"><span data-stu-id="d0959-150">They can also enter any feedback comments that they have.</span></span> <span data-ttu-id="d0959-151">Ja ieslēdzat opciju **Pārmantot atsauksmju dalībniekus no darbā pieņemšanas grupas**, personāla atlases darbinieks, par pieņemšanu darbā atbildīgais vadītājs un intervētāji tiek automātiski pievienoti komponentam Atsauksmes.</span><span class="sxs-lookup"><span data-stu-id="d0959-151">If you turn on the **Inherit feedback participants from Hiring Team** option, the recruiter, hiring manager, and interviewers are automatically entered in the Feedback component.</span></span> <span data-ttu-id="d0959-152">Organizācijas var atļaut intervētajiem skatīt citu personu atsauksmes pirms savu atsauksmju iesniegšanas.</span><span class="sxs-lookup"><span data-stu-id="d0959-152">Organizations can allow interviewers to view the feedback of other people before they submit their own feedback.</span></span> <span data-ttu-id="d0959-153">Organizācijas var atļaut intervētājiem arī rediģēt savas atsauksmes pēc to iesniegšanas.</span><span class="sxs-lookup"><span data-stu-id="d0959-153">Organizations can also allow interviewers to edit their feedback after they submit it.</span></span>

## <a name="powerapps-activity"></a><span data-ttu-id="d0959-154">Aktivitāte PowerApps</span><span class="sxs-lookup"><span data-stu-id="d0959-154">PowerApps activity</span></span>

<span data-ttu-id="d0959-155">Aktivitāte PowerApps sniedz jums iespēju iegult darbā pieņemšanas procesā Microsoft PowerApps programmu.</span><span class="sxs-lookup"><span data-stu-id="d0959-155">The PowerApps activity lets you embed a Microsoft PowerApps app in your hiring process.</span></span> <span data-ttu-id="d0959-156">Programma var būt obligāta visiem kandidātiem, tikai iekšējiem kandidātiem, tikai ārējiem kandidātiem vai nevienam kandidātam.</span><span class="sxs-lookup"><span data-stu-id="d0959-156">The app can be required for all applicants, internal applicants only, external applicants only, or no applicants.</span></span> <span data-ttu-id="d0959-157">Ja programma ir atzīmēta kā obligāta, tā ir jāizpilda, pirms var pāriet uz nākamo posmu.</span><span class="sxs-lookup"><span data-stu-id="d0959-157">If the app is marked as required, it must be completed before the stage can be advanced.</span></span> <span data-ttu-id="d0959-158">Ja programma nav atzīmēta kā obligāta, šī aktivitāte ir izvēles darbība un uz nākamo posmu var pāriet pat tad, ja programma nav izpildīta.</span><span class="sxs-lookup"><span data-stu-id="d0959-158">If the app isn't marked as required, the activity is an optional step, and the stage can be advanced even if the app isn't completed.</span></span>

<span data-ttu-id="d0959-159">Lai saglabātu aktivitāti PowerApps darbā pieņemšanas procesā, ir jāievada PowerApps ID.</span><span class="sxs-lookup"><span data-stu-id="d0959-159">To save the PowerApps activity to the hiring process, you must enter a PowerApps ID.</span></span> <span data-ttu-id="d0959-160">Lai uzzinātu PowerApps ID, pārejiet uz sadaļu [PowerApps](https://web.powerapps.com), atlasiet **Programmas** un pēc tam atlasiet **Detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="d0959-160">To find the PowerApps ID, go to [PowerApps](https://web.powerapps.com), select **Apps**, and then select **Details**.</span></span>

<span data-ttu-id="d0959-161">Ja atlasāt opciju **Atļaut pievienot dalībniekus šai aktivitātei**, lietojumprogrammai, kas izmanto aktivitāti PowerApps, var pievienot papildu dalībniekus.</span><span class="sxs-lookup"><span data-stu-id="d0959-161">If you select the **Allow adding participants for this activity** option, additional contributors can be added for an application that uses the PowerApps activity.</span></span> <span data-ttu-id="d0959-162">Piemēram, organizācija var izveidot PowerApps programmu, kas ir tehnisko amatu kandidātu intervijām paredzētu jautājumu bibliotēka.</span><span class="sxs-lookup"><span data-stu-id="d0959-162">For example, an organization has created a PowerApps app that is a library of interview questions for technical roles.</span></span> <span data-ttu-id="d0959-163">Organizācija vēlas pieņemt darbā jaunu programmatūras izstrādātāju un ir pievienojusi amata Programmatūras izstrādātājs darbā pieņemšanas procesam aktivitāti PowerApps.</span><span class="sxs-lookup"><span data-stu-id="d0959-163">The organization is now hiring a new software developer and has added the PowerApps activity to the hiring process for the Software Developer role.</span></span> <span data-ttu-id="d0959-164">Ja ir atlasīta opcija **Atļaut pievienot dalībniekus šai aktivitātei**, personāla atlases darbinieks vai par pieņemšanu darbā atbildīgais vadītājs, kas skata amata Programmatūras izstrādātājs kandidātu, var pievienot personas aktivitātei PowerApps.</span><span class="sxs-lookup"><span data-stu-id="d0959-164">If the **Allow adding participants for this activity** option is selected, a recruiter or hiring manager who is viewing an applicant for the Software Developer role can add people to the PowerApps activity.</span></span> <span data-ttu-id="d0959-165">Pēc tam šīs personas var skatīt programmu, kurā ir ietverti intervijas jautājumi.</span><span class="sxs-lookup"><span data-stu-id="d0959-165">Those people can then view the app that has the interview questions.</span></span>

> [!NOTE]
> <span data-ttu-id="d0959-166">Aktivitāte PowerApps ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.</span><span class="sxs-lookup"><span data-stu-id="d0959-166">The PowerApps activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="youtube-activity"></a><span data-ttu-id="d0959-167">Aktivitāte YouTube</span><span class="sxs-lookup"><span data-stu-id="d0959-167">YouTube activity</span></span>

<span data-ttu-id="d0959-168">Aktivitāte YouTube sniedz jums iespēju darbā pieņemšanas procesa ietveros kopīgot YouTube video.</span><span class="sxs-lookup"><span data-stu-id="d0959-168">The YouTube activity lets you share a YouTube video as part of your hiring process.</span></span> <span data-ttu-id="d0959-169">Lai saglabātu aktivitāti YouTube darbā pieņemšanas procesā, ir jānorāda YouTube video vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="d0959-169">To save the YouTube activity to the hiring process, you must specify the URL of the YouTube video.</span></span> <span data-ttu-id="d0959-170">Tāpat kā aktivitātes PowerApps gadījumā varat atļaut dalībnieku pievienošanu aktivitātei.</span><span class="sxs-lookup"><span data-stu-id="d0959-170">As for the PowerApps activity, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="d0959-171">Ja atlasāt opciju **Rādīt tikai kandidātam**, video tiek rādīts tikai kandidātam pieejamā satura ietvaros.</span><span class="sxs-lookup"><span data-stu-id="d0959-171">If you select the **Show only to candidate** option, the video is shown only as part of the candidate experience.</span></span> <span data-ttu-id="d0959-172">Tas netiek rādīts darbā pieņemšanas procesa ietvaros programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="d0959-172">It isn't shown in the hiring process in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="d0959-173">Aktivitāte YouTube ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.</span><span class="sxs-lookup"><span data-stu-id="d0959-173">The YouTube activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="web-content-activity"></a><span data-ttu-id="d0959-174">Aktivitāte Tīmekļa saturs</span><span class="sxs-lookup"><span data-stu-id="d0959-174">Web content activity</span></span>

<span data-ttu-id="d0959-175">Aktivitāte Tīmekļa saturs sniedz jums iespēju iegult darbā pieņemšanas procesā tiešsaistes saturu.</span><span class="sxs-lookup"><span data-stu-id="d0959-175">The Web content activity lets you embed online content in your hiring process.</span></span> <span data-ttu-id="d0959-176">Lai saglabātu aktivitāti Tīmekļa saturs darbā pieņemšanas procesā, ir jānorāda satura vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="d0959-176">To save the Web content activity to the hiring process, you must specify the URL of the content.</span></span> <span data-ttu-id="d0959-177">Tāpat kā aktivitāšu PowerApps un YouTube gadījumā varat atļaut dalībnieku pievienošanu aktivitātei.</span><span class="sxs-lookup"><span data-stu-id="d0959-177">As for the PowerApps and YouTube activities, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="d0959-178">Ja atlasāt opciju **Rādīt tikai kandidātam**, saturs tiek rādīts tikai kandidātam pieejamā satura ietvaros.</span><span class="sxs-lookup"><span data-stu-id="d0959-178">If you select the **Show only to candidate** option, the content is shown only as part of the candidate experience.</span></span> <span data-ttu-id="d0959-179">Tas netiek rādīts darbā pieņemšanas procesa ietvaros programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="d0959-179">It isn't shown in the hiring process in Attract.</span></span> <span data-ttu-id="d0959-180">Varat atlasīt rādītā satura izmēru.</span><span class="sxs-lookup"><span data-stu-id="d0959-180">You can select the size of the content that is shown.</span></span>

> [!NOTE]
> <span data-ttu-id="d0959-181">Aktivitāte Tīmekļa aktivitāte ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums</span><span class="sxs-lookup"><span data-stu-id="d0959-181">The Web content activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="microsoft-forms-activity"></a><span data-ttu-id="d0959-182">Aktivitāte Microsoft Forms</span><span class="sxs-lookup"><span data-stu-id="d0959-182">Microsoft Forms activity</span></span>

<span data-ttu-id="d0959-183">Aktivitāte Microsoft Forms sniedz jums iespēju iegult darbā pieņemšanas procesā Microsoft Forms veidlapu.</span><span class="sxs-lookup"><span data-stu-id="d0959-183">The Microsoft Forms activity lets you embed a Microsoft Forms form in your hiring process.</span></span> <span data-ttu-id="d0959-184">Microsoft Forms sniedz jums iespēju izveidot testus, aptaujas un balsojumus.</span><span class="sxs-lookup"><span data-stu-id="d0959-184">Microsoft Forms lets you create quizzes, surveys, and polls.</span></span> <span data-ttu-id="d0959-185">Lai saglabātu aktivitāti Microsoft Forms darbā pieņemšanas procesā, ir jānorāda veidlapas vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="d0959-185">To save the Microsoft Forms activity to the hiring process, you must specify of the URL of the form.</span></span> <span data-ttu-id="d0959-186">Tāpat kā aktivitāšu PowerApps un YouTube un Tīmekļa saturs gadījumā varat atļaut dalībnieku pievienošanu aktivitātei.</span><span class="sxs-lookup"><span data-stu-id="d0959-186">As for the PowerApps, YouTube, and Web content activities, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="d0959-187">Ja atlasāt opciju **Rādīt tikai kandidātam**, veidlapa tiek rādīta tikai kandidātam pieejamā satura ietvaros.</span><span class="sxs-lookup"><span data-stu-id="d0959-187">If you select the **Show only to candidate** option, the form is shown only as part of the candidate experience.</span></span> <span data-ttu-id="d0959-188">Tas netiek rādīts darbā pieņemšanas procesa ietvaros programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="d0959-188">It isn't shown in the hiring process in Attract.</span></span>

<span data-ttu-id="d0959-189">Autori var mainīt Microsoft Forms iestatījumus, lai atļautu savu aptauju vai testu izpildīt lietotājiem ārpus savas organizācijas.</span><span class="sxs-lookup"><span data-stu-id="d0959-189">In Microsoft Forms, authors can change their settings to let users outside their organization respond to their survey or quiz.</span></span> <span data-ttu-id="d0959-190">Šādā gadījumā lietotāji iesniedz atbildes anonīmi.</span><span class="sxs-lookup"><span data-stu-id="d0959-190">In this case, users submit responses anonymously.</span></span> <span data-ttu-id="d0959-191">Ja vēlaties redzēt, kas ir izpildījuši jūsu aptauju vai testu, varat pieprasīt, lai respondenti aptaujas vai testa ietvaros ievadītu savu vārdu.</span><span class="sxs-lookup"><span data-stu-id="d0959-191">If you want to see who has filled out your survey or quiz, you can require that respondents enter their names as part of the survey or quiz.</span></span>

> [!NOTE]
> <span data-ttu-id="d0959-192">Aktivitāte Microsoft Forms ir pieejama tikai tad, ja jums ir visaptverošais darbā pieņemšanas papildinājums.</span><span class="sxs-lookup"><span data-stu-id="d0959-192">The Microsoft Forms activity is available only with the Comprehensive hiring add-on.</span></span>
