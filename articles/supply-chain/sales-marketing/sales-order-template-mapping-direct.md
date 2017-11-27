---
title: "Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition ietverto pārdošanas pasūtījumu galveņu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="8b643-103">Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="8b643-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8b643-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition ietverto pārdošanas pasūtījumu galveņu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="8b643-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="8b643-105">Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="8b643-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="8b643-106">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs.</span><span class="sxs-lookup"><span data-stu-id="8b643-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="8b643-107">Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="8b643-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="8b643-108">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="8b643-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="8b643-109">[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="8b643-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="8b643-110">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="8b643-110">Templates and tasks</span></span>

<span data-ttu-id="8b643-111">Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="8b643-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="8b643-112">Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="8b643-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="8b643-113">Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu sinhronizēšanai ar programmu Sales tiek izmantota tālāk norādītā veidne un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="8b643-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="8b643-114">**Veidnes nosaukums līdzeklī Datu integrācija:** Pārdošanas pasūtījumi (no Fin and Ops uz Sales) — tieši</span><span class="sxs-lookup"><span data-stu-id="8b643-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="8b643-115">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="8b643-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="8b643-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="8b643-116">OrderHeader</span></span>
    - <span data-ttu-id="8b643-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="8b643-117">OrderLine</span></span>

<span data-ttu-id="8b643-118">Lai varētu veikt pārdošanas rēķinu galveņu un rindu sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="8b643-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="8b643-119">Preces (no Fin and Ops uz Sales) — tieši</span><span class="sxs-lookup"><span data-stu-id="8b643-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="8b643-120">Konti (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)</span><span class="sxs-lookup"><span data-stu-id="8b643-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="8b643-121">Kontaktpersonas kā debitori (no Sales uz Fin and Ops) — tieši (ja tiek izmantots)</span><span class="sxs-lookup"><span data-stu-id="8b643-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="8b643-122">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="8b643-122">Entity set</span></span>

| <span data-ttu-id="8b643-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b643-123">Finance and Operations</span></span>  | <span data-ttu-id="8b643-124">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="8b643-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="8b643-125">CDS pārdošanas pasūtījumu virsraksti</span><span class="sxs-lookup"><span data-stu-id="8b643-125">CDS sales order headers</span></span> | <span data-ttu-id="8b643-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="8b643-126">SalesOrders</span></span>       |
| <span data-ttu-id="8b643-127">CDS pārdošanas pasūtījumu rindas</span><span class="sxs-lookup"><span data-stu-id="8b643-127">CDS sales order lines</span></span>   | <span data-ttu-id="8b643-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="8b643-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="8b643-129">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="8b643-129">Entity flow</span></span>

