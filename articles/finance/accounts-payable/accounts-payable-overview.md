---
title: Kreditoru pārskata konfigurēšana
description: Šajā rakstā ir aprakstītas lapas, kas tiek izmantotas, lai iestatītu moduļa Parādi kreditoriem pamata un papildu funkcionalitāti. Tajā ir aprakstītas arī iestatīšanas darbības, kas ir jāizpilda, pirms sākat iestatīt moduli Parādi kreditoriem.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eed11cbe73ede71cabf83655fc1d37b1a979a4c
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830287"
---
# <a name="configure-accounts-payable-overview"></a><span data-ttu-id="9310f-104">Kreditoru pārskata konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9310f-104">Configure Accounts payable overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9310f-105">Šajā rakstā ir aprakstītas lapas, kas tiek izmantotas, lai iestatītu moduļa Parādi kreditoriem pamata un papildu funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="9310f-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable.</span></span> <span data-ttu-id="9310f-106">Tajā ir aprakstītas arī iestatīšanas darbības, kas ir jāizpilda, pirms sākat iestatīt moduli Parādi kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9310f-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="9310f-107">Priekšnosacījumi moduļa Kreditori iestatīšanai</span><span class="sxs-lookup"><span data-stu-id="9310f-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="9310f-108">Lai varētu iestatīt moduli Kreditori, ir jāizpilda šāda iestatīšana:</span><span class="sxs-lookup"><span data-stu-id="9310f-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="9310f-109">Virsgrāmatā:</span><span class="sxs-lookup"><span data-stu-id="9310f-109">In General ledger:</span></span>
    -   <span data-ttu-id="9310f-110">Ja plānojat izmantot maksājumu žurnālus, iestatiet maksājumu žurnālus.</span><span class="sxs-lookup"><span data-stu-id="9310f-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="9310f-111">Ja plānojat darbināt valūtas maiņas kursa korekcijas, iestatiet valūtu kodus lapā Valūtas, iestatiet maiņas kursa tipus lapā Maiņas kursa tipi un iestatiet valūtas maiņas kursus lapā Valūtas maiņas kursi.</span><span class="sxs-lookup"><span data-stu-id="9310f-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="9310f-112">Modulī Kases un bankas vadība iestatiet banku kontus, ko izmantot ar maksāšanas metodēm.</span><span class="sxs-lookup"><span data-stu-id="9310f-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="9310f-113">Iestatījumu lapas modulim Parādi kreditoriem</span><span class="sxs-lookup"><span data-stu-id="9310f-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="9310f-114">Izmantojiet nākamās lapas, lai katrai juridiskajai personai iestatītu moduļa Kreditori pamata funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="9310f-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="9310f-115">Lapas ir uzskaitītas ieteicamajā iestatīšanas secībā.</span><span class="sxs-lookup"><span data-stu-id="9310f-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="9310f-116">Lai iestatīšanas procesu padarītu vienkāršāku, no pirmajiem izveidotajiem ierakstiem varat izveidot veidnes.</span><span class="sxs-lookup"><span data-stu-id="9310f-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="9310f-117">Veidnē vērtības parasti tiek ievadītas daudzos laukos, lai parādītu līdzekļus, kurus organizācija vēlas ieviest konkrētam kreditora tipam.</span><span class="sxs-lookup"><span data-stu-id="9310f-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="9310f-118">Lapā Apmaksas nosacījumi definējiet apmaksas nosacījumus, kurus piešķirat pārdošanas pasūtījumiem, pirkšanas pasūtījumiem, debitoriem un kreditoriem, un kas nosaka rēķinu izpildes datumus.</span><span class="sxs-lookup"><span data-stu-id="9310f-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="9310f-119">Plašāku informāciju skatiet šeit: [Kreditora maksājumu papildmaksu definēšana](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="9310f-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="9310f-120">Lapā Maksāšanas metodes — kreditori izveidojiet un uzturiet informāciju par to, kā organizācija maksā saviem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9310f-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="9310f-121">Lapā Kreditoru grupas izveidojiet un uzturiet kreditoru grupas, kurām ir kopīgi svarīgi parametri attiecībā uz grāmatošanu, nosegšanu un maksājumiem, atskaišu veidošanu un prognozēšanu.</span><span class="sxs-lookup"><span data-stu-id="9310f-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="9310f-122">Lapā Kreditoru grāmatošanas metodes definējiet, kā kreditoru transakcijas tiek grāmatotas virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="9310f-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="9310f-123">Lapā Kreditoru moduļa parametri iestatiet noklusējuma iestatījumus, kas tiek lietoti, ja nav norādīti konkrētāki iestatījumi, parametrus dažādu veidu funkcionalitātei un dažādas numuru sērijas modulim Kreditori.</span><span class="sxs-lookup"><span data-stu-id="9310f-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="9310f-124">Lapā Formas iestatīšana definējiet dažādu ar kreditoriem saistītu dokumentu formātu un ko organizācija lieto, lai sekotu ieejas plūsmām no kreditoriem un ievadītu iemeslus maksājumu plūsmai pie kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9310f-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="9310f-125">Lapā Kreditori izveidojiet un uzturiet kreditoru kontus, kā arī nodokļu iestādes, kurām jūsu organizācija atskaitās par pārdošanas nodokli.</span><span class="sxs-lookup"><span data-stu-id="9310f-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="9310f-126">Neobligātās iestatījumu lapas modulim Parādi kreditoriem</span><span class="sxs-lookup"><span data-stu-id="9310f-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="9310f-127">Papildus pamata funkcionalitātei modulī Kreditori ietilpst arī cita funkcionalitāte, ko varat iestatīt.</span><span class="sxs-lookup"><span data-stu-id="9310f-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="9310f-128">Papildu iestatīšanas lapas ir sakārtotas pēc funkcionalitātes.</span><span class="sxs-lookup"><span data-stu-id="9310f-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="9310f-129">**Politikas**</span><span class="sxs-lookup"><span data-stu-id="9310f-129">**Policies**</span></span>
