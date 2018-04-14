---
title: "Brīdinājumu pārskats"
description: "Šajā tēmā ir sniegta vispārēja informācija par brīdinājumu pakešveida apstrādi programmā Microsoft Dynamics 365 for Finance and Operations. Brīdinājumus var izmantot, lai saņemtu informāciju par notikumiem, kurus vēlaties izsekot darbdienas laikā."
author: tjvass
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: 1f0b5ff383c8bb2d1ac892ef771e15f0afec2655
ms.contentlocale: lv-lv
ms.lasthandoff: 03/23/2018

---

# <a name="alerts-overview"></a><span data-ttu-id="6c41d-104">Brīdinājumu pārskats</span><span class="sxs-lookup"><span data-stu-id="6c41d-104">Alerts overview</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/pre-release.md)] 

## <a name="about-alerts"></a><span data-ttu-id="6c41d-105">Par brīdinājumiem</span><span class="sxs-lookup"><span data-stu-id="6c41d-105">About alerts</span></span>
<span data-ttu-id="6c41d-106">Brīdinājumus ģenerē kritisko notikumu ziņošanas sistēma par programmā Microsoft Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6c41d-106">Alerts form a notification system for critical events in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="6c41d-107">Brīdinājumus var izmantot, lai saņemtu informāciju par notikumiem, kurus vēlaties izsekot darbdienas laikā.</span><span class="sxs-lookup"><span data-stu-id="6c41d-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="6c41d-108">Jūs varat viegli izveidot brīdinājumu kārtulas, lai tādējādi saņemtu brīdinājumus par nokavētām piegādēm, dzēstiem pasūtījumiem, cenu izmaiņām vai citiem notikumiem, uz kuriem jāreaģē.</span><span class="sxs-lookup"><span data-stu-id="6c41d-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="6c41d-109">Uzņēmuma resursu plānošanas (ERP) procesā ir vairāki tipiski scenāriji, kuros var izmantot programmas Finance and Operations brīdinājumu funkciju.</span><span class="sxs-lookup"><span data-stu-id="6c41d-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature in Finance and Operations can be used.</span></span> <span data-ttu-id="6c41d-110">Tālāk ir sniegti daži piemēri.</span><span class="sxs-lookup"><span data-stu-id="6c41d-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="6c41d-111">1. scenārijs. Brīdinājuma kārtulas izveidošana jaunam pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="6c41d-111">Scenario 1: Create an alert rule for new sales orders</span></span>
1. <span data-ttu-id="6c41d-112">Atveriet lapu **Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="6c41d-113">Darbību rūts cilnes **Opcijas** grupā **Kopīgot** atlasiet **Izveidot pielāgotu brīdinājumu**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="6c41d-114">Dialoglodziņa **Izveidot brīdinājumu kārtulu** kopsavilkuma cilnes **Brīdināt, ja** laukā **Notikums** atlasiet **Ir izveidots ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="6c41d-115">2. scenārijs. Brīdinājuma kārtulas izveidošana piegādes datuma atlikšanai.</span><span class="sxs-lookup"><span data-stu-id="6c41d-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>
1. <span data-ttu-id="6c41d-116">Atveriet lapu **Visi pirkšanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="6c41d-117">Lai piekļūtu pirkšanas pasūtījuma datiem, atlasiet pirkšanas pasūtījuma ID.</span><span class="sxs-lookup"><span data-stu-id="6c41d-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="6c41d-118">Izvērsiet kopsavilkuma cilni **Pirkšanas pasūtījuma galvene** .</span><span class="sxs-lookup"><span data-stu-id="6c41d-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="6c41d-119">Darbību rūts cilnes **Opcijas** grupā **Kopīgot** atlasiet **Izveidot pielāgotu brīdinājumu**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="6c41d-120">Dialoglodziņa **Izveidot brīdinājumu kārtulu** kopsavilkuma cilnes **Brīdināt, ja** laukā **Lauks** atlasiet **Piegādes datums**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="6c41d-121">Laukā **Notikums** atlasiet **ir atlikts**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="6c41d-122">Kad dialoglodziņš **Izveidot brīdinājuma kārtulu** ir aizvērts, izveidotā kārtula tiek parādīta lapā **Brīdinājuma kārtulu pārvaldīšana**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="6c41d-123">Lapu **Brīdinājuma kārtulu pārvaldīšana** var izmantot, lai atjauninātu esošās brīdinājuma kārtulas.</span><span class="sxs-lookup"><span data-stu-id="6c41d-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="6c41d-124">Piemēram, var mainīt notikumu aktivizēšanas elementus, atjaunināt notikumu paziņojumus un atjaunināt beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="6c41d-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="6c41d-125">Lai atvērtu lapu **Brīdinājuma kārtulu pārvaldīšana**, izmantojiet darbību rūts cilnes **Opcijas** pogu **Brīdināt**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="6c41d-126">Kas notiek, ja tiek izveidota brīdinājuma kārtula?</span><span class="sxs-lookup"><span data-stu-id="6c41d-126">What occurs when an alert rule is created?</span></span>
<span data-ttu-id="6c41d-127">Izveidojot brīdinājuma kārtulas, iepriekš definētu notikumu var saistīt ar noteiktu lauku.</span><span class="sxs-lookup"><span data-stu-id="6c41d-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="6c41d-128">Piemēram, iestājas laukā norādītais datums vai tiek mainīts lauka saturs.</span><span class="sxs-lookup"><span data-stu-id="6c41d-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="6c41d-129">Vai arī var saistīt notikumu ar konkrētas lapas ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="6c41d-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="6c41d-130">Piemēram, tiek izveidots vai dzēsts ieraksts.</span><span class="sxs-lookup"><span data-stu-id="6c41d-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="6c41d-131">Ja notiek lapā konkrētajam laukam vai ierakstam atlasītais notikums, tiek nosūtīts brīdinājums.</span><span class="sxs-lookup"><span data-stu-id="6c41d-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="6c41d-132">Piemēram, tiek izveidota kārtula, kurā noteikta pirkšanas pasūtījuma rindas lauks **Piegādes datums** tiek saistīts ar notikumu **šis izpildes termiņš bija pirms šāda laika**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="6c41d-133">Tiek iestatīts piecu dienu laika ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="6c41d-133">You set the time frame to five days.</span></span> <span data-ttu-id="6c41d-134">Šādā gadījumā piecas dienas pēc pirkšanas pasūtījuma rindas piegādes datuma sasniegšanas tiek nosūtīts brīdinājums.</span><span class="sxs-lookup"><span data-stu-id="6c41d-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="6c41d-135">Turklāt brīdinājuma kārtulas varat precizēt, iestatot nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="6c41d-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="6c41d-136">Piemēram, brīdinājumus var nosūtīt par jaunajiem pirkšanas pasūtījumiem, kas tiek izveidoti noteiktiem kreditoru kontiem.</span><span class="sxs-lookup"><span data-stu-id="6c41d-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="6c41d-137">Sagatavošanās brīdinājuma izveidei</span><span class="sxs-lookup"><span data-stu-id="6c41d-137">Preparing for an alert</span></span>
<span data-ttu-id="6c41d-138">Pirms brīdinājuma kārtulas iestatīšanas padomājiet, kad un kādās situācijās vēlaties saņemt brīdinājumus.</span><span class="sxs-lookup"><span data-stu-id="6c41d-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="6c41d-139">Kad ir zināms, par kuriem notikumiem vēlaties saņemt paziņojumus, programmā Finance and Operations atveriet lapu, kurā tiek parādīti dati, kas izraisa šo notikumu.</span><span class="sxs-lookup"><span data-stu-id="6c41d-139">When you know which event you want to be notified about, in Finance and Operations, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="6c41d-140">Notikums var būt datums, kas iestājas, vai noteiktas izmaiņas, kuras ir veiktas.</span><span class="sxs-lookup"><span data-stu-id="6c41d-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="6c41d-141">Tāpēc ir jāatver lapa, kur ir norādīts datums vai kur ir redzams lauks, kur tiek parādītas izmaiņas vai jaunais ieraksts, kurš tiek izveidots.</span><span class="sxs-lookup"><span data-stu-id="6c41d-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="6c41d-142">Kad šī informācija ir iegūta, var izveidot brīdinājuma kārtulu.</span><span class="sxs-lookup"><span data-stu-id="6c41d-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="6c41d-143">Brīdinājuma kārtulas komponenti</span><span class="sxs-lookup"><span data-stu-id="6c41d-143">Components of an alert rule</span></span>
<span data-ttu-id="6c41d-144">Brīdinājuma kārtula ietver piecus komponentus.</span><span class="sxs-lookup"><span data-stu-id="6c41d-144">An alert rule has five components:</span></span>

