---
title: Reģistrējiet pabeigšanu, izmantojot darba kartes ierīci
description: Šajā tēmā ir aprakstīts, kā konfigurēt sistēmu, lai darba kartes ierīces lietotāji varētu ziņot par pabeigtajām precēm no ražošanas pasūtījuma uz krājumiem.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403266"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="75fcc-103">Reģistrējiet pabeigšanu, izmantojot darba kartes ierīci</span><span class="sxs-lookup"><span data-stu-id="75fcc-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75fcc-104">Darbinieki izmanto lapu **Pārskatu norises** darba kartes ierīcē, lai ziņotu par ražošanas darbam pabeigtajiem daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="75fcc-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="75fcc-105">Kontrolēt, vai krājumiem ir pievienoti pabeigtie daudzumi</span><span class="sxs-lookup"><span data-stu-id="75fcc-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="75fcc-106">Lai kontrolētu, vai un kā pēdējā operācijā fiziski pabeigtie daudzumi jāpievieno krājumiem, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="75fcc-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="75fcc-107">Dodieties uz **Preces kontrole \> Iestatīšana \> Ražošanas izpilde \> Ražošanas pasūtījuma noklusējuma vērtības**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="75fcc-108">Cilnē **Reģistrēt kā pabeigtu** iestatiet lauku **Atjaunināt pabeigto pārskatu tiešsaistē** uz vienu no tālāk minētajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="75fcc-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="75fcc-109">**Nē** — daudzums netiks pievienots krājumiem, kad daudzumi tiek reģistrēti pēdējā operācijā.</span><span class="sxs-lookup"><span data-stu-id="75fcc-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="75fcc-110">Ražošanas pasūtījuma statuss nekad nemainīsies.</span><span class="sxs-lookup"><span data-stu-id="75fcc-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="75fcc-111">**Statuss + daudzums** — ražošanas pasūtījuma statuss tiks mainīts uz *Reģistrēts kā pabeigts*, un daudzums tiks reģistrēts kā pabeigts noliktavā.</span><span class="sxs-lookup"><span data-stu-id="75fcc-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="75fcc-112">**Daudzums** — daudzums tiks reģistrēts kā pabeigts noliktavā, bet ražošanas pasūtījuma statuss nekad nemainīsies.</span><span class="sxs-lookup"><span data-stu-id="75fcc-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="75fcc-113">**Statuss** — mainīsies tika ražošanas pasūtījuma statuss.</span><span class="sxs-lookup"><span data-stu-id="75fcc-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="75fcc-114">Neviens daudzums netiks pievienots krājumiem, kad daudzumi tiek reģistrēti pēdējā operācijā.</span><span class="sxs-lookup"><span data-stu-id="75fcc-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="75fcc-115">Daudzumi netiek izsekoti krājumos, ja darbības, kuras ir reģistrētas kā pabeigtas, nav definētas kā pēdējā operācija.</span><span class="sxs-lookup"><span data-stu-id="75fcc-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="75fcc-116">Tomēr šos daudzumus var izmantot, lai skatītu norisi.</span><span class="sxs-lookup"><span data-stu-id="75fcc-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="75fcc-117">Tās var iekļaut arī kārtulās, kas kontrolē, vai darbinieki var sākt nākamo operāciju, pirms ir sasniegta noteiktā reģistrēto daudzumu robežvērtība iepriekšējā operācijā.</span><span class="sxs-lookup"><span data-stu-id="75fcc-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="75fcc-118">Varat definēt šīs kārtulas cilnē **Daudzuma pārbaude**, kas atrodas lapā **Ražošanas pasūtījuma noklusētās vērtības**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="75fcc-119">Papildinformāciju par to, kā strādāt ar lapu **Ražošanas pasūtījuma noklusētās vērtības**, skatiet [Ražošanas parametri ražošanas izpildē](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="75fcc-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="75fcc-120">Reģistrēt partijas kontrolētos elementus kā pabeigtus</span><span class="sxs-lookup"><span data-stu-id="75fcc-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="75fcc-121">Darba kartes ierīce atbalsta trīs scenārijus ziņošanai par partijas elementiem.</span><span class="sxs-lookup"><span data-stu-id="75fcc-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="75fcc-122">Šie scenāriji attiecas gan uz elementiem, kas ir iespējoti papildu noliktavas procesiem, gan uz elementiem, kas nav iespējoti papildu noliktavas procesiem.</span><span class="sxs-lookup"><span data-stu-id="75fcc-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="75fcc-123">**Manuāli piešķirtie partijas numuri:** darbinieki ievada pielāgotu partijas numuru.</span><span class="sxs-lookup"><span data-stu-id="75fcc-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="75fcc-124">Šis partijas numurs var būt no ārēja avota, kas sistēmai nav zināms.</span><span class="sxs-lookup"><span data-stu-id="75fcc-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="75fcc-125">**Iepriekš definētie partijas numuri:** darbinieki atlasa partijas numuru partiju numuru sarakstā, ko sistēma automātiski izveido pirms ražošanas pasūtījuma nodošanas darba kartes ierīcei.</span><span class="sxs-lookup"><span data-stu-id="75fcc-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="75fcc-126">**Fiksēti partijas numuri:** darbinieki neievada vai neatlasa partijas numuru.</span><span class="sxs-lookup"><span data-stu-id="75fcc-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="75fcc-127">Tā vietā sistēma automātiski piešķir ražošanas pasūtījumam partijas numuru, pirms tas tiek izlaists ražošanai.</span><span class="sxs-lookup"><span data-stu-id="75fcc-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="75fcc-128">Lai iespējotu katru scenāriju, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="75fcc-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="75fcc-129">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="75fcc-130">Atlasiet konfigurējamo preci.</span><span class="sxs-lookup"><span data-stu-id="75fcc-130">Select the product to configure.</span></span>
1. <span data-ttu-id="75fcc-131">Kopsavilkuma cilnes **Pārvaldīt krājumu** laukā **Partijas numuru grupa** atlasiet izsekošanas numuru grupu, kas iestatīta, lai atbalstītu jūsu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="75fcc-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="75fcc-132">Pēc noklusējuma, ja partijas kontrolētajai precei nav piešķirta partijas numuru grupa, darba kartes ierīce nodrošina manuālu partijas numura ievadi reģistrācijas kā pabeigts laikā.</span><span class="sxs-lookup"><span data-stu-id="75fcc-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="75fcc-133">Šajās apakšsadaļās aprakstīts, kā iestatīt izsekošanas numuru grupas, lai atbalstītu katru no trim scenārijiem pārskatam par partijas elementiem.</span><span class="sxs-lookup"><span data-stu-id="75fcc-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="75fcc-134">Partijas numura pārskata iespējošana darba kartes ierīcē</span><span class="sxs-lookup"><span data-stu-id="75fcc-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="75fcc-135">Lai iespējotu jūsu darbu karšu ierīces akceptēt partijas numuru, ziņojot par pabeigšanu, ir jāizmanto [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu tālāk norādītos līdzekļus (minētajā secībā).</span><span class="sxs-lookup"><span data-stu-id="75fcc-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="75fcc-136">Uzlabota lietotāja pieredze darba karšu ierīces norises pārskata dialogā</span><span class="sxs-lookup"><span data-stu-id="75fcc-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="75fcc-137">Iespējojiet, lai ievadītu partijas un sērijas numurus, vienlaikus ziņojot kā par pabeigtu no darba karšu ierīces (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="75fcc-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="75fcc-138">Iestatiet izsekošanas numuru grupu, kas ļauj darbiniekiem manuāli piešķirt partijas numuru</span><span class="sxs-lookup"><span data-stu-id="75fcc-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="75fcc-139">Lai ļautu manuāli piešķirt partijas numurus, izpildiet tālāk norādītās darbības izsekošanas numuru grupas iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="75fcc-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="75fcc-140">Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Dimensijas \> Izsekošanas numuru grupas**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="75fcc-141">Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.</span><span class="sxs-lookup"><span data-stu-id="75fcc-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="75fcc-142">Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Manuāli** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="75fcc-143">![Izsekošanas numuru grupu lapa](media/tracking-number-group-manual.png "Izsekošanas numuru grupu lapa")</span><span class="sxs-lookup"><span data-stu-id="75fcc-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="75fcc-144">Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā partijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.</span><span class="sxs-lookup"><span data-stu-id="75fcc-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="75fcc-145">Izmantojot šo scenāriju, lauks **Partijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, ir teksta lodziņš, kurā darbinieki var ievadīt jebkuru vērtību.</span><span class="sxs-lookup"><span data-stu-id="75fcc-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="75fcc-146">![Pārskata norises lapa ar lauku manuāliem partijas numuriem](media/job-card-device-batch-manual.png "Pārskata norises lapa ar lauku manuāliem partijas numuriem")</span><span class="sxs-lookup"><span data-stu-id="75fcc-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="75fcc-147">Iestatiet izsekošanas numuru grupu, kas nodrošina iepriekš definētu partijas numuru sarakstu</span><span class="sxs-lookup"><span data-stu-id="75fcc-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="75fcc-148">Lai nodrošinātu iepriekš definētu partijas numuru sarakstu, izpildiet tālāk norādītās darbības izsekošanas numuru grupas iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="75fcc-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="75fcc-149">Dodieties uz **Krājumu pārvaldība \> Iestatīšana > Dimensijas \> Izsekošanas numuru grupas**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="75fcc-150">Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.</span><span class="sxs-lookup"><span data-stu-id="75fcc-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="75fcc-151">Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Tikai krājumu transakcijām** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="75fcc-152">Lietojiet lauku **Daudzumam**, lai sadalītu partijas numurus pēc daudzuma, pamatojoties uz ievadīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="75fcc-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="75fcc-153">Piemēram, jums ir ražošanas pasūtījums desmit vienībām un lauks **Daudzumam** ir iestatīts uz *2*.</span><span class="sxs-lookup"><span data-stu-id="75fcc-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="75fcc-154">Šādā gadījumā, izveidojot ražošanas pasūtījumu, tam tiks piešķirti pieci partijas numuri.</span><span class="sxs-lookup"><span data-stu-id="75fcc-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="75fcc-155">![Izsekošanas numuru grupu lapa](media/tracking-number-group-predefined.png "Izsekošanas numuru grupu lapa")</span><span class="sxs-lookup"><span data-stu-id="75fcc-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="75fcc-156">Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā partijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.</span><span class="sxs-lookup"><span data-stu-id="75fcc-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="75fcc-157">Izmantojot šo scenāriju, lauks **Partijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, ir nolaižams saraksts, kurā darbiniekiem jāievada iepriekš definētā vērtība.</span><span class="sxs-lookup"><span data-stu-id="75fcc-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="75fcc-158">![Pārskata norises lapa ar iepriekš definēto partijas numuru sarakstu](media/job-card-device-batch-predefined.png "Pārskata norises lapa ar iepriekš definēto partijas numuru sarakstu")</span><span class="sxs-lookup"><span data-stu-id="75fcc-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="75fcc-159">Iestatiet izsekošanas numuru grupu, kas automātiski piešķir partijas numurus</span><span class="sxs-lookup"><span data-stu-id="75fcc-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="75fcc-160">Ja partijas numuri jāpiešķir automātiski — bez darbinieka ievades — veiciet tālāk minētās darbības, lai iestatītu izsekošanas numuru grupu.</span><span class="sxs-lookup"><span data-stu-id="75fcc-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="75fcc-161">Dodieties uz **Krājumu pārvaldība \> Iestatīšana \> Dimensijas \> Izsekošanas numuru grupas**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="75fcc-162">Izveidojiet vai atlasiet izsekošanas numuru grupu, kas jāiestata.</span><span class="sxs-lookup"><span data-stu-id="75fcc-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="75fcc-163">Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Tikai krājumu transakcijām** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="75fcc-164">Iestatiet opciju **Manuāli** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="75fcc-165">![Izsekošanas numuru grupu lapa](media/tracking-number-group-fixed.png "Izsekošanas numuru grupu lapa")</span><span class="sxs-lookup"><span data-stu-id="75fcc-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="75fcc-166">Iestatiet citas vērtības pēc vajadzības un pēc tam atlasiet šo izsekošanas numuru grupu kā partijas numuru grupu ražošanā laistām precēm, kurām vēlaties izmantot šo scenāriju.</span><span class="sxs-lookup"><span data-stu-id="75fcc-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="75fcc-167">Izmantojot šo scenāriju, lauks **Partijas numurs**, ko darba kartes ierīcē nodrošina lapa **Pārskata norise**, rāda vērtību, bet darbinieki nevar to rediģēt.</span><span class="sxs-lookup"><span data-stu-id="75fcc-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="75fcc-168">![Pārskata norises lapa ar fiksētu partijas numuru](media/job-card-device-batch-fixed.png "Pārskata norises lapa ar fiksētu partijas numuru")</span><span class="sxs-lookup"><span data-stu-id="75fcc-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="75fcc-169">Ziņojums par pabeigšanu noliktavas unikālajai vienībai</span><span class="sxs-lookup"><span data-stu-id="75fcc-169">Report as finished to a license plate</span></span>

<span data-ttu-id="75fcc-170">Papildu noliktavas procesi var izmantot noliktavas unikālās vienības dimensiju, lai izsekotu krājumus noliktavas vietās, kas ir iestatītas šim nolūkam.</span><span class="sxs-lookup"><span data-stu-id="75fcc-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="75fcc-171">Šādā gadījumā ir nepieciešams unikāls noliktavas vienības identifikators, kad darbinieks ziņo par pabeigtajiem daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="75fcc-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="75fcc-172">Noliktavas unikālās vienības ziņošanas un uzlīmes drukāšanas iespējošana</span><span class="sxs-lookup"><span data-stu-id="75fcc-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="75fcc-173">Lai izmantotu šajā sadaļā aprakstītos līdzekļus, jāizmanto [līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu tālāk norādītos līdzekļus (minētajā secībā).</span><span class="sxs-lookup"><span data-stu-id="75fcc-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="75fcc-174">Darbu kartes ierīcei ir pievienota noliktavas vienībai, lai ziņotu par pabeigšanu</span><span class="sxs-lookup"><span data-stu-id="75fcc-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="75fcc-175">Iespējojiet unikāla noliktavas vienības identifikatora automātisku ģenerēšanu, kad darba kartes ierīcē norādīts pabeigts statuss</span><span class="sxs-lookup"><span data-stu-id="75fcc-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="75fcc-176">Izdrukāt etiķeti no darba karšu ierīces</span><span class="sxs-lookup"><span data-stu-id="75fcc-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="75fcc-177">Iestatīt ziņošanu par pabeigšanu noliktavas unikālajai vienībai</span><span class="sxs-lookup"><span data-stu-id="75fcc-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="75fcc-178">Lai kontrolētu, vai darbiniekiem ir atkārtoti jāizmanto esoša noliktavas vienība vai jāģenerē jauna noliktavas vienība, kad tiek reģistrēta krājumu pabeigšana, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="75fcc-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="75fcc-179">Dodieties uz **Ražošanas kontrole \> Iestatīšana \> Ražošanas izpilde \> Konfigurēt darbu karti ierīcēm**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="75fcc-180">Iestatiet tālāk norādītās opcijas katrai ierīcei.</span><span class="sxs-lookup"><span data-stu-id="75fcc-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="75fcc-181">**Ģenerēt noliktavas vienību** — iestatiet šo opciju uz **Jā**, lai katram pārskatam ģenerētu jaunas noliktavas vienības pabeigšanu.</span><span class="sxs-lookup"><span data-stu-id="75fcc-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="75fcc-182">Iestatiet to uz **Nē**, ja katram pārskatam ir jāizmanto esoša noliktavas vienība kā pabeigta.</span><span class="sxs-lookup"><span data-stu-id="75fcc-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="75fcc-183">**Drukāt etiķeti** — iestatiet šo opciju uz **Jā**, ja darbiniekam ir jādrukā noliktavas vienības etiķete katram pārskatam kā pabeigta.</span><span class="sxs-lookup"><span data-stu-id="75fcc-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="75fcc-184">Iestatiet to uz **Nē**, ja etiķete nav nepieciešama.</span><span class="sxs-lookup"><span data-stu-id="75fcc-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="75fcc-185">![Konfigurēt darbu karti ierīču lapai](media/config-job-card-raf.png "Konfigurēt darbu karti ierīču lapai")</span><span class="sxs-lookup"><span data-stu-id="75fcc-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="75fcc-186">Lai konfigurētu etiķeti, dodieties uz **Noliktavas vadība \> Iestatīšana \> Dokumentu maršrutēšana \> Dokumentu maršrutēšana**.</span><span class="sxs-lookup"><span data-stu-id="75fcc-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="75fcc-187">Papildinformāciju skatiet [Iespējot noliktavas vienības etiķetes drukāšanu](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="75fcc-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
