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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a7ba4fa4771324b4bcb8464649bd8ce8f32024c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683568"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="7df0c-103">Problēmu novēršana sākotnējās sinhronizēšanas laikā</span><span class="sxs-lookup"><span data-stu-id="7df0c-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7df0c-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7df0c-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="7df0c-105">Konkrēti, tajā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="7df0c-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7df0c-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="7df0c-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="7df0c-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="7df0c-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="7df0c-108">Sākotnējās sinhronizācijas kļūdu pārbaude Finance and Operations programmā</span><span class="sxs-lookup"><span data-stu-id="7df0c-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="7df0c-109">Kad iespējojat kartēšanas veidnes, karšu statusam jābūt **Palaists**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="7df0c-110">Ja statuss ir **Nav palaists**, sākotnējās sinhronizācijas laikā radušās kļūdas.</span><span class="sxs-lookup"><span data-stu-id="7df0c-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="7df0c-111">Lai skatītu kļūdas, lapā **Duālais ieraksts** atlasiet cilni **Sākotnējās sinhronizācijas informācija**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Kļūda cilnē Sākotnējā sinhronizācijas informācija](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="7df0c-113">Sākotnējo sinhronizāciju nevar pabeigt: 400 nederīgs pieprasījums</span><span class="sxs-lookup"><span data-stu-id="7df0c-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="7df0c-114">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="7df0c-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="7df0c-115">Mēģinot palaist kartēšanu un sākotnējo sinhronizēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="7df0c-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="7df0c-116">*(\[Nederīgs pieprasījums\], Attālais serveris atgrieza kļūdu: (400) nederīgs pieprasījums.), AX eksportējot radās kļūda*</span><span class="sxs-lookup"><span data-stu-id="7df0c-116">*(\[Bad Request\], The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="7df0c-117">Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="7df0c-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="7df0c-118">Ja šī kļūda rodas konsekventi un nevar pabeigt sākotnējo sinhronizāciju, veiciet tālāk norādītās darbības, lai novērstu šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="7df0c-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="7df0c-119">Piesakieties programmas Finance and Operations virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="7df0c-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="7df0c-120">Atveriet Microsoft pārvaldības konsoli.</span><span class="sxs-lookup"><span data-stu-id="7df0c-120">Open Microsoft Management Console.</span></span>
3. <span data-ttu-id="7df0c-121">Rūtī **Pakalpojumi** pārbaudiet, vai ir palaists Microsoft Dynamics 365 datu importēšanas eksporta struktūras pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="7df0c-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="7df0c-122">Ja tas ir apturēts, restartējiet to, jo tas tas ir nepieciešams sākotnējai sinhronizēšanai.</span><span class="sxs-lookup"><span data-stu-id="7df0c-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="7df0c-123">Sākotnējās sinhronizācijas kļūda: 403 aizliegts</span><span class="sxs-lookup"><span data-stu-id="7df0c-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="7df0c-124">Sākotnējās sinhronizācijas laikā, iespējams, saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="7df0c-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="7df0c-125">*(\[Aizliegts\], Attālinātais serveris atgrieza kļūdu: (403) Aizliegts.), AX eksportējot radās kļūda*</span><span class="sxs-lookup"><span data-stu-id="7df0c-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="7df0c-126">Lai novērstu problēmu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="7df0c-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="7df0c-127">Piesakieties Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="7df0c-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="7df0c-128">Lapā **Azure Active Directory programma** izdzēsiet klientu **DtAppID** un pēc tam pievienojiet to vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="7df0c-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![DtAppID klients Azure AD programmu sarakstā](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a><span data-ttu-id="7df0c-130">Pašatsauces vai cirkulārās atsauces kļūmes sākotnējās sinhronizācijas laikā</span><span class="sxs-lookup"><span data-stu-id="7df0c-130">Self-reference or circular reference failures during initial synchronization</span></span>

<span data-ttu-id="7df0c-131">Var tikt parādīts kļūdas ziņojums, ja kādam no kartējumiem ir pašatsauces vai cirkulārās atsauces.</span><span class="sxs-lookup"><span data-stu-id="7df0c-131">You might receive an error messages if any of your mappings have self-references or circular references.</span></span> <span data-ttu-id="7df0c-132">Kļūdas ietilpst tālāk minētajās kategorijās.</span><span class="sxs-lookup"><span data-stu-id="7df0c-132">The errors fall into these categories:</span></span>

- [<span data-ttu-id="7df0c-133">Kļūdas Kreditori V2-uz-msdyn_vendors tabulas kartēšanā</span><span class="sxs-lookup"><span data-stu-id="7df0c-133">Errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>](#error-vendor-map)
- [<span data-ttu-id="7df0c-134">Kļūdas Debitori V3-uz-kontiem tabulas kartēšanā</span><span class="sxs-lookup"><span data-stu-id="7df0c-134">Errors in the Customers V3–to–Accounts table mapping</span></span>](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a><span data-ttu-id="7df0c-135">Atrisināt kļūdas Kreditori V2-uz-msdyn_vendors tabulas kartēšanā</span><span class="sxs-lookup"><span data-stu-id="7df0c-135">Resolve errors in the Vendors V2–to–msdyn_vendors table mapping</span></span>

<span data-ttu-id="7df0c-136">Jums var rasties sinhronizācijas kļūdas kartēšanā **Kreditori V2** uz **msdyn\_vendors**, ja tabulās ir esošas rindas ar vērtībām laukos **PrimaryContactPersonId** un **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-136">You might encounter initial synchronization errors for the mapping of **Vendors V2** to **msdyn\_vendors** if the tables have existing rows where there are values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields.</span></span> <span data-ttu-id="7df0c-137">Šīs kļūdas notiek tādēļ, ka **InvoiceVendorAccountNumber** ir pašatsauces lauks un **PrimaryContactPersonId** ir riņķveida atsauce kreditora kartēšanā.</span><span class="sxs-lookup"><span data-stu-id="7df0c-137">These errors occur because **InvoiceVendorAccountNumber** is a self-referencing field, and **PrimaryContactPersonId** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="7df0c-138">Saņemtajiem kļūdu ziņojumiem būs šāda forma.</span><span class="sxs-lookup"><span data-stu-id="7df0c-138">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="7df0c-139">*Nevarēja atrisināt lauka GUID: \<field\>. Uzmeklēšana netika atrasta: \<value\>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="7df0c-139">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="7df0c-140">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="7df0c-140">Here are some examples:</span></span>

- <span data-ttu-id="7df0c-141">*Nevarēja atrisināt lauka GUID: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="7df0c-141">*Couldn't resolve the guid for the field: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="7df0c-142">*Nevarēja atrisināt lauka GUID: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Uzmeklēšana netika atrasta: V24-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span><span class="sxs-lookup"><span data-stu-id="7df0c-142">*Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup was not found: V24-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*</span></span>

<span data-ttu-id="7df0c-143">Ja jebkādām rindām kreditora elementā ir vērtības laukos **PrimaryContactPersonId** un **InvoiceVendorAccountNumber**, izpildiet tālāk minētās darbības, lai sekmīgi pabeigtu sākotnējo sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7df0c-143">If any rows in the vendor entity have values in the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields, follow these steps to complete the initial synchronization.</span></span>

1. <span data-ttu-id="7df0c-144">Programmā Finance and Operations izdzēsiet laukus **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** kartējumā un tad saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7df0c-144">In the Finance and Operations app, delete the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields from the mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="7df0c-145">Duālā ieraksta kartēšanas lapā **Kreditori V2 (msdyn\_vendors)** cilnē **Tabulas kartējumi**, kreisajā filtrā atlasiet **Finance and Operations apps.Vendors V2**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-145">On the dual-write mapping page for **Vendors V2 (msdyn\_vendors)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations apps.Vendors V2**.</span></span> <span data-ttu-id="7df0c-146">Labajā filtrā atlasiet **Pārdošana. Kreditors**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-146">In the right filter, select **Sales.Vendor**.</span></span>
    2. <span data-ttu-id="7df0c-147">Meklējiet **primarycontactperson**, lai atrastu avota lauku **PrimaryContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-147">Search for **primarycontactperson** to find the **PrimaryContactPersonId** source field.</span></span>
    3. <span data-ttu-id="7df0c-148">Atlasiet **Darbības** un pēc tam atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-148">Select **Actions**, and then select **Delete**.</span></span>

        ![PrimaryContactPersonId lauka dzēšana](media/vend_selfref3.png)

    4. <span data-ttu-id="7df0c-150">Atkārtojiet šos soļus, lai dzēstu lauku **InvoiceVendorAccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-150">Repeat these steps to delete the **InvoiceVendorAccountNumber** field.</span></span>

        ![InvoiceVendorAccountNumber lauka dzēšana](media/vend-selfref4.png)

    5. <span data-ttu-id="7df0c-152">Saglabājiet jūsu izmaiņas kartējumā.</span><span class="sxs-lookup"><span data-stu-id="7df0c-152">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="7df0c-153">Izslēdziet izmaiņu izsekošanu elementam **Kreditors V2**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-153">Turn off change tracking for the **Vendors V2** entity.</span></span>

    1. <span data-ttu-id="7df0c-154">Darbvietā **Datu pārvaldība** atlasiet elementu **Datu tabulas**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-154">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="7df0c-155">Atlasiet entītiju **Kreditori V2**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-155">Select the **Vendors V2** entity.</span></span>
    3. <span data-ttu-id="7df0c-156">Darbību rūtī atlasiet **Opcijas** un pēc tam atlasiet **Mainīt izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-156">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Izmaiņu izsekošanas opcijas atlasīšana](media/selfref_options.png)

    4. <span data-ttu-id="7df0c-158">Atlasiet **Atspējot izmaiņu izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-158">Select **Disable Change Tracking**.</span></span>

        ![Atspējot izmaiņu izsekošanu atlasīšana](media/selfref_tracking.png)

3. <span data-ttu-id="7df0c-160">Palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-160">Run initial synchronization for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="7df0c-161">Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.</span><span class="sxs-lookup"><span data-stu-id="7df0c-161">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="7df0c-162">Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7df0c-162">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span> <span data-ttu-id="7df0c-163">Jums ir jāsinhronizē šis kartējums, ja vēlaties sinhronizēt primāro kontaktpersonu lauku kreditoru elementā, tāpēc ka sākotnējā sinhronizācija jāveic arī kontaktu rindām.</span><span class="sxs-lookup"><span data-stu-id="7df0c-163">You must sync this mapping if you want to sync the primary contact field on the vendors entity, because initial synchronization must also be done for the contact rows.</span></span>
5. <span data-ttu-id="7df0c-164">Pievienojiet **PrimaryContactPersonId** un **InvoiceVendorAccountNumber** laukus atpakaļ kartēšanai **Kreditori V2 (msdyn\_vendors)** un tad saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7df0c-164">Add the **PrimaryContactPersonId** and **InvoiceVendorAccountNumber** fields back to the **Vendors V2 (msdyn\_vendors)** mapping, and then save the mapping.</span></span>
6. <span data-ttu-id="7df0c-165">Vēlreiz palaidiet sākotnējo kartēšanas sinhronizāciju attiecībā uz **Kreditori V2 (msdyn\_vendors)**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-165">Run initial synchronization again for the **Vendors V2 (msdyn\_vendors)** mapping.</span></span> <span data-ttu-id="7df0c-166">Visas rindas tiks sinhronizētas, jo izmaiņu izsekošana ir atspējota.</span><span class="sxs-lookup"><span data-stu-id="7df0c-166">Because change tracking is turned off, all the rows will be synced.</span></span>
7. <span data-ttu-id="7df0c-167">Vēlreiz ieslēdziet izmaiņu izsekošanu elementam **Kreditors V2**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-167">Turn change tracking back on for the **Vendors V2** entity.</span></span>

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a><span data-ttu-id="7df0c-168">Novērst kļūdas rindas Debitori V3-uz-kontiem kartēšanā</span><span class="sxs-lookup"><span data-stu-id="7df0c-168">Resolve errors in the Customers V3–to–Accounts table mapping</span></span>

<span data-ttu-id="7df0c-169">Jums var rasties sinhronizācijas kļūdas kartēšanā **Debitori V3** uz **Konti**, ja tabulās ir esošas rindas ar vērtībām laukos **ContactPersonID** un **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-169">You might encounter initial synchronization errors for the mapping of **Customers V3** to **Accounts** if the tables have existing rows where there are values in the **ContactPersonID** and **InvoiceAccount** fields.</span></span> <span data-ttu-id="7df0c-170">Šīs kļūdas notiek tādēļ, ka **InvoiceAccount** ir pašatsauces lauks un **ContactPersonID** ir riņķveida atsauce kreditora kartēšanā.</span><span class="sxs-lookup"><span data-stu-id="7df0c-170">These errors occur because **InvoiceAccount** is a self-referencing field, and **ContactPersonID** is a circular reference in the vendor mapping.</span></span>

<span data-ttu-id="7df0c-171">Saņemtajiem kļūdu ziņojumiem būs šāda forma.</span><span class="sxs-lookup"><span data-stu-id="7df0c-171">The error messages that you receive will have the following form.</span></span>

<span data-ttu-id="7df0c-172">*Nevarēja atrisināt lauka GUID: \<field\>. Uzmeklēšana netika atrasta: \<value\>. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span><span class="sxs-lookup"><span data-stu-id="7df0c-172">*Couldn't resolve the guid for the field: \<field\>. The lookup was not found: \<value\>. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*</span></span>

<span data-ttu-id="7df0c-173">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="7df0c-173">Here are some examples:</span></span>

- <span data-ttu-id="7df0c-174">*Nevarēja atrisināt lauka GUID: primarycontactid.msdyn\_contactpersonid. Uzmeklēšana netika atrasta: 000056. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span><span class="sxs-lookup"><span data-stu-id="7df0c-174">*Couldn't resolve the guid for the field: primarycontactid.msdyn\_contactpersonid. The lookup was not found: 000056. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*</span></span>
- <span data-ttu-id="7df0c-175">*Nevarēja atrisināt lauka GUID: msdyn\_billingaccount.accountnumber. Uzmeklēšana netika atrasta: 1206-1. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai atsauces dati pastāv: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span><span class="sxs-lookup"><span data-stu-id="7df0c-175">*Couldn't resolve the guid for the field: msdyn\_billingaccount.accountnumber. The lookup was not found: 1206-1. Try this URL(s) to check if the reference data exists: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*</span></span>

<span data-ttu-id="7df0c-176">Ja jebkādām rindām debitora elementā ir vērtības laukos **ContactPersonID** un **InvoiceAccount**, izpildiet tālāk minētās darbības, lai sekmīgi pabeigtu sākotnējo sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="7df0c-176">If any rows in the customer entity have values in the **ContactPersonID** and **InvoiceAccount** fields, follow these steps to complete the initial synchronization.</span></span> <span data-ttu-id="7df0c-177">Varat izmantot šo pieeju jebkurām iebūvētajām tabulām, piemēram, **Uzņēmumi** un **Kontaktpersonas**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-177">You can use this approach for any out-of-box tables, such **Accounts** and **Contacts**.</span></span>

1. <span data-ttu-id="7df0c-178">Programmā Finance and Operations izdzēsiet laukus **ContactPersonID** un **InvoiceAccount** no **Debitori V3 (konti)** kartēšanas un tad saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7df0c-178">In the Finance and Operations app, delete the **ContactPersonID** and **InvoiceAccount** fields from the **Customers V3 (accounts)** mapping, and then save the mapping.</span></span>

    1. <span data-ttu-id="7df0c-179">Duālā ieraksta kartēšanas lapā **Debitori V3 (konti)**, cilnē **Tabulas kartējumi**, kreisajā filtrā atlasiet **Finance and Operations app.Customers V3**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-179">On the dual-write mapping page for **Customers V3 (accounts)**, on the **Table mappings** tab, in the left filter, select **Finance and Operations app.Customers V3**.</span></span> <span data-ttu-id="7df0c-180">Labajā filtrā atlasiet **Dataverse.konts**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-180">In the right filter, select **Dataverse.Account**.</span></span>
    2. <span data-ttu-id="7df0c-181">Meklējiet **kontaktpersonu**, lai atrastu avota lauku **ContactPersonID**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-181">Search for **contactperson** to find the **ContactPersonID** source field.</span></span>
    3. <span data-ttu-id="7df0c-182">Atlasiet **Darbības** un pēc tam atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-182">Select **Actions**, and then select **Delete**.</span></span>

        ![ContactPersonID lauka dzēšana](media/cust_selfref3.png)

    4. <span data-ttu-id="7df0c-184">Atkārtojiet šos soļus, lai dzēstu lauku **InvoiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-184">Repeat these steps to delete the **InvoiceAccount** field.</span></span>

        ![InvoiceAccount lauka dzēšana](media/cust_selfref4.png)

    5. <span data-ttu-id="7df0c-186">Saglabājiet jūsu izmaiņas kartējumā.</span><span class="sxs-lookup"><span data-stu-id="7df0c-186">Save your changes to the mapping.</span></span>

2. <span data-ttu-id="7df0c-187">Izslēdziet izmaiņu izsekošanu elementam **Debitori V3**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-187">Turn off change tracking for the **Customers V3** entity.</span></span>

    1. <span data-ttu-id="7df0c-188">Darbvietā **Datu pārvaldība** atlasiet elementu **Datu tabulas**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-188">In the **Data management** workspace, select the **Data tables** tile.</span></span>
    2. <span data-ttu-id="7df0c-189">Atlasiet entītiju **Dabitori V3**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-189">Select the **Customers V3** entity.</span></span>
    3. <span data-ttu-id="7df0c-190">Darbību rūtī atlasiet **Opcijas** un pēc tam atlasiet **Mainīt izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-190">On the Action Pane, select **Options**, and then select **Change tracking**.</span></span>

        ![Izmaiņu izsekošanas opcijas atlasīšana](media/selfref_options.png)

    4. <span data-ttu-id="7df0c-192">Atlasiet **Atspējot izmaiņu izsekošanu**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-192">Select **Disable Change Tracking**.</span></span>

        ![Atspējot izmaiņu izsekošanu atlasīšana](media/selfref_tracking.png)

3. <span data-ttu-id="7df0c-194">Palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7df0c-194">Run initial synchronization for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="7df0c-195">Sākotnējā sinhronizācija ir sekmīgi jāizpilda bez kļūdām.</span><span class="sxs-lookup"><span data-stu-id="7df0c-195">The initial synchronization should run successfully, without any errors.</span></span>
4. <span data-ttu-id="7df0c-196">Palaidiet sākotnējo sinhronizāciju **CDS kontaktpersonas V2 (kontaktpersonas)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7df0c-196">Run initial synchronization for the **CDS Contacts V2 (contacts)** mapping.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7df0c-197">Ir divas kartes, kurām ir vienāds nosaukums.</span><span class="sxs-lookup"><span data-stu-id="7df0c-197">There are two maps that have the same name.</span></span> <span data-ttu-id="7df0c-198">Pārliecinieties, ka izvēlaties karti ar sekojošu aprakstu cilnē **Detaļas**: **Duālā ieraksta veidne sinhronizācijai starp FO.CDS kreditora V2 kontaktpersonām un CDS.Contacts. Nepieciešama jauna pakotne \[Dynamics365SupplyChainExtended\].**</span><span class="sxs-lookup"><span data-stu-id="7df0c-198">Be sure to select the map that has the following description on the **Details** tab: **Dual-write template for sync between FO.CDS Vendor Contacts V2 to CDS.Contacts. Requires new package \[Dynamics365SupplyChainExtended\].**</span></span>

5. <span data-ttu-id="7df0c-199">Pievienojiet laukus **InvoiceAccount** un **ContactPersonId** atpakaļ kartējumam **Debitori V3 (konti)** un tad saglabājiet kartējumu.</span><span class="sxs-lookup"><span data-stu-id="7df0c-199">Add the **InvoiceAccount** and **ContactPersonId** fields back to the **Customers V3 (Accounts)** mapping, and then save the mapping.</span></span> <span data-ttu-id="7df0c-200">Abi lauki **InvoiceAccount** un **ContactPersonId** atkal ir daļa no tiešsaistes sinhronizācijas režīma.</span><span class="sxs-lookup"><span data-stu-id="7df0c-200">Both the **InvoiceAccount** field and the **ContactPersonId** field are now part of live synchronization mode again.</span></span> <span data-ttu-id="7df0c-201">Nākamajā darbībā veiciet sākotnējo sinhronizāciju šiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="7df0c-201">In the next step, you will do the initial synchronization for these fields.</span></span>
6. <span data-ttu-id="7df0c-202">Vēlreiz palaidiet sākotnējo sinhronizāciju **Debitori V3 (konti)** kartēšanai.</span><span class="sxs-lookup"><span data-stu-id="7df0c-202">Run initial synchronization again for the **Customers V3 (Accounts)** mapping.</span></span> <span data-ttu-id="7df0c-203">Tā kā izmaiņu izsekošana ir izslēgta, tiks sinhronizēti dati **InvoiceAccount** un **ContactPersonId** no Finance and Operations programmas uz Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7df0c-203">Because change tracking is turned off, the data for **InvoiceAccount** and **ContactPersonId** will be synced from the Finance and Operations app to Dataverse.</span></span>
7. <span data-ttu-id="7df0c-204">Lai sinhronizētu datus **InvoiceAccount** un **ContactPersonId** no Dataverse uz Finance and Operations programmu, izmantojiet datu integrācijas projektu.</span><span class="sxs-lookup"><span data-stu-id="7df0c-204">To sync the data for **InvoiceAccount** and **ContactPersonId** from Dataverse to the Finance and Operations app, you must use a data integration project.</span></span>

    1. <span data-ttu-id="7df0c-205">Power Apps izveidojiet datu integrācijas projektu starp **Pārdošana.Konts** un **Finance and Operations apps.Customers V3** tabulām.</span><span class="sxs-lookup"><span data-stu-id="7df0c-205">In Power Apps, create a data integration project between the **Sales.Account** and **Finance and Operations apps.Customers V3** tables.</span></span> <span data-ttu-id="7df0c-206">Datu virzienam jābūt no Dataverse uz programmu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7df0c-206">The data direction must be from Dataverse to the Finance and Operations app.</span></span> <span data-ttu-id="7df0c-207">Tā kā **InvoiceAccount** ir jauns atribūts duālajā ierakstā, iespējams, vēlēsities izlaist sākotnējo sinhronizāciju tam.</span><span class="sxs-lookup"><span data-stu-id="7df0c-207">Because **InvoiceAccount** is a new attribute in dual-write, you might want to skip initial synchronization for it.</span></span> <span data-ttu-id="7df0c-208">Papildinformāciju skatiet [Datu integrēšana pakalpojumā Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="7df0c-208">For more information, see [Integrate data into Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).</span></span>

        <span data-ttu-id="7df0c-209">Šajā attēlā ir parādīts projekts, kas atjaunina **CustomerAccount** un **ContactPersonId**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-209">The following illustration shows a project that updates **CustomerAccount** and **ContactPersonId**.</span></span>

        ![Datu integrācijas projekts, lai atjauninātu CustomerAccount un ContactPersonId](media/cust_selfref6.png)

    2. <span data-ttu-id="7df0c-211">Pievienojiet uzņēmuma kritērijus filtram Dataverse pusē, lai tiktu atjauninātas tikai tās rindas, kas atbilst filtra kritērijiem programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7df0c-211">Add the company criteria in the filter on the Dataverse side, so that only rows that match the filter criteria will be updated in the Finance and Operations app.</span></span> <span data-ttu-id="7df0c-212">Lai pievienotu filtru, atlasiet filtra pogu.</span><span class="sxs-lookup"><span data-stu-id="7df0c-212">To add a filter, select the filter button.</span></span> <span data-ttu-id="7df0c-213">Tad dialoglodziņā **Rediģēt vaicājumu** varat pievienot filtra vaicājumu, piemēram, **\_msdyn\_company\_value eq '\<guid\>'**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-213">Then, in the **Edit query** dialog box, you can add a filter query such as **\_msdyn\_company\_value eq '\<guid\>'**.</span></span> 

        > <span data-ttu-id="7df0c-214">[PIEZĪME] Ja filtra poga nav atrodama, izveidojiet atbalsta biļeti, lai lūgtu datu integrācijas grupai iespējot filtra iespēju jūsu nomniekam.</span><span class="sxs-lookup"><span data-stu-id="7df0c-214">[NOTE] If the filter button isn't present, create a support ticket to ask the data integration team to enable the filter capability on your tenant.</span></span>

        <span data-ttu-id="7df0c-215">Ja neievadāt filtra vaicājumu **\_msdyn\_company\_value**, visas rindas tiks sinhronizētas.</span><span class="sxs-lookup"><span data-stu-id="7df0c-215">If you don't enter a filter query for **\_msdyn\_company\_value**, all the rows will be synced.</span></span>

        ![Filtra vaicājuma pievienošana](media/cust_selfref7.png)

    <span data-ttu-id="7df0c-217">Rindu sākotnējā sinhronizācija tagad ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="7df0c-217">The initial synchronization of the rows is now completed.</span></span>

8. <span data-ttu-id="7df0c-218">Programmā Finance and Operations vēlreiz iespējojiet izmaiņu izsekošanu elementā **Debitori V3**.</span><span class="sxs-lookup"><span data-stu-id="7df0c-218">In the Finance and Operations app, turn change tracking back on for the **Customers V3** entity.</span></span>
