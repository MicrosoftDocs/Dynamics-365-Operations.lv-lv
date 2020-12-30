---
title: Starpuzņēmumu pasūtījumu filtrēšana, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju
description: Šajā tēmā tiek aprakstīts, kā filtrēt starpuzņēmumu pasūtījumus, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701037"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="b8a9f-103">Starpuzņēmumu pasūtījumu filtrēšana, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju</span><span class="sxs-lookup"><span data-stu-id="b8a9f-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8a9f-104">Varat filtrēt starpuzņēmumu pasūtījumus, lai novērstu elementu **Pasūtījumi** un **Pasūtījumu rindas** sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="b8a9f-105">Dažos gadījumos starpuzņēmumu pasūtījuma informācija nav nepieciešama klientu iesaistīšanās programmā.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="b8a9f-106">Katrs standarta Common Data Service elements tiek paplašināts ar atsaucēm uz lauku **IntercompanyOrder**, un duālās rakstīšanas kartes tiek modificētas, lai atsauktos uz papildu laukiem filtros.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="b8a9f-107">Rezultāts ir tāds, ka starpuzņēmumu pasūtījumi vairs netiek sinhronizēti.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="b8a9f-108">Šis process palīdz izvairīties no nevajadzīgiem datiem Customer Engagement programmā.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="b8a9f-109">Pievienojiet atsauci uz **IntercompanyOrder** kā **CDS pārdošanas pasūtījumu virsraksti**.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="b8a9f-110">Tā tiek aizpildīta tikai starpuzņēmumu pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="b8a9f-111">Lauks **IntercompanyOrder** ir pieejams elementā **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Kartes iestatīšana mērķim, SalesOrderHeader":::
    
2. <span data-ttu-id="b8a9f-113">Kad elements **CDS pārdošanas pasūtījumu virsraksti** ir paplašināts, lauks **IntercompanyOrder** ir pieejams kartē.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="b8a9f-114">Lietojiet filtru ar `INTERCOMPANYORDER == ""` kā vaicājuma virkni.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Pārdošanas pasūtījumu virsraksti, vaicājuma rediģēšana":::

3. <span data-ttu-id="b8a9f-116">Pievienojiet atsauci uz **IntercompanyInventTransId** kā **CDS pārdošanas pasūtījumu rindas**.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="b8a9f-117">Tā tiek aizpildīta tikai starpuzņēmumu pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="b8a9f-118">Lauks **InterCompanyInventTransID** ir pieejams elementā **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Kartes iestatīšana mērķim, SalesOrderLine":::

4. <span data-ttu-id="b8a9f-120">Kad elements **CDS pārdošanas pasūtījumu rindas** ir paplašināts, lauks **IntercompanyInventTransId** ir pieejams kartē.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="b8a9f-121">Lietojiet filtru ar `INTERCOMPANYINVENTTRANSID == ""` kā vaicājuma virkni.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Pārdošanas pasūtījuma rindas, vaicājuma rediģēšana":::

5. <span data-ttu-id="b8a9f-123">Paplašiniet elementu **Pārdošanas rēķina virsraksta V2** un **Pārdošanas rēķina rindas V2** tādā pašā veidā, kā jūs paplašinājāt Common Data Service elementus 1. un 2. darbībā.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="b8a9f-124">Pēc tam pievienojiet filtra vaicājumus.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-124">Then add the filter queries.</span></span> <span data-ttu-id="b8a9f-125">Filtra virkne elementam **Pārdošanas rēķina virsraksta V2** ir `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="b8a9f-126">Filtra virkne elementam **Pārdošanas rēķina rindu V2** ir `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Kartes iestatīšana mērķim, pāŗdošanas rēķina virsraksti":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Pārdošanas rēķinu virsraksti, vaicājuma rediģēšana":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Pārdošanas rēķinu rindas, vaicājuma rediģēšana":::

6. <span data-ttu-id="b8a9f-130">Elementam **Piedāvājumi** nav starpuzņēmumu attiecību.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="b8a9f-131">Ja kāds izveido piedāvājumu vienam no starpuzņēmumu debitoriem, visus šos debitorus var ievietot vienā debitoru grupā, izmantojot lauku **Klientgrupa**.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="b8a9f-132">Virsrakstu un rindas var paplašināt, lai pievienotu lauku **Klientgrupa**, un pēc tam filtrēt, lai neiekļautu šo grupu.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Kartes iestatīšana mērķim, pāŗdošanas piedāvājuma virsraksts":::

7. <span data-ttu-id="b8a9f-134">Pēc tam, kad pagarināt elementu **Piedāvājumi**, lietojiet filtru `CUSTGROUP !=  "<company>"` kā vaicājumu virkni.</span><span class="sxs-lookup"><span data-stu-id="b8a9f-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Pārdošanas piedāvājuma virsraksts, vaicājuma rediģēšana":::
