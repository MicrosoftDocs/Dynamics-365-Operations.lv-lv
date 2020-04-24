---
title: Vienības izmaksu cena un atgrieztā laidiena ID
description: Iespējams, vēlēsities, lai atgriezto preču izmaksas būtu vienādas ar preču izmaksām brīdī, kad pārdevāt preces debitoram. To var izdarīt, izmantojot **Atgrieztā laidiena ID**.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3d038b90595511b25863865045c5ce8ad45b1e0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216348"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="91a56-104">Vienības izmaksu cena un atgrieztā laidiena ID</span><span class="sxs-lookup"><span data-stu-id="91a56-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="91a56-105">Krājumos atgriezto preču izmaksas aprēķina, izmantojot pašreizējās preču izmaksas.</span><span class="sxs-lookup"><span data-stu-id="91a56-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="91a56-106">Tomēr, iespējams, vēlēsities, lai atgriezto preču izmaksas būtu vienādas ar preču izmaksām brīdī, kad pārdevāt preces debitoram.</span><span class="sxs-lookup"><span data-stu-id="91a56-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="91a56-107">To var izdarīt, izmantojot lauku **Atgrieztā laidiena ID** veidlapas **Pārdošanas pasūtījums** kopsavilkuma cilnē **Detalizēta informācija par rindu**.</span><span class="sxs-lookup"><span data-stu-id="91a56-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="91a56-108">Piemēram, aplūkosim šādu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="91a56-108">For example, consider the following scenario.</span></span> <span data-ttu-id="91a56-109">Jūs izrakstāt debitoram rēķinu.</span><span class="sxs-lookup"><span data-stu-id="91a56-109">You invoice a customer.</span></span> <span data-ttu-id="91a56-110">Pēc tam debitors atgriež jums piegādātās preces.</span><span class="sxs-lookup"><span data-stu-id="91a56-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="91a56-111">Jūs atgriežat preces krājumos.</span><span class="sxs-lookup"><span data-stu-id="91a56-111">You return the products to stock.</span></span> <span data-ttu-id="91a56-112">Šādā gadījumā, kreditējot debitoru par atgrieztajām precēm, šo preču izmaksas aprēķina, izmantojot pašreizējās preču izmaksas.</span><span class="sxs-lookup"><span data-stu-id="91a56-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="91a56-113">Tomēr, ja izmantojat lauku **Atgrieztā laidiena ID**, atgriezto preču izmaksas tiek aprēķinātas, izmantojot izmaksas, kas norādītas sākotnējās pārdošanas debitora rēķinā.</span><span class="sxs-lookup"><span data-stu-id="91a56-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="91a56-114">Lai atgriešanai no debitora izmantotu citas izmaksas, nevis pašreizējās izmaksas, lietojiet kādu no šīm metodēm.</span><span class="sxs-lookup"><span data-stu-id="91a56-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="91a56-115">1. metode. Manuāla vienības izmaksu cenas ievadīšana</span><span class="sxs-lookup"><span data-stu-id="91a56-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="91a56-116">Pēc noklusējuma, pievienojot krājumus atgriešanas pasūtījumam, tie tiek atgriezti krājumos pašreizējā izmaksu cenā.</span><span class="sxs-lookup"><span data-stu-id="91a56-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="91a56-117">Lai norādītu citu vienības izmaksu cenu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="91a56-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="91a56-118">Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="91a56-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="91a56-119">**Darbību rūts** grupā **Jauns** noklikšķiniet uz **Atgriešanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="91a56-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="91a56-120">Veidlapā **Izveidot atgriešanas pasūtījumu** atlasiet debitora kontu un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="91a56-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="91a56-121">Formā **Atgriešanas pasūtījums — AKA kods: %1, %2** atlasiet krājumu un pēc tam ievadiet negatīvu daudzumu laukā **Daudzums**.</span><span class="sxs-lookup"><span data-stu-id="91a56-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="91a56-122">Noklikšķiniet uz kopsavilkuma cilnes **Detalizēta informācija par rindu**.</span><span class="sxs-lookup"><span data-stu-id="91a56-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="91a56-123">Cilnē **Vispārīgi** ievadiet vērtību laukā **Vienības izmaksu cena**.</span><span class="sxs-lookup"><span data-stu-id="91a56-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="91a56-124">Šī vērtība tiek izmantota, kad preces tiek atgrieztas krājumos.</span><span class="sxs-lookup"><span data-stu-id="91a56-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="91a56-125">Ja neievadāt vērtību, atgriežot preces krājumos, tiek izmantota pašreizējā izmaksu cena.</span><span class="sxs-lookup"><span data-stu-id="91a56-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="91a56-126">2. metode. Izmaksu cenas automātiska ģenerēšana, pamatojoties uz debitora rēķina rindu</span><span class="sxs-lookup"><span data-stu-id="91a56-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="91a56-127">Atgriešanas rindu izveidei vēlams izmantot šo metodi.</span><span class="sxs-lookup"><span data-stu-id="91a56-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="91a56-128">Lai izmantotu preču izmaksas brīdī, kad pārdevāt preces debitoram, izveidojiet atgriešanas pasūtījumu un norādiet atgriežamo pārdošanas rindu.</span><span class="sxs-lookup"><span data-stu-id="91a56-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="91a56-129">Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="91a56-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="91a56-130">**Darbību rūts** grupā **Jauns** noklikšķiniet uz **Atgriešanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="91a56-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="91a56-131">Veidlapā **Izveidot atgriešanas pasūtījumu** atlasiet debitora kontu un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="91a56-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="91a56-132">Formas **Atgriešanas pasūtījums — AKA kods: %1, %2**, sadaļā **Darbību rūts** noklikšķiniet uz vienuma **Atrast pārdošanas pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="91a56-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="91a56-133">Veidlapā **Atrast pārdošanas pasūtījumu** atlasiet atgriežamo rēķina rindu un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="91a56-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="91a56-134">Kopsavilkuma cilnes **Detalizēta informācija par rindu** cilnes **Vispārīgi** laukā **Atgrieztā laidiena ID** ir parādīta vērtība no sākotnējās pārdošanas rindas.</span><span class="sxs-lookup"><span data-stu-id="91a56-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="91a56-135">Turklāt laukā **Vienības izmaksu cena** tiek parādīta izmaksu vērtība no sākotnējās pārdošanas rindas.</span><span class="sxs-lookup"><span data-stu-id="91a56-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="91a56-136">Izmaksu aprēķina piemērs</span><span class="sxs-lookup"><span data-stu-id="91a56-136">Cost calculation example</span></span>

