---
title: Ievadīt algu sākuma bilances
description: Šajā tēmā ir aprakstītas darbības sākuma bilanču ievadīšanai attiecībā uz ienākumu veida kodiem, ieturējumiem, atvieglojumiem un nodokļiem. Šī informācija ir vērtīga partneriem, lai datus jaunai algu ieviešanai migrētu vai pārsūtītu no citas sistēmas.
author: kherr75
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4bb8f565f5bf5630a7c5f8602b96e569692bc7c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507988"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="74fa5-104">Ievadīt algu sākuma bilances</span><span class="sxs-lookup"><span data-stu-id="74fa5-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74fa5-105">Šajā tēmā ir aprakstītas darbības sākuma bilanču ievadīšanai attiecībā uz ienākumu veida kodiem, ieturējumiem, atvieglojumiem un nodokļiem.</span><span class="sxs-lookup"><span data-stu-id="74fa5-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="74fa5-106">Šī informācija ir vērtīga partneriem, kuri datus jaunai algu ieviešanai pārsūtīta no citas sistēmas.</span><span class="sxs-lookup"><span data-stu-id="74fa5-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="74fa5-107">Lai sagatavotos ievadīt sākuma algu bilances, mēs pārbaudām tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="74fa5-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="74fa5-108">Darbinieka ieraksti ir ievadīti un ir pieejami sistēmā</span><span class="sxs-lookup"><span data-stu-id="74fa5-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="74fa5-109">Darbiniekiem tiek iestatīti un tiek piešķirti tālāk norādītie dati.</span><span class="sxs-lookup"><span data-stu-id="74fa5-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="74fa5-110">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="74fa5-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="74fa5-111">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="74fa5-111">Earning codes</span></span>
    - <span data-ttu-id="74fa5-112">Nodokļi</span><span class="sxs-lookup"><span data-stu-id="74fa5-112">Taxes</span></span>
    - <span data-ttu-id="74fa5-113">Atvieglojumi un atvilkumi</span><span class="sxs-lookup"><span data-stu-id="74fa5-113">Benefits and deductions</span></span>

