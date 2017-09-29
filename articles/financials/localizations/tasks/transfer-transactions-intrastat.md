--- 
title: "Transakciju pārsūtīšana uz Intrastat"
description: "Šajā procedūrā ir izklāstīta Intrastat parametru iestatīšana un transakciju pārsūtīšana uz Intrastat."
author: Anasyash
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: cc21497a6905cdb57bd687b7bff0d9dc810ba9eb
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="10521-103">Transakciju pārsūtīšana uz Intrastat</span><span class="sxs-lookup"><span data-stu-id="10521-103">Transfer transactions to the Intrastat</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10521-104">Šajā procedūrā ir izklāstīta Intrastat parametru iestatīšana un transakciju pārsūtīšana uz Intrastat.</span><span class="sxs-lookup"><span data-stu-id="10521-104">This procedure walks you through how to set up Intrastat parameters and transfer transactions to Intrastat.</span></span> <span data-ttu-id="10521-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma DEMF dati.</span><span class="sxs-lookup"><span data-stu-id="10521-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="create-new-and-update-existing-commodity-code"></a><span data-ttu-id="10521-106">Izveidojiet jaunu un atjauniniet esošu preces kodu</span><span class="sxs-lookup"><span data-stu-id="10521-106">Create new and update existing commodity code</span></span>
1. <span data-ttu-id="10521-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Iestatījumi > Kategorijas un atribūti > Kategoriju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="10521-107">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="10521-108">Sarakstā atrodiet vai atlasiet ierakstu Intrastat preču kodi.</span><span class="sxs-lookup"><span data-stu-id="10521-108">In the list, find or select the record "Intrastat commodity codes."</span></span>
3. <span data-ttu-id="10521-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="10521-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="10521-110">Koka struktūrā atlasiet “ieraksts”.</span><span class="sxs-lookup"><span data-stu-id="10521-110">In the tree, select 'a record'.</span></span>
    * <span data-ttu-id="10521-111">Piemēram, atlasiet 'Intrastat\Skaļrunis'.</span><span class="sxs-lookup"><span data-stu-id="10521-111">For example, select 'Intrastat\Speaker'.</span></span>  
5. <span data-ttu-id="10521-112">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="10521-112">Click Edit.</span></span>
6. <span data-ttu-id="10521-113">Izvērsiet sadaļu Ārējā tirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="10521-113">Expand the Foreign trade section.</span></span>
7. <span data-ttu-id="10521-114">Laukā Papildu vienības ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-114">In the Additional units field, enter or select a value.</span></span>
    * <span data-ttu-id="10521-115">Piemēram, atlasiet 'gab.'.</span><span class="sxs-lookup"><span data-stu-id="10521-115">For example, choose 'pcs'.</span></span>  
8. <span data-ttu-id="10521-116">Atlasiet Jā laukā Svars netiek lietots.</span><span class="sxs-lookup"><span data-stu-id="10521-116">Select Yes in the Weight not applicable field.</span></span>
9. <span data-ttu-id="10521-117">Koka struktūrā atlasiet “Intrastat”.</span><span class="sxs-lookup"><span data-stu-id="10521-117">In the tree, select 'Intrastat'.</span></span>
10. <span data-ttu-id="10521-118">Noklikšķiniet uz Jauns kategorijas zars.</span><span class="sxs-lookup"><span data-stu-id="10521-118">Click New category node.</span></span>
11. <span data-ttu-id="10521-119">Laukā Nosaukums ievadiet preces nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="10521-119">In the Name field, enter the name of commodity.</span></span>
    * <span data-ttu-id="10521-120">Piemēram, ierakstiet "Citas preces".</span><span class="sxs-lookup"><span data-stu-id="10521-120">For example, type 'Other commodity'.</span></span>  
12. <span data-ttu-id="10521-121">Laukā Kods ievadiet preces kodu.</span><span class="sxs-lookup"><span data-stu-id="10521-121">In the Code field, enter the commodity code.</span></span>
    * <span data-ttu-id="10521-122">Piemēram, ierakstiet '995 00 00'.</span><span class="sxs-lookup"><span data-stu-id="10521-122">For example, type '995 00 00'.</span></span>  
