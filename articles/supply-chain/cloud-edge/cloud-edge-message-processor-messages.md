---
title: Ziņojumu apstrādātāja ziņojumi
description: Šajā tēmā ir sniegta informācija par ziņojumu procesora ziņojumu līdzekli mēroga vienības darba noslodzei.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 86f15831f11dc9fdcada9639858fd3b18cdc7503
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271105"
---
# <a name="message-processor-messages"></a><span data-ttu-id="c268f-103">Ziņojumu apstrādātāja ziņojumi</span><span class="sxs-lookup"><span data-stu-id="c268f-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c268f-104">Ziņojumu procesora ziņojumi tiek izmantoti, palaižot mākoņa un malas skalas vienības [ražošanas darba noslodzei](cloud-edge-workload-manufacturing.md) un [noliktavas pārvaldības darba noslodzei](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="c268f-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="c268f-105">Liela apjoma datu apmaiņa notiek starp centrmezgla un mēroga vienības izvietošanas vidi, lai tos sinhronizētu, bet *ziņojumu procesors* apstrādās tikai dažus no šiem datu apmaiņas veidiem..</span><span class="sxs-lookup"><span data-stu-id="c268f-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="c268f-106">Ziņojumu procesora apstrādātos ziņojumus varat skatīt, noklikšķinot uz **Sistēmas administrēšana > Ziņojumu procesors > Ziņojumu procesora ziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="c268f-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="c268f-107">Ziņojumu režģa kolonnas un filtri</span><span class="sxs-lookup"><span data-stu-id="c268f-107">Message grid columns and filters</span></span>

<span data-ttu-id="c268f-108">Jūs varat izmantot laukus **Ziņojumu procesoru ziņojumu** lapas augšpusē, lai palīdzētu atrast jebkurus jūsu meklētos ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="c268f-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="c268f-109">Lielākā daļa šo filtru atbilst kolonnu virsrakstiem ziņojumu režģī.</span><span class="sxs-lookup"><span data-stu-id="c268f-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="c268f-110">Ir pieejami šādi filtri un kolonnu virsraksti:</span><span class="sxs-lookup"><span data-stu-id="c268f-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="c268f-111">**Ziņojuma veids** – norāda ziņojuma veidu.</span><span class="sxs-lookup"><span data-stu-id="c268f-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="c268f-112">**Ziņojumu rinda** – norāda rindas nosaukumu, kurā tiek apstrādāts ziņojums.</span><span class="sxs-lookup"><span data-stu-id="c268f-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="c268f-113">Ir sniegtas šādas rindas:</span><span class="sxs-lookup"><span data-stu-id="c268f-113">The following queues are provided:</span></span>
  - <span data-ttu-id="c268f-114">*Mēroga vienība uz centrmezglu*</span><span class="sxs-lookup"><span data-stu-id="c268f-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="c268f-115">*Noliktavas izpildes mērogotās vienības centrmezgls*</span><span class="sxs-lookup"><span data-stu-id="c268f-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="c268f-116">*Ražošanas izpildes mērogotās vienības centrmezgls*</span><span class="sxs-lookup"><span data-stu-id="c268f-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="c268f-117">**Ziņojuma stāvoklis** - norāda ziņojuma stāvokli.</span><span class="sxs-lookup"><span data-stu-id="c268f-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="c268f-118">Pastāv sekojošie statusi:</span><span class="sxs-lookup"><span data-stu-id="c268f-118">The following states exists:</span></span>
  - <span data-ttu-id="c268f-119">*Ievietots rindā* – Ziņojumu ir gatavs ziņojuma procesora apstrādei.</span><span class="sxs-lookup"><span data-stu-id="c268f-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="c268f-120">*Apstrādāts* – Ziņojuma procesors veiksmīgi apstrādāja ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="c268f-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="c268f-121">*Atcelts* – ziņojums tika apstrādāts, bet apstrāde neizdevās.</span><span class="sxs-lookup"><span data-stu-id="c268f-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="c268f-122">**Zīņojuma saturs** - Šis filtrs veic pilnu teksta meklēšanu ziņojuma saturam.</span><span class="sxs-lookup"><span data-stu-id="c268f-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="c268f-123">(Ziņojuma saturs režģī netiek rādīts.) Vairumu speciālo simbolu (piemēram, "-") filtrs uzskata par atstarpēm, un visus atstarpju simbolus uzskata par Būla OR operatoriem.</span><span class="sxs-lookup"><span data-stu-id="c268f-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="c268f-124">T=Piemēram, ja meklējat noteiktu `journalid` vērtību, kas vienāda ar "USMF-123456", sistēma atradīs visus ziņojumus, kas satur "USMF" vai "123456", kas, visticamāk, būs garš saraksts.</span><span class="sxs-lookup"><span data-stu-id="c268f-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="c268f-125">Tāpēc labāk būtu ievadīt tikai "123456", jo tādējādi tiks atgriezti precīzāki rezultāti.</span><span class="sxs-lookup"><span data-stu-id="c268f-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="c268f-126">Ziņojuma veida piemērs: pieprasīt krājumu korekcijas finanšu atjauninājumu</span><span class="sxs-lookup"><span data-stu-id="c268f-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="c268f-127">Piemēram, **Ziņojuma veids** *Pieprasīt krājumu korekcijas finanšu atjauninājumu* tiek izmantots, lai izveidotu un grāmatotu inventarizācijas žurnālu centrmezglā, kad darbinieks izmanto noliktavas programmu, lai [reģistrētu krājumu korekciju](cloud-edge-warehouse-inventory-adjustment.md) mēroga vienības noliktavas pārvaldības darba noslodzei.</span><span class="sxs-lookup"><span data-stu-id="c268f-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="c268f-128">Tā kā šis konkrētais process rodas no mēroga vienības, lauks **Ziņojumu rinda** rāda vērtību *Mēroga vienība centrmezglam*.</span><span class="sxs-lookup"><span data-stu-id="c268f-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="c268f-129">Šim ziņojuma veidam mēroga vienības darba noslodze ieraksta ziņojumu kā daļu no noliktavas programmas krājumu pielāgošanas operācijas.</span><span class="sxs-lookup"><span data-stu-id="c268f-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="c268f-130">Ziņojuma dati pēc tam tiek pārsūtīti uz centrmezglu kā daļa no tā paša procesa, ko izmanto [Commerce Data Exchange arhitektūrai](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="c268f-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="c268f-131">Ziņojums tiks atjaunināts, lai parādītu **Ziņojuma stāvokli** kā *Ievietots rindā*.</span><span class="sxs-lookup"><span data-stu-id="c268f-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="c268f-132">Ziņojumu procesors tad mēģina apstrādāt ziņojumu un atjaunina **Ziņojuma stāvokli** uz *Apstrādāts* veiksmīgi, vai *Atcelts* kļūmes gadījumā.</span><span class="sxs-lookup"><span data-stu-id="c268f-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="c268f-133">Apskatīt ziņojumu žurnālu, ziņojuma saturu un detalizētu informāciju</span><span class="sxs-lookup"><span data-stu-id="c268f-133">View the message log, message content, and details</span></span>

