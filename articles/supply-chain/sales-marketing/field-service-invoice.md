---
title: Sinhronizējiet līguma rēķinus risinājumā Field Service ar brīva teksta rēķiniem risinājumā Supply Chain Management
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Field Service ietverto līgumu rēķinu sinhronizēšanai ar brīva teksta rēķiniem programmā Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 21a77a0289055285f47323803a484c012e662e3a
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102738"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="25900-103">Sinhronizējiet līguma rēķinus risinājumā Field Service ar brīva teksta rēķiniem risinājumā Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="25900-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="25900-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Dynamics 365 Field Service ietverto līgumu rēķinu sinhronizēšanai ar brīva teksta rēķiniem programmā Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25900-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="25900-105">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="25900-105">Templates and tasks</span></span>

<span data-ttu-id="25900-106">Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu risinājumā Field Service ietverto līguma rēķinu sinhronizēšanu ar brīvā teksta rēķiniem risinājumā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25900-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="25900-107">**Veidnes nosaukums līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="25900-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="25900-108">Līguma rēķini (no Field Service uz Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="25900-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="25900-109">**Uzdevumu nosaukumi datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="25900-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="25900-110">Rēķinu virsraksti</span><span class="sxs-lookup"><span data-stu-id="25900-110">Invoice headers</span></span>
- <span data-ttu-id="25900-111">Rēķina rindas</span><span class="sxs-lookup"><span data-stu-id="25900-111">Invoice lines</span></span>

<span data-ttu-id="25900-112">Lai varētu veikt līguma rēķinu sinhronizāciju, ir nepieciešama tālāk norādītā sinhronizācija.</span><span class="sxs-lookup"><span data-stu-id="25900-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="25900-113">Konti (no Sales uz Supply Chain Management) – Tiešā</span><span class="sxs-lookup"><span data-stu-id="25900-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="25900-114">Elementu kopa</span><span class="sxs-lookup"><span data-stu-id="25900-114">Entity set</span></span>

| <span data-ttu-id="25900-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="25900-115">Field Service</span></span>  | <span data-ttu-id="25900-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="25900-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="25900-117">rēķini</span><span class="sxs-lookup"><span data-stu-id="25900-117">invoices</span></span>       | <span data-ttu-id="25900-118">Dataverse debitora brīva teksta rēķinu galvenes</span><span class="sxs-lookup"><span data-stu-id="25900-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="25900-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="25900-119">invoicedetails</span></span> | <span data-ttu-id="25900-120">Dataverse debitora brīva teksta rēķinu rindas</span><span class="sxs-lookup"><span data-stu-id="25900-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="25900-121">Elementu plūsma</span><span class="sxs-lookup"><span data-stu-id="25900-121">Entity flow</span></span>

<span data-ttu-id="25900-122">Rēķinus, kas ir izveidoti no līguma programmā Field Service, var sinhronizēt ar programmu Supply Chain Management, izmantojot Microsoft Dataverse datu integrācijas projektu.</span><span class="sxs-lookup"><span data-stu-id="25900-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="25900-123">Šo rēķinu atjauninājumi tiks sinhronizēti ar brīvā teksta rēķiniem risinājumā Supply Chain Management, ja brīvā teksta rēķinu uzskaites statuss ir **Apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="25900-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="25900-124">Pēc brīvā teksta rēķinu grāmatošanas risinājumā Supply Chain Management un pēc uzskaites statusa atjaunināšanas uz **Pabeigts** vairs nav iespējams sinhronizēt atjauninājumus no Field Service.</span><span class="sxs-lookup"><span data-stu-id="25900-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="25900-125">Risinājums Field Service CRM</span><span class="sxs-lookup"><span data-stu-id="25900-125">Field Service CRM solution</span></span>

