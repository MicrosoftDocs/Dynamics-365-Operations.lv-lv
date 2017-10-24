--- 
title: "Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu"
description: "Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a64413ac1840ef535252bd2d9752d52b26ccade1
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="2f91c-103">Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu</span><span class="sxs-lookup"><span data-stu-id="2f91c-103">Record vendor invoice and match against received quantity</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f91c-104">Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai.</span><span class="sxs-lookup"><span data-stu-id="2f91c-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="2f91c-105">Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana.</span><span class="sxs-lookup"><span data-stu-id="2f91c-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="2f91c-106">Lapā Kreditoru moduļa parametri pārliecinieties, ka ir atlasīta opcija Iespējot rēķinu salīdzināšanas pārbaudes, lauks Grāmatot rēķinu ar neatbilstībām ir iestatīts uz Pieprasīt apstiprinājumu un lauks Rindu atbilstības ierobežojumi ir iestatīts uz Trīsvirzienu atbilstība.</span><span class="sxs-lookup"><span data-stu-id="2f91c-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="2f91c-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="2f91c-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="2f91c-108">Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs.</span><span class="sxs-lookup"><span data-stu-id="2f91c-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="2f91c-109">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="2f91c-109">Create a purchase order</span></span>
1. <span data-ttu-id="2f91c-110">Dodieties uz Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="2f91c-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="2f91c-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2f91c-111">Click New.</span></span>
3. <span data-ttu-id="2f91c-112">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="2f91c-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2f91c-113">Laukā Kreditora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2f91c-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="2f91c-114">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2f91c-114">Click OK.</span></span>
6. <span data-ttu-id="2f91c-115">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="2f91c-115">Click Add line.</span></span>
7. <span data-ttu-id="2f91c-116">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2f91c-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="2f91c-117">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="2f91c-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="2f91c-118">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="2f91c-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="2f91c-119">Grāmatot produktu ieejas plūsmu</span><span class="sxs-lookup"><span data-stu-id="2f91c-119">Post a product receipt</span></span>
1. <span data-ttu-id="2f91c-120">Darbību rūtī noklikšķiniet uz Saņemt.</span><span class="sxs-lookup"><span data-stu-id="2f91c-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="2f91c-121">Noklikšķiniet uz Produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="2f91c-121">Click Product receipt.</span></span>
3. <span data-ttu-id="2f91c-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="2f91c-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2f91c-123">Laukā Produktu ieejas plūsma ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2f91c-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="2f91c-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2f91c-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="2f91c-125">Ierakstīt kreditora rēķinu un saskaņot to ar produktu ieejas plūsmu</span><span class="sxs-lookup"><span data-stu-id="2f91c-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="2f91c-126">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="2f91c-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="2f91c-127">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="2f91c-127">Click Invoice.</span></span>
3. <span data-ttu-id="2f91c-128">Laukā Numurs ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2f91c-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="2f91c-129">Noklikšķiniet uz Noklusējums no: Pasūtītais daudzums, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="2f91c-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="2f91c-130">Laukā Noklusējuma daudzums rindām atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="2f91c-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="2f91c-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2f91c-131">Click OK.</span></span>
7. <span data-ttu-id="2f91c-132">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="2f91c-132">Click Yes.</span></span>
8. <span data-ttu-id="2f91c-133">Noklikšķiniet uz Saskaņot produktu ieejas plūsmu.</span><span class="sxs-lookup"><span data-stu-id="2f91c-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="2f91c-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="2f91c-134">Click OK.</span></span>
10. <span data-ttu-id="2f91c-135">Darbību rūtī noklikšķiniet uz Pārskatīt.</span><span class="sxs-lookup"><span data-stu-id="2f91c-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="2f91c-136">Noklikšķiniet uz Detalizēta informācija par atbilstību.</span><span class="sxs-lookup"><span data-stu-id="2f91c-136">Click Matching details.</span></span>


