---
title: Personāla atlases kandidāti
description: Šajā tēmā ir parādīts, kā pieņemt kandidātus darbā risinājumā Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 529f419a4e3e4e8807c6938fd2425ae01ce282f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051813"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="919aa-103">Personāla atlases kandidāti</span><span class="sxs-lookup"><span data-stu-id="919aa-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="919aa-104">Dynamics 365 Human Resources palīdz pārvaldīt personāla atlases pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="919aa-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="919aa-105">Tas palīdz arī netraucēti pāriet no kandidātiem uz darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="919aa-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="919aa-106">Ja jūsu uzņēmums izmanto atsevišķu personāla atlases programmu, personāla atlases process var ietvert šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="919aa-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="919aa-107">Ievadiet darbinieku atlases pieprasījumu Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="919aa-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="919aa-108">Saņemt kandidātu nosūtījumus Personāla vadībā no personāla atlases programmas.</span><span class="sxs-lookup"><span data-stu-id="919aa-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="919aa-109">Pabeigt kandidātu apstiprināšanas procesu Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="919aa-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="919aa-110">Ja neizmantojat atsevišķu personāla atlases programmu, varat arī manuāli pārvaldīt kandidātus Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="919aa-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="919aa-111">Ja jūs esat administrators vai izstrādātājs un vēlaties integrēt Personāla vadību, izmantojot trešās puses personāla atlases programmu, skatiet [Konfigurēt Dataverse integrāciju](hr-admin-integration-common-data-service.md) un [Konfigurēt Dataverse virtuālās tabulas](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="919aa-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="919aa-112">Varat arī atrast darbā pieņemšanas integrācijas programmas [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="919aa-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="919aa-113">Lai izmēģinātu mūsu priekšskatījuma līdzekli integrēšanai ar LinkedIn Talent Hub, skatiet sadaļu [Integrēt ar LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="919aa-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="919aa-114">Iespējot personāla atlases pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="919aa-114">Enable recruiting requests</span></span>

<span data-ttu-id="919aa-115">Ja vēlaties iesniegt darbā pieņemšanas pieprasījumus Personāla vadībā, vispirms ir jāaktivizē funkcionalitāte **Personāla vadības kopīgajos parametros**.</span><span class="sxs-lookup"><span data-stu-id="919aa-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="919aa-116">Darbvietā **Personāla vadība** atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="919aa-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="919aa-117">Sadaļā **Iestatījumi** atlasiet **Personāla vadības kopīgotie parametri**.</span><span class="sxs-lookup"><span data-stu-id="919aa-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="919aa-118">Cilnē **Pieņemšana darbā** sadaļā **Personāla atlase** iestatiet **Iespējot personāla atlases pieprasījumus** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="919aa-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="919aa-119">Pievienot personāla atlases pieprasījuma vietu</span><span class="sxs-lookup"><span data-stu-id="919aa-119">Add a recruiting request location</span></span>

<span data-ttu-id="919aa-120">Ja jūsu uzņēmuma ir vairākas atrašanās vietas, varat pievienot tās, lai pieprasītāji varētu izvēlēties vietu, kur jaunais darbinieks strādās.</span><span class="sxs-lookup"><span data-stu-id="919aa-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="919aa-121">Atrašanās vieta tiks iekļauta darba sludinājumā.</span><span class="sxs-lookup"><span data-stu-id="919aa-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="919aa-122">Meklēšanas joslā ievadiet **personāla atlases pieprasījuma vietu**.</span><span class="sxs-lookup"><span data-stu-id="919aa-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="919aa-123">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="919aa-123">Select **New**.</span></span>

3. <span data-ttu-id="919aa-124">Laukā **Personāla atlases pieprasījuma vieta** ievadiet atrašanās vietas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="919aa-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Pievienot personāla atlases pieprasījuma vietu](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="919aa-126">Laukā **Apraksts** ievadiet atrašanās vietas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="919aa-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="919aa-127">Sadaļā **Atrašanās vieta** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="919aa-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="919aa-128">Ja parādās uznirstošais logs **Jaunā adrese**, ievadiet atrašanās vietas adresi.</span><span class="sxs-lookup"><span data-stu-id="919aa-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Ievadiet adresi](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="919aa-130">Sadaļā **Kontaktinformācija** ievadiet atrašanās vietas kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="919aa-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="919aa-131">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="919aa-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="919aa-132">Pievienot personāla atlases pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="919aa-132">Add a recruiting request</span></span>

<span data-ttu-id="919aa-133">Vadītāji var iesniegt personāla atlases pieprasījumus Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="919aa-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="919aa-134">Ja izmantojat atsevišķu personāla atlases programmu, pabeidzot šos soļus, tiks nosūtīts personāla atlases pieprasījums un sāksies personāla atlases process šajā lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="919aa-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="919aa-135">Pretējā gadījumā veiciet šo procedūru, lai sāktu darbplūsmu savam iekšējam personāla atlases procesam.</span><span class="sxs-lookup"><span data-stu-id="919aa-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="919aa-136">Atlasiet **Darbinieku pašapkalpošanās pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="919aa-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="919aa-137">Atlasiet cilni **Mana komanda**.</span><span class="sxs-lookup"><span data-stu-id="919aa-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="919aa-138">Atlasiet  **Pieprasījums, lai pieņemtu darbā**.</span><span class="sxs-lookup"><span data-stu-id="919aa-138">Select  **Request to recruit**.</span></span>

   ![Sākt personāla atlases pieprasījumu](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="919aa-140">Aizpildiet laukus **Apraksts**, **Darbs** un **Plānotais sākuma datums**.</span><span class="sxs-lookup"><span data-stu-id="919aa-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Pabeigt personāla atlases pieprasījumu](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="919aa-142">Atlasiet **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="919aa-142">Select **Continue**.</span></span> <span data-ttu-id="919aa-143">Tiek parādīts jūsu pozīcijas personāla atlases pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="919aa-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="919aa-144">Sadaļā **Vispārīgi** atlasiet rekrutētāju no **Rekrutētāju** nolaižamā saraksta un pēc tam atlasiet atrašanās vietu **Personāla atlases pieprasījuma vietas** nolaižamajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="919aa-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="919aa-145">Sadaļā **Darbs** mainiet nepieciešamo informāciju un pēc tam atlasiet **Izveidot detalizētu informāciju no darba**.</span><span class="sxs-lookup"><span data-stu-id="919aa-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Izveidot detalizētu informāciju no darba](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="919aa-147">Pārējā informācija jūsu ievadītajam darbam atlases pieprasījumā tiks aizpildīta ar noklusējuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="919aa-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="919aa-148">Sadaļā **Ārējais apraksts** ievadiet ārēju darba aprakstu.</span><span class="sxs-lookup"><span data-stu-id="919aa-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="919aa-149">Sadaļā **Amati** atlasiet **Pievienot** un pēc tam atlasiet amatu šim personāla atlases pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="919aa-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Pievienot amatu](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="919aa-151">Sadaļā **Prasmes** atlasiet **Pievienot** un pēc tam atlasiet prasmi.</span><span class="sxs-lookup"><span data-stu-id="919aa-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="919aa-152">Sadaļā **Izglītības prasības** atlasiet **Pievienot** un pēc tam atlasiet vērtības no **Izglītības** un **Izglītības līmeņa** nolaižamajiem logiem.</span><span class="sxs-lookup"><span data-stu-id="919aa-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Pievienot izglītības prasības](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="919aa-154">Sadaļā **Komentārs** pievienojiet komentārus pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="919aa-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="919aa-155">Sadaļā **Kompensācija** atlasiet līmeni no **Līmeņa** nolaižamā saraksta un pēc tam pielāgojiet **Zemu slieksni**, **Kontrolpunktu** un **Augstu slieksni**.</span><span class="sxs-lookup"><span data-stu-id="919aa-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="919aa-156">Kad jūsu personāla atlases pieprasījums ir pabeigts un jūs esat gatavs sākt personāla atlases procesu, izvēlņu joslā atlasiet **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="919aa-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Aktivizēt personāla atlases pieprasījumu](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="919aa-158">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="919aa-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="919aa-159">Skatīt un rediģēt atlases pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="919aa-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="919aa-160">Ja esat vadītājs un vēlaties skatīt savus pieprasījumus:</span><span class="sxs-lookup"><span data-stu-id="919aa-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="919aa-161">Atlasiet **Darbinieku pašapkalpošanās pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="919aa-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="919aa-162">Atlasiet cilni **Mana komanda**.</span><span class="sxs-lookup"><span data-stu-id="919aa-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="919aa-163">Sadaļā **Manas darba grupas informācija** atlasiet cilni **Personāla atlases pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="919aa-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Atlasiet cilni Personāla atlases pieprasījumi](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="919aa-165">Lai apskatītu vai rediģētu personāla atlases pieprasījumu, atlasiet to režģī.</span><span class="sxs-lookup"><span data-stu-id="919aa-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="919aa-166">Ja esat HR pro un vēlaties skatīt visus personāla atlases pieprasījumus:</span><span class="sxs-lookup"><span data-stu-id="919aa-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="919aa-167">Atlasiet **Personāla pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="919aa-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="919aa-168">Atlasiet **Personāla atlases pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="919aa-168">Select **Recruiting requests**.</span></span>

   ![Skatīt personāla atlases pieprasījumus Personāla pārvaldībā](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="919aa-170">Lai apskatītu vai rediģētu personāla atlases pieprasījumu, atlasiet to režģī.</span><span class="sxs-lookup"><span data-stu-id="919aa-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="919aa-171">Pievienot vai rediģēt kandidāta profilu</span><span class="sxs-lookup"><span data-stu-id="919aa-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="919aa-172">Ja jūsu uzņēmums ir integrēts ar citu programmu, lai pārvaldītu personāla atlases pieprasījumus, personāla atlases pieprasījumi tiek pārsūtīti uz šo programmu.</span><span class="sxs-lookup"><span data-stu-id="919aa-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="919aa-173">Pēc tam personāla atlases programma nosūta informāciju par kandidātu uz Personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="919aa-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="919aa-174">Pretējā gadījumā varat sekot saviem iekšējiem personāla atlases procesiem un ievadīt informāciju par kandidātu manuāli.</span><span class="sxs-lookup"><span data-stu-id="919aa-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="919aa-175">Atlasiet **Personāla pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="919aa-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="919aa-176">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="919aa-176">Select **Links**.</span></span>

3. <span data-ttu-id="919aa-177">Sadaļā **Personāla atlase** atlasiet **Kandidāti**.</span><span class="sxs-lookup"><span data-stu-id="919aa-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Skatīt kandidātus](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="919aa-179">Lai pievienotu kandidātu, atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="919aa-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="919aa-180">Lai rediģētu esošu kandidātu, izvēlieties kandidātu no saraksta un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="919aa-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="919aa-181">Tiek parādīts kandidāta profils.</span><span class="sxs-lookup"><span data-stu-id="919aa-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="919aa-182">Sadaļā **Kandidāta kopsavilkums** ievadiet vai rediģējiet informāciju par kandidātu pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="919aa-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="919aa-183">Sadaļā **Personāla atlases pieprasījums** atlasiet atlases pieprasījumu, lai saistītu kandidātu.</span><span class="sxs-lookup"><span data-stu-id="919aa-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="919aa-184">Pēc tam pabeidziet **Aprēķināto sākuma datumu**, **Pieņemšanas vadītāju**, **Amatu** un **Apraksta laukus**.</span><span class="sxs-lookup"><span data-stu-id="919aa-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Saistīt ar personāla atlases pieprasījumu](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="919aa-186">Aizpildiet visu informāciju, ko vēlaties iekļaut kandidāta ierakstā, sekojošajās jomās:</span><span class="sxs-lookup"><span data-stu-id="919aa-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="919aa-187">**Komentāri**</span><span class="sxs-lookup"><span data-stu-id="919aa-187">**Comments**</span></span>
   - <span data-ttu-id="919aa-188">**Profesionālā pieredze**</span><span class="sxs-lookup"><span data-stu-id="919aa-188">**Professional experience**</span></span>
   - <span data-ttu-id="919aa-189">**Kontaktinformācija**</span><span class="sxs-lookup"><span data-stu-id="919aa-189">**Contact information**</span></span>
   - <span data-ttu-id="919aa-190">**Izglītība**</span><span class="sxs-lookup"><span data-stu-id="919aa-190">**Education**</span></span>
   - <span data-ttu-id="919aa-191">**Prasmes**</span><span class="sxs-lookup"><span data-stu-id="919aa-191">**Skills**</span></span>
   - <span data-ttu-id="919aa-192">**Sertifikāti**</span><span class="sxs-lookup"><span data-stu-id="919aa-192">**Certificates**</span></span>
   - <span data-ttu-id="919aa-193">**Izvērtēšana**</span><span class="sxs-lookup"><span data-stu-id="919aa-193">**Screenings**</span></span>

8. <span data-ttu-id="919aa-194">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="919aa-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="919aa-195">Pieņemt darbā kandidātu</span><span class="sxs-lookup"><span data-stu-id="919aa-195">Hire a candidate</span></span>

<span data-ttu-id="919aa-196">Kad esat gatavs pieņemt darbā kandidātu, ievērojiet šo procedūru, lai nomainītu kandidātu uz darbinieku.</span><span class="sxs-lookup"><span data-stu-id="919aa-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="919aa-197">Kandidāta veidlapā atlasiet **Pieņemt darbā**.</span><span class="sxs-lookup"><span data-stu-id="919aa-197">On the candidate form, select **Hire**.</span></span>

   ![Pieņemt darbā kandidātu](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="919aa-199">Aizpildiet visus laukus veidlapā **Pieņemt darbā jaunu darbinieku**, sadaļā **Detalizēti** .</span><span class="sxs-lookup"><span data-stu-id="919aa-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Ievadīt jaunā darbinieka informāciju](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="919aa-201">Sadaļā **Amata detaļas** pēc nepieciešamības pārbaudiet un mainiet informāciju.</span><span class="sxs-lookup"><span data-stu-id="919aa-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="919aa-202">Sadaļā **Iekārtošanas kontrolsaraksti** atlasiet šim darbiniekam atbilstīgos iekārtošanas kontrolsarakstus.</span><span class="sxs-lookup"><span data-stu-id="919aa-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="919aa-203">Atlasiet **Turpināt**, lai izveidotu darbinieka ierakstu.</span><span class="sxs-lookup"><span data-stu-id="919aa-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="919aa-204">Atkarībā no jūsu organizācijas darbplūsmām kandidāta ieraksts var iziet caur papildu apstiprināšanas soļiem, pirms kļūst par darbinieka ierakstu.</span><span class="sxs-lookup"><span data-stu-id="919aa-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="919aa-205">Nolemt nepieņemt darbā kandidātu</span><span class="sxs-lookup"><span data-stu-id="919aa-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="919aa-206">Ja izlemjat nepieņemt kandidātu, sekojiet šai procedūrai, lai noņemtu to no pārbaudes procesa.</span><span class="sxs-lookup"><span data-stu-id="919aa-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="919aa-207">Kandidāta veidlapā atlasiet **Nepieņemt darbā**.</span><span class="sxs-lookup"><span data-stu-id="919aa-207">On the candidate form, select **Do not hire**.</span></span>

   ![Nepieņemt darbā kandidātu](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="919aa-209">Atlasiet **Pamatojuma kodu** un iekļaujiet komentārus.</span><span class="sxs-lookup"><span data-stu-id="919aa-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="919aa-210">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="919aa-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="919aa-211">Noraidīt kandidātu</span><span class="sxs-lookup"><span data-stu-id="919aa-211">Dismiss a candidate</span></span>

<span data-ttu-id="919aa-212">Ja nepieciešams, varat noraidīt kandidātu pēc pieņemšanas darbā.</span><span class="sxs-lookup"><span data-stu-id="919aa-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="919aa-213">Piemēram, kandidāts var noraidīt jūsu piedāvājumu vai neierasties darbā pirmajā dienā.</span><span class="sxs-lookup"><span data-stu-id="919aa-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="919aa-214">Kandidāta veidlapā atlasiet **Noraidīt kandidātu**.</span><span class="sxs-lookup"><span data-stu-id="919aa-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Noraidīt kandidātu](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="919aa-216">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="919aa-216">See also</span></span>

[<span data-ttu-id="919aa-217">Pakalpojuma Dataverse virtuālo tabulu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="919aa-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="919aa-218">Darbaspēka pārvaldība</span><span class="sxs-lookup"><span data-stu-id="919aa-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="919aa-219">Darba komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="919aa-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
