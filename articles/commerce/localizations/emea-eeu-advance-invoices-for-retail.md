---
title: Avansa rēķini programmai Commerce Austrumeiropā
description: Šajā tēmā ir paskaidrots, kā iestatīt avansa paziņojumus programmai Commerce Austrumeiropā.
author: epopov
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7bdd1d99ffbc1112226fd2db168cc5fc61615b9a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798836"
---
# <a name="advance-invoices-for-commerce-for-eastern-europe"></a><span data-ttu-id="8440a-103">Avansa rēķini programmai Commerce Austrumeiropā</span><span class="sxs-lookup"><span data-stu-id="8440a-103">Advance invoices for Commerce for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8440a-104">Šajā tēmā ir sniegta informācija par Austrumeiropas lokalizāciju un attiecas uz komercijas nozari.</span><span class="sxs-lookup"><span data-stu-id="8440a-104">The information in this topic applies to the Eastern European localization and is specific to the commerce industry.</span></span>

<span data-ttu-id="8440a-105">Polijā, Ungārijā un Čehijas Republikā, saņemot priekšapmaksu no debitora caur pārdošanas punktu (Point of Sale — POS), priekšapmaksa ir jāreģistrē nodokļu aprēķinam, un ir nepieciešams izveidot un drukāt avansa rēķina dokumentu, kurā norādīta priekšapmaksas summa.</span><span class="sxs-lookup"><span data-stu-id="8440a-105">For Poland, Hungary, and Czech Republic, when a prepayment is received from a customer via Point of Sale (POS), the prepayment must be registered for tax purposes, and it's required to generate and print an advance invoice document that includes the prepayment amount.</span></span> <span data-ttu-id="8440a-106">Turklāt Polijā avansa rēķinu transakcijas ir jāgrāmato virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="8440a-106">Additionally, for Poland, advance invoice transactions must be posted in the general ledger.</span></span>

<span data-ttu-id="8440a-107">Kad tiek veikts galīgais pārdošanas pasūtījuma rēķina grāmatojums, galīgajā dokumentā jāietver avansa rēķins un ir jānorāda visas priekšapmaksas.</span><span class="sxs-lookup"><span data-stu-id="8440a-107">When the invoice for the sales order is finally posted, the final document should include the advance invoice, and any prepayments should be indicated.</span></span>

