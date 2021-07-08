---
title: Darba sākšana ar plānošanas optimizāciju
description: Šajā tēmā ir paskaidrots, kā sākt izmantot plānošanas optimizācijas funkcionalitāti.
author: ChristianRytt
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 2867a4f9418e9435e2980fc24314914595ec44d0
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301678"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="e949b-103">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="e949b-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e949b-104">Kā [iepriekš paziņots](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), ir ieplānota plānošanas optimizācija, kas aizstātu esošo iebūvēto vispārējās plānošanas programmu.</span><span class="sxs-lookup"><span data-stu-id="e949b-104">As [previously announced](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="e949b-105">Ja pašlaik izmantojat iebūvēto vispārējās plānošanas programmu, jums tūlīt jāsāk plānot migrāciju uz plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="e949b-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="e949b-106">Ir svarīgi nekavējoties sākt migrācijas procesu, jo, kad tiek ieviests nolietojums, jūsu darbības var tikt ietekmētas.</span><span class="sxs-lookup"><span data-stu-id="e949b-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="e949b-107">Lai izvairītos no problēmām pēdējā brīdī, kad tiek ieviests nolietojums, mēs iesakām pabeigt migrāciju pirms 2020. gada 1. decembra.</span><span class="sxs-lookup"><span data-stu-id="e949b-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="e949b-108">Plānošanas optimizācijas funkcionalitāte pašlaik neatbalsta visus līdzekļus, kas ir pieejami Supply Chain Management iebūvētajā plānošanas programmā.</span><span class="sxs-lookup"><span data-stu-id="e949b-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="e949b-109">Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama plānošanas optimizācijā, atbilst jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="e949b-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="e949b-110">Pašlaik plānošanas optimizācijas funkcionalitāte Dynamics Lifecycle Services (LCS) netiek ieslēgta pēc noklusējuma, tāpēc jums ir iespēja veikt novērtēšanu pirms šī līdzekļa ieslēgšanas.</span><span class="sxs-lookup"><span data-stu-id="e949b-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="e949b-111">Jums jāpieprasa migrācijas izņēmumu plānošanas optimizācijā, ja vispārējās plānošanas process neiekļauj ražošanu (vispārējās plānošanas ģenerētus plānotos ražošanas pasūtījumus), un jums nepieciešama iebūvētā vispārējās plānošanas programmas versija, kas jaunāka par versiju 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="e949b-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="e949b-112">Sākot ar versiju 10.0.16, kļūda vidēs tiks parādīta, kad tiek palaista iebūvētā vispārējā plānošana bez plānoto ražošanas pasūtījumu ģenerēšanas.</span><span class="sxs-lookup"><span data-stu-id="e949b-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="e949b-113">Plānošanas optimizācija ir jāizmanto visiem jaunajiem izvietojumiem, kas vispārējās plānošanas laikā neģenerē plānotos ražošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="e949b-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="e949b-114">Īpašnieki, kam pieder esošās vides, kurās darbojas iebūvētā vispārējās plānošanas programma bez plānoto ražošanas pasūtījumu ģenerēšanas, saņems e-pastu ar sīkāku informāciju par izņēmuma procesu.</span><span class="sxs-lookup"><span data-stu-id="e949b-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="e949b-115">Iesakām jums strādāt ar partneri, lai novērtētu un plānotu migrāciju uz plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="e949b-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="e949b-116">Pirms plānošanas optimizācijas ieslēgšanas iesakām novērtēt plānošanas optimizācijas ietilpināšanas analīzes rezultātus.</span><span class="sxs-lookup"><span data-stu-id="e949b-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="e949b-117">Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e949b-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="availability"></a><span data-ttu-id="e949b-118">Pieejamība</span><span class="sxs-lookup"><span data-stu-id="e949b-118">Availability</span></span>

<span data-ttu-id="e949b-119">Plānošanas optimizācija pašlaik ir pieejama šādās Azure ģeogrāfiskās vietās: Amerikas Savienotās Valstis, Kanāda, Eiropa, Apvienotā Karaliste un Austrālija un Āzijas Klusā okeāna daļa.</span><span class="sxs-lookup"><span data-stu-id="e949b-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, Australia, and Asia Pacific.</span></span> <span data-ttu-id="e949b-120">Ja mēģināsit instalēt pievienojumprogrammu no cita ģeogrāfiskā reģiona, tad LCS rādīs ziņojumu, ka šī ģeogrāfiskā vērtība netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="e949b-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="e949b-121">Ņemiet vērā, ka plānošanas optimizācija neatbalsta Dynamics 365 Supply Chain Management lokālās izvietošanas.</span><span class="sxs-lookup"><span data-stu-id="e949b-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="e949b-122">Licencēšana</span><span class="sxs-lookup"><span data-stu-id="e949b-122">Licensing</span></span>

