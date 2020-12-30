---
title: Grāmatoto nomas darījumu atsaukšana
description: Šajā tēmā skaidrots, kā atsaukt grāmatotos nomas darījumus. Jebkuru darījumu, kas tiek izveidots, izmantojot līdzekļu nomu, var atsaukt.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 259fd8f41eade1e873225f0d95c499c8cb8c1a6a
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445790"
---
# <a name="reverse-posted-lease-transactions"></a>Grāmatoto nomas darījumu atsaukšana

[!include [banner](../includes/banner.md)]

Jebkuru darījumu, kas tiek izveidots, izmantojot līdzekļu nomu, var atsaukt. Darījumi, kas tiek atsaukti, izmantojot līdzekļu nomu, atjaunina jūsu nomas datus. Tāpēc tās atjaunina arī nomas saistību un LLT uzskaites vērtības.

Lai izveidotu nomas atsaukšanas darījumu, rīkojieties šādi.

1. Lapā **Līdzekļu darījumi** vai **Saistību darījumi** atlasiet darījumu un pēc tam atlasiet **Atsaukt darījumu**.
2. Parādītajā dialoglodziņā varat labot datumu, kad tiks grāmatots atsaukšanas ieraksts. Pēc noklusējuma lauks **Datums** ir iestatīts uz darījuma grāmatošanas datumu atlasītajam darījumam. Atsaukšanas ierakstu nevar grāmatot agrāk par atlasītā darījuma oriģinālo grāmatošanas datumu.
3. Atlasiet **Labi**. Tiek grāmatots žurnāla ieraksts, kas atceļ atlasīto ierakstu. Atcelšana tiek rādīta lapā **Līdzekļu darījumi** vai **Saistību darījumi**, un tiek atjaunināta pašreizējās bilances neto kopsumma, kas tiek rādīta lapā.

Atlasot **Atsaukšanas izsekošana**, parādās dialoglodziņš, kas rāda gan sākotnējos darījumus, gan atsauktos darījumus kopā ar saistīto numuru, kas tiek saukts par *izsekošanas numuru*. Lai atvieglotu atsaukšanas izpratni un uzlabotu redzamību, varat arī izsekot atsaukšanas, izmantojot nomas grafikus.

Lauks **Pēdējais žurnāla numurs** lapā **Grafiks** rāda darījumu žurnāla numurus. Kad darbība ir atsaukta, šis lauks tiek atjaunināts ar atsaukšanas darījuma žurnāla numuru. Turklāt tiek atzīmēta izvēles rūtiņa **Atsaukts**, lai norādītu, ka darījums ir atsaukts, un ir atlasīts lauks **Grāmatots**.

## <a name="revoke-a-reversed-transaction"></a>Anulētas darījuma atsaukšana

Lai atsauktu anulētu darījumu, veiciet šādas darbības.

1. Lapā **Grafiks** vai **Darījumi** atlasiet sākotnējo darījumu.
2. Izpildiet kādu no norādītajām transakcijām.

    - Ja atlasījāt darījumu lapā **Grafiks**, sekojiet žurnāla izveides darbībām sadaļā [Ikmēneša žurnāla ierakstu izveide partijā](create-monthly-journals-batch.md). Žurnāls ir manuāli jāgrāmato.
    - Ja atlasījāt darījumu lapā **Darījumi**, atlasiet **Atsaukt darījumu**. Tiek parādīts ziņojums, ka šī atsaukšana ir iepriekšējās anulēšanas atsaukšana, un jūs varat rediģēt grāmatošanas datumu šai atsaukšanai. Tomēr vispārējās biznesa pārbaudes ietekmē datumus, kurus var ievadīt laukā **Datums**. 

3. Atlasiet **Labi**. Tiek grāmatots žurnāla ieraksts, kas atceļ atlasīto ierakstu. Atsaukšana tiek rādīta lapā **Darījumi**, un neto kopējā pašreizējā bilance tiek atjaunota uz to, kas bija pirms pirmās atcelšanas. Tāpēc ietekme, kas atsaukšanai ir uz bilancēm, tiek anulēta.

Atlasot **Atsaukšanas izsekošana**, parādās dialoglodziņš, kas rāda gan sākotnējos darījumus, gan atsauktos darījumus kopā ar saistīto numuru.

Varat arī izsekot atsaukšanu, izmantojot atbilstošo lapu **Grafiki**. **Atgriešanas** lauks ir notīrīts, bet lauks **Žurnāls grāmatots** tiek atlasīts. Turklāt lauks **Pēdējais žurnāla numurs** tiek atjaunināts ar atsaukšanas darījuma žurnāla numuru un **Žurnāla numura** lauks tiek atjaunināts ar atgriešanas žurnāla numuru.
