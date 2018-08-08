--- 
title: "Brīva teksta rēķina izveidošana"
description: "Šajā rakstā ir paskaidrots, kā izveidot brīva teksta rēķinu."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="eb804-103">Brīva teksta rēķina izveidošana</span><span class="sxs-lookup"><span data-stu-id="eb804-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb804-104">Šajā rakstā ir paskaidrots, kā izveidot brīva teksta rēķinu.</span><span class="sxs-lookup"><span data-stu-id="eb804-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="eb804-105">Šai procedūrai izmantojiet demonstrācijas uzņēmuma “USMF” datus.</span><span class="sxs-lookup"><span data-stu-id="eb804-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="eb804-106">Brīva teksta rēķina izveidošana</span><span class="sxs-lookup"><span data-stu-id="eb804-106">Create a free text invoice</span></span>

1. <span data-ttu-id="eb804-107">Pārejiet uz sadaļu Debitori > Rēķini > Visi brīva teksta rēķini.</span><span class="sxs-lookup"><span data-stu-id="eb804-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="eb804-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="eb804-108">Click New.</span></span>
3. <span data-ttu-id="eb804-109">Laukā Debitora konts atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb804-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="eb804-110">Rēķina konts pēc noklusējuma būs tas pats konts, kas tiek izmantots debitora kontam.</span><span class="sxs-lookup"><span data-stu-id="eb804-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="eb804-111">Uzskaites statuss sākas ar Notiek, ja rēķins nav grāmatots.</span><span class="sxs-lookup"><span data-stu-id="eb804-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="eb804-112">Rēķina numurs tiek piešķirts, kad rēķins tiek grāmatots.</span><span class="sxs-lookup"><span data-stu-id="eb804-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="eb804-113">Ja lietojat SEPA mandātus, tad tiešā debeta mandāts automātiski tiks aizpildīts ar mandātu, kad atlasāt debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="eb804-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="eb804-114">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb804-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="eb804-115">Laukā Galvenais konts norādiet kāda konta numuru bez dimensijām.</span><span class="sxs-lookup"><span data-stu-id="eb804-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="eb804-116">Lai atrastu savu kontu, varat arī ievadīt vienu vai vairākas rakstzīmes galvenajam kontam un lietot uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="eb804-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="eb804-117">Dimensijas jūs ievadīsiet vēlākā šī ceļveža posmā.</span><span class="sxs-lookup"><span data-stu-id="eb804-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="eb804-118">Izvērsiet kopsavilkuma cilni Detalizēta informācija par rindu, lai savam galvenajam kontam pievienotu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="eb804-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="eb804-119">Noklikšķiniet uz cilnes Finanšu dimensiju rinda.</span><span class="sxs-lookup"><span data-stu-id="eb804-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="eb804-120">Šīs dimensijas ir tikai atlasītajai rindai.</span><span class="sxs-lookup"><span data-stu-id="eb804-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="eb804-121">PVN grupa tiek aizpildīta no debitora datiem.</span><span class="sxs-lookup"><span data-stu-id="eb804-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="eb804-122">Ja debitoram nav PVN grupas, tad tiek izmantota PVN grupa no galvenā konta.</span><span class="sxs-lookup"><span data-stu-id="eb804-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="eb804-123">Krājumu PVN grupa tiek aizpildīta no galvenā konta datiem.</span><span class="sxs-lookup"><span data-stu-id="eb804-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="eb804-124">Ja galvenajam kontam nav krājuma PVN grupas, tiek izmantota Virsgrāmatas PVN parametru sadaļā norādītā krājuma PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="eb804-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="eb804-125">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="eb804-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="eb804-126">Daudzums ir neobligāts.</span><span class="sxs-lookup"><span data-stu-id="eb804-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="eb804-127">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="eb804-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="eb804-128">Vienības cena ir neobligāta.</span><span class="sxs-lookup"><span data-stu-id="eb804-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="eb804-129">Šī summa tiek aprēķināta kā daudzums reiz vienības cena.</span><span class="sxs-lookup"><span data-stu-id="eb804-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="eb804-130">Taču varat ignorēt šo aprēķinu un ievadīt kādu summu.</span><span class="sxs-lookup"><span data-stu-id="eb804-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="eb804-131">Noklikšķiniet uz PVN, lai skatītu savam rēķinam aprēķināto PVN.</span><span class="sxs-lookup"><span data-stu-id="eb804-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="eb804-132">Skatiet PVN summas šajā lapā, vai šīs summas varat ignorēt cilnē Korekcija.</span><span class="sxs-lookup"><span data-stu-id="eb804-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="eb804-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="eb804-133">Click OK.</span></span>
12. <span data-ttu-id="eb804-134">Noklikšķiniet uz Maksas, lai savam rēķinam pievienotu kādu maksu.</span><span class="sxs-lookup"><span data-stu-id="eb804-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="eb804-135">Laukā Maksu kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb804-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="eb804-136">Laukā Maksu vērtība ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="eb804-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="eb804-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="eb804-137">Close the page.</span></span>
16. <span data-ttu-id="eb804-138">Noklikšķiniet uz Kopsummas, lai apskatītu kopsavilkumu par rēķina detalizēto informāciju un kopsummām.</span><span class="sxs-lookup"><span data-stu-id="eb804-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="eb804-139">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="eb804-139">Click Close.</span></span>
18. <span data-ttu-id="eb804-140">Lai grāmatotu rēķinu, klikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="eb804-140">Click Post to post the invoice.</span></span> <span data-ttu-id="eb804-141">Pirms grāmatošanas varēsiet to atcelt.</span><span class="sxs-lookup"><span data-stu-id="eb804-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="eb804-142">Lai mainītu savu rēķinu drukāšanas laiku: atlasiet Pašreizējais, lai katru rēķinu drukātu, līdzko tas ir atjaunināts, vai atlasiet Pēc, lai drukāšanu veiktu pēc tam, kad ir atjaunināti visi rēķini.</span><span class="sxs-lookup"><span data-stu-id="eb804-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="eb804-143">Ja vēlaties mainīt to, kā pirms grāmatošanas tiek pārbaudīts debitora kredīta limits, mainiet vienumu Kredīta limita tips.</span><span class="sxs-lookup"><span data-stu-id="eb804-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="eb804-144">Ja vēlaties drukāt rēķinu, atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="eb804-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="eb804-145">Ja vēlaties grāmatot rēķinu, atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="eb804-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="eb804-146">Rēķinu varat izdrukāt arī bez grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="eb804-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="eb804-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="eb804-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="eb804-148">Kopēt rindas</span><span class="sxs-lookup"><span data-stu-id="eb804-148">Copy lines</span></span>
<span data-ttu-id="eb804-149">Lai kopētu rindas brīva teksta rēķinā, atlasiet vienu vai vairākas rindas un pēc tam noklikšķiniet uz Kopēt atlasītās rindas.</span><span class="sxs-lookup"><span data-stu-id="eb804-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="eb804-150">Var norādīt kopiju skaitu vai kopēt piezīmes un pielikumus.</span><span class="sxs-lookup"><span data-stu-id="eb804-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="eb804-151">Varat kopēt sadales vai atļaut tās no jauna uzveidot pēc grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="eb804-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="eb804-152">Kopējot rindas, informāciju var mainīt pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="eb804-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="eb804-153">Brīva teksta rēķina izveide no veidnes</span><span class="sxs-lookup"><span data-stu-id="eb804-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="eb804-154">Brīva teksta rēķina izveidei varat izmantot veidni.</span><span class="sxs-lookup"><span data-stu-id="eb804-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="eb804-155">Cilnes “Rēķins” veidnē atlasot vienumu “Jauns”, varat atlasīt veidnes nosaukumu un debitora kontu, ko izmantot jaunā brīva teksta rēķina izveidē.</span><span class="sxs-lookup"><span data-stu-id="eb804-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="eb804-156">Varat arī izvēlēties noklusējuma vērtības, piemēram, maksāšanas termiņus un debitora maksāšanas metodi, vai izmantot vērtības, kas tika saglabātas veidnē.</span><span class="sxs-lookup"><span data-stu-id="eb804-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="eb804-157">Jauns brīva teksta rēķins tiks izveidots un varēsit rediģēt tajā esošās vērtības.</span><span class="sxs-lookup"><span data-stu-id="eb804-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


