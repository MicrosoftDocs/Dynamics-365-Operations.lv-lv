---
title: Sadalījumu apstrāde
description: Šajā rakstā ir sniegta informācija par sadalījumiem, to apstrādes iespējām programmā Microsoft Dynamics 365 Finance un to, kā tos var izmantot budžeta plānošanā. Sadalījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām. Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8216ebdd1f26601743e6b35849be0813d06b4a
ms.sourcegitcommit: 4676ea9646fa1a182103ecab93e78a69001f0b8d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/21/2020
ms.locfileid: "3612666"
---
# <a name="process-allocations"></a><span data-ttu-id="43810-105">Sadalījumu apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="43810-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43810-106">Šajā rakstā ir sniegta informācija par sadalījumiem, to apstrādes iespējām un to, kā tos var izmantot budžeta plānošanā.</span><span class="sxs-lookup"><span data-stu-id="43810-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="43810-107">Sadalījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām.</span><span class="sxs-lookup"><span data-stu-id="43810-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="43810-108">Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam.</span><span class="sxs-lookup"><span data-stu-id="43810-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="43810-109">Tālāk norādītās iespējas atbalsta šo procesu.</span><span class="sxs-lookup"><span data-stu-id="43810-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="43810-110">Manuāla transakcijas summu sadale, izmantojot uzskaites sadales sadalīšanas darbību vai lietojot dokumentam finanšu dimensijas noklusējuma veidnes.</span><span class="sxs-lookup"><span data-stu-id="43810-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="43810-111">Papildinformāciju skatiet tēmā [Uzskaites sadales.](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="43810-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="43810-112">Automātiska transakcijas summu sadale, ņemot vērā atsevišķā galvenajā kontā definētos sadalījuma nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="43810-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="43810-113">Sadalījuma konta ieraksti tiek ģenerēti katram žurnālam, pamatojoties uz procentuālajām vērtībām un mērķa virsgrāmatas kontu, ikreiz, kad uzskaites ieraksts atbilst kritērijiem, kas norādīti kā avota virsgrāmatas konts.</span><span class="sxs-lookup"><span data-stu-id="43810-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="43810-114">Papildinformāciju skatiet šeit: [Galvenā konta sadalījuma nosacījumi](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="43810-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="43810-115">Automātiska virsgrāmatas bilances vai fiksēto summu sadale, pamatojoties uz virsgrāmatas sadalījuma nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="43810-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="43810-116">Virsgrāmatas sadalījuma nosacījumi tiek apstrādāti periodiski, izmantojot sadalījuma žurnālus.</span><span class="sxs-lookup"><span data-stu-id="43810-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="43810-117">Papildinformāciju skatiet [Sadalījuma kārtulas](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="43810-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="43810-118">Sadalījumi budžeta plānošanas stadijā</span><span class="sxs-lookup"><span data-stu-id="43810-118">Allocations in budget planning</span></span>

<span data-ttu-id="43810-119">Virsgrāmatas sadalījuma nosacījumus var izmantot budžeta plānos.</span><span class="sxs-lookup"><span data-stu-id="43810-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="43810-120">Budžeta plānošanā izmantojot virsgrāmatas sadalījuma nosacījumus, sadalījuma nosacījumi darbojas tāpat kā virsgrāmatā, taču avota dati un mērķa dati tiek saņemti no budžeta plāna.</span><span class="sxs-lookup"><span data-stu-id="43810-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="43810-121">Varat manuāli atlasīt budžeta plāniem izmantojamos virsgrāmatas sadalījuma nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="43810-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="43810-122">Varat arī izmantot sadalījuma grafiku, kas darbojas kā daļa no darbplūsmas procesa.</span><span class="sxs-lookup"><span data-stu-id="43810-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="43810-123">Starpuzņēmuma virsgrāmatas sadalījuma nosacījumus nevar izmantot budžeta plānošanai.</span><span class="sxs-lookup"><span data-stu-id="43810-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>

