---
title: Ražošanas plūsmas versijas izveide
description: Šī procedūra ir vērsta uz to, lai izveidotu jaunu ražošanas plūsmas versiju.
author: cvocph
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a4b4847046af541644338157d95e6fcba315f9c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828998"
---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="bac74-103">Ražošanas plūsmas versijas izveide</span><span class="sxs-lookup"><span data-stu-id="bac74-103">Create a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bac74-104">Šī procedūra ir vērsta uz to, lai izveidotu jaunu ražošanas plūsmas versiju.</span><span class="sxs-lookup"><span data-stu-id="bac74-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="bac74-105">Lai veiktu šo procedūru, ir jādefinē lean manufacturing ražošanas uzdevuma parametrus un klases laika mērvienības.</span><span class="sxs-lookup"><span data-stu-id="bac74-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="bac74-106">Jums arī ir nepieciešams definēt vērtību plūsmu un ražošanas uzdevumu grupu.</span><span class="sxs-lookup"><span data-stu-id="bac74-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="bac74-107">Lai uzzinātu vairāk par lean manufacturing ražošanas plūsmām un darbībām, skatiet tehniskos dokumentus par Lean manufacturing programmai Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="bac74-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="bac74-108">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="bac74-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="bac74-109">Ražošanas plūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="bac74-109">Create a production flow</span></span>
1. <span data-ttu-id="bac74-110">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="bac74-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="bac74-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="bac74-111">Click New.</span></span>
3. <span data-ttu-id="bac74-112">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="bac74-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="bac74-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bac74-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bac74-114">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="bac74-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bac74-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="bac74-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bac74-116">Atlasiet pārvaldības struktūrvienību ar tipu vērtību plūsma.</span><span class="sxs-lookup"><span data-stu-id="bac74-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="bac74-117">Vērtību plūsma ir pārvaldības struktūrvienība, kas aptver visas vērtību plūsmas darbības un plūsmas.</span><span class="sxs-lookup"><span data-stu-id="bac74-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="bac74-118">Šajā posmā pārvaldības struktūrvienības ir ierobežotas ar juridisku personu un tām nav papildu funkcionalitātes.</span><span class="sxs-lookup"><span data-stu-id="bac74-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="bac74-119">Laukā Ražošanas uzdevumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="bac74-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bac74-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="bac74-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bac74-121">Atlasiet ražošanas plūsmai ražošanas uzdevumu grupu.</span><span class="sxs-lookup"><span data-stu-id="bac74-121">Select a production group for the production flow.</span></span> <span data-ttu-id="bac74-122">Ražošanas uzdevumu grupas ļauj definēt materiālu, darbaspēku un NP kontu ražošanas procesam.</span><span class="sxs-lookup"><span data-stu-id="bac74-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="bac74-123">Lai saistītu uzskaites kontekstu ar ražošanas plūsmu, ir jāatlasa ražošanas uzdevumu grupa.</span><span class="sxs-lookup"><span data-stu-id="bac74-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="bac74-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="bac74-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="bac74-125">Ražošanas plūsmas versijas izveide</span><span class="sxs-lookup"><span data-stu-id="bac74-125">Create a production flow version</span></span>
1. <span data-ttu-id="bac74-126">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="bac74-126">Click Add.</span></span>
2. <span data-ttu-id="bac74-127">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="bac74-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="bac74-128">Ja nepieciešams, nosakiet versijas beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="bac74-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="bac74-129">To var atjaunināt jebkurā brīdī, pat aktīvām versijām.</span><span class="sxs-lookup"><span data-stu-id="bac74-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="bac74-130">To var izmantot, lai plānotu versijas izslēgšanu.</span><span class="sxs-lookup"><span data-stu-id="bac74-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="bac74-131">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="bac74-131">Click OK.</span></span>
4. <span data-ttu-id="bac74-132">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="bac74-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="bac74-133">Laukā Mērvienība ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="bac74-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="bac74-134">Atrisināt maina izgatavošanas vienību.</span><span class="sxs-lookup"><span data-stu-id="bac74-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="bac74-135">Laukā Vidējais izgatavošanas laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="bac74-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="bac74-136">Nosakiet versijas vidējo izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="bac74-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="bac74-137">Ražošanas plūsmas versijas izgatavošanas kontrolei definējiet mērķtiecīgo vidējo izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="bac74-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="bac74-138">Izgatavošana ir definēta kā daudzums noteiktā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="bac74-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="bac74-139">Piemēram, izgatavošanas laiks ir 0,2 stundas uz 10 gabaliem.</span><span class="sxs-lookup"><span data-stu-id="bac74-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="bac74-140">8 stundu darba laikā tas atbilst dienas caurlaides jaudai 400 gabali.</span><span class="sxs-lookup"><span data-stu-id="bac74-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="bac74-141">Laukā Daudzums vienā ciklā ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="bac74-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="bac74-142">Definējiet daudzumu vienā ciklā, kas saistīts ar vidējo izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="bac74-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="bac74-143">Pārslēdziet sadaļas Detalizēta informācija par versiju paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="bac74-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="bac74-144">Laukā Minimālais izgatavošanas laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="bac74-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="bac74-145">Nosakiet minimālo izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="bac74-145">Define the minimum takt time.</span></span> <span data-ttu-id="bac74-146">Minimālajam izgatavošanas laikam jābūt mazākam par vai vienādam ar vidējo izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="bac74-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="bac74-147">Laukā Maksimālais izgatavošanas laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="bac74-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="bac74-148">Maksimālajam izgatavošanas laikam jābūt augstākam par vai vienādam ar vidējo izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="bac74-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="bac74-149">Laukā Faktiskā cikla laika periods (dienas) ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="bac74-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="bac74-150">Ievadiet Faktiskā cikla laika perioda dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="bac74-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="bac74-151">Faktiskā cikla laika periods ir dienu skaits, kuru laikā darbi tiek apkopoti no faktiskās minūtes atpakaļ, lai aprēķinātu faktisko cikla laiku.</span><span class="sxs-lookup"><span data-stu-id="bac74-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="bac74-152">Vērtību var mainīt jebkurā brīdī un tā tiek izmantota tikai faktisko cikla laiku aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="bac74-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="bac74-153">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="bac74-153">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]