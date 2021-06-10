---
title: Reģistrācijas piemērotības apstrāde
description: Šajā rakstā ir paskaidrots, kā izpildīt reģistrācijas piemērotības apstrādi.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4dd63e755f0afdbce411b3001410d2e56036e432
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054264"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="41f38-103">Reģistrācijas piemērotības apstrāde</span><span class="sxs-lookup"><span data-stu-id="41f38-103">Process enrollment eligibility</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="41f38-104">Šajā rakstā ir paskaidrots, kā izpildīt reģistrācijas piemērotības apstrādi.</span><span class="sxs-lookup"><span data-stu-id="41f38-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="41f38-105">Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Reģistrācijas piemērotības apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="41f38-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="41f38-106">Dialoglodziņā **Izpildīt atvieglojumu reģistrācijas piemērotības apstrādi** norādiet vērtības tālāk minētajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="41f38-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="41f38-107">Lauks</span><span class="sxs-lookup"><span data-stu-id="41f38-107">Field</span></span> | <span data-ttu-id="41f38-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="41f38-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="41f38-109">**Reģistrācijas periods**</span><span class="sxs-lookup"><span data-stu-id="41f38-109">**Enrollment period**</span></span> | <span data-ttu-id="41f38-110">Reģistrācijas periods, kuram apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="41f38-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="41f38-111">**Juridiska persona**</span><span class="sxs-lookup"><span data-stu-id="41f38-111">**Legal entity**</span></span> | <span data-ttu-id="41f38-112">Juridiskā persona, kam apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="41f38-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="41f38-113">**Nodarbinātais**</span><span class="sxs-lookup"><span data-stu-id="41f38-113">**Worker**</span></span> | <span data-ttu-id="41f38-114">Nodarbinātais, kuram apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="41f38-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="41f38-115">Ja šo lauku atstāsiet tukšu, reģistrācijas piemērotība tiks apstrādāta visiem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="41f38-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="41f38-116">**Atvieglojumu plāns**</span><span class="sxs-lookup"><span data-stu-id="41f38-116">**Benefit plan**</span></span> | <span data-ttu-id="41f38-117">Atvieglojumu plāns, kam apstrādāt reģistrācijas piemērotību.</span><span class="sxs-lookup"><span data-stu-id="41f38-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="41f38-118">Ja vēlaties izpildīt apstrādi fonā, atlasiet **Izpildīt fonā** un veiciet tālāk minētos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="41f38-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="41f38-119">Ievadiet informāciju apstrādei.</span><span class="sxs-lookup"><span data-stu-id="41f38-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="41f38-120">Lai iestatītu periodisku darbu, atlasiet **Periodiskums**, ievadiet periodiskuma informāciju un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="41f38-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="41f38-121">Lai iestatītu darba brīdinājumu, atlasiet **Brīdinājumi**, atlasiet saņemamos brīdinājumus un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="41f38-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="41f38-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="41f38-122">Select **OK**.</span></span> <span data-ttu-id="41f38-123">Apstrāde tiks izpildīta ar iestatītajiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="41f38-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="41f38-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="41f38-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="41f38-125">Skatīt procesa rezultātus</span><span class="sxs-lookup"><span data-stu-id="41f38-125">View Process Results</span></span>

