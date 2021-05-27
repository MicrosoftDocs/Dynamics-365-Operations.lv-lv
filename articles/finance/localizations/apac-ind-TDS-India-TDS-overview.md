---
title: Indijas No kopējo ienākumu summas atskaitītā nodokļa (TDS) pārskats
description: Šajā tēmā sniegta detalizēta informācija par Indijas No kopējo ienākumu summas atskaitīto nodokli (TDS). TDS dokumentācija sedz šīs iespējas funkcionalitāti.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023431"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="06089-104">Indijas No kopējo ienākumu summas atskaitītā nodokļa (TDS) pārskats</span><span class="sxs-lookup"><span data-stu-id="06089-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06089-105">Šajā tēmā sniegta detalizēta informācija par Indijas No kopējo ienākumu summas atskaitīto nodokli (TDS).</span><span class="sxs-lookup"><span data-stu-id="06089-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="06089-106">TDS dokumentācija sedz šīs iespējas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="06089-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="06089-107">Tajā skaidrots arī, kā veikt pamata iestatījumus TDS, aprēķināt TDS darījumos, pabeigt TDS norēķinu procesu, reģistrēt TDS sertifikātu numurus un ģenerēt TDS pieprasījumus, TDS pārskatus un TDS sertifikātus.</span><span class="sxs-lookup"><span data-stu-id="06089-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="06089-108">Šajā dokumentācijā ir iekļautas šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="06089-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="06089-109">TDS pamata iestatījumi</span><span class="sxs-lookup"><span data-stu-id="06089-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="06089-110">TDS aprēķinam izmantotā formulas veidotāja un sliekšņa ierobežojuma funkcionalitāte</span><span class="sxs-lookup"><span data-stu-id="06089-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="06089-111">TDS aprēķināšana rēķinos, maksājumos, parādzīmēs un starpuzņēmumu darījumos</span><span class="sxs-lookup"><span data-stu-id="06089-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="06089-112">Periodisks TDS norēķinu process un TDS summu nosegšana TDS iestādes kreditoriem</span><span class="sxs-lookup"><span data-stu-id="06089-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="06089-113">TDS sertifikātu numuru un datumu ierakstīšana un atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="06089-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="06089-114">Ievads TDS</span><span class="sxs-lookup"><span data-stu-id="06089-114">Introduction to TDS</span></span>

<span data-ttu-id="06089-115">Saskaņā ar 1961. gada ienākumu nodokļa aktu ieturēto nodokli atskaita pakalpojumu saņēmējs avansa maksājuma vai kredīta uzskaites laikā atkarībā no tā, kas notiek vispirms.</span><span class="sxs-lookup"><span data-stu-id="06089-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="06089-116">Personai, kas veic maksājumu, jāatskaita nodokļa summa, un pakalpojuma sniedzējam jāsamaksā tikai neto bilance.</span><span class="sxs-lookup"><span data-stu-id="06089-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="06089-117">TDS tiek lietots pakalpojumiem, kurus norāda valdība, un nodoklis tiek atskaitīts, izmantojot likmes, ko valdība norāda periodam.</span><span class="sxs-lookup"><span data-stu-id="06089-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="06089-118">Ieturējumu likme ir balstīta uz entītijas statusu, kas saņem maksājumu vai nodrošina pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="06089-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="06089-119">Statusi ietver **Individuālu**, **Nedalītu ģimeni** (**HUF**), **Uzņēmumu**, **Firmu**, **Personu asociāciju** (**AOP**), **Personu grupu** (**BOI**) un **Vietējo pašvaldību**.</span><span class="sxs-lookup"><span data-stu-id="06089-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="06089-120">Šajās sadaļās norādīti pakalpojumi, kam tiek pielietots TDS, kā to ir norādījusi Indijas valdība.</span><span class="sxs-lookup"><span data-stu-id="06089-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="06089-121">**Iedzīvotāji**</span><span class="sxs-lookup"><span data-stu-id="06089-121">**Residents**</span></span>

