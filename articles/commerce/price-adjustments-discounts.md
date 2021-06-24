---
title: Cenu korekcijas un atlaides
description: Šajā rakstā ir sniegta informācija par cenu korekcijām un atlaidēm programmā Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240946"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="bbbbc-103">Cenu korekcijas un atlaides</span><span class="sxs-lookup"><span data-stu-id="bbbbc-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bbbbc-104">Šajā rakstā ir sniegta informācija par cenu korekcijām un atlaidēm programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bbbbc-105">Programmā Commerce varat veikt preču cenu korekcijas, kā arī iestatīt atlaides, kas tiek lietotas rindas krājumam vai transakcijai pārdošanas punktā (POS), zvanu centra pārdošanas pasūtījumā vai tiešsaistes pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="bbbbc-106">Gan cenu korekcijas, gan atlaides var saistīt ar cenu grupām.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="bbbbc-107">Gan cenu korekcijām, gan atlaidēm var norādīt vienu sākuma datumu un beigu datumu vai atkārtošanās periodu, atlaides kodu un dažus papildu atribūtus.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="bbbbc-108">Cenu korekcijas un atlaides var lietot precēm, variantiem vai kategorijām.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="bbbbc-109">Ja precei tiek lietotas vairākas atlaides, debitors var saņemt vienu no atlaidēm vai kombinētu atlaidi atkarībā no konta konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="bbbbc-110">Commerce automātiski lieto to atlaidi vai atlaižu kombināciju, kas nodrošina debitoram izdevīgāko cenu.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="bbbbc-111">Iestatot cenas korekciju vai atlaidi, pārliecinieties, lai akceptētu, ka cenu grupas ir piešķirtas pareizo kanālus, katalogus, piederības vai lojalitātes programmas, kuras vēlaties piemērot atlaidi.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="bbbbc-112">Turklāt, ja vēlaties automātiski ģenerēt atlaides ID, pirms jaunas cenas korekcijas vai atlaides definēšanas iestatiet numuru sērijas lapā **Commerce rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="bbbbc-113">Varat dzēst cenas korekciju vai atlaidi.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="bbbbc-114">Taču tādējādi tiek zaudēta statistiskā informācija.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="bbbbc-115">Atlaižu vedi</span><span class="sxs-lookup"><span data-stu-id="bbbbc-115">Types of discounts</span></span>

<span data-ttu-id="bbbbc-116">Ir pieejami daudz atlaižu veidi:</span><span class="sxs-lookup"><span data-stu-id="bbbbc-116">There are many types of discounts:</span></span>

- <span data-ttu-id="bbbbc-117">**Vienkārša atlaide** — viena procentuālā vērtība vai summa.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="bbbbc-118">**Daudzuma atlaide** — atlaide, kas tiek lietota, ja tiek pirktas divas preces vai vairāk.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="bbbbc-119">**Komplekta piedāvājuma atlaide** — atlaide, kas tiek lietota, ja tiek nopirkta noteikta preču kombinācija.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="bbbbc-120">**Sliekšņa atlaide** — atlaide, kas tiek lietota, ja transakcijas kopsumma pārsniedz noteiktu summu.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="bbbbc-121">**Uz piedāvājumu balstīta atlaide** – atlaide, kas tiek piemērota, kad darbības kopsumma ir lielāka par norādīto summu un apmaksai tiek izmantots noteikts maksājuma tips (piemēram, skaidra nauda, kredītkarte vai debetkarte).</span><span class="sxs-lookup"><span data-stu-id="bbbbc-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="bbbbc-122">**Nosūtīšanas atlaide** – atlaide, kas tiek piemērota, kad darbības kopsumma ir lielāka par norādīto summu un pasūtījumā tiek izmantots noteikts piegādes veids (piemēram, divu dienu piegāde vai nakts piegāde).</span><span class="sxs-lookup"><span data-stu-id="bbbbc-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="bbbbc-123">Gan cenu korekcijas, gan atlaides var saistīt ar cenu grupām.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="bbbbc-124">Pēc tam cenu grupas var saistīt ar kanāliem, kategorijām, piederībām un lojalitātes programmām.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="bbbbc-125">Komplekta atlaidei un sliekšņa atlaidei ir rekvizīti ar nosaukumu “Saskaitīt preces, kam nevar piemērot atlaidi” un “Saskaitīt preces, kam nevar piemērot atlaidi, sasniedzot sliekšņa atlaidi”.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="bbbbc-126">Ja šie rekvizīti ir iespējoti, krājums, kas nav piemērots nevienai atlaidei, joprojām var palīdzēt kvalificēt transakciju atlaides saņemšanai, tomēr neatbilstošais krājums atlaidi nesaņems.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="bbbbc-127">Piemēram, ja tiek izveidota komplekta atlaide ar divām rindām, A un B, kur debitoram vajadzētu iegūt 10% atlaidi abiem krājumiem, bet krājumam A ir atzīmēta konfigurācija “Liegt visas atlaides”, tad krājums A šajā gadījumā netiktu iekļauts atlaidē.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="bbbbc-128">Tomēr, ja ir iespējots rekvizīts “Saskaitīt preces, kam nevar piemērot atlaidi”, tad A krājumu var izmantot, lai kvalificētos komplekta atlaidei, bet 10% atlaide tiks piemērota tikai krājumam B. Līdzīga loģika attiecas uz sliekšņa atlaidi.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="bbbbc-129">Tomēr rekvizītam “Saskaitīt preces, kam nevar piemērot atlaidi, sasniedzot sliekšņa atlaidi” ir vairāk iespēju, salīdzinot ar komplekta atlaižu rekvizītu “Saskaitīt preces, kam nevar piemērot atlaidi”.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="bbbbc-130">Ja ir iespējota sliekšņa atlaide un ja ir krājums ar jau esošu atlaidi, kas liegtu krājumam iegūt citas atlaides, tad par šo krājumu samaksātā cena kvalificēsies sliekšņa atlaidei, bet šim krājumam netiks piemērota papildu atlaide.</span><span class="sxs-lookup"><span data-stu-id="bbbbc-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
