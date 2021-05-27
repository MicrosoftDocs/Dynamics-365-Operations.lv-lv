---
title: Segt TDS maksājumus TDS iestādes kreditoriem un izveidot TDS challan
description: Šajā tēmā skaidrots, kā nomaksāt No kopējo ienākumu summas atskaitīto nodokļa (TDS) maksājumus TDS iestādes kreditoriem.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023425"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="26330-103">Segt TDS maksājumus TDS iestādes kreditoriem un izveidot TDS challan</span><span class="sxs-lookup"><span data-stu-id="26330-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26330-104">Šajā tēmā skaidrots, kā nomaksāt No kopējo ienākumu summas atskaitīto nodokļa (TDS) maksājumus TDS iestādes kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="26330-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="26330-105">Dodieties uz **Kreditori \> Maksājumi \> Kreditora maksājumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="26330-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="26330-106">[![Kreditora maksājumu žurnāla rinda](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="26330-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="26330-107">Lapā **Kreditoru maksājumu žurnāls** izvēlieties **Jauns**, lai izveidotu žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="26330-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="26330-108">Laukā **Konts** atlasiet TDS iestādes kreditoru, kuram veikt TDS maksājumus.</span><span class="sxs-lookup"><span data-stu-id="26330-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="26330-109">Atlasiet **Norēķinu darījumi**, lai atvērtu lapu **Norēķinu darījumi**, kur jūs variet skatīt nosegtos TDS darījumus TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="26330-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="26330-110">Norēķinu perioda laikā norēķinātie TDS darījumi tiek parādīti šādi:</span><span class="sxs-lookup"><span data-stu-id="26330-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="26330-111">TDS darījumi, kuros vērtētāja rakstura kategorija ir **Uzņēmums**, tiek parādīti kā viena darījumu rinda.</span><span class="sxs-lookup"><span data-stu-id="26330-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="26330-112">TDS darījumi, kur vērtētāja rakstura kategorija ir **HUF**, **Firma**, **Individuāls**, **AOP**, **BOI**, **Vietējā pašvaldība** vai **Citi**, tiek rādītas kā viena darījuma rinda.</span><span class="sxs-lookup"><span data-stu-id="26330-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="26330-113">Laukā **Summa** ir norādīta kopējā TDS summa, kas jāsamaksā TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="26330-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="26330-114">Atlasiet **Ieturētā nodokļa darījumi**, lai apskatītu dažādus TDS darījumus, kas ir iekļautas norēķinu ierakstam.</span><span class="sxs-lookup"><span data-stu-id="26330-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="26330-115">Varat apskatīt katras TDS darījumu sadalījumu, kas šajā lapā ir iekļauts apmaksas perioda norēķinu procesā.</span><span class="sxs-lookup"><span data-stu-id="26330-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="26330-116">Cilnē **Pārskats** atzīmējiet izvēles rūtiņu **Atzīmēt** TDS darījumiem, lai norēķinātos ar TDS iestādes kreditoru.</span><span class="sxs-lookup"><span data-stu-id="26330-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="26330-117">Cilne **Pārskats** parāda šādu informāciju par katru atvērto TDS darījumu:</span><span class="sxs-lookup"><span data-stu-id="26330-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="26330-118">**Datums** – pievienojiet TDS darījuma datumu.</span><span class="sxs-lookup"><span data-stu-id="26330-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="26330-119">**Dokuments** - virsgrāmatas dokumenta numurs.</span><span class="sxs-lookup"><span data-stu-id="26330-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="26330-120">**Avots** - modulis, kurā TDS darījums tiek ievietots.</span><span class="sxs-lookup"><span data-stu-id="26330-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="26330-121">**Kreditors/debitors** - kreditora vai debitora konta numurs, no kura TDS tiek atskaitīts.</span><span class="sxs-lookup"><span data-stu-id="26330-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="26330-122">**Ieturēšanas saņēmēja/puses nosaukums** – kreditora vai debitora nosaukums, no kura TDS tiek atskaitīts.</span><span class="sxs-lookup"><span data-stu-id="26330-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="26330-123">**Vērtētāja raksturs** – vērtētāja rakstura kategorija, kam pieder atskaitāmais.</span><span class="sxs-lookup"><span data-stu-id="26330-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="26330-124">**Summa** – rēķina summa, pēc kuras tika aprēķināta TDS.</span><span class="sxs-lookup"><span data-stu-id="26330-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="26330-125">**Nodokļu summa** – TDS summa, kas tika aprēķināta darījumam.</span><span class="sxs-lookup"><span data-stu-id="26330-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="26330-126">Notīriet izvēles rūtiņu **Atzīmēt** visiem TDS darījumiem, kas nav jānosedz TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="26330-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="26330-127">Cilnē **Vispārīgi** lauks **PAN** parāda atskaitāmā saņēmēja pastāvīgo konta numuru (PAN).</span><span class="sxs-lookup"><span data-stu-id="26330-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="26330-128">Lauks **Datums** parāda TDS aprēķina datumu, un lauks **Vērtība** rāda kopējo procentu likmi, kas tika izmantota TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="26330-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="26330-129">Atlasiet **Dokuments**, lai apskatītu dokumentu ierakstus TDS darījumam.</span><span class="sxs-lookup"><span data-stu-id="26330-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="26330-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="26330-130">Close the page.</span></span>
10. <span data-ttu-id="26330-131">Atlasiet **Ieturētā nodokļa komponentus**, lai atvērtu lapu **Ieturētā nodokļa komponenti**, kur varat skatīt TDS, kas tika aprēķināti uz TDS nodokļa komponentu noteiktam TDS nodokļa kodam.</span><span class="sxs-lookup"><span data-stu-id="26330-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="26330-132">Cilnē **Pārskats** lauks **Nodokļu komponents** rāda TDS nodokļa sastāvdaļu, kas tika izmantota darījumam.</span><span class="sxs-lookup"><span data-stu-id="26330-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="26330-133">Lauks **Summa** rāda TDS summu, kas tika aprēķināta TDS nodokļa komponentam pamatvalūtā.</span><span class="sxs-lookup"><span data-stu-id="26330-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="26330-134">Lauks **Uzkrātā summa** parāda kopējo TDS summu, kas tika aprēķināta TDS nodokļa komponentam visiem nosegtajiem darījumiem.</span><span class="sxs-lookup"><span data-stu-id="26330-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="26330-135">Cilnē **Summa** sadaļa **Noklusētā valūta** rāda TDS summu, kas tika aprēķināta TDS nodokļa komponentam noklusētajā valūtā.</span><span class="sxs-lookup"><span data-stu-id="26330-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="26330-136">Sadaļa **Sekundārā valūta** parāda summu sekundārajā valūtā.</span><span class="sxs-lookup"><span data-stu-id="26330-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="26330-137">Aizveriet lapu **Ieturētā nodokļa komponenti**.</span><span class="sxs-lookup"><span data-stu-id="26330-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="26330-138">Lapā **Atvērt darījumu rediģēšanu**, laukā **Summa** ievērojiet, ka ir atjaunināta kopējā norēķinu perioda summa, kas jāsedz TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="26330-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="26330-139">Lai nokārtotu dažādu TDS norēķinu periodu darījumus ar TDS iestādes kreditoru, atzīmējiet izvēles rūtiņu **Atzīmēt** darījumiem.</span><span class="sxs-lookup"><span data-stu-id="26330-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="26330-140">Aizveriet lapu **Atvērt darījumu rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="26330-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="26330-141">Ja norēķinam lapā **Ieturētā nodokļa darījumi** ir atlasīti tikai daži darījumi, atlasīto darījumu kopējā TDS summa tiek atjaunināta laukā **Labošana**, lapā **Atvērt darījumu rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="26330-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="26330-142">Labojuma summa tiek atjaunināta žurnāla rindā **Žurnāla dokumenta** lapā, un lapa **Atvērt darījumu rediģēšanu** tiek aizvērta.</span><span class="sxs-lookup"><span data-stu-id="26330-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="26330-143">Lapā **Žurnāla dokuments** lauks **Debets** parāda kopējo summu, kas jāapmaksā TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="26330-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="26330-144">Ievadiet detalizētu informāciju par korespondējošo kontu.</span><span class="sxs-lookup"><span data-stu-id="26330-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="26330-145">Ja TDS darījumiem ir atšķirīgas nodokļa kontu numuri (TAN), žurnāla rindas tiek izveidotas pēc TAN lapā **Žurnāla dokuments**.</span><span class="sxs-lookup"><span data-stu-id="26330-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="26330-146">Cilnē **Papildmaksas**, laukā **Maksas ID** field, atlasiet maksas ID, kura maksas tips ir **Procenti** vai **Citi**, lai iekasētu papildmaksu par aizkavētiem maksājumiem, kas veikti TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="26330-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="26330-147">Cilnes **Informācija par nodokļiem** sadaļā **Uzņēmuma informācija** lauks **Nosaukums** parāda uzņēmuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="26330-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="26330-148">**Ieturētā nodokļa** sadaļā lauks **Nodokļu konta numurs (TAN)** rāda TAN, kas ir piesaistīts darījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="26330-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="26330-149">Apstipriniet un grāmatojiet šo žurnālu.</span><span class="sxs-lookup"><span data-stu-id="26330-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="26330-150">Atlasiet **Ieturētais nodoklis \> Challan informācija**, lai ievadītu detalizētu informāciju par darījumu.</span><span class="sxs-lookup"><span data-stu-id="26330-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="26330-151">**Dokuments** – lauks parāda darījuma dokumenta numuru.</span><span class="sxs-lookup"><span data-stu-id="26330-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="26330-152">Atzīmējiet izvēles rūtiņu **TDS, kas deponēti ar grāmatas ierakstu**, ja TDS summa ir deponēta, izmantojot grāmatas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="26330-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="26330-153">Laukā **Challan numurs** ievadiet challan numuru, kas tiek izmantots, lai veiktu maksājumu TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="26330-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="26330-154">Laukā **Datums** ievadiet challan datumu.</span><span class="sxs-lookup"><span data-stu-id="26330-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="26330-155">Laukā **Bankas nosaukums** atlasiet tās bankas nosaukumu, kurai ir jāiemaksā TDS summa, kas jāmaksā TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="26330-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="26330-156">Šajā laukā ir uzskaitīti visi bankas konti, kas tika iestatīti TDS iestādes kreditoram, sadaļā **Kreditori \> Visi kreditori \> Iestatīt \> Bankas konti**.</span><span class="sxs-lookup"><span data-stu-id="26330-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="26330-157">Laukā **BSR kods** ievadiet bankas Pamata statistiskās atgriešanas (BSR) kodu.</span><span class="sxs-lookup"><span data-stu-id="26330-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="26330-158">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="26330-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="26330-159">Paraugs</span><span class="sxs-lookup"><span data-stu-id="26330-159">Example</span></span>

