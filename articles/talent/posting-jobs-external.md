---
title: Darbu publicēšana ārējās karjeras vietnēs no pakalpojuma Attract
description: Šajā tēmā ir sniegta informācija par to, kā izmantot Dynamics 365 for Talent - Attract, lai publicētu darbus ārējās personāla atlases vietnēs
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518563"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="60574-103">Darbu publicēšana ārējās karjeras vietnēs no pakalpojuma Attract</span><span class="sxs-lookup"><span data-stu-id="60574-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60574-104">Jūs vēlaties, lai jūsu atvērtās pozīcijas redz iespējami daudz kvalificētu kandidātu.</span><span class="sxs-lookup"><span data-stu-id="60574-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="60574-105">Personāla atlases vietnes, piemēram, Broadbean, palīdz jums sasniegt šo mērķi.</span><span class="sxs-lookup"><span data-stu-id="60574-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="60574-106">Microsoft Dynamics 365 Talent: pakalpojums Attract tagad ļauj jums publicēt vietnē Broadbean, un Microsoft pastāvīgi nodrošina jaunu piedāvājumu šajā jomā.</span><span class="sxs-lookup"><span data-stu-id="60574-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="60574-107">Darbu publicēšana vietnē Broadbean</span><span class="sxs-lookup"><span data-stu-id="60574-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="60574-108">Lai varētu publicēt darbus vietnē Broadbean, vispirms ir jākonfigurē Broadbean integrācija.</span><span class="sxs-lookup"><span data-stu-id="60574-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="60574-109">Lai publicētu darbus ārējās vietnēs, ir nepieciešama [visaptveroša nolīgšanas pievienojumprogramma](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="60574-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="60574-110">Šis līdzeklis pašreiz ir priekšskatījumā.</span><span class="sxs-lookup"><span data-stu-id="60574-110">This feature is currently in preview.</span></span> <span data-ttu-id="60574-111">Ja vēlaties to izmēģināt, jums [tā ir jāieslēdz pakalpojuma Attract administratora iestatījumos](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="60574-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="60574-112">Broadbean integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="60574-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="60574-113">Piesakieties pakalpojumā Attract kā administrators.</span><span class="sxs-lookup"><span data-stu-id="60574-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="60574-114">Atlasiet pogu **Iestatījumi** (zobrata simbols) lapas labās puses augšējā stūrī un pēc tam atlasiet **Administrēšanas centrs**.</span><span class="sxs-lookup"><span data-stu-id="60574-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="60574-115">Sadaļas **Iespējot Broadbean integrāciju** cilnē **Darbu sludinājuma dēļa iestatījumi** ieslēdziet integrāciju.</span><span class="sxs-lookup"><span data-stu-id="60574-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="60574-116">Sazinieties ar Broadbean un ievadiet informāciju laukā **Lietotājvārds, Klienta ID, Šifrēšanas pilnvara**.</span><span class="sxs-lookup"><span data-stu-id="60574-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="60574-117">Jūsu Broadbean akreditācijas dati ir jutīgi un konfidenciāli.</span><span class="sxs-lookup"><span data-stu-id="60574-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="60574-118">Tāpēc glabājiet un koplietojiet tos atbildīgi.</span><span class="sxs-lookup"><span data-stu-id="60574-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="60574-119">Ikviena persona, kurai administratora loma pakalpojumā Attract, var skatīt šos akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="60574-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="60574-120">Microsoft un Attract nav iesaistīti šo vērtību izveidē un saglabāšanā.</span><span class="sxs-lookup"><span data-stu-id="60574-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="60574-121">Jūsu pienākums ir tos atjaunināt pakalpojumā Attract un sadarboties ar Broadbean, lai atrisinātu jebkādas problēmas, kas ir saistītas ar jūsu akreditācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="60574-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="60574-122">Darba publicēšana vietnē Broadbean</span><span class="sxs-lookup"><span data-stu-id="60574-122">Post a job to Broadbean</span></span>

<span data-ttu-id="60574-123">Kad vietne Broadbean ir ieslēgta, personāla atlases darbinieki un administratori var publicēt tajā darbu.</span><span class="sxs-lookup"><span data-stu-id="60574-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="60574-124">Ir nepieciešams pieteikšanās uz darbu URL.</span><span class="sxs-lookup"><span data-stu-id="60574-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="60574-125">Pakalpojumā Attract atveriet darbu, kuru vēlaties publicēt vietnē Broadbean.</span><span class="sxs-lookup"><span data-stu-id="60574-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="60574-126">Sadaļā **Publikācijas** atlasiet pogu **Publicēt tagad**, kas atbilst vietnei Broadbean.</span><span class="sxs-lookup"><span data-stu-id="60574-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="60574-127">Izpildiet norādījumus Broadbean logā.</span><span class="sxs-lookup"><span data-stu-id="60574-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="60574-128">Pakalpojums Attract nosūta uz vietni Broadbean tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="60574-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="60574-129">Pieprasījuma ID</span><span class="sxs-lookup"><span data-stu-id="60574-129">Request ID</span></span>
- <span data-ttu-id="60574-130">Amata nosaukums</span><span class="sxs-lookup"><span data-stu-id="60574-130">Job title</span></span>
- <span data-ttu-id="60574-131">Darba apraksts</span><span class="sxs-lookup"><span data-stu-id="60574-131">Job description</span></span>
- <span data-ttu-id="60574-132">Amata atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="60574-132">Job location</span></span>
- <span data-ttu-id="60574-133">Pieteikšanās URL</span><span class="sxs-lookup"><span data-stu-id="60574-133">Apply URL</span></span>
- <span data-ttu-id="60574-134">Personāla atlases speciālista informācija</span><span class="sxs-lookup"><span data-stu-id="60574-134">Recruiter information</span></span>

<span data-ttu-id="60574-135">Kad publicēšana vietnē Broadbean ir sekmīgi pabeigta, pakalpojuma Attract darba sadaļā **Publikācijas** tiek parādīts Broadbean statuss **Publicēts**.</span><span class="sxs-lookup"><span data-stu-id="60574-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="60574-136">Vietnē Broadbean ir obligāti jāaizpilda lauks **Nozare**.</span><span class="sxs-lookup"><span data-stu-id="60574-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="60574-137">Šobrīd šis lauks pēc noklusējuma ir iestatīts ar vērtību **IT**.</span><span class="sxs-lookup"><span data-stu-id="60574-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="60574-138">Tomēr šo vērtību var nomainīt ar pareizo nozares opciju Broadbean darbu publicēšanas logā.</span><span class="sxs-lookup"><span data-stu-id="60574-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="60574-139">Darba publicēšanas visos atlasītajos darbu sludinājumu dēļos pabeigšana vietnē Broadbean ilgst kādu laiku.</span><span class="sxs-lookup"><span data-stu-id="60574-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="60574-140">Tāpēc var būt neliela aizkavēšanās, līdz pakalpojums Attract nodrošina darba statusa atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="60574-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="60574-141">Broadbean darba publikācijas skatīšana</span><span class="sxs-lookup"><span data-stu-id="60574-141">View a Broadbean job posting</span></span>

<span data-ttu-id="60574-142">Kad darbs ir publicēts vietnē Broadbean, to var skatīt, izmantojot pakalpojumu Attract.</span><span class="sxs-lookup"><span data-stu-id="60574-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="60574-143">Atveriet pakalpojumā Attract darbu, kuru vēlaties skatīt vietnē Broadbean.</span><span class="sxs-lookup"><span data-stu-id="60574-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="60574-144">Sadaļā **Publikācijas** atlasiet daudzpunktes pogu (**...**), kas atbilst vietnei Broadbean, un pēc tam atlasiet **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="60574-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="60574-145">Vietnē Broadbean publicētais darbs tiek parādīts jaunā logā.</span><span class="sxs-lookup"><span data-stu-id="60574-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="60574-146">Broadbean darba publikācijas atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="60574-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="60574-147">Darba publikāciju vietnē Broadbean var atjaunināt divējādi.</span><span class="sxs-lookup"><span data-stu-id="60574-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="60574-148">Atveriet pakalpojumā Attract darbu, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="60574-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="60574-149">Sadaļā **Publikācijas** atlasiet pogu **Atjaunināt publikāciju**, kas atbilst vietnei Broadbean.</span><span class="sxs-lookup"><span data-stu-id="60574-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="60574-150">Publikāciju rediģēšana Broadbean logā.</span><span class="sxs-lookup"><span data-stu-id="60574-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="60574-151">–vai–</span><span class="sxs-lookup"><span data-stu-id="60574-151">–or–</span></span>

1. <span data-ttu-id="60574-152">Atveriet pakalpojumā Attract darbu, kuru vēlaties skatīt vietnē Broadbean.</span><span class="sxs-lookup"><span data-stu-id="60574-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="60574-153">Sadaļā **Publikācijas** atlasiet daudzpunktes pogu (**...**), kas atbilst vietnei Broadbean, un pēc tam atlasiet **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="60574-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="60574-154">Broadbean logā rediģējiet darba datus un pēc tam vēlreiz publicējiet darbu.</span><span class="sxs-lookup"><span data-stu-id="60574-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="60574-155">Darba dati pakalpojumā Attract netiek mainīti.</span><span class="sxs-lookup"><span data-stu-id="60574-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="60574-156">Broadbean darba publikācijas noņemšana</span><span class="sxs-lookup"><span data-stu-id="60574-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="60574-157">Ja nepieciešamas, darba publikāciju vietnē Broadbean var noņemt.</span><span class="sxs-lookup"><span data-stu-id="60574-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="60574-158">Atveriet pakalpojumā Attract darbu, kuru vēlaties noņemt.</span><span class="sxs-lookup"><span data-stu-id="60574-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="60574-159">Sadaļā **Publikācijas** atlasiet daudzpunktes pogu (**...**), kas atbilst vietnei Broadbean, un pēc tam atlasiet **Noņemt publikāciju**.</span><span class="sxs-lookup"><span data-stu-id="60574-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="60574-160">Kad darba publikācija vietnē Broadbean ir noņemta, pakalpojumā Attract Broadbean elementam ir pieejama poga **Publicēt tagad**.</span><span class="sxs-lookup"><span data-stu-id="60574-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="60574-161">Šīs pogas klātbūtne norāda, ka darbs ir noņemts un to var publicēt atkal.</span><span class="sxs-lookup"><span data-stu-id="60574-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="60574-162">Ar Broadbean integrāciju saistīto problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="60574-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="60574-163">Ja darba publicēšana vietnē Broadbean rada problēmas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="60574-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="60574-164">Pārbaudiet, vai pakalpojumā Attract ievadītie Broadbean akreditācijas dati ir derīgi un pareizi.</span><span class="sxs-lookup"><span data-stu-id="60574-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="60574-165">Ja akreditācijas dati ir derīgi un pareizi, sazinieties ar [Broadbean atbalsta centru](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="60574-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="60574-166">Ja problēma joprojām pastāv, sazinieties ar [Microsoft atbalsta centru](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="60574-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