<span data-ttu-id="8b643-130">Pārdošanas pasūtījumi tiek izveidoti programmā Finance and Operations un sinhronizēti ar Sales.</span><span class="sxs-lookup"><span data-stu-id="8b643-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="8b643-131">Filtri veidnē palīdz nodrošināt, ka tiek sinhronizēti tikai saistītie pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="8b643-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="8b643-132">Sinhronizējot pārdošana pasūtījumu, no programmas Sales tiek sinhronizēts gan pasūtījumu veikušais debitors, gan rēķinu izrakstošais debitors.</span><span class="sxs-lookup"><span data-stu-id="8b643-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="8b643-133">Programmā Finance and Operations lauki **OrderingCustomerIsExternallyMaintained** un **InvoiceCustomerIsExternallyMaintained** tiek izmantoti, lai izsekotu sinhronizēšanu datu elementos.</span><span class="sxs-lookup"><span data-stu-id="8b643-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="8b643-134">Pārdošanas pasūtījums ir jāapstiprina programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b643-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="8b643-135">Ar programmu Sales tiek sinhronizēti tikai apstiprinātie pārdošanas pasūtījumi vai pārdošanas pasūtījumi, kuriem ir augstāks apstrādes statuss, piemēram, **Nosūtīts** vai **Iekļauts rēķinā**.</span><span class="sxs-lookup"><span data-stu-id="8b643-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="8b643-136">Pēc pārdošanas pasūtījuma izveidošanas vai izmainīšanas programmā Finance and Operations ir jāizpilda pakešuzdevums **Aprēķināt pārdošanas kopsummas**.</span><span class="sxs-lookup"><span data-stu-id="8b643-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="8b643-137">Ar programmu Sales tiek sinhronizēti tikai tie pārdošanas pasūtījumi, kuriem ir aprēķinātas pārdošanas kopsummas.</span><span class="sxs-lookup"><span data-stu-id="8b643-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="8b643-138">Pašlaik programmā Finance and Operations ietverto datu sinhronizēšanā ar programmu Sales netiek ietverti nodokļi, kas ir saistīti ar pārdošanas pasūtījuma galvenes maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="8b643-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="8b643-139">Programmā Sales netiek atbalstīta nodokļu informācija galvenes līmenī.</span><span class="sxs-lookup"><span data-stu-id="8b643-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="8b643-140">Taču ar rindas līmeņa maksājumiem saistītais nodoklis tiek ietverts sinhronizēšanā.</span><span class="sxs-lookup"><span data-stu-id="8b643-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="8b643-141">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="8b643-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="8b643-142">Elementam **Pasūtījums** ir pievienoti jauni lauki, kas tiek rādīti ekrāna.</span><span class="sxs-lookup"><span data-stu-id="8b643-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="8b643-143">**Tiek uzturēts ārēji** — iestatiet šīs opcijas vērtību **Jā**, ja pasūtījums ir iegūts no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b643-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="8b643-144">**Apstrādes statuss** — šajā laukā tiek rādīts pasūtījuma apstrādes statusu programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b643-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="8b643-145">Ir pieejamas šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="8b643-145">The following values are available:</span></span>

    - <span data-ttu-id="8b643-146">Aktīva</span><span class="sxs-lookup"><span data-stu-id="8b643-146">Active</span></span>
    - <span data-ttu-id="8b643-147">Akceptēts</span><span class="sxs-lookup"><span data-stu-id="8b643-147">Confirmed</span></span>
    - <span data-ttu-id="8b643-148">Pavadzīmes</span><span class="sxs-lookup"><span data-stu-id="8b643-148">Packing Slip</span></span>
    - <span data-ttu-id="8b643-149">Izveidots rēķins</span><span class="sxs-lookup"><span data-stu-id="8b643-149">Invoiced</span></span>
    - <span data-ttu-id="8b643-150">Izdots</span><span class="sxs-lookup"><span data-stu-id="8b643-150">Picked</span></span>
    - <span data-ttu-id="8b643-151">Daļēji izdots</span><span class="sxs-lookup"><span data-stu-id="8b643-151">Partially Picked</span></span>
    - <span data-ttu-id="8b643-152">Daļēji iepakots</span><span class="sxs-lookup"><span data-stu-id="8b643-152">Partially Packed</span></span>
    - <span data-ttu-id="8b643-153">Nosūtīts</span><span class="sxs-lookup"><span data-stu-id="8b643-153">Shipped</span></span>
    - <span data-ttu-id="8b643-154">Daļēji nosūtīts</span><span class="sxs-lookup"><span data-stu-id="8b643-154">Partially Shipped</span></span>
    - <span data-ttu-id="8b643-155">Daļēji iekļauts rēķinā</span><span class="sxs-lookup"><span data-stu-id="8b643-155">Partially Invoiced</span></span>
    - <span data-ttu-id="8b643-156">Atcelts</span><span class="sxs-lookup"><span data-stu-id="8b643-156">Cancelled</span></span>

