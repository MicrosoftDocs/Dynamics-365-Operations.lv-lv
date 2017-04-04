---
title: "Projekta resursu sadalījums"
description: "Šajā tēmā ir sniegta informācija par projekta resursu sadalījumā."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Projekta resursu sadalījums

Šajā tēmā ir sniegta informācija par projekta resursu sadalījumā.

Projektu vadītāji un resursu pārvaldītājiem, projekta plānošanas posma laikā viens uzdevums ir resursu sadali, ja tās noteiktu un rezervēt resursu pareizu darbu pie projekta. Programmā Microsoft Dynamics 365 operācijas, resursus projektu iespējas ļauj definēt lomas, kas tiek uzskatīti par pagaidu resursi, kas var rezervēt konkrētu iesaistīšanos vai daļu ielūgta. Šāds resursu sadalījuma veids ļauj projektu vadītājiem un resursu pārvaldniekiem veikt šādus uzdevumus:

-   Definēt lomu, kurai ir nepieciešamās kompetences, lai atvieglotu resursu saskaņošanu.
-   Lai definētu sākotnējās iesaistīšanās grafiku, kas balstās uz rezervēto līdzekļu izmantot lomas.
-   Novērtēt izmaksas un noteikt sākotnējo budžetu, pamatojoties uz piešķirtajām lomām un projekta resursiem.
-   Lieto lomas, lai novērtētu resursu rezervēšanu, kas nepieciešamas katrā darbā skaitu.
-   Novērtēt resursu skaitu, kas nepieciešami visā projekta dzīves ciklā.
-   Izstrādāt darba sadalījuma struktūras (WBS) projektu, izmantojot sākotnējo resursu piešķires.

