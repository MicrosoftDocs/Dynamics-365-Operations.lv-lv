---
title: Ģenerēto ER pārskatu rezultātu izsekošanas un to salīdzināšanas ar bāzlīnijas vērtībām uzlabojumi
description: Šajā tēmā ir sniegta informācija par ER bāzlīnijas līdzekļa uzlabojumiem Microsoft Dynamics 365 for Finance and Operations versijā 10.0.3 (2019. jūnijs).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 222a415f686c8028fc2a414f97eed0291d850ae7
ms.sourcegitcommit: 9917df8c0c9320955c61186cd922c8df894a4f25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700686"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a>Ģenerēto ER pārskatu rezultātu izsekošanas un to salīdzināšanas ar bāzlīnijas vērtībām uzlabojumi

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīta pirmā uzlabojumu kopa, kas ieviesta elektronisko pārskatu veidošanas (ER) struktūras bāzlīnijas līdzeklī. Šie uzlabojumi ir pieejami Microsoft Dynamics 365 for Finance and Operations versijā 10.0.3 (2019. gada jūnijs) un jaunākās versijās.

## <a name="automate-the-setting-of-baseline-rules"></a>Bāzlīnijas kārtulu iestatīšanas automatizācija

Tēmā [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md) ir paskaidrots, kā konfigurēt ER struktūru, lai apkopotu informāciju par ER formāta izpildēm un novērtētu šo izpilžu rezultātus. Šajā tēmā sniegtajā piemērā ir parādītas veicamās darbības.

Tālāk ir norādītas dažas darbības.

- Izpildiet ER formātu, lai ģenerētu izejošo failu, un saglabājiet failu lokāli.
- Pievienojiet lokāli saglabāto failu kā ER formātam pievienotās bāzlīnijas pielikumu.
- Konfigurējiet pievienotās bāzlīnijas kārtulu. Šajā konfigurācijā ir ietvertas šādas darbības:

    - norādīt ER formāta elementu, kas tiek izmantots, lai ģenerētu izejošo failu;
    - atlasīt pielikumu, kas attiecas uz ģenerēto izejošo failu.

> [!NOTE]
> Šīs darbības ir jāveic manuāli, kaut arī jaunās ER iespējas ļauj tās automatizēt. Lai uzzinātu vairāk par šo līdzekli, izpildiet šo piemēru.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Piemērs: bāzlīnijas kārtulu iestatīšanas automatizācija

Lai izpildītu šajā piemērā norādītās darbības, vispirms ir jāizpilda darbības, kas aprakstītas tēmā [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md) sniegtajā piemērā, līdz sadaļai “Jaunas bāzlīnijas pievienošana izveidotam ER formātam”.

### <a name="review-added-baseline"></a>Pievienotas bāzlīnijas pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Atlasiet **Bāzlīnijas**.

    > [!NOTE]
    > Poga **Bāzlīnijas** ir pieejama tikai tad, kad ER lietotāja parametrs **Palaist atkļūdošanas režīmā** ir ieslēgts pašreizējam uzņēmumam.

Bāzlīnija tika pievienota atlasītajam formātam **Formāts ER bāzlīniju apgūšanai**, bet šai bāzlīnijai vēl nav pievienotas bāzlīnijas kārtulas.

![Elektronisko pārskatu veidošanas formāta bāzlīniju lapa](media/GER-BaselineSample-AddBaseline2.PNG "Elektronisko pārskatu veidošanas formāta bāzlīniju lapas ekrānuzņēmums")