<span data-ttu-id="8b643-157">Iestatījums **Ir tikai ārēji uzturētas preces** tiek izmantots citos pārdošanas pasūtījumu scenārijos (piemēram, sinhronizējot programmā Sales ietvertos datus ar programmu Finance and Operations), lai pastāvīgi izsekotu tam, vai pārdošanas pasūtījumā ir ietvertas tikai ārēji uzturētas preces.</span><span class="sxs-lookup"><span data-stu-id="8b643-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="8b643-158">Ja pārdošanas pasūtījumā ir ietvertas tikai ārēji uzturētas preces, tās tiek uzturētas programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b643-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="8b643-159">Šis iestatījums palīdz nodrošināt to, ka nemēģināt sinhronizēt pārdošanas pasūtījuma rindas, kurās ietvertās preces nav zināmas programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b643-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="8b643-160">Ārēji uzturētiem pasūtījumiem lapā **Pārdošanas pasūtījums** ir paslēptas pogas **Izveidot rēķinu**, **Atcelt pasūtījumu**, **Pārrēķināt**, **Iegūt preces** un **Uzmeklēt adresi**, jo rēķini tiks izveidoti programmā Finance and Operations un sinhronizēti ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="8b643-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="8b643-161">Pasūtījumu lapu nevar rediģēt, jo pārdošanas pasūtījuma informācija tiks sinhronizēta no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b643-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="8b643-162">Tiek saglabāts pārdošanas pasūtījuma statuss **Aktīvs**, lai palīdzētu nodrošināt programmā Finance and Operations veikto izmaiņu nodošanu uz pārdošanas pasūtījumu programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="8b643-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="8b643-163">Lai kontrolētu šo darbību, līdzekļa Datu integrācija projektā iestatiet lauka **Statecode \[statuss\]** noklusējuma vērtību **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="8b643-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="8b643-164">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="8b643-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="8b643-165">Pirms pārdošanas pasūtījumu sinhronizēšanas ir svarīgi sistēmās atjaunināt tālāk norādītos iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="8b643-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="8b643-166">Iestatīšana programmā Sales</span><span class="sxs-lookup"><span data-stu-id="8b643-166">Setup in Sales</span></span>

- <span data-ttu-id="8b643-167">Pārliecinieties, ka darba grupai, kurai ir piešķirts ar Sales savienojumu kopu saistītais lietotājs, ir iestatītas vajadzīgās atļaujas.</span><span class="sxs-lookup"><span data-stu-id="8b643-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="8b643-168">Ja izmantojat demonstrācijas datus, tad lietotājam parasti ir administratora piekļuves atļauja, bet darba grupai nav administratora piekļuves atļaujas.</span><span class="sxs-lookup"><span data-stu-id="8b643-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="8b643-169">Ja darba grupai nav administratora piekļuves atļaujas, palaižot projektu līdzeklī Datu integrācija, saņemat kļūdas ziņojumu par to, ka trūkst galvenās darba grupas.</span><span class="sxs-lookup"><span data-stu-id="8b643-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="8b643-170">Pārejiet uz sadaļu **Iestatījumi** > **Drošība** > **Darba grupas**, atlasiet attiecīgo darba grupu, atlasiet **Pārvaldīt lomas** un atlasiet lomu, kurai ir piešķirtas vajadzīgās atļaujas, piemēram, **Sistēmas administrators**.</span><span class="sxs-lookup"><span data-stu-id="8b643-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="8b643-171">Pārejiet uz sadaļu **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana** un pārliecinieties, ka ir izmantoti tālāk norādītie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="8b643-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="8b643-172">Ir iestatīta opcijas **Lietot sistēmas cenu noteikšanas sistēmu** vērtība **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8b643-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="8b643-173">Ir iestatīta lauka **Atlaides aprēķināšanas metode** vērtība **Rindas vienums**.</span><span class="sxs-lookup"><span data-stu-id="8b643-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="8b643-174">Iestatīšana programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b643-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="8b643-175">Pārejiet uz sadaļu **Pārdošana un mārketings** > **Periodiskie uzdevumi** > **Aprēķināt pārdošanas kopsummas** un iestatiet darba izpildi pakešuzdevuma režīmā.</span><span class="sxs-lookup"><span data-stu-id="8b643-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="8b643-176">Iestatiet opcijas **Aprēķināt kopsummas pārdošanas pasūtījumiem** vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8b643-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="8b643-177">Šī darbība ir svarīga, jo ar programmu Sales tiek sinhronizēti tikai tie pārdošanas pasūtījumi, kuriem ir aprēķinātas pārdošanas kopsummas.</span><span class="sxs-lookup"><span data-stu-id="8b643-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="8b643-178">Pakešuzdevuma izpildes biežumam ir jāatbilst pārdošanas pasūtījumu sinhronizēšanas biežumam.</span><span class="sxs-lookup"><span data-stu-id="8b643-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="8b643-179">Iestatīšana datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="8b643-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="8b643-180">SalesHeader uzdevums</span><span class="sxs-lookup"><span data-stu-id="8b643-180">SalesHeader task</span></span>

