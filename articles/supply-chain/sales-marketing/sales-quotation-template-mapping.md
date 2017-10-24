---
title: "Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no Sales ar Finance and Operations"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Sales ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu."
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
ms.openlocfilehash: 9117b5af3beff7290816586f63091b12e357339c
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="f2f96-103">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no Sales ar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f2f96-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f2f96-104">Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="f2f96-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="f2f96-105">Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Sales (Sales) ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="f2f96-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="f2f96-106">Veidne un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="f2f96-106">Template and tasks</span></span>

<span data-ttu-id="f2f96-107">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanai no Sales ar Finance and Operations tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="f2f96-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="f2f96-108">**Veidnes nosaukums:** Pārdošanas piedāvājumi (Sales ar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f2f96-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="f2f96-109">**Projekta uzdevumu nosaukumi**</span><span class="sxs-lookup"><span data-stu-id="f2f96-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="f2f96-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f2f96-110">QuoteHeader</span></span>
    - <span data-ttu-id="f2f96-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f2f96-111">QuoteLine</span></span>

<span data-ttu-id="f2f96-112">Pirms pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanas ir jāveic tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="f2f96-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="f2f96-113">Preces (no Fin and Ops uz Sales)</span><span class="sxs-lookup"><span data-stu-id="f2f96-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="f2f96-114">Konti (no Sales uz Fin and Ops) (ja izmantoti)</span><span class="sxs-lookup"><span data-stu-id="f2f96-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="f2f96-115">Kontaktpersonas uz debitoriem (no Sales uz Fin un Ops) (ja tiek izmantotas)</span><span class="sxs-lookup"><span data-stu-id="f2f96-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="f2f96-116">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="f2f96-116">Entity set</span></span>

| <span data-ttu-id="f2f96-117">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="f2f96-117">Sales</span></span>        | <span data-ttu-id="f2f96-118">CDS</span><span class="sxs-lookup"><span data-stu-id="f2f96-118">CDS</span></span>           | <span data-ttu-id="f2f96-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f2f96-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="f2f96-120">Citāti</span><span class="sxs-lookup"><span data-stu-id="f2f96-120">Quotes</span></span>       | <span data-ttu-id="f2f96-121">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="f2f96-121">Quotation</span></span>     | <span data-ttu-id="f2f96-122">Pārdošanas piedāvājumu virsraksti</span><span class="sxs-lookup"><span data-stu-id="f2f96-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="f2f96-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="f2f96-123">QuoteDetails</span></span> | <span data-ttu-id="f2f96-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="f2f96-124">QuotationLine</span></span> | <span data-ttu-id="f2f96-125">CDS pārdošanas piedāvājuma rindas</span><span class="sxs-lookup"><span data-stu-id="f2f96-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="f2f96-126">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="f2f96-126">Entity flow</span></span>

<span data-ttu-id="f2f96-127">Pārdošanas piedāvājumi tiek izveidoti programmā Sales un sinhronizēti ar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2f96-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="f2f96-128">Pārdošanas piedāvājumi no Sales tiek sinhronizēti tikai tad, ja ir izpildīti tālāk norādītie nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="f2f96-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="f2f96-129">Visas preces pārdošanas piedāvājuma rindās ir ārēji uzturētas.</span><span class="sxs-lookup"><span data-stu-id="f2f96-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="f2f96-130">Pārdošanas piedāvājums ir aktīvs vai aktivizēts.</span><span class="sxs-lookup"><span data-stu-id="f2f96-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f2f96-131">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="f2f96-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="f2f96-132">Elementam Piedāvājums ir pievienots lauks **Ir tikai ārēji uzturētas preces**, lai konsekventi izsekotu, vai pārdošanas piedāvājumā ir ietvertas tikai ārēji uzturētas preces.</span><span class="sxs-lookup"><span data-stu-id="f2f96-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="f2f96-133">Ja pārdošanas piedāvājumā ir tikai ārēji uzturētas preces, tās tiek uzturētas programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2f96-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="f2f96-134">Šī izturēšanās palīdz nodrošināt, ka nemēģināsit sinhronizēt pārdošanas piedāvājuma rindas ar precēm, kas programmā Finance and Operations ir nezināmas.</span><span class="sxs-lookup"><span data-stu-id="f2f96-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="f2f96-135">Visas preces un rindas piedāvājumā tiek atjauninātas ar lauka **Ir tikai ārēji uzturētas preces** informāciju no piedāvājuma virsraksta.</span><span class="sxs-lookup"><span data-stu-id="f2f96-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="f2f96-136">Šī informācija ir atrodama elementa Piedāvājuma rinda laukā **Piedāvājumam ir tikai ārēji uzturētas preces**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="f2f96-137">Laukus **Atlaide**, **Maksas** un **Nodokļi** kontrolē kompleksi iestatījumi programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2f96-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="f2f96-138">Šie iestatījumi pašlaik neatbalsta integrācijas kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="f2f96-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="f2f96-139">Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** pārvalda un apstrādā programma Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2f96-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="f2f96-140">Programmā Sales risinājums tālāk norādītos laukus pārveido par tikai lasāmiem, jo attiecīgās vērtības netiek sinhronizētas ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2f96-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="f2f96-141">**Tikai lasāmi lauki pārdošanas piedāvājuma virsrakstā:** Atlaide %, Atlaide, Vedmaksa</span><span class="sxs-lookup"><span data-stu-id="f2f96-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="f2f96-142">**Tikai lasāmi lauki pārdošanas piedāvājuma rindās:** Nodokļi</span><span class="sxs-lookup"><span data-stu-id="f2f96-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f2f96-143">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="f2f96-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="f2f96-144">Pirms pārdošanas pasūtījumu sinhronizēšanas ir svarīgi sistēmas atjaunināt ar tālāk norādīto iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="f2f96-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="f2f96-145">Iestatīšana programmā Sales</span><span class="sxs-lookup"><span data-stu-id="f2f96-145">Setup in Sales</span></span>

