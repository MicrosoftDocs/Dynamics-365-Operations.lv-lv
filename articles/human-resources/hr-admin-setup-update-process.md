---
title: Procesa atjaunināšana
description: Microsoft Dynamics 365 Human Resources ir īsts programmatūras pakalpojums (software as a service — SaaS), kas nodrošina nepārtrauktus, bezkontakta pakalpojumu atjauninājumus lietojumprogrammu un platformu izmaiņām.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 267682f4497bacf70f93840a948d0e525dfa4aa1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092205"
---
# <a name="update-process"></a><span data-ttu-id="76ca0-103">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="76ca0-103">Update process</span></span>

<span data-ttu-id="76ca0-104">Microsoft Dynamics 365 Human Resources ir īsts programmatūras pakalpojums (software as a service — SaaS), kas nodrošina nepārtrauktus, bezkontakta pakalpojumu atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="76ca0-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="76ca0-105">Šie atjauninājumi ietver gan programmas, gan platformas izmaiņas, kas bieži sniedz būtiskus pakalpojuma uzlabojumus, ieskaitot regulējošos atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="76ca0-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="76ca0-106">Atjaunināšanas politika</span><span class="sxs-lookup"><span data-stu-id="76ca0-106">Update policy</span></span>

<span data-ttu-id="76ca0-107">Atjauninājumi tiek izlaisti ar regulāru kadenci visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="76ca0-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="76ca0-108">Human Resources atbalsts tiek nodrošināts saskaņā ar [Microsoft Lifecycle politiku](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kas nodrošina pastāvīgas un prognozējamas vadlīnijas atbalsta pieejamībai.</span><span class="sxs-lookup"><span data-stu-id="76ca0-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="76ca0-109">Laidienu kadence</span><span class="sxs-lookup"><span data-stu-id="76ca0-109">Release cadence</span></span>

