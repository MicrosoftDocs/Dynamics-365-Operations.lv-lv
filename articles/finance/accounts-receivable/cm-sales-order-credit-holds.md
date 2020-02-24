---
title: Kredīta aizturēšana pārdošanas pasūtījumiem
description: ''
author: mikefalkner
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 23f819139e74d81d24810c63bae1de19358983b9
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015315"
---
# <a name="credit-holds-for-sales-orders"></a>Kredīta aizturēšana pārdošanas pasūtījumiem
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Šajā tēmā ir aprakstīti kārtulu iestatījumi, kas tiek izmantoti, lai nodotu pārdošanas pasūtījumu kredīta aizturēšanai. Kredīta pārvaldības aizturēšanas kārtulas var tikt piemērotas atsevišķam debitoram vai debitoru grupai.  Aizturēšanas kārtulas nosaka atbildes uz tālāk norādītajiem apstākļiem.

1. Kavēto dienu skaits
2. Kontu statuss
3. Apmaksas nosacījumi
4. Kredītlimita derīgums beidzies
5. Nokavētā summa
6. Pārdošanas pasūtījuma summa
7. Izmantotā pieejamā kredīta daļa

Pastāv divi papildu parametri, kas kontrolē citus scenārijus, kas bloķēs pārdošanas pasūtījumu

1. Izmaiņas maksājuma noteikumos
2. Izmaiņas norēķinu atlaidēs

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Aizturēšanas un izslēgšanas kārtulu iestatīšana

Kad debitors sāk pārdošanas transakciju, informācija par pārdošanas pasūtījumu tiek pārskatīta, ņemot vērā aizturēšanas kārtulu kopu, kas nosaka, vai palielināt debitora kredīta summu un vai ļaut pārdošanai turpināties. Varat arī definēt izņēmumus, kas ignorēs aizturēšanas nosacījumus un ļaus apstrādāt pārdošanas pasūtījumu. Varat iestatīt aizturēšanas un izslēgšanas kārtulas lapā **Kredīta pārvaldība > Iestatījumi > Kredīta pārvaldības iestatīšana > Aizturēšanas kārtulas**.

### <a name="days-overdue"></a>Maksājuma saņemšanas laiks nokavēts

Atveriet cilni **Kavētās dienas**, ja aizturēšanas kārtula attiecas uz debitoru, kam ir viens vai vairāki rēķini, kas ir kavēti jau noteiktu dienu skaitu.
1. Atlasiet tā debitora diapazonu, kuram šī kārtula ir **Derīga**.
   - Atlasiet sadaļu **Tabula**, ja kārtula attiecas uz noteiktu debitoru.
   - Atlasiet sadaļu **Grupa**, ja kārtula tiek piemērota debitoru grupas līmenī. 
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem.
2. Kad diapazons ir norādīts, jums jānorāda **Konts/grupa**, kas tiks izmantota diapazonā.
   - Diapazonam **Tabula** uzmeklēšana nodrošinās sarakstu ar debitoriem, kuri jāatlasa. 
   - Atlasiet **Grupa**, ja kārtula attiecas uz debitora kredīta grupu.
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem. 
3. Atlasiet **Riska grupa**, lai izmantotu kritērijus kredīta pārvaldības aizturēšanas piemērošanai debitoriem, kas grupēti pēc vispārēju faktoru kopuma, piemēram, Dun un Bradstreet vērtējuma, to gadu skaits, kad tie bijuši biznesā, laiks, cik ilgi tie bijuši jūsu klienti, un tā tālāk.  
4. Atlasiet kārtulas veidu, ko jūs iestatāt. Opcija **Aizturēšana** radīs kārtulu, kas bloķē pasūtījumu. Opcija **Izslēgšana** radīs kārtulu, kas izslēdz citu kārtulu no pasūtījuma aizturēšanas. 
5. Atlasiet **Vērtības veids**. Noklusējuma ieraksts ir fiksēts dienu skaits. Ja izveidojat izslēgšanu, varat norādīt fiksētu dienu skaitu vai summu. 
6. Ievadiet **Kavēto** dienu skaitu, kas tiks atļauts atlasītajai aizturēšanas kārtulai, pirms pasūtījums tiek nodots kredīta pārvaldības aizturēšanas pārskatīšanai. Nokavēto dienu skaits atspoguļo papildu pagarinājuma dienu skaitu, kas tiek pievienots dienu skaitam, kas ir pēc apmaksas datuma, kas var būt rēķinam, pirms tas tiek uzskatīts par nokavētu. Ja **Vērtības tips** norādīts kā izslēgšanas summu, tad ievadiet summu un valūtu šai summai.

