---
title: Mazumtirdzniecības pārskati
description: Šajā tēmā ir aprakstīts pārskatu izveides un grāmatošanas process.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 4409811d2ef60174a316db10307dc7af4697398c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023315"
---
# <a name="retail-statements"></a><span data-ttu-id="072b1-103">Mazumtirdzniecības pārskati</span><span class="sxs-lookup"><span data-stu-id="072b1-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="072b1-104">Programmā Dynamics 365 Commerce pārskatu grāmatošanas process tiek izmantots, lai uzskaitītu transakcijas, kas tiek veiktas programmā Cloud Point of Sale (POS) vai Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="072b1-104">In Dynamics 365 Commerce, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="072b1-105">Pārskatu grāmatošanas process izmanto sadales grafiku, lai POS transakciju kopu ievilktu Headquarters (HQ) klientā.</span><span class="sxs-lookup"><span data-stu-id="072b1-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="072b1-106">Parametrus, kas ir definēti lapās **Commerce parametri** un **Veikali**, izmanto, lai atlasītu atsevišķos pārskatos ievilktās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="072b1-106">The parameters that are defined on the **Commerce parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="072b1-107">Tālāk esošajā attēlā parādīts pārskatu grāmatošanas process.</span><span class="sxs-lookup"><span data-stu-id="072b1-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="072b1-108">Šajā procesā POS reģistrētās transakcijas tiek pārsūtītas uz klientu, izmantojot Commerce plānotāju.</span><span class="sxs-lookup"><span data-stu-id="072b1-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Commerce scheduler.</span></span> <span data-ttu-id="072b1-109">Kad klients ir saņēmis transakcijas, varat izveidot, aprēķināt un grāmatot veikala transakciju pārskatu.</span><span class="sxs-lookup"><span data-stu-id="072b1-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="072b1-110">[![Pārskatu grāmatošanas process](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="072b1-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="072b1-111">Pārskatu izveide un grāmatošana</span><span class="sxs-lookup"><span data-stu-id="072b1-111">Creating and posting statements</span></span>

<span data-ttu-id="072b1-112">Pārskatu var izveidot manuāli, vai arī varat izmantot pakešveida apstrādi, kas iestatīta periodiskai palaišanai visas dienas garumā.</span><span class="sxs-lookup"><span data-stu-id="072b1-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="072b1-113">Abos gadījumos pārskatu izveidei un grāmatošanai tiek izmantotas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="072b1-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="072b1-114">Pārskata izveide</span><span class="sxs-lookup"><span data-stu-id="072b1-114">Create the statement</span></span>

<span data-ttu-id="072b1-115">Šī darbība identificē veikalu, kuram manuāli tiek veidots pārskats.</span><span class="sxs-lookup"><span data-stu-id="072b1-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="072b1-116">Konfigurējot pakešveida apstrādi, varat automātiski izveidot pārskatus par visiem veikaliem, pamatojoties uz jūsu definēto grafiku.</span><span class="sxs-lookup"><span data-stu-id="072b1-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="072b1-117">Pārskata aprēķini</span><span class="sxs-lookup"><span data-stu-id="072b1-117">Calculate the statement</span></span>

