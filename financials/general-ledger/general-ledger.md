---
title: "Virsgrāmata un finanšu atskaišu veidošanas sākumlapa"
description: "Izmantojiet Virsgrāmatu, lai definētu un pārvaldītu juridiskās personas finanšu ierakstus. Virsgrāmata ir debeta un kredīta ierakstu reģistrs. Šie ieraksti tiek klasificēti, izmantojot kontus, kas uzskaitīti kontu plānā."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: lv-lv
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="6462a-105">Virsgrāmata</span><span class="sxs-lookup"><span data-stu-id="6462a-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6462a-106">Izmantojiet Virsgrāmatu, lai definētu un pārvaldītu juridiskās personas finanšu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="6462a-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="6462a-107">Virsgrāmata ir debeta un kredīta ierakstu reģistrs.</span><span class="sxs-lookup"><span data-stu-id="6462a-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="6462a-108">Šie ieraksti tiek klasificēti, izmantojot kontus, kas uzskaitīti kontu plānā.</span><span class="sxs-lookup"><span data-stu-id="6462a-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="6462a-109">Var sadalīt vai piešķirt naudas summas vienam vai vairākiem kontiem vai kontu un dimensiju kombinācijām, pamatojoties uz sadalījuma noteikumiem.</span><span class="sxs-lookup"><span data-stu-id="6462a-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="6462a-110">Ir divu tipu sadalījumi: fiksētais un mainīgais.</span><span class="sxs-lookup"><span data-stu-id="6462a-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="6462a-111">Var arī kārtot transakcijas starp Virsgrāmatas kontiem un pārvērtēt valūtas summas.</span><span class="sxs-lookup"><span data-stu-id="6462a-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="6462a-112">Finanšu gada beigās jums ir jāģenerē slēgšanas transakcijas un jāsagatavo jūsu konti nākošajam finanšu gadam.</span><span class="sxs-lookup"><span data-stu-id="6462a-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="6462a-113">Varat izmantot konsolidācijas funkcionalitāti, lai kombinētu finanšu rezultātus no vairākām juridiskajām personām vienā apvienotā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="6462a-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="6462a-114">Apakšuzņēmumi var būt tajā pašā Microsoft Dynamics 365 for Finance and Operations datu bāzē vai atsevišķās datu bāzēs.</span><span class="sxs-lookup"><span data-stu-id="6462a-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="6462a-115">PVN</span><span class="sxs-lookup"><span data-stu-id="6462a-115">Sales tax</span></span>
<span data-ttu-id="6462a-116">Katrs uzņēmums vāc un maksā nodokļus dažādām nodokļu iestādēm.</span><span class="sxs-lookup"><span data-stu-id="6462a-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="6462a-117">Noteikumi un likmes ir atkarīgi no valsts/reģiona, novada, administratīvā apgabala un pilsētas.</span><span class="sxs-lookup"><span data-stu-id="6462a-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="6462a-118">Turklāt kārtulas ir regulāri jāatjaunina, kad nodokļu iestādes maina savas prasības.</span><span class="sxs-lookup"><span data-stu-id="6462a-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="6462a-119">Pārdošanas nodokļa kodi satur pamatinformāciju par to, cik daudz iekasējat un maksājat šīm iestādēm.</span><span class="sxs-lookup"><span data-stu-id="6462a-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="6462a-120">Iestatot pārdošanas nodokļa kodus, jūs definējat summas vai procentus, kas ir jāiekasē.</span><span class="sxs-lookup"><span data-stu-id="6462a-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="6462a-121">Varat arī definēt dažādas metodes, ar kurām šīs summas vai procenti tiek piešķirti transakciju summām.</span><span class="sxs-lookup"><span data-stu-id="6462a-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="6462a-122">Šīs sadaļas tēmās ir sniegta informācija par to, kā iestatīt pārdošanas nodokļa kodus attiecībā uz metodēm un likmēm, ko pieprasa nodokļu iestādes.</span><span class="sxs-lookup"><span data-stu-id="6462a-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







