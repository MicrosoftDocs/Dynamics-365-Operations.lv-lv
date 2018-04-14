--- 
title: "Piegādes"
description: "Šajā procedūrā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6e9ce934016139832b474d60d7dfc2e845434da2
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="d4e0b-103">Piegādes</span><span class="sxs-lookup"><span data-stu-id="d4e0b-103">Set up shipping carriers</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4e0b-104">Šajā procedūrā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="d4e0b-105">Transportēšanas koordinators pēc tam var piešķirt nosūtījuma pārvadātāju ienākošai vai izejošai kravai.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="d4e0b-106">Jauna nosūtījumu pārvadātāja izveide</span><span class="sxs-lookup"><span data-stu-id="d4e0b-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="d4e0b-107">Pārejiet uz sadaļu Transportēšanas pārvaldība > Iestatījumi > Pārvadātāji > Sūtījumu pārvadātāji.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="d4e0b-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-108">Click New.</span></span>
3. <span data-ttu-id="d4e0b-109">Ierakstiet vērtību laukā Sūtījumu pārvadātājs.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="d4e0b-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d4e0b-111">Laukā Režīms noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d4e0b-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d4e0b-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="d4e0b-114">Vispārējās informācijas ievade par nosūtījumu pārvadātāju</span><span class="sxs-lookup"><span data-stu-id="d4e0b-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="d4e0b-115">Pārslēdziet sadaļas Pārskats paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="d4e0b-116">Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas Aktivizēt nosūtīšanas pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="d4e0b-117">Laukā Kreditors noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d4e0b-118">Atlasiet kreditora kontu, kuram piešķirt nosūtījuma pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="d4e0b-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d4e0b-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d4e0b-121">Atlasiet opciju laukā Transportēšanas norēķinu veids.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="d4e0b-122">Atlasiet Manuāli, lai izmantotu transportēšanas norēķinu lapu, vai atlasiet EDI, lai atjauninātu norēķinus, izmantojot elektronisko datu apmaiņu (EDI).</span><span class="sxs-lookup"><span data-stu-id="d4e0b-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="d4e0b-123">Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas Aktivizēt pārvadātāja vērtējumu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="d4e0b-124">Nepieciešamo pakalpojumu izveide sūtījumu pārvadātājam</span><span class="sxs-lookup"><span data-stu-id="d4e0b-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="d4e0b-125">Pārslēdziet sadaļas Pakalpojumi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="d4e0b-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-126">Click New.</span></span>
3. <span data-ttu-id="d4e0b-127">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d4e0b-128">Ierakstiet vērtību laukā Pārvadātāja pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="d4e0b-129">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d4e0b-130">Laukā Transportēšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d4e0b-131">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d4e0b-132">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="d4e0b-133">Iestatiet pārvadātāja adresi (nav obligāti)</span><span class="sxs-lookup"><span data-stu-id="d4e0b-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="d4e0b-134">Pārslēdziet sadaļas Adreses izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="d4e0b-135">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-135">Click New.</span></span>
3. <span data-ttu-id="d4e0b-136">Laukā Nosaukums vai apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="d4e0b-137">Laukā Valsts/reģions noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d4e0b-138">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d4e0b-139">Laukā Pasta indekss noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d4e0b-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d4e0b-141">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d4e0b-142">Laukā Iela ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="d4e0b-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="d4e0b-144">Iestatiet nosūtījumu pārvadātāja novērtēšanas profilu</span><span class="sxs-lookup"><span data-stu-id="d4e0b-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="d4e0b-145">Pārslēdziet sadaļas Novērtējuma profili izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="d4e0b-146">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-146">Click New.</span></span>
3. <span data-ttu-id="d4e0b-147">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d4e0b-148">Ierakstiet vērtību laukā Novērtējuma profils.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="d4e0b-149">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d4e0b-150">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d4e0b-151">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d4e0b-152">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d4e0b-153">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="d4e0b-154">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="d4e0b-155">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d4e0b-156">Laukā Likmes noteikšanas programma noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d4e0b-157">Atlasiet likmes noteikšanas programmu, kura atbilst līgumam, kas jums noslēgts ar pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="d4e0b-158">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="d4e0b-159">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="d4e0b-160">Laukā Likmes šablons noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="d4e0b-161">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="d4e0b-162">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d4e0b-163">Laukā Tranzīta laika noteikšanas programma noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="d4e0b-164">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="d4e0b-165">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d4e0b-165">Click Save.</span></span>


