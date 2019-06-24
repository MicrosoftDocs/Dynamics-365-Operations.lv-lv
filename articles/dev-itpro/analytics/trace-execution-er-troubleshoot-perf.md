---
title: ER formāta izpildes izsekošana, lai novērstu veiktspējas problēmas
description: Šajā tēmā ir sniegta informācija par to, kā izmantot veiktspējas izsekošanas līdzekli elektronisko pārskatu veidošanā (ER), lai novērstu veiktspējas problēmas.
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
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
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576550"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>ER formātu izpildes izsekošana, lai novērstu veiktspējas problēmas

[!include[banner](../includes/banner.md)]

Elektronisko pārskatu veidošanas (ER) konfigurāciju izstrādes procesa ietvaros, lai izveidotu elektroniskus dokumentus, nosakiet metodi, kas tiek izmantota, lai iegūtu datus no Microsoft Dynamics 365 for Finance and Operations un ievadītu tos ģenerētajā izvadē. ER veiktspējas izsekošanas līdzeklis palīdz ievērojami samazināt laiku un izmaksas, kas saistītas ar ER formāta izpildes informācijas vākšanu un tās izmantošanu, lai novērstu veiktspējas problēmas. Šajā apmācībā ir sniegti norādījumi par to, kā informāciju par izpildīto ER formātu veiktspējas izsekošanu programmā Finance and Operations var izmantot, lai palīdzētu uzlabot veiktspēju.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai izpildītu šajā apmācībā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.

- Piekļuve programmai Finance and Operations vienai no šīm lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

- Piekļuve Regulatory Configuration Services (RCS) instancei, kas ir nodrošināta tam pašam nomniekam, kuram nodrošināta Finance and Operations instance, vienai no šādām lomām:

    - Elektroniskā pārskata izstrādātājs
    - Elektronisko pārskatu veidošanas funkcionālais konsultants
    - Sistēmas administrators

Nepieciešams arī lejupielādēt un lokāli saglabāt tālāk norādītos failus.

