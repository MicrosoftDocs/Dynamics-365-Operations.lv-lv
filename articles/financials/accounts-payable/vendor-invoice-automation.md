---
title: Kreditoru rēķinu izrakstīšanas automatizācija
description: Šajā tēmā ir paskaidrots, kādi līdzekļi ir pieejami kreditoru rēķinu (arī to rēķinu, kam ir pielikumi) automatizācijai visā procesa garumā.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81822294c86961137ff649be1f219b896cbc10c
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/25/2019
ms.locfileid: "896584"
---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="bb5b6-103">Kreditoru rēķinu izrakstīšanas automatizācija</span><span class="sxs-lookup"><span data-stu-id="bb5b6-103">Vendor invoice automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb5b6-104">Šajā tēmā ir paskaidrots, kādi līdzekļi ir pieejami kreditoru rēķinu (arī to rēķinu, kam ir pielikumi) automatizācijai visā procesa garumā.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="bb5b6-105">Organizācijas, kast vēlas uzlabot savus kreditoru procesus, rēķinu apstrādi bieži norāda kā vienu no galvenajiem procesiem, kura efektivitāti ir nepieciešams palielināt.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="bb5b6-106">Daudzos gadījumos šīs organizācijas papīra rēķinu apstrādi uztic trešās puses optiskās rakstzīmju pazīšanas (OCR) pakalpojumu sniedzējam.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="bb5b6-107">Viņi saņem ar mašīnu lasāmus rēķina metadatus kopā ar skenētu katra rēķina attēlu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="bb5b6-108">Automatizācijas nolūkos tiek izveidots “pēdējās jūdzes” risinājums, lai iespējotu šo artefaktu patēriņu rēķinu apstrādes sistēmā.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="bb5b6-109">Tagad programmatūra Microsoft Dynamics 365 for Finance and Operations jau sākotnēji nodrošina šī pēdējā soļa automatizāciju, izmantojot rēķinu automatizācijas risinājumu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-109">Microsoft Dynamics 365 for Finance and Operations now enables this “last mile” automation out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="bb5b6-110">Risinājuma konteksts</span><span class="sxs-lookup"><span data-stu-id="bb5b6-110">Solution context</span></span>

<span data-ttu-id="bb5b6-111">Rēķinu automatizācijas risinājums nodrošina standarta interfeisu, kas var pieņemt rēķina metadatus rēķina virsrakstam un rēķina rindām, kā arī pielikumiem, kas attiecas uz rēķinu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="bb5b6-112">Jebkura ārējā sistēma, kas var ģenerēt šim interfeisam atbilstošus artefaktus, varēs programmatūrā Finance and Operations nosūtīt plūsmu automātiskai rēķinu un pielikumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed into Finance and Operations for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="bb5b6-113">Tālāk esošajā attēlā ir parādīts parauga integrācijas scenārijs, kurā uzņēmums Contoso kopā ar OCR pakalpojumu sniedzēju izmanto kreditora rēķinu apstrādi.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="bb5b6-114">Uzņēmuma Contoso kreditori pakalpojumu sniedzējam sūta rēķinus, izmantojot e-pastu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="bb5b6-115">Izmantojot OCR apstrādi, pakalpojumu sniedzējs ģenerē rēķina metadatus (virsrakstu un/vai rindas) un skenēto rēķina attēlu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="bb5b6-116">Pēc tam integrācijas slānis šos artefaktus pārveido tā, lai programmatūra Finance and Operations varētu tos patērēt.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-116">An integration layer then transforms these artifacts so that Finance and Operations can consume them.</span></span>

![Parauga integrācijas scenārijs](media/vendor_invoice_automation_01.png)

<span data-ttu-id="bb5b6-118">Ja ir nepieciešama rēķinu integrācija, ir iespējamas vairākas iepriekšējā scenārija variācijas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="bb5b6-119">Datu migrācija ir cits lietošanas gadījums, kurā šo interfeisu var izmantot rēķinu un pielikumu izveidei programmatūrā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-119">Data migration is another use case where this interface can be used to create invoices and attachments in Finance and Operations.</span></span>

