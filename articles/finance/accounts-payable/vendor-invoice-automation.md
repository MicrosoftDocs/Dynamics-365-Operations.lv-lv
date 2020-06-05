---
title: Kreditoru rēķinu izrakstīšanas automatizācija
description: Šajā tēmā ir paskaidrots, kādi līdzekļi ir pieejami kreditoru rēķinu (arī to rēķinu, kam ir pielikumi) automatizācijai visā procesa garumā.
author: abruer
manager: AnnBe
ms.date: 05/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4560d7b61fa8f014f9a1185da087df8b1c8e61ba
ms.sourcegitcommit: b7af921189048d9f2eb4d3fd57c704c742bc96e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/23/2020
ms.locfileid: "3396013"
---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="5e003-103">Kreditoru rēķinu izrakstīšanas automatizācija</span><span class="sxs-lookup"><span data-stu-id="5e003-103">Vendor invoice automation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e003-104">Šajā tēmā ir paskaidrots, kādi līdzekļi ir pieejami kreditoru rēķinu (arī to rēķinu, kam ir pielikumi) automatizācijai visā procesa garumā.</span><span class="sxs-lookup"><span data-stu-id="5e003-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="5e003-105">Organizācijas, kast vēlas uzlabot savus kreditoru procesus, rēķinu apstrādi bieži norāda kā vienu no galvenajiem procesiem, kura efektivitāti ir nepieciešams palielināt.</span><span class="sxs-lookup"><span data-stu-id="5e003-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="5e003-106">Daudzos gadījumos šīs organizācijas papīra rēķinu apstrādi uztic trešās puses optiskās rakstzīmju pazīšanas (OCR) pakalpojumu sniedzējam.</span><span class="sxs-lookup"><span data-stu-id="5e003-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="5e003-107">Viņi saņem ar mašīnu lasāmus rēķina metadatus kopā ar skenētu katra rēķina attēlu.</span><span class="sxs-lookup"><span data-stu-id="5e003-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="5e003-108">Automatizācijas nolūkos tiek izveidots “pēdējās jūdzes” risinājums, lai iespējotu šo artefaktu patēriņu rēķinu apstrādes sistēmā.</span><span class="sxs-lookup"><span data-stu-id="5e003-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="5e003-109">Tagad ir iespējota šī pēdējā soļa automatizācija, izmantojot rēķinu automatizācijas risinājumu.</span><span class="sxs-lookup"><span data-stu-id="5e003-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="5e003-110">Risinājuma konteksts</span><span class="sxs-lookup"><span data-stu-id="5e003-110">Solution context</span></span>

<span data-ttu-id="5e003-111">Rēķinu automatizācijas risinājums nodrošina standarta interfeisu, kas var pieņemt rēķina metadatus rēķina virsrakstam un rēķina rindām, kā arī pielikumiem, kas attiecas uz rēķinu.</span><span class="sxs-lookup"><span data-stu-id="5e003-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="5e003-112">Jebkura ārējā sistēma, kas var ģenerēt šim interfeisam atbilstošus artefaktus, varēs nosūtīt plūsmu automātiskai rēķinu un pielikumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="5e003-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="5e003-113">Tālāk esošajā attēlā ir parādīts parauga integrācijas scenārijs, kurā uzņēmums Contoso kopā ar OCR pakalpojumu sniedzēju izmanto kreditora rēķinu apstrādi.</span><span class="sxs-lookup"><span data-stu-id="5e003-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="5e003-114">Uzņēmuma Contoso kreditori pakalpojumu sniedzējam sūta rēķinus, izmantojot e-pastu.</span><span class="sxs-lookup"><span data-stu-id="5e003-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="5e003-115">Izmantojot OCR apstrādi, pakalpojumu sniedzējs ģenerē rēķina metadatus (virsrakstu un/vai rindas) un skenēto rēķina attēlu.</span><span class="sxs-lookup"><span data-stu-id="5e003-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="5e003-116">Pēc tam integrācijas slānis šos artefaktus pārveido tā, lai tos varētu patērēt.</span><span class="sxs-lookup"><span data-stu-id="5e003-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![Parauga integrācijas scenārijs](media/vendor_invoice_automation_01.png)

