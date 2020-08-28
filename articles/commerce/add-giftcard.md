---
title: Dāvanu kartes modulis
description: Šajā tēmā tiek stāstīts par dāvanu kartes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661246"
---
# <a name="gift-card-module"></a><span data-ttu-id="3e67a-103">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="3e67a-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3e67a-104">Šajā tēmā tiek stāstīts par dāvanu kartes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3e67a-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3e67a-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="3e67a-105">Overview</span></span>

<span data-ttu-id="3e67a-106">Dāvanu kartes ir parastā maksājuma forma, un dāvanu kartes modulis var tikt izmantots norēķinu modulī, lai pieņemtu dāvanu kartes.</span><span class="sxs-lookup"><span data-stu-id="3e67a-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="3e67a-107">Dāvanu kartes modulis atbalsta Dynamics 365, SVS un Givex dāvanu kartes.</span><span class="sxs-lookup"><span data-stu-id="3e67a-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="3e67a-108">SVS un Givex dāvanu kartes tiek izpirktas, izmantojot Adyen maksājumu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="3e67a-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="3e67a-109">Plašāku informāciju par atbalstu ārējām dāvanu kartēm, piemēram, SVS un Givex, skatiet [Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="3e67a-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="3e67a-110">Attēlā zemāk redzams cilnes dāvanu kartes moduļa piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="3e67a-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dāvanu kartes moduļa piemērs](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="3e67a-112">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="3e67a-112">Module properties</span></span>

- <span data-ttu-id="3e67a-113">**Rādīt papildu laukus** - šis rekvizīts nosaka, kuri lauki ir jārāda dāvanu kartēm papildus dāvanu kartes numuram, kas vienmēr tiek parādīts pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="3e67a-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="3e67a-114">Piemēram, dažas dāvanu kartes atbalsta personas identifikācijas numura (PIN) rādīšanu, bet citas atbalsta PIN un beigu datuma parādīšanu.</span><span class="sxs-lookup"><span data-stu-id="3e67a-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="3e67a-115">Pretējā gadījumā šis rekvizīts var tikt iestatīts uz "Nav", kas parādītu tikai dāvanu kartes numuru un papildu laukus.</span><span class="sxs-lookup"><span data-stu-id="3e67a-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="3e67a-116">Atbalstītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="3e67a-116">Supported values:</span></span>
-   <span data-ttu-id="3e67a-117">PIN</span><span class="sxs-lookup"><span data-stu-id="3e67a-117">PIN</span></span>
-   <span data-ttu-id="3e67a-118">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="3e67a-118">Expiration date</span></span>
-   <span data-ttu-id="3e67a-119">PIN un beigu datums</span><span class="sxs-lookup"><span data-stu-id="3e67a-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="3e67a-120">None</span><span class="sxs-lookup"><span data-stu-id="3e67a-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="3e67a-121">Vietas iestatījumi dāvanu karšu moduļiem</span><span class="sxs-lookup"><span data-stu-id="3e67a-121">Site settings for gift card modules</span></span>

<span data-ttu-id="3e67a-122">Commerce vietnes veidotājā sadaļā **Vietnes iestatījumi \>Paplašinājumi** ir dāvanu kartes moduļa iestatījums ar nosaukumu **Atbalstīto dāvanu karšu veids**.</span><span class="sxs-lookup"><span data-stu-id="3e67a-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="3e67a-123">Šis iestatījums atbalsta trīs vērtības:</span><span class="sxs-lookup"><span data-stu-id="3e67a-123">This setting supports three values:</span></span>
- <span data-ttu-id="3e67a-124">**Dynamics 365 dāvanu karte** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai Dynamics 365 dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="3e67a-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="3e67a-125">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="3e67a-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="3e67a-126">**SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="3e67a-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="3e67a-127">Šis iestatījums tiek atbalstīts pierakstītiem un anonīmiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="3e67a-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="3e67a-128">**Dynamics 365, SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj Dynamics 365, GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="3e67a-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="3e67a-129">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="3e67a-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="3e67a-130">Dāvanu kartes moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="3e67a-130">Add a gift card module to a page</span></span>

<span data-ttu-id="3e67a-131">Instrukcijas par to, kā pievienot dāvanu kartes moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="3e67a-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e67a-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="3e67a-132">Additional resources</span></span>

[<span data-ttu-id="3e67a-133">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="3e67a-133">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3e67a-134">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="3e67a-134">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="3e67a-135">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="3e67a-135">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3e67a-136">Maksājuma modulis</span><span class="sxs-lookup"><span data-stu-id="3e67a-136">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="3e67a-137">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="3e67a-137">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="3e67a-138">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="3e67a-138">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="3e67a-139">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="3e67a-139">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3e67a-140">Atbalsts ārējām dāvanu kartēm</span><span class="sxs-lookup"><span data-stu-id="3e67a-140">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
