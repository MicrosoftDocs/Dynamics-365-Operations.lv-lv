--- 
title: " Nepārtrauktības programmu lietošana"
description: "Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus."
author: scott-tucker
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d3b5690bfbd10b77e784d35d0c4f4518de58333
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="use-a-continuity-program"></a><span data-ttu-id="bce58-103"> Nepārtrauktības programmu lietošana</span><span class="sxs-lookup"><span data-stu-id="bce58-103">Use a continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="bce58-104">Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="bce58-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="bce58-105">Lai pabeigtu šo procedūru, lietotājam ir jābūt iestatītam kā zvanu centra lietotājam.</span><span class="sxs-lookup"><span data-stu-id="bce58-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="bce58-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="bce58-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="bce58-107">Dodieties uz Mazumtirdzniecība un komercija > Debitori > Debitoru apkalpošana.</span><span class="sxs-lookup"><span data-stu-id="bce58-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="bce58-108">Laukā SearchText ierakstiet 'Zane', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="bce58-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="bce58-109">Parādīsies detalizētās meklēšanas uznirstošais dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="bce58-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="bce58-110">Ja tas neparādās, noklikšķiniet uz Meklēt, pa labi no šī lauka.</span><span class="sxs-lookup"><span data-stu-id="bce58-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="bce58-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="bce58-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bce58-112">Jābūt tikai vienai rindai, kurā redzams Zane Siliņa.</span><span class="sxs-lookup"><span data-stu-id="bce58-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="bce58-113">Atlasiet rindu, noklikšķinot uz atzīmes kolonnu, kas atrodas pa kreisi no režģa.</span><span class="sxs-lookup"><span data-stu-id="bce58-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="bce58-114">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="bce58-114">Click Select.</span></span>
5. <span data-ttu-id="bce58-115">Noklikšķiniet uz Jauns pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="bce58-115">Click New sales order.</span></span>
    * <span data-ttu-id="bce58-116">Ir ieteicams atzīmēt pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="bce58-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="bce58-117">Tas būs nepieciešams vēlāk šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="bce58-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="bce58-118">Laukā Krājuma kods ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="bce58-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="bce58-119">Tas ir nepārtrauktības krājums USRT demonstrācijas datos.</span><span class="sxs-lookup"><span data-stu-id="bce58-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="bce58-120">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="bce58-120">Click Complete.</span></span>
8. <span data-ttu-id="bce58-121">Laukā Maksājuma metode ievadiet 'Visa'.</span><span class="sxs-lookup"><span data-stu-id="bce58-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="bce58-122">Noklikšķiniet uz Pievienot kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="bce58-122">Click Add credit card.</span></span>
    * <span data-ttu-id="bce58-123">Ievadiet nepieciešamo kredītkartes informāciju šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="bce58-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="bce58-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="bce58-124">Click OK.</span></span>
11. <span data-ttu-id="bce58-125">Izvērsiet sadaļu Maksājums.</span><span class="sxs-lookup"><span data-stu-id="bce58-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="bce58-126">Lai iesniegtu zvanu centra pasūtījumu, pasūtījumam ir jāievada maksājumi.</span><span class="sxs-lookup"><span data-stu-id="bce58-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="bce58-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="bce58-127">Click OK.</span></span>
13. <span data-ttu-id="bce58-128">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="bce58-128">Click Submit.</span></span>
    * <span data-ttu-id="bce58-129">Jūs esat pabeidzis jauna nepārtrauktību pasūtījuma izveidi.</span><span class="sxs-lookup"><span data-stu-id="bce58-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="bce58-130">Pēc tam izpildiet divas pakešuzdevumu apstrādes, kas tiek izmantotas, lai apstrādātu nepārtrauktības pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="bce58-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="bce58-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bce58-131">Close the page.</span></span>
15. <span data-ttu-id="bce58-132">Dodieties uz Mazumtirdzniecība un komercija > Nepārtrauktība > Nepārtrauktības maksājumu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="bce58-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="bce58-133">Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="bce58-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="bce58-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="bce58-134">Click OK.</span></span>
18. <span data-ttu-id="bce58-135">Dodieties uz Mazumtirdzniecība un komercija > Nepārtrauktība > Izveidot nepārtrauktības apakšpasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="bce58-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="bce58-136">Šī procesa laikā tiks izveidoti jauni pārdošanas pasūtījumi, pamatojoties uz nepārtrauktības programmas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="bce58-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="bce58-137">Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="bce58-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="bce58-138">Krājums '88000' ir nepārtrauktības krājums USRT demonstrācijas datos.</span><span class="sxs-lookup"><span data-stu-id="bce58-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="bce58-139">Laukā Pārdošanas pasūtījums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bce58-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="bce58-140">Ievadiet pārdošanas pasūtījuma numuru, kas atzīmējāt iepriekš šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="bce58-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="bce58-141">Tas saglabās apstrādes laiku minimālu šai procedūrai.</span><span class="sxs-lookup"><span data-stu-id="bce58-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="bce58-142">Lauks pārdošanas pasūtījums ir neobligāts--jūs varat apstrādāt visus pasūtījumus jebkurai programmai.</span><span class="sxs-lookup"><span data-stu-id="bce58-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="bce58-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="bce58-143">Click OK.</span></span>