13. <span data-ttu-id="10521-123">Laukā Draudzīgais nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-123">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="10521-124">Piemēram, ierakstiet 'Cits'.</span><span class="sxs-lookup"><span data-stu-id="10521-124">For example, type 'Other'.</span></span>  
14. <span data-ttu-id="10521-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="10521-125">Click Save.</span></span>
15. <span data-ttu-id="10521-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="10521-126">Close the page.</span></span>

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a><span data-ttu-id="10521-127">Piešķiriet preces kodu preces hierarhijai un izlaistai precei</span><span class="sxs-lookup"><span data-stu-id="10521-127">Assign commodity code to product hierarchy and released product</span></span>
1. <span data-ttu-id="10521-128">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="10521-128">Use the Quick Filter to find records.</span></span> <span data-ttu-id="10521-129">Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību “pārdošana”.</span><span class="sxs-lookup"><span data-stu-id="10521-129">For example, filter on the Name field with a value of 'sales'.</span></span>
2. <span data-ttu-id="10521-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="10521-130">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="10521-131">Koka struktūrā izvērsiet elementu “kategorijas līmenis”.</span><span class="sxs-lookup"><span data-stu-id="10521-131">In the tree, expand 'a category node'.</span></span>
    * <span data-ttu-id="10521-132">Piemēram, izvērsiet 'Pārdošanas hierarhija\Sadzīves audiosistēma'.</span><span class="sxs-lookup"><span data-stu-id="10521-132">For example, expand 'Sales hierarchy\Home audio'.</span></span>  
4. <span data-ttu-id="10521-133">Koka struktūrā atlasiet “kategorija, kas tiks piešķirta preces kodam”.</span><span class="sxs-lookup"><span data-stu-id="10521-133">In the tree, select 'the category to assign to the commodity code'.</span></span>
    * <span data-ttu-id="10521-134">Piemēram, atlasiet 'Pārdošanas hierarhija\Sadzīves audiosistēma/Skaļruņi'.</span><span class="sxs-lookup"><span data-stu-id="10521-134">For example, select 'Sales hierarchy\Home audio\Speakers.</span></span>  
5. <span data-ttu-id="10521-135">Izvērsiet sadaļu Preču kodi.</span><span class="sxs-lookup"><span data-stu-id="10521-135">Expand the Commodity codes section.</span></span>
6. <span data-ttu-id="10521-136">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="10521-136">Click Add.</span></span>
7. <span data-ttu-id="10521-137">Laukā Atlasīt hierarhiju atlasiet “Instrastat”.</span><span class="sxs-lookup"><span data-stu-id="10521-137">In the Select hierarchy field, select 'Intrastat'.</span></span>
8. <span data-ttu-id="10521-138">Sarakstā atrodiet un atlasiet preces kodu</span><span class="sxs-lookup"><span data-stu-id="10521-138">In the list, find and select the commodity code</span></span>
    * <span data-ttu-id="10521-139">Piemēram, atlasiet '920 20 34 Skaļrunis'.</span><span class="sxs-lookup"><span data-stu-id="10521-139">For example, select '920 20 34 Speaker'.</span></span>  
9. <span data-ttu-id="10521-140">Noklikšķiniet uz SelectCodes.</span><span class="sxs-lookup"><span data-stu-id="10521-140">Click SelectCodes.</span></span>
10. <span data-ttu-id="10521-141">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10521-141">Click OK.</span></span>
11. <span data-ttu-id="10521-142">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="10521-142">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="10521-143">Sarakstā izvēlieties izlaisto preci, kas tiks piešķirta preces kodam.</span><span class="sxs-lookup"><span data-stu-id="10521-143">In the list, choose the released product that you will assign to the commodity code.</span></span>
    * <span data-ttu-id="10521-144">Piemēram, atlasiet 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="10521-144">For example, choose 'D0001'.</span></span>  
13. <span data-ttu-id="10521-145">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="10521-145">Click Edit.</span></span>
14. <span data-ttu-id="10521-146">Izvērsiet sadaļu Ārējā tirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="10521-146">Expand the Foreign trade section.</span></span>
15. <span data-ttu-id="10521-147">Laukā Prece ievadiet preces kodu</span><span class="sxs-lookup"><span data-stu-id="10521-147">In the Commodity field, enter the commodity code</span></span>
    * <span data-ttu-id="10521-148">Piemēram, atlasiet vērtību '920 20 34 Skaļrunis'.</span><span class="sxs-lookup"><span data-stu-id="10521-148">For example, select value '920 20 34 Speaker'.</span></span>    