| Fails                                  | Saturs                               |
|---------------------------------------|---------------------------------------|
| Veiktspējas izsekošanas modelis.versija.1     | [Parauga ER datu modeļa konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| Veiktspējas izsekošanas metadati.versija.1  | [Parauga ER metadatu konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| Veiktspējas izsekošanas kartējums.versija.1.1 | [Parauga ER modeļa kartējuma konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Veiktspējas izsekošanas formāts.versija.1.1  | [Parauga ER formāta konfigurācija](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a>Konfigurēt ER parametrus

Katra ER veiktspējas izsekošana, kas tiek ģenerēta programmā Finance and Operations, tiek saglabāta kā izpildes žurnāla ieraksta pielikums. Šo pielikumu pārvaldībai tiek izmantota programmas Finance and Operations dokumentu pārvaldības (Document Management — DM) struktūras. Vispirms ir jākonfigurē ER parametri, lai norādītu DM dokumenta tipu, kas jāizmanto veiktspējas izsekošanas pievienošanai. Programmā Finance and Operations, darbvietā **Elektronisko pārskatu veidošana** atlasiet **Elektronisko pārskatu veidošanas parametri**. Pēc tam lapas **Elektronisko pārskatu veidošanas parametri** cilnes **Pielikumi** laukā **Citi** atlasiet DM dokumenta tipu, kas tiks izmantots veiktspējas izsekošanai.

![Lapa Elektronisko pārskatu veidošanas parametri programmā Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

Lai DM dokumenta tips būtu pieejams uzmeklēšanas laukā **Citi**, tas ir jākonfigurē lapā **Dokumentu tipi** (**Organizācijas administrēšana \> Dokumentu pārvaldība \> Dokumentu tipi**) šādā veidā:

- **Klase:** Pievienot failu
- **Grupa:** Fails

![Lapa Dokumentu tipi programmā Finance and Operations](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Atlasītajam dokumenta tipam jābūt pieejamam ikvienā pašreizējās Finance and Operations instances uzņēmumā, jo DM pielikumi attiecas tikai uz konkrētu uzņēmumu.

### <a name="configure-rcs-parameters"></a>RCS parametru konfigurēšana

ER veiktspējas izsekošana, kas tiek ģenerēta programmā Finance and Operations, tiks importēta RCS analīzes veikšanai, izmantojot ER formāta noformētāju un ER kartēšanas noformētāju. Tā kā ER veiktspējas izsekošana tiek uzglabāta kā izpildes žurnāla ieraksta pielikums, kas ir saistīts ar ER formātu, RCS parametri ir jākonfigurē iepriekš, lai norādītu DM dokumenta tipu, kas jāizmanto veiktspējas izsekošanas pievienošanai. Tādā RCS instancē, kas nodrošināta jūsu uzņēmumam, darbvietā **Elektronisko pārskatu veidošana** atlasiet **Elektronisko pārskatu veidošanas parametri.** Pēc tam lapas **Elektronisko pārskatu veidošanas parametri** cilnes **Pielikumi** laukā **Citi** atlasiet DM dokumenta tipu, kas tiks izmantots veiktspējas izsekošanai.

![Lapa Elektronisko pārskatu veidošanas parametri pakalpojumā RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

Lai DM dokumenta tips būtu pieejams uzmeklēšanas laukā **Citi**, tas ir jākonfigurē lapā **Dokumentu tipi** (**Organizācijas administrēšana \> Dokumentu pārvaldība \> Dokumentu tipi**) šādā veidā:

- **Klase:** Pievienot failu
- **Grupa:** Fails

## <a name="design-an-er-solution"></a>ER risinājuma izstrāde

Pieņemsim, ka esat sācis izstrādāt jaunu ER risinājumu, lai ģenerētu jaunu pārskatu, kurā parādītas kreditoru darbības. Pašlaik varat atrast atlasītā kreditora transakcijas lapā **Kreditoru transakcijas** (pārejiet uz **Parādi kreditoriem \> Kreditori \> Visi kreditori**, atlasiet kreditoru un pēc tam darbību rūtī, cilnē **Kreditors**, grupā **Transakcijas** atlasiet vienumu **Transakcijas**). Tomēr ir nepieciešams, lai visas kreditoru transakcijas vienlaicīgi būtu vienā elektroniskajā dokumentā XML formātā. Šis risinājums sastāv no vairākām ER konfigurācijām, kas ietver nepieciešamo datu modeli, metadatus, modeļa kartējumu un formāta komponentus.

1. Piesakieties RCS instancē, kas nodrošināta jūsu uzņēmumam.
2. Šajā apmācībā jūs izveidosit un modificēsit nepieciešamās konfigurācijas parauga uzņēmumam **Litware, Inc.** Tādēļ pārliecinieties, ka šis konfigurācijas nodrošinātājs ir pievienots RCS un atlasīts kā aktīvs. Norādījumus skatiet procedūrā [Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
4. Lapā **Konfigurācijas** importējiet ER konfigurācijas, kuras lejupielādējāt kā priekšnosacījumu pakalpojumā RCS, šādā secībā: datu modelis, metadati, modeļa kartējums, formāts. Katrai konfigurācijai rīkojieties šādi.

    1. Darbību rūtī atlasiet **Mainīt \> Ielādēt no XML faila**.
    2. Atlasiet **Pārlūkot**, lai atlasītu atbilstošu failu nepieciešamajai ER konfigurācijai XML formātā.
    3. Atlasiet **Labi**.

    ![Lapa Konfigurācijas pakalpojumā RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>Palaidiet ER risinājumu, lai izsekotu izpildi

Pieņemsim, ka esat pabeidzis izstrādāt ER risinājuma pirmo versiju. Tagad vēlaties to pārbaudīt savā FInance and Operations instancē un analizēt izpildes veiktspēju.

### <a id='import-configuration'></a>ER konfigurācijas importēšana no pakalpojuma RCS programmā Finance and Operations

1. Pierakstieties savā Finance and Operations instancē.
2. Šīs apmācības ietvaros importēsit konfigurācijas no savas RCS instances (kur izstrādājat ER komponentus) savā Finance and Operations instancē (kur tos testējat un izmantojat). Tāpēc ir jāpārliecinās, ka ir sagatavoti visi vajadzīgie artefakti. Norādījumus skatiet procedūrā [Importēt elektronisko pārskatu (ER) konfigurācijas no Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).
3. Veiciet šādas darbības, lai importētu konfigurācijas no RCS programmā Finance and Operations.

    1. Darbvietā **Elektronisko pārskatu veidošana**, **Litware, Inc.** konfigurācijas nodrošinātāja elementā atlasiet **Repozitoriji**.
    2. Lapā **Konfigurācijas repozitorijs** atlasiet repozitoriju ar tipu **RCS** un pēc tam atlasiet **Atvērt**.
    3. Kopsavilkuma cilnē **Konfigurācijas** atlasiet konfigurāciju **Veiktspējas izsekošanas formāts**.
    4. Kopsavilkuma cilnē **Versijas** atlasiet atlasītās konfigurācijas versiju **1.1** un pēc tam atlasiet **Importēt**.

    ![Lapa Konfigurācijas repozitorijs programmā Finance and Operations](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

Datu modeļa un modeļa kartējuma konfigurāciju atbilstošās versijas automātiski tiek importētas kā priekšnosacījumi importētajai ER formāta konfigurācijai.

### <a name="turn-on-the-er-performance-trace"></a>ER veiktspējas izsekošanas ieslēgšana

1. Risinājumā Finance and Operations dodieties uz sadaļu **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Dialoglodziņa **Lietotāja parametri** sadaļā **Izpildes izsekošana** rīkojieties šādi.

    1. Laukā **Izpildes izsekošanas formāts** atlasiet vienumu **Atkļūdot izsekošanas formātu**, lai sāktu apkopot informāciju par ER formāta izpildi. Atlasot šo vērtību, veiktspējas izsekošana apkopos informāciju par laiku, kas tiek patērēts šādām darbībām:

        - Katra datu avota palaišana modeļa kartējumā, kas tiek izsaukts datu iegūšanai
        - Katra formāta vienuma apstrāde, lai ievadītu datus ģenerētajā izvadē

        Lauku **Izpildes izsekošanas formāts** izmanto, lai norādītu ģenerētās veiktspējas izsekošanas formātu, kurā tiek uzglabāta izpildes informācijas ER formāta un kartēšanas elementiem. Atlasot kā vērtību **Atkļūdot izsekošanas formātu**, varēsit analizēt izsekošanas saturu ER operāciju noformētājā un skatīt ER formāta vai kartēšanas elementus, kas minēti izsekošanā.

    2. Iestatiet tālāk minētajām opcijām vienumu **Jā**, lai apkopotu noteiktu informāciju par ER modeļa kartējuma un ER formāta komponentu izpildi:

        - **Apkopot vaicājumu statistiku** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota šāda informācija:

            - Datu avotu veikto datu bāzes izsaukumu skaits
            - Datu bāzes dublētu izsaukumu skaits
            - Informācija par SQL priekšrakstiem, kas izmantoti datu bāzes izsaukumu veikšanai

        - **Izsekot kešdarbes piekļuvi** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par ER modeļa kartējuma kešatmiņas izmantošanu.
        - **Izsekot datu piekļuvi** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par datu bāzes izsaukumu skaitu izpildītajiem datu avotiem, kas atbilst tipam “ierakstu saraksts”.
        - **Izsekot saraksta uzskaitījumu** — ja šī opcija ir ieslēgta, veiktspējas izsekošanā tiks apkopota informācija par ierakstu skaitu, kas pieprasīti no datu avotiem, kuri atbilst tipam “ierakstu saraksts”.

    > [!NOTE]
    > Parametri dialoglodziņā **Lietotāja parametri** dialoglodziņā ir raksturīgi lietotājam un pašreizējam uzņēmumam.

    ![Dialoglodziņš Lietotāja parametri programmā Finance and Operations](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a>ER formāta palaišana

1. Programmā Finance and Operations atlasiet uzņēmumu **DEMF**.
2. Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas izsekošanas formāts**.
4. Darbību rūtī atlasiet **Palaist**.

Ņemiet vērā, ka ģenerētajā failā ir ietverta informācija par 265 transakcijām sešiem kreditoriem.

## <a name="review-the-execution-trace"></a>Izpildes izsekošanas pārskatīšana

### <a id='export-trace'></a>Eksportēt ģenerēto izsekošanu no programmas Finance and Operations

Veiktspējas izsekošana ir atdalīta no avota ER formāta, un to var serializēt ārējā zip failā.

1. Risinājumā Finance and Operations dodieties uz sadaļu **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas atkļūdošanas žurnāli**.
2. Lapā **Elektronisko pārskatu palaišanas žurnāli**, kreisajā rūtī, laukā **Konfigurācijas nosaukums** atlasiet **Veiktspējas izsekošanas formāts**, lai atrastu žurnāla ierakstus, kas ģenerēti, izpildot konfigurāciju **Veiktspējas izsekošanas formāts**.
3. Atlasiet pogu **Pielikumi** (papīra saspraudes simbols) lapas augšējā labajā stūrī vai nospiediet **Ctrl+Shift+A**.

    ![Poga Pielikumi lapā Elektronisko pārskatu palaišanas žurnāli programmā Finance and Operations](./media/GER-PerfTrace-GER-DebugLog.png)

4. Lapas **Elektronisko pārskatu palaišanas žurnālu pielikumi** darbību rūtī atlasiet **Atvērt**, lai iegūtu veiktspējas izsekošanu kā zip failu un saglabātu to lokāli.

    ![Lapa Elektronisko pārskatu palaišanas žurnālu pielikumi programmā Finance and Operations](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Ģenerētajai izsekošanai ir atsauce uz avota ER pārskatu, izmantojot unikālu pārskata identifikatoru tikai **GUID** formātā. Formāta versijas numerācija netiek ņemta vērā.

Ņemiet vērā, ka saistība starp veiktspējas izsekošanu, kas ir ģenerēta izpildītajam ER formātam, un ER modeļa kartējumu ir balstīta uz izmantoto saknes deskriptoru un kopējo datu modeli. Formāta un modeļa kartējuma versijas numerācija netiek ņemta vērā. Modeļa kartējuma karodziņa **Modeļa kartējuma noklusējums** iestatījums arī netiek ņemts vērā.

### <a id='import-trace'></a>Importēt ģenerēto izsekošanu RCS

1. Pakalpojuma RCS darbvietā **Elektroniskie pārskati** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurāciju kokā izvērsiet vienumu **Veiktspējas izsekošanas modelis** un atlasiet vienumu **Veiktspējas izsekošanas formāts**.
3. Darbību rūtī atlasiet **Noformētājs**.
4. Lapā **Formāta noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.
5. Dialoglodziņā **Veiktspējas izsekošanas rezultātu iestatījumi** atlasiet **Importēt veiktspējas izsekošanu**.
6. Atlasiet **Pārlūkot**, lai atlasītu zip failu, ko iepriekš eksportējāt no programmas Finance and Operations.
7. Atlasiet **Labi**.

    ![Dialoglodziņš Veiktspējas izsekošanas rezultātu iestatījumi pakalpojumā RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — formāta izpilde

1. Pakalpojumā RCS, lapā **Formāta noformētājs** atlasiet **Izvērst/sakļaut**, lai izvērstu visu formāta vienumu saturu.

    Ņemiet vērā, ka dažiem pašreizējā formāta vienumiem tiek rādīta papildu informācija:

    - Faktiskais laiks, kas patērēts, ievadot datus ģenerētajā izvadē, izmantojot formāta vienumu
    - Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, ģenerējot visu izvadi

    ![Formāta noformētāja lapa pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Aizveriet lapu **Formāta noformētājs**.

### <a id='use-trace'></a>Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums

1. Pakalpojuma RCS lapā **Konfigurācijas**, konfigurāciju kokā atlasiet vienumu **Veiktspējas izsekošanas kartējums**.
2. Darbību rūtī atlasiet **Noformētājs**.
3. Atlasiet **Noformētājs**.
4. Lapā **Modeļa kartējuma noformētājs**, darbību rūtī atlasiet **Veiktspējas izsekošana**.
5. Atlasiet iepriekš importēto izsekošanu.
6. Atlasiet **Labi**.

Ņemiet vērā, ka kļūst pieejama jauna informācija par dažiem pašreizējā modeļa kartējuma datu avota vienumiem:

- Faktiskais laiks, kas patērēts, iegūstot datus, izmantojot datu avotu
- Tas pats laiks, kas izteikts procentos no kopējā laika, kurš patērēts, palaižot visu modeļa kartējumu

Ņemiet vērā, ka ER jūs informē par to, ka pašreizējais modeļa kartējums dublē datu bāzes pieprasījumus, kamēr tiek izpildīts VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avots. Šāda dublēšana notiek tāpēc, ka kreditoru transakciju saraksts tiek izsaukts divas reizes katram atkārtotajam kreditora ierakstam:

- Viens izsaukums tiek veikts, lai ievadītu informāciju par katru transakciju datu modelī, pamatojoties uz konfigurētajiem saistījumiem.
- Viens izsaukums tiek veikts, lai ievadītu aprēķināto transakciju skaitu katram kreditoram datu modelī.

![Ziņojums par datu bāzes pieprasījumu dublikātiem lapā Modeļa kartējuma noformētājs pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

Vērtība **\[Q:530\]** norāda, ka VendTrans tabula tika izsaukta 530 reizes, lai atgrieztu ierakstu no šīs tabulas uz VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avotu. Vērtība **\[530\]** norāda, ka VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avots tika izsaukts 530 reizes, lai atgrieztu ierakstu no šī datu avota un ievadītu tā informāciju datu modelī.

Ieteicams izmantot kešdarbi VendTable/\<Relations/VendTrans.VendTable\_AccountNum datu avotam, lai samazinātu izsaukumu skaitu, kas veikti, lai iegūtu informāciju par 265 transakcijām un palīdzētu uzlabot modeļa kartējuma veiktspēju.

Tas arī var būt noderīgi, lai samazinātu LedgerTransTypeList datu avotam veikto izsaukumu skaitu. Šis datu avots tiek izmantots, lai katru **LedgerTransType** uzskaitījuma vērtību saistītu ar tā etiķeti. Izmantojot šo datu avotu, varat atrast atbilstošu etiķeti un ievadīt to katras kreditora transakcijas datu modelī. Pašreizējais izsaukumu skaits šim datu avotam (9027) ir diezgan liels 265 transakcijām.

![Lapa Modeļa kartējuma noformētājs pakalpojumā RCS, kurā norādīti 9027 izsaukumi uz datu avotu](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Modeļa kartējuma uzlabošana, pamatojoties uz informāciju no izpildes izsekošanas

### <a name="modify-the-logic-of-the-model-mapping"></a>Modeļa kartējuma loģikas modificēšana

1. Veiciet šīs darbības, lai izmantotu kešdarbi, lai palīdzētu novērst dublētus izsaukumus datu bāzē.

    1. Pakalpojuma RCS lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avoti** atlasiet vienumu **VendTable**.
    2. Atlasiet **Kešatmiņa**.
    3. Izvērsiet vienumu **VendTable**, izvērsiet “viens pret daudziem” relāciju sarakstu VendTable datu avotam (vienums **\<Relācijas**) un atlasiet vienumu **VendTrans.VendTable\_AccountNum**.
    4. Atlasiet **Kešatmiņa**.

    ![Kešdarbes iestatīšana, lai palīdzētu novērst dublētus izsaukumus](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Veiciet šīs darbības, lai LedgerTransTypeList datu avotu iekļautu VendTable datu avota tvērumā.

    1. Rūtī **Datu avota tipi** izvērsiet vienumu **Funkcijas** un atlasiet vienumu **Aprēķinātais lauks**.
    2. Rūtī **Datu avoti** atlasiet vienumu **VendTable**.
    3. Atlasiet **Pievienot**.
    4. Laukā **Nosaukums** ievadiet **\$TransType**.
    5. Atlasiet **Rediģēt formulu**.
    6. Laukā **Formula** ievadiet **LedgerTransTypeList**.
    7. Atlasiet **Saglabāt**.
    8. Aizveriet lapu **Formulas redaktors**.
    9. Noklikšķiniet uz **Labi**.

3. Veiciet šīs darbības, lai veiktu lauka **\$TransType** kešdarbi.

    1. Atlasiet vienumu **LedgerTransTypeList**.
    2. Atlasiet **Kešatmiņa**.
    3. Atlasiet vienumu **VendTable.\$TransType**.
    4. Atlasiet **Kešatmiņa**.

    ![Kešdarbes iestatīšana laukam $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Veiciet šīs darbības, lai mainītu lauku **\$TransTypeRecord**, lai tas sāktu izmantot kešoto lauku **\$TransType**.

    1. Rūtī **Datu avoti** izvērsiet vienumu **VendTable**, izvērsiet vienumu **\<Relācijas**, izvērsiet vienumu **VendTrans.VendTable\_AccountNum** un atlasiet vienumu **VendTable.VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.
    2. Atlasiet **Rediģēt**.
    3. Atlasiet **Rediģēt formulu**.
    4. Laukā **Formula** atrodiet šādu izteiksmi:

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. Laukā **Formula** ievadiet šādu izteiksmi:

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Atlasiet **Saglabāt**.
    7. Aizveriet lapu **Formulas redaktors**.
    8. Atlasiet **Labi**.

5. Atlasiet **Saglabāt**.
6. Aizveriet lapu **Modeļa kartējuma noformētājs**.
7. Aizveriet lapu **Modeļa kartējumi**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ER modeļa kartējuma modificētās versijas pabeigšana

1. Pakalpojuma RCS lapā **Konfigurācijas**, kopsavilkuma cilnē **Versijas** atlasiet konfigurācijas **Veiktspējas izsekošanas kartējums** versiju **1.2**.
2. Atlasiet **Mainīt statusu**.
3. Atlasiet **Pabeigt**.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a>Modificētās ER modeļa kartējuma konfigurācijas importēšana no RCS programmā Finance and Operations

Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER konfigurācijas importēšana no pakalpojuma RCS programmā Finance and Operations](#import-configuration) minētās darbības, lai importētu konfigurācijas **Veiktspējas izsekošanas kartējums** versiju 1.2 programmā Finance and Operations.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Modificētā ER risinājuma palaišana, lai izsekotu izpildi

### <a name="run-the-er-format"></a>ER formāta palaišana

Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.

## <a name="review-the-execution-trace"></a>Izpildes izsekošanas pārskatīšana

### <a name="export-the-generated-trace-from-finance-and-operations"></a>Eksportēt ģenerēto izsekošanu no programmas Finance and Operations

Atkārtojiet šīs tēmas iepriekšējā sadaļā [Eksportēt ģenerēto izsekošanu no programmas Finance and Operations](#export-trace) minētās darbības, lai saglabātu jaunu veiktspējas izsekošanu lokāli.

### <a name="import-the-generated-trace-into-rcs"></a>Importēt ģenerēto izsekošanu RCS

Atkārtojiet šīs tēmas iepriekšējā sadaļā [Importēt ģenerēto izsekošanu RCS](#import-trace) minētās darbības, lai importētu jauno veiktspējas izsekošanu pakalpojumā RCS.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums

Atkārtojiet šīs tēmas iepriekšējā sadaļā [Veiktspējas izsekošanas izmantošana analīzes veikšanai pakalpojumā RCS — modeļa kartējums](#use-trace) minētās darbības, lai analizētu jaunāko veiktspējas izsekošanu.

Ņemiet vērā, ka korekcijas, kuras veicāt modeļa kartējumam, likvidēja datu bāzes vaicājumu dublikātus. Datu bāzu tabulu un datu avotu izsaukumu skaits šim modeļa kartējumam arī ir samazināts. Tādēļ ir uzlabojusies ER risinājuma kopējā veiktspēja.

![Izsekot informāciju par VendTable datu avotu lapā Modeļa kartējuma noformētājs pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

Izsekošanas informācijā VendTable datu avota vērtība **\[12\]** norāda, ka šis datu avots tika izsaukts 12 reizes. Vērtība **\[Q:6\]** norāda, ka seši izsaukumi tika pārveidoti par datu bāzes izsaukumiem uz VendTable tabulu. Vērtība **\[C:6\]** norāda, ka ieraksti, kas tika ienesti no datu bāzes, tika kešoti, un seši citi izsaukumi tika apstrādāti, izmantojot kešatmiņu.

Ņemiet vērā, ka LedgerTransTypeList datu avota izsaukumu skaits ir samazināts no 9027 līdz 240.

![Izsekot informāciju par LedgerTransTypeList datu avotu lapā Modeļa kartējuma noformētājs pakalpojumā RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a>Pārskatīt izpildes izsekošanu programmā Finance and Operations

Papildus pakalpojumam RCS dažas Finance and Operations versijas var nodrošināt ER struktūras noformētāja iespējas. Šīm Finance and Operations versijām ir opcija **Iespējot noformēšanas režīmu**, ko var ieslēgt. Šo opciju var atrast lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi**, kuru varat atvērt, izmantojot darbvietu **Elektronisko pārskatu veidošana**.

![Opcija Iespējot noformēšanas režīmu lapā Elektronisko pārskatu veidošanas parametri programmā Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Ja izmantojat vienu no šīm Finance and Operations versijām, varat analizēt ģenerēto veiktspējas izsekošanu informāciju tieši programmā Finance and Operations. Tās nav jāeksportē no Finance and Operations un jāimportē pakalpojumā RCS.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Pārskatīt izpildes izsekošanu, izmantojot ārējos rīkus

### <a name="configure-user-parameters"></a>Konfigurēt lietotāja parametrus

1. Risinājumā Finance and Operations dodieties uz sadaļu **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.
2. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
3. Dialoglodziņā **Lietotāja parametri**, sadaļā **Izpildes izsekošana**, laukā **Izpildes izsekošanas formāts** atlasiet **PerfView XML.**

### <a name="run-the-er-format"></a>ER formāta palaišana

Atkārtojiet šīs tēmas iepriekšējā sadaļā [ER formāta palaišana](#run-format) minētās darbības, lai ģenerētu jaunu veiktspējas izsekošanu.

Ņemiet vērā, ka tīmekļa pārlūkprogramma piedāvā lejupielādēt zip failu. Šis fails satur veiktspējas izsekošanu PerfView formātā. Pēc tam varat izmantot PerfView veiktspējas analīzes rīku, lai analizētu ER formāta izpildes informāciju.