<span data-ttu-id="26330-160">Periods 01/04/2009 tiek nosegts ar **Nomas** TDS komponentu grupu, izmantojot periodisko TDS norēķinu procesu.</span><span class="sxs-lookup"><span data-stu-id="26330-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="26330-161">Kopējā TDS 141 625,00 summa tiek grāmatota TDS kreditora iestādes kontā TDS norēķinu periodam.</span><span class="sxs-lookup"><span data-stu-id="26330-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="26330-162">Šo summu var skatīt laukā **Summa**, lapā **Atvērt darījumu rediģēšanu** TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="26330-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="26330-163">Ja jūs izvēlieties **Ieturētā nodokļa darījumi**, lai aplūkotu dažādus TDS darījumus, kas tika nosegti konkrētam periodam, tiek parādīta šāda informācija.</span><span class="sxs-lookup"><span data-stu-id="26330-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="26330-164">TDS summa</span><span class="sxs-lookup"><span data-stu-id="26330-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="26330-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="26330-165">16,995.00</span></span>  |
| <span data-ttu-id="26330-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="26330-166">22,660.00</span></span>  |
| <span data-ttu-id="26330-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="26330-167">28,325.00</span></span>  |
| <span data-ttu-id="26330-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="26330-168">16,995.00</span></span>  |
| <span data-ttu-id="26330-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="26330-169">28,325.00</span></span>  |
| <span data-ttu-id="26330-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="26330-170">16,995.00</span></span>  |
| <span data-ttu-id="26330-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="26330-171">11,330.00</span></span>  |