<span data-ttu-id="41f38-126">Šajā rakstā ir paskaidrots, kā skatīt reģistrācijas piemērotības rezultātus.</span><span class="sxs-lookup"><span data-stu-id="41f38-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="41f38-127">Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Procesa rezultāti**.</span><span class="sxs-lookup"><span data-stu-id="41f38-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="41f38-128">Veidlapā **Procesa rezultāti** ir norādīti šādi lauki:</span><span class="sxs-lookup"><span data-stu-id="41f38-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="41f38-129">Lauks</span><span class="sxs-lookup"><span data-stu-id="41f38-129">Field</span></span> | <span data-ttu-id="41f38-130">apraksts</span><span class="sxs-lookup"><span data-stu-id="41f38-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="41f38-131">**Procesa ID**</span><span class="sxs-lookup"><span data-stu-id="41f38-131">**Process ID**</span></span> | <span data-ttu-id="41f38-132">Unikālais ID darbinieku, juridisko personu un procesa izpildes kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="41f38-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="41f38-133">**Procesu tips**</span><span class="sxs-lookup"><span data-stu-id="41f38-133">**Process type**</span></span> | <span data-ttu-id="41f38-134">Tas identificē procesu, kas tika palaists.</span><span class="sxs-lookup"><span data-stu-id="41f38-134">This identifies the process that was run.</span></span> <span data-ttu-id="41f38-135">Piemēram: Uzņemšana.</span><span class="sxs-lookup"><span data-stu-id="41f38-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="41f38-136">**Laikspiedols**</span><span class="sxs-lookup"><span data-stu-id="41f38-136">**Time stamp**</span></span> | <span data-ttu-id="41f38-137">Laiks, kad tika palaists atbilstības process.</span><span class="sxs-lookup"><span data-stu-id="41f38-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="41f38-138">**Juridiska persona**</span><span class="sxs-lookup"><span data-stu-id="41f38-138">**Legal entity**</span></span> | <span data-ttu-id="41f38-139">Juridiskā persona, kas norādīta uzņemšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="41f38-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="41f38-140">**Darbinieks**</span><span class="sxs-lookup"><span data-stu-id="41f38-140">**Worker**</span></span> | <span data-ttu-id="41f38-141">Darbinieks, kurš tika apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="41f38-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="41f38-142">\*\*Plāns</span><span class="sxs-lookup"><span data-stu-id="41f38-142">\*\*Plan</span></span> | <span data-ttu-id="41f38-143">Atvieglojumu plāns, kuram tika mēģināts veikt uzņemšanu.</span><span class="sxs-lookup"><span data-stu-id="41f38-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="41f38-144">**Piemērojamības kārtula**</span><span class="sxs-lookup"><span data-stu-id="41f38-144">**Eligibility rule**</span></span> | <span data-ttu-id="41f38-145">Piemērojamības kārtula, kas tika apstrādāta.</span><span class="sxs-lookup"><span data-stu-id="41f38-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="41f38-146">Ja radās kļūda, pirms tika palaista piemērojamība, šis lauks būs tukšs.</span><span class="sxs-lookup"><span data-stu-id="41f38-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="41f38-147">Piemēram, ja darbiniekam nav noteikta kompensācija, piemērojamības process netiks izpildīts, un šis lauks tiks atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="41f38-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="41f38-148">**Rezultāta statuss**</span><span class="sxs-lookup"><span data-stu-id="41f38-148">**Result status**</span></span> | <span data-ttu-id="41f38-149">Tas būs atbilstīgs vai neatbilstīgs.</span><span class="sxs-lookup"><span data-stu-id="41f38-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="41f38-150">Rezultāta statuss būs neatbilstīgs, ja darbinieks neatbilst piemērojamības nosacījumu kritērijam, ja darbiniekam trūkst nepieciešamās informācijas, piemēram, atalgojuma biežums vai fiksēta kompensācija, vai ja atvieglojumu plānā trūkst informācijas, kas liedz darbiniekiem tikt iesaistītam.</span><span class="sxs-lookup"><span data-stu-id="41f38-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="41f38-151">**Rezultāta ziņojums**</span><span class="sxs-lookup"><span data-stu-id="41f38-151">**Result message**</span></span> | <span data-ttu-id="41f38-152">Norāda, kāpēc darbiniekam nav tiesību saņemt atvieglojumu plānu vai ja piemērojamības kārtula ir pieņemta.</span><span class="sxs-lookup"><span data-stu-id="41f38-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |



[!INCLUDE[footer-include](../includes/footer-banner.md)]