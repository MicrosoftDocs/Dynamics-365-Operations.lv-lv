--- 
title: "Krājumu reģistrēšana pamata noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu"
description: "Šajā procedūrā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat pamata noliktavas iestatījumus krājumu vadības modulī."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a5fa86bace459d694ab0a2ec289e11b0e4420932
ms.openlocfilehash: 184f38347e2525f3efef9b0d55003a94a75380d4
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="25891-103">Krājumu reģistrēšana pamata noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu</span><span class="sxs-lookup"><span data-stu-id="25891-103">Register items for a basic warehousing enabled item using an item arrival journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25891-104">Šajā procedūrā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat pamata noliktavas iestatījumus krājumu vadības modulī.</span><span class="sxs-lookup"><span data-stu-id="25891-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="25891-105">Tas parasti būtu jāveic saņemšanas darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="25891-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="25891-106">Šo procedūru varat palaist demonstrācijas datu uzņēmumā USMF, izmantojot piemēra vērtības.</span><span class="sxs-lookup"><span data-stu-id="25891-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="25891-107">Ja neizmantojat USMF, tad pirms šī ceļveža uzsākšanas pārliecinieties, ka jums ir apstiprināts pirkšanas pasūtījums ar atvērtu pirkšanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="25891-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="25891-108">Rindas vienībai ir jābūt esošai krājumā, tā nedrīkst lietot preču variantus, un tai nedrīkst būt izsekošanas dimensiju.</span><span class="sxs-lookup"><span data-stu-id="25891-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="25891-109">Krājuma vienībai jābūt saistītai ar noliktavas dimensijas grupu, kurā ir aktīva vieta un noliktava.</span><span class="sxs-lookup"><span data-stu-id="25891-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="25891-110">Krājumu saņemšanas žurnāla virsraksta izveide</span><span class="sxs-lookup"><span data-stu-id="25891-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="25891-111">Dodieties uz Krājumu vadība > Žurnāla ieraksti > Krājumu saņemšana > Krājumu saņemšana.</span><span class="sxs-lookup"><span data-stu-id="25891-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="25891-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="25891-112">Click New.</span></span>
3. <span data-ttu-id="25891-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="25891-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="25891-114">Ja izmantojat USMF, varat ierakstīt WHS.</span><span class="sxs-lookup"><span data-stu-id="25891-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="25891-115">Ja izmantojat citus datus, izvēlētajam žurnālam ir jābūt šādiem rekvizītiem: Pārbaudīt izdošanas vietu vērtībai ir jābūt Nē un Karantīnas pārraudzība vērtībai ir jābūt Nē.</span><span class="sxs-lookup"><span data-stu-id="25891-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="25891-116">Ierakstiet vērtību laukā Pavadzīme.</span><span class="sxs-lookup"><span data-stu-id="25891-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="25891-117">Šis ir kreditora izsniegtajā pavadzīmē norādītais pavadzīmes ID.</span><span class="sxs-lookup"><span data-stu-id="25891-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="25891-118">Pievienojiet unikālu numuru.</span><span class="sxs-lookup"><span data-stu-id="25891-118">Add a unique number.</span></span>  
5. <span data-ttu-id="25891-119">Atlasiet pirkšanas pasūtījumu laukā Numurs...</span><span class="sxs-lookup"><span data-stu-id="25891-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="25891-120">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="25891-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="25891-121">Rindu pievienošana krājumu saņemšanas žurnālam</span><span class="sxs-lookup"><span data-stu-id="25891-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="25891-122">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="25891-122">Click Functions.</span></span>
2. <span data-ttu-id="25891-123">Noklikšķiniet uz Izveidot rindas.</span><span class="sxs-lookup"><span data-stu-id="25891-123">Click Create lines.</span></span>
    * <span data-ttu-id="25891-124">Šajā žurnālā rindas var ievadīt manuāli vai izveidot automātiski.</span><span class="sxs-lookup"><span data-stu-id="25891-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="25891-125">Šajā piemērā tiks parādīts, kā tās izveidot automātiski.</span><span class="sxs-lookup"><span data-stu-id="25891-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="25891-126">Atzīmējiet izvēles rūtiņu Inicializēt skaitu vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="25891-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="25891-127">Šajā piemērā žurnāla rindu skaits tiks inicializēts atbilstoši nereģistrētajam skaitam no pirkšanas pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="25891-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="25891-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="25891-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="25891-129">Grāmatot žurnālu</span><span class="sxs-lookup"><span data-stu-id="25891-129">Post the journal</span></span>
1. <span data-ttu-id="25891-130">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="25891-130">Click Post.</span></span>
2. <span data-ttu-id="25891-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="25891-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="25891-132">Preču ieejas plūsmas ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="25891-132">Generate the product receipt</span></span>
1. <span data-ttu-id="25891-133">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="25891-133">Click Functions.</span></span>
2. <span data-ttu-id="25891-134">Noklikšķiniet uz Produktu ieejas plūsma.</span><span class="sxs-lookup"><span data-stu-id="25891-134">Click Product receipt.</span></span>
3. <span data-ttu-id="25891-135">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="25891-135">Click OK.</span></span>


