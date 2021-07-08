---
title: Noliktavas pasūtījumi darba slodzes mākoņa un malas mēroga vienībām
description: Šajā tēmā ir sniegta informācija par noliktavas pasūtījuma iespēju, kas tiek izmantota kā daļa no noliktavas mēroga vienības darba noslodzes.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 080d45170c726cd0351ab344254aa36c1c56ba55
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271260"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="93f3c-103">Noliktavas pasūtījumi darba slodzes mākoņa un malas mēroga vienībām</span><span class="sxs-lookup"><span data-stu-id="93f3c-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]

> [!WARNING]
> <span data-ttu-id="93f3c-104">Ne visas biznesa funkcionalitātes tiek pilnībā atbalstītas publiskajā priekšskatījumā, kad darba slodzes mēroga vienības tiek izmantotas.</span><span class="sxs-lookup"><span data-stu-id="93f3c-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="93f3c-105">Izmantojot malas mēroga mērvienības, noteikti izmantojiet tikai tādus procesus, ko šī tēma skaidri apraksta kā atbalstītus.</span><span class="sxs-lookup"><span data-stu-id="93f3c-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="93f3c-106">Kas ir noliktavas pasūtījumi?</span><span class="sxs-lookup"><span data-stu-id="93f3c-106">What are warehouse orders?</span></span>

