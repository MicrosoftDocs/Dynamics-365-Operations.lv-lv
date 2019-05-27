---
title: Cenu korekcijas un atlaides
description: Šajā rakstā ir sniegta informācija par cenu korekcijām un atlaidēm programmā Microsoft Dynamics 365 for Retail.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 61ac8e5fbdc4d91bb5bc5372a7fb96633043473a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549456"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="f11f0-103">Cenu korekcijas un atlaides</span><span class="sxs-lookup"><span data-stu-id="f11f0-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f11f0-104">Šajā rakstā ir sniegta informācija par cenu korekcijām un atlaidēm programmā Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f11f0-104">This article provides information about price adjustments and discounts in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="f11f0-105">Programmā Dynamics 365 for Retail varat veikt preču cenu korekcijas, kā arī iestatīt atlaides, kas tiek lietotas rindas krājumam vai transakcijai pārdošanas punktā (POS), zvanu centra pārdošanas pasūtījumā vai tiešsaistes pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="f11f0-105">In Dynamics 365 for Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="f11f0-106">Gan cenu korekcijas, gan atlaides var saistīt ar cenu grupām.</span><span class="sxs-lookup"><span data-stu-id="f11f0-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="f11f0-107">Gan cenu korekcijām, gan atlaidēm var norādīt vienu sākuma datumu un beigu datumu vai atkārtošanās periodu, atlaides kodu un dažus papildu atribūtus.</span><span class="sxs-lookup"><span data-stu-id="f11f0-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="f11f0-108">Cenu korekcijas un atlaides var lietot precēm, variantiem vai kategorijām.</span><span class="sxs-lookup"><span data-stu-id="f11f0-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="f11f0-109">Ja precei tiek lietotas vairākas atlaides, debitors var saņemt vienu no atlaidēm vai kombinētu atlaidi atkarībā no konta konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="f11f0-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="f11f0-110">Dynamics 365 for Retail automātiski lieto to atlaidi vai atlaižu kombināciju, kas nodrošina debitoram izdevīgāko cenu.</span><span class="sxs-lookup"><span data-stu-id="f11f0-110">Dynamics 365 for Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="f11f0-111">Iestatot cenas korekciju vai atlaidi, pārliecinieties, lai akceptētu, ka cenu grupas ir piešķirtas pareizo kanālus, katalogus, piederības vai lojalitātes programmas, kuras vēlaties piemērot atlaidi.</span><span class="sxs-lookup"><span data-stu-id="f11f0-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="f11f0-112">Turklāt, ja vēlaties automātiski ģenerēt atlaides ID, pirms jaunas cenas korekcijas vai atlaides definēšanas iestatiet numuru sērijas lapā **Mazumtirdzniecības rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="f11f0-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="f11f0-113">Varat dzēst cenas korekciju vai atlaidi.</span><span class="sxs-lookup"><span data-stu-id="f11f0-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="f11f0-114">Taču tādējādi tiek zaudēta statistiskā informācija.</span><span class="sxs-lookup"><span data-stu-id="f11f0-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="f11f0-115">Atlaižu vedi</span><span class="sxs-lookup"><span data-stu-id="f11f0-115">Types of discounts</span></span>

<span data-ttu-id="f11f0-116">Ir pieejami četri mazumtirdzniecības atlaižu veidi.</span><span class="sxs-lookup"><span data-stu-id="f11f0-116">There are four types of retail discounts:</span></span>

- <span data-ttu-id="f11f0-117">**Vienkārša atlaide** — viena procentuālā vērtība vai summa.</span><span class="sxs-lookup"><span data-stu-id="f11f0-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="f11f0-118">**Daudzuma atlaide** — atlaide, kas tiek lietota, ja tiek pirktas divas preces vai vairāk.</span><span class="sxs-lookup"><span data-stu-id="f11f0-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="f11f0-119">**Komplekta piedāvājuma atlaide** — atlaide, kas tiek lietota, ja tiek nopirkta noteikta preču kombinācija.</span><span class="sxs-lookup"><span data-stu-id="f11f0-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="f11f0-120">**Sliekšņa atlaide** — atlaide, kas tiek lietota, ja transakcijas kopsumma pārsniedz noteiktu summu.</span><span class="sxs-lookup"><span data-stu-id="f11f0-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="f11f0-121">Gan cenu korekcijas, gan atlaides var saistīt ar cenu grupām.</span><span class="sxs-lookup"><span data-stu-id="f11f0-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="f11f0-122">Pēc tam cenu grupas var saistīt ar kanāliem, kategorijām, piederībām un lojalitātes programmām.</span><span class="sxs-lookup"><span data-stu-id="f11f0-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
