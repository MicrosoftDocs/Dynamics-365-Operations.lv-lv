--- 
title: "Kanban daudzuma ieteikumu aprēķins"
description: "Šajā procedūrā parādīts, kā optimizēt Kanban lielumu un daudzumu konkrētam Kanban nosacījumam, izmantojot Kanban daudzuma aprēķinus."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a817dbc02890d863f68c5bf2a6cc11b9a5328060
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="38681-103">Kanban daudzuma ieteikumu aprēķins</span><span class="sxs-lookup"><span data-stu-id="38681-103">Calculate kanban quantity suggestions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38681-104">Šajā procedūrā parādīts, kā optimizēt Kanban lielumu un daudzumu konkrētam Kanban nosacījumam, izmantojot Kanban daudzuma aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="38681-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="38681-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="38681-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="38681-106">Šī procedūra ir paredzēta vērtību plūsmas pārvaldniekam.</span><span class="sxs-lookup"><span data-stu-id="38681-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="38681-107">Šīs procedūras priekšnosacījums ir paveikta procedūra Jaunas Kanban daudzuma aprēķināšanas politikas pievienošana Kanban nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="38681-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="38681-108">Kanban daudzuma aprēķina izveide</span><span class="sxs-lookup"><span data-stu-id="38681-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="38681-109">Pārejiet uz sadaļu Ražošanas kontrole > Periodiskie uzdevumi > Kanban daudzuma aprēķins > Aprēķināt Kanban daudzumu.</span><span class="sxs-lookup"><span data-stu-id="38681-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="38681-110">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="38681-110">Click New.</span></span>
3. <span data-ttu-id="38681-111">Laukā Nosaukums ierakstiet Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="38681-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="38681-112">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="38681-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="38681-113">Atlasiet politiku, ko izveidojāt procedūrā Jaunas Kanban daudzuma aprēķināšanas politikas pievienošana Kanban nosacījumam.</span><span class="sxs-lookup"><span data-stu-id="38681-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="38681-114">Piemēram, Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="38681-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="38681-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="38681-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="38681-116">Laukā Nosacījums aktīvs no datuma iestatiet datumu un laiku 2012-12-17T08:00:00'.</span><span class="sxs-lookup"><span data-stu-id="38681-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="38681-117">Šis datums tiek izmantots, lai noteiktu, kuri fiksētie Kanban nosacījumi ir ietverti Kanban daudzuma aprēķinos.</span><span class="sxs-lookup"><span data-stu-id="38681-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="38681-118">Laukā Izpildītā pieprasījuma perioda sākuma datums iestatiet datumu un laiku 2012-11-17T09:00:00.</span><span class="sxs-lookup"><span data-stu-id="38681-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="38681-119">Datums, no kura tiek iekļauti pagātnes pieprasījuma darījumi, lai aprēķinātu Kanban daudzumu.</span><span class="sxs-lookup"><span data-stu-id="38681-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="38681-120">Laukā Izpildītā pieprasījuma perioda beigu datums iestatiet datumu un laiku 2012-12-17T07:59:59.</span><span class="sxs-lookup"><span data-stu-id="38681-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="38681-121">Datums, līdz kuram pagātnes pieprasījuma darījumi tiek iekļauti, lai aprēķinātu Kanban daudzumu.</span><span class="sxs-lookup"><span data-stu-id="38681-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="38681-122">Laukā Pieprasījuma perioda sākuma datums iestatiet datumu un laiku 2012-12-17T08:00:00.</span><span class="sxs-lookup"><span data-stu-id="38681-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="38681-123">Datums, no kura tiek iekļauti pašreizējie pieprasījuma darījumi, lai aprēķinātu Kanban daudzumu.</span><span class="sxs-lookup"><span data-stu-id="38681-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="38681-124">Laukā Pieprasījuma perioda beigu datums iestatiet datumu un laiku 2013-01-16T07:59:59.</span><span class="sxs-lookup"><span data-stu-id="38681-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="38681-125">Datums, līdz kuram tiek iekļauti pašreizējie pieprasījuma darījumi, lai aprēķinātu Kanban daudzumu.</span><span class="sxs-lookup"><span data-stu-id="38681-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="38681-126">Kanban daudzuma priekšlikuma ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="38681-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="38681-127">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="38681-127">Click Save.</span></span>
2. <span data-ttu-id="38681-128">Noklikšķiniet uz Ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="38681-128">Click Generate.</span></span>
    * <span data-ttu-id="38681-129">Tas ģenerē Kanban daudzuma priekšlikuma rindu Kanban nosacījumam 000020.</span><span class="sxs-lookup"><span data-stu-id="38681-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="38681-130">Kanban daudzuma aprēķināšanas izpilde</span><span class="sxs-lookup"><span data-stu-id="38681-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="38681-131">Noklikšķiniet uz Aprēķināt.</span><span class="sxs-lookup"><span data-stu-id="38681-131">Click Calculate.</span></span>
    * <span data-ttu-id="38681-132">Tas aprēķina Kanban daudzuma priekšlikumu.</span><span class="sxs-lookup"><span data-stu-id="38681-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="38681-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="38681-133">Click OK.</span></span>
