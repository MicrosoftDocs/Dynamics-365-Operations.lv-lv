---
title: Grupējiet ierakstus un apkopojiet aprēķinus, izmantojot GROUPBY datu avotus
description: Šajā tēmā ir paskaidrots, kā GROUPBY tipa datu avotus izmantot elektroniskajā ziņošanā (ER).
author: NickSelin
ms.date: 01/31/2022
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
ms.openlocfilehash: 5a6cdc486c5f799bdedafa38e90be989fd328c96
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075757"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Grupējiet ierakstus un apkopojiet aprēķinus, izmantojot GROUPBY datu avotus

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Kad jūs konfigurējat [Elektroniskā ziņošana (ER)](general-electronic-reporting.md) modeļu kartējumus vai formātus, varat [pievienot](#AddMmDataSource2) nepieciešamie datu avoti **GroupBy** veids.

Projektēšanas laikā a **GroupBy** datu avots ir konfigurēts, lai identificētu šādus elementus:

- A [bāzes datu avots](#BaseDataSource) kurā ir ieraksti, kas izpildlaikā tiks grupēti
- [Lauku grupēšana](#GroupingFields) no bāzes datu avota, kas tiks izmantots ierakstu grupēšanai izpildlaikā
- [Apkopotās funkcijas](#AggregateFunctions) kas norāda kopējos aprēķinus, kas izpildes laikā tiks veikti katrai atklātajai grupai

Izpildes laikā ir konfigurēts **GroupBy** datu avots sagrupē ierakstus, kuriem grupēšanas laukos ir vienādas vērtības, un pēc tam atgriež ierakstu sarakstu. Katrs ieraksts apzīmē vienu grupu. Katrai grupai datu avots parāda lauku vērtības, pēc kurām tika grupēti sākotnējie ieraksti, aprēķināto apkopoto funkciju vērtības un grupai piederošā bāzes datu avota ierakstu sarakstu.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a> Apkopotās funkcijas

Izpildlaikā katrs apkopotais aprēķins tiek veikts katrai ierakstu grupai. Šis aprēķins tiek veikts, izmantojot viena lauka vērtību vai izteiksmi datu avota ierakstos, kas atlasīti grupēšanai rediģējamajā datu avotā.**GroupBy** veids. Pašlaik tiek atbalstītas šādas apkopotās funkcijas:

- **AVG** – Šī funkcija atgriež vidējo vērtību grupā. To var izmantot tikai ar ciparu laukiem.
- **SKAITĪT** – Šī funkcija atgriež grupā atrasto vienumu skaitu.
- **Min** – Šī funkcija atgriež minimālo vērtību starp vērtībām grupā.
- **Maks** – Šī funkcija atgriež maksimālo vērtību starp vērtībām grupā.
- **SUMMA** – Šī funkcija atgriež visu grupas vērtību summu. To var izmantot tikai ar ciparu laukiem.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Izpildes vieta

Kad rediģējat a **GroupBy** datu avotu un norādiet bāzes datu avotu, kurā ir ieraksti, kas jāgrupē, sistēma automātiski nosaka visefektīvāko [atrašanās vieta](#ExecutionLocation) tā izpildei **GroupBy** datu avots. Ja bāzes datu avots ir [jautājams](er-functions-list-filter.md#usage-notes) (tas ir, ja to var palaist datu bāzes līmenī), lietojumprogrammu datu bāze tiek norādīta arī kā rediģējamā faila izpildes vieta **GroupBy** datu avots. Pretējā gadījumā kā izpildes vieta tiek norādīta lietojumprogrammu servera atmiņa.

Varat manuāli mainīt automātiski noteikto izpildes vietu, atlasot vietu, kas ir piemērojama konfigurētajam datu avotam. Ja atlasītā izpildes vieta nav piemērojama, a [validācijas kļūda](er-components-inspections.md#i5) tiek izmests projektēšanas laikā.

> [!TIP]
> Mēs iesakām izmantot datu bāzes atrašanās vietu, lai grupētu datu avotus, kas atklāj lielu skaitu ierakstu.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a> Atmiņas patēriņš

Pēc noklusējuma, ja a **GroupBy** datu avots tiek palaists atmiņā, lietojumprogrammu servera atmiņa tiek izmantota, lai saglabātu katrai atklātajai grupai piederošā bāzes datu avota ierakstus kā vienas grupas ierakstus. Lai samazinātu atmiņas patēriņu, varat apspiest ierakstu krātuvi **GroupBy** datu avoti, ja tie ir konfigurēti, lai aprēķinātu tikai apkopotas funkcijas, un to grupas ieraksti netiek izmantoti izpildlaikā. Lai šādā veidā samazinātu atmiņas patēriņu, iespējojiet **Samaziniet atmiņas izmantošanu ER, ja ierakstu grupēšana tiek izmantota tikai apkopojumu aprēķināšanai** funkcija sadaļā **Funkciju pārvaldība** darba vieta.

## <a name="alternatives"></a><a name="Alternatives"></a> Alternatīvas

Līdzīgus apkopojumus var aprēķināt, izmantojot [savādāk](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) datu avotu veidi vai ER iebūvētās funkcijas.

Lai uzzinātu vairāk par šo līdzekli, izpildiet tālāk norādīto piemēru.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a> Piemērs: izmantojiet GROUPBY datu avotu apkopotiem aprēķiniem un ierakstu grupēšanai

Šajā piemērā parādīts, kā lietotājs sistēmas administratora vai elektroniskās atskaites funkcionālā konsultanta lomā var konfigurēt ER modeļa kartējumu, kam ir **GROUPBY** datu avots, ko izmanto, lai aprēķinātu apkopotās funkcijas un grupu ierakstus. Šis modeļa kartējums tiek izmantots kontroles ziņojuma drukāšanai, kad tiek ģenerēta Intrastat deklarācija. Šis pārskats ļauj pārskatīt Intrastat transakcijas, par kurām ziņots.

Šajā piemērā minētās procedūras var pabeigt **DEMF** uzņēmums Microsoft Dynamics 365 Finance. 

### <a name="prepare-sample-data"></a>Sagatavojiet datu paraugus

Pārliecinieties, vai jums ir Intrastat darījumi, lai ziņotu par **Intrastat** lappuse. Jums ir jābūt darījumiem ar dažādiem transporta kodiem, jo jūs grupēsit transakcijas pēc **Transports** lauks šajā piemērā.

![Intrastat darījumu sagatavošana Intrastat lapā.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>ER struktūras konfigurēšana

Izpildiet sadaļā [ER struktūras konfigurēšana](er-quick-start2-customize-report.md#ConfigureFramework) norādītās darbības, lai iestatītu ER parametru minimālo kopu. Šī iestatīšana ir jāpabeidz, pirms sākat izmantot ER ietvaru, lai izstrādātu ER modeļa kartējumu.

### <a name="import-the-standard-er-format-configuration"></a>Standarta ER formāta konfigurācijas importēšana

Izpildiet sadaļā [Importēt standarta ER formāta konfigurāciju](er-quick-start2-customize-report.md#ImportERSolution1) norādītās darbības, lai pašreizējai instancei pievienotu Dynamics 365 Finance standarta ER konfigurācijas. Importēt 1. versiju **Intrastat modelis** konfigurāciju no repozitorija.

### <a name="create-a-custom-data-model-configuration"></a>Izveidojiet pielāgotu datu modeļa konfigurāciju

Izpildiet šajā punktā norādītās [darbības, lai pievienotu pielāgotu datu modeļa konfigurāciju](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration), lai manuāli pievienotu jaunu **Intrastat modeļa (Litware)** ER datu modeļa konfigurāciju, kas iegūta no importētās **Intrastat modeļa** konfigurācijas.

### <a name="configure-a-custom-data-model-component"></a>Pielāgota datu modeļa komponenta konfigurēšana

Veiciet šīs darbības, lai veiktu nepieciešamās izmaiņas atvasinātajā **Intrastat modeļa (Litware)** datu modelī, lai to varētu izmantot transporta kodu atklāšanai, kuriem ir nepieciešamā informācija.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. **Lapas Konfigurācijas konfigurācijas** kokā atlasiet **Intrastat modelis (litware)**.
3. Atlasiet **Noformētājs**.
4. Lapas **Datu modeļa noformētājs** modeļa kokā atlasiet **Intrastat**.
5. Atlasiet **Jauns**, lai atlasītajam **Intrastat** zaram pievienotu jaunu ligzdotu zaru. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums** ievadiet **Transports**.
    2. Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

6. Atlasiet **Jauns**, lai tikko pievienotajam **transporta** mezglam pievienotu jaunu ligzdotu mezglu. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums** ievadiet **Kods**.
    2. Laukā **Vienuma veids** atlasiet **Virkne**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

7. Atlasiet **Jauns**, lai transporta **mezglam pievienotu vēl vienu ligzdotu** mezglu. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums ievadiet** TotalInvoicedAmount **·**.
    2. Laukā **Vienuma veids** atlasiet **Reāls**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

8. Atlasiet **Jauns**, lai transporta **mezglam pievienotu vēl vienu ligzdotu** mezglu. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums ievadiet** NumberOfTransactions **·**.
    2. Laukā **Vienuma veids** atlasiet **Vesels skaitlis**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

9. Atlasiet **Jauns**, lai transporta **mezglam pievienotu vēl vienu ligzdotu** mezglu. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Laukā **Nosaukums** ievadiet **Transakcija**.
    2. Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

10. Tikko pievienotajam transakcijas **zaram** kopsavilkuma cilnē Zars **atlasiet** Pārslēgt preces atsauci **.**
11. **Dialoglodziņa Krājuma atsauces** pārslēgšana datu modeļa kokā atlasiet **CommodityRecord**. Pēc tam atlasiet **Labi**.

![Konfigurētais datu modelis ER datu modeļu noformētājā.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Pielāgota datu modeļa noformējuma pabeigšana

Izpildiet norādītās [darbības, lai pabeigtu datu modeļa](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) noformējumu, lai pabeigtu atvasinātā **Intrastat modeļa (Litware)** datu modeļa izstrādi.

### <a name="create-a-new-model-mapping-configuration"></a>Jauna modeļa kartēšanas konfigurācijas izveidošana

Izpildiet šajā punktā norādītās darbības, kas norādītas kā [Izveidot jaunu modeļa kartēšanas konfigurāciju](er-quick-start1-new-solution.md#CreateModelMapping), lai manuāli pievienotu jaunu **Intrastat paraugu kartēšanas** ER modeļa kartēšanas konfigurāciju atvasinātajai **Intrastat modeļa (Litware)** konfigurācijai.

### <a name="add-a-new-model-mapping-component"></a>Pievienot jaunu modeļa kartēšanas komponentu

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. **Lapas Konfigurācijas konfigurācijas** kokā izvērsiet **Intrastat modeļa** konfigurāciju.
3. Atlasiet **Intrastat izlases kartēšanas** konfigurāciju.
4. Atlasiet **Noformētājs**, lai atvērtu kartējumu sarakstu.
5. Atlasiet **Dzēst**, lai noņemtu esošo kartēšanas komponentu.
6. Atlasiet **Jauns**, lai pievienotu jaunu kartēšanas komponentu.
7. Laukā **Definīcija** atlasiet **Intrastat**.
8. Laukā **Nosaukums ievadiet** Intrastat **kartējumu**.
9. Atlasiet **Noformētājs**, lai konfigurētu jauno kartējumu.

### <a name="design-the-added-model-mapping-component"></a>Pievienotā modeļa kartēšanas komponenta noformēšana

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a> Datu avota pievienošana, lai piekļūtu lietojumprogrammu tabulai

Konfigurējiet datu avotu, lai piekļūtu lietojumprogrammu tabulām, kurās ir detalizēta informācija par Intrastat darbībām.

1. Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.
2. **Rūtī Datu avoti** atlasiet **Pievienot sakni**, lai pievienotu jaunu datu avotu, kas tiks izmantots, lai piekļūtu Intrastat **tabulai**. Katrs ieraksts **Intrastat** tabulā apzīmē vienu Intrastat darbību.
3. **Dialoglodziņa Datu avota rekvizīti** laukā **Nosaukums** ievadiet **Transakcija**.
4. Laukā **Tabula** ievadiet **Intrastat**.
5. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a> Pievienojiet datu avotu Intrastat darījumu grupai

Konfigurēt a **GroupBy** datu avots, lai grupētu Intrastat darījumus un aprēķinātu apkopotās funkcijas.

1. Uz **Modeļu kartēšanas dizainers** lapā, sadaļā **Datu avotu veidi** rūts, atlasiet **Funkcijas\\ Grupēt pēc**.
2. Iekš **Datu avoti** rūts, atlasiet **Pievienojiet sakni** lai pievienotu jaunu datu avotu, kas tiks izmantots Intrastat darījumu grupēšanai un apkopojuma funkciju aprēķināšanai.
3. Iekš **Datu avota rekvizīti** dialoglodziņā **Vārds** laukā, ievadiet **TransportRecord**.
4. Izvēlieties **Rediģēt grupu pēc** lai konfigurētu grupēšanas nosacījumus.
5. Uz **Rediģējiet parametrus "Grupēt pēc".** lapā, datu avotu sarakstā labajā rūtī atlasiet **Darījums** datu avotu un paplašiniet to.
6. Izvēlieties **Pievienot lauku \> Ko grupēt** lai norādītu, ka **Darījums** datu avots ir atlasīts kā <a name="BaseDataSource">bāzes datu avots</a> konfigurētajiem **GroupBy** datu avots. Ieraksti par **Darījums** datu avots tiks grupēts, un šī datu avota lauku vērtības tiks izmantotas aprēķiniem apkopotās funkcijās.
7. Izvēlieties **Darījums\Transports** lauku un pēc tam atlasiet **Pievienot lauku \> Grupēts lauks** lai norādītu, ka **Transports** bāzes datu avota lauks ir atlasīts kā <a name="GroupingFields">grupēšanas kritērijs</a> konfigurētajiem **GroupBy** datu avots. Citiem vārdiem sakot, ieraksti par **Darījums** datu avots tiks grupēts, pamatojoties uz vērtību **Transports** lauks. Katrs konfigurētā ieraksts **GroupBy** datu avots attēlos vienu transporta kodu, kas ir atrasts bāzes datu avota ierakstos.
8. Izvēlieties **Darījums\SummaMST** laukā un pēc tam veiciet šīs darbības:

    1. Izvēlieties **Pievienot lauku \> Apkopotie lauki** lai norādītu, ka an<a name="AggregateFunctions">agregāta funkcija</a> tiks aprēķināts šim laukam.
    2. Iekš **Apkopojumi** rūtī ierakstā, kas ir pievienots atlasītajam **Darījums\SummaMST** laukā **Metode** laukā atlasiet **Summa** funkcija.
    3. Iekš **Vārds** neobligāts lauks, ievadiet **TotalInvoicedAmount**.

    Šie iestatījumi nosaka, ka katrai transporta grupai kopējā summa **Darījums\SummaMST** lauks tiks aprēķināts.

9. Izvēlieties **Darījums\RecID** laukā un pēc tam veiciet šīs darbības:

    1. Izvēlieties **Pievienot lauku \> Apkopotie lauki** lai norādītu, ka šim laukam tiks aprēķināta apkopotā funkcija.
    2. Iekš **Apkopojumi** rūtī ierakstā, kas ir pievienots atlasītajam **Darījums\RecID** laukā **Metode** laukā atlasiet **Skaitīt** funkcija.
    3. Iekš **Vārds** neobligāts lauks, ievadiet **Darījumu skaits**.

    Šie iestatījumi nosaka, ka katrai transporta grupai tiks aprēķināts transakciju skaits grupā.

10. Atlasiet **Saglabāt**.
11. Pārskatiet<a name="ExecutionLocation">izpildi</a> rediģējamā datu avota parametri. Ievērojiet to **Automātiski noteikt** ir automātiski atlasīts mapē **Izpildes vieta** lauks un **Izpilde plkst** lauks satur vērtību **SQL**. Šie iestatījumi norāda, ka atlasītais **Darījums** bāzes datu avots pašlaik ir vaicājums, un jūs varat palaist rediģējamo **GroupBy** datu avots datu bāzes līmenī.
12. Atveriet meklēšanu **Izpildes vieta** laukā, lai pārskatītu pieejamo vērtību sarakstu. Ņemiet vērā, ka varat izvēlēties **Vaicājums** vai **Atmiņā** lai to piespiestu **GroupBy** datu avots, kas jāpalaiž datu bāzes līmenī vai lietojumprogrammu servera atmiņā.
13. Izvēlieties **Saglabāt** un aizveriet **Rediģējiet parametrus "Grupēt pēc".** lappuse.
14. Izvēlieties **labi** lai pabeigtu iestatījumus **GroupBy** datu avots.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a> Saistiet GroupBy datu avotu ar datu modeļa laukiem

Saistiet konfigurēto datu avotu ar datu modeļa laukiem, lai norādītu, kā datu modelis izpildes laikā tiks aizpildīts ar lietojumprogrammas datiem.

1. Uz **Modeļu kartēšanas dizainers** lapā, sadaļā **Datu modelis** rūti, izvērsiet **Transports** mezgls.
2. Iekš **Datu avoti** rūti, izvērsiet **TransportRecord** datu avots.
3. Pievienojiet saiti, lai atklātu atklāto transporta grupu sarakstu:

    1. Iekš **Datu modelis** rūti, atlasiet **Transports** lieta.
    2. Iekš **Datu avoti** rūti, atlasiet **TransportRecord** datu avots.
    3. Atlasiet **Saistīt**.

4. Pievienojiet saiti, lai atklātu katras atklātās transporta grupas transporta kodu:

    1. Izvēlieties **Transports.Kods** datu modeļa vienums.
    2. Izvēlieties **TransportRecord.grouped.TransportMode** grupēts lauks.
    3. Atlasiet **Saistīt**.

5. Pievienojiet saistījumu, lai parādītu aprēķināto apkopoto funkciju vērtības katrai atklātajai transporta grupai:

    1. Izvēlieties **Transports.NumberOfTransactions** datu modeļa vienums.
    2. Izvēlieties **TransportRecord.aggregated.NumberOfTransactions** apkopots lauks.
    3. Atlasiet **Saistīt**.
    4. Izvēlieties **Transport.TotalInvoicedAmount** datu modeļa vienums.
    5. Izvēlieties **TransportRecord.aggregated.TotalInvoicedAmount** apkopots lauks.
    6. Atlasiet **Saistīt**.

6. Pievienojiet saiti, lai atklātu darījumu ierakstus, kas pieder katrai atklātajai transporta grupai:

    1. Izvēlieties **Transports. Darījums** datu modeļa vienums.
    2. Izvēlieties **TransportRecord.lines** lauks.
    3. Atlasiet **Saistīt**.

    Varat turpināt konfigurēt saistījumus ligzdotajiem vienumiem **Transports. Darījums** datu modeļa vienums un **TransportRecord.lines** datu avota lauku, lai izpildlaikā parādītu informāciju par Intrastat transakcijām, kas pieder katrai atklātajai transporta grupai.

![Konfigurētā modeļa kartēšana ER modeļa kartēšanas noformētājā.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Atkļūdojiet pievienoto modeļa kartēšanas komponentu

Izmantojiet [ER datu avota atkļūdotājs](er-debug-data-sources.md) lai pārbaudītu konfigurēto modeļa kartēšanu.

1. Uz **Modeļu kartēšanas dizainers** lapu, atlasiet **Sāciet atkļūdošanu**.
2. Uz **Atkļūdot datu avotus** lapā, kreisajā rūtī atlasiet **TransportRecord** datu avots un pēc tam atlasiet **Lasīt visus ierakstus**.
3. Paplašiniet **TransportRecord** datu avotu un pēc tam veiciet šīs darbības:

    1. Izvēlieties **TransportRecord.grouped.TransportMode** datu avots.
    2. Atlasiet **Iegūt vērtību**.
    3. Izvēlieties **TransportRecord.grouped.NumberOfTransactions** datu avots.
    4. Atlasiet **Iegūt vērtību**.
    5. Izvēlieties **TransportRecord.grouped.TotalInvoicedAmount** datu avots.
    6. Atlasiet **Iegūt vērtību**.

4. Labajā rūtī atlasiet **Paplašināt visu**.

The **TransportRecord** datu avots atklāj divus ierakstus un uzrāda divus transporta kodus. Katram transporta kodam tiek aprēķināts darījumu skaits un kopējā rēķina summa.

> [!NOTE]
> "Slinks lasīšanas" pieeja tiek izmantota, ja a **GroupBy** datu avots tiek izsaukts, lai optimizētu datu bāzes izsaukumus. Tāpēc dažas lauka vērtības a **GroupBy** datu avots tiek aprēķināti ER datu avota atkļūdotājs tikai tad, ja tie ir saistīti ar datu modeļa laukiem.

![Datu avota atkļūdošanas rezultāti lapā Atkļūdošanas datu avoti.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Vai ir kāds veids, kā aprēķināt kopsummas, kad tiek aprēķinātas grupas kopsummas?

Jā. Lai aprēķinātu kopējās summas, konfigurējiet citu **GroupBy** datu avots, kur **GroupBy** Iepriekš konfigurētais datu avots tiek izmantots kā bāzes datu avots. Nākamajā attēlā parādīts **Kopsummas** datu avots **GroupBy** veids, kas tiek izmantots, lai aprēķinātu kopsavilkumu **SUMMA** funkcija, pamatojoties uz **SUMMA** agregācija **TransportRecord** datu avots **GroupBy** veids.

![Summē datu avotu ER modeļa kartēšanas noformētājā.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Nākamajā attēlā parādīti rezultāti **Kopsummas** datu avota atkļūdošana.

![Kopējo datu avota atkļūdošanas rezultāti lapā Atkļūdošanas datu avoti.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [Atkļūdot izpildītā ER formāta datu avotus, lai analizētu datu plūsmu un transformāciju](er-debug-data-sources.md)
- [DATU APKOPOŠANAS datu avotu izmantošana Elektronisko pārskatu formātos](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
