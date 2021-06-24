---
title: Lietojuma pārvaldības informācijas panelis
description: Šajā tēmā skaidrots, kā izmantot lietojuma pārvaldības informācijas paneli, lai pārraudzītu elektronisko rēķinu izrakstīšanas pakalpojuma lietošanu un saglabātu to atbilstību.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130510"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="01b80-103">Lietojuma pārvaldības informācijas panelis</span><span class="sxs-lookup"><span data-stu-id="01b80-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01b80-104">**Lietojuma pārvaldības** informācijas panelis palīdz pārraudzīt elektronisko rēķinu izrakstīšanas pakalpojuma lietošanu un tādēļ palīdz uzņēmumam saglabāt atbilstību attiecībā uz tā ikmēneša lietojumu.</span><span class="sxs-lookup"><span data-stu-id="01b80-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="01b80-105">Atbilstību nosaka, aprēķinot iesniegšanas apjomu un salīdzinot to ar iesniegšanas iegādāto apjomu, lai identificētu jebkādas iegādātā apjoma un izmantotā apjoma novirzes.</span><span class="sxs-lookup"><span data-stu-id="01b80-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="01b80-106">Informācijas panelis ietver šādus indikatorus:</span><span class="sxs-lookup"><span data-stu-id="01b80-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="01b80-107">Viens izmaksu indikators, ko var izmantot, lai pārraudzītu patēriņu licencēšanas atbilstības nolūkiem:</span><span class="sxs-lookup"><span data-stu-id="01b80-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="01b80-108">Lietojums mēnesī (eksports)</span><span class="sxs-lookup"><span data-stu-id="01b80-108">Usage per month (export)</span></span>

- <span data-ttu-id="01b80-109">Trīs darbību indikatori, ko var izmantot elektronisko rēķinu izrakstīšanas pakalpojuma lietošanas pārvaldības nolūkiem:</span><span class="sxs-lookup"><span data-stu-id="01b80-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="01b80-110">Lietojums pēc līdzekļa</span><span class="sxs-lookup"><span data-stu-id="01b80-110">Usage by feature</span></span>
    - <span data-ttu-id="01b80-111">Lietojums pēc vides</span><span class="sxs-lookup"><span data-stu-id="01b80-111">Usage by environment</span></span>
    - <span data-ttu-id="01b80-112">Lietojums mēnesī (imports)</span><span class="sxs-lookup"><span data-stu-id="01b80-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="01b80-113">Mērījuma tvērums</span><span class="sxs-lookup"><span data-stu-id="01b80-113">Measurement scope</span></span>

- <span data-ttu-id="01b80-114">Mērvienība:</span><span class="sxs-lookup"><span data-stu-id="01b80-114">Unit of measure:</span></span> 

    <span data-ttu-id="01b80-115">**Lietojuma pārvaldības** informācijas panelis uzskaita biznesa dokumentu un importēto elektronisko rēķinu iesniegšanu.</span><span class="sxs-lookup"><span data-stu-id="01b80-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="01b80-116">Organizācija:</span><span class="sxs-lookup"><span data-stu-id="01b80-116">Organization:</span></span> 

    <span data-ttu-id="01b80-117">Uzskaite tiek summēta ar jūsu uzņēmuma nomnieka ID neatkarīgi no Microsoft Dynamics 365 Finance vai Dynamics 365 Supply Chain Management instanču skaita vai juridisko personu skaita, kur elektronisko rēķinu izrakstīšanas pakalpojums ir iespējots.</span><span class="sxs-lookup"><span data-stu-id="01b80-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="01b80-118">Indikators: lietojums mēnesī (eksports)</span><span class="sxs-lookup"><span data-stu-id="01b80-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="01b80-119">Šis indikators sniedz detalizētu informāciju par elektroniskajiem rēķiniem, ko jūsu uzņēmums izsniedz noteiktā periodā.</span><span class="sxs-lookup"><span data-stu-id="01b80-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="01b80-120">Sfēra</span><span class="sxs-lookup"><span data-stu-id="01b80-120">Scope</span></span>