[![Projekta dzīves cikls](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Kā projektu plānojot ieņēmumus, plānotie resursi var aizvietot ar personālu resursus. Projekta vadītājs var doties atpakaļ un atjaunināt resourcing rezervācijas laikā kādu no projekta posmiem.

## <a name="set-up-project-resources"></a>Projekta resursu iestatīšana
Ir jāiestata kalendārs un jāsaista tas ar darbinieku vai nodarbināto. Kalendārs tiek izmantots, lai plānotu projektu un darba laiks, resursi, kas ir rezervēti projekta. Kalendāra iestatīšanas laikā projektu vadītāji var veikt resursu izlīdzināšanu resursu optimizācijas ietvaros. Pamatojoties uz kalendāra grafiku, resursiem var noteikt ierobežojumus. Kalendāru var iestatīt **kalendāri** lapā. 

Iestatot darba ņēmējs kā projekta resursu, jūs varat izvēlēties no darba ņēmējiem, kas strādā uzņēmumā, kuram vēlaties iestatīt resursu vai izvēlēties darba ņēmēju no citiem uzņēmumiem jūsu organizācijā. Tie ir starpuzņēmumu resursi. Tālākminētajās darbībās ir paskaidrots, kā iestatīt darba ņēmējs kā projekta resursu jūsu uzņēmumā un kā tos iestatīt starpuzņēmumu projekta resursu.

### <a name="set-up-a-worker-as-a-project-resource"></a>Nodarbinātā kā projekta resursa iestatīšana

1.  Par **darbinieku** lapa, jo **darbinieku** sarakstā atlasiet darba ņēmējs, ko jūs pievienojat kā projekta resursu un darbinieka ieraksta atvēršana.
2.  Rūtī darbības noklikšķiniet uz **projektu**&gt;**Setup**&gt;**projekta iestatījuma**.
3.  Atlasiet Kalendārs un pēc tam aizveriet lapu.

Jūs varat arī norādīt resursam noklusējuma projektus kā iepriekšēju piešķiri. Iepriekšējas piešķires var izmantot, ja resursu pārvaldnieks vai projektu vadītājs iepriekš zina, kurā projektā resurss veiks darbu. Iepriekšējas piešķires arī var balstīties uz projekta sponsora vai debitora pieprasījumu. Lai veiktu projekta iepriekšēju piešķiri, lapas **Piešķirt projektus** cilnes **Projekti** sarakstā **Atlikušie projekti** atlasiet attiecīgo projektu.

### <a name="set-up-an-intercompany-resource"></a>Iestatītu starpuzņēmumu resurss

Uzstādot darba ņēmējs kā starpuzņēmumu resurss, jums jāaizpilda kreditēšanas kompānija un aizņēmumu iestatījumiem. 

**Kreditēšanas uzņēmums:**

1.  Programmā Dynamics 365 operācijām, pārliecinātos, ka kreditēšanas uzņēmums ir atlasīta, un pēc tam pabeidziet procedūrā augstāk, ", kas izveidota kā projekta resursu darba ņēmējs."
2.  Dodieties uz * Virsgrāmatu * *&gt; * * kontējumu uzstādījumi * *&gt;**starpuzņēmumu kontiem**. Click **New**.
3.  Ar * juridiska persona ID * * lauku, atlasiet kreditēšanas uzņēmums. Aizpildiet atlikušos laukus pēc vajadzības un pēc tam noklikšķiniet uz **saglabāt**.
4.  Iet * * projekta vadības un grāmatvedības * *&gt; * * uzstādīšanas * *&gt;**cenas * * &gt;**transfertcenu**.** **
5.  Uz * * transfertcenu * * formu, noklikšķiniet uz **New**, un * * aizņēmumu juridiskai personai * * lauku, atlasiet atbilstošu uzņēmumu.
6.  Ja vēlaties tikai aizdevuma aizņēmumu uzņēmuma resurss, kas izveidota šīs sadaļas sākumā **resursu** lauku, atlasiet izveidoto resursa nosaukums. Ja vēlaties veikt visus resursus uzņēmuma pieejams uzņēmuma aizņēmumiem, atstāt * * resursu * * lauku tukšu.
7.  Iet uz * projektu pārvaldības un grāmatvedības * *&gt; * * uzstādīšanas * *&gt;**projekta vadības un uzskaites parametros**, un * * starpuzņēmumu * * cilnes, kas * * starpuzņēmumu resursu plānošanas un laika grafikus * * lauku uz **Jā**.

**Aizņēmumu uzņēmumā:**

1.  Dodieties uz **projektu pārvaldības un grāmatvedības**&gt;**projekta resursus**&gt;**resursu saraksts**.
2.  Meklēšanas filtru, ievadiet vārdu, kuru izveidojāt iepriekšējā procedūrā, par aizdevumu uzņēmumam, lai pārliecinātos, ka vārds tiek iekļauts sarakstā resursu aizņēmumu uzņēmuma resurss.

## <a name="manage-resource-competencies"></a>Resursu kompetenču pārvaldība
Resursu kompetence ir būtiska daļa no resursu pārvaldību. Kompetences var izmantot kā bāzlīniju, lai noteiktu resursus, kuriem ir atbilstošā prasmju, izglītības, sertifikācijas un projektu pieredzes attiecība. Šī informācija ir jāiestata katram resursam un tā regulāri jāatjaunina. Šādā veidā var palielināt iespējas, kad konkrētas resursu kompetences tiek saskaņotas laikā projekta resursu piešķires laikā. [![Prasmes, sertifikātus, izglītības un projekta pieredzes piemēri](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Tālāk minētajās procedūrās ir paskaidrots, kā iestatīt dažas resursu kompetences. 

Lai iestatītu nodarbinātā kompetences, var izmantot saraksta lapu **Nodarbinātie** modulī Personāla vadība vai saraksta lapu **Resursi** modulī Projektu vadība un uzskaite. Procedūras, **darbinieku** saraksta lapa cilvēkresursi tiek izmantota.

### <a name="set-up-competencies-certificates"></a>Kompetenču iestatīšana: sertifikāti

1.  Saraksta lapā **Nodarbinātie** atlasiet tāda nodarbinātā rindu, attiecībā uz kuru pievienosit sertifikāta informāciju.
2.  Sadaļas Darbību rūts cilnē **Nodarbinātais**, grupā **Kompetences** noklikšķiniet uz **Sertifikāti**.
3.  Klikšķiniet **Jauns**.
4.  Laukā **Sertifikāta veids** atlasiet **PMP**.
5.  Laukā **Sākuma datums** atlasiet **01.10.2015.**.
6.  Noklikšķiniet uz **Saglabāt** un pēc tam aizveriet lapu.

### <a name="set-up-competencies-skills"></a>Komptenču iestatīšana: prasmes

1.  Saraksta lapā **Nodarbinātie** pārbaudiet, vai iepriekšējā procedūrā izmantotais nodarbinātais joprojām ir atlasīts. Pēc tam sadaļas Darbību rūts cilnē **Nodarbinātais**, grupā **Kompetences** noklikšķiniet uz **Prasmes**.
2.  Klikšķiniet **Jauns**.
3.  Laukā **Prasme** atlasiet **Projektu vadība**.
4.  Laukā **Līmenis** atlasiet **5 Eksperta līmenis**.
5.  Laukā **Līmeņa datums** atlasiet **14.01.2014.**.
6.  Laukā **Pieredzes gadu skaits** ievadiet **10**.
7.  Noklikšķiniet uz **Saglabāt** un pēc tam aizveriet lapu.

## <a name="create-a-new-project"></a>Izveidot jaunu projektu
1.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**darbvietām**&gt;**projektu vadība**.
2.  Noklikšķiniet uz **Jauns projekts** un ievadiet šādas vērtības:
    -   **Projekta tipu** – laika un materiālu
    -   **Projekta nosaukums** -XYZ Upgrade Phase 2
    -   **Projekta grupas** -TM\_NP
    -   **Projekta līguma ID** -00000002
3.  Noklikšķiniet uz **Izveidot projektu**.

### <a name="assign-a-resource-to-a-project"></a>Resursa piešķiršana projektam

1.  Noklikšķiniet uz **cilvēkresursu**&gt;**darbinieku**&gt;**darbinieku**.
2.  Sarakstā **Nodarbinātie** atlasiet tāda nodarbinātā ierakstu, kuram iepriekš veicāt kompetenču iestatīšanu, un atveriet nodarbinātā ierakstu.
3.  Sadaļas Darbību rūts cilnē **Projekts**, grupā **Iestatījumi** noklikšķiniet uz **Piešķirt projektus**.
4.  Lapā **Resursa apstiprināšanas projektu piešķires** noklikšķiniet uz cilnes **Projekti**.
5.  Šajā **projektam pievienot izvēlētajiem projektiem**, filtru Project, XYZ Upgrade Phase 2
6.  Rūtī **Atlikušie projekti** atlasiet projektu un pēc tam noklikšķiniet uz bultiņas, lai to pievienotu rūtī **Atlasītie projekti**.
7.  Aizvērt lapu.

Nepieciešamības gadījumā var arī piešķirt kategorijas resursam. Kategorijas tips ir Izmaksas vai Ieņēmumi. To nosaka jūsu organizācija. Ja nav piešķirto resursu kategorijas, Dynamics 365 operācijām uzmeklēt noklusētā kategorija stundu cenām, izmaksām un ieņēmumiem.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projekta resursu un lomu īpašību iestatīšana

Projekta vadītājs var izmantot projekta resursu sadalījuma funkcionalitāti, lai izveidotu lomas, kas nepieciešamas projektam. Lomas var izmantot, kad apstiprināti resursi ir vēl nav zināms, kad resursu rezervēšanu. Lomas var īslaicīgi reserved kā plānotos resursus tā, lai varētu turpināt projekta plānošanas posmos. 

[![Piemērs ir nozīme](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenārijs:** Contoso tika nolīgts, lai pabeigtu laika un materiālu projektu, kuram ir apstiprināta projekta privilēģijas. Jaunākais projektu vadītājs joprojām strādā pie projekta darba apjoma pabeigšanas. Resursu pārvaldītājs pašlaik ir identificēt konkrētos līdzekļus, kas tiks rezervēti darbu pie jauna projekta. Viena no lomām, projekta sponsoram pieprasīto projekta kritiska rakstura dēļ ir vecākais projekta vadītājs. Resursu pārvaldnieks jāapgūst jauni resursi un definētu lomu sistēmā, gadījumā, ja jaunākais projekta vadītājs prasa resursu informācijas projekta plānošanas laikā. 

Šādas darbības parādīt kā resursu pārvaldnieks var iestatīt vecākā projektu vadītāja lomu un piesaistīt resursa īpašības. Pēc tam šo lomu var izmantot, lai meklētu pieejamos resursus, kas atbilst nepieciešamajām resursu kompetencēm.

1.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**Setup**&gt;**resursu**&gt;**Setup lomas**.
2.  Noklikšķiniet uz **Jauns** un ievadiet šādas vērtības:
    -   **Lomas ID** -vecākais projekta vadītājs
    -   **Aprakstu** -vecākais projekta vadītājs
3.  Noklikšķiniet uz **Izveidot**.
4.  Atlasiet lomu **Vecākais projektu vadītājs** un pēc tam noklikšķiniet uz **Konfigurēt īpašības**.
5.  Laukā **Īpašību veids** atlasiet **Prasme**.
6.  Laukā **Pieejamās īpašības** ievadiet prasmi, ko meklējat.
7.  Laukā **Īpašību veids** atlasiet **Sertifikāts**.
8.  Laukā **Pieejamās īpašības** ievadiet meklējamo sertifikātu.
9.  Noklikšķiniet uz **Labi** un aizveriet lapu.

### <a name="assign-a-project-resource-to-a-project"></a>Projekta resursa piešķiršana projektam

1.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**kopējo**&gt;**projektu**&gt;**visus projektus, kas**, un atveriet **XYZ Upgrade Phase 2** projekta.
2.  Cilnē **Projekta grupa un plānošana** noklikšķiniet uz **Pievienot**.
3.  Laukā **Loma** atlasiet **Grupas dalībnieks**.
4.  Noklikšķiniet uz **Rezervēt no kalendāra**.
5.  Lapā **Resursu pieejamība** noklikšķiniet uz **Skata iestatījumi**.
6.  Lapā **Pielāgojiet skata iestatījumus** ievadiet šādas vērtības:
    -   **Datumu diapazona skata formātu** - dienā
    -   **Parādītu pieejamības apraksti** - Jā
    -   **Atlikušās jaudas displejs** - Jā
7.  Resursu sarakstā atlasiet resursu.
8.  Noklikšķiniet uz **cieto grāmatu**&gt;**pilnu jaudu**.
9.  Aizvērt lapu.

### <a name="assign-a-resource-to-a-default-role"></a>Resursa piešķiršana noklusējuma lomai

Lai palīdzētu projekta vai resursu pārvaldītājiem, var urbt uz leju tālāk par resursiem, kas var rezervēt projektam. Noklusējuma lomu var saistīt ar esošu resursu vai jauniegūtu resursu. Piemēram, kad Daniel bija nomāts, viņš bija pieredze un prasmes, lai aizpildītu biznesa analītiķis lomu. Resursu pārvaldnieks piešķirta šī loma kā Daniel noklusējuma loma. Tādēļ, resursu pārvaldnieks pievienot Daniel baseins biznesa analītiķi, kas ir pieejami darbam ar projektiem. 

Resursu rezervēšanas laikā projekta vadītāji var filtrēt lomu resursi, kas ir pieejami darbam ar projektiem. Viņi var izmantot šo informāciju kā vienu kritēriju, veicot vairāku kritēriju lēmumu analīzi resursu izpildes laikā. Viņi var pievienot arī citas resursa īpašības filtram, lai meklētu resursus, kuriem ir īpašas prasmes, izglītība un pieredze attiecīgajam projektam. 

**Scenārijs:** apstiprinātā projekta sākās, un vecākā projektu vadītāja lomu bija rezervēta kā plānoto resursu plānošanas posmā projekta laikā. Resursu pārvaldnieks ir ieguvis resursu, lai aizpildītu lomu Vecākais projektu vadītājs.

1.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**projekta resursus**&gt;**resursu saraksts**.
2.  Sarakstā **Resursi** atlasiet **Rihards Taurenis**.
3.  Noklikšķiniet uz **projekta resursu**&gt;**saglabāt**&gt;**resursu loma**.
4.  Noklikšķiniet uz **Jauns** un ievadiet šādas vērtības:
    -   **Efektīvas** - (pašreizējais datums)
    -   **Derīguma** - nekad
    -   **Loma** -vecākais projekta vadītājs
5.  Noklikšķiniet uz **Saglabāt** un pēc tam aizveriet lapu.
6.  Cilnē **Kompetences** pievienojiet prasmi **ProjectMgmt** un sertifikātu **PMP**.

## <a name="set-up-role-based-pricing"></a>Uz lomu balstītas cenu noteikšanas iestatīšana
Visas izmaksu, pārdošanas un pārsūtīšanas cenas var iestatīt lomām.

1.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**Setup**&gt;**cenu**&gt;**pārdošanas cenu (stundā)**.
2.  Click **New**.
3.  Ievadiet spēkā stāšanās datumu.
4.  Kolonnā **Loma** atlasiet lomu.
5.  Kolonnā **Cenu noteikšana** ievadiet cenu atlasītajai resursu lomai.

## <a name="form-a-project-team"></a>Veido projekta komanda
Izmantot funkcijas, kas iepriekš iestatīti projektā, projekta vadītājs ir jāpiesaista projekta lomas. Projektam var piešķirt vairākas lomas, un dinamika 365 operācijām automātiski iezīmē šīs lomas laikā atrunu, lai izvairītos no apjukuma. Piemēram, ja projekta vadītājs pieprasa trīs datorprogrammēšanas inženieru, trīs programmatūras inženieris lomas, kas ir programmatūras inženieris 1, programmatūras inženieris 2 un programmatūras inženieris 3 kā savas etiķetes tiek ģenerēts automātiski. Ja lomai iepriekš tika iestatītas lomas īpašības, tās tiek pielietotas kā filtrs resursu meklēšanas laikā. Lai precizētu meklēšanu, nepieciešamības gadījumā var pievienot papildu īpašības. 

Skata iestatījumus arī var pielāgot, lai nodrošinātu labāku pārskatu par resursu pieejamību. Ir pieejamas iespējas stundu, dienu, nedēļu, ceturkšņu un gada pieejamības attēlošanai. Pastāv arī iespēja rādīt pieejamo un atlikušo resursu noslodzi. Šī opcija ir noderīga laika pārvaldībai, novērtējot pieejamo laiku darbībām vai resursu pieejamību. 

Projekta vadītājs var atlasīt lomu lapas un tad, ja ir pieejams resurss, kas atbilst prasībai, atlasiet rezervēt resursu, lai aizpildītu lomu. Ņemiet vērā, ka resursi nav jārezervē šajā brīdī plānošanas posmā. Veidojot WBS, lomas var aizstāt ar personālu projekta resursus. Lomas tiek aizstāti ar personālu WBS resursiem, resursu iestatījumu automātiski atjaunina projekta komanda, uzskaitot un plānošanu. 

[![Projekta komandu saraksts, kas ietver lomas, gan faktiskie resursi](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektu vadītājam ir dažādas iespējas projekta resursu rezervācijai, piemēram, **Atlikusī noslodze**, **Pilna noslodze**, **Noslodzes procentuālā daļa** un **Norādiet stundas**. Šīs rezervēšanas iespējas var atcelt jebkurā laikā, ja mainās resursu piešķires. Tiek atbalstīti divi rezervāciju tipi:

-   **Grūti grāmatu** -resursu rezervēšana tika apstiprināts un apstiprināja strādāt pie saderināšanās norādīto termiņu.
-   **Mīksto grāmatu** -resursu rezervēšana tika varbūtēji ķērās pie saderināšanās norādīto termiņu.

Tālāk esošajā procedūrā izskaidrots, kā izveidot projekta grupu.

### <a name="create-a-project-team"></a>Projekta grupas izveide

1.  Saraksta lapā **Visi projekti** atlasiet projektu un pēc tam noklikšķiniet uz **Rediģēt**.
2.  Par **projekta komanda un plānošanas** cilni, jo **grafika beigu datuma** ievadiet grafika sākuma _ datumam pieskaitot vienu mēnesi. Piemēram, ja grafika sākuma datums ir 2017. gada 24 jūnijs (24/06/2017), ievadiet **24/07/2017**.
3.  Click **Add**.
4.  Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Vecākais projektu vadītājs**.
5.  Noklikšķiniet uz **Nepieciešamās kompetences**.
6.  Lapā **Īpašību izvēle** īpašības, ko iepriekš iestatījāt lomai Vecākais projektu vadītājs, tiek atlasītas pēc noklusējuma. Noklikšķiniet uz **OK**.
7.  Lapas **Pievienot projekta lomas** laukā **Resursu skaits** ievadiet **1**.
8.  Laukā **Resursi** uzmeklēšana parāda visus resursus, kuriem ir nepieciešamās kompetences. Atlasiet **Rihards Taurenis** un pēc tam noklikšķiniet uz **Izveidot**.
9.  Lapā **Projekts** noklikšķiniet uz **Pievienot**.
10. Rūts **Pievienot projekta lomas** laukā **Loma** atlasiet **Grupas dalībnieks**. Laukā **Resursu skaits** ievadiet **5**.
11. Noklikšķiniet uz **Izveidot**.
12. Lapā **Projekti** noklikšķiniet uz **Izpildīt resursu**.

## <a name="resource-capacity-synchronization"></a>Resursu noslodzes sinhronizācija
Resursu sinhronizācijas process palīdz nodrošināt to, ka kalendāra un pamatkalendāra informācija nokļūst projekta resursu plānošanā Ja kalendārs tiek mainīts, procesi veic nepieciešamos atjauninājumus projekta resursu plānošanai. Procesi arī palīdz uzlabot veiktspēju, jo kalendāru resursu informācija tiek sinhronizēta iepriekš, tādējādi resursu plānošanas informācijas atjauninājumi notiek ātrāk. Procesu plānošanu ieteicams veikt kā pakešuzdevumu, nevis atsevišķi katram procesam. Pretējā gadījumā pastāv risks, ka kāds aizmirsīs ietvertos datumus, kad pēdējo reizi tika sinhronizēta informācija. Ja netiek izmantoti ietvertie datumi, datu sinhronizācijas laikā var rasties pārrāvumi.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Kalendāra sinhronizācija](./media/projectresourcing04-1024x471.jpg)

**Synchronize resource capacity roll-ups**

Sinhronizācijas process ir paredzēts, lai sinhronizētu visu resursu kalendāra informāciju. Šajā informācijā ietilpst pamatkalendāra informācija par visām izmaiņām projekta resursu kalendāra noslodzes tabulā. Ja projekta ietvaros tiek pievienoti jauniem resursiem, sinhronizācija nodrošina atjauninātu kalendāru informācija ir pieejama. Šo sinhronizāciju var veikt jebkurā laikā. 

Ieteicams izmantot partijas. Opcijas ir pieejamas, sinhronizējot noslodzes rezervācijas.

-   Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**periodiskā**&gt;**jaudas sinhronizācija**&gt;**sinhronizēt resursu noslodzes roll ups**.

| Opcija | apraksts                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jā    | Sinhronizēt visus resursu datus ar kalendāra un pamatkalendāra informāciju un aizstāt visu informāciju projekta resursu noslodzes kalendārā.                                                  |
| Nē     | Sinhronizēt resursu datus, pamatojoties uz datumu intervāla kodu un norādītajiem sākuma un beigu datumiem. Šī opcija nedzēš esošos datus un atjaunina informāciju tikai par jaunpievienotiem resursiem. |

[![Sinhronizācijas process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Lomu iestatīšana WBS veidnēs
Projektu vadītāji var iestatīt WBS veidnes, kuras var lietot, izveidojot WBS jauniem projektiem. Projektu vadītāji var pievienot lomas, veidojot veidni. Izmantojiet šo procedūru, lai piešķirtu lomu WBS template.* * * *

1.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**Setup**&gt;**projektu**&gt;**darba sadalījuma struktūra veidnes**.
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
<td>Automātiski pievienot plānotos resursus, izmantojot lomas, kas ir saistītas ar uzdevumu. Dinamika 365 operācijām automātiski iesaka plānotos resursus, izmantojot vairāku kritēriju lēmumu analīzi, kas ir bāzēta uz lomām. Pēc lomu un darba (stundas) iestatīšanas uzdevumiem WBS struktūrā un struktūras nodošanas noklikšķiniet uz <strong>Automātiski ģenerēt grupu</strong>. Nepieciešamais plānoto resursu skaits tiek pievienots WBS struktūrai un cilnē <strong>Projekta un grupas plānošana</strong>.</td>
</tr>
<tr class="odd">
<td>Resurss (nolaižamais saraksts)</td>
<td>Lapā <strong>Palaist resursu piešķiri </strong>varat atlasīt resursus stingrai vai vieglai rezervācijai, pamatojoties uz noteiktu ilgumu. Jūs varat pielāgot skata iestatījumus, lai skatītu un iestatītu resursu darbību ilgumu. Jūs varat atlasīt un piešķirt resursus darba pakotņu līmenī, izmantojot šādas opcijas:
<ul>
<li><strong>Pieņemt</strong> — apstiprināt tāda resursa izmaiņas, kas ir piešķirts uzdevumam.</li>
<li><strong>Atcelt</strong> — atcelt tāda resursa izmaiņas, kas ir piešķirts uzdevumam.</li>
<li><strong>Automātiski piešķirt</strong> – šo opciju atlasa pieejams personāls resurss ar atbilstošu lomu, lai atlasīto uzdevumu.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**projektu**&gt;**visus projektus, kas**.
2.  Sarakstā atlasiet projektu **XYZ jaunināšanas fāze 2**.
3.  Noklikšķiniet uz **plāns**&gt;**aktivitātes**&gt;**darba sadalījuma struktūra**.
4.  Noklikšķiniet uz **Jauns**, lai pievienotu šādas pirmā līmeņa aktivitātes WBS struktūrā:
    -   Uzsākšana
    -   Plānošana
    -   Izpilda
    -   Pārraudzīšana un kontrole
    -   Tuva

5.  Iestatīt datumu un pūles (stundas), kā parādīts sekojošajā attēlā. [![Datumus un intensitātes noteikšanas](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
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
16. Noklikšķiniet uz **Soft piešķirt**&gt;**pilnu jaudu**.
17. Noklikšķiniet uz **Saglabāt** un aizveriet lapu. 

> [!NOTE] 
> Jūs nesaņemat brīdinājums, ka norādītā resursa tagad ir 2, jo tādu resursu skaitu, kas paliek pie 1.
18. Lapā **Darba sadalījuma struktūra ** pārbaudiet resursa piešķiri WBS struktūrā un pēc tam noklikšķiniet uz **Saglabāt**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resursu izpilde plānotiem resursiem
Projektu vadītājs var plānot nepieciešamo resursu lomas projektam. Resursu pārvaldnieks redzēs šos plānotos resursus kā pieprasījumus lapā **Resursu izpilde** un var piešķirt faktiskos resursus.

1.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**projektu**&gt;**visus projektus, kas**.
2.  Sarakstā atlasiet projektu **XYZ jaunināšanas fāze 2**.
3.  Noklikšķiniet uz **Projekts**.
4.  Noklikšķiniet uz **Rediģēt**.
5.  Par **projekta komanda un plānošanas** tab, * * * * noklikšķiniet **pievienot**.
6.  Dialoglodziņā **Pievienot lomas** atlasiet lomu **Programmatūras izstrādātājs**.
7.  Noklikšķiniet uz **Izveidot**.
8.  Aizveriet projekta lapu.
9.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**projekta resursus**&gt;**resursu piepildījumu**.
10. Atlasiet **Programmatūras izstrādātājs 1** projektam **XYZ jaunināšanas projekta fāze 2**.
11. Atlasiet nodarbināto un pēc tam noklikšķiniet uz **Piešķirt**.
12. Pārbaudiet, vai rinda vienumam **Programmatūras izstrādātājs 1** ir izdzēsta projektam **XYZ jaunināšanas projekta fāze 2**.
13. Cilnē **Projekta grupa un plānošana** projektam **XYZ jaunināšanas fāze 2** pārbaudiet, vai nodarbinātais, kuru atlasījāt 11. solī, ir pievienots kā **Programmatūras izstrādātājs**.

## <a name="requests-for-project-resources"></a>Projekta resursu pieprasījumus
Projekta resursu plānošanas funkcionalitāti atbalsta tikai resursu pārvaldītājiem izplatīt personāls resursiem saistībām vai projektiem. Lai iespējotu šo funkcionalitāti, veicot šādus uzdevumus, vai pārliecinātos, ka tās ir pabeigušas.

-   Iestatiet numuru sērijas.
-   Projektu vadības un grāmatvedības darbplūsmas iestatīšana.
-   Nodrošina resursu pieprasījuma darbplūsmu.

Pēc tam, kad esat pārbaudījis vai pabeigto uzdevumu iepriekš, pēc nepieciešamības var izpildīt šādus uzdevumus.

-   Izveidot resursu pieprasījumu no mīksta iegrāmatoti personāls resursu.
-   Uzraudzīt resursu pieprasījumu.
-   Izpildītu resursu pieprasījumu.
-   WBS lūgt personālu resurss.
-   Rezervēt resursu projektu bez personāls resursu pieprasījumu.

## <a name="monitor-project-teams"></a>Uzraudzīt projektu komandas
1.  Noklikšķiniet uz **projektu pārvaldības un grāmatvedības**&gt;**projektu**&gt;**visus projektus, kas**.
2.  Projektu sarakstā noklikšķiniet uz saites **Projekta ID** projektam **XYZ jaunināšanas fāze 2**.
3.  Kopsavilkuma cilnē **Projekta grupa un plānošana** pārbaudiet, vai minētie projekta resursi ir pareizi.



