---
title: "Laika un apmeklētības pārvaldība programmā Retail"
description: "Šajā tēmā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Finance and Operations — Retail atbalstītie laika un apmeklētības pārvaldības scenāriji."
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 21c29c3c37dfacdd98f5c3ec7698f07623da2285
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="d4bc9-103">Laika un apmeklētības pārvaldība programmā Retail</span><span class="sxs-lookup"><span data-stu-id="d4bc9-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4bc9-104">Šajā tēmā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Finance and Operations — Retail atbalstītie laika un apmeklētības pārvaldības scenāriji.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span> 

<a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="d4bc9-105">Darbinieku iestatījumu un plānošanas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="d4bc9-105">Manage worker setup and scheduling</span></span>
----------------------------------

### <a name="initial-configuration"></a><span data-ttu-id="d4bc9-106"> sākotnējā konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d4bc9-106">Initial configuration</span></span>

-   <span data-ttu-id="d4bc9-107">Palaidiet konfigurācijas vedni.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-107">Run the configuration wizard.</span></span>
-   <span data-ttu-id="d4bc9-108">Reģistrējiet darbiniekus kā laika reģistrācijas darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="d4bc9-109">Darbinieku grafika plānošana</span><span class="sxs-lookup"><span data-stu-id="d4bc9-109">Plan worker schedules</span></span>

-   <span data-ttu-id="d4bc9-110">Izveidojiet profilus, izmantojot darbu plānošanas sistēmu.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="d4bc9-111">Lai iegūtu papildus informāciju, skatiet <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-111">For more information, see <https://technet.microsoft.com/en-us/library/aa551234.aspx>.</span></span>

<span data-ttu-id="d4bc9-112">Informāciju par konfigurēšanas darbībām skatiet šeit: <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-112">For information about the configuration steps, see <https://technet.microsoft.com/en-us/library/aa496971.aspx>.</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="d4bc9-113">No mazumtirdzniecības modeļa atkarīga konfigurācija</span><span class="sxs-lookup"><span data-stu-id="d4bc9-113">Retail-specific configuration</span></span>

-   <span data-ttu-id="d4bc9-114">Iespējojiet funkcionalitātes Laika uzskaite profilu darbiniekiem, kuriem vēlaties aktivizēt laika reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="d4bc9-115">Noklikšķiniet uz **POS funkcionalitātes profili** &gt; **Funkcijas** &gt; **POS laika reģistrācijas** &gt; **Aktivizēt laika reģistrācijas**.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
-   <span data-ttu-id="d4bc9-116">Konfigurējiet pārdošanas punkta (POS) atļaujas grupas, lai iespējotu funkcijas Skatīt laika uzskaites ierakstus atļauju.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="d4bc9-117">Ar šo atļauju lietotājs var skatīt citu veikala (un citu veikalu, ar kuriem lietotājs ir saistīts, izmantojot adrešu grāmatu) darbinieku laika uzskaites reģistrācijas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="d4bc9-118">Šo atļauju ieteicams aktivizēt vadītāja lomai, bet ne kasiera lomai.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="d4bc9-119">Noklikšķiniet uz **POS atļauju grupas** &gt; **Skatīt darba laika uzskaites ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="d4bc9-120">Reģistra laiks</span><span class="sxs-lookup"><span data-stu-id="d4bc9-120">Register time</span></span>
### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="d4bc9-121">Kasiera un darbinieka, kas nav kasieris, laika reģistrācija</span><span class="sxs-lookup"><span data-stu-id="d4bc9-121">Cashier and non-cashier time registrations</span></span>

