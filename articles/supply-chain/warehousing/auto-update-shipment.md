---
title: Sūtījuma automātiskie atjauninājumi
description: Šī tēma sniedz apskatu par funkcionalitāti, kas nodrošina automātisku sūtījumu atjaunināšanu.
author: Mirzaab
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable,SalesTableListPage,SalesTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3402a4c90299cf52e489e85ed55aff9762796545
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580100"
---
# <a name="shipment-auto-updates"></a>Sūtījuma automātiskie atjauninājumi

[!include [banner](../includes/banner.md)]

Automātiskās atjaunināšanas piegādes funkcionalitāte automātiski atjaunina daudzumus (gan palielinājumus, gan samazinājumus) kravas līnijā, kas saistīta ar kravu, pēc tam, kad krava ir nodota noliktavai. Šī funkcionalitāte paliek ieslēgta, kamēr kravas līnija vai krava tiek apstrādāta kopumā. Kad tas tiek izmantots, pasūtījuma atjauninājumi var automātiski plūst uz noliktavu, neveicot manuālu iejaukšanos, līdz tiek veikti noliktavas darbi.

Kad automātiskās atjaunošanas sūtījuma funkcionalitāte netiek izmantota, tikai kvantitāte samazinās automātiskā plūsmā, līdz tiek izveidots noliktavas darbs. Lietotājiem ir manuāli jāatjaunina vai jādzēš rindas, un tad atkārtoti jāaizpilda rindas, ja pasūtījuma daudzums ir palielināts vai tiek pievienotas jaunas pasūtījuma rindas. Izmantojot automātiskās atjaunināšanas sūtījuma funkcionalitāti, uzņēmumi var bez raizēm sniegt atjauninājumus noliktavai, neuztraucoties, ka ar to saistītie sūtījumi un kravas neatspoguļo pasūtījumu rindas atjauninājumus.

Automātiskās atjaunināšanas sūtījuma funkcionalitāte attiecas uz pārdošanas pasūtījuma rindām un pārsūtīšanas pasūtījuma rindām, un tā ir ieslēgta konkrētai noliktavai. Tāpēc uzņēmumi pēc nepieciešamības var piemērot dažādas automātiskās atjaunināšanas sūtījumu ierobežojumus noliktavās. Pēc noklusējuma automātiskās atjaunināšanas sūtījuma ierobežojumu daudzuma samazinājumam piemēro visām noliktavām, kas izmanto noliktavas pārvaldības procesus. Kad šis noklusējuma politikas iestatījums tiek izmantots, tikai daudzuma samazināšanās automātiski tiek veikta sūtījumam un kravai līdz tiek veikti noliktavas darbi. Šī uzvedība līdzinās uzvedībai, kas tika izmantota pirms automātiskās atjaunināšanas sūtījumu funkcionalitātes ieviešanas.

## <a name="main-elements-of-the-functionality"></a>Funkcionalitātes galvenie elementi

Automātiskās atjaunināšanas sūtījuma funkcionalitāte galvenokārt balstās uz sūtījuma statusu, lai noteiktu, vai kravas līnijas daudzums ir jāmaina, kad pārdošanas pasūtījuma rindā vai pārsūtīšanas pasūtījuma rindā tiek veiktas izmaiņas. Tā arī galvenokārt paļaujas uz sūtījuma statusu, lai noteiktu, kad esošai noslodzei automātiski jāpievieno jauna kravas rinda. Kad sūtījuma statuss ir **Nokomplektēts** vai lielāks, netiek veikta automātiskā atjaunināšana.

Kopuma statuss ir paredzēts arī automātiskajiem atjauninājumiem. Kad kopums, kas saistīts ar kravas rindu, ir ar statusu **Aizturēts**, **Realizācijā**, **Nodots**, **Izvēlēts** vai **Nosūtīts**, ja lietotājs mēģina samazināt daudzumu noslodzes rindā (izmantojot pārdošanas pasūtījuma rindas vai pārsūtīšanas pasūtījuma rindas daudzuma samazināšanu), tiek parādīts šāds kļūdas ziņojums: "Rezervācijas nevar noņemt, jo ir izveidots darbs, kas balstās uz rezervāciju." Turklāt, kad kopums ir viens no iepriekš minētajiem kopuma statusiem, ja lietotājs mēģina netieši palielināt kravas rindas daudzumu, palielinot daudzumu pārdošanas pasūtījuma rindā vai pārsūtīšanas pasūtījuma rindā, daudzums kravas rindā netiek automātiski palielināts. Šādā gadījumā kravas rinda ir jāatjaunina manuāli.

