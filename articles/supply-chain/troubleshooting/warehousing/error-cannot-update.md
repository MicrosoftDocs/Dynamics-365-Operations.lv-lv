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
ms.openlocfilehash: da5905fb7ed1e890c85e891843379aa07de3279bd8972d6fc57136aa703c9ea4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762798"
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
