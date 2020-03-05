---
title: Dzīves notikumu apstrāde
description: Darbinieku dzīves cikla laikā Microsoft Dynamics 365 Human Resources katrs darbinieks var sastapties ar dažādām dzīves notikumu izmaiņām.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 91812432ead4b0afccfba30f8023f014e216236a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009818"
---
# <a name="process-life-events"></a><span data-ttu-id="1f498-103">Dzīves notikumu apstrāde</span><span class="sxs-lookup"><span data-stu-id="1f498-103">Process life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1f498-104">Darbinieku dzīves cikla laikā Microsoft Dynamics 365 Human Resources katrs darbinieks var sastapties ar dažādām dzīves notikumu izmaiņām.</span><span class="sxs-lookup"><span data-stu-id="1f498-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="1f498-105">Piemēram, laulība, izmaiņas nodarbinātībā vai apgādājamā/saņēmēja maiņa.</span><span class="sxs-lookup"><span data-stu-id="1f498-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="1f498-106">Lai izmantotu dzīves notikumus, atvieglojumu parametru veidlapā ir jāiespējo dzīves notikumi, jāiestata dzīves notikumu veidi un dzīves notikumu opcijas plānu veidiem.</span><span class="sxs-lookup"><span data-stu-id="1f498-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="1f498-107">Lai varētu apstrādāt dzīves notikumus, vismaz vienu reizi darbā pieņemšanas laika periodā ir jābūt jau izpildītai atvērtai reģistrācijai.</span><span class="sxs-lookup"><span data-stu-id="1f498-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="1f498-108">Savienotajās Valstīs atvērta reģistrācija parasti notiek reizi gadā.</span><span class="sxs-lookup"><span data-stu-id="1f498-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="1f498-109">Ārpus Savienotajām Valstīm atvērto reģistrāciju var izpildīt darbā pieņemšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="1f498-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="1f498-110">Nodarbinātajam nav jāatlasa atvieglojumu plāns, lai varētu apstrādāt dzīves notikumus, bet tie ir jāiekļauj atvērtajā reģistrācijas apstrādē.</span><span class="sxs-lookup"><span data-stu-id="1f498-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="1f498-111">Izmantojiet dzīves notikumu apstrādi, ja ir nodarbinātie, kuru dzīves notikumi notiks nākotnes datumā.</span><span class="sxs-lookup"><span data-stu-id="1f498-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="1f498-112">Šis notikums apstrādās visus dzīves notikumus, kas nav apstrādāti (piemēram, turpmākās dzīves notikumus vai dzīves notikumus, kas ir pievienoti un kas nav raksturīgi nevienam citam darbiniekam — viens piemērs ir jauns atvieglojums).</span><span class="sxs-lookup"><span data-stu-id="1f498-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="1f498-113">Reālā laika dzīves notikumi ir paslēpti.</span><span class="sxs-lookup"><span data-stu-id="1f498-113">Real time life events are hidden.</span></span>

<span data-ttu-id="1f498-114">Piemēram, ja šodien ir 1. februāris un 14. februārī nodarbinātajam Jānim Bērziņam jāmaina juridiskā persona, ja izpildīsiet dzīves notikumu apstrādi 15. februārim, sistēma apstrādās visus notikumus līdz 15. februārim.</span><span class="sxs-lookup"><span data-stu-id="1f498-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="1f498-115">Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Dzīves notikumu apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="1f498-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="1f498-116">Dialoglodziņā **Izpildīt dzīves notikumu apstrādi** norādiet vērtības tālāk minētajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="1f498-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="1f498-117">Lauks</span><span class="sxs-lookup"><span data-stu-id="1f498-117">Field</span></span> | <span data-ttu-id="1f498-118">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1f498-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1f498-119">Reģistrācijas periods</span><span class="sxs-lookup"><span data-stu-id="1f498-119">Enrollment period</span></span> | <span data-ttu-id="1f498-120">Reģistrācijas periods, kuram apstrādāt dzīves notikumus.</span><span class="sxs-lookup"><span data-stu-id="1f498-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="1f498-121">Juridiska persona</span><span class="sxs-lookup"><span data-stu-id="1f498-121">Legal entity</span></span> | <span data-ttu-id="1f498-122">Juridiskā persona, kam apstrādāt dzīves notikumus.</span><span class="sxs-lookup"><span data-stu-id="1f498-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="1f498-123">Dzīves notikuma datums</span><span class="sxs-lookup"><span data-stu-id="1f498-123">Life event date</span></span> | <span data-ttu-id="1f498-124">Sistēma apstrādā visus notikumus reģistrācijas periodā, kas notiek līdz šim datumam.</span><span class="sxs-lookup"><span data-stu-id="1f498-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="1f498-125">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="1f498-125">Worker</span></span> | <span data-ttu-id="1f498-126">Nodarbinātais, kuram apstrādāt dzīves notikumus.</span><span class="sxs-lookup"><span data-stu-id="1f498-126">The worker to process life events for.</span></span> <span data-ttu-id="1f498-127">Ja šo lauku atstāsiet tukšu, dzīves notikumi tiks apstrādāti visiem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="1f498-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="1f498-128">Ja vēlaties izpildīt apstrādi fonā, atlasiet **Izpildīt fonā** un veiciet tālāk minētos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="1f498-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="1f498-129">Ievadiet informāciju apstrādei.</span><span class="sxs-lookup"><span data-stu-id="1f498-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="1f498-130">Lai iestatītu periodisku darbu, atlasiet **Periodiskums**, ievadiet periodiskuma informāciju un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1f498-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="1f498-131">Lai iestatītu darba brīdinājumu, atlasiet **Brīdinājumi**, atlasiet saņemamos brīdinājumus un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1f498-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="1f498-132">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1f498-132">Select **OK**.</span></span> <span data-ttu-id="1f498-133">Apstrāde tiks izpildīta ar iestatītajiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="1f498-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="1f498-134">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1f498-134">Select **OK**.</span></span>