- <span data-ttu-id="01b80-121">Biznesa dokumentu skaits, kas ir iesniegti no programmas Finance un Supply Chain Management elektronisko rēķinu izrakstīšanas pakalpojumam, neatkarīgi no rindu skaita, ko šie biznesa dokumenti ietver.</span><span class="sxs-lookup"><span data-stu-id="01b80-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="01b80-122">Elektronisko rēķinu izrakstīšanas pakalpojumā iesniegto veiksmīgi apstrādāto biznesa dokumentu skaits.</span><span class="sxs-lookup"><span data-stu-id="01b80-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="01b80-123">Dokuments tiek uzskatīts par veiksmīgi apstrādātu, kad tiek pabeigta līdzekļu iestatījumā definēto darbību plūsma.</span><span class="sxs-lookup"><span data-stu-id="01b80-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="01b80-124">Kad elektroniskais rēķins tiek iesniegts ārējam tīmekļa pakalpojumam, uzskaite nav atkarīga no tīmekļa pakalpojumu apstrādes rezultātiem (pieņemts, noraidīts vai shēmas validācijas kļūda).</span><span class="sxs-lookup"><span data-stu-id="01b80-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="01b80-125">Ja tīmekļa pakalpojums saņēmis un atbildējis uz pieprasījumu no elektronisko rēķinu izrakstīšanas pakalpojuma, tad iesniegšana tiek uzskatīta par derīgu uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="01b80-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="01b80-126">**Izņēmums.** Biznesa dokumenti netiek uzskaitīti, ja tie no Finance un Supply Chain Management tiek atkārtoti iesniegti elektronisko rēķinu izrakstīšanas pakalpojumam, piemēram, scenārijos, kuros nepieciešams atkārtoti iesniegt vienu un to pašu biznesa dokumentu, lai mainītu elektroniskā rēķina statusu.</span><span class="sxs-lookup"><span data-stu-id="01b80-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="01b80-127">Piemēram, Brazīlijas elektroniskā rēķina (finanšu dokumenta) izsniegšana tiek uzskaitīta kā derīga, bet nav uzskaitīts atcelšanas pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="01b80-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="01b80-128">Aprēķins</span><span class="sxs-lookup"><span data-stu-id="01b80-128">Calculation</span></span>

<span data-ttu-id="01b80-129">Bilances aprēķins tiek aprēķināts šādi:</span><span class="sxs-lookup"><span data-stu-id="01b80-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="01b80-130">Bilance = Bezmaksas + Nopirkts – Izmantots</span><span class="sxs-lookup"><span data-stu-id="01b80-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="01b80-131">Kur:</span><span class="sxs-lookup"><span data-stu-id="01b80-131">Where:</span></span>

- <span data-ttu-id="01b80-132">Bezmaksas:</span><span class="sxs-lookup"><span data-stu-id="01b80-132">Free:</span></span>
  
    <span data-ttu-id="01b80-133">Biznesa dokumentu bezmaksas apjoms, ko debitors var iesniegt katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="01b80-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="01b80-134">Tajā ir ietverta pakete ar 100 biznesa dokumentiem, ko var iesniegt elektronisko rēķinu izrakstīšanas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="01b80-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="01b80-135">Bezmaksas apjoms nav kumulatīvs, un neviena atlikusī bilance netiek pārnesta uz nākamo periodu.</span><span class="sxs-lookup"><span data-stu-id="01b80-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="01b80-136">Nopirkts:</span><span class="sxs-lookup"><span data-stu-id="01b80-136">Purchased:</span></span>
  
    <span data-ttu-id="01b80-137">Pakete ar 1 000 biznesa dokumentiem, ko var iesniegt elektronisko rēķinu izrakstīšanas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="01b80-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="01b80-138">Šī pakete jūsu uzņēmumam ir jāiegādājas katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="01b80-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="01b80-139">Nopirktais apjoms nav kumulatīvs, un neviena atlikusī bilance netiek pārnesta uz nākamo periodu.</span><span class="sxs-lookup"><span data-stu-id="01b80-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="01b80-140">Izmantots:</span><span class="sxs-lookup"><span data-stu-id="01b80-140">Used:</span></span> 

    <span data-ttu-id="01b80-141">Biznesa dokumentu iesniegumu skaits elektroniskajā rēķinu izrakstīšanas pakalpojumā atbilstoši noteiktiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="01b80-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="01b80-142">Ja jūsu uzņēmums plāno pārsniegt 100 bezmaksas iesniegumu ikmēneša apjomu, iegādājieties maksimālo apjomu, lai nodrošinātu atbilstību Microsoft licencēšanas politikai attiecībā uz elektronisko rēķinu izrakstīšanas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="01b80-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="01b80-143">Pašlaik nopirktais apjoms ir jāievada manuāli atbilstoši iegādes datumam kā vairākas paketes ar 1000 iesniegumiem.</span><span class="sxs-lookup"><span data-stu-id="01b80-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="01b80-144">Indikators: lietojums pēc līdzekļa</span><span class="sxs-lookup"><span data-stu-id="01b80-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="01b80-145">Šis indikators rāda elektroniskā rēķina izrakstīšanas līdzekļa izmantošanu elektronisko rēķinu izsniegšanai noteiktā periodā.</span><span class="sxs-lookup"><span data-stu-id="01b80-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="01b80-146">Aprēķins:</span><span class="sxs-lookup"><span data-stu-id="01b80-146">Calculation:</span></span>
  
    <span data-ttu-id="01b80-147">Izmantots = skaits, cik reizes tika izmantots katrs elektronisko rēķinu izrakstīšanas līdzeklis, iesniedzot biznesa dokumentus elektronisko rēķinu izrakstīšanas pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="01b80-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="01b80-148">Indikators: lietojums pēc vides</span><span class="sxs-lookup"><span data-stu-id="01b80-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="01b80-149">Šis indikators rāda elektronisko rēķinu izrakstīšanas pakalpojumu vides izmantošanu noteiktā periodā.</span><span class="sxs-lookup"><span data-stu-id="01b80-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="01b80-150">Aprēķins:</span><span class="sxs-lookup"><span data-stu-id="01b80-150">Calculation:</span></span>
    
    <span data-ttu-id="01b80-151">Izmantots = skaits, cik reizes tika izmantota katra elektronisko rēķinu izrakstīšanas pakalpojuma vide, iesniedzot biznesa dokumentus elektronisko rēķinu izrakstīšanas pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="01b80-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="01b80-152">Indikators: lietojums mēnesī (imports)</span><span class="sxs-lookup"><span data-stu-id="01b80-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="01b80-153">Šis indikators rāda elektronisko rēķinu importēšanas apjomu programmā Finance un Supply Chain Management noteiktā periodā, izmantojot elektronisko rēķinu izrakstīšanas pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="01b80-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="01b80-154">Tvērums:</span><span class="sxs-lookup"><span data-stu-id="01b80-154">Scope:</span></span>

    <span data-ttu-id="01b80-155">Elektroniskie rēķini, kas importēti programmā Finance un Supply Chain Management, neņemot vērā rindu skaitu, ko ietver šie elektroniskie rēķini.</span><span class="sxs-lookup"><span data-stu-id="01b80-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="01b80-156">Aprēķins:</span><span class="sxs-lookup"><span data-stu-id="01b80-156">Calculation:</span></span>

    <span data-ttu-id="01b80-157">Saņemts = importēto elektronisko rēķinu skaits programmā Finance un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="01b80-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="01b80-158">Funkcijas</span><span class="sxs-lookup"><span data-stu-id="01b80-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="01b80-159">Pirkšana</span><span class="sxs-lookup"><span data-stu-id="01b80-159">Purchase</span></span>

