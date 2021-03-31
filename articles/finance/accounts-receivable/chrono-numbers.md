---
title: Dokumentu un kvīšu hronoloģiska numerācija
description: Šajā tēmā skaidrots, kā iestatīt un izmantot hronoloģiskus numurus piemērojamiem dokumentiem un saistītajām kvītīm.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 31745632de7339d167ac9f18f02e6611e1a78b28
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104412"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="30753-103">Dokumentu un kvīšu hronoloģiska numerācija</span><span class="sxs-lookup"><span data-stu-id="30753-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="30753-104">Dažās valstīs pastāv juridiska prasība numurēt dokumentus un saistītās kvītis hronoloģiskā secībā.</span><span class="sxs-lookup"><span data-stu-id="30753-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="30753-105">Hronoloģija ir jāatbalsta ar periodiem.</span><span class="sxs-lookup"><span data-stu-id="30753-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="30753-106">Visiem skaitļiem, kas attiecas uz agrākiem periodiem, jābūt mazākiem par skaitļiem, kas pieder vēlākiem periodiem.</span><span class="sxs-lookup"><span data-stu-id="30753-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="30753-107">Lai atbilstu šai prasībai, ir ieviesta hronoloģiska numerācijas funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="30753-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="30753-108">Šajā tēmā skaidrots, kā konfigurēt un izmantot hronoloģiskus numurus piemērojamiem dokumentiem un saistītajām kvītīm.</span><span class="sxs-lookup"><span data-stu-id="30753-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="30753-109">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="30753-109">Prerequisites</span></span>

<span data-ttu-id="30753-110">Līdzekļu pārvaldības darbvietā aktivizējiet **Hronoloģiskās numerācijas** līdzekli.</span><span class="sxs-lookup"><span data-stu-id="30753-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="30753-111">Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="30753-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="30753-112">Konfigurēt hronoloģisku numerāciju</span><span class="sxs-lookup"><span data-stu-id="30753-112">Configure chronological numbering</span></span>

<span data-ttu-id="30753-113">Hronoloģiska numerācija ietekmē tālāk norādītos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="30753-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="30753-114">**Debitori**</span><span class="sxs-lookup"><span data-stu-id="30753-114">**Accounts receivable**</span></span>
- <span data-ttu-id="30753-115">Rēķins debitoram</span><span class="sxs-lookup"><span data-stu-id="30753-115">Customer invoice</span></span>
- <span data-ttu-id="30753-116">Debitora rēķina dokuments</span><span class="sxs-lookup"><span data-stu-id="30753-116">Customer invoice voucher</span></span>
- <span data-ttu-id="30753-117">Pārdošanas kredīta nota</span><span class="sxs-lookup"><span data-stu-id="30753-117">Sales credit note</span></span>
- <span data-ttu-id="30753-118">Pārdošanas kredīta notas dokuments</span><span class="sxs-lookup"><span data-stu-id="30753-118">Sales credit note voucher</span></span>
- <span data-ttu-id="30753-119">Brīva teksta rēķins</span><span class="sxs-lookup"><span data-stu-id="30753-119">Free text invoice</span></span>
- <span data-ttu-id="30753-120">Rēķina dokuments brīvā tekstā</span><span class="sxs-lookup"><span data-stu-id="30753-120">Free text invoice voucher</span></span>
- <span data-ttu-id="30753-121">Brīva teksta kredīta nota</span><span class="sxs-lookup"><span data-stu-id="30753-121">Free text credit note</span></span>
- <span data-ttu-id="30753-122">Kredīta notas dokuments brīvā tekstā</span><span class="sxs-lookup"><span data-stu-id="30753-122">Free text credit note voucher</span></span>
- <span data-ttu-id="30753-123">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="30753-123">Packing slip</span></span>
- <span data-ttu-id="30753-124">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="30753-124">Packing slip voucher</span></span>
- <span data-ttu-id="30753-125">Pavadzīmes storno dokuments</span><span class="sxs-lookup"><span data-stu-id="30753-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="30753-126">Procentu paziņojums</span><span class="sxs-lookup"><span data-stu-id="30753-126">Interest note voucher</span></span>
- <span data-ttu-id="30753-127">Atgādinājuma vēstule</span><span class="sxs-lookup"><span data-stu-id="30753-127">Collection letter voucher</span></span>

