---
title: Kanban daudzuma aprēķināšanas ierobežojuma pievienošana Kanban kārtulai
description: Šajā procedūrā parādīts, kā izveidot Kanban daudzuma aprēķināšanas politiku un pievienot Kanban nosacījumu, lai optimizētu Kanban lielumu un daudzumus.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93f0c2024e7fbe7d9c6525d41207b788032e763a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147208"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="60661-103">Kanban daudzuma aprēķināšanas ierobežojuma pievienošana Kanban kārtulai</span><span class="sxs-lookup"><span data-stu-id="60661-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60661-104">Šajā procedūrā parādīts, kā izveidot Kanban daudzuma aprēķināšanas politiku un pievienot Kanban nosacījumu, lai optimizētu Kanban lielumu un daudzumus.</span><span class="sxs-lookup"><span data-stu-id="60661-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="60661-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="60661-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="60661-106">Šī procedūra ir paredzēta vērtību plūsmas pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="60661-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="60661-107">Šī procedūra ir nepieciešama, lai izveidotu procedūru Aprēķināt Kanban daudzuma ieteikumus.</span><span class="sxs-lookup"><span data-stu-id="60661-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="60661-108">Kanban daudzuma aprēķina politikas izveide</span><span class="sxs-lookup"><span data-stu-id="60661-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="60661-109">Pārejiet uz sadaļu Ražošanas kontrole > Periodiskie uzdevumi > Kanban daudzuma aprēķins > Kanban daudzuma aprēķinu politikas.</span><span class="sxs-lookup"><span data-stu-id="60661-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="60661-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="60661-110">Click New.</span></span>
3. <span data-ttu-id="60661-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="60661-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="60661-112">Piemēram, ierakstiet Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="60661-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="60661-113">Laukā Vispārējais plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="60661-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="60661-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="60661-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="60661-115">Atlasiet StaticPlan, lai aprēķinātu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="60661-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="60661-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="60661-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="60661-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="60661-117">Click Save.</span></span>
8. <span data-ttu-id="60661-118">Laukā Minimālais Kanban daudzums ievadiet "1".</span><span class="sxs-lookup"><span data-stu-id="60661-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="60661-119">Šis ir Kanban papildu skaits, ko lieto Kanban daudzuma aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="60661-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="60661-120">Iestatiet vērtību "1" laukā Drošības koeficients.</span><span class="sxs-lookup"><span data-stu-id="60661-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="60661-121">Šis ir faktors, kas tiek izmantots, lai aprēķinātu papildu drošības krājumu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="60661-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="60661-122">Laukā Dienas uz priekšu ievadiet “30”.</span><span class="sxs-lookup"><span data-stu-id="60661-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="60661-123">Šis ir dienu skaits pirms Kanban daudzuma aprēķināšanas datuma, kas iekļauts pieprasījuma aprēķināšanā.</span><span class="sxs-lookup"><span data-stu-id="60661-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="60661-124">Laukā Dienas aiz muguras ievadiet “30”.</span><span class="sxs-lookup"><span data-stu-id="60661-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="60661-125">Šis ir dienu skaits uz priekšu, skaitot no Kanban daudzuma aprēķināšanas datuma, kas iekļauts pieprasījuma aprēķināšanā.</span><span class="sxs-lookup"><span data-stu-id="60661-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="60661-126">Aprēķināšanai izmantotā formula ir redzama ar faktiskajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="60661-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="60661-127">Piemēram, Kanban daudzums = ((vidējais dienas pieprasījums x izpildes laiks x 2) / preču daudzums uz materiālu apstrādes vienību) + 1</span><span class="sxs-lookup"><span data-stu-id="60661-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="60661-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="60661-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="60661-129">Kanban daudzuma aprēķināšanas politikas pievienošana Kanban nosacījumam</span><span class="sxs-lookup"><span data-stu-id="60661-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="60661-130">Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="60661-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="60661-131">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="60661-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="60661-132">Šai procedūrai atlasiet Kanban nosacījumu 000020.</span><span class="sxs-lookup"><span data-stu-id="60661-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="60661-133">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="60661-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="60661-134">Pārslēdziet sadaļas Kanban daudzuma aprēķinu politikas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="60661-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="60661-135">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="60661-135">Click Add.</span></span>
    * <span data-ttu-id="60661-136">Pievienojiet Kanban daudzuma aprēķināšanas politiku, kuru izveidojāt iepriekšējā apakšuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="60661-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="60661-137">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="60661-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="60661-138">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="60661-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="60661-139">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="60661-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="60661-140">Atlasiet politiku Speaker2016, kuru izveidojāt iepriekšējā apakšuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="60661-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

