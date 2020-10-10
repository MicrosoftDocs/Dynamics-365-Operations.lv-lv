---
title: Darba sākšana ar plānošanas optimizāciju
description: Šajā tēmā ir paskaidrots, kā sākt izmantot plānošanas optimizācijas funkcionalitāti.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
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
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887268"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="965cb-103">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="965cb-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="965cb-104">Plānošanas optimizēšanas funkcionalitāte pašlaik neatbalsta visus līdzekļus, kas ir pieejami Microsoft iebūvētajā plānošanas programmā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="965cb-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="965cb-105">Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama plānošanas optimizācijā, atbilst jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="965cb-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="965cb-106">Pēc noklusējuma plānošanas optimizācijas funkcionalitāte nav ieslēgta Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="965cb-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="965cb-107">Tāpēc jums ir iespēja veikt savu novērtējumu, pirms tas ir ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="965cb-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="965cb-108">Laika gaitā plānošanas optimizācija aizstās esošo iebūvēto Supply Chain Management plānošanas programmu</span><span class="sxs-lookup"><span data-stu-id="965cb-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="965cb-109">Pirms plānošanas optimizācijas ieslēgšanas iesakām novērtēt plānošanas optimizācijas ietilpināšanas analīzes rezultātus.</span><span class="sxs-lookup"><span data-stu-id="965cb-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="965cb-110">Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="965cb-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="965cb-111">Pieejamība</span><span class="sxs-lookup"><span data-stu-id="965cb-111">Availability</span></span>
<span data-ttu-id="965cb-112">Plānošanas optimizācija pašlaik ir pieejama šādās Azure ģeogrāfiskās vietās: Amerikas Savienotās Valstis, Kanāda, Eiropa, Apvienotā Karaliste un Austrālija.</span><span class="sxs-lookup"><span data-stu-id="965cb-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="965cb-113">Ja mēģināsit instalēt pievienojumprogrammu no cita ģeogrāfiskā reģiona, tad LCS rādīs ziņojumu, ka šī ģeogrāfiskā vērtība netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="965cb-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="965cb-114">Ņemiet vērā, ka plānošanas optimizācija neatbalsta Dynamics 365 Supply Chain Management lokālās izvietošanas.</span><span class="sxs-lookup"><span data-stu-id="965cb-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="965cb-115">Licencēšana</span><span class="sxs-lookup"><span data-stu-id="965cb-115">Licensing</span></span>

<span data-ttu-id="965cb-116">Ja vispārējo plānošanu varat veikt, izmantojot pašreizējo licenci, jums nav jāiegādājas papildu licence, lai sāktu izmantot plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="965cb-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="965cb-117">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="965cb-117">Install the add-in</span></span>

<span data-ttu-id="965cb-118">Lai izmantotu plānošanas optimizāciju, instalējiet plānošanas optimizācijas pievienojumprogrammu sistēmai Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="965cb-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="965cb-119">Varat piekļūt pievienojumprogrammai no sava LCS projekta un ieslēgt plānošanas optimizācijas funkcionalitāti no Supply Chain Management lietotāja interfeisa (UI).</span><span class="sxs-lookup"><span data-stu-id="965cb-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="965cb-120">Plānošanas optimizācijas prasība ir ar LCS iespējota augstas pieejamības vide, 2. līmeņa vai augstāka, (ne OneBox vide) ar Dynamics 365 Supply Chain Management versiju 10.0.7 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="965cb-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="965cb-121">Ja mēģināsit instalēt pievienojumprogrammu OneBox vidē, instalēšana netiks pabeigta, un tā būs jāatceļ.</span><span class="sxs-lookup"><span data-stu-id="965cb-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="965cb-122">Piesakieties LCS un atveriet vēlamo vidi.</span><span class="sxs-lookup"><span data-stu-id="965cb-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="965cb-123">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="965cb-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="965cb-124">Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="965cb-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="965cb-125">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="965cb-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="965cb-126">Atlasiet **Plānošanas optimizācija**.</span><span class="sxs-lookup"><span data-stu-id="965cb-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="965cb-127">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="965cb-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="965cb-128">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="965cb-128">Select **Install**.</span></span>
1. <span data-ttu-id="965cb-129">Kopsavilkuma cilnē **Vides pievienojumprogramma** jāredz, ka tiek instalēta plānošanas optimizācija.</span><span class="sxs-lookup"><span data-stu-id="965cb-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="965cb-130">Pēc dažām minūtēm **Instalē** jāmainās uz **Instalēts** (iespējams, lapa jāatsvaidzina).</span><span class="sxs-lookup"><span data-stu-id="965cb-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="965cb-131">Kad instalēšana ir pabeigta, varat aktivizēt plānošanas optimizāciju Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="965cb-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="965cb-132">Plānošanas optimizācijas integrēšana</span><span class="sxs-lookup"><span data-stu-id="965cb-132">Planning Optimization integration</span></span>

