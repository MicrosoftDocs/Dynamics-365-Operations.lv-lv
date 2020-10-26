---
title: Eksperimenta izpildīšana un pārraudzīšana
description: Šajā tēmā ir aprakstīts, kā izpildīt un pārraudzīt eksperimentu trešās puses pakalpojumos. Šeit ir aprakstīts arī, kā veikt izmaiņas variantiem pēc eksperimenta sākšanas.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4cb7d863d9d69612aa0c340099c1f7861c9d12ba
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930243"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="b0c94-104">Eksperimenta izpildīšana un pārraudzīšana</span><span class="sxs-lookup"><span data-stu-id="b0c94-104">Run and monitor an experiment</span></span>

<span data-ttu-id="b0c94-105">Šajā tēmā ir aprakstīts, kā izpildīt un pārraudzīt eksperimentu trešās puses programmā, un veikt izmaiņas variantiem, ja tas nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="b0c94-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="b0c94-106">Pirms šajā tēmā norādīto darbību veikšanas jums vajadzēs [publicēt](experimentation-preview-publish.md) savu eksperimentu pakalpojumā Commerce.</span><span class="sxs-lookup"><span data-stu-id="b0c94-106">Before you complete the steps in this topic, you'll need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> <span data-ttu-id="b0c94-107">Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b0c94-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b0c94-108">Papildu darbības ir apskatītas atsevišķās tēmās.</span><span class="sxs-lookup"><span data-stu-id="b0c94-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="b0c94-109">[ ![Eksperimenta lietotāja maršruts – izpildīšana un pārraudzīšana](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b0c94-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="b0c94-110">Pēc variantu publicēšanas, visas darbības, kas jāveic pakalpojumā Commerce, lai izpildītu eksperimentu, ir pabeigtas.</span><span class="sxs-lookup"><span data-stu-id="b0c94-110">After you publish your variations, all the steps you need to do in Commerce to run your experiment are done.</span></span> <span data-ttu-id="b0c94-111">Nākamā darbība ir noteikt, kādu variantu rādīt katram lietotājam, kad tie pieprasa lapu.</span><span class="sxs-lookup"><span data-stu-id="b0c94-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="b0c94-112">To nosaka trešās puses pakalpojums, bet vispirms pakalpojumā ir jāaktivizē eksperiments.</span><span class="sxs-lookup"><span data-stu-id="b0c94-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="b0c94-113">Tā kā eksperimenta aktivizēšanas darbības dažādos pakalpojumos atšķiras, jums ir jārīkojas saskaņā ar pakalpojuma vai nodrošinātāja instrukcijām.</span><span class="sxs-lookup"><span data-stu-id="b0c94-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="b0c94-114">Ja eksperiments nav aktivizēts, lietotāji redzēs tikai lapas noklusējuma versiju – varianti netiks rādīti.</span><span class="sxs-lookup"><span data-stu-id="b0c94-114">If the experiment is not activated, users will only see the default version of the page - no variations will be displayed.</span></span>

<span data-ttu-id="b0c94-115">Lai apkopotu datus statistiski derīgiem rezultātiem, eksperiments ir jāveic pietiekami ilgu laiku.</span><span class="sxs-lookup"><span data-stu-id="b0c94-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="b0c94-116">Izmantojiet trešās puses pakalpojumu, lai eksperimenta izpildes laikā pārraudzītu ar eksperimentu saistītos datus un analīzi.</span><span class="sxs-lookup"><span data-stu-id="b0c94-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="b0c94-117">Variantu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="b0c94-117">Adjust your variations</span></span>
<span data-ttu-id="b0c94-118">Ja kāda iemesla dēļ ir nepieciešams veikt izmaiņas variantos, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b0c94-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0c94-119">Ja veicat izmaiņas tiešsaistes eksperimentā pakalpojumā Commerce vai trešās puses pakalpojumā, rezultāti var tikt būtiski ietekmēti.</span><span class="sxs-lookup"><span data-stu-id="b0c94-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="b0c94-120">Apsveriet iespēju eksperimentu izpildīt un pēc tam izveidot jaunu eksperimentu, ieviešot būtiskas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b0c94-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="b0c94-121">Dodieties uz **Eksperimenti** cilni vietnes veidotājā un atlasiet eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="b0c94-121">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
1. <span data-ttu-id="b0c94-122">Nolaižamajā izvēlnē atlasiet variantu, kuru vēlaties atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="b0c94-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="b0c94-123">Veiciet nepieciešamās izmaiņas, pēc tam priekšskatiet un publicējiet variantus.</span><span class="sxs-lookup"><span data-stu-id="b0c94-123">Make needed changes, then preview and publish the variations.</span></span> <span data-ttu-id="b0c94-124">Papildinformāciju skatiet sadaļā [Eksperimenta priekšskatīšana un publicēšana](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="b0c94-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="b0c94-125">Dodieties uz trešās puses pakalpojumu, lai veiktu jebkādas ar eksperimentu saistītas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b0c94-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="b0c94-126">Iepriekšējā darbība</span><span class="sxs-lookup"><span data-stu-id="b0c94-126">Previous step</span></span>
[<span data-ttu-id="b0c94-127">Eksperimenta priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="b0c94-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="b0c94-128">Nākošā darbība</span><span class="sxs-lookup"><span data-stu-id="b0c94-128">Next step</span></span>
[<span data-ttu-id="b0c94-129">Varianta publicēšana un eksperimenta pabeigšana</span><span class="sxs-lookup"><span data-stu-id="b0c94-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)