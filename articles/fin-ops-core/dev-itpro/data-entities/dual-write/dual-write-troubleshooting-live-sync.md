---
title: Tiešsaistes sinhronizācijas problēmu novēršana
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar tiešsaistes sinhronizāciju.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1c0dfebb3ef442f67d8489d7aed00305c02cf410
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748901"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Tiešsaistes sinhronizācijas problēmu novēršana

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar tiešsaistes sinhronizāciju.

> [!IMPORTANT]
> Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati. Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Tiešsaistes sinhronizācija rāda kļūdu 403 Aizliegts, kad veidojat rindu programmā Finance and Operations

Izveidojot rindu Finance and Operations programmā, iespējams, saņemsit šādu kļūdas ziņojumu:

*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"ziņojums\\":\\"Lietotājs nav organizācijas dalībnieks.\\"}}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts."}}".*

Lai labotu problēmu, izpildiet darbības, kas norādītas rakstā [Sistēmas prasības un priekšnosacījumi](requirements-and-prerequisites.md). Lai izpildītu šīs darbības, duālā ieraksta programmas lietotājiem, kas izveidoti sistēmā Dataverse, ir jābūt sistēmas administratora lomai. Arī atbildīgajai noklusējuma komandai ir jābūt sistēmas administratora lomai.

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Tiešsaistes sinhronizācija jebkurai tabulai nepārtraukti rāda līdzīgu kļūdu, veidojot rindu programmā Finance and Operations

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Varat saņemt kļūdas ziņojumu, piemēram, katru reizi, kad mēģināt saglabāt tabulas datus programmā Finance and Operations:

*Nevar saglabāt izmaiņas datu bāzē. Darba vienība nevar izpildīt transakciju. Nevar rakstīt datus elementa mērvienībās. Ieraksti UnitOfMeasureEntity neizdevās ar kļūdas ziņojumu Nevar sinhronizēt ar elementa mērvienībām.*

Lai atrisinātu problēmu, jums jāpārliecinās, ka priekšnosacījumu atsauces dati ir gan Finance and Operations, gan Dataverse. Piemēram, ja klients, kura Finance and Operations programmā esat, pieder noteiktai klientu grupai, pārliecinieties, ka šī klientu grupa pastāv sistēmā Dataverse.

Ja dati ir abās pusēs un apstiprinājāt, ka problēma nav saistīta ar datiem, izpildiet šīs darbības.

1. Apturiet saistīto tabulu.
2. Piesakieties Finance and Operations programmā un pārliecinieties, ka tabulās DualWriteProjectConfiguration un DualWriteProjectFieldConfiguration ir kļūmīgās rindas ieraksti. Šādi izskatās, piemēram, vaicājums, ja ir kļūdaina tabula **Klienti**.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Ja neveiksmīgajai rindai ir ieraksti pat pēc tabulas kartēšanas apturēšanas, dzēsiet rindas, kas ir saistītas ar neveiksmīgo tabulu. Atzīmējiet kolonnu **projectname** tabulā DualWriteProjectConfiguration un ienesiet ierakstu DualWriteProjectFieldConfiguration tabulā, izmantojot projekta nosaukumu, lai dzēstu rindu.
4. Sāciet tabulas kartēšanu. Pārbaudiet, vai dati ir sinhronizēti bez jebkādām problēmām.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Apstrādāt lasīšanas vai rakstīšanas privilēģiju kļūdas, kad Finance and Operations programmā tiek veidoti dati

Iespējams, saņemsit kļūdas ziņojumu "Nederīgs pieprasījums", kas līdzīgs šim piemēram, kad Finance and Operations programmā veidojat datus.

![Slikta pieprasījuma kļūmes ziņojuma piemērs](media/error_record_id_source.png)

Lai labotu problēmu, ir jāpiešķir pareiza drošības loma kartētas Dynamics 365 Sales vai Dynamics 365 Customer Service biznesa struktūrvienības grupai, lai iespējotu trūkstošās privilēģijas.

1. Programmā Finance and Operations atrodiet biznesa struktūrvienību, kas ir kartēta datu integrācijas savienojuma kopā.

    ![Organizācijas kartēšana](media/mapped_business_unit.png)

2. Piesakieties vidē ar modeļa vadītu Dynamics 365 programmu, pārejiet uz **Iestatījumi \> Drošība** un sameklējiet kartētās biznesa vienības grupu.

    ![Kartētās biznesa vienības grupa](media/setting_security_page.png)

3. Atveriet komandas lapu rediģēšanai, pēc tam atlasiet **Pārvaldīt lomas**, lai atvērtu dialoglodziņu **Pārvaldīt grupu lomas**.

    ![Lomu pārvaldības poga](media/manage_team_roles.png)

4. Piešķiriet lomu ar lasīšanas/rakstīšanas privilēģiju attiecīgajām tabulām un pēc tam atlasiet **Labi**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Labot sinhronizācijas problēmas vidē, kurai ir nesen mainījusies Dataverse vide

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Veidojot datus Finance and Operations programmā, iespējams, saņemsit šādu kļūdas ziņojumu:

*{"entityName": "CustCustomerV3Entity", "executionStatus": 2, "fieldResponses":\[\], "recordResponses":\[{"errorMessage": "**Nevar ģenerēt lietderīgās vērtības elementam CustCustomerV3Entity**", "logDateTime": "2019-08-27T 18:51:52.5843124Z", "verboseError": "Lietderīgas vērtības izveide neizdevās, kļūdas dēļ Nederīgs URI: URI ir tukšs."}\], "isErrorCountUpdated":true}*

Šādi izskatās kļūda modeļa vadītā Dynamics 365 lietojumprogrammā:

*No ISV koda radās neparedzēta kļūda. (ErrorType = ClientError) Negaidīts izņēmums no spraudņa (Izpildīt): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: neizdevās apstrādāt elementa kontu — (savienojuma izveides mēģinājums neizdevās, jo savienotā puse pēc noteikta laikposma nav atbilstoši atbildējusi vai izveidotais savienojums neizdevās, jo savienotais resursdators nav atbildējis*

Šī kļūda rodas, ja Dataverse vide tiek nepareizi atiestatīta tajā pašā laikā, kad mēģināt izveidot datus programmā Finance and Operations.

Lai novērstu problēmu, izpildiet šīs darbības.

1. Piesakieties Finance and Operations virtuālajā mašīnā (VM), atveriet SQL Server Management Studio (SSMS) un meklējiet rindas DUALWRITEPROJECTCONFIGURATIONENTITY tabulā, kur **internalentityname** ir vienāds ar **Klienti V3** un **externalentityname** ir vienāds ar **konti**. Šādi izskatās vaicājums.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Izmantojiet projekta nosaukumu no iepriekšējā vaicājuma rezultātus, lai palaistu šo vaicājumu.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Pārliecinieties, vai **externalenvironmentURL** kolonnai ir pareizs Dataverse vai programmas vietrādis URL. Dzēsiet visas dublētās rindas, kas norāda nepareizu Dataverse vietrādi URL. Dzēsiet atbilstošās rindas DUALWRITEPROJECTFIELDCONFIGURATION un DUALWRITEPROJECTCONFIGURATION tabulās.
4. Tabulas kartēšanas apturēšana un pēc tam atsākšana


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]