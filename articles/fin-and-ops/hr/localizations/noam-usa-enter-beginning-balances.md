---
title: "Ievadīt algu sākuma bilances"
description: "Šajā tēmā ir aprakstītas darbības sākuma bilanču ievadīšanai attiecībā uz ienākumu veida kodiem, ieturējumiem, atvieglojumiem un nodokļiem. Šī informācija ir vērtīga partneriem, lai datus jaunai algu ieviešanai migrētu vai pārsūtītu no citas sistēmas."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 736eedf270ac08b0bdf9364821f8a7bae981ade9
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="d27cf-104">Ievadīt algu sākuma bilances</span><span class="sxs-lookup"><span data-stu-id="d27cf-104">Enter payroll beginning balances</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="d27cf-105">Šajā tēmā ir aprakstītas darbības sākuma bilanču ievadīšanai attiecībā uz ienākumu veida kodiem, ieturējumiem, atvieglojumiem un nodokļiem.</span><span class="sxs-lookup"><span data-stu-id="d27cf-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="d27cf-106">Šī informācija ir vērtīga partneriem, kuri datus jaunai algu ieviešanai pārsūtīta no citas sistēmas.</span><span class="sxs-lookup"><span data-stu-id="d27cf-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="d27cf-107">Lai sagatavotos ievadīt sākuma algu bilances, mēs pārbaudām tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d27cf-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

> * <span data-ttu-id="d27cf-108">Darbinieka ieraksti ir ievadīti un ir pieejami sistēmā</span><span class="sxs-lookup"><span data-stu-id="d27cf-108">Employee records are entered and available in the system</span></span>
> * <span data-ttu-id="d27cf-109">Darbiniekiem tiek iestatīti un tiek piešķirti tālāk norādītie dati.</span><span class="sxs-lookup"><span data-stu-id="d27cf-109">The following data is set up and assigned to employees:</span></span>

> > * <span data-ttu-id="d27cf-110">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="d27cf-110">Pay cycles and pay periods</span></span>
> > * <span data-ttu-id="d27cf-111">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="d27cf-111">Earning codes</span></span>
> > * <span data-ttu-id="d27cf-112">Nodokļi</span><span class="sxs-lookup"><span data-stu-id="d27cf-112">Taxes</span></span>
> > * <span data-ttu-id="d27cf-113">Atvieglojumi un atvilkumi</span><span class="sxs-lookup"><span data-stu-id="d27cf-113">Benefits and deductions</span></span>

> * <span data-ttu-id="d27cf-114">Uzņēmumam ir jāizvēlas datums, kur var iestatīt algu sākuma bilances.</span><span class="sxs-lookup"><span data-stu-id="d27cf-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>

