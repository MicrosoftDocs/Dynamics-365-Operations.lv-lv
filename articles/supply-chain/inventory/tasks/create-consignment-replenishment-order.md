---
title: Sūtījuma papildināšanas pasūtījuma izveide
description: Šajā procedūrā parādīts kā izveidot jaunu sūtījuma papildināšanas pasūtījumu, lai jūs varētu izsekot paredzēto piegādi no kreditora jūsu sūtījumu krājumā.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cf2e8f742fee2dedaac72902d207af0081700ca
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845550"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="2aa4e-103">Sūtījuma papildināšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="2aa4e-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2aa4e-104">Šajā procedūrā parādīts kā izveidot jaunu sūtījuma papildināšanas pasūtījumu, lai jūs varētu izsekot paredzēto piegādi no kreditora jūsu sūtījumu krājumā.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="2aa4e-105">Tajā ir arī parādīts kā reģistrēt preču saņemšanu, lai sūtījumu krājums ir reģistrēts kā rīcībā esošos krājums, kas pieder kreditoram.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="2aa4e-106">Šo procedūru parasti veic sagādes speciālists.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="2aa4e-107">Šo ceļvedi var izmantot demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="2aa4e-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="2aa4e-109">Sūtījuma papildināšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="2aa4e-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="2aa4e-110">Dodieties uz Sagāde un avoti > Sūtījums > Sūtījuma papildināšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="2aa4e-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-111">Click New.</span></span>
3. <span data-ttu-id="2aa4e-112">Laukā Kreditora konts atlasiet kreditoru US-104.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="2aa4e-113">Nepieciešams atlasīt kreditoru, kas ir reģistrēts kā īpašnieks lapā Krājumu īpašnieki.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="2aa4e-114">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-114">Click OK.</span></span>
5. <span data-ttu-id="2aa4e-115">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-115">Click Add line.</span></span>
6. <span data-ttu-id="2aa4e-116">Laukā Krājuma kods ierakstiet M9211CI.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="2aa4e-117">Atlasiet vienumu, kas ir iestatīts sūtījuma krājumam.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="2aa4e-118">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="2aa4e-119">Laukā Pieprasītais piegādes datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="2aa4e-120">Pieprasītos un apstiprinātos datumus izmanto MRP programma preču saņemšanas paredzēšanai.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="2aa4e-121">Laukā Apstiprinātais piegādes datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="2aa4e-122">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="2aa4e-123">Noklikšķiniet uz cilnes Krājumu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="2aa4e-124">Atsvaidziniet lapu, lai parādītu īpašnieku laukā Krājuma dimensijas īpašnieks.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="2aa4e-125">Kreditors US-104 tagad ir norādīts kā īpašnieks.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="2aa4e-126">Pārbaudiet krājumu darbības statusu</span><span class="sxs-lookup"><span data-stu-id="2aa4e-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="2aa4e-127">Noklikšķiniet uz Krājumi.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-127">Click Inventory.</span></span>
2. <span data-ttu-id="2aa4e-128">Noklikšķiniet uz Transakcijas.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-128">Click Transactions.</span></span>
3. <span data-ttu-id="2aa4e-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2aa4e-130">Ievērojiet, ka saņemšanas lauks ir iestatīts uz Pasūtīts.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="2aa4e-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="2aa4e-132">Saņemt krājumus</span><span class="sxs-lookup"><span data-stu-id="2aa4e-132">Receive items</span></span>
1. <span data-ttu-id="2aa4e-133">Noklikšķiniet uz Produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-133">Click Product receipt.</span></span>
2. <span data-ttu-id="2aa4e-134">Laukā Ārējā produktu ieejas plūsma ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="2aa4e-135">Laukā Daudzums ievadiet skaitli, kas ir mazāks par skaitli, kas ir norādīts šeit.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="2aa4e-136">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="2aa4e-137">Pārbaudiet rīcībā esošo krājumu</span><span class="sxs-lookup"><span data-stu-id="2aa4e-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="2aa4e-138">Noklikšķiniet uz Krājumi.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-138">Click Inventory.</span></span>
2. <span data-ttu-id="2aa4e-139">Noklikšķiniet uz Rīcībā esošie krājumi.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-139">Click On-hand.</span></span>
3. <span data-ttu-id="2aa4e-140">Noklikšķiniet uz Pārskats.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-140">Click Overview.</span></span>
    * <span data-ttu-id="2aa4e-141">Krājumus, kas tika saņemti kā sūtījumu krājumi, kas pieder kreditoram, ir pieejami rīcībā esoši.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="2aa4e-142">Sūtījuma papildināšanas pasūtījuma Atlikušais daudzums tiek parādīts laukā Pasūtīts kopā.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="2aa4e-143">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-143">Close the page.</span></span>
5. <span data-ttu-id="2aa4e-144">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="2aa4e-144">Click Close.</span></span>

