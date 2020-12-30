---
title: Mazie kases posteņi Austrumeiropai un Krievijai
description: Šajā tēmā ir sniegta informācija par mazo kases posteņu funkcionalitāti, kas lietotājiem Igaunijā, Lietuvā, Čehijā, Ungārijā, Latvijā, Polijā un Krievijā ļauj sistēmā atainot kases operācijas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 268504
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 890300d1251b2befce47f62535f44771378f3cb7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408291"
---
# <a name="petty-cash-for-eastern-europe-and-russia"></a><span data-ttu-id="22b02-103">Mazie kases posteņi Austrumeiropai un Krievijai</span><span class="sxs-lookup"><span data-stu-id="22b02-103">Petty cash for Eastern Europe and Russia</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22b02-104">Šajā tēmā ir sniegta informācija par mazo kases posteņu funkcionalitāti, kas lietotājiem Igaunijā, Lietuvā, Čehijā, Ungārijā, Latvijā, Polijā un Krievijā ļauj sistēmā atainot kases operācijas.</span><span class="sxs-lookup"><span data-stu-id="22b02-104">This topic provides information about the petty cash functionality that lets users in Estonia, Lithuania, Czech Republic, Hungary, Latvia, Poland, and Russia reflect cash operations in the system.</span></span>

<span data-ttu-id="22b02-105">Mazo kases posteņu funkcionalitāti varat izmantot, lai automatizētu kases operācijas ieņēmumiem un izdevumiem, primāro dokumentu veidošanai un saistīto pārskatu drukāšanai.</span><span class="sxs-lookup"><span data-stu-id="22b02-105">You can use the petty cash functionality to automate operations for receipts and expenditures of cash, the creation of primary documents, and the printing of related reports.</span></span> <span data-ttu-id="22b02-106">Mazo kases posteņu funkcionalitāte jums ļauj veikt tālāk minētās operācijas.</span><span class="sxs-lookup"><span data-stu-id="22b02-106">The petty cash functionality lets you perform the following operations:</span></span>

-   <span data-ttu-id="22b02-107">Uzskaitīt pieejamo kases līdzekļu ieņēmumus un izdevumus.</span><span class="sxs-lookup"><span data-stu-id="22b02-107">Account the receipt and expenditure of available cash assets.</span></span>
-   <span data-ttu-id="22b02-108">Ģenerēt tipiskās kases formas: kases ieņēmumu orderus, kases izdevumu orderus un reģistrācijas žurnālu kases orderiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-108">Generate typical cash forms: Cash reimbursement slips, Cash disbursement slips, and a Journal of registration for cash slips.</span></span>
-   <span data-ttu-id="22b02-109">Kontrolēt maksimālo skaidras naudas summu, kas ir atļauta operācijām ar debitoriem, kreditoriem un tamlīdzīgi.</span><span class="sxs-lookup"><span data-stu-id="22b02-109">Control the maximum cash amount that is allowed for operations with customers, vendors, and so on.</span></span>
-   <span data-ttu-id="22b02-110">Sistēmā kases operācijas atainot dažādās valūtās.</span><span class="sxs-lookup"><span data-stu-id="22b02-110">Reflect cash operations in various currencies in the system.</span></span>
-   <span data-ttu-id="22b02-111">Ārvalstu valūtā veikto kases operāciju summas konvertēt uz noklusējuma valūtu, lai varētu veidot uzskaites pārskatus.</span><span class="sxs-lookup"><span data-stu-id="22b02-111">Convert the amounts of cash operations in foreign currency to the default currency to provide accounting reporting.</span></span>
-   <span data-ttu-id="22b02-112">Ģenerēt pārskatu **Kases grāmata** un kasiera pārskatu.</span><span class="sxs-lookup"><span data-stu-id="22b02-112">Generate a **Cash book** report and a cashier’s report.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="22b02-113">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="22b02-113">Prerequisites</span></span>
<span data-ttu-id="22b02-114">Pirms sākat varat izmantot mazo kases posteņu funkcionalitāti, ir jāizpilda tālāk minētie priekšnosacījumi.</span><span class="sxs-lookup"><span data-stu-id="22b02-114">Before you can use the petty cash functionality, you must complete the following prerequisites:</span></span>

-   <span data-ttu-id="22b02-115">Iestatiet kases kontus.</span><span class="sxs-lookup"><span data-stu-id="22b02-115">Set up cash accounts.</span></span>
-   <span data-ttu-id="22b02-116">Iestatiet kases grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="22b02-116">Set up cash posting profiles.</span></span>
-   <span data-ttu-id="22b02-117">Iestatiet numuru sērijas kases dokumentu numurēšanai.</span><span class="sxs-lookup"><span data-stu-id="22b02-117">Set up number sequences for cash document numbering.</span></span>
-   <span data-ttu-id="22b02-118">Iestatiet noklusējuma vērtības kases un bankas vadības parametriem.</span><span class="sxs-lookup"><span data-stu-id="22b02-118">Set up default values for Cash and bank management parameters.</span></span>
-   <span data-ttu-id="22b02-119">Iestatiet kases žurnālu nosaukumus virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="22b02-119">Set up cash journal names in General ledger.</span></span>

### <a name="set-up-cash-accounts"></a><span data-ttu-id="22b02-120">Iestatīt kases kontus</span><span class="sxs-lookup"><span data-stu-id="22b02-120">Set up cash accounts</span></span>

<span data-ttu-id="22b02-121">Lai iestatītu kontu Kase, atveriet sadaļu **Kases un bankas vadība** &gt; **Bankas konti** &gt; **Kases konti** un ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-121">To set up a Cash, open **Cash and bank management** &gt; **Bank accounts** &gt; **Cash accounts**, and enter the following information.</span></span>

| <span data-ttu-id="22b02-122">Lauks</span><span class="sxs-lookup"><span data-stu-id="22b02-122">Field</span></span>                 | <span data-ttu-id="22b02-123">Apraksts</span><span class="sxs-lookup"><span data-stu-id="22b02-123">Description</span></span>                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b02-124">Kase</span><span class="sxs-lookup"><span data-stu-id="22b02-124">Cash</span></span>                  | <span data-ttu-id="22b02-125">Ievadiet kodu, ar ko identificēt šo kases kontu (kasi).</span><span class="sxs-lookup"><span data-stu-id="22b02-125">Enter a code to identify the cash account (cash).</span></span>                                                                    |
| <span data-ttu-id="22b02-126">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="22b02-126">Name</span></span>                  | <span data-ttu-id="22b02-127">Ievadiet kases konta aprakstu.</span><span class="sxs-lookup"><span data-stu-id="22b02-127">Enter a description of the cash account.</span></span>                                                                             |
| <span data-ttu-id="22b02-128">Valūta</span><span class="sxs-lookup"><span data-stu-id="22b02-128">Currency</span></span>              | <span data-ttu-id="22b02-129">Atlasiet noklusējuma valūtas kodu kases transakcijām.</span><span class="sxs-lookup"><span data-stu-id="22b02-129">Select the default currency code for cash transactions.</span></span>                                                              |
| <span data-ttu-id="22b02-130">Numuru sēriju grupa</span><span class="sxs-lookup"><span data-stu-id="22b02-130">Number sequence group</span></span> | <span data-ttu-id="22b02-131">Ja kases dokumentu numerācijai ir jāatšķiras no parametros norādītās numerācijas, ievadiet kodu.</span><span class="sxs-lookup"><span data-stu-id="22b02-131">If the numbering of cash documents must differ from the numbering that is specified in the parameters, enter a code.</span></span> |
| <span data-ttu-id="22b02-132">Dažādas valūtas</span><span class="sxs-lookup"><span data-stu-id="22b02-132">More currencies</span></span>       | <span data-ttu-id="22b02-133">Atzīmējiet šo izvēles rūtiņu, lai ļautu grāmatot valūtas, kas atšķiras no uzskaites valūtas.</span><span class="sxs-lookup"><span data-stu-id="22b02-133">Select this check box to allow currencies that differ from the accounting currency to be posted.</span></span>                     |
| <span data-ttu-id="22b02-134">Negatīvs atlikums kasē</span><span class="sxs-lookup"><span data-stu-id="22b02-134">Negative cash</span></span>         | <span data-ttu-id="22b02-135">Atzīmējiet šo izvēles rūtiņu, lai ļautu izmantot negatīvas kases bilances jebkurā valūtā.</span><span class="sxs-lookup"><span data-stu-id="22b02-135">Select this check box to allow negative cash balances in any currency.</span></span>                                               |

