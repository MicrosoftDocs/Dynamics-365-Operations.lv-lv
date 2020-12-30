---
title: Virsgrāmatas sadalījumu žurnāla apstrāde
description: Šajā tēmā ir paskaidrots, kā apstrādāt sadalījuma pieprasījumu pakalpojumā Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33e989d3641ae1eaa28a55398fcf51674ac1ed72
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445615"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="35cf3-103">Virsgrāmatas sadalījumu žurnāla apstrāde</span><span class="sxs-lookup"><span data-stu-id="35cf3-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35cf3-104">Šajā tēmā ir paskaidrots, kā apstrādāt sadalījuma pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="35cf3-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="35cf3-105">Izmantojiet lapu Apstrādāt piešķiršanas pieprasījumu, lai izveidotu sadalījuma žurnālu, ko var pārskatīt un apstiprināt pirms grāmatošanas Virsgrāmatā vai grāmatot tieši Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="35cf3-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="35cf3-106">Pirms varēsiet izveidot sadalījumu žurnālu, jābūt vismaz vienai aktīvai Virsgrāmatas sadalījuma kārtulai.</span><span class="sxs-lookup"><span data-stu-id="35cf3-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="35cf3-107">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="35cf3-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="35cf3-108">Navigācijas rūtī dodieties uz **Moduļi > Virsgrāmata > Sadalījums > Apstrādāt sadalījuma pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="35cf3-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="35cf3-109">Laukā **Noteikums** nolaižamajā sarakstā atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35cf3-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="35cf3-110">Laukā **No datuma** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="35cf3-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="35cf3-111">Lauks **No datuma** ir ļoti svarīgs, ja virsgrāmata ir noteikuma datu avots.</span><span class="sxs-lookup"><span data-stu-id="35cf3-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="35cf3-112">Šis datums kontrolē, kuras Virsgrāmatas bilances iekļaut sadalījumā.</span><span class="sxs-lookup"><span data-stu-id="35cf3-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="35cf3-113">Laukā **Nulles avots** atlasiet **Apturēt**.</span><span class="sxs-lookup"><span data-stu-id="35cf3-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="35cf3-114">Tādējādi tiks apturēts sadalīšanas process un parādīsies ziņojums, kurā teikts, ka ir atlasīts nulles avota apjoms.</span><span class="sxs-lookup"><span data-stu-id="35cf3-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="35cf3-115">Laukā **Priekšlikuma opcijas** atlasiet **Tikai priekšlikums**.</span><span class="sxs-lookup"><span data-stu-id="35cf3-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="35cf3-116">Atlasiet **Tikai priekšlikums**, lai izskatītu un pēc izvēles apstiprinātu rezultātu sadalījuma žurnālos pirms grāmatot sadalījumu virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="35cf3-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="35cf3-117">Laukā Virsgrāmatas grāmatošanas datums ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="35cf3-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="35cf3-118">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="35cf3-118">Select **OK**.</span></span>
7. <span data-ttu-id="35cf3-119">Navigācijas rūtī dodieties uz **Moduļi > Virsgrāmata > Sadalījums > Sadalījuma žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="35cf3-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="35cf3-120">Atlasiet **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="35cf3-120">Select **Lines**.</span></span>
9. <span data-ttu-id="35cf3-121">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="35cf3-121">Select **Post**.</span></span>
10. <span data-ttu-id="35cf3-122">Atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="35cf3-122">Select **Post**.</span></span>

