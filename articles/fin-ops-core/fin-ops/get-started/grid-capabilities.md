---
title: Režģa iespējas
description: Šajā tēmā ir aprakstīti vairāki ietekmīgi režģa kontroles līdzekļi. Lai piekļūtu šīm iespējām, ir jābūt iespējotam jaunajam režģa līdzeklim.
author: jasongre
ms.date: 03/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 58a05f893549a8b9e2e5cb83d02475d0fb5b7277
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384444"
---
# <a name="grid-capabilities"></a>Režģa iespējas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Jaunā režģa kontrole piedāvā daudzas noderīgas un jaudīgas iespējas, ko var izmantot, lai uzlabotu lietotāju produktivitāti, izveidotu vairāk interesantu jūsu datu skatu un iegūtu izsmeļošu ieskatu datos. Šajā rakstā ir apskatītas tālāk norādītās iespējas 

- Aprēķina kopsummu
- Rakstīšana pirms sistēmas
- Matemātisko izteiksmju novērtēšana 
- Tabulveida datu grupēšana (iespējota atsevišķi, **izmantojot līdzekli Grupēšana režģos**)
- Kolonnu sasaldēšana (iespējota atsevišķi, izmantojot kolonnu **sasaldēšanu režģos**)
- Automātiski ietilpināt kolonnas platumu
- Izstiepjamas kolonnas

## <a name="calculating-totals"></a>Aprēķina kopsummu
Finance and Operations programmās lietotājiem ir iespēja redzēt kopsummas režģu skaitlisko kolonnu apakšdaļā. Šīs kopsummas tiek rādītas kājenes sadaļā režģa apakšdaļā. 

### <a name="showing-the-grid-footer"></a>Režģa kājenes parādīšana
Katra tabulas režģa apakšdaļā finanšu un operāciju programmās ir kājenes apgabals. Kājenē var tikt parādīta vērtīga informācija, kas saistīta ar datiem, kas parādās režģī. Tālāk ir sniegti daži šādas informācijas piemēri:

- Atlasīto rindu skaits tabulā (ja ir atlasīts vairāk nekā viens ieraksts)
- Kopsummas, kas atrodas konfigurēto skaitlisko kolonnu lejasdaļā
- Datu kopā ietverto rindu skaits 

Šī kājene pēc noklusējuma ir paslēpta, bet to var ieslēgt. Lai parādītu režģa kājeni, atlasiet pogu **Režģa opcijas** režģa galvenē, tad atlasiet opciju **Rādīt kājeni**. Pēc tam, kad būsiet ieslēdzis kājeni noteiktam režģim, šis iestatījums atgādinās par sevi, līdz lietotājs izvēlēsies slēpt kājeni. Lai slēptu kājeni, atlasiet **Slēpt kājeni** **Režģa opciju** izvēlnē.

### <a name="specifying-columns-with-totals"></a>Kolonnu ar kopsummām norādīšana
Pašlaik neviena kolonna pēc noklusējuma nerāda kopsummas. Tā tiek uzskatīta par vienreizējas iestatīšanas darbību, kas ir līdzīga kolonnu platumu pielāgošanai režģos. Kad esat norādījis, ka vēlaties redzēt kolonnas kopsummas, šis iestatījums tiek saglabāts nākamajai reizei, kad apmeklēsiet lapu.

Ir divi veidi, kā konfigurēt kolonnu, lai parādītu kopsummu. 

- Ar peles labo pogu noklikšķiniet kolonnā, kurai vēlaties redzēt kopsummu, un atlasiet **Aprēķināt šīs kolonnas kopsummu**. Šī darbība izraisa trīs notikumu rašanos:

    1. Kājene kļūst redzama. 
    2. Tiek saglabāta jūsu izvēle redzēt šīs kolonnas kopsummu. 
    3. Tiek uzsākts aprēķins šai kolonnai un citām kolonnām, kurām iepriekš konfigurējāt kopsummu skatīšanu. Laiks, kas nepieciešams, lai parādītu kopsummu, ir atkarīgs no summējamās datu kopas apjoma.