## <a name="scenarios"></a>Scenāriji

Automātiskās atjaunināšanas sūtījuma funkcionalitāte atbalsta četrus scenārijus: jaunas pasūtījuma rindas pievienošana, daudzuma palielināšana pasūtījuma rindā, daudzuma samazināšana pasūtījuma rindā un pasūtījuma rindas noņemšana.

- **Pievienot jaunu pasūtījuma rindu** – Kad **Automātiskās atjaunināšanas nosūtīšanas** lauks **Noliktavas** lapas **Noliktavas** kopsavilkuma cilnē (**Noliktavas pārvaldība \> Iestatīšana \> Noliktava \> Noliktavas**) ir iestatīts uz **Vienmēr**, ja pasūtījumam ir krava un jauna pasūtījuma rinda tiek pievienota pārdošanas pasūtījumam vai pārsūtīšanas pasūtījumam, pēc tam, kad noslodze jau ir izveidota pārdošanas pasūtījumam, esošā noslodze netiek atjaunināta. Jauna kravas rinda, kurai nav atsauces uz esošo noslodzi, tiek izveidota un saistīta ar esošo sūtījumu. Jaunā rinda tiek pievienota noslodzei un palaista.
- **Palielināt daudzumu pasūtījuma rindā** — Kad **Automātiskās atjaunināšanas sūtījuma** lauks ir iestatīts uz **Vienmēr**, ja pasūtījumam ir krava un daudzums esošā pārdošanas pasūtījuma rindā vai pārsūtīšanas pasūtījuma rindā ir palielināts, pēc tam, kad pārdošanas pasūtījumam jau ir izveidota noslodze, tās rinda tiek palielināta par tādu pašu daudzumu kā pasūtījuma rinda. Ja noslodze tika nodota, bet netika izveidots neviens darbs, noslodzes rinda tiek palielināta par tādu pašu daudzumu kā pasūtījuma rinda.
- **Samazināt daudzumu pasūtījuma rindā** — kad **Automātiskās atjaunināšanas sutījuma** lauks ir iestatīts uz **Vienmēr** vai **Uz daudzuma samazināšanos**, ja pasūtījumam ir paredzēts sūtīšana un daudzums esošā pārdošanas pasūtījuma rindas vai pārsūtīšanas pasūtījuma rinda tiek samazināta pēc tam, kad noslodze jau ir izveidota pārdošanas pasūtījumam, daudzums saistītajā noslodzes rindā tiek atjaunināts atbilstoši, ja vien daudzums šajā kravas rindā jau ir vienāds ar vai mazāks par jauno daudzumu pasūtījuma rindā. Šādā gadījumā noslodzes rinda netiek ietekmēta. Ja krava tika nodota, bet netika izveidots neviens darbs, daudzums saistītajā noslodzes rindā tiek atjaunināts atbilstoši, ja vien daudzums noslodzes rindā jau ir vienāds ar vai mazāks nekā jaunais daudzums pasūtījuma rindā. Šādā gadījumā noslodzes rinda tiek ietekmēta.
- **Noņemt pasūtījuma rindu** — Kad **Automātiskās atjaunināšanas sūtījuma** lauks ir iestatīts uz **Vienmēr** vai **Uz daudzuma samazināšanos**, ja lietotājs mēģina noņemt pasūtījuma rindu, kurā pastāv kravas rinda, tiek parādīts kļūdas ziņojums.

## <a name="example-scenario"></a>Piemēra situācija

Šim scenārijam ir jābūt instalētiem demo datiem, un jums ir jāizmanto **USMF** demo datu uzņēmums.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Ieslēgt automātiskās atjaunināšanas sūtījuma funkcionalitāti

Lai ieslēgtu automātiskās atjaunināšanas sūtījuma funkcionalitāti, veiciet sekojošās darbības.

