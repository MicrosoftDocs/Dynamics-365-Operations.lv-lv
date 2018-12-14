--- 
title: "Rēķinu un pamatdatu auditēšana kreditoru sistēmā"
description: "Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cc995b474e86272b49629f97e1b4d4b4fb597b9d
ms.openlocfilehash: 946076d682a10becdc2c4a8baff7f52de7893119
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="5646d-103">Rēķinu un pamatdatu auditēšana kreditoru sistēmā</span><span class="sxs-lookup"><span data-stu-id="5646d-103">Audit invoices and key data in AP system</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5646d-104">Kad pēc pirkšanas pasūtījuma saņemat rēķinu no preču vai pakalpojumu piegādātāja, šiem biznesa procesiem var būt nepieciešama preču vai pakalpojumu saņemšana pirms rēķina apstiprināšanas apmaksai.</span><span class="sxs-lookup"><span data-stu-id="5646d-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="5646d-105">Pirms sākat, pārliecinieties, ka ir atlasīta konfigurācijas atslēga Rēķinu salīdzināšana.</span><span class="sxs-lookup"><span data-stu-id="5646d-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="5646d-106">Lapā Kreditoru moduļa parametri pārliecinieties, ka ir atlasīta opcija Iespējot rēķinu salīdzināšanas pārbaudes, lauks Grāmatot rēķinu ar neatbilstībām ir iestatīts uz Pieprasīt apstiprinājumu un lauks Rindu atbilstības ierobežojumi ir iestatīts uz Trīsvirzienu atbilstība.</span><span class="sxs-lookup"><span data-stu-id="5646d-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="5646d-107">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="5646d-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="5646d-108">Šīs darbības veiktu lietotājs ar lomu Kreditoriem maksājamo parādu vadītājs vai Grāmatvedības vadītājs.</span><span class="sxs-lookup"><span data-stu-id="5646d-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="5646d-109">Pirkšanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="5646d-109">Create a purchase order</span></span>
1. <span data-ttu-id="5646d-110">Atv. **Visi pirkš. pasūt**.</span><span class="sxs-lookup"><span data-stu-id="5646d-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="5646d-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5646d-111">Click **New**.</span></span>
3. <span data-ttu-id="5646d-112">Laukā **Kreditora konts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5646d-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="5646d-113">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5646d-113">Click **OK**.</span></span>
5. <span data-ttu-id="5646d-114">Nokl. **Piev. r.**</span><span class="sxs-lookup"><span data-stu-id="5646d-114">Click **Add line**.</span></span>
6. <span data-ttu-id="5646d-115">Laukā **Krājuma kods** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5646d-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="5646d-116">Darbību rūtī noklikšķ. uz **Pirkšana**.</span><span class="sxs-lookup"><span data-stu-id="5646d-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="5646d-117">Noklikšķiniet uz **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="5646d-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="5646d-118">Grāmatot produktu ieejas plūsmu</span><span class="sxs-lookup"><span data-stu-id="5646d-118">Post a product receipt</span></span>
1. <span data-ttu-id="5646d-119">Darbību rūtī noklikšķ. uz **Saņemt**.</span><span class="sxs-lookup"><span data-stu-id="5646d-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="5646d-120">Nokl. **Pr. ieejas pl**.</span><span class="sxs-lookup"><span data-stu-id="5646d-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="5646d-121">Laukā **Prod. ieejas pl.** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5646d-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="5646d-122">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5646d-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="5646d-123">Ierakstīt kreditora rēķinu un saskaņot to ar produktu ieejas plūsmu</span><span class="sxs-lookup"><span data-stu-id="5646d-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="5646d-124">Darbību rūtī noklikšķ. uz **Rēķins > Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="5646d-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="5646d-125">Laukā **Numurs** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="5646d-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="5646d-126">Nokl. uz **Noklusējums no: Pasūt. daudz.**, lai atv. dialogl.</span><span class="sxs-lookup"><span data-stu-id="5646d-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="5646d-127">Laukā **Noklusējuma daudzums rindām** atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="5646d-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="5646d-128">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5646d-128">Click **OK**.</span></span>
6. <span data-ttu-id="5646d-129">Noklikšķiniet uz pogas **Jā**.</span><span class="sxs-lookup"><span data-stu-id="5646d-129">Click **Yes**.</span></span>
7. <span data-ttu-id="5646d-130">Nokl. **Sask. prod. ieejas pl.**.</span><span class="sxs-lookup"><span data-stu-id="5646d-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="5646d-131">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5646d-131">Click **OK**.</span></span>
9. <span data-ttu-id="5646d-132">Darbību rūtī nokl. uz **Pārskatīt**.</span><span class="sxs-lookup"><span data-stu-id="5646d-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="5646d-133">Nokl. **Atb. det. inf**.</span><span class="sxs-lookup"><span data-stu-id="5646d-133">Click **Matching details**.</span></span>


