--- 
title: "Pamatlīdzekļa grāmatošanas profilu iestatīšana"
description: "Šajā uzdevuma ceļvedī tiks iestatītas pamatlīdzekļu grāmatošanas metodes."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="1fcb4-103">Pamatlīdzekļa grāmatošanas profilu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1fcb4-103">Set up fixed asset posting profiles</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1fcb4-104">Šajā uzdevuma ceļvedī tiks iestatītas pamatlīdzekļu grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="1fcb4-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="1fcb4-106">Uzdevuma ceļvedī sniegti piemēri pamata grāmatošanas metodei, lai gan grāmatošanas metodes ir jāizveido jūsu konkrētajam kontu plānam un finanšu atskaišu prasībām.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="1fcb4-107">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Pamatlīdzekļu grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="1fcb4-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-108">Click New.</span></span>
3. <span data-ttu-id="1fcb4-109">Ievadiet vērtību laukā Grāmatošanas metode.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="1fcb4-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1fcb4-111">Jums vajadzēs izveidot grāmatošanas metodi katram pamatlīdzekļu transakciju tipam, kuru izmantosit darbā ar pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="1fcb4-112">Šī uzdevuma ceļveža sākumā tiks apskatīts Iegādes transakcijas tips.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="1fcb4-113">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-113">Click Add.</span></span>
6. <span data-ttu-id="1fcb4-114">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="1fcb4-115">Grupējumu lauks ļauj definēt grāmatošanas metodi tabulai (viens konts iestatīts katram pamatlīdzeklim) vai grupai (viens konts iestatīts katrai pamatlīdzekļu grupai).</span><span class="sxs-lookup"><span data-stu-id="1fcb4-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="1fcb4-116">Šajā uzdevuma ceļvedī vērtība būs iestatīta uz “Visi”, lai norādīto grāmatu lietotu visiem pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="1fcb4-117">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="1fcb4-118">Iegādēm varat ievadīt korespondējošo kontu vai atstāt to tukšu, aizpildot to specifiskām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="1fcb4-119">Laukā Transakcijas veids atlasiet „Iegādes korekcija”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="1fcb4-120">Iegādes korekcijas transakcijām izmantosim tos pašus kontus, kas izmantoti iegādes transakcijām.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="1fcb4-121">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-121">Click Add.</span></span>
10. <span data-ttu-id="1fcb4-122">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="1fcb4-123">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="1fcb4-124">Iegāžu korekcijām varat ievadīt korespondējošo kontu vai atstāt to tukšu, aizpildot to specifiskām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="1fcb4-125">Laukā Transakcijas veids atlasiet „Nolietojums”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="1fcb4-126">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-126">Click Add.</span></span>
14. <span data-ttu-id="1fcb4-127">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="1fcb4-128">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="1fcb4-129">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="1fcb4-130">Laukā Transakcijas veids atlasiet „Nolietojuma korekcija”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="1fcb4-131">Nolietojuma korekcijas transakcijām izmantosim tos pašus kontus, kas izmantoti nolietojuma transakcijām.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="1fcb4-132">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-132">Click Add.</span></span>
19. <span data-ttu-id="1fcb4-133">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="1fcb4-134">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="1fcb4-135">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="1fcb4-136">Laukā Transakcijas veids atlasiet „Izslēgšana — pārdošana”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="1fcb4-137">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-137">Click Add.</span></span>
24. <span data-ttu-id="1fcb4-138">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="1fcb4-139">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="1fcb4-140">Izslēgšanām varat ievadīt korespondējošo kontu vai atstāt to tukšu, aizpildot to specifiskām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="1fcb4-141">Laukā Transakcijas veids atlasiet „Izslēgšana — brāķis”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="1fcb4-142">Izmantosim tos pašus kontus Izslēgšanas pārdošanai un Izslēgšanas brāķim.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="1fcb4-143">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-143">Click Add.</span></span>
28. <span data-ttu-id="1fcb4-144">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="1fcb4-145">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="1fcb4-146">Izslēgšanām varat ievadīt korespondējošo kontu vai atstāt to tukšu, aizpildot to specifiskām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="1fcb4-147">Izvērsiet sadaļu Izslēgšana.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="1fcb4-148">Jums ir jāiestata izslēgšanas grāmatošanas metodes gan pārdošanai, gan brāķim.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="1fcb4-149">Sāksim ar izslēgšanas pārdošanas transakcijām.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="1fcb4-150">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-150">Click Add.</span></span>
32. <span data-ttu-id="1fcb4-151">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="1fcb4-152">Laukā Grāmatot vērtību atlasiet „Iegādes vērtība”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="1fcb4-153">Iegādes vērtība attieksies uz iegādes un iegādes korekcijas vērtībām visus gadus.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="1fcb4-154">Šiem transakciju tipiem varat definēt arī atsevišķus kontus.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="1fcb4-155">Varat iestatīt izslēgšanas procesu, kuru izmantot dažādiem kontiem, atkarībā no tā, vai izslēgšanas rezultātā rodas peļņa vai zaudējumi.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="1fcb4-156">Šajā piemērā pārdošanas vērtības tips tiks iestatīts uz "Visi", lai izmantotu vienādus kontus visu veidu izslēgšanām.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="1fcb4-157">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="1fcb4-158">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="1fcb4-159">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-159">Click Add.</span></span>
37. <span data-ttu-id="1fcb4-160">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="1fcb4-161">Laukā Grāmatot vērtību atlasiet „Nolietojums (iepriekšējie gadi)”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="1fcb4-162">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="1fcb4-163">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="1fcb4-164">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-164">Click Add.</span></span>
41. <span data-ttu-id="1fcb4-165">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="1fcb4-166">Laukā Grāmatot vērtību atlasiet „Nolietojums (šis gads)”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="1fcb4-167">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="1fcb4-168">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="1fcb4-169">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-169">Click Add.</span></span>
46. <span data-ttu-id="1fcb4-170">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="1fcb4-171">Laukā Grāmatot vērtību atlasiet „Nolietojuma korekcijas (iepriekšējie gadi)”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="1fcb4-172">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="1fcb4-173">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="1fcb4-174">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-174">Click Add.</span></span>
51. <span data-ttu-id="1fcb4-175">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="1fcb4-176">Laukā Grāmatot vērtību atlasiet „Nolietojuma korekcijas (šis gads)”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="1fcb4-177">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="1fcb4-178">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="1fcb4-179">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-179">Click Add.</span></span>
56. <span data-ttu-id="1fcb4-180">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="1fcb4-181">Laukā Grāmatot vērtību atlasiet „Atlikusī vērtība”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="1fcb4-182">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="1fcb4-183">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="1fcb4-184">Laukā Pārdošana vai brāķis atlasiet „Brāķis”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="1fcb4-185">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-185">Click Add.</span></span>
62. <span data-ttu-id="1fcb4-186">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="1fcb4-187">Laukā Grāmatot vērtību atlasiet „Iegādes vērtība”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="1fcb4-188">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="1fcb4-189">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="1fcb4-190">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-190">Click Add.</span></span>
67. <span data-ttu-id="1fcb4-191">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="1fcb4-192">Laukā Grāmatot vērtību atlasiet „Nolietojums (iepriekšējie gadi)”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="1fcb4-193">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="1fcb4-194">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="1fcb4-195">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-195">Click Add.</span></span>
71. <span data-ttu-id="1fcb4-196">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="1fcb4-197">Laukā Grāmatot vērtību atlasiet „Nolietojums (šis gads)”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="1fcb4-198">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="1fcb4-199">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="1fcb4-200">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-200">Click Add.</span></span>
76. <span data-ttu-id="1fcb4-201">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="1fcb4-202">Laukā Grāmatot vērtību atlasiet „Nolietojuma korekcijas (iepriekšējie gadi)”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="1fcb4-203">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="1fcb4-204">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="1fcb4-205">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-205">Click Add.</span></span>
81. <span data-ttu-id="1fcb4-206">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="1fcb4-207">Laukā Grāmatot vērtību atlasiet „Nolietojuma korekcijas (šis gads)”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="1fcb4-208">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="1fcb4-209">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="1fcb4-210">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-210">Click Add.</span></span>
86. <span data-ttu-id="1fcb4-211">Laukā Grāmata ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="1fcb4-212">Laukā Grāmatot vērtību atlasiet „Atlikusī vērtība”.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="1fcb4-213">Laukā Galvenais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="1fcb4-214">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="1fcb4-214">In the Offset account field, specify the desired values.</span></span>