-   <span data-ttu-id="d4bc9-122">Pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="d4bc9-122">On POS:</span></span>
    -   <span data-ttu-id="d4bc9-123">Ar ierašanos saistītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-123">Clock-in operations:</span></span>
        -   <span data-ttu-id="d4bc9-124">Piesakieties, veicot ar naudas kasti nesaistītu darbību, vai sadaļā Jaunu maiņa.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-124">Log on with a non-drawer operation or New shift.</span></span>
        -   <span data-ttu-id="d4bc9-125">Atlasiet darbību Laika uzskaite.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-125">Select a Time Clock operation.</span></span>
        -   <span data-ttu-id="d4bc9-126">Atlasiet vēlamo darbību.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-126">Select a desired operation:</span></span>
            -   <span data-ttu-id="d4bc9-127">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="d4bc9-127">Clock-in</span></span>
            -   <span data-ttu-id="d4bc9-128">Darba pārtraukums</span><span class="sxs-lookup"><span data-stu-id="d4bc9-128">Break for Work</span></span>
            -   <span data-ttu-id="d4bc9-129">Pusdienu pārtraukums</span><span class="sxs-lookup"><span data-stu-id="d4bc9-129">Break for Lunch</span></span>
            -   <span data-ttu-id="d4bc9-130">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="d4bc9-130">Clock-out</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d4bc9-131">Pašreizējais statuss</span><span class="sxs-lookup"><span data-stu-id="d4bc9-131">Current state</span></span></th>
    <th><span data-ttu-id="d4bc9-132">Pieejamās darbības</span><span class="sxs-lookup"><span data-stu-id="d4bc9-132">Available operations</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="d4bc9-133">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="d4bc9-133">Clock-in</span></span></td>
    <td><ul>
    <li><span data-ttu-id="d4bc9-134">Darba pārtraukums</span><span class="sxs-lookup"><span data-stu-id="d4bc9-134">Break for Work</span></span></li>
    <li><span data-ttu-id="d4bc9-135">Pusdienu pārtraukums</span><span class="sxs-lookup"><span data-stu-id="d4bc9-135">Break for Lunch</span></span></li>
    <li><span data-ttu-id="d4bc9-136">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="d4bc9-136">Clock-out</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d4bc9-137">Darba pārtraukums</span><span class="sxs-lookup"><span data-stu-id="d4bc9-137">Break for Work</span></span></td>
    <td><span data-ttu-id="d4bc9-138">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="d4bc9-138">Clock-in</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d4bc9-139">Pusdienu pārtraukums</span><span class="sxs-lookup"><span data-stu-id="d4bc9-139">Break for Lunch</span></span></td>
    <td><span data-ttu-id="d4bc9-140">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="d4bc9-140">Clock-in</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d4bc9-141">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="d4bc9-141">Clock-out</span></span></td>
    <td><span data-ttu-id="d4bc9-142">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="d4bc9-142">Clock-in</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="d4bc9-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="d4bc9-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>
-   <span data-ttu-id="d4bc9-144">Skatiet apstiprinājuma ziņojumu un pārbaudiet, vai pašreizējais aktivitātes laiks ir pareizs.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
-   <span data-ttu-id="d4bc9-145">Reģistrācijas žurnāls</span><span class="sxs-lookup"><span data-stu-id="d4bc9-145">Logbook:</span></span>
    -   <span data-ttu-id="d4bc9-146">Noklikšķiniet uz **Reģistrācijas žurnāls**, lai skatītu laika uzskaite aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-146">Click **Logbook** to view time clock activity.</span></span>
    -   <span data-ttu-id="d4bc9-147">Izmantojiet laika filtrus, lai atlasītu dažādus laika logus.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-147">Use time filters to select different time windows.</span></span>
    -   <span data-ttu-id="d4bc9-148">Ja strādājat vairākās veikala atrašanās vietās, laika reģistrācijas ieraksti ir redzami par visiem veikaliem, kuros ir reģistrēts laiks.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="d4bc9-149">Lai skatītu atlasītajā veikalā veiktās laika reģistrācijas, var izmantot veikalu filtru.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-149">You can use the store filter to view time registrations from a selected store.</span></span>

<!-- -->

