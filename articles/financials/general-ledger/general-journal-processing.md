---
title: Virsgrāmatas žurnāla apstrāde
description: Šajā tēmā ir aprakstītas programmā Microsoft Dynamics 365 for Finance and Operations pieejamās iespējas, kas var palīdzēt atvieglot Virsgrāmatas žurnāla apstrādi, kā arī palīdzēt nodrošināt, ka tiek iegūti pareizie dati un netiek pārkāpti iekšējās kontroles kritēriji.
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7efd250428f7675b96674dd02e3aeccefe653fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839235"
---
# <a name="general-journal-processing"></a><span data-ttu-id="68355-103">Virsgrāmatas žurnāla apstrāde</span><span class="sxs-lookup"><span data-stu-id="68355-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68355-104">Šajā tēmā ir aprakstītas programmā Microsoft Dynamics 365 for Finance and Operations pieejamās iespējas, kas var palīdzēt atvieglot Virsgrāmatas žurnāla apstrādi, kā arī palīdzēt nodrošināt, ka tiek iegūti pareizie dati un netiek pārkāpti iekšējās kontroles kritēriji.</span><span class="sxs-lookup"><span data-stu-id="68355-104">This topic describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="68355-105">Žurnālu nosaukumi</span><span class="sxs-lookup"><span data-stu-id="68355-105">Journal names</span></span>

<span data-ttu-id="68355-106">Viena no svarīgākajām iestatījumu jomām ir žurnālu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="68355-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="68355-107">Ir ieteicams norādīt žurnālu nosaukumus katram mērķim, piemēram, starpuzņēmumu transakcijām, uzkrājumu korekcijai un kļūdu labošanai.</span><span class="sxs-lookup"><span data-stu-id="68355-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="68355-108">Varat pielāgot katra žurnāla nosaukumu, lai palīdzētu padarīt katram mērķim paredzēto datu ievadi vienkāršu un drošu.</span><span class="sxs-lookup"><span data-stu-id="68355-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="68355-109">Lapā **Žurnālu nosaukumi**, jūs varat iestatīt šādus elementus:</span><span class="sxs-lookup"><span data-stu-id="68355-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="68355-110">**Darbplūsmas apstiprinājums** – lai palielinātu iekšējo pārbaudi, definējiet žurnāla darbplūsmas, kas izveido būtiskuma ierobežojumus pārskatīšanas un apstiprināšanas soļiem, pamatojoties uz tādiem kritērijiem, kā debeta summa.</span><span class="sxs-lookup"><span data-stu-id="68355-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="68355-111">Varat iestatīt darbplūsmas virsgrāmatas žurnāliem lapā **Virsgrāmatas darbplūsmas**.</span><span class="sxs-lookup"><span data-stu-id="68355-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="68355-112">**Noklusētās vērtības** – atlasiet noklusētās vērtības korespondējošiem kontiem, valūtai un finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="68355-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="68355-113">**Žurnāla pārbaude** – varat iestatīt ierobežojumus attiecībā uz uzņēmumu un konta tipu, kā arī segmentu vērtībām.</span><span class="sxs-lookup"><span data-stu-id="68355-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="68355-114">**Piemēri**</span><span class="sxs-lookup"><span data-stu-id="68355-114">**Examples**</span></span>

