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
ms.openlocfilehash: 32271e967da2e7f3702b0c6c2dcdba460aa1b382
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770624"
---
# <a name="process-allocations"></a><span data-ttu-id="c52f9-105">Sadalījumu apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="c52f9-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c52f9-106">Šajā rakstā ir sniegta informācija par sadalījumiem, to apstrādes iespējām un to, kā tos var izmantot budžeta plānošanā.</span><span class="sxs-lookup"><span data-stu-id="c52f9-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="c52f9-107">Sadalījumi tiek izmantoti, lai summas izplatītu vairāku virsgrāmatu kontu kombinācijām.</span><span class="sxs-lookup"><span data-stu-id="c52f9-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="c52f9-108">Tie palīdz nodrošināt, ka izdevumi vai ieņēmumi uzskaitē tiek aprēķināti pareizajam objektam.</span><span class="sxs-lookup"><span data-stu-id="c52f9-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="c52f9-109">Tālāk norādītās iespējas atbalsta šo procesu.</span><span class="sxs-lookup"><span data-stu-id="c52f9-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="c52f9-110">Manuāla transakcijas summu sadale, izmantojot uzskaites sadales sadalīšanas darbību vai lietojot dokumentam finanšu dimensijas noklusējuma veidnes.</span><span class="sxs-lookup"><span data-stu-id="c52f9-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="c52f9-111">Papildinformāciju skatiet tēmā [Uzskaites sadales.](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="c52f9-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="c52f9-112">Automātiska transakcijas summu sadale, ņemot vērā atsevišķā galvenajā kontā definētos sadalījuma nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="c52f9-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="c52f9-113">Sadalījuma konta ieraksti tiek ģenerēti katram žurnālam, pamatojoties uz procentuālajām vērtībām un mērķa virsgrāmatas kontu, ikreiz, kad uzskaites ieraksts atbilst kritērijiem, kas norādīti kā avota virsgrāmatas konts.</span><span class="sxs-lookup"><span data-stu-id="c52f9-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="c52f9-114">Automātiska virsgrāmatas bilances vai fiksēto summu sadale, pamatojoties uz virsgrāmatas sadalījuma nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="c52f9-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="c52f9-115">Virsgrāmatas sadalījuma nosacījumi tiek apstrādāti periodiski, izmantojot sadalījuma žurnālus.</span><span class="sxs-lookup"><span data-stu-id="c52f9-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="c52f9-116">Sadalījumi budžeta plānošanas stadijā</span><span class="sxs-lookup"><span data-stu-id="c52f9-116">Allocations in budget planning</span></span>

<span data-ttu-id="c52f9-117">Virsgrāmatas sadalījuma nosacījumus var izmantot budžeta plānos.</span><span class="sxs-lookup"><span data-stu-id="c52f9-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="c52f9-118">Budžeta plānošanā izmantojot virsgrāmatas sadalījuma nosacījumus, sadalījuma nosacījumi darbojas tāpat kā virsgrāmatā, taču avota dati un mērķa dati tiek saņemti no budžeta plāna.</span><span class="sxs-lookup"><span data-stu-id="c52f9-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="c52f9-119">Varat manuāli atlasīt budžeta plāniem izmantojamos virsgrāmatas sadalījuma nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="c52f9-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="c52f9-120">Varat arī izmantot sadalījuma grafiku, kas darbojas kā daļa no darbplūsmas procesa.</span><span class="sxs-lookup"><span data-stu-id="c52f9-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="c52f9-121">Starpuzņēmuma virsgrāmatas sadalījuma nosacījumus nevar izmantot budžeta plānošanai.</span><span class="sxs-lookup"><span data-stu-id="c52f9-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>





