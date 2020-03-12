---
title: Dynamics 365 Commerce priekšskatījuma vides konfigurēšana
description: Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce priekšskatījuma vidi, kad tā ir nodrošināta.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d72caee25c03e8167b94dd387c7861f98bd0f4cb
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057721"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="51ec0-103">Dynamics 365 Commerce priekšskatījuma vides konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="51ec0-103">Configure a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="51ec0-104">Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce priekšskatījuma vidi, kad tā ir nodrošināta.</span><span class="sxs-lookup"><span data-stu-id="51ec0-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="51ec0-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="51ec0-105">Overview</span></span>

<span data-ttu-id="51ec0-106">Šajā tēmā minētās procedūras veiciet tikai pēc tam, kad ir nodrošināta Commerce priekšskatījuma vide.</span><span class="sxs-lookup"><span data-stu-id="51ec0-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="51ec0-107">Informāciju par to, kā nodrošināt Commerce priekšskatījuma vidi, skatiet [Commerce priekšskatījuma vides nodrošināšana](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="51ec0-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="51ec0-108">Pēc tam, kad jūsu Commerce priekšskatījuma vide ir pilnībā nodrošināta, ir jāpabeidz papildu konfigurēšanas darbības pēc nodrošināšanas, pirms varat sākt novērtēt vidi.</span><span class="sxs-lookup"><span data-stu-id="51ec0-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="51ec0-109">Lai veiktu šīs darbības, ir jāizmanto Microsoft Dynamics Lifecycle Services (LCS) un Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51ec0-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="51ec0-110">Pirms darba sākšanas</span><span class="sxs-lookup"><span data-stu-id="51ec0-110">Before you start</span></span>

