---
title: Preču saņemšanas reģistrēšana pirkšanas pasūtījumā
description: Šajā tēmā ir paskaidrots, kā reģistrēt preču saņemšanu tieši pirkšanas pasūtījumā.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd8ca2cbd24f326c4eaf9cd39e32de0eca81149d
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018610"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="17de2-103">Preču saņemšanas reģistrēšana pirkšanas pasūtījumā</span><span class="sxs-lookup"><span data-stu-id="17de2-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17de2-104">Šajā tēmā ir paskaidrots, kā reģistrēt preču saņemšanu tieši pirkšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="17de2-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="17de2-105">Produktu ieejas plūsmu var reģistrēt arī noliktavā, un pēc tam to reģistrēt pirkšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="17de2-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="17de2-106">Šo uzdevumu parasti izpilda pirkšanas aģents vai kreditoru koordinators.</span><span class="sxs-lookup"><span data-stu-id="17de2-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="17de2-107">Šajā ceļvedī rādīto piemēru var izmantot demonstrācijas datus uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="17de2-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="17de2-108">Piemērā ir iekļautas darbības vienkārša pirkšanas pasūtījuma izveidošanai, lai jūs varētu izspēlēt šo procedūru kā uzdevuma ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="17de2-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="17de2-109">Ja šo procedūru izmantojāt pats saviem datiem, jums būtu jāsāk ar apakšuzdevumu **Reģistrēt preču saņemšanu**.</span><span class="sxs-lookup"><span data-stu-id="17de2-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="17de2-110">Sagatavot jaunu pirkšanas pasūtījumu preču saņemšanai</span><span class="sxs-lookup"><span data-stu-id="17de2-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="17de2-111">Pārejiet uz **Navigācijas rūts > Moduļi > Sagāde un avoti > Pirkšanas pieprasījumi > Visi pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="17de2-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="17de2-112">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="17de2-112">Select **New**.</span></span>
3. <span data-ttu-id="17de2-113">Laukā **Kreditora konts** ievadiet `US-101`.</span><span class="sxs-lookup"><span data-stu-id="17de2-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="17de2-114">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="17de2-114">Select **OK**.</span></span>
5. <span data-ttu-id="17de2-115">Laukā **Krājuma kods** ievadiet `M0001`.</span><span class="sxs-lookup"><span data-stu-id="17de2-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="17de2-116">Laukā **Daudzums** ievadiet `5`.</span><span class="sxs-lookup"><span data-stu-id="17de2-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="17de2-117">Darbību rūtī atlasiet **Pirkšana**.</span><span class="sxs-lookup"><span data-stu-id="17de2-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="17de2-118">Atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="17de2-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="17de2-119">Preču saņemšanas reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="17de2-119">Record receipt of goods</span></span>
1. <span data-ttu-id="17de2-120">Darbību rūtī atlasiet **Saņemt**.</span><span class="sxs-lookup"><span data-stu-id="17de2-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="17de2-121">Atlasiet **Preču ieejas plūsma**.</span><span class="sxs-lookup"><span data-stu-id="17de2-121">Select **Product receipt**.</span></span> <span data-ttu-id="17de2-122">Laukā **Daudzums** varat atlasīt dažādas opcijas tam daudzumam, ko vēlaties saņemt.</span><span class="sxs-lookup"><span data-stu-id="17de2-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="17de2-123">Piemēram, ja daudzums ir iepriekš reģistrēts noliktavā, varat atlasīt **Reģistrētais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="17de2-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="17de2-124">Šim piemēram lietojiet vērtību **Pasūtītais daudzums**.</span><span class="sxs-lookup"><span data-stu-id="17de2-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="17de2-125">Izvērsiet sadaļu **Pārskats**.</span><span class="sxs-lookup"><span data-stu-id="17de2-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="17de2-126">Laukā **Preču ieejas plūsma** ierakstiet jebkādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="17de2-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="17de2-127">Šis lauks tiek lietots, lai ievadītu atsauci, kas tiks izmantota kā dokuments produktu ieejas plūsmas žurnālam.</span><span class="sxs-lookup"><span data-stu-id="17de2-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="17de2-128">Izvērsiet sadaļu **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="17de2-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="17de2-129">Iestatiet **Daudzums** uz '4'.</span><span class="sxs-lookup"><span data-stu-id="17de2-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="17de2-130">Šeit jūs varat manuāli norādīt daudzumu, kas tiek saņemts katrai pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="17de2-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="17de2-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="17de2-131">Select **OK**.</span></span> <span data-ttu-id="17de2-132">Tagad preces ir reģistrētas kā saņemtas pirkšanas pasūtījumā, un produktu ieejas plūsmas žurnāls ir izveidots kā dokuments, kas to atspoguļo.</span><span class="sxs-lookup"><span data-stu-id="17de2-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="17de2-133">Produktu ieejas plūsmas darbību var izmantot, lai pārskatītu ar pirkšanas pasūtījumu izveidotos žurnālus un redzētu, kas un kad tika saņemts.</span><span class="sxs-lookup"><span data-stu-id="17de2-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

