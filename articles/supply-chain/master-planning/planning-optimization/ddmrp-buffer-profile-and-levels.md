---
title: Bufera profils un līmeņi
description: Šajā rakstā ir sniegta informācija par bufera profiliem un līmeņiem, kas nosaka minimālos un maksimālos krājumu līmeņus, kas ir jāsaglabā katrā dekompozīcijas vietā.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 57ee6206da926d0dbf62f562197538bfcdd41148
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428149"
---
# <a name="buffer-profile-and-levels"></a>Bufera profils un līmeņi

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Kad esat identificējuši atšifrēšanas punktus (atslēgas, ko stratēģiski glabāsiet noliktavā), ir jāizlemj, cik daudz krājumu (bufera) jūs paturēsiet pie katra no tiem. Šis uzdevums ir pieprasījumam noteiktu materiālu resursu plānošanas (DDMRP) otrais solis.

## <a name="buffer-levels-and-zones"></a>Bufera līmeņi un zonas

Katrā DDMRP krājumu buferī tiek definētas trīs vērtības: minimālais daudzums, maksimālais daudzums un atkārtota pasūtījuma punkts. Šīs vērtības izveido trīs atšķirību zonas, kas tiek identificētas ar šādiem krāsu kodiem:

- **sarkanā zona** – apgabals, kas ir zem minimālā daudzuma; Minimālais daudzums tiek saukts arī par "sarkanās krāsas augšpusi", un plānošanas stratēģijai jābūt veidotai, lai nodrošinātu, ka krājumu līmeņi vienmēr atrodas augstāk par šo punktu.
- **Dzeltena zona** – zona starp minimālo daudzumu un atkārtota pasūtījuma punktu. Atkārtota pasūtījuma punkts arī tiek saukts par "dzeltenas krāsas virspusi". Kad šis punkts ir sasniegts, sistēmai ir jāveic atkārtota pasūtījumu secība.
- **Zaļa zona** – apgabals starp atkārtota pasūtījuma punktu un maksimālo daudzumu. Maksimālais daudzums tiek saukts arī par "zaļās lapas augšpusi". Šis ir maksimālais līmenis, līdz kam krājums tiks papildināts.

Šajā attēlā redzamas trīs krāsainās zonas un veids, kā tās attiecas uz minimālo daudzumu, maksimālo daudzumu un pārkārtot punktu.

![DDMRP bufera zonas un līmeņi.](media/ddmrp-buffer-levels.png "DDMRP bufera zonas un līmeņi")

## <a name="calculating-the-buffer-zones"></a>Buferjoslu aprēķināšana

Šajā sadaļā skaidrots, kā tiek aprēķināts katras bufera zonas augstums.

Dzeltena zona parasti tiek aprēķināta vispirms. Šī zona ir daudzums, ko patērēt no brīža, kad pasūtījums tiek saņemts, līdz pasūtījums tiek saņemts. Citiem vārdiem sakot, tas ir paredzamais patēriņš papildināšanas izpildes laikā. Tas tiek aprēķināts, izmantojot šādu vienādojumu:

- **Dzeltenas** = *zonas vidējā dienas lietojums (ADU)* × atšifrēšanas *izpildes laiks*

Dekompozīcijas *izpildes laiks* norāda laiku, kas nepieciešams krājuma ražošanai vai saņemšanai, ja dekompozīcijas punkti vienmēr ir noliktavā. Parasti tas ir daudz īsāks par kopējo izpildes *laiku,* kas parasti tiek izmantots vispārējā plānošanā. Pareizi bufera iestatījumi ir atslēga, lai nodrošinātu, ka dekompilēšanas punkti vienmēr atrodas rezervē, bet netiek pārsniegti.

Sarkanā zona tiek aprēķināta, izmantojot šādus vienādojumus:

- **Sarkanās krāsas** = *ADU* × dekompozīcijas *izpildes laiks* × *izpildes laika koeficients*
- **Sarkanās drošības** = *sarkanās krāsas* × *novirzes koeficients*
- **Sarkanās zonas** = *sarkanās krāsas drošības* + *pamats*

