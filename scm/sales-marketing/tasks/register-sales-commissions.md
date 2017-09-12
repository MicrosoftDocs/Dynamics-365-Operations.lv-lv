--- 
title: "Pārdošanas komisiju reģistrēšana"
description: "Šajā procedūrā tiek parādīts, kā tiek aprēķinātas un reģistrētas pārdošanas komisijas."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: f195f9e466eab3cf87afea2b5d430d0ea25c5a83
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="register-sales-commissions"></a><span data-ttu-id="8c9ce-103">Pārdošanas komisiju reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="8c9ce-103">Register sales commissions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c9ce-104">Šajā procedūrā tiek parādīts, kā tiek aprēķinātas un reģistrētas pārdošanas komisijas.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="8c9ce-105">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="8c9ce-106">Pirms sākt šo ceļvedi, izpildiet ceļvedi ar nosaukumu "Pārdošanas komisijas noteikumu iestatīšana", lai nodrošinātu, ka jums ir visi nepieciešami komisijas aprēķina iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="8c9ce-107">Ņemiet vērā debitoru un krājumu skaitu, ko esat izvēlējies komisijas procesam, un izmantojiet tos, lai izveidotu pārdošanas pasūtījumu šajā ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="8c9ce-108">Rēķina izsniegšana par pārdošanas pasūtījumu, kas dod pārdevējam tiesības uz komisiju</span><span class="sxs-lookup"><span data-stu-id="8c9ce-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="8c9ce-109">Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="8c9ce-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-110">Click New.</span></span>
3. <span data-ttu-id="8c9ce-111">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8c9ce-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8c9ce-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8c9ce-114">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-114">Click OK.</span></span>
7. <span data-ttu-id="8c9ce-115">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="8c9ce-116">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-116">Click Change view.</span></span>
9. <span data-ttu-id="8c9ce-117">Noklikšķiniet uz Virsraksta skatījuma.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-117">Click Header view.</span></span>
10. <span data-ttu-id="8c9ce-118">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="8c9ce-119">Vērtība laukā Pārdošanas grupa apzīmē grupu ar vienu vai vairākiem pārdošanas pārstāvjiem, kas tai piešķirti.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="8c9ce-120">Cilvēki grupā ir tie, kas saņems komisijas, kad pasūtījums būs iekļauts rēķinā, atbilstoši iepriekš definētām likmēm un sadalījumam.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="8c9ce-121">Vērtība tiek kopēta no Debitora kartes, bet to var mainīt, ja vēlaties.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="8c9ce-122">Pārdošanas grupa tiek kopēta arī pārdošanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="8c9ce-123">To var mainīt, lai tā varētu atšķirties no virsrakstā un/vai starp rindām norādītās.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="8c9ce-124">Vērtība laukā Komisijas grupa atspoguļo grupu, kuru esat izveidojis vienam vai vairākiem debitoriem ar mērķi izsekot komisijas.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="8c9ce-125">Vērtība tiek kopēta no Debitora kartes, bet to var mainīt, ja vēlaties.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="8c9ce-126">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="8c9ce-127">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-127">Click Change view.</span></span>
13. <span data-ttu-id="8c9ce-128">Noklikšķiniet uz Rindas skats.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-128">Click Line view.</span></span>
14. <span data-ttu-id="8c9ce-129">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="8c9ce-130">Sarakstā atlasiet krājumu, kuru esat iestatījis komisijām.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="8c9ce-131">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8c9ce-132">Ņemiet vērā rindas Neto summu.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="8c9ce-133">Tie ir pārdošanas ieņēmumi, kuri šajā piemērā ir komisijas naudas aprēķina pamatā.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="8c9ce-134">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-134">Click Save.</span></span>
18. <span data-ttu-id="8c9ce-135">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="8c9ce-136">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-136">Click Invoice.</span></span>
20. <span data-ttu-id="8c9ce-137">Izvērsiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="8c9ce-138">Laukā Daudzums atlasiet vērtību Visi.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="8c9ce-139">Laukā Grāmatošana atlasiet vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="8c9ce-140">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-140">Click OK.</span></span>
24. <span data-ttu-id="8c9ce-141">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-141">Click OK.</span></span>
    * <span data-ttu-id="8c9ce-142">Grāmatošana var ilgt kādu minūti.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="8c9ce-143">Ļaujiet apstrādei beigties, neaizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="8c9ce-144">Reģistrēto pārdošanas komisiju pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="8c9ce-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="8c9ce-145">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="8c9ce-146">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-146">Click Invoice.</span></span>
3. <span data-ttu-id="8c9ce-147">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="8c9ce-148">Noklikšķiniet uz Komisijas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="8c9ce-149">Cilnē Pārskats ir parādītas rindas, kas atspoguļo pārdošanas pārstāvjiem maksājamās komisijas summas, kas ir saistītas ar rēķinā iekļauto pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="8c9ce-150">Apskatīsim to sīkāk.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-150">Let's review the details.</span></span>     
    * <span data-ttu-id="8c9ce-151">Ja Komisijas pārdošanas grupas iestatīšanai izmantojāt ceļvedi "Pārdošanas komisijas noteikumu iestatīšana", ir divi pārdevēji, kas saņems pārdošanas komisijas un komisija tiks sadalīta vienlīdzīgi starp tiem.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="8c9ce-152">Šajā piemērā komisijas kopējā summa tiek aprēķināta kā procentuāla daļa no pārdošanas ieņēmumiem (pasūtījuma rindas neto summa).</span><span class="sxs-lookup"><span data-stu-id="8c9ce-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="8c9ce-153">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-153">Close the page.</span></span>
6. <span data-ttu-id="8c9ce-154">Noklikšķiniet uz Dokuments.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-154">Click Voucher.</span></span>
    * <span data-ttu-id="8c9ce-155">Varat pārskatīt dokumentu transakcijas par komisijas summām, kas tika iegrāmatotas iepriekš definētos komisijas izdevumu un maksājamo komisiju kontos.</span><span class="sxs-lookup"><span data-stu-id="8c9ce-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


