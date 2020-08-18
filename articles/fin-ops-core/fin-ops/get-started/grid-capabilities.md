---
title: Režģa iespējas
description: Šajā tēmā ir aprakstīti vairāki ietekmīgi režģa kontroles līdzekļi. Lai piekļūtu šīm iespējām, ir jābūt iespējotam jaunajam režģa līdzeklim.
author: jasongre
manager: AnnBe
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b1dd5e852bdc116d0848687782c930b19eae7900
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/03/2020
ms.locfileid: "3651694"
---
# <a name="grid-capabilities"></a>Režģa iespējas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Jaunā režģa kontrole piedāvā daudzas noderīgas un jaudīgas iespējas, ko var izmantot, lai uzlabotu lietotāju produktivitāti, izveidotu vairāk interesantu jūsu datu skatu un iegūtu izsmeļošu ieskatu datos. Šajā rakstā ir apskatītas tālāk norādītās iespējas 

-  Aprēķina kopsummu
-  Datu grupēšana
-  Rakstīšana pirms sistēmas
-  Matemātisko izteiksmju novērtēšana 

## <a name="calculating-totals"></a>Aprēķina kopsummu
Programmatūrā Finance and Operations lietotājiem ir iespēja redzēt kopsummas režģos ciparu kolonnu lejasdaļā. Šīs kopsummas tiek rādītas kājenes sadaļā režģa apakšdaļā. 

### <a name="showing-the-grid-footer"></a>Režģa kājenes parādīšana
Katra Finance and Operations programmas tabulārā režģa apakšējā daļā ir kājenes apgabals. Kājenē var tikt parādīta vērtīga informācija, kas saistīta ar datiem, kas parādās režģī. Tālāk ir sniegti daži šādas informācijas piemēri:

- Atlasīto rindu skaits tabulā (ja ir atlasīts vairāk nekā viens ieraksts)
- Kopsummas, kas atrodas konfigurēto skaitlisko kolonnu lejasdaļā
- Datu kopā ietverto rindu skaits 

Šī kājene pēc noklusējuma ir paslēpta, bet to var viegli ieslēgt. Lai parādītu režģa kājeni, noklikšķiniet ar peles labo pogu režģī uz kolonnas galvenes un atlasiet opciju **Rādīt kājeni**. Pēc tam, kad kājene ir ieslēgta noteiktam režģim, šis iestatījums tiks saglabāts, kamēr lietotājs izvēlas slēpt kājeni, ko var izdarīt, ar peles labo pogu noklikšķinot uz kolonnas galvenes un atlasot **Paslēpt kājeni**.  Ievērojiet, ka turpmākā atjauninājumā plānots pārvietot darbības **Rādīt kājeni/paslēpt kājeni** novietojumu. 

### <a name="specifying-columns-with-totals"></a>Kolonnu ar kopsummām norādīšana
Pašlaik kolonnas netiks konfigurētas kopsummu rādīšanai pēc noklusējuma. Tā tiek uzskatīta par vienreizējas iestatīšanas darbību, kas ir līdzīga kolonnu platumu pielāgošanai režģos. Kad esat norādījis, ka vēlaties redzēt kolonnas kopsummas, šis iestatījums tiek saglabāts nākamajai reizei, kad apmeklēsiet lapu.  

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

Ja aprēķināsana notiek pārāk ilgi, varat atcelt operāciju, atlasot pogu **Atcelt**. Tomēr dažkārt datu kopa būs pārāk liela, lai aprēķinātu kopsummas (ierobežojums, ko nosaka jūsu organizācija), un jūs tiksiet informēts, lai vairāk filtrētu savus datus.

Kopsummas tiks automātiski atjauninātas, datu kopā atjauninot, dzēšot vai izveidojot rindas.  

