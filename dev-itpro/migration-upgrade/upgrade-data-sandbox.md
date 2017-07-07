---
title: "Datu jaunināšana smilškastes vidē"
description: "Šajā tēmā ir izskaidrots, kā veikt datu jaunināšanu no AX 2012 uz Dynamics 365 for Finance and Operations smilškastes vidē."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: lv-lv
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>Datu jaunināšana smilškastes vidē

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Šī uzdevuma rezultāts ir jaunināta datu bāze, ko var izmantot smilškastes vidē. Smilškastes vide ir vide, kurā biznesa lietotāji un funkcionālās grupas dalībnieki var pārbaudīt programmas funkcijas. Šī funkcionalitāte ietver pielāgojumus un datus, kas tika pārcelti no programmas Microsoft Dynamics AX 2012.

Ir ļoti ieteicams datu jaunināšanas procesu vispirms palaist izstrādes vidē un tikai pēc tam palaist to koplietotā smilškastes vidē, jo šādi var samazināt kopējo laiku, kas nepieciešams veiksmīgai datu jaunināšanai. Papildinformāciju skatiet sadaļā [Datu jaunināšana izstrādes vidē](prepare-data-upgrade.md).

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>Pārskats par smilškastes datu jaunināšanas procesu

Pirms sāksit jaunināt datus smilškastes vidē, dati izstrādes vidē jau būs jaunināti, kā izskaidrots sadaļā [Datu jaunināšana izstrādes vidē](prepare-data-upgrade.md). Abi procesi ir ļoti līdzīgi. Galvenā atšķirība ir tā, ka smilškastes vidē datu uzglabāšanai izmanto Microsoft Azure SQL datu bāzi, savukārt izstrādes vidē izmanto Microsoft SQL Server. Šī tehniskā atšķirība datu bāzes līmenī nozīmē, ka jums būs nedaudz jāmodificē datu jaunināšanas procedūra smilškastes vidē, jo dublējumu no AX 2012 datu bāzes instances nevar vienkārši atjaunot SQL datu bāzē.

![Smilškastes datu jaunināšanas process](./media/data-upgrade-sandbox.png)

Tālāk norādītas augstā līmeņa darbības jaunināšanas procesā.

1. Izveidojiet AX 2012 datu bāzes kopiju. Ļoti ieteicams izmantot kopiju, jo ir jādzēš noteikti objekti kopijā, kas tiks eksportēta.
2. Eksportējiet kopēto datu bāzi uz bacpac failu, izmantojot bezmaksas SQL Server rīku ar nosaukumu SQLPackage.exe. Šis rīks nodrošina īpaša tipa datu bāzes dublējumu, ko var importēt SQL datu bāzē.
3. Augšupielādējiet bacpac failu Azure krātuvē.
4. Lejupielādējiet bacpac failu Application Object Server (AOS) datorā smilškastes vidē un pēc tam importējiet to, izmantojot SQLPackage.exe. Pēc tam palaidiet skriptu importētajai datu bāzei, lai atiestatītu SQL datu bāzes lietotājus.
5. Palaidiet pakotni MajorVersionDataUpgrade.zip, lai veiktu datu jaunināšanu importētajai datu bāzei.

## <a name="create-a-copy-of-the-ax-2012-database"></a>AX 2012 datu bāzes kopijas izveide

Jauninātās AX 2012 datu bāzes kopija ir jāizveido, jo no datu bāzes ir jāizdzēš noteikti objekti. Šie objekti ietver visus Microsoft Windows autentifikācijas lietotājus. Šo izmaiņu rezultātā modificēto datu bāzi nevar izmantot programmai AX 2012. Šīs darbības laikā tiek izveidota datu bāzes kopija un dzēsti šie objekti.

Šī darbība ir jāveic datu bāzes administratoram (DBA) vai personai ar līdzīgām zināšanām un pieredzi.

Lai izveidotu datu bāzes kopiju, izveidojiet sākotnējās datu bāzes dublējumu un atjaunojiet to ar jaunu nosaukumu. Pārliecinieties, vai abām datu bāzēm ir pietiekami daudz vietas. Varat izveidot kopiju citā serverī. Tās SQL Server instances versija, kas darbina datu bāzi, nav svarīga.

Tālāk sniegts piemērs kodam, kas veido datu bāzes kopiju. Modificējiet šo piemēru tā, lai tas atbilstu attiecīgajiem datu bāžu nosaukumiem.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Pēc kopijas izveides palaidiet tai tālāk norādīto Transact-SQL (T-SQL) skriptu.
TODO 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>Kopētās datu bāzes eksportēšana uz bacpac failu

Eksportējiet kopēto datu bāzi uz bacpac failu, izmantojot rīku SQLPackage.exe. Šī darbība ir jāveic datu bāzes administratoram vai grupas dalībniekam ar līdzvērtīgām zināšanām.

Ir ļoti svarīgi pirms šīs darbības sākšanas instalēt jaunāko SQL Server Management Studio versiju. Lai gan rīks SQLPackage ir ietverts iepriekšējās Management Studio versijās, tas nedarbosies pareizi šajā darbībā, ja vispirms nebūs instalēta jaunākā versija.

