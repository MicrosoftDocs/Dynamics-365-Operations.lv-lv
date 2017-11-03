---
title: Intrastat
description: "Šajā rakstā ir sniegta informācija par Intrastat atskaišu veidošanu preču — un noteiktos gadījumos arī pakalpojumu — tirdzniecībai starp dažādām Eiropas Savienības (ES) valstīm/reģioniem. Tajā ir sniegts pārskats par atskaišu veidošanas procesu, kā arī aprakstīti nepieciešamie iestatījumi un priekšnosacījumi."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7c713f3a1cb5aa4758a72a7cc42c73c57b602219
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="intrastat"></a><span data-ttu-id="947c7-104">Intrastat</span><span class="sxs-lookup"><span data-stu-id="947c7-104">Intrastat</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="947c7-105">Šajā rakstā ir sniegta informācija par Intrastat atskaišu veidošanu preču — un noteiktos gadījumos arī pakalpojumu — tirdzniecībai starp dažādām Eiropas Savienības (ES) valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="947c7-105">This article provides information about Intrastat reporting for the trade of goods and, in some cases, services among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="947c7-106">Tajā ir sniegts pārskats par atskaišu veidošanas procesu, kā arī aprakstīti nepieciešamie iestatījumi un priekšnosacījumi.</span><span class="sxs-lookup"><span data-stu-id="947c7-106">It provides an overview of the reporting process, and describes the required settings and prerequisites.</span></span>

<span data-ttu-id="947c7-107">Intrastat ir sistēma informācijas vākšanai un statistikas ģenerēšanai par preču tirdzniecību starp dažādām Eiropas Savienības (ES) valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="947c7-107">Intrastat is the system for collecting information and generating statistics about the trade of goods among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="947c7-108">Intrastat atskaites ir nepieciešamas vienmēr, kad prece šķērso citas ES valsts/reģiona robežu.</span><span class="sxs-lookup"><span data-stu-id="947c7-108">Intrastat reporting is required whenever a product crosses the border of another EU country/region.</span></span> <span data-ttu-id="947c7-109">Vairākās valstīs/reģionos Intrastat atskaites attiecas arī uz pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="947c7-109">In several countries/regions, Intrastat reporting also applies to services.</span></span> <span data-ttu-id="947c7-110">Intrastat atskaitēs var vākt obligātus un neobligātus elementus.</span><span class="sxs-lookup"><span data-stu-id="947c7-110">Mandatory and optional elements can be collected in Intrastat reporting.</span></span> <span data-ttu-id="947c7-111">Obligāti ir šādi elementi: tās puses pievienotās vērtības nodokļa (PVN) numurs, kas ir atbildīga par informācijas sniegšanu, atsauces periods, plūsma (saņemšana vai nosūtīšana), astoņu ciparu preču kods, partnera dalībvalsts (saņemamo preču nosūtīšanas dalībvalsts un nosūtāmo preču saņemšanas dalībvalsts), preču vērtība, preču daudzums (neto masa un papildu vienības) un transakcijas veids.</span><span class="sxs-lookup"><span data-stu-id="947c7-111">The following elements are mandatory: the value-added tax (VAT) number of the party that is responsible for providing information, the reference period, the flow (arrival or dispatch), the eight-digit commodity code, the partner member state (member state of consignment on arrivals and member state of destination on dispatches), the value of the goods, the quantity of the goods (net mass and supplementary unit), and the nature of the transaction.</span></span> <span data-ttu-id="947c7-112">Valstis/reģioni saskaņā ar dažādiem nosacījumiem var vākt arī neobligātus elementus.</span><span class="sxs-lookup"><span data-stu-id="947c7-112">Countries/regions can also collect optional elements under various conditions.</span></span> <span data-ttu-id="947c7-113">Daži no neobligātajiem elementiem ir izcelsmes valsts/reģions, piegādes nosacījumi, transportēšanas veids un detalizētāks preču kods nekā CN8, nosūtāmo preču izcelsmes reģions un saņemamo preču mērķa reģions, statistiskā procedūra, statistiskā vērtība, preču apraksts un iekraušanas/izkraušanas osta/lidosta.</span><span class="sxs-lookup"><span data-stu-id="947c7-113">Some optional elements are the country/region of origin, the delivery terms, the mode of transport, a more detailed commodity code than CN8, the region of origin on dispatches and the region of destination on arrivals, the statistical procedure, the statistical value, a description of the goods, and the port/airport of loading/unloading.</span></span>

## <a name="overview-of-the-intrastat-reporting-process"></a><span data-ttu-id="947c7-114">Intrastat atskaišu veidošanas procesa apskats</span><span class="sxs-lookup"><span data-stu-id="947c7-114">Overview of the Intrastat reporting process</span></span>
<span data-ttu-id="947c7-115">Nākamajās sadaļās ir aprakstīta vispārējā informācijas plūsma, kas tiek izmantota Intrastat atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="947c7-115">The following sections describe the overall flow of information that is used for Intrastat reporting.</span></span>

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a><span data-ttu-id="947c7-116">1. Ievadiet transakciju, kas šķērso citas ES valsts/reģiona robežu</span><span class="sxs-lookup"><span data-stu-id="947c7-116">1. Enter a transaction that crosses the border of another EU country/region</span></span>

