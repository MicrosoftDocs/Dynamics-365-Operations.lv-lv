---
title: Aizkavēšanās tolerance (negatīvās dienas)
description: Šajā rakstā ir sniegta informācija par aizkavēšanās tolerances aprēķināšanu un to, kā tas ietekmē plānotā pasūtījuma izveidi plānošanas optimizācijā.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: fa4d2d1506546cacf5f9a7ec936f17601c5727d2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335381"
---
# <a name="delay-tolerance-negative-days"></a>Aizkavēšanās tolerance (negatīvās dienas)

[!include [banner](../../includes/banner.md)]

Aizkavēšanās tolerances funkcionalitāte ļauj veikt **optimizācijas** plānošanu, apsveriet negatīvās dienas vērtību, kas ir iestatīta vajadzību grupām, krājumu segumam un/vai vispārējām vajadzībām. Tā tiek lietota, lai pagarinātu aizkavēšanās tolerances periodu, kas piemērots vispārējās plānošanas laikā. Šādā veidā var izvairīties no jaunu piegādes pasūtījumu izveidošanas, ja esošā piegāde varēs segt pieprasījumu pēc nelielas kavēšanās. Funkcionalitātes mērķis ir noteikt, vai ir lietderīgi izveidot jaunu piegādes pasūtījumu attiecīgajam pieprasījumam.

## <a name="turn-delay-tolerance-features-on-or-off"></a>Ieslēgt vai izslēgt aizkavēšanās tolerances līdzekļus

Lai padarītu sistēmā pieejamu aizkavēšanās tolerances funkcionalitāti, dodieties uz [sadaļu](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) Līdzekļu pārvaldība un slēdziet šādas funkcijas:

- *Negatīvas dienas plānošanas optimizēšanai* — šī funkcija iespējo negatīvos dienu iestatījumus vajadzību grupām un krājumu vajadzībām. Attiecībā uz Piegādes ķēdes pārvaldības versiju 10.0.29 funkcija ir obligāta, un to nevar izslēgt.
- *Pasūtījuma piegādes automatizācija - šī funkcija* iespējo negatīvus dienu iestatījumus vispārējā plānam. (Plašāku informāciju skatiet [Pasūtījuma piegādes automatizācija](../make-to-order-supply-automation.md).)

## <a name="delay-tolerance-in-planning-optimization"></a>Aizkavēšanās tolerance Plānošanas optimizācijā

Aizkavēšanās tolerance norāda dienu skaitu, papildus izpildes laikam, kuru esat gatavs gaidīt, pirms pasūtāt jaunu papildināšanu, kad jau ir plānota esošā piegāde. Aizkavēšanās tolerance tiek definēta, izmantojot kalendārās dienas, nevis darba dienas.

Vispārējās plānošanas laikā, kad sistēma aprēķina aizkavēšanās toleranci, tā ņem vērā iestatījumu **Negatīvās dienas**. Vērtību Negatīvās dienas **var** iestatīt lapā **Vajadzības grupas**, Krājumu **vajadzības lapa** vai Vispārējo **plānu** lapa. Ja vairāk nekā vienā līmenī tiek piešķirtas negatīvas dienas, sistēma izmanto šādu hierarhiju, lai izlemtu, kuru iestatījumu izmantot:

- Ja vispārējā plāna lapā ir iespējotas negatīvās **dienas**, šis iestatījums ignorē visus pārējos negatīvos dienu iestatījumus, kad plāns tiek palaists.
- Ja lapā Krājumu vajadzība ir konfigurētas negatīvas **dienas**, šis iestatījums ignorē vajadzību grupas iestatījumu.
- Negatīvās dienas, kas ir konfigurētas **lapā** Vajadzības grupas, tiek lietotas tikai tad, ja nav konfigurētas negatīvas dienas atbilstošam krājumam vai plānam.

Sistēma saista aizkavēšanās tolerances aprēķinu ar *agrāko papildināšanas datumu*, kas ir vienāds ar šodienas datumu plus izpildes laiku. Aizkavēšanās tolerance tiek aprēķināta, izmantojot šādu formulu, kur *max()* atrod lielāko no divām vērtībām:

*maks(Agrākais papildināšanas datums, Pieprasījuma izpildes termiņš)* – *Pieprasījuma izpildes datums* + *Negatīvās dienas*

Šī formula nodrošina, ka vispārējā plānošana neveido jaunus piegādes pasūtījumus, ja preces izpildes laikā ir pietiekami daudz piegādes.

> [!NOTE]
> Aizkavēšanās tolerances aprēķins Plānošanas optimizācijā vienmēr izmanto dinamisko negatīvo dienu aprēķinu no iebūvētās vispārējās plānošanas. Iestatījums **Izmantot dinamiskās negatīvās dienas** lapā **Vispārējās plānošanas parametri** neietekmē šo uzvedību.

Ja esošais piedāvājums ietver pieprasījuma aizkavi, kas ir mazāka par vai vienāda ar aprēķināto aizkavēšanās toleranci, Plānošanas optimizācija piesaista esošo piedāvājumu ar pieprasījumu. Dažos gadījumos labāk ir novilcināt pieprasījumu, nevis panākt pārmērīgu piedāvājumu.

Tālāk minētās apakšsadaļas sniedz piemērus, kas parāda, kā aizkavēšanās tolerance ietekmē plānoto pasūtījumu izveidi Plānošanas optimizācijā.

### <a name="example-1"></a>1. piemērs

Precei ir šāda konfigurācija:

- **Izpildes laiks:** *10*
- **Negatīvās dienas:** *2*

Precei pastāv šādi piedāvājuma un pieprasījuma veidi:

- **Šodienas pieprasījums:** pārdošanas pasūtījums ar daudzumu 10
- **Piegāde 12 dienās:** pirkšanas pasūtījums ar daudzumu 10

Esošā piegāde var segt pieprasījumu 12 dienu laikā, un šis periods ir vienāds ar aizkavēšanās toleranci. Tāpēc, kad tiek palaista vispārējā plānošana, plānotie pasūtījumi netiek izveidoti.

### <a name="example-2"></a>2. piemērs

Precei ir šāda konfigurācija:

- **Izpildes laiks:** *10*
- **Negatīvās dienas:** *0*

Precei pastāv šādi piedāvājuma un pieprasījuma veidi:

- **Šodienas pieprasījums:** pārdošanas pasūtījums ar daudzumu 10
- **Piegāde 12 dienās:** pirkšanas pasūtījums ar daudzumu 10

Esošais piedāvājums var segt pieprasījumu tikai pēc 12 dienām. Tomēr aizkavēšanās tolerance ir 10 dienas. Tāpēc, kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums daudzumam 10.

### <a name="example-3"></a>3. piemērs

Precei ir šāda konfigurācija:

- **Izpildes laiks:** *10*
- **Negatīvās dienas:** *2*

Precei pastāv šādi piedāvājuma un pieprasījuma veidi:

- **Pieprasījums 11 dienās:** pārdošanas pasūtījums ar daudzumu 10
- **Piegāde 14 dienās:** pirkšanas pasūtījums ar daudzumu 10

Esošais piedāvājums var segt pieprasījumu tikai pēc trim dienām. Tomēr aizkavēšanās tolerance ir trīs dienas. (Šajā gadījumā aizkavēšanās tolerance iekļauj tikai divas negatīvās dienas. Pieprasījuma datums nav ietverts, jo tas ir pēc preces izpildes laika.) Tāpēc, kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums daudzumam 10.