- <span data-ttu-id="74fa5-114">Uzņēmumam ir jāizvēlas datums, kur var iestatīt algu sākuma bilances.</span><span class="sxs-lookup"><span data-stu-id="74fa5-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="74fa5-115">No mantojuma sistēmas tika vākta informācija par visiem ienākumiem, atvieglojumiem/atvilkumiem, atvieglojumu iemaksām, darbinieka nodokļiem un darba devēja nodokļiem, un to līdzšinējā gada (YTD) summām.</span><span class="sxs-lookup"><span data-stu-id="74fa5-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="74fa5-116">Kad plānojat ievadīt sākuma bilances, apsveriet, cik detalizētai šai informācijai ir jābūt.</span><span class="sxs-lookup"><span data-stu-id="74fa5-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="74fa5-117">Vairums uzņēmumu ievada vienu, konsolidētu līdzšinējā gada summu.</span><span class="sxs-lookup"><span data-stu-id="74fa5-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="74fa5-118">Taču, ja ir nepieciešama sīkāka informācija, bilances var ievadīt ar ceturkšņa pieaugumu.</span><span class="sxs-lookup"><span data-stu-id="74fa5-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="74fa5-119">Lēmums par nepieciešamo detalizētības līmeni arī nosaka, cik manuālo algas pārskatu ir jāizveido katram nodarbinātajam.</span><span class="sxs-lookup"><span data-stu-id="74fa5-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="74fa5-120">Vienai līdzšinējā gada summai katram darbiniekam ir nepieciešams tikai viens manuāls pārskats.</span><span class="sxs-lookup"><span data-stu-id="74fa5-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="74fa5-121">Lai to izdarītu, kā jaunajā algu sistēmā ievadīto summu izmantojiet līdzšinējā gada summas no iepriekšējās sistēmas gala algas pārskata.</span><span class="sxs-lookup"><span data-stu-id="74fa5-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="74fa5-122">Nākamajā piemērā ir parādīts, kā varat ievadīt darbinieku algu sākuma bilances, tostarp ienākumu veida kodus, atvieglojumu/atvilkumus un nodokļus.</span><span class="sxs-lookup"><span data-stu-id="74fa5-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="74fa5-123">Reālā piemērā jums būtu rindas krājums katram ienākumu veida kodam, atvieglojuma ieturējumam, atvieglojumu iemaksai, darbinieka nodoklim un darba devēja nodoklim, kuru ievadītā summa ir līdzšinējā gada summa.</span><span class="sxs-lookup"><span data-stu-id="74fa5-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="74fa5-124">Izmantojot šo kodu un summu sarakstu, izpildiet norādījumus par manuāla ienākumu un algas pārskata izveidošanu ar atspējotu uzskaiti, lai pārceltu sākuma bilances algu nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="74fa5-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="74fa5-125">Uzskaite ir jāatspējo, jo šo sākuma bilances algas pārskatu jūs nevēlaties grāmatot savā virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="74fa5-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="74fa5-126">Tas tika izdarīts mantojuma sistēmā un pārnāk uz jauno sistēmu, kad virsgrāmatā iestatāt sākuma bilances.</span><span class="sxs-lookup"><span data-stu-id="74fa5-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="74fa5-127">A.</span><span class="sxs-lookup"><span data-stu-id="74fa5-127">A.</span></span> <span data-ttu-id="74fa5-128">Kā iestatīt ienākumu veida kodus, ko izmantot algu sākuma bilancēm</span><span class="sxs-lookup"><span data-stu-id="74fa5-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="74fa5-129">Kad ievadāt algu sākuma bilances, pārliecinieties, ka ienākumu veida kodi, kurus jūs izmantosiet, ir konfigurēti ar iespējotu opciju “Atļaut ienākumu pārskata likmju rediģēšanu”.</span><span class="sxs-lookup"><span data-stu-id="74fa5-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="74fa5-130">Tas jums ļauj manuāli pielāgot summu no mantojuma sistēmas.</span><span class="sxs-lookup"><span data-stu-id="74fa5-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="74fa5-131">B.</span><span class="sxs-lookup"><span data-stu-id="74fa5-131">B.</span></span> <span data-ttu-id="74fa5-132">Izveidot ienākumu izrakstu darbiniekam, kam nepieciešama sākuma bilance</span><span class="sxs-lookup"><span data-stu-id="74fa5-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="74fa5-133">Šī darbība manuāli izveido ienākumu izrakstu katram nodarbinātajam par mantojuma sistēmas pēdējo apmaksas periodu, tādējādi izveidojot ienākumu izraksta rindas jaunajā algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="74fa5-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="74fa5-134">Ievadiet vienu rindu katram ienākumu veida kodam, kā arī līdzšinējā gada summu un stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="74fa5-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="74fa5-135">Piemēra darbības ir šādas:</span><span class="sxs-lookup"><span data-stu-id="74fa5-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="74fa5-136">Atveriet lapu **Visu ienākumu izraksti** un noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="74fa5-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="74fa5-137">Ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="74fa5-137">Enter the following:</span></span> 

    | <span data-ttu-id="74fa5-138">Lauks</span><span class="sxs-lookup"><span data-stu-id="74fa5-138">Field</span></span>      | <span data-ttu-id="74fa5-139">Vērtība</span><span class="sxs-lookup"><span data-stu-id="74fa5-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="74fa5-140">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="74fa5-140">Worker</span></span>     | <span data-ttu-id="74fa5-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="74fa5-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="74fa5-142">Apmaksas cikls</span><span class="sxs-lookup"><span data-stu-id="74fa5-142">Pay cycle</span></span>  | <span data-ttu-id="74fa5-143">sm</span><span class="sxs-lookup"><span data-stu-id="74fa5-143">sm</span></span>                    |
    | <span data-ttu-id="74fa5-144">Apmaksas periods</span><span class="sxs-lookup"><span data-stu-id="74fa5-144">Pay period</span></span> | <span data-ttu-id="74fa5-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="74fa5-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="74fa5-146">Cilnē **Ienākumu izraksta rinda** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="74fa5-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="74fa5-147">1. rinda: cilne **Ienākumu izraksta rinda**</span><span class="sxs-lookup"><span data-stu-id="74fa5-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="74fa5-148">Lauks</span><span class="sxs-lookup"><span data-stu-id="74fa5-148">Field</span></span>            | <span data-ttu-id="74fa5-149">Vērtība</span><span class="sxs-lookup"><span data-stu-id="74fa5-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="74fa5-150">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="74fa5-150">Earnings code</span></span>    | <span data-ttu-id="74fa5-151">Regulārā samaksa</span><span class="sxs-lookup"><span data-stu-id="74fa5-151">Regular pay</span></span> |
    | <span data-ttu-id="74fa5-152">Daudzums</span><span class="sxs-lookup"><span data-stu-id="74fa5-152">Quantity</span></span>         | <span data-ttu-id="74fa5-153">1.00</span><span class="sxs-lookup"><span data-stu-id="74fa5-153">1.00</span></span>        |
    | <span data-ttu-id="74fa5-154">Norma</span><span class="sxs-lookup"><span data-stu-id="74fa5-154">Rate</span></span>             | <span data-ttu-id="74fa5-155">30,000</span><span class="sxs-lookup"><span data-stu-id="74fa5-155">30,000</span></span>      |
    | <span data-ttu-id="74fa5-156">Cilne Detalizēta informācija par rindu</span><span class="sxs-lookup"><span data-stu-id="74fa5-156">Line details tab</span></span> |             |
    | <span data-ttu-id="74fa5-157">Manuāli</span><span class="sxs-lookup"><span data-stu-id="74fa5-157">Manual</span></span>           | <span data-ttu-id="74fa5-158">(iezīmēts)</span><span class="sxs-lookup"><span data-stu-id="74fa5-158">(marked)</span></span>    |

    <span data-ttu-id="74fa5-159">2. rinda: cilne **Ienākumu izraksta rinda**</span><span class="sxs-lookup"><span data-stu-id="74fa5-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="74fa5-160">Lauks</span><span class="sxs-lookup"><span data-stu-id="74fa5-160">Field</span></span>            | <span data-ttu-id="74fa5-161">Vērtība</span><span class="sxs-lookup"><span data-stu-id="74fa5-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="74fa5-162">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="74fa5-162">Earnings code</span></span>    | <span data-ttu-id="74fa5-163">Bonuss</span><span class="sxs-lookup"><span data-stu-id="74fa5-163">Bonus</span></span>    |
    | <span data-ttu-id="74fa5-164">Daudzums</span><span class="sxs-lookup"><span data-stu-id="74fa5-164">Quantity</span></span>         | <span data-ttu-id="74fa5-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="74fa5-165">1.0000</span></span>   |
    | <span data-ttu-id="74fa5-166">Norma</span><span class="sxs-lookup"><span data-stu-id="74fa5-166">Rate</span></span>             | <span data-ttu-id="74fa5-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="74fa5-167">4250.00</span></span>  |
    | <span data-ttu-id="74fa5-168">Cilne Detalizēta informācija par rindu</span><span class="sxs-lookup"><span data-stu-id="74fa5-168">Line details tab</span></span> |          |
    | <span data-ttu-id="74fa5-169">Manuālā</span><span class="sxs-lookup"><span data-stu-id="74fa5-169">Manual</span></span>           | <span data-ttu-id="74fa5-170">(iezīmēts)</span><span class="sxs-lookup"><span data-stu-id="74fa5-170">(marked)</span></span> |

    <span data-ttu-id="74fa5-171">3. rinda: cilne **Ienākumu izraksta rinda**</span><span class="sxs-lookup"><span data-stu-id="74fa5-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="74fa5-172">Lauks</span><span class="sxs-lookup"><span data-stu-id="74fa5-172">Field</span></span>           | <span data-ttu-id="74fa5-173">Vērtība</span><span class="sxs-lookup"><span data-stu-id="74fa5-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="74fa5-174">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="74fa5-174">Earnings code</span></span>   | <span data-ttu-id="74fa5-175">Komisija</span><span class="sxs-lookup"><span data-stu-id="74fa5-175">Commission</span></span> |
    | <span data-ttu-id="74fa5-176">Daudzums</span><span class="sxs-lookup"><span data-stu-id="74fa5-176">Quantity</span></span>        | <span data-ttu-id="74fa5-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="74fa5-177">1.0000</span></span>     |
    | <span data-ttu-id="74fa5-178">Norma</span><span class="sxs-lookup"><span data-stu-id="74fa5-178">Rate</span></span>            | <span data-ttu-id="74fa5-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="74fa5-179">!,299.00</span></span>   |
    | <span data-ttu-id="74fa5-180">Norma</span><span class="sxs-lookup"><span data-stu-id="74fa5-180">Rate</span></span>            | <span data-ttu-id="74fa5-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="74fa5-181">1,299.00</span></span>   |
    | <span data-ttu-id="74fa5-182">Cilne Detalizēta informācija par rindu</span><span class="sxs-lookup"><span data-stu-id="74fa5-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="74fa5-183">Manuālā</span><span class="sxs-lookup"><span data-stu-id="74fa5-183">Manual</span></span>          | <span data-ttu-id="74fa5-184">(iezīmēts)</span><span class="sxs-lookup"><span data-stu-id="74fa5-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="74fa5-185">Slīdņa **Manuāli** iestatīšana uz **Jā** cilnē **Detalizēta informācija par rindu** katrai ienākumu izraksta rindai ir veids, kā likt ievadīt algu sākuma bilances katram nodarbinātajam.</span><span class="sxs-lookup"><span data-stu-id="74fa5-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="74fa5-186">Rūtī **Darbība** noklikšķiniet uz **Izlaist ienākumu izrakstu** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="74fa5-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="74fa5-187">Rūtī **Darbība** noklikšķiniet uz **Algas pārskats**, lai atvērtu lapu **Ģenerēt algas pārskatus**, un iestatiet tālāk norādīto informāciju</span><span class="sxs-lookup"><span data-stu-id="74fa5-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="74fa5-188">Lauks</span><span class="sxs-lookup"><span data-stu-id="74fa5-188">Field</span></span>              | <span data-ttu-id="74fa5-189">Vērtība</span><span class="sxs-lookup"><span data-stu-id="74fa5-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="74fa5-190">Maksājuma datums</span><span class="sxs-lookup"><span data-stu-id="74fa5-190">Payment date</span></span>       | <span data-ttu-id="74fa5-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="74fa5-191">6/30/2017</span></span> |
    | <span data-ttu-id="74fa5-192">Maksājuma izdošanas veids</span><span class="sxs-lookup"><span data-stu-id="74fa5-192">Payment run type</span></span>   | <span data-ttu-id="74fa5-193">Manuālā</span><span class="sxs-lookup"><span data-stu-id="74fa5-193">Manual</span></span>    |
    | <span data-ttu-id="74fa5-194">Atspējot uzskaiti</span><span class="sxs-lookup"><span data-stu-id="74fa5-194">Disable accounting</span></span> |   <span data-ttu-id="74fa5-195">Jā</span><span class="sxs-lookup"><span data-stu-id="74fa5-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="74fa5-196">Šī darbība ir pieejama tikai tad, ja maksājuma izpildes tips ir manuāls un ja lietotājs vēlaties atspējot uzskaiti par apmaksas izpildi.</span><span class="sxs-lookup"><span data-stu-id="74fa5-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="74fa5-197">Noklikšķiniet uz **Labi** un aizveriet žurnālu **Informācijas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="74fa5-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="74fa5-198">Kādēļ slīdnis Atspējot uzskaiti ir jāiestata uz Jā, ģenerējot algu pārskatus?</span><span class="sxs-lookup"><span data-stu-id="74fa5-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="74fa5-199">Slīdni iestatot uz **Jā**, algas pārskatā netiek ļauta rindu izplatīšana virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="74fa5-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="74fa5-200">Virsgrāmatas summas tika atjauninātas iepriekš, kad tika ievadītas konta bilances no mantojuma sistēmas.</span><span class="sxs-lookup"><span data-stu-id="74fa5-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="74fa5-201">Ievadot algu sākuma bilances, varat ģenerēt pārskatus, kuros ietverta informācija no iepriekšējiem gadiem, kā arī identificēt ierobežojumus atvieglojumu un nodokļu nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="74fa5-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="74fa5-202">C.</span><span class="sxs-lookup"><span data-stu-id="74fa5-202">C.</span></span> <span data-ttu-id="74fa5-203">Izveidot algas pārskatus darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="74fa5-203">Create pay statements for employees</span></span>

