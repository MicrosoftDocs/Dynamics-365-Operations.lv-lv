---
title: Rēķinos neiekļautie ieņēmumi
description: Šajā rakstā ir izskaidrots, kā iestatīt krājumus un kontus, lai abonementa norēķinos izmantotu nenodzēsto ieņēmumu līdzekli.
author: JodiChristiansen
ms.date: 10/10/2022
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
ms.openlocfilehash: adf6f06ee454f368fa194315a87cfdec9e5e13da
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644173"
---
# <a name="unbilled-revenue"></a>Rēķinos neiekļautie ieņēmumi

Šajā rakstā ir aprakstīta nenos ieņēmumu aprēķināšanas funkcija, kas ļauj bilancē iekļaut visas rēķinu plānošanas summas. Šīs summas ir iekļautas nenosummoto ieņēmumu kontā un nenobīdīto ieņēmumu korespondējošā kontā, un rēķins par līgumu tiek izrakstīts ar apmaksas palīdzību.

## <a name="set-up-unbilled-revenue"></a>Iestatīt nenopildāmos ieņēmumus

Lai iestatītu nenopildītus ieņēmumus, veiciet šos soļus.

- Lapā Periodiskie **līguma norēķinu parametri** iestatiet laukus sadaļā Nenokārtoti **ieņēmumi**.
- Nenos ieņēmumu funkcija var tikt izmantota krājumiem, kuru krājuma **tipa lauks** ir iestatīts uz **Standarta**. To var izmantot arī atlikto maksājumu krājumiem. Lai izmantotu nenokārtotos ieņēmumus ar īstermiņa funkcionalitāti, iestatiet īstermiņa opcijas lapā **Periodiskā līguma norēķinu parametri**.

Lai iestatītu krājumus, kas izmanto nenopildāmos ieņēmumus, sekojiet šiem soļiem.

1. Cilnes Krājumi **lapā Nenosācāmo** ieņēmumu **iestatījums** atlasiet **Pievienot**.
2. Jaunā rindā krājuma kodā **atlasiet** krājuma kodu.
3. Laukā **Krājumu** saistība atlasiet krājumu saistību.
4. Atkārtojiet šīs darbības, lai pievienotu vairāk rindu.
5. Atlasiet **Saglabāt**.

Lai iestatītu krājumus un nenopildāmos ieņēmumu kontus, veiciet šos soļus.

1. Cilnes Konti **lapā Nenosācāmo** ieņēmumu **iestatījums** atlasiet **Pievienot**.
2. Jaunā rindā krājuma kodā **atlasiet** krājuma kodu.
3. Laukā **Krājumu** saistība atlasiet krājumu saistību.
4. Atlasiet kontus nenobīdītajiem ieņēmumiem, nenobīdītai atlaidei un nenobīdītajiem ieņēmumu nobīdei. Lai lietotu īstermiņa kontus, **·** **·** **·** **periodiskā līguma norēķinu parametru lapā lauks Īstermiņa nenosildāmā metode ir jāiestata uz Atritināmie periodi vai Fiksētais** gads.
5. Atkārtojiet šīs darbības, lai pievienotu vairāk rindu.
6. Atlasiet **Saglabāt**.

## <a name="use-unbilled-revenue"></a>Izmantot nenodzēsītos ieņēmumus

1. **Lapā Visi norēķinu grafiki** izveidojiet norēķinu grafiku.
2. Ja krājums vēl nav iestatīts ieņēmumu nenopildīšanai, **norēķinu** grafika rindā atzīmējiet izvēles rūtiņu Nenopildāmie ieņēmumi.
3. Iestatiet opciju **Nenoārdāmie** ieņēmumi uz **Jā**. Pēc tam pēc vajadzības pārskatiet un labojiet nenodzēsto ieņēmumu, atlaižu un nenodzēsto ieņēmumu korespondējošos kontus.
4. Norēķinu grafikā, atlasot neapstrādāto **ieņēmumu apstrādi**, atlasiet Izveidot žurnāla ierakstu, **lai** izveidotu sākotnējo žurnāla ierakstu nenosutādētajiem ieņēmumiem. Šis solis ir jāpabeidz pirms norēķinu grafika rēķina izrakstīšanas.
5. Pēc sākotnējā žurnāla ieraksta izveides atlasiet Ģenerēt **rēķinu**, lai izveidotu pārdošanas pasūtījumus un grāmatotu rēķinus rēķinu grafikiem.
6. Kad rēķini ir iegrāmatoti, varat pārskatīt audita informāciju **lapas** Visi norēķinu **grafiki cilnē Atjaunošana**.