1. Dodieties uz **Noliktavas vadība \> Iestatīšana \> Noliktava \> Noliktavas**.
2. Atlasiet noliktavu **24**.
3. Uz **Noliktavas** kopsavilkuma cilnes, **Automātiski atjaunināt sūtījumu** laukā mainiet vērtību no **Uz daudzuma samazināšanās** uz **Vienmēr**.

Kad vērtība ir mainīta uz **Vienmēr**, jebkuras pārdošanas pasūtījuma rindu un pārsūtīšanas pasūtījumu rindu daudzumu palielināšanās vai samazināšanās un visi jauno rindu papildinājumi tiek atspoguļoti sūtījumos un noslodzēm atlasītajā noliktavā, ņemot vērā iepriekš minētos atjaunināšanas ierobežojumus.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Mainiet kopuma veidni, lai kravas rindas netiktu automātiski apstrādātas.

Lai konfigurētu kopuma veidni tā, ka tā automātiski neapstrādā noslodzes rindas, veiciet sekojošās darbības.

1. Dodieties uz **Noliktavas vadība \> Iestatīšana \> Kopumi \> Kopuma veidnes**.
2. Iestatiet kopuma veidni **24 Sūtījums pēc noklusējuma**.
3. Atlasiet **Rediģēt**.
4. **Vispārīgi** kopsavilkuma cilnē iestatiet **Automatizēt kopuma izveides** opciju uz **Jā** un pārliecinieties, ka pārējās opcijas ir iestatītas uz **Nē**.

Ir svarīgi, lai neviens darbs netiek automātiski izveidots un nodots kā daļa no kopuma izveides procesa. Pēc darba izveides, kas saistīts ar noslodzes rindu un kas tika izveidota pārdošanas pasūtījuma rindai, noslodzes rinda vairs netiek automātiski atjaunināta, ja pārdošanas pasūtījuma rindā esošais daudzums tiek mainīts.

### <a name="create-a-sales-order"></a>Izveidot pārdošanas pasūtījumu

Lai izveidotu pārdošanas pasūtījumu, veiciet sekojošās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
2. Atlasiet klientu **US-003**.
3. Izveidojiet rindu krājuma kodam **A0001**.
4. Ievadiet daudzumu **10**. (Pārliecinieties, ka izmantojat noliktavu **24**.)
5. Atlasiet **Saglabāt**.
6. Darbību rūtī cilnē **Noliktava**, kas atrodas grupā **Darbības**, atlasiet **Nodot izpildei noliktavā**. Tiek izveidots sūtījums un kopums.

Tā kā iepriekš tika mainīta kopuma veidne, noslodze vai darbs netiek izveidots. Kravas statuss ir **Atvērts**, un kopuma statuss ir **Izveidots**.

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Samazināt pārdošanas pasūtījuma daudzumu.

Lai samazinātu pārdošanas pasūtījuma rindas daudzumu, veiciet sekojošās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
2. Atlasiet pārdošanas pasūtījumu, kuru tikko izlaidāt noliktavā.
3. Atlasiet pārdošanas pasūtījuma rindu. Laukā **Daudzums** mainiet vērtību no **10** uz **8**.
4. No pārdošanas pasūtījuma rindas atlasiet **Noliktavas \> Sūtījuma detaļas** Lapā **Sūtījuma detaļas** **Noslodzes rindas** kopsavilkuma cilnē daudzums ataino izmaiņas pārdošanas pasūtījuma rindā.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Palielināt pārdošanas pasūtījuma rindas daudzumu.

Lai palielinātu pārdošanas pasūtījuma rindas daudzumu, veiciet sekojošās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
2. Atlasiet pārdošanas pasūtījumu, kuru iepriekš izlaidāt noliktavā.
3. Mainīt rindas daudzumu no **8** uz **12**.
4. Atlasiet **Saglabāt**.
5. Atgriezieties lapā **Visi pārdošanas pasūtījumi** un vēlreiz atlasiet pārdošanas pasūtījumu.
5. Darbību rūtī cilnē **Noliktavas** grupā **Saistīta informācija** atlasiet **Sūtījuma detaļas**. Lapā **Sūtījuma detaļas** **Noslodzes rindas** kopsavilkuma cilnē daudzums ataino izmaiņas pārdošanas pasūtījuma rindā.

