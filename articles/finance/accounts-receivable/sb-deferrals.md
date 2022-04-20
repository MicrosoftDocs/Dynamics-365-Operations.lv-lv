---
title: Ieņēmumi un izdevumu atliktie ieņēmumi no abonementa rēķiniem
description: Šajā tēmā skaidrots, kā abonementa norēķinos iestatīt ieņēmumus un izdevumu atliktos maksājumus.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 5ff8d2f4663c53bf6dece1ef9af6609d5f0c5b50
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544561"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>Ieņēmumi un izdevumu atliktie ieņēmumi no abonementa rēķiniem

Šajā tēmā skaidrots, kā abonementa norēķinos iestatīt un izmantot ieņēmumus un izdevumu atliktos maksājumus. Atlikto maksājumu grafiki vienmēr tiek balstīti uz pamata oriģinālo dokumentu vai norēķinu grafiku un ir atkarīgi no tā. Tā kā tās ir izveidotas, pamatojoties uz noklusētajām vērtībām, tās nevar ievadīt vai izveidot atsevišķi.

Ieņēmumu un izdevumu atlikto maksājumu iestatīšanas un lietošanas process notiek vairākās lapās:

- **Ieņēmumu un izdevumu atlikto maksājumu parametru** lapā varat noteikt uzņēmuma preferences.
- Lapā Atlikto **maksājumu noklusējums** var iestatīt noklusējuma kontus un veidnes, kas tiek izmantotas atlikto maksājumu grafikiem.
- Lapās **Atlikto maksājumu veidnes** **un Atlikto maksājumu veidnes**, kas pamatotas uz notikumiem, var definēt veidnes, kas tiek izmantotas atlikto maksājumu grafikiem.
- Lapā Visi **atlikto maksājumu grafiki** var skatīt un rediģēt jebkuru atlikto maksājumu grafiku.

Ieņēmumus un izdevumu atliktos maksājumus var izmantot kopā ar periodiskiem līguma rēķiniem.

## <a name="revenue-and-expense-deferral-parameters"></a>Ieņēmumu un izdevumu atlikšanas parametri

Ieņēmumu **un izdevumu atlikto maksājumu parametru** lapa ietver sekojošos laukus.

