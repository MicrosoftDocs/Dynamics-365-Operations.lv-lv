---
title: Krājuma grāmatošana
description: Šī tēma skaidro cilni Krājumu grāmatošana lapā Krājumu grāmatošanas metode.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 464ffccd658003271b517038f430914fd5d8d50e
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783331"
---
# <a name="inventory-posting"></a>Krājuma grāmatošana

Cilnes **Krājumi** lapā Noliktavas grāmatošanas **metodes tiek** izmantotas, lai kontrolētu, kā krājuma darbības tiek grāmatotas Virsgrāmatā. Krājumu darbības ir darbības, kas nav izveidotas no pārdošanas pasūtījumiem, pirkšanas pasūtījumiem vai ražošanas pasūtījumiem. Tie automātiski grāmato fiziskos un finansiālos atjauninājumus krājumos vienlaicīgi. Viens izņēmums ir pārsūtīšanas pasūtījumi, kas atdala fiziskos un finansiālos atjauninājumus, kad nosūtat un saņemat krājumus.

Tabulā parādīti daži krājumu darbību piemēri.

| Darījuma veids | Ieejas vai izejas plūsma | Fiziskā grāmatošana, finanšu grāmatošana vai abi | Apraksts |
|---|---|---|---|
| Kustība | Abi | Abi | <p>Kustības žurnāls ir krājumu žurnāls, ko var izmantot krājumu pievienošanai vai noņemšanai. Tas darbojas kā krājumu korekciju žurnāls. Tomēr viena galvenā atšķirība ir tā, ka ir norādīts galvenais konts, kas korespondē ierakstu.</p><p>Kustības žurnāls ievada sākuma bilances un vienreizējus pielāgojumus, kas ir jāiekļauj izdevumos. Piemēram, tas tiek izmantots, kad krājumi tiek noņemti pārdošanas paraugs.</p><p>Kad žurnāls tiek grāmatots, fiziskie un finanšu grāmatojumi notiek vienlaicīgi.</p><p>Pozitīvi žurnāla rindu daudzumi norāda ieejas plūsmas, un negatīvie daudzumi attēlo izejas plūsmas.</p> |
| Krājumu korekcija | Abi | Abi | Krājumu korekciju žurnālu izmanto, lai pievienotu vai noņemtu krājumus. Tas neļauj atlasīt korespondējošo kontu. Virsgrāmatas ieraksta atjaunināšanai tiek izmantoti **tikai lapā Krājumu** grāmatošanas metode norādītie konti. |
| Pārsūtīšana (žurnāls) | Abi | Abi | <p>Pārsūtīšanas žurnāls tiek izmantots, lai pārvietotu krājumus no vienas vietas uz citu (izmantojot noliktavas dimensijas). Tas atjaunina preces informāciju krājuma darbībā ar jaunām preces vai izsekošanas dimensijām.</p><p>Pārsūtīšanas žurnāls izveido vienu rindu krājuma kustībai. Šai rindai ir lauki "no" un "uz" krājumu dimensijām. Katra rinda pārsūtīšanas žurnālā izveido divas krājumu darbības. Krājumu dimensijām "no" tiek izveidota viena darbība. Tā parāda izdošanu un tai ir negatīvs daudzums. Cita darbība tiek izveidota krājumu dimensijām "uz". Tas parāda saņemšanu un tam ir pozitīvs daudzums.</p><p>Pārsūtīšanas žurnāli var neveidojiet dokumentu, ja krājumu kustība tiek uzskatīta par ne-finanšu pārsūtīšanu. Krājumu dimensijas, kas atšķiras vērtībām **No** **un** Uz, nav atzīmētas ar lapā Noliktavas dimensiju grupa vai Izsekošanas dimensiju grupa opciju **Finanšu** krājumi. Piemēram, ja **·** **Atrašanās** vietas dimensijā nav atzīmēta opcija Finanšu krājumi un krājumi tiek pārvietoti no vienas atrašanās vietas uz citu vietu tajā pašā vietā un noliktavā, dokuments netiek izveidots.</p><p>Pārsūtīšanas žurnāli atšķiras no pārsūtīšanas pasūtījumiem, jo kustībai nav dokumentu. Grāmatojot žurnālu, var veikt vienas darbības atjaunināšanu. Pretēji, pārsūtīšanas pasūtījums var ģenerēt izdošanas un nosūtīšanas dokumentus, un, lai apstrādātu darbību, nepieciešami divi atjauninājumi.</p> |
| Pārsūtīšanas pasūtījuma nosūtīšanas p/z | Problēma | Abi | <p>Izveidojot jaunu pārsūtīšanas pasūtījumu, katrai rindas kombinācijai un krājumu dimensijai ir divas krājumu darbības: viena pārsūtīšanas pasūtījuma nosūtīšanai un viena pārsūtīšanas pasūtījuma saņemšanai. Kad tiek nosūtīts pārsūtīšanas pasūtījums, tiek atjauninātas divas krājumu darbības un 4 krājumu darbībām kopā tiek izveidotas divas papildu krājumu darbības tranzītā.</p><ol><li>Pirmā krājumu darbība tiek izmantota, lai izņemtu krājumu no avota noliktavas un atrašanās vietas. Šīs darbības izejas plūsmas statuss ir **Pārdots**, lai norādītu, ka krājums noliktavā vairs nav pieejams.</li><li>Otra krājuma darbība tiek izmantota, lai pievienotu krājumu tranzīta noliktavai, kas atlasīta noliktavai, no kuras krājums tiek pārsūtīts. Šīs transakcijas ieejas plūsmas statuss ir **Nopirkts**.</li><li>Trešā krājumu darbība ir pārsūtīšanai no tranzīta noliktavas uz mērķa noliktavu. Šīs darbības izejas plūsmas statuss ir Rezervēts **fiziski**. Šis statuss nodrošina, ka krājumu nevar patērēt citā procesā, kamēr tas vēl ir tranzītā.</li><li>Ceturtā krājumu darbība ir preču saņemšanai mērķa noliktavā. Šīs darbības ieejas plūsmas statuss ir **Pasūtīts**.</li></ol> |
| Pārsūtīšanas pasūtījuma saņemšanas p/z | Saņemšana | Abi | Kad pārsūtīšanas pasūtījums tiek saņemts mērķa noliktavā, krājumu darbības krājuma statuss, kas atrodas tranzīta noliktavā (iepriekšējā piemērā 3. numurs) **tiek** atjaunināts uz Pārdots, un krājumu darbības krājuma statuss mērķa noliktavā tiek atjaunināts uz **Nopirkts**. |
| Materiālu komplekti | Abi | Abi | Varat izmantot materiālu komplektu (MK) žurnālu, lai ziņotu par produktu kā pabeigtu un patērētu izejmateriālus, kas tika patērēti procesa laikā, neizmantojot ražošanas pasūtījumu. MK žurnālā parasti ir ietverta vismaz viena pozitīva rinda pabeigtai preču apstrādei, un viena vai vairākas negatīvas rindas patērētajiem izejmateriāliem. Pabeigto preču rinda ir saņemšana noliktavā, bet negatīvās rindas ir izejas plūsmas no krājumiem izejmateriāliem. Veidojot MK žurnālu, pirmā rinda ir MK virsraksts, un turpmākās rindas, kas tiek pievienotas, ir MK rindas. |
| Krājumu īpašumtiesību izmaiņas | Abi | Abi | Krājumu īpašumtiesību izmaiņu žurnāls tiek izmantots, lai mainītu no kreditora uz jūsu organizāciju nosūtīto krājumu īpašumtiesības. Krājuma īpašumtiesību izmaiņu žurnāli ir līdzīgi krājumu pārsūtīšanas žurnāliem, jo divas krājumu darbības ir saistītas ar katru rindas kombināciju un krājumu dimensiju. Viena krājumu darbība noņem krājumu **no** kreditora īpašumtiesību dimensijā, **bet otra pievieno krājumu juridiskajai personai īpašumtiesību dimensijā**. |
| Krājumu saņemšana | Saņemšana | Fizisks | Krājumu saņemšanas žurnāls tiek izmantots, lai atjauninātu krājumu saņemšanas statusu uz **Reģistrēts**. Parasti to izmanto preču pirkšanas pasūtījuma saņemšanai un pārdošanas pasūtījuma atgriešanai. |
| Ražošanas ievade | Saņemšana | Fizisks | Ražošanas ievades žurnāls ir līdzīgs krājumu saņemšanas žurnālam. Ievadītā ražošana tiek izmantota, lai noliktavā saņemtu pabeigtas preces no ražošanas pasūtījuma. Kad žurnāls ir iegrāmatots, krājumu darbības statuss tiek atjaunināts uz **Reģistrēts**. |
| Inventarizācija | Abi | Abi | Uzskaites žurnāls tiek izmantots, lai ierakstītu krājumu daudzumu, kas tika aprēķināts specifiskai krājumu dimensiju kombinācijai. Krājumu darbības tiek izveidotas, ja žurnāla rindai ir uzskaites starpība. Rinda, kurā uzskaitītais daudzums ir lielāks, izraisa ieejas plūsmu noliktavā. Rinda, kurā uzskaitītais daudzums ir mazāks, izraisa krājuma izdošanu. Rindās, kur saskaitītais daudzums sakrīt ar paredzamo daudzumu, nav krājuma darbību. |
| Etiķešu skaitīšana | Nav attiecināms | Nav attiecināms | Etiķešu inventarizācijas žurnāls tiek izmantots, lai izsekotu krājumu etiķetes, kas ir piešķirtas un izmantotas pilnai krājumu uzskaitei. Varat izmantot žurnālu, lai piešķirtu etiķetes numuru noteiktai krājuma kombinācijai un krājumu dimensijai un lai izsekotu etiķetes statusu pilnu krājumu laikā. Etiķešu inventarizācijas žurnāli neveidojiet krājumu darbības. |
| Kvalitātes pasūtījumi | Problēma | Fizisks | <p>Kvalitātes pasūtījums tiek izmantots dotās partijas testa rezultātu ierakstīšanai noliktavā. Katrs kvalitātes pasūtījums ir saistīts ar esošo krājumu darbību vai krājumu darbības daļu.</p><p>Kvalitātes pasūtījums izveidos jaunu krājumu darbību divos gadījumos:</p><ul><li>Kvalitātes pasūtījums ir atzīmēts kā **Destruktīvais** tests cilnē **Vispārīgi**.</li><li>Kvalitātes pasūtījums tiek atzīmēts kā **Karantīnā pēc** apstiprināšanas kļūmes **cilnē** Vispārīgi, un tests neizteic apstiprināšanu. Šajā gadījumā tiek izveidotas divas krājumu darbības. Viena krājuma darbība noņem krājumu no sākotnējās krājumu dimensiju kombinācijas un atrašanās vietas, bet otra pievieno krājumu karantīnas noliktavai.</li></ul> |
| Karantīnas pasūtījumi | Abi | Abi | <p>Karantīnas pasūtījumu noliktavas darbības ir kā pārsūtīšanas pasūtījums. Karantīnas noliktava tiek izmantota, lai izsekotu krājumus. Pastāv divas saņemšanas darbības un divas izejas plūsmas darbības.</p><p>Sākotnēji veidojot pasūtījumu, tiek izveidotas divas darbības. Saņemšanas darbības statuss karantīnas noliktavai **ir** pasūtīts, kas ir saistīta ar noliktavu, kurā atrodas krājums. Izejas plūsmas darbības statuss ir Pasūtīts **noliktavai**, kurā krājums tiek glabāts.</p><p>Kad karantīnas pasūtījums tiek sākts, tiek izveidotas divas papildu darbības un esošās darbības tiek atjauninātas. Karantīnas noliktavas ieejas plūsmas **darbības** statuss ir atjaunināts uz Saņemts, un noliktavas noliktavas izejas plūsmas darbības statuss tiek atjaunināts uz **Atskaitīts**.</p><p>Divas jaunās darbības tiek izmantotas, lai norādītu iespējamo kustību atpakaļ uz glabāšanas noliktavu. Saņemšanas darbības statuss ir Pasūtīts uzglabāšanas **noliktavai**, **un** šīs izdošanas darbības statuss karantīnas noliktavai ir Rezervēts fiziski.</p><p>Kad karantīnas pasūtījums tiek ziņots kā pabeigts, šī operācija parāda karantīnas pasūtījuma fizisko atjauninājumu. Saņemšanas statuss noliktavas noliktavā ir atjaunināts uz **Saņemts**.</p><p>Kad karantīnas pasūtījums tiek beigts, šī operācija ataino karantīnas pasūtījuma finansiālo atjauninājumu. Izejas plūsmas darbību statuss tiek atjaunināts uz **Pārdots**, un ieejas plūsmas darbību statuss tiek atjaunināts uz **Nopirkts**.</p><p>Alternatīvi karantīnas pasūtījumu var brāķēt. Šī operācija noņem krājumu no noliktavas. Kad karantīnas pasūtījums tiek brāķēts, paliek tikai trīs darbības. Glabāšanas noliktavas saņemšanas darbība ir noņemta, un atlikušās saņemšanas darbības statuss tiek atjaunināts uz **Nopirkts**. Divu izdošanas darbību statuss ir atjaunināts uz **Pārdots**. Šī operācija ir fizisks un finanšu atjauninājums pasūtījumam.</p> |

