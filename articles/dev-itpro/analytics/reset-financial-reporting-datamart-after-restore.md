---
title: "Finanšu pārskatu datuves atiestatīšana"
description: "Šajā tēmā ir aprakstīts, kā atiestatīt finanšu pārskatu datuvi."
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: lv-lv
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a>Finanšu pārskatu datuves atiestatīšana

[!include[banner](../includes/banner.md)]

Šajā tēmā ir izskaidrots, kā atiestatīt finanšu pārskatu datuvi tālāk norādītajās versijās.

- Microsoft Dynamics 365 for Finance and Operations Finanšu pārskati, laidiens 7.2.6.0 un jaunāks
- Microsoft Dynamics 365 for Finance and Operations Finanšu pārskati, laidiens 7.0.10000.4 un jaunāks
- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (lokālā)

Lai saņemtu Finance and Operations Finanšu pārskati laidienu 7.2.6.0, varat lejupielādēt KB 4052514 no <https://support.microsoft.com/en-us/help/4052514>.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a>Finanšu pārskatu datuves atiestatīšana Finance and Operations Finanšu pārskati laidienam 7.2.6.0 un jaunākam

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a>Finanšu pārskatu datuves atiestatīšana no pārskatu veidotāja

> [!NOTE]
> Šajā procedūrā ietvertās darbības tiek atbalstītas Finance and Operations Finanšu pārskati laidienā 7.2.6.0 un jaunākos. Ja jums ir agrāks laidiens, sazinieties ar atbalsta darba grupu, lai saņemtu palīdzību.

Noteiktos scenārijos jums var būt nepieciešams atiestatīt finanšu pārskatu datuvi. Šo uzdevumu varat veikt pārskatu veidotāja klientā. Tālāk ir aprakstīti daži scenāriji, kuros varētu rasties nepieciešamība atiestatīt datuvi.

- Finance and Operations datu bāze tika atjaunota, bet datuve netika atjaunota.
- Kādam periodam tiek rādīti nepareizi dati.
- Atbalsta dienests jūs instruē, ka traucējummeklēšanas procedūras ietvaros ir nepieciešams atiestatīt datuvi.

Datuves atiestatīšanu vajadzētu veikt tikai laikā, kad datu bāzes apstrādes apjoms ir mazs. Atiestatīšanas procesa laika finanšu pārskati nav pieejami.

#### <a name="reset-the-data-mart"></a>Datuves atiestatīšana

Lai atiestatītu datuvi, pārskatu veidotāja izvēlnē **Rīki** atlasiet **Atiestatīt datuvi**. Tiek parādīts dialoglodziņš ar divām sadaļām: **Statistika** un **Atiestatīt**.

[![Datuves atiestatīšanas dialoglodziņš](./media/Statistics.png)](./media/Statistics.png)

##### <a name="integration-attempts"></a>Integrācijas mēģinājumi

Režģī **Integrācijas mēģinājumi** tiek rādīts, cik reižu sistēma ir mēģinājusi integrēt transakcijas. Ja pirmie daži mēģinājumi ir nesekmīgi, sistēma datu integrēšanu turpina mēģināt vairākas dienas. Varat zināt, ka datuvi ir nepieciešams atiestatīt, ja šo mēģinājumu skaits ir 8 vai vairāk, kā arī, ja ir daudz dimensiju kombināciju vai transakciju ierakstu. Šādā gadījumā par datiem netiek ziņots.

##### <a name="data-status"></a>Datu statuss

Režģī **Datu statuss** ir sniegts momentuzņēmums par transakcijām, valūtas maiņas kursiem un dimensiju vērtībām datuvē. Liels daudzums novecojušu ierakstu norāda, ka ierakstiem ir notikuši daudzi atjauninājumi. Šāda situācija var palēnināt pārskatu ģenerēšanas laikus.

##### <a name="misaligned-main-account-categories"></a>Nesalāgotas galvenā konta kategorijas

Ja izmantojat laidienu, kas ir agrāks par Microsoft Dynamics 365 for Finance and Operations Finanšu pārskati laidienu 7.2.1, datuvi var būt nepieciešams atiestatīt, ja pārdēvējat kontus vai pārvietojat kontus starp dažādām kategorijām. Šīs darbības var izraisīt nepareizu galvenā konta kategoriju salāgošanu. Laukā **Nesalāgotas galvenā konta kategorijas** tiek rādīts, vai ir radusies šī problēma.

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a>Datuves atiestatīšana Finance and Operations Finanšu pārskati laidienā 7.2.6.0