| Lauks | Apraksts |
|---|---| 
| **Cilne** Grafiks | |
| Vienāds ar periodu | <p>Norādiet, vai dienu skaits periodā tiek izmantots, kad atlikto maksājumu grafikam tiek aprēķināta summa par periodu:</p><ul><li>**Jā** – katra perioda summa ir vienāda neatkarīgi no perioda dienu skaita. Daļēji periodi (piemēram, periodi atliktā maksājuma grafika sākumā vai beigās) tiks pārvērtāti.</li><li>**Nē** – summa tiek aprēķināta, pamatojoties uz dienu skaitu katrā periodā.</li></ul><p>Jūs variet ignorēt šo iestatījumu darbības līmenī.</p> |
| Pārdošanas atlaides atlikšanas opcija | <p>Norādiet, vai tiek izveidoti atsevišķi atlikto maksājumu grafiki atlaides un pārdošanas pasūtījuma summām:</p><ul><li>**Atsevišķs atlaides grafiks** – atlaides summa tiek turēta atsevišķi no ieņēmumu summas.<p>Šajā gadījumā, izveidojot un pēc tam grāmatojot pārdošanas pasūtījumu, tiek izveidoti divi atlikto maksājumu grafiki. Atlaides un ieņēmumu summas tiks grāmatotas dažādos atlikto maksājumu kontos.</p></li><li>**Sapludināt atlaidi ar ieņēmumiem** – atlaides summa ir apvienota ar ieņēmumu summu. Tiek izveidots viens atlikto maksājumu grafiks, un gan atlaides summa, gan ieņēmumu summa tiek grāmatota vienā atlikto maksājumu kontā.<p>Šajā gadījumā, izveidojot un pēc tam grāmatojot pārdošanas pasūtījumu, tiek izveidots viens atlikto maksājumu grafiks. Gan atlaides summa, gan ieņēmumu summa tiek grāmatota vienā atlikto maksājumu kontā.</p></li></ul><p>**Piezīme.** Lai piemērotu atlaides krājumiem, kas izmanto nenobīdāmo ieņēmumu līdzekli, atlasiet **opciju Atsevišķs grafiks atlaidei**. Pēc tam atlaides var piemērot visiem krājumiem, neņemot vērā to, vai tiek izmantota funkcija Nenodzēsti ieņēmumi. Ja ir **atlasīta opcija Sapludināt atlaidi** ar ieņēmumiem, atlaides nevar piemērot krājumiem, kam tiek izmantota funkcija Nenoslietotie ieņēmumi.</p> |
| Pirkšanas atlaides atlikšanas opcija | <p>Atlasiet, vai atlaides un pirkšanas pasūtījuma summām tiek izveidoti atsevišķi atlikto maksājumu grafiki:</p><ul><li>**Atsevišķs atlaides grafiks** – atlaides summa tiek turēta atsevišķi no izdevumu summas.<p>Šajā gadījumā tiek izveidoti divi atlikto maksājumu grafiki, kad pirkšanas pasūtījums tiek izveidots un pēc tam iegrāmatots. Atlaides un izdevumu summas tiek grāmatotas dažādos atlikto maksājumu kontos.</p></li><li>**Sapludināt atlaidi ar ieņēmumiem** – atlaides summa ir kombinēta ar izdevumu summu. Tiek izveidots viens atlikto maksājumu grafiks, un gan atlaides summa, gan izdevumu summa tiek grāmatota vienā atlikto maksājumu kontā.<p>Šajā gadījumā tiek izveidots viens atlikto maksājumu grafiks, kad pirkšanas pasūtījums tiek izveidots un pēc tam iegrāmatots. Gan atlaides summa, gan izdevumu summa tiek iegrāmatota vienā atliktā maksājuma kontā.</p></li></ul> |
| Konsolidēt iepriekšējos periodus | <p>Norādiet, vai atlikto maksājumu grafika rindas iepriekšējiem periodiem tiek konsolidētas:</p><ul><li>**Jā** – ja atliktā maksājuma sākuma datums ir periodā pirms darbības datuma, visas summas līdz darbības datuma periodam tiek kombinētas vienā atliktā maksājuma grafika rindā.</li><li>**Nē** – summas no visiem periodiem tiek glabātas atsevišķās atlikto maksājumu grafika rindās.<p>Ja atliktā maksājuma sākuma datums ir tajā pašā periodā vai vēlākā periodā nekā darbības datums, šī opcija neietekmē darbību.</p></li></ul><p>Šo iestatījumu var atjaunināt darbību līmenī.</p> |
| Noklusējuma atlikšanas sākuma datums | <p>Atlasiet noteikumu, kas tiek lietots atlikto maksājumu grafika sākuma datuma noteikšanai:</p><ul><li>**Darbības datums** – izmantojiet darbības datumu kā sākuma datumu.</li><li>**Pašreizējā mēneša sākums** – izmantojiet pirmo no pašreizējā mēneša kā sākuma datumu. Ja darbības datums ir pirmais no jebkura mēneša, pirmais no pašreizējam mēnesim ir sākuma datums.</li><li>**Nākamā mēneša sākums** – izmantojiet pirmo no nākamā mēneša kā sākuma datumu. Ja darbības datums ir pirmajā, tiek izmantots darbības datums. Pretējā gadījumā tiek izmantots nākamā mēneša pirmais mēnesis.</li><li>**15. noteikums** – ja darbības datums ir starp pirmo un piecpadsmito, izmantojiet šī mēneša pirmo datumu kā sākuma datumu. Ja darbības datums ir sešpadsmitais vai vēlāk, kā sākuma datumu izmantojiet nākamā mēneša pirmo datumu.</li></ul><p>Šo iestatījumu var atjaunināt darbību līmenī.</p> |
| Īstermiņa atlikšanas metode | <p>Atlasiet īstermiņa atliktā maksājuma metodi: Nav, Atritina **·** **periodus** vai Fiksēts **gads**.</p><p>|
| Atliktā maksājuma grāmatošanas metode | <p>Atlasiet metodi, kas tiek izmantota atlikto maksājumu darbību veidojiet:</p><ul><li>**Bilance –** izmantojiet bilances grāmatošanas metodi atlikto maksājumu darbību veidojiet.</li><li>**Peļņa un zaudējumi** – izmantojiet peļņas un zaudējumu grāmatošanas metodi atlikto maksājumu darbību izveidošanai. Kad darbības ir iegrāmatotas, jūs variet pārskatīt rēķina dokumentu, lai redzētu papildu ierakstus, kas līdzsvaro sākotnējās atpazīšanas un atpazīšanas korespondējošās summas.</li></ul> |
| Revertēt kredīta peļņu un zaudējumus | <p>**Piezīme.** Šis lauks ir pieejams tikai tad, ja lauka **Atlikto maksājumu grāmatošanas** metode iestatījums ir **Peļņa un zaudējumi**.</p><p>Norādiet, vai peļņas un zaudējumu summas tiek apgrieztas, ja rēķinu grafikam vai pārdošanas pasūtījumam tiek piemērota atgriešana, darba attiecību pārtraukšana vai atmaksa:</p><ul><li>**Jā** – atgriezt peļņas un zaudējumu summas un atlikto maksājumu grafikam lietot kredīta korekcijas summu.<p>Ja atgriešana notiek pusceļā caur rēķina periodu, summas tiek apgrieztas.</p></li><li>**Nē** – nav izveidota atgriešanas darbība peļņai un zaudējumiem, ja rēķinu grafikam vai pārdošanas pasūtījumam tiek piemērota atgriešana, darba attiecību pārtraukšana vai atmaksa.</li></ul> |
| **Cilne Atpazīšana** | |
| Automātiski grāmatot virsgrāmatas žurnālus | <p>Norādiet, vai žurnāla ieraksti, kas izveidoti ar ieņēmumu un izdevumu atliktajiem izdevumiem, tiek grāmatoti automātiski:</p><ul><li>**Jā** - automātiski grāmatot žurnāla ierakstus, kas izveidoti ar ieņēmumu un izdevumu atliktajiem izdevumiem.<p>**Padoms:** Atlasot **Jā**, var palīdzēt novērst uzskaites nesakritības, ko izraisa manuālas dokumentu izmaiņas.</p></li><li>**Nē** - žurnāla ieraksti, kas izveidoti ar ieņēmumu un izdevumu atliktajiem izdevumiem, nav automātiski grāmatoti. Visi žurnāli ir jāgrāmato manuāli.</li></ul> |
| Izveidot atzīšanas žurnāla kopsavilkumu | <p>Norādiet, vai pēc noklusējuma atpazīšanas dokumenti tiek konsolidēti:</p><ul><li>**Jā** – izveidojiet vienu dokumentu visām atpazīšanas rindām, kurām ir vienāds datums. Visas dokumenta rindas, kurām ir viens konts, tiek konsolidētas vienā rindā.</li><li>**Nē** – izveidojiet dokumentu katrai atpazīšanas rindai.</li></ul><p>Šo iestatījumu var atjaunināt lapā Atpazīšanas **apstrāde**.</p> |
| Žurnāla noklusējuma nosaukums | Atlasiet žurnāla nosaukumu žurnāliem, kas izveidoti no ieņēmumu un izdevumu atlikto maksājumu procesiem, piemēram, atzīšanas apstrādes. |
| Atzīšanas žurnāla rindas apraksts | <p>Atlasiet aprakstu, kas parādās žurnāla dokumenta rindas aprakstā:</p><ul><li>**Grafika rindas datumi** – parāda grafika rindu datumus žurnāla rindas aprakstā.</li><li>**Sākotnējās darbības detaļas** – rāda sākotnējo darbību informāciju žurnāla rindas aprakstā.<p>**Piemērs:** USMF-0001, CIV-00839, ieņēmumi no programmatūras</p></li></ul> |
| **Cilne Numuru sērijas** | Lietojiet šo cilni, lai iestatītu noklusējuma vērtības nomas numuru sērijām. Numuru sērijas ģenerēšanas ceļvedis tiek izmantots, lai automātiski ģenerētu un piešķirtu numuru sērijas. Numuru sērija nav jāmaina, ja vien ģenerētajā numuru sērijā nav jāveic manuālas izmaiņas. |
| Grafika numurs | Numurs, kas ir secība, kuru izmanto atlikto maksājumu grafikiem. |

