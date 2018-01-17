---
title: "Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales"
description: "Šajā tēmā ir aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition uz Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: d7e4c435a3344f6a5d66e1889b633d80cda085eb
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="b1c08-103">Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="b1c08-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b1c08-104">Šajā tēmā ir aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition uz Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="b1c08-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="b1c08-105">Veidne un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="b1c08-105">Template and tasks</span></span>

<span data-ttu-id="b1c08-106">Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšanai no Finance and Operations uz Sales tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="b1c08-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="b1c08-107">**Veidnes nosaukums datu integrācijā**</span><span class="sxs-lookup"><span data-stu-id="b1c08-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="b1c08-108">Pārdošanas pasūtījumi (no Fin and Ops uz Sales)</span><span class="sxs-lookup"><span data-stu-id="b1c08-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="b1c08-109">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="b1c08-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="b1c08-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="b1c08-110">OrderHeader</span></span>
    - <span data-ttu-id="b1c08-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="b1c08-111">OrderLine</span></span>

<span data-ttu-id="b1c08-112">Sinhronizācijas uzdevumi, kas ir jāveic pirms pārdošanas rēķina virsraksta un rindu sinhronizēšanas:</span><span class="sxs-lookup"><span data-stu-id="b1c08-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="b1c08-113">Preces (no Fin and Ops uz Sales)</span><span class="sxs-lookup"><span data-stu-id="b1c08-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="b1c08-114">Konti (no Sales uz Fin and Ops) (ja izmantoti)</span><span class="sxs-lookup"><span data-stu-id="b1c08-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="b1c08-115">Kontaktpersonas uz debitoriem (no Sales uz Fin un Ops) (ja tiek izmantotas)</span><span class="sxs-lookup"><span data-stu-id="b1c08-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="b1c08-116">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="b1c08-116">Entity set</span></span>

| <span data-ttu-id="b1c08-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1c08-117">Finance and Operations</span></span> |    <span data-ttu-id="b1c08-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="b1c08-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="b1c08-119">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="b1c08-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="b1c08-120">CDS pārdošanas pasūtījumu virsraksti</span><span class="sxs-lookup"><span data-stu-id="b1c08-120">CDS sales order headers</span></span>| <span data-ttu-id="b1c08-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="b1c08-121">SalesOrder</span></span>     | <span data-ttu-id="b1c08-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="b1c08-122">SalesOrders</span></span> |
| <span data-ttu-id="b1c08-123">CDS pārdošanas pasūtījumu rindas</span><span class="sxs-lookup"><span data-stu-id="b1c08-123">CDS sales order lines</span></span>  | <span data-ttu-id="b1c08-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="b1c08-124">SalesOrderLine</span></span> | <span data-ttu-id="b1c08-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="b1c08-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="b1c08-126">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="b1c08-126">Entity flow</span></span>

