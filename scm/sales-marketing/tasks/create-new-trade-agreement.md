--- 
title: "Jauna pakalpojumu līguma izveide"
description: "Šajā procedūrā parādīts, kā izveidot tirdzniecības līgumu, kur reģistrēt jaunu preces pārdošanas cenu, par kuru vienojāties ar noteiktu debitoru."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="6b83a-103">Jauna pakalpojumu līguma izveide</span><span class="sxs-lookup"><span data-stu-id="6b83a-103">Create a new trade agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b83a-104">Šajā procedūrā parādīts, kā izveidot tirdzniecības līgumu, kur reģistrēt jaunu preces pārdošanas cenu, par kuru vienojāties ar noteiktu debitoru.</span><span class="sxs-lookup"><span data-stu-id="6b83a-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="6b83a-105">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="6b83a-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6b83a-106">Ja jūs izmantojat savus datus pirms sākat veikt šajā ceļvedī aprakstītās darbības, jums ir jāpārliecinās, ka nosaukums Tirdzniecības līgumu žurnāls eksistē un Noklusējuma relācija ir iestatīta uz "Cena (pārdošana)".</span><span class="sxs-lookup"><span data-stu-id="6b83a-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="6b83a-107">Jauna tirdzniecības līgumu žurnāla izveide un grāmatošana</span><span class="sxs-lookup"><span data-stu-id="6b83a-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="6b83a-108">Dodieties uz sadaļu Pārdošana un mārketings > Cenas un atlaides > Tirdzniecības līgumu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="6b83a-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="6b83a-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6b83a-109">Click New.</span></span>
3. <span data-ttu-id="6b83a-110">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6b83a-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6b83a-111">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6b83a-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6b83a-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6b83a-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6b83a-113">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="6b83a-113">Click Lines.</span></span>
7. <span data-ttu-id="6b83a-114">Laukā Konta kods atlasiet "Tabula".</span><span class="sxs-lookup"><span data-stu-id="6b83a-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="6b83a-115">Šajā piemērā tiek atjaunināta cena noteiktam debitoram, kas nozīmē, ka jums ir jāizvēlas Tabula.</span><span class="sxs-lookup"><span data-stu-id="6b83a-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="6b83a-116">Ja veicat preču saraksta cenas atjaunināšanu, jāatlasa Visi, lai jaunā cena būtu derīga visiem debitoriem.</span><span class="sxs-lookup"><span data-stu-id="6b83a-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="6b83a-117">Ja cenas dažādos debitoru segmentos atšķiras, jāatlasa Grupa.</span><span class="sxs-lookup"><span data-stu-id="6b83a-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="6b83a-118">Lai atlasītu Grupa, ir jāiestata Debitoru cenu grupas.</span><span class="sxs-lookup"><span data-stu-id="6b83a-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="6b83a-119">Laukā Konta atlase noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6b83a-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6b83a-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6b83a-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="6b83a-121">Laukā Krājuma kods atlasiet "Tabula".</span><span class="sxs-lookup"><span data-stu-id="6b83a-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="6b83a-122">Kad ievadāt tirdzniecības līgums ar tipu "Cena (pārdošana)", "Tabula" ir jāatlasa tikai laukā Krājuma kods.</span><span class="sxs-lookup"><span data-stu-id="6b83a-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="6b83a-123">Tas ir tāpēc, ka cena ir absolūtā vērtība un nevar būt vienāda visiem produktiem vai produktu grupai.</span><span class="sxs-lookup"><span data-stu-id="6b83a-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="6b83a-124">Laukā Krājumu saistība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6b83a-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="6b83a-125">Sarakstā atlasiet preci, ko vēlaties ietvert līgumā.</span><span class="sxs-lookup"><span data-stu-id="6b83a-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="6b83a-126">Atzīmējiet, kuru preci atlasījāt.</span><span class="sxs-lookup"><span data-stu-id="6b83a-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="6b83a-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6b83a-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6b83a-128">Laukā No ievadiet minimālo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="6b83a-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="6b83a-129">Ja debitoram ir jāpasūta minimālais daudzums, pirms tas var pretendēt uz jaunu cenu, tad ir jānorāda daudzums šeit.</span><span class="sxs-lookup"><span data-stu-id="6b83a-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="6b83a-130">Ievadiet vērtību laukā Līdz, lai norādītu maksimālo daudzumu, virs kura līguma cena vairs nebūs derīga.</span><span class="sxs-lookup"><span data-stu-id="6b83a-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="6b83a-131">Ja piedāvājat cenas un atlaides, pamatojoties uz vairākiem daudzumu pārtraukumiem, norādiet katru daudzumu grupu kā minimālā un maksimālā daudzuma pāri attiecīgi laukos "No" un "Līdz".</span><span class="sxs-lookup"><span data-stu-id="6b83a-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="6b83a-132">Laukā Summa valūtā ievadiet cenu.</span><span class="sxs-lookup"><span data-stu-id="6b83a-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="6b83a-133">Laukā No datuma ievadiet datumu, no kura šis līgums ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="6b83a-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="6b83a-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6b83a-134">Click Save.</span></span>
18. <span data-ttu-id="6b83a-135">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="6b83a-135">Click Validate.</span></span>
19. <span data-ttu-id="6b83a-136">Noklikšķiniet uz Validēt atlasītās rindas.</span><span class="sxs-lookup"><span data-stu-id="6b83a-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="6b83a-137">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6b83a-137">Click OK.</span></span>
21. <span data-ttu-id="6b83a-138">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="6b83a-138">Click Post.</span></span>
22. <span data-ttu-id="6b83a-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6b83a-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="6b83a-140">Ar preci saistīto tirdzniecības līgumu skatīšana</span><span class="sxs-lookup"><span data-stu-id="6b83a-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="6b83a-141">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="6b83a-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="6b83a-142">Sarakstā atrodiet un atlasiet preci, kuras cenu tikko atjaunojāt.</span><span class="sxs-lookup"><span data-stu-id="6b83a-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="6b83a-143">Darbību rūtī noklikšķiniet uz Pārdot.</span><span class="sxs-lookup"><span data-stu-id="6b83a-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="6b83a-144">Noklikšķiniet uz Skatīt tirdzniecības līgumus.</span><span class="sxs-lookup"><span data-stu-id="6b83a-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="6b83a-145">Pārskatiet detalizētu informāciju par tikko izveidoto cenu tirdzniecības līgumu.</span><span class="sxs-lookup"><span data-stu-id="6b83a-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="6b83a-146">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6b83a-146">Close the page.</span></span>


