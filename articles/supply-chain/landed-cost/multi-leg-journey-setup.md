---
title: Vairākfāžu ceļojuma iestatījums
description: Šajā tēmā ir aprakstīts, kā iestatīt vairākfāžu ceļojumus Kopējo izmaksu modulim.
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 88e1d94f7c3a9b624447c5fc000afc3faab395f1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500434"
---
# <a name="multi-leg-journey-setup"></a><span data-ttu-id="1daaa-103">Vairākfāžu ceļojuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="1daaa-103">Multi-leg journey setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1daaa-104">Šajā tēmā ir aprakstīts, kā iestatīt vairākfāžu ceļojumus **Kopējo izmaksu** modulim.</span><span class="sxs-lookup"><span data-stu-id="1daaa-104">This topic describes how to set up multi-leg journeys for the **Landed cost** module.</span></span>

## <a name="legs"></a><span data-ttu-id="1daaa-105">Fāzes</span><span class="sxs-lookup"><span data-stu-id="1daaa-105">Legs</span></span>

<span data-ttu-id="1daaa-106">Fāzes tiek izmantotas, lai identificētu atsevišķas ceļojuma daļas.</span><span class="sxs-lookup"><span data-stu-id="1daaa-106">Legs are used to identify separate parts of a journey.</span></span> <span data-ttu-id="1daaa-107">Katra varētu būt veidota, atlasot nosūtīšanas ostas "uz" un "no" un šim sūtījumam izmantoto transportēšanas metodi.</span><span class="sxs-lookup"><span data-stu-id="1daaa-107">Each leg is built by selecting the "to" and "from" shipping ports, and the transportation method that is used for that leg.</span></span> <span data-ttu-id="1daaa-108">Izpildes laikus var saistīt ar katru fāzi.</span><span class="sxs-lookup"><span data-stu-id="1daaa-108">Lead times can be associated with each leg.</span></span> <span data-ttu-id="1daaa-109">Izpildes laiki var palīdzēt atsekot kravu, un to var izmantot arī, lai aprēķinātu paredzamo preču piegādes datumu reisā.</span><span class="sxs-lookup"><span data-stu-id="1daaa-109">Lead times can help track a shipment and can also be used to calculate the estimated delivery date of the goods on a voyage.</span></span> <span data-ttu-id="1daaa-110">Turklāt, kad ceļojuma posms ir pabeigts, reisa, nosūtīšanas konteinera un saistīto pirkšanas pasūtījuma rindu statusu var atjaunināt, izmantojot izsekošanas kontroles iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="1daaa-110">Additionally, when a leg of a journey is completed, the status of the voyage, shipping container, and associated purchase order lines can be updated through the tracking control setup.</span></span> <span data-ttu-id="1daaa-111">Ceļus var izmantot ar vienu ceļojuma veidni vai arī tos var atkārtoti izmantot vairākas ceļojuma veidnes.</span><span class="sxs-lookup"><span data-stu-id="1daaa-111">Legs can be used by a single journey template, or they can be reused by multiple journey templates.</span></span> <span data-ttu-id="1daaa-112">Konteinera iekraušana, muita un lokālais transports parasti tiek iestatīts kā fāzes, un tiem tiek izmantota neraksturīga nosūtīšanas osta.</span><span class="sxs-lookup"><span data-stu-id="1daaa-112">Container loading, customs, and local transport are generally set up as legs, and a non-specific shipping port is used for them.</span></span>