<span data-ttu-id="072b1-118">Veicot šo darbību, tiek atlasītas transakcijas rindas, pamatojoties uz kritērijiem, kas katram veikalam definēti lapās **Commerce parametri** un **Veikali**.</span><span class="sxs-lookup"><span data-stu-id="072b1-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Commerce parameters** and **Stores** pages.</span></span> <span data-ttu-id="072b1-119">Šajās lapās jūs definējat kritērijus un norādāt, kā tiek veikti transakciju aprēķini.</span><span class="sxs-lookup"><span data-stu-id="072b1-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="072b1-120">Lai pirms pārskata aprēķinu veikšanas skatītu pārskatā iekļauto transakciju sarakstu, izmantojiet lapu **Transakcijas**.</span><span class="sxs-lookup"><span data-stu-id="072b1-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="072b1-121">Pārskata aprēķinos kā aprēķinātā summa tiek izmantotas norēķinu uzskaites no reģistriem.</span><span class="sxs-lookup"><span data-stu-id="072b1-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="072b1-122">Saskaitīto summu var ievadīt arī manuāli.</span><span class="sxs-lookup"><span data-stu-id="072b1-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="072b1-123">Pārskatā visām maksāšanas metodēm tiek parādītas transakciju pārdošanas summas un faktiskās saskaitītās summas starpība.</span><span class="sxs-lookup"><span data-stu-id="072b1-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="072b1-124">Pārskats tiek grāmatots tikai tad, ja šī starpība ir mazāka par veikalam definēto maksimālo grāmatošanas starpību.</span><span class="sxs-lookup"><span data-stu-id="072b1-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="072b1-125">Pārskata aprēķinu procesā tiek izmantota globālo numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="072b1-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="072b1-126">Veicot pārskata aprēķinus, aprēķinos tiek ietverti tālāk norādītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="072b1-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="072b1-127">Atlasītajam datumu intervālam atzīmējiet transakcijas, kas netika iekļautas iepriekšējā pārskata aprēķinos.</span><span class="sxs-lookup"><span data-stu-id="072b1-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="072b1-128">Aprēķiniet kopsummas, kuru norēķini tika iekļauti atlasītajās transakcijās.</span><span class="sxs-lookup"><span data-stu-id="072b1-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="072b1-129">Atkarībā no pārskata metodes rezultāti tiek rādīti pārskata rindās.</span><span class="sxs-lookup"><span data-stu-id="072b1-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="072b1-130">Ja pārskata metode ir **Kopsumma**, katrai atlasītajās transakcijās ietvertajai maksāšanas metodei tiek izveidota rinda.</span><span class="sxs-lookup"><span data-stu-id="072b1-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="072b1-131">Ja pārskata metode ir **Personāls**, rinda tiek izveidota katrai maksāšanas metodei, kas ietverta atlasītā darbinieka veiktajās transakcijās.</span><span class="sxs-lookup"><span data-stu-id="072b1-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="072b1-132">Ja pārskata metode ir **POS terminālis**, rinda tiek izveidota katrai maksāšanas metodei, kas ietverta atlasītajā reģistrā veiktajās transakcijās.</span><span class="sxs-lookup"><span data-stu-id="072b1-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="072b1-133">Ja pārskata metode ir **Maiņa**, rinda tiek izveidota katrai maksāšanas metodei, kas ietverta maiņas laikā veiktajās transakcijās.</span><span class="sxs-lookup"><span data-stu-id="072b1-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="072b1-134">Ja lapā **Veikali** ir atzīmēta izvēles rūtiņa **Sadalīt pēc pārskata metodes**, tiek izveidots atsevišķs pārskats atbilstoši laukā **Pārskata metode** atlasītajai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="072b1-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="072b1-135">Ja veikala darba laiks sniedzas pāri pusnaktij, varat konfigurēt pārskatu grāmatošanu tā, lai tās pamatā būtu darba dienas beigas, nevis kalendārās dienas beigas.</span><span class="sxs-lookup"><span data-stu-id="072b1-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="072b1-136">Lapas **Veikali** kopsavilkuma cilnes FastTab **Izraksts/slēgšana** laukā **Darba dienas beigas** ievadiet laiku, līdz kuram ir jāreģistrē pēdējā transakcija, lai tā tiktu iekļauta darba dienas izrakstā.</span><span class="sxs-lookup"><span data-stu-id="072b1-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="072b1-137">Atzīmējiet izvēles rūtiņu **Grāmatot kā darba dienu**, lai grāmatotu transakcijas tajā pašā darba dienā.</span><span class="sxs-lookup"><span data-stu-id="072b1-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="072b1-138">Kad tiek grāmatots pārskats, transakcijas, kas reģistrētas vienas darba dienas laikā, var iekļaut tajā pašā pārdošanas pasūtījumā, pat ja dažas transakcijas ir veiktas pirms pusnakts, bet citas transakcijas — pēc pusnakts.</span><span class="sxs-lookup"><span data-stu-id="072b1-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="072b1-139">Piemērs: tādas darba dienas pārskata grāmatošana, kas ietver divas kalendārās dienas</span><span class="sxs-lookup"><span data-stu-id="072b1-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="072b1-140">Veikals ir atvērts laika posmā no plkst. 8.00 līdz 3.00, un veikala konfigurācijā ir atzīmēta izvēles rūtiņa **Grāmatot kā darba dienu**.</span><span class="sxs-lookup"><span data-stu-id="072b1-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="072b1-141">31. maijā tiek reģistrētas veikala transakcijas, kas veiktas laika posmā starp plkst. 8.00 un pusnakti.</span><span class="sxs-lookup"><span data-stu-id="072b1-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="072b1-142">Tiek reģistrētas arī veikala transakcijas, kas veiktas laika posmā starp plkst. 00.01 un 3.00 1. jūnijā.</span><span class="sxs-lookup"><span data-stu-id="072b1-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="072b1-143">Kad, noslēdzot darba dienu, tiek grāmatoti veikala pārskati, tiek ģenerēts pārdošanas pasūtījums, kas ietver visas darba laikā (8.00–3.00) reģistrētās transakcijas, pat ja šīs transakcijas ir veiktas divu dienu laikā: 31. maijā un 1. jūnijā.</span><span class="sxs-lookup"><span data-stu-id="072b1-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="072b1-144">Ja šim veikalam ir noņemta atzīme no izvēles rūtiņas **Grāmatot kā darba dienu**, darba dienas beigās grāmatojot veikala pārskatu, tiek ģenerēti atsevišķi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="072b1-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="072b1-145">Viens pārdošanas pasūtījums ietver transakcijas, kas reģistrētas 31. maijā darba laikā no plkst. 8.00 līdz pusnaktij, savukārt otrs pārdošanas pasūtījumu ietver transakcijas, kas reģistrētas 1. jūnijā laika posmā starp plkst. 00.01 un 3.00.</span><span class="sxs-lookup"><span data-stu-id="072b1-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="072b1-146">Lai varētu izveidot pārskatus, pārskata periodā ir jānoslēdz maiņas.</span><span class="sxs-lookup"><span data-stu-id="072b1-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="072b1-147">Pārskata grāmatošana</span><span class="sxs-lookup"><span data-stu-id="072b1-147">Post the statement</span></span>

<span data-ttu-id="072b1-148">Kad grāmatojat pārskatu, pārskatā tiek izveidoti pārdošanas pasūtījumi un rēķini.</span><span class="sxs-lookup"><span data-stu-id="072b1-148">When you post a statement, sales orders and invoices are created for the sales in the statement.</span></span>

- <span data-ttu-id="072b1-149">Pārdošanas transakcijas, kas veiktas skaidrā naudā un bez piegādes, tiek apkopotas vienā pārdošanas pasūtījumā, un to rēķins tiek izrakstīts veikalam piešķirtajam noklusējuma debitoram.</span><span class="sxs-lookup"><span data-stu-id="072b1-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="072b1-150">Transakcijām, kurām programmā ir pievienots debitors, POS sistēmā tiek ģenerēti atsevišķi pārdošanas pasūtījumi un rēķini — pa vienam katram unikālajam debitoram.</span><span class="sxs-lookup"><span data-stu-id="072b1-150">Sales for which a customer was added to the transaction in POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="072b1-151">Pārskatā iekļautajiem maksājumiem automātiski tiek izveidoti maksājumu žurnāli, un POS veikalā tiek atjaunināti krājumi.</span><span class="sxs-lookup"><span data-stu-id="072b1-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>