---
title: Opcija Saņemt šo neparādās groza vai preces informācijas lapās
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja opcija saņemšanai veikalā netiek parādīta groza lapās vai preču informācijas lapās.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585426"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="05dcf-103">Opcija "Saņemt šo" neparādās groza vai preces informācijas lapās</span><span class="sxs-lookup"><span data-stu-id="05dcf-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05dcf-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja opcija saņemšanai veikalā netiek parādīta groza lapās vai preču informācijas lapās.</span><span class="sxs-lookup"><span data-stu-id="05dcf-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="05dcf-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="05dcf-105">Description</span></span>

<span data-ttu-id="05dcf-106">Poga **Saņemt šo** netiek parādīta groza vai preces informācijas lapās.</span><span class="sxs-lookup"><span data-stu-id="05dcf-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="05dcf-107">Attēlā zemāk parādīts lapas piemērs, kurā iekļauta poga **Saņemt šo**.</span><span class="sxs-lookup"><span data-stu-id="05dcf-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Poga Saņemt šo](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="05dcf-109">Novēršana</span><span class="sxs-lookup"><span data-stu-id="05dcf-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="05dcf-110">Iespējot BTOPS paplašinājumu Commerce vietnes veidotājā</span><span class="sxs-lookup"><span data-stu-id="05dcf-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="05dcf-111">Lai iespējotu "pirkt tiešsaistē, saņemt veikalā" (BOPIS) paplašinājumu Commerce vietnes veidotājā, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="05dcf-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="05dcf-112">Atlasiet savu vietni.</span><span class="sxs-lookup"><span data-stu-id="05dcf-112">Select your site.</span></span>
1. <span data-ttu-id="05dcf-113">Atlasiet **Vietnes iestatījumi** un pēc tam atlasiet **Paplašinājumi**.</span><span class="sxs-lookup"><span data-stu-id="05dcf-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="05dcf-114">Pārliecinieties, vai opcija **Atspējot BOPIS** ir notīrīta.</span><span class="sxs-lookup"><span data-stu-id="05dcf-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="05dcf-115">Piegādes veidu konfigurēšana programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="05dcf-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="05dcf-116">Lai konfigurētu piegādes veidus Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="05dcf-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="05dcf-117">Pārejiet uz sadaļu **Sagāde un avoti \> Iestatīšana \> Piegādes veidi**.</span><span class="sxs-lookup"><span data-stu-id="05dcf-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="05dcf-118">Pārliecinieties, ka ir izveidots piegādes veids **Izsniegšana klientam** un vai tam ir piešķirtas preces un adreses.</span><span class="sxs-lookup"><span data-stu-id="05dcf-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="05dcf-119">Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri**.</span><span class="sxs-lookup"><span data-stu-id="05dcf-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="05dcf-120">Kreisās puses navigācijā atlasiet **Klienta pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="05dcf-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="05dcf-121">Pārliecinieties, vai **Piegādes savākšanas veids** ir konfigurēts pareizi.</span><span class="sxs-lookup"><span data-stu-id="05dcf-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="05dcf-122">Klienta pasūtījumu maksājumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="05dcf-122">Configure customer orders payments</span></span>

<span data-ttu-id="05dcf-123">Lai konfigurētu klienta pasūtījumu maksājumus Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="05dcf-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="05dcf-124">Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri**.</span><span class="sxs-lookup"><span data-stu-id="05dcf-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="05dcf-125">Kreisās puses navigācijā atlasiet **Klienta pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="05dcf-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="05dcf-126">Kopsavilkuma cilnē **Maksājumi** pārliecinieties, vai lauki **Apmaksas nosacījumi** un **Maksāšanas metode** ir iestatīti pareizi.</span><span class="sxs-lookup"><span data-stu-id="05dcf-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05dcf-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="05dcf-127">Additional resources</span></span>

[<span data-ttu-id="05dcf-128">Konfigurēt BOPIS</span><span class="sxs-lookup"><span data-stu-id="05dcf-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="05dcf-129">Iespējot vairākus pasūtījuma piegādes veidus klientu pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="05dcf-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="05dcf-130">Universālā kanāla Commerce pasūtījumu maksājumi</span><span class="sxs-lookup"><span data-stu-id="05dcf-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="05dcf-131">Veikalu atlasītāja modulis</span><span class="sxs-lookup"><span data-stu-id="05dcf-131">Store selector module</span></span>](../store-selector.md)
