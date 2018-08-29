--- 
title: "Pārdošanas nepārtrauktības programmas un saistīto pārdošanas pasūtījumu apstrādāšana"
description: "Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 5fe1823c9b684bbc5ac5bd0871cc5c0a0e6ce678
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="selling-continuity-programs-and-processing-related-sales-orders"></a><span data-ttu-id="cce93-103">Pārdošanas nepārtrauktības programmas un saistīto pārdošanas pasūtījumu apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="cce93-103">Selling continuity programs and processing related sales orders</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cce93-104">Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="cce93-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="cce93-105">Lai pabeigtu šo procedūru, lietotājam ir jābūt iestatītam kā zvanu centra lietotājam.</span><span class="sxs-lookup"><span data-stu-id="cce93-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="cce93-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="cce93-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="cce93-107">Dodieties uz Mazumtirdzniecība un komercija > Debitori > Debitoru apkalpošana.</span><span class="sxs-lookup"><span data-stu-id="cce93-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="cce93-108">Laukā SearchText ierakstiet 'Zane', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="cce93-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="cce93-109">Parādīsies detalizētās meklēšanas uznirstošais dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="cce93-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="cce93-110">Ja tas neparādās, noklikšķiniet uz Meklēt, pa labi no šī lauka.</span><span class="sxs-lookup"><span data-stu-id="cce93-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="cce93-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="cce93-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cce93-112">Jābūt tikai vienai rindai, kurā redzams Zane Siliņa.</span><span class="sxs-lookup"><span data-stu-id="cce93-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="cce93-113">Atlasiet rindu, noklikšķinot uz atzīmes kolonnu, kas atrodas pa kreisi no režģa.</span><span class="sxs-lookup"><span data-stu-id="cce93-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="cce93-114">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="cce93-114">Click Select.</span></span>
5. <span data-ttu-id="cce93-115">Noklikšķiniet uz Jauns pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="cce93-115">Click New sales order.</span></span>
    * <span data-ttu-id="cce93-116">Ir ieteicams atzīmēt pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="cce93-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="cce93-117">Tas būs nepieciešams vēlāk šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="cce93-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="cce93-118">Laukā Krājuma kods ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="cce93-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="cce93-119">Tas ir nepārtrauktības krājums USRT demonstrācijas datos.</span><span class="sxs-lookup"><span data-stu-id="cce93-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="cce93-120">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="cce93-120">Click Complete.</span></span>
8. <span data-ttu-id="cce93-121">Laukā Maksājuma metode ievadiet 'Visa'.</span><span class="sxs-lookup"><span data-stu-id="cce93-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="cce93-122">Noklikšķiniet uz Pievienot kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="cce93-122">Click Add credit card.</span></span>
    * <span data-ttu-id="cce93-123">Ievadiet nepieciešamo kredītkartes informāciju šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="cce93-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="cce93-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cce93-124">Click OK.</span></span>
11. <span data-ttu-id="cce93-125">Izvērsiet sadaļu Maksājums.</span><span class="sxs-lookup"><span data-stu-id="cce93-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="cce93-126">Lai iesniegtu zvanu centra pasūtījumu, pasūtījumam ir jāievada maksājumi.</span><span class="sxs-lookup"><span data-stu-id="cce93-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="cce93-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cce93-127">Click OK.</span></span>
13. <span data-ttu-id="cce93-128">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="cce93-128">Click Submit.</span></span>
    * <span data-ttu-id="cce93-129">Jūs esat pabeidzis jauna nepārtrauktību pasūtījuma izveidi.</span><span class="sxs-lookup"><span data-stu-id="cce93-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="cce93-130">Pēc tam izpildiet divas pakešuzdevumu apstrādes, kas tiek izmantotas, lai apstrādātu nepārtrauktības pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="cce93-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="cce93-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cce93-131">Close the page.</span></span>
15. <span data-ttu-id="cce93-132">Dodieties uz Mazumtirdzniecība un komercija > Nepārtrauktība > Nepārtrauktības maksājumu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="cce93-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="cce93-133">Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="cce93-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="cce93-134">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cce93-134">Click OK.</span></span>
18. <span data-ttu-id="cce93-135">Dodieties uz Mazumtirdzniecība un komercija > Nepārtrauktība > Izveidot nepārtrauktības apakšpasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="cce93-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="cce93-136">Šī procesa laikā tiks izveidoti jauni pārdošanas pasūtījumi, pamatojoties uz nepārtrauktības programmas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="cce93-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="cce93-137">Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="cce93-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="cce93-138">Krājums '88000' ir nepārtrauktības krājums USRT demonstrācijas datos.</span><span class="sxs-lookup"><span data-stu-id="cce93-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="cce93-139">Laukā Pārdošanas pasūtījums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cce93-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="cce93-140">Ievadiet pārdošanas pasūtījuma numuru, kas atzīmējāt iepriekš šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="cce93-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="cce93-141">Tas saglabās apstrādes laiku minimālu šai procedūrai.</span><span class="sxs-lookup"><span data-stu-id="cce93-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="cce93-142">Lauks Pārdošanas pasūtījums nav obligāts — varat apstrādāt visus pasūtījumus jebkurai programmai.</span><span class="sxs-lookup"><span data-stu-id="cce93-142">The Sales order field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="cce93-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="cce93-143">Click OK.</span></span>


