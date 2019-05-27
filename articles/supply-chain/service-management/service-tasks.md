---
title: Pakalpojumu uzdevumi
description: Izmantojiet pakalpojumu uzdevumus, lai aprakstītu uzdevumu, kas tiks veikts pakalpojuma pasūtījuma laikā. Šo informāciju var redzēt gan tehniskie speciālisti, gan debitori.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2538a7b4a4c13a299afb37dd336f2f5d6f36a23
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549844"
---
# <a name="service-tasks"></a><span data-ttu-id="6bc8d-104">Pakalpojumu uzdevumi</span><span class="sxs-lookup"><span data-stu-id="6bc8d-104">Service tasks</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bc8d-105">Izmantojiet pakalpojumu uzdevumus, lai aprakstītu uzdevumu, kas tiks veikts pakalpojuma pasūtījuma laikā.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="6bc8d-106">Šo informāciju var redzēt gan tehniskie speciālisti, gan debitori.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="6bc8d-107">Pakalpojumu uzdevumi tiek veidoti lapā **Pakalpojumu uzdevumi**, un tie tiek saistīti ar konkrētu pakalpojumu līgumu vai pakalpojuma pasūtījumu, veidojot pakalpojumu uzdevumu attiecības.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="6bc8d-108">Ikreiz, kad veidojat pakalpojumu uzdevumu attiecības, varat veidot:</span><span class="sxs-lookup"><span data-stu-id="6bc8d-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="6bc8d-109">Iekšējās piezīmes par uzdevumu, piemēram, detalizētas tehniskās prasības uzdevumam, kuras tehniskajiem speciālistiem ir svarīgi zināt.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="6bc8d-110">Ārējās piezīmes, kuras var redzēt kreditori.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-110">External notes that the customer can see.</span></span> <span data-ttu-id="6bc8d-111">Tās sniedz mazāk tehnisku skaidrojumu par uzdevumu, kas tiek veikts atbilstoši līgumam starp debitoru un pakalpojumu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="6bc8d-112">Kad ir izveidotas pakalpojumu uzdevumu attiecības starp pakalpojuma uzdevumu un pakalpojuma pasūtījumu vai pakalpojumu līgumu, varat norādīt pakalpojuma uzdevumu, kad veidojat pakalpojuma pasūtījuma rindas vai pakalpojumu līguma rindas pašreizējajam pakalpojuma pasūtījumam vai pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="6bc8d-113">Kad ģenerējat pakalpojumu pasūtījumus no pakalpojumu līguma, varat izmantot katrai pakalpojumu līguma rindai piešķirtos pakalpojumu uzdevumus, lai pakalpojumu pasūtījumos grupētu pakalpojuma pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="6bc8d-114">Pakalpojuma uzdevuma izveide</span><span class="sxs-lookup"><span data-stu-id="6bc8d-114">Create a service task</span></span>

1. <span data-ttu-id="6bc8d-115">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="6bc8d-116">Izveidojiet jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-116">Create a new line.</span></span>
3. <span data-ttu-id="6bc8d-117">Ievadiet pakalpojuma ID un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="6bc8d-118">Paraugs</span><span class="sxs-lookup"><span data-stu-id="6bc8d-118">Example</span></span>

<span data-ttu-id="6bc8d-119">Tehniskajam speciālistam ir jāveic divi darbi saistībā ar pārnesumkārbu (pakalpojumu objekts GB-1234) debitora vietā.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="6bc8d-120">Debitoram tiek izveidots pakalpojumu līgums, un ar darbiem tiek saistītas vairākas darbības.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="6bc8d-121">Zemāk redzams pakalpojumu līgums un pakalpojumu līguma rindas šiem diviem darbiem:</span><span class="sxs-lookup"><span data-stu-id="6bc8d-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="6bc8d-122">Pakalpojumu līgums</span><span class="sxs-lookup"><span data-stu-id="6bc8d-122">Service agreement</span></span>