## <a name="deferral-templates"></a>Atlikšanas veidnes

Izmantojiet lapu **Atlikto maksājumu veidnes**, lai definētu lineārās veidnes, kas tiek izmantotas atlikto maksājumu grafikiem.

Daži no veidnes izmantošanas āciem:

* Atliktā maksājuma garums tiek aprēķināts automātiski.
* Var atlikto maksājumu grafikiem, kuriem ir periodi, kuros atpazīšana ir izlaista.
* Jūs varat automatizēt atliktos maksājumus, piešķirot veidni precei, preču grupai, preču kategorijai, debitoriem vai debitoru grupai. Veidnes piešķire tiek veikta no atlikto **maksājumu noklusējumu** lapas.

Veidnēm ir pieejami vairāki periodu intervāli: ikdienas, mēneša vai finanšu periodi.

Veidnes rindas sastāv no tipa (Atpazīts **vai** **Izlaists**) un perioda garuma. Izlaisto rindu summa atlikto maksājumu grafika rindās ir 0 (nulle). Šī darbība var būt noderīga, ja nevēlaties atpazīt ieņēmumus visos periodos.

### <a name="create-a-deferral-template"></a>Izveidot atlikto maksājumu veidni

Lai izveidotu atlikto maksājumu veidni, sekojiet šiem soļiem.

