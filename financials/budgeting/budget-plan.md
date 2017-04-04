---
title: "Budžeta plānošana"
description: "Šī laboratorija mērķis ir paredzēt vadītā skatīt Microsoft Dynamics 365 darbības funkcionalitātes atjauninājumus budžeta plānošanas jomā. Šī uzdevuma nolūks ir ilustrēt budžeta plānošanas moduļa ātras konfigurēšanas piemēru un demonstrēt, kā var paveikt budžeta plānošanu, izmantojot šo konfigurāciju.  Šī laboratorija koncentrēsies tieši uz šādu darījumu pamatprocesiem vai uzdevumus - radot organizatorisko hierarhiju budžeta plānošanu un konfigurēšanu lietotāju drošības - nosakot budžeta plānu scenārijus, budžeta plānu kolonnas, izkārtojumus un Excel veidnes - izveidot un aktivizēt budžeta plānošanas procesā - radot budžeta plānu dokumentu, vilkšana reālos datus no Virsgrāmatas - izmantojot piešķīrumu pielāgot budžeta plānu dokumentu dati - Editing budžeta plānu dokumentu datus programmā Excel"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Budžeta plānošana

Šī laboratorija mērķis ir paredzēt vadītā skatīt Microsoft Dynamics 365 darbības funkcionalitātes atjauninājumus budžeta plānošanas jomā. Šī uzdevuma nolūks ir ilustrēt budžeta plānošanas moduļa ātras konfigurēšanas piemēru un demonstrēt, kā var paveikt budžeta plānošanu, izmantojot šo konfigurāciju.  Šī laboratorija koncentrēsies tieši uz šādu darījumu pamatprocesiem vai uzdevumus - radot organizatorisko hierarhiju budžeta plānošanu un konfigurēšanu lietotāju drošības - nosakot budžeta plānu scenārijus, budžeta plānu kolonnas, izkārtojumus un Excel veidnes - izveidot un aktivizēt budžeta plānošanas procesā - radot budžeta plānu dokumentu, vilkšana reālos datus no Virsgrāmatas - izmantojot piešķīrumu pielāgot budžeta plānu dokumentu dati - Editing budžeta plānu dokumentu datus programmā Excel 

<a name="prerequisites"></a>Priekšnosacījumi 
------------------

Šī apmācība, jums vajadzēs piekļūt Dynamics 365 par operatīvajai videi ar Contoso demo datu un nodrošināta kā administrators instancē. Nelietojiet, privātas pārlūka režīmā lab - Izrakstīties no otra konta pārlūkprogrammā, ja nepieciešams, un jāpiesakās ar Dynamics 365 darbību administratora akreditācijas datus. Kad ieejot Dynamics 365 operācijām, tu **ir** atzīmējiet izvēles rūtiņu "Saglabāt mani pieteicies". Tādējādi tiks izveidots pastāvīgs sīkfails, kas pašlaik nepieciešams programmai Excel. Ja jūs pieteikties Dynamics 365 operācijām, izmantojot pārlūkprogrammu, kas nav IE, tad jums tiks piedāvāts pieteikties programmā Excel App. Kad programmā Excel noklikšķināsit uz Pierakstīties, pārlūkprogrammā IE tiks atvērts uznirstošais logs. Pierakstīšanās laikā **IR** jāatzīmē izvēles rūtiņa Saglabāt manu pieteikuminformāciju. Ja programmā Excel noklikšķinot uz Pierakstīties, netiek atvērta neviena uzvedne, pārlūkprogrammā IE notīriet sīkfailu kešatmiņu.

## <a name="scenario-overview"></a>**Scenario overview**
Jūlija ir grāmatvede uzņēmumā Contoso Entertainment Systems (DEMF) Vācijā. Tuvojas 2016. finanšu gads, tādēļ viņai ir jāiestata uzņēmuma budžets nākamajam gadam. Tālāk ir aprakstīts budžeta sagatavošanas process.

1.  Jūlija izmanto iepriekšējā gada faktiskās summas kā sākuma punktu, lai izveidotu budžetu.
2.  Pamatojoties uz iepriekšējā gada faktiskajām summām, viņa aprēķina summas nākamā gada 12 mēnešiem.
3.  Jūlija pārskata budžetu kopā ar galveno grāmatvedi. Kad tas ir izdarīts, viņa veic nepieciešamās korekcijas budžeta plānā un pabeidz budžeta sagatavošanu.

Budžeta plānošanas scenārijs konfigurācijas shēma izskatās šādi:

![Screenshot1](./media/screenshot1-300x152.png)

