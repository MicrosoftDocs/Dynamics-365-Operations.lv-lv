---
title: Groza ikonas modulis
description: Šajā tēmā tiek stāstīts par groza ikonas moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661151"
---
# <a name="cart-icon-module"></a><span data-ttu-id="8c977-103">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="8c977-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8c977-104">Šajā tēmā tiek stāstīts par groza ikonas moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8c977-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8c977-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="8c977-105">Overview</span></span>

<span data-ttu-id="8c977-106">Groza ikonu modulis attēlo groza lapas galvenes modulī un parāda preču skaitu grozā.</span><span class="sxs-lookup"><span data-stu-id="8c977-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="8c977-107">Groza ikonas modulis parāda arī groza kopsavilkumu (to sauc arī par mini grozu), kad atrodaties virs groza ikonas.</span><span class="sxs-lookup"><span data-stu-id="8c977-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="8c977-108">Mini grozs sniedz lietotājam kopsavilkumu par krājumiem grozā bez nepieciešamības pāriet uz groza lapu.</span><span class="sxs-lookup"><span data-stu-id="8c977-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="8c977-109">Turklāt tas arī ļauj lietotājam doties tieši uz izrakstīšanās lapu, ja tie ir apmierināti ar kopsavilkumu.</span><span class="sxs-lookup"><span data-stu-id="8c977-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="8c977-110">Tas samazina lapu navigācijas skaitu un padara pasūtījumu ātrāku.</span><span class="sxs-lookup"><span data-stu-id="8c977-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="8c977-111">Attēlā zemāk redzams groza ikonas moduļa piemērs,, kurā ir parādīts mini grozs Fabrikam galvenē.</span><span class="sxs-lookup"><span data-stu-id="8c977-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Groza ikonas moduļa piemērs](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="8c977-113">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="8c977-113">Module properties</span></span>

- <span data-ttu-id="8c977-114">**Rādīt mini grozu** — ja tas ir patiess, šis rekvizīts iespējo groza kopsavilkumu (mini grozs), kas tiks parādīts, kad atrodaties virs groza ikonas.</span><span class="sxs-lookup"><span data-stu-id="8c977-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="8c977-115">Šī funkcionalitāte tiek atbalstīta tikai darbvirsmas skatu portiem.</span><span class="sxs-lookup"><span data-stu-id="8c977-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="8c977-116">Groza ikonas moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="8c977-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="8c977-117">Lai pievienotu groza ikonas moduli, skatiet [Galvenes modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="8c977-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c977-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8c977-118">Additional resources</span></span>

[<span data-ttu-id="8c977-119">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="8c977-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8c977-120">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="8c977-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8c977-121">Maksājuma modulis</span><span class="sxs-lookup"><span data-stu-id="8c977-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="8c977-122">Piegādes adreses modulis</span><span class="sxs-lookup"><span data-stu-id="8c977-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="8c977-123">Piegādes opciju modulis</span><span class="sxs-lookup"><span data-stu-id="8c977-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="8c977-124">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="8c977-124">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8c977-125">Dāvanu kartes modulis</span><span class="sxs-lookup"><span data-stu-id="8c977-125">Gift card module</span></span>](add-giftcard.md)
