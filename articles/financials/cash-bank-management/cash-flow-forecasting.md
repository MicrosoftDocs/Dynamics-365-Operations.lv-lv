---
title: Naudas plūsmas prognozēšana
description: Šajā tēmā ir sniegts pārskats par naudas plūsmas prognozēšanas procesu. Tajā ir arī paskaidrots, kā naudas plūsmas prognozēšana ir integrēta citos sistēmas moduļos.
author: saraschi2
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 681817f2879034d65b53666a9d56ec00cc175ad8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "324495"
---
# <a name="cash-flow-forecasting"></a>Naudas plūsmas prognozēšana

[!include [banner](../includes/banner.md)]

Varat izmantot naudas plūsmas prognozēšanas rīkus gaidāmās naudas plūsmas un valūtas prasību analīzei, lai varētu noteikt uzņēmuma gaidāmās skaidras naudas vajadzības. Lai iegūtu naudas plūsmas prognozi, ir jāizpilda tālāk norādītie uzdevumi.

- Jāidentificē un uzskaita visi likviditātes konti. Likviditātes konti ir uzņēmuma konti, kas ir paredzēti skaidras naudas vai tās ekvivalentu transakcijām.
- Jākonfigurē to transakciju darbību prognozes, kas ietekmē uzņēmuma likviditātes kontus.

Kad esat pabeidzis šos uzdevumus, varat aprēķināt un analizēt naudas plūsmas prognozes un gaidāmās valūtas vajadzības.

## <a name="cash-flow-forecasting-integration"></a>Naudas plūsmas prognozēšanas integrācija

Naudas plūsmas prognozēšanu var integrēt Virsgrāmatā un moduļos Parādi kreditoriem, Debitoru parādi, Budžeta veidošana un Krājumu vadība. Prognozēšanas procesam tiek izmantota sistēmā ievadītā transakciju informācija, un aprēķina procesā tiek iegūta katras transakcijas paredzamās skaidras naudas ietekmes prognoze. Aprēķinot naudas plūsmu, tiek ņemti vērā tālāk norādītie transakciju veidi.

- **Pārdošanas pasūtījumi** — pārdošanas pasūtījumi, kas vēl nav iekļauti rēķinos un izraisa fizisku vai finansiālu pārdošanu.
- **Pirkšanas pasūtījumi** — pirkšanas pasūtījumi, kas vēl nav iekļauti rēķinos un izraisa fizisku vai finansiālu pirkšanu.
- **Debitoru parādi** — atvērtās debitoru transakcijas (vēl neapmaksātie rēķini).
- **Parādi kreditoriem** — atvērtās kreditoru transakcijas (vēl neapmaksātie rēķini).
- **Virsgrāmatas transakcijas** — transakcijas, kam ir norādīts, ka vēlāk tās tiks grāmatotas.
- **Budžeta reģistra ieraksti** — budžeta reģistra ieraksti, kas ir atlasīti naudas plūsmas prognozēm.
- **Pieprasījuma apjoma prognozes** — krājumu budžeta modeļu rindas, kas ir atlasītas naudas plūsmas prognozēm.
- **Piegādes apjoma prognozes** — krājumu budžeta modeļu rindas, kas ir atlasītas naudas plūsmas prognozēm.

Lai gan nav tiešas integrācijas modulī Projektu vadība un uzskaite, ir pieejami vairāki veidi, kā ietvert projekta transakcijas naudas plūsmas prognozē. Grāmatotie projekta rēķini tiek ietverti prognozē kā daļa no atvērtajām debitoru transakcijām. Projekta izraisītie pārdošanas un pirkšanas pasūtījumi tiek ietverti prognozē kā atvērti pasūtījumi, kad tie tiek ievadīti sistēmā. Varat arī pārsūtīt projekta prognozes uz Virsgrāmatas budžeta modeli. Pēc tam šis Virsgrāmatas budžeta modelis tiek ietverts naudas plūsmas prognozē kā daļa no budžeta reģistra ierakstiem.

## <a name="configuration"></a>Konfigurācija

Lai konfigurētu naudas plūsmas prognozēšanas procesu, izmantojiet lapu **Naudas plūsmas prognozes iestatīšana**. Šajā lapā varat norādīt izsekojamos likviditātes kontus un noklusējuma prognozēšanas darbības katrā apgabalā.

### <a name="general-ledger"></a>Virsgrāmata

Vispirms ir jādefinē likviditātes konti, kas ir jāizseko, izmantojot naudas plūsmas prognozēšanu. Parasti šie likviditātes konti ir galvenie konti, kas ir saistīti ar bankas kontiem, kuri tiks izmantoti skaidras naudas saņemšanai un izmaksai. Lapas **Naudas plūsmas prognozes iestatīšana** cilnē **Virsgrāmata** atlasiet prognozēšanā ietveramos galvenos kontus. Ja lapā **Bankas konts** galvenajam kontam ir piesaistīts bankas konts, tas tiek rādīts laukā **Bankas konts**.

