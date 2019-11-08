---
title: Laika un apmeklētības pārvaldība programmā Retail
description: Šajā tēmā ir aprakstīti scenāriji, kas tiek atbalstīti laika un apmeklētības pārvaldībai programmā Dynamics 365 Retail.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 887b0ff8bf78cd99b3a2ec34416f0265297f556a
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570103"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="3472f-103">Laika un apmeklētības pārvaldība programmā Retail</span><span class="sxs-lookup"><span data-stu-id="3472f-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3472f-104">Šajā tēmā ir aprakstīti scenāriji, kas tiek atbalstīti laika un apmeklētības pārvaldībai programmā Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="3472f-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Retail.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="3472f-105">Darbinieku iestatījumu un plānošanas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="3472f-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="3472f-106"> sākotnējā konfigurācija</span><span class="sxs-lookup"><span data-stu-id="3472f-106">Initial configuration</span></span>

- <span data-ttu-id="3472f-107">Palaidiet konfigurācijas vedni.</span><span class="sxs-lookup"><span data-stu-id="3472f-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="3472f-108">Reģistrējiet darbiniekus kā laika reģistrācijas darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="3472f-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="3472f-109">Darbinieku grafika plānošana</span><span class="sxs-lookup"><span data-stu-id="3472f-109">Plan worker schedules</span></span>

