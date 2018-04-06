---
title: "Virsgrāmatas žurnāla apstrāde"
description: "Šajā rakstā ir aprakstītas programmas Microsoft Dynamics 365 for Finance and Operations iespējas, kas var palīdzēt vienkāršot Virsgrāmatas žurnālu apstrādi un arī nodrošināt pareizu datu ieguvi un pienācīgu iekšējo kontroli."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: eb46613f805999753c2ab73ffb91a6fdae04c68e
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="92309-103">Virsgrāmatas žurnāla apstrāde</span><span class="sxs-lookup"><span data-stu-id="92309-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="92309-104">Šajā rakstā ir aprakstītas programmas Microsoft Dynamics 365 for Finance and Operations iespējas, kas var palīdzēt vienkāršot Virsgrāmatas žurnālu apstrādi un arī nodrošināt pareizu datu ieguvi un pienācīgu iekšējo kontroli.</span><span class="sxs-lookup"><span data-stu-id="92309-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="92309-105">Žurnālu nosaukumi</span><span class="sxs-lookup"><span data-stu-id="92309-105">Journal names</span></span>

<span data-ttu-id="92309-106">Viena no svarīgākajām iestatījumu jomām ir žurnālu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="92309-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="92309-107">Ir ieteicams norādīt žurnālu nosaukumus katram mērķim, piemēram, starpuzņēmumu transakcijām, uzkrājumu korekcijai un kļūdu labošanai.</span><span class="sxs-lookup"><span data-stu-id="92309-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="92309-108">Varat pielāgot katra žurnāla nosaukumu, lai palīdzētu padarīt katram mērķim paredzēto datu ievadi vienkāršu un drošu.</span><span class="sxs-lookup"><span data-stu-id="92309-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="92309-109">Lapā **Žurnālu nosaukumi**, jūs varat iestatīt šādus elementus:</span><span class="sxs-lookup"><span data-stu-id="92309-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="92309-110">**Darbplūsmas apstiprinājums** – lai palielinātu iekšējo pārbaudi, definējiet žurnāla darbplūsmas, kas izveido būtiskuma ierobežojumus pārskatīšanas un apstiprināšanas soļiem, pamatojoties uz tādiem kritērijiem, kā debeta summa.</span><span class="sxs-lookup"><span data-stu-id="92309-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="92309-111">Virsgrāmatas žurnālu darbplūsmas var iestatīt lapā **Virsgrāmatas darbplūsmas**.</span><span class="sxs-lookup"><span data-stu-id="92309-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="92309-112">**Noklusētās vērtības** – atlasiet noklusētās vērtības korespondējošiem kontiem, valūtai un finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="92309-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="92309-113">**Žurnāla pārbaude** – varat iestatīt ierobežojumus attiecībā uz uzņēmumu un konta tipu, kā arī segmentu vērtībām.</span><span class="sxs-lookup"><span data-stu-id="92309-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="92309-114">**Piemēri**</span><span class="sxs-lookup"><span data-stu-id="92309-114">**Examples**</span></span>

