---
title: Izmaksu kontrolēšanas mobilā darbvieta
description: Šajā tēmā ir sniegta informācija par mobilo darbvietu Izmaksu kontrolēšana. Šī darbvieta ļauj izmaksu centra vadītājiem skatīt informāciju par izmaksu centra veiktspēju jebkurā laikā un vietā.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 22acdcfbecc1efe78a1b1be87e40b2e7d23506fc
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759452"
---
# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="46351-104">Izmaksu kontrolēšanas mobilā darbvieta</span><span class="sxs-lookup"><span data-stu-id="46351-104">Cost controlling mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46351-105">Šajā tēmā ir sniegta informācija par mobilo darbvietu **Izmaksu kontrolēšana**.</span><span class="sxs-lookup"><span data-stu-id="46351-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="46351-106">Šī darbvieta ļauj izmaksu centra vadītājiem skatīt informāciju par izmaksu centra veiktspēju jebkurā laikā un vietā.</span><span class="sxs-lookup"><span data-stu-id="46351-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="46351-107">Šī mobilā darbvieta ir paredzēta lietošanai kopā ar mobilo programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="46351-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="46351-108">Pārskats</span><span class="sxs-lookup"><span data-stu-id="46351-108">Overview</span></span>
<span data-ttu-id="46351-109">Mobilā darbvieta **Izmaksu kontrole** sniedz tūlītēju skatu uz izmaksu centru pašreizējo veiktspēju, faktiskās izmaksas salīdzinot ar budžetā paredzētajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="46351-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="46351-110">Varat skatīt detalizētu informāciju ar atsevišķu izmaksu elementu statusu.</span><span class="sxs-lookup"><span data-stu-id="46351-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="46351-111">Piemēram, darbinieks saņem uzaicinājumu uz starptautisku konferenci, bet organizācijai ir jāsedz visi ceļa izdevumi.</span><span class="sxs-lookup"><span data-stu-id="46351-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="46351-112">Darbinieks vaicā savam vadītājam, vai viņš var apmeklēt šo konferenci.</span><span class="sxs-lookup"><span data-stu-id="46351-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="46351-113">Vadītājs savā mobilajā ierīcē ātri atver mobilo darbvietu **Izmaksu kontrole**, lai apskatītu, vai ir pieejams budžets, lai darbinieks šo konferenci varētu apmeklēt.</span><span class="sxs-lookup"><span data-stu-id="46351-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="46351-114">Datu drošība</span><span class="sxs-lookup"><span data-stu-id="46351-114">Data security</span></span>
<span data-ttu-id="46351-115">Darbvietā **Izmaksu kontrole** datus aizsargā lietotāja akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="46351-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="46351-116">Izmaksu centra vadītājiem ir atļauts skatīt tikai datus par savu izmaksu centru.</span><span class="sxs-lookup"><span data-stu-id="46351-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="46351-117">Piekļuves līmeņa drošība tiek pārvaldīta modulī **Izmaksu uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="46351-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="46351-118">Izmaksu grāmatveži mobilās darbvietas **Izmaksu kontrole** konfigurāciju definē modulī **Izmaksu uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="46351-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="46351-119">Pēc darbvietas publicēšanas mobilajā programmā tā ir pieejama programmā.</span><span class="sxs-lookup"><span data-stu-id="46351-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="46351-120">Tādējādi visi organizācijas izmaksu centra vadītāji var skatīt datus vienādā formātā.</span><span class="sxs-lookup"><span data-stu-id="46351-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="46351-121">Darbības, skati un saites</span><span class="sxs-lookup"><span data-stu-id="46351-121">Actions, views, and links</span></span>
<span data-ttu-id="46351-122">Mobilajā darbvietā **Izmaksu kontrolēšana** ir pieejamas tālāk norādītās darbības, skati un saites.</span><span class="sxs-lookup"><span data-stu-id="46351-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="46351-123">**Darbības:**</span><span class="sxs-lookup"><span data-stu-id="46351-123">**Actions:**</span></span>

    -   <span data-ttu-id="46351-124">Izmantojiet vienumu **Atlasīt konfigurāciju**, lai atlasītu izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="46351-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="46351-125">Izmantojiet vienumu **Atlasīt izmaksu objektu**, lai atlasītu izmaksu centrus, par kuriem filtrēt datus.</span><span class="sxs-lookup"><span data-stu-id="46351-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="46351-126">Sarakstā redzamie izmaksu centri ir atkarīgi no modulī **Izmaksu uzskaite** piešķirtajām piekļuves tiesībām.</span><span class="sxs-lookup"><span data-stu-id="46351-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="46351-127">**Skati:** atkarībā no atlasītajām darbībām un konfigurācijas modulī **Izmaksu uzskaite** kartēs tiek rādīta tālāk norādītā informācija.</span><span class="sxs-lookup"><span data-stu-id="46351-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="46351-128">Faktiski pret budžetu (pašreizējais periods)</span><span class="sxs-lookup"><span data-stu-id="46351-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="46351-129">Faktiski pret pārskatīto budžetu (pašreizējais periods)</span><span class="sxs-lookup"><span data-stu-id="46351-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="46351-130">Faktiski pret budžetu (iepriekšējais periods)</span><span class="sxs-lookup"><span data-stu-id="46351-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="46351-131">Faktiski pret pārskatīto budžetu (iepriekšējais periods)</span><span class="sxs-lookup"><span data-stu-id="46351-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="46351-132">Faktiski pret budžetu (no gada sākuma)</span><span class="sxs-lookup"><span data-stu-id="46351-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="46351-133">Faktiski pret pārskatīto budžetu (no gada sākuma)</span><span class="sxs-lookup"><span data-stu-id="46351-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="46351-134">Katrā kartē tiek rādītas šādas summas: Faktiski, Budžets, Novirze un Novirze %.</span><span class="sxs-lookup"><span data-stu-id="46351-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="46351-135">**Saites:**</span><span class="sxs-lookup"><span data-stu-id="46351-135">**Links:**</span></span>

    -   <span data-ttu-id="46351-136">Informācija pašreizējam periodam</span><span class="sxs-lookup"><span data-stu-id="46351-136">Details for current period</span></span>
    -   <span data-ttu-id="46351-137">Informācija iepriekšējam periodam</span><span class="sxs-lookup"><span data-stu-id="46351-137">Details for previous period</span></span>
    -   <span data-ttu-id="46351-138">Informācija līdzšinējam gadam</span><span class="sxs-lookup"><span data-stu-id="46351-138">Details for year to date</span></span>

    <span data-ttu-id="46351-139">Atlasot saiti, katram izmaksu elementam tiek parādīta karte.</span><span class="sxs-lookup"><span data-stu-id="46351-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="46351-140">Katrā kartē tiek rādītas šādas summas: Faktiski, Budžets, Budžeta novirze, Budžeta novirze %, Pārskatītais budžets, Pārskatītā budžeta novirze un Pārskatītā budžeta novirze %.</span><span class="sxs-lookup"><span data-stu-id="46351-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="46351-141">[![Izmaksu elementa karte](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="46351-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="46351-142">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="46351-142">Prerequisites</span></span>
<span data-ttu-id="46351-143">Priekšnosacījumi atšķiras atkarībā no jūsu organizācijai izvietotās Microsoft Dynamics 365 versijas.</span><span class="sxs-lookup"><span data-stu-id="46351-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a><span data-ttu-id="46351-144">Priekšnosacījumi, ja izmantojat Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="46351-144">Prerequisites if you use Microsoft Dynamics 365 Finance</span></span>
<span data-ttu-id="46351-145">Ja jūsu organizācijai ir izvietota programma Finance, sistēmas administratoram ir jāpublicē mobilā darbvieta **Izmaksu kontrolēšana**.</span><span class="sxs-lookup"><span data-stu-id="46351-145">If Finance has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="46351-146">Norādījumus skatiet tēmā [Mobilās darbvietas publicēšana](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="46351-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="46351-147">Priekšnosacījumi, ja izmantojat versiju 1611 ar 3. platformas atjauninājumu vai jaunāku versiju</span><span class="sxs-lookup"><span data-stu-id="46351-147">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="46351-148">Ja jūsu organizācijai ir izvietota versija 1611 ar 3. platformas atjauninājumu vai jaunāku tā versiju, sistēmas administratoram ir jāizpilda tālāk norādītie priekšnoteikumi.</span><span class="sxs-lookup"><span data-stu-id="46351-148">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="46351-149">Priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="46351-149">Prerequisite</span></span></th>
<th><span data-ttu-id="46351-150">Loma</span><span class="sxs-lookup"><span data-stu-id="46351-150">Role</span></span></th>
<th><span data-ttu-id="46351-151">Apraksts</span><span class="sxs-lookup"><span data-stu-id="46351-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46351-152">Ieviesiet KB 4013633.</span><span class="sxs-lookup"><span data-stu-id="46351-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="46351-153">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="46351-153">System administrator</span></span></td>

<td><span data-ttu-id="46351-154">KB 4013633 ir X++ atjauninājums jeb metadatu labojumfails, kurā ir ietverta mobilā darbvieta <strong>Izmaksu kontrolēšana</strong>.</span><span class="sxs-lookup"><span data-stu-id="46351-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="46351-155">Lai ieviestu KB 4013633, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="46351-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="46351-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Lejupielādējiet metadatu labojumfailu no portāla Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="46351-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="46351-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Instalējiet metadatu labojumfailu</a>.</span><span class="sxs-lookup"><span data-stu-id="46351-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="46351-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Izveidojiet izvietojamu pakotni,</a> kas ietver modeli <strong>SCMMobile</strong>, un pēc tam augšupielādējiet izvietojamo pakotni pakalpojumā LCS.</span><span class="sxs-lookup"><span data-stu-id="46351-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="46351-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Lietojiet izvietojamo pakotni</a>.</span><span class="sxs-lookup"><span data-stu-id="46351-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46351-160">Publicējiet mobilo darbvietu <strong>Izmaksu kontrolēšana</strong>.</span><span class="sxs-lookup"><span data-stu-id="46351-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="46351-161">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="46351-161">System administrator</span></span></td>
<td><span data-ttu-id="46351-162">Skatiet tēmu <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobilās darbvietas publicēšana</a>.</span><span class="sxs-lookup"><span data-stu-id="46351-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="46351-163">Mobilās programmas lejupielāde un instalēšana</span><span class="sxs-lookup"><span data-stu-id="46351-163">Download and install the mobile app</span></span>
<span data-ttu-id="46351-164">Mobilās programmas Finance and Operations lejupielāde un instalēšana.</span><span class="sxs-lookup"><span data-stu-id="46351-164">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="46351-165">. Android tālruņiem</span><span class="sxs-lookup"><span data-stu-id="46351-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="46351-166">Tālruņiem iPhone</span><span class="sxs-lookup"><span data-stu-id="46351-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="46351-167">Pierakstīšanās mobilajā programmā</span><span class="sxs-lookup"><span data-stu-id="46351-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="46351-168">Palaidiet programmu savā mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="46351-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="46351-169">Ievadiet savu Dynamics 365 vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="46351-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="46351-170">Pirmajā pierakstīšanās reizē tiek prasīts ievadīt lietotājvārdu un paroli.</span><span class="sxs-lookup"><span data-stu-id="46351-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="46351-171">Ievadiet savus akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="46351-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="46351-172">Pēc pierakstīšanās tiek parādītas jūsu uzņēmumam pieejamās darbvietas.</span><span class="sxs-lookup"><span data-stu-id="46351-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="46351-173">Ņemiet vērā, ka gadījumā, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, jums būs jāatsvaidzina mobilo darbvietu saraksts.</span><span class="sxs-lookup"><span data-stu-id="46351-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="46351-174">[![Velciet, lai atsvaidzinātu](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="46351-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="46351-175">Skatiet sava izmaksu centra veiktspēju, izmantojot mobilo darbvietu Izmaksu kontrole</span><span class="sxs-lookup"><span data-stu-id="46351-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="46351-176">Mobilajā ierīcē atlasiet darbvietu **Izmaksu kontrole**.</span><span class="sxs-lookup"><span data-stu-id="46351-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="46351-177">Atlasiet vienumu **Izmaksu objektu kontrole**.</span><span class="sxs-lookup"><span data-stu-id="46351-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="46351-178">Atlasiet **Darbības**.</span><span class="sxs-lookup"><span data-stu-id="46351-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="46351-179">Atlasiet vienumu **Atlasīt konfigurāciju**, lai atlasītu izmaksu kontroles izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="46351-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="46351-180">Atlasiet **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="46351-180">Select **Done**.</span></span>
6.  <span data-ttu-id="46351-181">Atlasiet **Darbības**.</span><span class="sxs-lookup"><span data-stu-id="46351-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="46351-182">Atlasiet vienumu **Atlasīt izmaksu objektu**, lai atlasītu izmaksu centrus, kuriem jums ir piešķirta piekļuve.</span><span class="sxs-lookup"><span data-stu-id="46351-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="46351-183">Atlasiet **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="46351-183">Select **Done**.</span></span>
9.  <span data-ttu-id="46351-184">Skatiet vispārēju sava izmaksu centra veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="46351-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="46351-185">Atlasiet saiti **Informācija pašreizējam periodam**.</span><span class="sxs-lookup"><span data-stu-id="46351-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="46351-186">Skatiet atsevišķu izmaksu elementu veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="46351-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="46351-187">Varat arī meklēt konkrētus izmaksu elementus.</span><span class="sxs-lookup"><span data-stu-id="46351-187">You can also search for specific cost elements.</span></span>