### <a name="solution-components"></a><span data-ttu-id="bb5b6-120">Risinājuma komponenti</span><span class="sxs-lookup"><span data-stu-id="bb5b6-120">Solution components</span></span>

<span data-ttu-id="bb5b6-121">Risinājuma pēdas nospiedums sastāv no tālāk norādītajiem komponentiem.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="bb5b6-122">Datu elementi rēķina virsrakstam, rēķina rindām un rēķina pielikumiem</span><span class="sxs-lookup"><span data-stu-id="bb5b6-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="bb5b6-123">Izņēmumu apstrāde rēķiniem</span><span class="sxs-lookup"><span data-stu-id="bb5b6-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="bb5b6-124">Līdzās novietotu pielikumu skatītājs rēķinos</span><span class="sxs-lookup"><span data-stu-id="bb5b6-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="bb5b6-125">Atlikusī daļa šajā tēmā veltīta detalizētiem aprakstiem par šiem risinājuma komponentiem.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="bb5b6-126">Datu elementi</span><span class="sxs-lookup"><span data-stu-id="bb5b6-126">Data entities</span></span>

<span data-ttu-id="bb5b6-127">Datu pakotne ir darba vienība, kas ir jānosūta uz programmatūru Finance and Operations, lai varētu izveidot rēķina virsrakstus, rēķina rindas un rēķina pielikumus.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-127">A data package is the unit of work that must be sent to Finance and Operations, so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="bb5b6-128">Artefaktiem, kas veido datu pakotni, ir izmantoti tālāk norādītie datu elementi.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="bb5b6-129">Kreditora rēķina virsraksts</span><span class="sxs-lookup"><span data-stu-id="bb5b6-129">Vendor invoice header</span></span>
+ <span data-ttu-id="bb5b6-130">Kreditora rēķina rinda</span><span class="sxs-lookup"><span data-stu-id="bb5b6-130">Vendor invoice line</span></span>
+ <span data-ttu-id="bb5b6-131">Kreditora rēķina dokumenta pielikums</span><span class="sxs-lookup"><span data-stu-id="bb5b6-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="bb5b6-132">Kreditora rēķina dokumenta pielikums ir jauns datu elements, kas ir ieviests kā daļa no šī līdzekļa.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="bb5b6-133">Kreditora rēķina virsraksta elements ir modificēts tā, lai tas atbalstītu pielikumus.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="bb5b6-134">Kreditora rēķina rindas elements nav modificēts šim līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="bb5b6-135">Šajā tēmā nav sniegta detalizēta datu pakotnes definīcija.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="bb5b6-136">Tajā arī nav izskaidrots, kā izveidot datu pakotnes.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="bb5b6-137">Šo informāciju skatiet sadaļā [Datu elementi un pakotņu struktūra](../../dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="bb5b6-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="bb5b6-138">Lai ātri ģenerētu testa datus, kas ietver rēķinus un pielikumus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="bb5b6-139">Pierakstieties savā Finance and Operations instancē.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-139">Sign in to your Finance and Operations instance.</span></span>
1. <span data-ttu-id="bb5b6-140">Dodieties uz **Kreditori** > **Rēķini** > **Gaidošie kreditoru rēķini**.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="bb5b6-141">Izveidojiet rēķinus ar rindām un pielikumiem.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb5b6-142">Pielikumiem ir jābūt virsraksta pielikumiem.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-142">The attachments must be header attachments.</span></span> <span data-ttu-id="bb5b6-143">Pašlaik elements Kreditora rēķina dokumenta pielikums neatbalsta rindas pielikumus.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="bb5b6-144">Atveriet darbvietu **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="bb5b6-145">Izveidojiet eksportēšanas darbu, kas ietver elementus Kreditora rēķina virsraksts, Kreditora rēķina rinda un Kreditora rēķina dokumenta pielikums.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="bb5b6-146">Eksportējiet datus.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-146">Export the data.</span></span>
1. <span data-ttu-id="bb5b6-147">Lejupielādējiet eksportētos datus kā pakotni.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-147">Download the exported data as a package.</span></span> <span data-ttu-id="bb5b6-148">Tagad pakotni varat izmantot datu importēšanai mērķa instancēs testēšanas nolūkos.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="bb5b6-149">Juridiskās personas noteikšana rēķinam</span><span class="sxs-lookup"><span data-stu-id="bb5b6-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="bb5b6-150">Rēķini, kas tiek importēti, izmantojot datu pakotnes, ar juridisko personu, kam tie pieder, var būt saistīti divos veidos.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="bb5b6-151">Importēšanas darbs, kas apstrādā rēķinu, importē to tajā pašā uzņēmumā, kurā darbs tika plānots darbvietā **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="bb5b6-152">Citiem vārdiem sakot, darba uzņēmums nosaka uzņēmumu, kam pieder rēķins.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="bb5b6-153">Kad datu pakotne, kas ietver rēķinus, ir nosūtīta uz programmatūru Finance and Operations, izsaucējs (t.i., integrācijas programma, kas darbojas ārpus programmatūras Finance and Operations) var HTTP pieprasījumā skaidri norādīt uzņēmuma ID.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-153">When the data package that contains invoices is sent to Finance and Operations, the caller (that is, the integration application that runs outside of Finance and Operations) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="bb5b6-154">Šajā gadījumā uzņēmuma konteksts, kurā apstrādes darbs tiek izpildīts programmatūrā Finance and Operations, tiek ignorēts, un rēķini tiek importēti uzņēmumā, kas tika nodots, izmantojot HTTP pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-154">In this case, the company context in which the processing job runs in Finance and Operations is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5b6-155">Šī izturēšanās ir standarta datu pārvaldības izturēšanās.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="bb5b6-156">Tā ir izskaidrota šeit saistībā ar rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="bb5b6-157">Izņēmumu apstrāde</span><span class="sxs-lookup"><span data-stu-id="bb5b6-157">Exception processing</span></span>

