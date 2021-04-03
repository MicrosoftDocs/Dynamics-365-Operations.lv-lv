---
title: Ražošanas izpildes interfeisa izstrādāšana
description: Šajā tēmā ir aprakstīts, kā izstrādāt lietotāja interfeisa saturu katrai konfigurācijai.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 282785799b6d61a00a356fcc2ae86ff0e3b7b39f
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501034"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="8fd8c-103">Ražošanas izpildes interfeisa izstrādāšana</span><span class="sxs-lookup"><span data-stu-id="8fd8c-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8fd8c-104">Jūs varat izstrādāt lietotāja interfeisa saturu katrai konfigurācijai, ko izmanto ražošanas līmeņa izpildes interfeiss.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="8fd8c-105">Piemēram, darbiniekiem vienā darba šūnā, iespējams, ir jāspēj atvērt darba instrukcijas ražošanas līmenī, bet citā darba šūnā instrukcijas nav nepieciešamas.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="8fd8c-106">Šādā gadījumā ir jāizveido divas konfigurācijas, viena ar pogu dokumenta pielikumu atvēršanai un viena bez šīs pogas.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="8fd8c-107">Izveidot cilni</span><span class="sxs-lookup"><span data-stu-id="8fd8c-107">Design a tab</span></span>

<span data-ttu-id="8fd8c-108">Lapā **Ražošanas līmeņa izpildes konfigurēšana** varat izveidot un konfigurēt cilnes, darbību rūtī atlasot **Izveidot cilnes**.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="8fd8c-109">Katra cilne ir sadalīta četrās sadaļās, kā parādīts sekojošajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="8fd8c-110">![Cilnes izkārtojums](media/pfe-tab-layout.png "Cilnes izkārtojums")</span><span class="sxs-lookup"><span data-stu-id="8fd8c-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="8fd8c-111">Attēlā redzami šādi elementi:</span><span class="sxs-lookup"><span data-stu-id="8fd8c-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="8fd8c-112">Primārā rīkjosla</span><span class="sxs-lookup"><span data-stu-id="8fd8c-112">Primary toolbar</span></span>
1. <span data-ttu-id="8fd8c-113">Sekundārā rīkjosla</span><span class="sxs-lookup"><span data-stu-id="8fd8c-113">Secondary toolbar</span></span>
1. <span data-ttu-id="8fd8c-114">Galvenais skats</span><span class="sxs-lookup"><span data-stu-id="8fd8c-114">Main view</span></span>
1. <span data-ttu-id="8fd8c-115">Detalizēts skats</span><span class="sxs-lookup"><span data-stu-id="8fd8c-115">Detailed view</span></span>

<span data-ttu-id="8fd8c-116">Lai izveidotu un konfigurētu jaunu cilni, veiciet tālāk norādītās darbības:</span><span class="sxs-lookup"><span data-stu-id="8fd8c-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="8fd8c-117">Dodieties uz **Ražošanas kontrole \> Iestatījumi \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-117">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

1. <span data-ttu-id="8fd8c-118">Darbību rūtī atlasiet **Izveidot cilnes**, lai atvērtu lapu **Izveidot cilnes**.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="8fd8c-119">![Izveidot cilnes lapa](media/pfe-design-tabs.png "Izveidot cilnes lapa")</span><span class="sxs-lookup"><span data-stu-id="8fd8c-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="8fd8c-120">Atlasiet **Jauns** darbību rūtī.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="8fd8c-121">Lapas virsrakstā veiciet tālāk norādītos iestatījumus:</span><span class="sxs-lookup"><span data-stu-id="8fd8c-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="8fd8c-122">**Cilnes nosaukums** - norādiet cilnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="8fd8c-123">**Galvenais skats** – atlasiet starp diviem iepriekš definētiem darbu sarakstiem (*Aktīvie darbi*, *Visi darbi* vai *Mana iekāŗta*).</span><span class="sxs-lookup"><span data-stu-id="8fd8c-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="8fd8c-124">**Detalizētas informācijas skats** - izvēlieties starp tukšu vērtību vai **Darba detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="8fd8c-125">Ja atlasīsit tukšu vērtību, nebūs detalizēta skatījuma cilnē. Ja izvēlaties **Darba detalizētu informāciju**, detalizētajā skatījumā būs detalizēts darba apraksts, kas atlasīts darbu sarakstā galvenajā skatā.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="8fd8c-126">**Primārās rīkjoslas** sadaļā Izvēlieties, kurām pogām jābūt pieejamām primārajā rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="8fd8c-127">Kolonnā **Pieejamās darbības** redzams saraksts ar visām pogām, kuras var pievienot.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="8fd8c-128">Kolonnas **Atlasītās darbības** rāda visu to pogu saraksts, kas iekļautas pašreizējā konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="8fd8c-129">Izmantojiet pogas starp kolonnām, lai atlasītos vienumus pārvietotu starp kolonnām pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="8fd8c-130">Izmantojiet pogas augšup un lejup blakus kolonnai **Atlasītās darbībās**, lai kontrolētu secību, kādā pogas tiek rādītas lietotāja interfeisā.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="8fd8c-131">**Sekundārās** **rīkjoslas** sadaļā izvēlieties, kurām pogām jābūt pieejamām sekundārajā rīkjoslā.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="8fd8c-132">Kolonnā **Pieejamās darbības** redzams saraksts ar visām pogām, kuras var pievienot.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="8fd8c-133">Kolonnas **Atlasītās darbības** rāda visu to pogu saraksts, kas iekļautas pašreizējā konfigurācijā.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="8fd8c-134">Izmantojiet pogas starp kolonnām, lai atlasītos vienumus pārvietotu starp kolonnām pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="8fd8c-135">Izmantojiet pogas augšup un lejup blakus kolonnai **Atlasītās darbībās**, lai kontrolētu secību, kādā pogas tiek rādītas lietotāja interfeisā.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="8fd8c-136">Cilnes saistīšana ar konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="8fd8c-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="8fd8c-137">Pēc tam, kad visas cilnes ir izveidotas, tās var saistīt ar konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="8fd8c-138">Dodieties uz **Ražošanas kontrole \> Iestatījumi \> Ražošanas izpilde \> Konfigurēt ražotnes izpildi**.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-138">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

    <span data-ttu-id="8fd8c-139">![Konfigurēt ražošanas līmeņa izpildi](media/pfe-config-prod-floor-execution.png "Konfigurēt ražošanas līmeņa izpildi")</span><span class="sxs-lookup"><span data-stu-id="8fd8c-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="8fd8c-140">Kopsavilkuma cilnē **Cilnes atlase** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="8fd8c-141">Režģim tiek pievienota jauna rinda.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-141">A new row is added to the grid.</span></span> <span data-ttu-id="8fd8c-142">Šai jaunajai rindai atlasiet cilnes nosaukumu, kuru vēlaties pievienot konfigurācijai.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="8fd8c-143">Turpiniet pievienot papildu cilnes pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="8fd8c-144">Izmantojiet rīkjoslas pogu **Pārvietot uz augšu** un **Pārvietot uz leju**, lai pēc nepieciešamības kārtotu cilnes.</span><span class="sxs-lookup"><span data-stu-id="8fd8c-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="8fd8c-145">Cilnes tiks rādītas no kreisās uz labo tādā secībā, kā norādīts iepriekš attēlā (cilne virspusē tiek rādīta kreisajā pusē).</span><span class="sxs-lookup"><span data-stu-id="8fd8c-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]