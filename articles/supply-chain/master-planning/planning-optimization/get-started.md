---
title: Darba sākšana ar plānošanas optimizāciju
description: Šajā tēmā ir paskaidrots, kā sākt izmantot plānošanas optimizācijas funkcionalitāti.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774003"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="27d42-103">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="27d42-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="27d42-104">Plānošanas optimizēšanas funkcionalitāte pašlaik neatbalsta visus līdzekļus, kas ir pieejami Microsoft iebūvētajā plānošanas programmā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="27d42-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="27d42-105">Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama plānošanas optimizācijā, atbilst jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="27d42-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="27d42-106">Pēc noklusējuma plānošanas optimizācijas funkcionalitāte nav ieslēgta Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="27d42-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="27d42-107">Tāpēc jums ir iespēja veikt savu novērtējumu, pirms tas ir ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="27d42-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="27d42-108">Laika gaitā plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management plānošanas programmu</span><span class="sxs-lookup"><span data-stu-id="27d42-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="27d42-109">Pirms plānošanas optimizācijas ieslēgšanas iesakām novērtēt plānošanas optimizācijas ietilpināšanas analīzes rezultātus.</span><span class="sxs-lookup"><span data-stu-id="27d42-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="27d42-110">Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="27d42-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="27d42-111">Licencēšana</span><span class="sxs-lookup"><span data-stu-id="27d42-111">Licensing</span></span>

<span data-ttu-id="27d42-112">Ja vispārējo plānošanu varat veikt, izmantojot pašreizējo licenci, jums nav jāiegādājas papildu licence, lai sāktu izmantot plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="27d42-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="27d42-113">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="27d42-113">Install the add-in</span></span>

<span data-ttu-id="27d42-114">Lai izmantotu plānošanas optimizāciju, instalējiet plānošanas optimizācijas pievienojumprogrammu sistēmai Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="27d42-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="27d42-115">Varat piekļūt pievienojumprogrammai no sava LCS projekta un ieslēgt plānošanas optimizācijas funkcionalitāti no Supply Chain Management lietotāja interfeisa (UI).</span><span class="sxs-lookup"><span data-stu-id="27d42-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="27d42-116">Piesakieties LCS un atveriet vēlamo vidi.</span><span class="sxs-lookup"><span data-stu-id="27d42-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="27d42-117">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="27d42-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="27d42-118">Atlasiet **Uzturēt**vai ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="27d42-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="27d42-119">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="27d42-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="27d42-120">Atlasiet **Plānošanas optimizācija**.</span><span class="sxs-lookup"><span data-stu-id="27d42-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="27d42-121">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="27d42-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="27d42-122">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="27d42-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="27d42-123">Plānošanas optimizācijas integrēšana</span><span class="sxs-lookup"><span data-stu-id="27d42-123">Planning Optimization integration</span></span>

<span data-ttu-id="27d42-124">Lai konfigurētu, vai plānošanas optimizācijas pievienojumprogramma ir jāizmanto vispārējai plānošanai, dodieties uz **Vispārējā plānošana**\>**Iestatīšana**\>**Plānošanas optimizācija**\> **Integrēšanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="27d42-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="27d42-125">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="27d42-125">Connection status</span></span>

