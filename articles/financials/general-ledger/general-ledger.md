---
title: Virsgrāmata un finanšu atskaišu veidošanas sākumlapa
description: Izmantojiet Virsgrāmatu, lai definētu un pārvaldītu juridiskās personas finanšu ierakstus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85afebcc88ad1c087d5f1dabaac56f694534cf98
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "363365"
---
# <a name="general-ledger"></a><span data-ttu-id="ddaa9-103">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="ddaa9-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddaa9-104">Izmantojiet Virsgrāmatu, lai definētu un pārvaldītu juridiskās personas finanšu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="ddaa9-105">Virsgrāmata ir debeta un kredīta ierakstu reģistrs.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="ddaa9-106">Šie ieraksti tiek klasificēti, izmantojot kontus, kas uzskaitīti kontu plānā.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="ddaa9-107">Plānot kontu plānu</span><span class="sxs-lookup"><span data-stu-id="ddaa9-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="ddaa9-108">Galvenā konta tipi</span><span class="sxs-lookup"><span data-stu-id="ddaa9-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="ddaa9-109">Var sadalīt vai piešķirt naudas summas vienam vai vairākiem kontiem vai kontu un dimensiju kombinācijām, pamatojoties uz sadalījuma noteikumiem.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="ddaa9-110">Ir divu tipu sadalījumi: fiksētais un mainīgais.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="ddaa9-111">Var arī kārtot transakcijas starp Virsgrāmatas kontiem un pārvērtēt valūtas summas.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="ddaa9-112">Finanšu gada beigās jums ir jāģenerē slēgšanas transakcijas un jāsagatavo jūsu konti nākošajam finanšu gadam.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="ddaa9-113">Varat izmantot konsolidācijas funkcionalitāti, lai kombinētu finanšu rezultātus no vairākām juridiskajām personām vienā apvienotā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="ddaa9-114">Apakšuzņēmumi var būt ietverti tajā pašā Microsoft Dynamics 365 for Finance and Operations datu bāzē vai atsevišķās datu bāzēs.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="ddaa9-115">Konsolidēšanas un koriģēšanas apskats</span><span class="sxs-lookup"><span data-stu-id="ddaa9-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="ddaa9-116">Virsgrāmatas konta bilances</span><span class="sxs-lookup"><span data-stu-id="ddaa9-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="ddaa9-117">Finanšu dimensijas</span><span class="sxs-lookup"><span data-stu-id="ddaa9-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="ddaa9-118">[![Biznesa process](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="ddaa9-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="ddaa9-119">PVN</span><span class="sxs-lookup"><span data-stu-id="ddaa9-119">Sales tax</span></span>
<span data-ttu-id="ddaa9-120">Katrs uzņēmums vāc un maksā nodokļus dažādām nodokļu iestādēm.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="ddaa9-121">Noteikumi un likmes ir atkarīgi no valsts/reģiona, novada, administratīvā apgabala un pilsētas.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="ddaa9-122">Turklāt kārtulas ir regulāri jāatjaunina, kad nodokļu iestādes maina savas prasības.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="ddaa9-123">Pārdošanas nodokļa kodi satur pamatinformāciju par to, cik daudz iekasējat un maksājat šīm iestādēm.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="ddaa9-124">Iestatot pārdošanas nodokļa kodus, jūs definējat summas vai procentus, kas ir jāiekasē.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="ddaa9-125">Varat arī definēt dažādas metodes, ar kurām šīs summas vai procenti tiek piešķirti transakciju summām.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="ddaa9-126">Šīs sadaļas tēmās ir sniegta informācija par to, kā iestatīt pārdošanas nodokļa kodus attiecībā uz metodēm un likmēm, ko pieprasa nodokļu iestādes.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="ddaa9-127">PVN apskats</span><span class="sxs-lookup"><span data-stu-id="ddaa9-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="ddaa9-128">PVN likmju aprēķins, pamatojoties uz laukiem Aprēķina pamatā un Aprēķina metode</span><span class="sxs-lookup"><span data-stu-id="ddaa9-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="ddaa9-129">PVN maksājumi un noapaļošanas kārtulas</span><span class="sxs-lookup"><span data-stu-id="ddaa9-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="ddaa9-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ddaa9-130">Additional resources</span></span>

### <a name="whats-new"></a><span data-ttu-id="ddaa9-131">Kas jauns</span><span class="sxs-lookup"><span data-stu-id="ddaa9-131">What's new</span></span>

<span data-ttu-id="ddaa9-132">Lai uzzinātu par jaunajiem līdzekļiem, dodieties uz [Informācija par laidienu](https://docs.microsoft.com/en-us/business-applications-release-notes/).</span><span class="sxs-lookup"><span data-stu-id="ddaa9-132">Go to the [Release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/) to see what new features have been released.</span></span> 

### <a name="videos"></a><span data-ttu-id="ddaa9-133">Videoklipi</span><span class="sxs-lookup"><span data-stu-id="ddaa9-133">Videos</span></span>

<span data-ttu-id="ddaa9-134">Apskatiet video pamācības, kas tagad ir pieejamas [Microsoft Dynamics 365 YouTube kanālā](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="ddaa9-134">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

### <a name="blogs"></a><span data-ttu-id="ddaa9-135">Emuāri</span><span class="sxs-lookup"><span data-stu-id="ddaa9-135">Blogs</span></span>

<span data-ttu-id="ddaa9-136">Viedokļi, ziņas un cita informācija par moduli Kreditori un citiem risinājumiem ir pieejami [Microsoft Dynamics 365 emuārā](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span><span class="sxs-lookup"><span data-stu-id="ddaa9-136">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="ddaa9-137">[Microsoft Dynamics AX produktu darba grupas emuārā](https://blogs.msdn.microsoft.com/dax/) ir daudz rakstu par Virsgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-137">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="ddaa9-138">Lai gan daži no šiem rakstiem tika rakstīti iepriekšējai virsgrāmatas versijai, joprojām ir spēkā tie paši jēdzieni, un arī procedūras pašreizējā versijā ir līdzīgas.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-138">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="ddaa9-139">[Microsoft Dynamics Operations partneru kopienas emuārā](https://community.dynamics.com/partner/b/operationspartnercommunityblog) Microsoft Dynamics partneriem tiek sniegts vienots resurss, kur uzzināt par jaunumiem un tendencēm risinājumā MBS Operations.</span><span class="sxs-lookup"><span data-stu-id="ddaa9-139">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="ddaa9-140">Kopienas emuāri</span><span class="sxs-lookup"><span data-stu-id="ddaa9-140">Community blogs</span></span>

- [<span data-ttu-id="ddaa9-141">Svarīgākā informācija par Virsgrāmatu programmā Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddaa9-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

