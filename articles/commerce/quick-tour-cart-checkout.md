---
title: Pārskats par grozu un norēķināšanās lapām
description: Šajā tēmā sniegts pārskats par grozu un izrakstīšanas lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e932be31a301ef5aacb68fa4e710d8a9137b7263
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817782"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="24f0e-103">Pārskats par grozu un norēķināšanās lapām</span><span class="sxs-lookup"><span data-stu-id="24f0e-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="24f0e-104">Šajā tēmā sniegts pārskats par grozu un izrakstīšanas lapām Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="24f0e-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="24f0e-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="24f0e-105">Overview</span></span>

<span data-ttu-id="24f0e-106">Elektroniskās tirdzniecības tīmekļa vietnes groza lapā ir redzamas visas preces, ko klients pievienojis grozam.</span><span class="sxs-lookup"><span data-stu-id="24f0e-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="24f0e-107">Groza lapa tiek izveidota, izmantojot groza moduli.</span><span class="sxs-lookup"><span data-stu-id="24f0e-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="24f0e-108">Groza modulis ir konteiners, kas vieso visus moduļus, kas ir nepieciešami, lai parādītu grozā esošās preces.</span><span class="sxs-lookup"><span data-stu-id="24f0e-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="24f0e-109">Groza modulis var izmantot arī citus moduļus, lai parādītu pasūtījumu kopsavilkumu un visus veicināšanas kodus, kas ir piemēroti klienta pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="24f0e-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="24f0e-110">E-tirdzniecības tīmekļa vietnes izrakstīšanas lapa parāda darbību secību, kam klients seko, lai ievadītu visu informāciju, kas nepieciešama pasūtījuma izvietošanai.</span><span class="sxs-lookup"><span data-stu-id="24f0e-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="24f0e-111">Izrakstīšanas modulī var iekļaut moduļus, kas apstrādā piegādes adresi, piegādes metodes, norēķinu informāciju, pasūtījumu kopsavilkumu un citu informāciju, kas saistīta ar klienta pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="24f0e-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="24f0e-112">Groza lapa</span><span class="sxs-lookup"><span data-stu-id="24f0e-112">Cart page</span></span>

<span data-ttu-id="24f0e-113">Groza lapa kalpo kā iepirkumu soma un ietver visas preces, kas ir pievienotas grozam.</span><span class="sxs-lookup"><span data-stu-id="24f0e-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="24f0e-114">Tālāk redzamajā attēlā ir parādīts groza lapas piemērs, kura izveidota, izmantojot moduļu bibliotēku un “Fabrikam” tēmu.</span><span class="sxs-lookup"><span data-stu-id="24f0e-114">The following illustration show an example of a cart page that was built by using the module library and the "Fabrikam" theme.</span></span>

![Groza lapas piemērs](./media/cart2.PNG)

