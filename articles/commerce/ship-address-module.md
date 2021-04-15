---
title: Piegādes adreses modulis
description: Šajā tēmā ir apskatīts piegādes adrešu modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795433"
---
# <a name="shipping-address-module"></a><span data-ttu-id="e8159-103">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8159-104">Šajā tēmā ir aprakstīts piegādes adrešu modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e8159-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e8159-105">Piegādes adreses modulis ļauj klientiem pievienot vai atlasīt pasūtījuma piegādes adresi norēķināšanās plūsmas laikā.</span><span class="sxs-lookup"><span data-stu-id="e8159-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="e8159-106">Ja klients ir pierakstījies, tiek rādītas visas adreses, kas iepriekš tika saglabātas šim klientam, un klients var atlasīt kādu no tām.</span><span class="sxs-lookup"><span data-stu-id="e8159-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="e8159-107">Klients var arī pievienot jaunu adresi.</span><span class="sxs-lookup"><span data-stu-id="e8159-107">The customer can also add a new address.</span></span> <span data-ttu-id="e8159-108">Piegādes adreses modulis tiek izmantots visām precēm pasūtījumā, kuras nepieciešams piegādāt.</span><span class="sxs-lookup"><span data-stu-id="e8159-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="e8159-109">Piegādes adreses formātus var definēt Commerce Headquarters katrai valstij vai reģionam, un piegādes adreses modulis tad ievieš valsts/reģiona specifiskos nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="e8159-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="e8159-110">Kad debitori ievada piegādes adresi izrakstīšanās plūsmā, tiem ir opcija saglabāt adresi kā primāro adresi.</span><span class="sxs-lookup"><span data-stu-id="e8159-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="e8159-111">Šī opcija tiek rādīta tikai tad, ja debitors ir pieteicies.</span><span class="sxs-lookup"><span data-stu-id="e8159-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="e8159-112">Kaut arī piegādes adreses modulis nenodrošina adrešu validāciju, šī funkcionalitāte var tikt īstenota ar pielāgošanu.</span><span class="sxs-lookup"><span data-stu-id="e8159-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="e8159-113">Ilustrācijā zemāk redzams jauns piegādes adreses moduļa piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="e8159-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Piegādes adreses moduļa piemērs norēķināšanās lapā](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="e8159-115">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="e8159-115">Module properties</span></span>

| <span data-ttu-id="e8159-116">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="e8159-116">Property name</span></span> | <span data-ttu-id="e8159-117">Vērtības</span><span class="sxs-lookup"><span data-stu-id="e8159-117">Values</span></span> | <span data-ttu-id="e8159-118">apraksts</span><span class="sxs-lookup"><span data-stu-id="e8159-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e8159-119">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="e8159-119">Heading</span></span> | <span data-ttu-id="e8159-120">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="e8159-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e8159-121">Izvēles virsraksts piegādes adreses modulim.</span><span class="sxs-lookup"><span data-stu-id="e8159-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="e8159-122">Rādīt adreses veidu</span><span class="sxs-lookup"><span data-stu-id="e8159-122">Show address type</span></span> | <span data-ttu-id="e8159-123">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="e8159-123">**True** or **False**</span></span> | <span data-ttu-id="e8159-124">Ja šis neobligātais rekvizīts ir iestatīts kā **Patiess**, tiks parādīts adreses tips, piemēram, **Sākums** vai **Uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="e8159-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="e8159-125">Ja nav norādīts adreses tips, adrese automātiski tiks saglabāta kā **Tips**=**Cits**.</span><span class="sxs-lookup"><span data-stu-id="e8159-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="e8159-126">Iespējot automātisko ieteikumu</span><span class="sxs-lookup"><span data-stu-id="e8159-126">Enable auto suggestion</span></span>| <span data-ttu-id="e8159-127">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="e8159-127">**True** or **False**</span></span> | <span data-ttu-id="e8159-128">Ja šis neobligātais rekvizīts ir iestatīts uz **Patiess**, tiek sniegti automātiski adrešu ieteikumi.</span><span class="sxs-lookup"><span data-stu-id="e8159-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="e8159-129">Šos ieteikumus nodrošina Bing kartes.</span><span class="sxs-lookup"><span data-stu-id="e8159-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="e8159-130">Informāciju par to, kā iestatīt Bing karšu integrāciju jūsu vietnē, skatiet sadaļu [Veikalu atlasītāja modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="e8159-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="e8159-131">Šis līdzeklis ir pieejams kā Commerce versijas 10.0.15 laidiens.</span><span class="sxs-lookup"><span data-stu-id="e8159-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="e8159-132">Automātiskās ieteikšanas opcijas</span><span class="sxs-lookup"><span data-stu-id="e8159-132">Auto suggest options</span></span>| <span data-ttu-id="e8159-133">Skaits</span><span class="sxs-lookup"><span data-stu-id="e8159-133">A number</span></span>| <span data-ttu-id="e8159-134">Ja iespējoti automātiskie adrešu ieteikumi, varat norādīt papildu opcijas, piemēram, maksimālo nodrošināmo ieteikumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="e8159-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="e8159-135">Piegādes adreses moduļa pievienošana norēķināšanās lapā un nepieciešamo rekvizītu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e8159-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="e8159-136">Piegādes adreses moduli var pievienot tikai norēķināšanās modulim.</span><span class="sxs-lookup"><span data-stu-id="e8159-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="e8159-137">Lai iegūtu papildu informāciju par to, kā konfigurēt piegādes adreses moduli un pievienot to norēķinu lapai, skatiet sadaļu [Norēķināšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="e8159-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8159-138">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e8159-138">Additional resources</span></span>

[<span data-ttu-id="e8159-139">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e8159-140">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e8159-141">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e8159-142">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e8159-143">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="e8159-144">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="e8159-145">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e8159-146">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="e8159-147">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="e8159-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]