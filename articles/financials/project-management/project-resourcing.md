---
title: "Projekta resursu sadalījums"
description: "Šajā tēmā ir sniegta informācija par projekta resursu sadalījumu."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8139134ed230cc1525c698fadb20309afee0a68f
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="project-resourcing"></a>Projekta resursu sadalījums

[!include[banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par projekta resursu sadalījumu.

Viens no izaicinājumiem, ar ko projektu vadītāji un resursu pārvaldnieki saskaras projekta plānošanas posma laikā, ir resursu sadalījums, kura ietvaros viņiem ir jānosaka un jārezervē darbam projektā vajadzīgais resurss. Programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition projektu resursu sadalījuma iespējas jums ļauj definēt lomas, kas tiek uzskatītas par pagaidu resursiem, kurus var rezervēt noteiktai piesaistei vai piesaistes daļai. Šāds resursu sadalījuma veids ļauj projektu vadītājiem un resursu pārvaldniekiem veikt šādus uzdevumus:

- Definēt lomu, kurai ir nepieciešamās kompetences, lai varētu vienkārši noteikt resursu atbilstību.
- Izmantot lomas, lai definētu sākotnējo iesaistes grafiku, pamatojoties uz rezervētajiem resursiem.
- Novērtēt izmaksas un noteikt sākotnējo budžetu, pamatojoties uz piešķirtajām lomām un projekta resursiem.
- Izmantot lomas, lai noteiktu to resursu rezervāciju skaitu, kas ir nepieciešamas katrai iesaistei.
- Novērtēt resursu skaitu, kas ir nepieciešami visā projekta dzīves ciklā.
- Izstrādāt darba sadalījuma struktūras (WBS) projektu, izmantojot sākotnējo resursu piešķires.

[![Projekta dzīves cikls](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Projekta plānošanas gaitā ieplānotos resursus var aizstāt ar personāla resursiem. Projektu vadītājs jebkurā projekta posmā var arī atgriezties un atjaunināt resursu rezervācijas.

## <a name="set-up-project-resources"></a>Projekta resursu iestatīšana
Ir jāiestata kalendārs un jāsaista tas ar darbinieku vai nodarbināto. Kalendārs tiek izmantots, lai plānotu projektu un projektam rezervēto resursu darba laiku. Kalendāra iestatīšanas laikā projektu vadītāji resursu optimizēšanas ietvaros var veikt resursu izlīdzināšanu. Pamatojoties uz kalendāra grafiku, resursiem var noteikt ierobežojumus. Kalendāru varat iestatīt lapā **Kalendāri**.

Kad kādu nodarbināto iestatāt kā projekta resursu, varat atlasīt no nodarbinātajiem, kuri strādā uzņēmumā, kam iestatāt resursus. Varat arī atlasīt nodarbinātos no citiem uzņēmumiem jūsu organizācijā. Šie nodarbinātie tiek saukti par starpuzņēmumu resursiem.

Tālāk sniegtajos procedūru aprakstos ir paskaidrots, kā nodarbināto iestatīt kā projekta resursu jūsu uzņēmumā un kā iestatīt starpuzņēmumu projekta resursu.

### <a name="set-up-a-worker-as-a-project-resource"></a>Nodarbinātā kā projekta resursa iestatīšana

1. Lapas **Darbinieki** sarakstā **Nodarbinātie** atlasiet nodarbināto, kuru pievienojat kā projekta resursu, un atveriet nodarbinātā ierakstu.
2. Darbību rūtī atlasiet **Projekts** &gt; **Iestatījumi** &gt; **Projektu iestatījumi**.
3. Atlasiet kalendāru un pēc tam aizveriet lapu.

Jūs varat arī norādīt resursam noklusējuma projektus kā iepriekšēju piešķiri. Iepriekšējas piešķires var izmantot, ja resursu pārvaldnieks vai projektu vadītājs iepriekš zina, kurā projektā resurss veiks darbu. Iepriekšējas piešķires arī var balstīties uz projekta sponsora vai debitora pieprasījumu. Lai veiktu projekta iepriekšēju piešķiri, lapas **Piešķirt projektus** cilnes **Projekti** sarakstā **Atlikušie projekti** atlasiet attiecīgo projektu.

### <a name="set-up-an-intercompany-resource"></a>Starpuzņēmumu resursa iestatīšana

Kad nodarbināto iestatāt kā starpuzņēmumu resursu, iestatīšana ir jāveic gan patapināšanas uzņēmumā, gan piesaistīšanas uzņēmumā.

**Patapināšanas uzņēmumā**

1. Programmā Finance and Operations pārbaudiet, vai ir atlasīts patapināšanas uzņēmums, un pēc tam veiciet iepriekšējā sadaļā “Nodarbinātā kā projekta resursa iestatīšana” aprakstīto procedūru.
2. Lapā **Starpuzņēmumu uzskaite** atlasiet **Jauns**.
3. Laukā **Juridiskās personas ID** atlasiet patapināšanas uzņēmumu. Aizpildiet pārējos laukus ar atbilstošu informāciju un pēc tam atlasiet **Saglabāt**.
4. Lapā **Transfertcena** atlasiet **Jauns**.
5. Laukā **Piesaistīšanas juridiskā persona** atlasiet atbilstošo uzņēmumu.
6. Lai piesaistīšanas uzņēmumam aizdotu tikai to resursu, kuru izveidojāt šīs sadaļas sākumā, laukā **Resurss** atlasiet izveidotā resursa nosaukumu. Lai piesaistīšanas uzņēmumam būtu pieejami visi patapināšanas uzņēmuma resursi, lauks **Resurss** ir jāatstāj tukšs.
7. Lapā **Projektu vadības un uzskaites parametri**, cilnē **Starpuzņēmumu** opciju **Aktivizēt starpuzņēmumu resursu plānošanu un laika grafikus** iestatiet uz **Jā**.

**Piesaistīšanas uzņēmumā**

- Lapā **Resursu saraksts**, meklēšanas filtrā ievadiet tā resursu nosaukumu, kuru izveidojāt patapināšanas uzņēmumam, lai pārbaudītu, vai šis nosaukums ir ietverts piesaistīšanas uzņēmuma resursu sarakstā.

## <a name="manage-resource-competencies"></a>Resursu kompetenču pārvaldība
Resursu kompetencēm ir būtiska nozīme resursu vadības procesā. Kompetences var izmantot kā bāzlīniju, lai noteiktu resursus, kuriem ir atbilstošā prasmju, izglītības, sertifikācijas un projektu pieredzes attiecība. Šī informācija ir jāiestata katram resursam un tā regulāri jāatjaunina. Šādā veidā var palielināt iespējas, kad konkrētas resursu kompetences tiek saskaņotas laikā projekta resursu piešķires laikā.

[![Prasmju, sertifikāciju, izglītības un projektu pieredzes piemēri](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Tālāk minētajās procedūrās ir paskaidrots, kā iestatīt dažas resursu kompetences.

Lai iestatītu nodarbinātā kompetences, var izmantot saraksta lapu **Nodarbinātie** modulī Personāla vadība vai saraksta lapu **Resursi** modulī Projektu vadība un uzskaite. Tālāk norādītajām procedūrām tiek izmantota saraksta lapa **Nodarbinātie** modulī Personāla vadība.

### <a name="set-up-competencies-certificates"></a>Kompetenču iestatīšana: sertifikāti

1. Saraksta lapā **Nodarbinātie** atlasiet rindu tam nodarbinātajam, kuram pievienot sertifikāta informāciju.
2. Darbību rūts cilnē **Nodarbinātais**, grupā **Kompetences** atlasiet **Sertifikāti**.
3. Atlasiet **Jauns** un pēc tam laukā **Sertifikāta tips** atlasiet **PMP**.
4. Laukā **Sākuma datums** atlasiet **01.10.2015** un atlasiet **Saglabāt**.

### <a name="set-up-competencies-skills"></a>Komptenču iestatīšana: prasmes

1. Saraksta lapā **Nodarbinātie** pārbaudiet, vai iepriekšējā procedūrā izmantotais nodarbinātais joprojām ir atlasīts. Pēc tam darbību rūts cilnē **Nodarbinātais**, grupā **Kompetences** atlasiet **Prasmes**.
2. Atlasiet **Jauns**.
3. Laukā **Prasme** atlasiet **Projektu vadība**.
4. Laukā **Līmenis** atlasiet **5 Eksperta līmenis**.
5. Laukā **Līmeņa datums** atlasiet **14.01.2014.**.
6. Laukā **Pieredzes gadu skaits** ievadiet **10**.
7. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.

## <a name="create-a-new-project"></a>Izveidot jaunu projektu
1. Lapā **Projektu vadība** atlasiet **Jauns projekts** un ievadiet tālāk norādītās vērtības.

    - **Projekta veids:** Laiks un materiāls
    - **Projekta nosaukums:** XYZ jaunināšanas fāze 2
    - **Projektu grupa:** TM\_WIP
    - **Projekta līguma ID:** 00000002

2. Atlasiet **Izveidot projektu**.

### <a name="assign-a-resource-to-a-project"></a>Resursa piešķiršana projektam

1. Lapa **Nodarbinātie**, sarakstā **Nodarbinātie** atlasiet tāda nodarbinātā ierakstu, kuram iepriekš veicāt kompetenču iestatīšanu, un atveriet šī nodarbinātā ierakstu.
2. Darbību rūts cilnē **Projekts**, grupā **Iestatījumi** atlasiet **Piešķirt projektus**.
3. Lapā **Resursa apstiprināšanas projektu piešķires**, cilnē **Projekti**, laukā **Pievienot projektu atlasītajiem projektiem** filtrējiet pēc projekta **XYZ jaunināšanas fāze 2**.
4. Rūtī **Atlikušie projekti** atlasiet kādu projektu un pēc tam atlasiet bultiņas pogu, lai to pievienotu rūtī **Atlasītie projekti**.

Ja nepieciešams, resursam varat piešķirt arī kategorijas. Kategorijas tips ir **Izmaksas** vai **Ieņēmumi**. Kategorijas tipu nosaka jūsu organizācija. Ja resursam nav piešķirta neviena kategorija, tad programmā Finance and Operations tiek uzmeklēta noklusējuma kategorija izmaksu un ieņēmumu stundu likmēm.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projekta resursu un lomu īpašību iestatīšana

Projekta vadītājs var izmantot projekta resursu sadalījuma funkcionalitāti, lai izveidotu lomas, kas nepieciešamas projektam. Lomas var izmantot, ja resursu rezervēšanas laikā apstiprinātie resursi joprojām nav zināmi. Lomas var uz laiku rezervēt kā ieplānotos resursus, lai varētu turpināt projekta plānošanas posmus.

[![Lomas piemērs](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenārijs:** Contoso tika nolīgts, lai pabeigtu laika un materiālu projektu, kuram ir apstiprināta projekta privilēģijas. Jaunākais projektu vadītājs joprojām strādā pie projekta darba apjoma pabeigšanas. Resursu pārvaldnieks pašlaik norāda konkrētus resursus, kas tiks rezervēti darbam ar jauno projektu. Tā kā attiecīgais projekts ir ļoti svarīgs, projekta sponsors kā vienu no lomām pieprasīja lomu Vecākais projektu vadītājs. Resursu pārvaldniekam ir jāiegūst jaunais resurss un sistēmā jādefinē loma, lai tā būtu pieejama gadījumā, ja jaunākajam projektu vadītājam projekta plānošanas laikā ir nepieciešama resursa informācija.

Tālāk sniegtajos darbību aprakstos ir norādīts, kā resursu pārvaldnieks var iestatīt lomu Vecākais projektu vadītājs un piesaistīt tai resursa īpašības. Pēc tam šo lomu var izmantot, lai meklētu pieejamos resursus, kas atbilst nepieciešamajām resursu kompetencēm.

1. Lapā **Lomu iestatīšana** atlasiet **Jauns** un ievadiet tālāk norādītās vērtības.

    - **Lomas ID:** Vecākais projektu vadītājs
    - **Apraksts:** Vecākais projektu vadītājs

2. Atlasiet **Izveidot**.
3. Atlasiet lomu **Vecākais projektu vadītājs** un pēc tam atlasiet **Konfigurēt īpašības**.
4. Laukā **Īpašību veids** atlasiet **Prasme**.
5. Laukā **Pieejamās īpašības** ievadiet meklējamo prasmi.
6. Laukā **Īpašību veids** atlasiet **Sertifikāts**.
7. Laukā **Pieejamās īpašības** ievadiet meklējamo sertifikātu.

### <a name="assign-a-project-resource-to-a-project"></a>Projekta resursa piešķiršana projektam

1. Lapā **Visi projekti** atlasiet projektu **XYZ jaunināšanas fāze 2**.
2. Cilnē **Projekta grupa un plānošana** atlasiet **Pievienot**.
3. Laukā **Loma** atlasiet **Grupas dalībnieks**.
4. Atlasiet **Rezervēt no kalendāra**.
5. Lapā **Resursu pieejamība** atlasiet **Skata iestatījumi**.
6. Lapā **Pielāgojiet skata iestatījumus** ievadiet šādas vērtības:

    - **Datumu diapazona skata formāts:** Diena
    - **Parādīt pieejamības aprakstus:** Jā
    - **Rādīt atlikušo noslodzi:** Jā

7. Resursu sarakstā atlasiet resursu.
8. Atlasiet **Stingrā rezervēšana** un **Visa noslodze**.


### <a name="assign-a-resource-to-a-default-role"></a>Resursa piešķiršana noklusējuma lomai

Lai palīdzētu projektu vadītājiem vai resursu pārvaldniekiem, varat detalizētāk rādīt resursus, ko var rezervēt projektam. Noklusējuma lomu var saistīt ar esošu resursu vai jauniegūtu resursu. Piemēram, kad Rihards tika pieņemts darbā, viņa pieredze un prasmes bija piemērotas lomai Biznesa analītiķis. Resursu pārvaldnieks piešķīra šo lomu kā Rihards noklusējuma lomu. Tādējādi resursu pārvaldnieks pievienoja Danielu to biznesa analītiķu kopai, kuri ir pieejami darbam projektā.

Resursu rezervēšanas laikā projektu vadītāji var filtrēt lomu resursus, kas ir pieejami darbam projektos. Viņi var izmantot šo informāciju kā vienu kritēriju, veicot vairāku kritēriju lēmumu analīzi resursu izpildes laikā. Viņi var pievienot arī citas resursa īpašības filtram, lai meklētu resursus, kuriem ir īpašas prasmes, izglītība un pieredze attiecīgajam projektam.

**Scenārijs:** ir uzsākts apstiprināts projekts, un loma Vecākais projektu vadītājs ir rezervēta kā ieplānots resurss projekta plānošanas posma laikā. Resursu pārvaldnieks ir ieguvis resursu, lai aizpildītu lomu Vecākais projektu vadītājs.

1. Lapā **Resursu saraksts** atlasiet **Rihards Taurenis**.
2. Lapā **Resursa loma** atlasiet **Jauns** un ievadiet tālāk norādītās vērtības.

    - **Ir spēkā:** ievadiet pašreizējo datumu.
    - **Termiņa beigas:** ievadiet **Nekad**.
    - **Loma:** ievadiet **Vecākais projektu vadītājs**.

3. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
4. Cilnē **Kompetences** pievienojiet prasmi **ProjectMgmt** un sertifikātu **PMP**.

## <a name="set-up-role-based-pricing"></a>Uz lomu balstītas cenu noteikšanas iestatīšana
Visas izmaksu, pārdošanas un pārsūtīšanas cenas var iestatīt lomām.

1. Lapā **Pārdošanas cena (stunda)** atlasiet **Jauns** un ievadiet spēkā stāšanās datumu.
2. Kolonnā **Loma** atlasiet lomu.
3. Kolonnā **Cenu noteikšana** ievadiet cenu atlasītajai resursu lomai.

## <a name="form-a-project-team"></a>Projekta grupas veidošana
Lai lietotu lomas, kas iepriekš tika iestatītas projektā, projektu vadītājam šīs lomas ir jāsaista ar projektu. Projektam var piešķirt vairākas lomas. Lai nerastos pārpratumi, rezervēšanas laikā programma Finance and Operations šīm lomām etiķetes piešķir automātiski. Piemēram, ja projektu vadītājam ir nepieciešami trīs programmatūras inženieri, tiek automātiski ģenerētas trīs lomas Programmatūras inženieris, kuru etiķetes ir **1. programmatūras inženieris**, **2. programmatūras inženieris** un **3. programmatūras inženieris**. Ja lomai iepriekš tika iestatītas lomas īpašības, tās tiek pielietotas kā filtrs resursu meklēšanas laikā. Lai precizētu meklēšanu, nepieciešamības gadījumā var pievienot papildu īpašības.

Skata iestatījumus arī var pielāgot, lai nodrošinātu labāku pārskatu par resursu pieejamību. Ir pieejamas iespējas stundu, dienu, nedēļu, ceturkšņu un gada pieejamības attēlošanai. Pastāv arī iespēja rādīt pieejamo un atlikušo resursu noslodzi. Šī opcija ir noderīga laika pārvaldībai, kad novērtējat darbībām pieejamo laiku vai resursu pieejamību.

Projektu vadītājs var lapā atlasīt lomu un pēc tam, ja ir pieejams resurss, kas atbilst vajadzībai, viņš var rezervēt resursu šai lomai. Ņemiet vērā, ka šajā plānošanas posmā resursi nav jārezervē. Veidojot WBS, lomas var aizstāt ar projekta personāla resursiem. Ja WBS ietvaros lomas tiek aizstātas ar personāla resursiem, resursu iestatījumos tiek automātiski atjaunināts projekta grupas saraksts un plānošana.

[![Projekta grupas saraksts, kurā ir ietvertas gan lomas, gan faktiskie resursi](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektu vadītājam ir dažādas iespējas projekta resursu rezervācijai, piemēram, **Atlikusī noslodze**, **Pilna noslodze**, **Noslodzes procentuālā daļa** un **Norādiet stundas**. Šīs rezervēšanas iespējas var atcelt jebkurā laikā, ja mainās resursu piešķires. Tiek atbalstīti divi rezervāciju tipi:

- **Stingrā rezervācija** — resursa rezervācija ir apstiprināta darbam attiecīgajā iesaistē uz norādīto laiku.
- **Vieglā rezervēšana** — resursu rezervācijas ir uz laiku iestatītas darbam attiecīgajā iesaistē uz norādīto laiku.

Tālāk esošajā procedūrā izskaidrots, kā izveidot projekta grupu.

### <a name="create-a-project-team"></a>Projekta grupas izveide

1. Saraksta lapā **Visi projekti** atlasiet kādu projektu un pēc tam atlasiet **Rediģēt**.
2. Cilnes **Projekta grupa un plānošana** laukā **Grafika beigu datums** ievadiet grafika sākuma datumu, kam ir pieskaitīts viens mēnesis. Piemēram, ja grafika sākuma datums ir 2017. gada 24. jūnijs (24/06/2017), ievadiet **24/07/2017**.
3. Atlasiet **Pievienot**.
4. Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Vecākais projektu vadītājs**.
5. Atlasiet **Nepieciešamās kompetences**.
6. Lapā **Īpašību izvēle** īpašības, ko iepriekš iestatījāt lomai Vecākais projektu vadītājs, tiek atlasītas pēc noklusējuma. Atlasiet **Labi**.
7. Lapas **Pievienot projekta lomas** laukā **Resursu skaits** ievadiet **1**.
8. Laukā **Resursi** uzmeklēšana parāda visus resursus, kuriem ir nepieciešamās kompetences. Atlasiet **Rihards Taurenis** un pēc tam atlasiet **Izveidot**.
9. Lapā **Projekts** atlasiet **Pievienot**.
10. Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Grupas dalībnieks**. Laukā **Resursu skaits** ievadiet **5**.
11. Atlasiet **Izveidot**.
12. Lapā **Projekti** atlasiet **Izpildīt resursu**.

## <a name="resource-capacity-synchronization"></a>Resursu noslodzes sinhronizācija
Resursu sinhronizēšanas process palīdz nodrošināt to, ka informācija kalendāram un pamatkalendāram nokļūst projekta resursu plānošanā. Ja kalendārs tiek mainīts, procesi veic nepieciešamos atjauninājumus projekta resursu plānošanai. Šie procesi arī palīdz uzlabot veiktspēju, jo kalendāra resursu informācija tiek sinhronizēta jau iepriekš. Tāpēc resursu plānošanas informācijas atjauninājumi notiek ātrāk. Procesu plānošanu ieteicams veikt kā pakešuzdevumu, nevis atsevišķi katram procesam. Pretējā gadījumā pastāv risks, ka kāds aizmirsīs ietvertos datumus, kad pēdējo reizi tika sinhronizēta informācija. Ja netiek izmantoti ietvertie datumi, datu sinhronizācijas laikā var rasties pārrāvumi.

![Kalendāra sinhronizācija](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sinhronizēt resursu noslodzes apkopojumus

Sinhronizācijas process ir paredzēts, lai sinhronizētu visu resursu kalendāra informāciju. Šajā informācijā ir ietverta pamatkalendāra informācija par visām izmaiņām projekta resursu kalendāra noslodzes tabulā. Ja projektā tiek pievienoti jauni resursi, sinhronizācija palīdz garantēt to, ka ir pieejama atjaunināta kalendāra informācija. Šo sinhronizāciju var veikt jebkurā laikā.

Ieteicams izmantot partijas. Opcijas ir pieejamas noslodzes rezervāciju sinhronizēšanas laikā.

1. Atlasiet **Projektu vadība un uzskaite** &gt; **Periodisks** &gt; **Noslodzes sinhronizācija** &gt; **Sinhronizēt resursu noslodzes apkopojumus**.
2. Iestatiet opcijas nākamajā tabulā.

    | Opcija      | Apraksts |
    |-------------|-------------|
    | Perioda kods | Ja vēlaties, atlasiet virsgrāmatas datumu intervāla kodu, lai resursu noslodzes apkopojumu sinhronizācijas procesam iestatītu sākuma un beigu datumus. |
    | Sākuma datums  | Ievadiet resursu noslodzes apkopojumu sinhronizācijas procesa sākuma datumu. |
    | Beigu datums    | Ievadiet resursu noslodzes apkopojumu sinhronizācijas procesa beigu datumu. |

[![Sinhronizācijas process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Lomu iestatīšana WBS veidnēs
Projektu vadītāji var iestatīt WBS veidnes, kuras var lietot, izveidojot WBS jauniem projektiem. Projektu vadītāji var pievienot lomas veidnes izveides laikā. Izmantojiet šādu procedūru, lai piešķirtu lomu WBS veidnei.

1. Atlasiet **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Projekti** &gt; **Darba sadalījuma struktūras veidnes**.
2. Atlasītajai WBS veidnei atlasiet **Detalizēta informācija**.
3. Atlasiet sarakstā uzdevumu un pēc tam laukā **Loma** atlasiet lomu, kura tiks piešķirta uzdevumam.

### <a name="work-with-a-wbs"></a>Darbs ar WBS

Jūs varat izveidot jaunu WBS vai kopēt WBS no esošas WBS veidnes. Projektu vadītājs var ērti pārvaldīt resursus, piešķirot lomas jauniem uzdevumiem WBS struktūrā. Lomas var aizstāt vai nu pēc tam, kad resurss ir iegūts, vai arī pēc tam, kad ir identificēts apstiprināts resurss darbam pie attiecīgā uzdevuma. Šis elastīgums ļauj projektu vadītājiem veikt šādus uzdevumus:

- Identificēt resursu skaitu, kas nepieciešami WBS darba pakotnēm.
- Novērtēt projekta izmaksas.
- Noteikt sākotnējo budžetu.
- Novērtēt darbību ilgumu, pamatojoties uz lomām un resursiem.
- Izstrādāt dažus projekta vadības plānus, pamatojoties uz pieejamo projekta informāciju.

WBS struktūrā ir pievienotas papildu opcijas, lai labāk izmantotu resursu sadalījuma funkcionalitāti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcija</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resursu piešķires</td>
<td>Skatīt piešķirtos resursus, datumus, stundu skaitu un rezervācijas tipu uzdevumiem WBS struktūrā.</td>
</tr>
<tr class="even">
<td>Automātiski ģenerēt grupu</td>
<td>Automātiski pievienot plānotos resursus, izmantojot lomas, kas ir saistītas ar uzdevumu. Programmatūrā Finance and Operations tiek automātiski ieteikti ieplānotie resursi, izmantojot vairāku kritēriju lēmumu analīzi, kuras pamatā ir lomas. Pēc lomu un darba (stundas) iestatīšanas uzdevumiem WBS struktūrā un pēc struktūras nodošanas atlasiet <strong>Automātiski ģenerēt grupu</strong>. Nepieciešamais plānoto resursu skaits tiek pievienots WBS struktūrai un cilnē <strong>Projekta un grupas plānošana</strong>.</td>
</tr>
<tr class="odd">
<td>Resurss (nolaižamais saraksts)</td>
<td>Lapā <strong>Palaist resursu piešķiri </strong>varat atlasīt resursus stingrai vai vieglai rezervācijai, pamatojoties uz noteiktu ilgumu. Jūs varat pielāgot skata iestatījumus, lai skatītu un iestatītu resursu darbību ilgumu. Jūs varat atlasīt un piešķirt resursus darba pakotņu līmenī, izmantojot šādas opcijas:
<ul>
<li><strong>Pieņemt</strong> — apstiprināt tāda resursa izmaiņas, kas ir piešķirts uzdevumam.</li>
<li><strong>Atcelt</strong> — atcelt tāda resursa izmaiņas, kas ir piešķirts uzdevumam.</li>
<li><strong>Piešķirt automātiski</strong> — atlasītajam uzdevumam tiek automātiski atlasīts un piešķirts pieejams personāla resurss ar atbilstošu lomu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Lapā **Visi projekti** atlasiet projektu **XYZ jaunināšanas fāze 2**.
2. Atlasiet **Plāns** &gt; **Aktivitātes** &gt; **Darba sadalījuma struktūra**.
3. Atlasiet **Jauns**, lai WBS struktūrā pievienotu šādas pirmā līmeņa aktivitātes:

    - Uzsākšana
    - Plānošana
    - Izpilda
    - Pārraudzīšana un kontrole
    - Slēgt

4. Iestatiet datumus un darbu (stundas), kā parādīts nākamajā attēlā.

    [![Datumu un darba iestatīšana](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Atlasiet uzdevuma rindu **Uzsākšana** un pēc tam laukā **Loma** atlasiet **Vecākais projektu vadītājs**.
6. Atlasiet **Publicēt**.
7. Tajā pašā rindā, laukā **Resurss** atlasiet **Rihards Taurenis** un pēc tam atlasiet **Pieņemt**.
8. Atlasiet uzdevuma rindu **Plānošana** un pēc tam laukā **Loma** atlasiet **Biznesa analītiķis**.
9. Atlasiet **Publicēt** un pēc tam atlasiet **Automātiski ģenerēt grupu**.
10. Tiek parādīts ziņojuma lodziņš, un atlasiet tajā **Jā**.
11. Laukā **Resurss** pārbaudiet, vai vērtība ir **Biznesa analītiķis 1**.
12. Resursam **Biznesa analītiķis 1** atveriet uzmeklēšanu un atlasiet **Palaist resursu piešķires**. Pēc tam atlasiet nodarbināto attiecīgajam uzdevumam.
13. Atlasiet **Nestingrā piešķiršana** &gt; **Visa noslodze**.

    > [!NOTE] 
    > Netiek parādīts brīdinājums par to, ka norādītais resurss tagad ir 2, jo resursu skaits joprojām ir 1.

14. Lapā **Darba sadalījuma struktūra** pārbaudiet resursa piešķiri WBS struktūrā un pēc tam atlasiet **Saglabāt**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resursu izpilde plānotiem resursiem
Projektu vadītājs var plānot nepieciešamo resursu lomas projektam. Resursu pārvaldnieks redzēs šos plānotos resursus kā pieprasījumus lapā **Resursu izpilde** un var piešķirt faktiskos resursus.

1. Lapā **Visi projekti** atlasiet projektu **XYZ jaunināšanas fāze 2**.
2. Atlasiet **Projekts** un pēc tam atlasiet **Rediģēt**.
3. Cilnē **Projekta grupa un plānošana** atlasiet **Pievienot**.
4. Dialoglodziņā **Pievienot lomas** atlasiet lomu **Programmatūras izstrādātājs**.
5. Atlasiet **Izveidot** un pēc tam aizveriet projekta lapu.
6. Lapā **Resursu izpilde** projektam **XYZ jaunināšanas projekta fāze 2** atlasiet **Programmatūras izstrādātājs 1**.
7. Atlasiet nodarbināto un pēc tam atlasiet **Piešķirt**.
8. Pārbaudiet, vai rinda vienumam **Programmatūras izstrādātājs 1** ir izdzēsta projektam **XYZ jaunināšanas projekta fāze 2**.
9. Cilnē **Projekta grupa un plānošana** projektam **XYZ jaunināšanas fāze 2** pārbaudiet, vai nodarbinātais, kuru atlasījāt iepriekšējā darbībā, ir pievienots kā **Programmatūras izstrādātājs**.

## <a name="requests-for-project-resources"></a>Projekta resursu pieprasījumi
Projekta resursu plānošanas funkcionalitāte resursu pārvaldniekiem pa piesaistēm vai projektiem ļauj sadalīt tikai nokomplektētos resursus. Lai iespējoto šo funkcionalitāti, izpildiet tālāk norādītos uzdevumus vai pārliecinieties, ka tie jau ir izpildīti.

- Iestatiet numuru sērijas.
- Iestatiet projektu vadības un uzskaites darbplūsmas.
- Iespējojiet resursu pieprasījumu darbplūsmas.

Kad iepriekš norādītie uzdevumi ir izpildīti, pēc nepieciešamības varat izpildīt tālāk norādītos uzdevumus.

- Izveidojiet resursa pieprasījumu, izmantojot viegli rezervētu personāla resursu.
- Pārraugiet resursu pieprasījumus.
- Izpildiet resursu pieprasījumus.
- Pieprasiet nokomplektētu resursu no WBS.
- Rezervējiet projektam resursus bez nepieciešamības pieprasīt nokomplektētu resursu.

## <a name="monitor-project-teams"></a>Projektu grupu pārraudzība
1. Lapā **Visi projekti** atlasiet saiti **Projekta ID** projektam **XYZ jaunināšanas fāze 2**.
2. Kopsavilkuma cilnē **Projekta grupa un plānošana** pārbaudiet, vai minētie projekta resursi ir pareizi.

