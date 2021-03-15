---
title: Noņemtie vai novecojuši līdzekļi iepriekšējos laidienos
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir noņemti vai kuri tika plānoti noņemšanai no Dynamics 365 for Finance and Operations un iepriekšējiem šīs preces laidieniem.
author: sericks007
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b862938ec8226cc963fb8c85fcfc2241684eab7
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154389"
---
# <a name="removed-or-deprecated-features-in-previous-releases"></a>Noņemtie vai novecojuši līdzekļi iepriekšējos laidienos

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!IMPORTANT]
> Šī tēma vairs netiek atjaunināta. Lai skatītu pašreizējo to līdzekļu sarakstu, kuri ir noņemti vai novecojuši Finance and Operations programmās, meklējiet saturu **"Noņemti vai novecojuši līdzekļi"** saturu, kas attiecas uz izmantoto programmu.

Šajā tēmā ir aprakstīti līdzekļi, kas ir noņemti vai novecojuši programmā Dynamics 365 for Finance and Operations un iepriekšējos šīs preces laidienos.

- *Noņemts* līdzeklis produktā vairs nav pieejams.
- *Novecojis* līdzeklis netiek aktīvi attīstīts un var tikt noņemts turpmākos atjauninājumos.

Šis saraksts ir izveidots, lai jūs savā plānošanā varētu ņemt vērā, kuri līdzekļi tiek noņemti un kļūst novecojuši. 

