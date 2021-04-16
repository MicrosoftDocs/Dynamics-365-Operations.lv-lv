---
title: Izlaistās preces izveide vienam uzņēmumam
description: Šajā procedūrā parādīts, kā izveidot vienu izlaisto preci vienas juridiskās vienības kontekstā.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe1f34f268c6427c1381a9cfced49334893acc00
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833285"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="27cb0-103">Izlaistās preces izveide vienam uzņēmumam</span><span class="sxs-lookup"><span data-stu-id="27cb0-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27cb0-104">Šajā procedūrā parādīts, kā izveidot vienu izlaisto preci vienas juridiskās vienības kontekstā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="27cb0-105">Pēc izlaistās preces izveides tā uzreiz ir pieejama tikai šajā vienībā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="27cb0-106">Šo procedūru var izmēģināt paraugdatu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="27cb0-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="27cb0-107">Šo uzdevumu parasti veic preces noformētājs.</span><span class="sxs-lookup"><span data-stu-id="27cb0-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="27cb0-108">Izlaistās preces izveide</span><span class="sxs-lookup"><span data-stu-id="27cb0-108">Create a released product</span></span>
1. <span data-ttu-id="27cb0-109">Dodieties uz Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="27cb0-109">Go to Released products.</span></span>
2. <span data-ttu-id="27cb0-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="27cb0-110">Click New.</span></span>
3. <span data-ttu-id="27cb0-111">Laukā Preces numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="27cb0-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="27cb0-112">Ja preces numurs netiek automātiski ievadīts laukā Preces numurs, ievadiet unikālo preces numuru.</span><span class="sxs-lookup"><span data-stu-id="27cb0-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="27cb0-113">Šī darbība ir nepieciešama, ja preču numuriem nav iestatīta numuru secība.</span><span class="sxs-lookup"><span data-stu-id="27cb0-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="27cb0-114">Laukā Preces nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="27cb0-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="27cb0-115">Preces nosaukums pēc noklusējuma ir meklēšanas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="27cb0-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="27cb0-116">Ja nepieciešams, varat atlasīt, ka meklēšanas nosaukums ir jāmaina.</span><span class="sxs-lookup"><span data-stu-id="27cb0-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="27cb0-117">Laukā Krājumu modeļu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-118">Krājumu modeļu grupās ir ietverti iestatījumi, kas nosaka krājumu kontroles un apstrādes tipu to saņemšanas un izsniegšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="27cb0-119">Iestatījumi nosaka arī to, kā tiek aprēķināts krājumu patēriņš.</span><span class="sxs-lookup"><span data-stu-id="27cb0-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="27cb0-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="27cb0-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="27cb0-122">Laukā Krājumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-123">Krājumu grupas tiek izmantotas, lai pārvaldītu krājumus, sadalot krājumus grupās, pamatojoties uz krājumu raksturlielumiem.</span><span class="sxs-lookup"><span data-stu-id="27cb0-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="27cb0-124">Piemēram, lai pārvaldītu to, kā informācija tiek grāmatota galvenajos kontos, varat izveidot dažādu krājumu grupu sērijas, kas ir saistītas ar konkrētiem galvenajiem kontiem.</span><span class="sxs-lookup"><span data-stu-id="27cb0-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="27cb0-125">Tas ļauj izsekot krājumu vienību vērtību dažādos posmos.</span><span class="sxs-lookup"><span data-stu-id="27cb0-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="27cb0-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="27cb0-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="27cb0-128">Laukā Noliktavas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-129">Noliktavas dimensijas palīdz kontrolēt krājumu uzglabāšanu un izņemšanu no krājumiem.</span><span class="sxs-lookup"><span data-stu-id="27cb0-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="27cb0-130">Piemēram, noliktavas dimensija var iekļaut vietu un noliktavu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="27cb0-131">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="27cb0-132">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="27cb0-133">Laukā Izsekošanas dimensiju grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-134">Izsekošanas dimensiju grupa nosaka izsekošanas dimensijas, kuras var pievienot precei.</span><span class="sxs-lookup"><span data-stu-id="27cb0-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="27cb0-135">Piemēram, partijas numuru un sērijas numuru izmanto krājuma vienību izsekošanai.</span><span class="sxs-lookup"><span data-stu-id="27cb0-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="27cb0-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="27cb0-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="27cb0-138">Laukā Krājumu uzskaites vienība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-139">Krājuma vienība nosaka, kā prece tiek skaitīta, uzglabājot krājumos.</span><span class="sxs-lookup"><span data-stu-id="27cb0-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="27cb0-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="27cb0-141">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="27cb0-142">Laukā Pirkšanas vienība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-143">Pirkšanas vienībā nosaka, kā prece tiek skaitīta, iepērkot no kreditora.</span><span class="sxs-lookup"><span data-stu-id="27cb0-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="27cb0-144">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="27cb0-145">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="27cb0-146">Laukā Pārdošanas vienība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-147">Pārdošanas vienība nosaka, kā prece tiek skaitīta, pārdodot debitoram.</span><span class="sxs-lookup"><span data-stu-id="27cb0-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="27cb0-148">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="27cb0-149">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="27cb0-150">Laukā MK vienība noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-151">MK vienība nosaka, kā prece tiek skaitīta, iekļaujot to materiālu komplekta (MK).</span><span class="sxs-lookup"><span data-stu-id="27cb0-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="27cb0-152">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="27cb0-153">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="27cb0-154">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-155">Krājumu PVN grupa Pārdošanas nodokļu grupā nosaka, kā katram krājumam tiek aprēķināts PVN.</span><span class="sxs-lookup"><span data-stu-id="27cb0-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="27cb0-156">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="27cb0-157">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="27cb0-158">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="27cb0-159">Krājumu PVN grupa Pirkšanas nodokļu grupā nosaka, kā katram krājumam tiek aprēķināts pirkšanas nodoklis.</span><span class="sxs-lookup"><span data-stu-id="27cb0-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="27cb0-160">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="27cb0-161">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="27cb0-162">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="27cb0-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="27cb0-163">Preces īpašību pievienošana</span><span class="sxs-lookup"><span data-stu-id="27cb0-163">Add product characteristics</span></span>
1. <span data-ttu-id="27cb0-164">Izvērsiet vai sakļaujiet sadaļu Krājumu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="27cb0-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="27cb0-165">Laukā Neto svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="27cb0-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="27cb0-166">Laukā Taras svars ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="27cb0-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="27cb0-167">Laukā Bruto biezums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="27cb0-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="27cb0-168">Laukā Bruto platums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="27cb0-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="27cb0-169">Laukā Bruto augstums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="27cb0-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="27cb0-170">Laukā Tilpums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="27cb0-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="27cb0-171">Finanšu dimensiju pievienošana</span><span class="sxs-lookup"><span data-stu-id="27cb0-171">Add financial dimensions</span></span>
1. <span data-ttu-id="27cb0-172">Izvērsiet vai sakļaujiet sadaļu Finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="27cb0-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="27cb0-173">Laukā BusinessUnit noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="27cb0-174">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="27cb0-175">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="27cb0-176">Laukā CostCenter noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="27cb0-177">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="27cb0-178">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="27cb0-179">Laukā Nodaļa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="27cb0-180">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="27cb0-181">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="27cb0-182">Laukā ItemGroup noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="27cb0-183">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="27cb0-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="27cb0-184">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="27cb0-184">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]