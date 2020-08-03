---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 18. februāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 60b46f5bd8f5eeae8aedc9bf81f1e7892caa0c93
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555343"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="053bf-103">Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 18. februāris)</span><span class="sxs-lookup"><span data-stu-id="053bf-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

<span data-ttu-id="053bf-104">Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="053bf-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="053bf-105">Izmaiņas attiecas uz būvējuma numuru 8.1.2903.</span><span class="sxs-lookup"><span data-stu-id="053bf-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="053bf-106">Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.</span><span class="sxs-lookup"><span data-stu-id="053bf-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="053bf-107">Platformas update 32</span><span class="sxs-lookup"><span data-stu-id="053bf-107">Platform update 32</span></span> 

<span data-ttu-id="053bf-108">Platform update 32 tagad ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="053bf-108">Platform update 32 is now available.</span></span> <span data-ttu-id="053bf-109">Plašāku informāciju skatiet [Kas jauns vai mainīts Platform update 32 for Finance and Operations lietotnēs (2020. gada februāris)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span><span class="sxs-lookup"><span data-stu-id="053bf-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="053bf-110">Meklēšanas vērtības tiek saglabātas, kad tiek mainītas skatījuma opcijas racionalizētajā darbinieku veidlapā (383833)</span><span class="sxs-lookup"><span data-stu-id="053bf-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="053bf-111">Jaunā **Darbinieka** veidlapa tagad atceras meklēšanas vērtības, ja maināt skata opcijas un piemērojat izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="053bf-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="053bf-112">Atlīdzības pārvaldības kopsavilkuma elementi priekšskatījuma līdzeklī novirza uz nepareizo veidlapu (401861)</span><span class="sxs-lookup"><span data-stu-id="053bf-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="053bf-113">Fiksētās un mainīgās atlīdzības pārvaldības elementi tagad rāda pareizos ierakstus jaunajā veidlapā **Darbinieks**.</span><span class="sxs-lookup"><span data-stu-id="053bf-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="053bf-114">Attiecas tikai uz racionalizētās darbinieku veidlapas priekšskatījuma līdzekli.</span><span class="sxs-lookup"><span data-stu-id="053bf-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="053bf-115">Varat iespējot šo priekšskatījuma līdzekli **Līdzekļu pārvaldībā**.</span><span class="sxs-lookup"><span data-stu-id="053bf-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="053bf-116">Papildinformāciju skatiet tēmā [Līdzekļu pārvaldība](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="053bf-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a><span data-ttu-id="053bf-117">Tukša statusa lauks dažiem atvaļinājuma pieprasījumu ierakstiem pakalpojumā Common Data Service (414915)</span><span class="sxs-lookup"><span data-stu-id="053bf-117">Empty Status field for some leave request records in Common Data Service (414915)</span></span>

<span data-ttu-id="053bf-118">Šī izmaiņa labo Common Data Service problēmu, kad **Statusa** lauks atvaļinājuma pieprasījumā ir iestatīts uz **Pārskats**.</span><span class="sxs-lookup"><span data-stu-id="053bf-118">This change corrects an issue in Common Data Service when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="053bf-119">Common Data Service tagad ataino statusu.</span><span class="sxs-lookup"><span data-stu-id="053bf-119">Common Data Service now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="053bf-120">Prasmju atbilstību analīze ir iespējama tikai piešķirtajam darbam (411390)</span><span class="sxs-lookup"><span data-stu-id="053bf-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="053bf-121">Tagad varat veikt prasmju atbilstību analīzi par jebkuru darbu, kas definēts Human Resources.</span><span class="sxs-lookup"><span data-stu-id="053bf-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="053bf-122">Sistēmas valūta netiek sinhronizēta no Common Data Service uz Human Resources jaunās vidēs (418011)</span><span class="sxs-lookup"><span data-stu-id="053bf-122">System currency doesn't sync from Common Data Service to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="053bf-123">Sistēmas valūtu Common Data Service tagad var sinhronizēt ar Human Resources.</span><span class="sxs-lookup"><span data-stu-id="053bf-123">The system currency in Common Data Service can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="053bf-124">Priekšskatījumā</span><span class="sxs-lookup"><span data-stu-id="053bf-124">In preview</span></span>

- [<span data-ttu-id="053bf-125">Atvaļinājumu un prombūtnes priekšskatījuma līdzekļi</span><span class="sxs-lookup"><span data-stu-id="053bf-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="053bf-126">Atvieglojumu pārvaldības priekšskatījuma līdzekļi</span><span class="sxs-lookup"><span data-stu-id="053bf-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="053bf-127">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="053bf-127">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="053bf-128">Atjaunināts Common Data Service risinājums</span><span class="sxs-lookup"><span data-stu-id="053bf-128">Updated Common Data Service solution</span></span>

<span data-ttu-id="053bf-129">Jauns Common Data Service risinājums drīzumā būs pieejams ar šādām izmaiņām:</span><span class="sxs-lookup"><span data-stu-id="053bf-129">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="053bf-130">Apraksts</span><span class="sxs-lookup"><span data-stu-id="053bf-130">Description</span></span> | <span data-ttu-id="053bf-131">Labot</span><span class="sxs-lookup"><span data-stu-id="053bf-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="053bf-132">**Darba/amata** elementa izmaiņas</span><span class="sxs-lookup"><span data-stu-id="053bf-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="053bf-133">**Kompensācijas reģions** pievienots</span><span class="sxs-lookup"><span data-stu-id="053bf-133">**Compensation region** added</span></span></br><span data-ttu-id="053bf-134">**Finanšu dimensijas** pievienotas</span><span class="sxs-lookup"><span data-stu-id="053bf-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="053bf-135">**Darbinieka** elementa izmaiņas</span><span class="sxs-lookup"><span data-stu-id="053bf-135">**Worker** entity changes</span></span> | <span data-ttu-id="053bf-136">**Vārdu secība** pievienota</span><span class="sxs-lookup"><span data-stu-id="053bf-136">**Name sequence** added</span></span></br><span data-ttu-id="053bf-137">**Darbi no mājām** pievienoti</span><span class="sxs-lookup"><span data-stu-id="053bf-137">**Works from home** added</span></span></br><span data-ttu-id="053bf-138">**Valoda** pievienota</span><span class="sxs-lookup"><span data-stu-id="053bf-138">**Language** added</span></span></br><span data-ttu-id="053bf-139">**Darba stāža datums** pievienots</span><span class="sxs-lookup"><span data-stu-id="053bf-139">**Seniority date** added</span></span></br><span data-ttu-id="053bf-140">**Gadadienas datums** pievienots</span><span class="sxs-lookup"><span data-stu-id="053bf-140">**Anniversary date** added</span></span></br><span data-ttu-id="053bf-141">**Sākotnējais darbā pieņemšanas datums** pievienots</span><span class="sxs-lookup"><span data-stu-id="053bf-141">**Original hire date** added</span></span> |
| <span data-ttu-id="053bf-142">**Nodarbinātības** elementa izmaiņas</span><span class="sxs-lookup"><span data-stu-id="053bf-142">**Employment** entity changes</span></span> | <span data-ttu-id="053bf-143">**Finanšu dimensijas** pievienotas</span><span class="sxs-lookup"><span data-stu-id="053bf-143">**Financial dimensions** added</span></span></br><span data-ttu-id="053bf-144">**Darba attiecību pārtraukšanas pamatojums** pievienots</span><span class="sxs-lookup"><span data-stu-id="053bf-144">**Termination reason** added</span></span></br><span data-ttu-id="053bf-145">**Beigu datums** pārdēvēts no **Pārejas datuma**</span><span class="sxs-lookup"><span data-stu-id="053bf-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="053bf-146">**Probācijas datums** pievienots</span><span class="sxs-lookup"><span data-stu-id="053bf-146">**Probation date** added</span></span> |
| <span data-ttu-id="053bf-147">**Darbinieka adreses** elementa izmaiņas</span><span class="sxs-lookup"><span data-stu-id="053bf-147">**Worker address** entity changes</span></span> | <span data-ttu-id="053bf-148">**Adrese** pievienota</span><span class="sxs-lookup"><span data-stu-id="053bf-148">**Street address** added</span></span></br><span data-ttu-id="053bf-149">**1. adreses rinda**, **2. adreses rinda** un **3. adreses rinda** atzīmēta norakstīšanai</span><span class="sxs-lookup"><span data-stu-id="053bf-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="053bf-150">Jaunas mainīgās atlīdzības iestatījuma entitījas</span><span class="sxs-lookup"><span data-stu-id="053bf-150">New variable compensation setup entities</span></span> | <span data-ttu-id="053bf-151">**Atlīdzības mainīgā plāna tips**</span><span class="sxs-lookup"><span data-stu-id="053bf-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="053bf-152">**Atlīdzības mainīgā sistēma**</span><span class="sxs-lookup"><span data-stu-id="053bf-152">**Compensation variable plan**</span></span></br><span data-ttu-id="053bf-153">**Izmaksas noteikumi**</span><span class="sxs-lookup"><span data-stu-id="053bf-153">**Vesting rules**</span></span></br><span data-ttu-id="053bf-154">**Atlīdzības mainīgā plāna līmenis**</span><span class="sxs-lookup"><span data-stu-id="053bf-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="053bf-155">Jauna **Darbinieka kalendāra nodarbinātības** entitīja</span><span class="sxs-lookup"><span data-stu-id="053bf-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="053bf-156">**Darba kalendāra elements** pievienots</span><span class="sxs-lookup"><span data-stu-id="053bf-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="053bf-157">Jauna **Algas pozīcijas detalizētas informācijas** entitīja</span><span class="sxs-lookup"><span data-stu-id="053bf-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="053bf-158">**Algas pozīcijas detalizēta informācija** pievienota</span><span class="sxs-lookup"><span data-stu-id="053bf-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="053bf-159">Jauna **Nosaukuma** entitīja</span><span class="sxs-lookup"><span data-stu-id="053bf-159">New **Title** entity</span></span> | <span data-ttu-id="053bf-160">**Nosaukums** pievienots.</span><span class="sxs-lookup"><span data-stu-id="053bf-160">**Title** added.</span></span> <span data-ttu-id="053bf-161">Jaunais elements **Nosaukums** tiks iekļauts sinhronizācijas procesā starp Human Resources un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="053bf-161">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="053bf-162">Tam nebūs sākotnējas atsauces no entitījām **Amats** vai **Darbs**.</span><span class="sxs-lookup"><span data-stu-id="053bf-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="053bf-163">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="053bf-163">See also</span></span>

[<span data-ttu-id="053bf-164">Jaunumi un izmaiņas programmā Human Resources</span><span class="sxs-lookup"><span data-stu-id="053bf-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="053bf-165">Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu</span><span class="sxs-lookup"><span data-stu-id="053bf-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="053bf-166">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="053bf-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="053bf-167">Līdzekļu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="053bf-167">Manage features</span></span>](hr-admin-manage-features.md)