> * <span data-ttu-id="d27cf-115">No mantojuma sistēmas tika vākta informācija par visiem ienākumiem, atvieglojumiem/atvilkumiem, atvieglojumu iemaksām, darbinieka nodokļiem un darba devēja nodokļiem, un to līdzšinējā gada (YTD) summām.</span><span class="sxs-lookup"><span data-stu-id="d27cf-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="d27cf-116">Kad plānojat ievadīt sākuma bilances, apsveriet, cik detalizētai šai informācijai ir jābūt.</span><span class="sxs-lookup"><span data-stu-id="d27cf-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="d27cf-117">Vairums uzņēmumu ievada vienu, konsolidētu līdzšinējā gada summu.</span><span class="sxs-lookup"><span data-stu-id="d27cf-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="d27cf-118">Taču, ja ir nepieciešama sīkāka informācija, bilances var ievadīt ar ceturkšņa pieaugumu.</span><span class="sxs-lookup"><span data-stu-id="d27cf-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="d27cf-119">Lēmums par nepieciešamo detalizētības līmeni arī nosaka, cik manuālo algas pārskatu ir jāizveido katram nodarbinātajam.</span><span class="sxs-lookup"><span data-stu-id="d27cf-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="d27cf-120">Vienai līdzšinējā gada summai katram darbiniekam ir nepieciešams tikai viens manuāls pārskats.</span><span class="sxs-lookup"><span data-stu-id="d27cf-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="d27cf-121">Lai to izdarītu, kā jaunajā algu sistēmā ievadīto summu izmantojiet līdzšinējā gada summas no iepriekšējās sistēmas gala algas pārskata.</span><span class="sxs-lookup"><span data-stu-id="d27cf-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="d27cf-122">Nākamajā piemērā ir parādīts, kā varat ievadīt darbinieku algu sākuma bilances, tostarp ienākumu veida kodus, atvieglojumu/atvilkumus un nodokļus.</span><span class="sxs-lookup"><span data-stu-id="d27cf-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="d27cf-123">Reālā piemērā jums būtu rindas krājums katram ienākumu veida kodam, atvieglojuma ieturējumam, atvieglojumu iemaksai, darbinieka nodoklim un darba devēja nodoklim, kuru ievadītā summa ir līdzšinējā gada summa.</span><span class="sxs-lookup"><span data-stu-id="d27cf-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="d27cf-124">Izmantojot šo kodu un summu sarakstu, izpildiet norādījumus par manuāla ienākumu un algas pārskata izveidošanu ar atspējotu uzskaiti, lai pārceltu sākuma bilances algu nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="d27cf-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span>  <span data-ttu-id="d27cf-125">Uzskaite ir jāatspējo, jo šo sākuma bilances algas pārskatu jūs nevēlaties grāmatot savā virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="d27cf-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="d27cf-126">Tas tika izdarīts mantojuma sistēmā un pārnāk uz jauno sistēmu, kad virsgrāmatā iestatāt sākuma bilances.</span><span class="sxs-lookup"><span data-stu-id="d27cf-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="d27cf-127">A.</span><span class="sxs-lookup"><span data-stu-id="d27cf-127">A.</span></span> <span data-ttu-id="d27cf-128">Kā iestatīt ienākumu veida kodus, ko izmantot algu sākuma bilancēm</span><span class="sxs-lookup"><span data-stu-id="d27cf-128">How to set up earnings codes to be used on payroll beginning balances</span></span>
<span data-ttu-id="d27cf-129">Kad ievadāt algu sākuma bilances, pārliecinieties, ka ienākumu veida kodi, kurus jūs izmantosiet, ir konfigurēti ar iespējotu opciju “Atļaut ienākumu pārskata likmju rediģēšanu”.</span><span class="sxs-lookup"><span data-stu-id="d27cf-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="d27cf-130">Tas jums ļauj manuāli pielāgot summu no mantojuma sistēmas.</span><span class="sxs-lookup"><span data-stu-id="d27cf-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="d27cf-131">B.</span><span class="sxs-lookup"><span data-stu-id="d27cf-131">B.</span></span> <span data-ttu-id="d27cf-132">Izveidot ienākumu izrakstu darbiniekam, kam nepieciešama sākuma bilance</span><span class="sxs-lookup"><span data-stu-id="d27cf-132">Create earnings statement for an employee to have a beginning balance</span></span>
<span data-ttu-id="d27cf-133">Šī darbība manuāli izveido ienākumu izrakstu katram nodarbinātajam par mantojuma sistēmas pēdējo apmaksas periodu, tādējādi izveidojot ienākumu izraksta rindas jaunajā algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="d27cf-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="d27cf-134">Ievadiet vienu rindu katram ienākumu veida kodam, kā arī līdzšinējā gada summu un stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="d27cf-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="d27cf-135">Piemēra darbības ir šādas:</span><span class="sxs-lookup"><span data-stu-id="d27cf-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="d27cf-136">Atveriet lapu **Visu ienākumu izraksti** un noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-136">Open the **All earnings statements** page and click **New**.</span></span>  

<span data-ttu-id="d27cf-137">Ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d27cf-137">Enter the following:</span></span> 