<span data-ttu-id="bb5b6-158">Scenārijos, kuros kreditora rēķini programmatūrā Finance and Operations nonāk, izmantojot integrāciju, ir nepieciešams viegls veids, kā kreditoru grupas dalībniekam apstrādāt izņēmumus vai neizdevušos rēķinus un izveidot gaidošos rēķinus no rēķiniem, kas neizdevās.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="bb5b6-159">Šī izņēmumu apstrāde kreditoru rēķiniem tagad ir daļa no Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="bb5b6-160">Izņēmumu saraksta lapa</span><span class="sxs-lookup"><span data-stu-id="bb5b6-160">Exceptions list page</span></span>

<span data-ttu-id="bb5b6-161">Jaunā rēķinu izņēmumu saraksta lapa ir pieejama šeit: **Kreditori** > **Rēķini** > **Importēšanas kļūmes** > **Kreditoru rēķini, kuru importēšana bija nesekmīga**.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="bb5b6-162">Šajā lapā ir parādīti visi kreditora rēķina virsraksta ieraksti no datu elementa Kreditora rēķina virsraksts izstādīšanas tabulas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="bb5b6-163">Ņemiet vērā, ka tos pašus ierakstus varat skatīt no darbvietas **Datu pārvaldība**, kurā varat arī veikt tās pašas darbības, kas ir nodrošinātas izņēmumu apstrādes līdzeklī.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="bb5b6-164">Tomēr izņēmumu apstrādes līdzekļa nodrošinātais lietotāja interfeiss ir optimizēts funkcionālajam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Izņēmumu saraksta lapa](media/vendor_invoice_automation_02.png)

