---
title: Jaunas Kanban kārtulas izveide, dublējot esošu Kanban kārtulu
description: Šī procedūra koncentrējas uz esošo Kanban nosacījumu dublikāta radīšanu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b89fca4e55aa852bd127eb9b1bda07c0e5bcdc0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255137"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="12736-103">Jaunas Kanban kārtulas izveide, dublējot esošu Kanban kārtulu</span><span class="sxs-lookup"><span data-stu-id="12736-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12736-104">Šī procedūra koncentrējas uz esošo Kanban nosacījumu dublikāta radīšanu.</span><span class="sxs-lookup"><span data-stu-id="12736-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="12736-105">Tas ir noderīgi, ja vēlaties izveidot jaunus Kanban nosacījumus, pamatojoties uz esošajiem Kanban nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="12736-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="12736-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="12736-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="12736-107">Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie sagatavo ražošanas procesu izmanītai ražošanas plūsmai vai jauniem papildināšanas noteikumiem.</span><span class="sxs-lookup"><span data-stu-id="12736-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="12736-108">Kanban nosacījumu atlase</span><span class="sxs-lookup"><span data-stu-id="12736-108">Select a kanban rule</span></span>
1. <span data-ttu-id="12736-109">Dodieties uz Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="12736-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="12736-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="12736-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="12736-111">Precei M0006 atlasiet Kanban nosacījumu 000017.</span><span class="sxs-lookup"><span data-stu-id="12736-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="12736-112">Kanban nosacījumu dublēšana</span><span class="sxs-lookup"><span data-stu-id="12736-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="12736-113">Noklikšķiniet uz Dublējiet Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="12736-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="12736-114">Dublējot Kanban nosacījumus, ir iespējams mainīt tipu, datumus, aktivitātes un preču atlasi.</span><span class="sxs-lookup"><span data-stu-id="12736-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="12736-115">Mainiet preci šai procedūrai nākamajā darbībā.</span><span class="sxs-lookup"><span data-stu-id="12736-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="12736-116">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="12736-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="12736-117">Atlasiet M0007.</span><span class="sxs-lookup"><span data-stu-id="12736-117">Select M0007.</span></span>  
3. <span data-ttu-id="12736-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="12736-118">Click OK.</span></span>
    * <span data-ttu-id="12736-119">Ņemiet vērā, ka tiek izveidoti dublēti Kanban nosacījumi 000017.</span><span class="sxs-lookup"><span data-stu-id="12736-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]