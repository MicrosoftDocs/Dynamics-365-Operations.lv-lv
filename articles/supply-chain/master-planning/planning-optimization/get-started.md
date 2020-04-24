---
title: Darba sākšana ar plānošanas optimizāciju
description: Šajā tēmā ir paskaidrots, kā sākt izmantot plānošanas optimizācijas funkcionalitāti.
author: ChristianRytt
manager: tfehr
ms.date: 02/10/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4f9124e824a0b6d5035b2567cb19c2c494390d55
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213519"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="fcbaa-103">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="fcbaa-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcbaa-104">Plānošanas optimizēšanas funkcionalitāte pašlaik neatbalsta visus līdzekļus, kas ir pieejami Microsoft iebūvētajā plānošanas programmā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fcbaa-105">Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama plānošanas optimizācijā, atbilst jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="fcbaa-106">Pēc noklusējuma plānošanas optimizācijas funkcionalitāte nav ieslēgta Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fcbaa-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="fcbaa-107">Tāpēc jums ir iespēja veikt savu novērtējumu, pirms tas ir ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="fcbaa-108">Laika gaitā plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management plānošanas programmu</span><span class="sxs-lookup"><span data-stu-id="fcbaa-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="fcbaa-109">Pirms plānošanas optimizācijas ieslēgšanas iesakām novērtēt plānošanas optimizācijas ietilpināšanas analīzes rezultātus.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="fcbaa-110">Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fcbaa-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="fcbaa-111">Licencēšana</span><span class="sxs-lookup"><span data-stu-id="fcbaa-111">Licensing</span></span>

<span data-ttu-id="fcbaa-112">Ja vispārējo plānošanu varat veikt, izmantojot pašreizējo licenci, jums nav jāiegādājas papildu licence, lai sāktu izmantot plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="fcbaa-113">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="fcbaa-113">Install the add-in</span></span>

<span data-ttu-id="fcbaa-114">Lai izmantotu plānošanas optimizāciju, instalējiet plānošanas optimizācijas pievienojumprogrammu sistēmai Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fcbaa-115">Varat piekļūt pievienojumprogrammai no sava LCS projekta un ieslēgt plānošanas optimizācijas funkcionalitāti no Supply Chain Management lietotāja interfeisa (UI).</span><span class="sxs-lookup"><span data-stu-id="fcbaa-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="fcbaa-116">Plānošanas optimizācijas prasība ir ar LCS iespējota augstas pieejamības vide (ne OneBox vide) ar Dynamics 365 Supply Chain Management versiju 10.0.7 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="fcbaa-117">Piesakieties LCS un atveriet vēlamo vidi.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="fcbaa-118">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="fcbaa-119">Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="fcbaa-120">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="fcbaa-121">Atlasiet **Plānošanas optimizācija**.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="fcbaa-122">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="fcbaa-123">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-123">Select **Install**.</span></span>
1. <span data-ttu-id="fcbaa-124">Kopsavilkuma cilnē **Vides pievienojumprogramma** jāredz, ka tiek instalēta plānošanas optimizācija.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="fcbaa-125">Pēc dažām minūtēm **Instalē** jāmainās uz **Instalēts** (iespējams, lapa jāatsvaidzina).</span><span class="sxs-lookup"><span data-stu-id="fcbaa-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="fcbaa-126">Kad instalēšana ir pabeigta, varat aktivizēt plānošanas optimizāciju Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="fcbaa-127">Plānošanas optimizācijas integrēšana</span><span class="sxs-lookup"><span data-stu-id="fcbaa-127">Planning Optimization integration</span></span>

<span data-ttu-id="fcbaa-128">Lai konfigurētu, vai plānošanas optimizācijas pievienojumprogramma ir jāizmanto vispārējai plānošanai, dodieties uz **Vispārējā plānošana** \> **Iestatīšana** \> **Plānošanas optimizācijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="fcbaa-129">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="fcbaa-129">Connection status</span></span>

