---
title: Organizācijas struktūrvienību attiecību izstrāde
description: Šajā procedūrā ir aprakstīts, kā noformēt attiecības starp organizācijas vienībām.
author: mugunthanm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner, OMNodeSelection,  HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c6502a05d3cc53d8031b9f8e365454556513c3c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414090"
---
# <a name="design-the-relationships-between-organizational-units"></a><span data-ttu-id="e35c9-103">Organizācijas struktūrvienību attiecību izstrāde</span><span class="sxs-lookup"><span data-stu-id="e35c9-103">Design the relationships between organizational units</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e35c9-104">Šajā procedūrā ir aprakstīts, kā noformēt attiecības starp organizācijas vienībām.</span><span class="sxs-lookup"><span data-stu-id="e35c9-104">This procedure walks through how to design the relationship between organizational units.</span></span> <span data-ttu-id="e35c9-105">Pirms definējat attiecības, ir jāizveido jauns organizācijas nolūks, vai varat izmantot jau esošo organizācijas nolūku.</span><span class="sxs-lookup"><span data-stu-id="e35c9-105">You must create a new organization purpose before defining the relationship, or you can use the existing organization purpose.</span></span> <span data-ttu-id="e35c9-106">Demonstrācijas datu uzņēmums, kas tiek izmantots šīs procedūras izpildei, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="e35c9-106">The demo data company used to complete this procedure is USRT.</span></span> <span data-ttu-id="e35c9-107">Šis uzdevums ir paredzēts lietotajiem ar administratora lomu.</span><span class="sxs-lookup"><span data-stu-id="e35c9-107">This task is intended for the administrator role.</span></span>

1. <span data-ttu-id="e35c9-108">Dodieties uz Organizācijas administrēšana > Organizācijas > Organizāciju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="e35c9-108">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="e35c9-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e35c9-109">Click New.</span></span>
3. <span data-ttu-id="e35c9-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e35c9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e35c9-111">Noklikšķiniet uz Piešķirt nolūku.</span><span class="sxs-lookup"><span data-stu-id="e35c9-111">Click Assign purpose.</span></span>
5. <span data-ttu-id="e35c9-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e35c9-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="e35c9-113">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="e35c9-113">Click Add.</span></span>
7. <span data-ttu-id="e35c9-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e35c9-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e35c9-115">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="e35c9-115">Click OK.</span></span>
    * <span data-ttu-id="e35c9-116">Varat atlasīt tādu skaitu organizācijas nolūku, cik nepieciešams jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="e35c9-116">You can select as many organization purposes as required for your organization.</span></span>  
9. <span data-ttu-id="e35c9-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e35c9-117">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e35c9-118">Noklikšķiniet uz Iestatīt kā noklusējumu.</span><span class="sxs-lookup"><span data-stu-id="e35c9-118">Click Set as default.</span></span>
11. <span data-ttu-id="e35c9-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e35c9-119">Close the page.</span></span>
12. <span data-ttu-id="e35c9-120">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e35c9-120">Click Save.</span></span>
13. <span data-ttu-id="e35c9-121">Noklikšķiniet uz Skatīt.</span><span class="sxs-lookup"><span data-stu-id="e35c9-121">Click View.</span></span>
14. <span data-ttu-id="e35c9-122">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="e35c9-122">Click Edit.</span></span>
15. <span data-ttu-id="e35c9-123">Klikšķiniet Ievietot.</span><span class="sxs-lookup"><span data-stu-id="e35c9-123">Click Insert.</span></span>
16. <span data-ttu-id="e35c9-124">Noklikšķiniet uz Biznesa vienība.</span><span class="sxs-lookup"><span data-stu-id="e35c9-124">Click Business unit.</span></span>
17. <span data-ttu-id="e35c9-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e35c9-125">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="e35c9-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e35c9-126">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="e35c9-127">Klikšķiniet Ievietot.</span><span class="sxs-lookup"><span data-stu-id="e35c9-127">Click Insert.</span></span>
20. <span data-ttu-id="e35c9-128">Noklikšķiniet uz Komercijas kanāls.</span><span class="sxs-lookup"><span data-stu-id="e35c9-128">Click Commerce channel.</span></span>
21. <span data-ttu-id="e35c9-129">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e35c9-129">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="e35c9-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e35c9-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e35c9-131">Varat pievienot tik daudz organizācijas vienību, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="e35c9-131">You can add as many organization units as is required.</span></span>  
23. <span data-ttu-id="e35c9-132">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e35c9-132">Click Save.</span></span>
24. <span data-ttu-id="e35c9-133">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="e35c9-133">Click Close.</span></span>
25. <span data-ttu-id="e35c9-134">Noklikšķiniet uz Publicēt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="e35c9-134">Click Publish to open the drop dialog.</span></span>
26. <span data-ttu-id="e35c9-135">Laukā Spēkā stāšanās datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="e35c9-135">In the Effective date field, enter a date and time.</span></span>
27. <span data-ttu-id="e35c9-136">Laukā Spēkā stāšanās datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="e35c9-136">In the Effective date field, enter a date and time.</span></span>
28. <span data-ttu-id="e35c9-137">Laukā Aprakstīt izmaiņas ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e35c9-137">In the Describe changes field, type a value.</span></span>
29. <span data-ttu-id="e35c9-138">Noklikšķiniet uz Publicēt.</span><span class="sxs-lookup"><span data-stu-id="e35c9-138">Click Publish.</span></span>
30. <span data-ttu-id="e35c9-139">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="e35c9-139">Click Close.</span></span>

