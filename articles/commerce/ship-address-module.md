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
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7233b23020e6c82f39981d530095642902461807
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818402"
---
# <a name="shipping-address-module"></a><span data-ttu-id="4082e-103">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="4082e-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4082e-104">Šajā tēmā ir aprakstīts piegādes adrešu modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4082e-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4082e-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="4082e-105">Overview</span></span>

<span data-ttu-id="4082e-106">Piegādes adreses modulis ļauj klientiem pievienot vai atlasīt pasūtījuma piegādes adresi norēķināšanās plūsmas laikā.</span><span class="sxs-lookup"><span data-stu-id="4082e-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="4082e-107">Ja klients ir pierakstījies, tiek rādītas visas adreses, kas iepriekš tika saglabātas šim klientam, un klients var atlasīt kādu no tām.</span><span class="sxs-lookup"><span data-stu-id="4082e-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="4082e-108">Klients var arī pievienot jaunu adresi.</span><span class="sxs-lookup"><span data-stu-id="4082e-108">The customer can also add a new address.</span></span> <span data-ttu-id="4082e-109">Piegādes adreses modulis tiek izmantots visām precēm pasūtījumā, kuras nepieciešams piegādāt.</span><span class="sxs-lookup"><span data-stu-id="4082e-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="4082e-110">Piegādes adreses formātus var definēt Commerce Headquarters katrai valstij vai reģionam, un piegādes adreses modulis tad ievieš valsts/reģiona specifiskos nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="4082e-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="4082e-111">Kad debitori ievada piegādes adresi izrakstīšanās plūsmā, tiem ir opcija saglabāt adresi kā primāro adresi.</span><span class="sxs-lookup"><span data-stu-id="4082e-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="4082e-112">Šī opcija tiek rādīta tikai tad, ja debitors ir pieteicies.</span><span class="sxs-lookup"><span data-stu-id="4082e-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="4082e-113">Kaut arī piegādes adreses modulis nenodrošina adrešu validāciju, šī funkcionalitāte var tikt īstenota ar pielāgošanu.</span><span class="sxs-lookup"><span data-stu-id="4082e-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="4082e-114">Ilustrācijā zemāk redzams jauns piegādes adreses moduļa piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="4082e-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Piegādes adreses moduļa piemērs norēķināšanās lapā](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="4082e-116">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="4082e-116">Module properties</span></span>

| <span data-ttu-id="4082e-117">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="4082e-117">Property name</span></span> | <span data-ttu-id="4082e-118">Vērtības</span><span class="sxs-lookup"><span data-stu-id="4082e-118">Values</span></span> | <span data-ttu-id="4082e-119">apraksts</span><span class="sxs-lookup"><span data-stu-id="4082e-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="4082e-120">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="4082e-120">Heading</span></span> | <span data-ttu-id="4082e-121">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="4082e-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="4082e-122">Izvēles virsraksts piegādes adreses modulim.</span><span class="sxs-lookup"><span data-stu-id="4082e-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="4082e-123">Rādīt adreses veidu</span><span class="sxs-lookup"><span data-stu-id="4082e-123">Show address type</span></span> | <span data-ttu-id="4082e-124">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="4082e-124">**True** or **False**</span></span> | <span data-ttu-id="4082e-125">Ja šis neobligātais rekvizīts ir iestatīts kā **Patiess**, tiks parādīts adreses tips, piemēram, **Sākums** vai **Uzņēmums**.</span><span class="sxs-lookup"><span data-stu-id="4082e-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="4082e-126">Ja nav norādīts adreses tips, adrese automātiski tiks saglabāta kā **Tips**=**Cits**.</span><span class="sxs-lookup"><span data-stu-id="4082e-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="4082e-127">Piegādes adreses moduļa pievienošana norēķināšanās lapā un nepieciešamo rekvizītu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="4082e-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="4082e-128">Piegādes adreses moduli var pievienot tikai norēķināšanās modulim.</span><span class="sxs-lookup"><span data-stu-id="4082e-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="4082e-129">Lai iegūtu papildu informāciju par to, kā konfigurēt piegādes adreses moduli un pievienot to norēķinu lapai, skatiet sadaļu [Norēķināšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="4082e-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4082e-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="4082e-130">Additional resources</span></span>

[<span data-ttu-id="4082e-131">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="4082e-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4082e-132">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="4082e-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4082e-133">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="4082e-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4082e-134">Maksājuma modulis</span><span class="sxs-lookup"><span data-stu-id="4082e-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4082e-135">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="4082e-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4082e-136">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="4082e-136">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4082e-137">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="4082e-137">Gift card module</span></span>](add-giftcard.md)