<span data-ttu-id="b1c08-127">Pārdošanas pasūtījumi tiek izveidoti programmā Finance and Operations un sinhronizēti ar Sales.</span><span class="sxs-lookup"><span data-stu-id="b1c08-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="b1c08-128">Filtri veidnē nodrošina, ka sinhronizācijā tiek ietverti tikai saistītie pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="b1c08-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="b1c08-129">Tāda pārdošanas pasūtījuma sinhronizēšanā, kura izcelsme ir programma Sales, tiek ietverts gan pasūtošais, gan rēķinu izrakstošais debitors.</span><span class="sxs-lookup"><span data-stu-id="b1c08-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="b1c08-130">Programmā Finance and Operations lauki **OrderingCustomerIsExternallyMaintained** un **InvoiceCustomerIsExternallyMaintained** tiek izmantoti, lai sekotu līdzi sinhronizēšanai datu elementos.</span><span class="sxs-lookup"><span data-stu-id="b1c08-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="b1c08-131">**Pārdošanas pasūtījums** ir jāapstiprina programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b1c08-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="b1c08-132">Uz programmu Sales tiek sinhronizēti tikai apstiprinātie pārdošanas pasūtījumi vai pārdošanas pasūtījumi ar augstāku apstrādes statusu, piemēram, Nosūtīts vai Iekļauts rēķinā.</span><span class="sxs-lookup"><span data-stu-id="b1c08-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="b1c08-133">Pēc pārdošanas pasūtījuma izveidošanas vai modificēšanas programmā Finance and Operations ir jāizpilda pakešuzdevums **Aprēķināt pārdošanas kopsummas**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="b1c08-134">Uz CDS un Sales tiks sinhronizēti tikai pārdošanas pasūtījumi ar aprēķinātām pārdošanas kopsummām.</span><span class="sxs-lookup"><span data-stu-id="b1c08-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="b1c08-135">Nodokļi, kas ir saistīti ar maksām laukā **Pārdošanas pasūtījuma virsraksts**, pašlaik nav ietverti sinhronizēšanā no Finance and Operations uz Sales.</span><span class="sxs-lookup"><span data-stu-id="b1c08-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="b1c08-136">Tas ir tādēļ, ka Sales neatbalsta nodokļu informāciju virsraksta līmenī.</span><span class="sxs-lookup"><span data-stu-id="b1c08-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="b1c08-137">Nodokļi, kas ir saistīti ar maksām rindu līmenī, ir ietverti.</span><span class="sxs-lookup"><span data-stu-id="b1c08-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b1c08-138">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="b1c08-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b1c08-139">Elementam **Pasūtījums** ir pievienoti un lapā tiek rādīti jauni lauki:</span><span class="sxs-lookup"><span data-stu-id="b1c08-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="b1c08-140">**Tiek uzturēts ārēji** — iestatiet uz **Jā**, ja pasūtījums tiek saņemts no Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b1c08-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="b1c08-141">**Apstrādes statuss** — izmantots, lai parādītu pasūtījuma apstrādes statusu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b1c08-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="b1c08-142">Vērtības ir šādas:</span><span class="sxs-lookup"><span data-stu-id="b1c08-142">Values are:</span></span>

    - <span data-ttu-id="b1c08-143">Aktīvs</span><span class="sxs-lookup"><span data-stu-id="b1c08-143">Active</span></span>
    - <span data-ttu-id="b1c08-144">Akceptēts</span><span class="sxs-lookup"><span data-stu-id="b1c08-144">Confirmed</span></span>
    - <span data-ttu-id="b1c08-145">Pavadzīmes</span><span class="sxs-lookup"><span data-stu-id="b1c08-145">Packing Slip</span></span>
    - <span data-ttu-id="b1c08-146">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="b1c08-146">Invoiced</span></span>
    - <span data-ttu-id="b1c08-147">Izdots</span><span class="sxs-lookup"><span data-stu-id="b1c08-147">Picked</span></span>
    - <span data-ttu-id="b1c08-148">Daļēji izdots</span><span class="sxs-lookup"><span data-stu-id="b1c08-148">Partially Picked</span></span>
    - <span data-ttu-id="b1c08-149">Daļēji iepakots</span><span class="sxs-lookup"><span data-stu-id="b1c08-149">Partially Packed</span></span>
    - <span data-ttu-id="b1c08-150">Nosūtīts</span><span class="sxs-lookup"><span data-stu-id="b1c08-150">Shipped</span></span>
    - <span data-ttu-id="b1c08-151">Daļēji nosūtīts</span><span class="sxs-lookup"><span data-stu-id="b1c08-151">Partially Shipped</span></span>
    - <span data-ttu-id="b1c08-152">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="b1c08-152">Partially Invoiced</span></span>
    - <span data-ttu-id="b1c08-153">Atcelts</span><span class="sxs-lookup"><span data-stu-id="b1c08-153">Cancelled</span></span>