### <a name="milestone-billing"></a>Apmaksa pēc atskaites punktiem

Atskaites punkta rēķini darbojas ar nenoslēptiem ieņēmumiem saskaņā ar šādiem nosacījumiem:

- Ja atskaites punkta pamatvienums ir nenobīdāms (**atzīmēta** izvēles rūtiņa Nenobīdāmie ieņēmumi) un par atskaites punkta atvasinātajiem krājumiem tiek izrakstīti rēķini (**izvēles** rūtiņa Nenosūtāmie ieņēmumi ir notīrīta), ir jānorāda pamatvienību sākuma un beigu datumi. Šos datumus izmanto sākotnējā žurnāla ieraksta izveidošanai.
- Ja atskaites punkta pamatelements ir nenobīdāms (**atzīme** izvēles rūtiņa Noņemtie ieņēmumi ir notīrīta) un atskaites punkta apakšelementiem ir izrakstīti rēķini (**ir** atzīmēta izvēles rūtiņa Nenosūtāmie ieņēmumi), beigu datums jānorāda tikai pakārtotajiem krājumiem, kuriem vēlaties izveidot sākotnējo žurnāla ierakstu.

Katru atskaites punkta atvasināto krājumu var apstrādāt atsevišķi. Beigu datumus var norādīt, kad esat gatavs izveidot sākotnējo žurnāla ierakstu.

> [!NOTE]
> Ja sākotnējais žurnāla ieraksts atskaites punkta pamatelementam vai pakārtotajiem krājumiem jau ir izveidots vai ir izveidots rēķins, sākuma un beigu datumus nevar rediģēt.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Nenodzēsti ieņēmumi ar lineāro atlikto maksājumu

Lai lietotu nenorietītos ieņēmumus ar lineārā atlikto maksājumu grafikiem, sekojiet šiem soļiem.

1. **Lapā Visi norēķinu grafiki** izveidojiet norēķinu grafiku.
2. Pievienot elementu norēķinu grafika rindām.
3. Atlasiet **rindas atliktos** maksājumus.
4. Lapā Transakciju **atlikto maksājumu** veiciet šādas darbības:

    1. Iestatiet opciju **Atlikts** uz **Jā**.
    2. Pēc pieprasāmo kontu mainīšana.
    3. Sadaļā Grafiks **atlasiet** Lineārā **un** rediģējiet citas jums nepieciešamas vērtības.
    4. Atlasiet **Labi**.

5. Atlasiet **rindas nenobīdāmos** ieņēmumus un pēc tam veiciet šādas darbības:

    1. Iestatiet opciju **Nenoārdāmie** ieņēmumi uz **Jā**.
    2. Atlasiet kontus, ko izmantot ieņēmumu, atlaižu un ieņēmumu nobīdei.

6. Norēķinu grafika sadaļā Nenodzēsto **ieņēmumu apstrāde atlasiet** Izveidot **žurnāla ierakstu**. Alternatīvi izmantojiet lapu Nenodzēsto **ieņēmumu masveida apstrāde**, lai izveidotu žurnāla ierakstu.
7. Tiek izveidots atlikto maksājumu grafiks. Detalizētu informāciju var skatīt visu atlikto **maksājumu grafiku** lapā. Pēc atlikto maksājumu grafika izveides jūs variet rediģēt dažādas vērtības norēķinu grafika rindas krājumam. Piemēram, var labot vienības cenu, daudzumu vai datumus.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Nenoārdāmie ieņēmumi ar atliktajiem atliktajiem izdevumiem, kas pamatoti uz notikumu

Lai izmantotu nenodzēsītos ieņēmumus ar atlikto maksājumu grafikiem, kas pamatoti uz notikumiem, sekojiet šiem soļiem.

