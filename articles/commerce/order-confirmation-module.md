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
ms.openlocfilehash: 407fc2724d4b589ef5f611974f9358e879dba7ed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257151"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="4c48f-103">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="4c48f-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4c48f-104">Šī tēma apskata pasūtījuma apstiprināšanas moduļus un apraksta, kā izmantot tos Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4c48f-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4c48f-105">Pasūtījumu apstiprinājuma moduli izmanto, lai rādītu pasūtījuma apstiprinājuma informāciju pēc pasūtījuma veikšanas.</span><span class="sxs-lookup"><span data-stu-id="4c48f-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="4c48f-106">Tas parāda pasūtījuma apstiprinājuma ID, pasūtījuma kontaktinformāciju un citus pasūtījuma datus, piemēram, krājumus, kas tika iegādāti, maksājuma informāciju, saņemšanas iespējas un nosūtīšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="4c48f-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="4c48f-107">Pasūtījuma apstiprināšanas moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="4c48f-107">Order confirmation module properties</span></span>

| <span data-ttu-id="4c48f-108">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="4c48f-108">Property name</span></span>  | <span data-ttu-id="4c48f-109">Vērtības</span><span class="sxs-lookup"><span data-stu-id="4c48f-109">Values</span></span> | <span data-ttu-id="4c48f-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4c48f-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="4c48f-111">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="4c48f-111">Heading</span></span>        | <span data-ttu-id="4c48f-112">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="4c48f-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4c48f-113">Pasūtījuma apstiprināšanas modulim var būt virsraksts.</span><span class="sxs-lookup"><span data-stu-id="4c48f-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="4c48f-114">Pēc noklusējuma virsrakstam tiek izmantota **H2** virsraksta etiķete.</span><span class="sxs-lookup"><span data-stu-id="4c48f-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="4c48f-115">Tomēr etiķeti var mainīt atbilstoši pieejamības prasībām.</span><span class="sxs-lookup"><span data-stu-id="4c48f-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="4c48f-116">Kontaktpersonas tālruņa numurs</span><span class="sxs-lookup"><span data-stu-id="4c48f-116">Contact number</span></span> | <span data-ttu-id="4c48f-117">Teksts</span><span class="sxs-lookup"><span data-stu-id="4c48f-117">Text</span></span> | <span data-ttu-id="4c48f-118">Kontaktpersonas numuru var sniegt ar pasūtījumu saistītiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="4c48f-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="4c48f-119">Rādīt saņemšanas laika loga informācija</span><span class="sxs-lookup"><span data-stu-id="4c48f-119">Show pickup timeslot information</span></span> | <span data-ttu-id="4c48f-120">Patiess vai aplams</span><span class="sxs-lookup"><span data-stu-id="4c48f-120">True or False</span></span> | <span data-ttu-id="4c48f-121">Šis rekvizīts ir pieejams risinājumā Dynamics 365 Commerce 10.0.15 un jaunākos.</span><span class="sxs-lookup"><span data-stu-id="4c48f-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="4c48f-122">Kad patiess, tas rāda saņemšanas laika loga informāciju, ja tas ir paredzēts saņemšanas krājumam</span><span class="sxs-lookup"><span data-stu-id="4c48f-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="4c48f-123">Moduļi, ko var izmantot pasūtījuma konfigurācijas lapas modulī</span><span class="sxs-lookup"><span data-stu-id="4c48f-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="4c48f-124">Izveidojot pasūtījuma konfigurācijas lapu, papildus pasūtījuma konfigurācijas modulim varat pievienot citus atbilstošus moduļus.</span><span class="sxs-lookup"><span data-stu-id="4c48f-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="4c48f-125">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="4c48f-125">Here are some examples:</span></span>

- <span data-ttu-id="4c48f-126">**Ieteikumu modulis** — ieteikumu moduli var pievienot pasūtījuma konfigurācijas lapai, lai klientam ieteiktu citas preces.</span><span class="sxs-lookup"><span data-stu-id="4c48f-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="4c48f-127">**Mārketinga moduļi** — jebkuru mārketinga moduli var pievienot pasūtījuma konfigurācijas lapai, lai parādītu mārketinga saturu.</span><span class="sxs-lookup"><span data-stu-id="4c48f-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="4c48f-128">Pasūtījuma konfigurācijas moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="4c48f-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="4c48f-129">Lai pievienotu pasūtījuma konfigurācijas moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="4c48f-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4c48f-130">Dodieties uz **Veidnes** un pēc tam atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="4c48f-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="4c48f-131">Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet **Pasūtījuma konfigurācijas veidnes** nosaukumu un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="4c48f-132">Slotā **Pamatteksts** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4c48f-133">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Noklusējuma lapa** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4c48f-134">Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4c48f-135">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma konfigurācija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4c48f-136">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu veidni.</span><span class="sxs-lookup"><span data-stu-id="4c48f-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="4c48f-137">Pasūtījuma apstiprināšanas modulis netiks atveidots, jo tas prasa pasūtījuma apstiprināšanas numura kontekstu.</span><span class="sxs-lookup"><span data-stu-id="4c48f-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="4c48f-138">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="4c48f-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4c48f-139">Dodieties uz **Lapas** un atlasiet **Jauns**, lai izveidotu jaunu lapu.</span><span class="sxs-lookup"><span data-stu-id="4c48f-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="4c48f-140">Dialoglodziņā **Izvēlēties veidni** atlasiet **Pasūtījuma konfigurācijas veidne**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="4c48f-141">Sadaļā **Lapas nosaukums** ievadiet **Pasūtījuma konfigurācijas lapa** pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="4c48f-142">Moduļa **Noklusējuma lapa** slotā **Galvenais** atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Pievienot moduli**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4c48f-143">Dialoglodziņā **Pievienot moduli** atlasiet moduli **Pasūtījuma konfigurācija** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="4c48f-144">Pasūtījuma konfigurācijas moduļa rekvizītu rūtī atlasiet blakus zīmuļa simbolam **Virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="4c48f-145">Dialoglodziņa **Virsraksts** laukā **Virsraksta teksts** ievadiet virsraksta teksta **Pasūtījuma konfigurāciju** un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4c48f-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="4c48f-146">Atlasiet **Saglabāt** un pēc tam atlasiet **Priekšskatījums**, lai priekšskatītu lapu.</span><span class="sxs-lookup"><span data-stu-id="4c48f-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="4c48f-147">Atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.</span><span class="sxs-lookup"><span data-stu-id="4c48f-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c48f-148">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4c48f-148">Additional resources</span></span>

[<span data-ttu-id="4c48f-149">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="4c48f-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4c48f-150">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="4c48f-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4c48f-151">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="4c48f-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4c48f-152">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="4c48f-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4c48f-153">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="4c48f-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="4c48f-154">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="4c48f-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4c48f-155">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="4c48f-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="4c48f-156">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="4c48f-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]