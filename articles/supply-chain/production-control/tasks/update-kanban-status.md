---
title: Kanban statusa atjaunināšana
description: Ja kanban tiek iztukšots kļūdas dēļ, vai saņemtu kanban nepieciešams iztukšot, jums ir nepieciešams atjaunināt Kanban statusu.
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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 055765452579b1de74f1c2158de9c6cb4ee80f16
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252826"
---
# <a name="update-kanban-status"></a><span data-ttu-id="6a660-103">Kanban statusa atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="6a660-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a660-104">Ja Kanban tiek iztukšots kļūdas dēļ, vai saņemtu Kanban nepieciešams iztukšot, jums ir nepieciešams atjaunināt Kanban statusu.</span><span class="sxs-lookup"><span data-stu-id="6a660-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="6a660-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="6a660-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6a660-106">Šī procedūra ir paredzēta veikala vadītājam.</span><span class="sxs-lookup"><span data-stu-id="6a660-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="6a660-107">Atrast Kanban.</span><span class="sxs-lookup"><span data-stu-id="6a660-107">Find the kanban.</span></span>
1. <span data-ttu-id="6a660-108">Doties uz Ražošanas kontrole > Kanban > Kanban.</span><span class="sxs-lookup"><span data-stu-id="6a660-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="6a660-109">Atveriet materiālu apstrādes vienības statusa kolonnas filtru.</span><span class="sxs-lookup"><span data-stu-id="6a660-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="6a660-110">Noklikšķiniet uz Notīrīt.</span><span class="sxs-lookup"><span data-stu-id="6a660-110">Click Clear.</span></span>
    * <span data-ttu-id="6a660-111">Tas atiestata filtrus.</span><span class="sxs-lookup"><span data-stu-id="6a660-111">This resets the filters.</span></span>  
4. <span data-ttu-id="6a660-112">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="6a660-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6a660-113">Piemēram, filtrējiet pēc lauka Kartes numurs, izmantojot vērtību '000149'.</span><span class="sxs-lookup"><span data-stu-id="6a660-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="6a660-114">Mainīt statusu Iztukšots uz statusu Saņemts</span><span class="sxs-lookup"><span data-stu-id="6a660-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="6a660-115">Noklikšķiniet uz Atsaukt tukšu materiālu apstrādes vienību.</span><span class="sxs-lookup"><span data-stu-id="6a660-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="6a660-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="6a660-116">Click OK.</span></span>
    * <span data-ttu-id="6a660-117">Ņemiet vērā, ka materiālu apstrādes vienības statuss ir Saņemts.</span><span class="sxs-lookup"><span data-stu-id="6a660-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="6a660-118">Mainīt statusu Saņemts uz statusu Iztukšots</span><span class="sxs-lookup"><span data-stu-id="6a660-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="6a660-119">Noklikšķiniet Iztukšot Kanban.</span><span class="sxs-lookup"><span data-stu-id="6a660-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="6a660-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6a660-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6a660-121">Ņemiet vērā, ka materiālu apstrādes vienības statuss ir Iztukšots.</span><span class="sxs-lookup"><span data-stu-id="6a660-121">Notice that the Handling unit status is Emptied.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]