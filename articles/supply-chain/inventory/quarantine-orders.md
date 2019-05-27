---
title: Karantīnas pasūtījumi
description: Šajā tēmā ir aprakstīts, kā karantīnas pasūtījumi tiek izmantoti, lai bloķētu krājumus.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 523e51c705d76b6e8624887292395f8f239bcb65
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570475"
---
# <a name="quarantine-orders"></a><span data-ttu-id="8be30-103">Karantīnas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="8be30-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8be30-104">Šajā tēmā ir aprakstīts, kā karantīnas pasūtījumi tiek izmantoti, lai bloķētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="8be30-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="8be30-105">Karantīnas pasūtījumus var izmantot, lai bloķētu krājumu.</span><span class="sxs-lookup"><span data-stu-id="8be30-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="8be30-106">Piemēram, varat noteikt krājumu karantīnu kvalitātes kontroles iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="8be30-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="8be30-107">Krājumi, kam ir noteikta karantīna, tiek pārsūtīti uz karantīnas noliktavu.</span><span class="sxs-lookup"><span data-stu-id="8be30-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="8be30-108">**Piezīme.** Ja izmantojat papildu noliktavas pārvaldības procesus (modulī Noliktavas pārvaldība), karantīnas pasūtījumu apstrāde tiek izmantota tikai atgriešanas pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="8be30-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="8be30-109">Rīcībā esošo krājumu karantīna</span><span class="sxs-lookup"><span data-stu-id="8be30-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="8be30-110">Kad novietojat krājumus karantīnā, varat izveidot karantīnas pasūtījumus manuāli vai arī iestatīt, lai sistēma ienākošās apstrādes laikā automātiski izveidotu karantīnas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="8be30-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="8be30-111">Lai automātiski izveidotu karantīnas pasūtījumus, atlasiet opciju **Karantīnas pārraudzība** lapas **Krājumu modeļu grupas** cilnē **Krājumu politikas**.</span><span class="sxs-lookup"><span data-stu-id="8be30-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="8be30-112">Jums jānorāda arī noklusējuma karantīnas noliktava laukā **Karantīnas noliktava** saņemošajām noliktavām.</span><span class="sxs-lookup"><span data-stu-id="8be30-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="8be30-113">Ja fiziski rīcībā esošie krājumi tiek reģistrēti pirkšanas pasūtījumā vai ražošanas pasūtījumā, karantīnā novietotie krājumi tiek automātiski pārvietoti uz karantīnas noliktavu programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8be30-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="8be30-114">Šī kustība notiek tāpēc, ka karantīnas pasūtījuma statuss tiek mainīts uz **Sākts**.</span><span class="sxs-lookup"><span data-stu-id="8be30-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="8be30-115">Kad jūs izveidojat karantīnas pasūtījumus manuāli, krājumu nav nepieciešams iestatīt karantīnas pārraudzībai saistītajā krājuma modeļa grupā.</span><span class="sxs-lookup"><span data-stu-id="8be30-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="8be30-116">Šim procesam ir jānorāda rīcībā esošais krājums, kas jānovieto karantīnā, un karantīnas noliktava, kura jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="8be30-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="8be30-117">Lai palīdzētu plānot procesu, varat izmantot karantīnas pasūtījuma statusus.</span><span class="sxs-lookup"><span data-stu-id="8be30-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="8be30-118">Karantīnas pasūtījumu statusi</span><span class="sxs-lookup"><span data-stu-id="8be30-118">Quarantine order statuses</span></span>
<span data-ttu-id="8be30-119">Karantīnas pasūtījumiem var būt šāds statuss:</span><span class="sxs-lookup"><span data-stu-id="8be30-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="8be30-120">Izveidota</span><span class="sxs-lookup"><span data-stu-id="8be30-120">Created</span></span>
-   <span data-ttu-id="8be30-121">Uzsākts</span><span class="sxs-lookup"><span data-stu-id="8be30-121">Started</span></span>
-   <span data-ttu-id="8be30-122">Ziņots kā pabeigts</span><span class="sxs-lookup"><span data-stu-id="8be30-122">Reported as finished</span></span>
-   <span data-ttu-id="8be30-123">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="8be30-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="8be30-124">Izveidota</span><span class="sxs-lookup"><span data-stu-id="8be30-124">Created</span></span>