16. <span data-ttu-id="10521-149">Laukā Papildmaksas procentos ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="10521-149">In the Charges percentage field, enter a number.</span></span>
    * <span data-ttu-id="10521-150">Piemēram, ievadiet '3'.</span><span class="sxs-lookup"><span data-stu-id="10521-150">For example, enter '3'.</span></span>  
17. <span data-ttu-id="10521-151">Laukā Valsts/reģions ievadiet vai atlasiet izcelsmes valsti vai reģionu</span><span class="sxs-lookup"><span data-stu-id="10521-151">In the Country/region field, enter or select a country or region of origin</span></span>
    * <span data-ttu-id="10521-152">Piemēram, atlasiet 'AUT'.</span><span class="sxs-lookup"><span data-stu-id="10521-152">For example, select 'AUT'.</span></span>  
18. <span data-ttu-id="10521-153">Izvērsiet sadaļu Pārvaldīt krājumus.</span><span class="sxs-lookup"><span data-stu-id="10521-153">Expand the Manage inventory section.</span></span>
19. <span data-ttu-id="10521-154">Laukā Neto svars ievadiet svaru kilogramos.</span><span class="sxs-lookup"><span data-stu-id="10521-154">In the Net weight field, enter a weight in kg.</span></span>
    * <span data-ttu-id="10521-155">Piemēram, ievadiet '2.5'.</span><span class="sxs-lookup"><span data-stu-id="10521-155">For example, enter '2.5'.</span></span>  
20. <span data-ttu-id="10521-156">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="10521-156">Click Save.</span></span>

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a><span data-ttu-id="10521-157">Iestatiet Intrastat transakciju kodus un ārējās tirdzniecības parametrus</span><span class="sxs-lookup"><span data-stu-id="10521-157">Set up Intrastat transaction codes and foreign trade parameters</span></span>
1. <span data-ttu-id="10521-158">Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Transakciju kodi</span><span class="sxs-lookup"><span data-stu-id="10521-158">Go to Tax > Setup > Foreign trade > Transaction codes</span></span>
2. <span data-ttu-id="10521-159">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="10521-159">Click New.</span></span>
3. <span data-ttu-id="10521-160">Laukā Transakcijas kods ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-160">In the Transaction code field, type a value.</span></span>
    * <span data-ttu-id="10521-161">Piemēram, ievadiet '21' transakcijas kodam, kas tiek izmantots kā atgriešana.</span><span class="sxs-lookup"><span data-stu-id="10521-161">For example, enter '21' for the transaction code used as return.</span></span>  
4. <span data-ttu-id="10521-162">Laukā Nosaukums ierakstiet transakcijas koda nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="10521-162">In the Name field, type the name of transaction code.</span></span>
    * <span data-ttu-id="10521-163">Piemēram, ievadiet 'Atgriešana'.</span><span class="sxs-lookup"><span data-stu-id="10521-163">For example, enter 'Return'.</span></span>  
5. <span data-ttu-id="10521-164">Laukā Statistiskā summa atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="10521-164">In the Statistical amount field, select an option.</span></span>
    * <span data-ttu-id="10521-165">Piemēram, atlasiet "Tukšs', kas norāda Statistisko vērtību, kas jāpārskata transakcijām ar Transakcijas kodu "21", vienmēr ir nulle.</span><span class="sxs-lookup"><span data-stu-id="10521-165">For example, select 'Empty' which indicates that the Statistical value to be reported for transactions with Transaction code of "21" will always be zero.</span></span>  
6. <span data-ttu-id="10521-166">Dodieties uz Nodokļi > Iestatīšana > Ārējā tirdzniecība > Ārējās tirdzniecības parametri</span><span class="sxs-lookup"><span data-stu-id="10521-166">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
7. <span data-ttu-id="10521-167">Laukā Transakcijas kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-167">In the Transaction code field, enter or select a value.</span></span>
    * <span data-ttu-id="10521-168">Piemēram, atlasiet '11'.</span><span class="sxs-lookup"><span data-stu-id="10521-168">For example, select '11'.</span></span>  