Lai datuvi atiestatītu Finance and Operations Finanšu pārskati laidienā 7.2.6.0 un agrākos laidienos, dialoglodziņā **Atiestatīt datuvi** atzīmējiet izvēles rūtiņu **Atiestatīt datuvi** un pēc tam noklikšķiniet uz **Labi**. Datuves atiestatīšanu vajadzētu veikt tikai laikā, kad nav ieplānots darbs.

[![Datuves atiestatīšanas izvēles rūtiņa](./media/Reset-72.jpg)](./media/Reset-72.jpg)

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a>Datuves atiestatīšana un iemesla atlasīšana Microsoft Dynamics 365 for Finance and Operations Finanšu pārskati laidienā 7.3.0

Ja konstatējat, ka ir nepieciešams atiestatīt datuvi, atzīmējiet izvēles rūtiņu **Atiestatīt datuvi** un pēc tam laukā **Iemesls** atlasiet iemeslu. Ir pieejamas tālāk minētās opcijas.

- **Trūkstoši vai nepareizi dati** — pamatojoties uz statistisko informāciju, esat konstatējis, ka trūkst datu. Pirms turpināšanas ieteicams sadarboties ar atbalsta dienestu, lai noteiktu cēloni.
- **Atjaunot datu bāzi** — Finance and Operations datu bāze tika atjaunota, bet datuve netika atjaunota.
- **Cits** — datuvi atiestatāt cita iemesla dēļ. Ja raizējaties, ka varētu pastāvēt kāda problēma, sazinieties ar atbalsta dienestu, lai to noskaidrotu.

> [!NOTE]
> Pirms šo darbību veikšanas pārliecinieties, vai visiem esošajiem uzdevumiem ir pabeigta integrēšana. Integrācijas statusu varat apskatīt, atlasot **Rīki** &gt; **Integrācijas statuss**.

#### <a name="clear-users-and-companies"></a>Notīrīt lietotājus un uzņēmumus

Atzīmējiet izvēles rūtiņu **Notīrīt lietotājus un uzņēmumus**, ja atjaunojāt savu datu bāzi, bet pēc tam veicāt kādas izmaiņas lietotājiem vai uzņēmumiem. Vajadzībai atzīmēt šo izvēles rūtiņu vajadzētu rasties reti.

Kad esat gatavs sākt atiestatīšanas procesu, atlasiet **Labi**. Tiek parādīta uzvedne ar lūgumu apstiprināt, ka esat gatavs procesa sākšanai. Ņemiet vērā, ka atiestatīšanas laikā finanšu pārskati nav pieejami un pēc tam notiek sākotnējo datu integrēšana.

Ja vēlaties pārskatīt integrācijas statusu, atlasiet **Rīki** &gt; **Integrācijas statuss**, lai apskatītu pēdējo reizi, kad tika veikta integrēšana, un tās statusu.

[![Integrācijas statusa skatīšana](./media/Integration.png)](./media/Integration.png)

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a>Finanšu pārskatu datuves atiestatīšana Finance and Operations Finanšu pārskati laidienam 7.0.10000.4 un jaunākam

Ja savu Finance and Operations datu bāzi kaut kad atjaunojat no dublējuma vai kopējat datu bāzi no citas vides, ir jāizpilda šajā sadaļā norādītās darbības, lai palīdzētu nodrošināt, ka finanšu pārskatu datuve pareizi izmanto atjaunoto Finance and Operations datu bāzi.

> [!NOTE]
> Šajā procedūrā ietvertās darbības tiek atbalstītas Microsoft Dynamics AX programmas versijai 7.0.1 (2016. gada maijs) (programmas būvējums 7.0.1265.23014 un finanšu pārskatu būvējums 7.0.10000.4) un vēlākai. Ja lietojat vecāku Finance and Operations versiju, sazinieties ar atbalsta dienestu, lai saņemtu palīdzību.

### <a name="export-report-definitions"></a>Pārskatu definīciju eksportēšana

Vispirms izpildiet darbības pārskatu dizainu eksportēšanai no pārskatu veidotāja.