<span data-ttu-id="1daaa-113">Lai darbotos ar fāzēm, dodieties uz **Kopējās izmaksas \> Vairākfāžu ceļojuma izmaksas iestatījumi \> Fāzes**.</span><span class="sxs-lookup"><span data-stu-id="1daaa-113">To work with legs, go to **Landed cost \> Multi-leg journey setup \> Legs**.</span></span> <span data-ttu-id="1daaa-114">Tur ir iespējams apskatīt, atvērt, izveidot un dzēst ierakstus par brīvdienām.</span><span class="sxs-lookup"><span data-stu-id="1daaa-114">There, you can view, open, create, and delete records for legs.</span></span> <span data-ttu-id="1daaa-115">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katram ierakstam.</span><span class="sxs-lookup"><span data-stu-id="1daaa-115">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1daaa-116">Lauks</span><span class="sxs-lookup"><span data-stu-id="1daaa-116">Field</span></span> | <span data-ttu-id="1daaa-117">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1daaa-117">Description</span></span> |
|---|---|
| <span data-ttu-id="1daaa-118">Fāze</span><span class="sxs-lookup"><span data-stu-id="1daaa-118">Leg</span></span> | <span data-ttu-id="1daaa-119">Ievadiet nosūtīšanas ostai unikālu ID nosaukumu/numuru.</span><span class="sxs-lookup"><span data-stu-id="1daaa-119">Enter a unique identification name/number for the journey leg.</span></span> |
| <span data-ttu-id="1daaa-120">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1daaa-120">Description</span></span> | <span data-ttu-id="1daaa-121">Ievadiet ceļojuma fāzes aprakstu.</span><span class="sxs-lookup"><span data-stu-id="1daaa-121">Enter a description of the journey leg.</span></span> <span data-ttu-id="1daaa-122">Parasti šis apraksts identificē ostas "uz" un "no" vai ceļojuma soli.</span><span class="sxs-lookup"><span data-stu-id="1daaa-122">Typically, this description identifies the "to" and "from" ports, or the step of the journey.</span></span> |
| <span data-ttu-id="1daaa-123">No ostas</span><span class="sxs-lookup"><span data-stu-id="1daaa-123">From port</span></span> | <span data-ttu-id="1daaa-124">Ievadiet preces izcelsmes punktu fāzei.</span><span class="sxs-lookup"><span data-stu-id="1daaa-124">Enter the point of origin of the goods on the leg.</span></span> |
| <span data-ttu-id="1daaa-125">Uz ostu</span><span class="sxs-lookup"><span data-stu-id="1daaa-125">To port</span></span> | <span data-ttu-id="1daaa-126">Ievadiet preces galapunktu fāzei.</span><span class="sxs-lookup"><span data-stu-id="1daaa-126">Enter the point of destination of the goods on the leg.</span></span> |
| <span data-ttu-id="1daaa-127">Piegādes metode</span><span class="sxs-lookup"><span data-stu-id="1daaa-127">Delivery method</span></span> | <span data-ttu-id="1daaa-128">Ievadiet fāzes transportēšanas veidu.</span><span class="sxs-lookup"><span data-stu-id="1daaa-128">Enter the method of transport for the leg.</span></span> |

## <a name="journey-templates"></a><span data-ttu-id="1daaa-129">Maršruta veidnes</span><span class="sxs-lookup"><span data-stu-id="1daaa-129">Journey templates</span></span>

<span data-ttu-id="1daaa-130">Ceļojuma veidne nosaka vairākfāžu ceļojumu starp divām ostām, no kurām preces tiek transportētas reisa laikā.</span><span class="sxs-lookup"><span data-stu-id="1daaa-130">A journey template defines the multi-leg journey between two ports that goods travel during a voyage.</span></span> <span data-ttu-id="1daaa-131">Ceļojuma posms ir apvienots, lai noteiktu laika daudzumu, kas nepieciešams, lai preces varētu ceļot no kreditora izcelsmes punkta uz gala noliktavas galamērķi.</span><span class="sxs-lookup"><span data-stu-id="1daaa-131">The legs of the journey are combined to identify the amount of time that will be required for goods to travel from the vendor's point of origin to the final warehouse destination.</span></span> <span data-ttu-id="1daaa-132">Kad kravas kravas veidne tiek novietota ceļojuma veidnē, izpildes laiki identificēs katras reisa, konteinera un pirkuma rindu datumu un statusu.</span><span class="sxs-lookup"><span data-stu-id="1daaa-132">When the legs are put on the journey template in a specific order, the lead times will identify the date of each leg and status of the voyage, container, and purchase lines for the voyage.</span></span> <span data-ttu-id="1daaa-133">Lietojiet [Izsekošanas kontroles centru](delivery-information-setup.md), lai iestatītu izpildes laikus, kas ir saistīti ar katru kājai, kas veido ceļojuma veidni.</span><span class="sxs-lookup"><span data-stu-id="1daaa-133">You use the [Tracking control center](delivery-information-setup.md) to set up the lead times that are associated with each leg that makes up the journey template.</span></span> <span data-ttu-id="1daaa-134">Ceļojuma veidni izmanto arī, kad ir iestatītas reisa automātiskās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="1daaa-134">The journey template is also used when the automatic costs of a voyage are set up.</span></span> <span data-ttu-id="1daaa-135">Kad ir definēta transportēšana, ar preču transportēšanu saistītās izmaksas var definēt automātiskās izmaksu lapā.</span><span class="sxs-lookup"><span data-stu-id="1daaa-135">When a journey is defined, the cost that is associated with the transport of the goods can be defined on the auto costs page.</span></span>

