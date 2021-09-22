---
title: Kļūda rodas, ja izdošanas saraksta reģistrācijas laikā ir atlasīta atrašanās vieta
description: Kļūda rodas, ja izdošanas saraksta reģistrācijas laikā ir atlasīta atrašanās vieta.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef34b4fdcc572c56319f6cbf4913d822d8857595
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474968"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Kļūda rodas, ja izdošanas saraksta reģistrācijas laikā ir atlasīta atrašanās vieta

KB numurs: 4613106

## <a name="symptoms"></a>Simptomi

Šī problēma rodas, kad sistēma ir konfigurēta tā, lai automātiski rezervētu pārdošanas pasūtījumus. Ja mēģināsiet atlasīt izdošanas saraksta reģistrācijas rindas atrašanās vietu, jūs saņemat šādu kļūdas ziņojumu, kad izmantojat noliktavas vadības (WMS) rezervācijas procesus:

> Nevar atjaunināt daudzumu, izmantojot jaunas dimensijas

Šī problēma var rasties, jo norādītajā vietā nepietiek rīcībā esošo krājumu.

## <a name="resolution"></a>Novēršana

Sistēma darbojas kā paredzēts.

Scenārijos, kuros tiek izmantots noliktavas līmeņa rezervācijas process, ja rīcībā esošie krājumi netiks rezervēti visos krājumu dimensiju līmeņos un norādītajā vietā nav pietiekami daudz rīcībā esošo krājumu, ieteicams izdošanas rindā izmantot manuālo rezervēšanas procesu. Pēc tam varat izmantot funkciju *Rezervēt laidienu*, lai sadalītu zemākās rezervācijas, piemēram, atrašanās vietu, visiem pieejamajiem rīcībā esošajiem daudzumiem.
