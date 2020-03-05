---
title: Izmantojot nepārtrauktības programmu
description: Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd0bfcd99a23e4c639a6317adefb41a947a487a5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023260"
---
# <a name="using-continuity-program"></a><span data-ttu-id="1a57a-103">Izmantojot nepārtrauktības programmu</span><span class="sxs-lookup"><span data-stu-id="1a57a-103">Using continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1a57a-104">Šajā procedūrā ir aprakstīts, kā pārdot nepārtrauktības programmu, un apstrādāt saistītos pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="1a57a-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="1a57a-105">Lai pabeigtu šo procedūru, lietotājam ir jābūt iestatītam kā zvanu centra lietotājam.</span><span class="sxs-lookup"><span data-stu-id="1a57a-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="1a57a-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="1a57a-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="1a57a-107">Dodieties uz Retail un Commerce > Debitori > Debitoru apkalpošana.</span><span class="sxs-lookup"><span data-stu-id="1a57a-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="1a57a-108">Laukā SearchText ierakstiet 'Zane', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="1a57a-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="1a57a-109">Parādīsies detalizētās meklēšanas uznirstošais dialoglodziņš.</span><span class="sxs-lookup"><span data-stu-id="1a57a-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="1a57a-110">Ja tas neparādās, noklikšķiniet uz Meklēt, pa labi no šī lauka.</span><span class="sxs-lookup"><span data-stu-id="1a57a-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="1a57a-111">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1a57a-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1a57a-112">Jābūt tikai vienai rindai, kurā redzams Zane Siliņa.</span><span class="sxs-lookup"><span data-stu-id="1a57a-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="1a57a-113">Atlasiet rindu, noklikšķinot uz atzīmes kolonnu, kas atrodas pa kreisi no režģa.</span><span class="sxs-lookup"><span data-stu-id="1a57a-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="1a57a-114">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="1a57a-114">Click Select.</span></span>
5. <span data-ttu-id="1a57a-115">Noklikšķiniet uz Jauns pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="1a57a-115">Click New sales order.</span></span>
    * <span data-ttu-id="1a57a-116">Ir ieteicams atzīmēt pārdošanas pasūtījuma numuru.</span><span class="sxs-lookup"><span data-stu-id="1a57a-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="1a57a-117">Tas būs nepieciešams vēlāk šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="1a57a-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="1a57a-118">Laukā Krājuma kods ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="1a57a-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="1a57a-119">Tas ir nepārtrauktības krājums USRT demonstrācijas datos.</span><span class="sxs-lookup"><span data-stu-id="1a57a-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="1a57a-120">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="1a57a-120">Click Complete.</span></span>
8. <span data-ttu-id="1a57a-121">Laukā Maksājuma metode ievadiet 'Visa'.</span><span class="sxs-lookup"><span data-stu-id="1a57a-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="1a57a-122">Noklikšķiniet uz Pievienot kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="1a57a-122">Click Add credit card.</span></span>
    * <span data-ttu-id="1a57a-123">Ievadiet nepieciešamo kredītkartes informāciju šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="1a57a-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="1a57a-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1a57a-124">Click OK.</span></span>
11. <span data-ttu-id="1a57a-125">Izvērsiet sadaļu Maksājums.</span><span class="sxs-lookup"><span data-stu-id="1a57a-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="1a57a-126">Lai iesniegtu zvanu centra pasūtījumu, pasūtījumam ir jāievada maksājumi.</span><span class="sxs-lookup"><span data-stu-id="1a57a-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="1a57a-127">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1a57a-127">Click OK.</span></span>
13. <span data-ttu-id="1a57a-128">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="1a57a-128">Click Submit.</span></span>
    * <span data-ttu-id="1a57a-129">Jūs esat pabeidzis jauna nepārtrauktību pasūtījuma izveidi.</span><span class="sxs-lookup"><span data-stu-id="1a57a-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="1a57a-130">Pēc tam izpildiet divas pakešuzdevumu apstrādes, kas tiek izmantotas, lai apstrādātu nepārtrauktības pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="1a57a-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="1a57a-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1a57a-131">Close the page.</span></span>
15. <span data-ttu-id="1a57a-132">Dodieties uz Retail un Commerce > Nepārtrauktība > Nepārtrauktības maksājumu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="1a57a-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="1a57a-133">Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="1a57a-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="1a57a-134">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="1a57a-134">Click OK.</span></span>
18. <span data-ttu-id="1a57a-135">Dodieties uz Retail un Commerce > Nepārtrauktība > Izveidot nepārtrauktības apakšpasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="1a57a-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="1a57a-136">Šī procesa laikā tiks izveidoti jauni pārdošanas pasūtījumi, pamatojoties uz nepārtrauktības programmas iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="1a57a-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="1a57a-137">Laukā Nepārtrauktības krājums ierakstiet '88000', un pēc tam nospiediet taustiņu Tab.</span><span class="sxs-lookup"><span data-stu-id="1a57a-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="1a57a-138">Krājums '88000' ir nepārtrauktības krājums USRT demonstrācijas datos.</span><span class="sxs-lookup"><span data-stu-id="1a57a-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="1a57a-139">Laukā Pārdošanas pasūtījums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1a57a-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="1a57a-140">Ievadiet pārdošanas pasūtījuma numuru, kas atzīmējāt iepriekš šajā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="1a57a-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="1a57a-141">Tas saglabās apstrādes laiku minimālu šai procedūrai.</span><span class="sxs-lookup"><span data-stu-id="1a57a-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="1a57a-142">Lauks pārdošanas pasūtījums ir neobligāts--jūs varat apstrādāt visus pasūtījumus jebkurai programmai.</span><span class="sxs-lookup"><span data-stu-id="1a57a-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="1a57a-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1a57a-143">Click OK.</span></span>