<span data-ttu-id="1daaa-136">Lai darbotos ar ceļojuma veidnēm, dodieties uz **Kopējās izmaksas \> Vairākfāžu ceļojuma izmaksas iestatījumi \> Ceļojuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="1daaa-136">To work with journey templates, go to **Landed cost \> Multi-leg journey setup \> Journey templates**.</span></span> <span data-ttu-id="1daaa-137">Tur ir iespējams apskatīt, atvērt, izveidot un dzēst ceļojumu veidnes.</span><span class="sxs-lookup"><span data-stu-id="1daaa-137">There, you can view, open, create, and delete journey templates.</span></span>

<span data-ttu-id="1daaa-138">Katrai ceļojuma veidnei galvenē iestatiet šādus laukus.</span><span class="sxs-lookup"><span data-stu-id="1daaa-138">For each journey template, set the following fields on the header.</span></span>

| <span data-ttu-id="1daaa-139">Lauks</span><span class="sxs-lookup"><span data-stu-id="1daaa-139">Field</span></span> | <span data-ttu-id="1daaa-140">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1daaa-140">Description</span></span> |
|---|---|
| <span data-ttu-id="1daaa-141">Maršruta veidne</span><span class="sxs-lookup"><span data-stu-id="1daaa-141">Journey template</span></span> | <span data-ttu-id="1daaa-142">Ievadiet ceļojuma veidnei unikālu ID nosaukumu/numuru.</span><span class="sxs-lookup"><span data-stu-id="1daaa-142">Enter a unique identification name/number for the journey template.</span></span> <span data-ttu-id="1daaa-143">Parasti ceļojuma veidne raksturo ceļojuma izcelsmes punktu un galamērķa punktu.</span><span class="sxs-lookup"><span data-stu-id="1daaa-143">The journey template typically describes the point of origin and point of destination for the journey.</span></span> |
| <span data-ttu-id="1daaa-144">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1daaa-144">Description</span></span> | <span data-ttu-id="1daaa-145">Ievadiet ceļojumu veidnes aprakstu.</span><span class="sxs-lookup"><span data-stu-id="1daaa-145">Enter a description of the journey template.</span></span> <span data-ttu-id="1daaa-146">Apraksts parasti norāda ostas "uz" un "no" un ceļojuma tipu.</span><span class="sxs-lookup"><span data-stu-id="1daaa-146">The description typically indicates the "to" and "from" ports, and the type of travel.</span></span> |

<span data-ttu-id="1daaa-147">Sadaļā **Rindas** pievienojiet rindu katrai ceļojuma kājai un novietojiet rindas secībā.</span><span class="sxs-lookup"><span data-stu-id="1daaa-147">In the **Lines** section, add a line for each leg of the journey, and put the lines in order.</span></span> <span data-ttu-id="1daaa-148">Lai mainītu rindu secību, rīkjoslā izmantojiet bultiņas **Augšup** un **Lejup**.</span><span class="sxs-lookup"><span data-stu-id="1daaa-148">Use the **Up** and **Down** arrows on the toolbar to change the order of the lines.</span></span> <span data-ttu-id="1daaa-149">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katrai rindai.</span><span class="sxs-lookup"><span data-stu-id="1daaa-149">The following table describes the fields that are available for each line.</span></span>

