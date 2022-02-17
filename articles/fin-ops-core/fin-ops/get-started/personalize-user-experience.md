---
title: Lietotāja pieredzes personalizēšana
description: Šajā tēmā ir paskaidrots, kā varat personalizēt programmu.
author: jasongre
ms.date: 01/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 840a68d506664043c9affb67e801429e0594f0bd
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075426"
---
# <a name="personalize-the-user-experience"></a>Lietotāja pieredzes personalizēšana

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šajā tēmā izskaidrots, kā varat personalizēt programmu, un ir aptvertas šādas tēmas: 

- **Visas sistēmas opcijas** — šīs personalizēšanas opcijas tiek veiktas iestatīšanas lapā un ir pieejamas visiem lietotājiem. Kā piemērus varētu minēt krāsu dizainu un laika joslu. 
- **Ierobežota personalizācijas piekļuve** – šajā piekļuves līmenī, lietotāja darbības, kas ir saistītas ar tipisku lapas lietojumu, tiek automātiski saglabātas, un tās tiek atjaunotas nākamreiz, kad apmeklējat lapu. Piemēram, programma saglabā režģa kolonnu platumu, ja tās koriģējat, kā arī kopsavilkuma ciļņu izvēršanas vai sakļaušanas stāvokli. 
- **Pilnīga personalizācijas piekļuve** – šajā piekļuves līmenī lietotājiem ir piekļuve visām programmas personalizācijas iespējām. Jo īpaši tām ir piekļuve **Personalizācijas** rīkjoslai. 
- **Personalizāciju kopīgošana** — lietotāji, kuriem ir pilna personalizācijas piekļuve, var eksportēt savu lapu personalizācijas un koplietot tās ar citiem lietotājiem.
- **Personalizāciju administrēšana** — Priviliģētie lietotāji var piekļūt **Personalizāciju** administrēšanas lapai, lai pārvaldītu visas personalizācijas organizācijas līmenī. 

## <a name="system-wide-options-for-the-current-user"></a>Sistēmas mēroga opcijas pašreizējam lietotājam

Lapā **Lietotāja opcijas** ir vairāki visas sistēmas mēroga iestatījumi pašreizējam lietotājam. Šīs opcijas ir pieejamas visiem lietotājiem, pat lietotājiem, kuriem nav piešķirta nekāda piekļuve personalizācijai. Lai atvērtu lapu **Lietotāja opcijas**, navigācijas joslā atlasiet pogu **Iestatījumi** un pēc tam atlasiet **Lietotāja opcijas**. Lapā **Lietotāja opcijas** ir četras cilnes, kurās ir dažādi tālāk aprakstītie lietotāja iestatījumi.

- **Vizuāls** – atlasiet lapu krāsu dizainu un elementu noklusējuma izmēru.
- **Preferences**— atlasiet noklusējuma vērtības, kas tiek izmantotas katru reizi, kad atverat sistēmu. Šīs vērtības ietver noklusējuma uzņēmumu, sākuma lapu un noklusējuma skata/rediģēšanas režīmu. (Skata/rediģēšanas režīms nosaka, vai katru reizi, kad lapu atverat, lapa ir bloķēta un to var tikai apskatīt, vai lapa ir atvērta rediģēšanai.) Šajā cilnē ir arī opcijas valodai, laika joslai un datuma, laika un skaitļu formātiem. Visbeidzot šajā cilnē ir dažādas preferences, kas dažādos laidienos ir atšķirīgas.
- **Konts** – skatiet vai pielāgojiet savu lietotājvārdu un citas ar kontu saistītas opcijas.
- **Darbplūsma** – atlasiet ar darbplūsmu saistītas opcijas.

Papildus lietotāja iestatījumu mainīšanai var arī skatīt vai izdzēst lietojuma un personalizācijas datus no **Lietojuma datu** lapas. Lai skatītu lietojuma datus, atlasiet **Lietojuma dati** darbības rūtī. Cilnē **Personalizēšana** jūs varat skatīt un pārvaldīt izmaiņas, kuras personīgi veiktas sistēmas lapās. Šajā cilnē var arī atiestatīt līdzekli remarkas (tas ir, uznirstošos logus, kas ievieš jaunus sistēmas līdzekļus). Pēc tam tiks parādīts brīdinājums par iepriekš konstatētajiem līdzekļiem.

> [!NOTE]
> Ja ir ieslēgts līdzeklis [Saglabātie skati](saved-views.md), varat skatīt un pārvaldīt jūsu personalizācijas, atlasot **Personalizācijas** darbības rūtī **Lietotāja opcijas**.

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Ierobežota personalizācijas piekļuve (iepriekš netieši personalizācijas)

**Ierobežota personalizācijas piekļuve** līmenī lietotāja darbības, kas ir saistītas ar tipisku lapas lietojumu, tiek automātiski saglabātas, un tās tiek atjaunotas nākamreiz, kad apmeklējat lapu. Nav nepieciešama tieša saglabāšanas darbība. 

Šeit ir saraksts ar darbībām, kas atbilst tipiskai lapas lietošanai un ir ietvertas ierobežotas personalizācijas piekļuvē: 

