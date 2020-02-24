---
title: Lietotāja pieredzes personalizēšana
description: Šajā tēmā ir paskaidrots, kā varat personalizēt programmu.
author: jasongre
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745248a0c7e54b58b1d3e491f3bbb067ec0e2c2
ms.sourcegitcommit: d8a2301eda0e5d0a6244ebbbe4459ab6caa88a95
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029366"
---
# <a name="personalize-the-user-experience"></a>Lietotāja pieredzes personalizēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā varat personalizēt programmu.

Ir trīs pamata personalizācijas klases.

- Personalizācijas, kas veiktas iestatīšanas lapā. Kā piemērus varētu minēt krāsu dizainu un laika joslu.
- Personalizācijas, kas saistītas ar lapas lietojumu. Šādas personalizācijas ir zināmi kā *netiešas* personalizācijas. Piemēram, sistēma seko līdzi režģa kolonnu platumam, ja tās koriģējat, kā arī kopsavilkuma ciļņu izvēršanas vai sakļaušanas stāvoklim.
- Personalizācijas, ko lietotājs veic lapas izskatam, izmainot elementa parādīšanas un darbības šajā lapā metodi; bieži vien tas tiek panākts, izmantojot interaktīvu personalizēšanas režīmu. Šādas personalizācijas ir zināmi kā *tiešas* personalizācijas. Piemēram, lietotājs varētu pievienot, slēpt vai pārkārtot lapā esošos elementus.

Ikviena personalizācija, ko veic lietotājs, ir paredzēta tikai attiecīgajam lietotājam, neatkarīgi no personalizācijas tipa vai uzņēmuma, ar kuru lietotājs pašlaik mijiedarbojas. Izmaiņas, ko kādai lapai veic viens lietotājs, neietekmē citus lietotājus šajā sistēmā.

## <a name="system-wide-options-for-the-current-user"></a>Sistēmas mēroga opcijas pašreizējam lietotājam

Lapā **Lietotāja opcijas** ir vairāki visas sistēmas mēroga iestatījumi pašreizējam lietotājam. Lai atvērtu lapu **Lietotāja opcijas**, navigācijas joslā atlasiet pogu **Iestatījumi** (zobrata simbols) un pēc tam atlasiet **Lietotāja opcijas**. Lapā **Lietotāja opcijas** ir četras cilnes, kurās ir dažādi tālāk aprakstītie lietotāja iestatījumi.

- **Vizuāls** – atlasiet lapu krāsu dizainu un elementu noklusējuma izmēru.
- **Preferences**— atlasiet noklusējuma vērtības, kas tiek izmantotas katru reizi, kad atverat sistēmu. Šīs vērtības ietver uzņēmumu, sākuma lapu un noklusējuma skata/rediģēšanas režīmu. (Skata/rediģēšanas režīms nosaka, vai katru reizi, kad lapu atverat, lapa ir bloķēta un to var tikai apskatīt, vai lapa ir atvērta rediģēšanai.) Šajā cilnē ir arī opcijas valodai, laika joslai un datuma, laika un skaitļu formātiem. Visbeidzot šajā cilnē ir dažādas preferences, kas dažādos laidienos ir atšķirīgas.
- **Konts** – pielāgojiet savu lietotājvārdu un citas ar kontu saistītas opcijas.
- **Darbplūsma** – atlasiet ar darbplūsmu saistītas opcijas.

Papildus lietotāja iestatījumu mainīšanai var arī izmantot lapu **Lietojuma dati** lai apskatītu un izdzēstu lietojuma un personalizētos datus. Vienkārši atlasiet **Lietojuma dati** darbības rūtī.

Lietojot programmu, daudzi atlases elementi tiek saglabāti, lai turpmāk sistēmu būtu vieglāk izmantot. Cilnē **Personalizēšana** jūs varat skatīt un pārvaldīt izmaiņas, kuras personīgi veiktas sistēmas lapās. Šajā cilnē var arī atiestatīt līdzekli remarkas (tas ir, uznirstošos logus, kas ievieš jaunus sistēmas līdzekļus). Pēc tam tiks parādīts brīdinājums par iepriekš konstatētajiem līdzekļiem.

> [!NOTE]
> Ja ir ieslēgts līdzeklis [Saglabātie skati](saved-views.md), varat skatīt un pārvaldīt jūsu personalizācijas, atlasot **Personalizācijas** darbības rūtī **Lietotāja opcijas**.

## <a name="implicit-personalizations"></a>Netiešās personalizācijas