### <a name="accounts-status"></a>Kontu statuss

Atveriet cilni **Konta statuss**, ja aizturēšanas kārtula attiecas uz debitoru ar atlasīto konta statusu.
1. Atlasiet kārtulas veidu, ko jūs iestatāt.  Opcija **Aizturēšana** radīs kārtulu, kas aiztur pasūtījumu. Opcija **Izslēgšana** rada kārtulu, kas izslēdz citu kārtulu no pasūtījuma aizturēšanas. 
2. Atlasiet tādu vienuma **Konta statuss** vērtību, kas liks kārtulai aizturēt pārdošanas pasūtījumu vai izslēgt to.

### <a name="terms-of-payment"></a>Apmaksas nosacījumi

Atlasiet **Apmaksas nosacījumi**, ja aizturēšanas kārtula attiecas uz atlasīto apmaksas termiņu.
1. Atlasiet kārtulas veidu, ko jūs iestatāt.  Opcija **Aizturēšana** radīs kārtulu, kas aiztur pasūtījumu. Opcija **Izslēgšana** rada kārtulu, kas izslēdz citu kārtulu no pasūtījuma aizturēšanas. 
2. Atlasiet tādu vienuma **Apmaksas nosacījumi** vērtību, kas liks kārtulai aizturēt pārdošanas pasūtījumu vai izslēgt to.

### <a name="credit-limit-expired"></a>Kredītlimita derīgums beidzies

Atveriet cilni **Ir beidzies kredīta limits**, ja aizturēšanas kārtula attiecas uz debitoriem ar kredīta ierobežojumiem, kuri ir sasniegti.
1. Atlasiet tā debitora diapazonu, kuram šī kārtula ir **Derīga**.
   - Atlasiet sadaļu **Tabula**, ja kārtula attiecas uz noteiktu debitoru.
   - Atlasiet sadaļu **Grupa**, ja kārtula tiek piemērota debitoru grupas līmenī. 
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem.
2. Kad diapazons ir norādīts, jums jānorāda **Konts/grupa**, kas tiks izmantota diapazonā.
   - Diapazonam **Tabula** uzmeklēšana nodrošinās sarakstu ar debitoriem, kuri jāatlasa. 
   - Atlasiet **Grupa**, ja kārtula attiecas uz debitora kredīta pārvaldības grupu.
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem. 
3. Atlasiet **Riska grupa**, lai turpmāk ierobežotu to debitoru sarakstu, kuri tiks nodoti kredīta pārvaldības aizturēšanai. 
4. Atlasiet kārtulas veidu, ko jūs iestatāt. 
  - Atlasiet **Aizturēšana**, lai radītu kārtulu, kas aiztur pasūtījumu. 
  - Atlasiet **Izslēgšana**, lai radītu kārtulu, kas izslēdz citu kārtulu no pasūtījuma aizturēšanas. 
6. Ievadiet **Dienas, kopš kredīta limits ir sasniegts** atlasītajai aizturēšanas kārtulai, pirms pasūtījums tiek nodots kredīta pārvaldības aizturēšanai. Nokavēto dienu skaits nozīmē papildu pagarinājuma dienas, kas pievienotas dienu skaitam, kuras kredīta limits ir pārsniegts.

### <a name="overdue-amount"></a>Nokavētā summa