<span data-ttu-id="8be30-125">Ja karantīnas pasūtījums ir izveidots manuāli, bet krājums vēl nav novietots karantīnas noliktavā, karantīnas pasūtījumam ir statuss **Izveidots**.</span><span class="sxs-lookup"><span data-stu-id="8be30-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="8be30-126">Tiek ģenerētas divas krājumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="8be30-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="8be30-127">Viena transakcija ir izejas plūsmas transakcija, kurai var būt statuss **Pasūtīts**, **Rezervēts fiziski** vai **Izdots**.</span><span class="sxs-lookup"><span data-stu-id="8be30-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="8be30-128">Otrā transakcija ir ieejas plūsmas transakcija, kurai karantīnas noliktavā var būt statuss **Pasūtīts** vai **Reģistrēts**.</span><span class="sxs-lookup"><span data-stu-id="8be30-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="8be30-129">Jūs varat rezervēt, izdot un reģistrēt krājumu atjauninājumus, izmantojot parastos procesus.</span><span class="sxs-lookup"><span data-stu-id="8be30-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="8be30-130">Uzsākts</span><span class="sxs-lookup"><span data-stu-id="8be30-130">Started</span></span>

<span data-ttu-id="8be30-131">Kad karantīnas pasūtījumam ir statuss **Sākts**, krājumi tiek pārsūtīti no parastās noliktavas uz karantīnas noliktavu, un tiek ģenerētas divas krājumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="8be30-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="8be30-132">Vienai transakcijai ir statuss **Atskaitīts** un otrai transakcijai ir statuss **Saņemts**.</span><span class="sxs-lookup"><span data-stu-id="8be30-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="8be30-133">Vienlaicīgi tiek arī izveidotas divas krājumu transakcijas, lai izpildītu atgriešanas pārsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="8be30-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="8be30-134">Šīm transakcijām nav datuma.</span><span class="sxs-lookup"><span data-stu-id="8be30-134">These transactions aren't dated.</span></span> <span data-ttu-id="8be30-135">Vienai transakcijai ir statuss **Rezervēts fiziski** un otrai transakcijai ir statuss **Pasūtīts**.</span><span class="sxs-lookup"><span data-stu-id="8be30-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="8be30-136">Ziņots kā pabeigts</span><span class="sxs-lookup"><span data-stu-id="8be30-136">Reported as finished</span></span>

<span data-ttu-id="8be30-137">Noklikšķinot uz **Reģistrēt pabeigšanu**, sāktais karantīnas pasūtījums tiek reģistrēts kā pabeigts.</span><span class="sxs-lookup"><span data-stu-id="8be30-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="8be30-138">Krājums tiek atbrīvots no karantīnas, bet vēl netiek pārvietots atpakaļ uz parasto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="8be30-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="8be30-139">Kustību atpakaļ uz parasto noliktavu var apstrādāt, izmantojot krājumu saņemšanas žurnālu, ko var inicializēt pabeigšanas reģistrēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="8be30-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="8be30-140">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="8be30-140">Ended</span></span>

<span data-ttu-id="8be30-141">Kad karantīnas pasūtījums ir pabeigts, krājums tiek pārvietots no karantīnas noliktavas atpakaļ uz parasto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="8be30-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="8be30-142">Krājuma transakcijas statuss karantīnas noliktavā tiek iestatīts uz **Pārdots** un parastajā noliktavā — uz **Nopirkts**.</span><span class="sxs-lookup"><span data-stu-id="8be30-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="8be30-143">Karantīnas pasūtījuma brāķis</span><span class="sxs-lookup"><span data-stu-id="8be30-143">Quarantine order scrap</span></span>
<span data-ttu-id="8be30-144">Karantīnas pasūtījuma procesa ietvaros ir iespējams norakstīt krājumu.</span><span class="sxs-lookup"><span data-stu-id="8be30-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="8be30-145">Apstrādājot brāķi, krājuma statuss tiks iestatīts kā **Pārdots**, izmantojot izdošanas transakciju no karantīnas noliktavas.</span><span class="sxs-lookup"><span data-stu-id="8be30-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="8be30-146">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8be30-146">Additional resources</span></span>
--------

[<span data-ttu-id="8be30-147">Krājumu bloķēšana</span><span class="sxs-lookup"><span data-stu-id="8be30-147">Inventory blocking</span></span>](inventory-blocking.md)
