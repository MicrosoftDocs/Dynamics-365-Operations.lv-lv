---
title: "Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma ar Microsoft Dynamics 365 for Sales."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="169b7-103">Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="169b7-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="169b7-104">Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="169b7-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="169b7-105">Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma ar Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="169b7-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="169b7-106">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="169b7-106">Template and task</span></span>

<span data-ttu-id="169b7-107">Preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma (Finance and Operations) ar Microsoft Dynamics 365 for Sales (Sales) tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="169b7-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="169b7-108">Veidnes nosaukums: Preces (Fin and Ops ar Sales)</span><span class="sxs-lookup"><span data-stu-id="169b7-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="169b7-109">Projekta uzdevuma nosaukums: Preces</span><span class="sxs-lookup"><span data-stu-id="169b7-109">Name of task in project: Products</span></span>

<span data-ttu-id="169b7-110">Nepieciešamie sinhronizēšanas uzdevumi pirms preču sinhronizācijas: nav</span><span class="sxs-lookup"><span data-stu-id="169b7-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="169b7-111">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="169b7-111">Entity set</span></span>

| <span data-ttu-id="169b7-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="169b7-112">**Finance and Operations**</span></span> | <span data-ttu-id="169b7-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="169b7-113">**CDS**</span></span> | <span data-ttu-id="169b7-114">**pārdošana;**</span><span class="sxs-lookup"><span data-stu-id="169b7-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="169b7-115">Pārdodamas izlaistās preces</span><span class="sxs-lookup"><span data-stu-id="169b7-115">Sellable released products</span></span> | <span data-ttu-id="169b7-116">Prece</span><span class="sxs-lookup"><span data-stu-id="169b7-116">Product</span></span> | <span data-ttu-id="169b7-117">Preces</span><span class="sxs-lookup"><span data-stu-id="169b7-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="169b7-118">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="169b7-118">Entity flow</span></span>