<span data-ttu-id="68355-115">Žurnāla nosaukums var tikt izmantots tikai korekcijām.</span><span class="sxs-lookup"><span data-stu-id="68355-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="68355-116">Šādā gadījumā, jūs varat norādīt, ka tikai **Virsgrāmatas** konta tips ir derīgs visos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="68355-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="68355-117">[![Žurnāla pārbaudes kontu veidi](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="68355-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="68355-118">Žurnāla nosaukumu var izmantot tikai galveno kontu noteiktam segmentam vai diapazonam.</span><span class="sxs-lookup"><span data-stu-id="68355-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="68355-119">[![Žurnāla pārbaudes segments](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="68355-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="68355-120">Virsgrāmatas žurnālos ir pieejama opcija **Automātiskās atgriešana**.</span><span class="sxs-lookup"><span data-stu-id="68355-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="68355-121">Piemēram, jums ir uzkrājuma korekcija, kur faktiskais dokuments vēl nav apstrādāts, kā parādīts šajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="68355-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="68355-122">[![Virsgrāmatas žurnāla storno](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="68355-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="68355-123">Microsoft Excel pievienojumprogramma žurnāla ierakstu izveidei nodrošina papildu automatizācijas līmeni un atvieglo datu ievadi.</span><span class="sxs-lookup"><span data-stu-id="68355-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="68355-124">Darbība **Atvērt rindas programmā Excel** ir pieejama lapās **Virsgrāmatas žurnāls** un **Žurnāla dokuments**.</span><span class="sxs-lookup"><span data-stu-id="68355-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="68355-125">Lapā **Periodiskie žurnāli**, jūs varat iestatīt periodiskos žurnālus, lai automatizētu žurnāla apstrādi.</span><span class="sxs-lookup"><span data-stu-id="68355-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="68355-126">Jebkurā laikā varat izmantot dokumentu veidnes.</span><span class="sxs-lookup"><span data-stu-id="68355-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="68355-127">Lapā **Virsgrāmatas žurnāli** darbības **Saglabāt** un **Atlasīt dokumenta veidni** ir pieejamas lapas **Žurnāla dokuments** dokumentu rindiņu sadaļā **Funkcijas**.</span><span class="sxs-lookup"><span data-stu-id="68355-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="68355-128">Saistītā iestatīšana</span><span class="sxs-lookup"><span data-stu-id="68355-128">Related setup</span></span>
<span data-ttu-id="68355-129">Tālāk aprakstīta iestatīšana nav raksturīga Virsgrāmatas žurnāliem, bet palīdzēs nodrošināt pareizu un ērtu datu ievadi.</span><span class="sxs-lookup"><span data-stu-id="68355-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="68355-130">Galvenais konts</span><span class="sxs-lookup"><span data-stu-id="68355-130">Main account</span></span>

<span data-ttu-id="68355-131">Galvenā konta iestatīšana sniedz daudzas opcijas Virsgrāmatas žurnāla apstrādei:</span><span class="sxs-lookup"><span data-stu-id="68355-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="68355-132">**DC/CR prasība** – izmantojiet šo opciju, ja galvenais konts ir ierobežots ar debeta vai kredīta darbībām.</span><span class="sxs-lookup"><span data-stu-id="68355-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="68355-133">Iestatīšana ir apstiprināta, kad žurnāls tiek pārbaudīts vai grāmatots.</span><span class="sxs-lookup"><span data-stu-id="68355-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="68355-134">**Noklusētais korespondējošais konts**</span><span class="sxs-lookup"><span data-stu-id="68355-134">**Default offset account**</span></span>
-   <span data-ttu-id="68355-135">**Atlikts** — apturēt galvenā konta datu ievadi visiem uzņēmumiem vai konkrētam uzņēmumam/juridiskai personai.</span><span class="sxs-lookup"><span data-stu-id="68355-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="68355-136">**Neļaut manuālu ievadi** – neļaut lietotājiem manuāli ievadīt vērtību konta žurnālos.</span><span class="sxs-lookup"><span data-stu-id="68355-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="68355-137">**Noklusējuma/Pārbaudīt valūtu**</span><span class="sxs-lookup"><span data-stu-id="68355-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="68355-138">**Juridiskās personas ignorēšana** – šis iestatījums ir specifisks noteiktam uzņēmumam/juridiskai personai:</span><span class="sxs-lookup"><span data-stu-id="68355-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="68355-139">**Noklusējuma/Validēt PVN**</span><span class="sxs-lookup"><span data-stu-id="68355-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="68355-140">**Noklusējuma dimensija** – **Nav noteikta** vai **Fiksēta vērtība**.</span><span class="sxs-lookup"><span data-stu-id="68355-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="68355-141">**Fiksēta vērtība** palīdzēs nodrošināt, ka visiem grāmatojumiem šajā galvenajā kontā vienmēr tiks izmantota jebkura dimensijas vērtība, kas iestatīta kā **Fiksēta**.</span><span class="sxs-lookup"><span data-stu-id="68355-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="68355-142">**Grāmatojuma pārbaude**</span><span class="sxs-lookup"><span data-stu-id="68355-142">**Posting validation**</span></span>
    -   <span data-ttu-id="68355-143">**Lietotāja pārbaude** – šī opcija pārbauda, kuri lietotāji var grāmatot galvenajā kontā.</span><span class="sxs-lookup"><span data-stu-id="68355-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="68355-144">**Grāmatošanas veida validēšana** – šī opcija pārbauda, kuri grāmatošanas veidi ir atļauti galvenajam kontam.</span><span class="sxs-lookup"><span data-stu-id="68355-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="68355-145">Grāmatvedības struktūras un papildu kārtulu struktūras</span><span class="sxs-lookup"><span data-stu-id="68355-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="68355-146">Grāmatvedības struktūras un papildu kārtulu struktūras ir ļoti svarīgas, lai nodrošinātu, ka dati, kas ir nepieciešami finanšu pārskatiem un veiktspējas izsekošanai, tiek tverti Virsgrāmatas žurnāla un jebkuru dokumentu apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="68355-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="68355-147">Grāmatvedības struktūras un papildu kārtulu struktūras ļauj pielāgot datu ievades iespējas.</span><span class="sxs-lookup"><span data-stu-id="68355-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="68355-148">Datu ievadi var atļaut tikai finanšu dimensijām, kas ir atbilstošas katrā situācijā, kā arī ieviest prasību, ka vienmēr ir jātver obligāti nepieciešami un pareizi dati.</span><span class="sxs-lookup"><span data-stu-id="68355-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="68355-149">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="68355-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="68355-150">[Plānošana: kontu plāns](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="68355-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="68355-151">Žurnālu papildu kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="68355-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="68355-152">Žurnāla ieraksta izveide, izmantojot veidni</span><span class="sxs-lookup"><span data-stu-id="68355-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="68355-153">Žurnālu izveide un validēšana</span><span class="sxs-lookup"><span data-stu-id="68355-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="68355-154">Periodisko žurnālu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="68355-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="68355-155">Virsgrāmatas sadalījumu žurnāla apstrāde</span><span class="sxs-lookup"><span data-stu-id="68355-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="68355-156">Simulēt grāmatošanu</span><span class="sxs-lookup"><span data-stu-id="68355-156">Simulate posting</span></span>
<span data-ttu-id="68355-157">Vairumā žurnālu opcija **Simulēt grāmatošanu** ir pieejama izvēlnē **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="68355-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="68355-158">Apstiprinot žurnālu, izmantojot funkciju **Apstiprināt**, sistēma pārbauda, vai žurnālā nav noteiktu kļūdas nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="68355-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="68355-159">Ja tiek izmantota funkcija **Simulēt grāmatošanu**, sistēma palaiž visus tos pašus procesus, kas tiek palaisti grāmatošanas laikā bez faktiskas žurnāla grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="68355-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="68355-160">Pēc tam varat pārskatīt parādītos grāmatošanas ziņojumus, izlabot atrastās kļūdas, un pēc tam noklikšķiniet uz izvēlnes **Grāmatot**, lai grāmatotu žurnālu.</span><span class="sxs-lookup"><span data-stu-id="68355-160">You can then review the posting messages that are displayed, fix any errors that you find, and then click the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="68355-161">Opcija **Simulēt grāmatošanu** nav pieejama pakešveida apstrādei.</span><span class="sxs-lookup"><span data-stu-id="68355-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="68355-162">Taču ir pieejams pakešveida grāmatošanas simulēšanas kods, un izstrādātāji var paplašināt kodu, lai pievienotu šo funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="68355-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  
