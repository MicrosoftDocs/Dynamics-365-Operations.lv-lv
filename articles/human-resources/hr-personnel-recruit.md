---
title: Personāla atlases kandidāti
description: Šajā tēmā ir parādīts, kā pieņemt kandidātus darbā risinājumā Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669179"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="72111-103">Personāla atlases kandidāti</span><span class="sxs-lookup"><span data-stu-id="72111-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="72111-104">Dynamics 365 Human Resources palīdz pārvaldīt personāla atlases pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="72111-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="72111-105">Tas palīdz arī netraucēti pāriet no kandidātiem uz darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="72111-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="72111-106">Ja jūsu uzņēmums izmanto atsevišķu personāla atlases programmu, personāla atlases process var ietvert šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="72111-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="72111-107">Ievadiet darbinieku atlases pieprasījumu Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="72111-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="72111-108">Saņemt kandidātu nosūtījumus Personāla vadībā no personāla atlases programmas.</span><span class="sxs-lookup"><span data-stu-id="72111-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="72111-109">Pabeigt kandidātu apstiprināšanas procesu Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="72111-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="72111-110">Ja neizmantojat atsevišķu personāla atlases programmu, varat arī manuāli pārvaldīt kandidātus Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="72111-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="72111-111">Ja jūs esat administrators vai izstrādātājs un vēlaties integrēt Personāla vadību, izmantojot trešās puses personāla atlases programmu, skatiet [Konfigurēt Common Data Service integrāciju](hr-admin-integration-common-data-service.md) un [Konfigurēt Common Data Service virtuālos elementus](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="72111-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="72111-112">Varat arī atrast darbā pieņemšanas integrācijas programmas [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="72111-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="72111-113">Lai izmēģinātu mūsu priekšskatījuma līdzekli integrēšanai ar LinkedIn Talent Hub, skatiet sadaļu [Integrēt ar LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="72111-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="72111-114">Iespējot personāla atlases pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="72111-114">Enable recruiting requests</span></span>

<span data-ttu-id="72111-115">Ja vēlaties iesniegt darbā pieņemšanas pieprasījumus Personāla vadībā, vispirms ir jāaktivizē funkcionalitāte **Personāla vadības parametros**.</span><span class="sxs-lookup"><span data-stu-id="72111-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="72111-116">Darbvietā **Personāla vadība** atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="72111-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="72111-117">Sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="72111-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="72111-118">Cilnē **Vispārīgi** sadaļā **Personāla atlase** iestatiet **Iespējot personāla atlases pieprasījumus** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="72111-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![Iespējot personāla atlases pieprasījumus](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="72111-120">Pievienot personāla atlases pieprasījuma vietu</span><span class="sxs-lookup"><span data-stu-id="72111-120">Add a recruiting request location</span></span>

<span data-ttu-id="72111-121">Ja jūsu uzņēmuma ir vairākas atrašanās vietas, varat pievienot tās, lai pieprasītāji varētu izvēlēties vietu, kur jaunais darbinieks strādās.</span><span class="sxs-lookup"><span data-stu-id="72111-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="72111-122">Atrašanās vieta tiks iekļauta darba sludinājumā.</span><span class="sxs-lookup"><span data-stu-id="72111-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="72111-123">Meklēšanas joslā ievadiet **personāla atlases pieprasījuma vietu**.</span><span class="sxs-lookup"><span data-stu-id="72111-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="72111-124">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="72111-124">Select **New**.</span></span>

3. <span data-ttu-id="72111-125">Laukā **Personāla atlases pieprasījuma vieta** ievadiet atrašanās vietas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="72111-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Pievienot personāla atlases pieprasījuma vietu](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="72111-127">Laukā **Apraksts** ievadiet atrašanās vietas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="72111-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="72111-128">Sadaļā **Atrašanās vieta** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="72111-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="72111-129">Ja parādās uznirstošais logs **Jaunā adrese**, ievadiet atrašanās vietas adresi.</span><span class="sxs-lookup"><span data-stu-id="72111-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Ievadiet adresi](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="72111-131">Sadaļā **Kontaktinformācija** ievadiet atrašanās vietas kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="72111-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="72111-132">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="72111-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="72111-133">Pievienot personāla atlases pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="72111-133">Add a recruiting request</span></span>

<span data-ttu-id="72111-134">Vadītāji var iesniegt personāla atlases pieprasījumus Personāla vadībā.</span><span class="sxs-lookup"><span data-stu-id="72111-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="72111-135">Ja izmantojat atsevišķu personāla atlases programmu, pabeidzot šos soļus, tiks nosūtīts personāla atlases pieprasījums un sāksies personāla atlases process šajā lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="72111-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="72111-136">Pretējā gadījumā veiciet šo procedūru, lai sāktu darbplūsmu savam iekšējam personāla atlases procesam.</span><span class="sxs-lookup"><span data-stu-id="72111-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="72111-137">Atlasiet **Darbinieku pašapkalpošanās pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="72111-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="72111-138">Atlasiet cilni **Mana komanda**.</span><span class="sxs-lookup"><span data-stu-id="72111-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="72111-139">Atlasiet **Pieprasījums, lai pieņemtu darbā**.</span><span class="sxs-lookup"><span data-stu-id="72111-139">Select  **Request to recruit**.</span></span>

   ![Sākt personāla atlases pieprasījumu](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="72111-141">Aizpildiet laukus **Apraksts**, **Darbs** un **Plānotais sākuma datums**.</span><span class="sxs-lookup"><span data-stu-id="72111-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Pabeigt personāla atlases pieprasījumu](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="72111-143">Atlasiet **Turpināt**.</span><span class="sxs-lookup"><span data-stu-id="72111-143">Select **Continue**.</span></span> <span data-ttu-id="72111-144">Tiek parādīts jūsu pozīcijas personāla atlases pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="72111-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="72111-145">Sadaļā **Vispārīgi** atlasiet rekrutētāju no **Rekrutētāju** nolaižamā saraksta un pēc tam atlasiet atrašanās vietu **Personāla atlases pieprasījuma vietas** nolaižamajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="72111-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="72111-146">Sadaļā **Darbs** mainiet nepieciešamo informāciju un pēc tam atlasiet **Izveidot detalizētu informāciju no darba**.</span><span class="sxs-lookup"><span data-stu-id="72111-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Izveidot detalizētu informāciju no darba](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="72111-148">Pārējā informācija jūsu ievadītajam darbam atlases pieprasījumā tiks aizpildīta ar noklusējuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="72111-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="72111-149">Sadaļā **Ārējais apraksts** ievadiet ārēju darba aprakstu.</span><span class="sxs-lookup"><span data-stu-id="72111-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="72111-150">Sadaļā **Amati** atlasiet **Pievienot** un pēc tam atlasiet amatu šim personāla atlases pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="72111-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Pievienot amatu](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="72111-152">Sadaļā **Prasmes** atlasiet **Pievienot** un pēc tam atlasiet prasmi.</span><span class="sxs-lookup"><span data-stu-id="72111-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="72111-153">Sadaļā **Izglītības prasības** atlasiet **Pievienot** un pēc tam atlasiet vērtības no **Izglītības** un **Izglītības līmeņa** nolaižamajiem logiem.</span><span class="sxs-lookup"><span data-stu-id="72111-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Pievienot izglītības prasības](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="72111-155">Sadaļā **Komentārs** pievienojiet komentārus pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="72111-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="72111-156">Sadaļā **Kompensācija** atlasiet līmeni no **Līmeņa** nolaižamā saraksta un pēc tam pielāgojiet **Zemu slieksni**, **Kontrolpunktu** un **Augstu slieksni**.</span><span class="sxs-lookup"><span data-stu-id="72111-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="72111-157">Kad jūsu personāla atlases pieprasījums ir pabeigts un jūs esat gatavs sākt personāla atlases procesu, izvēlņu joslā atlasiet **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="72111-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Aktivizēt personāla atlases pieprasījumu](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="72111-159">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="72111-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="72111-160">Skatīt un rediģēt atlases pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="72111-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="72111-161">Ja esat vadītājs un vēlaties skatīt savus pieprasījumus:</span><span class="sxs-lookup"><span data-stu-id="72111-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="72111-162">Atlasiet **Darbinieku pašapkalpošanās pakalpojums**.</span><span class="sxs-lookup"><span data-stu-id="72111-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="72111-163">Atlasiet cilni **Mana komanda**.</span><span class="sxs-lookup"><span data-stu-id="72111-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="72111-164">Sadaļā **Manas darba grupas informācija** atlasiet cilni **Personāla atlases pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="72111-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Atlasiet cilni Personāla atlases pieprasījumi](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="72111-166">Lai apskatītu vai rediģētu personāla atlases pieprasījumu, atlasiet to režģī.</span><span class="sxs-lookup"><span data-stu-id="72111-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="72111-167">Ja esat HR pro un vēlaties skatīt visus personāla atlases pieprasījumus:</span><span class="sxs-lookup"><span data-stu-id="72111-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="72111-168">Atlasiet **Personāla pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="72111-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="72111-169">Atlasiet **Personāla atlases pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="72111-169">Select **Recruiting requests**.</span></span>

   ![Skatīt personāla atlases pieprasījumus Personāla pārvaldībā](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="72111-171">Lai apskatītu vai rediģētu personāla atlases pieprasījumu, atlasiet to režģī.</span><span class="sxs-lookup"><span data-stu-id="72111-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="72111-172">Pievienot vai rediģēt kandidāta profilu</span><span class="sxs-lookup"><span data-stu-id="72111-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="72111-173">Ja jūsu uzņēmums ir integrēts ar citu programmu, lai pārvaldītu personāla atlases pieprasījumus, personāla atlases pieprasījumi tiek pārsūtīti uz šo programmu.</span><span class="sxs-lookup"><span data-stu-id="72111-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="72111-174">Pēc tam personāla atlases programma nosūta informāciju par kandidātu uz Personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="72111-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="72111-175">Pretējā gadījumā varat sekot saviem iekšējiem personāla atlases procesiem un ievadīt informāciju par kandidātu manuāli.</span><span class="sxs-lookup"><span data-stu-id="72111-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="72111-176">Atlasiet **Personāla pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="72111-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="72111-177">Atlasiet **Saites**.</span><span class="sxs-lookup"><span data-stu-id="72111-177">Select **Links**.</span></span>

3. <span data-ttu-id="72111-178">Sadaļā **Personāla atlase** atlasiet **Kandidāti**.</span><span class="sxs-lookup"><span data-stu-id="72111-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Skatīt kandidātus](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="72111-180">Lai pievienotu kandidātu, atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="72111-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="72111-181">Lai rediģētu esošu kandidātu, izvēlieties kandidātu no saraksta un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="72111-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="72111-182">Tiek parādīts kandidāta profils.</span><span class="sxs-lookup"><span data-stu-id="72111-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="72111-183">Sadaļā **Kandidāta kopsavilkums** ievadiet vai rediģējiet informāciju par kandidātu pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="72111-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="72111-184">Sadaļā **Personāla atlases pieprasījums** atlasiet atlases pieprasījumu, lai saistītu kandidātu.</span><span class="sxs-lookup"><span data-stu-id="72111-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="72111-185">Pēc tam pabeidziet **Aprēķināto sākuma datumu**, **Pieņemšanas vadītāju**, **Amatu** un **Apraksta laukus**.</span><span class="sxs-lookup"><span data-stu-id="72111-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Saistīt ar personāla atlases pieprasījumu](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="72111-187">Aizpildiet visu informāciju, ko vēlaties iekļaut kandidāta ierakstā, sekojošajās jomās:</span><span class="sxs-lookup"><span data-stu-id="72111-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="72111-188">**Komentāri**</span><span class="sxs-lookup"><span data-stu-id="72111-188">**Comments**</span></span>
   - <span data-ttu-id="72111-189">**Profesionālā pieredze**</span><span class="sxs-lookup"><span data-stu-id="72111-189">**Professional experience**</span></span>
   - <span data-ttu-id="72111-190">**Kontaktinformācija**</span><span class="sxs-lookup"><span data-stu-id="72111-190">**Contact information**</span></span>
   - <span data-ttu-id="72111-191">**Izglītība**</span><span class="sxs-lookup"><span data-stu-id="72111-191">**Education**</span></span>
   - <span data-ttu-id="72111-192">**Prasmes**</span><span class="sxs-lookup"><span data-stu-id="72111-192">**Skills**</span></span>
   - <span data-ttu-id="72111-193">**Sertifikāti**</span><span class="sxs-lookup"><span data-stu-id="72111-193">**Certificates**</span></span>
   - <span data-ttu-id="72111-194">**Izvērtēšana**</span><span class="sxs-lookup"><span data-stu-id="72111-194">**Screenings**</span></span>

8. <span data-ttu-id="72111-195">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="72111-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="72111-196">Pieņemt darbā kandidātu</span><span class="sxs-lookup"><span data-stu-id="72111-196">Hire a candidate</span></span>

<span data-ttu-id="72111-197">Kad esat gatavs pieņemt darbā kandidātu, ievērojiet šo procedūru, lai nomainītu kandidātu uz darbinieku.</span><span class="sxs-lookup"><span data-stu-id="72111-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="72111-198">Kandidāta veidlapā atlasiet **Pieņemt darbā**.</span><span class="sxs-lookup"><span data-stu-id="72111-198">On the candidate form, select **Hire**.</span></span>

   ![Pieņemt darbā kandidātu](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="72111-200">Aizpildiet visus laukus veidlapā **Pieņemt darbā jaunu darbinieku**, sadaļā **Detalizēti** .</span><span class="sxs-lookup"><span data-stu-id="72111-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Ievadīt jaunā darbinieka informāciju](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="72111-202">Sadaļā **Amata detaļas** pēc nepieciešamības pārbaudiet un mainiet informāciju.</span><span class="sxs-lookup"><span data-stu-id="72111-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="72111-203">Sadaļā **Iekārtošanas kontrolsaraksti** atlasiet šim darbiniekam atbilstīgos iekārtošanas kontrolsarakstus.</span><span class="sxs-lookup"><span data-stu-id="72111-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="72111-204">Atlasiet **Turpināt**, lai izveidotu darbinieka ierakstu.</span><span class="sxs-lookup"><span data-stu-id="72111-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="72111-205">Atkarībā no jūsu organizācijas darbplūsmām kandidāta ieraksts var iziet caur papildu apstiprināšanas soļiem, pirms kļūst par darbinieka ierakstu.</span><span class="sxs-lookup"><span data-stu-id="72111-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="72111-206">Nolemt nepieņemt darbā kandidātu</span><span class="sxs-lookup"><span data-stu-id="72111-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="72111-207">Ja izlemjat nepieņemt kandidātu, sekojiet šai procedūrai, lai noņemtu to no pārbaudes procesa.</span><span class="sxs-lookup"><span data-stu-id="72111-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="72111-208">Kandidāta veidlapā atlasiet **Nepieņemt darbā**.</span><span class="sxs-lookup"><span data-stu-id="72111-208">On the candidate form, select **Do not hire**.</span></span>

   ![Nepieņemt darbā kandidātu](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="72111-210">Atlasiet **Pamatojuma kodu** un iekļaujiet komentārus.</span><span class="sxs-lookup"><span data-stu-id="72111-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="72111-211">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="72111-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="72111-212">Noraidīt kandidātu</span><span class="sxs-lookup"><span data-stu-id="72111-212">Dismiss a candidate</span></span>

<span data-ttu-id="72111-213">Ja nepieciešams, varat noraidīt kandidātu pēc pieņemšanas darbā.</span><span class="sxs-lookup"><span data-stu-id="72111-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="72111-214">Piemēram, kandidāts var noraidīt jūsu piedāvājumu vai neierasties darbā pirmajā dienā.</span><span class="sxs-lookup"><span data-stu-id="72111-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="72111-215">Kandidāta veidlapā atlasiet **Noraidīt kandidātu**.</span><span class="sxs-lookup"><span data-stu-id="72111-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Noraidīt kandidātu](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="72111-217">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="72111-217">See also</span></span>

[<span data-ttu-id="72111-218">Common Data Service virtuālo elementu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="72111-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="72111-219">Darbaspēka pārvaldība</span><span class="sxs-lookup"><span data-stu-id="72111-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="72111-220">Darba komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="72111-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)