Netiešās personalizācijas ir personalizācijas, ko jūs veicat, vienkārši izmantojot vadīklas, kuras saglabā savu pašreizējo redzamo stāvokli.

- **Režģa kolonnas platums** – varat pielāgot režģī rādīto kolonnu platumu, atlasot izmēra maiņas joslu pa kreisi vai pa labi no kolonnas virsraksta un pēc tam bīdot to pa kreisi vai pa labi, līdz kolonna ir nepieciešamajā platumā. Programma saglabā platumu, ko iestatāt kolonnai. Pēc tam, nākamreiz, atverot lapu, kurā iekļauts šis režģis, kolonnas lielums tiks mainīts līdz tādam platumam.
- **Režģa kolonnu kopsumma** — (pieejams tikai ar iespējotu jaunā režģa kontroli) varat izlemt, vai kopsumma ir jāparāda jebkuras skaitliskas kolonnas apakšpusē, kā arī to, vai ir redzama režģa kājene. Programma saglabā šos datus, lai šīs preferences tiktu saglabātas nākamajā reizē, kad atvērsit lapu. Papildinformāciju skatiet tēmā [Režģa iespējas](grid-capabilities.md). 
- **Kopsavilkuma cilnes** – dažām lapām ir izvēršamas sadaļas, kas tiek sauktas par *kopsavilkuma cilnēm*. Programma glabā informāciju par kopsavilkuma cilnēm, kuras esat izvērsis un sakļāvis. Pēc tam, nākamreiz, kad jūs atvērsit šo lapu, būs izvērstas vai sakļautas tās pašas kopsavilkuma cilnes, ņemot vērā jūsu pēdējo mijiedarbību ar šo lapu. Reizēm jūs varat palīdzēt uzlabot sistēmas veiktspēju, sakļaujot kādu kopsavilkuma cilni, jo programmai nav jāizgūst informācija par šo kopsavilkuma cilni, kamēr tā nav izvērsta. Kā šajā tēmā ir paskaidrots tālāk, varat mainīt arī kopsavilkuma ciļņu secību lapā.
- **Papildinformācijas lodziņš** – Dažām lapām ir rūts **Saistīta informācija**, kurā ir parādīta tikai lasāma informācija, kas saistīta ar pašreizējo lapas tēmu. Katru sadaļu rūtī **Saistīta informācija** sauc par *Papildinformācijas lodziņš*. Varat izvērst vai sakļaut rūti **Saistīta informācija**, kā arī varat izvērst vai sakļaut atsevišķus papildinformācijas lodziņus. Programma saglabā šīs preferences. Pēc tam, nākamreiz, kad atverat šo lapu, tiek izvērsta vai sakļauta rūts **Saistīta informācija** un atsevišķo papildinformācijas lodziņu stāvoklis, ņemot vērā jūsu pēdējo mijiedarbību ar šo lapu. Reizēm jūs varat palīdzēt uzlabot sistēmas veiktspēju, sakļaujot kādu Papildinformācijas lodziņu, jo programmai nav jāizgūst informācija par šiem Papildinformācijas lodziņiem, kamēr tā nav izvērsta.
- **Darbību rūtis** – vairumā lapu *darbību rūts* tiek rādīta lapas augšdaļā. Darbību rūtī ir pogas daudzām darbībām, ko pašreizējā lapā varat veikt. Bieži vien šīs pogas ir sakārtotas cilnēs. Varat piespraust visu darbību rūti atvērtā veidā, vai arī norādīt, ka pēc noklusējuma tai ir jābūt sakļautai. Pēc tam, nākamreiz, kad jūs atvērsit šo lapu, būs atvērtas vai sakļautas Darbības rūtis, ņemot vērā jūsu pēdējo mijiedarbību ar šo lapu. Ja jūs piespraudāt darbības rūti atvērtā veidā, tiks rādīta pēdējā cilne, kuru izmantojāt.
- **Ātrie filtri** – *ātrais filtrs* tiek rādīts virs daudziem režģiem. Ar ātro filtru varat filtrēt režģi, pamatojoties uz jūsu atlasīto kolonnu. Programma saglabā kolonnu, pēc kuras veicāt filtrēšanu. Pēc tam nākamajā reizē, kad atverat lapu, kurā atrodas šis režģis, režģis ir filtrēts pēc tās pašas kolonnas. Taču pēc tam varat izvēlēties citu kolonnu, lai filtrētu šo režģi.
- **Kolonnu virsrakstu filtri** – kad filtrējat režģi, izmantojot *kolonnu virsrakstu filtri*, pēc nepieciešamības varat mainīt filtra operatoru, lai atrastu jums nepieciešamos datus. Varat, piemēram, operatoru no **sākas ar** mainīt uz **ir precīzi**. Katru reizi, kad izmantojat kādu kolonnu virsrakstu filtru un maināt filtra operatoru, programma saglabā šīs izmaiņas. Pēc tam programma atjaunos filtra operatoru nākamajā reizē, kad filtrējat pēc šīs kolonnas.
- **Navigācijas rūts** – Varat atvērt *navigācijas rūti*, jebkuras lapas augšējā kreisajā rūtī atlasot pogu **Izvērsiet navigācijas rūti**. (Šī poga reizēm tiek saukta par _**Izvēlnes** pogu_, *hamburgeru*, *hamburgera izvēlni* vai *hamburgera pogu*.) Navigācijas rūti varat piespraust atvērtā veidā, vai arī norādīt, ka pēc noklusējuma tai ir jābūt sakļautai. Pēc tam, kad navigācijas rūti piespraužat atvērtā veidā, programma saglabā to atvērtu, līdz šo rūti sakļaujat.

