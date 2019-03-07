---
title: Virsgrāmatas sadalījuma žurnāla apstrāde
description: Izmantojiet lapu Apstrādāt piešķiršanas pieprasījumu, lai izveidotu sadalījuma žurnālu, ko var pārskatīt un apstiprināt pirms grāmatošanas Virsgrāmatā vai grāmatot tieši Virsgrāmatā.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2046e25719c9023bee99736488a4ee6f22723fe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "335650"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="92825-103">Virsgrāmatas sadalījuma žurnāla apstrāde</span><span class="sxs-lookup"><span data-stu-id="92825-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92825-104">Izmantojiet lapu Apstrādāt piešķiršanas pieprasījumu, lai izveidotu sadalījuma žurnālu, ko var pārskatīt un apstiprināt pirms grāmatošanas Virsgrāmatā vai grāmatot tieši Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="92825-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="92825-105">Pirms varēsiet izveidot sadalījumu žurnālu, jābūt vismaz vienai aktīvai Virsgrāmatas sadalījuma kārtulai.</span><span class="sxs-lookup"><span data-stu-id="92825-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="92825-106">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="92825-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="92825-107">Dodieties uz Virsgrāmata > Sadalījumi > Apstrādāt sadalījuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="92825-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="92825-108">Laukā Kārtula noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="92825-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="92825-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="92825-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="92825-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="92825-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="92825-111">Laukā No datuma ievadiet datumu,</span><span class="sxs-lookup"><span data-stu-id="92825-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="92825-112">No datuma ir ļoti svarīgs, ja Virsgrāmata ir noteikumu datu avotu.</span><span class="sxs-lookup"><span data-stu-id="92825-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="92825-113">Šis datums kontrolē, kuras Virsgrāmatas bilances iekļaut sadalījumā.</span><span class="sxs-lookup"><span data-stu-id="92825-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="92825-114">Laukā Nulles avots izvēlieties Apturēt.</span><span class="sxs-lookup"><span data-stu-id="92825-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="92825-115">Šādi tiks apturēts sadalījuma process un parādīts ziņojums, ka ir atlasīta nulles avota summa.</span><span class="sxs-lookup"><span data-stu-id="92825-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="92825-116">Laukā Priekšlikumu opcijas atlasiet "Tikai priekšlikums".</span><span class="sxs-lookup"><span data-stu-id="92825-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="92825-117">Atlasiet Priekšlikums tikai lai pārskatītu un pēc izvēles apstiprinātu rezultātu Sadalījuma žurnālos pirms grāmatošanas Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="92825-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="92825-118">Laukā Virsgrāmatas grāmatošanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="92825-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="92825-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="92825-119">Click OK.</span></span>
9. <span data-ttu-id="92825-120">Dodieties uz Virsgrāmata > Sadalījumi > Sadalījuma žurnāli.</span><span class="sxs-lookup"><span data-stu-id="92825-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="92825-121">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="92825-121">Click Lines.</span></span>
11. <span data-ttu-id="92825-122">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="92825-122">Click Post.</span></span>
12. <span data-ttu-id="92825-123">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="92825-123">Click Post.</span></span>

