---
title: Kanban statusa atjaunināšana
description: Ja kanban tiek iztukšots kļūdas dēļ, vai saņemtu kanban nepieciešams iztukšot, jums ir nepieciešams atjaunināt kanban statusu.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d069414829518c8c952a0e7a74cd0ae4f24c450
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571385"
---
# <a name="update-kanban-status"></a><span data-ttu-id="5faf9-103">Kanban statusa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5faf9-103">Update kanban status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5faf9-104">Ja kanban tiek iztukšots kļūdas dēļ, vai saņemtu kanban nepieciešams iztukšot, jums ir nepieciešams atjaunināt kanban statusu.</span><span class="sxs-lookup"><span data-stu-id="5faf9-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="5faf9-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="5faf9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5faf9-106">Šī procedūra ir paredzēta veikala vadītājam.</span><span class="sxs-lookup"><span data-stu-id="5faf9-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="5faf9-107">Atrast Kanban.</span><span class="sxs-lookup"><span data-stu-id="5faf9-107">Find the kanban.</span></span>
1. <span data-ttu-id="5faf9-108">Doties uz Ražošanas kontrole > Kanban > Kanban.</span><span class="sxs-lookup"><span data-stu-id="5faf9-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="5faf9-109">Atveriet materiālu apstrādes vienības statusa kolonnas filtru.</span><span class="sxs-lookup"><span data-stu-id="5faf9-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="5faf9-110">Noklikšķiniet uz Notīrīt.</span><span class="sxs-lookup"><span data-stu-id="5faf9-110">Click Clear.</span></span>
    * <span data-ttu-id="5faf9-111">Tas atiestata filtrus.</span><span class="sxs-lookup"><span data-stu-id="5faf9-111">This resets the filters.</span></span>  
4. <span data-ttu-id="5faf9-112">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="5faf9-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5faf9-113">Piemēram, filtrējiet pēc lauka Kartes numurs, izmantojot vērtību '000149'.</span><span class="sxs-lookup"><span data-stu-id="5faf9-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="5faf9-114">Mainīt statusu Iztukšots uz statusu Saņemts</span><span class="sxs-lookup"><span data-stu-id="5faf9-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="5faf9-115">Noklikšķiniet uz Atsaukt tukšu materiālu apstrādes vienību.</span><span class="sxs-lookup"><span data-stu-id="5faf9-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="5faf9-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="5faf9-116">Click OK.</span></span>
    * <span data-ttu-id="5faf9-117">Ņemiet vērā, ka materiālu apstrādes vienības statuss ir Saņemts.</span><span class="sxs-lookup"><span data-stu-id="5faf9-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="5faf9-118">Mainīt statusu Saņemts uz statusu Iztukšots</span><span class="sxs-lookup"><span data-stu-id="5faf9-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="5faf9-119">Noklikšķiniet Iztukšot Kanban.</span><span class="sxs-lookup"><span data-stu-id="5faf9-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="5faf9-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="5faf9-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5faf9-121">Ņemiet vērā, ka materiālu apstrādes vienības statuss ir Iztukšots.</span><span class="sxs-lookup"><span data-stu-id="5faf9-121">Notice that the Handling unit status is Emptied.</span></span>  

