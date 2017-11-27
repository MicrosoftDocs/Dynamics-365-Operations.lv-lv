---
title: "Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma ar Microsoft Dynamics 365 for Sales."
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
ms.openlocfilehash: 6c68c4482cacf70f003669cf335e52e47425d2f7
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="d5911-103">Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="d5911-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="d5911-104">Lai varētu lietot risinājumu No potenciāla klienta līdz skaidrai naudai, vispirms iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="d5911-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="d5911-105">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition ietverto preču tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="d5911-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="d5911-106">Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="d5911-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="d5911-107">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs.</span><span class="sxs-lookup"><span data-stu-id="d5911-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="d5911-108">Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="d5911-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="d5911-109">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="d5911-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="d5911-110">[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="d5911-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d5911-111">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="d5911-111">Templates and tasks</span></span>

<span data-ttu-id="d5911-112">Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="d5911-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="d5911-113">Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="d5911-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="d5911-114">Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti programmā Finance and Operations ietverto preču sinhronizēšanai ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="d5911-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="d5911-115">**Veidnes nosaukums līdzeklī Datu integrācija:** Preces (no Fin and Ops uz Sales) — tieši</span><span class="sxs-lookup"><span data-stu-id="d5911-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="d5911-116">**Uzdevuma nosaukums līdzekļa Datu integrācija projektā:** Preces</span><span class="sxs-lookup"><span data-stu-id="d5911-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="d5911-117">Lai varētu veikt preču sinhronizāciju, nav nepieciešams neviens sinhronizācijas uzdevums.</span><span class="sxs-lookup"><span data-stu-id="d5911-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="d5911-118">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="d5911-118">Entity set</span></span>

| <span data-ttu-id="d5911-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d5911-119">Finance and Operations</span></span>     | <span data-ttu-id="d5911-120">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="d5911-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="d5911-121">Pārdodamas izlaistās preces</span><span class="sxs-lookup"><span data-stu-id="d5911-121">Sellable released products</span></span> | <span data-ttu-id="d5911-122">Preces</span><span class="sxs-lookup"><span data-stu-id="d5911-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="d5911-123">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="d5911-123">Entity flow</span></span>

<span data-ttu-id="d5911-124">Preces tiek pārvaldītas programmā Finance and Operations un sinhronizētas ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="d5911-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="d5911-125">Datu elements **Pārdodamas izlaistās preces** programmā Finance and Operations nodrošina tikai *pārdodamo* preču eksportēšanu.</span><span class="sxs-lookup"><span data-stu-id="d5911-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="d5911-126">Pārdodamās preces ir preces, par kurām ir pieejama informācija, kas ir nepieciešama, lai tās varētu izmantot pārdošanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="d5911-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="d5911-127">Tie paši noteikumi attiecas uz preces validāciju, izmantojot funkciju **Validēt** lapā **Izlaistā prece**.</span><span class="sxs-lookup"><span data-stu-id="d5911-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="d5911-128">Preces numurs tiek izmantots kā atslēga.</span><span class="sxs-lookup"><span data-stu-id="d5911-128">The product number is used as a key.</span></span> <span data-ttu-id="d5911-129">Tāpēc, kad preces varianti tiek sinhronizēti ar programmu Sales, katram preces variantam ir atsevišķs preces ID.</span><span class="sxs-lookup"><span data-stu-id="d5911-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="d5911-130">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="d5911-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="d5911-131">Programmā Sales precēm ir pievienots jauns lauks **Tiek uzturēts ārēji**, lai norādītu, ka konkrētā prece tiek uzturēta ārēji.</span><span class="sxs-lookup"><span data-stu-id="d5911-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="d5911-132">Pēc noklusējuma, veicot importēšanu programmā Sales, tiek iestatīta vērtība **Jā**.</span><span class="sxs-lookup"><span data-stu-id="d5911-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="d5911-133">Ir pieejamas šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="d5911-133">The following values are available:</span></span>

