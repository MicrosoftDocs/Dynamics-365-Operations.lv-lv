---
title: Failu robots.txt pārvaldība
description: Šajā tēmā aprakstīts, kā pārvaldīt Microsoft Dynamics 365 Commerce robots.txt failus.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: ad87594b9c20d0c2b53e8d4e7c1170a78babe74b
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517456"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="5a305-103">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="5a305-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5a305-104">Šajā tēmā aprakstīts, kā pārvaldīt Microsoft Dynamics 365 Commerce robots.txt failus.</span><span class="sxs-lookup"><span data-stu-id="5a305-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5a305-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="5a305-105">Overview</span></span>

<span data-ttu-id="5a305-106">Robotu izslēgšanas standarts jeb robots.txt ir standarts, kuru tīmekļa vietnes izmanto, lai sazinātos ar tīmekļa robotiem.</span><span class="sxs-lookup"><span data-stu-id="5a305-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="5a305-107">Tas instruē tīmekļa robotus par jebkuru mājas lapas apgabalu, kuru nedrīkst apmeklēt.</span><span class="sxs-lookup"><span data-stu-id="5a305-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="5a305-108">Robotus bieži izmanto meklētājprogrammas, lai apzīmētu tīmekļa vietnes.</span><span class="sxs-lookup"><span data-stu-id="5a305-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="5a305-109">Lai izslēgtu robotus no servera, izveidojiet failu serverī.</span><span class="sxs-lookup"><span data-stu-id="5a305-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="5a305-110">Šajā failā jūs norādāt robotu piekļuves politiku.</span><span class="sxs-lookup"><span data-stu-id="5a305-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="5a305-111">Failam jābūt pieejamam, izmantojot HTTP lokālo URL **/robots.txt.**</span><span class="sxs-lookup"><span data-stu-id="5a305-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="5a305-112">robots.txt fails palīdz meklētājprogrammām indeksēt saturu jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="5a305-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="5a305-113">Dynamics 365 Commerce ļauj augšupielādēt failu robots.txt jūsu domēnam.</span><span class="sxs-lookup"><span data-stu-id="5a305-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="5a305-114">Katram domēnam jūsu Commerce vidē varat augšupielādēt vienu robots.txt failu un saistīt to ar šo domēnu.</span><span class="sxs-lookup"><span data-stu-id="5a305-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="5a305-115">Lai iegūtu papildinformāciju par failu robots.txt, apmeklējiet [Tīmekļa robotu lapas](https://www.robotstxt.org/)</span><span class="sxs-lookup"><span data-stu-id="5a305-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="5a305-116">Faila robots.txt augšupielāde</span><span class="sxs-lookup"><span data-stu-id="5a305-116">Upload a robots.txt file</span></span>