<span data-ttu-id="30753-128">**Kreditori**</span><span class="sxs-lookup"><span data-stu-id="30753-128">**Accounts payable**</span></span>
- <span data-ttu-id="30753-129">Rēķinu dokuments</span><span class="sxs-lookup"><span data-stu-id="30753-129">Invoice voucher</span></span>
- <span data-ttu-id="30753-130">Kredīta nota</span><span class="sxs-lookup"><span data-stu-id="30753-130">Credit note voucher</span></span>
- <span data-ttu-id="30753-131">Produktu ieejas plūsmas dokuments</span><span class="sxs-lookup"><span data-stu-id="30753-131">Product receipt voucher</span></span>

<span data-ttu-id="30753-132">**Projektu pārvaldība**</span><span class="sxs-lookup"><span data-stu-id="30753-132">**Project management**</span></span>
- <span data-ttu-id="30753-133">Rēķins</span><span class="sxs-lookup"><span data-stu-id="30753-133">Invoice</span></span>
- <span data-ttu-id="30753-134">Rēķinu dokuments</span><span class="sxs-lookup"><span data-stu-id="30753-134">Invoice voucher</span></span>
- <span data-ttu-id="30753-135">Kredīta piezīme</span><span class="sxs-lookup"><span data-stu-id="30753-135">Credit note</span></span>
- <span data-ttu-id="30753-136">Kredīta nota</span><span class="sxs-lookup"><span data-stu-id="30753-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="30753-137">Numuru secību definēšana</span><span class="sxs-lookup"><span data-stu-id="30753-137">Define number sequences</span></span>

<span data-ttu-id="30753-138">Lai definētu numuru secības, dodieties uz **Organizācijas administrēšana** > **Numuru secības** > **Numuru secības**.</span><span class="sxs-lookup"><span data-stu-id="30753-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="30753-139">Varat definēt tik daudz numuru secības, cik nepieciešams, lai segtu ietekmētos periodus nepieciešamajiem dokumentiem.</span><span class="sxs-lookup"><span data-stu-id="30753-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="30753-140">Norādiet uzņēmumu katrai numuru secībai.</span><span class="sxs-lookup"><span data-stu-id="30753-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="30753-141">Numuru secību segmentiem jābūt definētiem tā, lai tie periodiem nodrošinātu hronoloģiski secību.</span><span class="sxs-lookup"><span data-stu-id="30753-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="30753-142">Piemēram, segmentu nosaukumi var ietvert īpašu prefiksu, kas identificē noteiktu periodu.</span><span class="sxs-lookup"><span data-stu-id="30753-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Numuru secību iestatīšana](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="30753-144">Konfigurēt numuru secību grupas</span><span class="sxs-lookup"><span data-stu-id="30753-144">Configure number sequence groups</span></span>

<span data-ttu-id="30753-145">Lai konfigurētu numuru secību grupas, dodieties uz **Debitori** > **Iestatīšana** > **Debitoru parametri**.</span><span class="sxs-lookup"><span data-stu-id="30753-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="30753-146">Cilnē **Numuru secības** definējiet tik daudz numuru secību grupu, cik nepieciešams, lai ietvertu ietekmētos periodus.</span><span class="sxs-lookup"><span data-stu-id="30753-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="30753-147">Katrai grupai sadaļā **Atsauce** atlasiet vienu no atbalstītajām dokumenta atsaucēm un **Numuru secības koda** laukā skatiet numuru secību, kas iepriekš izveidota saistītajam periodam.</span><span class="sxs-lookup"><span data-stu-id="30753-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Numuru sēriju grupas iestatījumi](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="30753-149">Līdzīgi konfigurējiet numuru secību grupas moduļos **Kreditori** un **Projektu pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="30753-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="30753-150">Konfigurēt numuru secību grupu hronoloģiju</span><span class="sxs-lookup"><span data-stu-id="30753-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="30753-151">Lai konfigurētu numuru secību grupu hronoloģiju, dodieties uz **Organizācijas administrēšana** > **Numuru secības** > **Hronoloģiskas numuru secību grupas**.</span><span class="sxs-lookup"><span data-stu-id="30753-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="30753-152">Definējiet numuru secību grupu piemērojamības nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="30753-152">Define the applicability conditions for number sequence groups.</span></span>

