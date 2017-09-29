--- 
title: "Brīva teksta rēķina izveidošana"
description: "Šajā uzdevuma ceļvedī ir parādīts, kā izveidot brīva teksta rēķinu."
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
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
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="55323-103">Brīva teksta rēķina izveidošana</span><span class="sxs-lookup"><span data-stu-id="55323-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55323-104">Šajā uzdevuma ceļvedī ir parādīts, kā izveidot brīva teksta rēķinu.</span><span class="sxs-lookup"><span data-stu-id="55323-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="55323-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="55323-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="55323-106">Pārejiet uz sadaļu Debitori > Rēķini > Visi brīva teksta rēķini.</span><span class="sxs-lookup"><span data-stu-id="55323-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="55323-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="55323-107">Click New.</span></span>
3. <span data-ttu-id="55323-108">Laukā Debitora konts atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="55323-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="55323-109">Rēķina konts pēc noklusējuma būs tas pats konts, kas tiek izmantots debitora kontam.</span><span class="sxs-lookup"><span data-stu-id="55323-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="55323-110">Uzskaites statuss sākas ar Notiek, ja rēķins nav grāmatots.</span><span class="sxs-lookup"><span data-stu-id="55323-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="55323-111">Rēķina numurs tiek piešķirts, kad rēķins tiek grāmatots.</span><span class="sxs-lookup"><span data-stu-id="55323-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="55323-112">Ja lietojat SEPA mandātus, tad tiešā debeta mandāts automātiski tiks aizpildīts ar mandātu, kad atlasāt debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="55323-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="55323-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="55323-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="55323-114">Laukā Galvenais konts norādiet kāda konta numuru bez dimensijām.</span><span class="sxs-lookup"><span data-stu-id="55323-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="55323-115">Lai atrastu savu kontu, varat arī ievadīt vienu vai vairākas rakstzīmes galvenajam kontam un lietot uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="55323-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="55323-116">Dimensijas jūs ievadīsiet vēlākā šī ceļveža posmā.</span><span class="sxs-lookup"><span data-stu-id="55323-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="55323-117">Izvērsiet kopsavilkuma cilni Detalizēta informācija par rindu, lai savam galvenajam kontam pievienotu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="55323-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="55323-118">Noklikšķiniet uz cilnes Finanšu dimensiju rinda.</span><span class="sxs-lookup"><span data-stu-id="55323-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="55323-119">Šīs dimensijas ir tikai atlasītajai rindai.</span><span class="sxs-lookup"><span data-stu-id="55323-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="55323-120">PVN grupa tiek aizpildīta no debitora datiem.</span><span class="sxs-lookup"><span data-stu-id="55323-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="55323-121">Ja debitoram nav PVN grupas, tad tiek izmantota PVN grupa no galvenā konta.</span><span class="sxs-lookup"><span data-stu-id="55323-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="55323-122">Krājumu PVN grupa tiek aizpildīta no galvenā konta datiem.</span><span class="sxs-lookup"><span data-stu-id="55323-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="55323-123">Ja galvenajam kontam nav krājuma PVN grupas, tad tiek izmantota virsgrāmatas PVN parametros norādītā krājuma PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="55323-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="55323-124">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="55323-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="55323-125">Daudzums ir neobligāts.</span><span class="sxs-lookup"><span data-stu-id="55323-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="55323-126">Laukā Vienības cena ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="55323-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="55323-127">Vienības cena ir neobligāta.</span><span class="sxs-lookup"><span data-stu-id="55323-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="55323-128">Šī summa tiek aprēķināta kā daudzums reiz vienības cena.</span><span class="sxs-lookup"><span data-stu-id="55323-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="55323-129">Taču varat ignorēt šo aprēķinu un ievadīt kādu summu.</span><span class="sxs-lookup"><span data-stu-id="55323-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="55323-130">Noklikšķiniet uz PVN, lai skatītu savam rēķinam aprēķināto PVN.</span><span class="sxs-lookup"><span data-stu-id="55323-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="55323-131">Skatiet PVN summas šajā lapā, vai šīs summas varat ignorēt cilnē Korekcija.</span><span class="sxs-lookup"><span data-stu-id="55323-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="55323-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="55323-132">Click OK.</span></span>
12. <span data-ttu-id="55323-133">Noklikšķiniet uz Maksas, lai savam rēķinam pievienotu kādu maksu.</span><span class="sxs-lookup"><span data-stu-id="55323-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="55323-134">Laukā Maksu kods ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="55323-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="55323-135">Laukā Maksu vērtība ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="55323-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="55323-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="55323-136">Close the page.</span></span>
16. <span data-ttu-id="55323-137">Noklikšķiniet uz Kopsummas, lai apskatītu kopsavilkumu par rēķina detalizēto informāciju un kopsummām.</span><span class="sxs-lookup"><span data-stu-id="55323-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="55323-138">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="55323-138">Click Close.</span></span>
18. <span data-ttu-id="55323-139">Lai grāmatotu rēķinu, klikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="55323-139">Click Post to post the invoice.</span></span> <span data-ttu-id="55323-140">Pirms grāmatošanas varēsiet to atcelt.</span><span class="sxs-lookup"><span data-stu-id="55323-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="55323-141">Lai mainītu savu rēķinu drukāšanas laiku: atlasiet Pašreizējais, lai katru rēķinu drukātu, līdzko tas ir atjaunināts, vai atlasiet Pēc, lai drukāšanu veiktu pēc tam, kad ir atjaunināti visi rēķini.</span><span class="sxs-lookup"><span data-stu-id="55323-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="55323-142">Ja vēlaties mainīt to, kā pirms grāmatošanas tiek pārbaudīts debitora kredīta limits, mainiet vienumu Kredīta limita tips.</span><span class="sxs-lookup"><span data-stu-id="55323-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="55323-143">Ja vēlaties drukāt rēķinu, atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="55323-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="55323-144">Ja vēlaties grāmatot rēķinu, atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="55323-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="55323-145">Rēķinu varat izdrukāt arī bez grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="55323-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="55323-146">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="55323-146">Click OK.</span></span>


