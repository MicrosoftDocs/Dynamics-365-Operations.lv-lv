--- 
title: "PP piedāvājumu ievade un salīdzināšana un līgumu piešķiršana"
description: "Šajā procedūrā ir parādīts, kā ievadīt atbildes uz PP, noteikt punktu skaitu un salīdzināt piedāvājumus, un kā pēc tam piešķirt piedāvājumu vienam no kreditoriem."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="9ed27-103">PP piedāvājumu ievade un salīdzināšana un līgumu piešķiršana</span><span class="sxs-lookup"><span data-stu-id="9ed27-103">Enter and compare RFQ bids and award contracts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ed27-104">Šajā procedūrā ir parādīts, kā ievadīt atbildes uz PP, noteikt punktu skaitu un salīdzināt piedāvājumus, un kā pēc tam piešķirt piedāvājumu vienam no kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9ed27-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="9ed27-105">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="9ed27-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="9ed27-106">Pirms sākšanas jums ir nepieciešams PP ar divām rindām, kas ir nosūtīts vismaz diviem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9ed27-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="9ed27-107">Kā priekšnosacījumu tā izveidošanai varat palaist procedūru “Izveidot piedāvājuma pieprasījumu”.</span><span class="sxs-lookup"><span data-stu-id="9ed27-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="9ed27-108">Lai varētu palaist šo procedūru, ir nepieciešams iestatīt punktu skaitīšanas kritērijus.</span><span class="sxs-lookup"><span data-stu-id="9ed27-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="9ed27-109">Ievadīt atbildi no kreditora</span><span class="sxs-lookup"><span data-stu-id="9ed27-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="9ed27-110">Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Visi piedāvājumu pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="9ed27-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="9ed27-111">Atlasiet PP, kura statuss ir Nosūtīts, un noklikšķiniet uz numura Piedāvājuma pieprasījuma gadījums saites.</span><span class="sxs-lookup"><span data-stu-id="9ed27-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="9ed27-112">PP ir jāsūta vismaz 2 kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9ed27-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="9ed27-113">Noklikšķiniet uz Virsraksts, lai dotos uz kreditoru sarakstu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="9ed27-114">Atlasiet kreditoru, kuram vēlaties ievadīt PP atbildi.</span><span class="sxs-lookup"><span data-stu-id="9ed27-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="9ed27-115">Noklikšķiniet uz Ievadīt atbildi.</span><span class="sxs-lookup"><span data-stu-id="9ed27-115">Click Enter reply.</span></span>
6. <span data-ttu-id="9ed27-116">Darbību rūtī noklikšķiniet uz Atbilde.</span><span class="sxs-lookup"><span data-stu-id="9ed27-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="9ed27-117">Noklikšķiniet uz Kopēt datus uz atbildēm.</span><span class="sxs-lookup"><span data-stu-id="9ed27-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="9ed27-118">Ar šo darbību atlasītie dati, piemēram, daudzums, no PP gadījuma tiks kopēti uz PP atbildi.</span><span class="sxs-lookup"><span data-stu-id="9ed27-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="9ed27-119">Alternatīvi šo darbību varat izlaist un visus atbildes laukus aizpildīt manuāli, kad rediģējat atbildi.</span><span class="sxs-lookup"><span data-stu-id="9ed27-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="9ed27-120">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9ed27-120">Click Edit.</span></span>
9. <span data-ttu-id="9ed27-121">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9ed27-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="9ed27-122">Izvēlēties otru piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="9ed27-123">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9ed27-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="9ed27-124">Skaitīt piedāvājuma punktus</span><span class="sxs-lookup"><span data-stu-id="9ed27-124">Score the bid</span></span>
1. <span data-ttu-id="9ed27-125">Noklikšķiniet uz Virsraksts, lai dotos uz piedāvājuma punktu skaitīšanu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="9ed27-126">Izvērsiet piedāvājuma punktu skaitīšanas sadaļu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="9ed27-127">Laukā Punktu skaits ievadiet numuru vienam no punktu skaitīšanas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="9ed27-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="9ed27-128">Ja peles kursoru novietojat virs viena no punktu skaitīšanas kritērija, ar rīka padomu tiek parādīts nepieciešamo punktu diapazons.</span><span class="sxs-lookup"><span data-stu-id="9ed27-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="9ed27-129">Šajā demonstrācijā jebkuram kritērijam varat pievienot skaitli no 1 līdz 5.</span><span class="sxs-lookup"><span data-stu-id="9ed27-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="9ed27-130">Atlasiet citu punktu skaitīšanas kritēriju.</span><span class="sxs-lookup"><span data-stu-id="9ed27-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="9ed27-131">Laukā Punktu skaits ievadiet kādu numuru.</span><span class="sxs-lookup"><span data-stu-id="9ed27-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="9ed27-132">Izvērsiet sadaļu Anketas.</span><span class="sxs-lookup"><span data-stu-id="9ed27-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="9ed27-133">Ja PP gadījumam ir anketa, kas tika nosūtīta kreditoriem, tad anketas sadaļā varat ievadīt viņu atbildes.</span><span class="sxs-lookup"><span data-stu-id="9ed27-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="9ed27-134">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="9ed27-135">Ievadīt atbildi citam kreditoram</span><span class="sxs-lookup"><span data-stu-id="9ed27-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="9ed27-136">Atlasiet nākamo kreditoru, noņemot atzīmi tā kreditora izvēles rūtiņai, kuram tikko ievadījāt atbildi, un pēc tam atzīmējot rindu nākamajam kreditoram.</span><span class="sxs-lookup"><span data-stu-id="9ed27-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="9ed27-137">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9ed27-138">Noklikšķiniet uz Ievadīt atbildi.</span><span class="sxs-lookup"><span data-stu-id="9ed27-138">Click Enter reply.</span></span>
4. <span data-ttu-id="9ed27-139">Noklikšķiniet uz Kopēt datus uz atbildēm.</span><span class="sxs-lookup"><span data-stu-id="9ed27-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="9ed27-140">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="9ed27-140">Click Edit.</span></span>
6. <span data-ttu-id="9ed27-141">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9ed27-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="9ed27-142">Izvēlēties otru piedāvājuma rindu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="9ed27-143">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="9ed27-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="9ed27-144">Skaitīt otra piedāvājuma punktus</span><span class="sxs-lookup"><span data-stu-id="9ed27-144">Score the second bid</span></span>
1. <span data-ttu-id="9ed27-145">Noklikšķiniet uz Virsraksts, lai dotos uz piedāvājuma punktu skaitīšanu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="9ed27-146">Laukā Punktu skaits ievadiet kādu numuru.</span><span class="sxs-lookup"><span data-stu-id="9ed27-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="9ed27-147">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="9ed27-148">Laukā Punktu skaits ievadiet kādu numuru.</span><span class="sxs-lookup"><span data-stu-id="9ed27-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="9ed27-149">Salīdzināt atbildes</span><span class="sxs-lookup"><span data-stu-id="9ed27-149">Compare the replies</span></span>
1. <span data-ttu-id="9ed27-150">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="9ed27-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="9ed27-151">Noklikšķiniet uz Salīdzināt atbildes.</span><span class="sxs-lookup"><span data-stu-id="9ed27-151">Click Compare replies.</span></span>
3. <span data-ttu-id="9ed27-152">Laukā Rangs ievadiet kādu numuru.</span><span class="sxs-lookup"><span data-stu-id="9ed27-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="9ed27-153">Šajā lapā tiek rādīti piedāvājumi ar virsrakstu un rindām, kā arī kopējo punktu skaitu virsraksta līmenī.</span><span class="sxs-lookup"><span data-stu-id="9ed27-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="9ed27-154">Rindas varat salīdzināt, kārtojot režģī, lai salīdzināmās rindas atrastos līdzās.</span><span class="sxs-lookup"><span data-stu-id="9ed27-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="9ed27-155">Informācijā ir iekļautas arī tālāk uzskaitītās vērtības. Daudzums: kreditora piedāvātais daudzums.</span><span class="sxs-lookup"><span data-stu-id="9ed27-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="9ed27-156">Šis daudzums var nebūt vienāds ar daudzumu, kas norādīts PP.</span><span class="sxs-lookup"><span data-stu-id="9ed27-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="9ed27-157">Neto summa: kreditora piedāvātā cena pēc visu atlaižu atņemšanas rindā norādītajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="9ed27-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="9ed27-158">Novirze: dienu skaits, par kādu piedāvājuma virsrakstā vai rindā norādītais piegādes datums atšķiras no PP virsrakstā vai PP rindā pieprasītā piegādes datuma.</span><span class="sxs-lookup"><span data-stu-id="9ed27-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="9ed27-159">Katram piedāvājumam varat ievadīt rangu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="9ed27-160">Atlasiet virsraksta rindu otram piedāvājumam, kuram vēlaties noteikt rangu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="9ed27-161">Laukā Rangs ievadiet kādu numuru.</span><span class="sxs-lookup"><span data-stu-id="9ed27-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="9ed27-162">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9ed27-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="9ed27-163">Noraidīt piedāvājumu</span><span class="sxs-lookup"><span data-stu-id="9ed27-163">Reject a bid</span></span>
1. <span data-ttu-id="9ed27-164">Atlasiet virsraksta rindu piedāvājumam, kuru vēlaties noraidīt.</span><span class="sxs-lookup"><span data-stu-id="9ed27-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="9ed27-165">Vienlaicīgi varat pieņemt, noraidīt vai atgriezt tikai vienu piedāvājumu vai viena piedāvājuma rindas.</span><span class="sxs-lookup"><span data-stu-id="9ed27-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="9ed27-166">Atzīmējiet izvēles rūtiņu Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="9ed27-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="9ed27-167">Ja piedāvājuma virsrakstā atzīmējat izvēles rūtiņu Atzīmēt, tad tiek atzīmētas arī visas rindas.</span><span class="sxs-lookup"><span data-stu-id="9ed27-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="9ed27-168">Piedāvājumā varat arī atzīmēt rindu apakškopu, lai tās noraidītu vai pieņemtu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="9ed27-169">Ir iespējams pieņemt viena kreditora piedāvājumu noteiktām PP rindām, un pēc tam pārējās PP rindas piešķirt citam kreditoram, taču tas ir jādara 2 darbībās un vienlaicīgi tikai vienā piedāvājumā.</span><span class="sxs-lookup"><span data-stu-id="9ed27-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="9ed27-170">Ja pastāv citas rindas, varat pieņemt tikai sākotnējo piedāvājuma rindu vai tās alternatīvu, bet ne abas.</span><span class="sxs-lookup"><span data-stu-id="9ed27-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="9ed27-171">Noklikšķiniet uz Noraidīt.</span><span class="sxs-lookup"><span data-stu-id="9ed27-171">Click Reject.</span></span>
4. <span data-ttu-id="9ed27-172">Noklikšķiniet uz Parametri, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="9ed27-173">Laukā Noraidīšanas pamatojums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9ed27-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="9ed27-174">Atteikuma pamatojums tiks saglabāts atbildē.</span><span class="sxs-lookup"><span data-stu-id="9ed27-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="9ed27-175">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ed27-175">Click OK.</span></span>
7. <span data-ttu-id="9ed27-176">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ed27-176">Click OK.</span></span>
8. <span data-ttu-id="9ed27-177">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-177">Close the page.</span></span>
9. <span data-ttu-id="9ed27-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-178">Close the page.</span></span>
10. <span data-ttu-id="9ed27-179">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="9ed27-180">Pieņemt piedāvājumu</span><span class="sxs-lookup"><span data-stu-id="9ed27-180">Accept a bid</span></span>
1. <span data-ttu-id="9ed27-181">Atlasiet piedāvājumu, kuru vēlaties pieņemt, un pēc tam noklikšķiniet uz saites laukā Piedāvājuma pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="9ed27-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="9ed27-182">Darbību rūtī noklikšķiniet uz Atbilde.</span><span class="sxs-lookup"><span data-stu-id="9ed27-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="9ed27-183">Noklikšķiniet uz Akceptēt.</span><span class="sxs-lookup"><span data-stu-id="9ed27-183">Click Accept.</span></span>
    * <span data-ttu-id="9ed27-184">Ja esat atzīmējis vienas rindas, bet ne citas, tad pieņemšanas darbībā tiks iekļautas tikai atzīmētās rindas.</span><span class="sxs-lookup"><span data-stu-id="9ed27-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="9ed27-185">Vai vēlaties pieņemt visas piedāvājuma rindas, tad rindas nav jāatzīmē.</span><span class="sxs-lookup"><span data-stu-id="9ed27-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="9ed27-186">Noklikšķiniet uz Parametri, lai atvērtu nolaižamo dialogu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="9ed27-187">Šādi jūs varat ierakstīt piedāvājuma pieņemšanas pamatojumu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="9ed27-188">Pamatojums tiks saglabāts piedāvājumā.</span><span class="sxs-lookup"><span data-stu-id="9ed27-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="9ed27-189">Laukā Pieņemšanas pamatojums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9ed27-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="9ed27-190">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ed27-190">Click OK.</span></span>