1. **Lapā Visi norēķinu grafiki** izveidojiet norēķinu grafiku.
2. Pievienot elementu norēķinu grafika rindām.
3. Atlasiet **rindas atliktos** maksājumus.
4. Lapā Transakciju **atlikto maksājumu** veiciet šādas darbības:

    1. Iestatiet opciju **Atlikts** uz **Jā**.
    2. Pēc pieprasāmo kontu mainīšana.
    3. Sadaļā Grafiks **atlasiet** Pēc notikuma **, Veidne**, **Sadalījuma** **tips** un Termiņa **beigu konts**.
    4. Atlasiet **Labi**.

5. Atlasiet **rindas nenobīdāmos** ieņēmumus un pēc tam veiciet šādas darbības:

    - Iestatiet opciju **Nenoārdāmie** ieņēmumi uz **Jā**.
    - Atlasiet kontus, ko izmantot ieņēmumu, atlaižu un ieņēmumu nobīdei.

6. Norēķinu grafika sadaļā Nenodzēsto **ieņēmumu apstrāde atlasiet** Izveidot **žurnāla ierakstu**. Alternatīvi izmantojiet lapu Nenodzēsto **ieņēmumu masveida apstrāde**, lai izveidotu žurnāla ierakstu.
7. Tiek izveidots atlikto maksājumu grafiks. Detalizētu informāciju var skatīt visu atlikto **maksājumu grafiku** lapā. Pēc atlikto maksājumu grafika izveides jūs variet rediģēt dažādas vērtības norēķinu grafika rindas krājumam. Piemēram, var labot vienības cenu, daudzumu vai datumus. Atlikto maksājumu grafiks tiek pārrēķināts, ņemot vērā jaunās vērtības.

Sadales tiek pārrēķinātas, pamatojoties uz atlasīto sadalījuma tipu (**procenti**, **pabeigtā daļa** procentos vai Vienādas **summas**). Mainīgo summu **sadalījuma** tipam sadale tiek pārrēķināta, pamatojoties uz sākotnējās vērtības procentu ekvivalentu notikumam. Piemēram, sākotnējā vienības cena ir $100.00, un sākotnējās vērtības procenti tiek aprēķināti $55.00 (55 procenti). Ja vienības cena tiek mainīta $200.00, mainīgā notikuma summa kļūst $110.00 (joprojām 55 procenti).

> [!NOTE]
> Ja atlikto maksājumu grafika rindas ir atpazītas, norēķinu grafika rindas krājumu nevar rediģēt. Lai rediģētu rindas krājumu, vispirms ir jāatgriež atpazītās rindas. Pēc tam norēķinu grafika rindu var atjaunināt.

### <a name="unbilled-revenue-and-top-billing"></a>Nenodzēsti ieņēmumi un augšējais norēķini

Rēķinu izrakstīšanas grafiks tiek ievadīts trīs gadu laikā, un rēķini tiek izrakstīti reizi gadā trīs gadu periodā. Visa līguma summa tiek ierakstīta nenodzēsto ieņēmumu kontā, no kura tiek izveidoti gada rēķini. Korespondējošais konts ir ieņēmumu vai atlikto ieņēmumu konts.

Augšējais norēķins un nenoslietie ieņēmumi nedarbojas vienlaikus, jo saskaņošanas problēmas var rasties virsgrāmatā. Piemēram, krājumu grupas **iestatījuma lapā** krājumu grupa A ir **iestatīta tā, lai augšējo rindu lauka skaits būtu** iestatīts uz **2**. **Norēķinu grafika lapā ir** pievienotas trīs vienības. Visi trīs krājumi pieder krājumu grupai A. Kad sākotnējais žurnāla ieraksts ir izveidots nenos ieņēmumu funkcijai, visu trīs krājumu summa tiek apstrādāta uz nenostrādāto kontu. Kad tiek izveidots rēķins rēķinu grafikam, tiek iekļautas tikai divu augšējo krājumu summas. Tāpēc rēķina summa nesaskan ar summu, kas tika apstrādāta ar nenovienoto ieņēmumu kontu, un saskaņošanas problēmas rodas Virsgrāmatā.