-   <span data-ttu-id="9310f-130">Lapā Kreditoru rēķinu ierobežojumi iestatiet kreditoru rēķinu ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="9310f-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="9310f-131">**Rēķinu salīdzināšana**</span><span class="sxs-lookup"><span data-stu-id="9310f-131">**Invoice matching**</span></span>

-   <span data-ttu-id="9310f-132">Lapā Rēķinu kopsummu tolerances iestatiet tolerances attiecībā uz rēķinu kopsummām.</span><span class="sxs-lookup"><span data-stu-id="9310f-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="9310f-133">Lapā Atbilstības ierobežojumi iestatiet divvirzienu un trīsvirzienu atbilstības ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="9310f-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="9310f-134">Lapā Cenu tolerances iestatiet tolerances attiecībā uz vienību cenām.</span><span class="sxs-lookup"><span data-stu-id="9310f-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="9310f-135">Lapā Krājumu cenu tolerances grupas iestatiet tolerances grupas attiecībā uz krājumu cenām.</span><span class="sxs-lookup"><span data-stu-id="9310f-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="9310f-136">Lapā Kreditoru cenu tolerances grupas iestatiet tolerances grupas attiecībā uz kreditoru cenām.</span><span class="sxs-lookup"><span data-stu-id="9310f-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="9310f-137">Lapā Maksu tolerances iestatiet tolerances attiecībā uz maksām.</span><span class="sxs-lookup"><span data-stu-id="9310f-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="9310f-138">**Darbplūsma**</span><span class="sxs-lookup"><span data-stu-id="9310f-138">**Workflow**</span></span>

-   <span data-ttu-id="9310f-139">Lapā Kreditoru darbplūsmas iestatiet darbplūsmas konfigurācijas attiecībā uz žurnālu apstiprinājumiem un pirkšanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="9310f-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="9310f-140">**Iemesli**</span><span class="sxs-lookup"><span data-stu-id="9310f-140">**Reasons**</span></span>

-   <span data-ttu-id="9310f-141">Lapā Kreditoru iemesli iestatiet iemeslu kodus.</span><span class="sxs-lookup"><span data-stu-id="9310f-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="9310f-142">**Izmaksas**</span><span class="sxs-lookup"><span data-stu-id="9310f-142">**Charges**</span></span>

