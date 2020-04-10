---
title: Algas procesa iespējošana laikam un apmeklētībai
description: Šajā procedūrā ir parādīts, kā iespējot algu procesu attiecībā uz laiku un apmeklētību.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2df4695b796b4e96e01fe5dac538b344cb76b910
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146725"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="90232-103">Algas procesa iespējošana laikam un apmeklētībai</span><span class="sxs-lookup"><span data-stu-id="90232-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90232-104">Šajā procedūrā ir parādīts, kā iespējot algu procesu attiecībā uz laiku un apmeklētību.</span><span class="sxs-lookup"><span data-stu-id="90232-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="90232-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="90232-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="90232-106">Izveidot apmaksas tipu ar saistītu apmaksas likmi</span><span class="sxs-lookup"><span data-stu-id="90232-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="90232-107">Laiks un apmeklētība > Iestatījumi > Alga > Apmaksas veidi</span><span class="sxs-lookup"><span data-stu-id="90232-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="90232-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="90232-108">Click New.</span></span>
3. <span data-ttu-id="90232-109">Laukā Apmaksas tips ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="90232-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="90232-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="90232-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="90232-111">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="90232-111">Click Save.</span></span>
6. <span data-ttu-id="90232-112">Noklikšķiniet uz Likmes.</span><span class="sxs-lookup"><span data-stu-id="90232-112">Click Rates.</span></span>
    * <span data-ttu-id="90232-113">Apmaksas tipu likmes tiek iestatītas noteiktiem laika intervāliem, un darbiniekiem var izveidot individuālas likmes.</span><span class="sxs-lookup"><span data-stu-id="90232-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="90232-114">Ne vienmēr ir nepieciešams apmaksas tipu likmes izveidot laikam un apmeklētībai.</span><span class="sxs-lookup"><span data-stu-id="90232-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="90232-115">Šī informācija var jau pastāvēt algu sistēmā, kas tiek lietota algu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="90232-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="90232-116">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="90232-116">Click New.</span></span>
8. <span data-ttu-id="90232-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="90232-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="90232-118">Lauka Likme ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="90232-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="90232-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="90232-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="90232-120">Apmaksas līguma izveide</span><span class="sxs-lookup"><span data-stu-id="90232-120">Create a pay agreement</span></span>
1. <span data-ttu-id="90232-121">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90232-121">Close the page.</span></span>
2. <span data-ttu-id="90232-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90232-122">Close the page.</span></span>
3. <span data-ttu-id="90232-123">Dodieties uz Apmaksas līgumi.</span><span class="sxs-lookup"><span data-stu-id="90232-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="90232-124">Laiks un apmeklētība > Iestatījumi > Apmaksas līgumi</span><span class="sxs-lookup"><span data-stu-id="90232-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="90232-125">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="90232-125">Click New.</span></span>
5. <span data-ttu-id="90232-126">Laukā Apmaksas līgums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="90232-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="90232-127">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="90232-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="90232-128">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="90232-128">Click Save.</span></span>
8. <span data-ttu-id="90232-129">Noklikšķiniet uz Līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="90232-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="90232-130">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="90232-130">Click New.</span></span>
10. <span data-ttu-id="90232-131">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="90232-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="90232-132">Laukā Profila tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="90232-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="90232-133">Laukā Apmaksas tips ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="90232-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="90232-134">Iestatīt apmaksas līgumu laika un reģistrācijas darbiniekam</span><span class="sxs-lookup"><span data-stu-id="90232-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="90232-135">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90232-135">Close the page.</span></span>
2. <span data-ttu-id="90232-136">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90232-136">Close the page.</span></span>
3. <span data-ttu-id="90232-137">Dodieties uz Laika reģistrācijas darbinieki.</span><span class="sxs-lookup"><span data-stu-id="90232-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="90232-138">Laiks un apmeklētība > Iestatījumi > Laika reģistrācijas darbinieki</span><span class="sxs-lookup"><span data-stu-id="90232-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="90232-139">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="90232-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="90232-140">Noklikšķiniet uz cilnes Nodarbinātība.</span><span class="sxs-lookup"><span data-stu-id="90232-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="90232-141">Izvērsiet sadaļu Laika reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="90232-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="90232-142">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="90232-142">Click Edit.</span></span>
8. <span data-ttu-id="90232-143">Laukā Apmaksas līgums ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="90232-143">In the Pay agreement field, enter or select a value.</span></span>

