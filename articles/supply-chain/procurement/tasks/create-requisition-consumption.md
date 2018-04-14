--- 
title: "Patēriņa pieprasījuma izveide"
description: "Šajā procedūrā ir aprakstīts pieprasījuma izveides process."
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bad86a4726ce69015f318d9af98992b36d34b29a
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="f343d-103">Patēriņa pieprasījuma izveide</span><span class="sxs-lookup"><span data-stu-id="f343d-103">Create a requisition for consumption</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f343d-104">Šajā procedūrā ir aprakstīts pieprasījuma izveides process.</span><span class="sxs-lookup"><span data-stu-id="f343d-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="f343d-105">Tajā parādīti dažādi veidi, kā meklēt preces sagādes katalogā un kā pievienot preci, kas nav katalogā.</span><span class="sxs-lookup"><span data-stu-id="f343d-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="f343d-106">Pirms sākt šo procedūru, jums ir jāiestata pirkšanas ierobežojumus uz Patēriņš kā pieprasījumu noklusējuma tipu.</span><span class="sxs-lookup"><span data-stu-id="f343d-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="f343d-107">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="f343d-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="f343d-108">Šo procedūru var veikt tikai no lietotāja profila, kas ir iestatīts kā darbinieks.</span><span class="sxs-lookup"><span data-stu-id="f343d-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="f343d-109">Šo uzdevumu parasti veic darbinieks.</span><span class="sxs-lookup"><span data-stu-id="f343d-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="f343d-110">Darbinieka pieņemšanas darbā drošības loma ļaus veikt uzdevumus, vai, ja jūs izmantojat USMF, varat pieteikties kā Alicia.</span><span class="sxs-lookup"><span data-stu-id="f343d-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="f343d-111">Jauna pieprasījuma izveide</span><span class="sxs-lookup"><span data-stu-id="f343d-111">Create a new requisition</span></span>
1. <span data-ttu-id="f343d-112">Pārejiet uz sadaļu Sagāde un avoti > Pirkuma pieprasījumi > Mani sagatavotie pirkšanas pieprasījumi.</span><span class="sxs-lookup"><span data-stu-id="f343d-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="f343d-113">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f343d-113">Click New.</span></span>
3. <span data-ttu-id="f343d-114">Laukā Nosaukums dodiet pieprasījumam nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="f343d-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="f343d-115">Laukā Pieprasītais datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="f343d-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="f343d-116">Pēc noklusējuma, pieprasījuma datums un uzskaites datums tiek kopēti uz pirkšanas pieprasījuma rindām.</span><span class="sxs-lookup"><span data-stu-id="f343d-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="f343d-117">Tos var mainīt rindas līmenī.</span><span class="sxs-lookup"><span data-stu-id="f343d-117">They can be changed at the line level.</span></span> <span data-ttu-id="f343d-118">Pieprasītais datums ir pieprasītais piegādes datums.</span><span class="sxs-lookup"><span data-stu-id="f343d-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="f343d-119">Laukā Uzskaites datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="f343d-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="f343d-120">Uzskaites datums tiek izmantots, lai grāmatotu uzskaites ierakstu virsgrāmatā un pārbaudītu pieejamos budžeta līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="f343d-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="f343d-121">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f343d-121">Click OK.</span></span>
7. <span data-ttu-id="f343d-122">Laukā Pamatojums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f343d-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f343d-123">Darījuma pamatojuma iemesls, ko atlasījāt, pēc noklusējuma tiek parādīts pirkšanas pieprasījuma rindās, bet to var mainīt rindas līmenī.</span><span class="sxs-lookup"><span data-stu-id="f343d-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="f343d-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f343d-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f343d-125">Pamatojuma atlase</span><span class="sxs-lookup"><span data-stu-id="f343d-125">Select the reason</span></span>
10. <span data-ttu-id="f343d-126">Detalizētas informācijas laukā ievadiet aprakstošu pieprasījuma pamatojumu</span><span class="sxs-lookup"><span data-stu-id="f343d-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="f343d-127">Rindas pievienošana pieprasījumam</span><span class="sxs-lookup"><span data-stu-id="f343d-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="f343d-128">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="f343d-128">Click Add line.</span></span>
    * <span data-ttu-id="f343d-129">Ir divi veidi, kā pievienot rindas pirkšanas pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="f343d-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="f343d-130">Ja jūs jau zināt preces numuru vai jau zināt, ka jūs pieprasāt preci, kas nav preču katalogā, tad varat pievienot rindu tieši ar "Pievienot rindu".</span><span class="sxs-lookup"><span data-stu-id="f343d-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="f343d-131">Cits veids ir izmantot "Pievienot preces", kur varat izmantot meklēšanu un filtrēšanu, lai atrastu vienumus preču katalogā.</span><span class="sxs-lookup"><span data-stu-id="f343d-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="f343d-132">Noklikšķiniet uz tikko izveidotās rindas.</span><span class="sxs-lookup"><span data-stu-id="f343d-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="f343d-133">Pieprasītājs ir darbinieks, kas ir pieprasījis šo pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="f343d-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="f343d-134">Pēc noklusējuma persona, kas sagatavo pieprasījumu, ir darbinieks, kurš ir to pieprasījis.</span><span class="sxs-lookup"><span data-stu-id="f343d-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="f343d-135">Jums ir jābūt atļaujai sagatavot pieprasījuma rindu cita darbinieka vārdā.</span><span class="sxs-lookup"><span data-stu-id="f343d-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="f343d-136">Ja jums ir šādas atļaujas, tad šajā uzmeklēšanā parādīsies citi darbinieki.</span><span class="sxs-lookup"><span data-stu-id="f343d-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="f343d-137">Laukā Krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f343d-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f343d-138">Krājumus, kas ir pieejami izvēlei, ierobežo kategorijas piekļuves ierobežojumi un pērkošas juridiskās personas sagādes katalogs.</span><span class="sxs-lookup"><span data-stu-id="f343d-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="f343d-139">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="f343d-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="f343d-140">Vairāku preču pievienošana pieprasījumam</span><span class="sxs-lookup"><span data-stu-id="f343d-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="f343d-141">Noklikšķiniet uz Pievienot preces.</span><span class="sxs-lookup"><span data-stu-id="f343d-141">Click Add products.</span></span>
    * <span data-ttu-id="f343d-142">Tā ir opcija, kur var meklēt preces preču katalogā.</span><span class="sxs-lookup"><span data-stu-id="f343d-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="f343d-143">Laukā Atrast sagādes kategorijas līmeni, ierakstiet meklējamo kategorijas nosaukuma pirmo daļu un pēc tam noklikšķiniet uz Enter.</span><span class="sxs-lookup"><span data-stu-id="f343d-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="f343d-144">Piemēram, ierakstiet comput.</span><span class="sxs-lookup"><span data-stu-id="f343d-144">For example, type comput.</span></span>  
