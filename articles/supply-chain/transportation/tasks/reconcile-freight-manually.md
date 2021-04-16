---
title: Manuāla kravas saskaņošana
description: Šajā procedūrā parādīts kā saskaņot kravu manuāli.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a0a5450697a09e5e54e74b35b2576eb6bbd4cdf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838518"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="72c46-103">Manuāla kravas saskaņošana</span><span class="sxs-lookup"><span data-stu-id="72c46-103">Reconcile freight manually</span></span>

<span data-ttu-id="72c46-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="72c46-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="72c46-105">Šajā procedūrā parādīts kā saskaņot kravu manuāli.</span><span class="sxs-lookup"><span data-stu-id="72c46-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="72c46-106">To parasti veic transportēšanas koordinators.</span><span class="sxs-lookup"><span data-stu-id="72c46-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="72c46-107">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="72c46-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="72c46-108">Atlasiet kravu saskaņošanai</span><span class="sxs-lookup"><span data-stu-id="72c46-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="72c46-109">Dodieties uz Transportēšanas pārvaldība > Plānošana > Kravu plānošanas rīks.</span><span class="sxs-lookup"><span data-stu-id="72c46-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="72c46-110">Noņemiet atzīmi izvēles rūtiņai Slēpt nosūtītos un saņemtos.</span><span class="sxs-lookup"><span data-stu-id="72c46-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="72c46-111">Sarakstā atlasiet kravu ar kravas ID 00006.</span><span class="sxs-lookup"><span data-stu-id="72c46-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="72c46-112">Izveidot pārvadātāja rēķinu</span><span class="sxs-lookup"><span data-stu-id="72c46-112">Create a carrier invoice</span></span>
<span data-ttu-id="72c46-113">Ja saskaņojat kravu manuāli un nesaņemat pārvadātāja rēķinu automātiski, jūs varat izveidot rēķinu, izmantojot kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="72c46-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="72c46-114">Noklikšķiniet uz Saistītā informācija.</span><span class="sxs-lookup"><span data-stu-id="72c46-114">Click Related information.</span></span>
2. <span data-ttu-id="72c46-115">Noklikšķiniet uz Kravas pavadzīmes dati.</span><span class="sxs-lookup"><span data-stu-id="72c46-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="72c46-116">Noklikšķiniet uz Ģenerēt kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="72c46-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="72c46-117">Laukā Rēķins ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="72c46-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="72c46-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="72c46-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="72c46-119">Saskaņot rēķinu</span><span class="sxs-lookup"><span data-stu-id="72c46-119">Reconcile the invoice</span></span>
<span data-ttu-id="72c46-120">Saskaņojot pārvadātāja rēķinu un kravas pavadzīmi, tas jāveic rindu pa rindai.</span><span class="sxs-lookup"><span data-stu-id="72c46-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="72c46-121">Noklikšķiniet uz Saskaņot kravas pavadzīmes un rēķinus.</span><span class="sxs-lookup"><span data-stu-id="72c46-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="72c46-122">Izvērsiet sadaļu Rēķina informācija.</span><span class="sxs-lookup"><span data-stu-id="72c46-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="72c46-123">Izvērsiet sadaļu Detalizēta informācija par nesaskaņoto kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="72c46-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="72c46-124">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="72c46-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="72c46-125">Noklikšķiniet uz Saskaņot.</span><span class="sxs-lookup"><span data-stu-id="72c46-125">Click Match.</span></span>
6. <span data-ttu-id="72c46-126">Izvērsiet sadaļu Detalizēta informācija par saskaņoto kravas pavadzīmi</span><span class="sxs-lookup"><span data-stu-id="72c46-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="72c46-127">Iesniegt rēķinu apstiprināšanai</span><span class="sxs-lookup"><span data-stu-id="72c46-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="72c46-128">Noklikšķiniet uz Iesniegt apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="72c46-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="72c46-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="72c46-129">Close the page.</span></span>
3. <span data-ttu-id="72c46-130">Noņemiet atzīmi izvēles rūtiņai Paslēpt apstiprināto.</span><span class="sxs-lookup"><span data-stu-id="72c46-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="72c46-131">Noklikšķiniet uz Kreditoru rēķinu žurnāli.</span><span class="sxs-lookup"><span data-stu-id="72c46-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="72c46-132">Noklikšķiniet, lai sekotu saitei laukā Atsauces žurnāla numurs.</span><span class="sxs-lookup"><span data-stu-id="72c46-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="72c46-133">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="72c46-133">Click Lines.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]