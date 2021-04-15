---
title: Grāmatošanas definīciju piemēri
description: Šajā rakstā ir sniegti piemēri, kuros ir redzams, ka grāmatošanas definīcijas tiek lietotas pirkšanas pasūtījumu apgrūtinājumiem un budžeta asignējumiem.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f8875fd0f1894d7848b3afc76a55d052233b4c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817081"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="af7a4-103">Grāmatošanas definīciju piemēri</span><span class="sxs-lookup"><span data-stu-id="af7a4-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af7a4-104">Šajā rakstā ir sniegti piemēri, kuros ir redzams, ka grāmatošanas definīcijas tiek lietotas pirkšanas pasūtījumu apgrūtinājumiem un budžeta asignējumiem.</span><span class="sxs-lookup"><span data-stu-id="af7a4-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="af7a4-105">Pirms šīs tēmas lasīšanas jums ir jāpārzina grāmatošanas definīcijas un transakciju grāmatošanas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="af7a4-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="af7a4-106">Informāciju skatiet rakstā [Grāmatošanas definīcijas](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="af7a4-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="af7a4-107">Tālāk sniegtos piemērus var iestatīt lapā **Grāmatošanas definīcijas**.</span><span class="sxs-lookup"><span data-stu-id="af7a4-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="af7a4-108">Katrs piemērs satur trīs sadaļas.</span><span class="sxs-lookup"><span data-stu-id="af7a4-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="af7a4-109">Grāmatošanas definīcija — atbilstības kritēriji</span><span class="sxs-lookup"><span data-stu-id="af7a4-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="af7a4-110">Grāmatošanas definīcija — ģenerētie ieraksti</span><span class="sxs-lookup"><span data-stu-id="af7a4-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="af7a4-111">Transakcijas ar kontiem, dimensiju vērtībām un summām</span><span class="sxs-lookup"><span data-stu-id="af7a4-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="af7a4-112">Izmantojot grāmatošanas definīciju ģenerētie virsgrāmatas ieraksti</span><span class="sxs-lookup"><span data-stu-id="af7a4-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="af7a4-113">Ja tiek noteikta atbilstība starp kontiem un dimensiju vērtībām grāmatošanas definīcijas rūtī **Atbilstības kritēriji** un transakcijas kontiem un dimensiju vērtībām, tiek ģenerēti virsgrāmatas ieraksti, pamatojoties uz grāmatošanas definīcijas rūti **Ģenerētie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="af7a4-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="af7a4-114">Lai grāmatošanas definīciju saistītu ar konkrētu transakcijas tipu, izmantojiet lapu **Transakciju grāmatošanas definīcijas**.</span><span class="sxs-lookup"><span data-stu-id="af7a4-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="af7a4-115">Kad grāmatošanas definīciju esat saistījis ar transakcijas tipu un lapā **Virsgrāmatas parametri** esat atlasījis opciju **Izmantot grāmatošanas definīcijas**, visām atlasītā tipa transakcijām ir jālieto grāmatošanas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="af7a4-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="af7a4-116">Piemērs: pirkšanas pasūtījuma apgrūtinājumi</span><span class="sxs-lookup"><span data-stu-id="af7a4-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="af7a4-117">Ja iespējojat apgrūtinājumu apstrādi, atlasot opciju **Iespējot apgrūtinājumu apstrādi** lapā **Virsgrāmatas parametri**, visiem kontiem, kas ir jārezervē, ir jāizmanto grāmatošanas definīcijas, lai reģistrētu apgrūtinājumus virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="af7a4-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="af7a4-118">Parasti visi izdevumu konti tiek rezervēti bilancē.</span><span class="sxs-lookup"><span data-stu-id="af7a4-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="af7a4-119">Modulim **Pirkšana** apgrūtinājumu grāmatošanas definīcijas tiek iestatītas lapā **Grāmatošanas definīcijas**.</span><span class="sxs-lookup"><span data-stu-id="af7a4-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="af7a4-120">Pēc tam lapas **Darījuma grāmatošanas definīcijas** apgabalā **Pirkšana** varat atlasīt transakcijas veidu **Pirkšanas pasūtījums**, lai saistītu grāmatošanas definīciju ar pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="af7a4-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="af7a4-121">Visām pirkšanas pasūtījumu apgrūtinājumu dokumentu transakcijām ir jābūt saskaņotām (debetam ir jābūt vienādam ar kredītu) katrā unikālajā dokumenta dimensijā.</span><span class="sxs-lookup"><span data-stu-id="af7a4-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="af7a4-122">Grāmatošanas definīcija — atbilstības kritēriji</span><span class="sxs-lookup"><span data-stu-id="af7a4-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="af7a4-123">Konta struktūra</span><span class="sxs-lookup"><span data-stu-id="af7a4-123">Account structure</span></span>       | <span data-ttu-id="af7a4-124">Saskaņot konta numuru</span><span class="sxs-lookup"><span data-stu-id="af7a4-124">Match account number</span></span> | <span data-ttu-id="af7a4-125">Prioritāte</span><span class="sxs-lookup"><span data-stu-id="af7a4-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="af7a4-126">Konta struktūra — P&Z</span><span class="sxs-lookup"><span data-stu-id="af7a4-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="af7a4-127">1</span><span class="sxs-lookup"><span data-stu-id="af7a4-127">1</span></span>        |

