--- 
title: "Pirkšanas līguma izveide"
description: "Šī procedūra palīdz izveidot pirkšanas līgumu."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f060346308e7ee1191d0769664648cfe72c22b21
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="89e0d-103">Pirkšanas līguma izveide</span><span class="sxs-lookup"><span data-stu-id="89e0d-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89e0d-104">Šī procedūra palīdz izveidot pirkšanas līgumu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="89e0d-105">Parasti to veic pirkšanas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="89e0d-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="89e0d-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="89e0d-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="89e0d-107">Pirms sākt, jāiestata pirkšanas līgumu klasifikācijas.</span><span class="sxs-lookup"><span data-stu-id="89e0d-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="89e0d-108">Kad esat izveidojis vienošanos, to var izmantot, veidojot PP, un šādi pirkšanas līguma nosacījumi tiks kopēti virsrakstā un jebkurās pasūtījuma rindās, kuras līgums ietekmē.</span><span class="sxs-lookup"><span data-stu-id="89e0d-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="89e0d-109">Jauna pirkšanas līguma izveide</span><span class="sxs-lookup"><span data-stu-id="89e0d-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="89e0d-110">Pārejiet uz sadaļu Sagāde un avoti > Pirkšanas līgumi > Pirkšanas līgumi.</span><span class="sxs-lookup"><span data-stu-id="89e0d-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="89e0d-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="89e0d-111">Click New.</span></span>
3. <span data-ttu-id="89e0d-112">Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="89e0d-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="89e0d-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="89e0d-115">Laukā Pirkšanas līgumu klasifikācija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="89e0d-116">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="89e0d-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="89e0d-118">Izvērsiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="89e0d-118">Expand the General section.</span></span>
10. <span data-ttu-id="89e0d-119">Laukā Beigu datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="89e0d-120">Beigu datums būs noklusējuma datums visām saistību rindām un noteiks, cik ilgi katra saistība ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="89e0d-121">Laukā Dokumenta nosaukums ievadiet pirkuma līguma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="89e0d-122">Atstājiet lauku Noklusējuma saistības iestatītu Uz preču daudzumu attiecināmas saistības (vai mainiet, ja tā nav šādi iestatīta).</span><span class="sxs-lookup"><span data-stu-id="89e0d-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="89e0d-123">Noklusējuma saistību vērtība nosaka jūsu opcijas līguma rindās.</span><span class="sxs-lookup"><span data-stu-id="89e0d-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="89e0d-124">Ja jums ir nepieciešams jauns saistību tips, veidojot līguma rindas, ir jāmaina noklusējuma saistības virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="89e0d-125">Pastāv 4 saistību tipi: Uz preču daudzumu attiecināmas saistības — attiecībā uz noteiktu preču daudzumu; Uz preču vērtību attiecināmas saistības — attiecībā uz konkrētu preces valūtas summu; Uz preces kategorijas vērtību attiecināmās saistības — attiecībā uz konkrētu valūtas summu sagādes kategorijā, kur summa var būt attiecināma uz kataloga krājumu vai krājumu, kas nav katalogā; Uz vērtību attiecināmās saistības — attiecībā uz konkrētu valūtas summu, kuru var izpildīt ar jebkuru preci vai jebkuru sagādes kategoriju.</span><span class="sxs-lookup"><span data-stu-id="89e0d-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="89e0d-126">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="89e0d-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="89e0d-127">Saistību pievienošana</span><span class="sxs-lookup"><span data-stu-id="89e0d-127">Add a commitment</span></span>
1. <span data-ttu-id="89e0d-128">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-128">Click Add line.</span></span>
2. <span data-ttu-id="89e0d-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="89e0d-130">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="89e0d-131">Atlasiet preci, kurai vēlaties pievienot saistības.</span><span class="sxs-lookup"><span data-stu-id="89e0d-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="89e0d-132">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="89e0d-133">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="89e0d-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="89e0d-134">Tas ir kopējais daudzums, kuru vienojāties iegādāties no kreditora.</span><span class="sxs-lookup"><span data-stu-id="89e0d-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="89e0d-135">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="89e0d-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="89e0d-136">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="89e0d-137">Iestatiet opciju Sasniegts maksimums uz Jā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="89e0d-138">Opcija Sasniegts maksimums ierobežo saistību izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="89e0d-139">Jūs varat iegādāties tikai līdz daudzumam, kas norādīts rindas laukā Daudzums.</span><span class="sxs-lookup"><span data-stu-id="89e0d-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="89e0d-140">Sakļaujiet sadaļu Detalizēta rindas informācija.</span><span class="sxs-lookup"><span data-stu-id="89e0d-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="89e0d-141">Virsraksta nosacījumu pievienošana</span><span class="sxs-lookup"><span data-stu-id="89e0d-141">Add header conditions</span></span>
1. <span data-ttu-id="89e0d-142">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="89e0d-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="89e0d-143">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-143">Click Change view.</span></span>
3. <span data-ttu-id="89e0d-144">Noklikšķiniet uz Virsraksta skatījuma.</span><span class="sxs-lookup"><span data-stu-id="89e0d-144">Click Header view.</span></span>
4. <span data-ttu-id="89e0d-145">Izvērsiet noteikumu sadaļu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="89e0d-146">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="89e0d-147">Maksājuma nosacījumi no kreditora konta tiek šeit rādīti pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="89e0d-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="89e0d-148">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="89e0d-149">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="89e0d-150">Laukā Piegādes veids noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="89e0d-151">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="89e0d-152">Laukā Piegādes nosacījumi noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="89e0d-153">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="89e0d-154">Līguma apstiprināšana un aktivizēšana</span><span class="sxs-lookup"><span data-stu-id="89e0d-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="89e0d-155">Darbību rūtī noklikšķiniet uz Pirkšanas līgums.</span><span class="sxs-lookup"><span data-stu-id="89e0d-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="89e0d-156">Noklikšķiniet uz Apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="89e0d-156">Click Confirmation.</span></span>
    * <span data-ttu-id="89e0d-157">Iestatiet opciju Atzīmēt līgumu kā efektīvu uz Jā.</span><span class="sxs-lookup"><span data-stu-id="89e0d-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="89e0d-158">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="89e0d-158">Click OK.</span></span>
4. <span data-ttu-id="89e0d-159">Darbību rūtī noklikšķiniet uz Pirkšanas līgums.</span><span class="sxs-lookup"><span data-stu-id="89e0d-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="89e0d-160">Noklikšķiniet uz Pirkšanas līguma apstiprinājumi.</span><span class="sxs-lookup"><span data-stu-id="89e0d-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="89e0d-161">Opcija Priekšskatījums/Drukāt ļauj ģenerēt dokumentu pirkšanas līgumam, ko pēc tam var izdrukāt vai nosūtīt kreditoram.</span><span class="sxs-lookup"><span data-stu-id="89e0d-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="89e0d-162">Ja atjaunināt līgumu vēlāk un atkārtoti to apstiprināt, abas versijas tiks parādītas šeit.</span><span class="sxs-lookup"><span data-stu-id="89e0d-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="89e0d-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="89e0d-163">Close the page.</span></span>


