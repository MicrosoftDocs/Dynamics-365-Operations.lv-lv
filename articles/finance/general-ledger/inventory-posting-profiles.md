---
title: Krājumu grāmatošanas metodes
description: Šajā rakstā ir sniegts pārskats par krājumu grāmatošanas profiliem.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cae5b39ef8e6e153fe522dee1874deae2a2cb86e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901347"
---
# <a name="inventory-posting-profiles"></a>Krājumu grāmatošanas metodes

[!include [banner](../includes/banner.md)]

Noliktavas grāmatošanas metodes kontrolē krājumu apakšgrāmatas darbību grāmatošanu Virsgrāmatā. Krājumu apakšgrāmatas darījumus var ģenerēt **no** daudziem moduļiem, tostarp Pārdošana un mārketings, **Sagāde** un avotu, **Ražošanas** kontrole u.c. Krājumu apakšgrāmatas transakcijas var grāmatot jebkurā laikā, kad krājums tiek izmantots pārdošanas pasūtījumā vai pirkšanas pasūtījumā. 

Var grāmatot papildu krājumu apakšgrāmatas darījumus:
- Katru reizi, kad dokuments tiek atjaunināts.
- Grāmatojot pārdošanas pasūtījuma pavadzīmi vai rēķinu.
- Kad tiek ģenerēta pirkšanas pasūtījuma produktu ieejas plūsma vai rēķins.

Papildinformāciju skatiet krājumu apakšgrāmatas transakcijās.

## <a name="inventory-transaction-overview"></a>Krājumu darbību apskats

Katrā krājumu apakšgrāmatas darījumā ietilpst:
 - Daudzums 
 - Cena 
 - Vietne 
 - Noliktava 
 - Atrašanās vieta 

Krājumu apakšgrāmatas transakcijas izveido divus ierakstus Virsgrāmatā, izmantojot fizisko grāmatošanu un finanšu grāmatošanu. Papildinformāciju skatiet fiziskos [un finanšu atjauninājumos](/supply-chain/cost-management/physical-financial-updates.md).
Tālāk redzamais piemērs ir pirkšanas pasūtījums ar trīs rindām. Piemēram, pieņemiet, ka viss pasūtījums ir atsevišķai vietai un noliktavai. Katrai pirkšanas pasūtījuma rindai ir atsevišķs saistīts InventTrans ieraksts - zināms arī kā krājumu darbība - un katra rinda ir ar daudzumu 10. Šajā diagrammā parādīta viena pirkšanas pasūtījuma virsraksta saistība ar trim pirkšanas pasūtījuma rindām, katra ar vienu InventTrans ierakstu.

![Attiecību diagramma pirkšanas pasūtījumam ar trīs rindām katrs ar vienu InventTrans ierakstu.](./media/InventTransRelationship.PNG)

Pirmajā pirkšanas pasūtījuma rindā tiek saņemts daudzums 5. Pilns daudzums otrajai rindai, bet daudzums, kas nav saņemts pirkšanas pasūtījuma trešajā rindā. Tagad pastāv otra krājumu darbība, kas saistīta ar pirmo pirkšanas pasūtījuma rindu. Darbība otrajā pirkšanas pasūtījuma rindā tiks atjaunināta uz **Saņemts**, un trešā darbība paliks tā pati. Šajā diagrammā parādītas attiecības ar papildu InventTrans ierakstu pirkšanas pasūtījuma 1. rindai.

![Attiecību diagramma pirkšanas pasūtījumam ar trim rindām. Viena rinda ir daļēji saņemta un parāda divus InventTrans ierakstus.](./media/InventTransRelationshipPartialReceipt.PNG)

Šajā piemērā dokuments tiks grāmatots Virsgrāmatā; šis ir fiziskais dokuments. Krājumu modeļu grupa ir konfigurēta, lai grāmatotu fiziskos krājumus, un visi krājumi lieto to pašu krājumu modeļu grupu. Krājumu grāmatošanas metode tiek izmantota vienai galveno kontu kopai. Tiks izveidots viens dokuments, un InventTrans ieraksts saistīs gan InventTrans 1, gan InventTrans 2 ar vienu dokumentu.

Pēc tam tiek saņemts rēķins par daudzumu, kas ir saņemts 1. un 2. rindā. Virsgrāmatā ir izveidots cits dokuments; šis ir finanšu dokuments. Krājumu modeļu grupa ir konfigurēta finanšu krājumu grāmatošanai. Jaunais otrais dokuments ir saistīts ar InventTrans 1 un InventTrans 2.

