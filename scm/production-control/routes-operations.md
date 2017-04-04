---
title: "Maršrutiem un operācijām"
description: "Šajā tēmā ir sniegta informācija par maršrutiem un operācijām. Maršrutu nosaka process ražo preci vai preces variants. Tā apraksta katru soli (operācija), ražošanas procesu un kārtību, kādā jāveic šādas darbības. Katram solim maršrutu nosaka nepieciešamo operāciju resursus, nepieciešams uzstādīšanas laiks un izpildes laiks, un kā aprēķināt izmaksas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Maršrutiem un operācijām

Šajā tēmā ir sniegta informācija par maršrutiem un operācijām. Maršrutu nosaka process ražo preci vai preces variants. Tā apraksta katru soli (operācija), ražošanas procesu un kārtību, kādā jāveic šādas darbības. Katram solim maršrutu nosaka nepieciešamo operāciju resursus, nepieciešams uzstādīšanas laiks un izpildes laiks, un kā aprēķināt izmaksas.

<a name="overview"></a>Pārskats
--------

Maršruta apraksta darbību secību, kas vajadzīga, lai ražotu preces vai produkta variants. Katrai operācijai maršrutā nosaka arī operācijās resursi, kas nepieciešami, laiku, kas nepieciešams, lai iestatītu un izpildītu darbību un kā aprēķināt izmaksas. Var lietot, lai izveidotu vairākus produktus vienā maršrutā vai varat definēt unikālu maršrutu katram ražojumam vai ražojumu variants. Varat pat ir vairāki ceļi uz to pašu produktu. Šajā gadījumā maršruts, ko izmanto, ir atšķirīgs, atkarībā no tādiem faktoriem kā daudzums, kas ir jāražo. Microsoft Dynamics 365 operācijām maršrutā definīciju veido četri atsevišķi elementi, kas kopā, apraksta ražošanas procesā:

-   **Maršruta** -maršrutu nosaka ražošanas procesa struktūru. Citiem vārdiem sakot, tas nosaka operāciju secību.
-   **Operācija** – darbība identificē nosaukto solis maršrutu, piemēram, **montāžas**. Un tai pašā operācijā var rasties vairāki ceļi un var būt dažādas operācijas numuriem.
-   **FormāOperation relation** -formāOperation relation definē operāciju, piem., uzstādīšanas laiku un izpildes laiku, izmaksu kategorijas, patēriņa parametri un resursu prasības ekspluatācijas īpašības. Operācijas saistībai nodrošina operatīvās darbības mainās atkarībā no izmantoto operāciju maršrutā vai produktiem, kuri tiek ražoti rekvizītus.
-   **Maršruta versiju** – maršruta versiju definē maršruts, ko izmanto, lai ražotu preci vai preces variants. Maršruta versijas ļauj maršrutos atkārtoti lietots visā izstrādājumu vai mainījusies laika gaitā. Viņi arī iespējot dažādus maršrutus uz izmantot, lai ražotu vienu un to pašu produktu. Šajā gadījumā maršruts, ko izmanto, ir atkarīga no tādiem faktoriem kā atrašanās vieta vai daudzums, kas ir jāražo.

## <a name="routes"></a>Maršruti
Maršruta apraksta darbību secību, kas tiek izmantots, lai ražotu preces vai produkta variants. Katra operācija tiek piešķirts operācijas numuru un pārņēmēju darbībai. Operāciju secība veido maršrutu tīklu, kas var pārstāvēt virzīto diagramma, kas ir vienu vai vairākus sākuma punktus un vienu beigu punktu. Dynamics 365 operācijām, ir atšķirīgas atkarībā no konstrukcijas tipa maršrutos. Ir divu veidu maršrutiem, vienkāršu maršrutu un maršruta tīklu. Ražošanas kontroles parametri, var norādīt, vai drīkst izmantot tikai vienkāršu maršrutu vai vai sarežģītāka maršruta tīklu var izmantot.

### <a name="simple-routes"></a>Vienkārši maršruti

Vienkāršs maršruts ir secīgs, un tur ir tikai viena maršruta sākumpunkts.  