<span data-ttu-id="92309-115">Žurnāla nosaukums var tikt izmantots tikai korekcijām.</span><span class="sxs-lookup"><span data-stu-id="92309-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="92309-116">Šādā gadījumā, jūs varat norādīt, ka tikai **Virsgrāmatas** konta tips ir derīgs visos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="92309-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="92309-117">[![Žurnāla pārbaudes kontu veidi](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="92309-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="92309-118">Žurnāla nosaukumu var izmantot tikai galveno kontu noteiktam segmentam vai diapazonam.</span><span class="sxs-lookup"><span data-stu-id="92309-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="92309-119">[![Žurnāla pārbaudes segments](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="92309-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="92309-120">Virsgrāmatas žurnālos ir pieejama opcija **Automātiskās atgriešana**.</span><span class="sxs-lookup"><span data-stu-id="92309-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="92309-121">Piemēram, jums ir uzkrājuma korekcija, kur faktiskais dokuments vēl nav apstrādāts, kā parādīts šajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="92309-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="92309-122">[![Virsgrāmatas žurnāla storno](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="92309-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="92309-123">Microsoft Excel pievienojumprogramma žurnāla ierakstu veidošanai nodrošina papildu automatizācijas līmeni un atvieglo datu ievadi.</span><span class="sxs-lookup"><span data-stu-id="92309-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="92309-124">Darbība **Atvērt rindas programmā Excel** ir pieejama lapās **Virsgrāmatas žurnāls** un **Žurnāla dokuments**.</span><span class="sxs-lookup"><span data-stu-id="92309-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="92309-125">Lapā **Periodiskie žurnāli**, jūs varat iestatīt periodiskos žurnālus, lai automatizētu žurnāla apstrādi.</span><span class="sxs-lookup"><span data-stu-id="92309-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="92309-126">Jebkurā laikā varat izmantot dokumentu veidnes.</span><span class="sxs-lookup"><span data-stu-id="92309-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="92309-127">Lapā **Virsgrāmatas žurnāli** darbības **Saglabāt** un **Atlasīt dokumenta veidni** ir pieejamas lapas **Žurnāla dokuments** dokumentu rindiņu sadaļā **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="92309-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="92309-128">Saistītā iestatīšana</span><span class="sxs-lookup"><span data-stu-id="92309-128">Related setup</span></span>
<span data-ttu-id="92309-129">Šī iestatīšana nav raksturīga Virsgrāmatas žurnāliem, bet palīdzēs garantēt, ka datu ievade notiek pareizi un viegli.</span><span class="sxs-lookup"><span data-stu-id="92309-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="92309-130">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="92309-130">Main account</span></span>

<span data-ttu-id="92309-131">Galvenā konta iestatīšana sniedz daudzas opcijas Virsgrāmatas žurnāla apstrādei:</span><span class="sxs-lookup"><span data-stu-id="92309-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="92309-132">**DC/CR prasība** – izmantojiet šo opciju, ja galvenais konts ir ierobežots ar debeta vai kredīta darbībām.</span><span class="sxs-lookup"><span data-stu-id="92309-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="92309-133">Iestatīšana ir apstiprināta, kad žurnāls tiek pārbaudīts vai grāmatots.</span><span class="sxs-lookup"><span data-stu-id="92309-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="92309-134">**Noklusētais korespondējošais konts**</span><span class="sxs-lookup"><span data-stu-id="92309-134">**Default offset account**</span></span>
-   <span data-ttu-id="92309-135">**Atlikts** – apturēt galvenā konta datu ievadi visiem uzņēmumiem vai konkrētam uzņēmumam/juridiskai personai.</span><span class="sxs-lookup"><span data-stu-id="92309-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="92309-136">**Neļaut manuālu ievadi** – neļaut lietotājiem manuāli ievadīt vērtību konta žurnālos.</span><span class="sxs-lookup"><span data-stu-id="92309-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="92309-137">**Noklusējuma/Pārbaudīt valūtu**</span><span class="sxs-lookup"><span data-stu-id="92309-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="92309-138">**Juridiskās personas ignorēšana** – šis iestatījums ir specifisks noteiktam uzņēmumam/juridiskai personai:</span><span class="sxs-lookup"><span data-stu-id="92309-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="92309-139">**Noklusējuma/Validēt PVN**</span><span class="sxs-lookup"><span data-stu-id="92309-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="92309-140">**Noklusējuma dimensija** – **Nav noteikta** vai **Fiksēta vērtība**.</span><span class="sxs-lookup"><span data-stu-id="92309-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="92309-141">**Fiksēta vērtība** palīdzēs nodrošināt, ka visi grāmatojumi šajā galvenajā kontā vienmēr izmantos jebkuru dimensijas vērtību, kas iestatīta kā **Fiksēta**.</span><span class="sxs-lookup"><span data-stu-id="92309-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="92309-142">**Grāmatojuma pārbaude**</span><span class="sxs-lookup"><span data-stu-id="92309-142">**Posting validation**</span></span>
    -   <span data-ttu-id="92309-143">**Lietotāja pārbaude** – šī opcija pārbauda, kuri lietotāji var grāmatot galvenajā kontā.</span><span class="sxs-lookup"><span data-stu-id="92309-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="92309-144">**Grāmatošanas veida validēšana** – šī opcija pārbauda, kuri grāmatošanas veidi ir atļauti galvenajam kontam.</span><span class="sxs-lookup"><span data-stu-id="92309-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="92309-145">Grāmatvedības struktūras un papildu kārtulu struktūras</span><span class="sxs-lookup"><span data-stu-id="92309-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="92309-146">Grāmatvedības struktūras un papildu kārtulu struktūras ir ļoti svarīgas, lai nodrošinātu, ka dati, kas ir nepieciešami finanšu pārskatiem un veiktspējas izsekošanai, tiek tverti Virsgrāmatas žurnāla un jebkādas dokumentācijas apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="92309-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="92309-147">Grāmatvedības struktūras un papildu kārtulu struktūras ļauj pielāgot datu ievades iespējas.</span><span class="sxs-lookup"><span data-stu-id="92309-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="92309-148">Jūs varat atļaut datu ievadi tikai finanšu dimensijām, kas ir atbilstošas katrā situācijā, kā arī ieviest prasību par to, ka vienmēr jātver obligāti un pareizi dati.</span><span class="sxs-lookup"><span data-stu-id="92309-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="92309-149">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="92309-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="92309-150">[Plānošana: kontu plāns](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="92309-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="92309-151">Žurnālu papildu kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="92309-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="92309-152">Žurnāla ieraksta izveide, izmantojot veidni</span><span class="sxs-lookup"><span data-stu-id="92309-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="92309-153">Žurnālu izveide un validēšana</span><span class="sxs-lookup"><span data-stu-id="92309-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="92309-154">Periodu žurnālu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="92309-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="92309-155">Virsgrāmatas sadalījuma žurnāla apstrāde</span><span class="sxs-lookup"><span data-stu-id="92309-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



