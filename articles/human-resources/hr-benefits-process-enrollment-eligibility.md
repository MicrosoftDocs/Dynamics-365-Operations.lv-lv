---
title: Reģistrācijas piemērotības apstrāde
description: Šajā rakstā ir paskaidrots, kā izpildīt reģistrācijas piemērotības apstrādi.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dfb7f13dce48f33c111af491918702763f7e3b8a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419499"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="925c6-103">Reģistrācijas piemērotības apstrāde</span><span class="sxs-lookup"><span data-stu-id="925c6-103">Process enrollment eligibility</span></span>

<span data-ttu-id="925c6-104">Šajā rakstā ir paskaidrots, kā izpildīt reģistrācijas piemērotības apstrādi.</span><span class="sxs-lookup"><span data-stu-id="925c6-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="925c6-105">Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Reģistrācijas piemērotības apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="925c6-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="925c6-106">Dialoglodziņā **Izpildīt atvieglojumu reģistrācijas piemērotības apstrādi** norādiet vērtības tālāk minētajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="925c6-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="925c6-107">Lauks</span><span class="sxs-lookup"><span data-stu-id="925c6-107">Field</span></span> | <span data-ttu-id="925c6-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="925c6-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="925c6-109">**Reģistrācijas periods**</span><span class="sxs-lookup"><span data-stu-id="925c6-109">**Enrollment period**</span></span> | <span data-ttu-id="925c6-110">Reģistrācijas periods, kuram apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="925c6-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="925c6-111">**Juridiska persona**</span><span class="sxs-lookup"><span data-stu-id="925c6-111">**Legal entity**</span></span> | <span data-ttu-id="925c6-112">Juridiskā persona, kam apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="925c6-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="925c6-113">**Nodarbinātais**</span><span class="sxs-lookup"><span data-stu-id="925c6-113">**Worker**</span></span> | <span data-ttu-id="925c6-114">Nodarbinātais, kuram apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="925c6-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="925c6-115">Ja šo lauku atstāsiet tukšu, reģistrācijas piemērotība tiks apstrādāta visiem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="925c6-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="925c6-116">**Atvieglojumu plāns**</span><span class="sxs-lookup"><span data-stu-id="925c6-116">**Benefit plan**</span></span> | <span data-ttu-id="925c6-117">Atvieglojumu plāns, kam apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="925c6-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="925c6-118">Ja vēlaties izpildīt apstrādi fonā, atlasiet **Izpildīt fonā** un veiciet tālāk minētos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="925c6-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="925c6-119">Ievadiet informāciju apstrādei.</span><span class="sxs-lookup"><span data-stu-id="925c6-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="925c6-120">Lai iestatītu periodisku darbu, atlasiet **Periodiskums**, ievadiet periodiskuma informāciju un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="925c6-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="925c6-121">Lai iestatītu darba brīdinājumu, atlasiet **Brīdinājumi**, atlasiet saņemamos brīdinājumus un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="925c6-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="925c6-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="925c6-122">Select **OK**.</span></span> <span data-ttu-id="925c6-123">Apstrāde tiks izpildīta ar iestatītajiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="925c6-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="925c6-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="925c6-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="925c6-125">Skatīt procesa rezultātus</span><span class="sxs-lookup"><span data-stu-id="925c6-125">View Process Results</span></span>

<span data-ttu-id="925c6-126">Šajā rakstā ir paskaidrots, kā skatīt reģistrācijas piemērotības rezultātus.</span><span class="sxs-lookup"><span data-stu-id="925c6-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="925c6-127">Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Procesa rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="925c6-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="925c6-128">Veidlapā **Procesa rezultāti** ir norādīti šādi lauki:</span><span class="sxs-lookup"><span data-stu-id="925c6-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="925c6-129">Lauks</span><span class="sxs-lookup"><span data-stu-id="925c6-129">Field</span></span> | <span data-ttu-id="925c6-130">apraksts</span><span class="sxs-lookup"><span data-stu-id="925c6-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="925c6-131">**Procesa ID**</span><span class="sxs-lookup"><span data-stu-id="925c6-131">**Process ID**</span></span> | <span data-ttu-id="925c6-132">Unikālais ID darbinieku, juridisko personu un procesa izpildes kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="925c6-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="925c6-133">**Procesu tips**</span><span class="sxs-lookup"><span data-stu-id="925c6-133">**Process type**</span></span> | <span data-ttu-id="925c6-134">Tas identificē procesu, kas tika palaists.</span><span class="sxs-lookup"><span data-stu-id="925c6-134">This identifies the process that was run.</span></span> <span data-ttu-id="925c6-135">Piemēram: Uzņemšana.</span><span class="sxs-lookup"><span data-stu-id="925c6-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="925c6-136">**Laikspiedols**</span><span class="sxs-lookup"><span data-stu-id="925c6-136">**Time stamp**</span></span> | <span data-ttu-id="925c6-137">Laiks, kad tika palaists atbilstības process.</span><span class="sxs-lookup"><span data-stu-id="925c6-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="925c6-138">**Juridiska persona**</span><span class="sxs-lookup"><span data-stu-id="925c6-138">**Legal entity**</span></span> | <span data-ttu-id="925c6-139">Juridiskā persona, kas norādīta uzņemšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="925c6-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="925c6-140">**Darbinieks**</span><span class="sxs-lookup"><span data-stu-id="925c6-140">**Worker**</span></span> | <span data-ttu-id="925c6-141">Darbinieks, kurš tika apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="925c6-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="925c6-142">\*\*Plāns</span><span class="sxs-lookup"><span data-stu-id="925c6-142">\*\*Plan</span></span> | <span data-ttu-id="925c6-143">Atvieglojumu plāns, kuram tika mēģināts veikt uzņemšanu.</span><span class="sxs-lookup"><span data-stu-id="925c6-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="925c6-144">**Piemērojamības kārtula**</span><span class="sxs-lookup"><span data-stu-id="925c6-144">**Eligibility rule**</span></span> | <span data-ttu-id="925c6-145">Piemērojamības kārtula, kas tika apstrādāta.</span><span class="sxs-lookup"><span data-stu-id="925c6-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="925c6-146">Ja radās kļūda, pirms tika palaista piemērojamība, šis lauks būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="925c6-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="925c6-147">Piemēram, ja darbiniekam nav noteikta kompensācija, piemērojamības process netiks izpildīts, un šis lauks tiks atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="925c6-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="925c6-148">**Rezultāta statuss**</span><span class="sxs-lookup"><span data-stu-id="925c6-148">**Result status**</span></span> | <span data-ttu-id="925c6-149">Tas būs atbilstīgs vai neatbilstīgs.</span><span class="sxs-lookup"><span data-stu-id="925c6-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="925c6-150">Rezultāta statuss būs neatbilstīgs, ja darbinieks neatbilst piemērojamības nosacījumu kritērijam, ja darbiniekam trūkst nepieciešamās informācijas, piemēram, atalgojuma biežums vai fiksēta kompensācija, vai ja atvieglojumu plānā trūkst informācijas, kas liedz darbiniekiem tikt iesaistītam.</span><span class="sxs-lookup"><span data-stu-id="925c6-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="925c6-151">**Rezultāta ziņojums**</span><span class="sxs-lookup"><span data-stu-id="925c6-151">**Result message**</span></span> | <span data-ttu-id="925c6-152">Norāda, kāpēc darbiniekam nav tiesību saņemt atvieglojumu plānu vai ja piemērojamības kārtula ir pieņemta.</span><span class="sxs-lookup"><span data-stu-id="925c6-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

