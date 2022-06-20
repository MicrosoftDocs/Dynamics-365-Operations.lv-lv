---
title: Tiešsaistes sinhronizācijas problēmu novēršana
description: Šajā rakstā ir sniegta traucējummeklēšanas informācija, kas var palīdzēt novērst problēmas, kas saistītas ar tiešo sinhronizāciju.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9d27331b940a95168810c2f1ec4ae240a9df93a8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896710"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Tiešsaistes sinhronizācijas problēmu novēršana

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir sniegta traucējummeklēšanas informācija par dubulto rakstīšanas integrāciju starp Finanšu un operāciju programmām un Microsoft Dataverse. Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas ar tiešsaistes sinhronizāciju.

> [!IMPORTANT]
> Dažām problēmām, kurām šajā rakstu adresēs var būt nepieciešama sistēmas administratora loma Azure Active Directory vai (Azure AD) nomnieka administratora akreditācijas dati. Katrā sadaļā ir paskaidrots, vai ir vajadzīga konkrēta loma vai akreditācijas dati.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Tiešsaistes sihronizācija parāda kļūdu rindas izveidnes laikā

Veidojot rindu Finanšu un operāciju programmā, varat saņemt šādu kļūdas ziņojumu:

*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"ziņojums\\":\\"Lietotājs nav organizācijas dalībnieks.\\"}}\], Attālais serveris atgrieza kļūdu: (403) Aizliegts."}}".*

Lai labotu problēmu, izpildiet darbības, kas norādītas rakstā [Sistēmas prasības un priekšnosacījumi](requirements-and-prerequisites.md). Lai izpildītu šīs darbības, divkāršās rakstīšanas lietojumprogrammas lietotājiem, kuri tika izveidoti pakalpojumā Dataverse, ir jābūt ar sistēmas administratora lomu. Arī atbildīgajai noklusējuma komandai ir jābūt sistēmas administratora lomai.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Tiešsaistes sihronizācija parāda kļūdu, kad notiek mēģinājums saglabāt tabulas datus

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Mēģinot saglabāt tabulas datus finanšu un operāciju programmā, varat saņemt šādu kļūdas ziņojumu:

*Nevar saglabāt izmaiņas datu bāzē. Darba vienība nevar izpildīt transakciju. Nevar rakstīt datus elementa mērvienībās. Ieraksti UnitOfMeasureEntity neizdevās ar kļūdas ziņojumu Nevar sinhronizēt ar elementa mērvienībām.*

Lai novērstu šo problēmu, pārliecinieties, vai priekšnosacījumu atsauces dati pastāv gan finanšu, gan operāciju programmā, kā arī Dataverse. Piemēram, ja klienta ieraksts ietilpst konkrētā klientu grupā, pārliecinieties, ka šī klientu grupa pastāv pakalpojumā Dataverse.

Ja dati ir abās vietās un esat pārliecinājušies, ka problēma nav saistīta ar datiem, izpildiet tālāk minētās darbības.

1. Izmantojot Excel pievienojumprogrammu, atveriet entitīju **DualWriteProjectConfigurationEntity**. Lai izmantotu pievienojumprogrammu, iespējojiet dizaina režīmu Pievienojumprogrammai Finanses un operācijas Excel **un pievienojiet darblapai DualWriteProjectConfigurationEntity**. Papildinformāciju skatiet sadaļā [Elementa datu skatīšana un atjaunināšana programmā Excel](../../office-integration/use-excel-add-in.md).
2. Atlasiet un dzēsiet tos ierakstus, kuriem ir problēmas duālās rakstīšanas kartē un projektā. Katram divkāršās rakstīšanas kartējumam būs divi ieraksti.
3. Publicējiet izmaiņas, izmantojot Excel pievienojumprogrammu. Šī darbība ir svarīga, jo tādējādi tiek dzēsti ieraksti no entitījas un pakārtotajām tabulām.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Apstrādāt privilēģiju lasīšanas vai rakstīšanas kļūdas, veidojot datus finanšu un operāciju programmā