- Kad kājene ir redzama, atlasiet **Rādīt kopsummu** kājenes apgabalā tās kolonnas apakšā, kurai vēlaties redzēt kopsummu. Ja nav nevienas konfigurētas kolonnas, tad visām skaitliskajām kolonnām būs pieejama poga **Rādīt kopsummu**. 

    Kad vismaz viena kolonna ir konfigurēta kopsummām, pogas **Rādīt kopsummu** būs pieejamas tikai uzvirzot kursoru vai fokusējot. Darbība, atlasot **Rādīt kopsummu** tikai saglabā jūsu izvēli redzēt kopsummu šajā kolonnā, un šī izvēle tiek izmantota turpmāku lapas apmeklējumu laikā. Kājenē šis stāvoklis tiek norādīts ar svītru, kas parādās kolonnā. (Vai arī, ja datu kopa ir pietiekami maza, kopsumma tiek nekavējoties rādīta.)

Ja kļūdāties un nevēlaties redzēt kopsummu noteiktā kolonnā, ar peles labo pogu noklikšķiniet uz kolonnas un atlasiet **Paslēpt kopsummu**, vai arī atlasiet pogu **Paslēpt kopsummu** šīs kolonnas kājenē. Šī izvēle tiks saglabāta arī turpmākiem lapas apmeklējumiem. 

### <a name="calculating-totals"></a>Aprēķina kopsummu
Ja, atnākot uz lapu, kājene ir redzama un kolonnas jau ir konfigurētas kopsummām, tās var tikt rādītas kājenē vai arī var netikt rādītas. Šī darbība ir atkarīga no datu kopas izmēra lapā. Ja datu kopa ir pietiekami maza, kopsummas tiks rādītas automātiski vienlaikus ar rindu skaitu datu kopā. Ja kājenē zem kolonnām, ko konfigurējāt kopsummām, ir svītras, tad datu kopa ir pārāk liela, lai sistēma uzreiz parādītu kopsummas, un kopsummu aprēķināšanai vajadzīga tieša darbība. Lai to izdarītu, noklikšķiniet kājenē uz pogas **Aprēķināt** vai ar peles labo pogu noklikšķiniet uz kolonnas, kurai vēlaties kopsummu, un atlasiet **Aprēķināt šīs kolonnas kopsummu**.

Ja aprēķina pabeigšanai nepieciešams ilgs laiks, operāciju var atcelt, atlasot **pogu Atcelt**. Dažreiz datu kopa būs pārāk liela, lai aprēķinātu kopsummas (jūsu organizācijas noteiktais ierobežojums), un tā vietā jums tiks paziņots, ka dati tiks filtrēti vairāk. 

> [!NOTE]
> Sistēmas administrācijas var mainīt kopsummu aprēķināšanai pieejamo ierakstu skaita ierobežojumu, **koriģējot maksimālo lokālo ierakstu skaitu katram režģa** parametram **klienta veiktspējas opciju** lapā. Noklusējuma vērtība ir 25 000 ierakstu. Administratoriem jābūt uzmanīgiem, pielāgojot šo vērtību, jo pārāk liela vērtība var izsmelt lietotāja datorā pieejamo atmiņu. Ieteikums nedrīkst pārsniegt 50 000 ierakstu.   

Kopsummas tiks automātiski atjauninātas, datu kopā atjauninot, dzēšot vai izveidojot rindas.

## <a name="typing-ahead-of-the-system"></a>Rakstīšana pirms sistēmas
Daudzos biznesa scenārijos spēja ātri ievadīt datus sistēmā ir ļoti svarīga. Pirms jaunā režģa kontroles ieviešanas lietotāji varēja mainīt datus tikai pašreizējā rindā. Pirms tie var izveidot jaunu rindu vai pārslēgties uz citu rindu, tie bija spiesti gaidīt, lai sistēma veiksmīgi apstiprinātu visas izmaiņas. Lai samazinātu laiku, kad lietotāji gaida šo pabeigšanu, un lai uzlabotu lietotāju produktivitāti, jaunais režģis pielāgo šīs darbības, lai tās būtu asinhronas. Tāpēc lietotājs var pārvietoties uz citām rindām, lai veiktu izmaiņas, kamēr tiek gaidītas iepriekšējās rindas pārbaudes. 