1. Pārskatu veidotājā atlasiet **Uzņēmums** &gt; **Veidošanas bloku grupas**.
2. Atlasiet eksportējamo veidošanas bloku grupu un pēc tam atlasiet **Eksportēt**.

    > [!NOTE]
    > Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.

3. Atlasiet eksportējamās pārskatu definīcijas, veicot tālāk norādītās darbības.

    - Lai eksportētu visas pārskatu definīcijas un saistītos veidošanas blokus, atlasiet **Atlasīt visu**.
    - Lai eksportētu noteiktus pārskatus, rindas, kolonnas, koku struktūras vai dimensiju kopas, atlasiet atbilstošo cilni un pēc tam atlasiet eksportējamos vienumus. Lai cilnē atlasītu vairākus vienumus, nospiediet un turiet taustiņu Ctrl. Kad eksportēšanai atlasāt pārskatus, tiek atlasītas arī saistītās rindas, kolonnas, koki un dimensiju kopas.

4. Atlasiet **Eksportēt**.
5. Ievadiet faila nosaukumu un atlasiet drošu atrašanās vietu, kur vēlaties saglabāt eksportētās pārskatu definīcijas.
6. Atlasiet **Saglabāt**.

Failu varat kopēt vai augšupielādēt drošā atrašanās vietā. Šādi failu vēlāk var importēt citā vidē. Informācija par Microsoft Azure krātuves konta lietošanu skatiet šeit [Datu pārsūtīšana, izmantojot komandrindas utilītu AzCopy](/azure/storage/storage-use-azcopy).

> [!NOTE]
> Krātuves kontu Microsoft nenodrošina Dynamics 365 for Finance and Operations līguma ietvaros. Jums ir jāiegādājas krātuves konts vai jāizmanto atsevišķa Azure abonementa krātuves konts.

> [!WARNING]
> Ņemiet vērā D diska uzvedību Azure virtuālajās mašīnās (VM). Eksportētās veidošanas bloku grupas nedrīkst ilgstoši glabāt D diskā. Papildinformāciju par pagaidu diskiem skatiet šeit: [Izpratne par pagaidu disku Windows Azure virtuālajās mašīnās](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

### <a name="stop-services"></a>Pakalpojumu apturēšana

Tālāk norādītajos Microsoft Windows pakalpojumus būs atvērti savienojumi ar Finance and Operations datu bāzi. Tādēļ ir jālieto Microsoft attālā darbvirsma, lai izveidotu savienojumu ar visiem datoriem šajā vidē, un pēc tam ir jāizmanto fails services.msc, lai apturētu šos pakalpojumus.

- Globālā tīmekļa publicēšanas pakalpojums (visos Application Object Servers [AOS] datoros)
- Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)
- Management Reporter 2012 Process Service (tikai biznesa informācijas [BI] datoros)

### <a name="reset"></a>Atiestatīt

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a>Visjaunākās MinorVersionDataUpgrade.zip pakotnes lejupielādēšana

Lejupielādējiet visjaunāko MinorVersionDataUpgrade.zip pakotni. Norādījumus par to, kā atrast un lejupielādēt pareizo datu jaunināšanas pakotnes versiju, skatiet šeit: [Visjaunākās izvietojamās datu jaunināšanas pakotnes lejupielādēšana](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). Lai lejupielādētu MinorVersionDataUpgrade.zip pakotni, nav nepieciešams jauninājums. Tādēļ jums ir tikai jāizpilda darbības attiecīgās tēmas sadaļā “Visjaunākās izvietojamās datu jaunināšanas pakotnes lejupielādēšana”. Visas pārējās tēmā aprakstītās darbības varat izlaist.

#### <a name="run-scripts-against-the-finance-and-operations-database"></a>Skriptu palaišana ar Finance and Operations datu bāzi

Palaidiet tālāk norādītos skriptus ar Finance and Operations datu bāzi (nevis ar finanšu pārskatu datu bāzi).

- DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
- DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Šie skripti palīdz nodrošināt, ka lietotāju, lomu un izmaiņu izsekošanas iestatījumi ir pareizi.

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a>Windows PowerShell komandas palaišana datu bāzes atiestatīšanai