8. <span data-ttu-id="10521-169">Laukā Kredīta nota ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-169">In the Credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="10521-170">Šī vērtība norāda fizisko atgriešanu.</span><span class="sxs-lookup"><span data-stu-id="10521-170">This value also identifies the physical return.</span></span> <span data-ttu-id="10521-171">Kredīta piezīmes fiziskajai atgriešanai tiks pārsūtītas Intrastat žurnālā ar pretēju virzienu.</span><span class="sxs-lookup"><span data-stu-id="10521-171">The credit note for the physical return will be transferred in the Intrastat journal with opposite direction.</span></span> <span data-ttu-id="10521-172">Piemēram, saņemšanas atgriešana tiek pārsūtīta kā nosūtīšana.</span><span class="sxs-lookup"><span data-stu-id="10521-172">For example, the return of arrival is transferred as dispatch.</span></span>   <span data-ttu-id="10521-173">Pretējā gadījumā kredīta piezīme tiek uzskatīta par labojumu, un tiek pārsūtīta ar tādu pašu virzienu un pretēju zīmi.</span><span class="sxs-lookup"><span data-stu-id="10521-173">Otherwise, the credit note is considered a correction and is transferred with the same direction and opposite sign.</span></span> <span data-ttu-id="10521-174">Piemēram, saņemšanas labošana tiek pārsūtīta kā saņemšana ar negatīvu summu, un aktīvais karodziņš tiek iestatīts uz "Labojums".</span><span class="sxs-lookup"><span data-stu-id="10521-174">For example, the correction of arrival is transferred as an arrival with negative amount and the active flag is set to "Correction".</span></span>  
9. <span data-ttu-id="10521-175">Izvērsiet sadaļu Pārsūtīšana.</span><span class="sxs-lookup"><span data-stu-id="10521-175">Expand the Transfer section.</span></span>
10. <span data-ttu-id="10521-176">Atlasiet Jā laukā Krājumi ar preču kodu.</span><span class="sxs-lookup"><span data-stu-id="10521-176">Select Yes in the Items with commodity code field.</span></span>
    * <span data-ttu-id="10521-177">Atlasiet šo opciju, lai pārsūtītu tikai transakcijas ar piešķirtu preces kodu.</span><span class="sxs-lookup"><span data-stu-id="10521-177">Select this option to transfer only the transactions with a commodity code assigned.</span></span> <span data-ttu-id="10521-178">Transakcijas bez preces koda netiks pārsūtītas uz Intrastat.</span><span class="sxs-lookup"><span data-stu-id="10521-178">Transactions without a commodity code won't be transferred to Intrastat.</span></span>  
11. <span data-ttu-id="10521-179">Laukā Pārsūtīt, ja atbilst kritērijam atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="10521-179">In the Transfer when meeting criterion for field, select an option.</span></span>
    * <span data-ttu-id="10521-180">Piemēram, atlasiet vienumu “Viens no atlasītajiem”.</span><span class="sxs-lookup"><span data-stu-id="10521-180">For example, select 'One of the selected'.</span></span>  
12. <span data-ttu-id="10521-181">Izvērsiet sadaļu Preču kodu hierarhija.</span><span class="sxs-lookup"><span data-stu-id="10521-181">Expand the Commodity code hierarchy section.</span></span>
13. <span data-ttu-id="10521-182">Noklikšķiniet uz cilnes Valsts/reģiona rekvizīti.</span><span class="sxs-lookup"><span data-stu-id="10521-182">Click the Country/region properties tab.</span></span>
14. <span data-ttu-id="10521-183">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="10521-183">Click New.</span></span>
15. <span data-ttu-id="10521-184">Laukā Valsts/reģions ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-184">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="10521-185">Piemēram, atlasiet vērtību “FRA”.</span><span class="sxs-lookup"><span data-stu-id="10521-185">For example, select the value 'FRA'.</span></span>  
16. <span data-ttu-id="10521-186">Laukā Intrastat kods ievadiet valsts ISO kodu.</span><span class="sxs-lookup"><span data-stu-id="10521-186">In the Intrastat code field, enter the ISO code for the country.</span></span>
    * <span data-ttu-id="10521-187">Piemēram, ierakstiet “FR”.</span><span class="sxs-lookup"><span data-stu-id="10521-187">For example, type 'FR'.</span></span>  
