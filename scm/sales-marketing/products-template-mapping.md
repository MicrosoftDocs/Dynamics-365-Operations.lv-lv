---
title: "Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma ar Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="7df12-103">Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="7df12-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="7df12-104">Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="7df12-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="7df12-105">Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma ar Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="7df12-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="7df12-106">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="7df12-106">Template and task</span></span>

<span data-ttu-id="7df12-107">Preču sinhronizēšanai no Microsoft Dynamics 365 for Finance and Operations Enterprise izdevuma (Finance and Operations) ar Microsoft Dynamics 365 for Sales (Sales) tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="7df12-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="7df12-108">Veidnes nosaukums: Preces (Fin and Ops ar Sales)</span><span class="sxs-lookup"><span data-stu-id="7df12-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="7df12-109">Projekta uzdevuma nosaukums: Preces</span><span class="sxs-lookup"><span data-stu-id="7df12-109">Name of task in project: Products</span></span>

<span data-ttu-id="7df12-110">Nepieciešamie sinhronizēšanas uzdevumi pirms preču sinhronizācijas: nav</span><span class="sxs-lookup"><span data-stu-id="7df12-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="7df12-111">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="7df12-111">Entity set</span></span>

| <span data-ttu-id="7df12-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="7df12-112">**Finance and Operations**</span></span> | <span data-ttu-id="7df12-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="7df12-113">**CDS**</span></span> | <span data-ttu-id="7df12-114">**pārdošana;**</span><span class="sxs-lookup"><span data-stu-id="7df12-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="7df12-115">Pārdodamas izlaistās preces</span><span class="sxs-lookup"><span data-stu-id="7df12-115">Sellable released products</span></span> | <span data-ttu-id="7df12-116">Prece</span><span class="sxs-lookup"><span data-stu-id="7df12-116">Product</span></span> | <span data-ttu-id="7df12-117">Preces</span><span class="sxs-lookup"><span data-stu-id="7df12-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="7df12-118">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="7df12-118">Entity flow</span></span>

