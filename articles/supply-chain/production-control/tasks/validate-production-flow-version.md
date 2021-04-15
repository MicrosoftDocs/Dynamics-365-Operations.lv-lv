---
title: Ražošanas plūsmas un versijas pārbaude
description: Šajā procedūrā tiek parādīts, kā izveidot Lean ražošanā jaunu ražošanas plūsmu un pirmo versiju.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b46e3983cc95062e1c2073bb649f60df64807b99
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810986"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="74773-103">Ražošanas plūsmas un versijas pārbaude</span><span class="sxs-lookup"><span data-stu-id="74773-103">Validate a production flow and version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74773-104">Šajā procedūrā tiek parādīts, kā izveidot Lean ražošanā jaunu ražošanas plūsmu un pirmo versiju.</span><span class="sxs-lookup"><span data-stu-id="74773-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="74773-105">Priekšnosacījumi: ir jādefinē Lean ražošanas parametrus un klases laika mērvienības.</span><span class="sxs-lookup"><span data-stu-id="74773-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="74773-106">Jums arī ir nepieciešams definēt Vērtību plūsmu un Ražošanas uzdevumu grupu.</span><span class="sxs-lookup"><span data-stu-id="74773-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="74773-107">Skatiet tehniskos dokumentus par Lean ražošanas procesu, lai iepazītos ar ražošanas plūsmu un aktivitāšu koncepciju.</span><span class="sxs-lookup"><span data-stu-id="74773-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="74773-108">Šī procedūra attiecas uz juridisko personu USMF demonstrācijas datos.</span><span class="sxs-lookup"><span data-stu-id="74773-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="74773-109">Tomēr, pieņemot, ka juridiskā persona ir konfigurēta Lean ražošanas procesā, var izmantot citas juridiskas personas.</span><span class="sxs-lookup"><span data-stu-id="74773-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="74773-110">Ražošanas plūsmas izveide</span><span class="sxs-lookup"><span data-stu-id="74773-110">Create a production flow</span></span>
1. <span data-ttu-id="74773-111">Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Lean ražošanas plūsma > Ražošanas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="74773-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="74773-112">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="74773-112">Click New.</span></span>
3. <span data-ttu-id="74773-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="74773-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="74773-114">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="74773-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="74773-115">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="74773-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="74773-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="74773-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="74773-117">Vērtību plūsma ir pārvaldības struktūrvienība, kas aptver visas vērtību plūsmas darbības un plūsmas.</span><span class="sxs-lookup"><span data-stu-id="74773-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="74773-118">Šajā posmā pārvaldības struktūrvienības ir ierobežotas ar juridisku personu un tām nav papildu funkcionalitātes.</span><span class="sxs-lookup"><span data-stu-id="74773-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="74773-119">Laukā Ražošanas uzdevumu grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="74773-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="74773-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="74773-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="74773-121">Ražošanas uzdevumu grupas ļauj definēt materiālu, darbaspēku un NP kontu ražošanas procesam.</span><span class="sxs-lookup"><span data-stu-id="74773-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="74773-122">Lai saistītu uzskaites kontekstu ar ražošanas plūsmu, ir jāatlasa ražošanas uzdevumu grupa.</span><span class="sxs-lookup"><span data-stu-id="74773-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="74773-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="74773-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="74773-124">Ražošanas plūsmas versijas izveide</span><span class="sxs-lookup"><span data-stu-id="74773-124">Create a production flow version</span></span>
1. <span data-ttu-id="74773-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="74773-125">Click Add.</span></span>
2. <span data-ttu-id="74773-126">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="74773-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="74773-127">Versijas Beigu datumu var atjaunināt jebkurā laikā, pat aktīvām versijām.</span><span class="sxs-lookup"><span data-stu-id="74773-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="74773-128">Lietojiet versijas beigu datumu, lai plānotu versijas izslēgšanu.</span><span class="sxs-lookup"><span data-stu-id="74773-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="74773-129">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="74773-129">Click OK.</span></span>
4. <span data-ttu-id="74773-130">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="74773-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="74773-131">Laukā Mērvienība ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="74773-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="74773-132">Atlasiet Izgatavošanas laika vienība.</span><span class="sxs-lookup"><span data-stu-id="74773-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="74773-133">Laukā Vidējais izgatavošanas laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="74773-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="74773-134">Ražošanas plūsmas versijas izgatavošanas kontrolei definējiet mērķtiecīgo vidējo izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="74773-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="74773-135">Izgatavošana ir definēta kā daudzums noteiktā laika periodā.</span><span class="sxs-lookup"><span data-stu-id="74773-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="74773-136">Šajā piemērā izgatavošanas laiks ir 0,2 stundas uz 10 gabaliem.</span><span class="sxs-lookup"><span data-stu-id="74773-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="74773-137">8 stundu darba laikā tas atbilst dienas caurlaides jaudai 400 gabali.</span><span class="sxs-lookup"><span data-stu-id="74773-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="74773-138">Laukā Daudzums vienā ciklā ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="74773-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="74773-139">Izvērsiet vai sakļaujiet sadaļu Detalizēta informācija par versiju.</span><span class="sxs-lookup"><span data-stu-id="74773-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="74773-140">Laukā Minimālais izgatavošanas laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="74773-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="74773-141">Minimālajam izgatavošanas laikam jābūt mazākam par vai vienādam ar vidējo izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="74773-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="74773-142">Laukā Maksimālais izgatavošanas laiks ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="74773-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="74773-143">Maksimālajam izgatavošanas laikam jābūt augstākam par vai vienādam ar vidējo izgatavošanas laiku.</span><span class="sxs-lookup"><span data-stu-id="74773-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="74773-144">Ievadiet Faktiskā cikla laika perioda dienu skaitu.</span><span class="sxs-lookup"><span data-stu-id="74773-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="74773-145">Faktiskā cikla laika periods ir dienu skaits, kuru laikā darbi tiek apkopoti no faktiskās minūtes atpakaļ, lai aprēķinātu faktisko cikla laiku.</span><span class="sxs-lookup"><span data-stu-id="74773-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="74773-146">Vērtību var mainīt jebkurā brīdī un tā tiek izmantota tikai faktisko cikla laiku aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="74773-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="74773-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="74773-147">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]