---
title: Pasūtījumu informācijas modulis
description: Šī tēma apskata pasūtījuma informācijas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026021"
---
# <a name="order-details-module"></a><span data-ttu-id="0b233-103">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="0b233-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0b233-104">Šī tēma apskata pasūtījuma informācijas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0b233-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0b233-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="0b233-105">Overview</span></span>

<span data-ttu-id="0b233-106">Pasūtījumu informācijas moduli izmanto, lai rādītu pasūtījuma apstiprinājuma informāciju pēc pasūtījuma veikšanas.</span><span class="sxs-lookup"><span data-stu-id="0b233-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="0b233-107">Tas parāda pasūtījuma apstiprinājuma ID, pasūtījuma kontaktinformāciju un citus pasūtījuma datus, piemēram, krājumus, kas tika iegādāti, maksājuma informāciju un nosūtīšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="0b233-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="0b233-108">Pasūtījuma apstiprināšanas moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="0b233-108">Order confirmation module properties</span></span>

| <span data-ttu-id="0b233-109">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="0b233-109">Property name</span></span>  | <span data-ttu-id="0b233-110">Vērtības</span><span class="sxs-lookup"><span data-stu-id="0b233-110">Values</span></span> | <span data-ttu-id="0b233-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="0b233-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0b233-112">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="0b233-112">Heading</span></span>        | <span data-ttu-id="0b233-113">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="0b233-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0b233-114">Pasūtījuma apstiprināšanas modulim var būt virsraksts.</span><span class="sxs-lookup"><span data-stu-id="0b233-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="0b233-115">Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete.</span><span class="sxs-lookup"><span data-stu-id="0b233-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="0b233-116">Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="0b233-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0b233-117">Kontaktpersonas tālruņa numurs</span><span class="sxs-lookup"><span data-stu-id="0b233-117">Contact number</span></span> | <span data-ttu-id="0b233-118">Teksts</span><span class="sxs-lookup"><span data-stu-id="0b233-118">Text</span></span> | <span data-ttu-id="0b233-119">Kontaktpersonas numuru var sniegt ar pasūtījumu saistītiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="0b233-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="0b233-120">Moduļi, ko var izmantot pasūtījuma informācijas lapas modulī</span><span class="sxs-lookup"><span data-stu-id="0b233-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="0b233-121">Izveidojot pasūtījuma informācijas lapu, papildus pasūtījuma informācijas modulim varat pievienot citus atbilstošus moduļus.</span><span class="sxs-lookup"><span data-stu-id="0b233-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="0b233-122">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="0b233-122">Here are some examples:</span></span>

- <span data-ttu-id="0b233-123">**Ieteikumu modulis** — ieteikumu moduli var pievienot pasūtījuma informācijas lapai, lai klientam ieteiktu citas preces.</span><span class="sxs-lookup"><span data-stu-id="0b233-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="0b233-124">**Mārketinga moduļi** — jebkuru mārketinga moduli var pievienot pasūtījuma informācijas lapai, lai parādītu mārketinga saturu.</span><span class="sxs-lookup"><span data-stu-id="0b233-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="0b233-125">Pasūtījuma informācijas lapas moduļa izveide</span><span class="sxs-lookup"><span data-stu-id="0b233-125">Create an order details page module</span></span>

1. <span data-ttu-id="0b233-126">Izveidojiet lapas veidni ar nosaukumu **Pasūtījuma informācijas veidne**.</span><span class="sxs-lookup"><span data-stu-id="0b233-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="0b233-127">Noklusētās lapas slotā **Galvenais** pievienojiet pasūtījuma informācijas moduli.</span><span class="sxs-lookup"><span data-stu-id="0b233-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="0b233-128">Pasūtījuma informācijas modulī pievienojiet ieteikumu moduli.</span><span class="sxs-lookup"><span data-stu-id="0b233-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="0b233-129">Saglabājiet un priekšskatiet veidni.</span><span class="sxs-lookup"><span data-stu-id="0b233-129">Save and preview the template.</span></span> <span data-ttu-id="0b233-130">Pasūtījuma informācijas modulis netiks atveidots, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.</span><span class="sxs-lookup"><span data-stu-id="0b233-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="0b233-131">Pabeidziet rediģēt veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="0b233-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="0b233-132">Izmantojiet jūsu tikko izveidoto pasūtījuma informācijas veidni, lai izveidotu lapu ar nosaukumu **pasūtījuma informācijas lapa**.</span><span class="sxs-lookup"><span data-stu-id="0b233-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="0b233-133">Lapas strukturējumam pievienojiet noklusējuma lapu.</span><span class="sxs-lookup"><span data-stu-id="0b233-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="0b233-134">Slotā **Galvene** pievienojiet galvenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="0b233-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="0b233-135">Slotā **Kājene** pievienojiet kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="0b233-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="0b233-136">Slotā **Galvenais** pievienojiet pasūtījuma informācijas moduli.</span><span class="sxs-lookup"><span data-stu-id="0b233-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="0b233-137">Pasūtījuma informācijas moduļa rekvizītu rūtī pievienojiet virsrakstu **Pasūtījuma informācija**.</span><span class="sxs-lookup"><span data-stu-id="0b233-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="0b233-138">Zem pasūtījuma informācijas moduļa pievienojiet ieteikumu moduli un konfigurējiet to tā, lai tas izmantotu iestatījumus **Jauns** un **Vispirktākais**.</span><span class="sxs-lookup"><span data-stu-id="0b233-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="0b233-139">Saglabājiet un priekšskatiet lapu.</span><span class="sxs-lookup"><span data-stu-id="0b233-139">Save and preview the page.</span></span>
1. <span data-ttu-id="0b233-140">Pabeidziet rediģēt lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="0b233-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b233-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="0b233-141">Additional resources</span></span>

[<span data-ttu-id="0b233-142">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="0b233-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0b233-143">Container modulis</span><span class="sxs-lookup"><span data-stu-id="0b233-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0b233-144">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="0b233-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0b233-145">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="0b233-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0b233-146">Izrakstīšanas modulis</span><span class="sxs-lookup"><span data-stu-id="0b233-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0b233-147">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="0b233-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0b233-148">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="0b233-148">Footer module</span></span>](author-footer-module.md)
