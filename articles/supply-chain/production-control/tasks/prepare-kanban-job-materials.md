---
title: "Procesa sagatavošana Kanban darbam, kad materiāli ir pieejami darba šūnai"
description: "Šajā uzdevumā parādīts, ka sagatavot procesa Kanban darbu, kad visi darba šūnas materiāli ir pieejami."
author: johanhoffmann
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
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: fdedab1bfccafb4f8592aea8ec421e3ba311a94a
ms.contentlocale: lv-lv
ms.lasthandoff: 02/06/2018

---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="d4b97-103">Procesa sagatavošana Kanban darbam, kad materiāli ir pieejami darba šūnai</span><span class="sxs-lookup"><span data-stu-id="d4b97-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4b97-104">Šajā uzdevumā parādīts, ka sagatavot procesa Kanban darbu, kad visi darba šūnas materiāli ir pieejami.</span><span class="sxs-lookup"><span data-stu-id="d4b97-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="d4b97-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="d4b97-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="d4b97-106">Šis uzdevums ir paredzēts mašīnas operatoram.</span><span class="sxs-lookup"><span data-stu-id="d4b97-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="d4b97-107">Dodieties uz procesa darbu Kanban paneli.</span><span class="sxs-lookup"><span data-stu-id="d4b97-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="d4b97-108">Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4b97-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d4b97-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4b97-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d4b97-110">Atlasiet darba šūnu 1250 un noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="d4b97-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="d4b97-111">Sarakstā atlasiet 4. rindu.</span><span class="sxs-lookup"><span data-stu-id="d4b97-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="d4b97-112">Tukšā demonstrācijas uzņēmumā Kanban 000329 pirmais vēl nepabeigtais darbs ir 4. rindā.</span><span class="sxs-lookup"><span data-stu-id="d4b97-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="d4b97-113">Pārslēdziet sadaļas Izdošanas saraksts paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="d4b97-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="d4b97-114">Pārliecinieties, ka visiem izdošanas saraksta krājumiem piegādes statuss ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="d4b97-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="d4b97-115">Ja tiek atlasīti vairāki darbi, izdošanas saraksts parāda summāru kopsavilkumu par visiem krājumiem, kas nepieciešami atlasītajiem darbiem.</span><span class="sxs-lookup"><span data-stu-id="d4b97-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="d4b97-116">Noklikšķiniet uz Sagatavot.</span><span class="sxs-lookup"><span data-stu-id="d4b97-116">Click Prepare.</span></span>
    * <span data-ttu-id="d4b97-117">Sagatavošanas process ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="d4b97-117">The preparation process is now completed.</span></span> <span data-ttu-id="d4b97-118">Izvēles rūtiņa ar atzīmi visām izdošanas saraksta rindām norāda, tiek piegādes statuss ir Izdots.</span><span class="sxs-lookup"><span data-stu-id="d4b97-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

