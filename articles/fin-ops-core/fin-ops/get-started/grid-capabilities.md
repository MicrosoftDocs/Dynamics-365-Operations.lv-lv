---
title: Režģa iespējas
description: Šajā rakstā ir aprakstītas vairākas režģa kontroles jaudīgas funkcijas. Lai piekļūtu šīm iespējām, ir jābūt iespējotam jaunajam režģa līdzeklim.
author: jasongre
ms.date: 08/29/2022
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
ms.openlocfilehash: 096f441d39dde0f322ed117ab35a6a4641a38a93
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405470"
---
# <a name="grid-capabilities"></a>Režģa iespējas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Jaunā režģa kontrole piedāvā daudzas noderīgas un jaudīgas iespējas, ko var izmantot, lai uzlabotu lietotāju produktivitāti, izveidotu vairāk interesantu jūsu datu skatu un iegūtu izsmeļošu ieskatu datos. Šajā rakstā ir apskatītas tālāk norādītās iespējas 

- Aprēķināto vērtību rādīšana 
- Rakstīšana pirms sistēmas
- Matemātisko izteiksmju novērtēšana 
- Tabulu datu grupēšana (aktivizēta atsevišķi, izmantojot funkciju **Grupēšana režģos**)
- Iesaldēšanas kolonnas (aktivizē atsevišķi, izmantojot funkciju **Iesaldēšanas kolonnas režģī**)
- Automātiski ietilpināt kolonnas platumu
- Izstiepjamas kolonnas

## <a name="showing-calculated-values"></a>Aprēķināto vērtību rādīšana
Finanšu un operāciju programmās lietotāji var skatīt aprēķināto vērtību katrai režģa skaitliskai kolonnai. Kājenes sadaļa režģa apakšā parāda šīs aprēķinātās vērtības.

[![Aprēķināto vērtību rādīšana režģos](./media/grids-aggregation.png)](./media/grids-aggregation.png)

Versijās pirms 10.0.29 kopsumma ir vienīgā atbalstītā aprēķinātā vērtība. Tomēr, saskaņā ar versiju 10.0.29 pēc **paplašinātā** režģa apkopošanas iespēju funkcijas iespējošanas lietotāji var izvēlēties no šādām četrām aprēķinātajām vērtībām:

- Minimālā
- Maksimālā
- Kopā
- Vidējā

Vienā kolonnā var parādīt tikai vienu aprēķinātās vērtības tipu. Tomēr katru režģa kolonnu var konfigurēt, lai rādītu citu aprēķinātās vērtības tipu.

### <a name="showing-the-grid-footer"></a>Režģa kājenes parādīšana
Katras tabulas režģa apakšā ir kājenes apgabals finanšu un operāciju programmās. Kājenē var tikt parādīta vērtīga informācija, kas saistīta ar datiem, kas parādās režģī. Tālāk ir sniegti daži šādas informācijas piemēri:

- Atlasīto rindu skaits tabulā (ja ir atlasīts vairāk nekā viens ieraksts)
- Aprēķinātās vērtības konfigurēto ciparu kolonnu lejasdaļā (piemēram, kopsummas)
- Datu kopā ietverto rindu skaits 

Pēc noklusējuma šī kājene ir paslēpta, taču to var ieslēgt. Lai parādītu režģa kājeni, atlasiet pogu **Režģa opcijas** režģa galvenē, tad atlasiet opciju **Rādīt kājeni**. Pēc tam, kad būsiet ieslēdzis kājeni noteiktam režģim, šis iestatījums atgādinās par sevi, līdz lietotājs izvēlēsies slēpt kājeni. Lai slēptu kājeni, atlasiet **Slēpt kājeni** **Režģa opciju** izvēlnē.

### <a name="specifying-columns-with-calculated-values"></a>Kolonnu ar aprēķinātām vērtībām norādīšana
Pašlaik neviena kolonna pēc noklusējuma nerāda aprēķinātās vērtības. Tā vietā iestatījums tiek uzskatīts par vienreizēju aktivitāti, piemēram, kolonnu platuma pielāgošana režģos. Kad norādīsiet, ka vēlaties skatīt kolonnas aprēķināto vērtību, šis iestatījums tiks atcerētiess nākamajā lapas apmeklējuma reizē.

Pastāv divi kolonnas konfigurēšanas veidi aprēķinātās vērtības rādītājs:

- Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) kolonnā, kurai vēlaties skatīt aprēķināto vērtību. Ja ir **iespējots paplašinātās režģa** apkopošanas iespēju līdzeklis, atlasiet **skatīt kolonnu kopsummas** un pēc tam atlasiet vēlamo aprēķināto vērtību. Ja šī funkcija nav iespējota, atlasiet Kopsumma **šajā kolonnā**. Šī darbība izraisa trīs notikumu rašanos:

    1. Režģa kājene kļūst redzama. 
    2. Tiek saglabāta jūsu izvēle aprēķinātās kolonnas vērtības skatīšanai. 
    3. Vēlamais aprēķins tiek uzsākts kolonnai un visām citām kolonnām, kuras iepriekš konfigurējāt, lai parādītu aprēķināto vērtību. Aprēķināto vērtību jums nepieciešamais laiks ir atkarīgs no datu kopas lieluma.

- Kad kājene ir redzama, kājenes apgabalā, kurai vēlaties skatīt aprēķināto vērtību, atlasiet Rādīt kopsummu (**·** **vai** Atlasīt aprēķināto vērtību, **ja** ir iespējots paplašinātās režģa apkopošanas iespēju līdzeklis). Ja nav konfigurētu kolonnu, šī poga būs pieejama kājenē visās skaitliskās kolonnās.

    Pēc tam, kad ir konfigurēta vismaz viena kolonna, lai parādītu aprēķināto vērtību, **poga** Rādīt kopsummu (**vai** Atlasīt aprēķināto vērtību) būs pieejama tikai uz pretfokusu vai fokusu. Izvēloties pogu, tiek saglabāta tikai jūsu izvēle aprēķinātās vērtības skatīšanai kolonnā, tādējādi preference tiek piemērota turpmākās lapas apmeklējumu laikā. Kājenē šis stāvoklis tiek norādīts ar svītru, kas parādās kolonnā. (Ņemiet vērā, ka aprēķinātā vērtība nekavējoties parādīsies, ja datu kopa ir pietiekami maza.)

Ja tiek pieļauta kļūda un vairs nevēlaties skatīt aprēķināto vērtību noteiktā kolonnā, atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) kolonnā un pēc tam atlasiet **Paslēpt** kopsummu (**vai Skatīt kolonnu kopsummas Nav \>** **, ja ir iespējota paplašinātās režģa apkopošanas** iespēju funkcija). Alternatīvi šīs kolonnas **kājenē** **atlasiet Slēpt kopsummu** (vai Slēpt aprēķināto vērtību). Šī izvēle tiks saglabāta arī turpmākiem lapas apmeklējumiem. 

### <a name="calculating-aggregate-values"></a>Aprēķina uzkrātās vērtības
Kad dodieties uz lapu, kur kājenē ir redzama, un kolonnas jau ir konfigurētas aprēķināto vērtību parādītai, šīs vērtības var nebūt parādītas kājenē. Darbība ir atkarīga no datu kopas lieluma lapā. Ja datu kopa ir pietiekami maza, aprēķinātās vērtības kopā ar rindu skaitu datu kopā tiks parādītas automātiski. Ja kājenē zem konfigurētajām kolonnām ir domuzīmes, datu kopa ir pārāk liela, lai sistēma nekavējoties rādītu aprēķinātās vērtības. Šajā gadījumā, lai aprēķinātu vērtības, ir nepieciešama skaidri formulēta darbība. Lai aprēķinātu vērtības, kājenē **atlasiet** pogu Aprēķināt. Pēc izvēles atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) kolonnā, kurai vēlaties skatīt kopsummu, **un** pēc tam atlasiet Kopsumma šo kolonnu (**vai Skatīt kolonnu kopsummas un pēc tam vēlamo aprēķināto vērtību, ja ir iespējots paplašinātās režģa apkopošanas** **iespēju** līdzeklis).

Ja aprēķina veikšanai nepieciešams ilgs laiks, operāciju var atcelt jebkurā laikā, atlasot **Atcelt**. Dažreiz datu kopa būs pārāk liela, lai aprēķinātu kopējās vērtības (limitu, ko ierobežo jūsu organizācija). Šādā gadījumā tā vietā saņemsiet paziņojumu, lai filtrētu datus vairāk.

