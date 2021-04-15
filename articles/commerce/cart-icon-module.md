---
title: Groza ikonas modulis
description: Šajā tēmā aplūkots groza ikonas modulis un aprakstīta tā pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793085"
---
# <a name="cart-icon-module"></a><span data-ttu-id="a181f-103">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="a181f-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a181f-104">Šajā tēmā aplūkots groza ikonas modulis un aprakstīta tā pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a181f-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a181f-105">Groza ikonu modulis attēlo groza lapas galvenes modulī un parāda preču skaitu grozā.</span><span class="sxs-lookup"><span data-stu-id="a181f-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="a181f-106">Groza ikonas modulis parāda arī groza kopsavilkumu (to sauc arī par mini grozu), kad atrodaties virs groza ikonas.</span><span class="sxs-lookup"><span data-stu-id="a181f-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="a181f-107">Mini grozs sniedz lietotājam kopsavilkumu par krājumiem grozā bez nepieciešamības pāriet uz groza lapu.</span><span class="sxs-lookup"><span data-stu-id="a181f-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="a181f-108">Turklāt tas arī ļauj lietotājam doties tieši uz izrakstīšanās lapu, ja tie ir apmierināti ar kopsavilkumu.</span><span class="sxs-lookup"><span data-stu-id="a181f-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="a181f-109">Tas samazina lapu navigācijas skaitu un padara pasūtījumu ātrāku.</span><span class="sxs-lookup"><span data-stu-id="a181f-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="a181f-110">Groza ikonas modulis ir pieejams Dynamics 365 Commerce 10.0.11 laidienā.</span><span class="sxs-lookup"><span data-stu-id="a181f-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="a181f-111">Attēlā zemāk redzams groza ikonas moduļa piemērs,, kurā ir parādīts mini grozs Fabrikam galvenē.</span><span class="sxs-lookup"><span data-stu-id="a181f-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Groza ikonas moduļa piemērs](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="a181f-113">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="a181f-113">Module properties</span></span>

- <span data-ttu-id="a181f-114">**Rādīt mini grozu** — ja tas ir patiess, šis rekvizīts iespējo groza kopsavilkumu (mini grozs), kas tiks parādīts, kad atrodaties virs groza ikonas.</span><span class="sxs-lookup"><span data-stu-id="a181f-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="a181f-115">Šī funkcionalitāte tiek atbalstīta tikai darbvirsmas skatu portiem.</span><span class="sxs-lookup"><span data-stu-id="a181f-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="a181f-116">Groza ikonas moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="a181f-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="a181f-117">Lai pievienotu groza ikonas moduli, skatiet [Galvenes modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a181f-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a181f-118">Additional resources</span></span>

[<span data-ttu-id="a181f-119">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="a181f-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a181f-120">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="a181f-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a181f-121">Maksājumu modulis</span><span class="sxs-lookup"><span data-stu-id="a181f-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="a181f-122">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="a181f-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a181f-123">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="a181f-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="a181f-124">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="a181f-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="a181f-125">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="a181f-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a181f-126">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="a181f-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]