- **Režģa kolonnas platums** – varat pielāgot režģī rādīto kolonnu platumu, atlasot izmēra maiņas joslu pa kreisi vai pa labi no kolonnas virsraksta un pēc tam bīdot to pa kreisi vai pa labi, līdz kolonna ir nepieciešamajā platumā. Programma saglabā platumu, ko iestatāt kolonnai. Nākamreiz, atverot lapu, kolonnas lielums tiks mainīts līdz tādam platumam.
- **Režģa kājenes un kolonnu kopsumma** — *(Pieejams tikai, kad ir iespējots jaunā režģa kontrole)* Jūs varat izlemt, vai kopsumma ir jāparāda jebkuras skaitliskas kolonnas apakšpusē, un to, vai ir redzama režģa kājene. Programma saglabā šos datus un pielieto tos nākamreiz , kad atverat lapu. Plašāku informāciju skatiet sadaļā [Režģa iespējas](grid-capabilities.md). 
- **Kopsavilkuma cilnes** – dažām lapām ir izvēršamas sadaļas, kas tiek sauktas par *kopsavilkuma cilnēm*. Programma glabā informāciju par kopsavilkuma cilnēm, kuras esat izvērsis vai sakļāvis. Nākamreiz, kad jūs atvērsit šo lapu, būs izvērstas vai sakļautas tās pašas kopsavilkuma cilnes, ņemot vērā jūsu pēdējo mijiedarbību ar šo lapu. Reizēm jūs varat palīdzēt uzlabot sistēmas veiktspēju, sakļaujot kādu kopsavilkuma cilni, jo programmai nav jāizgūst informācija par šo kopsavilkuma cilni, kamēr tā nav izvērsta. Kā šajā tēmā ir paskaidrots tālāk, varat mainīt arī kopsavilkuma ciļņu secību lapā.
- **Papildinformācijas lodziņi** – Dažām lapām ir rūts **Saistīta informācija**, kurā ir parādīta tikai lasāma informācija, kas saistīta ar pašreizējo lapas tēmu. Katru sadaļu rūtī **Saistīta informācija** sauc par *Papildinformācijas lodziņš*. Varat izvērst vai sakļaut rūti **Saistīta informācija**, kā arī varat izvērst vai sakļaut atsevišķus papildinformācijas lodziņus. Programma saglabā šīs preferences. Nākamreiz, kad atverat šo lapu, tiek izvērsta vai sakļauta rūts **Saistīta informācija** un atsevišķo papildinformācijas lodziņu stāvoklis, ņemot vērā jūsu pēdējo mijiedarbību ar šo lapu. Reizēm jūs varat palīdzēt uzlabot sistēmas veiktspēju, sakļaujot kādu **Saistītās informācijas** rūti vai papildinformācijas lodziņu, jo programmai nav jāizgūst informācija par šiem Papildinformācijas lodziņiem, kamēr tā nav izvērsta.
- **Darbību rūtis** – vairumā lapu *darbību rūts* tiek rādīta lapas augšdaļā. Darbību rūtī ir pogas daudzām darbībām, ko pašreizējā lapā varat veikt. Bieži vien šīs pogas ir sakārtotas cilnēs. Varat *piespraust* visu darbību rūti atvērtā veidā, vai arī norādīt, ka pēc noklusējuma tai ir jābūt sakļautai. Nākamreiz, kad jūs atvērsit šo lapu, būs atvērtas vai sakļautas Darbības rūtis, ņemot vērā jūsu pēdējo mijiedarbību ar šo lapu. Ja jūs piespraudāt darbības rūti atvērtā veidā, tiks rādīta pēdējā cilne, kuru izmantojāt.
- **Ātrie filtri** – *ātrais filtrs* tiek rādīts virs daudziem režģiem. Ar ātro filtru varat filtrēt režģi, pamatojoties uz vienu jūsu atlasīto kolonnu. Programma saglabā kolonnu, pēc kuras veicāt filtrēšanu. Pēc tam nākamajā reizē, kad atverat lapu, šis režģis izmantos to pašu kolonnu, lai filtrētu pēc noklusējuma. Taču pēc tam joprojām varat izvēlēties citu kolonnu, lai filtrētu šo režģi.
- **Kolonnu virsrakstu filtri** – kad filtrējat režģi, izmantojot *kolonnu virsrakstu filtri*, pēc nepieciešamības varat mainīt filtra operatoru, lai atrastu jums nepieciešamos datus. Varat, piemēram, operatoru no **sākas ar** mainīt uz **ir precīzi**. Katru reizi, kad izmantojat kādu kolonnu virsrakstu filtru un maināt filtra operatoru, programma saglabā šīs izmaiņas. Pēc tam programma atjaunos filtra operatoru nākamajā reizē, kad filtrējat pēc šīs kolonnas.
- **Navigācijas rūts** – Varat atvērt *navigācijas rūti*, jebkuras lapas augšējā kreisajā rūtī atlasot pogu **Izvērsiet navigācijas rūti**. (Šī poga reizēm tiek saukta par _**Izvēlnes** pogu_, *hamburgeru*, *hamburgera izvēlni* vai *hamburgera pogu*.) Navigācijas rūti varat piespraust atvērtā veidā, vai arī norādīt, ka pēc noklusējuma tai ir jābūt sakļautai. Pēc tam, kad navigācijas rūti piespraužat atvērtā veidā, programma saglabā to atvērtu, līdz šo rūti sakļaujat.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Pilnās personalizācijas piekļuve (iepriekš skaidri izteiktas personalizācijas)

**Pilnīga personalizācijas piekļuve** līmenī lietotājiem ir piekļuve visām programmas personalizācijas iespējām. Tā kā dažādiem cilvēkiem un uzņēmumiem ir dažādas vajadzības, kad tie mijiedarbojas ar programmu, it īpaši attiecībā uz izmantotajiem laukiem, personalizācija nodrošina rīkus, kas ļauj lietotājiem un organizācijām pielāgot veidu, kādā informācija tiek padarīta un mijiedarboties programmā. Šīs iespējas ir būtiskas, lai nodrošinātu vienkāršotu, optimizētu pieredzi programmā, kas ir pielāgota jums un jūsu organizācijai. 

