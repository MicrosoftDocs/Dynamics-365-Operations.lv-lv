---
title: Analītisku atskaišu izmantošana programmā Microsoft Dynamics 365 for Talent - Attract
description: Šajā tēmā ir aprakstītas analītiskos pārskatus par darbā pieņemšanas procesa ieskatiem programmā Microsoft Dynamics 365 for Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: f69c45e885d789d05a081064f30ccd6ce6bfec52
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742892"
---
# <a name="use-analytic-reports"></a><span data-ttu-id="ec0ba-103">Izmantot analītiskos pārskatus</span><span class="sxs-lookup"><span data-stu-id="ec0ba-103">Use analytic reports</span></span>

<span data-ttu-id="ec0ba-104">Analītiskie pārskati programmā Attract nodrošina standarta komplektācijā (out-of-the-box — OOTB) iekļautu risinājumu darbā pieņemšanas procesa ieskatiem.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-104">Analytic reports in Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="ec0ba-105">Pieejamās funkcijas:</span><span class="sxs-lookup"><span data-stu-id="ec0ba-105">Availabe features include:</span></span>

- <span data-ttu-id="ec0ba-106">**Darba analīze** — noklikšķiniet uz cilnes **Analīze** darba ietvaros, lai skatītu darba kandidātu rādītājus.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="ec0ba-107">**Analīzes centrmezgls:**  — kreisajā navigācijas sadaļā noklikšķiniet uz **Analīze**, lai skatītu apkopotos rādītājus par visiem darbiem.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="ec0ba-108">**Lietotājam raksturīga drošība** — piekļuvi pārskatiem kontrolē Attract [loma](security-attract.md) un darba dalībnieka loma.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="ec0ba-109">**Šķērsfiltrēšana:**  — lai skatītu citus rādītājus, kas filtrēti pēc atlasītajiem datiem, pārskatā noklikšķiniet uz vizuālajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="ec0ba-110">Šis līdzeklis pašreiz ir [priekšskatījumā](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="ec0ba-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="ec0ba-111">Lai to izmēģinātu, jums ir nepieciešams [**Visaptverošais darbā pieņemšanas papildinājums**](attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="ec0ba-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="ec0ba-112">Visi publiskie priekšskatījuma pārskati tiek rādīti angļu valodā.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="ec0ba-113">Pārskatu atsvaidzināšanas biežums: ik pēc 3 stundām.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="ec0ba-114">Pēdējais atsvaidzināšanas laiks (vietējā laika joslā) atrodas pārskata sākumā.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="ec0ba-115">Atsvaidzināšanas laiki ir aptuveni un mainās atkarībā no datu apjoma un resursu noslodzes jūsu reģionā.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="ec0ba-116">Darba analīze</span><span class="sxs-lookup"><span data-stu-id="ec0ba-116">Job Analytics</span></span>

<span data-ttu-id="ec0ba-117">Pārskati Darba analīze ir atsevišķas vakances darbā pieņemšanas procesa momentuzņēmums.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="ec0ba-118">Galvenie rādītāji:</span><span class="sxs-lookup"><span data-stu-id="ec0ba-118">Key metrics include:</span></span>

- <span data-ttu-id="ec0ba-119">Aktīvie kandidāti pēc posma</span><span class="sxs-lookup"><span data-stu-id="ec0ba-119">Active applicants by stage</span></span>
- <span data-ttu-id="ec0ba-120">Kandidāta avots</span><span class="sxs-lookup"><span data-stu-id="ec0ba-120">Applicant source</span></span>
- <span data-ttu-id="ec0ba-121">Kandidāta tips (iekšējs vai ārējs)</span><span class="sxs-lookup"><span data-stu-id="ec0ba-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="ec0ba-122">Analīzes centrmezgls</span><span class="sxs-lookup"><span data-stu-id="ec0ba-122">Analytics Hub</span></span>

<span data-ttu-id="ec0ba-123">Pārskatos Analīzes centrmezgls tiek apkopoti dažādu darbu dati, lai atklātu darbā pieņemšanas procesā esošās tendences.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="ec0ba-124">Programmā Attract ir iekļauti divi OOTB pārskati: Konveijera apkopojums un Piltuves analīze.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="ec0ba-125">Konveijera apkopojums</span><span class="sxs-lookup"><span data-stu-id="ec0ba-125">Pipeline Summary</span></span>

<span data-ttu-id="ec0ba-126">Konveijera kopsavilkuma pārskatā tiek apkopoti dati par vakantām darba vietām.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="ec0ba-127">Galvenie rādītāji:</span><span class="sxs-lookup"><span data-stu-id="ec0ba-127">Key metrics include:</span></span>

- <span data-ttu-id="ec0ba-128">Kandidāti visos darbos pēc posma</span><span class="sxs-lookup"><span data-stu-id="ec0ba-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="ec0ba-129">Kandidāta avots</span><span class="sxs-lookup"><span data-stu-id="ec0ba-129">Applicant source</span></span>
- <span data-ttu-id="ec0ba-130">Vakantās darba vietas pēc darba stāža līmeņa</span><span class="sxs-lookup"><span data-stu-id="ec0ba-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="ec0ba-131">Piltuves analīze</span><span class="sxs-lookup"><span data-stu-id="ec0ba-131">Funnel Analysis</span></span>

<span data-ttu-id="ec0ba-132">Piltuves analīzes pārskatā tiek apkopoti dati par darba vietām, kas ir slēgtas kā aizpildītas.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="ec0ba-133">Galvenie rādītāji:</span><span class="sxs-lookup"><span data-stu-id="ec0ba-133">Key metrics include:</span></span>

- <span data-ttu-id="ec0ba-134">Laiks līdz pieņemšanai darbā</span><span class="sxs-lookup"><span data-stu-id="ec0ba-134">Time to hire</span></span>
- <span data-ttu-id="ec0ba-135">Konvertēšanas rādītāji (uzvirzot kursoru)</span><span class="sxs-lookup"><span data-stu-id="ec0ba-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="ec0ba-136">Piedāvājuma pieņemšanas koeficients</span><span class="sxs-lookup"><span data-stu-id="ec0ba-136">Offer acceptance rate</span></span>

<span data-ttu-id="ec0ba-137">Piezīme. Lai visprecīzāķ noteikti laiku līdz pieņemšanai darbā, ir ieteicams izmantot līdzekli [Piedāvājumu pārvaldība](offer-setup.md), kas ir pieejams kā daļa no Visaptverošā darbā pieņemšanas papildinājuma.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="ec0ba-138">Lai iegūtu papildu informāciju, mēģiniet virzīt kursoru virs vizuālajiem elementiem.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="ec0ba-139">Piemēram, virzot kursoru virs sadaļas **Aktīvie kandidāti** vizuālajiem materiāliem, tiek parādīts vidējais dienu skaits atsevišķā posmā.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="ec0ba-140">Analizējot šo informāciju, var gūt būtiskus ieskatus, lai samazinātu laiku līdz nolīgšanai un ļautu personāla atlases darbiniekiem koncentrēties uz veidiem, kā samazināt katram posmam veltīto laiku.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="ec0ba-141">Lietotājam raksturīga drošība</span><span class="sxs-lookup"><span data-stu-id="ec0ba-141">User-specific security</span></span>

<span data-ttu-id="ec0ba-142">Programmas Attract pārskati ir pieejami Administrators, Lasīt visu, Personāla atlases darbinieks un Par pieņemšanu darbā atbildīgais vadītājs [lomām.](security-attract.md)</span><span class="sxs-lookup"><span data-stu-id="ec0ba-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="ec0ba-143">Nepiešķirtajiem lietotājiem nav piekļuves nevienai analīzes pārskatu lapai (Darba analīze vai Analīzes centrmezgls).</span><span class="sxs-lookup"><span data-stu-id="ec0ba-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="ec0ba-144">Pārskatos Darba analīze tiek rādīti dati atlasītajam darbam.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="ec0ba-145">Pārskatos Analīzes centrmezgls tiek apkopoti dati par visiem darbiem, ko lietotājs var skatīt.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="ec0ba-146">Lietotājiem, kas lapā Darbi var skatīt gan Mani darbi, gan Visi darbi, pārskatos Analīzes centrmezgls ir pieejami šie paši skati.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="ec0ba-147">Šķērsfiltrēšana</span><span class="sxs-lookup"><span data-stu-id="ec0ba-147">Cross-filter</span></span>

<span data-ttu-id="ec0ba-148">Viena no Power BI izcilajām īpašībām ir visu pārskata lapā esošo vizuālo elementu savstarpējā saistība.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="ec0ba-149">Ja atlasīsit datu punktu uz kāda vizuālā elementa, visi pārējie vizuālie elementi lapā, kurā ir šīs datu izmaiņas, pamatojoties uz šo atlasi.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="ec0ba-150">Uzziniet vairāk un aplūkojiet piemēru sadaļā [Kā vizuālie elementi veic šķērsfiltrēšanu Power BIpārskatā](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="ec0ba-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="ec0ba-151">Eksportēt programmā Excel</span><span class="sxs-lookup"><span data-stu-id="ec0ba-151">Export to Excel</span></span>

<span data-ttu-id="ec0ba-152">Lai skatītu pārskata datus programmā Excel, varat noklikšķināt uz izvēlnes opcijas (trīs punkti) uz vizuālā elementa un atlasīt opciju **Eksportēt pamata datus**.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="ec0ba-153">Eksportētie dati tiks eksportēti kā filtrēti, respektējot lietotāja atļaujas programmā Attract.</span><span class="sxs-lookup"><span data-stu-id="ec0ba-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="ec0ba-154">Papildinformāciju skatiet sadaļā [Datu eksportēšana no vizualizācijas](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="ec0ba-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