Atveriet cilni **Nokavētā summa**, ja aizturēšanas kārtula attiecas uz debitoriem ar nokavētiem maksājumiem.
1. Atlasiet tā debitora diapazonu, kuram šī kārtula ir **Derīga**.
   - Atlasiet sadaļu **Tabula**, ja kārtula attiecas uz noteiktu debitoru.
   - Atlasiet sadaļu **Grupa**, ja kārtula tiek piemērota debitoru grupas līmenī. 
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem.
2. Kad diapazons ir norādīts, jums jānorāda **Konts/grupa**, kas tiks izmantota diapazonā.
   - Diapazonam **Tabula** uzmeklēšana nodrošinās debitoru uzmeklēšanu. 
   - Atlasiet **Grupa**, ja kārtula attiecas uz debitora kredīta pārvaldības grupu.
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem. 
3. Atlasiet **Riska grupa**, ja vēlaties turpmāk ierobežot to debitoru sarakstu, kuri tiks nodoti kredīta pārvaldības aizturēšanai. 
4. Atlasiet kārtulas veidu, ko jūs iestatāt. 
  - Atlasiet **Aizturēšana**, lai radītu kārtulu, kas aiztur pasūtījumu. 
  - Atlasiet **Izslēgšana**, lai radītu kārtulu, kas izslēdz citu kārtulu no pasūtījuma aizturēšanas. 
5. Ievadiet **Nokavētā summa** atlasītajai aizturēšanas kārtulai, pirms pasūtījums tiek nodots kredīta pārvaldības aizturēšanas pārskatīšanai. 
6. Atlasiet tādu vienuma **Vērtības veids** vērtību, kas nosaka vērtības veidu, kas tiks izmantots, lai pārbaudītu, cik daudz kredīta limita ir izmantots. Aizturēšanas kārtulās ir jānorāda procenti, bet izslēgšanai var būt norādīta fiksēta summa vai procenti.
slieksnis. Slieksnis ir saistīts ar kredīta limitu.
7. Ievadiet vērtību **Kredīta limita slieksnis** atlasītajai kārtulai, pirms debitors turpina kredīta pārvaldības aizturēšanu. Tā var būt summa vai procenti, kas balstīti uz vērtības tipu, kas atlasīts vērtības tipā.
8. Kārtula pārbauda, vai ir pārsniegtas vērtības **Kavētā summa** un **Kredīta limita slieksnis**. 

### <a name="sales-order"></a>Pārdošanas pasūtījums 

Atlasiet **Pārdošanas pasūtījums**, ja bloķēšanas kārtula attiecas uz pārdošanas pasūtījuma vērtību.
1. Atlasiet tā debitora diapazonu, kuram šī kārtula ir **Derīga**.
   - Atlasiet sadaļu **Tabula**, ja kārtula attiecas uz noteiktu debitoru.
   - Atlasiet sadaļu **Grupa**, ja kārtula tiek piemērota debitoru grupas līmenī. 
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem.
2. Kad diapazons ir norādīts, jums jānorāda **Konts/grupa**, kas tiks izmantota diapazonā.
   - Diapazonam **Tabula** uzmeklēšana nodrošinās debitoru uzmeklēšanu. 
   - Atlasiet **Grupa**, ja kārtula attiecas uz debitora kredīta pārvaldības grupu.
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem. 
3. Atlasiet **Riska grupa**, ja vēlaties turpmāk ierobežot to debitoru sarakstu, kuri tiks nodoti kredīta pārvaldības aizturēšanai. 
4. Atlasiet kārtulas veidu, ko jūs iestatāt.  
  - Atlasiet **Aizturēšana**, lai radītu kārtulu, kas aiztur pasūtījumu. 
  - Atlasiet **Izslēgšana**, lai radītu kārtulu, kas izslēdz citu kārtulu no pasūtījuma aizturēšanas. 
6. Ievadiet vienuma **Pārdošanas pasūtījuma summa** vērtību atlasītajai aizturēšanas kārtulai, pirms pasūtījums tiek nodots kredīta pārvaldības aizturēšanai. 

Pārdošanas pasūtījuma kārtulā ir ietverts papildu iestatījums, kas ignorē visas pārējās kārtulas. Lai izveidotu izņēmumu, kas izpildīs pārdošanas pasūtījumu, neņemot vērā nekādu citu kārtulu ietekmi, atzīmējiet izvēles rūtiņu **Izpildīt pārdošanas pasūtījumu**, kas atrodas izņēmumu rindā.

### <a name="credit-limit-used"></a>Kredītlimits izmantots

