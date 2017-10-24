--- 
title: "Periodu žurnālu grāmatošana"
description: "Periodiskos žurnālus reizēm sauc par cikliski atkārtotajiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtoti katru reizi, kad šis periodiskais žurnāls tiek izgūts."
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8eae11e0501db78e467e517b29a2bc19f5765e75
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="post-periodic-journals"></a><span data-ttu-id="28500-103">Periodu žurnālu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="28500-103">Post periodic journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28500-104">Periodiskos žurnālus reizēm sauc par cikliski atkārtotajiem žurnāliem, jo summa, teksts un cita informācija tiek atkārtoti katru reizi, kad šis periodiskais žurnāls tiek izgūts.</span><span class="sxs-lookup"><span data-stu-id="28500-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="28500-105">Kad veidojat periodisko žurnālu, norādiet atkārtošanās perioda intervālu, piemēram, dienas vai mēnešus.</span><span class="sxs-lookup"><span data-stu-id="28500-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="28500-106">Šajā uzdevuma ceļvedī tiks izveidots periodisks žurnāls ar atkārtošanos katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="28500-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="28500-107">Dodieties uz Virsgrāmata > Periodiskie uzdevumi > Periodiskie žurnāli.</span><span class="sxs-lookup"><span data-stu-id="28500-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="28500-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="28500-108">Click New.</span></span>
3. <span data-ttu-id="28500-109">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="28500-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="28500-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="28500-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="28500-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="28500-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="28500-112">Šis apraksts būs periodiskā žurnāla nosaukums, kad tas vēlāk tiks izgūts, tāpēc nodrošiniet, lai tam tiktu piešķirts piemērots nosaukums.</span><span class="sxs-lookup"><span data-stu-id="28500-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="28500-113">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="28500-113">Click Lines.</span></span>
    * <span data-ttu-id="28500-114">Periodiskā žurnālā parasti ir ietvertas vairākas žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="28500-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="28500-115">Taču šajā uzdevuma ceļvedī tiks pievienota tikai viena rinda.</span><span class="sxs-lookup"><span data-stu-id="28500-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="28500-116">Laukā Datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="28500-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="28500-117">Laukā Datums ir norādīts grāmatošanas datums nākamajai pārsūtīšanai uz ikdienas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="28500-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="28500-118">Žurnāliem, kas tiks izgūti katru mēnesi, ir ieteicams lietot tādu mēneša datumu, kad žurnāls tiks grāmatots, parasti tas ir pirmais vai pēdējais datums attiecīgajā periodā.</span><span class="sxs-lookup"><span data-stu-id="28500-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="28500-119">Lauku Datums var atstāt tukšu, un datumu var piešķirt, kad žurnāls tiek izgūts, izmantojot lauku Tukšs datums.</span><span class="sxs-lookup"><span data-stu-id="28500-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="28500-120">Kad transakcijas tiek izgūtas, šis lauks automātiski tiek atjaunināts uz nākamo periodisko datumu.</span><span class="sxs-lookup"><span data-stu-id="28500-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="28500-121">Laukā Konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="28500-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="28500-122">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="28500-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="28500-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="28500-123">Close the page.</span></span>
11. <span data-ttu-id="28500-124">Laukā Debets ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="28500-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="28500-125">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="28500-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="28500-126">Laukā Vienība atlasiet vērtību “Mēneši”.</span><span class="sxs-lookup"><span data-stu-id="28500-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="28500-127">Laukā Vienību skaits ievadiet “1”.</span><span class="sxs-lookup"><span data-stu-id="28500-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="28500-128">Laukā Pēdējais datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="28500-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="28500-129">Ievadot iepriekšējā perioda pēdējo datumu, tiek novērsta iespēja, ka periodiskais žurnāls nejauši tiek izveidots nepareizajā sākuma periodā.</span><span class="sxs-lookup"><span data-stu-id="28500-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="28500-130">Vēlāk pēdējais datums tiks atjaunināts katru reizi, kad periodiskais žurnāls tiek izgūts.</span><span class="sxs-lookup"><span data-stu-id="28500-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="28500-131">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="28500-131">Click Save.</span></span>
17. <span data-ttu-id="28500-132">Dodieties uz Noklusējuma informācijas panelis.</span><span class="sxs-lookup"><span data-stu-id="28500-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="28500-133">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="28500-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="28500-134">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="28500-134">Click New.</span></span>
20. <span data-ttu-id="28500-135">Laukā Nosaukums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="28500-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="28500-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="28500-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="28500-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="28500-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="28500-138">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="28500-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="28500-139">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="28500-139">Click Lines.</span></span>
25. <span data-ttu-id="28500-140">Noklikšķiniet uz Periodisko darbību žurnāls.</span><span class="sxs-lookup"><span data-stu-id="28500-140">Click Period journal.</span></span>
26. <span data-ttu-id="28500-141">Noklikšķiniet uz Izgūt žurnālu.</span><span class="sxs-lookup"><span data-stu-id="28500-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="28500-142">Laukā Līdz datumam ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="28500-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="28500-143">Vienums Līdz datumam darbojas kā robeždatums attiecībā uz periodiskajām dokumentu rindām.</span><span class="sxs-lookup"><span data-stu-id="28500-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="28500-144">Pamatojoties uz periodiskuma iestatījumu, vienas un tas pašas rindas vērtības Pēdējais datums un Līdz datumam galīgajā žurnālā var būt iekļautas vairākas reizes.</span><span class="sxs-lookup"><span data-stu-id="28500-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="28500-145">Vērtība Līdz datumam tiek automātiski atjaunināta, ņemot vērā sesijas datumu pēdējā reizē, kad periodiskā rinda tika pārsūtīta uz žurnālu.</span><span class="sxs-lookup"><span data-stu-id="28500-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="28500-146">Laukā Periodiskā žurnāla numurs ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="28500-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="28500-147">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="28500-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="28500-148">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="28500-148">Click OK.</span></span>
    * <span data-ttu-id="28500-149">Tagad periodisko darbību žurnālu var pārskatīt, apstiprināt vai grāmatot atkarībā no pieprasījuma un iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="28500-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


