---
title: "Plānot kontu plānu"
description: "Šajā tēmā ir sniegta informācija, kas jums palīdzēs savai organizācijai plānot kontu plānu."
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d6106125af91f8bf9b3ffc3047578f6c6f60f0eb
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="4c404-103">Plānot kontu plānu</span><span class="sxs-lookup"><span data-stu-id="4c404-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c404-104">Šajā tēmā ir sniegta informācija, kas jums palīdzēs savai organizācijai plānot kontu plānu.</span><span class="sxs-lookup"><span data-stu-id="4c404-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="4c404-105">Lai organizācijā izsekotu un uzturētu finanšu informāciju, varat iestatīt kontu plānu.</span><span class="sxs-lookup"><span data-stu-id="4c404-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="4c404-106">Kontu plāns ir kontu kopa, kas definē finanšu shēmu.</span><span class="sxs-lookup"><span data-stu-id="4c404-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="4c404-107">Lai turpmāk izsekotu šo kontu transakcijas, varat pievienot segmentus.</span><span class="sxs-lookup"><span data-stu-id="4c404-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="4c404-108">Šos segmentus sauc par finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="4c404-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="4c404-109">Piemēram, izdevumu kontā var iekļaut šādas finanšu dimensijas: Nodaļa, Izmaksu centrs un Nolūks.</span><span class="sxs-lookup"><span data-stu-id="4c404-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="4c404-110">Lietotāja definētās kārtulas nosaka to, kā finanšu dimensijas tiek pievienotas galvenajiem kontiem un citām finanšu dimensijām, kā arī to, kā var ievadīt transakcijas.</span><span class="sxs-lookup"><span data-stu-id="4c404-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="4c404-111">Šīs lietotāja definētās kārtulas sauc par konta struktūrām un papildu kārtulām.</span><span class="sxs-lookup"><span data-stu-id="4c404-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="4c404-112">Kontu plāns ir juridiskas personas virsgrāmatas kontu strukturētais saraksts.</span><span class="sxs-lookup"><span data-stu-id="4c404-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="4c404-113">Saraksts tiek lietots, lai sagatavotu finanšu pārskatus iestādēm un īpašniekiem.</span><span class="sxs-lookup"><span data-stu-id="4c404-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="4c404-114">Konti vispirms tiek grupēti kontu veidos un pēc tam apkopoti lielākās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="4c404-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="4c404-115">Vispārīgā līmenī konti tiek grupēti kā ieņēmumi un izmaksas (operāciju konti) un kā aktīvi un pasīvi (bilances konti).</span><span class="sxs-lookup"><span data-stu-id="4c404-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="4c404-116">Kontu plānu var kopīgot un jebkura juridiskā persona organizācijā to var izmantot.</span><span class="sxs-lookup"><span data-stu-id="4c404-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="4c404-117">Kontu plāns, ko izmanto juridiskā persona, tiek definēts lapā **Virsgrāmata**.</span><span class="sxs-lookup"><span data-stu-id="4c404-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="4c404-118">Tālāk ir minēti daži faktori, kas jāņem vērā, plānojot savas organizācijas kontu plāna strukturu.</span><span class="sxs-lookup"><span data-stu-id="4c404-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="4c404-119">Valsts vai reģiona, kurā ir bāzēta jūsu organizācija, atskaišu prasības</span><span class="sxs-lookup"><span data-stu-id="4c404-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="4c404-120">Juridiskās personas prasības atskaišu veidošanai</span><span class="sxs-lookup"><span data-stu-id="4c404-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="4c404-121">Nepieciešamā specifikācijas pakāpe ārējās organizācijās un savā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="4c404-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="4c404-122">Veidojiet kontu plānu lapā **Kontu plāns**.</span><span class="sxs-lookup"><span data-stu-id="4c404-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="4c404-123">Galvenos kontus varat izveidot lapā **Kontu plāns** vai **Galvenie konti**.</span><span class="sxs-lookup"><span data-stu-id="4c404-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="4c404-124">Galvenajos kontos nevajadzētu izmantot speciālās rakstzīmes, ko izmanto kā kontu plāna norobežotājus.</span><span class="sxs-lookup"><span data-stu-id="4c404-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="4c404-125">Pretējā gadījumā var veidoties nestabilitāte vai arī būs nepieciešams vienmēr izmantot uzmeklēšanas rezultātus vai dialoglodziņu, ievadot kontu un dimensiju kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="4c404-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="4c404-126">Papildinformāciju skatiet šeit: [Izveidot galveno kontu](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="4c404-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4c404-127">Microsoft Dynamics 365 for Finance and Operations versijā 8.0 (2018. gada aprīlis) var modificēt kontu plāna norobežotāju lapā **Virsgrāmatas parametri**.</span><span class="sxs-lookup"><span data-stu-id="4c404-127">In Microsoft Dynamics for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="4c404-128">Ir ieteicams saistīt galvenos kontus ar galvenā konta kategorijām, lai varētu izmantot noklusējuma finanšu pārskatus, neveicot jebkādas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="4c404-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="4c404-129">Tādējādi varat ātrāk un vieglāk izstrādāt un uzturēt pārskatus.</span><span class="sxs-lookup"><span data-stu-id="4c404-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="4c404-130">Kontu struktūras varat izveidot lapā **Konfigurēt kontu struktūras**.</span><span class="sxs-lookup"><span data-stu-id="4c404-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="4c404-131">Kontu struktūras nosaka derīgās kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="4c404-131">Account structures define valid combinations.</span></span> <span data-ttu-id="4c404-132">Šīs kombinācijas kopā ar galvenajiem kontiem izveido kontu plānu.</span><span class="sxs-lookup"><span data-stu-id="4c404-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="4c404-133">Papildinformāciju skatiet šeit: [Izveidot kontu struktūras](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="4c404-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="4c404-134">**Juridiskas personas prioritātes**</span><span class="sxs-lookup"><span data-stu-id="4c404-134">**Legal entity overrides**</span></span>

<span data-ttu-id="4c404-135">Daži galvenie konti nav derīgi visām juridiskajām personām un var attiekties tikai uz noteiktu laika periodu.</span><span class="sxs-lookup"><span data-stu-id="4c404-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="4c404-136">Šādā gadījumā varat izmantot sadaļu **Juridiskas personas prioritātes**, lai identificētu uzņēmumus, attiecībā uz kuriem šis galvenais konts ir jāaiztur, kā arī īpašnieku un periodu, kad šī dimensija ir aktīva.</span><span class="sxs-lookup"><span data-stu-id="4c404-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="4c404-137">Koplietošanas līmenī prioritātes nevar būt vairāk ierobežojošas nekā prioritātes, kas ir juridiskās personas līmenī.</span><span class="sxs-lookup"><span data-stu-id="4c404-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="4c404-138">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="4c404-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="4c404-139">Finanšu dimensijas</span><span class="sxs-lookup"><span data-stu-id="4c404-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="4c404-140">Papildu kārtulu struktūru izveide un piešķiršana</span><span class="sxs-lookup"><span data-stu-id="4c404-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)

