---
title: Secības elementu izpildes atlikšana elektronisko pārskatu formātos
description: Šajā rakstā skaidrots, kā atlikt secības elementa izpildi elektronisko pārskatu (ER) formātā.
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
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 5d4c5395c87c7bdc874f277a691e84081f68742d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880244"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>Secības elementu izpildes atlikšana ER formātos

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Pārskats

Elektronisko pārskatu ([ER)](general-electronic-reporting.md)[struktūras](tasks/er-format-configuration-2016-11.md) operāciju veidotāju varat izmantot, lai konfigurētu ER risinājuma formāta komponentu, kas tiek lietots izejošo dokumentu ģenerēšanai teksta formātā. Konfigurētā formāta komponenta hierarhisko struktūru veido dažādu tipu formātu elementi. Šos formāta elementus izmanto, lai izpildlaikā aizpildītu izveidotos dokumentus ar nepieciešamo informāciju. Pēc noklusējuma, palaižot ER formātu, formāta elementi tiek palaisti tādā pašā secībā, kādā tie atrodas formāta hierarhijā: pa vienam, no augšas uz leju. Tomēr noformēšanas laikā varat mainīt izpildes kārtību jebkuriem konfigurētā formāta komponenta secības elementiem.

Ieslēdzot konfigurētajā formātā secības formāta elementa <a name="DeferredSequenceExecution"></a>**Atliktās izpildes** opciju, varat atlikt (uz vēlāku laiku) šī elementa izpildi. Šādā gadījumā elements netiek palaists, kamēr nav palaisti visi citi tā pamatelementa elementi.

Lai uzzinātu vairāk par šo īpašību, pabeidziet šajā rakstā minēto piemēru.

## <a name="limitations"></a>Ierobežojumi

Opcija **Atliktā izpilde** tiek atbalstīta tikai tiem secības elementiem, kas ir konfigurēti ER formātam, kas tiek izmantots **izejošo** dokumentu ģenerēšanai teksta formātā.

Opcija **Atliktā izpilde** nav attiecināma uz secībām, kas ir konfigurētas kā apcirstas secības, kur maksimālais garums ir ierobežots.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Piemērs: Secības elementa izpildes atlikšana ER formātā

Tālāk aprakstītajās darbībās izskaidrots, kā lietotājs sistēmas administratora vai elektronisko pārskatu konsultanta [lomā](../sysadmin/tasks/assign-users-security-roles.md) var konfigurēt ER formātu, kas satur tādu secības elementu, kur izpildes secība formāta hierarhijā atšķiras no pasūtījuma.

Šos soļus var veikt **USMF** uzņēmumā Microsoft Dynamics 365 Finansēs.

### <a name="prerequisites"></a>Priekšnosacījumi

Lai izpildītu šo piemēru, jums programmas Finance uzņēmumā **USMF** jābūt piekļuvei vienai no tālak norādītajām lomām:

- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