Lai atbalstītu šo jauno uzvedību, rindas statusam ir pievienota jauna kolonna pa lbabi no rindas atlases kolonnas, kad režģis ir rediģēšanas režīmā. Šī kolonna norāda vienu no šiem statusiem:

- **Tukšs** – nav statusa attēla, kas norāda, ka sistēma ir veiksmīgi saglabājusi rindu.
- **Gaida apstrādi** — šis statuss norāda, ka izmaiņas rindā vēl nav saglabātas serverī, bet ir pārstrādājamo izmaiņu rindā. Pirms darbības veikšanas ārpus režģa ir jāgaida, kamēr tiks apstrādātas visas gaidošās izmaiņas. Turklāt teksts šajās rindās ir slīprakstā, lai norādītu rindu nesaglabāto statusu. 
- **Nederīgs stāvoklis** — šis statuss norāda, ka rindas apstrādes laikā tika izraisīts kāds brīdinājums vai ziņojums, un tas, iespējams, ir liedzis sistēmai saglabāt šīs rindas izmaiņas. Vecajā režģī, ja darbība bija nesekmīga, jūs tikāt aizvests atpakaļ uz rindu, lai nekavējoties labotu problēmu. Tomēr jaunajā režģī tiek paziņots, ka ir konstatēta apstiprināšanas problēma, bet varat izlemt, kad vēlaties labot rindas problēmas. Kad esat gatavs labot problēmu, varat manuāli pārvietot fokusu uz rindu. Kā alternatīvu jūs varat izvēlēties darbību **Labot šo problēmu**. Šī darbība nekavējoties pārvieto fokusu uz rindu, kurā ir problēma, un ļauj veikt labojumus režģī vai tā ārpusē. Ņemiet vērā, ka turpmākās gaidošās rindas tiek apturētas, līdz šis apstiprināšanas brīdinājums tiek novērsts. 
- **Apturēts** — šis statuss norāda, ka apstrāde ar serveri ir apturēta, jo rindas validācija izraisīja uznirstošo dialoglodziņu, kas pieprasa lietotāja ievadi. Tā kā lietotājs, iespējams, ievada datus citās rindās, uznirstošais dialoglodziņš netiek uzreiz parādīts šim lietotājam. Tā vietā tas tiks parādīts, kad lietotājs izvēlas atsākt apstrādi. Šim statusam ir pievienots paziņojums, kas informē lietotāju par šo situāciju. Paziņojums ietver darbību **Turpināt apstrādi**, kas izraisīs uznirstošo dialoglodziņu.

Kad lietotāji ievada datus pirms servera apstrādes vietas, tie var sagaidīt dažas datu ievades pieredzes pasliktinājumus, piemēram, informācijas trūkumu, kontroles līmeņa pārbaudi un noklusējuma vērtību ievadi. Lietotāji, kuriem nepieciešams nolaižamais saraksts, lai atrastu vērtību, tiek mudināti sagaidīt, kad serveris nokļūs pašreizējā rindā. Kontroles līmeņa validācija un noklusēto vērtību ievade arī notiks, kad serveris apstrādā šo rindu.

### <a name="pasting-from-excel"></a>Ielīmēšana no Excel
Lietotāji vienmēr ir spējuši eksportēt datus no finance and Operations programmu režģiem, izmantojot Microsoft Excel **mehānismu Eksportēt uz Excel**. Tomēr iespēja ievadīt datus pirms sistēmas ļauj jaunajam režģim atbalstīt tabulu kopēšanu no programmas Excel un ielīmēt tās tieši režģos Finance and Operations programmās. Režģa šūna, no kuras tiek sākta ielīmēšanas darbība, nosaka, kur kopēto tabulu sāk ielīmēt. Režģa saturs tiek pārrakstīts ar kopētās tabulas saturu, izņemot divos gadījumos:

- Ja kolonnu skaits kopētajā tabulā pārsniedz kolonnu skaitu, kas paliek režģī, sākot no ielīmēšanas vietas, lietotājam tiek paziņots, ka papildu kolonnas ir ignorētas. 
- Ja rindu skaits kopētajā tabulā pārsniedz rindu skaitu režģī, sākot no ielīmēšanas vietas, esošās šūnas tiek pārrakstītas ar ielīmēto saturu, un visas papildu rindas no kopētās tabulas tiek iespraustas kā jaunas rindas režģa apakšā. 

## <a name="evaluating-math-expressions"></a>Matemātisko izteiksmju novērtēšana
Produktivitātes veicināšanai lietotāji režģa ciparu šūnās var ievadīt matemātiskas formulas. Viņiem nav jāveic aprēķini programmā ārpus sistēmas. Piemēram, ja ievadāt **=15\*4** un pēc tam nospiežat taustiņu **TAB**, lai izietu no lauka, sistēma novērtēs izteiksmi un saglabās vērtību **60** laukam.

Lai sistēma atpazītu vērtību kā izteiksmi, sāciet vērtību ar vienādības zīmi (**=**). Papildinformāciju par atbalstītajiem operatoriem un sintaksi skatiet [Atbalstītie matemātiskie simboli](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Tabulas datu grupēšana
Biznesa lietotājiem bieži jāveic datu ekspromtanalīze. Lai gan to var izdarīt, eksportējot datus uz Microsoft Excel rakursatūrām **un izmantojot tās,** līdzeklis Grupēšana tīklos, kas ir atkarīgs no jaunā režģa vadības līdzekļa, ļauj lietotājiem organizēt savus tabulas datus interesantā veidā Finance and Operations programmās. Tā kā šis līdzeklis paplašina līdzekli **Kopsumma**, līdzeklis **Grupēšana** ļauj iegūt izsmeļošu ieskatu datos, sniedzot apakšsummas grupas līmenī.

Lai izmantotu šo funkciju, ar peles labo pogu noklikšķiniet uz kolonnas, pēc kuras vēlaties grupēt, un atlasiet **Grupēt pēc šīs kolonnas**. Veicot šo darbību, dati tiks šķiroti pēc atlasītās kolonnas, režģa sākumā tiks pievienota jauna kolonna **Grupēt pēc** un katras grupas sākumā tiks ievietotas “galvenes rindas”. Šīs virsraksta rindas sniedz tālak norādīto informāciju par katru grupu.

- Grupas datu vērtība 
- Kolonnas nosaukums (šī informācija ir īpaši noderīga, ja jums ir vairāki grupēšanas līmeņi.)
- Datu rindu skaits šajā grupā
- Kolonnu, kas konfigurētas kopsummu rādīšanai, apakšsummas

Kad ir aktivizēti [Saglabātie skati](saved-views.md), šo grupēšanu var saglabāt ar personalizāciju kā daļu no skata, lai nākamreiz, kad apmeklēsiet šo lapu, nodrošinātu ātru piekļuvi.

### <a name="multiple-levels-of-grouping"></a>Vairāki grupēšanas līmeņi
Kad dati ir grupēti pēc vienas kolonnas, datus var grupēt pēc citas kolonnas, vēlamajā kolonnā atlasot **Grupēt pēc šīs kolonnas**. Šo procesu var atkārtot, kamēr nav 5 ligzdotu grupēšanas līmeņu, kas ir maksimālais atbalstītais dziļums. Šajā brīdī vairs nevarēsit grupēt pēc papildu kolonnām.

Jebkurā brīdī varat noņemt grupēšanu jebkurā kolonnā, ar peles labo pogu noklikšķinot uz šīs kolonnas un atlasot **Atgrupēt**. Varat arī noņemt grupēšanu no visām kolonnām, atlasot **Režģa opcijas** un pēc tam atlasot **Atgrupēt visu**.

### <a name="sorting-grouped-data"></a>Grupēto datu kārtošana
Pēc datu grupēšanas pa vienai vai vairākām kolonnām var mainīt kārtošanas virzienu jebkurai grupēšanas kolonnai, izmantojot atbilstošo kolonnas galveni. 

Kārtošanas darbība, kārtojot pēc negrupētām kolonnām, ir atkarīga no produkta versijas:

- Versijā 10.0.24 un vecākā versijā, ja kārtojat pēc negrupētas kolonnas, grupēšana tiek noņemta no visām kolonnām un dati tiek kārtoti atlasītajā kolonnā. 
- Versijā 10.0.25 un jaunākās versijās, ja kārtojat pēc negrupētas kolonnas, grupēšana paliek neskarta un dati tiek kārtoti katrā grupā, pamatojoties uz atlasīto kolonnu.

### <a name="expanding-and-collapsing-groups"></a>Grupu paplašināšana un sakļaušana
Sākotnējai datu grupēšanai būs paplašinātas visas grupas. Varat izveidot kopsavilkuma skatījumus datiem, sakļaujot atsevišķas grupas, vai arī varat izmantot grupas paplašināšanu un sakļaušanu, lai palīdzētu pārvietoties pa datiem. Lai paplašinātu vai sakļautu grupu, atbilstošajā grupas virsraksta rindā atlasiet pogu Chevron (>). Ņemiet vērā, ka atsevišķu grupu paplašināšanas/sakļaušanas stāvoklis personalizācijā **netiek** saglabāts.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Rindu atlasīšana un atlases noņemšana grupas līmenī
Tāpat kā visas režģa rindas var atlasīt (vai noņemt atlasi), atzīmējot izvēles rūtiņu režģa pirmās kolonnas augšdaļā, var arī ātri atlasīt (vai noņemt atlasi) visas grupas rindas, atzīmējot izvēles rūtiņu atbilstošajā grupas galvenes rindā. Grupas galvenes rindas izvēles rūtiņa vienmēr atspoguļo šīs grupas rindu pašreizējo atlases stāvokli neatkarīgi no tā, vai ir atlasītas visas rindas, nav atlasīta neviena rinda vai ir atlasītas tikai dažas rindas.

### <a name="hiding-column-names"></a>Kolonnu nosaukumu paslēpšana
Grupējot datus, noklusējuma darbība ir parādīt kolonnas nosaukumu grupas galvenes rindā. Varat izvēlēties neiekļaut kolonnas nosaukumu grupu galvenes rindās, atlasot **Režģa opcijas** > **Paslēpt grupas kolonnas nosaukumu**.

### <a name="grouping-on-date-and-time-columns"></a>Grupēšana pēc datuma un laika kolonnām
Sākot ar versiju 10.0.24 laukiem Datums vai Datums, opcija ir pievienota grupai pa gadiem, mēnešiem vai dienām. Grupa "vērtība" atbilstošajā galvenes rindā atbildīs formātam no šī lauka. Turklāt laukiem DateTime un Time var grupēt pēc stundas, minūtes vai sekundes. 

## <a name="freezing-columns"></a>Iesaldēšanas kolonnas
Dažas kolonnas režģī var būt pietiekoši nozīmīgas kontekstam, ko nevēlaties ritināt ārpus skata. Tā vietā, iespējams, vēlēsities, lai šo kolonnu vērtības vienmēr būtu redzamas. Režģa **kolonnu** sasaldēšanas līdzeklis nodrošina šo elastību lietotājiem. 

Lai kolonnu iesaldētu, ar peles labo pogu noklikšķiniet kolonnas virsrakstā un pēc tam atlasiet **Iesaldēt kolonnu**. Pirmo reizi pabeidzot šo soli, atlasītā kolonna kļūst par pirmo kolonnu un vairs neritinās skatu. Visas sekojošās kolonnas, kas sasaldētas, tiks pievienotas pēdējās iesaldētās kolonnas labajā pusē. Lai pārkārtotu iesaldētās kolonnas pēc nepieciešamības, varat izmantot standarta funkcionalitāti Pārvietot. Tomēr iesaldētās kolonnas nevar pārvietot, lai tās parādītos starp atsaldēto kolonnu kopu. Tomēr iesaldētās kolonnas nevar pārvietot, lai tās parādītos starp atsaldēto kolonnu kopu.

Lai kolonnu atsaldētu, ar peles labo pogu noklikšķiniet kolonnas virsrakstā un pēc tam atlasiet **Atsaldēt kolonnu**. 

Ievērojiet, ka rindu atlase un rindu statusa kolonnas jaunajā režģī vienmēr tiek iesaldētas kā pirmās divas kolonnas. Tādējādi, kad šīs kolonnas ir iekļautas režģī, tās vienmēr būs redzamas lietotājam neatkarīgi no horizontālās ritināšanas pozīcijas režģī. Šīs divas kolonnas nevar pārkārtot.

## <a name="autofit-column-width"></a>Automātiski ietilpināt kolonnas platumu
Līdzīgi kā programma Excel, lietotāji var automātiski piestāt kolonnas izmēru, ņemot vērā šajā kolonnā pašlaik rādīto saturu. Lai to izdarītu, veiciet dubultklikšķi uz izmēru maiņas turi kolonnā vai, ievietojot fokusu kolonnas virsrakstā un nospiežot **A** (automātiskajai ietilpināšanai). Šī iespēja ir pieejama no versijas 10.0.23.

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kā iespējot jauno režģa kontroli manā vidē? 

**Jaunā režģa kontroles** līdzeklis ir pieejams tieši Līdzekļu pārvaldībā jebkurā vidē. Pēc līdzekļa iespējošanas līdzekļu pārvaldībā, visas turpmākās sesijas izmantos jauno režģa kontroli. 

Šis līdzeklis pēc noklusējuma tiek iespējots no 10.0.21. versijas, un ir paredzēts, ka tas kļūs par obligātu no 10.0.25. versijas. 

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Attīstītājs] Atteikšanās no atsevišķām lapām, izmantojot jauno režģi 
Ja jūsu organizācija atklāj lapu, kurā ir dažas problēmas, izmantojot jauno režģi, ir pieejams API, lai ļautu atsevišķai formai izmantot mantoto režģa vadīklu, joprojām ļaujot pārējai sistēmai izmantot jauno režģa vadīklu. Lai izņemtu atsevišķu lapu no jaunā režģa, pievienojiet šādu izsaukuma ierakstu `super()` formas `run()` metodē.

