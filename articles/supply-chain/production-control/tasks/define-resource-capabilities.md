--- 
title: "Resursu iespēju definēšana"
description: "Resursu iespējas apraksta, kādas operācijas šie resursi var paveikt."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: aa24d9506b8d044679403039e9c659a1ebbd2d5d
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="define-resource-capabilities"></a><span data-ttu-id="04d0b-103">Resursu iespēju definēšana</span><span class="sxs-lookup"><span data-stu-id="04d0b-103">Define resource capabilities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04d0b-104">Resursu iespējas apraksta, kādas operācijas šie resursi var paveikt.</span><span class="sxs-lookup"><span data-stu-id="04d0b-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="04d0b-105">Plānošanas laikā katra darba un operācijas prasības ir jāsaskaņo ar pieejamo resursu iespējām.</span><span class="sxs-lookup"><span data-stu-id="04d0b-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="04d0b-106">Šis uzdevuma ceļvedis jums palīdzēs izveidot resursa iespēju un piešķirt to kādam resursam.</span><span class="sxs-lookup"><span data-stu-id="04d0b-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="04d0b-107">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="04d0b-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="04d0b-108">Resursa iespējas veidošana</span><span class="sxs-lookup"><span data-stu-id="04d0b-108">Create a resource capability</span></span>
1. <span data-ttu-id="04d0b-109">Dodieties uz Resursu iespējas.</span><span class="sxs-lookup"><span data-stu-id="04d0b-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="04d0b-110">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="04d0b-110">Click New.</span></span>
3. <span data-ttu-id="04d0b-111">Laukā Iespēja ierakstiet resursa iespējas ID.</span><span class="sxs-lookup"><span data-stu-id="04d0b-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="04d0b-112">Katrai operācijai varat izmantot iespējas ID, lai norādītu, ka resursiem ir nepieciešama šī iespēja, lai varētu izpildīt operāciju.</span><span class="sxs-lookup"><span data-stu-id="04d0b-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="04d0b-113">Laukā Apraksts ievadiet iespējas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="04d0b-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="04d0b-114">Piešķirt iespēju resursam</span><span class="sxs-lookup"><span data-stu-id="04d0b-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="04d0b-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="04d0b-115">Click Add.</span></span>
2. <span data-ttu-id="04d0b-116">Laukā Resurss ierakstiet resursa ID.</span><span class="sxs-lookup"><span data-stu-id="04d0b-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="04d0b-117">Resursa iespēju var piešķirt vienam vai vairākiem resursiem.</span><span class="sxs-lookup"><span data-stu-id="04d0b-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="04d0b-118">Laukā Termiņa beigas ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="04d0b-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="04d0b-119">Šo lauku varat izmantot, lai norādītu, ka resursam iespēja ir tikai ierobežotu laiku.</span><span class="sxs-lookup"><span data-stu-id="04d0b-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="04d0b-120">Laukā Prioritāte ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="04d0b-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="04d0b-121">Kad plānojat darbus un operācijas, varat norādīt, vai resursi ir jāatlasa pēc prioritātes.</span><span class="sxs-lookup"><span data-stu-id="04d0b-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="04d0b-122">Ja izvēlaties to darīt un līdz pieprasītajam datumam attiecīgo darbu vai operāciju var izpildīt vairāki resursi, tad tiek atlasīts resurss, kuram ir viszemākā prioritāte attiecībā uz nepieciešamo iespēju.</span><span class="sxs-lookup"><span data-stu-id="04d0b-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="04d0b-123">Laukā Līmenis ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="04d0b-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="04d0b-124">Ja norādāt, ka darbam vai operācijai ir nepieciešama īpaša iespēja, varat arī norādīt minimālo nepieciešamo līmeni.</span><span class="sxs-lookup"><span data-stu-id="04d0b-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="04d0b-125">Izmantojiet iespēju līmeni, lai atšķirtu resursus, kas var izpildīt to pašu darbu, bet ar atšķirīgu ātrumu, jaudu, izmēriem un citiem faktoriem.</span><span class="sxs-lookup"><span data-stu-id="04d0b-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  


