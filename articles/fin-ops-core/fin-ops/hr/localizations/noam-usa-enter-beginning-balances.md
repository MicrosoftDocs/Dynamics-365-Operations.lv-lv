---
title: Ievadīt algu sākuma bilances
description: Šajā tēmā ir aprakstītas darbības sākuma bilanču ievadīšanai attiecībā uz ienākumu veida kodiem, ieturējumiem, atvieglojumiem un nodokļiem.
author: andreabichsel
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752154"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="1efdd-103">Ievadīt algu sākuma bilances</span><span class="sxs-lookup"><span data-stu-id="1efdd-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1efdd-104">Šajā tēmā ir aprakstītas darbības sākuma bilanču ievadīšanai attiecībā uz ienākumu veida kodiem, ieturējumiem, atvieglojumiem un nodokļiem.</span><span class="sxs-lookup"><span data-stu-id="1efdd-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="1efdd-105">Šī informācija ir vērtīga partneriem, kuri datus jaunai algu ieviešanai pārsūtīta no citas sistēmas.</span><span class="sxs-lookup"><span data-stu-id="1efdd-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="1efdd-106">Lai sagatavotos ievadīt sākuma algu bilances, mēs pārbaudām tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="1efdd-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="1efdd-107">Darbinieka ieraksti ir ievadīti un ir pieejami sistēmā</span><span class="sxs-lookup"><span data-stu-id="1efdd-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="1efdd-108">Darbiniekiem tiek iestatīti un tiek piešķirti tālāk norādītie dati.</span><span class="sxs-lookup"><span data-stu-id="1efdd-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="1efdd-109">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="1efdd-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="1efdd-110">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="1efdd-110">Earning codes</span></span>
    - <span data-ttu-id="1efdd-111">Nodokļi</span><span class="sxs-lookup"><span data-stu-id="1efdd-111">Taxes</span></span>
    - <span data-ttu-id="1efdd-112">Atvieglojumi un atvilkumi</span><span class="sxs-lookup"><span data-stu-id="1efdd-112">Benefits and deductions</span></span>

