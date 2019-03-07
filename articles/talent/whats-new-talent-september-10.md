---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 10. septembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "305368"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a><span data-ttu-id="33e74-103">Jaunumi un izmaiņas programmā Dynamics 365 for Talent Core HR (2018. gada 10. septembris)</span><span class="sxs-lookup"><span data-stu-id="33e74-103">What's new or changed in Dynamics 365 for Talent Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33e74-104">**8.1.138.0 būvējums**</span><span class="sxs-lookup"><span data-stu-id="33e74-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="33e74-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="33e74-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="33e74-106">Noteikta darba dienas laika izmantošana brīvā laika pieprasījumos (nepilna darba diena)</span><span class="sxs-lookup"><span data-stu-id="33e74-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="33e74-107">Ja atvaļinājuma un prombūtnes iestatījumi ir iestatīti tā, ka brīvai laika pieprasījumā tiek norādīts dienu skaits, tagad var aktivizēt arī nepilnas darba dienas definīciju.</span><span class="sxs-lookup"><span data-stu-id="33e74-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="33e74-108">Pēc tam, iesniedzot brīva laika pieprasījumus, lietotāji var norādīt, vai viņi pieprasa brīvu pirmo vai otro darba dienas daļu.</span><span class="sxs-lookup"><span data-stu-id="33e74-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="33e74-109">Šī opcija pēc noklusējuma ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="33e74-109">By default, this option is turned off.</span></span> <span data-ttu-id="33e74-110">Lai darbinieki varētu pieprasīt brīvu pirmo vai otro darba dienas daļu, šī opcija ir jāaktivizē personāla vadības parametru apgabalā **Atvaļinājums un prombūtne**.</span><span class="sxs-lookup"><span data-stu-id="33e74-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="33e74-111">Šī līdzekļa drošības privilēģija ir uzturēt personāla vadības parametrus.</span><span class="sxs-lookup"><span data-stu-id="33e74-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="33e74-112">Atvaļinājumu un prombūtnes ierakstu apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="33e74-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="33e74-113">Atkarībā no atvaļinājumu konfigurācijas veida darbiniekiem, kuri mēģina iesniegt brīvā laika pieprasījumu, kas pārsniedz to darba dienas ilgumu, tiek parādīts brīdinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="33e74-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="33e74-114">Tas nozīmē, ka viņi tiek brīdināti, ja viņi jebkurā datumā mēģina pieprasīt brīvu vairāk nekā pilnu darba dienu.</span><span class="sxs-lookup"><span data-stu-id="33e74-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="33e74-115">Šī validācijas opcija vienmēr ir ieslēgta.</span><span class="sxs-lookup"><span data-stu-id="33e74-115">This validation is always turned on.</span></span> <span data-ttu-id="33e74-116">Ikreiz, kad darbinieki pārsniedz darba dienas definēto robežvērtību, viņu brīvā laika pieprasījumā tiek parādīts brīdinājums.</span><span class="sxs-lookup"><span data-stu-id="33e74-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="33e74-117">Nosacījuma pārskatu papildu lauki darbplūsmās</span><span class="sxs-lookup"><span data-stu-id="33e74-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="33e74-118">Programmā Core HR vairākās darbplūsmās nosacījuma pārskatiem ir pievienoti papildu lauki un vietturi.</span><span class="sxs-lookup"><span data-stu-id="33e74-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="33e74-119">Tālāk norādītie lauki ir pievienoti kompensācijas, darba attiecību izbeigšanas un pārcelšanas darbplūsmās.</span><span class="sxs-lookup"><span data-stu-id="33e74-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="33e74-120">Nodarbinātības veids</span><span class="sxs-lookup"><span data-stu-id="33e74-120">EmploymentType</span></span>
- <span data-ttu-id="33e74-121">Juridiska persona</span><span class="sxs-lookup"><span data-stu-id="33e74-121">LegalEntity</span></span>
- <span data-ttu-id="33e74-122">Koriģētais nodarbinātā pieņemšanas darbā datums</span><span class="sxs-lookup"><span data-stu-id="33e74-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="33e74-123">Darba devēja paziņotā summa</span><span class="sxs-lookup"><span data-stu-id="33e74-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="33e74-124">Darba devēja paziņojuma vienība</span><span class="sxs-lookup"><span data-stu-id="33e74-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="33e74-125">Pārejas datums</span><span class="sxs-lookup"><span data-stu-id="33e74-125">TransitionDate</span></span>
- <span data-ttu-id="33e74-126">Nodarbinātajam paziņotā summa</span><span class="sxs-lookup"><span data-stu-id="33e74-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="33e74-127">Nodarbinātā pieņemšanas darbā datums</span><span class="sxs-lookup"><span data-stu-id="33e74-127">WorkerStartDate</span></span>
- <span data-ttu-id="33e74-128">Nodarbinātā paziņojuma vienība</span><span class="sxs-lookup"><span data-stu-id="33e74-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="33e74-129">Pārbaudes laika beigu datums</span><span class="sxs-lookup"><span data-stu-id="33e74-129">ProbationEndDate</span></span>
- <span data-ttu-id="33e74-130">Pozīcija</span><span class="sxs-lookup"><span data-stu-id="33e74-130">Position</span></span>
- <span data-ttu-id="33e74-131">Vienība</span><span class="sxs-lookup"><span data-stu-id="33e74-131">Union</span></span>
- <span data-ttu-id="33e74-132">Nodaļa</span><span class="sxs-lookup"><span data-stu-id="33e74-132">Department</span></span>
- <span data-ttu-id="33e74-133">Amata veids</span><span class="sxs-lookup"><span data-stu-id="33e74-133">PositionType</span></span>
- <span data-ttu-id="33e74-134">Uzņēmuma atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="33e74-134">CompLocation</span></span>
- <span data-ttu-id="33e74-135">Amats</span><span class="sxs-lookup"><span data-stu-id="33e74-135">Title</span></span>
- <span data-ttu-id="33e74-136">Amats</span><span class="sxs-lookup"><span data-stu-id="33e74-136">Job</span></span>
- <span data-ttu-id="33e74-137">Darba veids</span><span class="sxs-lookup"><span data-stu-id="33e74-137">JobType</span></span>
- <span data-ttu-id="33e74-138">Darbu grupa</span><span class="sxs-lookup"><span data-stu-id="33e74-138">JobFamily</span></span>
- <span data-ttu-id="33e74-139">Darba funkcija</span><span class="sxs-lookup"><span data-stu-id="33e74-139">JobFunction</span></span>