Ja vēlaties izmantot nenopildītos ieņēmumus, **atstājiet** krājumu grupas iestatījuma lapu tukšu vai iestatiet visas krājumu grupas tā, **lai** augšējo rindu skaits **būtu iestatīts uz 0** (nulli). Ja vēlaties izmantot augšējos norēķinus, nav pieejamas nesavienotās ieņēmumu darbības.

### <a name="examples"></a>Piemēri

Attiecībā uz versiju 10.0.29 periodiskiem līguma rēķinu parametriem tiek pievienots jauns parametrs. Ja iestatījums ir Jā, parametrs **Izmantot nenobīdītus** korespondējošos kontus **aktivizē divus jaunus kontus iestatījumā Nenobīdītie ieņēmumi**. Nenosūtāmo ieņēmumu korespondējošie un nenosūtāmie atlaižu korespondējošie konti kļūst pieejami, un tos vislabāk izmanto, veidojot rēķinu grafikus valūtā, kas nav uzskaites valūta. Izmantojot korespondējošos kontus, tiek nodrošināts, ka nenobīdītie ieņēmumi un nenobīdītās atlaides konti tiek apgriezti, izmantojot tos pašus maiņas kursus, ar kuriem tiek atsaukti to sākotnējie ieraksti. Sākotnējais žurnāla ieraksta **izveides process ir tāds** pats kā neapstrādāto ieņēmumu debets un ieņēmumu kreditēšana. Ja izmantojat atlaidi, sākotnējais žurnāla ieraksts ir tāds pats kā atlaides debets un kredīts, lai nenodzītu atlaidi. 

Šajā piemērā parādīts, kā izmantot nenosummotos ieņēmumus, lai bilancē atpazītu visu līguma summu kā nenozīmotus ieņēmumus. Ieraksta otra puse ir ieņēmumi vai atliktie ieņēmumi. Kad jūs klientam izrakstiet rēķinu, nenostādāmie ieņēmumi tiek atgriezti. Ieņēmumu atzīšana notiks rēķina izrakstīšanas laikā vai saskaņā ar iestatīto atliktā maksājuma atzīšanas grafiku.

#### <a name="assumptions"></a>Pieņēmumi

- Šā gada 1. janvārī debitors paraksta trīs gadu līgumu par $390.
- Līgumā ir divas daļas: licences un uzturēšanas līgums.
- Licences maksas pārdošanas cena ir grāmatota $300, un debitoram tiks izrakstīts rēķins $100 katra līguma gada 1. janvārī. Licences $300 tiks ņemta kā ieņēmumi, kad līgums ir parakstīts.
- Uzturēšanas maksas pārdošanas cena ir standarta $90 un debitoram tiks izrakstīti rēķini $30 katra līguma gada 1. janvārī. Apkopes $90 maksa tiks atlikta, un $2.50 tiks atpazīts katru līguma dzīves mēnesi.
- Rēķins debitoram tiks $130 katra trīs līguma gadu sākumā (1. janvārī).

#### <a name="steps"></a>Darbības

