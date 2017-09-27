---
title: "Budžeta plānošana"
description: "Šī uzdevuma mērķis ir jūs iepazīstināt ar funkcionalitātes atjauninājumiem Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise apgabalā Budžeta plānošana. Šī uzdevuma nolūks ir ilustrēt budžeta plānošanas moduļa ātras konfigurēšanas piemēru un demonstrēt, kā var paveikt budžeta plānošanu, izmantojot šo konfigurāciju.  Šajā uzdevumā galvenā uzmanība ir pievērsta tālāk uzskaitītajiem biznesa procesiem vai uzdevumiem. -    - Organizācijas hierarhijas izveidošana budžeta plānošanai un lietotāju drošības konfigurēšanai   - Budžeta plāna scenāriju, budžeta plāna kolonnu, izkārtojumu un Excel veidņu definēšana   - Budžeta plānošanas procesa izveidošana un aktivizēšana   - Budžeta plāna dokumenta izveidošana, izgūstot faktiskos datus no virsgrāmatas   - Sadalījumu izmantošana, lai koriģētu budžeta plāna dokumenta datus   - Budžeta plāna dokumenta datu rediģēšana programmā Excel"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 608ec87233acb05b0d46e367bcb7cd14985d7813
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="budget-planning"></a>Budžeta plānošana

[!include[banner](../includes/banner.md)]


Šī uzdevuma mērķis ir jūs iepazīstināt ar funkcionalitātes atjauninājumiem Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise apgabalā Budžeta plānošana. Šī uzdevuma nolūks ir ilustrēt budžeta plānošanas moduļa ātras konfigurēšanas piemēru un demonstrēt, kā var paveikt budžeta plānošanu, izmantojot šo konfigurāciju.  Šajā uzdevumā galvenā uzmanība ir pievērsta tālāk uzskaitītajiem biznesa procesiem vai uzdevumiem. -    - Organizācijas hierarhijas izveidošana budžeta plānošanai un lietotāju drošības konfigurēšanai   - Budžeta plāna scenāriju, budžeta plāna kolonnu, izkārtojumu un Excel veidņu definēšana   - Budžeta plānošanas procesa izveidošana un aktivizēšana   - Budžeta plāna dokumenta izveidošana, izgūstot faktiskos datus no virsgrāmatas   - Sadalījumu izmantošana, lai koriģētu budžeta plāna dokumenta datus   - Budžeta plāna dokumenta datu rediģēšana programmā Excel 

<a name="prerequisites"></a>Priekšnosacījumi 
------------------

Lai izpildītu šo apmācību, jums ir jāpiekļūst Dynamics 365 for Finance and Operations videi ar Contoso demonstrācijas datiem un jums ir jābūt norādītam kā šīs instances administratoram. Šī uzdevuma izpildē nedrīkst izmantot privātās pārlūkošanas režīmu — ja tas ir nepieciešams, pārlūkprogrammā izrakstieties no visiem citiem kontiem un pēc tam pierakstieties, izmantojot Dynamics 365 for Finance and Operations administratora akreditācijas datus. Pierakstoties programmatūrā Dynamics 365 for Finance and Operations, jums **IR JĀATZĪMĒ** izvēles rūtiņa Saglabāt manu pieteikuminformāciju. Tādējādi tiks izveidots pastāvīgs sīkfails, kas pašlaik nepieciešams programmai Excel. Ja pierakstāties programmatūrā Dynamics 365 for Finance and Operations, izmantojot citu pārlūkprogrammu, izņemot IE, tiek piedāvāts pierakstīties programmā Excel. Kad programmā Excel noklikšķināsit uz Pierakstīties, pārlūkprogrammā IE tiks atvērts uznirstošais logs. Pierakstīšanās laikā **IR** jāatzīmē izvēles rūtiņa Saglabāt manu pieteikuminformāciju. Ja programmā Excel noklikšķinot uz Pierakstīties, netiek atvērta neviena uzvedne, pārlūkprogrammā IE notīriet sīkfailu kešatmiņu.

## <a name="scenario-overview"></a>**Scenārija apskats**
Jūlija ir grāmatvede uzņēmumā Contoso Entertainment Systems (DEMF) Vācijā. Tuvojas 2016. finanšu gads, tādēļ viņai ir jāiestata uzņēmuma budžets nākamajam gadam. Tālāk ir aprakstīts budžeta sagatavošanas process.