3. <span data-ttu-id="f343d-145">Izmantojiet saīsni InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="f343d-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="f343d-146">Izmantojiet Filtru, lai filtrētu preču sarakstu atlasītajā kategorijā.</span><span class="sxs-lookup"><span data-stu-id="f343d-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="f343d-147">Atlasiet preces karti, ko vēlaties pievienot pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="f343d-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="f343d-148">Noklikšķiniet uz Pievienot rindām.</span><span class="sxs-lookup"><span data-stu-id="f343d-148">Click Add to lines.</span></span>
7. <span data-ttu-id="f343d-149">Laukā Daudzums ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="f343d-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="f343d-150">Laukā Atrast sagādes kategorijas līmeni, ierakstiet meklējamo kategorijas nosaukuma pirmo daļu un pēc tam noklikšķiniet uz Enter.</span><span class="sxs-lookup"><span data-stu-id="f343d-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="f343d-151">Piemēram, ierakstiet Augstas (marķieri).</span><span class="sxs-lookup"><span data-stu-id="f343d-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="f343d-152">Izmantojiet saīsni InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="f343d-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="f343d-153">Noklikšķiniet uz Pievienot rindām neuzskaitītas preces, lai pievienotu preci, kas nav norādīta sagādes katalogā.</span><span class="sxs-lookup"><span data-stu-id="f343d-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="f343d-154">Laukā Preces nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f343d-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="f343d-155">Laukā Mērvienība ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="f343d-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="f343d-156">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="f343d-156">Click OK.</span></span>
14. <span data-ttu-id="f343d-157">Laukā Krājuma apraksts pievienojiet preces aprakstu.</span><span class="sxs-lookup"><span data-stu-id="f343d-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="f343d-158">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="f343d-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="f343d-159">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="f343d-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="f343d-160">Ja jūs zināt cenu konkrētam kreditoram (kuru atlasījāt laukā Kreditora konts), tad šo cenu var ievadīt</span><span class="sxs-lookup"><span data-stu-id="f343d-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="f343d-161">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f343d-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f343d-162">Kreditori, kas ir pieejamai šajā laukā, ir atkarīgi no pirkšanas ierobežojumiem un statusa, kurš kreditoram ir pašreizējai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="f343d-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="f343d-163">Kā alternatīvu kreditora atlasei šeit, varat noklikšķināt uz pogas Ieteikt kreditoru.</span><span class="sxs-lookup"><span data-stu-id="f343d-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="f343d-164">Sarakstā atlasiet kreditoru, kuru vēlaties izmantot.</span><span class="sxs-lookup"><span data-stu-id="f343d-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="f343d-165">Laukā Ārējais krājuma kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f343d-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="f343d-166">Tas ir preces atsauces numurs, kas ir zināms kreditoram.</span><span class="sxs-lookup"><span data-stu-id="f343d-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="f343d-167">Piemēram, tas varētu būt preces krājumu kods kreditora katalogā.</span><span class="sxs-lookup"><span data-stu-id="f343d-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="f343d-168">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f343d-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="f343d-169">Sadaliet summas</span><span class="sxs-lookup"><span data-stu-id="f343d-169">Distribute amounts</span></span>
1. <span data-ttu-id="f343d-170">Noklikšķiniet uz Finanšu dati.</span><span class="sxs-lookup"><span data-stu-id="f343d-170">Click Financials.</span></span>
2. <span data-ttu-id="f343d-171">Noklikšķiniet uz Sadalīt summas.</span><span class="sxs-lookup"><span data-stu-id="f343d-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="f343d-172">Šajā procesā ir parādīts, kā sadalīt pirmās rindas izmaksas starp 2 kontiem.</span><span class="sxs-lookup"><span data-stu-id="f343d-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="f343d-173">To var izdarīt arī vēlāk, ja pieprasījums tiks pārskatīts.</span><span class="sxs-lookup"><span data-stu-id="f343d-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="f343d-174">Noklikšķiniet uz Sadalīt, lai izveidotu sadales rindu.</span><span class="sxs-lookup"><span data-stu-id="f343d-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="f343d-175">Laukā Virsgrāmatas konts atlasiet pirmo izmaksu centru, kam jāuzņemas daļa no izmaksām.</span><span class="sxs-lookup"><span data-stu-id="f343d-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="f343d-176">Atlasiet citu sadales rindu.</span><span class="sxs-lookup"><span data-stu-id="f343d-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="f343d-177">Laukā Virsgrāmatas konts norādiet otro izmaksu centru.</span><span class="sxs-lookup"><span data-stu-id="f343d-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="f343d-178">Noklikšķiniet uz Sadalīt vienādi.</span><span class="sxs-lookup"><span data-stu-id="f343d-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="f343d-179">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f343d-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="f343d-180">Skatīt rindu detalizētu informāciju</span><span class="sxs-lookup"><span data-stu-id="f343d-180">View line details</span></span>
1. <span data-ttu-id="f343d-181">Pārslēdziet sadaļas Detalizēta rindas informācija paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="f343d-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="f343d-182">Pieprasījuma iesniegšana</span><span class="sxs-lookup"><span data-stu-id="f343d-182">Submit the requisition</span></span>
1. <span data-ttu-id="f343d-183">Noklikšķiniet uz Darbplūsma, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="f343d-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="f343d-184">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="f343d-184">Click Submit.</span></span>
3. <span data-ttu-id="f343d-185">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f343d-185">Close the page.</span></span>
4. <span data-ttu-id="f343d-186">Laukā Komentārs ierakstiet piezīmi pieprasījuma apstiprinātājam.</span><span class="sxs-lookup"><span data-stu-id="f343d-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="f343d-187">Klikšķiniet Iesniegt.</span><span class="sxs-lookup"><span data-stu-id="f343d-187">Click Submit.</span></span>
6. <span data-ttu-id="f343d-188">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f343d-188">Close the page.</span></span>
7. <span data-ttu-id="f343d-189">Atsvaidziniet lapu.</span><span class="sxs-lookup"><span data-stu-id="f343d-189">Refresh the page.</span></span>


