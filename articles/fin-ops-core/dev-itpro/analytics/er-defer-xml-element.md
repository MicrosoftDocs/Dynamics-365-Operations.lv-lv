---
title: XML elementu izpildes atlikšana ER formātos
description: Šajā tēmā ir izskaidrots, kā atlikt XML izpildi elektroniskā pārskata (ER) formātā.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f89c671ae012907a4c3e07c09bdc867c1d67a101
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348073"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>XML elementu izpildes atlikšana ER formātos

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pārskats

Varat izmantot [Elektroniskās ziņošanas (ER)](general-electronic-reporting.md) struktūras operāciju veidotāju, lai [konfigurētu](./tasks/er-format-configuration-2016-11.md) tādu ER risinājuma [formāta komponentu](general-electronic-reporting.md#FormatComponentOutbound), kas tiek izmantots izejošo dokumentu ģenerēšanai XML formātā. Konfigurētā formāta komponenta hierarhisko struktūru veido dažādu tipu formātu elementi. Šos formāta elementus izmanto, lai izpildlaikā aizpildītu izveidotos dokumentus ar nepieciešamo informāciju. Pēc noklusējuma, palaižot ER formātu, formāta elementi tiek palaisti tādā pašā secībā, kādā tie atrodas formāta hierarhijā: pa vienam, no augšas uz leju. Tomēr noformēšanas laikā varat mainīt izpildes kārtību jebkuriem konfigurētā formāta komponenta XML elementiem.

Ieslēdzot konfigurētajā formātā XML elementa <a name="DeferredXmlElementExecution"></a>**Atliktās izpildes** opciju, varat atlikt (uz vēlāku laiku) šī elementa izpildi. Šādā gadījumā elements netiek palaists, kamēr nav palaisti visi citi tā pamatelementa elementi.

Lai iegūtu papildinformāciju par šo līdzekli, aizpildiet šajā tēmā sniegto piemēru.

## <a name="limitations"></a>Ierobežojumi

Opcija **Atliktā izpilde** tiek atbalstīta tikai tiem XML elementiem, kas ir konfigurēti ER formātam, kas tiek izmantots **izejošo** dokumentu ģenerēšanai XML formātā.

Opcija **Atliktā izpilde** tiek atbalstīta tikai tiem XML elementiem, kas atrodas tikai vienā citā XML elementā. Tāpēc tas nav attiecināms uz XML elementiem, kas atrodas citos formāta elementu tipos (piemēram, **XML secības** elementā).

Opcija **Atliktā izpilde** netiek atbalstīta tiem XML elementiem, kas atrodas formāta elementā **Standarta\\Fails**, ja opcijai **Sadalīt failu** atlasīts iestatījums **Jā**. Plašāku informāciju par to, kā sadalīt XML failus, skatiet [Ģenerēto XML failu sadalīšana, pamatojoties uz faila lielumu un satura daudzumu](er-split-files.md).

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>Piemērs: XML elementa izpildes atlikšana ER formātā

Tālāk aprakstītajās darbībās izskaidrots, kā lietotājs sistēmas administratora vai elektronisko pārskatu konsultanta [lomā](../sysadmin/tasks/assign-users-security-roles.md) var konfigurēt ER formātu, kas satur tādu XML elementu, kur izpildes secība formāta hierarhijā atšķiras no pasūtījuma.

Šīs darbības var veikt uzņēmumā **USMF** programmā Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Priekšnosacījumi

Lai izpildītu šo piemēru, jums programmas Finance uzņēmumā **USMF** jābūt piekļuvei vienai no tālak norādītajām lomām:

- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

Ja vēl neesat izpildījis piemēru tēmā [Secības elementu izpildes atlikšana ER formātos](er-defer-sequence-element.md#Example), lejupielādējiet tālāk norādītās parauga ER risinājumu [konfigurācijas](general-electronic-reporting.md#Configuration).

| Satura apraksts            | Faila nosaukums |
|--------------------------------|-----------|
| ER datu modeļa konfigurācija    | [Modelis atlikto elementu apgūšanai.versija.1.xml](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| ER modeļa kartējuma konfigurācija | [Kartēšana atlikto elementu apgūšanai.versija.1.xml](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Pirms sākšanas savā vietējā datorā jāielādē un jāsaglabā arī tālāk norādītā parauga ER risinājuma konfigurācija.

| Satura apraksts     | Faila nosaukums |
|-------------------------|-----------|
| ER formāta konfigurācija | [Formāts atlikto XML elementu apgūšanai.versija.1.xml](https://download.microsoft.com/download/4/7/8/478fa846-22e9-4fa0-89b1-d3aeae660067/FormattolearndeferredXMLelements.version.1.1.xml) |

### <a name="import-the-sample-er-configurations"></a>Parauga ER konfigurācijas failu importēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Ja lapā **Konfigurācijas** konfigurāciju kokā nav pieejama konfigurācija **Modelis atlikto elementu apgūšanai**, importējiet ER datu modeļa konfigurāciju:

    1. Atlasiet **Apmaiņa**, un pēc tam atlasiet **Ielādēt no XML faila**.
    2. Atlasiet **Pārlūkot**, atrodiet un atlasiet failu **Modelis atlikto elementu apgūšanai.1.xml** un pēc tam atlasiet **Labi**.

4. Ja konfigurāciju kokā nav pieejama konfigurācija **Kartēšana atlikto elementu apgūšanai** importējiet ER modeļa kartēšanas konfigurāciju:

    1. Atlasiet **Apmaiņa**, un pēc tam atlasiet **Ielādēt no XML faila**.
    2. Atlasiet **Pārlūkot**, atrodiet un atlasiet failu **Kartēšana atlikto elementu apgūšanai.1.1.xml** un pēc tam atlasiet **Labi**.

5. ER formāta konfigurācijas importēšana

    1. Atlasiet **Apmaiņa**, un pēc tam atlasiet **Ielādēt no XML faila**.
    2. Atlasiet **Pārlūkot**, atrodiet un atlasiet failu **Formāts atlikto XML elementu apgūšanai.1.1.xml** un pēc tam atlasiet **Labi**.

6. Konfigurāciju kokā izvērsiet **Modelis atlikto elementu apgūšanai**.
7. Konfigurāciju kokā pārskatiet importējamo ER konfigurāciju sarakstu.

    ![Konfigurāciju lapā importētās ER konfigurācijas.](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Konfigurāciju nodrošinātāja aktivizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** pārliecinieties, vai ir uzskaitīts [konfigurācijas nodrošinātājs](general-electronic-reporting.md#Provider) parauga uzņēmumam Litware, Inc. (`http://www.litware.com`) un vai tas ir atzīmēts kā aktīvs. Ja šis konfigurācijas nodrošinātājs nav uzskaitīts vai tas nav atzīmēts kā aktīvs, izpildiet darbības, kas aprakstītas tēmā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Litware, Inc. parauga uzņēmums lokalizācijas konfigurāciju lapā.](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Importētā modeļa kartējuma pārskatīšana

Pārskatiet ER modeļa kartējuma komponenta iestatījumus, kas ir konfigurēti, lai piekļūtu nodokļu darbībām, un atklājiet pieprasītos datus, kuriem atļauta piekļuve.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurāciju kokā izvērsiet vienumu **Modelis atlikto elementu apgūšanai**.
4. Atlasiet konfigurāciju **Kartēšana atlikto elementu apgūšanai**.
5. Atlasiet **Noformētājs**, lai atvērtu kartējumu sarakstu.
6. Atlasiet **Noformētājs**, lai pārskatītu kartēšanas detalizētu informāciju.
7. Atlasiet **Rādīt detalizētu informāciju**.
8. Pārskatiet datu avotus, kas konfigurēti, lai piekļūtu nodokļu darbībām:

    - **Transakciju** datu avots, kas pieder pie *Tabulas ierakstu* tipa, ir konfigurēts, lai piekļūtu **TaxTrans** pieteikumu tabulas ierakstiem.
    - **Dokumentu** datu avots, kas pieder pie *Aprēķinātā lauka* tipa, ir konfigurēts tā, lai atgrieztu vajadzīgos dokumentu kodus (**INV-10000349** un **INV-10000350**) kā ierakstu sarakstu.
    - **Filtrētais** datu avots, kas pieder pie *Aprēķinātā lauka* tipa, ir konfigurēts tā, lai no **Darbību** datu avota atlasītu tikai nepieciešamo dokumentu nodokļu darbības.
    - **\$TaxAmount** lauks, kas pieder pie *Aprēķinatā lauka* tipa, ir pievienots **Filtrēto** datu avotam, lai atklātu nodokļu vērtību, kurai ir pretēja zīme.
    - **Grupēto** datu avots, kas pieder pie *Grupēt pēc* tipa, ir konfigurēts tā, lai grupētu **Filtrēto** datu avota filtrētās nodokļu darbības.
    - **TotalSum** apkopojuma lauks no **Grupēto** datu avota ir konfigurēts tā, lai apkopotu **\$TaxAmount** lauku no **Filtrēto** datu avota visām šī datu avota filtrēto nodokļu darbībām.

        ![TotalSum apkopošanas lauks lapā Rediģēt "GroupBy" parametrus.](./media/ER-DeferredXml-GroupByParameters.png)

9. Pārskats par to, kā konfigurētie datu avoti ir saistīti ar datu modeli un kā tie atklāj datus, kuriem atļauta piekļuve, lai padarītu tos pieejamus ER formātā

    - **Filtrētais** datu avots ir saistīts ar datu modeļa **Data.List** lauku.
    - Lauks **\$TaxAmount** no **Filtrēto** datu avota ir saistīts ar datu modeļa lauku **Data.List.Value**.
    - Lauks **TotalSum** no **Grupēto** datu avota ir saistīts ar datu modeļa lauku **Data.Summary.Total**.

    ![Modeļu kartēšanas veidotāja lapa.](./media/ER-DeferredXml-ModelMapping.png)

10. Aizveriet lapas **Modeļu kartēšanas veidotājs** un **Modeļu kartējumi**.

### <a name="review-the-imported-format"></a>Pārskatīt importēto formātu

1. Lapā **Konfigurācijas**, konfigurācijas kokā atlasiet konfigurāciju **Formāts atlikto XML elementu apgūšanai**.
2. Atlasiet **Veidotājs**, lai pārskatītu formāta informāciju.
3. Atlasiet **Rādīt detalizētu informāciju**.
4. Pārskatiet ER formāta komponentu iestatījumus, kas ir konfigurēti tā, lai ģenerētu izejošo dokumentu XML formātā, kas ietver detalizētu informāciju par nodokļu darbībām:

    - XML elements **Pārskats\\Ziņojums** ir konfigurēts tā, lai aizpildītu izejošo dokumentu ar vienu mezglu, kas ietver ligzdotos XML elementus (**Virsraksts**, **Ieraksts** un **Kopsavilkums**).
    - XML elements **Pārskats\\Ziņojums\\Virsraksts** ir konfigurēts tā, lai aizpildītu izejošo dokumentu ar vienu virsraksta mezglu, kas parāda apstrādes sākšanas datumu un laiku.
    - XML formāta elements **Pārskats \\Ziņojums\\Ieraksts** ir konfigurēts tā, lai aizpildītu izejošo dokumentu ar vienu ieraksta mezglu, kas parāda detalizētu informāciju par vienu nodokļu darbību.
    - XML elements **Pārskats\\Ziņojums\\Kopsavilkums** ir konfigurēts tā, lai aizpildītu izejošo dokumentu ar vienu kopsavilkuma mezglu, kas ietver nodokļu vērtību kopsummu no apstrādātām nodokļu darbībām.

    ![Ziņojuma XML formāta elements un ligzdotie XML elementi lapā Formāta veidotājs.](./media/ER-DeferredXml-Format.png)

5. Cilnē **Kartēšana** pārskatiet tālāk norādīto informāciju.

    - Lai izveidotu vienu mezglu izejošajā dokumentā, elementam **Pārskats\\Ziņojums\\Virsraksts** nav jābūt saistītam ar datu avotu.
    - Atribūts **IzpildesDatumsLaiks** ģenerē datumu un laiku (tostarp milisekundēs), kad tiek pievienots virsraksta mezgls.
    - Elements **Pārskats\\Ziņojums\\Ieraksts** ir piesaistīts sarakstam **model.Data.List**, lai ģenerētu vienu ieraksta mezglu katram saistītā saraksta ierakstam.
    - Atribūts **TaxAmount** ir saistīts ar **model.Data.List.Value**, (kas tiek rādīta kā **\@.Vērtība** relatīvā ceļa skatā), lai ģenerētu pašreizējās nodokļu darbības nodokļu vērtību.
    - Artibūts **RunningTotal** ir vietturis nodokļu vērtību pašreizējai kopsummai. Pašlaik šim atribūtam nav izvades, jo tam nav konfigurēts ne saistījums, ne noklusētā vērtība.
    - Atribūts **ExecutionDateTime** ģenerē datumu un laiku (tostarp milisekundes), kad šajā pārskatā tiek apstrādāta pašreizējā darbība.
    - Lai izveidotu vienu mezglu izejošajā dokumentā, elementam **Pārskats\\Ziņojums\\Kopsavilkums** nav jābūt saistītam ar datu avotu.
    - Atribūts **TotalTaxAmount** ir saistīts ar **model.Data.Summary.Tota**, lai ģenerētu apstrādāto nodokļu darbību nodokļu vērtību summu.
    - Atribūts **IzpildesDatumsLaiks** ģenerē datumu un laiku (tostarp milisekundēs), kad tiek pievienots kopsavilkuma mezgls.

    ![Cilne Kartēšana formāta veidotāja lapā.](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>Importētā formāta palaišana

1. Lapā **Formāta veidotājs** atlasiet **Palaist**.
2. Lejupielādējiet failu, ko piedāvā tīmekļa pārlūkprogramma, un atveriet to pārskatīšanai.

    ![Importētā formāta lejupielādētais fails.](./media/ER-DeferredXml-Run.png)

Ievērojiet, ka kopsavilkuma mezgls parāda apstrādāto darbību nodokļu vērtību summu. Tā kā formāts ir konfigurēts, lai šīs summas atgriešanai izmantotu saistījumu **cmodel.Data.Summary.Total**, summa tiek aprēķināta, izsaucot **GroupBy** modeļa kartēšanas tipa **Grupētā** datu avota *TotalSum* apkopojumu. Lai aprēķinātu šo apkopojumu, modeļa kartēšana atkārto visas darbības, kas ir atlasītas **Filtrētajā** datu avotā. Salīdzinot kopsavilkuma mezgla un pēdējā ieraksta mezgla izpildes laikus, varat noteikt, ka summas aprēķins tika veikts 12 milisekundēs (MS). Salīdzinot pirmā un pēdējā ieraksta mezgla izpildes laikus, varat noteikt, ka visu ierakstu mezglu ģenerēšana tika veikta 9 milisekundēs(ms). Tāpēc kopā bija nepieciešamas 21 ms.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>Formāta modificēšana, lai aprēķināšanas pamatā būtu ģenerētā izvade

Ja darbības apjoms ir daudz plašāks par apjomu dotajā piemērā, aprēķināšanas laiks var palielināties un izraisīt veiktspējas problēmas. Mainot formāta iestatījumu, var palīdzēt novērst šīs veiktspējas problēmas. Tā kā jūs piekļūstat nodokļu vērtībām, lai tās iekļautu ģenerētajā pārskatā, varat atkārtoti izmantot šo informāciju nodokļu vērtību aprēķināšanai. Plašāku informāciju skatiet [Konfigurēt formātu, lai veiktu uzskaiti un summēšanu](./tasks/er-format-counting-summing-1.md).

1. Lapas **Formāta veidotājs** cilnē **Formāts**, formātu kokā atlasiet faila elementu **Pārskats**.
2. Atlasiet opcijai **Apkopot izvades datus** iestatījumu **Jā**. Tagad varat konfigurēt šo formātu, izmantojot ģēnerētā pārskata saturu kā datu avotu, kam var piekļūt, izmantojot iebūvētās ER funkcijas [Datu vākšanas](er-functions-category-data-collection.md) kategorijā.
3. Cilnē **Kartēšana** atlasiet XML elementu **Pārskats\\Ziņojums\\Ieraksts**.
4. Konfigurējiet izteiksmi **Apkopoto datu atslēgas nosaukums** kā `WsColumn`.
5. Konfigurējiet izteiksmi **Apkopoto datu atslēgas vērtība** kā `WsRow`.

    ![Ieraksta XML elements lapā Formāta veidotājs.](./media/ER-DeferredXml-Format3.png)

6. Atlasiet atribūtu **Pārskats\\Ziņojums\\Ieraksts\\TaxAmount**.
7. Konfigurējiet izteiksmi **Apkopoto datu atslēgas nosaukums** kā `SummingAmountKey`.

    ![TaxAmount atribūts lapā Formāta veidotājs.](./media/ER-DeferredXml-Format4.png)

    Varat apsvērt šo iestatījumu kā virtuālās darblapas izpildi, kur šūnas A1 vērtība tiek piesaistīta ar nodokļu summas vērtību no katras apstrādātās nodokļu darbības.

8. Atlasiet atribūtu **Pārskats\\Ziņojums\\Ieraksts\\RunningTotal** un pēc tam atlasiet **Rediģēt formulu**.
9. Konfigurējiet izteiksmi `SUMIF(SummingAmountKey, WsColumn, WsRow)`, izmantojot iebūvēto ER funkciju [SUMIF](er-functions-datacollection-sumif.md) un pēc tam atlasiet **Saglabāt**.

    ![SUMIF izteiksme.](./media/ER-DeferredXml-FormulaDesigner.png)

10. Aizveriet lapu **Formāta veidotājs**.
11. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
12. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Ģenerēts nodokļu vērtības saraksts ar tekošo kopsummu.](./media/ER-DeferredXml-Run1.png)

    Pēdējā ieraksta mezglā ir iekļauta nodokļu vērtību pašreizējā kopsumma, kas tiek aprēķināta visām apstrādātajām darbībām, izmantojot ģenerēto izvadi kā datu avotu. Šis datu avots sākas no pārskata sākuma un turpinās, aplūkojot pēdējo nodokļu darbību. Kopsavilkuma mezglā ir iekļauta visu apstrādāto darbību nodokļu vērtību summa, kas tiek aprēķināta modeļa kartēšanā, izmantojot *GroupBy* tipa datu avotu. Ievērojiet, ka šīs vērtības ir vienādas. Tādēļ **GroupBy** vietā var izmantot uz izvadi balstītu summēšanu. Salīdzinot pirmā ieraksta mezgla un kopsavilkuma mezgla izpildes laikus, varat noteikt, ka visu ierakstu mezglu ģenerēšana un summēšana tika veikta 11 milisekundēs(ms). Tāpēc, ciktāl tas attiecas uz ieraksta mezglu ģenerēšanu un nodokļu vērtību summēšanu, modificētais formāts ir aptuveni divas reizes ātrāks nekā sākotnējais formāts.

13. Atlasiet atribūtu **Pārskats\\Ziņojums\\Kopsavilkums\\TotalTaxAmount** un pēc tam atlasiet **Rediģēt formulu**.
14. Ievadiet esošās izteiksmes vietā izteiksmi `SUMIF(SummingAmountKey, WsColumn, WsRow)`.
15. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
16. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Ģenerēts nodokļu vērtību saraksts, izmantojot rediģēto formulu.](./media/ER-DeferredXml-Run2.png)

    Ievērojiet, ka nodokļu vērtību pašreizējā kopsumma pēdējā ieraksta mezglā tagad ir vienāda ar summu kopsavilkuma rindā.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Izvadē balstītas summēšanas vērtību izvietošana pārskata galvenē

Piemēram, varat modificēt formātu, ja pārskata galvenē jāuzrāda nodokļu vērtību summa.

1. Lapas **Formāta veidotājs** cilnē **Formāts** atlasiet XML elementu **Pārskats\\Ziņojums\\Kopsavilkums**.
2. Atlasiet **Pārvietot uz augšu**.
3. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
4. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Lejupielādētais pārskata virsraksta nodokļu vērtību fails.](./media/ER-DeferredXml-Run3.png)

    Ievērojiet, ka kopsavilkuma mezglā nodokļu vērtību summas tagad ir vienādas ar 0 (nulli), jo šī summa tagad tiek aprēķināta, pamatojoties uz ģenerēto izvadi. Kad tiek ģenerēts pirmais ieraskta mezgls, ģenerētā izvade vēl neietver ierakstu mezglus, kuriem ir detalizēta informācija par darbību. Varat konfigurēt šo formātu, lai atliktu elementa **Pārskats\\Ziņojums\\Kopsavilkums** izpildi, līdz visām nodokļu darbībām tiek palaists elements **Pārskats\\Ziņojums\\Ieraksts**.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>Kopsavilkuma XML elementa izpildes atlikšana, lai tiktu izmantota aprēķinātā kopsumma

1. Lapas **Formāta veidotājs** cilnē **Formāts** atlasiet XML elementu **Pārskats\\Ziņojums\\Kopsavilkums**.
2. Atlasiet opcijai **Atliktā izpilde** iestatījumu **Jā**.

    ![Atlikta kopsavilkuma XML elementa izpildes opcija lapā Formāta veidotājs.](./media/ER-DeferredXml-Format5.png)

3. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
4. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Lejupielādētais atliktās izpildes fails.](./media/ER-DeferredXml-Run4.png)

    Elements **Pārskats\\Ziņojumi\\Kopsavilkums** tagad tiek palaists tikai pēc tam, kad ir palaisti visi pārējie krājumi, kas ligzdoti zem tā pamatelementa **Pārskats\\Ziņojums**. Tādēļ tas tiek palaists pēc elementa **Pārskats\\Ziņojums\\Ieraksts** palaišanas visām datu avota **model.Data.List** nodokļu darbībām. Šo faktu atklāj pirmā un pēdējā ieraksta mezglu izpildes laiki, kā ari virsraksti un kopsavilkuma mezgli.

## <a name="additional-resources"></a>Papildu resursi

- [Konfigurēt formātu, lai veiktu uzskaiti un summēšanu](./tasks/er-format-counting-summing-1.md)
- [ER formāta izpildes izsekošana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md)
- [Secības elementu izpildes atlikšana ER formātos](er-defer-sequence-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