<span data-ttu-id="c268f-134">Detalizētu informāciju par ziņojumu var atrast, atlasot to režģī un pēc tam atverot cilnes **Žurnāls** vai **Ziņojuma saturs** ziņojumu režģī, kur tiek rādīts katrs apstrādes notikums.</span><span class="sxs-lookup"><span data-stu-id="c268f-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="c268f-135">Cilne **Ziņojuma saturs** ir atkarīga no **Ziņojuma veida**, un tādēļ tā teksta garums būs atšķirīgs.</span><span class="sxs-lookup"><span data-stu-id="c268f-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="c268f-136">Tipisks ziņojuma satura teksts tiks sākts ar **{** un beigties ar **}** un starp tiem ir tādi lauku nosaukumi kā `journalId` kam seko **:** un vērtība, piemēram, *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="c268f-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="c268f-137">Rīkjosla cilnē **Žurnāls** ietver šādas pogas:</span><span class="sxs-lookup"><span data-stu-id="c268f-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="c268f-138">**Žurnāls** – parāda apstrādes rezultātus.</span><span class="sxs-lookup"><span data-stu-id="c268f-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="c268f-139">Tas ir īpaši noderīgi, lai saprastu iemeslus apstrādes kļūmei ziņojumiem, kuru **Apstrādes rezultāts** ir *Neizdevās*.</span><span class="sxs-lookup"><span data-stu-id="c268f-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="c268f-140">**Komplekts** – vairākas ziņojumu apstrādes operācijas var tikt izpildītas kā daļa no vienas un tās pašas pakešapstrādes.</span><span class="sxs-lookup"><span data-stu-id="c268f-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="c268f-141">Izvēlieties šo pogu, lai aplūkotu šos detalizētos datus.</span><span class="sxs-lookup"><span data-stu-id="c268f-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="c268f-142">Piemēram, varat redzēt, vai eksistē atkarības, kurām nepieciešams, lai sistēma apstrādātu noteiktus ziņojumus noteiktā secībā.</span><span class="sxs-lookup"><span data-stu-id="c268f-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="c268f-143">Ziņojumu procesora pakešuzdevums</span><span class="sxs-lookup"><span data-stu-id="c268f-143">Message processor batch job</span></span>

<span data-ttu-id="c268f-144">Palaižot mākoņa un malas izvietošanu, pakešuzdevums *Ziņojumu procesors* tiks automātiski atsaukts, kad apstrādei tiek izveidots jauns ziņojums, tāpēc jums nevajadzētu šo darbu plānot manuāli.</span><span class="sxs-lookup"><span data-stu-id="c268f-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="c268f-145">Ja nepieciešams, varat piekļūt pakešuzdevumam, noklikšķinot uz **Sistēmas administrēšana > Ziņojumu procesors > Ziņojumu procesors**.</span><span class="sxs-lookup"><span data-stu-id="c268f-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="c268f-146">Manuāli apstrādāt vai atcelt ziņojumu</span><span class="sxs-lookup"><span data-stu-id="c268f-146">Manually process or cancel a message</span></span>

