---
title: Ierīces iestatīšana ražotnes izpildes interfeisa palaišanai
description: Ražotnes izpildes interfeiss tiek iestatīts visām ierīcēm ražotnē. Uzņēmumi parasti iestata katru ierīci atšķirīgi atkarībā no mērķa, kādam ierīce ir paredzēta. Piemēram, uzņēmumā var būt viena ierīce pieņemšanas zonā, kur darbinieki ierodas un aiziet, bet otra ražotnē, kur darbinieki pārvalda savus darbus.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution, HcmWorker, JmgProductionFloorExecutionDeviceConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0ae9ca901a7af8275db419e25a7297a77aab284e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857407"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Ierīces iestatīšana ražotnes izpildes interfeisa palaišanai

[!include [banner](../includes/banner.md)]

Ražotnes izpildes interfeiss tiek iestatīts visām ierīcēm ražotnē. Uzņēmumi parasti iestata katru ierīci atšķirīgi atkarībā no mērķa, kādam ierīce ir paredzēta. Piemēram, uzņēmumā var būt viena ierīce pieņemšanas zonā, kur darbinieki ierodas un aiziet, bet otra ražotnē, kur darbinieki pārvalda savus darbus.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Iestatīt konfigurāciju un filtrus noteiktai ierīcei

Lai uzstādītu ierīces konfigurācijas un darbu filtrus, **·** *piesakieties* lapā Ražošanas stāva izpilde, izmantojot kontu, kam ir drošības loma, kas ietver laika uzraudzības pienākumu uzturēšana. (No visām iebūvētajām drošības lomām šis pienākums ir tikai *Ražotnes uzraudzītājam*.) Pēc tam veiciet tālāk norādītās darbības.

1. Dodieties uz ierīci, ko vēlaties iestatīt, un pierakstieties programmā Microsoft Dynamics 365 Supply Chain Management kā ražotnes uzraudzītājs. (Izmantojiet kontu, kurā ietilpst *Uzturēt laika uzraudzības* pienākumu.)
1. Pārliecinieties, ka konfigurācija ir pieejama ierīcei, kuru iestatāt. Ja konfigurācija jau pastāv, tiek nodrošināta noklusējuma konfigurācija. Papildinformāciju par to, kā iestatīt konfigurāciju, skatiet tēmā [Ražotnes izpildes interfeisa konfigurēšana](production-floor-execution-configure.md).
1. Dodieties uz **Ražošanas kontrole \> Ražošanas izpilde \> Ražotnes izpilde**.

    Ja pašreizējā ierīcē vismaz vienu reizi jau ir konfigurēts ražotnes izpildes interfeiss, tiek atvērta pierakstīšanās lapa. Pretējā gadījumā tiek parādīta sveiciena lapa.

1. Pierakstīšanās lapā vai sveiciena lapā atlasiet **Konfigurēt**.
1. Atlasiet sarakstā konfigurāciju.
1. Atlasiet **Nākamais**.
1. Atlasiet vienu vai vairākus filtrus, ko lietot pašreizējai ierīcei. Šie filtri palīdzēs nodrošināt, ka ierīcē tiek parādīti tikai atbilstošie darbi. Lai iestatītu filtru, atlasiet filtra veidu, kas atver vērtību sarakstu, un pēc tam atlasiet filtrējamo vērtību. Pieejami tālāk norādītie filtri.

    - **Ražošanas vienība** — šis filtrs ir augstākā līmeņa filtrs. Parasti tas attiecas uz lielu darba apgabalu, kam ir vairākas resursu grupas un atsevišķi resursi tajā.
    - **Resursu grupa** — šis filtrs ir vidēja līmeņa filtrs. Parasti tas attiecas uz saistīto resursu kolekciju ierobežotā darbvietas apgabalā. Ja vispirms atlasāt filtru **Ražošanas vienība**, resursu grupu saraksts parāda tikai grupas no šīs vienības. Pretējā gadījumā tas parāda visas pieejamās resursu grupas.
    - **Resurss** — šis filtrs ir visspecifiskākais filtrs. Parasti tas attiecas uz noteiktu mašīnu vai citu atsevišķu resursu. Ja vispirms atlasāt filtru **Resursu grupa** un/vai **Ražošanas vienība**, resursu saraksts parāda tikai resursus no šīs grupas un/vai vienības. Pretējā gadījumā tas parāda visus pieejamos resursus.

1. Atlasiet **Labi**.
1. Tiek atvērta pierakstīšanās lapa, un ierīce ir gatava lietošanai.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Atļaut darbiniekam ignorēt noklusējuma filtrus

Varat piešķirt konkrētiem darbiniekiem atļauju mainīt filtra iestatījumus jebkurā izmantotajā ierīcē. Darbiniekiem, kam ir šī atļauja, ražotnes izpildes interfeiss nodrošina pogu **Filtrs** lapās **Visi darbi** un **Aktīvie darbi**.

> [!NOTE]
> Ja darbinieks maina filtru, jaunais filtrs tiek lietots no šā brīža turpmāk visiem lietotājiem, kas pierakstās šajā ierīcē.

Lai ļautu darbiniekam ignorēt noklusējuma darba filtrus, kas ir iestatīti ierīcei, veiciet tālāk norādītās darbības.

1. Dodieties uz **Laiks un apmeklētība \> Iestatījumi \> Laika reģistrācijas darbinieki**.
1. Atlasiet sarakstā darbinieku, lai atvērtu darbinieka lapu **Laika reģistrācijas darbinieki**.
1. Cilnē **Laika reģistrācija** iestatiet opciju **Iestatīt filtrus** uz *Jā*.

## <a name="run-the-interface-in-full-screen-mode"></a>Interfeisa palaišana pilnekrāna režīmā

Bieži vien palaidīsit ražotnes izpildes interfeisu, izmantojot ierīci, kas tiek izmantota tikai šim nolūkam. Tāpēc var būt lietderīgi palaist interfeisu pilnekrāna režīmā, neparādot nevienu navigāciju un/vai pārlūku Chrome.

- Lai paslēptu navigācijas rūti, kas tiek rādīta Supply Chain Management, pārlūka adreses joslā pievienojiet tālāk norādīto tekstu vietrāža URL beigās: `\&limitednav=true`.
- Lai paslēptu arī pārlūka adreses joslu, izmantojiet pārlūka iebūvēto pilnekrāna režīmu. (Instrukcijas skatiet pārlūka dokumentācijā.)

Attēla zemāk augšējā daļā ir parādīts, kā interfeiss izskatās pēc noklusējuma. Apakšējā daļā ir parādīts, kā tas izskatās pilnekrāna režīmā, kad navigācijas rūts ir paslēpta.

![Standarta pret pilnekrāna interfeiss.](media/pfei-full-screen.png "Standarta pret pilnekrāna interfeiss")

## <a name="extend-the-session-past-12-hours"></a>Pagarināt sesijas pēdējās 12 stundas

Pēc noklusējuma ražotnes interfeiss automātiski izrakstās, ja neviens to neizmanto 12 stundu laikā. Supply Chain Management lietotājam pēc tam ir jāpierakstās no jauna. Taču taimauta ierobežojumu var pagarināt līdz 90 dienām.

Lai pagarinātu taimauta ierobežojumu, pierakstieties programmā Supply Chain Management un dodieties uz **Sistēmas administrēšana \> Lietotāji \> Sesijas paplašinājumi**. Norādiet Supply Chain Management lietotāja kontu, kas tiek izmantots, lai pierakstītos ierīcē, un stundu skaitu, cik ilgi sesijai jāpaliek aktīvai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