- <span data-ttu-id="1efdd-113">Uzņēmumam ir jāizvēlas datums, kur var iestatīt algu sākuma bilances.</span><span class="sxs-lookup"><span data-stu-id="1efdd-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="1efdd-114">No mantojuma sistēmas tika vākta informācija par visiem ienākumiem, atvieglojumiem/atvilkumiem, atvieglojumu iemaksām, darbinieka nodokļiem un darba devēja nodokļiem, un to līdzšinējā gada (YTD) summām.</span><span class="sxs-lookup"><span data-stu-id="1efdd-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="1efdd-115">Kad plānojat ievadīt sākuma bilances, apsveriet, cik detalizētai šai informācijai ir jābūt.</span><span class="sxs-lookup"><span data-stu-id="1efdd-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="1efdd-116">Vairums uzņēmumu ievada vienu, konsolidētu līdzšinējā gada summu.</span><span class="sxs-lookup"><span data-stu-id="1efdd-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="1efdd-117">Taču, ja ir nepieciešama sīkāka informācija, bilances var ievadīt ar ceturkšņa pieaugumu.</span><span class="sxs-lookup"><span data-stu-id="1efdd-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="1efdd-118">Lēmums par nepieciešamo detalizētības līmeni arī nosaka, cik manuālo algas pārskatu ir jāizveido katram nodarbinātajam.</span><span class="sxs-lookup"><span data-stu-id="1efdd-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="1efdd-119">Vienai līdzšinējā gada summai katram darbiniekam ir nepieciešams tikai viens manuāls pārskats.</span><span class="sxs-lookup"><span data-stu-id="1efdd-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="1efdd-120">Lai to izdarītu, kā jaunajā algu sistēmā ievadīto summu izmantojiet līdzšinējā gada summas no iepriekšējās sistēmas gala algas pārskata.</span><span class="sxs-lookup"><span data-stu-id="1efdd-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="1efdd-121">Nākamajā piemērā ir parādīts, kā varat ievadīt darbinieku algu sākuma bilances, tostarp ienākumu veida kodus, atvieglojumu/atvilkumus un nodokļus.</span><span class="sxs-lookup"><span data-stu-id="1efdd-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="1efdd-122">Reālā piemērā jums būtu rindas krājums katram ienākumu veida kodam, atvieglojuma ieturējumam, atvieglojumu iemaksai, darbinieka nodoklim un darba devēja nodoklim, kuru ievadītā summa ir līdzšinējā gada summa.</span><span class="sxs-lookup"><span data-stu-id="1efdd-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="1efdd-123">Izmantojot šo kodu un summu sarakstu, izpildiet norādījumus par manuāla ienākumu un algas pārskata izveidošanu ar atspējotu uzskaiti, lai pārceltu sākuma bilances algu nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="1efdd-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="1efdd-124">Uzskaite ir jāatspējo, jo šo sākuma bilances algas pārskatu jūs nevēlaties grāmatot savā virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="1efdd-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="1efdd-125">Tas tika izdarīts mantojuma sistēmā un pārnāk uz jauno sistēmu, kad virsgrāmatā iestatāt sākuma bilances.</span><span class="sxs-lookup"><span data-stu-id="1efdd-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="1efdd-126">A.</span><span class="sxs-lookup"><span data-stu-id="1efdd-126">A.</span></span> <span data-ttu-id="1efdd-127">Kā iestatīt ienākumu veida kodus, ko izmantot algu sākuma bilancēm</span><span class="sxs-lookup"><span data-stu-id="1efdd-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="1efdd-128">Kad ievadāt algu sākuma bilances, pārliecinieties, ka ienākumu veida kodi, kurus jūs izmantosiet, ir konfigurēti ar iespējotu opciju “Atļaut ienākumu pārskata likmju rediģēšanu”.</span><span class="sxs-lookup"><span data-stu-id="1efdd-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="1efdd-129">Tas jums ļauj manuāli pielāgot summu no mantojuma sistēmas.</span><span class="sxs-lookup"><span data-stu-id="1efdd-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="1efdd-130">B.</span><span class="sxs-lookup"><span data-stu-id="1efdd-130">B.</span></span> <span data-ttu-id="1efdd-131">Izveidot ienākumu izrakstu darbiniekam, kam nepieciešama sākuma bilance</span><span class="sxs-lookup"><span data-stu-id="1efdd-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="1efdd-132">Šī darbība manuāli izveido ienākumu izrakstu katram nodarbinātajam par mantojuma sistēmas pēdējo apmaksas periodu, tādējādi izveidojot ienākumu izraksta rindas jaunajā algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="1efdd-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="1efdd-133">Ievadiet vienu rindu katram ienākumu veida kodam, kā arī līdzšinējā gada summu un stundu skaitu.</span><span class="sxs-lookup"><span data-stu-id="1efdd-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="1efdd-134">Piemēra darbības ir šādas:</span><span class="sxs-lookup"><span data-stu-id="1efdd-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="1efdd-135">Atveriet lapu **Visu ienākumu izraksti** un noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1efdd-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="1efdd-136">Ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="1efdd-136">Enter the following:</span></span> 

    | <span data-ttu-id="1efdd-137">Lauks</span><span class="sxs-lookup"><span data-stu-id="1efdd-137">Field</span></span>      | <span data-ttu-id="1efdd-138">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1efdd-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="1efdd-139">Nodarbinātais</span><span class="sxs-lookup"><span data-stu-id="1efdd-139">Worker</span></span>     | <span data-ttu-id="1efdd-140">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="1efdd-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="1efdd-141">Apmaksas cikls</span><span class="sxs-lookup"><span data-stu-id="1efdd-141">Pay cycle</span></span>  | <span data-ttu-id="1efdd-142">sm</span><span class="sxs-lookup"><span data-stu-id="1efdd-142">sm</span></span>                    |
    | <span data-ttu-id="1efdd-143">Apmaksas periods</span><span class="sxs-lookup"><span data-stu-id="1efdd-143">Pay period</span></span> | <span data-ttu-id="1efdd-144">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="1efdd-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="1efdd-145">Cilnē **Ienākumu izraksta rinda** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="1efdd-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="1efdd-146">1. rinda: cilne **Ienākumu izraksta rinda**</span><span class="sxs-lookup"><span data-stu-id="1efdd-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="1efdd-147">Lauks</span><span class="sxs-lookup"><span data-stu-id="1efdd-147">Field</span></span>            | <span data-ttu-id="1efdd-148">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1efdd-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="1efdd-149">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="1efdd-149">Earnings code</span></span>    | <span data-ttu-id="1efdd-150">Regulārā samaksa</span><span class="sxs-lookup"><span data-stu-id="1efdd-150">Regular pay</span></span> |
    | <span data-ttu-id="1efdd-151">Daudzums</span><span class="sxs-lookup"><span data-stu-id="1efdd-151">Quantity</span></span>         | <span data-ttu-id="1efdd-152">1.00</span><span class="sxs-lookup"><span data-stu-id="1efdd-152">1.00</span></span>        |
    | <span data-ttu-id="1efdd-153">Norma</span><span class="sxs-lookup"><span data-stu-id="1efdd-153">Rate</span></span>             | <span data-ttu-id="1efdd-154">30,000</span><span class="sxs-lookup"><span data-stu-id="1efdd-154">30,000</span></span>      |
    | <span data-ttu-id="1efdd-155">Cilne Detalizēta informācija par rindu</span><span class="sxs-lookup"><span data-stu-id="1efdd-155">Line details tab</span></span> |             |
    | <span data-ttu-id="1efdd-156">Manuāli</span><span class="sxs-lookup"><span data-stu-id="1efdd-156">Manual</span></span>           | <span data-ttu-id="1efdd-157">(iezīmēts)</span><span class="sxs-lookup"><span data-stu-id="1efdd-157">(marked)</span></span>    |

    <span data-ttu-id="1efdd-158">2. rinda: cilne **Ienākumu izraksta rinda**</span><span class="sxs-lookup"><span data-stu-id="1efdd-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="1efdd-159">Lauks</span><span class="sxs-lookup"><span data-stu-id="1efdd-159">Field</span></span>            | <span data-ttu-id="1efdd-160">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1efdd-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="1efdd-161">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="1efdd-161">Earnings code</span></span>    | <span data-ttu-id="1efdd-162">Bonuss</span><span class="sxs-lookup"><span data-stu-id="1efdd-162">Bonus</span></span>    |
    | <span data-ttu-id="1efdd-163">Daudzums</span><span class="sxs-lookup"><span data-stu-id="1efdd-163">Quantity</span></span>         | <span data-ttu-id="1efdd-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="1efdd-164">1.0000</span></span>   |
    | <span data-ttu-id="1efdd-165">Norma</span><span class="sxs-lookup"><span data-stu-id="1efdd-165">Rate</span></span>             | <span data-ttu-id="1efdd-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="1efdd-166">4250.00</span></span>  |
    | <span data-ttu-id="1efdd-167">Cilne Detalizēta informācija par rindu</span><span class="sxs-lookup"><span data-stu-id="1efdd-167">Line details tab</span></span> |          |
    | <span data-ttu-id="1efdd-168">Manuālā</span><span class="sxs-lookup"><span data-stu-id="1efdd-168">Manual</span></span>           | <span data-ttu-id="1efdd-169">(iezīmēts)</span><span class="sxs-lookup"><span data-stu-id="1efdd-169">(marked)</span></span> |

    <span data-ttu-id="1efdd-170">3. rinda: cilne **Ienākumu izraksta rinda**</span><span class="sxs-lookup"><span data-stu-id="1efdd-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="1efdd-171">Lauks</span><span class="sxs-lookup"><span data-stu-id="1efdd-171">Field</span></span>           | <span data-ttu-id="1efdd-172">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1efdd-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="1efdd-173">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="1efdd-173">Earnings code</span></span>   | <span data-ttu-id="1efdd-174">Komisija</span><span class="sxs-lookup"><span data-stu-id="1efdd-174">Commission</span></span> |
    | <span data-ttu-id="1efdd-175">Daudzums</span><span class="sxs-lookup"><span data-stu-id="1efdd-175">Quantity</span></span>        | <span data-ttu-id="1efdd-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="1efdd-176">1.0000</span></span>     |
    | <span data-ttu-id="1efdd-177">Norma</span><span class="sxs-lookup"><span data-stu-id="1efdd-177">Rate</span></span>            | <span data-ttu-id="1efdd-178">!,299.00</span><span class="sxs-lookup"><span data-stu-id="1efdd-178">!,299.00</span></span>   |
    | <span data-ttu-id="1efdd-179">Norma</span><span class="sxs-lookup"><span data-stu-id="1efdd-179">Rate</span></span>            | <span data-ttu-id="1efdd-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="1efdd-180">1,299.00</span></span>   |
    | <span data-ttu-id="1efdd-181">Cilne Detalizēta informācija par rindu</span><span class="sxs-lookup"><span data-stu-id="1efdd-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="1efdd-182">Manuālā</span><span class="sxs-lookup"><span data-stu-id="1efdd-182">Manual</span></span>          | <span data-ttu-id="1efdd-183">(iezīmēts)</span><span class="sxs-lookup"><span data-stu-id="1efdd-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="1efdd-184">Slīdņa **Manuāli** iestatīšana uz **Jā** cilnē **Detalizēta informācija par rindu** katrai ienākumu izraksta rindai ir veids, kā likt ievadīt algu sākuma bilances katram nodarbinātajam.</span><span class="sxs-lookup"><span data-stu-id="1efdd-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="1efdd-185">Rūtī **Darbība** noklikšķiniet uz **Izlaist ienākumu izrakstu** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="1efdd-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="1efdd-186">Rūtī **Darbība** noklikšķiniet uz **Algas pārskats**, lai atvērtu lapu **Ģenerēt algas pārskatus**, un iestatiet tālāk norādīto informāciju</span><span class="sxs-lookup"><span data-stu-id="1efdd-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="1efdd-187">Lauks</span><span class="sxs-lookup"><span data-stu-id="1efdd-187">Field</span></span>              | <span data-ttu-id="1efdd-188">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1efdd-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="1efdd-189">Maksājuma datums</span><span class="sxs-lookup"><span data-stu-id="1efdd-189">Payment date</span></span>       | <span data-ttu-id="1efdd-190">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="1efdd-190">6/30/2017</span></span> |
    | <span data-ttu-id="1efdd-191">Maksājuma izdošanas veids</span><span class="sxs-lookup"><span data-stu-id="1efdd-191">Payment run type</span></span>   | <span data-ttu-id="1efdd-192">Manuālā</span><span class="sxs-lookup"><span data-stu-id="1efdd-192">Manual</span></span>    |
    | <span data-ttu-id="1efdd-193">Atspējot uzskaiti</span><span class="sxs-lookup"><span data-stu-id="1efdd-193">Disable accounting</span></span> |   <span data-ttu-id="1efdd-194">Jā</span><span class="sxs-lookup"><span data-stu-id="1efdd-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="1efdd-195">Šī darbība ir pieejama tikai tad, ja maksājuma izpildes tips ir manuāls un ja lietotājs vēlaties atspējot uzskaiti par apmaksas izpildi.</span><span class="sxs-lookup"><span data-stu-id="1efdd-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="1efdd-196">Noklikšķiniet uz **Labi** un aizveriet žurnālu **Informācijas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="1efdd-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="1efdd-197">Kādēļ slīdnis Atspējot uzskaiti ir jāiestata uz Jā, ģenerējot algu pārskatus?</span><span class="sxs-lookup"><span data-stu-id="1efdd-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="1efdd-198">Slīdni iestatot uz **Jā**, algas pārskatā netiek ļauta rindu izplatīšana virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="1efdd-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="1efdd-199">Virsgrāmatas summas tika atjauninātas iepriekš, kad tika ievadītas konta bilances no mantojuma sistēmas.</span><span class="sxs-lookup"><span data-stu-id="1efdd-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="1efdd-200">Ievadot algu sākuma bilances, varat ģenerēt pārskatus, kuros ietverta informācija no iepriekšējiem gadiem, kā arī identificēt ierobežojumus atvieglojumu un nodokļu nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="1efdd-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="1efdd-201">C.</span><span class="sxs-lookup"><span data-stu-id="1efdd-201">C.</span></span> <span data-ttu-id="1efdd-202">Izveidot algas pārskatus darbiniekiem</span><span class="sxs-lookup"><span data-stu-id="1efdd-202">Create pay statements for employees</span></span>