Ja ir ieslēgts līdzeklis [Saglabātie skati](saved-views.md), lai saglabātu šīs izmaiņas lietotāja pieredzē konkrētam skatam, ir nepieciešama skaidra saglabāšana. Kad opcija **Saglabātie skati** ir izslēgta, šīs izmaiņas tiek automātiski saglabātas.

Tālāk norādītās sadaļas aptver personalizēšanas iespēju apjomu, kas ir pieejams lietotājiem **pilnīgas personalizēšanas piekļuves** līmenī. Tālāk ir norādītas dažas no šīm iespējām:

- Saīšņu izvēlnes opcijas
- **Personalizēšanas** rīkjosla
- Pievieno elementus, sarakstus un saites uz darbvietām
- Kopsavilkuma pievienošana no darbvietas informācijas panelim
- Informācijas paneļa personalizēšana

### <a name="shortcut-menu-options"></a>Saīšņu izvēlnes opcijas

Saīšņu izvēlne sniedz vienu veidu, kā tieši mainīt lapas interfeisu, lai tā labāk atbilstu jūsu prasībām vai jūsu uzņēmuma prasībām. (Saīšņu izvēlne tiek saukta arī par *izvēlni, kas tiek parādīta, noklikšķinot ar peles labo pogu,* vai *kontekstizvēlni*.)

Dažas no tipiskākajām un svarīgākajām izmaiņām, ko lapai var veikt, ir tieši pieejamas kā opcijas saīšņu izvēlnē. Piemēram, ja vēlaties režģim pievienot vai slēpt kolonnas, vienkārši noklikšķiniet ar peles labo pogu uz kolonnas virsraksta un pēc tam atlasiet **Ievietot kolonnas** vai **Slēpt šo kolonnu**.

Turklāt visparastākie personalizēšanas tipi ir pieejami, noklikšķinot ar peles labo pogu uz kāda elementa un pēc tam atlasot **Personalizēt**. (Ņemiet vērā, ka ne visus lapā esošos elementus var personalizēt.) Izmantojot šo personalizēšanas metodi, tiek parādīts elementa *rekvizītu logs*.

![Elementa rekvizītu personalizēšana.](./media/cli-element-property-window.png)

Rekvizītu logu varat izmantot, lai personalizētu kādu elementu tālāk norādītajos veidos.

- Mainīt elementa etiķeti.
- Paslēpt elementu, lai lapā tas nebūtu redzams. Šajā laukā esošie dati netiek dzēsti vai modificēti. Informācija vienkārši vairs netiek rādīta lapā.
- Ietvert informāciju kopsavilkuma cilnes kopsavilkuma sadaļā (ja elements atrodas kopsavilkuma cilnē).
- Izlaist lauku, lai tas nekad nebūtu fokusā, kad tiek ritināta lapa.
- Novērst šajā laukā esošo datu rediģēšanu (jebkuram ierakstam)
- Norādiet lauku, kas nepieciešams datu ievadei. Ja šajā laukā nav ievadīta neviena vērtība, tā tiek parādīta ar sarkanu apmali un zvaigznīti, lai norādītu šo stāvokli. Šī opcija ir pieejama tikai tad, ja ir aktivizēta versija 10.0.11, kad līdzekļi [Saglabātie skati](saved-views.md) un **Norādīt laukus kā obligātus, izmantojot personalizāciju** ir ieslēgti.

Atkarībā no elementa rekvizītu logā var būt citas personalizēšanas iespējas. Piemēram, elementa rekvizītu logā jums varētu būt iespējams attiecīgo elementu paaugstināt uz informācijas paneli, un šis rekvizītu logs noklusējuma informācijas paneļa elementiem varētu ļaut jums izveidot jaunu darbvietu.

### <a name="personalization-toolbar"></a>Personalizēšanas rīkjosla

Ja vēlaties lapā veikt vairākas izmaiņas vai izmaiņas, kuras nevar veikt, izmantojot citus mehānismus (piemēram, ja vēlāties pārkārtot elementus), var izmantot rīkjoslu **Personalizēšana**. Lai atvērtu **Personalizēšana** rīkjoslu, veiciet vienu no šīm darbībām:

- Atlasiet **CTRL+SHIFT+P** no jebkura elementa lapā.
- Atlasiet **Personalizēt šo lapu** elementa rekvizītu logā.
- Atlasiet **Personalizēt šo veidlapu** grupā **Personalizēt** cilnē **Opcijas** jebkuras lapas darbību panelī.
- Navigācijas joslā atlasiet pogu **Iestatījumi** (zobrata simbols) un pēc tam atlasiet **Personalizēt.**

