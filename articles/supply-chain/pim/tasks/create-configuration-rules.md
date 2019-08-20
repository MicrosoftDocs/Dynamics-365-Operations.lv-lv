---
title: Konfigurācijas kārtulu izveide
description: Ar šo procedūru tiek izveidoti konfigurācijas noteikumi, kurus var izmantot konfigurācijai atbilstoši dimensijām, lai ieviestu vai novērstu noteiktas MK rindu kombinācijas.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f15c0328e391d81c4c977f974553ae9135b207c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844901"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="46c49-103">Konfigurācijas kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="46c49-103">Create configuration rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46c49-104">Ar šo procedūru tiek izveidoti konfigurācijas noteikumi, kurus var izmantot konfigurācijai atbilstoši dimensijām, lai ieviestu vai novērstu noteiktas MK rindu kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="46c49-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="46c49-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="46c49-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="46c49-106">Šī ir septītā procedūra no astoņām, kurā ir skaidrots, kā veidot kombinācijas konfigurācijai atbilstoši dimensijām.</span><span class="sxs-lookup"><span data-stu-id="46c49-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="46c49-107">Pārejiet uz sadaļu Preču informācijas pārvaldība > Materiālu komplekti un formulas > Materiālu komplekti.</span><span class="sxs-lookup"><span data-stu-id="46c49-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="46c49-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="46c49-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="46c49-109">Atrodiet un atlasiet MK konfigurācijai atbilstoši dimensijām.</span><span class="sxs-lookup"><span data-stu-id="46c49-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="46c49-110">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="46c49-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="46c49-111">Noklikšķiniet uz Mainīt skatījumu.</span><span class="sxs-lookup"><span data-stu-id="46c49-111">Click Change view.</span></span>
5. <span data-ttu-id="46c49-112">Noklikšķiniet uz Virsraksta skatījuma.</span><span class="sxs-lookup"><span data-stu-id="46c49-112">Click Header view.</span></span>
    * <span data-ttu-id="46c49-113">Atveriet virsraksta skatu, lai piekļūtu kopsavilkuma cilnei Konfigurācijas maršruts.</span><span class="sxs-lookup"><span data-stu-id="46c49-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="46c49-114">Izvērsiet vai sakļaujiet sadaļu Konfigurācijas maršruts.</span><span class="sxs-lookup"><span data-stu-id="46c49-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="46c49-115">Kopsavilkuma cilnei Konfigurācijas maršruts jābūt izvērstā režīmā.</span><span class="sxs-lookup"><span data-stu-id="46c49-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="46c49-116">Noklikšķiniet uz Konfigurācijas noteikumi.</span><span class="sxs-lookup"><span data-stu-id="46c49-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="46c49-117">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="46c49-117">Click New.</span></span>
9. <span data-ttu-id="46c49-118">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="46c49-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="46c49-119">Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="46c49-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="46c49-120">Tiek rādīti krājumi pašreizējā konfigurācijas grupā.</span><span class="sxs-lookup"><span data-stu-id="46c49-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="46c49-121">Atlasiet to, kas atspoguļo nosacījumu kārtulā.</span><span class="sxs-lookup"><span data-stu-id="46c49-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="46c49-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="46c49-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="46c49-123">Atlasiet opciju laukā Metode.</span><span class="sxs-lookup"><span data-stu-id="46c49-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="46c49-124">Ir iespējams piemērot krājuma atlasi vai atcelt krājuma atlasi no citas konfigurācijas grupas.</span><span class="sxs-lookup"><span data-stu-id="46c49-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="46c49-125">Laukā Atvasinātā grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="46c49-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="46c49-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="46c49-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="46c49-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="46c49-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="46c49-128">Atlasiet vēlamo konfigurācijas grupu.</span><span class="sxs-lookup"><span data-stu-id="46c49-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="46c49-129">Laukā Atvasinātā krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="46c49-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="46c49-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="46c49-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="46c49-131">Atlasiet krājuma kodu, kas tiks atlasīts vai kura atlase tika noņemta atkarībā no izvēlētās metodes.</span><span class="sxs-lookup"><span data-stu-id="46c49-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="46c49-132">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="46c49-132">Close the page.</span></span>

