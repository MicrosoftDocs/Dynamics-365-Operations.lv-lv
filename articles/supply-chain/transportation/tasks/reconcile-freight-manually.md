--- 
title: "Manuāla kravas saskaņošana"
description: "Šajā procedūrā parādīts kā saskaņot kravu manuāli."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="eb64a-103">Manuāla kravas saskaņošana</span><span class="sxs-lookup"><span data-stu-id="eb64a-103">Reconcile freight manually</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb64a-104">Šajā procedūrā parādīts kā saskaņot kravu manuāli.</span><span class="sxs-lookup"><span data-stu-id="eb64a-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="eb64a-105">To parasti veic transportēšanas koordinators.</span><span class="sxs-lookup"><span data-stu-id="eb64a-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="eb64a-106">Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="eb64a-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="eb64a-107">Atlasiet kravu saskaņošanai</span><span class="sxs-lookup"><span data-stu-id="eb64a-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="eb64a-108">Dodieties uz Transportēšanas pārvaldība > Plānošana > Kravu plānošanas rīks.</span><span class="sxs-lookup"><span data-stu-id="eb64a-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="eb64a-109">Noņemiet atzīmi izvēles rūtiņai Slēpt nosūtītos un saņemtos.</span><span class="sxs-lookup"><span data-stu-id="eb64a-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="eb64a-110">Sarakstā atlasiet kravu ar kravas ID 00006.</span><span class="sxs-lookup"><span data-stu-id="eb64a-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="eb64a-111">Izveidot pārvadātāja rēķinu</span><span class="sxs-lookup"><span data-stu-id="eb64a-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="eb64a-112">Ja saskaņojat kravu manuāli un nesaņemat pārvadātāja rēķinu automātiski, jūs varat izveidot rēķinu, izmantojot kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="eb64a-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="eb64a-113">Noklikšķiniet uz Saistītā informācija.</span><span class="sxs-lookup"><span data-stu-id="eb64a-113">Click Related information.</span></span>
2. <span data-ttu-id="eb64a-114">Noklikšķiniet uz Kravas pavadzīmes dati.</span><span class="sxs-lookup"><span data-stu-id="eb64a-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="eb64a-115">Noklikšķiniet uz Ģenerēt kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="eb64a-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="eb64a-116">Laukā Rēķins ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="eb64a-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="eb64a-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="eb64a-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="eb64a-118">Saskaņot rēķinu</span><span class="sxs-lookup"><span data-stu-id="eb64a-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="eb64a-119">Saskaņojot pārvadātāja rēķinu un kravas pavadzīmi, tas jāveic rindu pa rindai.</span><span class="sxs-lookup"><span data-stu-id="eb64a-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="eb64a-120">Noklikšķiniet uz Saskaņot kravas pavadzīmes un rēķinus.</span><span class="sxs-lookup"><span data-stu-id="eb64a-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="eb64a-121">Izvērsiet sadaļu Rēķina informācija.</span><span class="sxs-lookup"><span data-stu-id="eb64a-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="eb64a-122">Izvērsiet sadaļu Detalizēta informācija par nesaskaņoto kravas pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="eb64a-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="eb64a-123">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="eb64a-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="eb64a-124">Noklikšķiniet uz Saskaņot.</span><span class="sxs-lookup"><span data-stu-id="eb64a-124">Click Match.</span></span>
6. <span data-ttu-id="eb64a-125">Izvērsiet sadaļu Detalizēta informācija par saskaņoto kravas pavadzīmi</span><span class="sxs-lookup"><span data-stu-id="eb64a-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="eb64a-126">Iesniegt rēķinu apstiprināšanai</span><span class="sxs-lookup"><span data-stu-id="eb64a-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="eb64a-127">Noklikšķiniet uz Iesniegt apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="eb64a-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="eb64a-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="eb64a-128">Close the page.</span></span>
3. <span data-ttu-id="eb64a-129">Noņemiet atzīmi izvēles rūtiņai Paslēpt apstiprināto.</span><span class="sxs-lookup"><span data-stu-id="eb64a-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="eb64a-130">Noklikšķiniet uz Kreditoru rēķinu žurnāli.</span><span class="sxs-lookup"><span data-stu-id="eb64a-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="eb64a-131">Noklikšķiniet, lai sekotu saitei laukā Atsauces žurnāla numurs.</span><span class="sxs-lookup"><span data-stu-id="eb64a-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="eb64a-132">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="eb64a-132">Click Lines.</span></span>