<span data-ttu-id="24f0e-116">Groza lapas galvenā daļa parāda visas preces, ko klients pievienojis grozam.</span><span class="sxs-lookup"><span data-stu-id="24f0e-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="24f0e-117">Tiek rādītas visas piemērojamās atlaides.</span><span class="sxs-lookup"><span data-stu-id="24f0e-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="24f0e-118">Šīs atlaides ietver sarežģītas atlaides.</span><span class="sxs-lookup"><span data-stu-id="24f0e-118">These discounts include complex discounts.</span></span> <span data-ttu-id="24f0e-119">Piemēram, ir "pērciet 3 preces un saņemiet 10% atlaidi" vai "pērciet pudeli un mugursomu, lai iegūtu 10% atlaidi".</span><span class="sxs-lookup"><span data-stu-id="24f0e-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="24f0e-120">Pasūtījuma kopsavilkuma modulis parāda summu, kas jāmaksā pēc atlaižu, piegādes maksas, nodokļu utt. piemērošanas.</span><span class="sxs-lookup"><span data-stu-id="24f0e-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="24f0e-121">Tur ir arī veicināšanas koda modulis, kas ļauj klientam piemērot vai noņemt veicināšanas kodus.</span><span class="sxs-lookup"><span data-stu-id="24f0e-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="24f0e-122">Klients var iepirkties anonīmi vai kā pierakstījies lietotājs.</span><span class="sxs-lookup"><span data-stu-id="24f0e-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="24f0e-123">Ja klients ir pierakstījies, preces grozā tiek saglabātas starp sesijām.</span><span class="sxs-lookup"><span data-stu-id="24f0e-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="24f0e-124">Šādā veidā klients var turpināt iepirkšanos no vairākām ierīcēm.</span><span class="sxs-lookup"><span data-stu-id="24f0e-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="24f0e-125">No groza klients var turpināt uz izrakstīšanos.</span><span class="sxs-lookup"><span data-stu-id="24f0e-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="24f0e-126">Klients var uzsākt izrakstīšanos kā vieslietotājs vai kā pierakstījies lietotājs.</span><span class="sxs-lookup"><span data-stu-id="24f0e-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="24f0e-127">Lai iegūtu informāciju par to, kā autorēt lapa grozu, skatiet [Groza moduļa pievienošana lapai](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="24f0e-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="24f0e-128">Izrakstīšanas lapa</span><span class="sxs-lookup"><span data-stu-id="24f0e-128">Checkout page</span></span>

<span data-ttu-id="24f0e-129">Izrakstīšanas lapa ir vieta, kur klienti ievada informāciju, kas nepieciešama pasūtījuma veikšanai.</span><span class="sxs-lookup"><span data-stu-id="24f0e-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="24f0e-130">Tālāk redzamajā attēlā ir parādīts norēķināšanās lapas piemērs, kura izveidota, izmantojot moduļu bibliotēku.</span><span class="sxs-lookup"><span data-stu-id="24f0e-130">The following illustration show an example of a checkout page that was built by using the module library.</span></span>

![Izrakstīšanas lapas piemērs](./media/Checkout.PNG)

<span data-ttu-id="24f0e-132">Izrakstīšanas lapas galvenā daļā ir vieta, kur tiek apkopota visa pasūtījuma informācija.</span><span class="sxs-lookup"><span data-stu-id="24f0e-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="24f0e-133">Šī informācija ietver piegādes adresi, piegādes opcijas un maksājuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="24f0e-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="24f0e-134">Izrakstīšana ir darbību secība, jo apstrādāšanai paredzētā informācija ir jāievada noteiktā secībā.</span><span class="sxs-lookup"><span data-stu-id="24f0e-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="24f0e-135">Piemēram, piegādes adrese jāievada pirms piegādes izmaksu aprēķināšanas un maksājuma autorizēšanas.</span><span class="sxs-lookup"><span data-stu-id="24f0e-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="24f0e-136">Piegādes adrese</span><span class="sxs-lookup"><span data-stu-id="24f0e-136">Shipping address</span></span>

<span data-ttu-id="24f0e-137">Piegādes adrese ir nepieciešama, ja preces ir jāpiegādā.</span><span class="sxs-lookup"><span data-stu-id="24f0e-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="24f0e-138">Adreses formātu Dynamics 365 Commerce var konfigurēt katrai piegādes lokalizācijai.</span><span class="sxs-lookup"><span data-stu-id="24f0e-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="24f0e-139">Piemēram, ja preces tiks piegādātas Amerikas Savienotajās Valstīs, piegādes adresē ir jāiekļauj mājas adrese, štats un pasta indekss.</span><span class="sxs-lookup"><span data-stu-id="24f0e-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="24f0e-140">Piegādes adreses laukiem tiek veikta zināma pamata ievades validācija, piemēram, lai apstiprinātu burtciparu rakstzīmes, maksimālo garumu un numurus.</span><span class="sxs-lookup"><span data-stu-id="24f0e-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="24f0e-141">Lai gan pašas adreses derīgums netiek verificēts, šo verifikāciju var veikt, izmantojot pielāgotus trešās puses pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="24f0e-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="24f0e-142">Piegādes adrese tiek lietota visām grozā esošajām precēm, kurām ir atlasīta opcija "piegāde".</span><span class="sxs-lookup"><span data-stu-id="24f0e-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="24f0e-143">Ja izmantojat norēķināšanās plūsmu, ko nodrošina moduļu bibliotēka, atsevišķas groza preces nevar piegādāt uz dažādām adresēm.</span><span class="sxs-lookup"><span data-stu-id="24f0e-143">If you use the checkout flow that is provided in the module library, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="24f0e-144">Ja šī iespēja ir nepieciešama, to var īstenot, izmantojot izrakstīšanas moduļu pielāgošanu.</span><span class="sxs-lookup"><span data-stu-id="24f0e-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="24f0e-145">Kad tiek norādīta piegādes adrese, tiek parādītas Dynamics 365 Commerce tiešsaistes veikalā pieejamās piegādes metodes.</span><span class="sxs-lookup"><span data-stu-id="24f0e-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="24f0e-146">Piegādes metodes un adreses, kuras tās atbalsta, var konfigurēt Commerce.</span><span class="sxs-lookup"><span data-stu-id="24f0e-146">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="24f0e-147">Maksājums</span><span class="sxs-lookup"><span data-stu-id="24f0e-147">Payment</span></span>

<span data-ttu-id="24f0e-148">Nākamā darbība izrakstīšanas plūsmā ir maksājums.</span><span class="sxs-lookup"><span data-stu-id="24f0e-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="24f0e-149">E-tirdzniecībā, lai veiktu pasūtījumus, var izmantot vairākas maksājumu metodes, piemēram, kredītkartes, dāvanu kartes un lojalitātes punktus.</span><span class="sxs-lookup"><span data-stu-id="24f0e-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="24f0e-150">Var tikt izmantots arī šo maksājuma metožu apvienojums.</span><span class="sxs-lookup"><span data-stu-id="24f0e-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="24f0e-151">Atkarībā no izmantotajām maksājuma metodēm, var būt nepieciešama papildu informācija.</span><span class="sxs-lookup"><span data-stu-id="24f0e-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="24f0e-152">Piemēram, kredītkartes maksājumam ir nepieciešama rēķina nosūtīšanas adrese.</span><span class="sxs-lookup"><span data-stu-id="24f0e-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="24f0e-153">Kredītkaršu maksājumi tiek apstrādāti, izmantojot Adyen Payment Connector.</span><span class="sxs-lookup"><span data-stu-id="24f0e-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="24f0e-154">Lojalitātes programmas punkti</span><span class="sxs-lookup"><span data-stu-id="24f0e-154">Loyalty points</span></span>

<span data-ttu-id="24f0e-155">Izrakstīšanas plūsmas laikā klients, kurš ir lojalitātes programmas dalībnieks un kam ir uzkrāti lojalitātes punkti, var pasūtījumā izpirkt šos lojalitātes punktus.</span><span class="sxs-lookup"><span data-stu-id="24f0e-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="24f0e-156">Lojalitātes punktu modulis tiek parādīts tikai tad, ja klients ir lojalitātes programmas dalībnieks.</span><span class="sxs-lookup"><span data-stu-id="24f0e-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="24f0e-157">Nereģistrētiem lietotājiem un vieslietotājiem šis modulis ir slēpts.</span><span class="sxs-lookup"><span data-stu-id="24f0e-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="24f0e-158">Dāvanu kartes</span><span class="sxs-lookup"><span data-stu-id="24f0e-158">Gift cards</span></span>

<span data-ttu-id="24f0e-159">Moduļu bibliotēka ļauj pasūtījumā izpirkt iekšējās dāvanu kartes.</span><span class="sxs-lookup"><span data-stu-id="24f0e-159">The module library lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="24f0e-160">Lai izmantotu iekšējo dāvanu karti, klientam ir jāpierakstās.</span><span class="sxs-lookup"><span data-stu-id="24f0e-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="24f0e-161">Papildu drošībai mēs iesakām pielāgot plūsmu, izmantojot iekšējo dāvanu karšu personīgo identifikācijas numuru (PIN).</span><span class="sxs-lookup"><span data-stu-id="24f0e-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="24f0e-162">Pierakstījušies lietotāji un vieslietotāji</span><span class="sxs-lookup"><span data-stu-id="24f0e-162">Signed-in and guest users</span></span>

<span data-ttu-id="24f0e-163">Klients var pabeigt izrakstīšanas procesu kā vieslietotājs vai kā pierakstījies lietotājs.</span><span class="sxs-lookup"><span data-stu-id="24f0e-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="24f0e-164">Ja klients pierakstās, tiek automātiski izgūta konta informācija, piemēram, saglabātās piegādes adreses un saglabātā kredītkartes informācija.</span><span class="sxs-lookup"><span data-stu-id="24f0e-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="24f0e-165">Pasūtījuma kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="24f0e-165">Order summary</span></span>

<span data-ttu-id="24f0e-166">Izrakstīšana parāda rindas preču kopsavilkumu grozā, lai klients varētu pārbaudīt pasūtījumu pirms tā veikšanas.</span><span class="sxs-lookup"><span data-stu-id="24f0e-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="24f0e-167">Rindas preces nevar labot izrakstīšanas plūsmas laikā.</span><span class="sxs-lookup"><span data-stu-id="24f0e-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="24f0e-168">Tomēr tiek sniegta saite uz grozu gadījumam, ja lietotājs vēlas atgriezties un rediģēt rindas preces.</span><span class="sxs-lookup"><span data-stu-id="24f0e-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="24f0e-169">Pēc tam, kad klients sniedz piegādes un rēķina informāciju, pasūtījuma kopsavilkums atspoguļo summu, kas jāmaksā pēc lojalitātes punktu, dāvanu karšu un citiem maksājumu piemērošanas.</span><span class="sxs-lookup"><span data-stu-id="24f0e-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="24f0e-170">Pasūtījuma apstiprinājums un e-pasts</span><span class="sxs-lookup"><span data-stu-id="24f0e-170">Order confirmation and email</span></span>

<span data-ttu-id="24f0e-171">Kad klients veic pasūtījumu, tiek noradīts apstiprinājuma numurs.</span><span class="sxs-lookup"><span data-stu-id="24f0e-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="24f0e-172">Šajā brīdī maksājums ir autorizēts, bet nav ieskaitīts.</span><span class="sxs-lookup"><span data-stu-id="24f0e-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="24f0e-173">Maksājums tiks ieskaitīts tikai tad, kad pasūtījums būs izpildīts (tas ir, kad tas būs nosūtīts vai saņemts).</span><span class="sxs-lookup"><span data-stu-id="24f0e-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="24f0e-174">Kad pasūtījums ir izveidots, klientam tiek nosūtīts pasūtījuma apstiprinājuma e-pasts.</span><span class="sxs-lookup"><span data-stu-id="24f0e-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="24f0e-175">Lai iegūtu vairāk informācijas par to, kā autorēt izrakstīšanas lapu, skatiet [Izrakstīšanas moduļa pievienošana lapai](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="24f0e-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24f0e-176">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="24f0e-176">Additional resources</span></span>

[<span data-ttu-id="24f0e-177">Mājas lapas pārskats</span><span class="sxs-lookup"><span data-stu-id="24f0e-177">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="24f0e-178">Preču papildinformācijas lapu apskats</span><span class="sxs-lookup"><span data-stu-id="24f0e-178">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="24f0e-179">Konta pārvaldības lapu pārskats</span><span class="sxs-lookup"><span data-stu-id="24f0e-179">Account management pages overview</span></span>](quick-tour-account-management.md)
