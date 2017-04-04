---
title: "MK aprēķinu grupas"
description: "Šajā rakstā ir sniegta informācija par materiālu komplektu (MK) aprēķinu grupām un to iestatīšanu. Lai izpildītu MK aprēķinu, ir jāiestata aprēķinu grupas un tās jāpiešķir atsevišķiem krājumiem, vai jāiestata noklusējuma aprēķinu grupa. MK aprēķināšanas laikā aprēķinu iestatījumi no aprēķinu grupas tad tiek izmantoti kā noklusējuma vērtības lapā MK aprēķins."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 893c6d42fc3de3e07d63f0ac61a287e81685cbad
ms.lasthandoff: 03/31/2017


---

# <a name="bom-calculations-groups"></a>MK aprēķinu grupas

Šajā rakstā ir sniegta informācija par materiālu komplektu (MK) aprēķinu grupām un to iestatīšanu. Lai izpildītu MK aprēķinu, ir jāiestata aprēķinu grupas un tās jāpiešķir atsevišķiem krājumiem, vai jāiestata noklusējuma aprēķinu grupa. MK aprēķināšanas laikā aprēķinu iestatījumi no aprēķinu grupas tad tiek izmantoti kā noklusējuma vērtības lapā MK aprēķins. 

Noklusējuma aprēķinu grupa ir nepieciešama lapā **Krājumu un noliktavas vadības parametri** vai precei raksturīga aprēķinu grupa ir nepieciešama lapā **Detalizēta informācija par izlaistajām precēm**. Sistēma vispirms meklē aprēķinu grupas iestatījuma **atbrīvo produkta detaļas** lapā. Ja tā neatrod aprēķinu grupu, tas izskatās **krājumu un noliktavu pārvaldības parametri** lapā. Ja sistēma nevar atrast aprēķinu grupa, lietotājs saņem kļūdas ziņojumu aprēķināšanas laikā. Aprēķinu grupa ietver politikas izmaksu cenas modelim, pārdošanas cenas modelim un brīdinājumu kontrolsarakstam. MK aprēķināšanas laikā aprēķinu iestatījumi no aprēķinu grupas tiek izmantoti kā noklusējuma vērtības lapā **MK aprēķins**.

## <a name="purposes-of-bom-calculation-groups"></a>MK aprēķinu grupu nolūki
MK aprēķinu grupu varat piešķirt krājumiem vairāku tālāk aprakstīto iemeslu dēļ.

-   Iestatot lauku **Izmaksu cenas modelis**, jūs norādāt iegādātā komponenta cenu seguma datu avotu ražoto krājumu plānoto izmaksu aprēķināšanas laikā. Daži ražotāji aprēķina plānotās izmaksas, izmantojot pirkšanas cenas tirdzniecības līgumus par iegādātajiem komponentiem vai citu pamatu, piemēram, pirkšanas cenas ierakstus kādā izmaksu aprēķināšanas versijā.
-   Iestatot lauku **Pārdošanas cenas modelis**, jūs norādāt, kā krājuma dati tiek izmantoti, lai aprēķinātu ierosināto pārdošanas cenu. Varat norādīt krājuma pārdošanas cenu vai izmaksu grupu. Daži ražotāji vēlas aprēķināt ierosināto pārdošanas cenu ražotajiem krājumiem. Aprēķinātā pārdošanas cena var atainot apkopoto cenu pieeju, kas ir balstīta uz komponenta pārdošanas cenas ierakstu. Aprēķinātā pārdošanas cena var attēlot arī pieeju “izmaksas-plus-uzcenojums”, kas ir balstīta uz komponenta cenas un piemērojamajiem peļņas procentiem, kas ir saistīti ar krājumu izmaksu grupu.
-   Izmantojot lauku **Pārtraukt izvēršanu**, jūs norādāt, ka MK aprēķina laikā ražots krājums izmaksu apkopošanas nolūkos ir jālieto kā iegādāts krājums. Tipiskajos scenārijos ir iesaistīti iegādātie krājumi, kas reizēm tiek ražoti, vai ražotie krājumi, kas tagad tiek iegādāti. Vispirms krājums tiks norādīts kā ražots krājums, lai definētu materiālu komplekta (MK) un maršruta informāciju, kā arī lai atbalstītu šī krājuma ražošanas pasūtījumus. Taču karodziņš **Pārtraukt izvēršanu** izmaksu aprēķiniem neļauj izmantojot šī krājuma MK un maršrutu. Tā vietā MK aprēķinā tiek izmantotas krājumam norādītās izmaksas.

## <a name="calculation-groups"></a>Aprēķinu grupas
Aprēķinu grupas jūs definējat izmaksu pārvaldības sadaļā **Iepriekš noteikto izmaksu politiku iestatīšana**. Krājumiem piešķirtās aprēķinu grupas jums ļauj norādīt, kā aprēķinam tiem iegūtas aprēķinu grupas norādītās izmaksas vai pārdošanas cenas komponenti. Lapā **Aprēķinu grupas** varat definēt izmaksu cenas modeli, alternatīvu izmaksu cenas modeli, pārdošanas cenas modeli un brīdinājumus.

