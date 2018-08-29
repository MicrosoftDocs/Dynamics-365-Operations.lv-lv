---
title: "PVN aprēķina metodes laukā Izcelsme"
description: "Šajā rakstā ir aprakstītas lauka Izcelsme opcijas PVN kodu lapā un kā PVN tiek aprēķināts atkarībā no atlasītās PVN koda opcijas."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1473eeb2950296f5ae6250d7a53794af3d9cba81
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="a6bef-103">PVN aprēķina metodes laukā Izcelsme</span><span class="sxs-lookup"><span data-stu-id="a6bef-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="a6bef-104">Šajā rakstā ir aprakstītas lauka Izcelsme opcijas PVN kodu lapā un kā PVN tiek aprēķināts atkarībā no atlasītās PVN koda opcijas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="a6bef-105">Katram lapā PVN kodi izveidotajam PVN kodam laukā Izcelsme ir jāatlasa aprēķina metode, kas tiek lietota nodokļu pamatsummai.</span><span class="sxs-lookup"><span data-stu-id="a6bef-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="a6bef-106">Procenti no neto summas</span><span class="sxs-lookup"><span data-stu-id="a6bef-106">Percentage of net amount</span></span>
<span data-ttu-id="a6bef-107">Aprēķina metode Procenti no neto summas ir lauka Izcelsme noklusējuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="a6bef-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="a6bef-108">PVN tiek aprēķināts kā procenti no pirkšanas vai pārdošanas summas, neieskaitot nekādu citu PVN.</span><span class="sxs-lookup"><span data-stu-id="a6bef-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="a6bef-109">Paraugs</span><span class="sxs-lookup"><span data-stu-id="a6bef-109">Example</span></span>

<span data-ttu-id="a6bef-110">Nodokļa likme ir 25%.</span><span class="sxs-lookup"><span data-stu-id="a6bef-110">The tax rate is 25%.</span></span> <span data-ttu-id="a6bef-111">Rēķina rindā ir norādīts daudzums 10 vienības ar vienības cenu 1,00, un debitors var saņemt rindas atlaidi 10%</span><span class="sxs-lookup"><span data-stu-id="a6bef-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="a6bef-112">Neto summa: (10 x 1,00) – 10% = 9,00 PVN: 9,00 x 25% = 2,25 Kopsumma: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="a6bef-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="a6bef-113"> Procenti no bruto summas</span><span class="sxs-lookup"><span data-stu-id="a6bef-113">Percentage of gross amount</span></span>
<span data-ttu-id="a6bef-114">Ja atlasāt metodi Procenti no bruto summas, PVN tiek aprēķināts kā procenti no bruto pārdošanas summas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="a6bef-115">Bruto summa ir rindas neto summa, ieskaitot visus rindas nodokļus un nodevas, izņemot to vienu nodokli, kuram lauka Izcelsme vērtība ir Procenti no bruto summas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="a6bef-116">Paraugs</span><span class="sxs-lookup"><span data-stu-id="a6bef-116">Example</span></span>

