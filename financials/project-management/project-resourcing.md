---
title: "Projekta resursu sadalījums"
description: "Šajā tēmā ir sniegta informācija par projekta resursu sadalījumu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5c00c63e3c55e818934c36b818c90025002092d4
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="project-resourcing"></a>Projekta resursu sadalījums

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegta informācija par projekta resursu sadalījumu.

Viens no izaicinājumiem, ar ko projektu vadītāji un resursu pārvaldnieki saskaras projekta plānošanas posma laikā, ir resursu sadalījums, kura ietvaros viņiem ir jānosaka un jārezervē darbam projektā vajadzīgais resurss. Programmatūrā Microsoft Dynamics 365 for Operations projektu resursu sadalījuma iespējas sniedz iespēju definēt lomas, kas tiek uzskatītas par pagaidu resursiem, kurus var rezervēt noteiktai iesaistei vai iesaistes daļai. Šāds resursu sadalījuma veids ļauj projektu vadītājiem un resursu pārvaldniekiem veikt šādus uzdevumus:

-   Definēt lomu, kurai ir nepieciešamās kompetences, lai atvieglotu resursu saskaņošanu.
-   Izmantot lomas, lai definētu sākotnējo iesaistes grafiku, pamatojoties uz rezervētajiem resursiem.
-   Novērtēt izmaksas un noteikt sākotnējo budžetu, pamatojoties uz piešķirtajām lomām un projekta resursiem.
-   Izmantot lomas, lai noteiktu to resursu rezervāciju skaitu, kas ir nepieciešamas katrai iesaistei.
-   Novērtēt resursu skaitu, kas nepieciešami visā projekta dzīves ciklā.
-   Izstrādāt darba sadalījuma struktūras (WBS) projektu, izmantojot sākotnējo resursu piešķires.