```this.forceLegacyGrid();```

Šis API tiks ievērots, līdz jaunā tīkla kontrole kļūs obligāta. Pašlaik šīs izmaiņas ir paredzētas 2022. gada oktobrim. Ja kādai problēmai nepieciešams izmantot šo API, ziņojiet par to Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Lapas piespiedu jaunā režģa izmantošanai pēc iepriekšējas iziešanas no režģa
Ja esat izvēlējies atsevišķu lapu, lai neizmantotu jauno režģi, iespējams, vēlēsieties pēc tam atkārtoti aktivizēt jauno režģi pēc pakārtoto problēmu atrisināšanas. Lai to paveiktu, vienkārši ir jānoņem izsaukums `forceLegacyGrid()`. Izmaiņas stāsies spēkā tikai pēc tam, kad notiks kāda no šīm darbībām:

- **Vides atkārtota izvietošana**: kad vide tiek atjaunināta un atkārtota izvietošana, tabula, kurā tiek glabātas lapas, kas ir aizstātas ar jauno režģi (FormControlReactGridState) tiek automātiski notīrīta.
- **Manuāla tabulas tīrīšana**: izstrādes scenārijiem ir jāizmanto SQL, lai notīrītu tabulu FormControlReactGridState un pēc tam restartētu AOS. Šī darbību kombinācija atiestatīs lapu kešatmiņu, kuras izvēlējās jaunajam režģim.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Izstrādātājs] Atsevišķu režģu izvēle ārpus rakstīšanas pirms sistēmas iespējas
Ir radušies daži scenāriji, kas neļauj labi strādāt ar *rakstīšanu pirms tīkla sistēmas* iespējas. (Piemēram, kāds kods, kas tiek aktivizēts, kad rinda tiek validēta, izraisa datu avota izpētes aktivizēšanu, un pēc tam izpēte var bojāt nesaistītos labojumus esošajās rindās.) Ja jūsu organizācija atklāj šādu scenāriju, ir pieejams API, kas ļauj izstrādātājam izvēlēties atsevišķu režģi no asinhronās rindas validācijas un atgriezties pie mantotās uzvedības.

