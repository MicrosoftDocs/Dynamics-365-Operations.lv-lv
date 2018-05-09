--- 
title: "Piegādes grafika izveide"
description: "Šajā procedūrā ir parādīts, kā pārdošanas pasūtījumam izveidot piegādes grafiku."
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 407337d31e0aa68217a27a5709da16ddc7d6e4a1
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-delivery-schedule"></a><span data-ttu-id="fc9f7-103">Piegādes grafika izveide</span><span class="sxs-lookup"><span data-stu-id="fc9f7-103">Create a delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc9f7-104">Šajā procedūrā ir parādīts, kā pārdošanas pasūtījumam izveidot piegādes grafiku.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="fc9f7-105">Piegādes grafiks tiek izmantots, kad pasūtījumā vai piedāvājumā minēto daudzumu ir pieprasīts piegādāt vairākos sūtījumos.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="fc9f7-106">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="fc9f7-107">Izveidot piegādes grafiku</span><span class="sxs-lookup"><span data-stu-id="fc9f7-107">Create delivery schedule</span></span>
1. <span data-ttu-id="fc9f7-108">Dodieties uz Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="fc9f7-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-109">Click New.</span></span>
3. <span data-ttu-id="fc9f7-110">Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="fc9f7-111">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-111">Click OK.</span></span>
5. <span data-ttu-id="fc9f7-112">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="fc9f7-113">Laukā Daudzums ievadiet skaitli, kas ir lielāks par 1.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="fc9f7-114">Noklikšķiniet uz Pārdošanas pasūtījuma rinda.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-114">Click Sales order line.</span></span>
8. <span data-ttu-id="fc9f7-115">Noklikšķiniet uz Piegādes grafiks.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="fc9f7-116">Lapa Piegādes grafiks ir vieta, kur varat norādīt sūtījumu skaitu, kādā debitoram tiks piegādāts viss pasūtījuma rindas daudzums.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="fc9f7-117">Pēc noklusējuma sistēma no sākotnējās pārdošanas rindas uz pirmo piegādes grafika rindu kopē kopējo daudzumu un citu piegādes informāciju.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="fc9f7-118">Šajā piemērā mēs izveidosim grafiku diviem sūtījumiem, un otrā sūtījuma datumam no pirmā būs nobīde par vienu nedēļu.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="fc9f7-119">Laukā Daudzums ievadiet skaitli, kas ir daļa no kopējā daudzuma.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="fc9f7-120">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-120">Click New.</span></span>
11. <span data-ttu-id="fc9f7-121">Laukā Daudzums ievadiet atlikušo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="fc9f7-122">Laukā Pieprasītais nosūtīšanas datums ievadiet datumu, kas ir par vienu nedēļu uz priekšu no pirmās piegādes rindas datuma.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="fc9f7-123">Abas opcijas kopsavilkuma cilnē Izmaksu konvertēšana kontrolē veidu, kā šīs izmaksas jāsadala pa piegādes grafika rindām, kad tās ir piešķirtas sākotnējai pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="fc9f7-124">Ja atlasāt Kopēt bruto summas, tad uz katru rindu tiek kopēta tāda pati summa.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="fc9f7-125">Ar opciju Piešķirt piegādes rindām šīs izmaksas tiek vienmērīgi sadalītas pa piegādes rindām.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="fc9f7-126">Iespējams sadalīt tikai fiksētas izmaksas, bet mainīgās izmaksas joprojām tiks kopētas uz rindām.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="fc9f7-127">Pārvietojiet kursoru prom no otrās piegādes rindas, lai atjauninātu lapu.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="fc9f7-128">Piegādes grafika rindām piešķirtajam kopējam daudzumam varat sekot līdzi, apskatot laukus Kopsumma un Atlicis.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="fc9f7-129">Ja atlikušais daudzums ir nulle, grafikam ir piešķirts viss daudzums no sākotnējās rindas.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="fc9f7-130">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-130">Click OK.</span></span>
    * <span data-ttu-id="fc9f7-131">Tagad piegādes grafiks ir kopēts uz pasūtījuma rindām.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="fc9f7-132">Sākotnējā pasūtījuma rinda, ko sauc par komerciālo rindu, ir pārvērsta par pasūtījuma rindu ar vairākām piegādēm.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="fc9f7-133">Tā ir atzīmēta ar atšķirīgu ikonu un darbojas kā piegādes rindu virsraksts.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="fc9f7-134">Abas jaunās rindas, sauktas par piegādes rindām, veido vienu piegādes grafiku.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="fc9f7-135">Pasūtījums tiks apstrādāts pret šīm rindām, nevis sākotnējo rindu.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="fc9f7-136">Ja tiek drukāti dokumenti, piemēram, apstiprinājuma pavadzīmes, izdošanas saraksti, pavadzīmes vai rēķini, tiek rādītas tikai piegādes rindas.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="fc9f7-137">Piegādes rindām var būt atšķirīgi piegādes datumi, daudzumi, piegādes režīmi un noliktavas dimensijas, piemēram, vieta un noliktava.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="fc9f7-138">Taču preču dimensijām vienmēr ir jāatbilst komerciālajā rindā norādītajām, un tās nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="fc9f7-139">Laukā Daudzums ievadiet skaitli, kas ir lielāks par pašreizējo.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="fc9f7-140">Atlasiet komerciālo rindu, lai redzētu daudzuma pārrēķināšanas ietekmi.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="fc9f7-141">Darbību rūtī noklikšķiniet uz Izdot un iepakot.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="fc9f7-142">Noklikšķiniet uz Grāmatot pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="fc9f7-143">Izvērsiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="fc9f7-144">Laukā Daudzums atlasiet vērtību Visi.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="fc9f7-145">Ņemiet vērā, ka pavadzīme tiks izveidota abām piegādes grafika rindām, nevis sākotnējai pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="fc9f7-146">Laukā Drukāt pavadzīmi atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="fc9f7-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-147">Click OK.</span></span>
23. <span data-ttu-id="fc9f7-148">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-148">Click Yes.</span></span>
24. <span data-ttu-id="fc9f7-149">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="fc9f7-149">Close the page.</span></span>


