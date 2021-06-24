---
title: Svītrkoda skeneru atbalsts Kanban pārsūtīšanas panelī
description: Kanban pārsūtīšanas panelis nodrošina skenera ievadi, izmantojot logrīka svītrkoda skeneri, lai atlasītu, sāktu, pabeigtu un iztukšotu Kanban darbu.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c48c4737c260004ea44109cfb2a0478a3e8653cc
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190068"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="810c8-103">Svītrkoda skeneru atbalsts Kanban pārsūtīšanas panelī</span><span class="sxs-lookup"><span data-stu-id="810c8-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="810c8-104">Kanban pārsūtīšanas panelis nodrošina skenera ievadi, izmantojot logrīka svītrkoda skeneri, lai atlasītu, sāktu, pabeigtu un iztukšotu Kanban darbu.</span><span class="sxs-lookup"><span data-stu-id="810c8-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

## <a name="registration-modes"></a><span data-ttu-id="810c8-105">Reģistrācijas režīmi</span><span class="sxs-lookup"><span data-stu-id="810c8-105">Registration modes</span></span>

<span data-ttu-id="810c8-106">Kopsavilkuma cilnē **Skenera reģistrācija** varat atlasīt reģistrācijas režīmu, kas nosaka to, kāda darbība tiek veikta, skenējot Kanban kartes numuru vai manuāli ievadot numuru laukā Kanban kartes numurs.</span><span class="sxs-lookup"><span data-stu-id="810c8-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="810c8-107">Iestatīt reģistrācijas režīmu</span><span class="sxs-lookup"><span data-stu-id="810c8-107">Set registration mode</span></span> | <span data-ttu-id="810c8-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="810c8-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="810c8-109">Sākums</span><span class="sxs-lookup"><span data-stu-id="810c8-109">Start</span></span>                 | <span data-ttu-id="810c8-110">Kanban pārsūtīšanas darbs tiek reģistrēts kā notiekošs.</span><span class="sxs-lookup"><span data-stu-id="810c8-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="810c8-111">Pabeigt</span><span class="sxs-lookup"><span data-stu-id="810c8-111">Complete</span></span>              | <span data-ttu-id="810c8-112">Kanban pārsūtīšanas darbs tiek reģistrēts kā pabeigts.</span><span class="sxs-lookup"><span data-stu-id="810c8-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="810c8-113">Tukšs</span><span class="sxs-lookup"><span data-stu-id="810c8-113">Empty</span></span>                 | <span data-ttu-id="810c8-114">Materiālu apstrādes vienība, uz ko ir atsauces Kanban kartē, tiek reģistrēta kā tukša.</span><span class="sxs-lookup"><span data-stu-id="810c8-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="810c8-115">Atlasīt</span><span class="sxs-lookup"><span data-stu-id="810c8-115">Select</span></span>                | <span data-ttu-id="810c8-116">Tiek reģistrēts Kanban kartes numurs, un Kanban sarakstā tiek automātiski atlasīts atsauces darbs.</span><span class="sxs-lookup"><span data-stu-id="810c8-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
## <a name="registration-mode-select"></a><span data-ttu-id="810c8-117">Reģistrācijas režīms Atlasīt</span><span class="sxs-lookup"><span data-stu-id="810c8-117">Registration mode Select</span></span>

