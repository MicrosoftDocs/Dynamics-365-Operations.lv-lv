---
title: Kreditoru apstiprināšana konkrētām precēm
description: Šī procedūra parāda, kā apstiprināt kreditorus īpašām precēm.
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fafa2f7da5575206d452f31bb297790874369dfd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383278"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="e2983-103">Kreditoru apstiprināšana konkrētām precēm</span><span class="sxs-lookup"><span data-stu-id="e2983-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2983-104">Šī procedūra parāda, kā apstiprināt kreditorus īpašām precēm.</span><span class="sxs-lookup"><span data-stu-id="e2983-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="e2983-105">Tas ļauj kontrolēt, kurus kreditorus var izmantot, kad preces tiek pievienots pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="e2983-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="e2983-106">Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="e2983-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="e2983-107">Šo uzdevumu parasti veic pirkšanas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="e2983-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="e2983-108">Navigācijas rūtī dodieties uz **Moduļi > Preču informācijas pārvaldība > Preces > Tirdzniecībā izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="e2983-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="e2983-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e2983-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e2983-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="e2983-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e2983-111">Izvērsiet kopsavilkuma cilni **Pirkšana**.</span><span class="sxs-lookup"><span data-stu-id="e2983-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="e2983-112">Ja laukā **Kreditors** ir parādīts sākotnējais kreditors, tad jums ir nepieciešams pievienot šo kreditoru kā apstiprināto kreditoru, veicot šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="e2983-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="e2983-113">Pierakstiet kreditora numuru, ja tas tiek parādīts.</span><span class="sxs-lookup"><span data-stu-id="e2983-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="e2983-114">Darbību rūtī noklikšķiniet uz **Pirkšana**.</span><span class="sxs-lookup"><span data-stu-id="e2983-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="e2983-115">Noklišķiniet uz **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="e2983-115">Click **Setup**.</span></span>
7. <span data-ttu-id="e2983-116">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e2983-116">Click **Add**.</span></span>
8. <span data-ttu-id="e2983-117">Laukā Kreditors ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2983-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="e2983-118">Atlasiet apstiprināto piegādātāju.</span><span class="sxs-lookup"><span data-stu-id="e2983-118">Select the approved vendor.</span></span> <span data-ttu-id="e2983-119">Vismaz vienai no rindām ir jābūt primārajam kreditoram, ja preces ierakstā bija viens.</span><span class="sxs-lookup"><span data-stu-id="e2983-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="e2983-120">Ja agrāk veicāt kreditora numura piezīmi, atlasiet to šeit.</span><span class="sxs-lookup"><span data-stu-id="e2983-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="e2983-121">Laukā **Termiņa beigas** ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="e2983-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="e2983-122">Atlasiet datumu, kas ir dažus mēnešus uz priekšu.</span><span class="sxs-lookup"><span data-stu-id="e2983-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="e2983-123">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e2983-123">Click **Add**.</span></span>
11. <span data-ttu-id="e2983-124">Laukā **Kreditors** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e2983-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="e2983-125">Laukā **Termiņa beigas** ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="e2983-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="e2983-126">Atlasiet datumu, kas atšķiras no iepriekšējā beigu datuma.</span><span class="sxs-lookup"><span data-stu-id="e2983-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="e2983-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2983-127">Close the page.</span></span>
14. <span data-ttu-id="e2983-128">Darbību rūtī noklikšķiniet uz **Apstiprinātie kreditori**.</span><span class="sxs-lookup"><span data-stu-id="e2983-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="e2983-129">Laukā **Termiņa beigas** ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="e2983-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="e2983-130">Šis datums darbojas kā filtrs, lai jūs varētu redzēt, kas ir apstiprinātie kreditori līdz noteiktam datumam.</span><span class="sxs-lookup"><span data-stu-id="e2983-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="e2983-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2983-131">Close the page.</span></span>
17. <span data-ttu-id="e2983-132">Darbību rūtī noklikšķiniet uz **Derīguma periods**.</span><span class="sxs-lookup"><span data-stu-id="e2983-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="e2983-133">Ievadiet datumu laukā **Rādīt kreditorus, kuriem beidzas derīguma termiņš**.</span><span class="sxs-lookup"><span data-stu-id="e2983-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="e2983-134">Šo lapu varat izmantot, lai identificētu kreditorus, kuru apstiprinājuma statuss beidzas pēc konkrēta datuma.</span><span class="sxs-lookup"><span data-stu-id="e2983-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="e2983-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2983-135">Close the page.</span></span>
20. <span data-ttu-id="e2983-136">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="e2983-136">Click **Edit**.</span></span>
21. <span data-ttu-id="e2983-137">Laukā **Apstiprināto kreditoru pārbaudes metode** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="e2983-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="e2983-138">Šajā laukā var izvēlēties, kam jānotiek, ja prece tiek pievienota pirkšanas pasūtījuma rindai, ja kreditors nav apstiprināts kreditors.</span><span class="sxs-lookup"><span data-stu-id="e2983-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="e2983-139">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e2983-139">Click **Save**.</span></span>
23. <span data-ttu-id="e2983-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2983-140">Close the page.</span></span>
24. <span data-ttu-id="e2983-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2983-141">Close the page.</span></span>
25. <span data-ttu-id="e2983-142">Navigācijas rūtī pārejiet uz **Pārejiet uz Moduļi > Sagāde un avoti > Kreditori > Kreditoru/krājumu saistības > Apstiprināto kreditoru saraksts pēc krājuma**.</span><span class="sxs-lookup"><span data-stu-id="e2983-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="e2983-143">Šī lapa sniedz pārskatu par visām precēm un apstiprinātajiem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="e2983-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="e2983-144">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2983-144">Close the page.</span></span>
27. <span data-ttu-id="e2983-145">Navigācijas rūtī dodieties uz **Moduļi > Sagāde un avoti > Kreditori > Visi kreditori**.</span><span class="sxs-lookup"><span data-stu-id="e2983-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="e2983-146">Jūs varat arī sākt no kreditora, un pēc tam pāriet uz šī kreditora konta apstiprināto preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="e2983-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="e2983-147">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e2983-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="e2983-148">Darbību rūtī noklikšķiniet uz **Sagāde**.</span><span class="sxs-lookup"><span data-stu-id="e2983-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="e2983-149">Noklikšķiniet uz **Apstiprināto piegādātāju saraksts pēc kreditora**.</span><span class="sxs-lookup"><span data-stu-id="e2983-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="e2983-150">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2983-150">Close the page.</span></span>
32. <span data-ttu-id="e2983-151">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e2983-151">Close the page.</span></span>