1. <span data-ttu-id="51ec0-111">Pierakstieties [LCS portālā](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="51ec0-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="51ec0-112">Dodieties uz savu projektu.</span><span class="sxs-lookup"><span data-stu-id="51ec0-112">Go to your project.</span></span>
1. <span data-ttu-id="51ec0-113">Augšējā izvēlnē atlasiet **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="51ec0-114">No saraksta atlasiet savu vidi.</span><span class="sxs-lookup"><span data-stu-id="51ec0-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="51ec0-115">Vides informācijas labajā pusē atlasiet **Visa informācija**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="51ec0-116">Lai atvērtu izvēlni, atlasiet **Pieteikties**, pēc tam atlasiet **Pieteikties vidē**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="51ec0-117">Pārliecinieties, ka ir atlasīta **USRT** juridiskā persona (augšējā labajā stūrī).</span><span class="sxs-lookup"><span data-stu-id="51ec0-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="51ec0-118">Konfigurējiet pārdošanas punktu LCS</span><span class="sxs-lookup"><span data-stu-id="51ec0-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="51ec0-119">Nodarbinātā saistīšana ar jūsu identitāti</span><span class="sxs-lookup"><span data-stu-id="51ec0-119">Associate a worker with your identity</span></span>

<span data-ttu-id="51ec0-120">Lai saistītu darbinieku ar jūsu identitāti LCS, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="51ec0-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="51ec0-121">Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība un komercija \> Darbinieki \> Nodarbinātie**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="51ec0-122">Sarakstā atrodiet un atlasiet šādu ierakstu **000713 – Endrjū Kollete**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="51ec0-123">Darbību rūtī atlasiet **Mazumtirdzniecība**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="51ec0-124">Atlasiet **Piesaistīt esošu identitāti**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="51ec0-125">Laukā **E-pasts** (pa labi no **Meklēt, izmantojot e-pastu**) ievadiet savu e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="51ec0-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="51ec0-126">Atlasiet **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-126">Select **Search**.</span></span>
1. <span data-ttu-id="51ec0-127">Atlasiet ierakstu ar savu vārdu.</span><span class="sxs-lookup"><span data-stu-id="51ec0-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="51ec0-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-128">Select **OK**.</span></span>
1. <span data-ttu-id="51ec0-129">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="51ec0-130">mākoņa POS aktivizēšana;</span><span class="sxs-lookup"><span data-stu-id="51ec0-130">Activate Cloud POS</span></span>

<span data-ttu-id="51ec0-131">Lai aktivizētu mākoņa POS LCS, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="51ec0-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="51ec0-132">Augšējā izvēlnē atlasiet **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="51ec0-133">No saraksta atlasiet savu vidi.</span><span class="sxs-lookup"><span data-stu-id="51ec0-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="51ec0-134">Vides informācijas labajā pusē atlasiet **Visa informācija**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="51ec0-135">Atlasiet **Pieteikšanās**, lai atvērtu izvēlni, un pēc tam atlasiet **Pieteikties mākoņa pārdošanas punktam**, lai atvērtu pārdošanas punktu (POS).</span><span class="sxs-lookup"><span data-stu-id="51ec0-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="51ec0-136">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-136">Select **Next**.</span></span>
1. <span data-ttu-id="51ec0-137">Piesakieties, izmantojot savu Microsoft Azure Active Directory (Azure AD) kontu.</span><span class="sxs-lookup"><span data-stu-id="51ec0-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="51ec0-138">Sadaļā **Veikala nosaukums** atlasiet **Sanfrancisko**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="51ec0-139">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-139">Select **Next**.</span></span>
1. <span data-ttu-id="51ec0-140">Sadaļā **Reģistrs un ierīce** atlasiet **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="51ec0-141">Atlasiet **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-141">Select **Activate**.</span></span> <span data-ttu-id="51ec0-142">Jūs esat izrakstījies un aizvirzīts uz POS pierakstīšanās lapu.</span><span class="sxs-lookup"><span data-stu-id="51ec0-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="51ec0-143">Tagad varat pieteikties mākoņa POS pieredzei, izmantojot operatora ID **000713** un paroli **123**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="51ec0-144">Iestatiet savu vietni pakalpojumā Commerce.</span><span class="sxs-lookup"><span data-stu-id="51ec0-144">Set up your site in Commerce</span></span>

<span data-ttu-id="51ec0-145">Lai sāktu iestatīt priekšskatījuma vietni pakalpojumā Commerce, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="51ec0-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="51ec0-146">Piesakieties vietnes pārvaldības rīkā, izmantojot URL vietrādi, kuru atzīmējāt, kad nodrošināšanas laikā inicializējāt e-Commerce (skatiet [e-Commerce inicializēšana](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="51ec0-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="51ec0-147">Atlasiet vietni **Fabrikam**, lai atvērtu vietnes iestatīšanas dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="51ec0-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="51ec0-148">Atlasiet domēnu, kuru ievadījāt, kad inicializējat e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="51ec0-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="51ec0-149">Kā noklusējuma kanālu atlasiet **Fabrikam paplašinātais tiešsaistes veikals**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="51ec0-150">(Pārliecinieties, ka atlasāt **paplašināto** tiešsaistes veikalu.)</span><span class="sxs-lookup"><span data-stu-id="51ec0-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="51ec0-151">Ka noklusējuma valodu atlasiet **en-us**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="51ec0-152">Atstājiet lauka **Path** vērtību tādu, kāda tā ir.</span><span class="sxs-lookup"><span data-stu-id="51ec0-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="51ec0-153">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-153">Select **OK**.</span></span> <span data-ttu-id="51ec0-154">Tiek parādīts vietnes lapu saraksts.</span><span class="sxs-lookup"><span data-stu-id="51ec0-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="51ec0-155">Darbu iespējošana</span><span class="sxs-lookup"><span data-stu-id="51ec0-155">Enable jobs</span></span>

<span data-ttu-id="51ec0-156">Lai iespējotu darbus pakalpojumā Commerce, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="51ec0-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="51ec0-157">Pierakstieties vidē (HQ).</span><span class="sxs-lookup"><span data-stu-id="51ec0-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="51ec0-158">Izmantojot izvēlni kreisajā pusē, dodieties uz **Mazumtirdzniecība un komercija \> Pieprasījumi un pārskati \> Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="51ec0-159">Šīs procedūras atlikušie soļi jāaizpilda katram no šiem darbiem:</span><span class="sxs-lookup"><span data-stu-id="51ec0-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="51ec0-160">Apstrādāt mazumtirdzniecības pasūtījuma e-pasta paziņojumu</span><span class="sxs-lookup"><span data-stu-id="51ec0-160">Process retail order email notification</span></span>
    * <span data-ttu-id="51ec0-161">Preču pieejamība</span><span class="sxs-lookup"><span data-stu-id="51ec0-161">Product availability</span></span>
    * <span data-ttu-id="51ec0-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="51ec0-162">P-0001</span></span>
    * <span data-ttu-id="51ec0-163">Darbs Sinhronizēt pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="51ec0-163">Synchronize orders job</span></span>

1. <span data-ttu-id="51ec0-164">Izmantojiet ātro filtru, lai meklētu darbu pēc nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="51ec0-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="51ec0-165">Ja darba statuss ir **Aizturēts**, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="51ec0-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="51ec0-166">Atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="51ec0-166">Select the record.</span></span>
    1. <span data-ttu-id="51ec0-167">Darbību rūtī noklikšķiniet uz cilnes **Pakešuzdevums**, pēc tam atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="51ec0-168">Atlasiet **Gaida** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="51ec0-169">Izpildīt pilnīgu datu sinhronizāciju</span><span class="sxs-lookup"><span data-stu-id="51ec0-169">Run full data synchronization</span></span>

<span data-ttu-id="51ec0-170">Lai pakalpojumā Commerce palaistu pilnu datu sinhronizāciju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="51ec0-170">To run full data synchronization in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="51ec0-171">Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība un komercija \> Mazumtirdzniecības uzstādīšana \> Mazumtirdzniecības plānotājs \> Kanāla datubāze**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-171">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="51ec0-172">Kanāls **Noklusējums** ir atlasīts no saraksta kreisajā pusē.</span><span class="sxs-lookup"><span data-stu-id="51ec0-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="51ec0-173">Izvēlieties citu pieejamo kanālu.</span><span class="sxs-lookup"><span data-stu-id="51ec0-173">Select the other available channel.</span></span> <span data-ttu-id="51ec0-174">Šī kanāla nosaukums **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="51ec0-175">Darbību rūtī atlasiet **Pilnīga datu sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="51ec0-176">Ievadiet **9999** kā sadales grafiku.</span><span class="sxs-lookup"><span data-stu-id="51ec0-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="51ec0-177">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-177">Select **OK**.</span></span>
1. <span data-ttu-id="51ec0-178">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="51ec0-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="51ec0-179">Kredītkartes informācijas pārbaude, lai veiktu pārbaudes pirkumus</span><span class="sxs-lookup"><span data-stu-id="51ec0-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="51ec0-180">Lai vietnē veiktu pārbaudes transakcijas, varat izmantot tālāk minēto pārbaudes kredītkartes informāciju.</span><span class="sxs-lookup"><span data-stu-id="51ec0-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="51ec0-181">**Kartes numurs:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="51ec0-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="51ec0-182">**Beigu datums:** 10/20</span><span class="sxs-lookup"><span data-stu-id="51ec0-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="51ec0-183">**Kartes verificēšanas vērtības (CVV) kods:** 737</span><span class="sxs-lookup"><span data-stu-id="51ec0-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51ec0-184">Pārbaudes vietnē nekādā gadījumā nemēģiniet izmantot īstas kredītkartes informāciju.</span><span class="sxs-lookup"><span data-stu-id="51ec0-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="51ec0-185">Nākamās darbības</span><span class="sxs-lookup"><span data-stu-id="51ec0-185">Next steps</span></span>

<span data-ttu-id="51ec0-186">Kad nodrošināšanas un konfigurēšanas darbības ir pabeigtas, varat novērtēt priekšskatījuma vidi.</span><span class="sxs-lookup"><span data-stu-id="51ec0-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="51ec0-187">Izmantojiet Commerce vietnes pārvaldības rīka URL, lai dotos uz autorēšanas pieredzi.</span><span class="sxs-lookup"><span data-stu-id="51ec0-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="51ec0-188">Izmantojiet Commerce vietnes pārvaldības rīka URL, lai dotos uz mazumtirdzniecības klienta vietnes pieredzi.</span><span class="sxs-lookup"><span data-stu-id="51ec0-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="51ec0-189">Lai konfigurētu neobligātos līdzekļus savai Commerce priekšskatījuma videi, skatiet [Commerce priekšskatījuma vides neobligāto līdzekļu konfigurēšana](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="51ec0-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51ec0-190">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="51ec0-190">Additional resources</span></span>

[<span data-ttu-id="51ec0-191">Dynamics 365 Commerce priekšskatījuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="51ec0-191">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="51ec0-192">Dynamics 365 Commerce priekšskatījuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="51ec0-192">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="51ec0-193">Izvēles funkciju konfigurēšana Dynamics 365 Commerce priekšskatījuma videi</span><span class="sxs-lookup"><span data-stu-id="51ec0-193">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="51ec0-194">Dynamics 365 Commerce priekšskatījuma vides BUJ</span><span class="sxs-lookup"><span data-stu-id="51ec0-194">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="51ec0-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="51ec0-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="51ec0-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="51ec0-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="51ec0-197">Microsoft Azure portāls</span><span class="sxs-lookup"><span data-stu-id="51ec0-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="51ec0-198">Dynamics 365 Commerce tīmekļa vietne</span><span class="sxs-lookup"><span data-stu-id="51ec0-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