1. Lapā Atlikto **maksājumu** veidnes atlasiet **Jauns**.
2. Laukā **Veidne** ievadiet nosaukumu.
3. Ievadiet aprakstu laukā **Apraksts**.
4. Laukā **Perioda biežums** atlasiet perioda biežumu.
5. Atlasiet **Pievienot**, lai pievienotu rindu rindu saraksta augšpusē, vai atlasiet Pievienot, **lai** pievienotu rindu saraksta apakšai.
6. **Laukā** Tips atlasiet perioda tipu.
7. **Laukā Perioda** garums norādiet perioda garumu.
8. 5. un 7. darbību atkārtojiet katrai papildu rindai, kas nepieciešama.
9. Atlasiet **Saglabāt**.

## <a name="deferral-defaults"></a>Atlikšanas noklusējumi

Izmantojiet lapu Atlikto **maksājumu noklusējums, lai iestatītu noklusējuma atlikto maksājumu kontus krājumiem un piešķirtu noklusētās** veidnes atliktajiem krājumiem. Var arī iestatīt atlikto maksājumu kontus maksām un piešķirt veidnes atliktajiem maksājumiem.

**Atliktais daudzums pēc krājuma**

Darbībām, kurām ir krājums (piemēram, pārdošanas pasūtījumi), varat piešķirt kontus un veidnes specifiskiem krājumiem un debitoriem. Ja darbība ir atlikta, šie iestatījumi tiks izmantoti kā noklusētās vērtības. Lai darbību atliktu pēc noklusējuma iestatīt, krājumi ir jāiestata lapā Atliktie **krājumi**.

**Atliktie maksājumu uz kontu**

Darbībām, kurās nav krājumu (piemēram, Virsgrāmatas žurnālu), var norādīt atlikto maksājumu kontus. Ja šie konti tiek lietoti darbības rindā, darbība tiek automātiski atzīmēta kā atlikta. Atbilstošā veidne un atpazīšanas konts tiks piešķirts darbības rindai.

**Visi darbību tipi (piemēram, cilnēs Pārdošanas pasūtījums, Pirkšana un Virsgrāmatas žurnāli)**

Lapas konti ir galvenie konti, kuriem nav finanšu dimensiju. Atpazīšanas konta finanšu dimensijas tiek ņemtas no debitora vai krājuma, pamatojoties uz jūsu organizāciju.

Katrai veidnes rindai jābūt lineārā vai uz notikumu balstītai veidnei. Tam nevar būt abi.

### <a name="for-sales-orders"></a>Pārdošanas pasūtījumiem

Lai norādītu atlikto maksājumu noklusējuma vērtības pārdošanas pasūtījumiem, sekojiet šiem soļiem.

1. Cilnē Pārdošanas **pasūtījums** atlasiet atlikto maksājumu tipu.
2. Lai pievienotu rindu, atlasiet **Pievienot**.
3. Laukā **Krājuma** kods atlasiet krājuma kodu. Krājuma kods nosaka atlikto maksājumu noklusējuma vērtību pielietošanu.
4. Norādiet, kā tiek lietots krājuma kods:

    * Ja krājuma **koda lauks** ir iestatīts uz **Tabula** **vai Grupa**, atlasiet krājuma saistību **laukā Krājumu** saistība.
    * Ja krājuma **koda** lauks ir iestatīts uz **Kategorija**, kategorijas relācijā atlasiet **kategorijas relāciju**.
    * Ja lauks **Krājuma kods** ir iestatīts uz **Visi**, noklusētās vērtības attiecas uz visiem piemērojamiem ierakstiem.

5. Norādiet, kā tiek lietots konta kods:

    * Ja konta **koda lauks** ir iestatīts uz **Tabula** **vai Grupa**, atlasiet konta saistību **laukā Kontu** saistība.
    * Ja lauks **Konta kods** ir iestatīts uz **Visi**, konts attiecas uz visiem ierakstiem.

