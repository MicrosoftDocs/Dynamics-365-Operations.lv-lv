---
title: Maršruti un operācijas
description: Šajā tēmā ir sniegta informācija par maršrutiem un operācijām.
author: sorenva
manager: tfehr
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable, ProdRouteJob, ProdRouteTrans, ProdRouteOverview, ProdRouteJobOverview, ProdRouteJobListPagePreviewPane, RouteTable, RouteVersionFeasibility, ProdRouteJobCurrent, RouteGroup, RouteProductionOrder, EngChgCaseRouteTablePart, EcoResProductProdTypeFormulaNoActiveRouteFormPart,
ms.author: sorenand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bb2f340afffc5f62c200b4daac311db435d796e
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895381"
---
# <a name="routes-and-operations"></a>Maršruti un operācijas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par maršrutiem un operācijām. Maršruts definē preces vai preces varianta ražošanas procesu. Tas raksturo katru ražošanas procesa darbību (operāciju) un šo darbību veikšanas secību. Maršruts definē arī katrai darbībai nepieciešamos operācijas resursus, nepieciešamo iestatīšanas un izpildes laiku un lietojamo izmaksu aprēķināšanas veidu.

<a name="overview"></a>Pārskats
--------

Maršruts raksturo preces vai preces varianta ražošanai nepieciešamo operāciju secību. Maršruts definē arī katrai operācijai nepieciešamos operācijas resursus, operācijas iestatīšanai un izpildei nepieciešamo laiku un lietojamo izmaksu aprēķināšanas veidu. Varat izmantot vienu maršrutu vairāku preču ražošanai vai definēt unikālu maršrutu katrai precei vai preces variantam. Varat pat izmantot vairākus maršrutus vienai precei. Šādā gadījumā izmantotais maršruts ir atkarīgs no tādiem faktoriem kā saražojamais daudzums. Maršruta definīcija programmatūrā FSupply Chain Management sastāv no četriem atsevišķiem elementiem, kas kopā raksturo ražošanas procesu:

-   **Maršruts** — maršruts definē ražošanas procesa struktūru. Citiem vārdiem sakot, tas definē operāciju secību.
-   **Operācija** — operācija norāda konkrētu maršruta darbību, piemēram, darbību **Montāža**. Vienu operāciju var izmantot vairākos maršrutos un tai var būt dažādi operācijas numuri.
-   **Operācijas saite** — operācijas saite definē operācijas darbības rekvizītus, piemēram, iestatīšanas un izpildes laiku, izmaksu kategorijas, patēriņa parametrus un resursu vajadzības. Operācijas saite nodrošina iespēju izmantot dažādus operācijas darbības rekvizītus atkarībā no maršruta, kurā tiek lietota šī operācija, vai ražotajām precēm.
-   **Maršruta versija** — maršruta versija definē maršrutu, kas tiek izmantots preces vai preces varianta ražošanai. Maršruta versijas sniedz iespēju atkārtoti lietot maršrutus dažādām precēm vai mainīt tos laika gaitā. Tās sniedz iespēju arī izmantot dažādus maršrutus vienas preces ražošanai. Šādā gadījumā izmantotais maršruts ir atkarīgs no tādiem faktoriem kā atrašanās vieta vai saražojamais daudzums.

## <a name="routes"></a>Maršruti
Maršruts raksturo preces vai preces varianta ražošanai izmantoto operāciju secību. Katrai operācijai tiek piešķirts operācijas numurs un nākamā operācija. Operāciju secība veido maršruta tīklu, ko var atainot, izmantojot virzienu diagrammu, kurā ir viens vai vairāki sākuma punkti un viens baigu punkts. Programmatūrā Supply Chain Management maršruti atšķiras pēc struktūras veida. Ir pieejami divi maršrutu veidi: vienkāršie maršruti un maršrutu tīkli. Sadaļā Ražošanas kontroles parametri varat norādīt to, vai var tikt izmantoti tikai vienkārši maršruti vai arī sarežģītāki maršrutu tīkli.

### <a name="simple-routes"></a>Vienkārši maršruti

Vienkāršs maršruts ir secīgs un tajā ir tikai viens sākuma punkts.  

