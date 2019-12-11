---
title: Pasūtījuma apstiprināšanas modulis
description: Šī tēma apskata pasūtījuma apstiprināšanas moduļus un apraksta, kā izveidot tos Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698330"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="4dcab-103">Pasūtījuma apstiprināšanas modulis</span><span class="sxs-lookup"><span data-stu-id="4dcab-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4dcab-104">Šī tēma apskata pasūtījuma apstiprināšanas moduļus un apraksta, kā izveidot tos Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4dcab-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4dcab-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="4dcab-105">Overview</span></span>

<span data-ttu-id="4dcab-106">Pasūtījuma apstiprināšanas modulis tiek izmantots, lai pasūtījuma apstiprināšanas lapā pēc pasūtījuma veikšanas parādītu apstiprinājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="4dcab-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="4dcab-107">Pasūtījuma apstiprināšanas modulis parāda pasūtījuma apstiprināšanas numuru un klienta e-pasta adresi, kas tika sniegta izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="4dcab-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="4dcab-108">Kad pasūtījums tiek veikts izrakstīšanas laikā, pasūtījuma apstiprināšanas numurs un klienta e-pasta adrese tiek nodoti pasūtījuma apstiprināšanas lapai kā vaicājuma virkne lapas URL.</span><span class="sxs-lookup"><span data-stu-id="4dcab-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="4dcab-109">Pasūtījuma apstiprināšanas modulis saņem šo informāciju un atveido pasūtījuma statusu pasūtījuma apstiprināšanas lapā.</span><span class="sxs-lookup"><span data-stu-id="4dcab-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="4dcab-110">Pasūtījuma apstiprināšanas modulim nepieciešams šis lapas konteksts, lai nodrošinātu pasūtījuma statusu.</span><span class="sxs-lookup"><span data-stu-id="4dcab-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="4dcab-111">Pasūtījuma apstiprināšanas moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="4dcab-111">Order confirmation module properties</span></span>

| <span data-ttu-id="4dcab-112">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="4dcab-112">Property name</span></span> | <span data-ttu-id="4dcab-113">Vērtības</span><span class="sxs-lookup"><span data-stu-id="4dcab-113">Values</span></span> | <span data-ttu-id="4dcab-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4dcab-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="4dcab-115">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="4dcab-115">Heading</span></span>       | <span data-ttu-id="4dcab-116">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="4dcab-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4dcab-117">Pasūtījuma apstiprināšanas modulim var būt virsraksts.</span><span class="sxs-lookup"><span data-stu-id="4dcab-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="4dcab-118">Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete.</span><span class="sxs-lookup"><span data-stu-id="4dcab-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="4dcab-119">Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="4dcab-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="4dcab-120">Moduļi, ko var izmantot pasūtījuma apstiprināšanas lapas modulī</span><span class="sxs-lookup"><span data-stu-id="4dcab-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="4dcab-121">**Ieteikumi** — ieteikumu moduli var ievietot pasūtījuma apstiprināšanas lapā, lai klientam ieteiktu citas preces.</span><span class="sxs-lookup"><span data-stu-id="4dcab-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="4dcab-122">**Mārketings** — mārketinga modulis var pievienot mārketinga saturu pasūtījuma apstiprināšanas lapai.</span><span class="sxs-lookup"><span data-stu-id="4dcab-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="4dcab-123">Pasūtījuma apstiprināšanas lapas moduļa izveide</span><span class="sxs-lookup"><span data-stu-id="4dcab-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="4dcab-124">Izveidojiet lapas veidni ar nosaukumu **pasūtījuma apstiprināšanas veidne**.</span><span class="sxs-lookup"><span data-stu-id="4dcab-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="4dcab-125">Noklusētās lapas slotā **Galvenais** pievienojiet pasūtījuma apstiprināšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="4dcab-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="4dcab-126">Pasūtījuma apstiprināšanas modulī pievienojiet ieteikumu moduli.</span><span class="sxs-lookup"><span data-stu-id="4dcab-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="4dcab-127">Saglabājiet un priekšskatiet veidni.</span><span class="sxs-lookup"><span data-stu-id="4dcab-127">Save and preview the template.</span></span> <span data-ttu-id="4dcab-128">Pasūtījuma apstiprināšanas moduli nedrīkst atveidot, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.</span><span class="sxs-lookup"><span data-stu-id="4dcab-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="4dcab-129">Pārbaudiet veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="4dcab-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="4dcab-130">Izmantojiet jūsu tikko izveidoto pasūtījuma apstiprināšanas veidni, lai izveidotu lapu ar nosaukumu **pasūtījuma apstiprināšanas lapa**.</span><span class="sxs-lookup"><span data-stu-id="4dcab-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="4dcab-131">Lapas strukturējumam pievienojiet noklusējuma lapu.</span><span class="sxs-lookup"><span data-stu-id="4dcab-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="4dcab-132">Slotā **Galvene** pievienojiet galvenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="4dcab-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="4dcab-133">Slotā **Kājene** pievienojiet kājenes fragmentu.</span><span class="sxs-lookup"><span data-stu-id="4dcab-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="4dcab-134">Slotā **Galvenais** pievienojiet pasūtījuma apstiprināšanas moduli.</span><span class="sxs-lookup"><span data-stu-id="4dcab-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="4dcab-135">Pasūtījuma apstiprināšanas moduļa rekvizītu rūtī pievienojiet virsrakstu **Pasūtījuma apstiprinājums**.</span><span class="sxs-lookup"><span data-stu-id="4dcab-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="4dcab-136">Zem pasūtījuma apstiprināšanas moduļa pievienojiet ieteikumu moduli un konfigurējiet to tā, lai tas izmantotu iestatījumus **Jauns** un **Vispirktākais**.</span><span class="sxs-lookup"><span data-stu-id="4dcab-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="4dcab-137">Saglabājiet un priekšskatiet lapu, reģistrējiet un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="4dcab-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4dcab-138">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4dcab-138">Additional resources</span></span>

[<span data-ttu-id="4dcab-139">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="4dcab-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4dcab-140">Container modulis</span><span class="sxs-lookup"><span data-stu-id="4dcab-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="4dcab-141">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="4dcab-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4dcab-142">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="4dcab-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4dcab-143">Izrakstīšanas modulis</span><span class="sxs-lookup"><span data-stu-id="4dcab-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4dcab-144">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="4dcab-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4dcab-145">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="4dcab-145">Footer module</span></span>](author-footer-module.md)
