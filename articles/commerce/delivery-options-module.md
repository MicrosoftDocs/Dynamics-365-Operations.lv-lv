---
title: Piegādes opciju modulis
description: Šajā tēmā ir apskatīti piegādes opciju moduļi un tiek paskaidrots, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9d8945348cbe3255ecc497f129d125ad11e9ceab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000853"
---
# <a name="delivery-options-module"></a><span data-ttu-id="b45b7-103">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="b45b7-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b45b7-104">Šajā tēmā ir apskatīti piegādes opciju moduļi un tiek paskaidrots, kā tos konfigurēt programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b45b7-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b45b7-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="b45b7-105">Overview</span></span>

<span data-ttu-id="b45b7-106">Piegādes opciju moduļi ļauj klientiem izvēlēties piegādes veidu, piemēram, nosūtīšanas vai saņemšanas to tiešsaistes pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="b45b7-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="b45b7-107">Piegādes adrese ir nepieciešama, lai noteiktu piegādes veidu.</span><span class="sxs-lookup"><span data-stu-id="b45b7-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="b45b7-108">Ja piegādes adrese mainās, piegādes opcijas ir jāizgūst no jauna.</span><span class="sxs-lookup"><span data-stu-id="b45b7-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="b45b7-109">Ja pasūtījumā ir iekļautas tikai tās preces, kas tiks saņemtas veikalā, šis modulis tiek automātiski slēpts.</span><span class="sxs-lookup"><span data-stu-id="b45b7-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="b45b7-110">Informāciju par to, kā konfigurēt piegādes veidus, skatiet sadaļās [Tiešsaistes kanāla iestatīšana](channel-setup-online.md) un [Iestatīt piegādes veidus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="b45b7-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="b45b7-111">Katram piegādes veidam var būt atbilstoša maksa.</span><span class="sxs-lookup"><span data-stu-id="b45b7-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="b45b7-112">Papildinformāciju par to, kā konfigurēt izmaksas tiešsaistes veikalam, skatiet [Omni-Channel Advanced automātiskās izmaksas](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="b45b7-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="b45b7-113">Commerce versijā 10.0.13 piegādes opciju modulis ir atjaunināts, lai atbalstītu līdzekļus **Galvenes izmaksas bez proporcijas** un **Nosūtīšana kā rindas maksa**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="b45b7-114">Ja proporcija ir izslēgta, ir sagaidāms, ka e-komercijas darbplūsma neļaus jauktu piegādes veidu grozā esošajām precēm (tas ir, dažas preces ir atlasītas nosūtīšanai, bet citas tiek atlasītas saņemšanai).</span><span class="sxs-lookup"><span data-stu-id="b45b7-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="b45b7-115">**Galvenes izmaksas bez proporcijas** līdzeklim ir nepieciešams, lai programmā Commerce Headquarters tiktu ieslēgta opcija **Iespējot konsekventu piegādes režīma apstrādi kanāla** karodziņā.</span><span class="sxs-lookup"><span data-stu-id="b45b7-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="b45b7-116">Kad šis karodziņš ir ieslēgts, nosūtīšanas izmaksas tiks piemērotas vai nu virsraksta līmenī, vai rindas līmenī atkarībā no Commerce headquarters konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="b45b7-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="b45b7-117">Fabrikam tēma atbalsta jauktu piegādes veidu, kur daži krājumi tiek atlasīti nosūtīšanai, bet citi tiek atlasīti saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="b45b7-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="b45b7-118">Šajā režīmā piegādes izmaksas tiks proporcionāli novērtētas visiem krājumiem, kas tiek atlasīti piegādes veidam.</span><span class="sxs-lookup"><span data-stu-id="b45b7-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="b45b7-119">Lai strādātu ar jauktu piegādes veidu, vispirms ir jākonfigurē līdzeklis **Galvenes izmaksas bez proporcijas** programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b45b7-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="b45b7-120">Plašāku informāciju par šo konfigurāciju skatiet [Samērot galvenes izmaksas, lai tās atbilstu pārdošanas rindām](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="b45b7-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="b45b7-121">Ja nosūtīšanas izmaksas attiecas uz rindas krājumiem, tās var tikt rādītas katra krājuma groza rindā.</span><span class="sxs-lookup"><span data-stu-id="b45b7-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="b45b7-122">Lai izmantotu šo funkcionalitāti, ir jābūt ieslēgtam rekvizītam **Parādīt sūtīšanas izmaksas rindas krājumā**, kas paredzēts gan groza modulim, gan norēķināšanās modulim.</span><span class="sxs-lookup"><span data-stu-id="b45b7-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="b45b7-123">Plašāku informāciju skatiet [Groza modulis](add-cart-module.md) un [Norēķināšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b45b7-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="b45b7-124">Ilustrācijā zemāk redzams piegādes opciju moduļa piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="b45b7-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Piegādes opciju moduļa piemērs norēķināšanās lapā](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="b45b7-126">Piegādes opciju moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="b45b7-126">Delivery options module properties</span></span>

| <span data-ttu-id="b45b7-127">Rekvizīts</span><span class="sxs-lookup"><span data-stu-id="b45b7-127">Property</span></span> | <span data-ttu-id="b45b7-128">Vērtības</span><span class="sxs-lookup"><span data-stu-id="b45b7-128">Values</span></span> | <span data-ttu-id="b45b7-129">apraksts</span><span class="sxs-lookup"><span data-stu-id="b45b7-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="b45b7-130">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="b45b7-130">Heading</span></span> | <span data-ttu-id="b45b7-131">Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**)</span><span class="sxs-lookup"><span data-stu-id="b45b7-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b45b7-132">Izvēles virsraksts piegādes opciju modulim.</span><span class="sxs-lookup"><span data-stu-id="b45b7-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="b45b7-133">Pielāgotās CSS klases nosaukums</span><span class="sxs-lookup"><span data-stu-id="b45b7-133">Custom CSS class name</span></span> | <span data-ttu-id="b45b7-134">Teksts</span><span class="sxs-lookup"><span data-stu-id="b45b7-134">Text</span></span> | <span data-ttu-id="b45b7-135">Pielāgota Cascading Style Sheets (CSS) klases nosaukums, kas tiks izmantots šī moduļa atveidei, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="b45b7-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="b45b7-136">Piegādes režīma filtra opcija</span><span class="sxs-lookup"><span data-stu-id="b45b7-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="b45b7-137">**Nefiltrēt** vai **Ar sūtīšanu nesaistīti veidi**</span><span class="sxs-lookup"><span data-stu-id="b45b7-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="b45b7-138">Vērtība, kas norāda, vai piegādes opciju modulim jāfiltrē visi piegādes veidi, kas nav saistīti ar nosūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="b45b7-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="b45b7-139">Piegādes opciju moduļa pievienošana norēķināšanās lapā un nepieciešamo rekvizītu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b45b7-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="b45b7-140">Piegādes opciju moduli var pievienot tikai norēķināšanās modulim.</span><span class="sxs-lookup"><span data-stu-id="b45b7-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="b45b7-141">Lai iegūtu papildu informāciju par to, kā konfigurēt piegādes opciju moduli un pievienot to norēķinu lapai, skatiet sadaļu [Norēķināšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b45b7-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b45b7-142">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b45b7-142">Additional resources</span></span>

[<span data-ttu-id="b45b7-143">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="b45b7-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b45b7-144">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="b45b7-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b45b7-145">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="b45b7-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b45b7-146">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="b45b7-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b45b7-147">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="b45b7-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b45b7-148">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="b45b7-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b45b7-149">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="b45b7-149">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="b45b7-150">Tiešsaistes kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b45b7-150">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="b45b7-151">Omni kanāla papildu automātiskās maksas</span><span class="sxs-lookup"><span data-stu-id="b45b7-151">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="b45b7-152">Proporcionāla virsraksta maksu sadalīšana atbilstošajās pārdošanas rindās</span><span class="sxs-lookup"><span data-stu-id="b45b7-152">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="b45b7-153">Iestatiet piegādes veidus</span><span class="sxs-lookup"><span data-stu-id="b45b7-153">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
