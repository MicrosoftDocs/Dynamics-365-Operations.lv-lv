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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172718"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="eb928-103">Problēmu novēršana sākotnējās sinhronizēšanas laikā</span><span class="sxs-lookup"><span data-stu-id="eb928-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="eb928-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eb928-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="eb928-105">Konkrēti, tajā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="eb928-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="eb928-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="eb928-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="eb928-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="eb928-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="eb928-108">Sākotnējās sinhronizācijas kļūdu pārbaude Finance and Operations programmā</span><span class="sxs-lookup"><span data-stu-id="eb928-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="eb928-109">Kad iespējojat kartēšanas veidnes, karšu statusam jābūt **Palaists**.</span><span class="sxs-lookup"><span data-stu-id="eb928-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="eb928-110">Ja statuss ir **Nav palaists**, sākotnējās sinhronizācijas laikā radušās kļūdas.</span><span class="sxs-lookup"><span data-stu-id="eb928-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="eb928-111">Lai skatītu kļūdas, lapā **Duālais ieraksts** atlasiet cilni **Sākotnējās sinhronizācijas informācija**.</span><span class="sxs-lookup"><span data-stu-id="eb928-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Sākotnējās sinhronizācijas detalizētas informācijas cilne](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="eb928-113">Sākotnējo sinhronizāciju nevar pabeigt: 400 nederīgs pieprasījums</span><span class="sxs-lookup"><span data-stu-id="eb928-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="eb928-114">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="eb928-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="eb928-115">Mēģinot palaist kartēšanu un sākotnējo sinhronizēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="eb928-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="eb928-116">*Attālais serveris atgrieza kļūdu: (400) nederīgs pieprasījums.), AX eksportējot radās kļūda*</span><span class="sxs-lookup"><span data-stu-id="eb928-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="eb928-117">Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma piemērs.</span><span class="sxs-lookup"><span data-stu-id="eb928-117">Here is an example of the full error message.</span></span>

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

<span data-ttu-id="eb928-118">Ja šī kļūda rodas konsekventi un nevar pabeigt sākotnējo sinhronizāciju, veiciet tālāk norādītās darbības, lai novērstu šo problēmu.</span><span class="sxs-lookup"><span data-stu-id="eb928-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="eb928-119">Piesakieties programmas Finance and Operations virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="eb928-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="eb928-120">Atveriet Microsoft pārvaldības konsoli.</span><span class="sxs-lookup"><span data-stu-id="eb928-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="eb928-121">Rūtī **Pakalpojumi** pārbaudiet, vai ir palaists Microsoft Dynamics 365 datu importēšanas eksporta struktūras pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="eb928-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="eb928-122">Ja tas ir apturēts, restartējiet to, jo tas tas ir nepieciešams sākotnējai sinhronizēšanai.</span><span class="sxs-lookup"><span data-stu-id="eb928-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="eb928-123">Sākotnējās sinhronizācijas kļūda: 403 aizliegts</span><span class="sxs-lookup"><span data-stu-id="eb928-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="eb928-124">Sākotnējās sinhronizācijas laikā, iespējams, saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="eb928-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="eb928-125">*(\[Aizliegts\], Attālinātais serveris atgrieza kļūdu: (403) Aizliegts.), AX eksportējot radās kļūda*</span><span class="sxs-lookup"><span data-stu-id="eb928-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="eb928-126">Lai novērstu problēmu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="eb928-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="eb928-127">Piesakieties Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="eb928-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="eb928-128">Lapā **Azure Active Directory programma** izdzēsiet klientu **DtAppID** un pēc tam pievienojiet to vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="eb928-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD pieteikumu saraksts](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="eb928-130">Pašatsauces kļūmes sākotnējās sinhronizācijas laikā</span><span class="sxs-lookup"><span data-stu-id="eb928-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="eb928-131">Var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram, ja kādam no kartējumiem ir pašatsauces:</span><span class="sxs-lookup"><span data-stu-id="eb928-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="eb928-132">*Vendors V2 rāda šādu kļūdu: ieraksta Id; jauns ieraksts, ErrorMessage: neizdevās atrisināt GUID laukam: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Netika atrasta uzmeklēšanas vērtība: CN-001. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="eb928-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="eb928-133">Šāda veida kļūda rodas, veicot sākotnējo sinhronizāciju kartējumiem ar pašatsaucēm.</span><span class="sxs-lookup"><span data-stu-id="eb928-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="eb928-134">Iepriekšējā piemērā lauka rēķina konta lauks atsaucas uz kreditora elementu.</span><span class="sxs-lookup"><span data-stu-id="eb928-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="eb928-135">Lai novērstu šo problēmu, iespējams, būs jāpalaiž kartēšana divas reizes pirms sākotnējās sinhronizācija ir veiksmīga.</span><span class="sxs-lookup"><span data-stu-id="eb928-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