Ja režģī ir atspējota asinhronā rindas validācija, lietotāji nevar izveidot jaunu rindu vai pārvietoties uz citu esošu rindu režģī, kamēr pašreizējā rindā ir validācijas problēmas. Kā šīs darbības blakusparādību tabulas nevar ielīmēt no programmas Excel finanšu un operāciju tīklos.

Lai izvēlētos atsevišķu režģi no asinhronās rindas validācijas, formas metodē pievienojiet šādu izsaukumu pēc `super()``run()`.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Šis uzaicinājums būtu jāizmanto tikai izņēmuma gadījumos, un tam nevajadzētu būt normai attiecībā uz visiem tīkliem.
> - Mēs neiesakām pārslēgt šo API izpildlaikā pēc veidlapas ielādes.

## <a name="developer-size-to-available-width-columns"></a>[Izstrādātājs] Pielāgot pieejamo kolonnu platumu
Ja izstrādātājs jaunā režģa kolonnās iestata rekvizītu **WidthMode** uz **SizeToAvailable**, šīm kolonnām sākotnēji ir tāds pats platums, kāds tām būtu, ja rekvizīts būtu iestatīts uz **SizeToContent**. Tomēr tās izplešas, lai izmantotu jebkādu pieejamo papildu platumu režģī. Ja vairākām kolonnām rekvizīts ir iestatīts uz **SizeToAvailable**, visas šīs kolonnas koplieto jebkādu pieejamo papildu platumu režģī. Tomēr, ja lietotājs manuāli maina lielumu vienai no šīm kolonnām, tad kolonna kļūst statiska. Tās paliks šajā platumā un vairs neaizņems pieejamo papildu režģa platumu.