<span data-ttu-id="e949b-123">Ja vispārējo plānošanu varat veikt, izmantojot pašreizējo licenci, jums nav jāiegādājas papildu licence, lai sāktu izmantot plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="e949b-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

## <a name="install-and-enable-planning-optimization"></a><span data-ttu-id="e949b-124">Instalēt un iespējot plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="e949b-124">Install and enable Planning Optimization</span></span>

<span data-ttu-id="e949b-125">Lai izmantotu plānošanas optimizāciju, pārliecinieties, vai visi sistēmas priekšnosacījumi ir savā vietā, un pēc tam iespējojiet tās licences atslēgu un instalējiet plānošanas optimizācijas pievienojumprogrammu Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e949b-125">To use Planning Optimization, you must make sure your system has all of the prerequisites in place and then enable its license key and install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e949b-126">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="e949b-126">Prerequisites</span></span>

<span data-ttu-id="e949b-127">Pirms pabeidzat instalēt plānošanas optimizēšanas pievienojumprogrammu, ir jāievieš šādi priekšnosacījumi:</span><span class="sxs-lookup"><span data-stu-id="e949b-127">Before you install the Planning Optimization Add-in, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="e949b-128">Supply Chain Management ir jāpalaiž ar LCS iespējotu 2. līmeņa vai augstākas pieejamības vidi, (ne OneBox vide) ar Dynamics 365 Supply Chain Management versiju 10.0.7 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="e949b-128">You must be running Supply Chain Management on an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="e949b-129">Ja mēģināsit instalēt pievienojumprogrammu OneBox vidē, instalēšana netiks pabeigta, un tā būs jāatceļ.</span><span class="sxs-lookup"><span data-stu-id="e949b-129">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

- <span data-ttu-id="e949b-130">Jūsu sistēmā jābūt iestatītai Power Platform integrācijai.</span><span class="sxs-lookup"><span data-stu-id="e949b-130">Your system must be set up for Power Platform integration.</span></span> <span data-ttu-id="e949b-131">Papildinformāciju skatiet rakstā [Microsoft Power Platform integrācija ar Finance and Operations programmām](../../../fin-ops-core/dev-itpro/power-platform/overview.md).</span><span class="sxs-lookup"><span data-stu-id="e949b-131">For more information, see [Microsoft Power Platform integration with Finance and Operations apps](../../../fin-ops-core/dev-itpro/power-platform/overview.md).</span></span>

### <a name="enable-the-planning-optimization-license"></a><span data-ttu-id="e949b-132">Iespējot plānošanas optimizācijas licenci</span><span class="sxs-lookup"><span data-stu-id="e949b-132">Enable the Planning Optimization license</span></span>

<span data-ttu-id="e949b-133">Lai izmantotu plānošanas optimizāciju, ir jāiespējo tās konfigurācijas atslēga.</span><span class="sxs-lookup"><span data-stu-id="e949b-133">To use Planning Optimization, you must enable its configuration key.</span></span> <span data-ttu-id="e949b-134">Lai to izdarītu:</span><span class="sxs-lookup"><span data-stu-id="e949b-134">To do so:</span></span>

