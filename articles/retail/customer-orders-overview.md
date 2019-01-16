---
title: "Debitoru pasūtījumi pārdošanas punktā Retail Modern POS (MPOS)"
description: "Šajā tēmā ir sniegta informācija par debitoru pasūtījumiem pārdošanas punktā Retail Modern POS (MPOS). Debitoru pasūtījumi tiek saukti arī par īpašajiem pasūtījumiem. Šajā tēmā ir iekļauta diskusija par saistītajiem parametriem un transakciju plūsmām."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: b54f39cc7896871d77f9371e6197bf6dbaac51de
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="customer-orders-in-retail-modern-pos-mpos"></a><span data-ttu-id="01b56-105">Debitoru pasūtījumi pārdošanas punktā Retail Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="01b56-105">Customer orders in Retail Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="01b56-106">Šajā tēmā ir sniegta informācija par debitoru pasūtījumiem pārdošanas punktā Retail Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="01b56-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="01b56-107">Debitoru pasūtījumi tiek saukti arī par īpašajiem pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="01b56-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="01b56-108">Šajā tēmā ir iekļauta diskusija par saistītajiem parametriem un transakciju plūsmām.</span><span class="sxs-lookup"><span data-stu-id="01b56-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="01b56-109">Visaptveroša kanāla mazumtirdzniecības pasaulē daudzi mazumtirgotāji nodrošina iespēju izmantot debitoru pasūtījumus jeb īpašos pasūtījumus, lai izpildītu dažādas preču un izpildes prasības.</span><span class="sxs-lookup"><span data-stu-id="01b56-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="01b56-110">Tālāk uzskaitīti daži tipiski scenāriji.</span><span class="sxs-lookup"><span data-stu-id="01b56-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="01b56-111">Debitors vēlas, lai preces tiek piegādātas uz konkrētu adresi konkrētā datumā.</span><span class="sxs-lookup"><span data-stu-id="01b56-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="01b56-112">Debitors preces vēlas saņemt tādā veikalā vai atrašanās vietā, kas atšķiras no veikala vai atrašanās vietas, kur debitors šīs preces iegādājās.</span><span class="sxs-lookup"><span data-stu-id="01b56-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="01b56-113">Debitors vēlas, lai klienta nopirktās preces tiktu izdotas kādam citam.</span><span class="sxs-lookup"><span data-stu-id="01b56-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="01b56-114">Mazumtirgotāji debitoru pasūtījumus izmanto arī ar mērķi mazināt pārdošanas zudumus, kurus pretējā gadījumā izraisītu krājumu deficīts, jo preces var piegādāt vai izdot dažādos laikos vai vietās.</span><span class="sxs-lookup"><span data-stu-id="01b56-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="01b56-115">Iestatīt debitoru pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="01b56-115">Set up customer orders</span></span>