| <span data-ttu-id="6bc8d-123">Project</span><span class="sxs-lookup"><span data-stu-id="6bc8d-123">Project</span></span> | <span data-ttu-id="6bc8d-124">Pakalpojumu līgums</span><span class="sxs-lookup"><span data-stu-id="6bc8d-124">Service agreement</span></span> | <span data-ttu-id="6bc8d-125">apraksts</span><span class="sxs-lookup"><span data-stu-id="6bc8d-125">Description</span></span>                                  | <span data-ttu-id="6bc8d-126">Grupa</span><span class="sxs-lookup"><span data-stu-id="6bc8d-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="6bc8d-127">9012</span><span class="sxs-lookup"><span data-stu-id="6bc8d-127">9012</span></span>    | <span data-ttu-id="6bc8d-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="6bc8d-128">000008\_001</span></span>       | <span data-ttu-id="6bc8d-129">Pārbaude un dilstošo detaļu nomaiņa — GB-1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="6bc8d-130">Prēmija</span><span class="sxs-lookup"><span data-stu-id="6bc8d-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="6bc8d-131">Pakalpojumu līguma rindas</span><span class="sxs-lookup"><span data-stu-id="6bc8d-131">Service agreement lines</span></span>

| <span data-ttu-id="6bc8d-132">apraksts</span><span class="sxs-lookup"><span data-stu-id="6bc8d-132">Description</span></span>             | <span data-ttu-id="6bc8d-133">Darbības veids</span><span class="sxs-lookup"><span data-stu-id="6bc8d-133">Transaction type</span></span> | <span data-ttu-id="6bc8d-134">Pakalpojumu objekts</span><span class="sxs-lookup"><span data-stu-id="6bc8d-134">Service object</span></span> | <span data-ttu-id="6bc8d-135">Pakalpojumu uzdevums</span><span class="sxs-lookup"><span data-stu-id="6bc8d-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="6bc8d-136">Pārbaude un tīrīšana</span><span class="sxs-lookup"><span data-stu-id="6bc8d-136">Inspection and cleaning</span></span> | <span data-ttu-id="6bc8d-137">Stundas</span><span class="sxs-lookup"><span data-stu-id="6bc8d-137">Hour</span></span>             | <span data-ttu-id="6bc8d-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-138">GB-1234</span></span>        | <span data-ttu-id="6bc8d-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-139">I/C - GB1234</span></span> |
| <span data-ttu-id="6bc8d-140">Ceļojums</span><span class="sxs-lookup"><span data-stu-id="6bc8d-140">Travel</span></span>                  | <span data-ttu-id="6bc8d-141">Expense</span><span class="sxs-lookup"><span data-stu-id="6bc8d-141">Expense</span></span>          | <span data-ttu-id="6bc8d-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-142">GB-1234</span></span>        | <span data-ttu-id="6bc8d-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-143">I/C - GB1234</span></span> |
| <span data-ttu-id="6bc8d-144">Materiāli</span><span class="sxs-lookup"><span data-stu-id="6bc8d-144">Materials</span></span>               | <span data-ttu-id="6bc8d-145">Objekts</span><span class="sxs-lookup"><span data-stu-id="6bc8d-145">Item</span></span>             | <span data-ttu-id="6bc8d-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-146">GB-1234</span></span>        | <span data-ttu-id="6bc8d-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-147">I/C - GB1234</span></span> |
| <span data-ttu-id="6bc8d-148">Dilstošo detaļu nomaiņa</span><span class="sxs-lookup"><span data-stu-id="6bc8d-148">Routine replacement</span></span>     | <span data-ttu-id="6bc8d-149">Stundas</span><span class="sxs-lookup"><span data-stu-id="6bc8d-149">Hour</span></span>             | <span data-ttu-id="6bc8d-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-150">GB-1234</span></span>        | <span data-ttu-id="6bc8d-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-151">RR - GB1234</span></span>  |
| <span data-ttu-id="6bc8d-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="6bc8d-152">GR-1</span></span>                    | <span data-ttu-id="6bc8d-153">Objekts</span><span class="sxs-lookup"><span data-stu-id="6bc8d-153">Item</span></span>             | <span data-ttu-id="6bc8d-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-154">GB-1234</span></span>        | <span data-ttu-id="6bc8d-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-155">RR - GB1234</span></span>  |
| <span data-ttu-id="6bc8d-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="6bc8d-156">GR-5</span></span>                    | <span data-ttu-id="6bc8d-157">Objekts</span><span class="sxs-lookup"><span data-stu-id="6bc8d-157">Item</span></span>             | <span data-ttu-id="6bc8d-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-158">GB-1234</span></span>        | <span data-ttu-id="6bc8d-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-159">RR - GB1234</span></span>  |

