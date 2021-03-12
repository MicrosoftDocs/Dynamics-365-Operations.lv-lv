---
title: Procesa sagatavošana Kanban darbam, kad materiāli nav pieejami darba šūnai
description: Šajā procedūrā parādīts, kā sagatavot procesa Kanban darbu, kad darba šūnai nav pieejami daži no nepieciešamajiem materiāliem un tādēļ ir nepieciešams atlasīt materiālus no noliktavas.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df0396a1d00e61ad82e52fc07779e239cd811ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994095"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="98fc9-103">Procesa sagatavošana Kanban darbam, kad materiāli nav pieejami darba šūnai</span><span class="sxs-lookup"><span data-stu-id="98fc9-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98fc9-104">Šajā procedūrā parādīts, kā sagatavot procesa Kanban darbu, kad darba šūnai nav pieejami daži no nepieciešamajiem materiāliem un tādēļ ir nepieciešams atlasīt materiālus no noliktavas.</span><span class="sxs-lookup"><span data-stu-id="98fc9-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="98fc9-105">Šīs procedūras izveides priekšnosacījums ir procedūra "Sagatavot procesa Kanban darbu, kad materiāli ir pieejami".</span><span class="sxs-lookup"><span data-stu-id="98fc9-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="98fc9-106">Šī procedūra ir paredzēta mašīnas operatoram.</span><span class="sxs-lookup"><span data-stu-id="98fc9-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="98fc9-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="98fc9-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="98fc9-108">Pārejiet uz sadaļu Ražošanas kontrole > Kanban > Kanban panelis procesa darbiem.</span><span class="sxs-lookup"><span data-stu-id="98fc9-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="98fc9-109">Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="98fc9-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="98fc9-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="98fc9-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98fc9-111">Atlasiet darba šūnu 1250.</span><span class="sxs-lookup"><span data-stu-id="98fc9-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="98fc9-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="98fc9-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="98fc9-113">Atlasiet Kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="98fc9-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="98fc9-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="98fc9-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="98fc9-115">Sarakstā noņemiet atzīmi no 4. rindas izvēles rūtiņas.</span><span class="sxs-lookup"><span data-stu-id="98fc9-115">In the list, deselect row 4.</span></span> <span data-ttu-id="98fc9-116">vai atlasiet 4. rindu, ja neesat izpildījis uzdevumu "Procesa Kanban darba sagatavošana, kad materiāli ir pieejami."</span><span class="sxs-lookup"><span data-stu-id="98fc9-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="98fc9-117">Pārslēdziet sadaļas Izdošanas saraksts paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="98fc9-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="98fc9-118">Piegādes statusā attēlotā ikona Nav ierakstu norāda, ka darba šūnā krājumam P0002 trūkst 48 vienumi.</span><span class="sxs-lookup"><span data-stu-id="98fc9-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="98fc9-119">Materiālu pārsūtīšana uz darba šūnu</span><span class="sxs-lookup"><span data-stu-id="98fc9-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="98fc9-120">Pārslēdziet sadaļas Pārvietošanas darbi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="98fc9-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="98fc9-121">Izmantojiet ātro filtru, lai Krājuma numura laukā filtrētu pēc vērtības P0002.</span><span class="sxs-lookup"><span data-stu-id="98fc9-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="98fc9-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="98fc9-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="98fc9-123">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="98fc9-123">Click Start.</span></span>
    * <span data-ttu-id="98fc9-124">Tiek veikta pārsūtīšana.</span><span class="sxs-lookup"><span data-stu-id="98fc9-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="98fc9-125">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="98fc9-125">Click Complete.</span></span>
    * <span data-ttu-id="98fc9-126">Krājums P0002 tagad ir pieejams Kanban darba izdošanas sarakstā.</span><span class="sxs-lookup"><span data-stu-id="98fc9-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="98fc9-127">Tas nozīmē, ka varat sagatavot Kanban ar visiem nepieciešamajiem materiāliem.</span><span class="sxs-lookup"><span data-stu-id="98fc9-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="98fc9-128">Noklikšķiniet uz Sagatavot.</span><span class="sxs-lookup"><span data-stu-id="98fc9-128">Click Prepare.</span></span>
    * <span data-ttu-id="98fc9-129">Ņemiet vērā, ka ikona Darba statusa laukā norāda, ka darbs ir gatavs.</span><span class="sxs-lookup"><span data-stu-id="98fc9-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

