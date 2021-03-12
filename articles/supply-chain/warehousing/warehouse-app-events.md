---
title: Noliktavas programmas notikumi
description: Šajā tēmā aprakstīta noliktavas programmas notikumu apstrāde, ko izmanto, lai apstrādātu noliktavas programmas notikumu ziņojumus kā daļu no pakešuzdevuma.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 66a5ca8a679563b59ca23992f7e0b4ee6fab470b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993808"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="3df08-103">Noliktavas lietojumprogrammas notikumu apstrāde</span><span class="sxs-lookup"><span data-stu-id="3df08-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3df08-104">Pakešuzdevumi, kas tiek izpildīti Supply Chain Management, var izmantot datus no noliktavas programmas izsniegtās notikumu apstrādes rindas, lai atbilstoši reaģētu uz signalizētajiem notikumiem.</span><span class="sxs-lookup"><span data-stu-id="3df08-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="3df08-105">Šis līdzeklis rindai pievieno svarīgus notikumus, atbildot uz noteiktiem darbību veidiem, ko veikuši darbinieki, izmantojot programmu.</span><span class="sxs-lookup"><span data-stu-id="3df08-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="3df08-106">Piemēram, izmantojot līdzekli **Izveidot un apstrādāt pārsūtīšanas pasūtījumus no noliktavas programmas**, pārsūtīšanas pasūtījuma virsraksts un rindas tiek izveidotas un atjauninātas aizmugursistēmā, kad sistēma palaiž pakešuzdevumu **Apstrādāt noliktavas programmas notikumus**.</span><span class="sxs-lookup"><span data-stu-id="3df08-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="3df08-107">Iespējot līdzekli Apstrādāt noliktavas programmas notikumus</span><span class="sxs-lookup"><span data-stu-id="3df08-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="3df08-108">Lai varētu izmantot šo līdzekli, tam vispirms jābūt iespējotam sistēmā.</span><span class="sxs-lookup"><span data-stu-id="3df08-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="3df08-109">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lapu, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="3df08-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="3df08-110">Līdzeklis Apstrādāt noliktavas programmas notikumus ir norādīts kā:</span><span class="sxs-lookup"><span data-stu-id="3df08-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="3df08-111">**Modulis** — Noliktavas vadība</span><span class="sxs-lookup"><span data-stu-id="3df08-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="3df08-112">**Līdzekļa nosaukums** — Apstrādāt noliktavas programmas notikumus</span><span class="sxs-lookup"><span data-stu-id="3df08-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="3df08-113">Iestatiet pakešuzdevumu, lai apstrādātu noliktavas programmas notikumus</span><span class="sxs-lookup"><span data-stu-id="3df08-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="3df08-114">Apstrādāt noliktavas programmas notikumus</span><span class="sxs-lookup"><span data-stu-id="3df08-114">Process warehouse app events</span></span>

<span data-ttu-id="3df08-115">Iestatiet ieplānotu pakešuzdevumu, lai apstrādātu noliktavas programmas notikumus pārsūtīšanas pasūtījumu izveidošanai un rindu atjauninājumiem.</span><span class="sxs-lookup"><span data-stu-id="3df08-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="3df08-116">Dodieties uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Apstrādāt noliktavas programmas notikumus**.</span><span class="sxs-lookup"><span data-stu-id="3df08-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="3df08-117">Tiek atvērts dialoglodziņš Apstrādāt noliktavas programmas notikumus.</span><span class="sxs-lookup"><span data-stu-id="3df08-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="3df08-118">Izvērsiet kopsavilkuma cilni **Palaist fonā** un iestatiet **Pakešapstrāde** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="3df08-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="3df08-119">Kopsavilkuma cilnē **Palaist fonā** atlasiet **Periodiskums**.</span><span class="sxs-lookup"><span data-stu-id="3df08-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="3df08-120">Atveras dialoglodziņš **Definēt periodiskumu**.</span><span class="sxs-lookup"><span data-stu-id="3df08-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="3df08-121">Iestatiet izpildes grafiku, kas nepieciešams jūsu biznesam.</span><span class="sxs-lookup"><span data-stu-id="3df08-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="3df08-122">Atlasiet **Labi** lai atgrieztos pie dialoglodziņa **Apstrādāt noliktavas programmas notikumus**.</span><span class="sxs-lookup"><span data-stu-id="3df08-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="3df08-123">Lai pievienotu pakešuzdevumu pakešuzdevumu rindai, atlasiet **Labi** dialoglodziņā **Apstrādāt noliktavas programmas notikumus**.</span><span class="sxs-lookup"><span data-stu-id="3df08-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="3df08-124">Vaicājumu noliktavas programmas notikumi</span><span class="sxs-lookup"><span data-stu-id="3df08-124">Query warehouse app events</span></span>