<span data-ttu-id="bb5b6-166">Šajā saraksta lapā ir tālāk norādītie lauki, kas tajā nonāk ar plūsmu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="bb5b6-167">**Uzņēmums** — uzņēmums, kam pieder rēķins</span><span class="sxs-lookup"><span data-stu-id="bb5b6-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="bb5b6-168">**Kļūdas ziņojums** — kļūdas ziņojums, ko sniedz datu pārvaldības struktūra, lai izskaidrotu, kādēļ nevarēja izveidot rēķinu</span><span class="sxs-lookup"><span data-stu-id="bb5b6-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="bb5b6-169">**Numurs** — rēķina numurs</span><span class="sxs-lookup"><span data-stu-id="bb5b6-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="bb5b6-170">**Rēķina konts**</span><span class="sxs-lookup"><span data-stu-id="bb5b6-170">**Invoice account**</span></span>
+ <span data-ttu-id="bb5b6-171">**Nosaukums** — kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="bb5b6-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="bb5b6-172">**Kreditora konts**</span><span class="sxs-lookup"><span data-stu-id="bb5b6-172">**Vendor account**</span></span>
+ <span data-ttu-id="bb5b6-173">**Pirkšanas pasūtījums** — rēķina pirkšanas pasūtījuma (PP) numurs</span><span class="sxs-lookup"><span data-stu-id="bb5b6-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="bb5b6-174">**Grāmatošanas datums**</span><span class="sxs-lookup"><span data-stu-id="bb5b6-174">**Posting date**</span></span>
+ <span data-ttu-id="bb5b6-175">**Rēķina datums**</span><span class="sxs-lookup"><span data-stu-id="bb5b6-175">**Invoice date**</span></span>
+ <span data-ttu-id="bb5b6-176">**Rēķina apraksts**</span><span class="sxs-lookup"><span data-stu-id="bb5b6-176">**Invoice description**</span></span>
+ <span data-ttu-id="bb5b6-177">**Valūta**</span><span class="sxs-lookup"><span data-stu-id="bb5b6-177">**Currency**</span></span>
+ <span data-ttu-id="bb5b6-178">**Žurnāls**</span><span class="sxs-lookup"><span data-stu-id="bb5b6-178">**Log**</span></span>
+ <span data-ttu-id="bb5b6-179">**Rindas atsauce** — identifikators, kas ir no ārējās sistēmas</span><span class="sxs-lookup"><span data-stu-id="bb5b6-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb5b6-180">Rindas atsauce nav rēķina ID.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="bb5b6-181">Šajā saraksta lapā ir arī priekšskatījuma rūts, kuru var izmantot tālāk norādītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="bb5b6-182">Skatiet visu kļūdas ziņojumu, lai jums nebūtu jāizvērš kolonna **Kļūdas ziņojums** režģī.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="bb5b6-183">Skatiet visu rēķina pielikumu sarakstu, ja rēķinam tādi ir.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="bb5b6-184">Saraksta lapa atbalsta arī tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="bb5b6-185">**Rediģēt** — atveriet izņēmumu ierakstu rediģēšanas režīmā, lai labotu problēmas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="bb5b6-186">**Opcijas** — piekļūstiet standarta opcijām, kas ir pieejamas saraksta lapās.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="bb5b6-187">Varat izmantot opciju **Pievienot darbvietai**, lai izņēmumu saraksta lapu piespraustu savai darbvietai kā sarakstu vai elementu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="bb5b6-188">Detalizētas informācijas par izņēmumu lapa</span><span class="sxs-lookup"><span data-stu-id="bb5b6-188">Exception details page</span></span>

<span data-ttu-id="bb5b6-189">Kad sākat rediģēšanas režīmu, tiek parādīta detalizētās informācijas par izņēmumu lapa rēķinam, kuram ir problēmas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="bb5b6-190">Ja rēķinam ir pielikumi, rēķins un noklusējuma pielikums tiek rādīti līdzās detalizētās informācijas par izņēmumu lapā.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Detalizētas informācijas par izņēmumu lapa](media/vendor_invoice_automation_03.png)