-   <span data-ttu-id="d4bc9-150">Atšķirīgas laika zonas</span><span class="sxs-lookup"><span data-stu-id="d4bc9-150">Different time zones:</span></span>
    -   <span data-ttu-id="d4bc9-151">Ja tiek skatīta laika uzskaite no citas atrašanās vietas (kasiera žurnālā vai izmantojot vadītāja scenārija opciju **Skatīt laika uzskaites ierakstus**) un šī atrašanās vieta atrodas citā laika joslā, redzamie laika uzskaites ieraksti tiek pārvērsti atbilstoši vietējai laika joslai.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="d4bc9-152">Piemēram, pieņemsim, ka esat divu veikalu vadītājs, no kuriem viens atrodas Arizonā, bet otrs atrodas Nevadā.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="d4bc9-153">Kasieris reģistrē ierašanos 9:00</span><span class="sxs-lookup"><span data-stu-id="d4bc9-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="d4bc9-154">pēc Arizonas laika.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-154">in Arizona.</span></span> <span data-ttu-id="d4bc9-155">Šajā brīdī Nevadā ir 8:00.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="d4bc9-156">Tāpēc, ja atrodaties veikalā Nevadā un skatāt laika reģistrācijas ierakstus, ir redzams, ka laika reģistrācija ir atzīmēta 8:00.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="d4bc9-157">Darbinieku laika reģistrācijas ierakstu skatīšana</span><span class="sxs-lookup"><span data-stu-id="d4bc9-157">View worker time registrations</span></span>
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="d4bc9-158">Skatiet darbinieka laika reģistrācijas ierakstus un filtrējiet tos pēc veikala vai aktivitātes tipa.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="d4bc9-159">Pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="d4bc9-159">On POS:</span></span>

-   <span data-ttu-id="d4bc9-160">Atlasiet opciju **Skatīt laika uzskaites ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-160">Select **View timeclock entries**.</span></span>
-   <span data-ttu-id="d4bc9-161">Var skatīt visu to darbinieku laika uzskaites reģistrācijas darbības, kas iedalīti tajos pašos veikalos, kur esat iedalīts jūs.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
-   <span data-ttu-id="d4bc9-162">Lai filtrētu laika reģistrācijas ierakstus, var izmantot aktivitātes tipa un veikala filtru.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="d4bc9-163">Laika reģistrācijas ierakstu apstrāde un pārvaldība</span><span class="sxs-lookup"><span data-stu-id="d4bc9-163">Process and manage time registrations</span></span>
<span data-ttu-id="d4bc9-164">Programmatūras Dynamics 365 for Finance and Operations — Retail lietotājs var sekot līdzi darbplūsmai, lai aprēķinātu, apstiprinātu un pārsūtītu laika reģistrācijas ierakstus algas aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="d4bc9-165">Primārās darbības</span><span class="sxs-lookup"><span data-stu-id="d4bc9-165">Primary operations</span></span>

-   <span data-ttu-id="d4bc9-166">Aprēķināt</span><span class="sxs-lookup"><span data-stu-id="d4bc9-166">Calculate</span></span>
-   <span data-ttu-id="d4bc9-167">Apstiprināt</span><span class="sxs-lookup"><span data-stu-id="d4bc9-167">Approve</span></span>
-   <span data-ttu-id="d4bc9-168">Iesniegt algas aprēķināšanai</span><span class="sxs-lookup"><span data-stu-id="d4bc9-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="d4bc9-169">Citas standarta darbības</span><span class="sxs-lookup"><span data-stu-id="d4bc9-169">Other common operations</span></span>

-   <span data-ttu-id="d4bc9-170">Aiziešana grupā</span><span class="sxs-lookup"><span data-stu-id="d4bc9-170">Bulk Clock-out</span></span>
-   <span data-ttu-id="d4bc9-171">Kavējuma reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="d4bc9-171">Register Absence</span></span>

<span data-ttu-id="d4bc9-172">Plašāku informāciju par to, kā apstrādāt laika un apmeklētības reģistrācijas, skatiet šeit: <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span><span class="sxs-lookup"><span data-stu-id="d4bc9-172">For more information about how to process time and attendance registrations, see <https://technet.microsoft.com/en-us/library/aa573180.aspx>.</span></span>




