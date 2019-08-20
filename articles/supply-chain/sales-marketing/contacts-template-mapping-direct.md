---
title: Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations
description: Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales ietverto elementu Kontaktpersona (kontaktpersonas) un Kontaktpersona (debitori) sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
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
ms.openlocfilehash: fbc75702c9db1e877addc4605dcb444c344dfa5c
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742451"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="7d0d2-103">Programmā Sales ietverto kontaktpersonu tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d0d2-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="7d0d2-104">Pirms risinājuma No potenciāla klienta līdz skaidrai naudai lietošanas izlasiet rakstu [Datu integrēšana pakalpojumā Common Data Service programmām](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="7d0d2-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="7d0d2-105">Šajā tēmā ir apskatītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Sales ietverto elementu Kontaktpersona (kontaktpersonas) un Kontaktpersona (debitori) tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="7d0d2-106">Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="7d0d2-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="7d0d2-107">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantots līdzeklis Datu integrācija, lai sinhronizētu datus programmu Finance and Operations un Sales instancēs.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="7d0d2-108">Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="7d0d2-109">Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="7d0d2-110">[![Datu plūsma risinājumā No potenciālā klienta līdz skaidrai naudai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="7d0d2-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7d0d2-111">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="7d0d2-111">Templates and tasks</span></span>

