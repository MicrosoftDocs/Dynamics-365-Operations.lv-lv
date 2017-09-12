---
title: "Pirkšanas pasūtījuma apstiprināšanas mobilā darbvieta"
description: "Šajā tēmā ir sniegta informācija par pirkšanas pasūtījuma apstiprināšanas mobilo darbvietu, kas ļauj skatīt pirkšanas pasūtījumus un atbilstoši reaģēt ar darbībām. Piemēram, varat apstiprināt vai noraidīt pirkšanas pasūtījumu."
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 12f710caea987dec9a343774f060e7dd7ca03ec4
ms.contentlocale: lv-lv
ms.lasthandoff: 07/18/2017

---

# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="22e99-104">Pirkšanas pasūtījuma apstiprināšanas mobilā darbvieta</span><span class="sxs-lookup"><span data-stu-id="22e99-104">Purchase order approval mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

<span data-ttu-id="22e99-105">Šajā tēmā ir sniegta informācija par mobilo darbvietu **Pirkšanas pasūtījuma apstiprināšana**.</span><span class="sxs-lookup"><span data-stu-id="22e99-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="22e99-106">Šajā darbvietā var apskatīt pirkšanas pasūtījumus un atbilstoši reaģēt ar darbībām.</span><span class="sxs-lookup"><span data-stu-id="22e99-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="22e99-107">Piemēram, varat apstiprināt vai noraidīt pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="22e99-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="22e99-108">Pārskats</span><span class="sxs-lookup"><span data-stu-id="22e99-108">Overview</span></span> 
<span data-ttu-id="22e99-109">Apstiprināmajiem pirkšanas pasūtījumiem ir jāizmanto apstiprināšanas darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="22e99-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="22e99-110">Darbplūsma var ietvert dažādus soļus, kam nepieciešams, lai darbības veic viena vai vairākas personas.</span><span class="sxs-lookup"><span data-stu-id="22e99-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="22e99-111">Piemēram, personai var būt nepieciešams izpildīt uzdevumu vai apstiprināt pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="22e99-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="22e99-112">**Pirkšanas pasūtījuma apstiprināšanas** mobilo darbvietu var viegli apskatīt un atbildēt uz pirkšanas pasūtījumiem no mobilās ierīces.</span><span class="sxs-lookup"><span data-stu-id="22e99-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="22e99-113">Šī darbvieta ļauj arī veikt daļu darbplūsmas darbību, ko var veikt no Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise tīmekļa klientā.</span><span class="sxs-lookup"><span data-stu-id="22e99-113">This workspace also lets you take the same workflow actions that you can take from the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="22e99-114">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="22e99-114">Prerequisites</span></span>
<span data-ttu-id="22e99-115">Priekšnosacījumi atšķiras atkarībā no jūsu organizācijai izvietotās Finance and Operations versijas.</span><span class="sxs-lookup"><span data-stu-id="22e99-115">The prerequisites vary, depending on the version of Finance and Operations that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a><span data-ttu-id="22e99-116">Priekšnosacījumi, ja lietojat Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise 2017. gada jūlija atjauninājumu</span><span class="sxs-lookup"><span data-stu-id="22e99-116">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update</span></span> 
<span data-ttu-id="22e99-117">Ja jūsu organizācijai ir izvietots Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise 2017. gada jūlija atjauninājums, sistēmas administratoram ir jāpublicē **Pirkšanas pasūtījuma apstiprināšana** mobilā darbvieta.</span><span class="sxs-lookup"><span data-stu-id="22e99-117">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="22e99-118">Norādījumus skatiet tēmā [Mobilās darbvietas publicēšana](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="22e99-118">For instructions, see [Publish a mobile workspace](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="22e99-119">Priekšnosacījumi, ja lietojat Microsoft Dynamics 365 for Operations versiju 1611 ar 3. platformas atjauninājumu vai jaunāku tā versiju.</span><span class="sxs-lookup"><span data-stu-id="22e99-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="22e99-120">Ja jūsu organizācija ir izvietota Microsoft Dynamics 365 for Operations versija 1611 ar 3. platformu atjauninājumu vai jaunāku tā versiju, sistēmas administratoram ir jāizpilda tālāk norādītie priekšnoteikumi.</span><span class="sxs-lookup"><span data-stu-id="22e99-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="22e99-121">Priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="22e99-121">Prerequisite</span></span></th>
<th><span data-ttu-id="22e99-122">Loma</span><span class="sxs-lookup"><span data-stu-id="22e99-122">Role</span></span></th>
<th><span data-ttu-id="22e99-123">apraksts</span><span class="sxs-lookup"><span data-stu-id="22e99-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22e99-124">Ieviesiet KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="22e99-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="22e99-125">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="22e99-125">System administrator</span></span></td>
<td><span data-ttu-id="22e99-126">KB 4017918 ir X++ atjauninājums vai metadatu labojumfails, kas ietver mobilo darbvietu <strong>Pirkšanas pasūtījuma apstiprināšana</strong>.</span><span class="sxs-lookup"><span data-stu-id="22e99-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="22e99-127">Lai ieviestu KB 4017918, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="22e99-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="22e99-128"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Lejupielādējiet metadatu labojumfailu no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="22e99-128"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="22e99-129"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</span><span class="sxs-lookup"><span data-stu-id="22e99-129"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="22e99-130"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Izveidojiet izvietojamu pakotni,</a> kas ietver modeli <strong>SCMMobile</strong>, un pēc tam augšupielādējiet izvietojamo pakotni pakalpojumā LCS.</span><span class="sxs-lookup"><span data-stu-id="22e99-130"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="22e99-131"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Lietojiet izvietojamo pakotni</a>.</span><span class="sxs-lookup"><span data-stu-id="22e99-131"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22e99-132">Publicējiet <strong>Pirkšanas pasūtījuma apstiprināšanas</strong> mobilo darbvietu.</span><span class="sxs-lookup"><span data-stu-id="22e99-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="22e99-133">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="22e99-133">System administrator</span></span></td>
<td><span data-ttu-id="22e99-134">Skatiet tēmu <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobilās darbvietas publicēšana</a>.</span><span class="sxs-lookup"><span data-stu-id="22e99-134">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="22e99-135">Mobilās programmas lejupielāde un instalēšana</span><span class="sxs-lookup"><span data-stu-id="22e99-135">Download and install the mobile app</span></span>
<span data-ttu-id="22e99-136">Lejupielādējiet un instalējiet mobilo programmu Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="22e99-136">Download and install the Microsoft Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="22e99-137">Android tālruņiem</span><span class="sxs-lookup"><span data-stu-id="22e99-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="22e99-138">Tālruņiem iPhone</span><span class="sxs-lookup"><span data-stu-id="22e99-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="22e99-139">Pierakstīšanās mobilajā programmā</span><span class="sxs-lookup"><span data-stu-id="22e99-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="22e99-140">Palaidiet programmu savā mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="22e99-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="22e99-141">Ievadiet savu Microsoft Dynamics 365 vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="22e99-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="22e99-142">Pirmajā pierakstīšanās reizē tiek prasīts ievadīt lietotājvārdu un paroli.</span><span class="sxs-lookup"><span data-stu-id="22e99-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="22e99-143">Ievadiet savus akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="22e99-143">Enter your credentials.</span></span>
4. <span data-ttu-id="22e99-144">Pēc pierakstīšanās tiek parādītas jūsu uzņēmumam pieejamās darbvietas.</span><span class="sxs-lookup"><span data-stu-id="22e99-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="22e99-145">Ņemiet vērā, ka gadījumā, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, jums būs jāatsvaidzina mobilo darbvietu saraksts.</span><span class="sxs-lookup"><span data-stu-id="22e99-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Pirkšanas pasūtījuma apstiprināšanas darbvieta pieejamo darbvietu sarakstā](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="22e99-147">Piešķirto pasūtījumu skatīšana</span><span class="sxs-lookup"><span data-stu-id="22e99-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="22e99-148">Mobilajā ierīcē atlasiet darbvietu **Pirkšanas pasūtījuma apstiprināšana**.</span><span class="sxs-lookup"><span data-stu-id="22e99-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="22e99-149">Atlasiet **Man piešķirtie pasūtījumi**, lai skatītu visus pirkšanas pasūtījumus, saistībā ar kuriem jums ir uzdots veikt darbības pirkšanas pasūtījuma apstiprināšanas darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="22e99-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="22e99-150">Atlasiet pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="22e99-150">Select an order.</span></span> <span data-ttu-id="22e99-151">Lapā **Pasūtījumu informācija** redzēsit pasūtījuma virsraksta informāciju un rindas.</span><span class="sxs-lookup"><span data-stu-id="22e99-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="22e99-152">Norādījumus varat atrast arī darbplūsmas uzdevumā.</span><span class="sxs-lookup"><span data-stu-id="22e99-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="22e99-153">Atlasiet **Uzskaites sadale**, lai atvērtu lapu **Virsraksta uzskaites sadale**.</span><span class="sxs-lookup"><span data-stu-id="22e99-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="22e99-154">Atgriezieties lapā **Pasūtījuma informācija** un atlasiet rindu.</span><span class="sxs-lookup"><span data-stu-id="22e99-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="22e99-155">No pasūtījuma rindas informācijas var pārlūkot arī līniju uzskaites sadales.</span><span class="sxs-lookup"><span data-stu-id="22e99-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="22e99-156">Darbības izpilde no pirkšanas pasūtījuma</span><span class="sxs-lookup"><span data-stu-id="22e99-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="22e99-157">Pēc tam, kad apskatījāt pirkšanas pasūtījumu, kas jums ir piešķirts, un izlasījāt darbplūsmas instrukcijas, jums jābūt gataviem izpildīt darbību.</span><span class="sxs-lookup"><span data-stu-id="22e99-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="22e99-158">Mobilajā ierīcē atlasiet darbvietu **Pirkšanas pasūtījuma apstiprināšana**.</span><span class="sxs-lookup"><span data-stu-id="22e99-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="22e99-159">Atlasiet **Man piešķirtie pasūtījumi**, lai skatītu visus pirkšanas pasūtījumus, saistībā ar kuriem jums ir uzdots veikt darbības pirkšanas pasūtījuma apstiprināšanas darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="22e99-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="22e99-160">Atlasiet pasūtījumu un skatiet detalizētas informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="22e99-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="22e99-161">Atlasiet vienumu **Darbības**, lai parādītu pieejamās darbības.</span><span class="sxs-lookup"><span data-stu-id="22e99-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="22e99-162">Pieejamās darbības ir atkarīgas no uzdevuma, kas jums ir piešķirts.</span><span class="sxs-lookup"><span data-stu-id="22e99-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="22e99-163">Uzdevuma darbības</span><span class="sxs-lookup"><span data-stu-id="22e99-163">Task action</span></span>    | <span data-ttu-id="22e99-164">Apstiprināšanas darbība</span><span class="sxs-lookup"><span data-stu-id="22e99-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="22e99-165">Aizpildīt</span><span class="sxs-lookup"><span data-stu-id="22e99-165">Complete</span></span>       | <span data-ttu-id="22e99-166">Akceptēt</span><span class="sxs-lookup"><span data-stu-id="22e99-166">Approve</span></span>          |
    | <span data-ttu-id="22e99-167">Atgrieztais</span><span class="sxs-lookup"><span data-stu-id="22e99-167">Return</span></span>         | <span data-ttu-id="22e99-168">Noraidīt</span><span class="sxs-lookup"><span data-stu-id="22e99-168">Reject</span></span>           |
    | <span data-ttu-id="22e99-169">Pieprasīt izmaiņas</span><span class="sxs-lookup"><span data-stu-id="22e99-169">Request change</span></span> | <span data-ttu-id="22e99-170">Pieprasīt izmaiņas</span><span class="sxs-lookup"><span data-stu-id="22e99-170">Request change</span></span>   |
    | <span data-ttu-id="22e99-171">Deleģēšana</span><span class="sxs-lookup"><span data-stu-id="22e99-171">Delegate</span></span>       | <span data-ttu-id="22e99-172">Deleģēšana</span><span class="sxs-lookup"><span data-stu-id="22e99-172">Delegate</span></span>         |

5. <span data-ttu-id="22e99-173">Atlasīt atbilstošu darbību.</span><span class="sxs-lookup"><span data-stu-id="22e99-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="22e99-174">Lapā **Uzdevuma izpilde** ievadiet komentāru.</span><span class="sxs-lookup"><span data-stu-id="22e99-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="22e99-175">Ņemiet vērā! Atlasot darbību **Deleģēt**, ir jāatlasa lietotājs, kam deleģēt uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="22e99-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="22e99-176">Atlasiet **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="22e99-176">Select **Done**.</span></span> <span data-ttu-id="22e99-177">Pēc darbvietas atsvaidzināšanas pirkšanas pasūtījums vairs nebūs jūsu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="22e99-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 

