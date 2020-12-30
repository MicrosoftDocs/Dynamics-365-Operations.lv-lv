---
title: No valsts konteksta atkarīgu EP modeļu kartējumu konfigurēšana
description: Šajā tēmā skaidrots, kā var iestatīt EP modeļa kartējumus, lai tie būtu atkarīgi no juridiskās personas, kas kontrolē to izmantošanu, valsts/reģiona konteksta.
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: a9035f128a1db4bcd126f09c0fe30c1857fa884a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680881"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>No valsts konteksta atkarīgu EP modeļu kartējumu konfigurēšana

[!include[banner](../includes/banner.md)]

Varat konfigurēt elektronisko pārskatu (EP) modeļu kartējumus tā, lai tie ieviestu vispārīgu datu modeli, bet būtu specifiski Dynamics 365 Finance. Šajā tēmā skaidrots, kā veidot vairākus EP modeļu kartējumus EP datu modelim, lai kontrolētu, kā tie tiek izmantoti atbilstošajiem EP formātiem, kas tiek palaisti no uzņēmumiem, kuriem ir atšķirīgs valsts/reģiona konteksts.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai izpildītu šajā tēmā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.

- Piekļuve Finance vienai no šīm lomām:
    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- Piekļuve Regulatory Configuration Services (RCS) instancei, kas ir nodrošināta tam pašam nomniekam, kuram nodrošināta Finance instance, vienai no šādām lomām:
    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

