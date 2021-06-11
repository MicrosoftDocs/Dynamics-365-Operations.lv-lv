---
title: Duālā ieraksta iestatīšana no Lifecycle Services
description: Šajā tēmā skaidrots, kā iestatīt duālo rakstīšanas savienojumu no Microsoft Dynamics pakalpojumiem Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103573"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="b5df3-103">Duālā ieraksta iestatīšana no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b5df3-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b5df3-104">Šajā tēmā skaidrots, kā iespējot duālo rakstīšanu no Microsoft Dynamics pakalpojumiem Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b5df3-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b5df3-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="b5df3-105">Prerequisites</span></span>

<span data-ttu-id="b5df3-106">Jums jāpabeidz Power Platform integrēšana atbilstoši aprakstam šādās tēmās:</span><span class="sxs-lookup"><span data-stu-id="b5df3-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="b5df3-107">Power Platform integrācija - Iespējot vides izvietošanas laikā</span><span class="sxs-lookup"><span data-stu-id="b5df3-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="b5df3-108">Power Platform integrācija - Iestatīt pēc vides izvietošanas</span><span class="sxs-lookup"><span data-stu-id="b5df3-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="b5df3-109">Iestatīt duālo rakstīšanu jaunajām Dataverse vidēm</span><span class="sxs-lookup"><span data-stu-id="b5df3-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="b5df3-110">Veiciet šos soļus, lai iestatītu duālo rakstīšanu no LCS **Vides informācijas** lapas:</span><span class="sxs-lookup"><span data-stu-id="b5df3-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="b5df3-111">Lapā **Vides informācija** izvērsiet **Power Platform integrācijas** sadaļu.</span><span class="sxs-lookup"><span data-stu-id="b5df3-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="b5df3-112">Atlasiet **Duālās rakstīšanas programmas** pogu.</span><span class="sxs-lookup"><span data-stu-id="b5df3-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform integrēšana](media/powerplat_integration_step2.png)

3. <span data-ttu-id="b5df3-114">Pārskatiet noteikumus un nosacījumus un atzīmējiet **Konfigurēt**.</span><span class="sxs-lookup"><span data-stu-id="b5df3-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="b5df3-115">Lai turpinātu, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b5df3-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="b5df3-116">Jūs varat pārraudzīt progresu, periodiski atsvaidzinot vides informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="b5df3-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="b5df3-117">Uzstādīšanai parasti nepieciešamas 30 minūtes vai mazāk.</span><span class="sxs-lookup"><span data-stu-id="b5df3-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="b5df3-118">Kad uzstādīšana ir pabeigta, ziņojums jūs informēs, vai process bija veiksmīgs vai ja tajā radās kļūme.</span><span class="sxs-lookup"><span data-stu-id="b5df3-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="b5df3-119">Ja iestatīšana neizdevās, tiek parādīts saistītais kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="b5df3-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="b5df3-120">Kļūdas jālabo pirms pārcelšanās uz nākamo darbību.</span><span class="sxs-lookup"><span data-stu-id="b5df3-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="b5df3-121">Atlasiet **Saite uz Power Platform vidi**, lai izveidotu saiti starp Dataverse un pašreizējās vides datu bāzēm.</span><span class="sxs-lookup"><span data-stu-id="b5df3-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="b5df3-122">Tas parasti aizņem mazāk kā 5 minūtes.</span><span class="sxs-lookup"><span data-stu-id="b5df3-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Saite uz Power Platform vidi":::

8. <span data-ttu-id="b5df3-124">Kad saistīšana ir pabeigta, tiek parādīta hipersaite.</span><span class="sxs-lookup"><span data-stu-id="b5df3-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="b5df3-125">Izmantojiet saiti, lai pieteiktos duālās rakstīšanas administrācijas apgabalā Finance and Operations vidē.</span><span class="sxs-lookup"><span data-stu-id="b5df3-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="b5df3-126">No turienes varat iestatīt elementu kartējumus.</span><span class="sxs-lookup"><span data-stu-id="b5df3-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="b5df3-127">Iestatīt duālo rakstīšanu jau esošai Dataverse videi</span><span class="sxs-lookup"><span data-stu-id="b5df3-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="b5df3-128">Lai esošajai Dataverse videi iestatītu duālo rakstīšanu, ir jāizveido Microsoft [atbalsta biļete](../../lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="b5df3-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="b5df3-129">Biļetē ir jāietver:</span><span class="sxs-lookup"><span data-stu-id="b5df3-129">The ticket must include:</span></span>

+ <span data-ttu-id="b5df3-130">Jūsu Finance and Operations vides ID.</span><span class="sxs-lookup"><span data-stu-id="b5df3-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="b5df3-131">Jūsu vides nosaukums no Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="b5df3-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="b5df3-132">Dataverse organizācijas ID vai Power Platform vides ID no Power Platform administrēšanas centra.</span><span class="sxs-lookup"><span data-stu-id="b5df3-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="b5df3-133">Jūsu biļetē pieprasiet, lai ID tiktu izmantots Power Platform integrācijai.</span><span class="sxs-lookup"><span data-stu-id="b5df3-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="b5df3-134">Jūs nevarat atsaistīt vides, izmantojot portālu LCS.</span><span class="sxs-lookup"><span data-stu-id="b5df3-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="b5df3-135">Lai noņemtu saiti videi, atveriet **Datu integrācijas** darbvietu Finance and Operations vidē un pēc tam atlasiet **Noņemt saiti**.</span><span class="sxs-lookup"><span data-stu-id="b5df3-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
