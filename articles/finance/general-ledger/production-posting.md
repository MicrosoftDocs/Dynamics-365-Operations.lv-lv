---
title: Ražošanas pasūtījuma grāmatošana
description: Šajā rakstā ir sniegta informācija par dažādiem ražošanas pasūtījumu grāmatošanas tipiem.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: d41725325a82b24c1e5aa6bd2c1a5322f3078ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879629"
---
# <a name="production-postings"></a>Ražošanas grāmatojumi

Šajā rakstā ir sniegta informācija par dažādiem grāmatošanas tipiem ražošanas pasūtījuma procesā.


## <a name="material-consumption"></a>Materiālu patēriņš

Materiāli tiek reģistrēti kā patērēti ražošanas procesa laikā, kad ražošanas izdošanas saraksta žurnāls tiek iegrāmatots. Tas izveido darbības, kas attur rīcībā esošos krājumus. Ražošanas parametros **var** norādīt, vai izejmateriālu vērtība, kas pašlaik tiek saražota (saukta par NP), ir jāgrāmato Virsgrāmatā.

Nepabeigto materiālu (NP) **·** **vērtība tiek grāmatota patērēto materiālu novērtētajām izmaksām un patērēto materiālu novērtētajām izmaksām NP** kontos. Ražošanas pasūtījuma izdošanas saraksta process ir fiziska grāmatošana krājumu darbībām, kas saistītas ar ražošanas pasūtījumu. Kad ražošanas pasūtījums ir reģistrēts kā pabeigts, fiziskās darbības tiek atceltas un saistītās krājumu darbības tiek finansiāli atjauninātas. Kad beigu žurnāls ir iegrāmatots, tiek izmantotas **patērēto materiālu** **izmaksas un patērēto materiālu izmaksas, tiek izmantoti** NP grāmatošanas tipi.

Ražošanas **cilne** lapā Noliktavas grāmatošanas profili **kontrolē,** kā ražošanas pasūtījumi tiek grāmatoti Virsgrāmatā. To izmanto, kad Virsgrāmatas **grāmatošanas** lauks lapā Ražošanas **kontroles** parametri **ir** iestatīts uz Krājums un resurss **, vai Krājums un** kategorija. 

Lai izdošanas sarakstu žurnāls ražošanas pasūtījumam tiktu grāmatots Virsgrāmatā, ir jāatbilst šādiem nosacījumiem:

-   Ražošanas **kontroles parametru lapā ir** jābūt atzīmētai izvēles rūtiņai Grāmatot **izdošanas sarakstu Virsgrāmatā**. Šo iestatījumu var ignorēt specifiskai vietai ražošanas kontroles parametros **pēc vietas** lapas.
-   Pirkšanas **pasūtījuma rindā** atlasītā krājuma krājumu **modeļu grupu lapā jābūt atzīmētai** izvēles rūtiņai Grāmatot fiziskos krājumus.
-   Krājumu grāmatošanas metodes lapā ir jānorāda **galvenie konti** šādiem grāmatošanas tipiem:
    -   **Patērēto materiālu novērtētās izmaksas**
    -   **Patērēto materiālu novērtētās izmaksas, NP**

## <a name="time-consumption"></a>laika patēriņš.

Laiks, ko darbinieki tērē ražošanas darbiem, tiek reģistrēts **Maršruta kartes žurnālā** vai **Darbu kartes žurnālā**. Kad šie žurnāli ir iegrāmatoti, virsgrāmatas grāmatošana atvēlētajā kontā resursiem, kas atrodas nepabeigtajā projektu (NP), tiek apstrādāta. Šī grāmatošana atspoguļo laika vērtību, kas pavadīts pie ražošanas pasūtījuma. Pēc tam, kad ražošanas pasūtījums ir reģistrēts kā pabeigts, šie NP konti tiek nosegti.

