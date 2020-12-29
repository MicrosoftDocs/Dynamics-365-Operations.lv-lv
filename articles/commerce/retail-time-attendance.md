---
title: Laika un apmeklētības pārvaldība programmā Retail
description: Šajā tēmā ir aprakstīti scenāriji, kas tiek atbalstīti laika un apmeklētības pārvaldībai programmā Dynamics 365 Commerce.
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
ms.openlocfilehash: cca5e3232450e75f931a621b278c134129fc745c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414168"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="b6925-103">Laika un apmeklētības pārvaldība programmā Retail</span><span class="sxs-lookup"><span data-stu-id="b6925-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b6925-104">Šajā tēmā ir aprakstīti scenāriji, kas tiek atbalstīti laika un apmeklētības pārvaldībai programmā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b6925-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Commerce.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="b6925-105">Darbinieku iestatījumu un plānošanas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="b6925-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="b6925-106"> sākotnējā konfigurācija</span><span class="sxs-lookup"><span data-stu-id="b6925-106">Initial configuration</span></span>

- <span data-ttu-id="b6925-107">Palaidiet konfigurācijas vedni.</span><span class="sxs-lookup"><span data-stu-id="b6925-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="b6925-108">Reģistrējiet darbiniekus kā laika reģistrācijas darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="b6925-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="b6925-109">Darbinieku grafika plānošana</span><span class="sxs-lookup"><span data-stu-id="b6925-109">Plan worker schedules</span></span>

- <span data-ttu-id="b6925-110">Izveidojiet profilus, izmantojot darbu plānošanas sistēmu.</span><span class="sxs-lookup"><span data-stu-id="b6925-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="b6925-111">Papildinformāciju skatiet tēmā [Profilu izveide, izmantojot darbu plānošanas sistēmu](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6925-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="b6925-112">Papildinformāciju par konfigurācijas darbībām skatiet tēmā [Laika un apmeklētības iestatīšana](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6925-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="commerce-specific-configuration"></a><span data-ttu-id="b6925-113">Commerce paredzēta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="b6925-113">Commerce-specific configuration</span></span>