<span data-ttu-id="74fa5-204">Kad ir izveidoti algas pārskati, kuriem ir sākuma bilances, ir jāpārbauda, vai šie algas pārskati precīzi atspoguļo algu datus.</span><span class="sxs-lookup"><span data-stu-id="74fa5-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="74fa5-205">Tāpat jums ir manuāli jāatjaunina atvieglojumu un nodokļu informācija, lai tā atbilstu vērtībām iepriekšējā algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="74fa5-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="74fa5-206">Kad esat pārbaudījis, vai summas no iepriekšējās algu sistēmas atbilst summām pašreizējos algas pārskatos, šie algas pārskati ir jāfinalizē.</span><span class="sxs-lookup"><span data-stu-id="74fa5-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="74fa5-207">Atveriet lapu **Visi algas pārskati**.</span><span class="sxs-lookup"><span data-stu-id="74fa5-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="74fa5-208">Iezīmējiet pēdējo ģenerēto algas pārskatu darbiniekam Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="74fa5-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="74fa5-209">Noklikšķiniet uz **Rediģēt**, lai atvērtu lapu **Algas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="74fa5-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="74fa5-210">Atveriet cilni **Atvieglojumu ieturējumi** un ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="74fa5-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="74fa5-211">Lauks</span><span class="sxs-lookup"><span data-stu-id="74fa5-211">Field</span></span>             | <span data-ttu-id="74fa5-212">Vērtība</span><span class="sxs-lookup"><span data-stu-id="74fa5-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="74fa5-213">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="74fa5-213">Benefit</span></span>           | <span data-ttu-id="74fa5-214">Ieturējuma summa</span><span class="sxs-lookup"><span data-stu-id="74fa5-214">Deduction amount</span></span> |
    | <span data-ttu-id="74fa5-215">401K</span><span class="sxs-lookup"><span data-stu-id="74fa5-215">401K</span></span>              | <span data-ttu-id="74fa5-216">Piedalīties</span><span class="sxs-lookup"><span data-stu-id="74fa5-216">Participate</span></span>      |
    | <span data-ttu-id="74fa5-217">Zobārstniecība</span><span class="sxs-lookup"><span data-stu-id="74fa5-217">Dental</span></span>            | <span data-ttu-id="74fa5-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="74fa5-218">SubSp</span></span>            |
    | <span data-ttu-id="74fa5-219">Apg. aprūpes izdevumi</span><span class="sxs-lookup"><span data-stu-id="74fa5-219">Dep care spending</span></span> | <span data-ttu-id="74fa5-220">Piedalīties</span><span class="sxs-lookup"><span data-stu-id="74fa5-220">Participate</span></span>      |
    | <span data-ttu-id="74fa5-221">Redze</span><span class="sxs-lookup"><span data-stu-id="74fa5-221">Vision</span></span>            | <span data-ttu-id="74fa5-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="74fa5-222">SupSp</span></span>            |

