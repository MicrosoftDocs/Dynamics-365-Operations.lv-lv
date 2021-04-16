---
title: Starpuzņēmumu pasūtījumu filtrēšana, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju
description: Šajā tēmā ir izskaidrots, kā filtrēt starpuzņēmumu pasūtījumus, lai pasūtījumu un pasūtījumu rindu elementi nebūtu sinhronizēti.
author: negudava
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 123427db61782490d348489c23e0eaf5f8b513c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748645"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="bc410-103">Starpuzņēmumu pasūtījumu filtrēšana, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju</span><span class="sxs-lookup"><span data-stu-id="bc410-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc410-104">Varat filtrēt starpuzņēmumu pasūtījumus, lai novērstu elementu **Pasūtījumi** un **Pasūtījumu rindas** sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="bc410-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="bc410-105">Dažos gadījumos starpuzņēmumu pasūtījuma informācija nav nepieciešama programmā Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="bc410-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="bc410-106">Katra standarta Dataverse tabula tiek paplašināta ar atsaucēm uz kolonnu **IntercompanyOrder**, un duālās rakstīšanas kartes tiek modificētas, lai atsauktos uz papildu kolonnām filtros.</span><span class="sxs-lookup"><span data-stu-id="bc410-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="bc410-107">Tādēļ starpuzņēmumu pasūtījumi vairs netiek sinhronizēti.</span><span class="sxs-lookup"><span data-stu-id="bc410-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="bc410-108">Šis process palīdz izvairīties no nevajadzīgiem datiem programmā Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="bc410-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="bc410-109">Paplašināt **CDS pārdošanas pasūtījumu virsrakstu** tabulu, pievienojot atsauci kolonnai **IntercompanyOrder**.</span><span class="sxs-lookup"><span data-stu-id="bc410-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="bc410-110">Šī kolonna tiek aizpildīta tikai starpuzņēmuma pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="bc410-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="bc410-111">Lauks **IntercompanyOrder** ir pieejams elementā **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="bc410-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Kartēt sagatavošanas sadaļas ar mērķa lapu CDS pārdošanas pasūtījumu galvenēm":::

2. <span data-ttu-id="bc410-113">Kad elements **CDS pārdošanas pasūtījumu virsraksti** ir paplašināts, kolonna **IntercompanyOrder** ir pieejama kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="bc410-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="bc410-114">Lietojiet filtru ar `INTERCOMPANYORDER == ""` kā vaicājuma virkni.</span><span class="sxs-lookup"><span data-stu-id="bc410-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Rediģēt vaicājuma dialoglodziņu CDS pārdošanas pasūtījumu galvenēm":::

3. <span data-ttu-id="bc410-116">Paplašināt **CDS pārdošanas pasūtījumu virsrakstu** tabulu, pievienojot atsauci kolonnai **IntercompanyOrder**.</span><span class="sxs-lookup"><span data-stu-id="bc410-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="bc410-117">Šī kolonna tiek aizpildīta tikai starpuzņēmuma pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="bc410-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="bc410-118">Kolonna **IntercompanyOrder** ir pieejama tabulā **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="bc410-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Kartēt sagatavošanas sadaļas ar mērķa lapu CDS pārdošanas pasūtījumu līnijām":::

4. <span data-ttu-id="bc410-120">Kad ir paplašināta tabula **CDS pārdošanas pasūtījumu rindas**, kolonna **IntercompanyInventTransId** ir pieejama kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="bc410-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="bc410-121">Lietojiet filtru ar `INTERCOMPANYINVENTTRANSID == ""` kā vaicājuma virkni.</span><span class="sxs-lookup"><span data-stu-id="bc410-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Rediģēt vaicājuma dialoglodziņu CDS pārdošanas pasūtījumu līnijām":::

5. <span data-ttu-id="bc410-123">Atkārtojiet 1. un 2. darbību, lai paplašinātu tabulu **Pārdošanas rēķina galvene V2** un pievienotu filtra vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="bc410-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="bc410-124">Šajā gadījumā izmantojiet `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` filtra vaicājuma virkni.</span><span class="sxs-lookup"><span data-stu-id="bc410-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Kartēt sagatavošanas sadaļas ar mērķa lapu Pārdošanas pasūtījumu galvene V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Rediģēt vaicājuma dialoglodziņu Pārdošanas pasūtījumu galvene V2":::

6. <span data-ttu-id="bc410-127">Atkārtojiet 3. un 4. darbību, lai paplašinātu tabulu **Pārdošanas rēķina līnijas V2** un pievienotu filtra vaicājumu.</span><span class="sxs-lookup"><span data-stu-id="bc410-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="bc410-128">Šajā gadījumā izmantojiet `INTERCOMPANYINVENTTRANSID == ""` filtra vaicājuma virkni.</span><span class="sxs-lookup"><span data-stu-id="bc410-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Rediģēt vaicājuma dialoglodziņu Pārdošanas pasūtījumu līnijas V2":::

7. <span data-ttu-id="bc410-130">Tabulai **Piedāvājumi** nav starpuzņēmumu attiecību.</span><span class="sxs-lookup"><span data-stu-id="bc410-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="bc410-131">Ja kāds izveido piedāvājumu vienam no starpuzņēmumu debitoriem, visus šos debitorus var ievietot vienā debitoru grupā, izmantojot kolonnu **CustGroup**.</span><span class="sxs-lookup"><span data-stu-id="bc410-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="bc410-132">Virsrakstu un rindas var paplašināt, pievienojot kolonnu **CustGroup** un pēc tam filtrējiet tā, lai grupa nebūtu iekļauta.</span><span class="sxs-lookup"><span data-stu-id="bc410-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Kartēt sagatavošanas sadaļas ar mērķa lapu Pārdošanas pasūtījumu galvene CDS":::

8. <span data-ttu-id="bc410-134">Pēc tabulas **Piedāvājumi** paplašināšanas lietojiet filtru `CUSTGROUP != "<company>"` kā vaicājumu virkni.</span><span class="sxs-lookup"><span data-stu-id="bc410-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Rediģēt vaicājuma dialoglodziņu Pārdošanas pasūtījumu galvene CDS":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]