<span data-ttu-id="965cb-133">Lai konfigurētu, vai plānošanas optimizācijas pievienojumprogramma ir jāizmanto vispārējai plānošanai, dodieties uz **Vispārējā plānošana** \> **Iestatīšana** \> **Plānošanas optimizācijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="965cb-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="965cb-134">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="965cb-134">Connection status</span></span>

<span data-ttu-id="965cb-135">Savienojuma statuss norāda pašreizējo savienojuma statusu starp Supply Chain Management un plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="965cb-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="965cb-136">Nākamajā tabulā ir parādītas iespējamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="965cb-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="965cb-137">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="965cb-137">Connection status</span></span> | <span data-ttu-id="965cb-138">Apraksts</span><span class="sxs-lookup"><span data-stu-id="965cb-138">Description</span></span> | <span data-ttu-id="965cb-139">Vai var izmantot plānošanas optimizāciju?</span><span class="sxs-lookup"><span data-stu-id="965cb-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="965cb-140">Savienojums izveidots</span><span class="sxs-lookup"><span data-stu-id="965cb-140">Connected</span></span> | <span data-ttu-id="965cb-141">Ir izveidots savienojums starp plānošanas optimizācijas pakalpojumu un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="965cb-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="965cb-142">Jā</span><span class="sxs-lookup"><span data-stu-id="965cb-142">Yes</span></span> |
| <span data-ttu-id="965cb-143">Savienojuma iespējošana</span><span class="sxs-lookup"><span data-stu-id="965cb-143">Enabling connection</span></span> | <span data-ttu-id="965cb-144">Pieprasījums ieslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="965cb-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="965cb-145">Nē</span><span class="sxs-lookup"><span data-stu-id="965cb-145">No</span></span> |
| <span data-ttu-id="965cb-146">Savienojums pārtraukts</span><span class="sxs-lookup"><span data-stu-id="965cb-146">Disconnected</span></span> | <span data-ttu-id="965cb-147">Nav savienojuma ar plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="965cb-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="965cb-148">Savienojumu var ieslēgt no LCS, kā aprakstīts iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="965cb-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="965cb-149">Nē</span><span class="sxs-lookup"><span data-stu-id="965cb-149">No</span></span> |
| <span data-ttu-id="965cb-150">Savienojuma atspējošana</span><span class="sxs-lookup"><span data-stu-id="965cb-150">Disabling connection</span></span> | <span data-ttu-id="965cb-151">Pieprasījums izslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="965cb-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="965cb-152">Nē</span><span class="sxs-lookup"><span data-stu-id="965cb-152">No</span></span> |
| <span data-ttu-id="965cb-153">Statusa iegūšana</span><span class="sxs-lookup"><span data-stu-id="965cb-153">Getting status</span></span> | <span data-ttu-id="965cb-154">Sistēma gaida statusa informāciju no plānošanas optimizācijas pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="965cb-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="965cb-155">Nē</span><span class="sxs-lookup"><span data-stu-id="965cb-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="965cb-156">Iespēja Plānošanas optimizācijas izmantošana</span><span class="sxs-lookup"><span data-stu-id="965cb-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="965cb-157">Opcijas **Izmantot plānošanas optimizāciju** iestatījums nosaka, kuru plānošanas programmu izmanto vispārējai plānošanai:</span><span class="sxs-lookup"><span data-stu-id="965cb-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="965cb-158">**Jā** – plānošanas optimizācija tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="965cb-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="965cb-159">**Nē** - Iebūvētā Supply Chain Management plānošanas programma tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="965cb-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="965cb-160">Ja esošie plānošanas pakešuzdevumi, kas tika izveidoti iebūvētās Supply Chain Management programmai, ir aktivizēti, kamēr opcija **Izmantot plānošanas optimizāciju** ir iestatīta uz **Jā**, šie darbi neizdosies.</span><span class="sxs-lookup"><span data-stu-id="965cb-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="965cb-161">Integrēšana ar iestatījumu</span><span class="sxs-lookup"><span data-stu-id="965cb-161">Integration with the setup</span></span>

<span data-ttu-id="965cb-162">Ja plānošanas optimizācijas priekšskatījums ir ieslēgts, vispārējā plānošana tiek veikta, izmantojot plānošanas optimizācijas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="965cb-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="965cb-163">Šādā gadījumā tiek ietekmēti vispārējās plānošanas rezultāti un līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="965cb-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="965cb-164">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="965cb-164">Additional resources</span></span>

[<span data-ttu-id="965cb-165">Priekšskatījuma noteikumi un nosacījumi</span><span class="sxs-lookup"><span data-stu-id="965cb-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="965cb-166">Plānošanas optimizācijas apskats</span><span class="sxs-lookup"><span data-stu-id="965cb-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="965cb-167">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="965cb-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="965cb-168">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="965cb-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="965cb-169">Filtru lietošana plānam</span><span class="sxs-lookup"><span data-stu-id="965cb-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="965cb-170">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="965cb-170">Cancel a planning job</span></span>](cancel-planning-job.md)
