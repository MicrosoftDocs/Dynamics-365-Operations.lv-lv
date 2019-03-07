---
title: Salāgojiet darbaspēka prasmes ar biznesa vajadzībām
description: Varat izsekot prasmes, kas piemīt darbiniekiem, kandidātiem vai kontaktpersonām vai kuriem tādām vajadzētu būt darbinieku, kandidātu vai kontaktpersonu lomas efektīvai izpildei. Varat arī norādīt prasmes, kas ir nepieciešamas konkrētam darbam.
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 0b86a8d134ef553db6719f4cefb02e4acfc00ae5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305295"
---
# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="b96cd-104">Salāgojiet darbaspēka prasmes ar biznesa vajadzībām</span><span class="sxs-lookup"><span data-stu-id="b96cd-104">Align workforce skills with business needs</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b96cd-105">Varat izsekot prasmes, kas piemīt darbiniekiem, kandidātiem vai kontaktpersonām vai kuriem tādām vajadzētu būt darbinieku, kandidātu vai kontaktpersonu lomas efektīvai izpildei.</span><span class="sxs-lookup"><span data-stu-id="b96cd-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="b96cd-106">Varat arī norādīt prasmes, kas ir nepieciešamas konkrētam darbam.</span><span class="sxs-lookup"><span data-stu-id="b96cd-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="b96cd-107">Izsekojamo prasmju piemēri ietver:</span><span class="sxs-lookup"><span data-stu-id="b96cd-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="b96cd-108">Supervizora — spēja uzraudzīt citu darbu.</span><span class="sxs-lookup"><span data-stu-id="b96cd-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="b96cd-109">Vadības — spēja vadīt darbiniekus un uzņēmuma domēnus.</span><span class="sxs-lookup"><span data-stu-id="b96cd-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="b96cd-110">Plānošanas — spēja raudzīties nākotnē, formulēt redzējumus un īstenot tos dzīvē.</span><span class="sxs-lookup"><span data-stu-id="b96cd-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="b96cd-111">HTML — spēja rakstīt HTML kodu.</span><span class="sxs-lookup"><span data-stu-id="b96cd-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="b96cd-112">Lai personai vai darbam varētu piešķirt kādu prasmi, izveidot prasmju kartēšanas meklēšanu vai prasmju profilu, par šīm prasmēm ir jāievada informācija lapā **Prasmes**.</span><span class="sxs-lookup"><span data-stu-id="b96cd-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="b96cd-113">Katrai prasmei varat atlasīt prasmju tipu un vērtēšanas modeli.</span><span class="sxs-lookup"><span data-stu-id="b96cd-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="b96cd-114">Vērtēšanas modeļi</span><span class="sxs-lookup"><span data-stu-id="b96cd-114">Rating models</span></span>
<span data-ttu-id="b96cd-115">Vērtēšanas modeļi palīdz novērtēt personas faktisko prasmju līmeni, to prasmju līmeni, ko šai personai būtu jācenšas sasniegt, vai prasmju līmeni, kas ir nepieciešams darbam.</span><span class="sxs-lookup"><span data-stu-id="b96cd-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="b96cd-116">Vērtējuma modelim var ievadīt ne vairāk kā 10 līmeņus.</span><span class="sxs-lookup"><span data-stu-id="b96cd-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="b96cd-117">Katram līmenim vērtēšanas modelī tiek piešķirts koeficients.</span><span class="sxs-lookup"><span data-stu-id="b96cd-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="b96cd-118">Koeficienta vērtība tiks izmantota, lai normalizētu rādītājus prasmēm, kas izmanto dažādu vērtēšanas modeļus.</span><span class="sxs-lookup"><span data-stu-id="b96cd-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="b96cd-119">Koeficientam ir jābūt skaitlim no 0 līdz 9, un katram līmenim ir nepieciešams unikāls koeficients.</span><span class="sxs-lookup"><span data-stu-id="b96cd-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="b96cd-120">Līmeņiem ar augstākām koeficienta vērtībām ir lielāka nozīme vērtēšanas modelī.</span><span class="sxs-lookup"><span data-stu-id="b96cd-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="b96cd-121">Darba prasmju norādīšana</span><span class="sxs-lookup"><span data-stu-id="b96cd-121">Specify job skills</span></span>
<span data-ttu-id="b96cd-122">Kad ievadāt informāciju par darbu, varat norādīt prasmes, kas personai ir nepieciešamas, lai varētu veikt attiecīgo darbu.</span><span class="sxs-lookup"><span data-stu-id="b96cd-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="b96cd-123">Turklāt varat norādīt vēlamo līmeni katrai prasmei, kā arī prasmes svarīguma līmeni.</span><span class="sxs-lookup"><span data-stu-id="b96cd-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="b96cd-124">Dažādos amatos vienādām prasmēm var būt nepieciešami dažādi nozīmīguma līmeņi.</span><span class="sxs-lookup"><span data-stu-id="b96cd-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="b96cd-125">Prasmju ievadīšana darbiniekiem, kandidātiem vai kontaktpersonām</span><span class="sxs-lookup"><span data-stu-id="b96cd-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="b96cd-126">Darbiniekiem, kandidātiem vai kontaktpersonām varat ievadīt mērķa prasmes vai faktiskās prasmes.</span><span class="sxs-lookup"><span data-stu-id="b96cd-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="b96cd-127">Mērķa prasme ir prasme, ko persona plāno sasniegt.</span><span class="sxs-lookup"><span data-stu-id="b96cd-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="b96cd-128">Faktiskā prasme ir prasme, kas personai piemīt pašlaik.</span><span class="sxs-lookup"><span data-stu-id="b96cd-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="b96cd-129">Prasmju kartēšana un prasmju kartēšanas profili</span><span class="sxs-lookup"><span data-stu-id="b96cd-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="b96cd-130">Varat izveidot prasmju kartēšanas meklēšanu, lai atrastu darbinieku, kandidātu vai kontaktpersonu, kas ir kvalificēta veikt noteikta veida uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="b96cd-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="b96cd-131">Veicot prasmju kartēšanas meklēšanu, kā kritēriji tiek izmantotas prasmes, izglītība, sertifikāti, atbildīgie amati un projektu pieredze un tiek atgriezti ievadītajiem kritērijiem atbilstošie rezultāti.</span><span class="sxs-lookup"><span data-stu-id="b96cd-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return results that match the criteria entered.</span></span>  <span data-ttu-id="b96cd-132">Piemēram, var būt lietderīgi zināt, kuri no darbiniekiem jūsu organizācijā ir ieguvuši CPA.</span><span class="sxs-lookup"><span data-stu-id="b96cd-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="b96cd-133">Prasmju kartēšanas profili ļauj atrast pašreizējos darbiniekus vai kandidātus ar kvalifikāciju, kas tieši atbilst uzņēmuma vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="b96cd-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="b96cd-134">Piemēram, varat izveidot prasmju kartēšanas profilu jūsu organizācijas vakancei.</span><span class="sxs-lookup"><span data-stu-id="b96cd-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="b96cd-135">Izveidojot profilu konkrētam darbam un kopējot prasmes, izglītību un sertifikātus no šī darba profilā, var ātri atrast darbiniekus, kandidātus un kontaktpersonas, kas atbilst vienam vai vairākiem profilā ievadītiem kritērijiem, un skatīt sarakstu ar kandidātiem, kuru prasmes visprecīzāk atbilst nepieciešamajam darbam.</span><span class="sxs-lookup"><span data-stu-id="b96cd-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

