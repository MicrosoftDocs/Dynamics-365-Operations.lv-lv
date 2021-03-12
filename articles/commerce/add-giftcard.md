---
title: Dāvanu kartes modulis
description: Šajā tēmā tiek stāstīts par dāvanu kartes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9626f33ced0433bc96ed58429e95d4f75af6508
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980386"
---
# <a name="gift-card-module"></a><span data-ttu-id="66826-103">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="66826-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="66826-104">Šajā tēmā tiek stāstīts par dāvanu kartes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="66826-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="66826-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="66826-105">Overview</span></span>

<span data-ttu-id="66826-106">Dāvanu kartes modulis var tikt izmantots norēķinu moduļos, lai pieņemtu dāvanu kartes, kas ir parastā maksājuma forma, ko izmanto e-komercijas darījumiem.</span><span class="sxs-lookup"><span data-stu-id="66826-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="66826-107">Dāvanu kartes modulis atbalsta Dynamics 365, SVS un Givex dāvanu kartes.</span><span class="sxs-lookup"><span data-stu-id="66826-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="66826-108">SVS un Givex dāvanu kartes tiek izpirktas, izmantojot Adyen maksājumu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="66826-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="66826-109">Plašāku informāciju par atbalstu ārējām dāvanu kartēm, piemēram, SVS un Givex, skatiet [Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="66826-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="66826-110">SVS un Givex dāvanu karšu izrakstīšanas atbalsts norēķinu plūsmas laikā ir pieejams Dynamics 365 Commerce 10.0.11 laidienā.</span><span class="sxs-lookup"><span data-stu-id="66826-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="66826-111">Ir pieejami divi dāvanu kartes moduļi:</span><span class="sxs-lookup"><span data-stu-id="66826-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="66826-112">**Dāvanu karte** - Šo moduli var izmantot izrakstīšanās lapā, lai izpirktu dāvanu karti kā norēķinu.</span><span class="sxs-lookup"><span data-stu-id="66826-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="66826-113">**Dāvanu kartes bilances pārbaude** - Šo moduli var izmantot jebkurā lapā, lai pārbaudītu dāvanu kartes bilanci.</span><span class="sxs-lookup"><span data-stu-id="66826-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="66826-114">Šis modulis ir pieejams Komercijas izlaidumā 10.0.14 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="66826-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="66826-115">Dāvanu kartes bilances pārbaudes modulis ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.</span><span class="sxs-lookup"><span data-stu-id="66826-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="66826-116">Attēlā zemāk redzams cilnes dāvanu kartes moduļa piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="66826-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dāvanu kartes moduļa piemērs](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="66826-118">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="66826-118">Module properties</span></span>

- <span data-ttu-id="66826-119">**Rādīt papildu laukus** - šis rekvizīts nosaka, kuri lauki ir jārāda dāvanu kartēm papildus dāvanu kartes numuram, kas vienmēr tiek parādīts pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="66826-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="66826-120">Piemēram, dažas dāvanu kartes atbalsta personas identifikācijas numura (PIN) rādīšanu, bet citas atbalsta PIN un beigu datuma parādīšanu.</span><span class="sxs-lookup"><span data-stu-id="66826-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="66826-121">Pretējā gadījumā šis rekvizīts var tikt iestatīts uz "Nav", kas parādītu tikai dāvanu kartes numuru un papildu laukus.</span><span class="sxs-lookup"><span data-stu-id="66826-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="66826-122">Atbalstītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="66826-122">Supported values:</span></span>
-   <span data-ttu-id="66826-123">PIN</span><span class="sxs-lookup"><span data-stu-id="66826-123">PIN</span></span>
-   <span data-ttu-id="66826-124">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="66826-124">Expiration date</span></span>
-   <span data-ttu-id="66826-125">PIN un beigu datums</span><span class="sxs-lookup"><span data-stu-id="66826-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="66826-126">None</span><span class="sxs-lookup"><span data-stu-id="66826-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="66826-127">Vietas iestatījumi dāvanu karšu moduļiem</span><span class="sxs-lookup"><span data-stu-id="66826-127">Site settings for gift card modules</span></span>

<span data-ttu-id="66826-128">Commerce vietnes veidotājā sadaļā **Vietnes iestatījumi \> Paplašinājumi** ir dāvanu kartes moduļa iestatījums ar nosaukumu **Atbalstīto dāvanu karšu veids**.</span><span class="sxs-lookup"><span data-stu-id="66826-128">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="66826-129">Šis iestatījums atbalsta trīs vērtības:</span><span class="sxs-lookup"><span data-stu-id="66826-129">This setting supports three values:</span></span>
- <span data-ttu-id="66826-130">**Dynamics 365 dāvanu karte** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai Dynamics 365 dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="66826-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="66826-131">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="66826-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="66826-132">**SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="66826-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="66826-133">Šis iestatījums tiek atbalstīts pierakstītiem un anonīmiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="66826-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="66826-134">**Dynamics 365, SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj Dynamics 365, GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="66826-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="66826-135">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="66826-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66826-136">Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.11 versijā, un tie ir nepieciešami tikai tad, ja ir nepieciešams atbalsts SVS vai Givex dāvanu kartēm.</span><span class="sxs-lookup"><span data-stu-id="66826-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="66826-137">Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="66826-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="66826-138">Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="66826-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="66826-139">Dāvanu kartes moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="66826-139">Add a gift card module to a page</span></span>

<span data-ttu-id="66826-140">Instrukcijas par to, kā pievienot dāvanu kartes moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="66826-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66826-141">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="66826-141">Additional resources</span></span>

[<span data-ttu-id="66826-142">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="66826-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="66826-143">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="66826-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="66826-144">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="66826-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="66826-145">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="66826-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="66826-146">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="66826-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="66826-147">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="66826-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="66826-148">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="66826-148">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="66826-149">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="66826-149">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="66826-150">Atbalsts ārējām dāvanu kartēm</span><span class="sxs-lookup"><span data-stu-id="66826-150">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="66826-151">SDK un moduļu bibliotēkas atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="66826-151">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
