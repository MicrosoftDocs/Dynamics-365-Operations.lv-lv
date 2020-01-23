---
title: Failu robots.txt pārvaldība
description: Šajā tēmā aprakstīts, kā pārvaldīt Microsoft Dynamics 365 Commerce robots.txt failus.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
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
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: e472f3612bd6860e7262bb128035f2aed3b39372
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946046"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="fc2be-103">Failu robots.txt pārvaldība</span><span class="sxs-lookup"><span data-stu-id="fc2be-103">Manage robots.txt files</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fc2be-104">Šajā tēmā aprakstīts, kā pārvaldīt Microsoft Dynamics 365 Commerce robots.txt failus.</span><span class="sxs-lookup"><span data-stu-id="fc2be-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fc2be-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="fc2be-105">Overview</span></span>

<span data-ttu-id="fc2be-106">Robotu izslēgšanas standarts jeb robots.txt ir standarts, kuru tīmekļa vietnes izmanto, lai sazinātos ar tīmekļa robotiem.</span><span class="sxs-lookup"><span data-stu-id="fc2be-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="fc2be-107">Tas instruē tīmekļa robotus par jebkuru mājas lapas apgabalu, kuru nedrīkst apmeklēt.</span><span class="sxs-lookup"><span data-stu-id="fc2be-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="fc2be-108">Robotus bieži izmanto meklētājprogrammas, lai apzīmētu tīmekļa vietnes.</span><span class="sxs-lookup"><span data-stu-id="fc2be-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="fc2be-109">Lai izslēgtu robotus no servera, izveidojiet failu serverī.</span><span class="sxs-lookup"><span data-stu-id="fc2be-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="fc2be-110">Šajā failā jūs norādāt robotu piekļuves politiku.</span><span class="sxs-lookup"><span data-stu-id="fc2be-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="fc2be-111">Failam jābūt pieejamam, izmantojot HTTP lokālo URL **/robots.txt.**</span><span class="sxs-lookup"><span data-stu-id="fc2be-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="fc2be-112">robots.txt fails palīdz meklētājprogrammām indeksēt saturu jūsu vietnē.</span><span class="sxs-lookup"><span data-stu-id="fc2be-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="fc2be-113">Dynamics 365 Commerce ļauj augšupielādēt failu robots.txt jūsu domēnam.</span><span class="sxs-lookup"><span data-stu-id="fc2be-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="fc2be-114">Katram domēnam jūsu Commerce vidē varat augšupielādēt vienu robots.txt failu un saistīt to ar šo domēnu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="fc2be-115">Lai iegūtu papildinformāciju par failu robots.txt, apmeklējiet [Tīmekļa robotu lapas](https://www.robotstxt.org/)</span><span class="sxs-lookup"><span data-stu-id="fc2be-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="fc2be-116">Faila robots.txt augšupielāde</span><span class="sxs-lookup"><span data-stu-id="fc2be-116">Upload a robots.txt file</span></span>

<span data-ttu-id="fc2be-117">Pēc tam, kad esat izveidojis un rediģējis failu robots.txt saskaņā ar [robotu izslēgšanas standartu](https://www.robotstxt.org/orig.html), pārliecinieties, vai fails ir pieejams datorā, kurā izmantosiet tirdzniecības autorēšanas rīkus.</span><span class="sxs-lookup"><span data-stu-id="fc2be-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="fc2be-118">Faila nosaukumam ir jābūt **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="fc2be-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="fc2be-119">Lai iegūtu vislabākos rezultātus, tam jābūt formātā, kas norādīts standartā.</span><span class="sxs-lookup"><span data-stu-id="fc2be-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="fc2be-120">Katrs Commerce klients ir atbildīgs par tā robots.txt faila satura apstiprināšanu un uzturēšanu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="fc2be-121">Lai augšupielādētu robots.txt failu, jums ir jāpierakstās Commerce kā sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="fc2be-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="fc2be-122">Lai Commerce vietnē augšupielādētu robots.txt failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="fc2be-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="fc2be-123">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="fc2be-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="fc2be-124">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="fc2be-125">Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="fc2be-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="fc2be-126">Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.</span><span class="sxs-lookup"><span data-stu-id="fc2be-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="fc2be-127">Atlasiet **Pārvaldīt**, lai augšupielādētu failu robots.txt domēnam jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="fc2be-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="fc2be-128">Labajā pusē esošajā izvēlnē atlasiet pogu **Augšupielādēt** (augšupvērstā bultiņā) blakus domēnam, kas ir saistīts ar failu robots.txt.</span><span class="sxs-lookup"><span data-stu-id="fc2be-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="fc2be-129">Tiek parādīts failu pārlūka dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="fc2be-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="fc2be-130">Dialoglodziņā pārlūkojiet un atlasiet failu robots.txt, kuru vēlaties augšupielādēt saistītajam domēnam, un pēc tam atlasiet **Atvērt**, lai pabeigtu augšupielādi.</span><span class="sxs-lookup"><span data-stu-id="fc2be-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="fc2be-131">Augšupielādes laikā Commerce pārbauda, vai fails ir teksta fails, bet tas nevalidē faila saturu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="fc2be-132">Faila robots.txt lejupielāde</span><span class="sxs-lookup"><span data-stu-id="fc2be-132">Download a robots.txt file</span></span>

<span data-ttu-id="fc2be-133">Lai Commerce vietnē lejupielādētu robots.txt failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="fc2be-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="fc2be-134">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="fc2be-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="fc2be-135">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="fc2be-136">Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="fc2be-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="fc2be-137">Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.</span><span class="sxs-lookup"><span data-stu-id="fc2be-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="fc2be-138">Atlasiet **Pārvaldīt**, lai lejupielādētu failu robots.txt domēnam jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="fc2be-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="fc2be-139">Labajā pusē esošajā izvēlnē atlasiet pogu **Lejupielādēt** (Lejupvērstā bultiņā) blakus domēnam, kas ir saistīts ar failu robots.txt.</span><span class="sxs-lookup"><span data-stu-id="fc2be-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="fc2be-140">Tiek parādīts failu pārlūka dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="fc2be-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="fc2be-141">Dialoglodziņā pārejiet uz vēlamo atrašanās vietu lokālajā diskā, apstipriniet vai ievadiet faila nosaukumu un pēc tam atlasiet **Saglabāt**, lai pabeigtu lejupielādi.</span><span class="sxs-lookup"><span data-stu-id="fc2be-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="fc2be-142">Šo procedūru var izmantot, lai lejupielādētu tikai failus robots.txt, kas iepriekš tika augšupielādēti, izmantojot Commerce autorēšanas rīkus.</span><span class="sxs-lookup"><span data-stu-id="fc2be-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="fc2be-143">Faila robots.txt dzēšana</span><span class="sxs-lookup"><span data-stu-id="fc2be-143">Delete a robots.txt file</span></span>

<span data-ttu-id="fc2be-144">Lai Commerce vietnē dzēstu robots.txt failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="fc2be-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="fc2be-145">Pierakstieties Commerce kā sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="fc2be-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="fc2be-146">Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="fc2be-147">Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="fc2be-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="fc2be-148">Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.</span><span class="sxs-lookup"><span data-stu-id="fc2be-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="fc2be-149">Atlasiet **Pārvaldīt**, lai dzēstu failu robots.txt domēnam jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="fc2be-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="fc2be-150">Labajā pusē esošajā izvēlnē atlasiet pogu **Dzēst** (atkritumu urnas simbols) blakus domēnam, kas ir saistīts ar failu robots.txt.</span><span class="sxs-lookup"><span data-stu-id="fc2be-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="fc2be-151">Parādās failu pārlūka logs.</span><span class="sxs-lookup"><span data-stu-id="fc2be-151">A file browser window appears.</span></span>
6. <span data-ttu-id="fc2be-152">Faila pārlūka logā pārlūkojiet un atlasiet failu robots.txt, kuru vēlaties dzēst saistītajam domēnam, un pēc tam atlasiet **Atvērt**, lai pabeigtu augšupielādi.</span><span class="sxs-lookup"><span data-stu-id="fc2be-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="fc2be-153">Tiek parādīts brīdinājuma ziņojuma lodziņš.</span><span class="sxs-lookup"><span data-stu-id="fc2be-153">A warning message box appears.</span></span>
7. <span data-ttu-id="fc2be-154">Ziņojuma lodziņā atlasiet **Dzēst**, lai apstiprinātu faila robots.txt dzēšanu.</span><span class="sxs-lookup"><span data-stu-id="fc2be-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="fc2be-155">Šo procedūru var izmantot, lai dzēstu tikai failus robots.txt, kas iepriekš tika augšupielādēti, izmantojot Commerce autorēšanas rīkus.</span><span class="sxs-lookup"><span data-stu-id="fc2be-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc2be-156">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fc2be-156">Additional resources</span></span>

[<span data-ttu-id="fc2be-157">Domēna nosaukuma konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="fc2be-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fc2be-158">Jaunas e-komercijas vietnes izvietošana</span><span class="sxs-lookup"><span data-stu-id="fc2be-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="fc2be-159">E-komercijas vietnes izveide</span><span class="sxs-lookup"><span data-stu-id="fc2be-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="fc2be-160">Tiešsaistes vietnes saistīšana ar kanālu</span><span class="sxs-lookup"><span data-stu-id="fc2be-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="fc2be-161">Pielāgotu lapu iestatīšana lietotāja pieteikumiem</span><span class="sxs-lookup"><span data-stu-id="fc2be-161">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="fc2be-162">Atbalsta pievienošana satura piegādes tīklam (CDN)</span><span class="sxs-lookup"><span data-stu-id="fc2be-162">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="fc2be-163">Veikala noteikšanas iespējošana pēc atrašanās vietas</span><span class="sxs-lookup"><span data-stu-id="fc2be-163">Enable location-based store detection</span></span>](enable-store-detection.md)
