---
title: Pārdošanas komisiju reģistrēšana
description: Šajā tēmā ir aprakstīts, kā tiek aprēķinātas un reģistrētas pārdošanas komisijas.
author: omulvad
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee75f3a0c9dea7a7c4a4f927651aaab1d6bdb5c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836378"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="94c5b-103">Pārdošanas komisiju reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="94c5b-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="94c5b-104">Šajā tēmā ir aprakstīts, kā tiek aprēķinātas un reģistrētas pārdošanas komisijas.</span><span class="sxs-lookup"><span data-stu-id="94c5b-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="94c5b-105">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="94c5b-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="94c5b-106">Pirms sākt šo ceļvedi, izpildiet ceļvedi ar nosaukumu "Pārdošanas komisijas noteikumu iestatīšana", lai nodrošinātu, ka jums ir visi nepieciešami komisijas aprēķina iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="94c5b-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="94c5b-107">Ņemiet vērā debitoru un krājumu skaitu, ko esat izvēlējies komisijas procesam, un izmantojiet tos, lai izveidotu pārdošanas pasūtījumu šajā ceļvedī.</span><span class="sxs-lookup"><span data-stu-id="94c5b-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="94c5b-108">Rēķina izsniegšana par pārdošanas pasūtījumu, kas dod pārdevējam tiesības uz komisiju</span><span class="sxs-lookup"><span data-stu-id="94c5b-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="94c5b-109">Navigācijas panelī atveriet **Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="94c5b-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-110">Select **New**.</span></span>
3. <span data-ttu-id="94c5b-111">Laukā **Debitora konts** nolaižamajā izvēlnē atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="94c5b-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="94c5b-112">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-112">Select **OK**.</span></span>
5. <span data-ttu-id="94c5b-113">Darbību rūtī atlasiet **Opcijas**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="94c5b-114">Atlasiet **Mainīt skatu**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-114">Select **Change view**.</span></span>
7. <span data-ttu-id="94c5b-115">Atlasiet **Virsraksta skats**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-115">Select **Header view**.</span></span>
8. <span data-ttu-id="94c5b-116">Izvērsiet sadaļu **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="94c5b-117">Vērtība laukā **Pārdošanas grupa** apzīmē grupu ar vienu vai vairākiem pārdošanas pārstāvjiem, kas tai piešķirti.</span><span class="sxs-lookup"><span data-stu-id="94c5b-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="94c5b-118">Cilvēki grupā ir tie, kas saņems komisijas, kad pasūtījums būs iekļauts rēķinā, atbilstoši iepriekš definētām likmēm un sadalījumam.</span><span class="sxs-lookup"><span data-stu-id="94c5b-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="94c5b-119">Vērtība tiek kopēta no Debitora kartes, bet to var mainīt, ja vēlaties.</span><span class="sxs-lookup"><span data-stu-id="94c5b-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="94c5b-120">Pārdošanas grupa tiek kopēta arī pārdošanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="94c5b-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="94c5b-121">To var mainīt, lai tā varētu atšķirties no virsrakstā un/vai starp rindām norādītās.</span><span class="sxs-lookup"><span data-stu-id="94c5b-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="94c5b-122">Vērtība laukā **Komisijas grupa** apzīmē grupu, kuru esat izveidojis vienam vai vairākiem debitoriem ar mērķi izsekot komisijas.</span><span class="sxs-lookup"><span data-stu-id="94c5b-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="94c5b-123">Vērtība tiek kopēta no Debitora kartes, bet to var mainīt, ja vēlaties.</span><span class="sxs-lookup"><span data-stu-id="94c5b-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="94c5b-124">Darbību rūtī atlasiet **Opcijas**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="94c5b-125">Atlasiet **Mainīt skatu**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-125">Select **Change view**.</span></span>
11. <span data-ttu-id="94c5b-126">Atlasīt **Rindas skats**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-126">Select **Line view**.</span></span>
12. <span data-ttu-id="94c5b-127">Lauka **Krājuma numurs** nolaižamajā izvēlnē atlasiet krājumu, ko esat iestatījis komisijām.</span><span class="sxs-lookup"><span data-stu-id="94c5b-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="94c5b-128">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="94c5b-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="94c5b-129">Ņemiet vērā rindas Neto summu.</span><span class="sxs-lookup"><span data-stu-id="94c5b-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="94c5b-130">Tie ir pārdošanas ieņēmumi, kuri šajā piemērā ir komisijas naudas aprēķina pamatā.</span><span class="sxs-lookup"><span data-stu-id="94c5b-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="94c5b-131">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-131">Select **Save**.</span></span>
15. <span data-ttu-id="94c5b-132">Darbības rūtī atlasiet **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="94c5b-133">Atlasīt **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="94c5b-134">Izvērsiet sadaļu **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="94c5b-135">Laukā **Daudzums** atlasiet vērtību **Visi**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="94c5b-136">Atlasiet vērtību **Jā** laukā **Grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="94c5b-137">Atlasiet **Labi**, pēc tam nākamajā rūtī atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="94c5b-138">Grāmatošana var ilgt kādu minūti.</span><span class="sxs-lookup"><span data-stu-id="94c5b-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="94c5b-139">Ļaujiet apstrādei beigties, neaizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="94c5b-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="94c5b-140">Reģistrēto pārdošanas komisiju pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="94c5b-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="94c5b-141">Darbības rūtī atlasiet **Rēķins** un pēc tam vēlreiz atlasiet **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="94c5b-142">Darbības rūtī atlasiet **Rēķins** un pēc tam atlasiet **Komisijas darbības**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="94c5b-143">Cilnē **Pārskats** ir parādītas rindas, kas atspoguļo pārdošanas pārstāvjiem maksājamās komisijas summas, kas ir saistītas ar rēķinā iekļauto pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="94c5b-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="94c5b-144">Apskatīsim to sīkāk.</span><span class="sxs-lookup"><span data-stu-id="94c5b-144">Let's review the details.</span></span>  
    - <span data-ttu-id="94c5b-145">Ja **Komisijas pārdošanas** grupas iestatīšanai izmantojāt ceļvedi “Pārdošanas komisijas noteikumu iestatīšana”, ir divi pārdevēji, kas saņems pārdošanas komisijas un komisija tiks sadalīta vienlīdzīgi starp tiem.</span><span class="sxs-lookup"><span data-stu-id="94c5b-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="94c5b-146">Šajā piemērā komisijas kopējā summa tiek aprēķināta kā procentuāla daļa no pārdošanas ieņēmumiem (pasūtījuma rindas neto summa).</span><span class="sxs-lookup"><span data-stu-id="94c5b-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="94c5b-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="94c5b-147">Close the page.</span></span>
4. <span data-ttu-id="94c5b-148">Izvēlēties **Dokuments**.</span><span class="sxs-lookup"><span data-stu-id="94c5b-148">Select **Voucher**.</span></span> <span data-ttu-id="94c5b-149">Varat pārskatīt dokumentu transakcijas par komisijas summām, kas tika iegrāmatotas iepriekš definētos komisijas izdevumu un maksājamo komisiju kontos.</span><span class="sxs-lookup"><span data-stu-id="94c5b-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]