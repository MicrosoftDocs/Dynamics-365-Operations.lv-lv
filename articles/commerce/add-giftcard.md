---
title: Dāvanu kartes modulis
description: Šajā tēmā aplūkoti Dāvanu kartes moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962767"
---
# <a name="gift-card-module"></a><span data-ttu-id="fc515-103">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="fc515-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc515-104">Šajā tēmā aplūkoti Dāvanu kartes moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fc515-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fc515-105">Dāvanu kartes modulis var tikt izmantots norēķinu moduļos, lai pieņemtu dāvanu kartes, kas ir parastā maksājuma forma, ko izmanto e-komercijas darījumiem.</span><span class="sxs-lookup"><span data-stu-id="fc515-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="fc515-106">Dāvanu kartes modulis atbalsta Dynamics 365, SVS un Givex dāvanu kartes.</span><span class="sxs-lookup"><span data-stu-id="fc515-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="fc515-107">SVS un Givex dāvanu kartes tiek izpirktas, izmantojot Adyen maksājumu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="fc515-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="fc515-108">Plašāku informāciju par atbalstu ārējām dāvanu kartēm, piemēram, SVS un Givex, skatiet [Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="fc515-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="fc515-109">SVS un Givex dāvanu karšu izrakstīšanas atbalsts norēķinu plūsmas laikā ir pieejams Dynamics 365 Commerce 10.0.11 laidienā.</span><span class="sxs-lookup"><span data-stu-id="fc515-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="fc515-110">Ir pieejami divi dāvanu kartes moduļi:</span><span class="sxs-lookup"><span data-stu-id="fc515-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="fc515-111">**Dāvanu karte** – Šo moduli var izmantot izrakstīšanās lapā, lai izpirktu dāvanu karti kā norēķinu.</span><span class="sxs-lookup"><span data-stu-id="fc515-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="fc515-112">**Dāvanu kartes bilances pārbaude** – Šo moduli var izmantot jebkurā lapā, lai pārbaudītu dāvanu kartes bilanci.</span><span class="sxs-lookup"><span data-stu-id="fc515-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="fc515-113">Šis modulis ir pieejams Komercijas izlaidumā 10.0.14 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="fc515-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="fc515-114">Dāvanu kartes bilances pārbaudes modulis ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.</span><span class="sxs-lookup"><span data-stu-id="fc515-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="fc515-115">Attēlā zemāk redzams cilnes dāvanu kartes moduļa piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="fc515-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dāvanu kartes moduļa piemērs](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="fc515-117">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="fc515-117">Module properties</span></span>

- <span data-ttu-id="fc515-118">**Rādīt papildu laukus** – šis rekvizīts nosaka, kuri lauki ir jārāda dāvanu kartēm papildus dāvanu kartes numuram, kas vienmēr tiek parādīts pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="fc515-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="fc515-119">Piemēram, dažas dāvanu kartes atbalsta personas identifikācijas numura (PIN) rādīšanu, bet citas atbalsta PIN un beigu datuma parādīšanu.</span><span class="sxs-lookup"><span data-stu-id="fc515-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="fc515-120">Pretējā gadījumā šis rekvizīts var tikt iestatīts uz "Nav", kas parādītu tikai dāvanu kartes numuru un papildu laukus.</span><span class="sxs-lookup"><span data-stu-id="fc515-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="fc515-121">Atbalstītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="fc515-121">Supported values:</span></span>
-   <span data-ttu-id="fc515-122">PIN</span><span class="sxs-lookup"><span data-stu-id="fc515-122">PIN</span></span>
-   <span data-ttu-id="fc515-123">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="fc515-123">Expiration date</span></span>
-   <span data-ttu-id="fc515-124">PIN un beigu datums</span><span class="sxs-lookup"><span data-stu-id="fc515-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="fc515-125">None</span><span class="sxs-lookup"><span data-stu-id="fc515-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="fc515-126">Vietas iestatījumi dāvanu karšu moduļiem</span><span class="sxs-lookup"><span data-stu-id="fc515-126">Site settings for gift card modules</span></span>