<span data-ttu-id="93f3c-107">*Noliktavas pasūtījumi* ir pasūtījuma veids, kas tika izveidots, lai atbalstītu pārkraušanas centra un mēroga vienību noliktavas izvietošanu.</span><span class="sxs-lookup"><span data-stu-id="93f3c-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="93f3c-108">Tie ļauj saņemt krājumus, veicot noliktavas darba noslodzi mēroga vienībā.</span><span class="sxs-lookup"><span data-stu-id="93f3c-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="93f3c-109">Ties pašlaik tiek lietoti tikai pirkšanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="93f3c-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="93f3c-110">Noliktavas pasūtījumi tiek izmantoti kā daļa no noliktavas pārvaldības apstrādes, piemēram, kad Warehouse Management mobile programma tiek izmantota, lai reģistrētu fiziskos rīcībā esošos krājumus ienākošā pirkšanas pasūtījuma apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="93f3c-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="93f3c-111">Noliktavas pasūtījumi tiek izveidoti kā daļa no *Pārsūtīšanas uz noliktavu* procesa, kas ir pieejams pirkšanas pasūtījumiem, kuros norādīta mēroga vienības noliktava un krājumi, kas ir iespējoti noliktavas pārvaldības procesu izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="93f3c-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93f3c-112">Noliktavas pasūtījumi ir pieejami tikai izvietošanās, kas izmanto noliktavas [pārvaldības darba noslodzes mākoņa un malas mēroga vienībām](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="93f3c-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="93f3c-113">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="93f3c-113">Create a warehouse order</span></span>

<span data-ttu-id="93f3c-114">Lai izveidotu pārdošanas pasūtījumu, veiciet sekojošās darbības.</span><span class="sxs-lookup"><span data-stu-id="93f3c-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="93f3c-115">Piesakieties Microsoft Dynamics 365 Supply Chain Management instancei, kas ir palaista centrmezglā.</span><span class="sxs-lookup"><span data-stu-id="93f3c-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="93f3c-116">(Jums jāuzsāk *Pārsūtīt uz noliktavu* process, kamēr esat pieteicies pārkraušanas punktā.)</span><span class="sxs-lookup"><span data-stu-id="93f3c-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="93f3c-117">Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="93f3c-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="93f3c-118">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="93f3c-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="93f3c-119">Lai skatītu saistītās noliktavas pasūtījuma rindas, atveriet atbilstošo pirkšanas pasūtījumu, atlasiet rindu sadaļā **Pirkšanas pasūtījuma rindas** un pēc tam rīkjoslā atlasiet **Noliktava \> Noliktavas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="93f3c-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="93f3c-120">Lai skatītu visas rindas, dodieties uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas**.</span><span class="sxs-lookup"><span data-stu-id="93f3c-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="93f3c-121">Jūs variet arī izraisīt *Palaišanas uz noliktavu* procesu no pakešuzdevuma, ejot uz **Noliktavas pārvaldība > Nodot uz noliktavu > Automātiska pirkšanas pasūtījumu izlaišana**.</span><span class="sxs-lookup"><span data-stu-id="93f3c-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="93f3c-122">Iestatot pakešuzdevumu, var atlasīt specifiskas pirkšanas pasūtījuma rindas, pamatojoties uz vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="93f3c-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="93f3c-123">Tipisks scenārijs būtu iestatīt periodisku pakešuzdevumu, kas atbrīvo visas apstiprinātās pirkšanas pasūtījuma rindas, kam paredzēts saņemt nākamo dienu.</span><span class="sxs-lookup"><span data-stu-id="93f3c-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="93f3c-124">Atgriešanas pasūtījuma atcelšana</span><span class="sxs-lookup"><span data-stu-id="93f3c-124">Cancel a warehouse order</span></span>

<span data-ttu-id="93f3c-125">Kā daļa no *Pārsūtīšanas uz noliktavu* procesa, pirkšanas pasūtījuma krājumu darbības ir saistītas ar noliktavas pasūtījumiem un bloķētas no atjaunināšanas ar pārkraušanas vietu.</span><span class="sxs-lookup"><span data-stu-id="93f3c-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="93f3c-126">Ja kļūdainā gadījumā izlaista noliktavai, vai arī ja ir kāds cits iemesls atsaukt noliktavas pasūtījuma rindu izveidošanu, varat pieprasīt atcelt noliktavas pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="93f3c-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="93f3c-127">Lai atceltu pārdošanas pasūtījumu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="93f3c-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="93f3c-128">Piesakieties Supply Chain Management instancei, kas ir palaista centrmezglā.</span><span class="sxs-lookup"><span data-stu-id="93f3c-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="93f3c-129">Dodieties uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas**.</span><span class="sxs-lookup"><span data-stu-id="93f3c-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="93f3c-130">Atlasiet saistīto rindu.</span><span class="sxs-lookup"><span data-stu-id="93f3c-130">Select the relevant line.</span></span>
1. <span data-ttu-id="93f3c-131">Darbību rūtī atlasiet **Atcelt noliktavas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="93f3c-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="93f3c-132">Pieprasījums atcelt rindas tiks noraidīts visām rindām, kas jau gaida atcelšanu vai kas aktīvi tiek apstrādātas noliktavā, kas palaiž tās darba slodzi mēroga vienībā.</span><span class="sxs-lookup"><span data-stu-id="93f3c-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="93f3c-133">Noliktavas pasūtījuma uzraudzīšana</span><span class="sxs-lookup"><span data-stu-id="93f3c-133">Monitor a warehouse order</span></span>

<span data-ttu-id="93f3c-134">**Noliktavas pasūtījuma rindu** skatā varat pārraudzīt ienākošās saņemšanas progresu, pārskatot kolonnas **Saņemamais daudzums** vērtības.</span><span class="sxs-lookup"><span data-stu-id="93f3c-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="93f3c-135">Lai skatītu detaļas, kas saistītas ar darbu, kas paveikts, izmantojot Warehouse Management mobile programmu, veiciet vienu no šīm darbībām.</span><span class="sxs-lookup"><span data-stu-id="93f3c-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="93f3c-136">Pārejiet uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas** un izmantojiet filtru, lai atrastu meklētās rindas.</span><span class="sxs-lookup"><span data-stu-id="93f3c-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="93f3c-137">Dodieties uz **Sagāde un avoti \> Pirkšanas pieprasījumi \> Visi pirkšanas pieprasījumi**, un atveriet attiecīgo pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="93f3c-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="93f3c-138">Sadaļā **Pirkšanas pasūtījuma rindas** atlasiet vienu vai vairākas rindas un pēc tam rīkjoslā atlasiet **Noliktava \> Noliktavas ieejas plūsmas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="93f3c-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
