---
title: Eksperimenta priekšskatīšana un publicēšana
description: Šajā tēmā ir aprakstīts, kā priekšskatīt un publicēt eksperimentu no Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/22/2020
ms.locfileid: "4414188"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="8f1b7-103">Eksperimenta priekšskatīšana un publicēšana</span><span class="sxs-lookup"><span data-stu-id="8f1b7-103">Preview and publish an experiment</span></span>

<span data-ttu-id="8f1b7-104">Šajā tēmā ir aprakstīts, kā priekšskatīt un publicēt eksperimentu pakalpojumā Dynamics 365 Commerce pēc tam, kad esat [pievienojis eksperimentu un rediģējis variantus](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="8f1b7-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="8f1b7-105">Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8f1b7-106">Papildu darbības ir apskatītas atsevišķās tēmās.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="8f1b7-107">[ ![Eksperimenta lietotāja maršruts – priekšskatīšana un publicēšana](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="8f1b7-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="8f1b7-108">Eksperimenta variantu priekšskatīšana</span><span class="sxs-lookup"><span data-stu-id="8f1b7-108">Preview your experiment variations</span></span>
<span data-ttu-id="8f1b7-109">Varat priekšskatīt variantus un turpināt to rediģēšanu, līdz tie izskatās tā, kā vēlaties.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="8f1b7-110">Lai priekšskatītu eksperimenta variantus Commerce vietnes veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="8f1b7-111">Zem komandjoslas esošajā variantu nolaižamajā izvēlnē atlasiet priekšskatāmo saturu.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="8f1b7-112">Komandjoslā atlasiet **Priekšskatīt**.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="8f1b7-113">Tiek parādīts publicējamā satura priekšskatījums.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="8f1b7-114">Lai priekšskatītu citu variantu, atlasiet to variantu nolaižamajā izvēlnē un vēlreiz atlasiet **Priekšskatīt**.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="8f1b7-115">Eksperimenta publicēšana</span><span class="sxs-lookup"><span data-stu-id="8f1b7-115">Publish your experiment</span></span>
<span data-ttu-id="8f1b7-116">Ja neizmantojat publicēšanas grupu, lai ieplānotu eksperimenta sākumu, un vēlaties to publicēt nekavējoties, komandjoslā atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="8f1b7-117">Tiks publicēti visi eksperimentam piederošie varianti.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="8f1b7-118">Ja lapai ir nepublicēts URL, vispirms URL jāpublicē, pretējā gadījumā tas nebūs redzams tīmekļa vietnes lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="8f1b7-119">Papildinformāciju skatiet sadaļā [Lapas saglabāšana, priekšskatīšana un publicēšana](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="8f1b7-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="8f1b7-120">Publicēšanas grupu izmantošana, lai ieplānotu eksperimenta sākumu</span><span class="sxs-lookup"><span data-stu-id="8f1b7-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="8f1b7-121">Vietnes veidotājā izveidoto variantu publicēšana var tikt ieplānota, izmantojot publicēšanas grupu.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="8f1b7-122">Publicētajā grupā varat pievienot lapu vai fragmentu savam eksperimentam, kreisajā navigācijas rūtī atlasot **Eksperimenti**.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="8f1b7-123">To var arī izdarīt, atlasot **Lapas** vai **Fragmenti** un izpildot instrukcijas sadaļā [Eksperimenta pievienošana un variantu rediģēšana](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="8f1b7-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="8f1b7-124">Informāciju par publicēšanas grupām, skatiet sadaļā [Darbs ar publicēšanas grupām](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="8f1b7-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="8f1b7-125">Izmantojot publicēšanas grupas ar eksperimentiem, ir jāņem vērā daži svarīgi apsvērumi.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="8f1b7-126">Kad publicēšanas grupai pievienojat lapu vai fragmentu, kurā tiek izpildīts eksperiments, publicēšanas grupā eksperiments tiks noņemts no lapas vai fragmenta.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="8f1b7-127">Eksperimenti, kas ir pievienoti lapām tiešsaistes vietnē, nav pieejami publicēšanas grupu lapām un otrādi.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="8f1b7-128">Līdzīgi lapas, kurās tiek izpildīti eksperimenti tiešsaistes vietnē, nav pieejamas citiem eksperimentiem publicēšanas grupās un otrādi.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="8f1b7-129">Kad publicējat vai ieplānojat publicēšanas grupu, tiek publicēts viss publicēšanas grupas saturs neatkarīgi no tā, vai ar publicēšanas grupu ir saistīts eksperiments.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="8f1b7-130">Tā kā publicēšanas grupa turpina pastāvēt pēc publicēšanas tiešsaistes vietnē, arī eksperimenti publicēšanas grupā saglabājas.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="8f1b7-131">Tāpēc nevarēsit saistīt citus eksperimentus ar to pašu lapu vai fragmentu.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="8f1b7-132">Lai izvairītos no šī ierobežojuma, dzēsiet visas publicēšanas grupas ar esošajiem eksperimentiem.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="8f1b7-133">Tāpat, ja vēlaties dzēst eksperimentu tiešsaistes vietnē, kas pastāv arī publicēšanas grupā, vispirms dzēsiet to no publicēšanas grupas.</span><span class="sxs-lookup"><span data-stu-id="8f1b7-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="8f1b7-134">Iepriekšējā darbība</span><span class="sxs-lookup"><span data-stu-id="8f1b7-134">Previous step</span></span>
[<span data-ttu-id="8f1b7-135">Eksperimenta pievienošana un rediģēšana</span><span class="sxs-lookup"><span data-stu-id="8f1b7-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="8f1b7-136">Nākamā darbība</span><span class="sxs-lookup"><span data-stu-id="8f1b7-136">Next step</span></span>
[<span data-ttu-id="8f1b7-137">Eksperimenta izpildīšana un pārraudzīšana</span><span class="sxs-lookup"><span data-stu-id="8f1b7-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
