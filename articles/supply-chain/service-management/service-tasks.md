---
title: Pakalpojumu uzdevumu pārskats
description: Izmantojiet pakalpojumu uzdevumus, lai aprakstītu uzdevumu, kas tiks veikts pakalpojuma pasūtījuma laikā. Šo informāciju var redzēt gan tehniskie speciālisti, gan debitori.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2864b481c67c078df73436d752069a6b6c78640
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206039"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="f0357-104">Pakalpojumu uzdevumu pārskats</span><span class="sxs-lookup"><span data-stu-id="f0357-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0357-105">Izmantojiet pakalpojumu uzdevumus, lai aprakstītu uzdevumu, kas tiks veikts pakalpojuma pasūtījuma laikā.</span><span class="sxs-lookup"><span data-stu-id="f0357-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="f0357-106">Šo informāciju var redzēt gan tehniskie speciālisti, gan debitori.</span><span class="sxs-lookup"><span data-stu-id="f0357-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="f0357-107">Pakalpojumu uzdevumi tiek veidoti lapā **Pakalpojumu uzdevumi**, un tie tiek saistīti ar konkrētu pakalpojumu līgumu vai pakalpojuma pasūtījumu, veidojot pakalpojumu uzdevumu attiecības.</span><span class="sxs-lookup"><span data-stu-id="f0357-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="f0357-108">Ikreiz, kad veidojat pakalpojumu uzdevumu attiecības, varat veidot:</span><span class="sxs-lookup"><span data-stu-id="f0357-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="f0357-109">Iekšējās piezīmes par uzdevumu, piemēram, detalizētas tehniskās prasības uzdevumam, kuras tehniskajiem speciālistiem ir svarīgi zināt.</span><span class="sxs-lookup"><span data-stu-id="f0357-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="f0357-110">Ārējās piezīmes, kuras var redzēt kreditori.</span><span class="sxs-lookup"><span data-stu-id="f0357-110">External notes that the customer can see.</span></span> <span data-ttu-id="f0357-111">Tās sniedz mazāk tehnisku skaidrojumu par uzdevumu, kas tiek veikts atbilstoši līgumam starp debitoru un pakalpojumu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="f0357-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="f0357-112">Kad ir izveidotas pakalpojumu uzdevumu attiecības starp pakalpojuma uzdevumu un pakalpojuma pasūtījumu vai pakalpojumu līgumu, varat norādīt pakalpojuma uzdevumu, kad veidojat pakalpojuma pasūtījuma rindas vai pakalpojumu līguma rindas pašreizējajam pakalpojuma pasūtījumam vai pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="f0357-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="f0357-113">Kad ģenerējat pakalpojumu pasūtījumus no pakalpojumu līguma, varat izmantot katrai pakalpojumu līguma rindai piešķirtos pakalpojumu uzdevumus, lai pakalpojumu pasūtījumos grupētu pakalpojuma pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="f0357-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="f0357-114">Pakalpojuma uzdevuma izveide</span><span class="sxs-lookup"><span data-stu-id="f0357-114">Create a service task</span></span>

1. <span data-ttu-id="f0357-115">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="f0357-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="f0357-116">Izveidojiet jaunu rindu.</span><span class="sxs-lookup"><span data-stu-id="f0357-116">Create a new line.</span></span>
3. <span data-ttu-id="f0357-117">Ievadiet pakalpojuma ID un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="f0357-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="f0357-118">Piemērs</span><span class="sxs-lookup"><span data-stu-id="f0357-118">Example</span></span>

<span data-ttu-id="f0357-119">Tehniskajam speciālistam ir jāveic divi darbi saistībā ar pārnesumkārbu (pakalpojumu objekts GB-1234) debitora vietā.</span><span class="sxs-lookup"><span data-stu-id="f0357-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="f0357-120">Debitoram tiek izveidots pakalpojumu līgums, un ar darbiem tiek saistītas vairākas darbības.</span><span class="sxs-lookup"><span data-stu-id="f0357-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="f0357-121">Zemāk redzams pakalpojumu līgums un pakalpojumu līguma rindas šiem diviem darbiem:</span><span class="sxs-lookup"><span data-stu-id="f0357-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="f0357-122">Pakalpojumu līgums</span><span class="sxs-lookup"><span data-stu-id="f0357-122">Service agreement</span></span>