<span data-ttu-id="1efdd-203">Kad ir izveidoti algas pārskati, kuriem ir sākuma bilances, ir jāpārbauda, vai šie algas pārskati precīzi atspoguļo algu datus.</span><span class="sxs-lookup"><span data-stu-id="1efdd-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="1efdd-204">Tāpat jums ir manuāli jāatjaunina atvieglojumu un nodokļu informācija, lai tā atbilstu vērtībām iepriekšējā algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="1efdd-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="1efdd-205">Kad esat pārbaudījis, vai summas no iepriekšējās algu sistēmas atbilst summām pašreizējos algas pārskatos, šie algas pārskati ir jāfinalizē.</span><span class="sxs-lookup"><span data-stu-id="1efdd-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="1efdd-206">Atveriet lapu **Visi algas pārskati**.</span><span class="sxs-lookup"><span data-stu-id="1efdd-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="1efdd-207">Iezīmējiet pēdējo ģenerēto algas pārskatu darbiniekam Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="1efdd-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="1efdd-208">Noklikšķiniet uz **Rediģēt**, lai atvērtu lapu **Algas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="1efdd-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="1efdd-209">Atveriet cilni **Atvieglojumu ieturējumi** un ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="1efdd-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="1efdd-210">Lauks</span><span class="sxs-lookup"><span data-stu-id="1efdd-210">Field</span></span>             | <span data-ttu-id="1efdd-211">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1efdd-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="1efdd-212">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="1efdd-212">Benefit</span></span>           | <span data-ttu-id="1efdd-213">Ieturējuma summa</span><span class="sxs-lookup"><span data-stu-id="1efdd-213">Deduction amount</span></span> |
    | <span data-ttu-id="1efdd-214">401K</span><span class="sxs-lookup"><span data-stu-id="1efdd-214">401K</span></span>              | <span data-ttu-id="1efdd-215">Piedalīties</span><span class="sxs-lookup"><span data-stu-id="1efdd-215">Participate</span></span>      |
    | <span data-ttu-id="1efdd-216">Zobārstniecība</span><span class="sxs-lookup"><span data-stu-id="1efdd-216">Dental</span></span>            | <span data-ttu-id="1efdd-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="1efdd-217">SubSp</span></span>            |
    | <span data-ttu-id="1efdd-218">Apg. aprūpes izdevumi</span><span class="sxs-lookup"><span data-stu-id="1efdd-218">Dep care spending</span></span> | <span data-ttu-id="1efdd-219">Piedalīties</span><span class="sxs-lookup"><span data-stu-id="1efdd-219">Participate</span></span>      |
    | <span data-ttu-id="1efdd-220">Redze</span><span class="sxs-lookup"><span data-stu-id="1efdd-220">Vision</span></span>            | <span data-ttu-id="1efdd-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="1efdd-221">SupSp</span></span>            |