<span data-ttu-id="3df08-125">Varat skatīt notikumu rindu un notikumu ziņojumus, ko ģenerējusi noliktavas programma, dodoties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Mobilās ierīces žurnāli \> Noliktavas programmas notikumi**.</span><span class="sxs-lookup"><span data-stu-id="3df08-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="3df08-126">Standarta notikumu rindas process</span><span class="sxs-lookup"><span data-stu-id="3df08-126">The standard event queue process</span></span>

<span data-ttu-id="3df08-127">Noliktavas programmas notikumu rinda parasti tiek izmantota ar sekojošo aprakstīto plūsmu:</span><span class="sxs-lookup"><span data-stu-id="3df08-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="3df08-128">Notikums tiek pievienots rindai ar notikuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="3df08-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="3df08-129">Jaunajam ziņojumam sākotnēji ir notikuma stāvoklis **Gaidīšana**, kas nozīmē, ka pakešuzdevums **Apstrādāt noliktavas programmas notikumus** neturpināsies un neapstrādās ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="3df08-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="3df08-130">Tiklīdz ziņojuma stāvoklis tiek atjaunināts uz **Ievietots rindā**, pakešuzdevums **Apstrādāt noliktavas programmas** notikumus turpināsies un apstrādās notikumu.</span><span class="sxs-lookup"><span data-stu-id="3df08-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="3df08-131">Pakešuzdevums atjaunina notikuma stāvokļus uz vai nu **Pabeigts** vai **Nesekmīgs**, atkarībā no tā, vai pieprasītais process bija iespējams.</span><span class="sxs-lookup"><span data-stu-id="3df08-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="3df08-132">Kad visu saistīto notikuma ziņojumu statuss ir **Pabeigts**, notikums tiek dzēsts no rindas.</span><span class="sxs-lookup"><span data-stu-id="3df08-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="3df08-133">Detalizētu piemēru skatiet šeit: [Pārsūtīšanas pasūtījuma izveide no noliktavas programmas procesa](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="3df08-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="3df08-134">Notikumu kļūdu apstrāde</span><span class="sxs-lookup"><span data-stu-id="3df08-134">Handle event errors</span></span>

<span data-ttu-id="3df08-135">Kā daļu no noliktavas notikumu apstrādes, pieprasītā ziņojuma aktivitāte nevar saņemt procesus no pakešuzdevuma.</span><span class="sxs-lookup"><span data-stu-id="3df08-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="3df08-136">Šādā gadījumā notikuma ziņojums mainīsies uz **Nesekmīgs**.</span><span class="sxs-lookup"><span data-stu-id="3df08-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="3df08-137">Varat izmantot informāciju no **Pakešuzdevumu žurnāla**, lai uzzinātu iemeslu un veiktu nepieciešamās darbības, lai labotu problēmas.</span><span class="sxs-lookup"><span data-stu-id="3df08-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="3df08-138">Detalizētu piemēru skatiet šeit: [Pārsūtīšanas pasūtījuma izveide no noliktavas programmas](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="3df08-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="3df08-139">Lai atiestatītu nesekmīgu noliktavas programmas notikuma ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="3df08-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="3df08-140">Doties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Mobilās ierīces žurnāli \> Noliktavas programmas notikumi**.</span><span class="sxs-lookup"><span data-stu-id="3df08-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="3df08-141">Kopsavilkuma cilnē **Noliktavas programmas notikumu ziņojumi** atrodiet un atlasiet atbilstošu notikumu, kam parādīts statuss **Nesekmīgs** kolonnā **Notikuma stāvoklis**.</span><span class="sxs-lookup"><span data-stu-id="3df08-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="3df08-142">Atlasiet **Atiestatīt** rīkjoslā **Noliktavas programmas notikumu ziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="3df08-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="3df08-143">Turpiniet darbu, līdz visi atbilstošie ziņojumi ir atiestatīti.</span><span class="sxs-lookup"><span data-stu-id="3df08-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="3df08-144">Varat arī noņemt notikuma ziņojumu **Nesekmīgs**, izmantojot opciju **Dzēst** rīkjoslā **Noliktavas programmas notikumu ziņojumi**.</span><span class="sxs-lookup"><span data-stu-id="3df08-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>
