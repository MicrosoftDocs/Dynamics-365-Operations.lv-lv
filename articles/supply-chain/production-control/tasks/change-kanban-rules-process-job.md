---
title: Procesa darba Kanban kārtulu maiņa
description: Šajā procedūrā aprakstīts konkrētajam Kanban izmantoto Kanban nosacījum maiņa.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e0e1989bcc4ca02d097f9ebff40f21158f26546
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981360"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="7a620-103">Procesa darba Kanban kārtulu maiņa</span><span class="sxs-lookup"><span data-stu-id="7a620-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a620-104">Šajā procedūrā aprakstīts konkrētajam Kanban izmantoto Kanban nosacījum maiņa.</span><span class="sxs-lookup"><span data-stu-id="7a620-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="7a620-105">Tas ir noderīgi noslodzes resursu līmeņu piešķiršanā vai sadalījumā.</span><span class="sxs-lookup"><span data-stu-id="7a620-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="7a620-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="7a620-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7a620-107">Šī procedūra ir paredzēta plānotājam, kas strādā lean manufacturing uzņēmumā un ir atbildīgs par vērtību plūsmu.</span><span class="sxs-lookup"><span data-stu-id="7a620-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="7a620-108">Kanban nosacījumu kopēšana</span><span class="sxs-lookup"><span data-stu-id="7a620-108">Copy kanban rule</span></span>
1. <span data-ttu-id="7a620-109">Dodieties uz Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="7a620-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="7a620-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="7a620-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7a620-111">Vienumam L0001 atlasiet Notikumu Kanban nosacījumi 000022.</span><span class="sxs-lookup"><span data-stu-id="7a620-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="7a620-112">Noklikšķiniet uz Dublējiet Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="7a620-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="7a620-113">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="7a620-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="7a620-114">Kanban nosacījumu mainīšana</span><span class="sxs-lookup"><span data-stu-id="7a620-114">Change kanban rule</span></span>
1. <span data-ttu-id="7a620-115">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="7a620-115">Close the page.</span></span>
2. <span data-ttu-id="7a620-116">Dodieties uz cilni Kanban darbu plānošana.</span><span class="sxs-lookup"><span data-stu-id="7a620-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="7a620-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="7a620-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7a620-118">Izvēlieties rindu ar Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="7a620-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="7a620-119">Noklikšķiniet uz Izmantot alternatīvus Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="7a620-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="7a620-120">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="7a620-120">Click Next.</span></span>
6. <span data-ttu-id="7a620-121">Laukā Kanban nosacījumi ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="7a620-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="7a620-122">Atlasiet Kanban nosacījumus, kas tika izveidoti iepriekš.</span><span class="sxs-lookup"><span data-stu-id="7a620-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="7a620-123">Šie ir kanban nosacījumi ar lielāko numuru.</span><span class="sxs-lookup"><span data-stu-id="7a620-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="7a620-124">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="7a620-124">Click Finish.</span></span>
    * <span data-ttu-id="7a620-125">Tagad Kanban darbs izmanto citus Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="7a620-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="7a620-126">Tas var noderēt darba šūnu noslodzes līmeņu piešķiršanā.</span><span class="sxs-lookup"><span data-stu-id="7a620-126">This can be useful to level load work cells.</span></span>  