- <span data-ttu-id="3472f-110">Izveidojiet profilus, izmantojot darbu plānošanas sistēmu.</span><span class="sxs-lookup"><span data-stu-id="3472f-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="3472f-111">Papildinformāciju skatiet tēmā [Profilu izveide, izmantojot darbu plānošanas sistēmu](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="3472f-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="3472f-112">Papildinformāciju par konfigurācijas darbībām skatiet tēmā [Laika un apmeklētības iestatīšana](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="3472f-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="3472f-113">No mazumtirdzniecības modeļa atkarīga konfigurācija</span><span class="sxs-lookup"><span data-stu-id="3472f-113">Retail-specific configuration</span></span>

- <span data-ttu-id="3472f-114">Iespējojiet funkcionalitātes Laika uzskaite profilu darbiniekiem, kuriem vēlaties aktivizēt laika reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="3472f-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="3472f-115">Noklikšķiniet uz **POS funkcionalitātes profili** &gt; **Funkcijas** &gt; **POS laika reģistrācijas** &gt; **Aktivizēt laika reģistrācijas**.</span><span class="sxs-lookup"><span data-stu-id="3472f-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="3472f-116">Konfigurējiet pārdošanas punkta (POS) atļaujas grupas, lai iespējotu funkcijas Skatīt laika uzskaites ierakstus atļauju.</span><span class="sxs-lookup"><span data-stu-id="3472f-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="3472f-117">Ar šo atļauju lietotājs var skatīt citu veikala (un citu veikalu, ar kuriem lietotājs ir saistīts, izmantojot adrešu grāmatu) darbinieku laika uzskaites reģistrācijas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="3472f-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="3472f-118">Šo atļauju ieteicams aktivizēt vadītāja lomai, bet ne kasiera lomai.</span><span class="sxs-lookup"><span data-stu-id="3472f-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="3472f-119">Noklikšķiniet uz **POS atļauju grupas** &gt; **Skatīt darba laika uzskaites ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="3472f-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="3472f-120">Reģistra laiks</span><span class="sxs-lookup"><span data-stu-id="3472f-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="3472f-121">Kasiera un darbinieka, kas nav kasieris, laika reģistrācija</span><span class="sxs-lookup"><span data-stu-id="3472f-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="3472f-122">Pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="3472f-122">On POS:</span></span>

    - <span data-ttu-id="3472f-123">Ar ierašanos saistītās darbības.</span><span class="sxs-lookup"><span data-stu-id="3472f-123">Clock-in operations:</span></span>

        - <span data-ttu-id="3472f-124">Piesakieties, veicot ar naudas kasti nesaistītu darbību, vai sadaļā Jaunu maiņa.</span><span class="sxs-lookup"><span data-stu-id="3472f-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="3472f-125">Atlasiet darbību Laika uzskaite.</span><span class="sxs-lookup"><span data-stu-id="3472f-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="3472f-126">Atlasiet vēlamo darbību.</span><span class="sxs-lookup"><span data-stu-id="3472f-126">Select a desired operation:</span></span>

            - <span data-ttu-id="3472f-127">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="3472f-127">Clock-in</span></span>
            - <span data-ttu-id="3472f-128">Darba pārtraukums</span><span class="sxs-lookup"><span data-stu-id="3472f-128">Break for Work</span></span>
            - <span data-ttu-id="3472f-129">Pusdienu pārtraukums</span><span class="sxs-lookup"><span data-stu-id="3472f-129">Break for Lunch</span></span>
            - <span data-ttu-id="3472f-130">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="3472f-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="3472f-131">Pašreizējais statuss</span><span class="sxs-lookup"><span data-stu-id="3472f-131">Current state</span></span></th>
        <th><span data-ttu-id="3472f-132">Pieejamās darbības</span><span class="sxs-lookup"><span data-stu-id="3472f-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="3472f-133">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="3472f-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="3472f-134">Darba pārtraukums</span><span class="sxs-lookup"><span data-stu-id="3472f-134">Break for Work</span></span></li>
        <li><span data-ttu-id="3472f-135">Pusdienu pārtraukums</span><span class="sxs-lookup"><span data-stu-id="3472f-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="3472f-136">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="3472f-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="3472f-137">Darba pārtraukums</span><span class="sxs-lookup"><span data-stu-id="3472f-137">Break for Work</span></span></td>
        <td><span data-ttu-id="3472f-138">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="3472f-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="3472f-139">Pusdienu pārtraukums</span><span class="sxs-lookup"><span data-stu-id="3472f-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="3472f-140">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="3472f-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="3472f-141">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="3472f-141">Clock-out</span></span></td>
        <td><span data-ttu-id="3472f-142">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="3472f-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="3472f-143">[![Laika uzskaites stāvokļi](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="3472f-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="3472f-144">Skatiet apstiprinājuma ziņojumu un pārbaudiet, vai pašreizējais aktivitātes laiks ir pareizs.</span><span class="sxs-lookup"><span data-stu-id="3472f-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="3472f-145">Reģistrācijas žurnāls</span><span class="sxs-lookup"><span data-stu-id="3472f-145">Logbook:</span></span>

    - <span data-ttu-id="3472f-146">Noklikšķiniet uz **Reģistrācijas žurnāls**, lai skatītu laika uzskaite aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="3472f-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="3472f-147">Izmantojiet laika filtrus, lai atlasītu dažādus laika logus.</span><span class="sxs-lookup"><span data-stu-id="3472f-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="3472f-148">Ja strādājat vairākās veikala atrašanās vietās, laika reģistrācijas ieraksti ir redzami par visiem veikaliem, kuros ir reģistrēts laiks.</span><span class="sxs-lookup"><span data-stu-id="3472f-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="3472f-149">Lai skatītu atlasītajā veikalā veiktās laika reģistrācijas, var izmantot veikalu filtru.</span><span class="sxs-lookup"><span data-stu-id="3472f-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="3472f-150">Atšķirīgas laika zonas</span><span class="sxs-lookup"><span data-stu-id="3472f-150">Different time zones:</span></span>

    - <span data-ttu-id="3472f-151">Ja tiek skatīta laika uzskaite no citas atrašanās vietas (kasiera žurnālā vai izmantojot vadītāja scenārija opciju **Skatīt laika uzskaites ierakstus**) un šī atrašanās vieta atrodas citā laika joslā, redzamie laika uzskaites ieraksti tiek pārvērsti atbilstoši vietējai laika joslai.</span><span class="sxs-lookup"><span data-stu-id="3472f-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="3472f-152">Piemēram, pieņemsim, ka esat divu veikalu vadītājs, no kuriem viens atrodas Arizonā, bet otrs atrodas Nevadā.</span><span class="sxs-lookup"><span data-stu-id="3472f-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="3472f-153">Kasieris reģistrē ierašanos 9:00</span><span class="sxs-lookup"><span data-stu-id="3472f-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="3472f-154">pēc Arizonas laika.</span><span class="sxs-lookup"><span data-stu-id="3472f-154">in Arizona.</span></span> <span data-ttu-id="3472f-155">Šajā brīdī Nevadā ir 8:00.</span><span class="sxs-lookup"><span data-stu-id="3472f-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="3472f-156">Tāpēc, ja atrodaties veikalā Nevadā un skatāt laika reģistrācijas ierakstus, ir redzams, ka laika reģistrācija ir atzīmēta 8:00.</span><span class="sxs-lookup"><span data-stu-id="3472f-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="3472f-157">Darbinieku laika reģistrācijas ierakstu skatīšana</span><span class="sxs-lookup"><span data-stu-id="3472f-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="3472f-158">Skatiet darbinieka laika reģistrācijas ierakstus un filtrējiet tos pēc veikala vai aktivitātes tipa.</span><span class="sxs-lookup"><span data-stu-id="3472f-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="3472f-159">Pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="3472f-159">On POS:</span></span>

- <span data-ttu-id="3472f-160">Atlasiet opciju **Skatīt laika uzskaites ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="3472f-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="3472f-161">Var skatīt visu to darbinieku laika uzskaites reģistrācijas darbības, kas iedalīti tajos pašos veikalos, kur esat iedalīts jūs.</span><span class="sxs-lookup"><span data-stu-id="3472f-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="3472f-162">Lai filtrētu laika reģistrācijas ierakstus, var izmantot aktivitātes tipa un veikala filtru.</span><span class="sxs-lookup"><span data-stu-id="3472f-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="3472f-163">Laika reģistrācijas ierakstu apstrāde un pārvaldība</span><span class="sxs-lookup"><span data-stu-id="3472f-163">Process and manage time registrations</span></span>

<span data-ttu-id="3472f-164">Retail lietotājs izpilda darbplūsmu, lai aprēķinātu, apstiprinātu un pārsūtītu laika reģistrācijas ierakstus algas aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="3472f-164">A Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="3472f-165">Primārās darbības</span><span class="sxs-lookup"><span data-stu-id="3472f-165">Primary operations</span></span>

- <span data-ttu-id="3472f-166">Aprēķināt</span><span class="sxs-lookup"><span data-stu-id="3472f-166">Calculate</span></span>
- <span data-ttu-id="3472f-167">Apstiprināt</span><span class="sxs-lookup"><span data-stu-id="3472f-167">Approve</span></span>
- <span data-ttu-id="3472f-168">Iesniegt algas aprēķināšanai</span><span class="sxs-lookup"><span data-stu-id="3472f-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="3472f-169">Citas standarta darbības</span><span class="sxs-lookup"><span data-stu-id="3472f-169">Other common operations</span></span>

- <span data-ttu-id="3472f-170">Aiziešana grupā</span><span class="sxs-lookup"><span data-stu-id="3472f-170">Bulk Clock-out</span></span>
- <span data-ttu-id="3472f-171">Kavējuma reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="3472f-171">Register Absence</span></span>

<span data-ttu-id="3472f-172">Papildinformāciju par laika un apmeklētības ierakstu apstrādi skatiet tēmā[Laika un apmeklētības ierakstu apstrāde](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="3472f-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