<span data-ttu-id="947c7-117">Debitora rēķins, brīva teksta rēķins, pirkšanas rēķins, projekta rēķins, debitora pavadzīme, kreditora produktu ieejas plūsma vai pārsūtīšanas pasūtījums tiek pārsūtīti uz Intrastat žurnālu tikai tad, ja mērķa (nosūtīšanai) vai nosūtīšanas (saņemšanai) valsts/reģiona tips ir **ES**.</span><span class="sxs-lookup"><span data-stu-id="947c7-117">A customer invoice, free text invoice, purchase invoice, project invoice, customer packing slip, vendor product receipt, or transfer order is transferred to the Intrastat journal only if the country/region type of the destination (on dispatches) or consignment (on arrivals) is **EU**.</span></span> <span data-ttu-id="947c7-118">Programmatūrā Microsoft Dynamics 365 for Operations (1611) šis līdzeklis ir paplašināts un sniedz iespēju norādīt EK iekšējo transakciju iekraušanas adreses.</span><span class="sxs-lookup"><span data-stu-id="947c7-118">This feature was extended for Microsoft Dynamics 365 for Operations (1611) and allows you to specify lading addresses for an intra-community transaction.</span></span> <span data-ttu-id="947c7-119">Ja iekraušanas adrese atšķiras no kreditora uzņēmuma adreses (vai ja atšķiras debitora uzņēmuma adrese atgriešanas pasūtījumam), tad Intrastat pārskatu veidošana strādā ar šo informāciju.</span><span class="sxs-lookup"><span data-stu-id="947c7-119">If a lading address differs with a vendor business address (or customer business address for return order) the Intrastat reporting will operate with this information.</span></span> <span data-ttu-id="947c7-120">Kad veidojat kādu pārdošanas pasūtījumu, brīva teksta rēķinu, pirkšanas pasūtījumu, kreditora rēķinu, projekta rēķinu vai pārsūtīšanas pasūtījumu, dažiem laukiem, kas ir saistīti ar ārējo tirdzniecību, dokumenta virsrakstā vai rindā ir noklusējuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="947c7-120">When you create a sales order, free text invoice, purchase order, vendor invoice, project invoice, or transfer order, some fields that are related to foreign trade have default values in the document header or on the line.</span></span> <span data-ttu-id="947c7-121">Noklusējuma transakcijas kods tiek ņemts no atbilstošā lauka lapā **Ārējās tirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="947c7-121">The default transaction code is taken from the corresponding field on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="947c7-122">Noklusējuma preču kods, izcelsmes valsts/reģions un izcelsmes novads tiek ņemti no krājuma.</span><span class="sxs-lookup"><span data-stu-id="947c7-122">The default commodity code, country/region of origin, and state/province of origin are taken from the item.</span></span> <span data-ttu-id="947c7-123">Šīs noklusējuma vērtības varat mainīt, ka arī varat aizpildīt citu ar ārējo tirdzniecību saistīto informāciju: statistisko procedūru, transportēšanas metodi un ostu.</span><span class="sxs-lookup"><span data-stu-id="947c7-123">You can change the default values and can also fill in other foreign trade–related information: the statistics procedure, transport method, and port.</span></span>

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="947c7-124">2. Lietojiet Intrastat žurnālu, lai ģenerētu informāciju par tirdzniecību starp ES valstīm/reģioniem</span><span class="sxs-lookup"><span data-stu-id="947c7-124">2. Use the Intrastat journal to generate information about trade among EU countries/regions</span></span>