<span data-ttu-id="c268f-147">Ja nepieciešams, varat manuāli apstrādāt vai atcelt ziņojumu atkarībā no tā pašreizējā stāvokļa.</span><span class="sxs-lookup"><span data-stu-id="c268f-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="c268f-148">Lai to izdarītu, atlasiet ziņojumu režģī un pēc tam atlasiet **Apstrādāt** vai **Atcelt** darbību rūtī</span><span class="sxs-lookup"><span data-stu-id="c268f-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="c268f-149">Iestatīt biznesa notikumus, lai piegādātu brīdinājumus par nesekmīgiem apstrādes rezultātiem</span><span class="sxs-lookup"><span data-stu-id="c268f-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="c268f-150">Papildus filtrēšanai **Ziņojuma stāvokļa** vērtībā *Atcelts*, lai pieprasītu neizdevušos ziņojumus, varat iestatīt [biznesa notikumus](../../fin-ops-core/dev-itpro/business-events/home-page.md) centrmazglā, lai brīdinātu jūs par neizdevušos apstrādes rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="c268f-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="c268f-151">Lai to izdarītu, aktivizējiet biznesa notikumu ar nosaukumu *Ziņojumu procesora ziņojums apstrādāts*  lapā **Biznesa notikumu katalogs** (**Sistēmas administrēšana > Iestatīšana > Biznesa notikumi > Biznesa notikumu katalogs**).</span><span class="sxs-lookup"><span data-stu-id="c268f-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="c268f-152">Kā aktivizēšanas procesa daļa jums tiks sniegta informācija, kas norāda, vai notikums ir specifisks vienai vai visām juridiskajām personām, un jānorāda **Galapunkta nosaukums**, kas jādefinē vispirms.</span><span class="sxs-lookup"><span data-stu-id="c268f-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="c268f-153">Ja **Kad rodas biznesa notikums** ir iestatīts uz *Microsoft Power Automate* (nevis *HTTPS*, piemēram), **Galapunkta nosaukums** tiks automātiski izveidots Supply Chain Management, pamatojoties uz *Microsoft Power Automate* iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="c268f-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="c268f-154">Microsoft Power Automate piemērs</span><span class="sxs-lookup"><span data-stu-id="c268f-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="c268f-155">Šajā piemērā izmantojiet **Kad rodas biznesa notikums** ar *Microsoft Power Automate* nosūta e-pasta ziņojumus, kuros ir InfoLog ziņojumi un hipersaites, lai atvērtu lapu **Ziņojumu procesora ziņojumi** noteiktam neizdevušās ziņojumam centrmezgla izvietošanā.</span><span class="sxs-lookup"><span data-stu-id="c268f-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="c268f-156">Ja nepieciešams, varat pievienot papildu loģiku, lai paziņojumus nosūtītu paralēli, izmantojot dažādus kanālus, un kontrolētu saņēmējus, balstoties uz notikuma datiem.</span><span class="sxs-lookup"><span data-stu-id="c268f-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="c268f-157">Sistēmā [Power Automate](https://preview.flow.microsoft.com) izveidojiet jaunu automatizētu mākoņa plūsmu plūsmas trigerim **Kad rodas biznesa notikums - Fin & Ops (Dynamics 365)**, kam seko **Parse JSON** un **Sūtīt e-pasta ziņojumu** darbības, kā parādīts šajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="c268f-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate automatizētā mākoņa plūsma":::

1. <span data-ttu-id="c268f-159">Darbības **Kad rodas biznesa notikums** laikā ir iespējams atrast vai ievadīt centrmezglu **Instance** kas seko **Kategorija** un pēc tam **Biznesa notikums** *Ziņojumu procesora ziņojums apstrādāts* kā parādīts šajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="c268f-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate darbība Kad notiek biznesa notikums":::

1. <span data-ttu-id="c268f-161">Darbībai **Parse JSON** ievadiet **Shēmu**, kas definē paplašinātos laukus.</span><span class="sxs-lookup"><span data-stu-id="c268f-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="c268f-162">Varat izmantot opciju *Lejupielādes shēma* lapā **Biznesa notikumu katalogs** Supply Chain Management vai arī sāciet, ielīmējot parauga shēmas tekstu.</span><span class="sxs-lookup"><span data-stu-id="c268f-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="c268f-163">Šis piemēra teksts ir parādīts pēc šī ilustrācijas.</span><span class="sxs-lookup"><span data-stu-id="c268f-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Parsēt JSON darbību":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="c268f-165">Darbībā **Sūtīt e-pasta zīņojumu** varat atlasīt atsevišķus laukus vai sākt, ielīmējot e-pasta pamatteksta piemēru laukā **Pamatteksts**.</span><span class="sxs-lookup"><span data-stu-id="c268f-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="c268f-166">Šis piemērs ir parādīts pēc šī ilustrācijas.</span><span class="sxs-lookup"><span data-stu-id="c268f-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate darbība Sūtīt e-pasta ziņojumu":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="c268f-168">Saglabājot biznesa notikumu, tas tiks automātiski aktivizēts un gatavs lietošanai kā Supply Chain Management daļa.</span><span class="sxs-lookup"><span data-stu-id="c268f-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
