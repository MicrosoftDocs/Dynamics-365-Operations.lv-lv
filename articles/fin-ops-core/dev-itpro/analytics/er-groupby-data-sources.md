---
title: Grupēt ierakstus un apkopot aprēķinus, izmantojot GROUPBY datu avotus
description: Šajā tēmā skaidrots, kā var izmantot GROUPBY tipa datu avotus Elektronisko pārskatu (ER).
author: NickSelin
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b79dfe62122a031ae9ed7f51ea7ff578cd47358
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462302"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Grupēt ierakstus un apkopot aprēķinus, izmantojot GROUPBY datu avotus

[!include[banner](../includes/banner.md)]

Konfigurējot elektronisko pārskatu [(ER) modeļa](general-electronic-reporting.md) kartējumus vai formātus, varat [pievienot](#AddMmDataSource2) pieprasītos GroupBy tipa datu **avotus**.

Design laikā GroupBy datu **avots** ir konfigurēts, lai identificētu šādus elementus:

- Bāzes [datu avots,](#BaseDataSource) kas satur ierakstus, kas izpildlaikā tiks grupēti
- [Pamatdatu](#GroupingFields) avota grupēšanas lauki, kas izpildlaikā tiks izmantoti grupēšanai
- [Apkopošanas funkcijas](#AggregateFunctions), kas norāda apkopotos aprēķinus, kas izpildlaikā tiks veikti katrai atklātajām grupām

Izpildlaikā konfigurēti **GroupBy** datu avotu grupu ieraksti, kuriem grupēšanas laukos ir tādas pašas vērtības, un pēc tam atgriež ierakstu sarakstu. Katrs ieraksts pārstāv vienu grupu. Katrai grupai datu avots atklāj lauka vērtības, pēc kurām tika grupēti sākotnējie ieraksti, aprēķināto aprēķina funkciju vērtības un grupai piederīgā pamatdatu avota ierakstu saraksts.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a> Apkopošanas funkcijas

Izpildlaikā katrs apkopošanas aprēķins tiek veikts katrai ierakstu grupai. Šis aprēķins tiek **veikts, lietojot viena lauka vai izteiksmes vērtību tā datu avota ierakstos, kas tika atlasīts grupēšanai rediģējamā datu avotā ar tipu GroupBy**. Pašlaik tiek atbalstītas šādas apkopošanas funkcijas:

- **Avg** – šī funkcija atgriež grupas vērtību vidējo rādītāju. To var izmantot tikai ar skaitliskiem laukiem.
- **SKAITS** – šī funkcija atgriež grupā atrasto krājumu skaitu.
- **Min** – šī funkcija atgriež minimālo vērtību starp vērtībām grupā.
- **Maksimums** – šī funkcija atgriež maksimālo vērtību starp vērtībām grupā.
- **SUM** – šī funkcija atgriež visu grupas vērtību summu. To var izmantot tikai ar skaitliskiem laukiem.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Izpildes vieta

Ja rediģējat **GroupBy** datu avotu un norādāt pamatdatu avotu, kas satur grupēšanai ierakstus, [...](#ExecutionLocation)**sistēma automātiski nosaka visnoderīgs novietojumu šī GroupBy** datu avota izpildei. Ja bāzes [datu](er-functions-list-filter.md#usage-notes) avots ir vaicājums (t.i., ja to var palaist datu bāzes līmenī), programmas datu bāze tiek norādīta arī kā rediģējamas **GroupBy** datu avota izpildes vieta. Pretējā gadījumā programmas servera atmiņa tiek norādīta kā izpildes vieta.

Jūs varat manuāli mainīt automātiski noteiktās izpildes vietu, izvēloties atrašanās vietu, kas ir piemērojama konfigurētam datu avotam. Ja atlasītā izpildes vieta nav piemērojama, izstrādes [laikā tiek](er-components-inspections.md#i5) parādīts apstiprināšanas kļūdas ziņojums.

> [!TIP]
> Ieteicams izmantot datu bāzes atrašanās vietu, lai grupētu datu avotus, kas atklāj lielu skaitu ierakstu.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a> Atmiņas patēriņš

Pēc noklusējuma, ja GroupBy **datu avots tiek palaists atmiņā, programmas servera atmiņa tiek izmantota, lai saglabātu pamatdatu avota ierakstus,** kas pieder katrai atklātai grupai kā vienas grupas ieraksti. Lai palīdzētu samazināt atmiņas patēriņu, varat likvidēt GroupBy **datu avotu ierakstu krātuvi,** ja tie ir konfigurēti, lai aprēķinātu tikai uzkrātās funkcijas un to grupas ieraksti izpildlaikā netiek izmantoti. Lai šādā veidā samazinātu atmiņas patēriņu, iespējojiet atmiņas lietošanas samazināšana ER, **kad ierakstu grupēšana tiek izmantota tikai, lai aprēķinātu apkopojumu līdzekli līdzekļu pārvaldības darbvietā**.**·**

## <a name="alternatives"></a><a name="Alternatives"></a> Alternatīvas

Līdzīgu apkopojumu var aprēķināt, izmantojot [dažādus](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) datu avotu vai ER iebūvēto funkciju tipus.

Lai uzzinātu vairāk par šo līdzekli, izpildiet tālāk norādīto piemēru.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a> Piemērs: GROUPBY datu avota izmantošana apkopotajiem aprēķiniem un ierakstu grupēšanai

Šajā piemērā parādīts, kā lietotājs sistēmas administratora vai elektronisko pārskatu funkcionālā konsultanta lomā var konfigurēt ER **modeļa kartēšanu, kam ir GROUPBY** datu avots, kas tiek izmantots, lai aprēķinātu apkopošanas funkcijas un grupas ierakstus. Šo modeļa kartējumu izmanto, lai drukātu kontroles pārskatu, kad tiek ģenerēta Intrastat deklarācija. Šis pārskats ļauj pārskatīt pārskatā ietvertās Intrastat darbības.

Procedūras šajā piemērā var izpildīt **MICROSOFT KONTROā** Dynamics 365 Finance. 

### <a name="prepare-sample-data"></a>Sagatavot parauga datus

Pārliecinieties, vai Intrastat lapā ir **Intrastat** darbības pārskatiem. Darbībām jābūt atšķirīgiem transportēšanas kodiem, jo darbības tiks grupētas pēc **lauka** Transports šajā piemērā.

![Intrastat darbību sagatavošana Intrastat lapā](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>ER struktūras konfigurēšana

Izpildiet sadaļā [ER struktūras konfigurēšana](er-quick-start2-customize-report.md#ConfigureFramework) norādītās darbības, lai iestatītu ER parametru minimālo kopu. Šis iestatījums ir jāpabeidz, pirms sākat lietot ER struktūru ER modeļa kartēšanas izstrādei.

### <a name="import-the-standard-er-format-configuration"></a>Standarta ER formāta konfigurācijas importēšana

Izpildiet sadaļā [Importēt standarta ER formāta konfigurāciju](er-quick-start2-customize-report.md#ImportERSolution1) norādītās darbības, lai pašreizējai instancei pievienotu Dynamics 365 Finance standarta ER konfigurācijas. Importēt No repozitorija **Intrastat modeļa** konfigurācijas 1. versiju.

### <a name="create-a-custom-data-model-configuration"></a>Pielāgota datu modeļa konfigurācijas izveide

Izpildiet [darbības](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration)**, kas sadaļā Pielāgotā datu modeļa konfigurācijas pievienošana, lai manuāli pievienotu jaunu Intrastat modeļa (litware)** ER **datu modeļa konfigurāciju, kas atvasināta no importētās Intrastat modeļa** konfigurācijas.

### <a name="configure-a-custom-data-model-component"></a>Konfigurēt pielāgotu datu modeļa komponentu

Ievērojiet šos soļus **, lai veiktu pieprasītās izmaiņas atvasinātajā Intrastat modeļa (litware)** datu modelī, tādējādi to var izmantot, lai atklātu transportēšanas kodus ar nepieciešamo informāciju.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Konfigurācijas lapas **konfigurācijas** kokā atlasiet Intrastat modeli **(Litware).**
3. Atlasiet **Noformētājs**.
4. **Datu modeļa veidotāja** lapā modeļa kokā atlasiet **Intrastat**.
5. Atlasiet **Jauns,** lai atlasītajam Intrastat zaram pievienotu jaunu ligzdotu **zaru**. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums ievadiet** Transportēšana **·**.
    2. Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

6. Atlasiet **Jauns,** lai pievienotu jaunu ligzdotu zaru **tikko** pievienotajam transportēšanas mezglam. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums** ievadiet **kodu**.
    2. Laukā **Vienuma veids** atlasiet **Virkne**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

7. Atlasiet **Jauns,** lai transportēšanas zaram pievienotu citu jaunu ligzdotu **zaru**. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums ievadiet** TotalInvoicedAmount **·**.
    2. Laukā **Vienuma veids** atlasiet **Reāls**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

8. Atlasiet **Jauns,** lai transportēšanas zaram pievienotu citu jaunu ligzdotu **zaru**. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums ievadiet** NumberOfTransactions **·**.
    2. Laukā **Vienuma veids** atlasiet **Vesels skaitlis**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

9. Atlasiet **Jauns,** lai transportēšanas zaram pievienotu citu jaunu ligzdotu **zaru**. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums** ievadiet **Darbība**.
    2. Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

10. Jūsu tikko **pievienotajam** darbības līmenim kopsavilkuma cilnē **Zars** atlasiet Mainīt **krājuma atsauci**.
11. **Datu modeļa koka dialoglodziņā** Pārslēgt krājuma atsauci atlasiet **CommodityRecord**. Pēc tam atlasiet **Labi**.

![Konfigurētais datu modelis ER datu modeļu noformētājā.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Pabeigt pielāgotā datu modeļa dizainu

Izpildiet datu modeļa [izstrādes darbības,](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) lai pabeigtu atvasinātā **Intrastat modeļa (litware) datu modeļa** dizainu.

### <a name="create-a-new-model-mapping-configuration"></a>Jauna modeļa kartēšanas konfigurācijas izveidošana

Izpildiet darbības, [...](er-quick-start1-new-solution.md#CreateModelMapping)**kas jāveic, veidojot jaunu modeļu kartēšanas konfigurāciju, lai manuāli pievienotu jaunu Intrastat** parauga kartēšanas ER **modeļa kartēšanas konfigurāciju atvasinātajai Intrastat modeļa (Litware) konfigurācijai**.

### <a name="add-a-new-model-mapping-component"></a>Pievienot jaunu modeļa kartēšanas komponentu

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. **Konfigurācijas lapas konfigurācijas** kokā izvērsiet **Intrastat modeļa** konfigurāciju.
3. **Atlasiet Intrastat parauga kartējuma** konfigurāciju.
4. Atlasiet **Noformētājs**, lai atvērtu kartējumu sarakstu.
5. Atlasiet Dzēst **,** lai noņemtu esošo kartēšanas komponentu.
6. Atlasiet **Jauns,** lai pievienotu jaunu kartēšanas komponentu.
7. Laukā **Definīcija** atlasiet **Intrastat**.
8. Laukā **Nosaukums ievadiet** Intrastat **kartējumu**.
9. Atlasiet **veidotāju**, lai konfigurētu jauno kartējumu.

### <a name="design-the-added-model-mapping-component"></a>Veidot pievienoto modeļa kartēšanas komponentu

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a> Datu avota pievienošana, lai piekļūtu programmas tabulai

Konfigurējiet datu avotu, lai piekļūtu programmas tabulām, kurās ir detalizēta informācija par Intrastat darbībām.

1. Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.
2. Datu avotu **rūtī atlasiet** Pievienot sakni **, lai** pievienotu jaunu datu avotu, kas tiks izmantots, lai piekļūtu **Intrastat tabulai**. Katrs Intrastat tabulas **ieraksts** pārstāv vienu Intrastat darbību.
3. **Datu avota rekvizītu** dialoglodziņa laukā Nosaukums **ievadiet** **Darbība**.
4. Laukā **Tabula** ievadiet **Intrastat**.
5. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a> Datu avota pievienošana Intrastat darbību grupēšanai

Konfigurējiet **GroupBy datu** avotu, lai grupētu Intrastat darbības un aprēķinātu apkopošanas funkcijas.

1. Modeļu kartēšanas **veidotāja** lapas datu avota **tipu** rūtī atlasiet **FunctionsGroup\\ by**.
2. Datu avotu **rūtī atlasiet** Pievienot sakni, lai pievienotu jaunu datu avotu, **kas** tiks izmantots Intrastat darbību grupēšanai un aprēķina apkopošanas funkcijas.
3. **Datu avota rekvizītu dialoglodziņa** laukā Nosaukums **ievadiet** **TransportRecord**.
4. Atlasiet **Labot grupu pēc,** lai konfigurētu grupēšanas nosacījumus.
5. Parametru lapā **"Grupēt pēc"** **datu** avotu sarakstā labajā rūtī atlasiet Darbības datu avotu un izvērsiet to.
6. Atlasiet **Pievienot lauku grupai \> Ko** **·**<a name="BaseDataSource">grupēt, lai norādītu, ka darbības datu avots ir atlasīts kā pamatdatu avots</a> konfigurētam **GroupBy** datu avotam. Transakcijas datu avota **ieraksti** tiks grupēti, un šī datu avota lauka vērtības tiks izmantotas aprēķiniem apkopošanas funkcijās.
7. Izvēlieties **Darījums\Transports** lauku un pēc tam atlasiet **Pievienot lauku \> Grupēts lauks** lai norādītu, ka **Transports** bāzes datu avota lauks ir atlasīts kā <a name="GroupingFields">grupēšanas kritērijs</a> konfigurētajiem **GroupBy** datu avots. Citiem vārdiem sakot, darbības datu **avota** ieraksti tiks grupēti, pamatojoties uz lauka Transportēšana **vērtību**. Katrs konfigurētā GroupBy **datu** avota ieraksts pārstāvēs vienu transportēšanas kodu, kas ir atrodams pamatdatu avota ierakstos.
8. Atlasiet lauku **Transaction\AmountMST** un pēc tam veiciet šādas darbības:

    1. Atlasiet **Lauku Pievienot aprēķināšanai \>, lai** norādītu, ka <a name="AggregateFunctions">šim laukam</a> tiks aprēķināta kopējā funkcija.
    2. **Kopsavilkuma rūts ieraksta**, **kas ir pievienots atlasītajam laukam Transaction\AmountMST**, **laukā Metode** atlasiet **funkciju** Summa.
    3. **Izvēles laukā** Nosaukums ievadiet **TotalInvoicedAmount**.

    Šie iestatījumi norāda, ka katrai transporta grupai tiks aprēķināta **kopējā lauka Transaction\AmountMST** summa.

9. Atlasiet lauku **Transaction\RecId** un pēc tam veiciet šādas darbības:

    1. Atlasiet **Lauku Pievienot aprēķināšanai \>, lai** norādītu, ka šim laukam tiks aprēķināta kopējā funkcija.
    2. Rūts Apkopojumi **ierakstā, kas ir** pievienots atlasītajam laukam Transaction\RecId **,** **laukā Metode atlasiet Skaita** **funkciju.**
    3. Laukā Nosaukums **nav** obligāti ievadiet **NumberOfTransactions**.

    Šie iestatījumi norāda, ka katrai transporta grupai tiks aprēķināts darbību skaits grupā.

10. Atlasiet **Saglabāt**.
11. Pārskatiet <a name="ExecutionLocation">rediģējama</a> datu avota izpildes parametrus. Ievērojiet **, ka laukā** Izpildes vieta automātiski ir **atlasīts** automātiskais datums un **lauka Izpilde** laukā ir iekļauta vērtība **SQL**. Šie iestatījumi norāda, ka atlasītais **transakcijas** bāzes datu avots pašlaik ir vaicājams, **un datu bāzes līmenī varat palaist rediģējamu GroupBy** datu avotu.
12. Atveriet meklēšanu izpildes vietas **laukam**, lai pārskatītu pieejamo vērtību sarakstu. Ievērojiet, ka varat atlasīt **query** vai **·** **atmiņā, lai groupBy** datu avots tiktu palaists datu bāzes līmenī vai programmas servera atmiņā.
13. Atlasiet **Saglabāt** un aizveriet parametru lapu **Rediģēt 'Grupēt pēc** '.
14. Atlasiet **Labi**, lai pabeigtu GroupBy datu **avota** iestatījumus.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a> GroupBy datu avota saistīšana ar datu modeļa laukiem

Saistiet konfigurēto datu avotu ar datu modeļa laukiem, lai norādītu, kā datu modelis izpildlaikā tiks aizpildīts ar programmas datiem.

1. Modeļu kartēšanas **veidotāja** lapā datu modeļa **rūtī** izvērsiet zaru **Transportēšana**.
2. Datu avotu **rūtī** izvērsiet TransportRecord **datu** avotu.
3. Pievienojiet saistījumu, lai atklātu atklāto transporta grupu sarakstu:

    1. **Datu modeļa rūtī** atlasiet krājumu **Transportēšana**.
    2. **Datu avotu rūtī** atlasiet **TransportRecord datu** avotu.
    3. Atlasiet **Saistīt**.

4. Pievienojiet saistījumu, lai atklātu katras atklātas transporta grupas transportēšanas kodu:

    1. Atlasiet transportēšanas **koda datu** modeļa krājumu.
    2. Atlasiet lauku **TransportRecord.grouped.TransportMode** grouped.
    3. Atlasiet **Saistīt**.

5. Pievienojiet saistījumu, lai atklātu aprēķināto apkopošanas funkciju vērtības katrai atklātai transporta grupai:

    1. Atlasiet krājumu **Transport.NumberOfTransactions** datu modelis.
    2. Atlasiet apkopoto **lauku TransportRecord.NumberOfTransactions**.
    3. Atlasiet **Saistīt**.
    4. Atlasiet krājumu **Transport.TotalInvoicedAmount** datu modelis.
    5. Atlasiet lauku **TransportRecord.aggregated.TotalInvoicedAmount**.
    6. Atlasiet **Saistīt**.

6. Pievienojiet saistījumu, lai atklātu darbību ierakstus, kas pieder katrai atklātai transporta grupai:

    1. Atlasiet transporta.darbības **datu** modeļa krājumu.
    2. Atlasiet lauku **TransportRecord.lines**.
    3. Atlasiet **Saistīt**.

    Varat turpināt konfigurēt saistījumus **transportēšanas ligzdotajiem krājumiem.Darbību** **datu modeļa elementa un TransportRecord.rindu** datu avota lauks, lai izpildlaikā atklātu informāciju par Intrastat darbībām, kas pieder katrai atklātai transporta grupai.

![Konfigurētā modeļa kartēšana ER modeļa kartēšanas noformētājā.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Atkļūdot pievienoto modeļa kartēšanas komponentu

[Izmantojiet ER datu avota atkļūdotāju,](er-debug-data-sources.md) lai pārbaudītu konfigurētā modeļa kartēšanu.

1. Modeļu kartēšanas veidotāja lapā **atlasiet Sākt atkļūdošanu** **.**
2. Lapas Atkļūdošanas **datu avoti** kreisajā rūtī **atlasiet TransportRecord** datu avotu un pēc tam atlasiet **Lasīt visus ierakstus**.
3. Izvērsiet TransportRecord **datu** avotu un pēc tam sekojiet šiem soļiem:

    1. **Atlasiet TransportRecord.grouped.TransportMode** datu avotu.
    2. Atlasiet **Iegūt vērtību**.
    3. Atlasiet TransportRecord.grouped.NumberOfTransactions **datu** avotu.
    4. Atlasiet **Iegūt vērtību**.
    5. **Atlasiet TransportRecord.grouped.TotalInvoicedAmount** datu avotu.
    6. Atlasiet **Iegūt vērtību**.

4. Labās puses rūtī atlasiet Izvērst **visu**.

TransportRecord **datu** avots atklāj divus ierakstus un parāda divus transportēšanas kodus. Katram transportēšanas kodam tiek aprēķināts darbību skaits un kopējā rēķinā iekļautā summa.

> [!NOTE]
> Pieeja "lalasot" tiek izmantota, ja GroupBy datu avots **tiek** izsaukts datu bāzes izsaukumu optimizšanai. Tāpēc dažas GroupBy **datu avota lauka vērtības tiek aprēķinātas ER datu avota atkļūdotājam tikai tad,** ja tās ir piesaistītas datu modeļa laukiem.

![Datu avota atkļūdošanas rezultāti lapā Atkļūdošanas datu avoti.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Vai kopsummas ir jāaprēķina, aprēķinot grupu kopsummas?

Jā. Lai aprēķinātu kopsummas, konfigurējiet citu **GroupBy** datu avotu **, kur iepriekš konfigurētais GroupBy** datu avots tiek izmantots kā bāzes datu avots. Šajā **attēlā** **parādīts GroupBy** **tipa kopējo datu avots, kas tiek izmantots, lai aprēķinātu kopējo SUM** funkciju, **pamatojoties uz GroupBy tipa TransportaRecord** **datu avota SUM** **apkopošanu.**

![Kopsummu datu avots ER modeļa kartēšanas veidotājā.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Šajā attēlā redzami Kopsummu datu **avota atkļūdošanas** rezultāti.

![Kopsummu datu avota atkļūdošanas rezultāti lapā Atkļūdošanas datu avoti.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [Atkļūdot izpildītā ER formāta datu avotus, lai analizētu datu plūsmu un transformāciju](er-debug-data-sources.md)
- [DATU APKOPOŠANAS datu avotu izmantošana Elektronisko pārskatu formātos](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