<span data-ttu-id="27d42-126">Savienojuma statuss norāda pašreizējo savienojuma statusu starp Supply Chain Management un plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="27d42-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="27d42-127">Nākamajā tabulā ir parādītas iespējamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="27d42-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="27d42-128">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="27d42-128">Connection status</span></span> | <span data-ttu-id="27d42-129">Apraksts</span><span class="sxs-lookup"><span data-stu-id="27d42-129">Description</span></span> | <span data-ttu-id="27d42-130">Vai var izmantot plānošanas optimizāciju?</span><span class="sxs-lookup"><span data-stu-id="27d42-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="27d42-131">Savienojums izveidots</span><span class="sxs-lookup"><span data-stu-id="27d42-131">Connected</span></span> | <span data-ttu-id="27d42-132">Ir izveidots savienojums starp plānošanas optimizācijas pakalpojumu un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="27d42-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="27d42-133">Jā</span><span class="sxs-lookup"><span data-stu-id="27d42-133">Yes</span></span> |
| <span data-ttu-id="27d42-134">Savienojuma iespējošana</span><span class="sxs-lookup"><span data-stu-id="27d42-134">Enabling connection</span></span> | <span data-ttu-id="27d42-135">Pieprasījums ieslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="27d42-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="27d42-136">Nē</span><span class="sxs-lookup"><span data-stu-id="27d42-136">No</span></span> |
| <span data-ttu-id="27d42-137">Savienojums pārtraukts</span><span class="sxs-lookup"><span data-stu-id="27d42-137">Disconnected</span></span> | <span data-ttu-id="27d42-138">Nav savienojuma ar plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="27d42-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="27d42-139">Savienojumu var ieslēgt no LCS, kā aprakstīts iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="27d42-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="27d42-140">Nē</span><span class="sxs-lookup"><span data-stu-id="27d42-140">No</span></span> |
| <span data-ttu-id="27d42-141">Savienojuma atspējošana</span><span class="sxs-lookup"><span data-stu-id="27d42-141">Disabling connection</span></span> | <span data-ttu-id="27d42-142">Pieprasījums izslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="27d42-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="27d42-143">Nē</span><span class="sxs-lookup"><span data-stu-id="27d42-143">No</span></span> |
| <span data-ttu-id="27d42-144">Statusa iegūšana</span><span class="sxs-lookup"><span data-stu-id="27d42-144">Getting status</span></span> | <span data-ttu-id="27d42-145">Sistēma gaida statusa informāciju no plānošanas optimizācijas pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="27d42-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="27d42-146">Nē</span><span class="sxs-lookup"><span data-stu-id="27d42-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="27d42-147">Iespēja Plānošanas optimizācijas izmantošana</span><span class="sxs-lookup"><span data-stu-id="27d42-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="27d42-148">Opcijas **Izmantot plānošanas optimizāciju** iestatījums nosaka, kuru plānošanas programmu izmanto vispārējai plānošanai:</span><span class="sxs-lookup"><span data-stu-id="27d42-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="27d42-149">**Jā** – plānošanas optimizācija tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="27d42-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="27d42-150">**Nē** - Iebūvētā Supply Chain Management plānošanas programma tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="27d42-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="27d42-151">Ja esošie plānošanas pakešuzdevumi, kas tika izveidoti iebūvētās Supply Chain Management programmai, ir aktivizēti, kamēr opcija **Izmantot plānošanas optimizāciju** ir iestatīta uz **Jā**, šie darbi neizdosies.</span><span class="sxs-lookup"><span data-stu-id="27d42-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="27d42-152">Integrēšana ar iestatījumu</span><span class="sxs-lookup"><span data-stu-id="27d42-152">Integration with the setup</span></span>

<span data-ttu-id="27d42-153">Ja plānošanas optimizācijas priekšskatījums ir ieslēgts, vispārējā plānošana tiek veikta, izmantojot plānošanas optimizācijas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="27d42-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="27d42-154">Šādā gadījumā tiek ietekmēti vispārējās plānošanas rezultāti un līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="27d42-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="27d42-155">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="27d42-155">Related resources</span></span>

[<span data-ttu-id="27d42-156">Priekšskatījuma noteikumi un nosacījumi</span><span class="sxs-lookup"><span data-stu-id="27d42-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="27d42-157">Plānošanas optimizācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="27d42-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="27d42-158">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="27d42-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="27d42-159">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="27d42-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="27d42-160">Filtru lietošana plānam</span><span class="sxs-lookup"><span data-stu-id="27d42-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="27d42-161">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="27d42-161">Cancel a planning job</span></span>](cancel-planning-job.md)