<span data-ttu-id="169b7-119">Preces tiek pārvaldītas programmā Finance and Operations un sinhronizētas ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="169b7-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="169b7-120">Datu elements **Pārdodamas izlaistās preces** programmā Finance and Operations eksportē tikai pārdodamas preces, un tas nozīmē, ka precēm ir nepieciešamā informācija, kas jāizmanto pārdošanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="169b7-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="169b7-121">Tie paši noteikumi ir spēkā, kad prece tiek validēta, izmantojot funkciju **Validēt** lapā **Izlaistā prece**.</span><span class="sxs-lookup"><span data-stu-id="169b7-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="169b7-122">**Preces numurs** tiek izmantots kā atslēga, proti, preču varianti tiek sinhronizēti pakalpojumā CDS un programmā Sales ar atsevišķiem **Preču ID** katram vienumam **Preces variants**.</span><span class="sxs-lookup"><span data-stu-id="169b7-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="169b7-123">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="169b7-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="169b7-124">Programmā Sales precēm tiek pievienots jauns lauks **Tiek ārēji uzturēts**, lai norādītu, ka konkrētā prece tiek uzturēta ārēji.</span><span class="sxs-lookup"><span data-stu-id="169b7-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="169b7-125">Importēšanas laikā uz programmu Sales vērtība pēc noklusējuma tiek iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="169b7-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="169b7-126">**Tiek ārēji uzturēts = Jā**: prece ir no Finance and Operations un nebūs rediģējama programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="169b7-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="169b7-127">**Tiek ārēji uzturēts = Nē**: prece ir ievadīta tieši programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="169b7-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="169b7-128">**Tiek ārēji uzturēts = Tukšs**: prece pastāv programmā Sales pirms risinājuma No potenciālā klienta līdz skaidrai naudai iespējošanas.</span><span class="sxs-lookup"><span data-stu-id="169b7-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="169b7-129">Lauka **Tiek ārēji uzturēts** informācija tiek izmantota, lai nodrošinātu, ka ar Finance and Operations tiek sinhronizēti tikai **Piedāvājumi** un **Pārdošanas pasūtījumi**, kuros preces ir **Ārēji uzturētas preces**.</span><span class="sxs-lookup"><span data-stu-id="169b7-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="169b7-130">**Ārēji uzturētas preces** tiek automātiski pievienotas pirmajam derīgajam vienumam **Cenrādis** ar to pašu valūtu.</span><span class="sxs-lookup"><span data-stu-id="169b7-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="169b7-131">Ņemiet vērā, ka saraksts tiek kārtots alfabētiskā secībā pēc vienuma **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="169b7-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="169b7-132">Preces pārdošanas cena no Finance and Operations tiek izmantota kā cena vienumā **Cenrādis**.</span><span class="sxs-lookup"><span data-stu-id="169b7-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="169b7-133">Tas nozīmē, ka programmā Sales ir nepieciešams vienums **Cenrādis** katram vienumam **Preces pārdošanas valūta** programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="169b7-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="169b7-134">Izlaisto pārdodamo preču valūta tiek iestatīta uz uzskaites valūtu juridiskajā personā, no kurienes šī prece ir eksportēta.</span><span class="sxs-lookup"><span data-stu-id="169b7-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="169b7-135">Preču sinhronizācija neizdosies bez vienuma **Cenrādis** ar atbilstošu valūtu.</span><span class="sxs-lookup"><span data-stu-id="169b7-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="169b7-136">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="169b7-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="169b7-137">Pirms veicat pirmo sinhronizāciju, esošajām precēm programmā Finance and Operations ir jaaizpilda **Atšķirīgo preču tabula**.</span><span class="sxs-lookup"><span data-stu-id="169b7-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="169b7-138">Esošās preces netiks sinhronizētas, kamēr nebūs pabeigts šis darbs.</span><span class="sxs-lookup"><span data-stu-id="169b7-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="169b7-139">Programmā Finance and Operations izmantojiet lauku Meklēt, lai atrastu vienumu **Aizpildīt atšķirīgo preču tabulu**.</span><span class="sxs-lookup"><span data-stu-id="169b7-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="169b7-140">Noklikšķiniet uz **Aizpildīt atšķirīgo preču tabulu**, lai palaistu darbu.</span><span class="sxs-lookup"><span data-stu-id="169b7-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="169b7-141">Šis darbs ir jāizpilda vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="169b7-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="169b7-142">Pārliecinieties, vai sadaļā **Avots -\> CDS kartējuma SalesUnitSymbol/DefaultSellingUnitOfMeasure** pārdošanas vienumam **Mērvienība** (UOM) programmā Finance and Operations ir norādīta nepieciešamā **ValueMap** informācija.</span><span class="sxs-lookup"><span data-stu-id="169b7-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="169b7-143">Atjauniniet **CDS organizācijas ID Organization_OrganizationId** sadaļā **Avots -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="169b7-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="169b7-144">Veidnes vērtība tiek iestatīta uz noklusējuma vērtību ORG001.</span><span class="sxs-lookup"><span data-stu-id="169b7-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="169b7-145">Atjauniniet vienuma **Vienību grupa** (**defaultuomscheduleid.name**) **ValueMap** sadaļā **CDS -\> Adresāts** tā, lai tas atbilstu vienumam **Vienību grupas** programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="169b7-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="169b7-146">Veidnes vērtība tiek iestatīta uz **Noklusējuma mērvienība**.</span><span class="sxs-lookup"><span data-stu-id="169b7-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="169b7-147">Pārliecinieties, vai visu preču pārdošanas mērvienības no Finance and Operations pastāv programmā Sales ar vienuma **CDS izdošanas saraksti** vērtību.</span><span class="sxs-lookup"><span data-stu-id="169b7-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="169b7-148">Pārliecinieties, vai programmā Sales pastāv **Cenrāži** katrai preču pārdošanas valūtai programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="169b7-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="169b7-149">Preces programmā Sales var izveidot ar statusu **Melnraksts** vai **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="169b7-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="169b7-150">Tas tiek kontrolēts programmas Sales sadaļas **Pārdošana** esošajā sadaļā **Sistēmas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="169b7-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="169b7-151">Preces, kas izveidotas ar melnraksta statusu, ir jāaktivizē pirms tos pievienošanas sadaļā **Piedāvājums** vai **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="169b7-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="169b7-152">Veidnes kartēšana datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="169b7-152">Template mapping in data integrator</span></span>

<span data-ttu-id="169b7-153">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="169b7-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Veidnes kartēšana datu integrētājā](./media/products-template-mapping-data-integrator-1.png)

![Veidnes kartēšana precēm datu integrētājā](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="169b7-156">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="169b7-156">Related topics</span></span>

[<span data-ttu-id="169b7-157">Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="169b7-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="169b7-158">Kontaktpersonu sinhronizēšana no programmas Sales uz kontaktpersonām vai klientiem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="169b7-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="169b7-159">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no programmas Sales uz programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="169b7-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="169b7-160">Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="169b7-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="169b7-161">Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="169b7-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


