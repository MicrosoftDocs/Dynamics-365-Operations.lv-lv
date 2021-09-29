---
title: ER formāta noformēšana, lai ģenerētos Excel dokumentus izdotu pa vairākām lapām
description: Šajā tēmā paskaidrots, kā noformēt Elektronisko atskaišu (ER) formātu, kas sadala Microsoft Excel ģenerēto dokumentu pa lapām.
author: NickSelin
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.openlocfilehash: ce29225c4bce24adc2abefc3d3d6f20774852af4
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488343"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>ER formāta noformēšana, lai ģenerētos Excel dokumentus izdotu pa vairākām lapām

[!include [banner](../includes/banner.md)]

Šajā tēmā parādīts, ka lietotājs ar sistēmas administratora vai elektroniskās ziņošanas funkcionālā konsultanta lomu var konfigurēt [Elektronisko atskaišu (ER)](general-electronic-reporting.md) formātu, lai ģenerētu izejošos dokumentus programmā Microsoft Excel un pārvaldītu dokumentu izdošanu pa lapām.

Šajā piemērām tiks pārveidots Microsoft nodrošinātais ER formāts, kuru izmanto vadības atskaites drukāšanās, kad ir [ģenerēts](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) Intrastat paziņojums. Šajā pārskatā var aplūkot ziņotās Intrastat transakcijas. Pārveidojumi ļaus izdot ģenerētās vadības atskaites pa lapām.

Šīs tēmas procedūras var pabeigt **DEMF** uzņēmumā. Kodēšana nav nepieciešama. Pirms sākšanas, lejupielādējiet un saglabājiet tālāk norādītos failus.

| Apraksts       | Faila nosaukums |
|-------------------|-----------| 
| Atskaites veidne 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Atskaites veidne 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>ER struktūras konfigurēšana