## <a name="explicit-personalizations"></a>Tiešās personalizācijas

Dažādiem lietotājiem un uzņēmumiem ir dažādi uzskati par to, kādi dati viņiem ir paši svarīgākie un kādi dati viņiem nav nepieciešami sava biznesa veikšanai. Jūs varat pielāgot veidu, kādā jūsu informācija ir sakārtota un tiek izmantota. Var arī norādīt, ka daļa informācijas ir jāslēpj. Šīs iespējas ir būtiskas personiskai un produktīvai pieredzei, un tās ir tiešo personalizāciju piemēri. Tiešās personalzācijas ir personalizācijas, ko veicat tieši, jo vēlēties mainīt elementa vai lapas izskatu vai darbību.

### <a name="shortcut-menu-options"></a>Saīšņu izvēlnes opcijas

Saīšņu izvēlne sniedz dažus veidus, kā tieši mainīt lapu, lai tā labāk atbilstu jūsu prasībām vai jūsu uzņēmuma prasībām. (Saīšņu izvēlne tiek saukta arī par *izvēlni, kas tiek parādīta, noklikšķinot ar peles labo pogu,* vai *kontekstizvēlni*.)

Dažas no tipiskākajām un svarīgākajām izmaiņām, ko lapai var veikt, ir tieši pieejamas kā opcijas saīšņu izvēlnē. Piemēram, sākot ar Platformas atjauninājums 17, ja vēlaties režģim pievienot vai slēpt kolonnas, vienkārši noklikšķiniet ar peles labo pogu uz kolonnas virsraksta un pēc tam atlasiet **Pievienot kolonnas** vai **Slēpt šo kolonnu**.

Turklāt visparastākie tiešās personalizēšanas tipi ir pieejami, noklikšķinot ar peles labo pogu uz kāda elementa un pēc tam atlasot **Personalizēt**. (Ņemiet vērā, ka ne visus lapā esošos elementus var personalizēt.) Izmantojot šo personalizēšanas metodi, tiek parādīts elementa rekvizītu logs.

![Elementa rekvizītu personalizēšana](./media/personalization-element-properties.png)

Rekvizītu logu varat izmantot, lai personalizētu kādu elementu tālāk norādītajos veidos.

- Mainīt elementa etiķeti.
- Paslēpt elementu, lai lapā tas nebūtu redzams. Šajā laukā esošie dati netiek dzēsti vai modificēti. Informācija vienkārši vairs netiek rādīta lapā.
- Ietvert informāciju kopsavilkuma cilnes kopsavilkuma sadaļā (ja elements atrodas kopsavilkuma cilnē).
- Izlaist lauku, lai tas nekad nebūtu fokusā, kad tiek ritināta lapa.
- Novērst šajā laukā esošo datu rediģēšanu (jebkuram ierakstam)

Atkarībā no elementa rekvizītu logā var būt citas personalizēšanas iespējas. Piemēram, elementa rekvizītu logā jums varētu būt iespējams attiecīgo elementu paaugstināt uz informācijas paneli, un šis rekvizītu logs informācijas panelim varētu ļaut jums izveidot jaunu darbvietu attiecīgajā informācijas panelī.

### <a name="the-personalization-toolbar"></a>Personalizēšanas rīkjosla

Ja vēlaties lapā veikt vairākas izmaiņas vai izmaiņas, kuras nevar veikt, izmantojot citus mehānismus (piemēram, ja vēlāties pārkārtot elementus), var izmantot rīkjoslu **Personalizēšana**. Lai atvērtu **Personalizēšana** rīkjoslu, veiciet vienu no šīm darbībām:

- Atlasiet **Personalizēt šo lapu** elementa rekvizītu logā.
- Atlasiet **Personalizēt šo veidlapu** grupā **Personalizēt** cilnē **Opcijas** jebkuras lapas darbību panelī.
- Navigācijas joslā atlasiet pogu **Iestatījumi** (zobrata simbols) un pēc tam atlasiet **Personalizēt.**

[![Personalizēšanas rīkjosla](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Pārvietošanās lapā

Kad rīkjosla **Personalizēšana** ir atvērta, pamatā esošā lapa ir tikai lasāma (citiem vārdiem, nevar rediģēt datus), bet tā joprojām ir interaktīva. Konkrēti, varat izvērst vai sakļaut rūti **Saistītā informācija**, pārslēgt cilnes un izvērst vai sakļaut sadaļas, tāpat kā parasti šīs darbības tiek veiktas lapā. Lai personalizēšana stātos spēkā sakļautajā sadaļā vai cilnē (piemēram, lai slēptu kopsavilkuma cilni), jums vienkārši jāizvēlas poga, kas tiek parādīta blakus tai sadaļai vai cilnei, ja uz tās pāriet, izmantojot tastatūru, vai novieto virs tās kursoru.

#### <a name="personalization-tools"></a>Personalizēšanas rīki

Rīkjoslā **Personalizēšana** ir pieejami tālāk uzskaitītie rīki.

- Izmantojiet rīku **Atlasīt**, lai atlasītu un mainītu elementa rekvizītus. Lai izmantotu šo rīku, rīkjoslā atlasiet pogu **Atlasīt** un pēc tam atlasiet vēlamo elementu. Elementa rekvizītu logs parādās, un jūs varat mainīt jebkurus šī elementa rekvizītus. Šo procesu varat atkārtot citiem elementiem, kurus attiecīgajā lapā var personalizēt. Ņemiet vērā, ka daži personalizēšanas rekvizīti var nebūt pieejami dažos scenārijos. Piemēram, jūs nevarat bloķēt lauku, kas ir obligāts.
- Izmantojiet rīku **Paslēpt**, lai slēptu kādu elementu šajā lapā. Lai izmantotu šo rīku, rīkjoslā atlasiet pogu **Paslēpt** un pēc tam atlasiet elementu, kuru vēlāties paslēpt. Kad izmantojiet rīku **Paslēpt**, visi pašlaik paslēptie elementi kļūst redzami, bet tiek rādīti ēnotā konteinerā. Pēc tam jūs varat padarīt elementu redzamu, atlasot to. Lai apskatītu, kā lapa izskatīsies, kad elementi ir paslēpti, pārslēdzieties uz citu personalizēšanas rīku.
- Pielietojiet rīku **Pievienot lauku**, lai pievienotu lauku savai lapai. Kad izmantojat šo rīku, varat pievienot tikai tādus laukus, kas ir daļa no lapas definīcijas. Informāciju par to, kā izveidot jaunus laukus, kuri nav daļa no pašreizējās lapas definīcijas, skatiet tēmā [Izveidot un strādāt ar pielāgotajiem laukiem](user-defined-fields.md). Kad uzdevumu joslā ir atlasīta poga **Pievienot lauku**, jums vispirms ir jāatlasa grupa vai apgabals, kur vēlaties pievienot lauku. Dialoglodziņā tiek rādīts saraksts ar laukiem, kas saistīti ar atlasīto grupu vai apgabalu. Šajā dialoglodziņā atlasiet vienu vai vairākus laukus, ko pievienot, un pēc tam atlasiet **Ievietot**. Lai noņemtu kādu lauku, ko iepriekš pievienojāt, atkārtojiet šo procesu, bet dialoglodziņā noņemiet attiecīgā lauka atlasi.
- Izmantojiet rīku **Pārvietot**, lai pārvietotu kādu elementu uz citu atrašanās vietu pašreizējā elementu grupā. Ņemiet vērā, ka jūs nevarat pārvietot elementu ārpus tā pamata grupas. Lai izmantotu šo rīku, rīkjoslā atlasiet pogu **Pārvietot** un pēc tam atlasiet elementu, kuru vēlāties pārvietot. Kad atlasāt kādu elementu, programma nosaka novietojumus, kur šo elementu var pārvietot. Šie novietojumi ir zināmi kā *nomešanas zonas*. Kad šo elementu velkat pa pašreizējo grupu, katra nomešanas zona tiek rādīta kā iekrāsota, trekna līnija blakus apgabalam, kur šo elementu var nomest.
- Izmantojiet rīku **Izlaist**, lai izņemtu kādu elementu no lapas tastatūras tabulācijas secības. Kad uzdevumu joslā atlasāt pogu **Izlaist**, visi pašlaik izlaistie elementi tiek rādīti ēnotā konteinerā. Varat interaktīvi noņemt vai pievienot laukus ciļņu secībai.
- Izmantojiet rīku **Rādīt galvenē**, kad vēlaties, lai lauks tiktu rādīts kopsavilkuma cilnes kopsavilkuma sadaļā. Kad uzdevumu joslā atlasāt pogu **Rādīt galvenē**, visi lauki, kas ir atlasīti kā kopsavilkuma lauki, tiek radīti ēnotā konteinerā. Atlasot laukus, varat interaktīvi pievienot laukus kopsavilkuma cilnes kopsavilkumam un noņemt laukus no tā.
- Izmantojiet rīku **Bloķēt**, lai kādu elementu atzīmētu kā rediģējamu vai nerediģējamu. Kad uzdevumu joslā atlasāt pogu **Bloķēt**, visi pašlaik nerediģējami elementi tiek rādīti ēnotā konteinerā. Pēc tam varat tos atkal padarīt par rediģējamiem. Ņemiet vērā, ka daži lauki ir obligāti un tos nevar padarīt nerediģējamus Pie šiem laukiem tiek rādīts piekaramās slēdzenes simbols.
- Izmantojiet pogu **Pievienot programmu no Power Apps** lai lapā iegultu programmu, kura ir izveidota, izmantojot Microsoft Power Apps. Plašāku informāciju par to, kā lapā iegult programmu no Power Apps, skatiet tēmā [Iegult programmas no Power Apps](embed-power-apps.md). Šī opcija ir pieejama tikai tad, ja ir atspējots līdzeklis [Saglabātie skati](saved-views.md).  
- Izmantojiet pogu**Pievienot programmu**, lai lapā iegultu programmu – vai nu to, kas izveidota no Microsoft Power Apps vai trešās puses. Šī opcija ir pieejama tikai tad, ja ir iespējots līdzeklis [Saglabātie skati](saved-views.md). 
- Izmantojiet rīku **Notīrīt**, lai lapai atiestatītu noklusējuma instalēto stāvokli. Tādējādi tiek noņemti visas pašreizējās lapas personalizēšanas iestatījumi. Šo darbību nevar atsaukt. Tādēļ šo rīku ir jāizmanto tikai tad, ja esat pārliecināts, ka vēlaties lapu atiestatīt.
- Izmantojiet rīku **Importēt**, lai ielādētu personalizēšanu no kāda faila, kuru iepriekš izveidojāt jūs pats vai kāds cits. Kad importējat lapu personalizācijas, varat izvēlēties, vai tās ir jāpievieno visām lapas esošajām personalizācijām vai jāaizstāj ar tām. Šo darbību nevar atsaukt. Tāpēc pēc personalizācijas importēšanas manuāli jānotīra vai jāatsauc nevēlamās izmaiņas.
- Izmantojiet rīku **Eksportēt**, lai savas personalizācijas šai lapai saglabātu kādā failā. Pēc tam savas personalizācijas varat koplietot ar citiem lietotājiem. Šiem lietotājiem ir nepieciešams tikai importēt failu, kurā ir jūsu personalizācijas šai lapai.
- Atlasiet pogu **Aizvērt**, lai rīkjoslu **Personalizēšana** aizvērtu un lapu atgrieztu tās iepriekšējā interaktīvajā stāvoklī.

Tradicionāli, kad tiek izmantota rīkjosla **Personalizēšana**, jūsu personalizācijas stājas spēkā, tiklīdz tos izdarāt. Tomēr, ja ir ieslēgts līdzeklis [Saglabātie skati](saved-views.md), jums ir viennozīmīgi jāsaglabā personalizācijas jūsu izvēlētajam skatam.

Dažreiz, kad atlasāt kādu rīku, blakus kādam elementam tiek rādīts piekaramās slēdzenes simbols. Šis simbols norāda, ka nevarat modificēt šī elementa rekvizītus, kas ir saistīti ar atlasīto rīku, jo šo rekvizītu izmaiņas neļaus lapai darboties pareizi.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Elementa, saraksta vai saites uz darbvietu pievienošana

Dažām lapām, kurās ir ietverti saraksti, personalizēšanas līdzeklis **Pievienot darbvietai** ir pieejams grupā **Personalizēt** darbības rūts cilnē **Opcijas**. Izmantojot šo līdzekli, jūs varat no pašreizējā saraksta pārvietot atbilstošo informāciju uz noteiktu darbvietu. Informācija, kas parādās darbvietā, var tikt balstīta vai nu uz visu sarakstu, vai arī uz saraksta filtrēto un sašķiroto versiju. Var arī norādīt, vai informācija darbvietā tiek rādīta kā saraksts, kopsavilkuma elements, kurā var rādīt sarakstā esošo elementu skaitu, vai kā saite.

> [!NOTE]
> Ja ir ieslēgts līdzeklis [Saglabātie skati](saved-views.md), saturs, ko virzāt uz darbvietu, ir tieši saistīts ar skatu. Skatījuma vaicājums tiek izmantots, lai ienestu datus darbvietā, un atbilstošais elements vai saite darbvietā atver lapu šim skatam, lai tam tiktu piemērots skata vaicājums un personalizācijas.

[![Pievienot darbvietai](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Lai darbvietai pievienotu kādu sarakstu, vispirms kārtojiet vai filtrējiet lapā esošo sarakstu, lai informācija tajā tiktu rādīta tā, kā to vēlaties rādīt darbvietā. (Ja ir ieslēgts līdzeklis Saglabātie skati, nevar turpināt darbu, kamēr nav saglabāts skats, kam ir šie nosacījumi.) Pēc tam atlasiet **Pievienot darbvietai**. Atlasiet darbvietu un pēc tam laukā **Prezentācija** atlasiet **Saraksts**. Kad atlasāt vienumu **Konfigurēt**, tiek parādīts dialoglodziņš, kur varat atlasīt kolonnas, kuras ir jārāda šīs darbvietas sarakstā. Varat arī norādīt etiķeti, kas ir izmantota sarakstam šajā darbvietā.
- Lai darbvietai pievienotu kādu elementu, vispirms filtrējiet lapā esošo sarakstu, lai tajā būtu redzami dati, kurus vajag apkopot vai kuriem vēlaties ātri piekļūt. (Ja ir ieslēgts līdzeklis Saglabātie skati, nevar turpināt darbu, kamēr nav saglabāts skats, kam ir šie nosacījumi.) Pēc tam atlasiet **Pievienot darbvietai**. Atlasiet darbvietu un pēc tam laukā **Prezentācija** atlasiet **Elements**. Kad ir atlasīts vienums **Konfigurēt**, tiek paradīts dialoglodziņš, kur varat norādīt etiķeti, kuru ir jāizmanto elementam šajā darbvietā. Var arī norādīt, vai elementam ir jārāda skaits. Pēc tam, kad elements ir pievienots darbvietai, varat to atlasīt, lai atvērtu pašreizējo lapu no darbvietas. Pēc tam varat apskatīt filtrēto sarakstu, kas ir saistīts ar elementu.
- Lai pievienotu saiti uz darbvietu, vispirms filtrējiet lapā esošo sarakstu tā, lai tajā būtu redzami jums interesējošie dati. (Ja ir ieslēgts līdzeklis Saglabātie skati, nevar turpināt darbu, kamēr nav saglabāts skats, kam ir šie nosacījumi.) Pēc tam atlasiet **Pievienot darbvietai**. Atlasiet darbvietu un pēc tam laukā **Prezentācija** atlasiet **Saite**. Kad ir atlasīts vienums **Konfigurēt**, tiek paradīts dialoglodziņš, kur varat norādīt etiķeti, kuru ir jāizmanto šai saitei. Pēc izvēles varat arī norādīt etiķeti jaunai sadaļai, kurā ir šī saite.

Kad jūs pievienojat sarakstu, elementu vai saiti darbvietai, varat atvērt šo darbvietu un mainīt tajā elementu secību, ja vēlaties.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Kopsavilkuma pievienošana no darbvietas informācijas panelim

Dažās darbvietās ir skaita elementi (t.i., elementi, kuros ir skaitļi), un jūs varētu vēlēties šos elementus rādīt arī savā informācijas panelī. Darbvietā ar peles labo pogu noklikšķiniet uz skaita elementa, atlasiet **Personalizēt** un pēc tam elementa rekvizīta logā atlasiet **Piespraust informācijas panelim**. Tad, kad nākamajā reizē, kad atverat un atsvaidzināt atlasīto informācijas paneli, šis skaits tiek rādīts zem attiecīgās darbvietas navigācijas elementa. Varat atlasīt, lai šis skaits tieši novirzītu uz datiem, kurus tas attēlo.

### <a name="personalizing-your-dashboard"></a>Sava informācijas paneļa personalizēšana

Informācijas panelis bieži vien ir pirmā lapa, ko redzat, atverot programmu. Informācijas paneli varat personalizēt tā, lai tajā tiktu rādīti vienīgi darbvietas elementi, kurus vēlaties redzēt. Varat arī pārkārtot elementus, lai tie parādās tādā secībā, kādā tos vēlaties redzēt, varat pārdēvēt darbvietas navigācijas elementus vai pievienot jaunu darbvietas elementu.

Lai personalizētu informācijas paneli, ar peles labo pogu noklikšķiniet uz jebkura elementa un pēc tam atlasiet **Personalizēt**, lai atvērtu elementa rekvizītu logu.

- Ja vēlaties slēpt vai pārdēvēt atlasīto elementu, izmaiņas varat veikt tieši rekvizītu logā.
- Lai pārkārtotu darbvietas elementus, rekvizītu logā atlasiet **Personalizēt šo lapu**, tādējādi atverot rīkjoslu **Personalizēšana**. Pēc tam varat izmantot rīku **Pārvietot**, lai elementus pārkārtotu pēc vēlēšanās.
- Lai pievienotu jaunu darbvietas elementu, rekvizītu logā atlasiet vienumu **Pievienot darbvietu**. Informācijas paneļa apakšā tiek izveidots jauns darbvietas elements. Šo jauno darbvietas elementu pēc vēlēšanās varat pārdēvēt. Sarakstus, elementus un saites darbvietai varat arī pievienot, kā aprakstīts šīs tēmas sadaļā [Sarakstu, elementu vai saišu pievienošana darbvietām](#adding-a-tile-list-or-link-to-a-workspace).

## <a name="administration-of-personalizations"></a>Personalizāciju administrēšana

Pēc lapas personalizēšanas savas personalizācijas varat kopīgot ar citiem lietotājiem, eksportējot personalizēto lapu. Pēc tam varat lūgt citiem lietotājiem atvērt personalizēto lapu un importēt jūsu izveidoto personalizēšanas failu. Vai arī savu personalizāciju failu varat iedot kādam lietotājam, kuram ir administratora privilēģijas. Pēc tam šis lietotājs var izmantot jūsu personalizēšanas failu vairākiem lietotājiem vienlaikus.

Lietotāji ar administratora privilēģijām var arī pārvaldīt personalizācijas citiem lietotājiem lapā **Personalizēšana**.

Klientiem, kuri neieslēdza [Saglabāti skati](saved-views.md) līdzeklī, šai lapai ir četras cilnes:

- **Lietot** – varat importēt vai atlasīt kādu personalizāciju vienam vai vairākiem lietotājiem. Lai personalizāciju lietotu vienam lietotājam vai vairākiem, vispirms atlasiet kādu lomu un lietotājus, kuriem ir šī loma. Pēc tam atlasiet esošu personalizāciju, kuru lietot atlasītajiem lietotājiem, vai importējiet personalizēšanas failu. Personalizācija tiek validēta un tiek lietota visiem atlasītajiem lietotājiem nākamajā reizē, kad viņi atver atlasīto lapu.
- **Notīrīt** – varat notīrīt visas lapai vai darbvietai paredzētās personalizācijas vienam vai vairākiem lietotājiem. Vispirms atlasiet lapu vai darbvietu, lai redzētu sarakstu ar lietotājiem, kuri to ir personalizējuši. Pēc tam atlasiet lietotājus, kuriem ir nepieciešams notīrīt šīs lapas vai darbvietas personalizācijas, un atlasiet **Notīrīt**. Tiek dzēstas visas personalizācijas, ko atlasītie lietotāji ir lietojuši atlasītajai lapai vai darbvietai. Šo darbību nevar atsaukt. Taču, ja šai lapai vai darbvietai bija saglabāta kāda personalizācija, šo personalizāciju var importēt vēlreiz.
- **Lietotāji** – Atlasiet lietotāju, lai redzētu sarakstu ar lapām, ko lietotājs ir personalizējis. Pēc tam varat ieslēgt vai izslēgt lietotāja spēju lietot personalizācijas konkrētām lapām vai visai sistēmai. Varat arī importēt, eksportēt vai notīrīt personalizēšanu lietotājam. Turklāt varat atiestatīt līdzekļa remarkas lietotājam. Šādā gadījumā, ja lietotājs iepriekš noraidīja visus uznirstošos logus, kas ievies jaunus līdzekļus, tie atkal parādīsies nākamajā reizē, kad lietotājs sastop šos līdzekļus.
- **Sistēma** – Jūs varat īslaicīgi izslēgt personalizēšanu visiem lietotājiem sistēmā. Šādā gadījumā visi personalizācijas tiek dzēsti visiem lietotājiem, un visas lapas tiek atiestatītas uz noklusējuma statusu. Ja vēlāk personalizēšanu atkal ieslēdzat, visas personalizācijas ir atkal lietotas. Varat arī neatgriezeniski dzēst visas personalizācijas visiem lietotājiem sistēmā. Personalizācijas, kas tika izdzēstas, nav iespējams atgūt. Tādēļ, pirms veicat šo uzdevumu, noteikti eksportējiet visas personalizācijas, kuras vēlāk varētu būt nepieciešams.

Klientiem, kuri ieslēdza [Saglabāti skati](saved-views.md) līdzeklī, **Personalizēšana** lapai ir piecas cilnes:

- **Publicētie skati** – Šie skati tika publicēti jūsu organizācijā. Lai mainītu lietotājus, uz kuriem attiecas šie skati, varat mainīt drošības lomas vai juridiskās personas, kas ir saistītas ar katru skatu. Varat arī eksportēt vai dzēst vienu vai vairākus publicētus skatus.
- **Nepublicētie skati** – Šie skati ir veidnes skati, kas tika importēti jūsu sistēmā, bet vēl netika publicēti. Jūs varat publicēt, eksportēt vai dzēst šos skatus.
- **Personiskie skati** – Šie skati ir sistēmas lietotāju izveidoti. Jūs varat publicēt personisku skatu organizācijai vai kopēt vienu vai vairākus no šiem skatiem citiem lietotājiem. Jūs arī varat eksportēt vai dzēst šos skatus, ja nepieciešams.
- **Lietotāji** – Atlasiet lietotāju, lai redzētu sarakstu ar lapām, ko lietotājs ir personalizējis. Pēc tam varat ieslēgt vai izslēgt lietotāja spēju lietot personalizācijas konkrētām lapām vai visai sistēmai. Varat arī importēt, eksportēt vai notīrīt personalizēšanu lietotājam. Turklāt varat atiestatīt līdzekļa remarkas lietotājam. Šādā gadījumā, ja lietotājs iepriekš noraidīja visus uznirstošos logus, kas ievies jaunus līdzekļus, tie atkal parādīsies nākamajā reizē, kad lietotājs sastop šos līdzekļus.
- **Sistēma** – Jūs varat īslaicīgi izslēgt personalizēšanu visiem lietotājiem sistēmā. Šādā gadījumā visi personalizācijas tiek dzēsti visiem lietotājiem, un visas lapas tiek atiestatītas uz noklusējuma statusu. Ja vēlāk personalizēšanu atkal ieslēdzat, visas personalizācijas ir atkal lietotas. Varat arī neatgriezeniski dzēst visas personalizācijas visiem lietotājiem sistēmā. Personalizācijas, kas tika izdzēstas, nav iespējams atgūt. Tādēļ, pirms veicat šo uzdevumu, noteikti eksportējiet visas personalizācijas, kuras vēlāk varētu būt nepieciešams.

Lietotāji, kuriem ir piekļuve **Personalizēšana** lapai, var arī importēt personiskos vai veidņu skatus, izmantojot pogu **Importēt skatus** darbības rūtī.

## <a name="personalizing-inventory-dimensions"></a>Krājumu dimensiju personalizēšana.

Kad personalizējat krājumu dimensiju iestatījumus lapā, ņemiet vērā iestatījumus, kas izveidoti, izmantojot opciju **Parādīt dimensijas**. Piemēram, jūs izmantojat personalizāciju, lai paslēptu kolonnu partijas numuru krājumu dimensijai, bet šī kolonna tiek rādīta nākamajā reizē, kad lapa tiek atvērta. Tā notiek, jo iestatījumi **Dimensiju rādīšana** kontrolē, kuras krājumu dimensiju kolonnas tiek rādītas. Iestatījumi **Dimensiju rādīšana** tiek lietoti visās lapās, un tiem ir prioritāte pār jebkādiem personalizētajiem krājumu dimensiju lauku iestatījumiem atsevišķās lapās.

Tāpēc, tāpat kā iepriekšējā piemērā, ja nevēlaties, lai lapā tiek parādīta partijas numura krājumu dimensijas kolonna, ir jānoņem attiecīgās dimensijas atzīme konkrētās lapas opcijas **Parādīt dimensijas** ietvaros.