### <a name="cost-price-model"></a>Izmaksu cenas modelis

Laukam **Izmaksu cenas modelis** ir četras opcijas:

-   **Krājuma izmaksu cena** — tiek izmantota izmaksu cena no tabulas **Izlaistā prece**, vai kā izmaksu cena tiek izmantota krājuma dimensiju kombinācija.
-   **Krājuma pirkšanas cena** — tiek izmantota pirkšanas cena no lapas **Izlaisto preču saraksts** cilnes **Pirkšana** lauka **Izmaksu cena**.
-   **Tirdzniecības līgumi** — varat konfigurēt tirdzniecības līgumus noteiktām krājumu un kreditoru kombinācijām vai konkrētām vietām. Kad šeit atlasāt opciju **Tirdzniecības līgumi**, tiks izmantots tirdzniecības līgums, kuru izveidojāt pirkšanas cenai, kopā ar krājumu un vietu.
-   **Krājumu cena** — lai aprēķinātu vienības izmaksas MK aprēķinā, tiek lietota pašreizējā krājumu vērtība šim krājumam. Vienības izmaksu cena tiek aprēķināta tikai tad, ja grāmatotais daudzums un fiziskais daudzums ir lielāki par 0 (nulli).

### <a name="alternative-cost-price"></a>Alternatīva izmaksu cena

Laukā **Alternatīvā izmaksu cena** ir tādas pašas opcijas kā laukā **Izmaksu cenas modelis**. Taču šis lauks tiek izmantots tikai tad, ja cenu nevar atrast primārajā izmaksu cenas modelī.

### <a name="sales-price-model"></a>Pārdošanas cenas modelis

Lauka **Pārdošanas cenas** aprēķināšanai pastāv divas opcijas:

-   **Izmaksu grupa** — kad ir atlasīta šī opcija, pārdošanas cena tiek aprēķināta, pamatojoties uz izmaksu cenu un peļņas iestatījumu procentiem no izmaksu grupas.
-   **Krājuma pārdošanas cena** — kad ir atlasīta šī opcija, tiek lietota pārdošanas cena kopsavilkuma cilnē **Pārdot** no tabulas Izlaistā prece.

### <a name="stop-explosion"></a>Pārtraukt izvēršanu

Izvēles rūtiņa **Pārtraukt izvēršanu** tiek izmantota, lai norādītu, kad ražots krājums ir jālieto kā pirkšanas krājums. Parasti jūs izvēles rūtiņu **Pārtraukt izvēršanu** atstājat neatzīmētu. Atzīmējot šo izvēles rūtiņu, jūs norādāt, ka MK aprēķina nolūkos ražots krājums ir jālieto kā pirkšanas komponents, nevis ražots komponents. Atkarībā no vietas šī krājuma izmaksas joprojām var tikt aprēķinātas, lietojot MK aprēķinus. Plānoto ražošanas pasūtījumu izvēršana tiek apturēta pie tāda MK, kura komponenti ir saistīti ar aprēķinu grupu, kurai ir atzīmēta izvēles rūtiņa **Pārtraukt izvēršanu**. Vispārējā plānošana ģenerē plānotos pasūtījumus pašam MK, nevis krājumiem, kas ir iekļauti šajā MK. Atzīmējot šo izvēles rūtiņu, jūs būtībā norādāt, ka krājumiem, kam ir šī aprēķinu grupa, MK aprēķinam netiks pieskaitītas izmaksas.

### <a name="warnings"></a>Brīdinājumi

Kopsavilkuma cilnē **Brīdinājumi** jūs atlasāt opcijas visiem brīdinājumu ziņojumiem, kas lietotājiem ir jāsaņem, kad viņi izpilda MK aprēķinus. Piemēram, ja atzīmējat izvēles rūtiņu **Nav MK**, tad lietotājs saņem brīdinājumu, kad vienam no komponentiem vai pamatkrājumam, kam ir palaists MK aprēķins, nav atrasta aktīva MK versija. Ja atzīmējat izvēles rūtiņu **Nav maršruta**, lietotājs saņem brīdinājumu, ja netiek atrasta aktīva maršruta versija. Ja savos maršrutos un operācijās izmantojat resursus, varat likt sistēmai pārbaudīt šos resursus. Ja resurss aktīvajā maršrutā netiek atrasts katrā rindiņā, lietotājs saņem brīdinājumu. Varat arī verificēt un pārbaudīt patēriņu. Patēriņš ir daudzums noteiktā maršrutā. Parasti tas parāda laika daudzumu, kas ir nepieciešams, lai ražošanas procesam izpildītu konkrētu operāciju. Varat pārbaudīt, vai krājumam nav izmaksu cenas. Ja krājumam nav aktīvas izmaksu cenas, MK aprēķinam netiek pieskaitītas nekādas izmaksas. Varat arī pārbaudīt un verificēt izmaksu cenas vecumu. Piemēram, ievadiet **60**, lai norādītu, ka vienības izmaksu cena ir jāpārvērtē pēc 60 dienām. Ja tiek sasniegts šis ierobežojums, sistēma ģenerē brīdinājumu. Piemēram, izmaksu cena krājumam tika ievadīta šī gada janvārī. Ja tagad ir augusts, kas nozīmē, ka kopš izmaksu cenas ievadīšanas ir pagājušas vairāk nekā 60 dienas, tad MK aprēķina palaišanas laikā lietotājs saņem brīdinājumu. Varat ievadīt procentuālu daudzumu laukā **Minimālā seguma summa**. Šī vērtība norāda uz vietu, kurā nav izpildīta minimālā seguma summa. Ja seguma summa nav izpildīta konkrētam komponentam, tad lietotājs saņem brīdinājumu. Tādēļ šis lauks palīdz garantēt, ka jūs nenosakāt pārāk zemas izmaksas un papildu uzturēšanas izmaksas, kas varētu būt nepieciešamas jūsu krājumiem.
Noklusējuma iestatījumi krājumu un noliktavas vadības parametros
--------------------------------------------------------------

