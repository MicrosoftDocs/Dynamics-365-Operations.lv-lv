---
title: Dynamics 365 Commerce novērtējuma vides konfigurācija
description: Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce novērtējuma vidi, pēc tās nodrošināšanas.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599728"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="d4258-103">Dynamics 365 Commerce novērtējuma vides konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d4258-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4258-104">Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 Commerce novērtējuma vidi, pēc tās nodrošināšanas.</span><span class="sxs-lookup"><span data-stu-id="d4258-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="d4258-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="d4258-105">Overview</span></span>

<span data-ttu-id="d4258-106">Šajā tēmā minētās procedūras veiciet tikai pēc tam, kad ir nodrošināta Commerce novērtējuma vide.</span><span class="sxs-lookup"><span data-stu-id="d4258-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="d4258-107">Informāciju par to, kā nodrošināt Commerce novērtējuma vidi, skatiet [Commerce novērtējuma vides nodrošināšana](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="d4258-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="d4258-108">Kad jūsu Commerce novērtējuma vide ir pilnībā nodrošināta, ir jāpabeidz papildu pēc nodrošināšanas konfigurācijas darbības, pirms var sākt novērtēt vidi.</span><span class="sxs-lookup"><span data-stu-id="d4258-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="d4258-109">Lai veiktu šīs darbības, ir jāizmanto Microsoft Dynamics Lifecycle Services (LCS) un Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d4258-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="d4258-110">Pirms darba sākšanas</span><span class="sxs-lookup"><span data-stu-id="d4258-110">Before you start</span></span>

