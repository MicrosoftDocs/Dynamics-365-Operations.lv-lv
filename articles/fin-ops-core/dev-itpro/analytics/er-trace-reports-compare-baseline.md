---
title: Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām
description: Šajā tēmā ir izskaidrots, kā ģenerēto elektronisko pārskatu (ER) rezultātus varat salīdzināt ar bāzlīnijas pārskata vērtībām.
author: NickSelin
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 9fabdef96b02747c84a76bf42997633842f185e9
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605209"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām

[!include[banner](../includes/banner.md)]

Varat izsekot tādu elektronisko pārskatu (ER) formātu rezultātus, kas ģenerē izejošos elektroniskos dokumentus. Kad izsekošanas ģenerēšana ir ieslēgta (izmantojot ER lietotāja parametru **Palaist atkļūdošanas režīmā** ), ER formāta izpildes žurnālā tiek ģenerēts jauns izsekošanas ieraksts katru reizi, kad tiek palaists ER pārskats. Katrā ģenerētajā izsekošanas reizē tiek saglabāta tālāk norādītā informācija.

- Visi brīdinājumi, ko ģenerēja validēšanas kārtulas
- Visas kļūdas, ko ģenerēja validēšanas kārtulas
- Visi ģenerētie faili, kas tiek saglabāti kā izsekošanas ieraksta pielikumi

Varat glabāt atsevišķus bāzlīnijas programmas failus jebkuram ER formātam. Faili tiek uzskatīti par bāzlīnijas failiem, ja tie apraksta palaisto pārskatu gaidītos rezultātus. Ja bāzlīnijas fails ir pieejams kādam ER formātam, kas tiek palaists, kamēr ir ieslēgta izsekošanas ģenerēšana, tad papildus iepriekš minētajai informācijai izsekošana saglabā arī rezultātus no ģenerētā elektroniskā dokumenta salīdzinājuma ar bāzlīnijas failu. Ar vienu klikšķi šo ģenerēto elektronisko dokumentu un tā bāzlīnijas failu varat arī saņemt vienā zip failā. Pēc tam varat veikt detalizētu salīdzināšanu, izmantojot kādu ārēju rīku, piemēram, WinDiff.

Varat novērtēt izsekošanu, lai analizētu, vai ģenerētajos elektroniskajos dokumentos ir gaidītais saturs. Šo novērtēšanu varat veikt lietotāju akcepttestēšanas (User Acceptance Testing — UAT) vidē, ja koda bāze ir mainīta (piemēram, ja veicāt migrēšanu uz jaunu programmas instanci, instalējāt labojumfailu pakotnes vai izvietojāt koda modifikācijas). Šādi varat pārliecināties, vai novērtējums neietekmē izmantoto ER pārskatu izpildi. Daudziem ER pārskatiem novērtēšanu var veikt neuzraudzītā režīmā.

Lai par šo līdzekli uzzinātu vairāk, noskatieties uzdevumu ceļvežus **ER Pārskatu ģenerēšana un rezultātu salīdzināšana (1. daļa)** un **ER Pārskatu ģenerēšana un rezultātu salīdzināšana (2. daļa)**, kas veido daļu no biznesa procesa **7.5.4.3 IT pakalpojumu/risinājumu testēšana (10679)** un ko var lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684). Šajos uzdevumu ceļvežos ir izklāstīts ER struktūras konfigurēšanas process, lai izmantotu bāzlīnijas failus ģenerēto elektronisko dokumentu novērtēšanai.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Piemērs: ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām

Šajā procedūrā ir izskaidrots, kā konfigurēt ER platformu, lai apkopotu informāciju par ER formāta izpildēm un pēc tam novērtētu šo izpilžu rezultātus. Novērtējuma ietvaros ģenerētie dokumenti tiek salīdzināti ar to bāzlīnijas failiem. Šajā piemērā jūs izveidosiet nepieciešamās ER konfigurācijas parauga uzņēmumam Litware, Inc. Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma. Šīs darbības var veikt, izmantojot jebkuru datu kopu.

