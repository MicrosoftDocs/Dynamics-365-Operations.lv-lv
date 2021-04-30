---
title: Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto kontu sinhronizēšanai ar programmu Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fff9171966045e9dad5f2c70087a568cfa075e43
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908136"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="5d1ea-103">Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5d1ea-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="5d1ea-104">Pirms risinājuma No potenciāla klienta līdz skaidrai naudai lietošanas izlasiet rakstu [Datu integrēšana pakalpojumā Microsoft Dataverse programmām](/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="5d1ea-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="5d1ea-105">Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Sales ietverto kontu tiešai sinhronizēšanai ar programmu Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5d1ea-106">Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="5d1ea-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5d1ea-107">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="5d1ea-108">Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="5d1ea-109">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="5d1ea-110">[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5d1ea-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5d1ea-111">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="5d1ea-111">Templates and tasks</span></span>

<span data-ttu-id="5d1ea-112">Lai piekļūtu pieejamajām veidnēm, atveriet [Power Apps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="5d1ea-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5d1ea-113">Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5d1ea-114">Tālāk norādītā veidne un pamata uzdevums tiek izmantoti programmā Sales ietverto kontu sinhronizēšanai ar programmu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="5d1ea-115">**Veidnes nosaukums līdzeklī Datu integrācija:** Konti (no Sales uz Fin and Ops) — tieši</span><span class="sxs-lookup"><span data-stu-id="5d1ea-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="5d1ea-116">**Projekta uzdevuma nosaukums:** Konti — debitori</span><span class="sxs-lookup"><span data-stu-id="5d1ea-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="5d1ea-117">Lai varētu veikt kontu/debitoru sinhronizāciju, nav nepieciešams neviens sinhronizācijas uzdevums.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="5d1ea-118">Entītiju kopa</span><span class="sxs-lookup"><span data-stu-id="5d1ea-118">Entity set</span></span>

| <span data-ttu-id="5d1ea-119">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="5d1ea-119">Sales</span></span>    | <span data-ttu-id="5d1ea-120">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5d1ea-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="5d1ea-121">Konti</span><span class="sxs-lookup"><span data-stu-id="5d1ea-121">Accounts</span></span> | <span data-ttu-id="5d1ea-122">Debitori V2</span><span class="sxs-lookup"><span data-stu-id="5d1ea-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="5d1ea-123">Entītiju plūsma</span><span class="sxs-lookup"><span data-stu-id="5d1ea-123">Entity flow</span></span>

<span data-ttu-id="5d1ea-124">Konti tiek pārvaldīti programmā Sales un tiek sinhronizēti ar programmu Supply Chain Management kā klienti.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="5d1ea-125">Šiem debitoriem tiek iestatīta rekvizīta **Tiek ārēji uzturēts** vērtība **Jā**, lai izsekotu debitorus, kas ir izveidoti no programmas Sales.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="5d1ea-126">Rēķina izrakstīšanas laikā šī informācija tiek izmantota, lai filtrētu rēķinus, kas ir sinhronizēti ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5d1ea-127">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="5d1ea-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5d1ea-128">Lapā **Konts** ir pieejams lauks **Konta numurs**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-128">The **Account Number** column is available on the **Account** page.</span></span> <span data-ttu-id="5d1ea-129">Tas ir iestatīts kā parasta un unikāla atslēga, lai nodrošinātu integrācijas atbalstu.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="5d1ea-130">Risinājuma Customer Relationship Management (CRM) parastās atslēgas līdzeklis var ietekmēt debitorus, kuri jau izmanto lauku **Konta numurs**, bet nelieto unikālās lauka **Konta numurs** vērtības katram kontam.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** column, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="5d1ea-131">Pašlaik integrācijas risinājumu neatbalsta šo gadījumu.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="5d1ea-132">Kad tiek izveidots jauns konts un lauka **Konta numurs** vērtība vēl nepastāv, to automātiski ģenerē, izmantojot numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="5d1ea-133">Šī vērtība sastāv no **ACC**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="5d1ea-134">Piemērs: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="5d1ea-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="5d1ea-135">Lietojot integrācijas risinājumu programmai Sales, jaunināšanas skripts lauku **Konta numurs** iestata esošajiem kontiem programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** column for existing accounts in Sales.</span></span> <span data-ttu-id="5d1ea-136">Ja nav norādīta lauka **Konta numurs** vērtība, tiek izmantota iepriekš norādītā numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5d1ea-137">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="5d1ea-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="5d1ea-138">Programmā Supply Chain Management ir jāatjaunina kartējums **CustomerGroupId**, norādot derīgu vērtību.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="5d1ea-139">Varat norādīt noklusējuma vērtību vai arī vērtību varat iestatīt, izmantojot vērtības karti.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="5d1ea-140">Noklusējuma veidnes vērtība ir **10**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-140">The default template value is **10**.</span></span>

- <span data-ttu-id="5d1ea-141">Pievienojot tālāk norādītos kartējumus, jūs varat samazināt programmā Supply Chain Management nepieciešamo manuālo atjauninājumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="5d1ea-142">Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="5d1ea-143">**SiteId**— vieta ir jānorāda, lai programmā Supply Chain Management ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="5d1ea-144">Noklusējuma vietu var ņemt no preces vai no debitora pasūtījuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="5d1ea-145">Noklusējuma veidnes vērtība ir **1**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="5d1ea-146">**WarehouseId**— noliktava ir jānorāda, lai programmā Supply Chain Management apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="5d1ea-147">Noklusējuma noliktavu var paņemt no preces vai no klienta pasūtījuma virsrakstā programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="5d1ea-148">Noklusējuma veidnes vērtība ir **13**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="5d1ea-149">**LanguageId**— valoda ir jānorāda, lai programmā Supply Chain Management ģenerētu piedāvājumu un pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="5d1ea-150">Pēc noklusējuma tiek izmantota valoda no debitora pasūtījuma virsraksta.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="5d1ea-151">Noklusējuma veidnes vērtība ir **en-us**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5d1ea-152">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="5d1ea-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="5d1ea-153">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** columns aren't included in the default mappings.</span></span> <span data-ttu-id="5d1ea-154">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-154">To map these columns, you must set up a value mapping that is specific to the data in the organizations that the table is synchronized between.</span></span>

<span data-ttu-id="5d1ea-155">Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5d1ea-156">Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5d1ea-156">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

![Veidnes kartējums līdzeklī Datu integrācija](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="5d1ea-158">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="5d1ea-158">Related topics</span></span>


[<span data-ttu-id="5d1ea-159">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="5d1ea-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5d1ea-160">Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5d1ea-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5d1ea-161">Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5d1ea-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="5d1ea-162">Programmā Sales ietverto pārdošanas pasūtījumu tieša sinhronizācija ar programmu Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5d1ea-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="5d1ea-163">Programmā Supply Chain Management ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="5d1ea-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]