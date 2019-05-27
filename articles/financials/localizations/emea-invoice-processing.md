---
title: Rēķina apstrāde
description: Šajā tēmā ir sniegta informācija par rēķinu apstrādāšanu Austrumeiropas valstīm.
author: v-kikozl
manager: AnnBe
ms.date: 07/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, VendParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-kikozl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 7b8279531d932a1c3cac75d2f72766475465345a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538161"
---
# <a name="invoice-processing"></a><span data-ttu-id="4de5b-103">Rēķina apstrāde</span><span class="sxs-lookup"><span data-stu-id="4de5b-103">Invoice processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4de5b-104">Šajā tēmā ir īsi aprakstīti daži valstij specifiskie scenāriji, piemēram, Eiropas Kopienas iekšējais pievienotās vērtības nodoklis (PVN) un atliktais nodoklis.</span><span class="sxs-lookup"><span data-stu-id="4de5b-104">This topic briefly describes some country-specific scenarios, such as intra-community value-added tax (VAT) and deferred tax.</span></span> <span data-ttu-id="4de5b-105">Rēķinu izrakstīšanas procesu ietekmē dažās Eiropas valstīs pastāvošās juridiskās prasības.</span><span class="sxs-lookup"><span data-stu-id="4de5b-105">Legal requirements for some European countries affect the invoicing process.</span></span> <span data-ttu-id="4de5b-106">Šajā tēmā ir sniegta arī informācija par to, kā šīm valstīm tiek apstrādāti debitoru un kreditoru rēķini.</span><span class="sxs-lookup"><span data-stu-id="4de5b-106">This topic provides also an information about how customer and vendor invoices are processed for these countries.</span></span> 
<table>
<thead>
<tr>
<th><span data-ttu-id="4de5b-107">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="4de5b-107">Scenario</span></span></th>
<th><span data-ttu-id="4de5b-108">Valstis</span><span class="sxs-lookup"><span data-stu-id="4de5b-108">Countries</span></span></th>
<th><span data-ttu-id="4de5b-109">Funkcionalitātes izmaiņu apraksts</span><span class="sxs-lookup"><span data-stu-id="4de5b-109">Description of the functionality changes</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4de5b-110">Debitoru un kreditoru PVN datumi</span><span class="sxs-lookup"><span data-stu-id="4de5b-110">Accounts receivable and Accounts payable dates for VAT</span></span></td>
<td><span data-ttu-id="4de5b-111">Čehija, Polija</span><span class="sxs-lookup"><span data-stu-id="4de5b-111">Czech Republic, Poland</span></span></td>
<td>
<p><span data-ttu-id="4de5b-112">Kad preces tiek iegādātas no Eiropas Savienības (ES) valstīm, ir pienākums veikt PVN pašnovērtējumu:</span><span class="sxs-lookup"><span data-stu-id="4de5b-112">When goods are purchased from European Union (EU) countries, there is an obligation of self-assessment of VAT:</span></span></p>
<ul>
<li><span data-ttu-id="4de5b-113">Pārdošanas PVN ir jāmaksā tajā PVN periodā, kad rēķins tika izrakstīts (dokumenta datumā).</span><span class="sxs-lookup"><span data-stu-id="4de5b-113">The output VAT must be paid in a VAT period where the invoice was issued (document date).</span></span></li>
<li><span data-ttu-id="4de5b-114">Pirkšanas PVN nevar atskaitīt pirms dokumenta saņemšanas (PVN reģistra datuma).</span><span class="sxs-lookup"><span data-stu-id="4de5b-114">The input VAT can’t be deducted before the document receipt (VAT register date).</span></span></li>
</ul>
<p><span data-ttu-id="4de5b-115">Lai atbalstītu šo scenāriju, ir jābūt konfigurētiem tālāk norādītajiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="4de5b-115">The following settings should be configured to support this scenario:</span></span></p>
<ul>
<li><span data-ttu-id="4de5b-116">Lapā <strong>Kreditoru parādu parametri</strong> iespējojiet parametru <strong>EK iekšējais PVN</strong> un <strong>EK iekšējā PVN dokumenta datums</strong>.</span><span class="sxs-lookup"><span data-stu-id="4de5b-116">On the <strong>Accounts payable parameters</strong> page, enable the <strong>Intra-community VAT</strong> and <strong>Document date for intra-community VAT</strong> parameters.</span></span></li>
<li><span data-ttu-id="4de5b-117">Iestatiet divus PVN kodus — vienu, kam ir pozitīva PVN likme, un vienu, kam ir negatīva PVN likme.</span><span class="sxs-lookup"><span data-stu-id="4de5b-117">Set up two sales tax codes, one that has a positive sales tax percentage and one that has a negative sales tax percentage.</span></span></li>
<li><span data-ttu-id="4de5b-118">Iestatiet PVN grupu, kas ietver gan pozitīvo, gan negatīvo PVN kodu.</span><span class="sxs-lookup"><span data-stu-id="4de5b-118">Set up a sales tax group that includes both the positive and negative sales tax codes.</span></span> <span data-ttu-id="4de5b-119">Negatīvajam PVN kodam parametru <strong>EK iekšējais PVN</strong> iestatiet uz <strong>Jā</strong>.</span><span class="sxs-lookup"><span data-stu-id="4de5b-119">For the negative sales tax code, set the <strong>Intracommunity VAT</strong> parameter to <strong>Yes</strong>.</span></span></li>
</ul>
<p><span data-ttu-id="4de5b-120">Pēc sekmīgas iestatīšanas pirkumiem būs divas grāmatotās PVN transakcijas:</span><span class="sxs-lookup"><span data-stu-id="4de5b-120">After successful setup, purchases will have two posted sales tax transactions:</span></span></p>
<ul>
<li><span data-ttu-id="4de5b-121">Pozitīva transakcija, kuras virziens ir <strong>saņemamais PVN</strong> un kuras PVN reģistra datums ir vienāds ar datumu no rēķina grāmatošanas lapas.</span><span class="sxs-lookup"><span data-stu-id="4de5b-121">A positive transaction that has a direction of <strong>sales tax receivable</strong> and a VAT register date that equals the date from the invoice posting page.</span></span></li>
<li><span data-ttu-id="4de5b-122">Negatīva transakcija, kuras virziens ir <strong>maksājamais PVN</strong> un kuras PVN reģistra datums ir vienāds ar dokumenta datumu.</span><span class="sxs-lookup"><span data-stu-id="4de5b-122">A negative transaction that has a direction of <strong>sales tax payable</strong> and a VAT register date that equals the document date.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4de5b-123">Modificējiet pārdošanas dokumenta datumu.</span><span class="sxs-lookup"><span data-stu-id="4de5b-123">Modify a sales document date.</span></span></td>
<td><span data-ttu-id="4de5b-124">Visas Austrumeiropas valstis</span><span class="sxs-lookup"><span data-stu-id="4de5b-124">All Eastern European countries</span></span></td>
<td><p><span data-ttu-id="4de5b-125">Projekta rēķinā varat modificēt lauku <strong>Dokumenta datums</strong>.</span><span class="sxs-lookup"><span data-stu-id="4de5b-125">You can modify the <strong>Document date</strong> field on a project invoice.</span></span> <span data-ttu-id="4de5b-126">Šis datums ir redzams izdrukātajā rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4de5b-126">This date appears on the printed invoice.</span></span></p>
<p><span data-ttu-id="4de5b-127">Lauks <strong>Dokumenta datums</strong> ir arī lapā <strong>Rēķina grāmatošana</strong> un <strong>Brīva teksta rēķins</strong>.</span><span class="sxs-lookup"><span data-stu-id="4de5b-127">There is also a <strong>Document date</strong> field on the <strong>Posting invoice</strong> and <strong>Free text invoice</strong> pages.</span></span> <span data-ttu-id="4de5b-128">Pēc rēķina grāmatošanas dokumenta datums ir redzams rēķina virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="4de5b-128">After you post an invoice, the document date appears on the invoice header.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="4de5b-129">Dokumenta datums valūtas maiņas kursiem</span><span class="sxs-lookup"><span data-stu-id="4de5b-129">Document date for exchange rates</span></span></td>
<td><span data-ttu-id="4de5b-130">Polija, Ungārija, Čehija</span><span class="sxs-lookup"><span data-stu-id="4de5b-130">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="4de5b-131">Likumdošana paredz atšķirīgus noteikumus komercdarbības transakciju derīgu valūtas maiņas kursu atlasīšanai.</span><span class="sxs-lookup"><span data-stu-id="4de5b-131">Legislation provides different rules for selecting valid exchange rates for business transactions.</span></span> <span data-ttu-id="4de5b-132">Laukā <strong>Maiņas kursa datums</strong> lapā <strong>Debitoru parādu parametri</strong> un <strong>Parādu kreditoriem parametri</strong> varat atlasīt datumu, kas pirkumu un pārdošanas dokumentiem ir jāizmanto summām uzskaites valūtas aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="4de5b-132">In the <strong>Exchange rate date</strong> field on the <strong>Accounts receivable parameters</strong> and <strong>Accounts payable parameters</strong> pages, you can select the date that should be used for amounts in the accounting currency calculation on purchase and sales documents.</span></span> <span data-ttu-id="4de5b-133">Datu ievadīšanas laikā sistēma izgūst transakcijas valūtas maiņas kursu, pamatojoties uz šo parametru.</span><span class="sxs-lookup"><span data-stu-id="4de5b-133">During data entry, the system retrieves the exchange rate for the transaction, based on this parameter.</span></span></p>
<blockquote>[!NOTE]<br><span data-ttu-id="4de5b-134">Ja lauku <strong>Maiņas kursa datums</strong> iestatāt uz <strong>Dokumenta datums (tikai ES tirdzniecība)</strong>, tad sistēma izmanto PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="4de5b-134">When you set the <strong>Exchange rate date</strong> field to <strong>Document date (for EU trade only)</strong>, the system uses the sales tax group.</span></span> <span data-ttu-id="4de5b-135">PVN grupai cilnē <strong>Vispārīgi</strong> pastāv parametrs <strong>ES tirdzniecība</strong>. Ja opcija <strong>ES tirdzniecība</strong> PVN grupai ir pārslēgta uz <strong>Jā</strong> un ja šī PVN grupa pastāv dokumenta virsrakstā, tad valūtas maiņas kursu sistēma izgūst, pamatojoties uz dokumenta datumu.</span><span class="sxs-lookup"><span data-stu-id="4de5b-135">For the sales tax group, there is a <strong>EU trade</strong> parameter on the <strong>General</strong> tab. If the <strong>EU trade</strong> option is set to <strong>Yes</strong> for the sales tax group, and if this sales tax group exists on the header of the document, the system retrieves the exchange rate based on the document date.</span></span> <span data-ttu-id="4de5b-136">Ja opcija <strong>ES tirdzniecība</strong> šai PVN grupai ir iestatīta uz <strong>Nē</strong>, tad valūtas maiņas kursu sistēma izgūst, pamatojoties uz dokumenta grāmatošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="4de5b-136">If the <strong>EU trade</strong> option is set to <strong>No</strong> for this sales tax group, the system retrieves the exchange rate based on the posting date of the document.</span></span></blockquote>
</td>
</tr>
<tr>
<td><span data-ttu-id="4de5b-137">Darījumu veikšanas datumi, PVN reģistra datumi un dokumentu un PVN datuma kontrole</span><span class="sxs-lookup"><span data-stu-id="4de5b-137">Trade dates, VAT register dates, and document and VAT date control</span></span></td>
<td><span data-ttu-id="4de5b-138">Polija, Ungārija, Čehija</span><span class="sxs-lookup"><span data-stu-id="4de5b-138">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="4de5b-139">Pārdošanas datums un dokumenta saņemšanas datums PVN pārskatiem ir jānorāda obligāti.</span><span class="sxs-lookup"><span data-stu-id="4de5b-139">The sales date and the document receipt date are required for VAT reporting:</span></span></p>
<ul>
<li><span data-ttu-id="4de5b-140">Pārdošanas datums ir transakcijas izpildes datums debitoru parādos.</span><span class="sxs-lookup"><span data-stu-id="4de5b-140">The sales date is the fulfilment date of the transaction in Accounts receivable.</span></span></li>
<li><span data-ttu-id="4de5b-141">Dokumentu saņemšanas datums ir datums, kas apliecina tiesības pieprasīt PVN samazinājumu debitoru parādos.</span><span class="sxs-lookup"><span data-stu-id="4de5b-141">The document receipt date is a date that demonstrates the rights to claim a VAT deduction in Accounts payable.</span></span> <span data-ttu-id="4de5b-142">Katram saņemtajam dokumentam ir datums, kuru izmantot auditēšanas nolūkos.</span><span class="sxs-lookup"><span data-stu-id="4de5b-142">Each document that is received has a date for audit purposes.</span></span></li>
</ul>
<p><span data-ttu-id="4de5b-143">Ungārijas funkcionalitāte datumu termiņiem, Čehijas funkcionalitāte izpildes datumiem un Polijas funkcionalitāte PVN reģistra datumam ietver prasību par nodokļu informācijas ziņošanu, kas ir balstīta uz datumu, kurš atšķiras no grāmatošanas datuma.</span><span class="sxs-lookup"><span data-stu-id="4de5b-143">The Hungarian functionality for date deadlines, the Czech Republic functionality for fulfill dates, and the Polish functionality for the VAT register date include the requirement for tax information reporting that is based on a date that differs from the posting date.</span></span></p>
<p><span data-ttu-id="4de5b-144">Lauks <strong>PVN reģistra datums</strong> atbalsta šo prasību, un tas ir redzams vairāk nekā 20 lapās.</span><span class="sxs-lookup"><span data-stu-id="4de5b-144">The <strong>Date of VAT register</strong> field supports this requirement and appears on more than 20 pages.</span></span> <span data-ttu-id="4de5b-145">Šīs lapas ietver žurnālus, pārdošanas pasūtījumus, pirkšanas pasūtījumus, brīva teksta rēķinus, kreditoru rēķinu žurnālus un projektu rēķinus.</span><span class="sxs-lookup"><span data-stu-id="4de5b-145">These pages include journals, sales orders, purchase orders, free-text invoices, vendor invoice journals, and project invoices.</span></span> <span data-ttu-id="4de5b-146">Atjauninot vai grāmatojot dokumentus, visi nodokļi tiek grāmatoti, izmantojot atbilstošo PVN reģistra datumu, un datums tiek ietverts tādās lapās kā, piemēram, debitoru un kreditoru rēķinu žurnālu lapas.</span><span class="sxs-lookup"><span data-stu-id="4de5b-146">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date is included on pages such as the customer and vendor invoice journals pages.</span></span></p>
<p><span data-ttu-id="4de5b-147">Čehijai lauks <strong>PVN reģistra datums</strong> grāmatošanas laikā var būt tukšs, ja tiek grāmatots atliktais PVN.</span><span class="sxs-lookup"><span data-stu-id="4de5b-147">Specifically, for the Czech Republic, the <strong>VAT register date</strong> field can be blank during posting, in the event of postponed VAT posting.</span></span> <span data-ttu-id="4de5b-148">Pretējā gadījumā šis lauks ir obligāts, un tas ir jāaizpilda.</span><span class="sxs-lookup"><span data-stu-id="4de5b-148">Otherwise, the field is mandatory and must be filled in.</span></span></p>
<p><span data-ttu-id="4de5b-149">Datuma validēšanas parametrus var iestatīt lapā <strong>PVN grupas</strong>.</span><span class="sxs-lookup"><span data-stu-id="4de5b-149">Date validation parameters can be set on the <strong>Sales tax groups</strong> page:</span></span></p>
<ul>
<li><span data-ttu-id="4de5b-150">Parametrs <strong>PVN reģistra aizpildīšanas datums</strong> un <strong>Pārdošanas datuma aizpildīšana</strong> tiek izmantots kā noklusējuma aizpildīšanas metode atbilstošajiem datumiem.</span><span class="sxs-lookup"><span data-stu-id="4de5b-150">The <strong>Date of VAT register filling</strong> and <strong>Sales date filling</strong> parameters are used as a default filling method for appropriate dates.</span></span> <span data-ttu-id="4de5b-151">Ir pieejama arī manuāla ievade un vairākas automatizētas ievades metodes.</span><span class="sxs-lookup"><span data-stu-id="4de5b-151">Manual input and several automated input methods are also available.</span></span></li>
<li><span data-ttu-id="4de5b-152">Lauks <strong>Obligātais pārdošanas datums</strong> norāda, vai pārdošanas datums ir jāievada pirms pārdošanas rēķina grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="4de5b-152">The <strong>Mandatory sales date</strong> field indicates whether the sales date must be entered before a sales invoice is posted.</span></span></li>
</ul>
<p><span data-ttu-id="4de5b-153">Lapā <strong>PVN reģistra transakcijas</strong> varat aizpildīt tukšos datumus, kas PVN reģistram paredzēti grāmatotajām nodokļu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="4de5b-153">On the <strong>VAT Register transactions</strong> page, you can fill in blank dates for the VAT register for posted tax transactions.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="4de5b-154">PVN reģistra datumi, kas ietver atlikto nodokli</span><span class="sxs-lookup"><span data-stu-id="4de5b-154">VAT register dates that include deferred tax</span></span></td>
<td><span data-ttu-id="4de5b-155">Ungārija</span><span class="sxs-lookup"><span data-stu-id="4de5b-155">Hungary</span></span></td>
<td>
<p><span data-ttu-id="4de5b-156">Ungārijas nodokļu noteikumi paredz, ka rēķini ir jāizveido vai nu izpildes laikā, vai ne vēlāk kā 15 dienas pēc izpildes.</span><span class="sxs-lookup"><span data-stu-id="4de5b-156">Hungary tax regulations require that invoices be created at either the time of fulfilment or no later than 15 days after fulfilment.</span></span></p>
<p><span data-ttu-id="4de5b-157">Izpildes datums ir datums, kad tika sniegti pasūtītie pakalpojumi, vai datums, kad tika piegādāti pasūtītie krājumi.</span><span class="sxs-lookup"><span data-stu-id="4de5b-157">The fulfilment date is either the date when the ordered services were provided or the date when ordered items were delivered.</span></span> <span data-ttu-id="4de5b-158">Kad atjaunināt vai grāmatojat dokumentus, visi nodokļi tiek grāmatoti, izmantojot atbilstošo PVN reģistra datumu, un šis datums tiek rādīts saistītajās lapās.</span><span class="sxs-lookup"><span data-stu-id="4de5b-158">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date appears on relevant pages.</span></span> <span data-ttu-id="4de5b-159">Turklāt noteikumi pieprasa, lai PVN par pastāvīgi piegādātajiem pakalpojumiem, piemēram, īri, nomu, konsultācijām un apkuri, atbilstu tālāk norādītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="4de5b-159">Additionally, regulations require that VAT on continuous delivery of services, such as renting, leasing, consulting, and heating, meet the following criteria:</span></span></p>
<ul>
<li><span data-ttu-id="4de5b-160">PVN ir jāgrāmato speciālā virsgrāmatas kontā un rēķina datumā.</span><span class="sxs-lookup"><span data-stu-id="4de5b-160">VAT must be posted to a dedicated general ledger account on the invoice date.</span></span></li>
<li><span data-ttu-id="4de5b-161">PVN no speciālajiem kontiem ir jāpārsūta uz saņemamā PVN kontu vai uz maksājamā PVN kontu, un apmaksas datumā tas ir jāietver PVN pārskatā.</span><span class="sxs-lookup"><span data-stu-id="4de5b-161">VAT must be transferred from the special accounts to a sales tax receivable account or a payable account, and must be included in the VAT report on the due date.</span></span></li>
</ul>
<p><span data-ttu-id="4de5b-162">Lai atbalstītu šīs prasības, virsgrāmatas grāmatojumus varat pārsūtīt uz atliktā ienākošā nodokļa kontu un atliktā izejošā nodokļa kontu.</span><span class="sxs-lookup"><span data-stu-id="4de5b-162">To support these requirements, you can transfer General ledger postings to the Deferred incoming tax account and the Deferred outgoing tax account.</span></span> <span data-ttu-id="4de5b-163">Taču vispirms ir jāizpilda tālāk norādītie priekšnosacījumi.</span><span class="sxs-lookup"><span data-stu-id="4de5b-163">However, you must first complete the following prerequisites:</span></span></p>
<ul>
<li><span data-ttu-id="4de5b-164">Virsgrāmatas grāmatošanas grupās iestatiet virsgrāmatas kontu Atliktais maksājamais PVN un Atliktais saņemamais PVN.</span><span class="sxs-lookup"><span data-stu-id="4de5b-164">Set up the Deferred VAT Payable and Deferred VAT Receivable ledger accounts in ledger posting groups.</span></span></li>
<li><span data-ttu-id="4de5b-165">Iespējojiet parametru <strong>Atliktais PVN</strong> attiecībā uz krājumu PVN grupām.</span><span class="sxs-lookup"><span data-stu-id="4de5b-165">Enable the <strong>Deferred VAT</strong> parameter for item sales tax groups.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4de5b-166">Obligātais PVN datums</span><span class="sxs-lookup"><span data-stu-id="4de5b-166">Mandatory VAT date</span></span></td>
<td><span data-ttu-id="4de5b-167">Polija</span><span class="sxs-lookup"><span data-stu-id="4de5b-167">Poland</span></span></td>
<td>
<p><span data-ttu-id="4de5b-168">Varat pieprasīt, lai PVN reģistra datums tiktu ietverts pirkšanas un pārdošanas transakciju ierakstos.</span><span class="sxs-lookup"><span data-stu-id="4de5b-168">You can require that the date of the VAT register be included in purchase and sales transaction records.</span></span> <span data-ttu-id="4de5b-169">Tāpēc PVN reģistra datumu var iegūt pirms transakcijas grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="4de5b-169">Therefore, the date of the VAT register can be captured before a transaction is posted.</span></span> <span data-ttu-id="4de5b-170">Šī funkcionalitāte jums palīdz izvairīties no vairāku transakciju apstrādes perioda beigās.</span><span class="sxs-lookup"><span data-stu-id="4de5b-170">This functionality helps you avoid having to handle multiple transactions at the end of the period.</span></span></p>
<p><span data-ttu-id="4de5b-171">Lauku <strong>PVN reģistra datums</strong> varat padarīt par obligātu, kad tiek grāmatotas debitoru vai kreditoru transakcijas.</span><span class="sxs-lookup"><span data-stu-id="4de5b-171">You can make the <strong>Date of VAT register</strong> field mandatory when customer or vendor transactions are posted.</span></span> <span data-ttu-id="4de5b-172">Lai šo lauku padarītu par obligātu, saistītajam debitora vai kreditora kontam aktivizējiet opciju <strong>Nepieciešams PVN datums</strong>.</span><span class="sxs-lookup"><span data-stu-id="4de5b-172">To make this field mandatory, enable the <strong>VAT date is required</strong> option for the related customer or vendor account.</span></span></p>
</td>
</tr>
</tbody>
</table>