6. Laukā **Galvenais** konts atlasiet atliktā maksājuma galveno kontu.
7. Ja lauka **Atlikto maksājumu grāmatošanas** **metode** vērtība ir Peļņa un zaudējumi, **·** **atlasiet sākotnējo ieņēmumu kontu laukā Sākotnējo ieņēmumu konts un ieņēmumu korespondējošo kontu laukā Ieņēmumu korespondējošais** konts.
8. Ja īstermiņa **atlikto maksājumu metodes** **·** **lauks** ir iestatīts uz Atritina periodus vai fiksētu gadu, **atlasiet īstermiņa atlikto maksājumu kontu laukā Īstermiņa atlikto maksājumu** konts.
9. Veidnei var atlasīt Pievienot **,** lai pievienotu rindu.
10. Laukā **Krājuma** kods atlasiet krājuma kodu.
11. Norādiet, kā tiek lietots krājuma kods:

    * Ja krājuma **koda lauks** ir iestatīts uz **Tabula** **vai Grupa**, atlasiet krājuma saistību **laukā Krājumu** saistība.
    * Ja krājuma **koda lauks** ir iestatīts uz **Kategorija**, atlasiet kategorijas saistību **laukā Kategorijas** relācija.
    * Ja lauks **Krājuma kods** ir iestatīts uz **Visi**, noklusētās vērtības attiecas uz visiem piemērojamiem ierakstiem.

12. Norādiet, kā tiek lietots konta kods:

    * Ja konta **koda lauks** ir iestatīts uz **Tabula** **vai Grupa**, atlasiet konta saistību **laukā Kontu** saistība.
    * Ja lauks **Konta kods** ir iestatīts uz **Visi**, konts attiecas uz visiem piemērojamajiem ierakstiem.
    * Atlasiet lineāro veidni laukā **Lineārā** veidne vai veidne, kas pamatota uz notikumu **, laukā Veidne, kas pamatota uz** notikumu.

13. Atlasiet **Saglabāt**.

### <a name="for-purchase-orders"></a>Pirkšanas pasūtījumiem

Lai norādītu atlikto maksājumu noklusējuma vērtības pirkšanas pasūtījumiem, sekojiet šiem soļiem.

1. Cilnē Iepirkšana **atlasiet** atlikto maksājumu tipu.
2. Lai pievienotu rindu, atlasiet **Pievienot**.
3. Laukā **Krājuma** kods atlasiet krājuma kodu.
4. Norādiet, kā tiek lietots krājuma kods:

    * Ja krājuma **koda lauks** ir iestatīts uz **Tabula** **vai Grupa**, atlasiet krājuma saistību **laukā Krājumu** saistība.
    * Ja krājuma **koda lauks** ir iestatīts uz **Kategorija**, atlasiet kategorijas saistību **laukā Kategorijas** relācija.
    * Ja lauks **Krājuma kods** ir iestatīts uz **Visi**, noklusētās vērtības attiecas uz visiem piemērojamiem ierakstiem.

5. Norādiet, kā tiek lietots konta kods:

    * Ja konta **koda lauks** ir iestatīts uz **Tabula** **vai Grupa**, atlasiet konta saistību **laukā Kontu** saistība.
    * Ja lauks **Konta kods** ir iestatīts uz **Visi**, konts attiecas uz visiem piemērojamajiem ierakstiem.

6. Laukā **Galvenais** konts atlasiet atliktā maksājuma galveno kontu.
7. Ja lauka **Atlikto maksājumu grāmatošanas** **metode** vērtība ir Peļņa un zaudējumi, **·** **atlasiet sākotnējo ieņēmumu kontu laukā Sākotnējo ieņēmumu konts un ieņēmumu korespondējošo kontu laukā Ieņēmumu korespondējošais** konts.
8. Ja īstermiņa **atlikto maksājumu metodes** **·** **lauks** ir iestatīts uz Atritina periodus vai fiksētu gadu, **atlasiet īstermiņa atlikto maksājumu kontu laukā Īstermiņa atlikto maksājumu** konts.
9. Veidnei atlasiet **Pievienot**, lai pievienotu rindu. 
10. Laukā **Krājuma** kods atlasiet krājuma kodu.
11. Norādiet, kā tiek lietots krājuma kods:

    * Ja krājuma **koda lauks** ir iestatīts uz **Tabula** **vai Grupa**, atlasiet krājuma saistību **laukā Krājumu** saistība.
    * Ja krājuma **koda lauks** ir iestatīts uz **Kategorija**, atlasiet kategorijas saistību **laukā Kategorijas** relācija.
    * Ja lauks **Krājuma kods** ir iestatīts uz **Visi**, noklusētās vērtības attiecas uz visiem piemērojamiem ierakstiem.