[![Vienkāršs maršruts](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Ja jūs varētu tikai vienkāršu maršrutiem, ražošanas kontroles parametri, Dynamics 365 operācijām automātiski ģenerē operāciju numurus (10, 20, 30 un tā tālāk), definējot maršrutu.

### <a name="route-networks"></a>Maršruta tīklu

Ja iespējojat sarežģītākas maršruta tīklu ražošanas kontroles parametrus, var definēt maršrutus, kas ir vairākus sākuma punktus un operācijas, kas var darboties paralēli.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Piezīmes.**

-   Katrai operācijai var būt tikai viens pārņēmēju darbībai un visa maršruta jābeidzas vienā piegājienā.
-   Nav garantijas, ka faktiski vairākas operācijas, kas ir pēctecis pašu darbību (piemēram, operācijas, 30 un 40, iepriekšējā attēlā) darbosies paralēli. Pieejamību un resursu ražīguma var pakļaut ierobežojumiem, par to, kādā veidā ir plānotas operācijas.
-   0 (nulle) nevar izmantot kā operācijas numuru. Šis numurs ir rezervēts, un to lieto, lai norādītu, ka pēdējā operācija maršrutā ir pēctecis operācija.

### <a name="parallel-operations"></a>Paralēlās darbības

Dažreiz, kombinācija vairāku operāciju resursi, kuriem ir atšķirīgas īpašības ir nepieciešama, lai veiktu operāciju. Piemēram, ka montāžas operācija var pieprasīt iekārtu, rīku un viens darbinieks ik pēc divām mašīnām, lai pārraudzītu darbību. Šajā piemērā var modelēt, izmantojot paralēlu operāciju, kur vienā operācijā ir nozīmēta kā primārās operācijas un citi ir sekundāri.  

[![Maršrutam, kurš ir primārās un sekundārās operācijas](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Parasti primārās operācijas pārstāv sašaurinājums resursu un nosaka izpildes laiku sekundārajām operācijām. Tomēr, plānošanā, kas saistīta ar ierobežota noslodze, resursi, kas tiek plānoti primārajai operācijai, gan sekundārajām operācijām jābūt pieejamiem, un tajā pašā laikā ir brīvas jaudas.  

Primārajai operācijai, gan sekundārajām operācijām jābūt vienu un to pašu operācijas numuru (30 iepriekšējā attēlā).  

Iepriekšējā piemērā primārās operācijas (30) resursu prasība ir mašīnu, tā kā resursu prasības sekundārajām operācijām (30' un 30 ') ir rīks, un darba ņēmējiem. Piecdesmit procentu slodzi palīdz garantēt ieplānotā darba ņēmējs var pārraudzīt divām mašīnām vienlaicīgi.

### <a name="approval-of-routes"></a>Maršrutu apstiprināšana

Maršrutu vispirms jāapstiprina, tikai tad to var izmantot plānošanas vai ražošanas procesā. Apstiprinājumu norāda, ka ir pabeigta maršruta dizains. Tas pats atbrīvots produkts vai nodotā produkta variants var būt vairākiem apstiprinātiem maršrutiem. Parasti, maršrutu apstiprināšana notiek, kad pirmā attiecīgā maršruta versija ir apstiprināta. Tomēr dažiem uzņēmējdarbības scenārijus, apstiprinājuma maršrutu un maršruta versiju ir atsevišķas aktivitātes, kas varētu ietvert dažādu procesu īpašniekiem.  

Katrā maršrutā var apstiprināto vai neapstiprināto atsevišķi. Tomēr, ņemiet vērā, ka, ja maršruts ir neapstiprināta, visas saistītās maršruta versijas ir arī Neapstiprināti. Ražošanas kontroles parametru, var norādīt, vai var būt neapstiprinātiem maršrutiem, un vai apstiprinātiem maršrutiem var mainīt.  

Ja jums jāveic uzskaite log, kurš apstiprina katram maršrutam, maršruta apstiprināšanas var pieprasīt elektronisko parakstu. Lietotājiem būs pēc tam, lai apstiprinātu savu identitāti, izmantojot [elektronisko parakstu](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Operācijas
Darbība ir solis ražošanas procesā. Dynamics 365 operācijām, katrai operācijai ir ID un vienkāršu aprakstu. Nākamajās tabulās norādīts raksturīgākie piemēri machine shop operācijas.

| Operācija  | apraksts        |
|------------|--------------------|
| PipeCut    | Cauruļu griešanas       |
| TIGweld    | TIG metināšanas        |
| JigAssy    | Džiga montāža       |
| Pārbaude | Kvalitātes pārbaude |

Operācija, piem., uzstādīšanas laika un izpildes laika, resursu prasības, izmaksu informācijas un patēriņa aprēķins, ekspluatācijas īpašības norādītas par operācijas saistībai. (Lai iegūtu papildinformāciju par operāciju saites, skatiet nākamo sadaļu).

## <a name="operation-relations"></a>Operāciju saites
Šādas darbības rekvizīti operācijas tiek uzturētas par operācijas saitēm:

-   Izmaksu kategorijas
-   Patēriņa parametri
-   Izpildes laikus
-   Pārstrādes daudzumu
-   Resursu vajadzības
-   Piezīmes un norādījumus

Var definēt vairākus darbībām saistībā ar vienu un to pašu darbību. Tomēr katras operācijas saistībai ir raksturīgs vienas operācijas un saglabā īpašības, kas raksturīgas maršrutu, atbrīvots produkts vai atbrīvo produktus, kas saistīti ar krājumu grupu kopa. Tāpēc vienā operācijā var izmantot vairākus maršrutus, kas ir dažādu ekspluatācijas īpašības. Turklāt var vieglāk saglabāt vispārējos datus, ja jūs izmantojat standarta operāciju pašu ekspluatācijas īpašībām, neatkarīgi no maršruta, kas tiek izmantota un produkts, ko ražo. Operācijas saistībai apjoms ir noteikts caur **priekšmeta kods**, **krājumu saistība**, **maršruta kods** un **maršruta attiecību** rekvizītus, kā parādīts sekojošajā tabulā.

| Krājuma kods | Krājumu saistība         | Maršruta kods | Maršruta atsauce   | Operācijas saistībai joma                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabula     | &lt;Preces ID&gt;;       | Maršruts      | &lt;Maršruta ID&gt; | Operāciju, kad tas tiek izmantots maršrutu ekspluatācijas īpašības kur **maršruta numurs**=&lt;maršruta ID&gt; nodotā produkta ražošanai kur **krājums**=&lt;vienuma ID&gt;.                                                                                                                        |
| Tabula     | &lt;Preces ID&gt;;       | Visus        |                  | Noklusējuma darbības operāciju, kad tas tiek izmantots, lai ražotu atbrīvots produkts rekvizītus, kur **krājums**=&lt;vienums ar ID&gt;. Citiem vārdiem sakot, šīs darbības īpašības piemērot, ja nav specifisks maršruta operāciju saistības atbrīvots produkts.                                     |
| Grupa     | &lt;Krājumu grupas ID&gt; | Maršruts      | &lt;Maršruta ID&gt; | Operāciju, kad tas tiek izmantots maršrutu ekspluatācijas īpašības kur **maršruta numurs**=&lt;maršruta ID&gt; atbrīvo produktus, kas ir saistīta ar vienuma grupu &lt;krājumu grupas ID&gt;, ja vien tur ir specifisks maršruta operācijas saistībai atbrīvots produkts.                         |
| Grupa     | &lt;Krājumu grupas ID&gt; | Visus        |                  | Noklusējuma darbību, kad to izmanto, lai ražotu atbrīvo produktus, kas ir saistīta ar vienuma grupu darbības īpašības &lt;krājumu grupas ID&gt;, ja vien pastāv konkrētāki operāciju attiecības.                                                                                                  |
| Visus       |                       | Maršruts      | &lt;Maršruta ID&gt; | Noklusējuma darbības rekvizīti, lietojot maršruta operācijas kur **maršruta numurs**=&lt;maršruta ID&gt;. Citiem vārdiem sakot, šīs darbības īpašības piemērot, ja nav nekādas operācijas saistībai, attiecībā uz šo maršrutu, kas ir raksturīgs kādai atbrīvots produkts vai tā ir saistīta ar krājumu grupu. |
| Visus       |                       | Visus        |                  | Noklusējuma darbības īpašības operāciju. Šīs darbības īpašības attiecas konkrētāki formāOperation relation neeksistē.                                                                                                                                                                |

Varat arī norādīt operācijas saistībai ir īpaša vieta. Šādā veidā operāciju ekspluatācijas īpašības var atšķirties atkarībā no atrašanās vietas (t.i., lapa), kurā darbība tiek veikta. Konfigurētas preces, var norādīt arī dažādu operatīvo rekvizītus katra produkta konfigurēšanu.  

Operāciju saites sniegt jums daudz elastību, definējot savu maršrutu. Turklāt iespēju definēt noklusējuma rekvizīti palīdz samazināt vispārējos datus, kas jums ir jāsaglabā. Tomēr šī elastība nozīmē arī, ka jums ir jāapzinās to modificēšanas darbība saistībā ar kontekstu.  

**Piezīme:** jo darbības rekvizīti tiek saglabāti operāciju saites par vienu darbību vienam maršrutam, visos gadījumos vienu un to pašu darbību (piemēram, montāža) ir pašā uzstādīšanas laiku, izpildes laika, resursu vajadzībām un tā tālāk. Tādēļ, ja divi gadījumi darbība notiek tajā pašā maršrutā, bet ir dažādi izpildes laiki, ir jāizveido divas atšķirīgas darbības, piemēram, Assembly1 un Assembly2.

### <a name="modifying-product-specific-routes"></a>Modificēšanas produktiem raksturīgus maršruti

Atverot **maršruta** lapa no **atbrīvo produkta detaļas** lapu, maršruta versijas, kas ir saistītas ar atlasīto atbrīvots produkts tiek parādīti. Šajā kontekstā katrai operācijai Dynamics 365 operācijām rāda ekspluatācijas īpašības no formāOperation relation vislabāk atbilst maršruta versijas. Jūs ievērosiet, ka operāciju saraksta, kas ietver **priekšmeta kods** un **maršruta kods** rekvizītus no operācijas saistībai. Tādēļ var noteikt, kuras formāOperation relation tiek parādīts.  

Par **maršruta** lapu, operāciju, piem., izpildes laiku vai cenu kategoriju darbības rekvizītus var mainīt. Jūsu veiktās izmaiņas tiek glabātas formāOperation relation, kas ir specifisks maršruta un atbrīvots produkts, kas ir minēta pašreizējo maršruta versiju. Ja operācijas saistībai, kas tiek parādīts nav konkrētu maršrutu un atbrīvots produkts pirms jūsu veiktās izmaiņas tiek saglabātas, sistēma izveido kopiju formāOperation relation. Šo kopiju *ir* konkrētu maršrutu un atbrīvots produkts. Tādēļ izmaiņas neietekmē citus ceļus vai atbrīvo produktus. Pārbaudīt, kuri formāOperation relation modificē par **maršruta** lapas, apskatīt **priekšmeta kods** un **maršruta kods** laukus.  

Var arī manuāli izveidot darbības, kas ir specifisks maršruta un atbrīvots produkts, izmantojot **kopēšanas un labojiet saistība** funkciju.  

**Piezīme:** ja pievienojat jaunu operāciju maršrutā **maršruta** lapu, formāOperation relation ir izveidotas tikai pašreizējā atbrīvots produkts. Tādēļ, ja trase tiek izmantots arī citu atbrīvo produktus, nav piemērojami formāOperation relation pastāvēs pacelto produktiem un maršrutu vairs nevar izmantot tās atbrīvo produktus.

### <a name="maintaining-operation-relations-per-route"></a>Saglabāt vienā maršruta operāciju saites

Atverot **maršruta detaļas** lapa no **maršruti** lapa saraksts, tiek parādīts saraksts operāciju saites, kas attiecas uz atlasīto maršrutu. Tādējādi var viegli pārbaudīt, kuras ekspluatācijas īpašības tiek izmantotas konkrētiem produktiem. Jūs varat mainīt noklusējuma rekvizītu vērtībām, gan īpašs nekustamā īpašuma vērtības.  

Pievienojot jaunu formāOperation relation **maršruta detaļas** lapu, **maršruta kods** laukā tiek automātiski iestatīts uz **maršruta**, un **maršruta attiecību** lauks ir iestatīts uz pašreizējais maršruts maršruta numurs.

### <a name="maintaining-operation-relations-per-operation"></a>Uzturēšanas operācijas attiecības vienā operācijā

No **operācijas** lapu, jūs varat atvērt **Operation relations** lapā. Šajā lapā jūs varat mainīt visu operāciju saites konkrētai operācijai. Operāciju saites, kas ir noklusētās vērtības, pat var modificēt.  

Ja jūsu uzņēmums izmanto standarta operāciju un ekspluatācijas parametri ir vienādi visās produktiem un procesiem, **Operation relations** lapas nodrošina ērtu veidu, kā saglabāt noklusējuma darbības īpašības šīm operācijām.

### <a name="applying-operation-relations"></a>Piemērojot operāciju saites

Dažos gadījumos Dynamics 365 operācijām ir jāatrod operācijas ekspluatācijas īpašības. Piemēram, izveidojot pirkšanas pasūtījumu, ekspluatācijas īpašībām katrai operācijai ir jākopē no operation relations ražošanas maršrutā. Šajās situācijās Dynamics 365 operācijām meklē attiecīgo operāciju attiecības no visraksturīgāko kombināciju vismaz noteiktu kombināciju.  

Ja Dynamics 365 darbības meklē visatbilstošākās formāOperation relation pacelto produktam formāOperation relation, kas atbilst krājuma ID atbrīvots produkts ir priekšroka dodama formāOperation relation sacensībām krājumu grupas ID Savukārt, formāOperation relation, kas atbilst krājuma grupas ID ir vēlamais pār noklusējuma formāOperation relation. Meklēšana tiek veikta šādā secībā:

1.  **Priekšmeta kods**=**tabulas** un **krājumu saistība**=&lt;vienuma ID&gt;
2.  **Priekšmeta kods**=**grupas** un **krājumu saistība**=&lt;krājumu grupas ID&gt;
3.  **Priekšmeta kods**=**visas**
4.  **Maršruta kods**=**maršruta** un **maršruta attiecību**=&lt;maršruta ID&gt;
5.  **Maršruta kods**=**visas**
6.  **Konfigurācijas**=&lt;konfigurācijas ID&gt;
7.  **Configuration**=
8.  **Vieta**=&lt;atrašanās vietas ID&gt;
9.  **Site**=

Tāpēc darbība būtu jāizmanto tikai vienu reizi katram maršrutam. Ja darbība notiek vairākas reizes vienu un to pašu maršrutu, visus gadījumus, šīs darbības būs pašas operācijas saistībai, un jūs nevarēsiet būt citādi rekvizīti (piemēram, izpildes laiku), katram gadījumam.

## <a name="route-versions"></a>Maršruta versijas
Maršruta versijas izmanto, lai pielāgotos izmaiņām produktu ražošanā vai nodrošinātu lielāku kontroli pār ražošanas procesu. Tie nosaka, kura trase būtu jāizmanto, ja konkrētu atbrīvots produkts vai variant atbrīvots produkts tiek ražots. Šādus ierobežojumus var izmantot, lai definētu, kuras trases atbrīvots produkts tiek izmantots:

-   Izstrādājuma izmēri (izmēru, krāsu, stilu, vai konfigurācija)
-   Ražošanas daudzums
-   Ražošanas vietas
-   Ražošanas datums

Kad esat ražo attiecīgo ražojumu noteiktā vietnē, ar noteiktu daudzumu, vai konkrētā periodā, var norādīt noteiktu maršruta versiju, kā noklusētā maršruta versijas. Tomēr, ņemiet vērā, ka tikai viens aktīvais maršruts ir atļauta konkrētā atbrīvots produkts un konkrētā noteikt ierobežojumus.  

Ražošanas kontroles parametri, var pieprasīt maršruta versijas derīguma termiņu vienmēr jānorāda.

### <a name="approval-of-route-versions"></a>Maršruta versijas apstiprināšana

Pirms maršruta versiju var izmantot plānošanā vai ražošanas process, tas ir jāapstiprina. Kad jūs apstiprināt maršruta versiju, jūs varat apstiprināt saistīto maršrutu. Tomēr, ņemiet vērā, ka maršruta versiju var apstiprināt tikai tad, ja saistīto maršruts arī apstiprināts.

### <a name="activating-the-default-route-version"></a>Aktivizēt maršruta versijas noklusējuma

Aktivizējot maršruta versiju, jūs norādāt to kā noklusētā maršruta versijas, kuru vispārējā plānošana izmanto, vai arī tas tiks izmantots, lai izveidotu – ražošanas pasūtījumus. Jums var būt tikai viena aktīva maršruta versija konkrētā kopumu ierobežojumus (piemēram, laikā, vietā vai daudzumu). Ja versija, ka jūs mēģināt aktivizēt konflikti ar versiju, kas jau darbojas, tiek parādīts kļūdas ziņojums. Lai novērstu neskaidrs aktivizēšanas, ir pēc tam deaktivizēt konfliktējošu versiju vai modificēt maršruta versiju ierobežojumus (parasti periods).

### <a name="electronic-signatures"></a>Elektroniskos parakstus

Ja jums jāsaglabā log, ka ieraksti, kas apstiprina un aktivizē katra maršruta versiju, elektronisko parakstu var pieprasīt šos uzdevumus. Pēc tam lietotājiem apstiprināt un aktivizēt maršruta versijas būs jāapstiprina sava identitāte, izmantojot [elektronisko parakstu](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Produkta izmaiņu, kas lieto lietu vadības

Produkta mainīt lietu apstiprināšanai un aktivizēšana jauniem vai mainītiem maršrutu un maršruta versijas sniedz jums ērts veids, kā skatīt apskatu par maršruta versiju ierobežojumus. Var apstiprināt un aktivizēt visus maršrutus, kas ir saistītas ar noteiktas izmaiņas vienā operācijā un dokumentē rezultātus produkta izmaiņu gadījumā.

## <a name="maintaining-routes"></a>Uzturēt ceļus
Atkarībā no uzņēmuma vajadzībām, jūs varētu samazināt pūles, kas ir nepieciešams, lai saglabātu procesa definīcijas.

### <a name="making-routes-independent-of-resources"></a>Veicot maršrutu neatkarīgi no resursu

Daudzās sistēmās, jānorāda maršrutā operācijas resursu vai resursu grupu, kas būtu veikt operāciju. Tomēr programmā Dynamics 365 operācijām, var definēt vairākas prasības, kas būtu piemērojama darbībai jāatbilst operācijas resursa. Tādēļ jānosaka līdz operācija tiek ieplānota faktiski nav īpašas darbības resursu vai resursu grupu, kas jāizmanto. Šī funkcionalitāte ir īpaši noderīga, ja jums ir daudz strādnieku vai mašīnām, kas var veikt un tai pašā operācijā.  

Piemēram, norādīt operācijai nepieciešams operācijas resursu **mašīna** tipa, kuram **zīmogošana** 20 tonnas iespējas. Plānošanas dzinējs tam atrisinās šīs prasības uz noteiktām operācijām resurss vai resursu grupa, operācija tiek plānota. Tā var norādīt tieši šīs prasības, nevis saistošas darbības konkrētu mašīnu, jums ir daudz elastīgāka. Turklāt, uzturēšana ir vieglāk, kad resursi tiek pārvietoti vai tiek pievienoti jauni resursi.  

Plašāku informāciju par dažāda veida resursiem un to izmantošanu skatiet operācijas resursa prasības un [resursu iespējas](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Koplietošanas ceļiem vairākās vietnēs

Ja jūs ražot to pašu produktu vairāk nekā vienā ražošanas vietā un soļi produkta ražošanai ir pats vispār vietas, bieži vien var noformēt kopīgu maršrutu, kas tiek lietots visās ražošanas vietnēs. Izveidot kopīgu ceļu, nav norādīt vietni pats maršruts. Tomēr vēl jāizveido maršruta versiju, kas saista kopīgu ceļu ar produktu katrā vietā.  

Jūs arī jāpārliecinās, ka resursu prasības katrai operācijai maršrutā neprasa īpašas darbības resursiem vai resursu grupām, bet tā vietā ir izteikti nepieciešamo resursu raksturojums. Pēc tam plānošanas dzinējs būs iespēja piešķirt operācijām piemērotu resursu no vietas, kurā ražošana tiek plānota uz. Piemēram, ja ir nelielas atšķirības izpildes laiku vai ir konkrētās vietas noteiktas operācijas uzstādīšanas laiku, šo informāciju var norādīt pievienojot papildu formāOperation relation šai vietnei.  

Iespēju pilnībā izmantot ieguvumus no koplietošanas ceļiem, jums vajadzētu izmantot resursu patēriņu uz atbilstošo materiālu komplekta (MK). Iestatot karogu par resursu patēriņu MK rindā, noliktavas un atrašanās vietu, kas būtu patērē izejmateriālus no ir secināt no operācija tiek plānota uz operācijas resursa. Tādēļ jānosaka līdz brīdim, kad ražošana tiek plānota faktiski nav noliktavas un atrašanās vietu. Šādā veidā, jūs varat veikt gan IMS un maršrutu neatkarīgi no fiziskās atrašanās vietas, kur produkts tiek ražots.

### <a name="standard-operation-relations"></a>Standarta operāciju saites

Ja jūsu uzņēmums izmanto standartizētas operācijas visā ražošanas un tur ir maz vai nav varianta sagatavošanas laiks, izpildes laika patēriņu aprēķina pašizmaksas aprēķins, un tā tālāk, varētu gūt labumu no izveides noklusējuma operāciju saites uz visām darbībām. Šajā gadījumā neradītu operāciju saites, kas attiecas uz jebkuru maršrutu vai atbrīvots produkts.  

Ja arī izteikt resursu prasības attiecībā uz prasmēm un spējām, un padarīt jūsu maršrutu vietu neatkarīgās, var uzturēt pastāvīgi uzturēt biznesa procesu līdz minimumam.  

Izmantojot šo pieeju, **Operation relations** lapa kļūst jūsu primārā mērķa saglabāšanai izpildes laiki un citus rekvizītus.

### <a name="resource-specific-process-times"></a>Resursu specifisko procesu reizes

Ja nenorādīsit operācijas resursa vai resursu grupas kā daļu no resursu prasības darbībai, piemērojami resursus varētu darboties dažādos ātrumos. Tādēļ, laiku, kas nepieciešams, lai apstrādātu darbība var atšķirties. Lai atrisinātu šo problēmu, var izmantot **Formula** lauku formāOperation relation, lai norādītu par izstrādes laika aprēķināšanu. Pieejamas šādas opcijas

-   **Standarta** -(noklusējuma variants) aprēķinā izmanto tikai laukus no operācijas saistībai, un norādītā izpildes laika reizina ar pasūtījuma daudzums.
-   **Jaudas** – aprēķins ietver **jaudas** laukā no operāciju resursu. Tādēļ laika resursa atkarīgo. Vērtība, kas norādīta resursa operācijas ir noslodzi stundā. Šī vērtība tiek reizināta ar pasūtījuma daudzums un **Factor** vērtību no operācijas saistībai.
-   **Partiju** – partijas ražīgums tiek aprēķināts, izmantojot informāciju no operācijas saistībai. Skaitu partijās un tāpēc izpildes laiks var pēc tam aprēķināti, pamatojoties uz pasūtījuma daudzumu.
-   **Resursu partiju** – šis variants būtībā ir tāds pats kā **partijas** variants. Tomēr aprēķinos ir iekļauti **partijas spēju** laukā no operāciju resursu. Tādēļ laika resursa atkarīgo.


<a name="see-also"></a>Skatiet arī
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


