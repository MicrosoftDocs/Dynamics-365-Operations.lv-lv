---
title: Kopuma izpildes paziņojumi
description: Šajā tēmā ir aprakstīti kopuma izpildes paziņojumi un paskaidrots, kā tos iestatīt.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fee112d3211f619b2146dd21c4f8a52ad33667d6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019158"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="d36c9-103">Kopuma izpildes paziņojumi</span><span class="sxs-lookup"><span data-stu-id="d36c9-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d36c9-104">*Kopuma izpildes paziņojumu* līdzeklis izmanto biznesa notikumus un darbību centru, lai piegādātu paziņojumus, kas saistīti ar kopuma izpildi.</span><span class="sxs-lookup"><span data-stu-id="d36c9-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="d36c9-105">Tas ļauj norādīt notikumu tipus, kas ģenerē paziņojumus, noliktavas, kas tos ģenerē, un lietotājus, kuri tos saņem.</span><span class="sxs-lookup"><span data-stu-id="d36c9-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="d36c9-106">Navigācijas joslas labajā pusē esošā poga **Rādīt ziņojumus** (zvana simbolu) norāda, kad pašreizējam lietotājam ir pieejams darbību centra ziņojums.</span><span class="sxs-lookup"><span data-stu-id="d36c9-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="d36c9-107">Lietotājs var atlasīt pogu **Rādīt ziņojumus**, lai atvērtu darbību centru un pārskatītu ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="d36c9-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="d36c9-108">Biznesa notikumi rodas, kad tiek darbināti biznesa procesi.</span><span class="sxs-lookup"><span data-stu-id="d36c9-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="d36c9-109">Biznesa procesus veido uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="d36c9-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="d36c9-110">Biznesa procesa laikā lietotāji, kas piedalās tajā, veic biznesa darbības, lai veiktu šos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="d36c9-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="d36c9-111">Biznesa notikumi nodrošina mehānismu, kas ļauj ārējām sistēmām saņemt paziņojumus no Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="d36c9-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="d36c9-112">Šādā veidā sistēma var veikt biznesa darbības, atbildot uz biznesa notikumiem.</span><span class="sxs-lookup"><span data-stu-id="d36c9-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="d36c9-113">Plašāku informāciju skatiet [Brīdinājumi kā biznesa notikumi](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="d36c9-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="d36c9-114">Līdzekļa Kopuma izpildes paziņojumu ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="d36c9-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="d36c9-115">Lai varētu izmantot līdzekli *Kopuma izpildes paziņojumi*, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="d36c9-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="d36c9-116">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="d36c9-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d36c9-117">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="d36c9-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d36c9-118">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="d36c9-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d36c9-119">**Līdzekļa nosaukums:** *Kopuma izpildes paziņojumi*</span><span class="sxs-lookup"><span data-stu-id="d36c9-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="d36c9-120">Scenārijs: sūtīt kopuma partijas izpildes paziņojumus darbību centram</span><span class="sxs-lookup"><span data-stu-id="d36c9-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="d36c9-121">Šajā scenārijā ir parādīta beigu plūsma paziņojumu par kopuma partijas izpildes kļūdu nosūtīšanai uz noteiktu lomu, izmantojot darbību centru.</span><span class="sxs-lookup"><span data-stu-id="d36c9-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="d36c9-122">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="d36c9-122">Make demo data available</span></span>

<span data-ttu-id="d36c9-123">Lai sekotu šim scenārijam, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="d36c9-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="d36c9-124">Pārliecinieties, vai kopumi ir palaisti partijas režīmā</span><span class="sxs-lookup"><span data-stu-id="d36c9-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="d36c9-125">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktavas pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="d36c9-126">Kopsavilkuma cilnē **Kopuma apstrāde** iestatiet opciju **Kopuma apstrādi partijās** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="d36c9-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="d36c9-127">Ja vēlaties atspējot kopuma partijas izpildes paziņojumus, iestatiet opciju **Atspējot kopuma apstrādes partijas paziņojumus** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="d36c9-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="d36c9-128">Konfigurēt kopuma paziņojuma politiku</span><span class="sxs-lookup"><span data-stu-id="d36c9-128">Configure a wave notification policy</span></span>

<span data-ttu-id="d36c9-129">Kopuma paziņojumu politikas definē sūtīto paziņojumu veidus un lietotājus, kuriem tiek sūtīts paziņojums.</span><span class="sxs-lookup"><span data-stu-id="d36c9-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="d36c9-130">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Kopumi \> Kopuma paziņojumu politikas**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="d36c9-131">Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d36c9-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="d36c9-132">**Kopuma paziņojumu politika:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="d36c9-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="d36c9-133">**Apraksts:** *Noliktavas 24 kopuma partijas kļūda*</span><span class="sxs-lookup"><span data-stu-id="d36c9-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="d36c9-134">**Sūtīt paziņojumu par:** *Tikai kļūda*</span><span class="sxs-lookup"><span data-stu-id="d36c9-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="d36c9-135">**Lomai:** *Sistēmas administrators*</span><span class="sxs-lookup"><span data-stu-id="d36c9-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="d36c9-136">Tā kā šajā scenārijā tiek izmantoti demonstrācijas dati, tiek atlasīta loma *Sistēmas administrators*, kas ir gadījumam.</span><span class="sxs-lookup"><span data-stu-id="d36c9-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="d36c9-137">Tādēļ, tā kā esat pieteicies kā sistēmas administrators, saņemsit paziņojumus.</span><span class="sxs-lookup"><span data-stu-id="d36c9-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="d36c9-138">Tomēr praksē parasti ir jāatlasa precīzāka loma, lai paziņotu par kopuma paketes izpildes kļūdām, piemēram, *Noliktavas pārvaldnieks*.</span><span class="sxs-lookup"><span data-stu-id="d36c9-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="d36c9-139">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="d36c9-140">Konfigurēt kopuma veidni</span><span class="sxs-lookup"><span data-stu-id="d36c9-140">Configure a wave template</span></span>

<span data-ttu-id="d36c9-141">Kopuma veidnes ļauj saistīt noteiktas kopuma metodes ar atbilstošo kopuma etiķešu veidni.</span><span class="sxs-lookup"><span data-stu-id="d36c9-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="d36c9-142">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="d36c9-143">Saraksta rūtī iestatiet **Kopuma veidnes tipa** lauku uz *Nosūtīšana* un pēc tam atlasiet *24 nosūtīšanas noklusējuma* kopuma veidni noliktavai 24.</span><span class="sxs-lookup"><span data-stu-id="d36c9-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="d36c9-144">Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Kopuma paziņojumu politika** uz *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="d36c9-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="d36c9-145">Konfigurēt darba veidni</span><span class="sxs-lookup"><span data-stu-id="d36c9-145">Configure a work template</span></span>

<span data-ttu-id="d36c9-146">Darba veidnes tiek izmantotas kopuma izpildes laikā, lai ģenerētu darbu.</span><span class="sxs-lookup"><span data-stu-id="d36c9-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="d36c9-147">Šajā scenārijā kopuma izpildei ir jāaktivizē kļūda.</span><span class="sxs-lookup"><span data-stu-id="d36c9-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="d36c9-148">Iestatot darba veidnes vaicājumu izmantot neesošu noliktavu, jūs nodrošināt, ka kopuma izpilde neizdodas un tādēļ nosūta paziņojumu.</span><span class="sxs-lookup"><span data-stu-id="d36c9-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="d36c9-149">Doties uz **Noliktavas pārvaldība \> Iestatījumi \> Darbs \> Darba veidnes**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d36c9-150">Saraksta rūtī iestatiet **Kopuma veidnes tipa** lauku uz *Pārdošanas pasūtījumi* un pēc tam atlasiet *24 SO Stage* darba veidni noliktavai 24.</span><span class="sxs-lookup"><span data-stu-id="d36c9-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="d36c9-151">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="d36c9-152">Vaicājumu redaktora dialoglodziņā cilnē **Diapazons** rediģējiet tālāk norādīto rindu (vai pievienojiet to, ja tāda nav):</span><span class="sxs-lookup"><span data-stu-id="d36c9-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="d36c9-153">**Tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="d36c9-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="d36c9-154">**Atveidotā tabula:** *Pagaidu darba darbības*</span><span class="sxs-lookup"><span data-stu-id="d36c9-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="d36c9-155">**Lauks:** *Noliktava*</span><span class="sxs-lookup"><span data-stu-id="d36c9-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="d36c9-156">**Kritēriji:** Mainīt vērtību no *24* uz *Kļūda*.</span><span class="sxs-lookup"><span data-stu-id="d36c9-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="d36c9-157">Atlasiet **Labi** un apstipriniet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="d36c9-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="d36c9-158">Izveidot pārdošanas pasūtījumu un nodot to noliktavai</span><span class="sxs-lookup"><span data-stu-id="d36c9-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="d36c9-159">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījums \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="d36c9-160">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d36c9-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="d36c9-161">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d36c9-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d36c9-162">**Noliktava:** *24*</span><span class="sxs-lookup"><span data-stu-id="d36c9-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="d36c9-163">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet otru rindu, kurai ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="d36c9-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="d36c9-164">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d36c9-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d36c9-165">**Daudzums:** *10*</span><span class="sxs-lookup"><span data-stu-id="d36c9-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="d36c9-166">Šie krājumi un daudzumi ir tikai piemēri.</span><span class="sxs-lookup"><span data-stu-id="d36c9-166">These items and quantities are only examples.</span></span> <span data-ttu-id="d36c9-167">Krājumiem ir jābūt pietiekamiem norādītajā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="d36c9-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="d36c9-168">Kamēr jaunā pasūtījuma rinda joprojām ir atlasīta, kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas**, atlasiet rīkjoslā **Krājumi \> Rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="d36c9-169">Lapā **Rezervācija** darbību rūtī atlasiet **Rezervēt vietu**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="d36c9-170">Tad aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="d36c9-170">Then close the page.</span></span>
1. <span data-ttu-id="d36c9-171">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="d36c9-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="d36c9-172">Paziņojumi no kopuma pakešuzdevuma izpildes</span><span class="sxs-lookup"><span data-stu-id="d36c9-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="d36c9-173">Atkarībā no biznesa notikumu iestatījuma, jūs visbeidzot saņemsiet paziņojumu par kopuma izpildes kļūmi.</span><span class="sxs-lookup"><span data-stu-id="d36c9-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="d36c9-174">Darbību centra ziņojums līdzīgs šim piemēram un ietvers saiti uz kopumu, kas neizdevās.</span><span class="sxs-lookup"><span data-stu-id="d36c9-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="d36c9-175">**Kopuma izpildes laikā radās kļūda**</span><span class="sxs-lookup"><span data-stu-id="d36c9-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="d36c9-176">Radās kļūda, izpildot kopumu USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="d36c9-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="d36c9-177">Pēdējie ziņojumi: kopumam USMF-000000001 netika izveidoti -000000001.</span><span class="sxs-lookup"><span data-stu-id="d36c9-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="d36c9-178">**Statuss**</span><span class="sxs-lookup"><span data-stu-id="d36c9-178">**STATUS**</span></span>  
> <span data-ttu-id="d36c9-179">Aktīvie</span><span class="sxs-lookup"><span data-stu-id="d36c9-179">Active</span></span>
>
> <span data-ttu-id="d36c9-180">Atvērt kopuma detalizēto informāciju</span><span class="sxs-lookup"><span data-stu-id="d36c9-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
