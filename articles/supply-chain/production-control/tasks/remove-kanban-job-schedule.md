---
title: Kanban darba noņemšana no grafika
description: Šajā procedūrā parādīts, kā noņemt plānoto procesa Kanban darbu no grafika, mainot tā darba statusu uz Nav plānots.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 566a174c631391577441e0f890bd9553dac0891c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204524"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="0951c-103">Kanban darba noņemšana no grafika</span><span class="sxs-lookup"><span data-stu-id="0951c-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0951c-104">Šajā procedūrā parādīts, kā noņemt plānoto procesa Kanban darbu no grafika, mainot tā darba statusu uz Nav plānots.</span><span class="sxs-lookup"><span data-stu-id="0951c-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="0951c-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="0951c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0951c-106">Šī procedūra ir paredzēta ražotnes vadītājam vai ražošanas plānotājam.</span><span class="sxs-lookup"><span data-stu-id="0951c-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="0951c-107">Plānotā Kanban darba atrašana</span><span class="sxs-lookup"><span data-stu-id="0951c-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="0951c-108">Pārejiet uz sadaļu Ražošanas kontrole > Kanban > Kanban darbu plānošana.</span><span class="sxs-lookup"><span data-stu-id="0951c-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="0951c-109">Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0951c-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0951c-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0951c-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0951c-111">Atlasiet darba šūnu 1250.</span><span class="sxs-lookup"><span data-stu-id="0951c-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="0951c-112">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="0951c-112">Click Select.</span></span>
5. <span data-ttu-id="0951c-113">Laukā Rādīt darba statusu atlasiet Plānots.</span><span class="sxs-lookup"><span data-stu-id="0951c-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="0951c-114">Plānota Kanban darba noņemšana no grafika</span><span class="sxs-lookup"><span data-stu-id="0951c-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="0951c-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0951c-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0951c-116">Atlasiet darbu, kura statuss ir Plānots, piemēram, darbu no 2012. gada 19. decembra.</span><span class="sxs-lookup"><span data-stu-id="0951c-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="0951c-117">Darbību rūtī noklikšķiniet uz Plānot.</span><span class="sxs-lookup"><span data-stu-id="0951c-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="0951c-118">Noklikšķiniet uz Atjaunot darba statusu.</span><span class="sxs-lookup"><span data-stu-id="0951c-118">Click Revert job status.</span></span>
4. <span data-ttu-id="0951c-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0951c-119">Click OK.</span></span>
    * <span data-ttu-id="0951c-120">Tas mainīs aktuālo darba statusu no Plānots uz Nav plānots un noņems to no apstrādes ziņojumu dēļa.</span><span class="sxs-lookup"><span data-stu-id="0951c-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]