<span data-ttu-id="22b02-136">Lai kādam kases kontam iestatītu kases bilances kontroles kārtulas, atlasiet kases kontu un pēc tam darbību rūtī, cilnē **Kases konts**, grupā **Atlikuma limits** noklikšķiniet uz **Atlikuma limits**.</span><span class="sxs-lookup"><span data-stu-id="22b02-136">To set up cash balance control rules for a cash account, select the cash account, and then, on the Action Pane, on the **Cash account** tab, in the **Balance limit** group, click **Balance limit**.</span></span> <span data-ttu-id="22b02-137">Ievadiet tālāk aprakstīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-137">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22b02-138">Lauks</span><span class="sxs-lookup"><span data-stu-id="22b02-138">Field</span></span></th>
<th><span data-ttu-id="22b02-139">Apraksts</span><span class="sxs-lookup"><span data-stu-id="22b02-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22b02-140">Valūtas tips</span><span class="sxs-lookup"><span data-stu-id="22b02-140">Currency type</span></span></td>
<td><span data-ttu-id="22b02-141">Atlasiet valūtas tipu no tālāk uzskaitītajiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-141">Select the type of currency:</span></span>
<ul>
<li><span data-ttu-id="22b02-142"><strong>Uzskaites valūta</strong> — izmantot uzņēmuma pamata valūtas kodu.</span><span class="sxs-lookup"><span data-stu-id="22b02-142"><strong>Accounting currency</strong> – Use the basic company currency code.</span></span></li>
<li><span data-ttu-id="22b02-143"><strong>Norādītā valūta</strong> — izmantot valūtas kodu, kas atšķiras no uzņēmuma pamata valūtas koda.</span><span class="sxs-lookup"><span data-stu-id="22b02-143"><strong>Indicated currency</strong> – Use a currency code that differs from the basic company currency code.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-144">Valūta</span><span class="sxs-lookup"><span data-stu-id="22b02-144">Currency</span></span></td>
<td><span data-ttu-id="22b02-145">Ja laukā <strong>Valūtas tips</strong> atlasījāt vērtību <strong>Norādītā valūta</strong>, tad atlasiet kādu valūtas kodu.</span><span class="sxs-lookup"><span data-stu-id="22b02-145">If you selected <strong>Indicated currency</strong> in the <strong>Currency type</strong> field, select a currency code.</span></span> <span data-ttu-id="22b02-146">Šis lauks ir nepieejams, ja laukā <strong>Valūtas tips</strong> atlasījāt vērtību <strong>Uzskaites valūta</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-146">This field is unavailable if you selected <strong>Accounting currency</strong> in the <strong>Currency type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-147">Atlikuma limita veids</span><span class="sxs-lookup"><span data-stu-id="22b02-147">Balance limit type</span></span></td>
<td><span data-ttu-id="22b02-148">Atlasiet vienu no tālāk aprakstītajām pieejamajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="22b02-148">Select one of the available values:</span></span>
<ul>
<li><span data-ttu-id="22b02-149"><strong>Maksimums</strong> — šim kases kontam kases atlikums nedrīkst pārsniegt summu <strong>Atlikuma limits</strong> (augstākā vērtība).</span><span class="sxs-lookup"><span data-stu-id="22b02-149"><strong>Maximum</strong> – The cash balance should not be allowed to exceed the <strong>Balance limit</strong> amount for the cash account (upper bound).</span></span></li>
<li><span data-ttu-id="22b02-150"><strong>Minimums</strong> — šim kases kontam kases atlikums nedrīkst būt zemāks par summu <strong>Atlikuma limits</strong> (zemākā vērtība).</span><span class="sxs-lookup"><span data-stu-id="22b02-150"><strong>Minimum</strong> – The cash balance should not be allowed to go below the <strong>Balance limit</strong> amount for the cash account (bottom bound).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-151">Pārbaudīt atlikuma limitu</span><span class="sxs-lookup"><span data-stu-id="22b02-151">Check balance limit</span></span></td>
<td><span data-ttu-id="22b02-152">No nākamajām opcijām atlasiet, kas kases dokumentiem notiek apstiprināšanas procesa laikā, ja šim kases kontam tiek pārsniegta summa <strong>Atlikuma limits</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-152">Select what occurs during the approval process for cash documents if the <strong>Balance limit</strong> amount for the cash account is exceeded:</span></span>
<ul>
<li><span data-ttu-id="22b02-153"><strong>Pieņemt</strong> — limits var tikt pārsniegts.</span><span class="sxs-lookup"><span data-stu-id="22b02-153"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="22b02-154"><strong>Brīdinājums</strong> — limits var tikt pārsniegts, bet lietotājam tiek parādīts brīdinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="22b02-154"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="22b02-155">Kases dokuments tiek ratificēts vai apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="22b02-155">The cash document is confirmed or approved.</span></span></li>
<li><span data-ttu-id="22b02-156"><strong>Kļūda</strong> — nedrīkst pārsniegt ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="22b02-156"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="22b02-157">Lietotājs saņem kļūdas ziņojumu, un kases dokuments netiek ratificēts vai apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="22b02-157">The user receives an error message, and the cash document isn&#39;t confirmed or approved.</span></span></li>
</ul>
<span data-ttu-id="22b02-158">Papildinformāciju par kases dokumentu apstiprināšanas procesu skatiet tālāk šīs tēmas sadaļā &quot;Kases transakciju apstiprināšana un grāmatošana&quot;.</span><span class="sxs-lookup"><span data-stu-id="22b02-158">For more information about the approval process for cash documents, see the &quot;Cash transaction approval and posting&quot; section, later in this topic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-159">Atlikuma limits</span><span class="sxs-lookup"><span data-stu-id="22b02-159">Balance limit</span></span></td>
<td><span data-ttu-id="22b02-160">Ievadiet limitu kases kontu atlikumam.</span><span class="sxs-lookup"><span data-stu-id="22b02-160">Enter a limit for the cash account balance.</span></span> <span data-ttu-id="22b02-161">Šai summai ir jābūt jūsu norādītajā valūtā.</span><span class="sxs-lookup"><span data-stu-id="22b02-161">The amount should be in the currency that you specified.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a><span data-ttu-id="22b02-162">Iestatīt kases grāmatošanas metodes</span><span class="sxs-lookup"><span data-stu-id="22b02-162">Set up cash posting profiles</span></span>

<span data-ttu-id="22b02-163">Kases grāmatošanas metodes definē grāmatojumus virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="22b02-163">Cash posting profiles define postings to the general ledger.</span></span> <span data-ttu-id="22b02-164">Lai iestatītu kases grāmatošanas metodi, dodieties uz **Kases** **un bankas pārvaldība** &gt; **Iestatīšana** &gt; **Kases grāmatošanas metodes** un atlasiet vai izveidojiet grāmatošanas metodi.</span><span class="sxs-lookup"><span data-stu-id="22b02-164">To set up a cash posting profile, go to **Cash** **and bank management** &gt; **Setup** &gt; **Cash posting profiles**, and select or create a posting profile.</span></span> <span data-ttu-id="22b02-165">Ievadiet tālāk aprakstīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-165">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22b02-166">Lauks</span><span class="sxs-lookup"><span data-stu-id="22b02-166">Field</span></span></th>
<th><span data-ttu-id="22b02-167">Apraksts</span><span class="sxs-lookup"><span data-stu-id="22b02-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22b02-168">Derīgs</span><span class="sxs-lookup"><span data-stu-id="22b02-168">Valid for</span></span></td>
<td><span data-ttu-id="22b02-169">Atlasiet, vai grāmatošanas metode attiecas uz konkrētu kases kontu vai uz visiem kases kontiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-169">Select whether the posting profile applies to a specific cash account or all cash accounts:</span></span>
<ul>
<li><span data-ttu-id="22b02-170"><strong>Tabula</strong> — ja kases kontam pastāv kāda grāmatošanas metodes rinda, tad kases transakciju grāmatošanai tiek lietota šī rinda.</span><span class="sxs-lookup"><span data-stu-id="22b02-170"><strong>Table</strong> – If there is a posting profile line for the cash account, that line is used for cash transaction posting.</span></span></li>
<li><span data-ttu-id="22b02-171"><strong>Visi</strong> — šim kases kontam nav grāmatošanas metodes rindas.</span><span class="sxs-lookup"><span data-stu-id="22b02-171"><strong>All</strong> – There is no posting profile line for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-172">Kase</span><span class="sxs-lookup"><span data-stu-id="22b02-172">Cash</span></span></td>
<td><span data-ttu-id="22b02-173">Ja laukā <strong>Derīgs</strong> atlasījāt vērtību <strong>Tabula</strong>, norādiet kases kontu.</span><span class="sxs-lookup"><span data-stu-id="22b02-173">If you selected <strong>Table</strong> in the <strong>Valid for</strong> field, specify the cash account.</span></span> <span data-ttu-id="22b02-174">Šis lauks paliek tukšs, ja laukā <strong>Derīgs</strong> atlasījāt vērtību <strong>Visi</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-174">This field remains blank if you selected <strong>All</strong> in the <strong>Valid for</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-175">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="22b02-175">Ledger account</span></span></td>
<td><span data-ttu-id="22b02-176">Ievadiet numuru virsgrāmatai, kuru šim kases kontam lietot ka summas kontu.</span><span class="sxs-lookup"><span data-stu-id="22b02-176">Enter the number of the ledger account to use as the summary account for the cash account.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a><span data-ttu-id="22b02-177">Iestatīt numuru sērijas kases dokumentiem</span><span class="sxs-lookup"><span data-stu-id="22b02-177">Set up number sequences for cash documents</span></span>

<span data-ttu-id="22b02-178">Lai iestatītu numuru sērijas kases dokumentiem, dodieties uz **Kases un bankas vadība** &gt; **Iestatīšana** &gt; **Kases un bankas vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="22b02-178">To set up number sequences for cash documents, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="22b02-179">Cilnē **Numuru sērija** norādiet numuru sēriju kodus dokumentiem **Kases ieņēmumu orderi**, **Kases izdevumu orderi**, **Kases storno dokuments** un **Valūtas pārrēķins**, un vienumam **Kases pārskata numurs**.</span><span class="sxs-lookup"><span data-stu-id="22b02-179">On the **Number sequence** tab, specify number sequence codes for the **Cash reimbursement slips**, **Cash disbursement slips**, **Cash correction voucher**, and **Exchange adjustment** documents, and for **Cash report number**.</span></span>

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a><span data-ttu-id="22b02-180">Iestatīt noklusējuma vērtības kases un bankas vadības parametriem</span><span class="sxs-lookup"><span data-stu-id="22b02-180">Set up default values for Cash and bank management parameters</span></span>

