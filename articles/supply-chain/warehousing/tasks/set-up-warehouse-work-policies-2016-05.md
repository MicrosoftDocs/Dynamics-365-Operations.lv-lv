--- 
title: "Noliktavas darba politiku iestatīšana "
description: "Ne vienmēr noliktavas procesi ietver noliktavas darbu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 22e359ee2ded2315c588c2dd5c3d62dee0440adf
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="349a7-103">Noliktavas darba politiku iestatīšana </span><span class="sxs-lookup"><span data-stu-id="349a7-103">Set up warehouse work policies</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="349a7-104">Ne vienmēr noliktavas procesi ietver noliktavas darbu.</span><span class="sxs-lookup"><span data-stu-id="349a7-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="349a7-105">Definējot darba politiku, jūs varat novērst darba izveidošanu izejmateriālu izdošanai un gatavās produkcijas izvietošanai preču kopai konkrētos novietojumos.</span><span class="sxs-lookup"><span data-stu-id="349a7-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="349a7-106">USMF demonstrācijas datu uzņēmums tika izmantots, lai izveidotu šo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="349a7-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="349a7-107">Šim uzdevumu ceļvedim ir nepieciešama Dynamics AX programma 7.0.1 vai jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="349a7-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="349a7-108">Dodieties uz Noliktavas vadība > Iestatīšana > Darbs > Darba politikas.</span><span class="sxs-lookup"><span data-stu-id="349a7-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="349a7-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="349a7-109">Click New.</span></span>
3. <span data-ttu-id="349a7-110">Darba politikas nosaukumu laukā ierakstiet 'Nav izvietošanas darbu'.</span><span class="sxs-lookup"><span data-stu-id="349a7-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="349a7-111">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="349a7-111">Click Save.</span></span>
5. <span data-ttu-id="349a7-112">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="349a7-112">Click Add.</span></span>
6. <span data-ttu-id="349a7-113">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="349a7-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="349a7-114">Darba pasūtījuma veida laukā atlasiet 'Pabeigto preču izvietošana'.</span><span class="sxs-lookup"><span data-stu-id="349a7-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="349a7-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="349a7-115">Click Add.</span></span>
9. <span data-ttu-id="349a7-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="349a7-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="349a7-117">Darba pasūtījuma veida laukā atlasiet 'Līdzproduktu un blakusproduktu izvietošana'.</span><span class="sxs-lookup"><span data-stu-id="349a7-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="349a7-118">Izvērsiet sadaļu Krājumu atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="349a7-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="349a7-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="349a7-119">Click Add.</span></span>
13. <span data-ttu-id="349a7-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="349a7-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="349a7-121">Sarakstā Noliktava ievadiet '51'.</span><span class="sxs-lookup"><span data-stu-id="349a7-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="349a7-122">Laukā Atrašanās vieta, ievadiet vai atlasiet '001'.</span><span class="sxs-lookup"><span data-stu-id="349a7-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="349a7-123">Izvērsiet sadaļu Preces.</span><span class="sxs-lookup"><span data-stu-id="349a7-123">Expand the Products section.</span></span>
17. <span data-ttu-id="349a7-124">Laukā Preču atlase, atlasiet 'Atlasīts'.</span><span class="sxs-lookup"><span data-stu-id="349a7-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="349a7-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="349a7-125">Click Add.</span></span>
19. <span data-ttu-id="349a7-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="349a7-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="349a7-127">Laukā Krājuma kods ievadiet vai atlasiet 'L0101'.</span><span class="sxs-lookup"><span data-stu-id="349a7-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="349a7-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="349a7-128">Click Save.</span></span>