| <span data-ttu-id="d27cf-138">Lauks</span><span class="sxs-lookup"><span data-stu-id="d27cf-138">Field</span></span>      | <span data-ttu-id="d27cf-139">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d27cf-139">Value</span></span>                 |
|------------|-----------------------|
| <span data-ttu-id="d27cf-140">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="d27cf-140">Worker</span></span>     | <span data-ttu-id="d27cf-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="d27cf-141">Michael Redmond</span></span>       |
| <span data-ttu-id="d27cf-142">Apmaksas cikls</span><span class="sxs-lookup"><span data-stu-id="d27cf-142">Pay cycle</span></span>  | <span data-ttu-id="d27cf-143">sm</span><span class="sxs-lookup"><span data-stu-id="d27cf-143">sm</span></span>                    |
| <span data-ttu-id="d27cf-144">Apmaksas periods</span><span class="sxs-lookup"><span data-stu-id="d27cf-144">Pay period</span></span> | <span data-ttu-id="d27cf-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="d27cf-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="d27cf-146">Cilnē **Ienākumu izraksta rinda** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d27cf-146">In the **Earnings statement line** tab, enter the following:</span></span>

<span data-ttu-id="d27cf-147">1. rinda: cilne **Ienākumu izraksta rinda**</span><span class="sxs-lookup"><span data-stu-id="d27cf-147">Line 1: **Earning statement line** tab</span></span>

| <span data-ttu-id="d27cf-148">Lauks</span><span class="sxs-lookup"><span data-stu-id="d27cf-148">Field</span></span>            | <span data-ttu-id="d27cf-149">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d27cf-149">Value</span></span>       |
|------------------|-------------|
| <span data-ttu-id="d27cf-150">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="d27cf-150">Earnings code</span></span>    | <span data-ttu-id="d27cf-151">Regulārā samaksa</span><span class="sxs-lookup"><span data-stu-id="d27cf-151">Regular pay</span></span> |
| <span data-ttu-id="d27cf-152">Daudzums</span><span class="sxs-lookup"><span data-stu-id="d27cf-152">Quantity</span></span>         | <span data-ttu-id="d27cf-153">1,00</span><span class="sxs-lookup"><span data-stu-id="d27cf-153">1.00</span></span>        |
| <span data-ttu-id="d27cf-154">Diapazons</span><span class="sxs-lookup"><span data-stu-id="d27cf-154">Rage</span></span>             | <span data-ttu-id="d27cf-155">30 000</span><span class="sxs-lookup"><span data-stu-id="d27cf-155">30,000</span></span>      |
| <span data-ttu-id="d27cf-156">Cilne Detalizēta informācija par rindu</span><span class="sxs-lookup"><span data-stu-id="d27cf-156">Line details tab</span></span> |             |
| <span data-ttu-id="d27cf-157">Manuālā</span><span class="sxs-lookup"><span data-stu-id="d27cf-157">Manual</span></span>           | <span data-ttu-id="d27cf-158">(iezīmēts)</span><span class="sxs-lookup"><span data-stu-id="d27cf-158">(marked)</span></span>    |

<span data-ttu-id="d27cf-159">2. rinda: cilne **Ienākumu izraksta rinda**</span><span class="sxs-lookup"><span data-stu-id="d27cf-159">Line 2: **Earning statement line** tab</span></span>

| <span data-ttu-id="d27cf-160">Lauks</span><span class="sxs-lookup"><span data-stu-id="d27cf-160">Field</span></span>            | <span data-ttu-id="d27cf-161">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d27cf-161">Value</span></span>    |
|------------------|----------|
| <span data-ttu-id="d27cf-162">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="d27cf-162">Earnings code</span></span>    | <span data-ttu-id="d27cf-163">Bonuss</span><span class="sxs-lookup"><span data-stu-id="d27cf-163">Bonus</span></span>    |
| <span data-ttu-id="d27cf-164">Daudzums</span><span class="sxs-lookup"><span data-stu-id="d27cf-164">Quantity</span></span>         | <span data-ttu-id="d27cf-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="d27cf-165">1.0000</span></span>   |
| <span data-ttu-id="d27cf-166">Norma</span><span class="sxs-lookup"><span data-stu-id="d27cf-166">Rate</span></span>             | <span data-ttu-id="d27cf-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="d27cf-167">4250.00</span></span>  |
| <span data-ttu-id="d27cf-168">Cilne Detalizēta informācija par rindu</span><span class="sxs-lookup"><span data-stu-id="d27cf-168">Line details tab</span></span> |          |
| <span data-ttu-id="d27cf-169">Manuālā</span><span class="sxs-lookup"><span data-stu-id="d27cf-169">Manual</span></span>           | <span data-ttu-id="d27cf-170">(iezīmēts)</span><span class="sxs-lookup"><span data-stu-id="d27cf-170">(marked)</span></span> |