<span data-ttu-id="fc515-127">Commerce vietnes veidotājā sadaļā **Vietnes iestatījumi \> Paplašinājumi** ir dāvanu kartes moduļa iestatījums ar nosaukumu **Atbalstīto dāvanu karšu veids**.</span><span class="sxs-lookup"><span data-stu-id="fc515-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="fc515-128">Šis iestatījums atbalsta trīs vērtības:</span><span class="sxs-lookup"><span data-stu-id="fc515-128">This setting supports three values:</span></span>
- <span data-ttu-id="fc515-129">**Dynamics 365 dāvanu karte** – kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai Dynamics 365 dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="fc515-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="fc515-130">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="fc515-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="fc515-131">**SVS un GIVEX dāvanu kartes** – kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="fc515-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="fc515-132">Šis iestatījums tiek atbalstīts pierakstītiem un anonīmiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="fc515-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="fc515-133">**Dynamics 365, SVS un GIVEX dāvanu kartes** – kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj Dynamics 365, GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="fc515-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="fc515-134">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="fc515-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc515-135">Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.11 versijā, un tie ir nepieciešami tikai tad, ja ir nepieciešams atbalsts SVS vai Givex dāvanu kartēm.</span><span class="sxs-lookup"><span data-stu-id="fc515-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="fc515-136">Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="fc515-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="fc515-137">Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="fc515-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="fc515-138">Paplašināt iekšējās dāvanu kartes, kas ir izmantojamas E-commerce veikalos</span><span class="sxs-lookup"><span data-stu-id="fc515-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="fc515-139">Pēc noklusējuma iekšējās dāvanu kartes nav optimizētas izmantošanai E-commerce veikalos.</span><span class="sxs-lookup"><span data-stu-id="fc515-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="fc515-140">Tāpēc, pirms atļaut maksājumu veikšanai izmantot iekšējās dāvanu kartes, tās ir jākonfigurē ar paplašinājumiem, kas palīdz padarīt tās drošākas.</span><span class="sxs-lookup"><span data-stu-id="fc515-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="fc515-141">Šeit ir dāvanu karšu zonas, kas jāpaplašina, pirms atļaujat iekšējās dāvanu kartes izmantot ražošanā:</span><span class="sxs-lookup"><span data-stu-id="fc515-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="fc515-142">**Dāvanu kartes numurs** — numuru sērijas tiek izmantotas, lai ģenerētu dāvanu karšu numurus iekšējām dāvanu kartēm.</span><span class="sxs-lookup"><span data-stu-id="fc515-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="fc515-143">Tā kā numuru sērijas var viegli prognozēt, ir jāpaplašina dāvanu karšu numuru ģenerēšana, lai izsniegtajiem dāvanu karšu numuriem tiktu izmantotas nejaušā veidā kriptogrāfiski drošas virknes.</span><span class="sxs-lookup"><span data-stu-id="fc515-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="fc515-144">**GetBalance** - **GetBalance** API tiek izmantots, lai iegūtu dāvanu kartes bilances.</span><span class="sxs-lookup"><span data-stu-id="fc515-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="fc515-145">Pēc noklusējuma šis API ir publisks.</span><span class="sxs-lookup"><span data-stu-id="fc515-145">By default, this API public.</span></span> <span data-ttu-id="fc515-146">Ja PIN kods nav nepieciešams, lai iegūtu dāvanu karšu bilances, pastāv risks, ka uzbrucējs var izmantot **GetBalance** API, lai mēģinātu uzmeklēt dāvanu karšu numurus, kuriem ir bilances.</span><span class="sxs-lookup"><span data-stu-id="fc515-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="fc515-147">Ieviešot gan PIN prasības iekšējām dāvanu kartēm, gan API droseli, jūs varat palīdzēt samazināt risku.</span><span class="sxs-lookup"><span data-stu-id="fc515-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="fc515-148">**PIN** — pēc noklusējuma iekšējās dāvanu kartes neatbalsta PIN.</span><span class="sxs-lookup"><span data-stu-id="fc515-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="fc515-149">Ir jāpaplašina iekšējās dāvanu kartes tā, lai būtu nepieciešams PIN, lai meklētu bilances.</span><span class="sxs-lookup"><span data-stu-id="fc515-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="fc515-150">Šo funkcionalitāti var izmantot arī, lai bloķētu dāvanu kartes pēc neveiksmīgiem mēģinājumiem ievadīt PIN.</span><span class="sxs-lookup"><span data-stu-id="fc515-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="fc515-151">Iespējot dāvanu karšu maksājumus viesa norēķināšanai</span><span class="sxs-lookup"><span data-stu-id="fc515-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="fc515-152">Pēc noklusējuma dāvanu karšu maksājumi nav iespējoti viesa (anonīma) norēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="fc515-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="fc515-153">Lai iespējotu tos, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="fc515-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="fc515-154">Dodieties uz **Mazumtirdzniecība un komercija \> Kanālu iestatījumi \> POS iestātīšana \> POS \> POS operacijas**.</span><span class="sxs-lookup"><span data-stu-id="fc515-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="fc515-155">Atlasiet un turiet režģa virsrakstu (vai noklikšķiniet ar peles labo pogu) un pēc tam atlasiet **Ievietot kolonnas**.</span><span class="sxs-lookup"><span data-stu-id="fc515-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="fc515-156">Dialoglodziņā **Ievietot kolonnas** atzīmējiet izvēles rūtiņu **AllowAnonymousAccess**.</span><span class="sxs-lookup"><span data-stu-id="fc515-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="fc515-157">Atlasiet **Atjaunināt**.</span><span class="sxs-lookup"><span data-stu-id="fc515-157">Select **Update**.</span></span>
1. <span data-ttu-id="fc515-158">Operācijām **520** (Dāvanu kartes bilance) un **214** iestatiet **AllowAccessmousAccess** vērtību uz **1**.</span><span class="sxs-lookup"><span data-stu-id="fc515-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="fc515-159">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="fc515-159">Select **Save**.</span></span>
1. <span data-ttu-id="fc515-160">Palaidiet plānotāja darbu **1090**, lai sinhronizētu izmaiņas ar kanālu datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="fc515-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="fc515-161">Dāvanu kartes moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="fc515-161">Add a gift card module to a page</span></span>

<span data-ttu-id="fc515-162">Instrukcijas par to, kā pievienot dāvanu kartes moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="fc515-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc515-163">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="fc515-163">Additional resources</span></span>

[<span data-ttu-id="fc515-164">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="fc515-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fc515-165">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="fc515-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fc515-166">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="fc515-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fc515-167">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="fc515-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fc515-168">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="fc515-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="fc515-169">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="fc515-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fc515-170">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="fc515-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="fc515-171">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="fc515-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fc515-172">Atbalsts ārējām dāvanu kartēm</span><span class="sxs-lookup"><span data-stu-id="fc515-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="fc515-173">SDK un moduļu bibliotēkas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="fc515-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
