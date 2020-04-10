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
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Problēmu novēršana sākotnējās sinhronizēšanas laikā

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service. Konkrēti, tajā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, var rasties sākotnējās sinhronizēšanas laikā. 

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Sākotnējās sinhronizācijas kļūdu pārbaude Finance and Operations programmā

Kad iespējojat kartēšanas veidnes, karšu statusam jābūt **Palaists**. Ja statuss ir **Nav palaists**, sākotnējās sinhronizācijas laikā radušās kļūdas. Lai skatītu kļūdas, lapā **Duālais ieraksts** atlasiet cilni **Sākotnējās sinhronizācijas informācija**.

![Sākotnējās sinhronizācijas detalizētas informācijas cilne](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Sākotnējo sinhronizāciju nevar pabeigt: 400 nederīgs pieprasījums

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Mēģinot palaist kartēšanu un sākotnējo sinhronizēšanu, jūs varētu saņemt šādu kļūdas ziņojumu:

*Attālais serveris atgrieza kļūdu: (400) nederīgs pieprasījums.), AX eksportējot radās kļūda*

Tālāk ir sniegts tabulas pilnā kļūdas ziņojuma piemērs.

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

Ja šī kļūda rodas konsekventi un nevar pabeigt sākotnējo sinhronizāciju, veiciet tālāk norādītās darbības, lai novērstu šo problēmu.

1. Piesakieties programmas Finance and Operations virtuālajā mašīnā (VM).
2. Atveriet Microsoft pārvaldības konsoli. 
3. Rūtī **Pakalpojumi** pārbaudiet, vai ir palaists Microsoft Dynamics 365 datu importēšanas eksporta struktūras pakalpojums. Ja tas ir apturēts, restartējiet to, jo tas tas ir nepieciešams sākotnējai sinhronizēšanai.

## <a name="initial-synchronization-error-403-forbidden"></a>Sākotnējās sinhronizācijas kļūda: 403 aizliegts

Sākotnējās sinhronizācijas laikā, iespējams, saņemsit šādu kļūdas ziņojumu:

*(\[Aizliegts\], Attālinātais serveris atgrieza kļūdu: (403) Aizliegts.), AX eksportējot radās kļūda*

Lai novērstu problēmu, izpildiet šīs darbības.

1. Piesakieties Finance and Operations programmā.
2. Lapā **Azure Active Directory programma** izdzēsiet klientu **DtAppID** un pēc tam pievienojiet to vēlreiz.

![Azure AD pieteikumu saraksts](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a>Pašatsauces kļūmes sākotnējās sinhronizācijas laikā

Var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram, ja kādam no kartējumiem ir pašatsauces:

*Vendors V2 rāda šādu kļūdu: ieraksta Id; jauns ieraksts, ErrorMessage: neizdevās atrisināt GUID laukam: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Netika atrasta uzmeklēšanas vērtība: CN-001. Izmēģiniet šos vietrāžus URL, lai pārbaudītu, vai pastāv atsauces dati: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

Šāda veida kļūda rodas, veicot sākotnējo sinhronizāciju kartējumiem ar pašatsaucēm. Iepriekšējā piemērā lauka rēķina konta lauks atsaucas uz kreditora elementu.

Lai novērstu šo problēmu, iespējams, būs jāpalaiž kartēšana divas reizes pirms sākotnējās sinhronizācija ir veiksmīga.

