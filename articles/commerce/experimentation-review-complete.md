---
title: Varianta publicēšana un eksperimenta pabeigšana
description: Šajā tēmā ir aprakstīts, kā publicēt veiksmīgu variantu un pabeigt eksperimentu Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930240"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="fe710-103">Varianta publicēšana un eksperimenta pabeigšana</span><span class="sxs-lookup"><span data-stu-id="fe710-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="fe710-104">Šajā tēmā ir aprakstīts, kā publicēt variantu, kas sniedza labākos rezultātus eksperimentā un kā pabeigt eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="fe710-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="fe710-105">Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe710-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="fe710-106">Papildu darbības ir apskatītas atsevišķās tēmās.</span><span class="sxs-lookup"><span data-stu-id="fe710-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="fe710-107">[ ![Eksperimenta lietotāja maršruts - pārskatīšana un pabeigšana](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="fe710-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="fe710-108">Pēc tam, kad [eksperiments ir izpildīts](experimentation-run-monitor.md) un ir apkopoti pietiekami daudz datu, lai noteiktu, kuru variantu vēlaties izmantot savā tiešsaistes vietnē, jūs publicēsit variantu un beigsit eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="fe710-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="fe710-109">Varianta publicēšana</span><span class="sxs-lookup"><span data-stu-id="fe710-109">Promote a variation</span></span>
<span data-ttu-id="fe710-110">Izmantojiet datus un analīzi, kas saistīta ar trešās puses pakalpojuma eksperimentu, lai izlemtu, kurš no variantiem sniedza vislabākos rezultātus.</span><span class="sxs-lookup"><span data-stu-id="fe710-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="fe710-111">Lai aizvietotu pašreizējo saturu tiešsaistes vietnē ar labāko variantu tā, lai tas būtu pieejams visiem tīmekļa vietnes lietotājiem, rīkojieties kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="fe710-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="fe710-112">Dodieties uz **Eksperimenti** cilni vietnes veidotājā un atlasiet eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="fe710-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="fe710-113">Augšējā joslā atlasiet **Pabeigt eksperimentu**.</span><span class="sxs-lookup"><span data-stu-id="fe710-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="fe710-114">Dialoglodziņa izvēlnē **Pabeigt eksperimentu** atlasiet **Pārskatīt eksperimenta datus**.</span><span class="sxs-lookup"><span data-stu-id="fe710-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="fe710-115">Tiek atvērts trešās puses pakalpojums, kur varat validēt rādītājus un noteikt, kurš no variantiem ir vislabākais.</span><span class="sxs-lookup"><span data-stu-id="fe710-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="fe710-116">Dialoglodziņa izvēlnē **Pabeigt eksperimentu** vietnes veidotājā atlasiet labāko variantu un pēc tam atlasiet **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="fe710-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="fe710-117">Atveriet trešās puses pakalpojumu un beidziet eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="fe710-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="fe710-118">Vietnes veidotājā atlasiet **Pabeigt**, lai pārrakstītu sākotnējo tiešsaistes lapu, un publicētu labāko variantu, lai tas būtu pieejams visiem tīmekļa vietnes lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="fe710-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="fe710-119">Ja izvēlaties saglabāt pašreizējo tiešsaistes lapu un nepublicēt variantu, atlasiet **Pārpublicēt sākotnējo lapu**.</span><span class="sxs-lookup"><span data-stu-id="fe710-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="fe710-120">Eksperimenta dzēšana</span><span class="sxs-lookup"><span data-stu-id="fe710-120">Delete your experiment</span></span>
<span data-ttu-id="fe710-121">Lai gan pakalpojumā Commerce nav nepieciešams dzēst pabeigtu eksperimentu, varat izvēlēties to dzēst, lai ietaupītu vietu vai iztīrītu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="fe710-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="fe710-122">Lai dzēstu eksperimentu, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="fe710-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="fe710-123">Dodieties uz **Eksperimenti** cilni vietnes veidotājā un atlasiet eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="fe710-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="fe710-124">Ja eksperiments joprojām ir aktīvs, pirms turpināt, beidziet eksperimentu trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="fe710-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="fe710-125">Komandjoslā atlasiet **Nepublicēt**, lai noņemtu varianta saturu no tiešsaistes vietnes.</span><span class="sxs-lookup"><span data-stu-id="fe710-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="fe710-126">Komandjoslā atlasiet **Dzēst**, lai dzēstu eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="fe710-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="fe710-127">Iepriekšējā darbība</span><span class="sxs-lookup"><span data-stu-id="fe710-127">Previous step</span></span>
[<span data-ttu-id="fe710-128">Eksperimenta izpildīšana un pārraudzīšana</span><span class="sxs-lookup"><span data-stu-id="fe710-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
