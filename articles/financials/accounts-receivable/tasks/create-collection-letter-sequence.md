--- 
title: "Atgādinājuma vēstules secības izveide"
description: "Izmantojiet šo uzdevumu ceļvedi, lai izveidotu atgādinājuma vēstuļu sēriju."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6331c3680169b305c4bfbfada4ba106b619be092
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="d82b5-103">Atgādinājuma vēstules secības izveide</span><span class="sxs-lookup"><span data-stu-id="d82b5-103">Create a collection letter sequence</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d82b5-104">Izmantojiet šo uzdevumu ceļvedi, lai izveidotu atgādinājuma vēstuļu sēriju.</span><span class="sxs-lookup"><span data-stu-id="d82b5-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="d82b5-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="d82b5-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d82b5-106">Pārejiet uz sadaļu Kredīts un iekasēšana > Iestatījumi > Iestatīt atgādinājuma vēstuļu secību.</span><span class="sxs-lookup"><span data-stu-id="d82b5-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="d82b5-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d82b5-107">Click New.</span></span>
3. <span data-ttu-id="d82b5-108">Laukā Atgādinājuma vēstuļu sērija ievadiet sērijas ID, kas pārstāvēs sēriju.</span><span class="sxs-lookup"><span data-stu-id="d82b5-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="d82b5-109">Tas tiks izmantots, kad iestatīsit grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="d82b5-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="d82b5-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d82b5-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d82b5-111">Maksāšanas nosacījumi nav obligāti.</span><span class="sxs-lookup"><span data-stu-id="d82b5-111">The terms of payment is optional.</span></span> <span data-ttu-id="d82b5-112">Ja ievadāt vērtību šeit, atgādinājuma vēstules papildmaksas rēķinā tiks izmantoti šie maksāšanas nosacījumi, nevis debitoram saglabātie maksāšanas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="d82b5-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="d82b5-113">Laukā Atgādinājuma vēstules kods atlasiet kodu pirmajai atgādinājuma vēstulei, ko vēlaties nosūtīt.</span><span class="sxs-lookup"><span data-stu-id="d82b5-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="d82b5-114">Pirmā atgādinājuma vēstule tiek izveidota atbilstoši rēķina apmaksas termiņam, vērtībai, ko šai rindai ievadāt pagarinājuma periodam laukā Dienas, un atbilstoši citai informācijai, ko ievadāt šai rindai.</span><span class="sxs-lookup"><span data-stu-id="d82b5-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="d82b5-115">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d82b5-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d82b5-116">Papildmaksas valūta pēc noklusējuma tiek ņemta no debitora valūtas norādes.</span><span class="sxs-lookup"><span data-stu-id="d82b5-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="d82b5-117">Šis valūtas kods var atšķirties no rēķina valūtas.</span><span class="sxs-lookup"><span data-stu-id="d82b5-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="d82b5-118">Noklikšķiniet uz Pievienot, lai pievienotu nākamo atgādinājuma vēstuli, kas tiks nosūtīta šajā sērijā</span><span class="sxs-lookup"><span data-stu-id="d82b5-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="d82b5-119">Daudzos gadījumos pirmā atgādinājuma vēstule ir tikai brīdinājums.</span><span class="sxs-lookup"><span data-stu-id="d82b5-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="d82b5-120">Varat pievienot papildmaksas, ja tādas nepieciešamas.</span><span class="sxs-lookup"><span data-stu-id="d82b5-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="d82b5-121">Laukā Atgādinājuma vēstules kods atlasiet nākamo atgādinājuma vēstuli, kura tiks nosūtīta šajā sērijā.</span><span class="sxs-lookup"><span data-stu-id="d82b5-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="d82b5-122">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d82b5-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="d82b5-123">Laukā Galvenais konts atlasiet ieņēmumu kontu, kas tiks izmantots papildmaksām.</span><span class="sxs-lookup"><span data-stu-id="d82b5-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="d82b5-124">Ievadiet papildmaksu, kas jāattiecina, grāmatojot šo atgādinājuma vēstuli.</span><span class="sxs-lookup"><span data-stu-id="d82b5-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="d82b5-125">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d82b5-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="d82b5-126">Atlasiet krājuma PVN grupu, ja papildmaksai jāaprēķina PVN.</span><span class="sxs-lookup"><span data-stu-id="d82b5-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="d82b5-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d82b5-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d82b5-128">Ievadiet minimālo kavējuma bilanci, kuru nepieciešams sasniegt pirms atgādinājuma vēstules nosūtīšanas.</span><span class="sxs-lookup"><span data-stu-id="d82b5-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="d82b5-129">Ievadiet pieļaujamo pagarinājuma dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="d82b5-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="d82b5-130">Šis ir dienu skaits pēc apmaksas datuma, pēc kuru paiešanas var tikt ģenerēta atgādinājuma vēstule.</span><span class="sxs-lookup"><span data-stu-id="d82b5-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="d82b5-131">Aprēķinos izmantotais apmaksas datums ir atkarīgs no atgādinājuma vēstules pozīcijas atgādinājuma vēstuļu secībā: ⦁ 1. atgādinājuma vēstules pagarinājuma periods ir saistīts ar rēķinā norādīto apmaksas termiņu.</span><span class="sxs-lookup"><span data-stu-id="d82b5-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="d82b5-132">⦁ 2. un turpmāko atgādinājuma vēstuļu pagarinājuma periods ir saistīts ar datumu, kurā atkarībā no atlases lapas Debitoru parādu parametri laukā Atjaunināt atgādinājuma vēstules kodu ir iegrāmatota vai izdrukāta iepriekšējā atgādinājuma vēstule.</span><span class="sxs-lookup"><span data-stu-id="d82b5-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="d82b5-133">Noklikšķiniet uz Pievienot, lai pievienotu pēdējo atgādinājuma vēstuli, kas tiks nosūtīta šajā sērijā.</span><span class="sxs-lookup"><span data-stu-id="d82b5-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="d82b5-134">Atgādinājuma vēstuļu sērijai varat pievienot līdz pieciem atgādinājuma vēstuļu kodiem.</span><span class="sxs-lookup"><span data-stu-id="d82b5-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="d82b5-135">Laukā Atgādinājuma vēstules kods atlasiet nākamo atgādinājuma vēstuli, kura tiks nosūtīta šajā sērijā.</span><span class="sxs-lookup"><span data-stu-id="d82b5-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="d82b5-136">Laukā Apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d82b5-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="d82b5-137">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="d82b5-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="d82b5-138">Ievadiet skaitli laukā Papildmaksas valūta.</span><span class="sxs-lookup"><span data-stu-id="d82b5-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="d82b5-139">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d82b5-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="d82b5-140">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d82b5-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="d82b5-141">Ievadiet skaitli laukā Minimālā nokavētā bilance.</span><span class="sxs-lookup"><span data-stu-id="d82b5-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="d82b5-142">Ievadiet skaitli laukā Dienas.</span><span class="sxs-lookup"><span data-stu-id="d82b5-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="d82b5-143">Atzīmējiet šo izvēles rūtiņu, lai apturētu papildu piegādes un rēķinu piesūtīšanu klientam.</span><span class="sxs-lookup"><span data-stu-id="d82b5-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="d82b5-144">Lai kontu atbloķētu, rēķinu izrakstīšanā atlasiet Nē un debitoru lapā atlasiet piegādes aizturēšanas lauku.</span><span class="sxs-lookup"><span data-stu-id="d82b5-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="d82b5-145">Izvērsiet kopsavilkuma cilni Piezīme.</span><span class="sxs-lookup"><span data-stu-id="d82b5-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="d82b5-146">Ievadiet tekstu, kuru saturēs atgādinājuma vēstules ar atlasīto atgādinājuma vēstuļu kodu.</span><span class="sxs-lookup"><span data-stu-id="d82b5-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="d82b5-147">Varat iztulkot šo tekstu vairākās valodās, izmantojot izvēlni Tulkojumi, kas atrodas virs piezīmes lodziņa.</span><span class="sxs-lookup"><span data-stu-id="d82b5-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