## <a name="grouping-data"></a>Datu grupēšana
Biznesa lietotājiem bieži jāveic datu ekspromtanalīze. Lai gan to var izdarīt, eksportējot datus uz Microsoft Excel un izmantojot pivot tabulas, **Grupēšanas** iespēja tabulārajā režģī ļauj lietotājiem programmās Finance and Operations organizēt savus datus interesantākos veidos. Līdzīgi kā šis līdzeklis paplašina līdzekli **Kopsumma**, arī **Grupēšana** ļauj iegūt izsmeļošu ieskatu datos, sniedzot apakšsummas grupas līmenī.

Lai izmantotu šo funkciju, ar peles labo pogu noklikšķiniet uz kolonnas, pēc kuras vēlaties grupēt, un atlasiet **Grupēt pēc šīs kolonnas**. Veicot šo darbību, dati tiks šķiroti pēc atlasītās kolonnas, režģa sākumā tiks pievienota jauna Grupa pēc kolonnas un katras grupas sākumā tiks ievietotas “galvenes rindas”. Šīs virsraksta rindas sniedz tālak norādīto informāciju par katru grupu. 
-  Grupas datu vērtība 
-  Kolonnas etiķete (šī informācija būs īpaši noderīga pēc vairāku grupēšanas līmeņu atbalsta.)
-  Datu rindu skaits šajā grupā
-  Kolonnu, kas konfigurētas kopsummu rādīšanai, apakšsummas

Kad ir aktivizēti [Saglabātie skati](saved-views.md), šo grupēšanu var saglabāt ar personalizāciju kā daļu no skata, lai nākamreiz, kad apmeklēsiet šo lapu, nodrošinātu ātru piekļuvi.  

Ja izvēlaties **Grupēt pēc šīs kolonnas** citai kolonnai, sākotnējā grupēšana tiks aizstāta, jo versijā 10.0.9 ar Platform Update 33 tiek atbalstīts tikai viens grupēšanas līmenis.

Lai režģī atceltu grupēšanu, ar peles labo pogu noklikšķiniet uz grupēšana kolonnas un atlasiet **Atgrupēt**.  

## <a name="typing-ahead-of-the-system"></a>Rakstīšana pirms sistēmas
Daudzos biznesa scenārijos spēja ātri ievadīt datus sistēmā ir ļoti svarīga. Pirms jaunā režģa kontroles ieviešanas lietotāji varēja mainīt datus tikai pašreizējā rindā. Pirms tie var izveidot jaunu rindu vai pārslēgties uz citu rindu, tie bija spiesti gaidīt, lai sistēma veiksmīgi apstiprinātu visas izmaiņas. Lai samazinātu laiku, kad lietotāji gaida šo pabeigšanu, un lai uzlabotu lietotāju produktivitāti, jaunais režģis pielāgo šīs darbības, lai tās būtu asinhronas. Tāpēc lietotājs var pārvietoties uz citām rindām, lai veiktu izmaiņas, kamēr tiek gaidītas iepriekšējās rindas pārbaudes. 

Lai atbalstītu šo jauno uzvedību, rindas statusam ir pievienota jauna kolonna pa lbabi no rindas atlases kolonnas, kad režģis ir rediģēšanas režīmā. Šī kolonna norāda vienu no šiem statusiem:

- **Tukšs** – nav statusa attēla, kas norāda, ka sistēma ir veiksmīgi saglabājusi rindu.
- **Gaida apstrādi** — šis statuss norāda, ka izmaiņas rindā vēl nav saglabātas serverī, bet ir pārstrādājamo izmaiņu rindā. Pirms darbības veikšanas ārpus režģa ir jāgaida, kamēr tiks apstrādātas visas gaidošās izmaiņas. Turklāt teksts šajās rindās ir slīprakstā, lai norādītu rindu nesaglabāto statusu. 
- **Nederīgs stāvoklis** — šis statuss norāda, ka rindas apstrādes laikā tika izraisīts kāds brīdinājums vai ziņojums, un tas, iespējams, ir liedzis sistēmai saglabāt šīs rindas izmaiņas. Vecajā režģī, ja darbība bija nesekmīga, jūs tikāt aizvests atpakaļ uz rindu, lai nekavējoties labotu problēmu. Tomēr jaunajā režģī tiek paziņots, ka ir konstatēta apstiprināšanas problēma, bet varat izlemt, kad vēlaties labot rindas problēmas. Kad esat gatavs labot problēmu, varat manuāli pārvietot fokusu uz rindu. Kā alternatīvu jūs varat izvēlēties darbību **Labot šo problēmu**. Šī darbība nekavējoties pārvieto fokusu uz rindu, kurā ir problēma, un ļauj veikt labojumus režģī vai tā ārpusē. Ņemiet vērā, ka turpmākās gaidošās rindas tiek apturētas, līdz šis apstiprināšanas brīdinājums tiek novērsts. 
- **Apturēts** — šis statuss norāda, ka apstrāde ar serveri ir apturēta, jo rindas validācija izraisīja uznirstošo dialoglodziņu, kas pieprasa lietotāja ievadi. Tā kā lietotājs, iespējams, ievada datus citās rindās, uznirstošais dialoglodziņš netiek uzreiz parādīts šim lietotājam. Tā vietā tas tiks parādīts, kad lietotājs izvēlas atsākt apstrādi. Šim statusam ir pievienots paziņojums, kas informē lietotāju par šo situāciju. Paziņojums ietver darbību **Turpināt apstrādi**, kas izraisīs uznirstošo dialoglodziņu.  
    
Kad lietotāji ievada datus pirms servera apstrādes vietas, tie var sagaidīt dažas datu ievades pieredzes pasliktinājumus, piemēram, informācijas trūkumu, kontroles līmeņa pārbaudi un noklusējuma vērtību ievadi. Lietotāji, kuriem nepieciešams nolaižamais saraksts, lai atrastu vērtību, tiek mudināti sagaidīt, kad serveris nokļūs pašreizējā rindā. Kontroles līmeņa validācija un noklusēto vērtību ievade arī notiks, kad serveris apstrādā šo rindu.   

### <a name="pasting-from-excel"></a>Ielīmēšana no Excel
Lietotāji vienmēr ir spējuši eksportēt datus no režģiem Finance and Operations programmās uz Excel, izmantojot **Eksportēt uz Excel** mehānismu. Tomēr spēja ievadīt datus pirms sistēmas iespējo jauno režģi, lai atbalstītu tabulu kopēšanu no Excel un ielīmētu tās tieši režģos Finance and Operations lietojumprogrammās. Režģa šūna, no kuras tiek sākta ielīmēšanas darbība, nosaka, kur kopēto tabulu sāk ielīmēt. Režģa saturs tiek pārrakstīts ar kopētās tabulas saturu, izņemot divos gadījumos:

- Ja kolonnu skaits kopētajā tabulā pārsniedz kolonnu skaitu, kas paliek režģī, sākot no ielīmēšanas vietas, lietotājam tiek paziņots, ka papildu kolonnas ir ignorētas. 
- Ja rindu skaits kopētajā tabulā pārsniedz rindu skaitu režģī, sākot no ielīmēšanas vietas, esošās šūnas tiek pārrakstītas ar ielīmēto saturu, un visas papildu rindas no kopētās tabulas tiek iespraustas kā jaunas rindas režģa apakšā. 

## <a name="evaluating-math-expressions"></a>Matemātisko izteiksmju novērtēšana
Produktivitātes veicināšanai lietotāji režģa ciparu šūnās var ievadīt matemātiskas formulas. Viņiem nav jāveic aprēķini programmā ārpus sistēmas. Piemēram, ja ievadāt **15\*4** un pēc tam nospiežat taustiņu **TAB**, lai izietu no lauka, sistēma novērtēs izteiksmi un saglabās vērtību **60** laukam.