<span data-ttu-id="01b80-160">Cilnē **Lietojums mēnesī (eksports)** atlasiet **Pirkums**, lai manuāli reģistrētu iegādāto iesniegumu summu.</span><span class="sxs-lookup"><span data-stu-id="01b80-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="01b80-161">Norādītajam datumam atlasiet **Jauns** un ievadiet šaja datumā iegādāto **Pakešu** skaitu.</span><span class="sxs-lookup"><span data-stu-id="01b80-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="01b80-162">**Daudzumu** aprēķina šādi:</span><span class="sxs-lookup"><span data-stu-id="01b80-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="01b80-163">Daudzums = Paketes \* 1,000</span><span class="sxs-lookup"><span data-stu-id="01b80-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="01b80-164">Aprēķinātais **Daudzums** tiek atainots dialoglodziņā **Pirkums** no indikatora **Lietojums mēnesī (eksports)**.</span><span class="sxs-lookup"><span data-stu-id="01b80-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="01b80-165">Grāmatot</span><span class="sxs-lookup"><span data-stu-id="01b80-165">Update</span></span>

<span data-ttu-id="01b80-166">Darbību rūtī atlasiet **Atjaunināt**, lai atsvaidzinātu aprēķinu un atjauninātu lapā un diagrammā parādītos datus.</span><span class="sxs-lookup"><span data-stu-id="01b80-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="01b80-167">Atiestatīt vēstures datus</span><span class="sxs-lookup"><span data-stu-id="01b80-167">Reset history data</span></span>

<span data-ttu-id="01b80-168">Darbību rūtī atlasiet **Atiestatīt vēstures datus**, lai atsvaidzinātu datu bāzi, no kuras tiek aprēķināti indikatori.</span><span class="sxs-lookup"><span data-stu-id="01b80-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="01b80-169">**Lietojuma pārvaldības** informācijas panelī netiek rādītas naudas summas.</span><span class="sxs-lookup"><span data-stu-id="01b80-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="01b80-170">Tā vietā tiek parādītas tikai uzskaitītās iesniegšanas un importēto dokumentu apjoms.</span><span class="sxs-lookup"><span data-stu-id="01b80-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
