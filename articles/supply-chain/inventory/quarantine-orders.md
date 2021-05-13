---
title: Karantīnas pasūtījumi
description: Šajā tēmā ir aprakstīts, ka izmantot karantīnas pasūtījumus, lai bloķētu krājumus.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956186"
---
# <a name="quarantine-orders"></a><span data-ttu-id="5d575-103">Karantīnas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="5d575-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d575-104">Šajā tēmā ir aprakstīts, ka izmantot karantīnas pasūtījumus, lai bloķētu krājumus.</span><span class="sxs-lookup"><span data-stu-id="5d575-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="5d575-105">Karantīnas pasūtījumi ļauj bloķēt krājumus.</span><span class="sxs-lookup"><span data-stu-id="5d575-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="5d575-106">Piemēram, varat noteikt krājumu karantīnu kvalitātes kontroles iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="5d575-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="5d575-107">Krājumi, kam ir noteikta karantīna, tiek pārsūtīti uz karantīnas noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5d575-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="5d575-108">Ja izmantojat papildu noliktavas pārvaldības procesus (modulī Noliktavas pārvaldība), karantīnas pasūtījumu apstrāde tiek izmantota tikai atgriešanas pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="5d575-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="5d575-109">Rīcībā esošo krājumu karantīna</span><span class="sxs-lookup"><span data-stu-id="5d575-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="5d575-110">Kad novietojat krājumus karantīnā, varat manuāli izveidot karantīnas pasūtījumus vai arī iestatīt, lai sistēma ienākošās apstrādes laikā tos izveidotu automātiski.</span><span class="sxs-lookup"><span data-stu-id="5d575-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="5d575-111">Lai iestatītu sistēmu automātiskai karantīnas pasūtījumu ģenerēšanai, sekojiet šiem darbībam.</span><span class="sxs-lookup"><span data-stu-id="5d575-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="5d575-112">Dodieties uz **Krājumu vadība \> Iestatīšana \> Krājumi \> Krājumu modeļu grupas**.</span><span class="sxs-lookup"><span data-stu-id="5d575-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="5d575-113">Atlasiet atbilstošo modeļu grupu saraksta rūtī vai izveidojiet jaunu modeļu grupu.</span><span class="sxs-lookup"><span data-stu-id="5d575-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="5d575-114">Kopsavilkuma cilnē **Krājumu politikas** atzīmējiet izvēles rūtiņu **Karantīnas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="5d575-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="5d575-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5d575-115">Close the page.</span></span>
1. <span data-ttu-id="5d575-116">Jums jānorāda noklusējuma karantīnas noliktava laukā **Karantīnas noliktava** saņemošajām noliktavām.</span><span class="sxs-lookup"><span data-stu-id="5d575-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="5d575-117">Ja krājums, kas noliktavā reģistrēts kā saņemts, pieder modeļu grupai, kurai atzīmēta izvēles rūtiņa **Karantīnas pārvaldība**, sistēma tai ģenerē karantīnas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="5d575-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="5d575-118">Karantīnas pasūtījums liek darbiniekiem pārvietot krājumu uz karantīnas noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5d575-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="5d575-119">Kad jūs manuāli izveidojat karantīnas pasūtījumus lapā **Karantīnas pasūtījumi**, krājumu nav nepieciešams iestatīt karantīnas pārraudzībai saistītajā krājuma modeļa grupā.</span><span class="sxs-lookup"><span data-stu-id="5d575-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="5d575-120">Šim procesam ir jānorāda rīcībā esošais krājums, kas jānovieto karantīnā, un karantīnas noliktava, kura jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="5d575-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="5d575-121">Lai palīdzētu plānot procesu, varat izmantot karantīnas pasūtījuma statusus.</span><span class="sxs-lookup"><span data-stu-id="5d575-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="5d575-122">Karantīnas pasūtījumu statusi</span><span class="sxs-lookup"><span data-stu-id="5d575-122">Quarantine order statuses</span></span>

<span data-ttu-id="5d575-123">Karantīnas pasūtījumiem var būt šāds statuss:</span><span class="sxs-lookup"><span data-stu-id="5d575-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="5d575-124">Izveidota</span><span class="sxs-lookup"><span data-stu-id="5d575-124">Created</span></span>
- <span data-ttu-id="5d575-125">Uzsākts</span><span class="sxs-lookup"><span data-stu-id="5d575-125">Started</span></span>
- <span data-ttu-id="5d575-126">Ziņots kā pabeigts</span><span class="sxs-lookup"><span data-stu-id="5d575-126">Reported as finished</span></span>
- <span data-ttu-id="5d575-127">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="5d575-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="5d575-128">Izveidota</span><span class="sxs-lookup"><span data-stu-id="5d575-128">Created</span></span>

