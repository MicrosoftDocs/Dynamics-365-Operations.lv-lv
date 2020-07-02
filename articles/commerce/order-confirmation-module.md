---
title: Pasūtījumu informācijas modulis
description: Šī tēma apskata pasūtījuma informācijas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: c2ec629d9fd027be01652351ab1c99001e063e30
ms.sourcegitcommit: 49656661c89c864e8e067259a601c3bbceb8bef4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/18/2020
ms.locfileid: "3464934"
---
# <a name="order-details-module"></a><span data-ttu-id="5eff2-103">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="5eff2-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5eff2-104">Šī tēma apskata pasūtījuma informācijas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5eff2-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5eff2-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="5eff2-105">Overview</span></span>

<span data-ttu-id="5eff2-106">Pasūtījumu informācijas moduli izmanto, lai rādītu pasūtījuma apstiprinājuma informāciju pēc pasūtījuma veikšanas.</span><span class="sxs-lookup"><span data-stu-id="5eff2-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="5eff2-107">Tas parāda pasūtījuma apstiprinājuma ID, pasūtījuma kontaktinformāciju un citus pasūtījuma datus, piemēram, krājumus, kas tika iegādāti, maksājuma informāciju un nosūtīšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="5eff2-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="5eff2-108">Pasūtījumu informācijas moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="5eff2-108">Order details module properties</span></span>

| <span data-ttu-id="5eff2-109">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="5eff2-109">Property name</span></span>  | <span data-ttu-id="5eff2-110">Vērtības</span><span class="sxs-lookup"><span data-stu-id="5eff2-110">Values</span></span> | <span data-ttu-id="5eff2-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="5eff2-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="5eff2-112">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="5eff2-112">Heading</span></span>        | <span data-ttu-id="5eff2-113">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="5eff2-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="5eff2-114">Pasūtījuma informācijas modulim var būt virsraksts.</span><span class="sxs-lookup"><span data-stu-id="5eff2-114">The order details module can have a heading.</span></span> <span data-ttu-id="5eff2-115">Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete.</span><span class="sxs-lookup"><span data-stu-id="5eff2-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="5eff2-116">Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="5eff2-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="5eff2-117">Kontaktpersonas tālruņa numurs</span><span class="sxs-lookup"><span data-stu-id="5eff2-117">Contact number</span></span> | <span data-ttu-id="5eff2-118">Teksts</span><span class="sxs-lookup"><span data-stu-id="5eff2-118">Text</span></span> | <span data-ttu-id="5eff2-119">Kontaktpersonas numuru var sniegt ar pasūtījumu saistītiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="5eff2-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="5eff2-120">Moduļi, ko var izmantot pasūtījuma informācijas lapas modulī</span><span class="sxs-lookup"><span data-stu-id="5eff2-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="5eff2-121">Izveidojot pasūtījuma informācijas lapu, papildus pasūtījuma informācijas modulim varat pievienot citus atbilstošus moduļus.</span><span class="sxs-lookup"><span data-stu-id="5eff2-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="5eff2-122">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="5eff2-122">Here are some examples:</span></span>

- <span data-ttu-id="5eff2-123">**Ieteikumu modulis** — ieteikumu moduli var pievienot pasūtījuma informācijas lapai, lai klientam ieteiktu citas preces.</span><span class="sxs-lookup"><span data-stu-id="5eff2-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="5eff2-124">**Mārketinga moduļi** — jebkuru mārketinga moduli var pievienot pasūtījuma informācijas lapai, lai parādītu mārketinga saturu.</span><span class="sxs-lookup"><span data-stu-id="5eff2-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="5eff2-125">Pasūtījuma informācijas moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="5eff2-125">Add an order details module to a page</span></span>

<span data-ttu-id="5eff2-126">Lai pievienotu pasūtījuma informācijas moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="5eff2-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5eff2-127">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="5eff2-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="5eff2-128">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Pasūtījuma informācijas veidnes** nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="5eff2-129">Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5eff2-130">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5eff2-131">Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5eff2-132">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma informācija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5eff2-133">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu veidni.</span><span class="sxs-lookup"><span data-stu-id="5eff2-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="5eff2-134">Pasūtījuma informācijas modulis netiks atveidots, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.</span><span class="sxs-lookup"><span data-stu-id="5eff2-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="5eff2-135">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="5eff2-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="5eff2-136">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="5eff2-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="5eff2-137">Dialoglodziņā **Izvēlēties veidni** atlasiet **Pasūtījuma informācijas veidne**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="5eff2-138">Sadaļā **Lapas nosaukums** ievadiet **Pasūtījuma informācijas lapa** pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="5eff2-139">Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5eff2-140">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma informācija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5eff2-141">Pasūtījuma informācijas moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="5eff2-142">Dialoglodziņa **Virsraksts** laukā **Virsraksta teksts** ievadiet virsraksta teksta **Pasūtījuma informāciju** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5eff2-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="5eff2-143">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="5eff2-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="5eff2-144">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="5eff2-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5eff2-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="5eff2-145">Additional resources</span></span>

[<span data-ttu-id="5eff2-146">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="5eff2-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5eff2-147">Konteinera modulis</span><span class="sxs-lookup"><span data-stu-id="5eff2-147">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5eff2-148">Iegādes lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="5eff2-148">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5eff2-149">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="5eff2-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5eff2-150">Izrakstīšanas modulis</span><span class="sxs-lookup"><span data-stu-id="5eff2-150">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5eff2-151">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="5eff2-151">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="5eff2-152">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="5eff2-152">Footer module</span></span>](author-footer-module.md)
