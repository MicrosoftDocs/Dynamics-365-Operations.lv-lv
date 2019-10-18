---
title: Fiziskie un finanšu atjauninājumi
description: Šajā tēmā ir sniegts pārskats par to, kāda veida darbības palielina vai samazina krājumu daudzumu.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4360f9132d31c9d0038f51c68c1f6c3fcaaa2025
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250874"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="d18d4-103">Fiziskie un finanšu atjauninājumi</span><span class="sxs-lookup"><span data-stu-id="d18d4-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d18d4-104">Šajā tēmā ir sniegts pārskats par to, kāda veida darbības palielina vai samazina krājumu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d18d4-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="d18d4-105">Programmā Dynamics 365 Supply Chain Management var fiziski un finansiāli atjaunināt krājumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="d18d4-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d18d4-106">Dažu tipu fiziskās un finanšu transakcijas palielina daudzumu, bet citas daudzumu samazina.</span><span class="sxs-lookup"><span data-stu-id="d18d4-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="d18d4-107">Fizisks palielinājums</span><span class="sxs-lookup"><span data-stu-id="d18d4-107">Physical increases</span></span>
<span data-ttu-id="d18d4-108">Kad fiziska transakcija tiek iegrāmatota, transakcijas ieraksta statuss ir **Saņemts**.</span><span class="sxs-lookup"><span data-stu-id="d18d4-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="d18d4-109">Turpmāk minētās transakcijas tiek uzskatītas par fizisku palielinājumu:</span><span class="sxs-lookup"><span data-stu-id="d18d4-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="d18d4-110">Pirkšanas pasūtījuma ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="d18d4-110">Purchase order receipt</span></span>
-   <span data-ttu-id="d18d4-111">Pārdošanas pasūtījuma pavadzīmes atgriešana</span><span class="sxs-lookup"><span data-stu-id="d18d4-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="d18d4-112">Ražošanas pasūtījuma atzīmēšana kā pabeigta</span><span class="sxs-lookup"><span data-stu-id="d18d4-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="d18d4-113">Blakusprodukts ražošanas pasūtījuma izdošanas sarakstā</span><span class="sxs-lookup"><span data-stu-id="d18d4-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="d18d4-114">Finansiāls palielinājums</span><span class="sxs-lookup"><span data-stu-id="d18d4-114">Financial increases</span></span>
<span data-ttu-id="d18d4-115">Kad finansiālas ieejas plūsmas transakcija tiek iegrāmatota, transakcijas ieraksta, kas palielina daudzumu, statuss ir **Nopirkts**.</span><span class="sxs-lookup"><span data-stu-id="d18d4-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="d18d4-116">Turpmāk minētās transakcijas tiek uzskatītas par finansiālu palielinājumu:</span><span class="sxs-lookup"><span data-stu-id="d18d4-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="d18d4-117">Kreditora rēķins</span><span class="sxs-lookup"><span data-stu-id="d18d4-117">Vendor invoice</span></span>
-   <span data-ttu-id="d18d4-118">Pārdošanas pasūtījuma rēķins par atgriešanu</span><span class="sxs-lookup"><span data-stu-id="d18d4-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="d18d4-119">Ražošanas pasūtījuma izmaksu aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="d18d4-119">Production order costing</span></span>
-   <span data-ttu-id="d18d4-120">Pozitīva daudzuma krājumu žurnāli, tādi kā pārvietošana, pelņa un zaudējumi, uzskaite, materiālu komplekti un pārsūtīšana</span><span class="sxs-lookup"><span data-stu-id="d18d4-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="d18d4-121">Darbības, kas palielina daudzumu</span><span class="sxs-lookup"><span data-stu-id="d18d4-121">Transactions that increase quantity</span></span>
<span data-ttu-id="d18d4-122">Darbības, kas palielina daudzumu, tiek grāmatotas, norādot kārtējo vidējo pašizmaksu.</span><span class="sxs-lookup"><span data-stu-id="d18d4-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="d18d4-123">Aprēķinātā kārtējā vidējā pašizmaksa ir pamatota uz katras transakcijas maksu par katru krājuma dimensiju, kas tiek finansiāli izsekota.</span><span class="sxs-lookup"><span data-stu-id="d18d4-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="d18d4-124">Informāciju par kārtējo vidējo pašizmaksu skatiet [Kārtējā vidējā pašizmaksa](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="d18d4-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="d18d4-125">Darbības, kas samazina daudzumu</span><span class="sxs-lookup"><span data-stu-id="d18d4-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="d18d4-126">Neatkarīgi no tā, kurš krājumu modelis ir saistīts ar attiecīgo krājumu, aprēķinātā kārtējā vidējā pašizmaksa tiek izmantota, grāmatojot darbību, kas samazina daudzumu.</span><span class="sxs-lookup"><span data-stu-id="d18d4-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="d18d4-127">Ir nepieciešams, lai transakcija, kas samazina daudzumu, pirms grāmatošanas nebūtu iepriekš atzīmēta citai transakcijai.</span><span class="sxs-lookup"><span data-stu-id="d18d4-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="d18d4-128">Ja fiziski rīcībā esošo krājumu daudzums kļūst par negatīvu skaitli, tiek izmantotas krājumu izmaksas, kas definētas krājumam formā **Krājums**.</span><span class="sxs-lookup"><span data-stu-id="d18d4-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="d18d4-129">Ja ir iespējota vairākvietu funkcionalitāte, šīs izmaksas būs krājumu izmaksas, kas definētas vietai lapā **Pasūtījuma noklusējuma iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="d18d4-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="d18d4-130">Fiziska izdošana un finansiāla izdošana</span><span class="sxs-lookup"><span data-stu-id="d18d4-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="d18d4-131">Kad fiziskas izejas plūsmas transakcija tiek iegrāmatota, transakcijas ieraksta statuss ir **Atskaitīts**.</span><span class="sxs-lookup"><span data-stu-id="d18d4-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="d18d4-132">Turpmāk minētās transakcijas tiek uzskatītas par fiziskām izejas plūsmām:</span><span class="sxs-lookup"><span data-stu-id="d18d4-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="d18d4-133">Ražošanas pasūtījuma izdošanas saraksta žurnāls</span><span class="sxs-lookup"><span data-stu-id="d18d4-133">Production order picking list journal</span></span>
-   <span data-ttu-id="d18d4-134">Pārdošanas pasūtījuma pavadzīme</span><span class="sxs-lookup"><span data-stu-id="d18d4-134">Sales order packing slip</span></span>
-   <span data-ttu-id="d18d4-135">Pirkšanas pasūtījuma pavadzīmes atgriešana</span><span class="sxs-lookup"><span data-stu-id="d18d4-135">Purchase order packing slip return</span></span>

<span data-ttu-id="d18d4-136">Kad finansiāla transakcija tiek iegrāmatota, transakcijas ieraksta statuss ir **Pārdots**.</span><span class="sxs-lookup"><span data-stu-id="d18d4-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="d18d4-137">Turpmāk minētās transakcijas tiek uzskatītas par finansiālām izejas plūsmām:</span><span class="sxs-lookup"><span data-stu-id="d18d4-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="d18d4-138">Ražošanas pasūtījuma pabeigšana</span><span class="sxs-lookup"><span data-stu-id="d18d4-138">Ending a production order</span></span>
-   <span data-ttu-id="d18d4-139">Pārdošanas pasūtījuma rēķins</span><span class="sxs-lookup"><span data-stu-id="d18d4-139">Sales order invoice</span></span>
-   <span data-ttu-id="d18d4-140">Kreditora rēķina atgriešana</span><span class="sxs-lookup"><span data-stu-id="d18d4-140">Vendor invoice return</span></span>
-   <span data-ttu-id="d18d4-141">Negatīva daudzuma krājumu žurnāli, tādi kā pārvietošana, pelņa un zaudējumi, uzskaite, materiālu komplekti un pārsūtīšana</span><span class="sxs-lookup"><span data-stu-id="d18d4-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="d18d4-142">Darbības, kas samazina daudzumu, tiek grāmatotas, norādot pašreizējo vidējo pašizmaksu.</span><span class="sxs-lookup"><span data-stu-id="d18d4-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="d18d4-143">Līdz ar to, lai izdošanas transakcijas segtu ar saņemšanas darbībām, pamatojoties uz katram krājumam piešķirto krājumu modeli, ir nepieciešama krājumu slēgšanas procedūra.</span><span class="sxs-lookup"><span data-stu-id="d18d4-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>