<span data-ttu-id="22b02-181">Lai iestatītu noklusējuma vērtības kases un bankas vadības parametriem mazo kases posteņu funkcionalitātei, dodieties uz **Kases un bankas vadība** &gt; **Iestatīšana** &gt; **Kases un bankas vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="22b02-181">To set up default values for Cash and bank management parameters for the petty cash functionality, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="22b02-182">Cilnē **Kase** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-182">On the **Cash** tab, enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22b02-183">Lauks</span><span class="sxs-lookup"><span data-stu-id="22b02-183">Field</span></span></th>
<th><span data-ttu-id="22b02-184">Apraksts</span><span class="sxs-lookup"><span data-stu-id="22b02-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22b02-185">Kase</span><span class="sxs-lookup"><span data-stu-id="22b02-185">Cash</span></span></td>
<td><span data-ttu-id="22b02-186">Atlasiet noklusējuma kases kontu žurnālos.</span><span class="sxs-lookup"><span data-stu-id="22b02-186">Select the default cash account in journals.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-187">Kases grāmatošana</span><span class="sxs-lookup"><span data-stu-id="22b02-187">Cash posting</span></span></td>
<td><span data-ttu-id="22b02-188">Ievadiet noklusējuma kases grāmatošanas metodi, kas tiek lietota, ja nav norādīta neviena cita grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="22b02-188">Enter the default cash posting profile that is used if no other posting profile is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-189">Dokumentu numuru kontrole</span><span class="sxs-lookup"><span data-stu-id="22b02-189">Check for voucher used</span></span></td>
<td><span data-ttu-id="22b02-190">Atlasiet, kas notiek, ja kases dokumenta pārbaudes laika tiek konstatēti numuru dublikāti.</span><span class="sxs-lookup"><span data-stu-id="22b02-190">Select what occurs if duplicate numbers are found during the check of the cash document number:</span></span>
<ul>
<li><span data-ttu-id="22b02-191">Neatļaut vienādus dokumentu numurus</span><span class="sxs-lookup"><span data-stu-id="22b02-191">Reject duplicate</span></span></li>
<li><span data-ttu-id="22b02-192">Neatļaut kopijas finanšu gada ietvaros</span><span class="sxs-lookup"><span data-stu-id="22b02-192">Reject copies within fiscal year</span></span></li>
<li><span data-ttu-id="22b02-193">Atļaut vienādus dokumentu numurus</span><span class="sxs-lookup"><span data-stu-id="22b02-193">Accept duplicates</span></span></li>
<li><span data-ttu-id="22b02-194">Brīdināt dublēšanās gadījumā</span><span class="sxs-lookup"><span data-stu-id="22b02-194">Warn in case of duplicates</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-195">Pārbaudīt operāciju limitu</span><span class="sxs-lookup"><span data-stu-id="22b02-195">Check operations limit</span></span></td>
<td><span data-ttu-id="22b02-196">Norādiet, kas notiek, ja tiek pārsniegts operācijām ar kontrahentiem noteiktais limits.</span><span class="sxs-lookup"><span data-stu-id="22b02-196">Specify what occurs if the limit for operations with counteragents is exceeded:</span></span>
<ul>
<li><span data-ttu-id="22b02-197"><strong>Pieņemt</strong> — limits var tikt pārsniegts.</span><span class="sxs-lookup"><span data-stu-id="22b02-197"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="22b02-198"><strong>Brīdinājums</strong> — limits var tikt pārsniegts, bet lietotājam tiek parādīts brīdinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="22b02-198"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="22b02-199">Šī operācija tiek grāmatota.</span><span class="sxs-lookup"><span data-stu-id="22b02-199">The operation is posted.</span></span></li>
<li><span data-ttu-id="22b02-200"><strong>Kļūda</strong> — nedrīkst pārsniegt ierobežojumu.</span><span class="sxs-lookup"><span data-stu-id="22b02-200"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="22b02-201">Lietotājs saņem kļūdas ziņojumu, un operācija netiek grāmatota.</span><span class="sxs-lookup"><span data-stu-id="22b02-201">The user receives an error message, and the operation isn&#39;t posted.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-202">Pārbaudes metode</span><span class="sxs-lookup"><span data-stu-id="22b02-202">Validation method</span></span></td>
<td><span data-ttu-id="22b02-203">Atlasiet pārbaudes metodi, kas tiek lietota, lai operācijām kontrolētu pārsniegšanas limitu summas.</span><span class="sxs-lookup"><span data-stu-id="22b02-203">Select the validation method that is used to control exceeded limit amounts for operations:</span></span>
<ul>
<li><span data-ttu-id="22b02-204"><strong>Operācija</strong> — pārbaude tiek veikta katrai transakcijai</span><span class="sxs-lookup"><span data-stu-id="22b02-204"><strong>Operation</strong> – Validation is done per transaction</span></span></li>
<li><span data-ttu-id="22b02-205"><strong>Līgums</strong> — pārbaude tiek veikta katrai transakcijai, kam ir norādīts līgums ar kontrahentu.</span><span class="sxs-lookup"><span data-stu-id="22b02-205"><strong>Agreement</strong> – Validation is done per transaction that has a specified contract with a counteragent.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-206">Operāciju limits</span><span class="sxs-lookup"><span data-stu-id="22b02-206">Operations limit</span></span></td>
<td><span data-ttu-id="22b02-207">Ievadiet maksimālo summu, kas kasē ir atļauta operācijām ar kontrahentiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-207">Enter the maximum amount that is allowed for operations with counteragents in cash.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-208">Grāmatošana agrākā datumā</span><span class="sxs-lookup"><span data-stu-id="22b02-208">Posting on earlier date</span></span></td>
<td><span data-ttu-id="22b02-209">Atzīmējiet šo izvēles rūtiņu, lai iespējotu kases transakciju grāmatošanu pirms kases transakcijas pēdējā datuma.</span><span class="sxs-lookup"><span data-stu-id="22b02-209">Select this check box to enable cash transactions to be posted before the last date of the cash transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-210">Dimensijas</span><span class="sxs-lookup"><span data-stu-id="22b02-210">Dimensions</span></span></td>
<td><span data-ttu-id="22b02-211">Ievadiet dimensijas laukos <strong>Nodaļas kods</strong>, <strong>Analītiskais kods</strong> un <strong>Mērķa kods</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-211">Enter dimensions in the <strong>Department code</strong>, <strong>Analytical code</strong>, and <strong>Purpose code</strong> fields.</span></span> <span data-ttu-id="22b02-212">Kases dokumentu drukāšanas forma atainos šo informāciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-212">The printing form for cash documents will reflect this information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-213">Lietot ratifikācijas statusu</span><span class="sxs-lookup"><span data-stu-id="22b02-213">Use confirm status</span></span></td>
<td><span data-ttu-id="22b02-214">Atzīmējiet šo izvēles rūtiņu, lai kases dokumentiem apstiprināšanas procesa laikā lietotu papildu statusu <strong>Ratificēts</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-214">Select this check box to use an additional status, <strong>Confirmed</strong>, during the approval process for cash documents.</span></span> <span data-ttu-id="22b02-215">(Papildinformāciju skatiet sadaļā &quot;Kases transakciju apstiprināšana un grāmatošana&quot;.)</span><span class="sxs-lookup"><span data-stu-id="22b02-215">(For more information, see the &quot;Cash transaction approval and posting&quot; section.)</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a><span data-ttu-id="22b02-216">Iestatīt kases žurnālu nosaukumus virsgrāmatā</span><span class="sxs-lookup"><span data-stu-id="22b02-216">Set up cash journal names in General ledger</span></span>

<span data-ttu-id="22b02-217">Lai izveidotu žurnālu kases transakciju grāmatošanai, dodieties uz **Virsgrāmata** &gt; **Žurnāla iestatīšana** &gt; **Žurnālu nosaukumi** un izveidojiet jaunu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="22b02-217">To create a journal for cash transaction posting, go to **General ledger** &gt; **Journal setup** &gt; **Journal names**, and create a new record.</span></span> <span data-ttu-id="22b02-218">Laukā **Žurnāla tips** norādiet **Kase**.</span><span class="sxs-lookup"><span data-stu-id="22b02-218">In the **Journal type** field, specify **Cash**.</span></span> <span data-ttu-id="22b02-219">Definējiet citus nepieciešamos noklusējuma žurnāla parametrus.</span><span class="sxs-lookup"><span data-stu-id="22b02-219">Define other default journal parameters as you require.</span></span>