17. <span data-ttu-id="10521-188">Laukā Valsts/reģiona tips atlasiet "ES".</span><span class="sxs-lookup"><span data-stu-id="10521-188">In the Country/region type field, select 'EU'.</span></span>
18. <span data-ttu-id="10521-189">Noklikšķiniet uz cilnes Numuru sērijas.</span><span class="sxs-lookup"><span data-stu-id="10521-189">Click the Number sequences tab.</span></span>

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a><span data-ttu-id="10521-190">Iestatiet piegādes veidus un nosacījumus izmaksu iekļaušanai Intrastat</span><span class="sxs-lookup"><span data-stu-id="10521-190">Set up Modes of delivery and rules for including charges in Intrastat</span></span>
1. <span data-ttu-id="10521-191">Dodieties uz Pārdošana un mārketings > Iestatīšana > Sadale > Piegādes veidi</span><span class="sxs-lookup"><span data-stu-id="10521-191">Go to Sales and marketing > Setup > Distribution > Modes of delivery</span></span>
2. <span data-ttu-id="10521-192">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="10521-192">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="10521-193">Piemēram, atlasiet “20 Air”.</span><span class="sxs-lookup"><span data-stu-id="10521-193">For example, select '20 Air'.</span></span>  
3. <span data-ttu-id="10521-194">Izvērsiet sadaļu Ārējā tirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="10521-194">Expand the Foreign trade section.</span></span>
4. <span data-ttu-id="10521-195">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="10521-195">Click Edit.</span></span>
5. <span data-ttu-id="10521-196">Laukā Transportēšana ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-196">In the Transport field, enter or select a value.</span></span>
    * <span data-ttu-id="10521-197">Piemēram, atlasiet “02”.</span><span class="sxs-lookup"><span data-stu-id="10521-197">For example, select '02'.</span></span>  
6. <span data-ttu-id="10521-198">Dodieties uz Debitoru parādi > Maksu iestatīšana > Maksas kods.</span><span class="sxs-lookup"><span data-stu-id="10521-198">Go to Accounts receivable > Charges setup > Charges code.</span></span>
7. <span data-ttu-id="10521-199">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="10521-199">Use the Quick Filter to find records.</span></span> <span data-ttu-id="10521-200">Piemēram, filtrējiet pēc lauka Maksas kods, izmantojot vērtību "kravu pārvadāšana".</span><span class="sxs-lookup"><span data-stu-id="10521-200">For example, filter on the Charges code field with a value of 'freight'.</span></span>
8. <span data-ttu-id="10521-201">Izvērsiet sadaļu Ārējā tirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="10521-201">Expand the Foreign trade section.</span></span>
9. <span data-ttu-id="10521-202">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="10521-202">Click Edit.</span></span>
10. <span data-ttu-id="10521-203">Atlasiet Jā laukā Intrastat rēķina vērtība.</span><span class="sxs-lookup"><span data-stu-id="10521-203">Select Yes in the Intrastat invoice value field.</span></span>
    * <span data-ttu-id="10521-204">Summa tiks pārsūtīta uz lauku Rēķina izmaksas un tiks saskaitīta ar pārsūtīto summu laukā Rēķina summa.</span><span class="sxs-lookup"><span data-stu-id="10521-204">The amount will be transferred to the  Invoice charges field and will be summarized with the amount transferred in the Invoice amount field.</span></span>    <span data-ttu-id="10521-205">Atlasiet Jā laukā Intrastat statistiskā vērtība, ja izmaiņu summa ir jāpārsūta uz lauku Statistiskās izmaksas un jāsaskaita ar vērtību Statistiskā summa.</span><span class="sxs-lookup"><span data-stu-id="10521-205">Select Yes in the Intrastat statistical value field if the amount of changes need to be transferred to the field Statistical charges and summarized with Statistical amount.</span></span>  

## <a name="sell-products-for-eu-customers"></a><span data-ttu-id="10521-206">Preču pārdošana ES debitoriem</span><span class="sxs-lookup"><span data-stu-id="10521-206">Sell products for EU customers</span></span>
1. <span data-ttu-id="10521-207">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="10521-207">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="10521-208">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="10521-208">Click New.</span></span>
3. <span data-ttu-id="10521-209">Laukā Debitora konts atlasiet ES debitoru</span><span class="sxs-lookup"><span data-stu-id="10521-209">In the Customer account field, select an EU customer</span></span>
    * <span data-ttu-id="10521-210">Piemēram, atlasiet “DE-012 Litware Retail”.</span><span class="sxs-lookup"><span data-stu-id="10521-210">For example, select "DE-012 Litware Retail".</span></span>  