<span data-ttu-id="947c7-125">Statistiskiem nolūkiem informāciju par tirdzniecību starp ES valstīm/reģioniem varat ģenerēt katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="947c7-125">For statistical purposes, you generate information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="947c7-126">Transakcijas no brīva teksta rēķina, debitora rēķina, debitora pavadzīmes, kreditora rēķina, kreditora pavadzīmes, projekta rēķina vai pārsūtīšanas pasūtījuma varat pārsūtīt saskaņā ar pārsūtīšanas kritērijiem, kas ir iestatīti lapā **Ārējās tirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="947c7-126">You can transfer transactions from a free text invoice, customer invoice, customer packing slip, vendor invoice, vendor packing slip, project invoice, or transfer order, according to the transfer criteria that are set up on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="947c7-127">Alternatīvi transakcijas varat ievadīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="947c7-127">Alternatively, you can enter transactions manually.</span></span> <span data-ttu-id="947c7-128">Pārsūtītās transakcijas Intrastat žurnālā varat atjaunināt manuāli, ja ir nepieciešami atjauninājumi.</span><span class="sxs-lookup"><span data-stu-id="947c7-128">You can manually update transferred transactions in the Intrastat journal, if any updates are required.</span></span> <span data-ttu-id="947c7-129">Noteiktos apstākļos, kas ir iestatīti lapā **Intrastat arhivēšana**, varat saspiest transakcijas Intrastat žurnālā.</span><span class="sxs-lookup"><span data-stu-id="947c7-129">Under specific conditions that are set up on the **Compression of Intrastat** page, you can compress the transactions in the Intrastat journal.</span></span> <span data-ttu-id="947c7-130">Dažās valstīs/reģionos jums ir ļauts piemērot mazu transakciju slieksni.</span><span class="sxs-lookup"><span data-stu-id="947c7-130">Some countries/regions let you apply a small transaction threshold.</span></span> <span data-ttu-id="947c7-131">Pēc tam par transakcijām, kuras atrodas zem šī sliekšņa, varat ziņot saskaņā ar norādīto preču kodu.</span><span class="sxs-lookup"><span data-stu-id="947c7-131">You can then report transactions that are below that threshold under the specified commodity code.</span></span> <span data-ttu-id="947c7-132">Preču kodu atbilstošajās Intrastat žurnāla rindās varat atjaunināt, pamatojoties uz iestatījumu **Minimālā robeža** lapā **Ārējās tirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="947c7-132">You can update the commodity code on the corresponding Intrastat journal lines, based on the **Minimum limit** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="947c7-133">Šīs transakcijas varat arī saspiest, pamatojoties uz iestatījumu **Intrastat arhivēšana**.</span><span class="sxs-lookup"><span data-stu-id="947c7-133">You can also compress those transactions, based on the **Compression of Intrastat** setting.</span></span> <span data-ttu-id="947c7-134">Intrastat žurnālā iekļauto transakciju pilnību varat pārbaudīt, pamatojoties uz iestatījumu **Pārbaudīt iestatījumu** lapā **Ārējās tirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="947c7-134">You can validate the completeness of the transactions in the Intrastat journal, based on the **Check setup** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="947c7-135">Iespējams, atbilstošajos laukos var pārbaudīt datu pilnību: valsts/reģions, novads, svars, preču kods, transakcijas kods, papildu vienība, osta, izcelsme, piegādes nosacījumi, transportēšanas metode un PVN reģistrācijas numurs.</span><span class="sxs-lookup"><span data-stu-id="947c7-135">The data in corresponding fields might be validated for completeness: country/region, state or province, weight, commodity code, transaction code, additional unit, port, origin, terms of delivery, transport method, and tax exempt number.</span></span> <span data-ttu-id="947c7-136">Transakcijas, kas nav pabeigtas, tiks atzīmētas kā nederīgas.</span><span class="sxs-lookup"><span data-stu-id="947c7-136">Transactions that aren't completed will be marked as not valid.</span></span>

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="947c7-137">3. Lietojiet Intrastat žurnālu, lai ziņotu informāciju par tirdzniecību starp ES valstīm/reģioniem</span><span class="sxs-lookup"><span data-stu-id="947c7-137">3. Use the Intrastat journal to report information about trade among EU countries/regions</span></span>

<span data-ttu-id="947c7-138">Statistiskiem nolūkiem informāciju par tirdzniecību starp ES valstīm/reģioniem varat ziņot katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="947c7-138">For statistical purposes, you report information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="947c7-139">Intrastat atskaiti varat drukāt, pamatojoties uz iestatījumiem **Atskaites formāta kartēšana** lapā **Ārējās tirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="947c7-139">You can print the Intrastat report, based on the **Report format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="947c7-140">Varat arī ģenerēt elektronisku failu, pamatojoties uz iestatījumiem **Faila formāta kartēšana** lapā **Ārējās tirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="947c7-140">You can also generate an electronic file, based on the **File format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="947c7-141">Papildinformāciju par Intrastat pārskatu veidošanu, tostarp nepieciešamajiem priekšnosacījumiem, skatiet Intrastat pārskatu veidošanas uzdevumu ierakstos:</span><span class="sxs-lookup"><span data-stu-id="947c7-141">For more information about Intrastat reporting, including required prerequisites, see the Intrastat reporting task recordings:</span></span>

