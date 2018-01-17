---
title: "Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales"
description: "Šajā tēmā ir aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas rēķina virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition uz Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 6db68236f512cc720e75c0d576ce4c49d6c87882
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="ac938-103">Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="ac938-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ac938-104">Šajā tēmā ir aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas rēķina virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition uz Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="ac938-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="ac938-105">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="ac938-105">Templates and tasks</span></span>

<span data-ttu-id="ac938-106">Pārdošanas rēķinu virsrakstu un rindu sinhronizēšanai no Finance and Operations uz Sales tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="ac938-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="ac938-107">**Veidnes nosaukums datu integrācijā**</span><span class="sxs-lookup"><span data-stu-id="ac938-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="ac938-108">Pārdošanas rēķini (no Fin and Ops uz Sales)</span><span class="sxs-lookup"><span data-stu-id="ac938-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="ac938-109">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="ac938-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="ac938-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="ac938-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="ac938-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="ac938-111">SalesInvoiceLine</span></span>

<span data-ttu-id="ac938-112">Sinhronizācijas uzdevumi, kas ir jāveic pirms pārdošanas rēķina virsraksta un rindu sinhronizēšanas:</span><span class="sxs-lookup"><span data-stu-id="ac938-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="ac938-113">Preces (no Fin and Ops uz Sales)</span><span class="sxs-lookup"><span data-stu-id="ac938-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="ac938-114">Konti (no Sales uz Fin and Ops) (ja izmantoti)</span><span class="sxs-lookup"><span data-stu-id="ac938-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="ac938-115">Kontaktpersonas (no Sales uz Fin and Ops) (ja izmantotas)</span><span class="sxs-lookup"><span data-stu-id="ac938-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="ac938-116">Pārdošanas pasūtījuma virsraksts un rindas (no Fin and Ops uz Sales)</span><span class="sxs-lookup"><span data-stu-id="ac938-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="ac938-117">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="ac938-117">Entity set</span></span>

| <span data-ttu-id="ac938-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac938-118">Finance and Operations</span></span>                               | <span data-ttu-id="ac938-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="ac938-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="ac938-120">Sales</span><span class="sxs-lookup"><span data-stu-id="ac938-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="ac938-121">Ārēji uzturētu debitora pārdošanas rēķinu virsraksti</span><span class="sxs-lookup"><span data-stu-id="ac938-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="ac938-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="ac938-122">SalesInvoice</span></span>     | <span data-ttu-id="ac938-123">Rēķini</span><span class="sxs-lookup"><span data-stu-id="ac938-123">Invoices</span></span>       |
| <span data-ttu-id="ac938-124">Ārēji uzturētu debitora pārdošanas rēķinu rindas</span><span class="sxs-lookup"><span data-stu-id="ac938-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="ac938-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="ac938-125">SalesInvoiceLine</span></span> | <span data-ttu-id="ac938-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="ac938-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="ac938-127">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="ac938-127">Entity flow</span></span>

<span data-ttu-id="ac938-128">Pārdošanas rēķini tiek izveidoti programmā Finance and Operations un sinhronizēti ar Sales.</span><span class="sxs-lookup"><span data-stu-id="ac938-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="ac938-129">Nodokļi, kas ir saistīti ar maksām laukā **Pārdošanas rēķina virsraksts**, pašlaik nav ietverti sinhronizēšanā no Finance and Operations uz Sales.</span><span class="sxs-lookup"><span data-stu-id="ac938-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="ac938-130">Tas ir tādēļ, ka Sales neatbalsta nodokļu informāciju virsraksta līmenī.</span><span class="sxs-lookup"><span data-stu-id="ac938-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="ac938-131">Nodokļi, kas ir saistīti ar maksām rindu līmenī, ir ietverti.</span><span class="sxs-lookup"><span data-stu-id="ac938-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ac938-132">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="ac938-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="ac938-133">Elementam **Rēķins** ir pievienots un lapā tiek rādīts lauks **Rēķina numurs**.</span><span class="sxs-lookup"><span data-stu-id="ac938-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="ac938-134">Poga **Izveidot rēķinu** lapā **Pārdošanas pasūtījums** ir paslēpta, jo rēķini tiks izveidoti programmā Finance and Operations un sinhronizēti uz Sales.</span><span class="sxs-lookup"><span data-stu-id="ac938-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="ac938-135">Lapu **Rēķins** nevar rediģēt, jo rēķini tiks sinhronizēti no Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac938-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="ac938-136">Kad saistītais rēķins no Finance and Operations ir sinhronizēts uz Sales, **Pārdošanas pasūtījuma statuss** automātiski mainās uz **Iekļauts rēķinā**.</span><span class="sxs-lookup"><span data-stu-id="ac938-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="ac938-137">Turklāt tā pārdošanas pasūtījuma īpašnieks, no kura rēķins tika izveidots, tiek piešķirts kā rēķina īpašnieks.</span><span class="sxs-lookup"><span data-stu-id="ac938-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="ac938-138">Šādi pārdošanas pasūtījuma īpašniekam tiek dota iespēja apskatīt rēķinu.</span><span class="sxs-lookup"><span data-stu-id="ac938-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ac938-139">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="ac938-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="ac938-140">Pirms pārdošanas rēķinu sinhronizēšanas ir svarīgi sistēmas atjaunināt ar tālāk norādīto iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="ac938-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="ac938-141">Iestatīšana programmā Sales</span><span class="sxs-lookup"><span data-stu-id="ac938-141">Setup in Sales</span></span>

