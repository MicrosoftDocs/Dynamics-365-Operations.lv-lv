---
title: Aizkavēšanās tolerance (negatīvās dienas)
description: Šajā tēmā ir sniegta informācija par aizkavēšanās tolerances aprēķināšanu un to, kā tā ietekmē plānotā pasūtījuma izveidi Plānošanas optimizācijā.
author: ChristianRytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cb03ccb208f19f540fefafd9964f74309736dc05
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577484"
---
# <a name="delay-tolerance-negative-days"></a>Aizkavēšanās tolerance (negatīvās dienas)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Aizkavēšanās tolerances funkcionalitāte ļauj Plānošanas optimizācijai ņemt vērā vērtību **Negatīvās dienas**, kas ir iestatīta vajadzību grupām. Tā tiek lietota, lai pagarinātu aizkavēšanās tolerances periodu, kas piemērots vispārējās plānošanas laikā. Šādā veidā var izvairīties no jaunu piegādes pasūtījumu izveidošanas, ja esošā piegāde varēs segt pieprasījumu pēc nelielas kavēšanās. Funkcionalitātes mērķis ir noteikt, vai ir lietderīgi izveidot jaunu piegādes pasūtījumu attiecīgajam pieprasījumam.

## <a name="turn-on-the-feature-in-your-system"></a>Līdzekļa ieslēgšana sistēmā

Lai padarītu aizkavēšanās tolerances funkcionalitāti pieejamu jūsu sistēmā, dodieties uz sadaļu [Līdzekļu pārvaldība](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet līdzekli *Negatīvās dienas Plānošanas optimizācijai*.

## <a name="delay-tolerance-in-planning-optimization"></a>Aizkavēšanās tolerance Plānošanas optimizācijā

Aizkavēšanās tolerance norāda dienu skaitu, papildus izpildes laikam, kuru esat gatavs gaidīt, pirms pasūtāt jaunu papildināšanu, kad jau ir plānota esošā piegāde. Aizkavēšanās tolerance tiek definēta, izmantojot kalendārās dienas, nevis darba dienas.

Vispārējās plānošanas laikā, kad sistēma aprēķina aizkavēšanās toleranci, tā ņem vērā iestatījumu **Negatīvās dienas**. Vērtību **Negatīvās dienas** var iestātīt lapā **Vajadzības grupas** vai lapā **Krājumu vajadzība**.

Sistēma saista aizkavēšanās tolerances aprēķinu ar *agrāko papildināšanas datumu*, kas ir vienāds ar šodienas datumu plus izpildes laiku. Aizkavēšanās tolerance tiek aprēķināta, izmantojot sekojošo formulu, kur *maks()* atrod lielāko no divām vērtībām:

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