<span data-ttu-id="d27cf-171">3. rinda: cilne **Ienākumu izraksta rinda**</span><span class="sxs-lookup"><span data-stu-id="d27cf-171">Line 3: **Earning statement line** tab</span></span>

| <span data-ttu-id="d27cf-172">Lauks</span><span class="sxs-lookup"><span data-stu-id="d27cf-172">Field</span></span>           | <span data-ttu-id="d27cf-173">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d27cf-173">Value</span></span>      |
|-----------------|------------|
| <span data-ttu-id="d27cf-174">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="d27cf-174">Earnings code</span></span>   | <span data-ttu-id="d27cf-175">Komisija</span><span class="sxs-lookup"><span data-stu-id="d27cf-175">Commission</span></span> |
| <span data-ttu-id="d27cf-176">Daudzums</span><span class="sxs-lookup"><span data-stu-id="d27cf-176">Quantity</span></span>        | <span data-ttu-id="d27cf-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="d27cf-177">1.0000</span></span>     |
| <span data-ttu-id="d27cf-178">Norma</span><span class="sxs-lookup"><span data-stu-id="d27cf-178">Rate</span></span>            | <span data-ttu-id="d27cf-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="d27cf-179">!,299.00</span></span>   |
| <span data-ttu-id="d27cf-180">Norma</span><span class="sxs-lookup"><span data-stu-id="d27cf-180">Rate</span></span>            | <span data-ttu-id="d27cf-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="d27cf-181">1,299.00</span></span>   |
| <span data-ttu-id="d27cf-182">Cilne Detalizēta informācija par rindu</span><span class="sxs-lookup"><span data-stu-id="d27cf-182">Line detail tab</span></span> |            |
| <span data-ttu-id="d27cf-183">Manuālā</span><span class="sxs-lookup"><span data-stu-id="d27cf-183">Manual</span></span>          | <span data-ttu-id="d27cf-184">(iezīmēts)</span><span class="sxs-lookup"><span data-stu-id="d27cf-184">(Marked)</span></span>   |

> [!NOTE]
> <span data-ttu-id="d27cf-185">Slīdņa **Manuāli** iestatīšana uz **Jā** cilnē **Detalizēta informācija par rindu** katrai ienākumu izraksta rindai ir veids, kā likt ievadīt algu sākuma bilances katram nodarbinātajam.</span><span class="sxs-lookup"><span data-stu-id="d27cf-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="d27cf-186">Rūtī **Darbība** noklikšķiniet uz **Izlaist ienākumu izrakstu** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="d27cf-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>

4. <span data-ttu-id="d27cf-187">Rūtī **Darbība** noklikšķiniet uz **Algas pārskats**, lai atvērtu lapu **Ģenerēt algas pārskatus**, un iestatiet tālāk norādīto informāciju</span><span class="sxs-lookup"><span data-stu-id="d27cf-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

| <span data-ttu-id="d27cf-188">Lauks</span><span class="sxs-lookup"><span data-stu-id="d27cf-188">Field</span></span>              | <span data-ttu-id="d27cf-189">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d27cf-189">Value</span></span>     |
|--------------------|-----------|
| <span data-ttu-id="d27cf-190">Maksājuma datums</span><span class="sxs-lookup"><span data-stu-id="d27cf-190">Payment date</span></span>       | <span data-ttu-id="d27cf-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="d27cf-191">6/30/2017</span></span> |
| <span data-ttu-id="d27cf-192">Maksājuma izdošanas veids</span><span class="sxs-lookup"><span data-stu-id="d27cf-192">Payment run type</span></span>   | <span data-ttu-id="d27cf-193">Manuālā</span><span class="sxs-lookup"><span data-stu-id="d27cf-193">Manual</span></span>    |
| <span data-ttu-id="d27cf-194">Atspējot uzskaiti</span><span class="sxs-lookup"><span data-stu-id="d27cf-194">Disable accounting</span></span> |   <span data-ttu-id="d27cf-195">Jā</span><span class="sxs-lookup"><span data-stu-id="d27cf-195">Yes</span></span>     |