Lai izpildītu šajā piemērā norādītās darbības, vispirms izpildiet darbības [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapā **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** pārbaudiet, vai ir uzskaitīts parauga uzņēmuma Litware, Inc. konfigurācijas nodrošinātājs un vai tas ir atzīmēts kā **Aktīvs**. Ja neredzat šos konfigurācijas nodrošinātājus, izpildiet darbības, kas aprakstītas sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-document-management-parameters"></a>Konfigurēt dokumentu pārvaldības parametrus

1. Dodieties uz **Organizācijas administrēšana** \> **Dokumentu pārvaldība** \> **Dokumentu tipi** un izveidojiet jaunu dokumenta tipu, lai saglabātu bāzlīnijas failus.
2. Laukā **Klase** ievadiet **Pievienot failu**.
3. Laukā **Grupa** ievadiet **Fails**.

![Lapa Dokumentu tipi.](media/GER-BaselineSample-SetupDocumentType.PNG "Dokumenta tipu lapas ekrānuzņēmums")

> [!NOTE]
> Katrai datu kopai, kurā plānojat izmantot ER bāzlīnijas līdzekli, ir jābūt konfigurētam jaunam dokumenta tipam ar tādu pašu nosaukumu.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>ER parametru konfigurēšana bāzlīnijas līdzekļa izmantošanas sākšanai

1. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.

    ![Elektronisko pārskatu darbvieta.](media/GER-BaselineSample-ERWorkspace.PNG "Elektronisko pārskatu darbvietas ekrānuzņēmums")

2. Cilnes **Pielikumi** laukā **Bāzlīnija** ievadiet vai atlasiet dokumenta tipu, kuru tikko izveidojāt.

    ![Elektronisko pārskatu parametru lapas pielikumu cilne.](media/GER-BaselineSample-ERParameters.PNG "Elektronisko pārskatu parametru lapas ekrānuzņēmums")

3. Atlasiet **Saglabāt** un pēc tam aizveriet lapu **Elektronisko pārskatu parametri**.

### <a name="add-a-new-er-model-configuration"></a>Pievienot jaunu ER modeļa konfigurāciju

1. Darbvietas **Elektroniskie pārskati** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
2. Darbību rūtī atlasiet **Izveidot konfigurāciju**.
3. Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **Modelis ER bāzlīniju apgūšanai**.
4. Atlasiet **Izveidot konfigurāciju**, lai apstiprinātu jauna ER datu modeļa ieraksta izveidi.

![Izveidojiet konfigurācijas dialoglodziņu, lai pievienotu jaunu ER modeļa konfigurāciju.](media/GER-BaselineSample-ModelAdd.PNG "Dialoglodziņa Izveidot konfigurāciju nolaižamā saraksta ekrānuzņēmums")

### <a name="design-a-data-model"></a>Datu modeļa izstrāde

1. Lapas **Konfigurācijas** darbības rūtī atlasiet **Veidotājs**.
2. Atlasiet **Jauns**.
3. Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **Sakne**.
4. Atlasiet **Pievienot**.
5. Atlasiet **Saknes atsauce**.
6. Atlasiet **Labi** un pēc tam **Saglabāt**.
7. Aizveriet lapu **Modeļa veidotājs**.
8. Atlasiet **Mainīt statusu**.
9. Atlasiet **Pabeigt** un pēc tam **Labi**.

![Lapa Konfigurācijas.](media/GER-BaselineSample-ModelComplete.PNG "Konfigurāciju lapas ekrānuzņēmums")

### <a name="add-a-new-er-format-configuration"></a>Jaunas ER formāta konfigurācijas pievienošana

1. Lapas **Konfigurācijas** darbības rūtī atlasiet **Izveidot konfigurāciju**.
2. Nolaižamajā dialoglodziņā lauku grupā **Jauns** atlasiet opciju **Formāts, pamatojoties uz datu modeli Modelis ER bāzlīniju apgūšanai**.
3. Laukā **Nosaukums** ievadiet **Formāts ER bāzlīniju apgūšanai**.
4. Atlasiet **Izveidot konfigurāciju**, lai apstiprinātu jauna ER formāta ieraksta izveidi.

![Izveidojiet konfigurācijas dialoglodziņu, lai pievienotu jaunu ER formāta konfigurāciju.](media/GER-BaselineSample-FormatAdd.PNG "Dialoglodziņa Izveidot konfigurāciju nolaižamā saraksta ekrānuzņēmums")

### <a name="design-a-format"></a>Formāta veidošana

Šim piemēram varat izveidot vienkāršu ER formātu, lai ģenerētu XML dokumentus.

1. Lapas **Konfigurācijas** darbības rūtī atlasiet **Veidotājs**.
2. Atlasiet **Pievienot sakni**.
3. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.

    1. Kokā atlasiet **Vispārīgi\\Fails**.
    2. Laikā **Nosaukums** ievadiet **Izvade**.
    3. Atlasiet **Labi**.

4. Atlasiet **Pievienot**.
5. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.

    1. Kokā atlasiet **XML\\Elements**.
    2. Laukā **Nosaukums** ievadiet **Dokuments**.
    3. Atlasiet **Labi**.

6. Kokā atlasiet **Izvade\\Dokuments**.
7. Atlasiet **Pievienot**.
8. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.

    1. Kokā atlasiet **XML\\Atribūts**.
    2. Laukā **Nosaukums** ievadiet **ID**.
    3. Atlasiet **Labi**.

    ![Formāta veidotāja lapa, kokā atlasītais XML atribūts.](media/GER-BaselineSample-FormatLayoutDesign.PNG "Formāta veidotāja lapas ekrānuzņēmums")

9. Cilnē **Kartēšana** atlasiet **Dzēst**.
10. Atlasiet **Pievienot sakni**.
11. Nolaižamā dialoglodziņa kokā atlasiet **Vispārīgi\\Lietotāja ievades parametrs** un pēc tam veiciet tālāk norādītās darbības.

    1. Laukā **Nosaukums** ievadiet **ID**.
    2. Laukā **Etiķete** ievadiet **Ievadīt ID**.
    3. Atlasiet **Labi**.

12. Kokā atlasiet **Izvade\\Dokuments\\ID**.
13. Atlasiet **Saistīt** un pēc tam **Saglabāt**.

![Formāta veidotāja lapa, cilne Kartēšana.](media/GER-BaselineSample-FormatMappingDesign.PNG "Formāta veidotāja lapas ekrānuzņēmums")

Balstoties uz izveidoto struktūru, konfigurētais formāts ģenerē XML failu. Šis XML satur elementu **Sakne**, kam ir atribūts **ID**, kas iestatīts uz vērtību, ko lietotājs ievada ER izpildlaika dialoglodziņā.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Jauna bāzlīnijas faila ģenerēšana izveidotam ER formātam

1. Lapas **Konfigurācijas** kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
2. Laukā **Ievadīt ID** ievadiet **1**.
3. Atlasiet **Labi**.

    ![Dialoglodziņš Elektronisko pārskatu parametri.](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Elektroniskā pārskata parametru dialoglodziņa ekrānuzņēmums")

4. Saglabājiet ģenerētā faila **out.Admin.xml** lokālo kopiju, lai vēlāk varētu to izmantot kā bāzlīniju šim ER formātam.

    ![Paziņojums par ģenerēto failu lapā Konfigurācijas.](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Paziņojuma par ģenerēto failu lapā Konfigurācijas ekrānuzņēmums")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>ER parametru konfigurēšana bāzlīnijas līdzekļa izmantošanai

1. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas** atlasiet vienumu **Lietotāja parametri**.
2. Atlasiet opcijai **Palaist atkļūdošanas režīmā** iestatījumu **Jā**.
3. Atlasiet **Labi**.

![Lietotāja parametru dialoglodziņš.](media/GER-BaselineSample-ERUserParameters.PNG "Lietotāja parametru dialoglodziņa ekrānuzņēmums")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Jaunas bāzlīnijas pievienošana izveidotam ER formātam

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Darbību rūtī atlasiet **Bāzlīnijas**.

    ![Bāzlīnijas poga lapā Konfigurācijas.](media/GER-BaselineSample-OpenBaselinePage.PNG "Bāzlīnijas pogas ekrānuzņēmums lapā Konfigurācijas")

3. Darbību rūtī atlasiet **Jauns**.
4. Atlasiet iepriekš izveidoto ER formātu **Formāts ER bāzlīniju apgūšanai**.
5. Atlasiet **Saglabāt**.

![Elektroniskā pārskata formāta bāzlīniju lapa.](media/GER-BaselineSample-AddBaseline.PNG "Elektronisko pārskatu formāta bāzlīniju lapu konfigurāciju ekrānuzņēmums")

Bāzlīnija tiek pievienota formātam **Formāts ER bāzlīniju apgūšanai**.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Pievienotās bāzlīnijas kārtulas konfigurēšana

1. Lapas **Elektronisko pārskatu veidošanas formāta bāzlīnijas** darbību rūtī atlasiet pogu **Pielikumi** (papīra saspraudes simbols).
2. Darbību rūtī atlasiet **Jauns** \> **Fails**. ER parametros iepriekš jābūt atlasītam dokumenta veidam **Fails**, kas tiks izmantots bāzlīniju failu glabāšanai.
3. Atlasiet **Pārlūkot** un atlasiet failu **out.Admin.xm**, kas tika ģenerēts, kad iepriekš palaidāt konfigurēto ER formātu.

    ![Lapa Pielikumi.](media/GER-BaselineSample-UploadBaselineFile.PNG "Pielikumu lapas ekrānuzņēmums")

4. Aizveriet lapu **Pielikumi**.
5. Kopsavilkuma cilnē **Bāzlīnijas** atlasiet **Jauns**.
6. Laukā **Nosaukums** ievadiet **1. bāzlīnija**.
7. Laukā **Faila komponenta nosaukums** ievadiet vai atlasiet **Izvade**. Šī vērtība norāda, ka konfigurētā bāzlīnija tiks salīdzināta ar failu, kas ģenerēts, izmantojot formāta elementu **Izvade**.
8. Laukā **Faila nosaukuma maska** ievadiet **\*.xml**.

    > [!NOTE]
    > Varat definēt faila nosaukuma masku. Kad ir definēta faila nosaukuma maska, bāzlīnijas ieraksts tiek izmantots ģenerētās ievades novērtēšanai tikai tad, ja ģenerētā izvades faila nosaukums atbilst šai maskai.

9. Ja konfigurētā bāzlīnija ir jāizmanto tikai tad, kad ER formātu **Formāts ER bāzlīniju apgūšanai** palaiž lietotāji, kuri ir pierakstījušies noteiktos uzņēmumos, atlasiet šos uzņēmumus laukā **Uzņēmumi**.
10. Laukā **Bāzlīnija** ievadiet vai atlasiet pielikumu **out.Admin**.
11. Atlasiet **Saglabāt**.

![Elektronisko pārskatu formāta bāzlīniju lapa, bāzlīnijas kopsavilkuma cilne ar atlasītu bāzlīniju.](media/GER-BaselineSample-SetupBaselineLine.PNG "Elektronisko pārskatu formāta bāzlīniju lapu konfigurāciju ekrānuzņēmums")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Paredzētā ER formāta palaišana un žurnāla pārskatīšana, lai analizētu rezultātus

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Kokā izvērsiet vienumu **Modelis ER bāzlīniju apgūšanai** un pēc tam atlasiet **Modelis ER bāzlīniju apgūšanai\\Formāts ER bāzlīniju apgūšanai**.
3. Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
4. Laukā **Ievadīt ID** ievadiet **1**.
5. Atlasiet **Labi**.
6. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas atkļūdošanas žurnāli**.

    ![Elektronisko pārskatu izpildes žurnālu lapa ar vienādām bāzlīnijām.](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Elektronisko pārskatu palaišanas žurnālu lapas ekrānuzņēmums")

    > [!NOTE]
    > Izpildes žurnālā ir ietverta informācija par ģenerētā faila salīdzinājuma rezultātiem ar konfigurēto bāzlīniju. Šajā piemērā žurnāls norāda, ka ģenerētais fails un bāzlīnija ir vienādi.

7. Atlasiet **Dzēst visu**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Paredzētā ER formāta palaišana un žurnāla pārskatīšana, lai analizētu rezultātus

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Kokā izvērsiet vienumu **Modelis ER bāzlīniju apgūšanai** un pēc tam atlasiet **Modelis ER bāzlīniju apgūšanai\\Formāts ER bāzlīniju apgūšanai**.
3. Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
4. Laukā **Ievadīt ID** ievadiet **2**.
5. Atlasiet **Labi**.
6. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas atkļūdošanas žurnāli**.

    ![Elektronisko pārskatu izpildes žurnālu lapa ar dažādām bāzlīnijām.](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Elektronisko pārskatu palaišanas žurnālu lapas ekrānuzņēmums")

    > [!NOTE]
    > Izpildes žurnālā ir ietverta informācija par ģenerētā faila salīdzinājuma rezultātiem ar konfigurēto bāzlīniju. Šajā piemērā žurnāls norāda, ka ģenerētais fails un bāzlīnija atšķiras.

7. Atlasiet **Salīdzināt**.

> [!NOTE]
> Ģenerētais fails un bāzlīnijas fails tiek piedāvāts kā .zip fails. Varat izmantot ārējos salīdzināšanas rīkus, piemēram, WinDiff, lai salīdzinātu failus un pārskatītu atšķirības.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu (EP) veidošanas struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