Ir trīs iespējamie veidi, kā grāmatot laika patēriņu atkarībā **no opcijas, kas atlasīta laukā Virsgrāmatas grāmatošana** lapā **Ražošanas kontroles parametri**.

## <a name="reporting-finished-goods-and-error-quantities"></a>Pārskati par pabeigtām precēm un kļūdainiem daudzumiem

Kad ražošanas pasūtījums ir **ziņots** kā pabeigts, pabeigtās preces tiek atjauninātas noliktavā, izmantojot **žurnālu Ziņot kā pabeigtu**. Ja izmantojat NP uzskaiti, Virsgrāmatas žurnāls tiek grāmatots, lai samazinātu NP kontu skaitu un palielinātu pabeigto preču krājumus. Žurnāls izmanto precei definētās standarta izmaksas. Ja ražošanas **kontroles parametru lapā** ir atlasīta opcija Izmantot **novērtēto izmaksu** cenu, tiks izmantotas novērtētās izmaksas no ražošanas pasūtījuma.

Izejmateriālu, kas atrodas nepabeigtajā ražošanā (NP), **·** **vērtība tiek grāmatota NP kontos Novērtētās ražošanas izmaksas un Aprēķinātās ražotās** izmaksas. Ražošanas **pasūtījuma pabeigšanas process** ir fiziskais atjauninājums krājumu darbībām, kas saistītas ar ražošanas pasūtījumu. Kad ražošanas pasūtījums ir pabeigts, fiziskās darbības tiek apgrieztas un saistītās krājumu darbības tiek finansiāli atjauninātas. Kad beigu žurnāls ir iegrāmatots, tiek izmantoti **ražoto** izmaksu **un ražoto izmaksu NP** grāmatošanas tipi.

Ražošanas **cilne** lapā Noliktavas grāmatošanas **profili tiek** izmantota, lai kontrolētu, kā ražošanas pasūtījumi tiks grāmatoti Virsgrāmatā. To izmanto, kad Virsgrāmatas **grāmatošanas** lauks lapā Ražošanas **kontroles** parametri **ir** iestatīts uz Krājums un resurss **, vai Krājums un** kategorija. Kopsavilkuma **cilni Virsgrāmatas krājumi** lapā **Ražošanas** grupas var izmantot arī, lai kontrolētu ražošanas pasūtījumu grāmatošanu, kad lauks ir iestatīts uz **Ražošanas grupas**.

Lai pabeigtu **žurnālu Ziņot kā pabeigtu** ražošanas pasūtījuma grāmatošanu Virsgrāmatā, jāatbilst šādiem nosacījumiem:
-   Ražošanas **kontroles parametru lapā ir jābūt** atzīmētai izvēles rūtiņai **Grāmatot pārskatu kā pabeigtu Virsgrāmatā**. Šo iestatījumu var ignorēt specifiskai vietai ražošanas kontroles parametros **pēc vietas** lapas.
-   Pirkšanas **pasūtījuma rindā** atlasītā krājuma krājumu **modeļu grupu lapā jābūt atzīmētai** izvēles rūtiņai Grāmatot fiziskos krājumus.
-   Galvenajiem kontiem jābūt norādītiem lapā Krājumu grāmatošanas **metode** šādiem grāmatošanas tipiem:
    -   **Plānotās ražošanas izmaksas**
    -   **Plānotās ražošanas izmaksas, NP**

## <a name="ending-the-production-order"></a>Ražošanas pasūtījuma pabeigšana

Pirms ražošanas pasūtījuma pabeigšanas faktiskās izmaksas tiek aprēķinātas saražotajiem daudzumiem. Visas novērtētās materiālu, darbu un papildu atbalsta izmaksas tiek apgrieztas un aizstātas ar faktiskajām izmaksām. Vispārējās pabeigtā krājuma izmaksas tiek debitētas **no ražoto** izmaksu konta un kreditētas uz **ražoto izmaksu NP** kontu. Materiāli, kas tika patērēti **ražošanas pasūtījuma laikā, tiek kreditēti patērēto materiālu izmaksās** un debitēti **NP konta materiālu izmaksās**.

