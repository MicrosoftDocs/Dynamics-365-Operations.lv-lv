---
title: Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma
description: Šajā procedūrā parādīts, kā izveidot pirkšanas pasūtījumu, pamatojoties uz pārdošanas pasūtījumu.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d7ce50532fb5bd6723b783d96d756085142e10
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843389"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="18d39-103">Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma</span><span class="sxs-lookup"><span data-stu-id="18d39-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18d39-104">Šajā procedūrā parādīts, kā izveidot pirkšanas pasūtījumu, pamatojoties uz pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="18d39-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="18d39-105">Pēc tam preces daudzums pirkšanas pasūtījumā tiek noteikts, lai nodrošinātu sākotnējā pārdošanas pasūtījuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="18d39-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="18d39-106">Pārdošanas pieprasījuma nodrošināšana šādā veidā ir alternatīvs risinājums aptverošākai un optimizētākai izplatīšanas prasību plānošanas metodei.</span><span class="sxs-lookup"><span data-stu-id="18d39-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="18d39-107">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="18d39-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="18d39-108">Pirkšanas pasūtījuma izveide no pārdošanas pasūtījuma</span><span class="sxs-lookup"><span data-stu-id="18d39-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="18d39-109">Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="18d39-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="18d39-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="18d39-110">Click New.</span></span>
3. <span data-ttu-id="18d39-111">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="18d39-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="18d39-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d39-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="18d39-113">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="18d39-113">Click OK.</span></span>
6. <span data-ttu-id="18d39-114">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="18d39-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="18d39-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d39-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="18d39-116">Ja izmantojat USMF, varat atlasīt D0001.</span><span class="sxs-lookup"><span data-stu-id="18d39-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="18d39-117">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="18d39-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="18d39-118">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="18d39-118">Click Add line.</span></span>
10. <span data-ttu-id="18d39-119">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="18d39-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="18d39-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d39-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="18d39-121">Ja izmantojat USMF, varat atlasīt T0020.</span><span class="sxs-lookup"><span data-stu-id="18d39-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="18d39-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d39-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="18d39-123">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="18d39-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="18d39-124">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="18d39-124">Click Save.</span></span>
15. <span data-ttu-id="18d39-125">Darbības rūtī noklikšķiniet uz vienuma Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="18d39-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="18d39-126">Noklikšķiniet uz Pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="18d39-126">Click Purchase order.</span></span>
    * <span data-ttu-id="18d39-127">Lapā Izveidot pirkšanas pasūtījumu ir parādīts visu atvērto pārdošanas pasūtījumu rindu saraksts, kas kopētas no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="18d39-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="18d39-128">Jūs varat pārskatīt pasūtījuma informāciju, un, ja nepieciešams, pārveidot izvēlēto informāciju, piemēram, pirkšanas daudzumu un cenas noteikšanas nosacījumus, pirms pirkumu izveidošanas.</span><span class="sxs-lookup"><span data-stu-id="18d39-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="18d39-129">Atlasiet opciju Iekļaut visus.</span><span class="sxs-lookup"><span data-stu-id="18d39-129">Select the Include all option.</span></span>
    * <span data-ttu-id="18d39-130">Ja vēlaties ģenerēt piegādes pasūtījumus tikai pārdošanas pasūtījumu rindu apakškopai, atlasiet tās atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="18d39-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="18d39-131">Lauks Kreditora konts var būt vai var nebūt aizpildīts ar kreditora numuru.</span><span class="sxs-lookup"><span data-stu-id="18d39-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="18d39-132">Ja precei ir iestatīts noklusējuma kreditors (saistītajās krājumu vajadzībās), šis kreditors tiks kopēts attiecīgajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d39-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="18d39-133">Pretējā gadījumā kreditors ir jāievada manuāli.</span><span class="sxs-lookup"><span data-stu-id="18d39-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="18d39-134">Šajā rokasgrāmatā neatkarīgi no tā, vai laukā Kreditora konts jau ir vērtība, tālāk aprakstītajās darbībās ir sniegti norādījumi atlasīt jaunu kreditoru, kas ir atšķirīgs katrai rindai.</span><span class="sxs-lookup"><span data-stu-id="18d39-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="18d39-135">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="18d39-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="18d39-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d39-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="18d39-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d39-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="18d39-138">Atlasiet otro pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="18d39-138">Select the second order line.</span></span>
22. <span data-ttu-id="18d39-139">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="18d39-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="18d39-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d39-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="18d39-141">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="18d39-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="18d39-142">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="18d39-142">Click Validate.</span></span>
26. <span data-ttu-id="18d39-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d39-143">Click OK.</span></span>
    * <span data-ttu-id="18d39-144">Ziņojums jūs informē, ka ir izveidots viens vai vairāki pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="18d39-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="18d39-145">Sistēma ģenerē atsevišķu pirkšanas pasūtījumu katram kreditoram, kas norādīts pārdošanas pasūtījumu rindām.</span><span class="sxs-lookup"><span data-stu-id="18d39-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="18d39-146">Tas nozīmē, ka gadījumā, ja vairākām pārdošanas rindām piegādi nodrošinās tas pats kreditors, tiks ģenerēts viens pirkšanas pasūtījums ar vairākām rindām.</span><span class="sxs-lookup"><span data-stu-id="18d39-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="18d39-147">No pārdošanas pasūtījumiem izveidotu pirkšanas pasūtījumu pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="18d39-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="18d39-148">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="18d39-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="18d39-149">Noklikšķiniet uz Saistītie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="18d39-149">Click Related orders.</span></span>
    * <span data-ttu-id="18d39-150">Lapā Saistītie pasūtījumi ir parādīts visu pasūtījumu saraksts, kas izveidoti no pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="18d39-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="18d39-151">Šajā piemērā ir divi pirkšanas pasūtījumi, kas attiecīgi izveidoti diviem dažādiem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="18d39-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="18d39-152">Noklikšķiniet, lai sekotu saitei laukā Pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="18d39-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="18d39-153">Katra pirkšanas pasūtījuma rinda ir saistīta ar pārdošanas pasūtījuma rindu, kas bija pirkšanas pamatā.</span><span class="sxs-lookup"><span data-stu-id="18d39-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="18d39-154">Saistība ar pārdošanas pasūtījumu ir norādīta kopsavilkuma cilnes Detalizēta rindas informācija cilnes Prece laukos Atsauces tips, Atsauces numurs un Atsauce uz partiju.</span><span class="sxs-lookup"><span data-stu-id="18d39-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="18d39-155">Izvērsiet vai sakļaujiet sadaļu Detalizēta rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="18d39-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="18d39-156">Noklikšķiniet uz cilnes Prece.</span><span class="sxs-lookup"><span data-stu-id="18d39-156">Click the Product tab.</span></span>
    * <span data-ttu-id="18d39-157">Lauks Atsauce uz partiju nodrošina, ka izmaksas no pašreizējā pirkuma tiek uzliktas piesaistītajam pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="18d39-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="18d39-158">Varat pārvietoties uz sākotnējo pārdošanas pasūtījumu, atverot saiti laukā Atsauces numurs.</span><span class="sxs-lookup"><span data-stu-id="18d39-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