- <span data-ttu-id="f2f96-146">Dodieties uz **Iestatījumi** &gt; **Administrēšana** &gt; **Sistēmas iestatījumi** &gt; **Sales** un pārliecinieties, vai lauks **Atlaides aprēķināšanas metode** ir iestatīts uz **Vienībai**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="f2f96-147">Šis iestatījums palīdz garantēt programmā Sales esošās rindas krājuma atlaides atbilstību iestatījumam programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2f96-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="f2f96-148">Pretējā gadījumā atlaide programmā Finance and Operations nebūs pareiza, jo programmā Finance and Operations atlaide tiks nolasīta kā atlaide par vienību pat tad, ja programmā Sales tā bija atlaide par rindu.</span><span class="sxs-lookup"><span data-stu-id="f2f96-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="f2f96-149">Iestatīšana programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f2f96-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="f2f96-150">Dodieties uz **Debitoru parādi** &gt; **Iestatījumi** &gt; **Debitoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="f2f96-151">Cilnē **Numuru sērija** atlasiet numuru sēriju pārdošanas piedāvājumiem un pēc tam noklikšķiniet uz **Skatīt detalizētu informāciju**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="f2f96-152">Pēc tam sadaļā **Vispārīgie iestatījumi** lauku **Manuāli** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="f2f96-153">Dodieties uz **Debitoru parādi** &gt; **Iestatījumi** &gt; **Debitoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="f2f96-154">Pēc tam cilnē **Sūtījumi** lauku **Piegādes datuma kontrole** iestatiet uz **Nav**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="f2f96-155">Šis iestatījums palīdz novērst sinhronizācijas neizdošanos pārdošanas piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="f2f96-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="f2f96-156">Iestatīšana datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="f2f96-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="f2f96-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f2f96-157">QuoteHeader</span></span>

- <span data-ttu-id="f2f96-158">Programmā Finance and Operations ir obligāti jāaizpilda lauks **Pieprasītais piegādes datums**; atstājot to tukšu, sinhronizācija neizdosies.</span><span class="sxs-lookup"><span data-stu-id="f2f96-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="f2f96-159">Lai novērstu šo problēmu tukša lauka gadījumā, no sadaļas **Avots &gt;CDS** tiek paņemts noklusējuma datums.</span><span class="sxs-lookup"><span data-stu-id="f2f96-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="f2f96-160">Šis datums ir jāatjaunina uz vajadzīgo vērtību.</span><span class="sxs-lookup"><span data-stu-id="f2f96-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="f2f96-161">Pašlaik nevarat ievadīt tādu vērtību kā **Šodien**, lai norādītu šodienas datumu.</span><span class="sxs-lookup"><span data-stu-id="f2f96-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="f2f96-162">Ir jāievada konkrēts datums.</span><span class="sxs-lookup"><span data-stu-id="f2f96-162">You must enter a specific date.</span></span> <span data-ttu-id="f2f96-163">Lauka **Pieprasītais piegādes datums** noklusējuma veidnes vērtība ir **01.01.2020.**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="f2f96-164">Lauks **Adreses valsts reģiona kods** programmā Finance and Operations ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="f2f96-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="f2f96-165">Lai palīdzētu novērst sinhronizācijas kļūdas, varat norādīt noklusējuma vērtību, ko izmantot gadījumos, ja lauks programmā Sales ir atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="f2f96-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="f2f96-166">Šī noklusējuma vērtība ir noderīga arī tādēļ, ka jums nav manuāli jāievada vērtība laukā **Valsts reģions** vietējām adresēm.</span><span class="sxs-lookup"><span data-stu-id="f2f96-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="f2f96-167">Laukam **DeliveryAddressCountryRegionISOCode** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="f2f96-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="f2f96-168">Atjauniniet lauka **CDS organizācijas ID** kartējumu sadaļā **Avots &gt; CDS** tā, lai tas atbilstu lauka **CDS organizācija** vērtībai elementā Organizācija.</span><span class="sxs-lookup"><span data-stu-id="f2f96-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="f2f96-169">Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f2f96-170">Lauka **Account_Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f2f96-171">Lauka **InvoiceAccount_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="f2f96-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f2f96-172">QuoteLine</span></span>

