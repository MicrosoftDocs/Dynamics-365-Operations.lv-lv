---
title: "Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no Sales ar Finance and Operations"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Sales ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu."
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
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="9ac94-103">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no Sales ar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9ac94-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9ac94-104">Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="9ac94-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="9ac94-105">Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanai no Microsoft Dynamics 365 for Sales (Sales) ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="9ac94-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="9ac94-106">Veidne un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="9ac94-106">Template and tasks</span></span>

<span data-ttu-id="9ac94-107">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanai no Sales ar Finance and Operations tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="9ac94-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="9ac94-108">**Veidnes nosaukums:** Pārdošanas piedāvājumi (Sales ar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="9ac94-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="9ac94-109">**Projekta uzdevumu nosaukumi**</span><span class="sxs-lookup"><span data-stu-id="9ac94-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="9ac94-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9ac94-110">QuoteHeader</span></span>
    - <span data-ttu-id="9ac94-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9ac94-111">QuoteLine</span></span>

<span data-ttu-id="9ac94-112">Pirms pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšanas ir jāveic tālāk norādītie sinhronizācijas uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="9ac94-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="9ac94-113">Preces</span><span class="sxs-lookup"><span data-stu-id="9ac94-113">Products</span></span>
- <span data-ttu-id="9ac94-114">Konti (ja tiek izmantoti)</span><span class="sxs-lookup"><span data-stu-id="9ac94-114">Accounts (if used)</span></span>
- <span data-ttu-id="9ac94-115">Kontaktpersonas (ja tiek izmantotas)</span><span class="sxs-lookup"><span data-stu-id="9ac94-115">Contacts (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="9ac94-116">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="9ac94-116">Entity set</span></span>

| <span data-ttu-id="9ac94-117">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="9ac94-117">Sales</span></span>        | <span data-ttu-id="9ac94-118">CDS</span><span class="sxs-lookup"><span data-stu-id="9ac94-118">CDS</span></span>           | <span data-ttu-id="9ac94-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9ac94-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="9ac94-120">Citāti</span><span class="sxs-lookup"><span data-stu-id="9ac94-120">Quotes</span></span>       | <span data-ttu-id="9ac94-121">Piedāvājums</span><span class="sxs-lookup"><span data-stu-id="9ac94-121">Quotation</span></span>     | <span data-ttu-id="9ac94-122">Pārdošanas piedāvājumu virsraksti</span><span class="sxs-lookup"><span data-stu-id="9ac94-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="9ac94-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="9ac94-123">QuoteDetails</span></span> | <span data-ttu-id="9ac94-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="9ac94-124">QuotationLine</span></span> | <span data-ttu-id="9ac94-125">CDS pārdošanas piedāvājuma rindas</span><span class="sxs-lookup"><span data-stu-id="9ac94-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="9ac94-126">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="9ac94-126">Entity flow</span></span>

<span data-ttu-id="9ac94-127">Pārdošanas piedāvājumi tiek izveidoti programmā Sales un sinhronizēti ar Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ac94-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="9ac94-128">Pārdošanas piedāvājumi no Sales tiek sinhronizēti tikai tad, ja ir izpildīti tālāk norādītie nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="9ac94-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="9ac94-129">Visas preces pārdošanas piedāvājuma rindās ir ārēji uzturētas.</span><span class="sxs-lookup"><span data-stu-id="9ac94-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="9ac94-130">Pārdošanas piedāvājums ir aktīvs vai aktivizēts.</span><span class="sxs-lookup"><span data-stu-id="9ac94-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9ac94-131">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="9ac94-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9ac94-132">Elementam Piedāvājums ir pievienots lauks **Ir tikai ārēji uzturētas preces**, lai konsekventi izsekotu, vai pārdošanas piedāvājumā ir ietvertas tikai ārēji uzturētas preces.</span><span class="sxs-lookup"><span data-stu-id="9ac94-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="9ac94-133">Ja pārdošanas piedāvājumā ir tikai ārēji uzturētas preces, tās tiek uzturētas programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ac94-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="9ac94-134">Šī izturēšanās palīdz nodrošināt, ka nemēģināsit sinhronizēt pārdošanas piedāvājuma rindas ar precēm, kas programmā Finance and Operations ir nezināmas.</span><span class="sxs-lookup"><span data-stu-id="9ac94-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="9ac94-135">Visas preces un rindas piedāvājumā tiek atjauninātas ar lauka **Ir tikai ārēji uzturētas preces** informāciju no piedāvājuma virsraksta.</span><span class="sxs-lookup"><span data-stu-id="9ac94-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="9ac94-136">Šī informācija ir atrodama elementa Piedāvājuma rinda laukā **Piedāvājumam ir tikai ārēji uzturētas preces**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="9ac94-137">Laukus **Atlaide**, **Maksas** un **Nodokļi** kontrolē kompleksi iestatījumi programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ac94-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="9ac94-138">Šie iestatījumi pašlaik neatbalsta integrācijas kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="9ac94-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="9ac94-139">Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** pārvalda un apstrādā programma Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ac94-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="9ac94-140">Programmā Sales risinājums tālāk norādītos laukus pārveido par tikai lasāmiem, jo attiecīgās vērtības netiek sinhronizētas ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ac94-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="9ac94-141">**Tikai lasāmi lauki pārdošanas piedāvājuma virsrakstā:** Atlaide %, Atlaide, Vedmaksa</span><span class="sxs-lookup"><span data-stu-id="9ac94-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="9ac94-142">**Tikai lasāmi lauki pārdošanas piedāvājuma rindās:** Nodokļi</span><span class="sxs-lookup"><span data-stu-id="9ac94-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9ac94-143">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="9ac94-143">Preconditions and mapping setup</span></span>

- <span data-ttu-id="9ac94-144">Pirms sinhronizējat pārdošanas piedāvājumus, programmā Sales atveriet sadaļas **Iestatījumi** &gt; **Administrēšana** &gt; **Sistēmas iestatījumi** &gt; **Pārdošana** un pārliecinieties, vai lauks **Atlaides aprēķināšanas metode** ir iestatīts uz **Vienībai**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-144">Before you synchronize sales quotations, in Sales, go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="9ac94-145">Šis iestatījums palīdz garantēt programmā Sales esošās rindas krājuma atlaides atbilstību iestatījumam programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ac94-145">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="9ac94-146">Pretējā gadījumā atlaide programmā Finance and Operations nebūs pareiza, jo programmā Finance and Operations atlaide tiks nolasīta kā atlaide par vienību pat tad, ja programmā Sales tā bija atlaide par rindu.</span><span class="sxs-lookup"><span data-stu-id="9ac94-146">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>
- <span data-ttu-id="9ac94-147">Programmā Finance and Operations atveriet sadaļas **Debitoru parādi** &gt; **Iestatījumi** &gt; **Debitoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-147">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="9ac94-148">Cilnē **Numuru sērija** atlasiet numuru sēriju pārdošanas piedāvājumiem un pēc tam noklikšķiniet uz **Skatīt detalizētu informāciju**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-148">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="9ac94-149">Pēc tam sadaļā **Vispārīgie iestatījumi** lauku **Manuāli** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-149">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="9ac94-150">Programmā Finance and Operations atveriet sadaļas **Debitoru parādi** &gt; **Iestatījumi** &gt; **Debitoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-150">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="9ac94-151">Pēc tam cilnē **Sūtījumi** lauku **Piegādes datuma kontrole** iestatiet uz **Nav**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-151">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="9ac94-152">Šis iestatījums palīdz novērst sinhronizācijas neizdošanos pārdošanas piedāvājumiem.</span><span class="sxs-lookup"><span data-stu-id="9ac94-152">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="9ac94-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9ac94-153">QuoteHeader</span></span>

- <span data-ttu-id="9ac94-154">Programmā Finance and Operations ir obligāti jāaizpilda lauks **Pieprasītais piegādes datums**; atstājot to tukšu, sinhronizācija neizdosies.</span><span class="sxs-lookup"><span data-stu-id="9ac94-154">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="9ac94-155">Lai novērstu šo problēmu tukša lauka gadījumā, no sadaļas **Avots &gt;CDS** tiek paņemts noklusējuma datums.</span><span class="sxs-lookup"><span data-stu-id="9ac94-155">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="9ac94-156">Šis datums ir jāatjaunina uz vajadzīgo vērtību.</span><span class="sxs-lookup"><span data-stu-id="9ac94-156">The date should be updated to a preferred value.</span></span> <span data-ttu-id="9ac94-157">Pašlaik nevarat ievadīt tādu vērtību kā **Šodien**, lai norādītu šodienas datumu.</span><span class="sxs-lookup"><span data-stu-id="9ac94-157">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="9ac94-158">Ir jāievada konkrēts datums.</span><span class="sxs-lookup"><span data-stu-id="9ac94-158">You must enter a specific date.</span></span> <span data-ttu-id="9ac94-159">Lauka **Pieprasītais piegādes datums** noklusējuma veidnes vērtība ir **01.01.2020.**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-159">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="9ac94-160">Lauks **Adreses valsts reģiona kods** programmā Finance and Operations ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="9ac94-160">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="9ac94-161">Lai palīdzētu novērst sinhronizācijas kļūdas, varat norādīt noklusējuma vērtību, ko izmantot gadījumos, ja lauks programmā Sales ir atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="9ac94-161">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="9ac94-162">Šī noklusējuma vērtība ir noderīga arī tādēļ, ka jums nav manuāli jāievada vērtība laukā **Valsts reģions** vietējām adresēm.</span><span class="sxs-lookup"><span data-stu-id="9ac94-162">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="9ac94-163">Laukam **DeliveryAddressCountryRegionISOCode** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="9ac94-163">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="9ac94-164">Atjauniniet lauka **CDS organizācijas ID** kartējumu sadaļā **Avots &gt; CDS** tā, lai tas atbilstu lauka **CDS organizācija** vērtībai elementā Organizācija.</span><span class="sxs-lookup"><span data-stu-id="9ac94-164">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="9ac94-165">Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-165">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="9ac94-166">Lauka **Account_Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-166">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="9ac94-167">Lauka **InvoiceAccount_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-167">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

### <a name="quoteline"></a><span data-ttu-id="9ac94-168">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9ac94-168">QuoteLine</span></span>

- <span data-ttu-id="9ac94-169">Atjauniniet lauka **CDS organizācijas ID** kartējumu sadaļā **Avots &gt; CDS** tā, lai tas atbilstu lauka **CDS organizācija** vērtībai elementā Organizācija.</span><span class="sxs-lookup"><span data-stu-id="9ac94-169">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="9ac94-170">Lauka **Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-170">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="9ac94-171">Lauka **Product_Organization_Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-171">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="9ac94-172">Lauka **Quotation_Organization_Organization_OrganizationId** noklusējuma veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-172">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="9ac94-173">Programmā Finance and Operations ir obligāti jāaizpilda lauks **Pieprasītais piegādes datums**; atstājot to tukšu, sinhronizācija neizdosies.</span><span class="sxs-lookup"><span data-stu-id="9ac94-173">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="9ac94-174">Lai novērstu šo problēmu tukša lauka gadījumā, no sadaļas **Avots &gt;CDS** tiek paņemts noklusējuma datums.</span><span class="sxs-lookup"><span data-stu-id="9ac94-174">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="9ac94-175">Šis datums ir jāatjaunina uz vajadzīgo vērtību.</span><span class="sxs-lookup"><span data-stu-id="9ac94-175">The date should be updated to a preferred value.</span></span> <span data-ttu-id="9ac94-176">Pašlaik nevarat ievadīt tādu vērtību kā **Šodien**, lai norādītu šodienas datumu.</span><span class="sxs-lookup"><span data-stu-id="9ac94-176">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="9ac94-177">Ir jāievada konkrēts datums.</span><span class="sxs-lookup"><span data-stu-id="9ac94-177">You must enter a specific date.</span></span> <span data-ttu-id="9ac94-178">Lauka **Pieprasītais piegādes datums** noklusējuma veidnes vērtība ir **01.01.2020.**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-178">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="9ac94-179">Varat pievienot tālāk norādītos kartējumus no sadaļas **CDS &gt; Adresāts**, lai palīdzētu nodrošināt piedāvājuma rindu importēšanu programmā Finance and Operations gadījumos, ja nav noklusējuma informācijas no debitora vai preces.</span><span class="sxs-lookup"><span data-stu-id="9ac94-179">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="9ac94-180">**SiteId** — vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="9ac94-180">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="9ac94-181">Laukam **SiteId** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="9ac94-181">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="9ac94-182">**WarehouseId** — noliktava ir jānorāda, lai programmā Finance and Operations apstrādātu piedāvājumu un pārdošanas pasūtījumu rindas.</span><span class="sxs-lookup"><span data-stu-id="9ac94-182">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="9ac94-183">Laukam **WarehouseId** nav noklusējuma veidnes vērtības.</span><span class="sxs-lookup"><span data-stu-id="9ac94-183">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="9ac94-184">Pārliecinieties, vai programmā Finance and Operations pārdošanas mērvienībai (UOM) obligātā vērtības karte ir norādīta lauka **Quantity_UOM** kartējumā **CDS &gt; Adresāts** vienumam **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-184">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="9ac94-185">Veidnes kartēšana datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="9ac94-185">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="9ac94-186">Laukus **Atlaide**, **Maksas** un **Nodokļi** kontrolē kompleksi iestatījumi programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ac94-186">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="9ac94-187">Šie iestatījumi pašlaik neatbalsta integrācijas kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="9ac94-187">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="9ac94-188">Pašreizējā versijā laukus **Cena**, **Atlaide**, **Maksa** un **Nodokļi** apstrādā programma Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9ac94-188">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="9ac94-189">Noklusējuma kartējumos nav iekļauti lauki **Maksājumu nosacījumi**, **Kravu pārvadājumu nosacījumi**, **Piegādes nosacījumi**, **Piegādes metode** un **Piegādes veids**.</span><span class="sxs-lookup"><span data-stu-id="9ac94-189">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="9ac94-190">Lai kartētu šos laukus, ir jāiestata vērtību kartējums, kas ir specifisks datiem organizācijās, kurās tiek sinhronizēts elements.</span><span class="sxs-lookup"><span data-stu-id="9ac94-190">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="9ac94-191">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="9ac94-191">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="9ac94-192">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9ac94-192">QuoteHeader</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="9ac94-195">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9ac94-195">QuoteLine</span></span>

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Veidnes kartēšana datu integrētājā](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="9ac94-198">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="9ac94-198">Related topics</span></span>

[<span data-ttu-id="9ac94-199">Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="9ac94-199">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="9ac94-200">Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9ac94-200">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="9ac94-201">Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9ac94-201">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