<span data-ttu-id="91a56-137">Ja izmantojat lauku **Atgrieztā laidiena ID** atgriešanas pasūtījuma rindā, lai norādītu vienības izmaksu cenu, tiek izmantotas izmaksas atgriešanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="91a56-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="91a56-138">Ja tiek izmantota krājumu slēgšanas vai pārrēķināšanas funkcionalitāte, izmaksas tiek koriģētas sākotnējā pārdošanas rindā.</span><span class="sxs-lookup"><span data-stu-id="91a56-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="91a56-139">Izmaksas preču atgriešanas pasūtījuma rindā tiek automātiski koriģētas, lai atspoguļotu tādas pašas izmaksas par gabalu.</span><span class="sxs-lookup"><span data-stu-id="91a56-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="91a56-140">Izveidojiet un izlaidiet preci, kuras nosaukums ir Pārbaude.</span><span class="sxs-lookup"><span data-stu-id="91a56-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="91a56-141">Veidlapā **Detalizēta informācija par izlaistajām precēm** norādiet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="91a56-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="91a56-142">Kopsavilkuma cilnes **Pārvaldīt izmaksas** laukā **Krājumu grupa** atlasiet grupu **Daļas**.</span><span class="sxs-lookup"><span data-stu-id="91a56-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="91a56-143">Kopsavilkuma cilnes **Vispārīgi** laukā **Krājumu modeļu grupa** atlasiet vienumu **DEF**.</span><span class="sxs-lookup"><span data-stu-id="91a56-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="91a56-144">Kopsavilkuma cilnē **Pirkšana** laukā **Cena** ierakstiet vērtību 10,00 kā krājuma izmaksu cenu.</span><span class="sxs-lookup"><span data-stu-id="91a56-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="91a56-145">**Darbību rūtī** noklikšķiniet uz **Dimensiju grupas**.</span><span class="sxs-lookup"><span data-stu-id="91a56-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="91a56-146">Laukā **Noliktavas dimensiju grupa** atlasiet **Tikai Vieta un Noliktava**.</span><span class="sxs-lookup"><span data-stu-id="91a56-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="91a56-147">Laukā **Izsekošanas dimensiju grupa** atlasiet **Nav aktīvu izsekošanas dimensiju**.</span><span class="sxs-lookup"><span data-stu-id="91a56-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="91a56-148">Izveidojiet pirkšanas pasūtījumu 10 gabaliem pārbaudāmā krājuma ar cenu 6,00 par gabalu un pēc tam grāmatojiet pirkšanas pasūtījuma rēķinu.</span><span class="sxs-lookup"><span data-stu-id="91a56-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="91a56-149">Izveidojiet otro pirkšanas pasūtījumu 10 gabaliem pārbaudāmā krājuma ar cenu 8,00 par gabalu un pēc tam grāmatojiet pirkšanas pasūtījuma rēķinu.</span><span class="sxs-lookup"><span data-stu-id="91a56-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="91a56-150">Grāmatojiet pārdošanas pasūtījuma rēķinu par piecu pārbaudes krājuma gabalu pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="91a56-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="91a56-151">Šajā gadījumā pārdošanas pasūtījuma rindas izmaksas ir 35,00 (5 gabali \* 7,00 vidējās izmaksas par gabalu).</span><span class="sxs-lookup"><span data-stu-id="91a56-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="91a56-152">Izveidojiet atgriešanas pasūtījumu debitoram.</span><span class="sxs-lookup"><span data-stu-id="91a56-152">Create a return order for the customer.</span></span> <span data-ttu-id="91a56-153">Veidlapā **Atrast pārdošanas pasūtījumu** atlasiet rēķina rindu un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="91a56-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="91a56-154">Formā **Atgriešanas pasūtījums — AKA kods: %1, %2** pārbaudiet, vai ir ģenerēts atgriešanas pasūtījums, lai atgrieztu pārbaudes krājumu.</span><span class="sxs-lookup"><span data-stu-id="91a56-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="91a56-155">Atgriešanas pasūtījuma iestatītais daudzums ir -5,00.</span><span class="sxs-lookup"><span data-stu-id="91a56-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="91a56-156">Laukā **Atgrieztā laidiena ID** tiek parādīts laidiena ID.</span><span class="sxs-lookup"><span data-stu-id="91a56-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="91a56-157">Šis laidiena ID tiek ņemts no debitoram pārdotā krājuma sākotnējā pārdošanas pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="91a56-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="91a56-158">Laukā **Vienības izmaksu cena** tiek parādīta izmaksu cena no sākotnējās pārdošanas rindas.</span><span class="sxs-lookup"><span data-stu-id="91a56-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="91a56-159">Reģistrējiet atgrieztu krājumu saņemšanu.</span><span class="sxs-lookup"><span data-stu-id="91a56-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="91a56-160">Grāmatojiet pavadzīmi atgrieztajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="91a56-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="91a56-161">Iegrāmatojiet rēķinu atgriešanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="91a56-161">Post an invoice for the return order.</span></span> <span data-ttu-id="91a56-162">Saraksta lapā **Visi pārdošanas pasūtījumi** atlasiet pārdošanas pasūtījumu, kuram pasūtījuma tips ir **Atgrieztais pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="91a56-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="91a56-163">Atveriet veidlapu **Krājumu darbības**.</span><span class="sxs-lookup"><span data-stu-id="91a56-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="91a56-164">Pārbaudiet, vai atgriešanas izmaksas ir 7,00 par gabalu, izmantojot vērtību laukā **Vienības izmaksu cena**, ar kopsummu 35,00 laukā **Izmaksu summa**.</span><span class="sxs-lookup"><span data-stu-id="91a56-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="91a56-165">Varat atvērt formu **Krājumu transakcijas** formā **Atgriešanas pasūtījums — AKA kods: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="91a56-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="91a56-166">Režģī **Rindas** noklikšķiniet uz **Krājums** \> **Darbības**.</span><span class="sxs-lookup"><span data-stu-id="91a56-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="91a56-167">Sadaļā Krājumu un noliktavas pārvaldība izmantojiet veidlapu **Slēgšana un pielāgošana**, lai palaistu procedūru **3. Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="91a56-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="91a56-168">Šī darbība pielāgo izmaksas sākotnējā pārdošanas rindā, kuru aprēķinātā vērtība bija -35,00 (5 gabali \* 7,00), uz -30.00 (5 gabali \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="91a56-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="91a56-169">Tas ir tādēļ, ka krājumu modeļu grupa izmanto metodi “pirmie iekšā, pirmie ārā” (FIFO) un pirmā pirkšanas pasūtījuma FIFO izmaksas ir 6,00 vienības par gabalu.</span><span class="sxs-lookup"><span data-stu-id="91a56-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="91a56-170">Turklāt šī darbība pielāgo izmaksas pārdoto preču atgriešanas rindā atbilstoši izmaksām par gabalu sākotnējā pārdošanas rindā.</span><span class="sxs-lookup"><span data-stu-id="91a56-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="91a56-171">Tādēļ izmaksas atgriešanas rindās tiek pielāgotas no 35,00 uz 30,00.</span><span class="sxs-lookup"><span data-stu-id="91a56-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