<span data-ttu-id="5e003-118">Ja ir nepieciešama rēķinu integrācija, ir iespējamas vairākas iepriekšējā scenārija variācijas.</span><span class="sxs-lookup"><span data-stu-id="5e003-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="5e003-119">Datu migrācija ir cits lietošanas gadījums, kurā šo interfeisu var izmantot rēķinu un pielikumu izveidei.</span><span class="sxs-lookup"><span data-stu-id="5e003-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="5e003-120">Risinājuma komponenti</span><span class="sxs-lookup"><span data-stu-id="5e003-120">Solution components</span></span>

<span data-ttu-id="5e003-121">Risinājuma pēdas nospiedums sastāv no tālāk norādītajiem komponentiem.</span><span class="sxs-lookup"><span data-stu-id="5e003-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="5e003-122">Datu elementi rēķina virsrakstam, rēķina rindām un rēķina pielikumiem</span><span class="sxs-lookup"><span data-stu-id="5e003-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="5e003-123">Izņēmumu apstrāde rēķiniem</span><span class="sxs-lookup"><span data-stu-id="5e003-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="5e003-124">Līdzās novietotu pielikumu skatītājs rēķinos</span><span class="sxs-lookup"><span data-stu-id="5e003-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="5e003-125">Atlikusī daļa šajā tēmā veltīta detalizētiem aprakstiem par šiem risinājuma komponentiem.</span><span class="sxs-lookup"><span data-stu-id="5e003-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="5e003-126">Datu elementi</span><span class="sxs-lookup"><span data-stu-id="5e003-126">Data entities</span></span>