Lai arī daudzums noslodzes rindā ir palielināts no 8 līdz 12, tikai astoņi krājumi paliek rezervēti, ja vien nav ieslēgta automātiska rezervācija. Tā kā daudzums, kas tika pievienots esošajai kravai, nav rezervēts, ja kopums tiek apstrādāts šajā vietā bez rezervēšanas, darbs tiek izveidots tikai daudzumam, kas jau ir rezervēts.

> [!NOTE]
> Kad daudzums pasūtījuma rindā tiek samazināts, daudzums noslodzes rindā netiek ietekmēts, ja tas jau ir vienāds vai mazāks nekā jaunais daudzums pasūtījuma rindā. Kad daudzums pasūtījuma rindā ir palielināts, noslodzes rinda tiek palielināta par tādu pašu daudzumu kā pasūtījuma rinda. Ja daudzums pasūtījuma rindā atšķiras no daudzuma noslodzes rindā, starpība paliek.

### <a name="add-a-sales-order-line"></a>Pievienojiet pārdošanas pasūtījuma rindu.

Lai pievienotu pārdošanas pasūtījuma rindu, veiciet sekojošās darbības.

1. Dodieties uz **Pārdošana un mārketings \> Pārdošanas pasūtījumi \> Visi pārdošanas pasūtījumi**.
2. Atlasiet pārdošanas pasūtījumu, kuru iepriekš izlaidāt noliktavā.
3. Izveidojiet rindu krājuma kodam **A0002**.
4. Laukā **Daudzums** ievadiet **10**. (Pārliecinieties, ka izmantojat noliktavu **24**.) Jaunā rinda tiek automātiski pievienota esošajam sūtījumam.
5. Atlasiet **Saglabāt**.
6. Atgriezieties lapā **Visi pārdošanas pasūtījumi** un vēlreiz atlasiet pārdošanas pasūtījumu.
7. Darbību rūtī cilnē **Noliktavas** grupā **Saistīta informācija** atlasiet **Sūtījuma detaļas**. Lapā **Sūtījuma detaļas** **Noslodzes rindas** kopsavilkuma cilnē ievērojiet otro noslodzes rindu.

Tā kā pārdošanas pasūtījuma rinda, ko tikko pievienojāt esošajam sūtījumam, nav rezervēta, ja kopums tiek apstrādāts šajā brīdī, darbs tiek izveidots tikai daudzumam pirmajā pārdošanas pasūtījuma rindā un pirmajā noslodzes rindā.

### <a name="process-a-wave"></a>Apstrādāt kopumu

Lai apstrādātu kopumu, veiciet sekojošās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Izejošie kopumi \> Sūtījuma kopumi \> Visi kopumi**.
2. Atlasiet iepriekš izveidoto kopumu.
3. Darbību rūts cilnē **Kopums**, grupā **Kopums** atlasiet **Apstrādāt**.

Kopums ir apstrādāts un izveido darbu rezervētajiem daudzumiem noslodzes rindās. Sūtījuma statuss tiek atjaunināts no **Atvērts** uz **Nokomplektēts**. Tā kā sūtījuma statuss tiek atjaunināts uz **Nokomplektēts**, jebkādas izmaiņas, kas rodas, piemēram, samazinājumi vai palielinājumi rindu daudzumos vai jaunu rindu pievienošana pārdošanas pasūtījumam, neietekmē esošās noslodzes rindas, kas saistītas ar nokomplektēto sūtījumu.

Ja sūtījuma statuss ir **Nokomplektēts** vai augstāks, pārdošanas pasūtījuma rindas daudzuma izmaiņas netiek atainotas vai validētas attiecībā pret noslodzes rindu, kas saistīta ar sūtījumu. Noslodzes rindas daudzuma izmaiņas jāveic tieši noslodzes rindā.

Apstiprināšana tiek veikta pēc tam, kad darbs ir izveidots noslodzes rindai un ir veikta rezervācija. Pārdošanas pasūtījuma rindas daudzuma samazinājums pēc tam tiek validēts attiecībā pret darba rindas rezervāciju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]