Lai sistēma atpazītu vērtību kā izteiksmi, sāciet vērtību ar vienādības zīmi (**=**). Papildinformāciju par atbalstītajiem operatoriem un sintaksi skatiet [Atbalstītie matemātiskie simboli](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kā iespējot jauno režģa kontroli manā vidē? 

**10.0.9/Platform update 33 vai jaunāka** **Jauno režģu kontroles** līdzeklis ir pieejams tieši Līdzekļu pārvaldībā jebkurā vidē. Tāpat kā citi publiskie priekšskatījuma līdzekļi, uz šī līdzekļa iespējošanu ražošanā attiecas [Lietošanas līguma papildu nosacījumi](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8/Platform update 32 vai 10.0.7/Platform update 31** Līdzekli **Jaunā režģa kontrole** var iespējot 1. līmeņa (Dev/Test) un 2. līmeņa (Smilškastes) vidē, lai nodrošinātu papildu testēšanas un noformējuma izmaiņas, veicot tālāk norādītās darbības.

1.  **Iespējot būvējumu izsniegšanu**: izpildīt šādu SQL priekšrakstu: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Atiestatiet IIS**, lai notīrītu statisko būvējuma kešatmiņu. 

3.  **Atrast funkciju**: atveriet darbvietu **Funkciju pārvaldība**. Ja **Jaunā režģa kontrole** nav redzama visu funkciju sarakstā, atlasiet **Pārbaudīt, vai nav atjauninājumu**.   

4.  **Iespējot funkciju**: atrodiet funkciju **Jaunā režģa kontrole** funkciju sarakstā un detalizētās informācijas rūtī atlasiet **Iespējot tūlīt**. Ņemiet vērā, ka ir nepieciešama pārlūkprogrammas atsvaidzināšana. 

Visas turpmākās lietotāja sesijas sāksies ar iespējotu jaunā režģa kontroli.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Attīstītājs] Atteikšanās no atsevišķām lapām, izmantojot jauno režģi 
Ja jūsu organizācija atklāj lapu, kurā ir dažas problēmas, izmantojot jauno režģi, ir pieejams API, lai ļautu atsevišķai formai izmantot mantoto režģa vadīklu, joprojām ļaujot pārējai sistēmai izmantot jauno režģa vadīklu. Lai izņemtu atsevišķu lapu no jaunā režģa, pievienojiet šādu izsaukuma ierakstu `super()` formas `run()` metodē.

        this.forceLegacyGrid();

Šis API tiks ievērots līdz 2021. gada oktobra izlaidumam, kad jaunā režģa kontrole kļūs obligāta. Lūdzu, ziņojiet par visām Microsoft problēmām, kam nepieciešams izmantot šo API. 

## <a name="known-issues"></a>Zināmās problēmas
Šajā sadaļā ir saglabāts saraksts ar zināmajām problēmām jaunajai režģa kontrolei, kamēr līdzeklis atrodas priekšskatījuma stāvoklī.  

### <a name="open-issues"></a>Aktuālās problēmas
-  Pēc **Jaunā režģa kontroles** līdzekļa iespējošanas dažas lapas turpinās izmantot esošo režģa kontroli. Tas notiks šādās situācijās:  
    -  Kartīšu saraksts atrodas lapā, kas tiek atveidots vairākās kolonnās.
    -  Grupētu kartīšu saraksts atrodas lapā.
    -  Režģa kolonna ar nereaģētu paplašināmo kontroli.

    Kad lietotājs pirmo reizi sastopas ar vienu no šīm situācijām, tiks parādīts ziņojums par lapas atsvaidzināšanu. Kad parādās šis ziņojums, lapa turpinās izmantot esošo režģi visiem lietotājiem līdz nākamās preces versijas atjaunināšanai. Šo scenāriju labākai apstrādei, lai varētu izmantot jauno režģi, tiks apsvērta turpmāka atjaunināšana.     

### <a name="fixed-as-part-of-10013"></a>Fiksēta kā daļa no 10.0.13

-  [Defekts 470173] Neaktīvo rindu izvēles rūtiņas tiek pārslēgtas, kad tiek noklikšķināts uz šūnas laukā
-  [Defekts 474848] Uzlabotie priekšskatījumi ar režģiem netiek rādīti
-  [Defekts 474851] Hipersaites atsauces grupas vadīklās nedarbojas 
-  [Defekts 471777] Nevar atlasīt laukus režģī, lai rediģētu vai izveidotu mobilo lietotni
-  [KB 4569441] Problēmas, atveidojot vairāku kolonnu kartīšu sarakstus, rīku padomus uz attēliem un displeju opcijas dažos laukos
-  [KB 4575279] Ne visas iezīmētās rindas tiek dzēstas Virsgrāmatas žurnālā
-  [KB 4575233] Displeja opcijas pēc pārcelšanās uz citu rindu netiek atjaunotas
-  [KB 4571095] Preču saņemšanas grāmatošana notiek, nejauši nospiežot taustiņu Enter (pareiza lapas noklusējuma darbības apstrāde)
-  [KB 4575437] Pārlūks ar rediģējamām vadīklām negaidīti aizveras
-  [KB 4569418] Dublēta rinda, kas izveidota pasūtījuma grafika formā
-  [KB 4575435] Uzlabotais priekšskatījums dažreiz saglabājas pat tad, ja peles rādītājs neatrodas lauka tuvumā
-  [KB 4575434] Pārlūks netiek filtrēts, ja lauks ir modificēts
-  [KB 4575430] Vērtības paroļu laukos netiek paslēptas režģī
-  [KB 4569438] "Apstrāde ir apturēta pārbaudes problēmas dēļ" parādās pēc rindu iezīmēšanas, kamēr tiek sakārtotas piegādātāja darbības
-  [KB 4569434] Atsvaidzinot juridisko personu formu, tiek iegūts mazāk ierakstu
-  [KB 4575297] Veicot rediģēšanu un tabulēšanu režģī, fokuss turpina pārvietoties uz uzdevuma reģistrētāja rūti
-  [KB 4566773] Labojumu darbības, kas dokumenta darbību vaicājumā netiek rādītas kā negatīvas 
-  [KB 4575288] Atlasot apmali starp rindām vienkāršā sarakstā, fokuss tiek atiestatīts uz aktīvo rindu
-  [KB 4575287] Fokuss neatgriežas pirmajā kolonnā, kad izmanto lejupvērsto bultiņu, lai izveidotu jaunu rindu žurnālos
-  [KB 4564819] Nevar dzēst rindas brīvā teksta rēķinā (jo datu avots ChangeGroupMode=ImplicitInnerOuter)
-  [KB 4563317] Rīku padomi/uzlabotie priekšskatījumi netiek parādīti attēliem

### <a name="fixed-as-part-of-10012"></a>Fiksēta kā daļa no 10.0.12

- [KB 4558545] Tabulas vadīklas neatjaunina parādīto vienumu saturu.
- [KB 4558570] Krājumi joprojām tiek parādīti lapā pēc tam, kad ieraksts ir dzēsts.
- [KB 4558572] Stils, kas ir saistīts ar Saraksta paneli **ExtendedStyle**, netiek lietots.
- [KB 4558573] Validācijas kļūdas nevar noteikt, ja nepieciešamās izmaiņas ir ārpus režģa.
- [KB 4558584] Negatīvie skaitļi netiek atveidoti pareizi.
- [KB 4560726] Pēc pārslēgšanās starp sarakstiem, izmantojot saraksta skata vadīklu, rodas "neparedzēta klienta kļūda".
- [KB 4562141] Režģa indeksi tiek izslēgti pēc jauna ieraksta pievienošanas.
- [KB 4562151] Uzdevumu reģistrētāja opcijas **Apstiprināt** un **Kopēt** nav pieejamas datuma/koda vadīklām. 
- [KB 4562153] Vairākas atlases izvēles rūtiņas nav redzamas saraksta/groza režģī.
- [KB 4562646] Dažkārt pēc vairāku atlases rindu atlasīšanas režģī nevar noklikšķināt ārpus režģa.
- [KB 4562647] Fokuss tiek atiestatīts uz pirmo vadīklu dialoglodziņā **Publicēt**, kad drošības lomu režģī tiek pievienota jauna rinda.
- [KB 4563310] Uzlabotais priekšskatījums netiek aizvērts pēc rindas maiņas.
- [KB 4563313] pārlūkā Internet Explorer, uzmeklēšanā atlasot vērtību, rodas "neparedzēta klienta kļūda".
- [KB 4564557] Pārlūki un nolaižamās izvēlnes netiek atvērtas programmā Internet Explorer
- [KB 4563324] Pēc darbvietas **Personāla vadība** atvēršanas nedarbojas navigācija.

### <a name="fixed-as-part-of-10011"></a>Fiksēta kā daļa no 10.0.11

- [Problēma 432458] Tukšas vai dublētas rindas tiek rādītas dažu pakārtoto kolekciju sākumā.
- [KB 4549711] Rindas maksājuma priekšlikumā nevar noņemt pareizi pēc tam, kad jaunā režģa kontrole ir iespējota.
- [KB 4558374] Nevar izveidot ierakstus, kas pieprasa polimorfisma selektora dialoglodziņu.
- [KB 4558375] Palīdzības teksts netiek uzrādīts jaunā režģa kolonnās.
- [KB 4558376] Saraksta paneļa režģi netiek atveidoti pareizā augstumā Internet Explorer.
- [KB 4558377] Dažām lapām netiek atveidoti kombinētā lodziņa kolonnu **SizeToAvailable** platumi.
- [KB 4558378] Detalizētā izrakstīšanās reizēm atver nepareizo ierakstu.
- [KB 4558379] Kļūda rodas, ja tiek atvērti pārlūki, kur **ReplaceOnLookup**=**Nē**.
- [KB 4558380] Pieejamā vieta režģī netiek aizpildīta uzreiz pēc tam, kad lappuses daļa ir sakļauta.
- [KB 4558381] Negatīvie skaitļi netiek atveidoti pareizi/lietotāji dažreiz iestrēgst pēc apstiprināšanas problēmu konstatēšanas.
- [KB 4558382] Rodas neparedzētas klienta kļūdas.
- [KB 4558383] Pēc pēdējā ieraksta dzēšanas vadīklas ārpus režģa netiek atjauninātas.
- [KB 4558587] Atsauces grupas, kurām ir kombinētie lodziņi aizstāšanas laukos, nerāda vērtības.
- [KB 4562143] Lauki netiek atjaunināti pēc rindas maiņas/režģa apstrādes, kas tiek iestrēdzis pēc rindas dzēšanas.
- [KB 4562645] Rodas izņēmums, ja tiek atvērts pārlūks, kamēr tiek izpildīti attālās servera administrēšanas rīku (RSAT) testi.

### <a name="fixed-as-part-of-10010"></a>Fiksēta kā daļa no 10.0.10

- [Problēma 414301] Daži dati no iepriekšējām rindām pazūd, kad tiek izveidotas jaunas rindas.
- [Defekts 417044] Saraksta stila režģiem nav neviena tukša režģa ziņojuma.
- [KB 4539058] Daži režģi (parasti uz kopsavilkuma cilnēm) dažreiz netiek atveidoti (bet tie tiks atveidoti, ja attālināt).
- [KB 4549734] Aktīvās rindas netiek apstrādātas kā atzīmētas, ja kolonna iezīmēšana ir paslēpta.
- [KB 4549796] Vērtības nevar rediģēt režģī, kad tā ir skatījuma režīmā.
- [KB 4558367] Mainot rindas, teksta izvēle nav konsekventa.
- [KB 4558368] Vairāku līmeņu izvēle, izmantojot tastatūru, ir atļauta vienas atlases scenārijā.
- [KB 4558369] Hierarhiskajā režģī pazūd statusa attēli.
- [KB 4558370] Jauna rinda netiek ritināta uz skatu.
- [KB 4558372] Jaunais režģis iestrēgst apstrādes režīmā, ja kolonnu skaits, kas tiek ielīmēts, pārsniedz atlikušo kolonnu skaitu režģī.
- [KB 4562631] Laika vērtības nav pareizi formatētas.

### <a name="quality-update-for-1009platform-update-33"></a>Kvalitātes atjauninājums 10.0.9./ Platformas atjauninājums 33

- [KB 4550367] Laika vērtības nav pareizi formatētas.
