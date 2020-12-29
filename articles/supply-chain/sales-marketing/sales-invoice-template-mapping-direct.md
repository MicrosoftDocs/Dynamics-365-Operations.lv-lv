---
title: Programmā Supply Chain Management ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto pārdošanas rēķinu galvu un rindu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6cbc4d86ac41d90480428ec5439d1360c4d67137
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432653"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="c8f4d-103">Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="c8f4d-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8f4d-104">Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto pārdošanas rēķinu galvu un rindu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="c8f4d-105">Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="c8f4d-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="c8f4d-106">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="c8f4d-107">Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="c8f4d-108">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="c8f4d-109">[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="c8f4d-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c8f4d-110">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="c8f4d-110">Templates and tasks</span></span>

<span data-ttu-id="c8f4d-111">Lai piekļūtu pieejamajām veidnēm, atveriet [Power Apps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="c8f4d-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="c8f4d-112">Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c8f4d-113">Programmā Supply Chain Management ietverto pārdošanas rēķinu galveņu un rindu sinhronizēšanai uz programmu Sale tiek izmantota tālāk norādītā veidne un pamata uzdevumi:</span><span class="sxs-lookup"><span data-stu-id="c8f4d-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="c8f4d-114">**Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas rēķini (no Fin and Ops uz Sales) — tieši</span><span class="sxs-lookup"><span data-stu-id="c8f4d-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="c8f4d-115">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="c8f4d-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="c8f4d-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="c8f4d-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="c8f4d-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="c8f4d-117">SalesInvoiceLine</span></span>

<span data-ttu-id="c8f4d-118">Lai varētu veikt pārdošanas rēķinu galveņu un rindu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="c8f4d-119">Preces (no Supply Chain Management uz Sales) – Tiešā</span><span class="sxs-lookup"><span data-stu-id="c8f4d-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="c8f4d-120">Konti (no Sales uz Supply Chain Management) - Tiešā (ja izmantots)</span><span class="sxs-lookup"><span data-stu-id="c8f4d-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="c8f4d-121">Kontaktpersonas (no Sales uz Supply Chain Management) - Tiešā (ja izmantots)</span><span class="sxs-lookup"><span data-stu-id="c8f4d-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="c8f4d-122">Pārdošanas pasūtījumu galvenes un rindas (no Supply Chain Management uz Sales) - Tiešā</span><span class="sxs-lookup"><span data-stu-id="c8f4d-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="c8f4d-123">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="c8f4d-123">Entity set</span></span>

| <span data-ttu-id="c8f4d-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c8f4d-124">Supply Chain Management</span></span>                              | <span data-ttu-id="c8f4d-125">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="c8f4d-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="c8f4d-126">Ārēji uzturētu debitora pārdošanas rēķinu virsraksti</span><span class="sxs-lookup"><span data-stu-id="c8f4d-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="c8f4d-127">Rēķini</span><span class="sxs-lookup"><span data-stu-id="c8f4d-127">Invoices</span></span>       |
| <span data-ttu-id="c8f4d-128">Ārēji uzturētu debitora pārdošanas rēķinu rindas</span><span class="sxs-lookup"><span data-stu-id="c8f4d-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="c8f4d-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="c8f4d-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c8f4d-130">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="c8f4d-130">Entity flow</span></span>

<span data-ttu-id="c8f4d-131">Pārdošanas rēķini tiek izveidoti programmatūrā Supply Chain Management un sinhronizēti ar Sales.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="c8f4d-132">Pašlaik programmā Finance and Operations ietverto datu sinhronizēšanā ar programmu Supply Chain Management netiek ietverti nodokļi, kas ir saistīti ar pārdošanas rēķina galvenes maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="c8f4d-133">Programmā Sales netiek atbalstīta nodokļu informācija galvenes līmenī.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="c8f4d-134">Taču ar rindas līmeņa maksājumiem saistītais nodoklis tiek ietverts sinhronizēšanā.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c8f4d-135">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="c8f4d-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="c8f4d-136">Elementam **Rēķins** ir pievienots lauks **Rēķina numurs**, un tas ir redzams lapā.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="c8f4d-137">Lapā **Pārdošanas pasūtījums** ir paslēpta poga **Izveidot rēķinu**, jo rēķini tiks izveidoti programmā Supply Chain Management un sinhronizēti ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="c8f4d-138">Lapu **Rēķins** nevar rediģēt, jo rēķini tiks sinhronizēti no programmas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="c8f4d-139">Kad saistītais rēķins programmatūrā Supply Chain Management ir sinhronizēts ar programmu Sales, lauka **Pārdošanas pasūtījuma statuss** vērtība tiek automātiski mainīta uz **Iekļauts rēķinā**.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="c8f4d-140">Turklāt tā pārdošanas pasūtījuma īpašnieks, no kura tika izveidots rēķins, tiek piešķirts kā rēķina īpašnieks.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="c8f4d-141">Tāpēc pārdošanas pasūtījuma īpašnieks var skatīt rēķinu.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c8f4d-142">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="c8f4d-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="c8f4d-143">Pirms rēķinu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="c8f4d-144">Iestatīšana programmā Sales</span><span class="sxs-lookup"><span data-stu-id="c8f4d-144">Setup in Sales</span></span>

<span data-ttu-id="c8f4d-145">Pārejiet uz sadaļu **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="c8f4d-146">Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="c8f4d-147">Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="c8f4d-148">Iestatīšana datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="c8f4d-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="c8f4d-149">SalesInvoiceHeader uzdevums</span><span class="sxs-lookup"><span data-stu-id="c8f4d-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="c8f4d-150">Pārliecinieties, ka pastāv nepieciešamais kartējums no **InvoiceCountryRegionId** uz **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="c8f4d-151">Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="c8f4d-152">Lai varētu izveidot rēķinus programmā Sales, ir nepieciešams cenrādis.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="c8f4d-153">Atjauniniet vienuma **pricelevelid.name \[cenrāža nosaukums\]** vērtību karti atbilstoši programmā Sales lietotajam cenrādim pēc valūtas.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="c8f4d-154">Varat izmantot noklusējuma cenrādi vienai valūtai.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="c8f4d-155">Ja jums ir cenrāži vairākās valūtās, varat izmantot vērtību karti.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="c8f4d-156">Vienuma **pricelevelid.name \[cenrāža nosaukums\]** veidnes vērtība ir vērtību karte, kuras pamatā ir valūta ar iestatījumu USD = CRM Service ASV (paraugs).</span><span class="sxs-lookup"><span data-stu-id="c8f4d-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="c8f4d-157">SalesInvoiceLine uzdevums</span><span class="sxs-lookup"><span data-stu-id="c8f4d-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="c8f4d-158">Pārliecinieties, ka pastāv nepieciešamais vienuma **Mērvienība** kartējums.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="c8f4d-159">Pārliecinieties, ka programmā Supply Chain Management pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="c8f4d-160">Kartējumam no **SalesUnitSymbol** uz **Quantity\_UOM** ir definēta veidnes vērtība ar vērtību karti.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c8f4d-161">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="c8f4d-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="c8f4d-162">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="c8f4d-163">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="c8f4d-164">Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="c8f4d-165">Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="c8f4d-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="c8f4d-166">SalesInvoiceHeader</span></span>

![Veidnes kartējums līdzeklī Datu integrācija](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="c8f4d-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="c8f4d-168">SalesInvoiceLine</span></span>

![Veidnes kartējums līdzeklī Datu integrācija](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="c8f4d-170">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="c8f4d-170">Related topics</span></span>

[<span data-ttu-id="c8f4d-171">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="c8f4d-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="c8f4d-172">Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c8f4d-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="c8f4d-173">Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Sales</span><span class="sxs-lookup"><span data-stu-id="c8f4d-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="c8f4d-174">Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c8f4d-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="c8f4d-175">Programmā Sales ietverto pārdošanas pasūtījumu tieša sinhronizācija ar programmu Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c8f4d-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