[![Personalizēšanas rīkjosla.](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Pārvietošanās lapā

Kad rīkjosla **Personalizēšana** ir atvērta, pamatā esošā lapa ir tikai lasāma (citiem vārdiem, nevar rediģēt datus), bet tā joprojām ir interaktīva. Konkrēti, varat izvērst vai sakļaut rūti **Saistītā informācija**, pārslēgt cilnes un izvērst vai sakļaut sadaļas, tāpat kā parasti šīs darbības tiek veiktas lapā. Lai personalizēšana stātos spēkā sakļautajā sadaļā vai cilnē (piemēram, lai slēptu kopsavilkuma cilni), jums vienkārši jāizvēlas poga, kas tiek parādīta blakus tai sadaļai vai cilnei, ja uz tās pāriet, izmantojot tastatūru, vai novieto virs tās kursoru.

#### <a name="personalization-tools"></a>Personalizēšanas rīki

Rīkjoslā **Personalizēšana** ir pieejami tālāk uzskaitītie rīki.

- Izmantojiet rīku **Atlasīt**, lai atlasītu un mainītu elementa rekvizītus. Lai izmantotu šo rīku, rīkjoslā atlasiet pogu **Atlasīt** un pēc tam atlasiet vēlamo elementu. Elementa rekvizītu logs parādās, kur jūs varat mainīt jebkurus šī elementa rekvizītus. Šo procesu varat atkārtot citiem elementiem, kurus attiecīgajā lapā var personalizēt. Ņemiet vērā, ka daži personalizēšanas rekvizīti var nebūt pieejami dažos scenārijos. Piemēram, jūs nevarat bloķēt lauku, kas ir obligāts.
- Izmantojiet rīku **Paslēpt**, lai slēptu kādu elementu šajā lapā. Lai izmantotu šo rīku, rīkjoslā atlasiet pogu **Paslēpt** un pēc tam atlasiet elementu, kuru vēlāties paslēpt. Kad izmantojiet rīku **Paslēpt**, visi pašlaik paslēptie elementi kļūst redzami, bet tie tiek rādīti ēnotā konteinerā. Pēc tam jūs varat padarīt elementu redzamu, atlasot to. Lai apskatītu, kā lapa izskatīsies, kad elementi ir paslēpti, pārslēdzieties uz citu personalizēšanas rīku vai aizveriet personalizēšanas rīkjoslu.
- Pielietojiet rīku **Pievienot laukus**, lai pievienotu laukus savai lapai. Kad izmantojat šo rīku, varat pievienot tikai tādus laukus, kas ir daļa no lapas definīcijas. Informāciju par to, kā izveidot jaunus laukus, kuri nav daļa no pašreizējās lapas definīcijas, skatiet tēmā [Izveidot un strādāt ar pielāgotajiem laukiem](user-defined-fields.md). Kad uzdevumu joslā ir atlasīta poga **Pievienot laukus**, jums vispirms ir jāatlasa režģis vai sadaļa, kur vēlaties pievienot lauku. Dialoglodziņā tiek rādīts saraksts ar laukiem, kas saistīti ar atlasīto režģi vai sadaļu. Dialoglodziņā atlasiet vienu vai vairākus laukus, ko pievienot vai nu no saraksta **Ieteiktie lauki** vai **Visi lauki**. Pēc vēlamo lauku izvēles atlasiet **Atjaunināt**. Lai noņemtu kādu lauku, ko iepriekš pievienojāt, atkārtojiet šo procesu, bet dialoglodziņā noņemiet attiecīgā lauka atlasi.

    Saraksts **Ieteicamie lauki** parāda laukus, kurus iepriekš ir pievienojis cits jūsu organizācijas lietotājs. Šis lauku saraksts tiek atjaunināts, pamatojoties uz **Rekomendāciju pakešuzdevuma** periodiskuma biežumu. Līdzīga pieredze pastāv, pievienojot jaunus filtra laukus, izmantojot lapas filtra rūti.

- Izmantojiet rīku **Pārvietot**, lai pārvietotu kādu elementu uz citu atrašanās vietu pašreizējā elementu grupā. Ņemiet vērā, ka jūs nevarat pārvietot elementu ārpus tā pamata grupas. Lai izmantotu šo rīku, rīkjoslā atlasiet pogu **Pārvietot** un pēc tam atlasiet elementu, kuru vēlāties pārvietot. Kad atlasāt kādu elementu, programma nosaka novietojumus, kur šo elementu var pārvietot. Šie novietojumi ir zināmi kā *nomešanas zonas*. Kad šo elementu velkat pa pašreizējo grupu, katra nomešanas zona tiek rādīta kā iekrāsota, trekna līnija blakus apgabalam, kur šo elementu var nomest.
- Izmantojiet rīku **Izlaist**, lai izņemtu kādu elementu no lapas tastatūras tabulācijas secības. Kad uzdevumu joslā atlasāt pogu **Izlaist**, visi pašlaik izlaistie elementi tiek rādīti ēnotā konteinerā. Varat interaktīvi noņemt vai pievienot laukus ciļņu secībai.
- Izmantojiet rīku **Rādīt galvenē**, kad vēlaties, lai lauks tiktu rādīts kopsavilkuma cilnes kopsavilkuma sadaļā. Kad uzdevumu joslā atlasāt pogu **Rādīt galvenē**, visi lauki, kas ir atlasīti kā kopsavilkuma lauki, tiek radīti ēnotā konteinerā. Atlasot laukus, varat interaktīvi pievienot laukus kopsavilkuma cilnes kopsavilkumam un noņemt laukus no kopsavilkuma.
- Izmantojiet rīku **Pieprasīt**, lai norādītu elementu, kas nepieciešams datu ievadei. Kad uzdevumu joslā atlasāt pogu **Pieprasīt**, visi elementi, kas ir personalizēti, lai padarītu tos obligātus, tiek rādīti ēnotā konteinerā. Pēc tam tie vairs nav nepieciešami. Šī opcija ir pieejama tikai tad, ja ir aktivizēta versija 10.0.12 un jaunāka versija, kad līdzeklis **Norādīt laukus kā obligātus, izmantojot personalizāciju** ir ieslēgts.
- Izmantojiet rīku **Bloķēt**, lai kādu elementu atzīmētu kā rediģējamu vai nerediģējamu. Kad uzdevumu joslā atlasāt pogu **Bloķēt**, visi pašlaik nerediģējami elementi tiek rādīti ēnotā konteinerā. Pēc tam varat tos atkal padarīt par rediģējamiem. Ņemiet vērā, ka daži lauki ir obligāti un tos nevar padarīt nerediģējamus Pie šiem laukiem tiek rādīts piekaramās slēdzenes simbols.
- Izmantojiet rīku **Pievienot programmu no Power Apps** lai lapā iegultu programmu, kura ir izveidota, izmantojot Microsoft Power Apps. Plašāku informāciju par to, kā lapā iegult programmu no Power Apps, skatiet tēmā [Iegult programmas no Power Apps](embed-power-apps.md). Šī opcija ir pieejama tikai tad, ja ir izslēgts līdzeklis [Saglabātie skati](saved-views.md).
- Izmantojiet pogu **Pievienot programmu**, lai lapā iegultu programmu – vai nu to, kas izveidota no Microsoft Power Apps vai trešās puses. Šī opcija ir pieejama tikai tad, ja ir ieslēgts līdzeklis [Saglabātie skati](saved-views.md). 
- Izmantojiet rīku **Notīrīt**, lai lapai atiestatītu noklusējuma instalēto stāvokli. Tādējādi tiek noņemti visas pašreizējās lapas personalizēšanas iestatījumi. Šo darbību nevar atsaukt. Tādēļ šo rīku ir jāizmanto tikai tad, ja esat pārliecināts, ka vēlaties lapu atiestatīt. Kad līdzeklis **Saglabātie skati** ir ieslēgts, šis rīks notīra personalizācijas pašreizējam skatam.
- Izmantojiet rīku **Importēt**, lai ielādētu personalizēšanu no kāda faila, kuru iepriekš izveidojāt jūs pats vai kāds cits. 

    - Kad opcija **Saglabātie skati** ir izslēgta, varat izvēlēties, vai pievienot vai aizstāt savus esošos personalizācijas ar personalizācijām, kas tiek importētas lapā. Šo darbību nevar atsaukt. Tāpēc pēc personalizācijas importēšanas manuāli jānotīra vai jāatsauc nevēlamās izmaiņas.
    - Kad līdzeklis **Saglabātie skati** ir ieslēgts, importētās personalizācijas kļūs par lapas skatu. Ja skats jau pastāv, jums būs iespēja izlaist importēšanu, aizstāt pašreizējo skatu, kam ir tāds pats nosaukums, vai pārdēvēt importēto skatu.

- Izmantojiet rīku **Eksportēt**, lai savas personalizācijas šai lapai saglabātu kādā failā. Pēc tam savas personalizācijas varat koplietot ar citiem lietotājiem. Šiem lietotājiem ir nepieciešams tikai importēt failu, kurā ir jūsu personalizācijas šai lapai. Kad līdzeklis **Saglabātie skati** ir ieslēgts, šis rīks saglabā jūsu pašreizējo skatu failā koplietošanai.
- Atlasiet pogu **Aizvērt**, lai rīkjoslu **Personalizēšana** aizvērtu un lapu atgrieztu tās iepriekšējā interaktīvajā stāvoklī.

Tradicionāli, kad tiek izmantota rīkjosla **Personalizēšana**, jūsu personalizācijas stājas spēkā, tiklīdz tos izdarāt. Tomēr, ja ir ieslēgts līdzeklis [Saglabātie skati](saved-views.md), jums ir viennozīmīgi jāsaglabā personalizācijas jūsu izvēlētajam skatam.

Dažreiz, kad atlasāt kādu rīku, blakus kādam elementam tiek rādīts piekaramās slēdzenes simbols. Šis simbols norāda, ka nevarat modificēt šī elementa rekvizītus, kas ir saistīti ar atlasīto rīku, jo šo rekvizītu izmaiņas neļaus lapai darboties pareizi.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Pievieno elementus, sarakstus un saites uz darbvietu

Dažām lapām, kurās ir ietverti saraksti, personalizēšanas līdzeklis **Pievienot darbvietai** ir pieejams grupā **Personalizēt** darbības rūts cilnē **Opcijas**. Izmantojot šo līdzekli, jūs varat no pašreizējā saraksta pārvietot atbilstošo informāciju uz noteiktu darbvietu. Informācija, kas parādās darbvietā, var tikt balstīta vai nu uz visu sarakstu, vai arī uz saraksta filtrēto un sašķiroto versiju. Var arī norādīt, vai informācija darbvietā tiek rādīta kā saraksts, kopsavilkuma elements, kurā var rādīt sarakstā esošo elementu skaitu, vai kā saite.

> [!NOTE]
> Ja ir ieslēgts līdzeklis [Saglabātie skati](saved-views.md), saturs, ko virzāt uz darbvietu, ir tieši saistīts ar skatu. Skatījuma vaicājums tiek izmantots, lai atgūtu datus darbvietā, un atbilstošais elements vai saite darbvietā atver lapu šim skatam, lai tam tiktu piemērots skata vaicājums un personalizācijas. Ja skats tiek atjaunināts, atbilstošie darbvietas elementi tiks pielāgoti jaunajai skata definīcijai.

[![Pievienot darbvietai.](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Lai darbvietai pievienotu kādu sarakstu, vispirms kārtojiet vai filtrējiet lapā esošo sarakstu, lai informācija tajā tiktu rādīta tā, kā to vēlaties rādīt darbvietā. (Ja ir ieslēgts līdzeklis **Saglabātie skati**, nevar turpināt darbu, kamēr nav saglabāts skats, kam ir šie nosacījumi.) Pēc tam atlasiet **Pievienot darbvietai**. Atlasiet darbvietu un pēc tam laukā **Prezentācija** atlasiet **Saraksts**. Kad atlasāt vienumu **Konfigurēt**, tiek parādīts dialoglodziņš, kur varat atlasīt kolonnas, kuras ir jārāda šīs darbvietas sarakstā. Varat arī norādīt etiķeti, kas ir izmantota sarakstam šajā darbvietā.
- Lai darbvietai pievienotu kādu elementu, vispirms filtrējiet lapā esošo sarakstu, lai tajā būtu redzami dati, kurus vajag apkopot vai kuriem vēlaties ātri piekļūt. (Ja ir ieslēgts līdzeklis **Saglabātie skati**, nevar turpināt darbu, kamēr nav saglabāts skats, kam ir šie nosacījumi.) Pēc tam atlasiet **Pievienot darbvietai**. Atlasiet darbvietu un pēc tam laukā **Prezentācija** atlasiet **Elements**. Kad ir atlasīts vienums **Konfigurēt**, tiek paradīts dialoglodziņš, kur varat norādīt etiķeti, kuru ir jāizmanto elementam šajā darbvietā. Var arī norādīt, vai elementam ir jārāda skaits. Pēc tam, kad elements ir pievienots darbvietai, varat to atlasīt, lai atvērtu pašreizējo lapu no darbvietas. Pēc tam varat apskatīt filtrēto sarakstu, kas ir saistīts ar elementu.
- Lai pievienotu saiti uz darbvietu, vispirms filtrējiet lapā esošo sarakstu tā, lai tajā būtu redzami jums interesējošie dati. (Ja ir ieslēgts līdzeklis **Saglabātie skati**, nevar turpināt darbu, kamēr nav saglabāts skats, kam ir šie nosacījumi.) Pēc tam atlasiet **Pievienot darbvietai**. Atlasiet darbvietu un pēc tam laukā **Prezentācija** atlasiet **Saite**. Kad ir atlasīts vienums **Konfigurēt**, tiek paradīts dialoglodziņš, kur varat norādīt etiķeti, kuru ir jāizmanto šai saitei. Varat arī pēc izvēles norādīt etiķeti sadaļai, kurā var ievietot šo saiti. Ja šīs sadaļas nav, tiks izveidota jauna sadaļa.

> [!NOTE]
> Sākot ar versiju 10.0.25, konfigurējot sarakstu, elementu vai saiti, iespējams, būs jāatlasa arī darbvietas skati, kuriem vēlaties pievienot elementu, ja **(Priekšskatījums) Saglabāto skatu atbalsts darbvietām** funkcija ir iespējota. Pieejamie darbvietas skati tiks parādīti mapē **Darbvietas iespējas** katra sadaļa **Konfigurēt** dialoglodziņš. 

Kad jūs pievienojat sarakstu, elementu vai saiti darbvietai, varat atvērt šo darbvietu un mainīt tajā elementu secību, ja vēlaties.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Kopsavilkuma pievienošana no darbvietas informācijas panelim

Dažās darbvietās ir skaita elementi (t.i., elementi, kuros ir skaitļi), un jūs varētu vēlēties šos elementus rādīt arī savā informācijas panelī. Darbvietā ar peles labo pogu noklikšķiniet uz skaita elementa, atlasiet **Personalizēt** un pēc tam elementa rekvizīta logā atlasiet **Piespraust informācijas panelim**. Nākamajā reizē, kad atverat (un atsvaidzināt) informācijas paneli, šis skaits tiek rādīts zem attiecīgās darbvietas navigācijas elementa. Varat atlasīt, lai šis skaits tieši novirzītu uz datiem, kurus tas attēlo.

### <a name="personalizing-your-dashboard"></a>Sava informācijas paneļa personalizēšana

Informācijas panelis bieži vien ir pirmā lapa, ko redzat, atverot programmu. To var personalizēt tāpat kā jebkuru citu lapu sistēmā, izmantojot tos pašus mehānismus, kas aprakstīti iepriekš šajā tēmā. 

> [!WARNING]
> Pašlaik, slēpjot saturu informācijas panelī, ir svarīgi tieši norādīt elementu, nevis ap to esošo atstarpi. Ja grupa tiek paslēpta ap elementu, var rasties negaidīti rezultāti, ja vēlāk tiek pievienoti papildu elementi vai ja sistēma ir pārslēgta uz citu valodu.

Viena unikāla personalizācijas iespēja, kas ir pieejama informācijas panelī, ir spēja pievienot elementus. 

- Ja ir izslēgta **Pilnas lappuses programmu** funkcija, jūs pievienojat jaunu elementu, ar peles labo pogu noklikšķinot uz elementa informācijas panelī un pēc tam atlasot **Pievienot darbvietu**. Informācijas paneļa apakšā tiek izveidots jauns darbvietas elements. Šo jauno darbvietas elementu pēc vēlēšanās varat pārdēvēt. Sarakstus, elementus un saites darbvietai varat arī pievienot, kā aprakstīts šīs tēmas sadaļā [Sarakstu, elementu vai saišu pievienošana darbvietai](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace).
- Ja ir ieslēgta **Pilnas lappuses programmu** funkcija, jūs pievienojat jaunu elementu, ar peles labo pogu noklikšķinot uz elementa informācijas panelī un pēc tam atlasot **Pievienot programmu**. Dialoglodziņā izvēlieties, vai vēlaties pievienot elementu jaunai darbvietai vai elementu, kurā ir saturs no Power Apps vai vietnes. Pēc tam veiciet norādītās darbības, lai konfigurētu izvēlēto opciju. Informācijas paneļa apakšā tiek izveidots jauns elements. Papildinformāciju par to, kā pievienot, rediģēt, dzēst un koplietot šīs iegultās lietojumprogrammas, skatiet sadaļā [Iegult pamatnes programmas no Power Apps](embed-power-apps.md) un [Iegult trešās puses programmas](embed-website.md).

## <a name="sharing-personalizations"></a>Personalizāciju koplietošana

Pēc lapas personalizēšanas ir dažas metodes, kuras var izmantot, lai kopīgotu personalizējumus ar citiem lietotājiem. Šajā sarakstā metodes ir sakārtotas secībā no visieteicamākās līdz vismazāk ieteicamajai.

1. Publicēt skatus lietotājiem.
2. Kopējiet skatus vai personalizēšanas lietotājiem.
3. Eksportēt un importēt skatījumus vai personalizēšanas.

### <a name="publish-views-to-users"></a>Publicēt skatus lietotājiem

Ja līdzeklis [Saglabātie skati](saved-views.md) ir ieslēgts un ja lapa atbalsta skatus, labākais veids, kā kopīgot personalizēšanas ar citiem lietotājiem, ir publicēt šo skatu lietotājiem, kuriem ir viena vai vairākas drošības lomas. Papildinformāciju skatiet sadaļā [Skatu publicēšana](saved-views.md#publishing-views).

### <a name="copy-views-or-personalizations-to-users"></a>Kopējiet skatus vai personalizēšanas lietotājiem

Ja līdzeklis [Saglabātie skati](saved-views.md) ir izslēgts vai lapa neatbalsta skatus, ieteicamais personalizēšanas veids ir to kopēšana starp lietotājiem. Šī metode ir pieejama tikai priviliģētiem lietotājiem (piemēram, sistēmas administratoriem). Tomēr administratori var skatīt konkrētu lietotāja personalizēšanu sistēmā (ieskaitot lietotāja personisko skatu, ja ir iespējoti saglabātie skati) un kopēt konfigurāciju citiem lietotājiem.

Ja ir iespējoti saglabātie skati, izpildiet šīs darbības, lai kopētu personalizēšanas.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Personalizēšana**.
2. Veiciet šīs darbības, lai kopētu personiskos skatus:

    1. Atlasiet **Personiskos skatus**.
    2. Izvēlieties sarakstā vajadzīgos skatus.
    3. Atlasiet **Kopēt lietotājiem**.
    4. Atlasiet lietotājus, kuriem izplatīt skatus.

    Izpildiet šīs darbības, lai kopētu personalizēšanas lapās, kas neatbalsta skatus:

    1. Atlasiet **Lietotāja iestatījumi**.
    2. Atlasiet lietotāju, kuram ir personalizēšana, ko vēlaties izplatīt.
    3. Atlasiet **Pārvaldīt visas personalizēšanas**.
    4. Izvēlieties sarakstā nepieciešamās personalizācijas.
    5. Atlasiet **Kopēt lietotājiem**.
    6. Atlasiet lietotājus, kuriem izplatīt personalizācijas.

Ja ir iespējoti saglabātie skati, izpildiet šīs darbības, lai kopētu personalizēšanu.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Personalizēšana**.
2. Atlasiet **Lietot**.
3. Atlasiet lietotājus, kuriem izplatīt personalizāciju.
4. Atlasiet **Atlasīt esošu personalizēšanu**.
5. Atrodiet un atlasiet (vienreizējo) personalizāciju, kas jums interesē.
6. Atlasiet **Labi**.

### <a name="export-and-import-views-or-personalizations"></a>Eksportēt un importēt skatījumus vai personalizēšanas

Cits veids, kā koplietot personalizēšanas, ir caur eksportu un importu. Atsevišķi lietotāji vai administrators, kas darbojas viņu vārdā, var izmantot šo metodi, lai eksportētu viņu personalizēšanas vai skatus, un tad piešķirt eksportēto failu citiem lietotājiem importēšanai. Alternatīvi lietotāji var sniegt eksportētās personalizēšanas lietotājam, kam ir administratora privilēģijas, un šis lietotājs var izmantot **Personalizēšanas** administrēšanas lapu, lai pielietotu personalizēšanas failu daudziem lietotājiem vienlaicīgi.

> [!IMPORTANT]
> Tā kā personalizācija saglabājas visos atjauninājumos, visu personalizāciju atkārtota importēšana pēc pakalpojuma atjaunināšanas vai jebkurā citā laikā ir nevajadzīga un ļoti nevēlama.

#### <a name="export"></a>Eksports

Vispārīgā gadījumā varat eksportēt vienu no saviem skatiem vai personalizācijām, atverot atbilstošo lapu, atverot personalizēšanas rīkjoslu **Personalizēšana** un pēc tam atlasot **Eksportēt**. Papildinformāciju par rīkjoslu skatiet šī temata iepriekšējā sadaļa [Personalizēšana](#personalization-toolbar). Alternatīvi, ja ir iespējoti [saglabātie skati](saved-views.md), varat atvērt **Iestatījums \> Lietotāja opcijas \> Personalizēšana**, lai apskatītu visu savu personalizēšanas sarakstu sistēmā. No turienes varat atlasīt eksportējamos skatus vai personalizēšanas un pēc tam atlasīt **Eksportēt**.

Turklāt administratori var eksportēt citu lietotāju personalizēšanas, izpildot šādas darbības.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Personalizēšana**.
2. Cilnē **Lietotāji** atlasiet vajadzīgo lietotāju.
3. Atrodiet un atlasiet skatu vai personalizāciju, kas jums interesē.
4. Atlasiet **Eksportēt**.

#### <a name="import"></a>Importēšana

Lai importētu skatu vai personalizēšanu, varat tikai atvērt rīkjoslu **Personalizēšana** un atlasīt **Importēt**. Turklāt administratori var importēt failu un nekavējoties to piešķirt vienam vai vairākiem lietotājiem.

Ja ir iespējoti saglabātie skati, izpildiet šīs darbības.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Personalizēšana**.
2. Darbību rūtī atlasiet **Importēt skatus \> Lietotāja skati**.
3. Atlasiet importa režīmu:

    - **Atlasīt noteiktus lietotājus** – piešķiriet skatījumu vai personalizēšanu atlasītajiem lietotājiem.
    - **Importēt kā** - Importēt skatījumu vai personalizēšanu tam pašam lietotājam, kas to eksportēja.

4. Atlasiet **Pārlūkot**, un atrodiet un atlasiet importējamo personalizēšanu.
5. Atlasiet **Nākamais**.
6. Ja 3. darbībā atlasījāt **Atlasīt noteiktus lietotājus**, atlasiet lietotājus, kuriem importēt personalizēšanu.
7. Atlasiet **Importēt**.
8. Pēc vajadzības atrisiniet konfliktus.

Ja ir iespējoti saglabātie skati, izpildiet šīs darbības.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Personalizēšana**.
2. Atlasiet **Lietot**.
3. Atlasiet lietotājus, kuriem izplatīt personalizāciju.
4. Atlasiet **Importēt personalizēšanas no faila**.
5. Atlasiet **Pārlūkot**, un atrodiet un atlasiet importējamo personalizēšanu.
6. Atlasiet **Labi**.

## <a name="administration-of-personalizations"></a>Personalizāciju administrēšana

Lapa **Personalizācija** ir galvenais centrmezgls personalizēšanas pārvaldībai organizācijas līmenī. Šīs lapas saturs un iespējas ir atkarīgas no tā, vai ir ieslēgts līdzeklis **Saglabātie skati**.

Attiecībā uz klientiem, kuri ir ieslēguši līdzekli **Saglabātie skati**, skatiet sadaļu "Skatu pārvaldīšana globāli" tēmā [Saglabātie skati](saved-views.md).

Klientiem, kuri vēl nav ieslēguši [Saglabāti skati](saved-views.md) līdzekli, šai lapai ir četras cilnes:

- **Lietot** – varat importēt vai atlasīt kādu personalizāciju vienam vai vairākiem lietotājiem. Lai personalizāciju lietotu vienam lietotājam vai vairākiem, vispirms atlasiet kādu lomu un lietotājus, kuriem ir šī loma. Pēc tam atlasiet esošu personalizāciju, kuru lietot atlasītajiem lietotājiem, vai importējiet personalizēšanas failu. Personalizācija tiek validēta un tiek lietota visiem atlasītajiem lietotājiem nākamajā reizē, kad viņi atver atlasīto lapu.
- **Notīrīt** – varat notīrīt visas lapai vai darbvietai paredzētās personalizācijas vienam vai vairākiem lietotājiem. Vispirms atlasiet lapu vai darbvietu, lai redzētu sarakstu ar lietotājiem, kuri to ir personalizējuši. Pēc tam atlasiet lietotājus, kuriem ir nepieciešams notīrīt šīs lapas vai darbvietas personalizācijas, un atlasiet **Notīrīt**. Tiek dzēstas visas personalizācijas, ko atlasītie lietotāji ir lietojuši atlasītajai lapai vai darbvietai. Šo darbību nevar atsaukt. Taču, ja šai lapai vai darbvietai bija saglabāta kāda personalizācija, šo personalizāciju var importēt vēlreiz.
- **Lietotāji** – Atlasiet lietotāju, lai redzētu sarakstu ar lapām, ko lietotājs ir personalizējis. Pēc tam varat ieslēgt vai izslēgt lietotāja spēju lietot personalizācijas konkrētām lapām vai visai sistēmai. Varat arī importēt, eksportēt vai notīrīt personalizēšanu lietotājam. Turklāt varat atiestatīt līdzekļa remarkas lietotājam. Šādā gadījumā, ja lietotājs iepriekš noraidīja visus uznirstošos logus, kas ievies jaunus līdzekļus, tie atkal parādīsies nākamajā reizē, kad lietotājs sastop šos līdzekļus.
- **Sistēma** – Jūs varat īslaicīgi izslēgt personalizēšanu visiem lietotājiem sistēmā. Šādā gadījumā visi personalizācijas tiek dzēsti visiem lietotājiem, un visas lapas tiek atiestatītas uz noklusējuma statusu. Ja vēlāk personalizēšanu atkal ieslēdzat, visas personalizācijas ir atkal lietotas. Varat arī neatgriezeniski dzēst visas personalizācijas visiem lietotājiem sistēmā. Personalizācijas, kas tika izdzēstas, nav iespējams atgūt. Tādēļ, pirms veicat šo uzdevumu, noteikti eksportējiet visas personalizācijas, kuras vēlāk varētu būt nepieciešams.

## <a name="personalizing-inventory-dimensions"></a>Krājumu dimensiju personalizēšana.

Kad personalizējat krājumu dimensiju iestatījumus lapā, ņemiet vērā iestatījumus, kas izveidoti, izmantojot opciju **Parādīt dimensijas**. Piemēram, jūs izmantojat personalizāciju, lai paslēptu kolonnu partijas numuru krājumu dimensijai, bet šī kolonna tiek rādīta nākamajā reizē, kad lapa tiek atvērta. Tā notiek, jo iestatījumi **Dimensiju rādīšana** kontrolē, kuras krājumu dimensiju kolonnas tiek rādītas. Iestatījumi **Dimensiju rādīšana** tiek lietoti visās lapās, un tiem ir prioritāte pār jebkādiem personalizētajiem krājumu dimensiju lauku iestatījumiem atsevišķās lapās.

Tāpēc, tāpat kā iepriekšējā piemērā, ja nevēlaties, lai lapā tiek parādīta partijas numura krājumu dimensijas kolonna, ir jānoņem attiecīgās dimensijas atzīme konkrētās lapas opcijas **Parādīt dimensijas** ietvaros.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