Varat iestatīt pakārtotās naudas plūsmas prognozi galvenajam kontam, kura transakcijas ir tieši saistītas ar cita galvenā konta transakcijām. Atbilstoši katrai sadaļā **Pakārtotajos kontos** pievienotajai rindai pakārtotajā galvenajā kontā tiek izveidota naudas plūsmas prognozes summa. Šī summa ir daļa no naudas plūsmas summām uz atlasīto primāro galveno kontu.

Vispirms lauka **Galvenais konts** iestatiet primāro galveno kontu, kurā sākotnēji notiks transakcijas. Laukā **Pakārtotais galvenais konts** iestatiet kontu, ko ietekmēs sākotnējā transakcijas primārajā galvenajā kontā. Iestatiet atbilstošas vērtības citos rindas laukos. Varat mainīt lauka **Procenti** vērtību, lai norādītu, kādā mērā primārais galvenais konts ietekmē pakārtoto galveno kontu. Pārdošanas vai pirkšanas prognozei atlasiet lauka **Apmaksas nosacījumi** vērtību, kas parasti atbilst vairumam debitoru vai kreditoru. Laukā **Grāmatošanas tips** iestatiet paredzamo grāmatošanas tipu, kas ir saistīts ar naudas plūsmas prognozi.

### <a name="accounts-payable"></a>Kreditoru parādi

Varat aprēķināt pirkšanas prognozi, izmantojot lapas **Naudas plūsmas prognozes iestatīšana** cilnē **Parādi kreditoriem** pieejamās iestatīšanas opcijas. Lai varētu konfigurēt parādu kreditoriem naudas plūsmas prognozēšanu, vispirms ir jākonfigurē maksāšanas nosacījumi, kreditoru grupas un kreditoru grāmatošanas profili.

Sadaļā **Pirkšanas prognozes noklusējuma vērtības** varat atlasīt pirkšanas naudas plūsmas prognozēšanas noklusējuma darbības. Trīs lauki nosaka skaidras naudas ietekmes laiku: **Laika intervāls starp piegādes datumu un rēķina datumu**, **Apmaksas nosacījumi** un **Laika intervāls starp rēķinā paredzēto apmaksas datumu un maksājuma datu**. Lauka **Apmaksas nosacījumi** noklusējuma iestatījums tiek izmantots prognozēšanai tikai tad, ja transakcijai nav norādīta attiecīgā vērtība. Izmantojiet maksāšanas nosacījumu, lai norādītu, cik dienas parasti ilgst katra procesa daļa.

Laukā **Likviditātes konti maksājumiem** ir norādīts likviditātes konts, kas visbiežāk tiek izmantots maksājumiem. Izmantojiet lauku **Procenti no summas, ko piešķirt naudas plūsmas prognozei**, lai norādītu, vai prognozēšanas laikā ir jāizmanto procentuāla daļa no summām. Atstājiet šo lauku tukšu, ja prognozēšanas laikā ir jāizmanto pilnas transakciju summas.

Varat aizstāt lauka **Laika intervāls starp rēķinā paredzēto apmaksas datumu un maksājuma datumu** noklusējuma iestatījumu noteiktām kreditoru grupām. Prognozēšanai tiek izmantota sadaļā **Pirkšanas prognozes noklusējuma vērtības** norādītā noklusējuma vērtība, ja vien ar transakcijā iesaistīto kreditoru saistītajai kreditoru grupai nav norādīta cita vērtība. Lai aizstātu noklusējuma vērtību, atlasiet kreditoru grupu un pēc tam iestatiet jauno vērtību laukā **Pirkšanas laiks**.

Varat aizstāt lauka **Likviditātes konts** noklusējuma iestatījumu noteiktiem kreditoru grāmatošanas profiliem. Prognozēšanai tiek izmantota sadaļā **Pirkšanas prognozes noklusējuma vērtības** norādītā noklusējuma vērtība, ja vien ar transakcijā iesaistīto kreditoru saistītajam grāmatošanas profilam nav norādīts cits likviditātes konts. Lai aizstātu noklusējuma vērtību, atlasiet grāmatošanas profilu un pēc tam norādiet to likviditātes kontu, kas tiks ietekmēts.

### <a name="accounts-receivable"></a>Debitoru parādi

Varat aprēķināt pārdošanas prognozi, izmantojot lapas **Naudas plūsmas prognozes iestatīšana** cilnē **Debitoru parādi** pieejamās iestatīšanas opcijas. Lai varētu konfigurēt debitoru parādu naudas plūsmas prognozēšanu, vispirms ir jākonfigurē maksāšanas nosacījumi, debitoru grupas un debitoru grāmatošanas profili.