-   <span data-ttu-id="9310f-143">Lapā Maksas kods iestatiet kodus maksām, kas tiek izmantotas pirkšanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="9310f-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="9310f-144">Lapā Kreditoru izmaksu grupa izveidojiet un uzturiet izmaksu grupas kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9310f-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="9310f-145">Lapā Krājumu maksu grupasizveidojiet un uzturiet maksu grupas attiecībā uz krājumiem.</span><span class="sxs-lookup"><span data-stu-id="9310f-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="9310f-146">Lapā Automātiskās maksas definējiet maksas, kas pasūtījumiem tiek piešķirtas automātiski.</span><span class="sxs-lookup"><span data-stu-id="9310f-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="9310f-147">**Papildu krājumi**</span><span class="sxs-lookup"><span data-stu-id="9310f-147">**Supplementary items**</span></span>

-   <span data-ttu-id="9310f-148">Lapā Papildu krājumu grupas - Kreditors izveidojiet un uzturiet papildu krājumu grupas kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9310f-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="9310f-149">Lapā Papildu krājumu grupas - Krājumi izveidojiet un uzturiet papildu krājumu grupas krājumiem.</span><span class="sxs-lookup"><span data-stu-id="9310f-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="9310f-150">**Sadale**</span><span class="sxs-lookup"><span data-stu-id="9310f-150">**Distribution**</span></span>

-   <span data-ttu-id="9310f-151">Lapā Piegādes nosacījumi izveidojiet un uzturiet nosacījumus attiecībā uz krājumu pārsūtīšanu no pārdevēja pie pircēja.</span><span class="sxs-lookup"><span data-stu-id="9310f-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="9310f-152">Lapā Piegādes režīmi izveidojiet un uzturiet transportēšanas metodes, kas tiek lietotas, kad pasūtījums no pārdevēja tiek piegādāts pircējam.</span><span class="sxs-lookup"><span data-stu-id="9310f-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="9310f-153">Lapā Adresātu kodi izveidojiet un uzturiet identifikatorus un aprakstus piegādes galamērķiem.</span><span class="sxs-lookup"><span data-stu-id="9310f-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="9310f-154">**Formas**</span><span class="sxs-lookup"><span data-stu-id="9310f-154">**Forms**</span></span>

-   <span data-ttu-id="9310f-155">Lapā Formu piezīmes izveidojiet standarta tekstu, kas ir redzams dažādās lapās.</span><span class="sxs-lookup"><span data-stu-id="9310f-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="9310f-156">Lapā Formu kārtošanas parametri iestatiet kārtošanas secību attiecībā uz pieprasījumiem, ieejas plūsmas sarakstiem, pavadzīmēm un rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="9310f-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="9310f-157">Lapā Drukas pārvaldības iestatīšana iestatiet drukas pārvaldības informāciju attiecībā uz lapu oriģināliem un kopijām.</span><span class="sxs-lookup"><span data-stu-id="9310f-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="9310f-158">**Maksājumi**</span><span class="sxs-lookup"><span data-stu-id="9310f-158">**Payments**</span></span>

-   <span data-ttu-id="9310f-159">Lapā Termiņatlaides iestatiet un pārvaldiet nosacījumus attiecībā uz termiņatlaižu saņemšanu.</span><span class="sxs-lookup"><span data-stu-id="9310f-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="9310f-160">Termiņatlaižu kodi ir saitīti ar kreditoriem un tiek pielietoti pirkšanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="9310f-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="9310f-161">Lapā Maksājumu grafiki iestatiet maksājumu grafikus, kas tiek izmantoti, lai pārvaldītu iemaksu maksājumus kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9310f-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="9310f-162">Lapā Maksāšanas dienas definējiet maksāšanas dienas, kas tiek lietotas, lai aprēķinātu izpildes datumus, un norādiet maksāšanas dienas noteiktai nedēļas vai mēneša dienai.</span><span class="sxs-lookup"><span data-stu-id="9310f-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="9310f-163">Lapā Komisijas maksa izveidojiet un uzturiet komisijas maksas, kas ir saistītas ar kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9310f-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="9310f-164">Lapā Maksājuma instrukcija izveidojiet un uzturiet maksājumu instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="9310f-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="9310f-165">**Statistika**</span><span class="sxs-lookup"><span data-stu-id="9310f-165">**Statistics**</span></span>

