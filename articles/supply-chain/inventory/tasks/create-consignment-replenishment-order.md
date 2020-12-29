---
title: Sūtījuma papildināšanas pasūtījuma izveide
description: Šajā tēmā aprakstīts, kā izveidot sūtījuma papildināšanas pasūtījumu, kur varat izsekot paredzamo piegādi no piegādātāja jūsu sūtījumu krājumos.
author: mkirknel
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e993190150e2d82088390d8db4b7c5ada2b0161
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433184"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="12a32-103">Sūtījuma papildināšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="12a32-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12a32-104">Šajā tēmā aprakstīts, kā izveidot sūtījuma papildināšanas pasūtījumu, kur varat izsekot paredzamo piegādi no piegādātāja jūsu sūtījumu krājumos.</span><span class="sxs-lookup"><span data-stu-id="12a32-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="12a32-105">Tajā ir arī parādīts kā reģistrēt preču saņemšanu, lai sūtījumu krājums ir reģistrēts kā rīcībā esošos krājums, kas pieder kreditoram.</span><span class="sxs-lookup"><span data-stu-id="12a32-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="12a32-106">Šo procedūru parasti veic sagādes speciālists.</span><span class="sxs-lookup"><span data-stu-id="12a32-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="12a32-107">Šo ceļvedi var izmantot demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="12a32-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="12a32-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="12a32-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="12a32-109">Sūtījuma papildināšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="12a32-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="12a32-110">Navigācijas rūtī ejiet uz **Moduļi > Iepirkumi un ārpakalpojumi > Sūtījums > Sūtījuma papildināšanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="12a32-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="12a32-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="12a32-111">Select **New**.</span></span>
3. <span data-ttu-id="12a32-112">Laukā **Piegādātāja konts** atlasiet piegādātāju **US-104** (jums jāizvēlas piegādātājs, kas ir reģistrēts kā īpašnieks lapā **krājumu īpašnieki** ).</span><span class="sxs-lookup"><span data-stu-id="12a32-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="12a32-113">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="12a32-113">Select **OK**.</span></span>
5. <span data-ttu-id="12a32-114">Atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="12a32-114">Select **Add line**.</span></span>
6. <span data-ttu-id="12a32-115">Laukā **Vienuma numurs** ierakstiet `M9211CI` (jums ir jāatlasa vienums, kas iestatīts sūtījuma krājumam).</span><span class="sxs-lookup"><span data-stu-id="12a32-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="12a32-116">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="12a32-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="12a32-117">Laukā **Pieprasītais piegādes datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="12a32-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="12a32-118">Pieprasītos un apstiprinātos datumus izmanto MRP programma preču saņemšanas paredzēšanai.</span><span class="sxs-lookup"><span data-stu-id="12a32-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="12a32-119">Laukā **Apstiprinātais piegādes datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="12a32-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="12a32-120">Izvērsiet sadaļu **Detalizēta informācija par rindu**.</span><span class="sxs-lookup"><span data-stu-id="12a32-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="12a32-121">Atlasiet cilni **Krājumu izmēri**.</span><span class="sxs-lookup"><span data-stu-id="12a32-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="12a32-122">Lai parādītu īpašnieku laukā **Krājumu izmēru īpašnieks**, atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="12a32-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="12a32-123">Kreditors US-104 tagad ir norādīts kā īpašnieks.</span><span class="sxs-lookup"><span data-stu-id="12a32-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="12a32-124">Pārbaudiet krājumu darbības statusu</span><span class="sxs-lookup"><span data-stu-id="12a32-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="12a32-125">Atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="12a32-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="12a32-126">Atlasiet **Darbības**.</span><span class="sxs-lookup"><span data-stu-id="12a32-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="12a32-127">Vajadzīgajā rindā ņemiet vērā, ka lauks **Saņemšana** ir iestatīts kā **Pasūtīts**.</span><span class="sxs-lookup"><span data-stu-id="12a32-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="12a32-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="12a32-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="12a32-129">Saņemt krājumus</span><span class="sxs-lookup"><span data-stu-id="12a32-129">Receive items</span></span>
1. <span data-ttu-id="12a32-130">Atlasiet **Preču ieejas plūsma**.</span><span class="sxs-lookup"><span data-stu-id="12a32-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="12a32-131">Laukā **Ārējā produkta saņemšana** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="12a32-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="12a32-132">Laukā **Daudzums** ievadiet skaitli, kas mazāks par tur parādīto skaitli.</span><span class="sxs-lookup"><span data-stu-id="12a32-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="12a32-133">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="12a32-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="12a32-134">Pārbaudiet rīcībā esošo krājumu</span><span class="sxs-lookup"><span data-stu-id="12a32-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="12a32-135">Atlasiet **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="12a32-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="12a32-136">Atlasiet **Rīcībā**.</span><span class="sxs-lookup"><span data-stu-id="12a32-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="12a32-137">Atlasiet **Pārskats**.</span><span class="sxs-lookup"><span data-stu-id="12a32-137">Select **Overview**.</span></span> <span data-ttu-id="12a32-138">Krājumus, kas tika saņemti kā sūtījumu krājumi, kas pieder kreditoram, ir pieejami rīcībā esoši.</span><span class="sxs-lookup"><span data-stu-id="12a32-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="12a32-139">Sūtījuma papildināšanas pasūtījuma atlikušais daudzums tiek rādīts laukā **Pasūtīts pavisam**.</span><span class="sxs-lookup"><span data-stu-id="12a32-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="12a32-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="12a32-140">Close the page.</span></span>

