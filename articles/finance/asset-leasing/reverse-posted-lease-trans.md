---
title: Grāmatoto nomas darījumu atsaukšana
description: Šajā rakstā ir izskaidrots, kā atsaukt grāmatotu nomas darbību. Jebkuru darījumu, kas tiek izveidots, izmantojot līdzekļu nomu, var atsaukt.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseTransactions
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4f23b6cca6ddf4da7a0232a5bc61785dbd451d55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908072"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
