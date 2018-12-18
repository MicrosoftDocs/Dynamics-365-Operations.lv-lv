---
title: "Lietotāja pieredzes personalizēšana"
description: "Šajā tēmā skaidrots, kā personalizēt programmatūru Microsoft Dynamics 365 for Finance and Operations."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7344f460fcb443a78b254e2387fbf5c9134bf674
ms.openlocfilehash: 1860b603f789aabca1ca58848a88e11a6e08e31f
ms.contentlocale: lv-lv
ms.lasthandoff: 09/28/2018

---

# <a name="personalize-the-user-experience"></a>Lietotāja pieredzes personalizēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā personalizēt programmatūru Microsoft Dynamics 365 for Finance and Operations.

Programmā Finance and Operations ir trīs galvenās personalizēšanas klases.

- Personalizācijas, kas tiek veiktas iestatīšanas lapā. Kā piemērus varētu minēt krāsu dizainu un laika joslu.
- Personalizācijas saistībā ar lapas lietojumu, sauktas par *netiešajām* personalizācijām. Piemēram, Finance and Operations seko līdzi režģa kolonnu platumam, ja tās koriģējat, kā arī kopsavilkuma ciļņu izvēršanas vai sakļaušanas stāvoklim.
- Personalizācijas, ko lietotājs veic lapas izskata mainīšanai, izmainot elementa parādīšanas un darbības šajā lapā metodi; bieži vien tas tiek panākts, izmantojot interaktīvu personalizēšanas režīmu. Šādas personalizācijas tiek sauktas par *tiešajām* personalizācijām. Lietotājs varētu, piemēram, pievienot, slēpt vai pārkārtot lapā esošos elementus.

Ikviena personalizācija, ko lietotājs veic programmā Finance and Operations, ir paredzēta tikai attiecīgajam lietotājam, neatkarīgi no personalizācijas tipa vai uzņēmuma, ar kuru lietotājs pašlaik mijiedarbojas. Izmaiņas, ko kādai lapai veic viens lietotājs, neietekmē citus lietotājus šajā sistēmā.

## <a name="system-wide-options-for-the-current-user"></a>Sistēmas mēroga opcijas pašreizējam lietotājam

Lapā **Lietotāja opcijas** ir vairāki visas sistēmas mēroga iestatījumi pašreizējam lietotājam. Lai atvērtu lapu **Lietotāja opcijas**, navigācijas joslā atlasiet izvēlni **Iestatījumi** (zobrata simbols) un pēc tam atlasiet **Lietotāja opcijas**. Lapā **Lietotāja opcijas** ir četras cilnes, kurās ir dažādi tālāk aprakstītie lietotāja iestatījumi.

- **Vizuāls** — atlasiet lapu krāsu dizainu un elementu noklusējuma izmēru.
- **Preferences** — atlasiet noklusējuma vērtības, kas tiek izmantotas katru reizi, kad atverat programmu Finance and Operations. Šīs vērtības ietver uzņēmumu, sākuma lapu un noklusējuma skata/rediģēšanas režīmu. (Skata/rediģēšanas režīms nosaka, vai katru reizi, kad lapu atverat, lapa ir bloķēta un to var tikai apskatīt, vai lapa ir atvērta rediģēšanai.) Šajā cilnē ir arī opcijas valodai, laika joslai un datuma, laika un skaitļu formātam. Visbeidzot šajā cilnē ir dažādas preferences, kas dažādos laidienos ir atšķirīgas.
- **Konts** — pielāgojiet savu lietotājvārdu un citas ar kontu saistītas opcijas.
- **Darbplūsma** — atlasiet ar darbplūsmu saistītas opcijas.

## <a name="implicit-personalizations"></a>Netiešās personalizācijas

Netiešās personalizācijas ir personalizācijas, ko jūs veicat, vienkārši izmantojot vadīklas, kuras “atcerēsies” savu pašreizējo redzamo stāvokli.

