---
title: Virsgrāmatas slēgšana perioda beigās
description: Šajā tēmā ir aprakstīti uzdevumi, kas parasti tiek veikti, virsgrāmatai izpildot perioda slēgšanu.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eca533ed1621ec3507d8510f75842c0f0165275
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839549"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="38cb9-103">Virsgrāmatas slēgšana perioda beigās</span><span class="sxs-lookup"><span data-stu-id="38cb9-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38cb9-104">Šajā tēmā ir aprakstīti uzdevumi, kas parasti tiek veikti, virsgrāmatai izpildot perioda slēgšanu.</span><span class="sxs-lookup"><span data-stu-id="38cb9-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="38cb9-105">Virsgrāmatā varat izpildīt perioda vai gada slēgšanas procedūru.</span><span class="sxs-lookup"><span data-stu-id="38cb9-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="38cb9-106">Slēgšanas procesi sagatavo sistēmu jaunajam periodam.</span><span class="sxs-lookup"><span data-stu-id="38cb9-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="38cb9-107">Lai sistēmu sagatavotu jaunam gadam, ir jāpalaiž gada beigu slēgšanas process.</span><span class="sxs-lookup"><span data-stu-id="38cb9-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="38cb9-108">Katrai organizācijai ir atšķirīgi procesi un darbības, kas jāveic perioda beigās.</span><span class="sxs-lookup"><span data-stu-id="38cb9-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="38cb9-109">Dažas no neobligātajām darbībām perioda beigās ir šādas:</span><span class="sxs-lookup"><span data-stu-id="38cb9-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="38cb9-110">pabeigt visus uzdevumus visiem citiem moduļiem, piemēram, Debitoru parādi, Kreditori un Krājumi;</span><span class="sxs-lookup"><span data-stu-id="38cb9-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="38cb9-111">pārbaudīt, vai visi žurnāli ir grāmatoti;</span><span class="sxs-lookup"><span data-stu-id="38cb9-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="38cb9-112">palaist ārvalstu valūtas pārvērtēšanas procesu, lai ģenerētu nerealizētās peļņas vai zaudējumu summas;</span><span class="sxs-lookup"><span data-stu-id="38cb9-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="38cb9-113">nosegt transakcijas visos virsgrāmatas kontos;</span><span class="sxs-lookup"><span data-stu-id="38cb9-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="38cb9-114">apstrādāt visus nepieciešamos sadalījumus;</span><span class="sxs-lookup"><span data-stu-id="38cb9-114">Process any required allocations.</span></span>
-   <span data-ttu-id="38cb9-115">manuāli grāmatot perioda beigu korekcijas;</span><span class="sxs-lookup"><span data-stu-id="38cb9-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="38cb9-116">reģistrēt žurnālā darbības un pārskatīt pārskatu **Virsgrāmatas žurnāls**;</span><span class="sxs-lookup"><span data-stu-id="38cb9-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="38cb9-117">veikt konsolidāciju, izmantojot konsolidēšanas uzņēmumu vai finanšu pārskatu;</span><span class="sxs-lookup"><span data-stu-id="38cb9-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="38cb9-118">ģenerēt perioda beigu finanšu pārskatus, izmantojot finanšu pārskatus;</span><span class="sxs-lookup"><span data-stu-id="38cb9-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="38cb9-119">iestatīt virsgrāmatas periodiem statusu **Aizturēta**, lai tālāka grāmatošana netiek veikta.</span><span class="sxs-lookup"><span data-stu-id="38cb9-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="38cb9-120">Lai atvieglotu kontroli, var arī ierobežot periodu noteiktai lietotāju grupai, kamēr tiek izpldītas perioda beigu darbības.</span><span class="sxs-lookup"><span data-stu-id="38cb9-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="38cb9-121">Nav ieteicams periodiem iestatīt statusu **Neatgriezeniski slēgts**, jo slēgtu periodu nevar atvērt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="38cb9-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="38cb9-122">Lai kārtotu un izsekotu dažādu periodu beigu procesiem nepieciešamos uzdevumus, var lietot darbvietu Finanšu perioda slēgšana.</span><span class="sxs-lookup"><span data-stu-id="38cb9-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="38cb9-123">Papildinformāciju skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="38cb9-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="38cb9-124">Finanšu perioda slēgšanas darbvieta</span><span class="sxs-lookup"><span data-stu-id="38cb9-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="38cb9-125">Gada beigu slēgšana</span><span class="sxs-lookup"><span data-stu-id="38cb9-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="38cb9-126">Masveida finanšu periodu slēgšana</span><span class="sxs-lookup"><span data-stu-id="38cb9-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)




