---
title: Elastīga noliktavas līmeņa dimensiju rezervācijas politika
description: Šajā rakstā ir aprakstīts krājumu rezervēšanas politika, kas ļauj uzņēmumiem pārdot partijas izsekotas preces un palaist to loģistiku kā WMS iespējotas operācijas rezervē noteiktas partijas debitoru pārdošanas pasūtījumiem, pat ja rezervāciju hierarhija, kas saistīta ar precēm, neļauj rezervēt noteiktu partiju.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fb42d4ccd2d8797a34f6351caf7dedbc1e957fd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885817"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Elastīga noliktavas līmeņa dimensiju rezervācijas politika

[!include [banner](../includes/banner.md)]

Ja *Partijas lejpusēja\[novietojuma\]* tipa krājumu rezervēšanas hierarhija ir saistīta ar precēm, tad uzņēmumi, kuri pārdod pēc partijas izsekotās preces un nodrošina savu loģistiku kā operācijas, kas ir iespējotas Microsoft Dynamics 365 noliktavas vadības sistēmai (WMS), nevar rezervēt konkrētas šo preču partijas debitoru veiktiem pārdošanas pasūtījumiem.

Līdzīgā veidā licencētas numura zīmes nevar rezervēt precēm pārdošanas pasūtījumos, kad šīs preces ir saistītas ar noklusējuma rezervāciju hierarhiju.

Šajā rakstā ir aprakstīts krājumu rezervēšanas politika, kas ļauj šiem uzņēmumiem rezervēt noteiktas partijas vai numura zīmes, *pat ja preces ir saistītas ar partiju rezervēšanas\[\]* hierarhiju zem novietojuma.

## <a name="inventory-reservation-hierarchy"></a>Krājumu rezervāciju hierarhija

Šajā sadaļā ir apkopota esošā krājumu rezervāciju hierarhija.

Krājumu rezervāciju hierarhija nosaka, ka, cik tas attiecas uz noliktavas dimensijām, pieprasījuma pasūtījumā ir obligātās vietas, noliktavas un krājumu statusa dimensijas. Citiem vārdiem sakot, obligātās dimensijas ir visas dimensijas virs atrašanās vietas dimensijas rezervāciju hierarhijā, bet noliktavas loģika ir atbildīga par atrašanās vietas piešķiršanu pieprasītajiem daudzumiem un atrašanās vietas rezervēšanu. Citiem vārdiem sakot, mijiedarbojoties pieprasījuma pasūtījuma un noliktavas operācijām, pieprasījuma pasūtījumā vajadzētu norādīt, kur pasūtījums ir jānosūta (proti, uz kādu vietu un noliktavu). Pēc tam noliktava paļaujas uz savu loģiku, lai atrastu nepieciešamo daudzumu noliktavas telpās.

Tomēr, lai atspoguļotu biznesa darbības modeli, izsekošanas dimensijām (partijas un sērijas numuri) tiek piemērota lielāka elastība. Krājumu rezervēšanas hierarhija var ietvert scenārijus, kuros ir spēkā tālāk norādītie nosacījumi:

- Uzņēmums paļaujas uz savām noliktavu operācijām, lai *pēc tam*, kad daudzumi ir atrasti noliktavas uzglabāšanas telpā, pārvaldītu tādu daudzumu izdošanu, kuriem ir partijas vai sērijas numuri. Šis modelis bieži tiek saukts par *Partijas lejpusējo\[novietojums\]* vai *Sērijas lejpusējo\[novietojums\]*. Parasti tas tiek izmantots, ja debitoriem, kuri pārdošanas uzņēmumā iesniedz pieprasījumu, nav svarīga preces partijas vai sērijas numura identifikācija.
- Uzņēmums paļaujas uz savām noliktavu operācijām, lai *pirms tam*, kad daudzumi ir atrasti noliktavas uzglabāšanas telpā, pārvaldītu tādu daudzumu izdošanu, kuriem ir partijas vai sērijas numuri. Ja partijas vai sērijas numuri ir svarīga daļa no debitora pasūtījuma specifikācijas, un tie tiek ierakstīti pieprasījuma pasūtījumā, noliktavas operācijas, kas atrod daudzumus noliktavā, ierobežo konkrēti pieprasītie numuri, un tām nav atļauts tās mainīt. Šis modelis bieži tiek saukts par *Partijas virspusējo\[novietojums\]* vai *Sērijas virspusējo\[novietojums\]*. Tā kā dimensijas virs novietojuma ir noteiktas prasības prasībām, kas jāizpilda, noliktavas loģika nedalīs tās. Šīs dimensijas **vienmēr** jānorāda pieprasījuma pasūtījumā vai saistītajās rezervācijās.

Šādos scenārijos grūtības rada tas, ka katrai izlaistajai precei var piešķirt tikai vienu krājumu rezervācijas hierarhiju. Tāpēc, lai WMS apkalpotu izsekotos krājumus, pēc hierarhijas piešķires nosaka, kad partijas vai sērijas numurs jārezervē (vai nu, kad tiek veikts pieprasījums, vai arī noliktavas izdošanas darbā); šo laiku nevar mainīt pēkšņi.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Elastīga partijas izsekoto krājumu rezervācija

### <a name="business-scenario"></a>Biznesa scenārijs

Šajā scenārijā uzņēmums izmanto krājumu stratēģiju, kur gatavās preces tiek izsekotas pēc partiju numuriem. Šis uzņēmums izmanto arī WMS noslodzi. Tā kā šai darba noslodzei ir labi aprīkota loģika, lai plānotu un izpildītu to krājumu izdošanu no noliktavas un nosūtīšanu, kuriem iespējotas partijas, lielākā daļa gatavo krājumu ir saistīti ar *Partijas lejpusēja\[novietojuma\]* krājumu rezervācijas hierarhiju. Šāda veida darbību iestatījumam ir priekšrocība, ka lēmumi (kuri ir efektīvi rezervācijas lēmumi) par to, kuras partijas izdot un kur tās ievietot noliktavā, tiek atlikti līdz noliktavas izdošanas darbību sākumam. Tās netiek izpildītas, kad tiek veikts debitora pasūtījums.

Kaut arī *Partijas lejpusēja\[novietojuma\]* rezervāciju hierarhija kalpo uzņēmuma biznesa mērķiem, daudziem no uzņēmuma stabilajiem debitoriem ir nepieciešama tā pati partija, ko tie iegādājās iepriekš, kad vēlreiz pasūtīja preces. Tāpēc uzņēmums meklē elastīgu pieeju partijas rezervācijas noteikumu piemērošanai, un tādējādi atkarībā no debitora pieprasījuma tam pašam krājumam izpaužas tālāk aprakstītā rīcība.

- Partijas numuru var ierakstīt un rezervēt laikā, kad pasūtījumu veic pārdošanas apstrādātājs, un to nevar mainīt noliktavas darbību laikā un/vai, ņemot vērā citas prasības. Šī rīcība palīdz garantēt, ka pasūtītais partijas numurs tiek nosūtīts debitoram.
- Ja debitoram partijas numurs nav svarīgs, noliktavas darbības var norādīt partijas numuru izdošanas darba laikā, pēc pārdošanas pasūtījuma reģistrācijas un rezervēšanas veikšanas.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Konkrētas partijas rezervācijas atļauśana pārdošanas pasūtījumā

Lai piemērotu vēlamo elastību partijas rezervācijas rīcībā krājumiem, kas ir saistīti ar *Partijas lejpusēja\[novietojuma\]* krājumu rezervēšanas hierarhiju, krājuma vadītājiem jāatzīmē izvēles rūtiņa **Atļaut rezervāciju pēc pieprasījuma pasūtījuma** līmenim **Partijas numurs** lapā **Krājumu rezervācijas hierarhija**.

![Krājumu rezervācijas hierarhijas elastīguma nodrošināšana.](media/Flexible-inventory-reservation-hierarchy.png)

Ja hierarhijā ir atlasīts līmenis **Partijas numurs**, tad automātiski tiks atlasītas visas dimensijas virs šī līmeņa un uz augšu līdz līmenim **Atrašanās vieta**. (Pēc noklusējuma visas dimensijas virs līmeņa **Atrašanās vieta** tiek atlasītas iepriekš.) Šāda rīcība ataino loģiku, ka pasūtījuma rindā rezervējot konkrētu partijas numuru, automātiski tiek rezervetas arī visas dimensijas diapazonā starp partijas numuru un novietojumu.

> [!NOTE]
> Izvēles rūtiņa **Atļaut rezervāciju pēc pieprasījuma pasūtījuma** attiecas tikai tiem uz rezervāciju hierarhijas līmeņiem, kas atrodas zemāk par noliktavas atrašanās vietu dimensiju.
>
> **Partijas numurs** un **Licencēta numura zīme** ir vienīgie hierarhijas līmeņi, kas ir atvērti elastīgai rezervācijas politikai. Citiem vārdiem sakot, izvēles rūtiņu **Atļaut rezervāciju pieprasījuma pasūtījumā** nevar atzīmēt līmeņiem **Atrašanās vieta** vai **Sērijas numurs**.
>
> Ja rezervāciju hierarhijā ir ietverta sērijas numura dimensija (kurai vienmēr jābūt zemākai par **Partijas numura** līmeni) un ja partijas numuram ir ieslēgta partijai specifiska rezervācija, sistēma turpinās nodrošināt sērijas numura rezervāciju un izdošanu, pamatojoties uz noteikumiem, kas attiecas uz rezervācijas politiku *Sērijas lejpusēja\[novietojuma\]*.

