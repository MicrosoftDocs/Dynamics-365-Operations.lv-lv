---
title: Starpuzņēmumu plānošana
description: Šī tēma apraksta starpuzņēmumu plānošanu un izskaidro, kā to konfigurēt ar Plānošanas optimizāciju programmā Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25c80ce27498131c6eb92174ab14a592bfa9915a
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672196"
---
# <a name="intercompany-planning"></a><span data-ttu-id="a5a98-103">Starpuzņēmumu plānošana</span><span class="sxs-lookup"><span data-stu-id="a5a98-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5a98-104">Dažām organizācijām loģistikas darbības ir atkarīgas no citām juridiskām personām (uzņēmumiem) organizācijā.</span><span class="sxs-lookup"><span data-stu-id="a5a98-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="a5a98-105">Šīs operācijas tiek apstrādātas, izmantojot starpuzņēmumu pārdošanu un pirkšanu, jo katrai juridiskajai personai ir atsevišķs kontu plāns.</span><span class="sxs-lookup"><span data-stu-id="a5a98-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="a5a98-106">Šī tēma apraksta starpuzņēmumu plānošanu un izskaidro, kā to konfigurēt ar Plānošanas optimizāciju programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a5a98-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="a5a98-107">Šī tēma izmanto šādus svarīgus starpuzņēmumu nosacījumus:</span><span class="sxs-lookup"><span data-stu-id="a5a98-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="a5a98-108">**Iepriekšējā plūsma** – relatīvā atsauce uzņēmumā vai piegādes ķēdē.</span><span class="sxs-lookup"><span data-stu-id="a5a98-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="a5a98-109">Tā norāda kustību izejmateriālu piegādātāja virzienā.</span><span class="sxs-lookup"><span data-stu-id="a5a98-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="a5a98-110">**Pakārtotā plūsma** – relatīvā atsauce uzņēmumā vai piegādes ķēdē.</span><span class="sxs-lookup"><span data-stu-id="a5a98-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="a5a98-111">Tā norāda kustību klienta virzienā.</span><span class="sxs-lookup"><span data-stu-id="a5a98-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="a5a98-112">**Plānotais starpuzņēmumu pieprasījums** - plānotais preces pieprasījums uzņēmumā, pamatojoties uz plānoto pieprasījumu pēc preces no pakārtotā uzņēmuma.</span><span class="sxs-lookup"><span data-stu-id="a5a98-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="a5a98-113">Vispārējā plānošanā plāns vienā uzņēmumā var ietvert plānoto starpuzņēmumu pieprasījumu, kas ir saistīts ar plānotajiem pasūtījumiem no plāna citā uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="a5a98-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="a5a98-114">Šī iespēja ir noderīga, jo tā nodrošina pilnīgu redzamību paredzētajos pasūtījumos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="a5a98-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="a5a98-115">Tā arī nodrošina, ka visi nepieciešamie plānotie piegādes pasūtījumi tiek izveidoti, bet bez nepieciešamības apstiprināt plānotos pasūtījumus starpuzņēmumu pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="a5a98-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="a5a98-116">Ja vispārējā plānošana tiek palaista no vispārējā plāna, kas ietver plānoto pakārtoto pieprasījumu, plānotie pirkšanas pasūtījumi no saistītiem starpuzņēmumu kreditoriem tiks iekļauti plānā kā pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="a5a98-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="a5a98-117">Nepieciešamie iestatījumi</span><span class="sxs-lookup"><span data-stu-id="a5a98-117">Required setup</span></span>