5. <span data-ttu-id="1efdd-222">Cilnē **Atvieglojumu iemaksas** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="1efdd-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="1efdd-223">Lauks</span><span class="sxs-lookup"><span data-stu-id="1efdd-223">Field</span></span>   | <span data-ttu-id="1efdd-224">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1efdd-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="1efdd-225">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="1efdd-225">Benefit</span></span> | <span data-ttu-id="1efdd-226">Seguma summa</span><span class="sxs-lookup"><span data-stu-id="1efdd-226">Contribution amount</span></span> |
    | <span data-ttu-id="1efdd-227">401K</span><span class="sxs-lookup"><span data-stu-id="1efdd-227">401K</span></span>    | <span data-ttu-id="1efdd-228">Piedalīties</span><span class="sxs-lookup"><span data-stu-id="1efdd-228">Participate</span></span>         |
    | <span data-ttu-id="1efdd-229">Zobārstniecība</span><span class="sxs-lookup"><span data-stu-id="1efdd-229">Dental</span></span>  | <span data-ttu-id="1efdd-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="1efdd-230">SubSp</span></span>               |
    | <span data-ttu-id="1efdd-231">Redze</span><span class="sxs-lookup"><span data-stu-id="1efdd-231">Vision</span></span>  | <span data-ttu-id="1efdd-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="1efdd-232">SubSp</span></span>               |