<span data-ttu-id="01b56-116">Tālāk ir aprakstīti daži no parametriem, ko var iestatīt lapā **Mazumtirdzniecības parametri**, lai definētu debitoru pasūtījumu izpildi.</span><span class="sxs-lookup"><span data-stu-id="01b56-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="01b56-117">**Noklusējuma depozīts procentos** — norādiet summu, kas debitoram ir jāsamaksā kā depozīts, lai pasūtījumu varētu apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="01b56-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="01b56-118">Noklusējuma depozīta summa tiek aprēķināta kā procenti no pasūtījuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="01b56-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="01b56-119">Atkarībā no privilēģijām veikala darbinieks var spēt ignorēt šo summu, izmantojot funkciju **Depozīta ignorēšana**.</span><span class="sxs-lookup"><span data-stu-id="01b56-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="01b56-120">**Atcelšanas maksa procentos** — ja debitora pasūtījuma atcelšanas gadījumā tiek piemērota maksa, norādiet šīs maksas summu.</span><span class="sxs-lookup"><span data-stu-id="01b56-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="01b56-121">**Atcelšanas maksas kods** — ja debitora pasūtījuma atcelšanas gadījumā tiek piemērota maksa, šī maksa pārdošanas pasūtījuma tiek apzīmēta ar maksas kodu.</span><span class="sxs-lookup"><span data-stu-id="01b56-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="01b56-122">Izmantojiet šo parametru, lai definētu atcelšanas maksas kodu.</span><span class="sxs-lookup"><span data-stu-id="01b56-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="01b56-123">**Nosūtīšanas maksas kods** — mazumtirgotāji var iekasēt papildu maksu par preču nosūtīšanu debitoram.</span><span class="sxs-lookup"><span data-stu-id="01b56-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="01b56-124">Šīs nosūtīšanas maksas summa pārdošanas pasūtījumā tiek apzīmēta ar maksas kodu.</span><span class="sxs-lookup"><span data-stu-id="01b56-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="01b56-125">Izmantojiet šo parametru, lai nosūtīšanas maksas kodu kartētu uz nosūtīšanas maksām debitora pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="01b56-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="01b56-126">**Atmaksāt nosūtīšanas maksas** — norādiet, vai ar debitora pasūtījumu saistītās nosūtīšanas maksas tiek atmaksātas.</span><span class="sxs-lookup"><span data-stu-id="01b56-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="01b56-127">**Maksimālā summa bez apstiprināšanas** — ja nosūtīšanas maksas tiek atmaksātas, norādiet maksimālo nosūtīšanas maksas atmaksu summu dažādos atgriešanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="01b56-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="01b56-128">Ja šī summa ir pārsniegta, lai turpinātu atmaksāšanas procesu, ir nepieciešams vadītāja veikts pārlabojums.</span><span class="sxs-lookup"><span data-stu-id="01b56-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="01b56-129">Lai izpildītu tālāk norādītos scenārijus, nosūtīšanas maksu atmaksa var pārsniegt sākotnēji samaksāto summu.</span><span class="sxs-lookup"><span data-stu-id="01b56-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="01b56-130">Maksas tiek lietotas pārdošanas pasūtījuma galvenes līmenī, un gadījumā, ja tiek atgriezts kāds daudzums no ražošanas rindas, maksimālo šīm precēm atļauto atmaksu par nosūtīšanas maksām un daudzumu nevar noteikt veidā, kas ir piemērots visiem mazumtirdzniecības debitoriem.</span><span class="sxs-lookup"><span data-stu-id="01b56-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    - <span data-ttu-id="01b56-131">Nosūtīšanas maksas rodas katrai nosūtīšanas instancei.</span><span class="sxs-lookup"><span data-stu-id="01b56-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="01b56-132">Ja debitors preces atgriež vairākas reizes, bet mazumtirgotāja politikā ir noteikts, ka atgriešanas nosūtīšanas izmaksas sedz mazumtirgotājs, tad nosūtīšanas maksas pārsniedz faktiskās nosūtīšanas maksas.</span><span class="sxs-lookup"><span data-stu-id="01b56-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="01b56-133">Transakciju plūsma debitoru pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="01b56-133">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="01b56-134">Izveidot debitora pasūtījumu pārdošanas punktā Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="01b56-134">Create a customer order in Retail Modern POS</span></span>

1. <span data-ttu-id="01b56-135">Pievienojiet transakcijai debitoru.</span><span class="sxs-lookup"><span data-stu-id="01b56-135">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="01b56-136">Pievienojiet grozam preces.</span><span class="sxs-lookup"><span data-stu-id="01b56-136">Add products to the cart.</span></span>
3. <span data-ttu-id="01b56-137">Noklikšķiniet uz **Izveidot debitora pasūtījumu** un pēc tam atlasiet pasūtījuma tipu.</span><span class="sxs-lookup"><span data-stu-id="01b56-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="01b56-138">Pasūtījuma tips var būt **Debitora pasūtījums** vai **Piedāvājums**.</span><span class="sxs-lookup"><span data-stu-id="01b56-138">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="01b56-139">Noklikšķiniet uz **Nosūtīt atlasīto** vai **Nosūtīt visu**, lai preces nosūtītu uz adresi debitora kontā, norādiet pieprasīto nosūtīšanas datumu un norādiet nosūtīšanas maksas.</span><span class="sxs-lookup"><span data-stu-id="01b56-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="01b56-140">Noklikšķiniet uz **Izdot atlasīto** vai **Izdot visu**, lai atlasītu preces, kas tiks izdotas no pašreizējā veikala vai cita veikala norādītajā datumā.</span><span class="sxs-lookup"><span data-stu-id="01b56-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="01b56-141">Iekasējiet depozīta summu, ja ir nepieciešams depozīts.</span><span class="sxs-lookup"><span data-stu-id="01b56-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="01b56-142">Rediģēt esošu debitora pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="01b56-142">Edit an existing customer order</span></span>

