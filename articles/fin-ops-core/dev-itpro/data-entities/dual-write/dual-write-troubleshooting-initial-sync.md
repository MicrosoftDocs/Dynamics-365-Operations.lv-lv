---
title: Problēmu novēršana sākotnējās sinhronizēšanas laikā
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410085"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="7025e-103">Problēmu novēršana sākotnējās sinhronizēšanas laikā</span><span class="sxs-lookup"><span data-stu-id="7025e-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7025e-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7025e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="7025e-105">Konkrēti, tajā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="7025e-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7025e-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="7025e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="7025e-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="7025e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="7025e-108">Sākotnējās sinhronizācijas kļūdu pārbaude Finance and Operations programmā</span><span class="sxs-lookup"><span data-stu-id="7025e-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="7025e-109">Kad iespējojat kartēšanas veidnes, karšu statusam jābūt **Palaists**.</span><span class="sxs-lookup"><span data-stu-id="7025e-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="7025e-110">Ja statuss ir **Nav palaists**, sākotnējās sinhronizācijas laikā radušās kļūdas.</span><span class="sxs-lookup"><span data-stu-id="7025e-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="7025e-111">Lai skatītu kļūdas, lapā **Duālais ieraksts** atlasiet cilni **Sākotnējās sinhronizācijas informācija**.</span><span class="sxs-lookup"><span data-stu-id="7025e-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Sākotnējās sinhronizācijas detalizētas informācijas cilne](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="7025e-113">Sākotnējo sinhronizāciju nevar pabeigt: 400 nederīgs pieprasījums</span><span class="sxs-lookup"><span data-stu-id="7025e-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="7025e-114">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="7025e-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="7025e-115">Mēģinot palaist kartēšanu un sākotnējo sinhronizēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="7025e-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="7025e-116">*Attālais serveris atgrieza kļūdu: (400) nederīgs pieprasījums.), AX eksportējot radās kļūda*</span><span class="sxs-lookup"><span data-stu-id="7025e-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="7025e-117">Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="7025e-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="7025e-118">Ja šī kļūda rodas konsekventi un nevar pabeigt sākotnējo sinhronizāciju, veiciet tālāk norādītās darbības, lai novērstu šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="7025e-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="7025e-119">Piesakieties programmas Finance and Operations virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="7025e-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="7025e-120">Atveriet Microsoft pārvaldības konsoli.</span><span class="sxs-lookup"><span data-stu-id="7025e-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="7025e-121">Rūtī **Pakalpojumi** pārbaudiet, vai ir palaists Microsoft Dynamics 365 datu importēšanas eksporta struktūras pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="7025e-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="7025e-122">Ja tas ir apturēts, restartējiet to, jo tas tas ir nepieciešams sākotnējai sinhronizēšanai.</span><span class="sxs-lookup"><span data-stu-id="7025e-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="7025e-123">Sākotnējās sinhronizācijas kļūda: 403 aizliegts</span><span class="sxs-lookup"><span data-stu-id="7025e-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="7025e-124">Sākotnējās sinhronizācijas laikā, iespējams, saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="7025e-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="7025e-125">*(\[Aizliegts\], Attālinātais serveris atgrieza kļūdu: (403) Aizliegts.), AX eksportējot radās kļūda*</span><span class="sxs-lookup"><span data-stu-id="7025e-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="7025e-126">Lai novērstu problēmu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="7025e-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="7025e-127">Piesakieties Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="7025e-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="7025e-128">Lapā **Azure Active Directory programma** izdzēsiet klientu **DtAppID** un pēc tam pievienojiet to vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="7025e-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD pieteikumu saraksts](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="7025e-130">Pašatsauces vai cirkulārās atsauces kļūmes sākotnējās sinhronizācijas laikā</span><span class="sxs-lookup"><span data-stu-id="7025e-130">Self-reference or circular-reference failures during initial synchronization</span></span>

<span data-ttu-id="7025e-131">Var tikt parādīts kļūdas ziņojums, ja kādam no kartējumiem ir pašatsauces vai cirkulārās atsauces.</span><span class="sxs-lookup"><span data-stu-id="7025e-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="7025e-132">Kļūdas ietilpst tālāk minētajās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="7025e-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="7025e-133">Kreditori V2 uz msdyn_vendors elementa kartējums</span><span class="sxs-lookup"><span data-stu-id="7025e-133">Vendors V2 to msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="7025e-134">Debitoru V3 uz kontu elementu kartēšana</span><span class="sxs-lookup"><span data-stu-id="7025e-134">Customers V3 to Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="7025e-135">Atrisiniet kļūdu kreditori V2 uz msdyn_vendors elementa kartēšanu</span><span class="sxs-lookup"><span data-stu-id="7025e-135">Resolve an error in Vendors V2 to msdyn_vendors entity mapping</span></span>

<span data-ttu-id="7025e-136">Jums var rasties tālāk minētās sinhronizācijas kļūdas kartēšanā **Kreditori V2** uz **msdyn_vendors**, ja elementos ir esoši ieraksti ar vērtībām laukos **PrimaryContactPersonId** un **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7025e-136">You might run into the following initial sync errors on the **Vendors V2** to **msdyn_vendors** mapping if the entities have existing records with values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="7025e-137">Tas notiek tādēļ, ka **InvoiceVendorAccountNumber** ir pašatsauces lauks un **PrimaryContactPersonId** ir riņķveida atsauce kreditora kartēšanā.</span><span class="sxs-lookup"><span data-stu-id="7025e-137">This because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="7025e-138">*Nevarēja atrisināt lauka GUID: <field>. Uzmeklēšana netika atrasta: <value>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="7025e-138">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

<span data-ttu-id="7025e-139">Tākāk ir minēti daži piemēri.</span><span class="sxs-lookup"><span data-stu-id="7025e-139">Here are a couple of examples:</span></span>

- <span data-ttu-id="7025e-140">*Nevarēja atrisināt ceļvedi laukam: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="7025e-140">*Couldn't resolve the guid for the field: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="7025e-141">*Nevarēja atrisināt ceļvedi laukam: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Uzmeklēšana netika atrasta: 1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1*</span><span class="sxs-lookup"><span data-stu-id="7025e-141">*Couldn't resolve the guid for the field: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*</span></span>

<span data-ttu-id="7025e-142">Ja jums ir ieraksti ar vērtībām šajos laukos kreditora elementā, izpildiet tālāk minētās darbības, kas norādītas sadaļā zemāk, lai sekmīgi pabeigtu sākotnējo sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7025e-142">If you have records with values in these fields in the vendor entity follow the steps in the below section to complete initial sync successfully.</span></span>

1. <span data-ttu-id="7025e-143">Programmā Finance and Operations izdzēsiet laukus **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** kartējumā un saglabājiet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="7025e-143">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping and save the changes.</span></span>

    1. <span data-ttu-id="7025e-144">Dodieties uz duālā ieraksta kartēšanas lapu **Kreditori V2 (msdyn_vendors)** un atlasiet cilni **Elementa kartējumi**. Kreisajā filtrā atlasiet **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="7025e-144">Navigate to the dual-write mapping page for **Vendors V2 (msdyn_vendors)**, and select the **Entity mappings** tab. In the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="7025e-145">Labajā filtrā atlasiet **Pārdošana. Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="7025e-145">In the right filter, select **Sales.Vendor**.</span></span>

    2. <span data-ttu-id="7025e-146">Meklējiet **primarycontactperson**, lai atrastu avota lauku **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="7025e-146">Search for **primarycontactperson** to find the source field **PrimaryContactPersonId**.</span></span>
    
    3. <span data-ttu-id="7025e-147">Noklikšķiniet uz pogas **Darbības** un atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7025e-147">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![pašatsauce vai cinkulārā atsauce Nr. 3](media/vend_selfref3.png)
    
    4. <span data-ttu-id="7025e-149">Atkārtiet, lai dzēstu lauku **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7025e-149">Repeat to delete the **InvoiceVendorAccountNumber** field.</span></span>
    
        ![pašatsauce vai cinkulārā atsauce Nr. 4](media/vend-selfref4.png)
    
    5. <span data-ttu-id="7025e-151">Saglabājiet kartēšanas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="7025e-151">Save the mapping changes.</span></span>

2. <span data-ttu-id="7025e-152">Atspējietot izmaiņu izsekošanu elementam **Kreditori V2**.</span><span class="sxs-lookup"><span data-stu-id="7025e-152">Disable the change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="7025e-153">Pārejiet uz **Datu pārvaldība \> datu entītijas**.</span><span class="sxs-lookup"><span data-stu-id="7025e-153">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="7025e-154">Atlasiet entītiju **Kreditori V2**.</span><span class="sxs-lookup"><span data-stu-id="7025e-154">Select the **Vendors V2** entity.</span></span>
    
    3. <span data-ttu-id="7025e-155">Izvēļņu joslā noklikšķiniet uz **Opcijas** un pēc tam uz **Mainīt izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7025e-155">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![pašatsauce vai cinkulārā atsauce Nr. 5](media/selfref_options.png)
    
    4. <span data-ttu-id="7025e-157">Noklikšķiniet uz **Atspējot Mainīt izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7025e-157">Click **Disable Change Tracking**.</span></span>
    
        ![pašatsauce vai cinkulārā atsauce Nr. 6](media/selfref_tracking.png)

3. <span data-ttu-id="7025e-159">Palaidiet sākotnējo **Kreditori v2 (msdyn_vendors)** kartēšanas sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7025e-159">Run the initial sync of **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="7025e-160">Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.</span><span class="sxs-lookup"><span data-stu-id="7025e-160">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="7025e-161">Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7025e-161">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="7025e-162">Jums ir jāsinhronizē šis kartējums, ja vēlaties sinhronizēt primāro kontaktpersonu lauku kreditoru elementā kā kontaktpersonu ierakstus, kuri arī sākotnēji ir jāsinhronizē.</span><span class="sxs-lookup"><span data-stu-id="7025e-162">You must sync this mapping if you want to sync primary contact field on vendors entity as the contacts records also need to be initial synced.</span></span>

5. <span data-ttu-id="7025e-163">Pievienojiet laukus **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** atpakaļ kartēšānai **Kreditori V2 (msdyn_vendors)** un saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7025e-163">Add the fields **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** back to the **Vendors V2 (msdyn_vendors)** mapping and save the mapping.</span></span>

6. <span data-ttu-id="7025e-164">Palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori v2 (msdyn_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="7025e-164">Run the initial sync again for the **Vendors V2 (msdyn_vendors)** mapping.</span></span> <span data-ttu-id="7025e-165">Visi ieraksti tiks sinhronizēti, jo izmaiņu izsekošana ir atspējota.</span><span class="sxs-lookup"><span data-stu-id="7025e-165">All the records will be synced, because change tracking is disabled.</span></span>

7. <span data-ttu-id="7025e-166">Iespējietot izmaiņu izsekošanu elementam **Kreditors V2**.</span><span class="sxs-lookup"><span data-stu-id="7025e-166">Enable change tracking for the **Vendors V2** entity.</span></span>

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="7025e-167">Novērst kļūdu elementa Debitori V3 uz kontiem kartēšanā</span><span class="sxs-lookup"><span data-stu-id="7025e-167">Resolve an error in Customers V3 to Accounts entity mapping</span></span>

<span data-ttu-id="7025e-168">Jums var rasties tālāk minētās sinhronizācijas kļūdas kartēšanā **Debitori V3** uz **Konti**, ja elementos ir esoši ieraksti ar vērtībām laukos **ContactPersonID** un **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="7025e-168">You might run into the following initial sync errors on the **Customers V3** to **Accounts** mapping if the entities have existing records with values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="7025e-169">Tas notiek tādēļ, ka **InvoiceAccount** ir pašatsauces lauks un **ContactPersonID** ir riņķveida atsauce kreditora kartēšanā.</span><span class="sxs-lookup"><span data-stu-id="7025e-169">This because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="7025e-170">*Nevarēja atrisināt lauka GUID: <field>. Uzmeklēšana netika atrasta: <value>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span><span class="sxs-lookup"><span data-stu-id="7025e-170">*Couldn't resolve the guid for the field: <field>. The lookup was not found: <value>. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*</span></span>

- <span data-ttu-id="7025e-171">*Nevarēja atrisināt ceļvedi laukam: primarycontactid.msdyn_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span><span class="sxs-lookup"><span data-stu-id="7025e-171">*Couldn't resolve the guid for the field: primarycontactid.msdyn_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*</span></span>
- <span data-ttu-id="7025e-172">*Nevarēja atrisināt ceļvedi laukam: msdyn_billingaccount.accountnumber. Uzmeklēšana netika atrasta: 1206-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1*</span><span class="sxs-lookup"><span data-stu-id="7025e-172">*Couldn't resolve the guid for the field: msdyn_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*</span></span>

<span data-ttu-id="7025e-173">Ja jums ir ieraksti ar vērtībām šajos laukos debitora elementā, izpildiet tālāk minētās darbības, kas norādītas sadaļā zemāk, lai sekmīgi pabeigtu sākotnējo sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7025e-173">If you have records with values in these fields in the customer entity follow the steps in the below section to complete initial sync successfully.</span></span> <span data-ttu-id="7025e-174">Varat izmantot šo pieeju jebkurām iebūvētajām entītijām, piemēram, uzņēmumiem un kontaktpersonām.</span><span class="sxs-lookup"><span data-stu-id="7025e-174">You can use this approach for any out-of-the-box entities such Accounts and Contacts.</span></span>

1. <span data-ttu-id="7025e-175">Programmā Finance and Operations izdzēsiet laukus **ContactPersonID** un **InvoiceAccount** no **Debitori V3 (konti)** kartēšanas un saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7025e-175">In the Finance and Operations app, delete the fields **ContactPersonID** and **InvoiceAccount** from the **Customers V3 (accounts)** mapping and save the mapping.</span></span>

    1. <span data-ttu-id="7025e-176">Dodieties uz duālā ieraksta kartēšanas lapu **Debitori V3 (konti)** un atlasiet cilni **Elementa kartējumi**. Kreisajā filtrā atlasiet **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="7025e-176">Navigate to the dual-write mapping page for **Customers V3 (accounts)**, select the **Entity mappings** tab. In the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="7025e-177">Labajā filtrā atlasiet **Common Data Service.konts**.</span><span class="sxs-lookup"><span data-stu-id="7025e-177">In the right filter, select **Common Data Service.Account**.</span></span>

    2. <span data-ttu-id="7025e-178">Meklējiet **kontaktpersonu**, lai atrastu avota lauku **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="7025e-178">Search for **contactperson** to find the source field **ContactPersonID**.</span></span>
    
    3. <span data-ttu-id="7025e-179">Noklikšķiniet uz pogas **Darbības** un atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7025e-179">Click the **Actions** button, and select **Delete**.</span></span>
    
        ![pašatsauce vai cinkulārā atsauce Nr. 3](media/cust_selfref3.png)
    
    4. <span data-ttu-id="7025e-181">Atkārtojiet, lai dzēstu lauku **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="7025e-181">Repeat to delete the **InvoiceAccount** field.</span></span>
    
        ![pašatsauce vai cinkulārā atsauce](media/cust_selfref4.png)
    
    5. <span data-ttu-id="7025e-183">Saglabājiet kartēšanas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="7025e-183">Save the mapping changes.</span></span>

2. <span data-ttu-id="7025e-184">Atspējietot izmaiņu izsekošanu elementam **Debitori V3**.</span><span class="sxs-lookup"><span data-stu-id="7025e-184">Disable the change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="7025e-185">Pārejiet uz **Datu pārvaldība \> datu entītijas**.</span><span class="sxs-lookup"><span data-stu-id="7025e-185">Navigate to **Data management \> Data Entities**.</span></span>
    
    2. <span data-ttu-id="7025e-186">Atlasiet entītiju **Dabitori V3**.</span><span class="sxs-lookup"><span data-stu-id="7025e-186">Select the **Customers V3** entity.</span></span>
    
    3. <span data-ttu-id="7025e-187">Izvēļņu joslā noklikšķiniet uz **Opcijas** un pēc tam uz **Mainīt izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7025e-187">Click **Options** from the menu bar, and then **Change tracking**.</span></span>
    
        ![pašatsauce vai cinkulārā atsauce Nr. 5](media/selfref_options.png)
    
    4. <span data-ttu-id="7025e-189">Noklikšķiniet uz **Atspējot Mainīt izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7025e-189">Click **Disable Change Tracking**.</span></span>
    
        ![pašatsauce vai cinkulārā atsauce Nr. 6](media/selfref_tracking.png)

3. <span data-ttu-id="7025e-191">Palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7025e-191">Run the initial sync for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="7025e-192">Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.</span><span class="sxs-lookup"><span data-stu-id="7025e-192">The initial sync should run successfully without any errors.</span></span>

4. <span data-ttu-id="7025e-193">Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7025e-193">Run the initial sync for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="7025e-194">Ir 2 kartes ar vienādu nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7025e-194">There are 2 maps with the same name.</span></span> <span data-ttu-id="7025e-195">Izvēlieties vienu ar aprakstu **Duālā ieraksta veidne sinhronizācijai starp FO.CDS kreditora V2 kontaktpersonām un CDS.Contacts. Nepieciešama jauna pakotne \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="7025e-195">Select the one with the description **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span> <span data-ttu-id="7025e-196">kartes cilnē **Detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="7025e-196">on the **Details** tab of the map.</span></span>

5. <span data-ttu-id="7025e-197">Pievienojiet laukus **InvoiceAccount** un **ContactPersonId** atpakaļ kartējumam **Debitori V3 (konti)** un saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7025e-197">Add the fields **InvoiceAccount** and **ContactPersonId** back to the **Customers V3 (Accounts)** mapping and save the mapping.</span></span> <span data-ttu-id="7025e-198">Tagad abi laiki **InvoiceAccount** un **ContactPersonId** atkal ir daļa no tiešsaistes sinhronizācijas režīma.</span><span class="sxs-lookup"><span data-stu-id="7025e-198">Now, both the **InvoiceAccount** field and the **ContactPersonId** field are again part of live sync mode.</span></span> <span data-ttu-id="7025e-199">Nākamajā darbībā pabeidziet sākotnējo sinhronizāciju šiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="7025e-199">In the next step, you complete the initial sync for these fields.</span></span>

6. <span data-ttu-id="7025e-200">Atkal palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7025e-200">Run the initial sync again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="7025e-201">Tā kā izmaiņu izsekošana ir atspējota, palaižot sinhronizāciju, tiks sinhronizēti dati **InvoiceAccount** un **ContactPersonId** no Finance and Operations programmas uz Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7025e-201">Because change tracking is disabled, running the sync will sync the data for **InvoiceAccount** and **ContactPersonId** from the Finance and Operations app to Common Data Service.</span></span>

7. <span data-ttu-id="7025e-202">Lai sinhronizētu datus **InvoiceAccount** un **ContactPersonId** no Common Data Service uz Finance and Operations, izmantojiet datu integrācijas projektu.</span><span class="sxs-lookup"><span data-stu-id="7025e-202">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations, you use a data integration project.</span></span>

    1. <span data-ttu-id="7025e-203">Sistēmā Power Apps izveidojiet datu integrācijas projektu starp **Pārdošana.Konts** un **Finance and Operations apps.Customers V3** elementiem.</span><span class="sxs-lookup"><span data-stu-id="7025e-203">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="7025e-204">Datu virzienam jābūt no Common Data Service uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7025e-204">The data direction must be from Common Data Service to the Finance and Operations app.</span></span>  <span data-ttu-id="7025e-205">Tā kā **InvoiceAccount** ir jauns atribūts duālajā ierakstā, iespējams, vēlēsities izlaist sākotnējo sinhronizāciju šim atribūtam.</span><span class="sxs-lookup"><span data-stu-id="7025e-205">Because **InvoiceAccount** is a new attribute in dual-write, you may want to skip initial sync for this attribute.</span></span> <span data-ttu-id="7025e-206">Papildinformāciju skatiet [Datu integrēšana pakalpojumā Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="7025e-206">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="7025e-207">Šajā attēlā ir parādīts projekts, kas atjaunina **CustomerAccount** un **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="7025e-207">The following image shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![pašatsauce vai cinkulārā atsauce](media/cust_selfref6.png)

    2. <span data-ttu-id="7025e-209">Pievienojiet uzņēmuma kritērijus filtram Common Data Service pusē, jo programmā tiks atjaunināti tikai tie ieraksti, kas atbilst filtra kritērijiem programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7025e-209">Add the company criteria in the filter on Common Data Service side, because only the records that match filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="7025e-210">Lai pievienotu filtru, noklikšķiniet uz filtra ikonas.</span><span class="sxs-lookup"><span data-stu-id="7025e-210">To add a filter, click the filter icon.</span></span> <span data-ttu-id="7025e-211">Dialoglodziņā **Rediģēt vaicājumu** varat pievienot filtra vaicājumu, piemēram, **_msdyn_company_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="7025e-211">In the **Edit query** dialog, you can add a filter query like **_msdyn_company_value eq '\<guid\>'**.</span></span> <span data-ttu-id="7025e-212">Ja filtra ikona nav atrodama, izveidojiet atbalsta biļeti, lai lūgtu datu integrācijas grupai iespējot filtra iespēju jūsu nomniekam.</span><span class="sxs-lookup"><span data-stu-id="7025e-212">If the filter icon is not present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span> <span data-ttu-id="7025e-213">Ja neievadāt filtra vaicājumu **_msdyn_company_value**, visi ieraksti tiek sinhronizēti.</span><span class="sxs-lookup"><span data-stu-id="7025e-213">If you do not enter a filter query for **_msdyn_company_value**, then all the records are synced.</span></span>

        ![pašatsauce vai cinkulārā atsauce](media/cust_selfref7.png)

        <span data-ttu-id="7025e-215">Tas pabeidz ierakstu sākotnējo sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7025e-215">This completes the initial sync of the records.</span></span>

8. <span data-ttu-id="7025e-216">Iespējojiet izmaiņu izsekošanu elementam **Debitori V3** programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7025e-216">Enable change tracking for the **Customers V3** entity in the Finance and Operations app.</span></span>