6. <span data-ttu-id="1efdd-233">Cilnē **Nodokļu ieturējumi** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="1efdd-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="1efdd-234">Lauks</span><span class="sxs-lookup"><span data-stu-id="1efdd-234">Field</span></span>           | <span data-ttu-id="1efdd-235">Vērtība</span><span class="sxs-lookup"><span data-stu-id="1efdd-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="1efdd-236">Nodokļa kods</span><span class="sxs-lookup"><span data-stu-id="1efdd-236">Tax code</span></span>        | <span data-ttu-id="1efdd-237">Ieturējuma summa</span><span class="sxs-lookup"><span data-stu-id="1efdd-237">Deduction amount</span></span> |
    | <span data-ttu-id="1efdd-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="1efdd-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="1efdd-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="1efdd-239">1600.00</span></span>          |
    | <span data-ttu-id="1efdd-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="1efdd-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="1efdd-241">825.75</span><span class="sxs-lookup"><span data-stu-id="1efdd-241">825.75</span></span>           |

7. <span data-ttu-id="1efdd-242">Cilnē **Nodokļu iemaksas** ievadiet tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="1efdd-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="1efdd-243">Noklikšķiniet uz **Aprēķināt**.</span><span class="sxs-lookup"><span data-stu-id="1efdd-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="1efdd-244">Pārliecinieties, ka algas pārskata kopsummas atbilst mantojuma sistēmas šī nodarbinātā līdzšinējā gada kopsummām.</span><span class="sxs-lookup"><span data-stu-id="1efdd-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="1efdd-245">Iespējams, finalizēšana ir jāatliek uz nākamo darbību, lai veiktu visu algas pārskatu vispārēju validēšanu kopumā.</span><span class="sxs-lookup"><span data-stu-id="1efdd-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="1efdd-246">Pēc validēšanas izejiet cauri visiem algas pārskatiem un finalizējiet tos.</span><span class="sxs-lookup"><span data-stu-id="1efdd-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="1efdd-247">Šo pašu procedūru var veikt ar ceturkšņa intervāliem, ja nepieciešams, visiem iepriekšējiem ceturkšņiem katru gadu.</span><span class="sxs-lookup"><span data-stu-id="1efdd-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="1efdd-248">Tas ir jādara tikai tad, ja klientam ir nepieciešams datus redzēt pa ceturksnim, neatgriežoties mantojuma sistēmā.</span><span class="sxs-lookup"><span data-stu-id="1efdd-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="1efdd-249">Ja pieļaujat kļūdu, ievadot darbinieka sākuma bilances</span><span class="sxs-lookup"><span data-stu-id="1efdd-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="1efdd-250">Transakcijas ir iespējams atsaukt un ievadīt no jauna.</span><span class="sxs-lookup"><span data-stu-id="1efdd-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="1efdd-251">Lai transakciju atsauktu, jums ir tikai jāizpilda tālāk norādītās darbības lapā **Visi algas pārskati**.</span><span class="sxs-lookup"><span data-stu-id="1efdd-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="1efdd-252">Noklikšķiniet uz **Atsaukt**.</span><span class="sxs-lookup"><span data-stu-id="1efdd-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="1efdd-253">Noklikšķiniet uz **Jā**, kad tiek parādīts ziņojums “Kad anulējat šo algas pārskatu, tiek izveidots anulēšanas algas pārskats, lai kompensētu šo algas pārskatu.</span><span class="sxs-lookup"><span data-stu-id="1efdd-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="1efdd-254">Nevienu no algas pārskatiem nevar rediģēt.</span><span class="sxs-lookup"><span data-stu-id="1efdd-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="1efdd-255">Vai vēlaties anulēt šo samaksas</span><span class="sxs-lookup"><span data-stu-id="1efdd-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="1efdd-256">pārskatu?”</span><span class="sxs-lookup"><span data-stu-id="1efdd-256">displays.</span></span> 

<span data-ttu-id="1efdd-257">Pēc algas pārskata anulēšanas varat ģenerēt jaunu nodarbinātā algas pārskatu no iepriekš izveidotā ienākumu izraksta.</span><span class="sxs-lookup"><span data-stu-id="1efdd-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="1efdd-258">Pirms ģenerējat jauno algas pārskatu, noteikti labojiet visas nepareizās ienākumu izraksta rindas, un pēc tam ģenerējiet jauno algas pārskatu ar pareizajām summām.</span><span class="sxs-lookup"><span data-stu-id="1efdd-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]