Zaļā zona tiek aprēķināta kā šādu trīs vienādojumu maksimālais rezultāts:

- *Minimālais pasūtījumu daudzums*
- *ADU* × *pasūtījuma cikls*
- *ADU* × dekompozīcijas *izpildes laiks* × *izpildes laika koeficients*

## <a name="calculating-average-daily-usage"></a>Vidējās ikdienas lietošanas aprēķināšana

Sistēma izmanto vienu no trim pieejām, lai aprēķinātu summu, ko patērēt dienā:

- **Vidējā ikdienas lietošana (iepriekš)** – šī pieeja ir balstīta uz faktisko pagātnes patēriņu.
- **Vidējā ikdienas izmantošana (uz priekšu)** – šī pieeja ir balstīta uz prognozēto nākotnes patēriņu.
- **Vidējā ikdienas lietošana (jaukta)** – šī pieeja ir balstīta uz svērtu pagātnes un prognozētā patēriņa sajaukums.

### <a name="average-daily-usage-past"></a>Vidējais dienas lietojums (iepriekš)

Pagātnes ADU tiek aprēķināta kā vidējais, pievienojot daudzumus, kas ir izmantoti katru dienu noteiktam pagājušo dienu skaitam un pēc tam dalot kopsummu ar dienu skaitu. Šajā attēlā parādīts, kā šī pieeja darbojas, kad aprēķins izskatās trīs dienas iepriekš.

![Vidējā ikdienas lietošanas (iepriekšējā) diagramma.](media/ddmrp-adu-past.png "Vidējā ikdienas lietošanas (iepriekšējā) diagramma")

Iepriekšējā ilustrācijā, ja šodien ir no 11. jūnija no rīta, ADU iepriekšējām trim dienām (8. jūnijs, 9. un 10. jūnijs) ir 21.

- **ADU (pagātne)** = (29 + 11 + 23) ÷ 3 = 21

Lai aprēķinātu vidējo dienas izmantojumu (iepriekš), tiek ņemtas vērā šādas darbības:

- Transakcijas, kurās krājuma daudzums ir mazāks par nulli (`inventtrans` tabulā)
- Darbības ar statusu Pasūtīts, Rezervēts *pasūtījums* *·*, Rezervēts *fiziski*, *Izdots*, Ieturēts *vai* Pārdots *·*
- Darbības, kas datētas ar izvēlēto atpakaļešo periodu (vidējais dienas lietošanas pagātnes periods)
- Darbības, kas nav noliktavas darbs, karantīna, pārdošanas piedāvājumi vai pārskati (`WHSWork`, `WHSQuarantine``SalesQuotation` vai )`Statement`
- Darbības, kas nav pārsūtīšanas žurnāli, kas ietilpst tajā pašā vajadzību dimensijā

### <a name="average-daily-usage-forward"></a>Vidējā ikdienas izmantošana (uz priekšu)

Jaunai precei, iespējams, jums nav pagātnes lietošanas datu. Tāpēc tā vietā varat izmantot prognozēto ADU virzību uz priekšu (piemēram, pamatojoties uz prognozēto pieprasījumu). Šajā attēlā parādīts, kā šī pieeja darbojas, kad aprēķins izskatās trīs dienas nākotnē (tostarp šodien).

![Vidējā ikdienas lietošanas (uz priekšu) diagramma.](media/ddmrp-adu-forward.png "Vidējā ikdienas lietošanas (uz priekšu) diagramma")

Iepriekšējā ilustrācijā, ja šodien ir no 11. jūnija no rīta, ADU nākamajām trim dienām (11. jūnijs, 12. un 13. jūnijs) ir 21,66.

- **ADU (uz priekšu)** = (18 + 18 + 29) ÷ 3 = 21,66

Lai aprēķinātu vidējo dienas izmantojumu (uz priekšu), tiek ņemtas vērā šādas darbības:

- Budžeta darbības krājumam, kura budžets ir atlasīts vispārējā plānā
- Darbības, kas datētas ar izvēlēto turpmāko periodu (vidējais dienas lietojuma uz priekšu periods)