> [!NOTE] 
> <span data-ttu-id="d27cf-196">Šī darbība ir pieejama tikai tad, ja maksājuma izpildes tips ir manuāls un ja lietotājs vēlaties atspējot uzskaiti par apmaksas izpildi.</span><span class="sxs-lookup"><span data-stu-id="d27cf-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

<span data-ttu-id="d27cf-197">Noklikšķiniet uz **Labi** un aizveriet žurnālu **Informācijas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="d27cf-198">Kādēļ slīdnis Atspējot uzskaiti ir jāiestata uz Jā, ģenerējot algu pārskatus?</span><span class="sxs-lookup"><span data-stu-id="d27cf-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>
<span data-ttu-id="d27cf-199">Slīdni iestatot uz **Jā**, algas pārskatā netiek ļauta rindu izplatīšana virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="d27cf-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="d27cf-200">Virsgrāmatas summas tika atjauninātas iepriekš, kad tika ievadītas konta bilances no mantojuma sistēmas.</span><span class="sxs-lookup"><span data-stu-id="d27cf-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="d27cf-201">Ievadot algu sākuma bilances, varat ģenerēt pārskatus, kuros ietverta informācija no iepriekšējiem gadiem, kā arī identificēt ierobežojumus atvieglojumu un nodokļu nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="d27cf-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>   

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="d27cf-202">C.</span><span class="sxs-lookup"><span data-stu-id="d27cf-202">C.</span></span> <span data-ttu-id="d27cf-203">Izveidot algas pārskatus darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="d27cf-203">Create pay statements for employees</span></span>
<span data-ttu-id="d27cf-204">Kad ir izveidoti algas pārskati, kuriem ir sākuma bilances, ir jāpārbauda, vai šie algas pārskati precīzi atspoguļo algu datus.</span><span class="sxs-lookup"><span data-stu-id="d27cf-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="d27cf-205">Tāpat jums ir manuāli jāatjaunina atvieglojumu un nodokļu informācija, lai tā atbilstu vērtībām iepriekšējā algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="d27cf-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="d27cf-206">Kad esat pārbaudījis, vai summas no iepriekšējās algu sistēmas atbilst summām pašreizējos algas pārskatos, šie algas pārskati ir jāfinalizē.</span><span class="sxs-lookup"><span data-stu-id="d27cf-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="d27cf-207">Atveriet lapu **Visi algas pārskati**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-207">Open the **All pay statements** page.</span></span>

2. <span data-ttu-id="d27cf-208">Iezīmējiet pēdējo ģenerēto algas pārskatu darbiniekam Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="d27cf-208">Highlight the last generated pay statement for Michael Redmond</span></span>

3. <span data-ttu-id="d27cf-209">Noklikšķiniet uz **Rediģēt**, lai atvērtu lapu **Algas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-209">Click **Edit** to open the **Pay statement** page.</span></span>

4. <span data-ttu-id="d27cf-210">Atveriet cilni **Atvieglojumu ieturējumi** un ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d27cf-210">Open the **Benefit deductions** tab and enter the following:</span></span>

