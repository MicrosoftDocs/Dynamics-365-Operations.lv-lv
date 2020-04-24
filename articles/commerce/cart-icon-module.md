---
title: Groza ikonas modulis
description: Šajā tēmā tiek stāstīts par groza ikonas moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261578"
---
# <a name="cart-icon-module"></a><span data-ttu-id="eca6d-103">Groza ikonas modulis</span><span class="sxs-lookup"><span data-stu-id="eca6d-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eca6d-104">Šajā tēmā tiek stāstīts par groza ikonas moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="eca6d-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="eca6d-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="eca6d-105">Overview</span></span>

<span data-ttu-id="eca6d-106">Groza ikonu modulis attēlo groza lapas galvenes modulī un parāda preču skaitu grozā.</span><span class="sxs-lookup"><span data-stu-id="eca6d-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="eca6d-107">Groza ikonas modulis parāda arī groza kopsavilkumu (to sauc arī par mini grozu), kad atrodaties virs groza ikonas.</span><span class="sxs-lookup"><span data-stu-id="eca6d-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="eca6d-108">Mini grozs sniedz lietotājam kopsavilkumu par krājumiem grozā bez nepieciešamības pāriet uz groza lapu.</span><span class="sxs-lookup"><span data-stu-id="eca6d-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="eca6d-109">Turklāt tas arī ļauj lietotājam doties tieši uz izrakstīšanās lapu, ja tie ir apmierināti ar kopsavilkumu.</span><span class="sxs-lookup"><span data-stu-id="eca6d-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="eca6d-110">Tas samazina lapu navigācijas skaitu un padara pasūtījumu ātrāku.</span><span class="sxs-lookup"><span data-stu-id="eca6d-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="eca6d-111">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="eca6d-111">Module properties</span></span>

- <span data-ttu-id="eca6d-112">**Rādīt mini grozu** — ja tas ir patiess, šis rekvizīts iespējo groza kopsavilkumu (mini grozs), kas tiks parādīts, kad atrodaties virs groza ikonas.</span><span class="sxs-lookup"><span data-stu-id="eca6d-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="eca6d-113">Šī funkcionalitāte tiek atbalstīta tikai darbvirsmas skatu portiem.</span><span class="sxs-lookup"><span data-stu-id="eca6d-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="eca6d-114">Groza ikonas moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="eca6d-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="eca6d-115">Lai pievienotu groza ikonas moduli, skatiet [Galvenes modulis](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="eca6d-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="eca6d-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="eca6d-116">Additional resources</span></span>

[<span data-ttu-id="eca6d-117">Pirkšanas lodziņa modulis</span><span class="sxs-lookup"><span data-stu-id="eca6d-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="eca6d-118">Groza modulis</span><span class="sxs-lookup"><span data-stu-id="eca6d-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="eca6d-119">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="eca6d-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="eca6d-120">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="eca6d-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="eca6d-121">Galvenes modulis</span><span class="sxs-lookup"><span data-stu-id="eca6d-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="eca6d-122">Kājenes modulis</span><span class="sxs-lookup"><span data-stu-id="eca6d-122">Footer module</span></span>](author-footer-module.md)
