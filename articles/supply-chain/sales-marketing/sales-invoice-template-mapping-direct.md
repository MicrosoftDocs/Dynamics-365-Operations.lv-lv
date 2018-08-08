---
title: "Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations pieejamo pārdošanas rēķinu galveņu un rindu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 70fc842463254b02d812447f93970a9da676057d
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="2849d-103">Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="2849d-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2849d-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations pieejamo pārdošanas rēķinu galveņu un rindu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for sales.</span><span class="sxs-lookup"><span data-stu-id="2849d-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="2849d-105">Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="2849d-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="2849d-106">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs.</span><span class="sxs-lookup"><span data-stu-id="2849d-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="2849d-107">Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="2849d-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="2849d-108">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="2849d-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="2849d-109">[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="2849d-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="2849d-110">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="2849d-110">Templates and tasks</span></span>

<span data-ttu-id="2849d-111">Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="2849d-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="2849d-112">Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="2849d-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="2849d-113">Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu sinhronizēšanai ar programmu Sales tiek izmantota tālāk norādītā veidne un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="2849d-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="2849d-114">**Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas rēķini (no Fin and Ops uz Sales) — tieši</span><span class="sxs-lookup"><span data-stu-id="2849d-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="2849d-115">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="2849d-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="2849d-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="2849d-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="2849d-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="2849d-117">SalesInvoiceLine</span></span>

<span data-ttu-id="2849d-118">Lai varētu veikt pārdošanas rēķinu galveņu un rindu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="2849d-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="2849d-119">Preces (no Fin and Ops uz Sales) — tieši</span><span class="sxs-lookup"><span data-stu-id="2849d-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="2849d-120">Konti (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)</span><span class="sxs-lookup"><span data-stu-id="2849d-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="2849d-121">Kontaktpersonas (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)</span><span class="sxs-lookup"><span data-stu-id="2849d-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="2849d-122">Pārdošanas pasūtījuma galvene un rindas (no Fin and Ops uz Sales) — tieši</span><span class="sxs-lookup"><span data-stu-id="2849d-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="2849d-123">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="2849d-123">Entity set</span></span>

| <span data-ttu-id="2849d-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2849d-124">Finance and Operations</span></span>                               | <span data-ttu-id="2849d-125">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="2849d-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="2849d-126">Ārēji uzturētu debitora pārdošanas rēķinu virsraksti</span><span class="sxs-lookup"><span data-stu-id="2849d-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="2849d-127">Rēķini</span><span class="sxs-lookup"><span data-stu-id="2849d-127">Invoices</span></span>       |
| <span data-ttu-id="2849d-128">Ārēji uzturētu debitora pārdošanas rēķinu rindas</span><span class="sxs-lookup"><span data-stu-id="2849d-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="2849d-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="2849d-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="2849d-130">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="2849d-130">Entity flow</span></span>

<span data-ttu-id="2849d-131">Pārdošanas rēķini tiek izveidoti programmā Finance and Operations un sinhronizēti ar Sales.</span><span class="sxs-lookup"><span data-stu-id="2849d-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="2849d-132">Pašlaik programmā Finance and Operations ietverto datu sinhronizēšanā ar programmu Sales netiek ietverti nodokļi, kas ir saistīti ar pārdošanas rēķina galvenes maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="2849d-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="2849d-133">Programmā Sales netiek atbalstīta nodokļu informācija galvenes līmenī.</span><span class="sxs-lookup"><span data-stu-id="2849d-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="2849d-134">Taču ar rindas līmeņa maksājumiem saistītais nodoklis tiek ietverts sinhronizēšanā.</span><span class="sxs-lookup"><span data-stu-id="2849d-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2849d-135">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="2849d-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="2849d-136">Elementam **Rēķins** ir pievienots lauks **Rēķina numurs**, un tas ir redzams lapā.</span><span class="sxs-lookup"><span data-stu-id="2849d-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="2849d-137">Lapā **Pārdošanas pasūtījums** ir paslēpta poga **Izveidot rēķinu**, jo rēķini tiks izveidoti programmā Finance and Operations un sinhronizēti ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="2849d-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="2849d-138">Lapu **Rēķins** nevar rediģēt, jo rēķini tiks sinhronizēti no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2849d-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="2849d-139">Kad saistītais rēķins programmā Finance and Operations ir sinhronizēts ar programmu Sales, lauka **Pārdošanas pasūtījuma statuss** vērtība tiek automātiski mainīta uz **Iekļauts rēķinā**.</span><span class="sxs-lookup"><span data-stu-id="2849d-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="2849d-140">Turklāt tā pārdošanas pasūtījuma īpašnieks, no kura tika izveidots rēķins, tiek piešķirts kā rēķina īpašnieks.</span><span class="sxs-lookup"><span data-stu-id="2849d-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="2849d-141">Tāpēc pārdošanas pasūtījuma īpašnieks var skatīt rēķinu.</span><span class="sxs-lookup"><span data-stu-id="2849d-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2849d-142">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="2849d-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="2849d-143">Pirms rēķinu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="2849d-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="2849d-144">Iestatīšana programmā Sales</span><span class="sxs-lookup"><span data-stu-id="2849d-144">Setup in Sales</span></span>

<span data-ttu-id="2849d-145">Pārejiet uz sadaļu **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="2849d-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="2849d-146">Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.</span><span class="sxs-lookup"><span data-stu-id="2849d-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="2849d-147">Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.</span><span class="sxs-lookup"><span data-stu-id="2849d-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="2849d-148">Iestatīšana datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="2849d-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="2849d-149">SalesInvoiceHeader uzdevums</span><span class="sxs-lookup"><span data-stu-id="2849d-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="2849d-150">Pārliecinieties, ka pastāv nepieciešamais kartējums no**InvoiceCountryRegionId** uz **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="2849d-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="2849d-151">Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni.</span><span class="sxs-lookup"><span data-stu-id="2849d-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="2849d-152">Lai varētu izveidot rēķinus programmā Sales, ir nepieciešams cenrādis.</span><span class="sxs-lookup"><span data-stu-id="2849d-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="2849d-153">Atjauniniet vienuma **pricelevelid.name \[cenrāža nosaukums\]** vērtību karti atbilstoši programmā Sales lietotajam cenrādim pēc valūtas.</span><span class="sxs-lookup"><span data-stu-id="2849d-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="2849d-154">Varat izmantot noklusējuma cenrādi vienai valūtai.</span><span class="sxs-lookup"><span data-stu-id="2849d-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="2849d-155">Ja jums ir cenrāži vairākās valūtās, varat izmantot vērtību karti.</span><span class="sxs-lookup"><span data-stu-id="2849d-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="2849d-156">Vienuma **pricelevelid.name \[cenrāža nosaukums\]** veidnes vērtība ir vērtību karte, kuras pamatā ir valūta ar iestatījumu USD = CRM Service ASV (paraugs).</span><span class="sxs-lookup"><span data-stu-id="2849d-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="2849d-157">SalesInvoiceLine uzdevums</span><span class="sxs-lookup"><span data-stu-id="2849d-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="2849d-158">Pārliecinieties, ka pastāv nepieciešamais vienuma **Mērvienība** kartējums.</span><span class="sxs-lookup"><span data-stu-id="2849d-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="2849d-159">Pārliecinieties, ka programmā Finance and Operations pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.</span><span class="sxs-lookup"><span data-stu-id="2849d-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="2849d-160">Kartējumam no **SalesUnitSymbol** uz **Quantity\_UOM** ir definēta veidnes vērtība ar vērtību karti.</span><span class="sxs-lookup"><span data-stu-id="2849d-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2849d-161">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="2849d-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="2849d-162">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="2849d-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="2849d-163">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="2849d-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="2849d-164">Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="2849d-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="2849d-165">Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2849d-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="2849d-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="2849d-166">SalesInvoiceHeader</span></span>

![Veidnes kartējums līdzeklī Datu integrācija](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="2849d-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="2849d-168">SalesInvoiceLine</span></span>

![Veidnes kartējums līdzeklī Datu integrācija](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="2849d-170">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="2849d-170">Related topics</span></span>

[<span data-ttu-id="2849d-171">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="2849d-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="2849d-172">Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2849d-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="2849d-173">Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="2849d-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="2849d-174">Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2849d-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="2849d-175">Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="2849d-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)