Tā kā aprēķinu izpildīšanai ir nepieciešamas aprēķinu grupas, jums krājumu vadības parametros ir jāiestata noklusējuma aprēķinu grupa. Šis iestatījums uzņēmumiem ļauj izmantot standarta izmaksu grupu un peļņas iestatījumus visiem krājumiem. Ja noteiktam krājumam ir īpašas aprēķinu prasības, lietotājs šim krājumam var piešķirt citādu aprēķinu grupu. Parasti aprēķinu grupas varat iestatīt MK komponentu krājumiem, nevis MK krājumiem. Taču, kad tiek rādīti brīdinājumu ziņojumi, aprēķinu grupas var lietot. Krājumiem piešķirtajai aprēķinu grupai ir lielāka prioritāte nekā noklusējuma vērtībai, kas ir iestatīta krājumu vadības parametros. Varat iestatīt noklusējuma parametru pie **izmaksu pārvaldība**&gt;**krājumu uzskaites politikas iestatījums**&gt;**parametrus**&gt;**krājumu uzskaites**&gt;**aprēķinu grupa**. Iestatot noklusējuma konfigurācijas grupu, varat arī konfigurēt brīdinājumu nosacījumus, kas MK aprēķināšanas procesa laikā lietotājiem parāda uzvednes, ja atlasītie komponenti varētu izraisīt aprēķina kļūdas.
Skatīt brīdinājuma ziņojums lapā Pabeigt
------------------------------------------

MK aprēķins ģenerē brīdinājuma ziņojumus. Varat skatīt brīdinājumus par atlasītu krājumu. Piemēram, sadaļā Pārdošana un mārketings izveidojiet jaunu pārdošanas pasūtījumu krājumam D0001. Pēc tam pārdošanas pasūtījuma rindā, izvēlnē **Atjaunināt rindu** noklikšķiniet uz **Aprēķināt, pamatojoties uz MK/formulu**, lai skatītu detalizētu informāciju par aprēķiniem un brīdinājumus. MK aprēķinu rezultātus varat skatīt arī lapā **Pabeigt**. Brīdinājumu ziņojumiem uz ražotiem krājumiem attiecas tikai divi brīdinājumu nosacījumi, bet uz visiem krājumiem attiecas četri brīdinājumu nosacījumi:
-   Identificēt, kad ražotam krājumam nav aktīva MK.
-   Identificēt, kad ražotam krājumam nav aktīva maršruta.
-   Identificēt, kad krājumam MK rindā daudzums ir 0 (nulle).
-   Identificēt, kad krājumam MK rindā izmaksas ir 0 (nulle) vai kad tam nav izmaksu ieraksta.
-   Identificēt, kad krājumam MK rindā ir novecojušas izmaksas. Brīdinājums atspoguļo aprēķina datuma ar norādīto maksimālo izmaksu vecuma salīdzinājumu.
-   Identificēt, kad krājumam MK rindā ienesīguma procenti ir mazāki par vēlamajiem.

Varat definēt vairākas MK aprēķinu grupas, atkarībā no tā, kāda brīdinājuma ziņojumu dažādība jums ir nepieciešama. Piemēram, vienai MK aprēķina grupai, kurai ir brīdinājuma nosacījumi par aktīvu MK un komponentu daudzums ir 0 (nulle), var pietikt ar komponentu izmaksu 0 (nulle). Kad sākat MK aprēķinu, varat ignorēt brīdinājuma nosacījumus, kas ir saistīti ar šo MK aprēķinu grupu. Brīdinājumu nosacījumus varat arī pievienot vai noņemt. Piemēram, ja pašreizējā situācijā nav iesaistīti maršrutēšanas dati, varat noņemt brīdinājuma nosacījumu par aktīvu maršrutu. **Piezīme.** Laiks un apmeklētība ietver lapu **Aprēķinu grupas**, bet šai lapai nav nekādas saistības ar MK aprēķinu grupām. Sadaļā Laiks un apmeklētība darbiniekus var piešķirt aprēķinu grupām, kas atspoguļo ar to pašu supervizoru vai vadītāju saistītu darbinieku grupēšanu. Darbinieku reģistrāciju aprēķinu supervizors vai vadītājs var izpildīt automātiski vai manuāli.


