---
title: Procesa atjaunināšana
description: Microsoft Dynamics 365 Human Resources ir īsts programmatūras pakalpojums (software as a service — SaaS), kas nodrošina nepārtrauktus, bezkontakta pakalpojumu atjauninājumus lietojumprogrammu un platformu izmaiņām.
author: andreabichsel
manager: tfehr
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bb5f7dc17c8f4f3a54bd285cb55088f2176db4a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113383"
---
# <a name="update-process"></a><span data-ttu-id="d5fc3-103">Procesa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="d5fc3-103">Update process</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d5fc3-104">Microsoft Dynamics 365 Human Resources ir īsts programmatūras pakalpojums (software as a service — SaaS), kas nodrošina nepārtrauktus, bezkontakta pakalpojumu atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="d5fc3-105">Šie atjauninājumi ietver gan programmas, gan platformas izmaiņas, kas bieži sniedz būtiskus pakalpojuma uzlabojumus, ieskaitot regulējošos atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="d5fc3-106">Atjaunināšanas politika</span><span class="sxs-lookup"><span data-stu-id="d5fc3-106">Update policy</span></span>

<span data-ttu-id="d5fc3-107">Atjauninājumi tiek izlaisti ar regulāru kadenci visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="d5fc3-108">Human Resources atbalsts tiek nodrošināts saskaņā ar [Microsoft Lifecycle politiku](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kas nodrošina pastāvīgas un prognozējamas vadlīnijas atbalsta pieejamībai.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="d5fc3-109">Laidienu kadence</span><span class="sxs-lookup"><span data-stu-id="d5fc3-109">Release cadence</span></span> 

<span data-ttu-id="d5fc3-110">Human Resources atjauninājumi tiek automātiski piemēroti visām vidēm.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="d5fc3-111">Human Resources nodrošina divu veidu laidienus.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="d5fc3-112">**Pakalpojuma atjauninājumi**: Atjauninājumi tiek veikti reizi divās nedēļās un ietver kļūdu labojumus un jaunus līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="d5fc3-113">Pakalpojuma atjauninājumi iekļauj arī noderīgus platformas atjauninājumus, kad tie tiek izlaisti.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="d5fc3-114">Lai iegūtu priekšstatu par to, kad tiek izlaisti platformas atjauninājumi, skatiet [3. tabula: platformas laidieni](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="d5fc3-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="d5fc3-115">Atjauninājumiem, kas tiek veikti reizi divās nedēļās, ir pakāpeniska globāla izlaišana reģionos.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="d5fc3-116">Papildinformāciju par atjauninājumiem reizi divās nedēļās skatiet [Jaunumi un izmaiņas Dynamics 365 Human Resources](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="d5fc3-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="d5fc3-117">Visi atbalstītie datu centri tiek atjaunināti ik pēc divām nedēļām, ja vien nav norādīts citādi.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="d5fc3-118">Atjauninājumos, kas notiek reizi divās nedēļās, ir ietverti ASV, Austrālijas, Eiropas, Apvienotās Karalistes, Āzijas un Kanādas reģioni.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="d5fc3-119">**Dataverse risinājuma atjauninājumi**: šie atjauninājumi pēc nepieciešamības parādās aptuveni ik pēc sešām nedēļām.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="d5fc3-120">Tie ietver jaunus elementus un izmaiņas esošajos elementos Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="d5fc3-121">Šie atjauninājumi tiek izlaisti tiem pašiem reģioniem kā atjauninājumi reizi divās nedēļās, un paiet aptuveni sešas nedēļas līdz tie tiek kopēti visos datu centros.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="d5fc3-122">Risinājumu atjauninājumi var būt vai var nebūt saskaņoti ar pakalpojumu atjauninājumiem reizi divās nedēļās.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="d5fc3-123">Kad tie tiek izlaisti, risinājuma atjauninājumi ir pieejami visiem datu centriem.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="d5fc3-124">Ja nevēlaties gaidīt, kamēr atjauninājumi tiek kopēti automātiski, varat lietot šos atjauninājumus manuāli jebkurā vidē jebkurā datu centrā.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="d5fc3-125">Ja nepieciešams, Human Resources nodrošina arī tālāk minētos labojumu veidus.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="d5fc3-126">**Pārstrādātais izdevums (labojumfails**): Kļūdu labojumi, kas var būt vai nu kopā ar pakalpojuma atjaunināšanas, kas notiek reizi divās nedēļās, laidienu, vai atsevišķi no tā</span><span class="sxs-lookup"><span data-stu-id="d5fc3-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="d5fc3-127">**Ārkārtas labojums**: Proaktīvi un reaktīvi labojumfaili, kas ir pēc būtības ir paši par sevi, var ietvert tikai konfigurācijas vai koda izmaiņas, lai atrisinātu tiešsaistes vietnes problēmas, un tie var būt atsevišķi no iknedēļas pakalpojuma atjaunināšanas, kas notiek reizi divās nedēļās, laidiena</span><span class="sxs-lookup"><span data-stu-id="d5fc3-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="d5fc3-128">Laidieni tiek pārbaudīti, testēti un apstiprināti iekšējā vidē.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="d5fc3-129">Pēc izveidotā ir izrakstīšanas, tas tiek izvietots ražošanā.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="d5fc3-130">Laidienu ritma izņēmumi 2020. gadā</span><span class="sxs-lookup"><span data-stu-id="d5fc3-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="d5fc3-131">Lai uzskaitītu brīvdienas, 2020. gada novembra un decembra izlaišanas grafiks ir šāds:</span><span class="sxs-lookup"><span data-stu-id="d5fc3-131">To account for holidays, the release schedule for November and December 2020 is as follows:</span></span>

- <span data-ttu-id="d5fc3-132">Novembra izlaidums: 2. novembris - 13. novembris</span><span class="sxs-lookup"><span data-stu-id="d5fc3-132">November release: November 2 - November 13</span></span>
- <span data-ttu-id="d5fc3-133">Decembra izlaidums: 30. novembris - 11. decembris</span><span class="sxs-lookup"><span data-stu-id="d5fc3-133">December release: November 30 - December 11</span></span>
 
<span data-ttu-id="d5fc3-134">Divu nedēļu izlaidumu kadence tiks atsākta kā parasti 2021. gada 11. janvārī.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-134">The two-week release cadence will resume as usual on January 11, 2021.</span></span>

## <a name="communications"></a><span data-ttu-id="d5fc3-135">Komunikācija</span><span class="sxs-lookup"><span data-stu-id="d5fc3-135">Communications</span></span>

<span data-ttu-id="d5fc3-136">Tālāk minētajās vietās varat uzzināt, kas ietverts Human Resources darbībā un kādi bijuši laidieni.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="d5fc3-137">Dynamics 365 Human Resources rīcības plāns</span><span class="sxs-lookup"><span data-stu-id="d5fc3-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="d5fc3-138">Dynamics 365 laidiena plāni</span><span class="sxs-lookup"><span data-stu-id="d5fc3-138">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="d5fc3-139">Jaunumi un izmaiņas Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="d5fc3-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="d5fc3-140">[Problēmu meklēšana Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (tikai ar platformu saistītām kļūdām)</span><span class="sxs-lookup"><span data-stu-id="d5fc3-140">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="d5fc3-141">Human Resources emuārs</span><span class="sxs-lookup"><span data-stu-id="d5fc3-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="d5fc3-142">Human Resources Yammer kopiena</span><span class="sxs-lookup"><span data-stu-id="d5fc3-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="d5fc3-143">Priekšskatījuma līdzekļi smilškastes vidē</span><span class="sxs-lookup"><span data-stu-id="d5fc3-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="d5fc3-144">Varat validēt priekšskatījuma līdzekļus smilškastes vidē pirms iespējot tos savā ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="d5fc3-145">Papildinformāciju par jaunu līdzekļu iespējošanu skatiet [Pārskats par līdzekļu pārvaldību](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="d5fc3-145">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="d5fc3-146">Visi jaunie līdzekļi paliek priekšskatījumā vismaz 30 dienas, un parasti 30-60 dienas.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="d5fc3-147">Galvenās funkcijas parasti ir pieejamas katra gada oktobrī un aprīlī pēc priekšskatījuma perioda.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="d5fc3-148">Tiklīdz jūs redzat jaunas iespējas Līdzekļu pārvaldības darbvietā, varat tās ieslēgt.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="d5fc3-149">Daži līdzekļi var būt ieslēgti pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-149">Some features may be on by default.</span></span>

<span data-ttu-id="d5fc3-150">Reizēm šis līdzeklis būs ieslēgts pēc noklusējuma, un to nevar izslēgt (piemēram, Līdzekļu pārvaldības darbvieta).</span><span class="sxs-lookup"><span data-stu-id="d5fc3-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="d5fc3-151">Kolīdz līdzeklis ir vispārīgi pieejams, to var ieslēgt vai izslēgt ražošanas vidēs.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="d5fc3-152">Līdzekļu pārvaldības darbvieta norāda, kad priekšskatījuma līdzeklis kļūs obligāts.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="d5fc3-153">Šis datums parasti ir 1. oktobris vai 1. aprīlis, lai to saskaņotu ar pusgada laidiena plāniem.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="d5fc3-154">Jūs nevarat izslēgt obligātos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="d5fc3-155">Kamēr tas kļūst obligāts, varat ieslēgt vai izslēgt līdzekli visās vidēs.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="d5fc3-156">Mēs noteikti iesakām priekšskatīt līdzekļus smilškastes vai izmēģinājuma vidē.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="d5fc3-157">Ir ieteicams izveidot pašreizējās ražošanas vides vai datu bāzes kopiju smilškastes vidē, lai varētu iegūt pilnīgu pieredzi ar jaunajiem līdzekļiem, izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="d5fc3-158">Papildinformāciju par smilškastes vides nodrošināšanu skatiet [Human Resources projekta nodrošināšana](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="d5fc3-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="d5fc3-159">Lai noņemtu testa vidi, skatiet [Instances noņemšana](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="d5fc3-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="d5fc3-160">Pārskata sniegšana par kļūdām</span><span class="sxs-lookup"><span data-stu-id="d5fc3-160">Report bugs</span></span>

<span data-ttu-id="d5fc3-161">Testējot priekšskatījuma līdzekļus vai izmēģinot jaunas iespējas, iespējams, atradīsiet vienumus, kas nedarbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="d5fc3-162">Lūdzu, sniedziet pārskatu par jebkurām kļūdām, izmantojot [Microsoft Dynamics 365 atbalstu](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="d5fc3-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="d5fc3-163">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="d5fc3-163">See also</span></span>

[<span data-ttu-id="d5fc3-164">Dynamics 365 un Power Platform laidiena plāni</span><span class="sxs-lookup"><span data-stu-id="d5fc3-164">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="d5fc3-165">Jaunumi un izmaiņas Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="d5fc3-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d5fc3-166">Programmatūras dzīves cikla politika</span><span class="sxs-lookup"><span data-stu-id="d5fc3-166">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