<span data-ttu-id="76ca0-110">Human Resources atjauninājumi tiek automātiski piemēroti visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="76ca0-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="76ca0-111">Human Resources nodrošina divu veidu laidienus.</span><span class="sxs-lookup"><span data-stu-id="76ca0-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="76ca0-112">**Pakalpojuma atjauninājumi**: iknedēļas atjauninājumi, kas ietver kļūdu labojumus un jaunus līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="76ca0-112">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="76ca0-113">Pakalpojuma atjauninājumi iekļauj arī noderīgus platformas atjauninājumus, kad tie tiek izlaisti.</span><span class="sxs-lookup"><span data-stu-id="76ca0-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="76ca0-114">Lai iegūtu priekšstatu par to, kad tiek izlaisti platformas atjauninājumi, skatiet [3. tabula: platformas laidieni](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="76ca0-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="76ca0-115">Iknedēļas atjauninājumi parasti tiek izlaisti trešdienās.</span><span class="sxs-lookup"><span data-stu-id="76ca0-115">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="76ca0-116">Papildinformāciju par iknedēļas atjauninājumiem skatiet [Jaunumi un izmaiņas Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span><span class="sxs-lookup"><span data-stu-id="76ca0-116">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="76ca0-117">Visi atbalstītie datu centri tiek atjaunināti katru nedēļu, ja vien nav norādīts citādi.</span><span class="sxs-lookup"><span data-stu-id="76ca0-117">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="76ca0-118">Iknedēļas atjauninājumi parasti sākas trešdien un tiek pabeigti līdz svētdienai.</span><span class="sxs-lookup"><span data-stu-id="76ca0-118">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="76ca0-119">Iknedēļas atjauninājumos ir ietverti ASV, Austrālijas, Eiropas, Apvienotās Karalistes, Āzijas un Kanādas reģioni.</span><span class="sxs-lookup"><span data-stu-id="76ca0-119">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="76ca0-120">**Common Data Service risinājuma atjauninājumi**: šie atjauninājumi pēc nepieciešamības parādās aptuveni ik pēc sešām nedēļām.</span><span class="sxs-lookup"><span data-stu-id="76ca0-120">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="76ca0-121">Tie ietver jaunus elementus un izmaiņas esošajos elementos Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="76ca0-121">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="76ca0-122">Šie atjauninājumi tiek izlaisti tiem pašiem reģioniem kā iknedēļas atjauninājumi, un paiet aptuveni sešas nedēļas līdz tie tiek kopēti visos datu centros.</span><span class="sxs-lookup"><span data-stu-id="76ca0-122">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="76ca0-123">Risinājumu atjauninājumi var būt vai var nebūt saskaņoti ar iknedēļas pakalpojumu atjauninājumiem.</span><span class="sxs-lookup"><span data-stu-id="76ca0-123">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="76ca0-124">Tālāk redzamajā tabulā ir parādīts grafika paraugs.</span><span class="sxs-lookup"><span data-stu-id="76ca0-124">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="76ca0-125">Nedēļa</span><span class="sxs-lookup"><span data-stu-id="76ca0-125">Week</span></span> | <span data-ttu-id="76ca0-126">Labošanas tips</span><span class="sxs-lookup"><span data-stu-id="76ca0-126">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="76ca0-127">1.</span><span class="sxs-lookup"><span data-stu-id="76ca0-127">1</span></span> | <span data-ttu-id="76ca0-128">Pakalpojuma atjauninājums (visi reģioni)</span><span class="sxs-lookup"><span data-stu-id="76ca0-128">Service update (all regions)</span></span> |
| <span data-ttu-id="76ca0-129">2.</span><span class="sxs-lookup"><span data-stu-id="76ca0-129">2</span></span> | <span data-ttu-id="76ca0-130">Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (1. nedēļas reģioni)</span><span class="sxs-lookup"><span data-stu-id="76ca0-130">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="76ca0-131">3</span><span class="sxs-lookup"><span data-stu-id="76ca0-131">3</span></span> | <span data-ttu-id="76ca0-132">Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (2. nedēļas reģioni)</span><span class="sxs-lookup"><span data-stu-id="76ca0-132">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="76ca0-133">4.</span><span class="sxs-lookup"><span data-stu-id="76ca0-133">4</span></span> | <span data-ttu-id="76ca0-134">Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (3. nedēļas reģioni)</span><span class="sxs-lookup"><span data-stu-id="76ca0-134">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="76ca0-135">5</span><span class="sxs-lookup"><span data-stu-id="76ca0-135">5</span></span> | <span data-ttu-id="76ca0-136">Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (4. nedēļas reģioni)</span><span class="sxs-lookup"><span data-stu-id="76ca0-136">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="76ca0-137">6</span><span class="sxs-lookup"><span data-stu-id="76ca0-137">6</span></span> | <span data-ttu-id="76ca0-138">Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (5. nedēļas reģioni)</span><span class="sxs-lookup"><span data-stu-id="76ca0-138">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="76ca0-139">7</span><span class="sxs-lookup"><span data-stu-id="76ca0-139">7</span></span> | <span data-ttu-id="76ca0-140">Pakalpojuma atjauninājums (visi reģioni) + risinājuma atjauninājums (6. nedēļas reģioni)</span><span class="sxs-lookup"><span data-stu-id="76ca0-140">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="76ca0-141">8</span><span class="sxs-lookup"><span data-stu-id="76ca0-141">8</span></span> | <span data-ttu-id="76ca0-142">Pakalpojuma atjauninājums (visi reģioni)</span><span class="sxs-lookup"><span data-stu-id="76ca0-142">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="76ca0-143">Kad tie tiek izlaisti, risinājuma atjauninājumi ir pieejami visiem datu centriem.</span><span class="sxs-lookup"><span data-stu-id="76ca0-143">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="76ca0-144">Ja nevēlaties gaidīt, kamēr atjauninājumi tiek kopēti automātiski, varat lietot šos atjauninājumus manuāli jebkurā vidē jebkurā datu centrā.</span><span class="sxs-lookup"><span data-stu-id="76ca0-144">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="76ca0-145">Ja nepieciešams, Human Resources nodrošina arī tālāk minētos labojumu veidus.</span><span class="sxs-lookup"><span data-stu-id="76ca0-145">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="76ca0-146">**Pārstrādātais izdevums (labojumfails**): kļūdu labojumi, kas var būt vai nu kopā ar iknedēļas pakalpojuma atjaunināšanas laidienu, vai atsevišķi no tā</span><span class="sxs-lookup"><span data-stu-id="76ca0-146">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="76ca0-147">**Ārkārtas labojums**: proaktīvi un reaktīvi labojumfaili, kas ir pēc būtības ir paši par sevi, var ietvert tikai konfigurācijas vai koda izmaiņas, lai atrisinātu tiešsaistes vietnes problēmas, un tie var būt atsevišķi no iknedēļas pakalpojuma atjaunināšanas laidiena</span><span class="sxs-lookup"><span data-stu-id="76ca0-147">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="76ca0-148">Laidieni tiek pārbaudīti, testēti un apstiprināti iekšējā vidē.</span><span class="sxs-lookup"><span data-stu-id="76ca0-148">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="76ca0-149">Pēc izveidotā ir izrakstīšanas, tas tiek izvietots ražošanā.</span><span class="sxs-lookup"><span data-stu-id="76ca0-149">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="76ca0-150">Izņēmumi 2019. gadā</span><span class="sxs-lookup"><span data-stu-id="76ca0-150">Exceptions in 2019</span></span>

<span data-ttu-id="76ca0-151">Tālāk minētie datumi ir izņēmumi no regulāro laidienu grafika.</span><span class="sxs-lookup"><span data-stu-id="76ca0-151">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="76ca0-152">Datums</span><span class="sxs-lookup"><span data-stu-id="76ca0-152">Date</span></span> | <span data-ttu-id="76ca0-153">Apraksts</span><span class="sxs-lookup"><span data-stu-id="76ca0-153">Description</span></span> |
| --- | --- |
| <span data-ttu-id="76ca0-154">25. novembra nedēļa</span><span class="sxs-lookup"><span data-stu-id="76ca0-154">Week of November 25</span></span> | <span data-ttu-id="76ca0-155">Nav atjauninājumu</span><span class="sxs-lookup"><span data-stu-id="76ca0-155">No updates</span></span> |
| <span data-ttu-id="76ca0-156">16. decembra nedēļa</span><span class="sxs-lookup"><span data-stu-id="76ca0-156">Week of December 16</span></span> | <span data-ttu-id="76ca0-157">Tikai mazsvarīgi atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="76ca0-157">Minor updates only</span></span> |
| <span data-ttu-id="76ca0-158">23. decembra nedēļa</span><span class="sxs-lookup"><span data-stu-id="76ca0-158">Week of December 23</span></span> | <span data-ttu-id="76ca0-159">Nav atjauninājumu</span><span class="sxs-lookup"><span data-stu-id="76ca0-159">No updates</span></span> |
| <span data-ttu-id="76ca0-160">30. decembra nedēļa</span><span class="sxs-lookup"><span data-stu-id="76ca0-160">Week of December 30</span></span> | <span data-ttu-id="76ca0-161">Nav atjauninājumu</span><span class="sxs-lookup"><span data-stu-id="76ca0-161">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="76ca0-162">Komunikācija</span><span class="sxs-lookup"><span data-stu-id="76ca0-162">Communications</span></span>

<span data-ttu-id="76ca0-163">Tālāk minētajās vietās varat uzzināt, kas ietverts Human Resources darbībā un kādi bijuši laidieni.</span><span class="sxs-lookup"><span data-stu-id="76ca0-163">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="76ca0-164">Dynamics 365 Human Resources rīcības plāns</span><span class="sxs-lookup"><span data-stu-id="76ca0-164">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="76ca0-165">Dynamics 365 laidiena plāni</span><span class="sxs-lookup"><span data-stu-id="76ca0-165">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="76ca0-166">Jaunumi un izmaiņas Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="76ca0-166">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="76ca0-167">[Problēmu meklēšana Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (tikai ar platformu saistītām kļūdām)</span><span class="sxs-lookup"><span data-stu-id="76ca0-167">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="76ca0-168">Human Resources emuārs</span><span class="sxs-lookup"><span data-stu-id="76ca0-168">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="76ca0-169">Human Resources Yammer kopiena</span><span class="sxs-lookup"><span data-stu-id="76ca0-169">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="76ca0-170">Priekšskatījuma līdzekļi smilškastes vidē</span><span class="sxs-lookup"><span data-stu-id="76ca0-170">Preview features in a sandbox environment</span></span>

<span data-ttu-id="76ca0-171">Varat validēt priekšskatījuma līdzekļus smilškastes vidē pirms iespējot tos savā ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="76ca0-171">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="76ca0-172">Papildinformāciju par jaunu līdzekļu iespējošanu skatiet [Pārskats par līdzekļu pārvaldību](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="76ca0-172">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="76ca0-173">Visi jaunie līdzekļi paliek priekšskatījumā vismaz 30 dienas, un parasti 30-60 dienas.</span><span class="sxs-lookup"><span data-stu-id="76ca0-173">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="76ca0-174">Galvenās funkcijas parasti ir pieejamas katra gada oktobrī un aprīlī pēc priekšskatījuma perioda.</span><span class="sxs-lookup"><span data-stu-id="76ca0-174">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="76ca0-175">Tiklīdz jūs redzat jaunas iespējas Līdzekļu pārvaldības darbvietā, varat tās ieslēgt.</span><span class="sxs-lookup"><span data-stu-id="76ca0-175">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="76ca0-176">Daži līdzekļi var būt ieslēgti pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="76ca0-176">Some features may be on by default.</span></span>

<span data-ttu-id="76ca0-177">Reizēm šis līdzeklis būs ieslēgts pēc noklusējuma, un to nevar izslēgt (piemēram, Līdzekļu pārvaldības darbvieta).</span><span class="sxs-lookup"><span data-stu-id="76ca0-177">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="76ca0-178">Kolīdz līdzeklis ir vispārīgi pieejams, to var ieslēgt vai izslēgt ražošanas vidēs.</span><span class="sxs-lookup"><span data-stu-id="76ca0-178">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="76ca0-179">Līdzekļu pārvaldības darbvieta norāda, kad priekšskatījuma līdzeklis kļūs obligāts.</span><span class="sxs-lookup"><span data-stu-id="76ca0-179">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="76ca0-180">Šis datums parasti ir 1. oktobris vai 1. aprīlis, lai to saskaņotu ar pusgada laidiena plāniem.</span><span class="sxs-lookup"><span data-stu-id="76ca0-180">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="76ca0-181">Jūs nevarat izslēgt obligātos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="76ca0-181">You can't turn off mandatory features.</span></span> <span data-ttu-id="76ca0-182">Kamēr tas kļūst obligāts, varat ieslēgt vai izslēgt līdzekli visās vidēs.</span><span class="sxs-lookup"><span data-stu-id="76ca0-182">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="76ca0-183">Mēs noteikti iesakām priekšskatīt līdzekļus smilškastes vai izmēģinājuma vidē.</span><span class="sxs-lookup"><span data-stu-id="76ca0-183">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="76ca0-184">Ir ieteicams izveidot pašreizējās ražošanas vides vai datu bāzes kopiju smilškastes vidē, lai varētu iegūt pilnīgu pieredzi ar jaunajiem līdzekļiem, izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="76ca0-184">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="76ca0-185">Papildinformāciju par smilškastes vides nodrošināšanu skatiet [Human Resources projekta nodrošināšana](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="76ca0-185">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="76ca0-186">Lai noņemtu testa vidi, skatiet [Instances noņemšana](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="76ca0-186">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="76ca0-187">Pārskata sniegšana par kļūdām</span><span class="sxs-lookup"><span data-stu-id="76ca0-187">Report bugs</span></span>

<span data-ttu-id="76ca0-188">Testējot priekšskatījuma līdzekļus vai izmēģinot jaunas iespējas, iespējams, atradīsiet vienumus, kas nedarbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="76ca0-188">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="76ca0-189">Lūdzu, sniedziet pārskatu par jebkurām kļūdām, izmantojot [Microsoft Dynamics 365 atbalstu](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="76ca0-189">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="76ca0-190">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="76ca0-190">See also</span></span>

- [<span data-ttu-id="76ca0-191">Dynamics 365 un Power Platform laidiena plāni</span><span class="sxs-lookup"><span data-stu-id="76ca0-191">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="76ca0-192">Jaunumi un izmaiņas Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="76ca0-192">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="76ca0-193">Programmatūras dzīves cikla politika</span><span class="sxs-lookup"><span data-stu-id="76ca0-193">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