- <span data-ttu-id="06089-122">Ienākumi no algām (saskaņā ar 192. sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="06089-123">Ienākumi no vērtspapīru procentiem (atbilstoši 193. sadaļai)</span><span class="sxs-lookup"><span data-stu-id="06089-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="06089-124">Ienākumi no dividendēm (saskaņā ar 194. sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="06089-125">Ienākumi no procentiem (saskaņā ar 194.A sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="06089-126">Ienākumi no loteriju vai mīklām (saskaņā ar 194.B sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="06089-127">Uzvara no zirgu skriešanas sacensībām (saskaņā ar 194.BB sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="06089-128">Darbuzņēmēji un apakšuzņēmumi (saskaņā ar 194.C sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="06089-129">Apdrošināšanas komisija (saskaņā ar 194.D sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="06089-130">Ienākumi no noguldījumiem saskaņā ar valsts taupības shēmu (saskaņā ar 194.EE sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="06089-131">Ienākumi no kopfonda vai UTI (saskaņā ar 194.F sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="06089-132">Komisija, atlīdzība, balva utt., par pārdošanu vai loteriju (saskaņā ar 194.G sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="06089-133">Komisijas vai starpnieka maksājums (saskaņā ar 194.H sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="06089-134">Noma (saskaņā ar 194.I sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="06089-135">Profesionālais pakalpojums (saskaņā ar 194.J sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="06089-136">Ienākumi no vienībām (saskaņā ar 194.K sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="06089-137">Kompensācijas izmaksa par noteikta nekustamā īpašuma iegādi (saskaņā ar 194.LA sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="06089-138">**Nerezidenti**</span><span class="sxs-lookup"><span data-stu-id="06089-138">**Non-residents**</span></span>

- <span data-ttu-id="06089-139">Maksājumi nerezidentu sporta veidiem vai sporta asociācijām (saskaņā ar 194.E sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="06089-140">Citas summas (saskaņā ar 195. sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="06089-141">Ienākumi attiecībā uz nerezidentu vienībām (saskaņā ar 196.A sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="06089-142">Ienākumi no ārvalstu valūtas parādzīmēm vai Indijas uzņēmuma daļām (saskaņā ar 196.C sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="06089-143">Ārvalstu investoru ienākumi no vērtspapīriem (saskaņā ar 196.D sadaļu)</span><span class="sxs-lookup"><span data-stu-id="06089-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="06089-144">Alga un visi citi pozitīvie ienākumi, kas nav saistīti ar ienākumiem (192. sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="06089-145">Vērtspapīru procenti (193. sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="06089-146">Procenti, kas nav procenti no vērtspapīriem (194.A sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="06089-147">Maksājumi līgumslēdzējiem un apakšuzņēmumi (194.C sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="06089-148">Laimesti no loterijas vai krustvārdu mīklām (194.B sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="06089-149">Uzvaras no zirgu skriešanas sacensībām (194.BB sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="06089-150">Apdrošināšanas komisija, kas sedz visus maksājumus par apdrošināšanas uzņēmumu (194.D sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="06089-151">Visi procenti, izņemot procentus par vērtspapīriem, kas tiek maksāti nerezidentiem, kas nav uzņēmums vai ārvalstu uzņēmums (195. sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="06089-152">Maksājums nerezidentam sportistiem, tostarp sporta asociācijai vai institūcijai.</span><span class="sxs-lookup"><span data-stu-id="06089-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="06089-153">Nerezidenta sportista gadījumā maksājumi par reklāmām, kā arī raksti par jebkuru spēli/sportu Indijā laikrakstos, žurnālos utt.</span><span class="sxs-lookup"><span data-stu-id="06089-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="06089-154">ir iekļauti (194.E sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="06089-155">Maksājums attiecībā uz depozītiem saskaņā ar NSS \[Valsts uzkrājumu shēmu\] (194.EE sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="06089-156">Maksājums saskaņā ar savstarpējo fondu vai UTI veikto vienību atpirkšanu (194.F sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="06089-157">Komisijas vai starpnieka maksājums (194.H sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="06089-158">Īres maksājums (194.I sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="06089-159">Maksa par profesionāliem vai tehniskiem pakalpojumiem (194.J sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="06089-160">Komisija tirdzniecības uzņēmumiem, izplatītājiem, pircējiem un loterijas biļešu pārdevējiem, ieskaitot atlīdzību vai laimestu par šādām biļetēm (194.G sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="06089-161">Ieņēmumi no ārvalstu valūtā iegādātajām vienībām vai ilgtermiņa kapitāla ieguvumiem, ko rada tādu vienību nodošana, kas iegādātas ārzemju valūtā (196.B sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="06089-162">Visu ienākumu izmaksāšana nerezidentiem attiecībā uz procentiem vai dividendēm par obligācijām un akcijām (196.C sadaļa)</span><span class="sxs-lookup"><span data-stu-id="06089-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="06089-163">TDS tiek aprēķināts pirkšanas, pārdošanas, pārdošanas ieņēmumiem, kredīta notām, pamatlīdzekļu iegādei, priekšapmaksai, avansa maksājumiem, parādzīmēm, būvdarbu nodokļiem un starpuzņēmumu darījumiem.</span><span class="sxs-lookup"><span data-stu-id="06089-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="06089-164">Pašreizējā Indijas nodokļa scenārijā TDS netiek aprēķināts pārdošanas darījumiem.</span><span class="sxs-lookup"><span data-stu-id="06089-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="06089-165">Tomēr sistēma ietver uzkrājumu, lai aprēķinātu TDS, kas atgūstami pārdošanas darījumos, jo īpaši starpuzņēmumu darījumos.</span><span class="sxs-lookup"><span data-stu-id="06089-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="06089-166">TDS aprēķinā vienmēr ņem vērā TDS komponentam noteikto slieksni un izņēmuma slieksni.</span><span class="sxs-lookup"><span data-stu-id="06089-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="06089-167">Periodisko TDS norēķinu process ir jāpalaiž, un TDS maksājumi ir jānokārto TDS iestādes kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="06089-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="06089-168">No piegādātājiem vai debitoriem saņemto TDS sertifikātu numurus un datumus var reģistrēt un atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="06089-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="06089-169">Turklāt veidlapu 26Q un 27Q ceturkšņa pārskatos var ģenerēt veidlapas 16A sertifikātu TDS, kas var tikt ģenerēts sadaļā Finanses.</span><span class="sxs-lookup"><span data-stu-id="06089-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="06089-170">TDS iestatīšana un darbs ar to</span><span class="sxs-lookup"><span data-stu-id="06089-170">Setting up and working with TDS</span></span>

<span data-ttu-id="06089-171">Šeit sniegts pārskats par TDS iestatīšanu un darbu ar to.</span><span class="sxs-lookup"><span data-stu-id="06089-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="06089-172">**TDS iestatīšana:**</span><span class="sxs-lookup"><span data-stu-id="06089-172">**TDS setup:**</span></span>

    - <span data-ttu-id="06089-173">Parametru iestatīšana:</span><span class="sxs-lookup"><span data-stu-id="06089-173">Parameter setup:</span></span>

        - <span data-ttu-id="06089-174">Virsgrāmatas parametros aktivizējiet ar TDS saistītos parametrus.</span><span class="sxs-lookup"><span data-stu-id="06089-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="06089-175">Virsgrāmatas parametros iestatiet numuru sēriju ieturētā nodokļa maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="06089-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="06089-176">Iestatiet parametrus sadaļās Kreditori un Debitori.</span><span class="sxs-lookup"><span data-stu-id="06089-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="06089-177">Pamata iestatīšana:</span><span class="sxs-lookup"><span data-stu-id="06089-177">Basic setup:</span></span>

        - <span data-ttu-id="06089-178">Iestatiet TDS reģistrācijas numurus uzņēmumam, debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="06089-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="06089-179">TDS komponentu grupu iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="06089-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="06089-180">Iestatiet TDS komponentus, pievienojiet tiem TDS sastāvdaļu grupas un nosakiet to slieksni un izņēmuma slieksni.</span><span class="sxs-lookup"><span data-stu-id="06089-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="06089-181">Iestatiet TDS iestādes.</span><span class="sxs-lookup"><span data-stu-id="06089-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="06089-182">Iestatīt TDS norēķinu periodus.</span><span class="sxs-lookup"><span data-stu-id="06089-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="06089-183">Iestatiet TDS nodokļu kodus un pievienojiet tiem TDS komponentus.</span><span class="sxs-lookup"><span data-stu-id="06089-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="06089-184">Iestatiet TDS nodokļu grupas un pievienojiet tiem TDS nodokļu kodus.</span><span class="sxs-lookup"><span data-stu-id="06089-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="06089-185">Formulas veidotājā definējiet aprēķināmo TDS nodokļa grupai.</span><span class="sxs-lookup"><span data-stu-id="06089-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="06089-186">Ierakstīt TDS koncesijas sertifikātu numurus.</span><span class="sxs-lookup"><span data-stu-id="06089-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="06089-187">Virsgrāmatas konti un uzņēmuma iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="06089-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="06089-188">Iestatiet TDS kreditoru un debitoru virsgrāmatas kontus.</span><span class="sxs-lookup"><span data-stu-id="06089-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="06089-189">Iestatiet uzņēmumam nodokļu atskaitīšanas un iekasēšanas konta numuru (TAN) un atskaitītāja veida kategoriju.</span><span class="sxs-lookup"><span data-stu-id="06089-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="06089-190">Citi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="06089-190">Other setup:</span></span>

        - <span data-ttu-id="06089-191">Iestatiet maksājumu grafiku, kas ietver TDS sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="06089-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="06089-192">Iestatiet maksājumu nodevas tipu maksājumiem TDS iestādei.</span><span class="sxs-lookup"><span data-stu-id="06089-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="06089-193">Iestatiet informāciju par TDS grupām, pastāvīgajiem kontu numuriem (PAN) un kreditoru un debitoru TAN.</span><span class="sxs-lookup"><span data-stu-id="06089-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="06089-194">**TDS aprēķina darījumos:**</span><span class="sxs-lookup"><span data-stu-id="06089-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="06089-195">Rēķini un maksājumi</span><span class="sxs-lookup"><span data-stu-id="06089-195">Invoices and payments</span></span>
    - <span data-ttu-id="06089-196">Parādzīmes</span><span class="sxs-lookup"><span data-stu-id="06089-196">Promissory notes</span></span>
    - <span data-ttu-id="06089-197">Avansa maksājumi</span><span class="sxs-lookup"><span data-stu-id="06089-197">Advance payments</span></span>
    - <span data-ttu-id="06089-198">Priekšapmaksas</span><span class="sxs-lookup"><span data-stu-id="06089-198">Prepayments</span></span>

3. <span data-ttu-id="06089-199">**TDS norēķini:**</span><span class="sxs-lookup"><span data-stu-id="06089-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="06089-200">Periodisko TDS norēķinu process</span><span class="sxs-lookup"><span data-stu-id="06089-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="06089-201">TDS maksājumu norēķini TDS iestādes kreditoriem un TDS challan izveide</span><span class="sxs-lookup"><span data-stu-id="06089-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="06089-202">**TDS uzziņas, pārskati un sertifikāts:**</span><span class="sxs-lookup"><span data-stu-id="06089-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="06089-203">Ierakstīt un atjaunināt TDS sertifikātu numurus un datumus.</span><span class="sxs-lookup"><span data-stu-id="06089-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="06089-204">Ģenerēt TDS pieprasījumu un grāmatoto TDS pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="06089-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="06089-205">Ģenerēt formu 27A, formu 26Q, formu 27Q TDS un e-TDS ceturkšņa pārskatus.</span><span class="sxs-lookup"><span data-stu-id="06089-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="06089-206">Ģenerēt formu 16A TDS sertifikātu.</span><span class="sxs-lookup"><span data-stu-id="06089-206">Generate a Form 16A TDS certificate.</span></span>
