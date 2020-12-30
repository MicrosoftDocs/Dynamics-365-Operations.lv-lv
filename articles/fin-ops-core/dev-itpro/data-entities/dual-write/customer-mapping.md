---
title: Integrētie debitoru pamatdati
description: Šajā tēmā aprakstīta debitoru datu integrācija starp programmām Finance and Operations un Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 801538e320ca78b0cc55bb4e4b8a80d38b9b48d6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685643"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="d4379-103">Integrētie debitoru pamatdati</span><span class="sxs-lookup"><span data-stu-id="d4379-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="d4379-104">Klienta datus var apgūt vairāk nekā vienā Dynamics 365 lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="d4379-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="d4379-105">Piemēram, klienta rinda var rasties, izmantojot pārdošanas darbību programmā Dynamics 365 Sales (modeļa vadītā programmā pakalpojumā Dynamics 365), vai rinda var rasties, izmantojot mazumtirdzniecības darbību pakalpojumā Dynamics 365 Commerce ( Finance and Operations programmā).</span><span class="sxs-lookup"><span data-stu-id="d4379-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="d4379-106">Neatkarīgi no tā, no kurienes radušies klienta dati, tie tiek integrēti aizkulisēs.</span><span class="sxs-lookup"><span data-stu-id="d4379-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="d4379-107">Integrētie klientu pamatdati sniedz jums elastību, lai varētu apgūt klienta datus jebkurā Dynamics 365 lietojumprogrammā, un sniedz visaptverošu skatījumu par klientu visā Dynamics 365 lietojumprogrammu komplektā.</span><span class="sxs-lookup"><span data-stu-id="d4379-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="d4379-108">Debitora datu plūsma</span><span class="sxs-lookup"><span data-stu-id="d4379-108">Customer data flow</span></span>

<span data-ttu-id="d4379-109">*Debitors* ir pareizi definēta koncepcija programmās.</span><span class="sxs-lookup"><span data-stu-id="d4379-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="d4379-110">Tādēļ debitoru datu integrēšana ietver tikai debitora koncepta saskaņošanu starp abām programmām.</span><span class="sxs-lookup"><span data-stu-id="d4379-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="d4379-111">Nākamajā attēlā ir parādīta debitoru datu plūsma.</span><span class="sxs-lookup"><span data-stu-id="d4379-111">The following illustration shows the customer data flow.</span></span>

![Debitora datu plūsma](media/dual-write-customer-data-flow.png)

<span data-ttu-id="d4379-113">Debitorus kopumā var iedalīt divos tipos: komerciālie/organizāciju debitori un debitori/galalietotāji.</span><span class="sxs-lookup"><span data-stu-id="d4379-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="d4379-114">Šie divi debitoru tipi tiek dažādi uzglabāti un apstrādāti programmās Finance and Operations un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d4379-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="d4379-115">Programmā Finance and Operations gan komerciālo/organizāciju debitoru, gan debitoru/galalietotāju pamatdati tiek apkopoti vienā tabulā, kas saucas **CustTable** (CustCustomerV3Entity), un tie tiek klasificēti, pamatojoties uz atribūtu **Veids**.</span><span class="sxs-lookup"><span data-stu-id="d4379-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="d4379-116">(Ja **Tips** ir iestatīts uz **Organizācija**, tad debitors ir komerciāls/organizācijas debitors, un ja **Tips** ir iestatīts uz **Persona**, tad debitors ir debitors/galalietotājs.) Primārā kontaktpersonas informācija tiek apstrādāta, izmantojot SMMContactPersonEntity elementu.</span><span class="sxs-lookup"><span data-stu-id="d4379-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="d4379-117">Programmā Dataverse komerciālie/organizāciju debitoru pamatdati tiek apkopoti Konta elementā, un tiek identificēti kā debitori, kas atribūts **RelationshipType** ir iestatīts uz **Debitorsr**.</span><span class="sxs-lookup"><span data-stu-id="d4379-117">In Dataverse, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="d4379-118">Gan debitorus/galalietotājus, gan kontaktpersonu pārstāv Kontaktpersonas elements.</span><span class="sxs-lookup"><span data-stu-id="d4379-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="d4379-119">Lai nodrošinātu skaidru dalījumu starp debitoru/galalietotāju un kontaktpersonu, elementam **Kontaktpersona** ir Būla karodziņš ar nosaukumu **Pārdodams**.</span><span class="sxs-lookup"><span data-stu-id="d4379-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="d4379-120">Ja **Pārdodams** ir **Patiess**, kontaktpersona ir debitors/galalietotājs, un šai kontaktpersonai var izveidot piedāvājumus un pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="d4379-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="d4379-121">Ja **Pārdodams** ir **Nepatiess**, kontaktpersona ir tikai debitora primārā kontaktpersona.</span><span class="sxs-lookup"><span data-stu-id="d4379-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="d4379-122">Kad nepārdodama kontaktpersona piedalās piedāvājumu vai pasūtījumu procesā **Pārdodams** ir iestatīts kā **Patiess**, lai atzīmētu kontaktpersonu kā pārdodamu kontaktpersonu.</span><span class="sxs-lookup"><span data-stu-id="d4379-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="d4379-123">Kontaktpersona, kas ir kļuvusi par pārdodamu kontaktpersonu, joprojām paliek pārdodama kontaktpersona.</span><span class="sxs-lookup"><span data-stu-id="d4379-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="d4379-124">Veidnes</span><span class="sxs-lookup"><span data-stu-id="d4379-124">Templates</span></span>