<span data-ttu-id="5e003-127">Datu pakotne ir darba vienība, kas ir jānosūta, lai varētu izveidot rēķina virsrakstus, rēķina rindas un rēķina pielikumus.</span><span class="sxs-lookup"><span data-stu-id="5e003-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="5e003-128">Artefaktiem, kas veido datu pakotni, ir izmantoti tālāk norādītie datu elementi.</span><span class="sxs-lookup"><span data-stu-id="5e003-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="5e003-129">Kreditora rēķina virsraksts</span><span class="sxs-lookup"><span data-stu-id="5e003-129">Vendor invoice header</span></span>
+ <span data-ttu-id="5e003-130">Kreditora rēķina rinda</span><span class="sxs-lookup"><span data-stu-id="5e003-130">Vendor invoice line</span></span>
+ <span data-ttu-id="5e003-131">Kreditora rēķina dokumenta pielikums</span><span class="sxs-lookup"><span data-stu-id="5e003-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="5e003-132">Kreditora rēķina dokumenta pielikums ir jauns datu elements, kas ir ieviests kā daļa no šī līdzekļa.</span><span class="sxs-lookup"><span data-stu-id="5e003-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="5e003-133">Kreditora rēķina virsraksta elements ir modificēts tā, lai tas atbalstītu pielikumus.</span><span class="sxs-lookup"><span data-stu-id="5e003-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="5e003-134">Kreditora rēķina rindas elements nav modificēts šim līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="5e003-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="5e003-135">Detalizētu informāciju par datu pakotnēm skatiet [datu pārvaldības pārskatā](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="5e003-135">For detailed information about data packages, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="5e003-136">Informāciju, kā izveidot datu pakotnes, izmantojot datu pārvaldības darbvietu, skatiet [datu pakotņu apstrāde un patērēšana Dynamics 365 Finance and Operations programmu risinājumā](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="5e003-136">For information about how to create data packages using the data management workspace, see [Process and consume data packages in Dynamics 365 Finance and Operations apps solution](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span></span>

<span data-ttu-id="5e003-137">Lai ātri ģenerētu testa datus, kas ietver rēķinus un pielikumus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5e003-137">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="5e003-138">Pierakstieties savā instancē.</span><span class="sxs-lookup"><span data-stu-id="5e003-138">Sign in to your instance.</span></span>
1. <span data-ttu-id="5e003-139">Dodieties uz **Kreditori** > **Rēķini** > **Gaidošie kreditoru rēķini**.</span><span class="sxs-lookup"><span data-stu-id="5e003-139">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="5e003-140">Izveidojiet rēķinus ar rindām un pielikumiem.</span><span class="sxs-lookup"><span data-stu-id="5e003-140">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e003-141">Pielikumiem ir jābūt virsraksta pielikumiem.</span><span class="sxs-lookup"><span data-stu-id="5e003-141">The attachments must be header attachments.</span></span> <span data-ttu-id="5e003-142">Pašlaik elements Kreditora rēķina dokumenta pielikums neatbalsta rindas pielikumus.</span><span class="sxs-lookup"><span data-stu-id="5e003-142">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="5e003-143">Atveriet darbvietu **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="5e003-143">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="5e003-144">Izveidojiet eksportēšanas darbu, kas ietver elementus Kreditora rēķina virsraksts, Kreditora rēķina rinda un Kreditora rēķina dokumenta pielikums.</span><span class="sxs-lookup"><span data-stu-id="5e003-144">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="5e003-145">Eksportējiet datus.</span><span class="sxs-lookup"><span data-stu-id="5e003-145">Export the data.</span></span>
1. <span data-ttu-id="5e003-146">Lejupielādējiet eksportētos datus kā pakotni.</span><span class="sxs-lookup"><span data-stu-id="5e003-146">Download the exported data as a package.</span></span> <span data-ttu-id="5e003-147">Tagad pakotni varat izmantot datu importēšanai mērķa instancēs testēšanas nolūkos.</span><span class="sxs-lookup"><span data-stu-id="5e003-147">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="5e003-148">Juridiskās personas noteikšana rēķinam</span><span class="sxs-lookup"><span data-stu-id="5e003-148">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="5e003-149">Rēķini, kas tiek importēti, izmantojot datu pakotnes, ar juridisko personu, kam tie pieder, var būt saistīti divos veidos.</span><span class="sxs-lookup"><span data-stu-id="5e003-149">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="5e003-150">Importēšanas darbs, kas apstrādā rēķinu, importē to tajā pašā uzņēmumā, kurā darbs tika plānots darbvietā **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="5e003-150">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="5e003-151">Citiem vārdiem sakot, darba uzņēmums nosaka uzņēmumu, kam pieder rēķins.</span><span class="sxs-lookup"><span data-stu-id="5e003-151">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="5e003-152">Kad datu pakotne, kas ietver rēķinus, ir nosūtīta uz programmu Finance, izsaucējs (t.i., integrācijas programma, kas darbojas ārpus Finance) var HTTP pieprasījumā skaidri norādīt uzņēmuma ID.</span><span class="sxs-lookup"><span data-stu-id="5e003-152">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="5e003-153">Šajā gadījumā uzņēmuma konteksts, kurā apstrādes darbs tiek izpildīts programmā Finance, tiek ignorēts, un rēķini tiek importēti uzņēmumā, kas tika nodots, izmantojot HTTP pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="5e003-153">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="5e003-154">Šī izturēšanās ir standarta datu pārvaldības izturēšanās.</span><span class="sxs-lookup"><span data-stu-id="5e003-154">This behavior is standard data management behavior.</span></span> <span data-ttu-id="5e003-155">Tā ir izskaidrota šeit saistībā ar rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="5e003-155">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="5e003-156">Izņēmumu apstrāde</span><span class="sxs-lookup"><span data-stu-id="5e003-156">Exception processing</span></span>

<span data-ttu-id="5e003-157">Scenārijos, kuros kreditora rēķini programmatūrā Finance and Operations nonāk, izmantojot integrāciju, ir nepieciešams viegls veids, kā kreditoru grupas dalībniekam apstrādāt izņēmumus vai neizdevušos rēķinus un izveidot gaidošos rēķinus no rēķiniem, kas neizdevās.</span><span class="sxs-lookup"><span data-stu-id="5e003-157">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="5e003-158">Šī izņēmumu apstrāde kreditoru rēķiniem tagad ir daļa no Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5e003-158">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="5e003-159">Izņēmumu saraksta lapa</span><span class="sxs-lookup"><span data-stu-id="5e003-159">Exceptions list page</span></span>

<span data-ttu-id="5e003-160">Jaunā rēķinu izņēmumu saraksta lapa ir pieejama šeit: **Kreditori** > **Rēķini** > **Importēšanas kļūmes** > **Kreditoru rēķini, kuru importēšana bija nesekmīga**.</span><span class="sxs-lookup"><span data-stu-id="5e003-160">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="5e003-161">Šajā lapā ir parādīti visi kreditora rēķina virsraksta ieraksti no datu elementa Kreditora rēķina virsraksts izstādīšanas tabulas.</span><span class="sxs-lookup"><span data-stu-id="5e003-161">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="5e003-162">Ņemiet vērā, ka tos pašus ierakstus varat skatīt no darbvietas **Datu pārvaldība**, kurā varat arī veikt tās pašas darbības, kas ir nodrošinātas izņēmumu apstrādes līdzeklī.</span><span class="sxs-lookup"><span data-stu-id="5e003-162">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="5e003-163">Tomēr izņēmumu apstrādes līdzekļa nodrošinātais lietotāja interfeiss ir optimizēts funkcionālajam lietotājam.</span><span class="sxs-lookup"><span data-stu-id="5e003-163">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Izņēmumu saraksta lapa](media/vendor_invoice_automation_02.png)

<span data-ttu-id="5e003-165">Šajā saraksta lapā ir tālāk norādītie lauki, kas tajā nonāk ar plūsmu.</span><span class="sxs-lookup"><span data-stu-id="5e003-165">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="5e003-166">**Uzņēmums** — uzņēmums, kam pieder rēķins</span><span class="sxs-lookup"><span data-stu-id="5e003-166">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="5e003-167">**Kļūdas ziņojums** — kļūdas ziņojums, ko sniedz datu pārvaldības struktūra, lai izskaidrotu, kādēļ nevarēja izveidot rēķinu</span><span class="sxs-lookup"><span data-stu-id="5e003-167">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="5e003-168">**Numurs** — rēķina numurs</span><span class="sxs-lookup"><span data-stu-id="5e003-168">**Number** – The invoice number</span></span>
+ <span data-ttu-id="5e003-169">**Rēķina konts**</span><span class="sxs-lookup"><span data-stu-id="5e003-169">**Invoice account**</span></span>
+ <span data-ttu-id="5e003-170">**Nosaukums** — kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="5e003-170">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="5e003-171">**Kreditora konts**</span><span class="sxs-lookup"><span data-stu-id="5e003-171">**Vendor account**</span></span>
+ <span data-ttu-id="5e003-172">**Pirkšanas pasūtījums** — rēķina pirkšanas pasūtījuma (PP) numurs</span><span class="sxs-lookup"><span data-stu-id="5e003-172">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="5e003-173">**Grāmatošanas datums**</span><span class="sxs-lookup"><span data-stu-id="5e003-173">**Posting date**</span></span>
+ <span data-ttu-id="5e003-174">**Rēķina datums**</span><span class="sxs-lookup"><span data-stu-id="5e003-174">**Invoice date**</span></span>
+ <span data-ttu-id="5e003-175">**Rēķina apraksts**</span><span class="sxs-lookup"><span data-stu-id="5e003-175">**Invoice description**</span></span>
+ <span data-ttu-id="5e003-176">**Valūta**</span><span class="sxs-lookup"><span data-stu-id="5e003-176">**Currency**</span></span>
+ <span data-ttu-id="5e003-177">**Žurnāls**</span><span class="sxs-lookup"><span data-stu-id="5e003-177">**Log**</span></span>
+ <span data-ttu-id="5e003-178">**Rindas atsauce** — identifikators, kas ir no ārējās sistēmas</span><span class="sxs-lookup"><span data-stu-id="5e003-178">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e003-179">Rindas atsauce nav rēķina ID.</span><span class="sxs-lookup"><span data-stu-id="5e003-179">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="5e003-180">Šajā saraksta lapā ir arī priekšskatījuma rūts, kuru var izmantot tālāk norādītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="5e003-180">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="5e003-181">Skatiet visu kļūdas ziņojumu, lai jums nebūtu jāizvērš kolonna **Kļūdas ziņojums** režģī.</span><span class="sxs-lookup"><span data-stu-id="5e003-181">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="5e003-182">Skatiet visu rēķina pielikumu sarakstu, ja rēķinam tādi ir.</span><span class="sxs-lookup"><span data-stu-id="5e003-182">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="5e003-183">Saraksta lapa atbalsta arī tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5e003-183">The list page supports the following actions:</span></span>

+ <span data-ttu-id="5e003-184">**Rediģēt** — atveriet izņēmumu ierakstu rediģēšanas režīmā, lai labotu problēmas.</span><span class="sxs-lookup"><span data-stu-id="5e003-184">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="5e003-185">**Opcijas** — piekļūstiet standarta opcijām, kas ir pieejamas saraksta lapās.</span><span class="sxs-lookup"><span data-stu-id="5e003-185">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="5e003-186">Varat izmantot opciju **Pievienot darbvietai**, lai izņēmumu saraksta lapu piespraustu savai darbvietai kā sarakstu vai elementu.</span><span class="sxs-lookup"><span data-stu-id="5e003-186">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="5e003-187">Detalizētas informācijas par izņēmumu lapa</span><span class="sxs-lookup"><span data-stu-id="5e003-187">Exception details page</span></span>

<span data-ttu-id="5e003-188">Kad sākat rediģēšanas režīmu, tiek parādīta detalizētās informācijas par izņēmumu lapa rēķinam, kuram ir problēmas.</span><span class="sxs-lookup"><span data-stu-id="5e003-188">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="5e003-189">Ja rēķinam ir pielikumi, rēķins un noklusējuma pielikums tiek rādīti līdzās detalizētās informācijas par izņēmumu lapā.</span><span class="sxs-lookup"><span data-stu-id="5e003-189">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Detalizētas informācijas par izņēmumu lapa](media/vendor_invoice_automation_03.png)

<span data-ttu-id="5e003-191">Iepriekšējā attēlā ienākošajam kreditora rēķina virsrakstam nebija nevienas rindas.</span><span class="sxs-lookup"><span data-stu-id="5e003-191">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="5e003-192">Tāpēc rindu sadaļa ir tukša.</span><span class="sxs-lookup"><span data-stu-id="5e003-192">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="5e003-193">Detalizētās informācijas par izņēmumu lapa atbalsta tālāk norādīto operāciju.</span><span class="sxs-lookup"><span data-stu-id="5e003-193">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="5e003-194">**Izveidot gaidošu rēķinu** — kad būsit labojis problēmas rēķinā kā daļu no izņēmumu apstrādes, varat noklikšķināt uz šīs pogas, lai izveidotu gaidošo rēķinu.</span><span class="sxs-lookup"><span data-stu-id="5e003-194">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="5e003-195">Gaidošo rēķinu izveide notiek fonā (kā asinhrona operācija).</span><span class="sxs-lookup"><span data-stu-id="5e003-195">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="5e003-196">Koplietoto pakalpojumu izņēmumu apstrāde salīdzinājumā ar apstrādi, kuras pamatā ir organizācija</span><span class="sxs-lookup"><span data-stu-id="5e003-196">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="5e003-197">Izņēmumu saraksta lapa atbalsta standarta drošības struktūras, kuras darbvieta **Datu pārvaldība** atbalsta izstādīšanas ierakstu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="5e003-197">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="5e003-198">Rēķinu importēšanas darbu var nodrošināt tālāk norādītajos veidos.</span><span class="sxs-lookup"><span data-stu-id="5e003-198">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="5e003-199">Pēc lietotāja lomas</span><span class="sxs-lookup"><span data-stu-id="5e003-199">By user role</span></span>
+ <span data-ttu-id="5e003-200">Pēc lietotāja</span><span class="sxs-lookup"><span data-stu-id="5e003-200">By user</span></span>
+ <span data-ttu-id="5e003-201">Pēc juridiskās personas</span><span class="sxs-lookup"><span data-stu-id="5e003-201">By legal entity</span></span>

![Importēšanas darbs, kas ir nodrošināts pēc lietotāja lomas un juridiskās personas](media/vendor_invoice_automation_04.png)

<span data-ttu-id="5e003-203">Ja rēķina importēšanas darbam ir konfigurēta drošība, izņēmumu saraksta lapa respektē šos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="5e003-203">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="5e003-204">Lietotāji varēs redzēt tikai tos rēķinu izņēmumu ierakstus, ko šis iestatījums ļauj viņiem skatīt.</span><span class="sxs-lookup"><span data-stu-id="5e003-204">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="5e003-205">Piemēram, uzņēmums Contoso ir izlēmis apstrādāt rēķinu izņēmumus pēc juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="5e003-205">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="5e003-206">Tādēļ drošība rēķina importēšanas darbā ir konfigurēta tā, lai lietotājs juridiskajā personā A varētu redzēt tikai juridiskās personas A rēķinu izņēmumus, savukārt lietotājs juridiskajā personā B varētu redzēt tikai juridiskās personas B izņēmumus. Šis iestatījums rēķinu izņēmumu pārvaldībai nodrošina pienākumu sadali.</span><span class="sxs-lookup"><span data-stu-id="5e003-206">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="5e003-207">Contoso var arī izlemt nelietot nekādu drošību, lai tie paši lietotāji varētu apstrādāt rēķinu izņēmumus visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="5e003-207">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="5e003-208">Šis iestatījums rēķinu izņēmumu pārvaldībai nodrošina koplietoto pakalpojumu scenāriju.</span><span class="sxs-lookup"><span data-stu-id="5e003-208">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="5e003-209">Līdzās novietotu pielikumu skatītājs</span><span class="sxs-lookup"><span data-stu-id="5e003-209">Side-by-side attachment viewer</span></span>

<span data-ttu-id="5e003-210">Lai palīdzētu jums viegli skatīt kreditoru rēķinu pielikumus, tālāk norādītajās lapās, kas tiek izmantotas rēķinu apstrādes procesā, tagad ir pieejams pielikumu skatītājs.</span><span class="sxs-lookup"><span data-stu-id="5e003-210">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="5e003-211">**Izņēmumu apstrāde**</span><span class="sxs-lookup"><span data-stu-id="5e003-211">**Exception handling**</span></span>
+ <span data-ttu-id="5e003-212">Lapa **Gaidošie kreditoru rēķini** (pieejama arī rēķinu pārskatīšanas procesā)</span><span class="sxs-lookup"><span data-stu-id="5e003-212">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="5e003-213">Uzziņu lapa **Rēķinu žurnāls** (grāmatotajiem rēķiniem)</span><span class="sxs-lookup"><span data-stu-id="5e003-213">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="5e003-214">Tālāk norādīta galvenā funkcionalitāte, ko nodrošina pielikumu skatītājs.</span><span class="sxs-lookup"><span data-stu-id="5e003-214">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="5e003-215">Skatiet visus pielikumu tipus, ko atbalsta dokumentu pārvaldība (failus, attēlus, vietrāžus URL un piezīmes).</span><span class="sxs-lookup"><span data-stu-id="5e003-215">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="5e003-216">Skatiet vairāklapu TIFF failus.</span><span class="sxs-lookup"><span data-stu-id="5e003-216">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="5e003-217">Veiciet tālāk norādītās darbības attēlu failiem.</span><span class="sxs-lookup"><span data-stu-id="5e003-217">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="5e003-218">Iezīmējiet attēla daļas.</span><span class="sxs-lookup"><span data-stu-id="5e003-218">Highlight parts of the image.</span></span>
  + <span data-ttu-id="5e003-219">Bloķējiet attēla daļas.</span><span class="sxs-lookup"><span data-stu-id="5e003-219">Block parts of the image.</span></span>
  + <span data-ttu-id="5e003-220">Pievienojiet attēlam anotācijas.</span><span class="sxs-lookup"><span data-stu-id="5e003-220">Add annotations to the image.</span></span>
  + <span data-ttu-id="5e003-221">Tuviniet un tāliniet attēlu.</span><span class="sxs-lookup"><span data-stu-id="5e003-221">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="5e003-222">Bīdiet attēlu.</span><span class="sxs-lookup"><span data-stu-id="5e003-222">Pan the image.</span></span>
  + <span data-ttu-id="5e003-223">Atsauciet darbības un atceltiem atsaukšanu tām.</span><span class="sxs-lookup"><span data-stu-id="5e003-223">Undo and redo actions.</span></span>
  + <span data-ttu-id="5e003-224">Pielāgojiet attēla lielumu.</span><span class="sxs-lookup"><span data-stu-id="5e003-224">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="5e003-225">Šīs darbības ir pieejama tikai attēlu failiem (JPEG, TIFF, PNG u.c.).</span><span class="sxs-lookup"><span data-stu-id="5e003-225">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="5e003-226">Visas izmaiņas, ko veicat attēlā, izmantojot šīs darbības, tiek saglabātas attēla failā.</span><span class="sxs-lookup"><span data-stu-id="5e003-226">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="5e003-227">Pašlaik pielikumu skatītājs neietver versiju izveides un auditēšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="5e003-227">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="5e003-228">Noklusējuma pielikums</span><span class="sxs-lookup"><span data-stu-id="5e003-228">Default attachment</span></span>

<span data-ttu-id="5e003-229">Ja kreditora rēķinā ir vairāk nekā viens pielikums, lapā **Pielikumi** vienu no dokumentiem varat iestatīt kā noklusējuma pielikumu.</span><span class="sxs-lookup"><span data-stu-id="5e003-229">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="5e003-230">Opcija **Ir noklusējuma pielikums** ir jauna opcija, kas tika pievienota kā daļa no šī līdzekļa.</span><span class="sxs-lookup"><span data-stu-id="5e003-230">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="5e003-231">Šī opcija ir parādīta arī datu elementā Kreditora rēķina dokumenta pielikums.</span><span class="sxs-lookup"><span data-stu-id="5e003-231">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="5e003-232">Tādējādi noklusējuma pielikumu var iestatīt, izmantojot integrācijas.</span><span class="sxs-lookup"><span data-stu-id="5e003-232">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="5e003-233">Kā noklusējuma pielikumu var iestatīt tikai vienu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5e003-233">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="5e003-234">Kad dokumentu esat iestatījis kā noklusējuma pielikumu, atverot rēķinu, tas tiek automātiski parādīts pielikumu skatītājā.</span><span class="sxs-lookup"><span data-stu-id="5e003-234">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="5e003-235">Ja kā noklusējuma pielikumu neiestatāt nevienu dokumentu, atverot rēķinu, pielikumu skatītājs neparāda nevienu pielikumu.</span><span class="sxs-lookup"><span data-stu-id="5e003-235">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="5e003-236">Rēķinu pielikumu rādīšana/paslēpšana</span><span class="sxs-lookup"><span data-stu-id="5e003-236">Show/hide invoice attachments</span></span>

<span data-ttu-id="5e003-237">Izmantojot uzziņu lapās **Izņēmumu apstrāde**, **Gaidošs rēķins** un **Rēķinu žurnāls** pieejamo jauno pogu, varat rādīt vai paslēpt pielikumu skatītāju.</span><span class="sxs-lookup"><span data-stu-id="5e003-237">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="5e003-238">Drošība</span><span class="sxs-lookup"><span data-stu-id="5e003-238">Security</span></span>

<span data-ttu-id="5e003-239">Tālāk norādītās pielikumu skatītāja darbības tiek kontrolētas, izmantojot no lomas atkarīgu drošību.</span><span class="sxs-lookup"><span data-stu-id="5e003-239">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="5e003-240">Iezīmēšana</span><span class="sxs-lookup"><span data-stu-id="5e003-240">Highlighting</span></span>
+ <span data-ttu-id="5e003-241">Bloķēts</span><span class="sxs-lookup"><span data-stu-id="5e003-241">Block</span></span>
+ <span data-ttu-id="5e003-242">Anotēšana</span><span class="sxs-lookup"><span data-stu-id="5e003-242">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="5e003-243">Lapa Gaidošie kreditoru rēķini</span><span class="sxs-lookup"><span data-stu-id="5e003-243">Pending vendor invoices page</span></span>

<span data-ttu-id="5e003-244">Tālāk norādītās privilēģijas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi vai lasīšanas/rakstīšanas piekļuvi iezīmēšanas, bloķēšanas un anotēšanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="5e003-244">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="5e003-245">**Uzturēt kreditora rēķina attēlu** — šī privilēģija nodrošina lasīšanas/rakstīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="5e003-245">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="5e003-246">**Skatīt kreditora rēķina attēlu** — šī privilēģija nodrošina tikai lasīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="5e003-246">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="5e003-247">Tālāk norādītie pienākumi pielikumu skatītājam nodrošina tikai lasīšanas vai lasīšanas/rakstīšanas piekļuvi tālāk aprakstītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="5e003-247">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="5e003-248">**Uzturēt kreditoru rēķinus** — šim pienākumam ir piešķirta privilēģija Uzturēt kreditora rēķina attēlu.</span><span class="sxs-lookup"><span data-stu-id="5e003-248">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="5e003-249">**Iegūt informāciju par kreditora rēķina statusu** — šim pienākumam ir piešķirta privilēģija Skatīt kreditora rēķina attēlu.</span><span class="sxs-lookup"><span data-stu-id="5e003-249">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="5e003-250">Tālāk norādītās lomas pielikumu skatītājam nodrošina tikai lasīšanas vai lasīšanas/rakstīšanas piekļuvi tālāk aprakstītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="5e003-250">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="5e003-251">**Kreditoru darbinieks** un **Kreditoru vadītājs** — šīm lomām ir piešķirts pienākums Uzturēt kreditoru rēķinus.</span><span class="sxs-lookup"><span data-stu-id="5e003-251">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="5e003-252">**Kreditoru darbinieks**, **Kreditoru vadītājs**, **Darbinieks, kas ir atbildīgs par kreditoru centralizētajiem maksājumiem**, un **Darbinieks, kas ir atbildīgs par kreditoru maksājumiem** — šīm lomām ir piešķirts pienākums Iegūt informāciju par kreditora rēķina statusu.</span><span class="sxs-lookup"><span data-stu-id="5e003-252">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="5e003-253">Detalizētas informācijas par rēķina izņēmumu lapa</span><span class="sxs-lookup"><span data-stu-id="5e003-253">Invoice exception details page</span></span>

<span data-ttu-id="5e003-254">Tālāk norādītās privilēģijas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi vai lasīšanas/rakstīšanas piekļuvi iezīmēšanas, bloķēšanas un anotēšanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="5e003-254">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="5e003-255">Šajā sadaļā minētās komplektācijā iekļautās lomas rēķina attēliem pielikumu skatītājā nodrošina tikai lasīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="5e003-255">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="5e003-256">Ja lomai ir jābūt arī rakstīšanas piekļuvei attēliem, varat piešķirt rakstīšanas piekļuvi šai lomai, izmantojot šeit aprakstīto privilēģiju un pienākumu.</span><span class="sxs-lookup"><span data-stu-id="5e003-256">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="5e003-257">**Uzturēt kreditora rēķina virsraksta elementa attēlu** — šī privilēģija rēķina attēliem pielikumu skatītājā nodrošina lasīšanas/rakstīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="5e003-257">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="5e003-258">**Skatīt kreditora rēķina virsraksta elementa attēlu** — šī privilēģija rēķina attēlam pielikumu skatītājā nodrošina tikai lasīšanas piekļuvi.</span><span class="sxs-lookup"><span data-stu-id="5e003-258">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="5e003-259">Tālāk norādītie pienākumi pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi tālāk aprakstītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="5e003-259">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="5e003-260">**Uzturēt kreditoru rēķinus** — šim pienākumam ir piešķirta privilēģija Uzturēt kreditora rēķina virsraksta elementa attēlu.</span><span class="sxs-lookup"><span data-stu-id="5e003-260">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="5e003-261">Tālāk norādītās lomas pielikumu skatītājam nodrošina tikai lasīšanas piekļuvi tālāk aprakstītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="5e003-261">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="5e003-262">**Kreditoru darbinieks** un **Kreditoru vadītājs** — šīm lomām ir piešķirts pienākums Uzturēt kreditoru rēķinus.</span><span class="sxs-lookup"><span data-stu-id="5e003-262">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="5e003-263">Pēc noklusējuma, ja lietotāja loma sniedz rediģēšanas tiesības jebkurā lapā, lietotājam rediģēšanas tiesības būs arī pielikumu skatītājā iezīmēšanas, bloķēšanas un anotēšanas darbībām.</span><span class="sxs-lookup"><span data-stu-id="5e003-263">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="5e003-264">Tomēr, ja pastāv scenāriji, kuros noteiktai lomai ir nepieciešamas rediģēšanas tiesības lapā, bet ne pielikumu skatītājā, to var panākt, izmantojot atbilstošās privilēģijas no iepriekšējā saraksta.</span><span class="sxs-lookup"><span data-stu-id="5e003-264">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>
