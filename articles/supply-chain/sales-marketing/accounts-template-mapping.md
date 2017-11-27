---
title: "Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti kontu sinhronizēšanai no Microsoft Dynamics 365 for Sales ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="a6c64-103">Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6c64-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a6c64-104">Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="a6c64-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="a6c64-105">Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti kontu sinhronizēšanai no Microsoft Dynamics 365 for Sales (Sales) ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="a6c64-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="a6c64-106">Veidne un uzdevums</span><span class="sxs-lookup"><span data-stu-id="a6c64-106">Template and task</span></span>

<span data-ttu-id="a6c64-107">Kontu sinhronizēšanai no Sales ar Finance and Operations tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="a6c64-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="a6c64-108">**Veidnes nosaukums:** Konti (Sales ar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a6c64-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="a6c64-109">**Projekta uzdevuma nosaukums:** Konti — Konts — Debitori</span><span class="sxs-lookup"><span data-stu-id="a6c64-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="a6c64-110">Nepieciešamie sinhronizēšanas uzdevumi pirms konta/debitora sinhronizācijas: nav</span><span class="sxs-lookup"><span data-stu-id="a6c64-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="a6c64-111">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="a6c64-111">Entity set</span></span>

| <span data-ttu-id="a6c64-112">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="a6c64-112">Sales</span></span>    | <span data-ttu-id="a6c64-113">CDS</span><span class="sxs-lookup"><span data-stu-id="a6c64-113">CDS</span></span>     | <span data-ttu-id="a6c64-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6c64-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="a6c64-115">Konti</span><span class="sxs-lookup"><span data-stu-id="a6c64-115">Accounts</span></span> | <span data-ttu-id="a6c64-116">Konts</span><span class="sxs-lookup"><span data-stu-id="a6c64-116">Account</span></span> | <span data-ttu-id="a6c64-117">Debitori</span><span class="sxs-lookup"><span data-stu-id="a6c64-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="a6c64-118">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="a6c64-118">Entity flow</span></span>

<span data-ttu-id="a6c64-119">Konti tiek pārvaldīti programmā Sales un sinhronizēti ar Finance and Operations kā debitori.</span><span class="sxs-lookup"><span data-stu-id="a6c64-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="a6c64-120">Rekvizīts **Tiek ārēji uzturēts** šiem debitoriem tiek iestatīts uz **Jā**, lai izsekotu debitorus, kas izveidoti no programmas Sales.</span><span class="sxs-lookup"><span data-stu-id="a6c64-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="a6c64-121">Rēķina izrakstīšanas laikā šī informācija tiek izmantota, lai filtrētu rēķinus, kas ir sinhronizēti ar programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="a6c64-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a6c64-122">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="a6c64-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a6c64-123">Lapā **Konts** ir pieejams lauks **Konta numurs**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="a6c64-124">Tas ir izveidots kā parasta un unikāla atslēga integrācijas atbalstam.</span><span class="sxs-lookup"><span data-stu-id="a6c64-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="a6c64-125">Risinājuma Klientu attiecību pārvaldība (CRM) parastās atslēgas līdzeklis var ietekmēt debitorus, kuri jau izmanto lauku **Konta numurs**, bet nelieto unikālās lauka **Konta numurs** vērtības katram kontam.</span><span class="sxs-lookup"><span data-stu-id="a6c64-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="a6c64-126">Pašlaik integrācijas risinājumu neatbalsta šo gadījumu.</span><span class="sxs-lookup"><span data-stu-id="a6c64-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="a6c64-127">Kad tiek izveidots jauns konts un lauka **Konta numurs** vērtība vēl nepastāv, to automātiski ģenerē, izmantojot numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="a6c64-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="a6c64-128">Šī vērtība sastāv no **ACC**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="a6c64-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="a6c64-129">Piemērs: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="a6c64-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="a6c64-130">Lietojot integrācijas risinājumu programmai Sales, jaunināšanas skripts lauku **Konta numurs** iestata esošajiem kontiem programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="a6c64-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="a6c64-131">Ja nav nevienas lauka **Konta numurs** vērtības, tiek izmantota iepriekš aprakstītā numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="a6c64-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a6c64-132">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="a6c64-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="a6c64-133">Programmatūrā Finance and Operations **CustomerGroupId** kartēšana no **CDS &gt; Adresāts** ir jāmaina uz derīgu vērtību.</span><span class="sxs-lookup"><span data-stu-id="a6c64-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="a6c64-134">Varat norādīt noklusējuma vērtību vai arī vērtību varat iestatīt, izmantojot vērtības karti.</span><span class="sxs-lookup"><span data-stu-id="a6c64-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="a6c64-135">Noklusējuma veidnes vērtība ir **10**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-135">The default template value is **10**.</span></span>
- <span data-ttu-id="a6c64-136">Lauks **Adreses valsts reģiona kods** programmā Finance and Operations ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="a6c64-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="a6c64-137">Lai izvairītos no sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā no **CDS &gt; Adresāts**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="a6c64-138">Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="a6c64-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="a6c64-139">Lauka **AddressCountryRegionISOCode** noklusējuma veidnes vērtība ir **ASV**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="a6c64-140">Lauka **DeliveryAddressCountryRegionISOCode** noklusējuma veidnes vērtība ir **ASV**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="a6c64-141">Pievienojot tālāk norādītos kartējumus no **CDS &gt; Adresāts**, varat palīdzēt samazināt programmā Finance and Operations nepieciešamo manuālo atjauninājumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="a6c64-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="a6c64-142">Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="a6c64-143">**SiteId** — vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="a6c64-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="a6c64-144">Noklusējuma vietu var ņemt no preces vai no debitora pasūtījuma virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="a6c64-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="a6c64-145">Lauka **SiteId** noklusējuma veidnes vērtība ir **1**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="a6c64-146">**WarehouseId** — noliktava ir jānorāda, lai programmā Finance and Operations apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="a6c64-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="a6c64-147">Noklusējuma noliktavu var ņemt no preces vai no debitora pasūtījuma virsrakstā programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a6c64-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="a6c64-148">Lauka **WarehouseId** noklusējuma veidnes vērtība ir **13**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="a6c64-149">**LanguageId** — valoda ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="a6c64-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="a6c64-150">Pēc noklusējuma tiek izmantota valoda no debitora pasūtījuma virsraksta.</span><span class="sxs-lookup"><span data-stu-id="a6c64-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="a6c64-151">Lauka **LanguageId** noklusējuma veidnes vērtība ir **lv-lv**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="a6c64-152">Atjauniniet CDS organizācijas ID (**Organization_OrganizationId**) kartējumā **Avots &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="a6c64-153">Noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="a6c64-154">Veidnes kartēšana datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="a6c64-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="a6c64-155">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="a6c64-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="a6c64-156">Lai kartētu šos laukus, ir jāiestata vērtību kartēšana.</span><span class="sxs-lookup"><span data-stu-id="a6c64-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="a6c64-157">Vērtību kartējumi ir specifiski datiem organizācijās, starp kurām ir sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="a6c64-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="a6c64-158">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="a6c64-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Veidnes kartēšana datu integrētājā](./media/accounts-template-mapping-data-integrator-1.png)

![Veidnes kartēšana kontiem datu integrētājā](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="a6c64-161">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="a6c64-161">Related topics</span></span>

[<span data-ttu-id="a6c64-162">Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="a6c64-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="a6c64-163">Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6c64-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="a6c64-164">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no programmas Sales uz programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a6c64-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="a6c64-165">Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="a6c64-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="a6c64-166">Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="a6c64-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




