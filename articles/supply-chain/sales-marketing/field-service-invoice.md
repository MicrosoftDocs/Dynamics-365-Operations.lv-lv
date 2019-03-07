---
title: Risinājumā Field Service ietverto līguma rēķinu sinhronizēšana ar brīva teksta rēķiniem risinājumā Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto līgumu rēķinu sinhronizēšanai ar brīva teksta rēķiniem programmā Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "333258"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="80bef-103">Programmā Field Service ietverto līgumu rēķinu sinhronizēšana ar brīva teksta rēķiniem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="80bef-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="80bef-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto līgumu rēķinu sinhronizēšanai ar brīva teksta rēķiniem programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80bef-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="80bef-105">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="80bef-105">Templates and tasks</span></span>

<span data-ttu-id="80bef-106">Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu risinājumā Field Service ietverto līguma rēķinu sinhronizēšanu ar brīvā teksta rēķiniem risinājumā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80bef-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="80bef-107">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="80bef-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="80bef-108">Līguma rēķini (no Field Service uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="80bef-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="80bef-109">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="80bef-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="80bef-110">Rēķinu virsraksti</span><span class="sxs-lookup"><span data-stu-id="80bef-110">Invoice headers</span></span>
- <span data-ttu-id="80bef-111">Rēķina rindas</span><span class="sxs-lookup"><span data-stu-id="80bef-111">Invoice lines</span></span>

<span data-ttu-id="80bef-112">Lai varētu veikt līguma rēķinu sinhronizāciju, ir nepieciešama tālāk norādītā sinhronizācija.</span><span class="sxs-lookup"><span data-stu-id="80bef-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="80bef-113">Konti (no Sales uz Fin and Ops) — tieši</span><span class="sxs-lookup"><span data-stu-id="80bef-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="80bef-114">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="80bef-114">Entity set</span></span>

| <span data-ttu-id="80bef-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="80bef-115">Field Service</span></span>  | <span data-ttu-id="80bef-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="80bef-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="80bef-117">rēķini</span><span class="sxs-lookup"><span data-stu-id="80bef-117">invoices</span></span>       | <span data-ttu-id="80bef-118">CDS debitora brīva teksta rēķinu virsraksti</span><span class="sxs-lookup"><span data-stu-id="80bef-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="80bef-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="80bef-119">invoicedetails</span></span> | <span data-ttu-id="80bef-120">CDS debitora brīva teksta rēķinu rindas</span><span class="sxs-lookup"><span data-stu-id="80bef-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="80bef-121">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="80bef-121">Entity flow</span></span>

<span data-ttu-id="80bef-122">Rēķinus, kas ir izveidoti no līguma programmā Field Service, var sinhronizēt ar programmu Finance and Operations, izmantojot Common Data Service (CDS) datu integrācijas projektu.</span><span class="sxs-lookup"><span data-stu-id="80bef-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="80bef-123">Šo rēķinu atjauninājumi tiks sinhronizēti ar brīvā teksta rēķiniem risinājumā Finance and Operations, ja brīvā teksta rēķinu uzskaites statuss ir **Apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="80bef-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="80bef-124">Pēc brīvā teksta rēķinu grāmatošanas risinājumā Finance and Operations un pēc uzskaites statusa atjaunināšanas uz **Pabeigts** vairs nav iespējams sinhronizēt atjauninājumus no Field Service.</span><span class="sxs-lookup"><span data-stu-id="80bef-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="80bef-125">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="80bef-125">Field Service CRM solution</span></span>

<span data-ttu-id="80bef-126">Entītijai **Rēķins** ir pievienots lauks **Ir rindas ar līguma izcelsmi**.</span><span class="sxs-lookup"><span data-stu-id="80bef-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="80bef-127">Šis lauks palīdz nodrošināt, ka tiek sinhronizēti tikai tie rēķini, kas izveidoti no līguma.</span><span class="sxs-lookup"><span data-stu-id="80bef-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="80bef-128">Vērtība ir **patiess**, ja rēķinā ir vismaz viena rēķina rinda, kas izveidota no līguma.</span><span class="sxs-lookup"><span data-stu-id="80bef-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="80bef-129">Entītijai **Rēķina rinda** ir pievienots lauks **Ir līguma izcelsme**.</span><span class="sxs-lookup"><span data-stu-id="80bef-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="80bef-130">Šis lauks palīdz nodrošināt, ka tiek sinhronizētas tikai tās rēķina rindas, kas izveidotas no līguma.</span><span class="sxs-lookup"><span data-stu-id="80bef-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="80bef-131">Vērtība ir **patiess**, ja rēķina rinda izveidota no līguma.</span><span class="sxs-lookup"><span data-stu-id="80bef-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="80bef-132">**Rēķina datums** ir obligāts lauks risinājumā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="80bef-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="80bef-133">Tādēļ laukā ir jābūt vērtībai risinājumā Field Service, pirms tiek veikta sinhronizēšana.</span><span class="sxs-lookup"><span data-stu-id="80bef-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="80bef-134">Lai izpildītu šo prasību, tiek pievienota šāda loģika.</span><span class="sxs-lookup"><span data-stu-id="80bef-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="80bef-135">Ja entītijas **Rēķins** lauks **Rēķina datums** ir tukšs (proti, ja tajā nav vērtības), tajā tiek iestatīts pašreizējais datums, kad tiek pievienota rēķina rinda, kas izveidota no līguma.</span><span class="sxs-lookup"><span data-stu-id="80bef-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="80bef-136">Lietotājs var mainīt lauku **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="80bef-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="80bef-137">Tomēr, kad lietotājs mēģina saglabāt rēķinu, kas izveidots no līguma, tiek parādīta biznesa procesa kļūda, ja rēķinā ir tukšs lauks **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="80bef-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="80bef-138">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="80bef-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="80bef-139">Programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="80bef-139">In Finance and Operations</span></span>

