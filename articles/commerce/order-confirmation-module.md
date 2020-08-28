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
ms.openlocfilehash: 5876b953a3b3d960c106acf37731fde13b93f8e7
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661176"
---
# <a name="order-details-module"></a><span data-ttu-id="48eac-103">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="48eac-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="48eac-104">Šī tēma apskata pasūtījuma informācijas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48eac-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="48eac-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="48eac-105">Overview</span></span>

<span data-ttu-id="48eac-106">Pasūtījumu informācijas moduli izmanto, lai rādītu pasūtījuma apstiprinājuma informāciju pēc pasūtījuma veikšanas.</span><span class="sxs-lookup"><span data-stu-id="48eac-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="48eac-107">Tas parāda pasūtījuma apstiprinājuma ID, pasūtījuma kontaktinformāciju un citus pasūtījuma datus, piemēram, krājumus, kas tika iegādāti, maksājuma informāciju un nosūtīšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="48eac-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="48eac-108">Pasūtījumu informācijas moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="48eac-108">Order details module properties</span></span>

| <span data-ttu-id="48eac-109">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="48eac-109">Property name</span></span>  | <span data-ttu-id="48eac-110">Vērtības</span><span class="sxs-lookup"><span data-stu-id="48eac-110">Values</span></span> | <span data-ttu-id="48eac-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="48eac-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="48eac-112">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="48eac-112">Heading</span></span>        | <span data-ttu-id="48eac-113">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="48eac-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="48eac-114">Pasūtījuma informācijas modulim var būt virsraksts.</span><span class="sxs-lookup"><span data-stu-id="48eac-114">The order details module can have a heading.</span></span> <span data-ttu-id="48eac-115">Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete.</span><span class="sxs-lookup"><span data-stu-id="48eac-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="48eac-116">Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="48eac-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="48eac-117">Kontaktpersonas tālruņa numurs</span><span class="sxs-lookup"><span data-stu-id="48eac-117">Contact number</span></span> | <span data-ttu-id="48eac-118">Teksts</span><span class="sxs-lookup"><span data-stu-id="48eac-118">Text</span></span> | <span data-ttu-id="48eac-119">Kontaktpersonas numuru var sniegt ar pasūtījumu saistītiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="48eac-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="48eac-120">Moduļi, ko var izmantot pasūtījuma informācijas lapas modulī</span><span class="sxs-lookup"><span data-stu-id="48eac-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="48eac-121">Izveidojot pasūtījuma informācijas lapu, papildus pasūtījuma informācijas modulim varat pievienot citus atbilstošus moduļus.</span><span class="sxs-lookup"><span data-stu-id="48eac-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="48eac-122">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="48eac-122">Here are some examples:</span></span>

- <span data-ttu-id="48eac-123">**Ieteikumu modulis** — ieteikumu moduli var pievienot pasūtījuma informācijas lapai, lai klientam ieteiktu citas preces.</span><span class="sxs-lookup"><span data-stu-id="48eac-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="48eac-124">**Mārketinga moduļi** — jebkuru mārketinga moduli var pievienot pasūtījuma informācijas lapai, lai parādītu mārketinga saturu.</span><span class="sxs-lookup"><span data-stu-id="48eac-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="48eac-125">Pasūtījuma informācijas moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="48eac-125">Add an order details module to a page</span></span>

<span data-ttu-id="48eac-126">Lai pievienotu pasūtījuma informācijas moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="48eac-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="48eac-127">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="48eac-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="48eac-128">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Pasūtījuma informācijas veidnes** nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="48eac-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="48eac-129">Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="48eac-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="48eac-130">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="48eac-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="48eac-131">Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="48eac-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="48eac-132">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma informācija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="48eac-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="48eac-133">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu veidni.</span><span class="sxs-lookup"><span data-stu-id="48eac-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="48eac-134">Pasūtījuma informācijas modulis netiks atveidots, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.</span><span class="sxs-lookup"><span data-stu-id="48eac-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="48eac-135">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="48eac-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="48eac-136">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="48eac-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="48eac-137">Dialoglodziņā **Izvēlēties veidni** atlasiet **Pasūtījuma informācijas veidne**.</span><span class="sxs-lookup"><span data-stu-id="48eac-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="48eac-138">Sadaļā **Lapas nosaukums** ievadiet **Pasūtījuma informācijas lapa** pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="48eac-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="48eac-139">Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="48eac-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="48eac-140">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma informācija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="48eac-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="48eac-141">Pasūtījuma informācijas moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="48eac-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="48eac-142">Dialoglodziņa **Virsraksts** laukā **Virsraksta teksts** ievadiet virsraksta teksta **Pasūtījuma informāciju** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="48eac-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="48eac-143">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="48eac-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="48eac-144">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="48eac-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48eac-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="48eac-145">Additional resources</span></span>

[<span data-ttu-id="48eac-146">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="48eac-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="48eac-147">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="48eac-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="48eac-148">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="48eac-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="48eac-149">Maksājuma modulis</span><span class="sxs-lookup"><span data-stu-id="48eac-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="48eac-150">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="48eac-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="48eac-151">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="48eac-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="48eac-152">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="48eac-152">Gift card module</span></span>](add-giftcard.md)