<span data-ttu-id="810c8-118">Ja izmantojat svītrkoda lasītāju, lai atlasītu darbu, tiek mainīts Kanban paneļa rādīšanas režīms.</span><span class="sxs-lookup"><span data-stu-id="810c8-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="810c8-119">Šajā režīmā ir spēkā šādi nosacījumi:</span><span class="sxs-lookup"><span data-stu-id="810c8-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="810c8-120">Tiek rādīts tikai ieskenētais Kanban darbs.</span><span class="sxs-lookup"><span data-stu-id="810c8-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="810c8-121">Kopsavilkuma cilnē **Detalizēti** tiek rādīta detalizēta informācija par atlasīto darbu.</span><span class="sxs-lookup"><span data-stu-id="810c8-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="810c8-122">Kopsavilkuma cilnē **Ziņojumi** tiek rādīti tikai ar atlasīto darbu saistītie ziņojumi.</span><span class="sxs-lookup"><span data-stu-id="810c8-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="810c8-123">Darba statusu var mainīt, izmantojot darbību rūti pieejamās funkcijas.</span><span class="sxs-lookup"><span data-stu-id="810c8-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="810c8-124">Šajā laikā Kanban pārsūtīšanas panelī joprojām tiek rādīts tikai viens darbs.</span><span class="sxs-lookup"><span data-stu-id="810c8-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="810c8-125">Varat manuāli atjaunināt informāciju darbu sarakstā, darbību rūti noklikšķinot uz **Atsvaidzināt** (Shift+F5).</span><span class="sxs-lookup"><span data-stu-id="810c8-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="810c8-126">Pēc informācijas atsvaidzināšanas atkal tiek rādīti visi darbu filtra rezultāti.</span><span class="sxs-lookup"><span data-stu-id="810c8-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="810c8-127">Darbu statuss un iespējamās darbības</span><span class="sxs-lookup"><span data-stu-id="810c8-127">Job status and possible actions</span></span>
<span data-ttu-id="810c8-128">Atlasīta darba statuss un jebkuru notikumu Kanban piesaistīto darbu statuss nosaka, vai varat turpināt darba apstrādi.</span><span class="sxs-lookup"><span data-stu-id="810c8-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="810c8-129">Tālāk esošajā tabulā ir sniegta informācija par šiem statusiem un uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="810c8-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="810c8-130">Statusi, kas ir pieejami darbiem vai materiālu apstrādes vienībām, uz kurām ir atsauces šajos darbos.</span><span class="sxs-lookup"><span data-stu-id="810c8-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="810c8-131">Katrs uzdevums, ko varat veikt konkrētajam darbam.</span><span class="sxs-lookup"><span data-stu-id="810c8-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="810c8-132">Darba tips</span><span class="sxs-lookup"><span data-stu-id="810c8-132">Job type</span></span></th>
<th><span data-ttu-id="810c8-133">Darba statuss vai materiālu apstrādes vienības statuss</span><span class="sxs-lookup"><span data-stu-id="810c8-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="810c8-134">Atjauniniet izdošanas sarakstu</span><span class="sxs-lookup"><span data-stu-id="810c8-134">Update picking list</span></span></th>
<th><span data-ttu-id="810c8-135">Sākums</span><span class="sxs-lookup"><span data-stu-id="810c8-135">Start</span></span></th>
<th><span data-ttu-id="810c8-136">Atjaunināt reģistrāciju</span><span class="sxs-lookup"><span data-stu-id="810c8-136">Update registration</span></span></th>
<th><span data-ttu-id="810c8-137">Pabeigt</span><span class="sxs-lookup"><span data-stu-id="810c8-137">Complete</span></span></th>
<th><span data-ttu-id="810c8-138">Tukšs</span><span class="sxs-lookup"><span data-stu-id="810c8-138">Empty</span></span></th>
<th><span data-ttu-id="810c8-139">Izveidot notikumu Kanban</span><span class="sxs-lookup"><span data-stu-id="810c8-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="810c8-140">Pārcelšana</span><span class="sxs-lookup"><span data-stu-id="810c8-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="810c8-141">Neplānots</span><span class="sxs-lookup"><span data-stu-id="810c8-141">Not planned</span></span></li>
<li><span data-ttu-id="810c8-142">Nav piesaistīto darbu, vai piesaistītie darbi ir pabeigti</span><span class="sxs-lookup"><span data-stu-id="810c8-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="810c8-143">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-143">Yes</span></span></td>
<td><span data-ttu-id="810c8-144">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-144">Yes</span></span></td>
<td><span data-ttu-id="810c8-145">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-145">Yes</span></span></td>
<td><span data-ttu-id="810c8-146">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-146">Yes</span></span></td>
<td><span data-ttu-id="810c8-147">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-147">No</span></span></td>
<td><span data-ttu-id="810c8-148">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810c8-149">Pārcelšana</span><span class="sxs-lookup"><span data-stu-id="810c8-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="810c8-150">Neplānots</span><span class="sxs-lookup"><span data-stu-id="810c8-150">Not planned</span></span></li>
<li><span data-ttu-id="810c8-151">Piesaistītais darbs nav pabeigts</span><span class="sxs-lookup"><span data-stu-id="810c8-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="810c8-152">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-152">Yes</span></span></td>
<td><span data-ttu-id="810c8-153">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-153">No</span></span></td>
<td><span data-ttu-id="810c8-154">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-154">Yes</span></span></td>
<td><span data-ttu-id="810c8-155">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-155">No</span></span></td>
<td><span data-ttu-id="810c8-156">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-156">No</span></span></td>
<td><span data-ttu-id="810c8-157">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810c8-158">Pārcelšana</span><span class="sxs-lookup"><span data-stu-id="810c8-158">Transfer</span></span></td>
<td><span data-ttu-id="810c8-159">Notiek</span><span class="sxs-lookup"><span data-stu-id="810c8-159">In progress</span></span></td>
<td><span data-ttu-id="810c8-160">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-160">Yes</span></span></td>
<td><span data-ttu-id="810c8-161">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-161">No</span></span></td>
<td><span data-ttu-id="810c8-162">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-162">Yes</span></span></td>
<td><span data-ttu-id="810c8-163">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-163">Yes</span></span></td>
<td><span data-ttu-id="810c8-164">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-164">No</span></span></td>
<td><span data-ttu-id="810c8-165">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810c8-166">Pārcelšana</span><span class="sxs-lookup"><span data-stu-id="810c8-166">Transfer</span></span></td>
<td><span data-ttu-id="810c8-167">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="810c8-167">Completed</span></span></td>
<td><span data-ttu-id="810c8-168">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-168">No</span></span></td>
<td><span data-ttu-id="810c8-169">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-169">No</span></span></td>
<td><span data-ttu-id="810c8-170">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-170">No</span></span></td>
<td><span data-ttu-id="810c8-171">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-171">No</span></span></td>
<td><span data-ttu-id="810c8-172">Jā</span><span class="sxs-lookup"><span data-stu-id="810c8-172">Yes</span></span></td>
<td><span data-ttu-id="810c8-173">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810c8-174">Pārsūtīšana vai apstrāde</span><span class="sxs-lookup"><span data-stu-id="810c8-174">Transfer or process</span></span></td>
<td><span data-ttu-id="810c8-175">Tukšs</span><span class="sxs-lookup"><span data-stu-id="810c8-175">Empty</span></span></td>
<td><span data-ttu-id="810c8-176">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-176">No</span></span></td>
<td><span data-ttu-id="810c8-177">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-177">No</span></span></td>
<td><span data-ttu-id="810c8-178">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-178">No</span></span></td>
<td><span data-ttu-id="810c8-179">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-179">No</span></span></td>
<td><span data-ttu-id="810c8-180">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-180">No</span></span></td>
<td><span data-ttu-id="810c8-181">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810c8-182">Pārsūtīšana vai apstrāde</span><span class="sxs-lookup"><span data-stu-id="810c8-182">Transfer or process</span></span></td>
<td><span data-ttu-id="810c8-183">Nav atrasta Kanban karte</span><span class="sxs-lookup"><span data-stu-id="810c8-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="810c8-184">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-184">No</span></span></td>
<td><span data-ttu-id="810c8-185">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-185">No</span></span></td>
<td><span data-ttu-id="810c8-186">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-186">No</span></span></td>
<td><span data-ttu-id="810c8-187">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-187">No</span></span></td>
<td><span data-ttu-id="810c8-188">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-188">No</span></span></td>
<td><span data-ttu-id="810c8-189">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810c8-190">Pārsūtīšana vai apstrāde</span><span class="sxs-lookup"><span data-stu-id="810c8-190">Transfer or process</span></span></td>
<td><span data-ttu-id="810c8-191">Ir atrasta Kanban karte, taču tā nav piešķirta Kanban</span><span class="sxs-lookup"><span data-stu-id="810c8-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="810c8-192">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-192">No</span></span></td>
<td><span data-ttu-id="810c8-193">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-193">No</span></span></td>
<td><span data-ttu-id="810c8-194">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-194">No</span></span></td>
<td><span data-ttu-id="810c8-195">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-195">No</span></span></td>
<td><span data-ttu-id="810c8-196">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-196">No</span></span></td>
<td><span data-ttu-id="810c8-197">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="810c8-198">Apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="810c8-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="810c8-199">Neplānots</span><span class="sxs-lookup"><span data-stu-id="810c8-199">Not planned</span></span></li>
<li><span data-ttu-id="810c8-200">Sagatavots</span><span class="sxs-lookup"><span data-stu-id="810c8-200">Prepared</span></span></li>
<li><span data-ttu-id="810c8-201">Notiek</span><span class="sxs-lookup"><span data-stu-id="810c8-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="810c8-202">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-202">No</span></span></td>
<td><span data-ttu-id="810c8-203">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-203">No</span></span></td>
<td><span data-ttu-id="810c8-204">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-204">No</span></span></td>
<td><span data-ttu-id="810c8-205">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-205">No</span></span></td>
<td><span data-ttu-id="810c8-206">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-206">No</span></span></td>
<td><span data-ttu-id="810c8-207">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="810c8-208">Apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="810c8-208">Process</span></span></td>
<td><span data-ttu-id="810c8-209">Pabeigts</span><span class="sxs-lookup"><span data-stu-id="810c8-209">Completed</span></span></td>
<td><span data-ttu-id="810c8-210">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-210">No</span></span></td>
<td><span data-ttu-id="810c8-211">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-211">No</span></span></td>
<td><span data-ttu-id="810c8-212">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-212">No</span></span></td>
<td><span data-ttu-id="810c8-213">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-213">No</span></span></td>
<td><span data-ttu-id="810c8-214">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-214">No</span></span></td>
<td><span data-ttu-id="810c8-215">Nē</span><span class="sxs-lookup"><span data-stu-id="810c8-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]