<span data-ttu-id="6bc8d-160">Pakalpojumu līguma rindām šiem diviem darbiem ir pievienoti divi pakalpojumu uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="6bc8d-161">Pakalpojumu uzdevumi nosaka darbības, kas pieder katram darbam.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="6bc8d-162">Pirmajā gadījumā pakalpojuma uzdevums I/C - GB1234 identificē visas pakalpojumu līguma rindas, kas ir iesaistītas objekta GB-1234 pārbaudē un tīrīšanā.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="6bc8d-163">Otrajā gadījumā pakalpojuma uzdevums RR - GB1234 identificē visas pakalpojumu līguma rindas, kas ir iesaistītas dilstošo detaļu nomaiņas darba veikšanā.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="6bc8d-164">Pakalpojumu uzdevumu attiecības, kas saista pakalpojumu uzdevumus pie konkrētā līguma, ir šādas:</span><span class="sxs-lookup"><span data-stu-id="6bc8d-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="6bc8d-165">Pakalpojumu uzdevumi</span><span class="sxs-lookup"><span data-stu-id="6bc8d-165">Service tasks</span></span>

| <span data-ttu-id="6bc8d-166">Pakalpojuma uzdevums</span><span class="sxs-lookup"><span data-stu-id="6bc8d-166">Service task</span></span> | <span data-ttu-id="6bc8d-167">Apraksts</span><span class="sxs-lookup"><span data-stu-id="6bc8d-167">Description</span></span>                             | <span data-ttu-id="6bc8d-168">Iekšējā piezīme</span><span class="sxs-lookup"><span data-stu-id="6bc8d-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="6bc8d-169">Ārējā piezīme</span><span class="sxs-lookup"><span data-stu-id="6bc8d-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="6bc8d-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-170">I/C - GB1234</span></span> | <span data-ttu-id="6bc8d-171">Ātrumkārbas GB-1234 pārbaude</span><span class="sxs-lookup"><span data-stu-id="6bc8d-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="6bc8d-172">Ātrumkārbas GB-1234 vizuālā un mehāniskā pārbaude un tīrīšana.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="6bc8d-173">Ātrumkārbas dilstošo detaļu pārbaude</span><span class="sxs-lookup"><span data-stu-id="6bc8d-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="6bc8d-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="6bc8d-174">RR - GB1234</span></span>  | <span data-ttu-id="6bc8d-175">GB-1234 detaļu dilstošo detaļu nomaiņa</span><span class="sxs-lookup"><span data-stu-id="6bc8d-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="6bc8d-176">GR-1 un GR-5 dilstošo detaļu nomaiņa (ātrumkārbām, kas ražotas pirms 2002. gada arī GR-2 detaļas nomaiņa)</span><span class="sxs-lookup"><span data-stu-id="6bc8d-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="6bc8d-177">Dilstošo detaļu nomaiņa</span><span class="sxs-lookup"><span data-stu-id="6bc8d-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="6bc8d-178">Pakalpojumu pasūtījumu grupēšana</span><span class="sxs-lookup"><span data-stu-id="6bc8d-178">Group service orders</span></span>

<span data-ttu-id="6bc8d-179">Kad automātiski veidojat pakalpojumu pasūtījumus, kā grupēšanas kritēriju varat izmantot pakalpojumu uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="6bc8d-180">Lai pakalpojumu pasūtījumus grupētu pēc pakalpojumu uzdevumiem, definējiet pakalpojumu līgumam, ka pakalpojumu pasūtījumi, kuru pamatā ir pakalpojumu līgums, jāgrupē pēc pakalpojumu uzdevumu ID kā to sākotnējā grupēšanas kritērija.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="6bc8d-181">**Grupēšana pēc pakalpojuma uzdevuma**</span><span class="sxs-lookup"><span data-stu-id="6bc8d-181">**Group by service task**</span></span>

1. <span data-ttu-id="6bc8d-182">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="6bc8d-183">Cilnes **Iestatījumi** laukā **Pakalpojumu pasūtījumu kombinēšana** atlasiet **Pēc pakalpojuma uzdevuma**.</span><span class="sxs-lookup"><span data-stu-id="6bc8d-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>