1.  Jūlija izmanto iepriekšējā gada faktiskās summas kā sākuma punktu, lai izveidotu budžetu.
2.  Pamatojoties uz iepriekšējā gada faktiskajām summām, viņa aprēķina summas nākamā gada 12 mēnešiem.
3.  Jūlija pārskata budžetu kopā ar galveno grāmatvedi. Kad tas ir izdarīts, viņa veic nepieciešamās korekcijas budžeta plānā un pabeidz budžeta sagatavošanu.

Budžeta plānošanas konfigurācijas shēma scenārijam izskatās šādi:

![Budžeta plānošanas konfigurācijas shēma](./media/screenshot1-300x152.png)

Budžeta sagatavošanai Jūlija izmanto šādu Excel veidni:

[![Excel veidne](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>1. vingrinājums. Konfigurācija
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**1. uzdevums. Organizācijas hierarhijas izveide**
Viss budžeta izstrādes process notiek finanšu daļā, tādēļ Jūlijai ir jāizveido ļoti vienkārša organizācijas hierarhija — kas sastāv tikai no finanšu daļas. 1.1. Pārejiet uz sadaļu Organizācijas hierarhijas (Organizācijas administrēšana &gt; Organizācijas &gt; Organizācijas hierarhijas) un noklikšķiniet uz pogas Jauns

![Organizācijas hierarhija](./media/screenshot3.png) 

1.2. Ievadiet organizācijas hierarhijas nosaukumu un noklikšķiniet uz pogas Piešķiršanas nolūks

[![Vārds](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Atlasiet vienumu Budžeta plānošanas nolūks, noklikšķiniet uz pogas Pievienot un piešķiriet jaunizveidoto organizācijas hierarhiju: 

[![Piešķiršanas nolūks](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Atkārtojiet iepriekšējo darbību organizācijas nolūkam Drošība. Kad darbība ir pabeigta, aizveriet formu.

[![Drošības organizācija](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Formā Organizācijas hierarhijas noklikšķiniet uz pogas Skats. Sadaļā Hierarhijas noformētājs noklikšķiniet uz Rediģēt un izveidojiet hierarhiju, noklikšķinot uz pogas Ievietot.

[![Ievietot](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Atlasiet budžeta hierarhijai vienumu Finanšu nodaļa. 

[![Finansēt](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Pēc tam noklikšķiniet uz pogas Publicēt un Aizvērt. Atlasiet 1/1/2015 kā hierarhijas publicēšanas spēkā stāšanās datumu.

[![Spēkā stāšanās datums](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>2. uzdevums. Lietotāja drošības konfigurēšana
Budžeta plānošanas procesā izmanto īpašas drošības politikas, lai konfigurētu piekļuvi budžeta plāna datiem. Jūlijai sev ir jāpiešķir piekļuve finanšu budžeta plāniem. 

2.1. Pārslēdzieties uz DEMF juridiskās personas kontekstu. 


2.2. Pārejiet uz Budžeta veidošana &gt; Iestatīšana &gt; Budžeta plānošana &gt; Budžeta plānošanas konfigurācija. Cilnē Parametri vienumam Drošības modeļa vērtība iestatiet vērtību Pamatojoties uz drošības organizāciju 

[![Parametri](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Dodieties uz Sistēmas administrēšana &gt; Lietotāji &gt; Lietotāji. Piešķiriet lietotājam Administrators (Jūlija Funderburka) lomu Budžeta pārvaldnieks. 

[![Budžeta pārvaldnieks](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Izvēlieties lietotāja lomu un noklikšķiniet uz Piešķirt organizācijas 

[![Piešķirt organizāciju](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Atlasiet Atsevišķi piešķirt piekļuvi noteiktām organizācijām. Atlasiet organizācijas hierarhiju, ko izveidojāt pirmās darbības laikā. Atlasiet zaru Finanses un noklikšķiniet uz pogas Piešķirt ar apakšelementiem 

***Svarīgi!*** *Veicot šo uzdevumu, pārliecinieties, ka ir atlasīts DEMF juridiskās personas konteksts, jo organizācijas drošība tiek lietota atkarībā no juridiskajās personas* 

[![Piešķirt piekļuvi](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>3. uzdevums. Scenāriju izveide
3.1. Pārejiet uz Budžeta veidošana&gt;Iestatīšana &gt; Budžeta plānošana &gt; Budžeta plānošanas konfigurācija. Lapā Scenāriji pārskatiet scenārijus, ko izmantosim tālāk šajā uzdevumā: Iepriekšējā gada faktiskās izmaksas un Budžeta. 

*Piezīme. Ja nepieciešams, šajā uzdevumā var izveidot un izmantot jaunus scenārijus.* 

[![Jauni scenāriji](./media/screenshot15.png)](./media/screenshot15.png) 

*Piezīme. Jūlija neizmanto oficiālu apstiprināšanas procesu budžeta sagatavošanai, tādēļ šajā uzdevumā izlaidīsim iestatīšanas darbību vienumam Darbplūsmas, Stadijas un Darbplūsmas stadijas un izmantosim esošos iestatījumus vienumam Automātiski apstiprināt darbplūsmu. Informāciju par šīs darbplūsmas konfigurāciju skatiet pielikumā.*

## <a name="task-4-create-budget-plan-columns"></a>4. uzdevums. Budžeta plāna kolonnu izveide
Budžeta plāna kolonnas ir atkarīgas no naudas vai daudzuma kolonnām, kuras var izmantot budžeta plāna dokumenta izkārtojumā. Mūsu piemērā ir jāizveido kolonna scenārijam Iepriekšējā gada faktiskās izmaksas un 12 kolonnas katram mēnesim budžeta gadā. Kolonnas var izveidot vai nu vienkārši noklikšķinot uz pogas Pievienot un ievadot vērtības, vai arī, izmantojot vienumu Datu elements. Šajā uzdevumā vērtību ierakstītīšanai mēs izmantosim vienumu Datu elements. 

4.1. Pārejiet uz Budžeta veidošana&gt;Iestatīšana &gt; Budžeta plānošana &gt; Budžeta plānošanas konfigurācija un atveriet lapu Kolonnas. Formas augšējā labajā stūrī noklikšķiniet uz Office pogas un atlasiet vienumu Kolonnas (bez filtra) 

[![Kolonnas bez filtra](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Sistēma atvērs Excel darbgrāmatu, kas jāizmanto vērtību aizpildīšanai. Ja tiek pieprasīts, noklikšķiniet uz Iespējot rediģēšanu un Uzticēties šai programmai 

[![Iespējot rediģēšanu](./media/screenshot18.png)](./media/screenshot18.png) 

[![Uzticēties šai programmai](./media/screenshot17.png)](./media/screenshot17.png)

4.3. Mums būs nepieciešamas papildu kolonnas, lai aizpildītu vērtības. Labajā rūtī noklikšķiniet uz Dizains, lai režģim pievienotu kolonnu: 

[![Dizains](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Noklikšķiniet uz mazās zīmuļa pogas blakus vienumam PlanColumns, lai apskatītu pieejamās kolonnas, ko var pievienot režģim 

[![Rediģēt](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Veiciet dubultklikšķi uz katra pieejamā lauka, lai to pievienotu vienumam Atlasītie lauki, un pēc tam noklikšķiniet uz Atjaunināt 

![Grāmatot](./media/screenshot21.png)](./media/screenshot21.png) 

4.6. Excel tabulā pievienojiet visas kolonnas, kas ir jāizveido. Programmā Excel lietojiet līdzekli Automātiskais aizpildījums, lai ātri pievienotu rindas. Pārliecinieties, ka rindas tiek pievienotas kā daļa no tabulas (izmantojot vertikālo ritjoslu, režģa augšpusē vajadzētu būt redzamām kolonnu galvenēm) 

[![Automātiskais aizpildījums](./media/screenshot22.png)](./media/screenshot22.png) 

4.7. Atgriezties programmatūrā Dynamics 365 for Finance and Operations un atsvaidziniet lapu. Programmatūrā Dynamics 365 for Finance and Operations ir redzamas publicētās vērtības. 

[![Atsvaidzināšana](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>5. uzdevums. Budžeta plāna dokumenta izkārtojumu un veidņu izveide
Izkārtojums definē, kā izskatīsies budžeta plāna dokumenta rindu režģis, kad lietotājs atver budžeta plāna dokumentu. Budžeta plāna dokumentu izkārtojumu var arī pārslēgt, lai datus aplūkotu no dažādiem aspektiem. Tā kā budžeta plāna dokumentam lietojamās kolonnas ir definētas, Jūlijai ir jāizveido budžeta plāna dokumenta izkārtojums, kas izskatīsies līdzīgi Excel tabulai, ko viņa izmanto, lai izveidotu budžeta datus (skatiet šī uzdevuma sadaļu Scenārija pārskats) 

5.1. Pārejiet uz Budžeta veidošana&gt;Iestatīšana &gt; Budžeta plānošana &gt; Budžeta plānošanas konfigurācija un atveriet lapu Izkārtojumi. Izveidojiet jaunu izkārtojumu ikmēneša budžeta ierakstam.

-   Atlasiet dimensiju kopu MA + BU, lai izkārtojumā iekļautu vienumu Galvenie konti un Biznesa vienības.
-   Norādiet visas budžeta plāna kolonnas, ko izveidojāt iepriekšējā darbībā sadaļā Elementi. Iestatiet, lai visas summas, izņemot iepriekšējā gada faktiskās izmaksas, būtu rediģējamas.
-   Noklikšķiniet uz pogas Apraksti, lai atlasītu, kuras finanšu dimensijas ir jāparāda rindā Apraksti.

[![Apraksti](./media/screenshot24.png)](./media/screenshot24.png) 

Pamatojoties uz budžeta plāna izkārtojuma definīciju, varam izveidot Excel veidni, kas jāizmanto kā alternatīva metode budžeta datu rediģēšanai. Excel veidnei ir jāatbilst budžeta plāna izkārtojuma definīcijai. Pēc Excel veidnes ģenerēšanas, budžeta plāna izkārtojumu nevar rediģēt, tāpēc šis uzdevums jāveic pēc tam, kad visi izkārtojuma komponenti ir definēti. 

5.2. Izkārtojumam, ko izveidojāt 5.1. darbībā, noklikšķiniet uz pogas Veidne &gt; Ģenerēt. Apstipriniet brīdinājuma ziņojumu. Lai skatītu šo veidni, noklikšķiniet uz Veidne &gt; Skats. 

*Piezīme. Noteikti atlasiet “Saglabāt kā” un atlasiet vietu, kur veidne ir jāglabā, lai to varētu rediģēt. Ja lietotājs dialoglodziņā atlasa vienumu “Atvērt” bez saglabāšanas, tad aizverot failu, failā veiktās izmaiņas netiek saglabātas.* 
[![Veidnes skats](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Neobligāta darbība&gt; Modificējiet Excel veidni, lai tā izskatās lietotājam draudzīgāka — pievienojiet kopsummu formulas, galvenes laukus, formatējumu utt. Saglabājiet izmaiņas un augšupielādējiet failu budžeta plāna izkārtojumā, noklikšķinot uz Izkārtojums &gt; Augšupielādēt [![Augšupielādēt](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>6. uzdevums. Budžeta plānošanas procesa izveide
Jūlijai ir jāizveido un jāaktivizē jauns budžeta plānošanas process, apvienojot iepriekš minētos visus iestatījumus, lai sāktu ievadīt budžeta plānus. Budžeta plānošanas procesā definē, kādas budžeta organizācijas, darbplūsma, izkārtojumi un veidnes tiks lietotas budžeta plānu izveidē. 

6.1. Pārejiet uz Budžeta veidošana &gt; Iestatīšana &gt; Budžeta plānošana &gt; Budžeta plānošanas process un izveidojiet jaunu ierakstu.

-   Budžeta plānošanas process — DEMF budžeta veidošana 2016. finanšu gadam
-   Budžeta cikls — 2016. finanšu gads
-   Virsgrāmata — DEMF
-   Noklusējuma konta struktūra — ražošanas peļņa un zaudējumi
-   Organizācijas hierarhija — atlasiet uzdevuma sākumā izveidoto hierarhiju
-   Budžeta plānošanas darbplūsma — piešķiriet Automātiska — Darbplūsmas apstiprināšana finanšu nodaļai
-   Budžeta plānošanas stadijas nosacījumos un veidnēs katrai darbplūsmas budžeta plānošanas stadijai jāatlasa, vai ir atļauta rindu pievienošana un modificēšana, un kādi izkārtojumi ir jāizmanto pēc noklusējuma.

*Piezīme. Varat izveidot papildu dokumentu izkārtojumus un piešķirt tos, lai tie būtu pieejami budžeta plānošanas darbplūsmas posmā, noklikšķinot uz pogas Alternatīvie izkārtojumi.* 

[![Alternatīvie izkārtojumi](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Atlasiet Darbības &gt; Aktivizēt, lai aktivizētu šo budžeta plānošanas darbplūsmu 

[![Aktivizēt](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>2. uzdevums. Procesa simulācija
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>7. uzdevums. Ģenerējiet budžeta plāna sākotnējos datus no Virsgrāmatas.
7.1. Pārejiet uz Budžeta veidošana &gt; Periodisks &gt; Budžeta plāna ģenerēšana no virsgrāmatas. Aizpildiet periodiskā procesa parametrus un noklikšķiniet uz pogas Ģenerēt. 

[![Ģenerēt](./media/screenshot29.png)](./media/screenshot29.png) 

7.2. Pārejiet uz Budžeta veidošana &gt; Budžeta plāni, lai atrastu procesa ģenerēšanas laikā izveidoto budžeta plānu. 

[![Budžeta plāns](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Atveriet dokumenta informāciju, noklikšķinot uz hipersaites Dokumenta numurs. Budžeta plāns tiek parādīts atbilstoši izkārtojumam, kāds tika definēts šī uzdevuma izpildes laikā 

[![Budžeta plāna displejs](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>8. uzdevums. Pašreizējā gada budžeta izveide, pamatojoties uz iepriekšējā gada faktiskajām summām
Budžeta plānā var izmantot sadalījuma metodes, lai viegli kopētu budžeta plānu informāciju no viena scenārija citā/izplatīt tos dažādos periodos/sadalītu pa dimensijām. Mēs izmantosim sadalījumus, lai izveidotu pašreizējā gada budžetu no iepriekšējā gada faktiskajam summām. 

8.1. Atlasiet visas rindas budžeta plāna dokumentu režģī un noklikšķiniet uz pogas Piešķirt budžetu 

[![Visas rindas](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Atlasiet sadalījuma metodi, perioda atslēgu, avota un mērķa scenārijus un noklikšķiniet uz Piešķirt 

[![Piešķirt](./media/screenshot33.png)](./media/screenshot33.png)

Iepriekšējā gada faktiskās summas tiks kopētas uz pašreizējā gada budžetu un sadalītas pa periodiem, izmantojot pārdošanas līknes perioda atslēgu. 

[![Pārdošanas līkne](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>9. uzdevums. Budžeta plāna dokumenta koriģēšana, izmantojot programmu Excel, un dokumenta pabeigšana
9.1. Noklikšķiniet uz pogas Darblapa, lai dokumenta saturu atvērtu programmā Excel

[![Excel](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Kad tiek atvērta Excel darbgrāmata, pielāgojiet budžeta plāna dokumenta skaitļus un noklikšķiniet uz pogas Publicēt.

[![Publicēšana](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Atkal atveriet budžeta plāna dokumentu programmatūrā Dynamics 365 for Finance and Operations. Noklikšķiniet uz Darbplūsma &gt; Iesniegt dokumentu automātiskai apstiprināšanai

[![Automātiska apstiprināšana](./media/screenshot37.png)](./media/screenshot37.png) 

Kad darbplūsma ir pabeigta, budžeta plāna dokumenta stadija mainās uz Apstiprināts. [![Apstiprināts](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Pielikums
========

### <a name="auto-approve-workflow-configuration"></a>Darbplūsmas konfigurācijas automātiska apstiprināšana

A. Budžeta veidošana &gt; Iestatīšana &gt; Budžeta plānošana &gt; Budžeta veidošanas darbplūsmas. Izveidojiet jaunu darbplūsmu, izmantojot veidni Budžeta veidošanas darbplūsmas:

[![Izveidot jaunu darbplūsmu](./media/screenshot39.png)](./media/screenshot39.png)

Šī darbplūsma ir tikai viens uzdevums — Budžeta plāna stadijas pāreja 

[![Stadijas pārejas budžeta plāns](./media/screenshot40.png)](./media/screenshot40.png) 

Saglabājiet un aktivizējiet darbplūsmu. 

B. Pārejiet uz Budžeta veidošana &gt; Iestatīšana &gt; Budžeta plānošana &gt; Budžeta plānošanas konfigurācija. Cilnē Stadijas izveidojiet divas stadijas — Sākotnējais un Iesniegts 

[![Sākotnējais un iesniegtais](./media/screenshot41.png)](./media/screenshot41.png)

C. Pārejiet uz Budžeta veidošana &gt; Iestatīšana &gt; Budžeta plānošana &gt; Budžeta plānošanas konfigurācija. Cilnē Darbplūsmas stadijas A darbības laikā izveidoto automātiskas apstiprināšanas darbplūsmu saistiet ar stadijām Sākotnējais un Iesniegts 

[![Budžeta veidošana un budžeta plānošana](./media/screenshot42.png)](./media/screenshot42.png)  