4. <span data-ttu-id="10521-211">Izvērsiet sadaļu Piegāde.</span><span class="sxs-lookup"><span data-stu-id="10521-211">Expand the Delivery section.</span></span>
5. <span data-ttu-id="10521-212">Laukā Piegādes veids ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-212">In the Mode of delivery field, enter or select a value.</span></span>
    * <span data-ttu-id="10521-213">Piemēram, atlasiet “20 Air”.</span><span class="sxs-lookup"><span data-stu-id="10521-213">For example, select '20 Air'.</span></span>  
6. <span data-ttu-id="10521-214">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10521-214">Click OK.</span></span>
7. <span data-ttu-id="10521-215">Novietojiet kursoru uz pirmās pārdošanas pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="10521-215">Place the cursor on the first row of sales order lines.</span></span>
8. <span data-ttu-id="10521-216">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-216">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="10521-217">Piemēram, atlasiet “D001”.</span><span class="sxs-lookup"><span data-stu-id="10521-217">For example, select 'D001'.</span></span>  
9. <span data-ttu-id="10521-218">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="10521-218">Expand the Line details section.</span></span>
10. <span data-ttu-id="10521-219">Noklikšķiniet uz cilnes Ārējā tirdzniecība.</span><span class="sxs-lookup"><span data-stu-id="10521-219">Click the Foreign trade tab.</span></span>
    * <span data-ttu-id="10521-220">Transportēšana tiek aizpildīta automātiski no izvēlētā piegādes veida.</span><span class="sxs-lookup"><span data-stu-id="10521-220">The transport is filled automatically from the chosen Mode of delivery.</span></span>  
11. <span data-ttu-id="10521-221">Laukā Osta ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-221">In the Port field, enter or select a value.</span></span>
12. <span data-ttu-id="10521-222">Noklikšķiniet uz Finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="10521-222">Click Financials.</span></span>
    * <span data-ttu-id="10521-223">Atbilstoši iestatījumiem šī summa tiks iekļauta Intrastat rēķina vērtībā.</span><span class="sxs-lookup"><span data-stu-id="10521-223">As per the settings, this amount will be included in Intrastat invoice value.</span></span>  
13. <span data-ttu-id="10521-224">Noklikšķiniet uz Uzturēt maksas.</span><span class="sxs-lookup"><span data-stu-id="10521-224">Click Maintain charges.</span></span>
14. <span data-ttu-id="10521-225">Laukā Maksas kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-225">In the Charges code field, enter or select a value.</span></span>
    * <span data-ttu-id="10521-226">Piemēram, atlasiet “KRAVAS PĀRVADĀŠANA”.</span><span class="sxs-lookup"><span data-stu-id="10521-226">For example, select 'FREIGHT'.</span></span>  
15. <span data-ttu-id="10521-227">Atzīmējiet izvēles rūtiņu Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="10521-227">Select the Keep check box.</span></span>
16. <span data-ttu-id="10521-228">Laukā Maksu vērtība ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="10521-228">In the Charges value field, enter a number.</span></span>
    * <span data-ttu-id="10521-229">Piemēram, ievadiet “10”.</span><span class="sxs-lookup"><span data-stu-id="10521-229">For example, enter '10'.</span></span>  
17. <span data-ttu-id="10521-230">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="10521-230">Click Save.</span></span>
18. <span data-ttu-id="10521-231">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="10521-231">Close the page.</span></span>
19. <span data-ttu-id="10521-232">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="10521-232">On the Action Pane, click Invoice.</span></span>
20. <span data-ttu-id="10521-233">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="10521-233">Click Invoice.</span></span>
21. <span data-ttu-id="10521-234">Izvērsiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="10521-234">Expand the Parameters section.</span></span>
22. <span data-ttu-id="10521-235">Laukā Daudzums atlasiet vērtību Visi.</span><span class="sxs-lookup"><span data-stu-id="10521-235">In the Quantity field, select 'All'.</span></span>
23. <span data-ttu-id="10521-236">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="10521-236">Expand the Setup section.</span></span>
24. <span data-ttu-id="10521-237">Laukā Rēķina datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="10521-237">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="10521-238">Piemēram, ievadiet “31.01.2015.”</span><span class="sxs-lookup"><span data-stu-id="10521-238">For example, enter '2015-01-31'.</span></span>  
25. <span data-ttu-id="10521-239">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10521-239">Click OK.</span></span>
26. <span data-ttu-id="10521-240">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10521-240">Click OK.</span></span>
27. <span data-ttu-id="10521-241">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="10521-241">Close the page.</span></span>
28. <span data-ttu-id="10521-242">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="10521-242">Click New.</span></span>
29. <span data-ttu-id="10521-243">Laukā Debitora konts atlasiet ES debitoru.</span><span class="sxs-lookup"><span data-stu-id="10521-243">In the Customer account field, select an EU customer.</span></span>
    * <span data-ttu-id="10521-244">Piemēram, atlasiet “DE-013 Trey Wholesales”</span><span class="sxs-lookup"><span data-stu-id="10521-244">For example, select 'DE-013 Trey Wholesales'</span></span>  