Atlasiet **Izmantotais kredīta limits**, ja bloķēšanas kārtula attiecas uz debitora kredīta limita summu, kas izmantota.
1. Atlasiet tā debitora diapazonu, kuram šī kārtula ir **Derīga**.
   - Atlasiet sadaļu **Tabula**, ja kārtula attiecas uz noteiktu debitoru.
   - Atlasiet sadaļu **Grupa**, ja kārtula tiek piemērota debitoru grupas līmenī. 
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem.
2. Kad diapazons ir norādīts, jums jānorāda **Konts/grupa**, kas tiks izmantota diapazonā.
   - Diapazonam **Tabula** uzmeklēšana nodrošinās debitoru uzmeklēšanu. 
   - Atlasiet **Grupa**, ja kārtula attiecas uz debitora kredīta pārvaldības grupu.
   - Atlasiet **Visi**, ja kārtula attiecas uz visiem debitoriem. 
3. Atlasiet **Riska grupa**, ja vēlaties turpmāk ierobežot to debitoru sarakstu, kuri tiks nodoti kredīta pārvaldības aizturēšanai. 
4. Atlasiet kārtulas veidu, ko jūs iestatāt.
   - Atlasiet **Aizturēšana**, lai radītu kārtulu, kas aiztur pasūtījumu. 
   - Atlasiet **Izslēgšana**, lai radītu kārtulu, kas izslēdz citu kārtulu no pasūtījuma aizturēšanas. 
5. Atlasiet **Atlikušais slieksnis**, kas nosaka kredīta limita procentus, kas aizturēs pārdošanas pasūtījumu. Ja pasūtījuma vērtība palielina kredīta limita summu, kas tiek izmantota virs procentiem, tad pasūtījums tiks aizturēts. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Aizturēt pārdošanas pasūtījumu, pamatojoties uz citiem kritērijiem
  
### <a name="rank-payment-terms"></a>Ranžēt maksājuma nosacījumus  

Varat piespiest kredīta kontroles kārtulas, kas jāizpilda, kad tiek mainīti maksājuma nosacījumi. Ierindojiet apmaksas nosacījumus un piešķiriet tiem ranga vērtību. Ja apmaksas noteikumus mainīsiet uz apmaksas noteikumiem, kuru vērtējums ir augstāks par iepriekšējiem apmaksas noteikumiem, pasūtījums tiks nosūtīts kredīta pārvaldībai un tam būs nepieciešams apstiprinājums.

Varat iestatīt apmaksas noteikumu klasifikāciju lapā **Kredīta pārvaldība > iestatījumi > Kredīta pārvaldības iestatīšana > Kārtot apmaksas noteikumus pēc ranga**.

1. Atlasiet apmaksas noteikumus laukā **Apmaksas noteikumu**, lai kārtotu pēc ranga; kad atlasāt noteikumu, apraksts tiks parādīts laukā **apraksts**.
2. Laukā **Rangs** atlasiet noteikuma rangu. Vērtības ir relatīvas attiecībā viena pret otru, lai varētu izmantot 1, 2, 3 vai 10, 20, 30. Lielākajai daļai noteikumu var izmantot vienu un to pašu vērtību, lai kredīta pārbaude aktivizētu tikai vienu vai divus apmaksas noteikumus.

### <a name="rank-settlement-discounts"></a>Ranžēt norēķinu atlaides   

Varat piespiest kredīta kontroles kārtulas, kas jāizpilda, kad tiek mainītas norēķinu atlaides. Ierindojiet norēķinu atlaides un piešķiriet tām ranga vērtību. Ja norēķinu atlaides mainīsiet uz norēķinu atlaidēm, kuru vērtējums ir augstāks par iepriekšējām norēķinu atlaidēm, pasūtījums tiks nosūtīts kredīta pārvaldībai un tam būs nepieciešams apstiprinājums.

Varat iestatīt apmaksas noteikumu klasifikāciju lapā **Kredīta pārvaldība > iestatījumi > Kredīta pārvaldības iestatīšana > Kārtot norēķinu atlaides pēc ranga**.

1. Atlasiet vienuma **Termiņatlaide** vērtību, kuru vēlaties kārtot pēc ranga. Tiks parādīts norēķinu atlaides **Apraksts**.
2. Atlasiet vērtību **Rangs**. Vērtības ir relatīvas attiecībā viena pret otru, lai varētu izmantot 1, 2, 3 vai 10, 20, 30. Lielākajai daļai norēķinu atlaižu var izmantot vienu un to pašu vērtību, lai kredīta pārbaude aktivizētu tikai vienu vai divas norēķinu atlaides.