Jūs jebkurā brīdī savā izvietojumā varat atļaut veikt partijai specifisko rezervāciju jau esošai rezervāciju hierarhijai *Partijas lejpusējs\[novietojums\]*. Šīs izmaiņas neietekmē rezervācijas un atvērto noliktavas darbu, kas tika izveidots pirms izmaiņu rašanās. Tomēr izvēles rūtiņu **Atļaut rezervāciju pēc pieprasījuma pasūtījuma** nevar dzēst, ja vienam vai vairākiem krājumiem, kas ir saistīti ar šo rezervāciju hierarhiju, eksistē izsniegšanas veidu **Rezervēts pasūtījumos**, **Rezervēts fiziski** vai **Pasūtīts** krājumu darbības.

> [!NOTE]
> Ja krājuma esošā rezervāciju hierarhija pasūtījumā neatļauj partijas specifikāciju, to var piešķirt rezervāciju hierarhijai, kas pieļauj partijas specifikāciju, ar nosacījumu, ka abās hierarhijās ir vienāda hierarhijas līmeņa struktūra. Lai veiktu atkārtotu piešķiršanu, izmantojiet funkciju **Mainīt krājumu rezervāciju hierarhijas**. Šīs izmaiņas var būt būtiskas, ja vēlaties novērst elastīgu partijas rezervāciju partijas izsekoto krājumu apakškopai, bet atļaut to pārējam preču portfelim.

Neatkarīgi no tā, vai ir atlasīta izvēles rūtiņa **Atļaut rezervāciju pēc pieprasījuma pasūtījuma**, ja nevēlaties krājumam pasūtījuma rindā rezervēt konkrētu partijas numuru, joprojām būs spēkā noklusējuma noliktavas darbību loģika, kas ir derīga rezervācijas hierarhijai *Partijas lejpusējs\[novietojums\]*.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Konkrētra partijas numura rezervācija debitora pasūtījumam

Pēc tam, kad partijas izsekotā krājuma krājumu rezervāciju hierarhija *Partijas lejpusējs\[novietojums\]* ir iestatīta, lai rezervāciju pārdošanas pasūtījumos atļautu konkrētus partiju numurus, pārdošanas pasūtījumu apstrādātaji var atkarībā no debitora pieprasījuma pieņemt debitora pasūtījumus tam pašam krājumam vienā no tālāk norādītajiem veidiem.

- **Pasūtījuma informācijas ievade, nenorādot partijas numuru** – šī pieeja jāizmanto, ja debitoram nav svarīga preces partijas specifikācija. Visi esošie procesi, kas sistēmā ir saistīti ar šī tipa pasūtījuma apstrādi, paliek nemainīgi. No lietotāju puses nav nepieciešami papildu apsvērumi.
- **Pasūtījuma informācijas ievade un konkrēta partijas numura rezervācija** – šī pieeja jālieto, kad debitors pieprasa konkrētu partiju. Parasti debitori pieprasīs konkrētu partiju, ja tie atkārtoti pasūta iepriekš iegādātu preci. Šo partijai specifiskās rezervācijas tipu dēvē par *ar pasūtījumu saistītu rezervāciju*.

Tālāk norādītais noteikumu kopums ir spēkā, ja tiek apstrādāti lieli preču daudzumi, un partijas numurs ir saistīts ar konkrētu pasūtījumu.

- Lai atļautu konkrēta partijas numura rezervāciju krājumam saskaņā ar rezervācijas politiku *Partijas lejpusējs\[novietojums\]*, sistēmai jārezervē visas dimensijas līdz atrašanās vietai. Šis diapazons parasti ietver noliktavas vienības dimensiju.
- Atrašanās vietas direktīvas netiek pielietotas, ja izdošanas darbs ir izveidots pārdošanas rindai, kas izmanto ar pasūtījumu saistītu partijas rezervāciju.
- Veicot noliktavā ar pasūtījumu saistītu partiju darba apstrādi, ne lietotājam, ne sistēmai nav atļauts mainīt partijas numuru. (Šī apstrāde ietver izņēmumu apstrādi.)

Tālāk piemērā ir parādītas visi plūsmas posmi.

## <a name="example-scenario-batch-number-allocation"></a>Piemēra scenārijs: partijas numura piešķiršana

Šajā piemērā jābūt instalētiem demonstrāciju datiem, un jums ir jāizmanto **USMF** demonstrācijas datu uzņēmums.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a>Krājumu rezervēšanas hierarhijas iestatīšana, lai atļautu partijai specifisku rezervāciju

1. Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Krājums \> Rezervēšanas hierarhija**.
2. Atlasiet **Jauns**.
3. Laukā **Nosaukums** ievadiet nosaukumu (piemēram, **BatchFlex**).
4. Laukā **Apraksts** ievadiet aprakstu (piemēram, **Elastīgs partijas numura novietojums**).
5. Laukā **Atlasīts** atlasiet **Sērijas numurs** un **Īpašnieks**, un pēc tam atlasiet kreiso bulttaustiņu, lai tos pārvietotu uz lauku **Pieejams**.
6. Atlasiet **Labi**.
7. Dimensijas līmeņa rindā **Partijas numurs** atzīmējiet izvēles rūtiņu **Atļaut rezervāciju pēc pieprasījuma pasūtījuma**. Automātiski tiek atlasīti līmeņi **Noliktavas vienība** un **Atrašanās vieta**, un to izvēles rūtiņas nevar dzēst.
8. Atlasiet **Saglabāt**.

### <a name="create-a-new-released-product"></a>Jaunas izlaistās preces izveide

1. Iestatiet preces trīs pamatdatu parametrus, izmantojot tālāk norādītās vērtības.

    - Laukā **Noliktavas dimensiju grupa** atlasiet **Izstrādājumi**.
    - Laukā **Izsekošanas dimensijas grupa** atlasiet **Batch-Phy**.
    - Laukā **Rezervācijas hierarhija** atlasiet **BatchFlex**.

2. Izveidojiet divus partiju numurus, piemēram, **B11** un **B22**.
3. Pievienojiet krājumu daudzumus rīcībā esošajiem krājumiem, izmantojot tālāk norādītās vērtības.

    | Noliktava | Paketes numurs | Vieta | Numura zīme | Daudzums |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Nav          | 10.       |
    | 24        | B11          | FL-001   | LP11          | 10.       |
    | 24        | B22          | FL-002   | LP22          | 10.       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a>Pārdošanas pasūtījumu informācijas ievade