Atkarībā no izmaksu modeļa, iespējams, jūsu krājumu apakšgrāmatas transakcijām saistībā ar krājumu slēgšanu un nosegšanu varētu eksistēt trešā virsgrāmatas grāmatošana. Lai iegūtu papildu informāciju, dodieties uz Krājumu [slēgšanu](/supply-chain/cost-management/inventory-close.md). Detalizētu informāciju par visām krājumu darbībām var skatīt, ejot uz vaicājumiem **par krājumu** > **vadību un pārskatiem** > **Par darbībām**.

>[!Important]
> Krājumu darbības tiks sadalītas katrai unikālai krājumu dimensiju kombinācijai un katrai daļējai atjaunināšanai. Tas tika parādīts iepriekšējā piemērā par daļējiem atjauninājumiem.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Sadalīt krājumus, pamatojoties uz krājumu dimensijas piemēru

Piemērā pirkšanas pasūtījuma rinda 3 ir serializēts krājums. Saņemšanas procesa laikā pirkšanas pasūtījumam tiek reģistrēti desmit sērijas numuri. Krājumu darbība tiks sadalīta 10 krājumu darbībās. Šajā diagrammā parādītas attiecības un papildu krājumu darbības, katru ar savu sērijas numuru saistībā ar 3. pirkšanas pasūtījumu.

![Attiecību diagramma pirkšanas pasūtījumam ar trim rindām. Viena rinda ir serializēta un rāda papildu InventTrans ierakstus](./media/InventTransRelationshipSerialNumber.PNG)

Iepriekš minētajā piemērā, ja katrs sērijas numurs tiek saņemts vienā produktu ieejas plūsmā, tiks izveidots viens papildu dokuments. Fiziskā dokumenta lauks tiks saistīts ar katru sērijas numuru. Tas pats attiecas uz finanšu atjauninājumu, kad pirkšanas pasūtījums tiek iekļauts rēķinā.

## <a name="inventory-transactions"></a>Krājumu darbības

Krājumu darbības var skatīt lapas Krājumu darbības **sadaļā Krājumu** un **noliktavas vadība vai** **Izmaksu pārvaldība**. Varat arī skatīt krājumu darbības, kas attiecas uz noteiktu pirmdokumenta rindu, piemēram, pirkšanas pasūtījuma rindu vai pārdošanas pasūtījuma rindu, atlasot **Krājumi** un pēc tam atlasot **Darbības**. 

Krājumu **darbību lapā** ir šādi lauki.

