---
title: Failu robots.txt pārvaldība
description: Šajā tēmā aprakstīts, kā pārvaldīt Microsoft Dynamics 365 Commerce robots.txt failus.
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9b832d6714447f8957095c8c87d48527087f12d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794239"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="01c41-103">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="01c41-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="01c41-104">Šajā tēmā aprakstīts, kā pārvaldīt Microsoft Dynamics 365 Commerce robots.txt failus.</span><span class="sxs-lookup"><span data-stu-id="01c41-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="01c41-105">Robotu izslēgšanas standarts jeb robots.txt ir standarts, kuru tīmekļa vietnes izmanto, lai sazinātos ar tīmekļa robotiem.</span><span class="sxs-lookup"><span data-stu-id="01c41-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="01c41-106">Tas instruē tīmekļa robotus par jebkuru mājas lapas apgabalu, kuru nedrīkst apmeklēt.</span><span class="sxs-lookup"><span data-stu-id="01c41-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="01c41-107">Robotus bieži izmanto meklētājprogrammas, lai apzīmētu tīmekļa vietnes.</span><span class="sxs-lookup"><span data-stu-id="01c41-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="01c41-108">Lai izslēgtu robotus no servera, izveidojiet failu serverī.</span><span class="sxs-lookup"><span data-stu-id="01c41-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="01c41-109">Šajā failā jūs norādāt robotu piekļuves politiku.</span><span class="sxs-lookup"><span data-stu-id="01c41-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="01c41-110">Failam jābūt pieejamam, izmantojot HTTP lokālo URL **/robots.txt.**</span><span class="sxs-lookup"><span data-stu-id="01c41-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="01c41-111">robots.txt fails palīdz meklētājprogrammām indeksēt saturu jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="01c41-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="01c41-112">Dynamics 365 Commerce ļauj augšupielādēt failu robots.txt jūsu domēnam.</span><span class="sxs-lookup"><span data-stu-id="01c41-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="01c41-113">Katram domēnam jūsu Commerce vidē varat augšupielādēt vienu robots.txt failu un saistīt to ar šo domēnu.</span><span class="sxs-lookup"><span data-stu-id="01c41-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="01c41-114">Lai iegūtu papildinformāciju par failu robots.txt, apmeklējiet [Tīmekļa robotu lapas](https://www.robotstxt.org/)</span><span class="sxs-lookup"><span data-stu-id="01c41-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="01c41-115">Faila robots.txt augšupielāde</span><span class="sxs-lookup"><span data-stu-id="01c41-115">Upload a robots.txt file</span></span>

<span data-ttu-id="01c41-116">Pēc tam, kad esat izveidojis un rediģējis failu robots.txt saskaņā ar [robotu izslēgšanas standartu](https://www.robotstxt.org/orig.html), pārliecinieties, vai fails ir pieejams datorā, kurā izmantosiet tirdzniecības autorēšanas rīkus.</span><span class="sxs-lookup"><span data-stu-id="01c41-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="01c41-117">Faila nosaukumam ir jābūt **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="01c41-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="01c41-118">Lai iegūtu vislabākos rezultātus, tam jābūt formātā, kas norādīts standartā.</span><span class="sxs-lookup"><span data-stu-id="01c41-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="01c41-119">Katrs Commerce klients ir atbildīgs par tā robots.txt faila satura apstiprināšanu un uzturēšanu.</span><span class="sxs-lookup"><span data-stu-id="01c41-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="01c41-120">Lai augšupielādētu robots.txt failu, jums ir jāpierakstās Commerce kā sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="01c41-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="01c41-121">Lai Commerce vietnē augšupielādētu robots.txt failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="01c41-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="01c41-122">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="01c41-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="01c41-123">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="01c41-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="01c41-124">Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="01c41-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="01c41-125">Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.</span><span class="sxs-lookup"><span data-stu-id="01c41-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="01c41-126">Atlasiet **Pārvaldīt**, lai augšupielādētu failu robots.txt domēnam jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="01c41-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="01c41-127">Labajā pusē esošajā izvēlnē atlasiet pogu **Augšupielādēt** (augšupvērstā bultiņa) blakus domēnam, kas ir saistīts ar failu robots.txt.</span><span class="sxs-lookup"><span data-stu-id="01c41-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="01c41-128">Tiek parādīts failu pārlūka dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="01c41-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="01c41-129">Dialoglodziņā pārlūkojiet un atlasiet failu robots.txt, kuru vēlaties augšupielādēt saistītajam domēnam, un pēc tam atlasiet **Atvērt**, lai pabeigtu augšupielādi.</span><span class="sxs-lookup"><span data-stu-id="01c41-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="01c41-130">Augšupielādes laikā Commerce pārbauda, vai fails ir teksta fails, bet tas neapliecina faila saturu.</span><span class="sxs-lookup"><span data-stu-id="01c41-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="01c41-131">Faila robots.txt lejupielāde</span><span class="sxs-lookup"><span data-stu-id="01c41-131">Download a robots.txt file</span></span>

<span data-ttu-id="01c41-132">Lai Commerce vietnē lejupielādētu robots.txt failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="01c41-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="01c41-133">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="01c41-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="01c41-134">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="01c41-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="01c41-135">Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="01c41-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="01c41-136">Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.</span><span class="sxs-lookup"><span data-stu-id="01c41-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="01c41-137">Atlasiet **Pārvaldīt**, lai lejupielādētu failu robots.txt domēnam jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="01c41-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="01c41-138">Labajā pusē esošajā izvēlnē atlasiet pogu **Lejupielādēt** (lejupvērstā bultiņa) blakus domēnam, kas ir saistīts ar failu robots.txt.</span><span class="sxs-lookup"><span data-stu-id="01c41-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="01c41-139">Tiek parādīts failu pārlūka dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="01c41-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="01c41-140">Dialoglodziņā pārejiet uz vēlamo atrašanās vietu lokālajā diskā, apstipriniet vai ievadiet faila nosaukumu un pēc tam atlasiet **Saglabāt**, lai pabeigtu lejupielādi.</span><span class="sxs-lookup"><span data-stu-id="01c41-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="01c41-141">Šo procedūru var izmantot, lai lejupielādētu tikai failus robots.txt, kas iepriekš tika augšupielādēti, izmantojot Commerce autorēšanas rīkus.</span><span class="sxs-lookup"><span data-stu-id="01c41-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="01c41-142">Faila robots.txt dzēšana</span><span class="sxs-lookup"><span data-stu-id="01c41-142">Delete a robots.txt file</span></span>

<span data-ttu-id="01c41-143">Lai Commerce vietnē dzēstu robots.txt failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="01c41-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="01c41-144">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="01c41-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="01c41-145">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="01c41-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="01c41-146">Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="01c41-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="01c41-147">Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.</span><span class="sxs-lookup"><span data-stu-id="01c41-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="01c41-148">Atlasiet **Pārvaldīt**, lai dzēstu failu robots.txt domēnam jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="01c41-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="01c41-149">Labajā pusē esošajā izvēlnē atlasiet pogu **Dzēst** (atkritumu urnas simbols) blakus domēnam, kas ir saistīts ar failu robots.txt.</span><span class="sxs-lookup"><span data-stu-id="01c41-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="01c41-150">Tiek parādīts failu pārlūka logs.</span><span class="sxs-lookup"><span data-stu-id="01c41-150">A file browser window appears.</span></span>
6. <span data-ttu-id="01c41-151">Faila pārlūka logā pārlūkojiet un atlasiet failu robots.txt, kuru vēlaties dzēst saistītajam domēnam, un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="01c41-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="01c41-152">Tiek parādīts brīdinājuma ziņojuma lodziņš.</span><span class="sxs-lookup"><span data-stu-id="01c41-152">A warning message box appears.</span></span>
7. <span data-ttu-id="01c41-153">Ziņojuma lodziņā atlasiet **Dzēst**, lai apstiprinātu faila robots.txt dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="01c41-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="01c41-154">Šo procedūru var izmantot, lai dzēstu tikai failus robots.txt, kas iepriekš tika augšupielādēti, izmantojot Commerce autorēšanas rīkus.</span><span class="sxs-lookup"><span data-stu-id="01c41-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01c41-155">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="01c41-155">Additional resources</span></span>

[<span data-ttu-id="01c41-156">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="01c41-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="01c41-157">Jauna e-tirdzniecības nomnieka izvietošana</span><span class="sxs-lookup"><span data-stu-id="01c41-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="01c41-158">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="01c41-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="01c41-159">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="01c41-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="01c41-160">Novirzīšanas URL lielapjoma augšupielāde</span><span class="sxs-lookup"><span data-stu-id="01c41-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="01c41-161">B2C nomnieka iestatīšana programmā Commerce</span><span class="sxs-lookup"><span data-stu-id="01c41-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="01c41-162">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="01c41-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="01c41-163">Vairāku B2C nomnieku konfigurēšana Commerce vidē</span><span class="sxs-lookup"><span data-stu-id="01c41-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="01c41-164">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="01c41-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="01c41-165">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="01c41-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
