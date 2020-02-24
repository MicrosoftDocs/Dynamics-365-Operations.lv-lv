---
title: Brīva teksta rēķina izveide
description: Šajā tēmā izskaidrots, kā izveidot brīva teksta rēķinus.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 909dd5bcaf1fa3b82adb44d265e312f9acc607d2
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000074"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="8c72b-103">Brīva teksta rēķina izveide</span><span class="sxs-lookup"><span data-stu-id="8c72b-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c72b-104">Šajā tēmā izskaidrots, kā izveidot brīva teksta rēķinus.</span><span class="sxs-lookup"><span data-stu-id="8c72b-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="8c72b-105">Šai procedūrai izmantojiet demonstrācijas uzņēmuma **USMF** datus.</span><span class="sxs-lookup"><span data-stu-id="8c72b-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="8c72b-106">Brīva teksta rēķina izveidošana</span><span class="sxs-lookup"><span data-stu-id="8c72b-106">Create a free text invoice</span></span>

1. <span data-ttu-id="8c72b-107">Dodieties uz **Debitoru parādi \> Rēķini \> Visi brīva teksta rēķini**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="8c72b-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-108">Select **New**.</span></span>
3. <span data-ttu-id="8c72b-109">Laukā **Debitora konts** atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8c72b-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="8c72b-110">Pēc noklusējuma konts, kas ir atlasīts kā debitora konts, tiek izmantots kā rēķina konts.</span><span class="sxs-lookup"><span data-stu-id="8c72b-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="8c72b-111">Ja rēķins nav grāmatots, uzskaites statuss sākas ar **Notiek**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="8c72b-112">Rēķina numurs tiek piešķirts, kad rēķins tiek grāmatots.</span><span class="sxs-lookup"><span data-stu-id="8c72b-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="8c72b-113">Ja lietojat vienotās eiro maksājumu zonas (SEPA) mandātus, tad tiešā debeta mandāts automātiski tiek ievadīts, kad atlasāt debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="8c72b-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="8c72b-114">Laukā **Apraksts** ievadiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8c72b-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="8c72b-115">Laukā **Galvenais konts** norādiet kāda konta numuru, kuram nav dimensiju.</span><span class="sxs-lookup"><span data-stu-id="8c72b-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="8c72b-116">Dimensijas jūs ievadīsiet vēlākā šīs tēmas posmā.</span><span class="sxs-lookup"><span data-stu-id="8c72b-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="8c72b-117">Lai atrastu kontu, varat arī ievadīt vienu vai vairākas rakstzīmes galvenajam kontam un lietot uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="8c72b-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="8c72b-118">Atlasiet kopsavilkuma cilni **Rindas informācija**, lai galvenajam kontam pievienotu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="8c72b-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="8c72b-119">Atlasiet cilni **Finanšu dimensiju rinda**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="8c72b-120">Šīs dimensijas ir tikai atlasītajai rindai.</span><span class="sxs-lookup"><span data-stu-id="8c72b-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="8c72b-121">PVN grupu aizpilda no debitora datiem.</span><span class="sxs-lookup"><span data-stu-id="8c72b-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="8c72b-122">Ja debitoram nav PVN grupas, tad tiek izmantota PVN grupa no galvenā konta.</span><span class="sxs-lookup"><span data-stu-id="8c72b-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="8c72b-123">Krājumu PVN grupa tiek aizpildīta no galvenā konta datiem.</span><span class="sxs-lookup"><span data-stu-id="8c72b-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="8c72b-124">Ja galvenajam kontam nav krājuma PVN grupas, tad tiek izmantota Virsgrāmatas PVN parametros norādītā krājuma PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="8c72b-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="8c72b-125">Pēc izvēles: laukā **Daudzums** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8c72b-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="8c72b-126">Pēc izvēles: laukā **Vienības cena** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="8c72b-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="8c72b-127">Šī summa tiek aprēķināta kā daudzums reiz vienības cena.</span><span class="sxs-lookup"><span data-stu-id="8c72b-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="8c72b-128">Taču varat ignorēt šo aprēķinu, ievadot kādu summu.</span><span class="sxs-lookup"><span data-stu-id="8c72b-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="8c72b-129">Atlasiet **PVN**, lai skatītu rēķinam aprēķināto PVN.</span><span class="sxs-lookup"><span data-stu-id="8c72b-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="8c72b-130">Varat skatīt PVN summas šajā lapā, vai šīs summas varat ignorēt cilnē **Korekcija**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="8c72b-131">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-131">Select **OK**.</span></span>
12. <span data-ttu-id="8c72b-132">Atlasiet **Maksas**, lai savam rēķinam pievienotu kādu maksu. </span><span class="sxs-lookup"><span data-stu-id="8c72b-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="8c72b-133">Laikā **Maksu kods** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8c72b-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="8c72b-134">Laukā **Maksu vērtība** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="8c72b-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="8c72b-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="8c72b-135">Close the page.</span></span>
16. <span data-ttu-id="8c72b-136">Atlasiet **Kopsummas**, lai skatītu kopsavilkumu par rēķina detalizēto informāciju un kopsummām.</span><span class="sxs-lookup"><span data-stu-id="8c72b-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="8c72b-137">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-137">Select **Close**.</span></span>
18. <span data-ttu-id="8c72b-138">Atlasiet **Grāmatot**, lai rēķinu grāmatotu.</span><span class="sxs-lookup"><span data-stu-id="8c72b-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="8c72b-139">Joprojām būs iespēja atcelt pirms faktiskās iegrāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="8c72b-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="8c72b-140">Rēķinu drukāšanas laiku var mainīt.</span><span class="sxs-lookup"><span data-stu-id="8c72b-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="8c72b-141">Atlasiet **Pašreizējais**, lai katru rēķinu drukātu, līdzko tas ir atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="8c72b-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="8c72b-142">Atlasiet **Pēc**, lai drukāšanu veiktu pēc tam, kad ir atjaunināti visi rēķini.</span><span class="sxs-lookup"><span data-stu-id="8c72b-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="8c72b-143">Lai mainītu to, kā debitora kredīta limits tiek pārbaudīts pirms rēķina grāmatošanas, mainiet vērtību laukā **Kredīta limita veids**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="8c72b-144">Lai izdrukātu rēķinu, iestatiet šo opciju pozīcijā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="8c72b-145">Lai grāmatotu rēķinu, iestatiet šo opciju pozīcijā **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="8c72b-146">Rēķinu varat izdrukāt arī bez tā grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="8c72b-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="8c72b-147">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="8c72b-148">Kopēt rindas</span><span class="sxs-lookup"><span data-stu-id="8c72b-148">Copy lines</span></span>
<span data-ttu-id="8c72b-149">Lai kopētu rindas brīva teksta rēķinā, atlasiet vienu vai vairākas rindas un pēc tam atlasiet **Kopēt atlasītās rindas**.</span><span class="sxs-lookup"><span data-stu-id="8c72b-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="8c72b-150">Varat norādīt veicamo kopiju skaitu un varat arī kopēt piezīmes un pielikumus.</span><span class="sxs-lookup"><span data-stu-id="8c72b-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="8c72b-151">Varat vai nu kopēt sadales, vai atļaut tās no jauna izveidot pēc grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="8c72b-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="8c72b-152">Pēc rindu kopēšanas informāciju var mainīt pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="8c72b-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="8c72b-153">Brīva teksta rēķina izveide no veidnes</span><span class="sxs-lookup"><span data-stu-id="8c72b-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="8c72b-154">Brīva teksta rēķina izveidei varat izmantot veidni.</span><span class="sxs-lookup"><span data-stu-id="8c72b-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="8c72b-155">Cilnes **Rēķins** veidnē atlasot vienumu **Jauns no veidnes**, varat atlasīt veidnes nosaukumu un debitora kontu, ko izmantot jaunā brīva teksta rēķina izveidē.</span><span class="sxs-lookup"><span data-stu-id="8c72b-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="8c72b-156">Noklusējuma vērtības, piemēram, maksāšanas termiņus un maksāšanas metodi, var automātiski aizpildīt no debitora datiem, vai arī varat izmantot vērtības, kas tika saglabātas veidnē.</span><span class="sxs-lookup"><span data-stu-id="8c72b-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="8c72b-157">Jauns brīva teksta rēķins ir izveidots, un tā vērtības var rediģēt pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="8c72b-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