- **Režģa kolonnas** — varat pielāgot režģī rādīto kolonnu platumu, atlasot izmēra maiņas joslu pa kreisi vai pa labi no kolonnas virsraksta un pēc tam bīdot to pa kreisi vai pa labi, līdz kolonna ir nepieciešamajā platumā. Programma Finance and Operations saglabā platumu, ko iestatāt kolonnai. Pēc tam programma maina kolonnas lielumu atbilstoši šim platumam katru reizi, kad atverat lapu, kur atrodas šis režģis.
- **Kopsavilkuma cilnes** — dažām lapām ir izvēršamas sadaļas, kas tiek sauktas par *kopsavilkuma cilnēm*. Programma Finance and Operations glabā informāciju par kopsavilkuma cilnēm, kuras esat izvērsis un sakļāvis. Pēc tam katru reizi, kad atgriežaties šajā lapā, būs izvērstas vai sakļautas tās pašas kopsavilkuma cilnes, ņemot vērā jūsu pēdējo mijiedarbību ar šo lapu. Reizēm varat palīdzēt uzlabot sistēmas veiktspēju, sakļaujot kādu kopsavilkuma cilni, jo programmai Finance and Operations nav jāizgūst informācija par šo kopsavilkuma cilni, kamēr tā nav izvērsta. Kā šajā tēmā paskaidrots tālāk, varat mainīt arī kopsavilkuma ciļņu secību lapā.
- **Papildinformācija** — dažām lapām ir sadaļa, kas tiek saukta par *papildinformācijas rūti*. Šajā rūtī ir tikai lasāma informācija, kas ir saistīta ar pašreizējo lapas tēmu. Katru sadaļu papildinformācijas rūtī sauc par *papildinformācijas lodziņu*. Varat paslēpt vai rādīt visu papildinformācijas rūti, kā arī varat izvērst vai sakļaut atsevišķus papildinformācijas lodziņus. Programma Finance and Operations saglabā jūsu preferences. Pēc tam katru reizi, kad atgriežaties šajā lapā, tiek atjaunots papildinformācijas rūts un atsevišķo papildinformācijas lodziņu stāvoklis, ņemot vērā jūsu pēdējo mijiedarbību ar šo lapu. Reizēm varat palīdzēt uzlabot sistēmas veiktspēju, sakļaujot kādu papildinformācijas lodziņu, jo programmai Finance and Operations nav jāizgūst informācija par šo papildinformācijas rūtiņu, kamēr tā nav izvērsta.
- **Darbību rūtis** — vairumā lapu *darbību rūts* tiek rādīta lapas augšdaļā. Darbību rūtī ir pogas daudzām darbībām, ko pašreizējā lapā varat veikt. Bieži vien šīs pogas ir sakārtotas cilnēs. Varat piespraust atvērtu visu darbību rūti, vai arī norādīt, ka pēc noklusējuma tai ir jābūt aizvērtai. Pēc tam nākamajā reizē, kad atverat šo lapu, programma Finance and Operations atjauno darbību rūts piesprausto stāvokli. Ja darbību rūts ir piesprausta atvērtā stāvoklī, Finance and Operations rāda arī jūsu pēdējo izmantoto darbību cilni.
- **Ātrie filtri** — *ātrais filtrs* tiek rādīts virs daudziem režģiem. Ar ātro filtru varat filtrēt režģi, pamatojoties uz jūsu atlasīto kolonnu. Programma Finance and Operations saglabā kolonnu, pēc kuras veicāt filtrēšanu. Pēc tam nākamajā reizē, kad atverat lapu, kurā atrodas šis režģis, režģis ir filtrēts pēc tās pašas kolonnas. Taču pēc tam šo režģi varat filtrēt pēc citas kolonnas.
- **Kolonnu virsrakstu filtri** — kad filtrējat režģi, izmantojot *kolonnu virsrakstu filtrus*, pēc nepieciešamības varat mainīt filtra operatoru, lai atrastu jums nepieciešamos datus. Varat, piemēram, operatoru no **sākas ar** mainīt uz **ir precīzi**. Katru reizi, kad izmantojat kādu kolonnu virsrakstu filtru un modificējat filtra operatoru, Finance and Operations saglabā šīs izmaiņas. Pēc tam programma atjauno filtra operatoru nākamajā reizē, kad filtrējat pēc šīs kolonnas.
- **Navigācijas rūts** — *navigācijas rūti* varat atvērt, jebkuras lapas kreisajā rūtī atlasot pogu **Izvēlne**. (Poga **Izvēlne** reizēm tiek saukta par *hamburgeru*, *hamburgera izvēlni* vai *hamburgera pogu*.) Navigācijas rūti varat piespraust atvērtā veidā, vai arī norādīt, ka pēc noklusējuma tai ir jābūt sakļautai. Kad navigācijas rūti piespraužat atvērtā veidā, Finance and Operations saglabā to atvērtu, līdz šo rūti sakļaujat.