12. Norādiet, kā tiek lietots konta kods:

    * Ja konta **koda lauks** ir iestatīts uz **Tabula** **vai** Grupa, izvēlieties konta saistību konta **relācijā**.
    * Ja lauks **Konta kods** ir iestatīts uz **Visi**, konts attiecas uz visiem piemērojamajiem ierakstiem.
    * Atlasiet lineāro veidni laukā **Lineārā** veidne vai veidne, kas pamatota uz notikumu **, laukā Veidne, kas pamatota uz** notikumu.

13. Atlasiet **Saglabāt**.

### <a name="for-general-journals"></a>Virsgrāmatas žurnāliem

Lai norādītu atlikto maksājumu noklusējuma vērtības virsgrāmatas žurnāla ierakstiem, sekojiet šiem soļiem.

1. Atlasiet cilni **Virsgrāmatas** žurnāls.
2. Atliktā maksājumam atlasiet **Pievienot**, lai pievienotu rindu.
3. Ja īstermiņa **atlikto maksājumu metodes** **·** **lauks** ir iestatīts uz Atritina periodus vai fiksētu gadu, **atlasiet īstermiņa atlikto maksājumu kontu laukā Īstermiņa atlikto maksājumu** konts.
4. Laukā **Atlikto maksājumu** konts atlasiet atlikto maksājumu kontu.
5. Laukā **Atzīšanas konts** atlasiet atzīšanas kontu.
6. Ja lauka **Atlikto maksājumu grāmatošanas** **metode** vērtība ir Peļņa un zaudējumi, **·** **atlasiet sākotnējo ieņēmumu kontu laukā Sākotnējo ieņēmumu konts un ieņēmumu korespondējošo kontu laukā Ieņēmumu korespondējošais** konts.
7. Atlasiet lineāro veidni laukā **Lineārā** veidne vai veidne, kas pamatota uz notikumu **, laukā Veidne, kas pamatota uz** notikumu.
8. Atlasiet **Saglabāt**.

### <a name="for-free-text-invoices"></a>Brīvā teksta rēķiniem

Lai noteiktu atlikto maksājumu noklusējuma vērtības brīvā teksta rēķiniem, sekojiet šiem soļiem.

1. Atlasiet cilni **Brīva teksta rēķins**.
2. Atliktā maksājumam atlasiet **Pievienot**, lai pievienotu rindu.
3. Norādiet, kā tiek lietots konta kods:

    * Ja konta **koda lauks** ir iestatīts uz **Tabula** **vai Grupa**, atlasiet konta saistību **laukā Kontu** saistība.
    * Ja laukam **Konta kods** ir iestatīts uz **Visi**, konta kods attiecas uz visiem piemērojamajiem ierakstiem.

4. Laukā **Atlikto maksājumu** konts atlasiet atlikto maksājumu kontu.
5. Ja īstermiņa **atlikto maksājumu metodes** **·** **lauks** ir iestatīts uz Atritina periodus vai fiksētu gadu, **atlasiet īstermiņa atlikto maksājumu kontu laukā Īstermiņa atlikto maksājumu** konts.
6. Laukā **Atzīšanas konts** atlasiet atzīšanas kontu.
7. Ja lauka **Atlikto maksājumu grāmatošanas** **metode** vērtība ir Peļņa un zaudējumi, **·** **atlasiet sākotnējo ieņēmumu kontu laukā Sākotnējo ieņēmumu konts un ieņēmumu korespondējošo kontu laukā Ieņēmumu korespondējošais** konts.
8. Atlasiet lineāro veidni laukā **Lineārā** veidne vai veidne, kas pamatota uz notikumu **, laukā Veidne, kas pamatota uz** notikumu.
9. Atlasiet **Saglabāt**.

### <a name="for-invoice-journals"></a>Rēķinu žurnāliem

Lai norādītu atlikto maksājumu noklusējuma vērtības rēķinu žurnāla ierakstiem, sekojiet šiem soļiem.