<span data-ttu-id="bb5b6-192">Iepriekšējā attēlā ienākošajam kreditora rēķina virsrakstam nebija nevienas rindas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="bb5b6-193">Tāpēc rindu sadaļa ir tukša.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="bb5b6-194">Detalizētās informācijas par izņēmumu lapa atbalsta tālāk norādīto operāciju.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="bb5b6-195">**Izveidot gaidošu rēķinu** — kad būsit labojis problēmas rēķinā kā daļu no izņēmumu apstrādes, varat noklikšķināt uz šīs pogas, lai izveidotu gaidošo rēķinu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="bb5b6-196">Gaidošo rēķinu izveide notiek fonā (kā asinhrona operācija).</span><span class="sxs-lookup"><span data-stu-id="bb5b6-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="bb5b6-197">Koplietoto pakalpojumu izņēmumu apstrāde salīdzinājumā ar apstrādi, kuras pamatā ir organizācija</span><span class="sxs-lookup"><span data-stu-id="bb5b6-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="bb5b6-198">Izņēmumu saraksta lapa atbalsta standarta drošības struktūras, kuras darbvieta **Datu pārvaldība** atbalsta izstādīšanas ierakstu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="bb5b6-199">Rēķinu importēšanas darbu var nodrošināt tālāk norādītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="bb5b6-200">Pēc lietotāja lomas</span><span class="sxs-lookup"><span data-stu-id="bb5b6-200">By user role</span></span>
+ <span data-ttu-id="bb5b6-201">Pēc lietotāja</span><span class="sxs-lookup"><span data-stu-id="bb5b6-201">By user</span></span>
+ <span data-ttu-id="bb5b6-202">Pēc juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="bb5b6-202">By legal entity</span></span>

![Importēšanas darbs, kas ir nodrošināts pēc lietotāja lomas un juridiskās personas](media/vendor_invoice_automation_04.png)

<span data-ttu-id="bb5b6-204">Ja rēķina importēšanas darbam ir konfigurēta drošība, izņēmumu saraksta lapa respektē šos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="bb5b6-205">Lietotāji varēs redzēt tikai tos rēķinu izņēmumu ierakstus, ko šis iestatījums ļauj viņiem skatīt.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="bb5b6-206">Piemēram, uzņēmums Contoso ir izlēmis apstrādāt rēķinu izņēmumus pēc juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="bb5b6-207">Tādēļ drošība rēķina importēšanas darbā ir konfigurēta tā, lai lietotājs juridiskajā personā A varētu redzēt tikai juridiskās personas A rēķinu izņēmumus, savukārt lietotājs juridiskajā personā B varētu redzēt tikai juridiskās personas B izņēmumus. Šis iestatījums rēķinu izņēmumu pārvaldībai nodrošina pienākumu sadali.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="bb5b6-208">Contoso var arī izlemt nelietot nekādu drošību, lai tie paši lietotāji varētu apstrādāt rēķinu izņēmumus visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="bb5b6-209">Šis iestatījums rēķinu izņēmumu pārvaldībai nodrošina koplietoto pakalpojumu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="bb5b6-210">Līdzās novietotu pielikumu skatītājs</span><span class="sxs-lookup"><span data-stu-id="bb5b6-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="bb5b6-211">Lai palīdzētu jums viegli skatīt kreditoru rēķinu pielikumus, tālāk norādītajās lapās, kas tiek izmantotas rēķinu apstrādes procesā, tagad ir pieejams pielikumu skatītājs.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="bb5b6-212">**Izņēmumu apstrāde**</span><span class="sxs-lookup"><span data-stu-id="bb5b6-212">**Exception handling**</span></span>
+ <span data-ttu-id="bb5b6-213">Lapa **Gaidošie kreditoru rēķini** (pieejama arī rēķinu pārskatīšanas procesā)</span><span class="sxs-lookup"><span data-stu-id="bb5b6-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="bb5b6-214">Uzziņu lapa **Rēķinu žurnāls** (grāmatotajiem rēķiniem)</span><span class="sxs-lookup"><span data-stu-id="bb5b6-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="bb5b6-215">Tālāk norādīta galvenā funkcionalitāte, ko nodrošina pielikumu skatītājs.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="bb5b6-216">Skatiet visus pielikumu tipus, ko atbalsta dokumentu pārvaldība (failus, attēlus, vietrāžus URL un piezīmes).</span><span class="sxs-lookup"><span data-stu-id="bb5b6-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="bb5b6-217">Skatiet vairāklapu TIFF failus.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="bb5b6-218">Veiciet tālāk norādītās darbības attēlu failiem.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="bb5b6-219">Iezīmējiet attēla daļas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="bb5b6-220">Bloķējiet attēla daļas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-220">Block parts of the image.</span></span>
  + <span data-ttu-id="bb5b6-221">Pievienojiet attēlam anotācijas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="bb5b6-222">Tuviniet un tāliniet attēlu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="bb5b6-223">Bīdiet attēlu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-223">Pan the image.</span></span>
  + <span data-ttu-id="bb5b6-224">Atsauciet darbības un atceltiem atsaukšanu tām.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="bb5b6-225">Pielāgojiet attēla lielumu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5b6-226">Šīs darbības ir pieejama tikai attēlu failiem (JPEG, TIFF, PNG u.c.).</span><span class="sxs-lookup"><span data-stu-id="bb5b6-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="bb5b6-227">Visas izmaiņas, ko veicat attēlā, izmantojot šīs darbības, tiek saglabātas attēla failā.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="bb5b6-228">Pašlaik pielikumu skatītājs neietver versiju izveides un auditēšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="bb5b6-229">Noklusējuma pielikums</span><span class="sxs-lookup"><span data-stu-id="bb5b6-229">Default attachment</span></span>