## <a name="known-issues"></a>Zināmās problēmas
Šajā sadaļā tiek uzturēts saraksts ar zināmām problēmām jaunajai režģa kontrolei.

### <a name="open-issues"></a>Aktuālās problēmas
- Pēc **Jaunā režģa kontroles** līdzekļa iespējošanas dažas lapas turpinās izmantot esošo režģa kontroli. Tas notiks šādās situācijās:
 
    - Kartīšu saraksts atrodas lapā, kas tiek atveidots vairākās kolonnās.
    - Grupētu kartīšu saraksts atrodas lapā.
    - Režģa kolonna ar nereaģētu paplašināmo kontroli.

    Kad lietotājs pirmo reizi sastopas ar vienu no šīm situācijām, tiks parādīts ziņojums par lapas atsvaidzināšanu. Kad parādās šis ziņojums, lapa turpinās izmantot esošo režģi visiem lietotājiem līdz nākamās preces versijas atjaunināšanai. Šo scenāriju labākai apstrādei, lai varētu izmantot jauno režģi, tiks apsvērta turpmāka atjaunināšana.

- [KB 4582758] Ieraksti ir izplūduši, mainot tālummaiņu no 100 uz jebkuru citu procentuālo vērtību
- [KB 4592012] Radusies neparedzēta klienta kļūda IE11, ielīmējot vairākas rindas no Excel

    Microsoft neatbalsta labojumu šai problēmai


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