## <a name="explicit-personalizations"></a>Tiešās personalizācijas

Dažādiem lietotājiem un uzņēmumiem ir dažādi uzskati par to, kādi dati viņiem ir paši svarīgākie vai kādi dati viņiem nav nepieciešami sava biznesa veikšanai. Programmā Finance and Operations varat pielāgot veidu, kādā jūsu informācija ir sakārtota un tiek izmantota. Var arī norādīt, ka daļa informācijas ir jāslēpj. Šīs iespējas ir būtiskas personiskai un produktīvai funkcionalitātei, un tās ir tiešo personalizāciju piemēri. Tiešās personalzācijas ir personalizācijas, ko veicat tieši un ar mērķi mainīt elementa vai lapas izskatu vai darbību.

### <a name="shortcut-menu-options"></a>Saīšņu izvēlnes opcijas

Saīšņu izvēlne nodrošina dažus veidus, kā tieši mainīt lapu, lai tā labāk atbilstu jūsu prasībām vai jūsu uzņēmuma prasībām. (Saīšņu izvēlne tiek saukta arī par *izvēlni, kas tiek parādīta, noklikšķinot ar peles labo pogu,* vai *kontekstizvēlni*.)

Dažas no tipiskākajām un svarīgākajām izmaiņām, ko lapai var veikt, ir tieši pieejamas kā opcijas saīšņu izvēlnē. Piemēram, sākot ar Platformas atjauninājums 17, ja vēlaties režģim pievienot vai slēpt kolonnas, vienkārši noklikšķiniet ar peles labo pogu uz režģa kolonnas virsraksta un pēc tam atlasiet **Pievienot kolonnas** vai **Slēpt šo kolonnu**.

Turklāt visparastākie tiešās personalizēšanas tipi ir pieejami, noklikšķinot ar peles labo pogu uz kāda elementa un pēc tam atlasot **Personalizēt**. (Ņemiet vērā, ka ne visus lapā esošos elementus var personalizēt.) Kad lietojat šo personalizēšanas metodi, tiek parādīts elementa rekvizītu logs.

