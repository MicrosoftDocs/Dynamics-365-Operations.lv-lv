---
title: Darba sadale
description: Šajā tēmā ir sniegta informācija par darba sadales funkcionalitāti. Šī funkcionalitāte ļauj sadalīt lielus darba pasūtījumus vairākos mazākos darba pasūtījumos, kurus pēc tam var piešķirt vairākiem noliktavas darbiniekiem. Tādējādi vienu un to pašu darbu var vienlaikus paņemt vairāki noliktavas darbinieki.
author: mirzaab
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eae1e722a7c4d819cbca398eb14a2b36fa04eec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830766"
---
# <a name="work-split"></a><span data-ttu-id="0b9b6-105">Darba sadale</span><span class="sxs-lookup"><span data-stu-id="0b9b6-105">Work split</span></span>

<span data-ttu-id="0b9b6-106">Darba sadales funkcionalitāte ļauj sadalīt lielus darba ID (proti, darba pasūtījumus, kuriem ir vairākas rindas) vairākos mazākos darba ID, kurus pēc tam var piešķirt vairākiem noliktavas darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="0b9b6-107">Tādējādi vienu un to pašu darba izveides numuru var vienlaikus paņemt vairāki noliktavas darbinieki.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b9b6-108">Varat sadalīt tikai tādus darba pasūtījumus, kuru statuss ir *Atvērts* vai *Nepabeigts*.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="0b9b6-109">Darba sadales funkcionalitātes ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="0b9b6-109">Turn on the work split functionality</span></span>