Šī darbība ir svarīga, jo eksportēšana būs jāveic atkārtoti darbības pārtraukuma laikā pirms pāriešanas tiešsaistē. Tālāk sniegti daži padomi.

- Bacpac process ļoti intensīvi noslogo ievadizvadi un centrālo procesoru. Tāpēc eksportēšanu veiciet jaudīgā datorā.
- Rīks SQLPackage ir jāpalaiž lokāli datorā, kas vieso datu bāzi. Rīku SQLPackage nepalaidiet lokālā klēpjdatorā, kas savienots ar datu bāžu datoru, jo šis process intensīvi noslogo arī tīklu.

Pēc tam kā administrators atveriet logu **Komandu uzvedne** un izpildiet tālāk norādītās komandas.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Tālāk sniegts parametru skaidrojums.

- **ssn** (avota servera nosaukums) — tā SQL Server nosaukums, no kura jāeksportē. Šajā piemērā izmantotajam procesam šis parametrs vienmēr ir jāiestata uz **localhost**.
- **sdn** (avota datu bāzes nosaukums) — eksportējamās datu bāzes nosaukums.
- **tf** (mērķa fails) — tā faila ceļš un nosaukums, uz kuru jāeksportē. Mapei ir jau jāpastāv, taču failu izveidos process.
- **/p:CommandTimeout** — taimauta vērtība katram vaicājumam. Šis parametrs ļauj eksportēt lielākas tabulas, nesasniedzot taimautu.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Bacpac faila augšupielāde Azure krātuvē

Augšupielādējiet savu bacpac failu Azure krātuvē. Skatiet UsingStorageExplorer.docx TODO

### <a name="import-the-bacpac-file-into-sql-database"></a>Bacpac faila importēšana SQL datu bāzē

Šīs darbības laikā eksportēto bacpac failu importēsit SQL datu bāzes instancē, ko lieto jūsu smilškastes vide. Vispirms savā smilškastes AOS datorā jums ir jāinstalē jaunākā Management Studio versija. Pēc tam failu importēsit, izmantojot rīku SQLPackage.exe.

Šos uzdevumus veiksit tieši AOS datorā savā smilškastes vidē, jo noteiktas ugunsmūra kārtulas ierobežo piekļuvi SQL datu bāzes instancei. Taču, izmantojot AOS datoru, varat iegūt piekļuvi.

Tāpat kā eksportēšanas darbībā, pirms importēšanas sākšanas ir jābūt instalētai jaunākajai Management Studio versijai. Šo darbību nevarēs veikt, izmantojot vecāku versiju.

Veiktspējas nolūkos bacpac failu ieteicams novietot D diskā AOS datorā. Azure virtuālajās mašīnās (VM) D disks ir fizisks disks, kam parasti ir augstāka veiktspēja, nekā citiem pieejamajiem diskiem.

Kā administrators atveriet logu **Komandu uzvedne** un izpildiet tālāk norādītās komandas.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Tālāk sniegts parametru skaidrojums.

- **tsn** (mērķa servera nosaukums) — tā SQL Azure servera nosaukumus, kurā jāimportē. Nosaukumu var atrast pakalpojumā LCS. Pievienojiet tam sufiksu **.database.windows.net**.
- **tdn** (mērķa datu bāzes nosaukums) — tās datu bāzes nosaukums, kurā jāimportē. Datu bāzes nedrīkst būt jau izveidotas. Tās tiks izveidotas importēšanas procesā.
- **sf** (avota fails) — tā faila ceļš un nosaukums, no kura jāimportē.
- **tp** (mērķa parole) — SQL parole mērķa SQL datu bāzes instancei.
- **tu** (mērķa lietotājs) — SQL lietotājvārds mērķa SQL datu bāzes instancei. Ieteicams izmantot **sqladmin**. Šī lietotāja paroli varat izgūt no sava LCS projekta.
- **/p:CommandTimeout** — taimauta vērtība katram vaicājumam. Šis parametrs ļauj eksportēt lielākas tabulas, nesasniedzot taimautu.
- **/p:DatabaseServiceObjective** — izveidotās datu bāzes pakalpojuma pakāpes līmenis. Esošās datu bāzes vērtību varat pārbaudīt, izmantojot Management Studio. Ar peles labo pogu noklikšķiniet uz datu bāzes un pēc tam atlasiet **Rekvizīti**.

Pēc komandu palaišanas saņemsit tālāk norādīto brīdinājumu. Varat to droši ignorēt.

![Smilškastes kļūda](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>Pakotnes MajorVersionDataUpgrade.zip palaišana

Palaidiet datu jaunināšanas izvietojamo pakotni, kā aprakstīts sadaļā [Datu jaunināšana izstrādes, demonstrācijas un smilškastes vidēs](upgrade-data-to-latest-update.md).

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>Datu bāzes kopijas jaunināšana izstrādes vidē

Ir noderīgi jaunināt to pašu datu bāzi izstrādes vidē. Ja jums izstrādes vidēm ir pieejama datu bāzes kopija, būs daudz vieglāk izpētīt jauninātajā smilškastes vidē atrastās kļūdas.

