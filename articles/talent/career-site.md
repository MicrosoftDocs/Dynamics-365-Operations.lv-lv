---
title: "Karjeras vietnes funkcionalitāte programmā Attract"
description: "Šajā rakstā ir sniegts apskats par kandidātu karjeras vietnes funkcionalitāti programmatūrā Microsoft Dynamics 365 for Talent - Attract. Tajā arī ir paskaidrots, kā iestatīt šo funkcionalitāti."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: lv-lv
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="c3d42-104">Karjeras vietnes funkcionalitāte programmā Attract</span><span class="sxs-lookup"><span data-stu-id="c3d42-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3d42-105">Šajā rakstā ir sniegts apskats par kandidātu karjeras vietnes funkcionalitāti programmatūrā Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="c3d42-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="c3d42-106">Tajā arī ir paskaidrots, kā iestatīt šo funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="c3d42-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="c3d42-107">Pārskats</span><span class="sxs-lookup"><span data-stu-id="c3d42-107">Overview</span></span>

<span data-ttu-id="c3d42-108">Attract nodrošina vienu karjeras vietni katrai nomnieka videi.</span><span class="sxs-lookup"><span data-stu-id="c3d42-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="c3d42-109">Piemēram, ja organizācijai ir izstrādes vide un testēšanas vide, viena karjeras vietne ir paredzēta izstrādes videi un otra karjeras vietne ir paredzēta testēšanas videi.</span><span class="sxs-lookup"><span data-stu-id="c3d42-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="c3d42-110">Katra karjeras vietne ir **pilnībā izolēta**, un tām ir savs autentifikācijas mehānisms.</span><span class="sxs-lookup"><span data-stu-id="c3d42-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="c3d42-111">Darbi un kandidātu profili netiek kopīgoti starp karjeras vietnēm.</span><span class="sxs-lookup"><span data-stu-id="c3d42-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="c3d42-112">Pēc noklusējuma karjeras vietne ir publiska.</span><span class="sxs-lookup"><span data-stu-id="c3d42-112">By default, the career site is public.</span></span> <span data-ttu-id="c3d42-113">Tāpēc kandidāti nepierakstoties var skatīt visus darbus, kas atzīmēti kā ārēji.</span><span class="sxs-lookup"><span data-stu-id="c3d42-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="c3d42-114">Tomēr, lai veiktu pārējās darbības, kandidātiem ir jāpierakstās.</span><span class="sxs-lookup"><span data-stu-id="c3d42-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="c3d42-115">Karjeras vietnes pārvaldība</span><span class="sxs-lookup"><span data-stu-id="c3d42-115">Career site management</span></span>

<span data-ttu-id="c3d42-116">Iestatījumi kontrolē šādus karjeras vietnes vienumus.</span><span class="sxs-lookup"><span data-stu-id="c3d42-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="c3d42-117">**Organizācijas nosaukums:** organizācijas nosaukums parādās navigācijas joslā karjeras vietnes augšdaļā.</span><span class="sxs-lookup"><span data-stu-id="c3d42-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="c3d42-118">Atlasot organizācijas nosaukumu, kandidāti pāriet uz lapu, kurā norādīti visi atvērtie darbi.</span><span class="sxs-lookup"><span data-stu-id="c3d42-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="c3d42-119">**Organizācijas logotips:** organizācijas logotipa attēls parādās karjeras vietnes augšējā kreisajā stūrī.</span><span class="sxs-lookup"><span data-stu-id="c3d42-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="c3d42-120">Atlasot organizācijas logotipa attēlu, kandidāti pāriet uz lapu, kurā norādīti visi atvērtie darbi.</span><span class="sxs-lookup"><span data-stu-id="c3d42-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="c3d42-121">Lai iestatītu vērtības tādiem vienumiem kā organizācijas nosaukums un logotips, pierakstieties programmā Attract kā administrators, izvēlnē **Iestatījumi** (zobrata simbols) atlasiet vienumu **Administrēšanas centrs** un pēc tam atlasiet cilni **Uzņēmuma informācija**.</span><span class="sxs-lookup"><span data-stu-id="c3d42-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="c3d42-122">Logotipa attēlam, kas parādās karjeras vietnē, ir fiksēts augstums 20 pikseļi (px).</span><span class="sxs-lookup"><span data-stu-id="c3d42-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="c3d42-123">Attēls, ko pievienojat administrēšanas centrā, tiek mērogots atbilstoši vajadzīgajam izmēram.</span><span class="sxs-lookup"><span data-stu-id="c3d42-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="c3d42-124">Tāpēc atkarībā no attēla platums var mainīties.</span><span class="sxs-lookup"><span data-stu-id="c3d42-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="c3d42-125">Karjeras vietnes vietrādis URL</span><span class="sxs-lookup"><span data-stu-id="c3d42-125">Career site URL</span></span>

