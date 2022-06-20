---
title: Finance and Operations programmu jaunināšanas problēmu novēršana
description: Šajā rakstā ir sniegta traucējummeklēšanas informācija, kas var palīdzēt jums novērst problēmas, kas saistītas ar Finanšu un operāciju programmu jaunināšanu.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 954268b03be2be90f67dc9b7756f33215856864a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882147"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Finance and Operations programmu jaunināšanas problēmu novēršana

[!include [banner](../../includes/banner.md)]





Šajā rakstā ir sniegta traucējummeklēšanas informācija par dubulto rakstīšanas integrāciju starp Finanšu un operāciju programmām un Dataverse. It īpaši tā sniedz informāciju, kas var palīdzēt jums novērst problēmas, kas ir saistītas ar Finanšu un operāciju programmu jaunināšanu.

> [!IMPORTANT]
> Dažas no problēmām, kurām šajā rakstu adresēs var būt nepieciešama sistēmas administratora loma vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="database-synchronization-errors"></a>Datu bāzes sinhronizēšanas kļūdas

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Varat saņemt kļūdas **ziņojumu, kas ir līdzīgs šim piemēram, kad mēģināsit izmantot DualWriteProjectConfiguration** tabulu, lai atjauninātu Finanšu un operāciju programmu uz platformu atjauninājumam 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Lai novērstu problēmu, izpildiet šīs darbības.

1. Piesakieties virtuālajā mašīnā (VM) programmai Finanses un operācijas.
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

1. Piesakieties programmas Finanses un operācijas VM.
2. Dodieties uz **Darbvietas \> Datu pārvaldība**, atlasiet elementu **Struktūras parametri** un pēc tam cilnē **Tabulas iestatījumi** atlasiet **Atsvaidzināt elementu sarakstu**, lai atsvaidzinātu tabulas.
3. Dodieties uz **Darbvietas \> Datu pārvaldība**, atlasiet cilni **Datu tabulas** un pārliecinieties, ka tabula ir uzskaitīta. Ja tabula nav uzskaitīta, piesakieties programmas Finanses un operācijas VM un pārliecinieties, ka tabula ir pieejama.
4. Atveriet lapu **Tabulu kartēšana** no duālās **rakstīšanas** lapas Finanšu un operāciju programmā.
5. Atlasiet **Atsvaidzināt elementu sarakstu**, lai automātiski aizpildītu kolonnas tabulas kartējumos.

Ja problēma joprojām nav novērsta, veiciet šādas darbības.

> [!IMPORTANT]
> Izpildot šīs darbības, tabula tiek dzēsta un atkārtoti pievienota. Lai izvairītos no problēmām, noteikti veiciet darbības precīzi.

1. Finanšu un operāciju programmā dodieties uz sadaļu **Darbalauku \> datu** pārvaldība un atlasiet elementu **Datu tabulas**.
2. Atrodiet tabulu, kuraim trūkst atribūts. Rīkjoslā noklikšķiniet uz **Modificēt mērķa kartēšanu**.
3. Rūtī **Kartes iestatīšana mērķim** noklikšķiniet uz **Ģenerēt kartēšanu**.
4. Atveriet lapu **Tabulu kartēšana** no duālās **rakstīšanas** lapas Finanšu un operāciju programmā.
5. Ja atribūts kartē netiek automātiski aizpildīts, pievienojiet to manuāli, noklikšķinot uz pogu **Pievienot atribūtu** un pēc tam noklikšķinot uz **Saglabāt**. 
6. Atlasiet karti un noklikšķiniet uz **Palaist**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]