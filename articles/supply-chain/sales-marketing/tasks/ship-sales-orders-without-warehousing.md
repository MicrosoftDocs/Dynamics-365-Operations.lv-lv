---
title: Pārdošanas pasūtījumu sūtīšana bez noliktavas
description: Šajā tēmā paskaidrots, kā atjaunināt pārdošanas pasūtījumu, kad preces tiek nosūtītas debitoram.
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a2079ae02c01d30eb648e9cc95ee9cf6599048b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205885"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="f423d-103">Pārdošanas pasūtījumu sūtīšana bez noliktavas</span><span class="sxs-lookup"><span data-stu-id="f423d-103">Ship sales orders without warehousing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f423d-104">Šajā tēmā paskaidrots, kā atjaunināt pārdošanas pasūtījumu, kad preces tiek nosūtītas debitoram.</span><span class="sxs-lookup"><span data-stu-id="f423d-104">This topic explains how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="f423d-105">Šis ceļvedis attiecas uz izpildes plūsmu, kas nav iestatīta noliktavas vadībai (ne pamata, ne uzlabotai noliktavai), un tādēļ preču izdošana nav jāreģistrē pirms nosūtīšanas.</span><span class="sxs-lookup"><span data-stu-id="f423d-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="f423d-106">Šo procedūru varat izpildīt, izmantojot savus datus vai demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="f423d-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="f423d-107">Abos gadījumos, pirms sākt šo uzdevumu, izveidojiet pārdošanas pasūtījumu inventarizētajai precei, kuras daudzums ir lielāks nekā 1</span><span class="sxs-lookup"><span data-stu-id="f423d-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="f423d-108">Lai izvairītos no grāmatošanas kļūdas, nepieciešams pārbaudīt, vai preces rīcībā esošais daudzums vietā un noliktavā, ko atlasījāt pasūtījumā, sedz pasūtījuma daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f423d-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you've selected on the order covers the order quantity.</span></span>

## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="f423d-109">Pasūtījuma pavadzīmes grāmatošana</span><span class="sxs-lookup"><span data-stu-id="f423d-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="f423d-110">Navigācijas panelī atveriet **Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="f423d-110">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="f423d-111">Sarakstā atrodiet un atlasiet pasūtījumu, kas izveidots šim uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="f423d-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="f423d-112">Darbību rūtī noklikšķiniet uz **Izdot un iepakot**.</span><span class="sxs-lookup"><span data-stu-id="f423d-112">On the Action Pane, select **Pick and pack**.</span></span>
4. <span data-ttu-id="f423d-113">Atlasiet **Grāmatot pavadzīmi**.</span><span class="sxs-lookup"><span data-stu-id="f423d-113">Select **Post packing slip**.</span></span>
5. <span data-ttu-id="f423d-114">Izvērsiet vai sakļaujiet sadaļu **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="f423d-114">Expand or collapse the **Parameters** section.</span></span>
6. <span data-ttu-id="f423d-115">Laukā **Daudzums** atlasiet vērtību **Visi**.</span><span class="sxs-lookup"><span data-stu-id="f423d-115">In the **Quantity** field, select **All**.</span></span>
    - <span data-ttu-id="f423d-116">Citas opcijas ietver **Piegādāt tūlīt** un **Izdots**.</span><span class="sxs-lookup"><span data-stu-id="f423d-116">Other options include **Deliver now** and **Picked**.</span></span> <span data-ttu-id="f423d-117">Ja pasūtījuma rinda ir jānosūta daļēji un laukā **Piegādāt tūlīt** pasūtījuma rindā ir norādīts daudzums, jums jāatlasa **Piegādāt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="f423d-117">If the order line is to be shipped partially and the **Deliver now** field on the order line contains a quantity, you would select **Deliver now**.</span></span> <span data-ttu-id="f423d-118">Ja jūsu organizācijas izpildes plūsma ietver izdošanu kā atsevišķu procesu, kas tiek pārvaldīts un reģistrēts ar izdošanas sarakstu, jums jāatlasa **Izdots**.</span><span class="sxs-lookup"><span data-stu-id="f423d-118">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select **Picked**.</span></span>  
    - <span data-ttu-id="f423d-119">Pārbaudiet, vai opcija **Grāmatošana** ir iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="f423d-119">Check that the **Posting** option is set to **Yes**.</span></span>  
