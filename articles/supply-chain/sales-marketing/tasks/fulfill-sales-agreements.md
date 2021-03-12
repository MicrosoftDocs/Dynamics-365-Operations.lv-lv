---
title: Pārdošanas līgumu nosacījumu izpilde
description: Šajā procedūrā ir parādīts, kā izpildīt pārdošanas līgumu, piesaistot tam pārdošanas pasūtījumus.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fca2f8777f5ce3b6a96be7fcab4f011aefd9d80b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991768"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="b7c67-103">Pārdošanas līgumu nosacījumu izpilde</span><span class="sxs-lookup"><span data-stu-id="b7c67-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b7c67-104">Šajā procedūrā ir parādīts, kā izpildīt pārdošanas līgumu, piesaistot tam pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="b7c67-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="b7c67-105">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="b7c67-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="b7c67-106">Pirms uzsākt darbu ar šo ceļvedi, pārliecinieties, ka jums ir spēkā esošs pārdošanas līgums, kura tips ir "Uz preču vērtību attiecināmas saistības".</span><span class="sxs-lookup"><span data-stu-id="b7c67-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="b7c67-107">Vai arī varat palaist uzdevuma ceļvedi ar nosaukumu "Pārdošanas līgumu izveide".</span><span class="sxs-lookup"><span data-stu-id="b7c67-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="b7c67-108">Pārdošanas pasūtījuma nodošana izpildei no līguma</span><span class="sxs-lookup"><span data-stu-id="b7c67-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="b7c67-109">Dodieties uz sadaļu Pārdošana un mārketings > Pārdošanas līgumi > Pārdošanas līgumi.</span><span class="sxs-lookup"><span data-stu-id="b7c67-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="b7c67-110">Sarakstā atveriet līgumu, uz kuru pamatojoties vēlaties veikt pasūtījuma nodošanu izpildei.</span><span class="sxs-lookup"><span data-stu-id="b7c67-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="b7c67-111">Darbības rūtī noklikšķiniet uz vienuma Pārdošanas līgums.</span><span class="sxs-lookup"><span data-stu-id="b7c67-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="b7c67-112">Noklikšķiniet uz Izpildīt pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-112">Click Release order.</span></span>
    * <span data-ttu-id="b7c67-113">Kā norādīts tekstā lapas Izveidot izpildpasūtījumu augšdaļā, informācija, kas nepieciešama pārdošanas pasūtījuma rindām atšķirsies atkarībā no tā, vai līgums ir balstīts uz daudzumu vai vērtību.</span><span class="sxs-lookup"><span data-stu-id="b7c67-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="b7c67-114">Šajā ceļvedī izmantotā līguma tips ir "Uz preču vērtību attiecināmas saistības".</span><span class="sxs-lookup"><span data-stu-id="b7c67-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="b7c67-115">Tādēļ šīs lapas sadaļa Rindas ir tukša.</span><span class="sxs-lookup"><span data-stu-id="b7c67-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="b7c67-116">Ja saistību pamatā būtu daudzums, rindas informācija tiktu kopēta no attiecīgā līguma.</span><span class="sxs-lookup"><span data-stu-id="b7c67-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="b7c67-117">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="b7c67-117">Click Create.</span></span>
    * <span data-ttu-id="b7c67-118">Ziņojums jūs informē, ka ir izveidots pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="b7c67-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="b7c67-119">Tā kā pasūtījumā nav nevienas rindas, ir jāpievieno pasūtījuma rindas informācija, lai pabeigtu nodošanas izpildei procesu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="b7c67-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-120">Close the page.</span></span>