1. Atlasiet cilni **Rēķinu** žurnāls.
2. Atliktā maksājumam atlasiet **Pievienot**, lai pievienotu rindu.
3. Norādiet, kā tiek lietots konta kods:

    * Ja konta **koda lauks** ir iestatīts uz **Tabula** **vai Grupa**, atlasiet konta saistību **laukā Kontu** saistība.
    * Ja laukam **Konta kods** ir iestatīts uz **Visi**, konta kods attiecas uz visiem piemērojamajiem ierakstiem.

4. Laukā **Atlikto maksājumu** konts atlasiet atlikto maksājumu kontu.
5. Ja īstermiņa **atlikto maksājumu metodes** **·** **lauks** ir iestatīts uz Atritina periodus vai fiksētu gadu, **atlasiet īstermiņa atlikto maksājumu kontu laukā Īstermiņa atlikto maksājumu** konts.
6. Laukā **Atzīšanas konts** atlasiet atzīšanas kontu.
7. Ja lauka **Atlikto maksājumu grāmatošanas** **metode** vērtība ir Peļņa un zaudējumi, **·** **atlasiet sākotnējo ieņēmumu kontu laukā Sākotnējo ieņēmumu konts un ieņēmumu korespondējošo kontu laukā Ieņēmumu korespondējošais** konts.
8. Atlasiet lineāro veidni laukā **Lineārā** veidne vai veidne, kas pamatota uz notikumu **, laukā Veidne, kas pamatota uz** notikumu.
9. Atlasiet **Saglabāt**.

### <a name="items-that-are-deferred-by-default"></a>Krājumi, kas atlikti pēc noklusējuma

Izmantojiet lapu **Atliktie krājumi pēc noklusējuma,** lai definētu, kuri krājumi pēc noklusējuma tiek atlikti. Varat iestatīt darbību tipus, kam tiks atlikti krājumi. Varat norādīt, vai atsevišķs krājums ir atlikts vai visa krājumu grupa vai kategorija.

Iestatot krājumus kā atliktos maksājumus, atlasiet noklusējuma kontus un veidnes lapā Atlikto **maksājumu noklusējums**. Ja konti un veidnes nav atlasīti, darbību rindas, kur šie krājumi tiek ievadīti, netiks atliktas.

Krājumiem, kas atlikti, balstoties uz pārdošanas vai pirkšanas kategoriju, ar ko tie ir saistīti, atlikto maksājumu iestatījumi ir balstīti uz kategoriju. Tomēr, ja kategorija nav atlasīta **kategorijas** relācijas laukā, tiek izmantoti tās kategorijas atliktā maksājuma iestatījumi, kas ir augstāka rangā. Piemēram, jūs pievienojat mājas **video pārdošanas** kategoriju, bet ne transportlīdzekļa **pārdošanas** kategoriju. Kad pievienojat atlikto maksājumu krājumu, kas ir saistīts **ar** kategoriju Tāpēc, **precei tiek izmantoti mājas video** atlikto maksājumu iestatījumi.

### <a name="set-up-deferred-items"></a>Iestatīt atliktos krājumus

Lai iestatītu krājumus, kas tiek atlikti pēc noklusējuma, sekojiet šiem soļiem.

1. Lapā Krājumi **, kas atlikti pēc noklusējuma**, atlasiet cilni, kuru vēlaties: Pārdošanas **pasūtījums vai** Iepirkšana **·**.
2. Lai pievienotu rindu, atlasiet **Pievienot**.
3. Laukā **Krājuma** kods atlasiet krājuma kodu.
4. Norādiet, kā tiek lietots krājuma kods:

    * Ja krājuma **koda lauks** ir iestatīts uz **Grupa** vai **Tabula**, atlasiet krājuma saistību **laukā Krājumu** saistība.
    * Ja krājuma **koda lauks** ir iestatīts uz **Kategorija**, atlasiet kategorijas saistību **laukā Kategorijas** relācija.

5. 2. un 4. darbību atkārtojiet katrai papildu rindai, kas nepieciešama.
6. Atlasiet **Saglabāt**.

## <a name="deferred-charges"></a>Atliktās maksas

Izmantojiet lapu **Atlikto maksājumu maksājumi**, lai noteiktu, kuras maksas pēc noklusējuma ir atliktas.

> [!NOTE]
> * Pašlaik atliktās maksas ir pieejamas tikai pārdošanas pasūtījumiem.
> * Maksas var atlikt tikai rindu līmenī. Lai atliktu maksu pārdošanas pasūtījuma virsraksta līmenī, maksājumu pārdošanas pasūtījumā var iestatīt kā atliktu krājumu atsevišķā rindā.
> * Lai atliktu maksu brīvā teksta rēķinam, maksa ir jāievada kā atsevišķa atliktā rēķina rinda.
> * Šī funkcionalitāte nav pieejama atbalsta maksām un ieņēmumu sadales funkcionalitātei.