Sadaļā **Pārdošanas prognozes noklusējuma vērtības** varat atlasīt pārdošanas naudas plūsmas prognozēšanas noklusējuma darbības. Trīs lauki nosaka skaidras naudas ietekmes laiku: **Laika intervāls starp nosūtīšanas datumu un rēķina datumu**, **Apmaksas nosacījumi** un **Laika intervāls starp rēķinā paredzēto apmaksas datumu un maksājuma datu**. Lauka **Apmaksas nosacījumi** noklusējuma iestatījums tiek izmantots prognozēšanai tikai tad, ja transakcijai nav norādīta attiecīgā vērtība. Izmantojiet maksāšanas nosacījumu, lai norādītu, cik dienas parasti ilgst katra procesa daļa. 

Laukā **Likviditātes konti maksājumiem** ir norādīts likviditātes konts, kas visbiežāk tiek izmantots maksājumiem. Izmantojiet lauku **Procenti no summas, ko piešķirt naudas plūsmas prognozei**, lai norādītu, vai prognozēšanas laikā ir jāizmanto procentuāla daļa no summām. Atstājiet šo lauku tukšu, ja prognozēšanas laikā ir jāizmanto pilnas transakciju summas.

Varat aizstāt lauka **Laika intervāls starp rēķinā paredzēto apmaksas datumu un maksājuma datumu** noklusējuma iestatījumu noteiktām debitoru grupām. Prognozēšanai tiek izmantota sadaļā **Pārdošanas prognozes noklusējuma vērtības** norādītā noklusējuma vērtība, ja vien ar transakcijā iesaistīto debitoru saistītajai debitoru grupai nav norādīta cita vērtība. Lai aizstātu noklusējuma vērtību, atlasiet debitoru grupu un pēc tam iestatiet jauno vērtību laukā **Pārdošanas laiks**.

Varat aizstāt lauka **Likviditātes konts** noklusējuma iestatījumu noteiktiem debitoru grāmatošanas profiliem. Prognozēšanai tiek izmantota sadaļā **Pārdošanas prognozes noklusējuma vērtības** norādītā noklusējuma vērtība, ja vien ar transakcijā iesaistīto debitoru saistītajam grāmatošanas profilam nav norādīts cits likviditātes konts. Lai aizstātu noklusējuma vērtību, atlasiet grāmatošanas profilu un pēc tam iestatiet to likviditātes kontu, kas tiks ietekmēts.

### <a name="budgeting"></a>Budžeta veidošana

Naudas plūsmas prognozēs var ietvert budžetus, kas ir izveidoti no budžeta modeļiem. Lapas **Naudas plūsmas prognozes iestatīšana** cilnē **Budžeta veidošana** atlasiet prognozē ietveramos budžeta modeļus. Pēc budžeta modeļa iespējošanas naudas plūsmas prognozēšanai jaunie budžeta reģistra ieraksti pēc noklusējuma tiek ietveri prognozēs. Atsevišķiem budžeta reģistra ierakstiem var atcelt ietveršanu naudas plūsmas prognozēs.

### <a name="inventory-management"></a>Krājumu vadība

Naudas plūsmas prognozēs var ietvert krājumu piegādes apjoma un pieprasījuma apjoma prognozes. Lapas **Naudas plūsmas prognozes iestatīšana** cilnē **Krājumu vadība** atlasiet naudas plūsmas prognozē ietveramo budžeta modeli. Atsevišķās piegādes apjoma un pieprasījuma apjoma prognozes rindās var atcelt ietveršanu naudas plūsmas prognozēs.

### <a name="calculation"></a>Aprēķins

Lai varētu skatīt naudas plūsmas prognozēšanu, vispirms ir jāpalaiž naudas plūsmas aprēķina process. Aprēķina process nodrošina ievadīto transakciju gaidāmās skaidras naudas ietekmes prognoze.

Aprēķiniet naudas plūsmas prognozi, izmantojot lapu **Aprēķināt naudas plūsmas prognozi**. Varat aprēķināt pilnu naudas plūsmas prognozi vai inkrementālo naudas plūsmas prognozi. 

- Lai notīrītu visas naudas plūsmas prognozes transakcijas un pārrēķinātu, iestatiet lauka **Naudas plūsmas prognozes aprēķinu metode** vērtību **Kopsumma**. Ir ieteicams izmanto šo metodi, ja ilgu laiku neesat atjauninājis naudas plūsmas prognozi. 
- Lai atjauninātu esošo naudas plūsmas informāciju tikai par jaunajām transakcijām, iestatiet lauka **Naudas plūsmas prognozes aprēķina metode** vērtību **Jauns**. Lapā tiek rādīts datums, kad pēdējo reizi tika veikts naudas plūsmas aprēķins.