<span data-ttu-id="80bef-140">Integrēšanas veikšanai ir jāiestata rēķina izcelsme, lai atšķirtu tādus brīva teksta rēķinus risinājumā Finance and Operations, kuri izveidoti no līguma rēķiniem risinājumā Field Service.</span><span class="sxs-lookup"><span data-stu-id="80bef-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="80bef-141">Ja rēķina izcelsmes tips ir **Līguma rēķina integrācija**, lauks **Ārējais rēķina numurs** tiek rādīts **Pārdošanas rēķina** virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="80bef-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="80bef-142">Papildus parādīšanai rēķina virsrakstā, informāciju **Ārējais rēķina numurs** var izmantot, lai palīdzētu nodrošināt, ka rēķini, kas izveidoti no Field Service līguma rēķiniem, tiek filtrēti, kad risinājumā Finance and Operations ietvertie rēķini tiek sinhronizēti ar Field Service.</span><span class="sxs-lookup"><span data-stu-id="80bef-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="80bef-143">Atveriet sadaļu **Debitoru parādi** \> **Iestatīšana** \> **Rēķinu izcelsmes kodi**.</span><span class="sxs-lookup"><span data-stu-id="80bef-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="80bef-144">Atlasiet **Jauns**, lai izveidotu jaunu rēķina izcelsmi.</span><span class="sxs-lookup"><span data-stu-id="80bef-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="80bef-145">Laukā **Rēķina izcelsme** ievadiet rēķina izcelsmes nosaukumu, piemēram, **FS**.</span><span class="sxs-lookup"><span data-stu-id="80bef-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="80bef-146">Laukā **Apraksts** ievadiet aprakstu, piemēram, **Field Service līguma rēķins**.</span><span class="sxs-lookup"><span data-stu-id="80bef-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="80bef-147">Atzīmējiet izvēles rūtiņu **Izcelsmes tipa piešķire**.</span><span class="sxs-lookup"><span data-stu-id="80bef-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="80bef-148">Laukā **Rēķina izcelsmes tips** iestatiet vērtību **Līguma rēķina integrācija**.</span><span class="sxs-lookup"><span data-stu-id="80bef-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="80bef-149">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="80bef-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="80bef-150">Datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="80bef-150">In the Data Integration project</span></span>

<span data-ttu-id="80bef-151">Uzdevums: **Rēķina rindas**</span><span class="sxs-lookup"><span data-stu-id="80bef-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="80bef-152">Pārliecinieties, ka noklusējuma vērtība Finance and Operations laukā **Galvenā konta parādāmā vērtība** ir atjaunināta atbilstoši vēlamajai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="80bef-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="80bef-153">Noklusējuma veidnes vērtība ir **401100**.</span><span class="sxs-lookup"><span data-stu-id="80bef-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="80bef-154">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="80bef-154">Template mapping in Data integration</span></span>

<span data-ttu-id="80bef-155">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="80bef-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a><span data-ttu-id="80bef-156">Līguma rēķini (no Field Service uz Fin and Ops): Rēķina virsraksti</span><span class="sxs-lookup"><span data-stu-id="80bef-156">Agreement invoices (Field Service to Fin and Ops): Invoice headers</span></span>

<span data-ttu-id="80bef-157">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="80bef-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a><span data-ttu-id="80bef-158">Līguma rēķini (no Field Service uz Fin and Ops): Rēķina rindas</span><span class="sxs-lookup"><span data-stu-id="80bef-158">Agreement invoices (Field Service to Fin and Ops): Invoice lines</span></span>

<span data-ttu-id="80bef-159">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="80bef-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