<span data-ttu-id="af7a4-128"><em>Tukša lauka \**Saskaņot konta numuru</em>* vērtība nozīmē, ka visi atbilstošie konti definētajā kontu struktūrā ir ietverti atbilstības noteikšanas kārtulā.</span><span class="sxs-lookup"><span data-stu-id="af7a4-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="af7a4-129">Grāmatošanas definīcija — ģenerētie ieraksti</span><span class="sxs-lookup"><span data-stu-id="af7a4-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="af7a4-130">Konta struktūra</span><span class="sxs-lookup"><span data-stu-id="af7a4-130">Account structure</span></span> | <span data-ttu-id="af7a4-131">Ģenerētais konta numurs</span><span class="sxs-lookup"><span data-stu-id="af7a4-131">Generated account number</span></span>                    | <span data-ttu-id="af7a4-132">Ģenerētais debets/kredīts</span><span class="sxs-lookup"><span data-stu-id="af7a4-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="af7a4-133">Bilance</span><span class="sxs-lookup"><span data-stu-id="af7a4-133">Balance</span></span>           | <span data-ttu-id="af7a4-134">300143 —(apgrūtinājuma konts)</span><span class="sxs-lookup"><span data-stu-id="af7a4-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="af7a4-135">Tā pati</span><span class="sxs-lookup"><span data-stu-id="af7a4-135">Same</span></span>                   |
| <span data-ttu-id="af7a4-136">Bilance</span><span class="sxs-lookup"><span data-stu-id="af7a4-136">Balance</span></span>           | <span data-ttu-id="af7a4-137">300144 — (apgrūtinājuma rezerves konts)</span><span class="sxs-lookup"><span data-stu-id="af7a4-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="af7a4-138">Līdzsvara noturēšana</span><span class="sxs-lookup"><span data-stu-id="af7a4-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="af7a4-139">Transakcijas ar kontiem, dimensiju vērtībām un summām</span><span class="sxs-lookup"><span data-stu-id="af7a4-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="af7a4-140">Konti un dimensijas vērtības ir iegūtas no uzskaites sadalēm, kas ir ievadītas pirkšanas pasūtījuma rindām, vai no kontiem un dimensijām, kas tiek automātiski ģenerēti, pamatojoties uz kreditoru, krājumu, kategoriju un dimensiju veidņu noklusējuma iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="af7a4-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="af7a4-141">Konts + dimensijas</span><span class="sxs-lookup"><span data-stu-id="af7a4-141">Account + dimensions</span></span>           | <span data-ttu-id="af7a4-142">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="af7a4-142">Debit</span></span>  | <span data-ttu-id="af7a4-143">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="af7a4-143">Credit</span></span> | <span data-ttu-id="af7a4-144">Komentārs</span><span class="sxs-lookup"><span data-stu-id="af7a4-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="af7a4-145">606400-OU\_1-OU\_3566-Apmācība</span><span class="sxs-lookup"><span data-stu-id="af7a4-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="af7a4-146">250,00</span><span class="sxs-lookup"><span data-stu-id="af7a4-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="af7a4-147">Izmantojot grāmatošanas definīciju ģenerētie virsgrāmatas ieraksti</span><span class="sxs-lookup"><span data-stu-id="af7a4-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="af7a4-148">Tiek izveidoti ģenerētie virsgrāmatas ieraksti, lai reģistrētu apgrūtinājumus.</span><span class="sxs-lookup"><span data-stu-id="af7a4-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="af7a4-149">Konts + dimensijas</span><span class="sxs-lookup"><span data-stu-id="af7a4-149">Account + dimensions</span></span>           | <span data-ttu-id="af7a4-150">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="af7a4-150">Debit</span></span>  | <span data-ttu-id="af7a4-151">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="af7a4-151">Credit</span></span> | <span data-ttu-id="af7a4-152">Komentārs</span><span class="sxs-lookup"><span data-stu-id="af7a4-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="af7a4-153">300143-OU\_1-OU\_3566-Apmācība</span><span class="sxs-lookup"><span data-stu-id="af7a4-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="af7a4-154">250,00</span><span class="sxs-lookup"><span data-stu-id="af7a4-154">250.00</span></span> |        |         |
| <span data-ttu-id="af7a4-155">300144-OU\_1-OU\_3566-Apmācība</span><span class="sxs-lookup"><span data-stu-id="af7a4-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="af7a4-156">250,00</span><span class="sxs-lookup"><span data-stu-id="af7a4-156">250.00</span></span> |         |

