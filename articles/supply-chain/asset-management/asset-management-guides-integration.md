---
title: Integrēt Dynamics 365 Supply Chain Management (Līdzekļu pārvaldība) ar Dynamics 365 Guides
description: Šajā tēmā skaidrots, kā integrēt Līdzekļu pārvaldības moduli programmā Microsoft  Dynamics 365 Supply Chain Management ar Dynamics 365 Guides, lai izmantotu jauktās realitātes ceļvežiem jūsu ikdienas pakalpojumos un uzturēšanas darbplūsmās.
author: kamaybac
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 4af14a66c839ccee02008057ad1de8ef5b9d291b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813921"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="6cd19-103">Integrēt Dynamics 365 Supply Chain Management (Līdzekļu pārvaldība) ar Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="6cd19-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="6cd19-104">Jūs varat integrēt **Līdzekļu pārvaldības** moduli programmā Microsoft Dynamics 365 Supply Chain Management ar Dynamics 365 Guides, lai izmantotu jauktās realitātes ceļvežus jūsu ikdienas pakalpojumos un uzturēšanas darbplūsmās.</span><span class="sxs-lookup"><span data-stu-id="6cd19-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="6cd19-105">Ja ceļvedis ir saistīts ar Līdzekļu pārvaldības darba pasūtījumu, darbinieks, kurš atver darba pasūtījuma uzturēšanas kontrolsarakstu Supply Chain Management (Dynamics 365) mobilajā programmā, redz, ka ceļvedis ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="6cd19-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="6cd19-106">Darbinieks pēc tam var atrast un atvērt ceļvedi programmā Dynamics 365 Guides HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6cd19-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6cd19-107">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="6cd19-107">Prerequisites</span></span>