-   <span data-ttu-id="9310f-166">Lapā Vecumstruktūras periodu definīcijas iestatiet lietotāja definētus intervālus, kas tiek izmantoti, lai analizētu kreditoru kontu sadalījumu pa termiņiem.</span><span class="sxs-lookup"><span data-stu-id="9310f-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="9310f-167">Lapā Biznesa nozare izveidojiet biznesa nozaru (Line of Business — LOB) kodus, kas tiek piešķirti kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="9310f-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="9310f-168">**Nodoklis 1099**</span><span class="sxs-lookup"><span data-stu-id="9310f-168">**Tax 1099**</span></span>

-   <span data-ttu-id="9310f-169">Lapā **1099 lauki** pārbaudiet un atjauniniet minimālās summas, par kurām ir jāatskaitās Iekšējam ieņēmumu dienestam (Internal Revenue Service — IRS), pamatojoties uz visjaunākajām IRS prasībām.</span><span class="sxs-lookup"><span data-stu-id="9310f-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="9310f-170">**Neobligāti iestatījumi citiem moduļiem**</span><span class="sxs-lookup"><span data-stu-id="9310f-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="9310f-171">**Organizācijas administrēšana**</span><span class="sxs-lookup"><span data-stu-id="9310f-171">**Organization administration**</span></span>

-   <span data-ttu-id="9310f-172">Lapā Numuru sērijas iestatiet numuru sēriju grupas rēķinu numuriem.</span><span class="sxs-lookup"><span data-stu-id="9310f-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="9310f-173">Iestatiet adreses informāciju šādās lapās:</span><span class="sxs-lookup"><span data-stu-id="9310f-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="9310f-174">Adreses iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9310f-174">Address setup</span></span>
    -   <span data-ttu-id="9310f-175">NAF kodi (Francija)</span><span class="sxs-lookup"><span data-stu-id="9310f-175">NAF codes</span></span>
    -   <span data-ttu-id="9310f-176">Importēt pasta indeksus</span><span class="sxs-lookup"><span data-stu-id="9310f-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="9310f-177">**Virsgrāmata**</span><span class="sxs-lookup"><span data-stu-id="9310f-177">**General ledger**</span></span>

-   <span data-ttu-id="9310f-178">Lapā Finanšu dimensijas iestatiet finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="9310f-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="9310f-179">Iestatiet nodokļu informāciju šādās lapās:</span><span class="sxs-lookup"><span data-stu-id="9310f-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="9310f-180">PVN kodi</span><span class="sxs-lookup"><span data-stu-id="9310f-180">Sales tax codes</span></span>
    -   <span data-ttu-id="9310f-181">PVN grupas</span><span class="sxs-lookup"><span data-stu-id="9310f-181">Sales tax groups</span></span>
    -   <span data-ttu-id="9310f-182">Krājumu PVN grupas</span><span class="sxs-lookup"><span data-stu-id="9310f-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="9310f-183">Kontu grupa</span><span class="sxs-lookup"><span data-stu-id="9310f-183">Account group</span></span>
    -   <span data-ttu-id="9310f-184">PVN reģistrācijas kodi</span><span class="sxs-lookup"><span data-stu-id="9310f-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="9310f-185">PVN jurisdikcijas</span><span class="sxs-lookup"><span data-stu-id="9310f-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="9310f-186">Nodokļu iestādes</span><span class="sxs-lookup"><span data-stu-id="9310f-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="9310f-187">PVN apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="9310f-187">Sales tax settlement periods</span></span>

<span data-ttu-id="9310f-188">**Kases un bankas vadība**</span><span class="sxs-lookup"><span data-stu-id="9310f-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="9310f-189">Lapā Maksājuma mērķu kodi iestatiet centrālās bankas mērķa kodu.</span><span class="sxs-lookup"><span data-stu-id="9310f-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>