## <a name="sequence-the-application-of-rules"></a>Noteikumu piemērošanas secība

Kārtulas tiek palaistas noteiktā secībā, ko maināt, lai tās atbilstu jūsu organizācijas vajadzībām. 

- Viena pārdošanas pasūtījuma izslēgšanas kārtulu instancēm ļauj ignorēt visas kārtulas, kas varētu aizturēt pārdošanas pasūtījumu. Izveidojiet pārdošanas pasūtījuma izslēgšanas kārtulu un atzīmējiet opciju **Izpildīt pārdošanas pasūtījumu**. Pasūtījums netiks aizturēts, ja šis izslēgšanas nosacījums ir patiess, un netiks pārbaudītas citas kārtulas.
- Aizturēšanas kārtulas var nodot aizturēto pasūtījumu.
- Izslēgšanas kārtulas var darboties pēc aizturēšanas kārtulām. Izslēgšanas kārtulas ietekmēs tikai to kārtulu, kurā tās ir definētas. 
- Aizturēšanas un izslēgšanas kārtulas tiek izpildītas tabulā, pēc tam grupā, pēc tam visos pasūtījumos. Šīs apstrādes secības dēļ aizturēšanas kārtula var pastāvēt visos līmeņos, kuri netiks izpildīti, jo ir palaista izslēgšanas kārtula tabulas vai grupas līmenī.
- Izņēmumi neignorē aizturēšanas kārtulu, ja tie atrodas vienā līmenī. Piemēram, izslēgšanas kārtula grupas līmenī neignorēs aizturēšanas kārtulu grupas līmenī. Nav jāiestata izslēgšana visos līmeņos, izņemot, kā norādīts iepriekš ar vienu pārdošanas pasūtījuma izslēgšanas kārtulas instanci. 

Kārtulas **Izmantotais kredīta** darbība tiks mainīta atkarībā no parametra **Pārbaudīt pārdošanas pasūtījuma kredīta limitu** iestatījumiem, kas atrodas veidlapā Kredīta un kolekcijas parametrs.
- Ja parametrs ir iestatīts kā Nē, tad izmantotā kredīta ierobežojuma kārtula netiks palaista.
- Ja parametrs ir iestatīts kā Jā un ja vienums **Ziņot, kad tiek pārsniegts kredīta limits** ir iestatīts uz brīdinājumu, jūs saņemsiet brīdinājumu, kad kredīta limits tik pārsniegts. Kārtulas **Izmantotais kredīta limits** tiks palaistas, lai apskatītu, vai jums ir kārtulas, ko vēlaties palaist. Tomēr, lai to izdarītu, parasti nav jāpievieno kārtulas.
- Ja parametrs ir iestatīts kā Jā un ja viens **Ziņot, kad tiek pārsniegts kredīta limits** ir iestatīts uz kļūdu, tad kredīta limits tiks pārbaudīts un pasūtījums tiks aizturēts, ja kredīta limits ir pārsniegts. Turklāt kārtulas **Izmantotais kredīta limits** tiks palaistas, lai apskatītu, vai jums ir kārtulas, kuras vēl būtu nepieciešams palaist. Kļūdas ziņojums netiks rādīts, bet tiks rādīts aizturēšanas iemesls **Pārsniegts kredīta limits**. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Iestatījumi, kas mainīs veidu, kādā pasūtījums tiek aizturēts

Pasūtījumus var izslēgt no kredīta pārvaldības, pat ja pastāv kārtulas. 

- Ja maināt vienuma **Izslēgt debitoru no kredīta pārvaldības** iestatījumu **Visi debitori > Atlasīt debitoru > Kredīta un iekasēšanas kopsavilkuma cilne** uz **Jā**, tad neviens pasūtījums šim debitoram netiks apstrādāts
- Ja maināt vērtību **Izslēgt debitoru no kredīta pārvaldības** **pārdošanas pasūtījuma galvenē** **Kredīta pārvaldības cilnē** uz **Jā**, tad kredīta pārvaldības kārtulas netiks apstrādātas. Šo iestatījumu var iestatīt tikai kredīta darbinieks vai kredīta vadītājs.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Aizturēto pasūtījumu apstrāde, izmantojot kredīta pārvaldības aizturēšanas sarakstu