- <span data-ttu-id="ac938-142">Sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Sales** pārliecinieties, vai **Lietot sistēmas cenu aprēķinu sistēmu** ir iestatīts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ac938-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="ac938-143">Sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Sales** pārliecinieties, vai **Atlaides aprēķināšanas metode** ir iestatīts uz **Rindas elements**.</span><span class="sxs-lookup"><span data-stu-id="ac938-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="ac938-144">Iestatīšana datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="ac938-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="ac938-145">SalesInvoiceHeader uzdevums</span><span class="sxs-lookup"><span data-stu-id="ac938-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="ac938-146">Atjauniniet kartējumu vienumam **CDS organizācijas ID** sadaļā **Avots** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="ac938-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="ac938-147">Lauka **SalesOrder_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="ac938-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="ac938-148">Lauka **Account_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="ac938-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="ac938-149">Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="ac938-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="ac938-150">Pārliecinieties, vai nepieciešamais kartējums pastāv sadaļā **Avots** > **CDS attiecībā uz InvoiceCountryRegionId** uz **BillingAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="ac938-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="ac938-151">Veidnes vērtība ir **ValueMap** ar kartēto valstu skaitu.</span><span class="sxs-lookup"><span data-stu-id="ac938-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="ac938-152">Lai izveidotu rēķinus programmā Sales, ir nepieciešams **Cenrādis**.</span><span class="sxs-lookup"><span data-stu-id="ac938-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="ac938-153">Atjauniniet lauku **ValueMap** sadaļā **CDS** > **Mērķis attiecībā uz pricelevelid.name [Cenrāža nosaukums]** uz programmā Sales izmantoto vērtību **Cenrādis** atkarībā no valūtas.</span><span class="sxs-lookup"><span data-stu-id="ac938-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="ac938-154">Varat izmantot noklusējuma vērtību **Cenrādis** vienai valūtai vai izmantot vērtību **ValueMap**, ja **Cenrāži** jums ir vairākās valūtās.</span><span class="sxs-lookup"><span data-stu-id="ac938-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="ac938-155">Veidnes vērtība attiecībā uz **pricelevelid.name [Cenrāža nosaukums]** ir no vērtības **Valūta** atkarīga vērtība **ValueMap**.</span><span class="sxs-lookup"><span data-stu-id="ac938-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="ac938-156">usd: CRM Service ASV (paraugs).</span><span class="sxs-lookup"><span data-stu-id="ac938-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="ac938-157">SalesInvoiceLine uzdevums</span><span class="sxs-lookup"><span data-stu-id="ac938-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="ac938-158">Pārliecinieties, vai nepieciešamais kartējums pastāv sadaļā **Avots** > **CDS mērvienībai**.</span><span class="sxs-lookup"><span data-stu-id="ac938-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="ac938-159">Pārliecinieties, vai nepieciešamā vērtība **ValueMap** vienumam **SalesUnitSymbol** programmā Finance and Operations pastāv sadaļā **Avots** > **CDS kartējums**.</span><span class="sxs-lookup"><span data-stu-id="ac938-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="ac938-160">Veidnes vērtība ar vienumu **ValueMap** ir definēta vienumam **SalesUnitSymbol uz Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="ac938-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="ac938-161">Atjauniniet kartējumu vienumam **CDS organizācijas ID sadaļā Avots** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="ac938-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="ac938-162">Lauka **SalesInvoicer_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="ac938-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="ac938-163">Lauka **Product_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="ac938-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="ac938-164">Veidnes kartējums datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="ac938-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="ac938-165">Lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids** nav ietverti noklusējuma kartējumos.</span><span class="sxs-lookup"><span data-stu-id="ac938-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="ac938-166">Šo lauku kartēšanas nolūkos ir jāiestata vērtību kartējums, kurš ir specifisks datiem tajās organizācijās, starp kurām elements tiek sinhronizēts.</span><span class="sxs-lookup"><span data-stu-id="ac938-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="ac938-167">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="ac938-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Veidnes kartēšana datu integrētājā](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Veidnes kartēšana datu integrētājā](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Veidnes kartēšana datu integrētājā](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="ac938-172">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="ac938-172">Related topics</span></span>

[<span data-ttu-id="ac938-173">Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="ac938-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="ac938-174">Kontu sinhronizēšana no programmas Sales uz klientiem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac938-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="ac938-175">Kontaktpersonu sinhronizēšana no programmas Sales uz kontaktpersonām vai klientiem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac938-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="ac938-176">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no programmas Sales uz programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ac938-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="ac938-177">Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="ac938-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