<span data-ttu-id="8440a-108">Ja pārdošanas pasūtījumi tiek izveidoti no debitoru parādiem, ir manuāli jāizveido avansa rēķini, izmantojot procedūru, kas aprakstīta tēmā [Avansa rēķini Austrumeiropas valstīm](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span><span class="sxs-lookup"><span data-stu-id="8440a-108">If you generate sales orders from Accounts receivable, you must manually generate advance invoices by using the procedure in [Advance invoices for Eastern Europe](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/emea-advance-invoice).</span></span> <span data-ttu-id="8440a-109">Ja pārdošanas pasūtījumi tiek izveidoti ar POS starpniecību, sistēma izveido un grāmato avansa rēķinus jūsu vietā.</span><span class="sxs-lookup"><span data-stu-id="8440a-109">If you generate sales orders via POS, the system generates and posts the advance invoices for you.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="8440a-110">Atbalstītie scenāriji</span><span class="sxs-lookup"><span data-stu-id="8440a-110">Supported scenarios</span></span>

<span data-ttu-id="8440a-111">Tālāk ir norādīti atbalstītie scenāriji.</span><span class="sxs-lookup"><span data-stu-id="8440a-111">The following scenarios are supported:</span></span>

- <span data-ttu-id="8440a-112">Izveidojiet un grāmatojiet avansa rēķinu.</span><span class="sxs-lookup"><span data-stu-id="8440a-112">Create and post an advance invoice.</span></span>
- <span data-ttu-id="8440a-113">Modificējiet depozīta summu.</span><span class="sxs-lookup"><span data-stu-id="8440a-113">Modify a deposit amount.</span></span> <span data-ttu-id="8440a-114">Ja debitors izlemj palielināt depozīta summu, tiek izsniegts papildu avansa rēķins.</span><span class="sxs-lookup"><span data-stu-id="8440a-114">If a customer decides to increase the amount of a deposit, an additional advance invoice is issued.</span></span> <span data-ttu-id="8440a-115">Visu pārējo depozīta summas izmaiņu gadījumā (piemēram, ja debitora pasūtījums ir labots) tiek izveidota kredīta nota avansa rēķinam, kas tika izveidots iepriekš, un tiek izveidots un grāmatots jauns avansa rēķins par laboto summu.</span><span class="sxs-lookup"><span data-stu-id="8440a-115">For all other changes to the deposit amount (for example, if a customer order is edited), a credit note is created for the advance invoice that was previously generated, and a new advance invoice is generated and posted for the corrected amount.</span></span>
- <span data-ttu-id="8440a-116">Atceliet pārdošanas pasūtījumu, kuram ir saistīti avansa rēķini.</span><span class="sxs-lookup"><span data-stu-id="8440a-116">Cancel a sales order that has linked advance invoices.</span></span> <span data-ttu-id="8440a-117">Šādā gadījumā avansa rēķinam tiek izveidota kredīta nota.</span><span class="sxs-lookup"><span data-stu-id="8440a-117">In this case, a credit note is created for the advance invoice.</span></span>
- <span data-ttu-id="8440a-118">Grāmatojiet pārdošanas pasūtījuma rēķinu, kuram ir saistīti avansa rēķini.</span><span class="sxs-lookup"><span data-stu-id="8440a-118">Post a sales order invoice that has linked advance invoices.</span></span> <span data-ttu-id="8440a-119">Avansa rēķins, kas ir saistīts ar pārdošanas pasūtījumu, tiek atsaukts par pārdošanas rēķina summu.</span><span class="sxs-lookup"><span data-stu-id="8440a-119">The advance invoice that is linked to a sales order is reversed for the amount of the sales invoice.</span></span> <span data-ttu-id="8440a-120">Avansa rēķina transakcijas tiek nosegtas ar avansa rēķina atsaukšanas transakcijām.</span><span class="sxs-lookup"><span data-stu-id="8440a-120">The advance invoice transactions are settled with advance invoice reversal transactions.</span></span>

## <a name="set-up-advance-invoices"></a><span data-ttu-id="8440a-121">Avansa rēķinu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8440a-121">Set up advance invoices</span></span>

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a><span data-ttu-id="8440a-122">Ieslēgt avansa rēķinu veidošanas funkcionalitāti</span><span class="sxs-lookup"><span data-stu-id="8440a-122">Turn on the functionality for creating advance invoices</span></span>

1. <span data-ttu-id="8440a-123">Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Komercijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="8440a-123">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span>
2. <span data-ttu-id="8440a-124">Cilnes **Debitoru pasūtījumi** kopsavilkuma cilnē **Pasūtījums** iestatiet opcijai **Izveidot avansa rēķinu depozītam** vienumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8440a-124">On the **Customer orders** tab, on the **Order** FastTab, set the **Create advance invoice for deposit** option to **Yes**.</span></span>

### <a name="define-the-parameters-for-posting-advance-invoices"></a><span data-ttu-id="8440a-125">Parametru definēšana avansa rēķinu grāmatošanai</span><span class="sxs-lookup"><span data-stu-id="8440a-125">Define the parameters for posting advance invoices</span></span>

1. <span data-ttu-id="8440a-126">Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru moduļa parametri**.</span><span class="sxs-lookup"><span data-stu-id="8440a-126">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="8440a-127">Cilnes **Atjauninājumi** kopsavilkuma cilnē **Avansa rēķins** iestatiet vērtības laukos **Grāmatošanas metode**, **PVN grupa** un **Krājumu PVN grupa**.</span><span class="sxs-lookup"><span data-stu-id="8440a-127">On the **Updates** tab, on the **Advance invoice** FastTab, set the **Posting profile**, **Sales tax group**, and **Item sales tax group** fields.</span></span> <span data-ttu-id="8440a-128">Ja šie lauki ir iestatīti pareizi, avansa rēķins tiks grāmatots.</span><span class="sxs-lookup"><span data-stu-id="8440a-128">If these fields are set correctly, the advance invoice will be posted.</span></span> <span data-ttu-id="8440a-129">Ja šie lauki nav iestatīti, avansa rēķini netiks grāmatoti.</span><span class="sxs-lookup"><span data-stu-id="8440a-129">If these fields aren't set, advance invoices won't be posted.</span></span>

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a><span data-ttu-id="8440a-130">PVN priekšapmaksas žurnāla dokumenta summā grāmatošanas izslēgšana</span><span class="sxs-lookup"><span data-stu-id="8440a-130">Turn off posting of the Sales tax on prepayment journal voucher</span></span>

<span data-ttu-id="8440a-131">PVN priekšapmaksas žurnāla dokumenta summā nedrīkst grāmatot, ja ir ieslēgta avansa rēķina grāmatošana.</span><span class="sxs-lookup"><span data-stu-id="8440a-131">The Sales tax on prepayment journal voucher must not be posted if advance invoice posting is turned on.</span></span> <span data-ttu-id="8440a-132">Lai pārbaudītu, vai šī prasība ir izpildīta, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="8440a-132">To verify that this requirement is met, follow these steps.</span></span>

1. <span data-ttu-id="8440a-133">Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru moduļa parametri**.</span><span class="sxs-lookup"><span data-stu-id="8440a-133">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="8440a-134">Cilnes **Virsgrāmata un PVN** kopsavilkuma cilnē **Maksājums** pārliecinieties, ka tālāk minētie lauki ir tukši vai tajos ir iestatīts vienums **Nē**.</span><span class="sxs-lookup"><span data-stu-id="8440a-134">On the **Ledger and sales tax** tab, on the **Payment** FastTab, make sure that the following fields are blank or set to **No**:</span></span>

    - <span data-ttu-id="8440a-135">PVN priekšapmaksas žurnāla dokumenta summā</span><span class="sxs-lookup"><span data-stu-id="8440a-135">Sales tax on prepayment journal voucher</span></span>
    - <span data-ttu-id="8440a-136">Grāmatošanas profils priekšapmaksas žurnāla dokumenta summā</span><span class="sxs-lookup"><span data-stu-id="8440a-136">Posting profile with prepayment journal voucher</span></span>
    - <span data-ttu-id="8440a-137">Nodokļu grupa priekšapmaksai</span><span class="sxs-lookup"><span data-stu-id="8440a-137">Tax group for prepayment</span></span>
    - <span data-ttu-id="8440a-138">Krājumu PVN grupa</span><span class="sxs-lookup"><span data-stu-id="8440a-138">Item Sales tax group</span></span>

## <a name="print-advance-invoices"></a><span data-ttu-id="8440a-139">Avansa rēķinu drukāšana</span><span class="sxs-lookup"><span data-stu-id="8440a-139">Print advance invoices</span></span>

<span data-ttu-id="8440a-140">Varat drukāt avansa rēķinus no POS, izmantojot Microsoft Windows printeri, kas ir pievienots aparatūras stacijai.</span><span class="sxs-lookup"><span data-stu-id="8440a-140">You can print advance invoices from POS on a Microsoft Windows printer that is connected to the hardware station.</span></span> <span data-ttu-id="8440a-141">Pastāv divas opcijas avansa rēķina drukāšanai no POS.</span><span class="sxs-lookup"><span data-stu-id="8440a-141">There are two options for printing an advance invoice from POS:</span></span>

- <span data-ttu-id="8440a-142">**Drukāt avansa rēķinu pēc transakcijas noslēgšanas POS.**</span><span class="sxs-lookup"><span data-stu-id="8440a-142">**Print an advance invoice after a transaction is concluded in POS.**</span></span> <span data-ttu-id="8440a-143">Šī opcija tiek izpildīta automātiski, ja avansa rēķins tika izveidots un Windows printeris tika pareizi iestatīts.</span><span class="sxs-lookup"><span data-stu-id="8440a-143">This option occurs automatically if an advance invoice was generated and a Windows printer was correctly set up.</span></span> <span data-ttu-id="8440a-144">Šādā gadījumā tiek drukāts tikai pēdējais avansa rēķinu, kas saistīts ar debitora pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="8440a-144">In this case, only the last advance invoice that is linked to the customer order is printed.</span></span>
- <span data-ttu-id="8440a-145">**Atkārtoti drukāt avansa rēķinu no transakciju žurnālā.**</span><span class="sxs-lookup"><span data-stu-id="8440a-145">**Reprint an advance invoice from the transaction journal.**</span></span> <span data-ttu-id="8440a-146">Atlasiet **Rādīt žurnālu**, lai atvērtu transakciju žurnālu, atrodiet debitora pasūtījumu un pēc tam atlasiet **Drukāt avansa rēķinu**.</span><span class="sxs-lookup"><span data-stu-id="8440a-146">Select **Show journal** to open the transactions journal, find the customer order, and then select **Print Advance invoice**.</span></span> <span data-ttu-id="8440a-147">Šādā gadījumā tiek drukāti visi avansa rēķini, kas saistīti ar debitora pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="8440a-147">In this case, all advance invoices that are linked to the customer order are printed.</span></span>

### <a name="set-up-a-windows-printer"></a><span data-ttu-id="8440a-148">Windows printera iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8440a-148">Set up a Windows printer</span></span>

<span data-ttu-id="8440a-149">Veiciet šādas darbības, lai iespējotu dokumentu drukāšanu no POS, izmantojot Windows printeri, kas ir savienots ar aparatūras stacija.</span><span class="sxs-lookup"><span data-stu-id="8440a-149">Follow these steps to enable documents to be printed from POS on a Windows printer that is connected to the hardware station.</span></span>

1. <span data-ttu-id="8440a-150">Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> POS iestatīšana \> POS profili \> Aparatūras profili**.</span><span class="sxs-lookup"><span data-stu-id="8440a-150">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
2. <span data-ttu-id="8440a-151">Atlasiet aparatūras profilu, kas attiecas uz veikalu, kurā tiek izmantots printeris.</span><span class="sxs-lookup"><span data-stu-id="8440a-151">Select a hardware profile that is related to the store where the printer is used.</span></span>
3. <span data-ttu-id="8440a-152">Sadaļā **Printeris** vai **2. printeris** atjauniniet iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="8440a-152">In either the **Printer** section or the **Printer 2** section, update the settings:</span></span>

    - <span data-ttu-id="8440a-153">Laukā **Printeris** atlasiet **Windows draiveris**.</span><span class="sxs-lookup"><span data-stu-id="8440a-153">In the **Printer** field, select **Windows driver**.</span></span>
    - <span data-ttu-id="8440a-154">Laukā **Ierīces nosaukums** ievadiet printera nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8440a-154">In the **Device name** field, enter the name of the printer.</span></span>

4. <span data-ttu-id="8440a-155">Pārejiet uz **Mazumtirdzniecība un komercija \> Mazumtirdzniecības un komercijas IT \> Sadales grafiks**.</span><span class="sxs-lookup"><span data-stu-id="8440a-155">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="8440a-156">Atlasiet darbu **1090** un pēc tam atlasiet **Izpildīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="8440a-156">Select job **1090**, and then select **Run now**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]