1. <span data-ttu-id="d4258-111">Pierakstieties [LCS portālā](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="d4258-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="d4258-112">Dodieties uz savu projektu.</span><span class="sxs-lookup"><span data-stu-id="d4258-112">Go to your project.</span></span>
1. <span data-ttu-id="d4258-113">Augšējā izvēlnē atlasiet **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="d4258-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="d4258-114">No saraksta atlasiet savu vidi.</span><span class="sxs-lookup"><span data-stu-id="d4258-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="d4258-115">Vides informācijas labajā pusē atlasiet **Pieteikties vidē**.</span><span class="sxs-lookup"><span data-stu-id="d4258-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="d4258-116">Jūs tiksiet nosūtīts uz Commerce galveno biroju.</span><span class="sxs-lookup"><span data-stu-id="d4258-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="d4258-117">Pārliecinieties, ka ir atlasīta **USRT** juridiskā persona (augšējā labajā stūrī).</span><span class="sxs-lookup"><span data-stu-id="d4258-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="d4258-118">Pēc nodrošināšanas darbību laikā Commerce Headquarters, pārliecinieties, ka **USRT** juridiskā persona vienmēr ir atlasīta.</span><span class="sxs-lookup"><span data-stu-id="d4258-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="d4258-119">Pārdošanas punkta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d4258-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="d4258-120">Nodarbinātā saistīšana ar jūsu identitāti</span><span class="sxs-lookup"><span data-stu-id="d4258-120">Associate a worker with your identity</span></span>

<span data-ttu-id="d4258-121">Lai saistītu darbinieku ar jūsu identitāti, veiciet Commerce Headquarters norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d4258-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="d4258-122">Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība un komercija \> Darbinieki \> Nodarbinātie**.</span><span class="sxs-lookup"><span data-stu-id="d4258-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="d4258-123">Sarakstā atrodiet un atlasiet šādu ierakstu **000713 – Endrjū Kollete**.</span><span class="sxs-lookup"><span data-stu-id="d4258-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="d4258-124">Darbību rūtī atlasiet **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d4258-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="d4258-125">Atlasiet **Piesaistīt esošu identitāti**.</span><span class="sxs-lookup"><span data-stu-id="d4258-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="d4258-126">Laukā **E-pasts** (pa labi no **Meklēt, izmantojot e-pastu**) ievadiet savu e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="d4258-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="d4258-127">Atlasiet **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="d4258-127">Select **Search**.</span></span>
1. <span data-ttu-id="d4258-128">Atlasiet ierakstu ar savu vārdu.</span><span class="sxs-lookup"><span data-stu-id="d4258-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="d4258-129">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d4258-129">Select **OK**.</span></span>
1. <span data-ttu-id="d4258-130">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d4258-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="d4258-131">mākoņa POS aktivizēšana;</span><span class="sxs-lookup"><span data-stu-id="d4258-131">Activate Cloud POS</span></span>

<span data-ttu-id="d4258-132">Lai aktivizētu mākoņa POS, veiciet LCS norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d4258-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="d4258-133">Augšējā izvēlnē atlasiet **Mākoņvides**.</span><span class="sxs-lookup"><span data-stu-id="d4258-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="d4258-134">No saraksta atlasiet savu vidi.</span><span class="sxs-lookup"><span data-stu-id="d4258-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="d4258-135">Vides informācijas labajā pusē atlasiet **Pieteikties mākoņa pārdošanas punktā**.</span><span class="sxs-lookup"><span data-stu-id="d4258-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="d4258-136">Atlasiet **Tālāk**, lai atvērtu dialoglodziņu **Pirms darba sākšanas**.</span><span class="sxs-lookup"><span data-stu-id="d4258-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="d4258-137">Atstājiet lauku **Servera URL**, kā tas ir.</span><span class="sxs-lookup"><span data-stu-id="d4258-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="d4258-138">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="d4258-138">Select **Next**.</span></span>
1. <span data-ttu-id="d4258-139">Piesakieties, izmantojot savu Microsoft Azure Active Directory (Azure AD) kontu.</span><span class="sxs-lookup"><span data-stu-id="d4258-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="d4258-140">Sadaļā **Veikala nosaukums** atlasiet **Sanfrancisko** un pēc tam atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="d4258-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="d4258-141">Sadaļā **Reģistrs un ierīce** atlasiet **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="d4258-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="d4258-142">Atlasiet **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="d4258-142">Select **Activate**.</span></span> <span data-ttu-id="d4258-143">Jūs esat izrakstījies un aizvirzīts uz POS pierakstīšanās lapu.</span><span class="sxs-lookup"><span data-stu-id="d4258-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="d4258-144">Tagad varat pieteikties mākoņa POS pieredzei, izmantojot operatora ID **000713** un paroli **123**.</span><span class="sxs-lookup"><span data-stu-id="d4258-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="d4258-145">Iestatiet savu vietni pakalpojumā Commerce.</span><span class="sxs-lookup"><span data-stu-id="d4258-145">Set up your site in Commerce</span></span>

<span data-ttu-id="d4258-146">Lai sāktu iestatīt novērtējuma vietni pakalpojumā Commerce, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d4258-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d4258-147">Piesakieties vietņu veidotājā, izmantojot URL vietrādi, kuru atzīmējāt, kad nodrošināšanas laikā inicializējāt e-komerciju (skatiet [e-komercijas inicializēšana](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="d4258-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="d4258-148">Atlasiet vietni **Fabrikam**, lai atvērtu vietnes iestatīšanas dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d4258-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="d4258-149">Atlasiet domēnu, kuru ievadījāt, kad inicializējat e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="d4258-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="d4258-150">Kā noklusējuma kanālu atlasiet **Fabrikam paplašinātais tiešsaistes veikals**.</span><span class="sxs-lookup"><span data-stu-id="d4258-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="d4258-151">(Pārliecinieties, ka atlasāt **paplašināto** tiešsaistes veikalu.)</span><span class="sxs-lookup"><span data-stu-id="d4258-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="d4258-152">Ka noklusējuma valodu atlasiet **en-us**.</span><span class="sxs-lookup"><span data-stu-id="d4258-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="d4258-153">Atstājiet lauka **Path** vērtību tādu, kāda tā ir.</span><span class="sxs-lookup"><span data-stu-id="d4258-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="d4258-154">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d4258-154">Select **OK**.</span></span> <span data-ttu-id="d4258-155">Tiek parādīts vietnes lapu saraksts.</span><span class="sxs-lookup"><span data-stu-id="d4258-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="d4258-156">Darbu iespējošana</span><span class="sxs-lookup"><span data-stu-id="d4258-156">Enable jobs</span></span>

<span data-ttu-id="d4258-157">Lai iespējotu darbus pakalpojumā Commerce, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d4258-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d4258-158">Pierakstieties vidē (HQ).</span><span class="sxs-lookup"><span data-stu-id="d4258-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="d4258-159">Izmantojot izvēlni kreisajā pusē, dodieties uz **Mazumtirdzniecība un komercija \> Pieprasījumi un pārskati \> Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="d4258-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="d4258-160">Šīs procedūras atlikušie soļi jāaizpilda katram no šiem darbiem:</span><span class="sxs-lookup"><span data-stu-id="d4258-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="d4258-161">Apstrādāt mazumtirdzniecības pasūtījuma e-pasta paziņojumu</span><span class="sxs-lookup"><span data-stu-id="d4258-161">Process retail order email notification</span></span>
    * <span data-ttu-id="d4258-162">Preču pieejamība</span><span class="sxs-lookup"><span data-stu-id="d4258-162">Product availability</span></span>
    * <span data-ttu-id="d4258-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="d4258-163">P-0001</span></span>
    * <span data-ttu-id="d4258-164">Darbs Sinhronizēt pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="d4258-164">Synchronize orders job</span></span>

1. <span data-ttu-id="d4258-165">Izmantojiet ātro filtru, lai meklētu darbu pēc nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="d4258-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="d4258-166">Ja darba statuss ir **Izpilda**, veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="d4258-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="d4258-167">Atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4258-167">Select the record.</span></span>
    1. <span data-ttu-id="d4258-168">Darbību rūtī noklikšķiniet uz cilnes **Pakešuzdevums**, pēc tam atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="d4258-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="d4258-169">Atlasiet **Atcelt** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d4258-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="d4258-170">Pēc izvēles var arī iestatīt atkārtošanās intervālu uz vienu (1) minūti šādiem darbiem:</span><span class="sxs-lookup"><span data-stu-id="d4258-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="d4258-171">Apstrādāt mazumtirdzniecības pasūtījuma e-pasta paziņojuma darbu</span><span class="sxs-lookup"><span data-stu-id="d4258-171">Process retail order email notification job</span></span>
* <span data-ttu-id="d4258-172">P-0001 darbs</span><span class="sxs-lookup"><span data-stu-id="d4258-172">P-0001 job</span></span>
* <span data-ttu-id="d4258-173">Darbs Sinhronizēt pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="d4258-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="d4258-174">Izpildīt pilnīgu datu sinhronizāciju</span><span class="sxs-lookup"><span data-stu-id="d4258-174">Run full data synchronization</span></span>

<span data-ttu-id="d4258-175">Lai pakalpojumā Commerce palaistu pilnu datu sinhronizāciju, veiciet Commerce Headquarters norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d4258-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="d4258-176">Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi \> Mazumtirdzniecība un komercija \> Mazumtirdzniecības uzstādīšana \> Komercijas plānotājs \> Kanāla datubāze**.</span><span class="sxs-lookup"><span data-stu-id="d4258-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="d4258-177">Atlasiet kanālu ar nosaukumu **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="d4258-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="d4258-178">Darbību rūtī atlasiet **Pilnīga datu sinhronizācija**.</span><span class="sxs-lookup"><span data-stu-id="d4258-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="d4258-179">Ievadiet **9999** kā sadales grafiku.</span><span class="sxs-lookup"><span data-stu-id="d4258-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="d4258-180">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d4258-180">Select **OK**.</span></span>
1. <span data-ttu-id="d4258-181">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d4258-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="d4258-182">Kredītkartes informācijas pārbaude, lai veiktu pārbaudes pirkumus</span><span class="sxs-lookup"><span data-stu-id="d4258-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="d4258-183">Lai vietnē veiktu pārbaudes transakcijas, varat izmantot tālāk minēto pārbaudes kredītkartes informāciju.</span><span class="sxs-lookup"><span data-stu-id="d4258-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="d4258-184">**Kartes numurs:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="d4258-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="d4258-185">**Beigu datums:** 10/20</span><span class="sxs-lookup"><span data-stu-id="d4258-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="d4258-186">**Kartes verificēšanas vērtības (CVV) kods:** 737</span><span class="sxs-lookup"><span data-stu-id="d4258-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4258-187">Pārbaudes vietnē nekādā gadījumā nemēģiniet izmantot īstas kredītkartes informāciju.</span><span class="sxs-lookup"><span data-stu-id="d4258-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d4258-188">Nākamās darbības</span><span class="sxs-lookup"><span data-stu-id="d4258-188">Next steps</span></span>

<span data-ttu-id="d4258-189">Kad nodrošināšanas un konfigurēšanas darbības ir pabeigtas, varat sākt izmantot novērtējuma vidi.</span><span class="sxs-lookup"><span data-stu-id="d4258-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="d4258-190">Izmantojiet Commerce vietnes veidotāja URL, lai dotos uz autorēšanas pieredzi.</span><span class="sxs-lookup"><span data-stu-id="d4258-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="d4258-191">Izmantojiet Commerce vietnes URL, lai dotos uz mazumtirdzniecības klienta vietnes pieredzi.</span><span class="sxs-lookup"><span data-stu-id="d4258-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="d4258-192">Lai konfigurētu neobligātos līdzekļus savai Commerce novērtējuma videi, skatiet [Commerce novērtējuma vides neobligāto līdzekļu konfigurācija](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="d4258-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4258-193">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d4258-193">Additional resources</span></span>

[<span data-ttu-id="d4258-194">Dynamics 365 Commerce novērtējuma vides pārskats</span><span class="sxs-lookup"><span data-stu-id="d4258-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="d4258-195">Dynamics 365 Commerce novērtējuma vides nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="d4258-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="d4258-196">Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="d4258-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="d4258-197">BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi</span><span class="sxs-lookup"><span data-stu-id="d4258-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="d4258-198">Bieži uzdotie jautājumi par Dynamics 365 Commerce novērtējuma vidi</span><span class="sxs-lookup"><span data-stu-id="d4258-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="d4258-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d4258-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="d4258-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="d4258-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="d4258-201">Microsoft Azure portāls</span><span class="sxs-lookup"><span data-stu-id="d4258-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="d4258-202">Dynamics 365 Commerce tīmekļa vietne</span><span class="sxs-lookup"><span data-stu-id="d4258-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