| <span data-ttu-id="1daaa-150">Lauks</span><span class="sxs-lookup"><span data-stu-id="1daaa-150">Field</span></span> | <span data-ttu-id="1daaa-151">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1daaa-151">Description</span></span> |
|---|---|
| <span data-ttu-id="1daaa-152">Fāze</span><span class="sxs-lookup"><span data-stu-id="1daaa-152">Leg</span></span> | <span data-ttu-id="1daaa-153">Izvēlieties fāzi, ko pievienot ceļojumam.</span><span class="sxs-lookup"><span data-stu-id="1daaa-153">Select a leg to add to the journey.</span></span> |
| <span data-ttu-id="1daaa-154">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1daaa-154">Description</span></span> | <span data-ttu-id="1daaa-155">Fāzes apraksts.</span><span class="sxs-lookup"><span data-stu-id="1daaa-155">The description of the leg.</span></span> |
| <span data-ttu-id="1daaa-156">No ostas</span><span class="sxs-lookup"><span data-stu-id="1daaa-156">From port</span></span> | <span data-ttu-id="1daaa-157">Osta, kas ir preču izcelsmes vieta fāzē.</span><span class="sxs-lookup"><span data-stu-id="1daaa-157">The port that is the point of origin of the goods on the leg.</span></span> <span data-ttu-id="1daaa-158">Šī osta ir osta "uz", kas tiek izmantota, lai noteiktu automātiskās reisa izmaksas.</span><span class="sxs-lookup"><span data-stu-id="1daaa-158">This port is the "to" port that is used to determine the auto costs for a voyage.</span></span> |
| <span data-ttu-id="1daaa-159">Uz ostu</span><span class="sxs-lookup"><span data-stu-id="1daaa-159">To port</span></span> | <span data-ttu-id="1daaa-160">Preču galamērķa osta fāzē.</span><span class="sxs-lookup"><span data-stu-id="1daaa-160">The final destination port of the goods on the leg.</span></span> |
| <span data-ttu-id="1daaa-161">Piegādes veids</span><span class="sxs-lookup"><span data-stu-id="1daaa-161">Mode of delivery</span></span> | <span data-ttu-id="1daaa-162">Piegādes veids, ko izmanto fāzē.</span><span class="sxs-lookup"><span data-stu-id="1daaa-162">The mode of delivery that is used for the leg.</span></span> |
| <span data-ttu-id="1daaa-163">Maršruts no ostas</span><span class="sxs-lookup"><span data-stu-id="1daaa-163">Journey from port</span></span> | <span data-ttu-id="1daaa-164">Ja, lai noteiktu automātiskās izmaksas, tiek izmantota fāzei norādītā osta, atzīmējiet šo izvēles rūtiņu, lai identificētu to kā "ceļojuma no" ostu.</span><span class="sxs-lookup"><span data-stu-id="1daaa-164">If the port that is specified for the leg is used to determine the auto costs, select this check box to identify it as the "journey from" port.</span></span> <span data-ttu-id="1daaa-165">Šī osta tiks parādīta reisa galvenē.</span><span class="sxs-lookup"><span data-stu-id="1daaa-165">This port will be shown on the voyage header.</span></span> |
| <span data-ttu-id="1daaa-166">Maršruts uz ostu</span><span class="sxs-lookup"><span data-stu-id="1daaa-166">Journey to port</span></span> | <span data-ttu-id="1daaa-167">Ja, lai noteiktu automātiskās izmaksas, tiek izmantota fāzei norādītā osta, atzīmējiet šo izvēles rūtiņu, lai identificētu to kā "ceļojuma uz" ostu.</span><span class="sxs-lookup"><span data-stu-id="1daaa-167">If the port that is specified for the leg is used to determine the auto costs, select this check box to identify it as the "journey to" port.</span></span> <span data-ttu-id="1daaa-168">Šī osta tiks parādīta reisa galvenē.</span><span class="sxs-lookup"><span data-stu-id="1daaa-168">This port will be shown on the voyage header.</span></span> |
| <span data-ttu-id="1daaa-169">Nosūtīšanas uzņēmums</span><span class="sxs-lookup"><span data-stu-id="1daaa-169">Shipping company</span></span> | <span data-ttu-id="1daaa-170">Atlasiet sūtīšanas uzņēmumu, kuru izmanto fāzē.</span><span class="sxs-lookup"><span data-stu-id="1daaa-170">Select the shipping company that is used for the leg.</span></span> |