| Lauks            | Apraksts                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Krājuma numurs      | Ar darbību saistītais krājuma numurs.                                                                  |
| Fiziskais datums    | Datums, kad krājums tiek saņemts noliktavā, atstāj noliktavu, patērēts ražošanā vai tiek ražots. Piemēram, grāmatošanas datums
Pavadzīmes grāmatošana pārdošanas pasūtījumam vai produktu ieejas plūsmas grāmatošanai pirkšanas pasūtījumam.                             |
| Finansiālais datums   | Datums, kad krājumu darbība ir slēgta un izmaksas reģistrētas Virsgrāmatā. Piemēram, rēķina grāmatošanas datums 
ģenerēšanu pārdošanas vai pirkšanas pasūtījumam. Atsauces dokumenta atjauninājumi nav atļauti pēc finanšu datuma aizpildītiem. |
| Atsauce        | Norāda darbības avotu un laukā Numurs parādītā dokumenta **tipu**. Piemēram, pārdošanas pasūtījums, pirkšanas pasūtījums vai pārsūtīšanas pasūtījuma ieejas plūsma.                                                 |
| Numurs           | Norāda darbības atsauces ID. Piemēram, ja atsauces lauks **norāda** pārdošanas pasūtījumu, numura **lauks** norāda pārdošanas pasūtījuma numuru.                                                       |
| Ieejas plūsma (statuss) | Krājumu darbībām, kas ir saņemšanas, šis lauks norāda saņemšanas statusu. Piemēram, pirkšanas pasūtījums ir ieejas plūsma, un tā statuss varētu būt Pasūtīts **vai** Nopirkts **·**.                                                            |
| Izejas plūsma (statuss)   | Krājumu darbībām, kas ir izejas plūsmas, šis lauks norāda izejas plūsmas statusu. Piemēram, pārdošanas pasūtījums ir izdošana, un statuss varētu būt Pasūtīts **vai** Pārdots **·**.                         |
| Daudzums         | Krājumu darbības daudzums. Pozitīvi skaitļi tiek izmantoti krājumu saņemšanai, bet negatīvie skaitļi tiek izmantoti krājumu izejas plūsmām.                                                                                                                          |
| Vienība             | Mērvienība, kurā izteikts daudzums.                                                                                   |
| Pieļaujamā svara daudzums      | Darbības pieļaujamā svara daudzums. Papildinformāciju skatiet lapā Par pieļaujamā [svara krājumiem](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Pieļaujamā svara vienība          | Pieļaujamā svara mērvienība, norādīta pieļaujamā svara daudzuma vērtība.                                                         |
| Izmaksu summa      | Krājumu darbības beigu izmaksas. Lauks tiek aizpildīts, ja darbība tiek finansiāli atjaunināta. Atkarībā no izmaksu metodoloģijas, krājumu slēgšanas un koriģēšanas process var atjaunināt šo lauku.                            |

## <a name="inventory-status"></a>Krājumu statuss

Katrai krājumu darbībai ir statuss, kas tiek rādīts laukā Saņemšana **vai** **Izdošana**. Izmantotais lauks ir atkarīgs no krājumu darbību tipa. Ieejas plūsmas ir darbības, kas palielina krājumu. Piemēram, pirkšanas pasūtījums ar pozitīvu daudzumu vai pārdošanas pasūtījuma atgriešanu ar negatīvu daudzumu. Izejas plūsmas ir krājumu darbības, kas samazina krājumu daudzumu. Piemēram, pārdošanas pasūtījums ar pozitīvu daudzumu vai pirkšanas pasūtījuma atgriešana ar negatīvu daudzumu.

### <a name="receipt-status"></a>Ieejas plūsmas statuss

Tabulā ir aprakstīts ieejas **plūsmas** statuss.

| **Ieejas plūsmas statuss** | **Apraksts**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Pasūtīts            | Ieejas plūsmas krājumu darbību sākotnējais statuss. Tas ietver pirkšanas pasūtījumus ar pozitīvu daudzumu, ražošanas pasūtījumiem vai pārdošanas pasūtījuma atgriešanu ar negatīvu daudzumu.                                                   |
| Reģistrēts         | Šis statuss tiek izmantots, kad tiek veikts divu soļu saņemšanas process vai kad tiek izmantota krājumu saņemšana, lai norādītu, ka prece ir saņemta. To izmanto, kad partijas vai sērijas numuri tiek "piešķirti" vai reģistrēti pasūtījumā. Lai iegūtu papildu informāciju par krājumu pienākšanu, dodieties uz saņemšanas [apskatu](/supply-chain/inventory/arrival-overview.md). |
| Saņemts           | Šis statuss tiek izmantots, kad darbība ir fiziski atjaunināta. Pirkšanas pasūtījumam tas ir tad, kad tiek grāmatota produktu ieejas plūsma. Pārdošanas pasūtījuma atgriešanai tas ir tad, kad tiek grāmatota pavadzīme.                                                                            |
| Nopirkts          | Šis statuss tiek izmantots, kad darbība ir finansiāli atjaunināta. Pirkšanas pasūtījumam vai pārdošanas pasūtījuma atgriešanai tas ir tad, kad tiek ģenerēts rēķins.                                                                                             |

### <a name="issue-status"></a>Izejas plūsmas statuss

Tabulā ir aprakstīts problēmas **statuss**.

| **Izejas plūsmas statuss**  | **Apraksts**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Pasūtīts          | Izejas plūsmas darbību sākotnējais statuss. Tas ietver pārdošanas pasūtījumus ar pozitīvu daudzumu, ražošanas pasūtījumu MK vai formulas rindas, vai pirkšanas pasūtījuma atgriešanu ar negatīvu daudzumu.                                             |
| Rezervēts pasūtījumos  | Šis krājumu statuss norāda, ka krājumi ir rezervēti pret pasūtījumu, kas ir izveidots, bet vēl nav fiziski saņemts noliktavā. Kad krājums ir saņemts, statuss automātiski tiks atjaunināts uz Rezervēts **fiziski**. Lai iegūtu papildu informāciju par rezervācijām, dodieties uz Sadaļu [Rezervēt krājumu daudzumus](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Rezervēts fiziski | Šis statuss norāda, ka krājums ir piešķirts vai rezervēts pret noteiktu pasūtījumu. Kad krājumi ir rezervēti, tie nav fiziski pieejami citiem pasūtījumiem.                                 |
| Izdots         | Tas norāda, ka krājums ir izdots no noliktavas. Krājums joprojām ir fiziski noliktavā, nav noņemts, bet nav pieejams citiem pasūtījumiem.  |
| Atskaitīts          | Šis statuss tiek izmantots, kad darbība ir fiziski atjaunināta. Pārdošanas pasūtījumam tas notiek, grāmatojot pavadzīmi; pirkšanas pasūtījuma atgriešanai- šis vienums ir grāmatots produktu ieejas plūsmā.                                                                      |
| Pārdots              | Šis ir statuss, kas tiek izmantots, kad darbība ir finansiāli atjaunināta. Pirkšanas pasūtījumam vai pārdošanas pasūtījumam tas ir tad, kad tiek ģenerēts rēķins.|

Lai iegūtu papildu informāciju par krājumu darbībām, dodieties uz detalizētu informāciju [par krājumu darbībām](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Krājumu grāmatošanas metodes konfigurēšana

Lai konfigurētu krājumu grāmatošanas metodi, veiciet šādus soļus:

1.  Atveriet **krājumu vadības iestatījumu** > **grāmatošanas** > **·** > **grāmatošanu**.
2.  Atlasiet darbības tipa cilni. Piemēram, atlasiet Pirkšanas **pasūtījums**.
3.  Atlasiet radiopogu grāmatošanas tipam. Piemēram, atlasiet Pirkšanas **izdevumi izdevumiem**.
4.  Atlasiet **Jauna**.
5.  Laukā **Krājuma** kods atlasiet opciju Tabula **, Grupa** **·**, Visi **vai** **Kategorija**. Piemēram, lai konfigurētu grāmatošanas metodi specifiskai krājumu grupai, atlasiet **Grupa**.
     - **Ja 5.** solī atlasījāt Tabulu, atlasiet specifisko krājuma kodu grāmatošanas metodei **laukā Krājumu** saistība.
     - **Ja 5.** solī atlasījāt **Grupu**, laukā Krājumu saistība atlasiet grāmatošanas **metodei krājuma** grupu.
     - **Ja 5. solī** atlasījāt **Visi, krājumu saistības lauks** ir tukšs.
     - Ja 5. **solī** atlasījāt Kategoriju **, krājumu saistības lauks** ir tukšs. Lietojiet **lauku Kategorijas relācija**, lai atlasītu kategoriju, uz kuru attiecas grāmatošanas metode.

6.  Laukā **Konta kods atlasiet opciju Tabulai** **, Grupai** **vai** Visiem **.** Piemēram, lai grāmatošanas metodi piemērotu visiem kreditoriem, atlasiet **Visi**.
     - **Ja 5.** solī atlasījāt Tabulu, atlasiet konkrētu kreditora kodu grāmatošanas metodei **laukā Kontu** saistība.
     - **Ja 5.** solī atlasījāt Grupu, atlasiet kreditoru grupu grāmatošanas metodei **laukā Kontu** saistība.
     - **Ja 5.** solī atlasījāt **Viss, konta relācijas** lauks ir tukšs.

7.  Lai asociētu īpašu nodokļu grupu, kam ir atlasīts grāmatošanas tips, atlasiet **PVN grupu**. Ja šis lauks ir tukšs, grāmatošanas tips attiecas uz visām esošajām PVN grupām. Grāmatošana, kura ir norādīta PVN grupām, attiecas tikai uz pārdošanas un pirkšanas darbībām.
8.  Norādiet konta numuru, lai grāmatotu konta tipu laukā **Galvenais** konts. Ja konta numurs nav izveidots izmantošanai kā uzskaites tips, var izveidot jaunu kontu. Jūs izveidojat jaunu kontu Galvenā konta informācijas **lapā Virsgrāmatā**.

## <a name="additional-resources"></a>Papildu resursi

Katra cilne lapā Krājumu **grāmatošanas metode** attiecas uz apakšvirsgrāmatas nosaukumu Dynamics 365 Supply Chain Management. Papildinformāciju skatiet šeit:
-   [Pārdošanas pasūtījumu grāmatošana](sales-order-posting.md)
-   [Pirkšanas pasūtījuma grāmatošana](purchase-order-posting.md)
-   [Krājuma grāmatošana](inventory-posting.md)
-   [Ražošanas kontroles grāmatošana](production-posting.md)
-   [Standarta izmaksu novirzes grāmatošana](standard-cost-variance-posting.md)