Ja, palaižot **izmaksu aprēķinu**, atzīmējiet izvēles rūtiņu Beigt darbu, ražošanas pasūtījuma statuss tiek mainīts uz **Pabeigts**. Šis statuss neļauj pabeigtā ražošanas pasūtījumā nejauši iegrāmatot papildu izmaksas. Varat norādīt, ka pabeigto kļūdu daudzumu vērtība ir jāpiešķir labiem daudzumiem, kas tiek ziņoti kā pabeigti. Alternatīvi varat norādīt, ka kļūdu daudzumu vērtība tiek grāmatota atvēlētajā brāķa kontā. 

Lai norādītu noteiktu brāķa kontu, sekojiet šiem soļiem:
1.  Pārejiet uz **ražošanas kontroles iestatījuma** > **·** > **ražošanas kontroles parametriem**.
2.  Atlasiet cilni **Standarta** atjaunināšana.
3.  Laukā Brāķa **metode** atlasiet kontu **Brāķis**.
4.  Laukā Brāķa **konts** atlasiet galveno kontu, kur brāķis brāķa daudzumam ir jāgrāmato, kad ir pabeigts ražošanas pasūtījums. Piemēram, atlasiet izmaksu kontu, piemēram, 510380: Ražošanas brāķis.

Lai beigu žurnāls ražošanas pasūtījumam varētu grāmatot Virsgrāmatā, ir jāizpilda šādi nosacījumi:
-   Galvenajiem kontiem jābūt norādītiem lapā Krājumu grāmatošanas **metode vai** **Ražošanas grupas** šādiem grāmatošanas tipiem:
    -   **Patērēto materiālu izmaksas**
    -   **Patērēto materiālu izmaksas, NP**
    -   **Ražošanas izmaksas**
    -   **Ražošanas izmaksas, NP**
-   Šādiem tipiem izmaksu kategorijās **, resursu vai resursu** **grupu lapā** **ir** jānorāda galvenie konti:
    -   **Ražotās izmaksas saražotās**
    -   **Patērētās ražošanas izmaksas, NP**

## <a name="indirect-costs-for-production-orders"></a>Ražošanas pasūtījumu netiešās izmaksas

Apstrādājot darbības ražošanas pasūtījumam, jūs varat konfigurēt netiešās izmaksas, lai tvertu pieskaitāmās izmaksas vai papildu maksas virsgrāmatā. Fiziskās darbības netiešajām izmaksām tiek atpazītas krājumos, kad iegrāmatojiet izdošanas saraksta žurnālu vai ziņojiet par pabeigtu žurnālu. Grāmatojot beigu žurnālu, netiešās izmaksas finanšu darbības tiek atpazītas krājumos.

