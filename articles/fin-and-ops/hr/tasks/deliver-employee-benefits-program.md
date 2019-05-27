---
title: Darbinieku atvieglojumu programmas nodrošināšana
description: Šajā uzdevumā jums tiek parādīts, kā izveidot atvieglojumu elementus, kas tiks izmantoti, veidojot jaunus atvieglojumus.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0285c2be49edde701d6c6cf83ccdeac994434ab
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510486"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="b17db-103">Darbinieku atvieglojumu programmas nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="b17db-103">Deliver employee benefits program</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b17db-104">Šajā uzdevumā jums tiek parādīts, kā izveidot atvieglojumu elementus, kas tiks izmantoti, veidojot jaunus atvieglojumus.</span><span class="sxs-lookup"><span data-stu-id="b17db-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="b17db-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="b17db-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="b17db-106">Šis uzdevums ir paredzēts lietotājiem ar lomu Atlīdzību un atvieglojumu vadītājs.</span><span class="sxs-lookup"><span data-stu-id="b17db-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="b17db-107">Izveidot atvieglojumu elementus</span><span class="sxs-lookup"><span data-stu-id="b17db-107">Create benefit elements</span></span>
1. <span data-ttu-id="b17db-108">Šis uzdevums sākas no lapas Atvieglojumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="b17db-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="b17db-109">Sāciet uzdevumu, atverot šo lapu vai meklējot lapu Atvieglojumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="b17db-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="b17db-110">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="b17db-110">Click New.</span></span>
3. <span data-ttu-id="b17db-111">Laukā Tips ierakstiet nosaukumu tam atvieglojumu tipam, kuru veidojat.</span><span class="sxs-lookup"><span data-stu-id="b17db-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="b17db-112">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b17db-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b17db-113">Laukā Vienlaicīga reģistrācija atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="b17db-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="b17db-114">Lai ierobežotu darbinieku spēju reģistrēties vairākos medicīniskajos plānos, atlasiet Viena reģistrācija uz tipu.</span><span class="sxs-lookup"><span data-stu-id="b17db-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="b17db-115">Laukā Algu kategorija atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="b17db-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="b17db-116">Noklikšķiniet uz cilnes Plāni.</span><span class="sxs-lookup"><span data-stu-id="b17db-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="b17db-117">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="b17db-117">Click New.</span></span>
9. <span data-ttu-id="b17db-118">Laukā Plāns ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b17db-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="b17db-119">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b17db-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="b17db-120">Laukā Tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b17db-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="b17db-121">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b17db-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="b17db-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b17db-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b17db-123">Laukā Algas ietekme atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="b17db-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="b17db-124">Noklikšķiniet uz cilnes Opcijas.</span><span class="sxs-lookup"><span data-stu-id="b17db-124">Click the Options tab.</span></span>
16. <span data-ttu-id="b17db-125">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="b17db-125">Click New.</span></span>
17. <span data-ttu-id="b17db-126">Laukā Opcija ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b17db-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="b17db-127">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="b17db-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="b17db-128">Atvieglojuma izveide</span><span class="sxs-lookup"><span data-stu-id="b17db-128">Create a benefit</span></span>
1. <span data-ttu-id="b17db-129">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b17db-129">Close the page.</span></span>
2. <span data-ttu-id="b17db-130">Pārejiet uz sadaļu Personāla vadība > Atvieglojumi > Atvieglojumi.</span><span class="sxs-lookup"><span data-stu-id="b17db-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="b17db-131">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b17db-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="b17db-132">Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b17db-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b17db-133">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b17db-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b17db-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b17db-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b17db-135">Laukā Opcija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b17db-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b17db-136">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b17db-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="b17db-137">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b17db-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b17db-138">Laukā Stājas spēkā ievadiet kādu datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="b17db-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="b17db-139">Noklikšķiniet Izveidot atvieglojumu.</span><span class="sxs-lookup"><span data-stu-id="b17db-139">Click Create benefit.</span></span>
12. <span data-ttu-id="b17db-140">Pārslēdziet sadaļas Algas detalizēta informācija paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="b17db-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="b17db-141">Laukā Biežums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="b17db-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="b17db-142">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b17db-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b17db-143">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b17db-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b17db-144">Laukā Bāze atlasiet kādu opciju.</span><span class="sxs-lookup"><span data-stu-id="b17db-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="b17db-145">Laukā Summa vai likme ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="b17db-145">In the Amount or rate field, enter a number.</span></span>