<span data-ttu-id="fcbaa-130">Savienojuma statuss norāda pašreizējo savienojuma statusu starp Supply Chain Management un plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="fcbaa-131">Nākamajā tabulā ir parādītas iespējamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="fcbaa-132">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="fcbaa-132">Connection status</span></span> | <span data-ttu-id="fcbaa-133">Apraksts</span><span class="sxs-lookup"><span data-stu-id="fcbaa-133">Description</span></span> | <span data-ttu-id="fcbaa-134">Vai var izmantot plānošanas optimizāciju?</span><span class="sxs-lookup"><span data-stu-id="fcbaa-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="fcbaa-135">Savienojums izveidots</span><span class="sxs-lookup"><span data-stu-id="fcbaa-135">Connected</span></span> | <span data-ttu-id="fcbaa-136">Ir izveidots savienojums starp plānošanas optimizācijas pakalpojumu un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="fcbaa-137">Jā</span><span class="sxs-lookup"><span data-stu-id="fcbaa-137">Yes</span></span> |
| <span data-ttu-id="fcbaa-138">Savienojuma iespējošana</span><span class="sxs-lookup"><span data-stu-id="fcbaa-138">Enabling connection</span></span> | <span data-ttu-id="fcbaa-139">Pieprasījums ieslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="fcbaa-140">Nē</span><span class="sxs-lookup"><span data-stu-id="fcbaa-140">No</span></span> |
| <span data-ttu-id="fcbaa-141">Savienojums pārtraukts</span><span class="sxs-lookup"><span data-stu-id="fcbaa-141">Disconnected</span></span> | <span data-ttu-id="fcbaa-142">Nav savienojuma ar plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="fcbaa-143">Savienojumu var ieslēgt no LCS, kā aprakstīts iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="fcbaa-144">Nē</span><span class="sxs-lookup"><span data-stu-id="fcbaa-144">No</span></span> |
| <span data-ttu-id="fcbaa-145">Savienojuma atspējošana</span><span class="sxs-lookup"><span data-stu-id="fcbaa-145">Disabling connection</span></span> | <span data-ttu-id="fcbaa-146">Pieprasījums izslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="fcbaa-147">Nē</span><span class="sxs-lookup"><span data-stu-id="fcbaa-147">No</span></span> |
| <span data-ttu-id="fcbaa-148">Statusa iegūšana</span><span class="sxs-lookup"><span data-stu-id="fcbaa-148">Getting status</span></span> | <span data-ttu-id="fcbaa-149">Sistēma gaida statusa informāciju no plānošanas optimizācijas pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="fcbaa-150">Nē</span><span class="sxs-lookup"><span data-stu-id="fcbaa-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="fcbaa-151">Iespēja Plānošanas optimizācijas izmantošana</span><span class="sxs-lookup"><span data-stu-id="fcbaa-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="fcbaa-152">Opcijas **Izmantot plānošanas optimizāciju** iestatījums nosaka, kuru plānošanas programmu izmanto vispārējai plānošanai:</span><span class="sxs-lookup"><span data-stu-id="fcbaa-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="fcbaa-153">**Jā** – plānošanas optimizācija tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="fcbaa-154">**Nē** - Iebūvētā Supply Chain Management plānošanas programma tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="fcbaa-155">Ja esošie plānošanas pakešuzdevumi, kas tika izveidoti iebūvētās Supply Chain Management programmai, ir aktivizēti, kamēr opcija **Izmantot plānošanas optimizāciju** ir iestatīta uz **Jā**, šie darbi neizdosies.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="fcbaa-156">Integrēšana ar iestatījumu</span><span class="sxs-lookup"><span data-stu-id="fcbaa-156">Integration with the setup</span></span>

<span data-ttu-id="fcbaa-157">Ja plānošanas optimizācijas priekšskatījums ir ieslēgts, vispārējā plānošana tiek veikta, izmantojot plānošanas optimizācijas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="fcbaa-158">Šādā gadījumā tiek ietekmēti vispārējās plānošanas rezultāti un līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="fcbaa-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="fcbaa-159">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="fcbaa-159">Related resources</span></span>

[<span data-ttu-id="fcbaa-160">Priekšskatījuma noteikumi un nosacījumi</span><span class="sxs-lookup"><span data-stu-id="fcbaa-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="fcbaa-161">Plānošanas optimizācijas pārskats</span><span class="sxs-lookup"><span data-stu-id="fcbaa-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="fcbaa-162">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="fcbaa-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="fcbaa-163">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="fcbaa-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="fcbaa-164">Filtru lietošana plānam</span><span class="sxs-lookup"><span data-stu-id="fcbaa-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="fcbaa-165">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="fcbaa-165">Cancel a planning job</span></span>](cancel-planning-job.md)
