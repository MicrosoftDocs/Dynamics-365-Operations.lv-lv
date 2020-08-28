---
title: Maksājuma modulis
description: Šajā tēmā ir apskatīti maksājuma modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661215"
---
# <a name="payment-module"></a><span data-ttu-id="daa61-103">Maksājuma modulis</span><span class="sxs-lookup"><span data-stu-id="daa61-103">Payment module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="daa61-104">Šajā tēmā ir apskatīti maksājuma modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="daa61-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="daa61-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="daa61-105">Overview</span></span>

<span data-ttu-id="daa61-106">Maksājuma modulis ļauj klientiem apmaksāt pasūtījumus, izmantojot kredītkartes vai debitkartes.</span><span class="sxs-lookup"><span data-stu-id="daa61-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="daa61-107">Maksājumu integrāciju šim modulim nodrošina Dynamics 365 Payment Connector for Adyen.</span><span class="sxs-lookup"><span data-stu-id="daa61-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="daa61-108">Papildu informāciju par to, ka iestatīt un konfigurēt maksājuma savienotāju, skatiet [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="daa61-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="daa61-109">Maksājumu modulī tiek viesota maksājuma informācija, kas tiek piegādāta, izmantojot Adyen HTML vienrindas kadrā (iframe).</span><span class="sxs-lookup"><span data-stu-id="daa61-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="daa61-110">Maksājumu modulis mijiedarbojas ar Commerce Scale Unit, lai izgūtu informāciju par Adyen maksājumu.</span><span class="sxs-lookup"><span data-stu-id="daa61-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="daa61-111">Kā daļu no Commerce Scale Unit mijiedarbības maksājuma modulis var ļaut izsniegt rēķina adreses informāciju vai nu iframe, vai kā atsevišķs modulis.</span><span class="sxs-lookup"><span data-stu-id="daa61-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="daa61-112">Fabrikam tēmā rēķina adrese tiek rādīta atsevišķā modulī.</span><span class="sxs-lookup"><span data-stu-id="daa61-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="daa61-113">Šī pieeja atļauj vairāk formatēšanas elastību, jo adreses rindas var atveidot tā, ka tās atgādina piegādes adreses rindas.</span><span class="sxs-lookup"><span data-stu-id="daa61-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="daa61-114">Maksājuma modulis arī ir pierakstījies, lai saglabātu informāciju par maksājumu.</span><span class="sxs-lookup"><span data-stu-id="daa61-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="daa61-115">Maksājuma informācija un rēķina adrese tiek saglabātas un pārvaldītas, izmantojot Adyen maksājuma savienotāju.</span><span class="sxs-lookup"><span data-stu-id="daa61-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="daa61-116">Maksājuma modulis sedz visas pasūtījuma izmaksas, kas nav iekļautas lojalitātes programmas punktos vai dāvanu kartē.</span><span class="sxs-lookup"><span data-stu-id="daa61-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="daa61-117">Ja pasūtījuma kopsummu pilnībā sedz lojalitātes programmas punkti vai dāvanu karšu kredīti, maksājuma modulis tiks slēpts, un klients varēs veikt pasūtījumu bez tā.</span><span class="sxs-lookup"><span data-stu-id="daa61-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="daa61-118">Adyen maksājuma savienotājs atbalsta arī drošu klientu autentifikāciju (SCA).</span><span class="sxs-lookup"><span data-stu-id="daa61-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="daa61-119">Eiropas Savienības (ES) maksājumu pakalpojumu direktīvas 2.0 (PSD 2.0) daļa prasa, lai tiešsaistes pircēji tiktu autentificēti ārpus to tiešsaistes iepirkšanās pieredzes, kad tie izmanto elektronisko maksājumu metodi.</span><span class="sxs-lookup"><span data-stu-id="daa61-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="daa61-120">Norēķinu plūsmas laikā klienti tiek novirzīti uz savu banku vietni.</span><span class="sxs-lookup"><span data-stu-id="daa61-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="daa61-121">Pēc autentifikācijas tie tiek novirzīti uz Commerce norēķinu plūsmu.</span><span class="sxs-lookup"><span data-stu-id="daa61-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="daa61-122">Šīs novirzīšanas laikā informācija, ko klients ievadījis norēķinu plūsmā (piemēram, piegādes adrese, piegādes opcijas, dāvanu kartes informācija un lojalitātes informācija) saglabāsies.</span><span class="sxs-lookup"><span data-stu-id="daa61-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="daa61-123">Pirms jūs varat ieslēgt šo līdzekli, maksājuma savienotājam ir jābūt konfigurētam, lai varētu veikt programmas Commerce Headquarters SCA.</span><span class="sxs-lookup"><span data-stu-id="daa61-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="daa61-124">Plašāku informāciju skatiet [Droša klientu autentifikācija, izmantojot Adyen](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="daa61-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="daa61-125">Ilustrācijā zemāk ir parādīts dāvanu karšu, lojalitātes programmas, maksājumu moduļu piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="daa61-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Dāvanu karšu, lojalitātes programmas, maksājumu moduļu piemērs norēķināšanās lapā](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="daa61-127">Maksājuma moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="daa61-127">Payment module properties</span></span>

| <span data-ttu-id="daa61-128">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="daa61-128">Property name</span></span> | <span data-ttu-id="daa61-129">Vērtības</span><span class="sxs-lookup"><span data-stu-id="daa61-129">Values</span></span> | <span data-ttu-id="daa61-130">apraksts</span><span class="sxs-lookup"><span data-stu-id="daa61-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="daa61-131">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="daa61-131">Heading</span></span> | <span data-ttu-id="daa61-132">Virsraksta teksts</span><span class="sxs-lookup"><span data-stu-id="daa61-132">Heading text</span></span> | <span data-ttu-id="daa61-133">Izvēles virsraksts maksājuma modulim.</span><span class="sxs-lookup"><span data-stu-id="daa61-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="daa61-134">Iframe augstums</span><span class="sxs-lookup"><span data-stu-id="daa61-134">Height of the iframe</span></span> | <span data-ttu-id="daa61-135">Pikseļi</span><span class="sxs-lookup"><span data-stu-id="daa61-135">Pixels</span></span> | <span data-ttu-id="daa61-136">Iframe augstums pikseļos.</span><span class="sxs-lookup"><span data-stu-id="daa61-136">The iframe height, in pixels.</span></span> <span data-ttu-id="daa61-137">Augstumu var pielāgot pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="daa61-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="daa61-138">Radīt rēķina adresi</span><span class="sxs-lookup"><span data-stu-id="daa61-138">Show billing address</span></span> | <span data-ttu-id="daa61-139">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="daa61-139">**True** or **False**</span></span> | <span data-ttu-id="daa61-140">Ja šis rekvizīts ir iestatīts kā **Patiess**, norēķinu adrese tiks apkalpota ar Adyen, kas atrodas maksājumu moduļa iframe iekšpusē.</span><span class="sxs-lookup"><span data-stu-id="daa61-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="daa61-141">Ja tas ir iestatīts kā **Aplams**, rēķina adrese netiks apkalpota ar Adyen, un Commerce lietotājam būs jākonfigurē modulis, lai parādītu norēķinu adresi norēķinu lapā.</span><span class="sxs-lookup"><span data-stu-id="daa61-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="daa61-142">Maksājuma stils tiek ignorēts</span><span class="sxs-lookup"><span data-stu-id="daa61-142">Payment style override</span></span> | <span data-ttu-id="daa61-143">Kaskadētu stilu lapu (CSS) kods</span><span class="sxs-lookup"><span data-stu-id="daa61-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="daa61-144">Tā kā maksājuma modulis tiek viesots iframe, ir ierobežota stila iespēja.</span><span class="sxs-lookup"><span data-stu-id="daa61-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="daa61-145">Varat iegūt kādu stilu, izmantojot šo rekvizītu.</span><span class="sxs-lookup"><span data-stu-id="daa61-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="daa61-146">Lai ignorētu vietnes stilus, šis CSS kods ir jāielīmē kā šī rekvizīta vērtība.</span><span class="sxs-lookup"><span data-stu-id="daa61-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="daa61-147">Vietnes veidotāja CSS atsauces un stili netiek piemēroti šim modulim.</span><span class="sxs-lookup"><span data-stu-id="daa61-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="daa61-148">Norēķinu adrese</span><span class="sxs-lookup"><span data-stu-id="daa61-148">Billing address</span></span>

<span data-ttu-id="daa61-149">Maksājuma moduļa klienti sniedz norēķinu adresi maksājuma informācijai.</span><span class="sxs-lookup"><span data-stu-id="daa61-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="daa61-150">Tas arī ļauj izmantot piegādes adresi kā rēķina adresi, lai atvieglotu un paātrinātu izrakstīšanās plūsmu.</span><span class="sxs-lookup"><span data-stu-id="daa61-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="daa61-151">Ja rekvizīts **Rādīt norēķinu adresi** ir iestatīts kā **Aplams**, maksājuma modulis ir jākonfigurē norēķinu lapā.</span><span class="sxs-lookup"><span data-stu-id="daa61-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="daa61-152">Maksājuma moduļa pievienošana norēķinu lapā un nepieciešamo rekvizītu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="daa61-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="daa61-153">Maksājuma moduli var pievienot tikai norēķināšanās modulim.</span><span class="sxs-lookup"><span data-stu-id="daa61-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="daa61-154">Lai iegūtu vairāk informācijas par to, kā konfigurēt maksājuma moduli norēķinu lapai, skatiet [Norēķinu modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="daa61-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="daa61-155">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="daa61-155">Additional resources</span></span>

[<span data-ttu-id="daa61-156">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="daa61-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="daa61-157">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="daa61-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="daa61-158">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="daa61-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="daa61-159">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="daa61-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="daa61-160">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="daa61-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="daa61-161">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="daa61-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="daa61-162">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="daa61-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="daa61-163">Dynamics 365 maksājumu savienotājs pakalpojumam Adyen</span><span class="sxs-lookup"><span data-stu-id="daa61-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="daa61-164">Droša klientu autentifikācija, izmantojot Adyen</span><span class="sxs-lookup"><span data-stu-id="daa61-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
