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
ms.openlocfilehash: e4ee3bf07a1df445875197f38f655464cc9b44d3
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443853"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="7f620-103">Problēmu novēršana sākotnējās sinhronizēšanas laikā</span><span class="sxs-lookup"><span data-stu-id="7f620-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f620-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7f620-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="7f620-105">Konkrēti, tajā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="7f620-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f620-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="7f620-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="7f620-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="7f620-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="7f620-108">Sākotnējās sinhronizācijas kļūdu pārbaude Finance and Operations programmā</span><span class="sxs-lookup"><span data-stu-id="7f620-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="7f620-109">Kad iespējojat kartēšanas veidnes, karšu statusam jābūt **Palaists**.</span><span class="sxs-lookup"><span data-stu-id="7f620-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="7f620-110">Ja statuss ir **Nav palaists**, sākotnējās sinhronizācijas laikā radušās kļūdas.</span><span class="sxs-lookup"><span data-stu-id="7f620-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="7f620-111">Lai skatītu kļūdas, lapā **Duālais ieraksts** atlasiet cilni **Sākotnējās sinhronizācijas informācija**.</span><span class="sxs-lookup"><span data-stu-id="7f620-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Kļūda cilnē Sākotnējā sinhronizācijas informācija](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="7f620-113">Sākotnējo sinhronizāciju nevar pabeigt: 400 nederīgs pieprasījums</span><span class="sxs-lookup"><span data-stu-id="7f620-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="7f620-114">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="7f620-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="7f620-115">Mēģinot palaist kartēšanu un sākotnējo sinhronizēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="7f620-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="7f620-116">*(\[Nederīgs pieprasījums\], Attālais serveris atgrieza kļūdu: (400) nederīgs pieprasījums.), AX eksportējot radās kļūda*</span><span class="sxs-lookup"><span data-stu-id="7f620-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="7f620-117">Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="7f620-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="7f620-118">Ja šī kļūda rodas konsekventi un nevar pabeigt sākotnējo sinhronizāciju, veiciet tālāk norādītās darbības, lai novērstu šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="7f620-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="7f620-119">Piesakieties programmas Finance and Operations virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="7f620-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="7f620-120">Atveriet Microsoft pārvaldības konsoli.</span><span class="sxs-lookup"><span data-stu-id="7f620-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="7f620-121">Rūtī **Pakalpojumi** pārbaudiet, vai ir palaists Microsoft Dynamics 365 datu importēšanas eksporta struktūras pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="7f620-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="7f620-122">Ja tas ir apturēts, restartējiet to, jo tas tas ir nepieciešams sākotnējai sinhronizēšanai.</span><span class="sxs-lookup"><span data-stu-id="7f620-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="7f620-123">Sākotnējās sinhronizācijas kļūda: 403 aizliegts</span><span class="sxs-lookup"><span data-stu-id="7f620-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="7f620-124">Sākotnējās sinhronizācijas laikā, iespējams, saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="7f620-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="7f620-125">*(\[Aizliegts\], Attālinātais serveris atgrieza kļūdu: (403) Aizliegts.), AX eksportējot radās kļūda*</span><span class="sxs-lookup"><span data-stu-id="7f620-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="7f620-126">Lai novērstu problēmu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="7f620-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="7f620-127">Piesakieties Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="7f620-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="7f620-128">Lapā **Azure Active Directory programma** izdzēsiet klientu **DtAppID** un pēc tam pievienojiet to vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="7f620-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID klients Azure AD programmu sarakstā](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="7f620-130">Pašatsauces vai cirkulārās atsauces kļūmes sākotnējās sinhronizācijas laikā</span><span class="sxs-lookup"><span data-stu-id="7f620-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="7f620-131">Var tikt parādīts kļūdas ziņojums, ja kādam no kartējumiem ir pašatsauces vai cirkulārās atsauces.</span><span class="sxs-lookup"><span data-stu-id="7f620-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="7f620-132">Kļūdas ietilpst tālāk minētajās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="7f620-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="7f620-133">Kļūdas Kreditori V2-uz-msdyn_vendors elementa kartēšanā</span><span class="sxs-lookup"><span data-stu-id="7f620-133">Errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="7f620-134">Kļūdas Debitori V3-uz-kontiem elementa kartēšanā</span><span class="sxs-lookup"><span data-stu-id="7f620-134">Errors in the Customers V3–to–Accounts entity mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="7f620-135">Atrisināt kļūdas Kreditori V2-uz-msdyn_vendors elementa kartēšanā</span><span class="sxs-lookup"><span data-stu-id="7f620-135">Resolve errors in the Vendors V2–to–msdyn_vendors entity mapping</span></span>

<span data-ttu-id="7f620-136">Jums var rasties sinhronizācijas kļūdas kartēšanā **Kreditori V2** uz **msdyn\_vendors**, ja elementos ir esoši ieraksti ar vērtībām laukos **PrimaryContactPersonId** un **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7f620-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the entities have existing records where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="7f620-137">Šīs kļūdas notiek tādēļ, ka **InvoiceVendorAccountNumber** ir pašatsauces lauks un **PrimaryContactPersonId** ir riņķveida atsauce kreditora kartēšanā.</span><span class="sxs-lookup"><span data-stu-id="7f620-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="7f620-138">Saņemtajiem kļūdu ziņojumiem būs šāda forma.</span><span class="sxs-lookup"><span data-stu-id="7f620-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="7f620-139">*Nevarēja atrisināt lauka GUID: \<field\>. Uzmeklēšana netika atrasta: \<value\>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="7f620-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="7f620-140">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="7f620-140">Here are some examples:</span></span>

- <span data-ttu-id="7f620-141">*Nevarēja atrisināt lauka GUID: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="7f620-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="7f620-142">*Nevarēja atrisināt lauka GUID: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Uzmeklēšana netika atrasta: V24-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="7f620-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="7f620-143">Ja jums ir jebkādi ieraksti kreditoru entītijā ar vērtībām laukos **PrimaryContactPersonId** un **InvoiceVendorAccountNumber**, izpildiet tālāk minētās darbības, lai sekmīgi pabeigtu sākotnējo sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7f620-143">If any records in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="7f620-144">Programmā Finance and Operations izdzēsiet laukus **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** kartējumā un tad saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7f620-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="7f620-145">Duālā ieraksta kartēšanas lapā **Kreditori V2 (msdyn\_vendors)** cilnē **Elementa kartējumi**, kreisajā filtrā atlasiet **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="7f620-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Entity mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="7f620-146">Labajā filtrā atlasiet **Pārdošana. Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="7f620-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="7f620-147">Meklējiet **primarycontactperson**, lai atrastu avota lauku **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="7f620-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="7f620-148">Atlasiet **Darbības** un pēc tam atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7f620-148">Select **Actions**, and then select **Delete**.</span></span>

        ![PrimaryContactPersonId lauka dzēšana](media/vend_selfref3.png)

    4. <span data-ttu-id="7f620-150">Atkārtojiet šos soļus, lai dzēstu lauku **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7f620-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![InvoiceVendorAccountNumber lauka dzēšana](media/vend-selfref4.png)

    5. <span data-ttu-id="7f620-152">Saglabājiet jūsu izmaiņas kartējumā.</span><span class="sxs-lookup"><span data-stu-id="7f620-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="7f620-153">Izslēdziet izmaiņu izsekošanu elementam **Kreditors V2**.</span><span class="sxs-lookup"><span data-stu-id="7f620-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="7f620-154">Darbvietā **Datu pārvaldība** atlasiet elementu **Datu elementi**.</span><span class="sxs-lookup"><span data-stu-id="7f620-154">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="7f620-155">Atlasiet entītiju **Kreditori V2**.</span><span class="sxs-lookup"><span data-stu-id="7f620-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="7f620-156">Darbību rūtī atlasiet **Opcijas** un pēc tam atlasiet **Mainīt izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7f620-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Izmaiņu izsekošanas opcijas atlasīšana](media/selfref_options.png)

    4. <span data-ttu-id="7f620-158">Atlasiet **Atspējot izmaiņu izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7f620-158">Select **Disable Change Tracking**.</span></span>

        ![Atspējot izmaiņu izsekošanu atlasīšana](media/selfref_tracking.png)

3. <span data-ttu-id="7f620-160">Palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="7f620-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="7f620-161">Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.</span><span class="sxs-lookup"><span data-stu-id="7f620-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="7f620-162">Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7f620-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="7f620-163">Jums ir jāsinhronizē šis kartējums, ja vēlaties sinhronizēt primāro kontaktpersonu lauku kreditoru elementā, tāpēc ka sākotnējā sinhronizācija jāveic arī kontaktu ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="7f620-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact records.</span></span>
5. <span data-ttu-id="7f620-164">Pievienojiet **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** laukus atpakaļ kartēšanai **Kreditori V2 (msdyn\_vendors)** un tad saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7f620-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="7f620-165">Vēlreiz palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="7f620-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="7f620-166">Visi ieraksti tiks sinhronizēti, jo izmaiņu izsekošana ir atspējota.</span><span class="sxs-lookup"><span data-stu-id="7f620-166">Because change tracking is turned off, all the records will be synced.</span></span>
7. <span data-ttu-id="7f620-167">Vēlreiz ieslēdziet izmaiņu izsekošanu elementam **Kreditors V2**.</span><span class="sxs-lookup"><span data-stu-id="7f620-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-entity-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="7f620-168">Novērst kļūdas elementa Debitori V3-uz-kontiem kartēšanā</span><span class="sxs-lookup"><span data-stu-id="7f620-168">Resolve errors in the Customers V3–to–Accounts entity mapping</span></span>

<span data-ttu-id="7f620-169">Jums var rasties sinhronizācijas kļūdas kartēšanā **Debitori V3** uz **Konti**, ja elementos ir esoši ieraksti ar vērtībām laukos **ContactPersonID** un **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="7f620-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the entities have existing records where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="7f620-170">Šīs kļūdas notiek tādēļ, ka **InvoiceAccount** ir pašatsauces lauks un **ContactPersonID** ir riņķveida atsauce kreditora kartēšanā.</span><span class="sxs-lookup"><span data-stu-id="7f620-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="7f620-171">Saņemtajiem kļūdu ziņojumiem būs šāda forma.</span><span class="sxs-lookup"><span data-stu-id="7f620-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="7f620-172">*Nevarēja atrisināt lauka GUID: \<field\>. Uzmeklēšana netika atrasta: \<value\>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="7f620-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="7f620-173">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="7f620-173">Here are some examples:</span></span>

- <span data-ttu-id="7f620-174">*Nevarēja atrisināt lauka GUID: primarycontactid.msdyn\_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="7f620-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="7f620-175">*Nevarēja atrisināt lauka GUID: msdyn\_billingaccount.accountnumber. Uzmeklēšana netika atrasta: 1206-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="7f620-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="7f620-176">Ja jums ir jebkādi ieraksti debitoru entītijā ar vērtībām laukos **ContactPersonID** un **InvoiceAccount**, izpildiet tālāk minētās darbības, lai sekmīgi pabeigtu sākotnējo sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7f620-176">If any records in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="7f620-177">Varat izmantot šo pieeju jebkurām iebūvētajām entītijām, piemēram, **Uzņēmumiem** un **Kontaktpersonām**.</span><span class="sxs-lookup"><span data-stu-id="7f620-177">You can use this approach for any out-of-box entities, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="7f620-178">Programmā Finance and Operations izdzēsiet laukus **ContactPersonID** un **InvoiceAccount** no **Debitori V3 (konti)** kartēšanas un tad saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7f620-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="7f620-179">Duālā ieraksta kartēšanas lapā **Debitori V3 (konti)**, cilnē **Elementa kartējumi**, kreisajā filtrā atlasiet **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="7f620-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Entity mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="7f620-180">Labajā filtrā atlasiet **Common Data Service.konts**.</span><span class="sxs-lookup"><span data-stu-id="7f620-180">In the right filter, select **Common Data Service.Account**.</span></span>
    2. <span data-ttu-id="7f620-181">Meklējiet **kontaktpersonu**, lai atrastu avota lauku **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="7f620-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="7f620-182">Atlasiet **Darbības** un pēc tam atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7f620-182">Select **Actions**, and then select **Delete**.</span></span>

        ![ContactPersonID lauka dzēšana](media/cust_selfref3.png)

    4. <span data-ttu-id="7f620-184">Atkārtojiet šos soļus, lai dzēstu lauku **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="7f620-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![InvoiceAccount lauka dzēšana](media/cust_selfref4.png)

    5. <span data-ttu-id="7f620-186">Saglabājiet jūsu izmaiņas kartējumā.</span><span class="sxs-lookup"><span data-stu-id="7f620-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="7f620-187">Izslēdziet izmaiņu izsekošanu elementam **Debitori V3**.</span><span class="sxs-lookup"><span data-stu-id="7f620-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="7f620-188">Darbvietā **Datu pārvaldība** atlasiet elementu **Datu elementi**.</span><span class="sxs-lookup"><span data-stu-id="7f620-188">In the **Data management** workspace, select the **Data entities** tile.</span></span>
    2. <span data-ttu-id="7f620-189">Atlasiet entītiju **Dabitori V3**.</span><span class="sxs-lookup"><span data-stu-id="7f620-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="7f620-190">Darbību rūtī atlasiet **Opcijas** un pēc tam atlasiet **Mainīt izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7f620-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Izmaiņu izsekošanas opcijas atlasīšana](media/selfref_options.png)

    4. <span data-ttu-id="7f620-192">Atlasiet **Atspējot izmaiņu izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7f620-192">Select **Disable Change Tracking**.</span></span>

        ![Atspējot izmaiņu izsekošanu atlasīšana](media/selfref_tracking.png)

3. <span data-ttu-id="7f620-194">Palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7f620-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="7f620-195">Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.</span><span class="sxs-lookup"><span data-stu-id="7f620-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="7f620-196">Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7f620-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7f620-197">Ir divas kartes, kurām ir vienāds nosaukums.</span><span class="sxs-lookup"><span data-stu-id="7f620-197">There are two maps that have the same name.</span></span> <span data-ttu-id="7f620-198">Pārliecinieties, ka izvēlaties karti ar sekojošu aprakstu cilnē **Detaļas**: **Duālā ieraksta veidne sinhronizācijai starp FO.CDS kreditora V2 kontaktpersonām un CDS.Contacts. Nepieciešama jauna pakotne \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="7f620-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="7f620-199">Pievienojiet laukus **InvoiceAccount** un **ContactPersonId** atpakaļ kartējumam **Debitori V3 (konti)** un tad saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7f620-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="7f620-200">Abi lauki **InvoiceAccount** un **ContactPersonId** atkal ir daļa no tiešsaistes sinhronizācijas režīma.</span><span class="sxs-lookup"><span data-stu-id="7f620-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="7f620-201">Nākamajā darbībā veiciet sākotnējo sinhronizāciju šiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="7f620-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="7f620-202">Vēlreiz palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7f620-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="7f620-203">Tā kā izmaiņu izsekošana ir izslēgta, tiks sinhronizēti dati **InvoiceAccount** un **ContactPersonId** no Finance and Operations programmas uz Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="7f620-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Common Data Service.</span></span>
7. <span data-ttu-id="7f620-204">Lai sinhronizētu datus **InvoiceAccount** un **ContactPersonId** no Common Data Service uz Finance and Operations programmu, izmantojiet datu integrācijas projektu.</span><span class="sxs-lookup"><span data-stu-id="7f620-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Common Data Service to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="7f620-205">Sistēmā Power Apps izveidojiet datu integrācijas projektu starp **Pārdošana.Konts** un **Finance and Operations apps.Customers V3** elementiem.</span><span class="sxs-lookup"><span data-stu-id="7f620-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** entities.</span></span> <span data-ttu-id="7f620-206">Datu virzienam jābūt no Common Data Service uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7f620-206">The data direction must be from Common Data Service to the Finance and Operations app.</span></span> <span data-ttu-id="7f620-207">Tā kā **InvoiceAccount** ir jauns atribūts duālajā ierakstā, iespējams, vēlēsities izlaist sākotnējo sinhronizāciju tam.</span><span class="sxs-lookup"><span data-stu-id="7f620-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="7f620-208">Papildinformāciju skatiet [Datu integrēšana pakalpojumā Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="7f620-208">For more information, see [Integrate data into Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="7f620-209">Šajā attēlā ir parādīts projekts, kas atjaunina **CustomerAccount** un **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="7f620-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Datu integrācijas projekts, lai atjauninātu CustomerAccount un ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="7f620-211">Pievienojiet uzņēmuma kritērijus filtram Common Data Service pusē, lai tiktu atjaunināti tikai tie ieraksti, kas atbilst filtra kritērijiem programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7f620-211">Add the company criteria in the filter on the Common Data Service side, so that only records that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="7f620-212">Lai pievienotu filtru, atlasiet filtra pogu.</span><span class="sxs-lookup"><span data-stu-id="7f620-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="7f620-213">Tad dialoglodziņā **Rediģēt vaicājumu** varat pievienot filtra vaicājumu, piemēram, **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="7f620-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="7f620-214">[PIEZĪME] Ja filtra poga nav atrodama, izveidojiet atbalsta biļeti, lai lūgtu datu integrācijas grupai iespējot filtra iespēju jūsu nomniekam.</span><span class="sxs-lookup"><span data-stu-id="7f620-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="7f620-215">Ja neievadāt filtra vaicājumu **\_msdyn\_company\_value**, visi ieraksti tiks sinhronizēti.</span><span class="sxs-lookup"><span data-stu-id="7f620-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the records will be synced.</span></span>

        ![Filtra vaicājuma pievienošana](media/cust_selfref7.png)

    <span data-ttu-id="7f620-217">Ierakstu sākotnējā sinhronizācija tagad ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="7f620-217">The initial synchronization of the records is now completed.</span></span>

8. <span data-ttu-id="7f620-218">Programmā Finance and Operations vēlreiz iespējojiet izmaiņu izsekošanu elementā **Debitori V3**.</span><span class="sxs-lookup"><span data-stu-id="7f620-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