### <a name="make-a-new-baseline-rule"></a>Jaunas bāzlīnijas kārtulas izveide

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Kokā izvērsiet vienumu **Modelis ER bāzlīniju apgūšanai**.
3. Kokā atlasiet **Modelis ER bāzlīniju apgūšanai\\Formāts ER bāzlīniju apgūšanai**.
4. Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
5. Laukā **Ievadīt ID** ievadiet **1**.
6. Atlasiet opcijas **Izveidot bāzlīnijas failus** iestatījumu **Jā**.
7. Atlasiet **Labi**.

    ![Dialoglodziņš Elektronisko pārskatu parametri](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Dialoglodziņa Elektronisko pārskatu parametri ekrānuzņēmums")

8. Atlasiet **Bāzlīnijas**.

    ![Elektronisko pārskatu veidošanas formāta bāzlīniju lapa](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Elektronisko pārskatu veidošanas formāta bāzlīniju lapas ekrānuzņēmums")

    Ģenerētais izejošais fails tiek automātiski pievienots izpildītā ER formāta bāzlīnijai. Bāzlīnijas kārtula tiek automātiski pievienota šai bāzlīnijai un arī satur atsauci uz pievienoto failu.

9. Laukā **Nosaukums** ievadiet **1. bāzlīnija**.
10. Laukā **Faila nosaukuma maska** ievadiet **.xml**.
11. Atlasiet **Saglabāt**.

### <a name="run-the-format"></a>Formāta palaišana

Tagad varat pabeigt atlikušās piemēra darbības tēmā [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md), sākot no sadaļas “Paredzētā ER formāta palaišana un žurnāla pārskatīšana, lai analizētu rezultātus”.

> [!NOTE]
> Dzēšot automātiski pievienoto bāzlīnijas kārtulu kopsavilkuma cilnē **Bāzlīnijas**, pielikums ar atsauci netiek automātiski dzēsts.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Bāzlīnijas konfigurēšana, lai tā ignorētu pastāvīgi mainītās ER izvades daļas

Ja ER formāts ir izstrādāts, lai ietvertu informāciju, kas, palaižot formātu, tiek mainīta, formātam ir nepieciešams izmantot ER bāzlīnijas funkciju, lai salīdzinātu ģenerētos rezultātus ar bāzlīnijas vērtībām. Informācija var būt, piemēram, apstrādes datums un laiks vai ģenerēta dokumenta unikālais identifikators dažādos formātos (globāli unikālais identifikators \[GUID\] utt.). Jaunās ER iespējas ļauj konfigurēt bāzlīnijas kārtulu tā, lai tā ignorētu ER formāta maināmos elementus, kad formāts tiek palaists ar mērķi salīdzināt bāzlīnijas vērtības ar formāta izpildes rezultātiem. Lai uzzinātu vairāk par šo līdzekli, izpildiet šo piemēru.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Piemērs: bāzlīnijas konfigurēšana, lai tā ignorētu pastāvīgi mainītās ER izvades daļas

Lai izpildītu šajā piemērā norādītās darbības, vispirms ir jāizpilda darbības, kas aprakstītas tēmā [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md) sniegtajā piemērā.

### <a name="modify-a-configured-er-format"></a>Konfigurēta ER formāta modificēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Kokā izvērsiet vienumu **Modelis ER bāzlīniju apgūšanai**.
3. Kokā atlasiet **Modelis ER bāzlīniju apgūšanai\\Formāts ER bāzlīniju apgūšanai**.
4. Atlasiet **Noformētājs**.
5. Kokā atlasiet **Izvade\\Dokuments**.
6. Atlasiet **Pievienot**.
7. Nolaižamajā dialoglodziņā, kas atrodas kokā, atlasiet **XML\\Atribūts**.
8. Laukā **Nosaukums** ievadiet **ProcessingDateTime**.
9. Atlasiet **Labi**.
10. Cilnes **Kartēšana** kokā atlasiet **Izvade\\Dokuments\\ProcessingDateTime**.
11. Atlasiet **Rediģēt formulu**.
12. Laukā **Formula** ievadiet šo izteiksmi: **DATETIMEFORMAT(NOW(), "O")**.
13. Atlasiet **Saglabāt** un pēc tam **Testēt**.
14. Lai testētu konfigurēto izteiksmi atkārtoti, vēlreiz atlasiet **Testēt**.

    ![Formulas veidotāja lapa](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Formulas veidotāja lapas ekrānuzņēmums")

    > [!NOTE]
    > Cilnē **Testa rezultāts** tiek parādīts, ka katru reizi, kad konfigurētā izteiksme tiek izsaukta, tā atgriež citu datuma un laika vērtību.

15. Atlasiet lapu **Formulas veidotājs** un pēc tam atlasiet **Saglabāt**.

    ![Formāta veidotāja lapa](media/GER-BaselineSample-FormatMappingDesign2.PNG "Formāta veidotāja lapas ekrānuzņēmums")

16. Aizveriet lapu **Formāta veidotājs**.

### <a name="remove-an-existing-baseline-rule"></a>Esošas bāzlīnijas kārtulas noņemšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Atlasiet **Bāzlīnijas**.
3. Bāzlīniju sarakstā atlasiet bāzlīniju, kas konfigurēta formātam **Formāts ER bāzlīniju apgūšanai**.
4. Kopsavilkuma cilnē **Bāzlīnijas** atlasiet **Dzēst**, lai noņemtu iepriekš konfigurēto bāzlīnijas kārtulu.

![Elektronisko pārskatu veidošanas formāta bāzlīniju lapa](media/GER-BaselineSample-AddBaseline3.PNG "Elektronisko pārskatu veidošanas formāta bāzlīniju lapas ekrānuzņēmums")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Izveidotā ER formāta saistījumu aizstājēju definēšana

1. Lapas **Konfigurācijas** kopsavilkuma cilnē **Aizstājēji** atlasiet **Atlasīt komponentus**.
2. Formāta komponentu kokā izvērsiet **Izvade**, izvērsiet **Izvade\\Dokuments** un pēc tam atlasiet vienuma **Izvade\\Dokuments\\ProcessingDateTime** izvēles rūtiņu.

    ![Dialoglodziņš Atlasīt komponentus](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Dialoglodziņa Atlasīt komponentus ekrānuzņēmums")

3. Atlasiet **Labi**.

![Elektronisko pārskatu veidošanas formāta bāzlīniju lapa](media/GER-BaselineSample-AddBaseline4.PNG "Elektronisko pārskatu veidošanas formāta bāzlīniju lapas ekrānuzņēmums")

Atlasītais ER formāta komponents ir pievienots komponentu sarakstam kopsavilkuma cilnē **Aizstājēji**. Kad pamata ER formāts tiek palaists atkļūdošanas režīmā, katra komponenta saistījums formātā tiek aizstāts ar saistījumu, kas redzams kolonnā **Saistīšana**. Lai mainītu komponenta noklusējuma saistījumu, kas uzskaitīts kopsavilkuma cilnē **Aizstājēji**, atlasiet **Rediģēt**.

### <a name="make-a-new-baseline-rule"></a>Jaunas bāzlīnijas kārtulas izveide

Izpildiet darbības, kas aprakstītas šīs tēmas sadaļā “Piemērs: bāzlīnijas kārtulu iestatīšanas automatizācija”. Paziņojums brīdina, ka izejošais fails ir ģenerēts, izmantojot bāzlīnijas iestatījumus, un ir notikusi formāta saistījumu piespiedu aizstāšana.

![Paziņojums lapā Konfigurācijas](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Paziņojuma lapā Konfigurācijas ekrānuzņēmums")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Brīdinājumu par formāta saistījumu aizstāšanu izlaišana

Iestatot konkrētus ER parametrus, varat izlaist paziņojumus, kas brīdina par formāta saistījumu aizstāšanu. Šī izlaišana var noderēt, kad formāta saistījumi tiek aizstāti neuzraudzītā režīmā, izmantojot Regression Suite Automation Tool. Šajā gadījumā brīdinājumu var uzskatīt par palaista testa gadījuma kļūmi.

1. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas** atlasiet vienumu **Lietotāja parametri**.
2. Atlasiet opcijai **Izlaist bāzlīnijas brīdinājumus** iestatījumu **Jā** un pēc tam atlasiet **Labi**.

![Dialoglodziņš Lietotāja parametri](media/GER-BaselineSample-ERUserParameters1.png "Dialoglodziņa Lietotāja parametri ekrānuzņēmums")

### <a name="review-the-generated-baseline-file"></a>Ģenerētā bāzlīnijas faila pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Atlasiet **Bāzlīnijas**.
3. Atlasiet **Pielikumi**.

    ![Lapa Pielikumi](media/GER-BaselineSample-AttachedBaselineFile.PNG "Lapas Pielikumi ekrānuzņēmums")

    > [!NOTE]
    > Ģenerētajā failā ir ietverts apstrādes datuma un laika teksts (**"#"**) no saistījuma, kas tika konfigurēts pievienotajā bāzlīnijas kārtulā, nevis no formāta saistījuma.

4. Aizveriet lapu **Pielikumi**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Paredzētā ER formāta palaišana un žurnāla pārskatīšana, lai analizētu rezultātus

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Kokā izvērsiet vienumu **Modelis ER bāzlīniju apgūšanai**.
3. Kokā atlasiet **Modelis ER bāzlīniju apgūšanai\\Formāts ER bāzlīniju apgūšanai**.
4. Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
5. Laukā **Ievadīt ID** ierakstiet **1**.
6. Atlasiet **Labi**.
7. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas atkļūdošanas žurnāli**.

Izpildes žurnālā ir ietverta informācija par ģenerētā faila salīdzinājuma rezultātiem ar konfigurēto bāzlīniju. Žurnālā ir norādīts, ka ģenerētais fails un bāzlīnija ir vienādas, kaut arī izpildītais formāts ietver saistījumu pastāvīgi mainīgas datuma un laika vērtības ievadīšanai izejošajā failā.

> [!NOTE]
> Lai gan izejošais fails ir ģenerēts, izmantojot bāzlīnijas iestatījumus, kas iespējo formāta saistījumu piespiedu aizstāšanu, brīdinājumi par aizstāšanu netiek rādīti.

## <a name="exchange-baseline-settings-between-environments"></a>Bāzlīnijas iestatījumu apmaiņa starp vidēm

### <a name="export-baseline-settings"></a>Bāzlīnijas iestatījumu eksportēšana

Jaunās ER iespējas ļauj eksportēt bāzlīnijas iestatījumus atlasītajam ER formātam no pašreizējās Finance and Operations vides un saglabāt tos kā XML failus. 

Lai eksportētu bāzlīnijas iestatījumus, lapā **Elektronisko pārskatu veidošanas formāta bāzlīnijas** atlasiet **Eksportēt**.

### <a name="import-baseline-settings"></a>Importēt bāzlīnijas iestatījumus

Eksportētos bāzlīnijas iestatījumus var importēt citā Finance and Operations vidē. Vide vispirms ir jāimportē kā ER formāts. Pēc tam varat importēt bāzlīnijas iestatījumus.

Lai importētu bāzlīnijas iestatījumus no lokāli saglabāta XML faila, lapā **Elektronisko pārskatu veidošanas formāta bāzlīnijas** atlasiet **Importēt** un pēc tam atlasiet **Pārlūkot**, lai atlasītu XML failu.

![Dialoglodziņš Importēt bāzlīnijas iestatījumus](media/GER-BaselineSample-ImportBaseline1.PNG "Dialoglodziņa Importēt bāzlīnijas iestatījumus ekrānuzņēmums")

Lai importētu bāzlīnijas iestatījumus no XML faila, kas saglabāts Microsoft SharePoint serverī, balstoties uz pašreizējiem dokumentu pārvaldības iestatījumiem un atlasītā dokumenta veida, lapā **Elektronisko pārskatu veidošanas formāta bāzlīnijas** atlasiet **Importēt no avota**. Pēc tam atlasiet dokumenta veidu un XML failu. Dokumenta tips, kas nepieciešams, lai piekļūtu SharePoint mapei, ir jākonfigurē iepriekš.

![Dialoglodziņš Importēt no avota](media/GER-BaselineSample-ImportBaseline2.PNG "Dialoglodziņa Importēt no avota ekrānuzņēmums")

> [!NOTE]
> Varat izmantot uzdevumu ierakstītāju, lai reģistrētu darbības, kas jāveic nepieciešamā dokumenta veida un faila nosaukuma atlasīšanai dialoglodziņā **Importēt no avota**. Šādā veidā varat saglabāt nepieciešamos bāzlīnijas iestatījumus SharePoint serverī un pēc tam automātiski importēt tos, atskaņojot uzdevuma ierakstu, kad palaižat automātiskos testus ar Regression Suite Automation Tool.

## <a name="additional-resources"></a>Papildu resursi

- [Ģenerēto pārskatu rezultātu izsekošana un to salīdzināšana ar bāzlīnijas vērtībām](er-trace-reports-compare-baseline.md)
- [Uzdevumu reģistrētājs](../user-interface/task-recorder.md)
