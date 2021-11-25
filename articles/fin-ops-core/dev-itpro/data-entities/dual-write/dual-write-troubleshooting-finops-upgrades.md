---
title: Problēmu novēršana saistībā ar Finance and Operations programmu jauninājumiem
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar atjauninājumiem Finance and Operations lietojumprogrammās.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: db1602c2edaa2e6b6310cce04639ef7a8e43df15
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782785"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Problēmu novēršana saistībā ar Finance and Operations programmu jauninājumiem

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar atjauninājumiem Finance and Operations lietojumprogrammās.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="database-synchronization-errors"></a>Datu bāzes sinhronizēšanas kļūdas

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Iespējams, mēģinot izmantot **DualWriteProjectConfiguration** tabulu, lai atjauninātu Finance and Operations programmu uz 30. platformas atjauninājumu, saņemat kļūdas ziņojumu, kas līdzīgs šim piemēram.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
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

## <a name="missing-table-columns-issue-on-maps"></a>Kartēs trūkst tabulas kolonnu izejas plūsmas

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Lapā **Duālais ieraksts** var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram:

*Nav avota lauka \<field name\> sistēmā.*

![Trūkstošās avota kolonnas kļūdas ziņojuma piemērs.](media/error_missing_field.png)

Lai atrisinātu problēmu, vispirms veiciet šīs darbības, lai nodrošinātu, ka kolonnas atrodas tabulā.

1. Piesakieties programmas Finance and Operations VM.
2. Dodieties uz **Darbvietas \> Datu pārvaldība**, atlasiet elementu **Struktūras parametri** un pēc tam cilnē **Tabulas iestatījumi** atlasiet **Atsvaidzināt elementu sarakstu**, lai atsvaidzinātu tabulas.
3. Dodieties uz **Darbvietas \> Datu pārvaldība**, atlasiet cilni **Datu tabulas** un pārliecinieties, ka tabula ir uzskaitīta. Ja elements nav uzskaitīts, piesakieties Finance and Operations programmas VM, un pārliecinieties, ka šī tabula ir pieejama.
4. Atveriet lapu **Tabulas kartēšana** no lapas **Duālais ieraksts** Finance and Operations programmā.
5. Atlasiet **Atsvaidzināt elementu sarakstu**, lai automātiski aizpildītu kolonnas tabulas kartējumos.

Ja problēma joprojām nav novērsta, veiciet šādas darbības.

> [!IMPORTANT]
> Izpildot šīs darbības, tabula tiek dzēsta un atkārtoti pievienota. Lai izvairītos no problēmām, noteikti veiciet darbības precīzi.

1. Finance and Operations programmā atveriet **Darbvietas \> Datu pārvaldība** un atlasiet elementu **Datu tabulas**.
2. Atrodiet tabulu, kuraim trūkst atribūts. Rīkjoslā noklikšķiniet uz **Modificēt mērķa kartēšanu**.
3. Rūtī **Kartes iestatīšana mērķim** noklikšķiniet uz **Ģenerēt kartēšanu**.
4. Atveriet lapu **Tabulas kartēšana** no lapas **Duālais ieraksts** Finance and Operations programmā.
5. Ja atribūts kartē netiek automātiski aizpildīts, pievienojiet to manuāli, noklikšķinot uz pogu **Pievienot atribūtu** un pēc tam noklikšķinot uz **Saglabāt**. 
6. Atlasiet karti un noklikšķiniet uz **Palaist**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]