- <span data-ttu-id="f2f96-173">Atjauniniet lauka **CDS organizācijas ID** kartējumu sadaļā **Avots &gt; CDS** tā, lai tas atbilstu lauka **CDS organizācija** vērtībai elementā Organizācija.</span><span class="sxs-lookup"><span data-stu-id="f2f96-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="f2f96-174">Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f2f96-175">Lauka **Product_Organization_Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="f2f96-176">Lauka **Quotation_Organization_Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="f2f96-177">Programmā Finance and Operations ir obligāti jāaizpilda lauks **Pieprasītais piegādes datums**; atstājot to tukšu, sinhronizācija neizdosies.</span><span class="sxs-lookup"><span data-stu-id="f2f96-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="f2f96-178">Lai novērstu šo problēmu tukša lauka gadījumā, no sadaļas **Avots &gt;CDS** tiek paņemts noklusējuma datums.</span><span class="sxs-lookup"><span data-stu-id="f2f96-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="f2f96-179">Šis datums ir jāatjaunina uz vajadzīgo vērtību.</span><span class="sxs-lookup"><span data-stu-id="f2f96-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="f2f96-180">Pašlaik nevarat ievadīt tādu vērtību kā **Šodien**, lai norādītu šodienas datumu.</span><span class="sxs-lookup"><span data-stu-id="f2f96-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="f2f96-181">Ir jāievada konkrēts datums.</span><span class="sxs-lookup"><span data-stu-id="f2f96-181">You must enter a specific date.</span></span> <span data-ttu-id="f2f96-182">Lauka **Pieprasītais piegādes datums** noklusējuma veidnes vērtība ir **01.01.2020.**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="f2f96-183">Varat pievienot tālāk norādītos kartējumus no sadaļas **CDS &gt; Adresāts**, lai palīdzētu nodrošināt piedāvājuma rindu importēšanu programmā Finance and Operations gadījumos, ja nav noklusējuma informācijas no debitora vai preces.</span><span class="sxs-lookup"><span data-stu-id="f2f96-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="f2f96-184">**SiteId** — vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="f2f96-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f2f96-185">Laukam **SiteId** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="f2f96-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="f2f96-186">**WarehouseId** — noliktava ir jānorāda, lai programmā Finance and Operations apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="f2f96-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f2f96-187">Laukam **WarehouseId** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="f2f96-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="f2f96-188">Pārliecinieties, vai programmā Finance and Operations pārdošanas mērvienībai (UOM) obligātā vērtības karte ir norādīta lauka **Quantity_UOM** kartējumā **CDS &gt; Adresāts** vienumam **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="f2f96-189">Veidnes kartēšana datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="f2f96-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="f2f96-190">Laukus **Atlaide**, **Maksas** un **Nodokļi** kontrolē kompleksi iestatījumi programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2f96-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="f2f96-191">Šie iestatījumi pašlaik neatbalsta integrācijas kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="f2f96-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="f2f96-192">Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** apstrādā programma Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f2f96-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="f2f96-193">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="f2f96-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="f2f96-194">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="f2f96-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="f2f96-195">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="f2f96-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="f2f96-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="f2f96-196">QuoteHeader</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="f2f96-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="f2f96-199">QuoteLine</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="f2f96-202">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="f2f96-202">Related topics</span></span>

[<span data-ttu-id="f2f96-203">Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="f2f96-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="f2f96-204">Kontu sinhronizēšana no programmas Sales uz klientiem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f2f96-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="f2f96-205">Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f2f96-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