<span data-ttu-id="33e74-140">Tālāk norādītie lauki ir pievienoti amata darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="33e74-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="33e74-141">Pozīcija</span><span class="sxs-lookup"><span data-stu-id="33e74-141">Position</span></span>
- <span data-ttu-id="33e74-142">Vienība</span><span class="sxs-lookup"><span data-stu-id="33e74-142">Union</span></span>
- <span data-ttu-id="33e74-143">Nodaļa</span><span class="sxs-lookup"><span data-stu-id="33e74-143">Department</span></span>
- <span data-ttu-id="33e74-144">Amata veids</span><span class="sxs-lookup"><span data-stu-id="33e74-144">PositionType</span></span>
- <span data-ttu-id="33e74-145">Uzņēmuma atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="33e74-145">CompLocation</span></span>
- <span data-ttu-id="33e74-146">Amats</span><span class="sxs-lookup"><span data-stu-id="33e74-146">Title</span></span>
- <span data-ttu-id="33e74-147">Amats</span><span class="sxs-lookup"><span data-stu-id="33e74-147">Job</span></span>
- <span data-ttu-id="33e74-148">Darba veids</span><span class="sxs-lookup"><span data-stu-id="33e74-148">JobType</span></span>
- <span data-ttu-id="33e74-149">Darbu grupa</span><span class="sxs-lookup"><span data-stu-id="33e74-149">JobFamily</span></span>
- <span data-ttu-id="33e74-150">Darba funkcija</span><span class="sxs-lookup"><span data-stu-id="33e74-150">JobFunction</span></span>

<span data-ttu-id="33e74-151">Nosacījuma pārskatu lauki un vietturi ir pieejami visiem lietotājiem, kuriem ir piekļuves tiesības konfigurēt iepriekš norādītās darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="33e74-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="33e74-152">Pāriešana uz Attract no personāla vadības lapas</span><span class="sxs-lookup"><span data-stu-id="33e74-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="33e74-153">Ja ir iestatīts līdzeklis Attract, lietotājiem personāla vadības lapā **Darbā pieņemamie kandidāti** tiek parādīta norāde sākt ar Attract un netiek rādīts ziņojums “Mēs neatradām neko, ko šeit rādīt”.</span><span class="sxs-lookup"><span data-stu-id="33e74-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="33e74-154">Cita izmaiņas</span><span class="sxs-lookup"><span data-stu-id="33e74-154">Other changes</span></span>

<span data-ttu-id="33e74-155">Šis laidiens ietver vairākus papildu kļūdu labojumus.</span><span class="sxs-lookup"><span data-stu-id="33e74-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="33e74-156">Pieņemot darbā līgumdarbinieku, cilnei **Kompensācija** pieprasījumu/darbību lapā nav jābūt pieejamai.</span><span class="sxs-lookup"><span data-stu-id="33e74-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="33e74-157">Pieprasījuma par darba attiecību pārtraukšanu procesu var turpināt tikai tad, kad visos pieprasītajos laukos ir ievadīti dati.</span><span class="sxs-lookup"><span data-stu-id="33e74-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="33e74-158">Ir novērstas kārtošanas secības un datumu parādīšanas problēmas personāla vadības analīzē.</span><span class="sxs-lookup"><span data-stu-id="33e74-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