Julia izmanto šādas Excel veidni, lai sagatavotu budžetu:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>1. vingrinājums. Konfigurācija
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**1. uzdevums — Veidot organizācijas hierarhijai**
Viss budžeta izstrādes process notiek finanšu daļā, tādēļ Jūlijai ir jāizveido ļoti vienkārša organizācijas hierarhija — kas sastāv tikai no finanšu daļas. 1.1. Naviģējiet līdz organizācijas hierarhijas (organizācijas administrācija &gt;organizācijām &gt;organizācijas hierarhijas) un noklikšķiniet uz pogas Jauns

![Screenshot3](./media/screenshot3.png) 

1.2. Ievadiet organizācijas hierarhijai nosaukumu un noklikšķiniet uz pogas piešķirt mērķi

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Atlasiet budžeta plānošanas mērķi, noklikšķiniet uz pogas Add un piešķirt jaunizveidotās organizācijas hierarhijai: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Atkārtojiet iepriekšējo darbību organizācijas nolūkam Drošība. Kad darbība ir pabeigta, aizveriet formu.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Formā Organizācijas hierarhijas noklikšķiniet uz pogas Skats. Sadaļā Hierarhijas noformētājs noklikšķiniet uz Rediģēt un izveidojiet hierarhiju, noklikšķinot uz pogas Ievietot.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Atlasiet budžeta hierarhijai vienumu Finanšu nodaļa. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Pēc tam noklikšķiniet uz pogas Publicēt un Aizvērt. Atlasiet 1/1/2015 kā hierarhijas publicēšanas spēkā stāšanās datumu.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>2. uzdevums. Lietotāja drošības konfigurēšana
Budžeta plānošanas procesā izmanto īpašas drošības politikas, lai konfigurētu piekļuvi budžeta plāna datiem. Jūlijai sev ir jāpiešķir piekļuve finanšu budžeta plāniem. 2.1. Pārslēgties uz DEMF juridiska persona kontekstā: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Naviģējiet uz budžeta līdzekļu &gt;Setup &gt;budžeta plānošanu &gt;budžeta plānošanas konfigurāciju. Parametri cilnē iestatiet vērtību drošības modelis pamatojoties uz drošības organizācijas [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Dodieties uz sistēmas administrēšanu &gt;lietotājiem &gt;lietotājiem. Piešķiriet lietotājam Administrators (Jūlija Funderburka) lomu Budžeta pārvaldnieks. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Izvēlēties lietotāja lomai, un noklikšķiniet uz piešķirt organizācijām [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2.5. Atlasiet Atsevišķi piešķirt piekļuvi noteiktām organizācijām. Atlasiet organizācijas hierarhiju, ko izveidojāt pirmās darbības laikā. Izvēlēties soda mezglu un uz dotāciju ar bērniem pogu ***svarīgi!*** *-Pārliecinieties, vai esat DEMF juridiska persona kontekstā, veicot šo uzdevumu, attiecināta uz vienu juridisku vienību organizatorisko drošības*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>3. uzdevums. Scenāriju izveide
3.1. Naviģējiet uz budžeta līdzekļu&gt;Setup &gt;budžeta plānošanu &gt;budžeta plānošanas konfigurāciju. Lapā Scenāriji pārskatiet scenārijus, ko izmantosim tālāk šajā uzdevumā: Iepriekšējā gada faktiskās izmaksas un Budžeta. *Piezīme. Ja nepieciešams, šajā uzdevumā var izveidot un izmantot jaunus scenārijus.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*Piezīme: Julia budžeta sagatavošanai nelieto oficiālas apstiprināšanas procesu, mēs izlaidīs darbplūsmas posmiem un darbplūsmas posmiem setup šajā laboratorijā un izmantos esošo iestatījumu Automātiskā – apstiprināt darbplūsmu. Sk. papildinājumu šajā darbplūsmā konfigurācijai.*

## <a name="task-4-create-budget-plan-columns"></a>4. uzdevums. Budžeta plāna kolonnu izveide
Budžeta plāna kolonnas ir atkarīgas no naudas vai daudzuma kolonnām, kuras var izmantot budžeta plāna dokumenta izkārtojumā. Mūsu piemērā ir jāizveido kolonna scenārijam Iepriekšējā gada faktiskās izmaksas un 12 kolonnas katram mēnesim budžeta gadā. Kolonnas var izveidot vai nu vienkārši noklikšķinot uz pogas Pievienot un ievadot vērtības, vai arī, izmantojot vienumu Datu elements. Šajā uzdevumā vērtību ierakstītīšanai mēs izmantosim vienumu Datu elements. 4.1. Šajā budžeta līdzekļu&gt;Setup &gt;budžeta plānošanu &gt;budžeta plānošanas konfigurācijas atvērtajā kolonnas lapā. Noklikšķiniet uz Office pogas augšējā labajā stūrī, veidlapas un izvēlēties kolonnas (bezfiltra) [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. Sistēma atvērs Excel darbgrāmatu, kas jāizmanto vērtību aizpildīšanai. Ja tiek pieprasīts, noklikšķiniet uz iespējot rediģēšanai un uzticēties šo app [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Mums būs nepieciešams vairāk kolonnu aizpildīt vērtības. Pievienot kolonnu režģa rūtī labajā pusē noklikšķiniet uz noformējums: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Mazais zīmuļu pogu blakus PlanColumns, lai redzētu pieejamās kolonnas pievienot režģa [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Veiciet dubultklikšķi uz katru pieejamo lauku pievienot tos atlasītie lauki, un noklikšķiniet uz atjaunināt [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. Excel tabulā pievienojiet visas kolonnas, kas ir jāizveido. Programmā Excel lietojiet līdzekli Automātiskais aizpildījums, lai ātri pievienotu rindas. Pārliecinieties, vai kā daļa no tabulas pievieno rindas (izmantojot vertikālo ritjoslu, jābūt redzamiem uz režģa kolonnu galvenes) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4.7. Atgriezieties Dynamics 365 operācijām un atsvaidziniet lapu. Tiks parādītas publicēto vērtības dinamika 365 operācijām. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>5. uzdevums. Budžeta plāna dokumenta izkārtojumu un veidņu izveide
Izkārtojums definē, kā izskatīsies budžeta plāna dokumenta rindu režģis, kad lietotājs atver budžeta plāna dokumentu. Budžeta plāna dokumentu izkārtojumu var arī pārslēgt, lai datus aplūkotu no dažādiem aspektiem. Tā kā budžeta plāna dokumentam lietojamās kolonnas ir definētas, Jūlijai ir jāizveido budžeta plāna dokumenta izkārtojums, kas izskatīsies līdzīgi Excel tabulai, ko viņa izmanto, lai izveidotu budžeta datus (skatiet šī uzdevuma sadaļu Scenārija pārskats). 5.1. Šajā budžeta līdzekļu&gt;Setup &gt;budžeta plānošanu &gt;budžeta plānošanas konfigurācijas atvērt izkārtojumus lapu. Izveidojiet jaunu izkārtojumu ikmēneša budžeta ierakstam.

-   Atlasiet dimensiju kopu MA + BU, lai izkārtojumā iekļautu vienumu Galvenie konti un Biznesa vienības.
-   Norādiet visas budžeta plāna kolonnas, ko izveidojāt iepriekšējā darbībā sadaļā Elementi. Iestatiet, lai visas summas, izņemot iepriekšējā gada faktiskās izmaksas, būtu rediģējamas.
-   Noklikšķiniet uz pogas Apraksti, lai atlasītu, kuras finanšu dimensijas ir jāparāda rindā Apraksti.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) balstoties uz budžeta plānu izkārtojuma definīcijai, mēs varam izveidot Excel veidnei, lai izmantotu kā alternatīvs veids, kā labot budžeta dati. Excel veidnei ir jāatbilst budžeta plāna izkārtojuma definīcijai. Pēc Excel veidnes ģenerēšanas, budžeta plāna izkārtojumu nevar rediģēt, tāpēc šis uzdevums jāveic pēc tam, kad visi izkārtojuma komponenti ir definēti. 5.2. 5.1. izveidots izkārtojumu. Soli, noklikšķiniet uz pogas veidne &gt;ģenerēt. Apstipriniet brīdinājuma ziņojumu. Lai apskatītu šo veidni, noklikšķiniet uz veidnes &gt;skats. *Piezīme: Pārliecinieties, ka izvēlēties "Saglabāt kā", un atlasiet vietu, kur veidne ir jāglabā, lai to rediģētu. Ja lietotājs atlasa "Atvērt" logu, nesaglabājot izmaiņas, izmaiņas, kas darīts, lai failu netiks saglabāti, kad fails tiek aizvērts.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;Papildu solis&gt; modificējiet Excel veidni, lai tā izskatās vairāk lietotājam draudzīgs-pievienot kopsummas formulas, galvenes lauki, formatēšanas, utt. Saglabāt izmaiņas un augšupielādēt failu uz budžeta plānu izkārtojumu, noklikšķinot uz Izkārtojums &gt;augšupielādēt [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>6. uzdevums. Budžeta plānošanas procesa izveide
Jūlijai ir jāizveido un jāaktivizē jauns budžeta plānošanas process, apvienojot iepriekš minētos visus iestatījumus, lai sāktu ievadīt budžeta plānus. Budžeta plānošanas procesā definē, kādas budžeta organizācijas, darbplūsma, izkārtojumi un veidnes tiks lietotas budžeta plānu izveidē. 6.1. Naviģējiet uz budžeta līdzekļu &gt;Setup &gt;budžeta plānošanu &gt;budžeta plānošanas procesā un izveidot jaunu ierakstu.

-   Budžeta plānošanas process — DEMF budžeta veidošana 2016. finanšu gadam
-   Budžeta cikls — 2016. finanšu gads
-   Virsgrāmata — DEMF
-   Noklusējuma konta struktūra — ražošanas peļņa un zaudējumi
-   Organizācijas hierarhija — atlasiet uzdevuma sākumā izveidoto hierarhiju
-   Budžeta plānošanas darbplūsma — piešķiriet Automātiska — Darbplūsmas apstiprināšana finanšu nodaļai
-   Budžeta plānošanas stadijas nosacījumos un veidnēs katrai darbplūsmas budžeta plānošanas stadijai jāatlasa, vai ir atļauta rindu pievienošana un modificēšana, un kādi izkārtojumi ir jāizmanto pēc noklusējuma.

*Piezīme. Varat izveidot papildu dokumentu izkārtojumus un piešķirt tos, lai tie būtu pieejami budžeta plānošanas darbplūsmas posmā, noklikšķinot uz pogas Alternatīvie izkārtojumi.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Atlasiet darbības &gt;aktivizēt, lai aktivizētu šo budžetu plānošanas, darbplūsmas [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>2. uzdevums. Procesa simulācija
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>7. uzdevums. Ģenerējiet budžeta plāna sākotnējos datus no Virsgrāmatas.
7.1. Naviģējiet uz budžeta līdzekļu &gt;periodiskā &gt;izveidot budžeta plānu, no Virsgrāmatas. Aizpildiet periodiskā procesa parametrus un noklikšķiniet uz pogas Ģenerēt. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Naviģējiet uz budžeta līdzekļu &gt;budžeta plānus, lai atrastu budžeta plānu izveidoja Generate procesu. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7.3. Atveriet dokumenta informāciju, noklikšķinot uz hipersaites Dokumenta numurs. Budžeta plāna tiek rādīta atbilstoši definīcijai izkārtojumā, kas radīti šīs laboratorijas [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>8. uzdevums. Pašreizējā gada budžeta izveide, pamatojoties uz iepriekšējā gada faktiskajām summām
Budžeta plānā var izmantot sadalījuma metodes, lai viegli kopētu budžeta plānu informāciju no viena scenārija citā/izplatīt tos dažādos periodos/sadalītu pa dimensijām. Mēs izmantosim sadalījumus, lai izveidotu pašreizējā gada budžetu no iepriekšējā gada faktiskajam summām. 8.1. Budžeta plāna dokumenta režģa pick visas rindas un noklikšķiniet uz pogas piešķirt budžeta [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8.2. Atlasiet sadalījuma metodi, perioda atslēgu, avota un mērķa scenāriju un noklikšķiniet uz piešķirt 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

Iepriekšējo gadu faktiskās summas tiek kopēts kārtējā gada budžetu un piešķirt tiem periodiem, izmantojot Sales līkne perioda atslēgu pāri. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>9. uzdevums. Budžeta plāna dokumenta koriģēšana, izmantojot programmu Excel, un dokumenta pabeigšana
9.1. Noklikšķiniet uz pogas darblapas, lai programmā Excel atvērtu dokumenta saturu

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Kad tiek atvērta Excel darbgrāmata, pielāgojiet budžeta plāna dokumenta skaitļus un noklikšķiniet uz pogas Publicēt.

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Atgriezties pie budžeta plānu dokumentu Dynamics 365 operācijām. Noklikšķiniet uz darbplūsmas &gt;iesniegt automātiski apstiprināt dokumentu

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

Kad darbplūsma ir pabeigta, budžeta plānu dokumentu skatuves mainīsies uz apstiprināts. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Pielikums
========

### <a name="auto-approve-workflow-configuration"></a>Darbplūsmas konfigurācijas automātiska apstiprināšana

. Budžeta &gt;Setup &gt;budžeta plānošanu &gt;budžeta darbplūsmas, izveidot jaunu darbplūsmu veidnes budžeta plānošanas, darbplūsmas, izmantojot:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

Šīs darbplūsmas satur tikai viens uzdevums – skatuves pārejas budžeta plāns 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Saglabāt un aktivizēt darbplūsmu. 

B. Naviģējiet uz budžeta līdzekļu &gt;Setup &gt;budžeta plānošanu &gt;budžeta plānošanas konfigurāciju. Stadijas cilnē izveidot 2 posmos – sākotnējās un Submitted 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Naviģējiet uz budžeta līdzekļu &gt;Setup &gt;budžeta plānošanu &gt;budžeta plānošanas konfigurāciju. Cilnē darbplūsmas posmiem darbplūsma automātiski saistīt-apstiprināt izveidoja solis ar sākotnējo un Submitted posmi 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  


