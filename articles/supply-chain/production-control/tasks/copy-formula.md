---
title: Formulas kopēšana
description: Šajā procedūrā uzsvars tiek likts uz to, lai izveidotu formulu, kura iekļauj tādus pašus komponentus, kā esošā formula, bet ar nelielām atšķirībām.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26524f886a8af545869bacef4d57bfc14c0ed225
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432505"
---
# <a name="copy-a-formula"></a><span data-ttu-id="356d9-103">Formulas kopēšana</span><span class="sxs-lookup"><span data-stu-id="356d9-103">Copy a formula</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="356d9-104">Šajā procedūrā uzsvars tiek likts uz to, lai izveidotu formulu, kura iekļauj tādus pašus komponentus, kā esošā formula, bet ar nelielām atšķirībām.</span><span class="sxs-lookup"><span data-stu-id="356d9-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="356d9-105">Formulas rindu izveidei var izmantot funkciju Kopēt, lai kopētu esošo formulu, kurai ir visvairāk jums nepieciešamo komponentu.</span><span class="sxs-lookup"><span data-stu-id="356d9-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="356d9-106">Pēc tam var veikt nepieciešamās izmaiņas atsevišķās rindās jaunajā versijā.</span><span class="sxs-lookup"><span data-stu-id="356d9-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="356d9-107">Izmantojot funkciju Kopēt, nav jāizveido vairākas gandrīz identiskas formulas.</span><span class="sxs-lookup"><span data-stu-id="356d9-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="356d9-108">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="356d9-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="356d9-109">Formulas izveide</span><span class="sxs-lookup"><span data-stu-id="356d9-109">Create a formula</span></span>
1. <span data-ttu-id="356d9-110">Pārejiet uz sadaļu Preču informācijas pārvaldība > Materiālu komplekti un formulas > Formulas.</span><span class="sxs-lookup"><span data-stu-id="356d9-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="356d9-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="356d9-111">Click New.</span></span>
3. <span data-ttu-id="356d9-112">Laukā Formula ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="356d9-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="356d9-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="356d9-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="356d9-114">Ierakstiet atpazīstamu formulas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="356d9-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="356d9-115">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="356d9-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="356d9-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="356d9-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="356d9-117">Laukā Krājumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="356d9-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="356d9-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="356d9-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="356d9-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="356d9-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="356d9-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="356d9-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="356d9-121">Formulas rindu kopēšana</span><span class="sxs-lookup"><span data-stu-id="356d9-121">Copy formula lines</span></span>
1. <span data-ttu-id="356d9-122">Darbību rūtī noklikšķiniet uz Formula.</span><span class="sxs-lookup"><span data-stu-id="356d9-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="356d9-123">Noklikšķiniet uz Kopēt.</span><span class="sxs-lookup"><span data-stu-id="356d9-123">Click Copy.</span></span>
3. <span data-ttu-id="356d9-124">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="356d9-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="356d9-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="356d9-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="356d9-126">Laukā Formulas versija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="356d9-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="356d9-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="356d9-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="356d9-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="356d9-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="356d9-129">Kopēto formulas rindu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="356d9-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="356d9-130">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="356d9-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="356d9-131">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="356d9-131">Click Delete.</span></span>
3. <span data-ttu-id="356d9-132">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="356d9-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="356d9-133">Apstiprināt formulu</span><span class="sxs-lookup"><span data-stu-id="356d9-133">Approve formula</span></span>
1. <span data-ttu-id="356d9-134">Darbību rūtī noklikšķiniet uz Formula.</span><span class="sxs-lookup"><span data-stu-id="356d9-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="356d9-135">Noklikšķiniet uz Apstiprināt formulu.</span><span class="sxs-lookup"><span data-stu-id="356d9-135">Click Approve formula.</span></span>
3. <span data-ttu-id="356d9-136">Laukā Apstiprināja noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="356d9-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="356d9-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="356d9-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="356d9-138">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="356d9-138">Click Select.</span></span>
6. <span data-ttu-id="356d9-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="356d9-139">Click OK.</span></span>