<span data-ttu-id="bb5b6-230">Ja kreditora rēķinā ir vairāk nekā viens pielikums, lapā **Pielikumi** vienu no dokumentiem varat iestatīt kā noklusējuma pielikumu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="bb5b6-231">Opcija **Ir noklusējuma pielikums** ir jauna opcija, kas tika pievienota kā daļa no šī līdzekļa.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="bb5b6-232">Šī opcija ir parādīta arī datu elementā Kreditora rēķina dokumenta pielikums.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="bb5b6-233">Tādējādi noklusējuma pielikumu var iestatīt, izmantojot integrācijas.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="bb5b6-234">Kā noklusējuma pielikumu var iestatīt tikai vienu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="bb5b6-235">Kad dokumentu esat iestatījis kā noklusējuma pielikumu, atverot rēķinu, tas tiek automātiski parādīts pielikumu skatītājā.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="bb5b6-236">Ja kā noklusējuma pielikumu neiestatāt nevienu dokumentu, atverot rēķinu, pielikumu skatītājs neparāda nevienu pielikumu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="bb5b6-237">Rēķinu pielikumu rādīšana/paslēpšana</span><span class="sxs-lookup"><span data-stu-id="bb5b6-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="bb5b6-238">Izmantojot uzziņu lapās **Izņēmumu apstrāde**, **Gaidošs rēķins** un **Rēķinu žurnāls** pieejamo jauno pogu, varat rādīt vai paslēpt pielikumu skatītāju.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="bb5b6-239">Drošība</span><span class="sxs-lookup"><span data-stu-id="bb5b6-239">Security</span></span>

<span data-ttu-id="bb5b6-240">Tālāk norādītās pielikumu skatītāja darbības tiek kontrolētas, izmantojot no lomas atkarīgu drošību.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="bb5b6-241">Iezīmēšana</span><span class="sxs-lookup"><span data-stu-id="bb5b6-241">Highlighting</span></span>
+ <span data-ttu-id="bb5b6-242">Bloķēts</span><span class="sxs-lookup"><span data-stu-id="bb5b6-242">Block</span></span>
+ <span data-ttu-id="bb5b6-243">Anotēšana</span><span class="sxs-lookup"><span data-stu-id="bb5b6-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="bb5b6-244">Lapa Gaidošie kreditoru rēķini</span><span class="sxs-lookup"><span data-stu-id="bb5b6-244">Pending vendor invoices page</span></span>