<span data-ttu-id="5a305-117">Pēc tam, kad esat izveidojis un rediģējis failu robots.txt saskaņā ar [robotu izslēgšanas standartu](https://www.robotstxt.org/orig.html), pārliecinieties, vai fails ir pieejams datorā, kurā izmantosiet tirdzniecības autorēšanas rīkus.</span><span class="sxs-lookup"><span data-stu-id="5a305-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="5a305-118">Faila nosaukumam ir jābūt **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="5a305-119">Lai iegūtu vislabākos rezultātus, tam jābūt formātā, kas norādīts standartā.</span><span class="sxs-lookup"><span data-stu-id="5a305-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="5a305-120">Katrs Commerce klients ir atbildīgs par tā robots.txt faila satura apstiprināšanu un uzturēšanu.</span><span class="sxs-lookup"><span data-stu-id="5a305-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="5a305-121">Lai augšupielādētu robots.txt failu, jums ir jāpierakstās Commerce kā sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="5a305-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="5a305-122">Lai Commerce vietnē augšupielādētu robots.txt failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5a305-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5a305-123">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="5a305-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5a305-124">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="5a305-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5a305-125">Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5a305-126">Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.</span><span class="sxs-lookup"><span data-stu-id="5a305-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5a305-127">Atlasiet **Pārvaldīt**, lai augšupielādētu failu robots.txt domēnam jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="5a305-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5a305-128">Labajā pusē esošajā izvēlnē atlasiet pogu **Augšupielādēt** (augšupvērstā bultiņa) blakus domēnam, kas ir saistīts ar failu robots.txt.</span><span class="sxs-lookup"><span data-stu-id="5a305-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5a305-129">Tiek parādīts failu pārlūka dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="5a305-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="5a305-130">Dialoglodziņā pārlūkojiet un atlasiet failu robots.txt, kuru vēlaties augšupielādēt saistītajam domēnam, un pēc tam atlasiet **Atvērt**, lai pabeigtu augšupielādi.</span><span class="sxs-lookup"><span data-stu-id="5a305-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="5a305-131">Augšupielādes laikā Commerce pārbauda, vai fails ir teksta fails, bet tas neapliecina faila saturu.</span><span class="sxs-lookup"><span data-stu-id="5a305-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="5a305-132">Faila robots.txt lejupielāde</span><span class="sxs-lookup"><span data-stu-id="5a305-132">Download a robots.txt file</span></span>

<span data-ttu-id="5a305-133">Lai Commerce vietnē lejupielādētu robots.txt failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5a305-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5a305-134">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="5a305-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5a305-135">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="5a305-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5a305-136">Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5a305-137">Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.</span><span class="sxs-lookup"><span data-stu-id="5a305-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5a305-138">Atlasiet **Pārvaldīt**, lai lejupielādētu failu robots.txt domēnam jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="5a305-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5a305-139">Labajā pusē esošajā izvēlnē atlasiet pogu **Lejupielādēt** (lejupvērstā bultiņa) blakus domēnam, kas ir saistīts ar failu robots.txt.</span><span class="sxs-lookup"><span data-stu-id="5a305-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5a305-140">Tiek parādīts failu pārlūka dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="5a305-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="5a305-141">Dialoglodziņā pārejiet uz vēlamo atrašanās vietu lokālajā diskā, apstipriniet vai ievadiet faila nosaukumu un pēc tam atlasiet **Saglabāt**, lai pabeigtu lejupielādi.</span><span class="sxs-lookup"><span data-stu-id="5a305-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="5a305-142">Šo procedūru var izmantot, lai lejupielādētu tikai failus robots.txt, kas iepriekš tika augšupielādēti, izmantojot Commerce autorēšanas rīkus.</span><span class="sxs-lookup"><span data-stu-id="5a305-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="5a305-143">Faila robots.txt dzēšana</span><span class="sxs-lookup"><span data-stu-id="5a305-143">Delete a robots.txt file</span></span>

<span data-ttu-id="5a305-144">Lai Commerce vietnē dzēstu robots.txt failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5a305-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5a305-145">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="5a305-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="5a305-146">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="5a305-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="5a305-147">Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="5a305-148">Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.</span><span class="sxs-lookup"><span data-stu-id="5a305-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="5a305-149">Atlasiet **Pārvaldīt**, lai dzēstu failu robots.txt domēnam jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="5a305-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="5a305-150">Labajā pusē esošajā izvēlnē atlasiet pogu **Dzēst** (atkritumu urnas simbols) blakus domēnam, kas ir saistīts ar failu robots.txt.</span><span class="sxs-lookup"><span data-stu-id="5a305-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="5a305-151">Tiek parādīts failu pārlūka logs.</span><span class="sxs-lookup"><span data-stu-id="5a305-151">A file browser window appears.</span></span>
6. <span data-ttu-id="5a305-152">Faila pārlūka logā pārlūkojiet un atlasiet failu robots.txt, kuru vēlaties dzēst saistītajam domēnam, un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="5a305-153">Tiek parādīts brīdinājuma ziņojuma lodziņš.</span><span class="sxs-lookup"><span data-stu-id="5a305-153">A warning message box appears.</span></span>
7. <span data-ttu-id="5a305-154">Ziņojuma lodziņā atlasiet **Dzēst**, lai apstiprinātu faila robots.txt dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="5a305-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="5a305-155">Šo procedūru var izmantot, lai dzēstu tikai failus robots.txt, kas iepriekš tika augšupielādēti, izmantojot Commerce autorēšanas rīkus.</span><span class="sxs-lookup"><span data-stu-id="5a305-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a305-156">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5a305-156">Additional resources</span></span>

[<span data-ttu-id="5a305-157">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5a305-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5a305-158">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="5a305-158">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="5a305-159">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="5a305-159">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="5a305-160">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="5a305-160">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="5a305-161">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="5a305-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="5a305-162">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="5a305-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="5a305-163">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="5a305-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="5a305-164">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="5a305-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="5a305-165">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="5a305-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="5a305-166">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="5a305-166">Enable location-based store detection</span></span>](enable-store-detection.md)
