---
title: Varianta publicēšana un eksperimenta pabeigšana
description: Šajā tēmā ir aprakstīts, kā publicēt veiksmīgu variantu un pabeigt eksperimentu Dynamics 365 Commerce.
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
ms.openlocfilehash: 25cccbeae5c263a3032eeebf2fc5335e22c1415a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009931"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="8fdc4-103">Varianta publicēšana un eksperimenta pabeigšana</span><span class="sxs-lookup"><span data-stu-id="8fdc4-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="8fdc4-104">Šajā tēmā ir aprakstīts, kā publicēt variantu, kas sniedza labākos rezultātus eksperimentā un kā pabeigt eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="8fdc4-105">Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8fdc4-106">Papildu darbības ir apskatītas atsevišķās tēmās.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="8fdc4-107">[ ![Eksperimenta lietotāja maršruts - pārskatīšana un pabeigšana](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="8fdc4-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="8fdc4-108">Pēc tam, kad [eksperiments ir izpildīts](experimentation-run-monitor.md) un ir apkopoti pietiekami daudz datu, lai noteiktu, kuru variantu vēlaties izmantot savā tiešsaistes vietnē, jūs publicēsit variantu un beigsit eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="8fdc4-109">Varianta publicēšana</span><span class="sxs-lookup"><span data-stu-id="8fdc4-109">Promote a variation</span></span>
<span data-ttu-id="8fdc4-110">Izmantojiet datus un analīzi, kas saistīta ar trešās puses pakalpojuma eksperimentu, lai izlemtu, kurš no variantiem sniedza vislabākos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="8fdc4-111">Pēc tam varat to reklamēt, aizvietokot pašreizējo saturu tiešsaistes vietnē ar labāko variantu tā, lai tas būtu pieejams visiem tīmekļa vietnes lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="8fdc4-112">Lai reklamētu labāko variantu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="8fdc4-113">Commerce vietņu veidotājā kreisajā navigācijas rūtī atlasiet **Eksperimenti** un pēc tam atlasiet eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="8fdc4-114">Komandjoslā atlasiet **Pabeigt eksperimentu**.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="8fdc4-115">Dialoglodziņā **Pabeigt eksperimentu** atlasiet **Pārskatīt eksperimenta datus**.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="8fdc4-116">Tiek atvērts trešās puses pakalpojums, kur varat validēt rādītājus un noteikt, kurš no variantiem ir vislabākais.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="8fdc4-117">Dialoglodziņā **Pabeigt eksperimentu** atlasiet labāko variantu un pēc tam atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="8fdc4-118">Atveriet trešās puses pakalpojumu un beidziet eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="8fdc4-119">Vietnes veidotājā atlasiet **Pabeigt**, lai pārrakstītu sākotnējo tiešsaistes lapu, un publicētu labāko variantu, lai tas būtu pieejams visiem tīmekļa vietnes lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="8fdc4-120">Ja izvēlaties saglabāt pašreizējo tiešsaistes lapu un nepublicēt variantu, atlasiet **Pārpublicēt sākotnējo lapu**.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="8fdc4-121">Eksperimenta dzēšana</span><span class="sxs-lookup"><span data-stu-id="8fdc4-121">Delete your experiment</span></span>
<span data-ttu-id="8fdc4-122">Lai gan pakalpojumā Commerce nav nepieciešams dzēst pabeigtu eksperimentu, varat izvēlēties to dzēst, lai ietaupītu vietu vai iztīrītu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="8fdc4-123">Lai dzēstu eksperimentu Commerce vietņu veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="8fdc4-124">Kreisajā navigācijas rūtī atlasiet **Eksperimenti** un pēc tam atlasiet eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="8fdc4-125">Ja eksperiments joprojām ir aktīvs, pirms turpināt, beidziet eksperimentu trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="8fdc4-126">Komandjoslā atlasiet **Nepublicēt**, lai noņemtu varianta saturu no tiešsaistes vietnes.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="8fdc4-127">Atlasiet **Dzēst**, lai dzēstu eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="8fdc4-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="8fdc4-128">Iepriekšējā darbība</span><span class="sxs-lookup"><span data-stu-id="8fdc4-128">Previous step</span></span>
[<span data-ttu-id="8fdc4-129">Eksperimenta veikšana un uzraudzība</span><span class="sxs-lookup"><span data-stu-id="8fdc4-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