<span data-ttu-id="d4379-125">Debitora dati ietver visu informāciju par debitoru, piemēram, debitora grupu, adreses, kontaktinformāciju, maksājuma profilu, rēķina profilu un lojalitātes programmas statusu.</span><span class="sxs-lookup"><span data-stu-id="d4379-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="d4379-126">Tabulas karšu vākšana darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="d4379-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="d4379-127">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="d4379-127">Finance and Operations apps</span></span> | <span data-ttu-id="d4379-128">Citas Dynamics 365 programmas</span><span class="sxs-lookup"><span data-stu-id="d4379-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="d4379-129">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d4379-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="d4379-130">CDS kontaktpersonas V2</span><span class="sxs-lookup"><span data-stu-id="d4379-130">CDS Contacts V2</span></span>             | <span data-ttu-id="d4379-131">kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="d4379-131">contacts</span></span>                        | <span data-ttu-id="d4379-132">Šī veidne sinhronizē visu primāro, sekundāro un terciāro kontaktpersonas informāciju par debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="d4379-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="d4379-133">Debitoru grupas</span><span class="sxs-lookup"><span data-stu-id="d4379-133">Customer groups</span></span>             | <span data-ttu-id="d4379-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="d4379-134">msdyn_customergroups</span></span>            | <span data-ttu-id="d4379-135">Šī veidne sinhronizē debitoru grupas informāciju.</span><span class="sxs-lookup"><span data-stu-id="d4379-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="d4379-136">Debitora maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="d4379-136">Customer payment method</span></span>     | <span data-ttu-id="d4379-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="d4379-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="d4379-138">Šī veidne sinhronizē debitoru maksājuma metodes informāciju.</span><span class="sxs-lookup"><span data-stu-id="d4379-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="d4379-139">Debitori V3</span><span class="sxs-lookup"><span data-stu-id="d4379-139">Customers V3</span></span>                | <span data-ttu-id="d4379-140">konti</span><span class="sxs-lookup"><span data-stu-id="d4379-140">accounts</span></span>                        | <span data-ttu-id="d4379-141">Šī veidne sinhronizē debitora pamatinformāciju komerciāliem un organizācijas debitoriem.</span><span class="sxs-lookup"><span data-stu-id="d4379-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="d4379-142">Debitori V3</span><span class="sxs-lookup"><span data-stu-id="d4379-142">Customers V3</span></span>                | <span data-ttu-id="d4379-143">kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="d4379-143">contacts</span></span>                        | <span data-ttu-id="d4379-144">Šī veidne sinhronizē klienta pamatdatus par debitoriem un gala lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="d4379-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="d4379-145">Nosaukuma afiksi</span><span class="sxs-lookup"><span data-stu-id="d4379-145">Name affixes</span></span>                | <span data-ttu-id="d4379-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="d4379-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="d4379-147">Šī veidne sinhronizē nosaukumu afiksu atsauces datus par debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="d4379-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="d4379-148">Maksāšanas dienu rindas CDS V2</span><span class="sxs-lookup"><span data-stu-id="d4379-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="d4379-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="d4379-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="d4379-150">Šī veidne sinhronizē maksāšanas dienu rindas atsauces datus par debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="d4379-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="d4379-151">Maksāšanas dienas CDS</span><span class="sxs-lookup"><span data-stu-id="d4379-151">Payment days CDS</span></span>            | <span data-ttu-id="d4379-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="d4379-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="d4379-153">Šī veidne sinhronizē maksāšanas dienu atsauces datus par debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="d4379-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="d4379-154">Maksājumu grafika rindas</span><span class="sxs-lookup"><span data-stu-id="d4379-154">Payment schedule lines</span></span>      | <span data-ttu-id="d4379-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="d4379-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="d4379-156">Sinhronizē maksāšanas grafika rindu atsauces datus par debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="d4379-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="d4379-157">Maksājumu grafiks</span><span class="sxs-lookup"><span data-stu-id="d4379-157">Payment schedule</span></span>            | <span data-ttu-id="d4379-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="d4379-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="d4379-159">Šī veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="d4379-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="d4379-160">Apmaksas nosacījumi</span><span class="sxs-lookup"><span data-stu-id="d4379-160">Terms of payment</span></span>            | <span data-ttu-id="d4379-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="d4379-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="d4379-162">Šī veidne sinhronizē maksāšanas nosacījumu (apmaksas nosacījumu) atsauces datus par debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="d4379-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