5. <span data-ttu-id="74fa5-223">Cilnē **Atvieglojumu iemaksas** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="74fa5-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="74fa5-224">Lauks</span><span class="sxs-lookup"><span data-stu-id="74fa5-224">Field</span></span>   | <span data-ttu-id="74fa5-225">Vērtība</span><span class="sxs-lookup"><span data-stu-id="74fa5-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="74fa5-226">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="74fa5-226">Benefit</span></span> | <span data-ttu-id="74fa5-227">Seguma summa</span><span class="sxs-lookup"><span data-stu-id="74fa5-227">Contribution amount</span></span> |
    | <span data-ttu-id="74fa5-228">401K</span><span class="sxs-lookup"><span data-stu-id="74fa5-228">401K</span></span>    | <span data-ttu-id="74fa5-229">Piedalīties</span><span class="sxs-lookup"><span data-stu-id="74fa5-229">Participate</span></span>         |
    | <span data-ttu-id="74fa5-230">Zobārstniecība</span><span class="sxs-lookup"><span data-stu-id="74fa5-230">Dental</span></span>  | <span data-ttu-id="74fa5-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="74fa5-231">SubSp</span></span>               |
    | <span data-ttu-id="74fa5-232">Redze</span><span class="sxs-lookup"><span data-stu-id="74fa5-232">Vision</span></span>  | <span data-ttu-id="74fa5-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="74fa5-233">SubSp</span></span>               |