<span data-ttu-id="26330-172">Konkrētai TDS summai, varat atlasīt **Ieturētā nodokļa komponentus**, lai skatītu TDS, kas tika aprēķināti uz TDS nodokļa komponentu noteiktam TDS nodokļa kodam.</span><span class="sxs-lookup"><span data-stu-id="26330-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="26330-173">Šajā piemērā jūs atlasāt **Ieturētā nodokļa komponentus** TDS summai 16 995,00.</span><span class="sxs-lookup"><span data-stu-id="26330-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="26330-174">Tiek parādīta nodokļa summa, kas aprēķināta katram darījuma komponentam.</span><span class="sxs-lookup"><span data-stu-id="26330-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="26330-175">Nodokļa komponents</span><span class="sxs-lookup"><span data-stu-id="26330-175">Tax component</span></span> | <span data-ttu-id="26330-176">Apjoms</span><span class="sxs-lookup"><span data-stu-id="26330-176">Amount</span></span>    | <span data-ttu-id="26330-177">Akumulētā summa</span><span class="sxs-lookup"><span data-stu-id="26330-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="26330-178">TDS</span><span class="sxs-lookup"><span data-stu-id="26330-178">TDS</span></span>           | <span data-ttu-id="26330-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="26330-179">1,5000.00</span></span> | <span data-ttu-id="26330-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="26330-180">125,000.00</span></span>         |
| <span data-ttu-id="26330-181">Piemaksa</span><span class="sxs-lookup"><span data-stu-id="26330-181">Surcharge</span></span>     | <span data-ttu-id="26330-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="26330-182">1,500.00</span></span>  | <span data-ttu-id="26330-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="26330-183">12,500.00</span></span>          |
| <span data-ttu-id="26330-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="26330-184">PE-Cess</span></span>       | <span data-ttu-id="26330-185">330.00</span><span class="sxs-lookup"><span data-stu-id="26330-185">330.00</span></span>    | <span data-ttu-id="26330-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="26330-186">2,750.00</span></span>           |
| <span data-ttu-id="26330-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="26330-187">SHE Cess</span></span>      | <span data-ttu-id="26330-188">165.00</span><span class="sxs-lookup"><span data-stu-id="26330-188">165.00</span></span>    | <span data-ttu-id="26330-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="26330-189">1,375.00</span></span>           |