<span data-ttu-id="25900-126">Tabulai **Rēķins** ir pievienota kolonna **Ir rindas ar līguma izcelsmi**.</span><span class="sxs-lookup"><span data-stu-id="25900-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="25900-127">Šī kolonna palīdz nodrošināt tikai to rēķinu sinhronizāciju, kas izveidoti no līguma.</span><span class="sxs-lookup"><span data-stu-id="25900-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="25900-128">Vērtība ir **patiess**, ja rēķinā ir vismaz viena rēķina rinda, kas izveidota no līguma.</span><span class="sxs-lookup"><span data-stu-id="25900-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="25900-129">Tabulai **Rēķina rinda** ir pievienota kolonna **Ir līguma izcelsme**.</span><span class="sxs-lookup"><span data-stu-id="25900-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="25900-130">Šī kolonna palīdz nodrošināt tikai to rēķinu rindu sinhronizāciju, kas izveidotas no līguma.</span><span class="sxs-lookup"><span data-stu-id="25900-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="25900-131">Vērtība ir **patiess**, ja rēķina rinda izveidota no līguma.</span><span class="sxs-lookup"><span data-stu-id="25900-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="25900-132">**Rēķina datums** ir obligāts lauks risinājumā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25900-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="25900-133">Tādēļ kolonnā ir jābūt vērtībai risinājumā Field Service, pirms tiek veikta sinhronizēšana.</span><span class="sxs-lookup"><span data-stu-id="25900-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="25900-134">Lai izpildītu šo prasību, tiek pievienota šāda loģika.</span><span class="sxs-lookup"><span data-stu-id="25900-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="25900-135">Ja tabulas **Rēķins** kolonna **Rēķina datums** ir tukšs (proti, ja tajā nav vērtības), tajā tiek iestatīts pašreizējais datums, kad tiek pievienota rēķina rinda, kas izveidota no līguma.</span><span class="sxs-lookup"><span data-stu-id="25900-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="25900-136">Lietotājs var mainīt kolonnu **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="25900-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="25900-137">Tomēr, kad lietotājs mēģina saglabāt rēķinu, kas izveidots no līguma, tiek parādīta biznesa procesa kļūda, ja rēķinā ir tukša kolonna **Rēķina datums**.</span><span class="sxs-lookup"><span data-stu-id="25900-137">However, when the user tries to save an invoice that originates from an agreement, they receive a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="25900-138">Priekšnosacījumi un kartējuma iestatījums</span><span class="sxs-lookup"><span data-stu-id="25900-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="25900-139">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="25900-139">In Supply Chain Management</span></span>

<span data-ttu-id="25900-140">Integrēšanas veikšanai ir jāiestata rēķina izcelsme, lai atšķirtu tādus brīva teksta rēķinus risinājumā Supply Chain Management, kuri izveidoti no līguma rēķiniem risinājumā Field Service.</span><span class="sxs-lookup"><span data-stu-id="25900-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="25900-141">Ja rēķina izcelsmes tips ir **Līguma rēķina integrācija**, lauks **Ārējais rēķina numurs** tiek rādīts **Pārdošanas rēķina** virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="25900-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="25900-142">Papildus parādīšanai rēķina virsrakstā, informāciju **Ārējais rēķina numurs** var izmantot, lai palīdzētu nodrošināt, ka rēķini, kas izveidoti no Field Service līguma rēķiniem, tiek filtrēti, kad risinājumā Supply Chain Management ietvertie rēķini tiek sinhronizēti ar Field Service.</span><span class="sxs-lookup"><span data-stu-id="25900-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="25900-143">Atveriet sadaļu **Debitoru parādi** \> **Iestatīšana** \> **Rēķinu izcelsmes kodi**.</span><span class="sxs-lookup"><span data-stu-id="25900-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="25900-144">Atlasiet **Jauns**, lai izveidotu jaunu rēķina izcelsmi.</span><span class="sxs-lookup"><span data-stu-id="25900-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="25900-145">Laukā **Rēķina izcelsme** ievadiet rēķina izcelsmes nosaukumu, piemēram, **FS**.</span><span class="sxs-lookup"><span data-stu-id="25900-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="25900-146">Laukā **Apraksts** ievadiet aprakstu, piemēram, **Field Service līguma rēķins**.</span><span class="sxs-lookup"><span data-stu-id="25900-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="25900-147">Atzīmējiet izvēles rūtiņu **Izcelsmes tipa piešķire**.</span><span class="sxs-lookup"><span data-stu-id="25900-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="25900-148">Laukā **Rēķina izcelsmes tips** iestatiet vērtību **Līguma rēķina integrācija**.</span><span class="sxs-lookup"><span data-stu-id="25900-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="25900-149">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="25900-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="25900-150">Datu integrācijas projektā</span><span class="sxs-lookup"><span data-stu-id="25900-150">In the Data Integration project</span></span>

<span data-ttu-id="25900-151">Uzdevums: **Rēķina rindas**</span><span class="sxs-lookup"><span data-stu-id="25900-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="25900-152">Pārliecinieties, ka noklusējuma vērtība Supply Chain Management laukā **Galvenā konta parādāmā vērtība** ir atjaunināta atbilstoši vēlamajai vērtībai.</span><span class="sxs-lookup"><span data-stu-id="25900-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="25900-153">Noklusējuma veidnes vērtība ir **401100**.</span><span class="sxs-lookup"><span data-stu-id="25900-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="25900-154">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="25900-154">Template mapping in Data integration</span></span>

<span data-ttu-id="25900-155">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="25900-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="25900-156">Līguma rēķini (no Field Service uz Supply Chain Management): Rēķinu galvenes</span><span class="sxs-lookup"><span data-stu-id="25900-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="25900-157">[![Veidņu kartēšana Rēķinu virsrakstu datu integrācijā](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="25900-157">[![Template mapping in Data integration for invoice headers](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="25900-158">Līguma rēķini (no Field Service uz Supply Chain Management): Rēķinu rindas</span><span class="sxs-lookup"><span data-stu-id="25900-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="25900-159">[![Veidņu kartēšana Rēķinu rindu datu integrācijā](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="25900-159">[![Template mapping in Data integration for invoice lines](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]