<span data-ttu-id="af7a4-157">Šajā piemērā jebkurš konts, kas ietilpst konta struktūrā — P&Z, atbilst grāmatošanas definīcijas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="af7a4-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="af7a4-158">Tāpēc, novērtējot 606500-OU\_1-OU\_3566-Apmācība, ģenerētie ieraksti tiek izveidoti kontiem, kas grāmatošanas definīcijai ir definēti rūtī **Ģenerētie ieraksti**.</span><span class="sxs-lookup"><span data-stu-id="af7a4-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="af7a4-159">Piemērs: budžeta asignēšana</span><span class="sxs-lookup"><span data-stu-id="af7a4-159">Example: Budget appropriations</span></span>
<span data-ttu-id="af7a4-160">Ja iespējot budžeta asignēšanu, atlasot opciju **Iespējot budžeta asignēšanu** lapā **Virsgrāmatas parametri**, grāmatošanas definīcijas ir jāizmanto, lai reģistrētu budžeta reģistra ierakstus virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="af7a4-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="af7a4-161">Kad ir aktivizēta un ieslēgta budžeta kontroles konfigurācija, grāmatošanas definīcijas un transakciju grāmatošanas definīcijas var izmantot, lai atbalstītu asignējumu, pārskatījumu, pārsūtījumu, projektu, pamatlīdzekļu un piedāvājuma un pieprasījuma prognožu ierakstu reģistrēšanai virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="af7a4-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="af7a4-162">Lai iestatītu grāmatošanas definīciju budžeta reģistra ierakstiem, kuru budžeta veids ir **Sākotnējais budžets** un kam ir iespējota asignēšana, lapā **Grāmatošanas definīcijas** atlasiet moduli **Budžets**.</span><span class="sxs-lookup"><span data-stu-id="af7a4-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="af7a4-163">Pēc tam lapas **Darījuma grāmatošanas definīcijas** apgabalā **Budžets** varat izmantot budžeta kodus, lai saistītu grāmatošanas definīciju ar budžeta reģistra ierakstiem, kuru budžeta veids ir **Sākotnējais budžets**.</span><span class="sxs-lookup"><span data-stu-id="af7a4-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="af7a4-164">Kad ir iespējoti budžeta asignējumi un grāmatošanas definīcijas, budžeta reģistra ieraksti tiek reģistrēti budžeta kontroles nolūkā un virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="af7a4-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="af7a4-165">Grāmatošanas definīcija — atbilstības kritēriji</span><span class="sxs-lookup"><span data-stu-id="af7a4-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="af7a4-166">Konta struktūra</span><span class="sxs-lookup"><span data-stu-id="af7a4-166">Account structure</span></span>       | <span data-ttu-id="af7a4-167">Saskaņot konta numuru</span><span class="sxs-lookup"><span data-stu-id="af7a4-167">Match account number</span></span> | <span data-ttu-id="af7a4-168">Prioritāte</span><span class="sxs-lookup"><span data-stu-id="af7a4-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="af7a4-169">Konta struktūra — P&Z</span><span class="sxs-lookup"><span data-stu-id="af7a4-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="af7a4-170">1</span><span class="sxs-lookup"><span data-stu-id="af7a4-170">1</span></span>        |