3. <span data-ttu-id="38681-134">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="38681-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="38681-135">Ievērojiet, ka ieteicamais Kanban daudzums ir 2.</span><span class="sxs-lookup"><span data-stu-id="38681-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="38681-136">Preču daudzuma maiņa un atkārtots aprēķins</span><span class="sxs-lookup"><span data-stu-id="38681-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="38681-137">Iestatiet vērtību 5 laikā Preču daudzums.</span><span class="sxs-lookup"><span data-stu-id="38681-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="38681-138">Noklikšķiniet uz Aprēķināt.</span><span class="sxs-lookup"><span data-stu-id="38681-138">Click Calculate.</span></span>
3. <span data-ttu-id="38681-139">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="38681-139">Click OK.</span></span>
    * <span data-ttu-id="38681-140">Ievērojiet, ka ar Kanban daudzumu 5, ieteikums tiek mainīts uz Kanban daudzumu 4.</span><span class="sxs-lookup"><span data-stu-id="38681-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="38681-141">To ietekmē fakts, ka ar zemāku preču daudzumu nepieciešams vairāk Kanban sistēmu, lai apmierinātu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="38681-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="38681-142">Kanban nosacījuma atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="38681-142">Update kanban rule</span></span>
1. <span data-ttu-id="38681-143">Laukā Nosacījuma spēkā stāšanās datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="38681-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="38681-144">Iestatiet nākotnes datumu laukā Nosacījums aktīvs no datuma.</span><span class="sxs-lookup"><span data-stu-id="38681-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="38681-145">Piemēram, šodiena + viens gads.</span><span class="sxs-lookup"><span data-stu-id="38681-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="38681-146">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="38681-146">Click Update.</span></span>
3. <span data-ttu-id="38681-147">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="38681-147">Click OK.</span></span>
4. <span data-ttu-id="38681-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="38681-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="38681-149">Kanban nosacījuma izmaiņu pārbaude</span><span class="sxs-lookup"><span data-stu-id="38681-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="38681-150">Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="38681-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="38681-151">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="38681-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="38681-152">Atlasiet Kanban nosacījumu, kas tika izveidots iepriekšējā apakšuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="38681-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="38681-153">Tam būtu jābūt pirmajam Kanban nosacījumam sarakstā, kad tas sakārtots pēc numura.</span><span class="sxs-lookup"><span data-stu-id="38681-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="38681-154">Pārslēdziet sadaļas Detalizēti paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="38681-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="38681-155">Ievērojiet spēkā stāšanās datumu, kas nozīmē, ka šis nosacījums līdz šim datumam nav aktivizēts.</span><span class="sxs-lookup"><span data-stu-id="38681-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="38681-156">Pārslēdziet sadaļas Daudzumi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="38681-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="38681-157">Ņemiet vērā, ka tas ir noklusētais daudzums, kuru ievadījāt Kanban daudzuma aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="38681-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="38681-158">Ņemiet vērā, ka 4 ir fiksētais Kanban daudzums, kas noteikts Kanban daudzuma aprēķinā.</span><span class="sxs-lookup"><span data-stu-id="38681-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="38681-159">Noklikšķiniet uz cilnes ListPanel.</span><span class="sxs-lookup"><span data-stu-id="38681-159">Click the ListPanel tab.</span></span>


