---
title: Noliktavas pasūtījumi darba slodzes mākoņa un malas mēroga vienībām
description: Šajā tēmā ir sniegta informācija par noliktavas pasūtījuma iespēju, kas tiek izmantota kā daļa no noliktavas mēroga vienības darba noslodzes.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105718"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="548d8-103">Noliktavas pasūtījumi darba slodzes mākoņa un malas mēroga vienībām</span><span class="sxs-lookup"><span data-stu-id="548d8-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="548d8-104">Ne visas biznesa funkcionalitātes tiek pilnībā atbalstītas publiskajā priekšskatījumā, kad darba slodzes mēroga vienības tiek izmantotas.</span><span class="sxs-lookup"><span data-stu-id="548d8-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="548d8-105">Izmantojot malas mēroga mērvienības, noteikti izmantojiet tikai tādus procesus, ko šī tēma skaidri apraksta kā atbalstītus.</span><span class="sxs-lookup"><span data-stu-id="548d8-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="548d8-106">Kas ir noliktavas pasūtījumi?</span><span class="sxs-lookup"><span data-stu-id="548d8-106">What are warehouse orders?</span></span>

<span data-ttu-id="548d8-107">*Noliktavas pasūtījumi* ir pasūtījuma veids, kas tika izveidots, lai atbalstītu pārkraušanas centra un mēroga vienību noliktavas izvietošanu.</span><span class="sxs-lookup"><span data-stu-id="548d8-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="548d8-108">Tie ļauj saņemt krājumus, veicot noliktavas darba noslodzi mēroga vienībā.</span><span class="sxs-lookup"><span data-stu-id="548d8-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="548d8-109">Ties pašlaik tiek lietoti tikai pirkšanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="548d8-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="548d8-110">Noliktavas pasūtījumi tiek izmantoti kā daļa no noliktavas pārvaldības apstrādes, piemēram, kad noliktavas programma tiek izmantota, lai reģistrētu fiziskos rīcībā esošos krājumus ienākošā pirkšanas pasūtījuma apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="548d8-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="548d8-111">Noliktavas pasūtījumi tiek izveidoti kā daļa no *Pārsūtīšanas uz noliktavu* procesa, kas ir pieejams pirkšanas pasūtījumiem, kuros norādīta mēroga vienības noliktava un krājumi, kas ir iespējoti noliktavas pārvaldības procesu izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="548d8-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="548d8-112">Noliktavas pasūtījumi ir pieejami tikai izvietošanās, kas izmanto noliktavas [pārvaldības darba noslodzes mākoņa un malas mēroga vienībām](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="548d8-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="548d8-113">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="548d8-113">Create a warehouse order</span></span>

<span data-ttu-id="548d8-114">Lai izveidotu pārdošanas pasūtījumu, veiciet sekojošās darbības.</span><span class="sxs-lookup"><span data-stu-id="548d8-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="548d8-115">Piesakieties Microsoft Dynamics 365 Supply Chain Management instancei, kas ir palaista centrmezglā.</span><span class="sxs-lookup"><span data-stu-id="548d8-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="548d8-116">(Jums jāuzsāk *Pārsūtīt uz noliktavu* process, kamēr esat pieteicies pārkraušanas punktā.)</span><span class="sxs-lookup"><span data-stu-id="548d8-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="548d8-117">Dodieties uz **Sagāde un avoti \> Pirkšanas pasūtījumi \> Visi pirkšanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="548d8-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="548d8-118">Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="548d8-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="548d8-119">Lai skatītu saistītās noliktavas pasūtījuma rindas, atveriet atbilstošo pirkšanas pasūtījumu, atlasiet rindu sadaļā **Pirkšanas pasūtījuma rindas** un pēc tam rīkjoslā atlasiet **Noliktava \> Noliktavas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="548d8-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="548d8-120">Lai skatītu visas rindas, dodieties uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas**.</span><span class="sxs-lookup"><span data-stu-id="548d8-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="548d8-121">Atgriešanas pasūtījuma atcelšana</span><span class="sxs-lookup"><span data-stu-id="548d8-121">Cancel a warehouse order</span></span>

<span data-ttu-id="548d8-122">Kā daļa no *Pārsūtīšanas uz noliktavu* procesa, pirkšanas pasūtījuma krājumu darbības ir saistītas ar noliktavas pasūtījumiem un bloķētas no atjaunināšanas ar pārkraušanas vietu.</span><span class="sxs-lookup"><span data-stu-id="548d8-122">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="548d8-123">Ja kļūdainā gadījumā izlaista noliktavai, vai arī ja ir kāds cits iemesls atsaukt noliktavas pasūtījuma rindu izveidošanu, varat pieprasīt atcelt noliktavas pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="548d8-123">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="548d8-124">Lai atceltu pārdošanas pasūtījumu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="548d8-124">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="548d8-125">Piesakieties Supply Chain Management instancei, kas ir palaista centrmezglā.</span><span class="sxs-lookup"><span data-stu-id="548d8-125">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="548d8-126">Dodieties uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas**.</span><span class="sxs-lookup"><span data-stu-id="548d8-126">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="548d8-127">Atlasiet saistīto rindu.</span><span class="sxs-lookup"><span data-stu-id="548d8-127">Select the relevant line.</span></span>
1. <span data-ttu-id="548d8-128">Darbību rūtī atlasiet **Atcelt noliktavas pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="548d8-128">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="548d8-129">Pieprasījums atcelt rindas tiks noraidīts visām rindām, kas jau gaida atcelšanu vai kas aktīvi tiek apstrādātas noliktavā, kas palaiž tās darba slodzi mēroga vienībā.</span><span class="sxs-lookup"><span data-stu-id="548d8-129">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="548d8-130">Noliktavas pasūtījuma uzraudzīšana</span><span class="sxs-lookup"><span data-stu-id="548d8-130">Monitor a warehouse order</span></span>

<span data-ttu-id="548d8-131">**Noliktavas pasūtījuma rindu** skatā varat pārraudzīt ienākošās saņemšanas progresu, pārskatot kolonnas **Saņemamais daudzums** vērtības.</span><span class="sxs-lookup"><span data-stu-id="548d8-131">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="548d8-132">Lai skatītu detaļas, kas saistītas ar darbu, kas paveikts, izmantojot noliktavas programmu, veiciet vienu no šīm darbībām.</span><span class="sxs-lookup"><span data-stu-id="548d8-132">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="548d8-133">Pārejiet uz sadaļu **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Noliktavas pasūtījumu rindas** un izmantojiet filtru, lai atrastu meklētās rindas.</span><span class="sxs-lookup"><span data-stu-id="548d8-133">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="548d8-134">Dodieties uz **Sagāde un avoti \> Pirkšanas pieprasījumi \> Visi pirkšanas pieprasījumi**, un atveriet attiecīgo pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="548d8-134">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="548d8-135">Sadaļā **Pirkšanas pasūtījuma rindas** atlasiet vienu vai vairākas rindas un pēc tam rīkjoslā atlasiet **Noliktava \> Noliktavas ieejas plūsmas ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="548d8-135">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>
