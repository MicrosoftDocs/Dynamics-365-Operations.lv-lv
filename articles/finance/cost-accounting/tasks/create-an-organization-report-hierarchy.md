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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3db8465c462caffeaf6bd12d17c4b61355ed8eed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208755"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="b67b9-103">Organizācijas pārskatu hierarhijas izveide</span><span class="sxs-lookup"><span data-stu-id="b67b9-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b67b9-104">Izmantojiet šo procedūru, lai izveidotu pārskatu hierarhiju organizācijas pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="b67b9-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="b67b9-105">Šī ieraksta mērķis ir vadīt jūs dimensiju hierarhijā, lai varat turpināt, kamēr tiek izveidota visa organizācijas pārskatu struktūra.</span><span class="sxs-lookup"><span data-stu-id="b67b9-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="b67b9-106">Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="b67b9-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="b67b9-107">Dodieties uz Izmaksu uzskaite > Dimensijas > Dimensiju hierarhijas.</span><span class="sxs-lookup"><span data-stu-id="b67b9-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="b67b9-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-108">Click New.</span></span>
3. <span data-ttu-id="b67b9-109">Laukā HierarchyTypeComboBox atlasiet "Dimension classification hierarchy".</span><span class="sxs-lookup"><span data-stu-id="b67b9-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="b67b9-110">Atlasiet Dimensiju klasifikācijas hierarhija.</span><span class="sxs-lookup"><span data-stu-id="b67b9-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="b67b9-111">Veids Dimensiju klasifikācijas hierarhija tiek izmantots kārtulu definēšanai un pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="b67b9-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="b67b9-112">Tas atbalsta visas dimensijas, piemēram, izmaksu objektu, izmaksu elementu un statistiskās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="b67b9-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="b67b9-113">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="b67b9-113">Click Create.</span></span>
5. <span data-ttu-id="b67b9-114">Laukā Dimensijas hierarhijas nosaukums ierakstiet "Oganization USP2".</span><span class="sxs-lookup"><span data-stu-id="b67b9-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="b67b9-115">Laukā Dimensija ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b67b9-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="b67b9-116">Atlasiet Izmaksu centri.</span><span class="sxs-lookup"><span data-stu-id="b67b9-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="b67b9-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-117">Click Save.</span></span>
8. <span data-ttu-id="b67b9-118">Noklikšķiniet uz Skatīt hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="b67b9-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="b67b9-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-119">Click New.</span></span>
10. <span data-ttu-id="b67b9-120">Laukā Zara nosaukums ierakstiet "CEO".</span><span class="sxs-lookup"><span data-stu-id="b67b9-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="b67b9-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-121">Click Save.</span></span>
12. <span data-ttu-id="b67b9-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-122">Click New.</span></span>
13. <span data-ttu-id="b67b9-123">Laukā Zara nosaukums ierakstiet "CEO cost centers".</span><span class="sxs-lookup"><span data-stu-id="b67b9-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="b67b9-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-124">Click Save.</span></span>
15. <span data-ttu-id="b67b9-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-125">Click New.</span></span>
16. <span data-ttu-id="b67b9-126">Laukā Zara nosaukums ierakstiet "Region East".</span><span class="sxs-lookup"><span data-stu-id="b67b9-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="b67b9-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-127">Click Save.</span></span>
18. <span data-ttu-id="b67b9-128">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-128">Click New.</span></span>
19. <span data-ttu-id="b67b9-129">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b67b9-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="b67b9-130">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b67b9-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b67b9-131">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="b67b9-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="b67b9-132">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-132">Click Save.</span></span>
22. <span data-ttu-id="b67b9-133">Kokā atlasiet Oganization USP2\CEO\CEO izmaksu centri.</span><span class="sxs-lookup"><span data-stu-id="b67b9-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="b67b9-134">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-134">Click New.</span></span>
24. <span data-ttu-id="b67b9-135">Laukā Zara nosaukums ierakstiet "Region West".</span><span class="sxs-lookup"><span data-stu-id="b67b9-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="b67b9-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-136">Click Save.</span></span>
26. <span data-ttu-id="b67b9-137">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-137">Click New.</span></span>
27. <span data-ttu-id="b67b9-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b67b9-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="b67b9-139">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b67b9-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b67b9-140">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="b67b9-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="b67b9-141">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-141">Click Save.</span></span>
30. <span data-ttu-id="b67b9-142">Kokā atlasiet Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="b67b9-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="b67b9-143">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-143">Click New.</span></span>
32. <span data-ttu-id="b67b9-144">Laukā Zara nosaukums ierakstiet "CFO cost centers".</span><span class="sxs-lookup"><span data-stu-id="b67b9-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="b67b9-145">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-145">Click Save.</span></span>
34. <span data-ttu-id="b67b9-146">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-146">Click New.</span></span>
35. <span data-ttu-id="b67b9-147">Laukā Zara nosaukums ierakstiet "Marketing campa".</span><span class="sxs-lookup"><span data-stu-id="b67b9-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="b67b9-148">Laukā Zara nosaukums ierakstiet "Marketing campaign".</span><span class="sxs-lookup"><span data-stu-id="b67b9-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="b67b9-149">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-149">Click Save.</span></span>
38. <span data-ttu-id="b67b9-150">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-150">Click New.</span></span>
39. <span data-ttu-id="b67b9-151">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b67b9-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="b67b9-152">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b67b9-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b67b9-153">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="b67b9-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="b67b9-154">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-154">Click Save.</span></span>
42. <span data-ttu-id="b67b9-155">Koka struktūrā atlasiet “Organization USP2\CEO\CFO cost centers”.</span><span class="sxs-lookup"><span data-stu-id="b67b9-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="b67b9-156">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-156">Click New.</span></span>
44. <span data-ttu-id="b67b9-157">Laukā Zara nosaukums ierakstiet "Trade shows".</span><span class="sxs-lookup"><span data-stu-id="b67b9-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="b67b9-158">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-158">Click Save.</span></span>
46. <span data-ttu-id="b67b9-159">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-159">Click New.</span></span>
47. <span data-ttu-id="b67b9-160">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b67b9-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="b67b9-161">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b67b9-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b67b9-162">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="b67b9-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="b67b9-163">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-163">Click Save.</span></span>
50. <span data-ttu-id="b67b9-164">Kokā atlasiet Oganization USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="b67b9-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="b67b9-165">Laukā Zara nosaukums ierakstiet "CIO cost centers".</span><span class="sxs-lookup"><span data-stu-id="b67b9-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="b67b9-166">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-166">Click Save.</span></span>
53. <span data-ttu-id="b67b9-167">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-167">Click New.</span></span>
54. <span data-ttu-id="b67b9-168">Laukā Zara nosaukums ierakstiet "Call centers".</span><span class="sxs-lookup"><span data-stu-id="b67b9-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="b67b9-169">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-169">Click Save.</span></span>
56. <span data-ttu-id="b67b9-170">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="b67b9-170">Click New.</span></span>
57. <span data-ttu-id="b67b9-171">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b67b9-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="b67b9-172">Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b67b9-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="b67b9-173">Atlasiet dimensijas elementu, kas atbilst zaram.</span><span class="sxs-lookup"><span data-stu-id="b67b9-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="b67b9-174">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b67b9-174">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]