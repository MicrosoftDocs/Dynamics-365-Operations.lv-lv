--- 
title: "Pārdošanas pasūtījumu sūtīšana bez noliktavas"
description: "Šajā ceļvedī ir parādīts, kā atjaunināt pārdošanas pasūtījumu, kad preces tiek nosūtītas debitoram."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1d4d43ca62901ecd2280f21dfbeee9cb70ec600e
ms.contentlocale: lv-lv
ms.lasthandoff: 09/11/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="eb3b2-103">Pārdošanas pasūtījumu sūtīšana bez noliktavas</span><span class="sxs-lookup"><span data-stu-id="eb3b2-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb3b2-104">Šajā ceļvedī ir parādīts, kā atjaunināt pārdošanas pasūtījumu, kad preces tiek nosūtītas debitoram.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="eb3b2-105">Šis ceļvedis attiecas uz izpildes plūsmu, kas nav iestatīta noliktavas vadībai (ne pamata, ne uzlabotai noliktavai), un tādēļ preču izdošana nav jāreģistrē pirms nosūtīšanas.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="eb3b2-106">Šo procedūru varat izpildīt, izmantojot savus datus vai demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="eb3b2-107">Abos gadījumos, pirms sākt šo uzdevumu, izveidojiet pārdošanas pasūtījumu inventarizētajai precei, kuras daudzums ir lielāks nekā 1</span><span class="sxs-lookup"><span data-stu-id="eb3b2-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="eb3b2-108">Lai izvairītos no grāmatošanas kļūdas, nepieciešams pārbaudīt, vai preces rīcībā esošais daudzums vietā un noliktavā, ko atlasījāt pasūtījumā, sedz pasūtījuma daudzumu.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="eb3b2-109">Pasūtījuma pavadzīmes grāmatošana</span><span class="sxs-lookup"><span data-stu-id="eb3b2-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="eb3b2-110">Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="eb3b2-111">Sarakstā atrodiet un atlasiet pasūtījumu, kas izveidots šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="eb3b2-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="eb3b2-113">Darbību rūtī noklikšķiniet uz Izdot un iepakot.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="eb3b2-114">Noklikšķiniet uz Grāmatot pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="eb3b2-115">Izvērsiet vai sakļaujiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="eb3b2-116">Laukā Daudzums atlasiet vērtību Visi.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="eb3b2-117">Citas opcijas ietver Piegādāt tūlīt un Izdots.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="eb3b2-118">Ja pasūtījuma rinda ir jānosūta daļēji un laukā Piegādāt tūlīt pasūtījuma rindā ir norādīts daudzums, jums jāatlasa Piegādāt tūlīt.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="eb3b2-119">Ja jūsu organizācijas izpildes plūsma ietver izdošanu kā atsevišķu procesu, kas tiek pārvaldīts un reģistrēts ar izdošanas sarakstu, jums jāatlasa Izdots.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="eb3b2-120">Pārbaudiet, vai opcija Grāmatošana ir iestatīta uz Jā.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="eb3b2-121">Opcijai Drukāt pavadzīmi iestatiet Jā.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="eb3b2-122">Cilne Pārskats satur pavadzīmju sarakstu, kas jāģenerē šīs grāmatošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="eb3b2-123">Ja nosūtat atsevišķu pasūtījumu, parasti būs viena pavadzīme.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="eb3b2-124">Tomēr, ja šī pasūtījuma rindas tiek nosūtītas no dažādām vietām, grāmatošana tiks automātiski sadalīta atbilstošā dokumentu skaitā.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="eb3b2-125">Tas ir obligāts nosacījums, ko nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="eb3b2-126">Tāpat grāmatošana tiks sadalīta vairākos dokumentos, ja šī pasūtījuma rindas jānosūta uz dažādām piegādes adresēm un nosūtīšanas politika ir iestatīta tā, lai būtu nepieciešams sadalījums.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="eb3b2-127">Cilnē Rindas atlasiet rindu pasūtījuma rindai, kas tiks nosūtīta.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="eb3b2-128">Laukā Atjaunināt ievadiet skaitli, kas ir mazāks par sākotnējo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="eb3b2-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-129">Click OK.</span></span>
12. <span data-ttu-id="eb3b2-130">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-130">Click Yes.</span></span>
13. <span data-ttu-id="eb3b2-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-131">Close the page.</span></span>
14. <span data-ttu-id="eb3b2-132">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="eb3b2-133">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-133">Click Change view.</span></span>
16. <span data-ttu-id="eb3b2-134">Noklikšķiniet uz Virsraksta skatījuma.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-134">Click Header view.</span></span>
    * <span data-ttu-id="eb3b2-135">Ja visas pasūtījuma rindas ir pilnībā nosūtītas, pasūtījuma statuss mainās no Atvērts uz Piegādāts.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="eb3b2-136">Šajā piemērā pasūtījuma rinda ir daļēji nosūtīta.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="eb3b2-137">Tāpēc pasūtījuma statuss paliek Atvērts.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="eb3b2-138">Lauks Dokumenta statuss ir iestatīts uz Pavadzīme, jo vismaz viena no pasūtījuma rindām ir nosūtīta.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="eb3b2-139">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="eb3b2-140">Noklikšķiniet uz Rindas daudzums.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-140">Click Line quantity.</span></span>
19. <span data-ttu-id="eb3b2-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-141">Close the page.</span></span>
20. <span data-ttu-id="eb3b2-142">Darbību rūtī noklikšķiniet uz Izdot un iepakot.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="eb3b2-143">Noklikšķiniet uz Pavadzīme.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-143">Click Packing slip.</span></span>
    * <span data-ttu-id="eb3b2-144">Lapa Pavadzīmju žurnāls satur visus pavadzīmes dokumentus, kas tika ģenerēti pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="eb3b2-145">Ja vēlaties, varat pārskatīt datus par katru dokumentu un izdrukāt tos.</span><span class="sxs-lookup"><span data-stu-id="eb3b2-145">You can review details of each document and print them, if you wish.</span></span>  