1. Dodieties uz **Pārdošana un mārketings** \> **Pārdošanas pasūtījumi** \> **Visi pārdošanas pasūtījumi**.
2. Atlasiet **Jauns**.
3. Pārdošanas pasūtījumu virsrakstā, laukā **Debitora konts**, ievadiet **US-003**.
4. Pievienojiet rindu jaunajam krājumam un kā daudzumu ievadiet **10**. Pārliecinieties, ka laukam **Noliktava** ir atlasīts iestatījums **24**.
5. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Krājums** un pēc tam grupā **Uzturēt** atlasiet **Partijas rezervācija**. Lapā **Partijas rezervācija** tiek parādīts to partiju saraksts, kas ir pieejamas pasūtījuma rindas rezervācijai. Šajā piemērā tas rāda daudzumu **20** partijas numuram **B11** un daudzumu **10** partijas numuram **B22**. Ņemiet vērā, ka lapai **Partijas rezervācija** nevar piekļūt no rindas, ja krājums šajā rindā ir saistīts ar rezervāciju hierarhiju *Partijas lejpusējs\[novietojums\]*, ja vien tā nav iestatīta, lai atļautu partijai specifisku rezervāciju.

    > [!NOTE]
    > Lai pārdošanas pasūtījumam rezervētu konkrētu partiju, jāizmanto lapa **Partijas rezervācija**.
    >
    > Ja ievadāt partijas numuru tieši pārdošanas pasūtījumu rindā, sistēma izturēsies tā, it kā jūs ievadījāt konkrētu partijas vērtību krājumam, uz kuru attiecas rezervācijas princips *Partijas lejpusējs\[novietojums\]*. Kad saglabāsit rindu, tiks parādīts brīdinājuma ziņojums. Ja apstiprināt, ka partijas numurs ir jānorāda tieši pasūtījuma rindā, rindu neapstrādās parastā noliktavas pārvaldības loģika.
    >
    > Rezervējot daudzumu no lapas **Rezervācija**, neviena konkrēta pakete netiks rezervēta, un noliktavas darbību izpilde rindai sekos noteikumiem, kas tiek piemēroti saskaņā ar rezervēšanas politiku *Partijas lejpusējs\[novietojums\]*.

    Parasti šī lapa darbojas un ir tiek izmantota tādā pašā veidā, kā tā darbojas, un to izmanto krājumiem, kuriem ir ar tipu *Partijas augšpusējs\[novietojums\]* saistīta rezervāciju hierarhija. Tomēr tiek piemēroti tālāk norādītie izņēmumi.

    - Kopsavilkuma cilne **Avota rindai piesaistīti partijas numuri** tiek parādīti partijas numuri, kas ir rezervēti pasūtījuma rindai. Partijas vērtības režģī tiks rādītas visā pasūtījuma rindas izpildes ciklā, ieskaitot noliktavas apstrādes stadijas. Turpretī kopsavilkuma cilnē **Pārskats** regulāra pasūtījuma rindas rezervācija (tas ir, rezervēšana, kas tiek veikta dimensijām virs **Novietojuma** līmeņa) tiek rādīta režģī līdz vietai, kad tiek izveidots noliktavas darbs. Pēc tam rindas rezervāciju pārņem darba elements, un rindas rezervācija lapā vairs netiek rādīta. Kopsavilkuma cilne **Avota rindai piesaistīti partijas numuri** palīdz garantēt, ka pārdošanas pasūtījumu apsatrādātājs var apskatīt partiju numurus, kas tika piesaistīti klienta pasūtījumam jebkurā dzīves cikla laikā līdz rēķinu izrakstīšanai.
    - Papildus konkrētas partijas rezervēšanai lietotājs var manuāli atlasīt partijas konkrēto atrašanās vietu un numura zīmi, nevis ļaut sistēmai tās automātiski atlasīt. Šī iespēja ir saistīta ar pasūtījumu saistītas partijas rezervācijas mehānisma izkārtojumu. Kā minēts iepriekš, kad partijas numurs tiek rezervēts krājumam saskaņā ar rezervācijas politiku *Partijas lejpusējs\[novietojums\]*, sistēmai jārezervē visas dimensijas līdz atrašanās vietai. Tāpēc noliktavas darbs veiks tās pašas noliktavas dimensijas, ko rezervēja lietotāji, kuri strādāja ar pasūtījumiem, un tas varētu ne vienmēr atainot tādu krājuma glabāšanas novietojumu, kas izdošanas darbībām ir ērts vai pat iespējams. Ja pasūtījumu apstrādātāji ir informēti par noliktavas ierobežojumiem, tie, rezervējot partiju, varētu vēlēties manuāli atlasīt konkrētus novietojumus un noliktavas vienības. Šādā gadījumā lietotājam ir jāizmanto lapas galvenes funkcionalitāte **Parādīt dimensijas** un jāpievieno novietojuma un noliktavas vienība kopsavilkuma cilnes **Pārskats** režģī.

