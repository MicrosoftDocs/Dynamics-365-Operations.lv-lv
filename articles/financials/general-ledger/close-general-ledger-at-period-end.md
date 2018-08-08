---
title: "Virsgrāmatas slēgšana perioda beigās"
description: "Šajā tēmā ir aprakstīti uzdevumi, kas parasti tiek veikti, virsgrāmatai izpildot perioda slēgšanu."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 23d4b9b070a48e1964ecd6896afe071b564d1194
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="c80e8-103">Virsgrāmatas slēgšana perioda beigās</span><span class="sxs-lookup"><span data-stu-id="c80e8-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c80e8-104">Šajā tēmā ir aprakstīti uzdevumi, kas parasti tiek veikti, virsgrāmatai izpildot perioda slēgšanu.</span><span class="sxs-lookup"><span data-stu-id="c80e8-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="c80e8-105">Virsgrāmatā varat izpildīt perioda vai gada slēgšanas procedūru.</span><span class="sxs-lookup"><span data-stu-id="c80e8-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="c80e8-106">Slēgšanas procesi sagatavo sistēmu jaunajam periodam.</span><span class="sxs-lookup"><span data-stu-id="c80e8-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="c80e8-107">Lai sistēmu sagatavotu jaunam gadam, ir jāpalaiž gada beigu slēgšanas process.</span><span class="sxs-lookup"><span data-stu-id="c80e8-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="c80e8-108">Katrai organizācijai ir atšķirīgi procesi un darbības, kas jāveic perioda beigās.</span><span class="sxs-lookup"><span data-stu-id="c80e8-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="c80e8-109">Dažas no neobligātajām darbībām perioda beigās ir šādas:</span><span class="sxs-lookup"><span data-stu-id="c80e8-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="c80e8-110">pabeigt visus uzdevumus visiem citiem moduļiem, piemēram, Debitoru parādi, Kreditori un Krājumi;</span><span class="sxs-lookup"><span data-stu-id="c80e8-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="c80e8-111">pārbaudīt, vai visi žurnāli ir grāmatoti;</span><span class="sxs-lookup"><span data-stu-id="c80e8-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="c80e8-112">palaist ārvalstu valūtas pārvērtēšanas procesu, lai ģenerētu nerealizētās peļņas vai zaudējumu summas;</span><span class="sxs-lookup"><span data-stu-id="c80e8-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="c80e8-113">nosegt transakcijas visos virsgrāmatas kontos;</span><span class="sxs-lookup"><span data-stu-id="c80e8-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="c80e8-114">apstrādāt visus nepieciešamos sadalījumus;</span><span class="sxs-lookup"><span data-stu-id="c80e8-114">Process any required allocations.</span></span>
-   <span data-ttu-id="c80e8-115">manuāli grāmatot perioda beigu korekcijas;</span><span class="sxs-lookup"><span data-stu-id="c80e8-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="c80e8-116">reģistrēt žurnālā darbības un pārskatīt pārskatu **Virsgrāmatas žurnāls**;</span><span class="sxs-lookup"><span data-stu-id="c80e8-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="c80e8-117">veikt konsolidāciju, izmantojot konsolidēšanas uzņēmumu vai finanšu pārskatu;</span><span class="sxs-lookup"><span data-stu-id="c80e8-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="c80e8-118">ģenerēt perioda beigu finanšu pārskatus, izmantojot finanšu pārskatus;</span><span class="sxs-lookup"><span data-stu-id="c80e8-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="c80e8-119">iestatīt virsgrāmatas periodiem statusu **Aizturēta**, lai tālāka grāmatošana netiek veikta.</span><span class="sxs-lookup"><span data-stu-id="c80e8-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="c80e8-120">Lai atvieglotu kontroli, var arī ierobežot periodu noteiktai lietotāju grupai, kamēr tiek izpldītas perioda beigu darbības.</span><span class="sxs-lookup"><span data-stu-id="c80e8-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="c80e8-121">Nav ieteicams periodiem iestatīt statusu **Neatgriezeniski slēgts**, jo slēgtu periodu nevar atvērt atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="c80e8-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="c80e8-122">Lai kārtotu un izsekotu dažādu periodu beigu procesiem nepieciešamos uzdevumus, var lietot darbvietu Finanšu perioda slēgšana.</span><span class="sxs-lookup"><span data-stu-id="c80e8-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="c80e8-123">Papildinformāciju skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="c80e8-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="c80e8-124">Finanšu perioda slēgšanas darbvieta</span><span class="sxs-lookup"><span data-stu-id="c80e8-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="c80e8-125">Gada beigu slēgšana</span><span class="sxs-lookup"><span data-stu-id="c80e8-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="c80e8-126">Masveida finanšu periodu slēgšana</span><span class="sxs-lookup"><span data-stu-id="c80e8-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)