## <a name="fixed-receipt-price-posting"></a>Fiksētas saņemtā krājuma cenas grāmatošana

Fiksēta saņemtā krājuma cena ļauj precei izmantot standarta izmaksas. Tā ir alternatīva krājumam atlasīt **opciju** **Standarta izmaksas lapā** Krājumu modeļu grupa. Galvenā atšķirība, kad izmantojat fiksēto saņemšanas cenu, ir tā, ka izmaksu cena, kas pašreiz ir konfigurēta, tiks izmantota krājumam, kad saņemšana krājumos ir iegrāmatota. Fiksētai saņemtā krājuma cenai nav izmaksu pārvērtēšanas procesa. Grāmatojot finanšu atjauninājumu, pašreizējā izmaksu cena tiek izmantota grāmatošanas laikā. Ja izmaksu cena, kas tiek izmantota ieejas plūsmā un rēķinā, atšķiras, novirze tiks grāmatota fiksētās saņemšanas cenas peļņas un zaudējumu kontos.

Lai precei pēc izvēles lietotu fiksēto ieejas plūsmas cenu, ir jāveic šāda konfigurācija:

- Atzīmējiet **izvēles rūtiņu** Grāmatot fiziskos krājumus **lapā** Krājumu modeļu grupa krājumam, kas atlasīts krājumu darbības rindā.
- Atzīmējiet **izvēles rūtiņu Fiksētas** saņemšanas cena **krājumu modeļu grupas** lapā.
- Norādiet galvenos kontus šādiem grāmatošanas tipiem lapā **Krājumu grāmatošanas** metode:

    - Fiksētas saņemtā krājuma cenas peļņa
    - Fiksētas saņemtā krājuma cenas zaudējumi