- <span data-ttu-id="b6925-114">Iespējojiet funkcionalitātes Laika uzskaite profilu darbiniekiem, kuriem vēlaties aktivizēt laika reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="b6925-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="b6925-115">Noklikšķiniet uz **POS funkcionalitātes profili** &gt; **Funkcijas** &gt; **POS laika reģistrācijas** &gt; **Aktivizēt laika reģistrācijas**.</span><span class="sxs-lookup"><span data-stu-id="b6925-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="b6925-116">Konfigurējiet pārdošanas punkta (POS) atļaujas grupas, lai iespējotu funkcijas Skatīt laika uzskaites ierakstus atļauju.</span><span class="sxs-lookup"><span data-stu-id="b6925-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="b6925-117">Ar šo atļauju lietotājs var skatīt citu veikala (un citu veikalu, ar kuriem lietotājs ir saistīts, izmantojot adrešu grāmatu) darbinieku laika uzskaites reģistrācijas ierakstus.</span><span class="sxs-lookup"><span data-stu-id="b6925-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="b6925-118">Šo atļauju ieteicams aktivizēt vadītāja lomai, bet ne kasiera lomai.</span><span class="sxs-lookup"><span data-stu-id="b6925-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="b6925-119">Noklikšķiniet uz **POS atļauju grupas** &gt; **Skatīt darba laika uzskaites ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="b6925-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="b6925-120">Reģistra laiks</span><span class="sxs-lookup"><span data-stu-id="b6925-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="b6925-121">Kasiera un darbinieka, kas nav kasieris, laika reģistrācija</span><span class="sxs-lookup"><span data-stu-id="b6925-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="b6925-122">Pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="b6925-122">On POS:</span></span>

    - <span data-ttu-id="b6925-123">Ar ierašanos saistītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b6925-123">Clock-in operations:</span></span>

        - <span data-ttu-id="b6925-124">Piesakieties, veicot ar naudas kasti nesaistītu darbību, vai sadaļā Jaunu maiņa.</span><span class="sxs-lookup"><span data-stu-id="b6925-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="b6925-125">Atlasiet darbību Laika uzskaite.</span><span class="sxs-lookup"><span data-stu-id="b6925-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="b6925-126">Atlasiet vēlamo darbību.</span><span class="sxs-lookup"><span data-stu-id="b6925-126">Select a desired operation:</span></span>

            - <span data-ttu-id="b6925-127">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="b6925-127">Clock-in</span></span>
            - <span data-ttu-id="b6925-128">Darba pārtraukums</span><span class="sxs-lookup"><span data-stu-id="b6925-128">Break for Work</span></span>
            - <span data-ttu-id="b6925-129">Pusdienu pārtraukums</span><span class="sxs-lookup"><span data-stu-id="b6925-129">Break for Lunch</span></span>
            - <span data-ttu-id="b6925-130">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="b6925-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="b6925-131">Pašreizējais statuss</span><span class="sxs-lookup"><span data-stu-id="b6925-131">Current state</span></span></th>
        <th><span data-ttu-id="b6925-132">Pieejamās darbības</span><span class="sxs-lookup"><span data-stu-id="b6925-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="b6925-133">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="b6925-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="b6925-134">Darba pārtraukums</span><span class="sxs-lookup"><span data-stu-id="b6925-134">Break for Work</span></span></li>
        <li><span data-ttu-id="b6925-135">Pusdienu pārtraukums</span><span class="sxs-lookup"><span data-stu-id="b6925-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="b6925-136">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="b6925-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="b6925-137">Darba pārtraukums</span><span class="sxs-lookup"><span data-stu-id="b6925-137">Break for Work</span></span></td>
        <td><span data-ttu-id="b6925-138">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="b6925-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="b6925-139">Pusdienu pārtraukums</span><span class="sxs-lookup"><span data-stu-id="b6925-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="b6925-140">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="b6925-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="b6925-141">Aiziešana</span><span class="sxs-lookup"><span data-stu-id="b6925-141">Clock-out</span></span></td>
        <td><span data-ttu-id="b6925-142">Ierašanās</span><span class="sxs-lookup"><span data-stu-id="b6925-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="b6925-143">[![Laika uzskaites stāvokļi](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="b6925-143">[![Time Clock States](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="b6925-144">Skatiet apstiprinājuma ziņojumu un pārbaudiet, vai pašreizējais aktivitātes laiks ir pareizs.</span><span class="sxs-lookup"><span data-stu-id="b6925-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="b6925-145">Reģistrācijas žurnāls</span><span class="sxs-lookup"><span data-stu-id="b6925-145">Logbook:</span></span>

    - <span data-ttu-id="b6925-146">Noklikšķiniet uz **Reģistrācijas žurnāls**, lai skatītu laika uzskaite aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="b6925-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="b6925-147">Izmantojiet laika filtrus, lai atlasītu dažādus laika logus.</span><span class="sxs-lookup"><span data-stu-id="b6925-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="b6925-148">Ja strādājat vairākās veikala atrašanās vietās, laika reģistrācijas ieraksti ir redzami par visiem veikaliem, kuros ir reģistrēts laiks.</span><span class="sxs-lookup"><span data-stu-id="b6925-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="b6925-149">Lai skatītu atlasītajā veikalā veiktās laika reģistrācijas, var izmantot veikalu filtru.</span><span class="sxs-lookup"><span data-stu-id="b6925-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="b6925-150">Atšķirīgas laika zonas</span><span class="sxs-lookup"><span data-stu-id="b6925-150">Different time zones:</span></span>

    - <span data-ttu-id="b6925-151">Ja tiek skatīta laika uzskaite no citas atrašanās vietas (kasiera žurnālā vai izmantojot vadītāja scenārija opciju **Skatīt laika uzskaites ierakstus**) un šī atrašanās vieta atrodas citā laika joslā, redzamie laika uzskaites ieraksti tiek pārvērsti atbilstoši vietējai laika joslai.</span><span class="sxs-lookup"><span data-stu-id="b6925-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="b6925-152">Piemēram, pieņemsim, ka esat divu veikalu vadītājs, no kuriem viens atrodas Arizonā, bet otrs atrodas Nevadā.</span><span class="sxs-lookup"><span data-stu-id="b6925-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="b6925-153">Kasieris reģistrē ierašanos 9:00</span><span class="sxs-lookup"><span data-stu-id="b6925-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="b6925-154">pēc Arizonas laika.</span><span class="sxs-lookup"><span data-stu-id="b6925-154">in Arizona.</span></span> <span data-ttu-id="b6925-155">Šajā brīdī Nevadā ir 8:00.</span><span class="sxs-lookup"><span data-stu-id="b6925-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="b6925-156">Tāpēc, ja atrodaties veikalā Nevadā un skatāt laika reģistrācijas ierakstus, ir redzams, ka laika reģistrācija ir atzīmēta 8:00.</span><span class="sxs-lookup"><span data-stu-id="b6925-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="b6925-157">Darbinieku laika reģistrācijas ierakstu skatīšana</span><span class="sxs-lookup"><span data-stu-id="b6925-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="b6925-158">Skatiet darbinieka laika reģistrācijas ierakstus un filtrējiet tos pēc veikala vai aktivitātes tipa.</span><span class="sxs-lookup"><span data-stu-id="b6925-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="b6925-159">Pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="b6925-159">On POS:</span></span>