## <a name="daily-cash-operations-via-a-slip-journal"></a><span data-ttu-id="22b02-220">Ikdienas kases operācijas, izmantojot orderu žurnālu</span><span class="sxs-lookup"><span data-stu-id="22b02-220">Daily cash operations via a Slip journal</span></span>
<span data-ttu-id="22b02-221">Lai izveidotu kases dokumentu, izmantojot orderu žurnālu, dodieties uz **Kases un bankas vadība** &gt; **Kases transakcijas** &gt; **Orderu žurnāls** un izveidojiet jaunu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="22b02-221">To create a cash document via a Slip journal, go to **Cash and bank management** &gt; **Cash transactions** &gt; **Slip journal**, and create a new journal.</span></span> <span data-ttu-id="22b02-222">Darbību rūtī noklikšķiniet uz **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="22b02-222">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="22b02-223">Pievienojiet jaunu rindu un ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-223">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22b02-224">Lauks</span><span class="sxs-lookup"><span data-stu-id="22b02-224">Field</span></span></th>
<th><span data-ttu-id="22b02-225">Apraksts</span><span class="sxs-lookup"><span data-stu-id="22b02-225">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22b02-226">Datums</span><span class="sxs-lookup"><span data-stu-id="22b02-226">Date</span></span></td>
<td><span data-ttu-id="22b02-227">Ievadiet darījuma datumu.</span><span class="sxs-lookup"><span data-stu-id="22b02-227">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-228">Konts</span><span class="sxs-lookup"><span data-stu-id="22b02-228">Account</span></span></td>
<td><span data-ttu-id="22b02-229">Atlasiet kases kontu.</span><span class="sxs-lookup"><span data-stu-id="22b02-229">Select the cash account.</span></span> <span data-ttu-id="22b02-230">Pēc noklusējuma kases konts ir norādīts sadaļā Kases un bankas vadības parametri.</span><span class="sxs-lookup"><span data-stu-id="22b02-230">By default, a cash account is specified in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-231">Apraksts</span><span class="sxs-lookup"><span data-stu-id="22b02-231">Description</span></span></td>
<td><span data-ttu-id="22b02-232">Ievadiet skaidrojošu tekstu par transakciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-232">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-233">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="22b02-233">Debit Credit</span></span></td>
<td><span data-ttu-id="22b02-234">Ievadiet kases dokumenta summu vienā no tālāk norādītajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-234">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="22b02-235"><strong>Debets</strong> — izmantojiet šo lauku, lai reģistrētu kases ieņēmumus un kases ieņēmumu orderi.</span><span class="sxs-lookup"><span data-stu-id="22b02-235"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="22b02-236"><strong>Kredīts</strong> — izmantojiet šo lauku, lai reģistrētu kases izdevumus un kases izdevumu orderi.</span><span class="sxs-lookup"><span data-stu-id="22b02-236"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-237">Korespondējošā konta tipa korespondējošais konts</span><span class="sxs-lookup"><span data-stu-id="22b02-237">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="22b02-238">Atlasiet korespondējošā konta tipu un korespondējošā konta numuru.</span><span class="sxs-lookup"><span data-stu-id="22b02-238">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-239">Valūta</span><span class="sxs-lookup"><span data-stu-id="22b02-239">Currency</span></span></td>
<td><span data-ttu-id="22b02-240">Atlasiet transakcijas valūtas kodu.</span><span class="sxs-lookup"><span data-stu-id="22b02-240">Select the code for the transaction currency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-241">Dokuments</span><span class="sxs-lookup"><span data-stu-id="22b02-241">Voucher</span></span></td>
<td><span data-ttu-id="22b02-242">Šis lauks tiek aizpildīts automātiski, pamatojoties uz žurnāla iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="22b02-242">This field is filled in automatically, based on the journal setup.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-243">Pasūtījuma numurs</span><span class="sxs-lookup"><span data-stu-id="22b02-243">Order number</span></span></td>
<td><span data-ttu-id="22b02-244">Ja šim kases kontam nav norādīta neviena cita numuru sērija, šis lauks tiek aizpildīts automātiski, pamatojoties uz parametros norādīto numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="22b02-244">If no other number sequence is set up for the cash account, this field is filled in automatically, based on the number sequence that is specified in the parameters.</span></span> <span data-ttu-id="22b02-245">Ja nepieciešams, šajā lauka pasūtījuma numuru varat ievadīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="22b02-245">You can manually enter an order number in this field as you require.</span></span> <span data-ttu-id="22b02-246">Lai nepieļautu kases dokumentu numerācijas nesakritības, tiek lietots šāds kontroles kritērijs: tāda kases dokumenta numurs, kura operācijas datums ir agrāks, nedrīkst būt lielāks par tāda kases dokumenta numuru, kura operācijas datums ir vēlāks.</span><span class="sxs-lookup"><span data-stu-id="22b02-246">To prevent inconsistence in cash document numbering, the following control is applied: the number of a cash document that has an earlier date of operation can&#39;t be higher than number of a cash document that has a later date of operation.</span></span> <span data-ttu-id="22b02-247">Ja šis kontroles kritērijs nav nepieciešams, tad kases un bankas vadības parametru sadaļā atzīmējiet izvēles rūtiņu <strong>Grāmatošana agrākā datumā</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-247">If you don&#39;t require this control, select the <strong>Posting on earlier date</strong> check box in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-248">Apstiprināšanas statuss</span><span class="sxs-lookup"><span data-stu-id="22b02-248">Approval status</span></span></td>
<td><span data-ttu-id="22b02-249">Pirmās transakcijas statuss ir <strong>Nav</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-249">The first transaction status is <strong>None</strong>.</span></span> <span data-ttu-id="22b02-250">Papildinformāciju par transakcijas statusa iestatīšanu skatiet sadaļā &quot;Kases transakciju apstiprināšana un grāmatošana&quot;.</span><span class="sxs-lookup"><span data-stu-id="22b02-250">For information about how to set the transaction status, See the &quot;Cash transaction approval and posting&quot; section.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-251">Dokumenta tips</span><span class="sxs-lookup"><span data-stu-id="22b02-251">Document type</span></span></td>
<td><span data-ttu-id="22b02-252">Lauks cilnē <strong>Kases orderis</strong> tiek automātiski aizpildīts tālāk aprakstītajā veidā, pamatojoties uz summu, kuru ievadījāt šim kases dokumentam.</span><span class="sxs-lookup"><span data-stu-id="22b02-252">This field on the <strong>Cash order</strong> tab is filled in automatically, based on the amount that you entered for the cash document:</span></span>
<ul>
<li><span data-ttu-id="22b02-253"><strong>Kases ieņēmumu orderis</strong> — šī vērtība tiek lietota, ja kases kontam summu ievadījāt laukā <strong>Debets</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-253"><strong>Cash reimbursement slip</strong> – This value is used if you entered an amount in the <strong>Debit</strong> field for the cash account.</span></span></li>
<li><span data-ttu-id="22b02-254"><strong>Kases izdevumu orderis</strong> — šī vērtība tiek lietota, ja kases kontam summu ievadījāt laukā <strong>Kredīts</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-254"><strong>Cash disbursement slip</strong> – This value is used if you entered an amount in the <strong>Credit</strong> field for the cash account</span></span></li>
<li><span data-ttu-id="22b02-255"><strong>Labojums</strong> — kases kontam ievadījāt negatīvu summu laukā <strong>Debets</strong> vai laukā <strong>Kredīts</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-255"><strong>Correction</strong> – You entered a negative amount in either the <strong>Debit</strong> field or the <strong>Credit</strong> field for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-256">PVN grupa</span><span class="sxs-lookup"><span data-stu-id="22b02-256">Sales tax group</span></span></td>
<td><span data-ttu-id="22b02-257">Norādiet PVN kodu grupu, ko izmantot operācijas nodokļu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="22b02-257">Specify a sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-258">Krājumu PVN grupa</span><span class="sxs-lookup"><span data-stu-id="22b02-258">Item sales tax group</span></span></td>
<td><span data-ttu-id="22b02-259">Norādiet krājumu PVN grupu, ko izmantot operācijas nodokļu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="22b02-259">Specify an item sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-260">Iemesls</span><span class="sxs-lookup"><span data-stu-id="22b02-260">Reason</span></span></td>
<td><span data-ttu-id="22b02-261">Cilnē <strong>Kases orderis</strong> ievadiet tekstu, kas apraksta transakcijas priekšmetu.</span><span class="sxs-lookup"><span data-stu-id="22b02-261">On the <strong>Cash order</strong> tab, enter text that describes the transaction subject.</span></span> <span data-ttu-id="22b02-262">Šis teksts tiks drukāts kases ordera pārskata formā.</span><span class="sxs-lookup"><span data-stu-id="22b02-262">This text will be printed on the cash slip reporting form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-263">Dokumenta datums</span><span class="sxs-lookup"><span data-stu-id="22b02-263">Document Date</span></span></td>
<td><span data-ttu-id="22b02-264">Ievadiet aprakstu, numuru un datumu primārajam dokumentam, kurš ir transakcijas iemesls (piemēram, avansa pārskati, rēķins vai pasūtījums).</span><span class="sxs-lookup"><span data-stu-id="22b02-264">Enter the description, number, and date of the primary document that is the reason for the transaction (for example, advance reports, invoice, or order).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-265">Pārstāvja tips</span><span class="sxs-lookup"><span data-stu-id="22b02-265">Representative type</span></span></td>
<td><span data-ttu-id="22b02-266">Šim laukam var būt tālāk aprakstītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="22b02-266">This field can have the following values:</span></span>
<ul>
<li><span data-ttu-id="22b02-267"><strong>Nodarbinātais</strong> — uzmeklēšanas sadaļā <strong>Pārstāvis</strong> ir ietverts darbinieku saraksts, ja ir iestatīta lauka <strong>Korespondējošais konts</strong> vērtība <strong>Virsgrāmata</strong> vai <strong>Banka</strong>, vai kontrahenta kontaktpersonu saraksts, ja ir iestatīta lauka <strong>Korespondējošais konts</strong> vērtība <strong>Debitors</strong> vai <strong>Kreditors</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-267"><strong>Worker</strong> – The <strong>Representative</strong> lookup contains a list of employees if the <strong>Offset account</strong> field is set to <strong>Ledger</strong> or <strong>Bank</strong>, or a list of the counteragent&#39;s contact persons if the <strong>Offset account</strong> field is set to <strong>Customer</strong> or <strong>Vendor</strong>.</span></span> <span data-ttu-id="22b02-268">Lai iestatītu pārstāvjus, dodieties uz <strong>Pamata</strong> &gt; <strong>Iestatīšana</strong> &gt; <strong>Kontaktpersonas</strong> &gt; <strong>Kontaktpersona</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-268">To set up representatives, go to <strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Contact person</strong>.</span></span></li>
<li><span data-ttu-id="22b02-269"><strong>Cits</strong> — uzmeklēšanā <strong>Pārstāvis</strong> ir saraksts ar citiem debitoriem.</span><span class="sxs-lookup"><span data-stu-id="22b02-269"><strong>Other</strong> – The <strong>Representative</strong> lookup contains a list of other clients.</span></span> <span data-ttu-id="22b02-270">Lai iestatītu saņēmējus, kas netiek rādīti tabulā <strong>Debitori</strong> vai <strong>Kreditori</strong>, pārejiet uz sadaļu uz <strong>Virsgrāmata</strong> &gt; <strong>Saņēmēji</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-270">To set up receivers who don&#39;t appear in the <strong>Customers</strong> or <strong>Vendors</strong> table, go to <strong>General ledger</strong> &gt; <strong>Receivers</strong>.</span></span> <span data-ttu-id="22b02-271">Šis tips ir pieejams tikai Latvijai.</span><span class="sxs-lookup"><span data-stu-id="22b02-271">This type is available only for Latvia.</span></span> <span data-ttu-id="22b02-272">(Ir jābūt iespējotai konfigurācijas atslēgai <strong>CSELatvia</strong>.)</span><span class="sxs-lookup"><span data-stu-id="22b02-272">(The <strong>CSELatvia</strong> configuration key should be enabled.)</span></span></li>
<li><span data-ttu-id="22b02-273"><strong>Kreditors</strong> — uzmeklēšanā <strong>Pārstāvis</strong> ir saraksts ar kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="22b02-273"><strong>Vendor</strong> – The <strong>Representative</strong> lookup contains a list of vendors.</span></span> <span data-ttu-id="22b02-274">Lai iestatītu kreditorus, dodieties uz <strong>Parādi kreditoriem</strong> &gt; <strong>Kreditori</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-274">To set up vendors, go to <strong>Accounts payable</strong> &gt; <strong>Vendors</strong>.</span></span></li>
<li><span data-ttu-id="22b02-275"><strong>Debitors</strong> — uzmeklēšanā <strong>Pārstāvis</strong> ir saraksts ar debitoriem.</span><span class="sxs-lookup"><span data-stu-id="22b02-275"><strong>Customer</strong> – The <strong>Representative</strong> lookup contains a list of customers.</span></span> <span data-ttu-id="22b02-276">Lai iestatītu debitorus, dodieties uz <strong>Debitoru parādi</strong> &gt; <strong>Debitori</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-276">To set up customers, go to <strong>Accounts receivable</strong> &gt; <strong>Customers</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-277">Pārstāvis</span><span class="sxs-lookup"><span data-stu-id="22b02-277">Representative</span></span></td>
<td><span data-ttu-id="22b02-278">Atlasiet pārstāvi, kura tips atbilst laukā <strong>Pārstāvja tips</strong> norādītajam tipam.</span><span class="sxs-lookup"><span data-stu-id="22b02-278">Select a representative of the type that you specified in the <strong>Representative type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-279">Personas vārds</span><span class="sxs-lookup"><span data-stu-id="22b02-279">Name of person</span></span></td>
<td><span data-ttu-id="22b02-280">Šis lauks tiek aizpildīts automātiski, pamatojoties uz laukiem <strong>Korespondējošais konts</strong> un <strong>Pārstāvis</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-280">This field is filled in automatically, based on the <strong>Offset account</strong> and <strong>Representative</strong> fields.</span></span> <span data-ttu-id="22b02-281">Kases orderu drukāšanas forma atainos šo informāciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-281">The printing form for cash slips will reflect this information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-282">Personas apliecība</span><span class="sxs-lookup"><span data-stu-id="22b02-282">Identity card</span></span></td>
<td><span data-ttu-id="22b02-283">Šis lauks tiek aizpildīts automātiski, pamatojoties uz attiecīgās kontaktpersonas (pārstāvja) personas apliecības datiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-283">This field is filled in automatically, based on the identity card data for the contact person (representative).</span></span> <span data-ttu-id="22b02-284">Ja laukam <strong>Korespondējošā konta tips</strong> ir iestatīta vērtība <strong>Avansa turētājs</strong> un laukam <strong>Korespondējošais konts</strong> ir iestatīts darbinieka numurs, tad kases ieņēmumus vai izdevumus var veikt no darbinieka vai uz darbinieku.</span><span class="sxs-lookup"><span data-stu-id="22b02-284">If the <strong>Offset account type</strong> field is set to <strong>Advance holder</strong>, and the <strong>Offset account</strong> field is set to an employee number, cash receipts or expenditures can be done from or to the employee.</span></span> <span data-ttu-id="22b02-285">Tādā gadījumā lauks <strong>Personas apliecība</strong> tiek aizpildīts automātiski, izmantojot datus personas apliecībai no tabulas <strong>Darbinieks</strong> (<strong>Darbinieku uzskaite</strong> &gt; <strong>Darbinieku tabula</strong>).</span><span class="sxs-lookup"><span data-stu-id="22b02-285">In this case the <strong>Identity card</strong> field is filled in automatically by using data for the identity card from the <strong>Employee</strong> table (<strong>Staff accounting</strong> &gt; <strong>Employee table</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-286">Nolūks</span><span class="sxs-lookup"><span data-stu-id="22b02-286">Purpose</span></span></td>
<td><span data-ttu-id="22b02-287">Tabulā <strong>Nolūks</strong> attiecīgajai transakcijas summai definējiet vienu vai vairākus mērķa kodus.</span><span class="sxs-lookup"><span data-stu-id="22b02-287">In the <strong>Purpose</strong> table, define one or more destination codes for the transaction amount.</span></span> <span data-ttu-id="22b02-288">Atlasiet mērķa kodu laukā <strong>Nolūks</strong> un ievadiet skaidrojumu laukā <strong>Transakcijas teksts</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-288">Select a destination code in the <strong>Purpose</strong> field, and enter an explanation in the <strong>Transaction text</strong> field.</span></span> <span data-ttu-id="22b02-289">Laukā <strong>Summa</strong> ievadiet summu transakcijas valūtā.</span><span class="sxs-lookup"><span data-stu-id="22b02-289">In the <strong>Amount</strong> field, enter an amount in the transaction currency.</span></span> <span data-ttu-id="22b02-290">Laukā <strong>Procenti</strong> tiek rādīta mērķa summas attiecība pret kopējo transakcijas summu, izteikta procentu veidā.</span><span class="sxs-lookup"><span data-stu-id="22b02-290">The <strong>Percent</strong> field shows, as a percentage, the ratio of the destination amount to the total transaction amount.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-291">Atgādinājums</span><span class="sxs-lookup"><span data-stu-id="22b02-291">Remainder</span></span></td>
<td><span data-ttu-id="22b02-292">Atlikusī summa, kas ir aprēķināta.</span><span class="sxs-lookup"><span data-stu-id="22b02-292">The remaining amount that is calculated.</span></span> <span data-ttu-id="22b02-293">Ņemiet vērā, ka kopējā transakcijas summa ir jāpiešķir mērķa kodiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-293">Note that the whole transaction amount must be assigned to destination codes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-294">Amatpersonas</span><span class="sxs-lookup"><span data-stu-id="22b02-294">Officials</span></span></td>
<td><span data-ttu-id="22b02-295">Cilnē <strong>Amatpersonas</strong> norādiet atbildīgo personu vārdus, uzvārdus un amatus: Direktors, Galvenais grāmatvedis un Kasieris.</span><span class="sxs-lookup"><span data-stu-id="22b02-295">On the <strong>Officials</strong> tab, specify the names and titles for responsible persons: Director, Chief accountant, and Cashier.</span></span> <span data-ttu-id="22b02-296">Vērtības <strong>Amats</strong> tiek noteiktas pēc amatpersonu iestatīšanas lapas <strong>Amatpersonas</strong> cilnēs <strong>Vispārīgi</strong> un <strong>Virsgrāmata</strong> (<strong>Pamata</strong> &gt; <strong>Iestatīšana</strong> &gt; <strong>Kontaktpersonas</strong> &gt; <strong>Amatpersonas</strong>).</span><span class="sxs-lookup"><span data-stu-id="22b02-296">The <strong>Position</strong> values are determined by the setup of officials on the <strong>General</strong> and <strong>Ledger</strong> tabs of the <strong>Officials</strong> page (<strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Officials</strong>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-297">Priekšapmaksa</span><span class="sxs-lookup"><span data-stu-id="22b02-297">Prepayment</span></span></td>
<td><span data-ttu-id="22b02-298">Atzīmējiet šo izvēles rūtiņu, ja transakcija ir priekšapmaksa.</span><span class="sxs-lookup"><span data-stu-id="22b02-298">Select this check box if the transaction is a prepayment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-299">Grāmatošanas metode</span><span class="sxs-lookup"><span data-stu-id="22b02-299">Posting profile</span></span></td>
<td><span data-ttu-id="22b02-300">Ievadiet grāmatošanas metodi attiecīgajam kases kontam.</span><span class="sxs-lookup"><span data-stu-id="22b02-300">Enter the posting profile for the cash account.</span></span> <span data-ttu-id="22b02-301">Pēc noklusējuma tiek lietota grāmatošanas metode, kas ir norādīta sadaļā Kases un bankas vadības parametri.</span><span class="sxs-lookup"><span data-stu-id="22b02-301">By default, the posting profile that is specified in the Cash and bank management parameters is used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-302">Korespondējošo kontu grāmatošanas metode</span><span class="sxs-lookup"><span data-stu-id="22b02-302">Offset posting profile</span></span></td>
<td><span data-ttu-id="22b02-303">Ievadiet grāmatošanas metodi atlasītajam korespondējošajam kontam.</span><span class="sxs-lookup"><span data-stu-id="22b02-303">Enter the posting profile for the selected offset account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-304">Kopējā summa</span><span class="sxs-lookup"><span data-stu-id="22b02-304">Total amount</span></span></td>
<td><span data-ttu-id="22b02-305">Lapas apakšā esošajā lauku grupā <strong>Kopējā summa</strong> laukā <strong>Ieņēmumu</strong> tiek rādīta kopsumma, kas ir aprēķināta visiem pašreizējā žurnālā ievadītajiem kases ieņēmumu orderiem, un laukā <strong>Izdevumu</strong> tiek rādīta kopsumma visiem kases izdevumu orderiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-305">In the <strong>Total amount</strong> field group at the bottom of the page, the <strong>Reimb</strong> field shows the total that is calculated for all Cash reimbursement slips that are entered in the current journal, and the <strong>Disb</strong> field shows the total for all Cash disbursement slips.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="22b02-306">Lai pārbaudītu žurnālu ierakstus, darbību rūtī noklikšķiniet uz **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="22b02-306">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="daily-cash-operations-via-a-general-journal"></a><span data-ttu-id="22b02-307">Ikdienas kases operācijas, izmantojot virsgrāmatas žurnālu</span><span class="sxs-lookup"><span data-stu-id="22b02-307">Daily cash operations via a General journal</span></span>
<span data-ttu-id="22b02-308">Lai izveidotu kases transakciju, izmantojot virsgrāmatas žurnālu, dodieties uz **Virsgrāmata** &gt; **Žurnāla ieraksti** &gt; **Virsgrāmatas žurnāli** un izveidojiet jaunu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="22b02-308">To create a cash transaction via a General journal, go to **General ledger** &gt; **Journal entries** &gt; **General journals**, and create a new journal.</span></span> <span data-ttu-id="22b02-309">Darbību rūtī noklikšķiniet uz **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="22b02-309">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="22b02-310">Pievienojiet jaunu rindu un ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-310">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22b02-311">Lauks</span><span class="sxs-lookup"><span data-stu-id="22b02-311">Field</span></span></th>
<th><span data-ttu-id="22b02-312">Apraksts</span><span class="sxs-lookup"><span data-stu-id="22b02-312">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22b02-313">Datums</span><span class="sxs-lookup"><span data-stu-id="22b02-313">Date</span></span></td>
<td><span data-ttu-id="22b02-314">Ievadiet darījuma datumu.</span><span class="sxs-lookup"><span data-stu-id="22b02-314">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-315">Konta veids</span><span class="sxs-lookup"><span data-stu-id="22b02-315">Account type</span></span></td>
<td><span data-ttu-id="22b02-316">Atlasiet vienumu <strong>Mazie kases posteņi</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-316">Select <strong>Petty cash</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-317">Konts</span><span class="sxs-lookup"><span data-stu-id="22b02-317">Account</span></span></td>
<td><span data-ttu-id="22b02-318">Atlasiet kases konta numuru.</span><span class="sxs-lookup"><span data-stu-id="22b02-318">Select the cash account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-319">Darbības teksts</span><span class="sxs-lookup"><span data-stu-id="22b02-319">Transaction text</span></span></td>
<td><span data-ttu-id="22b02-320">Ievadiet skaidrojošu tekstu par transakciju.</span><span class="sxs-lookup"><span data-stu-id="22b02-320">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-321">Debetkarte</span><span class="sxs-lookup"><span data-stu-id="22b02-321">Debit Credit</span></span></td>
<td><span data-ttu-id="22b02-322">Ievadiet kases dokumenta summu vienā no tālāk norādītajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-322">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="22b02-323"><strong>Debets</strong> — izmantojiet šo lauku, lai reģistrētu kases ieņēmumus un kases ieņēmumu orderi.</span><span class="sxs-lookup"><span data-stu-id="22b02-323"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="22b02-324"><strong>Kredīts</strong> — izmantojiet šo lauku, lai reģistrētu kases izdevumus un kases izdevumu orderi.</span><span class="sxs-lookup"><span data-stu-id="22b02-324"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-325">Korespondējošā konta tipa korespondējošais konts</span><span class="sxs-lookup"><span data-stu-id="22b02-325">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="22b02-326">Atlasiet korespondējošā konta tipu un korespondējošā konta numuru.</span><span class="sxs-lookup"><span data-stu-id="22b02-326">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-327">Valūta</span><span class="sxs-lookup"><span data-stu-id="22b02-327">Currency</span></span></td>
<td><span data-ttu-id="22b02-328">Atlasiet transakcijas valūtas kodu.</span><span class="sxs-lookup"><span data-stu-id="22b02-328">Select the code for the transaction currency.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="22b02-329">Cilnē **Rēķins** varat norādīt grāmatošanas metodes atlasītajam kontam un korespondējošajam kontam.</span><span class="sxs-lookup"><span data-stu-id="22b02-329">On the **Invoice** tab, you can specify posting profiles for the selected account and offset account.</span></span> <span data-ttu-id="22b02-330">Ja reģistrētā transakcija ir priekšapmaksa, tad cilnē **Maksājums** atzīmējiet izvēles rūtiņu **Priekšapmaksa**. Lauku grupā **Pārstāvis** aizpildiet laukus tāpat, kā to izdarījāt orderu žurnāla rindās, lai izdrukātu pārskatā **Kase**.</span><span class="sxs-lookup"><span data-stu-id="22b02-330">If the registered transaction is a prepayment, select the **Prepayment** check box on the **Payment** tab. In the **Representative** field group, fill in the fields as you did for the Slip journal lines to print on the **Cash** report.</span></span> <span data-ttu-id="22b02-331">Lai pārbaudītu žurnālu ierakstus, darbību rūtī noklikšķiniet uz **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="22b02-331">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="cash-transaction-approval-and-posting"></a><span data-ttu-id="22b02-332">Kases transakciju apstiprināšana un grāmatošana</span><span class="sxs-lookup"><span data-stu-id="22b02-332">Cash transaction approval and posting</span></span>
<span data-ttu-id="22b02-333">Kases transakcijām var lietot šādus statusus: **Nav**, **Ratificēts**, **Apstiprināts** un **Noraidīts**.</span><span class="sxs-lookup"><span data-stu-id="22b02-333">For cash transactions, the following statuses can be applied: **None**, **Confirmed**, **Approved**, and **Rejected**.</span></span> <span data-ttu-id="22b02-334">Parametrs **Lietot ratifikācijas statusu** cilnes **Kase** kopsavilkuma cilnē **Apstiprinājums**, kurš atrodas sadaļā **Kases un bankas vadība** &gt; **Iestatīšana** &gt; **Kases un bankas vadības parametri**, jums ļauj aktivizēt divus papildu statusus: **Ratificēts** un **Noraidīts**.</span><span class="sxs-lookup"><span data-stu-id="22b02-334">A **Use confirm status** parameter on the **Approval** FastTab of the **Cash** tab at **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters** lets you activate two additional statuses: **Confirmed** and **Rejected**.</span></span> <span data-ttu-id="22b02-335">Ratifikācija ir piemērota, kad tiek izdoti kases dokumenti un kad kases ieņēmumus vai izdevumus koplieto divi darbinieki: grāmatvedis un kasieris.</span><span class="sxs-lookup"><span data-stu-id="22b02-335">Confirmation is appropriate when cash documents are issued, and cash receipts or expenditures are shared between two employees: accountant and cashier.</span></span> <span data-ttu-id="22b02-336">Funkcija **Atiestatīt statusu** maina pašreizējās transakcijas statusu.</span><span class="sxs-lookup"><span data-stu-id="22b02-336">The **Reset status** function changes the current transaction status.</span></span> <span data-ttu-id="22b02-337">**Apstiprināts** kļūst par **Ratificēts**, un **Ratificēts** kļūst par **Nav**.</span><span class="sxs-lookup"><span data-stu-id="22b02-337">**Approved** becomes **Confirmed**, and **Confirmed** becomes **None**.</span></span> <span data-ttu-id="22b02-338">Kases žurnāla ierakstus var rediģēt tikai tad, kad to statuss ir **Nav**.</span><span class="sxs-lookup"><span data-stu-id="22b02-338">Cash journal entries can be edited only when the status is **None**.</span></span> <span data-ttu-id="22b02-339">Kases transakcijas var noraidīt tikai tad, kad to transakcijas statuss ir **Ratificēts**.</span><span class="sxs-lookup"><span data-stu-id="22b02-339">Cash transactions can be rejected only if the transaction status is **Confirmed**.</span></span> <span data-ttu-id="22b02-340">Noraidītie kases dokumenti ir iekļauti pārskatā **Kases dokumentu reģistrācijas žurnāls**, bet tie netiek atspoguļoti pārskatā **Kases grāmata**.</span><span class="sxs-lookup"><span data-stu-id="22b02-340">Rejected cash documents are included on the **Journal of registration of cash documents** report, but they aren't reflected on the **Cash book** report.</span></span> <span data-ttu-id="22b02-341">Lai ratificētu kādu transakciju, atlasiet atbilstošo orderu žurnāla rindu un pēc tam noklikšķiniet uz **Dokumentu apstiprinājums** &gt; **Ratificēt**.</span><span class="sxs-lookup"><span data-stu-id="22b02-341">To confirm a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Confirm**.</span></span> <span data-ttu-id="22b02-342">Tiek ģenerēts kārtas numurs, pamatojoties uz norādīto numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="22b02-342">An order number is generated, based on the specified number sequence.</span></span> <span data-ttu-id="22b02-343">Transakcijas statuss mainās uz **Ratificēts**, un jūs vairs nevarat rediģēt šo žurnāla rindu.</span><span class="sxs-lookup"><span data-stu-id="22b02-343">The transaction status is changed to **Confirmed**, and you can no longer edit the journal line.</span></span> <span data-ttu-id="22b02-344">Kases konta atlikums nemainās.</span><span class="sxs-lookup"><span data-stu-id="22b02-344">The cash account balance remains unchanged.</span></span> <span data-ttu-id="22b02-345">Lai noraidītu kādu kases dokumentu, noklikšķiniet uz **Dokumentu apstiprinājums** &gt; **Noraidīt**.</span><span class="sxs-lookup"><span data-stu-id="22b02-345">To reject a cash document, click **Documents approval** &gt; **Reject**.</span></span> <span data-ttu-id="22b02-346">Šī opcija ir pieejama tikai dokumentiem, kuru statuss ir **Ratificēts**.</span><span class="sxs-lookup"><span data-stu-id="22b02-346">This option is available only for documents that have **Confirmed** status.</span></span> <span data-ttu-id="22b02-347">Lai apstiprinātu kādu transakciju, atlasiet atbilstošo orderu žurnāla rindu un pēc tam noklikšķiniet uz **Dokumentu apstiprinājums** &gt; **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="22b02-347">To approve a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Approve**.</span></span> <span data-ttu-id="22b02-348">Statuss **Apstiprināts** norāda, ka kases līdzekļi ir saņemti vai iztērēti.</span><span class="sxs-lookup"><span data-stu-id="22b02-348">The **Approved** status indicates that cash funds are received or expended.</span></span> <span data-ttu-id="22b02-349">Kases atlikums ir mainījies.</span><span class="sxs-lookup"><span data-stu-id="22b02-349">The cash balance is changed.</span></span> <span data-ttu-id="22b02-350">Kases transakciju var grāmatot.</span><span class="sxs-lookup"><span data-stu-id="22b02-350">The cash transaction can be posted.</span></span> <span data-ttu-id="22b02-351">Lai atceltu statusu **Apstiprināts** un atiestatītu uz statusu **Nav**, noklikšķiniet uz **Dokumentu apstiprinājums** &gt; **Atiestatīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="22b02-351">To cancel an **Approved** status and reset the status to **None**, click **Documents approval** &gt; **Reset status**.</span></span> <span data-ttu-id="22b02-352">Grāmatot var tikai apstiprinātas kases transakcijas.</span><span class="sxs-lookup"><span data-stu-id="22b02-352">Only approved cash transactions can be posted.</span></span> <span data-ttu-id="22b02-353">Lai grāmatotu žurnālu, noklikšķiniet uz **Grāmatot** &gt; **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="22b02-353">To post a journal, click **Post** &gt; **Post**.</span></span>

## <a name="print-a-cash-order"></a><span data-ttu-id="22b02-354">Drukāt kases orderi</span><span class="sxs-lookup"><span data-stu-id="22b02-354">Print a cash order</span></span>
<span data-ttu-id="22b02-355">Lai drukātu kases orderi, atlasiet orderu žurnāla rindu un pēc tam darbību rūtī noklikšķiniet uz **Drukāt** &gt; **Kases ordera pārskats**.</span><span class="sxs-lookup"><span data-stu-id="22b02-355">To print a cash order, select a Slip journal line, and then, on the Action Pane, click **Print** &gt; **Cash order report**.</span></span> <span data-ttu-id="22b02-356">Sistēma ģenerē drukāšanas formu kases ieņēmumu orderim vai kases izdevumu orderim, ņemot vērā to, vai atlasītajai rindai summa tika ievadīta laukā **Debets** vai laukā **Kredīts**.</span><span class="sxs-lookup"><span data-stu-id="22b02-356">The system generates a printing form for either a Cash reimbursement slip or a Cash disbursement slip, depending on whether an amount is entered in the **Debit** field the or **Credit** field for the selected line:</span></span>

-   <span data-ttu-id="22b02-357">Ja summa ir norādīta laukā **Debets**: Kases ieņēmumu orderis</span><span class="sxs-lookup"><span data-stu-id="22b02-357">If there is an amount in the **Debit** field: Cash reimbursement slip</span></span>
-   <span data-ttu-id="22b02-358">Ja summa ir norādīta laukā **Kredīts**: Kases izdevumu orderis</span><span class="sxs-lookup"><span data-stu-id="22b02-358">If there is an amount in the **Credit** field: Cash disbursement slip</span></span>

<span data-ttu-id="22b02-359">Drukāt var orderu žurnāla rindas, kuru statuss ir **Ratificēts**, **Apstiprināts** vai **Noraidīts**.</span><span class="sxs-lookup"><span data-stu-id="22b02-359">Slip journal lines that have **Confirmed**, **Approved**, or **Rejected** status can be printed.</span></span> <span data-ttu-id="22b02-360">Kases orderu dokumentus varat drukāt arī sadaļā **Kases un bankas vadība** &gt; **Pieprasījumi un pārskati** &gt; **Kases orderis**.</span><span class="sxs-lookup"><span data-stu-id="22b02-360">You can also print cash order documents at **Cash and bank management** &gt; **Inquires and reports** &gt; **Cash order**.</span></span>

## <a name="periodic-tasks"></a><span data-ttu-id="22b02-361">Periodiskie uzdevumi</span><span class="sxs-lookup"><span data-stu-id="22b02-361">Periodic tasks</span></span>
<span data-ttu-id="22b02-362">Tālāk norādītos uzdevumus var izpildīt šeit: **Kases un bankas vadība** &gt; **Periodiskie uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="22b02-362">The following tasks can be performed at **Cash and bank management** &gt; **Periodic tasks**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22b02-363">Periodiskais uzdevums</span><span class="sxs-lookup"><span data-stu-id="22b02-363">Periodic task</span></span></th>
<th><span data-ttu-id="22b02-364">Apraksts</span><span class="sxs-lookup"><span data-stu-id="22b02-364">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22b02-365">Pārbaudīt atlikuma limitu</span><span class="sxs-lookup"><span data-stu-id="22b02-365">Check balance limit</span></span></td>
<td><span data-ttu-id="22b02-366">Pārbaudiet atlikumu atlasītajam kases kontam noteiktajā datumā un parādiet rezultātu informatīvā ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="22b02-366">Check the balance for the selected cash account on the specified date, and show the result in an information message.</span></span> <span data-ttu-id="22b02-367">Atlikuma aprēķina var skaitīt tikai apstiprinātās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="22b02-367">Only approved transactions can be counted in the balance calculation.</span></span> <span data-ttu-id="22b02-368">Netiek ņemtas vērā transakcijas, kas ir atzīmētas ar statusu <strong>Algām</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-368">Transactions that are marked as <strong>For payroll</strong> aren&#39;t considered.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-369">Skaidras naudas atlikuma pārrēķins</span><span class="sxs-lookup"><span data-stu-id="22b02-369">Cash balance recalculation</span></span></td>
<td><span data-ttu-id="22b02-370">Izmantojiet šo uzdevumu, lai pārliecinātos, ka virsgrāmatas bilances kases kontiem atbilst kases atlikumam.</span><span class="sxs-lookup"><span data-stu-id="22b02-370">Use this task to make sure that the ledger balances for cash accounts fit the cash balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-371">Kases pārskata izveidošana (tikai Polijai)</span><span class="sxs-lookup"><span data-stu-id="22b02-371">Cash report creation (for Poland only)</span></span></td>
<td><span data-ttu-id="22b02-372">Izveidojiet pārskatu <strong>Kase</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-372">Create a <strong>Cash</strong> report.</span></span> <span data-ttu-id="22b02-373">Pārskata <strong>Kase</strong> numurs tiek ģenerēts, pamatojoties uz numuru sēriju, ko iestatījāt vienumam <strong>Pārskata numurs</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-373">The <strong>Cash</strong> report number is generated based on the number sequence that is set up for <strong>Report number</strong>.</span></span> <span data-ttu-id="22b02-374">Uzdevumam paredzētajā dialoglodziņā vienumam <strong>Beigu datums</strong> norādiet pēdējo datumu, kurā kases transakcijas ir jāskaita pārskatam <strong>Kase</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-374">In the dialog box for the task, in the <strong>To date</strong>, specify the last date for which cash transactions should be counted for the <strong>Cash</strong> report.</span></span> <span data-ttu-id="22b02-375">Izmantojiet funkciju <strong>Filtrēt</strong> cilnē <strong>Iekļaujamie ieraksti</strong>, lai norādītu papildu kritērijus kases transakciju atlases ierobežošanai.</span><span class="sxs-lookup"><span data-stu-id="22b02-375">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify additional criteria to limit the selection of cash transactions.</span></span> <span data-ttu-id="22b02-376">Šie kritēriji var iekļaut kases kontu numurus un valūtu kodus.</span><span class="sxs-lookup"><span data-stu-id="22b02-376">These criteria can include cash account numbers and currency codes.</span></span> <span data-ttu-id="22b02-377">Laukā <strong>Izveidoja</strong> atlasiet lietotāju, kurs ir atbildīgs par pārskata izveidošanu.</span><span class="sxs-lookup"><span data-stu-id="22b02-377">In the <strong>Create by</strong> field, select the user who is responsible for report creation.</span></span> <span data-ttu-id="22b02-378">Lai skatītu izveidoto pārskatu <strong>Kase</strong>, izmantojiet pogu <strong>Kases pārskati</strong> lapā <strong>Kases konti</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-378">To view the <strong>Cash</strong> report that is created, use the <strong>Cash reports</strong> button on the <strong>Cash accounts</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22b02-379">Kase — Valūtas pārrēķins FIFO un LIFO (tikai Polijai)</span><span class="sxs-lookup"><span data-stu-id="22b02-379">Cash - Exchange adjustment FIFO and LIFO (for Poland only)</span></span></td>
<td><span data-ttu-id="22b02-380">Aprēķiniet valūtas pārrēķinu pēc Polijas standartiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-380">Calculate the exchange adjustment per Polish standards.</span></span> <span data-ttu-id="22b02-381">Izmantojiet funkciju <strong>Filtrēt</strong> cilnē <strong>Iekļaujamie ieraksti</strong>, lai norādītu kases kontu, kuram izpildīt šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="22b02-381">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="22b02-382">Atzīmējiet izvēles rūtiņu <strong>Pārrēķins</strong>, lai izpildītu pilnu valūtas maiņas starpības pārrēķinu visiem atvērtajiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="22b02-382">Select the <strong>Recalculation</strong> check box to do a full recalculation of the exchange adjustment difference for all open periods.</span></span> <span data-ttu-id="22b02-383">Tālāk ir aprakstīts, kā notiek valūtas pārrēķināšana, ja tiek izmantota metode “pirmais iekšā, pirmais ārā” (first in, first out – FIFO) un metode “pēdējais iekšā, pirmais ārā” (last in, first out — LIFO).</span><span class="sxs-lookup"><span data-stu-id="22b02-383">Here is how the exchange adjustment is calculated when the first in, first out (FIFO) and last in, first out (LIFO) methods are used:</span></span>
<ul>
<li><span data-ttu-id="22b02-384"><strong>FIFO metode</strong> — sistēma meklē izdevumu transakciju, kurai ir agrāks transakcijas datums (mazāks kārtas numurs), un to nosedz ar ieejas plūsmas transakciju, kurai ir agrāks transakcijas datums (mazāks kārtas numurs).</span><span class="sxs-lookup"><span data-stu-id="22b02-384"><strong>FIFO method</strong> – The system searches for an expenditure transaction that has an earlier transaction date (smaller order number) and settles it with a receipt transaction that has an earlier transaction date (smaller order number).</span></span></li>
<li><span data-ttu-id="22b02-385"><strong>LIFO metode</strong> — sistēma meklē izdevumu transakciju, kurai ir vēlāks transakcijas datums (lielāks kārtas numurs), un to nosedz ar ieejas plūsmas transakciju, kurai ir vēlāks transakcijas datums (lielāks kārtas numurs).</span><span class="sxs-lookup"><span data-stu-id="22b02-385"><strong>LIFO method</strong> – The system searches for an expenditure transaction that has a later transaction date (larger order number) and settles it with a receipt transaction that has a later transaction date (larger order number).</span></span></li>
</ul>
<span data-ttu-id="22b02-386">Nosegtā summa tiek rādīta laukā <strong>Nosegts valūtā</strong>, lapā <strong>Kases transakcija</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-386">The settled amount is reflected in the <strong>Settled currency</strong> field on the <strong>Cash transaction</strong> page.</span></span> <span data-ttu-id="22b02-387">Ja pastāv valūtas pārrēķina starpība, šī summa tiek rādīta laukā <strong>Valūtas pārrēķina summa</strong>, un tabulā <strong>Kases transakcija</strong> tiek ģenerēta transakcija ar dokumenta tipu <strong>Valūtas kursu starpība</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-387">If there is an exchange adjustment difference, the amount is reflected in the <strong>Exchange adjustment amount</strong> field, and a transaction of the <strong>Exchange rate difference</strong> document type is generated in the <strong>Cash transaction</strong> table.</span></span> <span data-ttu-id="22b02-388">Virsgrāmatas konti peļņas/zaudējumu transakcijām ir iestatīti tabulā <strong>Valūta</strong> (<strong>Peļņa no valūtas kursa svārstībām</strong> un <strong>Zaudējumi no valūtas kursa svārstībām</strong>).</span><span class="sxs-lookup"><span data-stu-id="22b02-388">Ledger accounts for profit/loss transactions are set in the <strong>Currency</strong> table (<strong>Exchange rate financial profit</strong> and <strong>Exchange rate financial loss</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22b02-389">Ārvalstu valūtas pārvērtēšana — Kase</span><span class="sxs-lookup"><span data-stu-id="22b02-389">Foreign currency revaluation - Cash</span></span></td>
<td><span data-ttu-id="22b02-390">Izmantojiet šo uzdevumu, lai izmantotu atbilstošu bilanci noklusējuma valūtā pārskata datumā, kad operācijas tiek ievadītas ārvalstu valūtās.</span><span class="sxs-lookup"><span data-stu-id="22b02-390">Use this task to have an adequate balance in the default currency on the reporting date when the operations are entered in foreign currencies.</span></span> <span data-ttu-id="22b02-391">Izmantojiet funkciju <strong>Filtrēt</strong> cilnē <strong>Iekļaujamie ieraksti</strong>, lai norādītu kases kontu, kuram izpildīt šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="22b02-391">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="22b02-392">Šim uzdevumam paredzētajā dialoglodziņā izmantojiet laukus <strong>No valūtas</strong> un <strong>Uz valūtu</strong>, lai norādītu transakciju valūtas.</span><span class="sxs-lookup"><span data-stu-id="22b02-392">In the dialog box for the task, use the <strong>From currency</strong> and <strong>To Currency</strong> fields to specify transaction currencies.</span></span> <span data-ttu-id="22b02-393">Summu konvertētajā valūtā sistēma salīdzina ar summu noklusējuma valūtā, izmantojot maiņas kursu atlasītajā datumā.</span><span class="sxs-lookup"><span data-stu-id="22b02-393">The system compares the amount in the currency that was converted by using exchange rate on the selected date with the amount in the default currency.</span></span> <span data-ttu-id="22b02-394">Šo abu summu starpība (izņemot iepriekšējo valūtas pārrēķinu) ir aprēķinātais valūtas pārrēķins.</span><span class="sxs-lookup"><span data-stu-id="22b02-394">The difference between the two amounts (excluding the previous exchange adjustment) is the calculated exchange adjustment.</span></span> <span data-ttu-id="22b02-395">Šis uzdevums izveido apstiprinātu kases transakciju ar tipu <strong>Valūtas pārrēķins</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-395">This task creates an approved cash transaction of the <strong>Exchange adjustment</strong> type.</span></span> <span data-ttu-id="22b02-396">Virsgrāmatas transakcija tiek veidota, izmantojot virsgrāmatas kontu kasei un virsgrāmatas kontu, kurš ir norādīts tabulas <strong>Valūta</strong> vienumā <strong>Nerealizētā peļņa</strong> vai <strong>Nerealizētie zaudējumi</strong>.</span><span class="sxs-lookup"><span data-stu-id="22b02-396">The ledger transaction is formed by using the ledger account for cash and the ledger account that is specified in <strong>Unrealized profit</strong> or <strong>Unrealized loss</strong> in the <strong>Currency</strong> table.</span></span></td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a><span data-ttu-id="22b02-397">Pieprasījumi un pārskati</span><span class="sxs-lookup"><span data-stu-id="22b02-397">Inquiries and reports</span></span>

| <span data-ttu-id="22b02-398">Pieprasījums vai pārskats</span><span class="sxs-lookup"><span data-stu-id="22b02-398">Inquiry or report</span></span>                             | <span data-ttu-id="22b02-399">Apraksts</span><span class="sxs-lookup"><span data-stu-id="22b02-399">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22b02-400">Kases transakciju skats</span><span class="sxs-lookup"><span data-stu-id="22b02-400">Cash transactions view</span></span>                        | <span data-ttu-id="22b02-401">Orderu žurnāla rindai darbību rūtī izmantojiet pogu **Pieprasījumi**, lai skatītu virsgrāmatas transakcijas, kases atlikumu un citu informāciju</span><span class="sxs-lookup"><span data-stu-id="22b02-401">For a Slip journal line, use the **Inquiries** button on the Action Pane to view ledger transactions, the cash balance, and other information.</span></span>                                                                                  |
| <span data-ttu-id="22b02-402">Kases transakcija</span><span class="sxs-lookup"><span data-stu-id="22b02-402">Cash transaction</span></span>                              | <span data-ttu-id="22b02-403">Lai skatītu kases transakcijas, dodieties uz **Kases un bankas vadība** &gt; **Pieprasījumi un pārskati** &gt; **Kases transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="22b02-403">Go to **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash transactions** to view cash transactions.</span></span> <span data-ttu-id="22b02-404">Izmantojiet funkciju **Filtrēt**, lai norādītu papildu kritērijus kases transakciju atlases ierobežošanai.</span><span class="sxs-lookup"><span data-stu-id="22b02-404">Use the **Filter** function to specify additional criteria to limit the selection of cash transactions.</span></span> |
| <span data-ttu-id="22b02-405">Reģistrācijas žurnāls (Igaunijai, Krievijai)</span><span class="sxs-lookup"><span data-stu-id="22b02-405">Journal of registration (for Estonia, Russia)</span></span> | <span data-ttu-id="22b02-406">Pārskats sadaļā **Kases un bankas vadība** &gt; **Pieprasījumi un pārskati** &gt; **Reģistrācijas žurnāls** ataino visus izdotos kases ienākumu un kases izdevumu orderus.</span><span class="sxs-lookup"><span data-stu-id="22b02-406">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Journal of registration** reflects all cash reimbursement and cash disbursement slips that have been issued.</span></span>                                   |
| <span data-ttu-id="22b02-407">Kases grāmata (Latvijai, Lietuvai, Krievijai)</span><span class="sxs-lookup"><span data-stu-id="22b02-407">Cash book (for Latvia, Lithuania, Russia)</span></span>     | <span data-ttu-id="22b02-408">Pārskats sadaļā **Kases un bankas vadība** &gt; **Pieprasījumi un pārskati** &gt; **Kases grāmatas žurnāls** ataino faktiskās kases līdzekļu kustības (ieņēmumus un izdevumus).</span><span class="sxs-lookup"><span data-stu-id="22b02-408">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash book report** reflects actual cash fund movements (receipts and expenditures).</span></span>                                                            |





