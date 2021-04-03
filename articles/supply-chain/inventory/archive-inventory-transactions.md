---
title: Arhivēt krājumu transakcijas
description: Šajā tēmā ir aprakstīts, kā arhivēt krājumu darbību datus, lai palīdzētu uzlabot sistēmas veiktspēju.
author: sherry-zheng
manager: tfehr
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3a0fa65eb728e4ce96bdfc3f7a0f04901551ccea
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556431"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="4f221-103">Arhivēt krājumu transakcijas</span><span class="sxs-lookup"><span data-stu-id="4f221-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4f221-104">Laika gaitā krājumu darbību tabula (`InventTrans`) turpinās pieaugt un patērēt vairāk vietas datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="4f221-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="4f221-105">Tāpēc vaicājumi, kas ir veikti attiecībā pret tabulu, pakāpeniski kļūs lēnāki.</span><span class="sxs-lookup"><span data-stu-id="4f221-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="4f221-106">Šajā tēmā aprakstīts, kā var lietot krājumu *Darbību arhīva līdzekli*, lai arhivētu datus par krājumu darbībām, tādējādi uzlabojot sistēmas veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="4f221-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="4f221-107">Atlasītajā slēgtajā Virsgrāmatas periodā var arhivēt tikai finansiāli atjauninātas krājumu darbības.</span><span class="sxs-lookup"><span data-stu-id="4f221-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="4f221-108">Lai to arhivētu, finansiāli atjauninātajām izejošām krājumu darbībām jābūt ar izejas plūsmas statusu *Pārdots* un ienākošo krājumu darbībām jābūt ar statusu *Nopirkts*.</span><span class="sxs-lookup"><span data-stu-id="4f221-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="4f221-109">Arhivējot krājumu darbības, visas saistītās darbības tiek pārvietotas uz `InventTransArchive` tabulu.</span><span class="sxs-lookup"><span data-stu-id="4f221-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="4f221-110">Krājumu izdošanas darbības un krājumu saņemšanas darbības tiek arhivēta atsevišķi, pamatojoties uz krājuma ID (`itemId`) un krājumu dimensijas ID (`inventDimId`) kombināciju, un tās tiek novietotas apkopotās izejas plūsmas un summētās saņemšanas darbībās.</span><span class="sxs-lookup"><span data-stu-id="4f221-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="4f221-111">Ja vienā `itemId` un `inventDimId` kombinācijā ir tikai viena saņemšanas vai izdošanas darbība, darbība netiks arhivēta.</span><span class="sxs-lookup"><span data-stu-id="4f221-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="4f221-112">Līdzekļa ieslēgšana sistēmā</span><span class="sxs-lookup"><span data-stu-id="4f221-112">Turn on the feature in your system</span></span>