Naudas plūsmas prognozēšanai varat izmantot arī pakešapstrādes metodi. Lai palīdzētu nodrošināt prognozēšanas analīzes datu regulāru atjaunināšanu, iestatiet periodisku naudas plūsmas prognozes aprēķināšanas pakešapstrādes procesu.

### <a name="reporting"></a>Pārskatu veidošana

Pēc naudas plūsmas prognozes aprēķināšanas ir jāatsvaidzina saistītā analītisko pārskatu elementa informācija. Lapā **Elementu krātuve** atlasiet mēru **LedgerCovLiquidityMeasurement apkopots** un pēc tam noklikšķiniet uz **Atsvaidzināt**.

Naudas plūsmas prognozēšanas dati ir ietverti divās darbvietās. Vienā darbvietā ir ietverti dati par visiem uzņēmumiem, bet otrā darbvietā ir ietverti dati tikai par pašreizējo uzņēmumu.

Piekļuve visu uzņēmumu darbvietai tiek kontrolēta, izmantojot pienākumu **Skatīt naudas plūsmas visu uzņēmumu darbvietu**. Pēc noklusējuma darbvieta **Naudas pārskats — visi uzņēmumi** ir pieejama lietotājiem ar tālāk norādītajām lomām.

- Iestādes vadītājs
- Finanšu direktors
- Finanšu kontrolieris

Piekļuve pašreizējā uzņēmuma darbvietai tiek kontrolēta, izmantojot pienākumu **Skatīt naudas plūsmas pašreizējo uzņēmuma darbvietu**. Pēc noklusējuma darbvieta **Naudas pārskats — pašreizējais uzņēmums** ir pieejama lietotājiem ar tālāk norādītajām lomām.

- Grāmatvedis
- Uzskaites vadītājs
- Uzskaites supervizors
- Kreditoriem maksājamo parādu vadītājs
- Debitoru parādu vadītājs

Darbvietā **Naudas pārskats — visi uzņēmumi** tiek rādīti naudas plūsmas prognozēšanas analīzes dati sistēmas valūtā. Analīzei izmantoto sistēmas valūtu un sistēmas maiņas kursa tipu var definēt lapā **Sistēmas parametri**. Šajā darbvietā ir sniegts pārskats par visu uzņēmumu naudas plūsmas prognozēšanu un bankas kontu bilancēm. Skaidras naudas ieejas un izejas plūsmas diagramma sniedz pārskatu par gaidāmo naudas plūsmu un bilancēm sistēmas valūtā, kā arī detalizētu informāciju par prognozētajām transakcijām. Varat skatīt arī prognozētās bilances noteiktā valūtā.

Darbvietā **Naudas pārskats — pašreizējais uzņēmums** tiek rādīti naudas plūsmas prognozēšanas analīzes dati uzņēmumam definētajā uzskaites valūtā. Analīzei izmantoto uzskaites valūtu var definēt lapā **Virsgrāmata**. Šajā darbvietā ir sniegts pārskats par pašreizējā uzņēmuma naudas plūsmas prognozēšanu un bankas kontu bilancēm. Skaidras naudas ieejas un izejas plūsmas diagramma sniedz pārskatu par gaidāmo naudas plūsmu un bilancēm uzskaites valūtā, kā arī detalizētu informāciju par prognozētajām transakcijām. Varat skatīt arī prognozētās bilances noteiktā valūtā.

Papildinformāciju par naudas plūsmas prognozēšanas analīzi skatiet tēmā “Power BI satura pakotne Skaidras naudas apskats”.

Tālāk norādītajās lapās varat arī skatīt naudas plūsmas prognozēšanas datus par noteiktiem kontiem, pasūtījumiem un krājumiem.

- **Apgrozījuma bilance**: atlasiet opciju **Naudas plūsmas prognozes**, lai skatītu atlasītā galvenā konta gaidāmās naudas plūsmas.
- **Visi pārdošanas pasūtījumi**: cilnē **Rēķins** atlasiet opciju **Naudas plūsmas prognozes**, lai skatītu atlasītā pārdošanas pasūtījuma prognozēto skaidras naudas ietekmi.
- **Visi pirkšanas pasūtījumi**: cilnē **Rēķins** atlasiet opciju **Naudas plūsmas prognozes**, lai skatītu atlasītā pirkšanas pasūtījuma prognozēto skaidras naudas ietekmi.
- **Piegādes apjoma prognoze**: atlasiet opciju **Naudas plūsmas prognozes**, lai skatītu gaidāmās naudas plūsmas, kas ir saistītas ar atlasīto krājuma piegādes apjoma prognozi.
- **Pieprasījuma apjoma prognoze**: atlasiet opciju **Naudas plūsmas prognozes**, lai skatītu gaidāmās naudas plūsmas, kas ir saistītas ar atlasīto krājuma pieprasījuma apjoma prognozi.