[![Projekta dzīves cikls](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Projekta plānošanas gaitā ieplānotos resursus var aizstāt ar personāla resursiem. Projektu vadītājs var arī atgriezties un atjaunināt resursu rezervācijas jebkurā projekta posmā.

## <a name="set-up-project-resources"></a>Projekta resursu iestatīšana
Ir jāiestata kalendārs un jāsaista tas ar darbinieku vai nodarbināto. Kalendārs tiek izmantots, lai plānotu projektu un projektam rezervēto resursu darba laiku. Kalendāra iestatīšanas laikā projektu vadītāji var veikt resursu izlīdzināšanu resursu optimizācijas ietvaros. Pamatojoties uz kalendāra grafiku, resursiem var noteikt ierobežojumus. Kalendāru varat iestatīt lapā **Kalendāri**. 

Kad iestatāt nodarbināto kā projekta resursu, varat atlasīt kādu no nodarbinātajiem, kuri strādā uzņēmumā, kam iestatāt resursus, vai arī varat atlasīt nodarbinātos no citiem uzņēmumiem jūsu organizācijā. Tie ir starpuzņēmumu resursi. Tālāk sniegtajos procedūru aprakstos ir paskaidrot,s kā iestatīt nodarbināto kā projekta resursu jūsu uzņēmumā un kā iestatīt starpuzņēmumu projekta resursu.

### <a name="set-up-a-worker-as-a-project-resource"></a>Nodarbinātā kā projekta resursa iestatīšana

1.  Lapas **Darbinieki** sarakstā **Nodarbinātie** atlasiet nodarbināto, kuru pievienojat kā projekta resursu, un atveriet nodarbinātā ierakstu.
2.  Darbību rūtī noklikšķiniet uz **Projekts** &gt; **Iestatījumi** &gt; **Projektu iestatījumi**.
3.  Atlasiet kalendāru un pēc tam aizveriet lapu.

Jūs varat arī norādīt resursam noklusējuma projektus kā iepriekšēju piešķiri. Iepriekšējas piešķires var izmantot, ja resursu pārvaldnieks vai projektu vadītājs iepriekš zina, kurā projektā resurss veiks darbu. Iepriekšējas piešķires arī var balstīties uz projekta sponsora vai debitora pieprasījumu. Lai veiktu projekta iepriekšēju piešķiri, lapas **Piešķirt projektus** cilnes **Projekti** sarakstā **Atlikušie projekti** atlasiet attiecīgo projektu.

### <a name="set-up-an-intercompany-resource"></a>Starpuzņēmumu resursa iestatīšana

Kad iestatāt nodarbināto kā starpuzņēmumu resursu, ir jāveic iestatīšana gan uzņēmumā, kas aizdod, gan uzņēmumā, kas aizņemas. 

**Uzņēmumā, kas aizdod**

1.  Programmatūrā Dynamics 365 for Operations pārbaudiet, vai ir atlasīts uzņēmums, kas aizdod, un pēc tam veiciet iepriekš sadaļā “Nodarbinātā kā projekta resursa iestatīšana” aprakstīto procedūru.
2.  Pārejiet uz sadaļu **Virsgrāmata **&gt; **Grāmatošanas iestatīšana = **&gt; **Starpuzņēmumu uzskaite**. Noklikšķiniet uz **Jauns**.
3.  Laukā **Juridiskās personas ID** atlasiet uzņēmumu, kas aizdod. Aizpildiet pārējos laukus ar atbilstošu informāciju un pēc tam atlasiet vienumu **Saglabāt**.
4.  Pārejiet uz sadaļu **Projektu vadība un uzskaite **&gt; **Iestatījumi **&gt; **Cenas ** &gt; **Transfertcena**.** **
5.  Veidlapā **Transfērcena** noklikšķiniet uz **Jauns** un laukā **Juridiskā persona, kas veic piesaistīšanu** atlasiet atbilstošo uzņēmumu.
6.  Ja vēlaties aizdot uzņēmumam, kas aizņemas, tikai to resursu, kuru izveidojāt šīs sadaļas sākumā, laukā **Resurss** atlasiet izveidotā resursa nosaukumu. Ja vēlaties, lai uzņēmumam, kas aizņemas, būtu pieejami visi resursi, atstājiet lauku **Resurss** tukšu.
7.  Pārejiet uz sadaļu **Projektu vadība un uzskaite **&gt; **Iestatījumi **&gt; **Projektu vadības un uzskaites parametri** un cilnē **Starpuzņēmumu** iestatiet lauka **Aktivizēt starpuzņēmumu resursu plānošanu un laika grafikus** vērtību **Jā**.

**Uzņēmumā, kas aizņemas**

1.  Pārejiet uz sadaļu **Projektu vadība un uzskaite** &gt; **Projekta resursi** &gt; **Resursu saraksts**.
2.  Meklēšanas filtrā ievadiet tā resursu nosaukumu, kuru iepriekšējās procedūras ietvaros izveidojāt uzņēmumam, kas aizdod, lai pārbaudītu, vai šis nosaukums ir ietverts tā uzņēmuma resursu sarakstā, kas aizņemas.

## <a name="manage-resource-competencies"></a>Resursu kompetenču pārvaldība
Resursu kompetencēm ir būtiska nozīme resursu vadības procesā. Kompetences var izmantot kā bāzlīniju, lai noteiktu resursus, kuriem ir atbilstošā prasmju, izglītības, sertifikācijas un projektu pieredzes attiecība. Šī informācija ir jāiestata katram resursam un tā regulāri jāatjaunina. Šādā veidā var palielināt iespējas, kad konkrētas resursu kompetences tiek saskaņotas laikā projekta resursu piešķires laikā. [![Prasmju, sertifikāciju, izglītības un projektu pieredzes piemēri](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Tālāk minētajās procedūrās ir paskaidrots, kā iestatīt dažas resursu kompetences. 

Lai iestatītu nodarbinātā kompetences, var izmantot saraksta lapu **Nodarbinātie** modulī Personāla vadība vai saraksta lapu **Resursi** modulī Projektu vadība un uzskaite. Tālāk norādītajām procedūrām tiek izmantota saraksta lapa **Nodarbinātie** modulī Personāla vadība.

### <a name="set-up-competencies-certificates"></a>Kompetenču iestatīšana: sertifikāti

1.  Saraksta lapā **Nodarbinātie** atlasiet tāda nodarbinātā rindu, attiecībā uz kuru pievienosit sertifikāta informāciju.
2.  Sadaļas Darbību rūts cilnē **Nodarbinātais**, grupā **Kompetences** noklikšķiniet uz **Sertifikāti**.
3.  Noklikšķiniet uz **Jauns**.
4.  Laukā **Sertifikāta veids** atlasiet **PMP**.
5.  Laukā **Sākuma datums** atlasiet **01.10.2015.**.
6.  Noklikšķiniet uz **Saglabāt** un pēc tam aizveriet lapu.

### <a name="set-up-competencies-skills"></a>Komptenču iestatīšana: prasmes

1.  Saraksta lapā **Nodarbinātie** pārbaudiet, vai iepriekšējā procedūrā izmantotais nodarbinātais joprojām ir atlasīts. Pēc tam sadaļas Darbību rūts cilnē **Nodarbinātais**, grupā **Kompetences** noklikšķiniet uz **Prasmes**.
2.  Noklikšķiniet uz **Jauns**.
3.  Laukā **Prasme** atlasiet **Projektu vadība**.
4.  Laukā **Līmenis** atlasiet **5 Eksperta līmenis**.
5.  Laukā **Līmeņa datums** atlasiet **14.01.2014.**.
6.  Laukā **Pieredzes gadu skaits** ievadiet **10**.
7.  Noklikšķiniet uz **Saglabāt** un pēc tam aizveriet lapu.

## <a name="create-a-new-project"></a>Izveidot jaunu projektu
1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Darbvietas** &gt; **Projektu vadība**.
2.  Noklikšķiniet uz **Jauns projekts** un ievadiet šādas vērtības:
    -   **Projekta tips** — Laiks un materiāli
    -   **Projekta nosaukums** — 2. XYZ jaunināšanas posms
    -   **Projektu grupa** — TM\_WIP
    -   **Projekta līguma ID** — 00000002
3.  Noklikšķiniet uz **Izveidot projektu**.

### <a name="assign-a-resource-to-a-project"></a>Resursa piešķiršana projektam

1.  Noklikšķiniet uz **Personāla vadība** &gt; **Nodarbinātie** &gt; **Nodarbinātie**.
2.  Sarakstā **Nodarbinātie** atlasiet tāda nodarbinātā ierakstu, kuram iepriekš veicāt kompetenču iestatīšanu, un atveriet nodarbinātā ierakstu.
3.  Sadaļas Darbību rūts cilnē **Projekts**, grupā **Iestatījumi** noklikšķiniet uz **Piešķirt projektus**.
4.  Lapā **Resursa apstiprināšanas projektu piešķires** noklikšķiniet uz cilnes **Projekti**.
5.  Sadaļā **Pievienot projektu atlasītajiem projektiem** filtrējiet pēc projekta nosaukuma 2. XYZ jaunināšanas posms.
6.  Rūtī **Atlikušie projekti** atlasiet projektu un pēc tam noklikšķiniet uz bultiņas, lai to pievienotu rūtī **Atlasītie projekti**.
7.  Aizvērt lapu.

Nepieciešamības gadījumā var arī piešķirt kategorijas resursam. Kategorijas tips ir Izmaksas vai Ieņēmumi. To nosaka jūsu organizācija. Ja resursam nav piešķirta neviena kategorija, programmatūrā Dynamics 365 for Operations tiek uzmeklēta izmaksu un ieņēmumu noklusējuma stundu likmju kategorija.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projekta resursu un lomu īpašību iestatīšana

Projekta vadītājs var izmantot projekta resursu sadalījuma funkcionalitāti, lai izveidotu lomas, kas nepieciešamas projektam. Lomas var izmantot, ja apstiprinātie resursi joprojām nav zināmi resursu rezervēšanas laikā. Lomas var uz laiku rezervēt kā ieplānotos resursus, lai varētu turpināt projekta plānošanas posmus. 

[![Lomas piemērs](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenārijs:** Contoso tika nolīgts, lai pabeigtu laika un materiālu projektu, kuram ir apstiprināta projekta privilēģijas. Jaunākais projektu vadītājs joprojām strādā pie projekta darba apjoma pabeigšanas. Resursu pārvaldnieks pašlaik norāda konkrētus resursus, kas tiks rezervēti darbam ar jauno projektu. Viena no lomām, ko projekta nozīmīguma dēļ pieprasīja projekta sponsors, ir Vecākais projektu vadītājs. Resursu pārvaldniekam ir jāiegūst jaunais resurss un sistēmā jādefinē loma, lai tā būtu pieejama gadījumā, ja jaunākajam projektu vadītājam projekta plānošanas laikā ir nepieciešama resursa informācija. 

Tālāk sniegtajos darbību aprakstos ir norādīts, kā resursu pārvaldnieks var iestatīt lomu Vecākais projektu vadītājs un piesaistīt tai resursa īpašības. Pēc tam šo lomu var izmantot, lai meklētu pieejamos resursus, kas atbilst nepieciešamajām resursu kompetencēm.

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Resursi** &gt; **Lomu iestatīšana**.
2.  Noklikšķiniet uz **Jauns** un ievadiet šādas vērtības:
    -   **Lomas ID** — Vecākais projektu vadītājs
    -   **Apraksts** — Vecākais projektu vadītājs
3.  Noklikšķiniet uz **Izveidot**.
4.  Atlasiet lomu **Vecākais projektu vadītājs** un pēc tam noklikšķiniet uz **Konfigurēt īpašības**.
5.  Laukā **Īpašību veids** atlasiet **Prasme**.
6.  Laukā **Pieejamās īpašības** ievadiet prasmi, ko meklējat.
7.  Laukā **Īpašību veids** atlasiet **Sertifikāts**.
8.  Laukā **Pieejamās īpašības** ievadiet meklējamo sertifikātu.
9.  Noklikšķiniet uz **Labi** un aizveriet lapu.

### <a name="assign-a-project-resource-to-a-project"></a>Projekta resursa piešķiršana projektam

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Vispārīgi** &gt; **Projekti** &gt; **Visi projekti** un atveriet projektu **2. XYZ jaunināšanas posms**.
2.  Cilnē **Projekta grupa un plānošana** noklikšķiniet uz **Pievienot**.
3.  Laukā **Loma** atlasiet **Grupas dalībnieks**.
4.  Noklikšķiniet uz **Rezervēt no kalendāra**.
5.  Lapā **Resursu pieejamība** noklikšķiniet uz **Skata iestatījumi**.
6.  Lapā **Pielāgojiet skata iestatījumus** ievadiet šādas vērtības:
    -   **Datumu diapazona skata formāts** — Diena
    -   **Parādīt pieejamības aprakstus** — Jā
    -   **Rādīt atlikušo noslodzi** — Jā
7.  Resursu sarakstā atlasiet resursu.
8.  Noklikšķiniet uz **Stingrā rezervēšana** &gt; **Visa noslodze**.
9.  Aizvērt lapu.

### <a name="assign-a-resource-to-a-default-role"></a>Resursa piešķiršana noklusējuma lomai

Lai palīdzētu projektu vadītājiem vai resursu pārvaldniekiem, varat detalizētāk rādīt resursus, ko var rezervēt projektam. Noklusējuma lomu var saistīt ar esošu resursu vai jauniegūtu resursu. Piemēram, kad Rihards tika pieņemts darbā, viņa pieredze un prasmes bija piemērotas lomai Biznesa analītiķis. Resursu pārvaldnieks piešķīra šo lomu kā Rihards noklusējuma lomu. Tādējādi resursu pārvaldnieks pievienoja Danielu to biznesa analītiķu kopai, kuri ir pieejami darbam projektā. 

Resursu rezervēšanas laikā projektu vadītāji var filtrēt lomu resursus, kas ir pieejami darbam projektos. Viņi var izmantot šo informāciju kā vienu kritēriju, veicot vairāku kritēriju lēmumu analīzi resursu izpildes laikā. Viņi var pievienot arī citas resursa īpašības filtram, lai meklētu resursus, kuriem ir īpašas prasmes, izglītība un pieredze attiecīgajam projektam. 

**Scenārijs:** ir uzsākts apstiprināts projekts, un loma Vecākais projektu vadītājs ir rezervēta kā ieplānots resurss projekta plānošanas posma laikā. Resursu pārvaldnieks ir ieguvis resursu, lai aizpildītu lomu Vecākais projektu vadītājs.

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Projekta resursi** &gt; **Resursu saraksts**.
2.  Sarakstā **Resursi** atlasiet **Rihards Taurenis**.
3.  Noklikšķiniet uz **Projekta resursi** &gt; **Uzturēt** &gt; **Resursa loma**.
4.  Noklikšķiniet uz **Jauns** un ievadiet šādas vērtības:
    -   **Ir spēkā** — (pašreizējais datums)
    -   **Beigu datums** — Nekad
    -   **Loma** — Vecākais projektu vadītājs
5.  Noklikšķiniet uz **Saglabāt** un pēc tam aizveriet lapu.
6.  Cilnē **Kompetences** pievienojiet prasmi **ProjectMgmt** un sertifikātu **PMP**.

## <a name="set-up-role-based-pricing"></a>Uz lomu balstītas cenu noteikšanas iestatīšana
Visas izmaksu, pārdošanas un pārsūtīšanas cenas var iestatīt lomām.

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Cenas** &gt; **Pārdošanas cena (stunda)**.
2.  Noklikšķiniet uz **Jauns**.
3.  Ievadiet spēkā stāšanās datumu.
4.  Kolonnā **Loma** atlasiet lomu.
5.  Kolonnā **Cenu noteikšana** ievadiet cenu atlasītajai resursu lomai.

## <a name="form-a-project-team"></a>Projekta grupas veidošana
Lai lietotu lomas, kas iepriekš tika iestatītas projektā, projektu vadītājam šīs lomas ir jāsaista ar projektu. Projektam var piešķirt vairākas lomas, un rezervēšanas laikā programmatūrā Dynamics 365 for Operations šīs lomas tiek automātiski apzīmētas, lai nepieļautu neskaidrības. Piemēram, ja projektu vadītājam ir nepieciešami trīs programmatūras inženieri, tiek automātiski ģenerētas trīs lomas Programmatūras inženieris, kuru apzīmējumi ir “1. programmatūras inženieris”, “2. programmatūras inženieris” un “3. programmatūras inženieris”. Ja lomai iepriekš tika iestatītas lomas īpašības, tās tiek pielietotas kā filtrs resursu meklēšanas laikā. Lai precizētu meklēšanu, nepieciešamības gadījumā var pievienot papildu īpašības. 

Skata iestatījumus arī var pielāgot, lai nodrošinātu labāku pārskatu par resursu pieejamību. Ir pieejamas iespējas stundu, dienu, nedēļu, ceturkšņu un gada pieejamības attēlošanai. Pastāv arī iespēja rādīt pieejamo un atlikušo resursu noslodzi. Šī opcija ir noderīga laika pārvaldībai, novērtējot pieejamo laiku darbībām vai resursu pieejamību. 

Projektu vadītājs var lapā atlasīt lomu un pēc tam, ja ir pieejams resurss, kas atbilst vajadzībai, viņš var rezervēt resursu šai lomai. Ņemiet vērā, ka resursi nav jārezervē šajā plānošanas posma brīdī. Veidojot WBS, lomas var aizstāt ar projekta personāla resursiem. Ja WBS ietvaros lomas tiek aizstātas ar personāla resursiem, resursu iestatījumos tiek automātiski atjaunināts projekta grupas saraksts un plānošana. 

[![Projekta grupas saraksts, kurā ir ietvertas gan lomas, gan faktiskie resursi](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektu vadītājam ir dažādas iespējas projekta resursu rezervācijai, piemēram, **Atlikusī noslodze**, **Pilna noslodze**, **Noslodzes procentuālā daļa** un **Norādiet stundas**. Šīs rezervēšanas iespējas var atcelt jebkurā laikā, ja mainās resursu piešķires. Tiek atbalstīti divi rezervāciju tipi:

-   **Stingrā rezervācija** — resursa rezervācija ir apstiprināta darbam attiecīgajā iesaistē uz norādīto laiku.
-   **Vieglā rezervēšana** — resursu rezervācijas ir uz laiku iestatītas darbam attiecīgajā iesaistē uz norādīto laiku.

Tālāk esošajā procedūrā izskaidrots, kā izveidot projekta grupu.

### <a name="create-a-project-team"></a>Projekta grupas izveide

1.  Saraksta lapā **Visi projekti** atlasiet projektu un pēc tam noklikšķiniet uz **Rediģēt**.
2.  Cilnes **Projekta grupa un plānošana** laukā **Grafika beigu datums** ievadiet grafika sākuma datumu, kam ir pieskaitīts viens mēnesis. Piemēram, ja grafika sākuma datums ir 2017. gada 24. jūnijs (24/06/2017), ievadiet **24/07/2017**.
3.  Noklikšķiniet uz **Pievienot**.
4.  Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Vecākais projektu vadītājs**.
5.  Noklikšķiniet uz **Nepieciešamās kompetences**.
6.  Lapā **Īpašību izvēle** īpašības, ko iepriekš iestatījāt lomai Vecākais projektu vadītājs, tiek atlasītas pēc noklusējuma. Noklikšķiniet uz **Labi**.
7.  Lapas **Pievienot projekta lomas** laukā **Resursu skaits** ievadiet **1**.
8.  Laukā **Resursi** uzmeklēšana parāda visus resursus, kuriem ir nepieciešamās kompetences. Atlasiet **Rihards Taurenis** un pēc tam noklikšķiniet uz **Izveidot**.
9.  Lapā **Projekts** noklikšķiniet uz **Pievienot**.
10. Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Grupas dalībnieks**. Laukā **Resursu skaits** ievadiet **5**.
11. Noklikšķiniet uz **Izveidot**.
12. Lapā **Projekti** noklikšķiniet uz **Izpildīt resursu**.

## <a name="resource-capacity-synchronization"></a>Resursu noslodzes sinhronizācija
Resursu sinhronizācijas process palīdz nodrošināt to, ka kalendāra un pamatkalendāra informācija nokļūst projekta resursu plānošanā Ja kalendārs tiek mainīts, procesi veic nepieciešamos atjauninājumus projekta resursu plānošanai. Procesi arī palīdz uzlabot veiktspēju, jo kalendāru resursu informācija tiek sinhronizēta iepriekš, tādējādi resursu plānošanas informācijas atjauninājumi notiek ātrāk. Procesu plānošanu ieteicams veikt kā pakešuzdevumu, nevis atsevišķi katram procesam. Pretējā gadījumā pastāv risks, ka kāds aizmirsīs ietvertos datumus, kad pēdējo reizi tika sinhronizēta informācija. Ja netiek izmantoti ietvertie datumi, datu sinhronizācijas laikā var rasties pārrāvumi.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Kalendāra sinhronizācija](./media/projectresourcing04-1024x471.jpg)

**Resursu noslodzes apkopojumu sinhronizācija**

Sinhronizācijas process ir paredzēts, lai sinhronizētu visu resursu kalendāra informāciju. Šajā informācijā ietilpst pamatkalendāra informācija par visām izmaiņām projekta resursu kalendāra noslodzes tabulā. Ja projektā tiek pievienoti jauni resursi, sinhronizācija palīdz nodrošināt to, ka ir pieejama atjaunināta kalendāra informācija. Šo sinhronizāciju var veikt jebkurā laikā. 

Ieteicams izmantot partijas. Opcijas ir pieejamas, sinhronizējot noslodzes rezervācijas.

-   Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Periodiskās darbības** &gt; **Noslodzes sinhronizācija** &gt; **Sinhronizēt resursu noslodzes apkopojumus**.

| Opcija | Apraksts                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jā    | Sinhronizēt visus resursu datus ar kalendāra un pamatkalendāra informāciju un aizstāt visu informāciju projekta resursu noslodzes kalendārā.                                                  |
| Nē     | Sinhronizēt resursu datus, pamatojoties uz datumu intervāla kodu un norādītajiem sākuma un beigu datumiem. Šī opcija nedzēš esošos datus un atjaunina informāciju tikai par jaunpievienotiem resursiem. |

[![Sinhronizācijas process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Lomu iestatīšana WBS veidnēs
Projektu vadītāji var iestatīt WBS veidnes, kuras var lietot, izveidojot WBS jauniem projektiem. Projektu vadītāji var pievienot lomas veidnes izveides laikā. Lai piešķirtu lomu WBS veidnei, izmantojiet tālāk norādīto procedūru.** **

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Projekti** &gt; **Darba sadalījuma struktūras veidnes**.
2.  Noklikšķiniet uz **Detalizēta informācija** atlasītajai WBS veidnei.
3.  Atlasiet sarakstā uzdevumu un pēc tam laukā **Loma** atlasiet lomu, kura tiks piešķirta uzdevumam.

### <a name="work-with-a-wbs"></a>Darbs ar WBS

Jūs varat izveidot jaunu WBS vai kopēt WBS no esošas WBS veidnes. Projektu vadītājs var ērti pārvaldīt resursus, piešķirot lomas jauniem uzdevumiem WBS struktūrā. Lomas var aizstāt pēc tam, kad resurss ir iegūts, vai pēc tam, kad ir identificēts apstiprināts resurss darbam pie attiecīgā uzdevuma. Šis elastīgums ļauj projektu vadītājiem veikt šādus uzdevumus:

-   Identificēt resursu skaitu, kas nepieciešami WBS darba pakotnēm.
-   Novērtēt projekta izmaksas.
-   Noteikt sākotnējo budžetu.
-   Novērtēt darbību ilgumu, pamatojoties uz lomām un resursiem.
-   Izstrādāt dažus projekta vadības plānus, pamatojoties uz pieejamo projekta informāciju.

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
<td>Automātiski pievienot plānotos resursus, izmantojot lomas, kas ir saistītas ar uzdevumu. Programmatūrā Dynamics 365 for Operations tiek automātiski ieteikti ieplānotie resursi, izmantojot vairāku kritēriju lēmumu analīzi, kuras pamatā ir lomas. Pēc lomu un darba (stundas) iestatīšanas uzdevumiem WBS struktūrā un struktūras nodošanas noklikšķiniet uz <strong>Automātiski ģenerēt grupu</strong>. Nepieciešamais plānoto resursu skaits tiek pievienots WBS struktūrai un cilnē <strong>Projekta un grupas plānošana</strong>.</td>
</tr>
<tr class="odd">
<td>Resurss (nolaižamais saraksts)</td>
<td>Lapā <strong>Palaist resursu piešķiri </strong>varat atlasīt resursus stingrai vai vieglai rezervācijai, pamatojoties uz noteiktu ilgumu. Jūs varat pielāgot skata iestatījumus, lai skatītu un iestatītu resursu darbību ilgumu. Jūs varat atlasīt un piešķirt resursus darba pakotņu līmenī, izmantojot šādas opcijas:
<ul>
<li><strong>Pieņemt</strong> — apstiprināt tāda resursa izmaiņas, kas ir piešķirts uzdevumam.</li>
<li><strong>Atcelt</strong> — atcelt tāda resursa izmaiņas, kas ir piešķirts uzdevumam.</li>
<li><strong>Piešķirt automātiski</strong> — izmantojot šo opciju, tiek atlasīts pieejams personāla resurss ar atlasītajam uzdevumam atbilstošu lomu.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Projekti** &gt; **Visi projekti**.
2.  Sarakstā atlasiet projektu **XYZ jaunināšanas fāze 2**.
3.  Noklikšķiniet uz **Plāns** &gt; **Aktivitātes** &gt; **Darba sadalījuma struktūra**.
4.  Noklikšķiniet uz **Jauns**, lai pievienotu šādas pirmā līmeņa aktivitātes WBS struktūrā:
    -   Uzsākšana
    -   Plānošana
    -   Izpilda
    -   Pārraudzīšana un kontrole
    -   Tuva

5.  Iestatiet datumus un darbu (stundas), kā tas ir redzams tālāk esošajā ekrānuzņēmumā.[![Datumu un darba iestatīšana](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Atlasiet uzdevuma rindu **Uzsākšana** un pēc tam laukā **Loma** atlasiet **Vecākais projektu vadītājs**.
7.  Noklikšķiniet uz **Publicēt**.
8.  Tajā pašā rindā laukā **Resurss** atlasiet **Rihards Taurenis**.
9.  Noklikšķiniet uz **Akceptēt**.
10. Atlasiet uzdevuma rindu **Plānošana** un pēc tam laukā **Loma** atlasiet **Biznesa analītiķis**.
11. Noklikšķiniet uz **Publicēt** un pēc tam noklikšķiniet uz **Automātiski ģenerēt grupu**.
12. Dialoglodziņā, kas tiek parādīta, noklikšķiniet uz **Jā**.
13. Laukā **Resurss** pārbaudiet, vai vērtība ir **Biznesa analītiķis 1**.
14. Resursam **Biznesa analītiķis 1** atveriet uzmeklēšanu un noklikšķiniet uz **Palaist resursu piešķires veidlapu**.
15. Atlasiet nodarbināto attiecīgajam uzdevumam.
16. Noklikšķiniet uz **Vieglā piešķiršana** &gt; **Visa noslodze**.
17. Noklikšķiniet uz **Saglabāt** un aizveriet lapu. 

> [!NOTE] 
> Netiek parādīts brīdinājums par to, ka norādītais resurss tagad ir Nr. 2, jo resursu skaits joprojām ir 1.
18. Lapā **Darba sadalījuma struktūra** pārbaudiet resursa piešķiri WBS struktūrā un pēc tam noklikšķiniet uz **Saglabāt**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resursu izpilde plānotiem resursiem
Projektu vadītājs var plānot nepieciešamo resursu lomas projektam. Resursu pārvaldnieks redzēs šos plānotos resursus kā pieprasījumus lapā **Resursu izpilde** un var piešķirt faktiskos resursus.

1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Projekti** &gt; **Visi projekti**.
2.  Sarakstā atlasiet projektu **XYZ jaunināšanas fāze 2**.
3.  Noklikšķiniet uz **Projekts**.
4.  Noklikšķiniet uz **Rediģēt**.
5.  Cilnē **Projekta grupa un plānošana** noklikšķiniet** **uz **Pievienot**.
6.  Dialoglodziņā **Pievienot lomas** atlasiet lomu **Programmatūras izstrādātājs**.
7.  Noklikšķiniet uz **Izveidot**.
8.  Aizveriet projekta lapu.
9.  Noklikšķiniet uz**Projektu vadība un uzskaite** &gt; **Projekta resursi** &gt; **Resursu izpilde**.
10. Atlasiet **Programmatūras izstrādātājs 1** projektam **XYZ jaunināšanas projekta fāze 2**.
11. Atlasiet nodarbināto un pēc tam noklikšķiniet uz **Piešķirt**.
12. Pārbaudiet, vai rinda vienumam **Programmatūras izstrādātājs 1** ir izdzēsta projektam **XYZ jaunināšanas projekta fāze 2**.
13. Cilnē **Projekta grupa un plānošana** projektam **XYZ jaunināšanas fāze 2** pārbaudiet, vai nodarbinātais, kuru atlasījāt 11. solī, ir pievienots kā **Programmatūras izstrādātājs**.

## <a name="requests-for-project-resources"></a>Projekta resursu pieprasījumi
Projekta resursu plānošanas funkcija sniedz resursu pārvaldniekiem iespēju tikai sadalīt personāla resursus pa iesaistēm vai projektiem. Lai iespējoto šo funkciju, izpildiet tālāk norādītos uzdevumus vai pārliecinieties, ka tie jau ir izpildīti.

-   Iestatiet numuru sērijas.
-   Iestatiet projektu vadības un uzskaites darbplūsmas.
-   Iespējojiet resursu pieprasījumu darbplūsmu.

Kad esat izpildījis iepriekš norādītos uzdevumus vai pārliecinājies par to izpildi, varat izpildīt tālāk norādītos uzdevumus, ja tas ir vajadzīgs.

-   Izveidojiet resursa pieprasījumu, izmantojot viegli rezervētu personāla resursu.
-   Pārraugiet resursu pieprasījumus.
-   Izpildiet resursu pieprasījumus.
-   Pieprasiet personāla resursu no WBS.
-   Rezervējiet resursus projektam bez personāla resursa pieprasījuma.

## <a name="monitor-project-teams"></a>Projektu grupu pārraudzība
1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Projekti** &gt; **Visi projekti**.
2.  Projektu sarakstā noklikšķiniet uz saites **Projekta ID** projektam **XYZ jaunināšanas fāze 2**.
3.  Kopsavilkuma cilnē **Projekta grupa un plānošana** pārbaudiet, vai minētie projekta resursi ir pareizi.