<span data-ttu-id="4f221-113">Ja sistēmā vēl nav ietverti šajā tēmā aprakstītie līdzekļi, pārejiet uz sadaļu [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un iespējojiet līdzekli *Krājumu darbību arhīvs*.</span><span class="sxs-lookup"><span data-stu-id="4f221-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="4f221-114">Lietas, kas jāņem vērā pirms krājumu darbību arhivēšanas</span><span class="sxs-lookup"><span data-stu-id="4f221-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="4f221-115">Pirms krājumu darbību arhivēšanas ir jāapsver šādi biznesa scenāriji, jo tos ietekmēs darbība:</span><span class="sxs-lookup"><span data-stu-id="4f221-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="4f221-116">Kad jūs auditējat krājumu darbības no saistītiem dokumentiem, piemēram, pirkšanas pasūtījuma rindām, tās tiks parādītas kā arhivētas.</span><span class="sxs-lookup"><span data-stu-id="4f221-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="4f221-117">Lai pārskatītu arhivētās darbības, dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Tīrīt \> Krājumu darbību arhīvs**.</span><span class="sxs-lookup"><span data-stu-id="4f221-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="4f221-118">Arhivētajiem periodiem nevar atcelt krājumu slēgšanu.</span><span class="sxs-lookup"><span data-stu-id="4f221-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="4f221-119">Pirms varat atcelt krājumu slēgšanu, ir jāatgriež krājumu darbību arhīvs derīgs periodam.</span><span class="sxs-lookup"><span data-stu-id="4f221-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="4f221-120">Standarta izmaksu pārveidošanu nevar veikt arhivētiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="4f221-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="4f221-121">Pirms varat atcelt krājumu slēgšanu, ir jāatgriež krājumu darbību arhīvs derīgs periodam.</span><span class="sxs-lookup"><span data-stu-id="4f221-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="4f221-122">Krājumu pārskati, kas ir nākuši no krājumu darbībām, tiks ietekmēti, kad arhivēsiet krājumu darbības.</span><span class="sxs-lookup"><span data-stu-id="4f221-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="4f221-123">Šie pārskati ietver krājumu vecumstruktūras pārskatu un krājumu vērtību pārskatus.</span><span class="sxs-lookup"><span data-stu-id="4f221-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="4f221-124">Krājumu prognozes var tikt ietekmētas, ja tās tiek palaistas arhivēto periodu laika periodā.</span><span class="sxs-lookup"><span data-stu-id="4f221-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4f221-125">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="4f221-125">Prerequisites</span></span>

<span data-ttu-id="4f221-126">Krājumu darbības var arhivēt tikai to periodu laikā, kuros ir ievēroti šādi nosacījumi:</span><span class="sxs-lookup"><span data-stu-id="4f221-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="4f221-127">Virsgrāmatas periodam jābūt slēgtam.</span><span class="sxs-lookup"><span data-stu-id="4f221-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="4f221-128">Krājumu slēgšana jāveic arhīva perioda datumā vai pēc tā.</span><span class="sxs-lookup"><span data-stu-id="4f221-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="4f221-129">Periodam jābūt vismaz vienu gadu pirms arhīva perioda sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="4f221-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="4f221-130">Nedrīkst būt eksistējošu krājumu pārrēķini.</span><span class="sxs-lookup"><span data-stu-id="4f221-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="4f221-131">Arhivēt krājumu transakcijas</span><span class="sxs-lookup"><span data-stu-id="4f221-131">Archive inventory transactions</span></span>

<span data-ttu-id="4f221-132">Lai arhivētu krājumu darbības, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="4f221-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="4f221-133">Dodieties uz **Krājumu pārvaldība** \> **Periodiskie uzdevumi** \> **Tīrīt** \> **Krājumu darbību arhīvs**.</span><span class="sxs-lookup"><span data-stu-id="4f221-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="4f221-134">Parādās lapa **Krājumu darbību arhīvs**, kurā parādīts arhivēto procesu ierakstu saraksts.</span><span class="sxs-lookup"><span data-stu-id="4f221-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="4f221-135">![Krājumu transakcijas arhīva lapa](media/archive-inventory-empty.png "Krājumu darbību arhīva lapa")</span><span class="sxs-lookup"><span data-stu-id="4f221-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="4f221-136">Darbību rūtī atlasiet **Krājumu darbību arhīvs**, lai izveidotu krājumu darbību arhīvu.</span><span class="sxs-lookup"><span data-stu-id="4f221-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="4f221-137">Kopsavilkuma cilnes **Parametri** dialoglodziņā **Krājumu darbību arhīvs** iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="4f221-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="4f221-138">**No datuma slēgtajā Virsgrāmatas periodā** – atlasiet agrāko darbības datumu, ko iekļaut arhīvā.</span><span class="sxs-lookup"><span data-stu-id="4f221-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="4f221-139">**Līdz datuma slēgtajā Virsgrāmatas periodā** – atlasiet jaunākās darbības datumu, ko iekļaut arhīvā.</span><span class="sxs-lookup"><span data-stu-id="4f221-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="4f221-140">![Krājumu transakcijas arhīva dialoglodziņš](media/archive-inventory-dates.png "Krājumu darbību arhīva dialoglodziņš")</span><span class="sxs-lookup"><span data-stu-id="4f221-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="4f221-141">Atlasei būs pieejami tikai [priekšnosacījumiem](#prerequisites) atbilstošie periodi.</span><span class="sxs-lookup"><span data-stu-id="4f221-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="4f221-142">Kopsavilkuma cilnē **Izpildīt fonā** iestatiet pakešapstrādes detaļas pēc pieprasījuma.</span><span class="sxs-lookup"><span data-stu-id="4f221-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="4f221-143">Veiciet pakešuzdevumu darbības programmā Microsoft Dynamics 365 Supply Chain Management, kā parasti.</span><span class="sxs-lookup"><span data-stu-id="4f221-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="4f221-144">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4f221-144">Select **OK**.</span></span>
1. <span data-ttu-id="4f221-145">Jūs saņemat ziņojumu, kurā tiek parādīta uzvedne ar aicinājumu apstiprināt, ka vēlaties turpināt.</span><span class="sxs-lookup"><span data-stu-id="4f221-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="4f221-146">Uzmanīgi izlasiet ziņojumu un pēc tam atlasiet **Jā**, ja vēlaties turpināt.</span><span class="sxs-lookup"><span data-stu-id="4f221-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="4f221-147">Tiek saņemts ziņojums, ka krājumu darbību arhīva darbs ir pievienots pakešuzdevumu rindai.</span><span class="sxs-lookup"><span data-stu-id="4f221-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="4f221-148">Uzdevums sāks arhivēt krājumu darbības no atlasītā perioda.</span><span class="sxs-lookup"><span data-stu-id="4f221-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="4f221-149">Skatīt arhivētās krājumu transakcijas</span><span class="sxs-lookup"><span data-stu-id="4f221-149">View archived inventory transactions</span></span>

<span data-ttu-id="4f221-150">Lapa **Krājumu darbību arhīvs** rāda visu arhivēšanas vēsturi.</span><span class="sxs-lookup"><span data-stu-id="4f221-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="4f221-151">Katra režģa rinda rāda tādu informāciju kā arhīva izveidošanas datumu, lietotāju, kas to izveidoja, un tā statusu.</span><span class="sxs-lookup"><span data-stu-id="4f221-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="4f221-152">![Vēstures arhivēšana Krājumu darbību arhīva lapā](media/archive-inventory-full.png "Vēstures arhivēšana Krājumu darbību arhīva lapā")</span><span class="sxs-lookup"><span data-stu-id="4f221-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="4f221-153">Nolaižamajā sarakstā lapas augšpusē atlasiet vienu no šīm vērtībām, lai filtrētu režģī parādītos arhīvus:</span><span class="sxs-lookup"><span data-stu-id="4f221-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="4f221-154">**Aktīvs** – rādīt tikai aktīvos arhīvus, neatgrieztos arhīvus.</span><span class="sxs-lookup"><span data-stu-id="4f221-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="4f221-155">**Visi** – parāda visus arhīvus: gan aktīvos, gan apgrieztos.</span><span class="sxs-lookup"><span data-stu-id="4f221-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="4f221-156">Katram arhīvam režģī tiek sniegta šāda informācija:</span><span class="sxs-lookup"><span data-stu-id="4f221-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="4f221-157">**Aktīvs** – atzīme norāda, ka arhīvs ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="4f221-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="4f221-158">**No datuma** – senākās darbības datums, kuru var iekļaut arhīvā.</span><span class="sxs-lookup"><span data-stu-id="4f221-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="4f221-159">**No datuma** – jaunākās darbības datums, kuru var iekļaut arhīvā.</span><span class="sxs-lookup"><span data-stu-id="4f221-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="4f221-160">**Plānots pēc** – lietotāja konts, kas izveidoja arhīvu.</span><span class="sxs-lookup"><span data-stu-id="4f221-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="4f221-161">**Izpildīts** – arhīva izveidošanas datums.</span><span class="sxs-lookup"><span data-stu-id="4f221-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="4f221-162">**Reverss** – atzīme norāda, ka arhīvs ir anulēts.</span><span class="sxs-lookup"><span data-stu-id="4f221-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="4f221-163">**Pārtraukt pašreizējo atjaunināšanu** – atzīme norāda, ka arhīvs notiek, bet tas ir apturēts.</span><span class="sxs-lookup"><span data-stu-id="4f221-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="4f221-164">**Stāvoklis** – arhīva apstrādes statuss.</span><span class="sxs-lookup"><span data-stu-id="4f221-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="4f221-165">Iespējamās vērtības ir *Gaida*, *Notiek* un *Pabeigts*.</span><span class="sxs-lookup"><span data-stu-id="4f221-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="4f221-166">Rīkjosla virs režģa nodrošina šādas pogas, kuras var izmantot darbam ar atlasīto arhīvu:</span><span class="sxs-lookup"><span data-stu-id="4f221-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="4f221-167">**Arhivētās darbības** – apskatiet visas izvēlētā arhīva detaļas.</span><span class="sxs-lookup"><span data-stu-id="4f221-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="4f221-168">**Arhivēto darbību** lapa, kurā parādītas visas arhīva darbības.</span><span class="sxs-lookup"><span data-stu-id="4f221-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="4f221-169">![Arhivēto darbību lapa](media/archive-inventory-transactions.png "Arhivēto darbību lapa")</span><span class="sxs-lookup"><span data-stu-id="4f221-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="4f221-170">Lai skatītu papildinformāciju par noteiktu darbību lapā **Arhivētās darbības**, atlasiet to režģī un pēc tam darbību rūtī atlasiet **Arhivētās darbības detaļas**.</span><span class="sxs-lookup"><span data-stu-id="4f221-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="4f221-171">Lapa **Arhivēto darbību detaļas**, kas parādās, parāda tādu informāciju kā grāmatošana Virsgrāmatā, saistītās apakšgrāmatas atsauces un finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="4f221-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="4f221-172">**Apturēt arhivēšanu** - apturēt atlasīto arhīvu, kas pašlaik tiek apstrādāts.</span><span class="sxs-lookup"><span data-stu-id="4f221-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="4f221-173">Pauze stājas spēkā tikai pēc tam, kad ir izveidots arhivēšanas uzdevums.</span><span class="sxs-lookup"><span data-stu-id="4f221-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="4f221-174">Tāpēc var būt neliela aizkave, pirms pauze stājas spēkā.</span><span class="sxs-lookup"><span data-stu-id="4f221-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="4f221-175">Ja arhīvs ir apturēts, laukā **Pārtraukt pašreizējo atjaunināšanu** tiek parādīta atzīme.</span><span class="sxs-lookup"><span data-stu-id="4f221-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="4f221-176">**Atsākt arhivēšanu** - atsākt atlasītā arhīva apstrādi, kas pašlaik ir apturēts.</span><span class="sxs-lookup"><span data-stu-id="4f221-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="4f221-177">**Atsaukt** – anulēt atlasīto arhīvu.</span><span class="sxs-lookup"><span data-stu-id="4f221-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="4f221-178">Arhīvu var atsaukt tikai tad, ja tā lauks **Stāvoklis** ir iestatīts uz *Pabeigts*.</span><span class="sxs-lookup"><span data-stu-id="4f221-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="4f221-179">Ja arhīvs ir apturēts, laukā **Pārtraukt pašreizējo atjaunināšanu** tiek parādīta atzīme.</span><span class="sxs-lookup"><span data-stu-id="4f221-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
