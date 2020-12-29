---
title: Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto kontu sinhronizēšanai ar programmu Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
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
ms.openlocfilehash: 8aa03f94e0fb89a6d34ce014dbb6004a1a666327
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529214"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="9358a-103">Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9358a-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="9358a-104">Pirms risinājuma No potenciāla klienta līdz skaidrai naudai lietošanas izlasiet rakstu [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="9358a-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="9358a-105">Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto kontu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9358a-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="9358a-106">Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="9358a-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="9358a-107">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs.</span><span class="sxs-lookup"><span data-stu-id="9358a-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="9358a-108">Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="9358a-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="9358a-109">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="9358a-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="9358a-110">[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="9358a-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9358a-111">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="9358a-111">Templates and tasks</span></span>

<span data-ttu-id="9358a-112">Lai piekļūtu pieejamajām veidnēm, atveriet [Power Apps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="9358a-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="9358a-113">Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="9358a-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="9358a-114">Tālāk norādītā veidne un pamata uzdevums tiek izmantoti programmā Sales ietverto kontu sinhronizēšanai ar programmu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9358a-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="9358a-115">**Veidnes nosaukums līdzeklī Datu integrācija:** Konti (no Sales uz Fin and Ops) — tieši</span><span class="sxs-lookup"><span data-stu-id="9358a-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="9358a-116">**Projekta uzdevuma nosaukums:** Konti — debitori</span><span class="sxs-lookup"><span data-stu-id="9358a-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="9358a-117">Lai varētu veikt kontu/debitoru sinhronizāciju, nav nepieciešams neviens sinhronizācijas uzdevums.</span><span class="sxs-lookup"><span data-stu-id="9358a-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="9358a-118">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="9358a-118">Entity set</span></span>

| <span data-ttu-id="9358a-119">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="9358a-119">Sales</span></span>    | <span data-ttu-id="9358a-120">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9358a-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="9358a-121">Konti</span><span class="sxs-lookup"><span data-stu-id="9358a-121">Accounts</span></span> | <span data-ttu-id="9358a-122">Debitori V2</span><span class="sxs-lookup"><span data-stu-id="9358a-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="9358a-123">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="9358a-123">Entity flow</span></span>

<span data-ttu-id="9358a-124">Konti tiek pārvaldīti programmā Sales un tiek sinhronizēti ar programmu Supply Chain Management kā klienti.</span><span class="sxs-lookup"><span data-stu-id="9358a-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="9358a-125">Šiem debitoriem tiek iestatīta rekvizīta **Tiek ārēji uzturēts** vērtība **Jā**, lai izsekotu debitorus, kas ir izveidoti no programmas Sales.</span><span class="sxs-lookup"><span data-stu-id="9358a-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="9358a-126">Rēķina izrakstīšanas laikā šī informācija tiek izmantota, lai filtrētu rēķinus, kas ir sinhronizēti ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="9358a-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9358a-127">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="9358a-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9358a-128">Lapā **Konts** ir pieejams lauks **Konta numurs**.</span><span class="sxs-lookup"><span data-stu-id="9358a-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="9358a-129">Tas ir iestatīts kā parasta un unikāla atslēga, lai nodrošinātu integrācijas atbalstu.</span><span class="sxs-lookup"><span data-stu-id="9358a-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="9358a-130">Risinājuma Klientu attiecību pārvaldība (CRM) parastās atslēgas līdzeklis var ietekmēt debitorus, kuri jau izmanto lauku **Konta numurs**, bet nelieto unikālās lauka **Konta numurs** vērtības katram kontam.</span><span class="sxs-lookup"><span data-stu-id="9358a-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="9358a-131">Pašlaik integrācijas risinājumu neatbalsta šo gadījumu.</span><span class="sxs-lookup"><span data-stu-id="9358a-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="9358a-132">Kad tiek izveidots jauns konts un lauka **Konta numurs** vērtība vēl nepastāv, to automātiski ģenerē, izmantojot numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="9358a-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="9358a-133">Šī vērtība sastāv no **ACC**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="9358a-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="9358a-134">Piemērs: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="9358a-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="9358a-135">Lietojot integrācijas risinājumu programmai Sales, jaunināšanas skripts lauku **Konta numurs** iestata esošajiem kontiem programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="9358a-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="9358a-136">Ja nav norādīta lauka **Konta numurs** vērtība, tiek izmantota iepriekš norādītā numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="9358a-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9358a-137">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="9358a-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="9358a-138">Programmā Supply Chain Management ir jāatjaunina kartējums **CustomerGroupId**, norādot derīgu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9358a-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="9358a-139">Varat norādīt noklusējuma vērtību vai arī vērtību varat iestatīt, izmantojot vērtības karti.</span><span class="sxs-lookup"><span data-stu-id="9358a-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="9358a-140">Noklusējuma veidnes vērtība ir **10**.</span><span class="sxs-lookup"><span data-stu-id="9358a-140">The default template value is **10**.</span></span>

- <span data-ttu-id="9358a-141">Pievienojot tālāk norādītos kartējumus, jūs varat samazināt programmā Supply Chain Management nepieciešamo manuālo atjauninājumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="9358a-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="9358a-142">Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.</span><span class="sxs-lookup"><span data-stu-id="9358a-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="9358a-143">**SiteId**— vieta ir jānorāda, lai programmā Supply Chain Management ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="9358a-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="9358a-144">Noklusējuma vietu var ņemt no preces vai no debitora pasūtījuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="9358a-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="9358a-145">Noklusējuma veidnes vērtība ir **1**.</span><span class="sxs-lookup"><span data-stu-id="9358a-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="9358a-146">**WarehouseId**— noliktava ir jānorāda, lai programmā Supply Chain Management apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="9358a-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="9358a-147">Noklusējuma noliktavu var paņemt no preces vai no klienta pasūtījuma virsrakstā programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9358a-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="9358a-148">Noklusējuma veidnes vērtība ir **13**.</span><span class="sxs-lookup"><span data-stu-id="9358a-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="9358a-149">**LanguageId**— valoda ir jānorāda, lai programmā Supply Chain Management ģenerētu piedāvājumu un pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="9358a-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="9358a-150">Pēc noklusējuma tiek izmantota valoda no debitora pasūtījuma virsraksta.</span><span class="sxs-lookup"><span data-stu-id="9358a-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="9358a-151">Noklusējuma veidnes vērtība ir **en-us**.</span><span class="sxs-lookup"><span data-stu-id="9358a-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9358a-152">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="9358a-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="9358a-153">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="9358a-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="9358a-154">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="9358a-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="9358a-155">Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="9358a-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="9358a-156">Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9358a-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Veidnes kartējums līdzeklī Datu integrācija](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="9358a-158">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="9358a-158">Related topics</span></span>


[<span data-ttu-id="9358a-159">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="9358a-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="9358a-160">Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9358a-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="9358a-161">Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9358a-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="9358a-162">Programmā Sales ietverto pārdošanas pasūtījumu tieša sinhronizācija ar programmu Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9358a-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="9358a-163">Programmā Supply Chain Management ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="9358a-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

