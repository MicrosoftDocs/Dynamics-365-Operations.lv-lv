---
title: Izmantojiet SAVIENOJUMA datu avotus ER modeļu kartējumos, lai iegūtu datus no vairākām programmas tabulām
description: Šajā tēmā ir paskaidrots, kā elektroniskajos pārskatos (Electronic Reporting — ER) varat izmantot SAVIENOJUMA veida datu avotus.
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667958"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Izmantojiet SAVIENOJUMA datu avotus, lai iegūtu datus no vairākām programmas tabulām elektronisko pārskatu (ER) modeļu kartējumos

[!include[banner](../includes/banner.md)]

Konfigurējot elektronisko pārskatu (ER) modeļu kartējumus vai formātus, varat [pievienot](#review) vajadzīgos datu avotus **Savienojuma** veidam. Izstrādes laikā **Savienojuma** datu avots ir konfigurēts kā vairāku datu avotu kopa, no kuriem katrs atgriež ierakstu sarakstu. Katram datu avotam, izņemot pirmo, ir jādefinē nepieciešamie nosacījumi, lai pievienotos ierakstiem par pašreizējiem un iepriekšējiem datu avotiem. Izpildlaikā **Savienojuma** veida konfigurētais datu avots [atgriež](#executeERformat) vienu apvienotu ierakstu sarakstu, kas satur laukus no ligzdoto datu avotu ierakstiem.

Pašlaik tiek atbalstīti tālāk minētie savienojumu veidi.

- Ārējais (kreisais) savienojums:
    - Pievienojiet visus ierakstus no pirmā (kreisajā pusē) datu avota un pēc tam jebkuru atbilstību atbilstoši konfigurētajiem nosacījumu ierakstiem otrajā (labajā pusē) datu avotā.
- Iekšējais (labais) savienojums:
    - Pievienojiet tikai pirmā (kreisajā pusē) datu avota ierakstus un tikai otrā (labajā pusē) datu avota ierakstus, kas atbilst viens otram saskaņā ar konfigurētajiem nosacījumiem.

Konfigurētajā **Savienojuma** datu avotā, kad visu datu avotu veids ir **Tabulas ieraksti**, savienojuma datu avota izpildi var [veikt datu bāzes līmenī](#analyze), izmantojot vienu SQL izrakstu. Tas samazina datu bāzes izsaukumu skaitu, tādējādi uzlabojot modeļa kartēšanas veiktspēju. Pretējā gadījumā **Savienojuma datu** avota izpilde tiek veikta atmiņā.

> [!NOTE]
> Funkcijas **VALUEIN** izmantošana ER izteiksmēs, kas precizē nosacījumus ierakstu savienošanu savienojuma veida datu avotos, pagaidām vēl netiek atbalstīta. Papildinformāciju par šo funkciju skatiet lapā [Formulas izstrādātājs elektronisko pārskatu sniegšanā](general-electronic-reporting-formula-designer.md).

Lai iegūtu papildinformāciju par šo līdzekli, aizpildiet šajā tēmā sniegto piemēru.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Piemērs: izmantot SAVIENOJUMA datu avotus ER modeļu kartējumos

Tālākminētajās darbībās paskaidrots, kā sistēmas administrators vai elektronisko pārskatu noformētājs var konfigurēt elektronisko pārskatu (ER) modeļa kartēšanu, lai iegūtu datus no vairākām programmas tabulām uzreiz, izmantojot **Savienojuma** veida datu avotus nolūkā uzlabot datu piekļuves veiktspēju. Šīs darbības var veikt jebkuram uzņēmumam, kas izmanto Dynamics 365 Finance vai Regulatory Configuration Service (RCS).

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

Iepriekš jums ir arī jālejupielādē no [Microsoft lejupielādes centrs](https://go.microsoft.com/fwlink/?linkid=000000) un lokāli jāsaglabā tālāk minētie parauga ER konfigurācijas faili.

| **Satura apraksts**  | **Faila nosaukums**   |
|--------------------------|-----------------|
| Parauga **ER datu modeļa** konfigurācijas fails, kas piemēriem tiek izmantots kā datu avots.| [Modelis, lai uzzinātu SAVIENOJUMA datu avotus.versija.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Parauga **ER modeļa kartēšanas** konfigurācijas fails, kas piemēriem īsteno ER datu modeli. | [Kartēšana, lai uzzinātu SAVIENOJUMA datu avotus.versija.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Parauga **ER formāta** konfigurācijas fails. Šis fails apraksta datus, lai piemēriem aizpildītu ER formāta komponentu. | [Formāts, lai uzzinātu SAVIENOJUMA datu avotus.versija.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a>Konfigurācijas nodrošinātāja aktivizēšana

1. Piekļūstiet Finance vai RCS jūsu tīmekļa pārlūkprogrammas pirmajā sesijā.
2. Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.
3. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** pārliecinieties, vai ir uzskaitīts parauga uzņēmuma Litware, Inc. (http://www.litware.com) un vai tas ir atzīmēts kā **Aktīvs**. Ja neredzat šo konfigurācijas nodrošinātāju, izpildiet darbības, kas aprakstītas procedūrā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Elektronisko pārskatu darbvieta](./media/GER-JoinDS-ActiveProvider.PNG)

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
4.  ER formāta konfigurācijas faila importēšana.
    1. Atlasiet **Maiņa**.
    2. Atlasiet **Ielādēt no XML faila**.
    3. Atlasiet **Pārlūkot**, lai atrastu **Formāts, lai uzzinātu par SAVIENOŠANAS datu avotiem. versiju.1.1.xml** failu.
    4. Atlasiet **Labi**.
5.  Konfigurācijas kokā izvērsiet krājumu **Modelis, lai uzzinātu SAVIENOŠANAS datu avotu** , kā arī citus modeļa krājumus (ja pieejams).
6.  Aplūkojiet ER konfigurāciju sarakstu kokā, kā arī versijas informāciju kopsavilkuma cilnē **Versijas** —– tie tiks izmantoti kā datu avots jūsu parauga pārskatam.

    ![Elektronisko atskaišu veidošanas konfigurāciju lapa](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Ieslēgt izpildes izsekošanas opcijas
1.  Atlasiet **KONFIGURĀCIJAS**.
2.  Atlasiet **Lietotāja parametri**.
3.  Iestatiet izpildes izsekošanas parametrus, kā parādīts ekrānuzņēmumā tālāk.

    ![Elektronisko pārskatu veidošanas lietotāja parametru lapa](./media/GER-JoinDS-Parameters.PNG)

    Kad šie parametri ir ieslēgti, katrai importētā ER formāta faila izpildei tiks ģenerēta izpildes izsekošana. Izmantojot ģenerēto izpildes izsekošanas informāciju, var analizēt ER formāta un ER modeļa kartēšanas komponentu izpildi. Lai iegūtu papildinformāciju par ER izpildes izsekošanas līdzekli, apmeklējiet lapu [ER formāta izpildes izsekošana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md).

### <a name="review-er-model-mapping-part-1"></a>ER modeļa kartēšanas pārskatīšana (1. daļa)

Pārskatiet ER modeļa kartēšanas komponenta iestatījumus. Komponents ir konfigurēts, lai piekļūtu informācijai par ER konfigurāciju versijām, detalizētai informācijai par konfigurācijām un konfigurācijas nodrošinātājiem, neizmantojot **Savienošanas** datu avotu veidus.

1.  Atlasiet konfiguricāciju **Kartēšana, lai uzzinātu SAVIENOJUMA datu avotus**.
2.  Atlasiet **Noformētājs**, lai atvērtu kartējumu sarakstu.
3.  Atlasiet **Noformētājs**, lai pārskatītu kartēšanas detalizētu informāciju. 
4.  Atlasiet **Rādīt detalizētu informāciju**.
5.  Konfigurācijas kokā izvērsiet **Set1**  un **Set1.Details** datu modeļa vienības.

    1. Saistīšanas **Detalizēta informācija: ierakstu saraksts = versijas** norāda, ka vienums **Set1.Details** ir saistīts ar **Versijas** datu avotu, kas atgriež tabulas **ERSolutionVersionTable** ierakstus. Katrs šīs tabulas ieraksts pārstāv vienu ER konfigurācijas versiju. Šīs tabulas saturs ir parādīts kopsavilkuma cilnē **Versijas** cilnē, kas atrodas lapā **Konfigurācijas**.
    2. Saistīšanas **ConfigurationVersion: virkne = @.PublicVersionNumber** nozīmē, ka katras ER konfigurācijas versijas publiskās versijas vērtība tiek ņemta no tabulas  **ERSolutionVersionTable** lauka **PublicVersionNumber** un ievietota vienībā **ConfigurationVersion**.
    3. Saistīšana **ConfigurationTitle: virkne = @.'>Relations'.Solution.Name** norāda, ka ER konfigurācijas nosaukums ir ņemts no tabulas **ERSolutionTable** lauka **Nosaukums**, izmantojot daudzi pret vienu relāciju (**'>Relācijas'**) starp tabulām **ERSolutionVersionTable** un **ERSolutionTable**. Dotās programmas instances ER konfigurāciju nosaukumi tiek rādīti konfigurāciju kokā lapā **Konfigurācijas**.
    4. Saistīšana **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** nozīmē, ka konfigurācijas nodrošinātāja, kam pieder pašreizējā konfigurācija, nosaukums ir ņemts no tabulas **ERVendorTable** lauka **Nosaukums**, ko novērtē, izmantojot daudzi pret vienu relāciju starp tabulām **ERSolutionTable** un **ERVendorTable**. ER konfigurācijas nodrošinātāju nosaukumi tiek rādīti konfigurāciju kokā **Konfigurācijas** lapā katras konfigurācijas lapas galvenē. Visu ER konfigurācijas nodrošinātāju sarakstu var atrast tabulas lapā **Organizācijas administrēšana \> Elektroniskie pārskati\> Konfigurācijas nodrošinātājs**.

    ![ER modeļa kartēšanas noformētāja lapa](./media/GER-JoinDS-Set1Review.PNG)

6.  Konfigurācijas kokā izvērsiet **Set1.Summary** datu modeļa vienību.

    1. Saistījums **VersionsNumber: vesels skaitlis = VersionsSummary.aggregated.VersionsNumber** norāda, ka vienība **Set1.Summary.VersionsNumber** ir saistīta ar **Grupēt pēc** veida datu avota **VersionsSummary** apkopojuma lauku **VersionsNumber**, kas tika konfigurēts, lai atgrieztu tabulas **ERSolutionVersionTable** ierakstu skaitu, izmantojot datu avotu **Versijas**.

    ![GROUPBY datu avota parametru lapa](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  Aizvērt lapu.

### <a name="review"></a> ER modeļa kartēšanas pārskatīšana (2. daļa)

Pārskatiet ER modeļa kartēšanas komponenta iestatījumus. Komponents ir konfigurēts, lai piekļūtu informācijai par ER konfigurāciju versijām, detalizētai informācijai par konfigurācijām un konfigurācijas nodrošinātājiem, izmantojot **Savienošanas** datu avota veidu.

1.  Konfigurācijas kokā izvērsiet **Set2**  un **Set2.Details** datu modeļa vienības. Ņemiet vērā, ka saistījums **Detalizēta informācija: ierakstu saraksts = detalizēta informācija** norāda, ka vienība **Set2.Details** ir saistīta ar datu avotu **Detalizēta informācija**, kas ir konfigurēts kā **Savienojuma** veida datu avots.

    ![ER modeļa kartēšanas noformētāja lapa](./media/GER-JoinDS-Set2Review.PNG)

    **Savienojuma** datu avotu var pievienot, atlasot **Funkcijas\Savienojums** datu avotu:

    ![ER modeļa kartēšanas noformētāja lapa](./media/GER-JoinDS-AddJoinDS.PNG)

2.  Atlasiet datu avotu **Detalizēta informācija**.
3.  Atlasiet **Rediģēt** rūtī **Datu avoti**.
4.  Atlasiet **Rediģēt savienojumu**.
5.  Atlasiet **Rādīt detalizētu informāciju**.

    ![SAVIENOJUMA datu avota parametru lapa](./media/GER-JoinDS-JoinDSEditor.PNG)

    Šī lapa tiek izmantota, lai izstrādātu nepieciešamo **Savienojuma veida** datu avotu. Izpildlaikā šis datu avots izveidos vienu saistītu ierakstu sarakstu no datu avotiem, kas atrodas režģī **Savienotais saraksts**. Ierakstu savienošana tiks sākta no datu avota **ConfigurationProviders**, kas atrodas režģī kā pirmais (kolonna **Veids** tam ir tukša). Visu citu datu avotu ieraksti pēc tam tiks pievienoti pamata datu avota ierakstiem, pamatojoties uz to secību šajā režģī. Visiem savienošanās datu avotiem jābūt konfigurētiem kā datu avotiem, kas ligzdoti mērķa datu avotā (**1Versijas** datu avots ir ligzdots zem **1Konfigurācijas**; **1Konfigurācijas** datu avots ir ligzdots zem **ConfigurationProviders**). Katram konfigurētajam datu avotam ir jāietver savienojuma nosacījumi. Šī konkrētā **Savienojuma**datu avotā ir definēti tālāk norādītie savienojumi.

    - Katrs **ConfigurationProviders** datu avota ieraksts (attiecas uz **ERVendorTable** tabulu) ir savienots ar tikai tādiem **1Konfigurācijas** ierakstiem (minēts tabulā **ERSolutionTable**), kuriem ir tāda pati vērtība laukā **SolutionVendor** un **RecId**. **Iekšējā savienojuma** veids tiek lietots šim savienojumam, kā arī tālāk minētajiem nosacījumiem ierakstu saskaņošanai. 

    FILTRS (Konfigurācijas, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Katrs **1Konfigurācijas** datu avota ieraksts (attiecas uz **ERSolutionTable** tabulu) ir savienots ar tikai tādiem **1Versijas** ierakstiem (minēts tabulā **ERSolutionVersionTable**), kuriem ir tāda pati vērtība laukā **Solution** un **RecId**. **Iekšējā savienojuma** veids tiek lietots šim savienojumam, kā arī tālāk minētajiem nosacījumiem ierakstu saskaņošanai.

    FILTRS (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - Opcija **Izpilde** ir konfigurēta kā **Vaicājums**, kas nozīmē, ka šis savienojuma datu avots tiks izpildīts izpildlaikā datu bāzes līmenī kā tiešais SQL izsaukums.

    Ņemiet vērā, ka, lai pievienotos datu avotu ierakstiem, kas attēlo programmas tabulas, varat norādīt savienojuma nosacījumus, izmantojot citus lauku pārus, kas nav tie, kuri apraksta tos, kas pastāv AOT attiecībās starp šīm tabulām. Šo savienojuma veidu var konfigurēt, lai tas tiktu izpildīts arī datu bāzes līmenī.

6.  Aizvērt lapu.
7.  Atlasiet **Atcelt**.
8.  Konfigurācijas kokā izvērsiet **Set2.Summary** datu modeļa vienību.

    - Saistījums **VersionsNumber: vesels skaitlis = DetailsSummary.aggregated.VersionsNumber** norāda, ka vienība **Set2.Summary.VersionsNumber** ir saistīta ar **Grupēt pēc** veida datu avota **DetailsSummary** apkopojuma lauku **VersionsNumber**, kas tika konfigurēts, lai atgrieztu **Savienojuma** veida **Detalizētas informācijas** savienoto ierakstu skaitu.
    - Ņemiet vērā, ka vietas opcija **Izpilde** ir konfigurēta kā **Vaicājums**, kas nozīmē to, ka šis datu avots **Grupēt pēc** tiks izpildīts izpildlaikā kā tiešs SQL izsaukums datu bāzes līmenī. Tas ir iespējams, jo **Savienojuma** veida pamata datu avots **Detalizēta informācija** ir konfigurēts kā izpildīts datu bāzes līmenī.

    ![GROUPBY datu avota parametru lapa](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  Aizvērt lapu.
10. Atlasiet **Atcelt**.

### <a name="executeERformat"></a> Izpildīt ER formātu

1.  Piekļūstiet Finance vai RCS jūsu tīmekļa pārlūkprogrammas otrajā sesijā, izmantojot tos pašus akreditācijas datus un uzņēmumu kā pirmajā sesijā.
2.  Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
3.  Izvērsiet konfiguricāciju **Modelis, lai uzzinātu SAVIENOJUMA datu avotus**.
4.  Atlasiet konfiguricāciju **Formatēt, lai uzzinātu SAVIENOJUMA datu avotus**.
5.  Atlasiet **Noformētājs**.
6.  Atlasiet **Rādīt detalizētu informāciju**.
7.  Atlasīt **Kartēšana**.
8.  Atlasiet **Izvērst/Sakļaut**.

    Ņemiet vērā, ka šis formāts ir izveidots, lai aizpildītu ģenerēto teksta failu ar jaunu rindu katrai ER konfigurācijas versijai (**Versijas** secība). Katrā ģenerētajā rindā tiks iekļauts konfigurācijas nodrošinātāja nosaukums, kam pieder pašreizējā konfigurācija, konfigurācijas nosaukums un konfigurācijas versija, kas atdalīta ar semikolu. Ģenerētā faila pēdējā rindā būs ietverts atrasto ER konfigurāciju versiju skaits (**Kopsavilkuma** secība).

    ![ER formāta veidotāja lapa](./media/GER-JoinDS-FormatReview.PNG)

    Datu avoti **Dati** un **Kopsavilkums** tiek izmantoti, lai aizpildītu konfigurācijas versijas detalizētu informāciju ģenerētajā failā.

    - Informācija no datu modeļa **Set1** tiek izmantota, kad, palaižot ER formātu, lietotāja dialoga lapā izpildlaikā datu avotam **Atlasītājs** izvēlaties **Nē**.
    - Informācija no datu modeļa **Set2** tiek izmantota, kad lietotāja dialoga lapā izpildlaikā datu avotam **Atlasītājs** izvēlaties **Jā**.

    ![ER formāta veidotāja lapa](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  Atlasiet **Izpildīt**.
10. Dialoga lapā laukā **Izmantot SAVIENOJUMA datu avotu** atlasiet **Nē**.
11. Atlasiet **Labi**.
12. Pārskatīt ģenerēto failu.

    ![ER lietotāja dialoga lapa](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>Analizēt ER formāta izpildes izsekošanu

1.  Pirmajā Finance vai RCS sesijā atlasiet **Izstrādātājs**.
2.  Atlasiet **Veiktspējas izsekošana**.
3.  Režģī **Veiktspējas izsekošana** atlasiet vislabāko ER formāta pēdējās izpildes izsekošanas ierakstu, kas izmantoja pašreizējo modeļa kartēšanas komponentu.
4.  Atlasiet **Labi**.

    Ņemiet vērā, ka izpildes statistika informē par dublētajiem zvaniem uz programmas tabulām.

    - **ERSolutionTable** ir izsaukts tik daudz reižu, cik ir konfigurācijas versijas ierakstu tabulā **ERSolutionVersionTable**, lai gan šādu izsaukumu skaitu varētu samazināt veiktspējas uzlabošanas laikā.
    - **ERVendorTable** ir izsaukts divreiz katram konfigurācijas versijas ierakstam, kas tika atklāts tabulā **ERSolutionVersionTable**, lai gan arī šādu izsaukumu skaitu varētu samazināt.

    ![ER modeļa kartēšanas noformētāja lapa](./media/GER-JoinDS-Set1Run2.PNG)

5.  Aizvērt lapu.

### <a name="execute-er-format"></a>Izpildīt ER formātu

1.  Pārslēdzieties uz jūsu tīmekļa pārlūkprogrammas cilni ar otro Finance vai RCS sesiju.
2.  Atlasiet **Izpildīt**.
3.  Dialoga lapā laukā **Izmantot SAVIENOJUMA datu avotu** atlasiet **Jā**.
4.  Atlasiet **Labi**.
5.  Pārskatīt ģenerēto failu.

    ![ER lietotāja dialoga lapa](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> Analizēt ER formāta izpildes izsekošanu

1.  Pirmajā Finance vai RCS sesijā atlasiet **Izstrādātājs**.
2.  Atlasiet **Veiktspējas izsekošana**.
3.  Režģī **Veiktspējas izsekošana** atlasiet vislabāko ER formāta pēdējās izpildes izsekošanas ierakstu, kas izmantoja pašreizējo modeļa kartēšanas komponentu.
4.  Atlasiet **Labi**.

    Ievērojiet, ka izpildes statistika informē par tālāk minēto.

    - Pieteikumu datu bāze ir vienreiz izsaukta, lai iegūtu ierakstus no tabulas **ERVendorTable**, **ERSolutionTable** un **ERSolutionVersionTable** nolūkā piekļūt nepieciešamajiem laukiem.

    ![ER modeļa kartēšanas noformētāja lapa](./media/GER-JoinDS-Set2Run2.PNG)

    - Programmas datu bāze ir vienreiz izsaukta, lai aprēķinātu konfigurācijas versiju skaitu, lietojot savienojumus, kas tika konfigurēti datu avotā **Detalizēta informācija**.

    ![ER modeļa kartēšanas noformētāja lapa](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a>Papildu resursi

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[ER formāta izpildes izsekošana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md)
