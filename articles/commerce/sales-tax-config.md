---
title: Konfigurēt PVN tiešsaistes pasūtījumiem
description: Šajā tēmā sniegts pārskats par PVN grupas atlasi dažādiem tiešsaistes pasūtījumu veidiem risinājumā Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254845"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="e1fe7-103">Konfigurēt PVN tiešsaistes pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="e1fe7-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1fe7-104">Šajā tēmā sniegts pārskats par PVN grupas atlasi dažādiem tiešsaistes pasūtījumu veidiem risinājumā.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="e1fe7-105">Jūsu e-tirdzniecības kanāls var vēlēties atbalstīt opcijas, piemēram, piegādāšanu vai saņemšanu tiešsaistes pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="e1fe7-106">PVN piemērojamība ir balstīta uz opciju, ko atlasa tiešsaistes lietotāji.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="e1fe7-107">Kad vietnes klients izvēlas nopirkt preci tiešsaistē un saņem to ar sūtīšanu pa pastu, PVN tiek noteikts, pamatojoties uz klienta piegādes adreses nodokļu grupas iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="e1fe7-108">Kad klients vēlas saņemt nopirkto preci veikalā, PVN tiek noteikts, pamatojoties uz saņemšanas veikala nodokļu grupas iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="e1fe7-109">Pasūtījumi, kas nosūtīti uz klienta adresi</span><span class="sxs-lookup"><span data-stu-id="e1fe7-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="e1fe7-110">Parasti nodokļus tiešsaistes pasūtījumiem, kas nosūtāmi uz klienta adresēm, definē adresāts.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="e1fe7-111">Katrai PVN grupai ir mazumtirdzniecības mērķa nodokļu konfigurācija, kurā jūsu uzņēmums var definēt adresāta informāciju, piemēram, apgabals/reģions, rajons, apgabals un pilsēta hierarhiskā formā.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="e1fe7-112">Kad tiek veikts tiešsaistes pasūtījums, Commerce nodokļu programma izmanto katra pasūtījuma rindas krājuma piegādes adresi un atrod PVN grupas, kas atbilst ar mērķi balstītus nodokļu kritērijus.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="e1fe7-113">Piemēram, tiešsaistes pasūtījumam ar rindas krājuma piegādes adresi uz Sanfrancisko, Kalifornijā, nodokļu programma atradīs PVN grupu un PVN kodu Kalifornijā un tad aprēķiniet nodokli katram rindas krājumam atbilstoši.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="e1fe7-114">Uz klientu balstītas nodokļu grupas</span><span class="sxs-lookup"><span data-stu-id="e1fe7-114">Customer-based tax groups</span></span>

<span data-ttu-id="e1fe7-115">Commerce Headquarters ir divas vietas, kur ir konfigurētas klientu nodokļu grupas:</span><span class="sxs-lookup"><span data-stu-id="e1fe7-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="e1fe7-116">**Klienta profils**</span><span class="sxs-lookup"><span data-stu-id="e1fe7-116">**Customer's profile**</span></span>
- <span data-ttu-id="e1fe7-117">**Klienta sūtīšanas adrese**</span><span class="sxs-lookup"><span data-stu-id="e1fe7-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="e1fe7-118">Ja klienta profilam ir konfigurēta nodokļu grupa</span><span class="sxs-lookup"><span data-stu-id="e1fe7-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="e1fe7-119">Klienta profila ierakstam galvenajā birojā var būt konfigurēta PVN grupa, tomēr tiešsaistes pasūtījumiem PVN grupa, kas konfigurēta klienta profilā, netiks izmantota nodokļu programmai.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="e1fe7-120">Ja klienta sūtīšanas adresei ir konfigurēta nodokļu grupa</span><span class="sxs-lookup"><span data-stu-id="e1fe7-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="e1fe7-121">Ja klienta piegādes adreses ierakstam ir konfigurēta nodokļu grupa un tiešsaistes pasūtījums (vai rindas vienums) tiek nosūtīts uz klienta sūtīšanas adresi, nodokļu grupa, kas konfigurēta klienta adreses ierakstā, tiks izmantota nodokļu aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="e1fe7-122">Konfigurēt nodokļu grupu klienta sūtīšanas adreses ierakstam</span><span class="sxs-lookup"><span data-stu-id="e1fe7-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="e1fe7-123">Lai konfigurētu nodokļu grupu klienta sūtīšanas adreses ierakstam sadaļā Commerce Headquarters, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e1fe7-124">Dodieties uz **Visi klienti** un pēc tam atlasiet vēlamo klientu.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="e1fe7-125">Kopsavilkuma cilnē **Adreses** atlasiet vēlamo adresi un pēc tam atlasiet **Papildu opcijas \> Papildus**.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="e1fe7-126">Cilnes **Vispārīgi** lapā **Pārvaldīt adreses** iestatiet PVN vērtību pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="e1fe7-127">Nodokļu grupa ir definēta, izmantojot pasūtījuma rindas sūtīšanas adresi, un ar mērķi balstīti nodokļi ir konfigurēti pašā nodokļu grupā.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="e1fe7-128">Lai iegūtu papildu informāciju, skatiet sadaļu [Nodokļu iestatīšana tiešsaistes veikaliem, kas balstīti uz mērķi](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="e1fe7-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="e1fe7-129">Pasūtījuma saņemšana veikalā</span><span class="sxs-lookup"><span data-stu-id="e1fe7-129">Order pickup in store</span></span>

<span data-ttu-id="e1fe7-130">Pasūtījuma rindām ar saņemšanu veikalā vai saņemšanu pa ceļam tiek lietota atlasītā saņemšanas veikala nodokļu grupa.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="e1fe7-131">Papildinformāciju par to, kā konfigurēt nodokļu grupu noteiktam veikalam, skatiet sadaļā [Citu nodokļu opciju iestatīšana veikaliem](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="e1fe7-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="e1fe7-132">Kad pasūtījuma rinda tiek saņemta veikalā, tiek lietots klienta adreses nodokļa iestatījums (ja iestatīts), un tiks izmantota saņemšanas veikala nodokļa konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="e1fe7-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e1fe7-133">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e1fe7-133">Additional resources</span></span>

[<span data-ttu-id="e1fe7-134">PVN pārskats</span><span class="sxs-lookup"><span data-stu-id="e1fe7-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="e1fe7-135">PVN aprēķināšanas metodes laukā Izcelsme</span><span class="sxs-lookup"><span data-stu-id="e1fe7-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="e1fe7-136">PVN piešķire un pārrakstīšana</span><span class="sxs-lookup"><span data-stu-id="e1fe7-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="e1fe7-137">Visas summas un intervāla aprēķināšanas opcijas PVN kodiem</span><span class="sxs-lookup"><span data-stu-id="e1fe7-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="e1fe7-138">Nodokļa atbrīvojuma aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="e1fe7-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]