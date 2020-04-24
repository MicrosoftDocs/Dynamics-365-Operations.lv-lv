---
title: Līdzekļu kritiskuma veidi
description: Tēmā ir paskaidrot līdzekļu kritiskuma veidi Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c6d3742425a3b92282a62c142b9c325e2d7042f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216601"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="a8eb5-103">Līdzekļu kritiskuma veidi</span><span class="sxs-lookup"><span data-stu-id="a8eb5-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a8eb5-104">Tēmā ir paskaidrot līdzekļu kritiskuma veidi Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="a8eb5-105">Līdzekļu kritiskums ir saistīts ar līdzekļiem un tiek pārsūtīts uz darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="a8eb5-106">Darba pasūtījumā to mainīt nevar.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-106">It can't be changed on a work order.</span></span> <span data-ttu-id="a8eb5-107">Līdzekļu kritiskumu izmanto, lai darba pasūtījumu ieplānošanas laikā aprēķinātu darba pasūtījuma kritiskumu.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="a8eb5-108">Citiem vārdiem sakot, tas tiek izmantots, lai aprēķinātu, cik lielā mērā līdzekļa uzturēšanas darbs ietekmē ražošanas grafiku un produktivitāti jūsu uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="a8eb5-109">Plašāku informāciju par iestatījumiem, kas ir saistīti ar vērtējuma rezultātu aprēķināšanu darba pasūtījumu plānošanai, skatiet nodaļā [Līdzekļu pārvaldības parametri](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a8eb5-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="a8eb5-110">Lai iestatītu kritiskumu, vispirms izveidojiet kritiskuma veidus, kas jāizmanto līdzekļa iestatīšanā.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="a8eb5-111">Pēc tam iestatiet līdzekļa kritiskās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="a8eb5-112">Kritiskuma veidu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a8eb5-112">Set up criticality types</span></span>

1. <span data-ttu-id="a8eb5-113">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Kritiskuma veidi**.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="a8eb5-114">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a8eb5-115">Laukā **Kritiskums** ievadiet skaitli, kas norāda kritiskumu.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="a8eb5-116">Laukā **Nosaukums** ievadiet kritiskuma veida nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="a8eb5-117">Laukā **Koeficients** ievadiet koeficientu.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="a8eb5-118">Šis koeficients tiek izmantots darba pasūtījuma plānošanas aprēķināšanas laikā, lai noteiktu, kādu kritiskuma ierakstu izmantot.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="a8eb5-119">(Vienmēr tiek izmantots ieraksts, kuram ir augstākais koeficients.) Šis iestatījums ir atbilstošs, ja, kā parādīts nākamajā attēlā, tiek veidotas kritiskuma rindas, kurām ir tāda pati kritiskuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Kritiskuma veidu lapa](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="a8eb5-121">Līdzekļa kritisko vērtību iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a8eb5-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="a8eb5-122">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa kritiskās vērtības**.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="a8eb5-123">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a8eb5-124">Atkarībā no līdzekļu kritiskuma nepieciešamā detalizācijas līmeņa veiciet atbilstīgu atlasi laukos **Funkcionālais novietojums**, **Līdzekļa veids**, **Ražotājs**, **Modelis**, **Līdzeklis**, **Darba veida kategorija**, **Darba veids**, **Darba veida variants** un **Darba vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a8eb5-125">Kad līdzekļa kritiskums ir atlasīts, Līdzekļu pārvaldība iziet cauri visiem līdzekļu kritiskuma ierakstiem, lai pārbaudītu iespējamo atbilstību.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="a8eb5-126">Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="a8eb5-127">Citiem vārdiem sakot, Līdzekļu pārvaldība vispirms pārbauda **Darba vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="a8eb5-128">Ja atbilstība netiek atrasta, tā pārbauda **Darba veida variantu**.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="a8eb5-129">Ja atbilstība netiek atrasta, tā pārbauda **Darba veidu** un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="a8eb5-130">Kā jūs varat redzēt lapas izkārtojumā, šī uzvedība nozīmē, ka, lai atrastu visspecifiskāko kombināciju, Līdzekļu pārvaldība atbilstības meklēšanai pārbauda katru ierakstu no labās puses uz kreiso.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="a8eb5-131">Ja atbilstība netiek atrasta, tiek izmantots "noklusējuma" ieraksts, kam nav atlases iespēju.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="a8eb5-132">Laukā **Kritiskums** atlasiet vienu no kritiskuma vērtībām, kuru izveidojāt iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="a8eb5-133">Piezīmes par kritiskuma iestatīšanu</span><span class="sxs-lookup"><span data-stu-id="a8eb5-133">Notes about criticality setup</span></span>

- <span data-ttu-id="a8eb5-134">Ja maināt līdzekļa kritiskumu šajā iestatījumā pēc tam, kad esat to jau izmantojis darba pasūtījumā, kritiskums darba pasūtījumā netiek attiecīgi atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="a8eb5-135">Kritiskums darba pasūtījumā tiek pārrēķināts katru reizi, kad darba pasūtījuma rinda tiek pievienota vai dzēsta darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="a8eb5-136">Ja darba pasūtījumā ir vairāki darba pasūtījuma darbi, darba pasūtījumā vienmēr tiek izmantots augstākais kritiskums saskaņā ar lauku **Koeficients** lapā **Kritiskuma veidi**.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="a8eb5-137">Parasti līdzekļu kritiskums laika posmā var mainīties.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="a8eb5-138">Kritiskumu var ietekmēt jaunu iekārtu iegāde, atjaunošana un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="a8eb5-139">Apsveriet iespēju regulāri no jauna izvērtēt savu līdzekļu kritiskās vērtības (piemēram, reizi gadā vai katru otro gadu), lai nodrošinātu, ka jūsu kritiskuma definīcijas atbilst aktuālajiem ražošanas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
