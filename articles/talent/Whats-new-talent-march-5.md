---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 5. marts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fe24846ab98a75d474df045a62a72bfc41c64866
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741894"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a><span data-ttu-id="1582e-103">Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 5. marts)</span><span class="sxs-lookup"><span data-stu-id="1582e-103">What's new or changed in Dynamics 365 for Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1582e-104">Šajā tēmā ir aprakstīti jaunie vai izmainītie programmas Talent līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="1582e-104">This topic describes features that are either new or changed in Talent</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="1582e-105">Izmaiņas programmā Attract</span><span class="sxs-lookup"><span data-stu-id="1582e-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="1582e-106">Opciju kopu paplašināšana programmā Attract</span><span class="sxs-lookup"><span data-stu-id="1582e-106">Extending option sets in Attract</span></span>

<span data-ttu-id="1582e-107">Programmā Attract ir vairāki lauki, kas ir opciju kopas pakalpojumā Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1582e-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="1582e-108">Ir ieviestas jaunas iespējas, lai paplašinātu opciju kopas, tostarp lauks **Noraidīšanas pamatojums**, lauks **Nodarbinātības veids** un lauks **Darba stāža veids**.</span><span class="sxs-lookup"><span data-stu-id="1582e-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1582e-109">Lai izmantotu darba publicēšanas pakalpojumā LinkedIn funkcionalitāti, ir jāizmanto lauki **Nodarbinātības veids** un **Darba stāžs veids** lapā **Darba informācija**.</span><span class="sxs-lookup"><span data-stu-id="1582e-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="1582e-110">Šo lauku noklusējuma vērtības nodrošina pakalpojums LinkedIn, un tās tiek rādītas, kad darbs tiek publicēts.</span><span class="sxs-lookup"><span data-stu-id="1582e-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="1582e-111">Ja publicējat darbus pakalpojumā LinkedIn un izmaināt šo lauku esošās opciju kopas vērtības, darbs joprojām tiek publicēts, taču pakalpojumā LinkedIn netiek parādītas pielāgotās lauku **Nodarbinātības veids** un **Darba stāža veids** vērtības.</span><span class="sxs-lookup"><span data-stu-id="1582e-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="1582e-112">Izmaiņas pievienošanas procesā</span><span class="sxs-lookup"><span data-stu-id="1582e-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="1582e-113">Pievienošanas darba grupu privāts priekšskatījums</span><span class="sxs-lookup"><span data-stu-id="1582e-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="1582e-114">Tagad varat viegli kopīgot veidnes un sadarboties to izmantošanā visā savā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="1582e-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="1582e-115">Papildinformāciju skatiet rakstā [Dalīšanās ar labākās prakses piemēriem savā organizācijā, izmantojot pievienošanas darba grupas](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="1582e-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="1582e-116">Uzdevumu veicēju vietturu privāts priekšskatījums</span><span class="sxs-lookup"><span data-stu-id="1582e-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="1582e-117">Varat paplašināt savas veidnes, piešķirot aktivitātes lomām, nevis personām.</span><span class="sxs-lookup"><span data-stu-id="1582e-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="1582e-118">Pēc tam lomas tiek piešķirtas personām ceļveža izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="1582e-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="1582e-119">Papildinformāciju skatiet rakstā [Ceļvežu administrēšanas racionalizācija, piešķirot aktivitātes lomām](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="1582e-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="1582e-120">Izmaiņas programmā Core HR</span><span class="sxs-lookup"><span data-stu-id="1582e-120">Changes in Core HR</span></span>
<span data-ttu-id="1582e-121">**8.1.2178 būvējums**</span><span class="sxs-lookup"><span data-stu-id="1582e-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="1582e-122">Darbplūsmas konfigurēšana automātiskai pieprasījuma apstiprināšanai vai darbplūsmas izpildei, ja personāla vadības speciālists vai rindas vadītājs iesniedz vai atjaunina brīvā laika pieprasījumus</span><span class="sxs-lookup"><span data-stu-id="1582e-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="1582e-123">Ir pievienoti jauni darbplūsmas nosacījumi, kas sniedz iespēju automātiski apstiprināt brīvā laika pieprasījumus, ja tos ir iesniedzis darbinieka vadītājs vai personāla vadības speciālists.</span><span class="sxs-lookup"><span data-stu-id="1582e-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="1582e-124">Viens veids, kā darbplūsmā panākt šo automātisko apstiprināšanu, ir iespējot automātisku darbību, ko aktivizē darbplūsmas apstiprināšana.</span><span class="sxs-lookup"><span data-stu-id="1582e-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="1582e-125">Tālāk ir norādīti pievienotie nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="1582e-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="1582e-126">Iesniedza — tiek izmantots, lai novērtētu tā sistēmas lietotāja ID, kurš ir iesniedzis pieprasījumu darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="1582e-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="1582e-127">Kā vārdā iesniegts — tiek izmantots, lai novērtētu to, vai prombūtnes pieprasījums ir ticis iesniegts ar pieprasījumu saistītā nodarbinātā vārdā.</span><span class="sxs-lookup"><span data-stu-id="1582e-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="1582e-128">Iesniedzis personāla vadības speciālists — tiek izmantots, lai novērtētu to, vai sistēmas lietotājam, kurš ir iesniedzis pieprasījumu darbplūsmai, ir piešķirta personāla vadības speciālista loma.</span><span class="sxs-lookup"><span data-stu-id="1582e-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="1582e-129">Iesniedzis vadītājs — tiek izmantots, lai novērtētu to, vai lietotājs, kurš ir iesniedzis brīvā laika pieprasījumu darbplūsmai, ir ar pieprasījumu saistītā darbinieka vadītājs rindas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="1582e-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="1582e-130">Fiksētas atlīdzības iespējošana darbiniekiem ar gaidāmām amatu piešķirēm</span><span class="sxs-lookup"><span data-stu-id="1582e-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="1582e-131">Bieži vien darbinieki pievienojas organizācijai ar vēlāku sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="1582e-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="1582e-132">Šīs izmaiņas sniedz iespēju definēt fiksētu atlīdzību darbiniekiem, kuriem ir gaidāmas amatu piešķires.</span><span class="sxs-lookup"><span data-stu-id="1582e-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="1582e-133">Tukši amata algas lauki amata rediģēšanas laikā</span><span class="sxs-lookup"><span data-stu-id="1582e-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="1582e-134">Šīs izmaiņas nodrošina, ka tagad, pierasot esošo amatu izmaiņas, algas laukos pēc noklusējuma tiek norādītas pašreizējās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1582e-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="1582e-135">Citi dažādu kļūdu labojumi</span><span class="sxs-lookup"><span data-stu-id="1582e-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="1582e-136">Šajā laidienā ir ietverti citi nelieli kļūdu labojumi.</span><span class="sxs-lookup"><span data-stu-id="1582e-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="1582e-137">Jaunināšana uz Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1582e-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="1582e-138">Drīz būs pienācis termiņš jaunināšanai uz Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1582e-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="1582e-139">Pierakstieties PowerApps administrēšanas centrā, lai noteiktu, vai jūsu datu bāzi ir nepieciešams jaunināt.</span><span class="sxs-lookup"><span data-stu-id="1582e-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="1582e-140">Papildinformāciju par termiņiem un jaunināšanai nepieciešamajām darbībām skatiet rakstā [Jaunināšana uz Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="1582e-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="1582e-141">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="1582e-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="1582e-142">Papildu atlīdzības drošība (fiksētā un mainīgā)</span><span class="sxs-lookup"><span data-stu-id="1582e-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="1582e-143">Daudzās organizācijās atlīdzības un atvieglojumu pārvaldnieki var piekļūt tikai noteiktiem atlīdzības ierakstiem, piemēram, vadītāju vai reģionālo darbinieku ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="1582e-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="1582e-144">Šīs izmaiņas sniedz iespēju pārvaldīt un uzturēt atlīdzības plānus dažādām darbinieku grupām organizācijā.</span><span class="sxs-lookup"><span data-stu-id="1582e-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="1582e-145">Fiksētajiem un mainīgajiem plāniem var piešķirt drošības lomas, no kurām ir atkarīga piekļuve plāniem un ar tiem saistītajiem darbinieku datiem, piemēram, algu vai prēmiju ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="1582e-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="1582e-146">Šo atlīdzību šiem darbiniekiem var apstrādāt tikai lietotāji, kuriem ir piešķirtas lomas ar konkrētajām piekļuves atļaujām.</span><span class="sxs-lookup"><span data-stu-id="1582e-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24"></a><span data-ttu-id="1582e-147">Platform update 24</span><span class="sxs-lookup"><span data-stu-id="1582e-147">Platform update 24</span></span>
<span data-ttu-id="1582e-148">Papildinformāciju par atjauninājumu Platform update 24 skatiet [Jaunumi un izmaiņas Finance and Operations atjauninājumā Platform update 24 (2019. gada marts)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="1582e-148">For additional details about Platform update 24, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