<span data-ttu-id="a6bef-117">Nodokļu iestāde krājumu ir aplikusi ar speciāliem nodokļiem.</span><span class="sxs-lookup"><span data-stu-id="a6bef-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="a6bef-118">Šo nodokļu summa tiek pievienota neto summai pirms PVN aprēķināšanas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="a6bef-119">Tiek izmantoti tālāk norādītie PVN kodi.</span><span class="sxs-lookup"><span data-stu-id="a6bef-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="a6bef-120">1. NODOKLIS = 10%, izmantojot aprēķina metodi Procenti no neto summas</span><span class="sxs-lookup"><span data-stu-id="a6bef-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="a6bef-121">2. NODOKLIS = 20%, izmantojot aprēķina metodi Procenti no neto summas</span><span class="sxs-lookup"><span data-stu-id="a6bef-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="a6bef-122">PVN = 25%, izmantojot aprēķina metodi Procenti no bruto summas</span><span class="sxs-lookup"><span data-stu-id="a6bef-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="a6bef-123">Ja neto summa ir 10,00, tad 1. NODOKLIS ir 1,00 (10,00 x 10%) un 2. nodoklis ir 2,00 (10,00 x 20%).</span><span class="sxs-lookup"><span data-stu-id="a6bef-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="a6bef-124">Tālāk ir norādītas summas. Bruto summa: neto summa + 1. NODOKĻA summa + 2. NODOKĻA summa (10,00 + 1,00 + 2,00) = 13,00 PVN: 13,00 x 25% = 3,25 NODOKĻI un PVN kopā: 1,00 + 2,00 + 3,25 = 6,25 Kopsumma: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="a6bef-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="a6bef-125">**Piezīme.**</span><span class="sxs-lookup"><span data-stu-id="a6bef-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bef-126">Transakcijai var izmantoti tikai vienu nodokļa kodu, kam ir iestatīta lauka Izcelsme vērtība Procenti no bruto summas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="a6bef-127">Ja transakcijai ir norādīti vairāki šādi nodokļu kodi, tiek parādīts kļūdas ziņojums par to, ka nevar aprēķināt PVN.</span><span class="sxs-lookup"><span data-stu-id="a6bef-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="a6bef-128">PVN %</span><span class="sxs-lookup"><span data-stu-id="a6bef-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="a6bef-129">Ja atlasāt lauka Izcelsme vērtību PVN %, PVN tiek aprēķināts kā procenti no PVN, kas ir atlasīts laukā PVN uz PVN.</span><span class="sxs-lookup"><span data-stu-id="a6bef-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="a6bef-130">Vispirms tiek aprēķināts PVN, kas ir atlasīts laukā PVN uz PVN.</span><span class="sxs-lookup"><span data-stu-id="a6bef-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="a6bef-131">Pēc tam otrs PVN tiek aprēķināts, pamatojoties uz pirmā PVN summu.</span><span class="sxs-lookup"><span data-stu-id="a6bef-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="a6bef-132">Paraugs</span><span class="sxs-lookup"><span data-stu-id="a6bef-132">Example</span></span>

<span data-ttu-id="a6bef-133">Tiek izmantoti tālāk norādītie PVN kodi.</span><span class="sxs-lookup"><span data-stu-id="a6bef-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="a6bef-134">1. NODOKLIS = 10%, izmantojot metodi Procenti no neto summas</span><span class="sxs-lookup"><span data-stu-id="a6bef-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="a6bef-135">2. NODOKLIS = 20%, izmantojot metodi PVN %, ja lauka PVN uz PVN vērtība ir 1. nodoklis</span><span class="sxs-lookup"><span data-stu-id="a6bef-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="a6bef-136">PVN = 25%, izmantojot metodi Procenti no bruto summas</span><span class="sxs-lookup"><span data-stu-id="a6bef-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="a6bef-137">Neto summa: 10,00 1. NODOKLIS: 10,00 x 10% = 1,00 2. NODOKLIS: 1,00 x 20% = 0,20 Bruto summa: 10,00 + 1,00 + 0,20 = 11,20 PVN: 11,20 x 25% = 2,80 NODOKĻI un PVN kopā: 1,00+ 0,20 + 2,80 = 4,00 Kopsumma: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="a6bef-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="a6bef-138">**Piezīme.**</span><span class="sxs-lookup"><span data-stu-id="a6bef-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bef-139">Nevar veikt daudzlīmeņu nodokļa aprēķinu, pamatojoties uz nodokli.</span><span class="sxs-lookup"><span data-stu-id="a6bef-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="a6bef-140">Nevar aprēķināt nodokli, pamatojoties uz nodokli, kas jau ir aprēķināts, pamatojoties uz citu nodokli.</span><span class="sxs-lookup"><span data-stu-id="a6bef-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="a6bef-141">Transakcijai var veikt vairākus vienlīmeņa nodokļa koda aprēķinus, pamatojoties uz nodokli.</span><span class="sxs-lookup"><span data-stu-id="a6bef-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="a6bef-142"> Summa uz vienu vienību</span><span class="sxs-lookup"><span data-stu-id="a6bef-142">Amount per unit</span></span>
<span data-ttu-id="a6bef-143">Ja atlasāt lauka Izcelsme vērtību Sumam uz vienu vienību, PVN tiek aprēķināts kā fiksēta summa uz vienību, kas tiek reizināta ar dokumenta rindā ievadīto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="a6bef-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="a6bef-144">Laukā Vienība ir jāatlasa vienība.</span><span class="sxs-lookup"><span data-stu-id="a6bef-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="a6bef-145">Summa uz vienu vienību tiek norādīta lapā PVN koda vērtības.</span><span class="sxs-lookup"><span data-stu-id="a6bef-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="a6bef-146">Paraugs</span><span class="sxs-lookup"><span data-stu-id="a6bef-146">Example</span></span>

