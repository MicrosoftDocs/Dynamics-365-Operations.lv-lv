--- 
title: "Preču saņemšanas reģistrēšana pirkšanas pasūtījumā"
description: "Šajā procedūrā ir parādīts, kā reģistrēt preču saņemšanu tieši pirkšanas pasūtījumā."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="c306b-103">Preču saņemšanas reģistrēšana pirkšanas pasūtījumā</span><span class="sxs-lookup"><span data-stu-id="c306b-103">Record the receipt of goods on the purchase order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c306b-104">Šajā procedūrā ir parādīts, kā reģistrēt preču saņemšanu tieši pirkšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="c306b-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="c306b-105">Produktu ieejas plūsmu var reģistrēt arī noliktavā, un pēc tam to reģistrēt pirkšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="c306b-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="c306b-106">Šo uzdevumu parasti izpilda pirkšanas aģents vai kreditoru koordinators.</span><span class="sxs-lookup"><span data-stu-id="c306b-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="c306b-107">Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="c306b-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="c306b-108">Piemērā ir iekļautas darbības vienkārša pirkšanas pasūtījuma izveidošanai, lai jūs varētu izspēlēt šo procedūru kā uzdevuma ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="c306b-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="c306b-109">Ja šo procedūru izmantojāt pats saviem datiem, jums būtu jāsāk ar apakšuzdevumu Reģistrēt preču saņemšanu.</span><span class="sxs-lookup"><span data-stu-id="c306b-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="c306b-110">Sagatavot jaunu pirkšanas pasūtījumu preču saņemšanai</span><span class="sxs-lookup"><span data-stu-id="c306b-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="c306b-111">Dodieties uz Sagāde un avoti > Pirkšanas pasūtījumi > Visi pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="c306b-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="c306b-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c306b-112">Click New.</span></span>
3. <span data-ttu-id="c306b-113">Laukā Kreditora konts ievadiet US-101.</span><span class="sxs-lookup"><span data-stu-id="c306b-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="c306b-114">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c306b-114">Click OK.</span></span>
5. <span data-ttu-id="c306b-115">Laukā Krājuma kods ievadiet M0001.</span><span class="sxs-lookup"><span data-stu-id="c306b-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="c306b-116">Laukā Daudzums ievadiet 5.</span><span class="sxs-lookup"><span data-stu-id="c306b-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="c306b-117">Darbību rūtī noklikšķiniet uz Pirkt.</span><span class="sxs-lookup"><span data-stu-id="c306b-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="c306b-118">Noklikšķiniet uz Apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="c306b-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="c306b-119">Preču saņemšanas reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="c306b-119">Record receipt of goods</span></span>
1. <span data-ttu-id="c306b-120">Darbību rūtī noklikšķiniet uz Saņemt.</span><span class="sxs-lookup"><span data-stu-id="c306b-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="c306b-121">Noklikšķiniet uz Produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="c306b-121">Click Product receipt.</span></span>
    * <span data-ttu-id="c306b-122">Laukā Daudzums varat atlasīt dažādas opcijas tam daudzumam, ko vēlaties saņemt.</span><span class="sxs-lookup"><span data-stu-id="c306b-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="c306b-123">Piemēram, ja daudzums ir iepriekš reģistrēts noliktavā, varat atlasīt Reģistrētais daudzums.</span><span class="sxs-lookup"><span data-stu-id="c306b-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="c306b-124">Šim piemēram lietojiet vērtību Pasūtītais daudzums.</span><span class="sxs-lookup"><span data-stu-id="c306b-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="c306b-125">Laukā Produktu ieejas plūsma ierakstiet jebkādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c306b-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="c306b-126">Šis lauks tiek lietots, lai ievadītu atsauci, kas tiks izmantota kā dokuments produktu ieejas plūsmas žurnālam.</span><span class="sxs-lookup"><span data-stu-id="c306b-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="c306b-127">Izvērsiet sadaļu Rindas.</span><span class="sxs-lookup"><span data-stu-id="c306b-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="c306b-128">Daudzuma laukā iestatiet vērtību 4.</span><span class="sxs-lookup"><span data-stu-id="c306b-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="c306b-129">Šeit jūs varat manuāli norādīt daudzumu, kas tiek saņemts katrai pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="c306b-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="c306b-130">Sakļaujiet sadaļu Rindas.</span><span class="sxs-lookup"><span data-stu-id="c306b-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="c306b-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c306b-131">Click OK.</span></span>
    * <span data-ttu-id="c306b-132">Tagad preces ir reģistrētas kā saņemtas pirkšanas pasūtījumā, un produktu ieejas plūsmas žurnāls ir izveidots kā dokuments, kas to atspoguļo.</span><span class="sxs-lookup"><span data-stu-id="c306b-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="c306b-133">Produktu ieejas plūsmas darbību var izmantot, lai pārskatītu ar pirkšanas pasūtījumu izveidotos žurnālus un redzētu, kas un kad tika saņemts.</span><span class="sxs-lookup"><span data-stu-id="c306b-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


