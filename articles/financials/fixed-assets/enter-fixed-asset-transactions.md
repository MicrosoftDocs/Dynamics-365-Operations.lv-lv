---
title: "Pamatlīdzekļu transakciju opcijas"
description: "Šajā rakstā ir aprakstītas dažādās metodes, kas ir pieejamas pamatlīdzekļu transakciju izveidošanai."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 3d16b43eda0157e63a0d30fe806dac9a359d5fa4
ms.contentlocale: lv-lv
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="62827-103">Pamatlīdzekļu transakciju opcijas</span><span class="sxs-lookup"><span data-stu-id="62827-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="62827-104">Šajā rakstā ir aprakstītas dažādās metodes, kas ir pieejamas pamatlīdzekļu transakciju izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="62827-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="62827-105">Varat iestatīt pamatlīdzekļus, lai integrētu ar kreditoriem, debitoriem, sagādi un izcelsmi un Virsgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="62827-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="62827-106">Ja vēlaties, varat arī pārsūtīt noliktavas krājumu pārvaldību uz pamatlīdzekļiem iekšējai izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="62827-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="62827-107">Parādi kreditoriem</span><span class="sxs-lookup"><span data-stu-id="62827-107">Accounts payable</span></span>
<span data-ttu-id="62827-108">Pamatlīdzekļu transakcijas varat ievadīt lapā Žurnāla dokuments.</span><span class="sxs-lookup"><span data-stu-id="62827-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="62827-109">Šo lapu var atvērt tikai no lapas Rēķinu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="62827-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="62827-110">Lapu Žurnāla dokuments varat atvērt arī no lapas Rēķinu apstiprināšanas žurnāls.</span><span class="sxs-lookup"><span data-stu-id="62827-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="62827-111">Laukā Korespondējošā konta tips atlasiet Pamatlīdzekļi.</span><span class="sxs-lookup"><span data-stu-id="62827-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="62827-112">Pēc tam laukā Korespondējošais konts atlasiet pamatlīdzekļa numuru.</span><span class="sxs-lookup"><span data-stu-id="62827-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="62827-113">Cilnē Pamatlīdzekļi ievadiet vērtības laukos Transakcijas tips un Grāmata.</span><span class="sxs-lookup"><span data-stu-id="62827-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="62827-114">Debitoru parādi</span><span class="sxs-lookup"><span data-stu-id="62827-114">Accounts receivable</span></span>
<span data-ttu-id="62827-115">Pamatlīdzekļu transakcijas varat ievadīt lapā Brīva teksta rēķins.</span><span class="sxs-lookup"><span data-stu-id="62827-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="62827-116">Lapā Brīva teksta rēķins, režģī Rēķina rindas atlasiet kādu rindas krājumu.</span><span class="sxs-lookup"><span data-stu-id="62827-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="62827-117">Noklikšķiniet uz kopsavilkuma cilnes Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="62827-117">Click the Line details FastTab.</span></span> <span data-ttu-id="62827-118">Ievadiet norakstīšanas transakcijas pamatlīdzekļa numuru un grāmatu.</span><span class="sxs-lookup"><span data-stu-id="62827-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="62827-119">Brīvā teksta rēķiniem pamatlīdzekļa transakcijas tips vienmēr ir Norakstīšana - pārdošana.</span><span class="sxs-lookup"><span data-stu-id="62827-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="62827-120">Sagāde un avoti</span><span class="sxs-lookup"><span data-stu-id="62827-120">Procurement and sourcing</span></span>
<span data-ttu-id="62827-121">Pamatlīdzekļu transakcijas varat ievadīt lapā Pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="62827-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="62827-122">Ievadiet nepieciešamo informāciju, lai izveidotu pirkšanas pasūtījumu, un pēc tam noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="62827-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="62827-123">Lapā Pirkšanas pasūtījums noklikšķiniet uz kopsavilkuma cilnes Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="62827-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="62827-124">Pēc tam cilnē Pamatlīdzekļi ievadiet informāciju par pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="62827-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="62827-125">Lai grāmatotu iegādes transakciju esošam pamatlīdzeklim, norādiet šī pamatlīdzekļa numuru, grāmatu un transakcijas tipu.</span><span class="sxs-lookup"><span data-stu-id="62827-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="62827-126">Pamatlīdzekli nevar grāmatot, ja kāda informācija nav norādīta.</span><span class="sxs-lookup"><span data-stu-id="62827-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="62827-127">Lai grāmatotu iegādes transakciju jaunam pamatlīdzeklim, atzīmējiet opciju Vai jauns pamatlīdzeklis? un pēc tam atlasiet pamatlīdzekļu grupu, kurai piešķirt šo jauno pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="62827-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="62827-128">Tomēr nav pieejams neviens no pamatlīdzekļu laukiem, ja krājums ir krājumu modeļu grupā, kas izmanto standarta izmaksu krājumu modeli.</span><span class="sxs-lookup"><span data-stu-id="62827-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="62827-129">Turklāt opcijas, kas ir noteiktas lapā Pamatlīdzekļu parametri, nosaka, vai iegādes transakcijas varat grāmatot no pirkšanas moduļiem.</span><span class="sxs-lookup"><span data-stu-id="62827-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="62827-130">Ja pamatlīdzekļu iegādei tiek izmantots pirkšanas pasūtījums vai žurnāls Krājumi pamatlīdzekļiem, tiek ietekmēta krājumu vērtība.</span><span class="sxs-lookup"><span data-stu-id="62827-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="62827-131">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="62827-131">General ledger</span></span>
<span data-ttu-id="62827-132">Jebkuru pamatlīdzekļa transakcijas tipu var grāmatot lapā Virsgrāmatas žurnāls.</span><span class="sxs-lookup"><span data-stu-id="62827-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="62827-133">Varat arī izmantot žurnālus sadaļā Pamatlīdzekļi, lai grāmatotu pamatlīdzekļu darbības.</span><span class="sxs-lookup"><span data-stu-id="62827-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="62827-134">Pamatlīdzekļu darbības tipu ievadīšanas opcijas</span><span class="sxs-lookup"><span data-stu-id="62827-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="62827-135">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="62827-135">Transaction type</span></span>                    | <span data-ttu-id="62827-136">Modulis</span><span class="sxs-lookup"><span data-stu-id="62827-136">Module</span></span>                   | <span data-ttu-id="62827-137">Opcijas</span><span class="sxs-lookup"><span data-stu-id="62827-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="62827-138">Iegāde, Iegādes korekcija</span><span class="sxs-lookup"><span data-stu-id="62827-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="62827-139">Pamatlīdzekļi</span><span class="sxs-lookup"><span data-stu-id="62827-139">Fixed assets</span></span>             | <span data-ttu-id="62827-140">Pamatlīdzekļi, Krājumi pamatlīdzekļiem</span><span class="sxs-lookup"><span data-stu-id="62827-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="62827-141">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="62827-141">General ledger</span></span>           | <span data-ttu-id="62827-142">Virsgrāmatas žurnāls</span><span class="sxs-lookup"><span data-stu-id="62827-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="62827-143">Parādi kreditoriem</span><span class="sxs-lookup"><span data-stu-id="62827-143">Accounts payable</span></span>         | <span data-ttu-id="62827-144">Rēķinu žurnāls, Rēķinu apstiprināšanas žurnāls</span><span class="sxs-lookup"><span data-stu-id="62827-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="62827-145">Sagāde un avoti</span><span class="sxs-lookup"><span data-stu-id="62827-145">Procurement and sourcing</span></span> | <span data-ttu-id="62827-146">Pirkšanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="62827-146">Purchase order</span></span>                            |
| <span data-ttu-id="62827-147">Nolietojums</span><span class="sxs-lookup"><span data-stu-id="62827-147">Depreciation</span></span>                        | <span data-ttu-id="62827-148">Pamatlīdzekļi</span><span class="sxs-lookup"><span data-stu-id="62827-148">Fixed assets</span></span>             | <span data-ttu-id="62827-149">Pamatlīdzekļi</span><span class="sxs-lookup"><span data-stu-id="62827-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="62827-150">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="62827-150">General ledger</span></span>           | <span data-ttu-id="62827-151">Virsgrāmatas žurnāls</span><span class="sxs-lookup"><span data-stu-id="62827-151">General journal</span></span>                           |
| <span data-ttu-id="62827-152">Izslēgšana</span><span class="sxs-lookup"><span data-stu-id="62827-152">Disposal</span></span>                            | <span data-ttu-id="62827-153">Pamatlīdzekļi</span><span class="sxs-lookup"><span data-stu-id="62827-153">Fixed assets</span></span>             | <span data-ttu-id="62827-154">Pamatlīdzekļi</span><span class="sxs-lookup"><span data-stu-id="62827-154">Fixed assets</span></span>                              |
| <span data-ttu-id="62827-155">** **</span><span class="sxs-lookup"><span data-stu-id="62827-155">** **</span></span>                               | <span data-ttu-id="62827-156">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="62827-156">General ledger</span></span>           | <span data-ttu-id="62827-157">Virsgrāmatas žurnāls</span><span class="sxs-lookup"><span data-stu-id="62827-157">General journal</span></span>                           |
| <span data-ttu-id="62827-158">** **</span><span class="sxs-lookup"><span data-stu-id="62827-158">** **</span></span>                               | <span data-ttu-id="62827-159">Debitoru parādi</span><span class="sxs-lookup"><span data-stu-id="62827-159">Accounts receivable</span></span>      | <span data-ttu-id="62827-160">Brīva teksta rēķins</span><span class="sxs-lookup"><span data-stu-id="62827-160">Free text invoice</span></span>                         |



<span data-ttu-id="62827-161">Plašāku informāciju skatiet rakstā [Pamatlīdzekļu integrācija](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="62827-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




