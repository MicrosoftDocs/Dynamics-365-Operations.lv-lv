---
title: Nomas grāmatu iestatīšana
description: Šī tēma apraksta informāciju, kas tiek uzturēta nomas grāmatās. Nomas grāmatās ir iekļautas uzskaites politikas, kas nosaka, kā sistēmā tiek uzskaitīta noma.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 948860bb064dde1085fef4a74da2d9a600892294
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131009"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="94df0-104">Nomas grāmatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="94df0-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94df0-105">Nomas grāmatās ir iekļautas uzskaites politikas, kas nosaka, kā sistēmā tiek uzskaitīta noma.</span><span class="sxs-lookup"><span data-stu-id="94df0-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="94df0-106">Papildus skaidras naudas pamata uzskaitei līdzekļu noma atbalsta tālāk norādītos standartus.</span><span class="sxs-lookup"><span data-stu-id="94df0-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="94df0-107">Vispārpieņemtie uzskaites principi Amerikas Savienotajās valstīs (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="94df0-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="94df0-108">Uzskaites standartu kodifikācijas tēma 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="94df0-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="94df0-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="94df0-109">ASC 840</span></span>
- <span data-ttu-id="94df0-110">Starptautisko finanšu pārskatu standarts 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="94df0-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="94df0-111">Starptautiskais uzskaites standarts 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="94df0-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="94df0-112">Lai izveidotu nomas grāmatu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="94df0-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="94df0-113">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="94df0-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="94df0-114">Lai pievienotu grāmatu, atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="94df0-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="94df0-115">Iestatiet tālāk minētos laukus.</span><span class="sxs-lookup"><span data-stu-id="94df0-115">Set the following fields.</span></span>

    | <span data-ttu-id="94df0-116">Vārds, uzvārds</span><span class="sxs-lookup"><span data-stu-id="94df0-116">Name</span></span>                                     | <span data-ttu-id="94df0-117">Apraksts</span><span class="sxs-lookup"><span data-stu-id="94df0-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="94df0-118">Grāmatošanas līmenis</span><span class="sxs-lookup"><span data-stu-id="94df0-118">Posting layer</span></span>                            | <span data-ttu-id="94df0-119">Atlasiet izmantojamo grāmatošanas līmeni.</span><span class="sxs-lookup"><span data-stu-id="94df0-119">Select the posting layer to use.</span></span> <span data-ttu-id="94df0-120">Katra grāmata, kas pievienota nomai, ir iestatīta noteiktam grāmatošanas līmenim.</span><span class="sxs-lookup"><span data-stu-id="94df0-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="94df0-121">Katram grāmatošanas līmenim ir atšķirīgi grāmatošanas mērķi.</span><span class="sxs-lookup"><span data-stu-id="94df0-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="94df0-122">Nomas veids</span><span class="sxs-lookup"><span data-stu-id="94df0-122">Lease type</span></span>                               | <span data-ttu-id="94df0-123">Atlasiet, vai noma ir jāklasificē automātiski, vai arī tā ir jādefinē kā finanšu vai operatīvā noma.</span><span class="sxs-lookup"><span data-stu-id="94df0-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="94df0-124">Uzskaites struktūra</span><span class="sxs-lookup"><span data-stu-id="94df0-124">Accounting framework</span></span>                     | <span data-ttu-id="94df0-125">Atlasiet struktūru, kas ir saistīta ar grāmatu.</span><span class="sxs-lookup"><span data-stu-id="94df0-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="94df0-126">Nomas termiņa/lietderīgās lietošanas laika iestatīšana</span><span class="sxs-lookup"><span data-stu-id="94df0-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="94df0-127">Sistēma klasificēs nomu kā finanšu nomu, ja nomas veids ir iestatīts uz **Automātisks** un ja nomas termiņš līdzekļa lietderīgās lietošanas laiks ir lielāks vai vienāds ar šajā laukā ievadīto procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="94df0-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="94df0-128">Pašreizējās vērtības/līdzekļa patiesās vērtības iestatīšana</span><span class="sxs-lookup"><span data-stu-id="94df0-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="94df0-129">Ievadiet veselu skaitli, lai definētu slieksni, kas noteiks nomas tipu.</span><span class="sxs-lookup"><span data-stu-id="94df0-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="94df0-130">Ja nākotnes minimālo nomas maksājumu pašreizējā vērtība ir lielāka par lietotāja definēto vērtību no grāmatas iestatījuma un grāmatas nomas klasifikācija ir iestatīta uz Automātisks, sistēma klasificēs nomu kā finanšu nomu.</span><span class="sxs-lookup"><span data-stu-id="94df0-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="94df0-131">Īstermiņa slieksnis</span><span class="sxs-lookup"><span data-stu-id="94df0-131">Short-term threshold</span></span>                     | <span data-ttu-id="94df0-132">Ievadiet mēnešu skaitu, ko izmantot kā slieksni īstermiņa nomām.</span><span class="sxs-lookup"><span data-stu-id="94df0-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="94df0-133">Ja nomas termiņš ir mazāks par vai vienāds ar šeit ievadīto mēnešu skaitu, sistēma klasificēs nomu kā īstermiņa nomu, un tiks piemērota atliktā nomas maksa.</span><span class="sxs-lookup"><span data-stu-id="94df0-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="94df0-134">Nelielas vērtības slieksnis</span><span class="sxs-lookup"><span data-stu-id="94df0-134">Low value threshold</span></span>                      | <span data-ttu-id="94df0-135">Ievadiet summu, ko izmantot kā nelielas vērtības nomas robežvērtību.</span><span class="sxs-lookup"><span data-stu-id="94df0-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="94df0-136">Ja līdzekļa patiesā vērtība ir mazāka par vai vienāda ar šeit ievadīto vērtību, sistēma klasificēs nomu kā nelielas vērtības nomu, un tiks piemērota atliktā nomas maksa.</span><span class="sxs-lookup"><span data-stu-id="94df0-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="94df0-137">Maksāt kreditoram</span><span class="sxs-lookup"><span data-stu-id="94df0-137">Pay to vendor</span></span>                            | <span data-ttu-id="94df0-138">Iestatiet šo opciju kā **Jā**, lai atļautu grāmatot nomas maksājumus kā rēķinu kreditora kontā, kas norādīts katrā nomā.</span><span class="sxs-lookup"><span data-stu-id="94df0-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="94df0-139">Kad nomas maksājums būs grāmatots, tiks kreditēts kreditora konts.</span><span class="sxs-lookup"><span data-stu-id="94df0-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="94df0-140">Ja šī opcija ir iestatīta uz **Nē**, tā vietā tiks kreditēts konts, kas ir norādīts lapas **Nomas grāmatošanas parametri** grāmatošanas tipam **Nomas maksājums**.</span><span class="sxs-lookup"><span data-stu-id="94df0-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
    | <span data-ttu-id="94df0-141">Līzinga līgums</span><span class="sxs-lookup"><span data-stu-id="94df0-141">Leasing convention</span></span>                       | <span data-ttu-id="94df0-142">Atlasiet konvenciju nomas sākuma datumam:</span><span class="sxs-lookup"><span data-stu-id="94df0-142">Select the convention for the commencement date of the lease:</span></span><ul><li><span data-ttu-id="94df0-143"><b>Neviens</b> – kā sākuma datumu izmantot nomas sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="94df0-143"><b>None</b> – Use the lease's start date as the commencement date.</span></span></li><li><span data-ttu-id="94df0-144"><b>Pilns mēnesis</b> – kā sākuma datumu izmanto tā mēneša pirmo dienu, kurā iekrīt nomas sākuma datums.</span><span class="sxs-lookup"><span data-stu-id="94df0-144"><b>Full month</b> – Use the first day of the month that the lease's start date falls in as the commencement date.</span></span></li></ul><p><span data-ttu-id="94df0-145">Ja atlasāt <b>Neviens</b>, pastāv risks, ka saistību norakstīšanas un līdzekļa nolietojuma grafiki uzkrās un iegrāmatos izdevumus mēneša vidū, nevis imēneša beigās.</span><span class="sxs-lookup"><span data-stu-id="94df0-145">If you select <b>None</b>, there is a risk that the liability amortization and asset depreciation schedules will accrue and post expenses in the middle of the month instead of at the end of the month.</span></span> <span data-ttu-id="94df0-146">Atlasot <b>Pilns mēnesis</b>, jūs nodrošināt, ka sistēma sāks uzskaitīt nomu mēneša pirmajā datumā un visa mēneša izdevumi tiks uzkrāti un grāmatoti mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="94df0-146">By selecting <b>Full month</b>, you ensure that the system will start to account for the lease on the first day of the month, and that the whole month's expense will be accrued and posted on the last day of the month.</span></span></p><p><span data-ttu-id="94df0-147"><strong>Piezīme.</strong> Nomas līgumu līdzeklis ir jāieslēdz, izmantojot Līdzekļu pārvaldību.</span><span class="sxs-lookup"><span data-stu-id="94df0-147"><strong>Note:</strong> The feature for leasing conventions must be turned on through Feature management.</span></span> <span data-ttu-id="94df0-148"><b>Līdzekļu pārvaldības</b> darbvietā atrodiet un atlasiet līdzekli ar nosaukumu <b>Nomas līgums līdzekļa iznomāšanai</b>, un pēc tam atlasiet <b>Iespējot tūlīt</b>.</span><span class="sxs-lookup"><span data-stu-id="94df0-148">In the <b>Feature management</b> workspace, find and select the feature that is named <b>Leasing convention for asset leasing</b> feature, and then select <b>Enable now</b>.</span></span></p> |