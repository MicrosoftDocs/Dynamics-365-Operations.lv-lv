---
title: Jaunas Kanban kārtulas izveide, dublējot esošu Kanban kārtulu
description: Šī procedūra koncentrējas uz esošo Kanban nosacījumu dublikāta radīšanu.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc65dd80221cedd25890037afcb3d2617f22793
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149209"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="e0229-103">Jaunas Kanban kārtulas izveide, dublējot esošu Kanban kārtulu</span><span class="sxs-lookup"><span data-stu-id="e0229-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0229-104">Šī procedūra koncentrējas uz esošo Kanban nosacījumu dublikāta radīšanu.</span><span class="sxs-lookup"><span data-stu-id="e0229-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="e0229-105">Tas ir noderīgi, ja vēlaties izveidot jaunus Kanban nosacījumus, pamatojoties uz esošajiem Kanban nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="e0229-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="e0229-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="e0229-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e0229-107">Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie sagatavo ražošanas procesu izmanītai ražošanas plūsmai vai jauniem papildināšanas noteikumiem.</span><span class="sxs-lookup"><span data-stu-id="e0229-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="e0229-108">Kanban nosacījumu atlase</span><span class="sxs-lookup"><span data-stu-id="e0229-108">Select a kanban rule</span></span>
1. <span data-ttu-id="e0229-109">Dodieties uz Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="e0229-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="e0229-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0229-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0229-111">Precei M0006 atlasiet Kanban nosacījumu 000017.</span><span class="sxs-lookup"><span data-stu-id="e0229-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="e0229-112">Kanban nosacījumu dublēšana</span><span class="sxs-lookup"><span data-stu-id="e0229-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="e0229-113">Noklikšķiniet uz Dublējiet Kanban nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="e0229-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="e0229-114">Dublējot Kanban nosacījumus, ir iespējams mainīt tipu, datumus, aktivitātes un preču atlasi.</span><span class="sxs-lookup"><span data-stu-id="e0229-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="e0229-115">Mainiet preci šai procedūrai nākamajā darbībā.</span><span class="sxs-lookup"><span data-stu-id="e0229-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="e0229-116">Laukā Prece ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e0229-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="e0229-117">Atlasiet M0007.</span><span class="sxs-lookup"><span data-stu-id="e0229-117">Select M0007.</span></span>  
3. <span data-ttu-id="e0229-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e0229-118">Click OK.</span></span>
    * <span data-ttu-id="e0229-119">Ņemiet vērā, ka tiek izveidoti dublēti Kanban nosacījumi 000017.</span><span class="sxs-lookup"><span data-stu-id="e0229-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