Varat atpazīt netiešās izmaksas laika patēriņā, kas saistīts **ar Maršruta** karšu žurnāliem vai **Darbu karšu** žurnāliem. Beigot ražošanas pasūtījumu, šīs darbības tiek atceltas un grāmatotas finanšu kontos. Plašāku informāciju skatiet izmaksu aprēķināšanas [lapās](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Grāmatošanas Virsgrāmatā kontroles līmenis

Lapā Ražošanas **kontroles parametri varat** izmantot virsgrāmatas grāmatošanas **lauku**, lai iestatītu virsgrāmatas grāmatošanas līmeni ražošanas procesiem. 

Pieejami tālāk norādītie lauki:

### <a name="item-and-resource"></a>Krājums un resurss

Atlasot opciju Krājums **un resurss** Virsgrāmatas grāmatošanas **laukā**, grāmatošanas konti tiek nāk no operācijas maršrutā resursa vai resursu grupas. Konti konkrētajā resursā būs pirmā grāmatošanas opcija. Ja konts nav norādīts, tiks izmantoti resursu grupā norādītie konti. Katrai operācijas rindai maršrutā var būt viens resurss, kas norādīts kā **Izmaksu aprēķināšanas resurss**. Šis resurss tiek izmantots, lai noteiktu kontu, kas jāizmanto. Šī opcija parasti tiek izmantota, kad organizācija piešķir operācijas izmaksas resursiem. Izmaksas bieži ir augstākas resursiem un tiek izmantotas, lai palīdzētu pieņemt lēmumus "veikt pret pirkšanu". Šī ir detalizētākā grāmatošanas konfigurācija un ļauj granulētāko grāmatojumu kontroli un ražošanas procesa detalizētāko analīzi.

### <a name="item-and-category"></a>Krājums un kategorija

Atlasot opciju Krājums **un kategorija** **Virsgrāmatas** grāmatošanas laukā, grāmatošanas konti nāks no izmaksu kategorijas lapas, **kas** saistīta ar katru maršruta rindu. Katrai operācijas rindai maršrutā var būt trīs izmaksu kategorijas: **Uzstādīšanas** laiks, **Izpildes** laiks un **Daudzums**. Šī opcija parasti tiek izmantota, kad jūsu organizācijas galvenais fokuss ir uz procesa efektivitāti un aktivitātes ilgumu. Šī opcija ir vairāk apkopots grāmatošanas veids un joprojām nodrošina veidu, kā grupēt izmaksas kategorijās.

### <a name="production-group"></a>Ražošanas uzdevumu grupa

Atlasot opciju Ražošanas **grupas** virsgrāmatas grāmatošanas **laukā**, grāmatošanas konti tiek nāk no lapas **Ražošanas** grupas. **Ražošanas grupas** parasti tiek lietotas, ja vairāk nekā viena ražošanas rinda lieto līdzīgus produktus vai tai ir līdzīgs aprīkojums. Šo opciju var izmantot, lai salīdzinātu izmaksas divās dažādās ražošanas grupās.  
  
> [!NOTE]
> Ja pabeigto krājumu izmaksu aprēķināšanai tiek izmantota standarta metode, to atspoguļos beigu darbības. Ja faktiskās izmaksas un izmaksas, kas tiek aprēķinātas, izmantojot standarta metodi, atšķiras, atšķirības tiek grāmatotas kontā, kas rāda peļņu vai zaudējumus.

### <a name="route-groups-and-ledger-posting"></a>Maršrutu grupas un grāmatošana Virsgrāmatā

Katrai operācijas rindai maršrutā ir **norādīta Maršrutu** grupa. Laukus Uzstādīšanas laiks, **·** **·** **·** **·** **·** **Izpildes laiks un Daudzums, kas atrodas Maršruta grupa prognozē un izmaksu grupā, izmanto, lai kontrolētu, vai laiks tiks izmantots izmaksu grāmatošanai, grāmatojot darba karti vai maršruta kartes** žurnālu ražošanas pasūtījumā.**·** Ja opcijas ir deaktivizētas, dokuments netiks izveidots virsgrāmatā laika patēriņam.

Lai maršruta **karte vai** darbu **karšu žurnāls** varētu grāmatot ražošanas pasūtījuma Virsgrāmatā, jāizpilda šādi nosacījumi:

-   Maršruta **grupas** lapas izmaksu **un** **novērtējumu grupā ir jāatlasa** lauks Uzstādīšanas laiks, **Izpildes laiks** **vai** Daudzums.
-   Šādiem grāmatošanas tipiem galvenos **kontus** **ir jānorāda vai** **nu** lapā Izmaksu kategorija, Maršruts, **Maršrutu** grupa vai Ražošanas grupas:
    -   Plānotās ražošanas netiešās izmaksas
    -   Patērētās ražošanas novērtētās izmaksas, NP

Šajā diagrammā parādīta maršruta grupas saistība ar kopējās izmaksas aprēķināšanu katrai operācijai (maršruta rinda) noteiktā maršrutā. Katrai maršruta rindai ir viena maršrutu grupa. Maršruta grupa kontrolē uzstādīšanas laika, izpildes laika un daudzuma parametrus. Izmaksu **kategoriju cilnei** ir trīs opcijas **iestatīšanai**, **palaišanai** un daudzumam **,** kas tiek aktivizēti, pamatojoties uz maršruta grupu iestatījumiem. Kopsavilkuma **cilnē Hronometrāžas** ir trīs lauki, kas balstīti uz maršruta grupu.

Izmantotā formula ir balstīta uz to, vai opcija ir aktivizēta maršruta grupā. Izmaksas no atlasītās izmaksu kategorijas tiek reizinātas ar daudzumu, kas tika ievadīts hronometrāžas, lai aprēķinātu kopējās izmaksas.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Maršruta grupu saistība ar kopējām aprēķinātajām izmaksām.":::
Maršruta grupu saistība ar kopējām aprēķinātajām izmaksām. Katrai maršruta rindai ir viena maršrutu grupa. Maršruta grupa kontrolē uzstādīšanas laika, izpildes laika un daudzuma parametrus. Izmaksu kategoriju cilnei ir trīs opcijas iestatījumam, palaišanai un daudzumam, kas ir iespējoti, pamatojoties uz maršruta grupu iestatījumiem. Kopsavilkuma cilnē Hronometrāža ir trīs lauki, kas ir iespējoti un kuriem tiek izmaksātas izmaksas, pamatojoties uz maršruta grupu. Izmantotā formula ir balstīta uz to, ja opcija ir aktivizēta maršruta grupā. Izmaksas no atlasītās izmaksu kategorijas tiek reizinātas ar daudzumu, kas ievadīts hronometrāžas, lai aprēķinātu kopējās izmaksas.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Grāmatošanas metodes konfigurācijas paraugs

Tālāk sniegtajā tabulā ir norādīti noklusējuma grāmatošanas tipu piemēri ar galvenajiem kontiem un aprakstiem. 

 - Kolonna **Debets** /kredīts norāda, vai darbība parasti ir debets vai kredīts, vai arī dažos gadījumos tā var grāmatot. 
 - Kolonna **Klīringa** konts norāda, vai grāmatošanas tips ir tīrīšanas konts. Šajā kontā grāmatotā summa tiek automātiski apgriezta, grāmatojot vēlāku darbību. 
 - P **/F kolonna** norāda P fiziskai **grāmatošanai** un **F finanšu** grāmatošanai. 
 - Kolonna **Vienāda** norāda, vai galvenais konts noteiktam grāmatošanas tipam parasti ir tāds pats kā cits grāmatošanas tips. Vērtība kolonnā norāda grāmatošanas tipu, kam parasti sekots.

> [!NOTE]
> Ieteiktie galvenie konti un galveno kontu nosaukumi ir ieteikumi. Ieteicams strādāt ar savu grāmatvedi, lai noteiktu biznesa vajadzībām labāko konfigurāciju.


| Grāmatošanas tips  | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs| Konta veids | Vai debets/kredīts? | Dzēšanas konts | Fiziska vai finanšu | Izpildiet | Apraksts |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Patērēto materiālu novērtētās izmaksas      | 140100               | Materiālu krājumi        | Līdzeklis        | Kredīts         | Y                | P                     | Patērēto materiālu izmaksas                | Šo kontu izmanto, grāmatojot ražošanas pasūtījuma izdošanas saraksta žurnālu. Korespondējošais konts ir materiālu, NP novērtētās izmaksas. Summa šajā kontā tiek automātiski atcelta, kad ražošanas pasūtījums ir pabeigts. Šis konts parāda krājumu kontu bilancē.       |
| Patērēto materiālu novērtētās izmaksas, NP | 150150               | Ražošanas NP – materiāli | Līdzeklis        | Debets          | Y                | P                     | Plānotās ražošanas izmaksas, NP          | Šo kontu izmanto, grāmatojot ražošanas pasūtījuma izdošanas saraksta žurnālu. Šī konta korespondējošais konts ir aprēķinātās patērēto materiālu izmaksas. Summa šajā kontā tiek automātiski atcelta, kad ir pabeigts ražošanas pasūtījums. Šis konts jūsu bilancē parāda NP.                  |
| Plānotās ražošanas izmaksas               | 140200               | Pabeigto preču krājumi   | Līdzeklis        | Debets          | Y                | P                     | Ražošanas izmaksas                         | Šo kontu izmanto, kad ražošanas pasūtījumam grāmatojat pārskatu kā pabeigtu žurnālu. Korespondējošais konts ir aprēķinātās ražošanas izmaksas, NP. Summa šajā kontā tiek automātiski atcelta, kad ražošanas pasūtījums ir pabeigts. Šis konts parāda krājumu kontu bilancē. |
| Plānotās ražošanas izmaksas, NP          | 150150               | Ražošanas NP – materiāli | Līdzeklis        | Kredīts         | Y                | P                     | Ražošanas izmaksas, NP                    | Šo kontu izmanto, kad ražošanas pasūtījumam grāmatojat pārskatu kā pabeigtu žurnālu. Korespondējošais konts ir novērtētās ražošanas izmaksas. Summa šajā kontā tiek automātiski atcelta, kad ir pabeigts ražošanas pasūtījums. Šis konts jūsu bilancē parāda NP.                     |
| Patērēto materiālu izmaksas                | 140100               | Materiālu krājumi        | Līdzeklis        | Kredīts         | Nē                 | F                     | Patērēto materiālu novērtētās izmaksas      | Šis konts tiek lietots, lai identificētu materiālus, kas patērēti ražošanas pasūtījumā beigu procesa laikā. Korespondējošais konts ir patērēto materiālu izmaksas, NP.                                                                                                    |
| Patērēto materiālu izmaksas, NP           | 150150               | Ražošanas NP – materiāli | Līdzeklis        | Debets          | Nē                 | F                     | Patērēto materiālu novērtētās izmaksas, NP | Šis konts tiek lietots, lai atpazītu materiālus NP, kas patērēts ražošanas pasūtījumā beigu procesa laikā. Korespondējošais konts ir patērēto materiālu izmaksas.                                                |
| Ražošanas izmaksas                         | 140200               | Pabeigto preču krājumi   | Līdzeklis        | Debets          | Nē                 | F                     | Plānotās ražošanas izmaksas               | Šis konts tiek lietots, lai identificētu pabeigtās preces izmaksas, ko veido ražošanas pasūtījums, pabeidzot ražošanas pasūtījumu. Korespondējošais konts ir ražošanas izmaksu, NP konts.                                                                  |
| Ražošanas izmaksas, NP                    | 150150               | Ražošanas NP – materiāli | Līdzeklis        | Kredīts         | Nē                 | F                     | Plānotās ražošanas izmaksas, NP          | Šis konts tiek lietots, lai identificētu saražotās preces izmaksas NP, ko veido ražošanas pasūtījums, pabeidzot ražošanas pasūtījumu. Korespondējošais konts ir ražošanas izmaksu konts.                                     |

> [!NOTE]
> Racionālā **pakalpojuma NP ieejas** plūsmas un **racionālā pakalpojuma NP tīrīšanas** konts tiek izmantots ar atgriezeniskām izmaksu np ražošanas izmaksām. Lai iegūtu papildu informāciju, dodieties [uz atgriezenisko izmaksu aprēķināšanas sistēmu](/supply-chain/cost-management/backflush-costing.md).