Papildinformāciju skatiet sadaļā Fiksēta [saņemtā krājuma cena](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Pieļaujamā svara grāmatošana

Pieļaujamā svara produktus bieži izmanto tādās nozarēs kā pārtikas nozare, kur produkti nedaudz var atšķirties pēc svara, izmēra vai abos. Pieļaujamā svara preces izmanto divas mērvienības: krājumu vienība un pieļaujamā svara vienība. Krājumu svars noliktavā var atšķirties no svara, krājumu izsniedzot no noliktavas. Pieļaujamā svara preču apstrāde pielāgo krājumus.

Ja pieļaujamā svara pastāv novirze, atšķirības tiek grāmatotas kontos, **·** **·** **kas ir norādīti lapas Krājumu grāmatošanas profils laukos Pieļaujamā svara zaudējumi un Pieļaujamā svara** peļņa. Parasti viens galvenais konts tiek norādīts abos laukos.

Tālāk sniegtajā tabulā ir norādīti noklusējuma grāmatošanas tipu piemēri, un tajā ir ietverti galvenie konti un apraksti.

- "Debets/kredīts?" Kolonna norāda, vai darbība parasti ir debeta vai kredīta. Dažos gadījumos darbība var grāmatot debetus vai kredītus.
- Kolonna Tīrīšanas konts norāda, ka grāmatošanas tips ir tīrīšanas konts. Citiem vārdiem sakot, šajā kontā grāmatotā summa tiek automātiski atcelta, grāmatojot vēlāku darbību.
- Kolonna "P/F" norāda grāmatošanas tipu. "P" parāda fizisko grāmatošanu, un "F" parāda finanšu grāmatošanu.
- Kolonna "Sekot" norāda, vai galvenais konts grāmatošanas tipam parasti ir tāds pats kā galvenais konts citam grāmatošanas tipam. Tas norāda arī grāmatošanas tipu, kas parasti tiek izmantots grāmatošanai.

> [!NOTE]
> Galvenie konti un galveno kontu nosaukumi tabulā ir ieteikumi. Ieteicams strādāt ar savu grāmatvedi, lai noteiktu biznesa vajadzībām labāko konfigurāciju.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | P/F | Izpildiet | Apraksts |
|---|---|---|---|---|---|---|---|---|
| Pieļaujamā svara zaudējumu konts | 510520 | Krājumu korekcija | Izdevumi | | Nē | Abi | Pieļaujamā svara peļņas konts | Šo kontu izmanto, grāmatojot krājumu darbību, kurā pieļaujamā svara summa ir zemāka. |
| Pieļaujamā svara peļņas konts | 510520 | Krājumu korekcija | Izdevumi | | Nē | Abi | Pieļaujamā svara zaudējumu konts | Šo kontu izmanto, grāmatojot krājumu darbību, kuras pieļaujamā svara summa ir augstāka. |

Papildinformāciju par pieļaujamā svara precēm skatiet šeit: Par [pieļaujamā svara krājumiem](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) un [pieļaujamā svara preču apstrādi, izmantojot noliktavas pārvaldību](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Krājumu grāmatošana uz pamatlīdzekļu pārsūtīšanu

Krājums uz pamatlīdzekļu žurnālu (**Pamatlīdzekļu žurnāli Krājumi uz pamatlīdzekļu žurnālu) tiek izmantots, lai pārvietotu krājumus** \> **no** krājumiem un pārvērstu tos \>**pamatlīdzekļos**. Plašāku informāciju skatiet rakstā [Pamatlīdzekļu integrācija](/fixed-assets/fixed-asset-integration.md).

Tālāk sniegtajā tabulā ir norādīti noklusējuma grāmatošanas tipu piemēri, un tajā ir ietverti galvenie konti un apraksti.

- "Debets/kredīts?" Kolonna norāda, vai darbība parasti ir debeta vai kredīta. Dažos gadījumos darbība var grāmatot debetus vai kredītus.
- Kolonna Tīrīšanas konts norāda, ka grāmatošanas tips ir tīrīšanas konts. Citiem vārdiem sakot, šajā kontā grāmatotā summa tiek automātiski atcelta, grāmatojot vēlāku darbību.
- Kolonna "P/F" norāda grāmatošanas tipu. "P" parāda fizisko grāmatošanu, un "F" parāda finanšu grāmatošanu.
- Kolonna "Sekot" norāda, vai galvenais konts grāmatošanas tipam parasti ir tāds pats kā galvenais konts citam grāmatošanas tipam. Tas norāda arī grāmatošanas tipu, kas parasti tiek izmantots grāmatošanai.

> [!NOTE]
> Galvenie konti un galveno kontu nosaukumi tabulā ir ieteikumi. Ieteicams strādāt ar savu grāmatvedi, lai noteiktu biznesa vajadzībām labāko konfigurāciju.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | P/F | Izpildiet | Apraksts |
|---|---|---|---|---|---|---|---|---|
| Pamatlīdzekļa izdošana | 180100 | Materiālais pamatlīdzeklis | Līdzeklis | Kredīts | Nē | Abi | Nav attiecināms | Šo kontu izmanto, kad grāmatojat krājumu pamatlīdzekļu žurnālā, lai noņemtu krājumu no noliktavas un to pārveidotu par pamatlīdzekli. |

## <a name="moving-average-posting"></a>Pārvieto vidējo vērtību grāmatošanu

Vidējā pārvietošana ir izmaksu metode, kas balstīta uz vidējo principu. Krājumu jautājumu izmaksas nemainās laikā, kad tiek mainītas pirkšanas izmaksas. Starpība tiek kapitalizēta, pamatojoties uz proporcionālu aprēķinu. Atlikusī summa tiek iekļauta izdevumos.

Tālāk sniegtajā tabulā ir norādīti noklusējuma grāmatošanas tipu piemēri ar galvenajiem kontiem un aprakstiem.

- "Debets/kredīts?" Kolonna norāda, vai darbība parasti ir debeta vai kredīta. Dažos gadījumos darbība var grāmatot debetus vai kredītus.
- Kolonna Tīrīšanas konts norāda, ka grāmatošanas tips ir tīrīšanas konts. Citiem vārdiem sakot, šajā kontā grāmatotā summa tiek automātiski atcelta, grāmatojot vēlāku darbību.
- Kolonna "P/F" norāda grāmatošanas tipu. "P" parāda fizisko grāmatošanu, un "F" parāda finanšu grāmatošanu.
- Kolonna "Sekot" norāda, vai galvenais konts grāmatošanas tipam parasti ir tāds pats kā galvenais konts citam grāmatošanas tipam. Tas norāda arī grāmatošanas tipu, kas parasti tiek izmantots grāmatošanai.

> [!NOTE]
> Galvenie konti un galveno kontu nosaukumi tabulā ir ieteikumi. Ieteicams strādāt ar savu grāmatvedi, lai noteiktu biznesa vajadzībām labāko konfigurāciju.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | P/F | Izpildiet | Apraksts |
|---|---|---|---|---|---|---|---|---|
| Cenas atšķirība vidējās vērtības pārvietošanai | 510600 | Vidējās cenas starpības pārvietošana | Izdevumi | Abi | Nē | Abi | Nav attiecināms | Šo kontu lieto, ja izmaksas starp ieejas plūsmu un rēķinu atšķiras. |
| Pārvērtēšana vidējās vērtības pārvietošanai | 510610 | Vidējās pārvērtēšanas pārvietošana | Izdevumi | Abi | Nē | Abi | Nav attiecināms | Šo kontu izmanto, koriģējot preces pārvietošanās vidējās izmaksas |

## <a name="sample-posting-profile-configuration"></a>Grāmatošanas metodes konfigurācijas paraugs

Tālāk sniegtajā tabulā ir norādīti noklusējuma grāmatošanas tipu piemēri ar galvenajiem kontiem un aprakstiem.

| Grāmatošanas tips | Galvenā konta piemērs | Galvenā konta nosaukuma piemērs | Konta veids | Vai debets/kredīts? | Dzēšanas konts | P/F | Izpildiet | Apraksts |
|---|---|---|---|---|---|---|---|---|
| Krājumu izejas plūsma | 140100 | Materiālu krājumi | Līdzeklis | Kredīts | Nē | Abi | Krājumu ieejas plūsma | Šis konts tiek izmantots, kad grāmatotā krājumu darbība ir izejas plūsma (negatīvs daudzums) un nav saistīta ar pārdošanu, pirkšanu vai ražošanu. Korespondējošais konts ir krājumu izdevumu, zaudējumu konts. Šis konts parasti bilancē parāda krājumus. |
| Krājumu izdevumi, zaudējumi | 510100 | Krājumu peļņa un zaudējumi | Izdevumi | Debets | Nē | Abi | Krājumu izdevumi, ieņēmumi | Šis konts tiek izmantots, kad grāmatotā krājumu darbība ir izejas plūsma (negatīvs daudzums) un nav saistīta ar pārdošanu, pirkšanu vai ražošanu. Korespondējošais konts šajā kontā ir krājumu izejas plūsmas konts. |
| Krājumu ieejas plūsma | 140100 | Materiālu krājumi | Līdzeklis | Debets | Nē | Abi | Krājumu izejas plūsma | Šis konts tiek izmantots, kad iegrāmatotā krājumu darbība ir ieejas plūsma (pozitīvs daudzums) un nav saistīta ar pārdošanu, pirkšanu vai ražošanu. Korespondējošais konts ir krājumu izdevumu, peļņas konts. Šis konts parasti bilancē parāda krājumus. |
| Krājumu izdevumi, ieņēmumi | 510100 | Krājumu peļņa un zaudējumi | Izdevumi | Kredīts | Nē | Abi | Krājumu izdevumi, zaudējumi | Šis konts tiek izmantots, kad iegrāmatotā krājumu darbība ir ieejas plūsma (pozitīvs daudzums) un nav saistīta ar pārdošanu, pirkšanu vai ražošanu. Korespondējošais konts šajā kontā ir krājumu ieejas plūsmas konts. |
| Starpvienību kreditors | 231500 | Starpvienumu kreditors | Saistības | Debets | Nē | Abi | | Šo kontu izmanto, kad krājumi tiek pārsūtīti starp krājumu dimensijām, piemēram, vietām, un krājuma izmaksas dažādās vietās atšķiras. |
| Starpvienību debitors | 131500 | Starpvienumu debitori | Līdzeklis | Kredīts | Nē | Abi | | Šo kontu izmanto, kad krājumi tiek pārsūtīti starp krājumu dimensijām, piemēram, vietām, un krājuma izmaksas dažādās vietās atšķiras. |