7. <span data-ttu-id="b7c67-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-121">Close the page.</span></span>
8. <span data-ttu-id="b7c67-122">Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="b7c67-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="b7c67-123">Sarakstā atrodiet un atveriet pasūtījumu, kurš tika izveidots iepriekšējā uzdevumā veiktās pasūtījuma nodošanas izpildei rezultātā.</span><span class="sxs-lookup"><span data-stu-id="b7c67-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="b7c67-124">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-124">Click Add line.</span></span>
11. <span data-ttu-id="b7c67-125">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="b7c67-126">Laukā Krājuma numurs ierakstiet vai atlasiet krājumu, kas norādīts saistītajā pārdošanas līgumā.</span><span class="sxs-lookup"><span data-stu-id="b7c67-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="b7c67-127">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="b7c67-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b7c67-128">Pārliecinieties, ka ievadāt daudzumu, kas apvieno neto summu saskaņā ar saistīto pārdošanas līguma vērtību.</span><span class="sxs-lookup"><span data-stu-id="b7c67-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="b7c67-129">Ņemiet vērā, ka pārdošanas pasūtījums ir saistīts ar līgumu, tādēļ pasūtījuma rindai tiek piemērota atlaide procentos, par kuru panākta vienošanās.</span><span class="sxs-lookup"><span data-stu-id="b7c67-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="b7c67-130">Noklikšķiniet uz Labot rindu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-130">Click Update line.</span></span>
15. <span data-ttu-id="b7c67-131">Noklikšķiniet uz Piesaistīts.</span><span class="sxs-lookup"><span data-stu-id="b7c67-131">Click Attached.</span></span>
    * <span data-ttu-id="b7c67-132">Lapā Piesaistītais līgums tiek parādīts tā līguma ID un nosacījumi, no kura rinda tiek nodota izpildei.</span><span class="sxs-lookup"><span data-stu-id="b7c67-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="b7c67-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-133">Close the page.</span></span>
17. <span data-ttu-id="b7c67-134">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="b7c67-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="b7c67-135">Noklikšķiniet uz Piesaistītais pārdošanas līgums.</span><span class="sxs-lookup"><span data-stu-id="b7c67-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="b7c67-136">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="b7c67-137">Noklikšķiniet uz cilnes Izpilde.</span><span class="sxs-lookup"><span data-stu-id="b7c67-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="b7c67-138">Cilnē Izpilde ir parādīts kopsavilkums par visām pārdošanas pasūtījuma rindām, kas ir saistītas ar šīm saistībām, un to izpildes stāvokli, kā arī daudzumu, kas vēl nav nodots izpildei.</span><span class="sxs-lookup"><span data-stu-id="b7c67-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="b7c67-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-139">Close the page.</span></span>
22. <span data-ttu-id="b7c67-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-140">Close the page.</span></span>
23. <span data-ttu-id="b7c67-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="b7c67-142">Pārdošanas līguma lietošana pasūtījuma procesā</span><span class="sxs-lookup"><span data-stu-id="b7c67-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="b7c67-143">Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="b7c67-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="b7c67-144">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b7c67-144">Click New.</span></span>
3. <span data-ttu-id="b7c67-145">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b7c67-146">Sarakstā atrodiet un atlasiet debitoru, kas norādīts pārdošanas līgumā.</span><span class="sxs-lookup"><span data-stu-id="b7c67-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="b7c67-147">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b7c67-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b7c67-148">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="b7c67-148">Expand the General section.</span></span>
7. <span data-ttu-id="b7c67-149">Laukā Pārdošanas līguma ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b7c67-150">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b7c67-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b7c67-151">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="b7c67-151">Click Yes.</span></span>
10. <span data-ttu-id="b7c67-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b7c67-152">Click OK.</span></span>
11. <span data-ttu-id="b7c67-153">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="b7c67-154">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b7c67-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="b7c67-155">Laukā Krājuma numurs ierakstiet vai atlasiet krājumu, kas norādīts saistītajā pārdošanas līgumā.</span><span class="sxs-lookup"><span data-stu-id="b7c67-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="b7c67-156">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b7c67-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="b7c67-157">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b7c67-157">Click Save.</span></span>
16. <span data-ttu-id="b7c67-158">Darbību rūtī noklikšķiniet uz Izdot un iepakot.</span><span class="sxs-lookup"><span data-stu-id="b7c67-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="b7c67-159">Noklikšķiniet uz Grāmatot pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="b7c67-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="b7c67-160">Izvērsiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="b7c67-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="b7c67-161">Laukā Grāmatošana atlasiet vērtību Jā.</span><span class="sxs-lookup"><span data-stu-id="b7c67-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="b7c67-162">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b7c67-162">Click OK.</span></span>
21. <span data-ttu-id="b7c67-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b7c67-163">Click OK.</span></span>
22. <span data-ttu-id="b7c67-164">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="b7c67-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="b7c67-165">Noklikšķiniet uz Piesaistītais pārdošanas līgums.</span><span class="sxs-lookup"><span data-stu-id="b7c67-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="b7c67-166">Noklikšķiniet uz cilnes Izpilde.</span><span class="sxs-lookup"><span data-stu-id="b7c67-166">Click the Fulfillment tab.</span></span>