Kredīta pārvaldības aizturēšanas saraksts ļauj kredīta pārvaldniekiem skatīt visus pārdošanas pasūtījumus, kas ir aizturēti, un ļauj noņemt aizturēšanu, kad kredīta problēmas ir novērstas. Lapa **Kredīta pārvaldības aizturēšanas saraksts** parāda visus aizturētos pārdošanas pasūtījumus. Jūs varat skatīt aizturēšanas sarakstu lapā **Visi kredīta aizturēšanas gadījumi** (**Kredīta pārvaldība > Kredīta pārvaldības aizturēšanas saraksts > Visi kredīta aizturēšanas gadījumi**).
Pārdošanas pasūtījumi no visām juridiskajām personām tiek nosūtīti vienam kredīta pārvaldības aizturēšanas sarakstam, sniedzot centralizētu skatījumu par visām darbībām, kurām nepieciešama uzmanība. Lietotāji redzēs informāciju tikai par tām juridiskajām personām, kurām viņiem ir pieeja.

Pārdošanas pasūtījumu var ievietot aizturēšanas sarakstā tālāk norādīto iemeslu dēļ.
1. Debitoram ir rēķins, kas ir kavēts konkrētu dienu skaitu. 
2. Pasūtījumam ir noteikts konta statuss.
3. Pasūtījumam ir konkrēti apmaksas noteikumi.
4. Debitoram ir beidzies kredīta limits.
5. Debitoram ir kavēta summa, un tas ir izmantojis noteiktu procentu no kredīta limita
6. Pārdošanas pasūtījums pārsniedz noteiktu summu.
7. Debitors ir pārsniedzis noteiktu procentuālu daļu no tā kredīta limita.
8. Apmaksas noteikumi atšķiras no debitora noklusējuma apmaksas noteikumiem.
9. Norēķinu atlaides atšķiras no noklusējuma norēķinu atlaidēm, kas attiecas uz debitoru.

Aizturēšanas sarakstā katram pārdošanas pasūtījumam tiek rādīts aizturēšanas iemesls. Ja aizturēšanai ir vairāk nekā viens iemesls, iemesls tiks rādīts kā **Vairāki**. Darbību rūtī varat izmantot izvēlni **Aizturēšanas iemesli**, lai skatītu visus iemeslus, kāpēc pārdošanas pasūtījums tika aizturēts. **Aizturēšanas iemeslus** varat skatīt arī papildinformācijā.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Tiek palaisti pasūtījumi no apstrādājamā aizturēšanas saraksta

Kad esat izskatījis aizturēšanas iemeslus un esat tos mazinājis, varat palaist pārdošanas pasūtījumus tālākai apstrādei.

1) Atlasiet rindu aizturēšanas sarakstā. Varat palaist vairākus pasūtījumus, atlasot vairāk nekā vienu rindu.
2) Atlasiet **Palaišanas iemeslu** pasūtījumam, kas ir atlasīts palaišanai.  
3) Ievadiet **Palaišanas datumu** katram pasūtījumam, kas ir atlasīts palaišanai.  
4) Atlasiet izvēlni **Palaist** darbību rūtī, lai palaistu pasūtījumu. Šī izvēlne būs pieejama tikai pēc transakciju atlases. Lietotājam tiek piedāvātas divas opcijas.
 - Atlasiet **Ar iegrāmatošanu**, lai noņemtu aizturēšanu, un grāmatojiet dokumentu, izmantojot to pašu grāmatošanas procesu, kas tika lietots, kad tas tika aizturēts. Piemēram, ja pārdošanas pasūtījuma apstiprinājums tika aizturēts, pārdošanas pasūtījuma apstiprinājums tiks pabeigts pēc palaišanas. Pārdošanas pasūtījuma grāmatošanas forma tiks parādīta, ļaujot lietotājam grāmatot apstiprinājumu.
 - Atlasiet **Bez grāmatošanas**, lai noņemtu aizturēšanu, neveicot turpmāku apstrādi. Tagad pārdošanas pasūtījumu var manuāli grāmatot.

