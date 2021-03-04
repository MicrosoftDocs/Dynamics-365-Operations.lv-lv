---
title: Uzlabot ER risinājumu veiktspēju, pievienojot parameterizētus APRĒĶINĀTO LAUKU datu avotus
description: Šajā tēmā ir paskaidrots, kā var palīdzēt uzlabot Elektronisko atskaišu (Electroinic reporting - ER) risinājumu veiktspēju, pievienojot parameterizētus APRĒĶINĀTO LAUKU datu avotus.
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 940b696a06fb46bcd0557f059327cd4340448137
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681284"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>Uzlabot ER risinājumu veiktspēju, pievienojot parameterizētus APRĒĶINĀTO LAUKU datu avotus

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā var veikt [veiktspējas izsekošanu](trace-execution-er-troubleshoot-perf.md) attiecībā uz [Elektronisko atskaišu (ER)](general-electronic-reporting.md) formātiem, kas tiek palaisti, un tad izmantot šo izsekoto informāciju, lai palīdzētu uzlabot veiktspēju, konfigurējot parameterizētu **Aprēķinātā lauka** datu avotu.

ER konfigurāciju izstrādes procesa ietvaros, lai izveidotu biznesa dokumentus, nosakiet metodi, kas tiek izmantota, lai iegūtu datus no programmas un ievadītu tos ģenerētajā izvadē. Izveidojot **Aprēķinātā lauka** veida parameterizētu ER datu avotu, varat samazināt datu bāzes izsaukumu skaitu un ievērojami samazināt laiku un izmaksas, kas ir saistītas ar ER formāta izpildes detaļu savākšanu.

## <a name="prerequisites"></a>Priekšnosacījumi