<span data-ttu-id="a6bef-147">PVN kods ir iestatīts kā: USD 1,20 uz vienu vienību = kasti Pārdošanas rēķina rindā ir reģistrēta 25 krājuma kastu pārdošana PVN ir aprēķināts kā: 25 x1,20 =30,00</span><span class="sxs-lookup"><span data-stu-id="a6bef-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="a6bef-148">**Piezīme.**</span><span class="sxs-lookup"><span data-stu-id="a6bef-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6bef-149">Ja transakcija ir ievadīta, izmantojot citu vienību, nevis PVN kodam norādīto vienību, tā tiek automātiski konvertēta, pamatojoties uz vienību konvertācijām, kas ir iestatītas lapā Mērvienību pārveidošana.</span><span class="sxs-lookup"><span data-stu-id="a6bef-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="a6bef-150"> Summa uz vienību, papildu opcija</span><span class="sxs-lookup"><span data-stu-id="a6bef-150">Amount per unit, additional option</span></span>

<span data-ttu-id="a6bef-151">Cilnē Aprēķins varat atlasīt, vai kā summa uz vienību aprēķinātais nodoklis tiek aprēķināts un pieskaitīts neto pirms citiem nodokļu kodiem un tiek pieskaitīts neto summai, pirms tiek aprēķināti citi nodokļu kodi, kuriem ir atlasīta lauka Izcelsme vērtība Procenti no neto summas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="a6bef-152">Piemēri</span><span class="sxs-lookup"><span data-stu-id="a6bef-152">Examples</span></span>

<span data-ttu-id="a6bef-153">Pieņemsim, ka transakcijai tiek aprēķināti 2 nodokļu kodi.</span><span class="sxs-lookup"><span data-stu-id="a6bef-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="a6bef-154">NODOKLIS: lauka Izcelsme vērtība ir Summa uz vienu vienību un PVN, iestatītā vērtība ir 5,00 uz vienu vienību = gab.</span><span class="sxs-lookup"><span data-stu-id="a6bef-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="a6bef-155">PVN: lauka Izcelsme vērtība ir tāda, kā ir norādīts iepriekš sniegtajos piemēros, iestatītā vērtība ir 25%</span><span class="sxs-lookup"><span data-stu-id="a6bef-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="a6bef-156">Tiek pārdots 1 gab. krājuma par vienības cenu 10,00</span><span class="sxs-lookup"><span data-stu-id="a6bef-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="a6bef-157">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="a6bef-157">Example 1</span></span>

<span data-ttu-id="a6bef-158">PVN: lauka Izcelsme vērtība ir Procenti no bruto summas Opcija Aprēķināts pirms PVN aprēķināšanas neko neietekmē, jo PVN tiek aprēķināts kā procenti no bruto summas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="a6bef-159">NODOKLIS: 1 x 5,00 = 5,00 Bruto summa: 10,00 + 5,00 = 15,00 PVN: 15,00 x 25% = 3,75 PVN kopā: 5,00 + 3,75 = 8,75 Kopsumma: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="a6bef-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="a6bef-160">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="a6bef-160">Example 2</span></span>

<span data-ttu-id="a6bef-161">PVN: lauka Izcelsme vērtība ir Procenti no neto summas NODOKĻA aprēķinam nav atlasīta opcija Aprēķināts pirms PVN aprēķināšanas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="a6bef-162">Neto summa: 10,00 NODOKLIS: 1 x 5,00 = 5,00 PVN: 10,00 x 25% = 2,50 PVN kopā: 5,00 + 2,50 = 7,50 Kopsumma: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="a6bef-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="a6bef-163">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="a6bef-163">Example 3</span></span>