### <a name="rejecting-orders-in-the-hold-list"></a>Pasūtījumu noraidīšana aizturēšanas sarakstā
Varat izmantot **Atteikuma** izvēlni darbības rūtī, lai noraidītu pārdošanas pasūtījumu
1. Atlasiet rindu aizturēšanas sarakstā. Varat palaist vairākus pasūtījumus, atlasot vairāk nekā vienu rindu.
2. Pasūtījums tiks noņemts no aizturēšanas saraksta un pārdošanas pasūtījuma galvene tiks atjaunināta, lai parādītu, ka pasūtījums tika noraidīts.

### <a name="automatically-releasing-credit-management-holds"></a>Automātiska kredīta pārvaldības aizturēšanas palaišana
Pārdošanas pasūtījumi tiek ievietoti aizturēšanas sarakstā, pamatojoties uz aizturēšanas kārtulām. Tomēr daži aizturēšanas iemesli var laika gaitā mainīties, ja pārdošanas pasūtījums paliek aizturēšanas sarakstā konkrētu laika periodu. Piemēram, debitors var apmaksāt savu rēķinu, atbrīvojot savu kredīta limitu. 

Varat izmantot izvēlni **Novērtēt palaišanai**, lai pārskatītu pārdošanas pasūtījumus aizturēšanas sarakstā un tos automātiski palaistu, ja aizturēšanas pamatojums ir mīkstināts.
1.  Atlasiet izvēlni **Novērtēt palaišanai**
2.  Atlasiet **Apstrādāt aizturēšanas kārtulas**, lai pārskatītu visus pārdošanas pasūtījumus. Atlasiet **Procesa aizturēšanas kārtulas atlasītajām rindām**, lai pārskatītu tikai atlasītās rindas.
3. Tiks parādīts slīdnis, lai varētu atlasīt vienu debitoru. Atstājiet debitora nolaižamo sarakstu tukšu visiem debitoriem. 
4. Kad noklikšķināt uz Labi, process tiek palaists fonā, un varat turpināt darbu ar citiem uzdevumiem. Ja atlasāt pakešveida apstrādi pirms noklikšķināt uz Labi, process tiks palaists pakešveidā, kad noklikšķināsiet uz Labi. Iespējams, būs nepieciešams ilgāks laiks, lai apstrādātu sarakstā aizturētos pasūtījumus, tāpēc izmantojiet atsvaidzināšanu, lai atjauninātu pasūtījumu statusu. 
5.  Ja aizturēšanas iemesls vairs nav piemērojam pasūtījumam, aizturēšanas iemesls tiks uzskatīts par nederīgu, un jūs vairs neredzēsiet atzīmi blakus iemeslam, skatot aizturēšanas iemeslus.
6.  Ja visi aizturēšanas iemesli ir nodzēsti, tad aizturēšanas iemeslu sarakstā tiek pievienots jauns iemesls **Gatavs palaišanai**. Tagad pārdošanas pasūtījumu var automātiski palaist.
7.  Ja parametrs **Automātiski palaist** cilnē **Kredīts un iekasēšana > Iestatījumi > Kredīta un iekasēšanas parametri > Kredīts > Automātiskā palaišana** ir iestatīts uz **Ar grāmatošanu**, jums tiks piedāvāts grāmatot, izmantojot dokumenta, kas tika bloķēts, grāmatošanas veidlapu.
8.  Ja parametrs **Automātiski palaist** cilnē **Kredīts un iekasēšana > Iestatījumi > Kredīta un iekasēšanas parametri > Kredīts > Automātiskā palaišana** ir iestatīts uz **Bez grāmatošanas**, jums jāgrāmato pasūtījums manuāli.

### <a name="credit-management-approval-workflow"></a>Kredītu pārvaldības apstiprināšanas darbplūsmas

Varat arī izveidot **Kredīta pārvaldības darbplūsmas**, lai kontrolētu kredīta aizturēšanu palaišanu. Kad esat iestatījis darbplūsmu, izmantojot lapu **Kredīta pārvaldība > Iestatījumi > Kredīta pārvaldības darbplūsmas**, pasūtījumi, kas atzīmēti palaišanai vai noraidīšanai, tiks nosūtīti uz darbplūsmu, kur tie vispirms ir jāapstiprina, pirms tie tiks palaisti vai noraidīti. 

