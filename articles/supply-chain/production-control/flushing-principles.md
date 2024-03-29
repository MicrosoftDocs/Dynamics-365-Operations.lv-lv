---
title: Norakstīšanas principi
description: Šajā rakstā ir aprakstīti četri tīrīšanas principi, kas tiek izmantoti izejmateriālu patēriņam.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 89fd38ea6d2c1635e9d8974ab99c2e4cdae4d6be
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266434"
---
# <a name="flushing-principles"></a>Norakstīšanas principi

[!include [banner](../includes/banner.md)]

Norakstīšanas principi atspoguļo dažādas patēriņa stratēģijas ražošanas procesos izmantojiem izejmateriāliem. Patēriņš ir process, kas materiālu atskaita no rīcībā esošajiem krājumiem un iestata patērēto materiālu vērtību uz **Nepabeigtais darbs** (NP) ražošanas pasūtījumiem un partijas pasūtījumiem. Izejmateriālus parasti patērē no vietas, kura ir konfigurēta procesam, kas patērē materiālu. Šī vieta ir pazīstama kā ražošanas ievades vieta.

Pirms materiālu patēriņa materiāli tiek pārvietoti uz ievades vietu. Tālāk esošajā attēlā ir parādīts šis process.

[![scenario4a.](./media/scenario4a.png)](./media/scenario4a.png)

1. Materiālu noliktava
2. Izejmateriālu izdošana
3. Ražošanas ievades vieta
4. Izejmateriālu patēriņš
5. Ražošanas process

Materiālu patēriņu kontrolē, ievērojot tālāk norādītos četrus norakstīšanas principus.

- Manuālā
- Sākšana
- Pabeigt
- Pieejams atrašanās vietā.

Norakstīšanas principi tiek konfigurēti noklusējuma vērtību hierarhijā. Hierarhijas sākas ar izlaisto preci, kur norakstīšanas principam ir vērtība **Sākšana**. Materiālu komplekta (MK) vai formulas rindā norakstīšanas principu no preces var ignorēt. Noklusējuma norakstīšanas princips ražošanas MK rindās vai partijas pasūtījuma formulas rindās tiek ņemts no preces vai ignorētās vērtības materiālu komplektā vai formulās.

## <a name="description-of-the-flushing-principles"></a>Norakstīšanas principu apraksts

### <a name="manual"></a>Manuālā
Manuālais norakstīšanas princips norāda, ka materiālu patēriņa reģistrācija ir manuāla darbība. Šis princips ir izmantojams, ja, piemēram, vēlaties izsekot laiku un izsekošanas nolūkos ir jāuzskaita patērēto partiju numuru vai sērijas numuru daudzums. Manuālais patēriņš tiek reģistrēts ražošanas izdošanas saraksta žurnālā. Krājumiem, kas ir iespējoti noliktavas vadības procesiem (WMS), var pielietot rokā turamu plūsmu.

### <a name="start"></a>Sākt
Sākšanas norakstīšanas princips norāda, ka materiāls tiks automātiski patērēts, kad tiks sākts ražošanas pasūtījums. Patērēto materiālu daudzums ir proporcionāls sākto materiālu daudzumam. Sākšanas norakstīšanas principu lietojot kopā ar ražošanas izpildes sistēmu, to var izmantot arī materiālu norakstīšanai, kad ir sākta operācija vai apstrādes darbs. Šis princips ir izmantojams, ja, piemēram, novirze patēriņā ir zema, materiāli ir zemas vērtības materiāli, nav izsekošanas prasību vai operācijām ir īss izpildes laiks. 

### <a name="finish"></a>Pabeigt
Pabeigšanas norakstīšanas princips norāda, ka materiāls tiks automātiski patērēts, kad būs pabeigts ražošanas pasūtījums vai operācija, kas ir iestatīta materiālu patērēšanai, būs reģistrēta kā pabeigta. Patērēto materiālu daudzums ir proporcionāls pabeigto materiālu daudzumam. Pabeigšanas norakstīšanas principu lietojot kopā ar ražošanas izpildes sistēmu, to var izmantot arī materiālu norakstīšanai, kad ir pabeigta operācija vai apstrādes darbs. Šis princips ir izmantojams tajās pašās situācijās, kurās lietojams sākšanas princips. Tomēr pabeigšanas princips ir piemērots operācijām, kurām ir garāks izpildes laiks un kurās materiālus nedrīkst iestatīt uz NP pirms operācijas pabeigšanas.

> [!NOTE]
> Nevar izmantot beigu tīrīšanas principu kopā ar plānošanas krājumiem. Tā vietā ieteicams izmantot sākt tīrīšanas principu. Plānošanas krājumiem ir ražošanas *tips* plānošanas prece, un tikai līdzproduktus un blakusprodukti var tikt ziņoti kā pabeigti partijas pasūtījumos, kas ir izveidoti plānošanas krājumiem.

### <a name="available-at-location"></a>Pieejams atrašanās vietā.
Norakstīšanas princips Pieejams atrašanās vietā norāda, ka materiāls tiks automātiski patērēts, kad tas tiks reģistrēts kā izdots ražošanai. Materiāls ir reģistrēts kā izdots no vietas, kad ir pabeigts izejmateriālu izdošanas darbs vai kad materiāls ir pieejams ražošanas ievades vietā un materiālu komplekta rinda ir izlaista nosūtīšanai uz noliktavu. Procesa laikā ģenerētais izdošanas saraksts tiek grāmatots pakešuzdevumā. Šis princips ir izmantojams, ja, piemēram, attiecībā pret vienu ražošanas pasūtījumu ir jāveic daudz izdošanas darbību. Šajā gadījumā jums nav manuāli jāatjaunina izdošanas saraksts, un jūs varat iegūt pašreizējo NP bilances skatu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