<span data-ttu-id="26330-190">Ja jūs atlasījāt tikai TDS summas 16 995,00, 22 660,00 un 28 325,00 norēķiniem lapā **Ieturētā nodokļa darījumi** page, kopējā norēķinu summa tiek parādīta kā **67 980,00** laukā **Labošana**, lapā **Atvērt darījumu rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="26330-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="26330-191">Ja šis darījums ir atzīmēts norēķinam, un lapa **Atvērt darījumu rediģēšanu** ir aizvērta, summa **67 980,00** tiek parādīta laukā **Debets**, lapā **Žurnāla dokuments**.</span><span class="sxs-lookup"><span data-stu-id="26330-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="26330-192">Tagad varat grāmatot žurnālu un ģenerēt TDS challan maksājumu.</span><span class="sxs-lookup"><span data-stu-id="26330-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="26330-193">Avansa maksājumu korekcija, kas tiek veikta TDS iestāžu kreditoriem</span><span class="sxs-lookup"><span data-stu-id="26330-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="26330-194">Lai pielāgotu avansa maksājumu, kas veikts TDS iestādes kreditoram par faktisko maksājumu, dodieties uz sadaļu **Kreditori \> Kreditori \> Visi kreditori \> Darījumu rediģēšana**.</span><span class="sxs-lookup"><span data-stu-id="26330-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="26330-195">Ja faktiskais maksājums, kas ir veikts, pārsniedz avansa maksājumu, darījumam tiek ģenerēti divi challan maksājumu numuri.</span><span class="sxs-lookup"><span data-stu-id="26330-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="26330-196">Tomēr TDS vaicājumā tiek parādīts tikai pirmais challan maksājumu numurs.</span><span class="sxs-lookup"><span data-stu-id="26330-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