-   <span data-ttu-id="947c7-142">Ģenerēt ES Intrastat deklarāciju;</span><span class="sxs-lookup"><span data-stu-id="947c7-142">Generate an EU Intrastat declaration,</span></span>
-   <span data-ttu-id="947c7-143">Pārsūtīt transakcijas uz Intrastat;</span><span class="sxs-lookup"><span data-stu-id="947c7-143">Transfer transactions to the Intrastat,</span></span>
-   <span data-ttu-id="947c7-144">EK iekšējo transakciju iekraušanas adreses norādīšana.</span><span class="sxs-lookup"><span data-stu-id="947c7-144">Specifying lading address for an intra-community transaction.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="947c7-145">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="947c7-145">Prerequisites</span></span>
<span data-ttu-id="947c7-146">Nākamajā tabulā ir uzskaitīti priekšnosacījumi Intrastat pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="947c7-146">The following table lists the prerequisites for Intrastat reporting.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="947c7-147">Priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="947c7-147">Prerequisite</span></span></th>
<th><span data-ttu-id="947c7-148">Apraksts</span><span class="sxs-lookup"><span data-stu-id="947c7-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="947c7-149">Adreses iestatīšana</span><span class="sxs-lookup"><span data-stu-id="947c7-149">Address setup</span></span></td>
<td><span data-ttu-id="947c7-150">Iestatiet Starptautiskā Standartizācijas organizācijas (ISO) kodus valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="947c7-150">Set up International Organization for Standardization (ISO) codes for countries/regions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="947c7-151">Juridiska persona</span><span class="sxs-lookup"><span data-stu-id="947c7-151">Legal entity</span></span></td>
<td><span data-ttu-id="947c7-152">Iestatiet PVN reģistrācijas numurus importēšanai/eksportēšanai, filiāles numura paplašinājumu importēšanai/eksportēšanai un Intrastat kodu, kas ir piešķirts juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="947c7-152">Set up tax exempt numbers for import/export, the branch number extension for import/export, and the Intrastat code that is assigned to the legal entity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="947c7-153">Preču kategoriju hierarhija (pārdošanas hierarhija, sagādes hierarhija)</span><span class="sxs-lookup"><span data-stu-id="947c7-153">Product category hierarchy (sales hierarchy, procurement hierarchy)</span></span></td>
<td><span data-ttu-id="947c7-154">Piešķiriet Intrastat preču kodus kategoriju mezgliem cilnē <strong>Preču kodi</strong>, lapā <strong>Kategoriju hierarhija</strong>.</span><span class="sxs-lookup"><span data-stu-id="947c7-154">Assign the Intrastat commodity codes to the category nodes on the <strong>Commodity codes</strong> tab of the <strong>Category hierarchy</strong> page.</span></span> <span data-ttu-id="947c7-155">Kad kādu preču kodu piešķirat pamatkategorijas zaram, šis kods ir attiecināms uz visiem apakškategoriju zariem.</span><span class="sxs-lookup"><span data-stu-id="947c7-155">When you assign a commodity code to a parent category node, that code is applicable to all child category nodes.</span></span> <span data-ttu-id="947c7-156">Atlasītie preču kodi būs pieejami skatā <strong>Atlasīts</strong>, kad atlasāt preču kodu izlaisto preču detalizētajā informācijā, kā arī pārdošanas pasūtījuma, pirkšanas pasūtījuma un pārsūtīšanas pasūtījuma rindās.</span><span class="sxs-lookup"><span data-stu-id="947c7-156">The selected commodity codes will be available in the <strong>Selected</strong> view when you select a commodity code in the released product details, and on sales order, purchase order, and transfer order lines.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="947c7-157">Detalizēta informācija par izlaistajām precēm</span><span class="sxs-lookup"><span data-stu-id="947c7-157">Released product details</span></span></td>
<td><span data-ttu-id="947c7-158">Izlaistajām precēm iestatiet šādus ārējās tirdzniecības datus:</span><span class="sxs-lookup"><span data-stu-id="947c7-158">Set up the following foreign trade data for released products:</span></span>
<ul>
<li><span data-ttu-id="947c7-159"><strong>Preču kods</strong> — atlasiet no atlasīto preču saraksta, kas ir izgūts no piešķirtajām preču kategorijām vai no pilnā Intrastat preču kodu saraksta.</span><span class="sxs-lookup"><span data-stu-id="947c7-159"><strong>Commodity code</strong> – Select from either the list of selected commodities that is retrieved from assigned product categories or the full list of Intrastat commodity codes.</span></span></li>
<li><span data-ttu-id="947c7-160"><strong>Statistiskie maksu procenti</strong></span><span class="sxs-lookup"><span data-stu-id="947c7-160"><strong>Statistical charges percentage</strong></span></span></li>
<li><span data-ttu-id="947c7-161"><strong>Izcelsmes valsts/reģions</strong> — atlasiet noklusējuma valsti/reģionu, kur preces tika pilnībā iegūtas vai saražotas.</span><span class="sxs-lookup"><span data-stu-id="947c7-161"><strong>Country/region of origin</strong> – Select the default country/region where the goods were completely obtained or produced.</span></span></li>
<li><span data-ttu-id="947c7-162"><strong>Izcelsmes/adresāta novads</strong> — saņemamajām precēm atlasiet mērķa noklusējuma novadu un nosūtāmajam precēm atlasiet izcelsmes noklusējuma novadu.</span><span class="sxs-lookup"><span data-stu-id="947c7-162"><strong>State/province of origin/destination</strong> – Select the default state/province of destination for arrivals and the state/province of origin for dispatches.</span></span></li>
<li><span data-ttu-id="947c7-163"><strong>Neto svars (kg)</strong></span><span class="sxs-lookup"><span data-stu-id="947c7-163"><strong>Net weight in kg</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="947c7-164">Debitori</span><span class="sxs-lookup"><span data-stu-id="947c7-164">Customers</span></span></td>
<td><span data-ttu-id="947c7-165">Iestatiet debitora piegādes adresi ES valstī/reģionā.</span><span class="sxs-lookup"><span data-stu-id="947c7-165">Set up the customer delivery address in the EU country/region.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="947c7-166">Kreditori</span><span class="sxs-lookup"><span data-stu-id="947c7-166">Vendors</span></span></td>
<td><span data-ttu-id="947c7-167">Iestatiet kreditora adresi ES valstī/reģionā.</span><span class="sxs-lookup"><span data-stu-id="947c7-167">Set up the vendor address in the EU country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="947c7-168">Papildmaksas</span><span class="sxs-lookup"><span data-stu-id="947c7-168">Miscellaneous charges</span></span></td>
<td><span data-ttu-id="947c7-169">Iestatiet papildmaksu kodu, ko iekļaut rēķina summā, statistiskajā summā vai abās.</span><span class="sxs-lookup"><span data-stu-id="947c7-169">Set up the miscellaneous charges code to include in the invoice amount, the statistical amount, or both.</span></span> <span data-ttu-id="947c7-170">Lapā <strong>Maksu kodi</strong>, cilnē <strong>Ārējā tirdzniecība</strong> iespējojiet opciju <strong>Intrastat rēķina vērtība</strong>, lai maksu summu iekļautu rēķina vērtībā, un iespējojiet opciju <strong>Intrastat statistiska vērtība</strong>, lai šo maksu summu iekļautu statistiskajā vērtībā.</span><span class="sxs-lookup"><span data-stu-id="947c7-170">On the <strong>Charges codes</strong> page, on the <strong>Foreign trade</strong> tab, enable <strong>Intrastat invoice value</strong> to include the charges amount in the invoice value, and enable <strong>Intrastat statistical value</strong> to include the charges amount in the statistical value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="947c7-171">Elektroniskie pārskati</span><span class="sxs-lookup"><span data-stu-id="947c7-171">Electronic reporting</span></span></td>
<td><span data-ttu-id="947c7-172">Iestatiet elektronisko atskaišu konfigurācijas, lai Intrastat datus eksportētu elektroniskā failā, kuram ir tāds formāts, kādu pieprasa attiecīgās iestādes, un lai Intrastat datus priekšskatītu lietotājam draudzīgā, lasāmā formātā (piemēram, programmā Microsoft Excel).</span><span class="sxs-lookup"><span data-stu-id="947c7-172">Set up electronic reporting configurations to export Intrastat data in an electronic file that has the format that is requested by the relevant authorities, and to preview Intrastat data in a user-friendly, readable format (for example, in Microsoft Excel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="947c7-173">Noliktavas</span><span class="sxs-lookup"><span data-stu-id="947c7-173">Warehousing</span></span></td>
<td><span data-ttu-id="947c7-174">Kreditoru kontus saistiet ar noliktavu kodiem, lai aizpildītu PVN reģistrācijas numuru, kad veicat pārsūtīšanas pasūtījuma pārsūtīšanu.</span><span class="sxs-lookup"><span data-stu-id="947c7-174">Associate vendor accounts with warehouse codes for filling tax exempt number when transferring Transfer order.</span></span></td>
</tr>
</tbody>
</table>

## <a name="setup"></a><span data-ttu-id="947c7-175">Iestatījumi</span><span class="sxs-lookup"><span data-stu-id="947c7-175">Setup</span></span>
<span data-ttu-id="947c7-176">Nākamajās sadaļās ir aprakstīti Intrastat atskaitēm nepieciešamie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="947c7-176">The following sections describe the settings that are required for Intrastat reporting.</span></span>

### <a name="set-up-all-required-intrastat-related-lists"></a><span data-ttu-id="947c7-177">Iestatiet visus nepieciešamos ar Intrastat saistītos sarakstus</span><span class="sxs-lookup"><span data-stu-id="947c7-177">Set up all required Intrastat-related lists</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="947c7-178">Saraksts</span><span class="sxs-lookup"><span data-stu-id="947c7-178">List</span></span></th>
<th><span data-ttu-id="947c7-179">Papildinformācija</span><span class="sxs-lookup"><span data-stu-id="947c7-179">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="947c7-180">Preču kodi</span><span class="sxs-lookup"><span data-stu-id="947c7-180">Commodity codes</span></span></td>
<td><span data-ttu-id="947c7-181">Iestatiet kategoriju hierarhiju ar tipu <strong>Preču kods</strong> un ievadiet visus preču kodus saskaņā ar kombinētās nomenklatūru sarakstu.</span><span class="sxs-lookup"><span data-stu-id="947c7-181">Set up a category hierarchy of type <strong>Commodity code</strong>, and enter all commodity codes according to the combined nomenclature list.</span></span> <span data-ttu-id="947c7-182">Katrai precei jūs iestatāt šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="947c7-182">For each commodity, you set up the following information:</span></span>
<ul>
<li><span data-ttu-id="947c7-183">Preces nosaukums un preces kods</span><span class="sxs-lookup"><span data-stu-id="947c7-183">The name of the commodity and the commodity code</span></span></li>
<li><span data-ttu-id="947c7-184">Draudzīgais nosaukums un/vai tulkotais nosaukums</span><span class="sxs-lookup"><span data-stu-id="947c7-184">The friendly name and/or translated name</span></span></li>
<li><span data-ttu-id="947c7-185">Iestatījumi papildu vienību ziņošanai cilnē <strong>Ārējā tirdzniecība</strong>. Šo papildu vienību varat atlasīt vienību sarakstā.</span><span class="sxs-lookup"><span data-stu-id="947c7-185">Settings for reporting additional (supplementary) units on the <strong>Foreign trade</strong> tab. You can select the additional unit in the unit list.</span></span> <span data-ttu-id="947c7-186">Varat arī norādīt, vai preču svars ir jāziņo papildus atlasītajai papildu vienībai.</span><span class="sxs-lookup"><span data-stu-id="947c7-186">You can also specify whether the weight of commodities must be reported in addition to the selected additional unit.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="947c7-187">Darbību kodi</span><span class="sxs-lookup"><span data-stu-id="947c7-187">Transaction codes</span></span></td>
<td><span data-ttu-id="947c7-188">Iestatiet transakcijas veidu saskaņā ar jūsu valsts/reģiona prasībām.</span><span class="sxs-lookup"><span data-stu-id="947c7-188">Set up the nature of the transaction according to your country's/region's requirements.</span></span> <span data-ttu-id="947c7-189">Katram jūsu iestatītajam transakcijas kodam jums ir jāiestata kārtulas rēķinu summu un statistisko summu aprēķināšanai pārsūtīšanas pasūtījumiem un pārdošanas/pirkšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="947c7-189">For each transaction code that you set up, you must set up the rules for calculating invoice amounts and statistical amounts for transfer orders and sales/purchase orders.</span></span>
<ul>
<li><span data-ttu-id="947c7-190">Pārsūtīšanas pasūtījumiem rēķina summu un statistisko summu aprēķināšanai jūs iestatāt vienu no šādām kārtulām:</span><span class="sxs-lookup"><span data-stu-id="947c7-190">For transfer orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="947c7-191"><strong>Tukšs</strong> — summa būs 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="947c7-191"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="947c7-192"><strong>Finanšu izmaksu summa</strong> — summa būs vienāda ar finanšu izmaksām.</span><span class="sxs-lookup"><span data-stu-id="947c7-192"><strong>Financial cost amount</strong> – The amount will be equal to the financial cost.</span></span></li>
<li><span data-ttu-id="947c7-193"><strong>Kopējās izmaksas</strong> — summa būs vienāda ar transakcijas kopējām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="947c7-193"><strong>Total cost</strong> – The amount will be equal to the total cost of the transaction.</span></span></li>
<li><span data-ttu-id="947c7-194"><strong>Manuāls</strong> — summa būs vienāda ar summu, kas ir manuāli norādīta pārsūtīšanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="947c7-194"><strong>Manual</strong> – The amount will be equal to the amount that is manually specified on the transfer order line.</span></span></li>
</ul></li>
<li><span data-ttu-id="947c7-195">Pārdošanas pasūtījumiem un pirkšanas pasūtījumiem rēķina summu un statistisko summu aprēķināšanai jūs iestatāt vienu no šādām kārtulām:</span><span class="sxs-lookup"><span data-stu-id="947c7-195">For sales orders and purchase orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="947c7-196"><strong>Tukšs</strong> — summa būs 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="947c7-196"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="947c7-197"><strong>Rēķina summa</strong> — summa būs vienāda ar summu, kas ir iekļauta rēķinā par šo preci.</span><span class="sxs-lookup"><span data-stu-id="947c7-197"><strong>Invoice amount</strong> – The amount will be equal to the amount that is invoiced for the commodity.</span></span></li>
<li><span data-ttu-id="947c7-198"><strong>Pamatsumma</strong> — summa būs vienāda ar summu, par kādu tiktu izrakstīts rēķins, pirms tiek piemērotas jebkādas atlaides.</span><span class="sxs-lookup"><span data-stu-id="947c7-198"><strong>Base amount</strong> – The amount will be equal to the amount that would be invoiced before any discount is applied.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="947c7-199">Transportēšanas metodes</span><span class="sxs-lookup"><span data-stu-id="947c7-199">Transport methods</span></span></td>
<td><span data-ttu-id="947c7-200">Iestatiet transportēšanas režīmu saskaņā ar jūsu valsts/reģiona prasībām.</span><span class="sxs-lookup"><span data-stu-id="947c7-200">Set up the transport mode according to your country's/region's requirements.</span></span> <span data-ttu-id="947c7-201">Katram piegādes režīmam varat iestatīt noklusējuma transportēšanas metodi cilnē <strong>Ārējā tirdzniecība</strong>.</span><span class="sxs-lookup"><span data-stu-id="947c7-201">For each delivery mode, you can set up a default transport method on the <strong>Foreign trade</strong> tab.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="947c7-202">Ostas</span><span class="sxs-lookup"><span data-stu-id="947c7-202">Ports</span></span></td>
<td><span data-ttu-id="947c7-203">Iestatiet iekraušanas/izkraušanas ostu/lidostu, ja jūsu valsts/reģions vāc šo informāciju.</span><span class="sxs-lookup"><span data-stu-id="947c7-203">Set up the port/airport of loading/unloading if this information is collected by your country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="947c7-204">Statistikas procedūras</span><span class="sxs-lookup"><span data-stu-id="947c7-204">Statistics procedures</span></span></td>
<td><span data-ttu-id="947c7-205">Iestatiet statistikas procedūru, ja jūsu valsts/reģions vāc šo informāciju.</span><span class="sxs-lookup"><span data-stu-id="947c7-205">Set up the statistical procedure if this information is collected by your country/region.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a><span data-ttu-id="947c7-206">Iestatiet kārtulas Intrastat transakciju arhivēšanai</span><span class="sxs-lookup"><span data-stu-id="947c7-206">Set up rules for compressing Intrastat transactions</span></span>

<span data-ttu-id="947c7-207">Lapā **Intrastat arhivēšana** varat atlasīt laukus, kurus izmantot saspiešanai.</span><span class="sxs-lookup"><span data-stu-id="947c7-207">On the **Compression of Intrastat** page, you can select the fields to use for compression.</span></span> <span data-ttu-id="947c7-208">Visas transakcijas, kurām atlasītajiem laukiem Intrastat žurnālā ir tāda pati vērtību kombinācija, tiks saspiestas vienā transakcijā, kad Intrastat žurnālā palaižat saspiešanas funkciju.</span><span class="sxs-lookup"><span data-stu-id="947c7-208">All transactions that have the same combination of values for the selected fields in the Intrastat journal will be compressed into a single transaction when you run the Compress function in the Intrastat journal.</span></span>

### <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="947c7-209">Iestatīt starptautiskās tirdzniecības parametrus</span><span class="sxs-lookup"><span data-stu-id="947c7-209">Set up foreign trade parameters</span></span>

<span data-ttu-id="947c7-210">Lai iestatītu parametrus nākamajā tabulā, izmantojiet lapu **Ārējās tirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="947c7-210">Use the **Foreign trade parameters** page to set up the parameters in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="947c7-211">Cilne</span><span class="sxs-lookup"><span data-stu-id="947c7-211">Tab</span></span></th>
<th><span data-ttu-id="947c7-212">Parametri</span><span class="sxs-lookup"><span data-stu-id="947c7-212">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="947c7-213">Vispārīgi</span><span class="sxs-lookup"><span data-stu-id="947c7-213">General</span></span></td>
<td><ul>
<li><span data-ttu-id="947c7-214"><strong>Vispārīgi</strong> — norādiet tālāk aprakstīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="947c7-214"><strong>General</strong> – Specify the following information:</span></span>
<ul>
<li><span data-ttu-id="947c7-215">Noklusējuma transakcijas kodi pārdošanas pasūtījumiem, pirkšanas pasūtījumiem, kredīta notām un pārsūtīšanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="947c7-215">The default transaction codes for sales orders, purchase orders, credit notes, and transfer orders.</span></span> <span data-ttu-id="947c7-216">Transakcijas kods, kas ir iestatīts kredīta notām, tiek izmantots arī kā kods fizisko preču atgriešanai, un tas tiek izmantots noviržu fiziskajās atgriešanās pret labojumu kredīta notām.</span><span class="sxs-lookup"><span data-stu-id="947c7-216">The transaction code that is set up for credit notes is also used as the code for physical goods return and is used for deviating physical returns versus correction credit notes.</span></span></li>
<li><span data-ttu-id="947c7-217">Darbinieks, kas ir atbildīgs par Intrastat atskaišu sagatavošanu.</span><span class="sxs-lookup"><span data-stu-id="947c7-217">The employee who is responsible for preparing Intrastat reports.</span></span></li>
</ul></li>
<li><span data-ttu-id="947c7-218"><strong>Minimālā robeža</strong> — norādiet iestatījumus tādu transakciju atjaunināšanai, kas ir zem sliekšņa.</span><span class="sxs-lookup"><span data-stu-id="947c7-218"><strong>Minimum limit</strong> – Specify the settings for updating transactions that are below the threshold:</span></span>
<ul>
<li><span data-ttu-id="947c7-219">Sliekšņa summa un svars</span><span class="sxs-lookup"><span data-stu-id="947c7-219">The threshold amount and weight</span></span></li>
<li><span data-ttu-id="947c7-220">Preču kods, ko lietot transakcijām, kuras atrodas zem sliekšņa</span><span class="sxs-lookup"><span data-stu-id="947c7-220">The commodity code to apply to transactions that are under the threshold</span></span></li>
</ul></li>
<li><span data-ttu-id="947c7-221"><strong>Pārsūtīt</strong> — norādiet kritērijus transakciju pārsūtīšanai uz Intrastat žurnālu.</span><span class="sxs-lookup"><span data-stu-id="947c7-221"><strong>Transfer</strong> – Specify the criteria for transferring transactions to the Intrastat journal.</span></span> <span data-ttu-id="947c7-222">Varat norādīt, ka transakcijas tiek pārsūtītas tikai tad, ja krājumi atbilst vienam vai visiem no tālāk norādītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="947c7-222">You can specify that transactions are transferred only when the items meet one or all of the following criteria:</span></span>
<ul>
<li><span data-ttu-id="947c7-223">Krājumi nav pakalpojumu krājumi.</span><span class="sxs-lookup"><span data-stu-id="947c7-223">The items aren't service items.</span></span></li>
<li><span data-ttu-id="947c7-224">Krājumiem nav preces koda.</span><span class="sxs-lookup"><span data-stu-id="947c7-224">The items have a commodity code.</span></span></li>
<li><span data-ttu-id="947c7-225">Krājumiem ir svars.</span><span class="sxs-lookup"><span data-stu-id="947c7-225">The items have a weight.</span></span></li>
<li><span data-ttu-id="947c7-226">Krājumiem ir papildu vienības.</span><span class="sxs-lookup"><span data-stu-id="947c7-226">The items have additional units.</span></span></li>
</ul></li>
<li><span data-ttu-id="947c7-227"><strong>Pārbaudīt iestatījumus</strong> — norādiet kārtulas Intrastat datu pilnīguma pārbaudīšanai.</span><span class="sxs-lookup"><span data-stu-id="947c7-227"><strong>Check setup</strong> – Specify the rules for validating the completeness of Intrastat data.</span></span> <span data-ttu-id="947c7-228">Varat atlasīt, kuri dati tiek pārbaudīti.</span><span class="sxs-lookup"><span data-stu-id="947c7-228">You can select which data is validated.</span></span></li>
<li><span data-ttu-id="947c7-229"><strong>Noapaļošanas nosacījumi</strong> — norādiet tālāk uzskaitītos iestatījumus attiecībā uz summu un svaru noapaļošanu Intrastat atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="947c7-229"><strong>Rounding rules</strong> – Specify the following settings for rounding amounts and weights in Intrastat reporting:</span></span>
<ul>
<li><span data-ttu-id="947c7-230">Noapaļošanas nosacījums (precizitāte)</span><span class="sxs-lookup"><span data-stu-id="947c7-230">The rounding rule (precision)</span></span></li>
<li><span data-ttu-id="947c7-231">Noapaļošanas metode: uz augšu, uz leju vai parastā</span><span class="sxs-lookup"><span data-stu-id="947c7-231">The rounding method: up, down, or normal</span></span></li>
<li><span data-ttu-id="947c7-232">Decimāldaļskaitļu vietu skaits summām un svariem</span><span class="sxs-lookup"><span data-stu-id="947c7-232">The number of decimal places for amounts and weights</span></span></li>
<li><span data-ttu-id="947c7-233">Instrukcijas par tādu svaru noapaļošanu, kas ir mazāk par 1 kilogramu (kg): uz augšu līdz 1 kg, parastā, vai bez noapaļošanas</span><span class="sxs-lookup"><span data-stu-id="947c7-233">Instructions for rounding weights that are less than 1 kilogram (kg): up to 1 kg, normal, or no rounding</span></span></li>
</ul></li>
<li><span data-ttu-id="947c7-234"><strong>Elektronisko atskaišu veidošana</strong> — norādiet atsauces uz elektronisko atskaišu konfigurācijām, lai varētu ģenerēt elektronisku failu un atskaiti.</span><span class="sxs-lookup"><span data-stu-id="947c7-234"><strong>Electronic reporting</strong> – Specify references to electronic reporting configurations, so that you can generate an electronic file and report.</span></span></li>
<li><span data-ttu-id="947c7-235"><strong>Preču kodu hierarhija</strong> — norādiet kategoriju hierarhiju ar tipu <strong>Preču kods</strong>, kas apzīmē Intrastat preču kodu CN8.</span><span class="sxs-lookup"><span data-stu-id="947c7-235"><strong>Commodity code hierarchy</strong> – Specify the category hierarchy of the <strong>Commodity code</strong> type that represents Intrastat commodity code CN8.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="947c7-236">Aģenta kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="947c7-236">Agent contact information</span></span></td>
<td><span data-ttu-id="947c7-237">Norādiet aģenta nosaukumu/vārdu un uzvārdu, adresi, PVN reģistrācijas numuru, tālruņa numuru un faksa numuru.</span><span class="sxs-lookup"><span data-stu-id="947c7-237">Specify the agent's name, address, tax exempt number, telephone number, and fax number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="947c7-238">Valsts/reģiona rekvizīti</span><span class="sxs-lookup"><span data-stu-id="947c7-238">Country/region properties</span></span></td>
<td><span data-ttu-id="947c7-239">Pašreizējās juridiskās personas valsti/reģionu iestatiet uz <strong>Iekšzemes</strong>.</span><span class="sxs-lookup"><span data-stu-id="947c7-239">Set the country/region of the current legal entity to <strong>Domestic</strong>.</span></span> <span data-ttu-id="947c7-240">ES valstīm/reģioniem, kas piedalās ES tirdzniecībā ar pašreizējo juridisko personu, valsti/reģionu iestatiet uz <strong>ES</strong>.</span><span class="sxs-lookup"><span data-stu-id="947c7-240">Set the country/region of EU countries/regions that participate in EU trade with the current legal entity to <strong>EU</strong>.</span></span> <span data-ttu-id="947c7-241">Katrai valstij/reģionam jūs norādāt arī valsts/reģiona kodu ārējās tirdzniecības nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="947c7-241">For each country/region, you also identify country/region code for foreign trade purposes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="947c7-242">Numuru sērija</span><span class="sxs-lookup"><span data-stu-id="947c7-242">Number sequence</span></span></td>
<td><span data-ttu-id="947c7-243">Norādiet numuru secību Intrastat žurnālam.</span><span class="sxs-lookup"><span data-stu-id="947c7-243">Specify the number sequence for the Intrastat journal.</span></span></td>
</tr>
</tbody>
</table>

 