[![Elementa rekvizītu personalizēšana](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg)

Rekvizītu logu varat izmantot, lai personalizētu kādu elementu tālāk norādītajos veidos.

- Mainīt elementa etiķeti.
- Paslēpt elementu, lai lapā tas nebūtu redzams. Šajā laukā esošie dati netiek dzēsti vai modificēti. Informācija vienkārši vairs netiek rādīta lapā.
- Ietvert informāciju kopsavilkuma cilnes kopsavilkuma sadaļā (ja šis elements atrodas kopsavilkuma cilnē).
- Izlaist šo lauku, kad nospiežat taustiņu Tab, lai pārvietotos starp lapā esošajiem laukiem.
- Novērst šajā laukā esošo datu rediģēšanu (jebkuram ierakstam).

Atkarībā no elementa rekvizītu logā var būt citas personalizēšanas iespējas. Piemēram, elementa rekvizītu logā jums varētu būt iespējams attiecīgo elementu paaugstināt uz informācijas paneli, un šis rekvizītu logs informācijas panelim varētu ļaut jums izveidot jaunu darbvietu attiecīgajā informācijas panelī.

### <a name="the-personalization-toolbar"></a>Personalizēšanas rīkjosla

Ja vēlaties lapā veikt vairākas izmaiņas vai izmaiņas, kuras nevar veikt, izmantojot citus mehānismus (piemēram, pārkārtojot elementus), var izmantot rīkjoslu **Personalizēšana**. Lai atvērtu rīkjoslu **Personalizēšana**, elementa rekvizītu logā atlasiet **Personalizēt šo formu**. Vienumu **Personalizēt šo formu** varat atlasīt arī katras lapas darbību rūts cilnes **Opcijas** grupā **Personalizēt**.

[![Personalizēšanas rīkjosla](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

#### <a name="navigating-the-page"></a>Pārvietošanās lapā

Pārvietošanās lapā, ja ir atvērta rīkjosla **Personalizēšana**, ir atkarīga no instalētās platformas versijas.

- Pirms Platformas atjauninājuma 19, ja rīkjosla **Personalizēšana** ir atvērta, lapa ir pieejama tikai lasīšanas režīmā (tajā neko nevar ievadīt) un tā nav interaktīva (var veikt tikai lapā redzamo elementu izmaiņas). Ja vēlaties veikt elementu sakļautā sadaļā vai citā cilnē izmaiņas, ir jāaizver rīkjosla **Personalizēšana**, jāizvērš sadaļa vai jāpārslēdzas uz vēlamo cilni un pēc tam vēlreiz jāatver rīkjosla **Personalizēšana**.

- Sākot ar Platformas atjauninājumu 19, ja rīkjosla **Personalizēšana** ir atvērta, lapa vēl joprojām ir pieejama tikai lasīšanas režīmā, bet tā ir vairāk interaktīva. Konkrēti, ja rīkjosla **Personalizēšana** ir atvērta. var izvērst vai sakļaut rūti Papildinformācija, pārslēgt cilnes un izvērst vai sakļaut sadaļas tādā pašā veidā, kā tas lapā tiek darīt parasti. Lai personalizēšanas izmaiņas stātos spēkā sakļautajā sadaļā vai cilnē (piemēram, lai slēptu kopsavilkuma cilni), ir jāaktivizē poga, kas tiek parādīta blakus sakļautajai sadaļai vai cilnei, ja uz tās pāriet, izmantojot tastatūru, vai novieto virs tās kursoru.

#### <a name="personalization-tools"></a>Personalizēšanas rīki

Rīkjoslā **Personalizēšana** ir pieejami tālāk uzskaitītie rīki.

- Izmantojiet rīku **Atlasīt**, lai atlasītu un mainītu elementa rekvizītus. Atlasiet rīku **Atlasīt** un pēc tam atlasiet elementu, kura rekvizītus vēlaties modificēt. Kad atlasāt kādu elementu, tiek parādīts šī elementa rekvizītu logs, un jūs varat modificēt jebkurus šī elementa rekvizītus. Šo procesu varat atkārtot citiem elementiem, kurus attiecīgajā lapā ar personalizēt. Taču noteiktu elementu lietošanas veida dēļ programma Finance and Operations jums neļauj mainīt dažus to rekvizītus. Tādēļ, kad atlasāt kādu elementu, var tikt rādīts, ka dažus tā rekvizītus nevar modificēt. Piemēram, jūs nevarat paslēpt lauku, kas ir obligāts.
- Izmantojiet rīku **Pārvietot**, lai kādu elementu pārvietotu uz citu atrašanās vietu pašreizējā elementu grupā. (Elementu nevar pārvietot ārpus tā pamata grupas.) Atlasiet rīku **Pārvietot** un pēc tam atlasiet elementu, kuru vēlaties pārvietot. Kad atlasāt kādu elementu, programma Finance and Operations skenē lapu, lai noteiktu, kurp šo elementu var pārvietot. Pēc tam programma izveido virkni ar “nomešanas zonām”. Kad šo elementu velkat pa pašreizējo grupu, katra “nomešanas zona” tiek rādīta kā iekrāsota, trekna līnija blakus apgabalam, kur šo elementu var nomest.
- Izmantojiet rīku **Paslēpt**, lai slēptu kādu elementu šajā lapā. Atlasiet rīku **Paslēpt** un pēc tam atlasiet elementu, kuru vēlaties paslēpt. Kad atlasāt rīku **Paslēpt**, visi pašlaik paslēptie elementi kļūst redzami un tiek rādīti ēnotā konteinerā. Pēc tam varat atcelt to slēpšanu. Atlasot rīku **Atlasīt**, varat redzēt, kā lapa izskatās, kad atlasītie elementi tiek slēpti.

    - Sākot ar Platformu atjaunināšanas 18, obligātos laukus un sadaļas, kas ietver nepieciešamos laukus, var slēpt. Tas ļauj iegūt vienkāršotu pieredzi, ja obligātie lauki, kuri saskaņā ar biznesa loģiku ir iestatīti pēc noklusējuma, netiek parādīti. Slēptie obligātie lauki īslaicīgi tiek parādīti, ja, mēģinot veikt saglabāšanu, tie ir tukši.

- Izmantojiet rīku **Kopsavilkums**, kad vēlaties, lai elements tiktu rādīts kopsavilkuma cilnes kopsavilkuma sadaļā. Kopsavilkuma rīks attiecas tikai uz laukiem, kas atrodas kādā kopsavilkuma cilnes sadaļā. Kad atlasāt rīku **Kopsavilkums**, visi lauki, kas ir atlasīti kā kopsavilkuma lauki, tiek radīti ēnotā konteinerā. Atlasot laukus, varat interaktīvi pievienot laukus kopsavilkuma cilnes kopsavilkumam un noņemt laukus no kopsavilkuma cilnes kopsavilkuma.
- Izmantojiet rīku **Izlaist**, lai izņemtu kādu elementu no lapas tastatūras tabulācijas secības. Kad atlasāt rīku **Izlaist**, visi pašlaik izlaistie elementi tiek rādīti ēnotā konteinerā. Pēc tam varat tos atkal ietvert tabulācijas secībā.
- Izmantojiet rīku **Rediģēt**, lai kādu elementu atzīmētu kā rediģējamu vai nerediģējamu. Kad atlasāt rīku **Rediģēt**, visi pašlaik nerediģējamie elementi tiek rādīti ēnotā konteinerā. Pēc tam varat tos atkal padarīt par rediģējamiem. Ņemiet vērā, ka daži lauki ir obligāti un tos nevar padarīt nerediģējamus. Pie šiem laukiem tiek rādīts piekaramās slēdzenes simbols.
- Izmantojiet pogu **Ievietot**, lai redzētu sarakstu ar elementiem, ko var ievietot lapā.

    - Atlasiet rīku **Lauks** zem pogas **Ievietot**, lai savai lapai pievienotu lauku. Kad izmantojat rīku **Lauks**, varat pievienot tikai tādus laukus, kas veido daļu no lapas definīcijas, bet pašlaik attiecīgajā lapā netiek rādīti. Informāciju par to, kā izveidot jaunus laukus, kuri nav daļa no pašreizējās lapas definīcijas, skatiet tēmā [Pielāgoti lauki](user-defined-fields.md). Kad ir atlasīts rīks **Lauks**, jums vispirms ir jāatlasa grupa vai apgabals, kur vēlaties pievienot lauku. Dialoglodziņā tiek rādīts saraksts ar laukiem, kas ir saistīti ar atlasīto grupu vai apgabalu. Šajā dialoglodziņā atlasiet vienu vai vairākus laukus, ko pievienot, un pēc tam atlasiet **Ievietot**. Lai noņemtu kādu lauku, ko iepriekš pievienojāt, atkārtojiet šo procesu, bet dialoglodziņā noņemiet attiecīgā lauka atlasi.
    - Atlasiet rīku **PowerApp** zem pogas **Ievietot**, lai lapā iegultu programmu, kura tika izveidota, izmantojot Microsoft PowerApps. Plašāku informāciju par to, kā lapā iegult PowerApps programmu, skatiet tēmā [PowerApps iegulšana](embed-power-apps.md).

- Atlasiet pogu **Pārvaldīt**, lai skatītu ar visām pašreizējas lapas personalizēšanas darbībām saistīto pārvaldības opciju sarakstu.

    - Atlasiet vienumu **Notīrīt**, lai lapai atiestatītu noklusējuma instalēto stāvokli. Tādējādi tiek notīrītas visas pašreizējās lapas personalizācijas. Šo darbību nevar atsaukt. Tādēļ šī opcija ir jāizmanto tikai tad, ja esat pārliecināts, ka vēlaties lapu atiestatīt.
    - Atlasiet **Importēt**, lai ielādētu personalizāciju no kāda faila, kuru šai lapai iepriekš izveidojāt jūs pats vai kāds cits. Visas jūsu pašreizējās personalizācijas šai lapai tiek aizstātas ar personalizācijām no atlasītā faila.
    - Atlasiet **Eksportēt**, lai savas personalizācijas šai lapai saglabātu kādā failā. Savas personalizācijas varat koplietot ar citiem lietotājiem. Šiem lietotājiem ir nepieciešams tikai importēt failu, kurā ir jūsu personalizācijas šai lapai.

- Atlasiet pogu **Aizvērt**, lai rīkjoslu **Personalizēšana** aizvērtu un lapu atgrieztu tās iepriekšējā interaktīvajā stāvoklī.

Kad tiek izmantota rīkjosla **Personalizēšana**, operāciju saglabāšana notiek automātiski. Jūsu veiktā personalizēšana stājas spēkā, līdzko to veicat, un jums nav jāatlasa poga **Saglabāt**. Dažreiz, kad atlasāt kādu rīku, blakus kādam elementam tiek rādīts piekaramās slēdzenes simbols. Šis simbols norāda, ka nevarat modificēt šī elementa rekvizītus, kas ir saistīti ar atlasīto rīku, jo šo rekvizītu izmaiņas neļaus lapai darboties pareizi.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Elementa, saraksta vai saites uz darbvietu pievienošana

Dažām lapām, kurās ir saraksti, ir pieejams papildu personalizēšanas līdzeklis. Darbību rūts cilnes **Opcijas** grupā **Personalizēt** esošā poga **Pievienot darbvietu** ļauj jums noteiktā darbvietā rādīt informāciju no pašreizējā saraksta. Darbvietā varat rādīt filtrētu un sakārtotu informācijas skatu vai rādīt noklusējuma skatu. Var arī norādīt, vai informācija darbvietā tiek rādīta kā saraksts, kā kopsavilkuma elements, kurā var rādīt sarakstā esošo elementu skaitu, vai kā saite.

[![Pievienošana darbvietai](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Lai darbvietai pievienotu kādu sarakstu, vispirms kārtojiet vai filtrējiet lapā esošo sarakstu, lai informācija tajā tiktu rādīta tā, kā to vēlaties rādīt darbvietā. Pēc tam atlasiet **Pievienot darbvietai**. Atlasiet darbvietu un pēc tam laukā **Prezentācija** atlasiet **Saraksts**. Kad atlasāt vienumu **Konfigurēt**, tiek parādīts dialoglodziņš, kur varat atlasīt kolonnas, kuras ir jārāda šīs darbvietas sarakstā. Varat arī norādīt etiķeti, ko izmantot sarakstam šajā darbvietā.
- Lai darbvietai pievienotu kādu elementu, vispirms filtrējiet lapā esošo sarakstu, lai tajā būtu redzami dati, kurus vēlaties apkopot vai kuriem vēlaties ātri piekļūt. Pēc tam atlasiet **Pievienot darbvietai**. Atlasiet darbvietu un pēc tam laukā **Prezentācija** atlasiet **Elements**. Kad ir atlasīts vienums **Konfigurēt**, tiek paradīts dialoglodziņš, kur varat norādīt etiķeti, kuru izmantot elementam šajā darbvietā. Var arī norādīt, vai elementam ir jārāda skaits. Kad elements ir pievienots darbvietai, varat to atlasīt, lai no darbvietas atvērtu pašreizējo lapu un skatītu filtrēto sarakstu, kurš ir saistīts ar šo elementu.
- Lai pievienotu saiti uz darbvietu, vispirms filtrējiet lapā esošo sarakstu tā, lai tajā būtu redzami jums interesējošie dati. Pēc tam atlasiet **Pievienot darbvietai**. Atlasiet darbvietu un pēc tam laukā **Prezentācija** atlasiet **Saite**. Kad ir atlasīts vienums **Konfigurēt**, tiek paradīts dialoglodziņš, kur varat norādīt etiķeti, kuru izmantot šai saitei. Pēc izvēles varat arī norādīt etiķeti jaunai sadaļai, kurā būs šī saite.

Kad jūsu saraksts, elements vai saite ir pievienota darbvietai, varat atvērt šo darbvietu un mainīt tajā elementu secību, ja vēlaties.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Kopsavilkuma pievienošana no darbvietas informācijas panelim

Dažās darbvietās ir skaita elementi (t.i., elementi, kuros ir skaitļi), un jūs varētu vēlēties šos elementus rādīt arī savā informācijas panelī. Darbvietā ar peles labo pogu noklikšķiniet uz skaita elementa un pēc tam atlasiet vienumu **Personalizēt**. Pēc tam elementa rekvizītu logā atlasiet **Piespraust informācijas panelim**. Nākamajā reizē, kad atverat (un atsvaidzināt) atlasīto informācijas paneli, šis skaits tiek rādīts zem attiecīgās darbvietas navigācijas elementa. Varat atlasīt, lai šis skaits tieši novirzītu uz datiem, kurus tas attēlo.

### <a name="personalizing-your-dashboard"></a>Sava informācijas paneļa personalizēšana

Informācijas panelis bieži vien ir pirmā lapa, ko redzat, atverot programmu Finance and Operations. Informācijas paneli varat personalizēt tā, lai tajā tiktu rādīti vienīgi darbvietas elementi, kurus vēlaties redzēt. Varat arī pārkārtot elementus, lai tie atrastos tādā secībā, kādā tos vēlaties redzēt, varat pārdēvēt darbvietas navigācijas elementus vai pievienot pilnīgi jaunu darbvietas elementu.

Lai personalizētu informācijas paneli, ar peles labo pogu noklikšķiniet uz jebkura elementa un pēc tam atlasiet **Personalizēt**, lai atvērtu elementa rekvizītu logu.

- Ja vēlaties slēpt vai pārdēvēt atlasīto elementu, izmaiņas varat veikt tieši rekvizītu logā.
- Lai pārkārtotu darbvietas elementus, rekvizītu logā atlasiet **Personalizēt šo formu**, tādējādi atverot rīkjoslu **Personalizēšana**. Pēc tam varat izmantot rīku **Pārvietot**, lai elementus izkārtotu pēc vēlēšanās.
- Lai izveidotu jaunu darbvietas elementu, rekvizītu logā atlasiet vienumu **Pievienot darbvietu**. Informācijas paneļa apakšā tiek izveidots jauns darbvietas elements. Šo jauno darbvietas elementu pēc vēlēšanās varat pārdēvēt. Sarakstus, elementus un saites darbvietai varat arī pievienot, kā aprakstīts šīs tēmas sadaļā [Sarakstu, elementu vai saišu pievienošana darbvietām](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace).

## <a name="administration-of-personalization"></a>Personalizēšanas administrēšana

Pēc lapas personalizēšanas savas personalizācijas varat kopīgot ar citiem lietotājiem, eksportējot personalizēto lapu. Pēc tam varat lūgt citiem lietotājiem atvērt personalizēto lapu un importēt jūsu izveidoto personalizēšanas failu. Vai arī savu personalizēšanas failu varat iedot kādam lietotājam, kuram ir administratora privilēģijas. Pēc tam šis lietotājs var izmantot jūsu personalizēšanas failu vairākiem lietotājiem vienlaikus.

Lietotāji ar administratora privilēģijām lapā **Personalizācija** var arī pārvaldīt personalizācijas citiem lietotājiem. Šai lapai ir četras tālāk aprakstītās cilnes.

- **Lietot** — varat importēt vai atlasīt kādu personalizāciju vienam vai vairākiem lietotājiem. Lai personalizāciju lietotu vienam lietotājam vai vairākiem, vispirms atlasiet kādu lomu un lietotājus, kuriem ir šī loma. Pēc tam atlasiet esošu personalizāciju, kuru lietot atlasītajiem lietotājiem, vai importējiet personalizēšanas failu. Personalizācija tiek validēta un tiek lietota visiem atlasītajiem lietotājiem nākamajā reizē, kad viņi atver atlasīto lapu.
- **Notīrīt** — varat notīrīt visas lapai vai darbvietai paredzētās personalizācijas vienam vai vairākiem lietotājiem. Vispirms atlasiet lapu vai darbvietu, lai redzētu sarakstu ar lietotājiem, kuri to ir personalizējuši. Pēc tam atlasiet lietotājus, kuriem ir nepieciešams notīrīt šīs lapas vai darbvietas personalizācijas, un atlasiet **Notīrīt**. Tiek dzēstas visas personalizācijas, ko atlasītie lietotāji ir lietojuši atlasītajai lapai vai darbvietai. Šo darbību nevar atsaukt. Taču, ja šai lapai vai darbvietai bija saglabāta kāda personalizācija, šo personalizāciju var importēt vēlreiz.
- **Pārvaldnieks pēc lietotāja** — atlasiet lietotāju, lai redzētu sarakstu ar lapām, ko šis lietotājs ir personalizējis. Pēc tam varat iespējot vai atspējot atlasītā lietotāja spēju lietot personalizācijas konkrētām lapām vai visai sistēmai. Varat arī importēt, eksportēt vai notīrīt personalizāciju atlasītajam lietotājam.
- **Sistēma** — varat īslaicīgi atspējot visas personalizācijas visiem lietotājiem sistēmā. Šajā gadījumā personalizācijas tiek dzēstas. Visas lapas vienkārši tiek atiestatītas uz to noklusējuma stāvokli visiem lietotājiem. Ja vēlāk personalizāciju atkal iespējojat, visas personalizācijas tiek atkal lietotas. Varat arī neatgriezeniski dzēst visas personalizācijas visiem lietotājiem sistēmā. Izdzēstas personalizācijas nav iespējams atgūt. Tādēļ, pirms veicat šo uzdevumu, noteikti eksportējiet visas personalizācijas, kuras vēlāk varētu būt nepieciešams.

## <a name="personalization-of-inventory-dimensions"></a>Krājumu dimensiju personalizēšana

Kad personalizējat krājumu dimensiju iestatījumus lapā, ņemiet vērā iestatījumus, kas izveidoti, izmantojot opciju **Parādīt dimensijas**. Piemēram, jūs izmantojat personalizāciju, lai paslēptu kolonnu partijas numuru krājumu dimensijai, bet šī kolonna tiek rādīta nākamajā reizē, kad lapa tiek atvērta. Tā notiek, jo iestatījumi **Dimensiju rādīšana** kontrolē, kuras krājumu dimensiju kolonnas tiek rādītas.

Iestatījumi **Dimensiju rādīšana** tiek lietoti visās lapās, un tiem ir prioritāte pār jebkādiem personalizētajiem krājumu dimensiju lauku iestatījumiem atsevišķās lapās.

Tādējādi, tāpat kā iepriekšējā piemērā, ja nevēlaties, lai tiek parādīta partijas numura krājumu dimensijas kolonna, ir jānoņem attiecīgās dimensijas atzīme tabulas opcijas **Parādīt dimensijas** ietvaros. Galu galā šīs izmaiņas attieksies ne tikai uz vienu konkrēto lapu, bet uz visām lapām.