<span data-ttu-id="5d575-129">Ja karantīnas pasūtījums ir izveidots manuāli, bet krājums vēl nav novietots karantīnas noliktavā, karantīnas pasūtījumam ir statuss **Izveidots**.</span><span class="sxs-lookup"><span data-stu-id="5d575-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="5d575-130">Tiek ģenerētas divas krājumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="5d575-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="5d575-131">Viena transakcija ir izejas plūsmas transakcija, kurai var būt statuss **Pasūtīts**, **Rezervēts fiziski** vai **Izdots**.</span><span class="sxs-lookup"><span data-stu-id="5d575-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="5d575-132">Otrā transakcija ir ieejas plūsmas transakcija, kurai karantīnas noliktavā var būt statuss **Pasūtīts** vai **Reģistrēts**.</span><span class="sxs-lookup"><span data-stu-id="5d575-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="5d575-133">Jūs varat rezervēt, izdot un reģistrēt krājumu atjauninājumus, izmantojot parastos procesus.</span><span class="sxs-lookup"><span data-stu-id="5d575-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="5d575-134">Uzsākts</span><span class="sxs-lookup"><span data-stu-id="5d575-134">Started</span></span>

<span data-ttu-id="5d575-135">Kad karantīnas pasūtījumam ir statuss **Sākts**, krājumi tiek pārsūtīti no parastās noliktavas uz karantīnas noliktavu, un tiek ģenerētas divas krājumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="5d575-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="5d575-136">Vienai transakcijai ir statuss **Atskaitīts** un otrai transakcijai ir statuss **Saņemts**.</span><span class="sxs-lookup"><span data-stu-id="5d575-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="5d575-137">Vienlaicīgi tiek arī izveidotas divas krājumu transakcijas, lai izpildītu atgriešanas pārsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="5d575-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="5d575-138">Šīm transakcijām nav datuma.</span><span class="sxs-lookup"><span data-stu-id="5d575-138">These transactions aren't dated.</span></span> <span data-ttu-id="5d575-139">Vienai transakcijai ir statuss **Rezervēts fiziski** un otrai transakcijai ir statuss **Pasūtīts**.</span><span class="sxs-lookup"><span data-stu-id="5d575-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="5d575-140">Ziņots kā pabeigts</span><span class="sxs-lookup"><span data-stu-id="5d575-140">Reported as finished</span></span>

<span data-ttu-id="5d575-141">Lai pabeigtu sākto karantīnas pasūtījumu, atveriet pasūtījumu un darbību rūtī atlasiet **Ziņot, ka ir pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="5d575-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="5d575-142">Krājums tiek atbrīvots no karantīnas, bet vēl netiek pārvietots atpakaļ uz parasto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5d575-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="5d575-143">Kustību atpakaļ uz parasto noliktavu var apstrādāt, izmantojot krājumu saņemšanas žurnālu, ko var inicializēt pabeigšanas reģistrēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="5d575-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="5d575-144">Beidzās</span><span class="sxs-lookup"><span data-stu-id="5d575-144">Ended</span></span>

<span data-ttu-id="5d575-145">Kad karantīnas pasūtījums ir pabeigts, krājums tiek pārvietots no karantīnas noliktavas atpakaļ uz parasto noliktavu.</span><span class="sxs-lookup"><span data-stu-id="5d575-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="5d575-146">Krājuma transakcijas statuss karantīnas noliktavā tiek iestatīts uz *Pārdots* un parastajā noliktavā — uz *Nopirkts*.</span><span class="sxs-lookup"><span data-stu-id="5d575-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="5d575-147">Karantīnas pasūtījuma brāķis</span><span class="sxs-lookup"><span data-stu-id="5d575-147">Quarantine order scrap</span></span>

<span data-ttu-id="5d575-148">Karantīnas pasūtījuma procesa ietvaros ir iespējams norakstīt krājumu.</span><span class="sxs-lookup"><span data-stu-id="5d575-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="5d575-149">Apstrādājot brāķi, krājuma statuss ir iestatīts kā *Pārdots*, izmantojot izdošanas transakciju no karantīnas noliktavas.</span><span class="sxs-lookup"><span data-stu-id="5d575-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d575-150">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5d575-150">Additional resources</span></span>

- [<span data-ttu-id="5d575-151">Krājumu bloķēšana</span><span class="sxs-lookup"><span data-stu-id="5d575-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