7. <span data-ttu-id="9ed27-191">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="9ed27-191">Click OK.</span></span>
    * <span data-ttu-id="9ed27-192">Kad noklikšķināt uz Labi, ar šo tiek izveidots pirkšanas pasūtījums, pamatojoties uz PP pieņemšanā iekļautajām rindām.</span><span class="sxs-lookup"><span data-stu-id="9ed27-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="9ed27-193">Ja pastāv citi piedāvājumi, kas nav apstrādāti (pieņemti, noraidīti vai atgriezti), tad sistēma jums piedāvā noraidīt atlikušos piedāvājumus.</span><span class="sxs-lookup"><span data-stu-id="9ed27-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="9ed27-194">Skatīt ģenerēto pirkšanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="9ed27-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="9ed27-195">Darbību rūtī noklikšķiniet uz Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="9ed27-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="9ed27-196">Noklikšķiniet uz Pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="9ed27-196">Click Purchase order.</span></span>
    * <span data-ttu-id="9ed27-197">Šeit varat redzēt pirkšanas pasūtījumu, kas tika ģenerēts, kad pieņēmāt piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="9ed27-198">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-198">Close the page.</span></span>
4. <span data-ttu-id="9ed27-199">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-199">Close the page.</span></span>
5. <span data-ttu-id="9ed27-200">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-200">Close the page.</span></span>
6. <span data-ttu-id="9ed27-201">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9ed27-201">Close the page.</span></span>


