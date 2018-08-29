--- 
title: "Zvanu centra kanālu izveide un kanāla atribūtu definēšana"
description: "Šajā procedūrā ir aprakstīts, kā izveidot jaunu mazumtirdzniecības kanālu un definēt kanāla atribūtus."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 7ef094535214ecf4c65f95c36a93455446d7e388
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="35d64-103">Zvanu centra kanālu izveide un kanāla atribūtu definēšana</span><span class="sxs-lookup"><span data-stu-id="35d64-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="35d64-104">Šajā procedūrā ir aprakstīts, kā izveidot jaunu mazumtirdzniecības kanālu un definēt kanāla atribūtus.</span><span class="sxs-lookup"><span data-stu-id="35d64-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="35d64-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USRT.</span><span class="sxs-lookup"><span data-stu-id="35d64-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="35d64-106">Šī procedūra ir paredzēta lomai Mazumtirdzniecības IT.</span><span class="sxs-lookup"><span data-stu-id="35d64-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="35d64-107">Izveidot jaunu veikalu</span><span class="sxs-lookup"><span data-stu-id="35d64-107">Create new store</span></span>
1. <span data-ttu-id="35d64-108">Dodieties uz Visas darbvietas > Kanāla izvietošana.</span><span class="sxs-lookup"><span data-stu-id="35d64-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="35d64-109">Noklikšķiniet uz Jauns kanāls.</span><span class="sxs-lookup"><span data-stu-id="35d64-109">Click New channel.</span></span>
3. <span data-ttu-id="35d64-110">Noklikšķiniet uz Veikals.</span><span class="sxs-lookup"><span data-stu-id="35d64-110">Click Store.</span></span>
4. <span data-ttu-id="35d64-111">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="35d64-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="35d64-112">Laukā Veikala numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="35d64-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="35d64-113">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="35d64-114">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35d64-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="35d64-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="35d64-116">Laukā Noliktavas laika josla atlasiet atbilstošo opciju.</span><span class="sxs-lookup"><span data-stu-id="35d64-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="35d64-117">Laukā Kanāla profils noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="35d64-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="35d64-119">Laukā Valoda noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="35d64-120">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35d64-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="35d64-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="35d64-122">Laukā PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="35d64-123">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35d64-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="35d64-124">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="35d64-125">Laukā Debitoru adrešu grāmata noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35d64-126">Atlasiet adrešu grāmatu, kura ir izmantota debitoru saistīšanai ar šo veikalu.</span><span class="sxs-lookup"><span data-stu-id="35d64-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="35d64-127">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35d64-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="35d64-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="35d64-129">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="35d64-129">Click Select.</span></span>
22. <span data-ttu-id="35d64-130">Laukā Darbinieku adrešu grāmata noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="35d64-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35d64-131">Atlasiet adrešu grāmatu, kura ir izmantota kasieru saistīšanai ar šo kanālu.</span><span class="sxs-lookup"><span data-stu-id="35d64-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="35d64-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35d64-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="35d64-133">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="35d64-134">Noklikšķiniet uz Atlasīt.</span><span class="sxs-lookup"><span data-stu-id="35d64-134">Click Select.</span></span>
26. <span data-ttu-id="35d64-135">Laukā Noklusējuma debitors noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="35d64-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="35d64-136">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="35d64-137">Izvērsiet vai sakļaujiet sadaļu Ekrāna izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="35d64-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="35d64-138">Laukā Ekrāna izkārtojuma ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="35d64-139">Atlasiet noklusējuma POS ekrāna izkārtojumu šim veikalam.</span><span class="sxs-lookup"><span data-stu-id="35d64-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="35d64-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35d64-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="35d64-141">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="35d64-142">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="35d64-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="35d64-143">Noklikšķiniet uz Kanāla atribūti.</span><span class="sxs-lookup"><span data-stu-id="35d64-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="35d64-144">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="35d64-144">Click New.</span></span>
35. <span data-ttu-id="35d64-145">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="35d64-146">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35d64-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="35d64-147">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="35d64-148">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="35d64-148">Click Save.</span></span>
39. <span data-ttu-id="35d64-149">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35d64-149">Close the page.</span></span>
40. <span data-ttu-id="35d64-150">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="35d64-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="35d64-151">Noklikšķiniet uz Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="35d64-151">Click Payment methods.</span></span>
42. <span data-ttu-id="35d64-152">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="35d64-152">Click New.</span></span>
43. <span data-ttu-id="35d64-153">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="35d64-154">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="35d64-155">Izvērsiet vai sakļaujiet sadaļu Grāmatošana.</span><span class="sxs-lookup"><span data-stu-id="35d64-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="35d64-156">Laukā Konta numurs norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="35d64-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="35d64-157">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="35d64-157">Click Save.</span></span>
48. <span data-ttu-id="35d64-158">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35d64-158">Close the page.</span></span>
49. <span data-ttu-id="35d64-159">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="35d64-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="35d64-160">Noklikšķiniet uz Skaidrās naudas uzskaite.</span><span class="sxs-lookup"><span data-stu-id="35d64-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="35d64-161">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="35d64-161">Click New.</span></span>
52. <span data-ttu-id="35d64-162">Laukā Summa transakcijas valūtā ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="35d64-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="35d64-163">Laukā Valūta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="35d64-164">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35d64-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="35d64-165">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="35d64-166">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="35d64-166">Click Save.</span></span>
57. <span data-ttu-id="35d64-167">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35d64-167">Close the page.</span></span>
58. <span data-ttu-id="35d64-168">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="35d64-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="35d64-169">Noklikšķiniet uz Veikala vietrāžu grupas piešķire.</span><span class="sxs-lookup"><span data-stu-id="35d64-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="35d64-170">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="35d64-170">Click New.</span></span>
61. <span data-ttu-id="35d64-171">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="35d64-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="35d64-172">Laukā Vietrāžu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="35d64-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="35d64-173">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="35d64-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="35d64-174">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="35d64-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="35d64-175">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="35d64-175">Click Save.</span></span>
66. <span data-ttu-id="35d64-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="35d64-176">Close the page.</span></span>


