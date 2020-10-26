---
title: Eksperimenta pievienošana un variantu rediģēšana
description: Šajā tēmā ir aprakstīts, kā pievienot eksperimentu trešās puses pakalpojumam Dynamics 365 Commerce un kā rediģēt eksperimenta variantus.
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
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930246"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="21e60-103">Eksperimenta pievienošana un variantu rediģēšana</span><span class="sxs-lookup"><span data-stu-id="21e60-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="21e60-104">Šajā tēmā ir aprakstīts, kā pievienot eksperimentu pakalpojumā Commerce un kā veikt izmaiņas variantiem, lai tie atbilstu hipotēzei.</span><span class="sxs-lookup"><span data-stu-id="21e60-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so they align with your hypothesis.</span></span> <span data-ttu-id="21e60-105">Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="21e60-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="21e60-106">Papildu darbības ir apskatītas atsevišķās tēmās.</span><span class="sxs-lookup"><span data-stu-id="21e60-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="21e60-107">[ ![Eksperimenta lietotāja maršruts – pievienošana un rediģēšana](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="21e60-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="21e60-108">Pēc [eksperimenta iestatīšanas](experimentation-setup.md) trešās puses pakalpojumā, jūs pievienosit eksperimentu Dynamics 365 Commerce un rediģēsit eksperimenta variantus.</span><span class="sxs-lookup"><span data-stu-id="21e60-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="21e60-109">Plānošanas apsvērumi</span><span class="sxs-lookup"><span data-stu-id="21e60-109">Planning considerations</span></span>

