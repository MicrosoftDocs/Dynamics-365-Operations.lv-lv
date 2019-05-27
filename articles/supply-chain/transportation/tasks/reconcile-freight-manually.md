---
title: Manuāla kravas saskaņošana
description: Šajā procedūrā parādīts kā saskaņot kravu manuāli.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee2d114b0a725b947add3e155cc6445021fee998
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556738"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="450ed-103">Manuāla kravas saskaņošana</span><span class="sxs-lookup"><span data-stu-id="450ed-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="450ed-104">Šajā procedūrā parādīts kā saskaņot kravu manuāli.</span><span class="sxs-lookup"><span data-stu-id="450ed-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="450ed-105">To parasti veic transportēšanas koordinators.</span><span class="sxs-lookup"><span data-stu-id="450ed-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="450ed-106">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="450ed-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="450ed-107">Atlasiet kravu saskaņošanai</span><span class="sxs-lookup"><span data-stu-id="450ed-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="450ed-108">Dodieties uz Transportēšanas pārvaldība > Plānošana > Kravu plānošanas rīks.</span><span class="sxs-lookup"><span data-stu-id="450ed-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="450ed-109">Noņemiet atzīmi izvēles rūtiņai Slēpt nosūtītos un saņemtos.</span><span class="sxs-lookup"><span data-stu-id="450ed-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="450ed-110">Sarakstā atlasiet kravu ar kravas ID 00006.</span><span class="sxs-lookup"><span data-stu-id="450ed-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="450ed-111">Izveidot pārvadātāja rēķinu</span><span class="sxs-lookup"><span data-stu-id="450ed-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="450ed-112">Ja saskaņojat kravu manuāli un nesaņemat pārvadātāja rēķinu automātiski, jūs varat izveidot rēķinu, izmantojot kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="450ed-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="450ed-113">Noklikšķiniet uz Saistītā informācija.</span><span class="sxs-lookup"><span data-stu-id="450ed-113">Click Related information.</span></span>
2. <span data-ttu-id="450ed-114">Noklikšķiniet uz Kravas pavadzīmes dati.</span><span class="sxs-lookup"><span data-stu-id="450ed-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="450ed-115">Noklikšķiniet uz Ģenerēt kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="450ed-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="450ed-116">Laukā Rēķins ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="450ed-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="450ed-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="450ed-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="450ed-118">Saskaņot rēķinu</span><span class="sxs-lookup"><span data-stu-id="450ed-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="450ed-119">Saskaņojot pārvadātāja rēķinu un kravas pavadzīmi, tas jāveic rindu pa rindai.</span><span class="sxs-lookup"><span data-stu-id="450ed-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="450ed-120">Noklikšķiniet uz Saskaņot kravas pavadzīmes un rēķinus.</span><span class="sxs-lookup"><span data-stu-id="450ed-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="450ed-121">Izvērsiet sadaļu Rēķina informācija.</span><span class="sxs-lookup"><span data-stu-id="450ed-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="450ed-122">Izvērsiet sadaļu Detalizēta informācija par nesaskaņoto kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="450ed-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="450ed-123">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="450ed-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="450ed-124">Noklikšķiniet uz Saskaņot.</span><span class="sxs-lookup"><span data-stu-id="450ed-124">Click Match.</span></span>
6. <span data-ttu-id="450ed-125">Izvērsiet sadaļu Detalizēta informācija par saskaņoto kravas pavadzīmi</span><span class="sxs-lookup"><span data-stu-id="450ed-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="450ed-126">Iesniegt rēķinu apstiprināšanai</span><span class="sxs-lookup"><span data-stu-id="450ed-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="450ed-127">Noklikšķiniet uz Iesniegt apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="450ed-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="450ed-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="450ed-128">Close the page.</span></span>
3. <span data-ttu-id="450ed-129">Noņemiet atzīmi izvēles rūtiņai Paslēpt apstiprināto.</span><span class="sxs-lookup"><span data-stu-id="450ed-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="450ed-130">Noklikšķiniet uz Kreditoru rēķinu žurnāli.</span><span class="sxs-lookup"><span data-stu-id="450ed-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="450ed-131">Noklikšķiniet, lai sekotu saitei laukā Atsauces žurnāla numurs.</span><span class="sxs-lookup"><span data-stu-id="450ed-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="450ed-132">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="450ed-132">Click Lines.</span></span>

