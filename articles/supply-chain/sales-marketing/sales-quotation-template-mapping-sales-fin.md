---
title: "Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Finance and Operations"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales pieejamo pārdošanas piedāvājumu galveņu un rindu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 97536c27dea113cc3c019473f22d1925e7617f8f
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="c3a92-103">Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c3a92-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c3a92-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales pieejamo pārdošanas piedāvājumu galveņu un rindu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="c3a92-105">Lai varētu lietot risinājumu No potenciāla klienta līdz skaidrai naudai, vispirms iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="c3a92-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="c3a92-106">Veidne un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="c3a92-106">Template and tasks</span></span>

<span data-ttu-id="c3a92-107">Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="c3a92-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="c3a92-108">**Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas piedāvājumi (no Sales uz Fin and Ops) — tieši</span><span class="sxs-lookup"><span data-stu-id="c3a92-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="c3a92-109">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="c3a92-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="c3a92-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="c3a92-110">QuoteHeader</span></span>
    - <span data-ttu-id="c3a92-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="c3a92-111">QuoteLine</span></span>

<span data-ttu-id="c3a92-112">Pirms pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanas ir jāveic tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="c3a92-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="c3a92-113">Preces (no Fin and Ops uz Sales) — tieši</span><span class="sxs-lookup"><span data-stu-id="c3a92-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="c3a92-114">Konti (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)</span><span class="sxs-lookup"><span data-stu-id="c3a92-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="c3a92-115">Kontaktpersonas kā debitori (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)</span><span class="sxs-lookup"><span data-stu-id="c3a92-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="c3a92-116">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="c3a92-116">Entity set</span></span>

| <span data-ttu-id="c3a92-117">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="c3a92-117">Sales</span></span>        | <span data-ttu-id="c3a92-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c3a92-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="c3a92-119">Citāti</span><span class="sxs-lookup"><span data-stu-id="c3a92-119">Quotes</span></span>       | <span data-ttu-id="c3a92-120">CDS pārdošanas piedāvājuma galvene</span><span class="sxs-lookup"><span data-stu-id="c3a92-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="c3a92-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="c3a92-121">QuoteDetails</span></span> | <span data-ttu-id="c3a92-122">CDS pārdošanas piedāvājuma rindas</span><span class="sxs-lookup"><span data-stu-id="c3a92-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="c3a92-123">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="c3a92-123">Entity flow</span></span>

<span data-ttu-id="c3a92-124">Pārdošanas piedāvājumi tiek izveidoti programmā Sales un sinhronizēti ar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="c3a92-125">Pārdošanas piedāvājumi no Sales tiek sinhronizēti tikai tad, ja ir izpildīti tālāk norādītie nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="c3a92-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="c3a92-126">Visas pārdošanas piedāvājumā ietvertās piedāvātās preces ir ārēji uzturētas.</span><span class="sxs-lookup"><span data-stu-id="c3a92-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="c3a92-127">Pēc noklikšķināšanas uz **Aktivizēt piedāvājumu** pārdošanas piedāvājums ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="c3a92-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c3a92-128">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="c3a92-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="c3a92-129">Elementam **Piedāvājums** ir pievienots lauks **Ir tikai ārēji uzturētas preces**, lai pastāvīgi izsekotu to, vai pārdošanas piedāvājumā ir ietvertas tikai ārēji uzturētas preces.</span><span class="sxs-lookup"><span data-stu-id="c3a92-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="c3a92-130">Ja pārdošanas piedāvājumā ir tikai ārēji uzturētas preces, tās tiek uzturētas programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="c3a92-131">Šī darbība palīdz nodrošināt to, ka nemēģināt sinhronizēt pārdošanas piedāvājuma rindas, kurās ietvertās preces nav zināmas programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="c3a92-132">Visas pārdošanas piedāvājumā ietvertās piedāvātās preces tiek atjauninātas, izmantojot lauka**Ir tikai ārēji uzturētas preces** informāciju no pārdošanas piedāvājuma galvenes.</span><span class="sxs-lookup"><span data-stu-id="c3a92-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="c3a92-133">Šī informācija ir ietverta elementa **QuoteDetails** laukā **Piedāvājumā ir tikai ārēji uzturētas preces**.</span><span class="sxs-lookup"><span data-stu-id="c3a92-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="c3a92-134">Piedāvātajai precei var pievieno atlaidi, kas tiek sinhronizēta ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="c3a92-135">Galvenes lauki **Atlaide**, **Maksas** un **Nodokļi** tiek kontrolēti, izmantojot iestatījumus programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="c3a92-136">Pašlaik šie iestatījumi neatbalsta integrācijas kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="c3a92-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="c3a92-137">Pašlaik lauki **Cena**, **Atlaide**, **Maksa** un **Nodokļi** tiek uzturēti un apstrādāti programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="c3a92-138">Programmā Sales risinājums tālāk norādītos laukus pārveido par tikai lasāmiem, jo attiecīgās vērtības netiek sinhronizētas ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="c3a92-139">Tikai lasāmie lauki pārdošanas piedāvājuma galvenē: **Atlaide %**, **Atlaide** un **Vedmaksa**</span><span class="sxs-lookup"><span data-stu-id="c3a92-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="c3a92-140">Tikai lasāmie piedāvāto produktu lauki: **Nodoklis**</span><span class="sxs-lookup"><span data-stu-id="c3a92-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c3a92-141">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="c3a92-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="c3a92-142">Pirms pārdošanas piedāvājuma sinhronizēšanas ir svarīgi atjaunināt tālāk norādītos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="c3a92-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="c3a92-143">Iestatīšana programmā Sales</span><span class="sxs-lookup"><span data-stu-id="c3a92-143">Setup in Sales</span></span>