- <span data-ttu-id="8b643-181">Pārliecinieties, ka pastāv nepieciešamais kartējums no **InvoiceCountryRegionId** uz **BillingAddress\_Country** un no **DeliveryCountryRegionId** uz **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="8b643-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="8b643-182">Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni.</span><span class="sxs-lookup"><span data-stu-id="8b643-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="8b643-183">Lai varētu izveidot pasūtījumus programmā Sales, ir nepieciešams cenrādis.</span><span class="sxs-lookup"><span data-stu-id="8b643-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="8b643-184">Atjauniniet vienuma **pricelevelid.name \[cenrāža nosaukums\]** vērtību karti atbilstoši programmā Sales lietotajam cenrādim pēc valūtas.</span><span class="sxs-lookup"><span data-stu-id="8b643-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="8b643-185">Varat izmantot noklusējuma cenrādi vienai valūtai.</span><span class="sxs-lookup"><span data-stu-id="8b643-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="8b643-186">Ja jums ir cenrāži vairākās valūtās, varat izmantot vērtību karti.</span><span class="sxs-lookup"><span data-stu-id="8b643-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="8b643-187">Vienuma **pricelevelid.name \[cenrāža nosaukums\]** noklusējuma veidnes vērtība ir **CRM Service ASV (paraugs)**.</span><span class="sxs-lookup"><span data-stu-id="8b643-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="8b643-188">SalesLine uzdevums</span><span class="sxs-lookup"><span data-stu-id="8b643-188">SalesLine task</span></span>

- <span data-ttu-id="8b643-189">Pārliecinieties, ka pastāv nepieciešamais kartējums no **DeliveryCountryRegionId** uz **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="8b643-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="8b643-190">Veidnes vērtība ir vērtību karte, kur ir kartētas vairākas valstis vai reģioni.</span><span class="sxs-lookup"><span data-stu-id="8b643-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="8b643-191">Pārliecinieties, ka programmā Finance and Operations pastāv nepieciešamā vienuma **SalesUnitSymbol** vērtību karte.</span><span class="sxs-lookup"><span data-stu-id="8b643-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="8b643-192">Kartējumam no **SalesUnitSymbol** uz **Quantity\_UOM** ir definēta veidnes vērtība ar vērtību karti.</span><span class="sxs-lookup"><span data-stu-id="8b643-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8b643-193">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="8b643-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="8b643-194">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="8b643-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="8b643-195">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="8b643-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="8b643-196">Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="8b643-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b643-197">Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b643-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="8b643-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="8b643-198">OrderHeader</span></span>

![Veidnes kartējums datu integrētājā](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="8b643-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="8b643-200">OrderLine</span></span>

![Veidnes kartējums datu integrētājā](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="8b643-202">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="8b643-202">Related topics</span></span>

[<span data-ttu-id="8b643-203">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="8b643-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="8b643-204">Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b643-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="8b643-205">Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="8b643-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="8b643-206">Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b643-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="8b643-207">Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="8b643-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




