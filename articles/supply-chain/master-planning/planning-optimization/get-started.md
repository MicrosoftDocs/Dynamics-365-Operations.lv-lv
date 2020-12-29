---
title: Darba sākšana ar plānošanas optimizāciju
description: Šajā tēmā ir paskaidrots, kā sākt izmantot plānošanas optimizācijas funkcionalitāti.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
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
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/29/2020
ms.locfileid: "4433224"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="40158-103">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="40158-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="40158-104">Kā [iepriekš paziņots](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), ir ieplānota plānošanas optimizācija, kas aizstātu esošo iebūvēto vispārējās plānošanas programmu.</span><span class="sxs-lookup"><span data-stu-id="40158-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="40158-105">Ja pašlaik izmantojat iebūvēto vispārējās plānošanas programmu, jums tūlīt jāsāk plānot migrāciju uz plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="40158-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="40158-106">Ir svarīgi nekavējoties sākt migrācijas procesu, jo, kad tiek ieviests nolietojums, jūsu darbības var tikt ietekmētas.</span><span class="sxs-lookup"><span data-stu-id="40158-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="40158-107">Lai izvairītos no problēmām pēdējā brīdī, kad tiek ieviests nolietojums, mēs iesakām pabeigt migrāciju pirms 2020. gada 1. decembra.</span><span class="sxs-lookup"><span data-stu-id="40158-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="40158-108">Plānošanas optimizācijas funkcionalitāte pašlaik neatbalsta visus līdzekļus, kas ir pieejami Supply Chain Management iebūvētajā plānošanas programmā.</span><span class="sxs-lookup"><span data-stu-id="40158-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="40158-109">Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama plānošanas optimizācijā, atbilst jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="40158-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="40158-110">Pašlaik plānošanas optimizācijas funkcionalitāte Dynamics Lifecycle Services (LCS) netiek ieslēgta pēc noklusējuma, tāpēc jums ir iespēja veikt novērtēšanu pirms šī līdzekļa ieslēgšanas.</span><span class="sxs-lookup"><span data-stu-id="40158-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="40158-111">Jums jāpieprasa migrācijas izņēmumu plānošanas optimizācijā, ja vispārējās plānošanas process neiekļauj ražošanu (vispārējās plānošanas ģenerētus plānotos ražošanas pasūtījumus), un jums nepieciešama iebūvētā vispārējās plānošanas programmas versija, kas jaunāka par versiju 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="40158-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="40158-112">Sākot ar versiju 10.0.16, kļūda vidēs tiks parādīta, kad tiek palaista iebūvētā vispārējā plānošana bez plānoto ražošanas pasūtījumu ģenerēšanas.</span><span class="sxs-lookup"><span data-stu-id="40158-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="40158-113">Plānošanas optimizācija ir jāizmanto visiem jaunajiem izvietojumiem, kas vispārējās plānošanas laikā neģenerē plānotos ražošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="40158-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="40158-114">Īpašnieki, kam pieder esošās vides, kurās darbojas iebūvētā vispārējās plānošanas programma bez plānoto ražošanas pasūtījumu ģenerēšanas, saņems e-pastu ar sīkāku informāciju par izņēmuma procesu.</span><span class="sxs-lookup"><span data-stu-id="40158-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="40158-115">Iesakām jums strādāt ar partneri, lai novērtētu un plānotu migrāciju uz plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="40158-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="40158-116">Pirms plānošanas optimizācijas ieslēgšanas iesakām novērtēt plānošanas optimizācijas ietilpināšanas analīzes rezultātus.</span><span class="sxs-lookup"><span data-stu-id="40158-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="40158-117">Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="40158-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="40158-118">Pieejamība</span><span class="sxs-lookup"><span data-stu-id="40158-118">Availability</span></span>
<span data-ttu-id="40158-119">Plānošanas optimizācija pašlaik ir pieejama šādās Azure ģeogrāfiskās vietās: Amerikas Savienotās Valstis, Kanāda, Eiropa, Apvienotā Karaliste un Austrālija.</span><span class="sxs-lookup"><span data-stu-id="40158-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="40158-120">Ja mēģināsit instalēt pievienojumprogrammu no cita ģeogrāfiskā reģiona, tad LCS rādīs ziņojumu, ka šī ģeogrāfiskā vērtība netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="40158-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="40158-121">Ņemiet vērā, ka plānošanas optimizācija neatbalsta Dynamics 365 Supply Chain Management lokālās izvietošanas.</span><span class="sxs-lookup"><span data-stu-id="40158-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="40158-122">Licencēšana</span><span class="sxs-lookup"><span data-stu-id="40158-122">Licensing</span></span>

