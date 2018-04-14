--- 
title: "Pārdošanas pasūtījumu apstiprināšana"
description: "Šajā procedūrā parādīts, kā apstiprināt pārdošanas pasūtījumus."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b60dbe15eca10511f4aaaf472b512eb003fbf6bc
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="confirm-sales-orders"></a><span data-ttu-id="da866-103">Pārdošanas pasūtījumu apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="da866-103">Confirm sales orders</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da866-104">Šajā procedūrā parādīts, kā apstiprināt pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="da866-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="da866-105">Tiek parādīts, kā apstiprināt vienu pasūtījumu un kā apstiprināt vairākus pasūtījumus uzreiz.</span><span class="sxs-lookup"><span data-stu-id="da866-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="da866-106">Šos uzdevumus parasti veic pārdošanas pasūtījumu apstrādātājs.</span><span class="sxs-lookup"><span data-stu-id="da866-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="da866-107">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="da866-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="da866-108">Pirms sākt, pārliecinieties, ka vienam debitoram ir vairāki atvērti pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="da866-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="da866-109">Ja izmantojat USMF, varat izmantot debitoru US-027.</span><span class="sxs-lookup"><span data-stu-id="da866-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="da866-110">Viena pārdošanas pasūtījuma apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="da866-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="da866-111">Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="da866-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="da866-112">Sarakstā atrodiet un atlasiet pasūtījumu, kuru vēlaties apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="da866-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="da866-113">Noklikšķiniet uz saites uz pārdošanas pasūtījuma numura, lai atvērtu atlasīto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="da866-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="da866-114">Darbību rūtī noklikšķiniet uz Pārdot.</span><span class="sxs-lookup"><span data-stu-id="da866-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="da866-115">Noklikšķiniet uz Apstiprināt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="da866-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="da866-116">Izvērsiet vai sakļaujiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="da866-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="da866-117">Pārliecinieties, ka lauks Grāmatošana Jā ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="da866-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="da866-118">Opcijai Drukāt apstiprinājumu iestatiet Jā.</span><span class="sxs-lookup"><span data-stu-id="da866-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="da866-119">Lauks Kredīta limita pārbaude norāda metodi, ko izmanto, lai aprēķinātu debitora atlikušo kredītu.</span><span class="sxs-lookup"><span data-stu-id="da866-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="da866-120">Pēc noklusējuma, tā tiek kopēta no lapas Debitoru moduļa parametri.</span><span class="sxs-lookup"><span data-stu-id="da866-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="da866-121">Ja vēlaties izlaist kredīta limita pārbaudi, apstiprinot specifisku pārdošanas pasūtījumu, iestatiet Kredīta limita pārbaude uz Nav.</span><span class="sxs-lookup"><span data-stu-id="da866-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="da866-122">Tomēr jums jāzina ka, pat ja šis lauks ir iestatīts uz Nav, kredīta limita pārbaude tiek joprojām veikta, ja debitoru pamatdatos ir atlasīta opcija Obligātais kredīta limits.</span><span class="sxs-lookup"><span data-stu-id="da866-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="da866-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="da866-123">Click OK.</span></span>
9. <span data-ttu-id="da866-124">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="da866-124">Click Yes.</span></span>
10. <span data-ttu-id="da866-125">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="da866-125">Close the page.</span></span>
11. <span data-ttu-id="da866-126">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="da866-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="da866-127">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="da866-127">Click Change view.</span></span>
13. <span data-ttu-id="da866-128">Noklikšķiniet uz Virsraksta skatījuma.</span><span class="sxs-lookup"><span data-stu-id="da866-128">Click Header view.</span></span>
    * <span data-ttu-id="da866-129">Kad pasūtījums ir apstiprināts, Dokumenta statuss tiek iestatīts uz Apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="da866-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="da866-130">Darbību rūtī noklikšķiniet uz Pārdot.</span><span class="sxs-lookup"><span data-stu-id="da866-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="da866-131">Noklikšķiniet uz Pārdošanas pasūtījuma apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="da866-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="da866-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="da866-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="da866-133">Vairāku pārdošanas pasūtījumu vienlaicīga apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="da866-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="da866-134">Dodieties uz Pārdošana un mārketings > Pārdošanas pasūtījumi > Pasūtījuma apstiprināšana > Apstiprināt pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="da866-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="da866-135">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="da866-135">Click Select.</span></span>
3. <span data-ttu-id="da866-136">Sarakstā cilnē Diapazons atrodiet un atlasiet ierakstu ar atsauci uz lauku Debitora konts.</span><span class="sxs-lookup"><span data-stu-id="da866-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="da866-137">Laukā Kritēriji noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="da866-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="da866-138">Sarakstā atrodiet un atlasiet debitora kontu, kam ir vairāki pasūtījumi, kurus vēlaties apstiprināt masveidā.</span><span class="sxs-lookup"><span data-stu-id="da866-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="da866-139">Ja izmantojat USMF, var atlasīt kontu US-027.</span><span class="sxs-lookup"><span data-stu-id="da866-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="da866-140">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="da866-140">Click OK.</span></span>
    * <span data-ttu-id="da866-141">Cilnē Pārskats tiek parādīts pasūtījumu saraksts, kas atbilst vaicājuma kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="da866-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="da866-142">Tie tiks iekļauti apstiprinājumā.</span><span class="sxs-lookup"><span data-stu-id="da866-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="da866-143">Laukā Kopgrāmatojums tiek norādīts parametrs, pēc kura vairāki pasūtījumi jāapkopo vienā apstiprinājuma dokumentā.</span><span class="sxs-lookup"><span data-stu-id="da866-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="da866-144">Pēc noklusējuma opcija tiek kopēta no iestatījuma Noklusētās vērtības kopgrāmatojumam lapā Debitoru moduļa parametri.</span><span class="sxs-lookup"><span data-stu-id="da866-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="da866-145">Laukā Kopgrāmatojums atlasiet vērtību “Pasūtījums”.</span><span class="sxs-lookup"><span data-stu-id="da866-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="da866-146">Minimālie parametri, lai izveidotu kopgrāmatojumus, ir Rēķina konts un Valūta.</span><span class="sxs-lookup"><span data-stu-id="da866-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="da866-147">Tas nozīmē, ka kopgrāmatojumi, kuriem ir citi rēķina konti un citas valūtas, nav atļauti.</span><span class="sxs-lookup"><span data-stu-id="da866-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="da866-148">Papildu parametrus var iestatīt lapā Kopgrāmatošanas parametri, kas ir pieejama no lapas Kreditoru parametri.</span><span class="sxs-lookup"><span data-stu-id="da866-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="da866-149">Laukā Pārdošanas pasūtījums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="da866-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="da866-150">Sarakstā atlasiet pasūtījuma numuru, kuru vēlaties padarīt par koppasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="da866-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="da866-151">Noklikšķiniet uz Sakārtot.</span><span class="sxs-lookup"><span data-stu-id="da866-151">Click Arrange.</span></span>
11. <span data-ttu-id="da866-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="da866-152">Click OK.</span></span>
12. <span data-ttu-id="da866-153">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="da866-153">Click OK.</span></span>