<span data-ttu-id="21e60-110">Pirms pievienojat eksperimentu pakalpojumā Commerce, jums ir jāpieņem daži lēmumi, kas ietekmē veidu, kādā Commerce pārvalda jūsu saturu.</span><span class="sxs-lookup"><span data-stu-id="21e60-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="21e60-111">Eksperimenta tvēruma noteikšana</span><span class="sxs-lookup"><span data-stu-id="21e60-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="21e60-112">Kad pievienojat eksperimentu, jums tiek piedāvāts definēt eksperimenta tvērumu.</span><span class="sxs-lookup"><span data-stu-id="21e60-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="21e60-113">Eksperimenti ir definēti kā **daļēja** tvēruma vai **pilnīga** tvēruma.</span><span class="sxs-lookup"><span data-stu-id="21e60-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="21e60-114">Izvēlieties **daļēja**, ja vēlaties veikt eksperimentu noteiktā lapas daļā.</span><span class="sxs-lookup"><span data-stu-id="21e60-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="21e60-115">Atlasot šo opciju, ir jānosaka, kuri moduļi ir ietverti eksperimentā.</span><span class="sxs-lookup"><span data-stu-id="21e60-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="21e60-116">Izmaiņas, kas tiek veiktas noklusējuma lapas vai fragmenta daļām, kas nav saistītas ar eksperimentu, tiek automātiski sinhronizētas starp variantiem.</span><span class="sxs-lookup"><span data-stu-id="21e60-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="21e60-117">Izvēlieties **pilnīga**, ja vēlaties veikt eksperimentu visā lapā vai fragmentā.</span><span class="sxs-lookup"><span data-stu-id="21e60-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="21e60-118">Tiek izveidotas atsevišķas noklusējuma lapas vai fragmenta kopijas.</span><span class="sxs-lookup"><span data-stu-id="21e60-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="21e60-119">Nav nepieciešams atlasīt, kuri moduļi tiek ietverti eksperimentā, jo izmaiņām ir pieejama visa rediģēšanas virsma.</span><span class="sxs-lookup"><span data-stu-id="21e60-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="21e60-120">Moduļus varat pievienot, dzēst un pārkārtot pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="21e60-120">You can add, delete, and re-order modules as needed.</span></span> <span data-ttu-id="21e60-121">Tomēr, ja tiek veiktas izmaiņas noklusējuma lapā vai fragmentā, ar kuru ir saistīts eksperiments, šīs izmaiņas ir manuāli jāsinhronizē visos variantos.</span><span class="sxs-lookup"><span data-stu-id="21e60-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="21e60-122">Saistot eksperimentu ar lapu, kurā tiek izmantots izkārtojums, eksperimenta tvērums var būt tikai **pilnīgs**.</span><span class="sxs-lookup"><span data-stu-id="21e60-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="21e60-123">Izlemiet, vai vēlaties ieplānot eksperimenta publicēšanu</span><span class="sxs-lookup"><span data-stu-id="21e60-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="21e60-124">Ja vēlaties ieplānot eksperimenta publicēšanu tiešsaistes vietnē, pārliecinieties, ka saturs, kuru vēlaties saistīt ar eksperimentu, ir pieejams publicēšanas grupā *pirms* eksperimenta pievienošanas.</span><span class="sxs-lookup"><span data-stu-id="21e60-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="21e60-125">Papildinformāciju par publicēšanas grupām, skatiet sadaļā [Darbs ar publicēšanas grupām](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="21e60-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="21e60-126">Eksperimenta pievienošana</span><span class="sxs-lookup"><span data-stu-id="21e60-126">Connect your experiment</span></span>
<span data-ttu-id="21e60-127">Lai pievienotu eksperimentu, palaidiet vedni **Pievienot eksperimentu**.</span><span class="sxs-lookup"><span data-stu-id="21e60-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="21e60-128">Vednis palīdz veikt nepieciešamās darbības, lai pievienotu eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="21e60-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="21e60-129">Pabeidzot vedni, jūsu eksperiments ir pievienots, un varianti ir izveidoti un gatavi rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="21e60-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

1. <span data-ttu-id="21e60-130">Lai palaistu vedni, atlasiet cilni **Eksperimenti** vietnes veidotājā un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="21e60-130">To launch the wizard, select the **Experiments** tab in site builder and then select **Connect**.</span></span> <span data-ttu-id="21e60-131">Vai arī vednim varat piekļūt no lapas vai fragmenta redaktora.</span><span class="sxs-lookup"><span data-stu-id="21e60-131">Alternatively, the wizard can be accessed from a page or fragment editor.</span></span> <span data-ttu-id="21e60-132">Rediģēšanas režīmā komandjoslā atlasiet **Pievienot eksperimentu**.</span><span class="sxs-lookup"><span data-stu-id="21e60-132">In edit mode, select **Connect experiment** in the command bar.</span></span>

> [!NOTE]
> <span data-ttu-id="21e60-133">Lapu var vienlaicīgi pievienot tikai vienam eksperimentam.</span><span class="sxs-lookup"><span data-stu-id="21e60-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="21e60-134">Lai pievienotu lapu citam eksperimentam, vispirms dzēsiet eksperimentu, ar kuru lapa ir savienota pašlaik.</span><span class="sxs-lookup"><span data-stu-id="21e60-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="21e60-135">Izvēlieties lapu vai fragmentu, kurā vēlaties izpildīt eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="21e60-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="21e60-136">Iestatiet eksperimenta tvērumu uz **daļēju** vai **pilnīgu**, pamatojoties uz izvēli, ko veicāt augstāk minētajā sadaļā [Eksperimenta tvēruma noteikšana](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="21e60-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="21e60-137">Lai eksperimentētu ar visu lapu vai fragmentu, ir jāiespējo līdzekļa karodziņš **Eksperimentēt ar lapām vai fragmentiem**.</span><span class="sxs-lookup"><span data-stu-id="21e60-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="21e60-138">Papildinformāciju skatiet tēmā [Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="21e60-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="21e60-139">Vedņa pēdējā darbībā atlasiet **Ģenerēt variantus un iziet no vedņa**.</span><span class="sxs-lookup"><span data-stu-id="21e60-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="21e60-140">Eksperimentam tiek izveidoti varianti.</span><span class="sxs-lookup"><span data-stu-id="21e60-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="21e60-141">Variantu rediģēšana</span><span class="sxs-lookup"><span data-stu-id="21e60-141">Edit your variations</span></span>
<span data-ttu-id="21e60-142">Izejot no vedņa, tiek izveidoti varianti.</span><span class="sxs-lookup"><span data-stu-id="21e60-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="21e60-143">Pēc tam jūs rediģēsiet variantus, lai tie atspoguļotu eksperimenta hipotēzes pārbaudāmās izvēles.</span><span class="sxs-lookup"><span data-stu-id="21e60-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="21e60-144">Izvēlieties kādu no šīm procedūrām, kas atbilst eksperimenta tvērumam, ko izvēlējāties iepriekšējā sadaļā [Eksperimenta tvēruma noteikšana](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="21e60-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="21e60-145">Variantu rediģēšana eksperimentiem ar daļēju tvērumu</span><span class="sxs-lookup"><span data-stu-id="21e60-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="21e60-146">Izpildiet šīs darbības, ja eksperimenta tvērumu definējāt kā **daļēju** vednī **Pievienot eksperimentu**.</span><span class="sxs-lookup"><span data-stu-id="21e60-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="21e60-147">Redaktora skatā izmantojiet zem komandjoslas esošo variantu nolaižamo izvēlni, lai rediģētu katru variantu, pamatojoties uz sākotnējo hipotēzi.</span><span class="sxs-lookup"><span data-stu-id="21e60-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="21e60-148">Varat arī izveidot kontroles vai pamata variantu, atstājot kādu no variantiem nemainītu.</span><span class="sxs-lookup"><span data-stu-id="21e60-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="21e60-149">Atlasiet moduli ar ko eksperimentēt, atlasot daudzpunktes (...) un pēc tam atlasot **Pievienot eksperimentam**.</span><span class="sxs-lookup"><span data-stu-id="21e60-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="21e60-150">Variantu rediģēšana eksperimentiem ar pilnīgu tvērumu</span><span class="sxs-lookup"><span data-stu-id="21e60-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="21e60-151">Ja definējāt eksperimenta tvērumu kā **pilnīgu** vednī **Pievienot eksperimentu**, tad redaktora skatā izmantojiet zem komandjoslas esošo variantu nolaižamo izvēlni, lai rediģētu katru variantu, pamatojoties uz sākotnējo hipotēzi.</span><span class="sxs-lookup"><span data-stu-id="21e60-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="21e60-152">Jebkurā gadījumā varat arī izveidot kontroles vai pamata variantu, atstājot kādu no variantiem nemainītu.</span><span class="sxs-lookup"><span data-stu-id="21e60-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="21e60-153">Iepriekšējā darbība</span><span class="sxs-lookup"><span data-stu-id="21e60-153">Previous step</span></span>
[<span data-ttu-id="21e60-154">Eksperimenta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="21e60-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="21e60-155">Nākamā darbība</span><span class="sxs-lookup"><span data-stu-id="21e60-155">Next step</span></span>
[<span data-ttu-id="21e60-156">Eksperimenta priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="21e60-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