- Lai izpildītu šīs tēmas piemērus, jums ir jābūt piekļuvei vienai no šādām [lomām](../sysadmin/tasks/assign-users-security-roles.md):

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- Uzņēmumam jābūt iestatītam uz **DEMF**.
- Izpildiet šīs tēmas [1. papildinājumā](#appendix1) norādītās darbības, lai lejupielādētu parauga Microsoft ER risinājuma komponentus, kas nepieciešami, lai aizpildītu piemērus šajā tēmā.
- Izpildiet šīs tēmas [2. papildinājumā](#appendix2) norādītās darbības, lai konfigurētu minimālu ER parametru kopumu, kas nepieciešams, lai izmantotu ER struktūru, lai palīdzētu uzlabot parauga Microsoft ER risinājuma veiktspēju.

## <a name="import-the-sample-er-solution"></a>Parauga ER risinājuma failu importēšana

Iedomājieties, ka jums ir jāizstrādā ER risinājums, lai ģenerētu jaunu pārskatu, kurā parādītas kreditoru darbības. Pašlaik varat atrast atlasītā kreditora transakcijas lapā **Kreditoru transakcijas** (pārejiet uz **Parādi kreditoriem** \> **Kreditori** \> **Visi kreditori**, atlasiet kreditoru un pēc tam darbību rūtī, cilnē **Kreditors**, grupā **Transakcijas** atlasiet vienumu **Transakcijas**). Tomēr ir nepieciešams, lai visas kreditoru transakcijas kopā būtu vienā elektroniskajā dokumentā XML formātā. Šis risinājums sastāv no vairākām ER konfigurācijām, kas ietver nepieciešamo datu modeli, modeļa kartējumu un formāta komponentus.

Pirmais solis ir importēt parauga ER risinājumu, lai ģenerētu kreditora darbību pārskatu.

1. Piesakieties Microsoft Dynamics 365 Finance instancē, kas nodrošināta jūsu uzņēmumam.
2. Šajā tēmā jūs izveidosit un modificēsit nepieciešamās konfigurācijas parauga uzņēmumam **Litware, Inc.** . Pārliecinieties, ka šis konfigurācijas nodrošinātājs ir pievienots jūsu Finance instancei un atzīmēts kā aktīvs. Papildinformāciju skatiet [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
4. Lapā **Konfigurācijas** importējiet ER konfigurācijas, kuras lejupielādējāt kā priekšnosacījumu pakalpojumā Finance, šādā secībā: datu modelis, modeļa kartējums, formāts. Katrai konfigurācijai rīkojieties šādi.

    1. Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.
    2. Atlasiet **Pārlūkot** un atlasiet atbilstošu failu ER konfigurācijai XML formātā.
    3. Atlasiet **Labi**.

![Importētās konfigurācijas Konfigurāciju lapā](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>Parauga ER risinājuma failu priekšskatījums

### <a name="review-the-model-mapping"></a>Pārskatīt modeļa kartēšanu

1. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Veiktspējas uzlabošanas modelis** un pēc tam atlasiet **Veiktspējas uzlabošanas kartēšana**.
2. Darbību rūtī atlasiet **Noformētājs**.
3. Lapā **Datu avota kartējuma modelis** darbību rūtī atlasiet **Noformētājs**.

    Šī ER modeļa kartēšana ir veidota, lai veiktu šādas darbības:

    - Ielādēt tabulā VendTrans saglabāto kreditoru darbību sarakstu (**Trans** datu avots).
    - Katrai darbībai, ielādējiet no tabulas VendTable tā kreditora ierakstu, kuram ir grāmatota darbība (**\#Vend** datu avots).

    > [!NOTE]
    > Datu avots **\#Vend** ir konfigurēts, lai varētu ielādēt atbilstošo kreditora ierakstu, izmantojot esošo daudzkārtējo relāciju **\@.'\>Relācijas'.VendTable\_AccountNum**.

    Modeļa kartēšana šajā konfigurācijā implementē pamatdatu modeli jebkuram no šajā modelī kas ir izveidoti šim modelim un tiek palaisti risinājumā Finance. Tādējādi **Trans** datu avotu saturs ir pakļauts ER formātiem, piemēram, abstraktiem **modelis** datu avotiem.

    ![Trans datu avots Modeļu kartēšanas veidotāja lapā](media/er-calculated-field-ds-performance-mapping-1.png)

4. Aizveriet lapu **Modeļa kartējuma noformētājs**.
5. Aizveriet lapu **Datu avota kartējuma modelis**.

### <a name="review-format"></a>Pārskata formāts

1. Lapā **Konfigurācijas**, konfigurācijas kokā izvērsiet **Veiktspējas uzlabošanas modelis** un pēc tam atlasiet **Veiktspējas uzlabošanas formats**.
2. Darbību rūtī atlasiet **Noformētājs**.
3. Lapā **Formāta veidotājs** cilnē **Kartēšana** atlasiet **Izvērst/Sakļaut**.
4. Izvērst elementus **Modelis**, **Dati** un **Transakcija** .

    Šis ER formāts ir izveidots, lai ģenerētu kreditoru transakciju pārskatu XML formātā.

    ![Formātu datu avoti un konfigurētie formāta elementu saistījumi Formāta veidotāja lapā](media/er-calculated-field-ds-performance-format.png)

5. Aizveriet lapu **Formāta veidotājs**.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Parauga ER risinājuma palaišana, lai izsekotu izpildi

Iedomājieties, ka esat pabeidzis izstrādāt ER risinājuma pirmo versiju. Tagad vēlaties pārbaudīt risinājumu savā FInance instancē un analizēt izpildes veiktspēju.

### <a name="turn-on-the-er-performance-trace"></a>ER veiktspējas izsekošanas ieslēgšana

1. Atlasiet **DEMF** uzņēmumu.
2. Izpildiet darbības, kas aprakstītas [Ieslēgt ER veiktspējas izsekošanu](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) , lai izveidotu veiktspējas izsekošanu, kamēr tiek palaists ER formāts.

    ![Lietotāja parametru dialoglodziņš](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>ER formāta palaišana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas uzlabošanas formāts**.
3. Darbību rūtī atlasiet **Palaist**.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Izmantot veiktspējas izsekošanu, lai analizētu modeļa kartēšanas veiktspēju

1. Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas uzlabošanas kartēšana**.
2. Darbību rūtī atlasiet **Noformētājs**.
3. Lapā **Modeļa kartēšana** darbību rūtī atlasiet **Noformētājs**.
4. Lapā **Modeļa kartējuma noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.
5. Atlasiet pēdējo ģenerēto izsekošanu un pēc tam atlasiet **Labi**.

Tagad ir pieejama jauna informācija par dažiem pašreizējā modeļa kartējuma datu avota vienumiem:

- Faktiskais laiks, kas patērēts, iegūstot datus, izmantojot datu avotu
- Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, palaižot visu modeļa kartējumu

![Izpildes laika informācija Modeļa kartēšanas veidotāja lapā](./media/er-calculated-field-ds-performance-mapping-2.png)

Režģis **Veiktspējas statistika** rāda, ka **Trans** datu avots izsauc VendTrans tabulu vienu reizi. Vērtība **\[265\]\[Q:265\]** no **Trans** datu avota norāda, ka 265 kreditoru darbības ir paņemtas no programmas tabulas un atgrieztas datu modelī.

Režģis **Veiktspējas statistika** arī rāda, ka pašreizējā modeļa kartēšana dublē datu bāzes pieprasījumus, kamēr tiek palaists **\#Vend** datu avots. Šī dublēšana notiek tālāk norādīto iemeslu dēļ.

- Kreditoru tabula tiek izsaukta divas reizes katrai no 265 atkārtotajām kreditora transakcijam, kopā 530 izsaukumi:

    - Viens izsaukums tiek veikts, lai ievadītu kreditora konta numuru.
    - Viens izsaukums tiek veikts, lai ievadītu kreditora vārdu.

- Kreditoru tabula tiek izsaukta katrai no atkārtotajām kreditora transakcijam, pat ja iesniegtās transakcijas ir grāmatotas tikai pieciem kreditoriem. No 530 izsaukumiem 525 ir dublikāti. Sekojošajā attēlā parādīts ziņojums, ko saņemat par dubultajiem izsaukumiem (datu bāzes pieprasījumi).

![Ziņojums par datu bāzes pieprasījumu dublikātiem lapā Modeļa kartējuma noformētājs](./media/er-calculated-field-ds-performance-mapping-2a.png)

Ievērojiet, ka no kopējā modeļa kartēšanas izpildes laika (aptuveni astoņas sekundes) vairāk nekā 80 procenti (aptuveni sešas sekundes) ir izlietoti, izgūstot vērtības no VendTable pieteikumu tabulas. Šis procentuālais daudzums ir pārāk liels diviem piecu kreditoru atribūtiem, salīdzinot ar informācijas apjomu no VendTrans pieteikumu tabulas.

Lai samazinātu to izsaukumu skaitu, kas ir veikti, lai iegūtu detalizētu informāciju par katru transakciju, un lai uzlabotu modeļa kartēšanas veiktspēju, varat izmantot kešošanu **\#Vend** datu avotam.

> [!NOTE]
> Datu avots **Trans\\\#Vend** tiks kešots pašreizējās **Trans** datu avota transakcijas darbības sfēras izpildlaikā.

Kad tiek kešots **\#Vend** datu avots, dublēto izsaukumu skaits tiek samazināts no 525 uz 260, bet dublēšana netiek pilnībā likvidēta. Lai pilnībā izvairītos no dublēšanās, varat konfigurēt jaunu parameterizētu datu avotu veidam **Aprēķinātais lauks** .

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Modeļa kartējuma uzlabošana, pamatojoties uz informāciju no izpildes izsekošanas

### <a name="change-the-logic-of-the-model-mapping"></a>Modeļa kartējuma loģikas mainīšana

Veiciet šīs darbības, lai izmantotu kešatmiņu un **Aprēķinātais lauks** veida datu avotu , lai palīdzētu novērst dubultus izsaukumus uz datu bāzi.

1. Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas uzlabošanas kartēšana**.
2. Darbību rūtī atlasiet **Noformētājs**.
3. Lapā **Modeļa kartēšana** darbību rūtī atlasiet **Noformētājs**.
4. Lapā **Modeļa kartēšanas veidotājs** veiciet tālāk norādītās darbības, lai pievienotu datu avotu veidam **Tabulas ieraksts** , lai piekļūtu ierakstiem VendTable pieteikumu tabulā:

    1. Rūtī **Datu avota veidi** izvērsiet **Dynamics 365 for Operations** un atlasiet **Tabulas ieraksti**.
    2. Atlasiet **Pievienot sakni**.
    3. Dialoglodziņa laukā **Nosaukums** ievadiet **Vend**.
    4. Laukā **Tabula** ievadiet **VendTable**.
    5. Atlasiet **Labi**.

5. Varat parameterizēt izsaukumus uz **Aprēķinātais lauks** veidu datu avotiem tikai tad, ja šie datu avoti atrodas konteinerā. Tāpēc veiciet šīs darbības, lai pievienotu **Tukšs konteineris** veida datu avotu, lai uzglabātu jaunu **Aprēķinātais lauks** veida parameterizētu datu avotu:

    1. Rūtī **Datu avota veidi** izvērsiet **Vispārīgi** un atlasiet **Tukšs konteineris**.
    2. Atlasiet **Pievienot sakni**.
    3. Dialoglodziņa laukā **Nosaukums** ievadiet **Box**.
    3. Atlasiet **Labi**.

    ![Lodziņa datu avots Modeļu kartēšanas veidotāja lapā](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Veiciet šīs darbības, lai pievienotu **Aprēķinātais lauks** veida parameterizētu datu avotu:

    1. Rūtī **Datu avoti** atlasiet **Box**.
    2. Rūtī **Datu avota veidi** izvērsiet **Funkcijas** un atlasiet **Aprēķinātais lauks**.
    3. Atlasiet **Pievienot**.
    4. Dialoglodziņa laukā **Nosaukums** ievadiet **Vend**.
    5. Atlasiet **Rediģēt formulu**.
    6. Lapā **Formulas veidotājs** atlasiet **Parametri** , lai norādītu parametrus, kas ir jāsniedz, kad tiek izsaukts šis datu avots.
    7. Dialoglodziņā **Parametri** atlasiet **Jauns**.
    8. Laukā **Nosaukums** ievadiet **parmVendAccNumber**.
    9. Laukā **Tips** atlasiet **Virkne**.
    10. Atlasiet **Labi**.
    11. Laukā **Formula** ievadiet **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.
    12. Atlasiet **Saglabāt** un aizvēriet lapu **Formulas veidotājs** .
    13. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

7. Veiciet šīs darbības, lai iezīmētu pievienoto datu avotu kā kešoto izpildes laikā:

    1. Rūtī **Datu avoti** atlasiet **Box\\Vend**.
    2. Atlasiet **Kešatmiņa**.

    > [!NOTE]
    > Datu avots **Box\\Vend** tiks kešots visās **Trans** datu avota transakcijas darbības sfēras izpildlaikā.

8. Veiciet šīs darbības, lai atjauninātu ligzdoto **Trans\\\#Vend** datu avotu, lai tas izmantotu **Box\\Vend** datu avotu:

    1. Rūtī **Datu avoti** izvērsiet **Trans**.
    2. Atlasiet **Trans\\\#Vend** datu avotu un pēc tam atlasiet **Rediģēt** \> **Rediģēt formulu**.
    3. Lapā **Formulas veidotājs** laukā **Formula** ievadiet **Box.Vend(\@.AccountNum)**.
    4. Atlasiet **Saglabāt** un pēc tam aizvēriet lapu **Formulas veidotājs**.
    5. Atlasiet **Labi** , lai pabeigtu izmaiņas atlasītajā datu avotā.

9. Atlasiet **Saglabāt**.

    ![Vend datu avots Modeļu kartēšanas veidotāja lapā](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Aizveriet lapu **Modeļa kartējuma noformētājs**.
11. Aizveriet lapu **Modeļa kartējumi**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ER modeļa kartējuma modificētās versijas pabeigšana

1. Lapā **Konfigurācijas**, kopsavilkuma cilnē **Versijas** atlasiet konfigurācijas **Veiktspējas uzlabošanas kartējums** versiju **1.2.**.
2. Atlasiet **Mainīt statusu** \> **Pabeigt**, un pēc tam atlasiet **Labi**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Modificētā ER risinājuma palaišana, lai izsekotu izpildi

Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Izmantot veiktspējas izsekošanu, lai analizētu modeļa kartēšanas pielāgojumus 

1. Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas uzlabošanas kartēšana**.
2. Darbību rūtī atlasiet **Noformētājs**.
3. Lapā **Modeļa kartēšana** darbību rūtī atlasiet **Noformētājs**.
4. Lapā **Modeļa kartējuma noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.
5. Atlasiet pēdējo ģenerēto izsekošanu un pēc tam atlasiet **Labi**.

Ņemiet vērā, ka korekcijas, kuras veicāt modeļa kartējumam, likvidēja datu bāzes vaicājumu dublikātus. Datu bāzu tabulu un datu avotu izsaukumu skaits šim modeļa kartējumam arī ir samazināts.

![Izsekošanas informācija Modeļu kartēšanas veidotāja lapā 1](./media/er-calculated-field-ds-performance-mapping-5.png)

Kopējais izpildes laiks ir samazināts aptuveni 20 reizes (no aptuveni 8 sekundēm līdz aptuveni 400 milisekundēm). Tādēļ tika uzlabota ER risinājuma kopējā veiktspēja.

![Izsekošanas informācija Modeļu kartēšanas veidotāja lapā 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>1. papildinājums: lejupielādēt parauga Microsoft ER risinājuma komponentus

Nepieciešams lejupielādēt tālāk norādītos failus un saglabāt tos lokāli.

| Fails                                        | Saturs |
|---------------------------------------------|---------|
| Veiktspējas uzlabošanas modelis.versija.1     | [Parauga ER datu modeļa konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Veiktspējas uzlabošanas kartējums.versija.1.1 | [Parauga ER modeļa kartējuma konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Veiktspējas uzlabošanas formats.versija.1.1  | [Parauga ER formāta konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>2. papildinājums: ER struktūras konfigurēšana

Pirms sākat lietot ER struktūru, lai uzlabotu parauga Microsoft ER risinājuma veiktspēju, ir jākonfigurē minimāls ER parametru kopums.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurējiet ER parametrus

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.
3. Lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi** iestatiet opciju **Iespējot noformēšanas režīmu** uz **Jā**.
4. Cilnē **Pielikumi** iestatiet šādus parametrus:

    - Laukā **Konfigurācijas** atlasiet veidu **Fails** uzņēmumam **DEMF**.
    - Laukos **Darbu arhīvs**, **Pagaidu**, **Bāzlīnija** un **Citi** atlasiet veidu **Fails**.

Papildinformāciju par ER parametriem skatiet sadaļā [ER struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER konfigurācijas nodrošinātāja aktivizēšana

Katra pievienotā ER konfigurācija tiek atzīmēta kā piederoša ER konfigurācijas nodrošinātājam. Šim nolūkam tiek izmantots ER konfigurācijas nodrošinātājs, kas ir aktivizēts **Elektroniskie pārskati** darbvietā. Tāpēc, pirms sākat pievienot vai rediģēt ER konfigurācijas, jums ir jāaktivizē ER konfigurācijas nodrošinātājs **Elektroniskie pārskati** darbvietā.

> [!NOTE]
> Tikai ER konfigurācijas īpašnieks var rediģēt konfigurāciju. Tāpēc, pirms ER konfigurācija var tikt rediģēta, darbvietā **Elektroniskie pārskati** ir jāaktivizē atbilstošais ER konfigurācijas nodrošinātājs.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER konfigurācijas nodrošinātāju saraksta pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
3. Lapā **Konfigurācijas nodrošinātāju tabula** katram nodrošinātāja ierakstam ir unikāls nosaukums un URL. Pārskatiet šīs lapas saturu. Ja ieraksts **Litware, Inc.** jau pastāv, izlaidiet nākamo procedūru, [Jauna ER konfigurācijas nodrošinātāja pievienošana](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Jauna ER konfigurācijas nodrošinātāja pievienošana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
3. Lapā **Konfigurācijas nodrošinātāji** atlasiet **Jauns**.
4. Laukā **Nosaukums** ievadiet **Litware, Inc.**
5. Laukā **Interneta adrese** ievadiet `https://www.litware.com`.
6. Atlasiet **Saglabāt**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>ER konfigurācijas nodrošinātāja aktivizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** atlasiet elementu **Litware, Inc.** un pēc tam atlasiet **Iestatīt kā aktīvu**.

Papildinformāciju par ER konfigurācijas nodrošinātājiem skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [Elektronisko atskaišu veidošanas (ER) formāta failu izpildes uzraudzīšana, lai novērstu veiktspējas problēmas](trace-execution-er-troubleshoot-perf.md)
- [Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus.](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]