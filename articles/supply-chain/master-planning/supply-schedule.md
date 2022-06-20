---
title: Piegādes grafiks
description: Šajā rakstā ir sniegta informācija par Piegādes grafika lapu un tās iespējām.
author: t-benebo
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0e3937dd4cffc464f38b5770674364579bdb06d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851744"
---
# <a name="supply-schedule"></a>Piegādes grafiks

[!include [banner](../includes/banner.md)]

Lapā **Piegādes grafiks** tiek rādīts visaptverošs piegādes un pieprasījuma pārskats attiecībā uz produktu vai produktu saimi. Informācija tiek filtrēta pēc atrašanās vietas, galvenā plāna un periodiem. Varat šo lapu arī izmantot, lai izveidotu jaunus pasūtījumus, pārveidotu esošos plānotos pasūtījumus un palaistu galveno plānošanu.

## <a name="open-the-supply-schedule-page"></a>Atveriet Piegādes plānošanas lapu

Jūs varat atvērt lapu **Piegādes plānošana** jebkurā no šiem veidiem:

- Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Piegādes plānošana**. Dialoglodziņā **Pārveidot filtru** norādiet plānu un preci, kuru meklējat, nodrošinātajos laukos ievadot filtra vērtības. (Pārējā rakstā ievadīto filtru vērtību kolekcija tiek saukta par "filtru" vai "pašreizējais filtrs". Kad esat beidzis, atlasiet **Labi**.
- Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**. Atlasiet vai atveriet preci. Pēc tam darbību rūts cilnē **Plāns** grupā **Skatīt** atlasiet **Piegādes plānošana**.
- Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Pieprasījuma prognozēšana \> Krājumu sadalījuma principi**. Atlasiet krājuma sadalījuma principu, kas tiek izmantots kā preču saime. Darbību rūtī atlasiet **Piegādes plānošana**.
- Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Plānotie pasūtījumi**. Atlasiet vai atveriet plānoto pasūtījumu. Pēc tam darbību rūts cilnē **Skatīt** grupā **Skatīt** atlasiet **Piegādes plānošana**.

> [!NOTE]
> Atverot **Piegādes plānošanas** lapu no preces, preču saimes vai plānotā pasūtījuma, nav jāievada filtra vērtības. Sistēma izmantos noklusējuma perioda veidni.

## <a name="use-the-supply-schedule-page"></a>Lietojiet Piegādes plānošanas lapu

Lapa **Piegādes plānošana** sastāv no augšējās sadaļas, kopsavilkuma cilnes **Perioda beigu krājums**, papildu kopsavilkuma cilnes, kura kļūst redzama, pamatojoties rindā, kura tiek atlasīta augšējā sadaļā, un notikumu rūtī. (Lai atvērtu notikumu rūti un skatītu notikumu, labajā lapas malā atlasiet **Saistītā informācija**.)

### <a name="upper-section"></a>Augšējā sadaļa

Lapas **Piegādes plānošana** augšējā sadaļā ir režģis, kurā parādīti šādi preces vai preču saimes dati. Šie dati tiek sadalīti pa periodiem, kuri ir definēti **Perioda veidnes** vērtībā no filtra.

- **Perioda sākuma krājums** — Šī rinda parāda paredzamo krājuma bilanci perioda sākumā, ja notiek visi pasūtījumi sistēmā.
- **Perioda beigu krājums** — Šī rinda parāda paredzamo krājuma bilanci perioda beigās, ja notiek visi pasūtījumi sistēmā.
- **Perioda beigu piesaistītais krājums** — Šī rinda parāda paredzamo krājuma summu perioda beigās, kas tiek piesaistīts pret pieprasījumu nākotnē.
- **Perioda neto piegāde** — Šajā rindā parādīta atšķirība starp piegādi un pieprasījumu periodā.
- **Minimālais krājums** — Šis mezgls rāda drošības krājumu precei vai preču saimei. Lai izvērstu vai sakļautu šo mezglu, atlasiet to un pēc tam rīkjoslā atlasiet **Izvērst** vai **Sakļaut**. Šis mezgls tiek rādīts tikai tad, ja precei vai preču saimei ir drošības krājums.
- **Pieprasījums** — Šis mezgls rāda preces vai preču saimes pieprasījumu. Pieprasījums tiek grupēts pēc transakcijas veida. Lai izvērstu vai sakļautu šo mezglu, atlasiet to un pēc tam rīkjoslā atlasiet **Izvērst** vai **Sakļaut**. Pieprasījuma transakciju veidi ietver pārdošanu, pārsūtīšanu un krājuma žurnālus. Šis mezgls tiek rādīts tikai tad, ja precei vai preču saimei ir pieprasījums.
- **Piegāde** — Šis mezgls rāda preces vai preču saimes piegādi. Piegāde tiek grupēta pēc transakcijas veida. Lai izvērstu vai sakļautu šo mezglu, atlasiet to un pēc tam rīkjoslā atlasiet **Izvērst** vai **Sakļaut**. Piegādes transakciju veidi ietver ražošanu, iegādi un pārsūtīšanu. Šis mezgls tiek rādīts tikai tad, ja precei vai preču saimei ir piegāde.

Daudzas no pieejamajām rīkjoslas pogām, notikumu displeji un kopsavilkuma ciļņu displeji ir atkarīgi no jūsu veiktajām izvēlēm augšdaļā. Parasti jūs izvēlētos transakcijas veidu, atlasot vienu no rindām no mezgla **Piegāde** vai **Pieprasījums**. Pēc tam jūs izvēlētos periodu, atlasītajai rindai atlasot konkrētu kolonnu.

Lapas **Piegādes plānošana** augšējā sadaļā, rīkjoslā virs režģa ir šādas pogas:

- **Izvērst / Sakļaut** — Izvērsiet vai sakļaujiet atlasīto mezglu, piemēram mezglu **Pieprasījums** vai **Piegāde** un to apakšmezglus. (Mezgli rāda prefiksu **\[+\]** vai **\[-\]**, lai norādītu, vai tie pašlaik ir sakļauti vai izvērsti.)
- **Jauns** — Atver izvēlni, kurā katra komanda atver dialoglodziņu vai lapu, kura ļauj pievienot konkrētu atlases elementa veidu. Pieejamās komandas ietver **Prognozēt piegādi**, **Plānotais pasūtījums**, **Plānotais kanban**, **Jauns ražošanas pasūtījums**, **Pirkuma pasūtījums** un **Pārsūtīšanas pasūtījums**.
- **Vispārējā plānošana** — Palaiž vispārējo plānošanu. Tiek parādīts dialoglodziņš, kurā varat norādīt, kuru plānu palaist. Lauks **Vispārējais plāns** pēc noklusējuma tiek iestatīts tā, lai tas atbilstu pašreizējam filtram.
- **Maks. ziņot par pabeigtu** — Atver lapu **Max. ziņot par pabeigtu** precei, kura ir definēta pašreizējā filtrā.
- **Atjaunināt plānotos pasūtījumus** — Atver lapu **Plānotie pasūtījumi**, kurā tiek rādīti plānotie pasūtījumi precei vai preču saimei, kas ir definēta pašreizējā filtrā.
- **Līmenis** — Izklāj plānotos pasūtījumus atbilstoši iestatījumiem no dialoglodziņa, kas tiek parādīts.
- **Materiālu plāns pēc vietas** — Atver lapu **Krājumu segums** precei, kura ir definēta pašreizējā filtrā.
- **Kanban kārtula** — Atver lapu **Kanban kārtulas** precei, kura ir definēta pašreizējā filtrā.

### <a name="fasttabs"></a>Kopsavilkuma cilnes

Lapa **Piegādes plānošana** var saturēt šādas kopsavilkuma cilnes:

- **Perioda beigu krājums** — Šajā kopsavilkuma cilnē parādīti perioda beigu krājuma dati grafiskā formātā.
- **Piegādes profils** — Šajā kopsavilkuma cilnē parādīti piegādes dati grafiskā formātā. Tie kļūst redzami, ja augšdaļā atlasāt **Piegādes** mezglu vai rindu zem tā.
- **Kopsavilkums** — Šī kopsavilkma cilne rāda kopsavilkuma informāciju, kura ir saistīta ar transakcijas veidu, kuru atlasījāt augšdaļā. Piemēram, ja mezglā **Pieprasījums** atlasāt **Pārdošana**, šī kopsavilkuma cilne rāda laukus, kuri ir saistīti ar pārdošanas pasūtījumiem, piemēram, **Pieprasītās pārdošanas pasūtījumu rindas** vai **Kopsumma**. Ja **Piegādes** mezgla apakšmezglā **Ražošana** atlasāt **Ražošanas pasūtījumi**, šī kopsavilkuma cilne rāda laukus, kuri ir saistīti ar ražošanas pasūtījumiem, piemēram, **Plānotie ražošanas pasūtījumi** vai **Plānotā kopsumma**. Lauku vērtība ir atkarīgas no perioda, kuru atlasījāt augšdaļā. 
- **\[Transakcijas veids\] - \[Periods\]** — Šī kopsavilkuma cilne rāda pasūtījumus transakcijas veidam un periodam, kuru atlasījāt augšdaļā. Kopsavilkuma cilnes nosaukums parāda šo atlasi. Piemēram, tās nosaukums varētu būt **Pārdošanas pasūtījumi — nepabeigtie darbi** vai **Ražošanas pasūtījumi — 37. nedēļa**.

### <a name="action-pane"></a>Darbības rūts

Darbību rūtī ir pieejamas tālāk minētās pogas:

- **Pārveidot filtru** — Atveriet dialoglodziņu **Pārveidot filtru**, kurā varat atjaunināt filtra vērtības, un pēc tam no jauna atveriet lapu **Piegādes plānošana**, kurā parādīti atjauninātie filtra iestatījumi.
- **Rādīt kavēšanos** — Izceļ atbilstošās rindas augšējā sadaļā, ja šā veida transakcijai ir kavēts pasūtījums.

### <a name="factbox-pane"></a>Notikuma rūts

Lai atvērtu notikumu rūti un skatītu notikumu, labajā lapas malā atlasiet **Saistītā informācija**. **Piegādes plānošanas** lapā ir pieejami šādi notikumi:

- **Krājuma informācija** — Šis notikums rāda pamata informāciju par preci, kas ir definēta pašreizējā filtrā. Tas ir tukšs, ja filtrā definējat preču saimi.
- **Darbības** — Šis notikums rāda darbības pasūtījumiem no transakcijas veida, kuru atlasījāt augšējā sadaļā.
- **Kavēšanās** — Šis notikums rāda kavēšanos pasūtījumiem no transakcijas veida, kuru atlasījāt augšējā sadaļā.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
