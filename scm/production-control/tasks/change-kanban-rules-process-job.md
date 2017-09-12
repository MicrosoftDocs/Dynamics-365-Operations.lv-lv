--- 
title: "Procesa darba Kanban kārtulu maiņa"
description: "Šajā procedūrā aprakstīts konkrētajam Kanban izmantoto Kanban nosacījum maiņa."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="18d26-103">Procesa darba Kanban kārtulu maiņa</span><span class="sxs-lookup"><span data-stu-id="18d26-103">Change kanban rules for a process job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18d26-104">Šajā procedūrā aprakstīts konkrētajam Kanban izmantoto Kanban nosacījum maiņa.</span><span class="sxs-lookup"><span data-stu-id="18d26-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="18d26-105">Tas ir noderīgi noslodzes resursu līmeņu piešķiršanā vai sadalījumā.</span><span class="sxs-lookup"><span data-stu-id="18d26-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="18d26-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="18d26-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="18d26-107">Šī procedūra ir paredzēta plānotājam, kas strādā lean manufacturing uzņēmumā un ir atbildīgs par vērtību plūsmu.</span><span class="sxs-lookup"><span data-stu-id="18d26-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="18d26-108">Kanban nosacījumu kopēšana</span><span class="sxs-lookup"><span data-stu-id="18d26-108">Copy kanban rule</span></span>
1. <span data-ttu-id="18d26-109">Dodieties uz Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="18d26-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="18d26-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="18d26-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="18d26-111">Vienumam L0001 atlasiet Notikumu Kanban nosacījumi 000022.</span><span class="sxs-lookup"><span data-stu-id="18d26-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="18d26-112">Noklikšķiniet uz Dublējiet Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="18d26-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="18d26-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="18d26-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="18d26-114">Kanban nosacījumu mainīšana</span><span class="sxs-lookup"><span data-stu-id="18d26-114">Change kanban rule</span></span>
1. <span data-ttu-id="18d26-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="18d26-115">Close the page.</span></span>
2. <span data-ttu-id="18d26-116">Dodieties uz cilni Kanban darbu plānošana.</span><span class="sxs-lookup"><span data-stu-id="18d26-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="18d26-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="18d26-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="18d26-118">Izvēlieties rindu ar Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="18d26-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="18d26-119">Noklikšķiniet uz Izmantot alternatīvus Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="18d26-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="18d26-120">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="18d26-120">Click Next.</span></span>
6. <span data-ttu-id="18d26-121">Laukā Kanban nosacījumi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="18d26-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="18d26-122">Atlasiet Kanban nosacījumus, kas tika izveidoti iepriekš.</span><span class="sxs-lookup"><span data-stu-id="18d26-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="18d26-123">Šie ir kanban nosacījumi ar lielāko numuru.</span><span class="sxs-lookup"><span data-stu-id="18d26-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="18d26-124">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="18d26-124">Click Finish.</span></span>
    * <span data-ttu-id="18d26-125">Tagad Kanban darbs izmanto citus Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="18d26-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="18d26-126">Tas var noderēt darba šūnu noslodzes līmeņu piešķiršanā.</span><span class="sxs-lookup"><span data-stu-id="18d26-126">This can be useful to level load work cells.</span></span>  