> [!NOTE]
> Sistēmas administratori **var** **modificēt limitu ierakstu skaitam, kas ir pieejami apkopojumu aprēķināšanai, koriģējot maksimālo lokālo ierakstu skaitu katram režģa parametram klienta veiktspējas opciju** lapā. Noklusētā vērtība ir 25 000 ieraksti. Administratoriem ir jābūt uzmanīgiem, koriģējot šo vērtību, jo pārāk liela vērtība var saglabāt lietotāja datorā pieejamo atmiņas daudzumu. Ieteicams, lai vērtība nepārsniegtu 50 000 ierakstus.

Aprēķinātās vērtības tiks automātiski atjauninātas, atjauninot, dzēšot vai veidojot rindas datu kopā.

## <a name="typing-ahead-of-the-system"></a>Rakstīšana pirms sistēmas
Daudzos biznesa scenārijos spēja ātri ievadīt datus sistēmā ir ļoti svarīga. Pirms jaunas režģa kontroles ieviešanas lietotāji var mainīt datus tikai pašreizējā rindā. Tāpēc pēc izmaiņu veikšanas rindā lietotāji nevarēja pārslēgties uz citu rindu vai izveidot jaunu rindu, kamēr sistēma veiksmīgi validēja izmaiņas pašreizējā rindā un (rindas izveides gadījumā) darbojās visas loģikas, kas ir saistīta ar jaunas rindas izveidi. Lai palīdzētu samazināt laiku, ko lietotāji tērē, gaidot šo operāciju pabeigšanu, un palīdzētu uzlabot lietotāja produktivitāti, jaunais režģis pielāgo šīs darbības tā, lai tās būtu asinhronas. Lietotāji var izveidot jaunas rindas vai pārvietot uz citām rindām, lai veiktu izmaiņas iepriekšējās rindu apstiprināšanas un rindu izveides loģikas gaidīšanas laikā. 