Dažām šīs tēmas darbībām ir nepieciešama EP formāta izpilde. Dažos gadījumos EP formāta izpildi ietekmē tā uzņēmuma valsts/reģiona konteksts, ar kuru pašlaik esat pieteicies. Varat palaist EP formātu pašreizējā RCS instancē, ja uzņēmums, kam ir nepieciešamās valsts/reģiona konteksts, ir pieejams RCS. Pretējā gadījumā ir jāaugšupielādē aizpildīta EP modeļa kartēšanas un ER formāta konfigurāciju versija, kas izmanto EP datu modeli jūsu Finance instancē, un tad jāpalaiž EP formāts šajā Finance instancē. Lai iegūtu informāciju par to, kā importēt konfigurācijas, kas atrodas RCS par finanšu instanci, skatiet [Konfigurāciju importēšana no RCS ](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>Viena modeļa kartēšanas gadījums

Veiciet darbības šīs tēmas [1. papildinājumā](#appendix1), lai izstrādātu obligāto EP komponentus. Tagad jums ir modeļa kartēšanas konfigurācija **Kartēšana(vispārīgā**), kas ietver modeļa kartēšanu **Ieejas punkta** 1 definīcijai.

![ER konfigurāciju lapa](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Konfigurētā formāta izpilde

1.  Lapas **Konfigurācijas** kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
2.  Atlasiet **Labi**.

Ievērojiet, ka tīmekļa pārlūks piedāvā lejupielādēt teksta failu, kas tika ģenerēts, izmantojot izpildīto EP formātu. Tā kā šis formāts ir konfigurēts, lai izmantotu **1. ieejas punkta** definīciju, un tikai viens modeļa kartējums pašlaik ir pieejams pamatmodelī, kas ietver kartēšanu šai definīcijai, izpildītais EP formāts izmanto modeļa **Kartēšana (vispārīga)** kartēšanu no konfigurācijas **Kartēšana (vispārīga)** kā datu avotu. Tāpēc lejupielādētajam failam ir teksts **Vispārīgā funkcionalitāte 1**.

## <a name="multiple-shared-model-mappings-case"></a>Vairāku koplietojamo modeļu kartējumu gadījums

Veiciet darbības šīs tēmas [2. papildinājumā](#appendix2), lai izstrādātu obligāto EP komponentus. Tagad jums ir modeļa kartēšanas konfigurācija  **Kartēšana (Vispārīga)** un **Pielāgota kartēšana (vispārīga)**, kas ietver modeļa kartēšanu **1. ieejas punkta** definīcijai.

![ER konfigurāciju lapa](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Konfigurētā formāta izpilde

1.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Formāts kartējumu apgūšanai**.
2.  Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
3.  Atlasiet **Labi**.

Ievērojiet, ka atlasītā EP formāta izpilde ir neveiksmīga. Kļūdas ziņojums informē par to, ka modelim **Modelis, lai uzzinātu kartējumus** un definīcijai **1. ieejas punkts** modeļa kartēšanas konfigurācijās **Kartēšanas (vispārīgā)** un **Pielāgotā kartēšana (vispārīgā) pielāgotās** pastāv vairāk nekā viena modeļa kartēšana. Šis ziņojums iesaka arī izvēlēties vienu no šīm konfigurācijām kā noklusēto konfigurāciju.

![ER konfigurāciju lapa](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Definēt noklusējuma kartējuma konfigurāciju

Veiciet šīs darbības, lai definētu modeļa kartēšanas konfigurāciju **Pielāgotā kartēšana (vispārīgā)** kā noklusējuma konfigurāciju tā, lai tās kartējumus varētu izmantot kā datu avotus EP formātam **Formāts kartējumu apgūšanai**.

1.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Pielāgotā kartēšana (vispārīgā)**.
2.  Ja nepieciešams, atlasiet **Rediģēt**, lai pašreizējo lapu padarītu gatavu rediģēšanai.
3.  Iestatiet opciju **Noklusējums modeļu kartēšanai** kā **Jā**.
4.  Atlasiet **Saglabāt**.

![ER konfigurāciju lapa](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Konfigurētā formāta izpilde

1.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Formāts kartējumu apgūšanai**.
2.  Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
3.  Atlasiet **Labi**.

Ievērojiet, ka atlasītā EP formāta izpilde ir veiksmīga. Tīmekļa pārlūks piedāvā lejupielādēt teksta failu, kas tika ģenerēts, izmantojot izpildīto EP formātu. Tā kā šis formāts ir konfigurēts, lai izmantotu definīciju **1. ieejas punkts**, un kā noklusējuma konfigurācija tika atlasīts modeļa kartēšanas konfigurācija **Pielāgotā kartēšana (vispārīgi)**, izpildītais EP formāts izmantoja modeļa kartēšanu **Kartēšanas kopija (vispārīgi)** konfigurācijā  **Pielāgotā kartēšana (vispārīgi)** kā datu avotu. Tāpēc lejupielādētajam failam ir teksts **Vispārīgā pielāgotā funkcionalitāte 1**.

> [!NOTE]
> Ja maināt uzņēmumu, ar kuru pašlaik esat pieteicies, un vēlreiz palaižat šo EP formātu, jūs iegūstat tādu pašu saturu ģenerētajā failā, jo noklusētā EP modeļa kartēšanas konfigurācija nesatur no uzņēmuma atkarīgus ierobežojumus.

## <a name="multiple-mixed-model-mappings-case"></a>Vairāku jaukto modeļu kartējumu gadījums

Veiciet darbības šīs tēmas [3. papildinājumā](#appendix3), lai izstrādātu obligāto EP komponentus. Tagad jums ir modeļa kartēšanas konfigurācijas **Kartēšana (vispārīga)**, **Pielāgotā kartēšana (vispārīga)** un **Kartēšanas (FR) modeļa kartēšana** , kas ietver modeļa kartēšanu **1. ieejas punkta** definīcijai.

Ievērojiet, ka modeļa kartēšanas konfigurācijas **Kartēšana (FR)** 1. versija ir konfigurēta tā, ka tā attiecas tikai uz EP formātiem **Modelim kartēšanas apgūšanai**, kas tiek palaists tajos Finance uzņēmumos, kuriem ir Francijas valsts/reģiona konteksts.

![ER konfigurāciju lapa](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Konfigurētā formāta izpilde

1.  Mainīt uzņēmumu uz  **FRSI**.
2.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Formāts kartējumu apgūšanai**.
3.  Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
4.  Atlasiet **Labi**.

Ievērojiet, ka atlasītā EP formāta izpilde ir veiksmīga. Tīmekļa pārlūks piedāvā lejupielādēt teksta failu, kas tika ģenerēts, izmantojot izpildīto EP formātu. Tā kā šis formāts ir konfigurēts, lai izmantotu definīciju **1. ieejas punkts**, un kā noklusējuma konfigurācija tika atlasīts modeļa kartēšanas konfigurācija **Pielāgotā kartēšana (vispārīgi)**, izpildītais EP formāts izmantoja modeļa kartēšanu **Kartēšanas kopija (vispārīgi)** konfigurācijā  **Pielāgotā kartēšana (vispārīgi)** kā datu avotu. Tāpēc lejupielādētajam failam ir teksts **Vispārīgā pielāgotā funkcionalitāte 1**.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Noteikt Francijai specifisko kartēšanas konfigurāciju kā noklusēto konfigurāciju

Veiciet šīs darbības, lai definētu pielāgoto modeļa kartēšanas konfigurāciju **Kartēšana (FR)** kā noklusējuma konfigurāciju. Ņemiet vērā, ka, tā kā šis kartējums ir specifisks Francijai, tas tiks uzskatīts par noklusējuma kartējumu starp visām modeļa kartēšanas konfigurācijām, kurām ir konkretizēts valsts kods **FR** laukā **ISO valsts/reģiona kodi**.

1.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Kartēšana (FR)**.
2.  Ja nepieciešams, atlasiet **Rediģēt**, lai pašreizējo lapu padarītu gatavu rediģēšanai.
3.  Iestatiet opciju **Noklusējums modeļu kartēšanai** kā **Jā**.
4.  Atlasiet **Saglabāt**.

![ER konfigurāciju lapa](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Konfigurētā formāta izpilde

1.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Formāts kartējumu apgūšanai**.
2.  Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
3.  Atlasiet **Labi**.

Ievērojiet, ka atlasītā EP formāta izpilde ir veiksmīga. Tīmekļa pārlūks piedāvā lejupielādēt teksta failu, kas tika ģenerēts, izmantojot izpildīto EP formātu. Tā kā šis formāts ir konfigurēts, lai izmantotu definīciju **1. ieejas punkts**, un kā noklusējuma konfigurācija tika atlasīts modeļa kartēšanas konfigurācija **Kartēšana (FR)**, izpildītais EP formāts izmantoja modeļa kartēšanu **Kartēšana (FR)** konfigurācijā  **Kartēšana (FR)** kā datu avotu. Tāpēc lejupielādētajam failam ir teksts **FR funkcionalitāte 1**.

> [!NOTE]
> Ja maināt uzņēmumu, ar kuru pašlaik esat pieteicies, un vēlreiz palaižat šo EP formātu, izlaide būs atkarīga no atlasītā uzņēmuma valsts/reģiona konteksta.

## <a name="other-model-mapping-cases"></a>Citi modeļa kartēšanas gadījumi

Kā jau redzējāt, modeļa kartēšanas izvēle EP formāta izpildei darbojas šādā veidā:

- Modeļa kartēšanas definīcija, ko lieto EP formāts, tiek konkretizēta (šīs tēmas piemēros **1. ieejas punkts**).
- Visas kartēšanas konfigurācijas, kas ietver kartēšanu, kurai ir noteikta definīcija un kas ievēro jebkuru valstu/reģionu konteksta ierobežojumus, kas ir konfigurēti, var tikt izmantotas, lai palaistu EP formātu (šīs tēmas piemēros **Kartēšana (vispārīgā)**, **Pielāgotā kartēšana (vispārīgā)** un **Kartēšana (FR)**).
- Jebkurai noklusētā modeļa kartēšanai, kurai ir valsts/reģiona konteksta ierobežojumi, ir augstākā prioritāte atlasē (šīs tēmas piemēros **Kartēšana (FR)**).
- Jebkurai noklusētā modeļa kartēšanai, kurai nav valsts/reģiona konteksta ierobežojumi, ir nākamā augstākā prioritāte atlasē (šīs tēmas piemēros **Pielāgotā kartēšana (vispārīgi)**).
- Visiem modeļa kartējumiem, kuriem ir valsts/reģiona konteksta ierobežojumi, ir augstāka prioritāte atlasei nekā modeļa kartēšana, kurai nav valsts/reģiona konteksta ierobežojumu.

Tabulā ir sniegta informācija par modeļu kartēšanas atlases rezultātiem visiem iespējamiem gadījumiem modeļa kartēšanas iestatījumiem:

- 1. kolonna norāda, vai pirmais modeļu kartējums, kam nav norādīts valsts/reģiona konteksta ierobežojumi (piemēram koplietošanas kartējumam **Kartēšana (vispārīgā))**, ir klātesošs, un, ja ir, vai opcija **Noklusējums modeļa kartēšanai** ir iestatīta uz **Jā**.
- 2. kolonna norāda, vai otrais modeļu kartējums, kam nav norādīti valsts/reģiona konteksta ierobežojumi (piemēram koplietošanas kartējumam **Pielāgotā kartēšana (vispārīgā))**, ir klātesošs, un, ja ir, vai opcija **Noklusējums modeļa kartēšanai** ir iestatīta uz **Jā**.
- 3. kolonna norāda, vai pirmais modeļu kartējums, kam ir norādīti valsts/reģiona A konteksta ierobežojumi (piemēram Francijai specifiskajam kartējumam **Kartēšana (FR))**, ir klātesošs, un, ja ir, vai opcija **Noklusējums modeļa kartēšanai** ir iestatīta uz **Jā**.
- 4. kolonna norāda, vai otrais modeļu kartējums, kam ir norādīti valsts/reģiona A konteksta ierobežojumi un, ja ir, vai opcija **Noklusējums modeļa kartēšanai**  ir iestatīta uz **Jā**.
- 5. kolonnā ir sniegti modeļa kartēšanas atlases rezultāti EP formāta izpildei tā uzņēmuma kontrolē, kam ir valsts/reģiona A konteksts.
- 6. kolonnā ir sniegti modeļa kartēšanas atlases rezultāti EP formāta izpildei tā uzņēmuma kontrolē, kam ir valsts/reģiona A konteksts.

Tabulā ar plus zīmi (+) norāda modeļa kartēšanas konfigurācijas esamību pašreizējā Microsoft Azure pakalpojuma instancē, kas tiek izmantota EP formāta (Finance vai RCS) palaišanai.

| Pieteikums | Modeļa kartēšana 1 bez valsts/reģiona konteksta (MM1) | Modeļa kartēšana 2 bez valsts/reģiona konteksta (MM2) | Modeļa kartēšana 1 ar valsts/reģiona kontekstu A (MM1A) | Modeļa kartēšana 2 ar valsts/reģiona kontekstu A (MM2A) | Tiek palaists tā uzņēmuma kontrolē, kam ir valsts/reģiona konteksts A | Tiek palaists tā uzņēmuma kontrolē, kam ir valsts/reģiona konteksts B |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1.   |     2.   |    3    |    4.    |           5               |            6               |
|     1.   |         |         |         |         | Kļūda (trūkst kartējuma)   | Kļūda (trūkst kartējuma)    |
|     2.   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Kļūda (vairāki kartējumi) | Kļūda (vairāki kartējumi)  |
|     4.   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Kļūda (vairāki kartējumi) | MM1                        |
|     6   |     +   | noklusējums |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | noklusējums |         | MM1A                      | MM1                        |
|     8   |     +   |         | noklusējums |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | noklusējums | noklusējums | Kļūda (vairāki kartējumi) | MM1                        |
|    10.   | noklusējums |         |         |         | MM1                       | MM1                        |
|    11.   | noklusējums |    +    |         |         | MM1                       | MM1                        |
|    12.   | noklusējums |         |    +    |         | MM1                       | MM1                        |
|    13   | noklusējums | noklusējums |         |         | Kļūda (vairāki kartējumi) | Kļūda (vairāki kartējumi)  |
|    14.   | noklusējums |         | noklusējums |         | MM1A                      | MM1                        |
|    15   | noklusējums |         | noklusējums | noklusējums | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | noklusējums | noklusējums | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>Uzzināt, kāda kartēšana tika izmantota EP formāta izpildē

### <a name="configure-er-user-parameters"></a>ER lietotāju parametru konfigurēšana

1.  Lapas **Konfigurācijas** darbību rūtī, cilnē **KONFIGURĀCIJAS** atlasiet vienumu **Lietotāja parametri**.
2.  Atlasiet opcijai **Palaist atkļūdošanas režīmā** iestatījumu **Jā**.
4.  Atlasiet **Labi**.

### <a name="run-the-configured-format"></a>Konfigurētā formāta izpilde

1.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Formāts kartējumu apgūšanai**.
2.  Kopsavilkuma cilnē **Versijas** atlasiet **Palaist**.
3.  Atlasiet **Labi**.

### <a name="review-the-er-debug-log"></a>Skatīt EP atkļūdošanas žurnālu

1.  Navigācijas rūtī pārejiet uz sadaļu  **Moduļi \> Organizācijas administrēšana \> Elektroniskie pārskati \> Konfigurācijas atkļūdošanas žurnāls**.
2.  Atlasiet pogu **Pārlādēt šo lapu**.

![EP palaišanas žurnālu lapa](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Ievērojiet, ka ir pievienots jauns ieraksts EP atkļūdošanas žurnālam izpildītā EP formātā. Tā kā šī ieraksta lauks **Līmenis** ir iestatīts uz **Info**, ieraksts ir informatīvs. Tā kā formāta komponenta lauks ir iestatīts uz **Kartēšanas konfigurācija**, ieraksts informē par modeļa kartēšanu, kas tika izmantota, izpildot EP formātu **Formāts kartējumu apgūšanai** (atlasīts laukā **Konfigurācijas nosaukums**). Lauka **Ģenerētais teksts** saturs jūs informē, ka kartēšanas komponents **Kartēšana (FR)**, kas atrodas konfigurācijā **Kartēšana (FR)** ir izmantots šī pārskata palaišanai.

## <a name="appendix-1"></a><a name="appendix1"></a>1. pielikums

### <a name="configure-a-sample-data-model"></a>Konfigurēt parauga datu modeli

Piesakieties savā RCS instancē.

Šajā piemērā jūs izveidosiet konfigurāciju parauga uzņēmumam “Litware, Inc.”. Pirmkārt, lai izpildītu šīs darbības RCS, ir jāizpilda sekojošie soļi procedūrā [Konfigurācijas nodrošinātāja izveide un atzīmēšana ar aktīvu statusu](tasks/er-configuration-provider-mark-it-active-2016-11.md):

#### <a name="create-an-er-data-model-configuration"></a>Jaunas EP datu modeļa konfigurācijas izveide

1.  Noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.
2.  Atlasiet rūti **Pārskatu konfigurācijas**.
3.  Lapā **Konfigurācijas** atlasiet **Konfigurācijas izveidošana**.
4.  Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **Modelis kartējumu apgūšanai**.
5.  Atlasiet **Izveidot konfigurāciju**.
6.  Atlasiet kopsavilkuma cilni **Konfigurācijas komponenti**.

Ievērojiet, ka šīs EP konfigurācijas melnraksta 1. versija ir gatava rediģēšanai. Šajā versijā ir ietverts datu modeļa komponents.

#### <a name="design-a-sample-data-model"></a>Izveidot parauga datu modeli

1.  Lapā **Konfigurācijas** atlasiet **Veidotājs**.
2.  Atlasiet **Jauns**.
3.  Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **1. ieejas punkts**.
4.  Atlasiet **Pievienot**.
5.  Atlasiet **Jauns**.
6.  Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **Funkcionalitātes apraksts**.
7.  Atlasiet **Pievienot**.
8.  Atlasiet **Jauns**.
9.  Nolaižamā dialoglodziņa lauka grupā **Jauns mezgls** atlasiet **Modeļa sakne**.
10. Laukā **Nosaukums** ievadiet **2. ieejas punkts**.
11. Atlasiet **2. ieejas punkts**.
12. Atlasiet **Pievienot**.
13. Atlasiet **Jauns**.
14. Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **Funkcionalitātes apraksts**.
15. Atlasiet **Pievienot**.

    ![EP datu modeļa veidotāja lapa](./media/RCS-Context-specific-mapping-Model.PNG)

16. Atlasiet **Saglabāt**.
17. Aizvērt lapu.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>EP modeļa konfigurācijas modificētās versijas pabeigšana

1.  Lapas **Konfigurācijas** kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu**.

    > Mainiet izveidotā modeļa konfigurācijas statusu no **Melnraksts** uz **Pabeigts**, lai to varētu izmantot, lai izveidotu nepieciešamos modeļu kartējumus un formātus.

2.  Atlasiet **Pabeigt**.
3.  Atlasiet **Labi**.

Ņemiet vērā, ka izveidotā konfigurācija tiek saglabāta kā pabeigta versija 1.

### <a name="configure-a-sample-model-mapping"></a>Konfigurēt parauga modeļa kartējumu

#### <a name="create-an-er-model-mapping-configuration"></a>EP modeļa kartējuma konfigurācijas izveide

1.  Lapā **Konfigurācijas** atlasiet **Konfigurācijas izveidošana**.
2.  Nolaižamajā dialoglodziņā lauku grupā **Jauns** atlasiet opciju **Modeļa kartēšana, pamatojoties uz datu modeli Modelis kartējumu apgūšanai**.
3.  Laukā **Nosaukums** ievadiet **Kartēšana (Vispārīgā)**.
4.  Laukā **Datu modeļa definīcija**  atlasiet **1. ieejas punkts**.
5.  Atlasiet **Izveidot konfigurāciju**.

Ievērojiet, ka šīs EP konfigurācijas melnraksta 1. versija ir gatava rediģēšanai. Šajā versijā ir ietverts datu modeļa kartēšanas komponents.

#### <a name="design-a-sample-model-mapping"></a>Izveidot parauga modeļa kartējumu

1.  Lapā **Konfigurācijas** atlasiet **Veidotājs**.

    Ievērojiet, ka modeļa kartējums virziena veidam **Uz modeli** ir automātiski pievienots šim komponentam **1. ieejas punkta** definīcijai.
    
2.  Atlasiet **Veidotājs**, lai sāktu rediģēt pievienoto modeļa kartēšanu.
3.  Sadaļā **Datu modelis** atlasiet **Rediģēt**.
4.  Laukā **Formula** ievadiet **Vispārējā funkcionalitāte 1**.
5.  Atlasiet **Saglabāt**.
6.  Aizveriet lapu **Formāta veidotājs**.

    ![ER modeļa kartēšanas noformētāja lapa](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Atlasiet **Saglabāt**.
8.  Aizveriet lapu **Modeļa kartējuma noformētājs**.
9.  Atlasiet **Jauns**.
10. Laukā **Definīcija**  atlasiet **2. ieejas punkts**.
11. Laukā **Nosaukums** ievadiet **Kartēšana (Vispārīgā) 2**.
12. Atlasiet **Noformētājs**.
13. Sadaļā **Datu modelis** atlasiet **Rediģēt**.
14. Laukā **Formula** ievadiet **Vispārējā funkcionalitāte 2**.
15. Atlasiet **Saglabāt**.
16. Aizveriet lapu **Formāta veidotājs**.

    ![ER modeļa kartēšanas noformētāja lapa](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Atlasiet **Saglabāt**.
18. Aizveriet lapu **Modeļa kartējuma noformētājs**.

    ![EP modeļu kartējumu lapa](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Aizveriet lapu **Modeļa kartējumi**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Modeļa kartēšanas konfigurācijas modificētās versijas pabeigšana

1.  Lapas **Konfigurācijas** kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu**.

    > Mainiet izveidotā modeļa kartēšanas konfigurācijas statusu no **Melnraksts** uz **Pabeigts**, lai to varētu izmantot EP formāti.

2.  Atlasiet **Pabeigt**.
3.  Atlasiet **Labi**.

Ņemiet vērā, ka izveidotā konfigurācija tiek saglabāta kā pabeigta versija 1.

### <a name="configure-a-sample-format"></a>Parauga formāta konfigurēšana

#### <a name="create-an-er-format-configuration"></a>EP formāta konfigurēšana

1.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Modelis kartējumu apgūšanai**.
2.  Atlasiet **Izveidot konfigurāciju**.
3.  Nolaižamajā dialoglodziņā lauku grupā **Jauns** atlasiet opciju **Formāts, pamatojoties uz datu modeli Modelis EP kartējumu apgūšanai**.
4.  Laukā **Nosaukums** ievadiet **Formāts EP kartējumu apgūšanai**.
5.  Laukā **Datu modeļa definīcija**  atlasiet **1. ieejas punkts**.
6.  Atlasiet **Izveidot konfigurāciju**.

Ievērojiet, ka šīs EP konfigurācijas melnraksta 1. versija ir gatava rediģēšanai. Šajā versijā ir ietverts formāta komponents.

#### <a name="design-a-sample-format"></a>Parauga formāta veidošana

1.  Lapā **Konfigurācijas** atlasiet **Veidotājs**.
2.  Atlasiet **Pievienot sakni**.
3.  Grupā **Teksts** atlasiet vienumu **Virkne**.
4.  Atlasiet **Labi**.

#### <a name="bind-format-elements-to-a-data-source"></a>Saistīt formātā elementus ar datu avotu

1.  Lapā **Formāta veidotājs** cilnē **Kartēšana** izvērsiet modeļa datu avotu.
2.  Atlasiet lauku **Funkcionalitātes apraksts**.
3.  Atlasiet **Saistīt**.

    ![ER formāta veidotāja lapa](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Atlasiet **Saglabāt**.
5.  Aizvērt lapu.

## <a name="appendix-2"></a><a name="appendix2"></a>2. pielikums

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Konfigurēt parauga modeļa kartējumu vispārējai pielāgošanai

Iespējams, vēlēsieties pielāgot modeļa kartēšanu, ko jums piešķīra konfigurācijas nodrošinātājs (partneris), un pēc tam izmantot pielāgoto versiju kā datu avotu savam EP formātam. Šādā gadījumā ir jāizveido pielāgota EP modeļa kartēšanas konfigurācija, lai veiktu nepieciešamās izmaiņas esošajos modeļu kartējumos. Šajā papildinājumā aprakstītās procedūras izmanto modeli **Kartēšana (vispārīgi)** kā piemēru.

#### <a name="create-an-er-model-mapping-configuration"></a>EP modeļa kartējuma konfigurācijas izveide

1.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Pielāgotā kartēšana (vispārīgā)**.
2.  Atlasiet **Izveidot konfigurāciju**.
3.  Nolaižamajā dialoglodziņā lauka grupā **Jauns** atlasiet **Atvasināt no nosaukuma: kartēšana (vispārīga), Litware, Inc..**
4.  Laukā **Nosaukums** ievadiet **Pielāgotā kartēšana (vispārīgā)**.
5.  Atlasiet **Izveidot konfigurāciju**.

Ievērojiet, ka šīs EP konfigurācijas melnraksta 1. versija ir gatava rediģēšanai.

#### <a name="design-a-sample-model-mapping"></a>Izveidot parauga modeļa kartējumu

1.  Lapā **Konfigurācijas** atlasiet **Veidotājs**.

    > Ievērojiet, ka pamata konfigurācijas modeļu kartējumi ir automātiski kopēti uz šo konfigurāciju.

2.  Atlasiet **Kartēšanas kopija (vispārējā)**.
3.  Atlasiet **Noformētājs**.
4.  Sadaļā **Datu modelis** atlasiet **Rediģēt**.
5.  Laukā **Formula** ievadiet **Vispārējā pielāgotā funkcionalitāte 1**.
6.  Atlasiet **Saglabāt**.
7.  Aizvērt lapu.

    ![ER modeļa kartēšanas noformētāja lapa](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Atlasiet **Saglabāt**.
9.  Aizvērt lapu.
10. Atlasiet kartējumu **Kartēšanas kopija 2 (vispārējā)**.
11. Atlasiet **Noformētājs**.
12. Sadaļā **Datu modelis** atlasiet **Rediģēt**.
13. Laukā **Formula** ievadiet **Vispārējā pielāgotā funkcionalitāte 2**.
14. Atlasiet **Saglabāt**.
15. Aizvērt lapu.

    ![ER modeļa kartēšanas noformētāja lapa](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Atlasiet **Saglabāt**.
17. Aizvērt lapu.

    ![EP modeļu kartējumu lapa](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Aizvērt lapu.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Modeļa kartēšanas konfigurācijas modificētās versijas pabeigšana

1.  Lapas **Konfigurācijas** kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu**.

    > Mainiet izveidotā modeļa kartēšanas konfigurācijas statusu no **Melnraksts** uz **Pabeigts**, lai to varētu izmantot EP formāti.

2.  Atlasiet **Pabeigt**.
3.  Atlasiet **Labi**.

Ņemiet vērā, ka izveidotā konfigurācija tiek saglabāta kā pabeigta versija 1.

## <a name="appendix-3"></a><a name="appendix3"></a>3. pielikums

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Konfigurēt parauga modeļa kartējumu valstij/reģionam specifiskai pielāgošanai

Dažiem EP formātiem varētu būt valsts/reģiona specifiskas prasības datu sagatavošanai. Šādā gadījumā varat pārvaldīt atsevišķu EP modeļu kartēšanas konfigurāciju un izolēt šo valsts/reģiona specifisko prasību izpildi no vispārējās ieviešanas. Šajā papildinājumā aprakstītās procedūras izmanto EP formātu **Formāts kartējumu apgūšanai** un Francijai specifiskas prasības kā piemēru.

#### <a name="create-an-er-model-mapping-configuration"></a>EP modeļa kartējuma konfigurācijas izveide

Vispirms izveidojiet jaunu EP modeļa kartēšanas konfigurāciju, lai ieviestu valsts/reģiona specifiskās prasības. Izmantojiet savu pielāgoto EP modeļa kartēšanas konfigurāciju kā bāzi.

1.  Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Pielāgotā kartēšana (vispārīgā)**.
2.  Atlasiet **Izveidot konfigurāciju**.
3.  Nolaižamajā dialoglodziņā lauka grupā **Jauns** atlasiet **Atvasināt no nosaukuma: pielāgotā kartēšana (vispārīga), Litware, Inc..**
4.  Laukā **Nosaukums** ievadiet **Kartēšana (FR)**.
5.  Atlasiet **Izveidot konfigurāciju**.

Ievērojiet, ka šīs EP konfigurācijas melnraksta 1. versija ir gatava rediģēšanai.

#### <a name="design-a-sample-model-mapping"></a>Izveidot parauga modeļa kartējumu

1.  Lapā **Konfigurācijas** atlasiet **Veidotājs**.

    > Ievērojiet, ka pamata konfigurācijas modeļu kartējumi ir automātiski kopēti uz šo konfigurāciju.

2.  Atlasiet kartējumu **Kartēšanas kopijas kopija (vispārējā)**.
3.  Pārdēvējiet to uz **Kartēšana (FR)**.
4.  Atlasiet **Noformētājs**.
5.  Sadaļā **Datu modelis** atlasiet **Rediģēt**.
6.  Laukā **Formula** ievadiet **FR funkcionalitāte 1**.
7.  Atlasiet **Saglabāt**.
8.  Aizvērt lapu.

    ![ER modeļa kartēšanas noformētāja lapa](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Atlasiet **Saglabāt**.
10. Aizvērt lapu.
11. Atlasiet kartējumu **Kartēšanas kopijas kopija (vispārējā) 2**.
12. Pārdēvējiet to uz **Kartēšana (FR) 2**.
13. Atlasiet **Noformētājs**.
14. Sadaļā **Datu modelis** atlasiet **Rediģēt**.
15. Laukā **Formula** ievadiet **FR funkcionalitāte 2**.
16. Atlasiet **Saglabāt**.
17. Aizvērt lapu.

    ![ER modeļa kartēšanas noformētāja lapa](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Atlasiet **Saglabāt**.
19. Aizvērt lapu.

    ![EP modeļu kartējumu lapa](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Aizvērt lapu.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Norādīt valsts/reģiona konteksta ierobežojumus izmantošanai

1.  Lapas **Konfigurācijas** kopsavilkuma cilnē **ISO valsts/reģiona kodi** atlasiet **Jauns**.
2.  Laukā **ISO** atlasiet **FR**.
3.  Atlasiet **Saglabāt**.

Ņemiet vērā, ka jums ir jāpiesakās noteiktā uzņēmumā programmā Finance, lai palaistu EP formātu. Tāpēc šis uzņēmums var tikt uzskatīts par pusi, kas kontrolē gan EP formāta izpildi, gan atlases pareizu ER modeļa kartēšanu bāzes EP datu modelim. Pievienojot valsts kodu **FR**, jūs nosakāt, ka šis modeļa kartējums ir pieejams atlasei, lietojot EP formāta pamatdatu modeli tikai tad, ja šis formāts tiek palaists tā uzņēmuma kontrolē, kam ir Francijas valsts/reģiona konteksts.

Varat pievienot vairākus valstu/reģionu kodus vienai EP modeļa kartēšanas konfigurācijas versijai. Šādā veidā modeļa kartējumus, kas atrodas šajā modeļa kartēšanas konfigurācijā, var izmantot EP formātam, kas tiek palaists to uzņēmumu kontrolē, kuriem ir atšķirīgs valsts/reģiona konteksts.

Ievērojiet, ka valstu/reģionu kodu saraksts ir norādīts katrai EP modeļa kartēšanas konfigurācijas versijai, un tas var atšķirties atkarībā no versijas.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Modeļa kartēšanas konfigurācijas modificētās versijas pabeigšana

1.  Lapas **Konfigurācijas** kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu**.

    > Mainiet izveidotā modeļa kartēšanas konfigurācijas statusu no **Melnraksts** uz **Pabeigts**, lai to varētu izmantot EP formāti.

2.  Atlasiet **Pabeigt**.
3.  Atlasiet **Labi**.

Ņemiet vērā, ka izveidotā konfigurācija tiek saglabāta kā pabeigta versija 1.

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko ziņojumu (ER) pārskats](general-electronic-reporting.md)

[Elektronisko pārskatu modeļa kartēšanas pārvaldība atsevišķās elektronisko pārskatu konfigurācijās](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Lietot valsts/reģiona kontekstu](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Es konfigurēju divas kopīgas EP modeļa kartēšanas konfigurācijas RCS un atzīmēju vienu no tām kā noklusējuma modeļa kartēšanas konfigurāciju. Sekmīgi tika izveidots ER formāts, kas tika izveidots tai pašai bāzes EP datu modeļa konfigurācijai, lai testētu modeļu kartējumus. Pēc tam es importēju visu EP risinājumu (EP datu modelis, divas EP modeļa kartēšanas konfigurācijas un EP formāta konfigurācija) uz Finance. Kāpēc man tiek rādīts kļūdas ziņojums, kad mēģinu palaist to pašu EP formātu programmā Finance?
Noklusētais modeļa kartēšanas iestatījums ir specifisks videi. Tas ir konfigurēts RCS, bet nav eksportēts uz Finance. Lai sekmīgi palaistu šo ER formātu, jums ir jāatzīmē viena no ER modeļa kartēšanas konfigurācijām kā noklusējuma modeļa kartēšanas konfigurācija arī programmā Finance.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Es konfigurēju vienu modeļa kartējumu kā kopīgu modeļa kartēšanu un pabeidzu tā melnraksta versiju. Pēc tam es pievienoju jaunu modeļa kartēšanas konfigurāciju vienam un tam pašam datu modelim un to konfigurēju kā specifisku Francijai. Kāpēc koplietojamā modeļa kartēšana tiek atlasīta, kad tiek palaists EP formāts, kaut arī šis EP formāts izmanto pareizo saknes definīciju un izpilde tiek veikta tā uzņēmuma kontrolē, kam ir Francijas valsts/reģiona konteksts?
Pārliecinieties, vai koplietotā modeļa kartēšanas konfigurācija nav atzīmēta kā noklusētā modeļa kartēšanas konfigurācija. Pretējā gadījumā kartēšanas atlasē tai būs augstāka prioritāte. Pārliecinieties arī, vai Francijas specifiskā modeļa kartēšanas konfigurācija tiek ņemta vērā, kad EP formāta izpildes laikā tiek atlasīta kartēšana. EP modeļa kartēšanas konfigurācija ir pieejama atlasei tikai tad, ja ir izpildīts vismaz viens no šiem nosacījumiem:
- Vismaz viena EP modeļa kartēšanas konfigurācijas versija ir ar statusu **Pabeigta** vai **Kopīgota**. Šajā gadījumā versija, kurai ir visaugstākais versijas numurs, tiks izmantota EP formāta izpildei.
- Ir ieslēgta opcija **Palaist melnrakstu** EP modeļa kartēšanas konfigurācijai. Šajā gadījumā versija, kurai ir statuss **Melnraksts**, tiks izmantota EP formāta izpildei.
> Opcija **Palaist melnrakstu** kļūst pieejama lapā **Konfigurācijas** katrai EP modeļa kartēšanas konfigurācijai, ja ir ieslēgts EP lietotāja parametrs **Palaist iestatījumu**.