<span data-ttu-id="c3d42-126">Kad pirmo reizi [publicējat ārējo darbu](./Creating-jobs-Attract.md#postings), jūs varat kopēt saiti **Pieteikties** no programmas Attract.</span><span class="sxs-lookup"><span data-stu-id="c3d42-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="c3d42-127">Šīs saites vietrādis URL būs šādā formātā: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="c3d42-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="c3d42-128">Karjeras vietnes vietrādis URL ir vietrāža URL **Pieteikties** apakšvirkne.</span><span class="sxs-lookup"><span data-stu-id="c3d42-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="c3d42-129">To veido visi elementi līdz uzņēmuma nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="c3d42-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="c3d42-130">Tāpēc iepriekšējam vietrādim URL **Pieteikties** karjeras vietnes vietrādis URL ir `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="c3d42-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="c3d42-131">Autentifikācija opcijas</span><span class="sxs-lookup"><span data-stu-id="c3d42-131">Authentication options</span></span>

<span data-ttu-id="c3d42-132">Kandidātiem ir pieejamas šādas pierakstīšanās opcijas Attract karjeras vietnē.</span><span class="sxs-lookup"><span data-stu-id="c3d42-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="c3d42-133">Personiskais konts:</span><span class="sxs-lookup"><span data-stu-id="c3d42-133">Personal account:</span></span>

    - <span data-ttu-id="c3d42-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="c3d42-134">LinkedIn</span></span>
    - <span data-ttu-id="c3d42-135">Microsoft </span><span class="sxs-lookup"><span data-stu-id="c3d42-135">Microsoft</span></span>
    - <span data-ttu-id="c3d42-136">Google</span><span class="sxs-lookup"><span data-stu-id="c3d42-136">Google</span></span>
    - <span data-ttu-id="c3d42-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="c3d42-137">Facebook</span></span>

- <span data-ttu-id="c3d42-138">Darba vai mācību konts:</span><span class="sxs-lookup"><span data-stu-id="c3d42-138">Work or school account:</span></span>

    - <span data-ttu-id="c3d42-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="c3d42-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="c3d42-140">Azure AD pierakstīšanās ir paredzēta tikai iekšējiem kandidātiem.</span><span class="sxs-lookup"><span data-stu-id="c3d42-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="c3d42-141">Tāpēc to var lietot tikai iekšējie kandidāti, kuri izmanto attiecīgā uzņēmuma Azure AD akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="c3d42-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="c3d42-142">Piemēram, kandidāts, kas pašlaik ir Contoso Ltd darbinieks, vēlas pieteikties darbam nesaistītā uzņēmumā Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="c3d42-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="c3d42-143">Šajā gadījumā pierakstīšanās būs neveiksmīga, ja darbinieks mēģina lietot savus Azure AD akreditācijas datus no Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="c3d42-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="c3d42-144">Profila izveide un uzturēšana</span><span class="sxs-lookup"><span data-stu-id="c3d42-144">Create and maintain a profile</span></span>

<span data-ttu-id="c3d42-145">Pēc kandidātu pierakstīšanās karjeras vietnē viņi var atlasīt **Mans profils** navigācijas joslā lapas augšdaļā, lai izveidotu un uzturētu savu profilu.</span><span class="sxs-lookup"><span data-stu-id="c3d42-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="c3d42-146">Profils ietver personisko informāciju, informāciju par darba pieredzi, izglītības informāciju, dokumentus, saites un informāciju par prasmju kopām.</span><span class="sxs-lookup"><span data-stu-id="c3d42-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="c3d42-147">Pēc tam, kad profils ir izveidots, to var izmantot, lai pieteiktos kandidātu interesējošiem darbiem.</span><span class="sxs-lookup"><span data-stu-id="c3d42-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="c3d42-148">Profili arī palīdz programmai Attract ieteikt kandidātiem piemērotus darbus.</span><span class="sxs-lookup"><span data-stu-id="c3d42-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="c3d42-149">Piemērota darba atrašana</span><span class="sxs-lookup"><span data-stu-id="c3d42-149">Find the right job</span></span>

<span data-ttu-id="c3d42-150">Darbu saraksta lapā kandidāti var meklēt konkrētu darbu, ievadot meklējamos vārdus.</span><span class="sxs-lookup"><span data-stu-id="c3d42-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="c3d42-151">Meklēšanas funkcionalitāte veic meklējamo vārdu meklēšanu amatu nosaukumos un darba aprakstos un rezultātos parāda atbilstīgos darbus.</span><span class="sxs-lookup"><span data-stu-id="c3d42-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="c3d42-152">Kandidāti var filtrēt rezultātus jebkurā laikā, pamatojoties uz darba atrašanās vietu vai darba funkciju.</span><span class="sxs-lookup"><span data-stu-id="c3d42-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="c3d42-153">Kandidāti var apskatīt arī ieteikto darbu kopu karjeras vietnē.</span><span class="sxs-lookup"><span data-stu-id="c3d42-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="c3d42-154">Kandidātam ieteiktie darbi balstās uz kandidāta iepriekšējiem pieteikumiem, profilu un CV.</span><span class="sxs-lookup"><span data-stu-id="c3d42-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="c3d42-155">Darba ieteikumi tiek rādīti tikai tad, ja karjeras vietnē ir publicēti vismaz 10 darbi un ja kandidāts ir aizpildījis savu profilu.</span><span class="sxs-lookup"><span data-stu-id="c3d42-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="c3d42-156">Pieteikšanās darbiem</span><span class="sxs-lookup"><span data-stu-id="c3d42-156">Apply for jobs</span></span>

<span data-ttu-id="c3d42-157">Pēc tam, kad kandidāti ir atraduši piemērotu darbu, viņi var pieteikties, izmantojot pogu **Pieteikties** darba informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="c3d42-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="c3d42-158">Šajā brīdī kandidāti var izveidot jaunu profilu vai pārskatīt informāciju savā esošajā profilā.</span><span class="sxs-lookup"><span data-stu-id="c3d42-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="c3d42-159">Ja nepieciešams, kandidāti var arī augšupielādēt CV un pēc tam iesniegt darba pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="c3d42-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="c3d42-160">Pieteikuma statusa pārbaude</span><span class="sxs-lookup"><span data-stu-id="c3d42-160">Check application status</span></span>

<span data-ttu-id="c3d42-161">Pēc tam, kad kandidāti piesakās vienam vai vairākiem darbiem, viņi var atlasīt vienumu **Pieteikumi** navigācijas joslā lapas augšdaļā, lai skatītu savus atvērtos un slēgtos pieteikumus.</span><span class="sxs-lookup"><span data-stu-id="c3d42-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="c3d42-162">Kad kandidāti atver kādu no saviem pieteikumiem, viņi redz pašreizējo posmu un veicamās darbības.</span><span class="sxs-lookup"><span data-stu-id="c3d42-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="c3d42-163">Piemēram, ja kandidātam ir jānorāda iespējamie datumi intervijai klātienē, lapā ir parādītas pieejamās iespējas.</span><span class="sxs-lookup"><span data-stu-id="c3d42-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="c3d42-164">Iekšējie darbi</span><span class="sxs-lookup"><span data-stu-id="c3d42-164">Internal jobs</span></span>

<span data-ttu-id="c3d42-165">Pašlaik, darbi, kas ir atzīmēti kā iekšējie darbi un publicēti Attract karjeras vietnē, netiek parādīti karjeras vietnē.</span><span class="sxs-lookup"><span data-stu-id="c3d42-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="c3d42-166">Tie ir pieejami, tikai izmantojot tiešo vietrādi URL **Pieteikties**, ko var kopēt no programmas Attract.</span><span class="sxs-lookup"><span data-stu-id="c3d42-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