1. Iestatiet divus izlaistos krājumus kā nenopildāmus krājumus. Izmantojiet lapu **Nenopildāmo ieņēmumu** iestatījums, lai iestatītu krājumus un kontus, kas izmanto nenopildāmos ieņēmumus.
2. Šajā piemērā uzturēšanas maksa tiek atlikta. Krājumam ir nepieciešama atlikto maksājumu veidne, kas ir iestatīta atlikto **maksājumu veidņu** lapā. Veidnei ir mēneša **perioda** biežums un atpazīšanas perioda ilgums ir 36 mēneši. Tādēļ ieņēmumi mēnesī ir $2.50.
3. Lapā Atliktie **krājumi pēc noklusējuma** iestatiet lauku Uzturēšanas **maksa** uz Atlikto **maksājumu krājumu**. Šis solis un nākamais iemesls būs uzturēšanas maksas krājums tiek atlikts, kad tas tiek pārdots vai iekļauts norēķinu grafikā.
4. Atlasiet **atlikto maksājumu noklusējuma** \> **veidni** un no 2. soļa pievienojiet krājumu uzturēšanas maksai un lineārā veidnei. Uzturēšanas maksas krājums tiks saistīts ar 36 mēnešu atlikto maksājumu grafiku.
5. Izveidojiet norēķinu grafiku, kas ietver divas nenosācītas vienības. Rēķina grafiks līgumam ir iestatīts ar šādiem krājumiem.

    | Krājums | Sākuma datums | Beigu datums | Apjoms | Norēķinu biežums | Atlikto maksājumu krājums | Rēķinos neiekļautie ieņēmumi | Apraksts |
    |---|---|---|---|---|---|---|---|
    | Licence | 2022. gada 01. janvāris | 2024. gada 31. decembris | $100.00 | Reizi gadā | Nē | Jā | Debitoram katru gadu tiks izrakstīts $100.00 rēķins. Kopsumma $300.00 iepriekš tiks reģistrēta kā nenobīdāmie ieņēmumi bilancē un kā peļņas un zaudējumu ieņēmumi. Katrs rēķins samazina nenosaisāmo summu. |
    | Uzturēšana | 2022. gada 01. janvāris | 2024. gada 31. decembris | $30.00 | Reizi gadā | Jā | Jā | Debitoram katru gadu $30.00 rēķins. Kopsumma $90.00 iepriekš tiks reģistrēta kā nenobīdāmie ieņēmumi un atliktie ieņēmumi bilancē. Katrs rēķins samazina nenosaisāmo summu. Atliktie ieņēmumi tiks atpazīti ik mēnesi 36 mēnešu laikā. |

6. Lapā Visi **norēķinu grafiki** izmantojiet procesu Izveidot žurnāla ievadni, **lai** grāmatotu līguma vērtību bilancē kā nenozīmotus ieņēmumus.

Tiek izveidoti divi žurnāla ieraksti– viens katrai norēķinu grafika rindai.

| Konts | Debeta summa | Kredīta summa |
|---|---|---|
| Rēķinos neiekļauto ieņēmumu konts | $300.00 | |
| Ieņēmumu konts | | $300.00 |

| Konts | Debeta summa | Kredīta summa |
|---|---|---|
| Rēķinos neiekļauto ieņēmumu konts | $90.00 | |
| Atliktie ieņēmumi | | $90.00 |

Līgumam ir nepieciešams, lai katra gada sākumā tiktu izveidots debitora rēķins. Izmantojiet Rēķinu **izveides procesu**, lai izveidotu rēķinu. Kad rēķins ir izveidots, tiek grāmatots šāds rēķina dokuments.

| Konts| Debeta summa | Kredīta summa |
|---|---|---|
| Rēķinos neiekļauto ieņēmumu konts | | $130.00 |
| Debitori | $130.00 | |

Šo pašu žurnāla ierakstu izveidos rēķini, kas grāmatoti nākamo divu gadu sākumā. Nenodzēsto ieņēmumu konts katru gadu tiek samazināts rēķina **ģenerēšanas procesa** laikā. Nenobīdīto ieņēmumu korespondējošais konts tiek izmantots, lai līdzsvarotu nenodzēsto ieņēmumu kontu, ja tiek lietoti dažādi maiņas kursi. 

Pēdējā solī atpazīšanas žurnāla ieraksts tiek izveidots katru mēnesi, lai atpazītu atliktos ieņēmumus no uzturēšanas maksas. Žurnāla ierakstu var izveidot, izmantojot lapu **Atpazīšanas** apstrāde. Alternatīvi to var izveidot, atlasot **Atpazīt** atlikto maksājumu **grafika lapu rindām**.

| Galvenais konts | Debeta summa | Kredīta summa |
|---|---|---|
| Atliktie ieņēmumi | $2.50 | |
| Ieņēmumi | | $2.50 |

Šis žurnāla ieraksts tiks izveidots katru reizi, kad šim atliktam krājumam tiek palaists atpazīšanas process (kopā 36 reizes).

#### <a name="short-term-fixed-year"></a>Īstermiņa: fiksēts gads