<span data-ttu-id="7d0d2-112">Lai piekļūtu pieejamajām veidnēm, atveriet [PowerApps administrēšanas centru](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="7d0d2-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="7d0d2-113">Atlasiet **Projekti** un pēc tam augšējā labajā stūrī atlasiet **Jauns projekts**, lai atlasītu publiskās veidnes.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7d0d2-114">Tālāk ir norādītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Sales ietverto kontaktpersonu (Kontaktpersonas) elementu sinhronizēšanai ar kontaktpersonām (Debitori) programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="7d0d2-115">**Veidņu nosaukumi līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="7d0d2-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="7d0d2-116">Kontaktpersonas (no Sales uz Fin and Ops) — tieši</span><span class="sxs-lookup"><span data-stu-id="7d0d2-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="7d0d2-117">Kontaktpersonas kā debitori (no Sales uz Fin and Ops) — tieši</span><span class="sxs-lookup"><span data-stu-id="7d0d2-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="7d0d2-118">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="7d0d2-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="7d0d2-119">Kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="7d0d2-119">Contacts</span></span>
    - <span data-ttu-id="7d0d2-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="7d0d2-120">ContactToCustomer</span></span>

<span data-ttu-id="7d0d2-121">Lai varētu veikt kontaktpersonu sinhronizāciju, ir nepieciešams šāds sinhronizācijas uzdevums: Konti (no Sales uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="7d0d2-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="7d0d2-122">Elementu kopas</span><span class="sxs-lookup"><span data-stu-id="7d0d2-122">Entity sets</span></span>

| <span data-ttu-id="7d0d2-123">Pārdošana</span><span class="sxs-lookup"><span data-stu-id="7d0d2-123">Sales</span></span>    | <span data-ttu-id="7d0d2-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d0d2-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="7d0d2-125">Kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="7d0d2-125">Contacts</span></span> | <span data-ttu-id="7d0d2-126">CDS kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="7d0d2-126">CDS Contacts</span></span>           |
| <span data-ttu-id="7d0d2-127">Kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="7d0d2-127">Contacts</span></span> | <span data-ttu-id="7d0d2-128">Debitori V2</span><span class="sxs-lookup"><span data-stu-id="7d0d2-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="7d0d2-129">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="7d0d2-129">Entity flow</span></span>

<span data-ttu-id="7d0d2-130">Kontaktpersonas tiek pārvaldītas programmā Sales un tiek sinhronizētas ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="7d0d2-131">Programmā Sales ietverta kontaktpersona var tikt sinhronizēta ar programmu Finance and Operations kā kontaktpersona vai debitors.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="7d0d2-132">Lai noteiktu to, vai programmā Sales ietverta kontaktpersona ir jāsinhronizē ar programmu Finance and Operations kā kontaktpersona vai debitors, sistēma pārbauda tālāk norādītos kontaktpersonas rekvizītus programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="7d0d2-133">**Sinhronizēšana ar debitoru programmā Finance and Operations:** kontaktpersonas, kam ir iestatīta lauka **Ir aktīvs debitors** vērtība **Jā**</span><span class="sxs-lookup"><span data-stu-id="7d0d2-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="7d0d2-134">**Sinhronizēšana ar kontaktpersonu programmā Finance and Operations:** kontaktpersonas, kam ir iestatīta lauka **Ir aktīvs debitors** vērtība **Nē** un rekvizīta **Uzņēmums** (pamatkonts/kontaktpersona) vērtība norāda uz kontu (nevis kontaktpersonu).</span><span class="sxs-lookup"><span data-stu-id="7d0d2-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="7d0d2-135">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="7d0d2-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="7d0d2-136">Kontaktpersonai ir pievienots jauns lauks **Ir aktīvs debitors**.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="7d0d2-137">Šis lauks tiek izmantots, lai atšķirtu kontaktpersonas ar pārdošanas aktivitāti no kontaktpersonām bez pārdošanas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="7d0d2-138">Lauks **Ir aktīvs debitors** ir iestatīts uz **Jā** tikai tām kontaktpersonām, kurām pastāv saistīti piedāvājumi, pasūtījumi vai rēķini.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="7d0d2-139">Tikai šīs kontaktpersonas tiek sinhronizētas ar Finance and Operations kā debitori.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="7d0d2-140">Kontaktpersonai ir pievienots jauns lauks **IsCompanyAnAccount**.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="7d0d2-141">Šī lauka vērtība norāda to, vai kontaktpersona ir saistīta ar uzņēmumu (pamatkontu/kontaktpersonu), kura tips ir **Konts**.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="7d0d2-142">Šī informācija tiek izmantota, lai identificētu kontaktpersonas, kas ar Finance and Operations ir jāsinhronizē kā kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="7d0d2-143">Kontaktpersonai ir pievienots jauns lauks **Kontaktpersonas tālrunis**, lai palīdzētu garantēt parastu un unikālu atslēgu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="7d0d2-144">Izveidojot jaunu kontaktpersonu, lauka **Kontaktpersonas tālrunis** vērtība tiek automātiski ģenerēta, izmantojot numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="7d0d2-145">Šī vērtība sastāv no **CON**, kam seko pieaugoša numuru sērija un pēc tam sufikss, ko veido sešas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="7d0d2-146">Piemērs: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="7d0d2-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="7d0d2-147">Kad tiek lietots programmas Sales integrācijas risinājums, izpildot jaunināšanas skriptu, esošo kontaktpersonu lauka **Kontaktpersonas numurs** vērtības tiek iestatītas, izmantojot iepriekš minēto numuru sēriju.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="7d0d2-148">Jaunināšanas skripts iestata arī lauku **Ir aktīvs debitors** uz **Jā** visām kontaktpersonām ar pārdošanas aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="7d0d2-149">Programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d0d2-149">In Finance and Operations</span></span>

<span data-ttu-id="7d0d2-150">Kontaktpersonas tiek atzīmētas, izmantojot rekvizītu **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="7d0d2-151">Šis rekvizīts norāda, ka konkrētā kontaktpersona tiek uzturēta ārēji.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="7d0d2-152">Šajā gadījumā ārēji uzturētās kontaktpersonas tiek uzturētas programmā Sales.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="7d0d2-153">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="7d0d2-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="7d0d2-154">Kontaktpersona ar debitoru</span><span class="sxs-lookup"><span data-stu-id="7d0d2-154">Contact to customer</span></span>

- <span data-ttu-id="7d0d2-155">Lauks **CustomerGroup** programmā Finance and Operations ir obligāts.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="7d0d2-156">Lai palīdzētu nepieļaut sinhronizācijas kļūdām, varat norādīt noklusējuma vērtību kartējumā.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="7d0d2-157">Šo noklusējuma vērtību izmanto, ja lauks programmā Sales ir atstāts tukšs.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="7d0d2-158">Noklusējuma veidnes vērtība ir **10**.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-158">The default template value is **10**.</span></span>

- <span data-ttu-id="7d0d2-159">Pievienojot tālāk norādītos kartējumus, jūs varat samazināt programmā Finance and Operations nepieciešamo manuālo atjauninājumu skaitu.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="7d0d2-160">Varat izmantot noklusējuma vērtību vai arī vērtības karti no, piemēram, lauka **Valsts/reģions** vai **Pilsēta**.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="7d0d2-161">**SiteId** — noklusējuma vietu var definēt arī precēm programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="7d0d2-162">Vieta ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="7d0d2-163">Veidnes vērtība laukam **SiteId** nav definēta.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="7d0d2-164">**WarehouseId** — noklusējuma noliktavu var definēt arī precēm programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="7d0d2-165">Noliktava ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="7d0d2-166">Veidnes vērtība laukam **WarehouseId** nav definēta.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="7d0d2-167">**LanguageId** — valoda ir jānorāda, lai programmā Finance and Operations ģenerētu piedāvājumus un pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="7d0d2-168">Noklusējuma veidnes vērtība ir **en-us**.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7d0d2-169">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="7d0d2-169">Template mapping in Data integration</span></span>

<span data-ttu-id="7d0d2-170">Tālāk esošajos attēlos ir redzams piemērs veidnes kartējumam līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="7d0d2-171">Kartējums norāda to, kuru programmā Sales ietverto lauku informācija tiks sinhronizēta ar programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7d0d2-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="7d0d2-172">Kontaktpersona ar kontaktpersonu</span><span class="sxs-lookup"><span data-stu-id="7d0d2-172">Contact to contact</span></span>

![Veidnes kartējums datu integrētājā](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="7d0d2-174">Kontaktpersona ar debitoru</span><span class="sxs-lookup"><span data-stu-id="7d0d2-174">Contact to customer</span></span>

![Veidnes kartējums datu integrētājā](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="7d0d2-176">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="7d0d2-176">Related topics</span></span>

[<span data-ttu-id="7d0d2-177">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="7d0d2-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="7d0d2-178">Programmā Sales ietverto kontu tieša sinhronizēšana ar debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7d0d2-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="7d0d2-179">Programmā Finance and Operations ietverto preču tieša sinhronizēšana ar precēm programmā Sales</span><span class="sxs-lookup"><span data-stu-id="7d0d2-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="7d0d2-180">Programmā Finance and Operations ietverto pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="7d0d2-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="7d0d2-181">Programmā Finance and Operations ietverto pārdošanas rēķinu galveņu un rindu tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="7d0d2-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)


