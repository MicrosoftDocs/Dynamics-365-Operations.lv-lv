---
title: Piegādes adreses modulis
description: Šajā tēmā ir apskatīti piegādes adrešu modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985640"
---
# <a name="shipping-address-module"></a><span data-ttu-id="4f1e6-103">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="4f1e6-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f1e6-104">Šajā tēmā ir aprakstīts piegādes adrešu modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4f1e6-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="4f1e6-105">Overview</span></span>

<span data-ttu-id="4f1e6-106">Piegādes adreses modulis ļauj klientiem pievienot vai atlasīt pasūtījuma piegādes adresi norēķināšanās plūsmas laikā.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="4f1e6-107">Ja klients ir pierakstījies, tiek rādītas visas adreses, kas iepriekš tika saglabātas šim klientam, un klients var atlasīt kādu no tām.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="4f1e6-108">Klients var arī pievienot jaunu adresi.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-108">The customer can also add a new address.</span></span> <span data-ttu-id="4f1e6-109">Piegādes adreses modulis tiek izmantots visām precēm pasūtījumā, kuras nepieciešams piegādāt.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="4f1e6-110">Piegādes adreses formātus var definēt Commerce Headquarters katrai valstij vai reģionam, un piegādes adreses modulis tad ievieš valsts/reģiona specifiskos nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="4f1e6-111">Kad debitori ievada piegādes adresi izrakstīšanās plūsmā, tiem ir opcija saglabāt adresi kā primāro adresi.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="4f1e6-112">Šī opcija tiek rādīta tikai tad, ja debitors ir pieteicies.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="4f1e6-113">Kaut arī piegādes adreses modulis nenodrošina adrešu validāciju, šī funkcionalitāte var tikt īstenota ar pielāgošanu.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="4f1e6-114">Ilustrācijā zemāk redzams jauns piegādes adreses moduļa piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Piegādes adreses moduļa piemērs norēķināšanās lapā](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="4f1e6-116">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="4f1e6-116">Module properties</span></span>

| <span data-ttu-id="4f1e6-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="4f1e6-117">Property name</span></span> | <span data-ttu-id="4f1e6-118">Vērtības</span><span class="sxs-lookup"><span data-stu-id="4f1e6-118">Values</span></span> | <span data-ttu-id="4f1e6-119">apraksts</span><span class="sxs-lookup"><span data-stu-id="4f1e6-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="4f1e6-120">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="4f1e6-120">Heading</span></span> | <span data-ttu-id="4f1e6-121">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="4f1e6-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4f1e6-122">Izvēles virsraksts piegādes adreses modulim.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="4f1e6-123">Rādīt adreses veidu</span><span class="sxs-lookup"><span data-stu-id="4f1e6-123">Show address type</span></span> | <span data-ttu-id="4f1e6-124">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="4f1e6-124">**True** or **False**</span></span> | <span data-ttu-id="4f1e6-125">Ja šis neobligātais rekvizīts ir iestatīts kā **Patiess**, tiks parādīts adreses tips, piemēram, **Sākums** vai **Uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="4f1e6-126">Ja nav norādīts adreses tips, adrese automātiski tiks saglabāta kā **Tips**=**Cits**.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="4f1e6-127">Piegādes adreses moduļa pievienošana norēķināšanās lapā un nepieciešamo rekvizītu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4f1e6-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="4f1e6-128">Piegādes adreses moduli var pievienot tikai norēķināšanās modulim.</span><span class="sxs-lookup"><span data-stu-id="4f1e6-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="4f1e6-129">Lai iegūtu papildu informāciju par to, kā konfigurēt piegādes adreses moduli un pievienot to norēķinu lapai, skatiet sadaļu [Norēķināšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="4f1e6-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f1e6-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4f1e6-130">Additional resources</span></span>

[<span data-ttu-id="4f1e6-131">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="4f1e6-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4f1e6-132">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="4f1e6-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4f1e6-133">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="4f1e6-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4f1e6-134">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="4f1e6-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4f1e6-135">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="4f1e6-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4f1e6-136">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="4f1e6-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="4f1e6-137">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="4f1e6-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4f1e6-138">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="4f1e6-138">Gift card module</span></span>](add-giftcard.md)