[![Ierakstot pirms sistēmas.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Lai atbalstītu šo jauno uzvedību, rindas statusam ir pievienota jauna kolonna pa lbabi no rindas atlases kolonnas, kad režģis ir rediģēšanas režīmā. Šī kolonna norāda vienu no šiem statusiem:

- **Tukšs** – nav statusa attēla, kas norāda, ka sistēma ir veiksmīgi saglabājusi rindu.
- **Gaida apstrādi** — šis statuss norāda, ka izmaiņas rindā vēl nav saglabātas serverī, bet ir pārstrādājamo izmaiņu rindā. Pirms darbības veikšanas ārpus režģa ir jāgaida, kamēr tiks apstrādātas visas gaidošās izmaiņas. Turklāt teksts šajās rindās ir slīprakstā, lai norādītu rindu nesaglabāto statusu. 
- **Nederīgs stāvoklis** — šis statuss norāda, ka rindas apstrādes laikā tika izraisīts kāds brīdinājums vai ziņojums, un tas, iespējams, ir liedzis sistēmai saglabāt šīs rindas izmaiņas. Vecajā režģī, ja darbība bija nesekmīga, jūs tikāt aizvests atpakaļ uz rindu, lai nekavējoties labotu problēmu. Tomēr jaunajā režģī tiek paziņots, ka ir konstatēta apstiprināšanas problēma, bet varat izlemt, kad vēlaties labot rindas problēmas. Kad esat gatavs labot problēmu, varat manuāli pārvietot fokusu uz rindu. Kā alternatīvu jūs varat izvēlēties darbību **Labot šo problēmu**. Šī darbība nekavējoties pārvieto fokusu uz rindu, kurā ir problēma, un ļauj veikt labojumus režģī vai tā ārpusē. Ņemiet vērā, ka turpmākās gaidošās rindas tiek apturētas, līdz šis apstiprināšanas brīdinājums tiek novērsts. 
- **Apturēts** — šis statuss norāda, ka apstrāde ar serveri ir apturēta, jo rindas validācija izraisīja uznirstošo dialoglodziņu, kas pieprasa lietotāja ievadi. Tā kā lietotājs, iespējams, ievada datus citās rindās, uznirstošais dialoglodziņš netiek uzreiz parādīts šim lietotājam. Tā vietā tas tiks parādīts, kad lietotājs izvēlas atsākt apstrādi. Šim statusam ir pievienots paziņojums, kas informē lietotāju par šo situāciju. Paziņojums ietver darbību **Turpināt apstrādi**, kas izraisīs uznirstošo dialoglodziņu.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Atšķirības, ievadot datus pirms sistēmas
Ievadot datus pirms tā, kur sistēma apstrādā, var gaidīt dažas datu ievades pieredzes izmaiņas:

- Jūs ievērosiet, ka nav uzmeklēšanas nolaižamo sarakstu, lauku vērtības netiks pārbaudītas pēc pāriešanas uz citu kolonnu tajā pašā rindā, un kolonnas sākotnēji nerāda noklusējuma vērtības. Šāda situācija rodas, veidojot vai atjauninot pirms sistēmas. Tomēr pēc sistēmas līdz vietai, kur pašlaik rediģējat, standarta pieredze atsāksies. Ja jūs veicāt izmaiņas laukā, kas parasti saņem noklusējuma vērtību, jūsu izmaiņas ignorē noklusēto lauka vērtību, kad serveris sāk apstrādāt rindu.
- Ja izveidojat jaunu rindu, izmantojot taustiņu ar **lejupvērsto bultiņu**, visas kolonnas režģī tiks parādītas kā rediģējamas. Pēc noklusējuma fokuss tiks novietots pirmās kolonnas jaunajā rindā. Šī kolonna, iespējams, nav tā pati kolonna, kas saņēma sākotnējo fokusu mantojuma režģī, vai tā pati kolonna, **kas saņem fokusu pēc pogas Jauns** atlases. Jūsu organizācija var pielāgot sistēmu un mainīt kolonnu, kas saņem sākotnējo fokusu, ja ir **atlasīta lejupvērstās** bultiņas atslēga. Papildinformāciju skatiet slejas [norādīšanai, kura saņems sākotnējo fokusu, veidojot jaunas rindas, izmantojot sadaļas Ar lejupvērsto bultiņu taustiņu](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key). Neatkarīgi no tā, vai ir iespējams izmantot personalizēšanu, lai optimizētu katru datu ievades režģi. It īpaši varat pārkārtot laukus, lai pirmā kolonna būtu kolonna, kurā vēlaties sākt ievadīt datus. Iespējams, ka vēlēsieties arī vispārīgi pārkārtot laukus datu ievadei, samazināt cilnes apturēšanas laiku un slēpt visus laukus, kas nav nepieciešami datu ievadei šajā skatījumā.

### <a name="pasting-from-excel"></a>Ielīmēšana no Excel
Lietotāji vienmēr ir spēt eksportēt datus no finanšu un operāciju programmu režģiem Microsoft Excel, izmantojot **mehānismu Eksportēt uz Excel**. Tomēr spēja ievadīt datus pirms sistēmas ļauj jaunajam režģim atbalstīt tabulu kopēšanu no Excel un to tiešo ielīmēt finanšu un operāciju programmu režģos. Režģa šūna, no kuras tiek sākta ielīmēšanas darbība, nosaka, kur kopēto tabulu sāk ielīmēt. Režģa saturs tiek pārrakstīts ar kopētās tabulas saturu, izņemot divos gadījumos:

- Ja kolonnu skaits kopētajā tabulā pārsniedz kolonnu skaitu, kas paliek režģī, sākot no ielīmēšanas vietas, lietotājam tiek paziņots, ka papildu kolonnas ir ignorētas. 
- Ja rindu skaits kopētajā tabulā pārsniedz rindu skaitu režģī, sākot no ielīmēšanas vietas, esošās šūnas tiek pārrakstītas ar ielīmēto saturu, un visas papildu rindas no kopētās tabulas tiek iespraustas kā jaunas rindas režģa apakšā. 

## <a name="evaluating-math-expressions"></a>Matemātisko izteiksmju novērtēšana
Produktivitātes veicināšanai lietotāji režģa ciparu šūnās var ievadīt matemātiskas formulas. Viņiem nav jāveic aprēķini programmā ārpus sistēmas. Piemēram, ja ievadāt **=15\*4** un pēc tam nospiežat taustiņu **TAB**, lai izietu no lauka, sistēma novērtēs izteiksmi un saglabās vērtību **60** laukam.

[![Novērtējamās para&s izteiksmes.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Lai sistēma atpazītu vērtību kā izteiksmi, sāciet vērtību ar vienādības zīmi (**=**). Papildinformāciju par atbalstītajiem operatoriem un sintaksi skatiet [Atbalstītie matemātiskie simboli](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

No versijas 10.0.29 spēja novērtēt elektroniskās izteiksmes skaitliskās vadīklās ir paplašināta un tagad ir pieejama arī ārpus režģa.

## <a name="grouping-tabular-data"></a>Tabulas datu grupēšana
Biznesa lietotājiem bieži nepieciešams veikt datu ekspromtana analīzi. Lai arī Microsoft Excel šo analīzi var veikt, eksportējot datus uz un izmantojot koptabulas, **grupēšanas režģu funkcija, kas ir atkarīga no jaunās režģa kontroles funkcijas, ļauj lietotājiem organizēt savus tabulas** datus ļoti dažādos finanšu un operāciju programmu veidos. Tā kā šī funkcija paplašina **funkciju** Aprēķinātās vērtības, **grupēšana** ļauj iegūt datos saprotamus priekšstatus, grupas līmenī sniedzot aprēķinātas vērtības (piemēram, apakšsummas).

[![Datu grupēšana režģī.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Lai izmantotu šo funkciju, ar peles labo pogu noklikšķiniet uz kolonnas, pēc kuras vēlaties grupēt, un atlasiet **Grupēt pēc šīs kolonnas**. Veicot šo darbību, dati tiks šķiroti pēc atlasītās kolonnas, režģa sākumā tiks pievienota jauna kolonna **Grupēt pēc** un katras grupas sākumā tiks ievietotas “galvenes rindas”. Šīs virsraksta rindas sniedz tālak norādīto informāciju par katru grupu.

- Grupas datu vērtība 
- Kolonnas nosaukums (šī informācija ir īpaši noderīga, ja jums ir vairāki grupēšanas līmeņi.)
- Datu rindu skaits šajā grupā
- Aprēķinātās vērtības visām konfigurētajām kolonnām (piemēram, apakšsummas, ja kolonna ir konfigurēta, lai parādītu kopsummu)

Ar [iespējotus](saved-views.md) saglabātos skatus, varat saglabāt grupēšanu kā daļu no skata lapām, kas ļauj saglabāt vaicājumus skatos. Piemēram, tiem, kam ir lieli skatījumu atlasītāji. Papildinformāciju [skatiet sadaļā Pārslēgšanās](saved-views.md#switching-between-views) starp skatījumiem. 

### <a name="multiple-levels-of-grouping"></a>Vairāki grupēšanas līmeņi
Kad dati ir grupēti pēc vienas kolonnas, datus var grupēt pēc citas kolonnas, vēlamajā kolonnā atlasot **Grupēt pēc šīs kolonnas**. Šo procesu var atkārtot, kamēr nav 5 ligzdotu grupēšanas līmeņu, kas ir maksimālais atbalstītais dziļums. Šajā brīdī vairs nevarēsit grupēt pēc papildu kolonnām.

Jebkurā brīdī varat noņemt grupēšanu jebkurā kolonnā, ar peles labo pogu noklikšķinot uz šīs kolonnas un atlasot **Atgrupēt**. Varat arī noņemt grupēšanu no visām kolonnām, atlasot **Režģa opcijas** un pēc tam atlasot **Atgrupēt visu**.

### <a name="sorting-grouped-data"></a>Grupēto datu kārtošana
Pēc datu grupēšanas pēc vienas vai vairākām kolonnām, jebkuras grupēšanas kolonnas kārtošanas virzienu var mainīt, izmantojot atbilstošu kolonnas virsrakstu. 

Ja kārtojat kolonnā, kas nav grupēta, grupēšana netiek neskarta. Dati tiek kārtoti katrā grupā, pamatojoties uz atlasīto kolonnu.

### <a name="expanding-and-collapsing-groups"></a>Grupu paplašināšana un sakļaušana
Sākotnējai datu grupēšanai būs paplašinātas visas grupas. Varat izveidot kopsavilkuma skatījumus datiem, sakļaujot atsevišķas grupas, vai arī varat izmantot grupas paplašināšanu un sakļaušanu, lai palīdzētu pārvietoties pa datiem. Lai paplašinātu vai sakļautu grupu, atbilstošajā grupas virsraksta rindā atlasiet pogu Chevron (>). Ņemiet vērā, ka atsevišķu grupu paplašināšanas/sakļaušanas stāvoklis personalizācijā **netiek** saglabāts.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Rindu atlasīšana un atlases noņemšana grupas līmenī
Tāpat kā visas režģa rindas var atlasīt (vai noņemt atlasi), atzīmējot izvēles rūtiņu režģa pirmās kolonnas augšdaļā, var arī ātri atlasīt (vai noņemt atlasi) visas grupas rindas, atzīmējot izvēles rūtiņu atbilstošajā grupas galvenes rindā. Grupas galvenes rindas izvēles rūtiņa vienmēr atspoguļo šīs grupas rindu pašreizējo atlases stāvokli neatkarīgi no tā, vai ir atlasītas visas rindas, nav atlasīta neviena rinda vai ir atlasītas tikai dažas rindas.

### <a name="hiding-column-names"></a>Kolonnu nosaukumu paslēpšana
Grupējot datus, noklusējuma darbība ir parādīt kolonnas nosaukumu grupas galvenes rindā. Varat izvēlēties neiekļaut kolonnas nosaukumu grupu galvenes rindās, atlasot **Režģa opcijas** > **Paslēpt grupas kolonnas nosaukumu**.

### <a name="grouping-on-date-and-time-columns"></a>Grupēšana datumu un laika kolonnās
Ja grupēsiet laukus Datums vai Datums un Laiks, varat grupēt pēc gada, mēneša vai dienas. Grupa "vērtība" atbilstošajā virsraksta rindā saskanēs ar formātu no šī lauka. Turklāt laukiem DateTime un Laiks varat grupēt pēc stundas, minūtes vai otrā.

> [!IMPORTANT]
> Lietotāji pašlaik nevar pievienot grupēšanas kolonnu pēc tam, kad viņi ir sagrupēti datuma vai laika kolonnas segmentā.

## <a name="freezing-columns"></a>Iesaldēšanas kolonnas
Dažas kolonnas režģī var būt pietiekoši nozīmīgas kontekstam, ko nevēlaties ritināt ārpus skata. Tā vietā, iespējams, vēlēsieties, lai vērtības šajās kolonnās vienmēr būtu redzamas. Iesaldēšanas **kolonnas režģa** funkcija nodrošina lietotājiem šādu elastīgumu. 

[![Iesaldēšanas kolonnas režģī.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Lai kolonnu iesaldētu, ar peles labo pogu noklikšķiniet kolonnas virsrakstā un pēc tam atlasiet **Iesaldēt kolonnu**. Pirmo reizi pabeidzot šo soli, atlasītā kolonna kļūst par pirmo kolonnu un vairs neritinās skatu. Visas sekojošās kolonnas, kas sasaldētas, tiks pievienotas pēdējās iesaldētās kolonnas labajā pusē. Lai pārkārtotu iesaldētās kolonnas pēc nepieciešamības, varat izmantot standarta funkcionalitāti Pārvietot. Tomēr iesaldētās kolonnas nevar pārvietot, lai tās parādītos starp atsaldēto kolonnu kopu. Tomēr iesaldētās kolonnas nevar pārvietot, lai tās parādītos starp atsaldēto kolonnu kopu.

Lai kolonnu atsaldētu, ar peles labo pogu noklikšķiniet kolonnas virsrakstā un pēc tam atlasiet **Atsaldēt kolonnu**. 

Ievērojiet, ka rindu atlase un rindu statusa kolonnas jaunajā režģī vienmēr tiek iesaldētas kā pirmās divas kolonnas. Tādējādi, kad šīs kolonnas ir iekļautas režģī, tās vienmēr būs redzamas lietotājam neatkarīgi no horizontālās ritināšanas pozīcijas režģī. Šīs divas kolonnas nevar pārkārtot.

## <a name="autofit-column-width"></a>Automātiski ietilpināt kolonnas platumu
Tāpat kā programmā Excel lietotāji var piestāt, lai kolonna tiktu automātiski mainīta atbilstoši saturam, kas pašlaik tiek rādīts tajā. Vienkārši dubultskāršs (vai dubultklikšķis) izmēru maiņas turi kolonnā. Vai arī novietojiet fokusu kolonnas virsrakstā un pēc tam atlasiet **taustiņu A** (automātiskai ietilpināšanai).

## <a name="frequently-asked-questions"></a>Bieži uzdotie jautājumi
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kā iespējot jauno režģa kontroli manā vidē? 

**Jaunā režģa kontroles** līdzeklis ir pieejams tieši Līdzekļu pārvaldībā jebkurā vidē. Pēc līdzekļa iespējošanas līdzekļu pārvaldībā, visas turpmākās sesijas izmantos jauno režģa kontroli. 

Šī funkcija sāka būt aktivizēta pēc noklusējuma versijā 10.0.21. 2022. gada oktobrī tas kļūst obligāts.

## <a name="developer-topics"></a>Izstrādātāju tēmas

### <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Attīstītājs] Atteikšanās no atsevišķām lapām, izmantojot jauno režģi 
Ja jūsu organizācija atklāj lapu, kurā ir dažas problēmas, izmantojot jauno režģi, ir pieejams API, lai ļautu atsevišķai formai izmantot mantoto režģa vadīklu, joprojām ļaujot pārējai sistēmai izmantot jauno režģa vadīklu. Lai izņemtu atsevišķu lapu no jaunā režģa, pievienojiet šādu izsaukuma ierakstu `super()` formas `run()` metodē.

```this.forceLegacyGrid();```

Šis API tiks aprēķināts līdz ar nolietojumu, lai varētu noņemt mantojuma režģa kontroli. Tomēr tas būs pieejams vismaz 12 mēnešus pēc nolietojuma aprēķina. Ja kādai problēmai nepieciešams izmantot šo API, ziņojiet par to Microsoft.

#### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Lapas piespiedu jaunā režģa izmantošanai pēc iepriekšējas iziešanas no režģa
Ja esat izvēlējies atsevišķu lapu, lai neizmantotu jauno režģi, iespējams, vēlēsieties pēc tam atkārtoti aktivizēt jauno režģi pēc pakārtoto problēmu atrisināšanas. Lai to paveiktu, vienkārši ir jānoņem izsaukums `forceLegacyGrid()`. Izmaiņas stāsies spēkā tikai pēc tam, kad notiks kāda no šīm darbībām:

- **Vides atkārtota izvietošana**: kad vide tiek atjaunināta un atkārtota izvietošana, tabula, kurā tiek glabātas lapas, kas ir aizstātas ar jauno režģi (FormControlReactGridState) tiek automātiski notīrīta.
- **Manuāla tabulas tīrīšana**: izstrādes scenārijiem ir jāizmanto SQL, lai notīrītu tabulu FormControlReactGridState un pēc tam restartētu AOS. Šī darbību kombinācija atiestatīs lapu kešatmiņu, kuras izvēlējās jaunajam režģim.

### <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Izstrādātājs] Atsevišķu režģu izvēle ārpus ierakstīšanas iespējas pirms sistēmas iespējas
Daži scenāriji ir radušies, kas *neaizdod* sevi darbam, izmantojot ierakstot pirms režģa sistēmas iespējas. (Piemēram, daži kodi, kas tiek izraisīti, kad rinda ir validēta, izraisa datu avota izpēti, un tādējādi izpēte var sabojāt nesaistītos rediģējumus esošajās rindās.) Ja jūsu organizācija atklāj šādu scenāriju, ir pieejams API, kas ļauj izstrādātājam izvēlēties atsevišķu režģi no asinhronās rindu apstiprināšanas un atgriezties pie mantojuma uzvedības.

Ja asinhronā rindas apstiprināšana režģī ir atspējota, lietotāji nevar izveidot jaunu rindu vai pārvietot režģī uz citu esošo rindu, kamēr pašreizējā rindā ir validācijas problēmas. Šīs darbības rezultātā tabulas no Excel nevar ielīmēt finanšu un operāciju režģī.

Lai izvēlētos atsevišķu režģi no asinhronās rindu apstiprināšanas, `super()` pievienojiet formas metodē šādu `run()` izsaukumu.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Šo zvanu vajadzētu izsaukt tikai izņēmuma gadījumos, un tas nedrīkst būt visu režģu norma.
> - Nav ieteicams pārslēgt šo API izpildlaikā pēc formu ielādes.

### <a name="developer-size-to-available-width-columns"></a>[Izstrādātājs] Pielāgot pieejamo kolonnu platumu
Ja izstrādātājs jaunā režģa kolonnās iestata rekvizītu **WidthMode** uz **SizeToAvailable**, šīm kolonnām sākotnēji ir tāds pats platums, kāds tām būtu, ja rekvizīts būtu iestatīts uz **SizeToContent**. Tomēr tās izplešas, lai izmantotu jebkādu pieejamo papildu platumu režģī. Ja vairākām kolonnām rekvizīts ir iestatīts uz **SizeToAvailable**, visas šīs kolonnas koplieto jebkādu pieejamo papildu platumu režģī. Tomēr, ja lietotājs manuāli maina lielumu vienai no šīm kolonnām, tad kolonna kļūst statiska. Tās paliks šajā platumā un vairs neaizņems pieejamo papildu režģa platumu.

### <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Izstrādātājs] Tās kolonnas norādīšana, kura saņem sākotnējo fokusu, veidojot jaunas rindas, lietojot lejupvērsto bultiņu taustiņu
Kā tika apspriests [Atšķirības](#differences-when-entering-data-ahead-of-the-system), ievadot datus pirms sistēmas sadaļas, ja iespēja "Ierakstot pirms sistēmas" ir iespējota, un lietotājs izveido jaunu rindu, **izmantojot** taustiņu Ar lejupvērsto bultiņu, noklusējuma uzvedība tiek novietota jaunās rindas pirmajā kolonnā. Šī pieredze var atšķirties no pieredzes mantojuma režģī vai arī, ja ir **atlasīta** poga Jauns.

Lietotāji un organizācijas var izveidot saglabātus skatus, kas ir optimizēti datu ievadei. (Piemēram, var pārkārtot kolonnas tā, lai pirmā kolonna būtu tā, kurā vēlaties sākt ievadīt datus.) Turklāt no versijas 10.0.29 organizācijas var pielāgot šo uzvedību, izmantojot izvēlētāsControlOnCreate **()** metodi. Šī metode ļauj izstrādātājam norādīt kolonnu, kam jāsaņem sākotnējais fokuss, kad tiek veidota jauna rinda, izmantojot taustiņu **Ar lejupvērsto bultiņu**. Šis API paņem kontroles ID, kas atbilst kolonnai, kam jāsaņem sākotnējais fokuss.

### <a name="developer-handling-grids-with-non-react-extensible-controls"></a>[Izstrādātājs] Režģu apstrāde ar paplašināmām vadīklām, kas nav nodrīsamas
Ielādējot režģi, ja sistēma saskaras ar paplašināmu kontroli, kas nav balstīta uz paplašināmo kontroli, sistēma piestās mantojuma režģi atveidot. Kad lietotājs pirmo reizi saskarsies ar šo situāciju, tiks parādīts ziņojums ar norādi, ka lapa ir jāatsvaidzina. Pēc tam šī lapa ielādēs mantojuma režģi automātiski bez turpmākiem paziņojumiem lietotājiem līdz nākamajai sistēmas atjaunināšanai. 

Lai pavisam atrisinātu šo situāciju, paplašināmie kontroles autori var izveidot kontroles versiju to vadībai, kas tiks lietota režģī.  Pēc atjaunināšanas X++ **klase kontrolei var būt papildu klase ar atribūtu FormReactControlAttribute**, lai norādītu ar šo kontroli noslodzi Nodzēsiet saišķi. `SegmentedEntryControl` Skatiet klasi kā piemēru.  

## <a name="known-issues"></a>Zināmās problēmas
Šajā sadaļā tiek uzturēts saraksts ar zināmām problēmām jaunajai režģa kontrolei.

### <a name="open-issues"></a>Aktuālās problēmas
- Pēc **Jaunā režģa kontroles** līdzekļa iespējošanas dažas lapas turpinās izmantot esošo režģa kontroli. Tas notiks šādās situācijās:
 
    - [Atrisināti] Lapā ir karšu saraksts, kas tiek atveidots vairākās kolonnās.
        - Šī veida karšu sarakstu atbalsta Jauna režģa kontrole **, sākot** ar versiju 10.0.30. Var noņemt jebkuru forceLegacyGrid() lietošanu šim nolūkam. 
    - [Atrisināti] Lapā ir grupēts karšu saraksts.
        - Grupētie karšu saraksti tiek atbalstīti ar jaunu režģa **kontroli,** sākot ar versiju 10.0.30. Var noņemt jebkuru forceLegacyGrid() lietošanu šim nolūkam. 
    - [Atrisināti] Režģa kolonna, kurā nav no jauna paplašināma kontrole.
        - Paplašināmās kontroles var nodrošināt noslogotās kontroles versiju, kas tiks ielādēta, novietojot režģī un pielāgojot to kontroles definīciju, lai ielādētu šo kontroli, kad tā tiek lietota režģī. Papildinformāciju skatiet atbilstošajā izstrādātāja sadaļā. 

    Kad lietotājs pirmo reizi sastopas ar vienu no šīm situācijām, tiks parādīts ziņojums par lapas atsvaidzināšanu. Kad parādās šis ziņojums, lapa turpinās izmantot esošo režģi visiem lietotājiem līdz nākamās preces versijas atjaunināšanai. Šo scenāriju labākai apstrādei, lai varētu izmantot jauno režģi, tiks apsvērta turpmāka atjaunināšana.

- [KB 4582758] Ieraksti ir izplūduši, mainot tālummaiņu no 100 uz jebkuru citu procentuālo vērtību

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

