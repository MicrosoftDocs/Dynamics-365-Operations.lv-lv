---
title: Pakalpojumu intervāli
description: Pakalpojumu intervāls norāda biežumu, ar kādu pakalpojuma pasūtījuma rindas tiek izveidotas pakalpojumu līguma rindām, kad veidojat pakalpojumu pasūtījumus.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1027a6a1ddb1057ba039382d394522d6f9538a90
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432866"
---
# <a name="service-intervals"></a><span data-ttu-id="a2d1e-103">Pakalpojumu intervāli</span><span class="sxs-lookup"><span data-stu-id="a2d1e-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2d1e-104">Pakalpojumu līgumu intervāls norāda biežumu, ar kādu pakalpojuma pasūtījuma rindas tiek izveidotas pakalpojumu līguma rindām, kad automātiski veidojat pakalpojumu pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="a2d1e-105">Kad jūs veidojat pakalpojumu pasūtījumus automātiski, pakalpojuma pasūtījuma rindas tiek veidotas atbilstoši intervālam, kuru esat norādījuši pakalpojumu pasūtījuma rindai no vienošanās rindas sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="a2d1e-106">Ja pakalpojumu līguma rindas lauks **Intervāls** lapā **Pakalpojumu līgumi** ir tukšs, rinda ir vienreizējs notikums un netiek lietota, lai izveidotu pakalpojumu pasūtījumus atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="a2d1e-107">Paraugs</span><span class="sxs-lookup"><span data-stu-id="a2d1e-107">Example</span></span>

<span data-ttu-id="a2d1e-108">Šis piemērs parāda, kā pakalpojumu intervāls ietekmēs pakalpojumu līguma rindas un pakalpojuma pasūtījuma rindas pakalpojuma pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="a2d1e-109">Pakalpojumu līguma izveide</span><span class="sxs-lookup"><span data-stu-id="a2d1e-109">Create a service agreement</span></span>

<span data-ttu-id="a2d1e-110">Vispirms jūs izveidojat pakalpojumu līgumu un opcijai **Kombinēt pakalpojumu pasūtījumus** iestatāt vērtību **Pēc pakalpojumu līguma**.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="a2d1e-111">Noklikšķiniet uz **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="a2d1e-112">**Darbību rūtī** cilnē **Pakalpojumu līgums** grupā **Jauns** noklikšķiniet uz **Pakalpojumu līgums**, lai izveidotu jaunu pakalpojumu līgumu.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="a2d1e-113">Ievadiet aprakstu, atlasiet projekta lauku **Projekta ID** un ievadiet datumu laukā **Sākuma datums**.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="a2d1e-114">Laukā **Kombinēt pakalpojumu pasūtījumus** atlasiet **Pēc pakalpojumu līguma**.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="a2d1e-115">Tagad jūs esat izveidojuši sekojošo pakalpojumu līgumu:</span><span class="sxs-lookup"><span data-stu-id="a2d1e-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="a2d1e-116">Project</span><span class="sxs-lookup"><span data-stu-id="a2d1e-116">Project</span></span>      | <span data-ttu-id="a2d1e-117">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="a2d1e-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d1e-118">Jūsu projekts</span><span class="sxs-lookup"><span data-stu-id="a2d1e-118">Your project</span></span> | <span data-ttu-id="a2d1e-119">Norādītais projekta datums.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-119">The date you specified for the project.</span></span> <span data-ttu-id="a2d1e-120">Šajā piemērā tiek izmantots pašreizējais datums.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="a2d1e-121">Pakalpojumu līguma rindas izveide</span><span class="sxs-lookup"><span data-stu-id="a2d1e-121">Create a service agreement line</span></span>