30. <span data-ttu-id="10521-245">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10521-245">Click OK.</span></span>
31. <span data-ttu-id="10521-246">Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-246">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="10521-247">Piemēram, atlasiet “D0001”.</span><span class="sxs-lookup"><span data-stu-id="10521-247">For example, select 'D0001'.</span></span>  
32. <span data-ttu-id="10521-248">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="10521-248">Click Save.</span></span>
33. <span data-ttu-id="10521-249">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="10521-249">Click Invoice.</span></span>
34. <span data-ttu-id="10521-250">Laukā Rēķina datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="10521-250">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="10521-251">Piemēram, ievadiet datumu “31.01.2015.”</span><span class="sxs-lookup"><span data-stu-id="10521-251">For example, enter the date '2015-01-31'.</span></span>  
35. <span data-ttu-id="10521-252">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10521-252">Click OK.</span></span>
36. <span data-ttu-id="10521-253">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10521-253">Click OK.</span></span>

## <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="10521-254">Transakciju pārsūtīšana uz Intrastat</span><span class="sxs-lookup"><span data-stu-id="10521-254">Transfer transactions to the Intrastat</span></span>
1. <span data-ttu-id="10521-255">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="10521-255">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
2. <span data-ttu-id="10521-256">Noklikšķiniet uz Pārvest.</span><span class="sxs-lookup"><span data-stu-id="10521-256">Click Transfer.</span></span>
3. <span data-ttu-id="10521-257">Atlasiet Jā laukā Debitora rēķins.</span><span class="sxs-lookup"><span data-stu-id="10521-257">Select Yes in the Customer invoice field.</span></span>
4. <span data-ttu-id="10521-258">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="10521-258">Click Filter.</span></span>
5. <span data-ttu-id="10521-259">Sarakstā atzīmējiet rindu ar datumu</span><span class="sxs-lookup"><span data-stu-id="10521-259">In the list, mark the row with Date</span></span>
6. <span data-ttu-id="10521-260">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="10521-260">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="10521-261">Piemēram, ievadiet perioda filtru 2015. gada janvārim (precīza vērtība ir atkarīga no datuma formāta): 1.1.2015.–31.1.2015.</span><span class="sxs-lookup"><span data-stu-id="10521-261">For example, enter the filter for the period January 2015 (the exact value depends on your date format): 1/1/2015..1/31/2015</span></span>  
7. <span data-ttu-id="10521-262">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10521-262">Click OK.</span></span>
8. <span data-ttu-id="10521-263">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="10521-263">Click OK.</span></span>
9. <span data-ttu-id="10521-264">Sarakstā atrodiet un atlasiet pārsūtīto ierakstu.</span><span class="sxs-lookup"><span data-stu-id="10521-264">In the list, find and selected the transferred record.</span></span>
10. <span data-ttu-id="10521-265">Noklikšķiniet uz cilnes Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="10521-265">Click the General tab.</span></span>
    * <span data-ttu-id="10521-266">Pārskatiet pārsūtītos datus, tostarp saņēmēja/nosūtītāja valsti\reģionu, izcelsmes valsti, svaru, daudzumu, daudzumu papildmērvienībās, preci, transakcijas kodu, rēķinu summas un statistiskās summas.</span><span class="sxs-lookup"><span data-stu-id="10521-266">Review transferred data, including country\region of destination/dispatch, country of origin, weight, quantity, quantity in additional units, commodity, transaction code, invoice amounts and statistical amounts.</span></span>   <span data-ttu-id="10521-267">Ja nepieciešams, datus var modificēt.</span><span class="sxs-lookup"><span data-stu-id="10521-267">You can modify data if necessary.</span></span>  


