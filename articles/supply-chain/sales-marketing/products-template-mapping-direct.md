---
title: Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Sales
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar programmu Dynamics 365 Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 06/10/2019
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
ms.openlocfilehash: 38f0db7db0cc4f65d46cd241f75a7274f19f62cf
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251389"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="02f4e-103">Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Sales</span><span class="sxs-lookup"><span data-stu-id="02f4e-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="02f4e-104">Pirms risinājuma No potenciāla klienta līdz skaidrai naudai lietošanas izlasiet rakstu [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="02f4e-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="02f4e-105">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču tiešai sinhronizēšanai ar programmu Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="02f4e-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="02f4e-106">Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="02f4e-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="02f4e-107">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Supply Chain Management un Sales instancēs.</span><span class="sxs-lookup"><span data-stu-id="02f4e-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="02f4e-108">Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="02f4e-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="02f4e-109">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="02f4e-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="02f4e-110">[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="02f4e-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="02f4e-111">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="02f4e-111">Templates and tasks</span></span>

<span data-ttu-id="02f4e-112">Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="02f4e-112">To access the available templates, open [PowerApps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="02f4e-113">Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="02f4e-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="02f4e-114">Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti programmā Supply Chain Management ietverto preču sinhronizēšanai ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="02f4e-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="02f4e-115">**Veidnes nosaukums līdzeklī Datu integrācija:** Preces (no Supply Chain Management uz Sales) — tieši</span><span class="sxs-lookup"><span data-stu-id="02f4e-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="02f4e-116">**Uzdevuma nosaukums līdzekļa Datu integrācija projektā:** Preces</span><span class="sxs-lookup"><span data-stu-id="02f4e-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="02f4e-117">Lai varētu veikt preču sinhronizāciju, nav nepieciešams neviens sinhronizācijas uzdevums.</span><span class="sxs-lookup"><span data-stu-id="02f4e-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="02f4e-118">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="02f4e-118">Entity set</span></span>

| <span data-ttu-id="02f4e-119">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="02f4e-119">Supply Chain Management</span></span>    | <span data-ttu-id="02f4e-120">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="02f4e-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="02f4e-121">Pārdodamas izlaistās preces</span><span class="sxs-lookup"><span data-stu-id="02f4e-121">Sellable released products</span></span> | <span data-ttu-id="02f4e-122">Preces</span><span class="sxs-lookup"><span data-stu-id="02f4e-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="02f4e-123">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="02f4e-123">Entity flow</span></span>

<span data-ttu-id="02f4e-124">Preces tiek pārvaldītas programmā Supply Chain Management un tiek sinhronizēti ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="02f4e-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="02f4e-125">Datu elements **Pārdodamas izlaistās preces** programmā Supply Chain Management nodrošina tikai *pārdodamo* preču eksportēšanu.</span><span class="sxs-lookup"><span data-stu-id="02f4e-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="02f4e-126">Pārdodamās preces ir preces, par kurām ir pieejama informācija, kas ir nepieciešama, lai tās varētu izmantot pārdošanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="02f4e-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="02f4e-127">Tie paši noteikumi attiecas uz preces validāciju, izmantojot funkciju **Validēt** lapā **Izlaistā prece**.</span><span class="sxs-lookup"><span data-stu-id="02f4e-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="02f4e-128">Preces numurs tiek izmantots kā atslēga.</span><span class="sxs-lookup"><span data-stu-id="02f4e-128">The product number is used as a key.</span></span> <span data-ttu-id="02f4e-129">Tāpēc, kad preces varianti tiek sinhronizēti ar programmu Sales, katram preces variantam ir atsevišķs preces ID.</span><span class="sxs-lookup"><span data-stu-id="02f4e-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="02f4e-130">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="02f4e-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="02f4e-131">Programmā Sales precēm ir pievienots jauns lauks **Tiek uzturēts ārēji**, lai norādītu, ka konkrētā prece tiek uzturēta ārēji.</span><span class="sxs-lookup"><span data-stu-id="02f4e-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="02f4e-132">Pēc noklusējuma, veicot importēšanu programmā Sales, tiek iestatīta vērtība **Jā**.</span><span class="sxs-lookup"><span data-stu-id="02f4e-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="02f4e-133">Ir pieejamas šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="02f4e-133">The following values are available:</span></span>

- <span data-ttu-id="02f4e-134">**Jā**— prece ir iegūta no programmas Supply Chain Management, un to nevar rediģēt programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="02f4e-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="02f4e-135">**Nē** – prece ir tieši ievadīta programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="02f4e-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="02f4e-136">**(Tukšs)** – prece bija pieejama programmā Sales pirms risinājuma No potenciālā klienta līdz skaidrai naudai iespējošanas.</span><span class="sxs-lookup"><span data-stu-id="02f4e-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="02f4e-137">Lauks **Tiek uzturēts ārēji** palīdz nodrošināt, ka ar programmu Supply Chain Management tiek sinhronizēti tikai piedāvājumi un pārdošanas pasūtījumi, kas ir saistīti ar ārēji uzturētām precēm.</span><span class="sxs-lookup"><span data-stu-id="02f4e-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="02f4e-138">Ārēji uzturētās preces tiek automātiski pievienotas pirmajam derīgajam cenrādim tajā pašā valūtā.</span><span class="sxs-lookup"><span data-stu-id="02f4e-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="02f4e-139">Cenrāži ir sakārtoti alfabēta secībā pēc nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="02f4e-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="02f4e-140">Kā cena cenrādī tiek izmantota preces pārdošanas cena no programmas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="02f4e-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="02f4e-141">Tāpēc programmā Sales ir jābūt cenrādim atbilstoši katrai preču pārdošanas valūtai programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="02f4e-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="02f4e-142">Kā izlaisto pārdodamo preču valūta tiek iestatīta tās juridiskās personas uzskaites valūta, no kurienes šī prece ir eksportēta.</span><span class="sxs-lookup"><span data-stu-id="02f4e-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="02f4e-143">Preces sinhronizācija neizdosies, ja vien nebūs pieejams cenrādis atbilstošajā valūta.</span><span class="sxs-lookup"><span data-stu-id="02f4e-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="02f4e-144">Varat kontrolēt izmantoto cenrādi ar integrāciju, datu integrācijas projektā kartējot elementu pricelevelid.name [noklusējuma cenrādis (nosaukums)].</span><span class="sxs-lookup"><span data-stu-id="02f4e-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="02f4e-145">Ievadē jāizmanto tikai mazie burti.</span><span class="sxs-lookup"><span data-stu-id="02f4e-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="02f4e-146">Piemēram, modulī Pārdošana cenrāža ar nosaukumu “Standarta” noklusējuma vērtība būtu šāda: mērķa lauks: pricelevelid.name [Noklusējuma cenrādis (nosaukums)] un kartes veids: [ { "transformType": "Default", "defaultValue": "standarta" } ].</span><span class="sxs-lookup"><span data-stu-id="02f4e-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="02f4e-147">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="02f4e-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="02f4e-148">Pirms pirmās sinhronizēšanas reizes esošajām precēm programmā Supply Chain Management ir jāaizpilda tabula Atšķirīga prece.</span><span class="sxs-lookup"><span data-stu-id="02f4e-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="02f4e-149">Esošās preces netiek sinhronizētas, kamēr nav pabeigts šis darbs.</span><span class="sxs-lookup"><span data-stu-id="02f4e-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="02f4e-150">Programmā Supply Chain Management izmantojiet lauku Meklēt, lai atrastu vienumu **Aizpildīt atšķirīgo preču tabulu**.</span><span class="sxs-lookup"><span data-stu-id="02f4e-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="02f4e-151">Atlasiet **Aizpildīt atšķirīgu preču tabulu**, lai palaistu darbu.</span><span class="sxs-lookup"><span data-stu-id="02f4e-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="02f4e-152">Šis darbs ir jāpalaiž tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="02f4e-152">This job must be run only one time.</span></span>

- <span data-ttu-id="02f4e-153">Pārliecinieties, ka kartējumā no **SalesUnitSymbol** uz **DefaultUnit (nosaukums)** pastāv nepieciešamā pārdošanas mērenības (UOM) vērtību karte starp programmām Supply Chain Management un Sales.</span><span class="sxs-lookup"><span data-stu-id="02f4e-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="02f4e-154">Atjauniniet vienuma **Vienību grupa** (**defaultuomscheduleid.name**) vērtību karti atbilstoši vienumam **Vienību grupas** programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="02f4e-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="02f4e-155">Noklusējuma veidnes vērtība ir **Noklusējuma vienība**.</span><span class="sxs-lookup"><span data-stu-id="02f4e-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="02f4e-156">Pārliecinieties, ka programmā Sales pastāv visu preču pārdošanas UOM no programmas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="02f4e-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="02f4e-157">Pārliecinieties, ka programmā Sales pastāv cenrāži katrā preču pārdošanas valūtā no programmas Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="02f4e-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="02f4e-158">Kad programmā Sales tiek izveidotas preces, to statuss var būt **Melnraksts** vai **Aktīva**.</span><span class="sxs-lookup"><span data-stu-id="02f4e-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="02f4e-159">Šī darbība tiek kontrolēta programmas Sales sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana**.</span><span class="sxs-lookup"><span data-stu-id="02f4e-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="02f4e-160">Preces, kam izveides brīdī ir statuss **Melnraksts**, ir jāaktivizē, pirms tās var pievienot piedāvājumiem vai pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="02f4e-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="02f4e-161">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="02f4e-161">Template mapping in Data integration</span></span>

<span data-ttu-id="02f4e-162">Tālāk esošajā attēlā ir redzams piemērs veidnes kartēšanai līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="02f4e-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="02f4e-163">Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="02f4e-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Veidnes kartējums datu integrētājā](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="02f4e-165">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="02f4e-165">Related topics</span></span>

[<span data-ttu-id="02f4e-166">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="02f4e-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="02f4e-167">Programmā Sales esošo kontu tieša sinhronizēšana ar klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="02f4e-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="02f4e-168">Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai klientiem programmā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="02f4e-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="02f4e-169">Programmā Supply Chain Management ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="02f4e-169">Synchronize sales order headers and lines directly from Supply Chain Management to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="02f4e-170">Programmā Supply Chain ManagementSupply Chain Management ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="02f4e-170">Synchronize sales invoice headers and lines directly from Supply Chain ManagementSupply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