<span data-ttu-id="6cd19-108">Pirms varat pievienot ceļvežus Līdzekļu pārvaldības darba pasūtījumiem, ir jāveic šie priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="6cd19-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="6cd19-109">[Uzstādīt Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) 10.0.9 versiju vai jaunāku versiju.</span><span class="sxs-lookup"><span data-stu-id="6cd19-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="6cd19-110">[Ieslēgt duālo rakstīšanu Supply Chain Management programmām](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="6cd19-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="6cd19-111">[Ieslēgt lidojumu](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) **MRGuidesFeature** līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="6cd19-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="6cd19-112">(Ražošanas vidēm vispirms jāiesniedz atbalsta biļete, lai jūsu nomnieks būtu pievienots lidojuma grupai.)</span><span class="sxs-lookup"><span data-stu-id="6cd19-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="6cd19-113">[Ieslēgt šādas konfigurācijas atslēgas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) lapā **Licences konfigurācija**:</span><span class="sxs-lookup"><span data-stu-id="6cd19-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="6cd19-114">Līdzekļu pārvaldība \> Līdzekļu pārvaldības jauktā realitāte</span><span class="sxs-lookup"><span data-stu-id="6cd19-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="6cd19-115">Jauktā realitāte \> Jauktās realitātes ceļvedis</span><span class="sxs-lookup"><span data-stu-id="6cd19-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="6cd19-116">[Uzstādīt Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) 200.0.0.96 versiju vai jaunāku versiju.</span><span class="sxs-lookup"><span data-stu-id="6cd19-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="6cd19-117">Izmantot Dynamics 365 Guides ar Līdzekļu pārvaldību</span><span class="sxs-lookup"><span data-stu-id="6cd19-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="6cd19-118">Lai piesaistītu ceļvedi, Līdzekļu pārvaldībā jāizmanto uzturēšanas kontrolsaraksta rinda.</span><span class="sxs-lookup"><span data-stu-id="6cd19-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="6cd19-119">Varat izveidot saistību, izmantojot uzturēšanas kontrolsaraksta veidni, uzturēšanas darba veidu vai darba pasūtījumu, jo visi trīs ietver uzturēšanas kontrolsaraksta rindas.</span><span class="sxs-lookup"><span data-stu-id="6cd19-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="6cd19-120">Varat ietaupīt laiku, izmantojot veidni, jo veidne var tikt saistīta ar visiem uzturēšanas darbu veidiem, kas to izmanto.</span><span class="sxs-lookup"><span data-stu-id="6cd19-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="6cd19-121">Piemēram, ceļvedis, kas ir saistīts ar uzturēšanas darba veidu, tiek automātiski saistīts ar visiem darba pasūtījumiem, kas norāda šo darba veidu.</span><span class="sxs-lookup"><span data-stu-id="6cd19-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="6cd19-122">No otras puses, ceļvedis, kas ir tieši saistīts ar darba pasūtījumu, pastāv tikai šim darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="6cd19-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="6cd19-123">Saistīt ceļvedi ar uzturēšanas kontrolsaraksta veidni</span><span class="sxs-lookup"><span data-stu-id="6cd19-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="6cd19-124">Lai saistītu ceļvedi ar uzturēšanas kontrolsaraksta veidni, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="6cd19-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="6cd19-125">Izveidojiet ceļvedi, izmantojot Dynamics 365 Guides datoru un HoloLens programmas.</span><span class="sxs-lookup"><span data-stu-id="6cd19-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="6cd19-126">Informāciju par to, kā izveidot ceļvedi, skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="6cd19-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="6cd19-127">Izmantot datora programmu, lai izveidotu ceļvedi</span><span class="sxs-lookup"><span data-stu-id="6cd19-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="6cd19-128">Izmantot HoloLens programmu, lai ievietotu jūsu hologrammas</span><span class="sxs-lookup"><span data-stu-id="6cd19-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="6cd19-129">Supply Chain Management [izveidojiet uzturēšanas kontrolsaraksta veidni](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span><span class="sxs-lookup"><span data-stu-id="6cd19-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="6cd19-130">Saistiet ceļvedi, ko izveidojāt ar uzturēšanas kontrolsaraksta rindu jaunajā uzturēšanas kontrolsaraksta veidnē:</span><span class="sxs-lookup"><span data-stu-id="6cd19-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="6cd19-131">Kopsavilkuma cilnē **Uzturēšanas kontrolsaraksta rindas** atlasiet rindu, ar kuru vēlaties saistīt ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="6cd19-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="6cd19-132">Kopsavilkuma cilnē **Saistītie ceļveži** atlasiet **Pievienot ceļvedi**.</span><span class="sxs-lookup"><span data-stu-id="6cd19-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="6cd19-133">![Saistīt ceļvedi ar uzturēšanas kontrolsaraksta rindu](media/am-guides-integration-add-guide.png "Saistīt ceļvedi ar uzturēšanas kontrolsaraksta rindu")</span><span class="sxs-lookup"><span data-stu-id="6cd19-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="6cd19-134">Laukā **Nosaukums** atlasiet ceļvedi un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6cd19-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="6cd19-135">![Atlasīt ceļvedi Nosaukuma laukā](media/am-guides-integration-select-guide.png "Atlasīt ceļvedi Nosaukuma laukā")</span><span class="sxs-lookup"><span data-stu-id="6cd19-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="6cd19-136">Saistīt uzturēšanas kontrolsaraksta veidni ar darba veidu:</span><span class="sxs-lookup"><span data-stu-id="6cd19-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="6cd19-137">[Izveidot uzturēšanas darba veidu](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) vai atlasīt jau esošu uzturēšanas darba veidu.</span><span class="sxs-lookup"><span data-stu-id="6cd19-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="6cd19-138">Darbības rūtī atlasiet **Uzturēšanas darba veida noklusējumi**.</span><span class="sxs-lookup"><span data-stu-id="6cd19-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="6cd19-139">![Uzturēšanas darba veida noklusējumu poga](media/am-guides-integration-job-defaults.png "Uzturēšanas darba veida noklusējumu poga")</span><span class="sxs-lookup"><span data-stu-id="6cd19-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="6cd19-140">Izveidojiet rindu un tad atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6cd19-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="6cd19-141">![Izveidot rindu](media/am-guides-integration-add-line.png "Izveidot rindu")</span><span class="sxs-lookup"><span data-stu-id="6cd19-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="6cd19-142">Darbību rūtī atlasiet **Uzturēšanas kontrolsaraksts**.</span><span class="sxs-lookup"><span data-stu-id="6cd19-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="6cd19-143">![Uzturēšanas kontrolsaraksta poga](media/am-guides-integration-maintenance-checklist.png "Uzturēšanas kontrolsaraksta poga")</span><span class="sxs-lookup"><span data-stu-id="6cd19-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="6cd19-144">Kopsavilkuma cilnē **Uzturēšanas kontrolsaraksta rindas** pievienojiet rindu un pēc tam mainiet lauka **Veids** vērtību uz **Veidne**.</span><span class="sxs-lookup"><span data-stu-id="6cd19-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="6cd19-145">![Mainīt Veida vērtību](media/am-guides-integration-checklist-lines.png "Mainīt Veida vērtību")</span><span class="sxs-lookup"><span data-stu-id="6cd19-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="6cd19-146">Kopsavilkuma cilnē **Rindas detaļas** laukā **Veidne** atlasiet veidni, ar kuru esat saistījis ceļvedi, un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="6cd19-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="6cd19-147">![Atlasīt veidni](media/am-guides-integration-checklist-line-details.png "Atlasīt veidni")</span><span class="sxs-lookup"><span data-stu-id="6cd19-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="6cd19-148">[Izveidot darba pasūtījumu](work-orders/manually-created-workorders.md#create-work-order) un pēc tam atlasīt uzturēšanas darba veidu, kas izmanto uzturēšanas kontrolsaraksta veidni, ar kuru ir saistīts ceļvedis.</span><span class="sxs-lookup"><span data-stu-id="6cd19-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="6cd19-149">Ceļvedis ir automātiski saistīts ar darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="6cd19-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="6cd19-150">![Atlasīt uzturēšanas darba veidu](media/am-guides-integration-create-work-order.png "Atlasīt uzturēšanas darba veidu")</span><span class="sxs-lookup"><span data-stu-id="6cd19-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="6cd19-151">Skatiet ceļvedi, kas saistīts ar darba pasūtījumu un darbiniekiem:</span><span class="sxs-lookup"><span data-stu-id="6cd19-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="6cd19-152">Atveriet [Pamatlīdzekļu pārvaldības mobilo darbvieta](asset-management-mobile-workspace.md), lai piekļūtu darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="6cd19-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="6cd19-153">[Atveriet uzturēšanas kontrolsarakstu](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) darba pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="6cd19-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="6cd19-154">Atlasiet kontrolsaraksta rindu, lai apskatītu saistīto ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="6cd19-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="6cd19-155">![Ceļvedis, kas saistīts ar kontrolsaraksta rindu](media/am-guides-integration-show-guide.png "Ceļvedis, kas saistīts ar kontrolsaraksta rindu")</span><span class="sxs-lookup"><span data-stu-id="6cd19-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="6cd19-156">Atveriet ceļvedi programmā HoloLens.</span><span class="sxs-lookup"><span data-stu-id="6cd19-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="6cd19-157">![Atveriet ceļvedi programmā HoloLens](media/am-guides-integration-hololens-select.png "Atveriet ceļvedi programmā HoloLens")</span><span class="sxs-lookup"><span data-stu-id="6cd19-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="6cd19-158">Varat arī saistīt ceļvedi tieši darba pasūtījuma vai darba veida uzturēšanas kontrolsarakstā.</span><span class="sxs-lookup"><span data-stu-id="6cd19-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cd19-159">Pastāv zināma problēma, kur, saistot uzturēšanas kontrolsaraksta veidni ar noklusējuma uzturēšanas darba veidu, ceļvedis, kas ir saistīts ar veidni, netiek parādīts kopsavilkuma cilnē **Saistītie ceļveži** lapā **Uzturēšanas darba veida noklusējumi**.</span><span class="sxs-lookup"><span data-stu-id="6cd19-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="6cd19-160">Tomēr ceļvedis parādīsies pēc tam, kad darbaveids tiek lietots darba pasūtījumam kopsavilkuma cilnē **Saistītie ceļveži**.</span><span class="sxs-lookup"><span data-stu-id="6cd19-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="6cd19-161">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="6cd19-161">See also</span></span>

- [<span data-ttu-id="6cd19-162">Duālā ieraksta pārskats</span><span class="sxs-lookup"><span data-stu-id="6cd19-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="6cd19-163">Pārskats par līdzekļu pārvaldību</span><span class="sxs-lookup"><span data-stu-id="6cd19-163">Asset management overview</span></span>](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]