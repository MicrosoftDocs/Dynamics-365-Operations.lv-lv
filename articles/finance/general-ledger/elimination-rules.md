---
title: Korekciju kārtulas
description: Šajā tēmā ir sniegta informācija par korekciju kārtulām un dažādām korekciju ziņošanas iespējām.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a65cbd3d146abff5ceabea094fb735f8bd359f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968833"
---
# <a name="elimination-rules"></a><span data-ttu-id="03eb9-103">Korekciju kārtulas</span><span class="sxs-lookup"><span data-stu-id="03eb9-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03eb9-104">Šajā tēmā ir sniegta informācija par korekciju kārtulām un dažādām korekciju ziņošanas iespējām.</span><span class="sxs-lookup"><span data-stu-id="03eb9-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="03eb9-105">Korekcijas darbības ir nepieciešamas, kad pamata juridiska persona darbojas ar vienu vai vairākām pakārtotām juridiskām personām un tiek izmantoti konsolidētie finanšu pārskati.</span><span class="sxs-lookup"><span data-stu-id="03eb9-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="03eb9-106">Konsolidētajos finanšu pārskatos jābūt iekļautām tikai darbībām, kas veiktas starp konsolidēto organizāciju un citām personām ārpus šīs organizācijas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="03eb9-107">Tāpēc transakcijas starp juridiskajām personām, kas pieder vienai un tai pašai organizācijai, ir jānoņem no virsgrāmatas vai jākoriģē virsgrāmatā tā, lai tās netiktu rādītas finanšu pārskatos.</span><span class="sxs-lookup"><span data-stu-id="03eb9-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="03eb9-108">Ir vairāki veidi, kā ziņot korekcijas:</span><span class="sxs-lookup"><span data-stu-id="03eb9-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="03eb9-109">Korekciju kārtulu var izveidot un apstrādāt konsolidēšanas vai korekcijas uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="03eb9-110">Var izmantot finanšu pārskatu, lai parādītu korekciju kontus un dimensijas noteiktā rindā vai kolonnā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="03eb9-111">Var izmantot atsevišķu juridisku personu manuālo darbību ierakstu grāmatošanai, lai izsekotu korekcijas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="03eb9-112">Šajā tēmā ir pievērsta uzmanība korekciju kārtulām, kas tiek apstrādātas konsolidēšanas vai korekcijas uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="03eb9-113">Korekciju kārtulas varat iestatīt, lai izveidotu korekciju transakcijas juridiskajā personā, kura ir norādīta kā korekcijas mērķa juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="03eb9-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="03eb9-114">Šī mērķa juridiska persona ir pazīstama arī kā koriģēta juridiska persona.</span><span class="sxs-lookup"><span data-stu-id="03eb9-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="03eb9-115">Korekcijas žurnāli var tikt izveidoti konsolidācijas procesa laikā vai izmantojot korekcijas žurnāla priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="03eb9-116">Pirms likvidēšanas noteikumu iestatīšanas jums ir jāiepazīstas ar sekojošajiem terminiem:</span><span class="sxs-lookup"><span data-stu-id="03eb9-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="03eb9-117">**Avota juridiska persona** — juridiska persona, kurai koriģējamās summas ir iegrāmatotas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="03eb9-118">**Mērķa juridiska persona** — juridiska persona, kurā tiek grāmatoti korekcijas noteikumi.</span><span class="sxs-lookup"><span data-stu-id="03eb9-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="03eb9-119">**Koriģēta juridiska persona** — juridiska persona, kura ir norādīta kā mērķa juridiska persona korekcijai.</span><span class="sxs-lookup"><span data-stu-id="03eb9-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="03eb9-120">**Konsolidēta juridiska persona** — juridiska persona, kura tika izveidota, lai juridisku personu grupai ziņotu par finanšu rezultātiem.</span><span class="sxs-lookup"><span data-stu-id="03eb9-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="03eb9-121">Šajā juridiskajā personā ir konsolidēti juridisku personu finanšu dati, un finanšu pārskats tiek veidots no apvienotajiem datiem.</span><span class="sxs-lookup"><span data-stu-id="03eb9-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="03eb9-122">Šajā tabulā ir parādīti transakciju veidi, kurus var nākties koriģēt.</span><span class="sxs-lookup"><span data-stu-id="03eb9-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03eb9-123">Darījuma veids</span><span class="sxs-lookup"><span data-stu-id="03eb9-123">Transaction type</span></span></th>
<th><span data-ttu-id="03eb9-124">Piemērs</span><span class="sxs-lookup"><span data-stu-id="03eb9-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03eb9-125">Pārdošanas pasūtījuma ievade un rēķinu nosūtīšana (centralizēta apstrāde)</span><span class="sxs-lookup"><span data-stu-id="03eb9-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="03eb9-126">Jūs pārdodat preci debitoram citas juridiskas personas jūsu organizācijā vārdā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03eb9-127">Pārdošanas pasūtījuma ievade (starpuzņēmumu/uzņēmuma iekšienē) un rēķinu nosūtīšana</span><span class="sxs-lookup"><span data-stu-id="03eb9-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="03eb9-128">Jūs pārdodat preces starp juridiskām personām jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03eb9-129">Pirkšanas pasūtījumi (centralizēta apstrāde)</span><span class="sxs-lookup"><span data-stu-id="03eb9-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="03eb9-130">Jūs iegādājāties krājumus, izejvielas, pakalpojumus, pamatlīdzekļus un citas preces no kreditora citas juridiskas personas jūsu organizācijā vārdā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03eb9-131">Krājumu vadība (starpuzņēmumu/uzņēmuma iekšienē)</span><span class="sxs-lookup"><span data-stu-id="03eb9-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="03eb9-132">Jūs pārsūtat vienas juridiskas personas krājumus uz citas juridiskas personas jūsu organizācijā pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="03eb9-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="03eb9-133">Jūs pārsūtat vienas juridiskas personas krājumus uz citas juridiskas personas jūsu organizācijā krājumiem.</span><span class="sxs-lookup"><span data-stu-id="03eb9-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03eb9-134">Inventāra tranzīta izsekošana</span><span class="sxs-lookup"><span data-stu-id="03eb9-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="03eb9-135">Jūs pārsūtat krājumus starp vienas juridiskas personas noliktavām, kuras atrodas dažādās ģeogrāfiskās vietās.</span><span class="sxs-lookup"><span data-stu-id="03eb9-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03eb9-136">Parādu kreditoriem centralizēta rēķinu apstrāde</span><span class="sxs-lookup"><span data-stu-id="03eb9-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="03eb9-137">Jūs reģistrējat rēķinu citas juridiskas personas jūsu organizācijā vārdā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03eb9-138">Parādu kreditoriem centralizēta maksājumu apstrāde</span><span class="sxs-lookup"><span data-stu-id="03eb9-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="03eb9-139">Jūs apmaksājat rēķinu citas juridiskas personas jūsu organizācijā vārdā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03eb9-140">Kases pārvaldība un kase (centralizētā apstrāde)</span><span class="sxs-lookup"><span data-stu-id="03eb9-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="03eb9-141">Jūs apstrādājat nodokļu maksājumus, nodokļu atmaksājumus, procentu maksājumus, aizdevumus, avansus, samaksātās dividendes un iepriekšapmaksātus honorārus vai komisijas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="03eb9-142">Jūs apmaksājat izdevumus citas juridiskas personas jūsu organizācijā vārdā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="03eb9-143">Rēķins tiek ievadīts mērķa juridiskas personas grāmatās un jums ir jāsedz maksājumi juridisku personu starpā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="03eb9-144">Piemēram, viena juridiska persona apmaksā darbinieka izdevumu pārskatu citā juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="03eb9-145">Šādā gadījumā darbinieka izdevumu pārskatā ir izdevumi, kuri ir saistīti ar citu juridisku personu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="03eb9-146">Jūs pārvedat skaidru naudu no vienas juridiskas personas uz otru jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03eb9-147">Debitoru parādi (centralizēta apstrāde)</span><span class="sxs-lookup"><span data-stu-id="03eb9-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="03eb9-148">Jūs saņemat skaidru naudu par citas juridiskas personas debitora rēķinu un noguldāt čeku šīs juridiskas personas bankas kontā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03eb9-149">Algas (centralizēta apstrāde, starpuzņēmumu/uzņēmumā)</span><span class="sxs-lookup"><span data-stu-id="03eb9-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="03eb9-150">Jūs maksājat citas juridiskas personas algas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="03eb9-151">Piemēram, juridiska persona maksā algu saviem darbiniekiem, bet izdara atvilkumu par darbu, ko darbinieks paveicis citai juridiskai personai tā algu aprēķina izpildes posmā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="03eb9-152">Vai arī, darbinieks ir strādājis uz nepilnu slodzi gan juridiskajā personā A, gan juridiskajā personā B, un atalgojumu saņem no abiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="03eb9-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="03eb9-153">Šajos gadījumos darbinieka alga ietver maksājumus no abām juridiskām personām.</span><span class="sxs-lookup"><span data-stu-id="03eb9-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="03eb9-154">Grāmatotas tiek ne tikai algas, bet arī to nodokļi, pabalsti, atvilkumi un uzkrājumi.</span><span class="sxs-lookup"><span data-stu-id="03eb9-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="03eb9-155">Jūs pārvedat darbaspēku no vienas struktūrvienības vai nodaļas uz otru.</span><span class="sxs-lookup"><span data-stu-id="03eb9-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03eb9-156">Pamatlīdzekļi (starpuzņēmumu/uzņēmuma)</span><span class="sxs-lookup"><span data-stu-id="03eb9-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="03eb9-157">Jūs pārsūtat pamatlīdzekļus uz citas juridiskas personas pamatlīdzekļiem vai krājumiem.</span><span class="sxs-lookup"><span data-stu-id="03eb9-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03eb9-158">Sadalījumi (starpuzņēmumu/uzņēmuma)</span><span class="sxs-lookup"><span data-stu-id="03eb9-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="03eb9-159">Jūs apstrādājat korporatīvos sadalījumus.</span><span class="sxs-lookup"><span data-stu-id="03eb9-159">You process corporate allocations.</span></span> <span data-ttu-id="03eb9-160">Sadalījumi ir aktivitātes attiecībā uz jebkuru sadalīto kontu, neatkarīgi no izcelsmes moduļa.</span><span class="sxs-lookup"><span data-stu-id="03eb9-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="03eb9-161">Piemērs</span><span class="sxs-lookup"><span data-stu-id="03eb9-161">Example</span></span>
<span data-ttu-id="03eb9-162">Jūsu juridiska persona — juridiska persona A — pārdod logrīkus citai juridiskai personai jūsu organizācijā — juridiskai personai B. Šajā piemērā ir parādīts, kā var rasties nepieciešamība koriģēt transakcijas, kas notiek starp divām juridiskām personām:</span><span class="sxs-lookup"><span data-stu-id="03eb9-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="03eb9-163">Juridiska persona A pārdod logrīku, kas maksā 10,00 juridiskai personai B par 10,00.</span><span class="sxs-lookup"><span data-stu-id="03eb9-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="03eb9-164">Juridiska persona A pārdod logrīku, kas maksā 10,00 juridiskai personai B par 10,00 plus 2,00 par faktiskajām transporta izmaksām.</span><span class="sxs-lookup"><span data-stu-id="03eb9-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="03eb9-165">Juridiska persona A pārdod logrīku, kas maksā 10,00, juridiskai personai B par 15,00 un atzīst peļņu no šīs pārdošanas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="03eb9-166">Juridiska persona A pārdod logrīku, kas maksā 10,00, juridiskai personai B par 15,00 un atzīst daļu no peļņas no šīs pārdošanas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="03eb9-167">Juridiska persona B atzīst otru daļu no peļņas par pārdošanu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="03eb9-168">Līdz ar to ieņēmumi tiek sadalīti.</span><span class="sxs-lookup"><span data-stu-id="03eb9-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="03eb9-169">Ieņēmumu sadalīšana veicina pasūtīšanu no citas juridiskas personas organizācijā, nevis no ārējās organizācijas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="03eb9-170">Visas šīs transakcijas ir starpuzņēmumu transakcijas, kuras tiek grāmatotas abu pušu kontos.</span><span class="sxs-lookup"><span data-stu-id="03eb9-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="03eb9-171">Turklāt šajās transakcijās var tikt iekļautas uzcenojuma un nocenošanas summas, kad starpuzņēmumu pārdošanas summa nav vienāda ar preču vērtību.</span><span class="sxs-lookup"><span data-stu-id="03eb9-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="03eb9-172">Korekcijas noteikumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="03eb9-172">Set up elimination rules</span></span>
<span data-ttu-id="03eb9-173">Iestatot korekciju kārtulas, ir ieteicams izveidot finanšu dimensiju, kas ir īpaši paredzēta korekcijas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="03eb9-173">When setting up elimination rules, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="03eb9-174">Vairums klientu tai piešķir nosaukumu Darījumu partneris vai tamlīdzīgu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="03eb9-175">Ja izlemjat kādu finanšu dimensiju nelietot, jums noteikti ir nepieciešami galvenie konti, kas ir raksturīgi tikai starpuzņēmumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="03eb9-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="03eb9-176">Korekciju iestatījumi atrodamas moduļa Konsolidācijas apgabalā Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="03eb9-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="03eb9-177">Kad esat ievadījis kārtulas aprakstu, ir jāizvēlas uzņēmums, uz kuru šis korekciju žurnāls tiks grāmatots.</span><span class="sxs-lookup"><span data-stu-id="03eb9-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="03eb9-178">Tam ir jābūt uzņēmumam, kuram juridiskās personas iestatījumos ir atlasīta opcija **Lietot finanšu korekciju procesā**.</span><span class="sxs-lookup"><span data-stu-id="03eb9-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="03eb9-179">Ja nepieciešams, varat iestatīt datumu, kurā šī korekciju kārtula kļūst aktīva un kurā tās darbība beidzas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="03eb9-180">Ja vēlaties, lai tā būtu pieejama korekcijas priekšlikuma procesā, tad opcija **Aktīvs** ir jāiestata uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="03eb9-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="03eb9-181">Atlasiet žurnāla nosaukumu, kura tips ir **Korekcija**.</span><span class="sxs-lookup"><span data-stu-id="03eb9-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="03eb9-182">Kad pamatinformācija ir definēta, varat definēt faktiskās apstrādes kārtulas, noklikšķinot uz **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="03eb9-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="03eb9-183">Korekcijām ir divas opcijas — neto izmaiņas summas koriģēšana vai fiksētas summas definēšana.</span><span class="sxs-lookup"><span data-stu-id="03eb9-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="03eb9-184">Atlasiet savu pakalpojuma kontu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-184">Select your source account.</span></span> <span data-ttu-id="03eb9-185">Varat izmantot zvaigznīti (\*) kā aizstājzīmi.</span><span class="sxs-lookup"><span data-stu-id="03eb9-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="03eb9-186">Piemēram, 1\* kā sadalījuma datu avotu atlasītu visus kontus, kas sākas ar 1.</span><span class="sxs-lookup"><span data-stu-id="03eb9-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="03eb9-187">Kad ir atlasīti jūsu avota konti, opcija **Konta specifikācijas** nosaka kontu no izmantotā mērķa uzņēmuma.</span><span class="sxs-lookup"><span data-stu-id="03eb9-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="03eb9-188">Atlasiet vērtību **Avots**, ja vēlaties lietot to pašu galveno kontu, kurš definēts kontā **Avots**.</span><span class="sxs-lookup"><span data-stu-id="03eb9-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="03eb9-189">Ja atlasāt vērtību **Lietotāja definēts**, tad jums ir jānorāda galamērķa konts.</span><span class="sxs-lookup"><span data-stu-id="03eb9-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="03eb9-190">Dimensiju specifikācija darbojas tāpat.</span><span class="sxs-lookup"><span data-stu-id="03eb9-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="03eb9-191">Ja atlasāt vērtību **Avots**, tad mērķa uzņēmumā tiks lietotas tādas pašas dimensijas kā avota uzņēmumā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="03eb9-192">Ja atlasāt vērtību **Lietotāja definēts**, tad jums ir jānorāda dimensijas mērķa uzņēmumā, noklikšķinot uz izvēlnes vienuma **Mērķa dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="03eb9-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="03eb9-193">Atlasiet avota dimensijas un finanšu dimensijas un vērtības, kuras tiek lietotas kā korekcijas avots.</span><span class="sxs-lookup"><span data-stu-id="03eb9-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="03eb9-194">Korekcijas transakciju apstrāde</span><span class="sxs-lookup"><span data-stu-id="03eb9-194">Process elimination transactions</span></span>
<span data-ttu-id="03eb9-195">Korekciju transakcijas var apstrādāt divos veidos — kamēr notiek konsolidēšana tiešsaistē vai izveidojot korekciju žurnālu un izpildot korekciju priekšlikuma procesu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="03eb9-196">Šajā sadaļā galvenā uzmanība ir vērsta uz žurnāla izveidošanu un korekcijas procesa izpildi.</span><span class="sxs-lookup"><span data-stu-id="03eb9-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="03eb9-197">Ja kāds uzņēmums ir definēts kā korekcijas uzņēmums, tad modulī Konsolidācijas atlasiet vienumu **Korekciju žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="03eb9-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="03eb9-198">Pēc žurnāla nosaukuma atlasīšanas noklikšķiniet uz **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="03eb9-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="03eb9-199">Priekšlikumu varat palaist, atlasot izvēlni **Priekšlikumi** un pēc tam atlasot vienumu **Korekcijas priekšlikums**.</span><span class="sxs-lookup"><span data-stu-id="03eb9-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="03eb9-200">Atlasiet uzņēmumu, kurš ir konsolidēto datu avots, un pēc tam izvēlieties kārtulu, kuru vēlaties apstrādāt.</span><span class="sxs-lookup"><span data-stu-id="03eb9-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="03eb9-201">Ievadiet sākuma datumu, kad sākt meklēt korekcijas summas, un beigu datumu, kad beigt meklēt korekcijas summas.</span><span class="sxs-lookup"><span data-stu-id="03eb9-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="03eb9-202">Lauks **VG grāmatošanas datums** ir datums, kurš tiek izmantots žurnāla grāmatošanai virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="03eb9-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="03eb9-203">Kad noklikšķināt uz **Labi**, varat pārskatīt summas un grāmatot šo žurnālu.</span><span class="sxs-lookup"><span data-stu-id="03eb9-203">After you click **OK**, you can review the amounts and post the journal.</span></span>