Jūs varat izmantot nenokārtoto ieņēmumu **kopā** **ar īstermiņa funkcionalitāti, iestatot īstermiņa nenokārtoto lauku periodiskā līguma norēķinu parametru** lapā. Šajā piemērā parādīti aprēķini, kas tiek veikti, ja lietojat nenorietotos ieņēmumus kopā **ar** fiksētā gada īstermiņa nenosāktās metodes.

Tiek izveidots norēķinu grafiks, kas atbilst šādiem kritērijiem:

- **Sākuma datums:** 2020. gada 1. jūnijs
- **Beigu datums:** 2021. gada 31. decembris
- **Vienības cena:** $100
- **Biežums: mēneša**

**Lapā Visi norēķinu grafiki** sākotnējā žurnāla ieraksts tiek izveidots ar procesu **Izveidot žurnāla** ierakstu. Pašreizējās īstermiņa un ilgtermiņa summas tiek aprēķinātas šādi:

- **Pašreizējā īstermiņa nenorieto ieņēmumu summa:** $700
- **Pašreizējā ilgtermiņa nenoslēgto ieņēmumu summa:** $1,200

Rēķins ir izveidots norēķinu periodam no 2020. gada 1. jūnija līdz 2020. gada 30. novembrim. Pašreizējās īstermiņa un ilgtermiņa summas tiek aprēķinātas šādi:

- **Pašreizējā īstermiņa nenoslēdzto ieņēmumu summa:** $100
- **Pašreizējā ilgtermiņa nenoslēgto ieņēmumu summa:** $1,200

Rēķins ir izveidots norēķinu periodam no 2020. gada 1. decembra līdz 2020. gada 31. decembrim. Pašreizējās īstermiņa un ilgtermiņa summas tiek aprēķinātas šādi:

- **Pašreizējā īstermiņa nenosācīto ieņēmumu summa:** $1,200
- **Pašreizējā ilgtermiņa nenoslēgto ieņēmumu summa:** $0

#### <a name="short-term-rolling-periods"></a>Īstermiņa: notiek periodu atrite.

Jūs variet izmantot nenokārtoto **ieņēmumu kopā ar īstermiņa funkcionalitāti, iestatot īstermiņa nenokārtoto metodi periodiskā līguma norēķinu parametru** lapā. Šajā piemērā parādīti **aprēķini**, kas tiek veikti, ja kopā ar īstermiņa nenoildošo metodi tiek izmantoti nenosildoši ieņēmumi.

Tiek izveidots norēķinu grafiks, kas atbilst šādiem kritērijiem:

- **Sākuma datums:** 2020. gada 1. jūnijs
- **Beigu datums:** 2021. gada 31. decembris
- **Vienības cena:** $100
- **Biežums: mēneša**

**Lapā Visi norēķinu grafiki** sākotnējā žurnāla ieraksts tiek izveidots ar procesu **Izveidot žurnāla** ierakstu. Pašreizējās īstermiņa un ilgtermiņa summas tiek aprēķinātas šādi:

- **Pašreizējā īstermiņa nenosācīto ieņēmumu summa:** $1,200
- **Pašreizējā ilgtermiņa nenoslēgto ieņēmumu summa:** $700

Rēķins ir izveidots norēķinu periodam no 2020. gada 1. jūnija līdz 2020. gada 30. novembrim. Pašreizējās īstermiņa un ilgtermiņa summas tiek aprēķinātas šādi:

- **Pašreizējā īstermiņa nenosācīto ieņēmumu summa:** $1,200
- **Pašreizējā ilgtermiņa nenoslēgto ieņēmumu summa:** $100

Rēķins ir izveidots norēķinu periodam no 2020. gada 1. decembra līdz 2020. gada 31. decembrim. Pašreizējās īstermiņa un ilgtermiņa summas tiek aprēķinātas šādi:

- **Pašreizējā īstermiņa nenosācīto ieņēmumu summa:** $1,200
- **Pašreizējā ilgtermiņa nenoslēgto ieņēmumu summa:** $0

### <a name="items-with-revenue-allocation"></a>Krājumi ar ieņēmumu sadalījumu

Divas vienības ar dažādu norēķinu biežumu tiek pievienotas norēķinu grafikam. Gan izmanto nenodzēsītos ieņēmumus, gan atliktos krājumus.

