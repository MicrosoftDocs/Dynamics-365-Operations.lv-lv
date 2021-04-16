---
title: Procesa sagatavošana Kanban darbam, kad materiāli ir pieejami darba šūnai
description: Šajā uzdevumā parādīts, ka sagatavot procesa Kanban darbu, kad visi darba šūnas materiāli ir pieejami.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 460d55a8c4b8a8401db7abc43721cf0d114c27c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807828"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="cfa8f-103">Procesa sagatavošana Kanban darbam, kad materiāli ir pieejami darba šūnai</span><span class="sxs-lookup"><span data-stu-id="cfa8f-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cfa8f-104">Šajā uzdevumā parādīts, ka sagatavot procesa Kanban darbu, kad visi darba šūnas materiāli ir pieejami.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="cfa8f-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="cfa8f-106">Šis uzdevums ir paredzēts mašīnas operatoram.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="cfa8f-107">Dodieties uz procesa darbu Kanban paneli.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="cfa8f-108">Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cfa8f-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cfa8f-110">Atlasiet darba šūnu 1250 un noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="cfa8f-111">Sarakstā atlasiet 4. rindu.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="cfa8f-112">Tukšā demonstrācijas uzņēmumā Kanban 000329 pirmais vēl nepabeigtais darbs ir 4. rindā.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="cfa8f-113">Pārslēdziet sadaļas Izdošanas saraksts paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="cfa8f-114">Pārliecinieties, ka visiem izdošanas saraksta krājumiem piegādes statuss ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="cfa8f-115">Ja tiek atlasīti vairāki darbi, izdošanas saraksts parāda summāru kopsavilkumu par visiem krājumiem, kas nepieciešami atlasītajiem darbiem.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="cfa8f-116">Noklikšķiniet uz Sagatavot.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-116">Click Prepare.</span></span>
    * <span data-ttu-id="cfa8f-117">Sagatavošanas process ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-117">The preparation process is now completed.</span></span> <span data-ttu-id="cfa8f-118">Izvēles rūtiņa ar atzīmi visām izdošanas saraksta rindām norāda, tiek piegādes statuss ir Izdots.</span><span class="sxs-lookup"><span data-stu-id="cfa8f-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]