Ja xml elementu [izpildes atliktais maksājuma dokuments vēl nav pabeigts,](er-defer-xml-element.md#Example)[lejupielādējiet šādas ER](general-electronic-reporting.md#Configuration) risinājuma parauga konfigurācijas.

| Satura apraksts            | Faila nosaukums |
|--------------------------------|-----------|
| ER datu modeļa konfigurācija    | [Modelis atlikto elementu apgūšanai.versija.1.xml](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| ER modeļa kartējuma konfigurācija | [Kartēšana atlikto elementu apgūšanai.versija.1.xml](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Pirms sākšanas ir jāielādē un jāsaglabā arī tālāk norādītā parauga ER risinājuma konfigurācija.

| Satura apraksts     |Faila nosaukums |
|-------------------------|----------|
| ER formāta konfigurācija | [Formāts atlikto secību apgūšanai.versija.1.xml](https://download.microsoft.com/download/0/f/5/0f55c341-8285-4d92-a46d-475d9a010927/Formattolearndeferredsequences.version.1.1.xml) |

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
    2. Atlasiet **Pārlūkot**, atrodiet un atlasiet failu **Formāts atlikto secību apgūšanai.1.1.xml** un pēc tam atlasiet **Labi**.

6. Konfigurāciju kokā izvērsiet **Modelis atlikto elementu apgūšanai**.
7. Konfigurāciju kokā pārskatiet importējamo ER konfigurāciju sarakstu.

    ![Konfigurāciju lapā importētās ER konfigurācijas.](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Konfigurācijas nodrošinātāja aktivizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** pārliecinieties, vai ir uzskaitīts [konfigurācijas nodrošinātājs](general-electronic-reporting.md#Provider) parauga uzņēmumam Litware, Inc. (`http://www.litware.com`) un vai tas ir atzīmēts kā aktīvs. Ja šis konfigurācijas nodrošinātājs nav uzskaitīts vai arī tas nav atzīmēts kā aktīvs, [izpildiet darbības, kas norādītas sadaļā Konfigurācijas nodrošinātāja izveide, un atzīmējiet to kā aktīvu](./tasks/er-configuration-provider-mark-it-active-2016-11.md) rakstu.

    ![Litware, Inc. parauga uzņēmums lokalizācijas konfigurāciju lapā.](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

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

        ![TotalSum apkopošanas lauks lapā Rediģēt "GroupBy" parametrus.](./media/ER-DeferredSequence-GroupByParameters.png)

9. Pārskats par to, kā konfigurētie datu avoti ir saistīti ar datu modeli un kā tie atklāj datus, kuriem atļauta piekļuve, lai padarītu tos pieejamus ER formātā

    - **Filtrētais** datu avots ir saistīts ar datu modeļa **Data.List** lauku.
    - Lauks **\$TaxAmount** no **Filtrēto** datu avota ir saistīts ar datu modeļa lauku **Data.List.Value**.
    - Lauks **TotalSum** no **Grupēto** datu avota ir saistīts ar datu modeļa lauku **Data.Summary.Total**.

    ![Modeļu kartēšanas veidotāja lapa.](./media/ER-DeferredSequence-ModelMapping.png)

10. Aizveriet lapas **Modeļu kartēšanas veidotājs** un **Modeļu kartējumi**.

### <a name="review-the-imported-format"></a>Pārskatīt importēto formātu

1. Lapā **Konfigurācijas**, konfigurācijas kokā atlasiet konfigurāciju **Formāts atlikto secību apgūšanai**.
2. Atlasiet **Veidotājs**, lai pārskatītu formāta informāciju.
3. Atlasiet **Rādīt detalizētu informāciju**.
4. Pārskatiet ER formāta komponentu iestatījumus, kas ir konfigurēti tā, lai ģenerētu izejošo dokumentu teksta formātā, kas ietver detalizētu informāciju par nodokļu darbībām:

    - Secības formāta elements **Pārskats\\Rindas** ir konfigurēts tā, lai aizpildītu izejošo dokumentu ar vienu rindu, kas tiek ģenerēta no ligzdotajiem secības elementiem (**Virsraksts**, **Ieraksts** un **Kopsavilkums**).

        ![Rindu secības formāta elements un ligzdotie elementi lapā Formāta veidotājs.](./media/ER-DeferredSequence-Format.png)

    - Secības formāta elements **Pārskats\\Rindas\\Virsraksts** ir konfigurēts tā, lai aizpildītu izejošo dokumentu ar vienu virsraksta rindu, kas parāda apstrādes sākšanas datumu un laiku.
    - Secības formāta elements **Pārskats \\Rindas\\Ieraksts** ir konfigurēts tā, lai aizpildītu izejošo dokumentu ar vienu rindu, kas parāda detalizētu informāciju par atsevišķām nodokļu darbībām. Šīs nodokļu darbības tiek atdalītas ar semikolu.

        ![Ierakstu secības formāta elements, kas izmanto semikolu kā norobežotāju.](./media/ER-DeferredSequence-Format1.png)

    - Secības formāta elements **Pārskats\\Rindas\\Kopsavilkums** ir konfigurēts tā, lai aizpildītu izejošo dokumentu ar vienu kopsavilkuma rindu, kas ietver nodokļu vērtību kopsummu no apstrādātām nodokļu darbībām.

4. Cilnē **Kartēšana** pārskatiet tālāk norādīto informāciju.

    - Lai izveidotu vienu rindu izejošajā dokumentā, elementam **Pārskats\\Rinda\\Virsraksts** nav jābūt saistītam ar datu avotu.
    - **Prefikss1** elements ģenerē **P1** simbolus, lai norādītu, ka pievienotā rinda ir pārskata virsraksta rinda.
    - Elements **IzpildesDatums Laiks** ģenerē datumu un laiku (tostarp milisekundēs), kad tiek pievienota virsraksta rinda.
    - Elements **Pārskats\\Rindas\\Ieraksts** ir piesaistīts sarakstam **model.Data.List**, lai ģenerētu vienu rindu katram saistītā saraksta ierakstam.
    - Elements **Prefikss2** ģenerē **P2** simbolus, lai norādītu, ka pievienotā rinda ir paredzēta nodokļu darbību informācijai.
    - Elements **TaxAmount** ir saistīts ar **model.Data.List.Value**, (kas tiek rādīta kā **\@.Vērtība** relatīvā ceļa skatā), lai ģenerētu pašreizējās nodokļu darbības nodokļu vērtību.
    - Elements **RunningTotal** ir vietturis nodokļu vērtību pašreizējai kopsummai. Pašlaik šim elementam nav izvades, jo tam nav konfigurēts ne saistījums, ne noklusētā vērtība.
    - Elements **ExecutionDateTime** ģenerē datumu un laiku (tostarp milisekundes), kad šajā pārskatā tiek apstrādāta pašreizējā darbība.
    - Lai izveidotu vienu rindu izejošajā dokumentā, elementam **Pārskats\\Rinda\\Kopsavilkums** nav jābūt saistītam ar datu avotu.
    - Elements **Prefikss3** ģenerē **P3** simbolus, lai norādītu, ka pievienotajā rindā ir iekļauta kopējā nodokļu vērtība.
    - Elements **TotalTaxAmount** ir saistīts ar **model.Data.Summary.Tota**, lai ģenerētu apstrādāto nodokļu darbību nodokļu vērtību summu.
    - Elements **IzpildesDatumsLaiks** ģenerē datumu un laiku (tostarp milisekundēs), kad tiek pievienota kopsavilkuma rinda.

    ![Cilne Kartēšana formāta veidotāja lapā.](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>Importētā formāta palaišana

1. Lapā **Formāta veidotājs** atlasiet **Palaist**.
2. Lejupielādējiet failu, ko piedāvā tīmekļa pārlūkprogramma, un atveriet to pārskatīšanai.

    ![Lejupielādētais atskaites parauga fails.](./media/ER-DeferredSequence-Run.png)

Ievērojiet, ka kopsavilkuma rinda 22 parāda apstrādāto darbību nodokļu vērtību summu. Tā kā formāts ir konfigurēts, lai šīs summas atgriešanai izmantotu saistījumu **cmodel.Data.Summary.Total**, summa tiek aprēķināta, izsaucot **GroupBy** tipa, kas izmanto modeļa kartēšanu, **Grupētā** datu avota *TotalSum* apkopojumu. Lai aprēķinātu šo apkopojumu, modeļa kartēšana atkārto visas darbības, kas ir atlasītas **Filtrētajā** datu avotā. Salīdzinot 21. un 22. rindas izpildes laikus, varat noteikt, ka summas aprēķins tika veikts 10 milisekundēs(ms). Salīdzinot 2. un 21. rindas izpildes laikus, varat noteikt, ka visu darījumu rindu ģenerēšana tika veikta 7 milisekundēs(ms). Tāpēc kopā bija nepieciešamas 17 ms.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>Formāta modificēšana, lai summēšanas pamatā būtu ģenerētā izvade

Ja darbību apjoms ir daudz plašāks par apjomu dotajā piemērā, summēšanas laiks var palielināties un izraisīt veiktspējas problēmas. Mainot formāta iestatījumu, var palīdzēt novērst šīs veiktspējas problēmas. Tā kā jūs piekļūstat nodokļu vērtībām, lai tās iekļautu ģenerētajā pārskatā, varat atkārtoti izmantot šo informāciju nodokļu vērtību summēšanai. Plašāku informāciju skatiet [Konfigurēt formātu, lai veiktu uzskaiti un summēšanu](./tasks/er-format-counting-summing-1.md).

1. Lapas **Formāta veidotājs** cilnē **Formāts**, formātu kokā atlasiet faila elementu **Pārskats**.
2. Atlasiet opcijai **Apkopot izvades datus** iestatījumu **Jā**. Tagad varat konfigurēt šo formātu, izmantojot esošā pārskata saturu kā datu avotu, kam var piekļūt, izmantojot iebūvētās ER funkcijas [Datu vākšanas](er-functions-category-data-collection.md) kategorijā.
3. Cilnē **Kartēšana** atlasiet secības elementu **Pārskats\\Rinda**.
4. Konfigurējiet izteiksmi **Apkopoto datu atslēgas nosaukums** kā `WsColumn`.
5. Konfigurējiet izteiksmi **Apkopoto datu atslēgas vērtība** kā `WsRow`.

    ![Rindu secības elements lapā Formāta veidotājs.](./media/ER-DeferredSequence-Format3.png)

6. Atlasiet ciparu elementu **Pārskats\\Rindas\\Ieraksts\\TaxAmount**.
7. Konfigurējiet izteiksmi **Apkopoto datu atslēgas nosaukums** kā `SummingAmountKey`.

    ![TaxAmount ciparu elements lapā Formāta veidotājs.](./media/ER-DeferredSequence-Format4.png)

    Varat apsvērt šo iestatījumu kā virtuālās darblapas izpildi, kur šūnas A1 vērtība tiek piesaistīta ar nodokļu summas vērtību no katras apstrādātās nodokļu darbības.

8. Atlasiet skaitlisko elementu **Pārskats\\Rinda\\Ieraksts\\RunningTotal** un pēc tam atlasiet **Rediģēt formulu**.
9. Konfigurējiet izteiksmi `SUMIF(SummingAmountKey, WsColumn, WsRow)`, izmantojot iebūvēto ER funkciju [SUMIF](er-functions-datacollection-sumif.md).
10. Atlasiet **Saglabāt**.

    ![SUMIF izteiksme.](./media/ER-DeferredSequence-FormulaDesigner.png)

11. Aizveriet lapu **Formāta veidotājs**.
12. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
13. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Lejupielādētais fails - summētās nodokļu vērtības.](./media/ER-DeferredSequence-Run1.png)

    21. rindā ir iekļauta nodokļu vērtību pašreizējā kopsumma, kas tiek aprēķināta visām apstrādātajām darbībām, izmantojot ģenerēto izvadi kā datu avotu. Šis datu avots sākas no pārskata sākuma un turpinās, aplūkojot pēdējo nodokļu darbību. 22. rindā ir iekļauta visu apstrādāto darbību nodokļu vērtību summa, kas tiek aprēķināta modeļa kartēšanā, izmantojot *GroupBy* tipa datu avotu. Ievērojiet, ka šīs vērtības ir vienādas. Tādēļ **GroupBy** vietā var izmantot uz izvadi balstītu summēšanu. Salīdzinot 2. un 21. rindas izpildes laikus, varat noteikt, ka visu darījumu rindu ģenerēšana un summēšana tika veikta 9 milisekundēs(ms). Tāpēc, ciktāl tas attiecas uz detalizēto rindu ģēnerēšānu un nodokļu vērtību summēšanu, modificētais formāts ir aptuveni divas reizes ātrāks nekā sākotnējais formāts.

14. Atlasiet skaitlisko elementu **Pārskats\\Rindas\\Kopsavilkums\\KopējāNodokļuSumma** un pēc tam atlasiet **Rediģēt formulu**.
15. Ievadiet esošās izteiksmes vietā izteiksmi `SUMIF(SummingAmountKey, WsColumn, WsRow)`.
16. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
17. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Lejupielādētais fails ar labotu formulu.](./media/ER-DeferredSequence-Run2.png)

    Ievērojiet, ka nodokļu vērtību pašreizējā kopsumma pēdējā darbību informācijas rindā tagad ir vienāda ar summu kopsavilkuma rindā.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Izvadē balstītas summēšanas vērtību izvietošana pārskata galvenē

Piemēram, varat modificēt formātu, ja pārskata galvenē jāuzrāda nodokļu vērtību summa.

1. Lapas **Formāta veidotājs** cilnē **Formāts** atlasiet secības elementu **Pārskats\\Rindas\\Kopsavilkums**.
2. Atlasiet **Pārvietot uz augšu**.
3. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
4. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Lejupielādētais fails summēšanai pārskata galvenē.](./media/ER-DeferredSequence-Run3.png)

    Ievērojiet, ka kopsavilkuma 2. rindā nodokļu vērtību summa tagad ir vienāda ar 0 (nulli), jo šī summa tagad tiek aprēķināta, pamatojoties uz ģenerēto izvadi. Kad tiek ģenerēta 2. rinda, ģenerētā izvade vēl neietver rindas, kurām ir detalizēta informācija par darbību. Varat konfigurēt šo formātu, lai atliktu secības elementu **Pārskats\\Rindas\\Kopsavilkums** izpildi, līdz visām nodokļu darbībām tiek palaists secības elements **Pārskats\\Rindas\\Ieraksts**.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>Kopsavilkuma secības izpildes atlikšana, lai tiktu izmantota aprēķinātā kopsumma

1. Lapas **Formāta veidotājs** cilnē **Formāts** atlasiet secības elementu **Pārskats\\Rindas\\Kopsavilkums**.
2. Atlasiet opcijai **Atliktā izpilde** iestatījumu **Jā**.

    ![Atlikta kopsavilkuma secības elementa izpildes opcija lapā Formāta veidotājs.](./media/ER-DeferredSequence-Format5.png)

3. Atlasiet **Saglabāt** un pēc tam atlasiet **Palaist**.
4. Lejupielādējiet un pārskatiet failu, ko piedāvā tīmekļa pārlūkprogramma.

    ![Lejupielādētais fails - atliktā izpilde.](./media/ER-DeferredSequence-Run4.png)

    Secības elements **Pārskats\\Rindas\\Kopsavilkums** tagad tiek palaists tikai pēc tam, kad ir palaisti visi pārējie krājumi, kas ligzdoti zem tā pamatelementa **Pārskats\\Rindas**. Tādēļ tas tiek palaists pēc secības elementa **Pārskats\\Rindas\\Ieraksts** palaišanas visām datu avota **model.Data.List** nodokļu darbībām. So faktu atklāj 1., 2. un 3. rindas un pēdējās 22. rindas izpildes laiki.

## <a name="additional-resources"></a>Papildu resursi

- [Konfigurēt formātu, lai veiktu uzskaiti un summēšanu](./tasks/er-format-counting-summing-1.md)
- [ER formāta izpildes izsekošana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md)
- [XML elementu izpildes atlikšana ER formātos](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