### <a name="average-daily-usage-blended"></a>Vidējā dienas lietošana (jaukta)

Jauktā ADU apvieno vidējo pagātnes lietojumu un vidējo nākotnes izmantojumu, kā parādīts šajā ilustrācijā.

![Vidējā ikdienas lietošanas (jauktā) diagramma.](media/ddmrp-adu-blended.png "Vidējā ikdienas lietošanas (jauktā) diagramma")

Iepriekšējā ilustrācijā, ja šodien ir no 11. jūnija no rīta, jauktais ADU iepriekšējām un nākamajām trim dienām (no 8. līdz 13. jūnijam) ir 21,33.

- **ADU jauktais** = (*ADU aiz* + *ADU uz priekšu*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Bufera aprēķina koeficienti

Katram krājumam var definēt divus faktorus, lai koriģētu, cik lielām vajadzētu būt sarkanām un zaļām zonām. Šādā veidā varat kompensēt paredzamo izpildes laiku un pieprasījuma noviržu.

![Izpildes laika un novirzes koeficienti.](media/ddmrp-zone-factors.png "Izpildes laika un novirzes koeficienti")

Pirmais faktors ir izpildes *laika koeficients*. Vērtība ir decimālskaitļa vērtība no 0 līdz 1. Jo garāks ir izpildes laiks, jo mazākai ir jābūt vērtībai. Uz pieprasījumu balstītais institūts iesaka šādus diapazonus:

- **Ilgs izpildes laiks:** 0.20–0.40
- **Vidējais izpildes laiks:** 0.41–0.60
- **Īss izpildes laiks:** 0.61–1.00

Otrais koeficients ir novirzes *koeficients*. Vērtība ir decimālskaitļa vērtība no 0 līdz 1. Jo augstāka ir pieprasījuma novirze, jo mazākai ir jābūt vērtībai. Uz pieprasījumu balstītais institūts iesaka šādus diapazonus:

- **Zema novirze:** 0.20–0.40
- **Vidēja novirze:** 0.41–0.60
- **Augsta novirze:** 0.61–1.00

## <a name="buffer-calculation-examples"></a>Bufera aprēķina piemēri

Šis piemērs turpinās ar ražošanas piemēru, kas sniegts Krājumu [pozicionē.](ddmrp-inventory-positioning.md) Šajā piemērā atlasījāt atšifrēšanas punktus, kas samazina izpildes laiku no 21 dienas līdz piecām dienām, kā parādīts šajā ilustrācijā.

![Dekompozīcijas izpildes laika piemērs.](media/ddmrp-bom-decoupled-lead-time-example.png "Dekompozīcijas izpildes laika piemērs")

Šajā piemērā pieņemsim, ka ADU ir aprēķināts kā 23 gabali un, kā redzams iepriekšējā ilustrācijā, dekompozīcijas izpildes laiks ir piecas dienas. Izmantojot šīs vērtības, var aprēķināt dzelteno zonu, izmantojot šādu vienādojumu:

- **Dzeltenas zonas** = *ADU* × *dekompozīcijas izpildes laiks* = 115

![Dzeltenas zonas aprēķina piemērs.](media/ddmrp-example-calc-yellow.png "Dzeltenas zonas aprēķina piemērs")

Sarkanās zonas aprēķins ir līdzīgs dzeltenas zonas aprēķinam, bet tas ir noklusēts par novirzāmību un izpildes laiku. Šajā piemērā pieņemsim, ka esat ievērojis vidēju izpildes laiku (faktors = 0,50) un augstu pieprasījuma noviržu (koeficients = 0,8). Izmantojot šīs vērtības kopā ar komponentiem no dzeltenas zonas vienādojuma, varat aprēķināt sarkanu zonu, izmantojot šādus vienādojumus:

- **Sarkanās krāsas ADU** = *×* dekompozīcijas *izpildes laiks ×* izpildes laika koeficients *=* 57,5
- **Sarkanās drošības** = *sarkanās krāsas* × *novirzes faktors* = 46
- **Sarkanā zona** = *Sarkanā drošība* + *·* = 103,5

Sistēma noapaļos sarkanu zonu līdz 104 gabaliem (maks.), jo gabali tiek skaitīti veselos skaitļos.

![Sarkanās zonas aprēķina piemērs.](media/ddmrp-example-calc-red.png "Sarkanās zonas aprēķina piemērs")

Zaļās zonas aprēķins ietver arī komponentus no dzeltenas zonas vienādojuma, bet tas ļauj minimāli pasūtījuma lielumu, pasūtījuma ciklu un izpildes laika koeficientu. Šajā piemērā pieņemiet, ka nav pasūtījuma cikla (tādēļ jums nav laika ierobežojumu par to, cik bieži pasūtījums tiek pasūtīts) un minimālais pasūtījuma daudzums ir 10 gabali. Tad zaļā zona tiek aprēķināta kā šādu trīs vienādojumu maksimālais rezultāts:

- *Minimālais pasūtījumu daudzums* = 10
- *ADU* × *pasūtījuma cikls* = 0
- *ADU* × dekompozīcijas *izpildes* laiks × *izpildes laika koeficients* = 57,5

Sistēma noapaļos zaļu zonu līdz 58 gabaliem (maks.), jo gabali tiek skaitīti veselos skaitļos.

![Sarkanā zaļā aprēķina piemērs.](media/ddmrp-example-calc-green.png "Zaļās zonas aprēķina piemērs")

Šajā attēlā ir apkopoti šo zonu aprēķina rezultāti, izmantojot DDMRP bieži lietoto DDMRP grafiku.

![Zonas aprēķina rezultātu kopsavilkums](media/ddmrp-example-calc-summary.png "Zonas aprēķina rezultātu kopsavilkums")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a> Dinamiskās korekcijas

Dinamiskie pielāgojumi ļauj lietot pieprasījuma *korekcijas koeficientus* augstas vai zema pieprasījuma periodu laikā. Šis koeficients reizina ADU visos aprēķinos atlasītajam periodam. Pēc tam bufer zonas tiek modificētas savukārt. Šo faktoru parasti izmantosiet pēc sākotnējo bufera vērtību ģenerēšanas, lai varētu tās precīzi noregulēt laika gaitā un kā atbildi uz nosacījumu maiņu. Šis uzdevums ir DDMRP trešais solis.

Piemēram, var prasīt lielāku neprodukta pieprasījumu augustā, kad cilvēki atrodas atvaļinājumā. Tāpēc ir paredzams, ka pārdošana būs augstāka. Šajā gadījumā varat mainīt preces pieprasījuma **korekcijas koeficienta** vērtību uz *1,5* visām augusta nedēļām.

Šādā veidā bufera vērtības var aprēķināt laika gaitā un pēc tam tās pielāgot, pamatojoties uz vairāk nekā tikai sistēmas informāciju. Veicot pilnu DDMRP ieviešanu, jūs aprēķināsiet jaunas bufera vērtības katru dienu, izmantojot pakešuzdevumu, un automātiski akceptēsiet vērtības. Pēc tam jūs izpildīsiet plānošanu kā pakešuzdevumu un pārskatīsiet plānotos pasūtījumus katru dienu, lai piepildītu buferus.

## <a name="implement-buffers-in-supply-chain-management"></a>Implementē buferus piegādes ķēžu pārvaldībā

Šajā sadaļā ir aprakstīts, kā ieviest bufera zonas stratēģiju sistēmā Microsoft Dynamics 365 Supply Chain Management. Tiek pieņemts, ka jau esat izdarījis analīzi un aprēķinus, kas ieskicē šī raksta pirmajā pusē.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a> Buferu iestatīšana dekomupēšanas punkta vienumam

Izpildiet šīs darbības, lai iestatītu bufera vērtības atšifrēšanas punktam.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet izlaisto krājumu, kas ir iestatīts kā atšifrēšanas punkts. (Plašāku informāciju skatiet [Krājumu pozicionēšana](ddmrp-inventory-positioning.md).)
1. Darbību rūts cilnē Plāns **atlasiet** Krājumu **vajadzība**.
1. Krājumu vajadzības **lapā atlasiet** krājuma nodrošinājuma ierakstu, kas izveido atšifrēšanas punktu. (Šajā ierakstā tiks rādīts tās vajadzības grupas nosaukums, kura ir iestatīta dekompilēšanas punktu izveidojiet.)
1. Atlasiet cilni **Vispārēji**.
1. Ja vēlaties, lai sistēma pārrēķinātu bufera vērtības katru dienu vai katru nedēļu, pamatojoties uz pārdošanas vēsturi, prognozēm un vajadzības grupas iestatījumiem, rīkojieties šādi:

    1. Opciju **Bufera vērtības laika gaitā** iestatiet uz *Jā*.
    1. Ziņojuma lodziņš ziņo, ka manuālos bufera iestatījumus (**Minimums**, **Atkārtota pasūtījuma punkts** **un** Maksimums) tiks atiestatīti, ja turpināsiet. Atlasiet **Jā,** lai saglabātu jauno iestatījumu.

    Ja vēlaties aprēķināt vai ievadīt bufera iestatījumus tikai vienu reizi, veiciet šādas darbības:

    1. Opciju **Bufera vērtības laika gaitā** iestatīt uz *Nē*.
    1. Iestatiet laukus **Minimums**,**·** **Pārkārtot** punktu un Maksimums uz bufera vērtībām, kuras esat aprēķinājis krājumam, kā aprakstīts iepriekš šajā rakstā.

1. Iestatiet sekojošos laukus, lai pabeigtu DDMRP aprēķinu iestatīšanu krājumam:

    - **Pasūtījuma cikls** – norādiet dienu skaitu, kas ir jāpaiet starp krājuma pirkšanas pasūtījumiem. Iestatiet vērtību uz *0 (nulle*), ja pasūtījuma ierobežojumi nepastāv. Šis lauks ietekmē maksimālo daudzuma buferi, kā iepriekš aprakstīts šajā rakstā.
    - **Vidējā ikdienas lietošana** – pēc izvēles varat ievadīt krājumam aprēķināto ADU. Šis lauks ir paredzēts tikai informatīviem nolūkiem. Parasti vērtība tiek automātiski aprēķināta kā daļa no bufera aprēķiniem.
    - **Pasūtījuma sakrāšanas** slieksnis – norāda krājuma ikdienas pārdošanas minimālo skaitu, kas kvalificējas kā pārdošanas vārda (diezgan liels pieprasījums). Sistēma lieto šo lauku, lai palielinātu plānoto pasūtījumu atkārtoto pasūtījumu daudzumu augsta pieprasījuma periodos. Papildinformāciju skatiet sadaļā Uz [pieprasījumu balstīta plānošana](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a> Aprēķināt vai ievadīt dekompozīcijas izpildes laikus

Krājumiem, kur izvēlaties [atļaut](#set-up-buffers) sistēmai automātiski aprēķināt bufera zonas, veiciet šīs darbības, lai aprēķinātu vai ievadītu atšifrēšanas izpildes laikus atšifrēšanas punkta krājumam.

1. Atveriet lapu **Krājumu** segums šim dekompozīcijas punkta elementam. (Plašāku informāciju skatiet [Iestatīt buferus dekompilēšanas punkta krājumam](#set-up-buffers).)
1. Atlasiet krājumu vajadzību ierakstu, kas izveido dekompozīcijas punktu.
1. Atlasiet cilni **Bufera** vērtības.
1. Ja režģī netiek rādīti laika periodi, darbību rūtī cilnē Bufera **vērtības** atlasiet Pievienot laika **periodus**. Sistēma aizpilda režģi ar rindām katram ikdienas vai nedēļas laika periodam atkarībā no tā, vai lauks Min, **max un re-order point**[periods](ddmrp-inventory-positioning.md) vajadzību grupai ir iestatīts uz *Ikdienas* *vai Iknedēļas.* Sistēma pievienos pietiekamu rindu, lai sasniegtu krājumam piešķirtajām vajadzības grupām norādīto laika periodu.
1. Atlasiet laika periodu, kurā jāaprēķina dekompozīcijas izpildes laiks. (Parasti šis laika periods ir periods, kas ietver šodienas datumu.)
1. Darbību rūts cilnē Bufera **vērtības** atlasiet Aprēķināt atšifrēto **izpildes laiku**.
1. Dialoglodziņā Aprēķināt **dekompozīcijas izpildes** laiku iestatiet šādus laukus:

    - **MK** – atlasiet materiālu komplektu (MK), kuram vēlaties veikt aprēķinu.
    - **Datums** – atlasiet datumu, kurā vēlaties veikt aprēķinu. Pieejamo MK kopa tiks filtrēta, lai tiktu parādīti tikai mk, kas ir aktīvi atlasītajam datumam.
    - **Daudzums** - ievadiet daudzumu, kam vēlaties veikt aprēķinu. Pieejamo MK kopa tiks filtrēta, lai tiktu parādīti tikai tie MK, kas attiecas uz norādīto daudzumu.

1. Atlasiet **Labi**, lai palaistu aprēķinu, un aizveriet **dialoglodziņu Aprēķināt dekompozīcijas** izpildes laiku. Atšifrēta **izpildes laika kolonna** atlasītajam laika periodam tagad rāda aprēķināto vērtību.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a> Aprēķināt vai ievadīt vidējo dienas lietojumu

Krājumiem, kur izvēlaties [atļaut](#set-up-buffers) sistēmai automātiski aprēķināt buferjoslas, veiciet šīs darbības, lai aprēķinātu vai ievadītu DEkompozīcijas punkta krājuma ADU.

1. Atveriet lapu **Krājumu** segums šim dekompozīcijas punkta elementam. (Plašāku informāciju skatiet [Iestatīt buferus dekompilēšanas punkta krājumam](#set-up-buffers).)
1. Atlasiet krājumu vajadzību ierakstu, kas izveido dekompozīcijas punktu.
1. Atlasiet cilni **Bufera** vērtības.
1. Ja režģī netiek rādīti laika periodi, darbību rūtī cilnē Bufera **vērtības** atlasiet Pievienot laika **periodus**. Sistēma aizpilda režģi ar rindām katram ikdienas vai nedēļas laika periodam atkarībā no tā, vai lauks Min, **max un re-order point**[periods](ddmrp-inventory-positioning.md) vajadzību grupai ir iestatīts uz *Ikdienas* *vai Iknedēļas.* Turklāt noklusējuma vērtības izpildes laika koeficienta un **novirzes** **koeficienta laukiem** tiek ņemtas no vajadzību grupas. Šīs vērtības katrai rindai var labot pēc vajadzības.
1. Atlasiet laika periodu, kurā vēlaties aprēķināt ADU.
1. Darbību rūts cilnē Bufera **vērtības** atlasiet Aprēķināt vidējo **dienas lietojumu**. Sistēma mēģina apkopot datus, kas ir nepieciešami ADU aprēķinam, kā norādīts vajadzību [grupai](ddmrp-inventory-positioning.md).
1. Izpildiet kādu no šīm darbībām:

    - Ja nepieciešamie dati ir pieejami, aprēķina rezultāti tiek pievienoti kolonnai **Vidējais ikdienas** lietojums. Šajā gadījumā darbība nav nepieciešama.
    - Ja nepieciešamie dati nav pieejami, neviena vērtība netiek pievienota automātiski. Šādā gadījumā manuāli ievadiet plānotās vērtības katrai rindai, kurā plānojat aprēķināt bufera vērtības.

### <a name="calculate-and-apply-buffer-values"></a>Bufera vērtību aprēķināšana un pielietojiet tās

Krājumiem, kur izvēlaties atļaut [sistēmai](#set-up-buffers) automātiski aprēķināt bufera zonas, bufera vērtību aprēķinu var manuāli izraisīt, veicot šādas darbības.

1. Atbilstoši atšifrēšanas punkta krājumam konfigurējiet bufera aprēķinu, [...](#set-up-buffers)[aprēķiniet](#calc-lead-time) vai ievadiet atsaistītos izpildes laikus un [aprēķiniet](#calc-adu) vai ievadiet vidējo dienas lietošanu visiem atbilstošajiem laika periodiem, kā aprakstīts šajā rakstā.
1. Atveriet lapu **Krājumu** segums šim dekompozīcijas punkta elementam.
1. Atlasiet cilni **Bufera** vērtības, kurā jau ir jārāda laika periodu saraksts.
1. Atlasiet laika periodu, kurā jāaprēķina bufera vērtības. (Parasti šis laika periods būs periods, kas ietver šodienu.) Atlasītās rindas vērtībām jau ir jābūt vērtībām, kas nav nulles **, kolonnās Vidējais ikdienas** **lietojums un Atšifrētās izpildes laika** kolonnas.
1. Rediģējiet **lauku Pieprasījuma** korekcijas koeficients vienai vai vairākām rindām pēc vajadzības. Sistēma piemēros šo faktoru vidējā ikdienas lietošanas vērtībai **visos** buferu aprēķinos, kuros šī vērtība tiek izmantota. Šis koeficients ļauj koriģēt veidu, kādā pieprasījums svārstās pēc datuma (piemēram, brīvdienām vai sezonāliem krājumiem).
1. Darbību rūts cilnē Bufera **vērtības** atlasiet Aprēķināt min **., maks. un pārkārtoto punktu daudzumus**. Sistēma aprēķina un aizpilda **aprēķināto minimālo**, **·** **aprēķināto** pasūtījuma punktu un aprēķināto maksimālo kolonnu skaitu režģa lapā **Krājumu** vajadzība.
1. Kad aprēķināto vērtību pārskatīšana pabeigta, tās ir jālieto. Pretējā gadījumā tās neietekmēsies. Izmantojot aprēķinu vienai vai vairākām rindām, **vērtības no laukiem Aprēķinātais min**., **·** **·** **Aprēķinātais atkārtotais pasūtījums un Aprēķinātais maksimums attiecīgi tiek kopētas uz min**.,**·** **pasūtījuma punktu un Maks**. kolonnām. Darbību rūts cilnes Bufera **vērtības** grupā Veikt **darbību** atlasiet vienu no šīm pogām:

    - **Pieņemt visus aprēķinus** – pielietot visas aprēķinātās vērtības režģī.
    - **Apstipriniet aprēķinus atlasītajām rindām** – izmantojiet aprēķinātās vērtības tikai atlasītajām rindām.
    - **Atmest visus aprēķinus** – atmest visas aprēķinātās vērtības minimālajiem daudzumiem, maksimālajam daudzumam un atkārtota pasūtījuma punktiem režģī.
    - **Atmest aprēķinus atlasītajām rindām** – atmest visas aprēķinātās vērtības minimālajiem daudzumiem, maksimālajam daudzumam un pārkārtot punktus atlasītajām rindām.

### <a name="schedule-automatic-buffer-value-calculations"></a>Plānot automātiska bufera vērtības aprēķinus

Pēc tam, kad esat pilnīgi iestatījis DDMRP iestatījumus un apstiprinājis, ka tie darbojas, kā paredzēts, jūs, iespējams, vēlēsities iestatīt pakešuzdevumu periodiski pārrēķināt ADU un saistītās bufera vērtības pēc vajadzības, pamatojoties uz faktiskā patēriņa datiem un/vai atjauninātajām prognozēm. Šī procedūra attiecas tikai uz krājumiem, kuros izvēlaties ļaut sistēmai [automātiski aprēķināt bufera zonas](#set-up-buffers).

Sekojiet šiem soļiem, lai plānotu automātisko bufera vērtību aprēķinus.

1. Doties uz **vispārējās plānošanas vispārējās \> plānošanas \> DDMRP aprēķināt \> bufera vērtības**.
1. Bufera **vērtību aprēķināšanas** dialoglodziņā iestatiet šādus laukus:

    - **Aprēķināt vidējo dienas lietojumu** – iestatiet šo opciju *kā* Jā, lai pārrēķinātu dekomupēšanas punktu vienumu ADU katru reizi, kad tiek izpildīts darbs. Iestatiet to uz *Nē,* lai izlaistu šo aprēķinu. Parasti šo opciju vajadzētu iestatīt uz *Jā*.
    - **Aprēķināt dekompozīcijas izpildes laiku** — iestatiet šo opciju *kā* Jā, lai pārrēķinātu dekompozīcijas izpildes laikus katru reizi, kad darbs tiek palaists. Iestatiet to uz *Nē,* lai izlaistu šo aprēķinu. Parasti šo opciju vajadzētu iestatīt uz *Jā*.
    - **Bufera vērtību aprēķināšana** – iestatiet šo opciju kā Jā *,* lai atkārtoti aprēķinātu bufera vērtības katru reizi, kad tiek palaists darbs. Iestatiet to uz *Nē,* lai izlaistu šo aprēķinu. Parasti šo opciju vajadzētu iestatīt uz *Jā*.
    - **Pieņemt min., maks. un pārkārtošanas punkta** aprēķinu – *iestatiet* šo opciju uz Jā, lai automātiski apstiprinātu un lietotu pārrēķinātās bufera vērtības katru reizi, kad tiek izpildīts darbs. Iestatiet to uz *Nē*, lai nepārrēķinātās vērtības atstātu nepieejamas. Šajā gadījumā pārrēķinātās vērtības stāsies spēkā tikai tādā gadījumā, ja vien manuāli tās netiek lietotas **vēlāk no katras preces krājumu vajadzības** lapas. Parasti šo opciju vajadzētu iestatīt uz *Jā*.
    - **Vispārējais** plāns – atlasiet vispārējo plānu, kas ietver krājumus, kurus ietekmēs aprēķins. Aprēķins tiks attiecināts uz visām plāna filtra precēm, kuras turpmāk ierobežos šī **dialoglodziņa** filtra iestatījumi.

1. Lai ierobežotu ierakstu kopu, pie kuriem šis pakešuzdevums ir jāpalaiž, **kopsavilkuma** cilnē Ieraksti, lai iekļautu kopsavilkuma cilni, atlasiet Filtrēt, **·** **lai atvērtu dialoglodziņu** Uzziņas. Šis dialoglodziņš darbojas tāpat, kā citiem fona darbu [tipiem](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Piegādes ķēžu pārvaldībā.
1. Kopsavilkuma cilnē **Izpildīt fonā** norādiet, kā un cik bieži atlasītajiem krājumiem jāveic atlasītie aprēķini. Lauki darbojas tāpat, kā citi [fona darbu](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management.
1. Atlasiet **Labi**, lai pievienotu jauno darbu pakešuzdevumu rindai izpildei.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Pārskatīt un pārrēķināt atšifrēšanas izpildes laikus visiem krājumiem

Veiciet šos soļus, lai pārskatītu un pārrēķinātu visus atšifrējamos izpildes laikus, kas ir pieejami juridiskajā personām (uzņēmumam).

1. Dodieties uz **vispārējās plānošanas \> vispārējās plānošanas \> DDMRP dekompozīcijas \> izpildes laiku**.
1. Atšifrēta **izpildes laika** lapā pārlūkojiet un filtrējiet sarakstu pēc vajadzības, lai atrastu meklēto informāciju. Lai skatītu vēl vairāk informācijas par krājumu, atlasiet tā saiti krājuma **numura** kolonnā.
1. Ja vēlaties pārrēķināt dekompozīcijas izpildes laiku jebkuram elementam, **atlasiet elementu un pēc tam darbību rūtī atlasiet Aprēķināt dekompozīcijas** izpildes laiku. Tiek **parādīts dialoglodziņš Aprēķināt dekompozīcijas** izpildes laiku. Šis dialoglodziņš darbojas tāpat, kā tas ir, [aprēķinot tā](#calc-lead-time) paša elementa atšifrēšanas izpildes laikus krājumu **vajadzības** lapā.