1. <span data-ttu-id="01b56-143">Sākumlapa noklikšķiniet uz **Atrast pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="01b56-143">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="01b56-144">Atrodiet un atlasiet rediģējamo pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="01b56-144">Find and select the order to edit.</span></span> <span data-ttu-id="01b56-145">Lapas apakšpusē noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="01b56-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="01b56-146">Izdot pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="01b56-146">Pick up an order</span></span>

1. <span data-ttu-id="01b56-147">Sākumlapa noklikšķiniet uz **Atrast pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="01b56-147">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="01b56-148">Atlasiet izdodamo pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="01b56-148">Select the order to pick up.</span></span> <span data-ttu-id="01b56-149">Lapas apakšpusē noklikšķiniet uz **Izdošana un iepakošana**.</span><span class="sxs-lookup"><span data-stu-id="01b56-149">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="01b56-150">Noklikšķiniet uz **Izdot**.</span><span class="sxs-lookup"><span data-stu-id="01b56-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="01b56-151">Atcelt pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="01b56-151">Cancel an order</span></span>

1. <span data-ttu-id="01b56-152">Sākumlapa noklikšķiniet uz **Atrast pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="01b56-152">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="01b56-153">Atlasiet atceļamo pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="01b56-153">Select the order to cancel.</span></span> <span data-ttu-id="01b56-154">Lapas apakšpusē noklikšķiniet uz **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="01b56-154">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="01b56-155">Izveidot atgriešanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="01b56-155">Create a return order</span></span>

1. <span data-ttu-id="01b56-156">Sākumlapa noklikšķiniet uz **Atrast pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="01b56-156">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="01b56-157">Atlasiet atgriežamo pasūtījumu, atlasiet rēķinu šim pasūtījumam un pēc tam atlasiet preču rindu, kuras preces jāatdod.</span><span class="sxs-lookup"><span data-stu-id="01b56-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="01b56-158">Lapas apakšpusē noklikšķiniet uz **Atgriezt pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="01b56-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="01b56-159">Asinhrona transakciju plūsma debitoru pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="01b56-159">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="01b56-160">Debitoru pasūtījumus no pārdošanas punkta (point of sale — POS) klienta var izveidot gan sinhronajā režīmā, gan asinhronajā režīmā.</span><span class="sxs-lookup"><span data-stu-id="01b56-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="01b56-161">Iespējot debitoru pasūtījumu izveidošanu asinhronajā režīmā</span><span class="sxs-lookup"><span data-stu-id="01b56-161">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="01b56-162">Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profils** &gt; **Funkcionalitātes profili**.</span><span class="sxs-lookup"><span data-stu-id="01b56-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="01b56-163">Kopsavilkuma cilnē **Vispārīgi** opcijai **Izveidot debitora pasūtījumu asinhronā režīmā** iestatiet vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="01b56-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="01b56-164">Kad opcija **Izveidot debitora pasūtījumu asinhronā režīmā** ir iestatīta uz **Jā**, debitoru pasūtījumi vienmēr tiek veidoti asinhronajā režīmā, pat tad, ja ir pieejams pakalpojums Retail Transaction Service (RTS).</span><span class="sxs-lookup"><span data-stu-id="01b56-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="01b56-165">Ja šī opcija ir iestatīta uz **Nē**, tad debitoru pasūtījumi vienmēr tiek veidoti sinhronajā režīmā, izmantojot RTS.</span><span class="sxs-lookup"><span data-stu-id="01b56-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="01b56-166">Kad debitoru pasūtījumi tiek veidoti asinhronajā režīmā, tie tiek izvilkti un ievietoti programmatūrā Dynamics 365 for Retail, izmantojot vilkšanas (Pull — P) darbus.</span><span class="sxs-lookup"><span data-stu-id="01b56-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="01b56-167">Kad manuāli vai pakešuzdevuma apstrādes ietvaros tiek palaista funkcija **Sinhronizēt pasūtījumus**, programmatūrā Dynamics 365 for Retail tiek izveidoti atbilstošie pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="01b56-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01b56-168">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="01b56-168">Additional resources</span></span>

[<span data-ttu-id="01b56-169">Hibrīda debitoru pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="01b56-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)