<span data-ttu-id="0b9b6-110">Lai varētu izmantot darba sadales funkcionalitātiu, sistēmā ir jāieslēdz līdzeklis un tā priekšnosacījuma līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="0b9b6-111">Administratori var izmantot [līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļu statusu un tos ieslēgtu pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="0b9b6-112">Vispirms ieslēdziet priekšnosacījuma *Organizācijas mēroga darba aizturēšana* līdzekli, ja tas vēl nav ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="0b9b6-113">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="0b9b6-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="0b9b6-114">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="0b9b6-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0b9b6-115">**Līdzekļa nosaukums:** *Organizācijas līmeņa darba aizturēšana*</span><span class="sxs-lookup"><span data-stu-id="0b9b6-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="0b9b6-116">Kad šis līdzeklis ir aktivizēts, datu jaunināšana tiek automātiski piemērota pēc tam, kad līdzeklis ir ieslēgts visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="0b9b6-117">Pēc tam ieslēdziet līdzeli *Darba sadale*, kas ir norādīts tālāk norādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="0b9b6-118">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="0b9b6-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="0b9b6-119">**Līdzekļa nosaukums:** *Darba sadale*</span><span class="sxs-lookup"><span data-stu-id="0b9b6-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="0b9b6-120">Darba detalizētas informācijas un Visi darbi lapu uzlabojumi</span><span class="sxs-lookup"><span data-stu-id="0b9b6-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="0b9b6-121">*Darba sadales* līdzeklis pievieno tālāk minētās divas pogas cilnei **Darbs**, kas atrodas darbības rūtī **Darba detalizēta informācija** un lapās **Visi darbi**.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="0b9b6-122">**Sadalīt darbu** – sadala pašreizējā darba ID vairākos mazākos darba ID, kurus var apstrādāt atsevišķi darbinieki.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="0b9b6-123">**Atcelt darba sadales sesiju** — atceļ darba sadales sesiju un padara darbu pieejamu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="0b9b6-124">![Pogas Darba sadale un Atcelt darba sadales sesiju](media/Work_split_buttons.png "Pogas Darba sadale un Atcelt darba sadales sesiju")</span><span class="sxs-lookup"><span data-stu-id="0b9b6-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b9b6-125">Poga **Darba sadale** nav pieejama, ja ir izpildīts kāds no tālāk minētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="0b9b6-126">Darba statuss ir cits, nevis *Atvērts* vai *Nepabeigts*.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="0b9b6-127">Konteinera ID ir saistīts ar darba ID.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="0b9b6-128">(Konteineru nevar sistemātiski sadalīt, jo tam ir nepieciešamas fiziskas darbības.)</span><span class="sxs-lookup"><span data-stu-id="0b9b6-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="0b9b6-129">Darbs ir saistīts ar klasteri.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="0b9b6-130">Darba pasūtījuma veids ir cits, nevis viens no tālāk minētajiem veidiem.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="0b9b6-131">Pārdošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="0b9b6-131">Sales orders</span></span>
>    - <span data-ttu-id="0b9b6-132">Izejmateriālu izdošana</span><span class="sxs-lookup"><span data-stu-id="0b9b6-132">Raw material picking</span></span>
>    - <span data-ttu-id="0b9b6-133">Pārsūtīt izejas plūsmu</span><span class="sxs-lookup"><span data-stu-id="0b9b6-133">Transfer issue</span></span>
>
> - <span data-ttu-id="0b9b6-134">Pašlaik darbu sadala cits lietotājs.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-134">The work is currently being split by another user.</span></span> <span data-ttu-id="0b9b6-135">Ja mēģināt atvērt sadalīšanas lapu darbam, ko jau ir sadalījis cits lietotājs, tiek parādīts šāds kļūdas ziņojums: "Darbs ar ID \#\#\#\# pašlaik tiek sadalīts.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="0b9b6-136">Pēc dažām minūtēm mēģiniet vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-136">Retry in a few minutes.</span></span> <span data-ttu-id="0b9b6-137">Ja turpināt saņemt šādu paziņojumu, sazinieties ar vadītāju."</span><span class="sxs-lookup"><span data-stu-id="0b9b6-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="0b9b6-138">Jauns darba aizturēšanas iemesls *Sadalīt darbu* norāda, kad darba ID atrodas sadalīšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="0b9b6-139">Tas ir redzams gan lapā **Sadalīt darbu**, gan Warehouse Management mobile programmā, ja lietotājs mēģina palaist darbu.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-139">It's shown both on the **Split work** page and in the Warehouse Management mobile app if a user tries to run the work.</span></span> <span data-ttu-id="0b9b6-140">Ja tiek izmantoti aizturēšanas iemesli, lauka nosaukums **Aizturēts kopums** no darba ID tiek mainīts uz **Aizturēts**.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="0b9b6-141">Sākt darba sadali</span><span class="sxs-lookup"><span data-stu-id="0b9b6-141">Initiate a work split</span></span>

<span data-ttu-id="0b9b6-142">Līdzeklis pievieno jaunu **Darba sadales** lapu, kas ļauj lietotājiem sadalīt darba rindas no darba ID.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="0b9b6-143">Kad lapa tiek atvērta pirmo reizi, tā parāda rindas, kuru darba statuss ir *Atvērts* un kuras ir pieejamas sadalei.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="0b9b6-144">Darbības rūtī atlasiet **Sadalīt darbu**, lai apstrādātu atlasīto darbu.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="0b9b6-145">Lai sadalītu darbu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="0b9b6-146">Atveriet kādu no tālāk minētajām darba lapām.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="0b9b6-147">**Darba informācija** (**Noliktavas pārvaldība \> Darbs \> Darba informācija**)</span><span class="sxs-lookup"><span data-stu-id="0b9b6-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="0b9b6-148">**Viss darbs** (**Noliktavas pārvaldība \> Darbs \> Viss darbs**)</span><span class="sxs-lookup"><span data-stu-id="0b9b6-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="0b9b6-149">Režģī atlasiet darba ID, kuru sadalīt.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="0b9b6-150">Laukam **Darba pasūtījuma veids** jābūt iestatītam uz vienu no tālāk minētajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="0b9b6-151">Pārdošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="0b9b6-151">Sales orders</span></span>
    - <span data-ttu-id="0b9b6-152">Izejmateriālu izdošana</span><span class="sxs-lookup"><span data-stu-id="0b9b6-152">Raw material picking</span></span>
    - <span data-ttu-id="0b9b6-153">Pārsūtīt izejas plūsmu</span><span class="sxs-lookup"><span data-stu-id="0b9b6-153">Transfer issue</span></span>

1. <span data-ttu-id="0b9b6-154">Darbību rūts cilnē **Darbs** grupā **Darbs** atlasiet **Sadalīt darbu**.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="0b9b6-155">Tiek parādīta lapa **Sadalīt darbu** un parādītas darba rindas, kas ir atvērtas un pieejamas sadalīšanai.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="0b9b6-156">Pēc noklusējuma tiek parādītas tikai pieejamās darba rindas.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="0b9b6-157">Lai skatītu visas darba ID rindas (piemēram, rindas ar darba veidu *Izvietot*), virs režģa atzīmējiet izvēles rūtiņu **Rādīt visas rindas**.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="0b9b6-158">Tiek parādīts šāds paziņojums: "Lietotāji nevar apstrādāt darba rindas, līdz pabeidzat sadalīšanu un aizverat šo lapu."</span><span class="sxs-lookup"><span data-stu-id="0b9b6-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="0b9b6-159">Lauks pašreizējam darbam **Darba aizturēšanas iemesls** tiks iestatīts uz *Sadalīt darbu*, un darbs tiks aizturēts.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="0b9b6-160">![Aizturēšanas iemesls](media/Blocking_reason.png "Aizturēšanas iemesls")</span><span class="sxs-lookup"><span data-stu-id="0b9b6-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="0b9b6-161">Atlasiet rindas, kas jānoņem no pašreizējā darba ID un jāpievieno jaunā darba ID.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="0b9b6-162">Notiek tālāk aprakstītie notikumi:</span><span class="sxs-lookup"><span data-stu-id="0b9b6-162">The following events occur:</span></span>

    - <span data-ttu-id="0b9b6-163">Kad sadalāt darbu, atlasītā rinda vai rindas no sākotnējā darba ID tiek atceltas un pēc tam kopētas jaunā darba ID.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="0b9b6-164">Esošā darba veidnes struktūra un izvietojuma atrašanās vieta (un arī turpmākie izdošanas/izvietošanas pāri) tiek saglabāti.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="0b9b6-165">Tālāk minēto darba ID lauku vērtības tiek kopētas no oriģinālā darba uz jauno darbu.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="0b9b6-166">Kravas ID</span><span class="sxs-lookup"><span data-stu-id="0b9b6-166">Load ID</span></span>
        - <span data-ttu-id="0b9b6-167">Sūtījuma ID</span><span class="sxs-lookup"><span data-stu-id="0b9b6-167">Shipment ID</span></span>
        - <span data-ttu-id="0b9b6-168">Darba pasūtījuma veids</span><span class="sxs-lookup"><span data-stu-id="0b9b6-168">Work order type</span></span>
        - <span data-ttu-id="0b9b6-169">Pasūtījuma numurs</span><span class="sxs-lookup"><span data-stu-id="0b9b6-169">Order number</span></span>
        - <span data-ttu-id="0b9b6-170">Vieta</span><span class="sxs-lookup"><span data-stu-id="0b9b6-170">Site</span></span>
        - <span data-ttu-id="0b9b6-171">Noliktava</span><span class="sxs-lookup"><span data-stu-id="0b9b6-171">Warehouse</span></span>
        - <span data-ttu-id="0b9b6-172">Darba prioritāte</span><span class="sxs-lookup"><span data-stu-id="0b9b6-172">Work priority</span></span>
        - <span data-ttu-id="0b9b6-173">Darbu pūla ID</span><span class="sxs-lookup"><span data-stu-id="0b9b6-173">Work pool ID</span></span>
        - <span data-ttu-id="0b9b6-174">Kopuma ID</span><span class="sxs-lookup"><span data-stu-id="0b9b6-174">Wave ID</span></span>
        - <span data-ttu-id="0b9b6-175">Darba izveides numurs</span><span class="sxs-lookup"><span data-stu-id="0b9b6-175">Work creation number</span></span>

    - <span data-ttu-id="0b9b6-176">Tālāk minētie lauki netiek iekopēti jaunajā darba ID.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="0b9b6-177">**Darba ID** — no attiecīgās numuru secības tiek ģenerēts jauns darba ID.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="0b9b6-178">**Darba statuss** — šis lauks ir iestatīts uz *Atvērts*.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="0b9b6-179">**Aizturējis** — šis lauks sākotnēji ir iestatīts uz tukšu.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="0b9b6-180">**Mērķa numura zīmes ID** — šis lauks tiek atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="0b9b6-181">**Izveides datums un laiks** — šis lauks tiek iestatīts uz pašreizējo datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="0b9b6-182">**Aizturēts kopums/iesaldēts** — šis lauks tiek pārrakstīts oriģinālajam darba ID un jaunajam darba ID.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="0b9b6-183">Darbību rūtī atlasiet **Sadalīt darbu**.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="0b9b6-184">Kamēr darbs tiek sadalīts, tiek parādīts šāds paziņojums: "Darbības apstrāde — sadalīt darbu".</span><span class="sxs-lookup"><span data-stu-id="0b9b6-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="0b9b6-185">Kamēr šis ziņojums ir redzams, varat atcelt operāciju, ziņojuma lodziņā atlasot **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="0b9b6-186">Ja izvēles rūtiņa **Rādīt visas rindas** ir notīrīta, rinda, kas tika nodalīta un atcelta, režģī vairs netiks rādīta.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="0b9b6-187">Ja izvēles rūtiņa ir atzīmēta, jums būtu jāredz, ka šīs rindas vērtība **Darba statuss** ir mainīta uz *Atcelts*.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="0b9b6-188">Tiek norādīts tālāk redzamais paziņojums, kas norāda, ka jaunais darba ID ir izveidots: "Darbs \#\#\#\# ir izveidots, nodalot no sākotnējā darba \#\#\#\# ."</span><span class="sxs-lookup"><span data-stu-id="0b9b6-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="0b9b6-189">Citas darba rindas no sākotnējā darba ID (piemēram, *Izvietošanas* rindas) tiks koriģētas pēc nepieciešamības, lai atspoguļotu tās darba rindas, kas ir atceltas.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="0b9b6-190">Piemēram, ja oriģinālajam darba ID bija 15 rindu skaits *Nodot* un *Izdošanas* rindas ar kopējo daudzumu 10 tika atceltas, jaunais *Nodot* krājumu daudzums oriģinālajā darba ID tagad būs 5.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="0b9b6-191">Jaunais darbs netiks nekavējoties piešķirts nevienam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="0b9b6-192">Tomēr pēc nepieciešamības varat to piešķirt lietotājam, izmantojot lapas **Darba informācija** standarta funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b9b6-193">Varat sadalīt tikai tādus darba ID, kas satur divas vai vairākas pieejamās darba rindas.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="0b9b6-194">Ja atlasāt **Sadalīt darbu**, kurā ir tikai viena darba rinda, tiek parādīts šāds kļūdas ziņojums: "Vismaz vienai darba rindai ir jāpaliek sākotnējā darbā."</span><span class="sxs-lookup"><span data-stu-id="0b9b6-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="0b9b6-195">Šādā gadījumā sadalīšana netiks veikta.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="0b9b6-196">Pabeigt darba sadali</span><span class="sxs-lookup"><span data-stu-id="0b9b6-196">Finish a work split</span></span>

<span data-ttu-id="0b9b6-197">Lai pabeigtu darba sadali, ir jānoņem *Sadalīt darbu* aizturēšanas iemesls.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="0b9b6-198">Šo darbību var paveikt divos veidos.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="0b9b6-199">Lietotājs, kurš sadala darbu, aizver lapu **Sadalīt darbu**, augšējā labajā stūrī atlasot pogu **Aizvērt** (**X**).</span><span class="sxs-lookup"><span data-stu-id="0b9b6-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="0b9b6-200">Kad lapa tiek aizvērta, *Sadalīt darbu* aizturēšanas iemesls tiks noņemts.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="0b9b6-201">Šā darba stāvoklis *Aizturēts* tiks pārrēķināts, un, ja šim darbam nav neviena aizturēšanas iemesla, darbs tiks atjaunots.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="0b9b6-202">Katrs lietotājs atver darba ID un darbību rūtī atlasa pogu **Atcelt darba sadales sesiju**.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="0b9b6-203">*Sadalīt darbu* aizturēšanas iemesls tiks noņemts, un šā darba *Aizturēts* stāvoklis tiks pārrēķināts tāpat kā tad, kad lapa **Sadalīt darbu** tiek aizvērta.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="0b9b6-204">Kad *Sadalīt darbu* aizturēšanas iemesls ir noņemts, darbu var palaist mobilajā ierīcē, ar nosacījumu, ka stāvoklis **Aizturēts** darba ID ir iestatīts uz *Nē*.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-management-mobile-app"></a><span data-ttu-id="0b9b6-205">Kustības bloķēšana Warehouse Management mobile programmā</span><span class="sxs-lookup"><span data-stu-id="0b9b6-205">User blocking on the Warehouse Management mobile app</span></span>

<span data-ttu-id="0b9b6-206">Ja mēģināt izmantot Warehouse Management mobile programmu, lai palaistu saņemšanas darbu darba ID, kas jau ir sadalīts, saņemsit šādu kļūdas ziņojumu: "Darbs ar ID \#\#\#\# pašlaik tiek sadalīts."</span><span class="sxs-lookup"><span data-stu-id="0b9b6-206">If you try to use the Warehouse Management mobile app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="0b9b6-207">Ja saņemat šo ziņojumu, atlasiet **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="0b9b6-208">Pēc tam varat turpināt apstrādāt citu darbu.</span><span class="sxs-lookup"><span data-stu-id="0b9b6-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="0b9b6-209">Citas aizturētās operācijas</span><span class="sxs-lookup"><span data-stu-id="0b9b6-209">Other blocked operations</span></span>

<span data-ttu-id="0b9b6-210">Visas operācijas, kas pārveido darba rindas, darba krājumu darbības vai papildināšanas saites, kas saistītas ar sadalāmo darbu, neizdosies, un tiks parādīts šāds kļūdas ziņojums: "Darbs ar ID \#\#\#\# pašlaik tiek sadalīts."</span><span class="sxs-lookup"><span data-stu-id="0b9b6-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]