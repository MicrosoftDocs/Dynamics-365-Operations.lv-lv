--- 
title: "Algas procesa iespējošana laikam un apmeklētībai"
description: "Šajā procedūrā ir parādīts, kā iespējot algu procesu attiecībā uz laiku un apmeklētību."
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 22ce633f65847f10fbe507b71bfc2bb33f595501
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="3472e-103">Algas procesa iespējošana laikam un apmeklētībai</span><span class="sxs-lookup"><span data-stu-id="3472e-103">Enable the payroll process for time and attendance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3472e-104">Šajā procedūrā ir parādīts, kā iespējot algu procesu attiecībā uz laiku un apmeklētību.</span><span class="sxs-lookup"><span data-stu-id="3472e-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="3472e-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="3472e-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="3472e-106">Izveidot apmaksas tipu ar saistītu apmaksas likmi</span><span class="sxs-lookup"><span data-stu-id="3472e-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="3472e-107">Laiks un apmeklētība > Iestatījumi > Alga > Apmaksas veidi</span><span class="sxs-lookup"><span data-stu-id="3472e-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="3472e-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3472e-108">Click New.</span></span>
3. <span data-ttu-id="3472e-109">Laukā Apmaksas tips ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3472e-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="3472e-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3472e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3472e-111">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3472e-111">Click Save.</span></span>
6. <span data-ttu-id="3472e-112">Noklikšķiniet uz Likmes.</span><span class="sxs-lookup"><span data-stu-id="3472e-112">Click Rates.</span></span>
    * <span data-ttu-id="3472e-113">Apmaksas tipu likmes tiek iestatītas noteiktiem laika intervāliem, un darbiniekiem var izveidot individuālas likmes.</span><span class="sxs-lookup"><span data-stu-id="3472e-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="3472e-114">Ne vienmēr ir nepieciešams apmaksas tipu likmes izveidot laikam un apmeklētībai.</span><span class="sxs-lookup"><span data-stu-id="3472e-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="3472e-115">Šī informācija var jau pastāvēt algu sistēmā, kas tiek lietota algu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="3472e-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="3472e-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3472e-116">Click New.</span></span>
8. <span data-ttu-id="3472e-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3472e-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3472e-118">Lauka Likme ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="3472e-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="3472e-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3472e-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="3472e-120">Apmaksas līguma izveide</span><span class="sxs-lookup"><span data-stu-id="3472e-120">Create a pay agreement</span></span>
1. <span data-ttu-id="3472e-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3472e-121">Close the page.</span></span>
2. <span data-ttu-id="3472e-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3472e-122">Close the page.</span></span>
3. <span data-ttu-id="3472e-123">Dodieties uz Apmaksas līgumi.</span><span class="sxs-lookup"><span data-stu-id="3472e-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="3472e-124">Laiks un apmeklētība > Iestatījumi > Apmaksas līgumi</span><span class="sxs-lookup"><span data-stu-id="3472e-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="3472e-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3472e-125">Click New.</span></span>
5. <span data-ttu-id="3472e-126">Laukā Apmaksas līgums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3472e-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="3472e-127">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3472e-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="3472e-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3472e-128">Click Save.</span></span>
8. <span data-ttu-id="3472e-129">Noklikšķiniet uz Līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="3472e-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="3472e-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="3472e-130">Click New.</span></span>
10. <span data-ttu-id="3472e-131">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3472e-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="3472e-132">Laukā Profila tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3472e-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="3472e-133">Laukā Apmaksas tips ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="3472e-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="3472e-134">Iestatīt apmaksas līgumu laika un reģistrācijas darbiniekam</span><span class="sxs-lookup"><span data-stu-id="3472e-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="3472e-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3472e-135">Close the page.</span></span>
2. <span data-ttu-id="3472e-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3472e-136">Close the page.</span></span>
3. <span data-ttu-id="3472e-137">Dodieties uz Laika reģistrācijas darbinieki.</span><span class="sxs-lookup"><span data-stu-id="3472e-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="3472e-138">Laiks un apmeklētība > Iestatījumi > Laika reģistrācijas darbinieki</span><span class="sxs-lookup"><span data-stu-id="3472e-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="3472e-139">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3472e-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3472e-140">Noklikšķiniet uz cilnes Nodarbinātība.</span><span class="sxs-lookup"><span data-stu-id="3472e-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="3472e-141">Izvērsiet sadaļu Laika reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="3472e-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="3472e-142">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="3472e-142">Click Edit.</span></span>
8. <span data-ttu-id="3472e-143">Laukā Apmaksas līgums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3472e-143">In the Pay agreement field, enter or select a value.</span></span>


