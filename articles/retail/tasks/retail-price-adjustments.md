---
title: " Mazumtirdzniecības cenu korekcijas"
description: Šajā procedūrā aprakstīts, kā izveidot mazumtirdzniecības cenas korekciju.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9427d3955e5442e301c416e2960e071ca5d85a3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550032"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="5e6b3-103"> Mazumtirdzniecības cenu korekcijas</span><span class="sxs-lookup"><span data-stu-id="5e6b3-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5e6b3-104">Šajā procedūrā aprakstīts, kā izveidot mazumtirdzniecības cenas korekciju.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="5e6b3-105">Mazumtirdzniecības cenas korekciju var iestatīt tieši krājuma pārdošanas cenā, vai modificējot pārdošanas pamatcenu vai tirdzniecības līguma pārdošanas cenu.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="5e6b3-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="5e6b3-107">Noklikšķiniet uz Izcenojuma un atlaižu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="5e6b3-108">Noklikšķiniet uz cilnes Cenas korekcija.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="5e6b3-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-109">Click New.</span></span>
    * <span data-ttu-id="5e6b3-110">No šejienes varat izveidot visas visbiežāk izmantotās cenu un atlaižu kārtulas, tostarp mazumtirdzniecības atlaides, cenas korekciju, tirdzniecības līgumu žurnālus un kategorijas cenu noteikšanas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="5e6b3-111">Noklikšķiniet uz Cenas korekcija.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="5e6b3-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="5e6b3-113">Izvērsiet sadaļu Rindas.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="5e6b3-114">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-114">Click Add.</span></span>
    * <span data-ttu-id="5e6b3-115">Šajā piemērā laukā Prece ievadiet 81126.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="5e6b3-116">Pēc tam laukā Atlaide procentos ievadiet 10,0.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="5e6b3-117">Atlaides procentuālās vērtības veida cenas korekcija samazinās pārdošanas pamatcenu vai tirdzniecības līguma pārdošanas cenu.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="5e6b3-118">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-118">Click Add.</span></span>
    * <span data-ttu-id="5e6b3-119">Šajā piemērā laukā Prece ievadiet 81125.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="5e6b3-120">Pēc tam laukā Atlaides metode atlasiet Termiņatlaides summa.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="5e6b3-121">Laukā Termiņatlaides summa ievadiet 5,0.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="5e6b3-122">Termiņatlaides summas atlaides veids ir summa, kas iegūta no pamatcenas vai tirdzniecības līguma cenas.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="5e6b3-123">Noklikšķiniet uz Cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-123">Click Price groups.</span></span>
    * <span data-ttu-id="5e6b3-124">Laukā Cenu grupa atlasiet RP-Houston.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="5e6b3-125">Tādējādi cenas korekcija tiks piesaistīta Houston veikalam.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="5e6b3-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-126">Click Save.</span></span>
11. <span data-ttu-id="5e6b3-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-127">Close the page.</span></span>
12. <span data-ttu-id="5e6b3-128">Laukā Statuss atlasiet Iespējots.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="5e6b3-129">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-129">Click Save.</span></span>
14. <span data-ttu-id="5e6b3-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-130">Close the page.</span></span>
15. <span data-ttu-id="5e6b3-131">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="5e6b3-131">Refresh the page.</span></span>

