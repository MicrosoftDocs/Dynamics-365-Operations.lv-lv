---
title: Svītrkoda skeneru atbalsts Kanban pārsūtīšanas panelī
description: Kanban pārsūtīšanas panelis nodrošina skenera ievadi, izmantojot logrīka svītrkoda skeneri, lai atlasītu, sāktu, pabeigtu un iztukšotu Kanban darbu.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63a33af63144b78d0c375022b9802e11c255598
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "319458"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="23f5d-103">Svītrkoda skeneru atbalsts Kanban pārsūtīšanas panelī</span><span class="sxs-lookup"><span data-stu-id="23f5d-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23f5d-104">Kanban pārsūtīšanas panelis nodrošina skenera ievadi, izmantojot logrīka svītrkoda skeneri, lai atlasītu, sāktu, pabeigtu un iztukšotu Kanban darbu.</span><span class="sxs-lookup"><span data-stu-id="23f5d-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="23f5d-105">Reģistrācijas režīmi</span><span class="sxs-lookup"><span data-stu-id="23f5d-105">Registration modes</span></span>
------------------

<span data-ttu-id="23f5d-106">Kopsavilkuma cilnē **Skenera reģistrācija** varat atlasīt reģistrācijas režīmu, kas nosaka to, kāda darbība tiek veikta, skenējot Kanban kartes numuru vai manuāli ievadot numuru laukā Kanban kartes numurs.</span><span class="sxs-lookup"><span data-stu-id="23f5d-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="23f5d-107">Iestatīt reģistrācijas režīmu</span><span class="sxs-lookup"><span data-stu-id="23f5d-107">Set registration mode</span></span> | <span data-ttu-id="23f5d-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="23f5d-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f5d-109">Sākums</span><span class="sxs-lookup"><span data-stu-id="23f5d-109">Start</span></span>                 | <span data-ttu-id="23f5d-110">Kanban pārsūtīšanas darbs tiek reģistrēts kā notiekošs.</span><span class="sxs-lookup"><span data-stu-id="23f5d-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="23f5d-111">Pabeigt</span><span class="sxs-lookup"><span data-stu-id="23f5d-111">Complete</span></span>              | <span data-ttu-id="23f5d-112">Kanban pārsūtīšanas darbs tiek reģistrēts kā pabeigts.</span><span class="sxs-lookup"><span data-stu-id="23f5d-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="23f5d-113">Tukšs</span><span class="sxs-lookup"><span data-stu-id="23f5d-113">Empty</span></span>                 | <span data-ttu-id="23f5d-114">Materiālu apstrādes vienība, uz ko ir atsauces Kanban kartē, tiek reģistrēta kā tukša.</span><span class="sxs-lookup"><span data-stu-id="23f5d-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="23f5d-115">Atlasīt</span><span class="sxs-lookup"><span data-stu-id="23f5d-115">Select</span></span>                | <span data-ttu-id="23f5d-116">Tiek reģistrēts Kanban kartes numurs, un Kanban sarakstā tiek automātiski atlasīts atsauces darbs.</span><span class="sxs-lookup"><span data-stu-id="23f5d-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="23f5d-117">Reģistrācijas režīms Atlasīt</span><span class="sxs-lookup"><span data-stu-id="23f5d-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="23f5d-118">Ja izmantojat svītrkoda lasītāju, lai atlasītu darbu, tiek mainīts Kanban paneļa rādīšanas režīms.</span><span class="sxs-lookup"><span data-stu-id="23f5d-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="23f5d-119"> Šajā režīmā ir spēkā tālāk norādītie nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="23f5d-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="23f5d-120">Tiek rādīts tikai ieskenētais Kanban darbs.</span><span class="sxs-lookup"><span data-stu-id="23f5d-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="23f5d-121">Kopsavilkuma cilnē **Detalizēti** tiek rādīta detalizēta informācija par atlasīto darbu.</span><span class="sxs-lookup"><span data-stu-id="23f5d-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="23f5d-122">Kopsavilkuma cilnē **Ziņojumi** tiek rādīti tikai ar atlasīto darbu saistītie ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="23f5d-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="23f5d-123">Darba statusu var mainīt, izmantojot darbību rūti pieejamās funkcijas.</span><span class="sxs-lookup"><span data-stu-id="23f5d-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="23f5d-124">Šajā laikā Kanban pārsūtīšanas panelī joprojām tiek rādīts tikai viens darbs.</span><span class="sxs-lookup"><span data-stu-id="23f5d-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="23f5d-125">Varat manuāli atjaunināt informāciju darbu sarakstā, darbību rūti noklikšķinot uz **Atsvaidzināt** (Shift+F5).</span><span class="sxs-lookup"><span data-stu-id="23f5d-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="23f5d-126">Pēc informācijas atsvaidzināšanas atkal tiek rādīti visi darbu filtra rezultāti.</span><span class="sxs-lookup"><span data-stu-id="23f5d-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="23f5d-127">Darbu statuss un iespējamās darbības</span><span class="sxs-lookup"><span data-stu-id="23f5d-127">Job status and possible actions</span></span>
<span data-ttu-id="23f5d-128">Atlasīta darba statuss un jebkuru notikumu Kanban piesaistīto darbu statuss nosaka, vai varat turpināt darba apstrādi.</span><span class="sxs-lookup"><span data-stu-id="23f5d-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="23f5d-129">Tālāk esošajā tabulā ir sniegta informācija par šiem statusiem un uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="23f5d-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="23f5d-130">Statusi, kas ir pieejami darbiem vai materiālu apstrādes vienībām, uz kurām ir atsauces šajos darbos.</span><span class="sxs-lookup"><span data-stu-id="23f5d-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="23f5d-131">Katrs uzdevums, ko varat veikt konkrētajam darbam.</span><span class="sxs-lookup"><span data-stu-id="23f5d-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23f5d-132">Darba tips</span><span class="sxs-lookup"><span data-stu-id="23f5d-132">Job type</span></span></th>
<th><span data-ttu-id="23f5d-133">Darba statuss vai materiālu apstrādes vienības statuss</span><span class="sxs-lookup"><span data-stu-id="23f5d-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="23f5d-134">Atjauniniet izdošanas sarakstu</span><span class="sxs-lookup"><span data-stu-id="23f5d-134">Update picking list</span></span></th>
<th><span data-ttu-id="23f5d-135">Sākums</span><span class="sxs-lookup"><span data-stu-id="23f5d-135">Start</span></span></th>
<th><span data-ttu-id="23f5d-136">Atjaunināt reģistrāciju</span><span class="sxs-lookup"><span data-stu-id="23f5d-136">Update registration</span></span></th>
<th><span data-ttu-id="23f5d-137">Pabeigt</span><span class="sxs-lookup"><span data-stu-id="23f5d-137">Complete</span></span></th>
<th><span data-ttu-id="23f5d-138">Tukšs</span><span class="sxs-lookup"><span data-stu-id="23f5d-138">Empty</span></span></th>
<th><span data-ttu-id="23f5d-139">Izveidot notikumu Kanban</span><span class="sxs-lookup"><span data-stu-id="23f5d-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23f5d-140">Pārcelšana</span><span class="sxs-lookup"><span data-stu-id="23f5d-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="23f5d-141">Neplānots</span><span class="sxs-lookup"><span data-stu-id="23f5d-141">Not planned</span></span></li>
<li><span data-ttu-id="23f5d-142">Nav piesaistīto darbu, vai piesaistītie darbi ir pabeigti</span><span class="sxs-lookup"><span data-stu-id="23f5d-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="23f5d-143">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-143">Yes</span></span></td>
<td><span data-ttu-id="23f5d-144">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-144">Yes</span></span></td>
<td><span data-ttu-id="23f5d-145">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-145">Yes</span></span></td>
<td><span data-ttu-id="23f5d-146">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-146">Yes</span></span></td>
<td><span data-ttu-id="23f5d-147">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-147">No</span></span></td>
<td><span data-ttu-id="23f5d-148">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23f5d-149">Pārcelšana</span><span class="sxs-lookup"><span data-stu-id="23f5d-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="23f5d-150">Neplānots</span><span class="sxs-lookup"><span data-stu-id="23f5d-150">Not planned</span></span></li>
<li><span data-ttu-id="23f5d-151">Piesaistītais darbs nav pabeigts</span><span class="sxs-lookup"><span data-stu-id="23f5d-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="23f5d-152">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-152">Yes</span></span></td>
<td><span data-ttu-id="23f5d-153">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-153">No</span></span></td>
<td><span data-ttu-id="23f5d-154">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-154">Yes</span></span></td>
<td><span data-ttu-id="23f5d-155">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-155">No</span></span></td>
<td><span data-ttu-id="23f5d-156">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-156">No</span></span></td>
<td><span data-ttu-id="23f5d-157">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23f5d-158">Pārcelšana</span><span class="sxs-lookup"><span data-stu-id="23f5d-158">Transfer</span></span></td>
<td><span data-ttu-id="23f5d-159">Notiek</span><span class="sxs-lookup"><span data-stu-id="23f5d-159">In progress</span></span></td>
<td><span data-ttu-id="23f5d-160">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-160">Yes</span></span></td>
<td><span data-ttu-id="23f5d-161">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-161">No</span></span></td>
<td><span data-ttu-id="23f5d-162">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-162">Yes</span></span></td>
<td><span data-ttu-id="23f5d-163">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-163">Yes</span></span></td>
<td><span data-ttu-id="23f5d-164">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-164">No</span></span></td>
<td><span data-ttu-id="23f5d-165">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23f5d-166">Pārcelšana</span><span class="sxs-lookup"><span data-stu-id="23f5d-166">Transfer</span></span></td>
<td><span data-ttu-id="23f5d-167">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="23f5d-167">Completed</span></span></td>
<td><span data-ttu-id="23f5d-168">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-168">No</span></span></td>
<td><span data-ttu-id="23f5d-169">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-169">No</span></span></td>
<td><span data-ttu-id="23f5d-170">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-170">No</span></span></td>
<td><span data-ttu-id="23f5d-171">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-171">No</span></span></td>
<td><span data-ttu-id="23f5d-172">Jā</span><span class="sxs-lookup"><span data-stu-id="23f5d-172">Yes</span></span></td>
<td><span data-ttu-id="23f5d-173">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23f5d-174">Pārsūtīšana vai apstrāde</span><span class="sxs-lookup"><span data-stu-id="23f5d-174">Transfer or process</span></span></td>
<td><span data-ttu-id="23f5d-175">Tukšs</span><span class="sxs-lookup"><span data-stu-id="23f5d-175">Empty</span></span></td>
<td><span data-ttu-id="23f5d-176">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-176">No</span></span></td>
<td><span data-ttu-id="23f5d-177">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-177">No</span></span></td>
<td><span data-ttu-id="23f5d-178">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-178">No</span></span></td>
<td><span data-ttu-id="23f5d-179">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-179">No</span></span></td>
<td><span data-ttu-id="23f5d-180">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-180">No</span></span></td>
<td><span data-ttu-id="23f5d-181">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23f5d-182">Pārsūtīšana vai apstrāde</span><span class="sxs-lookup"><span data-stu-id="23f5d-182">Transfer or process</span></span></td>
<td><span data-ttu-id="23f5d-183">Nav atrasta Kanban karte</span><span class="sxs-lookup"><span data-stu-id="23f5d-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="23f5d-184">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-184">No</span></span></td>
<td><span data-ttu-id="23f5d-185">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-185">No</span></span></td>
<td><span data-ttu-id="23f5d-186">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-186">No</span></span></td>
<td><span data-ttu-id="23f5d-187">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-187">No</span></span></td>
<td><span data-ttu-id="23f5d-188">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-188">No</span></span></td>
<td><span data-ttu-id="23f5d-189">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23f5d-190">Pārsūtīšana vai apstrāde</span><span class="sxs-lookup"><span data-stu-id="23f5d-190">Transfer or process</span></span></td>
<td><span data-ttu-id="23f5d-191">Ir atrasta Kanban karte, taču tā nav piešķirta Kanban</span><span class="sxs-lookup"><span data-stu-id="23f5d-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="23f5d-192">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-192">No</span></span></td>
<td><span data-ttu-id="23f5d-193">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-193">No</span></span></td>
<td><span data-ttu-id="23f5d-194">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-194">No</span></span></td>
<td><span data-ttu-id="23f5d-195">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-195">No</span></span></td>
<td><span data-ttu-id="23f5d-196">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-196">No</span></span></td>
<td><span data-ttu-id="23f5d-197">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23f5d-198">Apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="23f5d-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="23f5d-199">Neplānots</span><span class="sxs-lookup"><span data-stu-id="23f5d-199">Not planned</span></span></li>
<li><span data-ttu-id="23f5d-200">Sagatavots</span><span class="sxs-lookup"><span data-stu-id="23f5d-200">Prepared</span></span></li>
<li><span data-ttu-id="23f5d-201">Notiek</span><span class="sxs-lookup"><span data-stu-id="23f5d-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="23f5d-202">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-202">No</span></span></td>
<td><span data-ttu-id="23f5d-203">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-203">No</span></span></td>
<td><span data-ttu-id="23f5d-204">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-204">No</span></span></td>
<td><span data-ttu-id="23f5d-205">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-205">No</span></span></td>
<td><span data-ttu-id="23f5d-206">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-206">No</span></span></td>
<td><span data-ttu-id="23f5d-207">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23f5d-208">Apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="23f5d-208">Process</span></span></td>
<td><span data-ttu-id="23f5d-209">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="23f5d-209">Completed</span></span></td>
<td><span data-ttu-id="23f5d-210">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-210">No</span></span></td>
<td><span data-ttu-id="23f5d-211">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-211">No</span></span></td>
<td><span data-ttu-id="23f5d-212">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-212">No</span></span></td>
<td><span data-ttu-id="23f5d-213">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-213">No</span></span></td>
<td><span data-ttu-id="23f5d-214">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-214">No</span></span></td>
<td><span data-ttu-id="23f5d-215">Nē</span><span class="sxs-lookup"><span data-stu-id="23f5d-215">No</span></span></td>
</tr>
</tbody>
</table>