<span data-ttu-id="40158-123">Ja vispārējo plānošanu varat veikt, izmantojot pašreizējo licenci, jums nav jāiegādājas papildu licence, lai sāktu izmantot plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="40158-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="40158-124">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="40158-124">Install the add-in</span></span>

<span data-ttu-id="40158-125">Lai izmantotu plānošanas optimizāciju, instalējiet plānošanas optimizācijas pievienojumprogrammu sistēmai Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="40158-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="40158-126">Varat piekļūt pievienojumprogrammai no sava LCS projekta un ieslēgt plānošanas optimizācijas funkcionalitāti no Supply Chain Management lietotāja interfeisa (UI).</span><span class="sxs-lookup"><span data-stu-id="40158-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="40158-127">Plānošanas optimizācijas prasība ir ar LCS iespējota augstas pieejamības vide, 2. līmeņa vai augstāka, (ne OneBox vide) ar Dynamics 365 Supply Chain Management versiju 10.0.7 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="40158-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="40158-128">Ja mēģināsit instalēt pievienojumprogrammu OneBox vidē, instalēšana netiks pabeigta, un tā būs jāatceļ.</span><span class="sxs-lookup"><span data-stu-id="40158-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="40158-129">Piesakieties LCS un atveriet vēlamo vidi.</span><span class="sxs-lookup"><span data-stu-id="40158-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="40158-130">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="40158-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="40158-131">Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="40158-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="40158-132">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="40158-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="40158-133">Atlasiet **Plānošanas optimizācija**.</span><span class="sxs-lookup"><span data-stu-id="40158-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="40158-134">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="40158-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="40158-135">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="40158-135">Select **Install**.</span></span>
1. <span data-ttu-id="40158-136">Kopsavilkuma cilnē **Vides pievienojumprogramma** jāredz, ka tiek instalēta plānošanas optimizācija.</span><span class="sxs-lookup"><span data-stu-id="40158-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="40158-137">Pēc dažām minūtēm **Instalē** jāmainās uz **Instalēts** (iespējams, lapa jāatsvaidzina).</span><span class="sxs-lookup"><span data-stu-id="40158-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="40158-138">Kad instalēšana ir pabeigta, varat aktivizēt plānošanas optimizāciju Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="40158-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="40158-139">Plānošanas optimizācijas papildinājuma instalēšanas galvenais nolūks ir savienot pakalpojumu un vidi.</span><span class="sxs-lookup"><span data-stu-id="40158-139">The main purpose of installing the Planning Optimization add-in is to connect the service and the environment.</span></span> <span data-ttu-id="40158-140">Tāpēc jums ir jāinstalē pievienojumprogramma atsevišķi katrai videi, kurā izmantosiet plānošanas optimizāciju neatkarīgi no tā, kāds kods tiek pārvietots starp vidēm.</span><span class="sxs-lookup"><span data-stu-id="40158-140">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="40158-141">Plānošanas optimizācijas integrēšana</span><span class="sxs-lookup"><span data-stu-id="40158-141">Planning Optimization integration</span></span>

<span data-ttu-id="40158-142">Lai konfigurētu, vai plānošanas optimizācijas pievienojumprogramma ir jāizmanto vispārējai plānošanai, dodieties uz **Vispārējā plānošana** \> **Iestatīšana** \> **Plānošanas optimizācijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="40158-142">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="40158-143">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="40158-143">Connection status</span></span>

<span data-ttu-id="40158-144">Savienojuma statuss norāda pašreizējo savienojuma statusu starp Supply Chain Management un plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="40158-144">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="40158-145">Nākamajā tabulā ir parādītas iespējamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="40158-145">The following table shows the possible values.</span></span>