![Hronoloģiska numuru iestatīšana](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="30753-154">Lauks</span><span class="sxs-lookup"><span data-stu-id="30753-154">Field</span></span>            | <span data-ttu-id="30753-155">Apraksts</span><span class="sxs-lookup"><span data-stu-id="30753-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30753-156">Ir spēkā</span><span class="sxs-lookup"><span data-stu-id="30753-156">Effective</span></span>  | <span data-ttu-id="30753-157">Numuru secību grupas piemērojamības sākuma datums.</span><span class="sxs-lookup"><span data-stu-id="30753-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="30753-158">Termiņa beigas</span><span class="sxs-lookup"><span data-stu-id="30753-158">Expiration</span></span>      | <span data-ttu-id="30753-159">Numuru secību grupas piemērojamības beigu datums.</span><span class="sxs-lookup"><span data-stu-id="30753-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="30753-160">Ja netiek lietots beigu datums, atlasiet **Nekad**.</span><span class="sxs-lookup"><span data-stu-id="30753-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="30753-161">Numuru sēriju grupa</span><span class="sxs-lookup"><span data-stu-id="30753-161">Number sequence group</span></span> | <span data-ttu-id="30753-162">Numuru secību grupa, kas tiks izmantota dokumentu numuru ģenerēšanai periodā.</span><span class="sxs-lookup"><span data-stu-id="30753-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="30753-163">Oriģinālā numuru secību grupa</span><span class="sxs-lookup"><span data-stu-id="30753-163">Original number sequence group</span></span> | <span data-ttu-id="30753-164">Šis numuru secības grupas kods tiek izmantots papildu filtrēšanai gadījumos, kad dokumentiem jau ir piešķirta noteikta *pastāvīga* numuru secību grupa.</span><span class="sxs-lookup"><span data-stu-id="30753-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="30753-165">Tukša vērtība tiek uzskatīta par noteiktu vērtību.</span><span class="sxs-lookup"><span data-stu-id="30753-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="30753-166">Ja ir jāignorē iepriekšējā piešķirtā grupa, šim iestatījumam izmantojiet opciju **Noklusējuma**.</span><span class="sxs-lookup"><span data-stu-id="30753-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="30753-167">Noklusētā vērtība</span><span class="sxs-lookup"><span data-stu-id="30753-167">Default</span></span> | <span data-ttu-id="30753-168">Ja ieslēgts, sistēma ignorē iepriekšējo piešķirto dokumenta numuru secību grupu un piemērojamības analīzei izmanto tikai periodu sākuma un beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="30753-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="30753-169">Ja izslēgts, atlasei sistēma izmanto pilnu kombināciju **Stājies spēkā** + **Derīguma termiņš** + **Sākotnējā numuru secību grupa**.</span><span class="sxs-lookup"><span data-stu-id="30753-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="30753-170">Dokumentu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="30753-170">Document posting</span></span>
<span data-ttu-id="30753-171">Grāmatojot dokumentu, dokumentam tiek piešķirta atbilstoša numuru secību grupa, pamatojoties uz dokumenta grāmatošanas datumu, un pēc tam izmantota, lai ģenerētu dokumenta numuru, kas balstīts uz konstatēto numuru secību.</span><span class="sxs-lookup"><span data-stu-id="30753-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="30753-172">Sistēma sniedz ziņojumu par numuru secību grupas piešķiri.</span><span class="sxs-lookup"><span data-stu-id="30753-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Dokumenta numurs](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="30753-174">Dažām valstīm jau ir noteikta loģika dokumentu numerācijai.</span><span class="sxs-lookup"><span data-stu-id="30753-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="30753-175">Šajā gadījumā valstij noteiktā loģika pārrakstīs **Hronoloģiskās numerācijas** funkciju.</span><span class="sxs-lookup"><span data-stu-id="30753-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>