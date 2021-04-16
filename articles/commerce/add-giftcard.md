---
title: Dāvanu kartes modulis
description: Šajā tēmā aplūkoti Dāvanu kartes moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797675"
---
# <a name="gift-card-module"></a><span data-ttu-id="8beeb-103">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="8beeb-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8beeb-104">Šajā tēmā aplūkoti Dāvanu kartes moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8beeb-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8beeb-105">Dāvanu kartes modulis var tikt izmantots norēķinu moduļos, lai pieņemtu dāvanu kartes, kas ir parastā maksājuma forma, ko izmanto e-komercijas darījumiem.</span><span class="sxs-lookup"><span data-stu-id="8beeb-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="8beeb-106">Dāvanu kartes modulis atbalsta Dynamics 365, SVS un Givex dāvanu kartes.</span><span class="sxs-lookup"><span data-stu-id="8beeb-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="8beeb-107">SVS un Givex dāvanu kartes tiek izpirktas, izmantojot Adyen maksājumu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="8beeb-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="8beeb-108">Plašāku informāciju par atbalstu ārējām dāvanu kartēm, piemēram, SVS un Givex, skatiet [Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="8beeb-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8beeb-109">SVS un Givex dāvanu karšu izrakstīšanas atbalsts norēķinu plūsmas laikā ir pieejams Dynamics 365 Commerce 10.0.11 laidienā.</span><span class="sxs-lookup"><span data-stu-id="8beeb-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="8beeb-110">Ir pieejami divi dāvanu kartes moduļi:</span><span class="sxs-lookup"><span data-stu-id="8beeb-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="8beeb-111">**Dāvanu karte** - Šo moduli var izmantot izrakstīšanās lapā, lai izpirktu dāvanu karti kā norēķinu.</span><span class="sxs-lookup"><span data-stu-id="8beeb-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="8beeb-112">**Dāvanu kartes bilances pārbaude** - Šo moduli var izmantot jebkurā lapā, lai pārbaudītu dāvanu kartes bilanci.</span><span class="sxs-lookup"><span data-stu-id="8beeb-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="8beeb-113">Šis modulis ir pieejams Komercijas izlaidumā 10.0.14 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="8beeb-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="8beeb-114">Dāvanu kartes bilances pārbaudes modulis ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.</span><span class="sxs-lookup"><span data-stu-id="8beeb-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="8beeb-115">Attēlā zemāk redzams cilnes dāvanu kartes moduļa piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="8beeb-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dāvanu kartes moduļa piemērs](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="8beeb-117">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="8beeb-117">Module properties</span></span>

- <span data-ttu-id="8beeb-118">**Rādīt papildu laukus** - šis rekvizīts nosaka, kuri lauki ir jārāda dāvanu kartēm papildus dāvanu kartes numuram, kas vienmēr tiek parādīts pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="8beeb-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="8beeb-119">Piemēram, dažas dāvanu kartes atbalsta personas identifikācijas numura (PIN) rādīšanu, bet citas atbalsta PIN un beigu datuma parādīšanu.</span><span class="sxs-lookup"><span data-stu-id="8beeb-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="8beeb-120">Pretējā gadījumā šis rekvizīts var tikt iestatīts uz "Nav", kas parādītu tikai dāvanu kartes numuru un papildu laukus.</span><span class="sxs-lookup"><span data-stu-id="8beeb-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="8beeb-121">Atbalstītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="8beeb-121">Supported values:</span></span>
-   <span data-ttu-id="8beeb-122">PIN</span><span class="sxs-lookup"><span data-stu-id="8beeb-122">PIN</span></span>
-   <span data-ttu-id="8beeb-123">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="8beeb-123">Expiration date</span></span>
-   <span data-ttu-id="8beeb-124">PIN un beigu datums</span><span class="sxs-lookup"><span data-stu-id="8beeb-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="8beeb-125">None</span><span class="sxs-lookup"><span data-stu-id="8beeb-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="8beeb-126">Vietas iestatījumi dāvanu karšu moduļiem</span><span class="sxs-lookup"><span data-stu-id="8beeb-126">Site settings for gift card modules</span></span>

<span data-ttu-id="8beeb-127">Commerce vietnes veidotājā sadaļā **Vietnes iestatījumi \> Paplašinājumi** ir dāvanu kartes moduļa iestatījums ar nosaukumu **Atbalstīto dāvanu karšu veids**.</span><span class="sxs-lookup"><span data-stu-id="8beeb-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="8beeb-128">Šis iestatījums atbalsta trīs vērtības:</span><span class="sxs-lookup"><span data-stu-id="8beeb-128">This setting supports three values:</span></span>
- <span data-ttu-id="8beeb-129">**Dynamics 365 dāvanu karte** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai Dynamics 365 dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="8beeb-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="8beeb-130">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="8beeb-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="8beeb-131">**SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="8beeb-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="8beeb-132">Šis iestatījums tiek atbalstīts pierakstītiem un anonīmiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="8beeb-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="8beeb-133">**Dynamics 365, SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj Dynamics 365, GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="8beeb-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="8beeb-134">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="8beeb-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8beeb-135">Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.11 versijā, un tie ir nepieciešami tikai tad, ja ir nepieciešams atbalsts SVS vai Givex dāvanu kartēm.</span><span class="sxs-lookup"><span data-stu-id="8beeb-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="8beeb-136">Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="8beeb-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="8beeb-137">Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="8beeb-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="8beeb-138">Dāvanu kartes moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="8beeb-138">Add a gift card module to a page</span></span>

<span data-ttu-id="8beeb-139">Instrukcijas par to, kā pievienot dāvanu kartes moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="8beeb-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8beeb-140">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8beeb-140">Additional resources</span></span>

[<span data-ttu-id="8beeb-141">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="8beeb-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8beeb-142">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="8beeb-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="8beeb-143">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="8beeb-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8beeb-144">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="8beeb-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="8beeb-145">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="8beeb-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="8beeb-146">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="8beeb-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="8beeb-147">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="8beeb-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="8beeb-148">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="8beeb-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8beeb-149">Atbalsts ārējām dāvanu kartēm</span><span class="sxs-lookup"><span data-stu-id="8beeb-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="8beeb-150">SDK un moduļu bibliotēkas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="8beeb-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]