- <span data-ttu-id="d5911-134">**Jā** — prece ir iegūta no programmas Finance and Operations, un to nevar rediģēt programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="d5911-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="d5911-135">**Nē** — prece ir tieši ievadīta programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="d5911-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="d5911-136">**(Tukšs)** — prece bija pieejama programmā Sales pirms risinājuma No potenciālā klienta līdz skaidrai naudai iespējošanas.</span><span class="sxs-lookup"><span data-stu-id="d5911-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="d5911-137">Lauks **Tiek uzturēts ārēji** palīdz nodrošināt, ka ar programmu Finance and Operations tiek sinhronizēti tikai piedāvājumi un pārdošanas pasūtījumi, kas ir saistīti ar ārēji uzturētām precēm.</span><span class="sxs-lookup"><span data-stu-id="d5911-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="d5911-138">Ārēji uzturētās preces tiek automātiski pievienotas pirmajam derīgajam cenrādim tajā pašā valūtā.</span><span class="sxs-lookup"><span data-stu-id="d5911-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="d5911-139">Cenrāži ir sakārtoti alfabēta secībā pēc nosaukuma.</span><span class="sxs-lookup"><span data-stu-id="d5911-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="d5911-140">Kā cena cenrādī tiek izmantota preces pārdošanas cena no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d5911-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="d5911-141">Tāpēc programmā Sales ir jābūt cenrādim atbilstoši katrai preču pārdošanas valūtai programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d5911-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="d5911-142">Kā izlaisto pārdodamo preču valūta tiek iestatīta tās juridiskās personas uzskaites valūta, no kurienes šī prece ir eksportēta.</span><span class="sxs-lookup"><span data-stu-id="d5911-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="d5911-143">Preces sinhronizācija neizdosies, ja vien nebūs pieejams cenrādis atbilstošajā valūta.</span><span class="sxs-lookup"><span data-stu-id="d5911-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="d5911-144">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="d5911-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="d5911-145">Pirms pirmās sinhronizēšanas reizes esošajām precēm programmā Finance and Operations ir jāaizpilda tabula Atšķirīga prece.</span><span class="sxs-lookup"><span data-stu-id="d5911-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="d5911-146">Esošās preces netiek sinhronizētas, kamēr nav pabeigts šis darbs.</span><span class="sxs-lookup"><span data-stu-id="d5911-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="d5911-147">Programmā Finance and Operations izmantojiet lauku Meklēt, lai atrastu vienumu **Aizpildīt atšķirīgo preču tabulu**.</span><span class="sxs-lookup"><span data-stu-id="d5911-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="d5911-148">Atlasiet **Aizpildīt atšķirīgu preču tabulu**, lai palaistu darbu.</span><span class="sxs-lookup"><span data-stu-id="d5911-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="d5911-149">Šis darbs ir jāpalaiž tikai vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="d5911-149">This job must be run only one time.</span></span>

- <span data-ttu-id="d5911-150">Pārliecinieties, ka kartējumā no **SalesUnitSymbol** uz **DefaultUnit (nosaukums)** pastāv nepieciešamā pārdošanas mērenības (UOM) vērtību karte starp programmām Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="d5911-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="d5911-151">Atjauniniet vienuma**Vienību grupa** (**defaultuomscheduleid.name**) vērtību karti atbilstoši vienumam **Vienību grupas** programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="d5911-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="d5911-152">Noklusējuma veidnes vērtība ir **Noklusējuma vienība**.</span><span class="sxs-lookup"><span data-stu-id="d5911-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="d5911-153">Pārliecinieties, ka programmā Sales pastāv visu preču pārdošanas UOM no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d5911-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="d5911-154">Pārliecinieties, ka programmā Sales pastāv cenrāži katrā preču pārdošanas valūtā no programmas Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d5911-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="d5911-155">Kad programmā Sales tiek izveidotas preces, to statuss var būt **Melnraksts** vai **Aktīva**.</span><span class="sxs-lookup"><span data-stu-id="d5911-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="d5911-156">Šī darbība tiek kontrolēta programmas Sales sadaļā **Iestatījumi** > **Administrēšana** > **Sistēmas iestatījumi** > **Pārdošana**.</span><span class="sxs-lookup"><span data-stu-id="d5911-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="d5911-157">Preces, kam izveides brīdī ir statuss **Melnraksts**, ir jāaktivizē, pirms tās var pievienot piedāvājumiem vai pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="d5911-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d5911-158">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="d5911-158">Template mapping in Data integration</span></span>

<span data-ttu-id="d5911-159">Tālāk esošajā attēlā ir redzams piemērs veidnes kartēšanai līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="d5911-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="d5911-160">Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d5911-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Veidnes kartējums datu integrētājā](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="d5911-162">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="d5911-162">Related topics</span></span>

[<span data-ttu-id="d5911-163">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="d5911-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="d5911-164">Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d5911-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="d5911-165">Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d5911-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="d5911-166">Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="d5911-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="d5911-167">Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="d5911-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