| <span data-ttu-id="f0357-123">Project</span><span class="sxs-lookup"><span data-stu-id="f0357-123">Project</span></span> | <span data-ttu-id="f0357-124">Pakalpojumu līgums</span><span class="sxs-lookup"><span data-stu-id="f0357-124">Service agreement</span></span> | <span data-ttu-id="f0357-125">apraksts</span><span class="sxs-lookup"><span data-stu-id="f0357-125">Description</span></span>                                  | <span data-ttu-id="f0357-126">Grupa</span><span class="sxs-lookup"><span data-stu-id="f0357-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="f0357-127">9012</span><span class="sxs-lookup"><span data-stu-id="f0357-127">9012</span></span>    | <span data-ttu-id="f0357-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="f0357-128">000008\_001</span></span>       | <span data-ttu-id="f0357-129">Pārbaude un dilstošo detaļu nomaiņa — GB-1234</span><span class="sxs-lookup"><span data-stu-id="f0357-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="f0357-130">Prēmija</span><span class="sxs-lookup"><span data-stu-id="f0357-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="f0357-131">Pakalpojumu līguma rindas</span><span class="sxs-lookup"><span data-stu-id="f0357-131">Service agreement lines</span></span>

| <span data-ttu-id="f0357-132">apraksts</span><span class="sxs-lookup"><span data-stu-id="f0357-132">Description</span></span>             | <span data-ttu-id="f0357-133">Darbības veids</span><span class="sxs-lookup"><span data-stu-id="f0357-133">Transaction type</span></span> | <span data-ttu-id="f0357-134">Pakalpojumu objekts</span><span class="sxs-lookup"><span data-stu-id="f0357-134">Service object</span></span> | <span data-ttu-id="f0357-135">Pakalpojumu uzdevums</span><span class="sxs-lookup"><span data-stu-id="f0357-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="f0357-136">Pārbaude un tīrīšana</span><span class="sxs-lookup"><span data-stu-id="f0357-136">Inspection and cleaning</span></span> | <span data-ttu-id="f0357-137">Stundas</span><span class="sxs-lookup"><span data-stu-id="f0357-137">Hour</span></span>             | <span data-ttu-id="f0357-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="f0357-138">GB-1234</span></span>        | <span data-ttu-id="f0357-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="f0357-139">I/C - GB1234</span></span> |
| <span data-ttu-id="f0357-140">Ceļojums</span><span class="sxs-lookup"><span data-stu-id="f0357-140">Travel</span></span>                  | <span data-ttu-id="f0357-141">Expense</span><span class="sxs-lookup"><span data-stu-id="f0357-141">Expense</span></span>          | <span data-ttu-id="f0357-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="f0357-142">GB-1234</span></span>        | <span data-ttu-id="f0357-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="f0357-143">I/C - GB1234</span></span> |
| <span data-ttu-id="f0357-144">Materiāli</span><span class="sxs-lookup"><span data-stu-id="f0357-144">Materials</span></span>               | <span data-ttu-id="f0357-145">Objekts</span><span class="sxs-lookup"><span data-stu-id="f0357-145">Item</span></span>             | <span data-ttu-id="f0357-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="f0357-146">GB-1234</span></span>        | <span data-ttu-id="f0357-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="f0357-147">I/C - GB1234</span></span> |
| <span data-ttu-id="f0357-148">Dilstošo detaļu nomaiņa</span><span class="sxs-lookup"><span data-stu-id="f0357-148">Routine replacement</span></span>     | <span data-ttu-id="f0357-149">Stundas</span><span class="sxs-lookup"><span data-stu-id="f0357-149">Hour</span></span>             | <span data-ttu-id="f0357-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="f0357-150">GB-1234</span></span>        | <span data-ttu-id="f0357-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="f0357-151">RR - GB1234</span></span>  |
| <span data-ttu-id="f0357-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="f0357-152">GR-1</span></span>                    | <span data-ttu-id="f0357-153">Objekts</span><span class="sxs-lookup"><span data-stu-id="f0357-153">Item</span></span>             | <span data-ttu-id="f0357-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="f0357-154">GB-1234</span></span>        | <span data-ttu-id="f0357-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="f0357-155">RR - GB1234</span></span>  |
| <span data-ttu-id="f0357-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="f0357-156">GR-5</span></span>                    | <span data-ttu-id="f0357-157">Objekts</span><span class="sxs-lookup"><span data-stu-id="f0357-157">Item</span></span>             | <span data-ttu-id="f0357-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="f0357-158">GB-1234</span></span>        | <span data-ttu-id="f0357-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="f0357-159">RR - GB1234</span></span>  |