<span data-ttu-id="af7a4-171"><em>Tukša lauka \**Saskaņot konta numuru</em>* vērtība nozīmē, ka visi atbilstošie konti definētajā kontu struktūrā ir ietverti atbilstības noteikšanas kārtulā.</span><span class="sxs-lookup"><span data-stu-id="af7a4-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="af7a4-172">Grāmatošanas definīcija — ģenerētie ieraksti</span><span class="sxs-lookup"><span data-stu-id="af7a4-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="af7a4-173">Konta struktūra</span><span class="sxs-lookup"><span data-stu-id="af7a4-173">Account structure</span></span> | <span data-ttu-id="af7a4-174">Ģenerētais konta numurs</span><span class="sxs-lookup"><span data-stu-id="af7a4-174">Generated account number</span></span>              | <span data-ttu-id="af7a4-175">Ģenerētais debets/kredīts</span><span class="sxs-lookup"><span data-stu-id="af7a4-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="af7a4-176">Konta struktūra</span><span class="sxs-lookup"><span data-stu-id="af7a4-176">Account structure</span></span> | <span data-ttu-id="af7a4-177">300145 — (novērtēto ieņēmumu konts)</span><span class="sxs-lookup"><span data-stu-id="af7a4-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="af7a4-178">Tā pati</span><span class="sxs-lookup"><span data-stu-id="af7a4-178">Same</span></span>                   |
| <span data-ttu-id="af7a4-179">Konta struktūra</span><span class="sxs-lookup"><span data-stu-id="af7a4-179">Account structure</span></span> | <span data-ttu-id="af7a4-180">300146 — (asignēšanas konts)</span><span class="sxs-lookup"><span data-stu-id="af7a4-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="af7a4-181">Līdzsvara noturēšana</span><span class="sxs-lookup"><span data-stu-id="af7a4-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="af7a4-182">Transakcijas ar kontiem, dimensiju vērtībām un summām</span><span class="sxs-lookup"><span data-stu-id="af7a4-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="af7a4-183">Budžeta konta ieraksta kontus, dimensiju vērtības un summas var ievadīt lapā **Budžeta reģistra ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="af7a4-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="af7a4-184">Konts + dimensijas</span><span class="sxs-lookup"><span data-stu-id="af7a4-184">Account + dimensions</span></span>           | <span data-ttu-id="af7a4-185">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="af7a4-185">Debit</span></span> | <span data-ttu-id="af7a4-186">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="af7a4-186">Credit</span></span> | <span data-ttu-id="af7a4-187">Komentārs</span><span class="sxs-lookup"><span data-stu-id="af7a4-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="af7a4-188">606400-OU\_1-OU\_3566-Apmācība</span><span class="sxs-lookup"><span data-stu-id="af7a4-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="af7a4-189">250,00</span><span class="sxs-lookup"><span data-stu-id="af7a4-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="af7a4-190">Izmantojot grāmatošanas definīciju ģenerētie virsgrāmatas ieraksti</span><span class="sxs-lookup"><span data-stu-id="af7a4-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="af7a4-191">Tiek izveidoti ģenerētie virsgrāmatas ieraksti, lai reģistrētu sākotnējo budžetu katrā dimensijā.</span><span class="sxs-lookup"><span data-stu-id="af7a4-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="af7a4-192">Konts + dimensijas</span><span class="sxs-lookup"><span data-stu-id="af7a4-192">Account + dimensions</span></span>           | <span data-ttu-id="af7a4-193">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="af7a4-193">Debit</span></span>  | <span data-ttu-id="af7a4-194">Kredītkarte</span><span class="sxs-lookup"><span data-stu-id="af7a4-194">Credit</span></span> | <span data-ttu-id="af7a4-195">Komentārs</span><span class="sxs-lookup"><span data-stu-id="af7a4-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="af7a4-196">300145-OU\_1-OU\_3566-Apmācība</span><span class="sxs-lookup"><span data-stu-id="af7a4-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="af7a4-197">250,00</span><span class="sxs-lookup"><span data-stu-id="af7a4-197">250.00</span></span> |         |
| <span data-ttu-id="af7a4-198">300146-OU\_1-OU\_3566-Apmācība</span><span class="sxs-lookup"><span data-stu-id="af7a4-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="af7a4-199">250,00</span><span class="sxs-lookup"><span data-stu-id="af7a4-199">250.00</span></span> |        |         |

<span data-ttu-id="af7a4-200">Šajā piemērā jebkurš konts, kas ietilpst konta struktūrā — P&Z, atbilst grāmatošanas definīcijas kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="af7a4-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="af7a4-201">Tāpēc, novērtējot 606400-OU\_1-OU\_3566-Apmācība, tiek izveidoti ģenerētie virsgrāmatas ieraksti.</span><span class="sxs-lookup"><span data-stu-id="af7a4-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]