<span data-ttu-id="b1c08-154">Iestatījums **Ir tikai ārēji uzturētas preces** tiek lietots citos pārdošanas pasūtījumu scenārijos (sinhronizēšanai no Sales uz Finance and Operation), lai konsekventi sekotu līdzi tam, vai pārdošanas pasūtījumu pilnībā veido **Ārēji uzturētas preces** — tādā gadījumā preces tiek uzturētas programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b1c08-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="b1c08-155">Šādi tiek nodrošināts, ka jūs nemēģināt sinhronizēt pārdošanas pasūtījuma rindas ar precēm, kas programmā Finance and Operations nav zināmas.</span><span class="sxs-lookup"><span data-stu-id="b1c08-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="b1c08-156">Ārēji uzturētiem pasūtījumiem pogas **Izveidot rēķinu**, **Atcelt pasūtījumu**, **Pārrēķināt**, **Iegūt preces** un **Uzmeklēt adresi** lapā **Pārdošanas pasūtījums** tiek slēptas, jo rēķini tiks izveidoti programmā Finance and Operations un sinhronizēti uz Sales.</span><span class="sxs-lookup"><span data-stu-id="b1c08-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="b1c08-157">Pasūtījuma lapu nevar rediģēt, jo pārdošanas pasūtījuma informācija tiks sinhronizēta no Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b1c08-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="b1c08-158">**Pārdošanas pasūtījuma statuss** saglabājas aktīvs, lai nodrošinātu, ka izmaiņas no Finance and Operations var plūst uz elementu **Pārdošanas pasūtījums** programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="b1c08-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="b1c08-159">Tas tiek kontrolēts, datu integrācijas projektā noklusējuma **Statecode [Statuss]** iestatot uz **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b1c08-160">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="b1c08-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="b1c08-161">Pirms pārdošanas pasūtījumu sinhronizēšanas ir svarīgi sistēmas atjaunināt ar tālāk norādīto iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="b1c08-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="b1c08-162">Iestatīšana programmā Sales</span><span class="sxs-lookup"><span data-stu-id="b1c08-162">Setup in Sales</span></span>

- <span data-ttu-id="b1c08-163">Nodrošiniet atļaujas tai darba grupai, kurai ir piešķirts lietotājs (no savas programmas Sales **Savienojumu kopa**).</span><span class="sxs-lookup"><span data-stu-id="b1c08-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="b1c08-164">Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuve, bet darba grupai tās nav.</span><span class="sxs-lookup"><span data-stu-id="b1c08-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="b1c08-165">Bez šī iestatījuma jums tiks parādīts kļūdas ziņojums, ka trūkst galvenās darba grupas, kad projektu palaižat no datu integrētāja.</span><span class="sxs-lookup"><span data-stu-id="b1c08-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="b1c08-166">Sadaļā **Iestatījumi** > **Drošība** > **Darba grupas** atlasiet attiecīgo darba grupu, noklikšķiniet uz **Pārvaldīt lomas** un atlasiet lomu ar vēlamajām atļaujām, piemēram, Sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="b1c08-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="b1c08-167">Sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Sales** pārliecinieties, vai **Lietot sistēmas cenu aprēķinu sistēmu** ir iestatīts uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="b1c08-168">Sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Sales** pārliecinieties, vai **Atlaides aprēķināšanas metode** ir iestatīts uz **Rindas elements**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="b1c08-169">Iestatīšana programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1c08-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="b1c08-170">Vienumu **Pārdošana un mārketings** > **Periodiskie uzdevumi** > **Aprēķināt pārdošanas kopsummas** iestatiet palaišanai pakešuzdevuma veidā ar vienumu **Aprēķināt kopsummas pārdošanas pasūtījumiem** iestatītu uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="b1c08-171">Tas ir svarīgi, jo uz CDS un Sales tiks sinhronizēti tikai pārdošanas pasūtījumi ar aprēķinātām pārdošanas kopsummām.</span><span class="sxs-lookup"><span data-stu-id="b1c08-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="b1c08-172">Pakešuzdevuma izpildes biežumam ir jāatbilst pārdošanas pasūtījumu sinhronizēšanas biežumam.</span><span class="sxs-lookup"><span data-stu-id="b1c08-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="b1c08-173">Iestatīšana datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="b1c08-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="b1c08-174">SalesHeader uzdevums</span><span class="sxs-lookup"><span data-stu-id="b1c08-174">SalesHeader task</span></span>

