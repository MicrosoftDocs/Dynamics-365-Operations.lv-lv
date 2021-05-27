---
title: Aprēķināt TDS rēķinos, izmantojot žurnālus
description: Šajā tēmā ir uzskaitīti soļi, lai aprēķinātu No kopējo ienākumu summas atskaitīto nodokli (TDS) žurnālos.
author: kailiang
ms.date: 02/12/2021
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023432"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="e1308-103">Aprēķināt TDS rēķinos, izmantojot žurnālus</span><span class="sxs-lookup"><span data-stu-id="e1308-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1308-104">Šajā tēmā ir uzskaitīti soļi, lai aprēķinātu No kopējo ienākumu summas atskaitīto nodokli (TDS) žurnālos.</span><span class="sxs-lookup"><span data-stu-id="e1308-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="e1308-105">Sāciet, atverot **Virsgrāmatas žurnāla** lapu (**Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli**).</span><span class="sxs-lookup"><span data-stu-id="e1308-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="e1308-106">[![Virsgrāmatas žurnāli](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="e1308-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="e1308-107">Izveidojiet žurnāla rindas, izmantojot tabulā uzskaitītās žurnāla formas.</span><span class="sxs-lookup"><span data-stu-id="e1308-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="e1308-108">Atlasiet konta tipu un korespondējošā konta tipu un ievadiet darījuma summu.</span><span class="sxs-lookup"><span data-stu-id="e1308-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="e1308-109">Lapā **Rēķinu apstiprināšanas žurnāls** atlasiet **Meklēt dokumentus** un atlasiet rēķinus, kuros aprēķināt TDS.</span><span class="sxs-lookup"><span data-stu-id="e1308-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="e1308-110">Apskatiet rēķinus, kas izveidoti **Rēķinu reģistra** lapā vai **Meklēt dokumentus** lapā.</span><span class="sxs-lookup"><span data-stu-id="e1308-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="e1308-111">Lapas **Žurnālu dokuments** cilnē **Vispārīgi** skatiet vai modificējiet noklusējuma TDS grupu, kas noteikta kreditoram vai debitoram laukā **TDS grupa**.</span><span class="sxs-lookup"><span data-stu-id="e1308-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="e1308-112">TDS summa, kas tiek aprēķināta žurnāla rindās, ir balstīta uz formulu, kas definēta TDS nodokļu kodiem, kas uzskaitīti **TDS grupas** laukā.</span><span class="sxs-lookup"><span data-stu-id="e1308-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="e1308-113">Lauks **Ieturētā nodokļu grupa**  un lauks **TCS grupa** kļūst pieejams, ja atlasāt TDS grupu laukā **TDS grupa**.</span><span class="sxs-lookup"><span data-stu-id="e1308-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="e1308-114">**Ieturēto nodokļu grupas** lauks ir pieejams tikai **Virsgrāmatas žurnāla** lapā.</span><span class="sxs-lookup"><span data-stu-id="e1308-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="e1308-115">TDS tiek aprēķināts tikai tad, ja izvēles rūtiņa **Aprēķināt ieturēto nodokli** ir atzīmēta kreditoram vai debitoram lapās **Visi kreditori** vai **Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="e1308-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="e1308-116">Atlasiet cilni **Informācija par nodokļiem**. Ja nepieciešams, atlasiet uzņēmuma alternatīvās adreses, kas šajā laukā iestatītas uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="e1308-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="e1308-117">Uzņēmuma nosaukumu varat skatīt laukā **Nosaukums**, kas atrodas lauku grupā **Uzņēmuma informācija**.</span><span class="sxs-lookup"><span data-stu-id="e1308-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="e1308-118">Skatiet kreditora vai debitora ar nodokli saņēmēja kategorijas būtību laukā **Vērtētāja raksturs**, kas atrodas zem lauka grupas **Ieturētais nodoklis**.</span><span class="sxs-lookup"><span data-stu-id="e1308-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="e1308-119">Laukā **Nodokļu konta numurs** (**TAN**) skatiet atlasītā uzņēmuma parādītais nosaukuma TAN.</span><span class="sxs-lookup"><span data-stu-id="e1308-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="e1308-120">Atlasiet **Ieturēto nodokli** **Ieturētā nodokļa** izvēlnē, lai atvērtu lapu **Ieturētā nodokļa pagaidu darījumi**.</span><span class="sxs-lookup"><span data-stu-id="e1308-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="e1308-121">Šie lauki tiek parādīti lapas **Ieturētā nodokļa pagaidu darījumi** augšējā rūtī.</span><span class="sxs-lookup"><span data-stu-id="e1308-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="e1308-122">**Ieturētā nodokļa kopsumma** - TDS kopsumma, kas aprēķināta darījumam TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="e1308-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="e1308-123">**Vērtība** - kopējā procentuālā vērtība, kas tika izmantota darījuma TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="e1308-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="e1308-124">Kopējā procentuālā vērtība ir balstīta uz formulu, kas noteikta TDS nodokļu kodiem un pievienota TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="e1308-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="e1308-125">**Koriģētā ieturētā nodokļa kopsumma** - kopējā koriģētā TDS summa visiem nodokļu kodiem TDS grupā.</span><span class="sxs-lookup"><span data-stu-id="e1308-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="e1308-126">**TDS** – ja atlasīts, TDS grupa tiek pievienota darījumam.</span><span class="sxs-lookup"><span data-stu-id="e1308-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="e1308-127">Lauki cilnēs **Pārskats**, **Vispārīgi** un **Korekcija** lapā **Pagaidu ieturētā nodokļa darījumi** parāda aprēķināto TDS summu un pielāgoto TDS summas informāciju par katru TDS nodokļa kodu, kas pievienots TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="e1308-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="e1308-128">Atlasiet **Slieksnis**, lai atvērtu lapu **Slieksnis**.</span><span class="sxs-lookup"><span data-stu-id="e1308-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="e1308-129">Skatiet sliekšņa ierobežojumu un izņēmuma sliekšņa ierobežojumu, kas definēts TDS nodokļa komponentam, kurš pievienots konkrētam TDS nodokļa kodam šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="e1308-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="e1308-130">Atlasiet **Formulas veidotāju**, lai atvērtu **Formulas veidotāja** formu.</span><span class="sxs-lookup"><span data-stu-id="e1308-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="e1308-131">Skatiet šajā lapā specifisku TDS nodokļa kodu definēto formulu.</span><span class="sxs-lookup"><span data-stu-id="e1308-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="e1308-132">Aizveriet lapas **Formulas veidotājs** un **Pagaidu ieturētā nodokļa darījumi**, lai atgrieztos **Žurnāla dokumentu** lapā.</span><span class="sxs-lookup"><span data-stu-id="e1308-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="e1308-133">Ievadiet pārējo nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="e1308-133">Enter the other required details.</span></span> <span data-ttu-id="e1308-134">Apstipriniet un grāmatojiet šo žurnālu.</span><span class="sxs-lookup"><span data-stu-id="e1308-134">Validate and post the journal.</span></span> <span data-ttu-id="e1308-135">TDS summa, kas ir aprēķināta pirkšanas rēķiniem, tiek grāmatota kreditora kontā.</span><span class="sxs-lookup"><span data-stu-id="e1308-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="e1308-136">TDS summa, kas tiek aprēķināta pārdošanas rēķinos, tiek grāmatota debitoru kontā, kas katrai TDS nodokļu kodam ir definēts TDS grupā.</span><span class="sxs-lookup"><span data-stu-id="e1308-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="e1308-137">TDS nodokļu kodu kreditoru vai debitoru konti ir definēti **Ieturētā nodokļa kodu** lapā.</span><span class="sxs-lookup"><span data-stu-id="e1308-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="e1308-138">Atlasiet **Grāmatoto ieturēto nodokli**, lai atvērtu **Ieturētā** **nodokļa** **darījumu** lapu.</span><span class="sxs-lookup"><span data-stu-id="e1308-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="e1308-139">Laukā **Vērtība** tiek parādīta kopējā procentuālā vērtība, kas tiek izmantota darījuma TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="e1308-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="e1308-140">Lauki cilnēs **Pārskats**, **Vispārīgi** un **Summa** ieturētā nodokļa darījuma lapā parāda aprēķināto TDS summu un pielāgoto TDS summas informāciju par katru TDS nodokļa kodu, kas pievienots TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="e1308-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