- <span data-ttu-id="6c41d-145">**Notikums** — notikums, kas aktivizē brīdinājuma kārtulu var būt datums, kas iestājas, vai noteiktas izmaiņas, kas ir veiktas.</span><span class="sxs-lookup"><span data-stu-id="6c41d-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="6c41d-146">Notikumu definē dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Sūtīt e-pasta brīdinājumus par darba statusa izmaiņām**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="6c41d-147">**Nosacījums** — lai kontrolētu brīdinājuma par notikumiem saņemšanas laiku, dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt par** var atlasīt kārtulas saturu.</span><span class="sxs-lookup"><span data-stu-id="6c41d-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="6c41d-148">Kārtulu var piešķirt vai nu tikai pašreizējam ierakstam, vai visiem lapā redzamajiem ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="6c41d-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="6c41d-149">Ja kārtulas attiecas uz visām juridiskajām personām, var iestatīt vienuma **Visas organizācijas** opciju **Jā**.</span><span class="sxs-lookup"><span data-stu-id="6c41d-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="6c41d-150">**Kārtulas derīguma termiņa beigas** — dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt līdz** var norādīt, cik ilgi brīdinājuma kārtulai jādarbojas.</span><span class="sxs-lookup"><span data-stu-id="6c41d-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="6c41d-151">**Saturs** — dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt ar** var norādīt tēmas un ziņojuma tekstu, kurš jāizmanto brīdinājuma ziņojumos.</span><span class="sxs-lookup"><span data-stu-id="6c41d-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="6c41d-152">**Lietotājs** — dialoglodziņa **Izveidot brīdinājuma kārtulu** kopsavilkuma cilnē **Brīdināt kuru** var norādīt, kuram lietotājam jāsaņem brīdinājuma ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="6c41d-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="6c41d-153">Pēc noklusējuma tiek atlasīts jūsu lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="6c41d-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c41d-154">Šī opcija attiecas tikai uz organizācijas administratoriem.</span><span class="sxs-lookup"><span data-stu-id="6c41d-154">This option is restricted to organization administrators.</span></span>