- <span data-ttu-id="b1c08-175">Atjauniniet kartējumu vienumam **CDS organizācijas ID sadaļā Avots** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="b1c08-176">Lauka **Account_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="b1c08-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="b1c08-177">Lauka **InvoiceAccount_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="b1c08-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="b1c08-178">Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="b1c08-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="b1c08-179">Pārliecinieties, vai nepieciešamais kartējums pastāv sadaļā **Avots** > **CDS attiecībā uz InvoiceCountryRegionId uz BillingAddress_Country** un attiecībā uz **DeliveryCountryRegionId uz DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="b1c08-180">Veidnes vērtība ir **ValueMap** ar kartēto valstu skaitu.</span><span class="sxs-lookup"><span data-stu-id="b1c08-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="b1c08-181">Lai izveidotu pasūtījumus programmā Sales, ir nepieciešams **Cenrādis**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="b1c08-182">Atjauniniet lauku **ValueMap** sadaļā **CDS** > **Mērķis** attiecībā uz **pricelevelid.name [Cenrāža nosaukums]** uz programmā Sales izmantoto vērtību **Cenrādis** atkarībā no valūtas.</span><span class="sxs-lookup"><span data-stu-id="b1c08-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="b1c08-183">Varat izmantot noklusējuma vērtību **Cenrādis** vienai valūtai vai izmantot vērtību **ValueMap**, ja **Cenrāži** jums ir vairākās valūtās.</span><span class="sxs-lookup"><span data-stu-id="b1c08-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="b1c08-184">Lauka **pricelevelid.name [Cenrāža nosaukums]** noklusējuma veidnes vērtība ir CRM Service USA (paraugs).</span><span class="sxs-lookup"><span data-stu-id="b1c08-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="b1c08-185">SalesLine uzdevums</span><span class="sxs-lookup"><span data-stu-id="b1c08-185">SalesLine task</span></span>

- <span data-ttu-id="b1c08-186">Atjauniniet kartējumu vienumam **CDS organizācijas ID sadaļā Avots** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="b1c08-187">Lauka **SalesOrder_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="b1c08-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="b1c08-188">Lauka **Product_Organization_OrganizationId** noklusējuma veidnes vērtība ir ORG001.</span><span class="sxs-lookup"><span data-stu-id="b1c08-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="b1c08-189">Pārliecinieties, vai nepieciešamais kartējums pastāv sadaļā **Avots** > **CDS** attiecībā uz **DeliveryCountryRegionId** uz **DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="b1c08-190">Veidnes vērtība ir **ValueMap** ar kartēto valstu skaitu.</span><span class="sxs-lookup"><span data-stu-id="b1c08-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="b1c08-191">Pārliecinieties, vai nepieciešamā vērtība **ValueMap** vienumam **SalesUnitSymbol** programmā Finance and Operations pastāv sadaļā **Avots** > **CDS kartējums**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="b1c08-192">Veidnes vērtība ar vienumu **ValueMap** ir definēta vienumam **SalesUnitSymbol uz Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="b1c08-193">Veidnes kartēšana datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="b1c08-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="b1c08-194">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="b1c08-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="b1c08-195">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="b1c08-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="b1c08-196">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="b1c08-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="b1c08-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="b1c08-197">OrderHeader</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-order-template-mapping-data-integrator-1.png)

![Veidnes kartēšana datu integrētājā](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="b1c08-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="b1c08-200">OrderLine</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-order-template-mapping-data-integrator-3.png)

![Veidnes kartēšana datu integrētājā](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="b1c08-203">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="b1c08-203">Related topics</span></span>

[<span data-ttu-id="b1c08-204">Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="b1c08-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="b1c08-205">Kontu sinhronizēšana no programmas Sales uz klientiem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1c08-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="b1c08-206">Kontaktpersonu sinhronizēšana no programmas Sales uz kontaktpersonām vai klientiem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1c08-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="b1c08-207">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no programmas Sales uz programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1c08-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="b1c08-208">Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="b1c08-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