<span data-ttu-id="a6bef-164">PVN: lauka Izcelsme vērtība ir Procenti no neto summas NODOKĻA aprēķinam ir atlasīta opcija Aprēķināts pirms PVN aprēķināšanas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="a6bef-165">Neto summa: 10,00 NODOKLIS: 1 x 5,00 = 5,00 PVN: (10,00 + 5,00) x 25% = 3,75 PVN kopā: 5,00 + 3,75 = 8,75 Kopsumma: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="a6bef-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="a6bef-166">4. piemērs</span><span class="sxs-lookup"><span data-stu-id="a6bef-166">Example 4</span></span>

<span data-ttu-id="a6bef-167">3. un 1. piemēra rezultāti ir vienādi, jo ir tikai viens nodoklis.</span><span class="sxs-lookup"><span data-stu-id="a6bef-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="a6bef-168">Pieņemsim, ka jums ir divi NODOKĻI un tikai viens no tiem ir iekļauts neto summā PVN aprēķinam. 1. NODOKLIS: 5,00, izmantojot metodi Summa uz vienu vienību un opciju Aprēķināts pirms PVN aprēķināšanas 2. NODOKLIS: 2,50, izmantojot metodi Summa uz vienu vienību un neizmantojot opciju Aprēķināts pirms PVN aprēķināšanas PVN: 25%, izmantojot metodi Procenti no neto summas Neto summa: 10,00 1. NODOKLIS: 1 x 5,00 = 5,00 2. NODOKLIS: 1 x 2,50 = 2,50 Ar PVN apliekamā neto summa: 10,00 + 5,00 = 15,00 PVN: 15,00 x 25% = 3,75 PVN kopā, ieskaitot nodokļus: 5,00 + 2,50 + 3,75 = 11,25 Kopsumma: 10,00 + 11,25 = 21,25 25% PVN tiek aprēķināts summai, ko veido neto summa (10,00) + 1. NODOKLIS (5,00) = 15,00.</span><span class="sxs-lookup"><span data-stu-id="a6bef-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="a6bef-169">2. NODOKLIS tiek pieskaitīts nodokļu summai pēc PVN aprēķināšanas.</span><span class="sxs-lookup"><span data-stu-id="a6bef-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="a6bef-170"> Neto summai aprēķinātie procenti</span><span class="sxs-lookup"><span data-stu-id="a6bef-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="a6bef-171">Izmantojot metodi Neto summai aprēķinātie procenti, nodokļu aprēķins tiek veikts atšķirīgi atkarībā no dokumenta vai žurnāla parametra Summas ietver PVN iestatījuma.</span><span class="sxs-lookup"><span data-stu-id="a6bef-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="a6bef-172">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="a6bef-172">Example 1</span></span>

<span data-ttu-id="a6bef-173">Dokumentam/žurnālam ir iestatīta parametra Summas ietver PVN vērtība Jā Transakcijas rindas summa: 10,00 Nodokļa likme: 25% PVN: transakcijas rindas summa x nodokļa likme (10,00 x 25%) = 2,50 Nodokļa pamatsumma (sākotnējā summa): transakcijas rindas summa – PVN (10,00 – 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="a6bef-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="a6bef-174">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="a6bef-174">Example 2</span></span>

<span data-ttu-id="a6bef-175">Dokumentam/žurnālam ir iestatīta parametra Summas ietver PVN vērtība Nē Transakcijas rindas summa: 10,00 Nodokļa likme: 25% PVN: (transakcijas rindas summa x nodokļa likme)/(100 – nodokļa likme) ((10,00 x 25%)/(100% – 25%)) = 3,33 Nodokļa pamatsumma (sākotnējā summa): transakcijas rindas summa = 10,00</span><span class="sxs-lookup"><span data-stu-id="a6bef-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="a6bef-176">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a6bef-176">Additional resources</span></span>
--------

[<span data-ttu-id="a6bef-177">PVN likmes noteikšana atkarībā no laukiem Aprēķina pamatā un Aprēķina metode</span><span class="sxs-lookup"><span data-stu-id="a6bef-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="a6bef-178">PVN kodu visas summas un intervāla aprēķināšanas opcijas</span><span class="sxs-lookup"><span data-stu-id="a6bef-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)