6. <span data-ttu-id="74fa5-234">Cilnē **Nodokļu ieturējumi** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="74fa5-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="74fa5-235">Lauks</span><span class="sxs-lookup"><span data-stu-id="74fa5-235">Field</span></span>           | <span data-ttu-id="74fa5-236">Vērtība</span><span class="sxs-lookup"><span data-stu-id="74fa5-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="74fa5-237">Nodokļa kods</span><span class="sxs-lookup"><span data-stu-id="74fa5-237">Tax code</span></span>        | <span data-ttu-id="74fa5-238">Ieturējuma summa</span><span class="sxs-lookup"><span data-stu-id="74fa5-238">Deduction amount</span></span> |
    | <span data-ttu-id="74fa5-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="74fa5-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="74fa5-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="74fa5-240">1600.00</span></span>          |
    | <span data-ttu-id="74fa5-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="74fa5-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="74fa5-242">825.75</span><span class="sxs-lookup"><span data-stu-id="74fa5-242">825.75</span></span>           |

7. <span data-ttu-id="74fa5-243">Cilnē **Nodokļu iemaksas** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="74fa5-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="74fa5-244">Noklikšķiniet uz **Aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="74fa5-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="74fa5-245">Pārliecinieties, ka algas pārskata kopsummas atbilst mantojuma sistēmas šī nodarbinātā līdzšinējā gada kopsummām.</span><span class="sxs-lookup"><span data-stu-id="74fa5-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="74fa5-246">Iespējams, finalizēšana ir jāatliek uz nākamo darbību, lai veiktu visu algas pārskatu vispārēju validēšanu kopumā.</span><span class="sxs-lookup"><span data-stu-id="74fa5-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="74fa5-247">Pēc validēšanas izejiet cauri visiem algas pārskatiem un finalizējiet tos.</span><span class="sxs-lookup"><span data-stu-id="74fa5-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="74fa5-248">Šo pašu procedūru var veikt ar ceturkšņa intervāliem, ja nepieciešams, visiem iepriekšējiem ceturkšņiem katru gadu.</span><span class="sxs-lookup"><span data-stu-id="74fa5-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="74fa5-249">Tas ir jādara tikai tad, ja klientam ir nepieciešams datus redzēt pa ceturksnim, neatgriežoties mantojuma sistēmā.</span><span class="sxs-lookup"><span data-stu-id="74fa5-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="74fa5-250">Ja pieļaujat kļūdu, ievadot darbinieka sākuma bilances</span><span class="sxs-lookup"><span data-stu-id="74fa5-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="74fa5-251">Transakcijas ir iespējams atsaukt un ievadīt no jauna.</span><span class="sxs-lookup"><span data-stu-id="74fa5-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="74fa5-252">Lai transakciju atsauktu, jums ir tikai jāizpilda tālāk norādītās darbības lapā **Visi algas pārskati**.</span><span class="sxs-lookup"><span data-stu-id="74fa5-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="74fa5-253">Noklikšķiniet uz **Atsaukt**.</span><span class="sxs-lookup"><span data-stu-id="74fa5-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="74fa5-254">Noklikšķiniet uz **Jā**, kad tiek parādīts ziņojums “Kad anulējat šo algas pārskatu, tiek izveidots anulēšanas algas pārskats, lai kompensētu šo algas pārskatu.</span><span class="sxs-lookup"><span data-stu-id="74fa5-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="74fa5-255">Nevienu no algas pārskatiem nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="74fa5-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="74fa5-256">Vai vēlaties anulēt šo samaksas</span><span class="sxs-lookup"><span data-stu-id="74fa5-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="74fa5-257">pārskatu?”</span><span class="sxs-lookup"><span data-stu-id="74fa5-257">displays.</span></span> 

<span data-ttu-id="74fa5-258">Pēc algas pārskata anulēšanas varat ģenerēt jaunu nodarbinātā algas pārskatu no iepriekš izveidotā ienākumu izraksta.</span><span class="sxs-lookup"><span data-stu-id="74fa5-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="74fa5-259">Pirms ģenerējat jauno algas pārskatu, noteikti labojiet visas nepareizās ienākumu izraksta rindas, un pēc tam ģenerējiet jauno algas pārskatu ar pareizajām summām.</span><span class="sxs-lookup"><span data-stu-id="74fa5-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 