AOS datorā palaidiet Microsoft Windows PowerShell kā lietotājs ar administratora tiesībām un palaidiet tālāk norādītās komandas, lai atiestatītu integrāciju starp Finance and Operations un finanšu pārskatiem.

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

Tālāk ir sniegts paskaidrojums par komandā **Reset-DatamartIntegration** ietvertajiem parametriem.

- Parametra **-Reason** derīgās vērtības ir **SERVICING**, **BADDATA** un **OTHER**.
- Parametra **-ReasonDetail** vērtība ir brīvs teksts.
- Iemesla un iemesla informācijas vērtības tiek reģistrētas telemetrijas/vides pārraudzībā.

> [!NOTE]
> Pēc šo komandu palaišanas jums tiks lūgts ievadīt **Y**, lai apstiprinātu, ka vēlaties atiestatīt datu bāzi.

#### <a name="restart-services"></a>Pakalpojumu restartēšana

Izmantojiet failu services.msc, lai atkal startētu pakalpojumus, ko iepriekš apturējāt.

- Globālā tīmekļa publicēšanas pakalpojums (visos AOS datoros)
- Microsoft Dynamics 365 for Finance and Operations lielapjoma pārvaldības pakalpojums (tikai tajos AOS datoros, kas nav privāti)
- Management Reporter 2012 apstrādes pakalpojums (tikai BI datoros)

#### <a name="import-report-definitions"></a>Pārskatu definīciju importēšana

Importējiet savus pārskatu dizainus no pārskatu veidotāja, izmantojot eksportēšanas laikā izveidoto failu.

1. Pārskatu veidotājā atlasiet **Uzņēmums** &gt; **Veidošanas bloku grupas**.
2. Atlasiet eksportējamo veidošanas bloku grupu un pēc tam atlasiet **Eksportēt**.

    > [!NOTE]
    > Programmatūrā Dynamics 365 for Finance and Operations tiek atbalstīta tikai viena veidošanas bloku grupa **Noklusējuma**.

3. Atlasiet veidošanas bloku **Noklusējums** un pēc tam atlasiet **Importēt**.
4. Atlasiet failu, kurā ir eksportētās pārskatu definīcijas, un pēc tam atlasiet **Atvērt**.
5. Dialoglodziņā **Importēšana** atlasiet importējamās pārskata definīcijas.

    - Lai importētu visas pārskatu definīcijas un saistītos veidošanas blokus, atlasiet **Atlasīt visu**.
    - Lai importētu noteiktus pārskatus, rindas, kolonnas, kokus vai dimensiju kopas, atlasiet importējamos vienumus.

6. Atlasiet **Importēt**.

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a>Finanšu pārskatu datuves atiestatīšana programmai Finance and Operations (lokālā)

1. Līdziet visiem lietotājiem iziet no Finance and Operations pārskatu veidotāja un finanšu pārskatu apgabala.
2. Palaidiet tālāk norādīto skriptu ar finanšu pārskatu datu bāzi (MRDB).

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. Apcērtiet vai izdzēsiet visus ierakstus no tabulas FINANCIALREPORTS programmas Finance and Operations datu bāzē (AXDB).
4. Apcērtiet vai izdzēsiet visus ierakstus no tabulas FINANCIALREPORTVERSION, ja šāda tabula pastāv programmas Finance and Operations datu bāzē. Ja šī tabula nepastāv programmas Finance and Operations datu bāzē, izlaidiet šo soli.
5. Palaidiet skriptu **ResetDatamart.sql** ar finanšu pārskatu datu bāzi. Šis skripts atspējo datuves integrēšanu, izdzēš visus datuves datus un pēc tam no jauna iespējo datuves integrēšanu.

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. Pēc atiestatīšanas varat manuāli pārbaudīt datu pārlādēšanu, finanšu pārskatu datu bāzei izpildot tālāk norādīto vaicājumu.

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    Pārliecinieties, vai visām rindām ir vērtība **LastRunTime** un vai vienums **StateType** ir iestatīts uz **5**. Vienuma **StateType** vērtība **5** norāda, ka dati tika sekmīgi pārlādēti. Vērtība **7** norāda uz kļūmes stāvokli. Reizēm organizācijas hierarhijas kartei šāds stāvoklis ir pēc pirmās izpildīšanas reizes. Taču kļūmes stāvoklim vajadzētu atrisināties automātiski.

