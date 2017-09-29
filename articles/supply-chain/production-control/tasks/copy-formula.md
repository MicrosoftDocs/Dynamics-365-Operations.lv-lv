--- 
title: "Formulas kopēšana"
description: "Šajā procedūrā uzsvars tiek likts uz to, lai izveidotu formulu, kura iekļauj tādus pašus komponentus, kā esošā formula, bet ar nelielām atšķirībām."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 036bd9f592ca584afad9d4b9b7a49a9787076056
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="copy-a-formula"></a><span data-ttu-id="1c3df-103">Formulas kopēšana</span><span class="sxs-lookup"><span data-stu-id="1c3df-103">Copy a formula</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c3df-104">Šajā procedūrā uzsvars tiek likts uz to, lai izveidotu formulu, kura iekļauj tādus pašus komponentus, kā esošā formula, bet ar nelielām atšķirībām.</span><span class="sxs-lookup"><span data-stu-id="1c3df-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="1c3df-105">Formulas rindu izveidei var izmantot funkciju Kopēt, lai kopētu esošo formulu, kurai ir visvairāk jums nepieciešamo komponentu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="1c3df-106">Pēc tam var veikt nepieciešamās izmaiņas atsevišķās rindās jaunajā versijā.</span><span class="sxs-lookup"><span data-stu-id="1c3df-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="1c3df-107">Izmantojot funkciju Kopēt, nav jāizveido vairākas gandrīz identiskas formulas.</span><span class="sxs-lookup"><span data-stu-id="1c3df-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="1c3df-108">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USP2.</span><span class="sxs-lookup"><span data-stu-id="1c3df-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="1c3df-109">Formulas izveide</span><span class="sxs-lookup"><span data-stu-id="1c3df-109">Create a formula</span></span>
1. <span data-ttu-id="1c3df-110">Pārejiet uz sadaļu Preču informācijas pārvaldība > Materiālu komplekti un formulas > Formulas.</span><span class="sxs-lookup"><span data-stu-id="1c3df-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="1c3df-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1c3df-111">Click New.</span></span>
3. <span data-ttu-id="1c3df-112">Laukā Formula ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1c3df-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="1c3df-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1c3df-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="1c3df-114">Ierakstiet atpazīstamu formulas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="1c3df-115">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1c3df-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1c3df-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="1c3df-117">Laukā Krājumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1c3df-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="1c3df-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1c3df-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="1c3df-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1c3df-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="1c3df-121">Formulas rindu kopēšana</span><span class="sxs-lookup"><span data-stu-id="1c3df-121">Copy formula lines</span></span>
1. <span data-ttu-id="1c3df-122">Darbību rūtī noklikšķiniet uz Formula.</span><span class="sxs-lookup"><span data-stu-id="1c3df-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="1c3df-123">Noklikšķiniet uz Kopēt.</span><span class="sxs-lookup"><span data-stu-id="1c3df-123">Click Copy.</span></span>
3. <span data-ttu-id="1c3df-124">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1c3df-125">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1c3df-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1c3df-126">Laukā Formulas versija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="1c3df-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1c3df-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="1c3df-128">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1c3df-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="1c3df-129">Kopēto formulas rindu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="1c3df-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="1c3df-130">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="1c3df-131">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="1c3df-131">Click Delete.</span></span>
3. <span data-ttu-id="1c3df-132">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="1c3df-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="1c3df-133">Apstiprināt formulu</span><span class="sxs-lookup"><span data-stu-id="1c3df-133">Approve formula</span></span>
1. <span data-ttu-id="1c3df-134">Darbību rūtī noklikšķiniet uz Formula.</span><span class="sxs-lookup"><span data-stu-id="1c3df-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="1c3df-135">Noklikšķiniet uz Apstiprināt formulu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-135">Click Approve formula.</span></span>
3. <span data-ttu-id="1c3df-136">Laukā Apstiprināja noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1c3df-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1c3df-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1c3df-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1c3df-138">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="1c3df-138">Click Select.</span></span>
6. <span data-ttu-id="1c3df-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="1c3df-139">Click OK.</span></span>


