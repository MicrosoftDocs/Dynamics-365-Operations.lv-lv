---
title: Virsgrāmatas kalendāra maiņa vai atkārtota piešķiršana
description: Šajā tēmā skaidrots, kā mainīt virsgrāmatai pašreiz piešķirto kalendāru un kā virsgrāmatai piešķirt jaunu kalendāru.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039954"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="a95e5-103">Virsgrāmatas kalendāra maiņa vai atkārtota piešķiršana</span><span class="sxs-lookup"><span data-stu-id="a95e5-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a95e5-104">Šajā tēmā skaidrots, kā mainīt virsgrāmatai pašreiz piešķirto kalendāru un kā virsgrāmatai piešķirt jaunu kalendāru.</span><span class="sxs-lookup"><span data-stu-id="a95e5-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="a95e5-105">Problēma</span><span class="sxs-lookup"><span data-stu-id="a95e5-105">Issue</span></span>

<span data-ttu-id="a95e5-106">Dažkārt uzņēmumiem ir jāmaina esošais kalendārs, kas ir piešķirts virsgrāmatai, vai jāpiešķir jauns kalendārs.</span><span class="sxs-lookup"><span data-stu-id="a95e5-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="a95e5-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="a95e5-107">Resolution</span></span>

<span data-ttu-id="a95e5-108">Pastāv divi virsgrāmatas kalendāra maiņas vai atkārtotas piešķires scenāriji.</span><span class="sxs-lookup"><span data-stu-id="a95e5-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="a95e5-109">Pirmais scenārijs ir saistīts ar esoša kalendāra, kas jau ir piešķirts virsgrāmatai, maiņu.</span><span class="sxs-lookup"><span data-stu-id="a95e5-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="a95e5-110">Otrais scenārijs ietver jauna kalendāra izveidi un tā piešķiršanu virsgrāmatai.</span><span class="sxs-lookup"><span data-stu-id="a95e5-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="a95e5-111">Abas izmaiņas var veikt jebkurā laikā, pat pēc transakciju iegrāmatošanas virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="a95e5-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="a95e5-112">Esoša finanšu kalendāra maiņa</span><span class="sxs-lookup"><span data-stu-id="a95e5-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="a95e5-113">Lai mainītu esošu kalendāru, kas ir piešķirts jūsu virsgrāmatai, dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmata** un atlasiet finanšu kalendāra saiti, lai atvērtu lapu **Virsgrāmatas kalendāri**.</span><span class="sxs-lookup"><span data-stu-id="a95e5-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="a95e5-114">Pastāv ierobežojumi izmaiņām, kuras var veikt kalendārā.</span><span class="sxs-lookup"><span data-stu-id="a95e5-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="a95e5-115">Piemēram, varat mainīt gada *periodu* sākuma un beigu datumus, bet kalendārā nevar mainīt *gada* sākuma un beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="a95e5-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="a95e5-116">Lai mainītu periodus gadā, atlasiet atbilstošo kalendāru un gadu.</span><span class="sxs-lookup"><span data-stu-id="a95e5-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="a95e5-117">Vispirms izmantojiet pogu **Dzēst periodu**, lai dzēstu dažus vai visus esošos darba periodus.</span><span class="sxs-lookup"><span data-stu-id="a95e5-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="a95e5-118">Varat dzēst visus darbības periodus, izņemot pirmo.</span><span class="sxs-lookup"><span data-stu-id="a95e5-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="a95e5-119">Pēc tam izmantojiet pogu **Sadalīt periodu**, lai atlikušo periodu vai periodus sadalītu jaunos periodos, ievadot nākamā perioda atbilstošo sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="a95e5-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="a95e5-120">Pēc periodu maiņas kalendārā katrai juridiskajai personai (uzņēmumam), kam kalendārs ir piešķirts, jāpalaiž process **Pārrēķināt virsgrāmatas periodus**.</span><span class="sxs-lookup"><span data-stu-id="a95e5-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="a95e5-121">Lai gan nav brīdinājuma ziņojuma, kas atgādinātu par nepieciešamību pabeigt šo darbību, pārrēķina procesā ir nepieciešams atjaunināt periodu, kas ir piešķirts katrai virsgrāmatā iegrāmatotajai transakcijai.</span><span class="sxs-lookup"><span data-stu-id="a95e5-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="a95e5-122">Lai izpildītu pārrēķināšanas procesu, katra uzņēmuma lapā **Virsgrāmatas iestatīšana** atlasiet **Pārrēķināt virsgrāmatas periodus**.</span><span class="sxs-lookup"><span data-stu-id="a95e5-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="a95e5-123">Ja pārrēķina process netiks izpildīts, transakciju bilances apgrozījuma bilancē vai finanšu pārskatos var būt nepareizi iekļautas periodos.</span><span class="sxs-lookup"><span data-stu-id="a95e5-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="a95e5-124">Šādā gadījumā bilances var labot jebkurā laikā, palaižot pārrēķināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="a95e5-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="a95e5-125">Jauna finanšu kalendāra piešķiršana</span><span class="sxs-lookup"><span data-stu-id="a95e5-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="a95e5-126">Lai piešķirtu jaunu finanšu kalendāru, dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmata** un atlasiet **Rediģēt**, lai lapa **Virsgrāmata** pārietu rediģēšanas režīmā.</span><span class="sxs-lookup"><span data-stu-id="a95e5-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="a95e5-127">Pēc tam laukā **Finanšu kalendārs** atlasiet jaunu finanšu kalendāru.</span><span class="sxs-lookup"><span data-stu-id="a95e5-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="a95e5-128">Pēc virsgrāmatas finanšu kalendāra maiņas ir jāizpilda darbība **Pārrēķināt virsgrāmatas periodus**.</span><span class="sxs-lookup"><span data-stu-id="a95e5-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="a95e5-129">Kad piešķirat virsgrāmatai jaunu finanšu kalendāru, ziņojums atgādina par nepieciešamību pabeigt šo darbību.</span><span class="sxs-lookup"><span data-stu-id="a95e5-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="a95e5-130">Kaut arī ziņojums šķietami norāda, ka pārrēķina process ir neobligāts, tā nav taisnība.</span><span class="sxs-lookup"><span data-stu-id="a95e5-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="a95e5-131">Jāatjaunina periods, kas piešķirts katrai virsgrāmatā iegrāmatotai transakcijai.</span><span class="sxs-lookup"><span data-stu-id="a95e5-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="a95e5-132">Lai izpildītu pārrēķināšanas procesu, lapā **Virsgrāmatas iestatīšana** atlasiet **Pārrēķināt virsgrāmatas periodus**.</span><span class="sxs-lookup"><span data-stu-id="a95e5-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="a95e5-133">Ja pārrēķina process netiks izpildīts, transakciju bilances apgrozījuma bilancē vai finanšu pārskatos var būt nepareizi iekļautas periodos.</span><span class="sxs-lookup"><span data-stu-id="a95e5-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="a95e5-134">Šādā gadījumā bilances var labot jebkurā laikā, palaižot pārrēķināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="a95e5-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
