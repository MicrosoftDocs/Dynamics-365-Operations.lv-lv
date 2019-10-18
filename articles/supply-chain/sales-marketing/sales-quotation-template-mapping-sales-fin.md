---
title: Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Supply Chain Management
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto pārdošanas piedāvājumu galvu un rindu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ddc81aa7ff462304cb6e22c919221217f7a1e019
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251251"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="ecd67-103">Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ecd67-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecd67-104">Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto pārdošanas piedāvājumu galvu un rindu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="ecd67-105">Pirms risinājuma No potenciāla klienta līdz skaidrai naudai lietošanas izlasiet rakstu [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="ecd67-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="ecd67-106">Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="ecd67-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="ecd67-107">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs.</span><span class="sxs-lookup"><span data-stu-id="ecd67-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="ecd67-108">Risinājuma ´No potenciālā klienta līdz skaidrai naudai´ veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="ecd67-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="ecd67-109">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="ecd67-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="ecd67-110">[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="ecd67-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="ecd67-111">Veidne un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="ecd67-111">Template and tasks</span></span>

<span data-ttu-id="ecd67-112">Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu sinhronizēšanai ar programmu Supply Chain Management tiek izmantota tālāk norādītā veidne un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="ecd67-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="ecd67-113">**Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas piedāvājumi (no Sales uz Supply Chain Management) — tieši</span><span class="sxs-lookup"><span data-stu-id="ecd67-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="ecd67-114">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="ecd67-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="ecd67-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="ecd67-115">QuoteHeader</span></span>
    - <span data-ttu-id="ecd67-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="ecd67-116">QuoteLine</span></span>

<span data-ttu-id="ecd67-117">Pirms pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanas ir jāveic tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="ecd67-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="ecd67-118">Preces (no Supply Chain Management uz Sales) – Tiešā</span><span class="sxs-lookup"><span data-stu-id="ecd67-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="ecd67-119">Konti (no Sales uz Supply Chain Management) - Tiešā (ja izmantots)</span><span class="sxs-lookup"><span data-stu-id="ecd67-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="ecd67-120">Kontaktpersonas Klientiem (no Sales uz Supply Chain Management) — Tiešā (ja izmantots)</span><span class="sxs-lookup"><span data-stu-id="ecd67-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="ecd67-121">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="ecd67-121">Entity set</span></span>

| <span data-ttu-id="ecd67-122">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="ecd67-122">Sales</span></span>        | <span data-ttu-id="ecd67-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ecd67-123">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="ecd67-124">Citāti</span><span class="sxs-lookup"><span data-stu-id="ecd67-124">Quotes</span></span>       | <span data-ttu-id="ecd67-125">CDS pārdošanas piedāvājuma galvene</span><span class="sxs-lookup"><span data-stu-id="ecd67-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="ecd67-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="ecd67-126">QuoteDetails</span></span> | <span data-ttu-id="ecd67-127">CDS pārdošanas piedāvājuma rindas</span><span class="sxs-lookup"><span data-stu-id="ecd67-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="ecd67-128">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="ecd67-128">Entity flow</span></span>

<span data-ttu-id="ecd67-129">Pārdošanas piedāvājumi tiek izveidoti programmā Sales un sinhronizēti ar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="ecd67-130">Pārdošanas piedāvājumi no Sales tiek sinhronizēti tikai tad, ja ir izpildīti tālāk norādītie nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="ecd67-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="ecd67-131">Visas pārdošanas piedāvājumā ietvertās piedāvātās preces ir ārēji uzturētas.</span><span class="sxs-lookup"><span data-stu-id="ecd67-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="ecd67-132">Pēc noklikšķināšanas uz **Aktivizēt piedāvājumu** pārdošanas piedāvājums ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="ecd67-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ecd67-133">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="ecd67-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="ecd67-134">Elementam **Piedāvājums** ir pievienots lauks **Ir tikai ārēji uzturētas preces**, lai pastāvīgi izsekotu to, vai pārdošanas piedāvājumā ir ietvertas tikai ārēji uzturētas preces.</span><span class="sxs-lookup"><span data-stu-id="ecd67-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="ecd67-135">Ja pārdošanas piedāvājumā ir tikai ārēji uzturētas preces, tās tiek uzturētas programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="ecd67-136">Šī darbība palīdz nodrošināt to, ka nemēģināt sinhronizēt pārdošanas piedāvājuma rindas, kurās ietvertās preces nav zināmas programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="ecd67-137">Visas pārdošanas piedāvājumā ietvertās piedāvātās preces tiek atjauninātas, izmantojot lauka **Ir tikai ārēji uzturētas preces** informāciju no pārdošanas piedāvājuma galvenes.</span><span class="sxs-lookup"><span data-stu-id="ecd67-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="ecd67-138">Šī informācija ir ietverta elementa **QuoteDetails** laukā **Piedāvājumā ir tikai ārēji uzturētas preces**.</span><span class="sxs-lookup"><span data-stu-id="ecd67-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="ecd67-139">Piedāvātajai precei var pievieno atlaidi, kas tiek sinhronizēta ar programmu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="ecd67-140">Galvenes lauki **Atlaide**, **Maksas** un **Nodokļi** tiek kontrolēti, izmantojot iestatījumus programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="ecd67-141">Pašlaik šie iestatījumi neatbalsta integrācijas kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="ecd67-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="ecd67-142">Pašlaik lauki **Cena**, **Atlaide**, **Maksa** un **Nodokļi** tiek uzturēti un apstrādāti programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="ecd67-143">Programmā Sales risinājums tālāk norādītos laukus pārveido par tikai lasāmiem, jo attiecīgās vērtības netiek sinhronizētas ar programmu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="ecd67-144">Tikai lasāmie lauki pārdošanas piedāvājuma galvenē: **Atlaide %**, **Atlaide** un **Vedmaksa**</span><span class="sxs-lookup"><span data-stu-id="ecd67-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="ecd67-145">Tikai lasāmie piedāvāto produktu lauki: **Nodoklis**</span><span class="sxs-lookup"><span data-stu-id="ecd67-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ecd67-146">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="ecd67-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="ecd67-147">Pirms pārdošanas piedāvājuma sinhronizēšanas ir svarīgi atjaunināt tālāk norādītos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="ecd67-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="ecd67-148">Iestatīšana programmā Sales</span><span class="sxs-lookup"><span data-stu-id="ecd67-148">Setup in Sales</span></span>

- <span data-ttu-id="ecd67-149">Pārliecinieties, ka darba grupai, kurai ir piešķirts ar Sales savienojumu kopu saistītais lietotājs, ir iestatītas vajadzīgās atļaujas.</span><span class="sxs-lookup"><span data-stu-id="ecd67-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="ecd67-150">Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuves atļauja, bet darba grupai nav administratora piekļuves atļaujas.</span><span class="sxs-lookup"><span data-stu-id="ecd67-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="ecd67-151">Ja darba grupai nav administratora piekļuves atļaujas, palaižot projektu līdzeklī Datu integrācija, saņemat kļūdas ziņojumu par to, ka trūkst galvenās darba grupas.</span><span class="sxs-lookup"><span data-stu-id="ecd67-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="ecd67-152">Lai iestatītu darba grupas atļaujas, pārejiet uz sadaļu **Iestatījumi** &gt; **Drošība** &gt; **Darba grupas** un atlasiet attiecīgo darba grupu.</span><span class="sxs-lookup"><span data-stu-id="ecd67-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="ecd67-153">Atlasiet **Pārvaldīt lomas** un pēc tam atlasiet lomu, kurai ir piešķirtas vajadzīgās atļaujas, piemēram, **Sistēmas administrators**.</span><span class="sxs-lookup"><span data-stu-id="ecd67-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="ecd67-154">Pārejiet uz sadaļu **Iestatījumi** &gt; **Administrēšana** &gt; **Sistēmas iestatījumi** &gt; **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="ecd67-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="ecd67-155">Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ecd67-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="ecd67-156">Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.</span><span class="sxs-lookup"><span data-stu-id="ecd67-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="ecd67-157">Iestatīšana datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="ecd67-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="ecd67-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="ecd67-158">QuoteHeader</span></span>

- <span data-ttu-id="ecd67-159">Pārliecinieties, ka pastāv nepieciešamais kartējums no **Shipto\_country** uz **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="ecd67-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="ecd67-160">Vērtību kartē varat definēt noklusējuma vērtību, kas tiek izmantota, ja ir atstāta tukša vērtība.</span><span class="sxs-lookup"><span data-stu-id="ecd67-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="ecd67-161">Vienkārši atstājiet kreiso pusi tukšu un labajā pusē iestatiet vajadzīgo valsti vai reģionu.</span><span class="sxs-lookup"><span data-stu-id="ecd67-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="ecd67-162">Tādējādi jums nav jāievada valsts vai reģions iekšzemes pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="ecd67-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="ecd67-163">Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni un kur tukšai vērtībai atbilst vērtība **ASV**.</span><span class="sxs-lookup"><span data-stu-id="ecd67-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="ecd67-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="ecd67-164">QuoteLine</span></span>

- <span data-ttu-id="ecd67-165">Pārliecinieties, ka nepieciešamā vienuma **SalesUnitSymbol** vērtību karte ir programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="ecd67-166">Pārliecinieties, ka programmā Sales ir definētas nepieciešamās vienības.</span><span class="sxs-lookup"><span data-stu-id="ecd67-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="ecd67-167">Kartējumam no **oumid.name** uz **SalesUnitSymbol** ir definēta veidnes vērtība ar vērtību karti.</span><span class="sxs-lookup"><span data-stu-id="ecd67-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="ecd67-168">Pēc izvēles varat pievienot tālāk norādītos kartējumus, lai palīdzētu nodrošināt pārdošanas piedāvājuma rindu importēšanu programmā Supply Chain Management gadījumos, ja nav pieejama debitora vai preces noklusējuma informācija.</span><span class="sxs-lookup"><span data-stu-id="ecd67-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="ecd67-169">**SiteId**— vieta ir jānorāda, lai programmā Supply Chain Management ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="ecd67-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="ecd67-170">Laukam **SiteId** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="ecd67-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="ecd67-171">**WarehouseId**— noliktava ir jānorāda, lai programmā Supply Chain Management apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="ecd67-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="ecd67-172">Laukam **WarehouseId** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="ecd67-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="ecd67-173">Veidnes kartēšana datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="ecd67-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="ecd67-174">Lauki **Atlaide**, **Maksas** un **Nodokļi** tiek kontrolēti, izmantojot saliktus iestatījumus programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="ecd67-175">Pašlaik šie iestatījumi neatbalsta integrācijas kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="ecd67-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="ecd67-176">Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** apstrādā programma Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ecd67-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="ecd67-177">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="ecd67-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="ecd67-178">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="ecd67-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="ecd67-179">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="ecd67-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="ecd67-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="ecd67-180">QuoteHeader</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="ecd67-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="ecd67-182">QuoteLine</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="ecd67-184">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="ecd67-184">Related topics</span></span>

[<span data-ttu-id="ecd67-185">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="ecd67-185">Prospect to cash</span></span>](prospect-to-cash.md)