Ja izveidojat datus finanšu un operāciju programmā, varat saņemt kļūdas ziņojumu "Nederīgs pieprasījums".

![Slikta pieprasījuma kļūmes ziņojuma piemērs.](media/error_record_id_source.png)

Lai novērstu problēmu, ir jāiespējo trūkstošā privilēģija, kartēto Dynamics 365 Sales vai Dynamics 365 Customer Service biznesa vienību darba grupai piešķirot pareizu drošības lomu.

1. Finanšu un operāciju programmā atrodiet biznesa vienību, kas ir kartēta datu integrācijas savienojuma kopā.

    ![Organizācijas kartēšana.](media/mapped_business_unit.png)

2. Lietojumprogrammā Customer Engagement, pierakstieties vidē, ejiet uz **Iestatījumi\> Drošība** un atrodiet kartētās biznesa vienības darba grupu.

    ![Kartētās biznesa vienības grupa.](media/setting_security_page.png)

3. Atveriet darba grupas lapu rediģēšanai un atlasiet **Pārvaldīt lomas**.

    ![Lomu pārvaldības poga.](media/manage_team_roles.png)

4. Dialoglodziņā **Darba grupu lomu pārvaldība** piešķiriet lomu, kurai ir lasīšanas/rakstīšanas privilēģija atbilstoŠajām tabulām, un pēc tam atlasiet **Labi**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Labot sinhronizācijas problēmas vidē, kurai ir nesen mainījusies Dataverse vide

**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators

Izveidojot datus Finanšu un operāciju programmā, varat saņemt šādu kļūdas ziņojumu:

*{"entityName": "CustCustomerV3Entity", "executionStatus": 2, "fieldResponses":\[\], "recordResponses":\[{"errorMessage": "**Nevar ģenerēt lietderīgās vērtības elementam CustCustomerV3Entity**", "logDateTime": "2019-08-27T 18:51:52.5843124Z", "verboseError": "Lietderīgas vērtības izveide neizdevās, kļūdas dēļ Nederīgs URI: URI ir tukšs."}\], "isErrorCountUpdated":true}*

Kļūdas ziņojums lietojumprogrammā Customer Engagement:

> Radās neparedzēta kļūda no ISV koda. (ErrorType = ClientError) Negaidīts izņēmums no spraudņa (Izpilde): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: neizdevās apstrādāt entitījas konu - (Savienojuma mēģinājums neizdevās, jo savienotā puse neatbildēja pareizi pēc laika perioda vai izveidotais savienojums neizdevās, jo savienotais resursdators nevarēja atbildēt.

Šī kļūda rodas, ja Dataverse, mēģinot izveidot datus finanšu un operāciju programmā, vide nav pareizi atiestatīta.

> [!IMPORTANT]
> Ja esat pārsaistījuši vides, jums ir jāaptur visas entitīju kartes, pirms turpināt veikt mazināšanas darbības.

Lai novērstu šo problēmu, ir jāveic darbības gan programmā Dataverse Finanses, gan Operācijas.

1. Finanšu un operāciju programmā veiciet šādas darbības:

    1. Izmantojot Excel pievienojumprogrammu, atveriet entitīju **DualWriteProjectConfigurationEntity**. Lai izmantotu pievienojumprogrammu, iespējojiet dizaina režīmu Pievienojumprogrammai Finanses un operācijas Excel **un pievienojiet darblapai DualWriteProjectConfigurationEntity**. Papildinformāciju skatiet sadaļā [Elementa datu skatīšana un atjaunināšana programmā Excel](../../office-integration/use-excel-add-in.md).
    2. Atlasiet un dzēsiet tos ierakstus, kuriem ir problēmas duālās rakstīšanas kartē un projektā. Katram divkāršās rakstīšanas kartējumam būs divi ieraksti.
    3. Publicējiet izmaiņas, izmantojot Excel pievienojumprogrammu. Šī darbība ir svarīga, jo tādējādi tiek dzēsti ieraksti no entitījas un pakārtotajām tabulām.
    4. Lai palīdzētu novērst kļūdas, atkārtoti sasaistot finanses Dataverse un operācijas vai vides, pārliecinieties, vai saglabājas nekādas duālās rakstīšanas konfigurācijas.

2. Pakalpojumā Dataverse izpildiet šīs darbības:

    1. Pierakstieties Dataverse vidē (piemēram, `https://*****.crm.dynamics.com/`).
    2. Dodieties uz **Papildu iestatījumi**\>**Papildu meklēšana**.
    3. Atlasiet **Divkāršās rakstīšanas palaišanas laika konfigurēšana**.
    4. Atlasiet skatāmo kolonnu.
    5. Atlasiet **Rezultāti**, lai skatītu konfigurācijas.
    6. Dzēst visas instances.

3. Finanšu un operāciju programmā veiciet šādas darbības:

    1. Izmantojot Excel pievienojumprogrammu, atveriet entitīju **DualWriteProjectConfigurationEntity**. Lai izmantotu pievienojumprogrammu, iespējojiet dizaina režīmu Pievienojumprogrammai Finanses un operācijas Excel **un pievienojiet darblapai DualWriteProjectConfigurationEntity**. Papildinformāciju skatiet sadaļā [Elementa datu skatīšana un atjaunināšana programmā Excel](../../office-integration/use-excel-add-in.md).
    2. Atlasiet un dzēsiet tos ierakstus, kuriem ir problēmas duālās rakstīšanas kartē un projektā. Katram divkāršās rakstīšanas kartējumam būs divi ieraksti.
    3. Publicējiet izmaiņas, izmantojot Excel pievienojumprogrammu. Šī darbība ir svarīga, jo tādējādi tiek dzēsti ieraksti no entitījas un pakārtotajām tabulām.
    4. Lai palīdzētu novērst kļūdas, atkārtoti sasaistot finanses Dataverse un operācijas vai vides, pārliecinieties, vai saglabājas nekādas duālās rakstīšanas konfigurācijas.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Tiešsaistes sinhronizācijas kļūda pēc tam, kad veida pilna datu bāzes kopēšana

Iespējams, saņemsit šādu kļūdas ziņojumu pēc tam, kad palaidīsit pilnu datu bāzes kopēšanu no vienas sistēmas uz citu un pēc tam mēģināt palaist datu bāzes operāciju:

*SecureConfig Organization (???) nesakrīt ar faktisko CRM organizāciju (???).*

Kļūdas ziņojums tiek rādīts no divkāršās rakstīšanas palaišanas laika spraudni, lai nodrošinātu, ka divkāršās rakstīšanas konfigurācijas, kas ir iestatīta vienā sistēmā, nevar tikt lietota citā sistēmā.

Lai novērstu problēmu, pēc datu bāzes atjaunošanas dzēsiet visus ierakstus no tabulas **msdyn_dualwriteruntimeconfig**. Papildinformāciju skatiet rakstā [Divkāršās rakstīšanas vižu atsaistīšana un atkārtota saistīšana](relink-environments.md).

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Tiešsaistes sinhronizācijas problēmas, kuras rada nepareiza vaicājuma filtra sintakse divkāršās rakstīšanas kartēs

Lai gan divkāršās rakstīšanas kartes filtra vaicājuma izteiksme ir sintaktiski pareiza, tā varētu nedarboties, kā paredzēts. Filtra izteiksme atrodas entitījā, nevis atsevišķā vaicājumu objekta datu avotā. Tāpēc ģenerētais SQL vaicājums neatgriež paredzamos rezultātus.

Tālāk ir minēts piemērs.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

Varētu sagaidīt, ka būtu projekti ar izfiltrētu vecākelementu. Taču filtrs nedarbojas, jo tas tiek tulkots uz vaicājumu, kas atgādina piemēru tālāk.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Faktiskajā rezultātā lauks `parentProject` tiek aprēķināts kā `null`. Taču `null` nav tas pats, kas tukša virkne. Šīs nesakritības dēļ vaicājuma filtrs neatgriež derīgus rezultātus.

Lai novērstu problēmu, izpildiet šīs darbības.

1. Pievienojiet aprēķinātu kolonnu, kuru var pievienot paplašinājuma modelim un kuru balsta loģika, kura pārkonvertē `null` par tukšu virkni.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Lietojiet jaunās apstrādātās kolonnas filtru noklusējuma kolonnas vietā.

Lai aprēķinātu filtru izstrādes vidē, varat izmantot šo X++ kodu, lai pārbaudītu rezultātus. Palaidiet šo kodu kā atsevišķu programmu. Varat to lietot, lai aprēķinātu dažādus filtrus, kuri ir piemērojami entitījai, pirms lietojat šos filtrus duālās rakstīšanas kartēs. Šo vaicājumu var palaist pret datu bāzi, lai izvērtētu neatbilstības.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Dati no finanšu un operāciju programmām nav sinhronizēti ar Dataverse

Veicot tiešo sinhronizāciju, var rasties problēma, Dataverse kur tikai daļa datu ir sinhronizēta no finanšu un operāciju programmām vai arī dati vispār nav sinhronizēti.

> [!NOTE]
> Šo problēmu ir jānovērš izstrādes posmā.

Pirms uzsākat problēmas novēršanu, pārskatiet šādus priekšnosacījumus:

+ Pārbaudiet, vai pielāgotās izmaiņas ir ierakstītas vienas transakcijas tvērumā.
+ Biznesa notikumi un divkāršās rakstīšanas ietvars neapstrādā `doinsert()`, `doUpdate()` un `recordset()` darbības vai ierakstus, kuros ir atzīmēts `skipBusinessEvents(true)`. Ja jūsu kods atrodas Šajās funkcijās, divkāršā rakstīšana netiks aktivizēta.
+ Biznesa notikumi ir jāreģistrē kartējamajam datu avotam. Daži datu avoti var izmantot ārēju savienojumu, un tos var atzīmēt kā lasāmus tikai Finanšu un operāciju programmās. Šie datu avoti netiek izsekoti.
+ Izmaiņas tiks aktivizētas vienīgi tad, ja pārveidojumi atrodas kartētajos laukos. Nekartēto lauku pārveidojumi neaktivizēs divkāršo rakstīšanu.
+ Pārbaudiet, vai filtru aprēķini rada derīgu rezultātu.

### <a name="troubleshooting-steps"></a>Problēmu novēršanas darbības

1. Pārskatiet lauku kartējumus divkāršās rakstīšanas administratora lapā. Ja lauks nav kartēts no finanšu un operāciju programmām Dataverse uz to, tas netiks izsekots. Piemēram, šajā ilustrācijā lauks Apraksts ir **izsekots** Dataverse no Finanšu un operāciju programmām, bet ne no programmas Apraksts. Šis lauks Finanšu un operāciju programmās netiks izsekots.

    ![Izsekotais lauks.](media/live-sync-troubleshooting-1.png)

2. Nosakiet, vai datu avots tiek izsekots biznesa notikumu definīcijā. Piemēram, Šajā attēlā izmaiņas netiks izsekotas nevienam laukam no tabulas **DefaultDimensionDAVs** un tai pakārtotajām tabulām. Datu avoti, kuri izmanto ārējo savienojumu un kuri ir atzīmēti kā tikai lasāmi, netiek izsekoti.

    ![Lauks, kas netiek izsekots.](media/live-sync-troubleshooting-2.png)

3. Nosakiet, vai kartētie tabulas lauki tiek parādīti tabulā **BUSINESSEVENTSDEFINITION**, kā parādīts Šajā attēlā. Ja meklēto lauku nevarat atrast vaicājuma rezultātā, to neaktivizēs divkāršā rakstīšana.

    ![Izsekotais lauks tabulā.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Piemēra situācija

Finanšu un operāciju programmās kontaktpersonas ieraksta adresei ir atjauninājums, bet adreses maiņa nav sinhronizēta Dataverse. Šāds scenārijs notiek, jo **BusinessEventsDefinition** tabulā nav ierakstu, kuriem būtu ietekmētās tabulas un entitījas apvienojums. Konkrēti, tabula **LogisticsPostalAddress** nav entitījas **smmContactpersonCDSV2Entity** datu avots. Entitījas **smmContactpersonCDSV2Entity** datu avots ir **smmContactPersonV2Entity**, savukārt entitītjas **smmContactPersonV2Entity** datu avots ir **LogisticsPostalAddressBaseEntity**. Tabula **LogisticsPostalAddress** ir entitījas **LogisticsPostalAddressBaseEntity** datu avots.

Līdzīga situācija var rasties dažos nestandarta modeļos, piemēram, gadījumos, kad tabula, kas tiek modificēta Finanšu un operāciju programmās, nav sasaistīta ar entītiju, kas to ietver. Piemēram, primārā adrese ir dati, kas aprēķināti entitījā **smmContactPersonCDSV2Entity**. Divkāršās rakstīšanas satvars mēģina noteikt, kā izmaiņas pakārtotajā tabulā tiek kartētas atpakaļ uz entitījām. Parasti šāda pieeja ir pietiekama. Taču dažos gadījumos saite ir tik sarežģīta, ka vajadzīgs konkretizēt. Ir jāpārliecinās, ka saistītās tabulas **RecId** ir tieši pieejams entitījā. Pēc tam jāpievieno statiskā metode, lai pārraudzītu tabulas izmaiņas.

Piemēram, pārskatiet metodi **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()**. Lai apstrādātu šo situāciju, ir pārveidotas entitījas **CustCustomerV3entity** un **VendVendorV2Entity**.

Lai novērstu problēmu, izpildiet šīs darbības.

1. Pievienojiet entitījai **smmContactPersonV2Entity** lauku **PrimaryPostalAddressRecId**. Padariet to par iekšējo.

    ![Lauks pievienots entitījai smmContactPersonV2Entity.](media/Troubleshoot_live_sync_issue_1.png)

2. Pievienojiet to pašu lauku entitījai **smmContactPersonCDSV2Entity**.

    ![Lauks pievienots entitījaismmContactPersonCDSV2Entity.](media/Troubleshoot_live_sync_issue_2.png)

3. Pievienojiet **smmContactPersonCDSV2Entity** klasei šādu metodi.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Sinhronizējiet datu bāzi un izveidojiet lietojumprogrammu.
5. Apturiet visas divkāršās rakstīšanas kartes, kuras ir izveidotas entitījā **smmContactPersonCDSV2Entity**.
6. Sāciet kartēšanu. Vajadzētu būt redzamai jaunai tabulai (Šajā piemērā — **LogisticsPostalAddress**), kuru sākāt izsekot, izmantojot kolonnu **RefTableName** rindai, kurā **refentityname** vērtība tabulā **BusinessEventsDefinition** ir vienāda ar **smmContactPersonCDSV2Entity**.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Kļūda, izveidojot ierakstu, kurā no programmas Finanses un operācijas tika nosūtīti vairāki ieraksti vienā Dataverse paketē

Jebkurai darbībai finanšu un operāciju programma izveido datus paketē un sūta tos kā pakešuzdevumus Dataverse. Ja divi ieraksti ir izveidoti kā daļa no vienas darbības un tie sazzās viens ar otru, iespējams, saņemsit kļūdas ziņojumu, kas līdzīgs šim piemēram, programmā Finanses un operācijas:

*Nevar rakstītn datus entitījā aaa_fundingsources. Nevar uzmeklēt ebecsfs_contracts ar vērtībām {PC00...}. Nevar uzmeklēt aaa_fundingsources ar vērtībām {PC00...}. Rakstīšana uz aaa_fundingources neizdevās ar kļūdas ziņojumu Izņēmuma ziņojums: Attālinātais serveris atgrieza kļūdu (400) Nederīgs pieprasījums.*

Lai novērstu šo problēmu, izveidojiet elementa attiecības programmā Finanses un operācijas, lai norādītu, ka šīs divas entītijas ir saistītas viena ar otru un ka saistītie ieraksti tiek apstrādāti vienā un tajā pašā darbībā.

## <a name="enable-verbose-logging-of-error-messages"></a>Iespējo kļūdas ziņojumu izvērsto reģistrēšanu

Finanšu un operāciju programmā varat saskarties ar kļūdām, kas saistītas ar Dataverse vidi. Kļūdas ziņojums varētu nesaturēt pilno ziņojuma tekstu vai citus saistošus datus. Lai iegūtu vairāk informācijas, varat iespējot izvērsto reģistrēšanu, iestatot IsDebugMode **karodziņu**, **kas ir norādīts DualWriteProjectConfigurationEntity** entītijā visās projekta konfigurācijās Finanšu un operāciju programmās.

1. Izmantojot Excel pievienojumprogrammu, atveriet entitīju **DualWriteProjectConfigurationEntity**. Lai izmantotu pievienojumprogrammu, iespējojiet dizaina režīmu Pievienojumprogrammai Finanses un operācijas Excel **un pievienojiet darblapai DualWriteProjectConfigurationEntity**. Papildinformāciju skatiet sadaļā [Elementa datu skatīšana un atjaunināšana programmā Excel](../../office-integration/use-excel-add-in.md).
2. Iestatiet projektā karodziņu **IsDebugMode** uz **Jā**.
3. Palaidiet scenāriju.
4. Izvērstie ieraksti ir pieejami tabulā **DualWriteErrorLog**. Lai uzmeklētu datus, izmantojot tabulas pārlūku, izmantojiet šo URL: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Lai tvertu vairāk ierakstu atkļūdošanas režīmā, instalējiet atjauninājumu sadaļā [KB 4595434 (Tukšu vērtību, kuras izplatītas Divkāršās rakstīšanas tiešsaistes sinhronizācijā, labošana)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Kļūda, klientam vai kontaktpersonai pievienojot adresi

Mēģinot pievienot debitora adresi vai kontaktu Finanšu un operāciju programmās, varat saņemt šādu kļūdas ziņojumu, Dataverse vai:

*Nevar rakstīt datus uz entitīju msdyn_partypostaladdresses.Writes to DirPartyPostalAddressLocationCDSEntity neizdevās ar kļūdas ziņojumu Pieprasījums neizdevās ar statusa kodu BadRequest un CDS kļūdas kodu : 0x80040265 atbildes ziņojums: Spraudnī radās kļūda. Ieraksts ar atribūta vērtībām Atrašanās vietas ID jau pastāv. Entitījas atslēgai Atrašanās vietas ID atslēga ir vajadzīgs, ka šī atribūtu kopa satur unikālas vērtības. Atlasiet unikālās vērtības un mēģiniet vēlreiz.*

Lai novērstu problēmu, instalējiet divkāršās rakstīšanas saskaņošanas pakotnes versiju (2.2.2.60) tā, lai tabulas **Adrese** atslēgas tiek definētas, kā parādīts Šajā tabulā.

| Rekvizīts | Vērtība |
|---|---|
| Parādāmais vārds | **Atrašanās vietas atslēga** |
| Nosaukums/vārds, uzvārds | **msdyn_locationkey** |
| Lauki | **msdyn_locationid**, **parentid** |
| Statuss | **Aktīvie** |
| Sistēmas uzdevums | Tukšs |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Kļūda, klientam vai kontaktpersonai pievienojot adresi Dataverse

Iespējams, mēģinot pievienot klientu lietojumprogrammā Dataverse, saņemsit šādu kļūdas ziņojumu:

*"RecordError0":"Rakstīšana neizdevās entitījai Klientu V3 ar nezināmu izņēmumu — Puses ieraksts netika atrasts puses veidam ´Organizācija´'"}.*

Kad pakalpojumā Dataverse tiek izveidots klients, tiek ģenerēts jauns puses numurs. Kļūdas ziņojums tiek parādīts, kad debitora ieraksts kopā ar pusi ir sinhronizēts ar finanšu un operāciju programmām, bet debitora ieraksts ar citu puses numuru jau pastāv.

Lai novērstu problēmu, atrodiet klientu, izmantojot puses uzmeklēšanu. Ja klients nepastāv, izveidojiet jaunu klienta ierakstu. Ja klients pastāv, izmantojiet esošo pusi, lai izveidotu jaunu klienta ierakstu.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Kļūda, pakalpojumā Dataverse izveidojot jaunu klientu, piegādātāju vai kontaktpersonu.

Iespējams, saņemsit šādu kļūdas ziņojumu, mēģinot pakalpojumā Dataverse izveidot jaunu klientu, piegādātāju vai kontaktpersonu:

*Nevar atjaunināt puses veidu no 'DirOrganization' uz 'DirPerson', tā vietā vajadzētu dzēst esošo pusi un pēc tam ievadīt jauno veidu.*

Pakalpojumā Dataverse ir tabulas **msdyn_party** skaitļu secība. Kad Dataverse ir izveidots konts, tiek izveidota jauna puse (piemēram, **Organizācijas** tipa **Party-001**). Šie dati tiek sūtīti uz programmu Finanses un operācijas. Dataverse Ja vide ir Dataverse atiestatīta vai Finanšu un operāciju vide ir saistīta ar citu vidi, Dataverse un tad tiek izveidots jauns kontaktpersonas ieraksts, tiek izveidota jauna puses vērtība, **kas sākas ar Party-001**. Šoreiz izveidotais puses ieraksts būs **Personas** tipa **Party-001**. Kad šie dati ir sinhronizēti, finanšu un operāciju programmas parāda iepriekšējo kļūdas ziņojumu, **jo puses ieraksts Party-001** **ar organizācijas** tipu jau pastāv.

Lai novērstu šo problēmu, nomainīt automātisko skaitļu secību Dataverse tabulas **msdyn_party** laukam **msdyn_partynumber** uz citu automātisko skaitļu secību.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Veiktspējas problēma klienta vai kontaktpersonas kartēšanā

Iespējams, varēsit daļēji uzlabot tiešsaistes sinhronizācijas sniegumu klientiem un kontaktpersonām, pielāgojot **getEntityDataSourceToFieldMapping** metodi (entitījā **CustCustomerV3Entity**) un metodi **getEntityDataSourceToFieldMapping** (**smmContactPersonCDSV2Entity** entitījā). Šie pielāgojumi samazina ierakstu skaitu tabulā **BusinessEventsDefinition**. Taču šis ierakstu skaita samazinājums samazina pacelto notikumu skaitu.

Metode **getEntityDataSourceToFieldMapping** entitījā **CustCustomerV3Entity** nodrošina, ka klienta elektroniskās vai pasta adreses atjauninājums aktivizē biznesa notikumus, tāpēc atjauninātie dati tiks sūtīti uz Dataverse. Ja nelietojat visus laukus un nav vajadzīga informācija divkārŠajā rakstīšanā, izkomentējiet atbilstošās metodes rindas. Katrs izsekotais lauks un tabula, kuru pievieno Šajā metodē, pievieno ierakstu tabulā **BusinessEventsDefinition** izsekotās tabulas un izsekotās entitījas apvienojumam.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Līdzīgā veidā metode **getEntityDataSourceToFieldMapping** entitījā **smmContactPersonCDSV2Entity** nodrošina, ka kontaktpersonas elektroniskās vai pasta adreses atjauninājums aktivizē biznesa notikumus, tāpēc atjauninātie dati tiks sūtīti uz Dataverse. Šajā metodē varat izkomentēt rindas jebkuram laukam, kuru nelietojat.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Pēc metožu atjaunināšanas, izpildiet tālāk norādītās darbības.

1. Sinhronizējiet datu bāzi un izveidojiet lietojumprogrammu.
2. Apturiet visas divkāršās rakstīšanas kartes entitījā **smmContactPersonCDSV2Entity** un **CustCustomerV3Entity**.
3. Sāciet kartēšanu. Jums vajadzētu redzēt mazāk ierakstu entitījās **smmContactPersonCDSV2Entity** un **CustCustomerV3Entity** un tabulā **BusinessEventsDefinition**, un sniegumam vajadzētu daļēji uzlaboties.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
