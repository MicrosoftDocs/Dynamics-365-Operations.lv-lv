---
title: Izmantojiet SAVIENOJUMA datu avotus ER modeļu kartējumos, lai iegūtu datus no vairākām programmas tabulām
description: Šajā tēmā ir paskaidrots, kā elektroniskajos pārskatos (Electronic Reporting — ER) varat izmantot SAVIENOJUMA veida datu avotus.
author: NickSelin
ms.date: 04/26/2021
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
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: c9a06c048e98676e30a6652cad6634c2e13531d4ebc6d35f325f4c7153cd82ae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723217"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Izmantojiet SAVIENOJUMA datu avotus, lai iegūtu datus no vairākām programmas tabulām elektronisko pārskatu (ER) modeļu kartējumos

[!include[banner](../includes/banner.md)]

Konfigurējot elektronisko pārskatu (ER) modeļu kartējumus vai formātus, varat [pievienot](#review) vajadzīgos datu avotus **Savienojuma** veidam. Izstrādes laikā **Savienojuma** datu avots ir konfigurēts kā vairāku datu avotu kopa, no kuriem katrs atgriež ierakstu sarakstu. Katram datu avotam, izņemot pirmo, ir jādefinē nepieciešamie nosacījumi, lai pievienotos ierakstiem par pašreizējiem un iepriekšējiem datu avotiem. Izpildlaikā **Savienojuma** veida konfigurētais datu avots [atgriež](#executeERformat) vienu apvienotu ierakstu sarakstu, kas satur laukus no ligzdoto datu avotu ierakstiem.

Pašlaik tiek atbalstīti tālāk minētie savienojumu veidi.

- Ārējais (kreisais) savienojums:
    - Pievienojiet visus ierakstus no pirmā (kreisajā pusē) datu avota un pēc tam jebkuru atbilstību atbilstoši konfigurētajiem nosacījumu ierakstiem otrajā (labajā pusē) datu avotā.
- Iekšējais (labais) savienojums:
    - Pievienojiet tikai pirmā (kreisajā pusē) datu avota ierakstus un tikai otrā (labajā pusē) datu avota ierakstus, kas atbilst viens otram saskaņā ar konfigurētajiem nosacījumiem.

Konfigurētajā **Savienojuma** datu avotā, kad visu datu avotu veids ir **Tabulas ieraksti**, savienojuma datu avota izpildi var [veikt datu bāzes līmenī](#analyze), izmantojot vienu SQL izrakstu. Šis izraksts samazina datu bāzes izsaukumu skaitu, tādējādi uzlabojot modeļa kartēšanas veiktspēju. Pretējā gadījumā **Savienojuma datu** avota izpilde tiek veikta atmiņā.

> [!NOTE]
> Funkcijas **VALUEIN** izmantošana ER izteiksmēs, kas precizē nosacījumus ierakstu savienošanu savienojuma veida datu avotos, pagaidām vēl netiek atbalstīta. Papildinformāciju par šo funkciju skatiet lapā [Formulas izstrādātājs elektronisko pārskatu sniegšanā](general-electronic-reporting-formula-designer.md).

Lai iegūtu papildinformāciju par šo līdzekli, aizpildiet šajā tēmā sniegto piemēru.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Piemērs: izmantot SAVIENOJUMA datu avotus ER modeļu kartējumos

Tālākminētajās darbībās paskaidrots, kā sistēmas administrators vai elektronisko pārskatu noformētājs var konfigurēt elektronisko pārskatu (ER) modeļa kartēšanu, lai iegūtu datus no vairākām programmas tabulām uzreiz, izmantojot **Savienojuma** veida datu avotus nolūkā uzlabot datu piekļuves veiktspēju. Šīs darbības var veikt jebkuram uzņēmumam, kas izmanto Dynamics 365 Finance vai Regulatory Configuration Services (RCS).

### <a name="prerequisites"></a>Priekšnosacījumi

Lai izpildītu šīs tēmas piemērus, jums jābūt piekļuvei vienam no tālāk minētā atkarībā no tā, kāds pakalpojums tiek izmantots šo darbību pabeigšanai.

**Piekļuve Finance vienai no šīm lomām:**

- Elektroniskā pārskata izstrādātājs
- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

**Piekļuve pakalpojumam RCS vienai no šīm lomām:**

- Elektroniskā pārskata izstrādātājs
- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

Jums arī vispirms jāizpilda darbības, kas ir aprakstītas procedūrā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Iepriekš ir jāielādē un jāsaglabā šādi ER konfigurācijas failu paraugi:

| **Satura apraksts**  | **Faila nosaukums**   |
|--------------------------|-----------------|
| Parauga **ER datu modeļa** konfigurācijas fails, kas piemēriem tiek izmantots kā datu avots.| [Modelis, lai uzzinātu SAVIENOJUMA datu avotus.versija.1.1.xml](https://download.microsoft.com/download/5/c/1/5c1d8a57-6ebd-425b-bc5d-c71dde92c6af/ModeltolearnJOINdatasources.version.1.xml) |
| Parauga **ER modeļa kartēšanas** konfigurācijas fails, kas piemēriem īsteno ER datu modeli. | [Kartēšana, lai uzzinātu SAVIENOJUMA datu avotus.versija.1.1.xml](https://download.microsoft.com/download/9/2/f/92f339ca-41fc-4f5e-b458-6983c957d3dd/MappingtolearnJOINdatasources.version.1.1.xml)|
| Parauga **ER formāta** konfigurācijas fails. Šis fails apraksta datus, lai piemēriem aizpildītu ER formāta komponentu. | [Formāts, lai uzzinātu SAVIENOJUMA datu avotus.versija.1.1.xml](https://download.microsoft.com/download/f/f/8/ff8f1b48-14d0-4c73-9145-bcdf8b5265bc/FormattolearnJOINdatasources.version.1.1.xml) |

### <a name="activate-a-configurations-provider"></a>Konfigurācijas nodrošinātāja aktivizēšana

1. Piekļūstiet Finance vai RCS jūsu tīmekļa pārlūkprogrammas pirmajā sesijā.
2. Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.
3. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** pārliecinieties, vai ir uzskaitīts konfigurācijas nodrošinātājs parauga uzņēmumam [Litware, Inc.](http://www.litware.com) un vai tas ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas aprakstītas procedūrā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Elektronisko pārskatu darbvieta.](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>Importēt parauga ER konfigurācijas failus

1. Atlasiet **Pārskatu konfigurācijas**.
2. Importēt ER datu modeļa konfigurācijas failu.
    1. Atlasiet **Maiņa**.
    2. Atlasiet **Ielādēt no XML faila**.
    3. Atlasiet **Pārlūkot**, lai atrastu **Modeli, lai uzzinātu par SAVIENOŠANAS datu avotiem. versiju.1.1.xml** failu.
    4. Atlasiet **Labi**.
3. Importēt ER modeļa kartēšanas konfigurācijas failu.
    1. Atlasiet **Maiņa**.
    2. Atlasiet **Ielādēt no XML faila**.
    3. Atlasiet **Pārlūkot**, lai atrastu **Kartēšana, lai uzzinātu par SAVIENOŠANAS datu avotiem. versiju.1.1.xml** failu.
    4. Atlasiet **Labi**.
4. ER formāta konfigurācijas faila importēšana.
    1. Atlasiet **Maiņa**.
    2. Atlasiet **Ielādēt no XML faila**.
    3. Atlasiet **Pārlūkot**, lai atrastu **Formāts, lai uzzinātu par SAVIENOŠANAS datu avotiem. versiju.1.1.xml** failu.
    4. Atlasiet **Labi**.
5. Konfigurācijas kokā izvērsiet krājumu **Modelis, lai uzzinātu SAVIENOŠANAS datu avotu** , kā arī citus modeļa krājumus (ja pieejams).
6. Aplūkojiet ER konfigurāciju sarakstu kokā, kā arī versijas informāciju kopsavilkuma cilnē **Versijas** —– tie tiks izmantoti kā datu avots jūsu parauga pārskatam.

    ![Elektronisko atskaišu veidošanas konfigurāciju lapa.](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Ieslēgt izpildes izsekošanas opcijas

1. Atlasiet **KONFIGURĀCIJAS**.
2. Atlasiet **Lietotāja parametri**.
3. Iestatiet izpildes izsekošanas parametrus, kā parādīts ekrānuzņēmumā tālāk.

    ![Elektronisko pārskatu veidošanas lietotāja parametru lapa.](./media/GER-JoinDS-Parameters.PNG)

    Kad šie parametri ir ieslēgti, katrai importētā ER formāta faila izpildei tiks ģenerēta izpildes izsekošana. Izmantojot ģenerēto izpildes izsekošanas informāciju, var analizēt ER formāta un ER modeļa kartēšanas komponentu izpildi. Lai iegūtu papildinformāciju par ER izpildes izsekošanas līdzekli, apmeklējiet lapu [ER formāta izpildes izsekošana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md).

### <a name="review-er-model-mapping-part-1"></a>ER modeļa kartēšanas pārskatīšana (1. daļa)

Pārskatiet ER modeļa kartēšanas komponenta iestatījumus. Komponents ir konfigurēts, lai piekļūtu informācijai par ER konfigurāciju versijām, detalizētai informācijai par konfigurācijām un konfigurācijas nodrošinātājiem, neizmantojot **Savienošanas** datu avotu veidus.

1. Atlasiet konfiguricāciju **Kartēšana, lai uzzinātu SAVIENOJUMA datu avotus**.
2. Atlasiet **Noformētājs**, lai atvērtu kartējumu sarakstu.
3. Atlasiet **Noformētājs**, lai pārskatītu kartēšanas detalizētu informāciju.
4. Atlasiet **Rādīt detalizētu informāciju**.
5. Konfigurācijas kokā izvērsiet **Set1** un **Set1.Details** datu modeļa vienības.

    1. Saistīšanas **Detalizēta informācija: ierakstu saraksts = versijas** norāda, ka vienums **Set1.Details** ir saistīts ar **Versijas** datu avotu, kas atgriež tabulas **ERSolutionVersionTable** ierakstus. Katrs šīs tabulas ieraksts pārstāv vienu ER konfigurācijas versiju. Šīs tabulas saturs ir parādīts kopsavilkuma cilnē **Versijas** cilnē, kas atrodas lapā **Konfigurācijas**.
    2. Saistīšanas **ConfigurationVersion: virkne = @.PublicVersionNumber** nozīmē, ka katras ER konfigurācijas versijas publiskās versijas vērtība tiek ņemta no tabulas **ERSolutionVersionTable** lauka **PublicVersionNumber** un ievietota vienībā **ConfigurationVersion**.
    3. Saistīšana **ConfigurationTitle: virkne = @.'>Relations'.Solution.Name** norāda, ka ER konfigurācijas nosaukums ir ņemts no tabulas **ERSolutionTable** lauka **Nosaukums**, izmantojot daudzi pret vienu relāciju (**'>Relācijas'**) starp tabulām **ERSolutionVersionTable** un **ERSolutionTable**. Dotās programmas instances ER konfigurāciju nosaukumi tiek rādīti konfigurāciju kokā lapā **Konfigurācijas**.
    4. Saistīšana **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** nozīmē, ka konfigurācijas nodrošinātāja, kam pieder pašreizējā konfigurācija, nosaukums ir ņemts no tabulas **ERVendorTable** lauka **Nosaukums**, ko novērtē, izmantojot daudzi pret vienu relāciju starp tabulām **ERSolutionTable** un **ERVendorTable**. ER konfigurācijas nodrošinātāju nosaukumi tiek rādīti konfigurāciju kokā **Konfigurācijas** lapā katras konfigurācijas lapas galvenē. Visu ER konfigurācijas nodrošinātāju sarakstu var atrast tabulas lapā **Organizācijas administrēšana \> Elektroniskie pārskati \> Konfigurācijas nodrošinātājs**.

    ![Lietotāja modeļa kartējuma noformētāja lapa, saistīto datu modeļa vienumu saraksts.](./media/GER-JoinDS-Set1Review.PNG)

6. Konfigurācijas kokā izvērsiet **Set1.Summary** datu modeļa vienību.

    1. Saistījums **VersionsNumber: vesels skaitlis = VersionsSummary.aggregated.VersionsNumber** norāda, ka vienība **Set1.Summary.VersionsNumber** ir saistīta ar **Grupēt pēc** veida datu avota **VersionsSummary** apkopojuma lauku **VersionsNumber**, kas tika konfigurēts, lai atgrieztu tabulas **ERSolutionVersionTable** ierakstu skaitu, izmantojot datu avotu **Versijas**.

    ![Rediģēt parametru lapu 'Grupēt pēc'.](./media/GER-JoinDS-Set1GroupByReview.PNG)

7. Aizvērt lapu.

### <a name="review-er-model-mapping-part-2"></a><a name="review"></a> ER modeļa kartēšanas pārskatīšana (2. daļa)

Pārskatiet ER modeļa kartēšanas komponenta iestatījumus. Komponents ir konfigurēts, lai piekļūtu informācijai par ER konfigurāciju versijām, detalizētai informācijai par konfigurācijām un konfigurācijas nodrošinātājiem, izmantojot **Savienošanas** datu avota veidu.

1. Konfigurācijas kokā izvērsiet **Set2** un **Set2.Details** datu modeļa vienības. Saistījums **Detalizēta informācija: ierakstu saraksts = detalizēta informācija** norāda, ka vienība **Set2.Details** ir saistīta ar datu avotu **Detalizēta informācija**, kas ir konfigurēts kā **Savienojuma** veida datu avots.

    ![ER modeļa kartēšanas veidotāja lapa, kurā redzama paplašinātā 2. kopa: ieraksta datu modeļa vienumi.](./media/GER-JoinDS-Set2Review.PNG)

    **Savienojuma** datu avotu var pievienot, atlasot **Funkcijas\Savienojums** datu avotu:

    ![Lietotāja modeļa kartējuma noformētāja lapa, savienojuma datu avota tips.](./media/GER-JoinDS-AddJoinDS.PNG)

2. Atlasiet datu avotu **Detalizēta informācija**.
3. Atlasiet **Rediģēt** rūtī **Datu avoti**.
4. Atlasiet **Rediģēt savienojumu**.
5. Atlasiet **Rādīt detalizētu informāciju**.

    ![SAVIENOJUMA datu avota parametru lapa.](./media/GER-JoinDS-JoinDSEditor.PNG)

    Šī lapa tiek izmantota, lai izstrādātu nepieciešamo **Savienojuma veida** datu avotu. Izpildlaikā šis datu avots izveidos vienu saistītu ierakstu sarakstu no datu avotiem, kas atrodas režģī **Savienotais saraksts**. Ierakstu savienošana tiks sākta no datu avota **ConfigurationProviders**, kas atrodas režģī kā pirmais (kolonna **Veids** tam ir tukša). Visu citu datu avotu ieraksti pēc tam tiks pievienoti pamata datu avota ierakstiem, pamatojoties uz to secību šajā režģī. Visiem savienošanās datu avotiem jābūt konfigurētiem kā datu avotiem, kas ligzdoti mērķa datu avotā (`1Versions` datu avots ir ligzdots zem `1Configurations`; `1Configurations` datu avots ir ligzdots zem **ConfigurationProviders** ). Katram konfigurētajam datu avotam ir jāietver savienojuma nosacījumi. Šī konkrētā **Savienojuma** datu avotā ir definēti tālāk norādītie savienojumi.

    - Katrs **ConfigurationProviders** datu avota ieraksts (attiecas uz **ERVendorTable** tabulu) ir savienots ar tikai tādiem **1Konfigurācijas** ierakstiem (minēts tabulā **ERSolutionTable** ), kuriem ir tāda pati vērtība laukā **SolutionVendor** un **RecId**. **Iekšējā savienojuma** veids tiek lietots šim savienojumam, kā arī tālāk minētajiem nosacījumiem ierakstu saskaņošanai.

    FILTRS (Konfigurācijas, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Katrs **1Konfigurācijas** datu avota ieraksts (attiecas uz **ERSolutionTable** tabulu) ir savienots ar tikai tādiem **1Versijas** ierakstiem (minēts tabulā **ERSolutionVersionTable** ), kuriem ir tāda pati vērtība laukā **Solution** un **RecId**. **Iekšējā savienojuma** veids tiek lietots šim savienojumam, kā arī tālāk minētajiem nosacījumiem ierakstu saskaņošanai.

    FILTRS (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - Opcija **Izpilde** ir konfigurēta kā **Vaicājums**, kas nozīmē, ka šis savienojuma datu avots tiks izpildīts izpildlaikā datu bāzes līmenī kā tiešais SQL izsaukums.

    Lai pievienotos datu avotu ierakstiem, kas attēlo programmas tabulas, varat norādīt savienojuma nosacījumus, izmantojot citus lauku pārus, kas nav tie, kuri apraksta tos, kas pastāv AOT attiecībās starp šīm tabulām. Šo savienojuma veidu var konfigurēt, lai tas tiktu izpildīts arī datu bāzes līmenī.

6. Aizvērt lapu.
7. Atlasiet **Atcelt**.
8. Konfigurācijas kokā izvērsiet **Set2.Summary** datu modeļa vienību.

    - Saistījums **VersionsNumber: vesels skaitlis = DetailsSummary.aggregated.VersionsNumber** norāda, ka vienība **Set2.Summary.VersionsNumber** ir saistīta ar **Grupēt pēc** veida datu avota **DetailsSummary** apkopojuma lauku **VersionsNumber**, kas tika konfigurēts, lai atgrieztu **Savienojuma** veida **Detalizētas informācijas** savienoto ierakstu skaitu.
    - Vietas opcija **Izpilde** ir konfigurēta kā **Vaicājums**, kas nozīmē to, ka šis datu avots **Grupēt pēc** tiks izpildīts izpildlaikā kā tiešs SQL izsaukums datu bāzes līmenī. Tas ir iespējams, jo **Savienojuma** veida pamata datu avots **Detalizēta informācija** ir konfigurēts kā izpildīts datu bāzes līmenī.

    ![GROUPBY datu avota parametru lapa.](./media/GER-JoinDS-Set2GroupByReview.PNG)

9. Aizvērt lapu.
10. Atlasiet **Atcelt**.

### <a name="execute-er-format"></a><a name="executeERformat"></a> Izpildīt ER formātu

1. Piekļūstiet Finance vai RCS jūsu tīmekļa pārlūkprogrammas otrajā sesijā, izmantojot tos pašus akreditācijas datus un uzņēmumu kā pirmajā sesijā.
2. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
3. Izvērsiet konfiguricāciju **Modelis, lai uzzinātu SAVIENOJUMA datu avotus**.
4. Atlasiet konfiguricāciju **Formatēt, lai uzzinātu SAVIENOJUMA datu avotus**.
5. Atlasiet **Noformētājs**.
6. Atlasiet **Rādīt detalizētu informāciju**.
7. Atlasiet **Kartēšana**.
8. Atlasiet **Izvērst/Sakļaut**.

    Šis formāts ir izveidots, lai aizpildītu ģenerēto teksta failu ar jaunu rindu katrai ER konfigurācijas versijai (**Versijas** secība). Katrā ģenerētajā rindā tiks iekļauts konfigurācijas nodrošinātāja nosaukums, kam pieder pašreizējā konfigurācija, konfigurācijas nosaukums un konfigurācijas versija, kas atdalīta ar semikolu. Ģenerētā faila pēdējā rindā būs ietverts atrasto ER konfigurāciju versiju skaits (**Kopsavilkuma** secība).

    ![ER formāta veidotāja lapa, cilne Formāts.](./media/GER-JoinDS-FormatReview.PNG)

    Datu avoti **Dati** un **Kopsavilkums** tiek izmantoti, lai aizpildītu konfigurācijas versijas detalizētu informāciju ģenerētajā failā.

    - Informācija no datu modeļa **Set1** tiek izmantota, kad, palaižot ER formātu, lietotāja dialoga lapā izpildlaikā datu avotam **Atlasītājs** izvēlaties **Nē**.
    - Informācija no datu modeļa **Set2** tiek izmantota, kad lietotāja dialoga lapā izpildlaikā datu avotam **Atlasītājs** izvēlaties **Jā**.

    ![ER formāta veidotāja lapa, cilne Kartēšana.](./media/GER-JoinDS-FormatMappingReview.PNG)

9. Atlasiet **Izpildīt**.
10. Dialoga lapā laukā **Izmantot SAVIENOJUMA datu avotu** atlasiet **Nē**.
11. Atlasiet **Labi**.
12. Pārskatīt ģenerēto failu.

    ![Elektroniskā pārskata parametru ģenerētais fails, kas nelieto JOIN datu avotu.](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>Analizēt ER formāta izpildes izsekošanu

1. Pirmajā Finance vai RCS sesijā atlasiet **Izstrādātājs**.
2. Atlasiet **Veiktspējas izsekošana**.
3. Režģī **Veiktspējas izsekošana** atlasiet vislabāko ER formāta pēdējās izpildes izsekošanas ierakstu, kas izmantoja pašreizējo modeļa kartēšanas komponentu.
4. Atlasiet **Labi**.

    Izpildes statistika informē par dublētajiem zvaniem uz programmas tabulām.

    - **ERSolutionTable** ir izsaukts tik daudz reižu, cik ir konfigurācijas versijas ierakstu tabulā **ERSolutionVersionTable**, lai gan šādu izsaukumu skaitu varētu samazināt veiktspējas uzlabošanas laikā.
    - **ERVendorTable** ir izsaukts divreiz katram konfigurācijas versijas ierakstam, kas tika atklāts tabulā **ERSolutionVersionTable**, lai gan arī šādu izsaukumu skaitu varētu samazināt.

    ![Eexcution statistika ER Modeļu kartēšanas veidotāja lapā.](./media/GER-JoinDS-Set1Run2.PNG)

5. Aizvērt lapu.

### <a name="execute-er-format"></a>Izpildīt ER formātu

1. Pārslēdzieties uz jūsu tīmekļa pārlūkprogrammas cilni ar otro Finance vai RCS sesiju.
2. Atlasiet **Izpildīt**.
3. Dialoga lapā laukā **Izmantot SAVIENOJUMA datu avotu** atlasiet **Jā**.
4. Atlasiet **Labi**.
5. Pārskatīt ģenerēto failu.

    ![Elektroniskā pārskata parametru ģenerētais fails, kas lieto JOIN datu avotu.](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><a name="analyze"></a> Analizēt ER formāta izpildes izsekošanu

1. Pirmajā Finance vai RCS sesijā atlasiet **Izstrādātājs**.
2. Atlasiet **Veiktspējas izsekošana**.
3. Režģī **Veiktspējas izsekošana** atlasiet vislabāko ER formāta pēdējās izpildes izsekošanas ierakstu, kas izmantoja pašreizējo modeļa kartēšanas komponentu.
4. Atlasiet **Labi**.

    Statistika informē par tālāk norādīto.

    - Pieteikumu datu bāze ir vienreiz izsaukta, lai iegūtu ierakstus no tabulas **ERVendorTable**, **ERSolutionTable** un **ERSolutionVersionTable** nolūkā piekļūt nepieciešamajiem laukiem.

    ![Lietotāja modeļa kartējuma lapas veiktspējas statistikas dati.](./media/GER-JoinDS-Set2Run2.PNG)

    - Programmas datu bāze ir vienreiz izsaukta, lai aprēķinātu konfigurācijas versiju skaitu, lietojot savienojumus, kas tika konfigurēti datu avotā **Detalizēta informācija**.

    ![ER modeļu kartēšanas veidotāja lapa, kurā redzami programmas datu bāzes izsaukumi.](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="limitations"></a>Ierobežojumi

Kā redzams no piemēra šajā tēmā, **SAVIENOJUMA** datu avots var tikt izveidots no vairākiem datu avotiem, kas apraksta atsevišķas to ierakstu datu kopas, kas ir jāpievieno. Šos datu avotus jūs varat konfigurēt, izmantojot iebūvēto ER [FILTRA](er-functions-list-filter.md) funkciju. Konfigurējot datu avotu tā, ka tas tiek izsaukts ārpus **SAVIENOJUMA** datu avota, jūs varat izmantot uzņēmuma diapazonus kā daļu no nosacījuma datu atlasei. Sākotnējā **SAVIENOJUMA** datu avota ieviešana neatbalsta šāda veida datu avotus. Piemēram, kad izsaucat uz [FILTRA](er-functions-list-filter.md) balstītu datu avotu, kas ietilpst **SAVIENOJUMA** datu avota izpildes jomā, ja izsauktajam datu avotam ir uzņēmuma diapazoni kā daļa no nosacījuma datu atlasei, izveidojas izņēmums.

Microsoft Dynamics 365 Finance versijā 10.0.12 (2020. gada augusts) jūs varat izmantot uzņēmuma diapazonus kā daļu no nosacījuma datu atlasei uz [FILTRA](er-functions-list-filter.md) balstītos datu avotos, kas tiek izsaukti ar **SAVIENOJUMA** datu avota izpildes jomu. Programmas [vaicājuma](../dev-ref/xpp-library-objects.md#query-object-model) veidotāja ierobežojumu dēļ uzņēmumu diapazoni tiek atbalstīti tikai pirmajam **SAVIENOJUMA** datu avotam.

### <a name="example"></a>Paraugs

Piemēram, jums ir jāveic viens izsaukums programmas datu bāzei, lai iegūtu vairāku uzņēmumu ārējās tirdzniecības transakciju sarakstu un to krājumu vienības, kas minētas šajās transakcijās.

Šādā gadījumā tiek konfigurēti šādi artefakti jūsu ER modeļu kartēšanā:

- **Intrastat** saknes datu avots, kas pārstāv **Intrastat** tabulu.
- **Vienības** saknes datu avots, kas pārstāv **InventTable** tabulu.
- **Uzņēmumu** saknes datu avots, kas atgriež uzņēmumu sarakstu (**DEMF** un **GBSI** šajā piemērā), kur transakcijām jāpiekļūst. Uzņēmuma kods ir pieejams no lauka **Companies.Code**.
- **X1** saknes datu avots, kam ir izteiksme `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))`. Kā daļa no nosacījuma datu atlasei šī izteiksme ietver uzņēmuma diapazonu definīciju `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)`.
- **X2** datu avots kā ligzdots **X1** datu avota krājums. Tajā ir ietverta izteiksme `FILTER (Items, Items.ItemId = X1.ItemId)`.

Visbeidzot jūs varat konfigurēt **SAVIENOJUMA** datu avotu, kur **X1** ir pirmais datu avots un **X2** ir otrais datu avots. Jūs varat norādīt **Vaicājumu** kā **Izpildes** opciju, lai piespiestu ER palaist šo datu avotu datu bāzes līmenī kā tiešo SQL zvanu.

Kad tiek palaists konfigurētais datu avots, kamēr ER izpilde ir [izsekota](trace-execution-er-troubleshoot-perf.md), šāds paziņojums tiek parādīts ER modeļa kartēšanas izstrādātājā kā daļa no ER veiktspējas izsekošanas.

`SELECT ... FROM INTRASTAT T1 CROSS JOIN INVENTTABLE T2 WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF',N'GBSI') )) AND ((T2.PARTITION=?) AND (T2.ITEMID=T1.ITEMID AND (T2.DATAAREAID = T1.DATAAREAID) AND (T2.PARTITION = T1.PARTITION))) ORDER BY T1.DISPATCHID,T1.SEQNUM`

> [!NOTE]
> Kļūda rodas tad, ja tiek palaists **SAVIENOJUMA** datu avots, kas ir konfigurēts tā, lai tas ietvertu datu atlases nosacījumus, kuriem ir uzņēmuma diapazoni, kas paredzēti izpildāmā **SAVIENOJUMA** datu avota papildu datu avotiem.

## <a name="additional-resources"></a>Papildu resursi

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[ER formāta izpildes izsekošana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