Ja jūs iekļaujat uzdevumus palaišanai ar grāmatošanu vai palaišanai bez grāmatošanas savā darbplūsmā, arī darbplūsmas apstiprinājums palaidīs pārdošanas pasūtījumu. Tomēr, ja rodas palaišanas procesa kļūme iestatīšanas informācijas trūkuma vai citu iemeslu dēļ, jums būs jāatsauc pārdošanas pasūtījums no darbplūsmas, jānovērš problēma, kas izraisīja kļūmi, un pēc tam vēlreiz jāiesniedz pasūtījums darbplūsmai.

Ja neiekļaujat darbplūsmā uzdevumus palaišanai ar grāmatošanu vai palaišanai bez grāmatošanas , darbplūsmas apstiprināšanas process vienkārši ļaus jums nodot pārdošanas pasūtījumu manuāli, kad apstiprinājums būs pabeigts.

### <a name="forced-credit-hold"></a>Piespiedu kredīta aizturēšana  
  
Reizēm pārdošanas pasūtījumi var būt aizturēti pat tad, ja pasūtījums neatbilst aizturēšanas kārtulu kritērijiem. Piemēram, kredīta pārvaldnieks var tikt informēts par ar debitoru nesaistītu problēmu un nolemt manuāli nodot pasūtījumus aizturēšanai, līdz problēma tiek novērsta. Varat manuāli likt, lai pārdošanas pasūtījums tiek aizturēts, ja rodas šāda situācija.

1. Atveriet pārdošanas pasūtījumu, kuru vēlaties aizturēt.  
2. Atlasiet **Piespiedu kredīta aizturēšana** cilnes **Kredīta pārvaldība** darbību rūtī **Kredīta pārvaldība**.
3. Atlasiet **Piespiedu aizturēšanas iemesls**.
4. Noklikšķiniet uz **Labi**. Pārdošanas pasūtījums tiks atgriezts kredīta pārvaldības aizturēšanas sarakstā.

Varat arī piespiedu kārtā aizturēt vairākus pasūtījumus, izmantojot lapu **Kredīta pārvaldība > Periodiskie uzdevumi > Piespiedu kredīta aizturēšana**. Piemēram, varat konkrētam klientam aizturēt visus pārdošanas pasūtījumus.
1. Atlasiet **Piespiedu aizturēšanas iemesls**. 
2. Noklikšķiniet uz **Ieraksti, kas jāiekļauj**, lai atlasītu aizturētos pārdošanas pasūtījumus. 
3. Noklikšķiniet uz **LABI**, lai apstrādātu atlasītos pārdošanas pasūtījumus.

Piespiedu kārtā aizturētos pārdošanas pasūtījumus nevar apstrādāt ar darbplūsmu.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Palaižot pasūtījumus, kas tika pievienoti kredīta pārvaldības aizturēšanas sarakstam ar piespiedu kredīta aizturēšanu
Pārdošanas pasūtījumus, kas ir aizturēti piespiedu kārtā, nevar palaist automātiski. Ja pārdošanas pasūtījums tika aizturēts piespiedu kārtā un jūs esat izmantojis procesu, kas automātiski palaiž pārdošanas pasūtījumus, pārdošanas pasūtījums tiks rādīts kā **Gatavs palaišanai** un paliks aizturēšanas sarakstā. Lai palaistu pasūtījumu, jums jāizmanto izvēlne **Palaist**.
 
## <a name="free-text-invoices-retail-orders-and-project-invoice-support-in-credit-management"></a>Brīva teksta rēķini, mazumtirdzniecības pasūtījumi un projekta rēķinu atbalsts kredīta pārvaldībā 
Kredīta pārvaldību pašreiz var izmantot tikai pārdošanas pasūtījumiem. Brīva teksta rēķini, mazumtirdzniecības pārdošanas pasūtījumu punkts un zvanu centra pasūtījumi izmantos pagaidu kredīta limitus un apdrošināšanas/garantijas, kas tiek pievienotas, lai pielāgotu kredīta limitu. Tie neizmantos aizturēšanas kārtulas, un tie netiks ievietoti aizturēšanas sarakstā, ja ir problēma ar kredīta limitu.

Nav atbalsta projektu rēķiniem kredīta pārvaldībā.
