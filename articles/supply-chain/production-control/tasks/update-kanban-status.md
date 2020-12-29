---
title: Kanban statusa atjaunināšana
description: Ja kanban tiek iztukšots kļūdas dēļ, vai saņemtu kanban nepieciešams iztukšot, jums ir nepieciešams atjaunināt kanban statusu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8559c0843d7e6e538b5b29dc394a50d05462ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432945"
---
# <a name="update-kanban-status"></a><span data-ttu-id="a772d-103">Kanban statusa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="a772d-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a772d-104">Ja kanban tiek iztukšots kļūdas dēļ, vai saņemtu kanban nepieciešams iztukšot, jums ir nepieciešams atjaunināt kanban statusu.</span><span class="sxs-lookup"><span data-stu-id="a772d-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="a772d-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="a772d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a772d-106">Šī procedūra ir paredzēta veikala vadītājam.</span><span class="sxs-lookup"><span data-stu-id="a772d-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="a772d-107">Atrast Kanban.</span><span class="sxs-lookup"><span data-stu-id="a772d-107">Find the kanban.</span></span>
1. <span data-ttu-id="a772d-108">Doties uz Ražošanas kontrole > Kanban > Kanban.</span><span class="sxs-lookup"><span data-stu-id="a772d-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="a772d-109">Atveriet materiālu apstrādes vienības statusa kolonnas filtru.</span><span class="sxs-lookup"><span data-stu-id="a772d-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="a772d-110">Noklikšķiniet uz Notīrīt.</span><span class="sxs-lookup"><span data-stu-id="a772d-110">Click Clear.</span></span>
    * <span data-ttu-id="a772d-111">Tas atiestata filtrus.</span><span class="sxs-lookup"><span data-stu-id="a772d-111">This resets the filters.</span></span>  
4. <span data-ttu-id="a772d-112">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a772d-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a772d-113">Piemēram, filtrējiet pēc lauka Kartes numurs, izmantojot vērtību '000149'.</span><span class="sxs-lookup"><span data-stu-id="a772d-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="a772d-114">Mainīt statusu Iztukšots uz statusu Saņemts</span><span class="sxs-lookup"><span data-stu-id="a772d-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="a772d-115">Noklikšķiniet uz Atsaukt tukšu materiālu apstrādes vienību.</span><span class="sxs-lookup"><span data-stu-id="a772d-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="a772d-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="a772d-116">Click OK.</span></span>
    * <span data-ttu-id="a772d-117">Ņemiet vērā, ka materiālu apstrādes vienības statuss ir Saņemts.</span><span class="sxs-lookup"><span data-stu-id="a772d-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="a772d-118">Mainīt statusu Saņemts uz statusu Iztukšots</span><span class="sxs-lookup"><span data-stu-id="a772d-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="a772d-119">Noklikšķiniet Iztukšot Kanban.</span><span class="sxs-lookup"><span data-stu-id="a772d-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="a772d-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="a772d-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a772d-121">Ņemiet vērā, ka materiālu apstrādes vienības statuss ir Iztukšots.</span><span class="sxs-lookup"><span data-stu-id="a772d-121">Notice that the Handling unit status is Emptied.</span></span>  