Detalizēta informācija par Finance and Operations programmu objektiem ir pieejama tēmā [Tehniskās atsauces pārskati](https://docs.microsoft.com/dynamics/s-e/). Varat salīdzināt dažādās šo pārskatu versijas, lai noskaidrotu, kuri objekti ir mainīti vai noņemti katrā Finance and Operations programmu versijā.

## <a name="finance-1007-with-platform-update-31"></a>Finance 10.0.7 ar 31. platformas atjauninājumu

### <a name="chinese-voucher-types-without-account-groups-selection"></a>Ķīniešu dokumentu veidi bez kontu grupu atlases
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mainīts uz līdzekli ar kontu grupu atlasi. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: līdz 2020. gada 1. decembrim mēs plānojam vairs neatbalstīt ķīniešu dokumentu tipu iestatīšanu bez kontu grupu atlases. Sīkāka informācija par jauna līdzekļa izstrādi pieejama sadaļā Jaunumi 10.0.7 |

## <a name="finance-and-operations-1006-with-platform-update-30"></a>Finance and Operations 10.0.6 ar 30. platformas atjauninājumu


### <a name="dimensionhashgethashstr-_message"></a>DimensionHash.getHash(str _message)

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Operētājsistēmā Windows noveco SHA1 izmantošana, kā dokumentēts sadaļā [SHA1 sertifikātu izpilde Windows](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Pieteikums |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: 2020. gada 1. aprīlī izstrādātājiem ir jāizmanto platformas API, kas atrodams klasē **HasFunction**. |

### <a name="hashcomputesha1hashstring-message"></a>Hash.ComputeSHA1Hash(virknes ziņojums)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Operētājsistēmā Windows noveco SHA1 izmantošana, kā dokumentēts sadaļā [SHA1 sertifikātu izpilde Windows](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Platforma |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: 2020. gada 1. aprīlī izstrādātājiem ir jāizmanto platformas API, kas atrodams klasē **HasFunction**. |


### <a name="formdatetimecontrolsetutcstring"></a>FormDateTimeControl.setUtcString()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mēs noņēmam **setUtcString ()** metodi, jo ir pieejama labāka nomaiņas metode. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Platforma |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: līdz 2020. gada 1. oktobrim mēs plānojam vairs neatbalstīt **setUtcString()** metodi. Tā vietā izstrādātājiem ir jāizmanto metode **setUtcDateTime()**. |

### <a name="blacklist-report-it--feature-reference-it-00001"></a>Melnā saraksta pārskats (IT) — Līdzekļa atsauce IT-00001

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Nav likumīgi nepieciešama. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Itāļu lokalizācija |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: līdz 2020. gada 1. oktobrim mēs plānojam vairs neatbalstīt **Melnā saraksta pārskatu (IT) – Līdzekļa atsauci IT-00001**. |

### <a name="domestic-tax-report--feature-reference-it-00003"></a>Iekšzemes nodokļu pārskats — Līdzekļa atsauce IT-00003

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Nav likumīgi nepieciešama. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē |
| **Ietekmētie produkta apgabali**         | Itāļu lokalizācija |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: līdz 2020. gada 1. oktobrim mēs plānojam vairs neatbalstīt **Iekšzemes nodokļu pārskatu – Līdzekļa atsauci IT-00003**. |


## <a name="finance-and-operations-1005-with-platform-update-29"></a>Finance and Operations 10.0.5 ar 29. platformas atjauninājumu

### <a name="us-payroll-tax-updates"></a>ASV algas nodokļa atjauninājumi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mēs pārtraucam nodokļu atjauninājumus ASV algu funkcionalitātei sakarā ar zemu lietojuma līmeni un uzlabotu funkcionalitāti, kas tagad tiek piedāvāta, izmantojot stratēģiskās integrācijas.  |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Payroll |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: mēs plānojam līdz 2024. gada 31. jūlijam vairs nenodrošināt nodokļu atjauninājumus ASV algas klientiem. Funkcionalitāte paliks precē, bet uzlabojumi vairs neatjauninās šo funkcionalitāti, un visi preces defekti tiks izvērtēti katrā gadījumā atsevišķi. |

>[!NOTE]
> Tas ataino izmaiņas no sākotnējā pārtraukšanas datuma — 2021. gada 1. oktobra. Papildinformāciju skatiet rakstā [Nodokļu atjauninājumu pārtraukšana līdzeklim ASV alga programmā Microsoft Dynamics 365 for Finance and Operations](https://aka.ms/financepayrollfaq).


### <a name="data-management-staging-clean-up"></a>Datu pārvaldības sagatavošanas iztīrīšana
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Neatbilst pamata prasībām, kas nepieciešamas periodiskas tīrīšanas plānošanai. |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, līdzeklis Darba vēstures tīrīšana tiek pievienots, lai izpildītu scenārijus kopumā. |
| **Ietekmētie produkta apgabali**         | Datu pārvaldība |
| **Izvietošanas iespēja**              | Visus  |
| **Statuss**                         | Novecojis: funkcionalitātes noņemšanas mērķa laikposms ir 2020. gada decembris. |

## <a name="finance-and-operations-1004-with-platform-update-28"></a>Finance and Operations 10.0.4 ar 28. platformas atjauninājumu

### <a name="france-fec-accounting-data-export-in-xml"></a>Francija: FEC uzskaites datu eksports XML formātā

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar TXT formātu, **Franču FEC audita fails** ir pieejams, izmantojot ceļu **Virsgrāmata** \> **Periodiskie uzdevumi** \> **Datu eksports**.
| **Vai ir aizstāts ar citu līdzekli?**   | Jā |
| **Ietekmētie produkta apgabali**         | Virsgrāmata |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis. Funkcionalitātes noņemšanas mērķa laikposms ir 2020. gada jūlijs. |


### <a name="legacy-navigation-bar"></a>Mantotā navigācijas josla

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Galvenes līdzinājums ar citiem Dynamics un Office produktiem. Plašāku informāciju skatiet tēmā [Atjauninātā navigācijas josla, kas atrodas atbilstoši Office galvenei](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar).
| **Vai ir aizstāts ar citu līdzekli?**   | Sākot ar atjauninājumu Platform update 24, tika ieviesta pārveidota navigācijas josla ar meklēšanas iespējām. |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: sākot ar 2020. aprīli, mantotā navigācijas josla vairs nebūs pieejama. Līdz tam brīdim klienti var atgriezties pie mantotās navigācijas joslas, izmantojot lapu **Klienta veiktspējas opcijas**. |


## <a name="finance-and-operations-1002-with-platform-update-26"></a>Finance and Operations 10.0.2 ar 26. platformas atjauninājumu


### <a name="legacy-default-action-behavior"></a>Mantotā noklusējuma darbību uzvedība

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Noklusējuma darbību mantotās uzvedības rezultātā tiek izveidota neparedzēta kolonna ar noklusējuma darbības saiti pēc tam, kad tabulas kolonnas ir pārkārtotas, izmantojot personalizēšanu. Jaunais fiksēto noklusējuma darbību līdzeklis to koriģē. Papildinformāciju skatiet tēmā [Fiksētās noklusējuma darbības tabulās](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Vai ir aizstāts ar citu līdzekli?**   | Sākot ar 21. platformas atjauninājumu, tika ieviests “fiksēto noklusējuma darbību” līdzeklis. Šo līdzekli var iespējot lapā **Klienta veiktspējas opcijas**. |
| **Ietekmētie produkta apgabali**         | Tabulas tīmekļa klientā |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: sākot ar 2020. gada aprīli, fiksētās noklusējuma darbības būs noklusējuma uzvedība, un nebūs paredzēts mehānisms, lai atgrieztos pie mantotās uzvedības. |

### <a name="legacy-is-one-of-filtering-experience"></a>Mantotā filtrēšanas darbība "ir viens no"

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Filtrēšanas darbība “ir viens no” tika pārstrādāta 22. platformas atjauninājumā, paredzot, ka nākotnē tā būs vienīgā filtrēšanas darbība “ir viens no”. |
| **Vai ir aizstāts ar citu līdzekli?**   | Sākot ar 22. platformas atjauninājumu, uzlabota filtrēšanas darbība “ir viens no” kļuva pieejama lapā **Klienta veiktspējas opcijas**. Papildinformāciju skatiet sadaļā [Optimizēta filtra “ir viens no” izmantošana](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering). |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: sākot ar 2020. gada aprīli, uzlabotā filtrēšanas darbība “ir viens no” būs noklusējuma darbība, un nebūs paredzēts mehānisms, lai atgrieztos pie mantotās uzvedības. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Parametrs, lai iespējotu pārdošanas pasūtījumus ar vairākiem projekta līguma finansējuma avotiem
Atbalsts no projekta atkarīgu pārdošanas pasūtījumu izveidei, ja projekta līgumam ir vairāki finansējuma avoti, tiek iespējots, izmantojot sadaļas **Projektu pārvaldības parametri** iestatījumu **Atļaut pārdošanas pasūtījumus projektam ar vairākiem finansējuma avotiem**. Pēc noklusējuma šis parametrs nav iespējots. 

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Funkcionalitāte vienmēr būs iespējota pēc parametra noņemšanas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nr.p.k. Funkcionalitāte, kas nodrošina atbalstu no projekta atkarīgiem pārdošanas pasūtījumiem ar vairākiem finansējuma avotiem, vienmēr būs iespējota.   |
| **Ietekmētie produkta apgabali**         |Parametrs **Atļaut pārdošanas pasūtījumus projektiem ar vairākiem finansējuma avotiem** tiks noņemts. Pēc parametra noņemšanas tiks mainītas šādas metodes: **ctrlSalesOrderTable** metode **ProjStatusType** klasē, **validate** metode **ProjId** laukā un **run** metode **SalescreateOrder** formā. Pēc parametra noņemšanas būs novecojušas šādas metodes: **IsSalesOrderAllowedForMultipleFundingSources** metode **ProjTable** tabulas failā, **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled** metode **ProjTable** tabulas failā, **AllowSalesOrdersForMultipleFundingSources** datu lauks **ProjParameters** formā un **ProjParameterEntity** failos, **IsAssociatedToMultipleFundingSourcesContract** privātā metode **ProjTable** tabulas failā. |
| **Izvietošanas iespēja**              | Visus  |
| **Statuss**                         | Atbalsta pārtraukšana ir paredzēta 2020. gada aprīļa laidienu kopumā. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>Mantoti darbplūsmas pārskati izsekošanas un gadījumu statusam

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mantotajiem darbplūsmas ziņojumiem izsekošanas un gadījumu statusam tiek pārtraukts atbalsts, jo uz tiem vairs nav atsauces navigācijā. Pārskatu nosaukumi ir WorkflowWorkflowInstanceByStatusReport un WorkflowWorkflowTrackingReport. |
| **Vai ir aizstāts ar citu līdzekli?**   | Tā vietā var izmantot darbplūsmas vēstures formu. |
| **Ietekmētie produkta apgabali**         | Tīmekļa klients |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: funkcionalitātes noņemšanas mērķa laikposms ir 2020. gada aprīlis. |

## <a name="finance-and-operations-1001-with-platform-update-25"></a>Finance and Operations 10.0.1 ar 25. platformas atjauninājumu

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Novecojušie API un iespējamas traucējumus radošas izmaiņas


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Atvasināšana no iekšējām klasēm ir novecojusi

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Pirms 25. platformas atjauninājuma bija iespējams izveidot klasi vai tabulu, kura atvasināta no iekšējas klases/tabulas, kas ir definēta citā pakotnē/modulī. Šāda kodēšanas prakse nav droša. Sākot ar 25. platformas atjauninājumu, kompilators parādīs brīdinājumu. |
| **Vai ir aizstāts ar citu līdzekli?**   | Kompilatora brīdinājums tiks aizstāts ar kļūdu 26. platformas atjauninājumā. Šī izmaiņa ir atpakaļsaderīga izpildlaikā, tādējādi 25. platformas atjauninājumu vai jaunāku versiju var izvietot jebkurā smilškastes vai ražošanas vidē bez nepieciešamības modificēt pielāgoto kodu. Šīs izmaiņas ietekmē tikai izstrādes un kompilēšanas laiku.|
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: brīdinājums tiks aizstāts ar kompilēšanas kļūdu 26. platformas atjauninājumā. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Iekšējo metožu ignorēšana ir novecojusi

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Pirms 25. platformas atjauninājuma bija iespējams ignorēt iekšēju metodi atvasinātā klasē, kas definēta citā pakotnē/modulī. Šāda kodēšanas prakse nav droša. Sākot ar 25. platformas atjauninājumu, kompilators parādīs brīdinājumu. |
| **Vai ir aizstāts ar citu līdzekli?**   | Šis brīdinājums tiks aizstāts ar kompilācijas kļūdu 26. platformas atjauninājumā. Šī izmaiņa ir atpakaļsaderīga izpildlaikā, tādējādi 25. platformas atjauninājumu vai jaunāku versiju var izvietot jebkurā smilškastes vai ražošanas vidē bez nepieciešamības modificēt pielāgoto kodu. Šīs izmaiņas ietekmē tikai izstrādes un kompilēšanas laiku. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visus |
| **Statuss**                         | Novecojis: brīdinājums tiks aizstāts ar kompilēšanas kļūdu 26. platformas atjauninājumā. |

## <a name="finance-and-operations-1000-with-platform-update-24"></a>Finance and Operations 10.0.0 ar 24. platformas atjauninājumu

### <a name="renaming-released-products"></a>Izlaisto preču pārdēvēšana 
| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Izmantojot funkciju **Pārdēvēt primāro atslēgu**, lai izmainītu izlaistās preces ItemId, tiek atjauninātas tikai tiešās ārējās atslēgas atsauces. Vecais ItemId tiks saglabāts jebkādās citās atsaucēs par izlaisto preci, piemēram, ražošanas pasūtījumos. Rezultātā var rasties neatbilstīgi dati, kas pēc tam bloķē biznesa procesu. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nr.p.k. |
| **Ietekmētie produkta apgabali**         | Preču informācijas pārvaldība |
| **Izvietošanas iespēja**              | Visu  |
| **Statuss**                         | Noņemts, sākot ar Finance and Operations 10.0.0 ar 24. platformas atjauninājumu.|


## <a name="finance-and-operations-813-with-platform-update-23"></a>Finance and Operations 8.1.3 ar 23. platformas atjauninājumu

### <a name="sql-server-reporting-services-reportviewer-control"></a>SQL Server pārskatu izveides pakalpojumu vadīkla ReportViewer
Klienti var izmantot darbību **Eksportēt**, kas paredzēta iegultajā SQL Server pārskatu izveides pakalpojumu (SSRS) vadīklā ReportViewer, lai lejupielādētu dokumentus, kas izveidoti Finance and Operations programmās. Šis pārskata HTML noformējums nodrošina lietotājiem dokumenta priekšskatījumu bez lapdales.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Versija bez lapdales HTML priekšskatījumā **nenodrošina** precīzu atbilstību fiziskajiem dokumentiem, kas galu galā tiek izveidoti programmā Finance and Operations. Pilnībā ieviešot PDF kā standarta formātu biznesa dokumentiem, lietotāji var izmantot modernas skatīšanas iespējas ar uzlabotu veiktspēju, veidojot pieteikumu pārskatus. |
| **Vai ir aizstāts ar citu līdzekli?**   | Turpmāk PDF dokumenti būs noklusējuma formāts pārskatiem, kurus atveido programma Finance and Operations.   |
| **Ietekmētie produkta apgabali**         | Šīs izmaiņas **neietekmē** klientu scenārijus, kuros pārskati tiek izplatīti elektroniski vai nosūtīti tieši uz printeriem.    |
| **Izvietošanas iespēja**              | Visus  |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. 2019. gada maija platformas atjauninājumā ir paredzēta funkcionalitāte, lai automātiski priekšskatītu pieteikumu pārskatus, izmantojot iegulto PDF skatītāju. |

### <a name="client-kpi-controls"></a>Klienta KPI vadīklas
Izstrādātājs var modificēt iegultos galvenos veiktspējas rādītājus (KPI) programmā Visual Studio, un lietotājs var veikt to turpmāku pielāgošanu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Tādu vietējā klienta vadīklu gadījumā, ko izmanto, lai definētu KPI, ir zema klientu aktivitāte un ir nepieciešams izstrādātājs, lai pievienotu izsekojamus rādītājus. |
| **Vai ir aizstāts ar citu līdzekli?**   | PowerBI.com pakalpojums nodrošina pasaules līmeņa rīkus KPI definēšanai un pārvaldībai, balstoties uz datiem no ārējiem avotiem.  Turpmākajos laidienos ir paredzēta iespēja pakalpojumā PowerBI.com viesotus risinājumus iegult programmas darbvietās.   |
| **Ietekmētie produkta apgabali**         | Šis atjauninājums neļaus izstrādātājiem ieviest jaunas KPI vadīklas Visual Studio noformētājā.    |
| **Izvietošanas iespēja**              | Visus  |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Novecojušie API un turpmākas traucējumus radošas izmaiņas

#### <a name="field-groups-containing-invalid-field-references"></a>Lauku grupas, kas ietver nederīgas lauku atsauces

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Tabulu metadatu definīcijās var būt lauku grupas, kas ietver nederīgas lauku atsauces. Izvietošanas gadījumā tas var izraisīt izpildlaika kļūmes modulī Finanšu pārskati un SQL Server pārskatu izveides pakalpojumos (SSRS). Šī problēma pašlaik tiek klasificēta kā *kompilatora brīdinājums*, nevis *kļūda*, līdz ar to izvietojamas pakotnes izveidi un izvietošanu var veikt, nenovēršot problēmu. Lai novērstu šo problēmu:<br><br>1. Noņemiet nederīgo lauka atsauci no tabulas lauku grupas definīcijas.<br><br>2. Pārkompilējiet.<br><br>3. Pārliecinieties, ka ir atrisināti visi brīdinājumi vai kļūdas. |
| **Vai ir aizstāts ar citu līdzekli?**   | Šis brīdinājums tiks aizstāts ar kompilācijas kļūdu turpmākajās versijās. |
| **Ietekmētie produkta apgabali**         | Visual Studio izstrādes rīki |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Novecojis: brīdinājums ir kompilācijas laika kļūda ar platformas atjauninājumiem Finance and Operations programmu 10.0.11 versijā. |

#### <a name="complete-list"></a>Pilnīgs saraksts
Lai piekļūtu pilnīgam tādu API sarakstam, kuriem tiek pārtraukts atbalsts, skatiet tēmu [Atbalsta pārtraukšana metodēm un metadatu elementiem](deprecation-deletion-apis.md).

## <a name="finance-and-operations-81-with-platform-update-20"></a>Finance and Operations 8.1 ar 20. platformas atjauninājumu

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Partijas pārnešanas noteikumi apakšgrāmatas žurnāla kontu ierakstiem
Režīms Sinhronā pārnešana Virsgrāmatas parametros ir novecojis.  Šis režīms ir aizstāts tikai ar opciju Asinhroni un plānoto partiju, kas jau pastāv kā pārnešanas opcijas. Papildinformāciju skatiet emuārā [Virsgrāmatas parametri — partijas pārsūtīšanas kārtulas](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mēs noņēmām sinhrono opciju veiktspējas ietekmes uz sistēmu dēļ. |
| **Vai aizstāts ar citu līdzekli?**   | Opciju Asinhroni un plānoto partiju var izmantot opcijas Sinhroni vietā.   |
| **Ietekmētie produkta apgabali**         | Virsgrāmata, Debitori, Kreditori, Sagāde, Izdevumu    |
| **Izvietošanas iespēja**              | Visus  |
| **Statuss**                         | Novecojis: funkcionalitātes noņemšanas mērķa laikposms ir 10.0 versija.|

### <a name="electronic-reporting-for-russia"></a>Elektroniskā pārskata veidošanas formāts Krievijai
Līdzeklis deklarāciju .txt un .xml failu formātu konfigurēšanai. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Nomainīts ar elektronisku iesniegšanu. |
| **Vai aizstāts ar citu līdzekli?**   | Jā. |
| **Ietekmētie produkta apgabali**         | Virsgrāmata |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Noņemts, sākot ar Finance and Operations 8.1 ar 20. platformas atjauninājumu. |

### <a name="financial-reports-generator-for-russia"></a>Finanšu pārskatu veidotājs Krievijai
Rīks uzskaites un nodokļu pārskatu datu vākšanas iestatīšanai un datu uz XLS un DOC pārskatu veidnēm eksportēšanai. Funkcionālās daļas: datu eksportēšana uz XLS un DOC pārskata veidnēm, vaicājumi, fiksētie rekvizīti ir noņemti. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Noņemtās daļas ir aizstātas ar elektroniskajiem pārskatiem. |
| **Vai aizstāts ar citu līdzekli?**   | Jā. Finanšu pārskatu iestatīšanas lietotāja interfeiss ir jāizmanto, lai iestatītu datu apkopošanas kārtulas pēc Virsgrāmatas kontiem vai nodokļu reģistriem. Datu eksportēšana uz dažādu failu veidiem, fiksēti rekvizīti un vaicājumam līdzīgu datu apkopošanas kārtulas ir jākonfigurē elektronisko pārskatu sadaļā. |
| **Ietekmētie produkta apgabali**         | Virsgrāmata. |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Noņemts, sākot ar Finance and Operations 8.1 ar 20. platformas atjauninājumu. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Integrācija ar ārējiem nodrošinātājiem elektronisko pārskatu sūtīšanai pa sakaru kanāliem Krievijai
Līdzeklis izveidoto deklarācijas elektronisko failu eksportēšanai uz mapi tālākai nosūtīšanai oficiālajiem elektronisko pārskatu nodrošinātajiem, kā arī importēšanai atpakaļ valsts iestādēm.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar konfigurējamu elektronisko ziņojumu līdzekli. |
| **Vai aizstāts ar citu līdzekli?**   | Jā.  |
| **Ietekmētie produkta apgabali**         | Virsgrāmata, nodokļi |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Noņemts, sākot ar Finance and Operations 8.1 ar 20. platformas atjauninājumu. |


### <a name="profit-tax-register-wizard"></a>Peļņas nod. reģ. vednis
Līdzeklis jaunu peļņas nodokļa reģistru veidņu izveidei. Šis līdzeklis rada X++ objektus jauniem reģistriem, kuri pēc tam tiek izveidoti kā veidnes ar pievienotu atbilstošu aprēķina loģiku.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Līdzeklis nav saderīgs ar Finance and Operations paplašināšanas modeli. |
| **Vai aizstāts ar citu līdzekli?**   | Nav |
| **Ietekmētie produkta apgabali**         | Nodoklis |
| **Izvietošanas iespēja**              | Visu |
| **Statuss**                         | Noņemts, sākot ar Finance and Operations 8.1 ar 20. platformas atjauninājumu. |


## <a name="finance-and-operations-80-with-platform-update-15"></a>Finance and Operations 8.0 ar 15. platformas atjauninājumu
Ar šo laidienu nav noņemts vai atzīts par novecojušu neviens līdzeklis. 15. platformas atjauninājums ir kumulatīvs un satur jaunus vai mainītus līdzekļus no 13. platformas atjauninājuma, 14. platformas atjauninājuma un 15. platformas atjauninājuma.

## <a name="finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Finance and Operations Enterprise Edition 7.3 ar 12. platformas atjauninājumu

### <a name="personalized-product-recommendations"></a>Personalizēti preču ieteikumi 
Sākot ar 2018. gada 15. februāri, mazumtirgotāji vairs nevarēs rādīt personalizētus preču ieteikumus pārdošanas punkta (POS) ierīcē. Papildinformāciju skatiet rakstā [Preču ieteikumu pārskats](../../../commerce/product-recommendations.md).  

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mēs noņemam preču ieteikumu pakalpojuma pašreizējo versiju, jo pārveidojam šo līdzekli, pievienojot tam uzlabotu algoritmu un jaunākas uz mazumtirdzniecību orientētas iespējas.  |
| **Vai aizstāts ar citu līdzekli?**   | Nē. Tomēr 2018. gada vasaras sākumā mēs plānojam atjaunot so līdzekli, lai izmantotu jaunu ieteikumu pakalpojumu.   |
| **Ietekmētie produkta apgabali**         | Personalizēti preču ieteikumi pārdošanas punktā.                                                    |
| **Izvietošanas iespēja**              | Visi                                                                                      |
| **Statuss**                         |Noņemts kopš 2018. gada 15. februāra. Tas ietekmē debitorus, kas izmanto programmu Dynamics 365 for Operations 1611 un jaunākas tās versijas.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Elektronisko pārskatu veidošanas (ER) funkciju saraksta paplašinājums
Vairs netiek atbalstīta iespēja ieviest pielāgotas funkcijas, ko izmantot ER izteiksmju veidotājā (papildinformāciju skatiet šeit: [Elektronisko pārskatu veidošanas (ER) funkciju saraksta paplašināšana](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)). Līdz ar ER programmēšanas interfeisa (API) izmaiņu ieviešanu tas API, kurš bija paredzēts iebūvētu funkciju izsaukšanai no ER izteiksmju veidotāja, ir kļuvis iekšējs, un to vairs nevar paplašināt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Koda noslēgšanas iniciatīva  |
| **Vai aizstāts ar citu līdzekli?**   | Nav. Katrreiz, kad ir nepieciešama jauna iebūvēta funkcija, ir nepieciešams adresēt jaunu paplašinājuma pieprasījumu ER struktūras darba grupai.<br><br>Kā pagaidu risinājumu, kamēr ER darba grupa izstrādā pieprasīto funkciju, nepieciešamo loģiku var ieprogrammēt kā pielāgotas programmas klases metodi. Šai metodei ER izteiksmē var piekļūt kā rekvizītam no pievienotā ER datu avota ar tipu **Programma\Klase**, kas attiecas uz šo pielāgoto programmas klasi.  |
| **Ietekmētie produkta apgabali**         | Elektronisko pārskatu veidošanas struktūra                                                      |
| **Izvietošanas iespēja**              | Visus                                                                                      |
| **Statuss**                         | Noņemts, sākot ar Finance and Operations Enterprise Edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Pārskats “Krājumi pēc krājumu grupas” un “Krājumi pēc krājumu dimensijas vecumstruktūras”

Abi šie pārskati vairs netiek atbalstīti programmā Finance and Operations. Lai uzlabotu lietotāju funkcionalitāti, to vietā var izmantot pārskatu **Krājumu vecumstruktūras**.

| &nbsp;  | &nbsp; |
|--------------|-----------------------|
| **Novecošanas pamatojums**       | Funkcionalitātes dublēšanās  |
| **Vai aizstāts ar citu līdzekli?** | Jā. Šie abi pārskati ir aizstāti ar pārskatu **Krājumu vecumstruktūras**.     |
| **Ietekmētie produkta apgabali**       | Krājumu pārvaldība, Izmaksu pārvaldība        |
| **Izvietošanas iespēja**        | Visi|
| **Statuss**                       | Novecojis: izvēlnes elementi šiem abiem pārskatiem ir noņemti versijā 7.3. Taču produktā joprojām atrodas šiem pārskatiem paredzētais kods. Šo kodu ir plānots noņemt turpmākajos laidienos. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Vietnē AppSource pieejamās Power BI satura pakotnes
Pakalpojumā Microsoft Power BI veikto produktu atjauninājumu dēļ satura pakotnes **Izmaksu pārvaldība**, **Finanšu veiktspēja** un **Mazumtirdzniecības kanāla veiktspēja**, kas ir pieejamas vietnē [Microsoft AppSource](https://appsource.microsoft.com), ir novecojušas. Programmā Finance and Operations kļūst novecojušas arī sistēmas administrēšanas veidlapas, kas tika izmantotas šo satura pakotņu izvietošanai vietnē PowerBI.com.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Produktu atjauninājumi pakalpojumā Microsoft Power BI. |
| **Vai aizstāts ar citu līdzekli?**   | Satura pakotnes **Izmaksu pārvaldība**, **Finanšu veiktspēja** un **Mazumtirdzniecības kanāla veiktspēja**, kas pieejamas vietnē [AppSource](https://appsource.microsoft.com), tiek aizstātas ar analītiskām lietojumprogrammām, kuras nodrošina risinājumu integrāciju datu bāzes līmenī. Papildinformāciju par analītiskām programmām skatiet rakstā [Darbvietās iegultais Power BI saturs](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Ietekmētie produkta apgabali**         | Izmaksu pārvaldība, Finanses un Retail                                                                                               |
| **Izvietošanas iespēja**              | Tikai mākonī (Integrācija ar PowerBI.com netiek atbalstīta lokālajos izvietojumos.)                                                                                                            |
| **Statuss**                         | Novecojis: funkcionalitātes noņemšanas mērķa laikposms ir 2018. gada 2. ceturksnis.    |

### <a name="standard-ui-in-data-management-workspace"></a>Standarta UI datu pārvaldības darbvietā

Standarta UI datu pārvaldībā ir pārmantotais UI, un tas ir noklusējuma UI, kurš tiek radīts lietotājiem, kad viņi apmeklē datu pārvaldības darbvietu.

| &nbsp;  | &nbsp; |
|------------------|-------------------------|
| **Novecošanas/noņemšanas pamatojums** | Mēs cenšamies jaunajā UI nodrošināt jaunu lietotāja funkcionalitāti.             |
| **Vai aizstāts ar citu līdzekli?**   | Veco UI nomaina jaunais UI, kura nosaukums ir *Uzlabotie skati*.            |
| **Ietekmētie produkta apgabali**         | Datu pārvaldības darbvieta                                                     |
| **Izvietošanas iespēja**              | Visi                                                                           |
| **Statuss**                         | Novecojis: funkcionalitātes noņemšanas mērķa laikposms ir 2018. gada 2. ceturksnis. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Akcīze, PVN, pakalpojuma nodoklis Indijai

Šie nodokļi ir ietilpināti Indijas GST.

|  &nbsp;                                           |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Noņemšanas vai novecošanas pamatojums**       | Šie nodokļi ir ietilpināti Indijas GST.                          |
| **Vai aizstāts ar citu līdzekli?**            | Indijas GST                                                              |
| **Ietekmētie produkta apgabali**                  | Nodokļi                                                                     |
| **Izvietošanas iespēja**                       | Visi moduļi                                                   |
| **Statuss**                                  | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |    

### <a name="file-validation-utility-fvu-for-india"></a>Failu validēšanas utilīta (FVU) Indijai

|              &nbsp;                               |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Noņemšanas vai novecošanas pamatojums**       | Debitoru lietojuma trūkums                                                  |
| **Vai aizstāts ar citu līdzekli?**            | Nē                                                                      |
| **Ietekmētie produkta apgabali**                  | Indijas ieturētais nodoklis                                                  |
| **Izvietošanas iespēja**                       | Visi moduļi                                                                    |
| **Statuss**                                  | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.   |        

### <a name="tdstcs-certificate-for-india"></a>TDS/TCS sertifikāts Indijai

Lietotāji to var lejupielādēt no valsts portāla.

|             &nbsp;                                |    &nbsp;                                                                     |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Noņemšanas vai novecošanas pamatojums**       | Debitoru lietojuma trūkums                                                  |
| **Vai aizstāts ar citu līdzekli?**            | Nē                                                                      |
| **Ietekmētie produkta apgabali**                  | Indijas ieturētais nodoklis                                                  |
| **Izvietošanas iespēja**                       | Visi moduļi                                                                   |
| **Statuss**                                  | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Eksporta/importa (EXIM) veicināšanas shēma Indijai


|              &nbsp;                               |        &nbsp;                                                                 |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Noņemšanas vai novecošanas pamatojums**       | Debitoru lietojuma trūkums                                                  |
| **Vai aizstāts ar citu līdzekli?**            | Nē                                                                      |
| **Ietekmētie produkta apgabali**                  | Eksportēšana un importēšana                                                       |
| **Izvietošanas iespēja**                       | Visi moduļi                                                                    |
| **Statuss**                                  | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Personalizēti preču ieteikumi 
Sākot ar 2018. gada 15. februāri, mazumtirgotāji vairs nevarēs rādīt personalizētus preču ieteikumus pārdošanas punkta (POS) ierīcē. Papildinformāciju skatiet rakstā [Preču ieteikumu pārskats](../../../commerce/product-recommendations.md).  

|  &nbsp; |  &nbsp;|
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mēs noņemam preču ieteikumu pakalpojuma pašreizējo versiju, jo pārveidojam šo līdzekli, pievienojot tam uzlabotu algoritmu un jaunākas uz mazumtirdzniecību orientētas iespējas.  |
| **Vai aizstāts ar citu līdzekli?**   | Nē. Tomēr 2018. gada vasaras sākumā mēs plānojam atjaunot so līdzekli, lai izmantotu jaunu ieteikumu pakalpojumu.   |
| **Ietekmētie produkta apgabali**         | Personalizēti preču ieteikumi pārdošanas punktā.                                                    |
| **Izvietošanas iespēja**              | Visi                                                                                      |
| **Statuss**                         |Noņemts kopš 2018. gada 15. februāra. Tas ietekmē debitorus, kas izmanto programmu Dynamics 365 for Retail 7.2 un jaunākas tās versijas. |


## <a name="finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Finance and Operations Enterprise Edition 2017. gada jūlija izdevums ar 8. platformas atjauninājumu

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Valūtas konvertēšana uzskaites un pārskata valūtām

Valūtas konvertēšana uzskaites un pārskata valūtām tika ieviesta, kad tika ieviests eiro.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ierobežots lietojums un papildināšana ar juridiskās personas kopēšanas funkcionalitāti kā aizvietojumu.      |
| **Vai aizstāts ar citu līdzekli?**   | Nē, bet tika pievienoti līdzekļi “Kopēt juridisko personu” un “Konfigurācijas”, lai būtu ērtāk pāriet uz uzņēmumu, kam ir mainīgas pamata prasības. |
| **Ietekmētie produkta apgabali**         | Finanšu pārvaldība     |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.   |


### <a name="warehouse-mobile-devices-portal"></a>Noliktavas mobilo ierīču portāls

Noliktavas mobilo ierīču portāls (Warehouse mobile devices portal — WMDP) bija savrupa komponents, kas bija paredzēts lokālai lietotāja veiktai izvietošanai. Šis komponents vairs netiek atbalstīts pakalpojumā Finance and Operations. WMDP funkcionalitāte ir aizstāta ar iekšēju programmu, kas uzlabo lietotāju iespējas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Funkcionalitātes dublēšanās.       |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā. Šis līdzeklis ir aizstāts ar Finance and Operations - Warehousing. Papildinformāciju par iestatīšanu un priekšnoteikumiem skatiet rakstā [Programmas Noliktavas instalēšanas un konfigurēšanas pārskats](../../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Ietekmētie produkta apgabali**         | Noliktavas pārvaldība, Transportēšanas pārvaldība     |
| **Izvietošanas iespēja**              | Noliktavas mobilo ierīču portāls (Warehouse mobile devices portal — WMDP) bija savrupa komponents, kas bija paredzēts lokālai lietotāja veiktai izvietošanai.               |
| **Statuss**                         | Novecojis: funkcionalitātes noņemšanas mērķa laikposms ir 2019. gada 4. ceturksnis.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Detalizētās bankas darbību atbilstības kārtula manuālai atbilstības noteikšanai

Atbilstības kārtula tika izmantota, lai atlasītu un atzīmētu bankas dokumentu, manuāli nosakot dokumentu atbilstību saskaņošanas darblapā.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ierobežots lietojums.                                                                         |
| **Vai aizstāts ar citu līdzekli?**   | Nē. Saskaņojamo dokumentu atrašanai ir jāizmanto kolonnu filtrēšanas iespējas. |
| **Ietekmētie produkta apgabali**         | Kases un bankas vadība                                                               |
| **Izvietošanas iespēja**              | Visus                                                                                    |
| **Statuss**                         | Noņemts kopš 2017. gada jūlija.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 ar 3. platformas atjauninājumu

### <a name="aeb-payment-formats-for-spain"></a>AEB maksājumu formāti Spānijai

Consejo Superior Bancario maksājumu formāti tika izmantoti, lai pārskaitījumu failus nosūtītu uz banku debitoru un kreditoru maksājumiem. Šo formātu saturu noteica Asociación Española de Banca. Tas attiecas uz Cuaderno 19, 32, 58, 34.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šie maksājumu formāti vairs netiek izmantoti.                                  |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 formātiem Kredīta pārskaitījums un Tiešā debeta maksājums Spānijai |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem, Debitoru parādi                                    |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Bankas maksājumu pārskaitījums Lietuvai

Bankas maksājumu pārskaitījumi tika ģenerēti un drukāti, Lietuvai izmantojot eksporta formātu Maksājuma pārsūtījums (LT). Lietuvas tirgus 2005. gadā sāka izmantot LITAS — vienoto elektronisko banku sistēmu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šie maksājumu formāti vairs netiek izmantoti.                        |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Lietuvai     |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem                                               |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Maksājumu formāti BBS Direkte Remittering Norvēģijai

Maksājumu formāti BBS Direkte Remittering ietver debitora maksājuma iekasēšanas eksportēšanu (tiešais debets) un atgrieztā ziņojuma importēšanu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šie maksājumu formāti vairs netiek izmantoti.  |
| **Vai aizstāts ar citu līdzekli?**   | Tiešā debeta ziņojumu ģenerēšanai Norvēģijai var izmantot maksājumu formātu AvtaleGiro debitors. Atgrieztā ziņojuma importēšana tiks ieviesta turpmākajos laidienos. |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem, Debitoru parādi   |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Rīks Kontu plāns Spānijai

Šis rīks tiek lietots, kad kontu plānam Spānijā ir nepieciešamas būtiskas izmaiņas. Lietotāji var importēt jaunu kontu plānu programmas Microsoft Excel vai teksta formātā, kā arī var importēt finanšu pārskatus.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ierobežots lietojums                                                  |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                                             |
| **Ietekmētie produkta apgabali**         | Virsgrāmata                                                 |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="dom80-payment-format-for-belgium"></a>Maksājuma formāts Dom80 Beļģijai

Mantojuma Beļģijas maksājuma formāts maksājumu iekasēšanai (tiešais debets).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis maksājuma formāts vairs netiek izmantots.                          |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO 20022 maksājuma formātu Tiešais debets Beļģijai         |
| **Ietekmētie produkta apgabali**         | Debitoru parādi                                            |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG maksājumu formāti Šveicei

AMNA/EZAG formāti ir integrēti ESR sistēmā, jo tiem var būt atsauces numurs. Tā kā atsauces numurs nav obligāts, šos formātus var izmantot, lai apstrādātu jebkurus kreditoru maksājumus. Šos formātus lieto uzņēmumi, kuru bankas konta atrašanās vieta nav “Postfinance”.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šie maksājumu formāti vairs netiek izmantoti.                        |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Šveicei   |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem                                               |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>Maksājumu formāts EDIFACT-DIRDEB Austrijai

Maksājuma formāts EDIFACT-DIRDEB maksājumu iekasēšanai (tiešais debets).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis maksājuma formāts vairs netiek izmantots.                          |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO 20022 maksājuma formātu Tiešais debets Austrijai         |
| **Ietekmētie produkta apgabali**         | Debitoru parādi                                            |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="edivat-for-belgium"></a>EDIVAT Beļģijai

EDIVAT ir novecojis Beļģijas standarts elektroniskajai deklarēšanai, izmantojot drošu pastu. Programmā Dynamics AX 2012 tiek saglabāts tikai lasīšanas risinājums, lai nodrošinātu piekļuvi vēsturiskajiem datiem.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šī funkcionalitāte vairs netiek izmantota.                           |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                                             |
| **Ietekmētie produkta apgabali**         | Virsgrāmata                                                 |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>Maksājumu importēšanas formāts eGiro EDIFACT CREMUL Norvēģijai

eGiro ir balstīts uz starptautisko standartu UN EDIFACT CREMUL (Daudzkārtēja kredīta izziņas paziņojums), kurš tiek izmantots automātiskai debitoru maksājumu grāmatošanai. Programmā Dynamics AX, eGiro ir ieviests kā klientu maksājumu importēšanas formāts.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis maksājuma formāts vairs netiek izmantots.                                                     |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 Camt.054 paziņojuma importēšanu. |
| **Ietekmētie produkta apgabali**         | Debitoru parādi                                                                       |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.                            |

### <a name="external-inventory-for-poland"></a>Ārējie krājumi Polijai

Pierādījums par precēm, kas no kreditora tiek ņemtas pārdošanai bez pirkšanas. Preces, ar kurām darbības tiek veiktas ārējos krājumos, neietekmē standarta krājumus, un tās var pārdot un pēc tam iegādāties automātiski. Šis process izveido reālu krājumu kustības.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar citu līdzekli                                    |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar pamata funkcionalitāti Ienākošs sūtījums                |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem, Krājumu vadība                         |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Finanšu pārskatu ģenerators Austrumeiropai

Tiek izmantots rīks, lai iestatītu uzskaites un nodokļu pārskatu datu vākšanu un eksportētu datus uz XLS un DOC pārskatu veidnēm.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ierobežots lietojums                                                                            |
| **Vai aizstāts ar citu līdzekli?**   | Nē. Turpmākajos laidienos šis rīks tiks aizstāts ar elektronisko pārskatu veidošanas konfigurācijām. |
| **Ietekmētie produkta apgabali**         | Virsgrāmata                                                                           |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Debitora maksājumu transakciju importēšana Somijai

Varat atlasīt importa formātu Somijas maksājumiem, lai importētu debitoru maksājumu transakcijas no bankas nodrošināta ārēja faila.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis maksājuma formāts vairs netiek izmantots.                                                     |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 Camt.054 paziņojuma importēšanu. |
| **Ietekmētie produkta apgabali**         | Debitoru parādi                                                                       |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Maksājumu transakciju importēšana virsgrāmatas žurnālā Somijai

Formāts, kas ir raksturīgs Somijai, tiek izmantots, lai virsgrāmatā importētu uzskaites transakcijas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis maksājuma formāts vairs netiek izmantots.                                                     |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 Camt.053 bankas izraksta importēšanu, izmantojot Detalizēta bankas darbību saskaņošana. |
| **Ietekmētie produkta apgabali**         | Debitoru parādi                                                                       |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integrācija ar Isabel sinhronizēto (CIS) Beļģijai

Isabel ir elektroniskās banku sistēmas struktūra Eiropā un faktiskais standarts Beļģijā.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Integrēšana ar Isabel klientu ir pārtraukta.   |
| **Vai aizstāts ar citu līdzekli?**   | Nē. Maksājumu formāti, kas vairs netiek izmantoti, tiek aizstādi ar ISO20022 maksājuma formātu Kredīta pārskaitījums Beļģijai. |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem     |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Kontu plāna un uzskaites nosacījumu modifikācijas Spānijai

Šis līdzeklis tiek izmantots kontu plāna un uzskaites nosacījumu izmaiņām Spānijā. Tas kartē kontus, lai veco kontu plānu palīdzētu pārveidot par jaunu kontu plānu, un iepriekšējo finanšu gadu salīdzina ar jauno finanšu gadu, pat ja tie tika grāmatoti dažādos kontu numuros.

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ierobežots lietojums                                                  |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                                             |
| **Ietekmētie produkta apgabali**         | Virsgrāmata                                                 |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Kreditora maksājuma formāts Pagamento Fornittori

Mantots Itālijas maksājuma formāts kredīta pārskaitījumiem.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis maksājuma formāts vairs netiek izmantots.                          |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Itālijai         |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem                                               |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="payment-export-formats-for-estonia"></a>Maksājuma eksportēšanas formāti Igaunijai

Formāti Telehansa un Teleservice tiek izmantoti bankas maksājumu eksportēšanai.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šie maksājumu formāti vairs netiek izmantoti.                        |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Igaunijai       |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem                                               |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="payment-file-archive-for-norway"></a>Maksājumu failu arhīvs Norvēģijai

Kad tiek ģenerēti maksājumu faili, šo failu arhīvs automātiski arhivē visus failus, kas tiek izveidoti — pat failus, kas bija iepriekš rakstīti vai lasīti.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar citu līdzekli                                        |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar arhivētajiem elektronisko pārskatu darbiem                            |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem, Debitoru parādi, Organizācijas administrēšana |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.     |

### <a name="payment-import-formats-for-estonia"></a>Maksājuma importēšanas formāti Igaunijai

Formāti Telehansa un TeleTeenus tiek izmantoti bankas maksājumu importēšanai.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šie maksājumu formāti vairs netiek izmantoti.                                                    |
| **Vai ir aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 Camt.054 bankas paziņojuma importēšanu. |
| **Ietekmētie produkta apgabali**         | Debitoru parādi                                                                        |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.                             |

### <a name="payroll-information-in-human-resources"></a>Algas informācija personāla vadībā

Personāla vadības algas informācija

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šī funkcionalitāte ir aizstāta ar pamata lapām Alga un Personāla vadība.  |
| **Vai aizstāts ar citu līdzekli?**   | Lapas **Atvieglojumi**, **Ienākumi** un citas saistītās lapas, kas iepriekš atradās modulī ASV alga, ir pārkonfigurētas un tagad veido daļu no moduļa Personāla vadība pamata konfigurācijas, lai palīdzētu atbalstīt ārējo algu apstrādi. Šai funkcionalitātei piekļūst, izmantojot konfigurācijas atslēgu **Personāla vadība 1** \> **Alga**. |
| **Ietekmētie produkta apgabali**         | Personāla vadība, Alga   |
| **Statuss**                         | Noņemts, sākot ar Dynamics 365 for Operations versiju 1611.    |

### <a name="performance-management-goal-workflow"></a>Veiktspējas pārvaldības mērķu darbplūsma

Veiktspējas pārvaldība ietver mērķu pārvaldīšanu un integrēšanu ar veiktspējas pārskatiem.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Veiktspējas pārvaldība tika pārveidota, un mērķa lapu skaits tika samazināts, lai vienkāršotu šo procesu.                 |
| **Vai aizstāts ar citu līdzekli?**   | Nē. Mērķi ir redzami vadītājiem, izmantojot portālu Vadītāja pašapkalpošanās, un vadītājs tos var mainīt un apskatīt. |
| **Ietekmētie produkta apgabali**         | Cilvēkkapitāla pārvaldība       |
| **Statuss**                         | Noņemts, sākot ar Dynamics 365 for Operations versiju 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Maksājumu formāti Postgirot un Postgirot Utland Zviedrijai

Maksājumu formāti Postgirot un Postgirot Utland Zviedrijai.

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šie maksājumu formāti vairs netiek izmantoti.                        |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Zviedrijai        |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem                                               |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="radio-frequency-identifier"></a>Radiofrekvences identifikators

Radiofrekvences identifikācija (RFID) ir datu vākšanas tehnoloģija, kas izmanto elektroniskos tagus identifikācijas datu glabāšanai un prasībām atbilstošu lasītāju šo identifikācijas datu uztveršanai.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Zems klientu lietojums un ierobežota līdzekļu kopa.   |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                              |
| **Ietekmētie produkta apgabali**         | Krājumu vadība                            |
| **Statuss**                         | Noņemts, sākot ar Dynamics 365 for Operations 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Pārskats par valsts rēķinu numerāciju Latvijai

Latvijas likumdošana nodrošina īpašus noteikumus par pārdošanas rēķinu numerāciju. Šī funkcionalitāte jums ļauj pārdošanas rēķiniem piešķirt īpašus numurus, pamatojoties uz lietotāju vai lietotāju grupu. Pēc tam varat ģenerēt pārskatu vai XML failu. Varat arī izdrukāt pārskatu par izmantotajiem rēķinu numuriem.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Valsts rēķinu numerācija vairs nav jāuztur. Pārskats par izmantotajiem rēķinu numuriem vairs nav nepieciešams. |
| **Vai aizstāts ar citu līdzekli?**   | Nē       |
| **Ietekmētie produkta apgabali**         | Debitoru parādi    |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Iestatīt uzņēmuma vadītāja un galvenā grāmatveža vārdus Lietuvai

Uzņēmuma vadītāja un galvenā grāmatveža vārdus var norādīta uzņēmuma informācijā un izmantot dažādās vietējo pārskatu izdrukās.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Aizstāts ar citu līdzekli                                     |
| **Vai aizstāts ar citu līdzekli?**   | Jā, šiem pašiem nolūkiem var izmantot amatpersonu iestatīšanu.   |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem, Debitoru parādi, Kases un bankas vadība |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.  |

### <a name="shipping-carrier-interface"></a>Sūtījumu pārvadātāja interfeiss

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Funkcionalitātes dublēšanās   |
| **Vai aizstāts ar citu līdzekli?**   | Daļēji aizstāts ar līdzekli Transportēšanas pārvaldība |
| **Ietekmētie produkta apgabali**         | Pārdošana un mārketings, Krājumu vadība  |
| **Statuss**                         | Noņemts, sākot ar Dynamics 365 for Operations versiju 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>Maksājumu formāti Telepay Norvēģijai

Maksājumu formāti Telepay ietver kreditoru maksājumu eksportēšanu (kredīta pārskaitījums) un debitoru maksājumu iekasēšanu (tiešais debets).

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šie maksājumu formāti vairs netiek izmantoti.                                                        |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 Kredīta pārskaitījuma maksājuma formāts un AvtaleGiro debitora maksājuma formāts Norvēģijai, kā arī pain.002 un camt.054 bankas paziņojuma atgriešanas failu importēšana. |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem, Debitoru parādi                                                          |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Kreditoru maksājumu eksportēšanas formāti Somijai

Divi formāti maksājumu eksportēšanai ir pieejami Somijā. LM02 (FI) tiek izmantots iekšzemes maksājumiem un LUM2 (FI) tiek izmantots ārvalstu maksājumiem.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šie maksājumu formāti vairs netiek izmantoti.                        |
| **Vai aizstāts ar citu līdzekli?**   | Jā, ar ISO20022 maksājuma formātu Kredīta pārskaitījums Somijai       |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem                                               |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="warehouse-management-ii"></a>Noliktavas vadība II

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Risinājumam Noliktavas vadība II (WMS II), kas bija pieejams modulī **Krājumu pārvaldība** , ir tāda pati funkcionalitāte kā modulim **Noliktavas vadība** , kas tika izlaists atjauninājumā Dynamics AX 2012 R3.                                                                         |
| **Vai ir aizstāts ar citu līdzekli?**   | Modulis **Noliktavas vadība** , kas tika izlaists atjauninājumos AX 2012 R3, Dynamics AX 2012 R3 CU8 un Dynamics AX 2012 R3 CU9, aizstāj līdzekļa Noliktavas vadība II līdzekļus. Jaunajam modulim ir uzlabotāki līdzekļi un elastīgāki noliktavas vadības procesi nekā modulim Noliktavas vadība II. |
| **Ietekmētie produkta apgabali**         | Krājumu vadība, Pārdošana un mārketings, Sagāde un avoti   |
| **Statuss**                         | Noņemts, sākot ar Dynamics 365 for Operations versiju 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Darbinieku atgādinājumi personāla vadībā

Personāla vadības algas informācija

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Zems lietojums                                                           |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                                                  |
| **Ietekmētie produkta apgabali**         | Personāla vadība                                                     |
| **Statuss**                         | Noņemts, sākot ar Dynamics 365 for Operations versiju 1611 |

### <a name="workflow-for-creating-goals"></a>Darbplūsma mērķu izveidošanai

Darbplūsma darbinieku mērķu izveidošanas pārvaldībai ir viena no vairākām darbplūsmām, kas bija pieejamas, lai palīdzētu koordinēt veiktspējas pārvaldības procesu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Programmā Finance and Operations ir pilnībā pārveidota veiktspējas pārvaldība.     |
| **Vai aizstāts ar citu līdzekli?**   | Pārveidotais līdzeklis Veiktspējas pārvaldība sniedz lielāku kontroli pār mērķu saturu, mērījumiem, kas tiek izmantoti progresa izsekošanai, un pavaddokumentu piesaistīšanu. Mērķus var glabāt kā veidnes un pēc tam lietot atkārtoti. Šis līdzeklis jums var palīdzēt ātrāk iestatīt papildu mērķus saviem darbiniekiem. |
| **Ietekmētie produkta apgabali**         | Cilvēkkapitāla pārvaldība                 |
| **Statuss**                         | Noņemts, sākot ar Dynamics 365 for Operations versiju 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Spēja atcelt kreditora rēķinā veiktās izmaiņas

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Veiktspējas uzlabojums        |
| **Vai aizstāts ar citu līdzekli?**   | Nē                             |
| **Ietekmētie produkta apgabali**         | Kreditori               |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF, AxD un AxBC integrācijas

Programmu integrācijas struktūrā (Application Integration Framework — AIF) var veikt datu apmaiņu ar ārējām sistēmām, izmantojot biznesa loģiku, kas tiek izmantota kā pakalpojumi. Programmā Dynamics AX ir ietverti pakalpojumi, kuru darbības nodrošināšanai tiek izmantoti dokumenti un .NET Business Connector (AxBC). Dokuments tiek izveidots, izmantojot XML. XML kodā ir ietverta virsraksta informācija, kas tiek pievienota, lai izveidotu *ziņojumu*, kuru var pārsūtīt uz programmu Dynamics AX vai no tās. Dokumentu piemēros ietilpst pārdošanas pasūtījumi un pirkšanas pasūtījumi. Taču gandrīz jebkuru elementu, piemēram, debitoru, var pārstāvēt ar dokumentu. Uz dokumentiem balstītie pakalpojumi lieto **Axd \<Document\>** klases.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | AIF un AxDs arhitektūru nevarēja mērogot uz mākoņa pakalpojumu. Radās veiktspējas problēmas saistībā ar lielapjoma importēšanu.                                        |
| **Vai aizstāts ar citu līdzekli?**   | Šis līdzeklis ir aizstāts ar datu importēšanas/eksportēšanas struktūru, kura atbalsta periodisku lielapjoma importēšanu/eksportēšanu. Strādājot ar AxBC, ieteicams lietot faktiskās tabulas. |
| **Ietekmētie produkta apgabali**         | AxDs, AxBCs un AIF   |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.   |

### <a name="billing-code-rate-scripts"></a>Norēķinu koda likmes skripti

Norēķinu skripti tika izmantoti, lai aprēķinātu norēķinu likmes norēķinu kodiem. Šiem skriptiem bija nepieciešama pielāgota izstrāde programmēšanas valodā C Sharp vai Visual Basic. Pašreizējā Dynamics AX versijā **norēķinu koda likmes skripti** netiek atbalstīti.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Programmā Dynamics AX 7.0 netika pievienots atbalsts pielāgotiem C Sharp vai Visual Basic skriptiem. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē                                                                                      |
| **Ietekmētie produkta apgabali**         | Publiskais sektors, modulis “Debitoru parādi”                                    |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.                                                          |

### <a name="boms-without-bom-versions"></a>MK bez MK versijām

Kad tika atspējota konfigurācijas atslēga **MK versijas**, materiālu komplektu (MK) versijas tika paslēptas visās formās, un starp izlaistajām precēm un MK sistēma lika izmantot attiecību 1:1. Pašreizējā Dynamics AX versijā nevar atspējot konfigurācijas atslēgu **MK versijas**.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Konfigurācijas atslēgas izmantošana, lai kontrolētu MK versijas, netiek mērogota mākoņa vidē. |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                                                                      |
| **Ietekmētie produkta apgabali**         | Preču informācijas pārvaldība, Krājumu vadība                                    |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.                                                          |

### <a name="brazilian-bordero"></a>Brazīlijas Bordero

Īpaša maksāšanas metode Brazīlijas uzņēmumiem

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Brazīlijas lokalizācijā ir pārtraukts atbalsts Brazīlijas maksāšanas metodei Bordero |
| **Vai aizstāts ar citu līdzekli?**   | Nē   |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem   |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="brazilian-sintegra-statement"></a>Brazīlijas izraksts Sintegra

Federālā nodokļa izraksts ICMS nodokļiem

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis izraksts vairs nav lietojams noteiktos Brazīlijas štatos. |
| **Vai aizstāts ar citu līdzekli?**   | Nē. Lietotāji var izmantot vispārīgo elektronisko atskaišu veidošanas rīku, lai konfigurētu šo izrakstu, ja konkrētās situācijās tas ir nepieciešams. |
| **Ietekmētie produkta apgabali**         | Finanšu grāmatas    |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brazīlijas NF-e nejaušību režīms SCAN

(SCAN) nejaušību vide tiek izmantota, lai ģenerētu, eksportētu un importētu Nota Fiscal eletrônica (NF-e) statusu, kad nav pieejama vide Secretaria da Fazenda (SEFAZ).

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šī nejaušību metode vairs nav lietojama visos Brazīlijas štatos |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                                                          |
| **Ietekmētie produkta apgabali**         | Debitoru parādi                                                         |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.              |

### <a name="business-analyzer"></a>Biznesa analizators

Šī mobilā programmas lietotājiem ļauj pārskatīt galvenos biznesa rādītājus.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šī funkcionalitāte ir aizstāta ar citu līdzekli.   |
| **Vai aizstāts ar citu līdzekli?**   | Microsoft Power BI satura pakotnē Finanšu veiktspējas pārraudzība tiks ietverti galvenie finanšu rādītāji, kas iepriekš bija pieejami biznesa analizatorā. |
| **Ietekmētie produkta apgabali**         | Virsgrāmata      |
| **Statuss**                         | Novecojis: biznesa analizatora lietošana ir novecojusi.    |

### <a name="business-statistics"></a>Vadības statistika

Biznesa statistikas uzziņu iestatījums, kas jums var palīdzēt analizēt organizācijas veiktspēju

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Mantojuma pieeja biznesa informācijai (BI), zems klientu lietojums un ierobežota līdzekļu kopa |
| **Vai aizstāts ar citu līdzekli?**   | Jauni BI risinājumi pašreizējai Dynamics AX versijai                                      |
| **Ietekmētie produkta apgabali**         | Sagāde un avoti, Parādi kreditoriem, Pārdošana un mārketings, Debitoru parādi         |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Mainīt dokumenta datuma funkciju rēķinu apstiprināšanas žurnālā

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Zems lietojums                                                               |
| **Vai aizstāts ar citu līdzekli?**   | Jā. Grāmatotajā kreditora transakcijā var mainīt dokumenta datumu. |
| **Ietekmētie produkta apgabali**         | Kreditori                                                        |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03 maksājuma formāts Nīderlandei

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis formāts Nīderlandē vairs nav lietojams, jo tas ir aizstāts ar SEPA funkcionalitāti. |
| **Vai aizstāts ar citu līdzekli?**   | SEPA maksājumu eksportēšana  |
| **Ietekmētie produkta apgabali**         | Visi moduļi     |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.   |

### <a name="compliance-center"></a>Atbilstības centrs

Atbilstības centrs bija uzņēmuma portāla vietne dokumentācijas prasību pārvaldīšanai, lai nodrošinātu atbilstību ar Sarbanes-Oxley likumu saistītajām iniciatīvām.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Debitoru lietojuma trūkums. Microsoft SharePoint nodrošina tādas pašas iespējas, kādas bija pieejamas atbilstības centrā. |
| **Vai aizstāts ar citu līdzekli?**   | Nē   |
| **Ietekmētie produkta apgabali**         | Atbilstība un iekšējā kontrole  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.    |

### <a name="connector-for-microsoft-dynamics"></a>Microsoft Dynamics paredzētā Connector sistēma

Šis rīks tika izmantots programmā Microsoft Dynamics CRM ietverto pamatdatu integrēšanai Dynamics ERP lietojumprogrammās.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šī funkcionalitāte ir aizstāta ar citu līdzekli. |
| **Vai ir aizstāts ar citu līdzekli?**   | Dataverse                                      |
| **Ietekmētie produkta apgabali**         | Dynamics savienotājs                         |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Konteinera vienība un rīcībā esošie vairākdimensiju krājumi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Funkcionalitātes dublēšanās |
| **Vai aizstāts ar citu līdzekli?**   | Jā. Sākot ar versiju AX 2012, šī funkcionalitāte ir aizstāta ar konsolidēto partijas pasūtījumu līdzekļu kopu. Šī līdzekļu kopa ietver konsolidēto rīcībā esošo krājumu skatu. |
| **Ietekmētie produkta apgabali**         | Preču informācijas pārvaldība, Ražošanas kontrole, Krājumu vadība, Pārdošana un mārketings  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0. |

### <a name="cue-group-metadata"></a>Norādījumu grupas metadati

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Norādījumu grupas tika izmantotas, lai papildinformācijas apgabalā parādītu vienu vai vairākus norādījumus. Pastāvēja uzņemšanas ierobežojumi, un bija arī veiktspējas problēmas, jo ieraksta izmaiņas primārajā formā izraisīja vienu vaicājumu katram norādījumu grupas norādījumam. |
| **Vai aizstāts ar citu līdzekli?**   | Nē      |
| **Ietekmētie produkta apgabali**         | Visi moduļi    |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.  |

### <a name="cue-metadata"></a>Norādījuma metadati

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Norādījuma metadati bija ierobežoti ar informāciju par skaitu vai summu.    |
| **Vai aizstāts ar citu līdzekli?**   | Tika ieviesti elementa metadati, lai modelēšanai nodrošinātu lielāku elastību. Piemēram, varat modelēt pašreizējo skaitu, navigāciju un galvenos veiktspējas rādītājus (KPI). Skaita elementa metadati ir tiešs norādījuma metadatu aizstājējs. |
| **Ietekmētie produkta apgabali**         | Visi moduļi           |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Dānijas čeka formāts

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ir pārtraukta atbalsta sniegšana Dānijas čeka formāta izkārtojumam, un šī atskaite ir noņemta no DK lokalizācijas. |
| **Vai aizstāts ar citu līdzekli?**   | Nē    |
| **Ietekmētie produkta apgabali**         | Visi moduļi    |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.  |

### <a name="data-partitions"></a>Datu nodalījumi

Datu nodalījumi nodrošina loģisku datu nošķiršanu Dynamics AX datu bāzē.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Datu nodalījumi tika ieviesti versijā Dynamics AX 2012 R2, lai nodrošinātu datu nošķiršanu. Tipiskā scenārijā uzņēmumam ir filiāles, un datiem no vienas filiāles nevajadzētu būt redzamiem citai filiālei, lai gan abas filiāles pārvalda tā pati IT nodaļa. Taču bija nepieciešami papildu skripti un pārvaldība visā programmā, lai izveidotu jaunus nodalījumus un aizpildītu tos ar datiem, kā arī lai veiktu nodalījuma datu dublējumus. Mākonī, kur var piekļūt platformas pakalpojuma (PaaS) datu bāzu pakalpojumiem (Microsoft Azure SQL datu bāzei), izmantot datu bāzi kā nošķiršanas konteineru ir daudz efektīvāk, nekā veikt nošķiršanu programmā. Neatkarīgi no tā, vai datu nodalījumu izmantošana ir nepieciešama filiālēm, vairākiem nomniekiem vai tikai mērogam, mēs uzskatām, ka ar scenārijiem daudz labāk var strādāt, izmantojot vairākas Finance and Operations instances. |
| **Vai ir aizstāts ar citu līdzekli?**   | Debitoriem, kas izmanto datu nodalījumus, ir jāizmanto vairākas Finance and Operations instances, ja datu bāzes līmeņu atdalīšana ir būtisks jautājums.    |
| **Ietekmētie produkta apgabali**         | Visi moduļi  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Datu bāzes un failu koplietošanas krātuve pielikumiem

Programmā Dynamics AX 2012 varēja glabāt pielikumus datu bāzē un failu koplietojumos. Abas šīs opcijas vairs netiek atbalstītas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Failu koplietošanas krātuve vairs netiek atbalstīta, jo mākoņvides nevar sazināties ar lokālajiem failu koplietojumiem. Datu bāzes krātuve ir novecojusi, un tās vietā tiek izmantota Azure Blob krātuve. Azure Blob krātuve ir līdzvērtīga krātuvei datu bāzē, jo vienīgais veids, kā piekļūt dokumentiem, ir izmantot Finance and Operations klienta formas. Tas nodrošina papildu priekšrocību — šī krātuve neietekmē negatīvi datu bāzes darbību. Blob krātuve ir noklusējuma krātuves mehānisms dokumentu pārvaldībai, un tā darbojas uzreiz. |
| **Vai ir aizstāts ar citu līdzekli?**   | Datu bāzes krātuve ir novecojusi, un tās vietā tiek izmantota Azure Blob krātuve.   |
| **Ietekmētie produkta apgabali**         | Visi moduļi  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.   |

### <a name="delimitation"></a>Norobežošana

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šai funkcionalitātei netika atrasts pielietojums. |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                     |
| **Ietekmētie produkta apgabali**         | Laiks un apmeklētība                    |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.         |

### <a name="desktop-client"></a>Darbvirsmas klients

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ir pārveidotas Dynamics AX klienta lietošanas iespējas, lai uzlabotu lietojamību dažādās platformās un ierīcēs.                      |
| **Vai aizstāts ar citu līdzekli?**   | Jaunais tīmekļa klients ir balstīts uz darbvirsmas formas metadatiem un programmēšanas modeli, kas ir modificēti tā, lai nodrošinātu bagātīgu tīmekļa platformu. |
| **Ietekmētie produkta apgabali**         | Visi moduļi  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.   |

### <a name="direct-database-connection"></a>Tiešs datu bāzes savienojums

Versijā Dynamics AX 2012 R3 programma Retail Modern POS varēja izveidot tiešu savienojumu ar kanāla DB līdzīgi kā programma Enterprise POS. Šī funkcija bija pieejama papildus Retail Modern POS standarta sakaru metodei, izmantojot Retail Server.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Tiešajai datu bāzes savienojamībai bija nepieciešami zemākas drošības protokoli, un tā galvenokārt tika izmantota, lai sasniegtu augstāko veiktspējas līmeni. Programmatūras Finance and Operations veiktspējas un drošības uzlabojumu dēļ šī funkcionalitāte tagad rada vairāk problēmu, nekā tā atrisina. |
| **Vai ir aizstāts ar citu līdzekli?**   | Nē. Tagad tiek atbalstīti tikai standarta Retail Server sakari.  |
| **Ietekmētie produkta apgabali**         | Kanāla DB/Retail Modern POS   |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.  |

### <a name="dutch-swift-mt940"></a>Holandes SWIFT MT940

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Tagad tiek izmantota vispārīgā funkcionalitāte, nevis lokalizētā funkcionalitāte.                    |
| **Vai aizstāts ar citu līdzekli?**   | Jā, šī funkcionalitāte ir aizstāta ar detalizētas bankas darbību saskaņošanas funkcionalitāti. |
| **Ietekmētie produkta apgabali**         | Visi moduļi                                                                              |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL Vācijai)

Šī funkcionalitāte nodrošināja paplašināmās komerciālo atskaišu valodas (eXtensible Business Reporting Language — XBRL) izvades, kas ir paredzēta speciāli Vācijas eBilanz taksonomijai.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Debitoru lietojuma trūkums  |
| **Vai aizstāts ar citu līdzekli?**   | Šis līdzeklis nav aizstāts ar citu līdzekli, bet Vācijas tirgū ir pieejamas vairākas specializētas XBRL pakotnes, kas nodrošina bagātīgu XBRL funkcionalitāti. |
| **Ietekmētie produkta apgabali**         | Management Reporter      |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.  |

### <a name="enterprise-portal-client"></a>Uzņēmuma portāla klients

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Ir nodrošināta viena klienta platforma.  |
| **Vai aizstāts ar citu līdzekli?**   | Jaunais tīmekļa klients ir balstīts uz darbvirsmas formas metadatiem un programmēšanas modeli, kas ir modificēti tā, lai nodrošinātu bagātīgu tīmekļa platformu. |
| **Ietekmētie produkta apgabali**         | Visi moduļi  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.   |

### <a name="environmental-sustainability"></a>Vides ilgtspēja

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Zems klientu lietojums un ierobežota līdzekļu kopa  |
| **Vai aizstāts ar citu līdzekli?**   | Nē              |
| **Ietekmētie produkta apgabali**         | Atbilstības un iekšējās vadīklas, Parādi kreditoriem  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0. |

### <a name="form-activex-and-managed-host-controls"></a>Forma ActiveX un pārvaldītās resursdatora vadīklas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | ActiveX un pārvaldīto resursdatora vadīklu pamatā ir novecojušais darbvirsmas klients. |
| **Vai aizstāts ar citu līdzekli?**   | Paplašināmā kontroles struktūra atbalsta tādu jaunu vadīklu veidošanu, kuras ir balstītas uz valodu HTML, CSS un JavaScript un ir augstākā līmeņa vadīklas Microsoft Visual Studio Tooling vidē. |
| **Ietekmētie produkta apgabali**         | Visi moduļi     |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Ģenerēt pārbaudes, izmantojot paketi

Pārbaudes ģenerēšanu nevar veikt, izmantojot paketi, bet lietotājs to joprojām var izdarīt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Nav formas, ar kuru saglabāt un parādīt iegūto pārbaudes failu, kad tas tiek ģenerēts, izmantojot pakešuzdevumu. |
| **Vai aizstāts ar citu līdzekli?**   | Pārbaudes joprojām var ģenerēt, un lietotājs kontrolē vietu, kur šis fails tiek saglabāts.   |
| **Ietekmētie produkta apgabali**         | Parādi kreditoriem, Debitoru parādi, Kases un bankas vadība  |
| **Statuss**                         | Noņemts, sākot ar AX 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Vācu DTAUS maksājuma eksportēšana un konta izraksta importēšana (kopsummas un transakcijas)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis formāts Vācijā vairs nav lietojams, jo tas ir aizstāts ar vienotās eiro maksājumu zonas (Single Euro Payments Area — SEPA) funkcionalitāti.                    |
| **Vai aizstāts ar citu līdzekli?**   | Jā, šī funkcionalitāte ir aizstāta ar SEPA maksājumu eksportēšanas un detalizētās bankas darbību saskaņošanas funkcionalitāti kontu pārskatu importēšanai. |
| **Ietekmētie produkta apgabali**         | Visi moduļi  |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="german-dtazv-payment-format-in-domestic-currency"></a>Vācijas DTAZV maksājuma formāts vietējā valūtā

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šis formāts Vācijā vairs nav lietojams, jo tas ir aizstāts ar SEPA funkcionalitāti. |
| **Vai ir aizstāts ar citu līdzekli?**   | SEPA maksājumu eksportēšana    |
| **Ietekmētie produkta apgabali**         | Kreditoru parādi   |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.    |

### <a name="german-mt940-import"></a>Vācu MT940 importēšana

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Tagad tiek izmantota vispārīgā funkcionalitāte, nevis lokalizētā funkcionalitāte.                    |
| **Vai aizstāts ar citu līdzekli?**   | Jā, šī funkcionalitāte ir aizstāta ar detalizētas bankas darbību saskaņošanas funkcionalitāti. |
| **Ietekmētie produkta apgabali**         | Visi moduļi                                                                              |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.                           |

### <a name="german-xml-eu-sales-list"></a>Vācijas XML ES pārdošanas saraksts

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Vairs netiek atbalstīts XML formāts Vācijas ES pārdošanas saraksta atskaitēm. Lai ES pārdošanas saraksta atskaites iesniegtu Vācijas nodokļu birojā, var izmantot tikai ELMA5 teksta faila formātu. |
| **Vai aizstāts ar citu līdzekli?**   | Nē         |
| **Ietekmētie produkta apgabali**         | Nodokļi        |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.   |

### <a name="gl-ssrs-reports"></a>GL SSRS atskaites

Ir noņemtas atskaites, kas ietvēra šādus izvēlnes vienumus: **Kopsavilkuma apgrozījuma bilance**, **Detalizēta apgrozījuma bilance**, **Kontu plāns**, **Auditācijas pieraksti**, **Bilances** un **Bilances saraksts**.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Finanšu Microsoft SQL Server Reporting Services (SSRS) pārskati ir aizstāti ar Management Reporter iespējām un noklusējuma pārskatiem. |
| **Vai aizstāts ar citu līdzekli?**   | Management Reporter (pašreizējā Dynamics AXversijā ar apzīmējumu **Finanšu pārskatu veidošana** )    |
| **Ietekmētie produkta apgabali**         | Virsgrāmata   |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart un FormPart metadati

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | InfoPart un FormPart metadati ļāva izveidot papildinformācijas lodziņus diviem dažādiem klientiem. |
| **Vai aizstāts ar citu līdzekli?**   | InfoPart metadati, kas bija vienkāršotā formas definīcija, ar jaunināšanas rīkiem ir pārveidoti par formu. FormPart metadati, kas veidoja atsauci uz formu, ir aizstāti ar tiešāku atsauci, ko veido jaunināšanas rīki. |
| **Ietekmētie produkta apgabali**         | Visi moduļi    |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.        |

### <a name="main-account-list-page"></a>Galvenā konta saraksta lapa

Saraksts ar kontiem juridiskajai personai un saistītā bilances informācija

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Bilances informācija ir pieejama saraksta lapā **Apgrozījuma bilance** pēc konta un dimensijas.  |
| **Vai aizstāts ar citu līdzekli?**   | Sadaļā **Galvenie konti** ir ietverts tāds pats kontu saraksts, kas atrodas saraksta lapā **Galvenais konts**. Režģa skats sadaļā **Galvenie konti** arī rāda vēl mazāku, režģa tipa skatu. |
| **Ietekmētie produkta apgabali**         | Virsgrāmata      |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malaizijas un Singapūras bankas naudas plūsmas atskaite

Šis līdzeklis lietotājam ļauj drukāt naudas plūsmas atskaiti, kurā ir redzamas transakcijas un detalizēta informācija par skaidras naudas ienākošajām un izejošajām plūsmām attiecībā uz noteiktu laika diapazonu atlasītajiem bankas kontiem.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šo pašu informāciju var saņemt pieprasošās bankas transakcijas. |
| **Vai aizstāts ar citu līdzekli?**   | Ar pieprasošās bankas transakciju                                            |
| **Ietekmētie produkta apgabali**         | Kases un bankas vadība                                                |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums.          |

### <a name="mexican-cfd-electronic-invoice"></a>Meksikas CFD elektroniskais rēķins

Šis līdzeklis ļāva ģenerēt Meksikas elektroniskos rēķinus, izmantojot metodi Comprobante Fiscal Digital (CFD), kurā uzņēmums paraksta rēķinu, no valdības pieprasot saistīto autorizāciju. Šis līdzeklis nodrošina arī ikmēneša atskaiti, kas ietver visus šajā periodā izsniegtos elektroniskos rēķinus.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šī metode vairs nav piemērojama. Nodokļu iestādes atzina par novecojušu elektronisko rēķinu ģenerēšanu, izmantojot CFD metodi, un aizstāja ar metodi Comprobante Fiscal Digital a través de Internet (CFDI), kur parakstīšana tiek deleģēta trešās puses nodrošinātājam (PAC). Ikmēneša atskaite ir noņemta, un vaicājuma opcija lietotājam ļauj pieprasīt uzziņas par vēsturiskajām transakcijām. |
| **Vai aizstāts ar citu līdzekli?**   | Nē    |
| **Ietekmētie produkta apgabali**         | Debitori, Projekts   |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="mexico-realized-and-unrealized-vat"></a>Meksikas realizētais un nerealizētais PVN

Programmā Dynamics AX 2012 nerealizētais pievienotās vērtības nodoklis (PVN) tika pārvaldīts, izmantojot Meksikai raksturīgo nerealizētā nodokļa pārvaldības funkcionalitāti.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Funkcionalitātes dublēšanās  |
| **Vai aizstāts ar citu līdzekli?**   | Jā, šī funkcionalitāte ir aizstāta ar standarta nosacījuma pārdošanas nodokļa funkcionalitāti, ko nodrošina pamats. |
| **Ietekmētie produkta apgabali**         | Nodokļi   |
| **Statuss**                         | Novecojis: šim līdzeklim nav noteikts noņemšanas datums. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook integrēšana


| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šī funkcionalitāte ir aizstāta ar Microsoft Exchange Server integrāciju. |
| **Vai aizstāts ar citu līdzekli?**   | Jā                                                                            |
| **Ietekmētie produkta apgabali**         | Pārdošana un mārketings                                                            |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Krājumu un noliktavas vadības žurnālu privāta bloķēšana

Krājumu un noliktavas žurnāli vairs neatbalsta iespēju atzīmēt žurnālu kā privātu atlasītam lietotājam. Tiek atbalstīta tikai žurnālu kā privātu bloķēšana lietotāju grupām un bloķēšanas rediģēšanas laikā.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Šai funkcionalitātei netika atrasts pielietojums. |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                     |
| **Ietekmētie produkta apgabali**         | Krājumu vadība                   |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.         |

### <a name="product-builder"></a>Preču konfigurators

Preču konfigurators tika izmantots, lai dinamiski konfigurētu krājumus no pārdošanas pasūtījuma, pirkšanas pasūtījuma, ražošanas pasūtījuma, pārdošanas piedāvājuma, projektu piedāvājuma vai krājuma vajadzības. Pamatojoties uz preces modeli, kam bija modelēšanas mainīgie, lietotājs varēja atlasīt klienta prasībām atbilstošas vērtības un iegūt unikālu preces variantu, kuram bija MK un maršruts.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Preču konfiguratorā gala lietotājs varēja redzēt X++ kodu, tāpēc tas netiek atbalstīts pašreizējā Dynamics AX versijā. Tas ir noņemts, lai izvairītos no uzturēšanas darbu dublēšanās attiecībā uz ietilpīgām kodu bāzēm, kas pārklājas.  |
| **Vai aizstāts ar citu līdzekli?**   | Jā. Konfigurācija atbilstoši ierobežojumam tika ieviesta versijā Dynamics AX 2012, kad jau bija paziņots par preču konfigurētāja novecošanu nākamajās versijās. Lai nodrošinātu šo konfigurāciju, tehnoloģija konfigurācijai atbilstoši ierobežojumam tiek izvēlēta preču šablonos. Papildinformāciju skatiet šeit: [Preces konfigurēšanas pārskats](../../../supply-chain/pim/build-product-configuration-model.md). |
| **Ietekmētie produkta apgabali**         | Preču informācijas pārvaldība, Pārdošana un mārketings  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.      |

### <a name="production-floor-app"></a>Ražotnes programma
Tā ir progr. planšetdatoriem, kas darb. ar Windows 8.1 RT un Windows 8.1 Pro.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Pārejot uz tīmekļa klientu, var nodrošināt līdzīgu funkcionalitāti, izmantojot vietējo Dynamics AX 7.0 klientu. Darbu kartes ierīce nodrošina ražotnes lietot. interf., kas optimizēts skārienier. un planšetdat. formu faktoriem. |
| **Vai aizstāts ar citu līdzekli?**   | Jā. Darbu kartes ierīce, kas ir iegulta versijā Dynamics AX 7.0.                                                                           |
| **Ietekmētie produkta apgabali**         | Ražošanas kontrole                                                |
| **Statuss**                         | Novecojis: šim līdzeklim vēl nav noteikts noņemšanas datums no Microsoft veikala.                                                |


### <a name="rename-product-dimension"></a>Pārdēvējiet preces dimensiju

Šis līdzeklis jums ļauj nosaukumu vienai no trim standarta preces dimensijām (lielumam, krāsai vai stilam) mainīt pret nosaukumu, kas labāk atbilst jūsu biznesa vajadzībām. Pārdēvēšana iekļāva visas etiķetes, kurās tika izmantots šis preces dimensijas nosaukums.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Pašreizējā Dynamics AX versija neatbalsta etiķešu izmaiņas izpildlaikā. |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                                                            |
| **Ietekmētie produkta apgabali**         | Preču informācijas pārvaldība                                                |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.                                                |

### <a name="retail-server-connectivity-using-http"></a>Retail Server savienojamība, izmantojot HTTP

Versijā Dynamics AX 2012 R3 Retail Server darbības nodrošināšanai varēja izmantot HTTP sakarus (bez aizsardzības). To varēja veikt papildus standarta sakariem, izmantojot HTTPS.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Jauno drošības prasību dēļ tagad tiek atbalstīti tikai droši sakari, izmantojot TLS 1.2 (vai jaunāka versija, ja pieejama). Pašapkalpošanās instalētājs automātiski konfigurēs datoru šādam saziņas veidam. |
| **Vai aizstāts ar citu līdzekli?**   | Nē. Tagad tiek atbalstīti tikai standarta HTTPS sakari. |
| **Ietekmētie produkta apgabali**         | Mazumtirdzniecības serveris  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0. |

### <a name="role-center-pages"></a>Informācijas centru lapas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Informācijas centra lapas bija veidotas, izmantojot novecojušo uzņēmuma portāla platformu, kas pašreizējā Dynamics AX versijā ir aizstāta ar jauno tīmekļa klienta platformu. |
| **Vai aizstāts ar citu līdzekli?**   | Jaunais darbvietas formas modelis lietotājiem sniedz uz procesu centrētu dizainu, kas nodrošina ērtu piekļuvi bieži lietotajiem uzdevumiem šajā procesā.                       |
| **Ietekmētie produkta apgabali**         | Visi moduļi    |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>PVN jurisdikcijas

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Zems klientu lietojums un ierobežota līdzekļu kopa |
| **Vai aizstāts ar citu līdzekli?**   | Nē                                           |
| **Ietekmētie produkta apgabali**         | ASV pārdošanas nodoklis                                 |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.               |

### <a name="sites-services"></a>Site Services

Pakalpojumi Sites Services jums ļauj veidot vietnes, kas jūsu biznesa procesus paplašina uz internetu, neizmantojot IT atbalstu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Programmā Dynamics AX izmantotajai Microsoft Azure infrastruktūrai ir jaunas iespējas, ko var izmantot šī līdzekļa vietā (piemēram, Azure vietnes). |
| **Vai aizstāts ar citu līdzekli?**   | Nē   |
| **Ietekmētie produkta apgabali**         | HR personāla atlase, Pieteikumu pārvaldība, Piedāvājumu pieprasījums, Kreditora reģistrēšana, Sadarbības darbvietas iespējām un kampaņām  |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS pieprasījuma prognozēšanas stratēģija

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Līdzekļa dizainu nevar atbalstīt jaunajā mākoņa arhitektūrā. |
| **Vai aizstāts ar citu līdzekli?**   | Azure algoritmiskās mācīšanās pieprasījuma prognozēšanas stratēģija                           |
| **Ietekmētie produkta apgabali**         | Vispārējā plānošana                                                              |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Kreditora rēķinu kopa bez detalizētās informācijas par grāmatošanu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Zems lietojums. Šī funkcionalitāte ir aizstāta ar rēķinu žurnālu, kuram ir darbplūsmas funkcionalitāte. |
| **Vai aizstāts ar citu līdzekli?**   | Ar rēķinu žurnāla darbplūsmas iespējām.     |
| **Ietekmētie produkta apgabali**         | Kreditori |
| **Statuss**                         | Noņemts, sākot ar Dynamics AX 7.0.    |


### <a name="virtual-company-accounts"></a>Virtuālie datu faili

Programmā Dynamics AX vairs netiek atbalstīts virtuālo datu failu līdzeklis. Virtuālo datu failu līdzeklis lietotājiem ļāva iestatīt tabulas, ko varēja kopīgot ar uzņēmumu kopu. Šī līdzekļa aprakstu varat skatīt šeit: [Datu faili un virtuālie datu faili](https://msdn.microsoft.com/library/aa834382(v=ax.10).aspx). Šis līdzeklis darbojas, grupējot tabulas kolekcijās, kuras tiek piešķirtas virtuāliem datu failiem, kas ir esošo “reālo” uzņēmumu grupas. Vaicājumi tiek veidoti tā, lai visi uzņēmumi virtuālajā datu failā varētu piekļūt saistīto tabulu kolekcijās iekļautajiem datiem.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | - Pirms datu šķirošanas tabulās ir jāiestata virtuālie datu faili. Virtuālo datu failu modernizēšana esošajā implementācijā ir ļoti sarežģīta.<br><br>- Tā kā pašreizējā Dynamics AX versijā ir veikta apjomīga datu normalizācija, ir grūti zināt, ko pievienot tabulu kolekcijām. Piemēram, ir grūti zināt, kuras tabulas kopīgot. Tāpat ir nepieciešams pievienot arī visas tabulas, uz kurām pastāv atsauces no virtuālajā datu failā esošajām tabulām. Tabulu normalizēšanas dēļ pat vienkāršiem pamatdatiem, kas ir izklāti vairākās tabulās, ir jābūt daļai no virtuālā datu faila. Jebkāda šeit pieļauta kļūda izraisīs funkcionālas problēmas.<br><br>- Kad tabula ir daļa no virtuāla datu faila, tā zaudē informāciju par datu izcelsmi, un tiek reģistrēts tikai virtuālais datu fails.   |
| **Vai aizstāts ar citu līdzekli?** | Lai tabulas padarītu pieejamas no visiem uzņēmumiem, var izmantot globālās tabulas. Pašlaik aizstājēja nav. |   
| **Ietekmētie produkta apgabali**       | Visi moduļi |   
| **Statuss**                       | Noņemts, sākot ar Dynamics AX 7.0.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 planšetdatoru programma

Windows 8 planšetdatoru programma nodrošināja izdevumu ievades un apstiprināšanas funkcijas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Finance and Operations ir saderīga ar planšetdatoriem. Planšetdatoru programma vairs nav nepieciešama.    |
| **Vai aizstāts ar citu līdzekli?**   | Nē.          |
| **Ietekmētie produkta apgabali**         | Izmaksu pārvaldība   |
| **Statuss**                         | Noņemts: šī funkcionalitāte ir pieejama tikai versijā Dynamics AX 2012 R3. |

### <a name="workplanner"></a>Darbu plānotājs

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Novecošanas/noņemšanas pamatojums** | Zems lietojums |
| **Vai aizstāts ar citu līdzekli?**   | Nē, bet lapa **Profila saistība**, kura tiek atvērta no lapas **Profilu grupas**, atbalsta tādu pašu biznesa scenāriju kā novecojusī lapa **Darbu plānotājs**. |
| **Ietekmētie produkta apgabali**         | Laiks un apmeklētība     |
| **Statuss**                         | Šis kods nav noņemts. Taču forma JmgWorkPlanner netika migrēta.    |

### <a name="x-financial-statements"></a>X++ finanšu pārskati

| &nbsp;  | &nbsp; |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Novecošanas/noņemšanas pamatojums</strong> |                         Šī funkcionalitāte ir aizstāta ar citu līdzekli.                         |
|  <strong>Vai aizstāts ar citu līdzekli?</strong>  | Management Reporter (pašreizējā Dynamics AXversijā ar apzīmējumu <strong>Finanšu pārskatu veidošana</strong> ) |
|     <strong>Ietekmētie produkta apgabali</strong>     |                                              Virsgrāmata                                              |
|             <strong>Statuss</strong>             |                                      Noņemts, sākot ar Dynamics AX 2012                                      |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]