### <a name="set-up-deferred-charges"></a>Iestatīt atliktās maksas

Lai iestatītu atliktās maksas, sekojiet šiem soļiem.

1. Lapā Atlikto **maksājumu** papildmaksas atlasiet **Pievienot**, lai pievienotu rindu.
2. Laukā **Maksas** kods atlasiet maksas kodu.
3. Laukā **Maksas** relācija atlasiet maksas saistību.
4. 1. un 3. darbību atkārtojiet katrai nepieciešamai papildu rindai.
5. Atlasiet **Saglabāt**.

## <a name="event-based-deferral-templates"></a>Uz notikumiem balstītas atlikšanas veidnes

Izmantojiet lapu Uz **notikumu balstītas atlikto** **maksājumu veidnes, lai definētu uz notikumiem balstītas** atlikto maksājumu veidnes, kuras var izmantot atlikto maksājumu darbībām un piešķirt atlikto maksājumu noklusējuma lapā.

### <a name="create-an-event-based-template"></a>Uz notikumiem balstītas veidnes izveide

Lai izveidotu atlikto maksājumu veidni, kas pamatota uz notikumu, sekojiet šiem soļiem.

1. Lapā Uz notikumiem **balstītas atlikto** maksājumu veidnes atlasiet **Jauns**.
2. **Laukā** Veidne ievadiet unikālu veidnes nosaukumu.
3. Ievadiet aprakstu laukā **Apraksts**.
4. Laukā **Sadalījuma** tips atlasiet sadalījuma tipu:

    * **Mainīgā summa** – piešķiriet konkrētu summu katrai ievadītai rindai.
    * **Vienāda summa** – piešķiriet to pašu summu katrai ievadītai rindai. 
    * **Procenti** – sadaliniet summu, kas ir balstīta uz katrai rindai ievadīto procentuālo vērtību.
    * **Pabeigtības procenti** – piešķiriet uzkrāto pabeigtības vērtību katrai ievadītajai rindai.
    * **Mainīgais** daudzums – piešķiriet noteiktu daudzumu katrai ievadītai rindai.

5. Ja vēlaties **, lai katra notikuma** rinda rēķinā **tiktu** sadalīta ar vienību skaitu, iestatiet opciju Izveidot atsevišķus notikumus pa vienībām uz Jā. Iestatiet to **uz Nē**, ja nevēlaties sadalīt notikuma rindas.
6. Laukā **Termiņa beigu** konts atlasiet termiņa beigu kontu.
7. Atlasiet **Pievienot**, lai pievienotu rindu rindu saraksta augšpusē, vai atlasiet Pievienot, **lai** pievienotu rindu saraksta apakšai.
8. **Laukā** Apraksts ievadiet notikuma aprakstu.
9. Ja Sadalījuma **tipa lauks** ir iestatīts uz **Procenti**, norādiet sadalījuma procentus **laukā Sadalījuma** procenti. Procentuālajai vērtībai ir jābūt diapazonā no 0 (nulle) līdz 100. Ja atstājat lauku Sadalījuma **procenti** tukšu, procenti tiek uzskatīti par 0. Visu procentu summa ir parādīta laukā **Kopējie** procenti lapas apakšpusē, un tai jābūt vienādai ar 100.
10. Laukā **Mēneši līdz derīguma** termiņa beigām norādiet mēnešu skaitu, cik ilgi notikums ir derīgs. Darbības atliktā maksājuma beigu datums tiek automātiski ievadīts, pamatojoties uz šo vērtību.
11. Atzīmējiet izvēles **rūtiņu Atpazīt pēc grāmatošanas**, lai automātiski atpazītu ieņēmumus, kad darbība ir grāmatota. Ja atstājat izvēles rūtiņu tukšu, ieņēmumi jāatpazīst manuāli.
12. Laukā **Atzīšanas konts** atlasiet notikuma atpazīšanas kontu, ja notikums izmanto citu kontu, kas nav viss atlikto maksājumu grafiks. Šis lauks tiek lietots kopā ar izvēles rūtiņu **Atpazīt pēc grāmatošanas**.
13. 7. un 12. darbību atkārtojiet katrai nepieciešamai papildu rindai.
14. Atlasiet **Saglabāt**.