## <a name="activities"></a><span data-ttu-id="1daaa-171">Aktivitātes</span><span class="sxs-lookup"><span data-stu-id="1daaa-171">Activities</span></span>

<span data-ttu-id="1daaa-172">Iestatījumi lapā **Darbības** izveido aktivitāšu tipus, kas var rasties kādā ostas fāzē.</span><span class="sxs-lookup"><span data-stu-id="1daaa-172">The settings on the **Activities** page establish the types of activities that can occur at the destination port of a leg.</span></span> <span data-ttu-id="1daaa-173">Lietotāji, kuri strādā lapā **Visi pārvadāšanas konteineri**, var izvēlēties starp šīm vērtībām, kad tie novērtē katras aktivitātes ilgumu un reģistrē faktisko ilgumu salīdzināšanas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="1daaa-173">Users who work on the **All shipping containers** page can select among these values when they estimate the duration of each activity and record the actual duration for comparison purposes.</span></span>

<span data-ttu-id="1daaa-174">Lai iestatītu savas aktivitātes, dodieties uz **Kopējās izmaksas \> Vairākfāžu ceļojumu iestatīšana \> Darbības**.</span><span class="sxs-lookup"><span data-stu-id="1daaa-174">To set up your activities, go to **Landed cost \> Multi-leg journeys setup \> Activities**.</span></span> <span data-ttu-id="1daaa-175">Jūs varat izmantot pogas Darbību rūtī, lai pievienotu, noņemtu un rediģētu darbības.</span><span class="sxs-lookup"><span data-stu-id="1daaa-175">There, you can add, remove, and edit activities by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="1daaa-176">Tālāk esošajā tabulā ir aprakstīti pieejamie lauki katrai darbībai režģī.</span><span class="sxs-lookup"><span data-stu-id="1daaa-176">The following table describes the fields that are available for each activity in the grid.</span></span>

| <span data-ttu-id="1daaa-177">Lauks</span><span class="sxs-lookup"><span data-stu-id="1daaa-177">Field</span></span> | <span data-ttu-id="1daaa-178">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1daaa-178">Description</span></span> |
|---|---|
| <span data-ttu-id="1daaa-179">Aktivitāte</span><span class="sxs-lookup"><span data-stu-id="1daaa-179">Activity</span></span> | <span data-ttu-id="1daaa-180">Darbības nosaukums.</span><span class="sxs-lookup"><span data-stu-id="1daaa-180">The name of the activity.</span></span> |
| <span data-ttu-id="1daaa-181">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1daaa-181">Description</span></span> | <span data-ttu-id="1daaa-182">Darbības apraksts.</span><span class="sxs-lookup"><span data-stu-id="1daaa-182">A description of the activity.</span></span> |
| <span data-ttu-id="1daaa-183">Nosūtīšanas uzņēmums</span><span class="sxs-lookup"><span data-stu-id="1daaa-183">Shipping company</span></span> | <span data-ttu-id="1daaa-184">Atlasiet nosūtīšanas uzņēmuma kreditora kontu, kas ir saistīts ar darbību.</span><span class="sxs-lookup"><span data-stu-id="1daaa-184">The vendor account of the shipping company that is associated with the activity.</span></span> |