Izpildiet sadaļā [ER struktūras konfigurēšana](er-quick-start2-customize-report.md#ConfigureFramework) norādītās darbības, lai iestatītu ER parametru minimālo kopu. Šī iestatīšana jāpabeidz, pirms varat sākt izmantot ER struktūru, lai veidotu standarta ER formāta pielāgotu versiju.

## <a name="import-the-standard-er-format-configuration"></a>Standarta ER formāta konfigurācijas importēšana

Izpildiet sadaļā [Importēt standarta ER formāta konfigurāciju](er-quick-start2-customize-report.md#ImportERSolution1) norādītās darbības, lai pašreizējai instancei pievienotu Dynamics 365 Finance standarta ER konfigurācijas. **Intrastat atskaites** formāta konfigurācijas importa versija **1.9**. Bāzes **Intrastat modelis** konfigurācijas bāzes versija 1 tiek automātiski importēta no repozitorija.

## <a name="customize-the-standard-er-format"></a>Standarta ER formāta pielāgošana

### <a name="create-the-custom-er-format"></a>Pielāgotā ER formāta izveide

Šajā scenārijā jūs pārstāvat Litware, Inc., kurš pašlaik atlasīts kā aktīvais ER konfigurācijas nodrošinātājs. Ir jāizveidot jauna ER formāta konfigurācija, par bāzi izmantojot konfigurāciju **Intrastat atskaite**.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Intrastat modelis** un pēc tam atlasiet **Intrastat pārskats**. Litware, Inc. izmantos šīs ER formāta konfigurācijas versiju 1.9 kā pielāgotās versijas bāzi.
3. Atlasiet **Izveidot konfigurāciju**, lai atvērtu nolaižamo dialoglodziņu. Varat izmantot šo dialoglodziņu, lai izveidotu jaunu konfigurāciju pielāgotam maksājuma formātam.
4. Lauka grupā **Jauns** atlasiet opciju **Atvasināt no nosaukuma: Intrastat pārskats, Microsoft**.
5. Laukā **Nosaukums** ievadiet **Intrastat pārskats Litware**.
6. Atlasiet **Izveidot konfigurāciju**, lai izveidotu jaunu formātu.

Tiek izveidota ER formāta konfigurācijas **Intrastat pārskats Litware** versija 1.9.1. Šīs versijas [statuss](general-electronic-reporting.md#component-versioning) ir **Melnraksts** un to var rediģēt. Pielāgotā ER formāta pašreizējais saturs atbilst Microsoft nodrošinātā formāta saturam.

### <a name="make-the-custom-format-runnable"></a>Pielāgota formāta padarīšana par izpildāmu

Tagad, kad ir izveidota pielāgotā formāta pirmā versija un tai ir statuss **Melnraksts**, varat formātu palaist testēšanas nolūkos. Lai palaistu pārskatu, apstrādājiet kreditora maksājumu, izmantojot maksāšanas metodi, kas attiecas uz pielāgoto ER formātu. Pēc noklusējuma, izsaucot ER formātu no programmas, tiek [ņemtas vērā](general-electronic-reporting.md#component-versioning) tikai tās versijas, kuru statuss ir **Pabeigts** vai **Koplietots**. Šī darbība neļauj izmantot ER formātus, kuri nav pabeigti. Tomēr testējot, programmai var likt izmantot ER formāta versiju ar statusu **Melnraksts**. Šādā veidā var pielāgot pašreizējo formāta versiju, ja ir nepieciešamas kādas modifikācijas. Papildinformāciju skatiet sadaļā [Piemērojamība](electronic-reporting-destinations.md#applicability).

Lai izmantotu ER formāta melnraksta versiju, jums jāatzīmē ER formāts.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Dialoglodziņā **Lietotāja parametri** iestatiet opciju **Palaist iestatījumus** uz **Jā** un pēc tam atlasiet **Labi**.
4. Atlasiet **Rediģēt**, lai pašreizējo lapu varētu rediģēt pēc nepieciešamības.
5. Konfigurācijas koka skata kreisajā rūtī izvērsiet **Intrastat pārskats Litware**.
6. Iestatiet **Melnraksta palaišanas** opciju uz **Jā** un pēc tam atlasiet **Saglabāt**.

    ![Melnraksta opcijas palaišana lapā konfigurācijas.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Lai lietotu pielāgoto ER formātu, iestatiet ārējās tirdzniecības parametrus

Izpildiet šīs darbības, lai konfigurētu ārējās tirdzniecības parametrus, lai varat lietot pielāgoto formātu.

1. Dodieties uz **Nodokļi** \>**Iestatīšana** \>**Ārējā tirdzniecība** \>**Ārējās tirdzniecības parametri**.
2. Lapā **Ārējās tirdzniecības parametri**, kopsavilkuma cilnes **Elektroniskie pārskati** laukā **Failu formātu kartēšana** atlasiet **Intrastat pārskats Litware**.
3. Laukā **Pārskata formāta kartēšana** atlasiet **Intrastat pārskats Litware**.
4. Atlasiet **Saglabāt**.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>Konfigurējiet pielāgoto formātu, lai lietotu lejupielādēto pārskata veidni

### <a name="review-the-first-downloaded-excel-template"></a>Pārskatiet pirmo lejupielādēto Excel veidni

1. Excel darbvirsmas programmā atveriet **ERIntrastatReportDemo1.xlsx** veidnes failu, kuru lejupielādējāt iepriekš.
2. Pārbaudiet, vai veidne satur nosauktos diapazonus, lai izveidotu pārskata galvenes, informācijas un kājenes sadaļas ģenerētajos dokumentos.

    ![Excel pārskata 1 izkārtojums darbvirsmas programmā.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Aizstājiet pašreizējo Excel veidni pielāgotā ER formātā

Pielāgotajam ER formātam ir jāpievieno jauna Excel veidne.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, kreisās rūts konfigurāciju kokā izvērsiet **Intrastat modelis** \>**Intrastat pārskats**, un atlasiet konfigurāciju **Intrastat pārskats Litware**.
3. Atlasiet **Noformētājs**.
4. Lapā **Formāta noformētājs**, darbību rūtī atlasiet **Rādīt informāciju**.
5. Pārliecinieties, ka ir atlasīts saknes komponents **Intrastat Excel** un pēc tam darbību rūts cilnē **Importēt**, grupā **Importēt** atlasiet **Atjaunināt no Excel**.
6. Dialoglodziņā **Atjaunināt no Excel** atlasiet **Atjaunināt veidni**.
7. Dialoglodziņā **Atvērt** meklējiet un atlasiet failu **ERIntrastatReportDemo1.xlsx**, kuru iepriekš lejupielādējāt, pēc tam atlasiet **Atvērt**.
8. Atlasiet **Labi**.
9. Atlasiet **Saglabāt**.

![Noformējiet struktūru ER formāta noformētājā pēc jaunās Excel veidnes pievienošanas.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Mainiet datu saistīšanu, lai ģenerētajā pārskatā rādītu elementu aprakstus

1. Lapā **Formāta veidotājs** atlasiet cilni **Kartēšana**.
2. Izvērsiet **Intrastat**\>**Pārskatu rindas** un atlasiet komponentu **Preču kodu hierarhija**.
3. Atlasiet **Rediģēt formulu**.
4. Mainiet saistīšanas formulu no `@.CommodityCode` uz `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Atlasiet **Saglabāt**.

![Konfigurētā saistīšana, lai rādītu elementa aprakstu ER formāta noformētājā.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Intrastat paziņojuma vadības pārskata ģenerēšana

Vispirms pārliecinieties, ka **Intrastat** lapā ir pārskatam vajadzīgās Instrastat transakcijas.

![Transakcijas Intrastat lapā.](./media/er-paginate-excel-reports-transactions1.gif)

Pēc tam lietojiet pielāgoto ER formātu, lai ģenerētu Intrastat deklarācijas vadības pārskatu.

1. Dodieties uz **Nodokļi** \> **Deklarācijas** \> **Ārējā tirdzniecība** \> **Intrastat**.
2. Lapā **Intrastat**, darbību rūtī atlasiet **Izvades dati**\>**Pārskats**.
3. Dialoglodziņā **Intrastat pārskats** veiciet tālāk norādītās darbības, lai palaistu pārskatu:

    1. Iestatiet laukus **Datums no** un **Datums līdz**, lai pārskatā iekļautu konkrētas Intrastat transakcijas.
    2. Atlasiet opcijai **Ģenerēt failu** iestatījumu **Nē**.
    3. Atlasiet opcijai **Izveidot pārskatu** iestatījumu **Jā**.
    4. Atlasiet **Labi**.

4. Lejupielādējiet un saglabājiet ģenerēto dokumentu.
5. Atveriet dokumentu programmā Excel un to pārskatiet.

    ![Ģenerētais Excel dokuments darbvirsmas programmā.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Konfigurējiet pielāgoto formātu, lai ģenerētos dokumentus izdotu pa lapām

### <a name="review-the-second-downloaded-excel-template"></a>Pārskatiet otro lejupielādēto Excel veidni

1. Programmā Excel atveriet veidnes failu **ERIntrastatReportDemo2.xlsx**, kuru lejupielādējāt iepriekš.
2. Salīdziniet šo veidni ar veidni **ERIntrastatReportDemo1.xlsx** un pārbaudiet, vai tā satur vairākus jaunos Excel nosaukumus, lai izveidotu un aizpildītu lappušu sadaļas ģenerētajos dokumentos:

    - Ir pievienots diapazons **ReportPageHeader**, lai izveidotu lappušu galvenes.
    - Ir pievienots diapazons **ReportPageFooter**, lai izveidotu lappušu kājenes.
    - Šūna **ReportPageFooter\_PageLines** tiek konfigurēta, lai rādītu transakciju skaitu katrā lapā.
    - Šūna **ReportPageFooter\_PageAmount** tiek konfigurēta, lai rādītu kopējo transakciju skaitu katrā lapā.
    - Šūna **ReportPageFooter\_PageWeight** tiek konfigurēta, lai rādītu kopējo transakciju svaru katrā lapā.
    - Šūna **ReportPageFooter\_RunningCounterLines** tiek konfigurēta, lai rādītu transakciju palaidēja skaitītāju no pārskata sākuma līdz pašreizējai lappusei.
    - Šūna **ReportPageFooter\_RunningTotalAmount** tiek konfigurēta, lai rādītu apjomu, kas tiek kopumā palaists visām transakcijām no pārskata sākuma līdz pašreizējai lappusei.
    - Šūna **ReportPageFooter\_RunningTotalWeight** tiek konfigurēta, lai rādītu svaru, kas tiek kopumā palaists visām transakcijām no pārskata sākuma līdz pašreizējai lappusei.

    ![Excel pārskata 2 izkārtojums darbvirsmas programmā.](./media/er-paginate-excel-reports-template2a.gif)

    **CommodityCode** šūna šajā veidnē tiek konfigurēta, lai aplauztu šūnas tekstu. Tā kā transakcijas informācijas rinda ir konfigurēta tā, lai tā automātiski ietilptu rindas augstumā, visas rindas augstumam ir automātiski jāmainās, kad tiek aplauzts teksts šūnā **CommodityCode**.

    ![CommodityCode šūna tiek konfigurēta, lai aplauztu šūnas tekstu.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Atkārtojiet pašreizējās Excel veidnes aizstāšanu pielāgotajā ER formātā

1. Izpildiet šīs tēmas sadaļā [Pašreizējās Excel veidnes aizstāšana pielāgotajā ER formātā](#replace-template) norādītās darbības. Taču 7. darbībā atlasiet failu **ERIntrastatReportDemo2.xlsx**.
2. Lapā **Formāta veidotājs** izvērsiet **Intrastat**.
3. Nodēvējiet [Diapazona](er-fillable-excel.md#range-component) formāta komponentus, kuri ir pievienoti rediģējamajam ER formātam, lai sinhronizētu struktūru ar struktūru no piemērotās Excel veidnes:

    1. Atlasiet komponentu **Diapazons**, kas ir saistīts ar Excel nosaukumu **ReportPageHeader**.
    2. Cilnē **Formāts** laukā **Nosaukums** ievadiet **Ziņot par lappuses galveni**.
    3. Atlasiet komponentu **Diapazons**, kas ir saistīts ar Excel nosaukumu **ReportPageFooter**.
    4. Cilnē **Formāts** laukā **Nosaukums** ievadiet **Ziņot par lappuses kājeni**.

4. Atlasiet **Saglabāt**.

![Noformējiet struktūru ER formāta noformētājā pēc Excel veidnes aizstāšanas.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Nomainiet formāta struktūru, lai ieviestu dokumentu izdošanu pa lapām

1. Lapā **Formāta noformētājs** kreisās rūts formatēšanas kokā atlasiet saknes komponentu **Intrastat**.
2. Atlasiet **Pievienot**.
3. Dialoglodziņā **Pievienot** atlasiet **Excel** komponentu grupas komponentu [Lapa](er-fillable-excel.md#page-component).
4. Dialoglodziņā **Komponentu rekvizīti** laukā **Nosaukums** ievadiet **Pārskata lappuse**. Pēc tam atlasiet **Labi**.
5. Lai izmantotu komponentu **Pārskata lapas galvene** kā lapas galveni katrā ģenerētajā lapā, izpildiet tālāk norādītās darbības:

    1. Atlasiet komponentu **Pārskata lapas galvene** un pēc tam atlasiet **Griezt**.
    2. Atlasiet komponentu **Pārskata lapas galvene** un pēc tam atlasiet **Ielīmēt**.
    3. Izvērsiet **Pārskata lapa**.
    4. Lai uzspiestu **Lappuses** komponentu, lai šo diapazonu [uzskatītu](er-fillable-excel.md#page-component-structure) par lappuses galveni, atlasiet **Pārskata lappuses galvene** un pēc tam cilnes **Formatēt** laukā **Replicēšanas virziens** atlasiet **Bez replicēšanas**.

6. Lai ģenerēto dokumentu izdotu pa lapām tā, lai tiktu ņemtu vērā pārskata rindu saturs, izpildiet tālāk norādītās darbības:

    1. Atlasiet komponentu **Pārskata rindas** un pēc tam atlasiet **Griezt**.
    2. Atlasiet komponentu **Pārskata lapas galvene** un pēc tam atlasiet **Ielīmēt**.

7. Lai iekļautu pārskata kājeni pēc pārskata rindām, bet pirms pēdējās lapas kājenes, izpildiet tālāk noteiktās darbības:

    1. Atlasiet komponentu **Pārskata kājene** un pēc tam atlasiet **Griezt**.
    2. Atlasiet komponentu **Pārskata lapas galvene** un pēc tam atlasiet **Ielīmēt**.

8. Lai izmantotu komponentu **Pārskata kājene** kā lapas kājeni katrā ģenerētajā lapā, izpildiet tālāk norādītās darbības:

    1. Atlasiet komponentu **Pārskata lapas kājene** un pēc tam atlasiet **Griezt**.
    2. Atlasiet komponentu **Pārskata lapas galvene** un pēc tam atlasiet **Ielīmēt**.
    3. Lai uzspiestu **Lappuses** komponentu, lai šo diapazonu [uzskatītu](er-fillable-excel.md#page-component-structure) par lappuses kājeni, atlasiet **Pārskata lappuses kājene** un pēc tam cilnes **Formatēt** laukā **Replicēšanas virziens** atlasiet **Bez replicēšanas**.

![Noformējiet struktūru ER formāta noformētājā pēc dokumenta izdošanas pa lapām.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Pievienojiet datu avotus, lai aprēķinātu lapas kājeņu kopējo apjomu

Ir jākonfigurē jaunie datu avoti, lai aprēķinātu lapu kopskaitu, palaidēja skaitītāju un palaidēja kopējās vērtības un lai tās rādītu lappuses kājenes sadaļā. Šim nolūkam iesakām lietot [Datu kolekcijas](er-data-collection-data-sources.md) datu avotus.

1. Lapā **Formāta veidotājs** atlasiet cilni **Kartēšana**.
2. Vēlreiz atlasiet **Pievienot sakni**, tad veiciet šādas darbības:

    1. Dialoglodziņā **Pievienot datu avotu**, sadaļā **Vispārīgi** atlasiet **Tukšot konteineru**.
    2. Dialoglodziņā **Konteinera tukšošanas datu avota rekvizīti**, laukā **Nosaukums** ievadiet **Kopā**.
    3. Atlasiet **Labi**.

3. Atlasiet datu avotu **Kopā**, atlasiet **Pievienot** un pēc tam izpildiet tālāk norādītās darbības:

    1. Dialoglodziņā **Pievienot datu avotu**, sadaļā **Vispārīgi** atlasiet **Tukšot konteineru**.
    2. Dialoglodziņā **Konteinera tukšošanas datu avota rekvizīti**, laukā **Nosaukums** ievadiet **Lappuse**.
    3. Atlasiet **Labi**.

4. Vēlreiz atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Dialoglodziņā **Pievienot datu avotu**, sadaļā **Vispārīgi** atlasiet **Tukšot konteineru**.
    2. Dialoglodziņā **Konteinera tukšošanas datu avota rekvizīti**, laukā **Nosaukums** ievadiet **Palaišana**.
    3. Atlasiet **Labi**.

5. Atlasiet datu avotu **Total.Page**, atlasiet **Pievienot** un pēc tam izpildiet tālāk norādītās darbības:

    1. Dialoglodziņā **Pievienot datu avotu**, sadaļā **Funkcijas** atlasiet **Datu kolekcija**.
    2. Dialoglodziņā **Datu kolekcijas datu avota rekvizīti**, laukā **Nosaukums** ievadiet **Daudzums**.
    3. Laukā **Vienuma veids** atlasiet **Reāls**.
    4. Atlasiet opcijai **Apkopot visas vērtības** iestatījumu **Jā**.
    5. Atlasiet **Labi**.

6. Vēlreiz atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Dialoglodziņā **Pievienot datu avotu**, sadaļā **Funkcijas** atlasiet **Datu kolekcija**.
    2. Dialoglodziņā **Datu kolekcijas datu avota rekvizīti**, laukā **Nosaukums** ievadiet **Svars**.
    3. Laukā **Vienuma veids** atlasiet **Reāls**.
    4. Atlasiet opcijai **Apkopot visas vērtības** iestatījumu **Jā**.
    5. Atlasiet **Labi**.

7. Atlasiet datu avotu **Total.Running**, atlasiet **Pievienot** un pēc tam izpildiet tālāk norādītās darbības:

    1. Dialoglodziņā **Pievienot datu avotu**, sadaļā **Funkcijas** atlasiet **Datu kolekcija**.
    2. Dialoglodziņā **Datu kolekcijas datu avota rekvizīti**, laukā **Nosaukums** ievadiet **Daudzums**.
    3. Laukā **Vienuma veids** atlasiet **Reāls**.
    4. Atlasiet opcijas **Apkopot visas vērtības** lauku **Jā**.
    5. Atlasiet **Labi**.

8. Vēlreiz atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Dialoglodziņā **Pievienot datu avotu**, sadaļā **Funkcijas** atlasiet **Datu kolekcija**.
    2. Dialoglodziņā **Datu kolekcijas datu avota rekvizīti**, laukā **Nosaukums** ievadiet **Svars**.
    3. Laukā **Vienuma veids** atlasiet **Reāls**.
    4. Atlasiet opcijas **Apkopot visas vērtības** lauku **Jā**.
    5. Atlasiet **Labi**.

9. Vēlreiz atlasiet **Pievienot**, tad veiciet šādas darbības:

    1. Dialoglodziņā **Pievienot datu avotu**, sadaļā **Funkcijas** atlasiet **Datu kolekcija**.
    2. Dialoglodziņā **Datu kolekcijas datu avota rekvizīti**, laukā **Nosaukums** ievadiet **Rindas**.
    3. Laukā **Vienuma veids** atlasiet **Vesels skaitlis**.
    4. Atlasiet opcijas **Apkopot visas vērtības** lauku **Jā**.
    5. Atlasiet **Labi**.

10. Atlasiet **Saglabāt**.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Pievienojiet datu avotus, lai kontrolētu lappuses kājenes redzamību

Ja plānojat kontrolēt lappuses kājenes redzamību un neplānojat iekļaut kājeni beigu lappusē, ja tā satur transakcijas, konfigurējiet jaunu datu avotu, lai aprēķinātu vajadzīgo palaidēja skaitītāju.

1. Lapā **Formāta veidotājs** atlasiet cilni **Kartēšana**.
2. Atlasiet datu avotu **Total.Running**, atlasiet **Pievienot** un pēc tam izpildiet tālāk norādītās darbības.
3. Dialoglodziņā **Pievienot datu avotu**, sadaļā **Funkcijas** atlasiet **Datu kolekcija**.
4. Dialoglodziņā **Datu kolekcijas datu avota rekvizīti**, laukā **Nosaukums** ievadiet **Lines2**.
5. Laukā **Vienuma veids** atlasiet **Vesels skaitlis**.
6. Atlasiet opcijai **Apkopot visas vērtības** iestatījumu **Jā**.
7. Atlasiet **Labi**.
8. Atlasiet **Saglabāt**.

![ER formāta noformētājā pievienotie datu avoti.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Konfigurējiet saistījumus, lai apkopotu kopējās vērtības

1. Lapā **Formāta noformētājs** kreisās rūts formatēšanas kokā izvērsiet komponentu **Pārskata rindas** un atlasiet ligzdoto komponentu **Rēķina vērtība**.
2. Atlasiet **Rediģēt formulu**.
3. Mainiet saistīšanas formulu no `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` uz `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > Līdztekus daudzuma vērtības ievietošanai Excel šūnā katrai iterācijas transakcijai, šis saistījums apkopo vērtību datu kolekcijas datu avotā  **Total.Page.Amount**.

4. Atlasiet ligzdoto komponentu **Svars**.
5. Atlasiet **Rediģēt formulu**.
6. Mainiet saistīšanas formulu no `@.'$RoundedWeight'` uz `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > Līdztekus svara vērtības ievietošanai Excel šūnā katrai iterācijas transakcijai, šis saistījums apkopo vērtību datu kolekcijas datu avotā  **Total.Page.Weight**.

![Konfigurētie saistījumi kopējo vērtību apkopošanai ER formāta noformētājā.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Konfigurējiet saistījumus, lai aizpildītu lappuses kājenes kopējās vērtības

1. Lapā **Formāta noformētājs** formāta kokā izvērsiet komponentu **Pārskata lapas kājene** atlasiet ligzdoto **Diapazona** komponentu, kas atsaucas uz Excel šūnu **ReportPageFooter\_PageAmount** un pēc tam izpildiet tālāk norādītās darbības:

    1. Lapās rūts datu avotu kokā atlasiet vienumu **Total.Page.Amount.Sum()**.
    2. Atlasiet **Saistīt**.
    3. Atlasiet **Rediģēt formulu**.
    4. Atjauniniet formulu uz `Total.Page.Amount.Sum(false)`.

    > [!NOTE]
    > Ir jānorāda šīs funkcijas arguments kā **Aplams**, lai uzturētu pašreizējās lapas apkopotos datus, jo šie dati ir vajadzīgi, lai aprēķinātu summas palaidēja kopējo vērtību, kopējās rindas katrā lapā un rindu palaidēja skaitītāju.

2. Formāta kokā izvērsiet komponentu Pārskata lapas kājene atlasiet ligzdoto **Diapazona** komponentu, kas atsaucas uz Excel šūnu **ReportPageFooter\_PageWeight** un pēc tam izpildiet tālāk noradītās darbības.

    1. Lapās rūts datu avotu kokā atlasiet vienumu **Total.Page.Weight.Sum()**.
    2. Atlasiet **Saistīt**.
    3. Atlasiet **Rediģēt formulu**.
    4. Atjauniniet formulu uz `Total.Page.Weight.Sum(false)`.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Konfigurējiet saistījumus, lai lappuses palaišanas kopējās vērtības

1. Lapā **Formāta noformētājs** formāta kokā izvērsiet komponentu **Pārskata lapas kājene** atlasiet ligzdoto **Diapazona** komponentu, kas atsaucas uz Excel šūnu **ReportPageFooter\_RunningTotalAmount** un pēc tam izpildiet tālāk norādītās darbības:

    1. Lapās rūts datu avotu kokā atlasiet vienumu **Total.Running.Amount.Collect()**.
    2. Atlasiet **Saistīt**.
    3. Atlasiet **Rediģēt formulu**.
    4. Atjauniniet formulu uz `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`.

    > [!NOTE]
    > `Total.Running.Amount.Sum(false)` operands atgriež iepriekš apkopoto daudzuma palaidēja kopējo vērtību. `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` operands atgriež pašreizējās lapas kopējo daudzumu. Otrā operanda ligzdotās funkcijas arguments ir jānorāda kā **Patiess**, lai iestatītu `Total.Page.Amount` datu kolekciju, kolīdz šī vērtība ir ielikta `Total.Running.Amount` palaidēja kopējā kolekcijā. Norādītajam argumentam ir jāsāk apkopot nākamās lapas kopējā vērtība no 0 (nulles) vērtības.
    >
    > Tiek izsaukta funkcija `Total.Running.Amount.Sum(false)`, lai ievadītu daudzuma palaidēja kopējo vērtību pašreizējās lapas šūnā Excel **ReportPageFooter\_RunningTotalAmount**.

2. Formāta kokā izvērsiet komponentu Pārskata lapas kājene atlasiet ligzdoto **Diapazona** komponentu, kas atsaucas uz Excel šūnu **ReportPageFooter\_RunningTotalWeight** un pēc tam izpildiet tālāk noradītās darbības.

    1. Lapās rūts datu avotu kokā atlasiet vienumu **Total.Running.Weight.Collect()**.
    2. Atlasiet **Saistīt**.
    3. Atlasiet **Rediģēt formulu**.
    4. Atjauniniet formulu uz `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Konfigurējiet saistījumus, lai aizpildītu lapas palaidēja skaitītāju

1. Lapā **Formāta noformētājs** formāta kokā izvērsiet komponentu **Pārskata lapas kājene** atlasiet ligzdoto **Diapazona** komponentu, kas atsaucas uz Excel šūnu **ReportPageFooter\_RunningCounterLines** un pēc tam izpildiet tālāk norādītās darbības:
2. Atlasiet **Rediģēt formulu**.
3. Pievienojiet formulu `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))`.

    > [!NOTE]
    > Šī formula atgriež apkopoto daudzuma vērtību skaitu visam pārskatam. Šis skaitlis ir vienāds ar transakciju skaitu, kurām pašlaik tiek veikta iterācija. Vienlaikus formula apkopo atgriezto vērtību kolekcijā **Total.Running.Lines**.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Konfigurējiet saistījumus, lai aizpildītu lapas kājenes skaitītāju

1. Lapā **Formāta noformētājs** formāta kokā izvērsiet komponentu **Pārskata lapas kājene** atlasiet ligzdoto **Diapazona** komponentu, kas atsaucas uz Excel šūnu **ReportPageFooter\_PageLines** un pēc tam izpildiet tālāk norādītās darbības:
2. Atlasiet **Rediģēt formulu**.
3. Pievienojiet formulu `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)`.

    > [!NOTE]
    > Šī formula aprēķina pašreizējās lapas transakciju skaitu kā starpību starp transakciju skaitu, kuras tika apkopotas **Total.Page.Amount.Result** visam pārskatam un transakciju skaitu, kuras ir saglabātas šajā posmā **Total.Running.Lines.Sum**. Tā kā transakciju skaits pašreizējai lapai tiek glabāts **Total.Running.Lines** komponenta **Diapazons** komponenta saistījumā, kas atsaucas uz Excel šūnu **ReportPageFooter\_RunningCounterLines**, transakciju skaits pašreizējā lapā vēl nav iekļauts. Tāpēc šī starpība ir vienāda ar transakciju skaitu pašreizējā lapā.

![Konfigurētie saistījumi lapas kājenes skaitītāja aizpildīšanai ER formāta noformētājā.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Komponenta redzamības konfigurēšana

Varat mainīt lapas galvenes un kājenes redzamību konkrētā ģenerētā dokumenta lapā, lai slēptu šādus elementus:

- Lapas galvene ir pirmajā lapā, jo pārskata galvenē jau ir kolonnu nosaukumi
- Lapas galvene jebkurā lapā, kurai nav transakcijas, kura var parādīties pēdējā lapā
- Lapas kājene jebkurā lapā, kurai nav transakcijas, kura var parādīties pēdējā lapā

Lai mainītu redzamību, atjauniniet komponentu **Pārskata lapas galvene** un **Pārskata lapas kājene** rekvizītu **Iespējots**.

1. Lapā **Formāta noformētājs** kreisās rūts formatēšanas kokā izvērsiet komponentu **Pārskata lapa** un atlasiet ligzdoto komponentu **Pārskata lapas galvene** un pēc tam izpildiet tālāk norādītās darbības.

    1. Laukam **Iespējots** atlasiet **Rediģēt**.
    2. Lapā **Formulas veidotājs** laukā **Formula** ievadiet šādu izteiksmi:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Formāta kokā atlasiet ligzdoto komponentu **Pārskata lapas kājene** un pēc tam izpildiet tālāk norādītās darbības:

    1. Laukam **Iespējots** atlasiet **Rediģēt**.
    2. Lapā **Formulas veidotājs** laukā **Formula** ievadiet šādu izteiksmi:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > Konstrukcija `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` tiek izmantota, lai aprēķinātu transakciju skaitu pašreizējā lapā. `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` konstrukciju izmanto, lai pašreizējās lapas transakciju skaitu pievienotu kolekcijai, lai pareizi apstrādātu nākamās lapas kājenes redzamību.
    >
    > `Total.Running.Lines` kolekciju nevar izmantot atkārtoti, jo bāzes komponenta rekvizīts **Iespējots** tiek apstrādāts **pēc tam**, kad ligzdoto komponentu saistījumi ir apstrādāti. Kad rekvizīts **Iespējots** ir apstrādāts, kolekcija `Total.Running.Lines` jau tiek palielināta par pašreizējās lapas transakciju skaitu.

3. Atlasiet **Saglabāt**.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Intrastat paziņojuma vadības pārskata ģenerēšana (atjaunināts)

1. Pārliecinieties, ka **Intrastat** lapā ir 24 transakcijas. Atkārtojiet šīs tēmas iepriekšējā sadaļā [Intrastat deklarācijas vadības pārskata ģenerēšana](#generate-intrastat-control-report) minētās darbības, lai ģenerētu un pārskatītu vadības pārskatu.

    Visas transakcijas tiek rādītas pirmajā lapā. Lapu kopējais skaits un skaitītāji ir vienādi ar pārskatu kopējām vērtībām un skaitītājiem. Lapas galvenes diapazons tiek slēpts pirmajā lapā, jo pārskata galvenē jau ir kolonnu nosaukumi. Lapas galvene un kājene tiek slēpta otrajā lapā, jo lapa nesatur transakcijas.

    ![Ģenerētais Excel dokuments darbvirsmas programmā.](./media/er-paginate-excel-reports-document2.gif)

2. Atjauniniet abas transakcijas **Intrastat** lapā, mainot **Krājuma numura** kodu no **D00006** uz **L0010**. Ņemiet vērā, ka jaunā krājuma preces nosaukums **Aktīvā stereo skaļruņa pāris** ir garāks, nekā sākotnējā krājuma preces nosaukums **Standarta skaļrunis**. Šī situācija uzspiež teksta aplaušanu ģenerētā dokumenta atbilstošajā šūnā. Dokumenta sadalījums pa lapām un ar lapām saistītā summēšana un skaitīšana tagad būs atjaunināta. Atkārtojiet sadaļā [Intrastat deklarācijas vadības pārskata ģenerēšana](#generate-intrastat-control-report) minētās darbības, lai ģenerētu un pārskatītu vadības pārskatu.

    Pašlaik transakcijas tiek rādītas divās lapās, bet lappušu kopējās vērtības un skaitītāji tiek aprēķināti pareizi. Lapas galvenes diapazons tiek pareizi slēpts pirmajā lapā un ir redzami otrajā lapā. Lapas kājene ir redzama abās lapās, jo tās satur transakcijas.

    ![Atjauninātais ģenerētais Excel dokuments darbvirsmas programmā.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Vai ir veids, kādā atpazīt, kad pēdējo lapu apstrādāt Lappušu formāta komponents?

**Lappuses** komponents [neuzrāda](er-fillable-excel.md#page-component-limitations) informāciju par apstrādāto lapu skaitu un lapu kopējo skaitu ģenerētajā dokumentā. Taču jūs tāpat varat konfigurēt ER [formulas](er-formula-language.md), lai atpazītu pēdējo lappusi. Lūk, piemērs:

- Aprēķiniet kopējo jau apstrādāto transakciju skaitu, izmantojot komponentu **Pārskata lapas** komponentu. Šo aprēķinu varat veikt, lietojot formulu `COUNT(Total.Page.Amount.Result)`. 
- Aprēķiniet kopējo jau apstrādāto transakciju skaitu, kuras jāapstrādā, pamatojoties `model.CommodityRecord` saistījumā, kas tiek konfigurēts komponentam **Pārskata rindas**. Šo aprēķinu varat veikt, lietojot formulu `COUNT(model.CommodityRecord)`.
- Salīdziniet abus skaitļus, lai atpazītu pēdējo lapu. Kad abas vērtības ir vienādas, tiek ģenerēta pēdējā lapa.

> [!NOTE]
> Iesakām šo pieeju lietot tikai tad, ja komponenta **Pārskata rindas** rekvizīts **Iespējots** nesatur formulas, kuras varētu palaišanas laikā atgriezt vērtību [Nepatiess](er-formula-supported-data-types-primitive.md#boolean) dažiem no iterācijas [ierakstiem](er-formula-supported-data-types-composite.md#record) no saistītā [Ierakstu saraksta](er-formula-supported-data-types-composite.md#record-list).

## <a name="additional-resources"></a>Papildu resursi

- [Konfigurācijas noformēšana dokumentu ģenerēšanai Excel formātā](er-fillable-excel.md)
- [DATU APKOPOŠANAS datu avotu izmantošana Elektronisko pārskatu (ER) formātos](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