| <span data-ttu-id="d27cf-211">Lauks</span><span class="sxs-lookup"><span data-stu-id="d27cf-211">Field</span></span>                           | <span data-ttu-id="d27cf-212">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d27cf-212">Value</span></span>            |
|---------------------------------|------------------|
| <span data-ttu-id="d27cf-213">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="d27cf-213">Benefit</span></span>                         | <span data-ttu-id="d27cf-214">Ieturējuma summa</span><span class="sxs-lookup"><span data-stu-id="d27cf-214">Deduction amount</span></span> |
| <span data-ttu-id="d27cf-215">401K</span><span class="sxs-lookup"><span data-stu-id="d27cf-215">401K</span></span> | <span data-ttu-id="d27cf-216">Piedalīties</span><span class="sxs-lookup"><span data-stu-id="d27cf-216">Participate</span></span>              | <span data-ttu-id="d27cf-217">3000.00</span><span class="sxs-lookup"><span data-stu-id="d27cf-217">3000.00</span></span>          |
| <span data-ttu-id="d27cf-218">Zobārstniecība</span><span class="sxs-lookup"><span data-stu-id="d27cf-218">Dental</span></span> | <span data-ttu-id="d27cf-219">SubSp</span><span class="sxs-lookup"><span data-stu-id="d27cf-219">SubSp</span></span>                  | <span data-ttu-id="d27cf-220">495,00</span><span class="sxs-lookup"><span data-stu-id="d27cf-220">495.00</span></span>           |
| <span data-ttu-id="d27cf-221">Apg. aprūpes izdevumi</span><span class="sxs-lookup"><span data-stu-id="d27cf-221">Dep care spending</span></span> | <span data-ttu-id="d27cf-222">Piedalīties</span><span class="sxs-lookup"><span data-stu-id="d27cf-222">Participate</span></span> | <span data-ttu-id="d27cf-223">2500.00</span><span class="sxs-lookup"><span data-stu-id="d27cf-223">2500.00</span></span>          |
| <span data-ttu-id="d27cf-224">Redze</span><span class="sxs-lookup"><span data-stu-id="d27cf-224">Vision</span></span> | <span data-ttu-id="d27cf-225">SupSp</span><span class="sxs-lookup"><span data-stu-id="d27cf-225">SupSp</span></span>                  | <span data-ttu-id="d27cf-226">500,00</span><span class="sxs-lookup"><span data-stu-id="d27cf-226">500.00</span></span>           |

5. <span data-ttu-id="d27cf-227">Cilnē **Atvieglojumu iemaksas** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d27cf-227">In the **Benefit contributions** tab and enter the following:</span></span>

| <span data-ttu-id="d27cf-228">Lauks</span><span class="sxs-lookup"><span data-stu-id="d27cf-228">Field</span></span>              | <span data-ttu-id="d27cf-229">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d27cf-229">Value</span></span>               |
|--------------------|---------------------|
| <span data-ttu-id="d27cf-230">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="d27cf-230">Benefit</span></span>            | <span data-ttu-id="d27cf-231">Seguma summa</span><span class="sxs-lookup"><span data-stu-id="d27cf-231">Contribution amount</span></span> |
| <span data-ttu-id="d27cf-232">401K</span><span class="sxs-lookup"><span data-stu-id="d27cf-232">401K</span></span> | <span data-ttu-id="d27cf-233">Piedalīties</span><span class="sxs-lookup"><span data-stu-id="d27cf-233">Participate</span></span> | <span data-ttu-id="d27cf-234">3000,00</span><span class="sxs-lookup"><span data-stu-id="d27cf-234">3000,00</span></span>             |
| <span data-ttu-id="d27cf-235">Zobārstniecība</span><span class="sxs-lookup"><span data-stu-id="d27cf-235">Dental</span></span> | <span data-ttu-id="d27cf-236">SubSp</span><span class="sxs-lookup"><span data-stu-id="d27cf-236">SubSp</span></span>     | <span data-ttu-id="d27cf-237">495,00</span><span class="sxs-lookup"><span data-stu-id="d27cf-237">495.00</span></span>              |
| <span data-ttu-id="d27cf-238">Redze</span><span class="sxs-lookup"><span data-stu-id="d27cf-238">Vision</span></span> | <span data-ttu-id="d27cf-239">SubSp</span><span class="sxs-lookup"><span data-stu-id="d27cf-239">SubSp</span></span>     | <span data-ttu-id="d27cf-240">500,00</span><span class="sxs-lookup"><span data-stu-id="d27cf-240">500.00</span></span>              |

6. <span data-ttu-id="d27cf-241">Cilnē **Nodokļu ieturējumi** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d27cf-241">In the **Tax deductions** tab, enter the following:</span></span>

| <span data-ttu-id="d27cf-242">Lauks</span><span class="sxs-lookup"><span data-stu-id="d27cf-242">Field</span></span>           | <span data-ttu-id="d27cf-243">Vērtība</span><span class="sxs-lookup"><span data-stu-id="d27cf-243">Value</span></span>            |
|-----------------|------------------|
| <span data-ttu-id="d27cf-244">Nodokļa kods</span><span class="sxs-lookup"><span data-stu-id="d27cf-244">Tax code</span></span>        | <span data-ttu-id="d27cf-245">Ieturējuma summa</span><span class="sxs-lookup"><span data-stu-id="d27cf-245">Deduction amount</span></span> |
| <span data-ttu-id="d27cf-246">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="d27cf-246">USA-FED-ER-FICA</span></span> | <span data-ttu-id="d27cf-247">1600.00</span><span class="sxs-lookup"><span data-stu-id="d27cf-247">1600.00</span></span>          |
| <span data-ttu-id="d27cf-248">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="d27cf-248">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="d27cf-249">825.75</span><span class="sxs-lookup"><span data-stu-id="d27cf-249">825.75</span></span>           |