- **Krājuma numurs 1000:** Surface Pro 128GB

    - **Norēķinu biežums:** vienreizējs
    - **Vienības cena:** $1,500
    - **Savrupa pārdošanas cena:** $1,600
    - **Līguma ieņēmumi:** $1,465.26

- **Krājuma kods S0021: apdrošināšana**, kas tiek pārdota kopā ar krājuma kodu 1000

    - **Norēķinu biežums:** mēneša 12 mēneši
    - **Vienības cena:** $20 skaits mēnesī
    - **Savrupa pārdošanas cena:** $25
    - **Līguma ieņēmumi:** $264.74

Tā kā abi krājumi izmanto nenos ieņēmumu un ieņēmumu sadalījumu, kopējā līguma summa atjaunošanas rindā ir 0 (nulle). Tiek **pievienota kolonna** Līguma ieņēmumi un parādīta līguma ieņēmumu summa.

Tabulā ir parādīts krājumu un rēķina sākotnējais žurnāla ieraksts.

| Galvenais konts | Debeta summa | Kredīta summa |
|---|---|---|
| **Krājuma 1000 žurnāla ieraksts** | | | 
| Nenodzēsto ieņēmumu konts (401250) | $1,465.26 | |
| Atlikto ieņēmumu konts (250 600) | | $1,465.26 |
| **Krājuma 0021 žurnāla ieraksts** | | | 
| Nenodzēsto ieņēmumu konts (401250) | $274.74 | |
| Atlikto ieņēmumu konts (250 600) | | $274.74 |
| **Rēķins** | | |
| Rēķinos neiekļauto ieņēmumu konts | | $1,465.26 |
| Rēķinos neiekļauto ieņēmumu konts | | $274.74 |
| Dev. konts (130 100) | $1,488.16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Izmaiņas norēķinu grafika rindā, norēķinu detalizētas informācijas rindā vai ieņēmumu sadalījumā

Ja vienības cena vai daudzums tiek mainīts, jāatjaunina līguma ieņēmumu summa katram krājumam, kas ir daļa no ieņēmumu sadalījuma. Tādēļ žurnāla ieraksts tiek pārrēķināts.

Piemēram, krājuma 1000 vienības cena tiek mainīta no $1,500 uz $1,600. Šajā gadījumā līguma ieņēmumu summa tiek automātiski pārrēķināta kā $1,549.47. Krājuma S0021 līguma ieņēmumi tiek pārrēķināti kā $290.53.

Kad izmaiņas tiek apstiprinātas un fiksētas, tiek atcelti abu krājumu sākotnējie žurnāla ieraksti un tiek izveidoti jauni žurnāla ieraksti:

- **Vienība 1000:** ieraksta sākotnējais $1,465.26 ieraksts ir atcelts. Žurnālam ir izveidots $1,549.47 ieraksts.
- **Krājums S0021:** ieraksta sākotnējais $274.74 ieraksts ir atcelts. Žurnālam ir izveidots $290.53 ieraksts.

#### <a name="termination"></a>Izbeigšana

Krājuma S0021 sākuma datums ir 2020. gada janvāris, un tā beigu datums ir 2020. gada decembris, bet ar to pārtraukta 2020. gada jūnijā. Abu krājumu līguma ieņēmumu summa ir jāpārrēķina:

- **Krājums 1000:** līguma ieņēmumi tiek pārrēķināti kā $1,567.67.
- **Krājums S0021:** līguma ieņēmumi tiek pārrēķināti kā $124.00.

Tiek izveidots korekciju žurnāla ieraksts rindā, ar kuru pārtrauktas darba attiecības. Ir atsaukts žurnāla ieraksts rindai, kas pieder tam pašam vairāku elementu izkārtojumā (MEA) numuram, un tiek izveidots jauns žurnāla ieraksts:

- **Vienība 1000:** ieraksta sākotnējais $1,465.26 ieraksts ir atcelts. Ir izveidots korekciju $1,549.47 ieraksts.
- **Krājums S0021:** ieraksta sākotnējais $274.74 ieraksts ir atcelts. Žurnālam ir izveidots $124.00 ieraksts.
