---
title: Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu
description: Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai.
author: ShivamPandey-msft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9d3fab4be1de90783d5885cf46b9e0cf6ee74b5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820621"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="5d859-103">Kreditora rēķina reģistrēšana un atbilstības pārbaude pret saņemto daudzumu</span><span class="sxs-lookup"><span data-stu-id="5d859-103">Record vendor invoice and match against received quantity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d859-104">Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai.</span><span class="sxs-lookup"><span data-stu-id="5d859-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="5d859-105">Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana.</span><span class="sxs-lookup"><span data-stu-id="5d859-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="5d859-106">Lapā Kreditoru moduļa parametri pārliecinieties, ka ir atlasīta opcija Iespējot rēķinu salīdzināšanas pārbaudes, lauks Grāmatot rēķinu ar neatbilstībām ir iestatīts uz Pieprasīt apstiprinājumu un lauks Rindu atbilstības ierobežojumi ir iestatīts uz Trīsvirzienu atbilstība.</span><span class="sxs-lookup"><span data-stu-id="5d859-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="5d859-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="5d859-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="5d859-108">Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs.</span><span class="sxs-lookup"><span data-stu-id="5d859-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="5d859-109">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="5d859-109">Create a purchase order</span></span>
1. <span data-ttu-id="5d859-110">Dodieties uz Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="5d859-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="5d859-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="5d859-111">Click New.</span></span>
3. <span data-ttu-id="5d859-112">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="5d859-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5d859-113">Laukā Kreditora konts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5d859-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="5d859-114">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="5d859-114">Click OK.</span></span>
6. <span data-ttu-id="5d859-115">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="5d859-115">Click Add line.</span></span>
7. <span data-ttu-id="5d859-116">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5d859-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="5d859-117">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="5d859-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="5d859-118">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="5d859-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="5d859-119">Grāmatot produktu ieejas plūsmu</span><span class="sxs-lookup"><span data-stu-id="5d859-119">Post a product receipt</span></span>
1. <span data-ttu-id="5d859-120">Darbību rūtī noklikšķiniet uz Saņemt.</span><span class="sxs-lookup"><span data-stu-id="5d859-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="5d859-121">Noklikšķiniet uz Produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="5d859-121">Click Product receipt.</span></span>
3. <span data-ttu-id="5d859-122">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5d859-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5d859-123">Laukā Produktu ieejas plūsma ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5d859-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="5d859-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="5d859-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="5d859-125">Ierakstīt kreditora rēķinu un saskaņot to ar produktu ieejas plūsmu</span><span class="sxs-lookup"><span data-stu-id="5d859-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="5d859-126">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="5d859-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="5d859-127">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="5d859-127">Click Invoice.</span></span>
3. <span data-ttu-id="5d859-128">Laukā Numurs ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5d859-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="5d859-129">Noklikšķiniet uz Noklusējums no: Pasūtītais daudzums, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="5d859-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="5d859-130">Laukā Noklusējuma daudzums rindām atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="5d859-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="5d859-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="5d859-131">Click OK.</span></span>
7. <span data-ttu-id="5d859-132">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="5d859-132">Click Yes.</span></span>
8. <span data-ttu-id="5d859-133">Noklikšķiniet uz Saskaņot produktu ieejas plūsmu.</span><span class="sxs-lookup"><span data-stu-id="5d859-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="5d859-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="5d859-134">Click OK.</span></span>
10. <span data-ttu-id="5d859-135">Darbību rūtī noklikšķiniet uz Pārskatīt.</span><span class="sxs-lookup"><span data-stu-id="5d859-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="5d859-136">Noklikšķiniet uz Detalizēta informācija par atbilstību.</span><span class="sxs-lookup"><span data-stu-id="5d859-136">Click Matching details.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]