> <span data-ttu-id="b96cd-136">**Piezīme.** Prasmju kartēšanas rezultātu sarakstā var tikt parādīti vai prasmju profilā var tikt iekļauti tikai darbinieki, kandidāti un kontaktpersonas, kas ir izvēlēti iekļaušanai prasmju kartēšanas meklējumos.</span><span class="sxs-lookup"><span data-stu-id="b96cd-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="b96cd-137">Lai prasmju kartēšanas rezultātos iekļautu darbinieku, kandidātu vai kontaktpersonu, iestatiet opciju **Iekļaut prasmju kartēšanā** uz Jā šādās lapās.</span><span class="sxs-lookup"><span data-stu-id="b96cd-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>
> 
> + <span data-ttu-id="b96cd-138">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="b96cd-138">Worker</span></span>
> + <span data-ttu-id="b96cd-139">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="b96cd-139">Employee</span></span>
> + <span data-ttu-id="b96cd-140">Kandidāts</span><span class="sxs-lookup"><span data-stu-id="b96cd-140">Applicant</span></span>
> + <span data-ttu-id="b96cd-141">Kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="b96cd-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="b96cd-142">Prasmju atšķirības analīze un prasmju profila analīze</span><span class="sxs-lookup"><span data-stu-id="b96cd-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="b96cd-143">Varat izveidot prasmju profila analīzi, lai skatītu darbinieka, kandidāta vai kontaktpersonas kompetenču sarakstu no konkrēta datuma.</span><span class="sxs-lookup"><span data-stu-id="b96cd-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="b96cd-144">Varat izveidot prasmju starpības analīzi, lai salīdzinātu personas prasmes un konkrētam darbam nepieciešamās prasmes.</span><span class="sxs-lookup"><span data-stu-id="b96cd-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="additional-resources"></a><span data-ttu-id="b96cd-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b96cd-145">Additional resources</span></span>
--------

[<span data-ttu-id="b96cd-146">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="b96cd-146">Human resources</span></span>](index.md)