<span data-ttu-id="bb5b6-245">Tālāk norādītās privilēģijas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi vai lasīšanas/rakstīšanas piekļuvi iezīmēšanas, bloķēšanas un anotēšanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="bb5b6-246">**Uzturēt kreditora rēķina attēlu** — šī privilēģija nodrošina lasīšanas/rakstīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="bb5b6-247">**Skatīt kreditora rēķina attēlu** — šī privilēģija nodrošina tikai lasīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="bb5b6-248">Tālāk norādītie pienākumi pielikumu skatītājam nodrošina tikai lasīšanas vai lasīšanas/rakstīšanas piekļuvi tālāk aprakstītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="bb5b6-249">**Uzturēt kreditoru rēķinus** — šim pienākumam ir piešķirta privilēģija Uzturēt kreditora rēķina attēlu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="bb5b6-250">**Iegūt informāciju par kreditora rēķina statusu** — šim pienākumam ir piešķirta privilēģija Skatīt kreditora rēķina attēlu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="bb5b6-251">Tālāk norādītās lomas pielikumu skatītājam nodrošina tikai lasīšanas vai lasīšanas/rakstīšanas piekļuvi tālāk aprakstītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="bb5b6-252">**Kreditoru darbinieks** un **Kreditoru vadītājs** — šīm lomām ir piešķirts pienākums Uzturēt kreditoru rēķinus.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="bb5b6-253">**Kreditoru darbinieks**, **Kreditoru vadītājs**, **Darbinieks, kas ir atbildīgs par kreditoru centralizētajiem maksājumiem**, un **Darbinieks, kas ir atbildīgs par kreditoru maksājumiem** — šīm lomām ir piešķirts pienākums Iegūt informāciju par kreditora rēķina statusu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="bb5b6-254">Detalizētas informācijas par rēķina izņēmumu lapa</span><span class="sxs-lookup"><span data-stu-id="bb5b6-254">Invoice exception details page</span></span>

<span data-ttu-id="bb5b6-255">Tālāk norādītās privilēģijas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi vai lasīšanas/rakstīšanas piekļuvi iezīmēšanas, bloķēšanas un anotēšanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5b6-256">Šajā sadaļā minētās komplektācijā iekļautās lomas rēķina attēliem pielikumu skatītājā nodrošina tikai lasīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="bb5b6-257">Ja lomai ir jābūt arī rakstīšanas piekļuvei attēliem, varat piešķirt rakstīšanas piekļuvi šai lomai, izmantojot šeit aprakstīto privilēģiju un pienākumu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="bb5b6-258">**Uzturēt kreditora rēķina virsraksta elementa attēlu** — šī privilēģija rēķina attēliem pielikumu skatītājā nodrošina lasīšanas/rakstīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="bb5b6-259">**Skatīt kreditora rēķina virsraksta elementa attēlu** — šī privilēģija rēķina attēlam pielikumu skatītājā nodrošina tikai lasīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="bb5b6-260">Tālāk norādītie pienākumi pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi tālāk aprakstītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="bb5b6-261">**Uzturēt kreditoru rēķinus** — šim pienākumam ir piešķirta privilēģija Uzturēt kreditora rēķina virsraksta elementa attēlu.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="bb5b6-262">Tālāk norādītās lomas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi tālāk aprakstītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="bb5b6-263">**Kreditoru darbinieks** un **Kreditoru vadītājs** — šīm lomām ir piešķirts pienākums Uzturēt kreditoru rēķinus.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="bb5b6-264">Pēc noklusējuma, ja lietotāja loma sniedz rediģēšanas tiesības jebkurā lapā, lietotājam rediģēšanas tiesības būs arī pielikumu skatītājā iezīmēšanas, bloķēšanas un anotēšanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="bb5b6-265">Tomēr, ja pastāv scenāriji, kuros noteiktai lomai ir nepieciešamas rediģēšanas tiesības lapā, bet ne pielikumu skatītājā, to var panākt, izmantojot atbilstošās privilēģijas no iepriekšējā saraksta.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>
