---
title: Nodoklis nav aprēķināts vai nodokļa summa ir nulle
description: Šajā tēmā ir sniegta traucējummeklēšanas informācija, kas var palīdzēt, kad nodokļa summa ir 0 (nulle) vai nodoklis nav aprēķināts.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947674"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="8b42a-103">Nodoklis nav aprēķināts vai nodokļa summa ir nulle</span><span class="sxs-lookup"><span data-stu-id="8b42a-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b42a-104">Transakcijai, iespējams, ir rindas summa, kas nav 0 (nulle), bet vai nu nodoklis nav aprēķināts, vai aprēķinātā nodokļa summa ir 0.</span><span class="sxs-lookup"><span data-stu-id="8b42a-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="8b42a-105">Lai novērstu šo problēmu, ja nepieciešams, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8b42a-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="8b42a-106">Pārbaudiet, vai transakcija pareizi atlasīja nodokļu kodus</span><span class="sxs-lookup"><span data-stu-id="8b42a-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="8b42a-107">Ja transakcija neatlasa pareizos nodokļu kodus vai neatlasa nodokļu kodus, tai netiks aprēķināti nodokļi.</span><span class="sxs-lookup"><span data-stu-id="8b42a-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="8b42a-108">Lai pārbaudītu, vai darbība pareizi atlasa nodokļu kodus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="8b42a-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="8b42a-109">Transakciju rindā kopsavilkuma cilnē **Rindas informācija**, cilnē **Iestatījums** sadaļā **PVN** pārbaudiet, vai pareizās PVN grupas ir atlasītas laukos **Krājumu PVN grupa** un **PVN grupa**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="8b42a-110">Ja nav atlasītas pareizās nodokļu grupas, atlasiet tās.</span><span class="sxs-lookup"><span data-stu-id="8b42a-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="8b42a-111">[![Krājumu PVN grupas un PVN grupas lauki](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="8b42a-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="8b42a-112">Dodieties uz **Nodokļi** \> **Netiešie nodokļi** \> **Pārdošanas nodoklis** \> **Pārdošanas nodokļa grupas**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="8b42a-113">Atlasiet atbilstošo PVN grupu un pēc tam kopsavilkuma cilnē **Iestatījumi** atzīmējiet PVN kodu laukā **PVN kods**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="8b42a-114">[![PVN grupu lapa](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="8b42a-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="8b42a-115">Dodieties uz **Nodokļi** \> **Netiešie nodokļi** \> **PVN** \> **Krājuma PVN grupas**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="8b42a-116">Atlasiet atbilstošo krājumu PVN grupu un pēc tam kopsavilkuma cilnē **Iestatījumi** pārbaudiet, vai PVN kods laukā **PVN kods** atbilst PVN grupas PVN kodam.</span><span class="sxs-lookup"><span data-stu-id="8b42a-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="8b42a-117">[![Krājuma PVN grupu lapa](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="8b42a-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="8b42a-118">Ja nodokļu kodi neatbilst, atjauniniet PVN kodu vienai no grupām.</span><span class="sxs-lookup"><span data-stu-id="8b42a-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="8b42a-119">Pārbaudiet, vai atlasītie nodokļu kodi nav neapliekajami un tiem ir pareizā nodokļu likmes vērtība</span><span class="sxs-lookup"><span data-stu-id="8b42a-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="8b42a-120">Ja nodokļu kodi ir neapliekami vai arī nodokļa likme ir 0 (nulle), nodokļu aprēķina rezultāts būs 0.</span><span class="sxs-lookup"><span data-stu-id="8b42a-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="8b42a-121">Veiciet šīs darbības, lai noteiktu, vai atlasītie nodokļu kodi ir neapliekami un vai tiem tiek piemērota pareizā nodokļu likme.</span><span class="sxs-lookup"><span data-stu-id="8b42a-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="8b42a-122">Dodieties uz **Nodokļi** \> **Netiešie nodokļi** \> **Pārdošanas nodoklis** \> **Pārdošanas nodokļa grupas**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="8b42a-123">Atlasiet atbilstošo PVN grupu un pēc tam kopsavilkuma cilnē **Iestatījumi** pārbaudiet, vai izvēles rūtiņa **Neapliekams** ir notīrīta.</span><span class="sxs-lookup"><span data-stu-id="8b42a-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="8b42a-124">Ja tas ir atlasīts, notīriet to.</span><span class="sxs-lookup"><span data-stu-id="8b42a-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="8b42a-125">[![Neapliekamā izvēles rūtiņa PVN grupu lapā](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="8b42a-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="8b42a-126">Dodieties uz **Nodoklis** \> **Netiešie nodokļi** \> **PVN** \> **PVN kodi**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="8b42a-127">Atlasiet atbilstošo PVN kodu un pēc tam pārbaudiet, ka nodokļa likmes vērtība laukā **Vērtība** nav 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="8b42a-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="8b42a-128">Ja tā ir 0, atjauniniet lauku tā, lai tas būtu iestatīts uz pareizo nodokļa likmi.</span><span class="sxs-lookup"><span data-stu-id="8b42a-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="8b42a-129">[![Vērtības lauks lapā PVN kodu vērtības](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="8b42a-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="8b42a-130">Noteikt, vai nulle ir pareizā nodokļa summa</span><span class="sxs-lookup"><span data-stu-id="8b42a-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="8b42a-131">Dažos scenārijos nodokļa summa 0 (nulle) ir pareiza.</span><span class="sxs-lookup"><span data-stu-id="8b42a-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="8b42a-132">Veiciet šīs darbības, lai noteiktu, vai 0 ir pareizā nodokļu summa jūsu transakcijai.</span><span class="sxs-lookup"><span data-stu-id="8b42a-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="8b42a-133">Dodieties uz **Virsgrāmata** \> **Virsgrāmatas iestatīšana** \> **Virsgrāmatas parametri**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="8b42a-134">Cilnē **PVN** laukā **Aprēķina metode** pārbaudiet, vai ir atlasīta **Kopsumma**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="8b42a-135">[![Aprēķina metodes lauks virsgrāmatas parametru lapā](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="8b42a-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="8b42a-136">Dodieties uz **Nodoklis** \> **Netiešie nodokļi** \> **PVN** \> **PVN kodi**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="8b42a-137">Atlasiet atbilstošo PVN kodu, atlasiet **Aprēķins** \> **Robežbāze** un pārbaudiet, vai aprēķina pamatā ir iestatīta **Rēķina bilances neto summa** vai **rēķina kopsumma, iekļaujot citas PVN summas**.</span><span class="sxs-lookup"><span data-stu-id="8b42a-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="8b42a-138">Plašāku informāciju skatiet [Rēķina kopsumma, iekļaujot citas PVN summas](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="8b42a-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="8b42a-139">Ja pareizās vērtības ir iestatītas 2. un 4. darbībā, nosakiet, vai transakcijas kopsumma ir 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="8b42a-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="8b42a-140">Ja kopējā summa ir 0, nodokļa summa 0 ir paredzamais rezultāts.</span><span class="sxs-lookup"><span data-stu-id="8b42a-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="8b42a-141">Tā kā nodokļa aprēķins ir balstīts uz rēķina bilances kopsummu un šī summa nav rinda pa rindai, nodokļa summa 0 tiks piešķirta katrai rindai pēc nodokļu aprēķina.</span><span class="sxs-lookup"><span data-stu-id="8b42a-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="8b42a-142">Noteikt, vai pielāgojums pastāv</span><span class="sxs-lookup"><span data-stu-id="8b42a-142">Determine whether customization exists</span></span>

<span data-ttu-id="8b42a-143">Ja esat pabeidzis iepriekšējās sadaļās norādītās darbības, bet nav atraduši nekādu problēmu, nosakiet, vai pielāgošana eksistē.</span><span class="sxs-lookup"><span data-stu-id="8b42a-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="8b42a-144">Ja pielāgošana nepastāv, izveidojiet Microsoft pakalpojuma pieprasījumu turpmākam atbalstam.</span><span class="sxs-lookup"><span data-stu-id="8b42a-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
