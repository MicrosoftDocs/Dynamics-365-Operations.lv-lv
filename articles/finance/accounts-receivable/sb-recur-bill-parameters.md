---
title: Periodisko līguma norēķinu parametri
description: Šajā rakstā ir izskaidrots, kā iestatīt noklusējuma vērtības norēķinu grafikiem, kas tiek izveidoti periodiskiem līguma rēķiniem. Tajā skaidrots arī, kā izveidot norēķinu grafika grupas.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 64d6e21c2d8c588a64f0f4cf8b7a0bafc853bcab
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644008"
---
# <a name="recurring-contract-billing-parameters"></a>Periodisko līguma norēķinu parametri

Izmantojiet lapu **Periodiskie līguma norēķinu parametri**, lai iestatītu noklusējuma vērtības norēķinu grafikiem, kas tiek izveidoti periodiskiem līguma rēķiniem. Visi izveidotie rēķinu grafiki sākumā izmantos šīs noklusējuma vērtības. Tomēr pēc pieprasīšanas varat mainīt katra norēķinu grafika vērtības.

## <a name="general-tab"></a>Cilne Vispārīgi

1. Lapas Periodiskie **līguma norēķinu parametri** cilnes **·** **Vispārīgi laukā Norēķinu grafika grupa** atlasiet norēķinu grafika grupu. Papildinformāciju par to, kā iestatīt norēķinu grafika grupas, skatiet [tālāk](#set-up-billing-schedule-groups) šī raksta sadaļā Norēķinu grafika grupas.
2. Laukā Darba **attiecību pārtraukšanas** veids atlasiet, kā tiek aprēķināts galīgais rēķins, ja norēķinu grafiks tiek pārtraukts:

    - **Pielāgot grafiku** . Nogrieziet norēķinu grafiku darba attiecību pārtraukšanas datumā, mainiet grafika statusu uz Pēdējie norēķini un koriģējiet saistīto atlikto maksājumu grafiku, atceļot summu, **kas** vairs nav jāpazīst. Ja norēķinu sākuma datums ir pēc atbrīvošanas datuma, pārējie norēķinu periodi tiek noņemti.
    - **Atlikušais** rēķins - pievienojiet atlikušās summas norēķinu grafikā darba attiecību pārtraukšanas periodam, **mainiet** grafika statusu uz Pēdējie norēķini un atjauniniet atlikto maksājumu grafiku. Ja norēķinu sākuma datums ir pēc atbrīvošanas datuma, visu atlikušo norēķinu periodu kopējā summa tiek pievienota norēķinu periodam, un atlikušie norēķinu periodi tiek noņemti.
    - **Nav korekciju** - pārtrauciet norēķinu grafiku darba attiecību pārtraukšanas datumā. Norēķinu grafikā nav veiktas korekcijas.

3. Laukā **Unikāls grafika veids** atlasiet Nav **, lai** norādītu, ka debitori ir ierobežoti ar vienu norēķinu grafiku. Atlasiet **Katru debitoru vai** uz **katru lietotāju,** lai norādītu, ka debitori ir ierobežoti ar unikālu grafiku.
4. Iestatiet opciju **Līdzināt uz mēnesi**, lai **saskaņotu** norēķinu grafika detaļu rindas ar mēneša beigām, kad tiek izveidots vai atjaunināts norēķinu grafiks. Iestatiet to uz Nē **, lai** izmantotu inkrementālos datumus.
5. Lai sadalītu **norēķinu summas, pamatojoties** uz perioda **dienu** skaitu, iestatiet opciju Sadalīt daļējos periodus uz Jā. Iestatiet to kā **Nē**, lai katram norēķinu periodam būtu vienāda summa neatkarīgi no dienu skaita.
6. Ja iestatāt opciju **Sadalīt** **daļējos** periodus uz Jā, **iestatiet metodes laukā Proration** **vērtību** Ikdienas, lai sadalītu summas atbilstoši perioda dienu skaitam. Iestatiet tai mēneša **summu**, kas vienāda ar katru mēnesi.
7. Norādiet, vai jaunizveidotie norēķinu grafiki pēc noklusējuma ir aizturēti.

    > [!NOTE]
    > Lai noņemtu norēķinu grafika aizturēšanu, lietotājam ir jābūt lietotāju grupas daļai. Atlasiet **noņemt aizturēšanas lietotāju grupas ignorēšanu**, lai iestatītu lietotāju grupu, kurā ir **iespējota opcija Atļaut** noņemšanas aizturēšanu.

8. Laukā **Rēķina darbības** veids atlasiet noklusējuma rēķina darbības veidu jaunajiem norēķinu grafikiem.
9. Iestatiet opciju Saskaņot **atlikto maksājumu uz norēķinu opciju** Uz **jā**, lai saskaņotu atbilstošo atlikto maksājumu grafiku tā, lai tam tiek izmantoti tādi paši datumi kā norēķinu grafikam. Iestatiet to uz **Nē,** lai datumi būtu atšķirīgi.
10. Ja izmantojat ieņēmumu sadalīšanas iespēju, iestatiet opciju Automātiski **izveidot** **ieņēmumu sadalījumu uz Jā,** kad krājumi tiek pievienoti norēķinu grafikam. Ieņēmumu **sadalīšanas** izvēles rūtiņa tiks automātiski atzīmēta norēķinu grafika rindā, ja krājums ir iestatīts kā ieņēmumu sadalīts krājums. Iestatiet opciju Nē **,** ja vēlaties manuāli atzīmēt izvēles rūtiņu Ieņēmumu **sadalīšana**.
11. Lai norēķinu **grafikam varētu** izrakstīt rēķinus **dažādiem** debitoriem, iestatiet opciju Debitora sadalīšana kā Jā. Ja opcija ir iestatīta **uz** Jā **, norēķinu** grafika virsrakstā un norēķinu grafika rindā ir pieejama opcija Debitora sadalīšana. 
12. Iestatiet laukus pārdošanas pasūtījuma izveidei:

    - Rēķinus var konsolidēt pēc perioda, debitora vai krājuma. Var iestatīt jebkādu **vērtību Jā** **un Nē** kombināciju. Rēķinus var arī sadalīt pēc krājumu grupas.
    - Rēķiniem ir pieejamas šādas grāmatošanas opcijas:

        - **Izveidot pārdošanas pasūtījumu** – izveidot tikai pārdošanas pasūtījumu.
        - **Rādīt rēķina grāmatošanu** – rēķinu pārdošanas pasūtījumā un atvērt lapu, kur varat manuāli grāmatot rēķinu.
        - **Izveidot papildmaksas teksta** rēķinu — atlasiet šo opciju, ja izmantojat brīvā teksta rēķinus.
        - **Grāmatot rēķinu automātiski** – izrakstīt rēķinu pārdošanas pasūtījumam un automātiski to iegrāmatot.

    - Lai pievienotu **aprakstu, kas ietver norēķinu sākuma** datumu un beigu **datumu**, iestatiet opciju Pievienot norēķinu datumus krājuma aprakstam.
    - Iestatiet opciju Neiekļaut **nulles patēriņu** kā Jā **,** lai izslēgtu norēķinu grafika rindas, kam nav patēriņa. Iestatiet to uz **Nē**, lai ietvertu šīs rindas pārdošanas pasūtījumā.
    - Iestatiet opciju **Nedrukāt pakārtotos** krājumus **uz** Jā, ja pārdošanas pasūtījumā nevēlaties drukāt ieņēmumu sadalīšanas pakārtotos krājumus. Rēķinā tiks parādīts tikai pamatobjekts. Ja (paslēpto) pakārtoto krājumu neto summa ir summa, kas nav nulle, pamatrindu neto summa rāda pakārtoto rindu kopsavilkumu. Iestatiet opciju Nē, lai **pārdošanas** rēķinā drukātu visus pakārtotos krājumus zem pamatelementa.

12. Iestatiet laukus atbalstam un atjaunošanai:

    - Iestatiet opciju **Automātiski iespējot atbalstu un atjaunošanu** uz **Jā**, lai automātiski izmantotu pārdošanas pasūtījuma atbalsta un atjaunošanas līdzekli.
    - Laukā **Atbalsta un atjaunošanas līmenis** atlasiet noklusējuma atbalstu un atjaunošanas līmeni.
    - Laukā **Atbalsta un atjaunošanas daudzums** norādiet atbalsta un atjaunošanas daudzumu.
    - Laukā **Noklusējuma atbalsta un atjaunošanas sākuma** datums norādiet datumu, kas ir jāizmanto kā noklusējuma sākuma datums atbalstam un atjaunošanai:

        - **Darbības datums** – izmantojiet darbības datumu kā sākuma datumu.
        - **Pašreizējā mēneša sākums** – izmantojiet pirmo no pašreizējā mēneša kā sākuma datumu.
        - **Nākamā mēneša sākums** – izmantojiet pirmo no nākamā mēneša kā sākuma datumu. Ja darbības datums ir pirmais, tiek izmantots pirmais no pašreizējam mēnesim.
        - **15. noteikums** – lietojiet šī mēneša pirmo datumu kā sākuma datumu, ja darbības datums ir starp mēneša pirmo un piecpadsmito datumu. Ja darbības datums ir sešpadsmitais vai vēlāk, kā sākuma datumu izmantojiet nākamā mēneša pirmo datumu.

    - Iestatiet opciju **Iekļaut atlaidi aprēķinā uz** Jā **,** lai iekļautu atlaides summu atbalsta vai atjaunošanas summā. Iestatiet to uz **Nē,** lai izslēgtu atlaides summu.
    - Laukos Atbalsta **biežums un** **Atjaunošanas** biežums atlasiet biežumu, kas jāizmanto, kad rēķinu grafikam tiek pievienoti atbalsta un atjaunošanas krājumi: **katru** dienu, **·** **katru** mēnesi, ceturkšņa, **pusgadu** vai **gadu.**
    - Lai jauno **krājumu sākuma un beigu datumus** **līdzinātu** esošiem krājumiem, pamatojoties uz krājumu grupu, iestatiet opciju Saskaņot pēc krājumu grupas.
    - Lai noteiktu **atjaunošanas krājuma līdzinājuma** **datumu**, pamatojoties uz nākamā nenosātinātā perioda datumu pēc atjaunošanas sākuma, iestatiet opciju Līdzināt uz nākamo nenokārtoto periodu.
    - Iestatiet opciju **Kopēt sērijas** numuru uz Jā **,** lai kopētu krājuma sērijas numuru no sākotnējās pārdošanas pasūtījuma rindas uz atbilstošo rēķina grafika rindu.

13. Ja norēķinu grafikā izmantojat eskalāciju, atlasiet metodi, kas tiek izmantota plaša patēriņa cenu indeksa aprēķinam.
14. Ja vēlaties **reģistrēt cenu izmaiņas** norēķinu grafika **rindās**, iestatiet opciju Sekot cenas izmaiņām uz Jā. Ja norēķinu grafika rinda tiek manuāli mainīta no standarta uz dzīvokļu un tiek ievadīta jauna cena, audita informācija tiek izsekota norēķinu grafika rindā. Iestatiet opciju uz **Nē**, ja nevēlaties atsekot šīs izmaiņas.
15. Norādiet, vai ieraksti pēc noklusējuma tiek filtrēti pēc sākuma datuma vai beigu datuma lapā Ģenerēt **rēķinu**.
16. Ja izmantojat līdzekli **Nenobīdāmie** ieņēmumi, norādiet izmantotās opcijas:

    - Ja vēlaties **vienlaicīgi izveidot un** grāmatot **Virsgrāmatas** žurnālu, iestatiet opciju Grāmatot Virsgrāmatas žurnālu automātiski. Iestatiet to uz **Nē**, ja vēlaties izveidot Virsgrāmatas žurnālu un pēc tam manuāli to grāmatot.
    - Laukā **Noklusējuma žurnāla nosaukums** atlasiet noklusēto žurnāla nosaukumu, ko izmantot, veidojot Virsgrāmatas žurnālu.
    - Ja izmantojat **metodi**, laukā Īstermiņa nenosāciet aprēķināšanas metode atlasiet īstermiņa neanobieto metodi. Atlasot **Nav**, īstermiņa funkcionalitāte netiks izmantota ar nenovienotiem ieņēmumiem. Atlasiet Notiek **periodu atrite**, lai vienmēr lietotu 12 mēnešus vai **fiksētu gadu** atlikušā finanšu gada izmantošanai.

17. Norādiet opcijas, kas tiek izmantotas, kad tiek pārtraukts norēķinu grafiks un tā rindas:

    - **Izsniegt kredītu** - izveidojiet kredīta notu, kad tiek pārtraukts norēķinu grafiks vai norēķinu grafika rinda.
    - **Kredīta korekcija** - izveidojiet kredīta korekciju norēķinu grafikam, ja rinda ir izbeigta. Kredīta korekcija tiek parādīta norēķinu grafika nākamajā norēķinu periodā. Kredīta korekcija atjauninās rēķina summu nākamajam norēķinu periodam, līdz kredīts ir pabeigts norēķinu grafikam.
    - **Nav kredīta** - neveidojiet kredīta korekciju vai kredīta notu, ja tiek pārtraukts norēķinu grafiks vai norēķinu grafika rinda. Šī opcija ir pieejama tikai tad, kad opcija **Nav korekcijas** tiek izmantota, lai pārtrauktu rēķinu izrakstīšanas grafiku.
18. Ja opcija **Vienreizējs** **·** **var** pārtraukt darba attiecības ar atmaksu ir iestatīta uz Nē un norēķinu grafiks ar norēķinu biežumu Vienreizējs, **norēķinu** grafika rindas statuss mainās uz Pārtraukts pēc norēķinu grafika rēķina izrakstīšanas. Šo norēķinu grafiku nevar pārtraukt, un nevar izsniegt kredītu. Ja **vienreizēji var** **·** **·** **pārtraukt** darba attiecības ar atmaksu, ir iestatīts uz Jā, rēķinu grafika rindai ar norēķinu biežumu Viens laiks būs Aktīvs statuss pēc rēķina izrakstīšanas grafika. Norēķinu grafika rindu var pārtraukt un veikt atmaksu. 
19. Parametros **iestatītā** ikdienas opcija Automātiski pārtraukt darba attiecību pārtraukšanas tiks iestatīta uz masveida darba attiecību pārtraukšanas lapu un norēķinu grafika virsrakstu un rindu pārtraukšanas dialogiem. To var mainīt atbrīvošanas procesa laikā. Ja iestatījums ir **Jā**, tad atmaksas summa tiks aprēķināta, izmantojot dienas likmi. Ja iestatījums ir **Nē**, tas tiks kreditēts, pamatojoties uz darba attiecību pārtraukšanas datumu un norēķinu biežumu. Piemēram, ja izmantojat Mēneša biežumu un rēķina summa tika $100 mēnesim, kredīta summa tiek palielināta $100. Ja norēķinu biežums ir Vienreizējs, kredīta summa tiek $0.00. Lai saņemtu atmaksu par vienreizējo norēķinu biežumu, ikdienas likmei jābūt Iestatītai kā Jā. 
20. Lai **izveidotu jaunu atlikto maksājumu grafiku**, kredīta opcijai **izveidot** atlikto maksājumu iestatiet vērtību Izveidot atlikto maksājumu kā Jā, ja kreditēsit esošo atlikto maksājumu grafiku. Atstājiet opciju iestatītu uz **Nē**, lai izveidotu kredītu esošajā atlikto maksājumu grafikā.

## <a name="sequence-number-tab"></a>Cilne Secības numurs

Izmantojiet cilni **Sērijas** numurs lapā Periodiskie **līguma norēķinu parametri**, lai iestatītu noklusējuma vērtību norēķinu grafika numuriem. Noklusējuma vērtības ir iestatītas numuru sēriju **lapā (Organizācijas** administrēšanas **\> numuru sērijas \> Numuru sērijas**).

## <a name="set-up-billing-schedule-groups"></a>Iestatīt norēķinu grafika grupas

Izmantojiet lapu **Norēķinu grafika grupa**, lai izveidotu norēķinu grafika grupu periodiskiem līguma norēķiniem. Kad tiek izveidots jauns norēķinu grafiks un tam tiek pielietota norēķinu grafika grupa, **lapā** Norēķinu grafika grupa definētās vērtības tiek ievadītas kā noklusējuma vērtības norēķinu grafikam. Varat mainīt jebkuras noklusējuma vērtības izveidotam konkrētam norēķinu grafikam. Varat iestatīt vairākas norēķinu grafika grupas un pēc tam piešķirt vienu no tām kā noklusējuma norēķinu grafika grupu lapā **Periodiskie līguma norēķinu parametri**.

Lai izveidotu norēķinu grafika grupu periodiskiem līguma rēķiniem, sekojiet šiem soļiem.

1. Lapā Norēķinu **grafika grupa** atlasiet **Jauns**, lai izveidotu norēķinu grafika grupu.
2. Laukā **Norēķinu grafika grupa** ievadiet unikālu identifikatoru.
3. Ievadiet aprakstu laukā **Apraksts**.
4. Laukā **Norēķinu biežums** norādiet, cik bieži rēķinu grafikam ir izrakstīts rēķins debitoram: **vienreizējs**, ikdienas, **·** **ikmēneša**, **ceturkšņa**, **puslaiks** vai **reizi gadā.**
5. Laukā **Norēķinu intervāls** ievadiet norēķinu intervālu. Piemēram, iestatiet lauku Norēķinu biežums **uz Mēnesis** **un** Rēķina intervāls **uz** **2, lai** izrakstītu rēķinu katru mēnesi.
6. Laukā **Cenu noteikšanas** metode atlasiet noklusējuma cenu noteikšanas metodi krājumiem norēķinu grafikā.

    - **Standarta** – aprēķiniet vienības cenu, pamatojoties uz ievadīto kopējo daudzumu, **un izmantojiet standarta cenu noteikšanu no Izlaisto preču** informācijas pārvaldības lapas.
    - **Flat** – izmantojiet vienotās cenas, kas tiek ievadītas norēķinu grafika rindā.
    - **Pakāpe** – aprēķiniet vienības cenu, izmantojot fiksētu daudzumu dažādās cenu noteikšanas iekavās. Pirms pārcelšanas uz nākamo cenu noteikšanas iekavu ir jāaizpilda katra pakāpe.
    - **Vienotā pakāpe** – aprēķina vienības cenu, izmantojot fiksētu daudzumu un paplašinātās cenas summas dažādām cenu noteikšanas iekavām. Cena, kas tiek pieprasīta norēķinu periodā, izmanto paplašināto cenu, kas atbilst pakāpei, kurā atrodas norēķinu daudzums.

7. **Laukā Krājuma** veids atlasiet krājumu tipu norēķinu grupai:

    - **Standarta** – atlasiet šo vērtību, ja daudzums ir statisks.
    - **Lietojums** – atlasiet šo vērtību mērītājiem vai patēriņa tipa krājumiem. Ja jūs atlasāt šo vērtību, **·** **iestatiet** Usage lasījuma opciju lauku, lai ievadītu vērtību (lasījumu) norēķinu periodam mērītājā vai ierīcē. Patērētā vērtība tiks aprēķināta, pamatojoties uz iepriekšējo norēķinu periodu un pašreizējo jūsu ievadīto lasījumu.
    - **Atskaites punkts** – izvēlieties šo vērtību, lai izmantotu Atskaites punkta norēķinu funkcionalitāti. Ja izvēlaties šo vērtību, **laukā Atskaites** punkta veidne izvēlieties atskaites punkta veidni, ja izmantojat to.
    - **Patēriņš** – izvēlieties šo vērtību, lai ievadītu vērtību, kas tiek patērēta norēķinu periodam.

8. Lai izveidotu **konsolidēto rēķinu** un atsevišķu **rēķinu** kombināciju tam pašam debitoram, opciju Rēķins iestatiet atsevišķi. Piemēram, debitoram ir pieci norēķinu grafiki. Trīs no tām tiks konsolidētas vienā rēķinā, bet katram no pārējiem rēķiniem ir nepieciešams atsevišķs rēķins. Iestatiet opciju Nē **, lai** debitoram izveidotu tikai vienu konsolidētu rēķinu.
9. Iestatiet opciju **Atjaunot automātiski**, lai **automātiski** atjaunotu periodisko norēķinu grafiku nākamajam norēķinu periodam, kad tiek izveidots rēķins. Iestatiet to kā **Nē**, lai manuāli atjaunotu norēķinu grafiku. Laukā Rindas **, kas jāpievieno katrai atjaunošanai**, norādiet, cik rindu pievienosit katrai atjaunošanai.
10. Iestatiet opciju **Eskalācija**, lai **lietotu** *eskalācijas (cenas palielinājumus*) norēķinu grafikiem, kas saistīti ar šo norēķinu grafika grupu.
