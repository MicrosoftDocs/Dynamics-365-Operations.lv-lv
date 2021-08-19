---
title: Testēšanas ar elektroniskajiem pārskatiem automatizēšana
description: Šajā tēmā ir paskaidrots, kā varat lietot elektronisko pārskatu (Electronic reporting — ER) struktūras bāzlīnijas līdzekli, lai automatizētu dažu funkciju testēšanu programmā .
author: NickSelin
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: da69cc903197dbfae536c8494f126074c51aa77f9522d57f2673c97b1e682d9d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749804"
---
# <a name="automate-testing-with-electronic-reporting"></a>Testēšanas ar elektroniskiem pārskatiem automatizēšana

[!include[banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā varat lietot elektronisko pārskatu (Electronic reporting — ER) struktūru, lai automatizētu dažu funkciju testēšanu. Šīs tēmas piemērā ir parādīts, kā automatizēt kreditoru maksājumu apstrādes testēšanu.

Programma izmanto ER struktūru, lai izveidotu maksājumu failus un atbilstošos dokumentus kreditoru maksājumu apstrādes laikā. ER struktūra sastāv no datu modeļa, modeļa kartēšanas un formāta komponentiem, kas atbalsta maksājumu apstrādi dažādiem maksājumu veidiem un dokumentu izveidi dažādos formātos. Šos komponentus var lejupielādēt no Microsoft Dynamics Lifecycle Services (LCS) un importēt instancē.

Varat arī pielāgot katru Microsoft komponentu un izmantot to kā pamatu savam pielāgotajam komponentam. Izveidojot pielāgotu versiju, varat veikt izmaiņas, kas atbalsta noteiktas vajadzības. Piemēram, varat pielāgot ER datu modeli un ER modeļa kartēšanu, lai piekļūtu klientiem atbilstošiem programmas datiem, vai arī varat mainīt ER formātu, lai modificētu izveidotā dokumenta izkārtojumu.

Varat izmantot pielāgotus ER formātus, lai apstrādātu maksājumu failus, kas ģenerē kreditoru maksājumus, kā arī lai apstrādātu kontroles pārskatus. ER komponentiem tiek atbalstīta versiju izveide. Tādējādi Microsoft var nodrošināt atjauninātas ER risinājumu versijas kreditoru maksājumu apstrādei, un jūs varat automātiski sapludināt atjaunināto versiju ar jūsu pielāgoto komponentu, to pārbāzējot. Tomēr jums ir jāpārbauda pārbāzētā versija, lai pārliecinātos, ka tā darbojas, kā paredzēts.

ER datu modeļi un ER modeļu kartēšana ir kopīga daudziem ER formātiem, kas tiek izmantoti, lai apstrādātu dažādu veidu maksājumus un lai ģenerētu maksājumu dokumentus atbilstoši valsts/reģiona prasībām. Tāpēc ir ļoti vēlams automatizēt piemērotības lietotājam un integrācijas testēšanu, lai tā tiktu veikta automātiski vairākos uzņēmumos, taču lai tiktu arī ņemts vērā katra mērķa uzņēmuma valsts/reģiona konteksts, izmantotas dažādas datu kopas un citi parametri.

Lai iegūtu papildinformāciju par to, kā izveidot pielāgotu formāta versiju, kuras pamatā ir formāts, ko saņēmāt no konfigurācijas nodrošinātāja, skatiet tēmu [(ER) formāta jaunināšana, pieņemot šī formāta jaunu bāzes versiju](./tasks/er-upgrade-format.md)pamatversiju.

## <a name="key-concepts"></a>Galvenie principi

Funkcionālie prasmīgie lietotāji var autorēt piemērotības lietotājam un integrācijas testēšanu bez nepieciešamības rakstīt pirmkodu.

- Izmantojiet ER bāzlīnijas līdzekli, lai ģenerētos dokumentus salīdzinātu ar šablona kopijām. Papildinformāciju skatiet tēmā [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md).
- Izmantojiet uzdevuma reģistrētāju, lai ierakstītu testa gadījumus un iekļautu bāzlīnijas novērtējumu. Papildinformāciju skatiet tēmā [Uzdevuma reģistrētāja resursi](../user-interface/task-recorder.md).
- Grupējiet testa gadījumus nepieciešamajiem testa scenārijiem. Papildinformāciju skatiet sadaļā [Lietotāja akcepta testu izveidošana un automatizēšana](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - Izmantojiet biznesa procesu modelētāju (BPM) pakalpojumā LCS, lai izveidotu piemērotības lietotājam testus.
    - Izmantojiet BPM testu bibliotēkas, lai izveidotu testu plānu un testu komplektus Microsoft Azure DevOps Services (Azure DevOps).

Funkcionālie prasmīgie lietotāji var izpildīt piemērotības lietotājam un integrācijas testus.

- Izmantojiet Regression Suite Automation Tool (RSAT), lai izpildītu vēlamā testu komplekta testa gadījumus.
- Sniedziet pārskatu par testēšanas rezultātiem pakalpojumā Azure DevOps un izmantojiet šo pakalpojumu, lai izpētītu šos rezultātus.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu izpildīt šajā tēmā aprakstītos uzdevumus, ir jāizpilda tālāk norādītie priekšnosacījumi.

- Izvietojiet topoloģiju, kas atbalsta testu automatizāciju. Jums ir jābūt piekļuvei šīs topoloģijas instancei ar lomu **Sistēmas administrators**. Minētajā topoloģijā ir jāietver demonstrācijas dati, kas tiks izmantoti šajā piemērā. Papildinformāciju skatiet tēmā [Tādu topoloģiju izvietošana un lietošana, kuras atbalsta pastāvīgu būvēšanu un testu automatizēšanu](../perf-test/continuous-build-test-automation.md).
- Lai automātiski izpildītu piemērotības lietotājam un integrācijas testus, topoloģijā, kuru izmantojat, ir jāinstalē RSAT un atbilstoši jākonfigurē. Informāciju par to, kā instalēt un konfigurēt RSAT un konfigurēt to darbam ar Finance and Operations programmām un Azure DevOps, skatiet [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Pievērsiet uzmanību rīka izmantošanas priekšnosacījumiem. Nākamajā attēlā ir parādīts RSAT iestatījumu piemērs. Zilajā taisnstūrī ir redzami parametri, kas norāda piekļuvi Azure DevOps. Zaļajā taisnstūrī ir redzami parametri, kas norāda piekļuvi instancei.

    ![RSAT iestatījumi.](media/GER-Configure.png "RSAT iestatījumu dialoglodziņa ekrānuzņēmums")

- Lai kārtotu testa gadījumus komplektos veiksmīgai pareizas izpildes secības nodrošināšanai un lai varētu apkopot testu izpildes žurnālus turpmākai pārskatu sniegšanai un izmeklēšanai, jums ir nepieciešama piekļuve pakalpojumam Azure DevOps no izvietotās topoloģijas.
- Lai izpildītu šajā tēmā sniegto piemēru, mēs iesakām lejupielādēt failu [ER izmantošana RSAT testiem](https://go.microsoft.com/fwlink/?linkid=874684). Šajā zip failā ir tālāk norādītās uzdevumu vadlīnijas.

    | Saturs                                           | Faila nosaukums un atrašanās vieta |
    |---------------------------------------------------|------------------------|
    | Uzdevuma reģistrēšanas paraugs datu sagatavošanai testam | Prepare\\Recording.xml |
    | Uzdevuma reģistrēšanas paraugs kreditora maksājuma apstrādei   | Process\\Recording.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Kreditoru moduļa sagatavošana kreditoru maksājumu apstrādei

1. Pierakstieties savā instancē.
2. Lejupielādējiet tālāk norādītās ER konfigurācijas no LCS. Norādījumus skatiet tēmā [(ER) konfigurācijas importēšana no Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).

    - ER modeļa konfigurācija **Maksājuma modelis**
    - ER modeļa kartēšanas konfigurācija **Maksājumu modeļa kartēšana 1611**
    - ER formāta konfigurācija **BACS (UK)**

    ![Elektronisko atskaišu veidošanas konfigurācijas.](media/GER-Configurations.png "Elektronisko pārskatu lapu konfigurāciju ekrānuzņēmums")

3. Atlasiet **GBSI** demonstrācijas datu uzņēmumu, kam ir Apvienotās Karalistes valsts/reģiona konteksts.
4. Konfigurējiet kreditoru parametrus.

    1. Dodieties uz **Kreditori \> Maksājuma iestatījumi \> Maksāšanas metodes**.
    2. Atlasiet maksāšanas metodi **Elektroniski**.
    3. Konfigurējiet atlasīto maksāšanas metodi tā, lai tā izmantotu ER formātu **BACS (UK)**, ko lejupielādējāt iepriekš kreditora maksājuma apstrādei.

        1. Kopsavilkuma cilnē **Failu formāti** iestatiet opciju **Vispārīgs elektroniskās eksportēšanas formāts** uz **Jā**.
        2. Laukā **Eksportēšanas formāta konfigurācija** atlasiet **BACS (UK)**.

    ![Maksāšanas veidu lapa.](media/GER-APParameters.png "Maksājuma metodes lapas ekrānuzņēmums")

    > [!NOTE]
    > Ja jums ir atvasinātā versija šim ER formātam, kas tika izveidots pielāgojumu atbalstam, varat atlasīt šo konfigurāciju maksāšanas metodē **Elektroniski**.

5. Izveidojiet kreditoru maksājuma piemēru.

    1. Dodieties uz **Kreditori \> Maksājumi \> Maksājumu žurnāls**.
    2. Pārliecinieties, vai maksājumu žurnāls nav grāmatots.

        ![Maksājumu žurnāla lapa.](media/GER-APJournal.png "Maksājuma žurnāla lapas ekrānuzņēmums")

    3. Atlasiet **Rindas** un ievadiet rindu, kurā ir tālāk norādītā informācija.

        | Lauks               | Vērtības piemērs   |
        |---------------------|-----------------|
        | Kreditora nosaukums         | GB\_SI\_000001  |
        | Debetkarte               | 1,000.00        |
        | Valūta            | GBP             |
        | Korespondējošā konta tips | Banka            |
        | Korespondējošais konts      | GBSI OPER       |
        | Maksāšanas metode   | Elektronisks      |

    ![Kreditora maksājumu lapa.](media/GER-APJournalLines.png "Kreditora maksājumu lapas ekrānuzņēmums")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>ER struktūras sagatavošana kreditoru maksājumu apstrādes testam

### <a name="configure-er-parameters"></a>Konfigurējiet ER parametrus

1. Dodieties uz **Organizācijas administrēšana \> Elektroniskie pārskati \> Elektronisko pārskatu parametri**.
2. Cilnes **Pielikumi** laukā **Bāzlīnija** atlasiet vienumu **Fails** kā dokumenta veidu, ko dokumentu pārvaldības (DM) struktūra izmanto, lai saglabātu dokumentus, kas ir saistīti ar bāzlīnijas līdzekli kā DM pielikumi.

    ![Elektronisko pārskatu veidošanas parametru lapa.](media/GER-ERParameters.png "Elektronisko pārskatu parametru lapas ekrānuzņēmums")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Ar kreditoru maksājumiem saistīto dokumentu bāzlīniju kopiju ģenerēšana

1. Dodieties uz **Kreditori \> Maksājumi \> Maksājumu žurnāls**.
2. Atlasiet **Rindas**.
3. Atlasiet **Ģenerēt maksājumus**.
4. Atlasiet maksāšanas metodi **Elektroniski**.
5. Atlasiet **GBSI OPER** bankas kontu.
6. Iestatiet opciju **Drukāt kontroles pārskatu** uz **Jā**.
7. Lejupielādējiet ģenerēto izvadi kā zip failu.
8. Atveriet lejupielādēto failu.
9. No lejupielādētā faila izvelciet tālāk norādītos failus.

    - **Fails**, maksājuma fails teksta formātā
    - **ERVendOutPaymControlReport** kontroles pārskata fails XLSX formātā

    ![Izgūtie faili.](media/GER-APJournalProcessed.png "Programmā Windows explorer izvilkto failu nosaukumu ekrānuzņēmums")

### <a name="turn-on-the-er-baseline-feature"></a>ER bāzlīnijas līdzekļa ieslēgšana

1. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
2. Darbību rūts cilnē **Konfigurācijas** atlasiet **Lietotāja parametri**.
3. Atlasiet opcijai **Palaist atkļūdošanas režīmā** iestatījumu **Jā**.

Ieslēdzot parametru **Palaist atkļūdošanas režīmā**, jūs liksiet ER struktūrai piespiedu kārtā veikt tālāk norādītās darbības pēc jebkura ER formāta izpildes, kas ģenerē izejošos dokumentus.

1. Noteikt, vai kādam no izpildītā ER formāta komponentiem tika konfigurēta bāzlīnija.
2. Noteikt, vai katra konfigurētā bāzlīnija ir spēkā pašreizējos apstākļos (pierakstītā uzņēmuma kods, ģenerētās izvades faila nosaukums un faila nosaukuma paplašinājums u. c.).
3. Katrai piemērojamai bāzlīnijai veiciet tālāk norādītās darbības.

    1. Salīdziniet izvadi, kas ir ģenerēta ER formāta izpildes laikā ar atbilstošo bāzlīniju.
    2. Saglabājiet salīdzinājuma rezultātus ER konfigurāciju atkļūdošanas žurnālā.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>ER bāzlīniju konfigurācija kreditoru maksājumu apstrādei

1. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
2. Atlasiet **Bāzlīnijas**.
3. Atlasiet **Jauns**.
4. Laukā **Atsauce** atlasiet formātu **BACS (UK)**.
5. Atlasiet **Pielikumi**.
6. Pievienojiet jaunu bāzlīniju kreditora maksājuma failam, kā aprakstīts tālāk.

    1. Atlasiet **Jauns**.
    2. Laukā **Veids** atlasiet vienuma **Fails** DM dokumenta veidu, ko konfigurējāt ER parametros, lai saglabātu bāzlīnijas artefaktus.
    3. Pārlūkojiet, lai atlasītu lokāli saglabāto vienuma **Fails** maksājuma failu teksta formātā.
    4. Laukā **Apraksts** ievadiet **Maksājuma txt fails**.

7. Pievienojiet jaunu bāzlīniju kreditora maksājuma kontroles pārskatam, kā aprakstīts tālāk.

    1. Atlasiet **Jauns**.
    2. Laukā **Veids** atlasiet vienuma **Fails** DM dokumenta veidu, ko konfigurējāt ER parametros, lai saglabātu bāzlīnijas artefaktus.
    3. Pārlūkojiet, lai atlasītu lokāli saglabāto kontroles pārskata failu **ERVendOutPaymControlReport** XLSX formātā.
    4. Laukā **Apraksts** ievadiet **Maksājuma XLSX kontroles pārskats**.

    ![Bāzlīnijas kreditora maksājuma kontroles pārskatam.](media/GER-BaselineAttachments.png "Konfigurācijas lapas ekrānuzņēmums ar atlasītu maksājumu XLSX kontroles pārskatu")

8. Aizvērt lapu.
9. Kopsavilkuma cilnē **Bāzlīnijas** atlasiet **Jauna**, lai konfigurētu maksājuma faila bāzlīniju.

    1. Nosauciet rindu par **Maksājuma faila bāzlīnijas iestatījumi**.
    2. Laukā **Faila komponenta nosaukums** atlasiet **Fails**, lai lietotu šo bāzlīniju ER formāta izvadei, kas ģenerē maksājuma failu BACS (UK) teksta formātā.
    3. Laukā **Uzņēmumi** atlasiet **GBSI**, lai piemērotu šo bāzlīniju, kad GBSI uzņēmumā tiek palaists **BACS (UK)** ER formāts.
    4. Laukā **Faila nosaukuma maska** ievadiet **\*.TXT**, lai izmantotu šo bāzlīniju tikai **faila** formāta komponenta izvadēm ar faila nosaukuma paplašinājumu **.txt**.
    5. Laukā **Bāzlīnija** atlasiet **Maksājuma TXT fails**, lai šo bāzlīniju izmantotu salīdzinājumam ar ģenerēto izvadi.

10. Atlasiet **Jauna**, lai konfigurētu bāzlīniju kontroles pārskatam.

    1. Nosauciet rindu par **Kontroles pārskata bāzlīnijas iestatījumi**.
    2. Laukā **Faila komponenta nosaukums** atlasiet **ERVendOutPaymControlReport**, lai lietotu šo bāzlīniju ER formāta izvadei, kas ģenerē kontroles pārskatu.
    3. Laukā **Uzņēmumi** atlasiet **GBSI**, lai piemērotu šo bāzlīniju, kad GBSI uzņēmumā tiek palaists **BACS (UK)** ER formāts.
    4. Laukā **Faila nosaukuma maska** ievadiet **\*.XLSX**, lai izmantotu šo bāzlīniju tikai **ERVendOutPaymControlReport** formāta komponenta izvadēm, kurām faila nosaukuma paplašinājumā ir **.xslx**.
    5. Laukā **Bāzlīnija** atlasiet **Maksājuma XLSX kontroles pārskats**, lai šo bāzlīniju izmantotu salīdzinājumam ar ģenerēto izvadi.

    ![Bāzlīnijas kopsavilkuma cilnes lapā Konfigurācijas.](media/GER-BaselineRules.png "Bāzes līnijas kopsavilkuma cilnes ekrānuzņēmums lapā Konfigurācijas")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Testu reģistrēšana kreditoru maksājumu apstrādes validācijai

Kā funkcionāls prasmīgais lietotājs varat reģistrēt savas darbības kreditoru maksājumu apstrādes testēšanai. Mēs iesakām atskaņot (un rediģēt pēc nepieciešamības) iepriekš lejupielādēto uzdevuma reģistrēšanu **Prepare\\Recording.xml**. Šī reģistrēšana tiek izmantota, lai iestatītu visus testēšanas datus pareizā stāvoklī. Šī darbība ir nepieciešama, jo testēšanu var veikt daudz reižu, un katram testam jāizmanto dati, kas atrodas vienā stāvoklī.

### <a name="reset-user-settings"></a>Lietotāja iestatījumu atiestatīšana

1. Atveriet Noklusējuma informācijas paneli.
2. Atlasiet pogu **Iestatījumi** (zobrata simbols).
3. Atlasiet **Lietotāja opcijas**.
4. Atlasiet **Lietojuma dati**.
5. Atlasiet **Atiestatīt**.
6. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atiestatīt lietojuma datus.
7. Aizvērt lapu.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Darbību reģistrēšana datu sagatavošanai testam

1. Atlasiet pogu **Iestatījumi** (zobrata simbols).
2. Atlasiet **Uzdevuma reģistrētājs**.
3. Atlasiet **Atskaņot reģistrēšanu**.
4. Atlasiet **Atvērt no šī datora**.
5. Atlasiet **Pārlūkot** un atlasiet lokāli saglabāto failu **Prepare\\Recording.xml**.
6. Atlasiet **Sākt**.
7. Turpiniet atlasīt opciju **Atskaņot nākamo gaidošo darbību**, līdz ir atskaņotas visas reģistrēšanā norādītās darbības.

Šī uzdevuma reģistrēšana veic tālāk norādītās darbības.

1. Iestata apstrādātā maksājuma rindas statusu uz **Nav**.

    ![Uzdevuma reģistrēšanas darbības no 3. līdz 4.](media/GER-Recording1Review1.png "Uzdevuma ierakstīšanas soļu no 3. līdz 4. ekrānuzņēmums")

2. Ieslēdz ER lietotāja parametru **Palaist atkļūdošanas režīmā**.

    ![Uzdevuma reģistrēšanas darbības no 9. līdz 10.](media/GER-Recording1Review2.png "Uzdevuma ierakstīšanas soļu no 9. līdz 10. ekrānuzņēmums")

3. Iztīra ER atkļūdošanas žurnālu, kas satur ģenerēto failu un bāzlīniju salīdzinājuma rezultātus.

    ![Uzdevuma reģistrēšanas darbības no 13. līdz 15.](media/GER-Recording1Review3.png "Uzdevuma ierakstīšanas soļu no 13. līdz 15. ekrānuzņēmums")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Darbību reģistrēšana kreditoru maksājumu apstrādes testēšanai

Mēs iesakām atskaņot (un rediģēt pēc nepieciešamības) iepriekš lejupielādēto uzdevuma reģistrēšanu **Process\\Recording.xml**. Šī reģistrēšana tiek izmantota, lai apstrādātu kreditoru maksājumus un validētu ģenerēto dokumentu un atbilstošo bāzlīniju salīdzinājuma rezultātus.

1. Atlasiet pogu **Iestatījumi** (zobrata simbols).
2. Atlasiet **Uzdevuma reģistrētājs**.
3. Atlasiet **Atskaņot reģistrēšanu**.
4. Atlasiet **Atvērt no šī datora**.
5. Atlasiet **Pārlūkot** un atlasiet lokāli saglabāto failu **Process\\Recording.xml**.
6. Atlasiet **Sākt**.
7. Turpiniet atlasīt opciju **Atskaņot nākamo gaidošo darbību**, līdz ir atskaņotas visas reģistrēšanā norādītās darbības.

Šī uzdevuma reģistrēšana veic tālāk norādītās darbības.

1. Sāk kreditoru maksājumu apstrādi.
2. Atlasa pareizos izpildlaika parametrus un ieslēdz kontroles pārskata ģenerēšanu.

    ![Uzdevuma reģistrēšanas darbības no 3. līdz 8.](media/GER-Recording2Review1.png "Uzdevuma ierakstīšanas soļu no 3. līdz 8. ekrānuzņēmums")

3. Piekļūst ER atkļūdošanas žurnālam, lai reģistrētu ģenerēto izvades datu un atbilstošo bāzlīniju salīdzinājuma rezultātus.

    ER atkļūdošanas žurnālā salīdzinājuma rezultāti parādās laukā **Ģenerētais teksts**. Lauki **Formāta komponents** un **Formāta ceļš, kas izraisīja ierakstu žurnālā** attiecas uz faila komponentu, kuram ģenerētā izvade tika salīdzināta ar bāzlīniju.

    ![Pieteikumi lapā Elektronisko pārskatu palaišanas žurnāli.](media/GER-ERDebugLog.png "Ekrānuzņēmums pieteikumiem lapā Elektronisko pārskatu palaišanas žurnāli")

4. Pašreizējās izvades datu un bāzlīnijas salīdzinājums tiek reģistrēts, izmantojot uzdevuma reģistrētāja opciju **Validēt** un atlasot  **Pašreizējā vērtība**.

    ![Izmantojot validēšanas opciju salīdzinājumam ar pašreizējo vērtību.](media/GER-TRRecordValidation.png "Ekrānuzņēmums validācijas opcijas lietošanai salīdzinājumam ar pašreizējo vērtību")

    Tālāk redzamajā attēlā ir parādīts, kā uzdevuma reģistrēšanā izskatās reģistrētās validācijas darbības.

    ![Uzdevuma reģistrēšanas darbības no 13. līdz 15.](media/GER-Recording2Review2.png "Uzdevuma ierakstīšanas 13. un 15. soļa ekrānuzņēmums")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Reģistrēto testu pievienošana pakalpojumā Azure DevOps

1. Atveriet Azure DevOps vidi.
2. Atlasiet projektu, ko definējāt RSAT parametros, kad [konfigurējāt rīku](#prerequisites).
3. Atlasiet testa plānu, ko definējāt RSAT parametros, kad [konfigurējāt rīku](#prerequisites).
4. Izveidojiet jaunu testa gadījumu atlasītajam testa plānam, kā norādīts tālāk.

    1. Nosauciet testa gadījumu par **Datu sagatavošana kreditora elektroniskā maksājuma apstrādes testam**.
    2. Pievienojiet failu **Recording.xml** no iepriekš lejupielādētās mapes **Prepare**.

5. Izveidojiet jaunu testa gadījumu atlasītajam testa plānam, kā norādīts tālāk.

    1. Nosauciet testa gadījumu par **Kreditora maksājumu apstrādes, izmantojot ER formātu BACS (UK), tests**.
    2. Pievienojiet failu **Recording.xml** no iepriekš lejupielādētās mapes **Process**.

    ![Jauni testa gadījumi atlasītajam testa plānam.](media/GER-RSAT-DevOps-Tests-Passed.png "Ekrānuzņēmums jauniem testa gadījumiem atlasītajam testa plānam")

> [!NOTE]
> Pievērsiet uzmanību, lai pievienotie testi tiktu izpildīti pareizā secībā.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>RSAT sagatavošana reģistrēto testu izpildei

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Testu ielāde no Azure DevOps rīkā RSAT

1. Atveriet lokālo RSAT programmu pašreizējā topoloģijā.
2. Atlasiet **Ielādēt**, lai testus, kas pašlaik atrodas Azure DevOps, ielādētu rīkā RSAT.

    ![RSAT ielādētie testi.](media/GER-RSAT-RSAT-Tests-Loaded.png "RSAT iekrauto testu ekrānuzņēmums")

### <a name="create-automation-and-parameters-files"></a>Automatizācijas un parametru failu izveide

1. Rīkā RSAT atlasiet testus, ko ielādējāt no Azure DevOps.
2. Atlasiet **Jauns**, lai izveidotu RSAT automatizācijas un parametru failus.

    ![Automatizācijas un parametru faili, kas izveidoti RSAT.](media/GER-RSAT-RSAT-Tests-Initiated.png "RSAT automatizācijas un parametru failu, kas izveidoti RSAT, ekrānuzņēmums")

### <a name="modify-the-parameters-files"></a>Parametru failu modificēšana

1. Rīkā RSAT atlasiet testa gadījumu **Datu sagatavošana kreditora elektroniskā maksājuma apstrādes testam**.
2. Atlasiet **Rediģēt**.
3. Atvērtās Microsoft Excel darbgrāmatas darblapā **Vispārēji** mainiet uzņēmuma kodu uz **GBSI**, jo šis uzņēmums tiks izmantots testa izpildei.
4. Rīkā RSAT atlasiet testa gadījumu **Kreditora maksājumu apstrādes, izmantojot ER formātu BACS (UK), tests**.
5. Atlasiet **Rediģēt**.
6. Atvērtās Excel darbgrāmatas darblapā **Vispārēji** mainiet uzņēmuma kodu uz **GBSI.**
7. Darblapā **ERFormatMappingRunLogTable** ievērojiet, ka šūnās A:3 un C:3 ir teksts no ER atkļūdošanas žurnāla tabulas laukiem, kas tiek izmantoti, lai validētu izvades datu un bāzlīnijas salīdzinājuma rezultātus. Šie teksti tiks izmantoti, lai novērtētu ER atkļūdošanas žurnāla ierakstus, kas ir izveidoti testa izpildes laikā.

    ![ERFormatMappingRunLogTable darblapa.](media/GER-RSAT-RSAT-ExcelParameters.png "Ekrānuzņēmums darblapai ERFormatMappingRunLogTable")

## <a name="run-the-tests-and-analyze-the-results"></a>Testu izpilde un rezultātu analīze

### <a name="run-the-tests-in-rsat"></a>Testu izpilde rīkā RSAT

1. Rīkā RSAT atlasiet ielādētos testus.
2. Atlasiet **Izpildīt**.

Ievērojiet, ka testa gadījumi tiek automātiski izpildīti programmā, izmantojot tīmekļa pārlūkprogrammu.

### <a name="analyze-the-results-of-test-execution"></a>Testa izpildes rezultātu analīze

Testa izpildes rezultāti tiek saglabāti rīkā RSAT. Ievērojiet, ka abi testi tika izpildīti veiksmīgi.

![Testi, kas izgāja RSAT.](media/GER-RSAT-RSAT-Tests-Passed.png "RSAT izgājušo testu ekrānuzņēmums")

Ievērojiet, ka testa izpildes rezultāti tiek nosūtīti arī pakalpojumā Azure DevOps, lai jūs varētu veikt padziļinātu analīzi.

![Testa izpildes rezultāti Azure DevOps.](media/GER-RSAT-DevOps-Tests-Added.png "Testa izpildes rezultātu ekrānuzņēmums Azure DevOps")

### <a name="simulate-a-situation-where-tests-fail"></a>Neveiksmīga testa situācijas simulācija

Šis testa komplekts ir neveiksmīgs, ja vismaz viens no ģenerētajiem rezultātiem neatbilst atbilstošajai bāzlīnijai. Lai šādu situāciju panāktu, varat izmantot savu atvasināto formāta **BACS (UK)** versiju, kas ģenerē maksājuma failu ar atšķirīgu saturu, nekā atbilstošajā bāzlīnijā. Lai simulētu šo situāciju, varat izmantot to pašu formātu **BACS (UK)**, bet mainiet maksājuma summu apstrādātajā maksājuma rindā.

1. Atveriet programmu un dodieties uz **Kreditori \> Maksājumi \> Maksājumu žurnāls**.
2. Atlasiet **Rindas**.
3. Atlasiet maksājuma rindu un pēc tam atlasiet **Maksājuma statuss \> Nav**.
4. Laukā **Debets** mainiet vērtību no **1000,00** uz **2000,00**.
5. Atlasiet **Saglabāt**, lai saglabātu izmaiņas.

### <a name="run-the-tests-in-rsat"></a>Testu izpilde rīkā RSAT

1. Rīkā RSAT atlasiet ielādētos testus.
2. Atlasiet **Izpildīt**.

Ievērojiet, ka testa gadījumi tiek automātiski izpildīti programmā, izmantojot tīmekļa pārlūkprogrammu.

### <a name="analyze-the-results-of-test-execution"></a>Testa izpildes rezultātu analīze

Testa izpildes rezultāti tiek saglabāti rīkā RSAT. Ievērojiet, ka otrais tests neizdevās otrās izpildes laikā.

![Neizdevušies testa rezultāti RSAT.](media/GER-RSAT-RSAT-Tests-Failed.png "RSAT neizdevušos testa rezultātu ekrānuzņēmums")

Ievērojiet, ka testa izpildes rezultāti tiek nosūtīti arī pakalpojumā Azure DevOps, lai jūs varētu veikt padziļinātu analīzi.

![Neizdevušies testa rezultāti Azure DevOps.](media/GER-RSAT-DevOps-Tests-Failed.png "Neizdevušos testa rezultātu ekrānuzņēmums Azure DevOps")

Varat piekļūt katra testa statusam. Varat arī piekļūt izpildes žurnālam, lai analizētu kļūdas iemeslus. Nākamajā attēlā izpildes žurnālā ir redzams, ka kļūda radās ģenerētā maksājuma faila satura un tā bāzlīnijas satura atšķirību dēļ.

![Izpildes žurnāls kļūmes analīzei Azure DevOps.](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Izpildes žurnāla ekrānuzņēmums, lai analizētu kļūmi Azure DevOps")

Tātad, kā jau ir redzams, jebkura ERformāta funkcionalitāti var novērtēt automātiski, izmantojot RSAT kā testēšanas platformu un izmantojot uzdevuma reģistrētājam atbilstošus testa gadījumus, kas izmanto ER bāzlīnijas funkciju.

## <a name="additional-resources"></a>Papildu resursi

- [Uzdevuma reģistrētāja resursi](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Piemērotības lietotājiem testu izveide un automatizēšana](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Tādu vižu izvietošana, kuras atbalsta un izmanto pastāvīgu būvēšanu un testu automatizēšanu](../perf-test/continuous-build-test-automation.md)
- [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md)
- [ER Jaunināt savu formātu, pieņemot šī formāta jaunu bāzes versiju](tasks/er-upgrade-format.md)
- [ER Importēt konfigurāciju no Lifecycle Services](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]