- <span data-ttu-id="b6925-160">Atlasiet opciju **Skatīt laika uzskaites ierakstus**.</span><span class="sxs-lookup"><span data-stu-id="b6925-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="b6925-161">Var skatīt visu to darbinieku laika uzskaites reģistrācijas darbības, kas iedalīti tajos pašos veikalos, kur esat iedalīts jūs.</span><span class="sxs-lookup"><span data-stu-id="b6925-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="b6925-162">Lai filtrētu laika reģistrācijas ierakstus, var izmantot aktivitātes tipa un veikala filtru.</span><span class="sxs-lookup"><span data-stu-id="b6925-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="b6925-163">Laika reģistrācijas ierakstu apstrāde un pārvaldība</span><span class="sxs-lookup"><span data-stu-id="b6925-163">Process and manage time registrations</span></span>

<span data-ttu-id="b6925-164">Commerce lietotājs izpilda darbplūsmu, lai aprēķinātu, apstiprinātu un pārsūtītu laika reģistrācijas ierakstus algas aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="b6925-164">A Commerce user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="b6925-165">Primārās darbības</span><span class="sxs-lookup"><span data-stu-id="b6925-165">Primary operations</span></span>

- <span data-ttu-id="b6925-166">Aprēķināt</span><span class="sxs-lookup"><span data-stu-id="b6925-166">Calculate</span></span>
- <span data-ttu-id="b6925-167">Apstiprināt</span><span class="sxs-lookup"><span data-stu-id="b6925-167">Approve</span></span>
- <span data-ttu-id="b6925-168">Iesniegt algas aprēķināšanai</span><span class="sxs-lookup"><span data-stu-id="b6925-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="b6925-169">Citas standarta darbības</span><span class="sxs-lookup"><span data-stu-id="b6925-169">Other common operations</span></span>

- <span data-ttu-id="b6925-170">Aiziešana grupā</span><span class="sxs-lookup"><span data-stu-id="b6925-170">Bulk Clock-out</span></span>
- <span data-ttu-id="b6925-171">Kavējuma reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="b6925-171">Register Absence</span></span>

<span data-ttu-id="b6925-172">Papildinformāciju par laika un apmeklētības ierakstu apstrādi skatiet tēmā[Laika un apmeklētības ierakstu apstrāde](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="b6925-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