7. <span data-ttu-id="f423d-120">Opcijai **Drukāt pavadzīmi** iestatiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="f423d-120">Set the **Print packing slip** option to **Yes**.</span></span> <span data-ttu-id="f423d-121">Cilne **Pārskats** satur pavadzīmju sarakstu, kas jāģenerē šīs grāmatošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="f423d-121">The **Overview** tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="f423d-122">Ja nosūtat atsevišķu pasūtījumu, parasti būs viena pavadzīme.</span><span class="sxs-lookup"><span data-stu-id="f423d-122">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="f423d-123">Tomēr, ja šī pasūtījuma rindas tiek nosūtītas no dažādām vietām, grāmatošana tiks automātiski sadalīta atbilstošā dokumentu skaitā.</span><span class="sxs-lookup"><span data-stu-id="f423d-123">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="f423d-124">Tas ir obligāts nosacījums, ko nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="f423d-124">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="f423d-125">Tāpat grāmatošana tiks sadalīta vairākos dokumentos, ja šī pasūtījuma rindas jānosūta uz dažādām piegādes adresēm un nosūtīšanas politika ir iestatīta tā, lai būtu nepieciešams sadalījums.</span><span class="sxs-lookup"><span data-stu-id="f423d-125">Similarly, the posting will also be split into multiple documents if the order's lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
8. <span data-ttu-id="f423d-126">Cilnē **Rindas** atlasiet rindu pasūtījuma rindai, kas tiks nosūtīta.</span><span class="sxs-lookup"><span data-stu-id="f423d-126">On the **Lines** tab, select the row for the order line to be shipped.</span></span>
9. <span data-ttu-id="f423d-127">Laukā **Atjaunināt** ievadiet skaitli, kas ir mazāks par sākotnējo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f423d-127">In the **Update** field, enter a number lower than the original quantity.</span></span>
10. <span data-ttu-id="f423d-128">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f423d-128">Select **OK**.</span></span>
11. <span data-ttu-id="f423d-129">Atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="f423d-129">Select **Yes**.</span></span>
12. <span data-ttu-id="f423d-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f423d-130">Close the page.</span></span>
13. <span data-ttu-id="f423d-131">Darbību rūtī atlasiet **Opcijas**.</span><span class="sxs-lookup"><span data-stu-id="f423d-131">On the Action Pane, select **Options**.</span></span>
14. <span data-ttu-id="f423d-132">Atlasiet **Mainīt skatu**.</span><span class="sxs-lookup"><span data-stu-id="f423d-132">Select **Change view**.</span></span>
15. <span data-ttu-id="f423d-133">Atlasiet **Virsraksta skats**.</span><span class="sxs-lookup"><span data-stu-id="f423d-133">Select **Header view**.</span></span>
    - <span data-ttu-id="f423d-134">Ja visas pasūtījuma rindas ir pilnībā nosūtītas, pasūtījuma statuss mainās no Atvērts uz Piegādāts.</span><span class="sxs-lookup"><span data-stu-id="f423d-134">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    - <span data-ttu-id="f423d-135">Šajā piemērā pasūtījuma rinda ir daļēji nosūtīta.</span><span class="sxs-lookup"><span data-stu-id="f423d-135">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="f423d-136">Tāpēc pasūtījuma statuss paliek Atvērts.</span><span class="sxs-lookup"><span data-stu-id="f423d-136">This is why the the order status remains Open.</span></span>     
    - <span data-ttu-id="f423d-137">Lauks **Dokumenta statuss** ir iestatīts uz Pavadzīme, jo vismaz viena no pasūtījuma rindām ir nosūtīta.</span><span class="sxs-lookup"><span data-stu-id="f423d-137">The **Document status** field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
16. <span data-ttu-id="f423d-138">Darbību rūtī atlasiet **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="f423d-138">On the Action Pane, select **General**.</span></span>
17. <span data-ttu-id="f423d-139">Atlasiet **Rindas daudzums**.</span><span class="sxs-lookup"><span data-stu-id="f423d-139">Select **Line quantity**.</span></span>
18. <span data-ttu-id="f423d-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f423d-140">Close the page.</span></span>
19. <span data-ttu-id="f423d-141">Darbību rūtī noklikšķiniet uz **Izdot un iepakot**.</span><span class="sxs-lookup"><span data-stu-id="f423d-141">On the Action Pane, select **Pick and pack**.</span></span>
20. <span data-ttu-id="f423d-142">Atlasiet **Pavadzīme**.</span><span class="sxs-lookup"><span data-stu-id="f423d-142">Select **Packing slip**.</span></span> <span data-ttu-id="f423d-143">Lapa **Pavadzīmju žurnāls** satur visus pavadzīmes dokumentus, kas tika ģenerēti pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="f423d-143">The **Packing slip journal** page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="f423d-144">Ja vēlaties, varat pārskatīt datus par katru dokumentu un izdrukāt tos.</span><span class="sxs-lookup"><span data-stu-id="f423d-144">You can review details of each document and print them, if you wish.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]