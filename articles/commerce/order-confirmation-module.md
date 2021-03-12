---
title: Pasūtījuma apstiprināšanas modulis
description: Šī tēma apskata pasūtījuma apstiprināšanas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972751"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="d858f-103">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="d858f-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d858f-104">Šī tēma apskata pasūtījuma apstiprināšanas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d858f-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d858f-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="d858f-105">Overview</span></span>

<span data-ttu-id="d858f-106">Pasūtījumu apstiprinājuma moduli izmanto, lai rādītu pasūtījuma apstiprinājuma informāciju pēc pasūtījuma veikšanas.</span><span class="sxs-lookup"><span data-stu-id="d858f-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="d858f-107">Tas parāda pasūtījuma apstiprinājuma ID, pasūtījuma kontaktinformāciju un citus pasūtījuma datus, piemēram, krājumus, kas tika iegādāti, maksājuma informāciju, saņemšanas iespējas un nosūtīšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="d858f-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="d858f-108">Pasūtījuma apstiprināšanas moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="d858f-108">Order confirmation module properties</span></span>

| <span data-ttu-id="d858f-109">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="d858f-109">Property name</span></span>  | <span data-ttu-id="d858f-110">Vērtības</span><span class="sxs-lookup"><span data-stu-id="d858f-110">Values</span></span> | <span data-ttu-id="d858f-111">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d858f-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d858f-112">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="d858f-112">Heading</span></span>        | <span data-ttu-id="d858f-113">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="d858f-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d858f-114">Pasūtījuma apstiprināšanas modulim var būt virsraksts.</span><span class="sxs-lookup"><span data-stu-id="d858f-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="d858f-115">Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete.</span><span class="sxs-lookup"><span data-stu-id="d858f-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="d858f-116">Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="d858f-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="d858f-117">Kontaktpersonas tālruņa numurs</span><span class="sxs-lookup"><span data-stu-id="d858f-117">Contact number</span></span> | <span data-ttu-id="d858f-118">Teksts</span><span class="sxs-lookup"><span data-stu-id="d858f-118">Text</span></span> | <span data-ttu-id="d858f-119">Kontaktpersonas numuru var sniegt ar pasūtījumu saistītiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="d858f-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="d858f-120">Rādīt saņemšanas laika loga informācija</span><span class="sxs-lookup"><span data-stu-id="d858f-120">Show pickup timeslot information</span></span> | <span data-ttu-id="d858f-121">Patiess vai aplams</span><span class="sxs-lookup"><span data-stu-id="d858f-121">True or False</span></span> | <span data-ttu-id="d858f-122">Šis rekvizīts ir pieejams risinājumā Dynamics 365 Commerce 10.0.15 un jaunākos.</span><span class="sxs-lookup"><span data-stu-id="d858f-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="d858f-123">Kad patiess, tas rāda saņemšanas laika loga informāciju, ja tas ir paredzēts saņemšanas krājumam</span><span class="sxs-lookup"><span data-stu-id="d858f-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="d858f-124">Moduļi, ko var izmantot pasūtījuma konfigurācijas lapas modulī</span><span class="sxs-lookup"><span data-stu-id="d858f-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="d858f-125">Izveidojot pasūtījuma konfigurācijas lapu, papildus pasūtījuma konfigurācijas modulim varat pievienot citus atbilstošus moduļus.</span><span class="sxs-lookup"><span data-stu-id="d858f-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="d858f-126">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="d858f-126">Here are some examples:</span></span>

- <span data-ttu-id="d858f-127">**Ieteikumu modulis** — ieteikumu moduli var pievienot pasūtījuma konfigurācijas lapai, lai klientam ieteiktu citas preces.</span><span class="sxs-lookup"><span data-stu-id="d858f-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="d858f-128">**Mārketinga moduļi** — jebkuru mārketinga moduli var pievienot pasūtījuma konfigurācijas lapai, lai parādītu mārketinga saturu.</span><span class="sxs-lookup"><span data-stu-id="d858f-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="d858f-129">Pasūtījuma konfigurācijas moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="d858f-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="d858f-130">Lai pievienotu pasūtījuma konfigurācijas moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="d858f-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d858f-131">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="d858f-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d858f-132">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Pasūtījuma konfigurācijas veidnes** nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d858f-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="d858f-133">Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d858f-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d858f-134">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d858f-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d858f-135">Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d858f-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d858f-136">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma konfigurācija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d858f-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d858f-137">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu veidni.</span><span class="sxs-lookup"><span data-stu-id="d858f-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="d858f-138">Pasūtījuma apstiprināšanas modulis netiks atveidots, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.</span><span class="sxs-lookup"><span data-stu-id="d858f-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="d858f-139">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="d858f-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d858f-140">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="d858f-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="d858f-141">Dialoglodziņā **Izvēlēties veidni** atlasiet **Pasūtījuma konfigurācijas veidne**.</span><span class="sxs-lookup"><span data-stu-id="d858f-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="d858f-142">Sadaļā **Lapas nosaukums** ievadiet **Pasūtījuma konfigurācijas lapa** pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d858f-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="d858f-143">Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="d858f-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d858f-144">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma konfigurācija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d858f-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d858f-145">Pasūtījuma konfigurācijas moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="d858f-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="d858f-146">Dialoglodziņa **Virsraksts** laukā **Virsraksta teksts** ievadiet virsraksta teksta **Pasūtījuma konfigurāciju** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="d858f-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="d858f-147">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="d858f-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="d858f-148">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="d858f-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d858f-149">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d858f-149">Additional resources</span></span>

[<span data-ttu-id="d858f-150">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="d858f-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d858f-151">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="d858f-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d858f-152">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="d858f-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d858f-153">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="d858f-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d858f-154">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="d858f-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d858f-155">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="d858f-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d858f-156">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="d858f-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="d858f-157">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="d858f-157">Gift card module</span></span>](add-giftcard.md)
