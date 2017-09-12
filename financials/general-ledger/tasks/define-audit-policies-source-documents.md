--- 
title: "Pirmdokumentu audita ierobežojumu definēšana"
description: "Šajā procedūrā ir parādīts, kā izveidot un palaist audita ierobežojuma nosacījumus."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4b05f744120e940bfea3e92b8aac3e41fc8151d9
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="4033f-103">Pirmdokumentu audita ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="4033f-103">Define audit policies for source documents</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4033f-104">Šajā procedūrā ir parādīts, kā izveidot un palaist audita ierobežojuma nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="4033f-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="4033f-105">Piemērā tiek izmantotas izdevumu atskaites ar viesnīcu izdevumu tipu.</span><span class="sxs-lookup"><span data-stu-id="4033f-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="4033f-106">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="4033f-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="4033f-107">Auditora loma ietver šo uzdevumu veikšanai atbilstošās atļaujas.</span><span class="sxs-lookup"><span data-stu-id="4033f-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="4033f-108">Pārejiet uz sadaļu Audita rīks >; Iestatīšana > Ierobežojuma nosacījumu tips.</span><span class="sxs-lookup"><span data-stu-id="4033f-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="4033f-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4033f-109">Click New.</span></span>
3. <span data-ttu-id="4033f-110">Laukā Kārtulas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4033f-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="4033f-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="4033f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4033f-112">Laukā Vaicājuma nosaukums atlasiet Izdevumu atskaites rinda</span><span class="sxs-lookup"><span data-stu-id="4033f-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="4033f-113">Vaicājuma tipa laukā atlasiet Apkopojums</span><span class="sxs-lookup"><span data-stu-id="4033f-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="4033f-114">Laukā Juridiska persona atlasiet Juridiska persona</span><span class="sxs-lookup"><span data-stu-id="4033f-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="4033f-115">Laukā Dokumenta datuma atsauce atlasiet Modificēšanas datums un laiks</span><span class="sxs-lookup"><span data-stu-id="4033f-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="4033f-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="4033f-116">Click Save.</span></span>
10. <span data-ttu-id="4033f-117">Pārejiet uz sadaļu Audita rīks > Iestatīšana > Audita ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="4033f-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="4033f-118">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="4033f-118">Click New.</span></span>
12. <span data-ttu-id="4033f-119">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4033f-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="4033f-120">Izvērsiet sadaļu Politikas organizācijas.</span><span class="sxs-lookup"><span data-stu-id="4033f-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="4033f-121">Koka struktūrā atlasiet “Contoso Entertainment System USA”.</span><span class="sxs-lookup"><span data-stu-id="4033f-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="4033f-122">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="4033f-122">Click Add.</span></span>
16. <span data-ttu-id="4033f-123">Koka struktūrā atlasiet “Contoso Consulting USA”.</span><span class="sxs-lookup"><span data-stu-id="4033f-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="4033f-124">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="4033f-124">Click Add.</span></span>
18. <span data-ttu-id="4033f-125">Koka struktūrā atlasiet “Contoso Retail USA”.</span><span class="sxs-lookup"><span data-stu-id="4033f-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="4033f-126">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="4033f-126">Click Add.</span></span>
20. <span data-ttu-id="4033f-127">Sakļaujiet sadaļu Politikas organizācijas.</span><span class="sxs-lookup"><span data-stu-id="4033f-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="4033f-128">Izvērsiet sadaļu Ierobežojuma nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="4033f-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="4033f-129">Sarakstā atrodiet un atlasiet iepriekš izveidoto ierobežojuma nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="4033f-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="4033f-130">Noklikšķiniet uz Izveidot ierobežojuma nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="4033f-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="4033f-131">Laukā Spēkā stāšanās datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4033f-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="4033f-132">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="4033f-132">Click Filter.</span></span>
26. <span data-ttu-id="4033f-133">Sarakstā atlasiet rindu vienumam Izdevumu kategorija un detalizēto informāciju iestatiet uz Viesnīca</span><span class="sxs-lookup"><span data-stu-id="4033f-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="4033f-134">Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4033f-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="4033f-135">Noklikšķiniet uz cilnes Apkopot.</span><span class="sxs-lookup"><span data-stu-id="4033f-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="4033f-136">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="4033f-136">Click Add.</span></span>
30. <span data-ttu-id="4033f-137">Sarakstā atlasiet vērtību laukam Transakcijas summa</span><span class="sxs-lookup"><span data-stu-id="4033f-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="4033f-138">Laukā Lauks ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4033f-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="4033f-139">Laukā AggregateFunction atlasiet “Sum”.</span><span class="sxs-lookup"><span data-stu-id="4033f-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="4033f-140">Noklikšķiniet uz cilnes Grupēt pēc.</span><span class="sxs-lookup"><span data-stu-id="4033f-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="4033f-141">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="4033f-141">Click Add.</span></span>
35. <span data-ttu-id="4033f-142">Sarakstā atlasiet kādu vērtību vienumam Darbinieks </span><span class="sxs-lookup"><span data-stu-id="4033f-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="4033f-143">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="4033f-143">Click Add.</span></span>
37. <span data-ttu-id="4033f-144">Sarakstā atlasiet kādu vērtību vienumam Izdevumu kategorija</span><span class="sxs-lookup"><span data-stu-id="4033f-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="4033f-145">Laukā Lauks ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4033f-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="4033f-146">Noklikšķiniet uz cilnes Saturs.</span><span class="sxs-lookup"><span data-stu-id="4033f-146">Click the Having tab.</span></span>
40. <span data-ttu-id="4033f-147">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="4033f-147">Click Add.</span></span>
41. <span data-ttu-id="4033f-148">Atlasiet Transakcijas summa</span><span class="sxs-lookup"><span data-stu-id="4033f-148">Select Transaction amount</span></span>
42. <span data-ttu-id="4033f-149">Laukā Lauks ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="4033f-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="4033f-150">Laukā AggregateFunction atlasiet “Sum”.</span><span class="sxs-lookup"><span data-stu-id="4033f-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="4033f-151">Laukā Kritēriji ievadiet vērtību >2000.</span><span class="sxs-lookup"><span data-stu-id="4033f-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="4033f-152">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="4033f-152">Click OK.</span></span>
46. <span data-ttu-id="4033f-153">Noklikšķiniet uz Tests.</span><span class="sxs-lookup"><span data-stu-id="4033f-153">Click Test.</span></span>
47. <span data-ttu-id="4033f-154">Laukā Dokumentu atlases sākuma datums ievadiet kādu datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4033f-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="4033f-155">Laukā Dokumentu atlases beigu datums ievadiet kādu datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4033f-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="4033f-156">Noklikšķiniet uz Izpildīt testu.</span><span class="sxs-lookup"><span data-stu-id="4033f-156">Click Run test.</span></span>
50. <span data-ttu-id="4033f-157">Darbību rūtī noklikšķiniet uz Audita politika.</span><span class="sxs-lookup"><span data-stu-id="4033f-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="4033f-158">Noklikšķiniet uz Papildu opcijas.</span><span class="sxs-lookup"><span data-stu-id="4033f-158">Click Additional options.</span></span>
52. <span data-ttu-id="4033f-159">Laukā Sākuma datums ievadiet kādu datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4033f-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="4033f-160">Laukā Beigu datums ievadiet kādu datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="4033f-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="4033f-161">Noklikšķiniet uz Partija.</span><span class="sxs-lookup"><span data-stu-id="4033f-161">Click Batch.</span></span>
55. <span data-ttu-id="4033f-162">Izvērsiet sadaļu Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="4033f-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="4033f-163">Laukā Pakešapstrāde atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="4033f-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="4033f-164">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="4033f-164">Click OK.</span></span>
58. <span data-ttu-id="4033f-165">Pārejiet uz sadaļu Audita rīks > Audita gadījumi.</span><span class="sxs-lookup"><span data-stu-id="4033f-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="4033f-166">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4033f-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="4033f-167">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4033f-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="4033f-168">Izvērsiet sadaļu Saistības.</span><span class="sxs-lookup"><span data-stu-id="4033f-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="4033f-169">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4033f-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="4033f-170">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="4033f-170">In the list, click the link in the selected row.</span></span>