1. <span data-ttu-id="e949b-135">Ielieciet savu sistēmu uzturēšanas režīmā, kā aprakstīts sadaļā [Uzturēšanas režīms](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="e949b-135">Put your system into maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="e949b-136">Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="e949b-136">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="e949b-137">Cilnē **Konfigurācijas atslēgas** atzīmējiet izvēles rūtiņu **plānošanas optimizācijai**.</span><span class="sxs-lookup"><span data-stu-id="e949b-137">On the **Configuration keys** tab, select the check box for **Planning Optimization**.</span></span>
1. <span data-ttu-id="e949b-138">Izslēdziet uzturēšanas režīmu, kā aprakstīts sadaļā [Uzturēšanas režīms](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="e949b-138">Turn off maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="install-the-planning-optimization-add-in"></a><span data-ttu-id="e949b-139">Instalēt un iespējot plānošanas optimizācijas pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="e949b-139">Install the Planning Optimization Add-in</span></span>

<span data-ttu-id="e949b-140">Varat piekļūt pievienojumprogrammai no sava LCS projekta un ieslēgt plānošanas optimizācijas funkcionalitāti no Supply Chain Management lietotāja interfeisa (UI).</span><span class="sxs-lookup"><span data-stu-id="e949b-140">You must install the add-in from your LCS project and then turn on the Planning Optimization functionality from the Supply Chain Management user interface.</span></span>

<span data-ttu-id="e949b-141">Lai instalētu plānošanas optimizācijas pievienojumprogrammu:</span><span class="sxs-lookup"><span data-stu-id="e949b-141">To install the Planning Optimization Add-in:</span></span>

1. <span data-ttu-id="e949b-142">Piesakieties LCS un atveriet vēlamo vidi.</span><span class="sxs-lookup"><span data-stu-id="e949b-142">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="e949b-143">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="e949b-143">Go to **Full details**.</span></span>
1. <span data-ttu-id="e949b-144">Ritiniet līdz kopsavilkuma cilnei **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="e949b-144">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="e949b-145">Atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="e949b-145">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="e949b-146">Atlasiet **Plānošanas optimizācija**.</span><span class="sxs-lookup"><span data-stu-id="e949b-146">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="e949b-147">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="e949b-147">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="e949b-148">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="e949b-148">Select **Install**.</span></span>
1. <span data-ttu-id="e949b-149">Kopsavilkuma cilnē **Vides pievienojumprogramma** jāredz, ka tiek instalēta plānošanas optimizācija.</span><span class="sxs-lookup"><span data-stu-id="e949b-149">On the **Environment add-ins** FastTab, you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="e949b-150">Pēc dažām minūtēm **Instalē** jāmainās uz **Instalēts** (iespējams, lapa jāatsvaidzina).</span><span class="sxs-lookup"><span data-stu-id="e949b-150">After a few minutes, **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="e949b-151">Kad instalēšana ir pabeigta, varat aktivizēt plānošanas optimizāciju Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e949b-151">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="e949b-152">Plānošanas optimizācijas pievienojumprogrammas instalēšanas galvenais nolūks ir savienot pakalpojumu un vidi.</span><span class="sxs-lookup"><span data-stu-id="e949b-152">The main purpose of installing the Planning Optimization Add-in is to connect the service and the environment.</span></span> <span data-ttu-id="e949b-153">Tāpēc jums ir jāinstalē pievienojumprogramma atsevišķi katrai videi, kurā izmantosiet plānošanas optimizāciju neatkarīgi no tā, kāds kods tiek pārvietots starp vidēm.</span><span class="sxs-lookup"><span data-stu-id="e949b-153">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

## <a name="integrate-planning-optimization-with-your-system"></a><span data-ttu-id="e949b-154">Integrējiet plānošanas optimizāciju savā sistēmu</span><span class="sxs-lookup"><span data-stu-id="e949b-154">Integrate Planning Optimization with your system</span></span>

<span data-ttu-id="e949b-155">Lai konfigurētu, vai plānošanas optimizācijas pievienojumprogramma ir jāizmanto vispārējai plānošanai, dodieties uz **Vispārējā plānošana** \> **Iestatīšana** \> **Plānošanas optimizācijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="e949b-155">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

### <a name="connection-status"></a><span data-ttu-id="e949b-156">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="e949b-156">Connection status</span></span>

<span data-ttu-id="e949b-157">Savienojuma statuss norāda pašreizējo savienojuma statusu starp Supply Chain Management un plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="e949b-157">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="e949b-158">Nākamajā tabulā ir parādītas iespējamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="e949b-158">The following table shows the possible values.</span></span>

| <span data-ttu-id="e949b-159">Savienojuma statuss</span><span class="sxs-lookup"><span data-stu-id="e949b-159">Connection status</span></span> | <span data-ttu-id="e949b-160">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e949b-160">Description</span></span> | <span data-ttu-id="e949b-161">Vai var izmantot plānošanas optimizāciju?</span><span class="sxs-lookup"><span data-stu-id="e949b-161">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="e949b-162">Savienojums izveidots</span><span class="sxs-lookup"><span data-stu-id="e949b-162">Connected</span></span> | <span data-ttu-id="e949b-163">Ir izveidots savienojums starp plānošanas optimizācijas pakalpojumu un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e949b-163">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="e949b-164">Jā</span><span class="sxs-lookup"><span data-stu-id="e949b-164">Yes</span></span> |
| <span data-ttu-id="e949b-165">Savienojuma iespējošana</span><span class="sxs-lookup"><span data-stu-id="e949b-165">Enabling connection</span></span> | <span data-ttu-id="e949b-166">Pieprasījums ieslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="e949b-166">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e949b-167">Nē</span><span class="sxs-lookup"><span data-stu-id="e949b-167">No</span></span> |
| <span data-ttu-id="e949b-168">Savienojums pārtraukts</span><span class="sxs-lookup"><span data-stu-id="e949b-168">Disconnected</span></span> | <span data-ttu-id="e949b-169">Nav savienojuma ar plānošanas optimizācijas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="e949b-169">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="e949b-170">Savienojumu var ieslēgt no LCS, kā aprakstīts iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="e949b-170">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="e949b-171">Nē</span><span class="sxs-lookup"><span data-stu-id="e949b-171">No</span></span> |
| <span data-ttu-id="e949b-172">Savienojuma atspējošana</span><span class="sxs-lookup"><span data-stu-id="e949b-172">Disabling connection</span></span> | <span data-ttu-id="e949b-173">Pieprasījums izslēgt savienojumu ar plānošanas optimizācijas pakalpojumu pašlaik tiek veikts.</span><span class="sxs-lookup"><span data-stu-id="e949b-173">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e949b-174">Nē</span><span class="sxs-lookup"><span data-stu-id="e949b-174">No</span></span> |
| <span data-ttu-id="e949b-175">Statusa iegūšana</span><span class="sxs-lookup"><span data-stu-id="e949b-175">Getting status</span></span> | <span data-ttu-id="e949b-176">Sistēma gaida statusa informāciju no plānošanas optimizācijas pakalpojuma.</span><span class="sxs-lookup"><span data-stu-id="e949b-176">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="e949b-177">Nē</span><span class="sxs-lookup"><span data-stu-id="e949b-177">No</span></span> |

### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="e949b-178">Iespēja Plānošanas optimizācijas izmantošana</span><span class="sxs-lookup"><span data-stu-id="e949b-178">The Use Planning Optimization option</span></span>

<span data-ttu-id="e949b-179">Opcijas **Izmantot plānošanas optimizāciju** iestatījums nosaka, kuru plānošanas programmu izmanto vispārējai plānošanai:</span><span class="sxs-lookup"><span data-stu-id="e949b-179">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="e949b-180">**Jā** – plānošanas optimizācija tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="e949b-180">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="e949b-181">**Nē** - Iebūvētā Supply Chain Management plānošanas programma tiek izmantota vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="e949b-181">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

<span data-ttu-id="e949b-182">Šis iestatījums attiecas uz visām juridiskajām personām (uzņēmumiem).</span><span class="sxs-lookup"><span data-stu-id="e949b-182">This setting applies to all legal entities (companies).</span></span> <span data-ttu-id="e949b-183">Dažām juridiskajām personām nav iespējams izmantot Plānošanas optimizāciju un iebūvēto vispārējo plānošanu citās juridiskajās personas.</span><span class="sxs-lookup"><span data-stu-id="e949b-183">It is not possible to use Planning Optimization in some legal entities and the built-in master planning in other legal entities.</span></span>

> [!NOTE]
> <span data-ttu-id="e949b-184">Ja esošie plānošanas pakešuzdevumi, kas tika izveidoti iebūvētās Supply Chain Management programmai, ir aktivizēti, kamēr opcija **Izmantot plānošanas optimizāciju** ir iestatīta uz **Jā**, šie darbi neizdosies.</span><span class="sxs-lookup"><span data-stu-id="e949b-184">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="e949b-185">Integrēšana ar iestatījumu</span><span class="sxs-lookup"><span data-stu-id="e949b-185">Integration with the setup</span></span>

<span data-ttu-id="e949b-186">Ja plānošanas optimizācija ir ieslēgta, vispārējā plānošana tiek veikta, izmantojot plānošanas optimizācijas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="e949b-186">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="e949b-187">Šādā gadījumā tiek ietekmēti vispārējās plānošanas rezultāti un līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="e949b-187">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e949b-188">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e949b-188">Additional resources</span></span>

[<span data-ttu-id="e949b-189">Priekšskatījuma noteikumi un nosacījumi</span><span class="sxs-lookup"><span data-stu-id="e949b-189">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="e949b-190">Plānošanas optimizācijas apskats</span><span class="sxs-lookup"><span data-stu-id="e949b-190">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e949b-191">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="e949b-191">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="e949b-192">Plāna vēstures un plānošanas žurnālu skatīšana</span><span class="sxs-lookup"><span data-stu-id="e949b-192">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e949b-193">Filtru lietošana plānam</span><span class="sxs-lookup"><span data-stu-id="e949b-193">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="e949b-194">Plānošanas darba atcelšana</span><span class="sxs-lookup"><span data-stu-id="e949b-194">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
