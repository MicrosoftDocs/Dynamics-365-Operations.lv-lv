---
title: Tiešsaistes pasūtījumu nodokļi nav pareizi aprēķināti
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja tiešsaistes pasūtījumu nodokļi tiek nepareizi aprēķināti vai ja nodokļu grupa nav pareizi iestatīta pārdošanas rindā.
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
ms.openlocfilehash: 421df7545e285950ef8a3c4b753c8c6dc5f26422
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585425"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="c0410-103">Tiešsaistes pasūtījumu nodokļi nav pareizi aprēķināti</span><span class="sxs-lookup"><span data-stu-id="c0410-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c0410-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja tiešsaistes pasūtījumu nodokļi tiek nepareizi aprēķināti vai ja nodokļu grupa nav pareizi iestatīta pārdošanas rindā.</span><span class="sxs-lookup"><span data-stu-id="c0410-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="c0410-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="c0410-105">Description</span></span>

<span data-ttu-id="c0410-106">Kad tiek veikts e-komercijas pasūtījums, nodokļi ir nepareizi aprēķināti vai nodokļu grupa ir nepareizi iestatīta pārdošanas rindā.</span><span class="sxs-lookup"><span data-stu-id="c0410-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="c0410-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="c0410-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="c0410-108">Pārdošanas nodokļa konfigurēšana mazumtirdzniecības veikalam programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="c0410-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="c0410-109">Lai konfigurētu pārdošanas nodokli mazumtirdzniecības veikalam programmā Commerce Headquarters, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="c0410-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c0410-110">Dodieties uz **Mazumtirdzniecība un komercija \> Kanāli \> Visi mazumtirdzniecības veikali**.</span><span class="sxs-lookup"><span data-stu-id="c0410-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="c0410-111">Atlasiet veikalu, kuram konfigurēt pārdošanas nodokli.</span><span class="sxs-lookup"><span data-stu-id="c0410-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="c0410-112">Kopsavilkuma cilnes **Vispārīgi** sadaļā **Pārdošanas nodoklis** konfigurējiet veikala pārdošanas nodokļa informāciju.</span><span class="sxs-lookup"><span data-stu-id="c0410-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="c0410-113">Preču savākšanai no veikala pārdošanas nodokļa grupa tiek ņemta no veikala, kas ir atlasīts savākšanai.</span><span class="sxs-lookup"><span data-stu-id="c0410-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="c0410-114">Papildinformāciju skatiet sadaļā [Citu veikaliem pieejamo nodokļu opciju iestatīšana](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="c0410-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="c0410-115">Pārdošanas nodokļa konfigurēšana debitora adresei programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="c0410-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="c0410-116">Lai konfigurētu pārdošanas nodokli debitora adresei programmā Commerce Headquarters, izpildiet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="c0410-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c0410-117">Dodieties uz **Debitoru parādi \> Debitori \> Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="c0410-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="c0410-118">Izvēlieties debitoru, kuram konfigurēt pārdošanas nodokli.</span><span class="sxs-lookup"><span data-stu-id="c0410-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="c0410-119">Kopsavilkuma cilnē **Adreses** atlasiet adresi, kurai konfigurēt pārdošanas nodokli, atlasiet  **Papildu opcijas** un pēc tam atlasiet **Papildus**.</span><span class="sxs-lookup"><span data-stu-id="c0410-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="c0410-120">Kopsavilkuma cilnē **Vispārīgi** atlasiet **Nodokļu grupa**.</span><span class="sxs-lookup"><span data-stu-id="c0410-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="c0410-121">Laukā **Pārdošanas nodoklis** atlasiet atbilstošo vērtību.</span><span class="sxs-lookup"><span data-stu-id="c0410-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="c0410-122">Nosūtīšanai, kas ietver pārdošanas nodokli debitora adresē, rindas piegādes adrese nosaka rindas nodokļu grupu.</span><span class="sxs-lookup"><span data-stu-id="c0410-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="c0410-123">Ja debitors veic piegādi uz esošu adresi, kam jau ir konfigurēta nodokļu grupa, tiks izmantota esošā nodokļu grupa.</span><span class="sxs-lookup"><span data-stu-id="c0410-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="c0410-124">Pēc noklusējuma adresēm, kad tās tiek izveidotas, nav nodokļu grupas.</span><span class="sxs-lookup"><span data-stu-id="c0410-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="c0410-125">Vispārīgo pārdošanas nodokļa grupu konfigurēšana programmā Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="c0410-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="c0410-126">Lai konfigurētu vispārīgas pārdošanas nodokļa grupas Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c0410-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c0410-127">Dodieties uz **Nodokļi \> Netiešie nodokļi \> Pārdošanas nodoklis \> Pārdošanas nodokļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="c0410-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="c0410-128">Navigācijas kreisajā pusē atlasiet konfigurējamo nodokļu grupu.</span><span class="sxs-lookup"><span data-stu-id="c0410-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="c0410-129">Kopsavilkuma cilnē **Mazumtirdzniecības mērķis, balstoties uz nodokli**, konfigurējiet pārdošanas nodokļa grupas nodokļus.</span><span class="sxs-lookup"><span data-stu-id="c0410-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="c0410-130">Piegādei, kas neietver pārdošanas nodokli debitora adresē, rindas piegādes adrese un mērķa nodokļi, kas ir konfigurēti nodokļu grupai, nosaka nodokļu grupu.</span><span class="sxs-lookup"><span data-stu-id="c0410-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="c0410-131">Lai iegūtu papildu informāciju, skatiet sadaļu [Nodokļu iestatīšana tiešsaistes veikaliem, kas balstīti uz mērķi](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="c0410-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0410-132">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c0410-132">Additional resources</span></span>

[<span data-ttu-id="c0410-133">PVN tiešsaistes pasūtījumiem konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c0410-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)