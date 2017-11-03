---
title: "Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations"
description: "Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti kontaktpersonu (Kontaktpersonas) un kontaktpersonu (Debitori) sinhronizēšanai no Microsoft Dynamics 365 for Sales ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu."
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
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="27c64-103">Kontaktpersonu sinhronizēšana no Sales ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27c64-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="27c64-104">Pirms izmantojat risinājumu No potenciālā klienta līdz skaidrai naudai, iepazīstiet līdzekli [Dynamics 365 datu integrācija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="27c64-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="27c64-105">Šajā tēmā aplūkotas veidnes un pamata uzdevumi, kas tiek izmantoti kontaktpersonu (Kontaktpersonas) elementu un kontaktpersonu (Debitori) sinhronizēšanai no Microsoft Dynamics 365 for Sales (Sales) ar Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="27c64-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="27c64-106">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="27c64-106">Templates and tasks</span></span>

<span data-ttu-id="27c64-107">Kontaktpersonu (Kontaktpersonas) programmā Sales sinhronizēšanai ar kontaktpersonām (Debitori) programmā Finance and Operations tiek izmantotas tālāk norādītās veidnes un pamata uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="27c64-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="27c64-108">**Veidņu nosaukumi**</span><span class="sxs-lookup"><span data-stu-id="27c64-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="27c64-109">Kontaktpersonas (no Sales uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="27c64-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="27c64-110">Kontaktpersonas ar debitoriem (Sales ar Fin un Ops)</span><span class="sxs-lookup"><span data-stu-id="27c64-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="27c64-111">**Projekta uzdevumu nosaukumi**</span><span class="sxs-lookup"><span data-stu-id="27c64-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="27c64-112">Kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="27c64-112">Contacts</span></span>
    - <span data-ttu-id="27c64-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="27c64-113">ContactToCustomer</span></span>

<span data-ttu-id="27c64-114">Pirms kontaktpersonu sinhronizācijas ir jāveic šāds sinhronizācijas uzdevums: Konti (Sales ar Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="27c64-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="27c64-115">Elementu kopas</span><span class="sxs-lookup"><span data-stu-id="27c64-115">Entity sets</span></span>

| <span data-ttu-id="27c64-116">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="27c64-116">Sales</span></span>    | <span data-ttu-id="27c64-117">CDS</span><span class="sxs-lookup"><span data-stu-id="27c64-117">CDS</span></span>     | <span data-ttu-id="27c64-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27c64-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="27c64-119">Kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="27c64-119">Contacts</span></span> | <span data-ttu-id="27c64-120">Kontaktpersona</span><span class="sxs-lookup"><span data-stu-id="27c64-120">Contact</span></span> | <span data-ttu-id="27c64-121">CDS kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="27c64-121">CDS Contacts</span></span>           |
| <span data-ttu-id="27c64-122">Kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="27c64-122">Contacts</span></span> | <span data-ttu-id="27c64-123">Konts</span><span class="sxs-lookup"><span data-stu-id="27c64-123">Account</span></span> | <span data-ttu-id="27c64-124">Debitori V2</span><span class="sxs-lookup"><span data-stu-id="27c64-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="27c64-125">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="27c64-125">Entity flow</span></span>

<span data-ttu-id="27c64-126">Kontaktpersonas tiek pārvaldītas programmā Sales un sinhronizētas ar Common Data Service (CDS) un Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27c64-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="27c64-127">Kontaktpersona programmā Sales var kļūt par kontaktpersonu pakalpojumā CDS un programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27c64-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="27c64-128">Vai arī tā var kļūt par kontu pakalpojumā CDS un debitoru programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27c64-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="27c64-129">Lai noteiktu, vai kontaktpersona programmā Sales ir jāizdod sinhronizācijai ar CDS un Finance and Operations (piemēram, Kontaktpersonas programmā Sales &gt; Kontaktpersona pakalpojumā CDS &gt; Kontaktpersonas programmā Finance and Operations), sistēma kontaktpersonai programmā Sales aplūko tālāk norādītos rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="27c64-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="27c64-130">**Sinhronizēšana ar kontu pakalpojumā CDS un debitoru programmā Finance and Operations:** kontaktpersonas, kurām vienums **Ir aktīvs debitors** ir iestatīts uz **Jā**</span><span class="sxs-lookup"><span data-stu-id="27c64-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="27c64-131">**Sinhronizēšana ar kontaktpersonu pakalpojumā CDS un kontaktpersonu programmā Finance and Operations:** kontaktpersonas, kurām vienums **Ir aktīvs debitors** ir iestatīts uz **Nē** un **Uzņēmums** (pamatkonts/kontaktpersona) norāda uz kontu (nav kontaktpersona)</span><span class="sxs-lookup"><span data-stu-id="27c64-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="27c64-132">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="27c64-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="27c64-133">Kontaktpersonai ir pievienots jauns lauks **Ir aktīvs debitors**.</span><span class="sxs-lookup"><span data-stu-id="27c64-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="27c64-134">Šis lauks tiek izmantots, lai atšķirtu kontaktpersonas ar pārdošanas aktivitāti no kontaktpersonām bez pārdošanas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="27c64-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="27c64-135">Lauks **Ir aktīvs debitors** ir iestatīts uz **Jā** tikai tām kontaktpersonām, kurām pastāv saistīti piedāvājumi, pasūtījumi vai rēķini.</span><span class="sxs-lookup"><span data-stu-id="27c64-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="27c64-136">Tikai šīs kontaktpersonas tiek sinhronizētas ar Finance and Operations kā debitori.</span><span class="sxs-lookup"><span data-stu-id="27c64-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="27c64-137">Kontaktpersonai ir pievienots jauns lauks **IsCompanyAnAccount**.</span><span class="sxs-lookup"><span data-stu-id="27c64-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="27c64-138">Šis lauks tiek izmantots, lai norādītu, vai kontaktpersona ir piesaistīta uzņēmumam (pamatkonts/kontaktpersona) ar tipu **Konts**.</span><span class="sxs-lookup"><span data-stu-id="27c64-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="27c64-139">Šī informācija tiek izmantota, lai identificētu kontaktpersonas, kas ar Finance and Operations ir jāsinhronizē kā kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="27c64-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="27c64-140">Kontaktpersonai ir pievienots jauns lauks **Kontaktpersonas tālrunis**, lai palīdzētu garantēt parastu un unikālu atslēgu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="27c64-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="27c64-141">Izveidojot jaunu kontaktpersonu, lauka **Kontaktpersonas tālrunis** vērtība tiek automātiski ģenerēta, izmantojot numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="27c64-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="27c64-142">Šī vērtība sastāv no **CON**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="27c64-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="27c64-143">Piemērs: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="27c64-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="27c64-144">Programmai Sales pievienojot tai paredzēto integrācijas risinājumu, jaunināšanas skripts lauku **Kontaktpersonas tālrunis** iestata esošajām kontaktpersonām, izmantojot iepriekš aprakstīto numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="27c64-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="27c64-145">Jaunināšanas skripts iestata arī lauku **Ir aktīvs debitors** uz **Jā** visām kontaktpersonām ar pārdošanas aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="27c64-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="27c64-146">Programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27c64-146">In Finance and Operations</span></span> 

<span data-ttu-id="27c64-147">Kontaktpersonas tiek atzīmētas, izmantojot rekvizītu **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="27c64-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="27c64-148">Šis rekvizīts norāda, ka konkrētā kontaktpersona tiek uzturēta ārēji.</span><span class="sxs-lookup"><span data-stu-id="27c64-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="27c64-149">Šajā gadījumā ārēji uzturētās kontaktpersonas tiek uzturētas programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="27c64-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="27c64-150">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="27c64-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="27c64-151">Kontaktpersona ar kontaktpersonu</span><span class="sxs-lookup"><span data-stu-id="27c64-151">Contact to Contact</span></span>

- <span data-ttu-id="27c64-152">Atjauniniet lauku **CDS organizācijas ID** kartējumā **Avots &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="27c64-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="27c64-153">Noklusējuma **Organization_OrganizationId [organizācijas ID]** veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="27c64-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="27c64-154">Noklusējuma **PrimaryAccount_Organization_OrganizationId [organizācijas ID]** veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="27c64-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="27c64-155">Lauks **Adreses valsts reģiona kods** programmā Finance and Operations ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="27c64-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="27c64-156">Lai izvairītos no sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā **CDS &gt; Operācijas**.</span><span class="sxs-lookup"><span data-stu-id="27c64-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="27c64-157">Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="27c64-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="27c64-158">Lauka **PrimaryAddressCountryRegionISOCode** noklusējuma veidnes vērtība ir **ASV**.</span><span class="sxs-lookup"><span data-stu-id="27c64-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="27c64-159">Pārliecinieties, vai programmā Finance and Operations pastāv vērtība tālāk norādītajam laukam.</span><span class="sxs-lookup"><span data-stu-id="27c64-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="27c64-160">Ja šī informācija programmā Finance and Operations nav nepieciešama, varat noņemt kartējumu no **CDS &gt; Adresāts**.</span><span class="sxs-lookup"><span data-stu-id="27c64-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="27c64-161">**Lauka nosaukums programmā Finance and Operations:** Lēmums</span><span class="sxs-lookup"><span data-stu-id="27c64-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="27c64-162">**Kartējums:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="27c64-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="27c64-163">Kontaktpersona ar debitoru</span><span class="sxs-lookup"><span data-stu-id="27c64-163">Contact to Customer</span></span>

- <span data-ttu-id="27c64-164">Atjauniniet lauku **CDS organizācijas ID** kartējumā **Avots &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="27c64-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="27c64-165">Noklusējuma **Organization_OrganizationId [organizācijas ID]** veidnes vērtība ir **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="27c64-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="27c64-166">Lauks **Adreses valsts reģiona kods** programmā Finance and Operations ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="27c64-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="27c64-167">Lai izvairītos no sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā **CDS &gt; Adresāts**.</span><span class="sxs-lookup"><span data-stu-id="27c64-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="27c64-168">Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="27c64-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="27c64-169">Lauka **PrimaryAddressCountryRegionISOCode** noklusējuma veidnes vērtība ir **ASV**.</span><span class="sxs-lookup"><span data-stu-id="27c64-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="27c64-170">Lauks **CustomerGroup** programmā Finance and Operations ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="27c64-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="27c64-171">Lai izvairītos no sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā **CDS &gt; Adresāts**.</span><span class="sxs-lookup"><span data-stu-id="27c64-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="27c64-172">Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="27c64-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="27c64-173">Lauka **CustomerGroupId** noklusējuma veidnes vērtība ir **10**.</span><span class="sxs-lookup"><span data-stu-id="27c64-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="27c64-174">Pievienojot tālāk norādītos kartējumus no **CDS &gt; Adresāts**, varat palīdzēt samazināt programmā Finance and Operations veikto manuālo atjauninājumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="27c64-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="27c64-175">Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.</span><span class="sxs-lookup"><span data-stu-id="27c64-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="27c64-176">**SiteId** — noklusējuma vietu var definēt arī precēm programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27c64-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="27c64-177">Vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="27c64-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="27c64-178">Veidnes vērtība laukam **SiteId** nav definēta.</span><span class="sxs-lookup"><span data-stu-id="27c64-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="27c64-179">**WarehouseId** — noklusējuma noliktavu var definēt arī precēm programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="27c64-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="27c64-180">Noliktava ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="27c64-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="27c64-181">Veidnes vērtība laukam **WarehouseId** nav definēta.</span><span class="sxs-lookup"><span data-stu-id="27c64-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="27c64-182">**LanguageId** — valoda ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="27c64-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="27c64-183">Lauka **LanguageId** noklusējuma veidnes vērtība ir **lv-lv**.</span><span class="sxs-lookup"><span data-stu-id="27c64-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="27c64-184">Veidnes kartēšana datu integrētājā</span><span class="sxs-lookup"><span data-stu-id="27c64-184">Template mapping in data integrator</span></span>

<span data-ttu-id="27c64-185">Tālāk esošajos attēlos parādīts piemērs ar veidnes kartēšanu datu integrētājā.</span><span class="sxs-lookup"><span data-stu-id="27c64-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="27c64-186">Kontaktpersona ar kontaktpersonu</span><span class="sxs-lookup"><span data-stu-id="27c64-186">Contact to Contact</span></span>

![Veidnes kartēšana datu integrētājā](./media/contacts-template-mapping-data-integrator-1.png)

![Veidnes kartēšana kontaktpersonām datu integrētājā](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="27c64-189">Kontaktpersona ar debitoru</span><span class="sxs-lookup"><span data-stu-id="27c64-189">Contact to Customer</span></span>

![Veidnes kartēšana datu integrētājā](./media/contacts-template-mapping-data-integrator-3.png)

![Veidnes kartēšana kontaktpersonām datu integrētājā](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="27c64-192">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="27c64-192">Related topics</span></span>

[<span data-ttu-id="27c64-193">Preču sinhronizēšana no Finance and Operations ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="27c64-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="27c64-194">Kontu sinhronizēšana no Sales ar debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27c64-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="27c64-195">Pārdošanas piedāvājumu virsrakstu un rindu sinhronizēšana no programmas Sales uz programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27c64-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="27c64-196">Pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="27c64-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="27c64-197">Pārdošanas rēķinu virsrakstu un rindu sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="27c64-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