6. Lapā **Partijas rezervēšana** atlasiet partijas rindu **B11** un pēc tam atlasiet **Rezervēt rindu**. Automātiskās rezervēšanas laikā novietojuma un numura zīmju piešķiršanai nav norādīta loģika. Daudzumu laukā **Rezervācija** var ievadīt manuāli. Ievērojiet, ka kopsavilkuma cilnē **Avota rindai piesaistīti partijas numuri** partija **B11** tiek norādīta kā **Piešķirts**.

    ![Konkrēta partijas numura piešķiršana pārdošanas pasūtījuma rindai lapā Partijas rezervēšana.](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Pārdošanas pasūtījuma rindā norādītā daudzuma rezervāciju var veikt vairākām partijām. Tāpat tās pašas partijas rezervāciju var veikt vairākām vietām un noliktavas vienībām (ja novietojumiem ir iespējotas noliktavas vienības).
    >
    > Konkrētas partijas rezervēšana pārdošanas pasūtījuma rindā esošajam daudzumam arī var būt daļēja. Piemēram, 100 vienību kopējo daudzumu var rezervēt tā, ka 20 vienībām ir piešķirta konkrēta partija, turpretī 80 vienības tiek vietas un noliktavas līmeņos rezervētas jebkurai pieejamai partijai. Šādā gadījumā WMS veiks izdošanas operācijas, izmantojot divas atsevišķas darba rindas.

7. DOdieties uz **Preču informācijas pārvaldība** \> **Preces** \> **Nodotās preces**. Atlasiet savu vienību un pēc tam atlasiet **Pārvaldīt krājumu** \> **Skatīt** \> **Darbības**.

    ![Ar pasūtījumu saistīta rezervācija kā krājumu darbības tips.](media/Inventory-transactions-for-order-committed-reservation.png)

8. Pārskatiet vienuma krājumu transakcijas, kas saistītas ar pārdošanas pasūtījuma rindas rezervāciju.

    - Transakcijas, kurā lauks **Atsauces** ir iestatīts uz **Pārdošanas pasūtījums** un lauks **Izsniegšana** iestatīts uz **Rezervēts fiziski** parāda pasūtījuma rindas rezervāciju krājumu dimensijām virs līmeņa **Novietojums**. Saskaņā ar vienuma krājumu rezervēšanas hierarhiju šīs dimensijas ir novietojums, noliktava un krājuma statuss.
    - Transakcija, kurā lauks **Atsauce** ir iestatīts uz **Ar pasūtījumu saistīta rezervācija** un lauks **Izsniegšana** ir iestatīts uz **Rezervēts fiziski**, parāda pasūtījuma rindas rezervāciju konkrētam krājumam un visām krājuma dimensijām virs tā. Saskaņā ar vienuma krājumu rezervēšanas hierarhiju šīs dimensijas ir partijas numurs un novietojums. Šajā piemērā atrašanās vieta ir **Lielapjoma-001**.

9. Pārdošanas pasūtījuma virsrakstā atlasiet **Noliktava** \> **Darbības** \> **Pārvietot uz noliktavu**. Tagad pasūtījuma rinda ir viļņota, un tiek izveidota krava un darbs.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Tāda noliktavas darba pārskatīšana un apstrāde, kam ir ar pasūtījumu saistītu partiju numuri

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Noliktava** \> **Detalizēta informācija par darbu**

    Uz darbu, kas apstrādā izdošanas darbību partiju daudzumiem, kuri ir saistīti ar pārdošanas pasūtījuma rindu, attiecas tālāk norādītie raksturlielumi.

    - Lai izveidotu darbu, sistēma izmanto darba veidnes, bet ne novietojuma direktīvas. Visi standarta iestatījumi, kas definēti darba veidnēm, piemēram, maksimālais izdošanas rindu skaits vai noteikta mērvienība, tiks lietoti, lai noteiktu, kad jāizveido jauns darbs. Tomēr noteikumi, kas ar novietojuma direktīvām ir saistīti, lai identificētu izdošanas vietas, netiek ņemti vērā, jo ar pasūtījumu saistītajā rezervācija jau ir norādītas visas krājuma dimensijas. Šīs krājuma dimensijas ietver dimensijas noliktavas glabāšanas līmenī. Tāpēc darbs pārmanto šīs dimensijas, nekonsultējoties ar novietojuma direktīvām.
    - Partijas numurs netiek uzrādīts izdošanas rindā (kā tas ir darba rindas gadījumā, kas izveidota krājumam, kuram ir saistītā rezervācijas hierarhija *Partijas augšpusējs\[novietojums\]*.) Partijas numurs "no" un visas citas glabāšanas dimensijas tiek rādītas darba rindas darbu krājumu transakcijā, kam ir atsauce no saistītajām krājuma transakcijām.

        ![Noliktavas krājuma transakcija, kas izveidota no ar pasūtījumu saistītas rezervācijas.](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - Pēc darba izveides tiek noņemta vienuma krājuma transakcija, kurā lauks **Atsauce** ir iestatīts kā **Ar pasūtījumu saistīta rezervēšana**. Krājumu transakcija, kurā lauks **Atsauces** ir iestatīts uz **Darbs**, tagad ietver fizisko rezervāciju visām daudzuma krājumu dimensijām.

        Noliktavas darbības var turpināt darba izpildi parastajā kārtībā. Tomēr mobilās ierīces instrukcijās darbiniekam tiks norādīts izvēlēties konkrētu partijas numuru. Noliktavas vidēs, kur novietojumu pārvalda noliktavas vienības, pēc tam, kad darbinieks sasniedz vietu, kurā vairākās noliktavas vienībās tiek glabāta tā pati partija, viņš var izvēlēties no jebkuras noliktavas vienības, kas vēl nav rezervēta (piemēram, cita ar pasūtījumu saistīta rezervācija vai darbs, kas radies no šī tipa rezervācijas).

        Ja izrādās, ka nav praktiski izvēlēties no vietas, kas norādīta darba rindā, noliktavas operatori var izmantot vienu no tālāk norādītajām darbībām, lai novirzītu konkrētas partijas izdošanu no ērtākas atrašanās vietas.

        - Standarta darbība **Ignorēt atrašanās vietu** mobilajā ierīcē (ar nosacījumu, ka ir iespējots noliktavas darbinieka iestatījums **Atļaut izdošanas novietojuma ignorēšanu** )
        - Darbība **Mainīt atrašanāš vietu** lapā **Detalizēta informācija par darba sarakstu**. 

2. Mobilajā ierīcē pabeidziet darba izdošanu un nodošanu.

    Daudzums **10**, kas paredzēts partijas numuram **B11**, tagad ir izdots pārdošanas pasūtījuma rindai un ievietots atrašanās vietā **Aizmugurējās durvis**. Šajā brīdī tas ir sagatavots iekraušanai kravas automašīnā un nosūtīšanai uz debitora adresi.

## <a name="flexible-license-plate-reservation"></a>Elastīga numura zīmes rezervēšana

### <a name="business-scenario"></a>Biznesa scenārijs

Šajā scenārijā uzņēmums izmanto noliktavas pārvaldību un darba apstrādi un apstrādā kravu plānošanu atsevišķu palešu/konteineru līmenī ārpus Supply Chain Management pirms darba izveides. Šos konteinerus ataino numura zīmes krājumu dimensijās. Tāpēc, lai varētu izmantot šo pieeju, pirms saņemšanas darba veikšanas noteiktām numura zīmēm jābūt piešķirtām pārdošanas pasūtījuma rindām. Uzņēmums meklē elastību veidā, kā tiek apstrādāti numura zīmes rezervācijas noteikumi, lai šādi izturēšanās tiktu veikta sekojoši:

- Numura zīme var tikt ierakstīta un rezervēta laikā, kad pasūtījumu veic pārdošanas apstrādātājs, un to nevar pārņemt citas prasības. Šī rīcība palīdz garantēt, ka plānotā numura zīme tiek nosūtīta debitoram.
- Ja numura zīme vēl nav piešķirta pārdošanas pasūtījuma rindai, noliktavas personāls saņemšanas darba laikā var atlasīt numura zīmi, pēc pārdošanas pasūtījuma reģistrācijas un rezervācijas pabeigšanas.

### <a name="turn-on-flexible-license-plate-reservation"></a>Ieslēdziet elastīga numura zīmes rezervēšanu

Lai varētu izmantot elastīgu noliktavas vienības rezervāciju, diviem līdzekļiem ir jābūt iespējotiem sistēmā. Administratori var izmantot [līdzekļu pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļu statusu un tos ieslēgtu, ja tas nepieciešams. Šie līdzekļi ir jāaktivizē šādā secībā:

1. **Līdzekļa nosaukums:** *Elastīga noliktavas līmeņa dimensiju rezervācija*
1. **Līdzekļa nosaukums:** *elastīga, pasūtījuma izsniegta numura zīmes rezervēšana*

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a>Rezervēt noteiktu numura zīmi pārdošanas pasūtījumā

Lai aktivizētu numura zīmes rezervāciju pasūtījumā, ir jāatlasa izvēles rūtiņa **Atļaut rezervāciju pēc pieprasījuma pasūtījuma**, kas atrodas **Numura zīmes** līmenī, lapā **Krājumu rezervāciju hierarhija**, kas saistīta ar saistīto krājumu.

![Krājumu rezervēšanas hierarhijas lapa elastīgai numura zīmes rezervāciju hierarhijai.](media/Flexible-LP-reservation-hierarchy.png)

Jūs varat aktivizēt numura zīmes rezervāciju pasūtījumā jebkurā vietā jūsu izvietošanā. Šīs izmaiņas neietekmē rezervācijas vai atvērto noliktavas darbu, kas tika izveidots pirms izmaiņu rašanās. Tomēr jūs nevarat notīrīt **Atļaut rezervāciju pēc pieprasījuma pasūtījuma** izvēles rūtiņu, ja vienam vai vairākām atvērtajām, izejošajām krājumu darbībām, kam ir statuss *Rezervēts*, *Rezervēts pasūtījumā* vai *Rezervēts fiziski* krājumu darbības, pastāv vienam vai vairākiem vienumiem, kas saistīti ar šo rezervācijas hierarhiju.

Pat ja izvēles rūtiņa **Atļaut rezervāciju pēc pieprasījuma pasūtījuma** ir atlasīta **Numura zīmes** līmenī, joprojām ir iespējams, ka pasūtījumā *nav* rezervēta noteikta numura zīme. Šādā gadījumā tiek lietota noklusētā noliktavas operāciju loģika, kas ir derīga rezervāciju hierarhijai.

Lai rezervētu noteiktu numura zīmi, ir jāizmanto [Atvērto datu protokola (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process. Programmā var veikt šo rezervēšanu tieši no pārdošanas pasūtījuma, izmantojot komandas **Atvērt programmā Excel** opciju **Pasūtīt fiksētās rezervācijas katrai noliktavas vienībai**. Elementa datos, kas atvērti programmas Excel pievienojumprogrammā, ir jāievada šādi ar rezervāciju saistīti dati un pēc tam jāatlasa **Publicēt**, lai nosūtītu datus uz Supply Chain Management:

- Atsauce (tiek atbalstīta tikai *Pārdošanas pasūtījuma* vērtība.)
- Pasūtījuma numurs (vērtību var iegūt no partijas.)
- Laidiena ID
- Numura zīme
- Daudzums

Ja ir jārezervē noteikta numura zīme partijas izsekotajam krājumam, izmantojiet lapu **Partijas rezervēšana**, kā aprakstīts sadaļā [Ievadīt pārdošanas pasūtījuma informāciju](#sales-order-details).

Kad pārdošanas pasūtījuma rinda, kas izmanto pasūtījumu iesniegtu numura zīmes rezervāciju, tiek apstrādāta ar noliktavas operācijām, novietojuma direktīvas netiek izmantotas.

Ja noliktavas darba vienība sastāv no rindām, kas vienādas ar pilnu paleti, un tām ir ar numura zīme saistītie daudzumi, izdošanas procesu var optimizēt, izmantojot mobilās ierīces izvēlnes elementu, kur opcija **Apstrādāt ar numura zīmi** ir iestatīta uz *Jā*. Pēc tam noliktavas darbinieks var skenēt numura zīmi, lai pabeigtu izdošanu, nevis skenēt krājumus no darba pa vienam.

![Mobilās ierīces izvēlnes elements, kur opcija Rīkoties pēc numura zīmes ir iestatīta uz Jā.](media/Handle-by-LP-menu-item.png)

Tā kā **Rīkoties pēc numura zīmes** funkcionalitāte neatbalsta darbu, kas ietver vairākas paletes, labāk ir iegūt atsevišķu darba vienumu dažādām numura zīmēm. Lai izmantotu šo pieeju, pievienojiet **Pasūtījuma numura zīmes ID** lauku kā darba virsraksta pārtraukumu **Darba veidnes** lapā.

> [!NOTE]
> Ar pasūtījumu saistītā darba izveides procesā izdošanas darba rindām tiks piešķirta „ar pasūtījumu saistīta krājumu dimensijas” vērtība un nebūs iespējams tieši skatīt numura zīmes vērtību. Iestatot mobilās ierīces izvēlnes elementu, tiek atbalstīts tikai *lietotāja noteiktais* process.

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a>Piemērs scenārijs: iestatiet un apstrādājiet pasūtījuma fiksēto numura zīmes rezervāciju

Šis scenārijs parāda, kā iestatīt un apstrādāt pasūtījuma fiksēto numura zīmes rezervāciju.

### <a name="make-demo-data-available"></a>Padarīt demonstrācijas datus pieejamus

Šis scenārijs atsaucas uz vērtībām un ierakstiem, kas ir ietverti standarta demonstrācijas datos, kas tiek sniegti Supply Chain Management. Ja jūs vēlaties strādāt ar scenāriju, izmantojot šeit piedāvātās vērtības, pārliecinieties, ka strādājiet ar vidi, kurā ir instalēti demonstrācijas dati. Turklāt pirms sākšanas iestatiet uz **USMF** juridisko personu.

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a>Izveidot krājumu rezervācijas hierarhiju, kas atļauj numura zīmes rezervāciju

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Krājums \> Rezervēšanas hierarhija**.
1. Atlasiet **Jauns**.
1. Laukā **Nosaukums** ievadiet vērtību (piemēram, *FlexibleLP*).
1. Laukā **Apraksts** ievadiet vērtību (piemēram, *Flexible LP rezervācija*).
1. **Atlasītajā** sarakstā atlasiet **Partijas numuru**, **Sērijas numuru** un **Īpašnieku**.
1. Atlasiet **Noņemt** pogu ![bultiņa atpakaļ.](media/backward-button.png) lai pārvietotu atlasītus ierakstus uz **Pieejams** sarakstu.
1. Atlasiet **Labi**.
1. Dimensijas līmeņa rindā **Numura zīme** atzīmējiet izvēles rūtiņu **Atļaut rezervāciju pēc pieprasījuma pasūtījuma**. Automātiski tiek atlasīts līmenis **Novietojums** un to izvēles rūtiņu nevar dzēst.
1. Atlasiet **Saglabāt**.

### <a name="create-two-released-products"></a>Izveidot divas izlaistās preces

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Darbību rūtī atlasiet **Jauns**.
1. Dialoglodziņā **Jauns izlaists produkts** iestatiet sekojošus laukus:

    - **Preces numurs:** *Item1*
    - **Preces numurs:** *Item1*
    - **Krājumu modeļu grupa:** *FIFO*
    - **Krājuma grupa:** *Audio*
    - **Noliktavas dimensiju grupa:** *Izstrādājumi*
    - **Izsekošanas dimensiju grupa:** *Nav*
    - **Rezervāciju hierarhija:** *FlexibleLP*

1. Atlasiet **Labi**, lai izveidotu preci un aizvērtu dialoglodziņu.
1. Jaunā prece ir atvērta. Kopsavilkuma cilnē **Noliktava** iestatiet lauku **Vienības secības grupas ID** uz *ea*.
1. Atkārtojiet iepriekšējās darbības, lai izveidotu otru preci ar tādiem pašiem iestatījumiem, bet iestatiet **Preces numuru** un **Krājuma numura** laukus uz *Item2*.
1. Darbību rūtī cilne **Pārvaldīt krājumu** grupā **Skats** atlasiet **Rīcībā esošie krājumi**. Pēc tam atlasiet **Daudzuma pielāgošana**.
1. Pielāgojiet jauno vienību rīcībā esošos krājumus, kā norādīts šajā tabulā.

    | Vienums  | Noliktava | Novietojums | Numura zīme | Daudzums |
    |-------|-----------|----------|---------------|----------|
    | Item1 | 24        | FL-010   | LP01          | 10.       |
    | Item1 | 24        | FL-011   | LP02          | 10.       |
    | Item2 | 24        | FL-010   | LP01          | 5        |
    | Item2 | 24        | FL-011   | LP02          | 5        |

    > [!NOTE]
    > Ir jāizveido divas numura zīmes un izmantošanas vietas, kas ļauj izmantot jauktus krājumus, piemēram, *FL-010* un *FL-011*.

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a>Izveidot pārdošanas pasūtījumu un rezervēt noteiktu numura zīmi

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
1. Atlasiet **Jauns**.
1. Dialoglodziņā **Izveidot pārdošanas pasūtījumu** iestatiet sekojošas vērtības:

    - **Debitora konts:** *US-001*
    - **Noliktava:** *24*

1. Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Pārdošanas pasūtījuma izveide** un atveriet jauno pārdošanas pasūtījumu.
1. Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** pievienojiet rindu, kurai ir šādi iestatījumi:

    - **Preces numurs:** *Item1*
    - **Daudzums:** *10*

1. Pievienojiet otru pārdošanas pasūtījuma rindu, kam ir turpmāk aprakstītie iestatījumi:

    - **Preces numurs:** *Item2*
    - **Daudzums:** *5*

1. Atlasiet **Saglabāt**.
1. Kopsavilkuma cilnē **Rindas informācija** cilnē **Iestatīšana** atzīmējiet katras rindas **Laidiena ID** vērtību. Šīs vērtības tiks pieprasītas īpašas numura zīmes rezervēšanas laikā.

    > [!NOTE]
    > Lai rezervētu konkrētu numura zīmi, ir jāizmanto **Pasūtījuma rezervācijas uz licences plāksnīti** datu vienība. Lai rezervētu partijas izsekotu krājumu noteiktai numura zīmei, izmantojiet lapu **Partijas rezervēšana**, kā aprakstīts sadaļā [Ievadīt pārdošanas pasūtījuma informāciju](#sales-order-details).
    >
    > Ja ievadāt numura zīmi tieši pārdošanas pasūtījuma rindā un apstipriniet to sistēmā, noliktavas pārvaldības apstrāde netiks izmantota rindai.

1. Atlasiet **Atvērt programmā Microsoft Office**, atlasiet **Pasūtījuma rezervācijas uz licences plāksnīti** un lejupielādējiet failu.
1. Atveriet lejupielādēto failu programmā Excel un atlasiet **Iespējot rediģēšanu**, lai iespējotu Excel pievienojumprogrammas palaišanu.
1. Ja pirmo reizi palaižat Excel pievienojumprogrammu, atlasiet **Uzticēties šai pievienojumprogrammai**.
1. Ja tiek prasīts pierakstīties, atlasiet **Pierakstīties** un pēc tam pierakstieties, izmantojot tos pašus akreditācijas datus, ko izmantojāt, lai pierakstītos programmā Supply Chain Management.
1. Lai rezervētu krājumu noteiktai numura zīmei, programmas Excel pievienojumprogrammā atlasiet **Jauns**, lai pievienotu rezervācijas rindu, un pēc tam iestatiet šādas vērtības:

    - **Laidiena ID:** ievadiet **Laidiena ID** vērtību, kas atrasta pārdošanas pasūtījuma rindai *Item1*.
    - **Numura zīme:** *LP02*
    - **ReservedInventoryQuantity:** *10*

1. Atlasiet **Jauns**, lai pievienotu citu rezervāciju, un iestatiet šādas vērtības:

    - **Laidiena ID:** ievadiet **Laidiena ID** vērtību, kas atrasta pārdošanas pasūtījuma rindai *Item2*.
    - **Numura zīme:** *LP02*
    - **ReservedInventoryQuantity:** *5*

1. Programmas Excel pievienojumprogrammā atlasiet **Publicēt**, lai nosūtītu datus uz Supply Chain Management.

    > [!NOTE]
    > Rezervēšanas rinda sistēmā parādīsies tikai tad, ja publicēšana ir pabeigta bez kļūdām.

1. Atgriezieties pie Supply Chain Management. 
1. Lai pārskatītu krājuma rezervāciju, kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** izvēlnē **Krājumi** atlasiet **Uzturēt \> Rezervācija**. Ievērojiet, ka pārdošanas pasūtījuma rinda *Item1*, krājums *10* ir rezervēts un pārdošanas pasūtījuma rindai *Item2*, krājums *5* ir rezervēts.
1. Lai pārskatītu krājumu darbības, kas saistītas ar pārdošanas pasūtījuma rindas rezervāciju, kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** izvēlnē **Krājumi** atlasiet **Skatīt \> Darbības**. Ievērojiet, ka ar rezervāciju ir saistītas divas darbības: viena, kur **Atsauces** lauks ir iestatīts uz *Pārdošanas pasūtījumu* un viens, kur **Atsauces** lauks ir iestatīts kā *Pasūtījuma rezervācija*.

    > [!NOTE]
    > Transakcijas, kurā lauks **Atsauce** ir iestatīts uz *Pārdošanas pasūtījums* parāda pasūtījuma rindas rezervāciju krājumu dimensijām, kas ir virs līmeņa **Novietojums** (vietne, noliktava, krājumu statuss). Darbība, kurā **Atsauces** lauks ir iestatīts kā *Pasūtījuma rezervācija*, parāda pasūtījuma rindas rezervāciju konkrētai numura zīmei un vietai.

1. Lai palaistu pārdošanas pasūtījums, darbību rūtī cilnē **Noliktava** grupā **Darbības**, atlasiet **Pārvietot uz noliktavu**.

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a>Pārskatiet un apstrādājiet noliktavas darbu ar piešķirtajām licenču plāksnēm

1. Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** izvēlnē **Noliktava** atlasiet **Detalizēta informācija par darbu**.

    Ja rezervācija tiek veikta noteiktai paketei, sistēma neizmanto novietojuma direktīvas, kad tā izveido darbu pārdošanas pasūtījumam, kas izmanto numura zīmes rezervāciju. Tā kā pasūtījuma apstrādātā rezervācija norāda visas krājumu dimensijas, ieskaitot novietojumu, novietojuma direktīvas nav jāizmanto, jo šīs krājumu dimensijas ir vienkārši ievadītas darbā. Tās tiek rādītas sadaļā **No krājumu dimensijām** lapa **Darba krājumu darbības**.

    > [!NOTE]
    > Pēc darba izveides tiek noņemta vienuma krājuma transakcija, kurā lauks **Atsauce** ir iestatīts kā *Ar pasūtījumu saistīta rezervēšana*. Krājumu transakcija, kurā lauks **Atsauces** ir iestatīts uz *Darbs*, tagad ietver fizisko rezervāciju visām daudzuma krājumu dimensijām.

1. Mobilajā ierīcē pabeidziet saņemšanu un darbu izdošanu, izmantojot izvēlnes elementu, kurā ir atzīmēta izvēles rūtiņa **Rīkoties pēc numura zīmes**.

    > [!NOTE]
    > **Rīkoties pēc numura zīmes** funkcionalitāte palīdz apstrādāt visu numura zīmi. Ja ir jāapstrādā daļa no numura zīmes, šo funkcionalitāti nevar izmantot.
    >
    > Ieteicams izveidot atsevišķu darbu katrai numura zīmei. Lai to panāktu, **Darba veidnes** lapā izmantojiet funkciju **Darba virsraksta pārtraukumi**.

    Numura zīmes *LP02* tagad ir izdota pārdošanas pasūtījuma rindām un tiek nodota uz *Baydoor* novietojumu. Šajā brīdī tas ir sagatavots iekraušanai un nosūtīšanai uz debitora adresi.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Tāda noliktavas darba izņēmumu apstrāde, kam ir ar pasūtījumu saistītu partiju numuri

Uz noliktavas darbu ar pasūtījumu saistītu partijas numuru izdošanai attiecas tā pati standarta noliktavas izņēmuma apstrāde un darbības kā uz parastu darbu. Parasti atvērto darbu vai darba rindu var atcelt, to var pārtraukt, jo lietotāja novietojums ir pilns, tā var būt ar saīsinātu izdošanu un tā var būt atjaunināta kustības dēļ. Tāpat var tikt samazināts izdotais pabeigtā darba daudzums, vai arī darbu var atsaukt.

Visām šīm izņēmuma apstrādes darbībām tiek piemērots šāds pamatprincips: partijas numurs, kas tika rezervēts debitoram, nekad nevar tikt aizstāts ar citu partijas numuru, bet tā noliktavas dimensijas (novietojums un noliktavas vienība) var mainīt, izmantojot vai nu manuālu atjauninājumu, ko veic lietotājs, vai sistēmas automātisku atjaunināšanu. Automātiskās atjaunināšanas pamatā ir tā pati izlases veida noliktavas dimensiju piešķiršana, kas tiek piemērota, kad automātiski tika rezervēta konkrēta partija, bet netika norādītas noliktavas dimensijas.

### <a name="example-scenario"></a>Piemēra situācija

Šī scenārija piemērs ir situācija, kad iepriekš pabeigtais darbs tiek izdots, izmantojot funkciju **Samazināt izdoto daudzumu**. Šajā piemērā tiek pieņemts, ka jums jau ir pabeigtas darbības, kas aprakstītas [Piemēra scenārijā: partijas numura piešķiršana](#Example-batch-allocation). Tas turpinās no šī parauga.

1. Dodieties uz **Noliktavas pārvaldība** \> **Kravas** \> **Aktīvās kravas**.
2. Atlasiet noslodzi, kas tika izveidota saistībā ar jūsu pārdošanas pasūtījuma sūtījumu.
3. No kopsavilkuma cilnes **Noslodzes pasūtījuma rindas** atlasiet **Samazināt izdoto daudzumu**.
4. Lapas **Samazināt izdoto daudzumu** laukā **Pārvietot uz atrašānās vietu** atlasiet **FL-001**.
5. Laukā **Pārvietot uz noliktavas vienību** atlasiet **LP33**.
6. Režģa laukā **Krājumu daudzums līdz izdošanai** ievadiet **10**.
7. Atlasiet **Labi**.

Tālak norādīti neizdošanas darbības rezultāti.

- Iepriekš slēgtā darba statuss ir iestatīts uz **Atcelts**.
- Jauns tipa **Krājuma kustība** darbs ir izveidots neizdotajam **10** daudzumam ar partijas numuru **B11**. Šis darbs apzīmē pārvietošanos no novietojuma **Aizmugurējās durvis** uz noliktavas vienību **LP33** novietojumā **FL-001**. Statuss jāiestata uz **Slēgts**.
- Sistēma atkārtoti rezervē partijas numuru, kas tika sākotnēji pasūtīts, un piešķir novietojuma un noliktavas vienības ID. (Šis process ir līdzvērtīgs funkcijas **Rezerves rinda** palaišanai noteikta partijas numura pasūtījuma rindai). Rezultātā partija **B11** tiek rādīta kā piesaistīta lapas **Partijas rezervēšana** kopsavilkuma cilnē **Avota rindai piesaistīti partijas numuri**, un laukā **Rezervācija** partijas numuram **B11** ir norādīts daudzums **B10**. Turklāt lauks **Vieta** ir iestatīts kā **FL-001**, un lauks **Noliktavas vienība** ir iestatīts uz **LP11**. (Šos laukus var pievienot režģim, ja tie nav redzami.)

Tālāk norādītās tabulas sniedz pārskatu, kas parāda, kā sistēma apstrādā ar pasūtījumu saitītu partijas rezervāciju konkrētām noliktavas darbībām. Lai interpretētu tabulu saturu, pieņemiet, ka katra noliktavas darbība tiek izpildīta, ņemot vērā esošo noliktavas darbu, ko nosaka ar pasūtījumu saistītas partijas rezervācija, vai ka katras noliktavas darbības izpilde ietekmē šī tipa darbu.

> [!NOTE]
> Šajās tabulās kolonna "Partijas daudzums ir pieejams" norāda, vai partijas daudzums ir pieejams papildus daudzumam, kas vai nu jau ir rezervēts pašreizējām, ar pasūtījumu saistītās rezervācijām, vai arī to jau ir rezervējis noliktavas darbs, kas rodas no šī tipa rezervācijām.

#### <a name="override-the-pick-location-on-the-open-work"></a>Izdošanas novietojuma ignorēšana atvēŗtā darbā

<table>
<thead>
<tr>
<th>Galvenie iestatīšanas parametri</th>
<th>Partijas daudzums ir pieejams</th>
<th>Galvenās lietotāja darbības</th>
<th>Noliktavas darbs</th>
<th>Ar pasūtījumu saistītas partijas rezervēšana</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Opcija <strong>Atļaut izdošanas novietojuma ignorēšanu</strong> ir aktivizēta darbiniekam.</td>
<td>Jā</td>
<td>
<ol>
<li>Kad sākat izdošanas darbu, Warehouse Management mobile programmā atlasiet izvēlnes elementu <strong>Ignorēt atrašanās vietu</strong>.</li>
<li>Atlasiet <strong>Ieteikt</strong>.</li>
<li>Apstipriniet jauno atrašanās vietu, kas tiek piedāvāta, pamatojoties uz partijas daudzuma pieejamību.</li>
</ol>
</td>
<td>Pašreizējā darbā tiek veiktas tālāk norādītās darbības.
<ul>
<li>Novietojums izdošanas rindā tiek atjaunināts uz jauno novietojumu. (Ja novietojumu pārvalda noliktavas vienība, darba krājumu transakcijai tiek piešķirta izlases veda noliktavas vienība, un darbinieks var izdot no jebkuras noliktavas vienības, kurai ir pieejams daudzums.)</li>
<li>Ja daudzums jaunajā atrašanās vietā ir atrodams vairāk nekā vienā noliktavas vienībā, sākotnējā izdošanas rinda tiek sadalīta vairākās rindās, lai atbilstu katrai noliktavas vienībai.</li>
</ul>
</td>
<td>Nav attiecināms</td>
</tr>
<tr>
<td>Nē</td>
<td>
<ol>
<li>Kad sākat izdošanas darbu, Warehouse Management mobile programmā atlasiet izvēlnes elementu <strong>Ignorēt atrašanās vietu</strong>.</li>
<li>Manuāli ievadiet atrašānās vietu.</li>
</ol>
</td>
<td>Darbība <strong>Ignorēt atrašanās vietu</strong> nav iespējama. Tā neizdodas, un tiek izmesta kļūda.</td>
<td>Nav attiecināms</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Poga Pilna – darba rindas sadale, jo lietotāja atrašanās vietā radusies pārpilde

<table>
<thead>
<tr>
<th>Galvenie iestatīšanas parametri</th>
<th>Partijas daudzums ir pieejams</th>
<th>Galvenās lietotāja darbības</th>
<th>Noliktavas darbs</th>
<th>Ar pasūtījumu saistītas partijas rezervēšana</th>
</tr>
</thead>
<tbody>
<tr>
<td>Opcija <strong>Atļaut darba sadali</strong> ir aktivizēta mobilās ierīces izvēlnes elementā.</td>
<td>Nav attiecināms</td>
<td>
<ol>
<li>Kad apstrādājat izdošanas darbu, Warehouse Management mobile programmā atlasiet izvēlnes elementu <strong>Pilna</strong>.</li>
<li>Laukā <strong>izdošanas daudzums</strong> ievadiet daļēju nepieciešamās izdošanas daudzumu, lai norādītu pilnu noslodzi.</li>
</ol>
</td>
<td>
<ul>
<li>Pašreizējā darbā daudzums tiek atjaunināts uz atlikušo izdodamo daudzumu.</li>
<li>Izdotajam daudzumam tiek izveidots un slēgts jauns darbs.</li>
</ul></td>
<td>Nav attiecināms</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Izdotā pabeigtā darba daudzuma (no kravas) samazināšana

<table>
<thead>
<tr>
<th>Galvenie iestatīšanas parametri</th>
<th>Partijas daudzums ir pieejams</th>
<th>Galvenās lietotāja darbības</th>
<th>Noliktavas darbs</th>
<th>Ar pasūtījumu saistītas partijas rezervēšana</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Nav attiecināms</td>
<td>Jā</td>
<td>
<ol>
<li>Atveriet lapu <strong>Samazināt izdoto daudzumu</strong> no noslodzes rindas.</li>
<li>Ievadiet pilnu daudzumu, kuram tiks anulēta izdošana.</li>
<li>Atlasiet "pārvietot uz" atrašanās vietu/noliktavas vienību.</li>
</ol>
</td>
<td>
<ul> 
<li>Ar kravas rindu saistītais darbs ir atcelts.</li>
<li>Jaunais krājuma pārvietošanas darbs ir izveidots un slēgts.</li>
</ul>
</td>
<td>Daudzums ir atkārtoti rezervēts vienai partijai. Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</td>
</tr>
<tr>
<td>Nē</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Daudzums ir atkārtoti rezervēts tai pašai partijai un tai pašai atrašanās vietai un noliktavas vienībai (ja atrašanās vietu pārvalda noliktavas vienība), kas tika ievadīta izdošanas anulēšanas laikā.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Krājuma pārvietošana noliktavā

> [!NOTE]
> Šī noliktavas darbība ir piemērojama tikai **Darba izveides procesa** tipa kustībai, nevis kustībai pēc veidnes.

<table>
<thead>
<tr>
<th>Galvenie iestatīšanas parametri</th>
<th>Partijas daudzums ir pieejams</th>
<th>Galvenās lietotāja darbības</th>
<th>Noliktavas darbs</th>
<th>Ar pasūtījumu saistītas partijas rezervēšana</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Darbiniekam ir aktivizēta opcija <strong>Atļaut krājumu kustību saistītajā tīklā</strong>.</td>
<td>Jā</td>
<td>
<ol>
<li>Kustības sākšana Warehosue Management mobile programmā.</li>
<li>Enter "no" un "uz" atrašanās vietas.</li>
</ol></td>
<td>
<ul>
<li>Visā esošajā darbā, ko ietekmēja pārvietošana, izdošanas atrašanās vieta ir atjaunināta uz jaunu "uz" atrašanās vietu.</li>
<li>Jaunais krājuma pārvietošanas darbs ir izveidots un slēgts.</li>
</ul>
</td>
<td>Visas esošās rezervācijas, ko ietekmējusi daudzuma pārvietošana no dotās atrašanās vietas, ir rezervētas vienai partijai. Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</td>
</tr>
<tr>
<td>Nē</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Visas esošās rezervācijas, ko ietekmējusi daudzuma pārvietošana no dotās atrašanās vietas, ir rezervētas tai pašai partijai un jaunai "uz" atrašanās vietai un noliktavas vienībai (ja atrašanās vietu pārvalda noliktavas vienība).</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Izdotā pabeigtā darba daudzuma (no kravas vai kopuma) atsaukšana

<table>
<thead>
<tr>
<th>Galvenie iestatīšanas parametri</th>
<th>Partijas daudzums ir pieejams</th>
<th>Galvenās lietotāja darbības</th>
<th>Noliktavas darbs</th>
<th>Ar pasūtījumu saistītas partijas rezervēšana</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Nav attiecināms</td>
<td>Jā</td>
<td>
<ol>
<li>Atveriet lapu <strong>Atsaukt darbu</strong>.</li>
<li>Pieprasījuma lapā atlasiet opciju <strong>Atstāt krājumus pašreizējā atrašanās vietā</strong>.</li>
</ol>
</td>
<td>Viss ar kravu saistītais darbs ir atcelts.</td>
<td>Daudzums ir atkārtoti rezervēts vienai partijai. Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</td>
</tr>
<tr>
<td>Nē</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Daudzums tiek atkārtoti rezervēts vienai partijai, atrašanās vietai un noliktavas vienībai, kur daudzums tika atstāts atgriešanas brīdī.</td>
</tr>
<tr>
<td>Jā</td>
<td>
<ol>
<li>Atveriet lapu <strong>Atsaukt darbu</strong>.</li>
<li>Pieprasījuma lapā atlasiet opciju <strong>Piešķirt krājumus šai atrašanās vietai</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Pašreizējais darbs ir atcelts.</li>
<li>Jaunais krājuma pārvietošanas darbs ir izveidots un slēgts.</li>
</ul>
</td>
<td>Daudzums ir atkārtoti rezervēts vienai partijai. Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</td>
</tr>
<tr>
<td>Nē</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Daudzums tiek atkārtoti rezervēts vienai partijai, atrašanās vietai un noliktavas vienībai, kam daudzums tika piešķirts atcelšanas brīdī.</td>
</tr>
<tr>
<td>Jā/Nē</td>
<td>
<ol>
<li>Atveriet lapu <strong>Atsaukt darbu</strong>.</li>
<li>Pieprasījuma lapā atlasiet opciju <strong>Pārvietot krājumus uz šo atrašanās vietu</strong>.</li>
</ol>
</td>
<td>Atcelšana netiek atbalstīta.</td>
<td>Nav attiecināms</td>
</tr>
<tr>
<td>Jā/Nē</td>
<td>
<ol>
<li>Atveriet lapu <strong>Atsaukt darbu</strong>.</li>
<li>Pieprasījuma lapā atlasiet opciju <strong>Pārvietot krājumus, pamatojoties uz novietojuma direktīvām</strong>.</li>
</ol>
</td>
<td>Atcelšana netiek atbalstīta. </td>
<td>Nav attiecināms</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Sīsināt izdošanas daudzumu – reģistrēt daudzumu kā fiziski neatrodamu novietojuma/noliktavas vienībā, kamēr veicat izdošanas darbu

<table>
<thead>
<tr>
<th>Galvenie iestatīšanas parametri</th>
<th>Partijas daudzums ir pieejams</th>
<th>Galvenās lietotāja darbības</th>
<th>Noliktavas darbs</th>
<th>Ar pasūtījumu saistītas partijas rezervēšana</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Nav</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Nē</strong>.</td>
<td>Jā</td>
<td>
<ol>
<li>Kad apstrādājat izdošanas darbu, Warehouse Management mobile programmā atlasiet izvēlnes elementu <strong>Īss</strong>.</li>
<li>Laukā <strong>Izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</li>
<li>Laukā <strong>Pamatojums</strong> ievadiet <strong>Nav atkārtotas sadales</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Pašreizējais darbs tiek slēgts, un izdotais daudzums ir 0 (nulle).</li>
<li><strong>Uzskaites</strong> tipa krājumu transakcija un <strong>Pārdošanas</strong> izsniegšanas veids tiek izveidots, lai attēlotu pielāgojumu.</li>
</ul>
</td>
<td>Daudzums ir atkārtoti rezervēts vienai partijai. Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</td>
</tr>
<tr>
<td>Nē</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>
<ul>
<li>Saīsinātas izdošanas darbība neizdodas, un tiek izmesta kļūda.</li>
<li>Pašreizējais darbs paliek atvērts.</li>
</ul>
</td>
<td>Nav attiecināms</td>
</tr>
<tr>
<td rowspan='2'>Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Nav</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Jā</strong>.</td>
<td>Jā</td>
<td>
<ol>
<li>Kad apstrādājat izdošanas darbu, Warehouse Management mobile programmā atlasiet izvēlnes elementu <strong>Īss</strong>.</li>
<li>Laukā <strong>Izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</li>
<li>Laukā <strong>Pamatojums</strong> ievadiet <strong>Nav atkārtotas sadales</strong>.</li>
</ol>
</td>
<td>
<ul>
<li>Pašreizējais darbs tiek slēgts, un izdotais daudzums ir 0 (nulle).</li>
<li><strong>Uzskaites</strong> tipa krājumu transakcija un <strong>Pārdošanas</strong> izsniegšanas veids tiek izveidots, lai attēlotu pielāgojumu.</li>
</ul>
</td>
<td>Visas esošās rezervācijas, ko ietekmējusi daudzuma koriģēšana saīsinātās izdošanas vietā, ir rezervētas vienai partijai. Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</td>
</tr>
<tr>
<td>Nē</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Visas esošās rezervācijas, ko ietekmējusi daudzuma koriģēšana saīsinātās izdošanas vietā, ir noņemtas.</td>
</tr>
<tr>
<td>Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Manuāls</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Nē/Jā</strong>. Turklāt darbiniekam tiek aktivizēta opcija <strong>Atļaut manuālu krājumu pārdalīšanu</strong>.</td>
<td>Jā</td>
<td>
<ol>
<li>Kad apstrādājat izdošanas darbu, Warehouse Management mobile programmā atlasiet izvēlnes elementu <strong>Īss</strong>.</li>
<li>Laukā <strong>Saīsinātās izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</li>
<li>Laukā <strong>Pamatojums</strong> atlasiet <strong>Saīsinātā izdošana, izmantojot manuālu pārdalīšanu</strong>.</li>
<li>Sarakstā atlasiet atrašanās vietu / noliktavas vienību.</li>
</ol>
</td>
<td>
<ul>
<li>Pašreizējā darbā tiek veiktas tālāk norādītās darbības.
<ul>
<li>Pašreizējā izdošanas līnija tiek slēgta, un izdotais daudzums ir 0 (nulle).</li>
<li>Novietošanas rinda ir atcelta.</li>
<li>Izveidota jauna izdošanas rinda. Tā izmanto atrašanās vietu / noliktavas vienību, ko izvēlējies lietotājs.</li>
<li>Izveidota jauna novietošanas rinda.</li>
</ul>
</li>
<li><strong>Uzskaites</strong> tipa krājumu transakcija un <strong>Pārdošanas</strong> izsniegšanas veids tiek izveidots, lai attēlotu pielāgojumu.</li>
</ul>
</td>
<td>Nav attiecināms</td>
</tr>
<tr>
<td>Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Manuāls</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Nē</strong>. Turklāt darbiniekam tiek aktivizēta opcija <strong>Atļaut manuālu krājumu pārdalīšanu</strong>.</td>
<td>Nē</td>
<td>
<ol>
<li>Kad apstrādājat izdošanas darbu, Warehouse Management mobile programmā atlasiet izvēlnes elementu <strong>Īss</strong>.</li>
<li>Laukā <strong>Saīsinātās izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</li>
<li>Laukā <strong>Pamatojums</strong> atlasiet <strong>Saīsinātā izdošana, izmantojot manuālu pārdalīšanu</strong>.</li>
</ol>
</td>
<td>Saīsinātas izdošanas darbība neizdodas, un tiek izmesta kļūda.</td>
<td>Nav attiecināms</td>
</tr>
<tr>
<td>Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Manuāls</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Jā</strong>. Turklāt darbiniekam tiek aktivizēta opcija <strong>Atļaut manuālu krājumu pārdalīšanu</strong>.</td>
<td>Nē</td>
<td>
<ol>
<li>Kad apstrādājat izdošanas darbu, Warehouse Management mobile programmā atlasiet izvēlnes elementu <strong>Īss</strong>.</li>
<li>Laukā <strong>Saīsinātās izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</li>
<li>Laukā <strong>Pamatojums</strong> atlasiet <strong>Saīsinātā izdošana, izmantojot manuālu pārdalīšanu</strong>.</li>
<li>Sarakstā atlasiet atrašanās vietu / noliktavas vienību.</li>
</ol>
</td>
<td>
<ul>
<li>Pašreizējā darbā tiek veiktas tālāk norādītās darbības.
<ul>
<li>Pašreizējā izdošanas līnija tiek slēgta, un izdotais daudzums ir 0 (nulle).</li>
<li>Novietošanas rinda ir atcelta.</li>
</ul>
</li>
<li><strong>Uzskaites</strong> tipa krājumu transakcija un <strong>Pārdošanas</strong> izsniegšanas veids tiek izveidots, lai attēlotu pielāgojumu.</li>
</ul>
</td>
<td>Visas esošās rezervācijas, ko ietekmējusi daudzuma koriģēšana saīsinātās izdošanas vietā / noliktavas vienībā, ir noņemtas.</td>
</tr>
<tr>
<td>Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Automātisks</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Jā/Nē</strong>.</td>
<td>Nav attiecināms</td>
<td>
<ol>
<li>Kad apstrādājat izdošanas darbu, Warehouse Management mobile programmā atlasiet izvēlnes elementu <strong>Īss</strong>.</li>
<li>Laukā <strong>Saīsinātās izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</li>
<li>Laukā <strong>Pamatojums</strong> atlasiet <strong>Saīsinātā izdošana, izmantojot automātisku pārdalīšanu</strong>.</li>
</ol>
</td>
<td>Saīsināta izdošana, kas ietver automātisku pārdalīšanu, netiek atbalstīta.</td>
<td>Saīsināta izdošana, kas ietver automātisku pārdalīšanu, netiek atbalstīta.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Mainīt krājuma statusu

> [!NOTE]
> Šo noliktavas darbību var veikt no vairākiem ieejas punktiem. Šeit redzamajā piemēra izmantota darbība **Krājumu statusa maiņa** lapā **Rīcībā esošie krājumi pēc atrašanās vietas**.

<table>
<thead>
<tr>
<th>Galvenie iestatīšanas parametri</th>
<th>Partijas daudzums ir pieejams</th>
<th>Galvenās lietotāja darbības</th>
<th>Noliktavas darbs</th>
<th>Ar pasūtījumu saistītas partijas rezervēšana</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Cilnē <strong>Noliktava</strong>, ierakstā <strong>Noliktava</strong> lauks <strong>Noņemt rezervācijas un atzīmes</strong> ir iestatīts uz <strong>Rezervācijas</strong> vai <strong>Atzīmes un rezervācijas</strong>.</td>
<td>Jā</td>
<td>
<ol>
<li>Atlasiet noteiktu atrašanās vietu.</li>
<li>Atlasiet rindu, kurai ir noteikts krājums, atrašānās vieta un noliktavas vienība (ja atrašanās vietu pārvalda noliktavas vienība).</li>
<li>Atlasiet <strong>Krājumu statusa maiņa</strong>.</li>
<li>Iestatiet lauku <strong>Krājuma statuss</strong> uz <strong>Bloķēšana</strong>.</li>
</ol>
</td>
<td>Krājumu statusa izmaiņas nav atļautas daudzumiem, kas ir rezervēti darbam.</td>
<td>
<ul>
<li>Daudzums ir atkārtoti rezervēts vienai partijai. Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</li>
<li>Lai attēlotu izmaiņas krājumu statusa dimensijā, izveidotas divas <strong>Krājumu statusa maiņas</strong> tipa krājumu transakcijas.</li>
<li>Lai attēlotu bloķētā daudzuma rezervāciju, izveidota <strong>Krājuma bloķēšanas</strong> tipa krājumu transakcija un <strong>Rezervēts fiziski</strong> izsniegšanas veids.</li>
</ul>
</td>
</tr>
<tr>
<td>Nē</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Krājumu statusa izmaiņas nav atļautas daudzumiem, kas ir rezervēti darbam.</td>
<td>
<ul>
<li>Rezervēšana tiek noņemta.</li>
<li>Lai attēlotu izmaiņas krājumu statusa dimensijā, izveidotas divas <strong>Krājumu statusa maiņas</strong> tipa krājumu transakcijas.</li>
<li>Lai attēlotu bloķētā daudzuma rezervāciju, izveidota <strong>Krājuma bloķēšanas</strong> tipa krājumu transakcija un <strong>Rezervēts fiziski</strong> izsniegšanas veids.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'>Cilnē <strong>Noliktava</strong>, ierakstā <strong>Noliktava</strong> lauks <strong>Noņemt rezervācijas un atzīmes</strong> ir iestatīts uz <strong>Nav</strong>.</td>
<td>Jā</td>
<td>
<ol>
<li>Atlasiet noteiktu atrašanās vietu.</li>
<li>Atlasiet rindu, kurai ir noteikts krājums, atrašānās vieta un noliktavas vienība (ja atrašanās vietu pārvalda noliktavas vienība).</li>
<li>Atlasiet <strong>Krājumu statusa maiņa</strong>.</li>
<li>Iestatiet lauku <strong>Krājuma statuss</strong> uz <strong>Bloķēšana</strong>.</li>
</ol>
</td>
<td>Krājumu statusa izmaiņas nav atļautas daudzumiem, kas ir rezervēti darbam.</td>
<td>Daudzums ir atkārtoti rezervēts vienai partijai. Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</td>
</tr>
<tr>
<td>Nē</td>
<td>Skatīt iepriekšējo rindu.</td>
<td>Krājumu statusa izmaiņas nav atļautas daudzumiem, kas ir rezervēti darbam.</td>
<td>Krājumu statusa izmaiņas nav atļautas.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Ierobežojumi

- Pielāgojama noliktavas līmeņa dimensiju rezervēšanas funkcionalitāte neatbalsta tālāk norādītos līdzekļus.

    - Pieļaujamā svara pārvaldība
    - Negatīvi fiziskie krājumi
    - Rezervēšana pret pasūtīto piegādi
    - Pārsūtīšanas pasūtījumi un izejmateriālu izdošana

- Konteineru konsolidācijas kārtulai par iepakošanu pēc direktīvas vienības ir ierobežojumi. Ar pasūtījumu saistītām rezervācijām mēs iesakām neizmantot konteineru veidošanas veidnes, kur ir iespējots lauks **Iepakot pēc direktīvas vienības**. Pašreizējā versija novietojuma direktīvas netiek izmantotas, kad tiek izveidots noliktavas darbs. Tāpēc konteinerizācijas kopuma darbības laikā tiek lietota tikai viszemākā vienība vienību secību grupā (krājumu uzskaites vienība).

## <a name="see-also"></a>Skatiet arī

- [Partiju numuri modulī Noliktavas pārvaldība](/dynamicsax-2012/appuser-itpro/batch-numbers-in-warehouse-management)
- [Tās pašas partijas rezervēšana pārdošanas pasūtījumam](../sales-marketing/reserve-same-batch-sales-order.md)
- [Vecākās partijas izdošana mobilajā ierīcē](pick-oldest-batch.md)
- [Partijas un numura zīmes apstiprināšana](batch-and-license-plate-confirmation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]