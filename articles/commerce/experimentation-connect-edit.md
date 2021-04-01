---
title: Eksperimenta pievienošana un variantu rediģēšana
description: Šajā tēmā ir aprakstīts, kā pievienot eksperimentu trešās puses pakalpojumam Dynamics 365 Commerce un kā rediģēt eksperimenta variantus.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c295f6f8170b6314ddf2d0c3582343b312c815b6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238658"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="9269a-103">Eksperimenta pievienošana un variantu rediģēšana</span><span class="sxs-lookup"><span data-stu-id="9269a-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="9269a-104">Šajā tēmā ir aprakstīts, kā pievienot eksperimentu pakalpojumā Commerce un kā veikt izmaiņas variantiem tā, lai tie atbilstu hipotēzei.</span><span class="sxs-lookup"><span data-stu-id="9269a-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="9269a-105">Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9269a-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="9269a-106">Papildu darbības ir apskatītas atsevišķās tēmās.</span><span class="sxs-lookup"><span data-stu-id="9269a-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="9269a-107">[ ![Eksperimenta lietotāja maršruts – pievienošana un rediģēšana](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9269a-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="9269a-108">Pēc [eksperimenta iestatīšanas](experimentation-setup.md) trešās puses pakalpojumā, jūs pievienosit eksperimentu Dynamics 365 Commerce un rediģēsit eksperimenta variantus.</span><span class="sxs-lookup"><span data-stu-id="9269a-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="9269a-109">Plānošanas apsvērumi</span><span class="sxs-lookup"><span data-stu-id="9269a-109">Planning considerations</span></span>

<span data-ttu-id="9269a-110">Pirms pievienojat eksperimentu pakalpojumā Commerce, jums ir jāpieņem daži lēmumi, kas ietekmē veidu, kādā Commerce pārvalda jūsu saturu.</span><span class="sxs-lookup"><span data-stu-id="9269a-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="9269a-111">Eksperimenta tvēruma noteikšana</span><span class="sxs-lookup"><span data-stu-id="9269a-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="9269a-112">Kad pievienojat eksperimentu, jums tiek piedāvāts definēt eksperimenta tvērumu.</span><span class="sxs-lookup"><span data-stu-id="9269a-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="9269a-113">Eksperimenti ir definēti kā **daļēja** tvēruma vai **pilnīga** tvēruma.</span><span class="sxs-lookup"><span data-stu-id="9269a-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="9269a-114">Izvēlieties **daļēja**, ja vēlaties veikt eksperimentu noteiktā lapas daļā.</span><span class="sxs-lookup"><span data-stu-id="9269a-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="9269a-115">Atlasot šo opciju, ir jānosaka, kuri moduļi ir ietverti eksperimentā.</span><span class="sxs-lookup"><span data-stu-id="9269a-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="9269a-116">Izmaiņas, kas tiek veiktas noklusējuma lapas vai fragmenta daļām, kas nav saistītas ar eksperimentu, tiek automātiski sinhronizētas starp variantiem.</span><span class="sxs-lookup"><span data-stu-id="9269a-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="9269a-117">Izvēlieties **pilnīga**, ja vēlaties veikt eksperimentu visā lapā vai fragmentā.</span><span class="sxs-lookup"><span data-stu-id="9269a-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="9269a-118">Tiek izveidotas atsevišķas noklusējuma lapas vai fragmenta kopijas.</span><span class="sxs-lookup"><span data-stu-id="9269a-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="9269a-119">Nav nepieciešams atlasīt, kuri moduļi tiek ietverti eksperimentā, jo izmaiņām ir pieejama visa rediģēšanas virsma.</span><span class="sxs-lookup"><span data-stu-id="9269a-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="9269a-120">Moduļus varat pievienot, dzēst vai pārkārtot pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="9269a-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="9269a-121">Tomēr, ja tiek veiktas izmaiņas noklusējuma lapā vai fragmentā, ar kuru ir saistīts eksperiments, šīs izmaiņas ir manuāli jāsinhronizē visos variantos.</span><span class="sxs-lookup"><span data-stu-id="9269a-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="9269a-122">Saistot eksperimentu ar lapu, kurā tiek izmantots izkārtojums, eksperimenta tvērums var būt tikai **pilnīgs**.</span><span class="sxs-lookup"><span data-stu-id="9269a-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="9269a-123">Izlemiet, vai vēlaties ieplānot eksperimenta publicēšanu</span><span class="sxs-lookup"><span data-stu-id="9269a-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="9269a-124">Ja vēlaties ieplānot eksperimenta publicēšanu tiešsaistes vietnē, pārliecinieties, ka saturs, kuru vēlaties saistīt ar eksperimentu, ir pieejams publicēšanas grupā *pirms* eksperimenta pievienošanas.</span><span class="sxs-lookup"><span data-stu-id="9269a-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="9269a-125">Papildinformāciju par publicēšanas grupām, skatiet sadaļā [Darbs ar publicēšanas grupām](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="9269a-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="9269a-126">Eksperimenta pievienošana</span><span class="sxs-lookup"><span data-stu-id="9269a-126">Connect your experiment</span></span>
<span data-ttu-id="9269a-127">Lai pievienotu eksperimentu, palaidiet vedni **Pievienot eksperimentu**.</span><span class="sxs-lookup"><span data-stu-id="9269a-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="9269a-128">Vednis palīdz veikt nepieciešamās darbības, lai pievienotu eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="9269a-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="9269a-129">Pabeidzot vedni, jūsu eksperiments ir pievienots, un varianti ir izveidoti un gatavi rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="9269a-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="9269a-130">Lai sāktu eksperimenta savienošanu Commerce vietnes veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9269a-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9269a-131">Lai palaistu vedni **Savienot eksperimentu**, kreisajā navigācijas rūtī atlasiet **Eksperimenti** un pēc tam atlasiet **Savienot**.</span><span class="sxs-lookup"><span data-stu-id="9269a-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="9269a-132">Vai arī varam vednim piekļūt no lapas vai fragmentu redaktora, rediģējot to un komandjoslā atlasot **Savienot eksperimentu**.</span><span class="sxs-lookup"><span data-stu-id="9269a-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9269a-133">Lapu var vienlaicīgi pievienot tikai vienam eksperimentam.</span><span class="sxs-lookup"><span data-stu-id="9269a-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="9269a-134">Lai pievienotu lapu citam eksperimentam, vispirms dzēsiet eksperimentu, ar kuru lapa ir savienota pašlaik.</span><span class="sxs-lookup"><span data-stu-id="9269a-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="9269a-135">Izvēlieties lapu vai fragmentu, kurā vēlaties izpildīt eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="9269a-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="9269a-136">Iestatiet eksperimenta tvērumu uz **daļēju** vai **pilnīgu**, pamatojoties uz izvēli, ko veicāt augstāk minētajā sadaļā [Eksperimenta tvēruma noteikšana](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="9269a-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="9269a-137">Lai eksperimentētu ar visu lapu vai fragmentu, ir jāiespējo līdzekļa karodziņš **Eksperimentēt ar lapām vai fragmentiem**.</span><span class="sxs-lookup"><span data-stu-id="9269a-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="9269a-138">Papildinformāciju skatiet tēmā [Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9269a-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="9269a-139">Vedņa pēdējā darbībā atlasiet **Ģenerēt variantus un iziet no vedņa**.</span><span class="sxs-lookup"><span data-stu-id="9269a-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="9269a-140">Eksperimentam tiek izveidoti varianti.</span><span class="sxs-lookup"><span data-stu-id="9269a-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="9269a-141">Variantu rediģēšana</span><span class="sxs-lookup"><span data-stu-id="9269a-141">Edit your variations</span></span>
<span data-ttu-id="9269a-142">Izejot no vedņa, tiek izveidoti varianti.</span><span class="sxs-lookup"><span data-stu-id="9269a-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="9269a-143">Pēc tam jūs rediģēsiet variantus, lai tie atspoguļotu eksperimenta hipotēzes pārbaudāmās izvēles.</span><span class="sxs-lookup"><span data-stu-id="9269a-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="9269a-144">Izvēlieties kādu no šīm procedūrām, kas atbilst eksperimenta tvērumam, ko izvēlējāties iepriekšējā sadaļā [Eksperimenta tvēruma noteikšana](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="9269a-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="9269a-145">Variantu rediģēšana eksperimentiem ar daļēju tvērumu</span><span class="sxs-lookup"><span data-stu-id="9269a-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="9269a-146">Izpildiet šīs darbības, ja eksperimenta tvērumu definējāt kā **daļēju** vednī **Pievienot eksperimentu**.</span><span class="sxs-lookup"><span data-stu-id="9269a-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="9269a-147">Redaktora skatā izmantojiet zem komandjoslas esošo variantu nolaižamo izvēlni, lai rediģētu katru variantu, pamatojoties uz sākotnējo hipotēzi.</span><span class="sxs-lookup"><span data-stu-id="9269a-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="9269a-148">Varat arī izveidot kontroles vai pamata variantu, atstājot kādu no variantiem nemainītu.</span><span class="sxs-lookup"><span data-stu-id="9269a-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="9269a-149">Atlasiet moduli ar ko eksperimentēt, atlasot daudzpunktes (...) un pēc tam atlasot **Pievienot eksperimentam**.</span><span class="sxs-lookup"><span data-stu-id="9269a-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="9269a-150">Variantu rediģēšana eksperimentiem ar pilnīgu tvērumu</span><span class="sxs-lookup"><span data-stu-id="9269a-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="9269a-151">Ja definējāt eksperimenta tvērumu kā **pilnīgu** vednī **Pievienot eksperimentu**, tad redaktora skatā izmantojiet zem komandjoslas esošo variantu nolaižamo izvēlni, lai rediģētu katru variantu, pamatojoties uz sākotnējo hipotēzi.</span><span class="sxs-lookup"><span data-stu-id="9269a-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="9269a-152">Jebkurā gadījumā varat arī izveidot kontroles vai pamata variantu, atstājot kādu no variantiem nemainītu.</span><span class="sxs-lookup"><span data-stu-id="9269a-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="9269a-153">Iepriekšējā darbība</span><span class="sxs-lookup"><span data-stu-id="9269a-153">Previous step</span></span>
[<span data-ttu-id="9269a-154">Eksperimenta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9269a-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="9269a-155">Nākamā darbība</span><span class="sxs-lookup"><span data-stu-id="9269a-155">Next step</span></span>
[<span data-ttu-id="9269a-156">Eksperimenta priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="9269a-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]