<span data-ttu-id="7df12-119">Preces tiek pārvaldītas programmā Finance and Operations un sinhronizētas ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="7df12-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="7df12-120">Datu elements **Pārdodamas izlaistās preces** programmā Finance and Operations eksportē tikai pārdodamas preces, un tas nozīmē, ka precēm ir nepieciešamā informācija, kas jāizmanto pārdošanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="7df12-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="7df12-121">Tie paši noteikumi ir spēkā, kad prece tiek validēta, izmantojot funkciju **Validēt** lapā **Izlaistā prece**.</span><span class="sxs-lookup"><span data-stu-id="7df12-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="7df12-122">**Preces numurs** tiek izmantots kā atslēga, proti, preču varianti tiek sinhronizēti pakalpojumā CDS un programmā Sales ar atsevišķiem **Preču ID** katram vienumam **Preces variants**.</span><span class="sxs-lookup"><span data-stu-id="7df12-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="7df12-123">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="7df12-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="7df12-124">Programmā Sales precēm tiek pievienots jauns lauks **Tiek ārēji uzturēts**, lai norādītu, ka konkrētā prece tiek uzturēta ārēji.</span><span class="sxs-lookup"><span data-stu-id="7df12-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="7df12-125">Importēšanas laikā uz programmu Sales vērtība pēc noklusējuma tiek iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7df12-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="7df12-126">**Tiek ārēji uzturēts = Jā**: prece ir no Finance and Operations un nebūs rediģējama programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="7df12-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="7df12-127">**Tiek ārēji uzturēts = Nē**: prece ir ievadīta tieši programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="7df12-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="7df12-128">**Tiek ārēji uzturēts = Tukšs**: prece pastāv programmā Sales pirms risinājuma No potenciālā klienta līdz skaidrai naudai iespējošanas.</span><span class="sxs-lookup"><span data-stu-id="7df12-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="7df12-129">Lauka **Tiek ārēji uzturēts** informācija tiek izmantota, lai nodrošinātu, ka ar Finance and Operations tiek sinhronizēti tikai **Piedāvājumi** un **Pārdošanas pasūtījumi**, kuros preces ir **Ārēji uzturētas preces**.</span><span class="sxs-lookup"><span data-stu-id="7df12-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="7df12-130">**Ārēji uzturētas preces** tiek automātiski pievienotas pirmajam derīgajam vienumam **Cenrādis** ar to pašu valūtu.</span><span class="sxs-lookup"><span data-stu-id="7df12-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="7df12-131">Ņemiet vērā, ka saraksts tiek kārtots alfabētiskā secībā pēc vienuma **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="7df12-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="7df12-132">Preces pārdošanas cena no Finance and Operations tiek izmantota kā cena vienumā **Cenrādis**.</span><span class="sxs-lookup"><span data-stu-id="7df12-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="7df12-133">Tas nozīmē, ka programmā Sales ir nepieciešams vienums **Cenrādis** katram vienumam **Preces pārdošanas valūta** programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7df12-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="7df12-134">Izlaisto pārdodamo preču valūta tiek iestatīta uz uzskaites valūtu juridiskajā personā, no kurienes šī prece ir eksportēta.</span><span class="sxs-lookup"><span data-stu-id="7df12-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="7df12-135">Preču sinhronizācija neizdosies bez vienuma **Cenrādis** ar atbilstošu valūtu.</span><span class="sxs-lookup"><span data-stu-id="7df12-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="7df12-136">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="7df12-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="7df12-137">Pirms veicat pirmo sinhronizāciju, esošajām precēm programmā Finance and Operations ir jaaizpilda **Atšķirīgo preču tabula**.</span><span class="sxs-lookup"><span data-stu-id="7df12-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="7df12-138">Esošās preces netiks sinhronizētas, kamēr nebūs pabeigts šis darbs.</span><span class="sxs-lookup"><span data-stu-id="7df12-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="7df12-139">Programmā Finance and Operations izmantojiet lauku Meklēt, lai atrastu vienumu **Aizpildīt atšķirīgo preču tabulu**.</span><span class="sxs-lookup"><span data-stu-id="7df12-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="7df12-140">Noklikšķiniet uz **Aizpildīt atšķirīgo preču tabulu**, lai palaistu darbu.</span><span class="sxs-lookup"><span data-stu-id="7df12-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="7df12-141">Šis darbs ir jāizpilda vienu reizi.</span><span class="sxs-lookup"><span data-stu-id="7df12-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="7df12-142">Pārliecinieties, vai sadaļā **Avots -\> CDS kartējuma SalesUnitSymbol/DefaultSellingUnitOfMeasure** pārdošanas vienumam **Mērvienība** (UOM) programmā Finance and Operations ir norādīta nepieciešamā **ValueMap** informācija.</span><span class="sxs-lookup"><span data-stu-id="7df12-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="7df12-143">Pārliecinieties, vai mērvienības **Atbalstītās decimāldaļas** atbilst prasībām sadaļā **CDS -\> Adresāts**.</span><span class="sxs-lookup"><span data-stu-id="7df12-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="7df12-144">Ja jums ir nepieciešamas citas vērtības katrai mērvienībai, tās var mainīt, izmantojot mērvienības **ValueMap**, piemēram, [Katrs: 0] un [Mārciņa: 2].</span><span class="sxs-lookup"><span data-stu-id="7df12-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="7df12-145">Veidnes vērtība tiek iestatīta uz noklusējuma vērtību 0.</span><span class="sxs-lookup"><span data-stu-id="7df12-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="7df12-146">Atjauniniet **CDS organizācijas ID Organization_OrganizationId** sadaļā **Avots -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="7df12-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="7df12-147">Veidnes vērtība tiek iestatīta uz noklusējuma vērtību ORG001.</span><span class="sxs-lookup"><span data-stu-id="7df12-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="7df12-148">Atjauniniet vienuma **Vienību grupa** (**defaultuomscheduleid.name**) **ValueMap** sadaļā **CDS -\> Adresāts** tā, lai tas atbilstu vienumam **Vienību grupas** programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="7df12-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="7df12-149">Veidnes vērtība tiek iestatīta uz **Noklusējuma mērvienība**.</span><span class="sxs-lookup"><span data-stu-id="7df12-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="7df12-150">Pārliecinieties, vai visu preču pārdošanas mērvienības no Finance and Operations pastāv programmā Sales ar vienuma **CDS izdošanas saraksti** vērtību.</span><span class="sxs-lookup"><span data-stu-id="7df12-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="7df12-151">Pārliecinieties, vai programmā Sales pastāv **Cenrāži** katrai preču pārdošanas valūtai programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7df12-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="7df12-152">Preces programmā Sales var izveidot ar statusu **Melnraksts** vai **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="7df12-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="7df12-153">Tas tiek kontrolēts programmas Sales sadaļas **Pārdošana** esošajā sadaļā **Sistēmas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="7df12-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="7df12-154">Preces, kas izveidotas ar melnraksta statusu, ir jāaktivizē pirms tos pievienošanas sadaļā **Piedāvājums** vai **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="7df12-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="7df12-155">Veidnes kartēšana datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="7df12-155">Template mapping in data integrator</span></span>

<span data-ttu-id="7df12-156">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="7df12-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Veidnes kartēšana datu integrētājā](./media/products-template-mapping-data-integrator-1.png)

![Veidnes kartēšana precēm datu integrētājā](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="7df12-159">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="7df12-159">Related topics</span></span>

[<span data-ttu-id="7df12-160">Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7df12-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="7df12-161">Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7df12-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="7df12-162">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no Sales ar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7df12-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


