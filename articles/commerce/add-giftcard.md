---
title: Dāvanu kartes modulis
description: Šajā tēmā tiek stāstīts par dāvanu kartes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761085"
---
# <a name="gift-card-module"></a><span data-ttu-id="b4932-103">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="b4932-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b4932-104">Šajā tēmā tiek stāstīts par dāvanu kartes moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4932-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b4932-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="b4932-105">Overview</span></span>

<span data-ttu-id="b4932-106">Dāvanu kartes modulis var tikt izmantots norēķinu moduļos, lai pieņemtu dāvanu kartes, kas ir parastā maksājuma forma, ko izmanto e-komercijas darījumiem.</span><span class="sxs-lookup"><span data-stu-id="b4932-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="b4932-107">Dāvanu kartes modulis atbalsta Dynamics 365, SVS un Givex dāvanu kartes.</span><span class="sxs-lookup"><span data-stu-id="b4932-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="b4932-108">SVS un Givex dāvanu kartes tiek izpirktas, izmantojot Adyen maksājumu nodrošinātāju.</span><span class="sxs-lookup"><span data-stu-id="b4932-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="b4932-109">Plašāku informāciju par atbalstu ārējām dāvanu kartēm, piemēram, SVS un Givex, skatiet [Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="b4932-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="b4932-110">Ir pieejami divi dāvanu kartes moduļi:</span><span class="sxs-lookup"><span data-stu-id="b4932-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="b4932-111">**Dāvanu karte** - Šo moduli var izmantot izrakstīšanās lapā, lai izpirktu dāvanu karti kā norēķinu.</span><span class="sxs-lookup"><span data-stu-id="b4932-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="b4932-112">**Dāvanu kartes bilances pārbaude** - Šo moduli var izmantot jebkurā lapā, lai pārbaudītu dāvanu kartes bilanci.</span><span class="sxs-lookup"><span data-stu-id="b4932-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="b4932-113">Šis modulis ir pieejams Komercijas izlaidumā 10.0.14 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="b4932-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="b4932-114">Attēlā zemāk redzams cilnes dāvanu kartes moduļa piemērs norēķināšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="b4932-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Dāvanu kartes moduļa piemērs](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="b4932-116">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="b4932-116">Module properties</span></span>

- <span data-ttu-id="b4932-117">**Rādīt papildu laukus** - šis rekvizīts nosaka, kuri lauki ir jārāda dāvanu kartēm papildus dāvanu kartes numuram, kas vienmēr tiek parādīts pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="b4932-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="b4932-118">Piemēram, dažas dāvanu kartes atbalsta personas identifikācijas numura (PIN) rādīšanu, bet citas atbalsta PIN un beigu datuma parādīšanu.</span><span class="sxs-lookup"><span data-stu-id="b4932-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="b4932-119">Pretējā gadījumā šis rekvizīts var tikt iestatīts uz "Nav", kas parādītu tikai dāvanu kartes numuru un papildu laukus.</span><span class="sxs-lookup"><span data-stu-id="b4932-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="b4932-120">Atbalstītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="b4932-120">Supported values:</span></span>
-   <span data-ttu-id="b4932-121">PIN</span><span class="sxs-lookup"><span data-stu-id="b4932-121">PIN</span></span>
-   <span data-ttu-id="b4932-122">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="b4932-122">Expiration date</span></span>
-   <span data-ttu-id="b4932-123">PIN un beigu datums</span><span class="sxs-lookup"><span data-stu-id="b4932-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="b4932-124">None</span><span class="sxs-lookup"><span data-stu-id="b4932-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="b4932-125">Vietas iestatījumi dāvanu karšu moduļiem</span><span class="sxs-lookup"><span data-stu-id="b4932-125">Site settings for gift card modules</span></span>

<span data-ttu-id="b4932-126">Commerce vietnes veidotājā sadaļā **Vietnes iestatījumi \> Paplašinājumi** ir dāvanu kartes moduļa iestatījums ar nosaukumu **Atbalstīto dāvanu karšu veids**.</span><span class="sxs-lookup"><span data-stu-id="b4932-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="b4932-127">Šis iestatījums atbalsta trīs vērtības:</span><span class="sxs-lookup"><span data-stu-id="b4932-127">This setting supports three values:</span></span>
- <span data-ttu-id="b4932-128">**Dynamics 365 dāvanu karte** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai Dynamics 365 dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="b4932-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="b4932-129">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="b4932-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="b4932-130">**SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="b4932-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="b4932-131">Šis iestatījums tiek atbalstīts pierakstītiem un anonīmiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="b4932-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="b4932-132">**Dynamics 365, SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj Dynamics 365, GIVEX un SVS dāvanu karšu izpirkšanu.</span><span class="sxs-lookup"><span data-stu-id="b4932-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="b4932-133">Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.</span><span class="sxs-lookup"><span data-stu-id="b4932-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="b4932-134">Dāvanu kartes moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="b4932-134">Add a gift card module to a page</span></span>

<span data-ttu-id="b4932-135">Instrukcijas par to, kā pievienot dāvanu kartes moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b4932-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4932-136">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b4932-136">Additional resources</span></span>

[<span data-ttu-id="b4932-137">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="b4932-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b4932-138">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="b4932-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b4932-139">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="b4932-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b4932-140">Maksājuma modulis</span><span class="sxs-lookup"><span data-stu-id="b4932-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b4932-141">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="b4932-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b4932-142">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="b4932-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b4932-143">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="b4932-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b4932-144">Atbalsts ārējām dāvanu kartēm</span><span class="sxs-lookup"><span data-stu-id="b4932-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
