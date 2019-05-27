---
title: Piegādes
description: Šajā procedūrā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569106"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="0dd1c-103">Piegādes</span><span class="sxs-lookup"><span data-stu-id="0dd1c-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0dd1c-104">Šajā procedūrā parādīts, kā iestatīt nosūtījuma pārvadātāju un definēt tādu informāciju kā pakalpojums, piegādes režīms, transportēšanas norēķini, transportēšanas ierobežojumi un nosūtīšanas likme.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="0dd1c-105">Transportēšanas koordinators pēc tam var piešķirt nosūtījuma pārvadātāju ienākošai vai izejošai kravai.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="0dd1c-106">Jauna nosūtījumu pārvadātāja izveide</span><span class="sxs-lookup"><span data-stu-id="0dd1c-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="0dd1c-107">Pārejiet uz sadaļu Transportēšanas pārvaldība > Iestatījumi > Pārvadātāji > Sūtījumu pārvadātāji.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="0dd1c-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-108">Click New.</span></span>
3. <span data-ttu-id="0dd1c-109">Ierakstiet vērtību laukā Sūtījumu pārvadātājs.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="0dd1c-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0dd1c-111">Laukā Režīms noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0dd1c-112">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0dd1c-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="0dd1c-114">Vispārējās informācijas ievade par nosūtījumu pārvadātāju</span><span class="sxs-lookup"><span data-stu-id="0dd1c-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="0dd1c-115">Pārslēdziet sadaļas Pārskats paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="0dd1c-116">Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas Aktivizēt nosūtīšanas pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="0dd1c-117">Laukā Kreditors noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0dd1c-118">Atlasiet kreditora kontu, kuram piešķirt nosūtījuma pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="0dd1c-119">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0dd1c-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0dd1c-121">Atlasiet opciju laukā Transportēšanas norēķinu veids.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="0dd1c-122">Atlasiet Manuāli, lai izmantotu transportēšanas norēķinu lapu, vai atlasiet EDI, lai atjauninātu norēķinus, izmantojot elektronisko datu apmaiņu (EDI).</span><span class="sxs-lookup"><span data-stu-id="0dd1c-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="0dd1c-123">Atzīmējiet vai noņemiet atzīmi no izvēles rūtiņas Aktivizēt pārvadātāja vērtējumu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="0dd1c-124">Nepieciešamo pakalpojumu izveide sūtījumu pārvadātājam</span><span class="sxs-lookup"><span data-stu-id="0dd1c-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="0dd1c-125">Pārslēdziet sadaļas Pakalpojumi paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="0dd1c-126">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-126">Click New.</span></span>
3. <span data-ttu-id="0dd1c-127">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0dd1c-128">Ierakstiet vērtību laukā Pārvadātāja pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="0dd1c-129">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0dd1c-130">Laukā Transportēšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0dd1c-131">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0dd1c-132">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="0dd1c-133">Iestatiet pārvadātāja adresi (nav obligāti)</span><span class="sxs-lookup"><span data-stu-id="0dd1c-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="0dd1c-134">Pārslēdziet sadaļas Adreses izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="0dd1c-135">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-135">Click New.</span></span>
3. <span data-ttu-id="0dd1c-136">Laukā Nosaukums vai apraksts ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="0dd1c-137">Laukā Valsts/reģions noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0dd1c-138">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0dd1c-139">Laukā Pasta indekss noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0dd1c-140">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0dd1c-141">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0dd1c-142">Laukā Iela ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="0dd1c-143">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="0dd1c-144">Iestatiet nosūtījumu pārvadātāja novērtēšanas profilu</span><span class="sxs-lookup"><span data-stu-id="0dd1c-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="0dd1c-145">Pārslēdziet sadaļas Novērtējuma profili izvēršanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="0dd1c-146">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-146">Click New.</span></span>
3. <span data-ttu-id="0dd1c-147">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0dd1c-148">Ierakstiet vērtību laukā Novērtējuma profils.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="0dd1c-149">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0dd1c-150">Laukā Vieta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0dd1c-151">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0dd1c-152">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0dd1c-153">Laukā Noliktava noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0dd1c-154">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="0dd1c-155">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="0dd1c-156">Laukā Likmes noteikšanas programma noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0dd1c-157">Atlasiet likmes noteikšanas programmu, kura atbilst līgumam, kas jums noslēgts ar pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="0dd1c-158">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="0dd1c-159">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="0dd1c-160">Laukā Likmes šablons noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="0dd1c-161">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="0dd1c-162">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="0dd1c-163">Laukā Tranzīta laika noteikšanas programma noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="0dd1c-164">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="0dd1c-165">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0dd1c-165">Click Save.</span></span>

