---
title: Organizācijas pārskatu hierarhijas izveide
description: Izmantojiet šo procedūru, lai izveidotu pārskatu hierarhiju organizācijas pārskatiem.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57203a7ddbacd631cbf800fb3a98e35a485cb74f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976263"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="e2d99-103">Organizācijas pārskatu hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="e2d99-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2d99-104">Izmantojiet šo procedūru, lai izveidotu pārskatu hierarhiju organizācijas pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="e2d99-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="e2d99-105">Šī ieraksta mērķis ir vadīt jūs dimensiju hierarhijā, lai varat turpināt, kamēr tiek izveidota visa organizācijas pārskatu struktūra.</span><span class="sxs-lookup"><span data-stu-id="e2d99-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="e2d99-106">Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="e2d99-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="e2d99-107">Dodieties uz Izmaksu uzskaite > Dimensijas > Dimensiju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="e2d99-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="e2d99-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-108">Click New.</span></span>
3. <span data-ttu-id="e2d99-109">Laukā HierarchyTypeComboBox atlasiet "Dimension classification hierarchy".</span><span class="sxs-lookup"><span data-stu-id="e2d99-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="e2d99-110">Atlasiet Dimensiju klasifikācijas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="e2d99-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="e2d99-111">Veids Dimensiju klasifikācijas hierarhija tiek izmantots kārtulu definēšanai un pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="e2d99-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="e2d99-112">Tas atbalsta visas dimensijas, piemēram, izmaksu objektu, izmaksu elementu un statistiskās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e2d99-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="e2d99-113">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="e2d99-113">Click Create.</span></span>
5. <span data-ttu-id="e2d99-114">Laukā Dimensijas hierarhijas nosaukums ierakstiet "Oganization USP2".</span><span class="sxs-lookup"><span data-stu-id="e2d99-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="e2d99-115">Laukā Dimensija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2d99-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="e2d99-116">Atlasiet Izmaksu centri.</span><span class="sxs-lookup"><span data-stu-id="e2d99-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="e2d99-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-117">Click Save.</span></span>
8. <span data-ttu-id="e2d99-118">Noklikšķiniet uz Skatīt hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="e2d99-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="e2d99-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-119">Click New.</span></span>
10. <span data-ttu-id="e2d99-120">Laukā Zara nosaukums ierakstiet "CEO".</span><span class="sxs-lookup"><span data-stu-id="e2d99-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="e2d99-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-121">Click Save.</span></span>
12. <span data-ttu-id="e2d99-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-122">Click New.</span></span>
13. <span data-ttu-id="e2d99-123">Laukā Zara nosaukums ierakstiet "CEO cost centers".</span><span class="sxs-lookup"><span data-stu-id="e2d99-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="e2d99-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-124">Click Save.</span></span>
15. <span data-ttu-id="e2d99-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-125">Click New.</span></span>
16. <span data-ttu-id="e2d99-126">Laukā Zara nosaukums ierakstiet "Region East".</span><span class="sxs-lookup"><span data-stu-id="e2d99-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="e2d99-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-127">Click Save.</span></span>
18. <span data-ttu-id="e2d99-128">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-128">Click New.</span></span>
19. <span data-ttu-id="e2d99-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e2d99-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="e2d99-130">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2d99-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e2d99-131">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="e2d99-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="e2d99-132">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-132">Click Save.</span></span>
22. <span data-ttu-id="e2d99-133">Kokā atlasiet Oganization USP2\CEO\CEO izmaksu centri.</span><span class="sxs-lookup"><span data-stu-id="e2d99-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="e2d99-134">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-134">Click New.</span></span>
24. <span data-ttu-id="e2d99-135">Laukā Zara nosaukums ierakstiet "Region West".</span><span class="sxs-lookup"><span data-stu-id="e2d99-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="e2d99-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-136">Click Save.</span></span>
26. <span data-ttu-id="e2d99-137">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-137">Click New.</span></span>
27. <span data-ttu-id="e2d99-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e2d99-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="e2d99-139">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2d99-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e2d99-140">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="e2d99-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="e2d99-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-141">Click Save.</span></span>
30. <span data-ttu-id="e2d99-142">Kokā atlasiet Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="e2d99-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="e2d99-143">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-143">Click New.</span></span>
32. <span data-ttu-id="e2d99-144">Laukā Zara nosaukums ierakstiet "CFO cost centers".</span><span class="sxs-lookup"><span data-stu-id="e2d99-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="e2d99-145">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-145">Click Save.</span></span>
34. <span data-ttu-id="e2d99-146">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-146">Click New.</span></span>
35. <span data-ttu-id="e2d99-147">Laukā Zara nosaukums ierakstiet "Marketing campa".</span><span class="sxs-lookup"><span data-stu-id="e2d99-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="e2d99-148">Laukā Zara nosaukums ierakstiet "Marketing campaign".</span><span class="sxs-lookup"><span data-stu-id="e2d99-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="e2d99-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-149">Click Save.</span></span>
38. <span data-ttu-id="e2d99-150">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-150">Click New.</span></span>
39. <span data-ttu-id="e2d99-151">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e2d99-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="e2d99-152">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2d99-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e2d99-153">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="e2d99-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="e2d99-154">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-154">Click Save.</span></span>
42. <span data-ttu-id="e2d99-155">Koka struktūrā atlasiet “Organization USP2\CEO\CFO cost centers”.</span><span class="sxs-lookup"><span data-stu-id="e2d99-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="e2d99-156">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-156">Click New.</span></span>
44. <span data-ttu-id="e2d99-157">Laukā Zara nosaukums ierakstiet "Trade shows".</span><span class="sxs-lookup"><span data-stu-id="e2d99-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="e2d99-158">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-158">Click Save.</span></span>
46. <span data-ttu-id="e2d99-159">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-159">Click New.</span></span>
47. <span data-ttu-id="e2d99-160">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e2d99-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="e2d99-161">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2d99-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e2d99-162">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="e2d99-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="e2d99-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-163">Click Save.</span></span>
50. <span data-ttu-id="e2d99-164">Kokā atlasiet Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="e2d99-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="e2d99-165">Laukā Zara nosaukums ierakstiet "CIO cost centers".</span><span class="sxs-lookup"><span data-stu-id="e2d99-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="e2d99-166">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-166">Click Save.</span></span>
53. <span data-ttu-id="e2d99-167">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-167">Click New.</span></span>
54. <span data-ttu-id="e2d99-168">Laukā Zara nosaukums ierakstiet "Call centers".</span><span class="sxs-lookup"><span data-stu-id="e2d99-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="e2d99-169">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-169">Click Save.</span></span>
56. <span data-ttu-id="e2d99-170">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="e2d99-170">Click New.</span></span>
57. <span data-ttu-id="e2d99-171">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="e2d99-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="e2d99-172">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2d99-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="e2d99-173">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="e2d99-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="e2d99-174">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="e2d99-174">Click Save.</span></span>

