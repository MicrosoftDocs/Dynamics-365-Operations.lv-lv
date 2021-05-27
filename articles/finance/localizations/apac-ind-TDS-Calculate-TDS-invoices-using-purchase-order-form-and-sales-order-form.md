---
title: Aprēķināt TDS rēķinus, izmantojot pirkšanas pasūtījuma formu un pārdošanas pasūtījuma formu
description: Šajā tēmā ir uzskaitīti soļi, lai aprēķinātu Ieturēto nodokli avotā (TDS) dažādu veidu rēķinos.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023408"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="b46f1-103">Aprēķināt TDS rēķinus, izmantojot pirkšanas pasūtījuma formu un pārdošanas pasūtījuma formu</span><span class="sxs-lookup"><span data-stu-id="b46f1-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b46f1-104">Šajā tēmā ir uzskaitīti soļi ieturētā nodokļa aprēķināšanai avotā (TDS) dažādiem rēķinu tipiem, izmantojot **Pirkšanas pasūtījumu**, **Pirkšanas žurnālu**, **Virspasūtījumu** un **Pārdošanas pasūtījumu** lapas.</span><span class="sxs-lookup"><span data-stu-id="b46f1-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="b46f1-105">Veidojiet pirkšanas pasūtījumu, pirkšanas žurnālu, virspasūtījumu vai pārdošanas pasūtījumu, izmantojot norādīto lapu.</span><span class="sxs-lookup"><span data-stu-id="b46f1-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="b46f1-106">Ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="b46f1-106">Enter the required details.</span></span>

2. <span data-ttu-id="b46f1-107">Atlasiet cilni **Iestatīšana**, lai skatītu kreditora vai debitora vērtētāja raksturu.</span><span class="sxs-lookup"><span data-stu-id="b46f1-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="b46f1-108">Šī informācija ir uzskaitīta laukā **Vērtētāja raksturu** lauka grupā **Ieturēto nodokļu grupa**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="b46f1-109">**TDS grupas** laukā skatiet vai modificējiet noklusējuma TDS grupu, kas noteikta kreditoram vai debitoram.</span><span class="sxs-lookup"><span data-stu-id="b46f1-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="b46f1-110">**TCS grupas** lauks nav pieejams, ja atlasāt TDS grupu laukā **TDS grupa**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="b46f1-111">TDS tiek aprēķināts tikai tad, ja izvēles rūtiņa **Aprēķināt ieturēto nodokli** ir atzīmēta kreditoram vai debitoram lapā **Visi kreditori** vai **Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="b46f1-112">Cilnē **Rindas** izveidojiet krājuma rindas un ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="b46f1-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="b46f1-113">Atlasiet cilni **Iestatījumi** (rindas līmenis), lai apskatītu vai mainītu TDS grupu, kas definēta virsraksta līmenī.</span><span class="sxs-lookup"><span data-stu-id="b46f1-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="b46f1-114">TDS grupa tiek rādīta laukā **TDS grupa**, kas atrodas **Ieturēto nodokļu grupas** lauku grupā.</span><span class="sxs-lookup"><span data-stu-id="b46f1-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="b46f1-115">Atlasiet cilni **Informācija par nodokļiem** un atlasiet alternatīvās adreses, kas ir iestatīti uzņēmuma nosaukumam, kas tiek parādīts šajā laukā.</span><span class="sxs-lookup"><span data-stu-id="b46f1-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="b46f1-116">Uzņēmuma nosaukums ir parādīts laukā **Nosaukums**, kas atrodas lauku grupā **Uzņēmuma informācija**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="b46f1-117">Atlasītā uzņēmuma nosaukuma TAN tiek parādīts laukā **Nodokļu konta numurs** (**TAN**) lauku grupā **Ieturētais nodoklis**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="b46f1-118">Atlasiet **Ieturētais nodokli**, lai atvērtu **Pagaidu ieturētā nodokļa darījumu** lapu.</span><span class="sxs-lookup"><span data-stu-id="b46f1-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="b46f1-119">Skatīt sekojošos laukus augšējā rūtī lapā **Ieturētā nodokļa pagaidu darījumi**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="b46f1-120">**Ieturētā** **nodokļa** **kopsumma** - TDS kopsumma, kas aprēķināta darījumam TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="b46f1-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="b46f1-121">**Vērtība** - kopējā procentuālā vērtība, kas tika izmantota darījuma TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="b46f1-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="b46f1-122">Kopējā procentuālā vērtība ir balstīta uz formulu, kas noteikta TDS nodokļu kodiem un pievienota TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="b46f1-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="b46f1-123">**Koriģētā ieturētā nodokļa kopsumma** - kopējā koriģētā TDS summa visiem nodokļu kodiem TDS grupā.</span><span class="sxs-lookup"><span data-stu-id="b46f1-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="b46f1-124">**TDS** – ja atlasīts, TDS grupa tiek pievienota darījumam.</span><span class="sxs-lookup"><span data-stu-id="b46f1-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="b46f1-125">Lauki cilnēs **Pārskats**, **Vispārīgi** un **Korekcija** lapā **Pagaidu ieturētā nodokļa darījumi** parāda aprēķināto TDS summu un pielāgoto TDS summas informāciju par katru TDS nodokļa kodu, kas pievienots TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="b46f1-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="b46f1-126">Atlasiet **Slieksnis**, lai atvērtu lapu **Slieksnis**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="b46f1-127">Skatiet sliekšņa ierobežojumu, kas definēts TDS nodokļa komponentam, kurš pievienots konkrētam TDS nodokļa kodam šajā lapā.</span><span class="sxs-lookup"><span data-stu-id="b46f1-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="b46f1-128">Atlasiet **Formulas veidotāju**, lai atvērtu **Formulas veidotāja** lapu.</span><span class="sxs-lookup"><span data-stu-id="b46f1-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="b46f1-129">Skatiet šajā lapā specifisku TDS nodokļa kodu definēto formulu.</span><span class="sxs-lookup"><span data-stu-id="b46f1-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="b46f1-130">Grāmatot rēķinu.</span><span class="sxs-lookup"><span data-stu-id="b46f1-130">Post the invoice.</span></span> <span data-ttu-id="b46f1-131">TDS summa, kas aprēķināta pirkšanas rēķinos, tiek grāmatota maksājumu kontā, un TDS summa, kas aprēķināta pārdošanas rēķinos, tiek grāmatota debitoru kontā, kas ir definēts katram TDS nodokļu kodam TDS grupā.</span><span class="sxs-lookup"><span data-stu-id="b46f1-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="b46f1-132">TDS nodokļu kodu kreditoru vai debitoru konti ir definēti **Ieturētā nodokļa kodu** lapā.</span><span class="sxs-lookup"><span data-stu-id="b46f1-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="b46f1-133">Atlasiet **Vaicājuma** pogu **> Rēķins > Grāmatots ieturētais nodoklis**, lai atvērtu lapu **Ieturētā nodokļa darījumi**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="b46f1-134">Varat skatīt kopējo procentuālo vērtību, kas tiek izmantota darījuma TDS aprēķinam laukā **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="b46f1-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="b46f1-135">Cilnes **Pārskats**, **Vispārīgi** un **Summa** lauki lapā **Ieturētā nodokļa darījumi** tiek parādīta darījumam aprēķinātā TDS informācija.</span><span class="sxs-lookup"><span data-stu-id="b46f1-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="b46f1-136">Skatiet TDS aprēķina informāciju par katru TDS nodokļu kodu, kas ir pievienots TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="b46f1-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
