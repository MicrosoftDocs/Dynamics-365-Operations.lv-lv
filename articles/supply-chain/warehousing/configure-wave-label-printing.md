---
title: Iestatīt un lietot kopuma etiķešu drukāšanu
description: Šajā tēmā ir aprakstīta kopuma etiķešu drukāšana un paskaidrots, kā to iestatīt.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 6314fd25d8d8a0013984d484f57a832c26f82b5a
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/27/2020
ms.locfileid: "4433219"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="efcbd-103">Iestatīt un lietot kopuma etiķešu drukāšanu</span><span class="sxs-lookup"><span data-stu-id="efcbd-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efcbd-104">Kopuma etiķešu drukāšana piedāvā alternatīvu pieeju etiķešu drukāšanai, ieviešot jaunu kopuma darbības metodi, kas ļauj izveidot un drukāt etiķetes tieši no kopuma veidnes, kopuma izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="efcbd-105">Tāpēc etiķetes jau būs pieejamas, pirms darbinieki palaidīs darba pasūtījumu mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="efcbd-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="efcbd-106">Pēc tam darbinieki var pievienot nepieciešamās etiķetes izdošanas laikā, nevis pēc izdošanas.</span><span class="sxs-lookup"><span data-stu-id="efcbd-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="efcbd-107">Kopuma etiķešu drukāšana izmanto Zebra programmēšanas valodu (ZPL), lai izveidotu etiķešu izkārtojumus.</span><span class="sxs-lookup"><span data-stu-id="efcbd-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="efcbd-108">Etiķetes izkārtojums ir sadalīts trīs sadaļās (galvene, pamatteksts un kājene), lai atļautu etiķetes ar atkārtotu struktūru.</span><span class="sxs-lookup"><span data-stu-id="efcbd-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="efcbd-109">Kopuma etiķešu veidnes paziņo sistēmai, kuras etiķetes izkārtojums ir jāizmanto.</span><span class="sxs-lookup"><span data-stu-id="efcbd-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="efcbd-110">Lietotāji var norādīt, kurš printeris tiek lietots.</span><span class="sxs-lookup"><span data-stu-id="efcbd-110">Users can specify which printer is used.</span></span> <span data-ttu-id="efcbd-111">Pēc nepieciešamības etiķetes ir iespējams drukāt vairākos printeros vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="efcbd-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="efcbd-112">Lapa **Kopuma etiķešu vēsture** parāda ierakstus par visām etiķetēm, kas ir izveidotas, izmantojot šo iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="efcbd-113">Etiķetes var drukāt un salīdzināt, pamatojoties uz darba galvenēm, varat drukāt pārtraukuma etiķetes darba galvenei, kā arī varat drukāt konteinera satura etiķetes, gadījumu etiķetes un citas līdzīgas etiķetes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="efcbd-114">Šī funkcionalitāte neaizstāj esošo etiķešu drukāšanas funkcionalitāti, kas ir balstīta uz dokumentu maršrutēšanu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="efcbd-115">Kopuma etiķešu drukāšana piedāvā šādus uzlabojumus:</span><span class="sxs-lookup"><span data-stu-id="efcbd-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="efcbd-116">Etiķešu drukāšana atbilstoši kastu skaitam vienā darba līnijā, neizmantojot konteinerizēšanu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="efcbd-117">(A “kaste” ir vienība, kas norādīta vienību secību grupas rindās.)</span><span class="sxs-lookup"><span data-stu-id="efcbd-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="efcbd-118">Vairāku dažādu etiķešu secību drukāšana (piemēram, kastu un palešu etiķetes).</span><span class="sxs-lookup"><span data-stu-id="efcbd-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="efcbd-119">Iekļaut etiķetes uzskaitījumu (piemēram, 1/124, 2/124,... 124/124) un definēt uzskaitījuma diapazonu (piemēram, darba rinda, kravas rinda vai nosūtīšana).</span><span class="sxs-lookup"><span data-stu-id="efcbd-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="efcbd-120">Izveidot un drukāt preču transporta pavadzīmes ID etiķetēs, pirms preču transporta pavadzīme tiek ģenerēta.</span><span class="sxs-lookup"><span data-stu-id="efcbd-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="efcbd-121">Katrai kastei izveidot unikālu seriālo pārvadāšanas konteinera kodu (SSCC) un iekļaut to katrā etiķetē.</span><span class="sxs-lookup"><span data-stu-id="efcbd-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="efcbd-122">Izveidot GS1 atbilstošas numuru sērijas preču transporta pavadzīmju ID un SSCC.</span><span class="sxs-lookup"><span data-stu-id="efcbd-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="efcbd-123">Atkārtoti drukājiet etiķetes no mobilajām ierīcēm un bagātinātā klienta.</span><span class="sxs-lookup"><span data-stu-id="efcbd-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="efcbd-124">Etiķešu anulēšana (piemēram, īsajos izdošanas scenārijos) un atkārtota drukāšana.</span><span class="sxs-lookup"><span data-stu-id="efcbd-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="efcbd-125">Notīriet kopuma etiķešu vēsturi.</span><span class="sxs-lookup"><span data-stu-id="efcbd-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="efcbd-126">Dokumenta maršrutēšanas izkārtojumu uzlabojumi tiek koplietoti starp dokumentu maršrutēšanas izkārtojumiem un kopuma etiķešu izkārtojumiem.</span><span class="sxs-lookup"><span data-stu-id="efcbd-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="efcbd-127">(Papildinformāciju skatiet sadaļā [Dokumenta maršrutēšanas izkārtojums numura zīmēm](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="efcbd-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="efcbd-128">Šie uzlabojumi padara efektīvāku etiķešu pievienošanu kastēm pirms paletizācijas.</span><span class="sxs-lookup"><span data-stu-id="efcbd-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="efcbd-129">Tas jo īpaši atvieglo uzņēmumus, kas nosūta sūtījumus lieliem mazumtirgotājiem, kuri, skenējot katru kasti atsevišķi, automātiski apstiprina pasūtījuma kvītis.</span><span class="sxs-lookup"><span data-stu-id="efcbd-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="efcbd-130">Varat ieviest šajā tēmā aprakstītos konfigurāciju scenārijus vai nu atsevišķi, vai kombinācijā, atkarībā no jūsu uzņēmuma prasībām.</span><span class="sxs-lookup"><span data-stu-id="efcbd-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="efcbd-131">Varat izveidot vairākas kopuma etiķešu veidnes, kas darbojas secībā (kā parādīts 3. scenārijā).</span><span class="sxs-lookup"><span data-stu-id="efcbd-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="efcbd-132">Piemēram, varat izmantot 1. scenāriju, lai izdrukātu kastu etiķetes un 2. scenāriju, lai izdrukātu palešu etiķetes (ja paletes krājumā atšķiras pēc lieluma un salikuma).</span><span class="sxs-lookup"><span data-stu-id="efcbd-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="efcbd-133">Ieslēgt līdzekli Kopuma etiķešu drukāšana</span><span class="sxs-lookup"><span data-stu-id="efcbd-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="efcbd-134">Lai varētu izmantot līdzekli *Kopuma etiķešu drukāšana*, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="efcbd-135">Administratori var izmantot [Līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbvietu, lai pārbaudītu līdzekļa statusu un vajadzības gadījumā to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="efcbd-136">Tur šī iespēja ir uzskaitīta tālāk minētajā veidā:</span><span class="sxs-lookup"><span data-stu-id="efcbd-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="efcbd-137">**Modulis:** *Noliktavas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="efcbd-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="efcbd-138">**Līdzekļa nosaukums:** *Kopuma etiķešu drukāšana*</span><span class="sxs-lookup"><span data-stu-id="efcbd-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="efcbd-139">1. scenārijs: kopuma etiķešu drukāšana, ģenerējot viena kopuma etiķetes</span><span class="sxs-lookup"><span data-stu-id="efcbd-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="efcbd-140">Šajā scenārijā ir parādīts, kā uzņēmums var drukāt nosūtīšanas etiķetes lieliem mazumtirgotājiem, kuri, skenējot katru kasti atsevišķi, automātiski apstiprina pasūtījuma kvītis.</span><span class="sxs-lookup"><span data-stu-id="efcbd-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="efcbd-141">Šajā scenārijā tiek parādīti visi plūsmas posmi.</span><span class="sxs-lookup"><span data-stu-id="efcbd-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="efcbd-142">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="efcbd-142">Make demo data available</span></span>

<span data-ttu-id="efcbd-143">Lai sekotu šim scenārijam, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="efcbd-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="efcbd-144">Pārliecinieties, vai kopuma etiķešu metode ir pieejama</span><span class="sxs-lookup"><span data-stu-id="efcbd-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="efcbd-145">Lai padarītu pieejamu kopuma etiķešu drukāšanas metodi, var būt nepieciešams atkārtoti ģenerēt kopuma procesa metodes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="efcbd-146">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="efcbd-147">Apstipriniet, ka **waveLabelPrinting** ir sarakstā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="efcbd-148">Ja tā nav, darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**, lai to pievienotu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="efcbd-149">Konfigurēt kopuma veidni</span><span class="sxs-lookup"><span data-stu-id="efcbd-149">Configure a wave template</span></span>

<span data-ttu-id="efcbd-150">Kopuma veidnes ļauj saistīt noteiktas kopuma metodes ar atbilstošo kopuma etiķešu veidni.</span><span class="sxs-lookup"><span data-stu-id="efcbd-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="efcbd-151">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="efcbd-152">Atlasiet veidni, kā **62 Sūtījums pēc noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="efcbd-153">Kopsavilkuma cilnē **Metodes** pārvietojiet metodi **Kopuma etiķešu drukāšana** uz kolonnu **Atlasītās metodes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="efcbd-154">Kolonnā **Atlasītās metodes** atlasiet metodi **Kopuma etiķešu drukāšana** un iestatiet tās lauku **Kopuma darbības kods** uz *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="efcbd-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="efcbd-155">Papildinformāciju par kopuma darbību kodiem skatiet sadaļā [Kopuma darbību kodi](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="efcbd-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="efcbd-156">Izveidot kopuma etiķešu izkārtojumu</span><span class="sxs-lookup"><span data-stu-id="efcbd-156">Create a wave label layout</span></span>

<span data-ttu-id="efcbd-157">Etiķešu izkārtojums kontrolē, kāda informācija tiek drukāta uz etiķetes un kā tā ir izkārtota. Šeit ievadiet ZPL kodu, kas tiek nosūtīts uz printeri.</span><span class="sxs-lookup"><span data-stu-id="efcbd-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="efcbd-158">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="efcbd-159">Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-160">**Etiķetes izkārtojuma ID:** *Carton*</span><span class="sxs-lookup"><span data-stu-id="efcbd-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="efcbd-161">**Apraksts:** *kaste (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="efcbd-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="efcbd-162">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="efcbd-163">Darbību rūtī atlasiet **Kopuma etiķešu rindas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="efcbd-164">Tiek parādīta lapa **Kopuma etiķešu rindas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="efcbd-165">Šeit varat konfigurēt etiķetes dinamisko daļu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="efcbd-166">Pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-167">**Rindas ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="efcbd-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="efcbd-168">**Rindas tabulas nosaukums:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="efcbd-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="efcbd-169">**Rindas sākuma pozīcija:** *0*</span><span class="sxs-lookup"><span data-stu-id="efcbd-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="efcbd-170">Šis lauks definē vertikālo pozīciju, kur rinda sāksies etiķetē.</span><span class="sxs-lookup"><span data-stu-id="efcbd-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="efcbd-171">**Rindas augstums:** *0*</span><span class="sxs-lookup"><span data-stu-id="efcbd-171">**Row height:** *0*</span></span>

        <span data-ttu-id="efcbd-172">Šis lauks definē katras rindas augstumu (punktos) atbilstoši ZPL standartam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="efcbd-173">Rindas augstums ir pozitīvs horizontālajām etiķetēm un negatīvs vertikālajām etiķetēm.</span><span class="sxs-lookup"><span data-stu-id="efcbd-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="efcbd-174">Tā kā šajā piemērā ir tikai viena rinda, varat iestatīt vērtību *0* (nulle).</span><span class="sxs-lookup"><span data-stu-id="efcbd-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="efcbd-175">**Rindu skaits lapā:** *1*</span><span class="sxs-lookup"><span data-stu-id="efcbd-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="efcbd-176">Šis lauks definē rindu skaitu, ko var drukāt uz katras etiķetes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="efcbd-177">Šis iestatījums radīs atsevišķu ZPL etiķeti, ko drukāt katram ierakstam kopuma etiķešu tabulā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="efcbd-178">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-178">Close the page.</span></span>
1. <span data-ttu-id="efcbd-179">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="efcbd-180">Vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-181">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-182">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-183">**Lauks:** *Darba veids*</span><span class="sxs-lookup"><span data-stu-id="efcbd-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="efcbd-184">**Kritēriji:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="efcbd-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="efcbd-185">Šis vaicājums nodrošina, ka etiķetē tiks drukātas tikai izdošanas veida darba rindas, nevis izvietošanas veida darba rindas.</span><span class="sxs-lookup"><span data-stu-id="efcbd-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="efcbd-186">Ja vēlaties varēt drukāt preču transporta pavadzīmes ID, cilnē **Savienojumi** atlasiet tabulu **Darba rindas** un pievienojiet tai tabulu **Sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="efcbd-187">Aizveriet vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="efcbd-188">Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="efcbd-189">Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="efcbd-190">Piemēram, ja lietojat Zebra printerus, varat izmantot šādu kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="efcbd-191">Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes pamatteksts**, ievadiet vajadzīgā pamatteksta ZPL kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="efcbd-192">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="efcbd-193">Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes kājene**, ievadiet vajadzīgās kājenes ZPL kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="efcbd-194">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="efcbd-195">Šajā iestatījumā tiks drukāts viens katras etiķetes eksemplārs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="efcbd-196">Ja ir nepieciešamas vairākas kopijas (piemēram, viena kopija katrai paletes pusei), iestatiet **n** vērtību sekcijai **\^PQn** kājenē līdz nepieciešamajam kopiju skaitam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="efcbd-197">Piemēram, lai izdrukātu katras etiķetes četras kopijas, norādiet **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="efcbd-198">Tagad etiķete ir gatava lietošanai.</span><span class="sxs-lookup"><span data-stu-id="efcbd-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="efcbd-199">Izveidot kopuma etiķešu veidu</span><span class="sxs-lookup"><span data-stu-id="efcbd-199">Create a wave label type</span></span>

<span data-ttu-id="efcbd-200">Kopuma etiķešu veidi tiek izmantoti, lai saistītu kopuma etiķešu veidnes vienībai ar vienības secību grupas rindām.</span><span class="sxs-lookup"><span data-stu-id="efcbd-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="efcbd-201">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="efcbd-202">Pievienojiet kopuma etiķešu veidu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-203">**Etiķetes veids:** *Carton*</span><span class="sxs-lookup"><span data-stu-id="efcbd-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="efcbd-204">**Apraksts:** *kaste*</span><span class="sxs-lookup"><span data-stu-id="efcbd-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="efcbd-205">Iestatīt vienību secību grupas</span><span class="sxs-lookup"><span data-stu-id="efcbd-205">Set up unit sequence groups</span></span>

<span data-ttu-id="efcbd-206">Pēc tam iestatiet vienības secību grupu kopuma etiķetes veidam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="efcbd-207">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Vienību secību grupas**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="efcbd-208">Atlasiet grupu **Ea Box PL**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="efcbd-209">Rindā **Kaste** iestatiet lauku **Kopuma līmeņa veids** uz *Kartons*.</span><span class="sxs-lookup"><span data-stu-id="efcbd-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="efcbd-210">Izveidot kopuma etiķešu veidni</span><span class="sxs-lookup"><span data-stu-id="efcbd-210">Create a wave label template</span></span>

<span data-ttu-id="efcbd-211">Pēc tam izveidojiet kopuma etiķešu veidni kopuma etiķetes veidam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="efcbd-212">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidnes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="efcbd-213">Pievienojiet kopuma līmeņa veidni un galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="efcbd-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="efcbd-214">**Etiķetes veidnes nosaukums:** *Carton labels*</span><span class="sxs-lookup"><span data-stu-id="efcbd-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="efcbd-215">**Apraksts:** *Kastes etiķetes*</span><span class="sxs-lookup"><span data-stu-id="efcbd-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="efcbd-216">**Kopuma darbības kods:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="efcbd-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="efcbd-217">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="efcbd-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="efcbd-218">Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **Kopuma etiķešu veids** uz *Kaste*.</span><span class="sxs-lookup"><span data-stu-id="efcbd-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="efcbd-219">Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** pievienojiet jaunu rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-220">**Etiķetes izkārtojuma ID:** *Carton*</span><span class="sxs-lookup"><span data-stu-id="efcbd-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="efcbd-221">**Printera nosaukums:** atlasiet atbilstošu ZPL printeri.</span><span class="sxs-lookup"><span data-stu-id="efcbd-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="efcbd-222">**Izpildīt vaicājumu:** *Jā* (Šis iestatījums nav obligāts, bet tas ir ieteicams optimālai veiktspējai.)</span><span class="sxs-lookup"><span data-stu-id="efcbd-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="efcbd-223">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="efcbd-224">Neobligāti: ja iestatāt debitoram raksturīgu etiķešu noformējumu, ir jāizveido vaicājums, lai atrastu debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="efcbd-225">Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="efcbd-226">Pēc tam, vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-227">**Tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="efcbd-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="efcbd-228">**Atvasinātā tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="efcbd-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="efcbd-229">**Lauks:** *Konta numurs*</span><span class="sxs-lookup"><span data-stu-id="efcbd-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="efcbd-230">**Kritēriji:** ievadiet atbilstošo debitora konta numuru.</span><span class="sxs-lookup"><span data-stu-id="efcbd-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="efcbd-231">Kad esat pabeidzis, atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="efcbd-232">Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktora dialoglodziņu visai etiķešu veidnei.</span><span class="sxs-lookup"><span data-stu-id="efcbd-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="efcbd-233">Vaicājumu redaktora dialoglodziņā, cilnē **Kārtošana** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-234">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-235">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-236">**Lauks:** *Atsauces kravas rindas ID (Ieraksta ID)*</span><span class="sxs-lookup"><span data-stu-id="efcbd-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="efcbd-237">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="efcbd-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="efcbd-238">Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="efcbd-239">Ziņojuma lodziņš aicina apstiprināt grupēšanas atiestatīšanas darbību.</span><span class="sxs-lookup"><span data-stu-id="efcbd-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="efcbd-240">Lai turpinātu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="efcbd-241">Darbību rūtī atlasiet **Kopuma etiķešu veidņu grupēšana**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="efcbd-242">Dialoglodziņā **Kopuma etiķešu veidņu grupēšana** atlasiet rindu, kurā lauks **Atsauces lauka nosaukums** ir iestatīts uz *Atsauces kravas rindas ID*, un pēc tam atzīmējiet izvēles rūtiņu **Etiķešu kompilācijas ID** šai rindai.</span><span class="sxs-lookup"><span data-stu-id="efcbd-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="efcbd-243">Šis iestatījums izveidos vienu etiķetes secību (“carton 1 X”) kravas rindai visā kopumā, neņemot vērā darba grupēšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="efcbd-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="efcbd-244">Šo etiķešu secību var drukāt uz etiķešu izkārtojuma.</span><span class="sxs-lookup"><span data-stu-id="efcbd-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="efcbd-245">Konfigurēt numuru sērijas paplašinājumus</span><span class="sxs-lookup"><span data-stu-id="efcbd-245">Configure number sequence extensions</span></span>

<span data-ttu-id="efcbd-246">Numuru sērijas paplašinājumi kontrolē GS1 atbilstību noteiktām numuru sērijām.</span><span class="sxs-lookup"><span data-stu-id="efcbd-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="efcbd-247">Šī konfigurācija nav obligāta pašreizējam scenārijam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="efcbd-248">Papildinformāciju un konfigurācijas norādījumus skatiet sadaļā [Konfigurēt numuru sērijas paplašinājumus](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="efcbd-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="efcbd-249">Izveidot pārdošanas pasūtījumu un nodot to noliktavai</span><span class="sxs-lookup"><span data-stu-id="efcbd-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="efcbd-250">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījums \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="efcbd-251">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-252">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="efcbd-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="efcbd-253">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="efcbd-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="efcbd-254">Pievienojiet divus pārdošanas pasūtījumus, kam ir šādi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="efcbd-255">1. pārdošanas pasūtījuma rinda:</span><span class="sxs-lookup"><span data-stu-id="efcbd-255">Sales order line 1:</span></span>

        - <span data-ttu-id="efcbd-256">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="efcbd-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="efcbd-257">**Daudzums:** *9024*</span><span class="sxs-lookup"><span data-stu-id="efcbd-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="efcbd-258">**Vienība:** *katra* (9024 ea = 376 Box = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="efcbd-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="efcbd-259">2. pārdošanas pasūtījuma rinda:</span><span class="sxs-lookup"><span data-stu-id="efcbd-259">Sales order line 2:</span></span>

        - <span data-ttu-id="efcbd-260">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="efcbd-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="efcbd-261">**Daudzums:** *9016*</span><span class="sxs-lookup"><span data-stu-id="efcbd-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="efcbd-262">**Vienība:** *katra* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="efcbd-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="efcbd-263">Šeit sniegtie krājumi un daudzumi ir tikai piemēri.</span><span class="sxs-lookup"><span data-stu-id="efcbd-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="efcbd-264">Tie izmantos vienības secību grupu, ko definējāt iepriekš, tāpēc tiem ir jādefinē piemērota vienību pārveidošana no *ea* uz *Box* uz *PL* un krājumiem ir jābūt *62* noliktavā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="efcbd-265">Papildinformāciju skatiet sadaļā [Mērvienību un krājumu politikas](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="efcbd-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="efcbd-266">Atlasiet 1. pārdošanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-266">Select sales order line 1.</span></span> <span data-ttu-id="efcbd-267">Pēc tam sadaļas **Pārdošanas pasūtījuma rinda** izvēlnē **Krājumi** atlasiet **Rezervācijas**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="efcbd-268">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="efcbd-269">Atkārtojiet 4. un 5. soli pārdošanas pasūtījuma 2. rindai.</span><span class="sxs-lookup"><span data-stu-id="efcbd-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="efcbd-270">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="efcbd-271">Notiek tālāk aprakstītie notikumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-271">The following events occur:</span></span>

    - <span data-ttu-id="efcbd-272">Sistēma apstrādā izveidoto sūtījumu, izmantojot veidni, kas ietver etiķetes drukāšanas darbību.</span><span class="sxs-lookup"><span data-stu-id="efcbd-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="efcbd-273">Etiķetes izkārtojums tiks izmantots etiķetes formāta definēšanai un rezultāts būs etiķete, kas tiek drukāta uz printera, kas ir atlasīts etiķetes veidnē.</span><span class="sxs-lookup"><span data-stu-id="efcbd-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="efcbd-274">Kopuma etiķetes tiek ģenerētas un izdrukātas.</span><span class="sxs-lookup"><span data-stu-id="efcbd-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="efcbd-275">Etiķešu skaits būs vienāds ar kastu skaitu (šajā piemērā 376 kastu etiķetes 1. rindai un 322 kastu etiķetes 2. rindai).</span><span class="sxs-lookup"><span data-stu-id="efcbd-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="efcbd-276">Sūtījumiem tiek ģenerēts jauns preču transporta pavadzīmes ID.</span><span class="sxs-lookup"><span data-stu-id="efcbd-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="efcbd-277">Ja konfigurējāt numuru sērijas paplašinājumus, kopuma etiķešu ID sekos **SSCC-18** numura formātam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="efcbd-278">Varat skatīt un atkārtoti drukāt kopuma etiķetes no šādām lapām.</span><span class="sxs-lookup"><span data-stu-id="efcbd-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="efcbd-279">Katras lapas darbību rūts cilnē **Sūtījumi** grupā **Saistītā informācija**, atlasiet **Kopuma etiķetes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="efcbd-280">Visi sūtījumi \> Sūtījuma informācija</span><span class="sxs-lookup"><span data-stu-id="efcbd-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="efcbd-281">Visas kravas \> Kravas informācija</span><span class="sxs-lookup"><span data-stu-id="efcbd-281">All loads \> Load details</span></span>
- <span data-ttu-id="efcbd-282">Visi kopumi</span><span class="sxs-lookup"><span data-stu-id="efcbd-282">All waves</span></span>
- <span data-ttu-id="efcbd-283">Kopuma etiķetes</span><span class="sxs-lookup"><span data-stu-id="efcbd-283">Wave labels</span></span>
- <span data-ttu-id="efcbd-284">Kopuma etiķešu vēsture</span><span class="sxs-lookup"><span data-stu-id="efcbd-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="efcbd-285">2. scenārijs: kopuma etiķešu drukāšana konteinerizēšanai (bez kopuma etiķešu ierakstiem)</span><span class="sxs-lookup"><span data-stu-id="efcbd-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="efcbd-286">Šis scenārijs ļauj drukāt kopuma etiķetes, lietojot konteinerizēšanu, automātiskai krājumu sadalīšanai kastēs un tādēļ nav nepieciešams kopuma etiķešu ieraksts.</span><span class="sxs-lookup"><span data-stu-id="efcbd-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="efcbd-287">Šādā gadījumā konteinera ID darbojas kā SSCC vietturis.</span><span class="sxs-lookup"><span data-stu-id="efcbd-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="efcbd-288">Tālāk ir norādītas galvenās atšķirības starp šo scenāriju un 1. scenāriju:</span><span class="sxs-lookup"><span data-stu-id="efcbd-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="efcbd-289">**Kopuma etiķešu veidnes:** jūs nevarēsit atlasīt kopuma etiķešu veidu kopuma etiķešu veidnei, un nevajadzēs etiķešu kompilācijas grupēšanu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="efcbd-290">Pretējā gadījumā tiks konfigurēta kopuma etiķešu veidne, kas tiks saistīta ar kopuma veidni tādā pašā veidā, kā aprakstīts 1. scenārijā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="efcbd-291">Lai nepieļautu kopuma etiķešu ģenerēšanu, kopuma etiķešu veids ir jāatstāj tukšs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="efcbd-292">**Kopuma etiķešu izkārtojumi:** konfigurējiet kopuma etiķešu izkārtojuma rindas iestatījumus darba rindām, nevis kopuma etiķešu ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="efcbd-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="efcbd-293">Etiķetes izkārtojumam ir jākonfigurē rindas iestatījums, izmantojot **WHSWorkLine** tabulu, nevis **WHSWaveLabel** tabulu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="efcbd-294">Iestatījums **Rindu skaits lapā** kontrolē rindu skaitu, kas būs pamatteksta sadaļā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="efcbd-295">Šī konfigurācija ir piemērota arī uzņēmējdarbības scenārijiem, kur vairāki dažādi krājumi ir iepakoti vienā atzīmētā kastē vai uz paletes, un šo iepakošanas procesu var definēt pēc darba izveides (piemēram, darbs, kas grupēts pēc sūtījuma).</span><span class="sxs-lookup"><span data-stu-id="efcbd-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="efcbd-296">Šajā scenārijā tiek parādīti visi plūsmas posmi.</span><span class="sxs-lookup"><span data-stu-id="efcbd-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="efcbd-297">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="efcbd-297">Make demo data available</span></span>

<span data-ttu-id="efcbd-298">Lai sekotu šim scenārijam, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="efcbd-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="efcbd-299">Pārliecinieties, vai kopuma etiķešu metode ir pieejama</span><span class="sxs-lookup"><span data-stu-id="efcbd-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="efcbd-300">Lai padarītu pieejamu kopuma etiķešu drukāšanas metodi, var būt nepieciešams atkārtoti ģenerēt kopuma procesa metodes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="efcbd-301">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="efcbd-302">Apstipriniet, ka **waveLabelPrinting** ir sarakstā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="efcbd-303">Ja tā nav, darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**, lai to pievienotu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="efcbd-304">Iestatiet kopuma veidni</span><span class="sxs-lookup"><span data-stu-id="efcbd-304">Set up a wave template</span></span>

<span data-ttu-id="efcbd-305">Kopuma veidnes ļauj saistīt noteiktas kopuma metodes ar atbilstošo kopuma etiķešu veidni.</span><span class="sxs-lookup"><span data-stu-id="efcbd-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="efcbd-306">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="efcbd-307">Atlasiet veidni, kā **63 Konteinerizēšana**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="efcbd-308">Kopsavilkuma cilnē **Metodes** pārvietojiet metodi **Kopuma etiķešu drukāšana** uz kolonnu **Atlasītās metodes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="efcbd-309">Kolonnā **Atlasītās metodes** atlasiet metodi **Kopuma etiķešu drukāšana** un iestatiet tās lauku **Kopuma darbības kods** uz *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="efcbd-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="efcbd-310">Papildinformāciju par kopuma darbību kodiem skatiet sadaļā [Kopuma darbību kodi](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="efcbd-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="efcbd-311">Izveidot kopuma etiķešu izkārtojumu</span><span class="sxs-lookup"><span data-stu-id="efcbd-311">Create a wave label layout</span></span>

1. <span data-ttu-id="efcbd-312">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="efcbd-313">Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-314">**Etiķetes izkārtojuma ID:** *Carton*</span><span class="sxs-lookup"><span data-stu-id="efcbd-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="efcbd-315">**Apraksts:** *kaste (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="efcbd-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="efcbd-316">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="efcbd-317">Darbību rūtī atlasiet **Kopuma etiķešu rindas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="efcbd-318">Tiek parādīta lapa **Kopuma etiķešu rindas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="efcbd-319">Šeit varat konfigurēt etiķetes dinamisko daļu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="efcbd-320">Pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-321">**Rindas ID:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="efcbd-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="efcbd-322">**Rindas tabulas nosaukums:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="efcbd-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="efcbd-323">**Rindas sākuma pozīcija:** *500*</span><span class="sxs-lookup"><span data-stu-id="efcbd-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="efcbd-324">Šis lauks definē vertikālo pozīciju, kur rinda sāksies etiķetē.</span><span class="sxs-lookup"><span data-stu-id="efcbd-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="efcbd-325">**Rindas augstums:** *-50*</span><span class="sxs-lookup"><span data-stu-id="efcbd-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="efcbd-326">Šis lauks definē katras rindas augstumu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-326">This field defines the height of each row.</span></span> <span data-ttu-id="efcbd-327">Rindas augstums ir pozitīvs horizontālajām etiķetēm un negatīvs vertikālajām etiķetēm.</span><span class="sxs-lookup"><span data-stu-id="efcbd-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="efcbd-328">**Rindu skaits lapā:** *5*</span><span class="sxs-lookup"><span data-stu-id="efcbd-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="efcbd-329">Šis lauks definē rindu skaitu, ko var drukāt uz katras etiķetes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="efcbd-330">Šajā iestatījumā tiks drukātas vairākas ZPL etiķetes katram darbam, kur katra lapa var ietvert līdz piecām darba rindām.</span><span class="sxs-lookup"><span data-stu-id="efcbd-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="efcbd-331">Piemēram, ja etiķete tiek drukāta konteineram ar 12 rindām, tiks izdrukātas trīs etiķetes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="efcbd-332">Ja vēlaties drukāt atsevišķu etiķeti katrai izdošanas rindai, iestatiet šo vērtību uz *1*.</span><span class="sxs-lookup"><span data-stu-id="efcbd-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="efcbd-333">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-333">Close the page.</span></span>
1. <span data-ttu-id="efcbd-334">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="efcbd-335">Vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-336">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-337">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-338">**Lauks:** *Darba veids*</span><span class="sxs-lookup"><span data-stu-id="efcbd-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="efcbd-339">**Kritēriji:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="efcbd-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="efcbd-340">Ja vēlaties varēt drukāt preču transporta pavadzīmes ID, cilnē **Savienojumi** atlasiet tabulu **Darba rindas** un pievienojiet tai tabulu **Sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="efcbd-341">Aizveriet vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="efcbd-342">Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="efcbd-343">Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="efcbd-344">Piemēram, ja lietojat Zebra printerus, varat izmantot šādu kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="efcbd-345">Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes pamatteksts**, ievadiet vajadzīgā pamatteksta ZPL kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="efcbd-346">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="efcbd-347">Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes kājene**, ievadiet vajadzīgās kājenes ZPL kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="efcbd-348">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="efcbd-349">Šajā iestatījumā tiks drukāts viens katras etiķetes eksemplārs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="efcbd-350">Ja ir nepieciešamas vairākas kopijas (piemēram, viena kopija katrai paletes pusei), iestatiet **n** vērtību sekcijai **\^PQn** kājenē līdz nepieciešamajam kopiju skaitam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="efcbd-351">Piemēram, lai izdrukātu katras etiķetes četras kopijas, norādiet **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="efcbd-352">Tagad etiķete ir gatava lietošanai.</span><span class="sxs-lookup"><span data-stu-id="efcbd-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="efcbd-353">Izveidot kopuma etiķešu veidni</span><span class="sxs-lookup"><span data-stu-id="efcbd-353">Create a wave label template</span></span>

1. <span data-ttu-id="efcbd-354">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidnes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="efcbd-355">Pievienojiet kopuma līmeņa veidni un galvenē iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="efcbd-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="efcbd-356">**Etiķetes veidnes nosaukums:** *Container labels*</span><span class="sxs-lookup"><span data-stu-id="efcbd-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="efcbd-357">**Apraksts:** *Konteineru etiķetes*</span><span class="sxs-lookup"><span data-stu-id="efcbd-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="efcbd-358">**Kopuma darbības kods:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="efcbd-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="efcbd-359">**Noliktava:** *63*</span><span class="sxs-lookup"><span data-stu-id="efcbd-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="efcbd-360">Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-361">**Etiķetes izkārtojuma ID:** *Container*</span><span class="sxs-lookup"><span data-stu-id="efcbd-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="efcbd-362">**Printera nosaukums:** atlasiet atbilstošu ZPL printeri.</span><span class="sxs-lookup"><span data-stu-id="efcbd-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="efcbd-363">**Izpildīt vaicājumu:** *Jā* (Šis iestatījums nav obligāts, bet tas ir ieteicams optimālai veiktspējai.)</span><span class="sxs-lookup"><span data-stu-id="efcbd-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="efcbd-364">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="efcbd-365">Neobligāti: ja iestatāt debitoram raksturīgu etiķešu noformējumu, ir jāizveido vaicājums, lai atrastu debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="efcbd-366">Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="efcbd-367">Pēc tam, vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-368">**Tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="efcbd-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="efcbd-369">**Atvasinātā tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="efcbd-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="efcbd-370">**Lauks:** *Konta numurs*</span><span class="sxs-lookup"><span data-stu-id="efcbd-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="efcbd-371">**Kritēriji:** ievadiet atbilstošo debitora konta numuru.</span><span class="sxs-lookup"><span data-stu-id="efcbd-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="efcbd-372">Kad esat pabeidzis, atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="efcbd-373">Konfigurēt numuru sērijas paplašinājumus</span><span class="sxs-lookup"><span data-stu-id="efcbd-373">Configure number sequence extensions</span></span>

<span data-ttu-id="efcbd-374">Numuru sērijas paplašinājumi kontrolē GS1 atbilstību noteiktām numuru sērijām.</span><span class="sxs-lookup"><span data-stu-id="efcbd-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="efcbd-375">Šī konfigurācija nav obligāta pašreizējam scenārijam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="efcbd-376">Papildinformāciju un konfigurācijas norādījumus skatiet sadaļā [Konfigurēt numuru sērijas paplašinājumus](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="efcbd-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="efcbd-377">Izveidot pārdošanas pasūtījumu un nodot to noliktavai</span><span class="sxs-lookup"><span data-stu-id="efcbd-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="efcbd-378">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījums \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="efcbd-379">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-380">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="efcbd-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="efcbd-381">**Noliktava:** *63*</span><span class="sxs-lookup"><span data-stu-id="efcbd-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="efcbd-382">Pievienojiet piecas pārdošanas pasūtījuma rindas:</span><span class="sxs-lookup"><span data-stu-id="efcbd-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="efcbd-383">1. pārdošanas pasūtījuma rinda:</span><span class="sxs-lookup"><span data-stu-id="efcbd-383">Sales order line 1:</span></span>

        - <span data-ttu-id="efcbd-384">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="efcbd-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="efcbd-385">**Daudzums:** *10*</span><span class="sxs-lookup"><span data-stu-id="efcbd-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="efcbd-386">2. pārdošanas pasūtījuma rinda:</span><span class="sxs-lookup"><span data-stu-id="efcbd-386">Sales order line 2:</span></span>

        - <span data-ttu-id="efcbd-387">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="efcbd-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="efcbd-388">**Daudzums:** *20*</span><span class="sxs-lookup"><span data-stu-id="efcbd-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="efcbd-389">3. pārdošanas pasūtījuma rinda:</span><span class="sxs-lookup"><span data-stu-id="efcbd-389">Sales order line 3:</span></span>

        - <span data-ttu-id="efcbd-390">**Krājuma numurs:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="efcbd-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="efcbd-391">**Daudzums:** *20*</span><span class="sxs-lookup"><span data-stu-id="efcbd-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="efcbd-392">4. pārdošanas pasūtījuma rinda:</span><span class="sxs-lookup"><span data-stu-id="efcbd-392">Sales order line 4:</span></span>

        - <span data-ttu-id="efcbd-393">**Krājuma numurs:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="efcbd-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="efcbd-394">**Daudzums:** *40*</span><span class="sxs-lookup"><span data-stu-id="efcbd-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="efcbd-395">5. pārdošanas pasūtījuma rinda:</span><span class="sxs-lookup"><span data-stu-id="efcbd-395">Sales order line 5:</span></span>

        - <span data-ttu-id="efcbd-396">**Krājuma numurs:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="efcbd-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="efcbd-397">**Daudzums:** *50*</span><span class="sxs-lookup"><span data-stu-id="efcbd-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="efcbd-398">Šeit sniegtie krājumi un daudzumi ir tikai piemēri.</span><span class="sxs-lookup"><span data-stu-id="efcbd-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="efcbd-399">Krājumiem ir jābūt norādītajā noliktavā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="efcbd-400">Atlasiet 1. pārdošanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-400">Select sales order line 1.</span></span> <span data-ttu-id="efcbd-401">Pēc tam sadaļas **Pārdošanas pasūtījuma rinda** izvēlnē **Krājumi** atlasiet **Rezervācijas**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="efcbd-402">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="efcbd-403">Atkārtojiet 4. un 5. soli katrai papildu pārdošanas pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="efcbd-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="efcbd-404">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="efcbd-405">Notiek tālāk aprakstītie notikumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-405">The following events occur:</span></span>

    - <span data-ttu-id="efcbd-406">Sistēma apstrādā izveidoto sūtījumu, izmantojot veidni, kas ietver etiķetes drukāšanas darbību.</span><span class="sxs-lookup"><span data-stu-id="efcbd-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="efcbd-407">Etiķetes izkārtojums tiks izmantots etiķetes formāta definēšanai un gala rezultāts būs etiķete ar piecām rindām un, kas tiek drukāta uz printera, kas ir atlasīts etiķetes veidnē.</span><span class="sxs-lookup"><span data-stu-id="efcbd-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="efcbd-408">Sūtījumiem tiek ģenerēts jauns preču transporta pavadzīmes ID.</span><span class="sxs-lookup"><span data-stu-id="efcbd-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="efcbd-409">Ja konfigurējāt numuru sērijas paplašinājumus, kopuma etiķešu ID sekos **SSCC-18** numura formātam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="efcbd-410">Varat atkārtoti drukāt šīs kopuma etiķetes, dodoties uz **Noliktavas pārvaldība \> Pieprasījumi un pārskati \> Kopuma etiķešu vēsture**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="efcbd-411">3. scenārijs: kopuma etiķešu drukāšana vairākrindu etiķetēm</span><span class="sxs-lookup"><span data-stu-id="efcbd-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="efcbd-412">Šajā scenārijā ir parādīts, kā izmantot kopuma etiķešu drukāšanas funkcionalitāti, kad noliktavas procesos ir nepieciešamas vairākas nosūtīšanas etiķešu rindas.</span><span class="sxs-lookup"><span data-stu-id="efcbd-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="efcbd-413">Piemēram, atsevišķas etiķetes ir jādrukā kastēm un paletēm, un var būt nepieciešams drukāt pārtraukuma etiķetes visam sūtījumam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="efcbd-414">Pārtraukuma etiķetes ir atsevišķs etiķešu veids, ko var izmantot kā dalītāju starp ruļļiem un konteineriem, piemēram, sūtījuma ID un svītrkoda etiķetes, lai etiķetes varētu viegli kārtot pēc to drukāšanas.</span><span class="sxs-lookup"><span data-stu-id="efcbd-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="efcbd-415">Galvenā atšķirība starp šī scenārija konfigurāciju un 1. scenārija konfigurāciju, papildus faktam, ka ir iespējotas pārtraukuma etiķetes, ir tā, ka vairāki kopuma etiķešu veidi ir jāsaista ar kopuma etiķešu veidnēm un vienību secību grupas rindām.</span><span class="sxs-lookup"><span data-stu-id="efcbd-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="efcbd-416">Lai izpildītu šo konfigurāciju, šim scenārijam jāiestata šādi elementi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="efcbd-417">**Kopuma apstrādes metodes:** atzīmējiet kopuma etiķešu metodi kā “atkārtojamu”, pievienojiet to diviem (vai vairākiem) laikiem kopuma veidnē un iestatiet dažādus kopuma darbību kodus.</span><span class="sxs-lookup"><span data-stu-id="efcbd-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="efcbd-418">**Kopuma etiķešu veidnes:** konfigurējiet kopuma etiķešu veidnes un saistiet tās ar kopuma veidnēm.</span><span class="sxs-lookup"><span data-stu-id="efcbd-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="efcbd-419">Katrai kopuma etiķešu veidnei ir savs kopuma etiķetes veids.</span><span class="sxs-lookup"><span data-stu-id="efcbd-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="efcbd-420">**Kopuma etiķešu izkārtojumi:** tiks izveidoti vairāki kopuma etiķešu izkārtojumi.</span><span class="sxs-lookup"><span data-stu-id="efcbd-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="efcbd-421">Katrai etiķešu “rindai” būs atsevišķs etiķešu izkārtojums, kā arī pārtraukuma etiķešu izkārtojums.</span><span class="sxs-lookup"><span data-stu-id="efcbd-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="efcbd-422">Šajā scenārijā tiek parādīti visi plūsmas posmi.</span><span class="sxs-lookup"><span data-stu-id="efcbd-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="efcbd-423">Padarīt demonstrācijas datus pieejamus</span><span class="sxs-lookup"><span data-stu-id="efcbd-423">Make demo data available</span></span>

<span data-ttu-id="efcbd-424">Lai sekotu šim scenārijam, ir jābūt instalētiem demonstrācijas datiem, un jums ir jāatlasa **USMF** juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="efcbd-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="efcbd-425">Kopuma apstrādes metodes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="efcbd-425">Set up a wave process method</span></span>

1. <span data-ttu-id="efcbd-426">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma procesa metodes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="efcbd-427">Apstipriniet, ka **waveLabelPrinting** ir sarakstā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="efcbd-428">Ja tā nav, darbību rūtī atlasiet **Atkārtoti ģenerēt metodes**, lai to pievienotu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="efcbd-429">Metodei **waveLabelPrinting** atzīmējiet izvēles rūtiņu **Metode atkārtojama**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="efcbd-430">Iestatiet kopuma veidni</span><span class="sxs-lookup"><span data-stu-id="efcbd-430">Set up a wave template</span></span>

1. <span data-ttu-id="efcbd-431">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="efcbd-432">Atlasiet veidni, kā **62 Sūtījums pēc noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="efcbd-433">Kopsavilkuma cilnē **Metodes** pārvietojiet metodi **Kopuma etiķešu drukāšana** uz kolonnu **Atlasītās metodes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="efcbd-434">Kolonnā **Atlasītās metodes** piešķiriet **Kopuma darbības kods** vērtību, piemēram, *Kaste* metodei **Kopuma etiķešu drukāšana**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="efcbd-435">Papildinformāciju par kopuma darbību kodiem skatiet sadaļā [Kopuma darbību kodi](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="efcbd-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="efcbd-436">Pārvietojiet metodi **Kopuma etiķešu drukāšana** uz kolonnu **Atlasītās metodes** otro reizi.</span><span class="sxs-lookup"><span data-stu-id="efcbd-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="efcbd-437">Kolonnā **Atlasītās metodes** piešķiriet citu **Kopuma darbības kods** vērtību, piemēram, *Palete* otrai **Kopuma etiķešu drukāšana** metodei.</span><span class="sxs-lookup"><span data-stu-id="efcbd-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="efcbd-438">Papildinformāciju par kopuma darbību kodiem skatiet sadaļā [Kopuma darbību kodi](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="efcbd-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="efcbd-439">Izveidot trīs kopuma etiķešu izkārtojumus</span><span class="sxs-lookup"><span data-stu-id="efcbd-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="efcbd-440">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu izkārtojumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="efcbd-441">Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-442">**Etiķetes izkārtojuma ID:** *Carton*</span><span class="sxs-lookup"><span data-stu-id="efcbd-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="efcbd-443">**Apraksts:** *kaste (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="efcbd-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="efcbd-444">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="efcbd-445">Darbību rūtī atlasiet **Kopuma etiķešu rindas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="efcbd-446">Tiek parādīta lapa **Kopuma etiķešu rindas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="efcbd-447">Šeit varat konfigurēt etiķetes dinamisko daļu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="efcbd-448">Pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-449">**Rindas ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="efcbd-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="efcbd-450">**Rindas tabulas nosaukums:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="efcbd-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="efcbd-451">**Rindas sākuma pozīcija:** *0*</span><span class="sxs-lookup"><span data-stu-id="efcbd-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="efcbd-452">Šis lauks definē vertikālo pozīciju, kur rinda sāksies etiķetē.</span><span class="sxs-lookup"><span data-stu-id="efcbd-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="efcbd-453">**Rindas augstums:** *0*</span><span class="sxs-lookup"><span data-stu-id="efcbd-453">**Row height:** *0*</span></span>

        <span data-ttu-id="efcbd-454">Šis lauks definē katras rindas augstumu (punktos) atbilstoši ZPL standartam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="efcbd-455">Rindas augstums ir pozitīvs horizontālajām etiķetēm un negatīvs vertikālajām etiķetēm.</span><span class="sxs-lookup"><span data-stu-id="efcbd-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="efcbd-456">Tā kā šajā piemērā ir tikai viena rinda, varat iestatīt vērtību *0* (nulle).</span><span class="sxs-lookup"><span data-stu-id="efcbd-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="efcbd-457">**Rindu skaits lapā:** *1*</span><span class="sxs-lookup"><span data-stu-id="efcbd-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="efcbd-458">Šis lauks definē rindu skaitu, ko var drukāt uz katras etiķetes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="efcbd-459">Šis iestatījums radīs atsevišķu ZPL etiķeti, ko drukāt katram ierakstam kopuma etiķešu tabulā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="efcbd-460">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-460">Close the page.</span></span>
1. <span data-ttu-id="efcbd-461">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="efcbd-462">Vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-463">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-464">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-465">**Lauks:** *Darba veids*</span><span class="sxs-lookup"><span data-stu-id="efcbd-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="efcbd-466">**Kritēriji:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="efcbd-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="efcbd-467">Šis vaicājums nodrošina, ka etiķetē tiks drukātas tikai izdošanas veida darba rindas, nevis izvietošanas veida darba rindas.</span><span class="sxs-lookup"><span data-stu-id="efcbd-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="efcbd-468">Ja vēlaties varēt drukāt preču transporta pavadzīmes ID, cilnē **Savienojumi** atlasiet tabulu **Darba rindas** un pievienojiet tai tabulu **Sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="efcbd-469">Aizveriet vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="efcbd-470">Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="efcbd-471">Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="efcbd-472">Piemēram, ja lietojat Zebra printerus, varat izmantot šādu kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="efcbd-473">Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes pamatteksts**, ievadiet vajadzīgā pamatteksta ZPL kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="efcbd-474">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="efcbd-475">Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes kājene**, ievadiet vajadzīgās kājenes ZPL kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="efcbd-476">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="efcbd-477">Šajā iestatījumā tiks drukāts viens katras etiķetes eksemplārs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="efcbd-478">Ja ir nepieciešamas vairākas kopijas (piemēram, viena kopija katrai paletes pusei), iestatiet **n** vērtību sekcijai **\^PQn** kājenē līdz nepieciešamajam kopiju skaitam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="efcbd-479">Piemēram, lai izdrukātu katras etiķetes četras kopijas, norādiet **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="efcbd-480">Pirmā etiķete tagad ir gatava lietošanai.</span><span class="sxs-lookup"><span data-stu-id="efcbd-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="efcbd-481">Izveidojiet otru izkārtojuma ierakstu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-482">**Etiķetes izkārtojuma ID:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="efcbd-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="efcbd-483">**Apraksts:** *Palete*</span><span class="sxs-lookup"><span data-stu-id="efcbd-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="efcbd-484">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="efcbd-485">Darbību rūtī atlasiet **Kopuma etiķešu rindas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="efcbd-486">Tiek parādīta lapa **Kopuma etiķešu rindas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="efcbd-487">Šeit varat konfigurēt etiķetes dinamisko daļu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="efcbd-488">Pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-489">**Rindas ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="efcbd-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="efcbd-490">**Rindas tabulas nosaukums:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="efcbd-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="efcbd-491">**Rindas sākuma pozīcija:** *0*</span><span class="sxs-lookup"><span data-stu-id="efcbd-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="efcbd-492">Šis lauks definē vertikālo pozīciju, kur rinda sāksies etiķetē.</span><span class="sxs-lookup"><span data-stu-id="efcbd-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="efcbd-493">**Rindas augstums:** *0*</span><span class="sxs-lookup"><span data-stu-id="efcbd-493">**Row height:** *0*</span></span>

        <span data-ttu-id="efcbd-494">Šis lauks definē katras rindas augstumu (punktos) atbilstoši ZPL standartam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="efcbd-495">Rindas augstums ir pozitīvs horizontālajām etiķetēm un negatīvs vertikālajām etiķetēm.</span><span class="sxs-lookup"><span data-stu-id="efcbd-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="efcbd-496">Tā kā šajā piemērā ir tikai viena rinda, varat iestatīt vērtību *0* (nulle).</span><span class="sxs-lookup"><span data-stu-id="efcbd-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="efcbd-497">**Rindu skaits lapā:** *1*</span><span class="sxs-lookup"><span data-stu-id="efcbd-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="efcbd-498">Šis lauks definē rindu skaitu, ko var drukāt uz katras etiķetes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="efcbd-499">Šis iestatījums rada atsevišķu ZPL etiķeti, ko drukāt katram ierakstam kopuma etiķešu tabulā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="efcbd-500">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-500">Close the page.</span></span>
1. <span data-ttu-id="efcbd-501">Darbību rūtī atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="efcbd-502">Vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-503">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-504">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-505">**Lauks:** *Darba veids*</span><span class="sxs-lookup"><span data-stu-id="efcbd-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="efcbd-506">**Kritēriji:** *Izdošana*</span><span class="sxs-lookup"><span data-stu-id="efcbd-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="efcbd-507">Šis vaicājums nodrošina, ka etiķetē tiks drukātas tikai izdošanas veida darba rindas, nevis izvietošanas veida darba rindas.</span><span class="sxs-lookup"><span data-stu-id="efcbd-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="efcbd-508">Ja vēlaties varēt drukāt preču transporta pavadzīmes ID, cilnē **Savienojumi** atlasiet tabulu **Darba rindas** un pievienojiet tai tabulu **Sūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="efcbd-509">Aizveriet vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="efcbd-510">Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="efcbd-511">Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="efcbd-512">Piemēram, ja lietojat Zebra printerus, varat izmantot šādu kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="efcbd-513">Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes pamatteksts**, ievadiet vajadzīgā pamatteksta ZPL kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="efcbd-514">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="efcbd-515">Sadaļas **Pamatteksta sadaļa** laukā **Etiķetes kājene**, ievadiet vajadzīgās kājenes ZPL kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="efcbd-516">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="efcbd-517">Šajā iestatījumā tiks drukāts viens katras etiķetes eksemplārs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="efcbd-518">Ja ir nepieciešamas vairākas kopijas (piemēram, viena kopija katrai paletes pusei), iestatiet **n** vērtību sekcijai **\^PQn** kājenē līdz nepieciešamajam kopiju skaitam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="efcbd-519">Piemēram, lai izdrukātu katras etiķetes četras kopijas, norādiet **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="efcbd-520">Otrā etiķete tagad ir gatava lietošanai.</span><span class="sxs-lookup"><span data-stu-id="efcbd-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="efcbd-521">Izveidojiet trešo izkārtojuma ierakstu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-522">**Etiķetes izkārtojuma ID:** *Break*</span><span class="sxs-lookup"><span data-stu-id="efcbd-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="efcbd-523">**Apraksts:** *Pārtraukuma etiķete*</span><span class="sxs-lookup"><span data-stu-id="efcbd-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="efcbd-524">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="efcbd-525">Kopsavilkuma cilnei **Printera teksta izkārtojums** ir trīs sadaļas, kur var rakstīt printera kodu: **Galvenes sadaļa**, **Pamatteksta sadaļa** un **Kājenes sadaļa**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="efcbd-526">Sadaļas **Galvenes sadaļa** laukā **Etiķetes virsraksts**, ievadiet vajadzīgās galvenes ZPL kodu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="efcbd-527">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="efcbd-528">Šoreiz pamatteksts nav nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="efcbd-528">This time, no body is required.</span></span> <span data-ttu-id="efcbd-529">Tādēļ vienkārši ievadiet nepieciešamo tekstu sadaļā **Kājenes sadaļa**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="efcbd-530">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="efcbd-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="efcbd-531">Trešā etiķete tagad ir gatava lietošanai.</span><span class="sxs-lookup"><span data-stu-id="efcbd-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="efcbd-532">Trešā etiķete ir pārtraukuma etiķete, kas tiks izmantota kā dalītājs starp etiķešu ruļļiem.</span><span class="sxs-lookup"><span data-stu-id="efcbd-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="efcbd-533">Izveidot divus kopuma etiķešu veidus</span><span class="sxs-lookup"><span data-stu-id="efcbd-533">Create two wave label types</span></span>

1. <span data-ttu-id="efcbd-534">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="efcbd-535">Izveidojiet ierakstu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-536">**Etiķetes veids:** *Carton*</span><span class="sxs-lookup"><span data-stu-id="efcbd-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="efcbd-537">**Apraksts:** *Kaste*</span><span class="sxs-lookup"><span data-stu-id="efcbd-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="efcbd-538">Izveidojiet otru ierakstu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-539">**Etiķetes veids:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="efcbd-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="efcbd-540">**Apraksts:** *Palete*</span><span class="sxs-lookup"><span data-stu-id="efcbd-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="efcbd-541">Iestatīt vienību secību grupas</span><span class="sxs-lookup"><span data-stu-id="efcbd-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="efcbd-542">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Vienību secību grupas**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="efcbd-543">Atlasiet vai izveidojiet **Ea Box PL** grupu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="efcbd-544">Rindā **Kaste** iestatiet lauku **Kopuma līmeņa veids** uz *Kartons*.</span><span class="sxs-lookup"><span data-stu-id="efcbd-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="efcbd-545">Rindā **PL** iestatiet lauku **Kopuma līmeņa veids** uz *Palete*.</span><span class="sxs-lookup"><span data-stu-id="efcbd-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="efcbd-546">Izveidot kopuma etiķešu veidnes</span><span class="sxs-lookup"><span data-stu-id="efcbd-546">Create wave label templates</span></span>

1. <span data-ttu-id="efcbd-547">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \> Dokumentu maršrutēšana \> Kopuma etiķešu veidnes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="efcbd-548">Izveidojiet etiķešu veidni, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-549">**Etiķetes veidnes nosaukums:** *Carton labels*</span><span class="sxs-lookup"><span data-stu-id="efcbd-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="efcbd-550">**Apraksts:** *Kastu etiķetes*</span><span class="sxs-lookup"><span data-stu-id="efcbd-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="efcbd-551">**Kopuma darbības kods:** *Carton*</span><span class="sxs-lookup"><span data-stu-id="efcbd-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="efcbd-552">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="efcbd-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="efcbd-553">Kopsavilkuma cilnes **Vispārīgi** laukā **Kopuma etiķešu veids** atlasiet vērtību, piemēram, *Kaste*.</span><span class="sxs-lookup"><span data-stu-id="efcbd-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="efcbd-554">Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-555">**Etiķetes izkārtojuma ID:** *Carton*</span><span class="sxs-lookup"><span data-stu-id="efcbd-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="efcbd-556">**Printera nosaukums:** atlasiet atbilstošu ZPL printeri.</span><span class="sxs-lookup"><span data-stu-id="efcbd-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="efcbd-557">**Izpildīt vaicājumu:** *Jā* (Šis iestatījums nav obligāts, bet tas ir ieteicams optimālai veiktspējai.)</span><span class="sxs-lookup"><span data-stu-id="efcbd-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="efcbd-558">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="efcbd-559">Neobligāti: ja iestatāt debitoram raksturīgu etiķešu noformējumu, ir jāizveido vaicājums, lai atrastu debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="efcbd-560">Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="efcbd-561">Pēc tam, vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-562">**Tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="efcbd-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="efcbd-563">**Atvasinātā tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="efcbd-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="efcbd-564">**Lauks:** *Konta numurs*</span><span class="sxs-lookup"><span data-stu-id="efcbd-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="efcbd-565">**Kritēriji:** ievadiet atbilstošo debitora konta numuru.</span><span class="sxs-lookup"><span data-stu-id="efcbd-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="efcbd-566">Kad esat pabeidzis, atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="efcbd-567">Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktora dialoglodziņu visai etiķešu veidnei.</span><span class="sxs-lookup"><span data-stu-id="efcbd-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="efcbd-568">Vaicājumu redaktora dialoglodziņā, cilnē **Kārtošana** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-569">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-570">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-571">**Lauks:** *Atsauces kravas rindas ID (Ieraksta ID)*</span><span class="sxs-lookup"><span data-stu-id="efcbd-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="efcbd-572">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="efcbd-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="efcbd-573">Pievienojiet otru rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-574">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-575">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-576">**Lauks:** *Sūtījuma ID*</span><span class="sxs-lookup"><span data-stu-id="efcbd-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="efcbd-577">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="efcbd-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="efcbd-578">Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="efcbd-579">Ziņojuma lodziņš aicina apstiprināt grupēšanas atiestatīšanas darbību.</span><span class="sxs-lookup"><span data-stu-id="efcbd-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="efcbd-580">Lai turpinātu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="efcbd-581">Darbību rūtī atlasiet **Kopuma etiķešu veidņu grupēšana**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="efcbd-582">Dialoglodziņā **Kopuma etiķešu veidņu grupēšana** rindai, kur lauks **Atsauces lauka nosaukums** ir iestatīts uz *Sūtījuma ID*, iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="efcbd-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="efcbd-583">**Drukāt pārtraukuma etiķetes:** atzīmējiet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="efcbd-584">**Etiķetes izkārtojuma ID:** atlasiet pārtraukuma etiķeti.</span><span class="sxs-lookup"><span data-stu-id="efcbd-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="efcbd-585">(Piemēram, atlasiet etiķešu izkārtojumu *Break*, ko izveidojāt iepriekš šajā scenārijā.)</span><span class="sxs-lookup"><span data-stu-id="efcbd-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="efcbd-586">**Printera nosaukums:** atlasiet printeri pārtraukuma etiķetēm.</span><span class="sxs-lookup"><span data-stu-id="efcbd-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="efcbd-587">(Parasti, lai sadalītu etiķešu ruļļus, ir jāatlasa tas pats printeris, kas atlasīts kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="efcbd-588">Tomēr ir iespējami arī citi scenāriji.)</span><span class="sxs-lookup"><span data-stu-id="efcbd-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="efcbd-589">Rindai, kuras lauks **Atsauces lauka nosaukums** ir iestatīts uz *Atsauces kravas rindas ID*, atzīmējiet izvēles rūtiņu **Etiķešu kompilācijas ID**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="efcbd-590">Šis iestatījums izveidos vienu etiķetes secību (“carton 1 X”) kravas rindai visā kopumā, neņemot vērā darba grupēšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="efcbd-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="efcbd-591">Šo etiķešu secību var drukāt uz etiķešu izkārtojuma.</span><span class="sxs-lookup"><span data-stu-id="efcbd-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="efcbd-592">Turklāt atlasītās pārtraukuma etiķetes atdala dažādu sūtījumu etiķetes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="efcbd-593">Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Kopuma etiķešu veidņu grupēšana**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="efcbd-594">Izveidojiet otru etiķešu veidni, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-595">**Etiķetes veidnes nosaukums:** *Pallet labels*</span><span class="sxs-lookup"><span data-stu-id="efcbd-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="efcbd-596">**Apraksts:** *Palešu etiķetes*</span><span class="sxs-lookup"><span data-stu-id="efcbd-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="efcbd-597">**Kopuma darbības kods:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="efcbd-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="efcbd-598">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="efcbd-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="efcbd-599">Kopsavilkuma cilnes **Vispārīgi** laukā **Kopuma etiķešu veids** atlasiet vērtību, piemēram, *Palete*.</span><span class="sxs-lookup"><span data-stu-id="efcbd-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="efcbd-600">Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-601">**Etiķetes izkārtojuma ID:** *Pallet*</span><span class="sxs-lookup"><span data-stu-id="efcbd-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="efcbd-602">**Printera nosaukums:** atlasiet atbilstošu ZPL printeri.</span><span class="sxs-lookup"><span data-stu-id="efcbd-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="efcbd-603">**Izpildīt vaicājumu:** *Jā* (Šis iestatījums nav obligāts, bet tas ir ieteicams optimālai veiktspējai.)</span><span class="sxs-lookup"><span data-stu-id="efcbd-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="efcbd-604">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="efcbd-605">Neobligāti: ja iestatāt debitoram raksturīgu etiķešu noformējumu, ir jāizveido vaicājums, lai atrastu debitora kontu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="efcbd-606">Kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija** atlasiet **Rediģēt vaicājumu**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="efcbd-607">Pēc tam, vaicājumu redaktora dialoglodziņā, cilnē **Diapazons** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-608">**Tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="efcbd-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="efcbd-609">**Atvasinātā tabula:** *Sūtījumi*</span><span class="sxs-lookup"><span data-stu-id="efcbd-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="efcbd-610">**Lauks:** *Konta numurs*</span><span class="sxs-lookup"><span data-stu-id="efcbd-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="efcbd-611">**Kritēriji:** ievadiet atbilstošo debitora konta numuru.</span><span class="sxs-lookup"><span data-stu-id="efcbd-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="efcbd-612">Kad esat pabeidzis, atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="efcbd-613">Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atvērtu vaicājumu redaktora dialoglodziņu visai etiķešu veidnei.</span><span class="sxs-lookup"><span data-stu-id="efcbd-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="efcbd-614">Vaicājumu redaktora dialoglodziņā, cilnē **Kārtošana** pievienojiet rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-615">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-616">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-617">**Lauks:** *Atsauces kravas rindas ID (Ieraksta ID)*</span><span class="sxs-lookup"><span data-stu-id="efcbd-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="efcbd-618">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="efcbd-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="efcbd-619">Pievienojiet otru rindu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-620">**Tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-621">**Atveidotā tabula:** *Darba rindas*</span><span class="sxs-lookup"><span data-stu-id="efcbd-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="efcbd-622">**Lauks:** *Sūtījuma ID*</span><span class="sxs-lookup"><span data-stu-id="efcbd-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="efcbd-623">**Meklēšanas virziens:** *Augošā secībā*</span><span class="sxs-lookup"><span data-stu-id="efcbd-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="efcbd-624">Atlasiet **Labi**, lai aizvērtu vaicājumu redaktora dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="efcbd-625">Ziņojuma lodziņš aicina apstiprināt grupēšanas atiestatīšanas darbību.</span><span class="sxs-lookup"><span data-stu-id="efcbd-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="efcbd-626">Lai turpinātu, atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="efcbd-627">Darbību rūtī atlasiet **Kopuma etiķešu veidņu grupēšana**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="efcbd-628">Dialoglodziņā **Kopuma etiķešu veidņu grupēšana** rindai, kur lauks **Atsauces lauka nosaukums** ir iestatīts uz *Sūtījuma ID*, iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="efcbd-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="efcbd-629">**Drukāt pārtraukuma etiķetes:** atzīmējiet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="efcbd-630">**Etiķetes izkārtojuma ID:** atlasiet pārtraukuma etiķeti.</span><span class="sxs-lookup"><span data-stu-id="efcbd-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="efcbd-631">(Piemēram, atlasiet etiķešu izkārtojumu *Break*, ko izveidojāt iepriekš šajā scenārijā.)</span><span class="sxs-lookup"><span data-stu-id="efcbd-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="efcbd-632">**Printera nosaukums:** atlasiet printeri pārtraukuma etiķetēm.</span><span class="sxs-lookup"><span data-stu-id="efcbd-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="efcbd-633">(Parasti, lai sadalītu etiķešu ruļļus, ir jāatlasa tas pats printeris, kas atlasīts kopsavilkuma cilnē **Kopuma etiķešu veidnes informācija**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="efcbd-634">Tomēr ir iespējami arī citi scenāriji.)</span><span class="sxs-lookup"><span data-stu-id="efcbd-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="efcbd-635">Rindai, kuras lauks **Atsauces lauka nosaukums** ir iestatīts uz *Atsauces kravas rindas ID*, atzīmējiet izvēles rūtiņu **Etiķešu kompilācijas ID**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="efcbd-636">Šis iestatījums izveidos vienu etiķetes secību (“carton 1 X”) kravas rindai visā kopumā, neņemot vērā darba grupēšanas iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="efcbd-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="efcbd-637">Šo etiķešu secību var drukāt uz etiķešu izkārtojuma.</span><span class="sxs-lookup"><span data-stu-id="efcbd-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="efcbd-638">Turklāt atlasītās pārtraukuma etiķetes atdala dažādu sūtījumu etiķetes.</span><span class="sxs-lookup"><span data-stu-id="efcbd-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="efcbd-639">Konfigurēt numuru sērijas paplašinājumus</span><span class="sxs-lookup"><span data-stu-id="efcbd-639">Configure number sequence extensions</span></span>

<span data-ttu-id="efcbd-640">Numuru sērijas paplašinājumi kontrolē GS1 atbilstību noteiktām numuru sērijām.</span><span class="sxs-lookup"><span data-stu-id="efcbd-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="efcbd-641">Šī konfigurācija nav obligāta pašreizējam scenārijam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="efcbd-642">Papildinformāciju un konfigurācijas norādījumus skatiet sadaļā [Konfigurēt numuru sērijas paplašinājumus](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="efcbd-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="efcbd-643">Izveidot pārdošanas pasūtījumu un nodot to noliktavai</span><span class="sxs-lookup"><span data-stu-id="efcbd-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="efcbd-644">Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījums \> Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="efcbd-645">Izveidojiet pārdošanas pasūtījumu, kam ir turpmāk aprakstītie iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="efcbd-646">**Debitora konts:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="efcbd-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="efcbd-647">**Noliktava:** *62*</span><span class="sxs-lookup"><span data-stu-id="efcbd-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="efcbd-648">Pievienojiet divas pārdošanas pasūtījuma rindas:</span><span class="sxs-lookup"><span data-stu-id="efcbd-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="efcbd-649">1. pārdošanas pasūtījuma rinda:</span><span class="sxs-lookup"><span data-stu-id="efcbd-649">Sales order line 1:</span></span>

        - <span data-ttu-id="efcbd-650">**Krājuma numurs:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="efcbd-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="efcbd-651">**Daudzums:** *9024*</span><span class="sxs-lookup"><span data-stu-id="efcbd-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="efcbd-652">**Vienība:** *katra* (9024 ea = 376 Box = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="efcbd-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="efcbd-653">2. pārdošanas pasūtījuma rinda:</span><span class="sxs-lookup"><span data-stu-id="efcbd-653">Sales order line 2:</span></span>

        - <span data-ttu-id="efcbd-654">**Krājuma numurs:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="efcbd-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="efcbd-655">**Daudzums:** *9016*</span><span class="sxs-lookup"><span data-stu-id="efcbd-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="efcbd-656">**Vienība:** *katra* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="efcbd-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="efcbd-657">Šeit sniegtie krājumi un daudzumi ir tikai piemēri.</span><span class="sxs-lookup"><span data-stu-id="efcbd-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="efcbd-658">Tie izmantos vienības secību grupu, ko definējāt iepriekš, tāpēc tiem ir jādefinē piemērota vienību pārveidošana no *ea* uz *Box* uz *PL* un krājumiem ir jābūt *62* noliktavā.</span><span class="sxs-lookup"><span data-stu-id="efcbd-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="efcbd-659">Papildinformāciju skatiet sadaļā [Mērvienību un krājumu politikas](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="efcbd-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="efcbd-660">Atlasiet 1. pārdošanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-660">Select sales order line 1.</span></span> <span data-ttu-id="efcbd-661">Pēc tam sadaļas **Pārdošanas pasūtījuma rinda** izvēlnē **Krājumi** atlasiet **Rezervācijas**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="efcbd-662">Lapas **Rezervācija** darbību rūtī atlasiet **Rezervēt laidienu**, un pēc tam aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="efcbd-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="efcbd-663">Atkārtojiet 4. un 5. soli pārdošanas pasūtījuma 2. rindai.</span><span class="sxs-lookup"><span data-stu-id="efcbd-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="efcbd-664">Cilnē **Noliktava**, kas atrodas darbību rūtī, atlasiet **Nodot izpildei noliktavā**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="efcbd-665">Notiek tālāk aprakstītie notikumi:</span><span class="sxs-lookup"><span data-stu-id="efcbd-665">The following events occur:</span></span> 

    - <span data-ttu-id="efcbd-666">Sistēma apstrādā izveidoto sūtījumu, izmantojot veidni, kas ietver etiķetes drukāšanas darbību.</span><span class="sxs-lookup"><span data-stu-id="efcbd-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="efcbd-667">Etiķetes izkārtojums tiks izmantots etiķetes formāta definēšanai un rezultāts būs etiķete, kas tiek drukāta uz printera, kas ir atlasīts etiķetes veidnē.</span><span class="sxs-lookup"><span data-stu-id="efcbd-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="efcbd-668">Kopuma etiķetes tiek ģenerētas un izdrukātas.</span><span class="sxs-lookup"><span data-stu-id="efcbd-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="efcbd-669">Etiķešu skaits būs vienāds ar kastu skaitu (šajā piemērā 376 kastu etiķetes 1. rindai un 322 kastu etiķetes 2. rindai, 47 PL etiķetes 1. rindai, 47 PL etiķetes 2. rindai un divas pārtraukuma etiķetes ar sūtījuma ID).</span><span class="sxs-lookup"><span data-stu-id="efcbd-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="efcbd-670">Sūtījumiem tiek ģenerēts jauns preču transporta pavadzīmes ID.</span><span class="sxs-lookup"><span data-stu-id="efcbd-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="efcbd-671">Ja konfigurējāt numuru sērijas paplašinājumus, kopuma etiķešu ID sekos **SSCC-18** numura formātam.</span><span class="sxs-lookup"><span data-stu-id="efcbd-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="efcbd-672">Varat skatīt un atkārtoti drukāt kopuma etiķetes no šādām lapām:</span><span class="sxs-lookup"><span data-stu-id="efcbd-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="efcbd-673">Visi sūtījumi \> Sūtījuma informācija</span><span class="sxs-lookup"><span data-stu-id="efcbd-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="efcbd-674">Visas kravas \> Kravas informācija</span><span class="sxs-lookup"><span data-stu-id="efcbd-674">All loads \> Load details</span></span>
- <span data-ttu-id="efcbd-675">Visi kopumi</span><span class="sxs-lookup"><span data-stu-id="efcbd-675">All waves</span></span>
- <span data-ttu-id="efcbd-676">Kopuma etiķetes</span><span class="sxs-lookup"><span data-stu-id="efcbd-676">Wave labels</span></span>
- <span data-ttu-id="efcbd-677">Kopuma etiķešu vēsture</span><span class="sxs-lookup"><span data-stu-id="efcbd-677">Wave label history</span></span>

<span data-ttu-id="efcbd-678">Vairumam šo lapu varat atrast atbilstošo funkciju darbību rūts cilnē **Sūtījumi** grupā **Saistītā informācija**, atlasot **Kopuma etiķetes**.</span><span class="sxs-lookup"><span data-stu-id="efcbd-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
