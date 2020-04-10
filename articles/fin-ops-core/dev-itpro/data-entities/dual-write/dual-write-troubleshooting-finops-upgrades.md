---
title: Ar Finance and Operations programmu jaunināšanu saistītu problēmu novēršana
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar atjauninājumiem Finance and Operations lietojumprogrammās.
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
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172881"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Ar Finance and Operations programmu jaunināšanu saistītu problēmu novēršana

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar atjauninājumiem Finance and Operations lietojumprogrammās.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="database-synchronization-errors"></a>Datu bāzes sinhronizēšanas kļūdas

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Iespējams, mēģinot izmantot **DualWriteProjectConfiguration** elementu, lai atjauninātu Finance and Operations programmu uz 30. platformas atjauninājumu, saņemat kļūdas ziņojumu, kas līdzīgs šim piemēram.

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Lai novērstu problēmu, izpildiet šīs darbības.

1. Piesakieties programmas Finance and Operations virtuālajā mašīnā (VM).
2. Atveriet Visual Studio kā administrators un atveriet lietojumprogrammas objektu koku (AOT).
3. Meklēt **DualWriteProjectConfiguration**.
4. Lietojumprogrammas objektu kokā ar peles labo pogu noklikšķiniet uz **DualWriteProjectConfiguration** un atlasiet **Pievienot jaunajam projektam**. Atlasiet **Labi**, lai izveidotu jaunu projektu, kas izmanto noklusējuma opcijas.
5. Risinājumu pārlūkā ar peles labo pogu noklikšķiniet uz **Projekta rekvizīti** un iestatiet opciju **Sinhronizēt datu bāzi būvējumā** uz **Patiess**.
6. Izveidojiet projektu un apstipriniet, ka būvējums ir veiksmīgs.
7. Izvēlnē **Dynamics 365** atlasiet **Sinhronizēt datu bāzi.**
8. Atlasiet **Sinhronizēt**, lai veiktu pilnīgu datu bāzes sinhronizāciju.
9. Kad pilnīga datu bāzes sinhronizācija ir veiksmīgi pabeigta, atkārtoti palaidiet datu bāzes sinhronizācijas darbību pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) un pēc nepieciešamības izmantojiet manuālos jaunināšanas skriptus, lai varētu turpināt atjaunināšanu.

## <a name="missing-entity-fields-issue-on-maps"></a>Trūkstošu elementu lauku problēma kartēs

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Lapā **Duālais ieraksts** var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram:

*Nav avota lauka \<lauka nosaukums\> sistēmā.*

![Trūkstošā avota lauka kļūdas ziņojuma piemērs](media/error_missing_field.png)

Lai atrisinātu problēmu, vispirms veiciet šīs darbības, lai nodrošinātu, ka lauki atrodas entītijā.

1. Piesakieties programmas Finance and Operations VM.
2. Dodieties uz **Darbvietas \>Datu pārvaldība**, atlasiet elementu **Struktūras parametri** un pēc tam cilnē **Elementa iestatījumi** atlasiet **Atsvaidzināt elementu sarakstu**, lai atsvaidzinātu elementus.
3. Dodieties uz **Darbvietas \>Datu pārvaldība**, atlasiet cilni **Datu elementi** un pārliecinieties, ka elements ir uzskaitīts. Ja elements nav uzskaitīts, piesakieties Finance and Operations programmas VM, un pārliecinieties, ka šis elements ir pieejams.
4. Atveriet lapu **Elementa kartēšana** no lapas **Duālais ieraksts** Finance and Operations lietojumprogrammā.
5. Atlasiet **Atsvaidzināt elementu sarakstu**, lai automātiski aizpildītu laukus elementu kartējumos.

Ja problēma joprojām nav novērsta, veiciet šādas darbības.

> [!IMPORTANT]
> Izpildot šīs darbības, elements tiek dzēsts un atkārtoti pievienots. Lai izvairītos no problēmām, noteikti veiciet darbības precīzi.

1. Finance and Operations programmā atveriet **Darbvietas \>Datu pārvaldība**un atlasiet elementu **Datu elementi**.
2. Atrodiet elementu, kuram trūkst lauka. Atzīmējiet mērķa elementa, sagatavošanas tabulas, elementa nosaukuma un citu kolonnu vērtības.
3. Ja kāda no jūsu apstrādes grupām ir atkarīga no šī elementa, pirms elementa dzēšanas atbilstoši apstrādājiet grupas.
4. Dzēsiet elementu, kuram trūkst lauka.
5. Atlasiet **Jauns** un pievienojiet elementu atpakaļ. Norādiet vērtības, kuras atzīmējāt 2. darbības laikā.
6. Atveriet lapu **Elementa kartēšana** no lapas **Duālais ieraksts** Finance and Operations lietojumprogrammā.
7. Atlasiet **Atsvaidzināt elementu sarakstu**, lai automātiski aizpildītu laukus elementu kartējumos.