- <span data-ttu-id="c3a92-144">Pārliecinieties, ka darba grupai, kurai ir piešķirts ar Sales savienojumu kopu saistītais lietotājs, ir iestatītas vajadzīgās atļaujas.</span><span class="sxs-lookup"><span data-stu-id="c3a92-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="c3a92-145">Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuves atļauja, bet darba grupai nav administratora piekļuves atļaujas.</span><span class="sxs-lookup"><span data-stu-id="c3a92-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="c3a92-146">Ja darba grupai nav administratora piekļuves atļaujas, palaižot projektu līdzeklī Datu integrācija, saņemat kļūdas ziņojumu par to, ka trūkst galvenās darba grupas.</span><span class="sxs-lookup"><span data-stu-id="c3a92-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="c3a92-147">Lai iestatītu darba grupas atļaujas, pārejiet uz sadaļu **Iestatījumi** &gt; **Drošība** &gt; **Darba grupas** un atlasiet attiecīgo darba grupu.</span><span class="sxs-lookup"><span data-stu-id="c3a92-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="c3a92-148">Atlasiet **Pārvaldīt lomas** un pēc tam atlasiet lomu, kurai ir piešķirtas vajadzīgās atļaujas, piemēram, **Sistēmas administrators**.</span><span class="sxs-lookup"><span data-stu-id="c3a92-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="c3a92-149">Pārejiet uz sadaļu **Iestatījumi** &gt; **Administrēšana** &gt; **Sistēmas iestatījumi** &gt; **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="c3a92-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="c3a92-150">Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c3a92-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="c3a92-151">Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.</span><span class="sxs-lookup"><span data-stu-id="c3a92-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="c3a92-152">Iestatīšana datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="c3a92-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="c3a92-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="c3a92-153">QuoteHeader</span></span>

- <span data-ttu-id="c3a92-154">Pārliecinieties, ka pastāv nepieciešamais kartējums no **Shipto\_country** uz **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="c3a92-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="c3a92-155">Vērtību kartē varat definēt noklusējuma vērtību, kas tiek izmantota, ja ir atstāta tukša vērtība.</span><span class="sxs-lookup"><span data-stu-id="c3a92-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="c3a92-156">Vienkārši atstājiet kreiso pusi tukšu un labajā pusē iestatiet vajadzīgo valsti vai reģionu.</span><span class="sxs-lookup"><span data-stu-id="c3a92-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="c3a92-157">Tādējādi jums nav jāievada valsts vai reģions iekšzemes pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="c3a92-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="c3a92-158">Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni un kur tukšai vērtībai atbilst vērtība **ASV**.</span><span class="sxs-lookup"><span data-stu-id="c3a92-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="c3a92-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="c3a92-159">QuoteLine</span></span>

- <span data-ttu-id="c3a92-160">Pārliecinieties, ka programmā Finance and Operations pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.</span><span class="sxs-lookup"><span data-stu-id="c3a92-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="c3a92-161">Pārliecinieties, ka programmā Sales ir definētas nepieciešamās vienības.</span><span class="sxs-lookup"><span data-stu-id="c3a92-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="c3a92-162">Kartējumam no **oumid.name** uz **SalesUnitSymbol** ir definēta veidnes vērtība ar vērtību karti.</span><span class="sxs-lookup"><span data-stu-id="c3a92-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="c3a92-163">Pēc izvēles varat pievienot tālāk norādītos kartējumus, lai palīdzētu nodrošināt pārdošanas piedāvājuma rindu importēšanu programmā Finance and Operations gadījumos, ja nav pieejama debitora vai preces noklusējuma informācija.</span><span class="sxs-lookup"><span data-stu-id="c3a92-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="c3a92-164">**SiteId** — vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="c3a92-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="c3a92-165">Laukam **SiteId** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="c3a92-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="c3a92-166">**WarehouseId** — noliktava ir jānorāda, lai programmā Finance and Operations apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="c3a92-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="c3a92-167">Laukam **WarehouseId** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="c3a92-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="c3a92-168">Veidnes kartēšana datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="c3a92-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="c3a92-169">Laukus **Atlaide**, **Maksas** un **Nodokļi** kontrolē kompleksi iestatījumi programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="c3a92-170">Pašlaik šie iestatījumi neatbalsta integrācijas kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="c3a92-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="c3a92-171">Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** apstrādā programma Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c3a92-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="c3a92-172">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="c3a92-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="c3a92-173">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="c3a92-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="c3a92-174">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="c3a92-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="c3a92-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="c3a92-175">QuoteHeader</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="c3a92-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="c3a92-177">QuoteLine</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="c3a92-179">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="c3a92-179">Related topics</span></span>

[<span data-ttu-id="c3a92-180">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="c3a92-180">Prospect to cash</span></span>](prospect-to-cash.md)