<span data-ttu-id="a5a98-118">Lai izmantotu starpuzņēmumu plānošanu, jūsu sistēma ir jāsagatavo šādi:</span><span class="sxs-lookup"><span data-stu-id="a5a98-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="a5a98-119">Atbilstošās preces ir jānodod visiem saistītajiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="a5a98-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="a5a98-120">Plašāku informāciju skatiet šeit: [Konfigurēt un izmantot starpuzņēmumu tirdzniecību risinājumā Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="a5a98-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="a5a98-121">Pakārtotais pieprasījums ir jāsedz ar pirkšanu no kreditora, kam ir starpuzņēmumu saistība ar iepriekšējo uzņēmumu un saistītajām noklusējuma krājumu dimensijām (vieta un noliktava) debitoram.</span><span class="sxs-lookup"><span data-stu-id="a5a98-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="a5a98-122">Plašāku informāciju skatiet šeit: [Konfigurēt un izmantot starpuzņēmumu tirdzniecību risinājumā Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="a5a98-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="a5a98-123">Vispārējam plānam iepriekšējā posma uzņēmumā ir jāiekļauj plānotais pakārtotais pieprasījums, un pakārtotajos plānos ir jānorāda attiecīgais uzņēmums un vispārējais plāns.</span><span class="sxs-lookup"><span data-stu-id="a5a98-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="a5a98-124">Ietvert lejupstraumes plānoto pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="a5a98-124">Include planned downstream demand</span></span>

<span data-ttu-id="a5a98-125">Sekojiet šiem soļiem, lai konfigurētu vispārējo plānu, lai tas ietvertu plānoto pakārtoto pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="a5a98-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="a5a98-126">Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.</span><span class="sxs-lookup"><span data-stu-id="a5a98-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="a5a98-127">Atlasiet vai izveidojiet vispārējo plānu.</span><span class="sxs-lookup"><span data-stu-id="a5a98-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="a5a98-128">Kopsavilkuma cilnē **Starpuzņēmumu plānošana**, iestatiet tālāk minētos laukus:</span><span class="sxs-lookup"><span data-stu-id="a5a98-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="a5a98-129">**Iekļaut plānoto pakārtoto pieprasījumu** – iestatiet šo opciju uz *Jā*, lai varētu aktivizēt starpuzņēmumu plānošanu vispārējam plānam.</span><span class="sxs-lookup"><span data-stu-id="a5a98-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="a5a98-130">**Pakārtotie plāni** – ja iestatāt opciju **Iekļaut plānoto pakārtoto pieprasījumu** uz *Jā*, izmantojiet rīkjoslu un režģi, lai pievienotu vēlamos vispārējos plānus no citiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="a5a98-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="a5a98-131">Saistīt starp uzņēmumiem, izmantojot vairāklīmeņu piesaistes</span><span class="sxs-lookup"><span data-stu-id="a5a98-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="a5a98-132">Daudzlīmeņu piesaistei varat skatīt piesaistes starp uzņēmumiem, lai redzētu sākotnējo pieprasījuma avotu, ko sedz piegāde.</span><span class="sxs-lookup"><span data-stu-id="a5a98-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="a5a98-133">Lai apskatītu vairāklīmeņu piesaistes informāciju, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="a5a98-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="a5a98-134">Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Plānotie pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a5a98-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="a5a98-135">Atlasiet vai atveriet plānoto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a5a98-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="a5a98-136">Darbību rūtī cilnē **Skatīt** grupā **Prasības** atlasiet **Vairāklīmeņu piesaiste**.</span><span class="sxs-lookup"><span data-stu-id="a5a98-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="a5a98-137">Starpuzņēmumu piemērs, kas ietver divus uzņēmumus</span><span class="sxs-lookup"><span data-stu-id="a5a98-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="a5a98-138">Šim piemēram plānotais ražošanas pasūtījums tiek izveidots USMF uzņēmumā, lai nosegtu pārdošanas pasūtījumu DEMF uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="a5a98-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="a5a98-139">USMF tiešais pieprasījums ir plānotais starpuzņēmumu pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="a5a98-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="a5a98-140">Lai šis pieprasījums tiktu parādīts USMF, vispārējā plānošana tiek palaista vispirms DEMF un pēc tam USMF.</span><span class="sxs-lookup"><span data-stu-id="a5a98-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="a5a98-141">Sekojošajā attēlā parādīts, kā šis piemērs var parādīties lapā **Vairāklīmeņu piesaiste** plānotās ražošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="a5a98-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Starpuzņēmumu piemērs, kas ietver divus uzņēmumus](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="a5a98-143">Starpuzņēmumu piemērs, kas ietver trīs uzņēmumus</span><span class="sxs-lookup"><span data-stu-id="a5a98-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="a5a98-144">Šim piemēram plānotais pirkšanas pasūtījums tiek izveidots USMF uzņēmumā, lai nosegtu pārdošanas pasūtījumu FRRT uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="a5a98-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="a5a98-145">DEMF un USMF uzņēmumos tiešais pieprasījums ir plānotais starpuzņēmumu pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="a5a98-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="a5a98-146">Lai šis pieprasījums tiktu parādīts USMF, vispārējā plānošana tiek palaista vispirms FRRT un pēc tam DEMF, un visbeidzot USMF.</span><span class="sxs-lookup"><span data-stu-id="a5a98-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="a5a98-147">Sekojošajā attēlā parādīts, kā šis piemērs var parādīties lapā **Vairāklīmeņu piesaiste** plānotās ražošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="a5a98-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Starpuzņēmumu piemērs, kas ietver trīs uzņēmumus](media/IntercompanyPlanning2.png)