<span data-ttu-id="f0357-160">Pakalpojumu līguma rindām šiem diviem darbiem ir pievienoti divi pakalpojumu uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="f0357-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="f0357-161">Pakalpojumu uzdevumi nosaka darbības, kas pieder katram darbam.</span><span class="sxs-lookup"><span data-stu-id="f0357-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="f0357-162">Pirmajā gadījumā pakalpojuma uzdevums I/C - GB1234 identificē visas pakalpojumu līguma rindas, kas ir iesaistītas objekta GB-1234 pārbaudē un tīrīšanā.</span><span class="sxs-lookup"><span data-stu-id="f0357-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="f0357-163">Otrajā gadījumā pakalpojuma uzdevums RR - GB1234 identificē visas pakalpojumu līguma rindas, kas ir iesaistītas dilstošo detaļu nomaiņas darba veikšanā.</span><span class="sxs-lookup"><span data-stu-id="f0357-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="f0357-164">Pakalpojumu uzdevumu attiecības, kas saista pakalpojumu uzdevumus pie konkrētā līguma, ir šādas:</span><span class="sxs-lookup"><span data-stu-id="f0357-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="f0357-165">Pakalpojumu uzdevumi</span><span class="sxs-lookup"><span data-stu-id="f0357-165">Service tasks</span></span>

| <span data-ttu-id="f0357-166">Pakalpojuma uzdevums</span><span class="sxs-lookup"><span data-stu-id="f0357-166">Service task</span></span> | <span data-ttu-id="f0357-167">Apraksts</span><span class="sxs-lookup"><span data-stu-id="f0357-167">Description</span></span>                             | <span data-ttu-id="f0357-168">Iekšējā piezīme</span><span class="sxs-lookup"><span data-stu-id="f0357-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="f0357-169">Ārējā piezīme</span><span class="sxs-lookup"><span data-stu-id="f0357-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="f0357-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="f0357-170">I/C - GB1234</span></span> | <span data-ttu-id="f0357-171">Ātrumkārbas GB-1234 pārbaude</span><span class="sxs-lookup"><span data-stu-id="f0357-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="f0357-172">Ātrumkārbas GB-1234 vizuālā un mehāniskā pārbaude un tīrīšana.</span><span class="sxs-lookup"><span data-stu-id="f0357-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="f0357-173">Ātrumkārbas dilstošo detaļu pārbaude</span><span class="sxs-lookup"><span data-stu-id="f0357-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="f0357-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="f0357-174">RR - GB1234</span></span>  | <span data-ttu-id="f0357-175">GB-1234 detaļu dilstošo detaļu nomaiņa</span><span class="sxs-lookup"><span data-stu-id="f0357-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="f0357-176">GR-1 un GR-5 dilstošo detaļu nomaiņa (ātrumkārbām, kas ražotas pirms 2002. gada arī GR-2 detaļas nomaiņa)</span><span class="sxs-lookup"><span data-stu-id="f0357-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="f0357-177">Dilstošo detaļu nomaiņa</span><span class="sxs-lookup"><span data-stu-id="f0357-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="f0357-178">Pakalpojumu pasūtījumu grupēšana</span><span class="sxs-lookup"><span data-stu-id="f0357-178">Group service orders</span></span>

<span data-ttu-id="f0357-179">Kad automātiski veidojat pakalpojumu pasūtījumus, kā grupēšanas kritēriju varat izmantot pakalpojumu uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="f0357-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="f0357-180">Lai pakalpojumu pasūtījumus grupētu pēc pakalpojumu uzdevumiem, definējiet pakalpojumu līgumam, ka pakalpojumu pasūtījumi, kuru pamatā ir pakalpojumu līgums, jāgrupē pēc pakalpojumu uzdevumu ID kā to sākotnējā grupēšanas kritērija.</span><span class="sxs-lookup"><span data-stu-id="f0357-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="f0357-181">**Grupēšana pēc pakalpojuma uzdevuma**</span><span class="sxs-lookup"><span data-stu-id="f0357-181">**Group by service task**</span></span>

1. <span data-ttu-id="f0357-182">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="f0357-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="f0357-183">Cilnes **Iestatījumi** laukā **Pakalpojumu pasūtījumu kombinēšana** atlasiet **Pēc pakalpojuma uzdevuma**.</span><span class="sxs-lookup"><span data-stu-id="f0357-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>