<span data-ttu-id="a2d1e-122">Pēc tam izveidojiet pakalpojumu līguma rindu ar darbības tipu **Stunda**.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="a2d1e-123">Lai pabeigtu šo piemēra daļu, sadaļā **Pakalpojumu intervāli** izveidojiet 10 dienu pakalpojumu intervālu.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="a2d1e-124">Atlasiet tikko izveidoto pakalpojumu līgumu.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="a2d1e-125">Kopsavilkuma cilnē **Rindas** noklikšķiniet uz pogas **Pievienot**, lai izveidotu jaunu rindu lapas **Pakalpojumu līgumi** apakšdaļā.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="a2d1e-126">Laukā **Darbības tips** atlasiet **Stunda**.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="a2d1e-127">Laukā **Darbinieks** atlasiet darbinieku, kurš sniegs pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="a2d1e-128">Laukā **Pakalpojumu intervāls** atlasiet 10 dienu intervālu.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="a2d1e-129">Tagad jūs esat izveidojuši pakalpojumu līguma rindu ar šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="a2d1e-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="a2d1e-130">Darbības veids</span><span class="sxs-lookup"><span data-stu-id="a2d1e-130">Transaction type</span></span> | <span data-ttu-id="a2d1e-131">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="a2d1e-131">Start date</span></span>                               | <span data-ttu-id="a2d1e-132">Pakalpojumu intervāls</span><span class="sxs-lookup"><span data-stu-id="a2d1e-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="a2d1e-133">Stundas</span><span class="sxs-lookup"><span data-stu-id="a2d1e-133">Hour</span></span>             | <span data-ttu-id="a2d1e-134">Pašreizējais datums.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-134">The current date.</span></span>                        | <span data-ttu-id="a2d1e-135">Ik pēc 10 dienām</span><span class="sxs-lookup"><span data-stu-id="a2d1e-135">Every 10 days</span></span>    |
| <span data-ttu-id="a2d1e-136">Darbinieks</span><span class="sxs-lookup"><span data-stu-id="a2d1e-136">Worker</span></span>           | <span data-ttu-id="a2d1e-137">Darbinieks, kurš izpildīs pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="a2d1e-138">Rindai nav norādīts laika logs.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="a2d1e-139">Plānoto pakalpojumu pasūtījumu izveide</span><span class="sxs-lookup"><span data-stu-id="a2d1e-139">Create planned service orders</span></span>

<span data-ttu-id="a2d1e-140">Tagad varat izveidot plānotos pakalpojumu pasūtījumus un pakalpojumu pasūtījumu rindas nākamajam mēnesim.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="a2d1e-141">Lapā **Pakalpojumu līgumi** sadaļā **Darbību rūts** cilnē **Piegādāt** noklikšķiniet uz **Plānotie pakalpojumu pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="a2d1e-142">Lapā **Pakalpojumu pasūtījumu izveide** laukā **No datuma** ievadiet pašreizējo datumu, bet laukā **Līdz datumam** ievadiet datumu, kas ir vienu mēnesi no pašreizējā datuma.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="a2d1e-143">Slīdnim **Stunda** iestatiet vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="a2d1e-144">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-144">Click **OK**.</span></span>

<span data-ttu-id="a2d1e-145">Tā kā pakalpojuma pasūtījumā nepastāv grupēšana (to nosaka opcija **Pēc pakalpojumu līguma** laukā **Kombinēt pakalpojumu pasūtījumus**), katram pakalpojumu pasūtījumam tiek izveidota viena pakalpojumu pasūtījuma rinda.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="a2d1e-146">Izveidotie pakalpojuma pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="a2d1e-146">Service orders created</span></span>

<span data-ttu-id="a2d1e-147">Laika periodā, kuru norādījāt dialoglodziņā **Pakalpojumu pasūtījumu izveide**, iekļaujas trīs izveidotās pakalpojuma pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="a2d1e-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="a2d1e-148">Pakalpojuma pasūtījuma rindas var skatīt lapā **Pakalpojumu līgumi** (**Darbību rūts** \> cilne **Piegādāt** \> poga **Skatīt**).</span><span class="sxs-lookup"><span data-stu-id="a2d1e-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2d1e-149">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="a2d1e-149">Related topics</span></span>

[<span data-ttu-id="a2d1e-150">Pakalpojumu intervālu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="a2d1e-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