7. <span data-ttu-id="d27cf-250">Cilnē **Nodokļu iemaksas** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d27cf-250">In the **Tax contributions** tab enter the following:</span></span>

8. <span data-ttu-id="d27cf-251">Noklikšķiniet uz **Aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-251">Click **Calculate**.</span></span>
> [!IMPORTANT] 
> <span data-ttu-id="d27cf-252">Pārliecinieties, ka algas pārskata kopsummas atbilst mantojuma sistēmas šī nodarbinātā līdzšinējā gada kopsummām.</span><span class="sxs-lookup"><span data-stu-id="d27cf-252">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="d27cf-253">Iespējams, finalizēšana ir jāatliek uz nākamo darbību, lai veiktu visu algas pārskatu vispārēju validēšanu kopumā.</span><span class="sxs-lookup"><span data-stu-id="d27cf-253">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="d27cf-254">Pēc validēšanas izejiet cauri visiem algas pārskatiem un finalizējiet tos.</span><span class="sxs-lookup"><span data-stu-id="d27cf-254">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="d27cf-255">Šo pašu procedūru var veikt ar ceturkšņa intervāliem, ja nepieciešams, visiem iepriekšējiem ceturkšņiem katru gadu.</span><span class="sxs-lookup"><span data-stu-id="d27cf-255">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="d27cf-256">Tas ir jādara tikai tad, ja klientam ir nepieciešams datus redzēt pa ceturksnim, neatgriežoties mantojuma sistēmā.</span><span class="sxs-lookup"><span data-stu-id="d27cf-256">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="d27cf-257">Ja pieļaujat kļūdu, ievadot darbinieka sākuma bilances</span><span class="sxs-lookup"><span data-stu-id="d27cf-257">If you make a mistake Entering Beginning Balances for an Employee</span></span>
<span data-ttu-id="d27cf-258">Transakcijas ir iespējams atsaukt un ievadīt no jauna.</span><span class="sxs-lookup"><span data-stu-id="d27cf-258">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="d27cf-259">Lai transakciju atsauktu, jums ir tikai jāizpilda tālāk norādītās darbības lapā **Visi algas pārskati**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-259">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="d27cf-260">Noklikšķiniet uz **Atsaukt**.</span><span class="sxs-lookup"><span data-stu-id="d27cf-260">Click **Reverse**.</span></span>

2. <span data-ttu-id="d27cf-261">Noklikšķiniet uz **Jā**, kad tiek parādīts ziņojums “Kad anulējat šo algas pārskatu, tiek izveidots anulēšanas algas pārskats, lai kompensētu šo algas pārskatu.</span><span class="sxs-lookup"><span data-stu-id="d27cf-261">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="d27cf-262">Nevienu no algas pārskatiem nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="d27cf-262">Neither pay statement can be edited.</span></span> <span data-ttu-id="d27cf-263">Vai vēlaties anulēt šo samaksas</span><span class="sxs-lookup"><span data-stu-id="d27cf-263">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="d27cf-264">pārskatu?”</span><span class="sxs-lookup"><span data-stu-id="d27cf-264">displays.</span></span> 

<span data-ttu-id="d27cf-265">Pēc algas pārskata anulēšanas varat ģenerēt jaunu nodarbinātā algas pārskatu no iepriekš izveidotā ienākumu izraksta.</span><span class="sxs-lookup"><span data-stu-id="d27cf-265">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="d27cf-266">Pirms ģenerējat jauno algas pārskatu, noteikti labojiet visas nepareizās ienākumu izraksta rindas, un pēc tam ģenerējiet jauno algas pārskatu ar pareizajām summām.</span><span class="sxs-lookup"><span data-stu-id="d27cf-266">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 