[![Vienkāršs maršruts](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Ja sadaļā Ražošanas kontroles parametri iespējojat tikai vienkāršus maršrutus, kad definējat maršrutu, programmatūrā Supply Chain Management tiek automātiski ģenerēti operāciju numuri (10, 20, 30 utt.).

### <a name="route-networks"></a>Maršrutu tīkli

Ja sadaļā Ražošanas kontroles parametri iespējojat sarežģītākos maršrutu tīklus, varat definēt maršrutus, kuriem ir vairāki sākuma punkti, un operācijas, ko var izpildīt vienlaikus.  

[![Maršruta tīkls](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

> [!NOTE]
> -   Katrai operācijai var būt tikai viena nākamā operācija, un visam maršrutam ir jābeidzas ar vienu operāciju.
> -   Tādējādi nevar garantēt, ka vairākas operācijas, kam ir viena un tā pati nākamā operācija (piemēram, 30. un 40. operācija iepriekšējā attēlā), tiešām tiks veiktas paralēli. Operāciju plānošanu var ierobežot resursu pieejamība un noslodze.
> -   Kā operācijas numuru nevar norādīt skaitli 0 (nulle). Šis numurs ir rezervēts un tiek izmantots, lai norādītu, ka maršruta pēdējai operācijai nav nākamās operācijas.

### <a name="parallel-operations"></a>Vienlaicīgās operācijas

Dažreiz operācijas veikšanai ir nepieciešama tādu operācijas resursu kombinācija, kam ir dažādi raksturlielumi. Piemēram, montāžas operācijai var būt nepieciešama iekārta, darbarīks un viens darbinieks uz katrām divām iekārtām, kurš pārrauga operāciju. Šo piemēru var modelēt, izmantojot vienlaicīgas operācijas, no kurām viena ir norādīta kā galvenā operācija, bet pārējās ir sekundārās operācijas.  

[![Maršruts ar galveno un sekundārajām operācijām](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Parasti galvenā operācija ir saistīta ar deficīta resursu un nosaka sekundāro operāciju izpildes laiku. Taču, veicot ierobežotas noslodzes resursu plānošanu, resursiem, kas tiek ieplānoti gan galvenajai, gan sekundārajām operācijām, vienlaikus ir jābūt pieejamiem un ar brīvu noslodzi.  

Gan galvenajai, gan sekundārajām operācijām ir jābūt vienādiem operācijas numuriem (30 iepriekš esošajā attēlā).  

Iepriekš sniegtajā piemērā galvenās operācijas (30) resursu vajadzība ir iekārta, bet sekundāro operāciju (30' un 30'') resursu vajadzības ir darbarīks un darbinieks. Piecdesmit procentu noslodze palīdz nodrošināt to, ka ieplānotais darbinieks var vienlaikus pārraudzīt divas iekārtas.

### <a name="approval-of-routes"></a>Maršrutu apstiprināšana

Lai maršrutu varētu izmantot plānošanas vai ražošanas procesā, maršruts vispirms ir jāapstiprina. Apstiprinājums norāda, ka maršruta izstrāde ir pabeigta. Vienai izlaistajai precei vai preces variantam var būt vairāki apstiprināti maršruti. Parasti maršruta apstiprināšana tiek veikta, kad tiek apstiprināta pirmā saistītā maršruta versija. Taču dažos uzņēmējdarbības scenārijos maršruta un maršruta versijas apstiprināšana ir atsevišķas darbības, kam var būt dažādi procesa īpašnieki.  

Katru maršrutu var atsevišķi apstiprināt vai neapstiprināt. Taču ņemiet vērā to, ka gadījumā, ja maršruts ir neapstiprināts, arī visas saistītās maršruta versijas ir neapstiprinātas. Sadaļā Ražošanas kontroles parametri varat norādīt to, vai maršruti var būt neapstiprināti un vai var mainīt apstiprinātos maršrutus.  

Ja ir nepieciešams žurnālā reģistrēt katra maršruta apstiprinātāju, varat iestatīt elektroniskā paraksta prasību maršruta apstiprināšanai. Šādā gadījumā lietotājiem ir jāapstiprina sava identitāte, izmantojot [elektronisko parakstu](../../fin-and-ops/organization-administration/electronic-signature-overview.md).

## <a name="operations"></a>Operations
Operācija ir ražošanas procesa darbība. Katrai operācijai ir ID un vienkāršs apraksts. Tālāk esošajās tabulās ir sniegti tipiski mehāniskas darbnīcas operāciju piemēri.

| Operācija  | Apraksts        |
|------------|--------------------|
| PipeCut    | Cauruļu griešana       |
| TIGweld    | TIG metināšana        |
| JigAssy    | Automatizētā montāža       |
| Pārbaude | Kvalitātes pārbaude |

Operācijas darbības rekvizīti, piemēram, iestatīšanas un izpildes laiks, resursu vajadzības, izmaksu aprēķināšanas informācija un patēriņa aprēķināšanas metode, ir norādītas operācijas saitē. (Papildinformāciju par operāciju saitēm skatiet nākamajā sadaļā.)

## <a name="operation-relations"></a>Operāciju saites
Operācijas saitē tiek uzturēti tālāk norādītie operācijas darbības rekvizīti.

-   Izmaksu kategorijas
-   Patēriņa parametri
-   Izpildes laiki
-   Izpildes daudzumi
-   Resursu vajadzības
-   Piezīmes un norādījumi

Vienai operācijai varat definēt vairākas operāciju saites. Taču katra operācijas saite ir raksturīga vienai operācijai, un tajā ietvertie rekvizīti ir raksturīgi konkrētam maršrutam, izlaistajai precei vai izlaisto preču kopai, kas ir saistīta ar krājumu grupu. Tāpēc vairākos maršrutos var izmantot vienu operāciju ar dažādiem darbības rekvizītiem. Turklāt varat vieglāk uzturēt pamatdatus, ja izmantojat standarta operācijas ar vienādiem darbības rekvizītiem neatkarīgi no izmantotā maršruta un ražotās preces. Operācijas saites tvērums tiek definēts, izmantojot rekvizītus **Krājums kods**, **Krājuma saistība**, **Maršruta kods** un **Maršruta atsauce**, kā tas ir redzams tālāk esošajā tabulā.

| Krājuma kods | Krājumu saistība         | Maršruta kods | Maršruta atsauce   | Operācijas saites tvērums                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabula     | &lt;Preces ID&gt;;       | Maršruts      | &lt;Maršruta ID&gt; | Operācijas darbības rekvizīti gadījumā, ja operācija tiek izmantota maršrutā, kura **Maršruta numurs**=&lt;maršruta ID&gt;, lai saražotu izlaisto preci, kurai **Krājuma numurs**=&lt;krājuma ID&gt;.                                                                                                                        |
| Tabula     | &lt;Preces ID&gt;;       | Visus        |                  | Operācijas noklusējuma darbības rekvizīti gadījumā, ja operācija tiek izmantota, lai saražotu izlaisto preci, kurai **Krājuma numurs**=&lt;krājuma ID&gt;. Citiem vārdiem sakot, šie darbību rekvizīti tiek lietoti, ja izlaistajai precei nav maršrutam raksturīgas operācijas saites.                                     |
| Grupa     | &lt;Krājumu grupas ID&gt; | Maršruts      | &lt;Maršruta ID&gt; | Operācijas darbības rekvizīti gadījumā, ja operācija tiek izmantota maršrutā, kura **Maršruta numurs**=&lt;maršruta ID&gt;, lai saražotu izlaistās preces, kas ir saistītas ar krājumu grupu &lt;krājumu grupas ID&gt;, ja vien izlaistajai precei nav maršrutam raksturīgas operācijas saites.                         |
| Grupa     | &lt;Krājumu grupas ID&gt; | Visus        |                  | Operācijas noklusējuma darbības rekvizīti gadījumā, ja operācija tiek izmantota, lai saražotu izlaistās preces, kas ir saistītas ar krājumu grupu &lt;krājumu grupas ID&gt;, ja vien nav raksturīgākas operācijas saites.                                                                                                  |
| Visus       |                       | Maršruts      | &lt;Maršruta ID&gt; | Operācijas noklusējuma darbības rekvizīti gadījumā, ja operācija tiek izmantota maršrutā, kuram **Maršruta numurs**=&lt;maršruta ID&gt;. Citiem vārdiem sakot, šie darbību rekvizīti tiek lietoti, ja šim maršrutam nav operācijas saites, kas ir raksturīga izlaistajai precei vai ar to saistītajai krājumu grupai. |
| Visus       |                       | Visus        |                  | Operācijas noklusējuma darbības rekvizīti. Šie darbības rekvizīti tiek lietoti tad, ja nav raksturīgākas operācijas saites.                                                                                                                                                                |

Varat arī norādīt, ka operācijas saite ir raksturīga kādai vietai. Tādējādi operācijas darbības rekvizīti var atšķirties atkarībā no operācijas veikšanas vietas. Konfigurētajām precēm varat arī norādīt atšķirīgus darbības rekvizītus katrai preces konfigurācijai.  

Operāciju saites nodrošina lielu pielāgojamību maršrutu definēšanas laikā. Turklāt noklusējuma rekvizītu definēšanas iespēja palīdz samazināt uzturamo pamatdatu apjomu. Taču šīs pielāgojamības dēļ jums ir jāņem vērā konteksts, kurā modificējat operācijas saiti.  

> [!NOTE]
> Tā kā darbības rekvizīti katrai operācijai katrā maršrutā tiek glabāti operācijas relācijās, visiem vienas operācijas (piemēram, operācijas Montāža) gadījumiem ir vienādi iestatīšanas un izpildes laiki un resursu vajadzības. Tāpēc, ja vienā maršrutā ir nepieciešami divi operācijas gadījumi ar atšķirīgiem izpildes laikiem, ir jāizveido divas atsevišķas operācijas, piemēram, 1. montāža un 2. montāža.

### <a name="modifying-product-specific-routes"></a>Precei raksturīgo maršrutu modificēšana

Kad lapā **Nodoto preču papildinformācija** atverat lapu **Maršruts**, tiek parādītas ar atlasīto izlaisto preci saistītās maršruta versijas. Šajā konteksta programmatūrā Supply Chain Management tiek rādīti katras operācijas darbības rekvizīti no maršruta versijai visatbilstošākās operācijas relācijas. Operāciju sarakstā ir ietverti operācijas saites rekvizīti **Krājuma kods** un **Maršruta kods**. Tāpēc varat noteikt, kura operācijas saite tiek rādīta.  

Lapā **Maršruts** varat modificēt operācijas darbības rekvizītus, piemēram, izpildes laiku vai izmaksu kategorijas. Izmaiņas tiek saglabātas operācijas saitē, kas ir raksturīga maršrutam un izlaistajai precei, uz kuru ir atsauce pašreizējā maršruta versijā. Ja parādītā operācijas saite nav raksturīga maršrutam un izlaistajai precei, pirms izmaiņu saglabāšanas sistēmā tiek izveidota operācijas saites kopija. Šī kopija *ir* raksturīga maršrutam un izlaistajai precei. Tāpēc veiktās izmaiņas neietekmē citus maršrutus vai izlaistās preces. Lai pārbaudītu, kura operācijas saite tiek modificēta lapā **Maršruts**, skatiet lauku **Krājuma kods** un **Maršruta kods** vērtības.  

Varat arī manuāli izveidot maršrutam un izlaistajai precei raksturīgu operāciju, izmantojot funkciju **Kopēt un rediģēt relāciju**.  

> [!NOTE]
> Ja maršrutam pievienojat jaunu operāciju lapā **Maršruts**, operācijas relācija tiek izveidota tikai pašreizējai izlaistajai precei. Tāpēc, ja maršruts tiek izmantots arī citu izlaisto preču ražošanai, netiek izveidota šīm izlaistajām precēm paredzēta operācijas saite un maršrutu vairs nevar izmantot šo izlaisto preču ražošanai.

### <a name="maintaining-operation-relations-per-route"></a>Maršrutam raksturīgo operāciju saišu uzturēšana

Kad saraksta lapā **Maršruti** atverat lapu **Maršruta informācija**, tiek parādīts visu atlasītajam maršrutam lietojamo operāciju saišu saraksts. Tāpēc varat viegli pārbaudīt, kuri darbības rekvizīti tiek lietoti konkrētai precei. Varat modificēt gan noklusējuma rekvizītu vērtības, gan precei raksturīgās rekvizītu vērtības.  

Ja lapā **Maršruta informācija** pievienojat jaunu operācijas saiti, tiek automātiski iestatīta lauka **Maršruta kods** vērtība **Maršruts** un lauka **Maršruta atsauce** vērtība, kas atbilst pašreizējā maršruta numuram.

### <a name="maintaining-operation-relations-per-operation"></a>Operācijai raksturīgo operāciju saišu uzturēšana

Lapā **Operācijas** varat atvērt lapu **Operāciju saites**. Šajā lapā varat modificēt visas konkrētai operācijai raksturīgās operāciju saites. Varat pat modificēt operāciju saites, kurās ir ietvertas noklusējuma vērtības.  

Ja jūsu uzņēmumā tiek lietotas standarta operācijas un visām precēm un procesiem ir vienādi darbības parametri, lapā **Operāciju saites** varat ērti uzturēt šo operāciju noklusējuma darbības rekvizītus.

### <a name="applying-operation-relations"></a>Operāciju saišu lietošana

Dažos gadījumos programmatūrā Supply Chain Management ir jāatrod noteiktas operācijas darbības rekvizīti. Piemēram, izveidojot pirkšanas pasūtījumu, katras operācijas darbības rekvizīti ir jākopē no operāciju saitēm uz ražošanas maršrutiem. Šādos gadījumos programmatūrā Supply Chain Management tiek meklētas piemērotās operāciju saites, sākot ar visraksturīgāko un beidzot ar vismazāk raksturīgo kombināciju.  

Kad programmatūrā Supply Chain Management tiek meklēta izlaistai precei vispiemērotākā operācijas relācija, tai operācijas relācijai, kas atbilst izlaistās preces krājuma ID, ir augstāka prioritāte nekā operācijas relācijai, kas atbilst krājumu grupas ID. Savukārt operācijas saitei, kas atbilst krājumu grupas ID, ir augstāka prioritāte nekā noklusējuma operācijas saitei. Šī meklēšana tiek veikta tālāk norādītajā secībā.

1.  **Krājuma kods**=**Tabula** un **Krājuma saistība**=&lt;krājuma ID&gt;
2.  **Krājuma kods**=**Grupa** un **Krājuma saistība**=&lt;krājumu grupas ID&gt;
3.  **Krājuma kods**=**Visi**
4.  **Maršruta kods**=**Maršruts** un **Maršruta relācija**=&lt;maršruta ID&gt;
5.  **Maršruta kods**=**Visi**
6.  **Konfigurācija**=&lt;konfigurācijas ID&gt;
7.  **Konfigurācija**=
8.  **Vieta**=&lt;vietas ID&gt;
9.  **Vieta**=

Tāpēc operāciju drīkst izmantot tikai vienu reizi katrā maršrutā. Ja operācija tiek vairākas reizes lietota vienā maršrutā, visiem šīs operācijas gadījumiem ir viena un tā pati operācijas saite un katram gadījumam nevar izmantot atšķirīgus rekvizītus (piemēram, izpildes laikus).

## <a name="route-versions"></a>Maršruta versijas
Maršruta versijas tiek izmantotas, lai nodrošinātu preču variantu ražošanu vai lielāku kontroli pār ražošanas procesu. Tās definē to, kurš maršruts ir jāizmanto noteiktas izlaistās preces vai izlaistās preces varianta ražošanai. Lai definētu to, kurš maršruts ir jāizmanto izlaistajai precei, varat izmantot tālāk norādītos ierobežojumus.

-   Preču dimensijas (izmērs, krāsa, stils vai konfigurācija)
-   Ražošanas daudzums
-   Ražošanas vieta
-   Ražošanas datums

Ja prece tiek ražota noteiktā vietā, noteiktā daudzumā vai noteiktā laika periodā, varat norādīt noteiktu maršruta versiju kā noklusējuma maršruta versiju. Taču ņemiet vērā, ka konkrētai izlaistajai precei un konkrētai ierobežojumu kopai drīkst norādīt tikai vienu aktīvu maršrutu.  

Sadaļā Ražošanas kontroles parametri varat pieprasīt, lai vienmēr tiktu norādīts maršruta versijas derīguma laika periods.

### <a name="approval-of-route-versions"></a>Maršruta versiju apstiprināšana

Lai maršruta versiju varētu izmantot plānošanas vai ražošanas procesā, maršruta versija vispirms ir jāapstiprina. Kad apstiprināt maršruta versiju, varat apstiprināt arī saistīto maršrutu. Taču ņemiet vērā to, ka maršruta versiju var apstiprināt tikai tad, ja ir apstiprināts saistītais maršruts.

### <a name="activating-the-default-route-version"></a>Noklusējuma maršruta versijas aktivizēšana

Aktivizējot maršruta versiju, tā tiek norādīta kā noklusējuma maršruta versija, kas tiks izmantota galvenajai plānošanai vai ražošanas pasūtījumu izveidei. Noteiktai ierobežojumu (piemēram, perioda, vietas vai kvalitātes) kopai var būt tikai viena aktīva maršruta versija. Ja versija, ko mēģināt aktivizēt, rada konfliktu ar jau aktivizēto versiju, tiek parādīts kļūdas ziņojums. Šādā gadījumā ir jādeaktivizē konfliktējošā versija vai jāmodificē maršruta versijas ierobežojumi (parasti — periods), lai nepieļautu neatbilstošas versijas aktivizēšanu.

### <a name="electronic-signatures"></a>Elektroniskie paraksti

Ja ir nepieciešams žurnālā reģistrēt katras maršruta versijas apstiprinātāju un aktivizētāju, varat iestatīt elektroniskā paraksta prasību šo uzdevumu veikšanai. Šādā gadījumā lietotājiem, kuri apstiprina un aktivizē maršruta versijas, ir jāapstiprina sava identitāte, izmantojot [elektronisko parakstu](../../fin-and-ops/organization-administration/electronic-signature-overview.md).

### <a name="product-change-that-uses-case-management"></a>Preces izmaiņas, izmantojot gadījumu pārvaldību

Preces izmaiņu gadījums jaunu vai mainītu maršrutu vai maršruta versiju apstiprināšanai un aktivizēšanai nodrošina vienkāršu veidu, kā pārskatīt maršruta versiju ierobežojumus. Varat arī apstiprināt un aktivizēt visus maršrutus, kas ir saistīti ar noteiktām izmaiņām vienā operācijā un dokumentēt rezultātus preces izmaiņu gadījumā.

## <a name="maintaining-routes"></a>Maršrutu uzturēšana
Atkarībā no jūsu uzņēmējdarbības vajadzībām varat atvieglot procesa definīciju uzturēšanu.

### <a name="making-routes-independent-of-resources"></a>Maršruta neatkarības no resursiem konfigurēšana

Daudzās sistēmās maršrutā ir jānorāda operācijas resurss vai resursu grupa, kas ir jāizmanto operācijas veikšanai. Taču programmatūrā Supply Chain Management varat definēt prasību kopu, kam ir jāatbilst operācijas resursam, lai to varētu lietot operācijai. Tāpēc konkrētais operācijas resurss vai resursu grupa, kas ir jāizmanto, nav jānosaka līdz operācijas plānošanas laikam. Šī funkcionalitāte ir īpaši noderīga, ja ir pieejams daudz darbinieku vai iekārtu, kas var veikt vienu un to pašu operāciju.  

Piemēram, pieņemsim, ka norādāt, ka operācijai ir vajadzīgs veida **Iekārta** operācijas resurss, kura **štancēšanas** spēja ir 20 tonnas. Pēc tam operācijas plānošanas laikā plānošanas programma nodrošina šo vajadzību atrisināšanu, piešķirot noteiktu operācijas resursu vai resursu grupu. Tas, ka varat vienkārši norādīt šīs vajadzības, nesaistot operāciju ar noteiktu iekārtu, sniedz daudz lielāku pielāgojamību. Turklāt tādējādi tiek atvieglota uzturēšana resursu pārvietošanas vai jaunu resursu pievienošanas gadījumā.  

Papildinformāciju par dažādajiem resursu vajadzību veidiem un to, kā tos lietot, skatiet tēmās Operācijas resursu vajadzības un [Resursu iespējas](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Maršrutu koplietošana vairākās vietās

Ja ražojat vienu un to pašu preci vairākās ražošanas vietās un preces ražošanas darbības ir vienādas visās vietās, bieži vien varat izstrādāt koplietotu maršrutu, kas tiek izmantots visās ražošanas vietās. Lai izveidotu koplietotu maršrutu, nenorādiet vietu maršrutā. Taču joprojām ir jāizveido maršruta versija, kas saista koplietoto maršrutu ar preci katrā vietā.  

Ir arī jānodrošina, lai katras maršruta operācijas resursu vajadzības būtu izteiktas nevis kā noteikti operācijas resursi vai resursu grupas, bet gan kā nepieciešamo resursu raksturlielumi. Šādā gadījumā plānošanas programma varēs piešķirt atbilstošos operācijas resursus no vietas, kur ir ieplānota ražošana. Piemēram, ja pastāv nelielas izpildes laika atšķirības vai noteiktas operācijas iestatīšanas laiks ir raksturīgs vietai, varat norādīt šo informāciju, pievienojot šai vietai papildu operācijas saiti.  

Lai pilnībā izmantotu priekšrocības, ko sniedz koplietotie maršruti, ir jāizmanto arī resursu patēriņš atbilstošajā materiālu komplektā (MK). Kad iestatāt resursu patēriņa karodziņu MK rindā, noliktava un atrašanās vieta, no kuras ir jāpatērē šie izejmateriāli, tiek noteiktas, pamatojoties uz operācijas resursu, kam ir ieplānota attiecīgā operācija. Tāpēc noliktava un atrašanās vieta nav jānosaka līdz ražošanas plānošanas laikam. Tādējādi varat padarīt gan MK, gan maršrutu neatkarīgus no fiziskās atrašanās vietas, kur tiek ražota prece.

### <a name="standard-operation-relations"></a>Standarta operāciju saites

Ja jūsu uzņēmumā tiek izmantotas standartizētas ražošanas operācijas un rekvizīti (iestatīšanas un izpildes laiks, patēriņa aprēķināšanas metode, izmaksu aprēķināšanas metode utt.) ir vienādi vai atšķiras tikai nedaudz, ir ieteicams visām operācijām izveidot noklusējuma operāciju saites. Šādā gadījumā neveidojiet operāciju saites, kas ir raksturīgas kādam maršrutam vai izlaistajai precei.  

Turklāt, izsakot resursu vajadzības kā prasmes un iespējas un padarot maršrutus neatkarīgus no vietas, varat līdz minimumam samazināt jūsu biznesa procesa pastāvīgajai uzturēšanai vajadzīgo laiku.  

Ja lietojat šo pieeju, izpildes laika un citu rekvizītu uzturēšanai galvenokārt izmantojat lapu **Operāciju saites**.

### <a name="resource-specific-process-times"></a>Resursiem raksturīgs izpildes laiks

Ja operācijas resursu vajadzību ietvaros nenorādāt operācijas resursu vai resursu grupu, var atšķirties lietojamo resursu darbības ātrums. Tāpēc var atšķirties operācijas izpildei nepieciešamais laiks. Lai novērstu šo problēmu, varat izmantot operācijas saites lauku **Formula**, lai norādītu izpildes laika aprēķināšanas veidu. Pieejamas šādas opcijas

-   **Standarta** — (noklusējuma opcija) aprēķinam tiek izmantoti tikai operācijas saites lauki un norādītais izpildes laiks tiek reizināts ar pasūtījuma daudzumu.
-   **Noslodze** — aprēķinā tiek ietverts operācijas resursa lauks **Noslodze**. Tāpēc laiks ir atkarīgs no resursa. Operācijas resursam norādītā vērtība ir noslodze stundā. **Izpildes laiks** tiek aprēķināts kā **Pasūtījuma daudzums** dalīts ar **Noslodzi**.
-   **Partija** — izmantojot informāciju no operācijas saites, tiek aprēķināta partijas noslodze. Pēc tam, pamatojoties uz pasūtījuma daudzumu, var aprēķināt partiju skaitu un līdz ar to arī izpildes laiku.
-   **Resursu partija** — šī opcija ir gandrīz tāda pati kā opcija **Partija**. Taču aprēķinā tiek ietverts operācijas resursa lauks **Paketes noslodze**. Tāpēc laiks ir atkarīgs no resursa.

### <a name="set-up-route-groups"></a>Iestatīt maršrutu grupas

Maršrutu grupas varat definēt un to maršrutu vai darbu tipu varat iestatīt sadaļā **Ražošanas kontrole > Iestatīšana > Maršruti > Maršrutu grupas**. Katram maršruta/darba tipam maršrutu grupā varat atlasīt vai notīrīt tālāk aprakstītās opcijas.

- **Aktivizēšana** — atlasiet šo opciju, lai atlasītajam darba tipam iespējotu aprēķinus un plānošanu un lai saņemtu atsauksmes par darbu, kad tiek veikta darbu plānošana. Šī opcija ir jāatlasa, lai iespējotu darba tipu, un pēc tam ir jāatlasa pārējās opcijas šim darba tipam. Ja aktivizācija nav atlasīta, darba tips netiek iespējots neatkarīgi no pārējo opciju atlases. 
- **Darbu vadība** — atlasiet šo opciju, lai šo darba tipu iekļautu darbu pārvaldībā, kad tiek veikta darbu plānošana. 
- **Darba laiks** — atlasiet šo opciju, lai darba tipu plānotu saskaņā ar darba laika kalendāru, kas definēts operācijas resursiem, citādi tiek lietots gregoriāņu kalendārs. Darba laiku var plānot vai nu saskaņā ar gregoriāņu kalendāru, vai ar definēto darba laika kalendāru. Ja tiek atlasīta šī opcija, plānošana balstās uz definēto darba laika kalendāru. Turklāt darba tipa darbs tiek plānots no pusnakts tajā datumā, kas ir definēts kā darba sākuma datums.
- **Noslodze** — atlasiet šo opciju, lai rezervētu noslodzi darba tipam, kad tiek veikta darbu plānošana. Ja atlasāt šo opciju, noslodze tiek rezervēta, kad atlasītajam darba tipam tiek veikta darbu plānošana. Tas sniedz pārskatu par to, kuri darba tipi katrā maršrutu grupā izmanto operācijas resursus. Piemēram, gadījumā, kad žāvēšanas resursi ir deficīta resursi, šie resursi ir jānorāda kā deficīti. Žāvēšanas operācijas, kas ir piešķirtas gaidīšanas laika darba tipiem, rezervēs žāvēšanas resursus. 

Katram darba tipam jums tas vispirms ir jāaktivizē vai jādeaktivizē. Ja deaktivizēts, netiks ņemts vērā neviens no citiem iestatījumiem (darbu vadība, darba laiks un noslodze), jo šis darba tips nav aktīvs. 

Darba tipu klāstā ir atrodama Pārklāšanās. Pārklāšanās ļauj vienlaikus veikt dažādus darbus. Ka darbi pārklājas, resursus var izmantot, bet tos nevar rezervēt noteiktiem darbiem.
Tādēļ, ja iestatījumam Pārklāšanās ir atlasīta opcija Aktivizēšana, pārējiem iestatījumiem (darbu vadībai, darba laikam un noslodzei) šajā maršrutu grupā nav nekādas ietekmes. 

> [!NOTE]
> Kad jaunināt versijas, var rasties šāda kļūda: **"Plānošanas programmas izsaukšanas laikā radās CLR kļūda"**. Ja rodas šāda kļūda, dodieties uz lapu **Maršrutu grupas** un visiem maršrutiem, kur ir aktivizēta opcija **Pārklāšanās**, notīriet opcijas **Darbu vadība**, **Darba laiks** un **Noslodze**. 

## <a name="additional-resources"></a>Papildu resursi

- [Materiālu komplekti un formulas](bill-of-material-bom.md)

- [Ražošanas maršrutēšanā izmantotās izmaksu kategorijas](../cost-management/cost-categories-used-production-routings.md)

- [Resursu iespējas](resource-capabilities.md)

- [Elektronisko parakstu apskats](../../fin-and-ops/organization-administration/electronic-signature-overview.md)



