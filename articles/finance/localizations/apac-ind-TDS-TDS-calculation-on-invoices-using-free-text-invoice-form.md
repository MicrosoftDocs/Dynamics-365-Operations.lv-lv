---
title: TDS aprēķins rēķinos no Brīva teksta rēķina lapas
description: Šajā tēmā skaidrots, kā aprēķināt No kopējo ienākumu summas atskaitīto nodokli (TDS) rēķinos, izmantojot Brīvā teksta rēķina lapu.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023424"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="2e20a-103">TDS aprēķins rēķinos no Brīva teksta rēķina lapas</span><span class="sxs-lookup"><span data-stu-id="2e20a-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e20a-104">Šajā tēmā skaidrots, kā aprēķināt No kopējo ienākumu summas atskaitīto nodokli (TDS) rēķinos, izmantojot **Brīvā teksta rēķina** lapu.</span><span class="sxs-lookup"><span data-stu-id="2e20a-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="2e20a-105">Dodieties uz **Debitoru parādi \> Rēķini \> Visi brīva teksta rēķini**.</span><span class="sxs-lookup"><span data-stu-id="2e20a-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="2e20a-106">[![Brīva teksta rēķinu lapa](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="2e20a-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="2e20a-107">Atlasiet **Jauns**, lai izveidotu brīvā teksta rēķinu, un pēc tam ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="2e20a-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="2e20a-108">Atlasiet cilni **Rēķins**. Sadaļā **Ieturētā nodokļa grupa** lauks **Vērtētāja raksturs** parāda klienta atzīmju kategorijas veidu.</span><span class="sxs-lookup"><span data-stu-id="2e20a-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="2e20a-109">**TDS grupas** laukā pārskatiet vai mainiet noklusējuma TDS grupu, kas noteikta debitoram.</span><span class="sxs-lookup"><span data-stu-id="2e20a-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2e20a-110">**TCS grupas** lauks nav pieejams, kad atlasāt vērtību laukā **TDS grupa**.</span><span class="sxs-lookup"><span data-stu-id="2e20a-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="2e20a-111">TDS tiek aprēķināts tikai tad, ja opcija **Aprēķināt ieturēto nodokli** ir iestatīta uz **Jā** debitoram lapā **Visi debitori**.</span><span class="sxs-lookup"><span data-stu-id="2e20a-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="2e20a-112">Cilnē **Informācija par nodokļiem**, sadaļā **Informācija par uzņēmumu**, laukā **Nosaukums** atlasiet uzņēmuma nosaukumu alternatīvai adresei, kas ir iestatīta uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="2e20a-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="2e20a-113">Sadaļā **Ieturētais nodoklis** lauks **Nodokļu konta numurs (TAN)** rāda atlasītā uzņēmuma nodokļu konta numuru (TAN).</span><span class="sxs-lookup"><span data-stu-id="2e20a-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="2e20a-114">Cilnē **Rēķina rindas** izveidojiet rēķina rindas un ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="2e20a-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="2e20a-115">Sadaļas **Ieturēto nodokļu grupa** laukā **Nodokļu konta numurs (TAN)** ir redzams TAN, un **TDS grupas** laukā ir redzama TDS grupa.</span><span class="sxs-lookup"><span data-stu-id="2e20a-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="2e20a-116">Atlasiet **Ieturētais nodokli**, lai atvērtu **Pagaidu ieturētā nodokļa darījumu** lapu.</span><span class="sxs-lookup"><span data-stu-id="2e20a-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="2e20a-117">Šīs lapas augšējai daļai ir šādi lauki:</span><span class="sxs-lookup"><span data-stu-id="2e20a-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="2e20a-118">**Ieturētā nodokļa kopsumma** - TDS kopsumma, kas tika aprēķināta darījumam TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="2e20a-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="2e20a-119">**Vērtība** - kopējā procentuālā vērtība, kas tika izmantota darījuma TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="2e20a-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="2e20a-120">Kopējā procentuālā vērtība ir balstīta uz formulu, kas noteikta TDS nodokļu kodiem un pievienota TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="2e20a-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="2e20a-121">**Koriģētā ieturētā nodokļa kopsumma** - kopējā koriģētā TDS summa visiem nodokļu kodiem TDS grupā.</span><span class="sxs-lookup"><span data-stu-id="2e20a-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="2e20a-122">**TDS** - atlasītā izvēles rūtiņa norāda, ka TDS grupa ir pievienota darījumam.</span><span class="sxs-lookup"><span data-stu-id="2e20a-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="2e20a-123">Lauki cilnēs **Pārskats**, **Vispārīgi** un **Korekcija** parāda aprēķināto TDS summu un pielāgoto TDS summas informāciju par katru TDS nodokļa kodu, kas pievienots TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="2e20a-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="2e20a-124">Atlasiet **Slieksni**, lai atvērtu lapu **Slieksnis**, kur varat pārskatīt sliekšņa ierobežojumu, kas ir definēts TDS nodokļu komponentam, kas ir piesaistīts konkrētam TDS nodokļa kodam.</span><span class="sxs-lookup"><span data-stu-id="2e20a-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="2e20a-125">Select **Formulas veidotāju**, lai atvērtu **Formulas veidotāja** lapu, kurā varat pārskatīt noteiktam TDS nodokļa kodam definēto formulu.</span><span class="sxs-lookup"><span data-stu-id="2e20a-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="2e20a-126">Grāmatot brīva teksta rēķinu.</span><span class="sxs-lookup"><span data-stu-id="2e20a-126">Post the free text invoice.</span></span> <span data-ttu-id="2e20a-127">TDS summa, kas tiek aprēķināta brīvā teksta rēķinam, tiek grāmatota debitoru kontā, kas katrai TDS nodokļu kodam ir definēts TDS grupā.</span><span class="sxs-lookup"><span data-stu-id="2e20a-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="2e20a-128">TDS nodokļu kodu debitoru konti ir definēti **Ieturētā nodokļa kodu** lapā.</span><span class="sxs-lookup"><span data-stu-id="2e20a-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="2e20a-129">Atlasiet **Grāmatoto ieturēto nodokli**, lai atvērtu **Ieturētā nodokļa darījumu** lapu.</span><span class="sxs-lookup"><span data-stu-id="2e20a-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="2e20a-130">**Vērtība** - lauks parāda kopējo procentuālo vērtību, kas tika izmantota darījuma TDS aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="2e20a-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="2e20a-131">Cilņu **Pārskats**, **Vispārīgi** un **Summa** laukos rāda TDS summas, kas aprēķinātas rēķina rindās.</span><span class="sxs-lookup"><span data-stu-id="2e20a-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="2e20a-132">Pārskatiet TDS aprēķina informāciju par katru TDS nodokļu kodu, kas ir pievienots TDS grupai.</span><span class="sxs-lookup"><span data-stu-id="2e20a-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
