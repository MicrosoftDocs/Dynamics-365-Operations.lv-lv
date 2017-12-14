---
title: "Izejošais process"
description: "Šajā tēmā ir sniegts apskats par izejošo procesu modulī Krājumu vadība."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: f2cae64263769b5168d2bb9614d6388b42e23b49
ms.contentlocale: lv-lv
ms.lasthandoff: 12/14/2017

---

# <a name="outbound-process"></a><span data-ttu-id="41bb6-103">Izejošais process</span><span class="sxs-lookup"><span data-stu-id="41bb6-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="41bb6-104">Šajā tēmā ir sniegts apskats par izejošo procesu modulī Krājumu vadība.</span><span class="sxs-lookup"><span data-stu-id="41bb6-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="41bb6-105">Izdošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="41bb6-105">Output orders</span></span>

<span data-ttu-id="41bb6-106">Izdošanas pasūtījumi tiek lietoti, lai pārdošanas pasūtījumu rindas un pārsūtīšanas pasūtījumu rindas saistītu ar izejošajiem izdošanas procesiem, kuros tiek izmantoti izdošanas saraksti.</span><span class="sxs-lookup"><span data-stu-id="41bb6-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="41bb6-107">Kad izdošanas saraksti tiek ģenerēti no pārdošanas pasūtījumiem vai pārsūtīšanas pasūtījumiem, tad izdošanas pasūtījumi un sūtījumi tiek izveidoti automātiski.</span><span class="sxs-lookup"><span data-stu-id="41bb6-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="41bb6-108">Izdošanas sarakstam ar sūtījumu ir relācija “viens pret vienu”.</span><span class="sxs-lookup"><span data-stu-id="41bb6-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="41bb6-109">Pārsūtīšanas pasūtījuma sūtījumu vai pārdošanas pasūtījuma pavadzīmi var apstrādāt no sūtījuma.</span><span class="sxs-lookup"><span data-stu-id="41bb6-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="41bb6-110">Nākamajā diagrammā ir parādīts apskats par izejošo pasūtījumu apstrādi.</span><span class="sxs-lookup"><span data-stu-id="41bb6-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="41bb6-111">[![Apskats par izejošo pasūtījumu apstrādi](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="41bb6-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="41bb6-112">Varat iestatīt izejošās kārtulas, lai definētu, kā programmai ir jāapstrādā izejošais process.</span><span class="sxs-lookup"><span data-stu-id="41bb6-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="41bb6-113">Šīs kārtulas varat izmantot, lai kontrolētu nosūtīšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="41bb6-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="41bb6-114">Šīs kārtulas jūs it īpaši varat izmantot, lai kontrolētu, kurā nosūtīšanas procesa posmā var veikt nosūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="41bb6-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="41bb6-115">Nākamie iestatījumi nosaka veidu, kā tiek apstrādāti izejošie procesi.</span><span class="sxs-lookup"><span data-stu-id="41bb6-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="41bb6-116">Izdošanas maršruta statuss pārdošanas un pārsūtīšanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="41bb6-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="41bb6-117">Dodieties uz **Debitoru parādi** \> **Iestatījumi** \> **Debitoru parādu parametri** un pēc tam cilnē **Atjauninājumi** atlasiet kādu vērtību laukā **Izdošanas maršruta statuss**.</span><span class="sxs-lookup"><span data-stu-id="41bb6-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="41bb6-118">[![Izdošanas maršruta statusa lauks pārdošanas pasūtījumiem](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="41bb6-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="41bb6-119">Ja lauks **Izdošanas maršruta statuss** ir iestatīts uz **Pabeigts**, tad šis izdošanas process tiek automātiski izpildīts kā daļa no izdošanas sarakstu ģenerēšanas procedūras.</span><span class="sxs-lookup"><span data-stu-id="41bb6-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="41bb6-120">Ja šis lauks ir iestatīts uz **Aktivizēts**, tad izdošanas saraksta rindas ir jāatjaunina manuāli.</span><span class="sxs-lookup"><span data-stu-id="41bb6-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="41bb6-121">Tāda pati iestatīšana attiecas uz pārsūtīšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="41bb6-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="41bb6-122">Dodieties uz **Krājumu vadība** \> **Iestatījumi** \> **Krājumu un noliktavas vadības parametri** un pēc tam cilnē **Transports** atlasiet kādu vērtību laukā **Izdošanas maršruta statuss**.</span><span class="sxs-lookup"><span data-stu-id="41bb6-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="41bb6-123">[![Izdošanas maršruta statusa lauks pārsūtīšanas pasūtījumiem](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="41bb6-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="41bb6-124">Beigt izdošanas krājumu pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="41bb6-124">End output inventory orders</span></span>

<span data-ttu-id="41bb6-125">Dodieties uz **Krājumu vadība** \> **Iestatījumi** \> **Krājumu un noliktavas vadības parametri** un pēc tam cilnē **Vispārīgi** iestatiet opciju **Beigt izdošanas krājumu pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="41bb6-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="41bb6-126">[![Opcija Beigt izdošanas krājumu pasūtījumu](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="41bb6-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="41bb6-127">Ja noliktavas darbinieks samazina izdošanas sarakstā ietvertos daudzumus, no sūtījuma tiek noņemti attiecīgie krājumu pasūtījumā ietvertie daudzumi.</span><span class="sxs-lookup"><span data-stu-id="41bb6-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="41bb6-128">Ja noteiktā brīdī tiek atjaunināts izdošanas saraksts un ir iestata opcijas **Beigt krājumu izdošanas pasūtījumu** vērtība **Jā**, atlikušie daudzumi tiek ietverti atpakaļ pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="41bb6-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="41bb6-129">Ja ir iestatīta opcijas **Beigt krājumu izdošanas pasūtījumu** vērtība **Nē**, atlikušie daudzumi tiek saglabāti kā atvērta izdošanas pasūtījuma daudzums un tie ir jāpievieno jaunam izdošanas sarakstam, izmantojot funkcionalitāti **Atvērt izdošanas pasūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="41bb6-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="41bb6-130">[![Komanda Atvērt izdošanas pasūtījumus izvēlnē Funkcijas](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="41bb6-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="41bb6-131">[![Izvēlne Funkcijas lapā Atvērt izdošanas pasūtījumus](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="41bb6-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="41bb6-132">Samazināt daudzumu</span><span class="sxs-lookup"><span data-stu-id="41bb6-132">Reduce quantity</span></span>

<span data-ttu-id="41bb6-133">Trešais parametrs, ko varat izmantot kā daļu no izdošanas sarakstu ģenerēšanas procesa, ir parametrs **Samazināt daudzumu**.</span><span class="sxs-lookup"><span data-stu-id="41bb6-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="41bb6-134">Šī parametra iestatījums darbojas kopā ar iestatījumu **Rezervācija**, kas kā daļu no pārvietošanas uz noliktavu izsauc rezervēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="41bb6-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="41bb6-135">[![Parametrs Samazināt daudzumu](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="41bb6-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="41bb6-136">Izejošā procesa piemērs pārdošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="41bb6-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="41bb6-137">Šajā piemērā pastāv pārdošanas pasūtījums par diviem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="41bb6-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="41bb6-138">Izdošanas saraksta ģenerēšanas laikā jūs atlasāt parametru **Samazināt daudzumu**.</span><span class="sxs-lookup"><span data-stu-id="41bb6-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="41bb6-139">Tāpēc izlaišana un izdošanas rindu izveidošana notiek tikai pieejamajiem rīcībā esošajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="41bb6-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="41bb6-140">Izdošanas ir jāziņo, izmantojot reģistrācijas procesu izdošanas sarakstiem (**Izdošanas maršruta statuss** = **Aktivizēts**).</span><span class="sxs-lookup"><span data-stu-id="41bb6-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="41bb6-141">Krājumi, kas vēl nav rezervēti, tiek rezervēti izdošanas saraksta ģenerēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="41bb6-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="41bb6-142">Nepieejamos krājumus var noņemt no pārdošanas pasūtījuma vai pārvietot uz noliktavu vēlākai izejošajai apstrādei, kad krājumi ir pieejami izdošanai.</span><span class="sxs-lookup"><span data-stu-id="41bb6-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="41bb6-143">[![Atjaunināt izdošanas sarakstu](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="41bb6-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="41bb6-144">Tiklīdz visas izdošanas rindas lapā **Izdošanas saraksta reģistrācija** ir izdotas, saistītais sūtījums tiek pabeigts.</span><span class="sxs-lookup"><span data-stu-id="41bb6-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="41bb6-145">Pēc tam var uzsākt procesu pārdošanas pasūtījumu pavadzīmēm, pamatojoties uz izdotajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="41bb6-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="41bb6-146">[![Atjaunināt izejošos sūtījumus](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="41bb6-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