| <span data-ttu-id="40158-146">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="40158-146">Connection status</span></span> | <span data-ttu-id="40158-147">Apraksts</span><span class="sxs-lookup"><span data-stu-id="40158-147">Description</span></span> | <span data-ttu-id="40158-148">Vai var izmantot plānošanas optimizāciju?</span><span class="sxs-lookup"><span data-stu-id="40158-148">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="40158-149">Savienojums izveidots</span><span class="sxs-lookup"><span data-stu-id="40158-149">Connected</span></span> | <span data-ttu-id="40158-150">Ir izveidots savienojums starp plānošanas optimizācijas pakalpojumu un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="40158-150">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="40158-151">Jā</span><span class="sxs-lookup"><span data-stu-id="40158-151">Yes</span></span> |
| <span data-ttu-id="40158-152">Savienojuma iespējošana</span><span class="sxs-lookup"><span data-stu-id="40158-152">Enabling connection</span></span> | <span data-ttu-id="40158-153">Pieprasījums ieslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="40158-153">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="40158-154">Nē</span><span class="sxs-lookup"><span data-stu-id="40158-154">No</span></span> |
| <span data-ttu-id="40158-155">Savienojums pārtraukts</span><span class="sxs-lookup"><span data-stu-id="40158-155">Disconnected</span></span> | <span data-ttu-id="40158-156">Nav savienojuma ar plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="40158-156">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="40158-157">Savienojumu var ieslēgt no LCS, kā aprakstīts iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="40158-157">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="40158-158">Nē</span><span class="sxs-lookup"><span data-stu-id="40158-158">No</span></span> |
| <span data-ttu-id="40158-159">Savienojuma atspējošana</span><span class="sxs-lookup"><span data-stu-id="40158-159">Disabling connection</span></span> | <span data-ttu-id="40158-160">Pieprasījums izslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="40158-160">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="40158-161">Nē</span><span class="sxs-lookup"><span data-stu-id="40158-161">No</span></span> |
| <span data-ttu-id="40158-162">Statusa iegūšana</span><span class="sxs-lookup"><span data-stu-id="40158-162">Getting status</span></span> | <span data-ttu-id="40158-163">Sistēma gaida statusa informāciju no plānošanas optimizācijas pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="40158-163">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="40158-164">Nē</span><span class="sxs-lookup"><span data-stu-id="40158-164">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="40158-165">Iespēja Plānošanas optimizācijas izmantošana</span><span class="sxs-lookup"><span data-stu-id="40158-165">The Use Planning Optimization option</span></span>

<span data-ttu-id="40158-166">Opcijas **Izmantot plānošanas optimizāciju** iestatījums nosaka, kuru plānošanas programmu izmanto vispārējai plānošanai:</span><span class="sxs-lookup"><span data-stu-id="40158-166">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="40158-167">**Jā** – plānošanas optimizācija tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="40158-167">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="40158-168">**Nē** - Iebūvētā Supply Chain Management plānošanas programma tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="40158-168">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="40158-169">Ja esošie plānošanas pakešuzdevumi, kas tika izveidoti iebūvētās Supply Chain Management programmai, ir aktivizēti, kamēr opcija **Izmantot plānošanas optimizāciju** ir iestatīta uz **Jā**, šie darbi neizdosies.</span><span class="sxs-lookup"><span data-stu-id="40158-169">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="40158-170">Integrēšana ar iestatījumu</span><span class="sxs-lookup"><span data-stu-id="40158-170">Integration with the setup</span></span>

<span data-ttu-id="40158-171">Ja plānošanas optimizācija ir ieslēgta, vispārējā plānošana tiek veikta, izmantojot plānošanas optimizācijas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="40158-171">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="40158-172">Šādā gadījumā tiek ietekmēti vispārējās plānošanas rezultāti un līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="40158-172">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40158-173">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="40158-173">Additional resources</span></span>

[<span data-ttu-id="40158-174">Priekšskatījuma noteikumi un nosacījumi</span><span class="sxs-lookup"><span data-stu-id="40158-174">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="40158-175">Plānošanas optimizācijas apskats</span><span class="sxs-lookup"><span data-stu-id="40158-175">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="40158-176">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="40158-176">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="40158-177">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="40158-177">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="40158-178">Filtru lietošana plānam</span><span class="sxs-lookup"><span data-stu-id="40158-178">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="40158-179">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="40158-179">Cancel a planning job</span></span>](cancel-planning-job.md)
